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
description: "Learn how enhanced security mode supports safer browsing within Microsoft Edge."
---
# Browse safer within Microsoft Edge

This article describes how Microsoft Edge supports Enhance Secure Mode to provide safer browsing.

## Overview

Microsoft Edge is designed to give you more control over your browser’s security when browsing the web and visiting unfamiliar sites. With enhanced security, users can browse the unfamiliar parts of the web more securely, protected by additional security mitigations and protections.

The web platform has a lot of power designed to give site visitors a rich experience through the use of Javascript, web notifications, permissions, and so on. That power and accessibility is reflected in a larger exposure area for exploits and security vulnerabilities that untrustworthy sites can use for malicious activity. Enhance security mode is changing how we think about protecting users from the unknown and unfamiliar.  

Unprecedented in-the-wild exploits (also referred called 0-days) are more frequent. This feature aims to raise the security bar against V8-related exploits and neutralize them. Effective neutralization is achieved by running JIT-less engines and enabling additional guards for the browser. From an historical perspective, in 2021, 41% of in-the-wild exploits were mitigated with this security feature.

## About Enhance Secure Mode

The core of this feature starts by disabling the just-in-time (JIT) compiler in V8, to protect your browser with a series of protective guards. These protections include: Control-flow Enforcement Technology (CET), Arbitrary Code Guard (ACG), and Control Flow Guard (CFG) for the rendering process. Additionally, running JIT-less V8 will block writing to executable memory, which reduces the attack surface of the application for exploits.

You can learn more about the experimentation results from the Microsoft Edge Security team’s blog post: [Super Duper Secure Mode](https://microsoftedge.github.io/edgevr/posts/Super-Duper-Secure-Mode) and [tbd].

> [!NOTE]
> Web Assembly isn’t currently supported in this mode. We are actively working on Web Assembly support over the next few months as we continue testing, experimenting, and further developing the feature.

## What's new in Microsoft Edge security settings

ags
## See also

- [Video: Secure browsing on Microsoft Edge](microsoft-edge-video-security-smartscreen.md)
- [Super Duper Secure Mode](https://microsoftedge.github.io/edgevr/posts/Super-Duper-Secure-Mode/)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)