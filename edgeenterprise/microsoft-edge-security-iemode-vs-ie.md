---
title: "Microsoft Edge is more secure than Internet Explorer"
ms.author: gennlu
author: dan-wesley
manager: kawong
ms.date: 10/18/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Learn how Internet Explorer mode in Microsoft Edge provides better security than Internet Explorer."
---

# IE mode on Microsoft Edge is more secure than Internet Explorer

As the Internet evolved over the last 20 years, so have user needs and expectations for the browsers they use. Today, the Internet is foundational to many businesses, and having a modern browser designed to securely meet business needs is paramount. Microsoft Edge is a modern browser built to securely access the modern web. This article shows how Internet Explorer (IE) mode on Microsoft Edge is more secure than Internet Explorer.

## Introduction

Microsoft's internal telemetry shows that the browser is the #1 desktop app. The centrality of the browser as an everyday productivity tool means that the browser presents a large surface area exposed to attacks from the Internet. As the Internet and its applications have become more complex, so have security threats. Over the years, the threat landscape has evolved and attracted sophisticated threat actors including, but not limited to, nation states and organized criminal groups looking to profit via phishing, ransomware, and so on.

Although it's evolved and progressed with iterations up to IE11, IE is still based on technology that's 25 years old. It's a legacy browser that's architecturally outdated and unable to meet the security challenges of the modern web.

To keep an organization's networks safe against today's sophisticated threats, IT admins try to keep users using a modern browser. This ensures that they're protected by modern security features, most or all the time as they browse. Today's common practice of using a modern browser and the IE browser is a convenient workaround, but ineffective. Users who use the IE browser for one activity can easily end up using IE for all activities, which negates the protections that a modern browser provides.

Microsoft Edge is uniquely positioned to provide up-to-date security, enabling users to take advantage modern security technology as much as possible.

## Reduce threat surface area

We understand that modernizing your all your legacy sites at once, may not be feasible. With Microsoft Edge and IE mode, you can use a secure modern browser to access your legacy sites before you modernize them. Microsoft Edge with IE mode uses a unique dual-engine system, which lets you open sites with the IE engine or with the new modern engine. The browser engine is determined by the site you visit. Because the older IE engine is less secure, you want to limit use of the legacy engine to only open sites that you trust. Trusted sites are sites you own, control, or know are free of security vulnerabilities. As a best practice you should only access untrusted sites with the modern browser engine because it's more secure.

IE mode is designed to manage access to untrusted site. IE mode uses an "allowlist" where you identify the trusted sites that can use the legacy engine. Any site that's not on the list automatically opens using the modern engine for the safest browsing experience. Untrusted content from untrusted sources is always handled by the modern engine. With IE mode, you control which sites render using the legacy engine, and when you navigate to any other site, Microsoft Edge will automatically switch back to the modern engine. As a result, an organization doesn't have to rely on user behavior and practices to self-regulate and decide which browser to use. From the users' perspective, it's a fluid experience. They don't need to think about what's the 'right' browser to use because Microsoft Edge seamlessly opens the site they're trying to access, whether it's legacy site or a modern site.

IE mode is more secure than IE because toolbars aren't supported, which reduces the surface area for an attack. Toolbars are proven vectors for malware and phishing attacks. Additionally, the IE desktop app will be disabled after retirement, which will eliminate users' time using an outdated browser. For more information, see [Internet Explorer 11 desktop app retirement FAQ](aka.ms/iemodefaq). Users will be able to access to trusted legacy apps and sites identified in an allowlist for IE mode on Microsoft Edge.

The user will be in a modern environment without needing to adjust their behavior, but also without losing access to mission-critical legacy apps and sites. Microsoft Edge is the only browser that enables users to use a single browser to access both legacy and modern sites.

The next section explains why it's important to minimize the time users spend using the legacy browser engine.

## Minimize legacy browser use

The following sections highlight the reasons why it's important to minimize legacy browser engine use.

### Architectural deficiency

Architectural deficiency in IE stems from the fact that its original architecture didn't account for the complexity of the modern web or the modern threat landscape. IE evolved from a single process architecture that resulted in inadequate sandboxing and a comparatively broad attack surface. Modern browsers like Microsoft Edge are designed around a threat model based on the current threat landscape. These browsers include security advances like site isolation and hardware-based security features. For example, Intel’s Control-flow Enforcement Technology (CET), which handles many modern security threats. These security mitigations are NOT available in IE, making it an easy target for even simple attacks.

### Ease of exploitation

IE is easier to exploit than Microsoft Edge because of its architecture and lack of support for modern security features. It's easier to find a single vulnerability in IE that could lead to a Remote Code Execution (RCE) than it is to find a similar weakness in Microsoft Edge, where several vulnerabilities must be chained together to achieve a similar outcome. Additionally, ActiveX and Browser Helper Objects have become vulnerabilities and IE’s support for them makes the browser even easier to exploit.

### Speed of security patching

Browsers are one of the most used applications on the desktop, used to routinely download, and handle untrusted content from untrusted sources. To stay ahead of security threats, modern browsers can deploy security updates quickly. Because IE is tied to the Windows operating system, the speeds of security updates are limited and causes IE to remain vulnerable for a longer time. In contrast to IE, Microsoft Edge has a built-in updater with a much faster update cadence, reducing response time to days rather than weeks or months.

### Security researcher ecosystem

Improving real world browser security relies heavily on a broad ecosystem of external security researchers who are incentivized by bounty programs to find novel vulnerabilities and exploits. Internet Explorer doesn't support a bounty program, which limits the scope of its security improvements. In comparison, Microsoft Edge has a full-fledged bounty program and an internal vulnerability research team to advance state-of-the-art browser security. Because Microsoft Edge is based on Chromium Open Source, it also benefits from Chromium’s browser security ecosystem.

### Phishing protection using SmartScreen

SmartScreen, Microsoft’s phishing protection technology, blocks more phishing <sup>1</sup> and malware<sup>2</sup> attempts than Google Chrome’s Safe Browsing, according to an independent study by [CyberRatings.org](https://www.cyberratings.org/)

> [!NOTE]
> <sup>1</sup> Web Browsers vs. Phishing, Comparative Test Report (July 2021), CyberRatings.org<br>
> <sup>2</sup>Web Browsers vs. Malware, Comparative Test Report (July 2021), CyberRatings.org

Microsoft Edge provides full native support for SmartScreen, but IE is only partially supported because of its outdated architecture.

In addition to providing security advances that map to modern security practices, Microsoft Edge is more secure than Chrome for businesses on Windows 10. Microsoft Edge is also designed to take advantage of the security features, functionality, and tools available in the Microsoft 365 suite and Windows 10. This product ecosystem reduces security and privacy complexity for the IT team. For example, investments and decisions made for identity in Microsoft 365 can be easily applied to Microsoft Edge.

IE mode on Microsoft Edge is a unique solution that ensures users can access mission-critical IE legacy sites, while at the same time staying protected from modern threats.

## See also

- [About IE mode](/edge-ie-mode.md)
- [Additional Enterprise Mode information](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Security for your business](/ms-edge-security-for-business.md)
- [Microsoft Edge Enterprise landing page](aka.ms/microsoft-edge)