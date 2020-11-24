---
title: "Configure and troubleshoot Microsoft Edge sync"
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 11/24/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Configure and troubleshoot Microsoft Edge sync"
---

# Configure and troubleshoot Microsoft Edge sync

This article provides troubleshooting steps for the most commonly encountered sync issues. It also includes the recommended tools for gathering the logs needed for troubleshooting.

> [!NOTE]
> Applies to Microsoft Edge version 77 and above unless otherwise noted.

## Overview

Microsoft Edge sync enables users to access their browsing data across all their signed-in devices. The data supported by sync includes:

- Favorites
- Passwords
- Addresses and more (form-fill)
- Collections
- Settings
- Extension
- Open tabs
- History

Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.

> [!NOTE]
> Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.

## Prerequisites

Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:

- Azure AD Premium (P1 and P2)
- M365 Business Premium
- Office 365 E1 and above
- Azure Information Protection (AIP) (P1& P2)
- All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)

## Sync group policies

You can use the following group policies to configure and manage Microsoft Edge sync:

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.
- [AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): When this policy is set to disabled, history sync will also be disabled.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage. For more information, see [On-premises sync for Active Directory (AD) users](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).
- [ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn sync on by default and do not require user consent to sync.  

## Configure Microsoft Edge sync

Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service. When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing. Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).

To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) for those users. If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true)  PowerShell cmdlet.

> [!CAUTION]
> Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP. In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.

## Microsoft Edge and Enterprise State Roaming

The new Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming. However, the new Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key. For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).

## Troubleshoot sync issues

This section provides troubleshooting steps for the most encountered sync issues. It also includes the recommended tools for gathering the logs needed for troubleshooting.

### Identity issues versus sync issues

A popular use case for maintaining user identity in the browser is to support sync. For this reason, identity issues are frequently confused with sync issues. Understand the difference between identity and sync issue before you start troubleshooting sync.

