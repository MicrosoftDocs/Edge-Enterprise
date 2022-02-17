---
title: "Archived release notes for Microsoft Edge Beta Channel"
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 02/07/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Archived release notes for Microsoft Edge Beta Channel"
---

# Archived release notes for Microsoft Edge Beta Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Beta Channel. To understand Microsoft Edge channels, see the [Overview of the Microsoft Edge channels](microsoft-edge-channels.md). All the security updates are listed [here](microsoft-edge-relnotes-security.md).

## Version 97.0.1072.21: December 1

### Feature updates

- **Use current profile to sign into websites when multiple work or school accounts are signed in on a device.** When multiple work or school accounts are signed in on a device, users will be asked to choose an account from the account picker to continue their visits to websites. In this release, users will be prompted to allow Microsoft Edge to sign in to the websites automatically with the work and school account that's signed into current profile. Users can turn this feature on and off in **Settings/Profile preferences**.

- **Add support for Microsoft Endpoint Data Loss Prevention (DLP) on macOS.** Microsoft Endpoint DLP policy enforcement is available natively on macOS.

- **Open digitally signed PDF files.**  Digital signatures are used extensively to validate the authenticity of, and changes to, a document. Users can validate the signatures for PDF files directly from the browser, without the need for any add-ins.

- **Citations in Microsoft Edge.** Citing sources for research is a common requirement for students. They have to manage many research references and sources, which aren't easy tasks. They also have to translate these citations to proper citation formats like APA, MLA, and Chicago. This new "Citations" feature in Microsoft Edge (now in Preview) gives students a better way to manage and generate citations as they research online. With Citations turned on in Collections or from **Settings and more (Alt-F)**, Microsoft Edge automatically generates citations that students can use later so they can stay focused on their research. When they're done, they can easily compile these citations into a final deliverable. For more information, see [Previewing Citations in Microsoft Edge](https://blogs.windows.com/msedgedev/2021/11/04/preview-citations-feature-edge/).

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

- **Learn how to solve math problems with Math Solver.** We’re excited to announce that you can use Math Solver in Microsoft Edge to get help with a wide range of mathematical concepts. These concepts range from elementary arithmetic and quadratic equations to trigonometry and calculus. Math Solver lets you take a picture of a handwritten or printed math problem and then provides an instant solution with step-by-step instructions to help you learn how to reach the solution without help. Math Solver also comes with a mathematical keyboard that you can use to easily type math problems. This keyboard eliminates the need to search around a traditional keyboard to find the math characters you need. After solving your problem, Math Solver provides options to continue learning with quizzes, worksheets, and video tutorials.

- **Freeform highlighting on PDFs.** The PDF viewing and markup experience is improved with the addition of freeform highlighters. You can highlight sections in PDFs that you don't have access to, and scanned documents.

- **Hardware-enforced Stack Protection.**  Microsoft Edge will begin supporting an even safer browsing mode that uses hardware-dependent control flow for browser processes on supported hardware (Intel 11th Gen. or AMD Zen 3). Note: Because this is a Controlled Feature Rollout you may not notice this feature enabled on all devices. You can enable or disable Hardware-enforced Stack Protection by manipulating Image File Execution Options (IFEO) using group policy.

- **New warning dialog for typosquatting sites.** The browser will now show a warning on some sites with URLs that look similar to other sites. This UI uses client-side heuristics to warn users about sites that might be spoofing popular web sites. For more information, see [What is typosquatting?](https://support.microsoft.com/topic/what-is-typosquatting-54a18872-8459-4d47-b3e3-d84d9a362eb0).

- **Improved handoff between IE mode and the modern browser.**  Starting with this version of Microsoft Edge, navigations between Microsoft Edge and Internet Explorer mode will include form data and additional HTTP headers. Referrer headers, post data, forms data, and request methods will be forwarded correctly across the two experiences. You can specify which data types should be included using the [InternetExplorerIntegrationComplexNavDataTypes](/deployedge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) policy. For more information, see this FAQ: [My application requires transferring POST data between IE mode and Microsoft Edge](./edge-ie-mode-faq.md#my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported).

- **Cloud Site List Management for IE mode in Public Preview.**  Cloud Site List Management lets you manage your site lists for IE mode in the cloud without needing an on-premises infrastructure to host your organization's site list. You can access the Cloud Site List Management feature using the Microsoft Edge Site Lists experience in the Microsoft 365 Admin Center. To learn more, see the [Cloud Site List Management for IE mode (Public Preview)](./edge-ie-mode-cloud-site-list-mgmt.md) article.

- **Update Microsoft Edge WebWiew2 using WSUS.** IT Admins using WSUS to update Microsoft Edge will also be able to update Microsoft Edge WebView2 using WSUS. This capability gives admins an easier servicing process for offline devices.

- **WSUS updates for Server.** WSUS and Catalog updates for Microsoft Edge channels (Stable, Beta, Dev) will now apply to Windows Server SKUs that have Microsoft Edge installed, including Windows Server 2022. For more information on how to configure WSUS updates for Microsoft Edge, see [Update Microsoft Edge](https://docs.microsoft.com/mem/configmgr/apps/deploy-use/deploy-edge?bc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Fbreadcrumb%2Ftoc.json&toc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Ftoc.json#update-microsoft-edge).

### Policy updates

#### New Policies

- [ApplicationGuardUploadBlockingEnabled](/DeployEdge/microsoft-edge-policies#applicationguarduploadblockingenabled) - Prevents files from being uploaded while in Application Guard.
- [AudioProcessHighPriorityEnabled](/DeployEdge/microsoft-edge-policies#audioprocesshighpriorityenabled)  - Allow the audio process to run with priority above normal on Windows.
- [AutoLaunchProtocolsComponentEnabled](/DeployEdge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) - AutoLaunch Protocols Component Enabled.
- [EfficiencyMode](/DeployEdge/microsoft-edge-policies#efficiencymode) - Configure when efficiency mode should become active.
- [ForceSyncTypes](/DeployEdge/microsoft-edge-policies#forcesynctypes) - Configure the list of types that are included for synchronization.
- [InternetExplorerIntegrationComplexNavDataTypes](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) - Configure whether form data and HTTP headers will be sent when entering or exiting Internet Explorer mode.
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

- **View in File Explorer support for SharePoint Online libraries in Microsoft Edge.**  Now you can enable the View in File Explorer capability for SharePoint Online Modern Document Libraries. For this experience to be visible and work for your users, you will need to enable the Microsoft Edge ["Configure the View in File Explorer feature for SharePoint pages in Microsoft Edge"](/deployedge/microsoft-edge-policies#configureviewinfileexplorer) policy and update your SharePoint Online tenant configuration. Learn more: [View SharePoint files with File Explorer in Microsoft Edge - SharePoint in Microsoft 365 | Microsoft Docs](/SharePoint/sharepoint-view-in-edge).

- **Intranet zone file URL links will open in Windows File Explorer.**  You can allow file URL links to intranet zone files originating from intranet zone HTTPS websites to open Windows File Explorer for that file or directory. You can enable this experience using the [IntranetFileLinksEnabled](/deployedge/microsoft-edge-policies#intranetfilelinksenabled) policy.

- **Improvements to the downloads experience.**  Support for the download user experience is being extended to progressive web applications PWAs and WebView. We will also begin to support drag and drop to the File Explorer and Desktop.

- **Pick up where you left off on PDF documents.**  You can resume reading from the location where you last closed your PDF document.

- **Efficiency mode extends battery life when your laptop enters battery saver mode.**  Efficiency mode will become active when your laptop enters battery saver mode to allow the browser to manage resource usage to extend the battery life of your machine. You will have four options for when efficiency mode becomes active, Unplugged and low battery, Unplugged, Always, and Never. Note: This is a Controlled Feature Rollout. Devices with a battery should have the feature turned on.

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

- **Microsoft Edge moving to a 4-week cadence for updates in Beta and Stable channels.**  We will adopt a new, 4-week release cycle for major versions. You can read more about the decision here: https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/

- **New Extended stable option being offered.**  We are offering a new Extended Stable option to our managed Enterprise customers. The Extended Stable option will stay on even numbered revisions and update every 8 weeks. There will be a biweekly security update.  Additional information here: https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **Improvements to default behavior of opening MHTML files.**  MHTML files will continue to open in IE mode if IE mode is enabled, unless the MHTML file was saved from Microsoft Edge (using the Save As or Save Page As options in Microsoft Edge). If the file was saved from Microsoft Edge, it will now open in Microsoft Edge.  This change will fix a rendering issue that was observed when opening an MHTML file in IE mode when saved from Microsoft Edge.

- **Restrict private network requests to secure contexts.** Access to resources on local (intranet) networks from pages on the internet requires that those pages be delivered over HTTPS. This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, navigate to the [Chrome Platform Status entry](https://chromestatus.com/feature/5436853517811712). Two compatibility policies are available to support scenarios that need to preserve compatibility with non-secure pages: [InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) and [InsecurePrivateNetworkRequestAllowedForUrls](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls).

- **Block mixed content downloads.** Secure pages will only download files hosted on other secure pages, and downloads hosted on non-secure (non-HTTPS) pages will be blocked if initiated from a secure page. This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, navigate to the [Google security blog entry](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html).

- **Enable implicit sign-in for on-premises accounts.**   By enabling the OnlyOnPremisesImplicitSigninEnabled policy, only on-premises accounts will be enabled for implicit sign-in.  Microsoft Edge won't attempt to implicitly sign in to MSA or AAD accounts. Upgrade from on-premises accounts to AAD accounts will be stopped as well.

- **Free form text boxes added to PDF documents.**  We now support adding free form text boxes to PDF documents that you can use to fill in forms and add visible notes.

- **Update your passwords with ease.**  The browser will now take you directly to the Change Password page for a given website saving you time and clicks by avoiding the need to navigate to the page manually. Once you’re on this page the browser will also autofill your existing password and suggest a strong, unique new password.  Please note: currently this feature is available on a limited number of sites.  

- **New accessibility settings page.** We have brought accessibility-related settings together on a single page. You can find the new edge://settings/accessibility page under the main settings list. Here you can find settings to make the web page bigger, show a high visibility outline around the area of focus and other settings that can help improve your web browsing experience. We’ll continue to add new settings here in future versions of Microsoft Edge.

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

- **Initial Preferences in Microsoft Edge.**  Starting with Microsoft Edge version 93, deploying Microsoft Edge to your enterprise will become easier with the addition of [Initial Preferences](/deployedge/initial-preferences-support-on-microsoft-edge-browser).

- **IE mode on Microsoft Edge will support "no-merge" behavior.**  Starting with Microsoft Edge version 93, IE mode on Microsoft Edge will support "no-merge". For an end user, when a new browser window is launched from an IE mode application, it will be in a separate session, similar to the behavior in IE11. You will need to adjust your site list to configure sites that need to prevent session sharing. Behind the scenes, for each window of Microsoft Edge, the first time an IE mode tab is visited within that window, if it is one of the designated “no-merge” sites, that window is locked into a different “no-merge” IE session from all other Microsoft Edge windows at least until the last IE mode tab is closed in that window. Learn more [here](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--no-merge--option-that-was-supported-in-internet-explorer-11-).

- **Tab Groups.**  The ability to categorize tabs into user-defined groups helps you more effectively find, switch, and manage tabs across multiple workstreams. To enable this, we are turning on tab grouping beginning with Microsoft Edge version 93.

- **Hide the title bar while using Vertical Tabs.**  Get the extra few pixels back by hiding the browser's title bar, while in Vertical Tabs. Starting with Microsoft Edge version 93, you can go to edge://settings/appearance and under the Customize Toolbar section select the option to hide the title bar while in Vertical Tab mode.

- **Video Picture in Picture (PiP) from hover toolbar.**  Starting with Microsoft Edge version 93, it will become even easier to enter Picture in Picture (PiP) mode. When you hover over a supported video, a toolbar will appear that allows you to view that video in a PiP window.  Note: this is currently available for Microsoft Edge users on macOS.  Check back shortly as we continue our rollout to Windows users.

- **Removal of 3DES in TLS.**  Starting with Microsoft Edge version 93, support for the TLS_RSA_WITH_3DES_EDE_CBC_SHA cipher suite will be removed. This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, navigate to the [Chrome Platform Status entry](https://chromestatus.com/feature/6678134168485888). Additionally, in Microsoft Edge version 93, the [TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled) policy will be available to support scenarios that need to preserve compatibility with outdated servers. This compatibility policy will become obsolete and stop working in Microsoft Edge version 95. Ensure that you update affected servers before then.

- **Policies to bypass ClickOnce and DirectInvoke prompts.**  We have updated our policies to enable bypassing ClickOnce's prompts and DirectInvoke's app for specified file types, from specified domains. To do this, you will need to:

  - Enable [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) or [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - Enable [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes) policy and set the list of specific file types that ClickOnce and DirectInvoke should be disabled for
  - Enable the [AutoOpenAllowedForURLs](/deployedge/microsoft-edge-policies#autoopenallowedforurls) policy and set the list of specific domains that ClickOnce and DirectInvoke will be disabled for

  Note: AutoOpenAllowedForURLs is a supporter policy for AutoOpenFileTypes. If AutoOpenAllowedForURLs is not set and AutoOpenFileTypes is set, then file types listed will automatically open from all URLs.

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

- **Natural language search for browser history on the address bar**. Finding the article/website you are looking for is now easier thanks to natural language search right from the address bar. You can find search results based on page content/description/timing (such as "cake recipe from last week") in addition to titles/URL keyword matches alone.
Please note: this is a Controlled Feature Rollout. If you don’t see this feature, please check back shortly as we continue our rollout.

- **Users can easily get to Internet Explorer mode on Microsoft Edge**. Starting with Microsoft Edge version 92, users can reload a site in Internet Explorer mode on Microsoft Edge instead of relying on the standalone IE 11 application while waiting for a site to be configured in the Enterprise Mode Site List. Users will be prompted to add the site to their local site list such that navigating to the same page in Microsoft Edge will automatically render in IE mode for the next 30 days. You can use the *[InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed)* policy to configure this experience and allow access to the IE mode entry points as well as the ability to add sites to the local site list. You can use the *[InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays)* policy to adjust the number of days to keep sites on the local site list.
Note that KB5003698 or later is required for Windows 10, version 1909; or KB5003690 or later is required for Windows 10, version 2004, Windows 10, version 20H2, or Windows 10, version 21H1 for the end-to-end experience.

- **MHTML files will default to opening in Internet Explorer mode**. Starting in Microsoft Edge version 92 Stable, MHTML file types will automatically open in Internet Explorer mode on Microsoft Edge instead of the Internet Explorer (IE11) application. This is most commonly observed while trying to view Outlook emails in a browser. This change will occur only if IE11 is the default handler for this file type. If you'd prefer to change this, you can do so prior to installing the Stable version 92 update using [this guidance](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

- **Payment instruments are now synced across devices**. Beginning with Microsoft Edge version 92, you have the option to synchronize your payment information across your signed in devices.
Please note: this is a Controlled Feature Rollout. If you don’t see this feature, check back shortly as we continue our rollout.

- **"Disable developer mode extensions" warning can be permanently dismissed**. Beginning with Microsoft Edge version 92, you can turn off the warning "Disable developer mode extensions" by clicking on the 'Don't show this again' option.
Please note: this is a Controlled Feature Rollout. If you don’t see this feature, check back shortly as we continue our rollout.

- **Manage your extensions right from the toolbar**. The all-new extensions menu on the toolbar will allow you to hide/pin extensions easily. The quick links to manage extensions and find new extensions will make it easy for you to find new extensions and manage your existing ones.
Please note: this is a Controlled Feature Rollout. If you don’t see this feature, check back shortly as we continue our rollout.

- **Automatic HTTPS**. Users will have the option to upgrade navigation from HTTP to HTTPS on domains likely to support this more secure protocol. This support can also be configured to attempt delivery over HTTPS for all domains.
Please note: we are experimenting with this feature and this behavior won’t be seen if you have opted out of experiments.

- **Improvements to font rendering**. Improvements have been made to the rendering of text to improve clarity and reduce blurriness.
Please note: this is a Controlled Feature Rollout. If you don’t see this feature, check back shortly as we continue our rollout.

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

- **Identify network traffic originating from Microsoft Defender Application Guard containers at the proxy level**. Starting with Microsoft Edge version 91, there’s built in support to tag network traffic originating from Application Guard containers, allowing enterprises to identify them and apply specific policies.

- **Support option to allow synchronizing Favorites from the host to the Edge Application Guard container**. Starting with Microsoft Edge version 91, users have the option to configure Application Guard to synchronize their favorites from the host to the container. This ensures new favorites appear on the container as well.

- **Support for Speech Recognition APIs**. Starting with Microsoft Edge version 91, API support for speech recognition commands on Google.com and similar sites will be added. This feature is limited to a randomly selected group of users who have enabled experimentation. These users are giving feedback to the feature team.

- **Personalize your browser with new theme colors**. Make Microsoft Edge your own with one of the fourteen new theme colors on the Settings -> Appearance page. You can also install custom themes from the Microsoft Edge Add-on site. [Learn more](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

- **Interrupt Downloads** Starting with Microsoft Edge version 91 the browser will automatically interrupt downloads of types which could harm your computer if those downloads are started without a user interaction and are not supported by SmartScreen Application Reputation check. Users may override and continue to download by right clicking and choosing “Keep” on the download item. 
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

- **Single Sign On (SSO) is now available for Azure Active Directory (Azure AD) accounts and Microsoft Account (MSA) on macOS**. A user signed in on Microsoft Edge on macOS will now get automatically signed into websites that are configured to allow single sign on with Work and Microsoft accounts (for example, bing.com, office.com, msn.com, and outlook.com).

- **Kiosk mode.** Starting with Microsoft Edge version 90, we have locked down the UI print settings to only allow the configured printers and “Print to PDF” options. We have also done improvements within the assigned access single app kiosk mode to restrict the launch of other applications from the browser. For more information about the kiosk mode features please go [here](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features).

- **Printing:**

  - **New print rasterization mode for non-PostScript printers**. Starting with Microsoft Edge version 90, Admins can use a new policy to define print rasterization mode for their users. This policy  controls how Microsoft Edge prints to non-PostScript printers on Windows.  Sometimes print jobs on non-PostScript printers need to be rasterized to print correctly. The print options are Full and Fast.

  - **Additional page scaling options for printing**. Users are now able to customize scaling while printing webpages and PDF documents using additional options. The "Fit to Page" option ensures that the webpage or document is fit into the space available in the selected "Paper size" for printing. The "Actual size" option ensures that there are no changes in the size of the contents being printed regardless of the selected "Paper size".

- **Productivity:**

  - **Autofill suggestions are extended to include address fields content from clipboard**. Clipboard content is parsed when you click on a profile/address field (for example, phone, email, zip code, city, state, etc.) to show as autofill suggestions.

  - **Users can search for autofill suggestions even if a form or field isn’t detected**. Today if you have your information saved on Microsoft Edge, autofill suggestions pop up automatically and help you save time while filling out forms. In cases where autofill misses a form, or if you want to fetch data in forms that don't typically have autofill (like temporary forms), you can search for your information using autofill.

- **Access downloads from a flyout in the menu bar**. Downloads will appear in the top-right corner with all the active downloads in one place. This menu is easily dismissible so users can continue browsing uninterrupted, and they can monitor overall download progress right from the toolbar. [Learn more](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).


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

- **Kiosk mode enables additional lockdown capabilities**. Starting with Microsoft Edge version 89, we have added additional lockdown capabilities within kiosk mode to enable customers to get the job done in a productive and more secure experience. [Learn more](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **The Enterprise Mode Site List Manager tool will be available in the browser through the *edge://compat* page**. You can use this tool to create, edit and export your site list XML for Internet Explorer mode on Microsoft Edge. You can enable access to this tool as needed through group policy. [Learn More](./edge-ie-mode-site-list-manager.md).

- **Improve browser performance with sleeping tabs**. Sleeping tabs improves browser performance by putting inactive tabs to sleep to free up system resources like memory and CPU so active tabs or other applications can use them. Users can prevent sites from going to sleep and configure the length of time before an inactive tab goes to sleep. To keep users in their flow, there are also [heuristics](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) to prevent certain sites from going to sleep, such as intranet sites. This feature can be managed with group policies.

  > [!NOTE]
  > "Improve browser performance with sleeping tabs" is an update to the February 3 release notes for major version 89.0.774.18.

- **Reset your Microsoft Edge sync data in the cloud manually**. We are introducing a way to reset your Microsoft Edge sync data from within the product. This ensures that your data is cleared from Microsoft services, as well as resolving certain product issues that previously required a support ticket.

- **Improvements to text selection experience within PDF documents**. Users will begin to get a smoother and more consistent text selection experience across PDF documents opened in Microsoft Edge starting with version 89.

- **Date of birth field now supported in autofill**. Today Microsoft Edge helps you save time and effort while filling out forms and creating accounts online by auto filling your data like addresses, names, phone numbers, etc. Starting with Microsoft Edge version 89, we are adding support for another field that you can have saved and auto-filled - date of birth. You can view, edit and delete this information anytime in your profile settings.

- **Support for natural language search on the address bar, history search page, and the history hub**. Starting with Microsoft Edge version 89, finding an article/website will be easier with the natural language search on the address bar, history page, and history hub. Users can search for previously viewed page content/description/timing (such as "cake recipe from last week") in addition to titles/URL keyword matches. This feature is limited to a randomly selected group of users who have enabled experimentation. These users are giving feedback to the feature team.

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

  - Deprecate support for FTP protocol. Support for the legacy FTP protocol has been removed from Microsoft Edge. Attempting to navigate to an FTP link will result in the browser directing the Operating System to open an external application to handle the FTP link. Alternatively, IT administrators can configure Microsoft Edge to use IE Mode for sites that rely on the FTP protocol.
  - Adobe Flash support will be removed. Starting with Microsoft Edge Beta version 88, Adobe Flash capability and support will be removed. Learn more: [Update on Adobe Flash Player End of Support - Microsoft Edge Blog (windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Authentication:**

  - Single Sign On (SSO) now available for Azure Active Directory (Azure AD) accounts and Microsoft Account (MSA) on macOS and down-level Windows. A user signed in on Microsoft Edge on either macOS or down-level Microsoft Windows (7, 8.1) will now get automatically signed into websites that are configured to allow single sign on with Work and Microsoft accounts (e.g., bing.com, office.com, msn.com, outlook.com).<br>Note: A user may have to sign out and then sign back in if they'd signed into Microsoft Edge in a version prior to Microsoft Edge 88 to leverage this feature.
  - Automatically switch users on macOS to their work profile for sites that authenticate with their work account. Starting with Microsoft Edge version 88, we provide the ability to switch sites that authenticate with a user’s work profile on macOS.<br>Note: A user may have to sign out and then sign back in if they'd signed into Microsoft Edge in a version prior to Microsoft Edge 88 to leverage this feature.

- **Kiosk mode option to end session**. The "End session" button is now available in a kiosk mode public browsing experience. This feature ensures that browser data and settings are deleted when Microsoft Edge is closed. Learn more about kiosk mode features and roadmap, [Configure Microsoft Edge kiosk mode](./microsoft-edge-configure-kiosk-mode.md).

- **Security and Privacy:**

  - Alerts are generated if a user's password is found in an online leak. User passwords are checked against a repository of known-breached credentials and sends the user an alert if a match is found. To ensure security and privacy, user passwords are hashed and encrypted when they're checked against the database of leaked credentials.
  - Automatically upgrade mixed content. Secure pages delivered over HTTPS may contain references images that are served over non-secure HTTP. To improve privacy and security in Microsoft Edge 88, those images will be retrieved over HTTPS instead. If the image is not available over HTTPS, it will not be loaded.
  - View site permissions by site and by recent activity. Starting with Microsoft Edge 88, users will be able to manage site permissions more easily. They will be able to view permissions by web site rather than just permission type. Additionally, we’ve added a recent activity section that will show a user all the recent changes to their site permissions.
  - Increased controls for browser cookies. Starting with Microsoft Edge 88, users can delete third party cookies without affecting first party cookies. Users will also be able to filter their cookies by first or third party and sort by name, number of cookies, and the amount of data stored and last modified.

- **Performance:**

  - Improve browser performance with sleeping tabs. Sleeping tabs improves browser performance by putting inactive tabs to sleep to free up system resources like memory and CPU so active tabs or other applications can use them. Users can prevent sites from going to sleep and configure the length of time before an inactive tab goes to sleep. To keep users in their flow, there are also heuristics to prevent certain sites from going to sleep, such as intranet sites. This feature is limited to a randomly selected group of users who have enabled experimentation. We are planning to have the sleeping tabs feature enabled by default with Microsoft Edge version 89. This feature can be managed with group policies.
  - Improve Microsoft Edge startup speed with startup boost. To improve Microsoft Edge startup speed, we’ve developed a feature named startup boost. Startup boost makes Microsoft Edge launch faster by enabling Microsoft Edge to run in the background. Note: This feature is limited to a randomly selected group of users who have enabled experimentation. These users are giving feedback to the feature team.

- **Productivity:**

  - Improve productivity and multi-tasking with vertical tabs. As the number of horizontal tabs grows, site titles start to get cut off and tab controls are lost as each tab shrinks. This interrupts user workflow as they spend more time finding, switching, and managing their tabs and less time on the task at hand. Vertical tabs let users move their tabs to the side, where vertically aligned icons and longer site titles make it easier to quickly scan, identify and switch to the tab they want to open.
  - Auto filling the date of birth field. Microsoft Edge already helps save time and effort while filling out forms and creating accounts online by auto filling user data such as addresses, names, phone numbers, etc. Microsoft Edge now supports the date of birth field which users can save and auto fill. A user can view, edit and delete this information anytime in their profile settings.
  - Improvements to Recently closed in History. Recently closed now keeps the last 25 tabs and windows from any past browsing session rather than just the previous session. Users can select Recently closed in the new History experience to see all the tabs that were open.
  - “Your day at a glance” feature enabled by default. Starting with Microsoft Edge version 88, information workers can benefit from intelligent productivity features on their New tab page (NTP). We offer users signed in with their work or school account personalized and relevant content powered by their M365 Graph. Users can quickly scan their “Your day at a glance” modules to easily track their meetings and recent work as well as quickly launch the applications they want to use.

- **PDF:**

  - PDF document display in book view (two page). Starting with Microsoft Edge version 88, users can view PDF documents in a single page or in the two page book view. To change the view, click the **Page View** button in the toolbar.
  - Anchored text notes support for PDF files. Starting with Microsoft Edge version 87, users can add typed text notes on any piece of text in PDF files.
  - Smoother text selection experience in PDF documents. Users will get a smoother and consistent text selection experience across PDF documents opened in Microsoft Edge.
  - View webpages saved as PDF files in the Downloads bar. Users can now view the PDF files generated by setting "Save as PDF" as the printer destination for webpages in the Downloads bar.

- **Fonts:**

  - Browser icons are updated to the Fluent design system. As part of our continued work around Fluent Design in the browser, we've made changes to closer align icons to the new Microsoft icon system. These changes will impact many of our high-touch user interfaces, including tabs, address bar, as well as navigational and wayfinding icons found in our various menus.
  - Improved font rendering. Text rendering is improved for better clarity and to reduce blurriness.

### Policy updates

#### New policies

Sixteen new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added.

- [BlockExternalExtensions](./microsoft-edge-policies.md#blockexternalextensions) - Blocks external extensions from being installed.
- [InternetExplorerIntegrationLocalFileAllowed](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileallowed) - Allow launching of local files in Internet Explorer mode.
- [InternetExplorerIntegrationLocalFileExtensionAllowList](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist) - Open local files in Internet Explorer mode file extension allow list.
- [InternetExplorerIntegrationLocalFileShowContextMenu](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileshowcontextmenu) - Show context menu to open a link in Internet Explorer mode.
- [IntranetRedirectBehavior](./microsoft-edge-policies.md#intranetredirectbehavior) - Intranet Redirection Behavior.
- [PrinterTypeDenyList](./microsoft-edge-policies.md#printertypedenylist) - Disable printer types on the deny list.
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
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl) - Set the proxy .pac file URL.
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

- **Alerts are generated if a user's password is found in an online leak**. User passwords are checked against a repository of known-breached credentials and sends the user an alert if a match is found. To ensure security and privacy, user passwords are hashed and encrypted when they're checked against the database of leaked credentials.

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

- **Kiosk mode privacy features enabled**. Starting with Microsoft Edge version 87 kiosk mode features that will help enterprises around the privacy of user data will be enabled. These features will enable experiences such as clear the user data on exit, delete downloaded files and to reset the configured start experience after a specified amount of idle time. Learn more about how to [Configure Microsoft Edge kiosk mode](./microsoft-edge-configure-kiosk-mode.md)
- **ClickOnce deployment enabled by default**. ClickOnce is enabled by default in Microsoft Edge 87, which reduces the barriers for enterprises to deploy software and better align with Microsoft Edge Legacy browser behavior. Starting in Microsoft Edge 87, the ClickOnceEnabled policy's "Not configured" state will reflect the new default ClickOnce state of Enabled (as compared to the previous default state of Disabled).
- **The enterprise new tab page (NTP) integrates productivity with customizable, work-relevant feed content**. The enterprise NTP blends the Office 365 productivity page we offer to users signed in with their work or school account with personalized, work-relevant company and industry feeds that are organized in a single page. Users will be able to recognize the familiar Office 365 content and Microsoft Search for Business powered by Bing. In addition, they can easily flip to a customizable "My Feed" with content and modules that are relevant to the user, their company, or their industry, as well as a selection of other feeds that the organization has made available. [Learn more](/microsoft-365/admin/manage/manage-industry-news?preserve-view=true&view=o365-worldwide).

- **Privacy and Security:**

  - Support TLS Token Binding for policy-configured sites. TLS Token binding helps prevent token theft attacks to ensure that cookies can't be reused from a device other than the device upon which they were initially set. The use of TLS token binding requires setting the [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) policy and requires that the sites listed support this feature.

- **Keyboard support for highlighter on PDF files**. Users can use their keyboard keys to highlight any text on a PDF.

- **Printing:**

  - Choose which side to flip on when printing on both sides. Users can choose to flip on the long side or the short side of a sheet when printing on both sides.
  - Choose print rasterization mode for the enterprise. Control how Microsoft Edge prints to a non-PostScript printer on Windows. Sometimes print jobs on non-PostScript printers need to be rasterized to print correctly. The print options are "Full" and "Fast".

### Policy updates

#### New policies

Ten new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added.

- [ConfigureFriendlyURLFormat](./microsoft-edge-policies.md#configurefriendlyurlformat) - Configure the default paste format of URLs copied from Microsoft Edge, and determine if additional formats will be available to users.
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

* **Enforce enabling Sync by default across the enterprise.**  Administrators can enable synchronization for Azure Active Directory (Azure AD) accounts by default with the [ForceSync](./microsoft-edge-policies.md#forcesync) policy.

* **PDF updates:**

  * Table of contents for PDF Documents. Beginning with version 86, Microsoft Edge has added support for table of contents that lets users easily navigate through PDF documents.
  * Access all PDF functionalities on small form factor screens. Access all the capabilities of the Microsoft Edge PDF reader on devices with small screen sizes.
  * Pen support for highlighter on PDF files. With this update, users can use their digital pen to directly highlight text on PDF files, in the same way they would with a physical highlighter and paper.
  * Improved PDF scrolling. You will now be able to experience stutter free scrolling while navigating through long PDF documents.

* **Automatic profile switching on Windows 7, 8, and 8.1.** The automatic profile switching currently available in Microsoft Edge on Windows 10 is extended to downlevel Windows (Windows 7, 8,and  8.1). For more information, see the [automatic profile switching](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) blog post.

* **Users will see auto complete suggestions when they start typing a search query on the Microsoft Edge Add-ons website.** Auto complete will help users quickly complete their search query without having to type the entire string. This will be helpful because users won't have to remember correct spellings and they can choose from the available options that are displayed.

* **Remove the HTML5 Application Cache API.**  Beginning with Microsoft Edge version 86, the legacy Application Cache API that enables offline use of web pages is being removed from Microsoft Edge. Web Developers should review the [WebDev documentation](https://web.dev/appcache-removal/) for information on replacing  the Application Cache API with Service Workers.  Important: You can request an [AppCache OriginTrial Token](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) that allows sites to continue to use the deprecated Application Cache API until Microsoft Edge version 90.

* **Security:**

  * Secure DNS (DNS-over-HTTPS) Support.  Beginning with Microsoft Edge version 86, settings to control Secure DNS on un-managed devices is available. These settings aren't accessible to users on managed devices, but IT admins can enable or disable Secure DNS using the [dnsoverhttpsmode](./microsoft-edge-policies.md#dnsoverhttpsmode) group policy.


* **Add a custom image to the New Tab Page (NTP) using a group policy.** Beginning with Microsoft Edge version 86 the NTP has an option to replace the default image with a custom user-supplied image. The ability to manage the properties of this image is also supported by the group policy.

* **Match customized keyboard shortcuts to VS Code.** Microsoft Edge DevTools now supports customizing keyboard shortcuts in the DevTools to match with your editor/IDE. (In Microsoft Edge 84, we added the ability to match DevTools keyboard shortcuts to VS Code).

* **Replace [MetricsReportingEnabled]( /DeployEdge/microsoft-edge-policies#metricsreportingenabled) and [SendSiteInformationToImproveServices]( /DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) policies for downlevel Windows and macOS.** These policies are deprecated in Microsoft Edge version 86 and will become obsolete in Microsoft Edge version 89.<br>
These policies are replaced by [Allow Telemetry](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) on Windows 10, and the new [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) policy for all other platforms. This will let users manage the diagnostic data that gets sent to Microsoft for Windows 7, 8, 8.1 and macOS.

* **SameSite=Lax Cookies By Default**. To improve web security and privacy, cookies will now default to [SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite) handling by default. This means that cookies will only be sent in a first-party context and will be omitted for requests sent to third-parties. This change can cause compatibility impact on websites that require cookies for third-party resources to function correctly. To permit such cookies, web developers can mark cookies which should be set from and sent to third-party contexts by adding explicit `SameSite=none` and `Secure` attributes when the cookie is set. Enterprises that wish to exempt certain sites from this change can do so using the [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) policy, or can opt-out of the change across all sites using the [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled) policy.

### Policy updates

#### New policies

Nineteen new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [CollectionsServicesAndExportsBlockList](./microsoft-edge-policies.md#collectionsservicesandexportsblocklist) - Block access to a specified list of services and export targets in Collections.
- [DefaultSensorsSetting](./microsoft-edge-policies.md#defaultsensorssetting) - Default sensors setting.
- [DefaultSerialGuardSetting](./microsoft-edge-policies.md#defaultserialguardsetting) - Control use of the Serial API.
- [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) -  Send required and optional diagnostic data about browser usage.
- [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed) - Allow access to the Enterprise Mode Site List Manager tool.
- [ForceSync](./microsoft-edge-policies.md#forcesync) - Force synchronization of browser data and do not show the sync consent prompt.
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

- **Send to OneNote is available for Microsoft Edge Collections**. Everyone's excited to be able to send the information they've gathered in Collections to OneNote, where they can append it to a larger project and collaborate with others! And even more importantly, in Microsoft Edge 85, you'll be able send content to *Office for Mac* products (Word, Excel, and OneNote) for both Microsoft account and Azure Active Directory.

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

- On-prem Active Directory account auto sign in will only be targeted to organizations that turn it on. If users were already signed in with an on-prem AD account, they will now be able to sign out of it. Now, users will only be automatically signed in with the primary account on their operating system if it is a Microsoft account or an Azure Active Directory  account. Admins can enable auto sign in with an on-prem AD account using the ConfigureOnPremisesAccountAutoSignIn policy.

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
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin) - Configure automatic sign in with an Active Directory domain account when there is no Azure AD domain account.

#### Deprecated policies

The following policies continue to work in this release. They will become "obsolete" in a future release.

- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) - Re-enable Web Components v0 API until M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) - Allow WebDriver to Override Incompatible.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)