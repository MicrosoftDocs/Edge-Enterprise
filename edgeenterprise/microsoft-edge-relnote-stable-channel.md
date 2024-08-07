---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 08/07/2024
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

## Version 127.0.2651.86: August 1, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-1-2024).

### Feature update

- **Customize organization branding using the Microsoft Edge management service.** Admins can customize their organization's branding assets onto Edge for Business through the Microsoft Edge management service. This branding can help users signed in with a Microsoft Entra ID more easily differentiate between multiple profiles and browser windows through visual cues on the profile pill, profile flyout, and Edge for Business taskbar icon.

  This Microsoft Edge management service feature gives admins an enhanced experience to configure, preview, and customize how Edge for Business shows the following organization brand assets:

  - Organization name
  - Accent color
  - Organization logo
  - Edge for Business taskbar icon overlay

  For more information, see [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business) and [Organization branding](/deployedge/microsoft-edge-organization-branding).

## Version 126.0.2592.132: August 1, 2024

Fixed various bugs and performance issues for Extended Stable channel.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-1-2024).

## Version 127.0.2651.74: July 25, 2024

Fixed various bugs and performance issues, improved reliability, announcements, feature updates, and policy updates.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#july-25-2024).

### Dev Channel updates

The following Dev channel updates preceded this Stable channel release. The following Dev notes provide detailed information about the changes in each release.

- [Dev Channel update to 127.0.2610.3 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-127-0-2610-3-is-live/m-p/4156565)
- [Dev Channel update to 127.0.2638.2 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-127-0-2638-2-is-live/m-p/4168541)
- [Dev Channel update to 127.0.2651.8 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-127-0-2651-8-is-live/m-p/4173706)

### Improved reliability

- Fixed a browser crash that happened when using the Microsoft Edge Password Generator.  

### Fixes

