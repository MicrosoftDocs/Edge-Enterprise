---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 01/12/2023
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Microsoft Edge release notes for Stable Channel"
---
# Release notes for Microsoft Edge Stable Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Stable Channel.

- All the security updates are listed in [Release notes for Microsoft Edge Security Updates](./microsoft-edge-relnotes-security.md).
- Archived release notes for Microsoft Edge Stable Channel are located in [Archived release notes for Microsoft Edge Stable Channel](./microsoft-edge-relnote-archive-stable-channel.md).

 To understand Microsoft Edge channels, see the [Overview of the Microsoft Edge channels](./microsoft-edge-channels.md).

> [!NOTE]
> For the Stable Channel, updates will roll out progressively over one or more days. To learn more, see [Progressive rollouts for Microsoft Edge updates](./microsoft-edge-update-progressive-rollout.md).
>
> Microsoft Edge Web Platform constantly evolves to improve user experience, security, and privacy. To learn more, see [Site compatibility-impacting changes coming to Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## Version 108.0.1462.83: January 12, 2023

Fixed various bugs and performance issues for Extended Stable release.

## Version 109.0.1518.49: January 12, 2023

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-12-2023).

### Feature updates

- **Account Linking between a personal Microsoft account (MSA) and Azure Active Directory (AAD) account.** Microsoft is enabling users to link a personal Microsoft account (MSA) and Azure Active Directory (AAD) account through work or school.  Once linked, users can earn Microsoft Rewards points for Microsoft Bing searches done in their browser or Windows search box while signed in with their work or school account. For more information, see the [Account Linking FAQ](https://support.microsoft.com/account-billing/account-linking-faq-c66effb9-02e6-49c0-89e1-ae4d8644e6f7) and the [Account Linking IT Admins FAQ](https://support.microsoft.com/account-billing/account-linking-it-admins-faq-72f0dc4e-b632-439e-b90c-347043a7b75a). Tenant admins can also control this feature in the Message Center section of the Microsoft 365 Admin Center or by using the [LinkedAccountEnabled](/deployedge/microsoft-edge-policies#linkedaccountenabled) policy.

- **TLS server certificate verification changes.** In Microsoft Edge version 110, the certificate trust list and the certificate verifier will be decoupled from the host operating system’s root store.  Instead, the default certificate trust list and the certificate verifier will be provided by and shipped with the browser.  The [MicrosoftRootStoreEnabled](/deployedge/microsoft-edge-policies#microsoftrootstoreenabled) policy is now available for testing to control when the built-in root store and certificate verifier are used.  Support for the policy is planned to be removed in Microsoft Edge version 111.  For more information, see [Changes to Microsoft Edge browser TLS server certificate verification | Microsoft Learn](/deployedge/microsoft-edge-security-cert-verification).  **Note:** This is a controlled feature rollout in Microsoft Edge version 109.  If you don't see this feature, check back as we continue our rollout.

- **Text prediction.**  To help you write faster and with fewer mistakes, Microsoft Edge provides word and sentence predictions for long-form editable text fields on web pages.  Administrators can control the availability of text predictions using the [TextPredictionEnabled](/deployedge/microsoft-edge-policies#textpredictionenabled) policy.  Text prediction is currently only available in English within the US, India, and Australia.  We will continue to add new languages and regions in future versions of Microsoft Edge.  

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

## Version 108.0.1462.76: January 5, 2023

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 108.0.1462.54: December 16, 2022

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#december-16-2022).

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 108.0.1462.46: December 8, 2022

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 108.0.1462.42: December 5, 2022

> [!IMPORTANT]
> This update to Extended Stable contains a fix for [CVE-2022-4262](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-4262), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#december-5-2022)

### Feature updates

- **Graph APIs for Cloud Site List Management.** New Graph APIs that allow IT admins in organizations to create, manage, and publish their site lists for IE mode in the cloud.  For more information, see [Use the Edge API in Microsoft Graph](/graph/api/resources/browser-edge-api-overview?view=graph-rest-beta).

- **More reliable web defense.** Browse the web with more reliable protection thanks to the rewritten [Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) library for Microsoft Edge on Windows, Mac, and Linux. The new SmartScreen library was first made available on Windows and Mac, and now makes its debut on Linux with Microsoft Edge version 108. Microsoft Edge version 108 also brings new product optimizations (that is, better proxy handling) and bug fixes by having the SmartScreen library leverage Microsoft Edge’s built-in network stack.

### Policy updates

#### New policies

- [EncryptedClientHelloEnabled](/DeployEdge/microsoft-edge-policies#encryptedclienthelloenabled) - TLS Encrypted ClientHello Enabled
- [NewTabPageAppLauncherEnabled](/DeployEdge/microsoft-edge-policies#newtabpageapplauncherenabled) - Hide App Launcher on Microsoft Edge new tab page

#### Obsoleted policy

- [NewSmartScreenLibraryEnabled](/DeployEdge/microsoft-edge-policies#newsmartscreenlibraryenabled) Enable new SmartScreen library

## Version 107.0.1418.62: November 28, 2022

> [!IMPORTANT]
> This update contains a fix for [CVE-2022-4135](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-4135), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#november-28-2022).

## Version 106.0.1370.86: November 28, 2022

> [!IMPORTANT]
> This update to Extended Stable contains a fix for [CVE-2022-4135](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-4135), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#november-28-2022)

## Version 107.0.1418.56: November 21, 2022

Fixed various bugs and performance issues.

## Version 107.0.1418.52: November 17, 2022

Fixed various bugs and performance issues.

## Version 107.0.1418.42: November 10, 2022

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#november-10-2022).

## Version 106.0.1370.72: November 10, 2022

Fixed various bugs and performance issues for Extended Stable channel.

## Version 107.0.1418.35: November 3, 2022

Fixed various bugs and performance issues.

## Version 107.0.1418.26: October 29, 2022

> [!IMPORTANT]
> This update contains a fix for [CVE-2022-3723](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-3723), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-31-2022).

## Version 106.0.1370.61: October 29, 2022

> [!IMPORTANT]
> This update to Extended Stable contains a fix for [CVE-2022-3723](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-3723), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-31-2022)

## Version 106.0.1370.59: October 27, 2022

Fixed various bugs and performance issues for Extended Stable release.

## Version 107.0.1418.24: October 27, 2022

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-27-2022).

### Feature updates

- **Microsoft Edge sidebar.** The Microsoft Edge sidebar lets users access productivity tools side-by-side with their browsing window. For enterprise customers, the following experiences are currently turned on by default: Search, Discover, Office.com, and Outlook. Administrators can control the availability and configure the Microsoft Edge sidebar using the [HubsSidebarEnabled](/deployedge/microsoft-edge-policies#hubssidebarenabled), [ExtensionInstallBlockList](/deployedge/microsoft-edge-policies#extensioninstallblocklist), and [ExtensionInstallForceList](/deployedge/microsoft-edge-policies#extensioninstallforcelist) policies. The extension ID for each sidebar app can be found at *edge://sidebar-internals*.  For more information, see [Manage the sidebar in Microsoft Edge](/DeployEdge/microsoft-edge-sidebar).

- **New policy to give more flexibility in Microsoft Edge startup.** The [RestoreOnStartupUserURLsEnabled](/deployedge/microsoft-edge-policies#restoreonstartupuserurlsenabled) policy lets users add and remove their own URLs to open when starting Microsoft Edge while maintaining the mandatory list of sites specified by the admin.

### Policy updates

#### New policies

- [EdgeWorkspacesEnabled](/DeployEdge/microsoft-edge-policies#edgeworkspacesenabled) - Enable Workspaces
- [EnhanceSecurityModeBypassIntranet](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypassintranet) - Enhanced Security Mode configuraton for Intranet zone sites
- [EventPathEnabled](/DeployEdge/microsoft-edge-policies#eventpathenabled) - Re-enable the Event.path API until Microsoft Edge version 115
- [InternetExplorerIntegrationLocalMhtFileAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalmhtfileallowed) - Allow local MHTML files to open automatically in Internet Explorer mode
- [LinkedAccountEnabled](/DeployEdge/microsoft-edge-policies#linkedaccountenabled) - Enable the linked account feature
- [PerformanceDetectorEnabled](/DeployEdge/microsoft-edge-policies#performancedetectorenabled) - Performance Detector Enabled
- [RestoreOnStartupUserURLsEnabled](/DeployEdge/microsoft-edge-policies#restoreonstartupuserurlsenabled) - Allow users to add and remove their own sites during startup when the RestoreOnStartupURLs policy is configured
- [DefaultShareAdditionalOSRegionSetting](/DeployEdge/microsoft-edge-policies#defaultshareadditionalosregionsetting) - Set the default "share additional operating system region" setting
- [WebSelectEnabled](/DeployEdge/microsoft-edge-policies#webselectenabled) - Web Select Enabled
- [WebSQLAccess](/DeployEdge/microsoft-edge-policies#websqlaccess) - Force WebSQL to be enabled
- [WebSQLNonSecureContextEnabled](/DeployEdge/microsoft-edge-policies#websqlnonsecurecontextenabled) - Force WebSQL in non-secure contexts to be enabled

#### Deprecated policy

- [MicrosoftOfficeMenuEnabled](/DeployEdge/microsoft-edge-policies#microsoftofficemenuenabled) - Allow users to access the Microsoft Office menu

#### Obsoleted policy

- [BuiltinCertificateVerifierEnabled](/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) - Determines whether the built-in certificate verifier will be used to verify server certificates

## Version 106.0.1370.52: October 20, 2022

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 106.0.1370.47: October 14, 2022

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-14-2022).

## Version 106.0.1370.42: October 10, 2022

Fixed various bugs and performance issues.

## Version 106.0.1370.37: October 6, 2022

Fixed various bugs and performance issues.


<!--- from Version 106.0.1370.34: October 3, 2022 to Version 105.0.1343.27: September 2, 2022 -->
<!--- from Version 105.0.1343.25: September 1, 2022 to  Version 104.0.1293.70: August 25, 2022 -->

<!--- from Version 104.0.1293.63: August 19 to Version 102.0.1245.50: June 23 ---->
<!--- from Version 103.0.1264.37: June 23 to Version 102.0.1245.33: June 3 ---->
<!--- from Version 103.0.1264.37: June 23 to Version 102.0.1245.33: June 3 ---->
<!--- from Version 102.0.1245.30: May 31 to Version 100.0.1185.57: May 2 ---->
<!-- from Version 101.0.1210.32: April 28 to Version 100.0.1185.36: April 7 -->
<!---from Version 100.0.1185.29: April 1  to  Version 99.0.1150.36: March 7 --->
<!--- from Version 99.0.1150.30: March 3 to Version 98.0.1108.50: February 10 --->
<!--- from Version 98.0.1108.43: February 3 to Version 96.0.1054.72: January 6  -->
<!---- From Version 97.0.1072.55: January 6 to Version 96.0.1054.34: November 23 ---->
<!---archive from Version 96.0.1054.29: November 19 to Version 94.0.992.57: October 27 --->
<!-- archive from Version 95.0.1020.30: October 21 to Version 94.0.992.37: September 30 -->
<!-- archive from Version 94.0.992.31: September 24 to Version 93.0.961.44: September 9  -->
<!--- Archive from Version 93.0.961.38: September 2 to Version 92.0.902.62: July 29 --->
<!-- Archive from Version 92.0.902.55: July 22 to Version 91.0.864.37: May 27 -->
<!-- Archive from 89.0.774.45: March 4 to 90.0.818.66: May 20 ->
<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
