---
title: "Archived - release notes for Microsoft Edge Mobile Stable Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 05/22/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Archived release notes for Microsoft Edge Mobile Stable Channel"
---

# Archived - release notes for Microsoft Edge Mobile Stable Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Mobile Edge Stable Channel. All the security updates are listed [here](microsoft-edge-relnotes-security.md).

<!-- Version 122.0.2365.99 (Android and iOS): March 18, to 2024 Version 121.0.2277.84 (Android): January 29, 2024 -->

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

<!-- Version 119.0.2151.107: December 6, 2023 to Version 119.0.2151.46: November 7, 2023  -->
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
## Version 118.0.2088.81: November 1, 2023

Fixed various bugs and performance issues for iOS.

## Version 118.0.2088.68: October 25, 2023

Fixed various bugs and performance issues for iOS.

## Version 118.0.2088.66: October 24, 2023

Fixed various bugs and performance issues for Android.

## Version 118.0.2088.60: October 21, 2023

Fixed various bugs and performance issues for iOS.

## Version 118.0.2088.52: October 18, 2023

Fixed various bugs and performance issues.

### Feature update

- **Microsoft Tunnel for MAM strict mode.** When strict mode is turned on by MAM policy `com.microsoft.intune.mam.managedbrowser.StrictTunnelMode`, the network will be blocked until the tunnel is connected.

- **Overflow menu enablement for locked view mode.** Originally, overflow menu is disabled when Edge locked view mode is turned on by MDM policy `EdgeLockedViewMode=true`. Now, the overflow menu is enabled when Edge locked view mode is turned on.

