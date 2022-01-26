---
title: "Browse safer within Microsoft Edge"
ms.author: pchiquini
author: dan-wesley
manager: robfranco
ms.date: 01/25/2022
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

The web platform has a lot of power designed to give site visitors a small and intuitive browsing experience through the use of Javascript, web notifications, permissions, and so on. That power and accessibility is reflected in a larger exposure area for exploits and security vulnerabilities that untrustworthy sites can use for malicious activity. By enhancing your security on the browser, we're shifting conventional and well-established assumptions on how we think about protecting users from the unknown and unfamiliar.  

Unprecedented in-the-wild exploits (also referred called 0-days) are more frequent. This feature aims to raise the security bar against V8-related exploits and neutralize them. Effective neutralization is achieved by running JIT-less engines and enabling additional guards for the browser. From an historical perspective, in 2021, 41% of in-the-wild exploits were mitigated with this security feature alone.

## About this security feature

The core of this feature starts by disabling the just-in-time (JIT) compiler in V8, to protect your browser with a series of protective guards. These protections include: Control-flow Enforcement Technology (CET), Arbitrary Code Guard (ACG), and Control Flow Guard (CFG) for the rendering process. Additionally, running JIT-less V8 will block writing to executable memory, which reduces the attack surface of the application for exploits.

You can learn more about the experimentation results from the Microsoft Edge Security team’s blog post [published back in August 2021](https://microsoftedge.github.io/edgevr/posts/Super-Duper-Secure-Mode) and [its continuation blog post in February 2022]().

> [!NOTE]
> Web Assembly isn’t currently supported in this mode. We're working on Web Assembly support over the next few months as we continue testing, experimenting, and further developing the feature.

## What's new in Microsoft Edge security settings

With **Enhance your security on the web**, Microsoft Edge puts your browser in a mode where the security of your browser takes priority, giving you an extra layer of protection when browsing the web. You’ll still enjoy browsing when visiting top sites.

Use the following steps to set your security level.

1. In Microsoft Edge, go to **Settings and more** > **Settings** > **Privacy, search, and services.** 
2. Under **Security**, verify that **Enhance your security on the web** is enabled.
3. Select the option that's best for your browsing. 

The following toggle settings are available:

- Toggle Off (Default): Feature is turned off
- Toggle On – Balanced (Recommended): In this mode, your frequently browsed sites will be left out. The feature will only turn on when you browse sites that you don’t engage with often or are unknown to you.
- Toggle On – Strict: This will turn on the feature for all the sites you visit. 
Select the option that’s best for your browsing.

## Site list Exceptions

Enhancing your security doesn’t have a single centralized list of sites. This strategy is designed to reduce the risk of attack where an attacker can exploit an XSS vulnerability in one a site and use that vulnerability to attack other sites in the list. In contrast, each user will have their own unique site list, manually or intelligently populated to provide a tailored experience. A list that’s unique to each user means that an attacker has to predict which sites the user trusts, which makes exploitation more difficult.

### Learn about Exception site lists

The next drawing shows the three categories of sites in an exception site list.


#### Intelligent Site List

Many users want a high level of control, and we believe that most of them prefer to have many aspects of security feature automatically managed while still offering manual site list management. To address this, enhancing your security on the web uses an algorithm that runs locally in the browser. It’s also worth noting that site engagement scores are computed on your device and never leave it. This means that they are not synced across your devices or sent to Microsoft at any time.

> [!TIP]
> You can view your own site engagement scores by going to *edge://site-engagement*.

Furthermore, this algorithm learns from your behavior and manages the site list for you. That is, sites that users use most often will be treated the same way as users treat most of the web today. These sites can use JIT code and opt out the extra layer of security because of their familiarity and engagement frequency. In contrast, when a user navigates unfamiliar sites (sites not visited often) the site will enter in this new secure mode. We’re not claiming they’re bad sites; we’re saying they’re unfamiliar to you and Microsoft Edge. This being the case, we want to be more deliberate about what surface area is exposed to these sites.

#### Manual Site List

Users can manually add their own exceptions for their familiar websites. Adding a site to your unshared site list will remove the extra layer of protection to keep a site’s known reliability and compatibility. In other words, the security feature will be OFF for these manually added sites.

#### Admin Site List

Enterprise customers can create "Allow" or "Deny" lists to turn on or off security on sites they specify. Admins can configure this security feature using Group Policy settings. For more information about these policies, see [Enhance the security state in Microsoft Edge](/deployedge/microsoft-edge-policies#enhancesecuritymode). You can find the complete list of policies in the [Microsoft Edge browser policy documentation](/deployedge/microsoft-edge-policies).




## See also

- [Video: Secure browsing on Microsoft Edge](microsoft-edge-video-security-smartscreen.md)
- [Super Duper Secure Mode](https://microsoftedge.github.io/edgevr/posts/Super-Duper-Secure-Mode/)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)