---
title: "Microsoft Edge release notes for Mobile Stable Channel"
ms.author: charlielin
author: dan-wesley
manager: alexyuan
ms.date: 09/19/2023
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

## Version 117.0.2045.33: September 15, 2023

Fixed various bugs and performance issues.

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
<!-- Version 113.1774.36: May 8, 2023 to Version 112.0.1722.36: April 7, 2023 -->
<!-- Version 111.0.1661.43: March 18, 2023 to Version 109.0.1518.70: January 26, 2023 -->
<!-- Version Version 109.0.1518.58: January 18, 2023 to Version 108.0.1462.45: December 8, 2022  -->
<!-- Version 108.0.1462.43: December 7, 2022 to Version 106.0.1370.47: October 17, 2022 -->
<!-- Version 105.0.1343.38: September 13, 2022 to Version 101.0.1210.32: April 29, 2022 -->

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
