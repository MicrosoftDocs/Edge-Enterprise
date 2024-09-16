---
title: "Microsoft Edge release notes for Mobile Stable Channel"
ms.author: charlielin
author: dan-wesley
manager: alexyuan
ms.date: 09/16/2024
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

## Version 128.0.2739.82 (Android): September 16, 2024

Fixed various bugs and performance issues.

## Version 128.0.2739.72 (Android and iOS): September 10, 2024

Fixed various bugs and performance issues.

## Version 128.0.2739.64 (Android): September 5,2024

Fixed various bugs and performance issues.

## Version 128.0.2739.60 (iOS): September 4, 2024

Fixed various bugs and performance issues.

## Version 128.0.2739.60 (Android): September 3, 2024

Fixed various bugs and performance issues, general updates, enhancements, and feature updates.

### General updates

- [Android] Upgrade Intune MAM SDK to version 10.3.1
- [Android] Upgrade OneAuth SDK to version 3.0.0

### Bug fixes

- [Android] Fix AppProxy translation worked in InPrivate context unexpectedly
- [Android] Fix a bug related to policy of single device mode

### Enhancements

- [Android] General enhancements to NTLMSSO policies to make it more useful, and added support for 407 proxy auth challenges.
- [Android] Re-sign-in prompts and banners are reworded as "re-verify account" for clarity. These prompts and banners remind the user to verify their account by reinputting a password and refresh underlying tokens to keep account state healthy.
- [Android] Clear opened tabs data when signing out of Microsoft Entra ID if clear data is chosen.

### Feature updates

- **Deprecation of Copilot on Edge mobile.** Microsoft Copilot and the corresponding settings are removed from the Edge mobile application.  

  Copilot for work and web chat will be available to Entra ID users through the Microsoft 365 mobile application.

## Version 128.0.2739.42 (iOS): August 27, 2024

Fixed various bugs and performance issues, general updates, enhancements, feature updates, and new policies.

### General updates

- [iOS] Upgrade MS Tunnel SDK version 1.1.7
- [iOS] Upgrade Intune MAM SDK to version 19.5.1
- [iOS] Upgrade OneAuth SDK to version 3.0.0

### Bug fixes

