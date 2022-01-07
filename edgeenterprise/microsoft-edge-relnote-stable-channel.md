---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 01/06/2022
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

## Version 97.0.1072.55: January 6

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#january-6-2022).

### Feature updates

- **Use the current profile to sign into websites when multiple work or school accounts are signed in on a device.** When multiple work or school accounts are signed in on a device, users will be asked to choose an account from the account picker to continue their visits to websites. In this release, users will be prompted to let Microsoft Edge sign in to the websites automatically with the work or school account that's signed into the current profile. Users can turn this feature on and off in **Settings** > **Profile preferences**.

- **Add support for Microsoft Endpoint Data Loss Prevention (DLP) on macOS.** Microsoft Endpoint DLP policy enforcement will be available natively on macOS.

- **Automatic HTTPS.** Users can upgrade navigations from HTTP to HTTPS on domains likely to support this more secure protocol. This support can also be configured to attempt delivery over HTTPS for all domains. Note: This feature is a Controlled Feature Rollout. If you don’t see this feature, check back as we continue our rollout.

- **Block WebSQL in 3rd-party contexts.** Use of the legacy WebSQL feature will be blocked from 3rd-party frames. The [WebSQLInThirdPartyContextEnabled](/deployedge/microsoft-edge-policies#websqlinthirdpartycontextenabled) policy is available as an opt-out option until Microsoft Edge version 101. This change is happening in the Chromium project that Microsoft Edge is based on. For more information, see this [Chrome Platform Status](https://chromestatus.com/feature/5684870116278272) entry.

- **Citations in Microsoft Edge.** Citing sources for research is a common requirement for students. They have to manage many research references and sources, which aren't easy tasks. They also have to translate these citations to proper citation formats like APA, MLA, and Chicago. This new "Citations" feature, now in Preview in Microsoft Edge, gives students a better way to manage and generate citations as they research online. With Citations turned on in Collections or from **Settings and more (Alt-F)**, Microsoft Edge automatically generates citations that students can use later so they can stay focused on their research. When they're done, they can easily compile these citations into a final deliverable. For more information, see [Previewing Citations in Microsoft Edge](https://blogs.windows.com/msedgedev/2021/11/04/preview-citations-feature-edge/).

- **Control Flow Guard (CFG).** Microsoft Edge will start supporting more fine-grained protection by combating memory corruption vulnerabilities and by protecting against indirect calls. CFG is only supported with Windows 8 and later. For more information, see [Control Flow Guard](/windows/win32/secbp/control-flow-guard).
  
  > [!NOTE]
  > This is an evolving technology, please share your feedback to help us strengthen its support.

- **Control-flow Enforcement Technology (CET) available with security feature.** When you enable "Enhance your security on the web", Microsoft Edge will support an even safer browsing mode that uses hardware-dependent control flow for browser processes. CET is available on the following supported hardware: Intel 11th Gen. or AMD Zen 3.

### Policy updates

#### New Policies

- [AccessibilityImageLabelsEnabled](/DeployEdge/microsoft-edge-policies#accessibilityimagelabelsenabled) - Get Image Descriptions from Microsoft Enabled.
- [CORSNonWildcardRequestHeadersSupport](/DeployEdge/microsoft-edge-policies#corsnonwildcardrequestheaderssupport) - CORS non-wildcard request header support enabled.
- [EdgeDiscoverEnabled](/DeployEdge/microsoft-edge-policies#edgediscoverenabled) - Discover feature In Microsoft Edge.
- [EdgeEnhanceImagesEnabled](/DeployEdge/microsoft-edge-policies#edgeenhanceimagesenabled) - Enhance images enabled.
- [InternetExplorerModeTabInEdgeModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorermodetabinedgemodeallowed) - Allow sites configured for Internet Explorer mode to open in Microsoft Edge.
- [SameOriginTabCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#sameorigintabcaptureallowedbyorigins) - Allow Same Origin Tab capture by these origins.
- [ScreenCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#screencaptureallowedbyorigins) - Allow Desktop, Window, and Tab capture by these origins.
- [SerialAllowAllPortsForUrls](/DeployEdge/microsoft-edge-policies#serialallowallportsforurls) - Automatically grant sites permission to connect all serial ports.
- [SerialAllowUsbDevicesForUrls](/DeployEdge/microsoft-edge-policies#serialallowusbdevicesforurls) - Automatically grant sites permission to connect to USB serial devices.
- [SmartScreenDnsRequestsEnabled](/DeployEdge/microsoft-edge-policies#smartscreendnsrequestsenabled) - Enable Microsoft Defender SmartScreen DNS requests.
- [TabCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#tabcaptureallowedbyorigins) - Allow Tab capture by these origins.
- [WebSQLInThirdPartyContextEnabled](/DeployEdge/microsoft-edge-policies#websqlinthirdpartycontextenabled) - Force WebSQL in third-party contexts to be re-enabled.
- [WindowCaptureAllowedByOrigins](/DeployEdge/microsoft-edge-policies#windowcaptureallowedbyorigins) - Allow Window and Tab capture by these origins.

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
  
- **Improved handoff between IE mode and the modern browser.** Starting with this version of Microsoft Edge, navigations between Microsoft Edge and Internet Explorer mode will include form data and additional HTTP headers. Referrer headers, post data, forms data, and request methods will be forwarded correctly across the two experiences. You can specify which data types should be included using the InternetExplorerIntegrationComplexNavDataTypes policy. For more information, see this FAQ: [My application requires transferring POST data between IE mode and Microsoft Edge. Is this supported?](./edge-ie-mode-faq.md#my-application-requires-transferring-post-data-between-ie-mode-and-microsoft-edge-is-this-supported)

- **Update Microsoft Edge WebWiew2 using WSUS.** IT Admins using Windows Server Update Services (WSUS) to update Microsoft Edge will also be able to update Microsoft Edge WebView2 using WSUS. This capability gives admins an easier servicing process for offline devices.

- **WSUS updates for Server.** WSUS and Catalog updates for Microsoft Edge channels (Stable, Beta, and Dev) will now apply to Windows Server SKUs that have Microsoft Edge installed, including Windows Server 2022. For more information on how to configure WSUS updates for Microsoft Edge, see [Update Microsoft Edge](https://docs.microsoft.com/mem/configmgr/apps/deploy-use/deploy-edge?bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json&toc=https://docs.microsoft.com/DeployEdge/toc.json#update-microsoft-edge).

- **Microsoft Edge AutoLaunch Protocols Component.** Microsoft Edge 96 introduces the AutoLaunch Protocols [Component](https://textslashplain.com/2019/07/16/updating-browsers-quickly-flags-respins-and-components/) that contains lists of scheme-origin dictionaries to automatically allow or block. This protects customers from dangerous schemes (for example, a protocol handler with a 0-day) while eliminating prompts from known-safe pairings (for example, the Teams website can open the Teams client app). If for some reason, you don't want Microsoft Edge to block vulnerable protocol handlers and allow known-safe pairings, use the toggle in *edge://settings/content/applicationLinks*, or set the [AutoLaunchProtocolsComponentEnabled](/deployedge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) policy to False.

- **Launch Progressive Web App (PWA) directly via protocol links.** Let installed PWAs handle links that use a specific protocol for a more integrated experience.

- **Quickly view Office files in the browser.** Users can now view Office files including documents, spreadsheets, and presentations that they come across while browsing on Microsoft Edge right in the browser without needing to download the file and then open it in a different application. There will be no changes in the file open experience for Office files that are hosted on OneDrive or SharePoint.
  
- **Freeform highlighting on PDFs.** The PDF viewing and markup experience is improved with the addition of freeform highlighters. You can highlight sections in PDFs that you don't have access to, and scanned documents.

- **Control-flow Enforcement Technology (CET).** Microsoft Edge will begin supporting an even safer browsing mode that uses hardware-dependent control flow for browser processes on supported hardware (Intel 11th Gen. or AMD Zen 3). Note: Because this is a Controlled Feature Rollout you may not notice this feature enabled on all devices. You can enable or disable CET by manipulating Image File Execution Options (IFEO) using group policy.

- **New warning dialog for typosquatting sites.** The browser will show a warning on some sites with URLs that look very similar to other sites. This UI uses client-side heuristics to warn users about sites that might be spoofing popular web sites. For more information, see [What is typosquatting?](https://support.microsoft.com/topic/what-is-typosquatting-54a18872-8459-4d47-b3e3-d84d9a362eb0).
  
- **Dictionary added to mini-toolbar in Immersive Reader.**  We're adding dictionary functionality to the mini-toolbar to assist in your reading and research. You'll be able to look up the spelling and definitions of words more quickly and easily in the Immersive Reader experience.
  
- **Learn how to solve math problems with Math Solver.** We’re excited to announce that you can use Math Solver in Microsoft Edge to get help with a wide range of mathematical concepts. These concepts range from elementary arithmetic and quadratic equations to trigonometry and calculus. Math Solver lets you take a picture of a handwritten or printed math problem and then provides an instant solution with step-by-step instructions to help you learn how to reach the solution without help. Math Solver also comes with a mathematical keyboard that you can use to easily type math problems. This keyboard eliminates the need to search around a traditional keyboard to find the math characters you need. After solving your problem, Math Solver provides options to continue learning with quizzes, worksheets, and video tutorials.

### Policy updates

#### New Policies

- [ApplicationGuardUploadBlockingEnabled](/DeployEdge/microsoft-edge-policies#applicationguarduploadblockingenabled) Prevents files from being uploaded while in Application Guard
- [AudioProcessHighPriorityEnabled](/DeployEdge/microsoft-edge-policies#audioprocesshighpriorityenabled) Allow the audio process to run with priority above normal on Windows
- [AutoLaunchProtocolsComponentEnabled](/DeployEdge/microsoft-edge-policies#autolaunchprotocolscomponentenabled) AutoLaunch Protocols Component Enabled
- [BrowserLegacyExtensionPointsBlockingEnabled](/DeployEdge/microsoft-edge-policies#browserlegacyextensionpointsblockingenabled) Enable browser legacy extension point blocking
- [CrossOriginWebAssemblyModuleSharingEnabled](/DeployEdge/microsoft-edge-policies#crossoriginwebassemblymodulesharingenabled) Specifies whether WebAssembly modules can be sent cross-origin
- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) Specifies whether the display-capture permissions-policy is checked or skipped
- [EfficiencyMode](/DeployEdge/microsoft-edge-policies#efficiencymode) Configure when efficiency mode should become active
- [ForceSyncTypes](/DeployEdge/microsoft-edge-policies#forcesynctypes) Configure the list of types that are included for synchronization
- [InternetExplorerIntegrationComplexNavDataTypes](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcomplexnavdatatypes) Configure whether form data and HTTP headers will be sent when entering or exiting Internet Explorer mode
- [InternetExplorerModeToolbarButtonEnabled](/DeployEdge/microsoft-edge-policies#internetexplorermodetoolbarbuttonenabled) Show the Reload in Internet Explorer mode button in the toolbar
- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) Configure the pixel adjustment between window.open heights sourced from IE mode pages vs. Edge mode pages
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenwidthadjustment) Configure the pixel adjustment between window.open widths sourced from IE mode pages vs. Edge mode pages
- [IntranetFileLinksEnabled](/DeployEdge/microsoft-edge-policies#intranetfilelinksenabled) Allow intranet zone file URL links from Microsoft Edge to open in Windows File Explorer
- [NewSmartScreenLibraryEnabled](/DeployEdge/microsoft-edge-policies#newsmartscreenlibraryenabled) Enable new SmartScreen library
- [PrintPostScriptMode](/DeployEdge/microsoft-edge-policies#printpostscriptmode) Print PostScript Mode
- [PrintRasterizePdfDpi](/DeployEdge/microsoft-edge-policies#printrasterizepdfdpi) Print Rasterize PDF DPI
- [RendererAppContainerEnabled](/DeployEdge/microsoft-edge-policies#rendererappcontainerenabled) Enable renderer in app container
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) Configure ShadowStack crash rollback behavior
- [SharedLinksEnabled](/DeployEdge/microsoft-edge-policies#sharedlinksenabled) Show links shared from Microsoft 365 apps in History
- [TyposquattingCheckerEnabled](/DeployEdge/microsoft-edge-policies#typosquattingcheckerenabled) Configure Edge TyposquattingChecker
- [VisualSearchEnabled](/DeployEdge/microsoft-edge-policies#visualsearchenabled) Visual search enabled

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

- **Improvements to the downloads experience.** Support for the download user experience is extended to progressive web applications PWAs and WebView. We will also begin to support drag and drop to the File Explorer and Desktop.

- **Pick up where you left off on PDF documents.**  You will now be able to resume reading from where you last closed your PDF document.

- **Efficiency mode extends battery life when your laptop enters battery saver mode.**  Efficiency mode will become active when your laptop enters battery saver mode to allow the browser to manage resource usage to extend the battery life of your machine. You will have four options when efficiency mode becomes active: Unplugged and low battery, Unplugged, Always, and Never. Note: This feature is a Controlled Feature Rollout. If you don’t see this feature, check back shortly as we continue our rollout.

- **Free form text boxes added to PDF documents.** We now support adding free form text boxes to PDF documents. You can use these boxes to fill in forms and add visible notes.

- **Citation support added to Collections.**  We've improved the Collections experience, especially for students and researchers. Collections will start supporting citations and reading lists.

- **Update your passwords faster and with fewer clicks.** The browser will now take you directly to the Change Password page for a given website. This action saves you time and clicks by removing the need to navigate to the page manually. After you’re on this page, the browser will also autofill your existing password and suggest a strong, unique new password.  Note: Currently this feature is only available on a limited number of sites.

- **Auto-account creation.** We now provide additional support on Sign-Up pages by allowing you to create an online account with one click. You can do this by selecting the suggestion drop-down when you click on any form field in the Sign-Up form. Doing so will show not only information relevant to the Sign-Up form, but also a strong new password suggestion. Upon selection, all the relevant information gets populated in the respective fields and the suggested password will be automatically stored on submission to the website. Note: Currently this feature is only available on a limited number of sites.

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

- **New Extended stable option being offered.**  We are offering a new Extended Stable option to our managed Enterprise customers. The Extended Stable option will stay on even numbered revisions and update every 8 weeks. There will be a biweekly security update.  Additional information here: https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **Improvements to default behavior of opening MHTML files.**  MHTML files will continue to open in IE mode if IE mode is enabled, unless the MHTML file was saved from Microsoft Edge (using the Save As or Save Page As options in Microsoft Edge). If the file was saved from Microsoft Edge, it will now open in Microsoft Edge.  This change will fix a rendering issue that was observed when opening an MHTML file in IE mode when saved from Microsoft Edge.

- **Restrict private network requests to secure contexts.** Access to resources on local (intranet) networks from pages on the internet requires that those pages be delivered over HTTPS. This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, navigate to the [Chrome Platform Status entry](https://chromestatus.com/feature/5436853517811712). Two compatibility policies are available to support scenarios that need to preserve compatibility with non-secure pages: [InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) and [InsecurePrivateNetworkRequestAllowedForUrls](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls).

- **Block mixed content downloads.** Secure pages will only download files hosted on other secure pages, and downloads hosted on non-secure (non-HTTPS) pages will be blocked if initiated from a secure page. This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, navigate to the [Google security blog entry](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html).

- **Enable implicit sign-in for on-premises accounts.** By enabling the [OnlyOnPremisesImplicitSigninEnabled](/deployedge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) policy, only on-premises accounts will be enabled for implicit sign-in.  Microsoft Edge won't attempt to implicitly sign in to MSA or AAD accounts. Upgrade from on-premises accounts to AAD accounts will be stopped as well.

- **New accessibility settings page.**  We have brought accessibility-related settings together on a single page. You can find the new edge://settings/accessibility page under the main settings list. Here you can find settings to make the web page bigger, show a high visibility outline around the area of focus and other settings that can help improve your web browsing experience. We’ll continue to add new settings here in future versions of Microsoft Edge.

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

<!--  -->
<!--- Archive from Version 93.0.961.38: September 2 to Version 92.0.902.62: July 29 --->
<!-- Archive from Version 92.0.902.55: July 22 to Version 91.0.864.37: May 27 -->
<!-- Archive from 89.0.774.45: March 4 to 90.0.818.66: May 20 ->
<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
