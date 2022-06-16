---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 06/16/2022
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

## Version 102.0.1245.44: June 16

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 102.0.1245.41: June 13

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-13-2022).

## Version 102.0.1245.39: June 9

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-9-2022).

## Version 102.0.1245.33: June 3

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 102.0.1245.30: May 31

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-31-2022).

### Policy updates

#### New policies

- [AllHttpAuthSchemesAllowedForOrigins](/DeployEdge/microsoft-edge-policies#allhttpauthschemesallowedfororigins) - List of origins that allow all HTTP authentication
- [OutlookHubMenuEnabled](/DeployEdge/microsoft-edge-policies#outlookhubmenuenabled) - Allow users to access the Outlook menu
- [NetworkServiceSandboxEnabled](/DeployEdge/microsoft-edge-policies#networkservicesandboxenabled) - Enable the network service sandbox
- [UserAgentClientHintsGREASEUpdateEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsgreaseupdateenabled) - Control the User-Agent Client Hints GREASE Update feature

## Version 101.0.1210.53: May 19

Fixed various bugs and performance issues.

## Version 100.0.1185.60: May 13

Fixed various bugs and performance issues for Extended Stable release.

## Version 101.0.1210.47: May 13

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-13-2022).

## Version 101.0.1210.39: May 5

Fixed various bugs and performance issues.

## Version 100.0.1185.57: May 2

Fixed various bugs and performance issues for Extended Stable release.

## Version 101.0.1210.32: April 28

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-28-2022).

### Feature updates

- **Ability to set the default profile.** The [EdgeDefaultProfileEnabled](/DeployEdge/microsoft-edge-policies#edgedefaultprofileenabled) policy will let you set a default profile to use when opening the browser instead of the last profile that was used. This policy won't be applicable if the `--profile-directory` parameter has been specified.

- **Launch Progressive Web Apps (PWAs) from the favorites bar.** Improvements to the PWA launch experience will start appearing with an Apps icon that can be added to the toolbar.

- **Manage the "Allow extensions from other stores" setting.** Now you can use the [ControlDefaultStateOfAllowExtensionFromOtherStoresSettingEnabled](/DeployEdge/microsoft-edge-policies#controldefaultstateofallowextensionfromotherstoressettingenabled) policy to set the default state of the "Allow extensions from other stores" setting.

- **Improvements to the Enterprise Site List Manager.** Now you can configure shared cookies between Microsoft Edge and Internet Explorer on your enterprise site list. You can access the [Enterprise Site List Manager](/deployedge/edge-ie-mode-site-list-manager) at *edge://compat/SiteListManager*.

### Policy updates

#### New policies

- [ConfigureKeyboardShortcuts](/DeployEdge/microsoft-edge-policies#configurekeyboardshortcuts) - Configure the list of commands for which to disable keyboard shortcuts
- [ControlDefaultStateOfAllowExtensionFromOtherStoresSettingEnabled](/DeployEdge/microsoft-edge-policies#controldefaultstateofallowextensionfromotherstoressettingenabled) - Configure default state of Allow extensions from other stores setting
- [EdgeAssetDeliveryServiceEnabled](/DeployEdge/microsoft-edge-policies#edgeassetdeliveryserviceenabled) - Allow features to download assets from the Asset Delivery Service
- [EdgeDefaultProfileEnabled](/DeployEdge/microsoft-edge-policies#edgedefaultprofileenabled) - Default Profile Setting Enabled
- [InternetExplorerModeEnableSavePageAs](/DeployEdge/microsoft-edge-policies#internetexplorermodeenablesavepageas) - Allow Save page as in Internet Explorer mode
- [KioskSwipeGesturesEnabled](/DeployEdge/microsoft-edge-policies#kioskswipegesturesenabled) - Swipe gestures in Microsoft Edge kiosk mode enabled
- [MicrosoftOfficeMenuEnabled](/DeployEdge/microsoft-edge-policies#microsoftofficemenuenabled) - Allow users to access the Microsoft Office menu
- [SiteSafetyServicesEnabled](/DeployEdge/microsoft-edge-policies#sitesafetyservicesenabled) - Allow users to configure Site safety services

#### Deprecated policies

- [ForceCertificatePromptsOnMultipleMatches](/DeployEdge/microsoft-edge-policies#forcecertificatepromptsonmultiplematches) - Configure whether Microsoft Edge should automatically select a certificate when there are multiple certificate matches for a site configured with "AutoSelectCertificateForUrls"

#### Obsoleted policies

- [WebSQLInThirdPartyContextEnabled](/DeployEdge/microsoft-edge-policies#websqlinthirdpartycontextenabled) - Force WebSQL in third-party contexts to be re-enabled

## Version 100.0.1185.50: April 21

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 100.0.1185.44: April 15

> [!Important]
> This update contains a fix for [CVE-2022-1364](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-1364), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-15-2022).

## Version 100.0.1185.39: April 11

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 100.0.1185.36: April 7

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-7-2022).

## Version 100.0.1185.29: April 1

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-1-2022).

### Feature updates

- **Three-digit version number in the User-agent string.** Microsoft Edge will now send a three-digit version number, such as Edg/100 in the User-Agent header. This may confuse scripts or server-side analytics that use a buggy parser to determine the User-Agent string version number. You can use the [ForceMajorVersionToMinorPositionInUserAgent](/deployedge/microsoft-edge-policies#forcemajorversiontominorpositioninuseragent) policy to control whether the User-Agent string major version should be frozen at 99. Also, the **#force-major-version-to-minor** flag is available in *edge://flags* to freeze the major version in the User-Agent string to 99.

- **Streamlining Microsoft 365 Application Protocol Activations.** Microsoft 365 Application Protocol Activations on trusted Microsoft cloud storage services will now launch certain Microsoft 365 applications directly, including SharePoint subdomains and Microsoft OneDrive URLs. You can use the policies [AutoLaunchProtocolsComponentEnabled](/deployedge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) and [AutoLaunchProtocolsFromOrigins](/deployedge/microsoft-edge-policies#autolaunchprotocolsfromorigins) to enable the application protocol activation prompts if desired, and to define other applications and services where warnings are enabled or disabled.

- **Hardware-enforced Stack Protection.** Microsoft Edge will continue supporting more fine-grained protection by combating memory corruption vulnerabilities and by protecting indirect calls. Hardware-enforced stack protection is only supported by Windows 8 and later. For more information, see [Hardware-enforced Stack Protection](https://techcommunity.microsoft.com/t5/windows-kernel-internals-blog/developer-guidance-for-hardware-enforced-stack-protection/ba-p/2163340). This feature behavior can be controlled using the [ShadowStackCrashRollbackBehavior](/deployedge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) policy.

- **Preview PDF files in Microsoft Outlook and File Explorer.** Users can view a PDF file in a lightweight and rich read-only preview. This feature is available for Outlook Desktop PDF attachments or for local PDF files using File Explorer.

- **Open Digitally Signed PDF files.** Digital signatures are used extensively to validate the authenticity of a document and changes made in a document. You can use the [PDFSecureMode](/deployedge/microsoft-edge-policies#pdfsecuremode) policy to enable digital signature validation for PDF files, directly from the browser, without the need for any add-ins.

### Policy updates

#### New policies

- [AdsTransparencyEnabled](/DeployEdge/microsoft-edge-policies#adstransparencyenabled) - Configure if the ads transparency feature is enabled
- [DefaultWebHidGuardSetting](/DeployEdge/microsoft-edge-policies#defaultwebhidguardsetting) - Control use of the WebHID API
- [HideRestoreDialogEnabled](/DeployEdge/microsoft-edge-policies#hiderestoredialogenabled) - Hide restore pages dialog after browser crash
- [PDFSecureMode](/DeployEdge/microsoft-edge-policies#pdfsecuremode) - Secure mode and Certificate-based Digital Signature validation in native PDF reader
- [PromptOnMultipleMatchingCertificates](/DeployEdge/microsoft-edge-policies#promptonmultiplematchingcertificates) - Prompt the user to select a certificate when multiple certificates match
- [WebHidAskForUrls](/DeployEdge/microsoft-edge-policies#webhidaskforurls) - Allow the WebHID API on these sites
- [WebHidBlockedForUrls](/DeployEdge/microsoft-edge-policies#webhidblockedforurls) - Block the WebHID API on these sites

#### Deprecated policy

- [BackgroundTemplateListUpdatesEnabled](/DeployEdge/microsoft-edge-policies#backgroundtemplatelistupdatesenabled) - Enables background updates to the list of available templates for Collections and other features that use templates

#### Obsoleted policy

- [AllowSyncXHRInPageDismissal](/DeployEdge/microsoft-edge-policies#allowsyncxhrinpagedismissal) - Allow pages to send synchronous XHR requests during page dismissal

## Version 98.0.1108.92: March 26

Fixed various bugs and performance issues for Extended Stable release.

## Version 99.0.1150.55: March 26

> [!Important]
> This update contains a fix for [CVE-2022-1096](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-1096), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-26-2022).

## Version 99.0.1150.52: March 24

Fixed various bugs and performance issues.

## Version 98.0.1108.84: March 17

Fixed various bugs and performance issues for Extended Stable release.

## Version 99.0.1150.46: March 17

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-17-2022).

## Version 99.0.1150.39: March 10

Fixed various bugs and performance issues.

## Version 98.0.1108.76: March 9

Fixed various bugs and performance issues for Extended Stable release.

## Version 99.0.1150.36: March 7

Fixed various bugs and performance issues.

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
