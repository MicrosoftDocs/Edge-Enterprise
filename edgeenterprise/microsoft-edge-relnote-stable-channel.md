---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 10/15/2024
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

## Version 130.0.xxxx.xx: October x, 2024

Fixed various bugs and performance issues, Dev channel updates, announcements, feature updates, site compatibility impacting changes, and policy updates.

> [!NOTE]
> Portions of this release note are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).

### Dev Channel updates

The following Dev channel updates preceded this Stable channel release. The following Dev notes provide detailed information about the changes in each release.

- [Dev Channel update to 130.0.2808.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-130-0-2808-0-is-live/m-p/4237117)
- [Dev Channel update to 130.0.2821.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-130-0-2821-1-is-live/m-p/4242634)
- [Dev Channel update to 130.0.2835.2 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-130-0-2835-2-is-live/m-p/4250520)
- [Dev Channel update to 130.0.2849.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-130-0-2849-1-is-live/m-p/4255515)

### Fixes

- Fixed an issue that prevented the briefcase icon from appearing on the *edge://settings/sidebar* page when Edge Bar was disabled using the [StandaloneHubsSidebarEnabled](/deployedge/microsoft-edge-policies#standalonehubssidebarenabled) policy.

- Fixed an issue that caused rendering issues on some SharePoint sites.

### Announcements

