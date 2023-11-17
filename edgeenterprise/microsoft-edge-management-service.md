---
title: "Microsoft Edge management service"
ms.author: leahtu
author: dan-wesley
manager: archandr
ms.date: 11/17/2023
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Provides steps for configuring the Microsoft Edge management service."
---

# Microsoft Edge management service

> [!NOTE]
> Microsoft Edge for Business is now available in Edge stable version 116! [Learn more](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/microsoft-edge-for-business-faq/ba-p/3891837) about the new, dedicated work experience with native enterprise grade security, productivity, manageability, and AI built in.

The Microsoft Edge management service is an area in the Microsoft 365 admin center where admins can configure Microsoft Edge browser settings for their organization. These configurations are stored in the cloud and you can apply these settings to the browser using group assignment or group policy. Users must be logged into Microsoft Edge to retrieve these settings.

<!-- ====================================================================== -->
## Prerequisites

- You must have Microsoft Edge 115.0.1901.7 or greater installed.
- You must be a [Microsoft Edge Administrator](/azure/active-directory/roles/permissions-reference#edge-administrator) or a [Global Administrator](/azure/active-directory/roles/permissions-reference#global-administrator) to access the experience in Microsoft 365 Admin Center.
- You must be using one of the following supported operating systems: Windows 10+ or Windows Server 2016+. See [Microsoft Edge Supported Operating Systems](/deployedge/microsoft-edge-supported-operating-systems) for specifics.
<!-- ====================================================================== -->
## Access the experience

Use these steps to access the experience:

1. Go to the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal/Home#/homepage) and login.
1. In the main left navigation bar, go to **Settings** > **Microsoft Edge**.  
<!-- ====================================================================== -->
## Get started with configuration profiles

A configuration profile contains all the browser policy configurations, including extension settings.

Each configuration profile can be assigned to multiple Microsoft Entra groups, and a group can be assigned to multiple configuration profiles. When a group is assigned to multiple configuration profiles, the settings merge if there are no conflicting settings. If a user is a member of multiple Microsoft Entra groups with conflicting policy settings, then the profile priority is used to determine which policy setting is applied. The highest priority is applied, with "0" being the highest priority that you can assign.

#### Create a configuration profile

Follow these steps to create a configuration profile:

1. Under the **Configuration profiles** pivot, select **Add a profile**.  
1. Under **Add a configuration profile**, enter a profile name and description and then select **Add**.  

After confirmation, you'll be able to go to the profile and configure the policies, and extensions you want to use.

#### Import a configuration profile

If you previously exported a configuration profile from Microsoft Edge management service, you can import it to a profile. 

Follow these steps to import a profile:

1. Select the profile that you want to import your previously exported profile to.
2. Select **Import**.
3. Browse for the profile's JSON file and select **Import**.

#### Export a configuration profile

You can export a configuration profile as a JSON file. This export can be used to save a copy of your configurations and can be imported to a different profile.

Follow these steps to export a profile:

1. Select the profile you want to export.
2. Select **Export profile**.
3. Select **Export**.

#### Copy a configuration profile

Follow these steps to copy a configuration profile:

1. Under the **Configuration profiles** pivot, select the profile you want to make a copy.
1. Select **Copy profile**.
1. Under **Copy configuration profile**, enter a profile name and description and then select **Add**.

After confirmation, the new profile is created with the same configurations as the profile you copied.

#### Reorder priority of configuration profile

Follow these steps to reorder the priority of a configuration profile:

1. Under the **Configuration profiles** pivot, select the profile you want to change and select  **Reorder priority**.
1. Under **Reorder profile priority**, pick a priority number from the dropdown list.
1. Select **Save** after you finish making your changes.  

#### Configure a policy for a configuration profile

Follow these steps to configure a policy for a configuration profile:

1. Under the **Configuration profiles** pivot, select the profile you want to configure a policy for.  
1. Under the **Policies** pivot, select **Select policy**.
1. Under **Configure a policy**, search for the policy you want to configure for this profile. Set the configuration settings/values for the policy you select.
1. Select **Save**.  

<a name='assign-a-configuration-profile-to-an-microsoft-entra-group'></a>

#### Assign a configuration profile to a Microsoft Entra group

Follow these steps to assign a configuration profile to a Microsoft Entra group:

1. Under the **Configuration profiles** pivot, select the profile you want to assign.
1. Under the **Group assignment** pivot, select **Select group**.
1. Under **Select a security group**, select the group to assign the profile to.
1. Select **Select**. The profile will now be applied to all users in the selected group.

### Manage extensions

To manage extension settings for a profile, go **Microsoft Edge management**, select the profile you want to work with and then select the **Extensions** pivot. You can configure profile settings that apply to all extensions. Any extensions you add to be managed will appear in the profile. You can add an extension to the allow list, block list, or forced-installed list by setting the installation policy. If you configure specific settings on an individual extension, then those settings override the profile settings.

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

After the download is finished, you can apply the JSON as a value to the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) group policy.

