---
title: "Configure Microsoft Edge enterprise sync"
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 02/17/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Admin and user configuration options for Microsoft Edge sync"
---

# Configure Microsoft Edge enterprise sync

This article explains how to configure and use Microsoft Edge to sync user favorites, passwords, and other browser data across all signed-in devices.

> [!NOTE]
> Applies to Microsoft Edge version 77 or later unless otherwise noted.

## Overview

Microsoft Edge sync enables users to access their browsing data across all their signed-in devices. The data supported by sync includes:

- Favorites
- Passwords
- Addresses and more (form-fill)
- Collections
- Settings
- Extension
- Open tabs (available in Microsoft Edge version 88)
- History (available in Microsoft Edge version 88)

Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above. If a user is experiencing a sync issue they might need to reset sync in **Settings** > **Profiles** > **Reset sync**.

> [!NOTE]
> Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.

## Prerequisites

Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:

- Azure AD Premium (P1 or P2)
- M365 Business Premium
- Office 365 E1 and above
- Azure Information Protection (AIP) (P1 or P2)
- All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)

## Sync group policies

Admins can use the following group policies to configure and manage Microsoft Edge sync:

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.
- [AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): When this policy is set to disabled, history sync will also be disabled.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage. For more information, see [On-premises sync for Active Directory (AD) users](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).
- [ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn on sync by default and do not require user consent to sync.  

## Configure Microsoft Edge sync

Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service. When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing. Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).

To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) for those users. If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true)  PowerShell cmdlet.

> [!CAUTION]
> Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP. In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.

## Microsoft Edge and Enterprise State Roaming (ESR)

Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming. However, the Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key. For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## Frequently Asked Questions

### SECURITY and SERVER/DATA COMPLIANCE

#### Is the synced data encrypted?

The data is encrypted in transport using TLS 1.2 or greater. All data types are additionally encrypted at rest in Microsoft's service using AES128. All data types except those used for open tab and history sync are additionally encrypted before leaving the user’s device with keys managed via the [Azure Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.

#### Why don’t open tab and history data have more client-side encryption?

To reduce resource utilization on end-user devices, history data is generated server-side based on open tab roaming data. This process would not be possible with client-side encryption of this data. To disable open tab and history sync, apply the [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) or [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) policies.

#### Can tenant admins bring their own key?

Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).

#### Where is Microsoft Edge sync data stored?

Synced data for Azure AD accounts is stored in secure servers according to the tenant ID. For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.

#### Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?

No.

#### What terms of service does enterprise sync fall under?

Terms of service for Microsoft Edge sync falls under the Microsoft software license viewable in Microsoft Edge at *edge://terms*. Your Azure AD subscription and terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).

#### Does Microsoft Edge support Government Community Cloud (GCC) High compliance?

Not today. For customers in the GCC High cloud, Microsoft Edge sync is disabled.

### APPLYING SYNC

#### Why isn’t Microsoft Edge sync supported in all M365 subscriptions?

Enterprise sync depends on [Azure Information Protection](https://azure.microsoft.com/services/information-protection/), which is not available in all M365 subscriptions.

#### Is Microsoft Edge sync based on Enterprise State Roaming?

No. ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR. For more information, see [Microsoft Edge Sync](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) and [Microsoft Edge and Enterprise State Roaming](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming).

#### Will Microsoft Edge ever support syncing between Microsoft Edge and IE?

There are no plans to support this syncing. If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).

#### Will Microsoft Edge sync with Microsoft Edge Legacy?

No, it won't. We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the Microsoft Edge. We will ensure that existing data is migrated to the Microsoft Edge. Users will also be able to import data from browser of their choice, which also means that Microsoft Edge won't have a way to sync with IE.

### MANAGING SYNC

#### Is it possible to stop my users from syncing with a personal tenant?

Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.

## See also

- [Microsoft Edge Enterprise Sync](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
