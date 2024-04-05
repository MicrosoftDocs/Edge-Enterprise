---
title: "Microsoft Edge for Business Recommended Configuration Settings"
ms.author: mollymcnutt
author: dan-wesley
manager: archandr
ms.date: 04/04/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Configure Edge as a Secure Enterprise Browser in your organization."
---

# Microsoft Edge for Business Recommended Configuration Settings

This article provides recommended configurations for Edge for Business across managed and unmanaged devices for E3 and E5 licenses.

> [!NOTE]
> Edge for Business is the browser that's available through a work profile and surfaces enhanced security and productivity features. Edge for business will be referenced as "Edge" in this article.

## What is a Secure Enterprise Browser?

A secure enterprise browser is a web browser that is secure by default and designed with security features tailored for use within corporate or organizational environments. These browsers prioritize security, privacy, and manageability to mitigate browser-based cyber risks.

Often, secure enterprise browsers (SEBs) also include enhanced productivity features alongside their robust security measures. These productivity features are designed to improve user efficiency and facilitate collaboration within the organization while maintaining a secure browsing ecosystem.  

## The importance of a Secure Enterprise Browser

The browser has become more than just a tool; it's now a destination where 56% of the workday is spent. Within this digital realm, sensitive organizational and user data are often surfaced, whether it's through accessing company documents, communicating between users, or interacting with web-based applications.

The increased reliance on browsers heightens browser-based cyber risks. As a result, ensuring the security of browser environments has become paramount for organizations, with secure enterprise browsers emerging as essential tools to safeguard against the ever-evolving landscape of cyber threats. In today's modern work environment where remote work and the use of personal devices are common, the role of SEBs in mitigating such security breaches becomes even more crucial. Remote work introduces more security challenges, such as unsecured home networks, BYOD policies, and reliance on public or personal Wi-Fi, which can increase the risk of cyberattacks and data breaches. SEBs help address these challenges by providing a secure browsing environment with features such as strong encryption, advanced threat detection, and policy enforcement.

## The Microsoft Edge advantage

Edge continues to invest in the development of capabilities that transform the browser into a proactive agent, actively detecting and providing anticipatory protections against security concerns that organizations encounter.

Edge for Business capabilities are built on the following pillars:

1. Protect users and devices  
2. Protect sensitive organization data
3. Provide secure network access on any device
4. Enhance employee productivity with safe AI
5. Provide unified manageability

## Protecting users and devices

Microsoft Edge has a strong core security foundation inherited from Chromium. This platform is rapidly updated with the latest upstream changes that include security patches. In addition to the strong security foundation, Edge has the following unique capabilities powered by Microsoft Defender SmartScreen and Microsoft Entra ID for protection on the device and on the network.

