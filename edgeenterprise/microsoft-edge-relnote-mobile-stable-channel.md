---
title: "Microsoft Edge release notes for Mobile Stable Channel"
ms.author: charlielin
author: dan-wesley
manager: alexyuan
ms.date: 08/10/2023
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

## Version 115.0.1901.183: July 21, 2023

Fixed various bugs and performance issues for Android.

This release contains several security fixes for Android. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

## Version 114.0.1823.37: June 2, 2023

Fixed various bugs and performance issues.

### Policy update

- **iOS Website data store access.** Currently, the persistent data store is only statically used by personal accounts. Because work or school accounts can't use this data store, browsing data rather than cookies are lost when their sessions end. This new policy lets organizations access the data store dynamically, which persists browsing data for work or school accounts, giving users a better browsing experience. For more information, see this policy in [Manage Microsoft Edge on iOS and Android with Intune](/mem/intune/apps/manage-microsoft-edge#ios-website-data-store).

## Version 113.0.1774.50: May 18, 2023

Fixed various bugs and performance issues.

This release contains several security fixes for Android. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

## Version 113.1774.36: May 8, 2023

Fixed various bugs and performance issues.

### Feature updates

- **Open in Microsoft Edge option (iOS only).** This option is available for saving files to OneDrive.

- **Net-export supports open-in (iOS only).** This option now supports open-in instead of using the native mail app.

- **Shared Device Mode (SDM) for Edge mobile.** Generally available for Android.

## Version 112.0.1722.54: April 19, 2023

Fixed various bugs and performance issues.

This release contains several security fixes for Android. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

## Version 112.0.1722.44: April 12, 2023

Fixed various bugs and performance issues for iOS.

## Version 112.0.1722.36: April 7, 2023

Fixed various bugs and performance issues for Android.

### Feature updates

- **Translator, Read Aloud, Drop and developer tools (Android only).** These tools can be managed by Mobile Application Management (MAM) [disabledFeatures](/mem/intune/apps/manage-microsoft-edge#disable-specific-features) and the Mobile Device Management (MDM) policy, [EdgeDisabledFeatures](/deployedge/microsoft-edge-mobile-policies#edgedisabledfeatures).

## Version 111.0.1661.43: March 18, 2023

Fixed various bugs and performance issues.

### Feature updates

- **Support saving files to OneDrive for Business.** Save files securely with the Intune App Protection Policy. For more information, see [App protection policies overview](/mem/intune/apps/app-protection-policy).

- **Edge-specific policies are supported in the MDM channel.** These policies are now supported in version 111. For more information, see [Edge Specific](/deployedge/microsoft-edge-mobile-policies#edge-specific).

## Version 110.0.1587.61: March 1, 2023

Fixed various bugs and performance issues for Android.

## Version 110.0.1587.54: February 21, 2023

Fixed various bugs and performance issues.

### Feature updates

- **Microsoft Edge for iOS supports Microsoft Tunnel for MAM solution.** For more information, see [Learn about using Microsoft Tunnel with Mobile Application Management](/mem/intune/protect/microsoft-tunnel-mam).

## Version 109.0.1518.70: January 26, 2023

Fixed various bugs and performance issues.

This release contains several security fixes for iOS and Android. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

<!-- Version Version 109.0.1518.58: January 18, 2023 to Version 108.0.1462.45: December 8, 2022  -->
<!-- Version 108.0.1462.43: December 7, 2022 to Version 106.0.1370.47: October 17, 2022 -->
<!-- Version 105.0.1343.38: September 13, 2022 to Version 101.0.1210.32: April 29, 2022 -->

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
