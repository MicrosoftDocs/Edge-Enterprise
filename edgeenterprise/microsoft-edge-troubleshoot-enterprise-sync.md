---
title: "Diagnose and fix Microsoft Edge sync issues"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 07/18/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Guidance and tools a Microsoft Edge admin can use to troubleshoot and fix common enterprise sync issues"
---

# Diagnose and fix Microsoft Edge sync issues

This article provides troubleshooting guidance for the most common sync issues in a Microsoft Entra environment. It also includes troubleshooting steps and the recommended tools for gathering the logs needed for troubleshooting a sync issue.

If a user is experiencing an issue syncing browser data across their devices, they can perform a resync in **Settings** > **Profiles** > **Sync** > **Re-sync data to this device**.  Should the sync problem continue, click on "**Still having sync problems? Try another option**" for additional solutions, then choose "**Reset sync**". If the sync reset doesn't work, an admin or support staff member can use the guidance in this article to fix a sync issue. For more information, see [Perform a reset to fix a synchronization problem](/deployedge/edge-learnmore-reset-data-in-cloud#perform-a-reset-to-fix-a-synchronization-problem).

> [!NOTE]
> Applies to Microsoft Edge on Chromium, version 77 or later unless otherwise noted.

## Before you begin: identity issues versus sync issues

It's important to understand the difference between identity issues and sync issues. A popular use case for maintaining user identity in the browser is to support sync. For this reason, identity issues are frequently confused with sync issues. Understand the difference between identity and sync issue before you start troubleshooting sync.

Before you treat an issue as a sync issue, check to see if the user is signed into the browser with a valid account.

The next screenshot shows an example of an identity error. The error is **Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea**, which is found in *edge://sync-internals* under **Credentials**.

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue3.png" alt-text="Last Token Error EDGE_AUTH_ERROR: 3,54, 3ea":::

## Basic troubleshooting steps

