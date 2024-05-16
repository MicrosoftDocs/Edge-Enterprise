---
title: "Microsoft Edge release notes for Mobile Beta Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 05/16/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Microsoft Edge release notes for Mobile Beta Channel"
---

# Release notes for Microsoft Edge Mobile Beta Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Mobile Beta Channel.

To understand Microsoft Edge channels, see the [Overview of the Microsoft Edge channels](./microsoft-edge-channels.md).

You can download Beta versions of Edge Mobile from the following locations:

- Edge Android: [Microsoft Edge Beta – Apps on Google Play](https://play.google.com/store/apps/details?id=com.microsoft.emmx.beta)
- Edge iOS: [https://testflight.apple.com/join/rqvYCYOp](https://testflight.apple.com/join/rqvYCYOp)
<!---
Archived versions of these release notes are available at [Archived release notes for Microsoft Edge Beta Channel](./microsoft-edge-relnote-archive-beta-channel.md). --->

> [!NOTE]
> Microsoft Edge Web Platform constantly evolves to improve user experience, security, and privacy. To learn more, see [Site compatibility-impacting changes coming to Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## Version 125.0.2535.48 (Android and iOS): May 16, 2024

Fixed various bugs and performance issues, includes general updates, new features, and new policies.

### General updates

- [iOS] MS Tunnel Tunnel SDK updated to 1.0.17
- [iOS] Upgrade Intune iOS SDK to 19.3.1, with working time support
- [Android] Upgrade Intune Android SDK to 10.3.0, with working time support

### New features

- [Android] Edge Android now supports kerberos/negotiate authentication on Android via an [external SPNEGO authenticator app](https://github.com/google/android-kerberos-authenticator) integrated with Android account management framework
- [iOS & Android] Shared links feature will appear in overflow menu in work account
- [iOS] PAC policy now supports fail-close
- [iOS] Support certificate pinning via Intune, currently only supports limited number of Microsoft domains. Pending on Intune's improvements to support customizable cert-domain pair
- [iOS] Support of new iOS 17 relay proxy via policy `com.microsoft.intune.mam.managedbrowser.ProxyRelayUrl`

### New Policies

- [iOS] `com.microsoft.intune.mam.managedbrowser.ProfileAutoSwitchToWork` to resolve the conflict between Intune auto identity switch and Edge allow/block URL policies.
- [iOS and Android] Introduce MDM policy [EdgeCopilotEnabled](/deployedge/microsoft-edge-mobile-policies#edgecopilotenabled), to globally disable Copilot in Edge mobile, including the personal context.

## Version 125.0.2535.44 (Android): May 14, 2024

Fixed various bugs and performance issues.

## Version 125.0.2535.34 (Android and iOS): May 9, 2024

Fixed various bugs and performance issues.

## Version 125.0.2535.30 (Android and iOS): May 7, 2024

Fixed various bugs and performance issues.

## Version 125.0.2535.16 (iOS): April 30, 2024

Fixed various bugs and performance issues.

## Version 125.0.2535.14 (Android and iOS): April 29, 2024

Fixed various bugs and performance issues.

## Version 124.0.2478.50 (Android and iOS): April 18, 2024

Fixed various bugs and performance issues.

## Version 124.0.2478.46 (Android and iOS): April 16, 2024

Fixed various bugs and performance issues, made general updates, added new features and policies.

### General updates

- [iOS] MS Tunnel updated to 1.0.15, added privacy manifest file to comply with Apple App Store requirements.
- [iOS] updated Citrix mVPN iOS SDK to 24.2.1
- [iOS] added `protApp` param to Microsoft Bing Search resource token fetch request, so it will not be blocked by the CA policy, "requiring app protection." This token is needed for Copilot in Edge.
- [iOS] Intune SDK updated to 19.2.0

### Bug fixes

- [iOS] Fix disableFeatures policy bug for inPrivate mode, and handle corner cases where inPrivate not disabled.
- [Android] Fixed a bug in Guided switch.

### New features

- [Android] Re-enable Kerberos authentication suppport on Android with an external Negotiate Authenticator app.
- [Android and iOS] Copilot in Edge mobile now properly supports school scenarios.
- [iOS] Shared Device Mode support.
- [Android and iOS] In-flight, the feature "Shared Links" can be opened from Edge overflow menu.

### New policies

- [Android and iOS] Introduced a new MDM policy, "EdgeCopilotEnabled" to globally disable Copilot in Edge mobile, including on the personal context.

## Version 124.0.2478.36 (Android and iOS): April 11, 2024

Fixed various bugs and performance issues.

## Version 124.0.2478.33 (Android and iOS): April 10, 2024

Fixed various bugs and performance issues.

## Version 124.0.2478.20 (Android and iOS): April 2, 2024

Fixed various bugs and performance issues.

## Version 124.0.2478.9 (Android and iOS): March 28, 2024

Fixed various bugs and performance issues.

## Version 123.0.2420.50 (Android and iOS): March 20, 2024

Fixed various bugs and performance issues. It also includes new features and policy updates.

### General updates

- [iOS] Update MS Tunnel MAM SDK to 1.0.12
- [iOS] Update MS Intune MAM SDK to 19.1.0
- [Android] Remove "https" scheme check for managed bookmarks to support URLs such as `edge://…`
- [iOS] "Save to OneDrive" option in Microsoft Edge now has an upload progress indicator

### Bug fixes

- [iOS] URL Block policy also shows "Site blocked" alert for http POST requests
- [Android] Fix a bug that NLTM SSO policy doesn't work in some conditions
- [Android] Fix issues for brand logo policy
- [iOS] Fix issues for new File upload block policy and idle timer policy

### New features

- [After Stable release] The Shared links feature replaces "Collections" in the Microsoft Edge overflow menu
- [iOS][After Stable release] Shared device mode public preview
- Microsoft Edge Copilot toolbar is in the flight. It helps user summarize long web pages

### Policy updates

- [iOS][After Stable release] Introduces MAM policy to control the behavior the "Site Blocked" popup. This policy would let admins choose preferences between InPrivate and MSA if options are available.
`com.microsoft.intune.mam.managedbrowser.AutoTransitionModeOnBlock`
  - 0 (Default) - Always show choose popup windows
  - 1 - Only MSA account login, auto transition to MSA
  - 2 - When the MSA account login and InPrivate are enabled at the same time, auto transition to MSA
  - 3 - When the MSA account login and InPrivate are enabled at the same time, auto transition to InPrivate.

- [iOS][After Stable release] Introduce a policy to control the behavior of opening Intune unmanaged URL in work profile. Current behavior is "stay" and open the unmanaged URL in work profile. This policy allows admin to change behavior to switch to personal context and open the unmanaged URL.

  `com.microsoft.intune.mam.managedbrowser.ProfileAutoSwitch`
  - 0 (Default) -  The URLs are opened in normal tabs with work profile
  - 1 -  Edge respects Intune's protection policy, the behavior is based on the configuration of Receive data from other apps in Intune protection policy.
    - All apps  -  fall back to behavior for policy value 0
    - None or Policy managed apps
      - If personal profile is signed-in, the URLs are opened in normal tabs with personal profile
      - If personal profile isn't signed-in, the URLs are opened in InPrivate
      - If InPrivate is disabled, the URLs won't be opened
  - 2 (Android only) - Microsoft Edge checks **URLAllowlist** or **URLBlocklist**. Microsoft Edge opens allowed URLs in normal tabs with work profile. As for URLs in blocklist, they might or might not be opened in InPrivate or normal tabs with personal profile, it depends on how **openInPrivateIfBlocked** is configured.

## Version 123.0.2420.48 (Android and iOS): March 19, 2024

Fixed various bugs and performance issues.

## Version 123.0.2420.37 (Android and iOS): March 15, 2024

Fixed various bugs and performance issues.

## Version 123.0.2420.33 (Android and iOS): March 12, 2024

Fixed various bugs and performance issues.

### Fixes

- Fixed the issue that POST navigation is blocked silently without showing the UI.

## Version 123.0.2420.23 (Android and iOS): March 7, 2024

Fixed various bugs and performance issues.

## Version 123.0.2420.17 (Android): March 5, 2024

Fixed various bugs and performance issues.

## Version 122.0.2365.50 (Android): February 22, 2024

Fixed various bugs and performance issues.

## Version 122.0.2365.49 (iOS): February 22, 2024

Fixed various bugs and performance issues.

## Version 122.0.2365.18: February 7, 2024

### General Updates

- Updated the Intune Mobile Application Management (MAM) SDK to version 19.1.0.
- With the release of iOS 17, multiple persistent stores are now supported. Work and personal accounts have their own designated persistent store. The MAM policy [com.microsoft.intune.mam.managedbrowser.PersistentWebsiteDataStore](/mem/intune/apps/manage-microsoft-edge#ios-website-data-store) is no longer applicable.

### Bug fixes

- Addressed accessibility and UI issues related to implicit sign-in.
- Resolved several policy-related crashes and performance issues.
- [iOS] Fixed a bug preventing deep links from opening via `window.open()`.
- [iOS] Resolved an issue where the Intune SDK unexpectedly blocked "Open in Microsoft Edge".
- [iOS] Resolved an issue with closing tabs in InPrivate mode.

### Policy updates

- [iOS] Mobile Application Management (MDM) policy IdleTimeoutActions to specify actions to run when the timeout from the IdleTimeout policy is reached. Only `close_tabs` is supported.
- [iOS] MDM policy IdleTimeout to specify the length of time without user input (in minutes) before the browser runs actions configured via the IdleTimeoutActions policy.
- MAM policy to allow or block file uploads to specified domains.
  - `com.microsoft.intune.mam.managedbrowser.FileUploadBlockedForUrls`
  - `com.microsoft.intune.mam.managedbrowser.FileUploadAllowedForUrls`

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
