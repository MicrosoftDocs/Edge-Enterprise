---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 05/20/2024
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

## Version 125.0.2535.51: May 17, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-16-2024).

### Dev Channel updates

The following Dev channel updates preceded this Stable channel release. The following Dev notes provide detailed information about the changes in each release.

- [Dev Channel update to 125.0.2492.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-125-0-2492-1-is-live/m-p/4103542)
- [Dev Channel update to 125.0.2506.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-125-0-2506-0-is-live/m-p/4113302)
- [Dev Channel update to 125.0.2518.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-125-0-2518-0-is-live/m-p/4117088)

**Announcement**

Microsoft Defender Application Guard extension deprecation. Because Application Guard is deprecated, there won't be a migration to Edge Manifest V3. The corresponding extensions and associated [Windows Store app](https://apps.microsoft.com/detail/9n8gnlc8z9c8?hl=en-us&gl=US) will not be available after May 2024. This affects the following browsers: [Application Guard Extension - Chrome](https://chromewebstore.google.com/detail/application-guard-extensi/mfjnknhkkiafjajicegabkbimfhplplj) and [Application Guard Extension - Firefox](https://addons.mozilla.org/en-US/firefox/addon/application-guard-extension/). If you want to block unprotected browsers until you're ready to retire MDAG usage in your enterprise, we recommend using AppLocker policies or [Microsoft Edge management service](/deployedge/microsoft-edge-management-service). For more information, see [Microsoft Edge and Microsoft Defender Application Guard](/deployedge/microsoft-edge-security-windows-defender-application-guard), [Deprecated features in the Windows client - What's new in Windows](/windows/whats-new/deprecated-features), and [Microsoft Defender Application Guard - Windows Security](/windows/security/application-security/application-isolation/microsoft-defender-application-guard/md-app-guard-overview).

### Feature Updates

- **Improved user experience for Purview copy/paste controls in Edge.** Our Purview cut/copy/paste experience is now more user friendly with self-dismissing dialogs on successful paste. The existing "Paste to supported browsers" setting allows organizations to classify and protect the content that end users can paste – both to specific websites and through supported browsers. You can follow the instructions in [Use Endpoint data loss prevention (DLP)](/purview/endpoint-dlp-using?tabs=purview#create-your-dlp-policy) to create the DLP policy.

- **New Workspaces color display: browser window outline.** Workspaces each have a dedicated color, and that color is now displayed as an outline on the browser window. The previous experience applied the color across the entire tab strip in horizontal tab orientation, and across the title bar in vertical tab orientation. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Full Favorites Bar available in Workspaces.** Workspaces now display a user's full set of favorites in the Favorites Bar, with a dedicated workspace folder accessible from the bar. The previous experience replaced the Favorites Bar with the workspace favorites folder. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

### Policy updates

#### New policies

- [ImageEditorServiceEnabled](/deployedge/microsoft-edge-policies#imageeditorserviceenabled) - Enable the Designer for Image Editor feature
- [ZstdContentEncodingEnabled](/deployedge/microsoft-edge-policies#zstdcontentencodingenabled) - Enable zstd content encoding support
- [QRCodeGeneratorEnabled](/deployedge/microsoft-edge-policies#qrcodegeneratorenabled) - Enable QR Code Generator

#### Deprecated policies

- [AllowTokenBindingForUrls](/deployedge/microsoft-edge-policies#allowtokenbindingforurls) - Configure the list of sites for which Microsoft Edge will attempt to establish a Token Binding with (deprecated)

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

- **Customize organizational branding using the Microsoft Edge management service.** Admins can customize their organization's branding assets onto Edge for Business through the Microsoft Edge management service. This branding can help users signed in with a Microsoft Entra ID more easily differentiate between multiple profiles and browser windows through visual cues on the profile pill, profile flyout, and Edge for Business taskbar icon.

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

- **Updated UX for Microsoft Defender for Endpoint blocks.** Microsoft Edge now provides a different blocking experience for Microsoft Defender for Endpoint based blocks (Web Content Filtering and Custom Indicators). For more information, see [Web protection](/microsoft-365/security/defender-endpoint/web-protection-overview?view=o365-worldwide).

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

- Fixed a browser crash that occurred when the **UserDataDir** policy is used to specify a path on a network share. Note that using a network share location for the user data directory is generally unsupported.

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

- **Customize organizational branding using the Microsoft Edge management service.** Admins can customize their organization's branding assets onto Edge for Business through the Microsoft Edge management service. This branding can help users signed in with an Entra ID (formerly known as Azure Active Directory) more easily differentiate between multiple profiles and browser windows through visual cues on the profile pill, profile flyout, and Edge for Business taskbar icon.

  This Microsoft Edge management service feature will give admins an enhanced experience to configure, preview, and customize how Edge for Business shows the following organization brand assets:

  - Organization name
  - Accent color
  - Organization logo
  - Edge for Business taskbar icon overlay

  **Note:** This experience is in public preview and can be accessed by opting in to targeted release in the M365 admin center. For more information, see [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business).

- **Automatic profile switching controls for Microsoft Edge for Business in the Microsoft Edge management service.** The Microsoft Edge management service will provide admins with the ability to configure settings for automatic profile switching in the Microsoft Edge browser. This can help enforce context separation between their end users' work and personal browsing. **Note:** This experience is in public preview and can be accessed by opting in to targeted release in the M365 admin center.

### Policy updates

#### New policies

- [AccessControlAllowMethodsInCORSPreflightSpecConformant](/deployedge/microsoft-edge-policies#accesscontrolallowmethodsincorspreflightspecconformant) - Make Access-Control-Allow-Methods matching in CORS preflight spec conformant
- [AdditionalSearchBoxEnabled](/deployedge/microsoft-edge-policies#additionalsearchboxenabled) - Enable additional search box in browser
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

<!-- ===================== snip for archive ========================== -->
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
