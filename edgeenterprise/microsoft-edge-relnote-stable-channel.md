---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 10/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Microsoft Edge release notes for Stable Channel"
---

# Release notes for Microsoft Edge Stable Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Stable Channel.

- All the security updates are listed [here](microsoft-edge-relnotes-security.md).
- Archived release notes for Microsoft Edge Stable Channel are located [here](microsoft-edge-relnote-archive-stable-channel.md).

 To understand Microsoft Edge channels, see the [Overview of the Microsoft Edge channels](microsoft-edge-channels.md).

> [!NOTE]
> For the Stable Channel, updates will roll out progressively over one or more days. To learn more, see [Progressive rollouts for Microsoft Edge updates](microsoft-edge-update-progressive-rollout.md).
>
> Microsoft Edge Web Platform constantly evolves to improve user experience, security, and privacy. To learn more, see [Site compatibility-impacting changes coming to Microsoft Edge](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes).

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

## Version 93.0.961.38: September 2

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#september-02-2021).

### Feature updates

- **Initial Preferences in Microsoft Edge.**  Microsoft Edge now supports a limited number of Initial Preferences (formerly Master Preferences). IT admins can deploy these settings as default before the browser is run for the first time by their users. Additional information here: [Configure Microsoft Edge using Initial Preferences settings for the first run](/deployedge/initial-preferences-support-on-microsoft-edge-browser).

- **IE mode on Microsoft Edge will support "no-merge" behavior.**  For an end-user, when a new browser window is launched from an IE mode application, it will be in a separate session, similar to the no-merge behavior in IE11. You will need to adjust your site list to configure sites that need to prevent session sharing as "no-merge". Behind the scenes, for each window of Microsoft Edge, the first time an IE mode tab is visited within that window, if it is one of the designated “no-merge” sites, that window is locked into a different “no-merge” IE session from all other Microsoft Edge windows at least until the last IE mode tab is closed in that window. This follows previous behavior where users could launch IE with no-merge and could also launch Microsoft Edge without no-merge via other mechanisms.  Additional information here: [IE mode troubleshooting and FAQ | Microsoft Docs](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--nomerge--option-that-was-supported-in-internet-explorer-11-)