- [iOS] Fix a bug related to the [DefaultBrowserSettingEnabled](/deployedge/microsoft-edge-mobile-policies#defaultbrowsersettingenabled) policy.

### Enhancements

- [iOS] General enhancements to NTLMSSO policies to make it more useful, added support for 407 proxy auth challenges.
- [iOS] Re-sign-in prompts and banners are changed to "re-verify account" for clarity. These prompts and banners remind a user to verify their account by reinputting a password and refresh underlying tokens to keep account state healthy.
- [iOS] Clear opened tabs data when signing out of Microsoft Entra ID if clear data is chosen.

### Feature updates

- **Deprecation of Copilot on Edge mobile.** Microsoft Copilot and the corresponding settings are removed from the Edge mobile application.  

  Copilot for work and web chat will be available to Entra ID users through the Microsoft 365 mobile application.

### New Policies

- [iOS] Enable Web Inspector and add a new token (`webinspector`) of disabled features policy to disable it. Previously Web Inspector was disabled in Stable versions, but it's now enabled for general web site debugging and troubleshooting purposes.

## Version 127.0.2651.111 (Android and iOS): August 20, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.102 (Android and iOS): August 13, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.96 (iOS): August 8, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.90 (Android): August 6, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.82 (Android): August 1, 2024

Fixed various bugs and performance issues, general updates, and new policies.

### General updates

- [Android] Exclude Microsoft Entra ID Copilot from NTP's voice and camera search

### Bug fixes

- [Android] Fix a bug related to policy InPrivateModeAvailability
- [Android] Fix SSO bug when a blocked link is opened from Outlook

### New policies

- [Android] Disable UIR prompt pop-up via `com.microsoft.intune.mam.managedbrowser.disabledFeatures` or [EdgeDisabledFeatures](/deployedge/microsoft-edge-mobile-policies#edgedisabledfeatures) policy
- [Android] Add CIDR (Classless Inter-domain Routing) support in AllowListURLs/BlockListURLs feature
- [Android] New `com.microsoft.intune.mam.managedbrowser.InternalPagesBlockList` policy to allow IT admin disable edge internal pages

## Version 127.0.2651.81 (iOS): July 31, 2024

Fixed various bugs and performance issues, general updates, new policies, and enhancements.

### Bug fixes

- [iOS] Fix [DefaultBrowserSettingEnabled](/deployedge/microsoft-edge-mobile-policies#defaultbrowsersettingenabled) policy that didn't work
- [iOS] Fix the UI layout issue caused by changes in UIWindow safeAreaInsets leading to Webview content offset shift in certain situations

### General updates

- [iOS] Upgrade MS Tunnel SDK version 1.0.18
- [iOS] Upgrade Intune MAM SDK to version 19.4.1

### New policies

- [iOS] Disable UIR prompt pop-up via `com.microsoft.intune.mam.managedbrowser.disabledFeatures` or [EdgeDisabledFeatures](/deployedge/microsoft-edge-mobile-policies#edgedisabledfeatures) policy
- [iOS] Add CIDR (Classless Inter-domain Routing) support in AllowListURLs/BlockListURLs feature
- [iOS] New `com.microsoft.intune.mam.managedbrowser.InternalPagesBlockList` policy to allow IT admin disable edge internal pages

### Enhancements

- [iOS] Shared device mode support is generally available.

## Version 126.2592.120 (iOS): July 24, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.117 (Android): July 23, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.106 (Android and iOS): July 16, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.100 (Android and iOS): July 11, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.86 (Android and iOS): July 2, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.80 (Android): June 27, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.74 (Android): June 25, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.56 (Android and iOS): June 17, 2024

Fixed various bugs and performance issues, made general updates, added policies and enhancements.

### General updates

- [iOS] Upgrade MS Tunnel SDK version 1.1.0
- [Android and iOS] Update OneAuth SDK to 2.3.1

### Bug fixes

- [Android] Scrolling screenshot will be disabled if Intune APP (App Protection Policy) is configured to block screenshot.

### New policies

- [Android and iOS] Manage contextual search via policy `com.microsoft.intune.mam.managedbrowser.disabledFeatures=contextualsearch`
- [iOS] Introduce MDM policy **EdgeSharedDeviceSupportEnabled** to disable shared device mode.

### Enhancements

- [Android and iOS] Remove [Copilot](https://copilot.microsoft.com/#/) from default allowlist so that you can manage access to [Copilot](https://copilot.microsoft.com/#/) via URLs blocklist.
- [iOS] Support Passkey on iOS. This feature is disabled by default. It can be enabled by turning on the `flag edge-iOS-enable-passkey-signin` from *Edge://flags*.

<!-- ranges cut out for mobile stable archive -->
<!-- Version 125.0.2535.96 (Android and iOS): June 11, 2024 to Version 125.0.2535.51 (Android): May 21, 2024 --->
<!-- Version 124.0.2478.105 (iOS): May 17, 2024 to Version 124.0.2478.50 (Android and iOS): April 22, 2024 -->
<!-- Version 123.0.2420.108 (iOS): April 19, 2024 to Version 123.0.2420.56 (iOS): March 25, 2024 -->
<!-- Version 122.0.2365.99 (Android and iOS): March 18, to 2024 Version 121.0.2277.84 (Android): January 29, 2024 -->
<!-- Version 120.0.2210.150: January 21, 2024 to Version 120.0.2210.59: December 12, 2023 -->
<!-- Version 119.0.2151.107: December 6, 2023 to Version 119.0.2151.46: November 7, 2023  -->
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
