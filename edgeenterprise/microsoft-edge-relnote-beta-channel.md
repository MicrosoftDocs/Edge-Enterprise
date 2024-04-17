---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 04/17/2024
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

## Version 124.0.2478.49: April 17, 2024

Fixed various bugs and performance issues.

## Version 124.0.2478.39: April 12, 2024

Fixed various bugs and performance issues.

## Version 124.0.2478.27: April 8, 2024

Fixed various bugs and performance issues.

## Version 124.0.2478.19: April 1, 2024

Fixed various bugs and performance issues.

### Feature updates

- **Cross-device Search Query History suggestions.** The existing Search Query suggestions are enhanced with cross-device query history in both Recent Searches and browser searches for enterprise users who enable Edge Sync across devices/browsers. From now on Edge gives you the relevant query history suggestions that you used for previous searches, regardless of where you did it. You can always trust Edge to help you quickly re-find the information that you accessed before.

- **Enterprise secure AI controls in the Microsoft Edge management service.** The Microsoft Edge management service now provides a new dedicated space for admins to manage all AI-related policies in the Edge browser. This helps enhance security and productivity for managed users and devices.

## Version 124.0.2478.10: March 28, 2024

Fixed various bugs and performance issues, updated features, and policies.

### Dev Channel updates

The following Dev channel updates preceded this Beta channel release. The following Dev notes provide detailed information about the changes in each release.

- [Dev Channel update to 124.0.2438.2 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-124-0-2438-2-is-live/m-p/4079136)
- [Dev Channel update to 124.0.2450.2 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-124-0-2450-2-is-live/m-p/4085888)
- [Dev Channel update to 124.0.2464.2 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-124-0-2464-2-is-live/m-p/4092459)
- [Dev Channel update to 124.0.2478.6 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-124-0-2478-6-is-live/m-p/4097816)

### Feature updates

- **Email notifications for extension requests in the Microsoft Edge management service.** The Microsoft Edge management service provides admins with the ability to receive email notifications for extensions that their users requested. This helps inform them promptly of any new feedback. **Note:** This experience is in public preview and can be accessed by opting in to targeted release in the Microsoft 365 admin center.

- **Updated default profile pill for EDU users in Edge for Business.** To improve the applicability of the current Edge for Business default visuals, users signed in with an EDU account will see the default profile pill label updated to "School".

- **Desktop Shortcut for New Enterprise Devices.** New Microsoft Enterprise devices running through Windows Out of Box Experience (OOBE) for the first time will see a Microsoft Edge desktop shortcut automatically created. This desktop shortcut provides users with an alternative way to access their Microsoft Edge browser without needing to manually pin and configure their set-up.

