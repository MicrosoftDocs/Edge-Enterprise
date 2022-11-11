---
title: "Changes to Microsoft Edge browser TLS server certificate verification"
ms.author: erikan
author: dan-wesley
manager: arvindm
ms.date: 11/11/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "An overview of the changes to Microsoft Edge browser TLS server certificate verification"
---

# Changes to Microsoft Edge browser TLS server certificate verification

When establishing connections to an HTTPS server, Microsoft Edge verifies that the server has presented a certificate issued by an entity trusted by the browser. This trust relationship is established via a **certificate trust list** and the component responsible for performing the checks is called the **certificate verifier**.

In current versions of Microsoft Edge, both the certificate trust list and the certificate verifier logic are provided by underlying operating system (OS) platform.

In future versions of Microsoft Edge, both the certificate trust list and the certificate verifier will be provided by and shipped with the browser. This will decouple the list and verifier from the host operating system’s root store.

This change means that certificate verification logic will work consistently in Microsoft Edge on Windows, macOS, Linux, and Android. Due to Apple App Store policies, the Apple-provided root store and certificate verifier will continue to be used on iOS and iPadOS.

## Certificate trust list source

The root store that ships with Microsoft Edge will come from the Certificate Trust List (CTL) defined by the [Microsoft Trusted Root Certificate Program](/security/trusted-root/program-requirements). This is the same root certificate program that defines the list that ships with Microsoft Windows and, as a result, customers should expect to see no user-visible changes.

On other platforms, if a certificate was issued by a root certificate trusted by the platform but not by Microsoft’s Trusted Root Certificate Program, the certificate will no longer be trusted. This lack of trust isn’t expected to be a common situation, since most servers already ensure the TLS certificates that they use are trusted by Microsoft Windows.

Updates will be released on the cadence documented in the [release notes](/security/trusted-root/release-notes) for the Microsoft Trusted Root Program.

In addition to trusting the built-in roots that ship with Microsoft Edge, the browser will also query the underlying platform for—and trust—locally installed roots that users and/or enterprises installed.

## Rollout timeline and testing guidance

Starting in Microsoft Edge 109, an enterprise policy (**MicrosoftRootStoreEnabled**) and a flag in *edge://flags* (“Microsoft Root Store”) is available to control when the built-in root store and certificate verifier are used.

Devices that aren’t managed by the enterprise will start receiving the feature via a Controlled Feature Rollout (CFR). For more information, see [Microsoft Edge configurations and experimentation](/deployedge/edge-configuration-and-experiments), which explains how CFRs in Microsoft Edge work. For enterprise-managed devices, the existing platform-provided implementation will continue to be used in Microsoft Edge 109.

Starting with Microsoft Edge 110, the default will change for all devices, including enterprise-managed ones, to use the verifier implementation and CTL shipped with the browser. The **MicrosoftRootStoreEnabled** policy will continue to be available in this release to allow enterprises to revert to the previous behavior if unexpected issues are found and to report the issues to Microsoft.

Microsoft recommends that enterprises that have break-and-inspect proxies or other scenarios involving TLS server certificates issued by roots not in the Microsoft CTL to proactively test with the policy enabled in Microsoft Edge 109 and report any compatibility issues to Microsoft.

In Microsoft Edge 111, we plan to remove support for the **MicrosoftRootStoreEnabled** policy.

## See also

- [Security for your business](./ms-edge-security-for-business)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
