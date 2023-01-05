---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 01/05/2023
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
