---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 03/28/2022
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

## Version 99.0.1150.30: March 3

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-3-2022).

### Feature updates

- **Upcoming three-digit version number in user agent string.** Starting with version 100, Microsoft Edge will send a three-digit version number in the User-Agent header, for example "Edg/100". Starting with Microsoft Edge 97, site owners can test this upcoming agent string by enabling the **#force-major-version-to-100** experiment flag in *edge://flags* to ensure their User-Agent parsing logic is robust and works as expected.

- **Personalize multi-profile experiences with profile preferences for sites.** Users can personalize their multi-profile experience with the ability to create a customized list of sites for automatic profile switching in Microsoft Edge.

- **Navigate PDF documents using page thumbnails.** You'll now be able to navigate through your PDF document using thumbnails that represent the pages. These thumbnails will appear in the pane on the left side of the PDF reader.

- **Configure the list of domains for which the password manager User Interface (UI) for Save and Fill will be disabled.** Use the [PasswordManagerBlocklist](/deployedge/microsoft-edge-policies#passwordmanagerblocklist) policy to configure the list of domains (HTTP/HTTPS schemas and hostnames only) where Microsoft Edge should disable the password manager. This means that Save and Fill workflows will be disabled, which ensures that passwords for those websites can’t be saved or auto filled into web forms.

- **Custom primary password.** The browser already has the capability where users can add an authentication step before saved passwords are auto filled in web forms. This adds another layer of privacy and helps prevent unauthorized users from using saved passwords to log on websites. Custom primary password is an evolution of that same feature, where users will now be able to use a custom string of their choice as their primary password. After it's enabled, users will enter this password to authenticate themselves and have their saved passwords auto filled into web forms.

### Policy updates

#### New Policies

- [DoNotSilentlyBlockProtocolsFromOrigins](/DeployEdge/microsoft-edge-policies#donotsilentlyblockprotocolsfromorigins) - Define a list of protocols that can not be silently blocked by anti-flood protection
- [ForceMajorVersionToMinorPositionInUserAgent](/DeployEdge/microsoft-edge-policies#forcemajorversiontominorpositioninuseragent) - Enable or disable freezing the User-Agent string at major version 99
- [HubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#hubssidebarenabled) - Show Hubs Sidebar
- [InternetExplorerIntegrationCloudNeutralSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) - Configure reporting of potentially misconfigured neutral site URLs to the M365 Admin Center Site Lists app
- [InternetExplorerIntegrationCloudUserSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) - Configure reporting of IE Mode user list entries to the M365 Admin Center Site Lists app
- [PasswordManagerBlocklist](/DeployEdge/microsoft-edge-policies#passwordmanagerblocklist) - Configure the list of domains for which the password manager UI (Save and Fill) will be disabled
- [RelatedMatchesCloudServiceEnabled](/DeployEdge/microsoft-edge-policies#relatedmatchescloudserviceenabled) - Configure Related Matches in Find on Page
- [SignInCtaOnNtpEnabled](/DeployEdge/microsoft-edge-policies#signinctaonntpenabled) - Enable sign in click to action dialog
- [UserAgentReduction](/DeployEdge/microsoft-edge-policies#useragentreduction) - Enable or disable the User-Agent Reduction

## Version 98.0.1108.62: February 24

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 98.0.1108.56: February 17

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 98.0.1108.55: February 16

> [!Important]
> This update contains a fix for [CVE-2022-0609](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-0609), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#february-16-2022).

## Version 98.0.1108.50: February 10

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#february-10-2022).

## Version 98.0.1108.43: February 3

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#february-3-2022).

### Feature updates

- **Enhance your security on the web.** This is a browsing mode in Microsoft Edge where browser security takes priority, giving users an extra layer of protection when browsing the web. Administrators can apply group policies to end-user desktops (Windows, macOS, and Linux) to help protect against in-the-wild exploits (also referred to 0-days). The following group policies support this browsing mode:

  - [EnhanceSecurityMode](/deployedge/microsoft-edge-policies#enhancesecuritymode)
  - [EnhanceSecurityModeBypassListDomains](/deployedge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains)
  - [EnhanceSecurityModeEnforceListDomains](/deployedge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains)

- **Upcoming three-digit version number in user agent string.** Starting with version 100, Microsoft Edge will send a three-digit version number in the User-Agent header, for example "Edg/**100**". Starting with Microsoft Edge 97, site owners can test this upcoming user agent string by enabling the **#force-major-version-to-100** experiment flag in *edge://flags* to ensure their User-Agent parsing logic is robust and works as expected.

- **Deprecate WebRTC's Plan B SDP semantics.** This change deprecates a legacy Session Description Protocol (SDP) dialect called Plan B. This SDP format is being replaced by the Unified Plan, which is a spec-compliant and cross-browser compatible SDP format. For more information, see the Chrome Platform Status entry [PSA: Plan B should throw in M96 Beta and Stable](https://chromestatus.com/feature/5823036655665152), and [PSA: Plan B throwing in Stable and Extended Deprecation Trial End Date](https://groups.google.com/g/discuss-webrtc/c/gEHrZyYKsfU). Requesting a [Trial for RTCPeerConnection Plan B SDP Semantics](https://developer.chrome.com/origintrials/#/view_trial/3892235977954951169) allows sites to continue to use the deprecated API until version 101.

- **Overlay scrollbars added to Microsoft Edge.** We've updated our scrollbars with an overlay-based design. Users can turn this feature on in *edge://flags*.

### Policy updates

#### New Policies

- [AddressBarEditingEnabled](/DeployEdge/microsoft-edge-policies#addressbareditingenabled) - Configure address bar editing
- [AllowGamesMenu](/DeployEdge/microsoft-edge-policies#allowgamesmenu) - Allow users to access the games menu
- [EdgeFollowEnabled](/DeployEdge/microsoft-edge-policies#edgefollowenabled) - Enable Follow service in Microsoft Edge
- [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode) - Enhance the security state in Microsoft Edge
- [EnhanceSecurityModeBypassListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains) - Configure the list of domains for which enhance security mode will not be enforced
- [EnhanceSecurityModeEnforceListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains) - Configure the list of domains for which enhance security mode will always be enforced
- [InAppSupportEnabled](/DeployEdge/microsoft-edge-policies#inappsupportenabled) - In-app support Enabled
- [MicrosoftEdgeInsiderPromotionEnabled](/DeployEdge/microsoft-edge-policies#microsoftedgeinsiderpromotionenabled) - Microsoft Edge Insider Promotion Enabled
- [PrintStickySettings](/DeployEdge/microsoft-edge-policies#printstickysettings) - Print preview sticky settings
- [SandboxExternalProtocolBlocked](/DeployEdge/microsoft-edge-policies#sandboxexternalprotocolblocked) - Allow Microsoft Edge to block navigations to external protocols in a sandboxed iframe
- [U2fSecurityKeyApiEnabled](/DeployEdge/microsoft-edge-policies#u2fsecuritykeyapienabled) - Allow using the deprecated U2F Security Key API

## Version 97.0.1072.76: January 27

Fixed various bugs and performance issues.

### Feature updates

- **Upcoming three-digit version number in user agent string.** Starting with version 100, Microsoft Edge will send a three-digit version number in the User-Agent header, for example "Edg/**100**". Starting with Microsoft Edge 97, site owners can test this upcoming user agent string by enabling the **#force-major-version-to-100** experiment flag in *edge://flags* to ensure their User-Agent parsing logic is robust and works as expected.

## Version 96.0.1054.75: January 21

Fixed various bugs and performance issues for Extended Stable release.

## Version 97.0.1072.69: January 20

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-20-2022).

## Version 97.0.1072.62: January 13

Fixed various bugs and performance issues.

## Version 96.0.1054.72: January 6

Fixed various bugs and performance issues for Extended Stable release.

## Version 97.0.1072.55: January 6

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-6-2022).

### Feature updates

- **Use the current profile to sign into websites when multiple work or school accounts are signed in on a device.** When multiple work or school accounts are signed in on a device, users will be asked to choose an account from the account picker to continue their visits to websites. In this release, users will be prompted to let Microsoft Edge sign in to the websites automatically with the work or school account that's signed into the current profile. Users can turn this feature on and off in **Settings** > **Profile preferences**.

- **Add support for Microsoft Endpoint Data Loss Prevention (DLP) on macOS.** Microsoft Endpoint DLP policy enforcement will be available natively on macOS.

- **Automatic HTTPS.** Users can upgrade navigations from HTTP to HTTPS on domains likely to support this more secure protocol. This support can also be configured to attempt delivery over HTTPS for all domains. Note: This feature is a Controlled Feature Rollout. If you don’t see this feature, check back as we continue our rollout.

- **Block WebSQL in 3rd-party contexts.** Use of the legacy WebSQL feature will be blocked from 3rd-party frames. The [WebSQLInThirdPartyContextEnabled](/deployedge/microsoft-edge-policies#websqlinthirdpartycontextenabled) policy is available as an opt-out option until Microsoft Edge version 101. This change is happening in the Chromium project that Microsoft Edge is based on. For more information, see this [Chrome Platform Status](https://chromestatus.com/feature/5684870116278272) entry.

- **Citations in Microsoft Edge.** Citing sources for research is a common requirement for students. They have to manage many research references and sources, which aren't easy tasks. They also have to translate these citations to proper citation formats like APA, MLA, and Chicago. This new "Citations" feature, now in Preview in Microsoft Edge, gives students a better way to manage and generate citations as they research online. With Citations turned on in Collections or from **Settings and more (Alt-F)**, Microsoft Edge automatically generates citations that students can use later so they can stay focused on their research. When they're done, they can easily compile these citations into a final deliverable. For more information, see [Previewing Citations in Microsoft Edge](https://blogs.windows.com/msedgedev/2021/11/04/preview-citations-feature-edge/).

- **Control Flow Guard (CFG).** Microsoft Edge will start supporting more fine-grained protection by combating memory corruption vulnerabilities and by protecting indirect calls. CFG is only supported with Windows 8 and later. For more information, see [Control Flow Guard](/windows/win32/secbp/control-flow-guard).
  
  > [!NOTE]
  > This is an evolving technology, please share your feedback to help us strengthen its support.

### Policy updates

#### New Policies

- [AccessibilityImageLabelsEnabled](/DeployEdge/microsoft-edge-policies#accessibilityimagelabelsenabled) - Get Image Descriptions from Microsoft Enabled
- [CORSNonWildcardRequestHeadersSupport](/DeployEdge/microsoft-edge-policies#corsnonwildcardrequestheaderssupport) - CORS non-wildcard request header support enabled
- [EdgeDiscoverEnabled](/DeployEdge/microsoft-edge-policies#edgediscoverenabled) - Discover feature In Microsoft Edge
- [EdgeEnhanceImagesEnabled](/DeployEdge/microsoft-edge-policies#edgeenhanceimagesenabled) - Enhance images enabled
- [InternetExplorerModeTabInEdgeModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorermodetabinedgemodeallowed) - Allow sites configured for Internet Explorer mode to open in Microsoft Edge
- [SameOriginTabCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#sameorigintabcaptureallowedbyorigins) - Allow Same Origin Tab capture by these origins
- [ScreenCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#screencaptureallowedbyorigins) - Allow Desktop, Window, and Tab capture by these origins
- [SerialAllowAllPortsForUrls](/DeployEdge/microsoft-edge-policies#serialallowallportsforurls) - Automatically grant sites permission to connect all serial ports
- [SerialAllowUsbDevicesForUrls](/DeployEdge/microsoft-edge-policies#serialallowusbdevicesforurls) - Automatically grant sites permission to connect to USB serial devices
- [SmartScreenDnsRequestsEnabled](/DeployEdge/microsoft-edge-policies#smartscreendnsrequestsenabled) - Enable Microsoft Defender SmartScreen DNS requests
- [TabCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#tabcaptureallowedbyorigins) - Allow Tab capture by these origins
- [WebSQLInThirdPartyContextEnabled](/DeployEdge/microsoft-edge-policies#websqlinthirdpartycontextenabled) - Force WebSQL in third-party contexts to be re-enabled
- [WindowCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#windowcaptureallowedbyorigins) - Allow Window and Tab capture by these origins

## Version 96.0.1054.62: December 17

Fixed various bugs and performance issues.

## Version 96.0.1054.57: December 14

> [!Important]
> This update contains a fix for [CVE-2021-4102](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-4102), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#december-14-2021).

## Version 96.0.1054.53: December 10

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#december-10-2021).

## Version 96.0.1054.43: December 2

Fixed various bugs and performance issues.

## Version 96.0.1054.41: November 30

Fixed various bugs and performance issues.

## Version 96.0.1054.34: November 23

Fixed various bugs and performance issues.

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
