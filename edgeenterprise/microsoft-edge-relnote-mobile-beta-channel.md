---
title: "Microsoft Edge release notes for Mobile Beta Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 03/12/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Microsoft Edge release notes for Mobile Beta Channel"
---

# Release notes for Microsoft Edge Mobile Beta Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Mobile Beta Channel.
<!---
Archived versions of these release notes are available at [Archived release notes for Microsoft Edge Beta Channel](./microsoft-edge-relnote-archive-beta-channel.md). --->

> [!NOTE]
> Microsoft Edge Web Platform constantly evolves to improve user experience, security, and privacy. To learn more, see [Site compatibility-impacting changes coming to Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## Version 123.0.2420.33 (Android and iOS): March 12, 2024

Fixed various bugs and performance issues.

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
