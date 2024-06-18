---
title: "Changes to Microsoft Edge browser TLS server certificate verification"
ms.author: erikan
author: dan-wesley
manager: arvindm
ms.date: 08/21/2023
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "An overview of the changes to Microsoft Edge browser TLS server certificate verification"
---

# Changes to Microsoft Edge browser TLS server certificate verification

> [!NOTE]
> Microsoft Edge for Business is now available in Edge stable version 116! [Learn more](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/microsoft-edge-for-business-faq/ba-p/3891837) about the new, dedicated work experience with native enterprise grade security, productivity, manageability, and AI built in.

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

## Known locally-trusted certificate behavior differences on Windows
### Stricter RFC 5280 compliance
The new, built-in certificate verifier is more stringent in enforcing [RFC 5280](https://datatracker.ietf.org/doc/rfc5280/) requirements than the old, platform-based verifier.

Examples of stricter RFC 5280 compliance include:
1. Algorithm parameters for ECDSA algorithms must be absent. The old verifier would ignore the parameters while the new one rejects the certificate. For more information, see [Chromium issue 1453441](https://crbug.com/1453441) for more details.
2. Name constraints specifying an IP address must contain eight octets for IPv4 addresses and 32 octets for IPv6 addresses. If your certificate specifies an empty IP address, you should reissue the certificate and omit the IP address name constraint entirely.
3. Name constraints with an empty "excluded" list is invalid. The Windows certificate viewer shows this list as `Excluded=None` within the `Name Constraints` details. For more information, see [Chromium issue 1457348](https://crbug.com/1457348) for more details. Instead of specifying an empty list, omit it entirely.

### Application Policies extension

Prior to Microsoft Edge 115, the new verifier doesn't support the Windows-only "application policies" extension field that's described in the [CertGetEnhancedKeyUsage function documentation](/windows/win32/api/wincrypt/nf-wincrypt-certgetenhancedkeyusage#remarks). In Microsoft Edge 115, an update was made to ignore the extension. See [Chromium issue 1439638](https://crbug.com/1439638) for more details.

This extension uses the object identifier (OID) `1.3.6.1.4.1.311.21.10`. If the certificate includes this extension and marks it as critical, the connection fails with `ERR_CERT_INVALID`.

You can use one of the following ways to check if this scenario applies to your certificate:

1. A network log captured via `about:net-export` includes the string `ERROR: Unconsumed critical extension` in the `CERT_VERIFIER_TASK` with an OID value of `2B060104018237150A`.
2. Open the certificate with the Windows certificate viewer. In the "Show" filter, select "Critical Extensions Only". Check to see if an "Application Policies" field in present.
3. Run `certutil.exe` with the `-dump` switch and review the output to check for a critical Application Policies extension field.

If your certificate currently uses this extension, make sure that it now works in Microsoft Edge 115. Alternatively, reissue the certificate and instead rely solely on the enhanced key usage field (OID `2.5.29.37`) to specify allowed usages.

## Known revocation checking behavior differences on Windows
In addition to the more stringent RFC 5280 requirements, the new verifier _doesn't_ support LDAP-based certificate revocation list (CRL) URIs.

If your enterprise enables the **[RequireOnlineRevocationChecksForLocalAnchors](/deployedge/microsoft-edge-policies#requireonlinerevocationchecksforlocalanchors)** policy and the CRLs aren't valid per RFC 5280, your environment may start to see `ERR_CERT_NO_REVOCATION_MECHANISM` and/or `ERR_CERT_UNABLE_TO_CHECK_REVOCATION` errors.

Before Microsoft Edge 114, the new Chromium-based verifier enforces "Baseline Requirement" max ages for CRLs. For leaf revocations, the current maximum age is 7 days and for intermediate revocations, the current maximum age is 366 days. The check is performed by checking that the current time minus the "This Update" ("Effective Date") doesn't exceed those maximums. In Microsoft Edge 114, these requirements are no longer enforced for non-publicly trusted certificates. For more information, see [Chromium issue 971714](https://crbug.com/971714).

For Edge version 120 and below, the built-in verifier downloads revocation information via the browser's networking stack, such that HTTP Strict Transport Security (HSTS) upgrades apply. This upgrade can create an incompatibility with the requirement that the CRL information is hosted via HTTP (not HTTPS) if the host has an HSTS pin configured. This scenario has seen been addressed and fixed. More information can be found via [Chromium issue 1432246](https://crbug.com/1432246).

If you encounter `ERR_CERT_NO_REVOCATION_MECHANISM`, you should confirm that the CRL at the URI specified by the certificate returns a **DER encoded** (not PEM encoded) response.

If you encounter `ERR_CERT_UNABLE_TO_CHECK_REVOCATION` errors, you should confirm that the certificate issuer is also the CRL issuer, the certificate's `cRLIssuer` field isn't set, and that the CRL was issued recently enough. If you are on a version of Edge 120 or below, ensure that the URI hosting the CRL both uses the HTTP protocol and isn't on a host configured to use HSTS.

## See also

- [Microsoft Edge security for your business](ms-edge-security-for-business.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
