---
title: "Scratch pad for IE mode FAQ"
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 01/05/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Scratch pad for Microsoft Edge Internet Explorer mode"
---

# Scratch pad for Internet Explorer (IE) mode FAQ

This article provides customer FAQs for Microsoft Edge IE mode.

## Frequently Asked Questions

### Where can I find the "Reload in Internet Explorer mode" option?

This feature is available on Microsoft Edge version 92 or later. For this option to be available, you need to configure "Allow sites to be reloaded in Internet Explorer mode settings" in Microsoft Edge to "Allow".  For more information, see [Enable the local site list experience](/deployedge/edge-ie-mode-local-site-list#enable-the-local-site-list-experience).

### Why aren't pop-ups or redirected websites loading in IE mode or in Internet Explorer 11?

After configuring IE mode, certain websites, especially websites that create a new window or a site that gets redirected may not render in IE mode or open in Internet Explorer 11.

For this kind of redirected website, you can make use of the `allow-redirect="true"` in the site list configuration. For more information, see [Updated schema elements](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance#updated-schema-elements).

### Why aren't websites loading in IE mode when I launch Microsoft Edge for the first time?

Microsoft Edge needs to download the IE mode site list before it can apply IE mode settings. This process may not finish when the browser is starts. We have a policy that can force the loading of the site list before a website is loaded. For more information, see the [DelayNavigationsForInitialSiteListDownload](/deployedge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload) policy.

### Why can't I open files or pages that are found by using file:// URLs in Microsoft Edge?

This issue is because of a Chromium security restriction as described in [Restrictions on File Urls](https://textslashplain.com/2019/10/09/navigating-to-file-urls/). However, you can use Microsoft Edge’s IE mode feature to load web pages hosted on the **file://** protocol within an intranet zone. You can use of the [IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled) group policy to enable this functionality.

### Why are there rendering issues like text wrapping and content truncation when child windows are running in IE mode in Microsoft Edge?

The content area of a child window that renders in IE mode in Microsoft Edge is slightly different than what it is on Internet Explorer 11. If a web page has been designed with pixel-based alignments or positioning, you may experience incorrect rendering, text wrapping, and so on.

Two policy settings were added to Microsoft Edge version 95 that let you specify custom adjustments to the height and width of pop-up windows that are generated from IE mode sites via the `window.open` method. You can use the following policies to adjust window size:

- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/deployedge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) - This setting lets you specify a custom adjustment to the height of popup windows generated from the Internet Explorer mode site.
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/deployedge/microsoft-edge-policies#internetexplorerintegrationwindowopenwidthadjustment) - This setting lets you specify a custom adjustment to the width of popup windows generated from the Internet Explorer mode site.

### Why am I getting multiple authentication prompts when running a page in IE mode on Microsoft Edge?

The client certificate may be requested twice in IE mode. The first time around, the certificate selection dialog will be displayed in IE mode, and the second time around, the dialog will be displayed in Microsoft Edge. Both the the frame process and the window process need to request authentication.

After the favicon cache is created, you won't be asked for a client certificate again unless you delete the cache. Alternatively, you can set a rule in your server configuration, such as IIS, not to require a client certificate for the favicon.

### Why isn't "File > New session" available in Microsoft Edge?

Microsoft Edge doesn’t have the **File** > **New session** feature of Internet Explorer. We don’t have any plans to replicate this feature. However, you can make use of our Profile features and create multiple profiles so you can start a new session with another account.

<!--- begin error messages --->
## Error messages

### Error: “The connection for this site is not secure”

This error may happen if you're trying to open a legacy website in IE mode and the site's configured to run in TLS 1.0 or TLS 1.1, which are disabled by default in Microsoft Edge. For more information, see [Plan for change: TLS 1.0 and TLS 1.1 soon to be disabled by default](https://blogs.windows.com/msedgedev/2020/03/31/tls-1-0-tls-1-1-schedule-update-edge-ie11/)

### Error: “This form cannot be opened in a web browser. To open this form, use Microsoft InfoPath”

Certain applications may require you to load the web page in IE mode. You can use the IE mode feature in  Microsoft Edge.

You may also have to set the `compat-mode` attribute in Enterprise Mode Site List to **Default**. For more information, see [Enterprise Mode and the Enterprise Mode Site List](/internet-explorer/ie11-deploy-guide/what-is-enterprise-mode#enterprise-mode-and-the-enterprise-mode-site-list-1).

> [!TIP]
> Your users can easily view this site list and the compatibility mode by typing **about:compat** in Microsoft Edge.

<!-- end error messages ---->
