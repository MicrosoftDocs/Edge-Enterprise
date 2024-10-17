---
title: "Microsoft Edge release notes for Mobile Beta Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 10/15/2024
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

## Version 130.0.2849.40 (Android and iOS): October 15, 2024

Fixed various bugs and performance issues, general updates, new policies, and enhancements.

### General updates

- [iOS] Upgrade Intune MAM SDK to version 19.7.0
- [iOS] Upgrade MAM Tunnel SDK to version 1.1.12
- [iOS & Android] Enable wallpaper on NTP for Commercial user by default. A user can configure `com.microsoft.intune.mam.managedbrowser.NewTabPageLayout.Custom` to exclude the wallpaper.
- [iOS & Android] Enable weather widget on NTP for Commercial user by default. A user can add weather token to **DisableFeature** policy to disable it the widget.

### Bug fixes

- [iOS] Fix issue about single device mode force sign-in interrupted by external intent.
- [iOS] Fix **disableImportPasswords** policy not working as expected.

### New policies

- [iOS & Android] Support to disable weather widget on NTP via **DisableFeature** policy
(`com.microsoft.intune.mam.managedbrowser.disabledFeatures` in MAM) and **EdgeDisabledFeatures** in MDM, now supports disabling weather widget on NTP by using "weather" as value.

### Enhancements

- [iOS] Support removing specified account from sign in account list.
- [Android] Change default value of `recommendsCustomUi` to support passkey in Edge. Before these changes, the user can only use Google Password Manager and can't select Microsoft Authenticator to save passkey. After these changes, a user can select a 3rd party passkey app, including Microsoft Authenticator.
- [Android] Improve the feature experience for App proxy.
- [iOS & Android] Improve the occurrence of re-sign in prompts on NTP.
- [iOS & Android] General enhancements to NTLMSSO policies to make it more useful.
- [iOS & Android] Enable Managed Browser revamp feature by default with silent mode as the managed browser. This change helps customers remediate from non-compliant cases, such as no device registration.

## Version 130.0.2849.32 (Android and iOS): October 14, 2024

Fixed various bugs and performance issues.

## Version 130.0.2849.28 (Android and iOS): October 10, 2024

Fixed various bugs and performance issues.

## Version 130.0.2849.10 (iOS): September 30, 2024

Fixed various bugs and performance issues.

## Version 130.0.2849.6 (Android): September 27, 2024

Fixed various bugs and performance issues.

## Version 130.0.2849.4 (iOS): September 26, 2024

Fixed various bugs and performance issues.

## Version 129.0.2792.58 (Android): September 24, 2024

Fixed various bugs and performance issues.

## Version 129.0.2792.51 (iOS): September 19, 2024

Fixed various bugs and performance issues, general updates, new policies, and enhancements.

### General updates

- [iOS] Upgrade Intune MAM SDK to version 19.6.0
- [iOS] Upgrade MS OneAuth SDK version 3.3.0
- [iOS] Remove native AAD Copilot support

### Bug fixes

- [iOS] Fix managed bookmarks dismiss under AAD account (missing "XXX's Favorites" folder under favorites)
- [iOS] Fix downloaded files not properly moved in work profile
- [iOS] Fix a bug related to MAM Tunnel cannot be disconnected automatically when change to personal account
- [iOS] Fix disableFeatures policy - InPrivate mode disablement bug & support policy auto change
(The problem is when set `com.microsoft.intune.mam.managedbrowser.disabledFeatures='inprivate'`, the InPrivate mode can still be accessed, and the corresponding toolbar button remains functional. Expects the policy to support dynamic switching without needing to restart Edge. When InPrivate mode is disabled by the policy, the application should automatically exit InPrivate mode and close all open InPrivate tabs)

### New Policies

- [iOS] Support to disable Share and SendtoDevices via **DisableFeature** policy
(`com.microsoft.intune.mam.managedbrowser.disabledFeatures` in MAM and `EdgeDisabledFeatures` in MDM now support to config to disable Share and Sendtodevices in overflow menu by value `share|sendtodevices`)

### Enhancements

- [iOS] Improve the transition user experience for account switcher in iPad
- [iOS] Improve Web SSO for CMC (copilot.microsoft.com) login in MSA
- [iOS] Improve the occurrence of re-sign-in prompts by disallow user interaction for proactive-auth
- [iOS] Improve account verification by consider sync and news feed status
- [iOS] General enhancements to NTLMSSO policies to make it more useful

## Version 129.0.2792.49 (Android): September 19, 2024

Fixed various bugs and performance issues, general updates, new policies, and enhancements.

### General updates

- [Android] Upgrade Intune MAM SDK to version 10.4.0
- [Android] Upgrade MS OneAuth SDK version 3.3.0
- [Android] Remove native AAD Copilot support

### New Policies

- [Android] Support to disable Share and SendtoDevices via DisableFeature policy
(`com.microsoft.intune.mam.managedbrowser.disabledFeatures` in MAM and EdgeDisabledFeatures in MDM now support to config to disable Share and Sendtodevices in overflow menu by value `share|sendtodevices`)

### Enhancements

- [Android] Improve the occurrence of re-sign-in prompts by disallow user interaction for proactive-auth
- [Android] Improve account verification by consider sync and news feed status
- [Android] General enhancements to NTLMSSO policies to make it more useful

## Version 129.0.2792.37 (Android and iOS): September 12, 2024

Fixed various bugs and performance issues.

## Version 129.0.2792.33 (Android and iOS): September 10, 2024

