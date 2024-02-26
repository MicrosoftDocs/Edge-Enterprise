---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 02/23/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
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

## Version 122.0.2365.52: February 23, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#february-23-2024).

### Fixes

- Resolved an issue where PDF text fields and drop downs values were being rendered twice for specific files when using the Microsoft Edge built-in PDF reader powered by Adobe Acrobat.
- Resolved an issue where printing certain PDF files in landscape mode with the 'fit to printable area' option resulted in incorrect printing.

### Dev Channel updates

The following Dev channel updates preceded this Stable channel release. The following Dev notes provide detailed information about the changes in each release.

- [Dev Channel update to 122.0.2325.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/discussions/dev-channel-update-to-122-0-2325-0-is-live/m-p/4026405)
- [Dev Channel update to 122.0.2348.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/discussions/dev-channel-update-to-122-0-2348-0-is-live/m-p/4034978)
- [Dev Channel update to 122.0.2353.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/discussions/dev-channel-update-to-122-0-2353-0-is-live/m-p/4039264)
- [Dev Channel update to 122.0.2365.3 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-122-0-2365-3-is-live/m-p/4044002)

### Feature updates

- **Moving Managed Site Indicator (Briefcase icon) into the lock icon in the address bar omnibox.** The briefcase icon which signals that a page is managed via admin policies, has been moved into the lock icon in the address bar. End users can view details about the protections for a given page by clicking the lock icon in the address bar and then clicking the briefcase icon. For more information, see [Understand Data loss Prevention in Microsoft Edge](/deployedge/microsoft-edge-security-dlp).

- **Deprecation of the image enhancement feature.** To improve end user experience, the image enhancement feature is deprecated.

- **Configure recommended policies in the Microsoft Edge management service.** The Microsoft Edge management service now provides admins with the ability to set recommended policies. This gives end users permission to override their admin's policy configuration.