1. [Microsoft Defender SmartScreen](/windows/security/operating-system-security/virus-and-threat-protection/microsoft-defender-smartscreen/) gives industry leading protection against phishing, drive-by exploits, tech support scams, malware, malware advertising, and malicious downloads.  
2. [Typosquatting protection](/deployedge/microsoft-edge-policies#preventtyposquattingpromptoverride) is embedded in the browser to warn users if they mistype a commonly used website name and land on a malicious site instead.  
3. Increased zero-day protection surfaced through [Enhanced Security Mode](https://www.microsoft.com/en-us/edge/features/enhanced-security-mode?form=MA13FJ) safeguards against memory-related vulnerabilities by disabling just-in-time (JIT) JavaScript compilation and enabling more operating system protections for the browser.
4. Improved threat detections use new signals for the Security Operations Center (SOC), which provide valuable app level signals to Microsoft Defender.  

## Protecting sensitive data in the organization

Increased browser usage in the enterprise makes the browser the #1 surface for enterprise data egress. Sensitive organizational data is protected in Edge through various data leak prevention and auditing systems.  

1. Edge provides native support for [Microsoft Purview DLP](https://www.microsoft.com/en-us/security/business/information-protection/microsoft-purview-data-loss-prevention) for a seamless end user experience that protects the distribution of sensitive data in the browser.  
2. Edge can be integrated with [Microsoft Insider Risk Management](/purview/insider-risk-management) for policy-based risk monitoring, alerting, and auditing, which supports incident forensics and mitigation.
3. Edge supports [Microsoft Entra TRv2](/entra/external-id/tenant-restrictions-v2) which prevents unauthorized tenant access by providing advanced data exfiltration protection and supports multitenant scenarios.

## Provide secure network access on any device  

Edge provides a broad spectrum of capabilities to enable secure network access to any web resource from BYOD devices. These capabilities include secure network access to both internet (Microsoft 365, SaaS apps, and the rest of internet) and private applications (on-premises and cloud) with threat protection and data exfiltration protections enforced on the network to suit different customer needs.

1. [Microsoft Entra's Conditional Access](/entra/identity/conditional-access/overview) systems work seamlessly in Edge to provide productive protection of company assets and prevent unauthorized access.  
2. Edge uses [Microsoft Intune Mobile Application Management](/mem/intune/fundamentals/deployment-guide-enrollment-mamwe) and Microsoft Defender with Cloud Apps (coming soon) to enforce compliant device usage on unmanaged devices to provide optimal security.  
3. Edge integrates with [Azure Application Proxy](/entra/identity/app-proxy/overview-what-is-app-proxy) to secure remote access to on-premises applications.
4. Edge uses Zero Trust Network Access (ZTNA) infrastructure, powered by [Microsoft Entra](https://www.microsoft.com/en-us/security/business/identity-access/microsoft-entra-private-access) to help enforce compliance network access [in preview].  

## Safely introducing AI to the organization

Safely introduce AI by balancing productivity, data security, and compliance.

1. Copilot for work ensures [Commercial Data Protection (CDP)](/copilot/privacy-and-protections), meaning that Microsoft doesn't save or store any Large-language model (LLM) interactions. Data in motion is encrypted and no one in Microsoft can view the data, and LLM interactions can't be used to train the LLM model.  
2. Admins can block Copilot [access to page content](/copilot/edge), ensuring that company data isn't sent to the Copilot.  

## Providing unified manageability  

With the browser's importance to enterprise workflows, organizations see an increased need for a dedicated management experience to quickly deliver browser policies. With the Microsoft Edge management service, IT admins can streamline their browser management by reducing overhead, including reduced transition time when upgrading from E3 to E5.

1. Easily enable policy to corporate profiles in the browser through [Microsoft Edge management service](/deployedge/microsoft-edge-management-service) enables streamlined policy management to corporate profiles.

## Providing productivity in enterprise settings

Edge provides several features that enrich collaboration and maximize productivity in the browser.  

1. [Workspaces](https://www.microsoft.com/en-us/edge/features/workspaces?form=MA13FJ&ch=1) in Edge provide a platform for teams to easily collaborate and stay organized with cross-device syncing to supercharge productivity.  
2. [Compose](https://www.microsoft.com/en-us/edge/features/compose?form=MA13FJ) acts as an AI agent in the browser to support writing activities such as drafting emails, documents, and other materials.  
3. [Tab Groups](https://www.microsoft.com/en-us/edge/features/tab-groups?form=MA13FJ) helps users stay organized across in any browser window.
4. [Contextual summary with Copilot](/deployedge/edge-learnmore-copilot-page-summary-results) in Edge can provide support for more efficient research and browsing experiences.
5. The [work feed](/deployedge/microsoft-edge-enterprise-ntp) in Edge helps users stay up to date on the latest internal network and industry news.
6. [Text prediction](https://www.microsoft.com/en-us/edge/features/text-prediction?form=MA13FJ) in Edge streamlines communication in text boxes in the browser.  

## How to configure Edge as a Secure Enterprise Browser for E5 licenses

In the E5 License Tier, Microsoft recommends the following steps to get the most out of your E5 license.

Follow the steps below BEFORE following the steps in the E3 managed device section.

### For managed devices

1. Provide data leak protections across the machine and in the browser by deploying Purview DLP. For more information, see:  
   - [Learn about data loss prevention](/purview/dlp-learn-about-dlp)
   - [Create and deploy a data loss prevention policy](/purview/dlp-create-deploy-policy)
   - [Configure endpoint DLP settings](/purview/dlp-configure-endpoint-settings#sensitive-service-domain-groups)
   - [Using Endpoint DLP](/purview/endpoint-dlp-using#scenario-6-monitor-or-restrict-user-activities-on-sensitive-service-domains)
2. If your organization would like extensive logging of actions taken on the browser (good for capturing risk signals over time), then use Microsoft Purview Insider Risk Management.
   - For more information, see  [Insider risk management](/purview/insider-risk-management-solution-overview) 
3. Capture PDF and document sensitivity in the browser by using Microsoft Purview Information Protection and safely view in the browser. For more information, see:
   - [Get started with sensitivity labels](/purview/get-started-with-sensitivity-labels) 
   - [PDF reader in Microsoft Edge](/deployedge/microsoft-edge-pdf#protected-pdfs)
4. For easy DLP controls for Microsoft services accessed in the webs, configure Microsoft Defender for Cloud Apps AND turn on Edge for Business protections in the admin portal. For more information, see:
   - [Get started - Microsoft Defender for Cloud Apps](/defender-cloud-apps/get-started)
   - [In-browser protection with Microsoft Edge for Business - Microsoft Defender for Cloud Apps](/defender-cloud-apps/in-browser-protection)

### For BYOD (Bring Your Own Device)/unmanaged devices

Follow the steps below BEFORE following the steps in the E3 BYOD device section.

1. For easy DLP controls for Microsoft services accessed in the webs, configure Microsoft Defender for Cloud Apps AND turn on Edge for Business protections in the admin portal. For more information, see:
   - [Get started - Microsoft Defender for Cloud Apps](/defender-cloud-apps/get-started)
   - [In-browser protection with Microsoft Edge for Business - Microsoft Defender for Cloud Apps](/defender-cloud-apps/in-browser-protection)

## How to Configure Edge as a Secure Enterprise Browser for E3 licenses

In the E3 License Tier, Microsoft recommends the following steps to get the most out of your E3 license.  

### For managed devices

1. Deploy Conditional Access to ensure that your corporate assets are only accessed by authorized users from a protected environment, ensuring both productivity and security.  
   - For more information, see [Microsoft Edge and Conditional Access](/DeployEdge/ms-edge-security-conditional-access)
2. For granular controls (such as extension controls, safe AI, blocking insecure browsers, zero-day protection, and customized organizational branding in the browser), configure the Microsoft Edge Management Service.
   - For more information, see [Microsoft Edge management service](/deployedge/microsoft-edge-management-service)
3. If some of your users are multitenant, use TRv2 protections.  
   - For more information, see [Configure tenant restrictions](/entra/external-id/tenant-restrictions-v2#step-3-enable-tenant-restrictions-on-windows-managed-devices), [Microsoft Entra ID - Microsoft Entra External ID](/entra/external-id/external-identities-overview)
4. To heighten in-browser productivity, configure the work feed to help keep users focused and up to date.  
   - For more information, see [Microsoft Edge Enterprise new tab page](/deployedge/microsoft-edge-enterprise-ntp)
5. To help your users find work information as quickly as possible, enable Microsoft Bing @ Work (Search in Bing)  
   - For more information, see [Overview of Microsoft Search in Bing](/microsoftsearch/overview-microsoft-search-bing)
6. If your users need remote access to on-premises applications, use Azure Application Proxy.
   - For more information, see [Add an on-premises application for remote access through application proxy in Microsoft Entra ID](/entra/identity/app-proxy/application-proxy-add-on-premises-application)
7. Keep users safe on the web by enabling Website Typo Protection, Enhanced Security Mode (ESM), and Phishing Protection (Microsoft Defender Smart Screen). For more information, see:
   - Typo protection: [Microsoft Edge Browser Policy Documentation](/deployedge/microsoft-edge-policies#edge-website-typo-protection-settings-policies)
   - Enhanced Security Mode: [Browse more safely with Microsoft Edge](/DeployEdge/microsoft-edge-security-browse-safer)
   - Phishing protection: [Microsoft Defender SmartScreen overview - Windows Security](/windows/security/operating-system-security/virus-and-threat-protection/microsoft-defender-smartscreen/)

### For BYOD (Bring Your Own Device)/unmanaged devices  

1. Deploy Conditional Access to ensure that your corporate assets are only accessed by authorized users from a protected environment, ensuring both productivity and security.  
   -  For more information, see  [Microsoft Edge and Conditional Access](/DeployEdge/ms-edge-security-conditional-access)
2. For desktop BYOD coverage in the browser, set up Microsoft Intune MAM.
   -  For more information, see [Secure your corporate data using Microsoft Edge for Business](/mem/intune/apps/mamedge-overview).
3. For granular controls (such as extension controls, safe AI, blocking insecure browsers, zero-day protection, and customized organizational branding in the browser), configure Microsoft Edge Management Service.
   -  For more information, see  [Microsoft Edge management service](/deployedge/microsoft-edge-management-service).
4. If some of your users are multitenant, use TRv2 protections.  
   - For more information, see [Configure tenant restrictions](/entra/external-id/tenant-restrictions-v2#step-3-enable-tenant-restrictions-on-windows-managed-devices), [Microsoft Entra ID - Microsoft Entra External ID](/entra/external-id/external-identities-overview)
5.  To heighten in-browser productivity, configure the work feed to help keep users focused and up to date.  
    -  For more information, see  [Microsoft Edge Enterprise new tab page](/deployedge/microsoft-edge-enterprise-ntp) 
6. To help your users find work information as quickly as possible, enable Microsoft Bing @ Work (Search in Bing)  
   -  For more information, see  [Overview of Microsoft Search in Bing](/microsoftsearch/overview-microsoft-search-bing)
7. If your users need remote access to on-premises applications, use Azure Application Proxy.
   - For more information, see [Add an on-premises application for remote access through application proxy in Microsoft Entra ID](/entra/identity/app-proxy/application-proxy-add-on-premises-application)
8. Keep users safe on the web by enabling Website Typo Protection, Enhanced Security Mode (ESM), and Phishing Protection (Microsoft Defender Smart Screen). For more information, see:
   - Typo protection: [Microsoft Edge Browser Policy Documentation](/deployedge/microsoft-edge-policies#edge-website-typo-protection-settings-policies)
   - Enhanced Security Mode: [Browse more safely with Microsoft Edge](/DeployEdge/microsoft-edge-security-browse-safer)
   - Phishing protection: [Microsoft Defender SmartScreen overview - Windows Security](/windows/security/operating-system-security/virus-and-threat-protection/microsoft-defender-smartscreen/)

> [!NOTE]
> Commercial Data Protection (CDP) is always on by default in Copilot when signed in with Microsoft Entra ID except for Government and Education users. Enabling Commercial Data Protection (CDP) for Government and Education users instructions can be found [here](/copilot/manage).  
>
> Microsoft Intune MAM is also able to cover BYOD Mobile experiences and set up information can be found [here](/mem/intune/apps/manage-microsoft-edge).

## See also

- [Additional detailed Microsoft Edge for Business FAQs available in our Tech Community](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/microsoft-edge-for-business-faq/ba-p/3891837)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)

