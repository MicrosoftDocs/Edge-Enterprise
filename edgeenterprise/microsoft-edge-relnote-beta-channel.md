---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 12/09/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Microsoft Edge release notes for Beta Channel"
---

# Release notes for Microsoft Edge Beta Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Beta Channel. Archived versions of these release notes are available at [Archived release notes for Microsoft Edge Beta Channel](./microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> Microsoft Edge Web Platform constantly evolves to improve user experience, security, and privacy. To learn more, see [Site compatibility-impacting changes coming to Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## Version 109.0.1518.14: December 7, 2022

### Feature update

- **MSA-AAD Account Linking.** Microsoft is enabling users who have a personal Microsoft account (an MSA) and a Microsoft user account through their work or school (an Azure Active Directory account) to "link" the two types of accounts together. "Linked accounts" means that users will be able to see some of the content from their personal account alongside the tailored content from their work or school account. They're also able to earn Microsoft Rewards points in their personal account from their activities while using their work or school account. More blended experiences may be made available.  For more information, see the [Account Linking FAQ](https://support.microsoft.com/en-us/account-billing/account-linking-faq-c66effb9-02e6-49c0-89e1-ae4d8644e6f7) and the [Account Linking IT Admins FAQ](https://support.microsoft.com/en-us/account-billing/account-linking-it-admins-faq-72f0dc4e-b632-439e-b90c-347043a7b75a). Tenant admins can learn how to control this feature in the Message Center section of the Microsoft 365 Admin Center. Also, this feature can be controlled by using the [LinkedAccountEnabled](/deployedge/microsoft-edge-policies#linkedaccountenabled) policy.

- **TLS server certificate verification changes.**  In Microsoft Edge version 110, the certificate trust list and the certificate verifier will be decoupled from the host operating system’s root store.  Instead, the default certificate trust list and the certificate verifier will be provided by and shipped with the browser.  The [MicrosoftRootStoreEnabled](/deployedge/microsoft-edge-policies#microsoftrootstoreenabled) policy is now available for testing to control when the built-in root store and certificate verifier are used.  Support for the policy is planned for removal in Microsoft Edge version 111.  For more information, see [Changes to Microsoft Edge browser TLS server certificate verification](/deployedge/microsoft-edge-security-cert-verification).  **Note:** This feature is a controlled feature rollout in Microsoft Edge version 109.  If you don't see this feature, check back as we continue our rollout.  

### Policy updates

#### New policies

- [WebHidAllowAllDevicesForUrls](/DeployEdge/microsoft-edge-policies#webhidallowalldevicesforurls) - Allow listed sites to connect to any HID device
- [WebHidAllowDevicesForUrls](/DeployEdge/microsoft-edge-policies#webhidallowdevicesforurls) - Allow listed sites connect to specific HID devices
- [WebHidAllowDevicesWithHidUsagesForUrls](/DeployEdge/microsoft-edge-policies#webhidallowdeviceswithhidusagesforurls) - Automatically grant permission to these sites to connect to HID devices containing top-level collections with the given HID usage
- [MicrosoftRootStoreEnabled](/DeployEdge/microsoft-edge-policies#microsoftrootstoreenabled) - Determines whether the Microsoft Root Store and built-in certificate verifier will be used to verify server certificates
- [DefaultClipboardSetting](/DeployEdge/microsoft-edge-policies#defaultclipboardsetting) - Default clipboard site permission
- [ClipboardAllowedForUrls](/DeployEdge/microsoft-edge-policies#clipboardallowedforurls) - Allow clipboard use on specific sites
- [ClipboardBlockedForUrls](/DeployEdge/microsoft-edge-policies#clipboardblockedforurls) - Block clipboard use on specific sites
- [SearchFiltersEnabled](/DeployEdge/microsoft-edge-policies#searchfiltersenabled) - Search Filters Enabled

#### Deprecated policies

- [SetTimeoutWithout1MsClampEnabled](/DeployEdge/microsoft-edge-policies#settimeoutwithout1msclampenabled) - Control Javascript setTimeout() function minimum timeout
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains

## Version 108.0.1462.42: December 5, 2022

Fixed various bugs and performance issues.

## Version 108.0.1462.38: December 2, 2022

Fixed various bugs and performance issues.

## Version 108.0.1462.35: November 28, 2022

Fixed various bugs and performance issues.

## Version 108.0.1462.28: November 21, 2022

Fixed various bugs and performance issues.

## Version 108.0.1462.20: November 14, 2022

Fixed various bugs and performance issues.

<!---                   --->
<!--- from Version 108.0.1462.15: November 10, 2022 to Version 107.0.1418.13: October 18, 2022 -->
<!--- from Version 107.0.1418.8: October 13, 2022 to Version 106.0.1370.17: September 16, 2022 -->
<!-- from Version 106.0.1370.15: September 15, 2022 to Version Version 105.0.1343.10: August 19, 2022 ---->
<!--- from Version 105.0.1343.7: August 16, 2022 to Version 104.0.1293.21: July 14 ---->
<!--- from Version 104.0.1293.14: July 7 to Version 103.0.1264.17: June 6 ---->
<!--- from Version 103.0.1264.13: June 2 to Version 102.0.1245.12: May 13 ---->
<!--- from Version 102.0.1245.7: May 10 to Version 101.0.1210.14: April 12 ---->
<!--- from Version 101.0.1210.10: April 8 to Version 100.0.1185.12: March 18 --->
<!--- from Version 100.0.1185.10: March 17 to Version 99.0.1150.16: February 14 --->
<!--- From Version 99.0.1150.11: February 9 to Version 98.0.1108.27: January 19 --->
<!-- archive from Version 98.0.1108.23: January 14 to Version 97.0.1072.28: December 8 -->
<!--- Version 97.0.1072.21: December 1 to Version 96.0.1054.13: November 5  --->
<!--- archive from Version 96.0.1054.8: November 1 to Version 95.0.1020.14: October 5  --->
<!-- archive from version 95.0.1020.9: September 28 to version 94.0.992.14: September 7 -->
<!-- archive from Version 94.0.992.9: September 2 to Version 92.0.902.40: July 6 -->
<!--Archive from Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!-- Archive from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 --->
<!-- Archive from Version 87.0.664.12: October 20 to version 86.0.622.15: September 14 -->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