- **Updated HttpAllowlist policy.** Automatic HTTPS should now respect the [HttpAllowlist](/deployedge/microsoft-edge-policies#httpallowlist) policy, which provides a list of hostnames that HTTP should be permitted on.

- **Resolved issue.** Fixed an issue that prevented the Translate icon in the omnibox from being clickable.

### Announcement

- **SSE3 Requirement.** Microsoft Edge will stop supporting CPUs that lack SSE3 in Microsoft Edge 128. Devices with such CPUs won't receive any more updates. For more information, see [Microsoft Edge Supported Operating Systems](/deployedge/microsoft-edge-supported-operating-systems).

- **Token Binding.** Token Binding uses cryptographic certificates on both ends of the TLS connection in an attempt to close the security gap of bearer tokens, which might be lost or stolen.  We're planning to deprecate Token Binding in Microsoft Edge version 130. The [AllowTokenBindingForUrls](/deployedge/microsoft-edge-policies#allowtokenbindingforurls) policy is deprecated and will be obsolete in Microsoft Edge version 130.  

### Feature updates

- **Removal of mutation events.** Support for mutation events was removed. The [MutationObserver](https://developer.mozilla.org/en-US/docs/Web/API/MutationObserver) API can be used instead. Administrators can use the [MutationEventsEnabled](/deployedge/microsoft-edge-policies#mutationeventsenabled) policy as a temporary workaround. Enterprises should still work to remove their dependencies on these mutation events. For more information, see [Intent to Ship: Deprecate Mutation Events (google.com)](https://groups.google.com/a/chromium.org/g/blink-dev/c/jBEISy1p1XU).

- **Gift Card Redemption History in the Hub.** Users with an MSA or Microsoft Entra ID Linked Account can view and utilize information from gift card redemptions through Pay with Rewards or the Rewards Dashboard. Once a user successfully redeems a gift card with Pay with Rewards, information relating to their gift card (date, card number/pin, redemption status) redemption is added to a Redemption History. This information is located in the Wallet hub. Admins can control availability of this feature using the [EdgeWalletCheckoutEnabled](/deployedge/microsoft-edge-policies#edgewalletcheckoutenabled) policy. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Password Monitor policy update.** When the [PasswordMonitorAllowed](/deployedge/microsoft-edge-policies#passwordmonitorallowed) policy is enabled as mandatory, users won't see the consent screen to turn on the feature. Also, when set to Mandatory enabled, the UI in Settings will be disabled but remain in the 'On' state, and a briefcase icon is made visible next to it with this description displayed on hover - "This setting is managed by your organization."  For more information, see [Password Monitor auto-enabled for users](/deployedge/microsoft-edge-security-password-monitor).

### Policy updates

#### New policies

- [EdgeSidebarAppUrlHostBlockList](/deployedge/microsoft-edge-policies#edgesidebarappurlhostblocklist) - Control which apps cannot be opened in Microsoft Edge sidebar
- [CSSCustomStateDeprecatedSyntaxEnabled](/deployedge/microsoft-edge-policies#csscustomstatedeprecatedsyntaxenabled) - Controls whether the deprecated :--foo syntax for CSS custom state is enabled

#### Deprecated policies

- [SignInCtaOnNtpEnabled](/deployedge/microsoft-edge-policies#signinctaonntpenabled) - Enable sign in click to action dialog (deprecated)

#### Obsolete policies

- [ImmersiveReaderPictureDictionaryEnabled](/deployedge/microsoft-edge-policies#immersivereaderpicturedictionaryenabled) - Enable Picture Dictionary feature within Immersive Reader in Microsoft Edge (obsolete)
- [EdgeFollowEnabled](/deployedge/microsoft-edge-policies#edgefollowenabled) - Enable Follow service in Microsoft Edge (obsolete)

## Version 126.0.2592.113: July 18, 2024

Fixed various bugs and performance issues, improved reliability.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#july-18-2024).

### Improved reliability

- Fixed a renderer crash (STATUS_ACCESS_VIOLATION) that occurred when using some sites with web contents accessibility enabled, including on the Azure portal or Intune dashboard.

### Fixes

- Resolved an issue that allowed the Microsoft Edge New Tab Page feed to be activated even when the [NewTabPageContentEnabled](/deployedge/microsoft-edge-policies#newtabpagecontentenabled) policy was set to disabled.

## Version 126.0.2592.102: July 11, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#july-11-2024).

## Version 126.0.2592.87: July 2, 2024

Fixed various bugs and performance issues, improved reliability.

### Improved reliability

- Fixed a browser crash that occurred when an on-premises sync user deleted a Favorite.

## Version 126.0.2592.81: June 27, 2024

Fixed various bugs and performance issues, improved reliability.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-27-2024).

### Improved reliability

- Fixed a browser crash that occurred when a user interacted with a drop-down list with over 1,000 items.

### Fixes

- Resolved an issue that affected printing after scrolling down a webpage.  This fix adjusts for scroll offset when printing.

## Version 126.0.2592.68: June 20, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-20-2024).

## Version 126.0.2592.61: June 17, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.56: June 13, 2024

Fixed various bugs and performance issues, feature updates, and policy updates.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-13-2024).

### Dev Channel updates

The following Dev channel updates preceded this Stable channel release. The following Dev notes provide detailed information about the changes in each release.

- [Dev Channel update to 126.0.2552.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-126-0-2552-0-is-live/m-p/4131066)
- [Dev Channel update to 126.0.2566.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-126-0-2566-1-is-live/m-p/4133928)
- [Dev Channel update to 126.0.2578.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-126-0-2578-1-is-live/m-p/4144544)
- [Dev Channel update to 126.0.2592.11 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-126-0-2592-11-is-live/m-p/4154323)

### Feature updates

- **AI theme generator.** Microsoft Edge includes an AI theme generator that allows users to input a text prompt and generate a series of images to preview as browser themes. Applying the theme includes setting the generated image on the Edge new tab page and applying the image's dominant color to the browser frame. Admins can control availability to this feature using the [AIGenThemesEnabled](/deployedge/microsoft-edge-policies#aigenthemesenabled) policy. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Security setting controls in the Microsoft Edge management service.** The Microsoft Edge management service will provide admins with a dedicated experience to manage specific settings that help improve the security posture of their managed browser instances. **Note:** This experience is in public preview and can be accessed by opting in to targeted release in the Microsoft 365 admin center.

- **Copilot summarization notification.** The feature displays an Omnibox notification when users enter into a reading mode eligible page in Edge and offers them the option to open Copilot in the sidebar to generate a summary of the content. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

### Policy updates

#### New policies

- [ProactiveAuthWorkflowEnabled](/deployedge/microsoft-edge-policies#proactiveauthworkflowenabled) - Enable proactive authentication
- [InternetExplorerSetForegroundWhenActive](/deployedge/microsoft-edge-policies#internetexplorersetforegroundwhenactive) - Keep the active Microsoft Edge window with an Internet Explorer mode tab always in the foreground.

#### Obsoleted policies

- [MathSolverEnabled](/deployedge/microsoft-edge-policies#mathsolverenabled) - Let users snip a Math problem and get the solution with a step-by-step explanation in Microsoft Edge (obsolete)
- [ImmersiveReaderGrammarToolsEnabled](/deployedge/microsoft-edge-policies#immersivereadergrammartoolsenabled) - Enable Grammar Tools feature within Immersive Reader in Microsoft Edge (obsolete)

## Version 125.0.2535.92: June 6, 2024

Fixed various bugs and performance issues.

## Version 124.0.2478.131: June 4, 2024

Fixed various bugs and performance issues for Extended Stable channel.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-3-2024).

## Version 125.0.2535.85: June 3, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-3-2024).

**Announcement**

Microsoft Defender Application Guard extension deprecation. Because Application Guard is deprecated, there won't be a migration to Edge Manifest V3. The corresponding extensions and associated [Windows Store app](https://apps.microsoft.com/detail/9n8gnlc8z9c8?hl=en-us&gl=US) will not be available after May 2024. This affects the following browsers: [Application Guard Extension - Chrome](https://chromewebstore.google.com/detail/application-guard-extensi/mfjnknhkkiafjajicegabkbimfhplplj) and [Application Guard Extension - Firefox](https://addons.mozilla.org/en-US/firefox/extensions/). If you want to block unprotected browsers until you're ready to retire MDAG usage in your enterprise, we recommend using AppLocker policies or [Microsoft Edge management service](/deployedge/microsoft-edge-management-service). For more information, see [Microsoft Edge and Microsoft Defender Application Guard](/deployedge/microsoft-edge-security-windows-defender-application-guard), [Deprecated features in the Windows client - What's new in Windows](/windows/whats-new/deprecated-features), and [Microsoft Defender Application Guard - Windows Security](/windows/security/application-security/application-isolation/microsoft-defender-application-guard/md-app-guard-overview).


## Version 124.0.2478.127: May 30, 2024

Fixed various bugs and performance issues for Extended Stable channel.

> [!IMPORTANT]
> This update to Extended Stable channel contains a fix for [CVE-2024-5274](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2024-5274), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-24-2024).

<!--------------------------------------------------------------->
## Version 125.0.2535.79: May 30, 2024

Fixed various bugs and performance issues, improved reliability.

**Announcement**

Microsoft Defender Application Guard extension deprecation. Because Application Guard is deprecated, there won't be a migration to Edge Manifest V3. The corresponding extensions and associated [Windows Store app](https://apps.microsoft.com/detail/9n8gnlc8z9c8?hl=en-us&gl=US) will not be available after May 2024. This affects the following browsers: [Application Guard Extension - Chrome](https://chromewebstore.google.com/detail/application-guard-extensi/mfjnknhkkiafjajicegabkbimfhplplj) and [Application Guard Extension - Firefox](https://addons.mozilla.org/en-US/firefox/extensions/). If you want to block unprotected browsers until you're ready to retire MDAG usage in your enterprise, we recommend using AppLocker policies or [Microsoft Edge management service](/deployedge/microsoft-edge-management-service). For more information, see [Microsoft Edge and Microsoft Defender Application Guard](/deployedge/microsoft-edge-security-windows-defender-application-guard), [Deprecated features in the Windows client - What's new in Windows](/windows/whats-new/deprecated-features), and [Microsoft Defender Application Guard - Windows Security](/windows/security/application-security/application-isolation/microsoft-defender-application-guard/md-app-guard-overview).

### Improved reliability

- Fixed a browser crash which occurred on startup in cases where the profile information was cached in an incorrect format.

### Fixes

- Resolved an issue which affected the "View in File Explorer" option in SharePoint Online.  

<!--------------------------------------------------------------->
## Version 125.0.2535.67: May 24, 2024

Fixed various bugs and performance issues.

> [!IMPORTANT]
> This update to Stable channel contains a fix for [CVE-2024-5274](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2024-5274), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-24-2024).

**Announcement**

Microsoft Defender Application Guard extension deprecation. Because Application Guard is deprecated, there won't be a migration to Edge Manifest V3. The corresponding extensions and associated [Windows Store app](https://apps.microsoft.com/detail/9n8gnlc8z9c8?hl=en-us&gl=US) will not be available after May 2024. This affects the following browsers: [Application Guard Extension - Chrome](https://chromewebstore.google.com/detail/application-guard-extensi/mfjnknhkkiafjajicegabkbimfhplplj) and [Application Guard Extension - Firefox](https://addons.mozilla.org/en-US/firefox/extensions/). If you want to block unprotected browsers until you're ready to retire MDAG usage in your enterprise, we recommend using AppLocker policies or [Microsoft Edge management service](/deployedge/microsoft-edge-management-service). For more information, see [Microsoft Edge and Microsoft Defender Application Guard](/deployedge/microsoft-edge-security-windows-defender-application-guard), [Deprecated features in the Windows client - What's new in Windows](/windows/whats-new/deprecated-features), and [Microsoft Defender Application Guard - Windows Security](/windows/security/application-security/application-isolation/microsoft-defender-application-guard/md-app-guard-overview).

### Improved reliability

- Fixed a browser crash/hang which occurred when trying to select from a drop-down list with a large number of options.

## Version 124.0.2478.121: May 24, 2024

Fixed various bugs and performance issues for Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-24-2024).

## Version 125.0.2535.51: May 17, 2024

Fixed various bugs and performance issues, includes feature and policy updates.

> [!IMPORTANT]
> This update to Stable channel contains a fix for [CVE-2024-4947](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2024-4947), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-17-2024).

### Dev Channel updates

The following Dev channel updates preceded this Stable channel release. The following Dev notes provide detailed information about the changes in each release.

- [Dev Channel update to 125.0.2492.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-125-0-2492-1-is-live/m-p/4103542)
- [Dev Channel update to 125.0.2506.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-125-0-2506-0-is-live/m-p/4113302)
- [Dev Channel update to 125.0.2518.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-125-0-2518-0-is-live/m-p/4117088)

**Announcement**

Microsoft Defender Application Guard extension deprecation. Because Application Guard is deprecated, there won't be a migration to Edge Manifest V3. The corresponding extensions and associated [Windows Store app](https://apps.microsoft.com/detail/9n8gnlc8z9c8?hl=en-us&gl=US) will not be available after May 2024. This affects the following browsers: [Application Guard Extension - Chrome](https://chromewebstore.google.com/detail/application-guard-extensi/mfjnknhkkiafjajicegabkbimfhplplj) and [Application Guard Extension - Firefox](https://addons.mozilla.org/en-US/firefox/extensions/). If you want to block unprotected browsers until you're ready to retire MDAG usage in your enterprise, we recommend using AppLocker policies or [Microsoft Edge management service](/deployedge/microsoft-edge-management-service). For more information, see [Microsoft Edge and Microsoft Defender Application Guard](/deployedge/microsoft-edge-security-windows-defender-application-guard), [Deprecated features in the Windows client - What's new in Windows](/windows/whats-new/deprecated-features), and [Microsoft Defender Application Guard - Windows Security](/windows/security/application-security/application-isolation/microsoft-defender-application-guard/md-app-guard-overview).

### Feature Updates

- **Improved user experience for Purview copy/paste controls in Edge.** Our Purview cut/copy/paste experience is now more user friendly with self-dismissing dialogs on successful paste. The existing "Paste to supported browsers" setting allows organizations to classify and protect the content that end users can paste – both to specific websites and through supported browsers. You can follow the instructions in [Use Endpoint data loss prevention (DLP)](/purview/endpoint-dlp-using?tabs=purview#create-your-dlp-policy) to create the DLP policy.

- **New Workspaces color display: browser window outline.** Workspaces each have a dedicated color, and that color is now displayed as an outline on the browser window. The previous experience applied the color across the entire tab strip in horizontal tab orientation, and across the title bar in vertical tab orientation. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Full Favorites Bar available in Workspaces.** Workspaces now display a user's full set of favorites in the Favorites Bar, with a dedicated workspace folder accessible from the bar. The previous experience replaced the Favorites Bar with the workspace favorites folder. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

### Policy updates

#### New policies

- [ZstdContentEncodingEnabled](/deployedge/microsoft-edge-policies#zstdcontentencodingenabled) - Enable zstd content encoding support
- [QRCodeGeneratorEnabled](/deployedge/microsoft-edge-policies#qrcodegeneratorenabled) - Enable QR Code Generator

#### Deprecated policies

- [AllowTokenBindingForUrls](/deployedge/microsoft-edge-policies#allowtokenbindingforurls) - Configure the list of sites for which Microsoft Edge will attempt to establish a Token Binding with (deprecated)

<!-- Version 124.0.2478.109: May 16, 2024 to Version 124.0.2478.51: April 18, 2024 -->
<!-- ===================== snip for archive ========================== -->
<!-- Version 123.0.2420.97: April 12, 2024 to Version 123.0.2420.53: March 22, 2024 -->
<!-- Version 122.0.2365.106: March 21, 2024 to Version 120.0.2210.181: February 20, 2024 -->
<!-- Version 121.0.2277.128: February 15, 2024 to Version 118.0.2088.122: November 29, 2023 -->
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
