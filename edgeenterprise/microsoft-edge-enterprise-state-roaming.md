---
title: "Microsoft Edge and Enterprise State Roaming"
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 02/14/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Microsoft Edge and Enterprise State Roaming"
---

# Microsoft Edge and Enterprise State Roaming

This article explains how Microsoft Edge participation in the Enterprise State Roaming (ESR) offering is changing to better support sync across platforms and devices.

> [!NOTE]
> This article applies to Microsoft Edge version 77 or later.

## Introduction

With Windows 10, [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) users gained the ability to securely synchronize their user settings and application settings data to the cloud. [Enterprise State Roaming (ESR)](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) provides users with a unified experience across their Windows devices and reduces the time needed for configuring a new device.

As part of Microsoft Edge adopting the Chromium platform, its sync solution is now disconnected from Windows sync framework. This affects the relationship of Microsoft Edge to the ESR offering.

> [!IMPORTANT]
> The new Microsoft Edge does not participate in the ESR offering.

## What’s changing with Microsoft Edge?

With the new Microsoft Edge, the sync solution isn’t tied to Windows sync ecosystem. This enables us to offer Microsoft Edge across all the platforms, such as Windows 7, Windows 8.1, iOS, Android and macOS. This also enables us to offer sync for non-primary accounts on Windows. In addition, we can ship Microsoft Edge at a more frequent and flexible release cadence than Windows. (For more information, see [Windows updates to support the next version of Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md). All these factors highlighted the need to re-assess Microsoft Edge participation in the ESR offering.

ESR is framed as a Windows product offering with promises about how data from Windows devices is handled, but Microsoft Edge sync will extend beyond Windows devices. And, as the data roams across these devices, it makes it difficult to define the Microsoft Edge sync offering in the context of ESR. To simplify how sync works and is managed, and to accommodate the changes that are highlighted, a decision was made to pull Microsoft Edge out of the ESR offering.

## Does this mean Enterprises will lose the abilities they had as part of ESR?

No. Microsoft Edge will continue to support most of the abilities provided in the ESR offering.

### Unified experience across devices and new device configuration time

When a user is signed into their windows device with an Azure Active Directory (Azure AD account), Microsoft Edge will implicitly inherit that Identity on first launch of the new browser.

After a user has explicitly consented to turning on sync in the new Microsoft Edge, the browser will sync all the browser data, such as favorites, passwords, and history. This ensures a unified experience across devices and reduces the time needed to personalize the browser.

### Separation of corporate and consumer data

Organizations are in control of their data, and there is no mixing of corporate data in a consumer cloud account or consumer data in an enterprise cloud account.

### Enhanced security

Data is automatically encrypted before leaving the user’s Windows 10 device by using Azure Information Protection, and data stays encrypted at rest in the cloud. All content stays encrypted at rest in the cloud, except for the namespaces, like settings names.

### Monitoring

We will provide control and visibility over who syncs settings in your organization and on which devices through integration with the Azure AD portal. This capability will be enabled in a future release.

### Management

Admins will be able to control which members in your organization can enable sync. See [Configure Microsoft Edge sync](microsoft-edge-enterprise-sync.md#configure-microsoft-edge-sync) and [Sync group policies](microsoft-edge-enterprise-sync.md#sync-group-policies). Additionally, users can turn sync on/off for each of their devices as well as toggle each data attribute individually for sync.

### Key management

The synchronization feature leverages Azure Information Protection (AIP) to protect the synchronized data for only the user and the enterprise admins. AIP supports both Microsoft managed (default) and bring your own key for cloud-key management. The cloud-key management strategy your organization uses is transparent to Microsoft Edge and has no impact on the synchronization feature.

> [!IMPORTANT]
> [Hold your own key (HYOK)](https://docs.microsoft.com/azure/information-protection/configure-adrms-restrictions) and the Active Directory Rights Management Service aren't supported.

## Summary of sync attributes

The following data attributes will sync in the new version of Microsoft Edge at first launch:

- Favorites
- Passwords
- Form-fill
- History
- Open tabs (sessions)
- Settings (preferences)
- Extensions

The preceding list of attributes is different than the attributes that could be synced in Microsoft Edge Legacy. (For details about Microsoft Edge Legacy settings, see [Windows 10 roaming settings](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-windows-settings-reference).) Users can selectively enable/disable these attributes using Microsoft Edge settings. Given the difference in attributes between the two versions (for example, history), users might be asked to give sync consent again.

> [!NOTE]
> Unlike Microsoft Edge Legacy, the new Microsoft Edge doesn't use Windows credential Manager for passwords and as a result, won't sync passwords with Internet Explorer or other apps that use Windows Credential manager.

## Terms of service

Terms of service for Microsoft Edge sync falls under the Microsoft software license viewable in Microsoft Edge at *edge://terms*.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md)