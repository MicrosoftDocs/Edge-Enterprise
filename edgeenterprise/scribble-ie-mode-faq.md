---
title: "Scratch pad for IE mode FAQ"
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/10/2021
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

Internet Explorer 11 is being retired, and Microsoft Edge is the answer for accessing legacy and modern websites. If a legacy website doesn’t render or work correctly in Microsoft Edge you can use the IE mode feature in Microsoft Edge.

You can force a website to load in IE 11 by using the reload in IE mode feature. For more information, see  [Enable the local site list experience](https://docs.microsoft.com/en-us/deployedge/edge-ie-mode-local-site-list#enable-the-local-site-list-experience).

### How do I force a site to open in Microsoft Edge?

If you have Microsoft Edge installed and if it’s the default browser (configured by either via policy or manually), then all websites should open in Microsoft Edge unless a site is listed in the compatibility list.

If a website still loads in Internet Explorer 11 and if you don’t need Internet Explorer 11, you can disable it. For more information, see [Disable Internet Explorer 11](https://docs.microsoft.com/en-us/deployedge/edge-ie-disable-ie11).

If a website happens to load in IE mode in Microsoft Edge it’s because of an IE mode policy or a manual configuration that’s forcing Microsoft Edge to load the site in IE mode. Make sure you check the site in question to verify that it’s not in the IE Site list or in IE mode. You can do that by running [IE mode diagnostics](/deployedge/edge-ie-mode-faq#get-general-diagnostic-and-configuration-information). Explore our [troubleshooting guide](/deployedge/edge-ie-mode-faq) to identify and fix any other issues.

## Things that don't work

### You're unable to configure IE mode feature in Microsoft Edge

Verify you have followed the [prerequisites](/deployedge/edge-ie-mode#prerequisites) for IE mode, which includes enabling Internet Explorer 11 in Windows features. For more information, see  the [Microsoft Edge + Internet Explorer mode](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWEHMs) Getting Started guide and [Internet Explorer (IE) mode troubleshooting and FAQ](/deployedge/edge-ie-mode-faq).

### The "Reload in Internet Explorer mode" option is missing.

This feature is available on Microsoft Edge version 92 or later. For this option to be available, you need to configure "Allow sites to be reloaded in Internet Explorer mode settings" in Microsoft Edge to "Allow".  For more information, see [Enable the local site list experience](https://docs.microsoft.com/en-us/deployedge/edge-ie-mode-local-site-list#enable-the-local-site-list-experience).

### Pop-ups or redirected websites aren’t loading in IE mode or in Internet Explorer 11

Even after configuring IE mode, certain websites, especially websites that spawn a new window or a site that gets redirected may not render in IE mode or open in Internet Explorer 11.

For this kind of redirected website you can make use of the `allow-redirect="true"` in the site list configuration. For more information, see [Updated schema elements](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance#updated-schema-elements).

### Websites aren’t loading in IE mode when you launch Microsoft Edge for the first time

Microsoft Edge needs to download the IE mode site list before it can apply IE mode settings. This process may not finish when the browser is starts. We have a policy that can force the loading of the site list before a website is loaded. For more information, see the[DelayNavigationsForInitialSiteListDownload](/deployedge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload) policy.

## Error messages



## General best practices and requirements for IE mode and managing compatibility for Internet Explorer in Microsoft Edge

We recommend that you:

- Install the latest version of Microsoft Edge. See the Stable channel release notes (https://docs.microsoft.com/en-us/deployedge/microsoft-edge-relnote-stable-channel) 
- Follow the guidance in the getting started guide. See [Microsoft Edge + Internet Explorer mode Getting Started guide](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWEHMs) 
- Learn about IE mode. See [What is Internet Explorer (IE) mode?](https://docs.microsoft.com/en-us/deployedge/edge-ie-mode)
- Examined the trouble shooting guidance. See [Internet Explorer (IE) mode troubleshooting and FAQ](https://docs.microsoft.com/en-us/deployedge/edge-ie-mode-faq).
