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

To manage extension settings for a profile, go **Microsoft Edge management**, select the profile you want to work with and then select the **Extensions** pivot. You can configure profile settings that apply to all extensions. Any extensions you add to be managed will appear in the profile. You can add the an extension to the allow list, block list, or forced-installed list by setting the installation policy. If you configure specific settings on an individual extension, then those settings will override the profile settings.

#### Import existing extension settings to an existing configuration profile

Follow these steps to import extension settings:

1. Select the profile you want to import extension settings to and go to the **Extensions** pivot.
1. Select **Import JSON**.
1. Under **Import JSON**, browse for the JSON file that contains your extension settings and then select **Import**. Importing might overwrite any previous configurations. Note that it may take some time to complete the import if the file is large.

After confirmation, your profile will be populated with the imported settings.

#### Export extension settings to configure the ExtensionSettings policy

Follow these steps to export extension settings:

1. Select the profile you want to export extension settings from and go to the **Extensions** pivot.
1. Select **Export JSON** and the export will start downloading.

After the download is finished you can apply the JSON as a value to the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) group policy.

#### Manage profile settings for an extension

Follow these steps to manage profile settings:

1. Select a profile and go to the **Extensions** pivot.
1. Select **Manage profile** to configure any of the settings in the following table.

   | Setting | Description |
   |:-----|:-----|
   | Block all extensions | Users can't install any extensions (unless the extension is on the allow list). |
   | Allowed types of apps and extensions| Specify what types of app or extensions users are allowed to install. |
   | Install sources| Specify which URLs are allowed to install extensions. For URL pattern examples, see the [Defining match patterns](/microsoft-edge/extensions-chromium/developer-guide/match-patterns). |
   | External extensions | Allow or block installation of external extensions. |
   | Message for users when extension is blocked | Set a custom message that displays if users try to install a blocked extension. |
   | Blocked hosts | Prevent extensions from interacting with or modifying websites that you specify. The host pattern format is similar to [match patterns](/microsoft-edge/extensions-chromium/developer-guide/match-patterns) except you can't define the path. |
   | Allowed hosts | Allow extensions to interact with or modify websites, even if they're defined in blocked hosts. The host pattern format is similar to [match patterns](/microsoft-edge/extensions-chromium/developer-guide/match-patterns) except you can't define the path. |
   | Block extensions that require these permissions | Prevent users from installing/running extensions that need the permissions you select. |

1. When you're finished configuring extension settings, select **Save**.

#### Add an extension

#### Manage an extension

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