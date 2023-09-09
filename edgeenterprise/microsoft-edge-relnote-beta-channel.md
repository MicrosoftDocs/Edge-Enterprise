---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 09/08/2023
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

## Version 117.0.2045.21: September 6, 2023

Fixed various bugs and performance issues.

## Version 117.0.2045.12: August 29, 2023

Fixed various bugs and performance issues.

### Announcement: Deprecating the unload event

The Google Chrome team plans to deprecate the unload event starting in Chrome version 117. The deprecation is done by gradually changing the default so unload handlers stop firing on pages unless a page explicitly opts in to re-enable them. For more information, see [Deprecating the unload event - Chrome Developers](https://developer.chrome.com/blog/deprecating-unload/), and [Google Groups - Conversations](https://groups.google.com/a/chromium.org/g/blink-dev/c/dvusqw9-IhI/m/SBkm_u1RAQAJ).

While we haven't yet finalized the deprecation schedule, we anticipate that Microsoft Edge  follows Chrome's schedule with a possible delay of a release or two. If you're interested in testing with Microsoft Edge starting in version 118, the **ForcePermissionPolicyUnloadDefaultEnabled** policy is available or you can use the instructions documented at [Disable unload handlers by default and add Permissions-Policy to opt-in to enabling them](https://github.com/fergald/docs/blob/master/explainers/permissions-policy-deprecate-unload.md#disable-unload-handlers-by-default-and-add-permissions-policy-to-opt-in-to-enabling-them).

WebView2 will support both the permissions policy and the enterprise policy but won't be impacted by the gradual rollout in Microsoft Edge. We expect WebView2 will switch defaults when the roll out reaches 100% of page loads.

## Version 117.0.2045.9: August 25, 2023

Fixed various bugs and performance issues.

### Feature updates

- **Microsoft Edge for Business update.** Microsoft Edge for Business is a dedicated Microsoft Edge experience built for work that enables admins in organizations to give their users a productive and secure work browser across managed and unmanaged devices.  The Automatic Switching mechanism is designed to keep work and personal browsing separate for the end users. This mechanism currently switches users from personal to work browsing on applicable logins. The new update automatically starts switching users from work to personal browsing on applicable logins. For more information, see [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business).

- **E-tree in Wallet.** Users signed into Microsoft Edge with a personal Microsoft Account (MSA) can grow a virtual seed into a tree with Wallet.  Once it's grown, a real mangrove is planted.  Administrators can control the availability using the [EdgeWalletEtreeEnabled](/deployedge/microsoft-edge-policies#edge-wallet-e-tree-enabled) policy. Note: This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Deprecation of features.** To improve end user experience and simplify the More tools menu, the following features are being deprecated: Math Solver, Picture Dictionary, Citations, Grammar Tools, and Kids Mode.

- **Deprecation of Web Select.** To improve end user experience, this feature is being deprecated and will no longer be an option under Web Capture or via keyboard shortcut.

### Policy updates

#### New policies

- [AllowSystemNotifications](/deployedge/microsoft-edge-policies#allowsystemnotifications) - Allows system notifications
- [EdgeWalletEtreeEnabled](/deployedge/microsoft-edge-policies#edgewalletetreeenabled) - Edge Wallet E-Tree Enabled
- [GamerModeEnabled](/deployedge/microsoft-edge-policies#gamermodeenabled) - Enable Gamer Mode
- [SearchbarAllowed](/deployedge/microsoft-edge-policies#searchbarallowed) - Enable the Search bar
- [SearchbarIsEnabledOnStartup](/deployedge/microsoft-edge-policies#searchbarisenabledonstartup) -Allow the Search bar at Windows startup
- [ShowHistoryThumbnails](/deployedge/microsoft-edge-policies#showhistorythumbnails) - Show thumbnail images for browsing history
- [UploadFromPhoneEnabled](/deployedge/microsoft-edge-policies#uploadfromphoneenabled) - Enable upload files from phone in Microsoft Edge desktop

#### Obsoleted policy

- [WebSelectEnabled](/deployedge/microsoft-edge-policies#webselectenabled) - Web Select Enabled

## Version 116.0.1938.54: August 18, 2023

Fixed various bugs and performance issues.

## Version 116.0.1938.51: August 16, 2023

Fixed various bugs and performance issues.

## Version 116.0.1938.43: August 9, 2023

Fixed various bugs and performance issues.

## Version 116.0.1938.36: July 31, 2023

Fixed various bugs and performance issues.
<!-- Version 116.0.1938.29: July 24, 2023 to Version 115.0.1901.9: June 15, 2023 -->
<!-- from Version 115.0.1901.7: June 13, 2023 to Version 114.0.1823.18: May 15, 2023 -->
<!-- Version 114.0.1823.11: May 9, 2023 to Version 113.0.1774.15: April 18, 2023 -->
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
