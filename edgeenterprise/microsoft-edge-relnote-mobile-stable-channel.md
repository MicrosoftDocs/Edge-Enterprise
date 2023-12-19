---
title: "Microsoft Edge release notes for Mobile Stable Channel"
ms.author: charlielin
author: dan-wesley
manager: alexyuan
ms.date: 12/19/2023
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

## Version 120.0.2210.84: December 19, 2023

Fixed various bugs and performance issues for Android.

## Version 120.0.2210.64: December 12, 2023

Fixed various bugs and performance issues for Android.

### Policy support

For more information, see [Manage Microsoft Edge on iOS and Android with Intune](/mem/intune/apps/manage-microsoft-edge).

MAM Policy to configure web data store.  **Note:** The Default key value for `com.microsoft.intune.mam.managedbrowser.PersistentWebsiteDataStore` is changed to "2".

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
<!-- Version 114.0.1823.37: June 2, 2023 to Version 113.0.1774.50: May 18, 2023 -->
<!-- Version 113.1774.36: May 8, 2023 to Version 112.0.1722.36: April 7, 2023 -->
<!-- Version 111.0.1661.43: March 18, 2023 to Version 109.0.1518.70: January 26, 2023 -->
<!-- Version Version 109.0.1518.58: January 18, 2023 to Version 108.0.1462.45: December 8, 2022  -->
<!-- Version 108.0.1462.43: December 7, 2022 to Version 106.0.1370.47: October 17, 2022 -->
<!-- Version 105.0.1343.38: September 13, 2022 to Version 101.0.1210.32: April 29, 2022 -->

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
