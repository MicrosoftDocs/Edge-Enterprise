---
title: "Archived release notes for Microsoft Edge Stable Channel"
ms.author: collw
author: dan-wesley
manager: likuba
ms.date: 05/22/2023
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Archived release notes for Microsoft Edge Mobile Stable Channel"
---

# Archived release notes for Microsoft Edge Mobile Stable Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Mobile Edge Stable Channel. All the security updates are listed [here](microsoft-edge-relnotes-security.md).

<!-- Version Version 109.0.1518.58: January 18, 2023 to Version 108.0.1462.45: December 8, 2022  -->
## Version 109.0.1518.58: January 18, 2023

Fixed various bugs and performance issues for Android.

> [!NOTE]
> Release version 109 supports more than 30 policies. For more information, see [Microsoft Edge Mobile - Policies](/deployedge/microsoft-edge-mobile-policies).

## Version 108.0.1462.77: January 6, 2023

Fixed various bugs and performance issues for iOS.

## Version 108.0.1462.62: December 21, 2022

Fixed various bugs and performance issues.

## Version 108.0.1462.48: December 12, 2022

Fixed various bugs and performance issues for Android.

## Version 108.0.1462.45: December 8, 2022

Fixed various bugs for Android.

### Feature updates

- **Support Shared Device Mode (Android only).** Starting with Microsoft Edge 108 for Android, shared device mode will be supported as public preview. For more information, see [Microsoft applications that support shared device mode](/azure/active-directory/develop/msal-android-shared-devices#microsoft-applications-that-support-shared-device-mode).

## Version 108.0.1462.43: December 7, 2022

Fixed various bugs and performance issues for iOS.

## Version 107.0.1418.52: November 17, 2022

Fixed various bugs and performance issues.

## Version 107.0.1418.42: November 14, 2022

Fixed various bugs and performance issues.

## Version 107.0.1418.36: November 4, 2022

Fixed various bugs and performance issues.

## Version 107.0.1418.33: November 2, 2022

Fixed various bugs and performance issues.

## Version 107.0.1418.28: November 2, 2022

Fixed various bugs and performance issues.

## Version 106.0.1370.52: October 20, 2022

Fixed various bugs and performance issues.

## Version 106.0.1370.47: October 17, 2022

Fixed various bugs and performance issues.

## Version 105.0.1343.38: September 13, 2022

Fixed various bugs.

## Version 104.0.1293.60: August 17, 2022

> [!IMPORTANT]
> This update contains a fix for [CVE-2022-2856](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-2856), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-17-2022).

## Version 104.0.1293.58: August 16

Fixed various bugs.

### Feature updates

- **Support for disabling of inPrivate browsing and Password feature (iOS and Android).**  Before Microsoft Edge 104, Edge for iOS and Android disabled InPrivate browsing and Password (prompts to save passwords for the user) by default when only allow Work or School Accounts is configured.<br><br>
Starting with Microsoft Edge 104, you have more flexibility because InPrivate and Password won't be disabled by default when only allow Work or School Accounts is configured. Instead, you can decide whether to disable InPrivate browsing or Password by configuring the **com.microsoft.intune.mam.managedbrowser.disabledFeatures** key. For more information, see [Disable specific features](/mem/intune/apps/manage-microsoft-edge#disable-specific-features).

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
  - When a device's silent toggle is on, it doesn't affect Read Aloud playback as long as media volume is turned up.
  
