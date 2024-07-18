---
title: "Microsoft Edge and Conditional Access"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 07/18/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Microsoft Edge support for Conditional Access"
---

# Microsoft Edge and Conditional Access

This article describes how Microsoft Edge supports Conditional Access (CA) for managed devices and how you can access CA protected resources with unmanaged devices.

## Introduction

When it comes to managing and protecting your cloud resources, identity and access are both important. In a hybrid computing world, users can access your organization's resources using various devices and apps from anywhere at anytime. Just focusing on who can access a resource isn't good enough. You also need to factor in how a resource is accessed.

Conditional Access (CA) gives you a balance between security and productivity. For more information, see [Plan a Conditional Access deployment](/azure/active-directory/conditional-access/plan-conditional-access), a detailed guide to help plan and deploy Conditional Access (CA) in Microsoft Entra ID (*formerly known as Azure Active Directory*). (For more information about this name change, see [New name for Microsoft Entra ID](/azure/active-directory/fundamentals/new-name).)

Microsoft Edge natively supports access to CA protected resources on both [managed](#accessing-ca-protected-urls-with-microsoft-edge-on-managed-devices) and [unmanaged](#accessing-ca-protected-urls-with-microsoft-edge-on-byod-using-intune-mam) devices.

> [!NOTE]
> We have exempted Edge Auth from device-based controls enforcement. It is no longer necessary to create a manual exclusion for this scope while setting up Conditional Access. Edge Auth is a prerequisite for connected profile creation in Microsoft Edge.

## Accessing CA protected URLs with Microsoft Edge on managed devices

Microsoft Edge natively supports Microsoft Entra (*formerly known as Azure Active Directory*) Conditional Access. There's no need to install a separate extension, Edge's native support provides stable and high quality access. When you're signed into an Edge profile with enterprise Microsoft Entra ID (*formerly known as Azure Active Directory*) credentials, Microsoft Edge allows seamless access to enterprise cloud resources protected using CA. This support is available across all platforms, including all supported versions of Windows and macOS.

The respective Microsoft Entra (*formerly known as Azure Active Directory*) account needs to be connected to Windows, so a [Primary Refresh Token](/azure/active-directory/devices/concept-primary-refresh-token) is sent along with the request for evaluation in the Conditional Access policy. To add a work or school account to Windows, follow these steps to [Add or remove accounts on your PC](https://support.microsoft.com/windows/add-or-remove-accounts-on-your-pc-104dc19f-6430-4b49-6a2b-e4dbd1dcdf32#WindowsVersion=Windows_10). Note that there are limits to the number of work or school accounts connected to Windows, which is documented in this [device management FAQ](/azure/active-directory/devices/faq#i-can-t-add-more-than-3-azure-ad-user-accounts-under-the-same-user-session-on-a-windows-10-11-device--why).

## Accessing CA protected URLs with Microsoft Edge on BYOD using Intune MAM

Mobile Application Management (MAM) for unenrolled devices is commonly used for personal or bring your own devices (BYOD). MAM is an option for users who don't enroll their personal devices, but still need access to their organization's email, Teams meetings, and more. For more specific information about MAM, see [What is Microsoft Intune app management?](/mem/intune/apps/app-management) and the [MAM FAQ](/mem/intune/fundamentals/deployment-guide-enrollment-mamwe). For more information about conditional access on Windows devices, see [Require an app protection policy on Windows devices](/azure/active-directory/conditional-access/how-to-app-protection-policy-windows).

## Access issues

On a compliant device, the identity accessing the resource should match the identity on the profile. If it doesn't or the device is unmanaged, access is blocked and you'll see a message like the one in the following screenshot. In this example, `balas@contos.com` is the sign-in account needed to access the resource.

![Conditional access message in browser](./media/edge-security/microsoft-edge-security-conditional-access.png)

### Fixing access issues with Microsoft Edge on managed devices

If access is blocked, you have to switch to the required profile or create a profile with a matching identity. Select **Switch Edge profile** and Microsoft Edge will guide you through the sign-in process. For more information, see [Require an app protection policy on Windows devices (preview)](/azure/active-directory/conditional-access/how-to-app-protection-policy-windows).

You can also work with profile settings by selecting the account picture in the browser and using the dropdown menu for the following tasks:

- Manage your profiles - Click the gear icon (**Manage profile settings**) to open Edge Settings.
- Pick an existing profile - Select the profile name.
- Create a personal profile - Select **Set up a new personal profile**.
- Create a new work profile - Select **Other profiles** and then select **Set up a new work profile**. The "Other profiles" option also lets you **Browse as guest** or **Browse in Kids Mode**.

[Troubleshoot Conditional Access policies](/azure/active-directory/conditional-access/plan-conditional-access#troubleshoot-conditional-access-policies) provides more information about fixing a CA issue.

### Fixing access issues with unenrolled devices using Intune MAM

Access issues, such as an expired enrollment, and their resolution are in [Troubleshooting](/azure/active-directory/conditional-access/how-to-app-protection-policy-windows#troubleshooting).

## See also

- [What is Conditional Access?](/azure/active-directory/conditional-access/overview)
- [Require an app protection policy on Windows devices](/azure/active-directory/conditional-access/how-to-app-protection-policy-windows)
- [Video: Security, compatibility, and manageability](/deployedge/microsoft-edge-video-security-compatibility-manageability)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
