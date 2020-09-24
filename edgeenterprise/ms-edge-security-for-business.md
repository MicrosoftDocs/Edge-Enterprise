---
title: "Microsoft Edge security for your business"
ms.author: seanlynd
author: seanongit
manager: chuckf
ms.date: 09/22/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Microsoft Edge security for your business"
---

# Microsoft Edge security for your business

Microsoft Edge is built on top of the Chromium open source project—the same project that is core of Google Chrome—meaning it shares the same well-engineered and well-tested security architecture and design at its foundation. The Microsoft Edge security story doesn't stop there. In fact, **Microsoft Edge is more secure than Google Chrome for your business on Windows 10**. It has powerful, built-in defenses against phishing and malware and natively supports hardware isolation on Windows 10—there's no additional software required to achieve this secure baseline. Furthermore, when paired with native support for Microsoft 365 security and compliance services, Microsoft Edge brings additional, powerful security capabilities and features that help protect against data loss for even more benefits.

Let's get into the details, starting with **external threats** and then looking at **internal risks and information protection**.

## External threat protection

### Highest-rated protection against phishing and malware

Built into Microsoft Edge, SmartScreen blocks more phishing and malware attempts than Google Chrome's Safe Browsing, according to an [independent study from NSS Labs](https://www.nsslabs.com/tested-technologies/web-browser-security-wbs/). SmartScreen provides real-time reputation checks of sites and downloads as users work online, and is part of the [Microsoft Intelligent Security Graph](https://www.microsoft.com/microsoft-365/windows/intelligent-security), which draws signals and insights generated from Microsoft's large network of global assets, researchers, and partners. By running checks against dynamic, cloud-based lists of dangerous sites and downloads, Microsoft Edge helps to detect and block even ephemeral threats that quickly disappear.  

[Microsoft Edge with SmartScreen](https://docs.microsoft.com//DeployEdge/microsoft-edge-security-smartscreen) blocked 95.5% of phishing attempts and 98.5% of malware attempts [during the NSS Labs test](https://www.nsslabs.com/tested-technologies/web-browser-security-wbs/) compared to Chrome's Safe Browsing's rates of 86.9% and 86.0%, respectively.

### The only browser on Windows 10 that natively supports hardware isolation

Microsoft Edge is the only browser on Windows 10 that natively supports hardware isolation capabilities. As part of Windows 10 Pro or Enterprise, Microsoft Defender Application Guard (Application Guard) runs untrusted sites in a kernel isolated from the local device and internal networks. The untrusted sites are run in a "container" so when an attack emerges, it is sandboxed from the rest of the corporate network. For more information, see [Microsoft Edge support for Application Guard](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-defender-application-guard).

For Chrome, an extension is available to leverage Windows 10 hardware isolation—the MDAG extension. This extension then launches Microsoft Edge in order to leverage Application Guard's kernel level isolation. Additionally, to achieve similar kernel level isolation for a Chrome-only solution, one needs 3rd party isolation software.

> [!NOTE]
> Application Guard is available on Windows 10, 1809 and above. Application Guard isn't available on Windows 10 Home editions.

## Internal risks and information protection

### Native support for Microsoft 365 security without additional software

Aside from protecting against external threats, IT admins also must protect against internal risk. Protecting sensitive corporate data—robustly and at scale—is a top priority for IT administrators, particularly as workforces have decentralized. Microsoft Edge is the only browser with native support for Azure AD Conditional Access, Windows Information Protection, and the new Microsoft Endpoint Data Loss Prevention (DLP) without additional software required.

**Microsoft Edge is the only browser to natively support Conditional Access**. [Microsoft Edge's support for conditional access](https://docs.microsoft.com/DeployEdge/security-overview#conditional-access) makes it easy for organizations to utilize identity signals as part of their access control decisions. [Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) is the tool used by Azure Active Directory to bring signals together, to make decisions, and enforce organizational policies. Conditional Access is at the heart of the new identity driven control plane. To get Conditional Access support on Chrome, an additional plug-in is required.

> [!NOTE]
> Microsoft 365 E3 or higher subscription required for Azure AD Conditional Access.

**Microsoft Edge is the only browser to natively support Windows Information Protection (WIP)**, which provides protection to corporate data to help prevent accidental leaks by users on Windows 10 devices. [Microsoft Edge support for WIP](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-information-protection) can be configured to only allow IT mandated apps to access corporate data. It also provides leak controls—such as clipboard protection, encrypting files on download, and preventing file uploads to unauthorized network shares or cloud location—with a seamless user experience. WIP works on a perimeter-based configuration, where IT admins define the corporate boundary and all data inside that boundary is considered corporate. Chrome is not enlightened for WIP with leak controls.

> [!NOTE]
> Windows Information Protection (WIP) configuration requires licensing Microsoft Intune or Microsoft Endpoint Configuration Manager, or using a 3rd party mobile device management (MDM) solution, which may have additional licensing requirements.

**Microsoft Endpoint DLP will be natively supported only on Microsoft Edge upon its general availability in October**. Microsoft Endpoint Data Loss Prevention (DLP) integrates with Microsoft Security Center and extends information protection to Microsoft Edge to help alert users to non-compliant activity and prevent data loss as users work online. It discovers and labels sensitive data inside the enterprise that matches admin-defined criteria, such as files containing credit card numbers or governmental IDs (for example, social security numbers), financial information, etc. Microsoft Information Protection policies can be deployed to Microsoft Endpoint DLP without addition reconfiguration, including sensitive content identifiers and policies that IT admins have already customized. This is seamless deployment of information protection for IT admins.

> [!NOTE]
> Microsoft 365 E5 or Microsoft 365 E5 Compliance subscription required for Microsoft Endpoint Data Loss Prevention.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
