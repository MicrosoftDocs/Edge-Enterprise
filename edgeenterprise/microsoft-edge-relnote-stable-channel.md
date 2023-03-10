---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: collw
author: dan-wesley
manager: likuba
ms.date: 03/10/2023
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

## Version 111.0.xxxx.xx: March x, 2023

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

- **Enhanced security mode improvements.** Enhanced security mode now supports WebAssembly for macOS x64 and Linux x64. More cross-platform (ARM64) support is expected in the future. For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **New policy to clear IE mode data on browser exit.** The [InternetExplorerModeClearDataOnExitEnabled](/deployedge/microsoft-edge-policies#internetexplorermodecleardataonexitenabled) policy controls whether browsing history is deleted from Internet Explorer and Internet Explorer mode every time Microsoft Edge is closed. Users can also configure this setting in the 'Clear browsing data for Internet Explorer' option in the Privacy, search, and services menu of Settings (*edge://settings/privacy*).

### Policy updates

#### New policies

- [InternetExplorerModeClearDataOnExitEnabled](/DeployEdge/microsoft-edge-policies#internetexplorermodecleardataonexitenabled) - Clear history for IE and IE mode every time you exit
- [MouseGestureEnabled](/DeployEdge/microsoft-edge-policies#mousegestureenabled) - Mouse Gesture Enabled
- [PrintPreviewStickySettings](/DeployEdge/microsoft-edge-policies#printpreviewstickysettings) - Configure the sticky print preview settings

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

## Version 110.0.1587.41: February 9, 2023

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#february-9-2023).

### Feature updates

- **New Immersive Reader policies.** Immersive Reader in Microsoft Edge simplifies web page layouts, removes clutter, and helps you customize your reading experience. Using these new policies ([ImmersiveReaderGrammarToolsEnabled](/deployedge/microsoft-edge-policies#immersivereadergrammartoolsenabled) and [ImmersiveReaderPictureDictionaryEnabled](/deployedge/microsoft-edge-policies#immersivereaderpicturedictionaryenabled)), administrators can control the availability of Grammar Tools and Picture Dictionary features within Immersive Reader.

- **Enabling sync for Azure Active Directory signed in customers.** Microsoft Edge sync roams data across all signed in instances of Microsoft Edge. This data includes favorites, passwords, browsing history, open tabs, settings, apps, collections, and extensions.  For Azure Active Directory users who have sync turned off, after the browser is launched they'll see a notification prompt and have sync turned on for all signed in instances of Microsoft Edge. This sync enablement includes other devices where they're signed in. Additionally, if a user’s other devices don’t have history and open tabs sync on, those two toggles will be turned on. Organizations using the [SyncDisabled](/deployedge/microsoft-edge-policies#syncdisabled) policy won't be affected by this change.

- **Drop.** Microsoft Edge now offers a simple way to send files and notes across all your signed in mobile and desktop devices. Using the desktop version of Microsoft Edge, Drop can be managed through the sidebar (*edge://settings/sidebar*).  Administrators can control the availability of Drop using the [EdgeEDropEnabled](/deployedge/microsoft-edge-policies#edgeedropenabled) policy.

### Policy updates

#### New policies

- [AutofillMembershipsEnabled](/DeployEdge/microsoft-edge-policies#autofillmembershipsenabled) - Save and fill memberships
- [ImmersiveReaderGrammarToolsEnabled](/DeployEdge/microsoft-edge-policies#immersivereadergrammartoolsenabled) - Enable Grammar Tools feature within Immersive Reader in Microsoft Edge
- [ImmersiveReaderPictureDictionaryEnabled](/DeployEdge/microsoft-edge-policies#immersivereaderpicturedictionaryenabled) - Enable Picture Dictionary feature within Immersive Reader in Microsoft Edge
- [PrintPreviewStickySettings](/DeployEdge/microsoft-edge-policies#printpreviewstickysettings) - Configure the sticky print preview settings
- [SearchInSidebarEnabled](/DeployEdge/microsoft-edge-policies#searchinsidebarenabled) - Search in Sidebar enabled
- [WorkspacesNavigationSettings](/DeployEdge/microsoft-edge-policies#workspacesnavigationsettings) - Configure navigation settings per groups of URLs in Microsoft Edge Workspaces

#### Obsoleted policies

- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) - Specifies whether the display-capture permissions-policy is checked or skipped
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains
- [SetTimeoutWithout1MsClampEnabled](/DeployEdge/microsoft-edge-policies#settimeoutwithout1msclampenabled) - Control Javascript setTimeout() function minimum timeout
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) Configure ShadowStack crash rollback behavior

## Version 109.0.1518.78: February 2, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#february-2-2023).

## Version 109.0.1518.70: January 26, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-26-2023).

## Version 108.0.1462.95: January 26, 2023

Fixed various bugs and performance issues for Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-26-2023).

## Version 109.0.1518.69: January 25, 2023

Fixed various bugs and performance issues.

## Version 109.0.1518.61: January 19, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-19-2023).

## Version 108.0.1462.87: January 15, 2023

Fixed various bugs and performance issues for Extended Stable release.

## Version 109.0.1518.55: January 15, 2023

Fixed various bugs and performance issues.

## Version 109.0.1518.52: January 13, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-13-2023).

## Version 108.0.1462.83: January 12, 2023

Fixed various bugs and performance issues for Extended Stable release.

## Version 109.0.1518.49: January 12, 2023

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-12-2023).

### Feature updates

- **Account Linking between a personal Microsoft account (MSA) and Azure Active Directory (AAD) account.** Microsoft is enabling users to link a personal Microsoft account (MSA) and Azure Active Directory (AAD) account through work or school.  Once linked, users can earn Microsoft Rewards points for Microsoft Bing searches done in their browser or Windows search box while signed in with their work or school account. For more information, see the [Account Linking FAQ](https://support.microsoft.com/account-billing/account-linking-faq-c66effb9-02e6-49c0-89e1-ae4d8644e6f7) and the [Account Linking IT Admins FAQ](https://support.microsoft.com/account-billing/account-linking-it-admins-faq-72f0dc4e-b632-439e-b90c-347043a7b75a). Tenant admins can also control this feature in the Message Center section of the Microsoft 365 Admin Center or by using the [LinkedAccountEnabled](/deployedge/microsoft-edge-policies#linkedaccountenabled) policy.

- **TLS server certificate verification changes.** In Microsoft Edge version 111, the certificate trust list and the certificate verifier will be decoupled from the host operating system’s root store.  Instead, the default certificate trust list and the certificate verifier will be provided by and shipped with the browser.  The [MicrosoftRootStoreEnabled](/deployedge/microsoft-edge-policies#microsoftrootstoreenabled) policy is now available for testing to control when the built-in root store and certificate verifier are used.  Support for the policy is planned to be removed in Microsoft Edge version 113.  For more information, see [Changes to Microsoft Edge browser TLS server certificate verification | Microsoft Learn](/deployedge/microsoft-edge-security-cert-verification).  **Note:** This is a controlled feature rollout in Microsoft Edge version 109.  If you don't see this feature, check back as we continue our rollout.

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

- **Graph APIs for Cloud Site List Management.** New Graph APIs that allow IT admins in organizations to create, manage, and publish their site lists for IE mode in the cloud.  For more information, see [Use the Edge API in Microsoft Graph](/graph/api/resources/browser-edge-api-overview?view=graph-rest-beta&preserve-view=true).

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
