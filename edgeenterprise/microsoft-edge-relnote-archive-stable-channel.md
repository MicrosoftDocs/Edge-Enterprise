---
title: "Archived release notes for Microsoft Edge Stable Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 10/17/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Archived release notes for Microsoft Edge Stable Channel"
---

# Archived release notes for Microsoft Edge Stable Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Stable Channel. All the security updates are listed [here](microsoft-edge-relnotes-security.md).

<!-- Version 127.0.2651.105: August 15, 2024 to Version 127.0.2651.74: July 25, 2024 --->
## Version 127.0.2651.105: August 15, 2024

Fixed various bugs and performance issues, improved reliability.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-15-2024).

### Improved reliability
 
- Fixed a browser crash (STATUS_BREAKPOINT) that occurred when trying to upload documents on some websites.

## Version 126.0.2592.137: August 8, 2024

Fixed various bugs and performance issues for Extended Stable channel.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-8-2024).

## Version 127.0.2651.98: August 8, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-8-2024).

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

<!-- Version 126.0.2592.113: July 18, 2024 to Version 126.0.2592.61: June 17, 2024 --->

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

<!-- Version 126.0.2592.56: June 13, 2024 to version 125.0.2535.51: May 17, 2024 -->

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
## Version 124.0.2478.109: May 16, 2024

> [!IMPORTANT]
> This update to Stable channel (and Extended Stable channel) contains a fix for [CVE-2024-4947](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2024-4947), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-16-2024).

## Version 124.0.2478.105: May 14, 2024

> [!IMPORTANT]
> This update to Stable channel (and Extended Stable channel) contains a fix for [CVE-2024-4761](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2024-4761), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-14-2024).

## Version 124.0.2478.97: May 10, 2024

> [!IMPORTANT]
> This update to Stable channel (and Extended Stable channel) contains a fix for [CVE-2024-4671](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2024-4671), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-10-2024).

## Version 124.0.2478.80: May 2, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-2-2024).

### Feature updates

- **Sidebar Tools App - SpeedTest.** Adding a SpeedTest answer by default to the Tools app in the Microsoft Edge sidebar. For more information, see [Manage the sidebar in Microsoft Edge](/deployedge/microsoft-edge-sidebar).

## Version 124.0.2478.67: April 26, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-26-2024).

**Announcement: Insecure downloads over HTTP**

Users that download potentially dangerous content on HTTP sites will receive a UI warning, (for example, "sample.exe can't be downloaded securely"). The user can still choose to proceed by selecting "Keep" on the downloaded item's "..." menu. Admins can also use the [InsecureContentAllowedForUrls](/deployedge/microsoft-edge-policies#insecurecontentallowedforurls) policy to specify HTTP sites where the warning will be suppressed. The warning's enablement in Edge 124 was accidental. We have reverted the warning in this Stable Release. Admins can use the `InsecureDownloadWarnings` feature flag to test the impact of this upcoming feature. **Note:** The warning is planned to be turned on in a future Microsoft Edge version. (***Announcement updated May 9, 2024***)

### Fixes

- Removes "Microsoft chat provider for Copilot in Windows" from Windows Server devices. The component was incorrectly installed on some devices in a previous Microsoft Edge update.

### Feature updates

- **Email notifications for extension requests in the Microsoft Edge management service.** The Microsoft Edge management service now provides admins with the ability to receive email notifications for extensions that their users have requested. Once enabled, this will help inform them promptly of any new pending requests that they may have.

## Version 124.0.2478.51: April 18, 2024

Fixed various bugs and performance issues, improved reliability.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-18-2024).

### Dev Channel updates

The following Dev channel updates preceded this Stable channel release. The following Dev notes provide detailed information about the changes in each release.

- [Dev Channel update to 124.0.2438.2 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-124-0-2438-2-is-live/m-p/4079136)
- [Dev Channel update to 124.0.2450.2 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-124-0-2450-2-is-live/m-p/4085888)
- [Dev Channel update to 124.0.2464.2 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-124-0-2464-2-is-live/m-p/4092459)
- [Dev Channel update to 124.0.2478.6 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-124-0-2478-6-is-live/m-p/4097816)

### Feature updates

- **Email notifications for extension requests in the Microsoft Edge management service.** The Microsoft Edge management service provides admins with the ability to receive email notifications for extensions that their users requested. This notification helps inform them promptly of any new feedback. **Note:** This experience is in public preview and can be accessed by opting in to targeted release in the Microsoft 365 admin center.

- **Enterprise secure AI controls in the Microsoft Edge management service.** The Microsoft Edge management service now provides a new dedicated space for admins to manage all AI-related policies in the Edge browser. This helps enhance security and productivity for managed users and devices.

- **Customize organization branding using the Microsoft Edge management service.** Admins can customize their organization's branding assets onto Edge for Business through the Microsoft Edge management service. This branding can help users signed in with a Microsoft Entra ID more easily differentiate between multiple profiles and browser windows through visual cues on the profile pill, profile flyout, and Edge for Business taskbar icon.

  This Microsoft Edge management service feature gives admins an enhanced experience to configure, preview, and customize how Edge for Business shows the following organization brand assets:

  - Organization name
  - Accent color
  - Organization logo
  - Edge for Business taskbar icon overlay

  **Note:** This experience is in public preview and can be accessed by opting in to targeted release in the Microsoft 365 admin center. For more information, see [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business) and [Organization branding](/deployedge/microsoft-edge-organization-branding).

- **Automatic profile switching controls for Microsoft Edge for Business in the Microsoft Edge management service.** The Microsoft Edge management service provides admins with the ability to configure settings for automatic profile switching in the Microsoft Edge browser. This can help enforce context separation between their end users' work and personal browsing.

- **Updated Edge Profile account re-authentication popup when Browser to Web Single-Sign-On (SSO) fails.** Edge provides a browser to Web single sign-on (SSO) capability that lets a user sign in to their Edge Profile with a web account first and then automatically sign them into Microsoft first party websites.

  This is done by saving cached credentials. This approach works until there's an authentication challenge to the cached credentials. A typical scenario is when a user changes their password on a different device. The cached credentials on the current device become outdated and SSO fails. Edge detects this failure and shows a re-authentication popup that prompts the user to update their cached credentials on the current device.

