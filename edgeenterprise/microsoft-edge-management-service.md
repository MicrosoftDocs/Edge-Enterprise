---
title: "Microsoft Edge management service"
ms.author: katherinegan
author: dan-wesley
manager: archandr
ms.date: 09/17/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Provides steps for configuring the Microsoft Edge management service."
---

# Microsoft Edge management service

The Microsoft Edge management service is a platform in the Microsoft 365 admin center that enables admins to easily configure Microsoft Edge browser settings for their organization. These configurations are stored in the cloud and the settings can be applied to a user's browser through group assignment or group policy. Users must be logged into Microsoft Edge to retrieve these settings.

<!-- ====================================================================== -->
## Prerequisites

- You must have Microsoft Edge 115.0.1901.7 or greater installed.
- You must be a [Microsoft Edge Administrator](/azure/active-directory/roles/permissions-reference#edge-administrator) to access the experience in Microsoft 365 Admin Center.
- You must be using one of the following supported operating systems: Windows 10/11 or Windows Server 2016 or later. See [Microsoft Edge Supported Operating Systems](/deployedge/microsoft-edge-supported-operating-systems) for specifics.

> [!IMPORTANT]
> The Microsoft Edge management service uses the Cloud Policy service, which currently isn't available to customers who have the following plans: Office 365 operated by 21Vianet, Office 365 GCC, or Office 365 GCC High and DoD. [Learn more about the Cloud Policy service for Microsoft 365](/deployoffice/admincenter/overview-cloud-policy#requirements-for-using-cloud-policy).

<!-- ====================================================================== -->
## Access the experience

Use these steps to access the experience:

1. Go to the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal/Home#/homepage) and login.
1. In the main left navigation bar, go to **Settings** > **Microsoft Edge**.  
<!-- ====================================================================== -->

> [!NOTE]
> Preview for an updated user interface is currently rolling out. Some strings and pages may differ slightly from the following information.

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
2. Under the **Policies** pivot, select **Select policy**.
3. Under **Configure a policy**, search for the policy you want to configure for this profile. Set the configuration settings/values for the policy you select. If the policy is able to be set as either mandatory or recommended, optionally choose to "Allow users to override" the policy.
4. Select **Save**.  

<a name='assign-a-configuration-profile-to-an-microsoft-entra-group'></a>

#### Assign a configuration profile to a Microsoft Entra group

Follow these steps to assign a configuration profile to a Microsoft Entra group:

1. Under the **Configuration profiles** pivot, select the profile you want to assign.
1. Under the **Group assignment** pivot, select **Select group**.
1. Under **Select a security group**, select the group to assign the profile to.
1. Select **Select**. The profile will now be applied to all users in the selected group.

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

1. Sign in to the Microsoft 365 Admin Center. Go to **Settings** > **Microsoft Edge**. Under the **Configuration profiles** pivot, select the profile you want to assign and then click **Deploy** to select **Copy profile ID**.
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

If there's a conflict with policy that User and Device are both trying to set, Device Policy takes precedence over User Policy. If you want to give User Policy precedence you can change precedence in [EdgeManagementUserPolicyOverridesCloudMachinePolicy](/deployedge/microsoft-edge-policies#edgemanagementuserpolicyoverridescloudmachinepolicy) policy.

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
