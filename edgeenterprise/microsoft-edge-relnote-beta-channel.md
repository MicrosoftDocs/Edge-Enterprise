---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 06/28/2022
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

## Version 104.0.1293.X: June 2x

### Policy updates

#### New policies

- [AllowedDomainsForApps](/DeployEdge/microsoft-edge-policies#alloweddomainsforapps) - Define domains allowed to access Google Workspace
- [AskBeforeCloseEnabled](/DeployEdge/microsoft-edge-policies#askbeforecloseenabled) - Get user confirmation before closing a browser window with multiple tabs
- [BrowserCodeIntegritySetting](/DeployEdge/microsoft-edge-policies#browsercodeintegritysetting) - Configure browser process code integrity guard setting
- [DoubleClickCloseTabEnabled](/DeployEdge/microsoft-edge-policies#doubleclickclosetabenabled) - Double Click feature in Microsoft Edge enabled (only available in China)
- [ImportOnEachLaunch](/DeployEdge/microsoft-edge-policies#importoneachlaunch) - Allow import of data from other browsers on each Microsoft Edge launch
- [QuickSearchShowMiniMenu](/DeployEdge/microsoft-edge-policies#quicksearchshowminimenu) - Enables Microsoft Edge mini menu
- [PasswordManagerRestrictLengthEnabled](/DeployEdge/microsoft-edge-policies#passwordmanagerrestrictlengthenabled) - Restrict the length of passwords that can be saved in the Password Manager
- [PDFXFAEnabled](/DeployEdge/microsoft-edge-policies#pdfxfaenabled) - XFA support in native PDF reader enabled
- [TextPredictionEnabled](/DeployEdge/microsoft-edge-policies#textpredictionenabled) - Text prediction enabled by default

#### Obsoleted policy

- [U2fSecurityKeyApiEnabled](/DeployEdge/microsoft-edge-policies#u2fsecuritykeyapienabled) - Allow using the deprecated U2F Security Key API

## Version 103.0.1264.37: June 22

Fixed various bugs and performance issues.

## Version 103.0.1264.32: June 20

Fixed various bugs and performance issues.

## Version 103.0.1264.21: June 10

Fixed various bugs and performance issues.

## Version 103.0.1264.17: June 6

Fixed various bugs and performance issues.

## Version 103.0.1264.13: June 2

### Feature updates

- **Ability to control automatic profile switching.** The [GuidedSwitchEnabled](/DeployEdge/microsoft-edge-policies#guidedswitchenabled) policy lets Microsoft Edge prompt the user to switch to the appropriate profile when Microsoft Edge detects that a link is a personal or work link.

- **Client Certificate Switcher.** This feature will offer a way for users to clear the remembered certificate and resurface the certificate picker when visiting a site requiring http certificate authentication. Switching can be done without manually quitting Microsoft Edge.

- **More reliable web defense.** Browse the web with more reliable protection thanks to the rewritten [Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) library for Microsoft Edge on Windows. The [NewSmartScreenLibraryEnabled](microsoft-edge-policies.md#newsmartscreenlibraryenabled) policy will allow enterprise customers to continue using the legacy version of the library until it’s deprecated in Microsoft Edge version 105.

### Policy updates

#### New policies

- [GuidedSwitchEnabled](/DeployEdge/microsoft-edge-policies#guidedswitchenabled) - Guided Switch Enabled
- [InternetExplorerZoomDisplay](/DeployEdge/microsoft-edge-policies#internetexplorerzoomdisplay) - Display zoom in IE Mode tabs with DPI Scale included like it is in Internet Explorer
- [LiveCaptionsAllowed](/DeployEdge/microsoft-edge-policies#livecaptionsallowed) - Live captions allowed
- [OriginAgentClusterDefaultEnabled](/DeployEdge/microsoft-edge-policies#originagentclusterdefaultenabled) - Origin-keyed agent clustering enabled by default

## Version 102.0.1245.25: May 26

Fixed various bugs and performance issues.

## Version 102.0.1245.22: May 24

Fixed various bugs and performance issues.

## Version 102.0.1245.18: May 20

Fixed various bugs and performance issues.

## Version 102.0.1245.14: May 16

Fixed various bugs and performance issues.

## Version 102.0.1245.12: May 13

Fixed various bugs and performance issues.

## Version 102.0.1245.7: May 10

### Policy updates

#### New policies

- [AllHttpAuthSchemesAllowedForOrigins](/DeployEdge/microsoft-edge-policies#allhttpauthschemesallowedfororigins) - List of origins that allow all HTTP authentication
- [OutlookHubMenuEnabled](/DeployEdge/microsoft-edge-policies#outlookhubmenuenabled) - Allow users to access the Outlook menu
- [NetworkServiceSandboxEnabled](/DeployEdge/microsoft-edge-policies#networkservicesandboxenabled) - Enable the network service sandbox
- [UserAgentClientHintsGREASEUpdateEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsgreaseupdateenabled) - Control the User-Agent Client Hints GREASE Update feature

## Version 101.0.1210.39: May 5

Fixed various bugs and performance issues.

## Version 101.0.1210.31: April 27

Fixed various bugs and performance issues.

## Version 101.0.1210.26: April 22

Fixed various bugs and performance issues.

## Version 101.0.1210.19: April 18

Fixed various bugs and performance issues.

## Version 101.0.1210.14: April 12

Fixed various bugs and performance issues.

### Feature updates

- **Improvements to the Enterprise Site List Manager.** Now you can configure shared cookies between Microsoft Edge and Internet Explorer on your enterprise site list. You can access the [Enterprise Site List Manager](/deployedge/edge-ie-mode-site-list-manager) at *edge://compat/SiteListManager*.

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

