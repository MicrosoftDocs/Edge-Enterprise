---
title: "Microsoft Edge and Conditional Access"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 07/27/2023
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Microsoft Edge support for Conditional Access"
---

# Microsoft Edge and Conditional Access

> [!NOTE]
> Microsoft Edge for Business, the new, dedicated work experience for Microsoft Edge, is in preview today! [Try Microsoft Edge for Business](/deployedge/microsoft-edge-for-business), including the switching between work and personal browsing, and let us know what you think.
  
This article describes how Microsoft Edge supports Conditional Access, and how to access resources protected by Conditional Access.

A key aspect of cloud security is identity and access when it comes to managing your cloud resources. In a mobile-first, cloud-first world, users can access your organization's resources using various devices and apps from anywhere. As a result of this, just focusing on who can access a resource isn't sufficient. You also need to factor in how a resource is accessed. Azure Active Directory (Azure AD) Conditional Access helps you master the balance between security and productivity.

## Accessing Conditional Access protected resources in Microsoft Edge

Microsoft Edge natively supports Azure AD Conditional Access. There's no need to install a separate extension. When you're signed into a Microsoft Edge profile with enterprise Azure AD credentials, Microsoft Edge allows seamless access to enterprise cloud resources protected using Conditional Access.

The respective Azure AD account needs to be connected to Windows, so a [Primary Refresh Token](/azure/active-directory/devices/concept-primary-refresh-token) is sent along with the request for evaluation in the Conditional Access policy. To add a work or school account to Windows, follow these steps to [Add or remove accounts on your PC](https://support.microsoft.com/windows/add-or-remove-accounts-on-your-pc-104dc19f-6430-4b49-6a2b-e4dbd1dcdf32#WindowsVersion=Windows_10). There are limits to the number of work or school accounts connected to Windows, which is documented in this [device management FAQ](/azure/active-directory/devices/faq#i-can-t-add-more-than-3-azure-ad-user-accounts-under-the-same-user-session-on-a-windows-10-11-device--why). Note that with Microsoft Edge for iOS and Android version 108 or later, a device registered in Azure AD can provide a Device ID without signing into Microsoft Edge.

On a compliant device, the identity accessing the resource should match the identity on the profile. If it doesn't, you'll see a message like the one in the following screenshot. In this example, `testadmin@evostsoneboxtest.com` is the sign-in account needed to access the resource.

> [!NOTE]
> If a device isn't compliant, see [Mobile Application Management (MAM) for unenrolled devices in Microsoft Intune](#mobile-application-management-mam-for-unenrolled-devices-in-microsoft-intune) in this article.

![Conditional access message in browser](./media/edge-security/microsoft-edge-security-conditional-access.png)

To continue, you have to switch to the required profile (if you have one) or create a profile with matching identity.

To sign in and work with your profile, select the account picture in the top right corner of the browser. You can use the dropdown menu to complete the following tasks:

- Manage your profiles - Click the gear icon (**Manage profile settings**) to open Edge Settings.
- Pick an existing profile - Select the profile name.
- Create a personal profile - Select **Set up a new personal profile**.
- Create a new work profile - Select **Other profiles** and then select **Set up a new work profile**. The "Other profiles" option also lets you **Browse as guest** or **Browse in Kids Mode**.

This support is available across all platforms, including all supported versions of Windows and macOS.

> [!NOTE]
> Conditional Access isn't supported in InPrivate mode because there's no concept of a signed in profile for this mode.

### How to deploy Conditional Access in Azure Active Directory

[Plan a Conditional Access deployment](/azure/active-directory/conditional-access/plan-conditional-access) provides a detailed guide to help plan and deploy Conditional Access in Azure Active Directory.

## Mobile Application Management (MAM) for unenrolled devices in Microsoft Intune

MAM for unenrolled devices is commonly used for personal or bring your own devices (BYOD). MAM is an option for users who don't enroll their personal devices, but still need access to organization email, Teams meetings, and more.  For more specific information on MAM, see Microsoft Intune app management.

Conditional access might be blocked for the following reasons.

##### The user isn't signed into Microsoft Edge

Your admin might require users to be signed into Microsoft Edge to get access to MAM protected resources. Select **Switch Edge profile** and Microsoft Edge will guide you through the sign in process. For more information, see [Require an app protection policy on Windows devices (preview)](/azure/active-directory/conditional-access/how-to-app-protection-policy-windows).

##### There's an account issue

If there's a pre-existing, unregistered account, like `user@contoso.com` in Microsoft Edge, or if a user signs in without registering using the **Heads Up** page, then the account isn't properly enrolled in MAM. This configuration blocks the user from being properly enrolled in MAM. To fix this, sign in by entering the email address using different upper/lower case combinations. For example, if `RenataHall@fourthcoffee.com` was previously used to sign in, use `renatahall@fourthcoffee.com` to sign in. The user is shown a prompt. Clear the **Allow my organization to manage my device box** and then select **OK**. This action registers the device with your account and you'll be able to access your resources.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Video: Security, compatibility, and manageability](/deployedge/microsoft-edge-video-security-compatibility-manageability)
