---
title: "Browse more safely with Microsoft Edge"
ms.author: pchiquini
author: dan-wesley
manager: robfranco
ms.date: 02/4/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Learn how enhanced security supports safer browsing with Microsoft Edge."
---
# Browse more safely with Microsoft Edge

This article describes how Microsoft Edge provides safer browsing to enhance your security on the web.

## Overview

Microsoft Edge is designed to give you more control over your browser’s security when browsing the web and visiting unfamiliar sites. With enhanced security, users can browse the unfamiliar parts of the web more securely, protected by additional security mitigations and protections.

The web platform has a lot of power designed to give site visitors a smooth and intuitive browsing experience using Javascript, web notifications, permissions, and so on. That power can translate to more exposure when a user visits an untrustworthy site. By empowering you to enhance your security on Microsoft Edge, we're shifting conventional and well-established assumptions on how we think about protecting users from the unknown and unfamiliar.  

This feature aims to raise the security bar against V8-related exploits and neutralize them. Effective neutralization is achieved by running JIT-less engines and enabling additional guards for the browser.

## About “Enhance your security on the web”

This feature aims to raise the security bar against V8-related exploits and neutralize them. Effective neutralization is achieved by disabling just-in-time (JIT) JavaScript compilation and enabling advanced security guard rails included in the Windows operating system. These protections include Control-flow Enforcement Technology (CET), Arbitrary Code Guard (ACG), and Control Flow Guard (CFG) for the rendering process. These changes and protections make more difficult than ever before for a malicious site to write to executable memory and attack an end user.

You can learn more about the experimentation results from the Microsoft Edge Security team’s [blog post](https://microsoftedge.github.io/edgevr/posts/Super-Duper-Secure-Mode).

> [!NOTE]
> Sites that use WebAssembly are not currently supported in this mode. If you require access to a  site that needs WebAssembly, consider adding it to your exception list as described below.

## What's new in Microsoft Edge security settings

With **Enhance your security on the web**, Microsoft Edge puts your browser in a mode where the security of your browser takes priority, giving you an extra layer of protection when browsing the web.

Use the following steps to set your security level.

1. In Microsoft Edge, go to **Settings and more** > **Settings** > **Privacy, search, and services**.
2. Under **Security**, verify that **Enhance your security on the web** is enabled.
3. Select the option that's best for your browsing.

The following toggle settings are available:

- Toggle Off (Default): Feature is turned off
- Toggle On – Balanced (Recommended): In this mode, your frequently browsed sites will be left out. The feature will only turn on when you browse sites that you don’t engage with often or are unknown to you.
- Toggle On – Strict: This will turn on the feature for all the sites you visit.

Select the option that’s best for your browsing.

The following screenshot shows the "Enhance your security on the web" dialog, enabled and set to provide Balanced security.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-enhance-security-dialog.png" alt-text="Dialog to configure balanced security on the web.":::

## How "Balanced" mode works

Balanced mode is an adaptive mode that builds on user’s behavior on a particular device, and Microsoft’s understanding of risk across the web to give sites that users are most likely to use and trust full access to the web platform, while limiting what new and unfamiliar sites can do.

Each user will have their own unique site list, automatically populated based on their behavior and manually adjusted, to provide a tailored experience. A list that’s unique to each user means that attackers must predict which sites the user trusts, which makes broad exploitation more difficult.

The feature doesn’t have a single centralized list of sites. This strategy is designed to reduce the risk of attack where an attacker can exploit an XSS vulnerability in a site and use that vulnerability to attack other sites in the list. In contrast, each user will have their own unique site list, manually or intelligently populated to provide a tailored experience. A list that’s unique to each user means that an attacker must predict which sites the user trusts, which makes exploitation more difficult.

The next figure shows the three categories of exceptional site lists, based on how they're managed.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-site-list-categories.png" alt-text="Types of site lists based on handling":::

### Automatic exception list

Many users want a high level of control, and we believe that most of them prefer to have many aspects of security automatically managed while still offering manual site list management. To address this, "Enhance your security on the web" uses how often you visit a particular site. Site engagement scores are computed on your device and never leave it. This means that they're not synced across your devices or sent to Microsoft at any time.

> [!TIP]
> Site engagement scores can range from 0 (the user has no relationship with the site) to 100 (the user is heavily engaged with the site). You can view your own site engagement scores on your PC or device by going to *edge://site-engagement*.

Microsoft Edge uses these scores to learn from your behavior on a particular device and dynamically adjust which sites are automatically opted into this new more secure mode and which are not on that device. That is, sites you use most often will be treated the same way as users treat most of the web today. In contrast, when a user navigates unfamiliar sites (sites not visited often) the browser will enter in this new mode. We’re not claiming they’re bad sites; we’re saying they’re unfamiliar to you. This being the case, we want to be more deliberate about what surface area is exposed to these sites.

### Manual exception list

You might want to create exceptions for certain familiar websites that you trust. Any site you add as an exception will always have this security feature turned off. The following steps show how to add a site to your exception list.

1. In Microsoft Edge, select **Settings and more** > **Settings** > **Privacy, search, and services**.
2. Verify that **Enhance your security on the web** is turned on.
3. Under **Enhance your security on the web**, select **Exceptions**.
4. Select **Add a site**, type in the full URL, and then select **Add**.

> [!NOTE]
> You can use steps (1 - 3) to view sites in **Enhanced security exceptions**. You can **Edit** a site, **Remove** a site, or **Remove all** exceptions.

The next screenshot shows the dialog for security exceptions.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-enhanced-exceptions.png" alt-text="Dialog for configuring security exceptions":::

### Enterprise controls

Enterprise Admins can configure this security feature using Group Policy settings, including creating “Allow” and “Deny” lists to explicitly enhance security for their users when visiting certain sites, or disable the mode for others. For a complete list of policies, see the [Microsoft Edge browser policy documentation](/deployedge/microsoft-edge-policies).

## User experience with enhanced security

After a user turns on enhanced security, they'll see a banner with the words "Added security" in their URL navigation bar when they visit certain sites. This banner means that the current site is  protected with extra security mitigations as described above.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-added-security-banner.png" alt-text="Banner showing that added security is turned on.":::

When you click on the banner, you'll see the following flyout. In addition to the other security and privacy features in Microsoft Edge, this new security feature will be listed on the flyout as "Enhance security for this site". You can use this dialog to toggle enhanced security for the site on or off. The next screenshot shows the feature turned off for the site.  

> [!NOTE]
> This only appears when enhanced security is turned on.

The toggle setting you pick will be remembered the next time you go to the site. Additionally, when you turn the toggle off, the site will be automatically added to your Manual site list. This results in the site being added to your Exceptions directly from the browser without opening the **Settings** page. The next screenshot shows the dialog when enhanced security is turned off.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-enhanced-security-off.png" alt-text="Dialog with enhanced security turned off.":::

In contrast, if the toggle's turned on, the site will automatically be removed from your Manual site list. The next screenshot shows the dialog when enhanced security is turned on.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-enhanced-security-on.png" alt-text="Dialog with enhanced security turned on.":::

## Send us feedback

We want to get your feedback on our next iteration to improve "Enhance security on the web". If something doesn't work the way you expect, or if you have feedback to share on these changes, we want to hear from you. You can reach out to Microsoft Support to report issues or feedback. You can also leave feedback in our [TechCommunity forum](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise).

## See also

- [Video: Secure browsing on Microsoft Edge](microsoft-edge-video-security-smartscreen.md)
- [Super Duper Secure Mode](https://microsoftedge.github.io/edgevr/posts/Super-Duper-Secure-Mode/)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)