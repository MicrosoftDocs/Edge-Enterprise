---
title: "Microsoft Edge release notes for Mobile Stable Channel"
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 08/17/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Microsoft Edge release notes for Mobile Stable Channel"
---

# Release notes for Microsoft Edge Mobile Stable Channel

These release notes provide information about new features that are available to work or school accounts, and non-security updates that are included in the Microsoft Edge for Mobile Stable Channel.

To understand Microsoft Edge channels, see the [Overview of the Microsoft Edge channels](./microsoft-edge-channels.md).

All the Stable channel security updates are listed in [Release notes for Microsoft Edge Security Updates](./microsoft-edge-relnotes-security.md).

> [!NOTE]
> For the Stable Channel, updates roll out progressively over one or more days. To learn more, see [Progressive rollouts for Microsoft Edge updates](./microsoft-edge-update-progressive-rollout.md). There might be a delay before the new release is populated to the App Store (iOS) and Google Play (Android).

## Version 104.0.1293.60: August 17

> [!IMPORTANT]
> This update contains a fix for [CVE-2022-2856], which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-17-2022).

## Version 104.0.1293.58: August 16

Fixed various bugs.

### Feature updates

- **Support for disabling of inPrivate browsing and Password feature (iOS and Android).**  Before Microsoft Edge 104, Edge for iOS and Android disabled InPrivate browsing and Password (prompts to save passwords for the user) by default when only allow Work or School Accounts is configured.<br><br>
Starting with Microsoft Edge 104, you have more flexibility because InPrivate and Password won't be disabled by default when only allow Work or School Accounts is configured. Instead, you can decide whether to disable InPrivate browsing or Password by configuring the **com.microsoft.intune.mam.managedbrowser.disabledFeatures** key. For more information, see [Disable specific features](https://docs.microsoft.com/mem/intune/apps/manage-microsoft-edge#disable-specific-features).

## Version 103.1264.53: July 1

Fixed various bugs.

## Version 103.0.1264.38: June 30

Fixed various bugs.

## Version 102.0.1245.30: May 31

Fixed various bugs.

### Feature updates

- **Support switching network stack between Chromium and iOS (iOS only).** The [NetworkStackPref](/mem/intune/apps/manage-microsoft-edge#switch-network-stack-between-chromium-and-ios) policy lets you choose the network preference for Microsoft Edge for iOS.

### Policy updates

#### New policies

- [NetworkStackPref](/mem/intune/apps/manage-microsoft-edge#switch-network-stack-between-chromium-and-ios) - Choose the network preference for Microsoft Edge for iOS

## Version 101.0.1210.43: May 9

Fixed various bugs.

## Version 101.0.1210.32: April 29

Fixed various bugs.

### Feature updates

- **Read Aloud: background play and play in silent mode (iOS and Android)**
  - When playing in the background, users can control Read Aloud (pause, resume, play forwards, or play backwards) via the notification panel and lock screen.
  - When a user switches tabs in Microsoft Edge while using Read Aloud, they can use a floating control bar to pause, resume, or close Read Aloud.
  - When a device’s silent toggle is on, it doesn’t affect Read Aloud playback as long as media volume is turned up.
  
## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
