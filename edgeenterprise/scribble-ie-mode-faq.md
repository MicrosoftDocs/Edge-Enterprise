---
title: "Scratch pad for IE mode FAQ"
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 12/09/2021
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

### How do I force a site to open in Internet Explorer 11?

Internet Explorer 11 is being retired, and Microsoft Edge is the answer for accessing legacy and modern websites. If a legacy website doesn’t render or work correctly in Microsoft Edge, you can use the IE mode feature in Microsoft Edge.

You can force a website to load in IE 11 by using the reload in IE mode feature. For more information, see  [Enable the local site list experience](/deployedge/edge-ie-mode-local-site-list#enable-the-local-site-list-experience).

### How do I force a site to open in Microsoft Edge?

If Microsoft Edge is the default browser (configured by either via policy or manually), then all websites should open in Microsoft Edge unless a site is listed in the compatibility list.

If a website still loads in Internet Explorer 11 and if you don’t need Internet Explorer 11, you can disable it. For more information, see [Disable Internet Explorer 11](/deployedge/edge-ie-disable-ie11).

If a website happens to load in IE mode in Microsoft Edge, it’s because of an IE mode policy or a manual configuration that’s forcing Microsoft Edge to load the site in IE mode. Make sure you check the site in question to verify that it’s not in the IE Site list or in IE mode. You can do that by running [IE mode diagnostics](/deployedge/edge-ie-mode-faq#get-general-diagnostic-and-configuration-information). Explore our [troubleshooting guide](/deployedge/edge-ie-mode-faq) to identify and fix any other issues.

## Things that don't work

### You're unable to configure IE mode feature in Microsoft Edge

Verify you,ve followed the [prerequisites](/deployedge/edge-ie-mode#prerequisites) for IE mode, which includes enabling Internet Explorer 11 in Windows features. For more information, see  the [Microsoft Edge + Internet Explorer mode](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWEHMs) Getting Started guide and [Internet Explorer (IE) mode troubleshooting and FAQ](/deployedge/edge-ie-mode-faq).

### The "Reload in Internet Explorer mode" option is missing

This feature is available on Microsoft Edge version 92 or later. For this option to be available, you need to configure "Allow sites to be reloaded in Internet Explorer mode settings" in Microsoft Edge to "Allow".  For more information, see [Enable the local site list experience](/deployedge/edge-ie-mode-local-site-list#enable-the-local-site-list-experience).

### Pop-ups or redirected websites aren’t loading in IE mode or in Internet Explorer 11

Even after configuring IE mode, certain websites, especially websites that create a new window or a site that gets redirected may not render in IE mode or open in Internet Explorer 11.

For this kind of redirected website, you can make use of the `allow-redirect="true"` in the site list configuration. For more information, see [Updated schema elements](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance#updated-schema-elements).

### Websites aren’t loading in IE mode when you launch Microsoft Edge for the first time

Microsoft Edge needs to download the IE mode site list before it can apply IE mode settings. This process may not finish when the browser is starts. We have a policy that can force the loading of the site list before a website is loaded. For more information, see the [DelayNavigationsForInitialSiteListDownload](/deployedge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload) policy.

### You’re unable to open files or pages that are located using file:// URLs in Microsoft Edge

This issue is because of a Chromium security restriction as described in [Restrictions on File Urls](https://textslashplain.com/2019/10/09/navigating-to-file-urls/). However, you can use Microsoft Edge’s IE mode feature to load web pages hosted on the **file://** protocol within an intranet zone. You can use of the [IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled) group policy to enable this functionality.

### Certain web pages open in Internet Explorer 11 instead of opening in Microsoft Edge

If Microsoft Edge is the default browser, then all websites should open in Microsoft Edge unless the site is listed in the compatibility list.

> [!NOTE]
> For more information about making Microsoft Edge the default browser, see [Set Microsoft Edge as the default browser](/deployedge/edge-default-browser) and [Change your default browser in Windows 10](/windows/change-your-default-browser-in-windows-10-020c58c6-7d77-797a-b74e-8f07946c5db6).

If a website is still loads in Internet Explorer 11 and if you don’t this need this browser version, you can disable IE 11. For more information, see [Disable Internet Explorer 11](/deployedge/edge-ie-disable-ie11).

You can use IE mode in Microsoft Edge to force the rendering of an IE 11 compatible web page in Microsoft Edge. You can force a site to load in IE mode either by configuring IE mode policies or by using the reload in IE mode feature. For more information, see [Configure IE mode policies](/deployedge/edge-ie-mode-policies) and [Enable the local site list experience](/deployedge/edge-ie-mode-local-site-list#enable-the-local-site-list-experience).

Sometimes a proxy configuration such as Internet Explorer’s AutoConfig URL settings can cause issues. Try removing these proxy settings and test to see if the issue is fixed. For more information, see [Auto configuration settings for Internet Explorer 11](/internet-explorer/ie11-deploy-guide/auto-configuration-settings-for-ie11).

### You’re unable to download files from certain websites when running Microsoft Edge

Certain legacy websites may experience download issues when browsing in Microsoft Edge. These websites need to load in IE mode.

### Child windows running in IE mode in Microsoft Edge may experience rendering issues like text wrapping, and content getting cut off

The content area of a child window rendering in IE mode in Microsoft Edge is slightly different than what it is on Internet Explorer 11. If a web page has been designed with pixel-based alignments or positioning, you may experience incorrect rendering, text wrapping, and so on.

Two policy settings were added to Microsoft Edge from version 95 that let you specify custom adjustments to the height and width of pop-up windows generated from IE mode sites via the window.open method. You can use the following policies to adjust window size:

- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/deployedge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment)
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/deployedge/microsoft-edge-policies#internetexplorerintegrationwindowopenwidthadjustment)

### You may receive multiple authentication prompts when running a page in IE mode on Microsoft Edge

The client certificate may be requested twice in IE mode. The first time around, the certificate selection dialog will be displayed in IE mode, and the second time around, the dialog will be displayed in Microsoft Edge. This behavior is a design limitation that requires both the frame process and the window process to request authentication.

After the favicon cache is created, you won't be asked for a client certificate again unless you delete the cache. Alternatively, you can set a rule in your server configuration, such as IIS, not to require a client certificate for the favicon.

### "File > New session" isn’t available in Microsoft Edge

Microsoft Edge doesn’t have the **File > New session** feature of Internet Explorer. We don’t have any plans to replicate this feature. However, you can make use of our Profile features and create multiple profiles so you can start a new session with another account.

<!--- begin error messages --->
## Error messages

### Getting “The connection for this site is not secure” message when visiting certain sites with Microsoft Edge

This may happen if you are trying to open a legacy website in IE mode and the site is configured to run in TLS 1.0 or TLS 1.1, which are disabled by default in Microsoft Edge. For more information, see [Plan for change: TLS 1.0 and TLS 1.1 soon to be disabled by default](https://blogs.windows.com/msedgedev/2020/03/31/tls-1-0-tls-1-1-schedule-update-edge-ie11/)

### You receive the following error message: "Could not retrieve EMIE site list."

You might see this error on the *edge://compat/enterprise* page indicating that the site list download failed. This error could be caused by a syntax error in the Site list XML file.

### You receive the following error message “Error: 'This form cannot be opened in a web browser. To open this form, use Microsoft InfoPath'”

Certain applications may require you to run the web page in IE mode. You can use the IE mode feature in  Microsoft Edge.

You can force a website to load in IE 11 by either configuring IE mode policies or use the reload in IE mode feature.

You may also need to set the `compat-mode` attribute in Enterprise Mode Site List to **Default**. For more information, see [Enterprise Mode and the Enterprise Mode Site List](/internet-explorer/ie11-deploy-guide/what-is-enterprise-mode#enterprise-mode-and-the-enterprise-mode-site-list-1)

> [!TIP]
> Your users can easily view this site list and the compatibility mode by typing **about:compat** in IE 11 or Microsoft Edge.

<!-- end error messages ---->
