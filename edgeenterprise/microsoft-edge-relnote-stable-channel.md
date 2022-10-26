---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 10/20/2022
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

## Version 107.0.xxxx.x: October xx, 2022

### Feature updates

**MSA-AAD Account Linking.** Microsoft is enabling users who have a personal Microsoft account (an MSA) and a Microsoft user account through their work or school (an Azure Active Directory account) to "link" the two types of accounts together. "Linked accounts" means that users will be able to see some of the content from their personal account alongside the tailored content from their work or school account. They are also able to earn Microsoft Rewards points in their personal account from their activities while using their work or school account. Additional blended experiences may be made available. This feature can be controlled by using the [LinkedAccountEnabled](/deployedge/microsoft-edge-policies#linkedaccountenabled) policy. For more information, see ***Updated Link Needed***

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

## Version 106.0.1370.34: October 3, 2022

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-3-2022).

### Feature updates

- **More reliable web defense.** Browse the web with more reliable protection thanks to the rewritten [Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) library for Microsoft Edge on Windows and macOS. The new SmartScreen library was first made available on Windows with Microsoft Edge version 103, and now makes its debut on macOS with Microsoft Edge version 106. The [NewSmartScreenLibraryEnabled](/deployedge/microsoft-edge-policies#newsmartscreenlibraryenabled) policy is now deprecated in Microsoft Edge version 106 and will be obsolete in Microsoft Edge version 108.

- **Increased Work Results in the Microsoft Edge address bar.** We’ve increased the maximum number of work results that display in the address bar from 2 to 4, which offers greater visibility into the work content available to you as you search. This feature requires the [AddressBarMicrosoftSearchInBingProviderEnabled](/deployedge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled) policy enabled to work.

### Policy updates

#### New policies

- [EfficiencyModeEnabled](/DeployEdge/microsoft-edge-policies#efficiencymodeenabled) - Efficiency mode enabled
- [EfficiencyModeOnPowerEnabled](/DeployEdge/microsoft-edge-policies#efficiencymodeonpowerenabled) - Enable efficiency mode when the device is connected to a power source
- [InternetExplorerIntegrationAlwaysUseOSCapture](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationalwaysuseoscapture) - Always use the OS capture engine to avoid issues with capturing Internet Explorer mode tabs

#### Deprecated policies

- [NewSmartScreenLibraryEnabled](/DeployEdge/microsoft-edge-policies#newsmartscreenlibraryenabled) - Enable new SmartScreen library
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) - Configure ShadowStack crash rollback behavior

#### Obsoleted policies

- [OutlookHubMenuEnabled](/DeployEdge/microsoft-edge-policies#outlookhubmenuenabled) - Allow users to access the Outlook menu
- [EdgeDiscoverEnabled](/DeployEdge/microsoft-edge-policies#edgediscoverenabled) - Discover feature In Microsoft Edge

## Version 105.0.1343.53: September 26, 2022

Fixed various bugs and performance issues.

## Version 105.0.1343.50: September 22, 2022

Fixed various bugs and performance issues.

## Version 105.0.1343.42: September 15, 2022

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-15-2022).

## Version 104.0.1293.91: September 15, 2022

Fixed various bugs and performance issues for Extended Stable release.

## Version 105.0.1343.33: September 8, 2022

Fixed various bugs and performance issues.

## Version 104.0.1293.81: September 2, 2022

> [!IMPORTANT]
> This update to Extended Stable contains a fix for [CVE-2022-3075](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-3075), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-2-2022)

## Version 105.0.1343.27: September 2, 2022

> [!IMPORTANT]
> This update contains a fix for [CVE-2022-3075](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-3075), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-2-2022).

## Version 105.0.1343.25: September 1, 2022

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-1-2022).

### Feature updates

- **Enhanced security mode improvements.** Enhanced security mode now supports WebAssembly for x64 Windows. Additional cross-platform support is expected in the future. For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

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

#### Deprecated policies

- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains

#### Additional policy changes

- [GuidedSwitchEnabled](/DeployEdge/microsoft-edge-policies#guidedswitchenabled) - Add Linux platform support

## Version 104.0.1293.78: September 1, 2022

Fixed various bugs and performance issues for Extended Stable release.

## Version 104.0.1293.70: August 25, 2022

Fixed various bugs and performance issues.

## Version 104.0.1293.63 : August 19

> [!IMPORTANT]
> This update contains a fix for [CVE-2022-2856](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-2856), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-19-2022).

### Feature updates

- **Search in the Microsoft Edge sidebar.** Easily access an updated sidebar search via Microsoft Edge sidebar, including easy access to Microsoft Search in Bing for organizations. Note: This is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Gaming for the Microsoft Edge sidebar.** Play popular casual games for free. Administrators can control the availability of the Games menu in the Microsoft Edge sidebar. Note: This is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Discover in the Microsoft Edge sidebar.** Discover content relevant to the page you’re browsing including summaries, source information, and more. Note: This is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Get your favorite tools in the Microsoft Edge sidebar.** Easily access commonly used tools while you browse the web, including Calculator, Internet speed test, and Unit converter. Note: This is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Outlook in the Microsoft Edge sidebar.** Quickly and easily access Outlook Mail and Calendar. Note: This is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Office in the Microsoft Edge sidebar.** Quickly and easily access Microsoft Office documents and apps. Administrators can control the Microsoft Office menu in the Microsoft Edge sidebar. Note: This is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

## Version 104.0.1293.54: August 11

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 104.0.1293.47: August 5

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-5-2022).

