---
title: "Organization branding"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 04/15/2024
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

Now you can with support for organization branding! This branding can help users signed in with a Microsoft Entra ID more easily differentiate between multiple profiles and browser windows through visual cues on the profile pill, profile flyout, and Edge for Business taskbar icon. Organization branding  also allows companies to foster employee trust through customized branding, while growing affinity by serving an effective brand reinforcement strategy.

![Company branding for Contoso](media/microsoft-edge-organization-branding/efb-company-branding-new.png)

## Organization branding assets

Admins have the options to use the default Edge for Business branding elements or choose to customize branding for their organization.
Today, the feature supports configuration of the following visual elements:

- Organization name on the profile pill
- Organization logo, and color on the profile flyout
- Organization icon overlay on the Edge for Business taskbar icon

## Use default organization branding assets from Entra

Admins can choose to use default organization branding assets that have already been configured in the Microsoft Entra admin center. Default branding customizations can be enabled by admins by deploying the following policies:
- [OrganizationalBrandingOnWorkProfileUIEnabled](/deployedge/microsoft-edge-policies#organizationalbrandingonworkprofileuienabled)
- [OrganizationLogoOverlayOnAppIconEnabled](/deployedge/microsoft-edge-policies#organizationlogooverlayonappiconenabled)

When these policies are enabled, any applicable assets in your existing Microsoft Entra admin center will be used for organization branding in Microsoft Edge for Business.

For more details on defaults and checking what is already configured in Microsoft Entra, check your existing company branding.

*The Edge for Business taskbar icon overlay is not supported for MacOS.*

## Customize organization branding through the Microsoft Edge management service

> [!NOTE]
> This experience is in public preview and you can access it by opting in to targeted release in the Microsoft 365 Admin Center. Sign in to your account and go to **Settings** > **Org settings** > **Organization profile** > **Release preferences**, and then select the targeted release option.

Looking for more advanced customization options? The Edge management service provides admins with an enhanced experience to control, preview, and customize the look of Edge for Business.

To customize the Microsoft Edge browser with your organization's branding assets, sign in to the Microsoft 365 Admin Center and go to the **Organization branding** tab in the **Customization Settings** pivot within a configuration profile. A preview of how the browser elements look on a user's account is shown on the page.

If you don't have any branding policies enabled, the default Edge for Business branding will be displayed. When you choose **Use custom branding**, any existing branding assets associated with your Microsoft Entra ID are imported and displayed in the preview. These changes will not take effect until you choose **Save changes**.
<!------ add EMX screenshot in this area ---------->
From **Use custom branding**, you can customize each of the following browser elements with the brand assets you choose:

- Organization name: This name is displayed in the profile pill.
- Accent color: This color appears in the profile flyout header.
- Organization logo: This logo appears in the profile flyout header. You must upload an SVG (Scalable Vector Graphics) file with a maximum size of 150 KB.
- Taskbar icon: This logo overlays the Edge for Business icon on the taskbar. You must upload an SVG file with a maximum size of 150 KB (we recommend choosing a square logo).

  > [!TIP]
  > Square and horizontal logos provide the optimal visual branding experience.

After you finish customizing the browser elements with your organization branding assets, confirm that the preview displays the correct visual appearance and then select **Save changes**.

*Note: Organization branding via Edge management service is currently not supported for:*

- *Microsoft Edge Mobile*
- *Microsoft Edge for Business on unmanaged PCs and MacOS*
- *Customers with an Office 365 GCC or Office 365 GCC High and DoD plan*

## See also

- [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business)
- [Microsoft Edge management service](/deployedge/microsoft-edge-management-service)
