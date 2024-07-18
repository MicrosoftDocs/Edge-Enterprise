---
title: "Local site list for Internet Explorer (IE) mode"
ms.author: shisub
author: dan-wesley
manager: archandr
ms.date: 07/18/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Learn how to enable local site lists and configure easy access to IE mode"
---

# Configure local site list for Internet Explorer (IE) mode

This article explains how to configure easy access to Internet Explorer mode (IE mode) and allow the use of local site lists in your organization.

## Prerequisites

1. Windows updates

   - Windows 11

   - Windows 10, version 1809; Windows Server 2019 - [KB5015880](https://support.microsoft.com/en-us/topic/july-21-2022-kb5015880-os-build-17763-3232-preview-1c984723-cdf0-4a24-9a4f-5df11d3024a1) or later

   - Windows 10, version 1909 - [KB5003974](https://support.microsoft.com/topic/kb5003974-servicing-stack-update-for-windows-10-version-1909-june-15-2021-0e65680e-2d21-4a31-b97a-e24c022aeccf) and [KB5003698](https://support.microsoft.com/topic/june-15-2021-kb5003698-os-build-18363-1645-preview-1ecf117e-1f89-40f9-a0a5-ed5766737620) or later

   - Windows 10, version 2004; Windows 10, version 20H2 and Windows 10, version 21H - [KB5005260](https://support.microsoft.com/topic/kb5005260-servicing-stack-update-for-windows-10-version-2004-20h2-and-21h1-august-10-2021-ec4c5daa-2cec-4b06-be93-037f150fe3ba) and [KB5005101](https://support.microsoft.com/topic/september-1-2021-kb5005101-os-builds-19041-1202-19042-1202-and-19043-1202-preview-82a50f27-a56f-4212-96ce-1554e8058dc1) or later
   
   - Windows Server 2016 - [KB5022838](https://support.microsoft.com/en-us/topic/february-14-2023-kb5022838-os-build-14393-5717-1b9a609e-7ae7-4102-bad5-5994eddf154b) or later

2. Microsoft Edge version 92 (92.0.902.55 or later)

## Overview

IE mode is powered by the configuration of the Enterprise Mode Site List. While you're identifying and configuring sites on the site list to use IE mode, your users no longer need to wait or fall back to the standalone IE11 application.

Starting with Microsoft Edge version 92, repeated access to *unconfigured* IE mode sites is easier. Users can reload sites in IE mode. They can add these sites to their local site list to automatically render in IE mode for 30 days, while the organization's site list gets updated. When [IE11 is disabled](/deployedge/edge-ie-disable-ie11) in your environment, your users are no longer solely dependent on the organization's site list.

You can configure this experience through group policies for your organization.

> [!NOTE]
> An *unconfigured* site is one that requires IE mode but isn't configured to open in IE mode in the Enterprise Mode Site List.

## Enable the local site list experience

To enable the local site list experience, users can go to the URL *edge://settings/defaultBrowser* and set **Allow sites to be reloaded in Internet Explorer mode** to **Allow**.

:::image type="content" source="media/Edge-hybrid-IE-mode/internet-explorer-compatibilitiy.png" alt-text="Internet Explorer Compatibility":::

>[!Note]  
>
>1. If you have enabled IE mode testing through the *InternetExplorerIntegrationTestingAllowed* policy, you will see this setting, but it will be greyed out unless you  explicitly enable the *InternetExplorerIntegrationReloadInIEModeAllowed* policy.
>
>2. If **Allow sites to be reloaded in Internet Explorer mode** is set to **Default**, users might be able to reload sites in IE mode if they have existing Internet Explorer 11 usage.  

When this setting is enabled, users can reload a site in IE mode by selecting **Settings and more (the ellipses icon ...) > Reload in Internet Explorer mode**. Users can also select **Reload tab in Internet Explorer mode** when they right-click on a tab or choose **Open link in new Internet Explorer mode tab** when they right-click on a link.

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-screenshot.png" alt-text="Reload in Internet Explorer Mode":::

The **Reload in Internet Explorer mode** icon can be pinned to the toolbar. The toolbar button allows users to easily enter and exit IE mode and can be managed through the *edge://settings/appearance* URL.

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-icon-screenshot.png" alt-text="Reload in Internet Explorer Mode icon":::

>[!Note]
>If the user is on a site that's already in the organization's Enterprise Mode Site List, options to Reload in (or Exit) Internet Explorer mode will be visible but greyed out.

When the option is selected, the site reloads in IE mode. The IE mode indicator icon is visible to the left of the address bar. The flyout shows an option that users can toggle to **Open the page in Compatibility view** which adds the page to the Internet Explorer Compatibility view settings list and refreshes the page. Also, there's an option that users can toggle to **Open the page in Internet Explorer mode** next time. This adds the specific page the user is on to the local site list and will automatically open in IE mode for the next 30 days.

:::image type="content" source="media/Edge-hybrid-IE-mode/site-has-been-reloaded-in-ie-mode-screenshot2.png" alt-text="This page is open in Internet Explorer Mode":::

After a site has been reloaded in IE mode, "in-page" navigation will stay in IE mode (for example, a link, script, a form on the page, or a server-side redirect from another "in-page" navigation).  

While in IE mode, users will see a banner indicating they are in IE mode, the option to Leave IE mode,, and to pin the IE mode icon to the toolbar (if it isn't pinned already).

:::image type="content" source="media/Edge-hybrid-IE-mode/ie-mode-banner-screenshot.png" alt-text="IE Mode Banner":::

Users can choose to exit from IE mode using the Leave button on the banner, the pinned IE mode icon or **Settings and more (the ellipses icon ...) > Exit Internet Explorer mode**, otherwise Microsoft Edge will automatically exit from IE mode when a navigation that isn't "in-page" occurs (for example, using the address bar, the back button, or a favorite link).

Entries remain on the local site list for a default period of 30 days. We recommend you configure legacy sites for your organization in the Enterprise Mode Site List. The local site list will ensure that users can continue their workflow without being interrupted while the organization's site list gets updated. On day 31, when users navigate to the site, they'll see a banner explaining that the site will no longer load in IE mode. Users can add it back to the local site list if they so choose.

:::image type="content" source="media/Edge-hybrid-IE-mode/page-will-no-longer-load-in-ie-mode-screenshot.png" alt-text="Page will no longer load in IE mode":::

## Policies to configure the use of local site lists for IE mode

Two group policies are available to configure the local site list experience in Microsoft Edge. These policies are:

### Policy: InternetExplorerIntegrationReloadInIEModeAllowed

This policy corresponds to the Microsoft Edge setting "Allow sites to be reloaded in Internet Explorer mode". You can access this setting by going to the *edge://settings/defaultbrowser* URL.

- If you enable this policy, users can reload a site in IE mode by selecting **Settings and more (the ellipses icon ... > Reload in Internet Explorer mode**. Users can also select **Reload tab in Internet Explorer mode** when they right-click on a tab, or choose **Open link in new Internet Explorer mode tab** when they right click on a link.
Users can optionally tell Microsoft Edge to use IE mode for the site in the future. This choice will be remembered for a default of 30 days and can be managed using the policy *InternetExplorerIntegrationLocalSiteListExpirationDays*.

- If you disable this policy, users won't be allowed to reload an unconfigured site in IE mode.

- If you don't configure this policy, we'll show users options to reload unconfigured sites in IE mode depending on recent Internet Explorer 11 usage.

Note that this policy takes precedence over how you configured the [InternetExplorerIntegrationTestingAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) policy and that policy will be disabled.

### Policy: InternetExplorerIntegrationLocalSiteListExpirationDays

This policy can be used to adjust the number of days that a site remains on the local site list for users.  

- If you disable or don't configure this policy, a default value of 30 days is used.

- If you enable the policy, you must enter a value between 0-90 days to keep the site on a user's local site list.

This policy has no effect if you disabled the *InternetExplorerIntegrationReloadInIEModeAllowed* policy.

> [!NOTE]
> The local site list currently doesn't sync across devices. This improvement is currently in our backlog and we'll update this feature when it's available.

## See Also

- Disable Internet Explorer 11 - [Disable Internet Explorer 11](/deployedge/edge-ie-disable-ie11)
- Configure IE mode policies - [Configure IE mode Policies](/deployedge/edge-ie-mode-policies)
