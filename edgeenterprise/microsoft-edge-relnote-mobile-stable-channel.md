---
title: "Microsoft Edge release notes for Mobile Stable Channel"
ms.author: charlielin
author: dan-wesley
manager: alexyuan
ms.date: 04/10/2024
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

## Version 123.0.2420.90 (Android): April 10, 2024

Fixed various bugs and performance issues.

## Version 123.0.2420.74 (Android and iOS): April 2, 2024

Fixed various bugs and performance issues.

### General updates

- [iOS] Update Citrix mVPN SDK to version 24.2.1

### New features

- Start a flight to show Shared links entry point on the overflow menu

## Version 123.0.2420.61 (Android): March 25, 2024

Fixed various bugs and performance issues. This release includes general updates, and new policies.

### General updates

- [Android] Remove "https" scheme check for managed bookmarks to support URLs such as `edge://…`.

### Bug fixes

- [Android] Fix a bug that NLTM SSO policy doesn't work in some conditions.
- [Android] Fix issues for brand logo policy.

### Policy updates

- Introduce a policy to control the behavior of opening Intune unmanaged URL in work profile. Current behavior is "stay" and open the unmanaged URL in work profile. This policy allows admin to change behavior to switch to personal context and open the unmanaged URL.

  `com.microsoft.intune.mam.managedbrowser.ProfileAutoSwitch`
  - 0 (Default) - The URLs are opened in normal tabs with work profile
  - 1 - Edge respects Intune's protection policy, the behavior is based on the configuration of Receive data from other apps in Intune protection policy.
    - All apps - fall back to behavior for policy value 0
    - None or Policy managed apps
      - If personal profile is signed-in, the URLs are opened in normal tabs with personal profile
      - If personal profile isn't signed-in, the URLs are opened in InPrivate
      - If InPrivate is disabled, the URLs won't be opened
  - 2 (Android only) - Microsoft Edge checks **URLAllowlist** or **URLBlocklist**. Microsoft Edge opens allowed URLs in normal tabs with work profile. As for URLs in blocklist, they might or might not be opened in InPrivate or normal tabs with personal profile, it depends on how **openInPrivateIfBlocked** is configured.

## Version 123.0.2420.56 (iOS): March 25, 2024

Fixed various bugs and performance issues. This release includes general updates, new features, and new policies.

### General updates

- [iOS] Update MS Tunnel MAM SDK to 1.0.12
- [iOS] Update MS Intune MAM SDK to 19.1.0
- [iOS] "Save to OneDrive" option in Edge now has upload progress indicator.

### Bug fixes

- [iOS] URL Block policy also shows "Site blocked" alert for http POST requests.
- [iOS] Fix issues for new File upload block policy and idle timer policy.

### New features

- [iOS] Shared device mode public preview

### Policy updates

- [iOS] Introduces MAM policy to control the behavior the "Site Blocked" popup. This policy would let admins choose preferences between InPrivate and MSA if options are available.
`com.microsoft.intune.mam.managedbrowser.AutoTransitionModeOnBlock`
  - 0 (Default) - Always show choose popup windows
  - 1 - Only MSA account login, auto transition to MSA
  - 2 - When the MSA account login and InPrivate are enabled at the same time, auto transition to MSA
  - 3 - When the MSA account login and InPrivate are enabled at the same time, auto transition to InPrivate.

- [iOS] Introduce a policy to control the behavior of opening Intune unmanaged URL in work profile. Current behavior is "stay" and open the unmanaged URL in work profile. This policy allows admin to change behavior to switch to personal context and open the unmanaged URL.

  `com.microsoft.intune.mam.managedbrowser.ProfileAutoSwitch`
  - 0 (Default) - The URLs are opened in normal tabs with work profile
  - 1 - Edge respects Intune's protection policy, the behavior is based on the configuration of Receive data from other apps in Intune protection policy.
    - All apps - fall back to behavior for policy value 0
    - None or Policy managed apps
      - If personal profile is signed-in, the URLs are opened in normal tabs with personal profile
      - If personal profile isn't signed-in, the URLs are opened in InPrivate
      - If InPrivate is disabled, the URLs won't be opened

## Version 122.0.2365.99 (Android and iOS): March 18, 2024

Fixed various bugs and performance issues.

## Version 122.0.2365.86 (Android and iOS): March 12, 2024

Fixed various bugs and performance issues.

## Version 122.2365.78 (iOS): March 8, 2024

Fixed various bugs and performance issues.

### Fixes

- fixed a crash issue

## Version 122.0.2365.76 (Android): March 7, 2024

Fixed various bugs and performance issues.

### Feature update

- Extensions in Edge for Android can be disabled by MAM policy.
  - `com.microsoft.intune.mam.managedbrowser.disabledFeatures=extensions`

  Note: The Extensions feature is still in flight. It can be turned on by the Android Extension flag from *Edge://flags*.

## Version 122.2365.71 (iOS): March 6, 2024

Fixed various bugs and performance issues.

## Version 122.0.2365.56 (Android and iOS): February 26, 2024

Made general updates, fixed various bugs, and added new policy support.

### General updates

- Updated the Intune Mobile Application Management (MAM) SDK to version 19.1.0.
- With the release of iOS 17, multiple persistent stores are now supported. Work and personal accounts have their own designated persistent store. The MAM policy [`com.microsoft.intune.mam.managedbrowser.PersistentWebsiteDataStore`](/mem/intune/apps/manage-microsoft-edge#ios-website-data-store) is no longer applicable.

### Bug fixes

- Fixed crash with Microsoft MAM Tunnel
- Fixed bug for MDM policy EdgeBlockSignInEnabled
- Addressed accessibility and UI issues related to implicit sign-in.
- Resolved several policy-related crashes and performance issues.
- [iOS] Fixed a bug preventing deep links from opening via `window.open()`.
- [iOS] Resolved an issue where the Intune SDK unexpectedly blocked "Open in Microsoft Edge".
- [iOS] Resolved an issue with closing tabs in InPrivate mode.

### Policy updates

- [iOS] Mobile Application Management (MDM) policy IdleTimeoutActions to specify actions to run when the timeout from the IdleTimeout policy is reached. Only close_tabs is supported.
- [iOS] MDM policy IdleTimeout to specify the length of time without user input (in minutes) before the browser runs actions configured via the IdleTimeoutActions policy.
- MAM policy to allow or block file uploads to specified domains.
  - `com.microsoft.intune.mam.managedbrowser.FileUploadBlockedForUrls`
  - `com.microsoft.intune.mam.managedbrowser.FileUploadAllowedForUrls`

## Version 121.0.2277.133: February 20, 2024

Fixed various bugs and performance issues for Android and iOS.

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
