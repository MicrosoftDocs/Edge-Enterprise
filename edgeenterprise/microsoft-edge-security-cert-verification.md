---
title: "Changes to Microsoft Edge browser TLS server certificate verification"
ms.author: erikan
author: dan-wesley
manager: arvindm
ms.date: 04/18/2023
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "An overview of the changes to Microsoft Edge browser TLS server certificate verification"
---

# Changes to Microsoft Edge browser TLS server certificate verification

When establishing connections to an HTTPS server, Microsoft Edge verifies that the server has presented a certificate issued by an entity trusted by the browser. This trust relationship is established via a **certificate trust list** and the component responsible for performing the checks is called the **certificate verifier**.

In past versions of Microsoft Edge, both the default certificate trust list and the certificate verifier logic were provided by underlying operating system (OS) platform.

For managed devices, starting in Microsoft Edge 112 on Windows and macOS, both the default certificate trust list and the certificate verifier are provided by and shipped with the browser. This decouples the list and verifier from the host operating system's root store for the default verification behavior. See the [rollout timeline and testing guidance](#rollout-timeline-and-testing-guidance) for more detail about the timing of the change.

Even after the change, in addition to trusting the built-in roots that ship with Microsoft Edge, the browser queries the underlying platform for—and trusts—locally installed roots that users and/or enterprises installed. As a result, scenarios where a user or enterprise installed additional trusted roots to the host operating system's root store should continue to work.

This change means that certificate verification logic works consistently in Microsoft Edge on Windows and macOS. In a future to-be-determined release, the rollout will also apply to Linux and Android. Due to Apple App Store policies, the Apple-provided root store and certificate verifier will continue to be used on iOS and iPadOS.

## Default certificate trust list source

The root store that ships with Microsoft Edge on Windows and macOS comes from the Certificate Trust List (CTL) defined by the [Microsoft Trusted Root Certificate Program](/security/trusted-root/program-requirements). This is the same root certificate program that defines the list that ships with Microsoft Windows and, as a result, customers should expect to see no user-visible changes.

On macOS, if a certificate was issued by a root certificate trusted by the platform but not by Microsoft's Trusted Root Certificate Program, the certificate will no longer be trusted. This lack of trust isn't expected to be a common situation, since most servers already ensure the TLS certificates that they use are trusted by Microsoft Windows.

Updates will be released on the cadence documented in the [release notes](/security/trusted-root/release-notes) for the Microsoft Trusted Root Program.

## Rollout timeline and testing guidance

Starting in Microsoft Edge 109, an enterprise policy (**[MicrosoftRootStoreEnabled](/deployedge/microsoft-edge-policies#microsoftrootstoreenabled)**) and a flag in *edge://flags* (“Microsoft Root Store”) is available to control when the built-in root store and certificate verifier are used.

Devices that aren't managed by the enterprise started receiving the feature via a Controlled Feature Rollout (CFR) in Microsoft Edge 109 and reached 100% of non-managed devices in Edge 111. For more information, see [Microsoft Edge configurations and experimentation](/deployedge/edge-configuration-and-experiments), which explains how CFRs in Microsoft Edge work. For enterprise-managed devices, the existing platform-provided implementation was used through Microsoft Edge 111.

Starting with Microsoft Edge 112, the default changed for all Windows and macOS devices, including enterprise-managed ones, to use the verifier implementation and CTL shipped with the browser. The **MicrosoftRootStoreEnabled** policy will continue to be available in this release to allow enterprises to revert to the previous behavior if unexpected issues are found and to report the issues to Microsoft.

Microsoft recommends that enterprises that have break-and-inspect proxies or other scenarios involving TLS server certificates issued by roots not in the Microsoft CTL to proactively identify and report any compatibility issues to Microsoft.

In Microsoft Edge 113, we plan to remove support for the **MicrosoftRootStoreEnabled** policy.

## Known locally-trusted certificate behavior differences on Windows
The new verifier doesn't support the Windows-only "application policies" extension field which is described in the [CertGetEnhancedKeyUsage function documentation](/windows/win32/api/wincrypt/nf-wincrypt-certgetenhancedkeyusage#remarks). This extension uses the object identifier (OID) `1.3.6.1.4.1.311.21.10`. If the certificate includes this extension and marks it as critical, the connection will fail with `ERR_CERT_INVALID`.

There are a few ways to check if this applies to your certificate:
1. A network log captured via `about:net-export` will include the string `ERROR: Unconsumed critical extension` in the `CERT_VERIFIER_TASK` with an OID value of `2B060104018237150A`.
2. Open the certificate with the Windows certificate viewer, select "Critical Extensions Only" in the "Show" filter, and check if a "Application Policies" field in present.
3. Run `certutil.exe` with the `-dump` switch and review the output to check for a critical Application Policies extension field.

If your certificate currently uses this extension, please reissue the certificate and remove the use of the application policies field. You should instead rely solely on the enhanced key usage field (OID `2.5.29.37`) instead to specify allowed usages.

## Known revocation checking behavior differences on Windows
The new, built-in certificate verifier is more stringent in enforcing [RFC 5280](https://datatracker.ietf.org/doc/rfc5280/) requirements for certificate revocation lists (CRLs) than the old, platform-based verifier. Additionally, the new verifier _does not_ support LDAP-based CRL URIs.

If your enterprise enables the **[RequireOnlineRevocationChecksForLocalAnchors](/deployedge/microsoft-edge-policies#requireonlinerevocationchecksforlocalanchors)** policy and the CRLs are not valid per RFC 5280, your environment may start to see `ERR_CERT_NO_REVOCATION_MECHANISM` and/or `ERR_CERT_UNABLE_TO_CHECK_REVOCATION` errors.

The new Chromium-based verifier currently enforces "Baseline Requirement" max ages to CRLs. For leaf revocations, the current maximum age is 7 days and for intermediate revocations, the current maximum age is 366 days. The check is performed by checking that the current time minus the "This Update" ("Effective Date") does not exceed those maximums. If this creates problems in your environment, you are encouraged to share more information about the impact via [Chromium issue 971714](https://crbug.com/971714).

Since the new verifier downloads revocation information via the browser's networking stack, HTTP Strict Transport Security (HSTS) upgrades also apply. This can create an incompatibility with the requirement that the CRL information be hosted via HTTP (not HTTPS) if the host has an HSTS pin configured. If your environment is negatively impacted by this, you are encouraged  you are encouraged to share more information about the impact via [Chromium issue 1432246](https://crbug.com/1432246).

If you encounter `ERR_CERT_NO_REVOCATION_MECHANISM`, you should confirm that the CRL at the URI specified by the certificate returns a **DER encoded** (not PEM encoded) response.

If you encounter `ERR_CERT_UNABLE_TO_CHECK_REVOCATION` errors, you should confirm that the certificate issuer is also the CRL issuer, the certificate's `cRLIssuer` field is not set, the URI hosting the CRL both uses the HTTP protocol and is not on a host configured to use HSTS, and that the CRL was issued recently enough.

## See also

- [Microsoft Edge security for your business](ms-edge-security-for-business.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
