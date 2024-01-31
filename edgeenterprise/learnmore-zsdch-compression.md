---
title: "Considerations for zstd-based Shared Dictionary Compression for HTTP"
ms.author: erikan
author: dan-wesley
manager: megp
ms.date: 08/07/2022
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Enterprise considerations for zstd-based Shared Dictionary Compression for HTTP (ZSDCH) feature"
---

# Considerations for zstd-based Shared Dictionary Compression for HTTP 

This article presents Enterprise considerations for the zstd-based Shared Dictionary Compression for HTTP (ZSDCH) feature.

The infrastructure considerations largely also apply to the [Compression Dictionary Transport](https://datatracker.ietf.org/doc/draft-ietf-httpbis-compression-dictionary/) feature which has been implemented by the Chromium project. The Compressed Dictionary Transport feature is available to sites via the Origin Trial mechanism in Microsoft Edge 119 and above.

## What is ZSDCH?

ZSDCH is an experimental feature in Microsoft Edge that lets the browser use a shared dictionary to decompress responses served via HTTPS. When users visit a site (bing.com, for example) using the feature, they benefit from improved performance via reduced bandwidth requirements for the server to send the page back to the user.

The Compression Dictionary Transport feature targets the same scenarios and works in a similar manner.

## How does ZSDCH work?

ZSDCH works by having the browser send a new value, "zsdch", in the "Accept-Encoding" request header to indicate to the server that the browser supports ZSDCH compression.

If the server wants to use ZSDCH for future responses, it provides the typical response with a non-ZSDCH Content-Encoding but with an extra "get-dictionary" response header. This header provides a pointer to a location for the browser to fetch a ZSDCH dictionary for future use.

After the browser has fetched and cached the dictionary, future requests to the server will include a list of available dictionaries in a "avail-dictionary" header. If the server can serve a response compressed using one of the available dictionaries, it provides a response using the dictionary and specifies a "Content-Encoding" of "zsdch".

## How does the Compression Dictionary Transport feature work?

Similarly, when a Compression Dictionary Transport dictionary is available on the client during request time, the Compression Dictionary Transport advertises additional "Accept-Encoding" request header values ("sbr" and/or "zstd-d") along with a "Sec-Available-Dictionary" request header.

## What sites are these features being tested with?

To validate performance gains and compatibility with various network topologies, Edge advertises ZSDCH support when requesting content from bing.com, bing.cn, and msn.com. Edge also supports local testing by advertising it to servers with the "localhost" hostname.

The Compression Dictionary Transport feature is being tested by various sites, including non-Microsoft ones, using the Origin Trial mechanism.

## Potential interactions with network middleboxes

Some enterprises use network middleboxes that offer caching and/or network traffic inspection capabilities. Sometimes these products have a requirement that they can parse the response; otherwise, they may modify or block the response in a way that breaks the page.

Middleboxes that require that the Content-Encoding be an encoding that it understands must ensure they modify requests' Accept-Encoding header value to remove unsupported encodings. Otherwise, the web server may choose to offer a response that the middlebox will not be able to decode.

For caching layers that don't need to inspect the response, they must also correctly support the "Vary" header to ensure that a server response that includes the "avail-dictionary" and/or "sec-available-dictionary" header names in the "Vary" value is handled correctly and compressed responses aren't returned to clients that don't have the appropriate dictionary.

These practices are generic and would also apply to any new, future content encodings supported by browsers.

A proxy or middlebox can only interfere with the compression on a TLS connection if it's decrypting TLS traffic using a private interception certificate.

To minimize the risk to enterprise environments that don't follow the preceding best practices, Edge disables the ZDSCH feature when such a decrypting middle box is detected.

For the Compression Dictionary Transport feature, an explicit enterprise policy ([CompressionDictionaryTransportEnabled](/deployedge/microsoft-edge-policies#compressiondictionarytransportenabled)) is provided. Affected enterprises can use the policy to disable the feature while they work with vendors to update their products to properly handle new, unfamiliar content encodings.

## Verifying that ZSDCH is causing an issue in your environment

If you believe that ZSDCH is causing an undesirable issue in your environment, you can disable ZSDCH in Edge via these steps:

1. Open `edge://flags`.
1. Search for "#edge-enable-zsdch-content-encoding".
1. Set the value for the feature to "Disabled".
1. Restart Edge to have the change take effect.
1. Run the scenario that encountered an issue to determine if it still occurs or is resolved.
