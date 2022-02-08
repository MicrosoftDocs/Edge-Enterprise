---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 02/07/2022
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

## Version 98.0.1108.23: January 14

### Feature updates

- **Enhance your security on the web.** A browsing mode in Microsoft Edge where the security of your browser takes priority, giving you an extra layer of protection when browsing the web. Administrators can apply the following Group Policies to end-user desktops (Windows, macOS, and Linux) to help protect against zero days. These policies also make that important sites and line of business applications continue to work as expected. This feature is a huge step forward because it lets us mitigate unforeseen active zero days (based on historical trends). When turned on, this feature brings Hardware-enforced Stack Protection, Arbitrary Code Guard (ACG), and Content Flow Guard (CFG) as supporting security mitigations to increase users' security on the web.
Group Policies:
  - [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode)
  - [EnhanceSecurityModeBypassListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains)
  - [EnhanceSecurityModeEnforceListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains)

- **Custom primary password.** The browser already has the capability where users can add an authentication step before saved passwords are auto-filled in web forms. This adds another layer of privacy and helps prevent unauthorized users from using saved passwords to log on websites. Custom primary password is an evolution of that same feature, where users will now be able to use a custom string of their choice as their primary password. After it's enabled, users will enter this password to authenticate themselves and have their saved passwords auto filled into web forms.

- **Overlay scrollbars added to Microsoft Edge.** We've updated our scrollbars with an overlay-based design. Users can turn this feature on in *edge://flags*.

### Policy updates

#### New Policies

- [AddressBarEditingEnabled](/DeployEdge/microsoft-edge-policies#addressbareditingenabled) - Configure address bar editing.
- [EdgeFollowEnabled](/DeployEdge/microsoft-edge-policies#edgefollowenabled) - Enable Follow service in Microsoft Edge.
- [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode) - Enhance the security state in Microsoft Edge.
- [EnhanceSecurityModeBypassListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains) - Configure the list of domains for which enhance security mode will not be enforced.
- [EnhanceSecurityModeEnforceListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains) - Configure the list of domains for which enhance security mode will always be enforced.
- [InAppSupportEnabled](/DeployEdge/microsoft-edge-policies#inappsupportenabled) - In-app support Enabled.
- [MicrosoftEdgeInsiderPromotionEnabled](/DeployEdge/microsoft-edge-policies#microsoftedgeinsiderpromotionenabled) - Microsoft Edge Insider Promotion Enabled.
- [PrintStickySettings](/DeployEdge/microsoft-edge-policies#printstickysettings) - Print preview sticky settings.
- [SandboxExternalProtocolBlocked](/DeployEdge/microsoft-edge-policies#sandboxexternalprotocolblocked) - Allow Microsoft Edge to block navigations to external protocols in a sandboxed iframe.
- [U2fSecurityKeyApiEnabled](/DeployEdge/microsoft-edge-policies#u2fsecuritykeyapienabled) - Allow using the deprecated U2F Security Key API.

## Version 97.0.1072.54: January 5

Fixed various bugs and performance issues.

## Version 97.0.1072.52: January 3

Fixed various bugs and performance issues.

## Version 97.0.1072.41: December 20

Fixed various bugs and performance issues.

## Version 97.0.1072.34: December 13

Fixed various bugs and performance issues.

## Version 97.0.1072.28: December 8

Fixed various bugs and performance issues.

<!--- Version 97.0.1072.21: December 1 to Version 96.0.1054.13: November 5  --->
<!--- archive from Version 96.0.1054.8: November 1 to Version 95.0.1020.14: October 5  --->
<!-- archive from version 95.0.1020.9: September 28 to version 94.0.992.14: September 7 ---->
<!-- archive from Version 94.0.992.9: September 2 to Version 92.0.902.40: July 6 -->
<!--Archive on Oct 27 From Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
