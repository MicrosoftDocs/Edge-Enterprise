---
title: "Archived release notes for Microsoft Edge Beta Channel"
ms.author: leahtu
author: dan-wesley
manager: archandr
ms.date: 10/24/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Archived release notes for Microsoft Edge Beta Channel"
---

# Archived release notes for Microsoft Edge Beta Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Beta Channel. To understand Microsoft Edge channels, see the [Overview of the Microsoft Edge channels](microsoft-edge-channels.md). All the security updates are listed [here](microsoft-edge-relnotes-security.md).

<!-- Version 128.0.2739.42: August 22, 2024 to Version 128.0.2739.5: August 1, 2024 -->
## Version 128.0.2739.42: August 22, 2024

Fixed various bugs and performance issues, feature updates.

### Feature updates

- **Edge Bar improvements.** Microsoft Edge Bar, the detachable version of the Edge sidebar in Windows 10, has a changed entry point from the gear icon at the bottom of the Edge sidebar's fly out menu to the *edge://settings/sidebar* page.  

  For Windows 11 and Windows 10 users, clicking the gear icon now automatically opens the *edge://settings/sidebar* page.

  Also, the ability for Edge Bar to start automatically when starting a Windows 10 device is enabled again, the Close "X" icon was moved below the ellipsis menu at the bottom right corner of Edge Bar, and Copilot in Edge remains within the browser not in Edge Bar. **Note:** These features are a controlled feature rollout. If you don't see these features, check back as we continue our rollout.

  Disabling Edge Bar through the [StandaloneHubsSidebarEnabled](/deployedge/microsoft-edge-policies#standalonehubssidebarenabled) policy continues to work, there's a fix to make the UI and briefcase icon appear on the *edge://settings/sidebar* page coming soon.

## Version 128.0.2739.33: August 19, 2024

Fixed various bugs and performance issues.

### Fixes

- Fixed an issue that caused high CPU usage of renderer processes when running Selenium tests and calling `driver.quit()` to end the testing session.

## Version 128.0.2739.22: August 12, 2024

Fixed various bugs and performance issues.

## Version 128.0.2739.9: August 5, 2024

Fixed various bugs and performance issues.

## Version 128.0.2739.5: August 1, 2024

Fixed various bugs and performance issues, feature updates, and policy updates.

### Dev Channel updates

The following Dev channel updates preceded this Beta channel release. These notes provide detailed information about the changes in each release.

- [Dev Channel update to 128.0.2661.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-128-0-2661-0-is-live/m-p/4176024)
- [Dev Channel update to 128.0.2677.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-128-0-2677-1-is-live/m-p/4182622)
- [Dev Channel update to 128.0.2690.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-128-0-2690-1-is-live/m-p/4188392)
- [Dev Channel update to 128.0.2708.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-128-0-2708-0-is-live/m-p/4194430)
- [Dev Channel update to 128.0.2730.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-128-0-2730-0-is-live/m-p/4200632)

### Feature updates

- **SSE3 Requirement.** Microsoft Edge stopped supporting CPUs that lack SSE3. Devices with such CPUs won't receive any more updates. For more information, see [Microsoft Edge Supported Operating Systems](/deployedge/microsoft-edge-supported-operating-systems).

- **Copilot browser Context Policies.** The [DiscoverPageContextEnabled](/deployedge/microsoft-edge-policies#discoverpagecontextenabled) policy is obsoleted in Edge version 128 and doesn't work after Microsoft Edge 127.

  To summarize and answer questions based on browser context in Microsoft Edge, Copilot needs to be able to access the browser context. We're providing two new policies to offer more flexibility for admins to customize Edge browser context access across Copilot chats in Edge sidebar.

  - [CopilotPageContext](/deployedge/microsoft-edge-policies#copilotpagecontext) - Control Copilot access to browser context for Microsoft Entra ID profiles.
  - [CopilotCDPPageContext](/deployedge/microsoft-edge-policies#copilotcdppagecontext) - Control Copilot with Commercial Data Protection access to browser context for Microsoft Entra ID profiles.

- **Deprecation of the followable web feature.** To improve end user experience, the followable web feature is deprecated. The [EdgeFollowEnabled](/deployedge/microsoft-edge-policies#edgefollowenabled) policy is also obsolete.

- **EnforceLocalAnchorConstraintsEnabled policy obsoletion.** The [EnforceLocalAnchorConstraintsEnabled](/deployedge/microsoft-edge-policies#enforcelocalanchorconstraintsenabled) policy was previously deprecated and is now obsolete in Edge version 128. Since Microsoft Edge 112, constraints in certificates loaded from the platform certificate store are enforced. The [EnforceLocalAnchorConstraintsEnabled](/deployedge/microsoft-edge-policies#enforcelocalanchorconstraintsenabled) policy existed as a temporary opt-out in case an enterprise encountered issues with the constraints encoded in their private roots.

- **New Policy for Insecure Downloads over HTTP.** Users that download potentially dangerous content on HTTP sites will receive a UI warning in a future Microsoft Edge version. To prepare for this change, the [ShowDownloadsInsecureWarningsEnabled](/deployedge/microsoft-edge-policies#showdownloadsinsecurewarningsenabled) policy is now available for admins to enable or disable the warnings related to insecure downloads.

- **Get the latest updates effortlessly with instant update.** Instant update in Microsoft Edge ensures you get the latest browser updates automatically, when you step away from your computer. So you can just keep browsing, knowing you already have the latest updates to keep you safe online. For more information, see [Get instant updates in Microsoft Edge - Microsoft Support](https://support.microsoft.com/en-us/microsoft-edge/get-instant-updates-in-microsoft-edge-4820adad-dd32-470c-9bd9-dba1de71a7f1). **Note:** This feature is a controlled feature rollout to consumer customers. A release to enterprise users is TBD. If you don't see this feature, check back as we continue our rollout.

### Policy updates

#### New policies

- [ApplicationBoundEncryptionEnabled](/deployedge/microsoft-edge-policies#applicationboundencryptionenabled) - Enable Application Bound Encryption
- [DynamicCodeSettings](/deployedge/microsoft-edge-policies#dynamiccodesettings) - Dynamic Code Settings
- [KeyboardFocusableScrollersEnabled](/deployedge/microsoft-edge-policies#keyboardfocusablescrollersenabled) - Enable keyboard focusable scrollers
- [ShowDownloadsInsecureWarningsEnabled](/deployedge/microsoft-edge-policies#showdownloadsinsecurewarningsenabled) - Enable insecure download warnings

#### Obsoleted policies

- [DiscoverPageContextEnabled](/deployedge/microsoft-edge-policies#discoverpagecontextenabled) - Enable Discover access to page contents for AAD profiles (obsolete)
- [EnforceLocalAnchorConstraintsEnabled](/deployedge/microsoft-edge-policies#enforcelocalanchorconstraintsenabled) Determines whether the built-in certificate verifier enforces constraints encoded into trust anchors loaded from the platform trust store (deprecated)

<!-- Version 127.0.2651.74: July 25, 2024 to Version 127.0.2651.8: June 21, 2024 -->

## Version 127.0.2651.74: July 25, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.72: July 24, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.61: July 19, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.49: July 12, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.45: July 10, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.31: July 2, 2024

Fixed various bugs and performance issues.

## Version 127.0.2651.15: June 25, 2024

Fixed various bugs and performance issues.

### Fixes

- **Updated HttpAllowlist policy.** Automatic HTTPS should now respect the [HttpAllowlist](/deployedge/microsoft-edge-policies#httpallowlist) policy, which provides a list of hostnames that HTTP should be permitted on.
 
## Version 127.0.2651.8: June 21, 2024

Fixed various bugs and performance issues, feature updates, and policy updates.

### Dev Channel updates

The following Dev channel updates preceded this Beta channel release. These notes provide detailed information about the changes in each release.

- [Dev Channel update to 127.0.2610.3 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-127-0-2610-3-is-live/m-p/4156565)
- [Dev Channel update to 127.0.2638.2 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-127-0-2638-2-is-live/m-p/4168541)

**Announcement**

- **SSE3 Requirement.**  Microsoft Edge will stop supporting CPUs that lack SSE3 in Microsoft Edge 128. Devices with such CPUs won't receive any more updates. For more information, see [Microsoft Edge Supported Operating Systems](/deployedge/microsoft-edge-supported-operating-systems).

- **Token Binding.** Token Binding uses cryptographic certificates on both ends of the TLS connection in an attempt to close the security gap of bearer tokens, which might be lost or stolen. We're planning to deprecate Token Binding in Microsoft Edge version 130. The [AllowTokenBindingForUrls](/deployedge/microsoft-edge-policies#allowtokenbindingforurls) policy is deprecated and will be obsoleted in Microsoft Edge version 130.  

### Feature updates

- **Removal of mutation events.** Support for mutation events was removed. The [MutationObserver](https://developer.mozilla.org/en-US/docs/Web/API/MutationObserver) API can be used instead. Administrators can use the [MutationEventsEnabled](/deployedge/microsoft-edge-policies#mutationeventsenabled) policy as a temporary workaround. Enterprises should still work to remove their dependencies on these mutation events. For more information, see [Intent to Ship: Deprecate Mutation Events (google.com)](https://groups.google.com/a/chromium.org/g/blink-dev/c/jBEISy1p1XU).  

- **Gift Card Redemption History in the Hub.** Users with an MSA or Microsoft Entra ID Linked Account can view and utilize information from gift card redemptions through Pay with Rewards or the Rewards Dashboard. Once a user successfully redeems a gift card with Pay with Rewards, information relating to their gift card (date, card number/pin, redemption status) redemption is added to a Redemption History. This information is located in the Wallet hub. Admins can control availability of this feature using the [EdgeWalletCheckoutEnabled](/deployedge/microsoft-edge-policies#edgewalletcheckoutenabled) policy. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Password Monitor policy update.** When the [PasswordMonitorAllowed](/deployedge/microsoft-edge-policies#passwordmonitorallowed) policy is enabled as mandatory, users won't see the consent screen to turn on the feature. Also, when it's set to Mandatory enabled, the UI in Settings will be disabled but remain in the 'On' state, and a briefcase icon will be made visible next to it with this description displayed on hover - "This setting is managed by your organization."

### Policy updates

#### Deprecated policies

- [SignInCtaOnNtpEnabled](/deployedge/microsoft-edge-policies#signinctaonntpenabled) - Enable sign in click to action dialog (deprecated).  

#### Obsoleted policies

- [ImmersiveReaderPictureDictionaryEnabled](/deployedge/microsoft-edge-policies#immersivereaderpicturedictionaryenabled) - Enable Picture Dictionary feature within Immersive Reader in Microsoft Edge (obsolete).

<!-- Version 126.0.2592.68: June 20, 2024 to Version 126.0.2592.13: May 23, 2024 -->

## Version 126.0.2592.68: June 20, 2024

Fixed various bugs and performance issues.

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

- **AI theme generator.** Microsoft Edge includes an AI theme generator that allows users to input a text string and generate a series of images to preview as browser themes. Applying the theme includes setting the generated image on the Edge new tab page and applying the image's dominant color to the browser frame. Admins can control availability to this feature using the [AIGenThemesEnabled](/deployedge/microsoft-edge-policies#enables-dall-e-themes-generation) policy.  **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Security protection controls in the Microsoft Edge management service.**  The Microsoft Edge management service will provide admins with a dedicated experience to manage specific settings that help improve the security posture of their managed browser instances. **Note:** This experience is in public preview and can be accessed by opting in to targeted release in the Microsoft 365 admin center.

- **Copilot summarization notification.**  The feature displays an Omnibox notification when users enter into a reading mode eligible page in Edge and offers them the option to open Copilot in the sidebar to generate a summary of the content.  **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

### Policy updates
 
#### Obsoleted policies

-    [MathSolverEnabled](/deployedge/microsoft-edge-policies#mathsolverenabled) - Let users snip a Math problem and get the solution with a step-by-step explanation in Microsoft Edge (obsolete)
-    [ImmersiveReaderGrammarToolsEnabled](/deployedge/microsoft-edge-policies#immersivereadergrammartoolsenabled) - Enable Grammar Tools feature within Immersive Reader in Microsoft Edge (obsolete)

<!-- Version 125.0.2535.51: May 17, 2024 to Version 125.0.2535.13: April 29, 2024 -->
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

- [ZstdContentEncodingEnabled](/deployedge/microsoft-edge-policies#zstdcontentencodingenabled) - Enable zstd content encoding support
- [QRCodeGeneratorEnabled](/deployedge/microsoft-edge-policies#qrcodegeneratorenabled) - Enable QR Code Generators

<!-- Version 124.0.2478.67: April 26, 2024 to Version 124.0.2478.10: March 28, 2024 -->

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

- **Cross-device Search Query History suggestions.** The existing Search Query suggestions are enhanced with cross-device query history in both Recent Searches and browser searches for enterprise users who enable Microsoft Edge Sync across devices/browsers. From now on, Microsoft Edge gives you the relevant query history suggestions that you used for previous searches, regardless of where you did it. You can always trust Microsoft Edge to help you quickly refind the information that you accessed before.

- **Enterprise secure AI controls in the Microsoft Edge management service.** The Microsoft Edge management service now provides a new dedicated space for admins to manage all AI-related policies in the Microsoft Edge browser. This control helps enhance security and productivity for managed users and devices.

## Version 124.0.2478.10: March 28, 2024

Fixed various bugs and performance issues, updated features, and policies.

### Dev Channel updates

The following Dev channel updates preceded this Beta channel release. The following Dev notes provide detailed information about the changes in each release.

- [Dev Channel update to 124.0.2438.2 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-124-0-2438-2-is-live/m-p/4079136)
- [Dev Channel update to 124.0.2450.2 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-124-0-2450-2-is-live/m-p/4085888)
- [Dev Channel update to 124.0.2464.2 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-124-0-2464-2-is-live/m-p/4092459)
- [Dev Channel update to 124.0.2478.6 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-124-0-2478-6-is-live/m-p/4097816)

### Feature updates

- **Email notifications for extension requests in the Microsoft Edge management service.** The Microsoft Edge management service provides admins with the ability to receive email notifications for extensions that their users requested. These notifications help inform them promptly of any new feedback. **Note:** This experience is in public preview and can be accessed by opting in to targeted release in the Microsoft 365 admin center.

- **Updated default profile pill for EDU users in Edge for Business.** To improve the applicability of the current Edge for Business default visuals, users signed in with an EDU account will see the default profile pill label updated to "School".

- **Desktop Shortcut for New Enterprise Devices.** New Microsoft Enterprise devices running through Windows Out of Box Experience (OOBE) for the first time will see a Microsoft Edge desktop shortcut automatically created. This desktop shortcut provides users with an alternative way to access their Microsoft Edge browser without needing to manually pin and configure their set-up.

- **Updated profile options in new profile experience.** Many users unintentionally create empty profiles, cluttering their workspace and impeding their browsing experience. To reduce clutter and the likelihood of profile churn, updated First Run Experience (FRE) string options encourage users to sign-in and meaningfully create profiles for an improved browsing experience, or easily cancel unintentional creation. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Copilot Page Context Policies.** To summarize and answer questions based on page context in Microsoft Edge, Copilot needs to be able to access the page content. We're providing two new policies to offer more flexibility for admins to customize Edge page context access across Copilot chats in Edge sidebar.
   - [CopilotPageContext](/deployedge/microsoft-edge-policies#copilotpagecontext) - Control Copilot access to browser context for Microsoft Entra ID profiles
   - [CopilotCDPPageContext](/deployedge/microsoft-edge-policies#copilotcdppagecontext) - Control Copilot with Commercial Data Protection access to browser context for Microsoft Entra ID profiles
   - The [DiscoverPageContextEnabled](/deployedge/microsoft-edge-policies#discoverpagecontextenabled) policy is deprecated in Edge version 124 and is planned for obsoletion in Microsoft Edge version 127.

- **Inline Compose.** This feature allows users to rewrite text using Copilot. Users can highlight text they'd like to improve and use the Rewrite tool to iterate with different lengths, formats, and tones. Administrators can control availability using the [ComposeInlineEnabled](/deployedge/microsoft-edge-policies#composeinlineenabled) policy.

- **Updates to Settings pages on privacy, security, search, & services.**  To improve ease of use, we're updating Edge settings page into two sections: "Privacy and Security" and "Search and Services." This streamlined approach should enable users to find the settings they're interested in more easily. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Removal of Web SQL.** Web SQL support is fully removed. In prior releases, Web SQL support was disabled by default but could be re-enabled via the [WebSQLAccess policy](/deployedge/microsoft-edge-policies?branch=pr-en-us-4033#websqlaccess). After this change, there's no longer any mechanism to enable Web SQL support. This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, see [Intent to Deprecate and Remove Web SQL](https://groups.google.com/a/chromium.org/g/blink-dev/c/fWYb6evVA-w/m/pziWcvboAgAJ).

- **Sidebar Tools App - SpeedTest.** Adding a SpeedTest answer by default to the Tools app in the Microsoft Edge sidebar. For more information, see [Manage the sidebar in Microsoft Edge](/deployedge/microsoft-edge-sidebar).

- **Updated Edge Profile account re-authentication popup when Browser to Web Single-Sign-On (SSO) fails.** Microsoft Edge provides a browser to Web single sign-on (SSO) capability that lets a user sign in to their Edge Profile with a web account first and then automatically sign them into Microsoft first party websites.

  This reauthentication is done by saving cached credentials. This approach works until there's an authentication challenge to the cached credentials. A typical scenario is when a user changes their password on a different device. The cached credentials on the current device become outdated and SSO fails. Edge detects this failure and shows a reauthentication popup that asks the user to update their cached credentials on the current device.

- **Updated profile management and customization controls.** Enhancing the profile management and customization experience through surfaced profile controls and an expanded range of default avatars. With these updates, users can effortlessly tailor their profiles to their preferences and select from a broader collection of profile avatars.

- **Updated UX for Microsoft Defender for Endpoint blocks.** Microsoft Edge now provides a different blocking experience for Microsoft Defender for Endpoint based blocks (Web Content Filtering and Custom Indicators). For more information, see [Web protection](/microsoft-365/security/defender-endpoint/web-protection-overview?view=o365-worldwide&preserve-view=true).

### Policy updates

#### New policies

- [CopilotCDPPageContext](/deployedge/microsoft-edge-policies#copilotcdppagecontext) - Control Copilot with Commercial Data Protection access to browser context for Microsoft Entra ID profiles
- [CopilotPageContext](/deployedge/microsoft-edge-policies#copilotpagecontext) - Control Copilot access to browser context for Microsoft Entra ID profiles
- [MutationEventsEnabled](/deployedge/microsoft-edge-policies#mutationeventsenabled) - Enable deprecated/removed Mutation Events

#### Deprecated policies

- [DiscoverPageContextEnabled](/deployedge/microsoft-edge-policies#discoverpagecontextenabled) - Enable Discover access to page contents for Microsoft Entra ID profiles (deprecated)

#### Obsoleted policies

- [ThrottleNonVisibleCrossOriginIframesAllowed](/deployedge/microsoft-edge-policies#throttlenonvisiblecrossoriginiframesallowed) - Allows enabling throttling of nonvisible, cross-origin iframes (obsolete)
- [WebSQLAccess](/deployedge/microsoft-edge-policies#websqlaccess) - Force WebSQL to be enabled (obsolete)


<!-- Version 123.0.2420.65: March 27, 2024 to Version 122.0.2365.8: February 1, 2024 -->

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

- **Customize organization branding using the Microsoft Edge management service.** Admins can customize their organization's branding assets onto Edge for Business through the Microsoft Edge management service. This branding can help users signed in with a Microsoft Entra ID (formerly known as Azure Active Directory) more easily differentiate between multiple profiles and browser windows. This is done by visual cues on the profile pill, profile flyout, and Microsoft Edge for Business taskbar icon.

  The Microsoft Edge management service gives admins an enhanced experience to configure, preview, and customize how Microsoft Edge for Business shows the following organization brand assets:

  - Organization name
  - Accent color
  - Organization logo
  - Microsoft Edge for Business taskbar icon overlay

  For more information, see [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business).

- **Automatic profile switching controls for Microsoft Edge for Business in the Microsoft Edge management service.** The Microsoft Edge management service provides admins with the ability to configure settings for automatic profile switching in the Microsoft Edge browser. This feature can help enforce context separation between their end users' work and personal browsing. **Note:** This profile experience is in public preview.

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

<!-- Version 122.0.2365.59: February 27, 2024 to Version 122.0.2365.8: February 1, 2024 -->
## Version 122.0.2365.59: February 27, 2024

Fixed various bugs and performance issues.

## Version 122.0.2365.52: February 23, 2024

Fixed various bugs and performance issues.

## Version 122.0.2365.50: February 22, 2024

Fixed various bugs and performance issues.

### Fixes

- Resolved an issue when printing certain PDF files in landscape mode with the "fit to printable area" option, resulted in incorrect printing.

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

- **Configure recommended policies in the Microsoft Edge management service.** The Microsoft Edge management service provides admins with controls to configure recommended policies. This setting gives end users permission to override the configured policy.

### Policy updates

#### New policies

- [AIGenThemesEnabled](/deployedge/microsoft-edge-policies#aigenthemesenabled) Enables DALL-E themes generation
- [EnhanceSecurityModeAllowUserBypass](/deployedge/microsoft-edge-policies#enhancesecuritymodeallowuserbypass) Allow users to bypass Enhanced Security Mode
- [SuperDragDropEnabled](/deployedge/microsoft-edge-policies#super-drag-drop-enabled) Super Drag Drop Enabled

#### Obsoleted policies

- [EdgeEnhanceImagesEnabled](/deployedge/microsoft-edge-policies#edgeenhanceimagesenabled) Enhance images enabled 

<!-- Version 121.0.2277.83: January 25, 2024, 2023 to Version 121.0.2277.4: December 15, 2023 -->
## Version 121.0.2277.83: January 25, 2024

Fixed various bugs and performance issues.

## Version 121.0.2277.81: January 24, 2024

Fixed various bugs and performance issues.

## Version 121.0.2277.71: January 19, 2024

Fixed various bugs and performance issues.

## Version 121.0.2277.65: January 16, 2024

Fixed various bugs and performance issues.

## Version 121.0.2277.49: January 8, 2024

Fixed various bugs and performance issues.

### Feature update

- **Added support for AVIF and AV1 file formats.** Microsoft Edge now supports the AVIF and AV1 file formats, which offer better compression and higher quality images and videos. Users can enjoy faster loading times and better quality media on websites.  

## Version 121.0.2277.4: December 15, 2023

Fixed various bugs and performance issues.

### Feature updates

- **Enable organization branding in Edge for Business.**   Enable your organization's branding assets from Entra onto profile-related UI for profiles signed in with a Microsoft Entra ID (formerly known as Azure Active Directory) account. You can add your organization's details such as name to the profile pill, name and brand color to the profile flyout, and logo to overlay the Edge for Business taskbar icon. This branding can help users more easily differentiate between multiple profiles and browser windows.

   Admins can enable default organization branding through the following policies:

  - [OrganizationalBrandingOnWorkProfileUIEnabled](/deployedge/microsoft-edge-policies#organizationalbrandingonworkprofileuienabled
)
  - [OrganizationLogoOverlayOnAppIconEnabled](/deployedge/microsoft-edge-policies#organizationlogooverlayonappiconenabled)

  Admins need to have "company branding" assets configured in the Microsoft Entra admin center for branding assets to be applied to this feature.

  For more information, see [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business) and [Add company branding to your organization's sign-in page](/entra/fundamentals/how-to-customize-branding).

- **Microsoft Edge migrates the updates experience into Browser Essentials.** Getting alerts on available Edge Updates come from Browser Essentials instead of the Settings page for better visibility and experience. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **New Website Typo Protection policies.** The built-in Website Typo Protection warns users if it appears there's a mistyped popular domain name that could land users on a malicious webpage.  Administrators can control the availability and configure Website Typo Protection by using the [PreventTyposquattingPromptOverride](/deployedge/microsoft-edge-policies#preventtyposquattingpromptoverride) and [TyposquattingAllowListDomains](/deployedge/microsoft-edge-policies#typosquattingallowlistdomains) policies.

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


<!-- Version 120.0.2210.61: December 7, 2023 to Version 120.0.2210.7: November 13, 2023 -->

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

<!-- Version 119.0.2151.44: November 2, 2023, 2023 to Version 119.0.2151.24: October 23, 2023 -->
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
## Version 119.0.2151.12: October 17, 2023

Fixed various bugs and performance issues.

### Feature updates

- **Behavioral changes to the `beforeunload` event.** The behavior of the `beforeunload` event has changed. Calling `preventDefault` in a `beforeunload` event handler triggers a confirmation dialog. Setting `returnValue` to an empty string in a `beforeunload` event handler no longer triggers a confirmation dialog. This behavior takes effect starting in Microsoft Edge version 119. Administrators can temporarily opt out of this functionality by disabling the [BeforeunloadEventCancelByPreventDefaultEnabled](/deployedge/microsoft-edge-policies#beforeunloadeventcancelbypreventdefaultenabled) policy.

- **Split screen restore improvements.** Split screen allows you to simultaneously work on multiple tasks across two, side-by-side screens in one browsing tab to boost your productivity and multitask more efficiently. Now after the browser is restarted and the previous session is restored, the split tab will also be restored.

- **Additional capability to manage sidebar apps.** Administrators can utilize the "sidebar_auto_open_blocked" [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) policy field to control the auto-open behavior of sidebar apps.  For more information, see [Detailed guide to the ExtensionSettings](/deployedge/microsoft-edge-manage-extensions-ref-guide) policy.

- **Updates to Microsoft Edge enterprise sync settings page.** When the [ForceSyncTypes](/deployedge/microsoft-edge-policies#forcesynctypes) and [SyncTypesListDisabled](/deployedge/microsoft-edge-policies#synctypeslistdisabled) polices are used concurrently, the sync settings page (`edge://settings/profiles/sync`) accurately show the status for each data type.

### Policy updates

#### New policies

- [SwitchIntranetSitesToWorkProfile](/deployedge/microsoft-edge-policies#switchintranetsitestoworkprofile) - Switch intranet sites to a work profile
- [SwitchSitesOnIEModeSiteListToWorkProfile](/deployedge/microsoft-edge-policies#switchsitesoniemodesitelisttoworkprofile) - Switch sites on the IE mode site list to a work profile
- [OrganizationalBrandingOnWorkProfileUIEnabled](/deployedge/microsoft-edge-policies#organizationalbrandingonworkprofileuienabled) - Allow the use of your organization's branding assets from M365 on the profile-related UI of a work profile

## Version 118.0.2088.46: October 13, 2023

Fixed various bugs and performance issues.

## Version 118.0.2088.44: October 12, 2023

Fixed various bugs and performance issues.

## Version 118.0.2088.41: October 10, 2023

Fixed various bugs and performance issues.

## Version 118.0.2088.33: October 6, 2023

Fixed various bugs and performance issues.

## Version 118.0.2088.27: October 3, 2023

Fixed various bugs and performance issues.

## Version 118.0.2088.24: October 2, 2023

Fixed various bugs and performance issues.

## Version 118.0.2088.17: September 25, 2023

Fixed various bugs and performance issues.

<!-- Version 118.0.2088.11: September 20, 2023 to Version 117.0.2045.12: August 29, 2023 -->
## Version 118.0.2088.11: September 20, 2023

Fixed various bugs and performance issues.

### Feature updates

- **Microsoft Edge for Business Banner.**  Microsoft Edge for Business is a dedicated Microsoft Edge experience built for work that enables admins in organizations to give their users a productive and secure work browser across managed and unmanaged devices. The in-product Microsoft Edge for Business banner is being deprecated and will no longer be visible.

- **Find on page.** Searching for a word or phrase on a webpage is easier with the new smart find update to Find on page. For more information, see
[Find on page](https://www.microsoft.com/edge/features/find-on-page?form=MT00D8). Now when you search with Find on page, we suggest related matches and synonyms making it effortless to find what you're looking for, even if you misspell a word in your search query. When you search, select the suggested word to quickly locate the desired word or phrase on the page. Data is sent to Microsoft for processing.  For more information, see [Microsoft Edge's Privacy Whitepaper](/microsoft-edge/privacy-whitepaper/). Administrators can control the availability using the [RelatedMatchesCloudServiceEnabled](/deployedge/microsoft-edge-policies#relatedmatchescloudserviceenabled) policy.

- **New SmartScreen policy.**  The [ExemptSmartScreenDownloadWarnings](/deployedge/microsoft-edge-policies#exemptsmartscreendownloadwarnings) policy lets administrators create a dictionary of file type extensions with a corresponding list of domains that are exempted from SmartScreen AppRep warnings.  Files with file type extensions specified for domains identified by this policy are still subject to file type extension-based security warnings and mixed-content download warnings.

- **New Microsoft Edge Update policies.** The **MeteredUpdatesDefault** and **MeteredUpdates** policies allows administrators to control the "Download Updates over metered connections" setting (`edge://settings/help`). The **MeteredUpdatesDefault** applies to all apps and **MeteredUpdates** applies to targeted apps. When a policy is configured to Allow, updates occur on a metered connection, such as cellular connections or others where data usage is controlled.

### Policy updates

#### New policies

- [CompressionDictionaryTransportEnabled](/deployedge/microsoft-edge-policies#compressiondictionarytransportenabled) -Enable compression dictionary transport support
- [DataUrlInSvgUseEnabled](/deployedge/microsoft-edge-policies#dataurlinsvguseenabled) - Data URL support for SVGUseElement
- [ExemptSmartScreenDownloadWarnings](/deployedge/microsoft-edge-policies#exemptsmartscreendownloadwarnings) - Disable SmartScreen AppRep based warnings for specified file types on specified domains
- [ForcePermissionPolicyUnloadDefaultEnabled](/deployedge/microsoft-edge-policies#forcepermissionpolicyunloaddefaultenabled) - Controls whether unload event handlers can be disabled
- [PictureInPictureOverlayEnabled](/deployedge/microsoft-edge-policies#pictureinpictureoverlayenabled) - Enable Picture in Picture overlay feature on supported webpages in Microsoft Edge

## Version 117.0.2045.31: September 15, 2023

Fixed various bugs and performance issues.

## Version 117.0.2045.30: September 14, 2023

Fixed various bugs and performance issues.

## Version 117.0.2045.27: September 12, 2023

Fixed various bugs and performance issues.

## Version 117.0.2045.21: September 6, 2023

Fixed various bugs and performance issues.

## Version 117.0.2045.12: August 29, 2023

Fixed various bugs and performance issues.

### Announcement: Deprecating the unload event

The Google Chrome team plans to deprecate the unload event starting in Chrome version 117. The deprecation is done by gradually changing the default so unload handlers stop firing on pages unless a page explicitly opts in to re-enable them. For more information, see [Deprecating the unload event - Chrome Developers](https://developer.chrome.com/blog/deprecating-unload/), and [Google Groups - Conversations](https://groups.google.com/a/chromium.org/g/blink-dev/c/dvusqw9-IhI/m/SBkm_u1RAQAJ).

While we haven't finalized the deprecation schedule, we anticipate that Microsoft Edge  follows Chrome's schedule with a possible delay of a release or two. If you're interested in testing with Microsoft Edge starting in version 118, the **ForcePermissionPolicyUnloadDefaultEnabled** policy is available or you can use the instructions documented at [Disable unload handlers by default and add Permissions-Policy to opt-in to enabling them](https://github.com/fergald/docs/blob/master/explainers/permissions-policy-deprecate-unload.md#disable-unload-handlers-by-default-and-add-permissions-policy-to-opt-in-to-enabling-them).

WebView2 supports both the permissions policy and the enterprise policy but won't be impacted by the gradual rollout in Microsoft Edge. We expect WebView2 to switch defaults when the rollout reaches 100% of page loads.

<!-- Version 117.0.2045.9: August 25, 2023 to Version 116.0.1938.36: July 31, 2023 -->
## Version 117.0.2045.9: August 25, 2023

Fixed various bugs and performance issues.

### Feature updates

- **Microsoft Edge for Business update.** Microsoft Edge for Business is a dedicated Microsoft Edge experience built for work that enables admins in organizations to give their users a productive and secure work browser across managed and unmanaged devices. The Automatic Switching mechanism is designed to keep work and personal browsing separate for the end users. This mechanism currently switches users from personal to work browsing on applicable logins. The new update automatically starts switching users from work to personal browsing on applicable logins. For more information, see [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business).

- **E-tree in Wallet.** Users signed into Microsoft Edge with a personal Microsoft Account (MSA) can grow a virtual seed into a tree with Wallet. After it finishes growing, a real mangrove is planted.  Administrators can control the availability using the [EdgeWalletEtreeEnabled](/deployedge/microsoft-edge-policies#edge-wallet-e-tree-enabled) policy. Note: This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Deprecation of features.** To improve end user experience and simplify the More tools menu, the following features are being deprecated: Math Solver, Picture Dictionary, Citations, Grammar Tools, and Kids Mode.

- **Deprecation of Web Select.** To improve end user experience, this feature is being deprecated and will no longer be an option under Web Capture or via keyboard shortcut.

### Policy updates

#### New policies

- [AllowSystemNotifications](/deployedge/microsoft-edge-policies#allowsystemnotifications) - Allows system notifications
- [EdgeWalletEtreeEnabled](/deployedge/microsoft-edge-policies#edgewalletetreeenabled) - Edge Wallet E-Tree Enabled
- [GamerModeEnabled](/deployedge/microsoft-edge-policies#gamermodeenabled) - Enable Gamer Mode
- [SearchbarAllowed](/deployedge/microsoft-edge-policies#searchbarallowed) - Enable the Search bar
- [SearchbarIsEnabledOnStartup](/deployedge/microsoft-edge-policies#searchbarisenabledonstartup) -Allow the Search bar at Windows startup
- [ShowHistoryThumbnails](/deployedge/microsoft-edge-policies#showhistorythumbnails) - Show thumbnail images for browsing history
- [UploadFromPhoneEnabled](/deployedge/microsoft-edge-policies#uploadfromphoneenabled) - Enable upload files from phone in Microsoft Edge desktop

#### Obsoleted policy

- [WebSelectEnabled](/deployedge/microsoft-edge-policies#webselectenabled) - Web Select Enabled

## Version 116.0.1938.54: August 18, 2023

Fixed various bugs and performance issues.

## Version 116.0.1938.51: August 16, 2023

Fixed various bugs and performance issues.

## Version 116.0.1938.43: August 9, 2023

Fixed various bugs and performance issues.

## Version 116.0.1938.36: July 31, 2023

Fixed various bugs and performance issues.

<!-- Version 116.0.1938.29: July 24, 2023 to Version 115.0.1901.9: June 15, 2023 -->
## Version 116.0.1938.29: July 24, 2023

Fixed various bugs and performance issues.

### Feature update

- **Microsoft Edge for Business.** In addition to rich set of enterprise controls, security, and productivity features that you're already familiar with, Microsoft Edge for Business offers new refreshed look and feel, automatic switching to keep your work and personal browsing separate including fixes from private preview feedback, lightly managed Enterprise Personal Browser (MSA profile), and support for Unmanaged BYOPC. Microsoft Edge for Business is now turned on by default.  For more information, see [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business).

- **Locked Tabs in Edge Workspaces.** This feature lets you keep tabs where you put them in an Edge workspace. A locked tab can't be closed, dragged or otherwise moved out of a workspace window. To lock a tab, right-click the tab and choose "Lock Tab" from the context menu.  Click the lock icon on a tab to unlock it. Only the workspace creator and the user who locked the tab are permitted to unlock the tab. For more information, see [Microsoft Edge Workspaces](/deployedge/microsoft-edge-workspaces). **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **New Microsoft Edge PDF experience policy for WebView2.** The [NewPDFReaderWebView2List](/deployedge/microsoft-edge-webview-policies#newpdfreaderwebview2list) policy configures WebView2 applications to launch the new version of the PDF reader that's powered by Adobe Acrobat's PDF rendering engine.  The new PDF reader ensures that there's no loss of functionality and delivers an enhanced PDF experience. This experience includes richer rendering, improved performance, strong security for PDF file handling, and greater accessibility. Administrators can use the [NewPDFReaderWebView2List](/deployedge/microsoft-edge-webview-policies#newpdfreaderwebview2list) policy or WebView2 developers can explicitly enable the **msPdfSharedLibrary** experimental flag in code to use WebView2 with PDF powered by Adobe PDF Engine. For more information about the Adobe and Microsoft collaboration, see [Microsoft Edge and Adobe partner to improve the PDF experience](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/microsoft-edge-and-adobe-partner-to-improve-the-pdf-experience/ba-p/3733481).

### Policy updates

#### New policies

[ThrottleNonVisibleCrossOriginIframesAllowed](/deployedge/microsoft-edge-policies#throttlenonvisiblecrossoriginiframesallowed) - Allows enabling throttling of non-visible, cross-origin iframes

## Version 115.0.1901.183: July 21, 2023

Fixed various bugs and performance issues.

## Version 115.0.1901.181: July 19, 2023

Fixed various bugs and performance issues.

## Version 115.0.1901.178: July 17, 2023

Fixed various bugs and performance issues.

## Version 115.0.1901.175: July 14, 2023

Fixed various bugs and performance issues.

## Version 115.0.1901.170: July 11, 2023

Fixed various bugs and performance issues.

## Version 115.0.1901.165: July 6, 2023

Fixed various bugs and performance issues.

## Version 115.0.1901.157: June 28, 2023

Fixed various bugs and performance issues.

## Version 115.0.1901.151: June 23, 2023

Fixed various bugs and performance issues.

### Feature update

- **Autofill Autocomplete.** This feature helps you fill form fields faster on the web. When you start typing in a form field, Microsoft Edge suggests possible in-line completions when there's an exact match with your saved data in the browser. For example, if you type the first few characters of your address, autocomplete will suggest the rest of address - you can choose the autocomplete suggestion or continue typing as usual. Autofill options can be found in Settings (`edge://settings/personalinfo`).  **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

## Version 115.0.1901.14: June 19, 2023

Fixed various bugs and performance issues.

### Feature update

- **Microsoft Edge for Business.**  In addition to rich set of enterprise controls, security, and productivity features that you're already familiar with, Microsoft Edge for Business offers new refreshed look and feel, automatic switching to keep your work and personal browsing separate, lightly managed Enterprise Personal Browser (MSA profile), support for Unmanaged BYOPC, and Company Branding (coming soon).  

  To enable preview on a device, enter the following URLs in the Microsoft Edge address bar and set each flag to "Enabled".

  - `edge://flags/#edge-project-kodiak`

  - `edge://flags/#edge-project-kodiak-look-and-feel`

  - `edge://flags/#edge-project-kodiak-policy-filter`

  - `edge://flags/#edge-automatic-profile-switching`

  For more information, see [Microsoft Edge for Business (Early Preview)](/deployedge/microsoft-edge-for-business).

## Version 115.0.1901.9: June 15, 2023

Fixed various bugs and performance issues.
<!-- from Version 115.0.1901.7: June 13, 2023 to Version 114.0.1823.18: May 15, 2023 -->
## Version 115.0.1901.7: June 13, 2023

Fixed various bugs and performance issues.

### Feature update

- **Enhanced security mode improvements.** Enhanced security mode provides an extra layer of protection when browsing the web and visiting less familiar sites. Enhanced security mode is turned on by default to Balanced mode for x64 Windows, x64 macOS, x64 Linux, and ARM64 systems. **Note:** This feature is a controlled feature rollout in Microsoft Edge Beta 115. If you don't see this feature, check back as we continue our rollout.

  Also, administrators have two new policies to manage the Enhanced security mode user experience: **EnhanceSecurityModeIndicatorUIEnabled** and **EnhanceSecurityModeOptOutUXEnabled**. For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **Microsoft Edge management service.** Microsoft Edge management service is an area in the Microsoft 365 admin center where admins can manage the Microsoft Edge browser. It's a simple and easy-to-manage experience. Admins are able to configure all Microsoft Edge browser policies for their organization in a configuration profile and set-up the browser to use these settings. For more information, see [Microsoft Edge management service](/deployedge/microsoft-edge-management-service). **Note:** This experience is in public preview. We'll start rolling out this experience on June 9 and expect to finish the rollout by next week. You need to set up a Targeted release to opt in and view this experience in the M365 admin center.

### Policy updates

#### New policies

- [WalletDonationEnabled](/DeployEdge/microsoft-edge-policies#walletdonationenabled) - Wallet Donation Enabled
- [EnhanceSecurityModeIndicatorUIEnabled](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeindicatoruienabled) - Manage the indicator UI of the Enhanced Security Mode (ESM) feature in Microsoft Edge
- [EnhanceSecurityModeOptOutUXEnabled](/DeployEdge/microsoft-edge-policies#enhancesecuritymodeoptoutuxenabled) - Manage opt-out user experience for Enhanced Security Mode (ESM) in Microsoft Edge
- [ComposeInlineEnabled](/DeployEdge/microsoft-edge-policies#composeinlineenabled) - Compose is enabled for writing on the web
- [SearchForImageEnabled](/DeployEdge/microsoft-edge-policies#searchforimageenabled) - Search for image enabled

## Version 114.0.1823.43: June 8, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.41: June 6, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.37: June 2, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.35: May 31, 2023

Fixed various bugs and performance issues.

### Feature update

- **Microsoft Edge Sync Favorites Recovery.** The Microsoft Edge Sync Favorites Recovery feature lets sync users restore any favorites that they lost or deleted within the last 14 days. Users can access this feature from either the Microsoft Edge favorites hub or the *edge://favorites* page. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

## Version 114.0.1823.30: May 26, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.24: May 22, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.18: May 15, 2023

Fixed various bugs and performance issues.

<!-- Version 114.0.1823.11: May 9, 2023 to Version 113.0.1774.15: April 18, 2023 -->
## Version 114.0.1823.11: May 9, 2023

### Feature update

- **(Preview) Microsoft Edge Workspaces.** Edge Workspaces gives customers a way to organize their browsing tasks into dedicated windows. Edge Workspaces lets users share a set of browser tabs so working groups can view the same websites and latest working files in one place and stay on the same page. Each Edge Workspace contains its own sets of tabs and favorites, created and curated by the user and their collaborators. Edge Workspaces are automatically saved and kept up to date. For more information about this public preview, see [Microsoft Edge Workspaces](/deployedge/microsoft-edge-workspaces).

- **Option to attach the Edge sidebar to the Windows desktop.**  Users of the Microsoft Edge sidebar will be able to access their apps and sites directly from their Windows desktop. As an opt-in experience, users can attach the sidebar to their Windows desktop by clicking a "popout" icon near the base of the sidebar in the browser. This enables a side-by-side experience that works with any Windows app—including Microsoft Edge itself. Users enjoy streamlined access to the same set of powerful AI tools and web-based services, including Bing Chat, without launching a browser window, enhancing productivity regardless of where they are in Windows. Administrators can control the availability using the [StandaloneHubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#standalonehubssidebarenabled).

- **Enhanced security mode on by default.** Enhanced security mode provides an extra layer of protection when browsing the web and visiting less familiar sites. Enhanced security mode is turned on by default for x64 Windows, x64 macOS, x64 Linux, and ARM64 systems. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

### Policy updates

#### New policies

- [StandaloneHubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#standalonehubssidebarenabled) - Standalone Sidebar Enabled
- [ShowDownloadsToolbarButton](/DeployEdge/microsoft-edge-policies#showdownloadstoolbarbutton) - Show Downloads button on the toolbar

#### Obsoleted policy

- [MicrosoftRootStoreEnabled](/DeployEdge/microsoft-edge-policies#microsoftrootstoreenabled) - Determines whether the Microsoft Root Store and built-in certificate verifier is used to verify server certificates

#### Additional policy changes

- [EnhanceSecurityMode](/DeployEdge/microsoft-edge-policies#enhancesecuritymode) - BasicMode is deprecated
- [EdgeWorkspacesEnabled](/DeployEdge/microsoft-edge-policies#edgeworkspacesenabled) - If the policy isn't configured users are able to access the Microsoft Edge Workspaces feature

## Version 113.0.1774.35: May 5, 2023

Fixed various bugs and performance issues.

## Version 113.0.1774.32: May 4, 2023

### Feature update

- **Microsoft Edge PDF Share.** Users now have an easy option to share PDF documents as a link or attachment directly from the PDF toolbar.  **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

## Version 113.0.1774.27: May 1, 2023

Fixed various bugs and performance issues.

## Version 113.0.1774.23: April 25, 2023

Fixed various bugs and performance issues.

## Version 113.0.1774.15: April 18, 2023

Fixed various bugs and performance issues.
<!-- Version 113.0.1774.9: April 12, 2023 to Version 112.0.1722.15: March 21, 2023 -->
## Version 113.0.1774.9: April 12, 2023

### Feature update

- **Improvements to enhanced security mode.** Enhanced security mode provides an extra layer of protection when browsing the web and visiting unfamiliar sites.  Updates this release include a new flyout to improve user's experience when a site isn't working as expected. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Switch from Microsoft AutoUpdate to EdgeUpdater for macOS.** Microsoft Edge for macOS now uses a new updater named EdgeUpdater. This change only affects Microsoft Edge on macOS. If you use update preferences for Microsoft AutoUpdate to prevent browser updates, you'll need to transition to the new EdgeUpdater UpdateDefault policy before Microsoft Edge 113 to prevent future automatic updates.  For more information, see [Microsoft Edge for macOS switch from Microsoft AutoUpdate to EdgeUpdater](/deployedge/edge-learnmore-edgeupdater-for-macos).

### Policy updates

#### New policies

- [RestorePdfView](/DeployEdge/microsoft-edge-policies#restorepdfview) - Restore PDF view
- [ReadAloudEnabled](/DeployEdge/microsoft-edge-policies#readaloudenabled) - Enable Read Aloud feature in Microsoft Edge
- [ShowDownloadsToolbarButton](/DeployEdge/microsoft-edge-policies#showdownloadstoolbarbutton) - Show Downloads button on the toolbar
- [TabServicesEnabled](/DeployEdge/microsoft-edge-policies#tabservicesenabled) - Tab Services enabled

## Version 112.0.1722.39: April 10, 2023

Fixed various bugs and performances issues.

## Version 112.0.1722.33: April 5, 2023

Fixed various bugs and performance issues.

## Version 112.0.1722.31: April 3, 2023

Fixed various bugs and performance issues.

## Version 112.0.1722.23: March 28, 2023

Fixed various bugs and performance issues.

## Version 112.0.1722.15: March 21, 2023

Fixed various bugs and performance issues.

<!-- from Version 112.0.1722.11: March 17, 2023 to Version 111.0.1661.22: February 24, 2023 -->
## Version 112.0.1722.11: March 17, 2023

### Feature update

- **Enhanced security mode improvements.** Enhanced security mode now supports WebAssembly for ARM64. Cross-platform support is now available for x64 Windows, x64 macOS, x64 Linux and ARM64 systems.  For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **Added features for web app policy.** The [WebAppInstallForceList](/deployedge/microsoft-edge-policies#webappinstallforcelist) policy lets administrators configure a list of web apps that install silently, without user interaction, and which users can't uninstall or turn off.  This policy now supports `custom_name`, which permanently overrides the app name of installed apps and `custom_icon`, which permanently overrides the app icon of installed apps.

### Policy updates

#### New policies

- [CryptoWalletEnabled](/DeployEdge/microsoft-edge-policies#cryptowalletenabled) - Enable CryptoWallet feature

## Version 111.0.1661.43: March 16, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.41: March 13, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.39: March 10, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.38: March 9, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.37: March 8, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.34: March 6, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.30: March 3, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.27: March 2, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.24: February 27, 2023

Fixed various bugs and performance issues.

## Version 111.0.1661.22: February 24, 2023

Fixed various bugs and performance issues.

<!-- from Version 111.0.1661.15: February 16, 2023 to Version 110.0.1587.22: January 24, 2023 -->

## Version 111.0.1661.15: February 16, 2023

### Feature update

- **Enhanced security mode improvements.** Enhanced security mode now supports WebAssembly for macOS x64 and Linux x64. More cross-platform (ARM64) support is expected in the future. For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

- **New policy to clear IE mode data on browser exit.** The [InternetExplorerModeClearDataOnExitEnabled](/deployedge/microsoft-edge-policies#internetexplorermodecleardataonexitenabled) policy controls whether browsing history is deleted from Internet Explorer and Internet Explorer mode every time Microsoft Edge is closed. Users can also configure this setting in the 'Clear browsing data for Internet Explorer' option in the Privacy, search, and services menu of Settings (*edge://settings/privacy*).

### Policy updates

#### New policies

- [InternetExplorerModeClearDataOnExitEnabled](/DeployEdge/microsoft-edge-policies#internetexplorermodecleardataonexitenabled) - Clear history for IE and IE mode every time you exit
- [MouseGestureEnabled](/DeployEdge/microsoft-edge-policies#mousegestureenabled) - Mouse Gesture Enabled
- [PrintPreviewStickySettings](/DeployEdge/microsoft-edge-policies#printpreviewstickysettings) - Configure the sticky print preview settings

## Version 110.0.1587.40: February 8, 2023

Fixed various bugs and performance issues.

## Version 110.0.1587.35: February 3, 2023

Fixed various bugs and performance issues.

## Version 110.0.1587.30: January 30, 2023

Fixed various bugs and performance issues.

## Version 110.0.1587.22: January 24, 2023

Fixed various bugs and performance issues.

<!--- from Version 110.0.1587.17: January 20, 2023 to Version 109.0.1518.23: December 14, 2022 -->
## Version 110.0.1587.17: January 20, 2023

### Feature update

- **New Immersive Reader policies.**  Immersive Reader in Microsoft Edge simplifies web page layouts, removes clutter, and helps you customize your reading experience.  Administrators can use these new policies ([ImmersiveReaderGrammarToolsEnabled](/deployedge/microsoft-edge-policies#enable-grammar-tools-feature-within-immersive-reader-in-microsoft-edge) and [ImmersiveReaderPictureDictionaryEnabled](/deployedge/microsoft-edge-policies#enable-picture-dictionary-feature-within-immersive-reader-in-microsoft-edge)), to control the availability of Grammar Tools and Picture Dictionary features within Immersive Reader.

- **Enabling sync for Microsoft Entra ID signed in customers.**  Microsoft Edge sync roams data across all signed in instances of Microsoft Edge. This data includes favorites, passwords, browsing history, open tabs, settings, apps, collections, and extensions.  For Microsoft Entra users who have sync turned off, after the browser is launched they'll see a notification message and have sync turned on for all signed in instances of Microsoft Edge. This sync enablement includes other devices where they're signed in.  Additionally, if a user's other devices don't have history and open tabs sync on, those two toggles are turned on.  Organizations using the [SyncDisabled](/deployedge/microsoft-edge-policies#syncdisabled) policy aren't affected by this change.

- **In-browser JSON viewer.**  Improvements to how JSON files are displayed in the browser include a color-coded tree view with line numbers and the ability to collapse and expand the data.  This functionality triggers automatically when the browser navigates to a JSON file on the web or the user opens a local file.  Additional features and enhancements will roll out when they're available.  For more information and to provide feedback, visit [DevTools: In-browser JSON viewer](https://microsoftedge.github.io/DevTools/explainers/JSONViewer/explainer).

- **Split Screen.** This feature lets you browse faster with side by side tabs. Boost your productivity with two tabs side-by-side in one browser window. With split screen, you can multitask without losing focus.  Users can access Split Screen by clicking the toolbar icon or by selecting "Open link in split window" in the context menu.  **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

### Policy updates

#### New policies

- [ImmersiveReaderGrammarToolsEnabled](/DeployEdge/microsoft-edge-policies#immersivereadergrammartoolsenabled) - Enable Grammar Tools feature within Immersive Reader in Microsoft Edge
- [ImmersiveReaderPictureDictionaryEnabled](/DeployEdge/microsoft-edge-policies#immersivereaderpicturedictionaryenabled) - Enable Picture Dictionary feature within Immersive Reader in Microsoft Edge
- [PrintPreviewStickySettings](/DeployEdge/microsoft-edge-policies#printpreviewstickysettings) - Configure the sticky print preview settings
- [SearchInSidebarEnabled](/DeployEdge/microsoft-edge-policies#searchinsidebarenabled) - Search in Sidebar enabled
- [WorkspacesNavigationSettings](/DeployEdge/microsoft-edge-policies#workspacesnavigationsettings) - Configure navigation settings per groups of URLs in Microsoft Edge Workspaces

#### Obsoleted policies

- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) - Specifies whether the display-capture permissions-policy is checked or skipped
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains
- [SetTimeoutWithout1MsClampEnabled](/DeployEdge/microsoft-edge-policies#settimeoutwithout1msclampenabled) - Control JavaScript setTimeout() function minimum timeout
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) - Configure ShadowStack crash rollback behavior

## Version 109.0.1518.55: January 15, 2023

Fixed various bugs and performance issues.

## Version 109.0.1518.52: January 13, 2023

Fixed various bugs and performance issues.

## Version 109.0.1518.49: January 11, 2023

Fixed various bugs and performance issues.

## Version 109.0.1518.44: January 6, 2023

Fixed various bugs and performance issues.

## Version 109.0.1518.26: December 20, 2022

Fixed various bugs and performance issues.

## Version 109.0.1518.23: December 14, 2022

Fixed various bugs and performance issues.

## Version 109.0.1518.14: December 7, 2022

### Feature update

- **MSA-AAD Account Linking.** Microsoft is enabling users who have a personal Microsoft account (an MSA) and a Microsoft user account through their work or school (a Microsoft Entra account) to "link" the two types of accounts together. "Linked accounts" means that users are able to see some of the content from their personal account alongside the tailored content from their work or school account. They're also able to earn Microsoft Rewards points in their personal account from their activities while using their work or school account. More blended experiences might be made available.  For more information, see the [Account Linking FAQ](https://support.microsoft.com/en-us/account-billing/account-linking-faq-c66effb9-02e6-49c0-89e1-ae4d8644e6f7) and the [Account Linking IT Admins FAQ](https://support.microsoft.com/en-us/account-billing/account-linking-it-admins-faq-72f0dc4e-b632-439e-b90c-347043a7b75a). Tenant admins can learn how to control this feature in the Message Center section of the Microsoft 365 Admin Center. Also, this feature can be controlled by using the [LinkedAccountEnabled](/deployedge/microsoft-edge-policies#linkedaccountenabled) policy.

- **TLS server certificate verification changes.**  In Microsoft Edge version 110, the certificate trust list and the certificate verifier are decoupled from the host operating system's root store. Instead, the default certificate trust list and the certificate verifier are provided by and shipped with the browser.  The [MicrosoftRootStoreEnabled](/deployedge/microsoft-edge-policies#microsoftrootstoreenabled) policy is now available for testing to control when the built-in root store and certificate verifier are used.  Support for the policy is planned for removal in Microsoft Edge version 111.  For more information, see [Changes to Microsoft Edge browser TLS server certificate verification](/deployedge/microsoft-edge-security-cert-verification).  **Note:** This feature is a controlled feature rollout in Microsoft Edge version 109.  If you don't see this feature, check back as we continue our rollout.  

### Policy updates

#### New policies

- [WebHidAllowAllDevicesForUrls](/DeployEdge/microsoft-edge-policies#webhidallowalldevicesforurls) - Allow listed sites to connect to any HID device
- [WebHidAllowDevicesForUrls](/DeployEdge/microsoft-edge-policies#webhidallowdevicesforurls) - Allow listed sites connect to specific HID devices
- [WebHidAllowDevicesWithHidUsagesForUrls](/DeployEdge/microsoft-edge-policies#webhidallowdeviceswithhidusagesforurls) - Automatically grant permission to these sites to connect to HID devices containing top-level collections with the given HID usage
- [MicrosoftRootStoreEnabled](/DeployEdge/microsoft-edge-policies#microsoftrootstoreenabled) - Determines whether the Microsoft Root Store and built-in certificate verifier are used to verify server certificates
- [DefaultClipboardSetting](/DeployEdge/microsoft-edge-policies#defaultclipboardsetting) - Default clipboard site permission
- [ClipboardAllowedForUrls](/DeployEdge/microsoft-edge-policies#clipboardallowedforurls) - Allow clipboard use on specific sites
- [ClipboardBlockedForUrls](/DeployEdge/microsoft-edge-policies#clipboardblockedforurls) - Block clipboard use on specific sites
- [SearchFiltersEnabled](/DeployEdge/microsoft-edge-policies#searchfiltersenabled) - Search Filters Enabled

#### Deprecated policies

- [SetTimeoutWithout1MsClampEnabled](/DeployEdge/microsoft-edge-policies#settimeoutwithout1msclampenabled) - Control JavaScript setTimeout() function minimum timeout
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains

## Version 108.0.1462.42: December 5, 2022

Fixed various bugs and performance issues.

## Version 108.0.1462.38: December 2, 2022

Fixed various bugs and performance issues.

## Version 108.0.1462.35: November 28, 2022

Fixed various bugs and performance issues.

## Version 108.0.1462.28: November 21, 2022

Fixed various bugs and performance issues.

## Version 108.0.1462.20: November 14, 2022

Fixed various bugs and performance issues.

## Version 108.0.1462.15: November 10, 2022

### Feature update

- **Graph APIs for Cloud Site List Management.** New Graph APIs that allow IT admins in organizations to create, manage, and publish their site lists for IE mode in the cloud.  For more information, see [Use the Edge API in Microsoft Graph](/graph/api/resources/browser-edge-api-overview?view=graph-rest-beta&preserve-view=true).

- **More reliable web defense.** Browse the web with more reliable protection thanks to the rewritten [Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) library for Microsoft Edge on Windows, Mac, and Linux. The new SmartScreen library was first made available on Windows and Mac, and now makes its debut on Linux with Microsoft Edge version 108. Microsoft Edge version 108 also brings new product optimizations (that is better proxy handling) and bug fixes by having the SmartScreen library use Microsoft Edge's built-in network stack.

### Policy updates

#### New policies

- [EncryptedClientHelloEnabled](/DeployEdge/microsoft-edge-policies#encryptedclienthelloenabled) - TLS Encrypted ClientHello Enabled
- [NewTabPageAppLauncherEnabled](/DeployEdge/microsoft-edge-policies#newtabpageapplauncherenabled) - Hide App Launcher on Microsoft Edge new tab page

#### Obsoleted policy

- [NewSmartScreenLibraryEnabled](/DeployEdge/microsoft-edge-policies#newsmartscreenlibraryenabled) Enable new SmartScreen library

## Version 107.0.1418.23: October 26, 2022

Fixed various bugs and performance issues.

## Version 107.0.1418.20: October 24, 2022

Fixed various bugs and performance issues.

## Version 107.0.1418.16: October 20, 2022

Fixed various bugs and performance issues.

## Version 107.0.1418.13: October 18, 2022

Fixed various bugs and performance issues.

## Version 107.0.1418.8: October 13, 2022

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
- [WebSQLNonSecureContextEnabled](/DeployEdge/microsoft-edge-policies#websqlnonsecurecontextenabled) - Force WebSQL in nonsecure contexts to be enabled

#### Deprecated policy

- [MicrosoftOfficeMenuEnabled](/DeployEdge/microsoft-edge-policies#microsoftofficemenuenabled) - Allow users to access the Microsoft Office menu

#### Obsoleted policy

- [BuiltinCertificateVerifierEnabled](/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) - Determines whether the built-in certificate verifier are used to verify server certificates

## Version 106.0.1370.30: September 29, 2022

Fixed various bugs and performance issues.

## Version 106.0.1370.26: September 26, 2022

Fixed various bugs and performance issues.

## Version 106.0.1370.17: September 16, 2022

Fixed various bugs and performance issues.

## Version 106.0.1370.15: September 15, 2022

Fixed various bugs and performance issues.

### Feature updates

- **More reliable web defense.** Browse the web with more reliable protection thanks to the rewritten [Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) library for Microsoft Edge on Windows and macOS. The new SmartScreen library was first made available on Windows with Microsoft Edge version 103, and now makes its debut on macOS with Microsoft Edge version 106. The [NewSmartScreenLibraryEnabled](/deployedge/microsoft-edge-policies#newsmartscreenlibraryenabled) policy is now deprecated in Microsoft Edge version 106 and obsolete in Microsoft Edge version 107.

### Policy updates

#### New policies

- [EfficiencyModeEnabled](/DeployEdge/microsoft-edge-policies#efficiencymodeenabled) - Efficiency mode enabled
- [EfficiencyModeOnPowerEnabled](/DeployEdge/microsoft-edge-policies#efficiencymodeonpowerenabled) - Enable efficiency mode when the device is connected to a power source
- [InternetExplorerIntegrationAlwaysUseOSCapture](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationalwaysuseoscapture) Always use the OS capture engine to avoid issues with capturing Internet Explorer mode tabs

#### Deprecated policies

- [NewSmartScreenLibraryEnabled](/deployedge/microsoft-edge-policies#newsmartscreenlibraryenabled) – Allows the Microsoft Edge browser to load the new SmartScreen library for any SmartScreen checks on site URLs or application downloads.

#### Obsoleted policies

- [OutlookHubMenuEnabled](/DeployEdge/microsoft-edge-policies#outlookhubmenuenabled) - Allow users to access the Outlook menu
- [EdgeDiscoverEnabled](/DeployEdge/microsoft-edge-policies#edgediscoverenabled) - Discover feature In Microsoft Edge

## Version 105.0.1343.34: September 9, 2022

Fixed various bugs and performance issues.

## Version 105.0.1343.27: September 2, 2022

Fixed various bugs and performance issues.

## Version 105.0.1343.23: August 31, 2022

Fixed various bugs and performance issues.

## Version 105.0.1343.17: August 26, 2022

Fixed various bugs and performance issues.

## Version 105.0.1343.10: August 19, 2022

Fixed various bugs and performance issues.

## Version 105.0.1343.7: August 16, 2022

Fixed various bugs and performance issues.

### Feature updates

- **Improvement to the Cloud Site List Management experience for IE mode.**

  - You can restore to one of the last three published versions of your site list in the Microsoft 365 Admin Center. For more information, see [Restore a previous version of a site list](/deployedge/edge-ie-mode-cloud-site-list-mgmt#restore-a-previous-version-of-a-site-list).
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

#### Deprecated policy

- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains

#### Additional change

- [GuidedSwitchEnabled](/DeployEdge/microsoft-edge-policies#guidedswitchenabled) - Add Linux platform support

## Version 104.0.1293.44: August 3

Fixed various bugs and performance issues.

### Feature updates

- **Enhance your security on the web**. Improvements to **Enhance your security on the web** in *edge://settings/privacy* now include **Basic** as the new default option.  With this option, Microsoft Edge applies added security protection to the less visited sites. This preserves the user experience for the most popular sites on the web. For more information, see [Browse more safely with Microsoft Edge](/deployedge/microsoft-edge-security-browse-safer).

## Version 104.0.1293.41: August 1

Fixed various bugs and performance issues.

## Version 104.0.1293.35: July 25

Fixed various bugs and performance issues.

## Version 104.0.1293.25: July 18

Fixed various bugs and performance issues.

### Feature updates

- **Import Chrome data without Chrome during First Run Experience.** This feature lets a user bring in their Chrome data by logging in to their Google account during Microsoft Edge's First Run Experience. This feature can be turned off by disabling First Run Experience with the [HideFirstRunExperience](/deployedge/microsoft-edge-policies#hidefirstrunexperience) policy, or by setting [AutoImportAtFirstRun](/deployedge/microsoft-edge-policies#autoimportatfirstrun) to 'DisabledAutoImport'.

## Version 104.0.1293.21: July 14

Fixed various bugs and performance issues.

## Version 104.0.1293.14: July 7

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

## Version 103.0.1264.45: July 1

Fixed various bugs and performance issues.

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

- **Client Certificate Switcher.** This feature offers a way for users to clear the remembered certificate and resurface the certificate picker when visiting a site requiring http certificate authentication. Switching can be done without manually quitting Microsoft Edge.

- **More reliable web defense.** Browse the web with more reliable protection thanks to the rewritten [Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) library for Microsoft Edge on Windows. The [NewSmartScreenLibraryEnabled](microsoft-edge-policies.md#newsmartscreenlibraryenabled) policy allows enterprise customers to continue using the legacy version of the library until it's deprecated in Microsoft Edge version 105.

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

## Version 101.0.1210.10: April 8

### Feature updates

- **Ability to set default profile.** The [EdgeDefaultProfileEnabled](/DeployEdge/microsoft-edge-policies#edgedefaultprofileenabled) policy lets you set a default profile to be used when opening the browser rather than the last profile used. This policy isn't applicable if the `--profile-directory` parameter has been specified.

- **Launch Progressive Web Apps (PWAs) from Favorites Bar.** Improvements to the PWA launch experience begin to show up starting with an Apps icon that can be added to the toolbar.

- **Manage the "Allow extensions from other stores" setting.** Use the [ControlDefaultStateOfAllowExtensionFromOtherStoresSettingEnabled](/DeployEdge/microsoft-edge-policies#controldefaultstateofallowextensionfromotherstoressettingenabled) policy to control the default state of the "Allow extensions from other stores" setting.

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

#### Deprecated policy

- [ForceCertificatePromptsOnMultipleMatches](/DeployEdge/microsoft-edge-policies#forcecertificatepromptsonmultiplematches) - Configure whether Microsoft Edge should automatically select a certificate when there are multiple certificate matches for a site configured with "AutoSelectCertificateForUrls"

#### Obsoleted policy

- [WebSQLInThirdPartyContextEnabled](/DeployEdge/microsoft-edge-policies#websqlinthirdpartycontextenabled) - Force WebSQL in third-party contexts to be re-enabled


## Version 100.0.1185.27: March 31

Fixed various bugs and performance issues.

## Version 100.0.1185.23: March 28

Fixed various bugs and performance issues.

## Version 100.0.1185.17: March 23

Fixed various bugs and performance issues.

## Version 100.0.1185.12: March 18

Fixed various bugs and performance issues.

### Feature updates

- **Streamlining Microsoft 365 Application Protocol Activations.** Microsoft 365 Application Protocol Activations on trusted Microsoft cloud storage services will now launch certain Microsoft 365 applications directly, including SharePoint subdomains and Microsoft OneDrive URLs. You can use the policies [AutoLaunchProtocolsComponentEnabled](/deployedge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) and [AutoLaunchProtocolsFromOrigins](/deployedge/microsoft-edge-policies#autolaunchprotocolsfromorigins) to enable the application protocol activation prompts if desired, and to define other applications and services where warnings are enabled or disabled.

## Version 100.0.1185.10: March 17

### Feature updates

- **Improvements to the Cloud Site List Management experience for IE Mode.** You can configure session cookie sharing between Microsoft Edge and Internet Explorer for IE Mode on your site list in the Microsoft 365 Admin Center. **Note:** This is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout

- **Preview PDF files in Microsoft Outlook and File Explorer.** Users can view a PDF file in a lightweight and rich read-only preview.  Available for Outlook Desktop PDF attachments or for local PDF files using File Explorer.  

- **Installed web app synchronization across all desktop devices.** Websites or Progressive Web Apps (PWAs) that have been installed as applications will synchronize across all desktop devices that you've signed into and enabled sync on. They'll show as "Available apps" for you to install. An app removed from one device will sync the removal on all devices.

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

## Version 99.0.1150.39: March 10

### Feature updates

- **Improvements to the Cloud Site List Management experience for IE Mode.** Identify gaps in your enterprise site list by configuring reporting of site feedback with the [InternetExplorerIntegrationCloudUserSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) and [InternetExplorerIntegrationCloudNeutralSitesReporting](/deployedge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) policies. You can view local site list URLs from users and potentially misconfigured neutral site URLs in the Microsoft Edge site lists experience in the Microsoft 365 Admin Center. To learn more, see [View site feedback on the Microsoft 365 Admin Center](/deployedge/edge-ie-mode-cloud-site-list-mgmt#view-site-feedback-on-the-microsoft-365-admin-center-1).  **Note:** This is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

## Version 99.0.1150.30: March 2

Fixed various bugs and performance issues.

## Version 99.0.1150.25: February 25

Fixed various bugs and performance issues.

## Version 99.0.1150.21: February 22

Fixed various bugs and performance issues.

## Version 99.0.1150.16: February 14

Fixed various bugs and performance issues.

## Version 99.0.1150.11: February 9

### Feature updates

- **Upcoming three-digit version number in user agent string.** Starting with version 100, Microsoft Edge will send a three-digit version number in the User-Agent header, for example "Edg/100". Starting with Microsoft Edge 97, site owners can test this upcoming agent string by enabling the **#force-major-version-to-100** experiment flag in *edge://flags* to ensure their User-Agent parsing logic is robust and works as expected.

- **Personalize multi-profile experiences with profile preferences for sites.** Users can personalize their multi-profile experience with the ability to create a customized list of sites for automatic profile switching in Microsoft Edge.

- **Bidirectional Cookie Sharing for IE mode.** This feature expands on the cookie sharing capability already available and lets users sync specific session cookies from Internet Explorer/IE mode to Microsoft Edge. For more information, see [Cookie sharing between Microsoft Edge and Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

- **Navigate PDF documents using page thumbnails.** You will now be able to navigate through your PDF document using thumbnails that represent the pages. These thumbnails will appear in the pane on the left side of the PDF reader.

- **Configure the list of domains for which the password manager User Interface (UI) for Save and Fill will be disabled.** Use the [PasswordManagerBlocklist](/deployedge/microsoft-edge-policies#passwordmanagerblocklist) policy to configure the list of domains (HTTP/HTTPS schemas and hostnames only) where Microsoft Edge should disable the password manager. This means that Save and Fill workflows will be disabled, which ensures that passwords for those websites can't be saved or auto filled into web forms.

- **Update extensions to the Microsoft Edge Add-ons store using API's (in public preview).** You can integrate these API's directly into your build pipeline, and publish package updates to the Microsoft Edge Add-on website. To learn more, see [Using the Microsoft Edge Add-ons API (in private preview)](/microsoft-edge/extensions-chromium/publish/api/using-addons-api)

### Policy updates

#### New policies

- [AllowGamesMenu](/DeployEdge/microsoft-edge-policies#allowgamesmenu) - Allow users to access the games menu
- [DoNotSilentlyBlockProtocolsFromOrigins](/DeployEdge/microsoft-edge-policies#donotsilentlyblockprotocolsfromorigins) - Define a list of protocols that can not be silently blocked by anti-flood protection
- [HubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#hubssidebarenabled) - Show Hubs Sidebar
- [InternetExplorerIntegrationCloudNeutralSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudneutralsitesreporting) - Configure reporting of potentially misconfigured neutral site URLs to the M365 Admin Center Site Lists app
- [InternetExplorerIntegrationCloudUserSitesReporting](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudusersitesreporting) - Configure reporting of IE Mode user list entries to the M365 Admin Center Site Lists app
- [PasswordManagerBlocklist](/DeployEdge/microsoft-edge-policies#passwordmanagerblocklist) - Configure the list of domains for which the password manager UI (Save and Fill) will be disabled
- [RelatedMatchesCloudServiceEnabled](/DeployEdge/microsoft-edge-policies#relatedmatchescloudserviceenabled) - Configure Related Matches in Find on Page
- [SignInCtaOnNtpEnabled](/DeployEdge/microsoft-edge-policies#signinctaonntpenabled) - Enable sign in click to action dialog
- [UserAgentReduction](/DeployEdge/microsoft-edge-policies#useragentreduction) - Enable or disable the User-Agent Reduction

## Version 98.0.1108.48: February 8

Fixed various bugs and performance issues.

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
- [SandboxExternalProtocolBlocked](/DeployEdge/microsoft-edge-policies#sandboxexternalprotocolblocked) - Allow Microsoft Edge to block navigating to external protocols in a sandboxed iframe.
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

## Version 97.0.1072.21: December 1

### Feature updates

- **Use current profile to sign into websites when multiple work or school accounts are signed in on a device.** When multiple work or school accounts are signed in on a device, users are asked to choose an account from the account picker to continue their visits to websites. In this release, users are prompted to allow Microsoft Edge to sign in to the websites automatically with the work and school account that's signed into current profile. Users can turn this feature on and off in **Settings/Profile preferences**.

- **Add support for Microsoft Endpoint Data Loss Prevention (DLP) on macOS.** Microsoft Endpoint DLP policy enforcement is available natively on macOS.

- **Open digitally signed PDF files.**  Digital signatures are used extensively to validate the authenticity of, and changes to, a document. Users can validate the signatures for PDF files directly from the browser, without the need for any add-ins.

- **Citations in Microsoft Edge.** Citing sources for research is a common requirement for students. They have to manage many research references and sources, which aren't easy tasks. They also have to translate these citations to proper citation formats like APA, MLA, and Chicago. This new "Citations" feature in Microsoft Edge (now in Preview) gives students a better way to manage and generate citations as they research online. With Citations turned on in Collections or from **Settings and more (Alt-F)**, Microsoft Edge automatically generates citations that students can use later so they can stay focused on their research. When they're done, they can easily compile these citations into a final deliverable. For more information, see [Previewing Citations in Microsoft Edge](https://blogs.windows.com/msedgedev/2021/11/04/preview-citations-feature-edge/).

### Policy updates

#### New Policies

- [AccessibilityImageLabelsEnabled](/DeployEdge/microsoft-edge-policies#accessibilityimagelabelsenabled) - Get Image Descriptions from Microsoft Enabled
- [CORSNonWildcardRequestHeadersSupport](/DeployEdge/microsoft-edge-policies#corsnonwildcardrequestheaderssupport) - CORS nonwildcard request header support enabled
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

#### Obsoleted Policies

- [AppCacheForceEnabled](/deployedge/microsoft-edge-policies#appcacheforceenabled) - Allows the AppCache feature to be re-enabled, even if it's turned off by default.

## Version 96.0.1054.34: November 23

Fixed various bugs and performance issues.

## Version 96.0.1054.26: November 17

Fixed various bugs and performance issues.

## Version 96.0.1054.24: November 16

Fixed various bugs and performance issues.

## Version 96.0.1054.13: November 5

Fixed various bugs and performance issues.

## Version 96.0.1054.8: November 1

### Feature updates

- **Launch Progressive Web App (PWA) directly via protocol links.** Let installed PWAs handle links that use a specific protocol for a more integrated experience.

- **Learn how to solve math problems with Math Solver.** We're excited to announce that you can use Math Solver in Microsoft Edge to get help with a wide range of mathematical concepts. These concepts range from elementary arithmetic and quadratic equations to trigonometry and calculus. Math Solver lets you take a picture of a handwritten or printed math problem and then provides an instant solution with step-by-step instructions to help you learn how to reach the solution without help. Math Solver also comes with a mathematical keyboard that you can use to easily type math problems. This keyboard eliminates the need to search around a traditional keyboard to find the math characters you need. After solving your problem, Math Solver provides options to continue learning with quizzes, worksheets, and video tutorials.

- **Freeform highlighting on PDFs.** The PDF viewing and markup experience are improved with the addition of freeform highlighters. You can highlight sections in PDFs that you don't have access to, and scanned documents.

- **Hardware-enforced Stack Protection.**  Microsoft Edge begins supporting an even safer browsing mode that uses hardware-dependent control flow for browser processes on supported hardware (Intel 11th Gen. or AMD Zen 3). Note: Because this is a Controlled Feature Rollout, you might not notice this feature enabled on all devices. You can enable or disable Hardware-enforced Stack Protection by manipulating Image File Execution Options (IFEO) using group policy.

- **New warning dialog for typosquatting sites.** The browser will now show a warning on some sites with URLs that look similar to other sites. This UI uses client-side heuristics to warn users about sites that might be spoofing popular web sites. For more information, see [What is typosquatting?](https://support.microsoft.com/topic/what-is-typosquatting-54a18872-8459-4d47-b3e3-d84d9a362eb0).

- **Improved handoff between IE mode and the modern browser.**  Starting with this version of Microsoft Edge, navigation between Microsoft Edge and Internet Explorer mode includes form data and extra HTTP headers. Referrer headers, post data, forms data, and request methods are forwarded correctly across the two experiences. You can specify which data types should be included using the [InternetExplorerIntegrationComplexNavDataTypes](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) policy. For more information, see this FAQ: [My application requires transferring POST data between IE mode and Microsoft Edge](./edge-ie-mode-faq.md#my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported).

- **Cloud Site List Management for IE mode in Public Preview.**  Cloud Site List Management lets you manage your site lists for IE mode in the cloud without needing an on-premises infrastructure to host your organization's site list. You can access the Cloud Site List Management feature using the Microsoft Edge Site Lists experience in the Microsoft 365 Admin Center. To learn more, see the [Cloud Site List Management for IE mode (Public Preview)](./edge-ie-mode-cloud-site-list-mgmt.md) article.

- **Update Microsoft Edge WebWiew2 using WSUS.** IT Admins using WSUS to update Microsoft Edge will also be able to update Microsoft Edge WebView2 using WSUS. This capability gives admins an easier servicing process for offline devices.

- **WSUS updates for Server.** WSUS and Catalog updates for Microsoft Edge channels (Stable, Beta, Dev) will now apply to Windows Server SKUs that have Microsoft Edge installed, including Windows Server 2022. For more information on how to configure WSUS updates for Microsoft Edge, see [Update Microsoft Edge](/mem/configmgr/apps/deploy-use/deploy-edge?bc=%2FDeployEdge%2Fbreadcrumb%2Ftoc.json&toc=%2FDeployEdge%2Ftoc.json#update-microsoft-edge).

### Policy updates

#### New Policies

- [ApplicationGuardUploadBlockingEnabled](/DeployEdge/microsoft-edge-policies#applicationguarduploadblockingenabled) - Prevents files from being uploaded while in Application Guard.
- [AudioProcessHighPriorityEnabled](/DeployEdge/microsoft-edge-policies#audioprocesshighpriorityenabled)  - Allow the audio process to run with priority above normal on Windows.
- [AutoLaunchProtocolsComponentEnabled](/DeployEdge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) - AutoLaunch Protocols Component Enabled.
- [EfficiencyMode](/DeployEdge/microsoft-edge-policies#efficiencymode) - Configure when efficiency mode should become active.
- [ForceSyncTypes](/DeployEdge/microsoft-edge-policies#forcesynctypes) - Configure the list of types that are included for synchronization.
- [InternetExplorerIntegrationComplexNavDataTypes](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) - Configure whether form data and HTTP headers are sent when entering or exiting Internet Explorer mode.
- [InternetExplorerModeToolbarButtonEnabled](/DeployEdge/microsoft-edge-policies#internetexplorermodetoolbarbuttonenabled) - Show the Reload in Internet Explorer mode button in the toolbar.
- [PrintPostScriptMode](/DeployEdge/microsoft-edge-policies#printpostscriptmode) - Print in PostScript Mode.
- [PrintRasterizePdfDpi](/DeployEdge/microsoft-edge-policies#printrasterizepdfdpi) - Print in Rasterize PDF DPI.
- [RendererAppContainerEnabled](/DeployEdge/microsoft-edge-policies#rendererappcontainerenabled) - Enable renderer in app container.
- [SharedLinksEnabled](/DeployEdge/microsoft-edge-policies#sharedlinksenabled) - Show links shared from Microsoft 365 apps in History.
- [TyposquattingCheckerEnabled](/DeployEdge/microsoft-edge-policies#typosquattingcheckerenabled) - Configure Edge TyposquattingChecker.

<!-- end major 96 --->

## Version 95.0.1020.38: October 28

Fixed various bugs and performance issues.

## Version 95.0.1020.20: October 11

Fixed various bugs and performance issues.

## Version 95.0.1020.14: October 5

Fixed various bugs and performance issues.

## Version 95.0.1020.9: September 28

### Feature updates

- **View in File Explorer support for SharePoint Online libraries in Microsoft Edge.**  Now you can enable the View in File Explorer capability for SharePoint Online Modern Document Libraries. For this experience to be visible and work for your users, you'll need to enable the Microsoft Edge ["Configure the View in File Explorer feature for SharePoint pages in Microsoft Edge"](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) policy and update your SharePoint Online tenant configuration. Learn more: [View SharePoint files with File Explorer in Microsoft Edge - SharePoint in Microsoft 365 | Microsoft Docs](/SharePoint/sharepoint-view-in-edge).

- **Intranet zone file URL links will open in Windows File Explorer.**  You can allow file URL links to intranet zone files originating from intranet zone HTTPS websites to open Windows File Explorer for that file or directory. You can enable this experience using the [IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled) policy.

- **Improvements to the downloads experience.**  Support for the download user experience is being extended to progressive web applications PWAs and WebView. We'll also begin to support drag and drop to the File Explorer and Desktop.

- **Pick up where you left off on PDF documents.**  You can resume reading from the location where you last closed your PDF document.

- **Efficiency mode extends battery life when your laptop enters battery saver mode.**  Efficiency mode becomes active when your laptop enters battery saver mode to allow the browser to manage resource usage to extend the battery life of your machine. You'll have four options for when efficiency mode becomes active, Unplugged, and low battery, Unplugged, Always, and Never. Note: This is a Controlled Feature Rollout. Devices with a battery should have the feature turned on.

***New Policies***

- [BrowserLegacyExtensionPointsBlockingEnabled](/DeployEdge/microsoft-edge-policies#browserlegacyextensionpointsblockingenabled) - Enable browser legacy extension point blocking.
- [CrossOriginWebAssemblyModuleSharingEnabled](/DeployEdge/microsoft-edge-policies#crossoriginwebassemblymodulesharingenabled) - Specifies whether WebAssembly modules can be sent cross-origin.
- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) - Specifies whether the display-capture permissions-policy is checked or skipped.
- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) - Configure the pixel adjustment between window.open heights sourced from IE mode pages vs. Microsoft Edge mode pages.
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) - Configure the pixel adjustment between window.open widths sourced from IE mode pages vs. Microsoft Edge mode pages.
- [IntranetFileLinksEnabled](/DeployEdge/microsoft-edge-policies#intranetfilelinksenabled) - Allow intranet zone file URL links from Microsoft Edge to open in Windows File Explorer.
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) - Configure ShadowStack crash rollback behavior.
- [VisualSearchEnabled](/DeployEdge/microsoft-edge-policies#visualsearchenabled) - Enable visual search.

***Obsoleted Policies***

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) - Allow Internet Explorer mode testing.
- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) - Enable default legacy SameSite cookie behavior setting.

## Version 94.0.992.23: September 17

Fixed various bugs and performance issues.

## Version 94.0.992.19: September 13

Fixed various bugs and performance issues.

## Version 94.0.992.14: September 7

Fixed various bugs and performance issues.

## Version 94.0.992.9: September 2

### Feature updates

- **Microsoft Edge moving to a 4-week cadence for updates in Beta and Stable channels.**  We'll adopt a new, 4-week release cycle for major versions. You can read more about the decision here: https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/

- **New Extended stable option being offered.**  We're offering a new Extended Stable option to our managed Enterprise customers. The Extended Stable option stays on even numbered revisions and update every eight weeks. There is a biweekly security update.  Additional information here: https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **Improvements to default behavior of opening MHTML files.**  MHTML files continue to open in IE mode if IE mode is enabled, unless the MHTML file was saved from Microsoft Edge (using the Save As or Save Page As options in Microsoft Edge). If the file was saved from Microsoft Edge, it now opens in Microsoft Edge.  This change fixes a rendering issue that was observed when opening an MHTML file in IE mode when saved from Microsoft Edge.

- **Restrict private network requests to secure contexts.** Access to resources on local (intranet) networks from pages on the internet requires that those pages be delivered over HTTPS. This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, navigate to the [Chrome Platform Status entry](https://chromestatus.com/feature/5436853517811712). Two compatibility policies are available to support scenarios that need to preserve compatibility with nonsecure pages: [InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) and [InsecurePrivateNetworkRequestAllowedForUrls](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls).

- **Block mixed content downloads.** Secure pages only download files hosted on other secure pages, and downloads hosted on nonsecure (non-HTTPS) pages are blocked if initiated from a secure page. This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, navigate to the [Google security blog entry](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html).

- **Enable implicit sign-in for on-premises accounts.**   By enabling the OnlyOnPremisesImplicitSigninEnabled policy, only on-premises accounts are enabled for implicit sign-in.  Microsoft Edge doesn't attempt to implicitly sign in to MSA or Microsoft Entra accounts. Upgrade from on-premises accounts to Microsoft Entra accounts are stopped as well.

- **Free form text boxes added to PDF documents.**  We now support adding free form text boxes to PDF documents that you can use to fill in forms and add visible notes.

- **Update your passwords with ease.**  The browser will now take you directly to the Change Password page for a given website saving you time and mouse clicks by avoiding the need to navigate to the page manually. Once you're on this page the browser also autofills your existing password and suggest a strong, unique new password. Note: Currently this feature is available on a limited number of sites.  

- **New accessibility settings page.** We brought accessibility-related settings together on a single page. You can find the new edge://settings/accessibility page under the main settings list. Here you can find settings to make the web page bigger, show a high visibility outline around the area of focus and other settings that can help improve your web browsing experience. We'll continue to add new settings here in future versions of Microsoft Edge.

***New Policies***

- [ApplicationGuardPassiveModeEnabled](/DeployEdge/microsoft-edge-policies#applicationguardpassivemodeenabled) Ignore Application Guard site list configuration and browse Edge normally
- [OnlyOnPremisesImplicitSigninEnabled](/DeployEdge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) Only on-premises account enabled for implicit sign-in
- [WebRtcRespectOsRoutingTableEnabled](/DeployEdge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) Enable support for Windows OS routing table rules when making peer to peer connections via WebRTC

***Obsoleted Policy***

- [UserAgentClientHintsEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) Enable the User-Agent Client Hints feature

## Version 93.0.961.33: August 27

Fixed various bugs and performance issues.

## Version 93.0.961.27: August 20

Fixed various bugs and performance issues.

## Version 93.0.961.24: August 18

Fixed various bugs and performance issues.

## Version 93.0.961.11: August 3

### Feature updates

- **Initial Preferences in Microsoft Edge.**  Starting with Microsoft Edge version 93, deploying Microsoft Edge to your enterprise becomes easier with the addition of [Initial Preferences](/deployedge/initial-preferences-support-on-microsoft-edge-browser).

- **IE mode on Microsoft Edge will support "no-merge" behavior.**  Starting with Microsoft Edge version 93, IE mode on Microsoft Edge supports "no-merge". For an end user, when a new browser window is launched from an IE mode application, it is in a separate session, similar to the behavior in IE11. You'll need to adjust your site list to configure sites that need to prevent session sharing. Behind the scenes, for each window of Microsoft Edge, the first time an IE mode tab is visited within that window, if it is one of the designated "no-merge" sites, that window is locked into a different "no-merge" IE session from all other Microsoft Edge windows at least until the last IE mode tab is closed in that window. Learn more [here](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--no-merge--option-that-was-supported-in-internet-explorer-11-).

- **Tab Groups.**  The ability to categorize tabs into user-defined groups helps you more effectively find, switch, and manage tabs across multiple workstreams. To enable this, we're turning on tab grouping beginning with Microsoft Edge version 93.

- **Hide the title bar while using Vertical Tabs.**  Get the extra few pixels back by hiding the browser's title bar, while in Vertical Tabs. Starting with Microsoft Edge version 93, you can go to edge://settings/appearance and under the Customize Toolbar section select the option to hide the title bar while in Vertical Tab mode.

- **Video Picture in Picture (PiP) from hover toolbar.**  Starting with Microsoft Edge version 93, it will become even easier to enter Picture in Picture (PiP) mode. When you hover over a supported video, a toolbar appears that allows you to view that video in a PiP window. Note: this is currently available for Microsoft Edge users on macOS. Check back shortly as we continue our rollout to Windows users.

- **Removal of 3DES in TLS.**  Starting with Microsoft Edge version 93, support for the TLS_RSA_WITH_3DES_EDE_CBC_SHA cipher suite will be removed. This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, navigate to the [Chrome Platform Status entry](https://chromestatus.com/feature/6678134168485888). Additionally, in Microsoft Edge version 93, the [TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled) policy is available to support scenarios that need to preserve compatibility with outdated servers. This compatibility policy becomes obsolete and stops working in Microsoft Edge version 95. Ensure that you update affected servers before then.

- **Policies to bypass ClickOnce and DirectInvoke prompts.**  We updated our policies to enable bypassing ClickOnce's prompts and DirectInvoke's app for specified file types, from specified domains. To do this, you'll need to:

  - Enable [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) or [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - Enable [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes) policy and set the list of specific file types that ClickOnce and DirectInvoke should be disabled for
  - Enable the [AutoOpenAllowedForURLs](/deployedge/microsoft-edge-policies#autoopenallowedforurls) policy and set the list of specific domains that ClickOnce and DirectInvoke will be disabled for

  Note: AutoOpenAllowedForURLs is a supporter policy for AutoOpenFileTypes. If AutoOpenAllowedForURLs isn't set and AutoOpenFileTypes is set, then file types listed will automatically open from all URLs.

### New Policies

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
- [OneAuthAuthenticationEnforced](/DeployEdge/microsoft-edge-policies#oneauthauthenticationenforced) OneAuth Authentication Flow Enforced for signin
- [PasswordGeneratorEnabled](/DeployEdge/microsoft-edge-policies#passwordgeneratorenabled) Allow users to get a strong password suggestion whenever they are creating an account online
- [PrimaryPasswordSetting](/DeployEdge/microsoft-edge-policies#primarypasswordsetting) Configures a setting that asks users to enter their device password while using password autofill
- [PrintingWebpageLayout](/DeployEdge/microsoft-edge-policies#printingwebpagelayout) Sets layout for printing
- [RemoteDebuggingAllowed](/DeployEdge/microsoft-edge-policies#remotedebuggingallowed) Allow remote debugging
- [RelaunchWindow](/DeployEdge/microsoft-edge-policies#relaunchwindow) Set the time interval for relaunch
- [TravelAssistanceEnabled](/DeployEdge/microsoft-edge-policies#travelassistanceenabled) Enable travel assistance
- [TripleDESEnabled](/DeployEdge/microsoft-edge-policies#tripledesenabled) Enable 3DES cipher suites in TLS

#### Deprecated Policy

- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Enable default legacy SameSite cookie behavior setting

#### Obsoleted Policy

- [NewTabPageSetFeedType](/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) Configure the Microsoft Edge new tab page experience

#### Additional Change

- [ConfigureShare](/DeployEdge/microsoft-edge-policies#configureshare) Add mac platform support

## Version 93.0.961.18: August 10

Fixed various bugs and performance issues.

## Version 92.0.902.62: July 29

Fixed various bugs and performance issues.

## Version 92.0.902.55: July 21

Fixed various bugs and performance issues.

## Version 92.0.902.45: July 12

Fixed various bugs and performance issues.

## Version 92.0.902.40: July 6

Fixed various bugs and performance issues.

## Version 92.0.902.22: June 21

### Feature updates

- **Natural language search for browser history on the address bar**. Finding the article/website you're looking for is now easier thanks to natural language search right from the address bar. You can find search results based on page content/description/timing (such as "cake recipe from last week") in addition to titles/URL keyword matches alone.
Note: This is a Controlled Feature Rollout. If you don't see this feature, check back shortly as we continue our rollout.

- **Users can easily get to Internet Explorer mode on Microsoft Edge**. Starting with Microsoft Edge version 92, users can reload a site in Internet Explorer mode on Microsoft Edge instead of relying on the standalone IE 11 application while waiting for a site to be configured in the Enterprise Mode Site List. Users are prompted to add the site to their local site list such that navigating to the same page in Microsoft Edge will automatically render in IE mode for the next 30 days. You can use the *[InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed)* policy to configure this experience and allow access to the IE mode entry points and the ability to add sites to the local site list. You can use the *[InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays)* policy to adjust the number of days to keep sites on the local site list.
KB5003698 or later is required for Windows 10, version 1909; or KB5003690 or later is required for Windows 10, version 2004, Windows 10, version 20H2, or Windows 10, version 21H1 for the end-to-end experience.

- **MHTML files will default to opening in Internet Explorer mode**. Starting in Microsoft Edge version 92 Stable, MHTML file types will automatically open in Internet Explorer mode on Microsoft Edge instead of the Internet Explorer (IE11) application. This is most commonly observed while trying to view Outlook emails in a browser. This change occurs only if IE11 is the default handler for this file type. If you'd prefer to change this, you can do so before installing the Stable version 92 update using [this guidance](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

- **Payment instruments are now synced across devices**. Beginning with Microsoft Edge version 92, you can synchronize your payment information across your signed in devices.
Note: This is a Controlled Feature Rollout. If you don't see this feature, check back shortly as we continue our rollout.

- **"Disable developer mode extensions" warning can be permanently dismissed**. Beginning with Microsoft Edge version 92, you can turn off the warning "Disable developer mode extensions" by clicking on the 'Don't show this again' option.
Please note: this is a Controlled Feature Rollout. If you don't see this feature, check back shortly as we continue our rollout.

- **Manage your extensions right from the toolbar**. The all-new extensions menu on the toolbar will allow you to hide/pin extensions easily. The quick links to manage extensions and find new extensions will make it easy for you to find new extensions and manage your existing ones. Note: This is a Controlled Feature Rollout. If you don't see this feature, check back shortly as we continue our rollout.

- **Automatic HTTPS**. Users have the option to upgrade navigation from HTTP to HTTPS on domains likely to support this more secure protocol. This support can also be configured to attempt delivery over HTTPS for all domains. Note: We're experimenting with this feature and this behavior isn't seen if you opted out of experiments.

- **Improvements to font rendering**. Improvements are made to the rendering of text to improve clarity and reduce blurriness.
Note: This is a Controlled Feature Rollout. If you don't see this feature, check back shortly as we continue our rollout.

- **Microsoft Editor.**  Microsoft Editor offers enhanced spell checking, grammar checking, and text predictions. [Learn more](https://support.microsoft.com/en-us/office/microsoft-editor-checks-grammar-and-more-in-documents-mail-and-the-web-91ecbe1b-d021-4e9e-a82e-abc4cd7163d7).

### Policy updates

#### New policies

Eight new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added:

- [AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) Single sign-on for work or school sites using this profile enabled.
- [AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault) Configure Automatic HTTPS
- [HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled) Control use of the Headless Mode
- [InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed)Specifies whether to allow insecure websites to make requests to more-private network endpoints
- [InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls) Allow the listed sites to make requests to more-private network endpoints from insecure contexts
- [InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) Specify the number of days that a site remains on the local IE mode site list
- [InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) Allow unconfigured sites to be reloaded in Internet Explorer mode
- [SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed) Specifies whether SharedArrayBuffers can be used in a non cross-origin-isolated context

#### Obsoleted Policy

- [EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) Allow certificates signed using SHA-1 when issued by local trust anchors.

## Version 92.0.902.9: June 8

Fixed various bugs and performance issues.

## Version 91.0.864.41: June 3

Fixed various bugs and performance issues.

## Version 91.0.864.37: May 27

Fixed various bugs and performance issues.

## Version 91.0.864.36: May 26

Fixed various bugs and performance issues.

## Version 91.0.864.33: May 21

Fixed various bugs and performance issues.

## Version 91.0.864.27: May 14

Fixed various bugs and performance issues.

## Version 91.0.864.19: May 7

Fixed various bugs and performance issues.

## Version 91.0.864.15: May 3

Fixed various bugs and performance issues.

## Version 91.0.864.11: April 30

### Feature updates

- **Identify network traffic originating from Microsoft Defender Application Guard containers at the proxy level**. Starting with Microsoft Edge version 91, there's built in support to tag network traffic originating from Application Guard containers, allowing enterprises to identify them and apply specific policies.

- **Support option to allow synchronizing Favorites from the host to the Edge Application Guard container**. Starting with Microsoft Edge version 91, users can configure Application Guard to synchronize their favorites from the host to the container. This ensures new favorites appear on the container as well.

- **Support for Speech Recognition APIs**. Starting with Microsoft Edge version 91, API support for speech recognition commands on Google.com and similar sites are added. This feature is limited to a randomly selected group of users who enabled experimentation. These users are giving feedback to the feature team.

- **Personalize your browser with new theme colors**. Make Microsoft Edge your own with one of the fourteen new theme colors on the Settings -> Appearance page. You can also install custom themes from the Microsoft Edge Add-on site. [Learn more](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

- **Interrupt Downloads** Starting with Microsoft Edge version 91 the browser will automatically interrupt downloads of types that could harm your computer if those downloads are started without a user interaction and aren't supported by SmartScreen Application Reputation check. Users can override and continue to download by right clicking and choosing "Keep" on the download item. 
<!---
Enterprise administrators may opt out of this behavior one of these two policies: 

    - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](./deployedge/microsoft-edge-policies.md#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains --->
For more information, see [Microsoft Edge Security downloads interruptions](/deployedge/microsoft-edge-security-downloads-interruptions)

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
<!-- end major 91 -->

## Version 90.0.818.46: April 22

Fixed various bugs and performance issues.

## Version 90.0.818.42: April 20

Fixed various bugs and performance issues.

## Version 90.0.818.41: April 16

Fixed various bugs and performance issues.

## Version 90.0.818.38: April 14

Fixed various bugs and performance issues.

## Version 90.0.818.36: April 12

Fixed various bugs and performance issues.

## Version 90.0.818.27: April 2

Fixed various bugs and performance issues.

## Version 90.0.818.22: March 29

Fixed various bugs and performance issues.

## Version 90.0.818.14: March 22

Fixed various bugs and performance issues.
<!-- begin major 90 -->
## Version 90.0.818.8: March 16

### Feature updates

- **Single Sign On (SSO) is now available for Microsoft Entra accounts and Microsoft Account (MSA) on macOS**. A user signed in on Microsoft Edge on macOS will now get automatically signed into websites that are configured to allow single sign-on with Work and Microsoft accounts (for example, bing.com, office.com, msn.com, and outlook.com).

- **Kiosk mode.** Starting with Microsoft Edge version 90, we locked down the UI print settings to only allow the configured printers and "Print to PDF" options. We have also done improvements within the assigned access single app kiosk mode to restrict the launch of other applications from the browser. For more information about the kiosk mode features, [see](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features).

- **Printing:**

  - **New print rasterization mode for non-PostScript printers**. Starting with Microsoft Edge version 90, Admins can use a new policy to define print rasterization mode for their users. This policy  controls how Microsoft Edge prints to non-PostScript printers on Windows. Sometimes print jobs on non-PostScript printers need to be rasterized to print correctly. The print options are Full and Fast.

  - **Additional page scaling options for printing**. Users are now able to customize scaling while printing webpages and PDF documents using more options. The "Fit to Page" option ensures that the webpage or document is fit into the space available in the selected "Paper size" for printing. The "Actual size" option ensures that there are no changes in the size of the contents being printed regardless of the selected "Paper size".

- **Productivity:**

  - **Autofill suggestions are extended to include address fields content from clipboard**. Clipboard content is parsed when you click on a profile/address field (for example, phone, email, zip code, city, state, etc.) to show as autofill suggestions.

  - **Users can search for autofill suggestions even if a form or field isn't detected**. Today if you have your information saved on Microsoft Edge, autofill suggestions pop up automatically and help you save time while filling out forms. In cases where autofill misses a form, or if you want to fetch data in forms that don't typically have autofill (like temporary forms), you can search for your information using autofill.

- **Access downloads from a flyout in the menu bar**. Downloads appear in the top-right corner with all the active downloads in one place. This menu is easily dismissible so users can continue browsing uninterrupted, and they can monitor overall download progress right from the toolbar. [Learn more](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).


### Policy updates

#### New policies

Seven new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added:

- [ApplicationGuardFavoritesSyncEnabled](./microsoft-edge-policies.md#applicationguardfavoritessyncenabled) - Application Guard Favorites Sync Enabled
- [ManagedConfigurationPerOrigin](./microsoft-edge-policies.md#managedconfigurationperorigin) - Sets managed configuration values for websites to specific origins
- [PrintRasterizationMode](./microsoft-edge-policies.md#printrasterizationmode) - Print Rasterization Mode
- [QuickViewOfficeFilesEnabled](./microsoft-edge-policies.md#quickviewofficefilesenabled) - Manage QuickView Office files capability in Microsoft Edge
- [SSLErrorOverrideAllowedForOrigins](./microsoft-edge-policies.md#sslerroroverrideallowedfororigins) - Allow users to proceed from the HTTPS warning page for specific origins
- [WindowOcclusionEnabled](./microsoft-edge-policies.md#windowocclusionenabled) - Enable Window Occlusion
- [WindowsHelloForHTTPAuthEnabled](./microsoft-edge-policies.md#windowshelloforhttpauthenabled) - Windows Hello For HTTP Auth Enabled

#### Deprecated policies

- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - Enable Native Window Occlusion
- [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin)- Minimum TLS version enabled
<!-- end major 90 -->

## Version 89.0.774.54: March 13

Fixed various bugs and performance issues.

## Version 89.0.774.50: March 10

Fixed various bugs and performance issues.

## Version 89.0.774.48: March 8

Fixed various bugs and performance issues.

## Version 89.0.774.45: March 3

Fixed various bugs and performance issues.

## Version 89.0.774.39: February 26

Fixed various bugs and performance issues.

## Version 89.0.774.34: February 22

Fixed various bugs and performance issues.

## Version 89.0.774.27: February 12

Fixed various bugs and performance issues.

## Version 89.0.774.23: February 8

Fixed various bugs and performance issues.

## Version 89.0.774.18: February 3

### Feature updates

- **Kiosk mode enables additional lockdown capabilities**. Starting with Microsoft Edge version 89, we added more lockdown capabilities within kiosk mode to enable customers to get the job done in a productive and more secure experience. [Learn more](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **The Enterprise Mode Site List Manager tool will be available in the browser through the *edge://compat* page**. You can use this tool to create, edit, and export your site list XML for Internet Explorer mode on Microsoft Edge. You can enable access to this tool as needed through group policy. [Learn More](./edge-ie-mode-site-list-manager.md).

- **Improve browser performance with sleeping tabs**. Sleeping tabs improves browser performance by putting inactive tabs to sleep to free up system resources like memory and CPU so active tabs or other applications can use them. Users can prevent sites from going to sleep and configure the length of time before an inactive tab goes to sleep. To keep users in their flow, there are also [heuristics](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) to prevent certain sites from going to sleep, such as intranet sites. This feature can be managed with group policies.

  > [!NOTE]
  > "Improve browser performance with sleeping tabs" is an update to the February 3 release notes for major version 89.0.774.18.

- **Reset your Microsoft Edge sync data in the cloud manually**. We're introducing a way to reset your Microsoft Edge sync data from within the product. This action ensures that your data is cleared from Microsoft services, and resolving certain product issues that previously required a support ticket.

- **Improvements to text selection experience within PDF documents**. Users begin to get a smoother and more consistent text selection experience across PDF documents opened in Microsoft Edge starting with version 89.

- **Date of birth field now supported in autofill**. Today Microsoft Edge helps you save time and effort while filling out forms and creating accounts online by auto filling your data like addresses, names, phone numbers, etc. Starting with Microsoft Edge version 89, we're adding support for another field that you can have saved and autofilled - date of birth. You can view, edit, and delete this information anytime in your profile settings.

- **Support for natural language search on the address bar, history search page, and the history hub**. Starting with Microsoft Edge version 89, finding an article/website is easier with the natural language search on the address bar, history page, and history hub. Users can search for previously viewed page content/description/timing (such as "cake recipe from last week") in addition to titles/URL keyword matches. This feature is limited to a randomly selected group of users who enabled experimentation. These users are giving feedback to the feature team.

### Policy updates

#### New policies

- [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime) - Browsing Data Lifetime Settings
- [MAMEnabled](./microsoft-edge-policies.md#mamenabled) - Mobile App Management Enabled
- [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages) - Define an ordered list of preferred languages that websites should display in if the site supports the language
- [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled) - Allow recommendations and promotional notifications from Microsoft Edge
- [PrintingAllowedBackgroundGraphicsModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes) - Restrict background graphics printing mode
- [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault)- Default background graphics printing mode
- [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist)- Block smart actions  for a list of services

#### Obsoleted policies

- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) - Use a default referrer policy of no-referrer-when-downgrade
- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - Enable usage and crash-related data reporting
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices)|Send site information to improve Microsoft services
<!-- end major 89 -->

## Version 88.0.705.56: January 29

Fixed various bugs and performance issues.

## Version 88.0.705.49: January 20

Fixed various bugs and performance issues.

## Version 88.0.705.45: January 15

Fixed various bugs and performance issues.

## Version 88.0.705.41: January 11

Fixed various bugs and performance issues.

## Version 88.0.705.29: December 21

Fixed various bugs and performance issues.

<!-- begin major 88 -->
## Version 88.0.705.18: December 9

### Feature updates

- **Deprecations:**

  - Deprecate support for FTP protocol. Support for the legacy FTP protocol is removed from Microsoft Edge. Attempting to navigate to an FTP link results in the browser directing the Operating System to open an external application to handle the FTP link. Alternatively, IT administrators can configure Microsoft Edge to use IE Mode for sites that rely on the FTP protocol.
  - Adobe Flash support will be removed. Starting with Microsoft Edge Beta version 88, Adobe Flash capability and support will be removed. Learn more: [Update on Adobe Flash Player End of Support - Microsoft Edge Blog (windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Authentication:**

  - Single Sign On (SSO) now available for Microsoft Entra accounts and Microsoft Account (MSA) on macOS and down-level Windows. A user signed in on Microsoft Edge on either macOS or down-level Microsoft Windows (7, 8.1) will now get automatically signed into websites that are configured to allow single sign on with Work and Microsoft accounts (for example, bing.com, office.com, msn.com, outlook.com).<br>Note: A user might have to sign out and then sign back in if they'd signed into Microsoft Edge in a version before Microsoft Edge 88 to use this feature.
  - Automatically switch users on macOS to their work profile for sites that authenticate with their work account. Starting with Microsoft Edge version 88, we provide the ability to switch sites that authenticate with a user's work profile on macOS.<br>Note: A user may have to sign out and then sign back in if they'd signed into Microsoft Edge in a version prior to Microsoft Edge 88 to use this feature.

- **Kiosk mode option to end session**. The "End session" button is now available in a kiosk mode public browsing experience. This feature ensures that browser data and settings are deleted when Microsoft Edge is closed. Learn more about kiosk mode features and roadmap, [Configure Microsoft Edge kiosk mode](./microsoft-edge-configure-kiosk-mode.md).

- **Security and Privacy:**

  - Alerts are generated if a user's password is found in an online leak. User passwords are checked against a repository of known-breached credentials. A user gets an alert if a match is found. To ensure security and privacy, user passwords are hashed and encrypted when they're checked against the database of leaked credentials.
  - Automatically upgrade mixed content. Secure pages delivered over HTTPS might contain references images that are served over non-secure HTTP. To improve privacy and security in Microsoft Edge 88, those images will be retrieved over HTTPS instead. If the image isn't available over HTTPS, it will not be loaded.
  - View site permissions by site and by recent activity. Starting with Microsoft Edge 88, users are able to manage site permissions more easily. They'll be able to view permissions by web site rather than just permission type. Additionally, we added a recent activity section that shows a user all the recent changes to their site permissions.
  - Increased controls for browser cookies. Starting with Microsoft Edge 88, users can delete third-party cookies without affecting first party cookies. Users will also be able to filter their cookies by first or third party and sort by name, number of cookies, and the amount of data stored and last modified.

- **Performance:**

  - Improve browser performance with sleeping tabs. Sleeping tabs improves browser performance by putting inactive tabs to sleep to free up system resources like memory and CPU so active tabs or other applications can use them. Users can prevent sites from going to sleep and configure the length of time before an inactive tab goes to sleep. To keep users in their flow, there are also heuristics to prevent certain sites from going to sleep, such as intranet sites. This feature is limited to a randomly selected group of users who have enabled experimentation. We're planning to have the sleeping tabs feature enabled by default with Microsoft Edge version 89. This feature can be managed with group policies.
  - Improve Microsoft Edge startup speed with startup boost. To improve Microsoft Edge startup speed, we developed a feature named startup boost. Startup boost makes Microsoft Edge launch faster by enabling Microsoft Edge to run in the background. Note: This feature is limited to a randomly selected group of users who have enabled experimentation. These users are giving feedback to the feature team.

- **Productivity:**

  - Improve productivity and multi-tasking with vertical tabs. As the number of horizontal tabs grows, site titles start to get cut off and tab controls are lost as each tab shrinks. This interrupts user workflow as they spend more time finding, switching, and managing their tabs and less time on the task at hand. Vertical tabs let users move their tabs to the side, where vertically aligned icons and longer site titles make it easier to quickly scan, identify and switch to the tab they want to open.
  - Auto filling the date of birth field. Microsoft Edge already helps save time and effort while filling out forms and creating accounts online by auto filling user data such as addresses, names, phone numbers, etc. Microsoft Edge now supports the date of birth field which users can save and auto fill. A user can view, edit, and delete this information anytime in their profile settings.
  - Improvements to Recently closed in History. Recently closed now keeps the last 25 tabs and windows from any past browsing session rather than just the previous session. Users can select Recently closed in the new History experience to see all the tabs that were open.
  - "Your day at a glance" feature enabled by default. Starting with Microsoft Edge version 88, information workers can benefit from intelligent productivity features on their New tab page (NTP). We offer users signed in with their work or school account personalized and relevant content powered by their Microsoft 365 Graph. Users can quickly scan their "Your day at a glance" modules to easily track their meetings and recent work and quickly launch the applications they want to use.

- **PDF:**

  - PDF document display in book view (two pages). Starting with Microsoft Edge version 88, users can view PDF documents in a single page or in the two page book view. To change the view, select the **Page View** button in the toolbar.
  - Anchored text notes support for PDF files. Starting with Microsoft Edge version 87, users can add typed text notes on any piece of text in PDF files.
  - Smoother text selection experience in PDF documents. Users get a smoother and consistent text selection experience across PDF documents opened in Microsoft Edge.
  - View webpages saved as PDF files in the Downloads bar. Users can now view the PDF files generated by setting "Save as PDF" as the printer destination for webpages in the Downloads bar.

- **Fonts:**

  - Browser icons are updated to the Fluent design system. As part of our continued work around Fluent Design in the browser, we made changes to closer align icons to the new Microsoft icon system. These changes impact many of our high-touch user interfaces, including tabs, address bar, and navigational and wayfinding icons found in our various menus.
  - Improved font rendering. Text rendering is improved for better clarity and to reduce blurriness.

### Policy updates

#### New policies

Sixteen new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added.

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
- [UpdatePolicyOverride](./microsoft-edge-policies.md#updatepolicyoverride) - Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.
- [VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) - Configures availability of a vertical layout for tabs on the side of the browser.
- [WebRtcAllowLegacyTLSProtocols](./microsoft-edge-policies.md#webrtcallowlegacytlsprotocols) - Allow legacy TLS/DTLS downgrade in WebRTC.

#### Deprecated policies

The following policies are deprecated.

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) - Enable Proactive Authentication.
- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist) - Configure proxy bypass rules.
- [ProxyMode](./microsoft-edge-policies.md#proxymode) - Configure proxy server settings.
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl) - Set the proxy.pac file URL.
- [ProxyServer](./microsoft-edge-policies.md#proxyserver) - Configure address or URL of proxy server.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) - Allow WebDriver to Override Incompatible Policies.

#### Obsoleted policies

The following policies are obsoleted.

- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting) - Default Adobe Flash setting.
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls) - Allow the Adobe Flash plug-in on specific sites.
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls) - Block the Adobe Flash plug-in on specific sites.
- [RunAllFlashInAllowMode](./microsoft-edge-policies.md#runallflashinallowmode) - Extend Adobe Flash content setting to all content.

<!-- end major 88 -->

## Version 87.0.664.55: December 3

Fixed various bugs and performance issues. The following new feature is supported in this release.

- **Alerts are generated if a user's password is found in an online leak**. User passwords are checked against a repository of known-breached credentials and send the user an alert if a match is found. To ensure security and privacy, user passwords are hashed and encrypted when they're checked against the database of leaked credentials.

## Version 87.0.664.52: November 30

Fixed various bugs and performance issues.

## Version 87.0.664.40: November 18

Fixed various bugs and performance issues.

## Version 87.0.664.36: November 16

Fixed various bugs and performance issues.

## Version 87.0.664.30: November 9

Fixed various bugs and performance issues.

## Version 87.0.664.24: November 2

Fixed various bugs and performance issues.

## Version 87.0.664.18: October 26

Fixed various bugs and performance issues.

<!-- begin major 87 -->
## Version 87.0.664.12: October 20

### Feature updates

- **Kiosk mode privacy features enabled**. Starting with Microsoft Edge version 87 kiosk mode features that help enterprises around the privacy of user data will be enabled. These features will enable experiences such as clear the user data on exit, delete downloaded files and to reset the configured start experience after a specified amount of idle time. Learn more about how to [Configure Microsoft Edge kiosk mode](./microsoft-edge-configure-kiosk-mode.md)
- **ClickOnce deployment enabled by default**. ClickOnce is enabled by default in Microsoft Edge 87, which reduces the barriers for enterprises to deploy software and better align with Microsoft Edge Legacy browser behavior. Starting in Microsoft Edge 87, the ClickOnceEnabled policy's "Not configured" state reflects the new default ClickOnce state of Enabled (as compared to the previous default state of Disabled).
- **The enterprise new tab page (NTP) integrates productivity with customizable, work-relevant feed content**. The enterprise NTP blends the Office 365 productivity page we offer to users signed in with their work or school account with personalized, work-relevant company and industry feeds that are organized in a single page. Users are able to recognize the familiar Office 365 content and Microsoft Search for Business powered by Bing. In addition, they can easily flip to a customizable "My Feed" with content and modules that are relevant to the user, their company, or their industry, and a selection of other feeds that the organization made available. [Learn more](/microsoft-365/admin/manage/manage-industry-news?preserve-view=true&view=o365-worldwide).

- **Privacy and Security:**

  - Support TLS Token Binding for policy-configured sites. TLS Token binding helps prevent token theft attacks to ensure that cookies can't be reused from a device other than the device upon which they were initially set. The use of TLS token binding requires setting the [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) policy and requires that the sites listed support this feature.

- **Keyboard support for highlighter on PDF files**. Users can use their keyboard keys to highlight any text on a PDF.

- **Printing:**

  - Choose which side to flip on when printing on both sides. Users can choose to flip on the long side or the short side of a sheet when printing on both sides.
  - Choose print rasterization mode for the enterprise. Control how Microsoft Edge prints to a non-PostScript printer on Windows. Sometimes print jobs on non-PostScript printers need to be rasterized to print correctly. The print options are "Full" and "Fast".

### Policy updates

#### New policies

Ten new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added.

- [ConfigureFriendlyURLFormat](./microsoft-edge-policies.md#configurefriendlyurlformat) - Configure the default paste format of URLs copied from Microsoft Edge, and determine if other formats are available to users.
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) - Shopping in Microsoft Edge Enabled.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](./microsoft-edge-policies.md#hideinternetexplorerredirectuxforincompatiblesitesenabled) - Hide the one-time redirection dialog and the banner on Microsoft Edge.
- [KioskAddressBarEditingEnabled](./microsoft-edge-policies.md#kioskaddressbareditingenabled) - Configure address bar editing for kiosk mode public browsing experience.
- [KioskDeleteDownloadsOnExit](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) - Delete files downloaded as part of kiosk session when Microsoft Edge closes.
- [PasswordRevealEnabled](./microsoft-edge-policies.md#passwordrevealenabled) - Enable the Password reveal button.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerpreventbhoinstall) - Prevent install of the BHO to redirect incompatible sites from Internet Explorer to Microsoft Edge.
- [RedirectSitesFromInternetExplorerRedirectMode](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerredirectmode) - Redirect incompatible sites from Internet Explorer to Microsoft Edge.
- [SpeechRecognitionEnabled](./microsoft-edge-policies.md#speechrecognitionenabled) - Configure Speech Recognition.
- [WebCaptureEnabled](./microsoft-edge-policies.md#webcaptureenabled) - Enable the web capture feature in Microsoft Edge.

#### Deprecated Policy

[NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype) - Configure the Microsoft Edge new tab page experience.

#### Obsoleted Policy

[EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures) - Re-enable deprecated web platform features for a limited time.

<!-- end major 87 -->

## Version 86.0.622.43: October 16

Fixed various bugs and performance issues.

## Version 86.0.622.36: October 7

Fixed various bugs and performance issues.

## Version 86.0.622.31: October 1

Fixed various bugs and performance issues.

## Version 86.0.622.28: September 28

Fixed various bugs and performance issues.

## Version 86.0.622.15: September 14

Fixed various bugs and performance issues.
<!-- major 86 -->
## Version 86.0.622.11: September 9

### Feature updates

* **Internet Explorer mode:**

   * Let users use the Microsoft Edge User Interface (UI) to test sites in Internet Explorer mode. Beginning with Microsoft Edge version 86, administrators can enable a UI option for their users to load a tab in Internet Explorer mode for testing purposes or as a stopgap until sites are added to the site list XML.

* **Delete downloads from disk using download manager.** Users are now able to delete their downloaded files from their disk without leaving the browser. The new Delete downloads functionality exists within the context menu of downloads shelf or the downloads page.

* **Roll back to previous Microsoft Edge version.** The rollback feature lets administrators revert to a known good version of Microsoft Edge if there's an issue in the latest version of Microsoft Edge.
[Learn more](edge-learnmore-rollback.md).

* **Enforce enabling Sync by default across the enterprise.**  Administrators can enable synchronization for Microsoft Entra accounts by default with the [ForceSync](./microsoft-edge-policies.md#forcesync) policy.

- **PDF updates:**

  * Table of contents for PDF Documents. Beginning with version 86, Microsoft Edge has added support for table of contents that lets users easily navigate through PDF documents.
  * Access all PDF functionalities on small form factor screens. Access all the capabilities of the Microsoft Edge PDF reader on devices with small screen sizes.
  * Pen support for highlighter on PDF files. With this update, users can use their digital pen to directly highlight text on PDF files, in the same way they would with a physical highlighter and paper.
  * Improved PDF scrolling. You'll now be able to experience stutter free scrolling while navigating through long PDF documents.

* **Automatic profile switching on Windows 7, 8, and 8.1.** The automatic profile switching currently available in Microsoft Edge on Windows 10 is extended to downlevel Windows (Windows 7, 8, and  8.1). For more information, see the [automatic profile switching](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) blog post.

* **Users will see auto complete suggestions when they start typing a search query on the Microsoft Edge Add-ons website.** Auto complete will help users quickly complete their search query without having to type the entire string. This is helpful because users won't have to remember correct spellings and they can choose from the available options that are displayed.

* **Remove the HTML5 Application Cache API.**  Beginning with Microsoft Edge version 86, the legacy Application Cache API that enables offline use of web pages is being removed from Microsoft Edge. Web Developers should review the [WebDev documentation](https://web.dev/appcache-removal/) for information on replacing  the Application Cache API with Service Workers.  Important: You can request an [AppCache OriginTrial Token](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) that allows sites to continue to use the deprecated Application Cache API until Microsoft Edge version 90.

* **Security:**

  * Secure DNS (DNS-over-HTTPS) Support.  Beginning with Microsoft Edge version 86, settings to control Secure DNS on unmanaged devices is available. These settings aren't accessible to users on managed devices, but IT admins can enable or disable Secure DNS using the [dnsoverhttpsmode](./microsoft-edge-policies.md#dnsoverhttpsmode) group policy.


* **Add a custom image to the New Tab Page (NTP) using a group policy.** Beginning with Microsoft Edge version 86 the NTP can replace the default image with a custom user-supplied image. The ability to manage the properties of this image is also supported by the group policy.

* **Match customized keyboard shortcuts to VS Code.** Microsoft Edge DevTools now supports customizing keyboard shortcuts in the DevTools to match with your editor/IDE. (In Microsoft Edge 84, we added the ability to match DevTools keyboard shortcuts to VS Code).

* **Replace [MetricsReportingEnabled](/DeployEdge/microsoft-edge-policies#metricsreportingenabled) and [SendSiteInformationToImproveServices](/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) policies for downlevel Windows and macOS.** These policies are deprecated in Microsoft Edge version 86 and will become obsolete in Microsoft Edge version 89.<br>
These policies are replaced by [Allow Telemetry](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) on Windows 10, and the new [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) policy for all other platforms. This will let users manage the diagnostic data that gets sent to Microsoft for Windows 7, 8, 8.1 and macOS.

* **SameSite=Lax Cookies By Default**. To improve web security and privacy, cookies will now default to [SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite) handling by default. This means that cookies will only be sent in a first-party context and will be omitted for requests sent to third-parties. This change can cause compatibility impact on websites that require cookies for third-party resources to function correctly. To permit such cookies, web developers can mark cookies which should be set from and sent to third-party contexts by adding explicit `SameSite=none` and `Secure` attributes when the cookie is set. Enterprises that wish to exempt certain sites from this change can do so using the [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) policy, or can opt out of the change across all sites using the [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled) policy.

### Policy updates

#### New policies

Nineteen new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [CollectionsServicesAndExportsBlockList](./microsoft-edge-policies.md#collectionsservicesandexportsblocklist) - Block access to a specified list of services and export targets in Collections.
- [DefaultSensorsSetting](./microsoft-edge-policies.md#defaultsensorssetting) - Default sensors setting.
- [DefaultSerialGuardSetting](./microsoft-edge-policies.md#defaultserialguardsetting) - Control use of the Serial API.
- [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) -  Send required and optional diagnostic data about browser usage.
- [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed) - Allow access to the Enterprise Mode Site List Manager tool.
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
- [URLBlocklist](./microsoft-edge-policies.md#urlblocklist) - Block access to a list of URLs.
- [URLAllowlist](./microsoft-edge-policies.md#urlallowlist) - Define a list of allowed URLs.
- [UserAgentClientHintsEnabled](./microsoft-edge-policies.md#useragentclienthintsenabled) - Enable the User-Agent Client Hints feature.
- [UserDataSnapshotRetentionLimit](./microsoft-edge-policies.md#userdatasnapshotretentionlimit) - Limits the number of user data snapshots retained for use in case of emergency rollback.

#### Deprecated Policies

- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - Enable usage and crash-related data reporting.
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - Send site information to improve Microsoft services.

#### Obsoleted Policy

[TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled) - Enable a TLS 1.3 security feature for local trust anchors.

#### Policy caption changed

[NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - Enable Native Window Occlusion.

#### Policy description changed

- [AdsSettingForIntrusiveAdsSites](./microsoft-edge-policies.md#adssettingforintrusiveadssites)
- [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls)
- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled)
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy)
- [AutoImportAtFirstRun](./microsoft-edge-policies.md#autoimportatfirstrun)
- [AutoOpenFileTypes](./microsoft-edge-policies.md#autoopenfiletypes)
- [BrowserSignin](./microsoft-edge-policies.md#browsersignin)
- [ClearBrowsingDataOnExit](./microsoft-edge-policies.md#clearbrowsingdataonexit) 
- [ClickOnceEnabled](./microsoft-edge-policies.md#clickonceenabled)
- [CommandLineFlagSecurityWarningsEnabled](./microsoft-edge-policies.md#commandlineflagsecuritywarningsenabled)
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin)
- [ConfigureShare](./microsoft-edge-policies.md#configureshare)
- [CookiesAllowedForUrls](./microsoft-edge-policies.md#cookiesallowedforurls)
- [CustomHelpLink](./microsoft-edge-policies.md#customhelplink)
- [DefaultCookiesSetting](./microsoft-edge-policies.md#defaultcookiessetting)
- [DefaultGeolocationSetting](./microsoft-edge-policies.md#defaultgeolocationsetting)
- [DefaultImagesSetting](./microsoft-edge-policies.md#defaultimagessetting)
- [DefaultInsecureContentSetting](./microsoft-edge-policies.md#defaultinsecurecontentsetting)
- [DefaultJavaScriptSetting](./microsoft-edge-policies.md#defaultjavascriptsetting)
- [DefaultNotificationsSetting](./microsoft-edge-policies.md#defaultnotificationssetting)
- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting)
- [DefaultPopupsSetting](./microsoft-edge-policies.md#defaultpopupssetting)
- [DefaultSearchProviderEnabled](./microsoft-edge-policies.md#defaultsearchproviderenabled)
- [DefaultWebBluetoothGuardSetting](./microsoft-edge-policies.md#defaultwebbluetoothguardsetting)
- [DefaultWebUsbGuardSetting](./microsoft-edge-policies.md#defaultwebusbguardsetting)
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload)
- [DeveloperToolsAvailability](./microsoft-edge-policies.md#developertoolsavailability)
- [EnableSha1ForLocalAnchors](./microsoft-edge-policies.md#enablesha1forlocalanchors)
- [DownloadRestrictions](./microsoft-edge-policies.md#downloadrestrictions)
- [EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures)
- [WinHttpProxyResolverEnabled](./microsoft-edge-policies.md#winhttpproxyresolverenabled)
- [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol)
- [ExternalProtocolDialogShowAlwaysOpenCheckbox](./microsoft-edge-policies.md#externalprotocoldialogshowalwaysopencheckbox)
- [ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist)
- [ForceBingSafeSearch](./microsoft-edge-policies.md#forcebingsafesearch)
- [ForceYouTubeRestrict](./microsoft-edge-policies.md#forceyoutuberestrict)
- [HomepageIsNewTabPage](./microsoft-edge-policies.md#homepageisnewtabpage)
- [HomepageLocation](./microsoft-edge-policies.md#homepagelocation)
- [InPrivateModeAvailability](./microsoft-edge-policies.md#inprivatemodeavailability)
- [InternetExplorerIntegrationEnhancedHangDetection](./microsoft-edge-policies.md#internetexplorerintegrationenhancedhangdetection)
- [InternetExplorerIntegrationLevel](./microsoft-edge-policies.md#internetexplorerintegrationlevel)
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect)
- [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled)
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled)
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout)
- [NetworkPredictionOptions](./microsoft-edge-policies.md#networkpredictionoptions)
- [NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation)
- [NewTabPageSearchBox](./microsoft-edge-policies.md#newtabpagesearchbox)
- [NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype)
- [NonRemovableProfileEnabled](./microsoft-edge-policies.md#nonremovableprofileenabled)
- [PasswordProtectionWarningTrigger](./microsoft-edge-policies.md#passwordprotectionwarningtrigger)
- [PasswordProtectionLoginURLs](./microsoft-edge-policies.md#passwordprotectionloginurls)
- [PasswordProtectionChangePasswordURL](./microsoft-edge-policies.md#passwordprotectionchangepasswordurl)
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls)
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls)
- [PreventSmartScreenPromptOverride](./microsoft-edge-policies.md#preventsmartscreenpromptoverride)
- [PreventSmartScreenPromptOverrideForFiles](./microsoft-edge-policies.md#preventsmartscreenpromptoverrideforfiles)
- [ProxyMode](./microsoft-edge-policies.md#proxymode)
- [RegisteredProtocolHandlers](./microsoft-edge-policies.md#registeredprotocolhandlers)
- [RelaunchNotification](./microsoft-edge-policies.md#relaunchnotification)
- [RestoreOnStartup](./microsoft-edge-policies.md#restoreonstartup)
- [RestoreOnStartupURLs](./microsoft-edge-policies.md#restoreonstartupurls)
- [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern)
- [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin)
- [SmartScreenAllowListDomains](./microsoft-edge-policies.md#smartscreenallowlistdomains)
- [SmartScreenEnabled](./microsoft-edge-policies.md#smartscreenenabled)
- [SmartScreenForTrustedDownloadsEnabled](./microsoft-edge-policies.md#smartscreenfortrusteddownloadsenabled)
- [SmartScreenPuaEnabled](./microsoft-edge-policies.md#smartscreenpuaenabled)
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled)
- [TrackingPrevention](./microsoft-edge-policies.md#trackingprevention)
- [WebRtcLocalhostIpHandling](./microsoft-edge-policies.md#webrtclocalhostiphandling)

<!-- end 86 -->

## Version 85.0.564.41: August 25

Fixed various bugs and performance issues.

## Version 85.0.564.40: August 21

Fixed various bugs and performance issues.

## Version 85.0.564.36: August 17

Fixed various bugs and performance issues.

## Version 85.0.564.30: August 10

Fixed various bugs and performance issues.

## Version 85.0.564.23: August 3

Fixed various bugs and performance issues.
<!-- major 85 -->
## Version 85.0.564.18: July 28

### Feature updates

- **On-premises synchronization of Favorites and Settings**. Now you can synchronize browser favorites and settings between Active Directory profiles within your own environment without the need for cloud sync.

- **Microsoft Edge group policy support for trusting site + app combos to launch without a confirmation prompt.** Group policy support added that lets administrators add site + app combos that are trusted to launch without the confirmation prompt. This adds the ability for administrators to configure trusted protocol/origin combinations (such as Microsoft 365 apps) for their end-users to suppress the confirmation prompt when navigating to a URL that contains an app protocol.

- **PDF Highlighter tool**. This tool can be added to the toolbar for PDFs to easily highlight important text.

- **The Storage Access API is available**. The Storage Access API allows access to first-party storage in a third-party context when a user has provided a direct intent to allow storage that would otherwise be blocked by the browser's current configuration. For more information, see [Storage Access API](https://www.chromestatus.com/feature/5612590694662144).

- **Send to OneNote is available for Microsoft Edge Collections**. Everyone's excited to be able to send the information they've gathered in Collections to OneNote, where they can append it to a larger project and collaborate with others! And even more importantly, in Microsoft Edge 85, you'll be able send content to *Office for Mac* products (Word, Excel, and OneNote) for both Microsoft account and Microsoft Entra ID.

- **DevTools updates**. For details about the following updates, see [What's New In DevTools (Microsoft Edge 85)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools).

   - Microsoft Edge DevTools supports Surface Duo emulation. The Microsoft Edge DevTools can emulate the Surface Duo so you can test how your web content will look on dual-screen devices. To turn on this experiment in DevTools, enter Device Mode by pressing Ctrl+Shift+M on Windows or Command+Shift+M on macOS, and then select Surface Duo from the device drop-down list.
   - Microsoft Edge DevTools lets you match keyboard shortcuts to VS Code. The Microsoft Edge DevTools supports customizing keyboard shortcuts in the DevTools to match your editor/IDE. In Microsoft Edge 85, we are adding the ability to match DevTools keyboard shortcuts to VS Code. This change will help increase productively across VS Code and DevTools.

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
- [TLSCipherSuiteDenyList](./microsoft-edge-policies.md#tlsciphersuitedenylist) - Specify the TLS cipher suites to disable.

#### Obsoleted policies

- [EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) - Enable Domain Actions Download from Microsoft.
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) - Re-enable Web Components v0 API until M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies)- Allow WebDriver to Override Incompatible Policies.

<!--- END ---->

## Version 84.0.522.35: July 9

Fixed various bugs and performance issues.

## Version 84.0.522.28: June 26

Fixed various bugs and performance issues.

## Version 84.0.522.26: June 24

Fixed various bugs and performance issues.

## Version 84.0.522.20: June 15

Fixed various bugs and performance issues.

## Version 84.0.522.15: June 8

Fixed various bugs and performance issues.

## Version 84.0.522.11: June 2

### Feature updates

- This version of Microsoft Edge provides improved site list download times for Internet Explorer mode.  We've reduced download delay for the Internet Explorer mode site list to 0 seconds (down from a 60-second wait) in the absence of a cached site list. We've also added group policy support for cases when Internet Explorer mode home page navigations need to be delayed until the site list is downloaded. For more information, see the [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload) policy.

- Microsoft Edge now allows users to sign-into the browser when it's "run as administrator" on Windows 10. This will help customers running Microsoft Edge on Windows server or in remote-desktop and sandbox scenarios.

- Microsoft Edge now provides full mouse support when in full screen mode. Now you can use your mouse to access tabs, the address bar, and other items without having to exit full screen mode.

- Online purchase improvement. Add custom nicknames to saved debit or credit cards. Now you can distinguish and differentiate your credit cards when making online purchases. Nicknaming your debit or credit cards lets you choose the correct card when using autofill to select a payment method.

- TLS/1.0 and TLS/1.1 are disabled by default. To help discover impacted sites, you can set the *edge://flags/#display-legacy-tls-warnings* flag to cause Microsoft Edge to display a non-blocking "Not Secure" notice when loading pages that require legacy TLS protocols. The [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin) policy permits re-enabling of TLS/1.0 and TLS/1.1. This policy will remain available until at least Microsoft Edge version 88. For more information, see [Site compatibility-impacting changes coming to Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

- Collections improvements:

  - A note capability is added that lets you add a note or comment to an item in a collection. Notes are grouped together and stay attached to an item even if you sort the items in a collection. To try this new feature, right-click on an item and select "Add note".
  - You can change the background color of notes in collections. You can use color coding to help you organize information and increase productivity.
  - There are noticeable performance improvements, which lets you export your collections to  Excel in less time than in previous versions of Microsoft Edge.

- Additional Microsoft Edge API support:

  - The Storage Access API. This API allows access to first-party storage in a third-party context when a user provides a direct intent to allow storage that would otherwise be blocked by the browser's current configuration.

    As privacy is becoming increasingly important to users, requests for stricter browser defaults and user opt-in settings like blocking all third-party storage access are increasingly common. While these settings help improve privacy and block unwanted access by unknown or untrusted parties, they can have unwanted side effects such as blocking access to content the user may want to view (for example, social media and embedded media content.)

  - The Native File System API, which means you can give sites permissions to edit files or folders via the Native File System API.

- PDF improvements:

  - Read Aloud for PDF lets users listen to PDF content while carrying out other tasks that may be important for them. It also helps audio visual learners focus on reading the content, making learning easier.
  - PDF file editing is improved. Now you can save an edit made to a PDF back to the file instead of saving a copy each time you edit the PDF.

- Microsoft Edge now enables Translation in the Immersive Reader. When a user opens the Immersive Reader view, they get the option to translate the page to their desired language.

- DevTools supports customizing keyboard shortcuts to match your editor/IDE, which includes VS Code.

### Policy updates

#### New policies

Five new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [AppCacheForceEnabled](./microsoft-edge-policies.md#appcacheforceenabled) - Allows the AppCache feature to be re-enabled, even if it's turned off by default.
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy) - Application Guard Container Proxy.
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload) - Require that the Enterprise Mode Site List is available before tab navigation.
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - Enable Hiding of Native Windows.
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout) - Set a timeout for delay of tab navigation for the Enterprise Mode Site List.

#### Deprecated policies

- [AllowSyncXHRInPageDismissal](./microsoft-edge-policies.md#allowsyncxhrinpagedismissal) - Allow pages to send synchronous XHR requests during page dismissal.
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) - Determines whether the built-in certificate verifier will be used to verify server certificates.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled) - Enable stricter treatment for mixed content.

#### Obsoleted policy

[ForceNetworkInProcess](./microsoft-edge-policies.md#forcenetworkinprocess) - Force networking code to run in the browser process.

<!-- end 84 -->

## Version 83.0.478.44: June 1

Fixed various bugs and performance issues.

## Version 83.0.478.37: May 20

Fixed various bugs and performance issues.

## Version 83.0.478.33: May 15

Fixed various bugs and performance issues.

## Version 83.0.478.28: May 7

Fixed various bugs and performance issues.

## Version 83.0.478.25: May 4

Fixed various bugs and performance issues.

## Version 83.0.478.18: April 27

Fixed various bugs and performance issues.

## Version 83.0.478.13: April 22

### Feature updates

- Microsoft Defender SmartScreen improvements: Made several improvements to the Microsoft Defender SmartScreen service, such as improved protection from malicious sites that redirect when loading, and top-level frame blocking, which completely replaces malicious sites with the Microsoft Defender SmartScreen safety page. The top-level frame blocking prevents audio and other media from the malicious site from playing which gives an easier and less confusing experience.

- In response to user feedback, users can now exempt certain cookies from automatically clearing when the browser closes. This option is helpful if there's a site that users don't want to be signed out of, but still want to have all the other cookies cleared when the browser closes. To use this feature, go to *edge://settings/clearBrowsingDataOnClose* and enable the "Cookies and other site data" toggle.

- Automatic Profile Switching is now available to help you get to your work content more easily across profiles. If you use multiple profiles at work, you can check it out by navigating to a site requiring authentication from your work or school account while on your personal profile. When we detect a change, you will receive a prompt to switch to your work profile to access that site without having to authenticate to it. When you choose the work profile you want to switch to, the website will open in your work profile. This profile switching capability will help you keep your work and personal data separate and help you get to your work content more effortlessly. If you don't want the feature to prompt you to switch profiles, you can choose the don't ask me again option and it will get out of your way.

- Collections feature improvements:
  - You can use drag and drop to add an item to a collection without opening the collection. During the drag and drop you can also choose a location in the collection list where you want to put the item.
  - You can add multiple items to a collection instead of adding one item at a time. To add multiple items, select the items and then drag them to a collection. Or you can select the items, right-click and then pick the collection where you want the items.

- You can add all the tabs in an Edge window into a new collection without adding them individually. To add all the tabs, right-click on any tab and choose "Add all tabs to a new collection".

- Extension sync is now available. You can now sync your extensions across all your devices! Extensions from both the Microsoft and Chrome Stores will sync with Microsoft Edge. To use this feature: Click the ellipses (**…**) on the menu bar, select **Settings**. Under Your profile, click **Sync** to see the Sync options. Under **Profiles/Sync** use the toggle to enable Extensions. You can use the [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) group policy to disable syncing of extensions.

- Improved the message on the Downloads management page for insecure downloads that have been blocked.

- Immersive Reader improvements:
  - Added support for Adverbs in the Parts of Speech experience we have in Immersive Reader. While reading an article within the Immersive Reader, open the Grammar Tools and switch on Adverbs within Parts of Speech to highlight all the adverbs on the page.
  - Added the ability to select any content on a webpage and open it in Immersive Reader. This ability enables users to use the Immersive Reader and all the Learning Tools, such as Line Focus and Read Aloud, across all websites.

- Link doctor provides host correction and a search query to the users when they mistype a URL. For example: <br>
A user mistypes "powerbi as "powerbbi".com. Link doctor will suggest "powerbi".com as a correction and create a link to search for "powerbbi" in case the user is looking for something different.

- Allow users to save their decision to launch an external protocol for a specific site. Users can configure the [ExternalProtocolDialogShowAlwaysOpenCheckbox](/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox) policy to enable or disable this feature.

- Users can set Microsoft Edge as their default browser directly from Microsoft Edge **Settings**. This capability makes it easier for users to change their default browser, within the context of the browser itself, instead of having to search through the operating system settings. To use this feature, go to *edge://settings/defaultBrowser* and click **Make default**.

- Several DevTools updates, including new remote debugging support, UI improvements, and more. For more information, see [What's New In DevTools (Microsoft Edge 83)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

### Policy updates

#### New policies

15 new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [AllowSurfGame](./microsoft-edge-policies.md#allowsurfgame) - Allow surf game.
- [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) - Configure the list of sites for which Microsoft Edge will attempt to establish a Token Binding with.
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

The following policy will continue to work in this release. It will become "obsolete" in a future release.

[EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) Enable Domain Actions Download from Microsoft

<!--  end 83 -->

## Version 81.0.416.60: April 20

Fixed various bugs and performance issues.

## Version 81.0.416.58: April 17

Security updates.

## Version 81.0.416.50: April 10

Fixed various bugs and performance issues.

## Version 81.0.416.45: April 3

Fixed various bugs and performance issues.

## Version 81.0.416.41: March 30

Fixed various bugs and performance issues.

## Version 81.0.416.34: March 17

Fixed various bugs and performance issues.

## Version 81.0.416.31: March 12

Fixed various bugs and performance issues.

## Version 81.0.416.28: March 9

Fixed various bugs and performance issues.

## Version 81.0.416.20: February 28

Fixed various bugs and performance issues.

## Version 81.0.416.12: February 20

### Feature updates

- Collections is now available. You can get started by clicking the Collections icon next to the address bar. This action opens the Collections pane where you can create, edit, and view Collections. We designed Collections based on what you do on the web. If you're a shopper, a traveler, a teacher, or a student, Collections can help. [Learn more](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97).

- Allow the removal (Hide from toolbar) of the Collections button from the Microsoft Edge toolbar for consistency.

- On-prem Active Directory account auto sign in will only be targeted to organizations that turn it on. If users were already signed in with an on-prem AD account, they will now be able to sign out of it. Now, users will only be automatically signed in with the primary account on their operating system if it is a Microsoft account or a Microsoft Entra account. Admins can enable auto sign in with an on-prem AD account using the ConfigureOnPremisesAccountAutoSignIn policy.

- Application Guard. Extensions support now available in the container.

- Added a message to inform users that Internet Explorer isn't installed when they navigate to a page that is configured to open in Internet Explorer mode.

- Updated the 3D View tool in Microsoft Edge DevTools with a new feature to help debug z-index stacking context. 3D View shows a representation of the DOM (Document Object Model) depth using color and stacking, and the z-Index view helps you isolate the different stacking contexts of your page. [Learn more](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/).

- Localized the F12 Dev tools in 10 new languages, so they will match the language used in the rest of the browser. [Learn more](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/).

- Added support for Dolby Vision playback. On Dolby Vision-enabled Windows 10 Build 17134 (April 2018 Update), websites can show Dolby vision content. See how to enable Dolby Vision content from [Netflix](https://help.netflix.com/en/node/42384).

- Microsoft Edge can now identify and remove duplicate favorites and merge folders with the same name. To access the tool, click the star on the browser's toolbar and select "Remove duplicate favorites".  You will be able to confirm changes and any updates to your favorites will be synced across devices.

- We heard from users it can be difficult to distinguish a normal browsing window in dark theme from an InPrivate window since both window frames are dark. The new solid InPrivate blue pill in the top right corner helps reassure users they are browsing InPrivate.

- Open external links in the correct browser profile. Select a default profile for links opened for external apps to open in from *edge://settings/multiProfileSettings*.

- Added a warning to alert users who sign into a browser profile with an account after being previously signed in with another account. This will help prevent unintentional data merging.

- If you have payment cards saved in your Microsoft account, you can use them in Microsoft Edge while filling out payment forms. The cards in your Microsoft account will sync across desktop devices and the full details will be shared with the website after two-factor authentication (CVC code and your Microsoft identity.) For further convenience, you can choose to securely save a copy of the card on the device during authentication.

- Line Focus is designed for users who like to focus on a limited part of the content as they read. It lets users keep the focus on 1, 3 or 5 lines at a time and dims out the rest of the page to let users read without distraction. Users can scroll using touch or arrow keys and the focus shifts accordingly.

- Microsoft Edge is now integrated with Windows Speller on Windows platforms 8.1 and above. This integration provides greater language support, with access to more language dictionaries and the ability to use Windows custom dictionaries. There is no further action needed from the users when a language has been added in the OS language settings and a language spellcheck toggle is enabled in Microsoft Edge settings.

- When PDF documents are opened using Microsoft Edge, users will now be able to create highlights, change color, and delete highlights. This helps in referencing important parts of the document later, and for collaboration.

- When loading long PDF documents that have been optimized for web, the pages being viewed by the user will be loaded faster, parallelly, while the rest of the document is loading.

- Now it's easier to start the Immersive Reader for a website by just pressing the F9 key.

- Now it's easier to start Read Aloud by using a keyboard shortcut (Ctrl + Shift + U).

### Policy updates

#### New policies

12 new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled) - Enable Ambient Authentication for InPrivate and Guest profiles. 
- [AudioSandboxEnabled](./microsoft-edge-policies.md#audiosandboxenabled) - Allow the audio sandbox to run.
- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) - Use a default referrer policy of no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](./microsoft-edge-policies.md#globallyscopehttpauthcacheenabled) - Enable globally scoped HTTP auth cache.
- [ImportExtensions](./microsoft-edge-policies.md#importextensions) - Allow importing of extensions.
- [ImportCookies](./microsoft-edge-policies.md#importcookies) - Allow importing of Cookies.
- [ImportShortcuts](./microsoft-edge-policies.md#importshortcuts) - Allow importing of shortcuts.
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect) - Specify how "in-page" navigations to unconfigured sites behave when started from Internet Explorer mode pages.
- [OmniboxMSBProviderEnabled](./microsoft-edge-policies.md) - Enable Microsoft Search for Business provider in omnibox.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled) - Enable stricter treatment for mixed content.
- [TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled) - Enable a TLS 1.3 security feature for local trust anchors.
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin) - Configure automatic sign in with an Active Directory domain account when there is no Microsoft Entra domain account.

#### Deprecated policies

The following policies continue to work in this release. They will become "obsolete" in a future release.

- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) - Re-enable Web Components v0 API until M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) - Allow WebDriver to Override Incompatible.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
