---
title: "Microsoft Edge for Business"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 05/19/2023
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Information about Microsoft Edge for Business Preview"
---

# Microsoft Edge for Business (Early Preview)

This article describes the benefits that Microsoft Edge for Business will bring to your users and explains how to enable this feature and its functions in your organization.

> [!NOTE]
> This is a preview feature. Preview features or services are in development and are available as a preview so you can get early access and send us feedback.

## Introduction

Microsoft Edge for Business is a new, dedicated Microsoft Edge experience built for work that enables admins in organizations to give their users a productive and secure work browser across managed and unmanaged devices.  It has the same rich set of enterprise controls, security, and productivity features that you're already familiar with in Microsoft Edge, but it's built to help meet the evolving needs of businesses.

This preview experience encompasses the features summarized in the following table.

| Name | Description | Status |
|:-----|:-----|:------|
|  Separation of work and personal profiles    |  Easily separate between visually different work and lightly managed personal profiles for better productivity and security.    |  Early preview <br> (Instructions below)   |
|  Automatic profile switching    |  Maintain seamless work and personal context separation automatically based on browsing patterns.   |  Early preview <br> (Instructions below)     |
|  Enterprise controls    | Natively built-in rich enterprise controls for secure data access and leak prevention.    |  Available     |
|  Unmanaged BYOPC    |  Secure and compliant access to work resources on personal computers.    |  Private Preview<br>
(Onboarding instructions below) |
|  Company branding   |  Increase familiarity and trust with company branding.    |  Coming soon     |

You enable Microsoft Edge for Business by logging into the browser using your Azure Active Directory (AAD) account. This ensures that all your M365 services are accessible in your profile. Users can enable the early preview using the *edge://flags/#edge-project-kodiak*.  The next section has more information about flags you can use to enable different aspects of this experience.

[Insert video from Build]

## About this early preview

The early preview will include some visual treatments for the work profile, a lightly managed personal profile, and automatic switching between work and personal profiles for a limited number of websites.

To enable the early preview, users need to use Microsoft Edge version 112 or higher.
Users can enable different aspects of the early preview with the following flags:
- *edge://flags/#edge-project-kodiak* (overall experience)
- *edge://flags/#edge-project-kodiak-look-and-feel* (work browser visual treatment)
- *edge://flags/#edge-project-kodiak-policy-filter* (lightly managed personal profile)
- *edge://flags/#edge-automatic-profile-switching* (automatic switching)

## The Microsoft Edge for Business user experience

Configuring and activating the user experience is straight forward and easy to do. First, the user opens Microsoft Edge on a work device to launch Microsoft Edge for Business. The next step is to enable the personal browser window in the profile flyout. After this one-time set up the user can start browsing as normal. Work related sites such as sites that need a user's work login and Microsoft 365 apps and services, will automatically open in the work browser window. A growing set of popular sites will automatically open in the personal browser window.

### Enable personal browsing for users

The personal browsing option will be enabled by default, and users will have the option to create a personal browser profile. You can turn off the personal profile with a policy that prevents Microsoft Edge from creating a new profile. If you've already configured this policy, then the personal browsing option will not be available to your users.

### Enable automatic switching for users

Automatic switching is enabled by default. There will be a separate automatic switching policy that can be disabled.

## Security and Compliance

The personal browser will have the same security and compliance posture as Microsoft Edge for Business. Controls for security and compliance will remain with IT, whether the user has Microsoft Edge for Business or the personal browser open.

## Provide feedback

Your feedback while using Microsoft Edge for Business is valuable because it helps us improve the product! You can leave feedback by (?)

## Frequently Asked Questions

### How can I correct the wrong switching decision made by the browser?

There are 2 ways to change switching:

- Use the following Omnibar Switching icon to switch back to the preferred profile. This action will make the browser remember your choice for that URL.
- Go to *edge://settings/profiles/multiProfileSettings* and select **Choose preferred browser for sites** to turn off or select a preferred profile for the applicable site.

### Does the switching preference sync across other Microsoft Edge channels?

No, currently it does not. You will have to make switching preferences on each channel separately.  

### What sites does it switch on?

- Amazon
- BestBuy
- Target
- Walmart

### How can users control which browser window a website will open in?

The option to manage how sites open will appear in the browsing window that opens following the selection to open the URL in a different browser. Additionally, users can manage and customize their Microsoft Edge for Business and personal URL lists by navigating to **Choose how external links open** in Microsoft Edge settings.

### Will favorites, history, and passwords be shared between the Edge for Business and personal browser windows?

No – browser favorites, history, and passwords will not be shared between the browser windows.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)