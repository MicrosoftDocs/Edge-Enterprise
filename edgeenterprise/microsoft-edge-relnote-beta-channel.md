---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: leahtu
author: dan-wesley
manager: collw
ms.date: 06/02/2023
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

## Version 115.0.1823.xx: June x, 2023

Fixed various bugs and performance issues.

### Feature update

- **Enhanced security mode improvements.** Enhanced security mode provides an extra layer of protection when browsing the web and visiting less familiar sites. Enhanced security mode is turned on by default to Balanced mode for x64 Windows, x64 macOS, x64 Linux, and ARM64 systems. **Note:** This feature is a controlled feature rollout in Microsoft Edge Beta 115. If you don't see this feature, check back as we continue our rollout.

  Also, administrators have 2 new policies to manage the Enhanced security mode user experience: [EnhanceSecurityModeIndicatorUIEnabled] and [EnhanceSecurityModeOptOutUXEnabled].  For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **Microsoft Edge management service.** Microsoft Edge management service is an area in the M365 admin center where admins can manage the Microsoft Edge browser. It is a simple and easy-to-manage experience. Admins will be able to configure all Microsoft Edge browser policies for their organization in a configuration profile and set-up the browser to use these settings. <!-- For more information, see [link to Dan's doc].--> **Note:** This experience is in public preview. We'll start rolling out this experience on June 5 and expect to finish the rollout by the end of that week. You'll need to set up a Targeted release to opt in and view this experience in the M365 admin center.

### Policy updates

#### New policies

## Version 114.0.1823.37: June 2, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.35: May 31, 2023

Fixed various bugs and performance issues.

### Feature update

- **Microsoft Edge Sync Favorites Recovery.** The Microsoft Edge Sync Favorites Recovery feature lets sync users restore any favorites that they lost or deleted within the last 14 days. Users can access this feature from either the Microsoft Edge favorites hub or the *edge://favorites* page. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

## Version 114.0.1823.30: May 26, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.24: May 22, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.18: May 15, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.11: May 9, 2023

### Feature update

- **(Preview) Microsoft Edge Workspaces.** Edge Workspaces gives customers a way to organize their browsing tasks into dedicated windows. Edge Workspaces lets users share a set of browser tabs so working groups can view the same websites and latest working files in one place and stay on the same page. Each Edge Workspace contains its own sets of tabs and favorites, created and curated by the user and their collaborators. Edge Workspaces are automatically saved and kept up to date. For more information about this public preview, see [Microsoft Edge Workspaces](/deployedge/microsoft-edge-workspaces).

- **Option to attach the Edge sidebar to the Windows desktop.**  Users of the Microsoft Edge sidebar will be able to access their apps and sites directly from their Windows desktop. As an opt-in experience, users can attach the sidebar to their Windows desktop by clicking a "popout" icon near the base of the sidebar in the browser. This enables a side-by-side experience that works with any Windows app—including Microsoft Edge itself. Users enjoy streamlined access to the same set of powerful AI tools and web-based services, including Bing Chat, without launching a browser window, enhancing productivity regardless of where they are in Windows. Administrators can control the availability using the [StandaloneHubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#standalonehubssidebarenabled).

- **Enhanced security mode on by default.** Enhanced security mode provides an extra layer of protection when browsing the web and visiting less familiar sites. Enhanced security mode is turned on by default for x64 Windows, x64 macOS, x64 Linux, and ARM64 systems. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

### Policy updates

#### New policies

- [StandaloneHubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#standalonehubssidebarenabled) - Standalone Sidebar Enabled
- [ShowDownloadsToolbarButton](/DeployEdge/microsoft-edge-policies#showdownloadstoolbarbutton) - Show Downloads button on the toolbar

#### Obsoleted policy

- [MicrosoftRootStoreEnabled](/DeployEdge/microsoft-edge-policies#microsoftrootstoreenabled) - Determines whether the Microsoft Root Store and built-in certificate verifier will be used to verify server certificates

#### Additional policy changes

- [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode) - BasicMode is deprecated
- [EdgeWorkspacesEnabled](/DeployEdge/microsoft-edge-policies#edgeworkspacesenabled) - If the policy isn't configured users are able to access the Microsoft Edge Workspaces feature

## Version 113.0.1774.35: May 5, 2023

Fixed various bugs and performance issues.

## Version 113.0.1774.32: May 4, 2023

### Feature update

- **Microsoft Edge PDF Share.** Users now have an easy option to share PDF documents as a link or attachment directly from the PDF toolbar.  **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

## Version 113.0.1774.27: May 1, 2023

Fixed various bugs and performance issues.

## Version 113.0.1774.23: April 25, 2023

Fixed various bugs and performance issues.

## Version 113.0.1774.15: April 18, 2023

Fixed various bugs and performance issues.

<!-- Version 113.0.1774.9: April 12, 2023 to Version 112.0.1722.15: March 21, 2023 -->
<!-- from Version 112.0.1722.11: March 17, 2023 to Version 111.0.1661.22: February 24, 2023 -->
<!-- from Version 111.0.1661.15: February 16, 2023 to Version 110.0.1587.22: January 24, 2023 -->
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
