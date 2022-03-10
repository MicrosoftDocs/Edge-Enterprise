---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 03/10/2022
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

## Version 100.0.1185.X: March 10

### Feature updates

- **Improvements to the Cloud Site List Management experience for IE Mode.** Identify gaps in your enterprise site list by configuring reporting of site feedback with the [InternetExplorerIntegrationCloudUserSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) and [InternetExplorerIntegrationCloudNeutralSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) policies. You can view local site list URLs from users and potentially misconfigured neutral site URLs in the Microsoft Edge site lists experience in the Microsoft 365 Admin Center. To learn more, see [View site feedback on the Microsoft 365 Admin Center](/deployedge/edge-ie-mode-cloud-site-list-mgmt#view-site-feedback-on-the-microsoft-365-admin-center-1).  **Note:** This is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Preview PDF files in Microsoft Outlook and File Explorer.** Users can view a PDF file in a lightweight and rich read-only preview.  Available for Outlook Desktop PDF attachments or for local PDF files using File Explorer.  

- **Installed web app synchronization across all desktop devices.** Websites or Progressive Web Apps (PWAs) that have been installed as applications will synchronize across all desktop devices that you've signed into and enabled sync on. They'll show as "Available apps" for you to install. An app removed from one device will sync the removal on all devices.

### Policy updates

#### New Policies

- [AdsTransparencyEnabled](/DeployEdge/microsoft-edge-policies#adstransparencyenabled) - Configure if the ads transparency feature is enabled
- [ControlDefaultStateOfAllowExtensionFromOtherStoresSettingEnabled](/DeployEdge/microsoft-edge-policies#controldefaultstateofallowextensionfromotherstoressettingenabled) - Configure default state of Allow extensions from other stores setting
- [DefaultWebHidGuardSetting](/DeployEdge/microsoft-edge-policies#defaultwebhidguardsetting) - Control use of the WebHID API
- [EdgeAssetDeliveryServiceEnabled](/DeployEdge/microsoft-edge-policies#edgeassetdeliveryserviceenabled) - Allow features to download assets from the Asset Delivery Service
- [HideRestoreDialogEnabled](/DeployEdge/microsoft-edge-policies#hiderestoredialogenabled) - Hide restore pages dialog after browser crash
- [PDFSecureMode](/DeployEdge/microsoft-edge-policies#pdfsecuremode) - Secure mode and Certificate-based Digital Signature validation in native PDF reader
- [PromptOnMultipleMatchingCertificates](/DeployEdge/microsoft-edge-policies#promptonmultiplematchingcertificates) - Prompt the user to select a certificate when multiple certificates match
- [WebHidAskForUrls](/DeployEdge/microsoft-edge-policies#webhidaskforurls) - Allow the WebHID API on these sites
- [WebHidBlockedForUrls](/DeployEdge/microsoft-edge-policies#webhidblockedforurls) - Block the WebHID API on these sites

#### Deprecated Policy

- [BackgroundTemplateListUpdatesEnabled](/DeployEdge/microsoft-edge-policies#backgroundtemplatelistupdatesenabled) - Enables background updates to the list of available templates for Collections and other features that use templates

#### Obsoleted Policy

- [AllowSyncXHRInPageDismissal](/DeployEdge/microsoft-edge-policies#allowsyncxhrinpagedismissal) - Allow pages to send synchronous XHR requests during page dismissal

## Version 99.0.1150.30: March 2

Fixed various bugs and performance issues.

## Version 99.0.1150.25: February 25

Fixed various bugs and performance issues.

## Version 99.0.1150.21: February 22

Fixed various bugs and performance issues.

## Version 99.0.1150.16: February 14

Fixed various bugs and performance issues.

## Version 99.0.1150.11: February 9

### Feature updates

- **Upcoming three-digit version number in user agent string.** Starting with version 100, Microsoft Edge will send a three-digit version number in the User-Agent header, for example "Edg/100". Starting with Microsoft Edge 97, site owners can test this upcoming agent string by enabling the **#force-major-version-to-100** experiment flag in *edge://flags* to ensure their User-Agent parsing logic is robust and works as expected.

- **Personalize multi-profile experiences with profile preferences for sites.** Users can personalize their multi-profile experience with the ability to create a customized list of sites for automatic profile switching in Microsoft Edge.

- **Bidirectional Cookie Sharing for IE mode.** This feature expands on the cookie sharing capability already available and lets users sync specific session cookies from Internet Explorer/IE mode to Microsoft Edge. For more information, see [Cookie sharing between Microsoft Edge and Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

- **Navigate PDF documents using page thumbnails.** You will now be able to navigate through your PDF document using thumbnails that represent the pages. These thumbnails will appear in the pane on the left side of the PDF reader.

- **Configure the list of domains for which the password manager User Interface (UI) for Save and Fill will be disabled.** Use the [PasswordManagerBlocklist](/deployedge/microsoft-edge-policies#passwordmanagerblocklist) policy to configure the list of domains (HTTP/HTTPS schemas and hostnames only) where Microsoft Edge should disable the password manager. This means that Save and Fill workflows will be disabled, which ensures that passwords for those websites can’t be saved or auto filled into web forms.

- **Update extensions to the Microsoft Edge Add-ons store using API's (in public preview).** You can integrate these API's directly into your build pipeline, and publish package updates to the Microsoft Edge Add-on website. To learn more, see [Using the Microsoft Edge Add-ons API (in private preview)](/microsoft-edge/extensions-chromium/publish/api/using-addons-api)

### Policy updates

#### New Policies

- [AllowGamesMenu](/DeployEdge/microsoft-edge-policies#allowgamesmenu) - Allow users to access the games menu
- [DoNotSilentlyBlockProtocolsFromOrigins](/DeployEdge/microsoft-edge-policies#donotsilentlyblockprotocolsfromorigins) - Define a list of protocols that can not be silently blocked by anti-flood protection
- [HubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#hubssidebarenabled) - Show Hubs Sidebar
- [InternetExplorerIntegrationCloudNeutralSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) - Configure reporting of potentially misconfigured neutral site URLs to the M365 Admin Center Site Lists app
- [InternetExplorerIntegrationCloudUserSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) - Configure reporting of IE Mode user list entries to the M365 Admin Center Site Lists app
- [PasswordManagerBlocklist](/DeployEdge/microsoft-edge-policies#passwordmanagerblocklist) - Configure the list of domains for which the password manager UI (Save and Fill) will be disabled
- [RelatedMatchesCloudServiceEnabled](/DeployEdge/microsoft-edge-policies#relatedmatchescloudserviceenabled) - Configure Related Matches in Find on Page
- [SignInCtaOnNtpEnabled](/DeployEdge/microsoft-edge-policies#signinctaonntpenabled) - Enable sign in click to action dialog
- [UserAgentReduction](/DeployEdge/microsoft-edge-policies#useragentreduction) - Enable or disable the User-Agent Reduction

## Version 98.0.1108.48: February 8

Fixed various bugs and performance issues.

## Version 98.0.1108.43: February 3

Fixed various bugs and performance issues.

## Version 98.0.1108.42: February 2

Fixed various bugs and performance issues.

## Version 98.0.1108.39: January 31

Fixed various bugs and performance issues.

## Version 98.0.1108.33: January 24

Fixed various bugs and performance issues.

## Version 98.0.1108.27: January 19

Fixed various bugs and performance issues.


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