- **Live Captions.** The [LiveCaptionsAllowed](/deployedge/microsoft-edge-policies#livecaptionsallowed) policy was available since Microsoft Edge version 103 but this feature isn't generally available. Clients that have the [ExperimentationAndConfigurationServiceControl](/deployedge/microsoft-edge-policies#experimentationandconfigurationservicecontrol) policy set to 'FullMode' might receive the feature before broad availability. Broad availability will be announced via Microsoft Edge release notes.

- **Cancel dialog for beforeunload event.** Microsoft Edge is changing the behavior of the cancel dialog for the `beforeunload` event in Microsoft Edge version 131. Starting in version 131, calling `event.preventDefault` in a `beforeunload` event handler won't prevent the dialog from being shown. Instead, `event.returnValue = ''` needs to be called in the `beforeunload` event handler to prevent the cancel dialog. The [BeforeunloadEventCancelByPreventDefaultEnabled](/deployedge/microsoft-edge-policies#beforeunloadeventcancelbypreventdefaultenabled) policy is being obsoleted and will no longer work after Microsoft Edge version 130.

### Feature updates

- **Token Binding.** Token Binding uses cryptographic certificates on both ends of the TLS connection in an attempt to close the security gap of bearer tokens, which may be lost or stolen. Token Binding is deprecated in Microsoft Edge version 130. Also, the [AllowTokenBindingForUrls](/deployedge/microsoft-edge-policies#allowtokenbindingforurls) policy is now obsolete.

- **Copilot browser Context Policies.** The [EdgeEntraCopilotPageContext](/deployedge/microsoft-edge-policies#edgeentracopilotpagecontext) policy will be available starting from Microsoft Edge version 130 and will replace the [CopilotCDPPageContext](/deployedge/microsoft-edge-policies#copilotcdppagecontext) policy. The [CopilotCDPPageContext](/deployedge/microsoft-edge-policies#copilotcdppagecontext) policy is deprecated in Microsoft Edge version 130 and will be obsolete in Edge 133.

- **Elevating top settings and improving settings page navigability.** To make finding browser settings more efficient, Microsoft Edge is introducing three navigation improvements to Edge Settings. We aren’t changing the functionality of any setting, and all the settings stay on the same page as they are today but will be behind clickable sections. These changes are as follows.

  - Introduce quick access to the most used Settings actions on the first place users land when entering Edge Settings (the Profiles page). Clicking the button with the name of the setting navigates users directly to its location.

  - Make densely populated Settings pages (such as *Privacy, search, and services*, *Appearance*, *Cookies and site permissions*, *System and performance*) easier to navigate by introducing quick access to the most used actions located on that page. Clicking the button with the name of the setting takes users directly to its location.

  - For these densely populated pages, each lengthy section of settings will be a clickable "table of contents" with descriptive subtexts. This helps users locate settings directly and avoid unnecessary scrolling.

  **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

### Site compatibility impacting changes

### Policy updates

#### New policies

- [EdgeEntraCopilotPageContext](/deployedge/microsoft-edge-policies#edgeentracopilotpagecontext) - Control access to page content for Entra ID Profiles accessing Microsoft Copilot with Enterprise Data Protection (EDP) from the Microsoft Edge sidebar
- [ImageEditorServiceEnabled](/deployedge/microsoft-edge-policies#imageeditorserviceenabled) - Enable the Designer for Image Editor feature
- [PrivateNetworkAccessRestrictionsEnabled](/deployedge/microsoft-edge-policies#privatenetworkaccessrestrictionsenabled) - Specifies whether to apply restrictions to requests to more private network endpoints

#### Deprecated policies

- [CopilotCDPPageContext](/deployedge/microsoft-edge-policies#copilotcdppagecontext) - Control Copilot with Commercial Data Protection access to page context for Microsoft Entra ID profiles (deprecated)
- [NewBaseUrlInheritanceBehaviorAllowed](/deployedge/microsoft-edge-policies#newbaseurlinheritancebehaviorallowed) - Allows enabling the feature NewBaseUrlInheritanceBehavior (deprecated)
- [RSAKeyUsageForLocalAnchorsEnabled](/deployedge/microsoft-edge-policies#rsakeyusageforlocalanchorsenabled) - Check RSA key usage for server certificates issued by local trust anchors (deprecated)
- [UserAgentClientHintsGREASEUpdateEnabled](/deployedge/microsoft-edge-policies#useragentclienthintsgreaseupdateenabled) - Control the User-Agent Client Hints GREASE Update feature (deprecated)

#### Obsoleted policies

- [AllowTokenBindingForUrls](/deployedge/microsoft-edge-policies#allowtokenbindingforurls) - Configure the list of sites for which Microsoft Edge will attempt to establish a Token Binding with (obsolete)

## Version 129.0.2792.89: October 10, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-10-2024).

## Version 128.0.2739.113: October 10, 2024

Fixed various bugs and performance issues for Extended Stable channel.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-10-2024).

## Version 129.0.2792.79: October 3, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-3-2024).

## Version 128.0.2739.107: October 3, 2024

Fixed various bugs and performance issues for Extended Stable channel.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-3-2024).

## Version 128.0.2739.97: September 26, 2024

Fixed various bugs and performance issues for Extended Stable channel.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-26-2024).

## Version 129.0.2792.65: September 26, 2024

Fixed various bugs and performance issues, and feature updates.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-26-2024).

### Feature updates

- **Microsoft Edge sidebar updates.** For inactive sidebar users and new Edge users, the sidebar is turned OFF. Users can always return to **Settings > Sidebar** and turn the sidebar ON again at any time. For active sidebar users, the current sidebar state stays the same.
  
  Administrators can control the availability of the sidebar using the [HubsSidebarEnabled](/deployedge/microsoft-edge-policies#hubssidebarenabled) policy.

## Version 128.0.2739.90: September 19, 2024

Fixed various bugs and performance issues Extended Stable channel.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-19-2024).

## Version 129.0.2792.52: September 19, 2024

Fixed various bugs and performance issues, feature updates, site impacting compatibility changes, and policy updates.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-19-2024).

> [!NOTE]
> Portions of this release note are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).

### Dev Channel updates

The following Dev channel updates preceded this Stable channel release. The following Dev notes provide detailed information about the changes in each release.

- [Dev Channel update to 129.0.2752.4 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-129-0-2752-4-is-live/m-p/4215208)
- [Dev Channel update to 129.0.2766.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-129-0-2766-0-is-live/m-p/4218361)
- [Dev Channel update to 129.0.2779.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-129-0-2779-0-is-live/m-p/4226574)
- [Dev Channel update to 129.0.2792.10 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-129-0-2792-10-is-live/m-p/4232423)

### Fixes

- **Policy updates to allow wildcards.** The documentation for the following policies were inaccurate and were corrected. These policies support wildcards (*) in URL patterns when being configured: [ImagesAllowedForUrls](/deployedge/microsoft-edge-policies#imagesallowedforurls), [ImagesBlockedForUrls](/deployedge/microsoft-edge-policies#imagesblockedforurls), [InsecureContentAllowedForUrls](/deployedge/microsoft-edge-policies#insecurecontentallowedforurls), [InsecureContentBlockedForUrls](/deployedge/microsoft-edge-policies#insecurecontentblockedforurls), [PopupsAllowedForUrls](/deployedge/microsoft-edge-policies#popupsallowedforurls), [PopupsBlockedForUrls](/deployedge/microsoft-edge-policies#popupsblockedforurls).

### Feature updates

- **Update to Microsoft Edge supported operating systems.** The minimum supported macOS version is increased to macOS 11. Users on older versions of macOS will no longer receive Microsoft Edge updates. For more information, see [Microsoft Edge Supported Operating Systems](/DeployEdge/microsoft-edge-supported-operating-systems).

- **Deprecation of the CryptoWallet feature.** To improve end user experience, the CryptoWallet feature and the [CryptoWalletEnabled](/deployedge/microsoft-edge-policies#cryptowalletenabled) policy is deprecated. The [CryptoWalletEnabled](/deployedge/microsoft-edge-policies#cryptowalletenabled) policy will be obsolete in an upcoming release.

### Site compatibility impacting changes

- **Deprecation of non-standard declarative shadow DOM serialization.** The prototype implementation, which shipped in 2020 and then updated in 2023, contained a method called `getInnerHTML()` that could be used to serialize DOM trees containing shadow roots. That part of the prototype wasn't standardized with the rest of the declarative shadow DOM, and has only recently reached spec consensus (for details, see [GitHub](https://github.com/whatwg/html/issues/8867). As part of that consensus, the shape of the `getInnerHTML` API changed.

- **Deprecate the includeShadowRoots argument on DOMParser.** The `includeShadowRoots` argument was a never-standardized argument to the `DOMParser.parseFromString()` function, which was there to allow imperative parsing of HTML content that contains declarative shadow DOM. This function was shipped as part of the initial shipment of declarative shadow DOM. Since the standards discussion rematerialized in 2023, the shape of DSD APIs changed, including this feature for imperative parsing.

  Now that a standardized version of this API, in the form of `setHTMLUnsafe()` and `parseHTMLUnsafe()` shipped, the non-standard `includeShadowRoots` argument needs to be deprecated and removed. All usage should shift accordingly:

  Instead of:

  `(new DOMParser()).parseFromString(html,'text/html',{includeShadowRoots: true});`

  This can be used instead:

  `document.parseHTMLUnsafe(html);`

- **Rename inset-area to position-area**. The CSS working group ([CSSWG](https://www.w3.org/groups/wg/css/)) resolved to rename this property from `inset-area` to `position-area`. For more information, see the CSSWG discussion in [GitHub](https://github.com/w3c/csswg-drafts/issues/10209#issuecomment-2221005001).

  The old and new property names are supported for a few milestones, to help developers migrate to the new position-area name. We're shipping the new property name, `position-area`, as a synonym for `inset-area`.

  The `inset-area` property is currently planned for removal in Microsoft Edge version 131.

### Policy updates

#### New policies

- [PrintingLPACSandboxEnabled](/deployedge/microsoft-edge-policies#printinglpacsandboxenabled) - Enable Printing LPAC Sandbox

#### Deprecated policies

- [CryptoWalletEnabled](/deployedge/microsoft-edge-policies#cryptowalletenabled) - Enable CryptoWallet feature (deprecated)
- [EnhanceSecurityModeOptOutUXEnabled](/deployedge/microsoft-edge-policies#enhancesecuritymodeoptoutuxenabled) - Manage opt-out user experience for Enhanced Security Mode (ESM) in Microsoft Edge (deprecated)

## Version 128.0.2739.79: September 12, 2024

Fixed various bugs and performance issues, improved reliability.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-12-2024).

### Fixes

- Fixed an issue that caused deployed pinned Shortcuts to the Taskbar to be duplicated.

### Improved reliability

- Fixed a browser crash that occurred when trying to launch a custom protocol from a web page when using the [URLAllowlist](/deployedge/microsoft-edge-policies#urlallowlist) policy on a managed device.

## Version 128.0.2739.67: September 5, 2024

Fixed various bugs and performance issues.

## Version 128.0.2739.63: September 3, 2024

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-3-2024).

### Fixes

- Fixed an issue that prevented pages from fully loading when retrieving resources from the HTTP cache and DevTools showed the requests failing with net::ERR_FAILED.

## Version 128.0.2739.54: August 29, 2024

Fixed various bugs and performance issues, feature updates.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-29-2024).

### Fixes

- Fixed an issue that caused custom configured start pages to be stuck in the loading state.

### Feature updates

- **Security setting in the Microsoft Edge management service.** The Microsoft Edge management service gives admins a dedicated experience to manage specific settings that help improve the security posture of their managed browser instances.


## Version 128.0.2739.42: August 22, 2024

Fixed various bugs and performance issues, feature updates, and policy updates.

> [!IMPORTANT]
> This update to Stable channel contains a fix for [CVE-2024-7971](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2024-7971) and [CVE-2024-7965](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2024-7965), which have been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-22-2024).

### Dev Channel updates

The following Dev channel updates preceded this Stable channel release. The following Dev notes provide detailed information about the changes in each release.

- [Dev Channel update to 128.0.2661.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-128-0-2661-0-is-live/m-p/4176024)
- [Dev Channel update to 128.0.2677.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-128-0-2677-1-is-live/m-p/4182622)
- [Dev Channel update to 128.0.2690.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-128-0-2690-1-is-live/m-p/4188392)
- [Dev Channel update to 128.0.2708.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-128-0-2708-0-is-live/m-p/4194430)
- [Dev Channel update to 128.0.2730.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-128-0-2730-0-is-live/m-p/4200632)
- [Dev Channel update to 128.0.2739.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-128-0-2739-1-is-live/m-p/4206617)

### Fixes

- Fixed an issue that caused high CPU usage of renderer processes when running Selenium tests and calling `driver.quit()` to end the testing session.

### Feature updates

- **SSE3 Requirement.**  Microsoft Edge stopped supporting CPUs that lack SSE3. Devices with such CPUs won't receive any more updates. For more information, see [Microsoft Edge Supported Operating Systems](/deployedge/microsoft-edge-supported-operating-systems).

- **Copilot browser Context Policies.** The [DiscoverPageContextEnabled](/deployedge/microsoft-edge-policies#discoverpagecontextenabled) policy is obsoleted in Microsoft Edge version 128 and doesn't work after Microsoft Edge 127.

  To summarize and answer questions based on browser context in Microsoft Edge, Copilot needs to be able to access the browser context. We're providing two new policies to offer more flexibility for admins to customize Edge browser context access across Copilot chats in Edge sidebar.

  - [CopilotPageContext](/deployedge/microsoft-edge-policies#copilotpagecontext) - Control Copilot access to browser context for Microsoft Entra ID profiles.
  - [CopilotCDPPageContext](/deployedge/microsoft-edge-policies#copilotcdppagecontext) - Control Copilot with Commercial Data Protection access to browser context for Microsoft Entra ID profiles.

- **Deprecation of the followable web feature.** To improve end user experience, the followable web feature is deprecated. The [EdgeFollowEnabled](/deployedge/microsoft-edge-policies#edgefollowenabled) policy is also obsolete.

- **EnforceLocalAnchorConstraintsEnabled policy obsoletion.** The [EnforceLocalAnchorConstraintsEnabled](/deployedge/microsoft-edge-policies#enforcelocalanchorconstraintsenabled) policy was previously deprecated and is now obsolete in Edge version 128. Since Microsoft Edge 112, constraints in certificates loaded from the platform certificate store are enforced. The [EnforceLocalAnchorConstraintsEnabled](/deployedge/microsoft-edge-policies#enforcelocalanchorconstraintsenabled) policy existed as a temporary opt-out in case an enterprise encountered issues with the constraints encoded in their private roots.

- **New Policy for Insecure Downloads over HTTP.** Users that download potentially dangerous content on HTTP sites will receive a UI warning in a future Microsoft Edge version. To prepare for this change, the [ShowDownloadsInsecureWarningsEnabled](/deployedge/microsoft-edge-policies#showdownloadsinsecurewarningsenabled) policy is now available for admins to enable or disable the warnings related to insecure downloads

- **Edge Bar improvements.** Edge Bar, the detachable version of the Edge sidebar in Windows 10, has a changed entry point from the gear icon at the bottom of the Edge sidebar's fly out menu to the *edge://settings/sidebar* page.  

  For Windows 11 and Windows 10 users, clicking the gear icon will now automatically open the *edge://settings/sidebar* page.

  Also, the ability for Edge Bar to start automatically when starting a Windows 10 device has been enabled again, the Close "X" icon has been moved below the ellipsis menu at the bottom right corner of Edge Bar, and Copilot in Edge will remain within the browser not in Edge Bar. **Note:** These features are a controlled feature rollout. If you don't see these features, check back as we continue our rollout.

  Disabling Edge Bar through the [StandaloneHubsSidebarEnabled](/deployedge/microsoft-edge-policies#standalonehubssidebarenabled) policy continues to work, there's a fix to make the UI and briefcase icon appear on the *edge://settings/sidebar* page coming soon.

### Policy updates

#### New policies

- [ApplicationBoundEncryptionEnabled](/deployedge/microsoft-edge-policies#applicationboundencryptionenabled) - Enable Application Bound Encryption
- [DynamicCodeSettings](/deployedge/microsoft-edge-policies#dynamiccodesettings) - Dynamic Code Settings
- [ExtensionDeveloperModeSettings](/deployedge/microsoft-edge-policies#extensiondevelopermodesettings) - Control the availability of developer mode on extensions page
- [ExtensionExtendedBackgroundLifetimeForPortConnectionsToUrls](/deployedge/microsoft-edge-policies#extensionextendedbackgroundlifetimeforportconnectionstourls) - Configure a list of origins that grant an extended background lifetime to connecting extensions.
- [KeyboardFocusableScrollersEnabled](/deployedge/microsoft-edge-policies#keyboardfocusablescrollersenabled) - Enable keyboard focusable scrollers
- [ShowDownloadsInsecureWarningsEnabled](/deployedge/microsoft-edge-policies#showdownloadsinsecurewarningsenabled) - Enable insecure download warnings

#### Obsoleted policies

- [DiscoverPageContextEnabled](/deployedge/microsoft-edge-policies#discoverpagecontextenabled) - Enable Discover access to page contents for AAD profiles (obsolete)
- [EnforceLocalAnchorConstraintsEnabled](/deployedge/microsoft-edge-policies#enforcelocalanchorconstraintsenabled) - Determines whether the built-in certificate verifier will enforce constraints encoded into trust anchors loaded from the platform trust store (deprecated)
- [SiteSafetyServicesEnabled](/deployedge/microsoft-edge-policies#sitesafetyservicesenabled) - Allow users to configure Site safety services (obsolete)

<!-- ===================== snip for archive ========================== -->
<!-- Version 127.0.2651.105: August 15, 2024 to Version 127.0.2651.74: July 25, 2024 --->
<!-- Version 126.0.2592.113: July 18, 2024 to Version 126.0.2592.61: June 17, 2024 --->
<!-- Version 124.0.2478.109: May 16, 2024 to Version 124.0.2478.51: April 18, 2024 -->
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