#### Manage settings for all extensions

Follow these steps to manage profile settings:

1. Select a profile and go to the **Extensions** pivot.
1. Select **Manage extensions** to configure any of the settings in the following table.

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

Follow these steps to add an extension:

1. Select a profile and go to the **Extensions** pivot.
1. Select **Select extension**.
1. Under **Select an extension**, select an extension from the **Microsoft Edge Add-ons** store or specify an external extension ID.
1. Select **Select**.

#### Manage an extension

After selecting an extension, you can configure settings for a specific extension. These settings only apply to the extension that you select and will override any profile settings.

##### Manage extension policy

Decide if an extension is allowed, blocked, or forced by setting its installation policy. Follow these steps to configure this setting:

1. Select an extension.
1. Select **Manage installation policy** and choose one of the following options from the dropdown list:

   - Allow: Users can install the extension. This is the default setting.
   - Block: Users can't install the extension. You could remove the extension if users previously installed it. Also, you can write a message that displays when users try to install the extension.
   - Force: The extension is automatically installed. Users can't remove it. You can optionally specify an update URL for the initial extension installation and use it for subsequent updates.
   - Normal: The extension is automatically installed. Users can disable it. You can optionally specify an update URL for the initial extension installation and use it for subsequent updates.

1. Select **Save**.

##### Manage hosts

Control what websites extensions can access. Prevent extensions from altering web pages by specifying which URLs should block extensions from making changes or reading data from. Allow extensions to interact with or modify websites, even if they're defined in blocked hosts. The host pattern format is similar to [match patterns](/microsoft-edge/extensions-chromium/developer-guide/match-patterns) except you can't define the path. Follow these steps to configure this setting:

1. Select an extension.
1. Select **Manage hosts**. In the **Hosts** window, specify blocked and allowed host URLs.
1. Select **Save**.

##### Manage permissions

Prevent users from installing and using the extension if it requires certain permissions that your organization doesn't allow. Follow these steps to configure this setting:

1. Select an extension.
1. Select **Manage permissions**. You can choose to use the default permissions that were defined in the profile settings or change these permissions. Use the **Permissions** window to allow all permissions, or customize permissions by choosing certain permissions that aren't allowed.
1. Select **Save**.

##### Edit minimum version

Specify the minimum version required for the extension. The extension will be disabled if it's a version older than what's specified, even if its installation policy is forced. The format of the version string is the same as the one used in the extension manifest. Follow these steps to configure this setting:

1. Select an extension.
1. Select **Edit minimum version**. In the **Minimum version required** window, enter the minimum version in the textbox.
1. Select **Save**.

##### Manage toolbar state

Choose how an extension is displayed in the toolbar. Follow these steps to configure this setting:

1. Select an extension.
1. Under **Toolbar state**, choose one of the following options:

   - Hidden: This is the default setting.
   - Shown: Show the extension on installation. Users can hide it from the toolbar.
   - Force shown: Always show extension on the toolbar. Users won't be able to hide it from the toolbar.

1. Select **Save**.

### View extension requests

> [!NOTE]
> The Extension Feedback feature is available in Edge Stable 116 and later. This will start rolling out after Microsoft Edge Stable 116 is available, which means you'll see the feature on 09/07/2023.

