---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 06/17/2024
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

## Version 126.0.2592.61: June 17, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.56: June 13, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.53: June 12, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.49: June 10, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.36: June 3, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.24: May 28, 2024

Fixed various bugs and performance issues.

## Version 126.0.2592.13: May 23, 2024

Fixed various bugs and performance issues, Dev channel updates, feature updates, and policy updates.

### Dev Channel updates

The following Dev channel updates preceded this Beta channel release. These notes provide detailed information about the changes in each release.

- [Dev Channel update to 126.0.2552.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-126-0-2552-0-is-live/m-p/4131066)
- [Dev Channel update to 126.0.2566.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-126-0-2566-1-is-live/m-p/4133928)
- [Dev Channel update to 126.0.2578.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-126-0-2578-1-is-live/m-p/4144544)

### Feature updates

- **AI theme generator.** Microsoft Edge will include an AI theme generator, that allows users to input a text prompt and generate a series of images to preview as browser themes. Applying the theme includes setting the generated image on the Edge new tab page and applying the image's dominant color to the browser frame. Admins can control availability to this feature using the [AIGenThemesEnabled](/deployedge/microsoft-edge-policies#enables-dall-e-themes-generation) policy.  **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Security protection controls in the Microsoft Edge management service.**  The Microsoft Edge management service will provide admins with a dedicated experience to manage specific settings that help improve the security posture of their managed browser instances. **Note:** This experience is in public preview and can be accessed by opting in to targeted release in the Microsoft 365 admin center.

- **Copilot summarization notification.**  The feature displays an Omnibox notification when users enter into a reading mode eligible page in Edge and offers them the option to open Copilot in the sidebar to generate a summary of the content.  **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

### Policy updates
 
#### Obsoleted policies

