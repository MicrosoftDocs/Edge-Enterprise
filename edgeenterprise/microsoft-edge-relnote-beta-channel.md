---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 10/24/2024
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

## Version 131.0.2903.X: October X

Fixed various bugs and performance issues, Dev channel updates, feature updates, site compatibility impacting changes, and policy updates.

> [!NOTE]
> Portions of this release note are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).

### Dev Channel updates

The following Dev channel updates preceded this Beta channel release. These notes provide detailed information about the changes in each release.

- [Dev Channel update to 131.0.2863.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-131-0-2863-0-is-live/m-p/4260359)
- [Dev Channel update to 131.0.2875.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-131-0-2875-0-is-live/m-p/4267839)
- [Dev Channel update to 131.0.2889.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-131-0-2889-0-is-live/m-p/4273465)
- [Dev Channel update to 131.0.2903.5 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-131-0-2903-5-is-live/m-p/4277981)

### Feature updates

- **Cancel dialog for `beforeunload` event.** Microsoft Edge has changed the behavior of the cancel dialog for the `beforeunload` event. Calling `event.preventDefault` in a `beforeunload` event handler won't prevent the dialog from being shown. Instead, `event.returnValue = ''` needs to be called in the `beforeunload` event handler to prevent the cancel dialog. The [BeforeunloadEventCancelByPreventDefaultEnabled](/deployedge/microsoft-edge-policies?branch=pr-en-us-4908#beforeunloadeventcancelbypreventdefaultenabled) policy is obsolete and no longer works after Microsoft Edge version 130.

