---
title: "Need Microsoft Edge for compatibility with modern sites"
ms.author: laannade
author: dan-wesley
manager: ratetali
ms.date: 10/14/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Need Microsoft Edge for compatibility with modern web sites"
---

# Need Microsoft Edge for compatibility with modern web sites

The **HideInternetExplorerRedirectUXForIncompatibleSitesToMicrosoftEdgeEnabled** policy enables Internet Explorer users to continue browsing after they go to an incompatible site. Users that land on an incompatible site are automatically redirected to Microsoft Edge.

> [!NOTE]
> This article applies to Microsoft Edge version 87 or later.

## Overview

Many modern websites have designs that are incompatible with Internet Explorer. Whenever an Internet Explorer user visits an incompatible site they get a message that tells them the site is incompatible with their browser.

> [!NOTE]
> Microsoft maintains a list of all sites that are known to be incompatible with Internet Explorer.

## Microsoft Edge in action

When a user goes to site that is incompatible with Internet Explorer several things happen.

First, they're shown the one-time dialog in the next screenshot. This dialog explains why they're getting redirected and prompts for consent to copy their browsing data and preferences from Internet Explorer to Microsoft Edge. The following browsing data will be imported: Favorites, Passwords, Search engines, open tabs, History, settings, cookies, and the Home Page.  

![Browsing notification and prompt to import data and preferences.](media/edge-learnmore-neededge/neededge-dialog1.png)

Even if they don't give their consent by checking "Always bring over my browsing data and preferences from Internet Explorer", they can click **Continue browsing** to continue their session.

Finally, a website incompatibility banner, shown in the next screenshot, appears below the address bar for every redirection.

![Notification about modern sites and prompt to set Microsoft Edge as default browser or explore Microsoft Edge.](media/edge-learnmore-neededge/neededge-banner.png)

The website incompatibility banner:

- encourages the user to switch to Microsoft Edge
- offers to make Microsoft Edge as the default browser
- gives the user the option to explore Microsoft Edge

## Policies to configure redirection to Microsoft Edge

Three group policies must be configured to enable automatic redirection to Microsoft Edge. These policies are:

- RedirectSitesFromInternetExplorerPreventBHOInstall
- RedirectSitesFromInternetExplorerRedirectMode
- HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

### Policy: RedirectSitesFromInternetExplorerPreventBHOInstall

Redirection from Internet Explorer to Microsoft Edge requires an Internet Explorer Browser Helper Object (BHO) named "IEtoEdge BHO". The **RedirectSitesFromInternetExplorerPreventBHOInstall** policy controls whether or not this BHO is installed.  

- If you enable this policy, the BHO required for redirection will not be installed and your users will continue to see incompatibility messages for certain websites on Internet Explorer. If the BHO is already installed, it will be uninstalled the next time the Microsoft Edge Stable channel is updated.
- If you disable or don't configure this policy, the BHO will be installed. This is the default behavior.

In addition to needing the BHO, there is a dependency on the **RedirectSitesFromInternetExplorerRedirectMode**, which needs to be set to "Sitelist" or "Not Configured".

### Policy: RedirectSitesFromInternetExplorerRedirectMode

 This policy corresponds to the Microsoft Edge **Default browser** setting "Let Internet Explorer open sites in Microsoft Edge". You can access this setting by going to the *edge://settings/defaultbrowser* URL.  

- If you don't configure this policy or set it to "Sitelist", Internet Explorer will redirect incompatible sites to Microsoft Edge. This is the default behavior.
- If you disable this policy, incompatible sites aren't redirected to Microsoft Edge.

### Policy: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

This policy configures the user experience for incompatible site redirection to Microsoft Edge.  

- If you enable this policy, users never see the one-time redirection dialog and the redirection banner. No browser data or user preferences are imported.
- If you disable or don't configure this policy, the redirection dialog will be shown on the first redirection and the persistent redirection banner will be shown for sessions that start with a redirection.

  > [!NOTE]
  > User browsing data will be imported every time a user encounters a new redirection. However, this only happens if the user consented to the import on the one-time redirection dialog.

## Disable redirection to Microsoft Edge

Use the following steps to disable redirection for your users.

1. Set the **RedirectSitesFromInternetExplorerRedirectMode** policy to **Disabled**. This setting will stop redirecting as soon as the policy takes effect.
2. Set the **RedirectSitesFromInternetExplorerPreventBHOInstall** policy to **Enabled**. This setting will take effect after the next Microsoft Edge Stable channel update is installed.
3. Set the **HideInternetExplorerRedirectUXForIncompatibleSitesEnabled** policy to **Enabled**.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge Policies](https://docs.microsoft.com/deployedge/microsoft-edge-policies)