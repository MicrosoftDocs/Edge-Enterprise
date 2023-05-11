---
title: "Microsoft Edge management service"
ms.author: leahtu
author: dan-wesley
manager: arunesh.chandra
ms.date: 05/10/2023
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Provides steps for configuring the Microsoft Edge management service."
---

# Microsoft Edge management service

The Microsoft Edge management service is an area in the M365 admin center where admins can configure Microsoft Edge browser settings for their organization. These configurations are stored in the cloud and you can apply these settings to the browser using group assignment or group policy. Users must be logged into Microsoft Edge to retrieve these settings.

> [!NOTE]
> This experience is in public preview. We'll start rolling out this experience on May 23 and expect to finish the rollout by the end of that week. You'll need to set up a Targeted release to opt in and view this experience in the M365 admin center.

## Set up a Targeted release

There are two parts to setting up a Targeted release: identifying release preferences and picking the users for the release preference you configure.

Use the following steps as a guide to set up a Targeted release:

1. Sign into the Microsoft 365 admin center and then go to **Settings** > **Org settings**. Under the **Organization profile** tab, choose **Release preferences**. This window gives several release options: standard for everyone,  targeted for everyone, and targeted for selected users.
1. To enable a targeted release for all the users in your organization, select **Targeted release for everyone**, and then select **Save changes**.
1. To enable a targeted release for some people in your organization, select **Targeted release for selected users**, and then select **Save changes**. After you set up the release you want, the next step is to add the users for the release.
1. Choose **Select users** to add users one at a time, or **Upload users** to add them in bulk.
1. When you finish adding users, select **Save changes**.

For more information, see [Set up the Standard or Targeted release options](/microsoft-365/admin/manage/release-options-in-office-365?view=o365-worldwide).

## Prerequisites

- You must have Microsoft Edge Canary 114.0.1814.0 or greater installed.
- You must be a [Microsoft Edge Administrator](/azure/active-directory/roles/permissions-reference#edge-administrator) or a [Global Administrator](/azure/active-directory/roles/permissions-reference#global-administrator) to access the experience in Microsoft 365 Admin Center.

## Access the preview experience

Use these steps to access the preview experience:

1. Go to the Microsoft 365 admin center and login.
1. In the main left navigation bar, go to **Settings** > **Microsoft Edge**.  

## Get started with configuration profiles

A configuration profile contains all the browser policy configurations, including extension settings. We've expanded configuration profiles to handle all browser policies.

> [!NOTE]
> If you created a profile to manage your extensions during private preview, then you'll find those configurations in the profile with the same name.

Each configuration profile can only be assigned to one Azure Active Directory (Azure AD) group, and each group can only be assigned one configuration profile. However, the group that you select can contain other (nested) groups. If a user is a member of multiple Azure AD groups with conflicting policy settings, then the profile priority is used to determine which policy setting is applied. The highest priority is applied, with "1" being the highest priority that you can assign.

#### Create a configuration profile

Follow these steps to create a configuration profile:

1. Under the **Policy management** pivot, select **Add a profile**.  
1. Under **Add a configuration profile**, enter a profile name and description and then select **Add**.  

After confirmation, you'll be able to go to the profile and configure the policies and extensions you want to use.

#### Copy a configuration profile

Follow these steps to copy a configuration profile:

1. Under the **Policy management** pivot, select the profile you want to make a copy.
1. Select **Copy profile**.
1. Under **Copy configuration profile**, enter a profile name and description and then select **Add**.

After confirmation, the new profile is created with the same configurations as the profile you copied.

#### Reorder priority of configuration profile

Follow these steps to reorder the priority of a configuration profile:

1. Under the **Policy management** pivot, select **Reorder priority**  
1. Select a profile to change and under **Reorder profile priority**, pick a priority number from the dropdown list.  
1. Select **Save** after you finish making your changes.  

#### Configure a policy for a configuration profile

Follow these steps to configure a policy for a configuration profile:

1. Under the **Policy management** pivot, select the profile you want to configure a policy for  
1. Under the **Policies** pivot, select **Add policy**  
1. Under **Configure a policy**, search for the policy you want to configure for this profile. Set the configuration settings/values for the policy you select.
1. Select **Save**.  

#### Assign a configuration profile to an Azure AD group

> [!NOTE]
> You can only assign one group to a profile. If you want to assign a different group, then you need to remove the existing group and then assign a new group to the profile.

Follow these steps to assign a configuration profile to an Azure AD group:

1. Under the **Policy management** pivot, select the profile you want to assign.
1. Under the **Group assignment** pivot, select **Add group**.
1. Under **Select a security group**, select the group to assign the profile to.
1. Select **Add**. The profile will now be applied to all users in the selected group.

### Manage extensions

placeholder text

## Configure Microsoft Edge to use a configuration profile

placeholder text

### Enable the Edge Admin Center

placeholder text

### Set an enrollment token

placeholder text

## Feedback and support

This experience is supported by Microsoft Support. You can reach out to Microsoft Support to report issues or give feedback. You can also leave feedback in our [TechCommunity forum](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise).

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)