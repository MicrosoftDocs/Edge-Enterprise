---
title: "Need Microsoft Edge for compatibility with modern sites"
ms.author: laannade
author: dan-wesley
manager: ratetali
ms.date: 10/12/2020
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
- gives the user the option to explore Microsoft Edge.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)