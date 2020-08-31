---
title: "Microsoft Edge proxy settings"
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Use command-line options to configure proxy settings "
---

# How to use Microsoft Edge command-line options to configure proxy settings

This article describes how you can use command-line options to override the default system network settings.

>[!NOTE]
>This article applies to Microsoft Edge version 77 or later.

## System network settings

The Microsoft Edge network stack uses the system network settings by default. These settings include *proxy settings*, and *certificate and private key stores*.

There are scenarios where users request an alternative to using the system's default proxy settings. To support these scenarios, Microsoft Edge supports command-line options that you can use to configure custom proxy settings.

These command-line options correspond to the following policies in the **Proxy server** group:

- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist)
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode)
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl)
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver)
- [ProxySettings](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxysettings)

## Command-line options for proxy settings

Microsoft Edge supports the following proxy-related command-line options.

 **`--no-proxy-server`**
 
Tells Microsoft Edge not to use a Proxy, even if the system is otherwise configured to use one. It overrides any other proxy settings that are provided.

**`--proxy-auto-detect`**

Tells Microsoft Edge to try and automatically detect your proxy configuration. This argument is ignored if `--proxy-server` is configured.

**`--proxy-server=<scheme>=<uri>[:<port>][;...] | <uri>[:<port>] | "direct://"`**

Tells Microsoft Edge to use a custom proxy configuration. You can specify a custom proxy configuration in three ways.

1. Provide a semicolon-separated mapping of list scheme to url/port pairs. For example, `--proxy-server="http=proxy1:8080;ftp=ftpproxy"` tells Microsoft Edge to use HTTP proxy "proxy1:8080" for http URLs and HTTP proxy "ftpproxy:80" for ftp URLs.
2. By providing a single uri with optional port to use for all URLs. For example, `--proxy-server="proxy2:8080"` will use the proxy at "proxy2:8080" for all traffic.
3. By using the special "direct://" value. For example, `--proxy-server="direct://"` will make all connections not use a proxy. 

>[!NOTE]
>You can configure Microsoft Edge to try using a proxy and fallback to going direct if the proxy isn't available. For example, `--proxy-server="http://proxy2:8080,direct://`.

**`--proxy-bypass-list=(<trailing_domain>|<ip-address>)[:<port>][;...]`**

Tells Microsoft Edge to bypass any specified proxy for the specified semicolon-separated list of hosts. This flag must be used with `--proxy-server`.

>[!NOTE]
>Trailing-domain matching doesn't require "." separators, "\*microsoft.com" will match "imicrosoft.com". For example, `--proxy-server="proxy2:8080" --proxy-bypass-list="\*.microsoft.com;\*example.com;127.0.0.1:8080"` will use the proxy server "proxy2" on port 8080 for all hosts except requests for \*.microsoft.com, example.com, and 127.0.0.1 on port 8080. In the previous example, imicrosoft.com requests will still be proxied. However, iexample.com requests will bypass the proxy because \*example.com was specified instead of \*.example.com.

**`--proxy-pac-url=<pac-file-url>`**

Tells Microsoft Edge to use the PAC file at the specified URL. For example, `--proxy-pac-url="https://wpad/proxy.pac"` tells Microsoft Edge to resolve proxy information for URL requests using the **proxy.pac** file.

## Content license

> [!NOTE]
> Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms 
  described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/). The original page can be found [here](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## See also

- To see advanced configuration settings and additional options, consult the [proxy documentation](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md) in the Chromium Open Source project.
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