- **Support for saving logs to local devices.** For more information, see [Diagnostic logs](/mem/intune/apps/manage-microsoft-edge#diagnostic-logs)

### Policy support

Allow proceeding from the SSL warning page:

- MAM: com.microsoft.intune.mam.managedbrowser.SSLErrorOverrideAllowed (Android only)
- MDM: [SSLErrorOverrideAllowed](/deployedge/microsoft-edge-mobile-policies#sslerroroverrideallowed)

Control the behavior of opening external apps:

- MAM: [com.microsoft.intune.mam.managedbrowser.OpeningExternalApps](/mem/intune/apps/manage-microsoft-edge#block-opening-external-apps)

## Version 117.0.2045.65: October 11, 2023

Fixed various bugs and performance issues.

## Version 117.0.2045.53: October 6, 2023

Fixed various bugs and performance issues for Android.

<!-- Version 117.0.2045.33: September 15, 2023 to Version 116.0.1938.64: August 30, 2023  -->
## Version 117.0.2045.33: September 15, 2023

Fixed various bugs and performance issues for iOS.

### Feature update

- **Support for iOS 17.** Microsoft Edge for iOS supports iOS 17.

- **Shared Links feature.** This feature is released in Edge for Android as a public preview. By default, the shared links feature is turned off. It can be turned on by enabling the shared links flag in `Edge://flags`.

- **Edge shopping/coupons can be managed by MAM policy.** For example, to enable coupons: `com.microsoft.intune.mam.managedbrowser.disabledFeatures=coupons`.

- **New policy to manage the "import password" feature in MAM and MDM.** The following settings are available to manage this feature:

  - MAM: `com.microsoft.intune.mam.managedbrowser.disableImportPasswords`
  - MDM: `EdgeImportPasswordsDisabled`

- **Improvements to Bing Chat Enterprise for iOS and Android** For example, Bing Image Creator and Bing Visual Search.

## Version 116.0.1938.72: September 5, 2023

Fixed various bugs and performance issues for iOS.

### Feature update

This iOS version introduces a new MAM policy. This MAM policy controls whether Bing Chat Enterprise (BCE) can access content protected by an Intune App protection policy. When the policy is set to true, users can copy text from a protected web page and paste it into BCE. BCE can also access the page if users ask a question like "Summarize the current web page". The policy and its settings are as follows:<br>
`com.microsoft.intune.mam.managedbrowser.ChatAllowManagedContent=true (default)/false`.

## Version 116.0.1938.64: August 30, 2023

Fixed various bugs and performance issues.

### Feature update

- **Bing Chat Enterprise (BCE)** is available on Edge mobile for iOS and Android. By default, Bing Chat Enterprise is turned on. For detailed information about how to manage BCE, see [Bing Chat Enterprise](/mem/intune/apps/manage-microsoft-edge#bing-chat-enterprise).

<!-- Version 116.0.1938.56: August 21, 2023, to Version 115.0.1901.183: July 22, 2023 -->
## Version 116.0.1938.56: August 21, 2023

Fixed various bugs and performance issues for iOS.

### Feature updates

- Bing Chat Enterprise (BCE) is available on Edge mobile. By default, Bing Chat Enterprise is turned off. It can be turned on via Intune MAM policy `com.microsoft.intune.mam.managedbrowser.Chat=true`.

- The **Open in Microsoft Edge** option is available for saving files to OneDrive (Android).

- Brand info (logo) of New Tab Page (NTP) is now pulled from MS Graph. If you only configure brand logo in the Intune portal, you must also configure it in the Azure portal. For more information, see [Add company branding - Basics](/azure/active-directory/fundamentals/how-to-customize-branding#basics).

- InPrivate mode can be managed by Mobile Device Management (MDM) Policy setting for [InPrivateModeAvailability](/deployedge/microsoft-edge-mobile-policies#inprivatemodeavailability).

## Version 116.0.1938.53: August 21, 2023

Fixed various bugs and performance issues for Android.

## Version 115.0.1901.187: July 27, 2023

Fixed various bugs and performance issues for iOS.

## Version 115.0.1901.183: July 22, 2023

Fixed various bugs and performance issues for Android.

This release contains several security fixes for Android. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).


<!-- Version 114.0.1823.37: June 2, 2023 to Version 113.0.1774.50: May 18, 2023 -->
## Version 114.0.1823.37: June 2, 2023

Fixed various bugs and performance issues.

### Policy update

- **iOS Website data store access.** Currently, the persistent data store is only statically used by personal accounts. Because work or school accounts can't use this data store, browsing data rather than cookies are lost when their sessions end. This new policy lets organizations access the data store dynamically, which persists browsing data for work or school accounts, giving users a better browsing experience. For more information, see this policy in [Manage Microsoft Edge on iOS and Android with Intune](/mem/intune/apps/manage-microsoft-edge#ios-website-data-store).

## Version 113.0.1774.50: May 18, 2023

Fixed various bugs and performance issues.

This release contains several security fixes for Android. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

<!-- Version 113.1774.36: May 8, 2023 to Version 112.0.1722.36: April 7, 2023 -->
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


<!-- Version 111.0.1661.43: March 18, 2023 to Version 109.0.1518.70: January 26, 2023 -->
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

<!-- Version 109.0.1518.58: January 18, 2023 to Version 108.0.1462.45: December 8, 2022  -->
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

## Version 104.0.1293.58: August 16, 2022

Fixed various bugs.

### Feature updates

- **Support for disabling of inPrivate browsing and Password feature (iOS and Android).**  Before Microsoft Edge 104, Edge for iOS and Android disabled InPrivate browsing and Password (prompts to save passwords for the user) by default when only allow Work or School Accounts is configured.<br><br>
Starting with Microsoft Edge 104, you have more flexibility because InPrivate and Password won't be disabled by default when only allow Work or School Accounts is configured. Instead, you can decide whether to disable InPrivate browsing or Password by configuring the **com.microsoft.intune.mam.managedbrowser.disabledFeatures** key. For more information, see [Disable specific features](/mem/intune/apps/manage-microsoft-edge#disable-specific-features).

## Version 103.1264.53: July 1, 2022

Fixed various bugs.

## Version 103.0.1264.38: June 30, 2022

Fixed various bugs.

## Version 102.0.1245.30: May 31, 2022

Fixed various bugs.

### Feature updates

- **Support switching network stack between Chromium and iOS (iOS only).** The [NetworkStackPref](/mem/intune/apps/manage-microsoft-edge#switch-network-stack-between-chromium-and-ios) policy lets you choose the network preference for Microsoft Edge for iOS.

### Policy updates

#### New policies

- [NetworkStackPref](/mem/intune/apps/manage-microsoft-edge#switch-network-stack-between-chromium-and-ios) - Choose the network preference for Microsoft Edge for iOS

## Version 101.0.1210.43: May 9, 2022

Fixed various bugs.

## Version 101.0.1210.32: April 29, 2022

Fixed various bugs.

### Feature updates

- **Read Aloud: background play and play in silent mode (iOS and Android)**
  - When playing in the background, users can control Read Aloud (pause, resume, play forwards, or play backwards) via the notification panel and lock screen.
  - When a user switches tabs in Microsoft Edge while using Read Aloud, they can use a floating control bar to pause, resume, or close Read Aloud.
  - When a device's silent toggle is on, it doesn't affect Read Aloud playback as long as media volume is turned up.
  