If you blocked all extensions for your organization, you can see the extensions that your users are attempting to install. To view these extensions, go to a configuration profile and go to **Requests** in the **Extensions** pivot. You can then change the installation policy for these extensions to let users install it. To allow requests, use the [EdgeManagementExtensionsFeedbackEnabled](/deployedge/microsoft-edge-policies#edgemanagementextensionsfeedbackenabled) policy to enable reporting.

To enable reporting, use these steps:

1. Select a configuration profile you want to enable it for.
2. Under the policies pivot, select **Select policy**.
3. Under **Configure a policy**, search for [EdgeManagementExtensionsFeedbackEnabled](/deployedge/microsoft-edge-policies#edgemanagementextensionsfeedbackenabled) and set its value to Enabled.
4. Select **Save**.

To set the installation policy on a requested extension, use these steps:

1. Select an extension.
2. Select **Manage installation policy** and choose one of the following options from the dropdown list:
   - Allow: Users can install the extension. This is the default setting.
   - Block: Users can't install the extension. You can remove the extension if a user previously installed it. Also, you can write a message that displays when users try to install the extension.
   - Force: The extension is automatically installed. Users can't remove it. You can optionally specify an update URL for the initial extension installation and use it for subsequent updates.
   - Normal: The extension is automatically installed. Users can disable it. You can optionally specify an update URL for the initial extension installation and use it for subsequent updates.

3. Select **Save**.

#### Manage sidebar apps

To manage sidebar apps for a profile, go to the profile and navigate to the **Extensions** pivot. You can allow, block, or force enable specific sidebar apps.

Use the following steps to manage sidebar apps:

1. Select **Select extension**.
1. Under **Select an extension**, navigate to the **Sidebar apps** pivot and select an app.
1. Select **Select**.

After selecting a sidebar app, you can configure its installation policy to Allow, Block, or Force.

#### Manage enterprise secure AI settings

To manage enterprise secure AI settings for a profile, select the configuration profile you want to work with and then select the **Customization settings** pivot. You can configure AI related policies on this page. Any policy that's edited on this page will appear in the **Policies** pivot for that profile. You can configure policies for Copilot, as well as other policies that incorporate the use of AI. If you edit a policy on his page that already has a policy value, the new edit will override the existing value.

##### Manage settings for Copilot

The page will detect whether your organization has access to Copilot and the Microsoft Edge sidebar. Based on this information, one of the following states will exist:

- If Copilot and the Microsoft Edge sidebar are enabled, all policy settings in this section will be available to configure.

- If Copilot is enabled and the Microsoft Edge sidebar is disabled, the unapplicable settings will be disabled. However, the option to enable the sidebar will appear, and if enabled, will unlock the ability to configure the now applicable setting.

- If Copilot is disabled, all policy settings in this section won't be available to configure.

- If it can't be identified that Copilot is enabled for your organization, the default policy settings for this section will pertain and won't be available to configure.

##### Manage settings for other AI features

The settings in this section correspond to a Microsoft Edge browser policy that incorporates the use of AI. When a setting is configured for the first time, the updated value will appear in the **Policies** pivot for that configuration profile. To configure a setting:

1. Check/uncheck the box corresponding to the setting that you want to enable/disable respectively.
1. Select **Save changes**.

<!-- =================================================== -->
## Configure Microsoft Edge to use a configuration profile

After configuring a profile, the next step is to assign the profile.  

> [!NOTE]
> Any policies you apply with Microsoft Edge management service will be overridden if they conflict with an existing Group Policy Object (GPO) or Mobile Device Management (MDM) policy that's set on the device.

### Enable the Microsoft Edge management service

Use the following sections as a guide to enable the Microsoft Edge management service.

#### For Microsoft Edge version 115.1935 and later

Microsoft Edge management service is enabled by default. Work profiles signed in with Microsoft Entra accounts will check with the Edge management service for any policies assigned to them. If an enrollment token is configured through device management, that token will be used. To disable the checking in with the Edge management service you can set the [EdgeManagementEnabled](/deployedge/microsoft-edge-policies#edgemanagementenabled) policy to 0 or disabled.

### Set an enrollment token

Use the following sections as a guide to setting an enrollment token.

#### For Microsoft Edge version 115.1935 and later

If you don't want to assign the profile using group assignment in the Microsoft 365 Admin Center, then you can assign it through group policy. Each profile has a unique profile ID which is the value you can use for the [EdgeManagementEnrollmentToken](/deployedge/microsoft-edge-policies#edgemanagementenrollmenttoken) policy to assign the profile. After assignment, the users will receive the profile and the settings will be applied when they're signed into the Edge browser. These policies will be applied in addition to any from group assignment in the Microsoft 365 Admin Center.

Use these steps as a guide for setting an enrollment token:

1. Sign in to the Microsoft 365 Admin Center. Go to **Settings** > **Microsoft Edge**. Under the **Configuration profiles** pivot, select the profile you want to assign and then select **Copy token ID**.
2. Set the [EdgeManagementEnrollmentToken](/deployedge/microsoft-edge-policies#edgemanagementenrollmenttoken) policy value to the token ID. 
3. If Microsoft Edge is open, restart it.

#### Control policy source precedence

As stated previously, if policy is set in MDM or GPM, that value will override any value provided by Microsoft Edge management service. If you want the Microsoft Edge management service policy to override MDM/GPM policy you can set the override in the  [EdgeManagementPolicyOverridesPlatformPolicy](/deployedge/microsoft-edge-policies#edgemanagementpolicyoverridesplatformpolicy) policy. This is a private policy and must be set via the registry.

Set the value of [EdgeManagementPolicyOverridesPlatformPolicy](/deployedge/microsoft-edge-policies#edgemanagementpolicyoverridesplatformpolicy) under the key `SOFTWARE\Policies\Microsoft\Edge` in either `HKLM` or `HKCU`. If the key isn't there you can create it. In the following command line example, remember to use your token ID and restart Microsoft Edge if it's open.

```
reg add HKLM\Software\Policies\Microsoft\Edge /v EdgeManagementPolicyOverridesPlatformPolicy /t REG_ DWORD /d 1 
```

#### Control user/device policy precedence

Microsoft Edge policy has the concept of the audience that the policy is meant to apply to, this can be either "User" or "Device". In Microsoft Edge management service, the policy applied via Group Assignment is applied as User Policy, while policy pulled down via [EdgeManagementEnrollmentToken](/deployedge/microsoft-edge-policies#edgemanagementenrollmenttoken) is applied as Device Policy.

If there's a conflict with policy that User and Device are both trying to set, Device Policy takes precedence over User Policy. If you want to give User Policy precendence you can change precedence in [EdgeManagementUserPolicyOverridesCloudMachinePolicy](/deployedge/microsoft-edge-policies#edgemanagementuserpolicyoverridescloudmachinepolicy) policy.

1. You can set precedence via the registry by setting the value of "EdgeManagementUserPolicyOverridesCloudMachinePolicy" under the key `SOFTWARE\Policies\Microsoft\Edge` in either `HKLM` or `HKCU`. If the key isn't there, create it.
2. Add the reg key using the following command line example as a guide. (Remember to use your profile ID.)

   ```
   reg add HKLM\Software\Policies\Microsoft\Edge /v EdgeManagementUserPolicyOverridesCloudMachinePolicy /t REG_ DWORD /d 1 
   ```

3. If Microsoft Edge is open, restart it.

#### How the configuration profile is applied

The Click-to-Run service used by Microsoft Edge management service checks with Cloud Policy regularly to see if there are any configuration profiles that pertain to the user. If there are, then the appropriate policy settings are applied and take effect the next time the user opens Microsoft Edge.

**Here's a summary of what happens:**

- When a user signs into Microsoft Edge on a device for the first time, a check is immediately made to see if there's a configuration profile that pertains to the user.
- If the user isn't a member of a Microsoft Entra group that's assigned a configuration profile, then another check is made again in 24 hours.
- If the user is a member of a Microsoft Entra group that's assigned a configuration profile, then the appropriate policy settings are applied. A check is made again in 90 minutes.
- If there are any changes to the configuration profile since the last check, then the appropriate policy settings are applied and another check is made again in 90 minutes.
- If there aren't any changes to the configuration profile since the last check, another check is made again in 24 hours.
- If there's an error, a check is made when the user opens Microsoft Edge.
- If Microsoft Edge isn't running when the next check is scheduled, then the check will be made the next time the user opens Microsoft Edge.

> [!NOTE]
>
> - Policies from Cloud Policy are only applied when Microsoft Edge is restarted. The behavior is the same as with Group Policy. For Windows devices, policies are enforced based on the primary user that is signed into Microsoft Edge. If there are multiple accounts signed in, only policies for the primary account are applied. If the primary account is switched, most of the policies assigned to that account will not apply until Microsoft Edge is restarted. Some policies related to [privacy controls](/deployoffice/privacy/overview-privacy-controls) will apply without restarting Microsoft Edge.
> - If users are located in nested groups and the parent group is targeted for policies, the users in the nested groups will receive the policies. The nested groups and the users in those nested groups must be created in or synchronized to Microsoft Entra ID.
> - If the user is a member of multiple Microsoft Entra groups with conflicting policy settings, priority is used to determine which policy setting is applied. The highest priority is applied, with "0" being the highest priority that you can assign. You can set the priority by choosing **Reorder priority** on the **Configuration profiles** page.

<!-- ====================================================================== -->
## Feedback and support

This experience is supported by [Microsoft Support](https://support.microsoft.com/microsoft-edge). You can reach out to Microsoft Support to report issues or give feedback. You can also leave feedback in our [TechCommunity forum](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise).
<!-- ====================================================================== -->
## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
