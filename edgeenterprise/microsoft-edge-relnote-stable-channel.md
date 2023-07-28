---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 07/28/2023
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

## Version 115.0.1901.188: July 27, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.90: July 21, 2023

Fixed various bugs and performance issues for Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#july-21-2023).

## Version 115.0.1901.183: July 21, 2023

Fixed various bugs and performance issues for Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#july-21-2023).

### Feature update

- **Microsoft Edge management service.** Microsoft Edge management service is an area in the Microsoft 365 admin center where admins can manage the Microsoft Edge browser. It's a simple and easy-to-manage experience. Admins are able to configure all Microsoft Edge browser policies for their organization in a configuration profile and set-up the browser to use these settings. For more information, see [Microsoft Edge management service](/deployedge/microsoft-edge-management-service). **Note:** We'll start rolling out this experience on July 20 and expect to finish the rollout by next week.

### Policy updates

#### New policies

- [ComposeInlineEnabled](/deployedge/microsoft-edge-policies#composeinlineenabled) - Compose is enabled for writing on the web
- [EdgeManagementEnabled](/deployedge/microsoft-edge-policies#edgemanagementenabled) - Microsoft Edge management enabled
- [EdgeManagementEnrollmentToken](/deployedge/microsoft-edge-policies#edgemanagementenrollmenttoken) - Microsoft Edge management enrollment token
- [EdgeManagementExtensionsFeedbackEnabled](/deployedge/microsoft-edge-policies#edgemanagementextensionsfeedbackenabled) - Microsoft Edge management extensions feedback enabled
- [EnhanceSecurityModeIndicatorUIEnabled](/deployedge/microsoft-edge-policies#enhancesecuritymodeindicatoruienabled) - Manage the indicator UI of the Enhanced Security Mode (ESM) feature in Microsoft Edge
- [EnhanceSecurityModeOptOutUXEnabled](/deployedge/microsoft-edge-policies#enhancesecuritymodeoptoutuxenabled) - Manage opt-out user experience for Enhanced Security Mode (ESM) in Microsoft Edge
- [SearchForImageEnabled](/deployedge/microsoft-edge-policies#searchforimageenabled) - Search for image enabled
- [WalletDonationEnabled](/deployedge/microsoft-edge-policies#walletdonationenabled) - Wallet Donation Enabled

#### Additional policy changes

- [EnforceLocalAnchorConstraintsEnabled](/deployedge/microsoft-edge-policies#enforcelocalanchorconstraintsenabled) - Policy obsoletion delayed from 115 to 118

## Version 114.0.1823.86: July 17, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.82: July 13, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#july-13-2023).

## Version 114.0.1823.79, July 10, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.67: June 29, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-29-2023).

## Version 114.0.1823.58: June 22, 2023

Fixed various bugs and performance issues for Stable and Extended Stable release.

- **Google Docs Offline extension for Microsoft Edge.**  Google Docs Offline is an extension provided by Google to allow users to work on Google Docs, Sheets, Slides and Drive without internet access. This extension also provides advanced cut, copy, and paste functionalities across Google Editors.  The Google Docs Offline extension will be pre-installed and will be disabled by default for Microsoft Edge users. When a user navigates to Google Docs, the extension will be auto-enabled. Administrators can use the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) and [ExtensionInstallBlocklist](/deployedge/microsoft-edge-policies#extensioninstallblocklist) policies to block the auto-installation of the Google Docs Offline extension.  **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

## Version 114.0.1823.55: June 19, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.51: June 15, 2023

Fixed various bugs and performance issues for Stable and Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-15-2023).

### Feature update

- Web Select is now a part of Web Capture. Users can access Web Select through Web Capture feature or press **Ctrl** + **Shift** + **X** shortcut directly for quick access.

### Policy updates

#### Additional policy changes

- [WebSelectEnabled](/deployedge/microsoft-edge-policies#webselectenabled) - This policy is deprecated. It is currently supported but will become obsolete in version 117.
- [WebCaptureEnabled](/deployedge/microsoft-edge-policies#webcaptureenabled) - Since Web Select is now a part of Web Capture, this policy will enable/ disable both Web Select and Web Capture.

## Version 109.0.1518.115: June 13, 2023

> [!NOTE]
> This update was done for our M109 Windows down-level extended support.  We're shipping 109 to Win 7, 8, and 8.1 (including Server 2012 R2 which is based on Win 8.1).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-13-2023).

## Version 114.0.1823.43: June 8, 2023

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 114.0.1823.41: June 6, 2023

Fixed various bugs and performance issues.

> [!IMPORTANT]
> This update to Stable contains a fix for [CVE-2023-3079](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2023-3079), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-6-2023).

## Version 114.0.1823.37: June 2, 2023

Fixed various bugs and performance issues for Stable and Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-2-2023).

### Feature update

- **Microsoft Edge Workspaces.** Edge Workspaces provides a way for customers to organize their browsing tasks into dedicated windows. Edge Workspaces lets users share a set of browser tabs so working groups can view the same websites and latest working files in one place and stay on the same page. Each Edge Workspace contains its own set of tabs and favorites, all created and curated by the user and their collaborators. Edge Workspaces are automatically saved and kept up to date. For more information, see [Microsoft Edge Workspaces](/deployedge/microsoft-edge-workspaces).

### Policy updates

#### New policies

- [StandaloneHubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#standalonehubssidebarenabled) - Standalone Sidebar Enabled
- [ShowDownloadsToolbarButton](/DeployEdge/microsoft-edge-policies#showdownloadstoolbarbutton) - Show Downloads button on the toolbar

#### Obsoleted policy

- [MicrosoftRootStoreEnabled](/DeployEdge/microsoft-edge-policies#microsoftrootstoreenabled) - Determines whether the Microsoft Root Store and built-in certificate verifier will be used to verify server certificates

#### Additional policy changes

- [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode) - BasicMode is deprecated
- [EdgeWorkspacesEnabled](/DeployEdge/microsoft-edge-policies#edgeworkspacesenabled) - If the policy isn't configured users are able to access the Microsoft Edge Workspaces feature

## Version 113.0.1774.57: May 25, 2023

Fixed various bugs and performance issues.

## Version 112.0.1722.84: May 18, 2023

Fixed various bugs and performance issues for Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-18-2023).

## Version 113.0.1774.50: May 18, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-18-2023).

### Feature update

- **Microsoft recommended browser settings.** This new prompt in Microsoft Edge lets users benefit from the Microsoft recommended settings. This feature gives users the option to set Microsoft Edge as the default browser and/or set Microsoft Bing as the default search engine, if they aren't already selected. If a user accepts the prompt, their default browser is updated to Microsoft Edge, and their default search engine will be updated to Microsoft Bing. Administrators can control the availability of the default browser settings campaign using the [DefaultBrowserSettingsCampaignEnabled](/deployedge/microsoft-edge-policies#defaultbrowsersettingscampaignenabled) policy.

## Version 113.0.1774.42: May 11, 2023

Fixed various bugs and performance issues.

## Version 112.0.1722.77: May 9, 2023

Fixed various bugs and performance issues for Extended Stable release.

## Version 113.0.1774.35: May 5, 2023

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-5-2023).

### Feature update

- **Improvements to downloads security.** Microsoft Edge now has the capability to scan archives (.zip, .rar, .7z) for any malwares using Microsoft Defender SmartScreen. This functionality is currently available on Windows only and provides extra protection where known malwares were being distributed within these archives.

- **Improvements to enhanced security mode.**  Enhanced security mode provides an extra layer of protection when browsing the web and visiting unfamiliar sites.  In this release updates include consolidating the security level settings to Balanced and Strict mode.  For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **Switch from Microsoft Autoupdate to EdgeUpdater for macOS**. Microsoft Edge for macOS will start using a new updater named EdgeUpdater. This change only affects Microsoft Edge on macOS. If you use update preferences for Microsoft Autoupdate to prevent browser updates, you will need to transition to the new EdgeUpdater UpdateDefault policy before Microsoft Edge 113 to prevent future automatic updates. For more information, see [Microsoft Edge for macOS switches from Microsoft AutoUpdate to EdgeUpdater](/deployedge/edge-learnmore-edgeupdater-for-macos).

- **New policy for PDF View Settings.** The [RestorePdfView](/deployedge/microsoft-edge-policies#restorepdfview) policy lets Admins control PDF View Recovery in Microsoft Edge.  When enabled or if the policy isn't configured, Microsoft Edge will recover the last state of PDF view and land users on the section where they ended reading in the last session.

- **Updated Microsoft Root Store policy.** The [MicrosoftRootStoreEnabled](/deployedge/microsoft-edge-policies#microsoftrootstoreenabled) policy will now be supported in Microsoft Edge version 113 and 114.  It will be removed in Microsoft Edge version 115.  For more information, see [Changes to Microsoft Edge browser TLS server certificate verification](/deployedge/microsoft-edge-security-cert-verification).

### Policy updates

#### New policies

- [DiscoverPageContextEnabled](/DeployEdge/microsoft-edge-policies#discoverpagecontextenabled) - Enable Discover access to page contents for AAD profiles
- [DefaultBrowserSettingsCampaignEnabled](/DeployEdge/microsoft-edge-policies#DefaultBrowserSettingsCampaignEnabled) - Enables default browser settings campaigns
- [EnforceLocalAnchorConstraintsEnabled](/DeployEdge/microsoft-edge-policies#enforcelocalanchorconstraintsenabled) - Determines whether the built-in certificate verifier will enforce constraints encoded into trust anchors loaded from the platform trust store
- [RestorePdfView](/DeployEdge/microsoft-edge-policies#restorepdfview) - Restore PDF view
- [ReadAloudEnabled](/DeployEdge/microsoft-edge-policies#readaloudenabled) - Enable Read Aloud feature in Microsoft Edge
- [ShowDownloadsToolbarButton](/DeployEdge/microsoft-edge-policies#showdownloadstoolbarbutton) - Show Downloads button on the toolbar
- [TabServicesEnabled](/DeployEdge/microsoft-edge-policies#tabservicesenabled) - Tab Services enabled

## Version 112.0.1722.71: May 4, 2023

Fixed various bugs and performance issues for Extended Stable release.

## Version 112.0.1722.68: May 1, 2023

Fixed various bugs and performance issues.

## Version 112.0.1722.64: April 27, 2023

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 109.0.1518.100: April 24, 2023

> [!NOTE]
> This update was done for our M109 Windows down-level extended support. We're shipping 109 to Win 7, 8, and 8.1 (including Server 2012 R2 which is based on Win 8.1).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-24-2023).

## Version 112.0.1722.58: April 21, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-21-2023).

## Version 112.0.1722.48: April 14, 2023

> [!IMPORTANT]
> This update to Extended Stable contains a fix for [CVE-2023-2033](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2023-2033), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-14-2023).

## Version 112.0.1722.46: April 13, 2023

Fixed various bugs and performance issues.

## Version 112.0.1722.39: April 10, 2023

Fixed various bugs and performance issues.


<!-- from Version 112.0.1722.34: April 6, 2023 to Version 111.0.1661.43: March 15, 2023 -->
<!-- from Version 111.0.1661.41: March 13, 2023 to Version 110.0.1587.46: February 14, 2023 -->
<!-- from Version Version 110.0.1587.41: February 9, 2023 to Version 108.0.1462.83: January 12, 2023 -->
<!-- from Version 109.0.1518.49: January 12, 2023 to Version 108.0.1462.46: December 8, 2022 -->
<!-- from Version 108.0.1462.42: December 5, 2022 to Version 106.0.1370.59: October 27, 2022 -->
<!--- from Version 107.0.1418.24: October 27, 2022 to Version 106.0.1370.37: October 6, 2022 -->
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
