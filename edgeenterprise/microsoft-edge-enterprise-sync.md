---
title: "Configure Microsoft Edge enterprise sync"
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 05/16/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Admin and user options for configuring Microsoft Edge to sync favorites, passwords, and other browser data."
---

# Configure Microsoft Edge enterprise sync

This article explains how admins can configure Microsoft Edge to sync user favorites, passwords, and other browser data across all signed-in devices.
<!---
If you're not an admin, use  [Sign in to sync Microsoft Edge across devices](https://support.microsoft.com/microsoft-edge/sign-in-to-sync-microsoft-edge-across-devices-e6ffa79b-ed52-aa32-47e2-5d5597fe4674) as a guide to learn how to sign-in and sync Microsoft Edge across devices. ---->

> [!NOTE]
> Applies to Microsoft Edge on Chromium, version 77 or later unless otherwise noted.

## Introduction

Microsoft Edge sync enables users to access their browsing data across all their signed-in devices. The following data can be synchronized:

- Favorites
- Passwords
- Addresses and more (form-fill)
- Collections
- Settings
- Extensions
- Open tabs (available in Microsoft Edge version 88 or later)
- History (available in Microsoft Edge version 88 or later)

> [!NOTE]
> Additional device connectivity and configuration data (such as device name, device make,  and device model) is uploaded to support sync functionality.

### Sync functionality and user sync configuration

After sync is configured, sync functionality is enabled via user consent. Users can turn sync on or off for each of the supported data types. For more information, see [Sign in to sync Microsoft Edge across devices](https://support.microsoft.com/microsoft-edge/sign-in-to-sync-microsoft-edge-across-devices-e6ffa79b-ed52-aa32-47e2-5d5597fe4674).

> [!NOTE]
> If a user is experiencing a sync issue, they might need to reset sync in **Settings** > **Profiles** > **Reset sync**.

## Prerequisites

The following prerequisites apply to Microsoft Edge enterprise sync:

- Microsoft Edge version that supports the desired sync functions
- Subscription to a cloud service in a supported environment
- Azure Information Protection (AIP) (P1 or P2)

## Supported environments

Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:

- Azure AD Premium (P1 or P2)
  
  > [!NOTE]
  > Customers that only have Azure AD P1 or P2 need to enable Azure AD Enterprise State Roaming to provide AIP, which is required for Microsoft Edge sync. To learn more, see the [Enable Enterprise State Roaming in Azure Active Directory](/azure/active-directory/devices/enterprise-state-roaming-enable) article.

- Microsoft 365 Business Premium, Business Standard, or Business Basic

  > [!NOTE]
  > Business Basic is supported, but some existing tenants need to be backfilled with the RMS_S_BASIC service plan needed by AIP. Customers can file a support request if they need to backfill a tenant.

- Office 365 E1 and above
- All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, Microsoft 365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)

## Sync group policies

Admins can use the following group policies to configure and manage Microsoft Edge sync:

- [SyncDisabled](./microsoft-edge-policies.md#syncdisabled): Disables data synchronization.  This policy disables cloud synchronization only and has no effect on the RoamingProfileSupportEnabled policy.
- [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled): Disables saving browsing history and sync and open tabs sync.
- [AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): When this policy is set to disabled, history sync will also be disabled.
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): Configure the list of data types that are excluded from synchronization. Use this policy to limit the type of data uploaded to the Microsoft Edge synchronization service.
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage. The settings stored in Microsoft Edge profiles (favorites and preferences) are also saved to a file stored in the Roaming user profile folder (or the location specified by the administrator.) For more information, see [On-premises sync for Active Directory (AD) users](./microsoft-edge-on-premises-sync.md).
- [ForceSync](/deployedge/microsoft-edge-policies#forcesync): Force synchronization of browser data and don't show the sync consent prompt. Users can't disable this policy.

## Configure Microsoft Edge sync

Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service. When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing. For more information and instructions on how to enable AIP, see [Activating the protection service from Azure Information Protection (AIP)](/azure/information-protection/activate-office365).

> [!CAUTION]
> Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP. Any onboarding control policy that's used to restrict Microsoft Edge sync will also restrict other applications from protecting content using AIP.

To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps) for those users. If sync still isn't available after all the necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps) PowerShell cmdlet.

## Microsoft Edge and Enterprise State Roaming (ESR)

Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming. However, the Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key. For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## See also

- [Diagnose and fix Microsoft Edge sync issues](microsoft-edge-troubleshoot-enterprise-sync.md)
- [Microsoft Edge enterprise sync FAQ](microsoft-edge-enterprise-sync-faq.md)
- [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)