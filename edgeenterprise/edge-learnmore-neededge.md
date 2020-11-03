---
title: "Redirection from Internet Explorer to Microsoft Edge for compatibility with modern web sites"
ms.author: laannade
author: dan-wesley
manager: ratetali
ms.date: 10/19/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Redirection from Internet Explorer to Microsoft Edge for compatibility with modern web sites"
---

# Redirection from Internet Explorer to Microsoft Edge for compatibility with modern web sites

> [!NOTE]
> This article applies to Microsoft Edge Stable version 87 or later.

## Overview

Many modern websites have designs that are incompatible with Internet Explorer. Whenever an Internet Explorer user visits an incompatible public site, they get a message that tells them the site is incompatible with their browser, and they need to manually switch to a different browser.

The need to  manually switch to a different browser changes starting with Microsoft Edge Stable version 87.

When a user goes to a site that is incompatible with Internet Explorer, they will be automatically redirected to Microsoft Edge. This article describes the user experience for redirection and the group policies that are used to configure or disable automatic redirection.

> [!NOTE]
> Microsoft maintains a list of all sites that are known to be incompatible with Internet Explorer.

## Redirection experience

On redirection to Microsoft Edge, users are shown the one-time dialog in the next screenshot. This dialog explains why they're getting redirected and prompts for consent to copy their browsing data and preferences from Internet Explorer to Microsoft Edge. The following browsing data will be imported: Favorites, Passwords, Search engines, open tabs, History, settings, cookies, and the Home Page.

![Browsing notification and prompt to import data and preferences.](media/edge-learnmore-neededge/neededge-dialog1.png)

Even if they don't give their consent by checking "Always bring over my browsing data and preferences from Internet Explorer", they can click **Continue browsing** to continue their session.

Finally, a website incompatibility banner, shown in the next screenshot, appears below the address bar for every redirection.

![Notification about modern sites and prompt to set Microsoft Edge as default browser or explore Microsoft Edge.](media/edge-learnmore-neededge/neededge-banner.png)

The website incompatibility banner:

- encourages the user to switch to Microsoft Edge
- offers to make Microsoft Edge as the default browser
- gives the user the option to explore Microsoft Edge

When a site is redirected from Internet Explorer to Microsoft Edge, the Internet Explorer tab that started loading the site is closed if it had no prior content. Otherwise, the active tab view goes to a  Microsoft [support](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) page that explains why the site was redirected to Microsoft Edge.

> [!NOTE]
> After a redirection users can go back to using Internet Explorer for sites that are not on the Internet Explorer incompatibility list.  

## Policies to configure redirection to Microsoft Edge

> [!NOTE]
> These policies will be available as ADMX file updates by October 26, 2020 and will be available in Intune by November 9, 2020.

Three group policies must be configured to enable automatic redirection to Microsoft Edge. These policies are:

- RedirectSitesFromInternetExplorerPreventBHOInstall
- RedirectSitesFromInternetExplorerRedirectMode
- HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

### Policy: RedirectSitesFromInternetExplorerPreventBHOInstall

Redirection from Internet Explorer to Microsoft Edge requires an Internet Explorer Browser Helper Object (BHO) named "IEtoEdge BHO". The **RedirectSitesFromInternetExplorerPreventBHOInstall** policy controls whether or not this BHO is installed.  

- If you enable this policy, the BHO required for redirection will not be installed and your users will continue to see incompatibility messages for certain websites on Internet Explorer. If the BHO is already installed, it will be uninstalled the next time the Microsoft Edge Stable channel is updated.
- If you disable or don't configure this policy, the BHO will be installed. This is the default behavior.

In addition to needing the BHO, there is a dependency on the **RedirectSitesFromInternetExplorerRedirectMode**, which needs to be set to "Redirect sites based on the incompatible sites sitelist" or "Not Configured".

### Policy: RedirectSitesFromInternetExplorerRedirectMode

 This policy corresponds to the Microsoft Edge **Default browser** setting "Let Internet Explorer open sites in Microsoft Edge". You can access this setting by going to the *edge://settings/defaultbrowser* URL.  

- If you don't configure this policy or set it to "Sitelist", Internet Explorer will redirect incompatible sites to Microsoft Edge. This is the default behavior.
- To disable this policy, select **Enabled** AND then in the dropdown under Options: Redirect incompatible sites from Internet Explorer to Microsoft Edge, select **Disable**. In this state, incompatible sites aren't redirected to Microsoft Edge.

> [!NOTE]
> If you're on a personal device that isn't  managed by your organization, you'll see another setting named "Allow sites to be loaded in Internet Explorer mode" under **Internet Explorer compatibility**.
>
>If you're on a domain joined or Mobile Device Management (MDM) enrolled device, you won't see this option.
>
> Instead, if you want to let your users load sites in Internet Explorer mode, you can do so by configuring the policy [Allow Internet Explorer mode testing](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allow-internet-explorer-mode-testing).

### Policy: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

This policy configures the user experience for incompatible site redirection to Microsoft Edge.  

- If you enable this policy, users never see the one-time redirection dialog and the redirection banner. No browser data or user preferences are imported.
- If you disable or don't configure this policy, the redirection dialog will be shown on the first redirection and the persistent redirection banner will be shown for sessions that start with a redirection.

  > [!NOTE]
  > User browsing data will be imported every time a user encounters a new redirection. However, this only happens if the user consented to the import on the one-time redirection dialog.

## Disable redirection to Microsoft Edge

If you want to disable redirection BEFORE updating to Microsoft Edge Stable version 87, use the following step:

1. Set the **RedirectSitesFromInternetExplorerPreventBHOInstall** policy to **Enabled**. 

If you want to disable redirection AFTER updating to Microsoft Edge Stable version 87, use the following steps:

1. Set the **RedirectSitesFromInternetExplorerRedirectMode** policy to **Enabled** AND then in the dropdown under Options: Redirect incompatible sites from Internet Explorer to Microsoft Edge, select **Disable**. This setting will stop redirecting as soon as the policy takes effect.
2. Set the **RedirectSitesFromInternetExplorerPreventBHOInstall** policy to **Enabled**. This will uninstall the BHO after the next Microsoft Edge update.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge Policies](https://docs.microsoft.com/deployedge/microsoft-edge-policies)
