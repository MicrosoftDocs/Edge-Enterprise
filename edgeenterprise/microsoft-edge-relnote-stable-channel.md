---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 11/02/2023
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

## Version 119.0.2151.44: November 2, 2023

Fixed various bugs and performance issues.
<!---
Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#november-2-2023). -->

### Feature updates

- **Compression Dictionary Transport support.** A version of the [Compression Dictionary Transport](https://datatracker.ietf.org/doc/draft-ietf-httpbis-compression-dictionary/) feature is available for sites to use by participating in the associated origin trial. If your network uses a middlebox that inspects network traffic and/or you previously encountered issues with the ZSDCH feature, review the [Considerations for zstd-based Shared Dictionary Compression for HTTP](/DeployEdge/learnmore-zsdch-compression) page which contains updated guidance.

- **Behavioral changes to the beforeunload event.** The behavior of the beforeunload event has changed such that calling preventDefault in a beforeunload event handler triggers a confirmation dialog. Setting returnValue to an empty string in a beforeunload event handler no longer triggers a confirmation dialog. This behavior takes effect starting in Microsoft Edge version 119. Administrators can temporarily opt out of this functionality by disabling the [BeforeunloadEventCancelByPreventDefaultEnabled](/deployedge/microsoft-edge-policies#beforeunloadeventcancelbypreventdefaultenabled) policy.

- **Split screen restore improvements.** Split screen allows you to simultaneously work on multiple tasks across two, side-by-side screens in one browsing tab to boost your productivity and multitask more efficiently. Now after the browser is restarted and the previous session is restored, the split tab will also be restored. 

- **Additional capability to manage sidebar apps.** Administrators can utilize the "sidebar_auto_open_blocked" [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) policy field to control the auto-open behavior of sidebar apps.  For more information, see [Detailed guide to the ExtensionSettings](/deployedge/microsoft-edge-manage-extensions-ref-guide) policy.

- **Updates to Microsoft Edge enterprise sync settings page.** When the [ForceSyncTypes](/deployedge/microsoft-edge-policies#forcesynctypes) and [SyncTypesListDisabled](/deployedge/microsoft-edge-policies#synctypeslistdisabled) polices are used concurrently, the sync settings page (`edge://settings/profiles/sync`) accurately show the status for each data type.

### Policy updates

#### New policies

- [SwitchIntranetSitesToWorkProfile](/deployedge/microsoft-edge-policies#switchintranetsitestoworkprofile) - Switch intranet sites to a work profile
- [SwitchSitesOnIEModeSiteListToWorkProfile](/deployedge/microsoft-edge-policies#switchsitesoniemodesitelisttoworkprofile) - Switch sites on the IE mode site list to a work profile
- [OrganizationalBrandingOnWorkProfileUIEnabled](/deployedge/microsoft-edge-policies#organizationalbrandingonworkprofileuienabled) - Allow the use of your organization's branding assets from M365 on the profile-related UI of a work profile

## Version 118.0.2088.88: November 2, 2023

Fixed various bugs and performance issues for Extended Stable release.

## Version 118.0.2088.76: October 27, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-27-2023).

## Version 118.0.2088.69: October 24, 2023

Fixed various bugs and performance issues.

### Feature updates

- **Designer (Preview) in the Microsoft Edge sidebar.**  All Microsoft Edge users with Manifest version 4.8.5 or higher (users can see their version using `edge://sidebar-internals`), including those that are working on managed devices, can now add the Designer (Preview) app to the Edge sidebar by clicking on the "**+**" and setting the Designer (Preview) toggle to on. Designer (Preview) allows you to experience the generative AI capabilities offered by Microsoft Designer [https://designer.microsoft.com](https://designer.microsoft.com) from inside the Edge browser.

  Designer is a new AI system from Microsoft that generates visual, customizable designs based on your text description and images. This release will be available in English for the following country/regions: Australia, India, New Zealand, South Africa, and the United States.

  Administrators can manage sidebar apps including Designer (Preview) icon by using the policies described in [Manage the sidebar in Microsoft Edge](/deployedge/microsoft-edge-sidebar). The ID for Designer (Preview) app is 2cb2db96-3bd0-403e-abe2-9269b3761041.

## Version 118.0.2088.61: October 20, 2023

Fixed various bugs and performance issues.

## Version 118.0.2088.57: October 18, 2023

Fixed various bugs and performance issues.

### Feature updates

- **Icon change in Edge sidebar.**  The Bing icon entry point in the Microsoft Edge sidebar has been changed to the new Copilot icon. No other changes in this experience are expected.

## Version 118.0.2088.46: October 13, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-13-2023).

### Announcement: Icon change in Edge sidebar

In an upcoming update to Microsoft Edge, the Bing icon entry point in the Microsoft Edge sidebar will change to the new Copilot icon. No other changes in the experience are expected.

### Feature updates

- **Microsoft Edge for Business Banner.**  Microsoft Edge for Business is a dedicated Microsoft Edge experience built for work that enables admins in organizations to give their users a productive and secure work browser across managed and unmanaged devices. The in-product Microsoft Edge for Business banner is being deprecated and will no longer be visible.

- **Find on page.** Searching for a word or phrase on a webpage has become easier with the new smart find update to Find on page. For more information, see
[Find on page](https://www.microsoft.com/edge/features/find-on-page?form=MT00D8). Now when you search with Find on page, we suggest related matches and synonyms making it effortless to find what you're looking for, even if you misspell a word in your search query. When you search, simply select the suggested word to quickly locate the desired word or phrase on the page. Data is sent to Microsoft for processing.  For more information, see [Microsoft Edge's Privacy Whitepaper](/microsoft-edge/privacy-whitepaper/). Administrators can control the availability using the [RelatedMatchesCloudServiceEnabled](/deployedge/microsoft-edge-policies#relatedmatchescloudserviceenabled) policy.

- **New SmartScreen policy.**  The [ExemptSmartScreenDownloadWarnings](/deployedge/microsoft-edge-policies#exemptsmartscreendownloadwarnings) policy lets administrators create a dictionary of file type extensions with a corresponding list of domains that are exempted from SmartScreen AppRep warnings.  Files with file type extensions specified for domains identified by this policy are still subject to file type extension-based security warnings and mixed-content download warnings.

- **New Microsoft Edge Update policies.** The **MeteredUpdatesDefault** and **MeteredUpdates** policies allows administrators to control the "Download Updates over metered connections" setting (`edge://settings/help`). The **MeteredUpdatesDefault** applies to all apps and **MeteredUpdates** applies to targeted apps. When a policy is configured to Allow, updates occur on a metered connection, such as cellular connections or others where data usage is controlled.

### Policy updates

#### New policies

- [BeforeunloadEventCancelByPreventDefaultEnabled](/deployedge/microsoft-edge-policies#beforeunloadeventcancelbypreventdefaultenabled) - Control the behavior for the cancel dialog produced by the beforeunload event
- [CompressionDictionaryTransportEnabled](/deployedge/microsoft-edge-policies#compressiondictionarytransportenabled) - Enable compression dictionary transport support
- [DataUrlInSvgUseEnabled](/deployedge/microsoft-edge-policies#dataurlinsvguseenabled) - Data URL support for SVGUseElement
- [ExemptSmartScreenDownloadWarnings](/deployedge/microsoft-edge-policies#exemptsmartscreendownloadwarnings) - Disable SmartScreen AppRep based warnings for specified file types on specified domains
- [ForceBuiltInPushMessagingClient](/deployedge/microsoft-edge-policies#forcebuiltinpushmessagingclient) - Forces Microsoft Edge to use its built-in WNS push client to connect to the Windows Push Notification Service
- [ForcePermissionPolicyUnloadDefaultEnabled](/deployedge/microsoft-edge-policies#forcepermissionpolicyunloaddefaultenabled) - Controls whether unload event handlers can be disabled
- [PictureInPictureOverlayEnabled](/deployedge/microsoft-edge-policies#pictureinpictureoverlayenabled) - Enable Picture in Picture overlay feature on supported webpages in Microsoft Edge
- [SendMouseEventsDisabledFormControlsEnabled](/deployedge/microsoft-edge-policies#sendmouseeventsdisabledformcontrolsenabled) - Control the new behavior for event dispatching on disabled form controls

#### Deprecated policies

- [RendererCodeIntegrityEnabled](/deployedge/microsoft-edge-policies#renderercodeintegrityenabled) - Enable renderer code integrity

## Version 117.0.2045.60: October 6, 2023

Fixed various bugs and performance issues.

## Version 117.0.2045.55: October 4, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-4-2023).

## Version 117.0.2045.47: September 29, 2023

Fixed various bugs and performance issues.

> [!IMPORTANT]
> This update to Stable channel contains a fix for [CVE-2023-5217](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2023-5217), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-29-2023).

## Version 116.0.1938.98: September 29, 2023

Fixed various bugs and performance issues.

> [!IMPORTANT]
> This update to Extended Stable channel contains a fix for [CVE-2023-5217](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2023-5217), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-29-2023).

## Version 117.0.2045.43: September 25, 2023

Fixed various bugs and performance issues.

## Version 117.0.2045.41: September 23, 2023

Fixed various bugs and performance issues.

## Version 117.0.2045.40: September 22, 2023

Fixed various bugs and performance issues.

## Version 117.0.2045.36: September 19, 2023

Fixed various bugs and performance issues.

## Version 117.0.2045.35: September 19, 2023

Fixed various bugs and performance issues.

## Version 109.0.1518.140: September 15, 2023

> [!NOTE]
> This update was done for our M109 Windows down-level extended support. We're shipping 109 to Win 7, 8, and 8.1 (including Server 2012 R2 which is based on Win 8.1).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-15-2023).

<!-- from Version 117.0.2045.31: September 15, 2023 to Version 116.0.1938.62: August 25, 2023 -->
<!-- from Version 116.0.1938.54: August 21, 2023 to Version 114.0.1823.41: June 6, 2023 -->
<!-- from Version 114.0.1823.37: June 2, 2023 to Version 112.0.1722.77: May 9, 2023 -->
<!-- from Version 113.0.1774.35: May 5, 2023 to Version 112.0.1722.39: April 10, 2023 -->
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