- **Get the latest updates effortlessly with instant update.** Instant update in Microsoft Edge ensures you get the latest browser updates automatically, when you step away from your computer. You can keep browsing, knowing that you already have the latest updates to keep you safe online. For more information, see [Get instant updates in Microsoft Edge - Microsoft Support](https://support.microsoft.com/microsoft-edge/get-instant-updates-in-microsoft-edge-4820adad-dd32-470c-9bd9-dba1de71a7f1). **Note:** This feature is in private preview for enterprise customers. Future feature updates will be available via Microsoft Edge release notes.

### Site compatibility impacting changes

- **CSS Anchor Positioning: anchor-scope.** The `anchor-scope` property allows limiting the visibility of anchor names to a given subtree.

- **CSS font-variant-emoji.** The `font-variant-emoji` CSS property provides a way to control between colored (emoji-style) and monochromatic (text-style) emoji glyphs. This method can be also done by adding an emoji Variation Selector, specifically U+FE0E for text and U+FE0F for emoji, after each emoji codepoint.

- **CSS highlight inheritance.** With CSS highlight inheritance, the CSS highlight pseudo-classes, such as `::selection` and `::highlight`, inherit their properties through the pseudo highlight chain, rather than the element chain. The result is a more intuitive model for inheritance of properties in highlights.

- **Improvements to styling structure of `<details>` and `<summary>` elements.** Support more CSS styling for the structure of `<details>` and `<summary>` elements to allow these elements to be used in more cases where disclosure widgets or accordion widgets are built on the web. In particular, this change removes restrictions that prevented setting the display property on these elements, and adds a `::details-content` pseudo-element to style the container for the part that expands and collapses.

- **`@page` margin boxes.** Add support for page margin boxes, when printing a web document, or exporting it as PDF.

  The `@page` margin boxes let you define the contents in the margin area of a page, for example to provide custom headers and footers, rather than using the built-in headers and footers generated by the browser.

  A margin box is defined using an at-rule inside a CSS `@page` rule. The appearance and the contents of a margin box are specified with CSS properties inside the `@page` rule, including the `content` property. Counters are also supported, for page numbering. The specification defines two special counter names: `page` for the current page number and `pages` for the total number of pages.

- **@property support `<string>` syntax.** Support for `<string>` syntax component name for registered custom properties.

- **Support `currentcolor` in relative color syntax.** Allow relative colors in CSS (using the `from` keyword) to use `currentcolor` as a base. This lets you set complementary colors, based on an element's text color, for that element's borders, shadows, or backgrounds.

  This feature also includes use cases where color functions are nested with a dependency on `currentcolor`, for example: `color-mix (in srgb, rgb(from currentcolor r g b), white)) or rgb(from rgb(from currentcolor 1 g b) b g r)`.

- **Support external SVG resources for `clip-path`, `fill`, `stroke`, and `marker-*` properties.** This feature adds support for external references for clip paths, markers, and paint servers (for the `fill` and `stroke` properties). For example, `clip-path: url("resources.svg#myPath")`.

- **Direct Sockets API.** Allows Isolated Web Apps to establish direct transmission control protocol (TCP) and user datagram protocol (UDP) communications with network devices and systems as well as listen to and accept incoming connections.

- **Exempt Speculation-Rules header from CSP restrictions.** Updates the integration between speculation rules and CSP so that CSP only applies to `<script type=speculationrules>`, and not to the `Speculation-Rules` header. CSP's script policies are meant to protect against injection of scripts into HTML, and the CSP threat model doesn't relate to HTTP headers. This approach allows easier deployment of speculation rules from CDNs and other edge servers.

- **FedCM as a trust signal for the Storage Access API.** Reconciles the FedCM and Storage Access APIs by making a prior FedCM grant a valid reason to automatically approve a storage access request.

  When a user grants permission to use their identity with a third-party identity provider (IdP) on a relying party (RP), many IdPs require third-party cookies to function correctly and securely. This proposal aims to satisfy that requirement in a private and secure manner by updating the Storage Access API (SAA) permission checks to not only accept the permission grant given by a storage access prompt, but also the permission grant given by a FedCM prompt.

  A key property of this mechanism is limiting the grant to cases explicitly allowed by the RP with the FedCM permissions policy, enforcing a per-frame control for the RP and preventing passive surveillance by the IdP beyond the capabilities that FedCM already grants.

- **COOP value noopener-allow-popups.** Some origins can contain different applications with different levels of security requirements. In those cases, it can be beneficial to prevent scripts running in one application from being able to open and script pages of another same-origin application.

  In such cases, it can be beneficial for a document to ensure its opener can't script it, even if the opener document is a same-origin one. The `noopener-allow-popups` Cross-Origin-Opener-Policy value lets documents define that behavior.

<!----
- **Private Aggregation API: increase contribution limit to 100 for Protected Audience callers.** Enables Protected Audience script runners to make up to 100 contributions per Private Aggregation report, compared to the current limit of 20.

  Private Aggregation limits the number of histogram contributions that can be embedded in a single aggregatable report, dropping any additional contributions. Shared Storage callers can work around the limit by invoking another Shared Storage operation. However, Protected Audience callers have no persistent storage, so they lose their excess contributions at the end of their auction. This change is privacy neutral as the API's contributions are still limited by the same privacy budget.

  Due to padding, each Protected Audience report has a larger payload, even if it didn't need the larger contribution limit. It's expected that these larger reports will increase the cost of operating the Aggregation Service.
--->
- **Select parser relaxation.** This change makes the HTML parser allow more tags in `<select>` besides `<option>`, `<optgroup>`, and `<hr>`.

  This change is in support of the customizable `<select>` feature but is being shipped first because it can be done separately and has some compat risk.

- **WebGPU: Clip distances.** Adds the optional GPU feature `clip-distances` that allows setting user-defined clip distances in vertex shader outputs. This technique is useful for the applications that need to clip all vertices in a scene that are beyond a user-defined plane, such as many CAD applications.

- **WebGPU: GPUCanvasContext getConfiguration()**. Once `GPUCanvasContext configure()` is called with a configuration dictionary, the `GPUCanvasContext getConfiguration()` method can be used to check the canvas context configuration. It includes GPU `device`, `format`, `usage`, `viewFormats`, `colorSpace`, `toneMapping`, and `alphaMode` members. As discussed in [issue 4828](https://github.com/gpuweb/gpuweb/issues/4828), web apps can use it to detect whether HDR canvas is supported in WebGPU.

- **WebHID on dedicated workers.** Enables WebHID inside dedicated worker contexts. This lets the performance of heavy I/O and processing of data from a HID device on a separate thread, helping to reduce the performance impact on the main thread.

- **WebRTC `RTCRtpEncodingParameters.scaleResolutionDownTo`.** An API that configures WebRTC encoders to scale input frames if they're greater than the specified `maxWidth` and `maxHeight`. This API is similar to `scaleResolutionDownBy` except that resolution constraints are expressed in absolute terms (for example, 640x360) as opposed to relative terms (for example, scale down by 2), avoiding race conditions related to changing input frame size on the fly.

- **Remove the CSS Anchor Positioning property `inset-area`.** With the CSS Working Group resolution on renaming the `inset-area` property to `position-area`, this removal cleans up the implementation for a standards compliant feature.

- **Remove non-standard GPUAdapter `requestAdapterInfo()` method.** The WebGPU Working Group decided it was impractical for `requestAdapterInfo()` to trigger a permission prompt so they've removed that option and replaced it with the GPUAdapter `info` attribute so that web developers can get the same `GPUAdapterInfo` value synchronously.

### Policy updates

#### New policies

- [EdgeSidebarAppUrlHostAllowList](/deployedge/microsoft-edge-policies#edgesidebarappurlhostallowlist) - Allow specific apps to be opened in Microsoft Edge sidebar
- [PrivateNetworkAccessRestrictionsEnabled](/deployedge/microsoft-edge-policies#privatenetworkaccessrestrictionsenabled) - Specifies whether to apply restrictions to requests to more private network endpoints

#### Deprecated policies

- [NewBaseUrlInheritanceBehaviorAllowed](/deployedge/microsoft-edge-policies#newbaseurlinheritancebehaviorallowed) - Allows enabling the feature NewBaseUrlInheritanceBehavior (deprecated)
- [RSAKeyUsageForLocalAnchorsEnabled](/deployedge/microsoft-edge-policies#rsakeyusageforlocalanchorsenabled) - Check RSA key usage for server certificates issued by local trust anchors (deprecated)
- [UserAgentClientHintsGREASEUpdateEnabled](/deployedge/microsoft-edge-policies#useragentclienthintsgreaseupdateenabled) - Control the User-Agent Client Hints GREASE Update feature (deprecated)

#### Obsoleted policies

- [BeforeunloadEventCancelByPreventDefaultEnabled](/deployedge/microsoft-edge-policies#beforeunloadeventcancelbypreventdefaultenabled) - Control the behavior for the cancel dialog produced by the beforeunload event (obsolete)
- [SignInCtaOnNtpEnabled](/deployedge/microsoft-edge-policies#signinctaonntpenabled) - Enable sign in click to action dialog (obsolete)

## Version 130.0.2849.52: October 23, 2024

Fixed various bugs and performance issues.

## Version 130.0.2849.46: October 17, 2024

Fixed various bugs and performance issues.

## Version 130.0.2849.43: October 16, 2024

Fixed various bugs and performance issues.

### Announcements

- **Cancel dialog for beforeunload event.** Microsoft Edge is changing the behavior of the cancel dialog for the `beforeunload` event in Microsoft Edge version 131. Starting in version 131, calling `event.preventDefault` in a `beforeunload` event handler won't prevent the dialog from being shown. Instead, `event.returnValue = ''` needs to be called in the `beforeunload` event handler to prevent the cancel dialog. The [BeforeunloadEventCancelByPreventDefaultEnabled](/deployedge/microsoft-edge-policies?branch=main&branchFallbackFrom=pr-en-us-4867#beforeunloadeventcancelbypreventdefaultenabled) policy is being obsoleted and will no longer work after Microsoft Edge version 130.

## Version 130.0.2849.35: October 11, 2024

Fixed various bugs and performance issues, feature updates, and policy updates.

### Feature updates

- **Copilot browser Context Policies.** The [EdgeEntraCopilotPageContext](/deployedge/microsoft-edge-policies#edgeentracopilotpagecontext) policy will be available starting from Microsoft Edge version 130 and will replace the [CopilotCDPPageContext](/deployedge/microsoft-edge-policies#copilotcdppagecontext) policy. The [CopilotCDPPageContext](/deployedge/microsoft-edge-policies#copilotcdppagecontext) policy is deprecated in Microsoft Edge version 130 and will be obsolete in Edge 133.

### Policy updates

#### New policies

- [EdgeEntraCopilotPageContext](/deployedge/microsoft-edge-policies#edgeentracopilotpagecontext) - Control access to page content for Entra ID Profiles accessing Microsoft Copilot with Enterprise Data Protection (EDP) from the Microsoft Edge sidebar.

#### Deprecated policies

- [CopilotCDPPageContext](/deployedge/microsoft-edge-policies#copilotcdppagecontext) - Control Copilot with Commercial Data Protection access to page context for Microsoft Entra ID profiles (deprecated).

## Version 130.0.2849.27: October 7, 2024

Fixed various bugs and performance issues.

### Policy updates

#### New policies

- [ImageEditorServiceEnabled](/deployedge/microsoft-edge-policies#imageeditorserviceenabled) - Enable the Designer for Image Editor feature

## Version 130.0.2849.13: September 30, 2024

Fixed various bugs and performance issues.

### Fixes

- Fixed an issue that caused rendering issues on some SharePoint sites.

## Version 130.0.2849.5: September 26, 2024

Fixed various bugs and performance issues, feature updates, site compatibility impacting changes, and policy updates.

> [!NOTE]
> Portions of this release note are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).

### Dev Channel updates

The following Dev channel updates preceded this Beta channel release. These notes provide detailed information about the changes in each release.

- [Dev Channel update to 130.0.2808.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-130-0-2808-0-is-live/m-p/4237117)
- [Dev Channel update to 130.0.2821.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-130-0-2821-1-is-live/m-p/4242634)
- [Dev Channel update to 130.0.2835.2 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-130-0-2835-2-is-live/m-p/4250520)
- [Dev Channel update to 130.0.2849.1 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-130-0-2849-1-is-live/m-p/4255515)

### Fixes

- Fixed an issue that prevented the briefcase icon from appearing on the *edge://settings/sidebar* page when Edge Bar was disabled using the [StandaloneHubsSidebarEnabled](/deployedge/microsoft-edge-policies#standalonehubssidebarenabled) policy.  

### Announcement

- **Live Captions.** The [LiveCaptionsAllowed](/deployedge/microsoft-edge-policies#livecaptionsallowed) policy was available since Microsoft Edge version 103 but this feature isn't generally available. Clients that have the [ExperimentationAndConfigurationServiceControl](/deployedge/microsoft-edge-policies#experimentationandconfigurationservicecontrol) policy set to 'FullMode' might receive the feature before broad availability. Broad availability will be announced via Microsoft Edge release notes.

### Feature updates

- **Token Binding.** Token Binding uses cryptographic certificates on both ends of the TLS connection in an attempt to close the security gap of bearer tokens, which may be lost or stolen. Token Binding is deprecated in Microsoft Edge version 130. Also, the [AllowTokenBindingForUrls](/deployedge/microsoft-edge-policies#allowtokenbindingforurls) policy is now obsolete.

- **Edge on macOS now seamlessly opens links in Teams.** When you set the default browser to Microsoft Edge on macOS and enable the feature, web links from the Teams desktop app are sent via chats, channels, calendar, and other entry points. These links seamlessly open automatically in the profile signed into Teams app and skips the need to reauthenticate in the browser. This feature makes it faster and easier to access content. Administrators can control the availability of this feature using the "Choose Which Browser Opens Web Links" Microsoft 365 policy. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Elevating top settings and improving settings page navigability.** To make finding browser settings more efficient, Microsoft Edge is introducing three navigation improvements to Edge Settings. We aren’t changing the functionality of any setting, and all the settings stay on the same page as they are today but will be behind clickable sections. These changes are as follows.

  - Introduce quick access to the most used Settings actions on the first place users land when entering Edge Settings (the Profiles page). Clicking the button with the name of the setting navigates users directly to its location.

  - Make densely populated Settings pages (such as *Privacy, search, and services*, *Appearance*, *Cookies and site permissions*, *System and performance*) easier to navigate by introducing quick access to the most used actions located on that page. Clicking the button with the name of the setting takes users directly to its location.

  - For these densely populated pages, each lengthy section of settings will be a clickable "table of contents" with descriptive subtexts. This helps users locate settings directly and avoid unnecessary scrolling.

  **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

### Site compatibility impacting changes

- **CSS Container Queries flat tree lookup.** The specification for container queries changed to look up flat tree ancestors. This change is only relevant for shadow DOM where an element will now be able to see non-named containers inside shadow trees into which the element or one of its ancestors is slotted, even if the CSS rule doesn't use `::part()` or `::slotted()`.

- **CSS Nesting: The nested declarations rule.** Keeps bare declarations following a nested rule in their place, by wrapping those declarations in `CSSNestedDeclarations` rules during parsing.

- **Full and unprefixed box-decoration-break support.** Adds support for `box-decoration-break:clone` both for inline fragmentation (line layout) and block fragmentation (pagination for printing and multicol).

  Previously, only `box-decoration-break:slice` (the initial value) was supported for block fragmentation, whereas for inline fragmentation, `box-decoration-break:clone` was also supported, but only when using the `prefixed -webkit-box-decoration-break` property.

- **Allow more pseudo-elements and pseudo-classes after ::part().** CSS selectors that use the `::part()` pseudo-element are allowed to have other CSS pseudo-elements (except `::part()`) and many types of other CSS pseudo-classes after them. Combinators are still not allowed after `::part()`, and pseudo-classes that depend on tree structure aren't allowed.

  Previously only a limited set of pseudo-classes and pseudo-elements after `::part()` was allowed. This change allows all of the pseudo-classes and pseudo-elements that should be allowed. It means selectors such as `::part(part-name):enabled` and `::part(part-name)::marker` are now allowed.

- **Compression dictionary transport with shared Brotli and shared Zstandard.** This feature adds support for using designated previous responses, as an external dictionary for content encoding compressing responses with Brotli or Zstandard.

  Enterprises might experience potential compatibility issues with enterprise network infrastructure that intercepts HTTPS traffic and is sensitive to unknown content encodings. The enterprise policy [CompressionDictionaryTransportEnabled](/deployedge/microsoft-edge-policies#compressiondictionarytransportenabled) is available to turn off the compression dictionary transport feature.

- **Concurrent smooth scrollIntoView().** The [scrollIntoView()](https://developer.mozilla.org/en-US/docs/Web/API/Element/scrollIntoView) method with behavior: "smooth" lets developers create scroll containers that scroll to their descendants with a gentle scroll animation. This feature fixes the implementation of the API so that ongoing scrollIntoView animations aren't canceled by unrelated scrolls on other scroll containers.

  The feature also fixes cases where Edge fails to scroll to a page's fragment anchor because of a competing scrollIntoView that is invoked when the page loads.

- **Document picture-in-picture: add option to ignore window bounds cache.** This change adds a new parameter (`preferInitialWindowPlacement`) to the document picture-in-picture API that, when set to true, hints to the user agent that it shouldn't try to reuse the position or size of the previous document picture-in-picture from this site when opening this one.

  Often, a document picture-in-picture window closes and reopens multiple times for the same site, such as moving a video conference to and from PiP. The user agent is free to reopen the PiP window at its most recent size and location, so that it stays where the user last moved it and provides continuity between the PiP windows. However, if the new window is semantically unrelated to the previous window, such as if it's a new video call, then the developer can use this parameter to provide a hint to the user agent that this window might be better opened in its default position and size instead.

- **Improved error reporting in IndexedDB for large value read failures.** Change to reporting for certain error cases that were previously reported with a DOMException and the message "Failed to read large IndexedDB value."

  Now a DOMException is raised with the name "NotFoundError" when the file containing the data being read by an IDBRequest is missing from the disk so that sites can take the appropriate corrective action when an unrecoverable failure occurs. Corrective actions could include deleting the entry from the DB, notifying the user, or re-fetching the data from servers.

- **Keyboard focusable scroll containers.** This feature makes scrollers without focusable children keyboard-focusable by default.

  This is an important improvement to help make scrollers and contents within scrollers more accessible to all users. Keyboard focusable scrollers are enabled by default starting in version 130.

  If more time is needed to implement this feature, the [KeyboardFocusableScrollersEnabled](/deployedge/microsoft-edge-policies#keyboardfocusablescrollersenabled) policy is available starting with Edge 128.

- **Support non-special scheme URLs.** Previously, the URL parser didn't support non-special URLs. The parser parses non-special URLs as if they had an "opaque path," which isn't aligned with the URL Standard. Now, the URL parser parses non-special URLs correctly, following the URL Standard.

  See [bit.ly/url-non-special](https://docs.google.com/document/d/1LjxHl32fE4tCKugrK_PIso7mfXQVEeoD1wSnX2y0ZU8/edit?resourcekey=0-d1gP4X2sG7GPl9mlTeptIA#heading=h.voahsyj6c2dh) for more details.

- **WebAssembly JavaScript String Builtins.** This feature exposes common JavaScript string operations for import into WebAssembly. This lets you create and manipulate JavaScript strings from WebAssembly without support within WebAssembly. This still allows for a similar performance as supported string references.

- **WebGPU: Dual source blending.** Adds the optional GPU feature "dual-source-blending" that enables combining two fragment shader outputs into a single framebuffer. This technique is useful for applications that require complex blending operations, such as those based on Porter-Duff blend modes. By reducing the need for frequent pipeline state object changes, dual source blending can enhance performance and flexibility.

- **Web Serial: connected attribute and RFCOMM connection events.** This feature adds a boolean `SerialPort.connected` attribute. The attribute returns true if the serial port is logically connected. For wired serial ports, a port is logically connected if the port is physically attached to the system. For wireless serial ports, a port is logically connected if the device hosting the port has any open connections to the host.

  Previously, only wired serial ports dispatched connect and disconnect events. With this feature, Bluetooth RFCOMM serial ports dispatch these events when the port becomes logically connected or disconnected.

  This feature is intended to allow applications to detect when a Bluetooth RFCOMM serial port is available without opening the port.

- **Remove expectedImprovement in DelegatedInkTrailPresenter.** The expectedImprovement attribute tells web developers how much improvement the DelegatedInkTrails API will provide to their current ink latency. However, this attribute isn't worth the increase to fingerprinting entropy.

- **Deprecate non-standard GPUAdapter requestAdapterInfo() method.** The `requestAdapterInfo()` asynchronous method in WebGPU is redundant because developers can already get GPUAdapterInfo synchronously using the GPUAdapter info attribute.

### Policy updates

#### Obsoleted policies

- [AllowTokenBindingForUrls](/deployedge/microsoft-edge-policies#allowtokenbindingforurls) - Configure the list of sites for which Microsoft Edge will attempt to establish a Token Binding with (obsolete).

## Version 129.0.2792.52: September 19, 2024

Fixed various bugs and performance issues.

## Version 129.0.2792.50: September 18, 2024

Fixed various bugs and performance issues.

## Version 129.0.2792.41: September 13, 2024

Fixed various bugs and performance issues.

## Version 129.0.2792.31: September 9, 2024

Fixed various bugs and performance issues.

## Version 129.0.2792.21: September 3, 2024

Fixed various bugs and performance issues.

## Version 129.0.2792.12: August 29, 2024

Fixed various bugs and performance issues, feature updates.

### Dev Channel updates

The following Dev channel updates preceded this Beta channel release. These notes provide detailed information about the changes in each release.

- [Dev Channel update to 129.0.2752.4 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-129-0-2752-4-is-live/m-p/4215208)
- [Dev Channel update to 129.0.2766.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-129-0-2766-0-is-live/m-p/4218361)
- [Dev Channel update to 129.0.2779.0 is live. - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/articles/dev-channel-update-to-129-0-2779-0-is-live/m-p/4226574)

### Fixes

- **Policy updates to allow wildcards.** The documentation for the following policies were inaccurate and were corrected. These policies support wildcards (*) in URL patterns when being configured: [ImagesAllowedForUrls](/deployedge/microsoft-edge-policies#imagesallowedforurls), [ImagesBlockedForUrls](/deployedge/microsoft-edge-policies#imagesblockedforurls), [InsecureContentAllowedForUrls](/deployedge/microsoft-edge-policies#insecurecontentallowedforurls), [InsecureContentBlockedForUrls](/deployedge/microsoft-edge-policies#insecurecontentblockedforurls), [PopupsAllowedForUrls](/deployedge/microsoft-edge-policies#popupsallowedforurls), [PopupsBlockedForUrls](/deployedge/microsoft-edge-policies#popupsblockedforurls).

### Feature updates

- **Update to Microsoft Edge supported operating systems.** The minimum supported macOS version is increased to macOS 11. Users on older versions of macOS will no longer receive Microsoft Edge updates. For more information, see [Microsoft Edge Supported Operating Systems](/DeployEdge/microsoft-edge-supported-operating-systems).

- **Deprecation of the CryptoWallet feature.** To improve end user experience, the CryptoWallet feature and the [CryptoWalletEnabled](/deployedge/microsoft-edge-policies#cryptowalletenabled) policy is deprecated. The [CryptoWalletEnabled](/deployedge/microsoft-edge-policies#cryptowalletenabled) policy will be obsolete in an upcoming release.

- **Microsoft Edge sidebar updates.** For inactive sidebar users and new Microsoft Edge users, the sidebar is turned OFF. Users can always return to the **Settings** > **Sidebar** and turn the sidebar ON again at any time. For active sidebar users, the current sidebar state remains the same.
  
  Administrators can control the availability of the sidebar using the [HubsSidebarEnabled](/deployedge/microsoft-edge-policies#hubssidebarenabled) policy. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

### Policy updates

#### Deprecated policies

- [CryptoWalletEnabled](/deployedge/microsoft-edge-policies#cryptowalletenabled)  - Enable CryptoWallet feature (deprecated)
- [EnhanceSecurityModeOptOutUXEnabled](/deployedge/microsoft-edge-policies#enhancesecuritymodeoptoutuxenabled)  - Manage opt-out user experience for Enhanced Security Mode (ESM) in Microsoft Edge (deprecated)

<!--=========================== archived =================================-->
<!-- Version 128.0.2739.42: August 22, 2024 to Version 128.0.2739.5: August 1, 2024 -->
<!-- Version 127.0.2651.74: July 25, 2024 to Version 127.0.2651.8: June 21, 2024 -->
<!-- Version 126.0.2592.68: June 20, 2024 to Version 126.0.2592.13: May 23, 2024 -->
<!-- Version 125.0.2535.51: May 17, 2024 to Version 125.0.2535.13: April 29, 2024 -->
<!-- Version 124.0.2478.67: April 26, 2024 to Version 124.0.2478.10: March 28, 2024 -->
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