Before you start troubleshooting, check the [Common sync issues](#common-sync-issues) to see if any of these issues apply to your sync problem.

Use the following steps as a guide for troubleshooting a sync issue.

1. Sign in your Office 365 or Microsoft 365 admin portal and verify that your license is valid.
2. Sign in your Azure portal and verify that your Azure license is valid.
3. Sign out your account on the Microsoft Edge browser.
4. Make sure you're on the latest version of Microsoft Edge that supports all the sync features (at least 98.0.1108.43 (Official build) (64-bit)).
5. Perform a resync in **Settings** > **Profiles** > **Sync** > **Re-sync data to this device**.  For more information, see [Perform a reset to fix a synchronization problem](/deployedge/edge-learnmore-reset-data-in-cloud#perform-a-reset-to-fix-a-synchronization-problem).
6. Verify that your account is enabled for syncing. On a new tab, go to: *edge://sync-internals/*. The Summary section, shown in the next screenshot shows that sync is enabled.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/summary-confirm-sync-working.png" alt-text="Summary from  sync-internals":::

7. Verify that the device you're on is getting sync'ed. Go to *edge://sync-internals/* and select the **Sync Node Browser** tab. Open the **Device info** folder to see which devices are in the sync list.
8. Check your sign-in status. Go to *edge://signin-internals/*. The next screenshot shows the sign-in status for a user.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-get-signin-status-for-sync.png" alt-text="Get sign in status from sign-internals":::

9. Check to see if there are any policies that might prevent syncing. Go to *edge://policy/* to see the Policies page. The next screenshot shows an example of active policies for a signed in user. This page also shows Policy Precedence and Microsoft Edge Update Policies.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-ts-get-active-policies2.png" alt-text="Policies page for signed in user":::

## Common sync issues

### Issue: Can't access Microsoft 365 or Azure Information Protection subscription

Do you have a previous Microsoft 365 or Azure Information Protection (AIP) subscription that expired and then replaced with a new subscription? If so, then the tenant ID has changed and the service data needs to be reset. See the instructions for resetting data in [Issue: Cryptographer error encountered](#issue-cryptographer-error-encountered).

### Issue: "Sync is not available for this account."

If this error is encountered for a Microsoft Entra account, or if DISABLED_BY_ADMIN appears in *edge://sync-internals*, follow the steps in the next procedure sequentially until the problem is fixed.

> [!NOTE]
> Because the source of this error usually needs a configuration change in a Microsoft Entra tenant, these troubleshooting steps can only performed by a tenant admin.

1. Verify that the enterprise tenant has one of the supported subscriptions in [Configure Microsoft Edge enterprise sync](/deployedge/microsoft-edge-enterprise-sync). To find out which subscription you have, see [What subscription do I have?](/microsoft-365/admin/admin-overview/what-subscription-do-i-have). If the tenant doesn't have a supported subscription, they can either purchase Azure Information Protection separately, or upgrade to one of the supported subscriptions.
2. If a supported subscription is available, verify that the tenant has Azure Information Protection (AIP). If you need to check AIP status and, if necessary, activate  AIP, see these instructions: [Activating the protection service from Azure Information Protection](/azure/information-protection/activate-service).
3. If step 2 shows that AIP is active but sync still doesn't work, turn on Enterprise State Roaming (ESR). If you need to enable ESR, see these instructions: [Enable Enterprise State Roaming in Microsoft Entra ID](/azure/active-directory/devices/enterprise-state-roaming-enable).

   > [!NOTE]
   > ESR doesn't need to stay on. You can turn off ESR if this step fixes the issue.

4. Confirm that Azure Information Protection isn't scoped via an onboarding policy. You can use the [Get-AIPServiceOnboardingControlPolicy](/powershell/module/aipservice/get-aipserviceonboardingcontrolpolicy) PowerShell cmdlet to see if scoping is enabled. Make sure the aIPService PowerShell monitor is installed. You can get it here: [Install the AIPService PowerShell module for Azure Information Protection](/azure/information-protection/install-powershell). The next two examples show an unscoped configuration and a configuration scoped to a specific security group.

   ```powershell
    PS C:\Work\scripts\PowerShell> Get-AIPServiceOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False 
   ```

   ```powershell

    PS C:\Work\scripts\PowerShell> Get-AIPServiceOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False f1488a05-8196-40a6-9483-524948b90282   All
   ```

   If scoping is enabled, the affected user should either be added to the security group for the scope, or the scope should be removed. Scoping can be removed with the [Set-AIPServiceOnboardingControlPolicy](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy) PowerShell applet.

5. Confirm that the IPCv3Service is turned on in the tenant. The [Get-AIPServiceConfiguration](/powershell/module/aipservice/get-aipserviceconfiguration) PowerShell cmdlet shows the status of the service.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="Check to see if IPCv3Service is enabled.":::

6. If the issue isn't fixed, contact [Microsoft Edge support](https://www.microsoftedgeinsider.com/support).

### Issue: Stuck at "Setting up sync..." or "Couldn't connect to the sync server. Retrying..."

1. Try to sign out and then sign in.
2. Go to *edge://sync-internals*. If the following error appears under the **Type info** section, skip to the [Cryptographer error encountered](#issue-cryptographer-error-encountered) issue.

   `"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered"`

3. Try pinging the server endpoint. The server endpoint for a client is available in *edge://sync-internals*. The next screenshot shows endpoint information under **Environment Info**.

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-endpoint-info2.png" alt-text="Endpoint information":::

4. If the server endpoint is empty, or if server can't be pinged because there's a firewall in the environment, confirm that the necessary service endpoints are available to the client device.

   - Microsoft Edge sync service endpoints:
     -  `https://edge.microsoft.com`

    - Azure Information Protection endpoints:
      - `https://api.aadrm.com` (for most tenants)
      - `https://api.aadrm.de` (for tenants in Germany)
      - `https://api.aadrm.cn` (for tenants in China)
   - [Enterprise Firewall Configurations to Support WNS Traffic](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).

5. If the issue still isn't fixed, contact [Microsoft Edge support](https://www.microsoftedgeinsider.com/support).

### Issue: Cryptographer error encountered

This error is visible under **Type info** in *edge://sync-internals* and might mean that the user's service side data needs to be reset. The next example shows a cryptography error message:

`"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered".`

Use the following steps to fix this issue:

1. Restart Microsoft Edge and go to *edge://sync-internals*. Look at the **Microsoft Entra account Key Status** section to see if any of the following messages are present:
   - Last MIP Result = "Success": This error means server data might be encrypted with a lost key. A data reset is needed to resume sync.
   - Last MIP Result = "No permissions": It's possibly caused by a Microsoft Entra ID change or tenant subscription changes. A data reset is needed to resume sync.
   - Other errors may mean there's a server configuration issue.
2. If a data reset is needed, see [Reset Microsoft Edge data in the cloud](edge-learnmore-reset-data-in-cloud.md).

### Issue: "Sync has been turned off by your administrator."

Make sure that the [SyncDisabled policy](./microsoft-edge-policies.md#syncdisabled) isn't set.

## See also

- [Microsoft Edge Enterprise Sync](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge enterprise sync FAQ](microsoft-edge-enterprise-sync-faq.md)
- [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
