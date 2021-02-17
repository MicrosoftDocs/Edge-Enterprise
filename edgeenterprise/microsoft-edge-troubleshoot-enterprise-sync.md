---
title: "Diagnose and fix Microsoft Edge sync issues"
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 02/17/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Guidance and tools an Microsoft Edge admin can use to troubleshoot and fix common enterprise sync issues"
---

# Diagnose and fix Microsoft Edge sync issues

This article provides troubleshooting guidance for the most commonly encountered sync issues. It also includes the recommended tools for gathering the logs needed for troubleshooting a sync issue. If a user is experiencing an issue syncing browser data across their devices they can try resetting sync. [Learn more](edge-learnmore-reset-data-in-cloud.md)

> [!NOTE]
> Applies to Microsoft Edge version 77 or later unless otherwise noted.

## Identity issues versus sync issues

Before you begin it's important to understand the difference between identity issues and sync issues. A popular use case for maintaining user identity in the browser is to support sync. For this reason, identity issues are frequently confused with sync issues. Understand the difference between identity and sync issue before you start troubleshooting sync.

Before you treat an issue as a sync issue, check to see if the user is signed into the browser with a valid account.

The next screenshot shows an example of an identity error. The error is "**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea**", which is found in *edge://sync-internals* under **Credentials**:

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Last Token Error EDGE_AUTH_ERROR: 3,54, 3ea":::

## Common sync issues

### Issue: Can't access M365 or Azure Information Protection subscription

Do you have a previous M365 or Azure Information Protection (AIP) subscription that expired and then replaced with a new subscription? If so, then the tenant ID has changed and the service data needs to be reset. See the instructions for resetting data in the **Cryptographer error encountered** issue.
 
### Issue: “Sync is not available for this account.”

If this error is encountered for an Azure Active Directory account, or if DISABLED_BY_ADMIN appears in *edge://sync-internals*, follow the steps in the next procedure sequentially until the problem is fixed.

> [!NOTE]
> Because the source of this error is usually requires a configuration change in an Azure Active Directory tenant, these troubleshooting steps can only performed by a tenant admin and not by end users.

1. Verify that the enterprise tenant has a supported M365 subscription. The current list of available subscription types is [provided here](https://docs.microsoft.com/azure/information-protection/activate-office365). If the tenant doesn't have a supported subscription, they can either purchase Azure Information Protection separately, or upgrade to one of the supported subscriptions.
2. If a supported subscription is available, verify that the tenant has Azure Information Protection (AIP) available. The instructions for checking the AIP status and, if necessary, activating AIP are [here](https://docs.microsoft.com/azure/information-protection/activate-office365).
3. If step 2 shows that AIP is active but sync still doesn't work, turn on Enterprise State Roaming (ESR). The instructions for enabling ESR are [here](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-enable). Note that ESR does not need to stay on. You can turn off ESR if this step fixes the issue.
4. Confirm that Azure Information Protection is not scoped via an onboarding policy. You can use the [Get-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps)  PowerShell applet to see if scoping is enabled. The next two examples show an unscoped configuration and a configuration scoped to a specific security group.

   ```powershell
    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False 
   ```

   ```powershell

    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False f1488a05-8196-40a6-9483-524948b90282   All
   ```


   If scoping is enabled, the affected user should either be added to the security group for the scope, or the scope should be removed. In the example below, onboarding has scoped AIP to the indicated security group and the scoping should be removed with the [Set-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell applet.

5. Confirm that the IPCv3Service is turned on in the tenant. The [Get-AadrmConfiguration](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps)  PowerShell applet shows the status of the service.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="Check to see if IPCv3Service is enabled.":::

6. If the issue isn't fixed, contact [Microsoft Edge support](https://www.microsoftedgeinsider.com/support).

### Issue: Stuck at "Setting up sync..." or “Couldn’t connect to the sync server. Retrying…”

1. Try to sign out and then sign in.
2. Go to *edge://sync-internals*. If under the "**Type info**" section the following error is present, then  skip to the following issue, **Cryptographer error encountered**.

   `"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered"`

3. Try pinging the server endpoint. The server endpoint for a client is available in *edge://sync-internals*. The next screenshot shows endpoint information under **Environment Info**.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-endpoint-info.png" alt-text="Endpoint information":::

4. If the server endpoint is empty, or if server cannot be pinged and a firewall is present in the environment, confirm that the necessary service endpoints are available to the client computer.

   - Microsoft Edge sync service endpoints:
     - [https://edge-enterprise.activity.windows.com](https://edge-enterprise.activity.windows.com)
     - [https://edge.activity.windows.com](https://edge.activity.windows.com)
    - Azure Information Protection endpoints:
      - [https://api.aadrm.com](https://api.aadrm.com) (for most tenants)
      - [https://api.aadrm.de](https://api.aadrm.de) (for tenants in Germany)
      - [https://api.aadrm.cn](https://api.aadrm.cn) (for tenants in China)
   - [Windows Notification Service endpoints](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).

5. If the issue still isn't fixed, contact [Microsoft Edge support](https://www.microsoftedgeinsider.com/support).

### Issue: Cryptographer error encountered

This error is visible under **Type info** in *edge://sync-internals* and may mean that the user's service side data needs to be reset. The following example shows a cryptography error message:
<br>"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered".

1. Restart Microsoft Edge and navigate to *edge://sync-internals* and check the “**AAD Account Key Status**” section
   - "Success" in "Last MIP Result": the cryptographer error means server data might be encrypted with a lost key. Data reset is needed to resume sync.
   - "No permissions" in "Last MIP Result": It is possibly caused by an Azure AD change or tenant subscription changes. Data reset is needed to resume sync.
   - Other errors may mean server configuration issues.
2. If data reset is needed, see [Reset Microsoft Edge data in the cloud](edge-learnmore-reset-data-in-cloud.md).

### Issue: “Sync has been turned off by your administrator.”

Make sure that the [SyncDisabled policy](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled)  is not set.

## See also

- [Microsoft Edge Enterprise Sync](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
