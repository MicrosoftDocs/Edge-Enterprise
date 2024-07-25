---
title: "Configure Microsoft Edge enterprise sync"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 07/18/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Admin and user options for configuring Microsoft Edge to sync favorites, passwords, and other browser data."
---

# Configure Microsoft Edge enterprise sync

This article explains how admins can configure Microsoft Edge to sync user favorites, passwords, and other browser data across all signed-in devices.

> [!NOTE]
> Applies to Microsoft Edge on Chromium, version 77 or later unless otherwise noted.

## Introduction

Microsoft Edge sync enables users to access their browsing data across all their signed-in devices. Users can sync the following data:

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
> If a user is experiencing a sync issue, they might need to reset sync in **Settings** > **Profiles** > **Sync** > **Reset sync**.

## Prerequisites

The following prerequisites apply to Microsoft Edge enterprise sync:

- A Microsoft Edge version that supports the desired sync functions.
- An active subscription to a cloud service in a supported environment.
- An Enterprise Mobility + Security service plan, specifically A3, A5, E3, E5, G3, or G5.

Note that Department of Defense (DoD) and Government Community Cloud (GCC) subscriptions aren't supported at this time. For more information, refer to [Microsoft Edge enterprise sync FAQ](/deployedge/microsoft-edge-enterprise-sync-faq#does-microsoft-edge-support-government-community-cloud-gcc-high-and-azure-government-department-of-defense-dod-cloud-compliance).  

## Supported environments

Microsoft Edge sync for Microsoft Entra accounts is available for any of the following subscriptions:

- Microsoft Entra ID (P1 or P2)
  
  > [!NOTE]
  > Customers that only have Microsoft Entra ID P1 or P2 must enable Microsoft Entra Enterprise State Roaming (ESR). Microsoft Edge sync isn't part of ESR, but ESR is required to provide the AIP functionality that's needed for the P1 and P2 configurations. To learn more, see the [Enable Enterprise State Roaming in Microsoft Entra ID](/azure/active-directory/devices/enterprise-state-roaming-enable) article.

- Microsoft 365 Business Premium, Business Standard, or Business Basic

  > [!NOTE]
  > Business Basic or Business Standard is supported, but existing tenants need to be backfilled with the RMS_S_BASIC service plan needed by AIP. Customers that are having a sync issue should review [Diagnose and fix Microsoft Edge sync issues](/deployedge/microsoft-edge-troubleshoot-enterprise-sync) and [Reset Microsoft Edge data in the cloud](/deployedge/edge-learnmore-reset-data-in-cloud) before filing a support request. Business Premium includes Microsoft Entra ID  Plan 1 and Edge Enterprise Sync Services are available, see [Microsoft 365 Small and Medium-sized Businesses](https://aka.ms/M365BusinessPlans).

- Office 365 E1 and above
- All EDU subscriptions, including:
  - Microsoft Apps for Students or Faculty
  - Exchange Online for Students or Faculty
  - O365 A1 or above
  - Microsoft 365 A1 or above
  - Azure Information Protection P1 or P2 for Students or Faculty

## Sync group policies

Admins can use the following group policies to configure and manage Microsoft Edge sync:

- [SyncDisabled](./microsoft-edge-policies.md#syncdisabled): Disables data synchronization.  This policy disables cloud synchronization only and has no effect on the RoamingProfileSupportEnabled policy.
- [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled): Disables saving browsing history and sync and open tabs sync.
- [AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): When this policy is set to disabled, history sync will also be disabled.
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): Configure the list of data types that are excluded from synchronization. Use this policy to limit the type of data uploaded to the Microsoft Edge synchronization service.
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage. The settings stored in Microsoft Edge profiles (favorites and preferences) are also saved to a file stored in the Roaming user profile folder (or the location specified by the administrator.) For more information, see [On-premises sync for Active Directory (AD) users](./microsoft-edge-on-premises-sync.md).
- [ForceSync](/deployedge/microsoft-edge-policies#forcesync): Force synchronization of browser data and don't show the sync consent prompt. Users can't disable this policy.

## Use Azure Information Protection to configure Microsoft Edge sync

Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service. When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing. The protection service might be activated automatically, by using PowerShell, or by using the Azure portal. For more information and instructions on how to enable AIP, see [Activating the protection service from Azure Information Protection (AIP)](/azure/information-protection/activate-office365).

> [!CAUTION]
> Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP. Any onboarding control policy that's used to restrict Microsoft Edge sync will also restrict other applications from protecting content using AIP.

### Control user onboarding for a phased deployment

You can use the [Set-AipServiceOnboardingControlPolicy](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps) cmdlet to set the policy that controls user on-boarding for Azure Information Protection. If sync still isn't available after all the specified users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps) PowerShell cmdlet. For more information, see [Configuring onboarding controls for a phased deployment](/azure/information-protection/activate-service#configuring-onboarding-controls-for-a-phased-deployment).

## Microsoft Edge and Enterprise State Roaming (ESR)

Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Microsoft Entra Enterprise State Roaming. However, Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key. For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## See also

- [Diagnose and fix Microsoft Edge sync issues](microsoft-edge-troubleshoot-enterprise-sync.md)
- [Microsoft Edge enterprise sync FAQ](microsoft-edge-enterprise-sync-faq.md)
- [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [What is Azure Information Protection?](/azure/information-protection/what-is-information-protection)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
