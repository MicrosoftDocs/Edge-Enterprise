---
title: "Browse safer within Microsoft Edge"
ms.author: pchiquini
author: dan-wesley
manager: robfranco
ms.date: 02/02/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Learn how enhanced security supports safer browsing within Microsoft Edge."
---
# Browse safer within Microsoft Edge

This article describes how Microsoft Edge supports enhancing your security on the web.

## Overview

Microsoft Edge is designed to give you more control over your browser’s security when browsing the web and visiting unfamiliar sites. With enhanced security, users can browse the unfamiliar parts of the web more securely, protected by additional security mitigations and protections.

The web platform has a lot of power designed to give site visitors a smooth and intuitive browsing experience using Javascript, web notifications, permissions, and so on. That power can translate to more exposure when a user visits an untrustworthy site. By empowering you to enhance your security on Microsoft Edge, we're shifting conventional and well-established assumptions on how we think about protecting users from the unknown and unfamiliar.  

This feature aims to raise the security bar against V8-related exploits and neutralize them. Effective neutralization is achieved by running JIT-less engines and enabling additional guards for the browser. From an historical perspective, in 2021, 41% of in-the-wild exploits were mitigated with this security feature alone.

## About this security feature

The core of this feature starts by disabling the just-in-time (JIT) compiler in V8, to protect your browser with a series of protective guards. These protections include Control-flow Enforcement Technology (CET), Arbitrary Code Guard (ACG), and Control Flow Guard (CFG) for the rendering process. Additionally, running JIT-less V8 will block writing to executable memory, which reduces the attack surface of the application for exploits.

You can learn more about the experimentation results from the Microsoft Edge Security team’s [blog post published back in August 2021](https://microsoftedge.github.io/edgevr/posts/Super-Duper-Secure-Mode).

> [!NOTE]
> Web Assembly isn’t currently supported in this mode. We're working on Web Assembly support over the next few months as we continue testing, experimenting, and further developing the feature.

## What's new in Microsoft Edge security settings

With **Enhance your security on the web**, Microsoft Edge puts your browser in a mode where the security of your browser takes priority, giving you an extra layer of protection when browsing the web. You’ll still enjoy browsing when visiting top sites.

Use the following steps to set your security level.

1. In Microsoft Edge, go to **Settings and more** > **Settings** > **Privacy, search, and services**.
2. Under **Security**, verify that **Enhance your security on the web** is enabled.
3. Select the option that's best for your browsing.

The following toggle settings are available:

- Toggle Off (Default): Feature is turned off
- Toggle On – Balanced (Recommended): In this mode, your frequently browsed sites will be left out. The feature will only turn on when you browse sites that you don’t engage with often or are unknown to you.
- Toggle On – Strict: This will turn on the feature for all the sites you visit.

Select the option that’s best for your browsing.

The following screenshot shows the **Enhance your security on the web** dialog, enabled and set to provide Balanced security.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-enhance-security-dialog.png" alt-text="Dialog to configure balanced security on the web.":::

## Site list Exceptions

Enhancing your security doesn’t have a single centralized list of sites. This strategy is designed to reduce the risk of attack where an attacker can exploit an XSS vulnerability in one a site and use that vulnerability to attack other sites in the list. In contrast, each user will have their own unique site list, manually or intelligently populated to provide a tailored experience. A list that’s unique to each user means that an attacker must predict which sites the user trusts, which makes exploitation more difficult.

The next drawing shows the three categories of sites in an exception site list, based on how they're managed.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-site-list-categories.png" alt-text="Types of site lists based on handling":::

### Intelligent site list

Many users want a high level of control, and we believe that most of them prefer to have many aspects of security feature automatically managed while still offering manual site list management. To address this, enhancing your security on the web uses an algorithm that runs locally in the browser. It’s also worth noting that site engagement scores are computed on your device and never leave it. This means that they're not synced across your devices or sent to Microsoft at any time.

> [!TIP]
> Site engagement scores can range from 0 (the user has no relationship with the site) to 100 (the user is heavily engaged with the site). You can view your own site engagement scores by going to *edge://site-engagement*.

Furthermore, this algorithm learns from your behavior and manages the site list for you. That is, sites that users use most often will be treated the same way as users treat most of the web today. These sites can use JIT code and opt out the extra layer of security because of their familiarity and engagement frequency. In contrast, when a user navigates unfamiliar sites (sites not visited often) the site will enter in this new secure mode. We’re not claiming they’re bad sites; we’re saying they’re unfamiliar to you and Microsoft Edge. This being the case, we want to be more deliberate about what surface area is exposed to these sites.

### Manual site list

Users can manually add their own exceptions for their familiar websites. Adding a site to your unshared site list will remove the extra layer of protection to keep a site’s known reliability and compatibility. In other words, the security feature will be OFF for these manually added sites.

#### Make an exception for security enhancements

While preventing malware increases your security, you might want to create exceptions for certain familiar websites that you trust. Any site you add as an exception will always have this security feature turned off. The following steps show how to add a site to your exception list.

1. In Microsoft Edge, select **Settings and more** > **Settings** > **Privacy, search, and services**.
2. Verify that **Enhance your security on the web** is turned on.
3. Under **Enhance your security on the web**, select **Exceptions**.
4. Select **Add a site**, type in the full URL, and then select **Add**.

> [!NOTE]
> You can use steps (1 - 3) to view sites in **Enhanced security exceptions**. You can **Edit** a site, **Remove** a site, or **Remove all** exceptions.

The next screenshot shows the dialog for security exceptions.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-enhanced-exceptions.png" alt-text="Dialog for configuring security exceptions":::

### Admin site list

Enterprise customers can create "Allow" or "Deny" lists to turn security on or off for sites they specify. Admins can configure this security feature using Group Policy settings. For more information about these policies, see the [Microsoft Edge browser policy documentation](/deployedge/microsoft-edge-policies).

## User experience with enhanced security

After a user turns on enhanced security, they'll see a banner with the words "Added security" in their URL navigation bar. This banner means that the current site is running JIT-less and protected with extra security mitigations.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-added-security-banner.png" alt-text="Banner showing that added security is turned on.":::

When you click on the banner, you will see the following dialog pop up. In addition to the other features you’re familiar with, this new security feature will be listed on the flyout as "Enhance security for this site". You can use this dialog to toggle enhanced security for the site on or off.

> [!NOTE]
> This pop-up dialogue only appears when enhanced security is turned on.

The toggle setting you pick will be remembered the next time you go to the site. Additionally, when you turn the toggle off, the site will be automatically added to your Manual site list. This results in the site being added to your Exceptions directly from the browser without opening the **Settings** page. The next screenshot shows the dialog when enhanced security is turned off.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-enhanced-security-off.png" alt-text="Dialog with enhanced security turned off.":::

In contrast, if the toggle's turned on, the site will automatically be removed from your Manual site list. The next screenshot shows the dialog when enhanced security is turned on.

:::image type="content" source="media/microsoft-edge-security-browse-safer/browse-safer-enhanced-security-on.png" alt-text="Dialog with enhanced security turned on.":::

## Send us feedback

We want to get your feedback on our next iteration of enhanced security. If something looks broken, or if you have feedback to share on these changes, we want to hear from you. You can reach out to Microsoft Support to report issues or feedback. You can also leave feedback in our [TechCommunity forum](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise).

## See also

- [Video: Secure browsing on Microsoft Edge](microsoft-edge-video-security-smartscreen.md)
- [Super Duper Secure Mode](https://microsoftedge.github.io/edgevr/posts/Super-Duper-Secure-Mode/)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)