### Feature updates

- **Enhance your security on the web**. Improvements to **Enhance your security on the web** in *edge://settings/privacy* now include **Basic** as the new default option. With this option, Microsoft Edge will apply added security protection to the less visited sites. This feature preserves the user experience for the most popular sites on the web. For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **Import Chrome data without Chrome during First Run Experience.** This feature lets a user bring in their Chrome data by logging in to their Google account during Microsoft Edge's First Run Experience. This feature can be turned off by disabling First Run Experience with the [HideFirstRunExperience](/deployedge/microsoft-edge-policies#hidefirstrunexperience) policy, or by setting [AutoImportAtFirstRun](/deployedge/microsoft-edge-policies#autoimportatfirstrun) to 'DisabledAutoImport'.

### Policy updates

#### New policies

- [AllowedDomainsForApps](/DeployEdge/microsoft-edge-policies#alloweddomainsforapps) - Define domains allowed to access Google Workspace
- [AskBeforeCloseEnabled](/DeployEdge/microsoft-edge-policies#askbeforecloseenabled) - Get user confirmation before closing a browser window with multiple tabs
- [BrowserCodeIntegritySetting](/DeployEdge/microsoft-edge-policies#browsercodeintegritysetting) - Configure browser process code integrity guard setting
- [DoubleClickCloseTabEnabled](/DeployEdge/microsoft-edge-policies#doubleclickclosetabenabled) - Double Click feature in Microsoft Edge enabled (only available in China)
- [ImportOnEachLaunch](/DeployEdge/microsoft-edge-policies#importoneachlaunch) - Allow import of data from other browsers on each Microsoft Edge launch
- [QuickSearchShowMiniMenu](/DeployEdge/microsoft-edge-policies#quicksearchshowminimenu) - Enables Microsoft Edge mini menu
- [PasswordManagerRestrictLengthEnabled](/DeployEdge/microsoft-edge-policies#passwordmanagerrestrictlengthenabled) - Restrict the length of passwords that can be saved in the Password Manager
- [PDFXFAEnabled](/DeployEdge/microsoft-edge-policies#pdfxfaenabled) - XFA support in native PDF reader enabled
- [TextPredictionEnabled](/DeployEdge/microsoft-edge-policies#textpredictionenabled) - Text prediction enabled by default

#### Obsoleted policy

- [U2fSecurityKeyApiEnabled](/DeployEdge/microsoft-edge-policies#u2fsecuritykeyapienabled) - Allow using the deprecated U2F Security Key API

## Version 103.0.1264.77: July 28

Fixed various bugs and performance issues.

## Version 102.0.1245.62: July 27

Fixed various bugs and performance issues for Extended Stable release.

## Version 103.0.1264.71: July 22

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#july-22-2022).

## Version 103.0.1264.62: July 14

Fixed various bugs and performance issues. We recommend that users install this update to address the following issue.

### Known issue

Microsoft Edge on 32-bit (x86) Windows 10 Version 1809 may experience startup issues with the upcoming July Non-Security Windows Updates (KB5015880 - 17763.3224). This is fixed with the latest Microsoft Edge Stable channel release, version 103.0.1264.62. Enterprise users encountering this issue on Microsoft Edge Extended Stable channel version 102 need to disable the  [NewSmartScreenLibraryEnabled](/deployedge/microsoft-edge-policies#newsmartscreenlibraryenabled) policy.

## Version 103.0.1264.49: July 6

> [!Important]
> This update contains a fix for [CVE-2022-2294](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-2294), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#july-6-2022).

## Version 102.0.1245.56: July 6

Fixed various bugs and performance issues for Extended Stable release.

## Version 103.0.1264.44: June 30

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-30-2022).

## Version 102.0.1245.50: June 23

Fixed various bugs and performance issues for Extended Stable release.

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
