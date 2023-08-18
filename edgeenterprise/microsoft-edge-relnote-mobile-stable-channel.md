---
title: "Microsoft Edge release notes for Mobile Stable Channel"
ms.author: charlielin
author: dan-wesley
manager: alexyuan
ms.date: 08/21/2023
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

## Version 116.0.xxxx.xx: August 21, 2023

Fixed various bugs and performance issues.

?? This release contains several security fixes for Android. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

### Feature updates

- Bing Chat Enterprise is available on Edge mobile by default, and can be managed by Intune MAM policy `com.microsoft.intune.mam.managedbrowser.Chat=true/false`.

- The **Open in Microsoft Edge** option is available for saving files to OneDrive (Android).

- Brand info (logo) of New Tab Page (NTP) is now pulled from MS Graph. If you only configure brand logo in the Intune portal, you must also configure it in the Azure portal. For more information, see [Add company branding - Basics](/azure/active-directory/fundamentals/how-to-customize-branding#basics).

- InPrivate mode can be managed by Mobile Device Management (MDM) Policy setting for [InPrivateModeAvailability](/deployedge/microsoft-edge-mobile-policies#inprivatemodeavailability).

## Version 115.0.1901.187: July 27, 2023

Fixed various bugs and performance issues for iOS.

## Version 115.0.1901.183: July 22, 2023

Fixed various bugs and performance issues for Android.

This release contains several security fixes for Android. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

## Version 114.0.1823.37: June 2, 2023

Fixed various bugs and performance issues.

### Policy update

- **iOS Website data store access.** Currently, the persistent data store is only statically used by personal accounts. Because work or school accounts can't use this data store, browsing data rather than cookies are lost when their sessions end. This new policy lets organizations access the data store dynamically, which persists browsing data for work or school accounts, giving users a better browsing experience. For more information, see this policy in [Manage Microsoft Edge on iOS and Android with Intune](/mem/intune/apps/manage-microsoft-edge#ios-website-data-store).

## Version 113.0.1774.50: May 18, 2023

Fixed various bugs and performance issues.

This release contains several security fixes for Android. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

<!-- Version 113.1774.36: May 8, 2023 to Version 112.0.1722.36: April 7, 2023 -->
<!-- Version 111.0.1661.43: March 18, 2023 to Version 109.0.1518.70: January 26, 2023 -->
<!-- Version Version 109.0.1518.58: January 18, 2023 to Version 108.0.1462.45: December 8, 2022  -->
<!-- Version 108.0.1462.43: December 7, 2022 to Version 106.0.1370.47: October 17, 2022 -->
<!-- Version 105.0.1343.38: September 13, 2022 to Version 101.0.1210.32: April 29, 2022 -->

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
