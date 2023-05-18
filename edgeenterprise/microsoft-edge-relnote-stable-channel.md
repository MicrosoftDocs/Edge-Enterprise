---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: collw
author: dan-wesley
manager: likuba
ms.date: 05/18/2023
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

## Version 112.0.1722.84: May 18, 2023

Fixed various bugs and performance issues for Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-18-2023).

## Version 113.0.1774.50: May 18, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-18-2023).

## Version 113.0.1774.42: May 11, 2023

Fixed various bugs and performance issues.

## Version 112.0.1722.77: May 9, 2023

Fixed various bugs and performance issues for Extended Stable release.

## Version 113.0.1774.35: May 5, 2023

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-5-2023).

### Feature update

- **Improvements to downloads security.**Microsoft Edge now has the capability to scan archives (.zip, .rar, .7z) for any malwares using Microsoft Defender SmartScreen. This functionality is currently available on Windows only and provides extra protection where known malwares were being distributed within these archives.

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

## Version 112.0.1722.34: April 6, 2023

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-6-2023).

### Feature update

- **Enhanced security mode improvements.** Enhanced security mode now supports WebAssembly for ARM64. Cross-platform support is now available for x64 Windows, x64 macOS, x64 Linux and ARM64 systems. For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **Added features for web app policy.** The [WebAppInstallForceList](/deployedge/microsoft-edge-policies#webappinstallforcelist) policy lets administrators configure a list of web apps that install silently, without user interaction, and which users can't uninstall or turn off. This policy now supports custom_name, which permanently overrides the app name of installed apps and custom_icon, which permanently overrides the app icon of installed apps.

- **In-browser JSON viewer.**  Improvements to how JSON files are displayed in the browser, which includes a color-coded tree view with line numbers and the ability to collapse and expand the data.  This functionality will trigger automatically when the browser navigates to a JSON file on the web or the user opens a local one.  Additional features and enhancements will roll out as available.  For more information, see [View formatted JSON - Microsoft Edge Development](/microsoft-edge/devtools-guide-chromium/json-viewer/json-viewer).  Note: This is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout or you can navigate to `edge://flags` and search for JSON Viewer to manually enable.  

- **Updated new tab page policy.** The [NewTabPageHideDefaultTopSites](/deployedge/microsoft-edge-policies#newtabpagehidedefaulttopsites) policy hides the default top sites from the new tab page in Microsoft Edge. Starting on March 20th, when the policy is enabled it will also remove sponsored quick links from the new tab page.

- **Edit and save web images in Microsoft Edge.** You can right click on the desired web image and without leaving your browser window, crop, adjust lighting and color, and add filters. From there, you can save the edited image for later use. You can also start editing simply by hovering over an image and selecting edit image from the menu.

### Policy updates

#### New policies

- [CryptoWalletEnabled](/DeployEdge/microsoft-edge-policies#cryptowalletenabled) - Enable CryptoWallet feature

## Version 111.0.1661.62: March 30, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.54: March 24, 2023

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-24-2023).

### Feature update

- **New Microsoft Edge PDF experience policy.**  As part of the Adobe and Microsoft collaboration to re-envision the future workplace and your digital experiences, we are natively embedding the Adobe Acrobat PDF engine into the Microsoft Edge built-in PDF reader, with a release scheduled in March 2023. Administrators can start testing the new Microsoft Edge PDF reader which is powered by the Adobe Acrobat PDF engine by enabling the [NewPDFReaderEnabled](/deployedge/microsoft-edge-policies#newpdfreaderenabled) policy.  For more information, see [Microsoft Edge and Adobe partner to improve the PDF experience](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/microsoft-edge-and-adobe-partner-to-improve-the-pdf-experience/ba-p/3733481).  

- **Microsoft Edge Sidebar Improvements.** The Microsoft Edge sidebar lets users access productivity tools side-by-side with their browsing window. In this release, the sidebar has been enhanced to increase productivity and improve user experience. As communicated in our last release ([Microsoft Edge release notes for Stable Channel](/deployedge/microsoft-edge-relnote-stable-channel#version-1110166141-march-13-2023)), the sidebar now includes a toolbar button by default to access the experience. If admins enable the Discover app, hovering and clicking the toolbar button will invoke both the sidebar tower, and the new discover experience.

   With this release, admins now have the ability to disable the Discover app and still keep the Sidebar. In this situation, the Sidebar tower will always be shown. If an Admin chooses to enable the Sidebar but disable the Discover experience, the Sidebar can only be always shown or completely hidden. This default visibility can be changed in the Sidebar settings (*edge://settings/sidebar*).
 
   When an admin enables the Sidebar and the Discover experience, enterprise users can choose to 'always show' or 'auto hide'. More customization options for the sidebar toolbar button are planned in future versions of Microsoft Edge.  For more information, see [Manage the sidebar in Microsoft Edge](/DeployEdge/microsoft-edge-sidebar).

## Version 109.0.1518.95: March 23, 2023

> [!NOTE]
> This update was done for our M109 Windows down-level extended support.  We're shipping 109 to Win 7, 8, and 8.1 (including Server 2012 R2 which is based on Win 8.1).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-23-2023).

## Version 110.0.1587.78: March 23, 2023

Fixed various bugs and performance issues for Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-23-2023).

## Version 111.0.1661.51: March 21, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.44: March 16, 2023

### Policy updates

#### New policies

- [ShowAcrobatSubscriptionButton](/deployedge/microsoft-edge-policies#showacrobatsubscriptionbutton) - Shows button on native PDF viewer in Microsoft Edge that allows users to sign up for Adobe Acrobat subscription
- [NewPDFReaderEnabled](/DeployEdge/microsoft-edge-policies#newpdfreaderenabled) - Microsoft Edge built-in PDF reader powered by Adobe Acrobat enabled

## Version 111.0.1661.43: March 15, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.41: March 13, 2023

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-13-2023).

### Feature update

- **A New Microsoft Edge Sidebar.** In this release, the Sidebar introduces several new features and improvements aimed at enhancing productivity, convenience, and the user experience. Here are some of the highlights:<br><br>

  - **The New Discover:** Edge Copilot is a powerful tool that helps users boost their productivity and efficiency. It provides intelligent suggestions and insights based on the context of the web page and the user's goals. As the new Bing icon in the Toolbar, Edge Copilot helps users compose better emails, search the web faster, learn new skills, all done more conveniently.  
  - **Enhanced Sidebar Visibility:** With the new Auto-Hide functionality, a user can maximize the productivity and convenience of the sidebar without sacrificing valuable screen space. The Edge Sidebar can be hidden when a user isn't using it and it only reappears when a user needs it.  
  - **Evolved Sidebar Interaction:** The new Hover functionality lets users open the Sidebar by hovering on the Bing icon in the Toolbar. This enhances user productivity and convenience by providing a seamless and intuitive way to access their most used tools.  

  Admins retain the ability to control and customize the Sidebar and its experiences, as needed by using the following settings:<br><br>

  - If admins enable the Sidebar, users will have access to the Sidebar and Edge Copilot experience. The Sidebar will show at all times in the browser frame. Clicking on the Bing icon in the Toolbar will invoke the new Discover experience.
  - If admins choose the 'not configured' setting, users will have access to the Sidebar and Edge Copilot experience. Unlike when the Sidebar is 'enabled', their users will have the ability to always-show or auto-hide the Sidebar.
  - If admins disable the Sidebar, Discover and the Sidebar will be inaccessible for their users. **Note:** In this release, Admins do not have the ability to disable Discover and keep the Sidebar.

  Additional customization options for the sidebar toolbar button are planned in future versions of Microsoft Edge.

  For more information, see [Manage the sidebar in Microsoft Edge](/DeployEdge/microsoft-edge-sidebar) and [Microsoft Privacy Statement (Search, Microsoft Edge, and artificial intelligence)](https://privacy.microsoft.com/privacystatement).

- **Microsoft Feed on Microsoft 365 Edge New Tab Page.** We're rolling out a new experience to the Microsoft 365 tab of the Edge Enterprise New Tab Page. This experience will feature a new layout that centers on a larger version of the Microsoft Feed, featuring more productivity content, and moves the productivity cards including Important Emails, Recent SharePoint sites, Upcoming events, and To Do to the right-hand side of the Microsoft 365 tab.

- **Enhanced security mode improvements.** Enhanced security mode now supports WebAssembly for macOS x64 and Linux x64. More cross-platform (ARM64) support is expected in the future. For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **New policy to clear IE mode data on browser exit.** The [InternetExplorerModeClearDataOnExitEnabled](/deployedge/microsoft-edge-policies#internetexplorermodecleardataonexitenabled) policy controls whether browsing history is deleted from Internet Explorer and Internet Explorer mode every time Microsoft Edge is closed. Users can also configure this setting in the 'Clear browsing data for Internet Explorer' option in the Privacy, search, and services menu of Settings (*edge://settings/privacy*).

### Policy updates

#### New policies

- [InternetExplorerModeClearDataOnExitEnabled](/DeployEdge/microsoft-edge-policies#internetexplorermodecleardataonexitenabled) - Clear history for IE and IE mode every time you exit
- [MouseGestureEnabled](/DeployEdge/microsoft-edge-policies#mousegestureenabled) - Mouse Gesture Enabled
- [PrintPreviewStickySettings](/DeployEdge/microsoft-edge-policies#printpreviewstickysettings) - Configure the sticky print preview settings

## Version 110.0.1587.69: March 9, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-13-2023).

## Version 110.0.1587.63: March 3, 2023

Fixed various bugs and performance issues.

## Version 110.0.1587.57: February 25, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#february-25-2023).

## Version 110.0.1587.56: February 23, 2023

Fixed various bugs and performance issues.

## Version 110.0.1587.50: February 17, 2023

Fixed various bugs and performance issues.

## Version 110.0.1587.49: February 16, 2023

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 110.0.1587.46: February 14, 2023

Fixed various bugs and performance issues.

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
