---
title: "Microsoft Edge release notes for Mobile Stable Channel"
ms.author: charlielin
author: dan-wesley
manager: alexyuan
ms.date: 02/07/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
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

## Version 121.0.2277.107 (iOS): February 7, 2024

Fixed various bugs and performance issues.

## Version 121.0.2277.99 (iOS): February 6, 2024

Fixed various bugs and performance issues.

## Version 121.0.2277.105 (Android): February 5, 2024

Fixed various bugs and performance issues.

## Version 121.0.2277.86 (iOS): February 1, 2024

Fixed various bugs, added new policy support, and enhanced users' experience.

### Fixes

**iOS:**

- Resolved the issue with the "Open in Microsoft Edge" option not functioning due to Intune SDK problem.
- Upgraded Microsoft Tunnel MAM SDK to version 1.0.11.
- Fixed a background crash related to the policy manager.
- Upgraded Intune MAM SDK for iOS to version 19.0.0.

### Policy updates

#### New policies

- [EdgeBlockSignInEnabled](/deployedge/microsoft-edge-mobile-policies#edgeblocksigninenabled) to block Edge sign-in
- [ExperimentationAndConfigurationServiceControl](/deployedge/microsoft-edge-mobile-policies#experimentationandconfigurationservicecontrol), allowing customers to opt-in for experiments and gain early access to Microsoft Edge experimenting features.

### Enhancements

- News feeds is enabled for work or school accounts.

<!-- =================================================== -->
## Version 121.0.2277.84 (Android): January 29, 2024

Fixed various bugs, added new policy support, and enhanced users' experience.

### Fixes

**Android:**

- Fixed bugs related to bookmarks.
- Upgraded Intune MAM SDK to version 10.1.0.
 
### Policy updates

#### New policies

- [EdgeBlockSignInEnabled](/deployedge/microsoft-edge-mobile-policies#edgeblocksigninenabled) to block Edge sign-in
- [ExperimentationAndConfigurationServiceControl](/deployedge/microsoft-edge-mobile-policies#experimentationandconfigurationservicecontrol), allowing customers to opt-in for experiments and gain early access to Microsoft Edge experimenting features.
- [EdgeOneAuthProxy](/deployedge/microsoft-edge-mobile-policies#edgeoneauthproxy) to specify a dedicated proxy to sign in to Edge in Android

### Enhancements

- News feeds is enabled for work or school accounts.

<!-- =================================================== -->
## Version 120.0.2210.150: January 21, 2024

Fixed various bugs and performance issues for Android and iOS.

## Version 120.0.2210.141: January 17, 2024

Fixed various bugs and performance issues for Android and iOS.

## Version 120.0.2210.126: January 9, 2024

Fixed various bugs and performance issues for Android and iOS.

## Version 120.0.2210.115: January 5, 2024

Fixed various bugs and performance issues for Android.

## Version 120.0.2210.116: January 2, 2024

Fixed various bugs and performance issues for iOS.

## Version 120.0.2210.105: December 29, 2023

Fixed various bugs and performance issues for iOS.

## Version 120.0.2210.99: December 27, 2023

Fixed various bugs and performance issues.

**Note:** The app jump blocker feature is removed from Android and iOS.

## Version 120.0.2210.86: December 19, 2023

Fixed various bugs and performance issues for iOS.

## Version 120.0.2210.84: December 19, 2023

Fixed various bugs and performance issues for Android.

## Version 120.0.2210.78: December 15, 2023

Fixed various bugs and performance issues for iOS.

 **Note:** The default key value for [iOS Website data store](/mem/intune/apps/manage-microsoft-edge#ios-website-data-store) is changed to "2".

## Version 120.0.2210.64: December 12, 2023

Fixed various bugs and performance issues for Android.

### Policy support

For more information, see [Manage Microsoft Edge on iOS and Android with Intune](/mem/intune/apps/manage-microsoft-edge).

MAM Policy to configure search engine:

- `com.microsoft.intune.mam.managedbrowser.DefaultSearchProviderEnabled`
- `com.microsoft.intune.mam.managedbrowser.DefaultSearchProviderName`
- `com.microsoft.intune.mam.managedbrowser.DefaultSearchProviderSearchURL`

MAM Policy to configure pop-up behavior:

- `com.microsoft.intune.mam.managedbrowser.DefaultPopupsSetting`
- `com.microsoft.intune.mam.managedbrowser.PopupsAllowedForUrls`
- `com.microsoft.intune.mam.managedbrowser.PopupsBlockedForUrls`

### Policy update

#### New policies

- [EdgeBrandLogo](/deployedge/microsoft-edge-mobile-policies#edgebrandlogo) - Configure Brand logo in New Tab Page
- [EdgeBrandColor](/deployedge/microsoft-edge-mobile-policies#edgebrandcolor) - Configure Brand color in New Tab Page
- [EdgeProxyPacUrl](/deployedge/microsoft-edge-mobile-policies#edgeproxypacurl) - Specify a URL to a proxy auto-config (PAC) file
- [PopupsAllowedForUrls](/deployedge/microsoft-edge-mobile-policies#popupsallowedforurls) - Allow pop-up windows on specific sites
- [PopupsBlockedForUrls](/deployedge/microsoft-edge-mobile-policies#popupsblockedforurls) - Block pop-up windows on specific sites

## Version 120.0.2210.59: December 12, 2023

Fixed various bugs and performance issues for iOS.

### Policy support

For more information, see [Manage Microsoft Edge on iOS and Android with Intune](/mem/intune/apps/manage-microsoft-edge).

MAM Policy to configure search engine:

- `com.microsoft.intune.mam.managedbrowser.DefaultSearchProviderEnabled`
- `com.microsoft.intune.mam.managedbrowser.DefaultSearchProviderName`
- `com.microsoft.intune.mam.managedbrowser.DefaultSearchProviderSearchURL`

MAM Policy to configure pop-up behavior:

- `com.microsoft.intune.mam.managedbrowser.DefaultPopupsSetting`
- `com.microsoft.intune.mam.managedbrowser.PopupsAllowedForUrls`
- `com.microsoft.intune.mam.managedbrowser.PopupsBlockedForUrls`

### Policy update

#### New policies

- [EdgeBrandLogo](/deployedge/microsoft-edge-mobile-policies#edgebrandlogo) - Configure Brand logo in New Tab Page
- [EdgeBrandColor](/deployedge/microsoft-edge-mobile-policies#edgebrandcolor) - Configure Brand color in New Tab Page
- [EdgeProxyPacUrl](/deployedge/microsoft-edge-mobile-policies#edgeproxypacurl) - Specify a URL to a proxy auto-config (PAC) file
- [PopupsAllowedForUrls](/deployedge/microsoft-edge-mobile-policies#popupsallowedforurls) - Allow pop-up windows on specific sites
- [PopupsBlockedForUrls](/deployedge/microsoft-edge-mobile-policies#popupsblockedforurls) - Block pop-up windows on specific sites

## Version 119.0.2151.107: December 6, 2023

Fixed various bugs and performance issues for Android.

## Version 119.0.2151.105: December 5, 2023

Fixed various bugs and performance issues for iOS.

## Version 119.0.2151.96: November 30, 2023

Fixed various bugs and performance issues for iOS.

## Version 119.0.2151.92: November 28, 2023

Fixed various bugs and performance issues for Android and iOS.

## Version 119.0.2151.78: November 21, 2023

Fixed various bugs and performance issues for Android and iOS.

## Version 119.0.2151.65: November 13, 2023

Fixed various bugs and performance issues for Android and iOS.

## Version 119.0.2151.56: November 9, 2023

Fixed various bugs and performance issues for iOS.

## Version 119.0.2151.46: November 7, 2023

Fixed various bugs and performance issues for Android.

### Policy support (Android and iOS)

Configure to turn on Microsoft Defender SmartScreen:

- MAM: [com.microsoft.intune.mam.managedbrowser.SmartScreenEnabled](/mem/intune/apps/manage-microsoft-edge#microsoft-defender-smartscreen)
- MDM: [SmartScreenEnabled](/deployedge/microsoft-edge-mobile-policies#smartscreenenabled)

Configure to turn on ManagedFavorites (bookmarks):

- MDM: [ManagedFavorites](/deployedge/microsoft-edge-mobile-policies#managedfavorites)

<!-- Version 118.0.2088.81: November 1, 2023 to Version 117.0.2045.53: October 6, 2023  -->
<!-- Version 117.0.2045.33: September 15, 2023 to Version 116.0.1938.64: August 30, 2023  -->
<!-- Version 116.0.1938.56: August 21, 2023, to Version 115.0.1901.183: July 22, 2023 -->
<!-- Version 114.0.1823.37: June 2, 2023 to Version 113.0.1774.50: May 18, 2023 -->
<!-- Version 113.1774.36: May 8, 2023 to Version 112.0.1722.36: April 7, 2023 -->
<!-- Version 111.0.1661.43: March 18, 2023 to Version 109.0.1518.70: January 26, 2023 -->
<!-- Version Version 109.0.1518.58: January 18, 2023 to Version 108.0.1462.45: December 8, 2022  -->
<!-- Version 108.0.1462.43: December 7, 2022 to Version 106.0.1370.47: October 17, 2022 -->
<!-- Version 105.0.1343.38: September 13, 2022 to Version 101.0.1210.32: April 29, 2022 -->

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