- **Microsoft Edge has rebranded Web Capture to "Screenshot".**  Microsoft Edge changed the branding for Web Capture with an icon change and renamed the feature to "Screenshot". Users can easily use content from the web by taking a screenshot of a full page or a selected area. They can mark up the screenshot they took with a pen or touch later.  Administrators can control availability using the [WebCaptureEnabled](/deployedge/microsoft-edge-policies#webcaptureenabled) policy. For more information, see [Screenshot (microsoft.com)](https://www.microsoft.com/en-us/edge/features/screenshot?form=MA13FJ).
 
### Policy updates

#### New policies

- [AIGenThemesEnabled](/deployedge/microsoft-edge-policies#aigenthemesenabled) - Enables DALL-E themes generation
- [EnhanceSecurityModeAllowUserBypass](/deployedge/microsoft-edge-policies#enhancesecuritymodeallowuserbypass) - Allow users to bypass Enhanced Security Mode
- [SuperDragDropEnabled](/deployedge/microsoft-edge-policies#super-drag-drop-enabled) - Super Drag Drop enabled
- [UrlDiagnosticDataEnabled](/deployedge/microsoft-edge-policies#urldiagnosticdataenabled) - URL reporting in Edge diagnostic data enabled
- [EdgeOpenInSidebarEnabled](/deployedge/microsoft-edge-policies#edgeopeninsidebarenabled) - Enable open in Sidebar
- [EdgeSidebarCustomizeEnabled](/deployedge/microsoft-edge-policies#edgesidebarcustomizeenabled) - Enable sidebar customize

#### Obsolete policies

- [EdgeEnhanceImagesEnabled](/deployedge/microsoft-edge-policies#edgeenhanceimagesenabled) - Enhance images enabled (obsolete)

#### Additional policy changes

- [DiagnosticData](/deployedge/microsoft-edge-policies#diagnosticdata) - Send required and optional diagnostic data about browser usage. Supported on Windows since Stable 122 or later.

## Version 120.0.2210.181: February 20, 2024

Fixed various bugs and performance issues for Extended Stable channel.

## Version 121.0.2277.128: February 15, 2024

Fixed various bugs and performance issues.

### Fixes

- Edge has a feature that provides an option to import browser data on each launch from other browsers with user consent. This feature's state might not have been syncing and displaying correctly across multiple devices. This is fixed.

### Policy updates

#### Additional policy changes

- [EdgeManagementPolicyOverridesPlatformPolicy](/deployedge/microsoft-edge-policies#edgemanagementpolicyoverridesplatformpolicy) - For Microsoft Edge version 121.0.2277 and later, this policy will control all device policies.
- [EdgeManagementUserPolicyOverridesCloudMachinePolicy](/deployedge/microsoft-edge-policies#edgemanagementuserpolicyoverridescloudmachinepolicy)  - For Microsoft Edge version 121.0.2277 and later, this policy will control all per user profile policies.

<!-- =================================================== -->
## Version 120.0.2210.175: February 8, 2024

Fixed various bugs and performance issues for Extended Stable channel.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#february-8-2024).

## Version 121.0.2277.112: February 8, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#february-8-2024).

## Version 121.0.2277.110: February 7, 2024

Fixed various bugs and performance issues.

## Version 121.0.2277.106: February 5, 2024

Fixed various bugs and performance issues.

### Fixes

- Resolved an issue where the [IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled) policy didn't work as expected while opening `file://` links.

## Version 121.0.2277.98: February 1, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#february-1-2024).

## Version 120.0.2210.167: January 31, 2024

Fixed various bugs and performance issues for Extended Stable.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-31-2024).

## Version 121.0.2277.83: January 25, 2024

Fixed various bugs and performance issues. For more information, see [Improved reliability](#improved-reliability) and [Dev Channel updates](#dev-channel-updates).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-25-2024).

### Improved reliability

- Fixed a browser crash in on-premise sync

### Dev Channel updates

The following Dev channel updates preceded this Stable channel release. The following  Dev notes provide detailed information about the changes in each release.

- [Dev Channel update to 121.0.2274.0 is live - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/discussions/dev-channel-update-to-121-0-2274-0-is-live/m-p/4010747)
- [Dev Channel update to 121.0.2256.2 is live - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/discussions/dev-channel-update-to-121-0-2256-2-is-live/m-p/4004721)
- [Dev Channel update to 121.0.2248.1 is live - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/discussions/dev-channel-update-to-121-0-2248-1-is-live/m-p/3998824)
- [Dev Channel update to 121.0.2220.3 is live - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/discussions/dev-channel-update-to-121-0-2220-3-is-live/m-p/3986444)

### Feature updates

- **Enable organizational branding in Edge for Business.**   Enable your organization's branding assets from Entra onto profile-related UI for profiles signed in with an Entra ID (formerly known as Azure Active Directory) account. You can add your organization's details such as name to the profile pill, name and brand color to the profile flyout, and logo to overlay the Edge for Business taskbar icon. This branding can help users more easily differentiate between multiple profiles and browser windows.

  Default organizational branding can be enabled by admins through the following policies:

  - [OrganizationalBrandingOnWorkProfileUIEnabled](/deployedge/microsoft-edge-policies#organizationalbrandingonworkprofileuienabled
)
  - [OrganizationLogoOverlayOnAppIconEnabled](/deployedge/microsoft-edge-policies#organizationlogooverlayonappiconenabled)

  Admins will need to have "company branding" assets configured in the Microsoft Entra admin center for branding assets to be applied to this feature.

  For more information, see [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business) and [Add company branding to your organization's sign-in page](/entra/fundamentals/how-to-customize-branding).

- **Microsoft Edge migrates the updates experience into Browser Essentials.** Getting alerts on available Edge Updates will come from Browser Essentials instead of the Settings page for better visibility and experience. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Added support for AVIF and AV1 file formats.** Microsoft Edge now supports the AVIF and AV1 file formats which offer better compression and higher quality images and videos.  Users can enjoy faster loading times and better quality media on websites.  

- **E-tree in Wallet.** Users signed into Microsoft Edge with a personal Microsoft Account (MSA) can grow a virtual seed into a tree with Wallet. Once it's grown, a real tree is planted.  Administrators can control the availability using the [EdgeWalletEtreeEnabled](/deployedge/microsoft-edge-policies#edgewalletetreeenabled) policy.

- **New Website Typo Protection policies.** The built-in Website Typo Protection warns users if it appears there is a mistyped popular domain name which could land users on a malicious webpage.  Administrators can control the availability and configure Website Typo Protection by using the [PreventTyposquattingPromptOverride](/deployedge/microsoft-edge-policies#preventtyposquattingpromptoverride) and [TyposquattingAllowListDomains](/deployedge/microsoft-edge-policies#typosquattingallowlistdomains) policies.

### Policy updates

#### New policies

- [EdgeDisableDialProtocolForCastDiscovery](/deployedge/microsoft-edge-policies#edgedisabledialprotocolforcastdiscovery) - Disable DIAL protocol for cast device discovery
- [NativeHostsExecutablesLaunchDirectly](/deployedge/microsoft-edge-policies#nativehostsexecutableslaunchdirectly) - Force Windows executable Native Messaging hosts to launch directly
- [RelatedWebsiteSetsEnabled](/deployedge/microsoft-edge-policies#relatedwebsitesetsenabled) - Enable Related Website Sets
- [RelatedWebsiteSetsOverrides](/deployedge/microsoft-edge-policies#relatedwebsitesetsoverrides) - Override Related Website Sets
- [PreventTyposquattingPromptOverride](/deployedge/microsoft-edge-policies#preventtyposquattingpromptoverride) - Prevent bypassing Edge Website Typo Protection prompts for sites
- [TyposquattingAllowListDomains](/deployedge/microsoft-edge-policies#typosquattingallowlistdomains) - Configure the list of domains for which Edge Website Typo Protection won't trigger warnings
- [EdgeBlockSignInEnabled](/deployedge/microsoft-edge-mobile-policies#edgeblocksigninenabled) - Block users from signing in to Edge
- [ExperimentationAndConfigurationServiceControl](/deployedge/microsoft-edge-mobile-policies#experimentationandconfigurationservicecontrol) - Control communication with the Experimentation and Configuration Service

#### Obsoleted policies

- [SendMouseEventsDisabledFormControlsEnabled](/deployedge/microsoft-edge-policies#sendmouseeventsdisabledformcontrolsenabled) - Control the new behavior for event dispatching on disabled form controls
- [WebRtcAllowLegacyTLSProtocols](/deployedge/microsoft-edge-policies#webrtcallowlegacytlsprotocols) - Allow legacy TLS/DTLS downgrade in WebRTC (obsoleted)

## Version 120.0.2210.160: January 25, 2024

Fixed various bugs and performance issues for Extended Stable.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-25-2024).
<!-- ================== last note ===================== -->
## Version 120.0.2210.144: January 17, 2024

Fixed various bugs and performance issues.

> [!IMPORTANT]
> This update to Stable channel contains a fix for [CVE-2024-0519](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2024-0519), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-17-2024).

## Version 120.0.2210.133: January 11, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-11-2024).

## Version 120.0.2210.121: January 5, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-5-2024).

## Version 120.0.2210.91: December 21, 2023

Fixed various bugs and performance issues.

> [!IMPORTANT]
> This update to Stable channel contains a fix for [CVE-2023-7024](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2023-7024), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#december-21-2023).

## Version 120.0.2210.89: December 20, 2023

Fixed various bugs and performance issues.

### Feature updates

- **Microsoft Edge Workspaces improvements for offline functionality.** Any workspace previously opened on a device is cached locally and can be opened on that device from that cache even if it fails to connect. Changes persist on that device and are resolved into the synced version when a connection can finally be made. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

## Version 120.0.2210.77: December 14, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#december-14-2023).

## Version 120.0.2210.61: December 7, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#december-7-2023).

### Feature updates

- **RendererAppContainer.** For extra security benefits, the Windows native app container is enabled by default. Note: If Enterprise organizations identify a compatibility issue due to code injection from security software, they should follow up with the software publisher directly. Alternatively, they can use the [RendererAppContainerEnabled](/deployedge/microsoft-edge-policies#rendererappcontainerenabled) policy to trade off the security benefits in Microsoft Edge with their other software.

- **Updated SmartActionsBlockList policy.** The [SmartActionsBlockList](/deployedge/microsoft-edge-policies#smartactionsblocklist) policy is updated with new policy option mappings. Administrators can now configure the policy to control Smart actions like definitions on websites (smart_actions_website) or control Smart actions in pdfs and on websites (smart_actions).

### Policy updates

#### New policies

- [AutoDiscardSleepingTabsEnabled](/deployedge/microsoft-edge-policies#autodiscardsleepingtabsenabled) - Configure auto discard sleeping tabs
- [AutomaticProfileSwitchingSiteList](/deployedge/microsoft-edge-policies#automaticprofileswitchingsitelist) - Configure the automatic profile switching site list
- [Edge3PSerpTelemetryEnabled](/deployedge/microsoft-edge-policies#edge3pserptelemetryenabled) - Edge 3P SERP Telemetry Enabled
- [PostQuantumKeyAgreementEnabled](/deployedge/microsoft-edge-policies#postquantumkeyagreementenabled) - Enable post-quantum key agreement for TLS
- [WebAppSettings](/deployedge/microsoft-edge-policies#webappsettings) - Web App management settings
- [OrganizationLogoOverlayOnAppIconEnabled](/deployedge/microsoft-edge-policies#organizationlogooverlayonappiconenabled) - Allow your organization's logo from Microsoft Entra to be overlaid on the Microsoft Edge app icon of a work profile

## Version 118.0.2088.122: November 29, 2023

Fixed various bugs and performance issues for Extended Stable release.

> [!IMPORTANT]
> This update to Extended Stable channel contains a fix for [CVE-2023-6345](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2023-6345), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#november-29-2023).

<!-- Version 119.0.2151.97: November 29, 2023 to Version 118.0.2088.57: October 18, 2023 -->
<!-- from Version 118.0.2088.46: October 13, 2023 to Version 109.0.1518.140: September 15, 2023 -->
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
