---
title: Cloud Site List Management for IE mode (Public Preview)"
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 10/18/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Learn how to configure and use Cloud Site List Management for IE mode using the M365 Admin Center."
---

# Cloud Site List Management for IE mode (Public Preview)

This article explains how to configure and use Cloud Site List Management for Internet Explorer (IE) mode through the M365 Admin Center.

## Overview

Microsoft Edge with IE mode creates a seamless single browser experience for enterprise environments that have a mix of legacy and modern applications. You can control which applications need legacy compatibility such that your end-users have the most secure browsing experience without compromising business critical workflows. As you transition your workflows and applications from IE11 to IE mode, **Cloud Site List Management** lets you manage your site lists for IE mode in the cloud. This is done using the **Microsoft Edge Site Lists** experience in the **M365 Admin Center**. This experience is now in public preview.

The preview experience  lets you store your organization’s site list in a compliant cloud location instead of needing an on-premises infrastructure to host your site list. You can create, import, export site lists, and audit changes to site list entries through the M365 Admin Center. You can publish multiple site lists to the cloud and use group policy to assign different groups of devices to use different lists.

## Prerequisites

The following prerequisites apply to this public preview.

1. Customers must have an Azure AD tenant.
2. The tenant subscription must include Exchange Services. For more information, see the [FAQ](#faq).
3. Admins must have Microsoft Edge version 93 or greater installed and the latest version of the [policy files](https://aka.ms/edgeenterprise).
4. Admins need to be a Global Administrator or an Edge Administrator on the tenant to access the Microsoft Edge site lists experience.
   - To opt-in to the public preview, a Global Administrator is required to opt the tenant in to Targeted release. For more information, see [Opt in to public preview](#opt-in-to-public-preview).

## The preview experience

There are three aspects to the preview experience.

### Publish enterprise site list to the cloud

IT admins can publish one or more site lists to an authenticated endpoint that Microsoft Edge clients within their tenant can download for the IE mode experience. Admins can import the existing enterprise site list XML into the Microsoft Edge Site Lists experience in the M365 Admin Center and then publish it to the cloud location.

### Configure Microsoft Edge to use your cloud hosted site list

With Microsoft Edge version 93, admins can use the [InternetExplorerIntegrationCloudSiteList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist) setting to configure one of the cloud-hosted site lists that Microsoft Edge can consume for IE mode.

> [!IMPORTANT]
> When this policy is configured, it overrides the original InternetExplorerIntegrationSiteList policy.

### Manage site list contents on the M365 Admin Center

IT admins can create a new list or import an existing site list into the Microsoft Edge site lists experience. They can add, edit, delete site list contents, and view comment history to track changes to individual entries. The next section explains how to set up the Admin Center for Microsoft 365.

## Admin Center set up

Before you complete the steps to set up the Admin Center you must opt in to the public preview.

### Opt in to public preview

While in public preview, you need to opt-in to view preview experiences in the M365 Admin Center. You must be a global admin in Microsoft 365 to opt in.

Use the following steps to change how your organization receives Microsoft 365 updates.

> [!NOTE]
> It can take up to 24 hours for the following configuration changes to take effect in Microsoft 365. If you opt out of a targeted release after enabling it, your users may lose access to features that haven't reached the scheduled release yet.

1. Sign in to the Admin Center and then go to  **Settings > Org Setting**. Under the **Organization profile** tab, choose **Release preferences**.
2. To disable targeted release, select **Standard release**, then select **Save changes**.
3. To enable targeted release for all users in your organization, select **Targeted release for everyone**, then select **Save changes**.
4. To enable targeted release for some people in your organization, select **Targeted release for selected users**, then select **Save changes**.
5. Choose **Select users** to add users one at a time, or **Upload users** to add them in bulk.
6. When you finish adding users, select **Save changes**.

For more information, see [Set up the Standard or Targeted release options - Microsoft 365 admin](https://docs.microsoft.com/microsoft-365/admin/manage/release-options-in-office-365?view=o365-worldwide).

### Publish enterprise site list to the cloud

#### CREATE A SITE LIST 
#### IMPORT SITE LIST
#### Publish site list

## Associate the cloud-hosted site list with Microsoft Edge

x

## FAQ

x

## See also

- [About IE mode](./edge-ie-mode.md)
- [Additional Enterprise Mode information](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)