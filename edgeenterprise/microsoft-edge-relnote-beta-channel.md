---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 01/19/2023
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

## Version 110.0.0000.00: January 00, 2023

### Feature update

- **New Immersive Reader policies.**  Immersive Reader in Microsoft Edge simplifies web page layouts, removes clutter, and helps you customize your reading experience.  Using these new policies ([ImmersiveReaderGrammarToolsEnabled](/deployedge/microsoft-edge-policies#enable-grammar-tools-feature-within-immersive-reader-in-microsoft-edge) and [ImmersiveReaderPictureDictionaryEnabled](/deployedge/microsoft-edge-policies#enable-picture-dictionary-feature-within-immersive-reader-in-microsoft-edge)), administrators can control the availability of Grammar Tools and Picture Dictionary features within Immersive Reader.

- **Enabling sync for Azure Active Directory signed in customers.**  Microsoft Edge sync roams data across all signed in instances of Microsoft Edge. This data includes favorites, passwords, browsing history, open tabs, settings, apps, collections, and extensions.  For Azure Active Directory users who have sync turned off, after the browser is launched they will see a notification prompt and have sync turned on for all signed in instances of Microsoft Edge. This sync enablement includes other devices where they are signed in.  Additionally, if a user’s other devices don’t have history and open tabs sync on, those two toggles will be turned on.  Organizations using the [SyncDisabled](/deployedge/microsoft-edge-policies#syncdisabled) policy will not be affected by this change.

- **In-browser JSON viewer.**  Improvements to how JSON files are displayed in the browser include a color-coded tree view with line numbers and the ability to collapse and expand the data.  This functionality will trigger automatically when the browser navigates to a JSON file on the web or the user opens a local file.  Additional features and enhancements will roll out when they are available.  For more information and to provide feedback, visit [DevTools: In-browser JSON viewer](https://microsoftedge.github.io/DevTools/explainers/JSONViewer/explainer).

- **Split Screen.** This feature lets you browse faster with side by side tabs. Boost your productivity with two tabs side-by-side in one browser window. With split screen you can multitask without losing focus.  Users can access Split Screen by clicking the toolbar icon or by selecting "Open link in split window" in the context menu.  **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

### Policy updates

#### New policies

- [ImmersiveReaderGrammarToolsEnabled](/DeployEdge/microsoft-edge-policies#immersivereadergrammartoolsenabled) - Enable Grammar Tools feature within Immersive Reader in Microsoft Edge
- [ImmersiveReaderPictureDictionaryEnabled](/DeployEdge/microsoft-edge-policies#immersivereaderpicturedictionaryenabled) - Enable Picture Dictionary feature within Immersive Reader in Microsoft Edge
- [PrintPreviewStickySettings](/DeployEdge/microsoft-edge-policies#printpreviewstickysettings) - Configure the sticky print preview settings
- [SearchInSidebarEnabled](/DeployEdge/microsoft-edge-policies#searchinsidebarenabled) - Search in Sidebar enabled
- [WorkspacesNavigationSettings](/DeployEdge/microsoft-edge-policies#workspacesnavigationsettings) - Configure navigation settings per groups of URLs in Microsoft Edge Workspaces

#### Obsoleted policies

- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) - Specifies whether the display-capture permissions-policy is checked or skipped
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains
- [SetTimeoutWithout1MsClampEnabled](/DeployEdge/microsoft-edge-policies#settimeoutwithout1msclampenabled) - Control Javascript setTimeout() function minimum timeout
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) - Configure ShadowStack crash rollback behavior

## Version 109.0.1518.55: January 15, 2023

Fixed various bugs and performance issues.

## Version 109.0.1518.52: January 13, 2023

Fixed various bugs and performance issues.

## Version 109.0.1518.49: January 11, 2023

Fixed various bugs and performance issues.

## Version 109.0.1518.44: January 6, 2023

Fixed various bugs and performance issues.

## Version 109.0.1518.26: December 20, 2022

Fixed various bugs and performance issues.

## Version 109.0.1518.23: December 14, 2022

Fixed various bugs and performance issues.

<!---                   --->
<!--- from Version 109.0.1518.14: December 7, 2022 to Version 108.0.1462.20: November 14, 2022 -->
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
