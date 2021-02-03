---
title: "Microsoft Edge kiosk transition plan"
ms.author: aguta
author: aguta
manager: srugh
ms.date: 02/02/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Create a transition plan for Microsoft Edge kiosk"
---

# Create a transition plan for a Microsoft Edge kiosk

This article provides guidance on how to transition your kiosk from Microsoft Edge Legacy to Microsoft Edge.  

> [!NOTE]
> This article applies to Microsoft Edge Stable, Beta and Dev Channels, version 87 or later.

> [!IMPORTANT]
> When support ends for Microsoft Edge Legacy on March 9, 2021, this out of support desktop application will be removed and replaced with the new release of Microsoft Edge as part of the Windows Update Tuesday (or “B”) release on April 13, 2021. Because of this, you will need to set up a new kiosk in Microsoft Edge.

## Kiosk setup options

You have two options for setting up a kiosk.

- Option 1 (Recommended): Download and install the new version of Microsoft Edge and set up kiosk mode before to applying the Windows 10 Update Tuesday (or “B”) release to your devices on or after April 13, 2021.
- Option 2: After you apply the Windows 10 Update Tuesday (or “B”) release on or after April 13, 2021, Microsoft Edge Legacy, and its kiosk, will no longer be available. You will need to set up a kiosk in Microsoft Edge to run kiosk scenarios. With this option, you will experience a disruption in your kiosk environment—which is why we strongly recommend Option 1.  

## Kiosk setup steps

Use the following steps as a guide  to set up a kiosk in Microsoft Edge.

1. Evaluate your needs against released (and upcoming) kiosk mode functionality. The 
[Kiosk mode supported features](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features) table lists the features supported by kiosk mode in Microsoft Edge and Microsoft Edge Legacy. Use this table as a guide to transitioning to Microsoft Edge by comparing how these features are supported in both releases of Microsoft Edge. For information about the Microsoft Edge release schedule, see [Microsoft Edge release schedule](microsoft-edge-release-schedule.md).
2. Test the new kiosk in Microsoft Edge. We recommend that you test setting up kiosk mode in Microsoft Edge. A quick and easy way to test kiosk mode is to configure an assigned access single app via Windows Settings as described in [Configure using Windows Settings](microsoft-edge-configure-kiosk-mode.md#configure-using-windows-settings).
3. Develop a transition plan. Based on your testing and organizational needs, we recommend developing a transition plan and moving to the new version of Microsoft Edge before to support ends for Microsoft Edge Legacy on March 9, 2021.  

## Scenarios that require you to recreate an existing kiosk

If you update to Windows 10, version 20H2, the new version of Microsoft Edge will be installed and Microsoft Edge Legacy will be hidden and not usable. If so, you will need to set up a new kiosk as we've described.

## How to get help

Kiosk mode might be an important part of your everyday business, so we want to help make this transition as smooth as possible. If your business needs help with the transition, Microsoft Edge support from Microsoft is available. Additionally, if you experience site or app compatibility issues, get no-cost help using [App Assure](https://fasttrack.microsoft.com/portal). The App Assure compatibility promise is: if your web apps or sites work on Internet Explorer 11, supported versions of Google Chrome, or any version of Microsoft Edge, they'll work with the new version of Microsoft Edge.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)