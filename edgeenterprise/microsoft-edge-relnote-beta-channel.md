---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 11/23/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Microsoft Edge release notes for Beta Channel"
---

# Release notes for Microsoft Edge Beta Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Beta Channel. Archived versions of these release notes are available at [Archived release notes for Microsoft Edge Beta Channel](./microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> Microsoft Edge Web Platform constantly evolves to improve user experience, security, and privacy. To learn more, see [Site compatibility-impacting changes coming to Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

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

- **Control-flow Enforcement Technology (CET).**  Microsoft Edge will begin supporting an even safer browsing mode that uses hardware-dependent control flow for browser processes on supported hardware (Intel 11th Gen. or AMD Zen 3). Note: Because this is a Controlled Feature Rollout you may not notice this feature enabled on all devices. You can enable or disable CET by manipulating Image File Execution Options (IFEO) using group policy.

- **New warning dialog for typosquatting sites.** The browser will now show a warning on some sites with URLs that look very similar to other sites. This UI uses client-side heuristics to warn users about sites that might be spoofing popular web sites. For more information, see [What is typosquatting?](https://support.microsoft.com/topic/what-is-typosquatting-54a18872-8459-4d47-b3e3-d84d9a362eb0).

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

<!-- archive from Version 94.0.992.9: September 2 to Version 92.0.902.40: July 6 -->
<!--Archive on Oct 27 From Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
