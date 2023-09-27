---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 09/27/2023
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

## Version 118.0.2088.17: September 25, 2023

Fixed various bugs and performance issues.

## Version 118.0.2088.11: September 20, 2023

Fixed various bugs and performance issues.

### Feature updates

- **Microsoft Edge for Business Banner.**  Microsoft Edge for Business is a dedicated Microsoft Edge experience built for work that enables admins in organizations to give their users a productive and secure work browser across managed and unmanaged devices. The in-product Microsoft Edge for Business banner is being deprecated and will no longer be visible.

- **Find on page.** Searching for a word or phrase on a webpage has become easier with the new smart find update to Find on page. For more information, see
[Find on page](https://www.microsoft.com/edge/features/find-on-page?form=MT00D8). Now when you search with Find on page, we suggest related matches and synonyms making it effortless to find what you're looking for, even if you misspell a word in your search query. When you search, simply select the suggested word to quickly locate the desired word or phrase on the page. Data is sent to Microsoft for processing.  For more information, see [Microsoft Edge's Privacy Whitepaper](/microsoft-edge/privacy-whitepaper/). Administrators can control the availability using the [RelatedMatchesCloudServiceEnabled](/deployedge/microsoft-edge-policies#relatedmatchescloudserviceenabled) policy.

- **New SmartScreen policy.**  The [ExemptSmartScreenDownloadWarnings](/deployedge/microsoft-edge-policies#exemptsmartscreendownloadwarnings) policy lets administrators create a dictionary of file type extensions with a corresponding list of domains that will be exempted from SmartScreen AppRep warnings.  Files with file type extensions specified for domains identified by this policy will still be subject to file type extension-based security warnings and mixed-content download warnings.

- **New Microsoft Edge Update policies.** The **MeteredUpdatesDefault** and **MeteredUpdates** policies allows administrators to control the "Download Updates over metered connections" setting (`edge://settings/help`). The **MeteredUpdatesDefault** applies to all apps and **MeteredUpdates** applies to targeted apps. When a policy is configured to Allow, updates occur on a metered connection, such as cellular connections or others where data usage is controlled.

### Policy updates

#### New policies

- [CompressionDictionaryTransportEnabled](/deployedge/microsoft-edge-policies#compressiondictionarytransportenabled) -Enable compression dictionary transport support
- [DataUrlInSvgUseEnabled](/deployedge/microsoft-edge-policies#dataurlinsvguseenabled) - Data URL support for SVGUseElement
- [ExemptSmartScreenDownloadWarnings](/deployedge/microsoft-edge-policies#exemptsmartscreendownloadwarnings) - Disable SmartScreen AppRep based warnings for specified file types on specified domains
- [ForcePermissionPolicyUnloadDefaultEnabled](/deployedge/microsoft-edge-policies#forcepermissionpolicyunloaddefaultenabled) - Controls whether unload event handlers can be disabled
- [PictureInPictureOverlayEnabled](/deployedge/microsoft-edge-policies#pictureinpictureoverlayenabled) - Enable Picture in Picture overlay feature on supported webpages in Microsoft Edge

## Version 117.0.2045.31: September 15, 2023

Fixed various bugs and performance issues.

## Version 117.0.2045.30: September 14, 2023

Fixed various bugs and performance issues.

## Version 117.0.2045.27: September 12, 2023

Fixed various bugs and performance issues.

## Version 117.0.2045.21: September 6, 2023

Fixed various bugs and performance issues.

## Version 117.0.2045.12: August 29, 2023

Fixed various bugs and performance issues.

### Announcement: Deprecating the unload event

The Google Chrome team plans to deprecate the unload event starting in Chrome version 117. The deprecation is done by gradually changing the default so unload handlers stop firing on pages unless a page explicitly opts in to re-enable them. For more information, see [Deprecating the unload event - Chrome Developers](https://developer.chrome.com/blog/deprecating-unload/), and [Google Groups - Conversations](https://groups.google.com/a/chromium.org/g/blink-dev/c/dvusqw9-IhI/m/SBkm_u1RAQAJ).

While we haven't yet finalized the deprecation schedule, we anticipate that Microsoft Edge  follows Chrome's schedule with a possible delay of a release or two. If you're interested in testing with Microsoft Edge starting in version 118, the **ForcePermissionPolicyUnloadDefaultEnabled** policy is available or you can use the instructions documented at [Disable unload handlers by default and add Permissions-Policy to opt-in to enabling them](https://github.com/fergald/docs/blob/master/explainers/permissions-policy-deprecate-unload.md#disable-unload-handlers-by-default-and-add-permissions-policy-to-opt-in-to-enabling-them).

WebView2 supports both the permissions policy and the enterprise policy but won't be impacted by the gradual rollout in Microsoft Edge. We expect WebView2 will switch defaults when the roll out reaches 100% of page loads.

<!-- Version 117.0.2045.9: August 25, 2023 to Version 116.0.1938.36: July 31, 2023 -->
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
