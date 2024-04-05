---
title: "Organizational branding"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 04/05/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Information customizing organizational branding."
---

# Organizational branding

This document provides a guide to understanding and using branding for an organization.

## Introduction

Want to customize the look of Edge for Business?
Now you can customize your organization's branding onto Edge for Business. This branding can help users signed in with an Entra ID (formerly known as Azure Active Directory) more easily differentiate between multiple profiles and browser windows through visual cues on the profile pill, profile flyout, and Edge for Business taskbar icon. This visual option also allows companies to foster employee trust through specifically customized branding, while growing affinity by serving an effective brand reinforcement strategy.

![Company branding for Contoso](media/microsoft-edge-organization-branding/efb-company-branding-new.png)

> [!NOTE]
> This experience is in public preview and you can access it by opting in to targeted release in the M365 Admin Center. Sign in to your account and go to **Settings** > **Org settings** > **Organization profile** > **Release preferences**, and then select the targeted release option.

## Organization branding assets

You can use the default Edge for Business branding elements or customize branding for your organization.

### Use Defaults from Azure

Admins can choose to use and check default organization branding assets already configured in the Microsoft Entra admin center. Default branding can be enabled by admins through the following policies:

- [OrganizationalBrandingOnWorkProfileUIEnabled](/deployedge/microsoft-edge-policies#organizationalbrandingonworkprofileuienabled)
- [OrganizationLogoOverlayOnAppIconEnabled](/deployedge/microsoft-edge-policies#organizationlogooverlayonappiconenabled)

For more details about branding defaults and checking what's already configured in Microsoft Entra, [check your existing company branding](/entra/fundamentals/how-to-customize-branding).

### Customizable branding elements

Through the Microsoft Edge management service, admins have an enhanced experience to control, preview, and customize how Edge for Business shows the following organization brand assets:

- Name
- Color
- Logo
- Edge for Business icon overlay

The feature currently supports configuring the following UI options:

- Organization name to the profile pill.
- Organization name, logo, and color to the profile flyout.
- Organization icon to overlay the Edge for Business taskbar icon.

To customize the Microsoft browser with your organization's branding assets, sign in to the M365 Admin Center and go to the **Organization branding** tab. A preview of how the browser elements will look on a user's account is shown on the page.

If you don't have any branding policies enabled, the default Edge for Business branding will be displayed. When you choose **Use custom branding**, any existing branding assets associated with your Microsoft Entra ID will be imported and displayed in the preview. These changes won't take effect until you choose **Save changes**.

From **Use custom branding**, you can customize each of the following browser elements with the brand assets you choose:

- Organization name: This name will be displayed in the profile pill.
- Accent color: This color will appear in the profile flyout header.
- Organization logo: This logo will appear in the profile flyout header. You must upload a SVG (Scalable Vector Graphics) file with a maximum size of 150KB.
- Taskbar icon: This logo will overlay the Edge for Business icon on the taskbar. You must upload a SVG file with a maximum size of 150KB (we recommended choosing a square logo).

  > [!TIP]
  > Square and horizontal logos will provide the optimal visual branding experience.

After you finish customizing the browser elements with your organization branding assets, confirm that the preview displays the correct visual appearance and then select **Save changes**.

## See also

- [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business)
- [Microsoft Edge management service](/deployedge/microsoft-edge-management-service)
