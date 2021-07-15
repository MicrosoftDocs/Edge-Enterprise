---
title: "Microsoft Edge and Configurable sites in IE mode"
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Microsoft Edge and Configurable sites in IE mode"
---

# Learn about Configurable sites in IE mode

This article explains the Configurable sites feature of the Enterprise Mode Site List when using IE mode in Microsoft Edge.

## Prerequisites

- Windows updates

  - Windows 10 version 1909, Windows server version 1909 – KB4550945  or higher
  - Windows 10 version 1903, Windows server version 1903 – KB4550945  or higher
  - Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019 - KB4550969 or higher
  - Windows 10 version 1803 – KB4550944 or higher
  - Windows 10 version 1607, Windows Server 2016 - KB4556826 or higher
  - Windows 10 initial version, July 2015 - KB4550947 or higher
  - Windows 8.1 – KB4556798 or higher

- Microsoft Edge version 83 or later
- [IE mode](./edge-ie-mode.md) configured with Enterprise Mode Site List

## Overview

Configuring sites needing IE mode in the Enterprise Mode Site List will work well for most environments with legacy applications. However, in some cases this approach isn't the best to configure a subset of sites to open in IE mode without rendering an entire domain in IE mode. For example, when your environment contains both modern and legacy applications running on a single server and you would like the flexibility to render only the legacy applications in IE mode and the remaining applications to render in Microsoft Edge mode.

The solution is to use the Configurable sites feature of the Enterprise Mode Site List. When the feature is enabled, Microsoft Edge will allow sites with the "configurable" tag to participate in IE mode engine determination.

## How Configurable sites works

### Automatic switching from the Microsoft Edge engine to the IE mode engine

To use the Configurable sites feature, you'll need one or more sites in the Enterprise Mode Site List to have the `<open-in>Configurable</open-in>` option.

Example:

```
<site-list version="1">
  <site url="app.com">
    <open-in>Configurable</open-in>
  </site>
</site-list>
```

When the Configurable sites feature is enabled, the following behavior occurs:

1. When making a request to a Configurable site, Microsoft Edge will send the HTTP request header "`X-InternetExplorerModeConfigurable: 1`".
2. A Configurable site may send a redirect response (for example, HTTP 302) with the HTTP response header "`X-InternetExplorerMode: 1`" to request that Microsoft Edge loads the site in IE mode.
3. The target of the redirect (that is, the value of the **Location** response header) must also be a **Configurable** or **Neutral** site, otherwise the IE mode response header will be ignored. It's expected that the target of the redirect will usually be the same as the original URL. However, it doesn't have to be.

   > [!NOTE]
   > The redirect response is subject to caching according to Microsoft Edge's normal HTTP caching behavior for redirects.

### Switching back from IE mode engine to Microsoft Edge engine

Enabling Configurable sites in Microsoft Edge automatically enables the following behaviors in IE mode tabs:

1. When making a request to a Configurable site, IE mode tabs will send the HTTP request header "`X-InternetExplorerModeConfigurable: 1`", the same as Microsoft Edge tabs.
2. A Configurable site might send a redirect response (for example, HTTP 302) with the HTTP response header "`X-InternetExplorerMode: 0`" to request that the navigation switch back to Microsoft Edge mode.
3. The target of the redirect (that is, the value of the **Location** response header) must also be a **Configurable** or **Neutral** site, otherwise the IE mode response header will be ignored. It's expected that the target of the redirect will usually be the same as the original URL. However, it doesn't have to be.

   > [!NOTE]
   > The redirect response is subject to caching according to Microsoft Edge's normal HTTP caching behavior for redirects.

> [!TIP]
> Both browser engines send the same "`X-InternetExplorerModeConfigurable: 1`" request header to Configurable sites. You should use the User-Agent request header to distinguish between requests from Microsoft Edge mode vs. IE mode to avoid redirecting when the site is already loading in the correct engine.

## See also

- [About IE mode](./edge-ie-mode.md)
- [Additional Enterprise Mode information](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)