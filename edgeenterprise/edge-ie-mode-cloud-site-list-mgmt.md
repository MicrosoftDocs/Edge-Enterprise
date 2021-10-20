---
title: Cloud Site List Management for Internet Explorer (IE) mode (Public Preview)"
ms.author: shisub
author: danwesley
manager: srugh
ms.date: 10/19/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Learn how to configure and use Cloud Site List Management for IE mode using the Microsoft 365 Admin Center."
---

# Cloud Site List Management for IE mode (Public Preview)

This article explains how to configure and use Cloud Site List Management for Internet Explorer (IE) mode through the Microsoft 365 Admin Center.

## Overview

As you transition your workflows and applications from IE11 to IE mode, **Cloud Site List Management** lets you manage your site lists for IE mode in the cloud. You can work with site lists using the **Microsoft Edge Site Lists** experience in the **Microsoft 365 Admin Center**. 
**This experience is now in public preview.**

The preview experience lets you store your organization’s site list in a compliant cloud location instead of needing an on-premises infrastructure to host your site list. You can create, import, export site lists, and audit changes to site list entries through the Microsoft 365 Admin Center. You can publish multiple site lists to the cloud and use group policy to assign different groups of devices to use different lists.

## Prerequisites

The following prerequisites apply to this public preview.

1. Customers must have an Azure AD tenant.
2. The tenant subscription must include Exchange Services. For more information, see the [FAQ](#faq).
3. Admins must have Microsoft Edge version 93 or greater installed and the latest version of the [policy files](https://aka.ms/edgeenterprise).
4. Admins need to be a Global Administrator or a Microsoft Edge Administrator on the tenant to access the Microsoft Edge site lists experience.
   - To opt in to the public preview, a Global Administrator is required to opt the tenant in to Targeted release. For more information, see [Opt in to public preview](#opt-in-to-public-preview).

## The preview experience

There are three aspects to the preview experience.

### Publish enterprise site list to the cloud

IT admins can publish one or more site lists to an authenticated endpoint that Microsoft Edge clients within their tenant can download for the IE mode experience. Admins can import the existing enterprise site list XML into the Microsoft Edge Site Lists experience in the Microsoft 365 Admin Center and then publish it to the cloud location. 

### Associate the cloud-hosted site list with Microsoft Edge

With Microsoft Edge version 93, admins can use the [InternetExplorerIntegrationCloudSiteList](/docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist) setting to configure one of the cloud-hosted site lists that Microsoft Edge can consume for IE mode. Users must be signed in to Microsoft Edge for the client to consume the site list from the cloud.

> [!IMPORTANT]
> When this policy is configured, it overrides the original InternetExplorerIntegrationSiteList policy.

### Manage site list contents on the Microsoft 365 Admin Center

IT admins can create a new list or import an existing site list into the Microsoft Edge site lists experience. They can add, edit, delete site list contents, and view comment history to track changes to individual entries. The next section explains how to opt in to public preview and access the Microsoft Edge site lists experience in the M365 Admin Center.

## Opt in to public preview

While in public preview, you need to opt-in to view preview experiences in the Microsoft 365 Admin Center. You must be a global admin in Microsoft 365 to opt in.

Use the following steps to change how your organization receives Microsoft 365 updates.

> [!NOTE]
> It can take up to 24 hours for the following configuration changes to take effect in Microsoft 365. If you opt out of a targeted release after enabling it, your users may lose access to features that haven't reached the scheduled release yet.

1. Sign in to the [Admin Center](https://admin.microsoft.com) and then go to  **Settings > Org Setting**. Under the **Organization profile** tab, choose **Release preferences**.
2. To disable targeted release, select **Standard release**, then select **Save changes**.
3. To enable targeted release for all users in your organization, select **Targeted release for everyone**, then select **Save changes**.
4. To enable targeted release for some people in your organization, select **Targeted release for selected users**, then select **Save changes**.
5. Choose **Select users** to add users one at a time, or **Upload users** to add them in bulk.
6. When you finish adding users, select **Save changes**.

For more information, see [Set up the Standard or Targeted release options - Microsoft 365 admin](/docs.microsoft.com/microsoft-365/admin/manage/release-options-in-office-365?view=o365-worldwide).

## Publish enterprise site list to the cloud

Use the following steps as a guide to create site list, import a site list, and publish the site list. Before you can complete these steps, sign in the Microsoft 365 admin center.

1. Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) with your admin credentials.
2. On the left navigation pane, select **Settings > Org Settings**.
3. You will see **Microsoft Edge site lists (Preview)** option.

### Steps to create a site list

1. On the Org Settings page, select **Microsoft Edge site lists (Preview)**
2. On the resulting page, select **Create a new list**.
3. Enter a **Site list name** and a **Description**, and then select **Create**.
4. After you get confirmation,select **Close panel**. 

### Steps to import a site list

1. Select the site list you want to populate.
2. On the resulting page, select **Import list**.
3. On the right-hand panel, select **Browse**.
4. Select the file you want to import and then select **Upload** on the bottom of the panel.
5. You can skim through the URLs in the uploaded file. If you want to pick a different file, you can select **Upload a different file** at the top of the panel. If everything looks correct, select **Add** at the bottom of the panel.
6. After your list is imported, select **Close panel**. 

### Steps to publish a site list

1. To publish a site list, go back up a level to the Microsoft Edge site lists page. Select the breadcrumb above the site list name to go up a level.
2. On the Microsoft Edge site lists page, select the site list you want to publish to the cloud, and then select **Publish site list**.
3. On the right-hand panel, update the **Version number** and select **Publish the bottom of the panel.
4. After confirmation, select **Close panel**. The **Published status** icon, **Last published**, and **Last published by** are all updated.

## Associate the cloud-hosted site list with Microsoft Edge

Use the following steps to associate the cloud-hosted site list with Microsoft Edge.

1. To configure devices to use the Fabrikam – all users list example, go to the site list contents page and copy the **Site list ID**.
2. For the device group you pick, select **Enabled** and enter the **Site list ID** in the Configure the Enterprise Mode Cloud Site List policy.
3. You can run **gpupdate/force** from  the Command Prompt to update the device with the policy or wait for the group policy to take effect. After the policy is updated, you can verify that Microsoft Edge is reading the cloud site list by going to [edge://compat/enterprise](edge://compat/enterprise). You need to be signed into Microsoft Edge.

> [!NOTE]
> After publishing a site list the first time and updating group policy, you need to restart Microsoft Edge. Wait 60 seconds or select the Force Update button on [edge://compat/enterprise](edge://compat/enterprise). When publishing updates to an already associated site list, there may be an older version of the site list in the cache. This entry will be refreshed after 60 seconds. For more information, see [What happens if users log out of Microsoft Edge?](#what-happens-if-users-log-out-of-microsoft-edge).

## Manage site list contents on the Microsoft 365 Admin Center

You can add individual site entries, delete site entries and view change history for comments.
If you have hybrid sceanrios that require a your site list to be hosted on-premises, you can export your site list from the M365 Admin Center. Use the following steps as a guide for managing site list content. 

### Add individual sites to the site list

You can add individual sites to any site list. After adding sites to the list, you can use the predefined filters using the **Filter** button (next to the Search input area) to view updates to the list.

1. Go to the site list where you want to add a site.
2. Select **Add a site**.
3. Enter the site address and pick the engine that should be used to open the site. Add comments as needed and select **Save**.

   > [!NOTE]
   > The **Status** column for any entries added to a Published site list will show **Addition pending**. If you navigate to the list of site lists by selecting **Microsoft Edge site lists** at the top of the screen, you'll see that the **Published Status** column shows **Changes pending publish** to indicate that latest updates to the site list need to be published in order for users to receive them. You can use the **Filter** button _(next to the Search box)_ to select Addition pending to see all added entries that are pending publication.

### View the change history for site entries

1. Select the site entry that you want to see the change history for and then select **View comments**.

### Delete a site from the site list

Use the following steps to delete a site entry.

1. Pick the site list entry that you’d like to delete a site from. Select **Delete site**.
2. Select **Delete** at the bottom of the pane.
3. After you see confirmation that a site entry has been deleted, it will stay on the list until the site list is published to the cloud location. You can view the list of deleted sites before publishing by selecting the Filter button and filtering for sites in the **Delete pending** state.

   > [!NOTE]
   > The **Status** column for any entries deleted from a Published site list will show **Delete pending**. If you navigate to the list of site lists by selecting **Microsoft Edge site lists** at the top of the screen, you'll see that the **Published Status** column shows **Changes pending publish** to indicate that latest updates to the site list need to be published in order for users to receive them.You can use the **Filter** button _(next to the Search box)_ to select Delete pending to see all deleted entries that are pending publication.

### Export a site list

There are scenarios where you want to export a site list. For example, if you're unable to move your site list to the cloud right away or if you need to maintain a hybrid environment with site lists in the cloud as well as on-premises. You can use the Cloud Site List Management experience to manage updates to a site list in a central location and export the site list to the on-premises host.

1. On the Microsoft Edge site lists page, select the site list that you want to export.
2. On the resulting page you’ll see the site list entries and the **Export list** option.
3. Select Export list to download the site list xML file.

## FAQ

### Why is my tenant required to have an Exchange Service subscription for this feature?

This subscription ensures that the right backend association happens with your tenant immediately, which occurs when you first select Microsoft Edge site lists. When Exchange Services aren’t part of your subscription, the association request from the Microsoft 365 Admin Center will fail. An alert is sent to the provisioning system to address the problem.  This will result in a three day delay for you to use the experience.

### Can users who haven’t signed in to Microsoft Edge download the site list?

No, users must sign in to the browser to download the cloud hosted site list. You can configure a policy to allow Implicit Sign in to prevent user experience disruption. For more information, see [ImplicitSignInEnabled](/docs.microsoft.com/DeployEdge/microsoft-edge-policies#implicitsigninenabled).

### What is the default refresh interval after updates are made to site list contents?

The site list is refreshed in Microsoft Edge every two hours. You can change this interval the [NavigationDelayForInitialSiteListDownloadTimeout](/docs.microsoft.com/deployedge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout) policy. The minimum refresh interval is 30 minutes.

### What happens if users log out of Microsoft Edge?

Access to the site list requires explicit browser sign in for the first download. In a scenario where the user logs out after being logged in, the site list is cached in Microsoft Edge. The list will stay cached even if the user logs out of Microsoft Edge from their Azure Active Directory (Azure AD) account. Microsoft Edge will not try to fall back to the non-cloud download location while the Cloud site list policy is configured. Microsoft Edge attempts to update the cached site list at the following times (note that all attempts will fail if the user is not signed in to Microsoft Edge):

- 60 seconds after you restart the browser. If the 60 second startup delay needs to be shorter, you can use the [NavigationDelayForInitialSiteListDownloadTimeout](/docs.microsoft.com/deployedge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout) policy to change the amount of delay.
- Every two hours when Microsoft Edge is running.

## See also

- [About IE mode](./edge-ie-mode.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
