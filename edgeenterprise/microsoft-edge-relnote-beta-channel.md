---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 10/12/2022
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

## Version 107.0.0000.00: October 00

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

## Version 106.0.1370.30: September 29, 2022

Fixed various bugs and performance issues.

## Version 106.0.1370.26: September 26, 2022

Fixed various bugs and performance issues.

## Version 106.0.1370.17: September 16, 2022

Fixed various bugs and performance issues.

## Version 106.0.1370.15: September 15, 2022

Fixed various bugs and performance issues.

### Feature updates

- **More reliable web defense.** Browse the web with more reliable protection thanks to the rewritten [Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) library for Microsoft Edge on Windows and macOS. The new SmartScreen library was first made available on Windows with Microsoft Edge version 103, and now makes its debut on macOS with Microsoft Edge version 106. The [NewSmartScreenLibraryEnabled](/deployedge/microsoft-edge-policies#newsmartscreenlibraryenabled) policy is now deprecated in Microsoft Edge version 106 and will be obsolete in Microsoft Edge version 107.

### Policy updates

#### New policies

- [EfficiencyModeEnabled](/DeployEdge/microsoft-edge-policies#efficiencymodeenabled) - Efficiency mode enabled
- [EfficiencyModeOnPowerEnabled](/DeployEdge/microsoft-edge-policies#efficiencymodeonpowerenabled) - Enable efficiency mode when the device is connected to a power source
- [InternetExplorerIntegrationAlwaysUseOSCapture](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationalwaysuseoscapture) Always use the OS capture engine to avoid issues with capturing Internet Explorer mode tabs

#### Deprecated policies

- [NewSmartScreenLibraryEnabled](/deployedge/microsoft-edge-policies#newsmartscreenlibraryenabled) – Allows the Microsoft Edge browser to load the new SmartScreen library for any SmartScreen checks on site URLs or application downloads.

#### Obsoleted policies

- [OutlookHubMenuEnabled](/DeployEdge/microsoft-edge-policies#outlookhubmenuenabled) - Allow users to access the Outlook menu
- [EdgeDiscoverEnabled](/DeployEdge/microsoft-edge-policies#edgediscoverenabled) - Discover feature In Microsoft Edge

## Version 105.0.1343.34: September 9, 2022

Fixed various bugs and performance issues.

## Version 105.0.1343.27: September 2, 2022

Fixed various bugs and performance issues.

## Version 105.0.1343.23: August 31, 2022

Fixed various bugs and performance issues.

## Version 105.0.1343.17: August 26, 2022

Fixed various bugs and performance issues.

## Version 105.0.1343.10: August 19, 2022

Fixed various bugs and performance issues.

## Version 105.0.1343.7: August 16, 2022

Fixed various bugs and performance issues.

### Feature updates

- **Improvement to the Cloud Site List Management experience for IE mode.**

  - You can restore to one of the last 3 published versions of your site list in the Microsoft 365 Admin Center. For more information, see [Restore a previous version of a site list](/deployedge/edge-ie-mode-cloud-site-list-mgmt#restore-a-previous-version-of-a-site-list).
  - You can identify gaps in your enterprise site list by configuring reporting of site feedback with the [InternetExplorerIntegrationCloudUserSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) and [InternetExplorerIntegrationCloudNeutralSitesReporting policies](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting). You can view local site list URLs from users and potentially misconfigured neutral site URLs in the Microsoft Edge site lists experience in the Microsoft 365 Admin Center. To learn more, see [View site feedback on the Microsoft 365 Admin Center](/deployedge/edge-ie-mode-cloud-site-list-mgmt#view-site-feedback-on-the-microsoft-365-admin-center-1).
  - You can configure session cookie sharing between Microsoft Edge and Internet Explorer for IE mode on your site list in the Microsoft 365 Admin Center. To learn more, see [Cookie sharing between Microsoft Edge and Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

- **Improvements to the Cloud Site List Management experience for IE mode now available in GCC.** GCC customers can now utilize the full Microsoft Edge site list experience in the Microsoft 365 Admin Center.

### Policy updates

#### New policies

- [ExemptFileTypeDownloadWarnings](/DeployEdge/microsoft-edge-policies#exemptfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains
- [InternetExplorerIntegrationAlwaysWaitForUnload](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationalwayswaitforunload) - Wait for Internet Explorer mode tabs to completely unload before ending the browser session
- [MicrosoftEditorProofingEnabled](/DeployEdge/microsoft-edge-policies#microsofteditorproofingenabled) - Spell checking provided by Microsoft Editor
- [MicrosoftEditorSynonymsEnabled](/DeployEdge/microsoft-edge-policies#microsofteditorsynonymsenabled) - Synonyms are provided when using Microsoft Editor spell checker
- [PrintPdfAsImageDefault](/DeployEdge/microsoft-edge-policies#printpdfasimagedefault) - Print PDF as Image Default
- [UnthrottledNestedTimeoutEnabled](/DeployEdge/microsoft-edge-policies#unthrottlednestedtimeoutenabled) - JavaScript setTimeout will not be clamped until a higher nesting threshold is set

#### Deprecated policy

- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains

#### Additional change

- [GuidedSwitchEnabled](/DeployEdge/microsoft-edge-policies#guidedswitchenabled) - Add Linux platform support

## Version 104.0.1293.44: August 3

Fixed various bugs and performance issues.

### Feature updates

- **Enhance your security on the web**. Improvements to **Enhance your security on the web** in *edge://settings/privacy* now include **Basic** as the new default option.  With this option, Microsoft Edge will apply added security protection to the less visited sites. This preserves the user experience for the most popular sites on the web. For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

## Version 104.0.1293.41: August 1

Fixed various bugs and performance issues.

## Version 104.0.1293.35: July 25

Fixed various bugs and performance issues.

## Version 104.0.1293.25: July 18

Fixed various bugs and performance issues.

### Feature updates

- **Import Chrome data without Chrome during First Run Experience.** This feature lets a user bring in their Chrome data by logging in to their Google account during Microsoft Edge's First Run Experience. This feature can be turned off by disabling First Run Experience with the [HideFirstRunExperience](/deployedge/microsoft-edge-policies#hidefirstrunexperience) policy, or by setting [AutoImportAtFirstRun](/deployedge/microsoft-edge-policies#autoimportatfirstrun) to 'DisabledAutoImport'.

## Version 104.0.1293.21: July 14

Fixed various bugs and performance issues.


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

