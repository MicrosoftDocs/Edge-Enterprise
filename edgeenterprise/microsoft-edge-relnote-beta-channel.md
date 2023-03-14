---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: leahtu
author: dan-wesley
manager: collw
ms.date: 03/14/2023
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

## Version 112.0.xxxx.xx: March x, 2023

### Feature update

- **Microsoft Edge Sidebar Improvements.** The Microsoft Edge sidebar lets users access productivity tools side-by-side with their browsing window.  In this release, the sidebar has been enhanced to increase productivity and improve user experience.  As communicated in our last release ([Microsoft Edge release notes for Stable Channel](/deployedge/microsoft-edge-relnote-stable-channel#version-1110166141-march-13-2023)), the sidebar now includes a toolbar button by default to access the experience. If admins enable the Discover app, hovering and clicking the toolbar button will invoke both the sidebar tower and the new discover experience. With this release, admins now have the ability to disable the Discover app and still keep the Sidebar. In this situation, the Sidebar tower will be always be shown. If a user would like to hide their sidebar from always showing, they can do this in their Sidebar settings (*edge://settings/sidebar*). Additionally, Enterprise users can choose to 'always show' or 'auto hide', when an admin 'enables' the Sidebar. More customization options for the sidebar toolbar button are planned in future versions of Microsoft Edge.  For more information, see [Manage the sidebar in Microsoft Edge](/DeployEdge/microsoft-edge-sidebar).

- **Enhanced security mode improvements.** Enhanced security mode now supports WebAssembly (Wasm) for ARM64. Cross-platform support is now available for x64 Windows, x64 macOS, x64 Linux and ARM64 systems.  For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **Added features for web app policy.** The [WebAppInstallForceList](/deployedge/microsoft-edge-policies#webappinstallforcelist) policy lets administrators configure a list of web apps that install silently, without user interaction, and which users can't uninstall or turn off.  This policy now supports `custom_name`, which permanently overrides the app name of installed apps and `custom_icon`, which permanently overrides the app icon of installed apps.

### Policy updates

#### New policies

## Version 111.0.1661.41: March 13, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.39: March 10, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.38: March 9, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.37: March 8, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.34: March 6, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.30: March 3, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.27: March 2, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.24: February 27, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.22: February 24, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.15: February 16, 2023

### Feature update

- **Enhanced security mode improvements.** Enhanced security mode now supports WebAssembly for macOS x64 and Linux x64. More cross-platform (ARM64) support is expected in the future. For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **New policy to clear IE mode data on browser exit.** The [InternetExplorerModeClearDataOnExitEnabled](/deployedge/microsoft-edge-policies#internetexplorermodecleardataonexitenabled) policy controls whether browsing history is deleted from Internet Explorer and Internet Explorer mode every time Microsoft Edge is closed. Users can also configure this setting in the 'Clear browsing data for Internet Explorer' option in the Privacy, search, and services menu of Settings (*edge://settings/privacy*).

### Policy updates

#### New policies

- [InternetExplorerModeClearDataOnExitEnabled](/DeployEdge/microsoft-edge-policies#internetexplorermodecleardataonexitenabled) - Clear history for IE and IE mode every time you exit
- [MouseGestureEnabled](/DeployEdge/microsoft-edge-policies#mousegestureenabled) - Mouse Gesture Enabled
- [PrintPreviewStickySettings](/DeployEdge/microsoft-edge-policies#printpreviewstickysettings) - Configure the sticky print preview settings

## Version 110.0.1587.40: February 8, 2023

Fixed various bugs and performance issues.

## Version 110.0.1587.35: February 3, 2023

Fixed various bugs and performance issues.

## Version 110.0.1587.30: January 30, 2023

Fixed various bugs and performance issues.

## Version 110.0.1587.22: January 24, 2023

Fixed various bugs and performance issues.

<!---                   --->
<!--- from Version 110.0.1587.17: January 20, 2023 to Version 109.0.1518.23: December 14, 2022 -->
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
