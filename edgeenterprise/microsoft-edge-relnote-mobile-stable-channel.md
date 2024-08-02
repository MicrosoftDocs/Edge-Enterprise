---
title: "Microsoft Edge release notes for Mobile Stable Channel"
ms.author: charlielin
author: dan-wesley
manager: alexyuan
ms.date: 08/02/2024
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

### General updates

- [iOS] Upgrade MS Tunnel SDK version 1.0.18
- [iOS] Upgrade Intune MAM SDK to version 19.4.1

### Bug fixes

- [iOS] Fix [DefaultBrowserSettingEnabled](/deployedge/microsoft-edge-mobile-policies#defaultbrowsersettingenabled) policy that didn't work
- [iOS] Fix the UI layout issue caused by changes in UIWindow safeAreaInsets leading to Webview content offset shift in certain situations

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

## Version 125.0.2535.96 (Android and iOS): June 11, 2024

Fixed various bugs and performance issues.

## Version 125.0.2535.87 (Android and iOS): June 5, 2024

Fixed various bugs and performance issues.

## Version 125.0.2535.72 (Android and iOS): May 27, 2024

Fixed various bugs and performance issues.

## Version 125.0.2535.60 (iOS): May 23, 2024

Fixed various bugs and performance issues, provide general updates, add new features and policies.

### General updates

- MS Tunnel SDK updated to 1.0.17.
- Upgrade Intune iOS SDK to 19.3.1, with working time support.

### New features

- Shared links feature appears in overflow menu in work account. 
- PAC policy now supports fail-close.
- Support certificate pinning via Intune, currently only supports limited number of Microsoft domains. Pending on Intune's improvements to support customizable cert-domain pair.
- Support of new iOS 17 relay proxy via policy `com.microsoft.intune.mam.managedbrowser.ProxyRelayUrl`.

### New Policies

- `com.microsoft.intune.mam.managedbrowser.ProfileAutoSwitchToWork` to resolve the conflict between Intune auto identity switch and Edge allow/block URL policies.
- Introduce MDM policy [EdgeCopilotEnabled](/deployedge/microsoft-edge-mobile-policies#edgecopilotenabled), to globally disable Copilot in Edge mobile, including the personal context.

## Version 125.0.2535.51 (Android): May 21, 2024

Fixed various bugs and performance issues, provide a general update, add new features and policies.

### General updates

- Upgrade the Intune Android SDK to 10.3.0, with working time support.

### New features

- Edge Android now supports kerberos/negotiate authentication on Android via an [external SPNEGO authenticator app](https://github.com/google/android-kerberos-authenticator) integrated with Android account management framework.
- Shared links feature appears in overflow menu in work account.

### New Policies

- Introduce the MDM policy [EdgeCopilotEnabled](/deployedge/microsoft-edge-mobile-policies#edgecopilotenabled), to globally disable Copilot in Edge mobile, including the personal context.


## Version 124.0.2478.105 (iOS): May 17, 2024

Fixed various bugs and performance issues.

## Version 124.0.2478.104 (Android): May 15, 2024

Fixed various bugs and performance issues.

## Version 124.0.2478.89 (iOS): May 8, 2024

Fixed various bugs and performance issues.

## Version 124.0.2478.87 (Android): May 7, 2024

Fixed various bugs and performance issues.

## Version 124.0.2478.71 (iOS): April 30, 2024

Fixed various bugs and performance issues.

## Version 124.0.2478.71 (Android): April 29, 2024

### Policy updates

- MDM policy  [edgenewtabpagelayout](/deployedge/microsoft-edge-mobile-policies#edgenewtabpagelayout) to manage New Tab Page layout settings.
- MDM policy [edgenewtabpagelayoutcustom](/deployedge/microsoft-edge-mobile-policies#edgenewtabpagelayoutcustom) to manage New Tab Page custom setting.
- MDM policy [edgenewtabpagelayoutuserselectable](/deployedge/microsoft-edge-mobile-policies#edgenewtabpagelayoutuserselectable) to manage whether the New Tab Page layout is selectable by users.

Fixed various bugs and performance issues.

## Version 124.0.2478.62 (Android): April 25, 2024

Fixed various bugs and performance issues.

### Bug fixes

- [Android] Fixed a bug where setting Edge as the default browser caused repetition, and the button became unresponsive.
- [Android] Fixed a bug in shared device mode where the sign-in process was getting hung on the loading screen.

## Version 124.0.2478.50 (Android and iOS): April 22, 2024

Made general updates, fixed various bugs and performance issues, added new features and policies.

### General updates

- [iOS] MS Tunnel updated to 1.0.15, added privacy manifest file to comply with Apple App Store requirements.
- [iOS] updated Citrix mVPN iOS SDK to 24.2.1
- [iOS] added 'protApp' parameter to Microsoft Bing Search resource token fetch request, so it is not blocked by the CA "requiring app protection" policy. This token is needed for Copilot in Edge
- [iOS] Intune SDK updated to 19.2.0

### Bug fixes

- [iOS] Fix disableFeatures policy bug for inPrivate mode, handle corner cases where inPrivate not disabled
- [Android] Fixed a bug in Guided switch

### New features

- [Android] Re-enable Kerberos authentication support on Android with an external Negotiate Authenticator app.
- [Android and iOS] Copilot in Edge mobile now properly supports school scenarios.
- [iOS] Shared Device Mode support
- [Android and iOS] In-flight, the "Shared Links" feature can be opened from the Edge overflow menu.

### Policy updates

- [Android and iOS] Introduce MDM policy [EdgeCopilotEnabled](/deployedge/microsoft-edge-mobile-policies#edgecopilotenabled), to globally disable Copilot in Edge mobile, including the personal context.
- [Android and iOS] MDM policy [HideFirstRunExperience](/deployedge/microsoft-edge-mobile-policies#hidefirstrunexperience), to hide first run experience.
- [Android and iOS] MDM policy [DefaultBrowserSettingEnabled](/deployedge/microsoft-edge-mobile-policies#defaultbrowsersettingenabled), to disable default browser settings pop-up.
- [Android] MDM policy [PreventTyposquattingPromptOverride](/deployedge/microsoft-edge-mobile-policies#preventtyposquattingpromptoverride), to prevent bypassing Edge Website Typo Protection prompts for sites.
- [Android] MDM policy [TyposquattingAllowListDomains](/deployedge/microsoft-edge-mobile-policies#typosquattingallowlistdomains), to configure the list of domains for which Edge Website Typo Protection won't trigger warnings.

<!-- ranges cut out for mobile stable archive -->
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
