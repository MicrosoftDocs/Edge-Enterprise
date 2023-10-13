---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 10/13/2023
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
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

## Version 118.0.2088.46: October 13, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#october-13-2023).

### Announcement: Icon change in Edge sidebar

In an upcoming update to Microsoft Edge, the Bing icon entry point in the Microsoft Edge sidebar will change to the new Copilot icon. No other changes in the experience are expected.

### Feature updates

- **Microsoft Edge for Business Banner.**  Microsoft Edge for Business is a dedicated Microsoft Edge experience built for work that enables admins in organizations to give their users a productive and secure work browser across managed and unmanaged devices. The in-product Microsoft Edge for Business banner is being deprecated and will no longer be visible.

- **Find on page.** Searching for a word or phrase on a webpage has become easier with the new smart find update to Find on page. For more information, see
[Find on page](https://www.microsoft.com/edge/features/find-on-page?form=MT00D8). Now when you search with Find on page, we suggest related matches and synonyms making it effortless to find what you're looking for, even if you misspell a word in your search query. When you search, simply select the suggested word to quickly locate the desired word or phrase on the page. Data is sent to Microsoft for processing.  For more information, see [Microsoft Edge's Privacy Whitepaper](/microsoft-edge/privacy-whitepaper/). Administrators can control the availability using the [RelatedMatchesCloudServiceEnabled](/deployedge/microsoft-edge-policies#relatedmatchescloudserviceenabled) policy.

- **New SmartScreen policy.**  The [ExemptSmartScreenDownloadWarnings](/deployedge/microsoft-edge-policies#exemptsmartscreendownloadwarnings) policy lets administrators create a dictionary of file type extensions with a corresponding list of domains that are exempted from SmartScreen AppRep warnings.  Files with file type extensions specified for domains identified by this policy are still subject to file type extension-based security warnings and mixed-content download warnings.

- **New Microsoft Edge Update policies.** The **MeteredUpdatesDefault** and **MeteredUpdates** policies allows administrators to control the "Download Updates over metered connections" setting (`edge://settings/help`). The **MeteredUpdatesDefault** applies to all apps and **MeteredUpdates** applies to targeted apps. When a policy is configured to Allow, updates occur on a metered connection, such as cellular connections or others where data usage is controlled.

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

## Version: 117.0.2045.31: September 15, 2023

Fixed various bugs and performance issues.

> [!IMPORTANT]
> This update to Stable channel contains a fix for [CVE-2023-4863](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2023-4863), which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-15-2023).

### Announcement: Microsoft Edge for Business is available for unmanaged Windows devices

Microsoft Edge for Business is a dedicated Microsoft Edge experience built for work that enables admins in organizations to give their users a productive and secure work browser. This dedicated work experience is now available for unmanaged Windows devices using Microsoft Intune Mobile Application Management (MAM). This release includes the supporting changes for Microsoft Edge. When the required Intune update is released, more information will be available on how to test and deploy this feature with your users.

**Note:**

- Support is available for Windows 11, build 10.0.22621 (22H2) or later.

- Requires Microsoft Intune 2309 or higher

- App Protection Conditional Access is in Public Preview.

- If you have a Conditional Access (CA) policy on your tenant that targets "All cloud apps" that covers "Mobile apps and desktop clients" and requires a compliant device, app protection policies or has a "Block" grant control, your end users will not be able to MAM enroll. A change to support this is targeted for Microsoft Edge v118.

- If you want to continue testing/evaluating APP CA, you can choose to exclude the "Edge Auth" application from your cloud app targeting. Some Microsoft Edge features might not function properly until CA is satisfied, but MAM enrollment will be able to complete.

### Announcement: Deprecating the unload event

The Google Chrome team plans to deprecate the unload event starting in Chrome version 118. The deprecation will occur by gradually changing the default so unload handlers stop firing on pages unless a page explicitly opts in to re-enable them. For more information, see [Deprecating the unload event - Chrome Developers](https://developer.chrome.com/blog/deprecating-unload/), and [Google Groups - Conversations](https://groups.google.com/a/chromium.org/g/blink-dev/c/dvusqw9-IhI/m/SBkm_u1RAQAJ).

While we haven't yet finalized the deprecation schedule, we anticipate that Microsoft Edge will follow Chrome's schedule with a possible delay of a release or two. If you're interested in testing with Microsoft Edge starting in version 118, the **ForcePermissionPolicyUnloadDefaultEnabled** policy will be available or you can use the instructions documented at [Disable unload handlers by default and add Permissions-Policy to opt-in to enabling them](https://github.com/fergald/docs/blob/master/explainers/permissions-policy-deprecate-unload.md#disable-unload-handlers-by-default-and-add-permissions-policy-to-opt-in-to-enabling-them).

WebView2 will support both the permissions policy and the enterprise policy but won't be impacted by the gradual rollout in Microsoft Edge. We expect WebView2 will switch defaults when the roll out reaches 100% of page loads.

### Feature updates

- **Microsoft Edge for Business Banner.**  Administrators can control the availability of the in-product Microsoft Edge for Business banner using the [PromotionalTabsEnabled](/deployedge/microsoft-edge-policies#promotionaltabsenabled) policy.

- **Microsoft Edge Sync Favorites Recovery.** The Microsoft Edge Sync Favorites Recovery feature lets sync users restore any favorites that they lost or deleted within the last 14 days. Users can access this feature from either the Microsoft Edge favorites hub or the `edge://favorites` page. For more information, see [Recover lost or deleted favorites in Microsoft Edge - Microsoft Support](https://support.microsoft.com/topic/recover-lost-or-deleted-favorites-in-microsoft-edge-ac06270e-ba57-4266-8389-8bfd1df1aa5e)

- **Autofill Autocomplete.** This feature helps you fill form fields faster on the web. When you start typing in a form field, Microsoft Edge suggests possible in-line completions when there's an exact match with your saved data in the browser. For example, if you type the first few characters of your address, autocomplete will suggest the rest of address - you can choose the autocomplete suggestion or continue typing as usual. Autofill options can be found in Settings (`edge://settings/personalinfo`).

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

## Version 116.0.1938.54: August 21, 2023

Fixed various bugs and performance issues.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-21-2023).

### Feature update

- **Microsoft Edge for Business.** With native enterprise grade security, productivity, manageability, and AI built in, Edge for Business enables organizations to maximize productivity and security, and offers the ability to create separation between work and personal browsing with automatic switching between the lightly managed personal browser window (MSA profile) and the work browser window (Microsoft Entra ID). All users signing in with their Entra ID (formerly Azure Active Directory) will automatically receive Edge for Business and see an updated Edge icon with a briefcase to designate they're in the work browser window. For more information, [read our FAQ](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/microsoft-edge-for-business-faq/ba-p/3891837).

- **Option to attach the Edge sidebar to the Windows desktop.** Users of the Microsoft Edge sidebar will be able to access their apps and sites directly from their Windows 10 desktop. As an opt-in experience in Windows 10, users can attach the sidebar to their Windows desktop by clicking a "popout" icon near the base of the sidebar in the browser. This enables a side-by-side experience that works with any Windows app — including Microsoft Edge itself. Users enjoy streamlined access to the same set of powerful AI tools and web-based services, including Bing Chat, without launching a browser window, enhancing productivity regardless of where they are in Windows. Additional features and options are planned in future versions of Microsoft Edge. Administrators can control the availability of this feature using the [StandaloneHubsSidebarEnabled](/DeployEdge/microsoft-edge-policies#standalonehubssidebarenabled) policy.

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

- **New policy for Browser essentials.** Browser essentials help you gain additional insights about the health of your browser. It lets you stay informed about your browser's performance and security with a single, intuitive view that provides helpful suggestions for performance optimization and browser protection. The [PinBrowserEssentialsToolbarButton](/deployedge/microsoft-edge-policies#pinbrowseressentialstoolbarbutton) policy lets Admins configure whether to pin the Browser essentials button on the toolbar.

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

#### Additional policy changes

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

- **Google Docs Offline extension for Microsoft Edge.**  Google Docs Offline is an extension provided by Google to allow users to work on Google Docs, Sheets, Slides and Drive without internet access. This extension also provides advanced cut, copy, and paste functionalities across Google Editors.  The Google Docs Offline extension will be pre-installed and will be disabled by default for Microsoft Edge users. When a user navigates to Google Docs, the extension will be auto-enabled. Administrators can use the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) and [ExtensionInstallBlocklist](/deployedge/microsoft-edge-policies#extensioninstallblocklist) policies to block the auto-installation of the Google Docs Offline extension.  **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

## Version 114.0.1823.55: June 19, 2023

Fixed various bugs and performance issues.

## Version 114.0.1823.51: June 15, 2023

Fixed various bugs and performance issues for Stable and Extended Stable release.

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-15-2023).

### Feature update

- Web Select is now a part of Web Capture. Users can access Web Select through Web Capture feature or press **Ctrl** + **Shift** + **X** shortcut directly for quick access.

### Policy updates

#### Additional policy changes

- [WebSelectEnabled](/deployedge/microsoft-edge-policies#webselectenabled) - This policy is deprecated. It is currently supported but will become obsolete in version 117.
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
