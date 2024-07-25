---
title: "Changes to Microsoft Edge browser TLS server certificate verification"
ms.author: erikan
author: dan-wesley
manager: arvindm
ms.date: 07/18/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "An overview of the changes to Microsoft Edge browser TLS server certificate verification"
---

# Changes to Microsoft Edge browser TLS server certificate verification

When Microsoft Edge establishes connections to an HTTPS server, Edge verifies that the server has presented a certificate issued by an entity trusted by the browser. This trust relationship is established via a **certificate trust list** and the component responsible for performing the checks is called the **certificate verifier**.

In past versions of Microsoft Edge, both the default certificate trust list and the certificate verifier logic were provided by underlying operating system (OS) platform.

For managed devices, starting in Microsoft Edge 112 on Windows and macOS, both the default certificate trust list and the certificate verifier are provided by and shipped with the browser. This approach decouples the list and verifier from the host operating system's root store for the default verification behavior. See the [rollout timeline and testing guidance](#rollout-timeline-and-testing-guidance) for more detail about the timing of the change.

Even after the change, in addition to trusting the built-in roots that ship with Microsoft Edge, the browser queries the underlying platform for—and trusts—locally installed roots that users and/or enterprises installed. As a result, scenarios where a user or enterprise installed more roots to the host operating system's root store should continue to work.

This change means that certificate verification logic works consistently in Microsoft Edge on Windows and macOS. In a future to-be-determined release, the rollout will also apply to Linux and Android. Due to Apple App Store policies, the Apple-provided root store and certificate verifier continue to be used on iOS and iPadOS.

## Default certificate trust list source

The root store that ships with Microsoft Edge on Windows and macOS comes from the Certificate Trust List (CTL) defined by the [Microsoft Trusted Root Certificate Program](/security/trusted-root/program-requirements). This root certificate program defines the list that ships with Microsoft Windows. As a result, customers should expect to see no user-visible changes.

On macOS, if a certificate issued by a root certificate that's trusted by the platform but not by Microsoft's Trusted Root Certificate Program, the certificate is no longer trusted. This lack of trust isn't expected to be a common situation, since most servers already ensure the TLS certificates that they use are trusted by Microsoft Windows.

Updates are released on the cadence documented in the [release notes](/security/trusted-root/release-notes) for the Microsoft Trusted Root Program.

## Rollout timeline and testing guidance

Starting in Microsoft Edge 109, an enterprise policy (**[MicrosoftRootStoreEnabled](/deployedge/microsoft-edge-policies#microsoftrootstoreenabled)**) and a flag in *edge://flags* ("Microsoft Root Store") is available to control when the built-in root store and certificate verifier are used.

Devices that aren't managed by the enterprise started receiving the feature via a Controlled Feature Rollout (CFR) in Microsoft Edge 109 and reached 100% of non-managed devices in Edge 111. For more information, see [Microsoft Edge configurations and experimentation](/deployedge/edge-configuration-and-experiments), which explains how CFRs in Microsoft Edge work. For enterprise-managed devices, the existing platform-provided implementation was used through Microsoft Edge 111.

Starting with Microsoft Edge 112, the default changed for all Windows and macOS devices, including enterprise-managed ones, to use the verifier implementation and CTL shipped with the browser. The **MicrosoftRootStoreEnabled** policy continues to be available in this release to allow enterprises to revert to the previous behavior if unexpected issues are found and to report the issues to Microsoft.

Microsoft recommends that enterprises that have break-and-inspect proxies or other scenarios involving TLS server certificates issued by roots not in the Microsoft CTL to proactively identify and report any compatibility issues to Microsoft.

In Microsoft Edge 115, support for the **MicrosoftRootStoreEnabled** policy is removed.

## Known locally trusted certificate behavior differences on Windows
### Stricter RFC 5280 compliance
The new, built-in certificate verifier is more stringent in enforcing [RFC 5280](https://datatracker.ietf.org/doc/rfc5280/) requirements than the old, platform-based verifier.

Examples of stricter RFC 5280 compliance include:
1. Algorithm parameters for ECDSA algorithms must be absent. The old verifier would ignore the parameters while the new one rejects the certificate. For more information, see [Chromium issue 1453441](https://crbug.com/1453441) for more details.
2. Name constraints specifying an IP address must contain eight octets for IPv4 addresses and 32 octets for IPv6 addresses. If your certificate specifies an empty IP address, you should reissue the certificate and omit the IP address name constraint entirely.
3. Name constraints with an empty "excluded" list is invalid. The Windows certificate viewer shows this list as `Excluded=None` within the `Name Constraints` details. For more information, see [Chromium issue 1457348](https://crbug.com/1457348) for more details. Instead of specifying an empty list, omit it entirely.

## Known revocation checking behavior differences on Windows
In addition to the more stringent RFC 5280 requirements, the new verifier _doesn't_ support LDAP-based certificate revocation list (CRL) URIs.

If your enterprise enables the **[RequireOnlineRevocationChecksForLocalAnchors](/deployedge/microsoft-edge-policies#requireonlinerevocationchecksforlocalanchors)** policy and the CRLs aren't valid per RFC 5280, your environment may start to see `ERR_CERT_NO_REVOCATION_MECHANISM` and/or `ERR_CERT_UNABLE_TO_CHECK_REVOCATION` errors.

If you encounter `ERR_CERT_NO_REVOCATION_MECHANISM`, you should confirm that the CRL at the URI specified by the certificate returns a **DER encoded** (not PEM encoded) response.

## See also

- [Microsoft Edge security for your business](ms-edge-security-for-business.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