-    [MathSolverEnabled](/deployedge/microsoft-edge-policies#mathsolverenabled) - Let users snip a Math problem and get the solution with a step-by-step explanation in Microsoft Edge (obsolete)
-    [ImmersiveReaderGrammarToolsEnabled](/deployedge/microsoft-edge-policies#immersivereadergrammartoolsenabled) - Enable Grammar Tools feature within Immersive Reader in Microsoft Edge (obsolete)
 
## Version 125.0.2535.51: May 17, 2024

Fixed various bugs and performance issues.

## Version 125.0.2535.47: May 15, 2024

Fixed various bugs and performance issues.

## Version 125.0.2535.37: May 10, 2024

Fixed various bugs and performance issues.

## Version 125.0.2535.29: May 6, 2024

Fixed various bugs and performance issues.

### Feature updates

- **Improved user experience for Purview copy/paste controls in Edge.** Our Purview cut/copy/paste experience is now more user friendly with self-dismissing dialogs on successful paste. The existing "Paste to supported browsers" setting allows organizations to classify and protect the content that end users can paste – both to specific websites and through supported browsers. You can follow the instructions in [Use Endpoint data loss prevention (DLP)](/purview/endpoint-dlp-using?tabs=purview#create-your-dlp-policy) to create the DLP policy.

## Version 125.0.2535.13: April 29, 2024

Fixed various bugs and performance issues.

### Dev Channel updates

The following Dev channel updates preceded this Beta channel release. The following Dev notes provide detailed information about the changes in each release.

- [Dev Channel update to 125.0.2492.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-125-0-2492-1-is-live/m-p/4103542)
- [Dev Channel update to 125.0.2506.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-125-0-2506-0-is-live/m-p/4113302)
- [Dev Channel update to 125.0.2518.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-125-0-2518-0-is-live/m-p/4117088)

### Feature updates

- **Microsoft Defender Application Guard extension deprecation.** Because Application Guard is deprecated, there won't be a migration to Edge Manifest V3. The corresponding extensions and associated [Windows Store app](https://apps.microsoft.com/detail/9n8gnlc8z9c8?hl=en-us&gl=US) will not be available after May 2024. This affects the following browsers: [Application Guard Extension - Chrome](https://chromewebstore.google.com/detail/application-guard-extensi/mfjnknhkkiafjajicegabkbimfhplplj) and [Application Guard Extension - Firefox](https://addons.mozilla.org/en-US/firefox/extensions/category/privacy-security/). If you want to block unprotected browsers until you're ready to retire MDAG usage in your enterprise, we recommend using AppLocker policies or [Microsoft Edge management service](/deployedge/microsoft-edge-management-service). For more information, see [Microsoft Edge and Microsoft Defender Application Guard](/deployedge/microsoft-edge-security-windows-defender-application-guard), [Deprecated features in the Windows client - What's new in Windows](/windows/whats-new/deprecated-features), and [Microsoft Defender Application Guard - Windows Security](/windows/security/application-security/application-isolation/microsoft-defender-application-guard/md-app-guard-overview).

- **Auto-discarding Sleeping Tabs.** Tabs that have been sleeping for a long time are discarded to save memory. When a user navigates back to a discarded tab, the tab needs to be reloaded. This can be managed through the [AutoDiscardSleepingTabsEnabled](/deployedge/microsoft-edge-policies#autodiscardsleepingtabsenabled) policy. This policy is enabled if the [SleepingTabsEnabled](/deployedge/microsoft-edge-policies#sleepingtabsenabled) policy is enabled. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **New Workspaces color display: browser window outline.** Workspaces each have a dedicated color, and that color is now displayed as an outline on the browser window. The previous experience applied the color across the entire tab strip in horizontal tab orientation, and across the title bar in vertical tab orientation. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Full Favorites Bar available in Workspaces.** Workspaces now display a user's full set of favorites in the Favorites Bar, with a dedicated workspace folder accessible from the bar. The previous experience replaced the Favorites Bar with the workspace favorites folder. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

### Policy updates

#### New policies

- [ImageEditorServiceEnabled](/deployedge/microsoft-edge-policies#imageeditorserviceenabled) - Enable the Designer for Image Editor feature
- [ZstdContentEncodingEnabled](/deployedge/microsoft-edge-policies#zstdcontentencodingenabled) - Enable zstd content encoding support
- [QRCodeGeneratorEnabled](/deployedge/microsoft-edge-policies#qrcodegeneratorenabled) - Enable QR Code Generator

## Version 124.0.2478.67: April 26, 2024

Fixed various bugs and performance issues.

## Version 124.0.2478.51: April 18, 2024

Fixed various bugs and performance issues.

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
   - [CopilotPageContext](/deployedge/microsoft-edge-policies#copilotpagecontext) - Control Copilot access to browser context for Microsoft Entra ID profiles
   - [CopilotCDPPageContext](/deployedge/microsoft-edge-policies#copilotcdppagecontext) - Control Copilot with Commercial Data Protection access to browser context for Microsoft Entra ID profiles
   - The [DiscoverPageContextEnabled](/deployedge/microsoft-edge-policies#discoverpagecontextenabled) policy is deprecated in Edge version 124 and will be obsoleted in Edge version 127.

- **Inline Compose.** This feature allows users to rewrite text using Copilot. Users can highlight text they'd like to improve when writing in Edge and use the Rewrite tool to iterate with different lengths, formats, and tones. Administrators can control availability using the [ComposeInlineEnabled](/deployedge/microsoft-edge-policies#composeinlineenabled) policy.

- **Updates to Settings pages on privacy, security, search, & services.**  To improve ease of use, we're updating Edge settings page into two sections: "Privacy and Security" and "Search and Services." This streamlined approach should enable users to find the settings they're interested in more easily. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Removal of Web SQL.** Web SQL support is fully removed. In prior releases, Web SQL support was disabled by default but could be re-enabled via the [WebSQLAccess policy](/deployedge/microsoft-edge-policies?branch=pr-en-us-4033#websqlaccess). After this change, there's no longer any mechanism to enable Web SQL support. This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, see [Intent to Deprecate and Remove Web SQL](https://groups.google.com/a/chromium.org/g/blink-dev/c/fWYb6evVA-w/m/pziWcvboAgAJ).

- **Sidebar Tools App - SpeedTest.**  Adding a SpeedTest answer by default to the Tools app in the Microsoft Edge sidebar.  For more information, see [Manage the sidebar in Microsoft Edge](/deployedge/microsoft-edge-sidebar).

- **Updated Edge Profile account re-authentication popup when Browser to Web Single-Sign-On (SSO) fails.** Edge provides a browser to Web single sign-on (SSO) capability that lets a user sign in to their Edge Profile with a web account first and then automatically sign them into Microsoft first party websites.

  This is done by saving cached credentials. This approach works until there's an authentication challenge to the cached credentials. A typical scenario is when a user changes their password on a different device. The cached credentials on the current device become outdated and SSO fails. Edge detects this failure and shows a re-authentication popup that prompts the user to update their cached credentials on the current device.

- **Updated profile management and customization controls.** Enhancing the profile management and customization experience through surfaced profile controls and an expanded range of default avatars. With these updates, users can effortlessly tailor their profiles to their preferences and select from a broader collection of profile avatars.

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

<!-- Version 123.0.2420.65: March 27, 2024 to Version 122.0.2365.8: February 1, 2024 -->
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
