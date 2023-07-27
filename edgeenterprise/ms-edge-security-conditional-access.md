---
title: "Microsoft Edge and Conditional Access"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 07/10/2023
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

The respective Azure AD account needs to be connected to Windows, so a [Primary Refresh Token](/azure/active-directory/devices/concept-primary-refresh-token) is sent along with the request for evaluation in the Conditional Access policy. To add a work or school account to Windows, follow these steps to [Add or remove accounts on your PC](https://support.microsoft.com/windows/add-or-remove-accounts-on-your-pc-104dc19f-6430-4b49-6a2b-e4dbd1dcdf32#WindowsVersion=Windows_10). Bear in mind there are limits to the amount of work or school accounts connected to Windows, as documented in this [device management FAQ](/azure/active-directory/devices/faq#i-can-t-add-more-than-3-azure-ad-user-accounts-under-the-same-user-session-on-a-windows-10-11-device--why). Note that Microsoft Edge for iOS and Android version 108 or later, a device registered in Azure AD can provide a Device ID without sign in to Microsoft Edge.

On a compliant device, the identity accessing the resource should match the identity on the profile.  If it doesn't, you'll see a message like the one in the next screenshot. In the screenshot example, "testadmin@evostsoneboxtest.com" is the sign-in account needed to access the resource.

![Conditional access message in browser](./media/edge-security/microsoft-edge-security-conditional-access.png)

To continue, you have to switch to the required profile (if you have one) or create a profile with matching identity.

To sign in and work with your profile, select the account picture in the top right corner of the browser. You can use the dropdown menu to:

- Pick another profile. Select the profile name.
- Create a profile. Select **Add a profile**.
- Manage your profiles. Select **Manage profile settings**.

This support is available across all platforms, including all supported versions of Windows and macOS.

> [!NOTE]
> Conditional Access is not supported in InPrivate mode, as there's no concept of a signed in profile in this mode.

### How to deploy Conditional Access in Azure Active Directory

[Plan a Conditional Access deployment](/azure/active-directory/conditional-access/plan-conditional-access) provides a detailed guide to help plan and deploy Conditional Access in Azure Active Directory.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Video: Security, compatibility, and manageability](/deployedge/microsoft-edge-video-security-compatibility-manageability)