- **Removal of Web SQL -  Web SQL support is completely removed.** In prior releases, Web SQL support was disabled by default but could be re-enabled via the [WebSQLAccess](/deployedge/microsoft-edge-policies?branch=pr-en-us-4103#websqlaccess) policy. After this change, there is no longer any mechanism to enable Web SQL support. This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, see [Intent to Deprecate and Remove Web SQL](https://groups.google.com/a/chromium.org/g/blink-dev/c/fWYb6evVA-w/m/pziWcvboAgAJ).

- **Cross-device Search Query History suggestions.**  The existing Search Query suggestions have been enhanced with cross-device query history in both Recent Searches and browser searches for enterprise users who have enabled Edge Sync across devices/browsers. From now on Edge will provide you with the relevant query history suggestions that you have previously searched before no matter where you did it. You can always trust Edge to help you quickly re-find the information that you accessed before.

- **Extending support for viewing MIP Protected PDF Files to different sovereignties (including GCCH).** Sovereign cloud customers (including GCCH) will be able to open MIP protected PDF content in Microsoft Edge. This change will be available in the Microsoft Edge built-in PDF reader powered by Adobe Acrobat and the legacy Microsoft Edge PDF engine. **Note:** This feature is an experiment.  Admins can use the feature flag "**msMIPSovereigntyPdfViewSupport**" to test this feature.  

- **Copilot browser Context Policies.**
 To summarize and answer questions based on browser context in Microsoft Edge, Copilot needs to be able to access the browser context. We're providing two new policies to offer more flexibility for admins to customize Edge browser context access across Copilot chats in Edge sidebar.

   - [CopilotPageContext](/deployedge/microsoft-edge-policies#copilotpagecontext) - Control Copilot access to browser context for Microsoft Entra ID profiles.
   - [CopilotCDPPageContext](/deployedge/microsoft-edge-policies#copilotcdppagecontext) - Control Copilot with Commercial Data Protection access to browser context for Microsoft Entra ID profiles.
   - The [DiscoverPageContextEnabled](/deployedge/microsoft-edge-policies#discoverpagecontextenabled) policy is deprecated in Edge version 124 and will be obsoleted in Edge version 127.

- **Inline Compose.** This feature allows users to rewrite text using Copilot. Users can highlight text they'd like to improve when writing in Edge and use the Rewrite tool to iterate with different lengths, formats, and tones. Administrators can control availability using the [ComposeInlineEnabled](/deployedge/microsoft-edge-policies#composeinlineenabled) policy.

- **Updated profile management and customization controls.**
Enhancing the profile management and customization experience through surfaced profile controls and an expanded range of default avatars. With these updates, users can effortlessly tailor their profiles to their preferences and select from a broader collection of profile avatars.

- **Microsoft Edge migrates the updates experience into Browser Essentials.** Notifications on available Edge Updates will come from Browser Essentials instead of the Settings page for better visibility and experience.

- **Desktop Shortcut for New Enterprise Devices.** New Microsoft Enterprise devices, including Windows Enterprise SKUs, Windows Server SKUs and any domain-joined or AAD-joined devices, running through Windows Out of Box Experience (OOBE) for the first time will see a Microsoft Edge desktop shortcut automatically created. This desktop shortcut provides users with an alternative way to access their Microsoft Edge browser without needing to manually pin and configure their set-up.

- **Updated profile options in new profile experience.** Many users unintentionally create empty profiles, cluttering their workspace and impeding their browsing experience. To reduce clutter and the likelihood of profile churn, updated First Run Experience (FRE) string options encourage users to sign-in and meaningfully create profiles for an improved browsing experience, or easily cancel unintentional creation.

- **Updated default profile pill for EDU users in Edge for Business.** To improve the applicability of the current Edge for Business default visuals, users signed in with an EDU account will see the default profile pill label updated to "School".

- **Updated UX for Microsoft Defender for Endpoint blocks.** Microsoft Edge now provides a different blocking experience for Microsoft Defender for Endpoint based blocks (Web Content Filtering and Custom Indicators). For more information, see [Web protection](/microsoft-365/security/defender-endpoint/web-protection-overview?view=o365-worldwide&preserve-view=true).

### Policy updates

#### New policies

- [CopilotCDPPageContext](/deployedge/microsoft-edge-policies#copilotcdppagecontext) - Control Copilot with Commercial Data Protection access to browser context for Microsoft Entra ID profiles
- [CopilotPageContext](/deployedge/microsoft-edge-policies#copilotpagecontext) - Control Copilot access to browser context for Microsoft Entra ID profiles
- [MutationEventsEnabled](/deployedge/microsoft-edge-policies#mutationeventsenabled) - Enable deprecated/removed Mutation Events

#### Deprecated policies

- [DiscoverPageContextEnabled](/deployedge/microsoft-edge-policies#discoverpagecontextenabled) - Enable Discover access to page contents for AAD profiles (deprecated)

#### Obsoleted policies

- [ThrottleNonVisibleCrossOriginIframesAllowed](/deployedge/microsoft-edge-policies#throttlenonvisiblecrossoriginiframesallowed) - Allows enabling throttling of non-visible, cross-origin iframes (obsolete)
- [WebSQLAccess](/deployedge/microsoft-edge-policies#websqlaccess) - Force WebSQL to be enabled (obsolete)


<!-- Version 123.0.2420.97: April 12, 2024 to Version 123.0.2420.53: March 22, 2024 -->
## Version 123.0.2420.97: April 12, 2024

Fixed various bugs and performance issues, improved reliability.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-12-2024).

### Improved reliability

- Fixed a browser crash that was related to Microsoft Edge Sync.
  
## Version 123.0.2420.81: April 4, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-4-2024).

### Fixes

- Resolved an issue when using the Microsoft Edge built-in PDF reader powered by Adobe Acrobat caused fillable PDF form fields to not auto resize correctly when entering large text strings.

## Version 122.0.2365.120: April 4, 2024

Fixed various bugs and performance issues for Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-4-2024).

## Version 123.0.2420.65: March 27, 2024

Fixed various bugs and performance issues, includes security fixes, and improves reliability.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-29-2024).

### Improved reliability

- Fixed a browser crash that occurred when the **UserDataDir** policy is used to specify a path on a network share. Using a network share location for the user data directory is unsupported.

## Version 122.0.2365.113: March 27, 2024

Fixed various bugs and performance issues for Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-29-2024).

## Version 123.0.2420.53:  March 22, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-22-2024).

### Dev Channel updates

The following Dev channel updates preceded this Stable channel release. The following Dev notes provide detailed information about the changes in each release.

- [Dev Channel update to 123.0.2380.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-123-0-2380-1-is-live/m-p/4050755)
- [Dev Channel update to 123.0.2400.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-123-0-2400-1-is-live/m-p/4058807)
- [Dev Channel update to 123.0.2420.6 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-123-0-2420-6-is-live/m-p/4069388)

### Feature updates

- **Customize organization branding using the Microsoft Edge management service.** Admins can customize their organization's branding assets onto Edge for Business through the Microsoft Edge management service. This branding can help users signed in with a Microsoft Entra ID more easily differentiate between multiple profiles and browser windows through visual cues on the profile pill, profile flyout, and Microsoft Edge for Business taskbar icon.

  This Microsoft Edge management service feature gives admins an enhanced experience to configure, preview, and customize how Edge for Business shows the following organization brand assets:

  - Organization name
  - Accent color
  - Organization logo
  - Edge for Business taskbar icon overlay

  **Note:** This experience is in public preview and can be accessed by opting in to targeted release in the M365 admin center. For more information, see [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business).

- **Automatic profile switching controls for Microsoft Edge for Business in the Microsoft Edge management service.** The Microsoft Edge management service will provide admins with the ability to configure settings for automatic profile switching in the Microsoft Edge browser. This can help enforce context separation between their end users' work and personal browsing. **Note:** This experience is in public preview and can be accessed by opting in to targeted release in the M365 admin center.

### Policy updates

#### New policies

- [AccessControlAllowMethodsInCORSPreflightSpecConformant](/deployedge/microsoft-edge-policies#accesscontrolallowmethodsincorspreflightspecconformant) - Make Access-Control-Allow-Methods matching in CORS preflight spec conformant
- [AdditionalSearchBoxEnabled](/deployedge/microsoft-edge-policies#additionalsearchboxenabled) - Enable another search box in browser
- [AllowBackForwardCacheForCacheControlNoStorePageEnabled](/deployedge/microsoft-edge-policies#allowbackforwardcacheforcachecontrolnostorepageenabled) - Allow pages with Cache-Control: no-store header to enter back/forward cache
- [AllowWebAuthnWithBrokenTlsCerts](/deployedge/microsoft-edge-policies#allowwebauthnwithbrokentlscerts) - Allow Web Authentication requests on sites with broken TLS certificates.
- [BlockTruncatedCookies](/deployedge/microsoft-edge-policies#blocktruncatedcookies) - Block truncated cookies
- [DefaultWindowManagementSetting](/deployedge/microsoft-edge-policies#defaultwindowmanagementsetting) - Default Window Management permission setting
- [ExtensionInstallTypeBlocklist](/deployedge/microsoft-edge-policies#extensioninstalltypeblocklist) - Blocklist for extension install types
- [ExtensionManifestV2Availability](/deployedge/microsoft-edge-policies#extensionmanifestv2availability) - Control Manifest v2 extension availability
- [FileOrDirectoryPickerWithoutGestureAllowedForOrigins](/deployedge/microsoft-edge-policies#fileordirectorypickerwithoutgestureallowedfororigins) - Allow file or directory picker APIs to be called without prior user gesture
- [HttpAllowlist](/deployedge/microsoft-edge-policies#httpallowlist) - HTTP Allowlist
- [NewBaseUrlInheritanceBehaviorAllowed](/deployedge/microsoft-edge-policies#newbaseurlinheritancebehaviorallowed) - Allows enabling the feature NewBaseUrlInheritanceBehavior 
- [RequireOnlineRevocationChecksForLocalAnchors](/deployedge/microsoft-edge-policies#requireonlinerevocationchecksforlocalanchors) - Specify if online OCSP/CRL checks are required for local trust anchors
- [RSAKeyUsageForLocalAnchorsEnabled](/deployedge/microsoft-edge-policies#rsakeyusageforlocalanchorsenabled) - Check RSA key usage for server certificates issued by local trust anchors
- [ScreenCaptureWithoutGestureAllowedForOrigins](/deployedge/microsoft-edge-policies#screencapturewithoutgestureallowedfororigins) - Allow screen capture without prior user gesture
- [WindowManagementAllowedForUrls](/deployedge/microsoft-edge-policies#windowmanagementallowedforurls) - Allow Window Management permission on specified sites
- [WindowManagementBlockedForUrls](/deployedge/microsoft-edge-policies#windowmanagementblockedforurls) - Block Window Management permission on specified sites

<!-- Version 122.0.2365.106: March 21, 2024 to Version 120.0.2210.181: February 20, 2024 -->

## Version 122.0.2365.106: March 21, 2024

Fixed various bugs and performance issues for Extended Stable channel.

## Version 122.0.2365.92:  March 14, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-14-2024).

## Version 122.0.2365.80:  March 7, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-7-2024).

### Improved reliability

- Fixed a browser crash that occurred when the [BrowsingDataLifetime](/deployedge/microsoft-edge-policies#browsingdatalifetime) policy was enabled.

## Version 122.0.2365.66: March 1, 2024

Fixed various bugs and performance issues.

### Fixes

- Resolved a network issue that prevented sites from loading within a Microsoft Defender Application Guard window.

## Version 122.0.2365.63: February 29, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#february-29-2024).

## Version 122.0.2365.59: February 27, 2024

Fixed various bugs and performance issues.

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

- **Moving Managed Site Indicator (Briefcase icon) into the lock icon in the address bar omnibox.** The briefcase icon, which signals that a page is managed via admin policies, was moved into the lock icon in the address bar. End users can view details about the protections for a given page by clicking the lock icon in the address bar and then clicking the briefcase icon. For more information, see [Understand Data loss Prevention in Microsoft Edge](/deployedge/microsoft-edge-security-dlp).

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

<!-- Version 121.0.2277.128: February 15, 2024 to Version 118.0.2088.122: November 29, 2023 -->
## Version 121.0.2277.128: February 15, 2024

Fixed various bugs and performance issues.

### Fixes

- Edge has a feature that provides an option to import browser data on each launch from other browsers with user consent. This feature's state might not have been syncing and displaying correctly across multiple devices. This is fixed.

### Policy updates

#### Additional policy changes

- [EdgeManagementPolicyOverridesPlatformPolicy](/deployedge/microsoft-edge-policies#edgemanagementpolicyoverridesplatformpolicy) - For Microsoft Edge version 121.0.2277 and later, this policy controls all device policies.
- [EdgeManagementUserPolicyOverridesCloudMachinePolicy](/deployedge/microsoft-edge-policies#edgemanagementuserpolicyoverridescloudmachinepolicy)  - For Microsoft Edge version 121.0.2277 and later, this policy controls all per user profile policies.

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

- Fixed a browser crash in on-premises sync

### Dev Channel updates

The following Dev channel updates preceded this Stable channel release. The following  Dev notes provide detailed information about the changes in each release.

- [Dev Channel update to 121.0.2274.0 is live - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/discussions/dev-channel-update-to-121-0-2274-0-is-live/m-p/4010747)
- [Dev Channel update to 121.0.2256.2 is live - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/discussions/dev-channel-update-to-121-0-2256-2-is-live/m-p/4004721)
- [Dev Channel update to 121.0.2248.1 is live - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/discussions/dev-channel-update-to-121-0-2248-1-is-live/m-p/3998824)
- [Dev Channel update to 121.0.2220.3 is live - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/discussions/dev-channel-update-to-121-0-2220-3-is-live/m-p/3986444)

### Feature updates

- **Enable organization branding in Edge for Business.**   Enable your organization's branding assets from Entra onto profile-related UI for profiles signed in with a Microsft Entra ID account. You can add your organization's details such as name to the profile pill, name and brand color to the profile flyout, and logo to overlay the Edge for Business taskbar icon. This branding can help users more easily differentiate between multiple profiles and browser windows.

  Default organization branding can be enabled by admins through the following policies:

  - [OrganizationalBrandingOnWorkProfileUIEnabled](/deployedge/microsoft-edge-policies#organizationalbrandingonworkprofileuienabled
)
  - [OrganizationLogoOverlayOnAppIconEnabled](/deployedge/microsoft-edge-policies#organizationlogooverlayonappiconenabled)

  Admins need to have "company branding" assets configured in the Microsoft Entra admin center for branding assets to be applied to this feature.

  For more information, see [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business) and [Add company branding to your organization's sign-in page](/entra/fundamentals/how-to-customize-branding).

- **Microsoft Edge migrates the updates experience into Browser Essentials.** Getting alerts on available Edge Updates will come from Browser Essentials instead of the Settings page for better visibility and experience. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Added support for AVIF and AV1 file formats.** Microsoft Edge now supports the AVIF and AV1 file formats, which offer better compression and higher quality images and videos.  Users can enjoy faster loading times and better quality media on websites.  

- **E-tree in Wallet.** Users signed into Microsoft Edge with a personal Microsoft Account (MSA) can grow a virtual seed into a tree with Wallet. Once it's grown, a real tree is planted.  Administrators can control the availability using the [EdgeWalletEtreeEnabled](/deployedge/microsoft-edge-policies#edgewalletetreeenabled) policy.

- **New Website Typo Protection policies.** The built-in Website Typo Protection warns users if it appears there's a mistyped popular domain name that could land users on a malicious webpage.  Administrators can control the availability and configure Website Typo Protection by using the [PreventTyposquattingPromptOverride](/deployedge/microsoft-edge-policies#preventtyposquattingpromptoverride) and [TyposquattingAllowListDomains](/deployedge/microsoft-edge-policies#typosquattingallowlistdomains) policies.

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

<!-- ================== last note ===================== -->
<!-- Version 119.0.2151.97: November 29, 2023 to Version 118.0.2088.57: October 18, 2023 -->

## Version 119.0.2151.97: November 29, 2023

Fixed various bugs and performance issues.

> [!IMPORTANT]
> This update to Stable channel contains a fix for [CVE-2023-6345](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2023-CVE-2023-6345), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#november-29-2023).

## Version 119.0.2151.93: November 27, 2023

Fixed various bugs and performance issues.

## Version 118.0.2088.109: November 16, 2023

Fixed various bugs and performance issues for Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#november-16-2023).

## Version 119.0.2151.72: November 16, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#november-16-2023).

## Version 118.0.2088.102: November 9, 2023

Fixed various bugs and performance issues for Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#november-9-2023).

## Version 119.0.2151.58: November 9, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#november-9-2023).

### Policy update

- [EdgeManagementPolicyOverridesPlatformPolicy](/deployedge/microsoft-edge-policies#edgemanagementpolicyoverridesplatformpolicy) - Microsoft Edge management service policy overrides platform policy
- [EdgeManagementUserPolicyOverridesCloudMachinePolicy](/deployedge/microsoft-edge-policies#edgemanagementuserpolicyoverridescloudmachinepolicy) - Allow Microsoft Edge management service user policies to override policies set through an enrollment token

<!-- from Version 118.0.2088.46: October 13, 2023 to Version 109.0.1518.140: September 15, 2023 -->

## Version 118.0.2088.46: October 13, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-13-2023).

### Announcement: Icon change in Edge sidebar

In an upcoming update to Microsoft Edge, the Bing icon entry point in the Microsoft Edge sidebar changes to the new Copilot icon. No other changes in the experience are expected.

### Feature updates

- **Microsoft Edge for Business Banner.**  Microsoft Edge for Business is a dedicated Microsoft Edge experience built for work that enables admins in organizations to give their users a productive and secure work browser across managed and unmanaged devices. The in-product Microsoft Edge for Business banner is being deprecated and will no longer be visible.

- **Find on page.** Searching for a word or phrase on a webpage is easier with the new smart find update to Find on page. For more information, see
[Find on page](https://www.microsoft.com/edge/features/find-on-page?form=MT00D8). Now when you search with Find on page, we suggest related matches and synonyms making it effortless to find what you're looking for, even if you misspell a word in your search query. When you search, select the suggested word to quickly locate the desired word or phrase on the page. Data is sent to Microsoft for processing.  For more information, see [Microsoft Edge's Privacy Whitepaper](/microsoft-edge/privacy-whitepaper/). Administrators can control the availability using the [RelatedMatchesCloudServiceEnabled](/deployedge/microsoft-edge-policies#relatedmatchescloudserviceenabled) policy.

- **New SmartScreen policy.**  The [ExemptSmartScreenDownloadWarnings](/deployedge/microsoft-edge-policies#exemptsmartscreendownloadwarnings) policy lets administrators create a dictionary of file type extensions with a corresponding list of domains that are exempted from SmartScreen AppRep warnings.  Files with file type extensions specified for domains identified by this policy are still subject to file type extension-based security warnings and mixed-content download warnings.

- **New Microsoft Edge Update policies.** The **MeteredUpdatesDefault** and **MeteredUpdates** policies allows administrators to control the "Download Updates over metered connections" setting (`edge://settings/help`). The **MeteredUpdatesDefault** applies to all apps and **MeteredUpdates** applies to targeted apps. When a policy is configured to Allow, updates occur on a metered connection, such as cellular connections or others where data usage is controlled.

- **Support for WindowsTabManager API.** Microsoft Edge version 118 uses the new public Windows WindowTabManager API (for more information, see [WindowTabManager Class (Windows.UI.Shell) - Windows UWP applications](/uwp/api/windows.ui.shell.windowtabmanager?view=winrt-22621&viewFallbackFrom=winrt-22000)) to support features such as showing browser tabs in Alt+Tab, tab tearout, and taskbar pin glomming. These features will only work on newer Windows versions that support this API:

  - Windows 11: [May 24, 2023—KB5026446 (OS Build 22621.1778) Preview - Microsoft Support](https://support.microsoft.com/en-us/topic/may-24-2023-kb5026446-os-build-22621-1778-preview-3c547100-7a73-4ae6-bb7d-ebd02e87dc04)
  - Windows 10: [May 23, 2023—KB5026435 (OS Build 19045.3031) Preview - Microsoft Support](https://support.microsoft.com/en-us/topic/may-23-2023-kb5026435-os-build-19045-3031-preview-2751b693-5544-4110-bc0c-feb8dd7336b3)

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

### Policy updates

#### New policies

- [NewTabPageBingChatEnabled](/deployedge/microsoft-edge-policies#newtabpagebingchatenabled) - Disable Bing chat entry-points on Microsoft Edge Enterprise new tab page
- [NewTabPageCompanyLogoEnabled](/deployedge/microsoft-edge-policies#newtabpagecompanylogoenabled) - Hide the company logo on the Microsoft Edge new tab page

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
## Version: 117.0.2045.31: September 15, 2023

Fixed various bugs and performance issues.

> [!IMPORTANT]
> This update to Stable channel contains a fix for [CVE-2023-4863](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2023-4863), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-15-2023).

### Announcement: Microsoft Edge for Business is available for unmanaged Windows devices

Microsoft Edge for Business is a dedicated Microsoft Edge experience built for work that enables admins in organizations to give their users a productive and secure work browser. This dedicated work experience is now available for unmanaged Windows devices using Microsoft Intune Mobile Application Management (MAM). This release includes the supporting changes for Microsoft Edge. When the required Intune update is released, more information is available on how to test and deploy this feature with your users.

**Note:**

- Support is available for Windows 11, build 10.0.22621 (22H2) or later.

- Requires Microsoft Intune 2309 or higher

- App Protection Conditional Access is in Public Preview.

- If you have a Conditional Access (CA) policy on your tenant that targets "All cloud apps" that covers "Mobile apps and desktop clients" and requires a compliant device, app protection policies or has a "Block" grant control, your end users won't be able to MAM enroll. A change to support this is targeted for Microsoft Edge v118.

- If you want to continue testing/evaluating APP CA, you can choose to exclude the "Edge Auth" application from your cloud app targeting. Some Microsoft Edge features might not function properly until CA is satisfied, but MAM enrollment will be able to complete.

### Announcement: Deprecating the unload event

The Google Chrome team plans to deprecate the unload event starting in Chrome version 118. The deprecation occurs by gradually changing the default so unload handlers stop firing on pages unless a page explicitly opts in to re-enable them. For more information, see [Deprecating the unload event - Chrome Developers](https://developer.chrome.com/blog/deprecating-unload/), and [Google Groups - Conversations](https://groups.google.com/a/chromium.org/g/blink-dev/c/dvusqw9-IhI/m/SBkm_u1RAQAJ).

While we haven't yet finalized the deprecation schedule, we anticipate that Microsoft Edge will follow Chrome's schedule with a possible delay of a release or two. If you're interested in testing with Microsoft Edge starting in version 118, the **ForcePermissionPolicyUnloadDefaultEnabled** policy is available or you can use the instructions documented at [Disable unload handlers by default and add Permissions-Policy to opt-in to enabling them](https://github.com/fergald/docs/blob/master/explainers/permissions-policy-deprecate-unload.md#disable-unload-handlers-by-default-and-add-permissions-policy-to-opt-in-to-enabling-them).

WebView2 supports both the permissions policy and the enterprise policy but won't be impacted by the gradual rollout in Microsoft Edge. We expect WebView2 will switch defaults when the rollout reaches 100% of page loads.

### Feature updates

- **Microsoft Edge for Business Banner.**  Administrators can control the availability of the in-product Microsoft Edge for Business banner using the [PromotionalTabsEnabled](/deployedge/microsoft-edge-policies#promotionaltabsenabled) policy.

- **Microsoft Edge Sync Favorites Recovery.** The Microsoft Edge Sync Favorites Recovery feature lets sync users restore any favorites that they lost or deleted within the last 14 days. Users can access this feature from either the Microsoft Edge favorites hub or the `edge://favorites` page. For more information, see [Recover lost or deleted favorites in Microsoft Edge - Microsoft Support](https://support.microsoft.com/topic/recover-lost-or-deleted-favorites-in-microsoft-edge-ac06270e-ba57-4266-8389-8bfd1df1aa5e)

- **Autofill Autocomplete.** This feature helps you fill form fields faster on the web. When you start typing in a form field, Microsoft Edge suggests possible in-line completions when there's an exact match with your saved data in the browser. For example, if you type the first few characters of your address, autocomplete suggests the rest of address - you can choose the autocomplete suggestion or continue typing as usual. Autofill options can be found in Settings (`edge://settings/personalinfo`).

- **Deprecation of Web Select.** To improve end user experience, this feature is being deprecated and will no longer be an option under Web Capture or via keyboard shortcut.

- **Deprecation of features.** To improve end user experience and simplify the **More tools** menu, the following features are being deprecated: Math Solver, Picture Dictionary, Citations, Grammar Tools, and Kids Mode.

### Policy updates

#### New policies

- [AllowSystemNotifications](/deployedge/microsoft-edge-policies#allowsystemnotifications) - Allows system notifications
- [EdgeWalletEtreeEnabled](/deployedge/microsoft-edge-policies#edgewalletetreeenabled) - Edge Wallet E-Tree Enabled
- [GamerModeEnabled](/deployedge/microsoft-edge-policies#gamermodeenabled) - Enable Gamer Mode
- [SearchbarAllowed](/deployedge/microsoft-edge-policies#searchbarallowed) - Enable the Search bar
- [SearchbarIsEnabledOnStartup](/deployedge/microsoft-edge-policies#searchbarisenabledonstartup) - Allow the Search bar at Windows startup
- [ShowHistoryThumbnails](/deployedge/microsoft-edge-policies#showhistorythumbnails) - Show thumbnail images for browsing history
- [UploadFromPhoneEnabled](/deployedge/microsoft-edge-policies#uploadfromphoneenabled) - Enable upload files from phone in Microsoft Edge desktop
- [InternetExplorerIntegrationZoneIdentifierMhtFileAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationzoneidentifiermhtfileallowed) - Automatically open downloaded MHT or MHTML files from the web in Internet Explorer mode
- [PasswordDeleteOnBrowserCloseEnabled](/deployedge/microsoft-edge-policies#passworddeleteonbrowsercloseenabled) - Save passwords when Microsoft Edge closes
- [SplitScreenEnabled](/deployedge/microsoft-edge-policies#splitscreenenabled) - Enable split screen feature in Microsoft Edge

#### Deprecated policies

- [WebWidgetAllowed](/deployedge/microsoft-edge-policies#webwidgetallowed) - Enable the Search bar
- [WebWidgetIsEnabledOnStartup](/deployedge/microsoft-edge-policies#webwidgetisenabledonstartup) - Allow the Search bar at Windows startup

#### Obsoleted policy

- [WebSelectEnabled](/deployedge/microsoft-edge-policies#webselectenabled) - Web Select Enabled

## Version 116.0.1938.81: September 12, 2023

Fixed various bugs and performance issues for Stable and Extended Stable release.

> [!IMPORTANT]
> This update to Stable and Extended Stable contains a fix for [CVE-2023-4863](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2023-4863), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-12-2023).

## Version 116.0.1938.76: September 7, 2023

Fixed various bugs and performance issues for Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-7-2023).

## Version 116.0.1938.69: August 31, 2023

Fixed various bugs and performance issues for Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-31-2023).

## Version 116.0.1938.62: August 25, 2023

Fixed various bugs and performance issues for Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-25-2023).

### Feature update

- **Tab organization.**  Microsoft Edge offers helpful suggestions on how to organize tabs to save you time and keep you focused on the web content you care about. These suggestions augment the Tab Grouping feature built into Microsoft Edge. When two or more tabs are grouped together, Microsoft Edge can automatically generate a relevant name for the Tab Group. Furthermore, Microsoft Edge can suggest grouping for all of your tabs by using the "Group Similar Tabs" feature in the Tab Action menu. Administrators can control the availability of this feature using the [TabServicesEnabled](/deployedge/microsoft-edge-policies#tabservicesenabled) policy.

<!-- from Version 116.0.1938.54: August 21, 2023 to Version 114.0.1823.41: June 6, 2023 -->
## Version 116.0.1938.54: August 21, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-21-2023).

### Feature update

- **Microsoft Edge for Business.** With native enterprise grade security, productivity, manageability, and AI built in, Edge for Business enables organizations to maximize productivity and security, and offers the ability to create separation between work and personal browsing with automatic switching between the lightly managed personal browser window (MSA profile) and the work browser window (Microsoft Entra ID). All users signing in with their Microsoft Entra (formerly Azure Active Directory) user ID will automatically receive Edge for Business and see an updated Edge icon with a briefcase to designate they're in the work browser window. For more information, [read our FAQ](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/microsoft-edge-for-business-faq/ba-p/3891837).

- **Option to attach the Edge sidebar to the Windows desktop.** Users of the Microsoft Edge sidebar are able to access their apps and sites directly from their Windows 10 desktop. As an opt-in experience in Windows 10, users can attach the sidebar to their Windows desktop by clicking a "popout" icon near the base of the sidebar in the browser. This enables a side-by-side experience that works with any Windows app—including Microsoft Edge itself. Users enjoy streamlined access to the same set of powerful AI tools and web-based services, including Bing Chat, without launching a browser window, enhancing productivity regardless of where they are in Windows. More features and options are planned in future versions of Microsoft Edge. Administrators can control the availability of this feature using the [StandaloneHubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#standalonehubssidebarenabled) policy.

### Policy updates

#### New policies

- [ThrottleNonVisibleCrossOriginIframesAllowed ](/deployedge/microsoft-edge-policies#throttlenonvisiblecrossoriginiframesallowed) - Allows enabling throttling of non-visible, cross-origin iframes

#### Obsoleted policy

- [EventPathEnabled](/deployedge/microsoft-edge-policies#eventpathenabled) - Re-enable the Event.path API

## Version 115.0.1901.203: August 10, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.106: August 7, 2023

Fixed various bugs and performance issues for Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-7-2023).

### Feature update

- **New policy for Browser essentials.** Browser essentials help you gain extra insights about the health of your browser. It lets you stay informed about your browser's performance and security with a single, intuitive view that provides helpful suggestions for performance optimization and browser protection. The [PinBrowserEssentialsToolbarButton](/deployedge/microsoft-edge-policies#pinbrowseressentialstoolbarbutton) policy lets Admins configure whether to pin the Browser essentials button on the toolbar.

## Version 115.0.1901.200: August 7, 2023

Fixed various bugs and performance issues for Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-7-2023).

## Version 115.0.1901.188: July 27, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.90: July 21, 2023

Fixed various bugs and performance issues for Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#july-21-2023).

## Version 115.0.1901.183: July 21, 2023

Fixed various bugs and performance issues for Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#july-21-2023).

### Feature update

- **Microsoft Edge management service.** Microsoft Edge management service is an area in the Microsoft 365 admin center where admins can manage the Microsoft Edge browser. It's a simple and easy-to-manage experience. Admins are able to configure all Microsoft Edge browser policies for their organization in a configuration profile and set-up the browser to use these settings. For more information, see [Microsoft Edge management service](/deployedge/microsoft-edge-management-service). **Note:** We'll start rolling out this experience on July 20 and expect to finish the rollout by next week.

### Policy updates

#### New policies

- [ComposeInlineEnabled](/deployedge/microsoft-edge-policies#composeinlineenabled) - Compose is enabled for writing on the web
- [EdgeManagementEnabled](/deployedge/microsoft-edge-policies#edgemanagementenabled) - Microsoft Edge management enabled
- [EdgeManagementEnrollmentToken](/deployedge/microsoft-edge-policies#edgemanagementenrollmenttoken) - Microsoft Edge management enrollment token
- [EdgeManagementExtensionsFeedbackEnabled](/deployedge/microsoft-edge-policies#edgemanagementextensionsfeedbackenabled) - Microsoft Edge management extensions feedback enabled
- [EnhanceSecurityModeIndicatorUIEnabled](/deployedge/microsoft-edge-policies#enhancesecuritymodeindicatoruienabled) - Manage the indicator UI of the Enhanced Security Mode (ESM) feature in Microsoft Edge
- [EnhanceSecurityModeOptOutUXEnabled](/deployedge/microsoft-edge-policies#enhancesecuritymodeoptoutuxenabled) - Manage opt-out user experience for Enhanced Security Mode (ESM) in Microsoft Edge
- [SearchForImageEnabled](/deployedge/microsoft-edge-policies#searchforimageenabled) - Search for image enabled
- [WalletDonationEnabled](/deployedge/microsoft-edge-policies#walletdonationenabled) - Wallet Donation Enabled

#### More policy changes

- [EnforceLocalAnchorConstraintsEnabled](/deployedge/microsoft-edge-policies#enforcelocalanchorconstraintsenabled) - Policy obsoletion delayed from 115 to 118

## Version 114.0.1823.86: July 17, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.82: July 13, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#july-13-2023).

## Version 114.0.1823.79, July 10, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.67: June 29, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-29-2023).

## Version 114.0.1823.58: June 22, 2023

Fixed various bugs and performance issues for Stable and Extended Stable release.

- **Google Docs Offline extension for Microsoft Edge.**  Google Docs Offline is an extension provided by Google to allow users to work on Google Docs, Sheets, Slides and Drive without internet access. This extension also provides advanced cut, copy, and paste functionalities across Google Editors.  The Google Docs Offline extension is pre-installed and will be disabled by default for Microsoft Edge users. When a user navigates to Google Docs, the extension is auto-enabled. Administrators can use the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) and [ExtensionInstallBlocklist](/deployedge/microsoft-edge-policies#extensioninstallblocklist) policies to block the automatic installation of the Google Docs Offline extension.  **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

## Version 114.0.1823.55: June 19, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.51: June 15, 2023

Fixed various bugs and performance issues for Stable and Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-15-2023).

### Feature update

- Web Select is now a part of Web Capture. Users can access Web Select through Web Capture feature or press **Ctrl** + **Shift** + **X** shortcut directly for quick access.

### Policy updates

#### Additional policy changes

- [WebSelectEnabled](/deployedge/microsoft-edge-policies#webselectenabled) - This policy is deprecated. It's currently supported but will become obsolete in version 117.
- [WebCaptureEnabled](/deployedge/microsoft-edge-policies#webcaptureenabled) - Since Web Select is now a part of Web Capture, this policy will enable/ disable both Web Select and Web Capture.

## Version 109.0.1518.115: June 13, 2023

> [!NOTE]
> This update was done for our M109 Windows down-level extended support.  We're shipping 109 to Win 7, 8, and 8.1 (including Server 2012 R2 which is based on Win 8.1).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-13-2023).

## Version 114.0.1823.43: June 8, 2023

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 114.0.1823.41: June 6, 2023

Fixed various bugs and performance issues.

> [!IMPORTANT]
> This update to Stable contains a fix for [CVE-2023-3079](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2023-3079), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-6-2023).

<!-- from Version 114.0.1823.37: June 2, 2023 to Version 112.0.1722.77: May 9, 2023 -->

## Version 114.0.1823.37: June 2, 2023

Fixed various bugs and performance issues for Stable and Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-2-2023).

### Feature update

- **Microsoft Edge Workspaces.** Edge Workspaces provides a way for customers to organize their browsing tasks into dedicated windows. Edge Workspaces lets users share a set of browser tabs so working groups can view the same websites and latest working files in one place and stay on the same page. Each Edge Workspace contains its own set of tabs and favorites, all created and curated by the user and their collaborators. Edge Workspaces are automatically saved and kept up to date. For more information, see [Microsoft Edge Workspaces](/deployedge/microsoft-edge-workspaces).

### Policy updates

#### New policies

- [StandaloneHubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#standalonehubssidebarenabled) - Standalone Sidebar Enabled
- [ShowDownloadsToolbarButton](/DeployEdge/microsoft-edge-policies#showdownloadstoolbarbutton) - Show Downloads button on the toolbar

#### Obsoleted policy

- [MicrosoftRootStoreEnabled](/DeployEdge/microsoft-edge-policies#microsoftrootstoreenabled) - Determines whether the Microsoft Root Store and built-in certificate verifier will be used to verify server certificates

#### Additional policy changes

- [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode) - BasicMode is deprecated
- [EdgeWorkspacesEnabled](/DeployEdge/microsoft-edge-policies#edgeworkspacesenabled) - If the policy isn't configured users are able to access the Microsoft Edge Workspaces feature

## Version 113.0.1774.57: May 25, 2023

Fixed various bugs and performance issues.

## Version 112.0.1722.84: May 18, 2023

Fixed various bugs and performance issues for Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-18-2023).

## Version 113.0.1774.50: May 18, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-18-2023).

### Feature update

- **Microsoft recommended browser settings.** This new prompt in Microsoft Edge lets users benefit from the Microsoft recommended settings. This feature gives users the option to set Microsoft Edge as the default browser and/or set Microsoft Bing as the default search engine, if they aren't already selected. If a user accepts the prompt, their default browser is updated to Microsoft Edge, and their default search engine will be updated to Microsoft Bing. Administrators can control the availability of the default browser settings campaign using the [DefaultBrowserSettingsCampaignEnabled](/deployedge/microsoft-edge-policies#defaultbrowsersettingscampaignenabled) policy.

## Version 113.0.1774.42: May 11, 2023

Fixed various bugs and performance issues.

## Version 112.0.1722.77: May 9, 2023

Fixed various bugs and performance issues for Extended Stable release.

<!-- from Version 113.0.1774.35: May 5, 2023 to Version 112.0.1722.39: April 10, 2023 -->
## Version 113.0.1774.35: May 5, 2023

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-5-2023).

### Feature update

- **Improvements to downloads security.** Microsoft Edge now has the capability to scan archives (.zip, .rar, .7z) for any malware using Microsoft Defender SmartScreen. This functionality is currently available on Windows only and provides extra protection where known malwares were being distributed within these archives.

- **Improvements to enhanced security mode.**  Enhanced security mode provides an extra layer of protection when browsing the web and visiting unfamiliar sites.  In this release, updates include consolidating the security level settings to Balanced and Strict mode.  For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **Switch from Microsoft Autoupdate to EdgeUpdater for macOS**. Microsoft Edge for macOS will start using a new updater named EdgeUpdater. This change only affects Microsoft Edge on macOS. If you use update preferences for Microsoft Autoupdate to prevent browser updates, you'll need to transition to the new EdgeUpdater UpdateDefault policy before Microsoft Edge 113 to prevent future automatic updates. For more information, see [Microsoft Edge for macOS switches from Microsoft AutoUpdate to EdgeUpdater](/deployedge/edge-learnmore-edgeupdater-for-macos).

- **New policy for PDF View Settings.** The [RestorePdfView](/deployedge/microsoft-edge-policies#restorepdfview) policy lets Admins control PDF View Recovery in Microsoft Edge.  When enabled or if the policy isn't configured, Microsoft Edge recovers the last state of PDF view and land users on the section where they ended reading in the last session.

- **Updated Microsoft Root Store policy.** The [MicrosoftRootStoreEnabled](/deployedge/microsoft-edge-policies#microsoftrootstoreenabled) policy will now be supported in Microsoft Edge version 113 and 114.  It is removed in Microsoft Edge version 115.  For more information, see [Changes to Microsoft Edge browser TLS server certificate verification](/deployedge/microsoft-edge-security-cert-verification).

### Policy updates

#### New policies

- [DiscoverPageContextEnabled](/DeployEdge/microsoft-edge-policies#discoverpagecontextenabled) - Enable Discover access to page contents for Microsoft Entra profiles
- [DefaultBrowserSettingsCampaignEnabled](/DeployEdge/microsoft-edge-policies#DefaultBrowserSettingsCampaignEnabled) - Enables default browser settings campaigns
- [EnforceLocalAnchorConstraintsEnabled](/DeployEdge/microsoft-edge-policies#enforcelocalanchorconstraintsenabled) - Determines whether the built-in certificate verifier enforces constraints encoded into trust anchors loaded from the platform trust store
- [RestorePdfView](/DeployEdge/microsoft-edge-policies#restorepdfview) - Restore PDF view
- [ReadAloudEnabled](/DeployEdge/microsoft-edge-policies#readaloudenabled) - Enable Read Aloud feature in Microsoft Edge
- [ShowDownloadsToolbarButton](/DeployEdge/microsoft-edge-policies#showdownloadstoolbarbutton) - Show Downloads button on the toolbar
- [TabServicesEnabled](/DeployEdge/microsoft-edge-policies#tabservicesenabled) - Tab Services enabled

## Version 112.0.1722.71: May 4, 2023

Fixed various bugs and performance issues for Extended Stable release.

## Version 112.0.1722.68: May 1, 2023

Fixed various bugs and performance issues.

## Version 112.0.1722.64: April 27, 2023

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 109.0.1518.100: April 24, 2023

> [!NOTE]
> This update was done for our M109 Windows down-level extended support. We're shipping 109 to Win 7, 8, and 8.1 (including Server 2012 R2 which is based on Win 8.1).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-24-2023).

## Version 112.0.1722.58: April 21, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-21-2023).

## Version 112.0.1722.48: April 14, 2023

> [!IMPORTANT]
> This update to Extended Stable contains a fix for [CVE-2023-2033](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2023-2033), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-14-2023).

## Version 112.0.1722.46: April 13, 2023

Fixed various bugs and performance issues.

## Version 112.0.1722.39: April 10, 2023

Fixed various bugs and performance issues.

<!-- from Version 112.0.1722.34: April 6, 2023 to Version 111.0.1661.43: March 15, 2023 -->
## Version 112.0.1722.34: April 6, 2023

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-6-2023).

### Feature update

- **Enhanced security mode improvements.** Enhanced security mode now supports WebAssembly for ARM64. Cross-platform support is now available for x64 Windows, x64 macOS, x64 Linux and ARM64 systems. For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **Added features for web app policy.** The [WebAppInstallForceList](/deployedge/microsoft-edge-policies#webappinstallforcelist) policy lets administrators configure a list of web apps that install silently, without user interaction, and which users can't uninstall or turn off. This policy now supports custom_name, which permanently overrides the app name of installed apps and custom_icon, which permanently overrides the app icon of installed apps.

- **In-browser JSON viewer.**  Improvements to how JSON files are displayed in the browser, which includes a color-coded tree view with line numbers and the ability to collapse and expand the data.  This functionality triggers automatically when the browser navigates to a JSON file on the web or the user opens a local one.  More features and enhancements roll out as available.  For more information, see [View formatted JSON - Microsoft Edge Development](/microsoft-edge/devtools-guide-chromium/json-viewer/json-viewer).  Note: This is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout or you can navigate to `edge://flags` and search for JSON Viewer to manually enable.  

- **Updated new tab page policy.** The [NewTabPageHideDefaultTopSites](/deployedge/microsoft-edge-policies#newtabpagehidedefaulttopsites) policy hides the default top sites from the new tab page in Microsoft Edge. Starting on March 20, when the policy is enabled it will also remove sponsored quick links from the new tab page.

- **Edit and save web images in Microsoft Edge.** You can right click on the desired web image and without leaving your browser window, crop, adjust lighting and color, and add filters. From there, you can save the edited image for later use. You can also start editing simply by hovering over an image and selecting edit image from the menu.

### Policy updates

#### New policies

- [CryptoWalletEnabled](/DeployEdge/microsoft-edge-policies#cryptowalletenabled) - Enable CryptoWallet feature

## Version 111.0.1661.62: March 30, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.54: March 24, 2023

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-24-2023).

### Feature update

- **New Microsoft Edge PDF experience policy.**  As part of the Adobe and Microsoft collaboration to re-envision the future workplace and your digital experiences, we're natively embedding the Adobe Acrobat PDF engine into the Microsoft Edge built-in PDF reader, with a release scheduled in March 2023. Administrators can start testing the new Microsoft Edge PDF reader that is powered by the Adobe Acrobat PDF engine by enabling the [NewPDFReaderEnabled](/deployedge/microsoft-edge-policies#newpdfreaderenabled) policy.  For more information, see [Microsoft Edge and Adobe partner to improve the PDF experience](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/microsoft-edge-and-adobe-partner-to-improve-the-pdf-experience/ba-p/3733481).  

- **Microsoft Edge Sidebar Improvements.** The Microsoft Edge sidebar lets users access productivity tools side-by-side with their browsing window. In this release, the sidebar is enhanced to increase productivity and improve user experience. As communicated in our last release ([Microsoft Edge release notes for Stable Channel](/deployedge/microsoft-edge-relnote-stable-channel#version-1110166141-march-13-2023)), the sidebar now includes a toolbar button by default to access the experience. If admins enable the Discover app, hovering and clicking the toolbar button will invoke both the sidebar tower, and the new discover experience.

   With this release, admins now have the ability to disable the Discover app and still keep the Sidebar. In this situation, the Sidebar tower will always be shown. If an Admin chooses to enable the Sidebar but disable the Discover experience, the Sidebar can only be always shown or hidden. This default visibility can be changed in the Sidebar settings (*edge://settings/sidebar*).
 
   When an admin enables the Sidebar and the Discover experience, enterprise users can choose to 'always show', or 'auto hide'. More customization options for the sidebar toolbar button are planned in future versions of Microsoft Edge.  For more information, see [Manage the sidebar in Microsoft Edge](/DeployEdge/microsoft-edge-sidebar).

## Version 109.0.1518.95: March 23, 2023

> [!NOTE]
> This update was done for our M109 Windows down-level extended support.  We're shipping 109 to Win 7, 8, and 8.1 (including Server 2012 R2 which is based on Win 8.1).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-23-2023).

## Version 110.0.1587.78: March 23, 2023

Fixed various bugs and performance issues for Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-23-2023).

## Version 111.0.1661.51: March 21, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.44: March 16, 2023

### Policy updates

#### New policies

- [ShowAcrobatSubscriptionButton](/deployedge/microsoft-edge-policies#showacrobatsubscriptionbutton) - Shows button on native PDF viewer in Microsoft Edge that allows users to sign up for Adobe Acrobat subscription
- [NewPDFReaderEnabled](/DeployEdge/microsoft-edge-policies#newpdfreaderenabled) - Microsoft Edge built-in PDF reader powered by Adobe Acrobat enabled

## Version 111.0.1661.43: March 15, 2023

Fixed various bugs and performance issues.
<!-- from Version 111.0.1661.41: March 13, 2023 to Version 110.0.1587.46: February 14, 2023 -->
## Version 111.0.1661.41: March 13, 2023

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-13-2023).

### Feature update

- **A New Microsoft Edge Sidebar.** In this release, the Sidebar introduces several new features and improvements aimed at enhancing productivity, convenience, and the user experience. Here are some of the highlights:<br><br>

  - **The New Discover:** Edge Copilot is a powerful tool that helps users boost their productivity and efficiency. It provides intelligent suggestions and insights based on the context of the web page and the user's goals. As the new Bing icon in the Toolbar, Edge Copilot helps users compose better emails, search the web faster, learn new skills, all done more conveniently.  
  - **Enhanced Sidebar Visibility:** With the new Auto-Hide functionality, a user can maximize the productivity and convenience of the sidebar without sacrificing valuable screen space. The Edge Sidebar can be hidden when a user isn't using it and it only reappears when a user needs it.  
  - **Evolved Sidebar Interaction:** The new Hover functionality lets users open the Sidebar by hovering on the Bing icon in the Toolbar. This enhances user productivity and convenience by providing a seamless and intuitive way to access their most used tools.  

  Admins retain the ability to control and customize the Sidebar and its experiences, as needed by using the following settings:<br><br>

  - If admins enable the Sidebar, users have access to the Sidebar and Edge Copilot experience. The Sidebar always shows in the browser frame. Clicking on the Bing icon in the Toolbar invokes the new Discover experience.
  - If admins choose the 'not configured' setting, users have access to the Sidebar and Edge Copilot experience. Unlike when the Sidebar is 'enabled', their users have the ability to always-show or autohide the Sidebar.
  - If admins disable the Sidebar, Discover and the Sidebar will be inaccessible for their users. **Note:** In this release, Admins don't have the ability to disable Discover and keep the Sidebar.

  More customization options for the sidebar toolbar button are planned in future versions of Microsoft Edge.

  For more information, see [Manage the sidebar in Microsoft Edge](/DeployEdge/microsoft-edge-sidebar) and [Microsoft Privacy Statement (Search, Microsoft Edge, and artificial intelligence)](https://privacy.microsoft.com/privacystatement).

- **Microsoft Feed on Microsoft 365 Edge New Tab Page.** We're rolling out a new experience to the Microsoft 365 tab of the Edge Enterprise New Tab Page. This experience features a new layout that centers on a larger version of the Microsoft Feed, featuring more productivity content, and moves the productivity cards including Important Emails, Recent SharePoint sites, Upcoming events, and To Do to the right-hand side of the Microsoft 365 tab.

- **Enhanced security mode improvements.** Enhanced security mode now supports WebAssembly for macOS x64 and Linux x64. More cross-platform (ARM64) support is expected in the future. For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **New policy to clear IE mode data on browser exit.** The [InternetExplorerModeClearDataOnExitEnabled](/deployedge/microsoft-edge-policies#internetexplorermodecleardataonexitenabled) policy controls whether browsing history is deleted from Internet Explorer and Internet Explorer mode every time Microsoft Edge is closed. Users can also configure this setting in the 'Clear browsing data for Internet Explorer' option in the Privacy, search, and services menu of Settings (*edge://settings/privacy*).

### Policy updates

#### New policies

- [InternetExplorerModeClearDataOnExitEnabled](/DeployEdge/microsoft-edge-policies#internetexplorermodecleardataonexitenabled) - Clear history for IE and IE mode every time you exit
- [MouseGestureEnabled](/DeployEdge/microsoft-edge-policies#mousegestureenabled) - Mouse Gesture Enabled
- [PrintPreviewStickySettings](/DeployEdge/microsoft-edge-policies#printpreviewstickysettings) - Configure the sticky print preview settings

## Version 110.0.1587.69: March 9, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-13-2023).

## Version 110.0.1587.63: March 3, 2023

Fixed various bugs and performance issues.

## Version 110.0.1587.57: February 25, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#february-25-2023).

## Version 110.0.1587.56: February 23, 2023

Fixed various bugs and performance issues.

## Version 110.0.1587.50: February 17, 2023

Fixed various bugs and performance issues.

## Version 110.0.1587.49: February 16, 2023

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 110.0.1587.46: February 14, 2023

Fixed various bugs and performance issues.


<!-- from Version Version 110.0.1587.41: February 9, 2023 to Version 108.0.1462.83: January 12, 2023 -->
## Version 110.0.1587.41: February 9, 2023

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#february-9-2023).

### Feature updates

- **New Immersive Reader policies.** Immersive Reader in Microsoft Edge simplifies web page layouts, removes clutter, and helps you customize your reading experience. Admins using these new policies ([ImmersiveReaderGrammarToolsEnabled](/deployedge/microsoft-edge-policies#immersivereadergrammartoolsenabled) and [ImmersiveReaderPictureDictionaryEnabled](/deployedge/microsoft-edge-policies#immersivereaderpicturedictionaryenabled)), can control the availability of Grammar Tools and Picture Dictionary features within Immersive Reader.

- **Enabling sync for Microsoft Entra ID signed in customers.** Microsoft Edge sync roams data across all signed in instances of Microsoft Edge. This data includes favorites, passwords, browsing history, open tabs, settings, apps, collections, and extensions.  For Microsoft Entra users who have sync turned off, after the browser is launched they see a notification prompt and have sync turned on for all signed in instances of Microsoft Edge. This sync enablement includes other devices where they're signed in. Additionally, if a user's other devices don't have history and open tabs sync on, those two toggles are turned on. Organizations using the [SyncDisabled](/deployedge/microsoft-edge-policies#syncdisabled) policy aren't affected by this change.

- **Drop.** Microsoft Edge now offers a simple way to send files and notes across all your signed in mobile and desktop devices. Using the desktop version of Microsoft Edge, Drop can be managed through the sidebar (*edge://settings/sidebar*).  Administrators can control the availability of Drop using the [EdgeEDropEnabled](/deployedge/microsoft-edge-policies#edgeedropenabled) policy.

### Policy updates

#### New policies

- [AutofillMembershipsEnabled](/DeployEdge/microsoft-edge-policies#autofillmembershipsenabled) - Save and fill memberships
- [ImmersiveReaderGrammarToolsEnabled](/DeployEdge/microsoft-edge-policies#immersivereadergrammartoolsenabled) - Enable Grammar Tools feature within Immersive Reader in Microsoft Edge
- [ImmersiveReaderPictureDictionaryEnabled](/DeployEdge/microsoft-edge-policies#immersivereaderpicturedictionaryenabled) - Enable Picture Dictionary feature within Immersive Reader in Microsoft Edge
- [PrintPreviewStickySettings](/DeployEdge/microsoft-edge-policies#printpreviewstickysettings) - Configure the sticky print preview settings
- [SearchInSidebarEnabled](/DeployEdge/microsoft-edge-policies#searchinsidebarenabled) - Search in Sidebar enabled
- [WorkspacesNavigationSettings](/DeployEdge/microsoft-edge-policies#workspacesnavigationsettings) - Configure navigation settings per groups of URLs in Microsoft Edge Workspaces

#### Obsoleted policies

- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) - Specifies whether the display-capture permissions-policy is checked or skipped
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains
- [SetTimeoutWithout1MsClampEnabled](/DeployEdge/microsoft-edge-policies#settimeoutwithout1msclampenabled) - Control JavaScript setTimeout() function minimum timeout
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) Configure ShadowStack crash rollback behavior

## Version 109.0.1518.78: February 2, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#february-2-2023).

## Version 109.0.1518.70: January 26, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-26-2023).

## Version 108.0.1462.95: January 26, 2023

Fixed various bugs and performance issues for Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-26-2023).

## Version 109.0.1518.69: January 25, 2023

Fixed various bugs and performance issues.

## Version 109.0.1518.61: January 19, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-19-2023).

## Version 108.0.1462.87: January 15, 2023

Fixed various bugs and performance issues for Extended Stable release.

## Version 109.0.1518.55: January 15, 2023

Fixed various bugs and performance issues.

## Version 109.0.1518.52: January 13, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-13-2023).

## Version 108.0.1462.83: January 12, 2023

Fixed various bugs and performance issues for Extended Stable release.

<!-- from Version 109.0.1518.49: January 12, 2023 to Version 108.0.1462.46: December 8, 2022 -->
## Version 109.0.1518.49: January 12, 2023

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-12-2023).

### Feature updates

- **Account Linking between a personal Microsoft account (MSA) and Microsoft Entra account.** Microsoft is enabling users to link a personal Microsoft account (MSA) and Microsoft Entra account through work or school.  Once linked, users can earn Microsoft Rewards points for Microsoft Bing searches done in their browser or Windows search box while signed in with their work or school account. For more information, see the [Account Linking FAQ](https://support.microsoft.com/account-billing/account-linking-faq-c66effb9-02e6-49c0-89e1-ae4d8644e6f7) and the [Account Linking IT Admins FAQ](https://support.microsoft.com/account-billing/account-linking-it-admins-faq-72f0dc4e-b632-439e-b90c-347043a7b75a). Tenant admins can also control this feature in the Message Center section of the Microsoft 365 Admin Center or by using the [LinkedAccountEnabled](/deployedge/microsoft-edge-policies#linkedaccountenabled) policy.

- **TLS server certificate verification changes.** In Microsoft Edge version 111, the certificate trust list and the certificate verifier will be decoupled from the host operating system's root store.  Instead, the default certificate trust list and the certificate verifier will be provided by and shipped with the browser.  The [MicrosoftRootStoreEnabled](/deployedge/microsoft-edge-policies#microsoftrootstoreenabled) policy is now available for testing to control when the built-in root store and certificate verifier are used.  Support for the policy is planned to be removed in Microsoft Edge version 113.  For more information, see [Changes to Microsoft Edge browser TLS server certificate verification | Microsoft Learn](/deployedge/microsoft-edge-security-cert-verification).  **Note:** This is a controlled feature rollout in Microsoft Edge version 109.  If you don't see this feature, check back as we continue our rollout.

-  **Text prediction.** To help you write faster and with fewer mistakes, Microsoft Edge provides word and sentence predictions for long-form editable text fields on web pages. For more information, see [Text Prediction](https://www.microsoft.com/en-us/edge/features/text-prediction?msockid=2bf3e0ce845a692534f7f4ed857768e4&form=MA13FJ). When you type on editable text fields on Edge, data is sent to Microsoft for processing. For more information, see [Microsoft Edge Privacy Whitepaper - Microsoft Edge Development](/microsoft-edge/privacy-whitepaper/). Administrators can control the availability of text predictions using the [TextPredictionEnabled](/deployedge/microsoft-edge-policies#textpredictionenabled) policy. Text prediction is currently only available in English within the US, India, and Australia. We'll continue to add new languages and regions in future versions of Microsoft Edge.  

### Policy updates

#### New policies

- [WebHidAllowAllDevicesForUrls](/DeployEdge/microsoft-edge-policies#webhidallowalldevicesforurls) - Allow listed sites to connect to any HID device
- [WebHidAllowDevicesForUrls](/DeployEdge/microsoft-edge-policies#webhidallowdevicesforurls) - Allow listed sites connect to specific HID devices
- [WebHidAllowDevicesWithHidUsagesForUrls](/DeployEdge/microsoft-edge-policies#webhidallowdeviceswithhidusagesforurls) - Automatically grant permission to these sites to connect to HID devices containing top-level collections with the given HID usage
- [MicrosoftRootStoreEnabled](/DeployEdge/microsoft-edge-policies#microsoftrootstoreenabled) - Determines whether the Microsoft Root Store and built-in certificate verifier is used to verify server certificates
- [DefaultClipboardSetting](/DeployEdge/microsoft-edge-policies#defaultclipboardsetting) - Default clipboard site permission
- [ClipboardAllowedForUrls](/DeployEdge/microsoft-edge-policies#clipboardallowedforurls) - Allow clipboard use on specific sites
- [ClipboardBlockedForUrls](/DeployEdge/microsoft-edge-policies#clipboardblockedforurls) - Block clipboard use on specific sites
- [SearchFiltersEnabled](/DeployEdge/microsoft-edge-policies#searchfiltersenabled) - Search Filters Enabled

#### Deprecated policies

- [SetTimeoutWithout1MsClampEnabled](/DeployEdge/microsoft-edge-policies#settimeoutwithout1msclampenabled) - Control JavaScript setTimeout() function minimum timeout
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains

## Version 108.0.1462.76: January 5, 2023

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 108.0.1462.54: December 16, 2022

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#december-16-2022).

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 108.0.1462.46: December 8, 2022

Fixed various bugs and performance issues for Stable and Extended Stable release.

<!-- from Version 108.0.1462.42: December 5, 2022 to Version 106.0.1370.59: October 27, 2022 -->
## Version 108.0.1462.42: December 5, 2022

> [!IMPORTANT]
> This update to Extended Stable contains a fix for [CVE-2022-4262](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-4262), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#december-5-2022)

### Feature updates

- **Graph APIs for Cloud Site List Management.** New Graph APIs that allow IT admins in organizations to create, manage, and publish their site lists for IE mode in the cloud.  For more information, see [Use the Edge API in Microsoft Graph](/graph/api/resources/browser-edge-api-overview?view=graph-rest-beta&preserve-view=true).

- **More reliable web defense.** Browse the web with more reliable protection thanks to the rewritten [Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) library for Microsoft Edge on Windows, Mac, and Linux. The new SmartScreen library was first made available on Windows and Mac, and now makes its debut on Linux with Microsoft Edge version 108. Microsoft Edge version 108 also brings new product optimizations (that is, better proxy handling) and bug fixes by having the SmartScreen library use Microsoft Edge's built-in network stack.

### Policy updates

#### New policies

- [EncryptedClientHelloEnabled](/DeployEdge/microsoft-edge-policies#encryptedclienthelloenabled) - TLS Encrypted ClientHello Enabled
- [NewTabPageAppLauncherEnabled](/DeployEdge/microsoft-edge-policies#newtabpageapplauncherenabled) - Hide App Launcher on Microsoft Edge new tab page

#### Obsoleted policy

- [NewSmartScreenLibraryEnabled](/DeployEdge/microsoft-edge-policies#newsmartscreenlibraryenabled) Enable new SmartScreen library

## Version 107.0.1418.62: November 28, 2022

> [!IMPORTANT]
> This update contains a fix for [CVE-2022-4135](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-4135), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#november-28-2022).

## Version 106.0.1370.86: November 28, 2022

> [!IMPORTANT]
> This update to Extended Stable contains a fix for [CVE-2022-4135](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-4135), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#november-28-2022)

## Version 107.0.1418.56: November 21, 2022

Fixed various bugs and performance issues.

## Version 107.0.1418.52: November 17, 2022

Fixed various bugs and performance issues.

## Version 107.0.1418.42: November 10, 2022

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#november-10-2022).

## Version 106.0.1370.72: November 10, 2022

Fixed various bugs and performance issues for Extended Stable channel.

## Version 107.0.1418.35: November 3, 2022

Fixed various bugs and performance issues.

## Version 107.0.1418.26: October 29, 2022

> [!IMPORTANT]
> This update contains a fix for [CVE-2022-3723](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-3723), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-31-2022).

## Version 106.0.1370.61: October 29, 2022

> [!IMPORTANT]
> This update to Extended Stable contains a fix for [CVE-2022-3723](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-3723), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-31-2022)

## Version 106.0.1370.59: October 27, 2022

Fixed various bugs and performance issues for Extended Stable release.

<!--- from Version 107.0.1418.24: October 27, 2022 to Version 106.0.1370.37: October 6, 2022 -->

## Version 107.0.1418.24: October 27, 2022

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-27-2022).

### Feature updates

- **Microsoft Edge sidebar.** The Microsoft Edge sidebar lets users access productivity tools side-by-side with their browsing window. For enterprise customers, the following experiences are currently turned on by default: Search, Discover, Office.com, and Outlook. Administrators can control the availability and configure the Microsoft Edge sidebar using the [HubsSidebarEnabled](/deployedge/microsoft-edge-policies#hubssidebarenabled), [ExtensionInstallBlockList](/deployedge/microsoft-edge-policies#extensioninstallblocklist), and [ExtensionInstallForceList](/deployedge/microsoft-edge-policies#extensioninstallforcelist) policies. The extension ID for each sidebar app can be found at *edge://sidebar-internals*.  For more information, see [Manage the sidebar in Microsoft Edge](/DeployEdge/microsoft-edge-sidebar).

- **New policy to give more flexibility in Microsoft Edge startup.** The [RestoreOnStartupUserURLsEnabled](/deployedge/microsoft-edge-policies#restoreonstartupuserurlsenabled) policy lets users add and remove their own URLs to open when starting Microsoft Edge while maintaining the mandatory list of sites specified by the admin.

### Policy updates

#### New policies

- [EdgeWorkspacesEnabled](/DeployEdge/microsoft-edge-policies#edgeworkspacesenabled) - Enable Workspaces
- [EnhanceSecurityModeBypassIntranet](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypassintranet) - Enhanced Security Mode configuration for Intranet zone sites
- [EventPathEnabled](/DeployEdge/microsoft-edge-policies#eventpathenabled) - Re-enable the Event.path API until Microsoft Edge version 115
- [InternetExplorerIntegrationLocalMhtFileAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalmhtfileallowed) - Allow local MHTML files to open automatically in Internet Explorer mode
- [LinkedAccountEnabled](/DeployEdge/microsoft-edge-policies#linkedaccountenabled) - Enable the linked account feature
- [PerformanceDetectorEnabled](/DeployEdge/microsoft-edge-policies#performancedetectorenabled) - Performance Detector Enabled
- [RestoreOnStartupUserURLsEnabled](/DeployEdge/microsoft-edge-policies#restoreonstartupuserurlsenabled) - Allow users to add and remove their own sites during startup when the RestoreOnStartupURLs policy is configured
- [DefaultShareAdditionalOSRegionSetting](/DeployEdge/microsoft-edge-policies#defaultshareadditionalosregionsetting) - Set the default "share additional operating system region" setting
- [WebSelectEnabled](/DeployEdge/microsoft-edge-policies#webselectenabled) - Web Select Enabled
- [WebSQLAccess](/DeployEdge/microsoft-edge-policies#websqlaccess) - Force WebSQL to be enabled
- [WebSQLNonSecureContextEnabled](/DeployEdge/microsoft-edge-policies#websqlnonsecurecontextenabled) - Force WebSQL in non-secure contexts to be enabled

#### Deprecated policy

- [MicrosoftOfficeMenuEnabled](/DeployEdge/microsoft-edge-policies#microsoftofficemenuenabled) - Allow users to access the Microsoft Office menu

#### Obsoleted policy

- [BuiltinCertificateVerifierEnabled](/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) - Determines whether the built-in certificate verifier will be used to verify server certificates

## Version 106.0.1370.52: October 20, 2022

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 106.0.1370.47: October 14, 2022

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-14-2022).

## Version 106.0.1370.42: October 10, 2022

Fixed various bugs and performance issues.

## Version 106.0.1370.37: October 6, 2022

Fixed various bugs and performance issues.

## Version 106.0.1370.34: October 3, 2022

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-3-2022).

### Feature updates

- **More reliable web defense.** Browse the web with more reliable protection thanks to the rewritten [Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) library for Microsoft Edge on Windows and macOS. The new SmartScreen library was first made available on Windows with Microsoft Edge version 103, and now makes its debut on macOS with Microsoft Edge version 106. The [NewSmartScreenLibraryEnabled](/deployedge/microsoft-edge-policies#newsmartscreenlibraryenabled) policy is now deprecated in Microsoft Edge version 106 and will be obsolete in Microsoft Edge version 108.

- **Increased Work Results in the Microsoft Edge address bar.** We've increased the maximum number of work results that display in the address bar from 2 to 4, which offers greater visibility into the work content available to you as you search. This feature requires the [AddressBarMicrosoftSearchInBingProviderEnabled](/deployedge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled) policy enabled to work.

### Policy updates

#### New policies

- [EfficiencyModeEnabled](/DeployEdge/microsoft-edge-policies#efficiencymodeenabled) - Efficiency mode enabled
- [EfficiencyModeOnPowerEnabled](/DeployEdge/microsoft-edge-policies#efficiencymodeonpowerenabled) - Enable efficiency mode when the device is connected to a power source
- [InternetExplorerIntegrationAlwaysUseOSCapture](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationalwaysuseoscapture) - Always use the OS capture engine to avoid issues with capturing Internet Explorer mode tabs

#### Deprecated policies

- [NewSmartScreenLibraryEnabled](/DeployEdge/microsoft-edge-policies#newsmartscreenlibraryenabled) - Enable new SmartScreen library
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) - Configure ShadowStack crash rollback behavior

#### Obsoleted policies

- [OutlookHubMenuEnabled](/DeployEdge/microsoft-edge-policies#outlookhubmenuenabled) - Allow users to access the Outlook menu
- [EdgeDiscoverEnabled](/DeployEdge/microsoft-edge-policies#edgediscoverenabled) - Discover feature In Microsoft Edge

## Version 105.0.1343.53: September 26, 2022

Fixed various bugs and performance issues.

## Version 105.0.1343.50: September 22, 2022

Fixed various bugs and performance issues.

## Version 105.0.1343.42: September 15, 2022

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-15-2022).

## Version 104.0.1293.91: September 15, 2022

Fixed various bugs and performance issues for Extended Stable release.

## Version 105.0.1343.33: September 8, 2022

Fixed various bugs and performance issues.

## Version 104.0.1293.81: September 2, 2022

> [!IMPORTANT]
> This update to Extended Stable contains a fix for [CVE-2022-3075](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-3075), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-2-2022)

## Version 105.0.1343.27: September 2, 2022

> [!IMPORTANT]
> This update contains a fix for [CVE-2022-3075](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-3075), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-2-2022).

## Version 105.0.1343.25: September 1, 2022

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-1-2022).

### Feature updates

- **Enhanced security mode improvements.** Enhanced security mode now supports WebAssembly for x64 Windows. More cross-platform support is expected in the future. For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **Improvement to the Cloud Site List Management experience for IE mode.**

  - You can restore to one of the last 3 published versions of your site list in the Microsoft 365 Admin Center. For more information, see [Restore a previous version of a site list](/deployedge/edge-ie-mode-cloud-site-list-mgmt#restore-a-previous-version-of-a-site-list).
  - You can identify gaps in your enterprise site list by configuring reporting of site feedback with the [InternetExplorerIntegrationCloudUserSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) and [InternetExplorerIntegrationCloudNeutralSitesReporting policies](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting). You can view local site list URLs from users and potentially misconfigured neutral site URLs in the Microsoft Edge site lists experience in the Microsoft 365 Admin Center. To learn more, see [View site feedback on the Microsoft 365 Admin Center](/deployedge/edge-ie-mode-cloud-site-list-mgmt#view-site-feedback-on-the-microsoft-365-admin-center-1).
  - You can configure session cookie sharing between Microsoft Edge and Internet Explorer for IE mode on your site list in the Microsoft 365 Admin Center. To learn more, see [Cookie sharing between Microsoft Edge and Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

- **Improvements to the Cloud Site List Management experience for IE mode now available in GCC.** GCC customers can now utilize the full Microsoft Edge site list experience in the Microsoft 365 Admin Center.

### Policy updates

#### New policies

- [ExemptFileTypeDownloadWarnings](/DeployEdge/microsoft-edge-policies#exemptfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains
- [InternetExplorerIntegrationAlwaysWaitForUnload](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationalwayswaitforunload) - Wait for Internet Explorer mode tabs to completely unload before ending the browser session
- [MicrosoftEditorProofingEnabled](/DeployEdge/microsoft-edge-policies#microsofteditorproofingenabled) - Spell checking provided by Microsoft Editor
- [MicrosoftEditorSynonymsEnabled](/DeployEdge/microsoft-edge-policies#microsofteditorsynonymsenabled) - Synonyms are provided when using Microsoft Editor spell checker
- [PrintPdfAsImageDefault](/DeployEdge/microsoft-edge-policies#printpdfasimagedefault) - Print PDF as Image Default
- [UnthrottledNestedTimeoutEnabled](/DeployEdge/microsoft-edge-policies#unthrottlednestedtimeoutenabled) - JavaScript setTimeout won't be clamped until a higher nesting threshold is set

#### Deprecated policies

- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains

#### Additional policy changes

- [GuidedSwitchEnabled](/DeployEdge/microsoft-edge-policies#guidedswitchenabled) - Add Linux platform support

## Version 104.0.1293.78: September 1, 2022

Fixed various bugs and performance issues for Extended Stable release.

## Version 104.0.1293.70: August 25, 2022

Fixed various bugs and performance issues.

## Version 104.0.1293.63: August 19

> [!IMPORTANT]
> This update contains a fix for [CVE-2022-2856](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-2856), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-19-2022).

### Feature updates

- **Search in the Microsoft Edge sidebar.** Easily access an updated sidebar search via Microsoft Edge sidebar, including easy access to Microsoft Search in Bing for organizations. Note: This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Gaming for the Microsoft Edge sidebar.** Play popular casual games for free. Administrators can control the availability of the Games menu in the Microsoft Edge sidebar. Note: This feature is a controlled rollout. If you don't see this feature, check back as we continue our rollout.

- **Discover in the Microsoft Edge sidebar.** Discover content relevant to the page you're browsing including summaries, source information, and more. Note: This is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Get your favorite tools in the Microsoft Edge sidebar.** Easily access commonly used tools while you browse the web, including Calculator, Internet speed test, and Unit converter. Note: This is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Outlook in the Microsoft Edge sidebar.** Quickly and easily access Outlook Mail and Calendar. Note: This is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Office in the Microsoft Edge sidebar.** Quickly and easily access Microsoft Office documents and apps. Administrators can control the Microsoft Office menu in the Microsoft Edge sidebar. Note: This is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

## Version 104.0.1293.54: August 11

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 104.0.1293.47: August 5

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-5-2022).

### Feature updates

- **Enhance your security on the web**. Improvements to **Enhance your security on the web** in *edge://settings/privacy* now include **Basic** as the new default option. With this option, Microsoft Edge applies added security protection to the less visited sites. This feature preserves the user experience for the most popular sites on the web. For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **Import Chrome data without Chrome during First Run Experience.** This feature lets a user bring in their Chrome data by logging in to their Google account during Microsoft Edge's First Run Experience. This feature can be turned off by disabling First Run Experience with the [HideFirstRunExperience](/deployedge/microsoft-edge-policies#hidefirstrunexperience) policy, or by setting [AutoImportAtFirstRun](/deployedge/microsoft-edge-policies#autoimportatfirstrun) to 'DisabledAutoImport'.

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

## Version 103.0.1264.77: July 28

Fixed various bugs and performance issues.

## Version 102.0.1245.62: July 27

Fixed various bugs and performance issues for Extended Stable release.

## Version 103.0.1264.71: July 22

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#july-22-2022).

## Version 103.0.1264.62: July 14

Fixed various bugs and performance issues. We recommend that users install this update to address the following issue.

### Known issue

Microsoft Edge on 32-bit (x86) Windows 10 Version 1809 might experience startup issues with the upcoming July Non-Security Windows Updates (KB5015880 - 17763.3224).  issue is fixed with the latest Microsoft Edge Stable channel release, version 103.0.1264.62. Enterprise users encountering this issue on Microsoft Edge Extended Stable channel version 102 need to disable the  [NewSmartScreenLibraryEnabled](/deployedge/microsoft-edge-policies#newsmartscreenlibraryenabled) policy.

## Version 103.0.1264.49: July 6

> [!Important]
> This update contains a fix for [CVE-2022-2294](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-2294), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#july-6-2022).

## Version 102.0.1245.56: July 6

Fixed various bugs and performance issues for Extended Stable release.

## Version 103.0.1264.44: June 30

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-30-2022).

## Version 102.0.1245.50: June 23

Fixed various bugs and performance issues for Extended Stable release.

## Version 103.0.1264.37: June 23

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-23-2022).

### Feature updates

- **Ability to control automatic profile switching.** The [GuidedSwitchEnabled](/DeployEdge/microsoft-edge-policies#guidedswitchenabled) policy lets Microsoft Edge prompt the user to switch to the appropriate profile when Microsoft Edge detects that a link is a personal or work link.

- **Client Certificate Switcher.** This feature offers a way for users to clear the remembered certificate and resurface the certificate picker when visiting a site requiring http certificate authentication. Switching can be done without manually quitting Microsoft Edge.

- **More reliable web defense.** Browse the web with more reliable protection thanks to the rewritten [Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) library for Microsoft Edge on Windows. The [NewSmartScreenLibraryEnabled](microsoft-edge-policies.md#newsmartscreenlibraryenabled) policy allows enterprise customers to continue using the legacy version of the library until it's deprecated in Microsoft Edge version 105.

- **Work Search Banner in the Microsoft Edge address bar.** This banner helps you stay in the flow of your work by narrowing your search focus to work-only results. To see work focused results from your organization, select the banner at the beginning of your search. To be directed to your organization's workplace search results page, select the banner at any point of your search. Use the [AddressBarMicrosoftSearchInBingProviderEnabled](/deployedge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled) policy to turn this feature on or off.

### Policy updates

#### New policies

- [GuidedSwitchEnabled](/DeployEdge/microsoft-edge-policies#guidedswitchenabled) - Guided Switch Enabled
- [InternetExplorerZoomDisplay](/DeployEdge/microsoft-edge-policies#internetexplorerzoomdisplay) - Display zoom in IE Mode tabs with DPI Scale included like it is in Internet Explorer
- [LiveCaptionsAllowed](/DeployEdge/microsoft-edge-policies#livecaptionsallowed) - Live captions allowed
- [OriginAgentClusterDefaultEnabled](/DeployEdge/microsoft-edge-policies#originagentclusterdefaultenabled) - Origin-keyed agent clustering enabled by default

#### Additional policy changes

- [SleepingTabsTimeout](/DeployEdge/microsoft-edge-policies#sleepingtabstimeout) - Set the background tab inactivity timeout for sleeping tabs. **Note:** A timeout of 30 seconds of inactivity was added to this policy.

## Version 102.0.1245.44: June 16

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 102.0.1245.41: June 13

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-13-2022).

## Version 102.0.1245.39: June 9

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-9-2022).

## Version 102.0.1245.33: June 3

Fixed various bugs and performance issues for Stable and Extended Stable release.

## Version 102.0.1245.30: May 31, 2022

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-31-2022).

### Policy updates

#### New policies

- [AllHttpAuthSchemesAllowedForOrigins](/DeployEdge/microsoft-edge-policies#allhttpauthschemesallowedfororigins) - List of origins that allow all HTTP authentication
- [OutlookHubMenuEnabled](/DeployEdge/microsoft-edge-policies#outlookhubmenuenabled) - Allow users to access the Outlook menu
- [NetworkServiceSandboxEnabled](/DeployEdge/microsoft-edge-policies#networkservicesandboxenabled) - Enable the network service sandbox
- [UserAgentClientHintsGREASEUpdateEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsgreaseupdateenabled) - Control the User-Agent Client Hints GREASE Update feature

## Version 101.0.1210.53: May 19, 2022

Fixed various bugs and performance issues.

## Version 100.0.1185.60: May 13, 2022

Fixed various bugs and performance issues for Extended Stable release.

## Version 101.0.1210.47: May 13, 2022

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-13-2022).

## Version 101.0.1210.39: May 5, 2022

Fixed various bugs and performance issues.

## Version 100.0.1185.57: May 2, 2022

Fixed various bugs and performance issues for Extended Stable release.

## Version 101.0.1210.32: April 28

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-28-2022).

### Feature updates

- **Ability to set the default profile.** The [EdgeDefaultProfileEnabled](/DeployEdge/microsoft-edge-policies#edgedefaultprofileenabled) policy lets you set a default profile to use when opening the browser instead of the last profile that was used. This policy won't be applicable if the `--profile-directory` parameter has been specified.

- **Launch Progressive Web Apps (PWAs) from the favorites bar.** Improvements to the PWA launch experience starts appearing with an Apps icon that can be added to the toolbar.

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

- **Hardware-enforced Stack Protection.** Microsoft Edge continues supporting more fine-grained protection by combating memory corruption vulnerabilities and by protecting indirect calls. Hardware-enforced stack protection is only supported by Windows 8 and later. For more information, see [Hardware-enforced Stack Protection](https://techcommunity.microsoft.com/t5/windows-kernel-internals-blog/developer-guidance-for-hardware-enforced-stack-protection/ba-p/2163340). This feature behavior can be controlled using the [ShadowStackCrashRollbackBehavior](/deployedge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) policy.

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

## Version 99.0.1150.30: March 3

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#march-3-2022).

### Feature updates

- **Upcoming three-digit version number in user agent string.** Starting with version 100, Microsoft Edge sends a three-digit version number in the User-Agent header, for example "Edg/100". Starting with Microsoft Edge 97, site owners can test this upcoming agent string by enabling the **#force-major-version-to-100** experiment flag in *edge://flags* to ensure their User-Agent parsing logic is robust and works as expected.

- **Personalize multi-profile experiences with profile preferences for sites.** Users can personalize their multi-profile experience with the ability to create a customized list of sites for automatic profile switching in Microsoft Edge.

- **Navigate PDF documents using page thumbnails.** You'll now be able to navigate through your PDF document using thumbnails that represent the pages. These thumbnails appear in the pane on the left side of the PDF reader.

- **Configure the list of domains for which the password manager User Interface (UI) for Save and Fill will be disabled.** Use the [PasswordManagerBlocklist](/deployedge/microsoft-edge-policies#passwordmanagerblocklist) policy to configure the list of domains (HTTP/HTTPS schemas and hostnames only) where Microsoft Edge should disable the password manager. This means that Save and Fill workflows will be disabled, which ensures that passwords for those websites can't be saved or auto filled into web forms.

- **Custom primary password.** The browser already has the capability where users can add an authentication step before saved passwords are auto filled in web forms. This adds another layer of privacy and helps prevent unauthorized users from using saved passwords to sign in to websites. Custom primary password is an evolution of that same feature, where users will now be able to use a custom string of their choice as their primary password. After it's enabled, users will enter this password to authenticate themselves and have their saved passwords auto filled into web forms.

### Policy updates

#### New Policies

- [DoNotSilentlyBlockProtocolsFromOrigins](/DeployEdge/microsoft-edge-policies#donotsilentlyblockprotocolsfromorigins) - Define a list of protocols that aren't silently blocked by anti-flood protection
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

- **Upcoming three-digit version number in user agent string.** Starting with version 100, Microsoft Edge sends a three-digit version number in the User-Agent header, for example "Edg/**100**". Starting with Microsoft Edge 97, site owners can test this upcoming user agent string by enabling the **#force-major-version-to-100** experiment flag in *edge://flags* to ensure their User-Agent parsing logic is robust and works as expected.

- **Deprecate WebRTC's Plan B SDP semantics.** This change deprecates a legacy Session Description Protocol (SDP) dialect called Plan B. This SDP format is being replaced by the Unified Plan, which is a spec-compliant and cross-browser compatible SDP format. For more information, see the Chrome Platform Status entry [PSA: Plan B should throw in M96 Beta and Stable](https://chromestatus.com/feature/5823036655665152), and [PSA: Plan B throwing in Stable and Extended Deprecation Trial End Date](https://groups.google.com/g/discuss-webrtc/c/gEHrZyYKsfU). Requesting a [Trial for RTCPeerConnection Plan B SDP Semantics](https://developer.chrome.com/origintrials/#/view_trial/3892235977954951169) allows sites to continue to use the deprecated API until version 101.

- **Overlay scrollbars added to Microsoft Edge.** We've updated our scrollbars with an overlay-based design. Users can turn on this feature in *edge://flags*.

### Policy updates

#### New Policies

- [AddressBarEditingEnabled](/DeployEdge/microsoft-edge-policies#addressbareditingenabled) - Configure address bar editing
- [AllowGamesMenu](/DeployEdge/microsoft-edge-policies#allowgamesmenu) - Allow users to access the games menu
- [EdgeFollowEnabled](/DeployEdge/microsoft-edge-policies#edgefollowenabled) - Enable Follow service in Microsoft Edge
- [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode) - Enhance the security state in Microsoft Edge
- [EnhanceSecurityModeBypassListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodebypasslistdomains) - Configure the list of domains for which enhance security mode won't be enforced
- [EnhanceSecurityModeEnforceListDomains](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeenforcelistdomains) - Configure the list of domains for which enhance security mode will always be enforced
- [InAppSupportEnabled](/DeployEdge/microsoft-edge-policies#inappsupportenabled) - In-app support Enabled
- [MicrosoftEdgeInsiderPromotionEnabled](/DeployEdge/microsoft-edge-policies#microsoftedgeinsiderpromotionenabled) - Microsoft Edge Insider Promotion Enabled
- [PrintStickySettings](/DeployEdge/microsoft-edge-policies#printstickysettings) - Print preview sticky settings
- [SandboxExternalProtocolBlocked](/DeployEdge/microsoft-edge-policies#sandboxexternalprotocolblocked) - Allow Microsoft Edge to block navigation to external protocols in a sandboxed iframe
- [U2fSecurityKeyApiEnabled](/DeployEdge/microsoft-edge-policies#u2fsecuritykeyapienabled) - Allow using the deprecated U2F Security Key API

## Version 97.0.1072.76: January 27

Fixed various bugs and performance issues.

### Feature updates

- **Upcoming three-digit version number in user agent string.** Starting with version 100, Microsoft Edge sends a three-digit version number in the User-Agent header, for example "Edg/**100**". Starting with Microsoft Edge 97, site owners can test this upcoming user agent string by enabling the **#force-major-version-to-100** experiment flag in *edge://flags* to ensure their User-Agent parsing logic is robust and works as expected.

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

- **Use the current profile to sign into websites when multiple work or school accounts are signed in on a device.** When multiple work or school accounts are signed in on a device, users are asked to choose an account from the account picker to continue their visits to websites. In this release, users are prompted to let Microsoft Edge sign in to the websites automatically with the work or school account that's signed into the current profile. Users can turn this feature on and off in **Settings** > **Profile preferences**.

- **Add support for Microsoft Endpoint Data Loss Prevention (DLP) on macOS.** Microsoft Endpoint DLP policy enforcement is available natively on macOS.

- **Automatic HTTPS.** Users can upgrade navigation from HTTP to HTTPS on domains likely to support this more secure protocol. This support can also be configured to attempt delivery over HTTPS for all domains. Note: This feature is a Controlled Feature Rollout. If you don't see this feature, check back as we continue our rollout.

- **Block WebSQL in 3rd-party contexts.** Use of the legacy WebSQL feature will be blocked from 3rd-party frames. The [WebSQLInThirdPartyContextEnabled](/deployedge/microsoft-edge-policies#websqlinthirdpartycontextenabled) policy is available as an opt-out option until Microsoft Edge version 101. This change is happening in the Chromium project that Microsoft Edge is based on. For more information, see this [Chrome Platform Status](https://chromestatus.com/feature/5684870116278272) entry.

- **Citations in Microsoft Edge.** Citing sources for research is a common requirement for students. They have to manage many research references and sources, which aren't easy tasks. They also have to translate these citations to proper citation formats like APA, MLA, and Chicago. This new "Citations" feature, now in Preview in Microsoft Edge, gives students a better way to manage and generate citations as they research online. With Citations turned on in Collections or from **Settings and more (Alt-F)**, Microsoft Edge automatically generates citations that students can use later so they can stay focused on their research. When they're done, they can easily compile these citations into a final deliverable. For more information, see [Previewing Citations in Microsoft Edge](https://blogs.windows.com/msedgedev/2021/11/04/preview-citations-feature-edge/).

- **Control Flow Guard (CFG).** Microsoft Edge starts supporting more fine-grained protection by combating memory corruption vulnerabilities and by protecting indirect calls. CFG is only supported with Windows 8 and later. For more information, see [Control Flow Guard](/windows/win32/secbp/control-flow-guard).
  
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

## Version 96.0.1054.29: November 19

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#november-19-2021).

### Feature updates

- **Cloud Site List Management for IE mode in Public Preview.** Cloud Site List Management lets you manage your site lists for IE mode in the cloud without needing an on-premises infrastructure to host your organization's site list. You can access the Cloud Site List Management feature using the Microsoft Edge Site Lists experience in the Microsoft 365 Admin Center. To learn more, see the [Cloud Site List Management for IE mode (Public Preview)](./edge-ie-mode-cloud-site-list-mgmt.md) article.
  
- **Improved handoff between IE mode and the modern browser.** Starting with this version of Microsoft Edge, navigation between Microsoft Edge and Internet Explorer mode includes form data and extra HTTP headers. Referrer headers, post data, forms data, and request methods are forwarded correctly across the two experiences. You can specify which data types should be included using the InternetExplorerIntegrationComplexNavDataTypes policy. For more information, see this FAQ: [My application requires transferring POST data between IE mode and Microsoft Edge. Is this supported?](./edge-ie-mode-faq.md#my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported)

- **Update Microsoft Edge WebView2 using WSUS.** IT Admins using Windows Server Update Services (WSUS) to update Microsoft Edge will also be able to update Microsoft Edge WebView2 using WSUS. This capability gives admins an easier servicing process for offline devices.

- **WSUS updates for Server.** WSUS and Catalog updates for Microsoft Edge channels (Stable, Beta, and Dev) will now apply to Windows Server SKUs that have Microsoft Edge installed, including Windows Server 2022. For more information on how to configure WSUS updates for Microsoft Edge, see [Update Microsoft Edge](/mem/configmgr/apps/deploy-use/deploy-edge).

- **Microsoft Edge AutoLaunch Protocols Component.** Microsoft Edge 96 introduces the AutoLaunch Protocols [Component](https://textslashplain.com/2019/07/16/updating-browsers-quickly-flags-respins-and-components/) that contains lists of scheme-origin dictionaries to automatically allow or block. This protects customers from dangerous schemes (for example, a protocol handler with a 0-day) while eliminating prompts from known-safe pairings (for example, the Teams website can open the Teams client app). If for some reason, you don't want Microsoft Edge to block vulnerable protocol handlers and allow known-safe pairings, use the toggle in *edge://settings/content/applicationLinks*, or set the [AutoLaunchProtocolsComponentEnabled](/deployedge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) policy to False.

- **Launch Progressive Web App (PWA) directly via protocol links.** Let installed PWAs handle links that use a specific protocol for a more integrated experience.

- **Quickly view Office files in the browser.** Users can now view Office files including documents, spreadsheets, and presentations that they come across while browsing on Microsoft Edge right in the browser without needing to download the file and then open it in a different application. There will be no changes in the file open experience for Office files that are hosted on OneDrive or SharePoint.
  
- **Freeform highlighting on PDFs.** The PDF viewing and markup experience are improved with the addition of freeform highlighters. You can highlight sections in PDFs that you don't have access to, and scanned documents.

- **Hardware-enforced Stack Protection.** Microsoft Edge begins supporting an even safer browsing mode that uses hardware-dependent control flow for browser processes on supported hardware (Intel 11th Gen. or AMD Zen 3). Note: Because this is a Controlled Feature Rollout, you might not notice this feature enabled on all devices. You can enable or disable Hardware-enforced Stack Protection by manipulating Image File Execution Options (IFEO) using group policy.

- **New warning dialog for typosquatting sites.** The browser shows a warning on some sites with URLs that look similar to other sites. This UI uses client-side heuristics to warn users about sites that might be spoofing popular web sites. For more information, see [What is typosquatting?](https://support.microsoft.com/topic/what-is-typosquatting-54a18872-8459-4d47-b3e3-d84d9a362eb0).
  
- **Dictionary added to mini-toolbar in Immersive Reader.**  We're adding dictionary functionality to the mini-toolbar to help your reading and research. You are able to look up the spelling and definitions of words more quickly and easily in the Immersive Reader experience.
  
- **Learn how to solve math problems with Math Solver.** We're excited to announce that you can use Math Solver in Microsoft Edge to get help with a wide range of mathematical concepts. These concepts range from elementary arithmetic and quadratic equations to trigonometry and calculus. Math Solver lets you take a picture of a handwritten or printed math problem and then provides an instant solution with step-by-step instructions to help you learn how to reach the solution without help. Math Solver also comes with a mathematical keyboard that you can use to easily type math problems. This keyboard eliminates the need to search around a traditional keyboard to find the math characters you need. After solving your problem, Math Solver provides options to continue learning with quizzes, worksheets, and video tutorials.

- **Split tunnel VPN support for WebRTC.** Allows enterprise customers to gain the benefit of VPN split tunneling for peer-to-peer traffic on Microsoft Edge. You can enable this feature using the [WebRtcRespectOsRoutingTableEnabled](/deployedge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) policy.

### Policy updates

#### New Policies

- [ApplicationGuardUploadBlockingEnabled](/DeployEdge/microsoft-edge-policies#applicationguarduploadblockingenabled) - Prevents files from being uploaded while in Application Guard
- [AudioProcessHighPriorityEnabled](/DeployEdge/microsoft-edge-policies#audioprocesshighpriorityenabled) - Allow the audio process to run with priority above normal on Windows
- [AutoLaunchProtocolsComponentEnabled](/DeployEdge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) - AutoLaunch Protocols Component Enabled
- [EfficiencyMode](/DeployEdge/microsoft-edge-policies#efficiencymode) - Configure when efficiency mode should become active
- [ForceSyncTypes](/DeployEdge/microsoft-edge-policies#forcesynctypes) - Configure the list of types that are included for synchronization
- [InternetExplorerIntegrationComplexNavDataTypes](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) - Configure whether form data and HTTP headers will be sent when entering or exiting Internet Explorer mode
- [InternetExplorerModeToolbarButtonEnabled](/DeployEdge/microsoft-edge-policies#internetexplorermodetoolbarbuttonenabled) - Show the Reload in Internet Explorer mode button in the toolbar
- [PrintPostScriptMode](/DeployEdge/microsoft-edge-policies#printpostscriptmode) - Print PostScript Mode
- [PrintRasterizePdfDpi](/DeployEdge/microsoft-edge-policies#printrasterizepdfdpi) - Print Rasterize PDF DPI
- [RendererAppContainerEnabled](/DeployEdge/microsoft-edge-policies#rendererappcontainerenabled) - Enable renderer in app container
- [SharedLinksEnabled](/DeployEdge/microsoft-edge-policies#sharedlinksenabled) - Show links shared from Microsoft 365 apps in History
- [TyposquattingCheckerEnabled](/DeployEdge/microsoft-edge-policies#typosquattingcheckerenabled) - Configure Edge TyposquattingChecker

## Version 95.0.1020.53: November 12

Fixed various bugs and performance issues.

## Version 95.0.1020.44: November 4

Fixed various bugs and performance issues.

## Version 94.0.992.58: October 30

Fixed various bugs and performance issues for Extended Stable release.

## Version 95.0.1020.40: October 29

> [!IMPORTANT]
> This update contains a fix for [CVE-2021-38000](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-38000) and [CVE-2021-38003](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-38003) which have been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide)

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-29-2021).

## Version 95.0.1020.38: October 28

Fixed various bugs and performance issues.

## Version 94.0.992.57: October 27

Fixed various bugs and performance issues for Extended Stable release.

## Version 95.0.1020.30: October 21

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-21-2021).

### Feature updates

- **View in File Explorer support for SharePoint Online libraries in Microsoft Edge.**  Now you can enable the View in File Explorer capability on SharePoint Online Modern Document Libraries. For this experience to be visible and work for your users, you need to enable the Microsoft Edge policy [Configure the View in File Explorer feature for SharePoint pages in Microsoft Edge](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) and update your SharePoint Online tenant configuration. Learn more: [View SharePoint files with File Explorer in Microsoft Edge](/SharePoint/sharepoint-view-in-edge).

- **Intranet zone file URL links will open in Windows File Explorer.**  You can allow file URL links to intranet zone files originating from intranet zone HTTPS websites to open Windows File Explorer for that file or directory. You can enable this experience using the [IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled) policy.

- **Improvements to the downloads experience.** Support for the download user experience is extended to progressive web applications PWAs and WebView. We'll also begin to support drag and drop to the File Explorer and Desktop.

- **Pick up where you left off on PDF documents.**  You'll now be able to resume reading from where you last closed your PDF document.

- **Efficiency mode extends battery life when your laptop enters battery saver mode.**  Efficiency mode becomes active when your laptop enters battery saver mode to allow the browser to manage resource usage to extend the battery life of your machine. You'll have four options when efficiency mode becomes active: Unplugged and low battery, Unplugged, Always, and Never. Note: This feature is a Controlled Feature Rollout. If you don't see this feature, check back shortly as we continue our rollout.

- **Free form text boxes added to PDF documents.** We now support adding free form text boxes to PDF documents. You can use these boxes to fill in forms and add visible notes.

- **Citation support added to Collections.**  We've improved the Collections experience, especially for students and researchers. Collections will start supporting citations and reading lists.

- **Update your passwords faster and with fewer clicks.** The browser will now take you directly to the Change Password page for a given website. This action saves you time and clicks by removing the need to navigate to the page manually. After you're on this page, the browser will also autofill your existing password and suggest a strong, unique new password.  Note: Currently this feature is only available on a limited number of sites.

- **Auto-account creation.** We now provide extra support on Sign-Up pages by allowing you to create an online account with one click. You can do this by selecting the suggestion drop-down when you click on any form field in the Sign-Up form. Doing so shows not only information relevant to the Sign-Up form, but also a strong new password suggestion. Upon selection, all the relevant information gets populated in the respective fields and the suggested password are automatically stored on submission to the website. Note: Currently this feature is only available on a limited number of sites.

### Policy updates

#### New Policies

- [BrowserLegacyExtensionPointsBlockingEnabled](/DeployEdge/microsoft-edge-policies#browserlegacyextensionpointsblockingenabled) Enable browser legacy extension point blocking
- [CrossOriginWebAssemblyModuleSharingEnabled](/DeployEdge/microsoft-edge-policies#crossoriginwebassemblymodulesharingenabled) Specifies whether WebAssembly modules can be sent cross-origin
- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) Specifies whether the display-capture permissions-policy is checked or skipped
- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) Configure the pixel adjustment between window.open heights sourced from IE mode pages vs. Edge mode pages
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenwidthadjustment) Configure the pixel adjustment between window.open widths sourced from IE mode pages vs. Edge mode pages
- [IntranetFileLinksEnabled](/DeployEdge/microsoft-edge-policies#intranetfilelinksenabled) Allow intranet zone file URL links from Microsoft Edge to open in Windows File Explorer
- [NewSmartScreenLibraryEnabled](/DeployEdge/microsoft-edge-policies#newsmartscreenlibraryenabled) Enable new SmartScreen library
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) Configure ShadowStack crash rollback behavior
- [VisualSearchEnabled](/DeployEdge/microsoft-edge-policies#visualsearchenabled) Visual search enabled

#### Obsoleted Policies

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) Allow Internet Explorer mode testing
- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Enable default legacy SameSite cookie behavior setting

## Version 94.0.992.50: October 14

Fixed various bugs and performance issues.

## Version 94.0.992.47: October 11

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-11-2021).

## Version 94.0.992.38: October 1

> [!Important]
> This update contains a fix for [CVE-2021-37975](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37975) and [CVE-2021-37976](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37976) which have been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide)

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-01-2021).

## Version 94.0.992.37: September 30

Fixed various bugs & performance issues.

## Version 94.0.992.31: September 24

> [!Important]
> This update contains a fix for [CVE-2021-37973](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37973) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-24-2021).

### Feature updates

- **Microsoft Edge has completed the move to a 4-week cadence for updates.**  We have adopted a new 4-week release cycle for major versions. Read more here: https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/

- **New Extended stable option being offered.**  We're offering a new Extended Stable option to our managed Enterprise customers. The Extended Stable option stays on even numbered revisions and update every eight weeks. There will be a biweekly security update.  Additional information here: https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **Improvements to default behavior of opening MHTML files.**  MHTML files continue to open in IE mode if IE mode is enabled, unless the MHTML file was saved from Microsoft Edge (using the Save As or Save Page As options in Microsoft Edge). If the file was saved from Microsoft Edge, it will now open in Microsoft Edge.  This change fixes a rendering issue that was observed when opening an MHTML file in IE mode when saved from Microsoft Edge.

- **Restrict private network requests to secure contexts.** Access to resources on local (intranet) networks from pages on the internet requires that those pages be delivered over HTTPS. This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, navigate to the [Chrome Platform Status entry](https://chromestatus.com/feature/5436853517811712). Two compatibility policies are available to support scenarios that need to preserve compatibility with non-secure pages: [InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) and [InsecurePrivateNetworkRequestAllowedForUrls](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls).

- **Block mixed content downloads.** Secure pages will only download files hosted on other secure pages, and downloads hosted on non-secure (non-HTTPS) pages will be blocked if initiated from a secure page. This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, navigate to the [Google security blog entry](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html).

- **Enable implicit sign-in for on-premises accounts.** By enabling the [OnlyOnPremisesImplicitSigninEnabled](/deployedge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) policy, only on-premises accounts will be enabled for implicit sign-in.  Microsoft Edge won't attempt to implicitly sign in to MSA or Microsoft Entra accounts. Upgrade from on-premises accounts to Microsoft Entra accounts will be stopped as well.

- **New accessibility settings page.**  We have brought accessibility-related settings together on a single page. You can find the new edge://settings/accessibility page under the main settings list. Here you can find settings to make the web page bigger, show a high visibility outline around the area of focus and other settings that can help improve your web browsing experience. We'll continue to add new settings here in future versions of Microsoft Edge.

***New Policies***

- [ApplicationGuardPassiveModeEnabled](/DeployEdge/microsoft-edge-policies#applicationguardpassivemodeenabled) Ignore Application Guard site list configuration and browse Edge normally
- [OnlyOnPremisesImplicitSigninEnabled](/DeployEdge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) Only on-premises account enabled for implicit sign-in
- [WebRtcRespectOsRoutingTableEnabled](/DeployEdge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) Enable support for Windows OS routing table rules when making peer to peer connections via WebRTC

***Obsoleted Policy***

- [UserAgentClientHintsEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) Enable the User-Agent Client Hints feature

## Version 93.0.961.52: September 16

>[!Important]
>This update contains a fix for [CVE-2021-30633](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30632) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-16-2021).

## Version 93.0.961.47: September 11

> [!Important]
> This update contains a fix for [CVE-2021-30632](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30632) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-11-2021).

## Version 93.0.961.44: September 9

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-09-2021).

## Version 93.0.961.38: September 2

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-02-2021).

### Feature updates

- **Initial Preferences in Microsoft Edge.**  Microsoft Edge now supports a limited number of Initial Preferences (formerly Master Preferences). IT admins can deploy these settings as default before the browser is run for the first time by their users. Additional information here: [Configure Microsoft Edge using Initial Preferences settings for the first run](/deployedge/initial-preferences-support-on-microsoft-edge-browser).

- **IE mode on Microsoft Edge will support "no-merge" behavior.**  For an end-user, when a new browser window is launched from an IE mode application, it is in a separate session, similar to the no-merge behavior in IE11. You'll need to adjust your site list to configure sites that need to prevent session sharing as "no-merge". Behind the scenes, for each window of Microsoft Edge, the first time an IE mode tab is visited within that window, if it's one of the designated "no-merge" sites, that window is locked into a different "no-merge" IE session from all other Microsoft Edge windows at least until the last IE mode tab is closed in that window. This follows previous behavior where users could launch IE with no-merge and could also launch Microsoft Edge without no-merge via other mechanisms.  Additional information here: [IE mode troubleshooting and FAQ | Microsoft Docs](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--nomerge--option-that-was-supported-in-internet-explorer-11-)

- **New policy to stop implicit sign in.**  The [ImplicitSignInEnabled](/deployedge/microsoft-edge-policies#implicitsigninenabled) policy allows system administrators to disable implicit sign-in on Microsoft Edge browsers.

- **Policies to bypass ClickOnce and DirectInvoke prompts.** We have updated our policies to enable bypassing ClickOnce's prompts and DirectInvoke's app for specified file types, from specified domains. To do this, you'll need to:

  - Enable [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) or [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - Enable [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes) policy and set the list of specific file types that ClickOnce and DirectInvoke should be disabled for
  - Enable the [AutoOpenAllowedForURLs](/deployedge/microsoft-edge-policies#autoopenallowedforurls) policy and set the list of specific domains that ClickOnce and DirectInvoke will be disabled for.

  Note: AutoOpenAllowedForURLs is a supporter policy for AutoOpenFileTypes. If AutoOpenAllowedForURLs isn't set and AutoOpenFileTypes is set, then file types listed will automatically open from all URLs.

- **Tab Groups.**  We're turning on tab grouping that provides the ability to categorize tabs into user-defined groups and helps you more effectively find, switch, and manage tabs across multiple workstreams.  

- **Hide the title bar while using Vertical Tabs.**  Get the extra few pixels back by hiding the browser's title bar, while in Vertical Tabs. Now you can go to edge://settings/appearance and under the Customize Toolbar section select the option to hide the title bar while in Vertical Tab mode.

- **Video Picture in Picture (PiP) from hover toolbar.**  When you hover over a supported video, a toolbar appears that allows you to view that video in a PiP window.  Note: This is currently available for Microsoft Edge users on macOS.  

- **Removal of 3DES in TLS. Support for the TLS_RSA_WITH_3DES_EDE_CBC_SHA cipher suite will be removed.** This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, navigate to the [Chrome Platform Status entry](https://chromestatus.com/feature/6678134168485888). Additionally, in Microsoft Edge version 93, the [TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled) policy is available to support scenarios that need to preserve compatibility with outdated servers. This compatibility policy becomes obsolete and stop working in Microsoft Edge version 95. Ensure that you update affected servers before then.

***New Policies***

- [AutoplayAllowlist](/DeployEdge/microsoft-edge-policies#autoplayallowlist) Allow media autoplay on specific sites
- [CECPQ2Enabled](/DeployEdge/microsoft-edge-policies#cecpq2enabled) CECPQ2 post-quantum key-agreement enabled for TLS
- [ConfigureViewInFileExplorer](/DeployEdge/microsoft-edge-policies#configureviewinfileexplorer) Configure the View in File Explorer feature for SharePoint pages in Microsoft Edge
- [DefaultJavaScriptJitSetting](/DeployEdge/microsoft-edge-policies#defaultjavascriptjitsetting) Control use of JavaScript JIT
- [ShowPDFDefaultRecommendationsEnabled](/DeployEdge/microsoft-edge-policies#showpdfdefaultrecommendationsenabled) Allow notifications to set Microsoft Edge as default PDF reader
- [FeatureFlagOverridesControl](/DeployEdge/microsoft-edge-policies#featureflagoverridescontrol) Configure users ability to override feature flags
- [ImplicitSignInEnabled](/DeployEdge/microsoft-edge-policies#implicitsigninenabled) Enable implicit sign-in
- [InternetExplorerIntegrationCloudSiteList](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist) Configure the Enterprise Mode Cloud Site List
- [InternetExplorerIntegrationSiteListRefreshInterval](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsitelistrefreshinterval) Configure how frequently the Enterprise Mode Site List is refreshed
- [JavaScriptJitAllowedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitallowedforsites) Allow JavaScript to use JIT on these sites
- [JavaScriptJitBlockedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitblockedforsites) Block JavaScript from using JIT on these sites
- [LocalBrowserDataShareEnabled](/DeployEdge/microsoft-edge-policies#localbrowserdatashareenabled) Enable Windows to search local Microsoft Edge browsing data
- [MAUEnabled](/DeployEdge/microsoft-edge-policies#mauenabled) Always use Microsoft AutoUpdate as the updater for Microsoft Edge
- [MSAWebSiteSSOUsingThisProfileAllowed](/DeployEdge/microsoft-edge-policies#msawebsitessousingthisprofileallowed) Allow single sign-on for Microsoft sites using this profile
- [OneAuthAuthenticationEnforced](/DeployEdge/microsoft-edge-policies#oneauthauthenticationenforced) OneAuth Authentication Flow Enforced for sign in
- [PasswordGeneratorEnabled](/DeployEdge/microsoft-edge-policies#passwordgeneratorenabled) Allow users to get a strong password suggestion whenever they're creating an account online
- [PrimaryPasswordSetting](/DeployEdge/microsoft-edge-policies#primarypasswordsetting) Configures a setting that asks users to enter their device password while using password autofill
- [PrintingWebpageLayout](/DeployEdge/microsoft-edge-policies#printingwebpagelayout) Sets layout for printing
- [RemoteDebuggingAllowed](/DeployEdge/microsoft-edge-policies#remotedebuggingallowed) Allow remote debugging
- [RelaunchWindow](/DeployEdge/microsoft-edge-policies#relaunchwindow) Set the time interval for relaunch
- [TravelAssistanceEnabled](/DeployEdge/microsoft-edge-policies#travelassistanceenabled) Enable travel assistance
- [TripleDESEnabled](/DeployEdge/microsoft-edge-policies#tripledesenabled) Enable 3DES cipher suites in TLS
- [WAMAuthBelowWin10RS3Enabled](/DeployEdge/microsoft-edge-policies#wamauthbelowwin10rs3enabled) WAM for authentication below Windows 10 RS3 enabled

***Deprecated Policy***

- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Enable default legacy SameSite cookie behavior setting

***Obsoleted Policy***

- [NewTabPageSetFeedType](/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) Configure the Microsoft Edge new tab page experience

***Additional Change***

- [ConfigureShare](/DeployEdge/microsoft-edge-policies#configureshare) Add mac platform support
- [PasswordMonitorAllowed](/DeployEdge/microsoft-edge-policies#passwordmonitorallowed) Add mac platform support

## Version 92.0.902.84: August 26

Fixed various bugs & performance issues.

## Version 92.0.902.78: August 19

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-19-2021).

## Version 92.0.902.73: August 12

Fixed various bugs & performance issues.

## Version 92.0.902.67: August 5

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-05-2021).

## Version 92.0.902.62: July 29

Fixed various bugs & performance issues.

### Modified Policy

- AutoplayAllowed – Setting to "Disabled" now sets media autoplay to "Limit"

## Version 92.0.902.55: July 22

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#july-22-2021).

### Feature updates

- **Users can easily get to Internet Explorer mode on Microsoft Edge**. Starting with Microsoft Edge version 92, users can reload a site in Internet Explorer mode on Microsoft Edge instead of relying on the standalone IE 11 application while waiting for a site to be configured in the Enterprise Mode Site List. Users are prompted to add the site to their local site list such that navigating to the same page in Microsoft Edge will automatically render in IE mode for the next 30 days. You can use the [InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) policy to configure this experience and allow access to the IE mode entry points and the ability to add sites to the local site list. You can use the [InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) policy to adjust the number of days to keep sites on the local site list. KB5003698 or later is required for Windows 10, version 1909; or KB5003690 or later is required for Windows 10, version 2004, Windows 10, version 20H2, or Windows 10, version 21H1 for the end-to-end experience. For more information, see [Local site list in IE mode](/deployedge/edge-ie-mode-local-site-list).

- **MHTML files will default to opening in Internet Explorer mode**. Starting in Microsoft Edge version 92 Stable, MHTML file types will automatically open in Internet Explorer mode on Microsoft Edge instead of the Internet Explorer (IE11) application. This is most commonly observed while trying to view Outlook emails in a browser. This change occurs only if IE11 is the default handler for this file type. If you'd prefer to change this, you can do so prior to installing the Stable version 92 update using [this guidance](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

- **"Disable developer mode extensions" warning can be dismissed for 2 weeks**. Beginning with Microsoft Edge version 92, you can snooze the warning "Disable developer mode extensions" for two weeks by selecting the option in the warning dialog dropdown.

- **Manage your extensions right from the toolbar**. The all-new extensions menu on the toolbar allows you to hide/pin extensions easily. The quick links to manage extensions and find new extensions make it easy for you to find new extensions and manage your existing ones.

- **Default for autoplay will be set to Limit**.  To help you maintain your focus online, we have changed the default for autoplaying media to Limit from Allow, beginning with Microsoft Edge version 92.

- **Payment instruments are now synced across devices**. Beginning with Microsoft Edge version 92, you have the option to synchronize your payment information across your signed in devices. Note: This is a Controlled Feature Rollout. If you don't see this feature, check back shortly as we continue our rollout.
Currently this feature is available only in the US and only for MSA users (not Microsoft Entra ID)

- **Improvements to font rendering**. Improvements have been made to the rendering of text to improve clarity and reduce blurriness. Note: Tthis is a Controlled Feature Rollout. If you don't see this feature, check back shortly as we continue our rollout.

- **Toolbar button features like Favorites and Collections will remember the user's choice to pin them to the side of the window**. Now enabled by default, if the user chooses to pin a toolbar button, it will always open in the pinned state until they decide to unpin.
a
- **Users can now manage the 'Allow single sign-on for work or school sites using this profile' option via group policy**.  'Allow single sign-on for work or school sites using this profile' allows non-AAD profiles to be able to use single sign-on for work or school sites using work or school credentials present on the machine. This option shows up for end-users as a toggle in Settings -> Profiles -> Profile Preferences for non-AAD profiles only.  You can use the [AADWebSiteSSOUsingThisProfileEnabled](/deployedge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) policy to configure the behavior.  

- **Password health**. It's important to use strong, unique passwords across different accounts to stay safe online. However, that's easier said than done and most users exhibit poor password habits like using weak passwords that are easy to guess, or reuse the same strong passwords across accounts.<br>

   With this latest version of Microsoft Edge, your task of using strong and unique passwords becomes slightly easier! Microsoft Edge will now tell you whether saved passwords are strong enough and also indicate whether they've been used across multiple sites, helping you stay safer online. You can find your password health information in your list of saved passwords in the edge://settings/passwords page.
  
- **Added privacy for your saved passwords**. If you're using a device you share with others or have left your computer unlocked for whatever reason, you can now opt for a second verification using your device password to avoid others getting access to your website passwords. Simple!

- **Outlook extension**.  Stay on top of your Microsoft Outlook inbox, calendar, tasks, and more without having to open a new browser window.  You can get the new Outlook extension here: [Microsoft Outlook - Microsoft Edge Addons](https://microsoftedge.microsoft.com/addons/detail/microsoft-outlook/kkpalkknhlklpbflpcpkepmmbnmfailf?hl=en-US)

- **In alignment with the Chromium open source project, Microsoft Edge is updating the way it renders tables on web pages**. This change fixes known issues and brings Microsoft Edge closer to the specified way tables are meant to render across the web/other browsers. We recommend that you test important workflows in your environment for unexpected issues. A full explainer is available [here](https://docs.google.com/document/d/16PFD1GtMI9Zgwu0jtPaKZJ75Q2wyZ9EZnVbBacOfiNA/edit).

- **Microsoft Editor.**  Microsoft Editor offers enhanced spell checking, grammar checking, and text predictions. [Learn more](https://support.microsoft.com/en-us/office/microsoft-editor-checks-grammar-and-more-in-documents-mail-and-the-web-91ecbe1b-d021-4e9e-a82e-abc4cd7163d7). 

### New Policies

- [AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) Single sign-on for work or school sites using this profile enabled
- [AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault) Configure Automatic HTTPS
- [HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled) Control use of the Headless Mode
- [InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) Specifies whether to allow insecure websites to make requests to more-private network endpoints
- [InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls) Allow the listed sites to make requests to more-private network endpoints from insecure contexts
- [InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) Specify the number of days that a site remains on the local IE mode site list
- [InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) Allow unconfigured sites to be reloaded in Internet Explorer mode
- [SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed) Specifies whether SharedArrayBuffers can be used in a non cross-origin-isolated context

### Deprecated Policy

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) Allow Internet Explorer mode testing

### Obsoleted Policy

- [EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) Allow certificates signed using SHA-1 when issued by local trust anchors

## Version 91.0.864.71: July 19

> [!Important]
>This update contains a fix for [CVE-2021-30563](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30563) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#july-19-2021).

## Version 91.0.864.67: July 8

Fixed various bugs and performance issues.

## Version 91.0.864.64: July 2

Fixed various bugs and performance issues.

## Version 91.0.864.59: June 24

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-24-2021).

## Version 91.0.864.54: June 18

> [!Important]
> This update contains a fix for [CVE-2021-30554](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30554) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-18-2021).

## Version 91.0.864.48: June 11

> [!Important]
>This update contains a fix for [CVE-2021-30551](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30551) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-11-2021).

## Version 91.0.864.41: June 3

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-3-2021).

## Version 91.0.864.37: May 27

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-27-2021).

### Feature updates

- **Identify network traffic originating from Microsoft Defender Application Guard containers at the proxy level**. Starting with Microsoft Edge version 91, there's built in support to tag network traffic originating from Application Guard containers, allowing enterprises to identify them and apply specific policies.

- **Support option to allow synchronizing Favorites from the host to the Edge Application Guard container**. Starting with Microsoft Edge version 91, users have the option to configure Application Guard to synchronize their favorites from the host to the container. This ensures new favorites appear on the container as well.

- **Starting with Microsoft Edge version 91 the browser will automatically interrupt downloads of types which could harm your computer if those downloads are started without a user interaction and are not supported by SmartScreen Application Reputation check**. Users may override and continue to download by right clicking and choosing "Keep" on the download item. Enterprise administrators may opt out of this behavior by configuring the following policy:
  - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings.md) - Disable download file type extension-based warnings for specified file types on domains

    For more information, see [Microsoft Edge Security downloads interruptions](microsoft-edge-security-downloads-interruptions.md).

- **Support for Speech Recognition APIs**. Starting with Microsoft Edge version 91, API support for speech recognition commands on Google.com and similar sites are added. This feature is limited to a randomly selected group of users who enabled experimentation. These users are giving feedback to the feature team.

- **Personalize your browser with new theme colors**. Make Microsoft Edge your own with one of the 14 new theme colors on the Settings -> Appearance page. You can also install custom themes from the Microsoft Edge Add-on site. [Learn more](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

### Policy updates

#### New policies

Six new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added:

- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) - Application Guard Traffic Identification
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) - Explicitly allowed network ports
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) - Allow importing of startup page settings
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) - Let users snip a Math problem and get the solution with a step-by-step explanation in Microsoft Edge
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) - Allow Microsoft News content on the new tab page
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) - Allow quick links on the new tab page

#### Obsoleted Policy

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) - Enable Proactive Authentication

## Version 90.0.818.66: May 20

Fixed various bugs and performance issues.

## Version 90.0.818.62: May 13

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-13-2021).

## Version 90.0.818.56: May 6

Fixed various bugs and performance issues.

## Version 90.0.818.51: April 29

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-29-2021).

## Version 90.0.818.49: April 26

Fixed various bugs and performance issues.

## Version 90.0.818.46: April 22 ##

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-22-2021).

## Version 90.0.818.42: April 19

Fixed various bugs and performance issues.

## Version 90.0.818.41: April 16 ##

> [!Important]
>This update contains a fix for [CVE-2021-21224](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21224) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-16-2021).

## Version 90.0.818.39: April 15 ##

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-15-2021).

## Feature updates ##

- **Single Sign On (SSO) is now available for Microsoft Entra accounts and Microsoft Account (MSA) on macOS.** A user signed in on Microsoft Edge on macOS will now get automatically signed into websites that are configured to allow single sign-on with Work and Microsoft accounts (for example, bing.com, office.com, msn.com, and outlook.com).

- **Kiosk mode.** Starting with Microsoft Edge version 90, we have locked down the UI print settings to only allow the configured printers and "Print to PDF" options. We have also done improvements within the assigned access single app kiosk mode to restrict the launch of other applications from the browser. For more information about the kiosk mode features go [here](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features).

- **Interrupt Downloads** Starting with Microsoft Edge version 91 the browser will automatically interrupt downloads of types that could harm your computer if those downloads are started without a user interaction and aren't supported by SmartScreen Application Reputation check. Users may override and continue to download by right clicking and choosing "Keep" on the download item.
Enterprise administrators may opt out of this behavior one of these two policies:
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains
For more information, see [Microsoft Edge Security downloads interruptions](/deployedge/microsoft-edge-security-downloads-interruptions)

- **Printing**:

  - **New print rasterization mode for non-PostScript printers.** Starting with Microsoft Edge version 90, Admins can use a new policy to define print rasterization mode for their users. This policy controls how Microsoft Edge prints to non-PostScript printers on Windows. Sometimes print jobs on non-PostScript printers need to be rasterized to print correctly. The print options are Full and Fast.
    
  - **Additional page scaling options for printing.** Users are now able to customize scaling while printing webpages and PDF documents using more options. The "Fit to Page" option ensures that the webpage or document is fit into the space available in the selected "Paper size" for printing. The "Actual size" option ensures that there are no changes in the size of the contents being printed regardless of the selected "Paper size".

- **Productivity:**

  - **Autofill suggestions are extended to include address fields content from clipboard.** Clipboard content is parsed when you click on a profile/address field (for example, phone, email, zip code, city, state, etc.) to show as autofill suggestions.

  - **Users can search for autofill suggestions even if a form or field isn't detected.** Today if you have your information saved on Microsoft Edge, autofill suggestions pop up automatically and help you save time while filling out forms. In cases where autofill misses a form, or if you want to fetch data in forms that don't typically have autofill (like temporary forms), you can search for your information use autofill.

-  **Access downloads from a flyout in the menu bar.** Downloads appear in the top-right corner with all the active downloads in one place. This menu is easily dismissible so users can continue browsing uninterrupted, and they can monitor overall download progress right from the toolbar. [Learn more](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).

- **Improvements to font rendering.** Starting with Microsoft Edge version 90, we made improvements to the rendering of text to improve clarity and reduce blurriness. Part of the font rendering improvements land in Beta version 90 but are disabled by default.

- **Kids mode.** We've updated the policy so that when the policy is enabled, it disables the Kid Mode feature in addition to family safety. More about Kids Mode [here](https://go.microsoft.com/fwlink/?linkid=2146910)

## Policy updates

## New policies

Eight new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added:
-    [ApplicationGuardFavoritesSyncEnabled](/DeployEdge/microsoft-edge-policies#applicationguardfavoritessyncenabled) - Application Guard Favorites Sync Enabled
- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) Application Guard Traffic Identification
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) Explicitly allowed network ports
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) Allow importing of startup page settings
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) Let users snip a Math problem and get the solution with a step-by-step explanation in Microsoft Edge
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) Allow Microsoft News content on the new tab page
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) Allow quick links on the new tab page
-    [FetchKeepaliveDurationSecondsOnShutdown](/DeployEdge/microsoft-edge-policies#fetchkeepalivedurationsecondsonshutdown)- Fetch keepalive duration on shutdown
-    [ManagedConfigurationPerOrigin](/DeployEdge/microsoft-edge-policies#managedconfigurationperorigin) - Sets managed configuration values for websites to specific origins
-    [PrintRasterizationMode](/DeployEdge/microsoft-edge-policies#printrasterizationmode) - Print Rasterization Mode
-    [QuickViewOfficeFilesEnabled](/DeployEdge/microsoft-edge-policies#quickviewofficefilesenabled) - Manage QuickView Office files capability in Microsoft Edge
-    [SSLErrorOverrideAllowedForOrigins](/DeployEdge/microsoft-edge-policies#sslerroroverrideallowedfororigins) - Allow users to proceed from the HTTPS warning page for specific origins
-    [WindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#windowocclusionenabled) - Enable Window Occlusion
-    [WindowsHelloForHTTPAuthEnabled](/DeployEdge/microsoft-edge-policies#windowshelloforhttpauthenabled) - Windows Hello For HTTP Auth Enabled

## Deprecated policies

- [ProactiveAuthEnabled](/DeployEdge/microsoft-edge-policies#proactiveauthenabled) Enable Proactive Authentication
-    [NativeWindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - Enable Native Window Occlusion
-    [SSLVersionMin](/DeployEdge/microsoft-edge-policies#sslversionmin)- Minimum TLS version enabled

## Version 89.0.774.77: April 14

> [!Important]
>This update contains a fix for  [CVE-2021-21206](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21206) and [CVE-2021-21220](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21220) which has been reported by the Chromium team as having an exploit in the wild.  For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-14-2021).

## Version 89.0.774.76: April 12

Fixed various bugs and performance issues.

## Version 89.0.774.75: April 8

Fixed various bugs and performance issues.

## Version 89.0.774.68: April 1

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#april-1-2021).

## Version 89.0.774.63: March 25

Fixed various bugs and performance issues.

## Version 89.0.774.57: March 18

Fixed various bugs and performance issues.

## Version 89.0.774.54: March 13

> [!IMPORTANT]
> This update contains [CVE-2021-21193](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21193) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#march-13-2021).

## Version 89.0.774.50: March 10

Fixed various bugs and performance issues.

## Version 89.0.774.48: March 8

Fixed various bugs and performance issues.

<!-- begin major 89 -->

## Version

> [!IMPORTANT]
> This update contains [CVE-2021-21166](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21166) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#march-4-2021).

### Resolved issues

- **Taskbar and Start menu shortcut updates and fixes:**
  - Right-clicking the Microsoft Edge shortcut in the Start menu now properly shows the option to unpin Microsoft Edge from the taskbar when it's pinned.
  - Start layouts that include a [taskbar configuration](/windows/configuration/configure-windows-10-taskbar) to pin Microsoft Edge to the taskbar will no longer result in a second Microsoft Edge shortcut getting pinned to the taskbar.
  - Organizations using Windows Roaming Profiles will no longer see a blank white icon in place of the Microsoft Edge icon on the taskbar when their users sign in Windows.

### Feature updates

- **Kiosk mode enables additional lockdown capabilities**. Starting with Microsoft Edge version 89, we have added more lockdown capabilities within kiosk mode to enable customers to get the job done in a productive and more secure experience. [Learn more](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **The Enterprise Mode Site List Manager tool will be available in the browser through the *edge://compat* page**. You can use this tool to create, edit, and export your site list XML for Internet Explorer mode on Microsoft Edge. You can enable access to this tool as needed through group policy. [Learn More](./edge-ie-mode-site-list-manager.md).

- **Improve browser performance with sleeping tabs**. Sleeping tabs improves browser performance by putting inactive tabs to sleep to free up system resources like memory and CPU so active tabs or other applications can use them. Users can prevent sites from going to sleep and configure the length of time before an inactive tab goes to sleep. To keep users in their flow, there are also [heuristics](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) to prevent certain sites from going to sleep, such as intranet sites. This feature can be managed with group policies.

- **Reset your Microsoft Edge sync data in the cloud manually**. We're introducing a way to reset your Microsoft Edge sync data from within the product. This ensures that your data is cleared from Microsoft services, and resolving certain product issues that previously required a support ticket.

- **Intelligent enablement of Single sign-on (SSO) for all Windows Microsoft Entra accounts for users with a single non-Azure AD Microsoft Edge profile**.  Automatically turn on this setting for users that might benefit the most from this feature. If a user has only one Microsoft Edge profile (and it's not Microsoft Entra ID or Kids Mode), the setting is automatically turned on when Microsoft Edge launches. This autotoggle will also automatically turn off if a user later chooses to sign into a different Microsoft Edge profile with a Microsoft Entra account. Users can manually update their preferences for this feature in **Settings > Profiles >Profile Preferences > Allow single sign-on for work or school sites using this profile**.

- **Improvements to text selection experience within PDF documents**. Users begin to get a smoother and more consistent text selection experience across PDF documents opened in Microsoft Edge starting with version 89.

- **Date of birth field now supported in autofill**. Today Microsoft Edge helps you save time and effort while filling out forms and creating accounts online by auto filling your data like addresses, names, phone numbers, etc. Starting with Microsoft Edge version 89, we're adding support for another field that you can have saved and autofilled - date of birth. You can view, edit, and delete this information anytime in your profile settings.

### Policy updates

#### New policies

Seven new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added.

- [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime) - Browsing Data Lifetime Settings
- [MAMEnabled](./microsoft-edge-policies.md#mamenabled) - Mobile App Management Enabled
- [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages) - Define an ordered list of preferred languages that websites should display in if the site supports the language
- [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled) - Allow recommendations and promotional notifications from Edge
- [PrintingAllowedBackgroundGraphicsModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes) - Restrict background graphics printing mode
- [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault) - Default background graphics printing mode
- [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist) - Block smart actions  for a list of services

#### Obsoleted policies

The following policies are obsoleted.

- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) - Use a default referrer policy of no-referrer-when-downgrade
- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - Enable usage and crash-related data reporting
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - Send site information to improve Microsoft services

<!-- end major 89 -->

## Version 88.0.705.81: February 25

Fixed various bugs and performance issues.

## Version 88.0.705.74: February 17

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#february-17-2021).

## Version 88.0.705.68: February 11

Fixed various bugs and performance issues.

## Version 88.0.705.63: February 5

> [!IMPORTANT]
> This update contains [CVE-2021-21148](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21148) which has been reported by the Chromium team as having an exploit in the wild.

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#february-5-2021).

## Version 88.0.705.62: February 4

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#february-4-2021).

Fixed various bugs and performance issues.

## Version 88.0.705.56: January 28

Fixed various bugs and performance issues.

## Version 88.0.705.53: January 26

Fixed various bugs and performance issues.

## Version 88.0.705.50: January 21

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#january-21-2021).

<!--- begin major 88  --->
### Feature updates

- **Deprecations:**

  - Deprecate support for FTP protocol. Support for the legacy FTP protocol has been removed from Microsoft Edge. Attempting to navigate to an FTP link results in the browser directing the Operating System to open an external application to handle the FTP link. Alternatively, IT administrators can configure Microsoft Edge to use IE Mode for sites that rely on the FTP protocol.
  - Adobe Flash support is removed. Starting with Microsoft Edge Beta version 88, Adobe Flash capability and support will be removed. Learn more: [Update on Adobe Flash Player End of Support - Microsoft Edge Blog (windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Authentication:**

  - Single Sign On (SSO) now available for Microsoft Entra accounts and Microsoft Account (MSA) on down-level Windows. A user signed in on Microsoft Edge on down-level Microsoft Windows (7, 8.1) will now get automatically signed into websites that are configured to allow single sign-on with Work and Microsoft accounts (for example, bing.com, office.com, msn.com, outlook.com).<br>Note: A user may have to sign out and then sign back in if they'd signed into Microsoft Edge in a version prior to Microsoft Edge 88 to leverage this feature.
  
  - Single sign-on (SSO) to work sites using any Windows Microsoft Entra accounts on system in non-Azure AD Microsoft Edge profiles. This feature can be enabled for any profile that isn't signed-in with a work/school account and isn't guest or in-private and allows the use of any signed-in work/school account on operating system with that profile. This feature can be configured in **Settings** > **Profiles** > **Profile Preferences** > **Allow single sign-on for work or school sites using this profile**.
  
    > [!NOTE]
    > "Single sign-on (SSO) for all Windows accounts using the Microsoft Edge profile" is an update to the January 21 release notes.

- **Kiosk mode option to end session**. The "End session" button is now available in a kiosk mode public browsing experience. This feature ensures that browser data and settings are deleted when Microsoft Edge is closed. Learn more about kiosk mode features and roadmap, [Configure Microsoft Edge kiosk mode](./microsoft-edge-configure-kiosk-mode.md).

- **Security and Privacy:**

  - Alerts are generated if a user's password is found in an online leak. User passwords are checked against a repository of known-breached credentials and send the user an alert if a match is found. To ensure security and privacy, user passwords are hashed and encrypted when they're checked against the database of leaked credentials.
  - Automatically upgrade mixed content. Secure pages delivered over HTTPS may contain references images that are served over non-secure HTTP. To improve privacy and security in Microsoft Edge 88, those images will be retrieved over HTTPS instead. If the image is not available over HTTPS, it will not be loaded.
  - View site permissions by site and by recent activity. Starting with Microsoft Edge 88, users are able to manage site permissions more easily. They'll be able to view permissions by web site rather than just permission type. Additionally, we've added a recent activity section that shows a user all the recent changes to their site permissions.
  - Increased controls for browser cookies. Starting with Microsoft Edge 88, users can delete third party cookies without affecting first party cookies. Users will also be able to filter their cookies by first or third party and sort by name, number of cookies, and the amount of data stored and last modified.

- **Passwords:**

  - Password Generator. Microsoft Edge offers a built-in strong password generator that you can use when signing up for a new account or when changing an existing password. Just look for the browser-suggested password drop-down in the password field and when selected, it will automatically save to the browser and sync across devices for easy future use.
  - Password Monitor. When any of your passwords saved to the browser match with those seen in the list of leaked credentials, Microsoft Edge notifies you and prompt you to update your password. Password Monitor scans for matches on your behalf and is on by default.
  - Edit Password. You can now edit your saved passwords directly in Microsoft Edge Settings. Any time a password has been updated outside of Microsoft Edge, it's easy to replace the saved older password with the new one by editing the saved entry in Settings. 

- **Improve Microsoft Edge startup speed with startup boost**. To improve Microsoft Edge startup speed, we've developed a feature named startup boost. Startup boost makes Microsoft Edge launch faster by enabling Microsoft Edge to run in the background. Note: This feature is limited to a randomly selected group of users who have enabled experimentation. These users are giving feedback to the feature team.

- **Productivity:**

  - Improve productivity and multi-tasking with vertical tabs. As the number of horizontal tabs grows, site titles start to get cut off and tab controls are lost as each tab shrinks. This interrupts user workflow as they spend more time finding, switching, and managing their tabs and less time on the task at hand. Vertical tabs let users move their tabs to the side, where vertically aligned icons and longer site titles make it easier to quickly scan, identify and switch to the tab they want to open.
  - Auto filling the date of birth field. Microsoft Edge already helps save time and effort while filling out forms and creating accounts online by auto filling user data such as addresses, names, phone numbers, etc. Microsoft Edge now supports the date of birth field which users can save and auto fill. A user can view, edit, and delete this information anytime in their profile settings.
  - Improvements to Recently closed in History. Recently closed now keeps the last 25 tabs and windows from any past browsing session rather than just the previous session. Users can select Recently closed in the new History experience to see all the tabs that were open.
  - "Your day at a glance" feature enabled by default. Starting with Microsoft Edge version 88, information workers can benefit from intelligent productivity features on their New tab page (NTP). Microsoft Edge 87 users will also experience these features within two weeks after Microsoft Edge 88 release. We offer users signed in with their work or school account personalized and relevant content powered by their M365 Graph. Users can quickly scan their "Your day at a glance" modules to easily track their meetings and recent work and quickly launch the applications they want to use.

- **History and open tabs sync**. History and open tabs sync is now available for users to enjoy. Enabling these features help users pick up where they left off by making their browsing history and open tabs available on all their syncing devices. We've updated sync and browser history policies, so now users are connected and productive across any devices by using Microsoft Edge. [Learn more](https://blogs.windows.com/windowsexperience/2021/01/21/this-year-lets-resolve-to-make-the-most-of-our-time-online-and-better-protect-ourselves-from-online-threats/).

- **PDF:**

  - PDF document display in book view (two pages). Starting with Microsoft Edge version 88, users can view PDF documents in a single page or in the two page book view. To change the view, click the **Page View** button in the toolbar.
  - Anchored text notes support for PDF files. Starting with Microsoft Edge version 87, users can add typed text notes on any piece of text in PDF files.

- **Fonts:**

  - Browser icons are updated to the Fluent design system. As part of our continued work around Fluent Design in the browser, we've made changes to closer align icons to the new Microsoft icon system. These changes impact many of our high-touch user interfaces, including tabs, address bar, and navigational and wayfinding icons found in our various menus.
  - Improved font rendering. Text rendering is improved for better clarity and to reduce blurriness.

### Policy updates

#### New policies

Eighteen new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added.

- [BasicAuthOverHttpEnabled](./microsoft-edge-policies.md#basicauthoverhttpenabled) - Allow Basic authentication for HTTP.
- [BlockExternalExtensions](./microsoft-edge-policies.md#blockexternalextensions) - Blocks external extensions from being installed.
- [InternetExplorerIntegrationLocalFileAllowed](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileallowed) - Allow launching of local files in Internet Explorer mode.
- [InternetExplorerIntegrationLocalFileExtensionAllowList](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist) - Open local files in Internet Explorer mode file extension allowlist.
- [InternetExplorerIntegrationLocalFileShowContextMenu](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileshowcontextmenu) - Show context menu to open a link in Internet Explorer mode.
- [IntranetRedirectBehavior](./microsoft-edge-policies.md#intranetredirectbehavior) - Intranet Redirection Behavior.
- [PrinterTypeDenyList](./microsoft-edge-policies.md#printertypedenylist) - Disable printer types on the blocklist.
- [ShowMicrosoftRewards](./microsoft-edge-policies.md#showmicrosoftrewards) - Show Microsoft Rewards experiences.
- [SleepingTabsEnabled](./microsoft-edge-policies.md#sleepingtabsenabled) - Configure Sleeping Tabs.
- [SleepingTabsTimeout](./microsoft-edge-policies.md#sleepingtabstimeout) - Set the background tab inactivity timeout for Sleeping Tabs.
- [SleepingTabsBlockedForUrls](./microsoft-edge-policies.md#sleepingtabsblockedforurls) - Block Sleeping Tabs on specific sites.
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled) - Enable startup boost.
- [TargetBlankImpliesNoOpener](./microsoft-edge-policies.md#targetblankimpliesnoopener) - Don't set window.opener for links targeting _blank.
- [UpdatePolicyOverride](./microsoft-edge-policies.md#updatepolicyoverride) - Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.
- [VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) - Configures availability of a vertical layout for tabs on the side of the browser.
- [WebRtcAllowLegacyTLSProtocols](./microsoft-edge-policies.md#webrtcallowlegacytlsprotocols) - Allow legacy TLS/DTLS downgrade in WebRTC.
- [WebWidgetAllowed](./microsoft-edge-policies.md#webwidgetallowed) - Enable the Web widget.
- [WebWidgetIsEnabledOnStartup](./microsoft-edge-policies.md#webwidgetisenabledonstartup) - Allow the Web widget at Windows startup.

#### Deprecated Policies

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) - Enable Proactive Authentication.
- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist) - Configure proxy bypass rules.
- [ProxyMode](./microsoft-edge-policies.md#proxymode) - Configure proxy server settings.
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl) - Set the proxy .pac file URL.
- [ProxyServer](./microsoft-edge-policies.md#proxyserver) - Configure address or URL of proxy server.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) - Allow WebDriver to Override Incompatible Policies.

### Obsoleted Policies

- [AllowPopupsDuringPageUnload](./microsoft-edge-policies.md#allowpopupsduringpageunload) - Allows a page to show popups during its unloading.
- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting) - Default Adobe Flash setting.
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls) - Allow the Adobe Flash plug-in on specific sites.
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls) - Block the Adobe Flash plug-in on specific sites.
- [RunAllFlashInAllowMode](./microsoft-edge-policies.md#runallflashinallowmode) - Extend Adobe Flash content setting to all content.
<!--- end major 88  --->
## Version 87.0.664.75: January 7

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#january-7-2021).

## Version 87.0.664.66: December 17

Fixed various bugs and performance issues.

## Version 87.0.664.60: December 10

Fixed various bugs and performance issues.

## Version 87.0.664.57: December 7

Fixed various bugs and performance issues. Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#december-7-2020).

## Version 87.0.664.55: December 3

Fixed various bugs and performance issues. The following feature was updated for this release.

- **Shopping is enabled by default**. Starting with Microsoft Edge version 87, enterprise users can benefit from shopping in Microsoft Edge. With Shopping features, Microsoft Edge helps users find coupons and better prices while shopping online. (The coupon experience was released with Stable version 87.0.664.41). The price comparison experience is now available with this update. This feature can be configured using the [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) policy. See our [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) and [Learn More](/microsoft-edge/privacy-whitepaper#shopping) about Microsoft Shopping.

## Version 87.0.664.52: November 30

Fixed various bugs and performance issues.

## Version 87.0.664.47: November 23

Fixed various bugs and performance issues.

<!-- begin major 87 --->
## Version 87.0.664.41: November 19

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#november-19-2020).

### Feature updates

- **Automatic redirection for incompatible sites from Internet Explorer to Microsoft Edge**. Starting with the Microsoft Edge 87 Stable update, public websites that show an incompatibility message on Internet Explorer will be automatically redirected to Microsoft Edge. To learn more and to configure this experience, see [Redirecting incompatible sites](./edge-learnmore-neededge.md).

- **Kiosk mode privacy features enabled**. Starting with Microsoft Edge version 87, kiosk mode features that help enterprises around the privacy of user data are enabled. These features enable experiences such as clear the user data on exit, delete downloaded files and to reset the configured start experience after a specified amount of idle time. Learn more about how to [Configure Microsoft Edge kiosk mode](./microsoft-edge-configure-kiosk-mode.md)

- **Shopping features enabled by default**. Starting with Microsoft Edge version 87 enterprise users can also benefit from shopping in Edge. With Shopping features, Microsoft Edge helps users to find coupons and better prices while shopping online. Coupon experience is available with this update and price comparison will be released in upcoming updates for Microsoft Edge 87. This feature can be configured through [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) policy. See our [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) and [Learn More](/microsoft-edge/privacy-whitepaper#shopping) about Microsoft Shopping.

- **ClickOnce deployment enabled by default**. ClickOnce is enabled by default in Microsoft Edge 87, which reduces the barriers for enterprises to deploy software and better align with Microsoft Edge Legacy browser behavior. Starting in Microsoft Edge 87, the ClickOnceEnabled policy's "Not configured" state reflects the new default ClickOnce state of Enabled (as compared to the previous default state of Disabled).

- **The enterprise new tab page (NTP) integrates productivity with customizable, work-relevant feed content**. The enterprise NTP blends the Office 365 productivity page we offer to users signed in with their work or school account with personalized, work-relevant company and industry feeds that are organized in a single page. Users are able to recognize the familiar Office 365 content and Microsoft Search for Business powered by Bing. In addition, they can easily customize "My Feed" by choosing the most relevant content to them from the available content and modules for their organization. IT Administrators can control the News feed settings for their  organization, including the selected industry for the Microsoft Edge new tab page by going to Microsoft 365 admin center. [Learn more](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/)

- **Privacy and Security:**

  - Support TLS Token Binding for policy-configured sites. TLS Token binding helps prevent token theft attacks to ensure that cookies can't be reused from a device other than the device upon which they were initially set. The use of TLS token binding requires setting the [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) policy and requires that the sites listed support this feature.

- **Keyboard support for highlighter on PDF files**. Users can use their keyboard keys to highlight any text on a PDF.

- **Printing:**

  - Choose which side to flip on when printing on both sides. Users can choose to flip on the long side or the short side of a sheet when printing on both sides.
  - Choose print rasterization mode for the enterprise. Control how Microsoft Edge prints to a non-PostScript printer on Windows. Sometimes print jobs on non-PostScript printers need to be rasterized to print correctly. The print options are "Full" and "Fast".

### Policy updates

#### New policies

Ten new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added.

- [ConfigureFriendlyURLFormat](./microsoft-edge-policies.md#configurefriendlyurlformat) - Configure the default paste format of URLs copied from Microsoft Edge, and determine if more formats are available to users.
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) - Shopping in Microsoft Edge enabled.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](./microsoft-edge-policies.md#hideinternetexplorerredirectuxforincompatiblesitesenabled) - Hide the one-time redirection dialog and the banner on Microsoft Edge.
- [KioskAddressBarEditingEnabled](./microsoft-edge-policies.md#kioskaddressbareditingenabled) - Configure address bar editing for kiosk mode public browsing experience.
- [KioskDeleteDownloadsOnExit](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) - Delete files downloaded as part of kiosk session when Microsoft Edge closes.
- [PasswordRevealEnabled](./microsoft-edge-policies.md#passwordrevealenabled) - Enable Password reveal button.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerpreventbhoinstall) - Prevent install of the browser helper object (BHO) to redirect incompatible sites from Internet Explorer to Microsoft Edge.
- [RedirectSitesFromInternetExplorerRedirectMode](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerredirectmode) - Redirect incompatible sites from Internet Explorer to Microsoft Edge.
- [SpeechRecognitionEnabled](./microsoft-edge-policies.md#speechrecognitionenabled) - Configure Speech Recognition.
- [WebCaptureEnabled](./microsoft-edge-policies.md#webcaptureenabled) - Enable web capture feature in Microsoft Edge.

#### Deprecated Policy

[NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype) - Configure the Microsoft Edge new tab page experience.

#### Obsoleted Policy

[EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures) - Re-enable deprecated web platform features for a limited time.

<!-- end major 87 -->

## Version 86.0.622.69: November 13

> [!IMPORTANT]
> This update contains [CVE-2020-16013](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16013) and [CVE-2020-16017](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16017), that have been reported by the Chromium team as having an exploit in the wild.

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#november-13-2020).

## Version 86.0.622.68: November 11

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#november-11-2020)

## Version 86.0.622.63: November 4

> [!IMPORTANT]
> This update contains [CVE-2020-16009](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16009), that has been reported by the Chromium team as having an exploit in the wild.

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#november-4-2020).

## Version 86.0.622.61: November 2

Fixed various bugs and performance issues.

## Version 86.0.622.58: October 29

Fixed various bugs and performance issues.

## Version 86.0.622.56: October 27

Fixed various bugs and performance issues.

## Version 86.0.622.51: October 22

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#october-22-2020)

## Version 86.0.622.48: October 20

Fixed various bugs and performance issues.

## Version 86.0.622.43: October 15

Fixed various bugs and performance issues.

## Version 86.0.622.38: October 9

Security updates are listed [here](./microsoft-edge-relnotes-security.md#october-9-2020)

### Feature updates

* **Roll back to previous Microsoft Edge version.** The rollback feature lets administrators revert to a known good version of Microsoft Edge if there's an issue in the latest version of Microsoft Edge. **Note:** Stable version 86.0.622.38 is the first version you can roll back to, which means that Stable version 87 is the first version ready to roll back from. [Learn more](edge-learnmore-rollback.md).

* **Enforce enabling Sync by default across the enterprise.**  Administrators can enable synchronization for Microsoft Entra accounts by default with the [ForceSync](./microsoft-edge-policies.md#forcesync) policy.

* **Automatic profile switching on Windows 7 and 8.1.** The automatic profile switching currently available in Microsoft Edge on Windows 10 is extended to downlevel Windows (Windows 7 and 8.1). For more information, see the [automatic profile switching](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) blog post.

* **SameSite=Lax Cookies By Default**. To improve web security and privacy, cookies will now default to [SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite) handling by default. This means that cookies will only be sent in a first-party context and will be omitted for requests sent to third-parties. This change can cause compatibility impact on websites that require cookies for third-party resources to function correctly. To permit such cookies, web developers can mark cookies, which should be set from and sent to third-party contexts by adding explicit `SameSite=none` and `Secure` attributes when the cookie is set. Enterprises that wish to exempt certain sites from this change can do so using the [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) policy, or can opt out of the change across all sites using the [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled) policy.

* **Remove the HTML5 Application Cache API.**  Beginning with Microsoft Edge version 86, the legacy Application Cache API that enables offline use of web pages is being removed from Microsoft Edge. Web Developers should review the [WebDev documentation](https://web.dev/appcache-removal/) for information on replacing  the Application Cache API with Service Workers.  Important: You can request an [AppCache OriginTrial Token](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) that allows sites to continue to use the deprecated Application Cache API until Microsoft Edge version 90.

* **Privacy and Security:**

  * Replace [MetricsReportingEnabled](/DeployEdge/microsoft-edge-policies#metricsreportingenabled) and [SendSiteInformationToImproveServices](/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) policies for downlevel Windows and macOS. These policies are deprecated in Microsoft Edge version 86 and will become obsolete in Microsoft Edge version 89.<br>
These policies are replaced by [Allow Telemetry](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) on Windows 10, and the new [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) policy for all other platforms. This lets users manage the diagnostic data that gets sent to Microsoft for Windows 7, 8, 8.1 and macOS.
  * Secure DNS (DNS-over-HTTPS) support.  Beginning with Microsoft Edge version 86, settings to control Secure DNS on unmanaged devices is available. These settings aren't accessible to users on managed devices, but IT admins can enable or disable Secure DNS using the [dnsoverhttpsmode](./microsoft-edge-policies.md#dnsoverhttpsmode) group policy.

* **Internet Explorer mode:** Let users use the Microsoft Edge User Interface (UI) to test sites in Internet Explorer mode. Beginning with Microsoft Edge version 86, administrators can enable a UI option for their users to load a tab in Internet Explorer mode for testing purposes or as a stopgap until sites are added to the site list XML.

* **PDF updates:**

  * Table of contents for PDF Documents. Beginning with version 86, Microsoft Edge has added support for table of contents that lets users easily navigate through PDF documents.
  * Access all PDF functionalities on small form factor screens. Access all the capabilities of the Microsoft Edge PDF reader on devices with small screen sizes.
  * Pen support for highlighter on PDF files. With this update, users can use their digital pen to directly highlight text on PDF files, in the same way they would with a physical highlighter and paper.
  * Improved PDF scrolling. You'll now be able to experience stutter free scrolling while navigating through long PDF documents.

* **Users will see auto complete suggestions when they start typing a search query on the Microsoft Edge Add-ons website.** Auto complete will help users quickly complete their search query without having to type the entire string. This is helpful because users won't have to remember correct spellings and they can choose from the available options that are displayed.

* **Add a custom image to the New Tab Page (NTP) using a group policy.** Beginning with Microsoft Edge version 86 the NTP has an option to replace the default image with a custom user-supplied image. The ability to manage the properties of this image is also supported by the group policy.

* **Match customized keyboard shortcuts to VS Code.** Microsoft Edge DevTools now supports customizing keyboard shortcuts in the DevTools to match with your editor/IDE. (In Microsoft Edge 84, we added the ability to match DevTools keyboard shortcuts to VS Code).

* **Delete downloads from disk using download manager.** Users are now able to delete their downloaded files from their disk without leaving the browser. The new Delete downloads functionality exists within the context menu of downloads shelf or the downloads page.

### Policy updates

#### New policies

Twenty-three new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [CollectionsServicesAndExportsBlockList](./microsoft-edge-policies.md#collectionsservicesandexportsblocklist) - Block access to a specified list of services and export targets in Collections.
- [DefaultFileSystemReadGuardSetting](./microsoft-edge-policies.md#defaultfilesystemreadguardsetting) - Control use of the File System API for reading.
- [DefaultFileSystemWriteGuardSetting](./microsoft-edge-policies.md#defaultfilesystemwriteguardsetting) - Control use of the File System API for writing.
- [DefaultSensorsSetting](./microsoft-edge-policies.md#defaultsensorssetting) - Default sensors setting.
- [DefaultSerialGuardSetting](./microsoft-edge-policies.md#defaultserialguardsetting) - Control use of the Serial API.
- [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) - Send required and optional diagnostic data about browser usage.
- [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed) - Allow access to the Enterprise Mode Site List Manager tool.
- [FileSystemReadAskForUrls](./microsoft-edge-policies.md#filesystemreadaskforurls) - Allow read access via the File System API on these sites.
- [FileSystemReadBlockedForUrls](./microsoft-edge-policies.md#filesystemreadblockedforurls) - Block read access via the File System API on these sites.
- [FileSystemWriteAskForUrls](./microsoft-edge-policies.md#filesystemwriteaskforurls) - Allow write access to files and directories on these sites.
- [FileSystemWriteBlockedForUrls](./microsoft-edge-policies.md#filesystemwriteblockedforurls) - Block write access to files and directories on these sites.
- [ForceSync](./microsoft-edge-policies.md#forcesync) - Force synchronization of browser data and don't show the sync consent prompt.
- [InsecureFormsWarningsEnabled](./microsoft-edge-policies.md#insecureformswarningsenabled) - Enable warnings for insecure forms.
- [InternetExplorerIntegrationTestingAllowed](./microsoft-edge-policies.md#internetexplorerintegrationtestingallowed) - Allow Internet Explorer mode testing.
- [SpotlightExperiencesAndRecommendationsEnabled](./microsoft-edge-policies.md#spotlightexperiencesandrecommendationsenabled) - Choose whether users can receive customized background images and text, suggestions, notifications, and tips for Microsoft services.
- [NewTabPageAllowedBackgroundTypes](./microsoft-edge-policies.md#newtabpageallowedbackgroundtypes) - Configure the background types allowed for the new tab page layout.
- [SaveCookiesOnExit](./microsoft-edge-policies.md#savecookiesonexit) - Save cookies when Microsoft Edge closes.
- [SensorsAllowedForUrls](./microsoft-edge-policies.md#sensorsallowedforurls) - Allow access to sensors on specific sites.
- [SensorsBlockedForUrls](./microsoft-edge-policies.md#sensorsblockedforurls) - Block access to sensors on specific sites.
- [SerialAskForUrls](./microsoft-edge-policies.md#serialaskforurls) - Allow the Serial API on specific sites.
- [SerialBlockedForUrls](./microsoft-edge-policies.md#serialblockedforurls) - Block the Serial API on specific sites.
- [UserAgentClientHintsEnabled](./microsoft-edge-policies.md#useragentclienthintsenabled) - Enable the User-Agent Client Hints feature.
- [UserDataSnapshotRetentionLimit](./microsoft-edge-policies.md#userdatasnapshotretentionlimit) - Limits the number of user data snapshots retained for use in case of emergency rollback.

#### Deprecated Policies

- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - Enable usage and crash-related data reporting.
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - Send site information to improve Microsoft services.

#### Obsoleted Policy

[TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled) - Enable a TLS 1.3 security feature for local trust anchors.

## Version 85.0.564.70: October 6

Fixed various bugs and performance issues.

## Version 85.0.564.68: October 1

Fixed various bugs and performance issues.

## Version 85.0.564.63: September 23

Security updates are listed [here](./microsoft-edge-relnotes-security.md#september-23-2020)

## Version 85.0.564.51: September 9

Security updates are listed [here](./microsoft-edge-relnotes-security.md#september-9-2020)

## Version 85.0.564.44: August 31

Fixed various bugs and performance issues.

<!-- 85.0.564.41: August 27 -->

## Version 85.0.564.41: August 27

Security updates are listed [here](./microsoft-edge-relnotes-security.md#august-27-2020)

### Feature updates

- **On-premises synchronization of Favorites and Settings**. Now you can synchronize browser favorites and settings between Active Directory profiles within your own environment without the need for cloud sync.

- **Microsoft Edge group policy support for trusting site + app combos to launch without a confirmation prompt.**. Group policy support added that lets administrators add site + app combos that are trusted to launch without the confirmation prompt. This adds the ability for administrators to configure trusted protocol/origin combinations (such as Microsoft 365 apps) for their end-users to suppress the confirmation prompt when navigating to a URL that contains an app protocol.

- **PDF Highlighter tool**. This tool can be added to the toolbar for PDFs to easily highlight important text.

- **The Storage Access API is available**. The Storage Access API allows access to first-party storage in a third-party context when a user has provided a direct intent to allow storage that would otherwise be blocked by the browser's current configuration. For more information, see [Storage Access API](https://www.chromestatus.com/feature/5612590694662144).

- **Send to OneNote is available for Microsoft Edge Collections**. Everyone's excited to be able to send the information they've gathered in Collections to OneNote, where they can append it to a larger project and collaborate with others! And even more importantly, in Microsoft Edge 85, you are able send content to *Office for Mac* products (Word, Excel, and OneNote) for both Microsoft account and Microsoft Entra ID.

- **DevTools updates**. For details about the following updates, see [What's New In DevTools (Microsoft Edge 85)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools).

   - Microsoft Edge DevTools supports Surface Duo emulation. The Microsoft Edge DevTools can emulate the Surface Duo so you can test how your web content looks on dual-screen devices. To turn on this experiment in DevTools, enter Device Mode by pressing Ctrl+Shift+M on Windows or Command+Shift+M on macOS, and then select Surface Duo from the device drop-down list.
   - Microsoft Edge DevTools lets you match keyboard shortcuts to VS Code. The Microsoft Edge DevTools supports customizing keyboard shortcuts in the DevTools to match your editor/IDE. In Microsoft Edge 85, we're adding the ability to match DevTools keyboard shortcuts to VS Code. This change helps increase productively across VS Code and DevTools.

### Policy updates

#### New policies

Thirteen new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [AutoLaunchProtocolsFromOrigins](./microsoft-edge-policies.md#autolaunchprotocolsfromorigins) - Define a list of protocols that can launch an external application from listed origins without prompting the user.
- [AutoOpenAllowedForURLs](./microsoft-edge-policies.md#autoopenallowedforurls) - URLs where AutoOpenFileTypes can apply.
- [AutoOpenFileTypes](./microsoft-edge-policies.md#autoopenfiletypes) - List of file types that should be automatically opened on download.
- [DefaultSearchProviderContextMenuAccessAllowed](./microsoft-edge-policies.md#defaultsearchprovidercontextmenuaccessallowed) - Allow default search provider context menu search access.
- [EnableSha1ForLocalAnchors](./microsoft-edge-policies.md#enablesha1forlocalanchors) - Allow certificates signed using SHA-1 when issued by local trust anchors. <!--- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](./microsoft-edge-policies.md#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains. -->
- [IntensiveWakeUpThrottlingEnabled](./microsoft-edge-policies.md#intensivewakeupthrottlingenabled) - Control the IntensiveWakeUpThrottling feature.
- [NewTabPagePrerenderEnabled](./microsoft-edge-policies.md#newtabpageprerenderenabled) - Enable preload of the new tab page for faster rendering.
- [NewTabPageSearchBox](./microsoft-edge-policies.md#newtabpagesearchbox) - Configure the new tab page search box experience.
- [PasswordMonitorAllowed](./microsoft-edge-policies.md#passwordmonitorallowed) - Allow users to be alerted if their passwords are found to be unsafe.
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled) - Enable using roaming copies for Microsoft Edge profile data.
- [RoamingProfileLocation](./microsoft-edge-policies.md#roamingprofilelocation) - Set the roaming profile directory.
- [TLSCsipherSuiteDenyList](./microsoft-edge-policies.md#tlsciphersuitedenylist) - Specify the TLS cipher suites to disable.

#### Obsoleted policies

- [EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) - Enable Domain Actions Download from Microsoft.
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) - Re-enable Web Components v0 API until M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies)- Allow WebDriver to Override Incompatible Policies.

## Version 84.0.522.63: August 20

Security updates are listed [here](./microsoft-edge-relnotes-security.md#august-20-2020).

## Version 84.0.522.61: August 17

Fixed various bugs and performance issues.

## Version 84.0.522.59: August 11

Security updates are listed [here](./microsoft-edge-relnotes-security.md#august-11-2020)

## Version 84.0.522.58: August 10

Fixed various bugs and performance issues.

## Version 84.0.522.52: August 1

Fixed various bugs and performance issues.

## Version 84.0.522.50: July 31

Fixed various bugs and performance issues.

## Version 84.0.522.49: July 29

Security updates are listed [here](./microsoft-edge-relnotes-security.md#july-29-2020)

## Version 84.0.522.48: July 28

Fixed various bugs and performance issues.

## Version 84.0.522.44: July 23

Fixed various bugs and performance issues.

## Version 84.0.522.40: July 16

Security updates are listed [here](./microsoft-edge-relnotes-security.md#july-16-2020)

### Feature updates

- This version of Microsoft Edge provides improved site list download times for Internet Explorer mode. We've reduced download delay for the Internet Explorer mode site list to 0 seconds (down from a 60-second wait) in the absence of a cached site list. We've also added group policy support for cases when Internet Explorer mode home page navigation need to be delayed until the site list is downloaded. For more information, see the [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload) policy.

- Microsoft Edge now allows users to sign-into the browser when it's "run as administrator" on Windows 10. This helps customers running Microsoft Edge on Windows server or in remote-desktop and sandbox scenarios.

- Microsoft Edge now provides full mouse support when in full screen mode. Now you can use your mouse to access tabs, the address bar, and other items without having to exit full screen mode.

- Online purchase improvement. Add custom nicknames to saved debit or credit cards. Now you can distinguish and differentiate your credit cards when making online purchases. Nicknaming your debit or credit cards lets you choose the correct card when using autofill to select a payment method.

- TLS/1.0 and TLS/1.1 are disabled by default.  The [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin) policy permits re-enabling of TLS/1.0 and TLS/1.1. This policy remains available until at least Microsoft Edge version 88. For more information, see [Site compatibility-impacting changes coming to Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

- Collections improvements:

  - A note capability is added that lets you add a note or comment to an item in a collection. Notes are grouped together and stay attached to an item even if you sort the items in a collection. To try this new feature, right-click on an item and select "Add note".
  - You can change the background color of notes in collections. You can use color coding to help you organize information and increase productivity.
  - There are noticeable performance improvements, which let you export your collections to  Excel in less time than in previous versions of Microsoft Edge.

- Extra Microsoft Edge API support:

  - The Storage Access API is enabled for experimentation. This feature is enabled for home users and Enterprise users with the [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol) policy set to "Full". This feature is enabled by default for all users in Microsoft Edge Stable Channel version 85.
  
    As privacy is becoming increasingly important to users, requests for stricter browser defaults and user opt-in settings like blocking all third-party storage access are increasingly common. While these settings help improve privacy and block unwanted access by unknown or untrusted parties, they can have unwanted side effects such as blocking access to content the user may want to view (for example, social media and embedded media content.)

    The Storage Access API allows access to first-party storage in a third-party context when a user provides a direct intent to allow storage that would otherwise be blocked by the browser's current configuration. For more information, see [Storage Access API](https://www.chromestatus.com/feature/5612590694662144).

  - The Native File System API, which means you can give sites permissions to edit files or folders via the Native File System API.

- PDF improvements:

  - Read Aloud for PDF lets users listen to PDF content while carrying out other tasks that may be important for them. It also helps audio visual learners focus on reading the content, making learning easier.
  - PDF file editing is improved. Now you can save an edit made to a PDF back to the file instead of saving a copy each time you edit the PDF.

- Microsoft Edge now enables Translation in the Immersive Reader. When a user opens the Immersive Reader view, they get the option to translate the page to their desired language.

- Several DevTools updates, including support for customizing keyboard shortcuts to match VS Code and viewing the DevTools in high contrast.  For more information, see [What's New In DevTools (Microsoft Edge 84)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/05/devtools).

### Policy updates

#### New policies

Seven new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [AppCacheForceEnabled](./microsoft-edge-policies.md#appcacheforceenabled) - Allows the AppCache feature to be re-enabled, even if it's turned off by default.
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy) - Configure the settings for the Application Guard Container Proxy.
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload) - Require that the Enterprise Mode Site List is available before tab navigation.
- [WinHttpProxyResolverEnabled](./microsoft-edge-policies.md#winhttpproxyresolverenabled) - Use the Windows proxy resolver.
- [InternetExplorerIntegrationEnhancedHangDetection](./microsoft-edge-policies.md#internetexplorerintegrationenhancedhangdetection) - Configure enhanced hang detection for Internet Explorer mode.
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - To reduce CPU and power consumption Microsoft Edge will detect when a window is covered by other windows, and will suspend work painting pixels.
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout) - Set a timeout for delay of tab navigation for the Enterprise Mode Site List.

#### Deprecated policies

- [AllowSyncXHRInPageDismissal](./microsoft-edge-policies.md#allowsyncxhrinpagedismissal) - Allow pages to send synchronous XHR requests during page dismissal.
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) - Determines whether the built-in certificate verifier will be used to verify server certificates.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled) - Enable stricter treatment for mixed content.

#### Obsoleted policy

[ForceNetworkInProcess](./microsoft-edge-policies.md#forcenetworkinprocess) - Force networking code to run in the browser process.

<!-- End 84 -->
## Version 83.0.478.64: July 13

Fixed various bugs and performance issues.

## Version 83.0.478.61: July 7

Fixed various bugs and performance issues.

## Version 83.0.478.58: June 30

Fixed various bugs and performance issues.

## Version 83.0.478.56: June 24

Fixed various bugs and performance issues.

Security updates are listed [here](./microsoft-edge-relnotes-security.md#june-24-2020)

## Version 83.0.478.54: June 17

Security updates are listed [here](./microsoft-edge-relnotes-security.md#june-17-2020)

## Version 83.0.478.50: June 15

Fixed various bugs and performance issues.

## Version 83.0.478.45: June 4

Security updates are listed [here](./microsoft-edge-relnotes-security.md#june-4-2020)

## Version 83.0.478.44: June 1

Fixed various bugs and performance issues.

## Version 83.0.478.37: May 21

Security updates are listed [here](./microsoft-edge-relnotes-security.md#may-21-2020)

### Feature updates

- Microsoft Edge updates will now roll out gradually. Going forward, updates for Microsoft Edge will be rolled out to our users over a period of a few days. This enables us to protect more of you from accidental buggy updates, which improves your update experience. As a user you'll continue to get seamless auto-updates. If your organization isn't enrolled for auto-updates, you won't be affected by this change. To learn more, see the [progressive rollouts article](microsoft-edge-update-progressive-rollout.md).
- Microsoft Defender SmartScreen improvements: Made several improvements to the Microsoft Defender SmartScreen service, such as improved protection from malicious sites that redirect when loading, and top-level frame blocking, which completely replaces malicious sites with the Microsoft Defender SmartScreen safety page. The top-level frame blocking prevents audio and other media from the malicious site from playing which gives an easier and less confusing experience.

- In response to user feedback, users can now exempt certain cookies from automatically clearing when the browser closes. This option is helpful if there's a site that users don't want to be signed out of, but still want to have all the other cookies cleared when the browser closes. To use this feature, go to *edge://settings/clearBrowsingDataOnClose* and enable the "Cookies and other site data" toggle.

- Automatic Profile Switching is now available to help you get to your work content more easily across profiles. If you use multiple profiles at work, you can check it out by navigating to a site requiring authentication from your work or school account while on your personal profile. When we detect this, you'll receive a prompt to switch to your work profile to access that site without having to authenticate to it. When you choose the work profile you want to switch to, the website will open in your work profile. This profile switching capability helps you keep your work and personal data separate and help you get to your work content more effortlessly. If you don't want the feature to prompt you to switch profiles, you can choose the don't ask me again option and it gets out of your way.

- Collections feature improvements:
  - You can use drag and drop to add an item to a collection without opening the collection. During the drag and drop you can also choose a location in the collection list where you want to put the item.
  - You can add multiple items to a collection instead of adding one item at a time. To add multiple items, select the items and then drag them to a collection. Or you can select the items, right-click and then pick the collection where you want the items.

- You can add all the tabs in an Microsoft Edge window into a new collection without adding them individually. To do this action, right-click on any tab and choose "Add all tabs to a new collection".

- Extension sync is now available. You can now sync your extensions across all your devices! Extensions from both the Microsoft and Chrome Stores sync with Microsoft Edge. To use this feature: Click the ellipses (**…**) on the menu bar, select **Settings**. Under Your profile, click **Sync** to see the Sync options. Under **Profiles/Sync** use the toggle to enable Extensions. You can use the [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) group policy to disable syncing of extensions.

- Improved the message on the Downloads management page for insecure downloads that have been blocked.

- Immersive Reader improvements:
  - Added support for Adverbs in the Parts of Speech experience we have in Immersive Reader. While reading an article within the Immersive Reader, open the Grammar Tools and switch on Adverbs within Parts of Speech to highlight all the adverbs on the page.
  - Added the ability to select any content on a webpage and open it in Immersive Reader. This ability enables users to use the Immersive Reader and all the Learning Tools, such as Line Focus and Read Aloud, across all websites.

- Link doctor provides host correction and a search query to the users when they mistype a URL. For example: <br>
A user mistypes "powerbi" as "powerbbi".com. Link doctor suggests "powerbi".com as a correction and create a link to search for "powerbbi" in case the user is looking for something different.

- Allow users to save their decision to launch an external protocol for a specific site. Users can configure the [ExternalProtocolDialogShowAlwaysOpenCheckbox](/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox) policy to enable or disable this feature.

- Users can set Microsoft Edge as their default browser directly from Microsoft Edge **Settings**. This makes it easier for users to change their default browser, within the context of the browser itself, instead of having to search through the operating system settings. To use this feature, go to *edge://settings/defaultBrowser* and click **Make default**.

- Several DevTools updates, including new remote debugging support, UI improvements, and more. For more information, see [What's New In DevTools (Microsoft Edge 83)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

- Microsoft Defender for Cloud Apps warn scenario is now available. This enables admins to set up warn, a new category of Defender for Cloud Apps blocks, where the user can override a Defender for Cloud Apps block page. MDATP E5 blocks are natively integrated with SmartScreen blocks in Microsoft Edge for a seamless experience. This experience allows for a full page red block with the message "This website is blocked by your organization", instead of just a toast notification.

- Disallow synchronous XmlHttpRequest in page dismissal. Sending of synchronous XmlHttpRequests during unload of a webpage will be removed. This change improves browser performance and reliability, but may impact web applications that haven't yet been updated to use more modern web APIs, including sendBeacon and fetch. The Group Policy to disable this change and permit synchronous XHR during page dismissal will be available until Microsoft Edge 88. For more information, see [Site compatibility-impacting changes coming to Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

### Policy updates

#### New policies

Fifteen new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [AllowSurfGame](./microsoft-edge-policies.md#allowsurfgame) - Allow surf game.
- [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) - Configure the list of sites for which Microsoft Edge attempts to establish a Token Binding with.
- [BingAdsSuppression](./microsoft-edge-policies.md#bingadssuppression) - Block all ads on Bing search results.
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) - Determines whether the built-in certificate verifier will be used to verify server certificates.
- [ClearCachedImagesAndFilesOnExit](./microsoft-edge-policies.md#clearcachedimagesandfilesonexit) - Clear cached images and files when Microsoft Edge closes.
- [ConfigureShare](./microsoft-edge-policies.md#configureshare) - Configure the Share experience.
- [DeleteDataOnMigration](./microsoft-edge-policies.md#deletedataonmigration) - Delete old browser data on migration.
- [DnsOverHttpsMode](./microsoft-edge-policies.md#dnsoverhttpsmode) - Control the mode of DNS-over-HTTPS.
- [DnsOverHttpsTemplates](./microsoft-edge-policies.md#dnsoverhttpstemplates) - Specify URI template of desired DNS-over-HTTPS resolver.
- [FamilySafetySettingsEnabled](./microsoft-edge-policies.md#familysafetysettingsenabled) - Allow users to configure Family safety.
- [LocalProvidersEnabled](./microsoft-edge-policies.md#localprovidersenabled) - Allow suggestions from local providers.
- [ScrollToTextFragmentEnabled](./microsoft-edge-policies.md#scrolltotextfragmentenabled) - Enable scrolling to text specified in URL fragments.
- [ScreenCaptureAllowed](./microsoft-edge-policies.md#screencaptureallowed) - Allow or deny screen capture.
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) - Configure the list of types that are excluded from synchronization.
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - Enable Hiding of Native Windows.

#### Deprecated policy

The following policy continues to work in this release. It will become "obsolete" in a future release.

[EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) Enable Domain Actions Download from Microsoft

<!-- end 83 -->

## Version 81.0.416.77: May 18

Fixed various bugs and performance issues.

## Version 81.0.416.72: May 7

Security updates are listed [here](./microsoft-edge-relnotes-security.md#may-7-2020)

## Version 81.0.416.68: April 29

Security updates are listed [here](./microsoft-edge-relnotes-security.md#april-29-2020)

## Version 81.0.416.64: April 23

Security updates are listed [here](./microsoft-edge-relnotes-security.md#april-23-2020)

## Version 81.0.416.58: April 17

Security updates are listed [here](./microsoft-edge-relnotes-security.md#april-17-2020)

## Version 81.0.416.53: April 13

Security updates are listed [here](./microsoft-edge-relnotes-security.md#april-13-2020)

### Feature updates

- Added support for Windows Information Protection (WIP), which helps enterprises protect sensitive data from unauthorized disclosure. [Learn More](./microsoft-edge-security-windows-information-protection.md).

- Collections are now available. To get started, select the Collections icon next to the address bar. This action opens the Collections pane where you can create, edit, and view Collections. We designed Collections based on what you do on the web. If you're a shopper, a traveler, a teacher, or a student, Collections can help. [Learn more](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97).

- Allow the removal (Hide from toolbar) of the Collections button from the Microsoft Edge toolbar for consistency.

- On-premises Active Directory account auto sign in will only be targeted to organizations that turn it on.  If users were already signed in with an on-premises AD account, they'll be able to sign out of it. Users will only be automatically signed in with the primary account on their operating system if it's a Microsoft account or a Microsoft Entra account. Admins can enable auto sign in with an on-premises AD account using the ConfigureOnPremisesAccountAutoSignIn policy.

- Application Guard. Extensions support now available in the container.

- Added a message to inform users that Internet Explorer isn't installed when they navigate to a page that's configured to open in Internet Explorer mode.

- Updated the 3D View tool in Microsoft Edge DevTools with a new feature to help debug z-index stacking context. 3D View shows a representation of the DOM (Document Object Model) depth using color and stacking, and the z-Index view helps you isolate the different stacking contexts of your page. [Learn more](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/).

- The F12 Dev tools are localized in 10 new languages, so they'll match the language used in the rest of the browser. [Learn more](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/).

- Added support for Dolby Vision playback. On Dolby Vision-enabled Windows 10 Build 17134 (April 2018 Update), websites can show Dolby vision content. See how to enable Dolby Vision content from [Netflix](https://help.netflix.com/en/node/42384).

- Microsoft Edge can now identify and remove duplicate favorites and merge folders with the same name. To access the tool, select the star on the browser's toolbar and select "Remove duplicate favorites".  You can that confirm changes and any updates to your favorites will be synced across devices.

- We heard from users it can be difficult to distinguish a normal browsing window in dark theme from an InPrivate window since both window frames are dark. The new solid InPrivate blue pill in the top right corner helps reassure users they're browsing InPrivate.

- Open external links in the correct browser profile. Select a default profile for links opened for external apps to open in from *edge://settings/multiProfileSettings*.

- Added a warning that alerts users who sign into a browser profile with an account after being previously signed in with another account. This warning helps prevent unintentional data merging.

- If you have payment cards saved in your Microsoft account, you can use them in Microsoft Edge while filling out payment forms. The cards in your Microsoft account will sync across desktop devices and the full details will be shared with the website after two-factor authentication (CVC code and your Microsoft identity.) For further convenience, you can choose to securely save a copy of the card on the device during authentication.

- Line Focus is designed for users who like to focus on a limited part of the content as they read. It lets users keep the focus on one, three, or five lines at a time and dims out the rest of the page to let users read without distraction. Users can scroll using touch or arrow keys and the focus shifts accordingly.

- Microsoft Edge is now integrated with Windows Speller on Windows platforms 8.1 and above. This integration provides greater language support, with access to more language dictionaries and the ability to use Windows custom dictionaries. There's no further action needed from the users when a language is added in the OS language settings. Also, a language spellcheck toggle is enabled in Microsoft Edge settings.

- When PDF documents are opened using Microsoft Edge, users will now be able to create highlights, change color, and delete highlights. This feature helps in referencing important parts of the document later, and for collaboration.

- When loading long PDF documents that have been optimized for web, the pages being viewed by the user will be loaded faster, parallelly, while the rest of the document is loading.

- Now it's easier to start the Immersive Reader for a website by just pressing the F9 key.

- Now it's easier to start Read Aloud by using a keyboard shortcut (Ctrl + Shift + U).

- Added an MSI command line parameter that lets you suppress Desktop icon creation when you install Microsoft Edge. The following example shows how to use this new parameter: <br>
`MicrosoftEdgeEnterpriseX64.msi DONOTCREATEDESKTOPSHORTCUT=true`<br>
There will be a group policy to support this functionality in an upcoming release.

### Policy updates

#### New policies

11 new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled) - Enable Ambient Authentication for InPrivate and Guest profiles. 
- [AudioSandboxEnabled](./microsoft-edge-policies.md#audiosandboxenabled) - Allow the audio sandbox to run.
- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) - Use a default referrer policy of no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](./microsoft-edge-policies.md#globallyscopehttpauthcacheenabled) - Enable globally scoped HTTP auth cache.
- [ImportExtensions](./microsoft-edge-policies.md#importextensions) - Allow importing of extensions.
- [ImportCookies](./microsoft-edge-policies.md#importcookies) - Allow importing of Cookies.
- [ImportShortcuts](./microsoft-edge-policies.md#importshortcuts) - Allow importing of shortcuts.
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect) - Specify how "in-page" navigations to unconfigured sites behave when started from Internet Explorer mode pages.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled) - Enable stricter treatment for mixed content.
- [TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled) - Enable a TLS 1.3 security feature for local trust anchors.
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin) - Configure automatic sign in with an Active Directory domain account when there is no Microsoft Entra domain account.

#### Policy name and caption changes

The policy `OmniboxMSBProviderEnabled` is changed to [AddressBarMicrosoftSearchInBingProviderEnabled](/DeployEdge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled) - The caption for the policy is "Enable Microsoft Search in Bing suggestions in the address bar".

#### Deprecated policies

The following policies continue to work in this release. They will become "obsolete" in a future release.

- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) - Re-enable Web Components v0 API until M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) - Allow WebDriver to Override Incompatible.

#### Resolved issues

- Fixed an issue where IE mode on Microsoft Edge caused an ongoing download dialog to show even after the file was downloaded.
- Fixed an issue where Microsoft Edge was dropping session cookies when a page already in IE mode triggered to open a new IE mode tab.

## Version 80.0.361.111: April 7

Fixed various bugs and performance issues.

## Version 80.0.361.109: April 1

Security updates are listed [here](./microsoft-edge-relnotes-security.md#april-1-2020)

## Version 80.0.361.69: March 19

Security updates are listed [here](./microsoft-edge-relnotes-security.md#march-19-2020)

## Version 80.0.361.66: March 4

Security updates are listed [here](./microsoft-edge-relnotes-security.md#march-4-2020)

## Version 80.0.361.62: February 25

Security updates are listed [here](./microsoft-edge-relnotes-security.md#february-25-2020)

## Version 80.0.361.57: February 20

Security updates are listed [here](./microsoft-edge-relnotes-security.md#february-20-2020)

## Version 80.0.361.56: February 19

Fixed various bugs and performance issues.

## Version 80.0.361.54: February 14

### Resolved issues

- Fixed an issue where Password, Payment, and Cookies fail to get imported in Microsoft Edge.

## Version 80.0.361.50: February 11

Fixed various bugs and performances fixes.

## Version 80.0.361.48: February 7

Security updates are listed [here](./microsoft-edge-relnotes-security.md#february-7-2020)

### Feature updates

- Added SmartScreen protection from downloading potentially unwanted apps. [Learn more](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus)
- Added support for Dolby Vision playback.
- Enabled users of Windows Mixed Reality to view 360° videos on VR headsets.
- Added an option to Reading View to increase text spacing.
- Added support for erasing link using the Surface Pen eraser.
- Added support for using the arrow keys and spacebar to draw on feedback screenshots in editor mode.
- Improved the reliability of screenshots so they stop appearing all black when submitting feedback.
- Added dark theme support to the local new tab page that is shown when the device isn't connected to the internet.
- Added the ability for websites that are installed as apps to be restored when a browser session is restored after an update, crash, and so on.
- Added dark theme support to PDF UI when the browser is managed by Group Policy.
- Updated Adobe Flash to version 32.0.0.321. [Learn more](https://helpx.adobe.com/flash-player/release-note/fp_32_air_32_release_notes.html)

### Policy updates

#### New policies

16 new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [AlternateErrorPagesEnabled](./microsoft-edge-policies.md#alternateerrorpagesenabled) - Suggest similar pages when a webpage can't be found.
- [DefaultInsecureContentSetting](./microsoft-edge-policies.md#defaultinsecurecontentsetting)  - Control use of insecure content exceptions.
- [DNSInterceptionChecksEnabled](./microsoft-edge-policies.md#dnsinterceptionchecksenabled) - DNS interception checks enabled.
- [HideFirstRunExperience](./microsoft-edge-policies.md#hidefirstrunexperience) - Hide the First-run experience and splash screen.
- [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) - Allow insecure content on specified sites.
- [InsecureContentBlockedForUrls](./microsoft-edge-policies.md#insecurecontentblockedforurls) - Block insecure content on specified sites.
- [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled) - Enable default legacy SameSite cookie behavior setting.
- [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) - Revert to legacy SameSite behavior for cookies on specified sites.
- [PaymentMethodQueryEnabled](./microsoft-edge-policies.md#paymentmethodqueryenabled) - Allow websites to query for available payment methods.
- [PersonalizationReportingEnabled](./microsoft-edge-policies.md#personalizationreportingenabled) - Allow personalization of ads, search, and news by sending browsing history to Microsoft.
- [PinningWizardAllowed](./microsoft-edge-policies.md#pinningwizardallowed) - Allow Pin to taskbar wizard.
- [SmartScreenPuaEnabled](./microsoft-edge-policies.md#smartscreenpuaenabled) - Configure Microsoft Defender SmartScreen to block potentially unwanted apps.
- [TotalMemoryLimitMb](./microsoft-edge-policies.md#totalmemorylimitmb) - Set limit on megabytes of memory a single Microsoft Edge instance can use.
- [WebAppInstallForceList](./microsoft-edge-policies.md#webappinstallforcelist) - Configure list of force-installed Web Apps.
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) - Re-enable Web Components v0 API until M84.
- [WebRtcLocalIpsAllowedUrls](./microsoft-edge-policies.md#webrtclocalipsallowedurls) - Manage exposure of local IP addresses by WebRTC.

#### Deprecated policies

The following policy was deprecated.

- [NewTabPageCompanyLogo](./microsoft-edge-policies.md#newtabpagecompanylogo) - Set new tab page company logo.

### Resolved issues

- Fixed an issue where audio isn't working in Citrix environment.
- Fixed an issue where Microsoft Edge and legacy Microsoft Edge side-by-side experience results in broken legacy links and crashes.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)