- **Updated profile options in new profile experience.** Many users unintentionally create empty profiles, cluttering their workspace and impeding their browsing experience. To reduce clutter and the likelihood of profile churn, updated First Run Experience (FRE) string options encourage users to sign-in and meaningfully create profiles for an improved browsing experience, or easily cancel unintentional creation. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Copilot Page Context Policies.** To summarize and answer questions based on page context in Microsoft Edge, Copilot needs to be able to access the page content. We're providing two new policies to offer more flexibility for admins to customize Edge page context access across Copilot chats in Edge sidebar.
   - [CopilotPageContext](/deployedge/microsoft-edge-policies#copilotpagecontext) - Control Copilot access to page contents for Microsoft Entra ID profiles
   - [CopilotCDPPageContext](/deployedge/microsoft-edge-policies#copilotcdppagecontext) - Control Copilot with Commercial Data Protection access to page contents for Microsoft Entra ID profiles

   - The [DiscoverPageContextEnabled](/deployedge/microsoft-edge-policies#discoverpagecontextenabled) policy is deprecated in Edge version 124 and will be obsoleted in Edge version 127.

- **Updates to Settings pages on privacy, security, search, & services.**  To improve ease of use, we're updating Edge settings page into two sections: "Privacy and Security" and "Search and Services." This streamlined approach should enable users to find the settings they're interested in more easily. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Removal of Web SQL.** Web SQL support is fully removed. In prior releases, Web SQL support was disabled by default but could be re-enabled via the [WebSQLAccess policy](/deployedge/microsoft-edge-policies?branch=pr-en-us-4033#websqlaccess). After this change, there's no longer any mechanism to enable Web SQL support. This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, see [Intent to Deprecate and Remove Web SQL](https://groups.google.com/a/chromium.org/g/blink-dev/c/fWYb6evVA-w/m/pziWcvboAgAJ).

- **Sidebar Tools App - SpeedTest.**  Adding a SpeedTest answer by default to the Tools app in the Microsoft Edge sidebar.  For more information, see [Manage the sidebar in Microsoft Edge](/deployedge/microsoft-edge-sidebar).

- **Updated Edge Profile account re-authentication popup when Browser to Web Single-Sign-On (SSO) fails.** Edge provides a browser to Web single sign-on (SSO) capability that lets a user sign in to their Edge Profile with a web account first and then automatically sign them into Microsoft first party websites.

  This is done by saving cached credentials. This approach works until there's an authentication challenge to the cached credentials. A typical scenario is when a user changes their password on a different device. The cached credentials on the current device become outdated and SSO fails. Edge detects this failure and shows a re-authentication popup that prompts the user to update their cached credentials on the current device.

- **Updated profile management and customization controls.** Enhancing the profile management and customization experience through surfaced profile controls and an expanded range of default avatars. With these updates, users can effortlessly tailor their profiles to their preferences and select from a broader collection of profile avatars.

### Policy updates

#### New policies

- [CopilotCDPPageContext](/deployedge/microsoft-edge-policies#copilotcdppagecontext) - Control Copilot with Commercial Data Protection access to page context for Microsoft Entra ID profiles
- [CopilotPageContext](/deployedge/microsoft-edge-policies#copilotpagecontext) - Control Copilot access to page context for Microsoft Entra ID profiles
- [MutationEventsEnabled](/deployedge/microsoft-edge-policies#mutationeventsenabled) - Enable deprecated/removed Mutation Events

#### Deprecated policies

- [DiscoverPageContextEnabled](/deployedge/microsoft-edge-policies#discoverpagecontextenabled) - Enable Discover access to page contents for AAD profiles (deprecated)

#### Obsoleted policies

- [ThrottleNonVisibleCrossOriginIframesAllowed](/deployedge/microsoft-edge-policies#throttlenonvisiblecrossoriginiframesallowed) - Allows enabling throttling of non-visible, cross-origin iframes (obsolete)
- [WebSQLAccess](/deployedge/microsoft-edge-policies#websqlaccess) - Force WebSQL to be enabled (obsolete)

## Version 123.0.2420.65: March 27, 2024

Fixed various bugs and performance issues.
 
## Version 123.0.2420.53: March 21, 2024

Fixed various bugs and performance issues.


## Version 123.0.2420.51: March 20, 2024

Fixed various bugs and performance issues.

## Version 123.0.2420.41: March 15, 2024

Fixed various bugs and performance issues.

## Version 123.0.2420.32: March 11, 2024

Fixed various bugs and performance issues.

## Version 123.0.2420.20: March 5, 2024

Fixed various bugs and performance issues.

## Version 123.0.2420.10: February 29, 2024

Fixed various bugs and performance issues.

### Dev Channel updates

The following Dev channel updates preceded this Beta channel release. The following Dev notes provide detailed information about the changes in each release.

- [Dev Channel update to 123.0.2380.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-123-0-2380-1-is-live/m-p/4050755)
- [Dev Channel update to 123.0.2400.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-123-0-2400-1-is-live/m-p/4058807)
- [Dev Channel update to 123.0.2420.6 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-123-0-2420-6-is-live/m-p/4069388)

### Feature updates

- **Customize organizational branding using the Microsoft Edge management service.** Admins can customize their organization's branding assets onto Edge for Business through the Microsoft Edge management service. This branding can help users signed in with a Microsoft Entra ID (formerly known as Azure Active Directory) more easily differentiate between multiple profiles and browser windows through visual cues on the profile pill, profile flyout, and Microsoft Edge for Business taskbar icon.

  The Microsoft Edge management service gives admins an enhanced experience to configure, preview, and customize how Microsoft Edge for Business shows the following organization brand assets:

  - Organization name
  - Accent color
  - Organization logo
  - Microsoft Edge for Business taskbar icon overlay

  For more information, see [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business).

- **Automatic profile switching controls for Microsoft Edge for Business in the Microsoft Edge management service.** The Microsoft Edge management service provides admins with the ability to configure settings for automatic profile switching in the Microsoft Edge browser. This can help enforce context separation between their end users' work and personal browsing. Note: This experience is in public preview.

- **Extending support for viewing MIP Protected PDF Files to different sovereignties (including GCCH).** Sovereign cloud customers (including GCCH) can open MIP protected PDF content in Microsoft Edge. This change is available in the Microsoft Edge built-in PDF reader powered by Adobe Acrobat and the legacy Microsoft Edge PDF engine.  **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

### Policy updates

#### New policies

- [ExtensionInstallTypeBlocklist](/deployedge/microsoft-edge-policies#extensioninstalltypeblocklist) - Blocklist for extension install types
- [ExtensionManifestV2Availability](/deployedge/microsoft-edge-policies#extensionmanifestv2availability) - Control Manifest v2 extension availability
- [DefaultWindowManagementSetting](/deployedge/microsoft-edge-policies#defaultwindowmanagementsetting) - Default Window Management permission setting
- [WindowManagementAllowedForUrls](/deployedge/microsoft-edge-policies#windowmanagementallowedforurls) - Allow Window Management permission on specified sites
- [WindowManagementBlockedForUrls](/deployedge/microsoft-edge-policies#windowmanagementblockedforurls) - Block Window Management permission on specified sites
- [RSAKeyUsageForLocalAnchorsEnabled](/deployedge/microsoft-edge-policies#rsakeyusageforlocalanchorsenabled) - Check RSA key usage for server certificates issued by local trust anchors
- [ScreenCaptureWithoutGestureAllowedForOrigins](/deployedge/microsoft-edge-policies#screencapturewithoutgestureallowedfororigins) - Allow screen capture without prior user gesture
 
## Version 122.0.2365.59: February 27, 2024

Fixed various bugs and performance issues.

## Version 122.0.2365.52: February 23, 2024

Fixed various bugs and performance issues.

## Version 122.0.2365.50: February 22, 2024

Fixed various bugs and performance issues.

### Fixes

- Resolved an issue where printing certain PDF files in landscape mode with the "fit to printable area" option, resulted in incorrect printing.

## Version 122.0.2365.38: February 16, 2024

Fixed various bugs and performance issues.

### Feature updates

- **Microsoft Edge has rebranded Web Capture to "Screenshot".**  Microsoft Edge changed the branding for Web Capture with an icon change and renamed the feature to "Screenshot". Users can easily use content from the web by taking a screenshot of a full page or a selected area. They can mark up the screenshot they took with a pen or touch later.  Administrators can control availability using the [WebCaptureEnabled](/deployedge/microsoft-edge-policies#webcaptureenabled) policy.  For more information, see [Screenshot (microsoft.com)](https://www.microsoft.com/en-us/edge/features/screenshot?form=MA13FJ). 

## Version 122.0.2365.30: February 12, 2024

Fixed various bugs and performance issues.

## Version 122.0.2365.16: February 5, 2024

Fixed various bugs and performance issues.

## Version 122.0.2365.8: February 1, 2024

Fixed various bugs and performance issues.

### Fixes

- Resolved an issue where PDF text fields and drop downs values were being rendered twice for specific files when using the Microsoft Edge built-in PDF reader powered by Adobe Acrobat.

### Dev Channel updates

The following Dev channel updates preceded this Beta channel release. The following Dev notes provide detailed information about the changes in each release.

- [Dev Channel update to 122.0.2325.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/discussions/dev-channel-update-to-122-0-2325-0-is-live/m-p/4026405)
- [Dev Channel update to 122.0.2348.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/discussions/dev-channel-update-to-122-0-2348-0-is-live/m-p/4034978)
- [Dev Channel update to 122.0.2353.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/discussions/dev-channel-update-to-122-0-2353-0-is-live/m-p/4039264)
- [Dev Channel update to 122.0.2365.3 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-122-0-2365-3-is-live/m-p/4044002)
    
### Feature updates

- **Moving Managed Site Indicator (Briefcase icon) into the lock icon in the address bar omnibox.**  The briefcase icon, which signals that a page is managed, is moved into the lock icon within the address bar. If an admin wants to see whether there are protections for a given page, they can select to open the lock icon in the address bar to look for the briefcase icon.

- **Deprecation of the image enhancement feature.** To improve end user experience, the image enhancement feature is deprecated.  

- **Configure recommended policies in the Microsoft Edge management service.** The Microsoft Edge management service provides admins with controls to configure recommended policies. This gives end users permission to override the configured policy.

### Policy updates

#### New policies

- [AIGenThemesEnabled](/deployedge/microsoft-edge-policies#aigenthemesenabled) Enables DALL-E themes generation
- [EnhanceSecurityModeAllowUserBypass](/deployedge/microsoft-edge-policies#enhancesecuritymodeallowuserbypass) Allow users to bypass Enhanced Security Mode
- [SuperDragDropEnabled](/deployedge/microsoft-edge-policies#super-drag-drop-enabled) Super Drag Drop Enabled

#### Obsoleted policies

- [EdgeEnhanceImagesEnabled](/deployedge/microsoft-edge-policies#edgeenhanceimagesenabled) Enhance images enabled  

<!-- Version 121.0.2277.83: January 25, 2024, 2023 to Version 121.0.2277.4: December 15, 2023 -->
<!-- Version 120.0.2210.61: December 7, 2023 to Version 120.0.2210.7: November 13, 2023 -->
<!-- Version 119.0.2151.44: November 2, 2023, 2023 to Version 119.0.2151.24: October 23, 2023 -->
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
