---
title: "Considerations for zstd-based Shared Dictionary Compression for HTTP"
ms.author: erikan
author: dan-wesley
manager: megp
ms.date: 08/03/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Enterprise considerations for zstd-based Shared Dictionary Compression for HTTP (ZSDCH) feature"
---

# Considerations for zstd-based Shared Dictionary Compression for HTTP 

This article presents Enterprise considerations for the zstd-based Shared Dictionary Compression for HTTP (ZSDCH) feature.

## What is ZSDCH?

ZSDCH is an experimental feature in Microsoft Edge that lets the browser use a shared dictionary to decompress responses served via HTTPS. When users visit a site (bing.com, for example) using the feature, they benefit from improved performance via reduced bandwidth requirements for the server to send the page back to the user.

## How does ZSDCH work?

ZSDCH works by having the browser send a new value, "zsdch", in the "Accept-Encoding" request header to indicate to the server that the browser supports ZSDCH compression.

If the server wants to use ZSDCH for future responses, it provides the typical response with a non-ZSDCH Content-Encoding but with an extra "get-dictionary" response header. This header provides a pointer to a location for the browser to fetch a ZSDCH dictionary for future use.

After the browser has fetched and cached the dictionary, future requests to the server will include a list of available dictionaries in a "avail-dictionary" header. If the server can serve a response compressed using one of the available dictionaries, provides a response using the dictionary and specifies a "Content-Encoding" of "zsdch".

## What sites are this feature being tested with?

To validate performance gains and compatibility with various network topologies, Edge advertises support when requesting content from bing.com, bing.cn, and msn.com. Edge also supports local testing by advertising it to servers with the "localhost" hostname.

## Potential interactions with network middleboxes

Some enterprises use network middleboxes that offer caching and/or network traffic inspection capabilities. Sometimes these products have a requirement that they can parse the response; otherwise, they may modify or block the response in a way that breaks the page.

Middleboxes that require that the Content-Encoding be an encoding that it understands must ensure they modify requests' Content-Encoding header value to remove unsupported encodings. Otherwise, the web server may choose to offer a response that the middlebox will not be able to decode.

For caching layers that don't need to inspect the response, they must also correctly support the "Vary" header to ensure that a server that responds with "Vary: Accept-Encoding, avail-dictionary" is handled correctly and compressed responses aren't returned to clients that don't have the appropriate dictionary.

To minimize the risk to enterprise environments that don't follow the preceding best practices, Edge disables the feature by default for enterprise-managed devices. These practices are generic and would also apply to any new, future content encodings supported by browsers.

A proxy or middlebox can only interfere with ZSDCH compression on a TLS connection if it's decrypting TLS traffic using a private interception certificate. A future change to Edge will safely enable the feature for managed devices by detecting this case and disabling ZSDCH in these scenarios.

Since a break-and-inspect middlebox can ensure appropriate Content-Encoding header values are sent, a future change in Edge might remove the heuristic to disable ZSDCH in those settings. If undesirable interactions are found, enterprises are required to ask their vendors to update their products to properly handle new, unfamiliar content encodings.

## Verifying that ZSDCH is causing an issue in your environment

If you believe that ZSDCH is causing an undesirable issue in your environment, you can disable ZSDCH in Edge via these steps:

1. Open `edge://flags`.
1. Search for "#edge-enable-zsdch-content-encoding".
1. Set the value for the feature to "Disabled".
1. Restart Edge to have the change take effect.
1. Run the scenario that encountered an issue to determine if it still occurs or is resolved.