- **New policy to stop implicit sign in.**  The [ImplicitSignInEnabled](/deployedge/microsoft-edge-policies#implicitsigninenabled) policy allows system administrators to disable implicit sign-in on Microsoft Edge browsers.

- **Policies to bypass ClickOnce and DirectInvoke prompts.** We have updated our policies to enable bypassing ClickOnce's prompts and DirectInvoke's app for specified file types, from specified domains. To do this, you will need to:

  - Enable [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) or [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - Enable [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes) policy and set the list of specific file types that ClickOnce and DirectInvoke should be disabled for
  - Enable the [AutoOpenAllowedForURLs](/deployedge/microsoft-edge-policies#autoopenallowedforurls) policy and set the list of specific domains that ClickOnce and DirectInvoke will be disabled for.

  Note: AutoOpenAllowedForURLs is a supporter policy for AutoOpenFileTypes. If AutoOpenAllowedForURLs is not set and AutoOpenFileTypes is set, then file types listed will automatically open from all URLs.

- **Tab Groups.**  We are turning on tab grouping which provides the ability to categorize tabs into user-defined groups and helps you more effectively find, switch and manage tabs across multiple workstreams.  

- **Hide the title bar while using Vertical Tabs.**  Get the extra few pixels back by hiding the browser's title bar, while in Vertical Tabs. Now you can go to edge://settings/appearance and under the Customize Toolbar section select the option to hide the title bar while in Vertical Tab mode.

- **Video Picture in Picture (PiP) from hover toolbar.**  When you hover over a supported video, a toolbar will appear that allows you to view that video in a PiP window.  Please note: this is currently available for Microsoft Edge users on macOS.  

- **Removal of 3DES in TLS. Support for the TLS_RSA_WITH_3DES_EDE_CBC_SHA cipher suite will be removed.** This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, navigate to the [Chrome Platform Status entry](https://chromestatus.com/feature/6678134168485888). Additionally, in Microsoft Edge version 93, the [TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled) policy will be available to support scenarios that need to preserve compatibility with outdated servers. This compatibility policy will become obsolete and stop working in Microsoft Edge version 95. Ensure that you update affected servers before then.

***New Policies***

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
- [WAMAuthBelowWin10RS3Enabled](/DeployEdge/microsoft-edge-policies#wamauthbelowwin10rs3enabled) WAM for authentication below Windows 10 RS3 enabled

***Deprecated Policy***

- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) Enable default legacy SameSite cookie behavior setting

***Obsoleted Policy***

- [NewTabPageSetFeedType](/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) Configure the Microsoft Edge new tab page experience

***Additional Change***

- [ConfigureShare](/DeployEdge/microsoft-edge-policies#configureshare) Add mac platform support
- [PasswordMonitorAllowed](/DeployEdge/microsoft-edge-policies#passwordmonitorallowed) Add mac platform support

## Version 92.0.902.84: August 26

Fixed various bugs & performance issues.

## Version 92.0.902.78: August 19

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-19-2021).

## Version 92.0.902.73: August 12

Fixed various bugs & performance issues.

## Version 92.0.902.67: August 5

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#august-05-2021).

## Version 92.0.902.62: July 29

Fixed various bugs & performance issues.

### Modified Policy

- AutoplayAllowed – Setting to “Disabled” now sets media autoplay to “Limit”

## Version 92.0.902.55: July 22

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#july-22-2021).

### Feature updates

**Users can easily get to Internet Explorer mode on Microsoft Edge**. Starting with Microsoft Edge version 92, users can reload a site in Internet Explorer mode on Microsoft Edge instead of relying on the standalone IE 11 application while waiting for a site to be configured in the Enterprise Mode Site List. Users will be prompted to add the site to their local site list such that navigating to the same page in Microsoft Edge will automatically render in IE mode for the next 30 days. You can use the [InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) policy to configure this experience and allow access to the IE mode entry points as well as the ability to add sites to the local site list. You can use the [InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) policy to adjust the number of days to keep sites on the local site list. Note that KB5003698 or later is required for Windows 10, version 1909; or KB5003690 or later is required for Windows 10, version 2004, Windows 10, version 20H2, or Windows 10, version 21H1 for the end-to-end experience. For more information, see [Local site list in IE mode](/deployedge/edge-ie-mode-local-site-list).

**MHTML files will default to opening in Internet Explorer mode**. Starting in Microsoft Edge version 92 Stable, MHTML file types will automatically open in Internet Explorer mode on Microsoft Edge instead of the Internet Explorer (IE11) application. This is most commonly observed while trying to view Outlook emails in a browser. This change will occur only if IE11 is the default handler for this file type. If you'd prefer to change this, you can do so prior to installing the Stable version 92 update using [this guidance](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

**"Disable developer mode extensions" warning can be dismissed for 2 weeks**. Beginning with Microsoft Edge version 92, you can snooze the warning "Disable developer mode extensions" for 2 weeks by selecting the option in the warning dialog dropdown.

**Manage your extensions right from the toolbar**. The all-new extensions menu on the toolbar will allow you to hide/pin extensions easily. The quick links to manage extensions and find new extensions will make it easy for you to find new extensions and manage your existing ones.

**Default for autoplay will be set to Limit**.  To help you maintain your focus online, we have changed the default for autoplaying media to Limit from Allow, beginning with Microsoft Edge version 92.

**Payment instruments are now synced across devices**. Beginning with Microsoft Edge version 92, you have the option to synchronize your payment information across your signed in devices. Please note: this is a Controlled Feature Rollout. If you don’t see this feature, please check back shortly as we continue our rollout.
Currently this feature is available only in the US and only for MSA users (not AAD)

**Improvements to font rendering**. Improvements have been made to the rendering of text to improve clarity and reduce blurriness. Please note: this is a Controlled Feature Rollout. If you don’t see this feature, please check back shortly as we continue our rollout.

**Toolbar button features like Favorites and Collections will remember the user's choice to pin them to the side of the window**. Now enabled by default, if the user chooses to pin a toolbar button, it will always open in the pinned state until they decide to unpin.

**Users can now manage the 'Allow single sign-on for work or school sites using this profile' option via group policy**.  'Allow single sign-on for work or school sites using this profile' allows non-AAD profiles to be able to use single sign-on for work or school sites using work or school credentials present on the machine. This option shows up for end-users as a toggle in Settings -> Profiles -> Profile Preferences for non-AAD profiles only.  You can use the [AADWebSiteSSOUsingThisProfileEnabled](/deployedge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) policy to configure the behavior.  

**Password health**
It’s important to use strong, unique passwords across different accounts to stay safe online. However, that's easier said than done and most users exhibit poor password habits like using weak passwords that are easy to guess, or reuse the same strong passwords across accounts.

With this latest version of Microsoft Edge, your task of using strong and unique passwords becomes a little bit easier! Microsoft Edge will now tell you whether saved passwords are strong enough and also indicate whether they’ve been used across multiple sites, helping you stay safer online. You can find your password health information in your list of saved passwords in the edge://settings/passwords page.
  
**Added privacy for your saved passwords**
If you are using a device you share with others or have left your computer unlocked for whatever reason, you can now opt for a second verification using your device password to avoid others getting access to your website passwords. Simple!

**Outlook extension**.  Stay on top of your Microsoft Outlook inbox, calendar, tasks and more without having to open a new browser window.  You can get the new Outlook extension here: [Microsoft Outlook - Microsoft Edge Addons](https://microsoftedge.microsoft.com/addons/detail/microsoft-outlook/kkpalkknhlklpbflpcpkepmmbnmfailf?hl=en-US)

**In alignment with the Chromium open source project, Microsoft Edge is updating the way it renders tables on web pages**. This change fixes known issues and brings Microsoft Edge closer to the specified way tables are meant to render across the web/other browsers. We recommend that you test important workflows in your environment for unexpected issues. A full explainer is available [here](https://docs.google.com/document/d/16PFD1GtMI9Zgwu0jtPaKZJ75Q2wyZ9EZnVbBacOfiNA/edit).

### New Policies

- [AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) Single sign-on for work or school sites using this profile enabled
- [AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault) Configure Automatic HTTPS
- [HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled) Control use of the Headless Mode
- [InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) Specifies whether to allow insecure websites to make requests to more-private network endpoints
- [InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls) Allow the listed sites to make requests to more-private network endpoints from insecure contexts
- [InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) Specify the number of days that a site remains on the local IE mode site list
- [InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) Allow unconfigured sites to be reloaded in Internet Explorer mode
- [SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed) Specifies whether SharedArrayBuffers can be used in a non cross-origin-isolated context

### Deprecated Policy

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) Allow Internet Explorer mode testing

### Obsoleted Policy

- [EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) Allow certificates signed using SHA-1 when issued by local trust anchors

## Version 91.0.864.71: July 19

> [!Important]
>This update contains a fix for [CVE-2021-30563](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30563) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#july-19-2021).

## Version 91.0.864.67: July 8

Fixed various bugs and performance issues.

## Version 91.0.864.64: July 2

Fixed various bugs and performance issues.

## Version 91.0.864.59: June 24

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-24-2021).

## Version 91.0.864.54: June 18

> [!Important]
> This update contains a fix for [CVE-2021-30554](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30554) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-18-2021).

## Version 91.0.864.48: June 11

> [!Important]
>This update contains a fix for [CVE-2021-30551](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30551) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-11-2021).

## Version 91.0.864.41: June 3

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#june-3-2021).

## Version 91.0.864.37: May 27

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-27-2021).

### Feature updates

- **Identify network traffic originating from Microsoft Defender Application Guard containers at the proxy level**. Starting with Microsoft Edge version 91, there’s built in support to tag network traffic originating from Application Guard containers, allowing enterprises to identify them and apply specific policies.

- **Support option to allow synchronizing Favorites from the host to the Edge Application Guard container**. Starting with Microsoft Edge version 91, users have the option to configure Application Guard to synchronize their favorites from the host to the container. This ensures new favorites appear on the container as well.

- **Starting with Microsoft Edge version 91 the browser will automatically interrupt downloads of types which could harm your computer if those downloads are started without a user interaction and are not supported by SmartScreen Application Reputation check**. Users may override and continue to download by right clicking and choosing “Keep” on the download item. Enterprise administrators may opt out of this behavior by configuring the following policy:
  - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings.md) - Disable download file type extension-based warnings for specified file types on domains

    For more information, see [Microsoft Edge Security downloads interruptions](microsoft-edge-security-downloads-interruptions.md).

- **Support for Speech Recognition APIs**. Starting with Microsoft Edge version 91, API support for speech recognition commands on Google.com and similar sites will be added. This feature is limited to a randomly selected group of users who have enabled experimentation. These users are giving feedback to the feature team.

- **Personalize your browser with new theme colors**. Make Microsoft Edge your own with one of the fourteen new theme colors on the Settings -> Appearance page. You can also install custom themes from the Microsoft Edge Add-on site. [Learn more](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

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

<!-- Archive from 89.0.774.45: March 4 to 90.0.818.66: May 20 ->
<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