Fixed various bugs and performance issues.

## Version 129.0.2792.24 (Android and iOS): September 5, 2024

Fixed various bugs and performance issues.

## Version 129.0.2792.20 (Android and iOS): September 3, 2024

Fixed various bugs and performance issues.

## Version 129.0.2792.11 (Android and iOS): August 29, 2024

Fixed various bugs and performance issues.

## Version 128.0.2739.40 (Android and iOS): August 22, 2024

Fixed various bugs and performance issues.

## Version 128.0.2739.35 (iOS): August 19, 2024

Fixed various bugs and performance issues, new policies, general updates, and enhancements.

### General updates

- [iOS] Upgrade MS Tunnel SDK version 1.1.7
- [iOS] Upgrade Intune MAM SDK to version 19.5.1
- [iOS] Upgrade OneAuth SDK to version 3.0.0

### Bug fixes

- [iOS] Fix a bug related to the [DefaultBrowserSettingEnabled](/deployedge/microsoft-edge-mobile-policies#defaultbrowsersettingenabled) policy.

### New Policies

- [iOS] Enable Web Inspector and add a new token (`webinspector`) of disabled features policy to disable it. Previously Web Inspector was disabled in Stable versions, but it's now enabled for general web site debugging and troubleshooting purposes.

### Enhancements

- [iOS] General enhancements to NTLMSSO policies to make it more useful, added support for 407 proxy auth challenges.
- [iOS] Re-sign-in prompts and banners are changed to "re-verify account" for clarity. These prompts and banners remind a user to verify their account by reinputting a password and refresh underlying tokens to keep account state healthy.
- [iOS] Clear opened tabs data when signing out of Microsoft Entra ID if clear data is chosen.

## Version 128.0.2739.34 (Android): August 19, 2024

Fixed various bugs and performance issues, general updates, and enhancements.

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

## Version 128.0.2739.27 (Android and iOS): August 15, 2024

Fixed various bugs and performance issues.

## Version 128.0.2739.23 (iOS): August 13, 2024

Fixed various bugs and performance issues.

## Version 128.0.2739.22 (Android): August 13, 2024

Fixed various bugs and performance issues.

## Version 128.0.2739.18 (Android and iOS): August 8, 2024

Fixed various bugs and performance issues.

## Version 128.0.2739.14 (Android): August 7, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.73 (Android and iOS): July 25, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.69 (Android and iOS): July 23, 2024

Fixed various bugs and performance issues, general updates, new policies, and enhancements.

### General updates

- [iOS] Upgrade MS Tunnel SDK version 1.0.18
- [iOS] Upgrade Intune MAM SDK to version 19.4.1
- [Android] Exclude Microsoft Entra ID Copilot from NTP's voice and camera search

### Bug fixes

- [iOS] Fix **DefaultBrowserSettingEnabled** policy that didn't work
- [iOS] Fix the UI layout issue caused by changes in UIWindow `safeAreaInsets` leading to Webview content offset shift in certain situations
- [Android] Fix a bug related to policy **InPrivateModeAvailability**
- [Android] Fix SSO bug when a blocked link is opened from Outlook

### New policies

- [iOS & Android] Disable UIR prompt pop-up via **com.microsoft.intune.mam.managedbrowser.disabledFeatures** or **EdgeDisabledFeatures** policy
- [iOS & Android] Add CIDR (Classless Inter-domain Routing) support in AllowListURLs/BlockListURLs feature
- [iOS & Android] New **com.microsoft.intune.mam.managedbrowser.InternalPagesBlockList** policy to allow IT admin disable edge internal pages

### Enhancements

- [iOS] Avoid multiple auth prompt dialog for NTLMSSO management
- [iOS] Enhance URL blocklist in MAM with respect to policy description

## Version 127.0.2651.59: (Android and iOS): July 19, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.55 (Android): July 16, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.54 (iOS): July 16, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.46 (Android and iOS): July 12, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.40 (Android and iOS): July 10, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.30 (Android and iOS): July 2, 2024

Fixed various bugs and performance issues.
 
## Version 127.0.2651.19 (Android): June 27, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.5 (Android): June 21, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.55 (Android and iOS): June 13, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.50 (Android and iOS): June 11, 2024

Fixed various bugs and performance issues, general updates, new policies, and enhancements.

### General updates

- [iOS] Upgrade MS Tunnel SDK version 1.1.0
- [Android and iOS] Update OneAuth SDK to 2.3.1

### Bug fixes

- [Android] Scrolling screenshot will be disabled if Intune APP (App Protection Policy) is configured to block screenshot

### New policies

- [Android and iOS] Manage contextual search via policy `com.microsoft.intune.mam.managedbrowser.disabledFeatures=contextualsearch`
- [iOS] Introduce MDM policy **EdgeSharedDeviceSupportEnabled** to disable shared device mode

### Enhancements

- [Android and iOS] Remove [Copilot](https://copilot.microsoft.com/) from default allowlist so that you can manage access to [Copilot](https://copilot.microsoft.com/) via URLs blocklist.
- [iOS] Support Passkey on iOS. This feature is disabled by default. It can be enabled by turning on the flag `edge-iOS-enable-passkey-signin` from *Edge://flags*.

## Version 126.0.2592.42 (Android and iOS): June 6, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.38 (Android and iOS): June 4, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.23 (Android and iOS): May 28, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.12 (Android and iOS): May 23, 2024

Fixed various bugs and performance issues.

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