Before you treat an issue as a sync issue, check to see if the user is signed into the browser with a valid account. If you encounter an identity issues as an account not properly signing in or the wrong account appearing as the user’s default account, refer to the [Identity troubleshooting guide](https://dev.azure.com/microsoft/Edge/_wiki/wikis/Edge.wiki/48883/Identity-TSG).

The next screenshot shows an example of an identity error found in *edge://sync-internals*.

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Identity error":::

### Common sync issues

#### Issue: Can't access M365 or Azure Information Protection subscription

Do you have a previous M365 or Azure Information Protection (AIP) subscription that expired and then replaced with a new subscription? If so, then the tenant ID has changed and the service data needs to be reset. See the instructions for resetting data in the **Cryptographer error encountered** issue.

#### Issue: “Sync is not available for this account.”

If this error is encountered for an Azure Active Directory account, or if DISABLED_BY_ADMIN appears in *edge://sync-internals*, follow the steps in the next procedure sequentially until the problem is fixed.

> [!NOTE]
> Because the source of this error is usually requires a configuration change in an Azure Active Directory tenant, these troubleshooting steps can only performed by a tenant admin and not by end users.

1. Verify that the enterprise tenant has a supported M365 subscription. The current list of available subscription types is [provided here](https://docs.microsoft.com/azure/information-protection/activate-office365). If the tenant doesn't have a supported subscription, they can either purchase Azure Information Protection separately, or upgrade to one of the supported subscriptions.
2. If a supported subscription is available, verify that the tenant has Azure Information Protection (AIP) available. The instructions for checking the AIP status and, if necessary, activating AIP are [here](https://docs.microsoft.com/azure/information-protection/activate-office365).
3. If step 2 shows that AIP is active but sync still doesn't work, turn on Enterprise State Roaming (ESR). The instructions for enabling ESR are [here](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-enable). Note that ESR does not need to stay on. You can turn ESR off if this step fixes the issue.
4. Confirm that Azure Information Protection is not scoped via an onboarding policy. You can use the [Get-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps)  PowerShell applet to see if scoping is enabled. The next two examples show an unscoped configuration and a configuration scoped to a specific security group.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-unscoped-cfg.png" alt-text="Unscoped configuration":::

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg.png" alt-text="Scoped configuration":::

   If scoping is enabled, the affected user should either be added to the security group for the scope, or the scope should be removed. In the example below, onboarding has scoped AIP to the indicated security group and the scoping should be removed with the [Set-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell applet.

5. Confirm that the IPCv3Service is turned on in the tenant. The [Get-AadrmConfiguration](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps)  PowerShell applet shows the status of the service.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="Check to see if IPCv3Service is enabled.":::

6. If the issue isn't fixed, collect logs via OCV and them to Microsoft Edge team.

#### Issue: Stuck at "Setting up sync..." or “Couldn’t connect to the sync server. Retrying…”

1. Try to sign out and then sign in.
2. Go to *edge://sync-internals*. If under the "**Type info**" section the following error is present, then  skip to the following issue, **Cryptographer error encountered**.

   `"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered"`

3. Try pinging the server endpoint. The server endpoint for a client is available in *edge://sync-internals*. The next screenshot shows endpoint information under **Environment Info**.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-endpoint-info.png" alt-text="Endpoint information":::

4. If the server endpoint is empty, or if server cannot be pinged and a firewall is present in the environment, confirm that the necessary service endpoints are available to the client computer.

   - Edge sync service endpoints:
     - [https://enterprise.activity.windows.com](https://enterprise.activity.windows.com)
     - [https://edge.activity.windows.com](https://edge.activity.windows.com)
    - Azure Information Protection endpoints:
      - [https://api.aadrm.com](https://api.aadrm.com) (for most tenants)
      - [https://api.aadrm.de](https://api.aadrm.de) (for tenants in Germany)
      - [https://api.aadrm.cn](https://api.aadrm.cn) (for tenants in China)
   - [Windows Notification Service endpoints](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).

5. If the issue still isn't fixed, collect logs via OCV and send them to the Microsoft Edge team.

### Issue: Cryptographer error encountered

This error is visible under **Type info** in *edge://sync-internals* and may mean that the user's service side data needs to be reset. The next screenshot shows an example of a cryptographer error.

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-crypto-error.png" alt-text="Cryptographer error.":::

1. Restart Edge and navigate to *edge://sync-internals* and check the “**AAD Account Key Status**” section
   - "Success" in "Last MIP Result": the cryptographer error means server data might be encrypted with a lost key. Data reset is needed to resume sync.
   - "No permissions" in "Last MIP Result": It is possibly caused by alias change or tenant subscription changes. Data reset is needed to resume sync.
   - Other errors may mean server configuration issues.
2. If data reset is needed, please contact Edge Support.

#### Issue: “Sync has been turned off by your administrator.”

Make sure that the [SyncDisabled policy](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled)  is not set.

## Frequently Asked Questions

### SECURITY and SERVER/DATA COMPLIANCE

#### Is the synced data encrypted?

The data is encrypted in transport using TLS 1.2 or greater. All data types are additionally encrypted at rest in Microsoft's service using AES128. All data types except those used for open tab and history sync are additionally encrypted before leaving the user’s device with keys managed via the [Azure Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.

#### Why don’t open tab and history data have additional client-side encryption?

To reduce resource utilization on end user devices, history data is generated server-side based on open tab roaming data. This process would not be possible with client-side encryption of this data. To disable open tab and history sync, apply the [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) or [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) policies.

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

Enterprise sync depends on[Azure Information Protection](https://azure.microsoft.com/services/information-protection/), which is not available in all M365 subscriptions.

#### Is Microsoft Edge sync based on Enterprise State Roaming?

No. ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR. For more information, see [Microsoft Edge Sync](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) and [Microsoft Edge and Enterprise State Roaming](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming).

#### Will Microsoft Edge ever support syncing between Microsoft Edge and IE?

There are no plans to support this syncing. If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).

#### Will Microsoft Edge sync with Microsoft Edge Legacy?

No, it won't. We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the Microsoft Edge. We will ensure that existing data is migrated to the Microsoft Edge. Users will also be able to import data from browser of their choice. This also means that new Microsoft Edge browser won't have a way to sync with IE.

### MANAGING SYNC

#### Is it possible to stop my users from syncing with a personal tenant?

Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.

## See also

- [Microsoft Edge Enterprise Sync](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
