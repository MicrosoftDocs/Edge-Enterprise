---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 01/24/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Microsoft Edge release notes for Beta Channel"
---

# Release notes for Microsoft Edge Beta Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Beta Channel. Archived versions of these release notes are available at [Archived release notes for Microsoft Edge Beta Channel](./microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> Microsoft Edge Web Platform constantly evolves to improve user experience, security, and privacy. To learn more, see [Site compatibility-impacting changes coming to Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## Version 121.0.2277.81: January 24, 2024

Fixed various bugs and performance issues.

## Version 121.0.2277.71: January 19, 2024

Fixed various bugs and performance issues.

## Version 121.0.2277.65: January 16, 2024

Fixed various bugs and performance issues.

## Version 121.0.2277.49: January 8, 2024

Fixed various bugs and performance issues.

### Feature update

- **Added support for AVIF and AV1 file formats.** Microsoft Edge now supports the AVIF and AV1 file formats which offer better compression and higher quality images and videos.  Users can enjoy faster loading times and better quality media on websites.  

## Version 121.0.2277.4: December 15, 2023

Fixed various bugs and performance issues.

### Feature updates

- **Enable organizational branding in Edge for Business.**   Enable your organization's branding assets from Entra onto profile-related UI for profiles signed in with an Entra ID (formerly known as Azure Active Directory) account. You can add your organization's details such as name to the profile pill, name and brand color to the profile flyout, and logo to overlay the Edge for Business taskbar icon. This branding can help users more easily differentiate between multiple profiles and browser windows.

  Default organizational branding can be enabled by admins through the following policies:

  - [OrganizationalBrandingOnWorkProfileUIEnabled](/deployedge/microsoft-edge-policies#organizationalbrandingonworkprofileuienabled
)
  - [OrganizationLogoOverlayOnAppIconEnabled](/deployedge/microsoft-edge-policies#organizationlogooverlayonappiconenabled)

  Admins will need to have "company branding" assets configured in the Microsoft Entra admin center for branding assets to be applied to this feature.

  For more information, see [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business) and [Add company branding to your organization's sign-in page](/entra/fundamentals/how-to-customize-branding).

- **Microsoft Edge migrates the updates experience into Browser Essentials.** Getting alerts on available Edge Updates will come from Browser Essentials instead of the Settings page for better visibility and experience. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **New Website Typo Protection policies.** The built-in Website Typo Protection warns users if it appears there is a mistyped popular domain name which could land users on a malicious webpage.  Administrators can control the availability and configure Website Typo Protection by using the [PreventTyposquattingPromptOverride](/deployedge/microsoft-edge-policies#preventtyposquattingpromptoverride) and [TyposquattingAllowListDomains](/deployedge/microsoft-edge-policies#typosquattingallowlistdomains) policies.

### Policy updates

#### New policies

- [EdgeDisableDialProtocolForCastDiscovery](/deployedge/microsoft-edge-policies#edgedisabledialprotocolforcastdiscovery) - Disable DIAL protocol for cast device discovery
- [NativeHostsExecutablesLaunchDirectly](/deployedge/microsoft-edge-policies#nativehostsexecutableslaunchdirectly) - Force Windows executable Native Messaging hosts to launch directly
- [RelatedWebsiteSetsEnabled](/deployedge/microsoft-edge-policies#relatedwebsitesetsenabled) - Enable Related Website Sets
- [RelatedWebsiteSetsOverrides](/deployedge/microsoft-edge-policies#relatedwebsitesetsoverrides) - Override Related Website Sets
- [PreventTyposquattingPromptOverride](/deployedge/microsoft-edge-policies#preventtyposquattingpromptoverride) - Prevent bypassing Edge Website Typo Protection prompts for sites
- [TyposquattingAllowListDomains](/deployedge/microsoft-edge-policies#typosquattingallowlistdomains) - Configure the list of domains for which Edge Website Typo Protection won't trigger warnings

#### Obsoleted policies

- [SendMouseEventsDisabledFormControlsEnabled](/deployedge/microsoft-edge-policies#sendmouseeventsdisabledformcontrolsenabled) - Control the new behavior for event dispatching on disabled form controls

## Version 120.0.2210.61: December 7, 2023

Fixed various bugs and performance issues.

## Version 120.0.2210.57: December 6, 2023

Fixed various bugs and performance issues.

## Version 120.0.2210.49: December 1, 2023

Fixed various bugs and performance issues.

## Version 120.0.2210.39: November 27, 2023

Fixed various bugs and performance issues.

## Version 120.0.2210.22: November 21, 2023

Fixed various bugs and performance issues.

## Version 120.0.2210.7: November 13, 2023

Fixed various bugs and performance issues.

### Feature updates

- **RendererAppContainer.** For extra security benefits, the Windows native app container is enabled by default. **Note:** If Enterprise organizations identify a compatibility issue due to code injection from security software, they should follow up with the software publisher directly. Alternatively, they can use the [RendererAppContainerEnabled](/deployedge/microsoft-edge-policies#rendererappcontainerenabled) policy to trade off the security benefits in Microsoft Edge with their other software.

- **Updated SmartActionsBlockList Policy.**  The [SmartActionsBlockList](/deployedge/microsoft-edge-policies#smartactionsblocklist) policy is updated with new policy option mappings.  Administrators can now configure the policy to control Smart actions like definitions on websites (smart_actions_website) or control Smart actions in pdfs and on websites (smart_actions).

- **Microsoft Edge Workspaces improvements for offline functionality.**  Any workspace opened on a device previously is cached locally and can be opened on that device from that cache even if it fails to connect. Changes persist on that device and are resolved into the synced version when a connection can finally be made. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

### Policy updates

#### New policies

- [AutoDiscardSleepingTabsEnabled](/deployedge/microsoft-edge-policies#autodiscardsleepingtabsenabled) - Configure auto discard sleeping tabs
- [AutomaticProfileSwitchingSiteList](/deployedge/microsoft-edge-policies#automaticprofileswitchingsitelist) - Configure the automatic profile switching site list
- [Edge3PSerpTelemetryEnabled](/deployedge/microsoft-edge-policies#edge3pserptelemetryenabled) - Edge 3P SERP Telemetry Enabled
- [WebAppSettings](/deployedge/microsoft-edge-policies#webappsettings) - Web App management settings

## Version 119.0.2151.44: November 2, 2023

Fixed various bugs and performance issues.

## Version 119.0.2151.42: November 1, 2023

Fixed various bugs and performance issues.

## Version 119.0.2151.38: October 30, 2023

Fixed various bugs and performance issues.

## Version 119.0.2151.32: October 27, 2023

Fixed various bugs and performance issues.

## Version 119.0.2151.30: October 26, 2023

Fixed various bugs and performance issues.

## Version 119.0.2151.24: October 23, 2023

Fixed various bugs and performance issues.

<!-- Version 119.0.2151.12: October 17, 2023 to Version 118.0.2088.17: September 25, 2023 -->
<!-- Version 118.0.2088.11: September 20, 2023 to Version 117.0.2045.12: August 29, 2023 -->
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
