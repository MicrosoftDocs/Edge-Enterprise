---
title: "Organization branding"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 04/12/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Information customizing organization branding."
---

# Organization branding

This document provides a guide to understanding and using organization branding within Microsoft Edge for Business.

## Introduction

Want to customize the look of Edge for Business?

Now you can customize your organization's branding in Edge for Business. This branding can help users signed in with a Microsoft Entra ID (formerly known as Azure Active Directory) more easily differentiate between multiple profiles and browser windows through visual cues on the profile pill, profile flyout, and Edge for Business taskbar icon. Organization branding  also allows companies to foster employee trust through customized branding, while growing affinity by serving an effective brand reinforcement strategy.

![Company branding for Contoso](media/microsoft-edge-organization-branding/efb-company-branding-new.png)

## Branding support

Organization branding isn't supported for:

* Government - GCC tenants
* Intune MAM
* Microsoft Edge for mobile devices
* The following aspects of macOS:
  - Deploying Edge management service organization branding configuration to the macOS.
  - Overlaying the organization Logo on the Edge for Business taskbar icon.

## Organization branding assets

You will have the option to use the default Edge for Business branding elements or customize branding for your organization.

You can apply the following elements of your organization's branding in Edge for Business:

* Name
* Color
* Logo
* Edge for Business Icon Overlay

Today, the feature supports configuring the following UI options:

* Organization name to the profile pill
* Organization name, logo, and color to the profile flyout
* Organization icon to overlay the Edge for Business taskbar icon

## Customize organization branding through the Microsoft Edge management service

> [!NOTE]
> This experience is in public preview and you can access it by opting in to targeted release in the Microsoft 365 Admin Center. Sign in to your account and go to **Settings** > **Org settings** > **Organization profile** > **Release preferences**, and then select the targeted release option.

The Edge management service provides admins with an enhanced experience to control, preview, and customize Edge for Business.

To customize the Microsoft Edge browser with your organization's branding assets, sign in to the Microsoft 365 Admin Center and go to the **Organization branding** tab in the **Customization Settings** pivot within a configuration profile. A preview of how the browser elements look on a user's account is shown on the page.

If you don't have any branding policies enabled, the default Edge for Business branding will be displayed. When you choose **Use custom branding**, any existing branding assets associated with your Microsoft Entra ID are imported and displayed in the preview. These changes will not take effect until you choose **Save changes**.

From **Use custom branding**, you can customize each of the following browser elements with the brand assets you choose:

* Organization name: This name is displayed in the profile pill.
* Accent color: This color appears in the profile flyout header.
* Organization logo: This logo appears in the profile flyout header. You must upload an SVG (Scalable Vector Graphics) file with a maximum size of 150 KB.
* Taskbar icon: This logo overlays the Edge for Business icon on the taskbar. You must upload an SVG file with a maximum size of 150 KB (we recommend choosing a square logo).

  > [!TIP]
  > Square and horizontal logos provide the optimal visual branding experience.

After you finish customizing the browser elements with your organization branding assets, confirm that the preview displays the correct visual appearance and then select **Save changes**.

### Use defaults from Entra

Admins can choose to use and check default organization branding assets already configured in the Microsoft Entra admin center. Default branding can be enabled by admins through the following policies:

* [OrganizationalBrandingOnWorkProfileUIEnabled](/deployedge/microsoft-edge-policies#organizationalbrandingonworkprofileuienabled)
* [OrganizationLogoOverlayOnAppIconEnabled](/deployedge/microsoft-edge-policies#organizationlogooverlayonappiconenabled)

For more details on defaults and checking what is already configured in Microsoft Entra, [check your existing company branding](/entra/fundamentals/how-to-customize-branding).

## See also

* [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business)
* [Microsoft Edge management service](/deployedge/microsoft-edge-management-service)
