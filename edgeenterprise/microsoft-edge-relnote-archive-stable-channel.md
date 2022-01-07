---
title: "Archived release notes for Microsoft Edge Stable Channel"
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 01/06/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Archived release notes for Microsoft Edge Stable Channel"
---

# Archived release notes for Microsoft Edge Stable Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Stable Channel. All the security updates are listed [here](microsoft-edge-relnotes-security.md).

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

**MHTML files will default to opening in Internet Explorer mode**. Starting in Microsoft Edge version 92 Stable, MHTML file types will automatically open in Internet Explorer mode on Microsoft Edge instead of the Internet Explorer (IE11) application. This is most commonly observed while trying to view Outlook emails in a browser. This change will occur only if IE11 is the default handler for this file type. If you'd prefer to change this, you can do so prior to installing the Stable version 92 update using [this guidance](/docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).

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

## Version 90.0.818.66: May 20

Fixed various bugs and performance issues.

## Version 90.0.818.62: May 13

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#may-13-2021).

## Version 90.0.818.56: May 6

Fixed various bugs and performance issues.

## Version 90.0.818.51: April 29

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-29-2021).

## Version 90.0.818.49: April 26

Fixed various bugs and performance issues.

## Version 90.0.818.46: April 22 ##

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-22-2021).

## Version 90.0.818.42: April 19

Fixed various bugs and performance issues.

## Version 90.0.818.41: April 16 ##

> [!Important]
>This update contains a fix for [CVE-2021-21224](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21224) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-16-2021).

## Version 90.0.818.39: April 15 ##

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-15-2021).

## Feature updates ##

-	 **Single Sign On (SSO) is now available for Azure Active Directory (Azure AD) accounts and Microsoft Account (MSA) on macOS.** A user signed in on Microsoft Edge on macOS will now get automatically signed into websites that are configured to allow single sign on with Work and Microsoft accounts (for example, bing.com, office.com, msn.com, and outlook.com).

- **Kiosk mode.** Starting with Microsoft Edge version 90, we have locked down the UI print settings to only allow the configured printers and “Print to PDF” options. We have also done improvements within the assigned access single app kiosk mode to restrict the launch of other applications from the browser. For more information about the kiosk mode features please go [here](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features).

- **Interrupt Downloads** Starting with Microsoft Edge version 91 the browser will automatically interrupt downloads of types which could harm your computer if those downloads are started without a user interaction and are not supported by SmartScreen Application Reputation check. Users may override and continue to download by right clicking and choosing “Keep” on the download item.
Enterprise administrators may opt out of this behavior one of these two policies:
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains
For more information, see [Microsoft Edge Security downloads interruptions](/deployedge/microsoft-edge-security-downloads-interruptions)

- **Printing**:

    - **New print rasterization mode for non-PostScript printers.** Starting with Microsoft Edge version 90, Admins can use a new policy to define print rasterization mode for their users. This policy controls how Microsoft Edge prints to non-PostScript printers on Windows. Sometimes print jobs on non-PostScript printers need to be rasterized to print correctly. The print options are Full and Fast.
    
  -	**Additional page scaling options for printing.** Users are now able to customize scaling while printing webpages and PDF documents using additional options. The "Fit to Page" option ensures that the webpage or document is fit into the space available in the selected "Paper size" for printing. The "Actual size" option ensures that there are no changes in the size of the contents being printed regardless of the selected "Paper size".

-	**Productivity:**

    -	**Autofill suggestions are extended to include address fields content from clipboard.** Clipboard content is parsed when you click on a profile/address field (for example, phone, email, zip code, city, state, etc.) to show as autofill suggestions.

    -	**Users can search for autofill suggestions even if a form or field isn’t detected.** Today if you have your information saved on Microsoft Edge, autofill suggestions pop up automatically and help you save time while filling out forms. In cases where autofill misses a form, or if you want to fetch data in forms that don't typically have autofill (like temporary forms), you can search for your information use autofill.

-	**Access downloads from a flyout in the menu bar.** Downloads will appear in the top-right corner with all the active downloads in one place. This menu is easily dismissible so users can continue browsing uninterrupted, and they can monitor overall download progress right from the toolbar. [Learn more](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).

-	**Improvements to font rendering.** Starting with Microsoft Edge version 90, we made improvements to the rendering of text to improve clarity and reduce blurriness. Part of the font rendering improvements will land in Beta version 90 but are disabled by default.

- **Kids mode.** We have updated the policy so that when the policy is enabled, it will disable the Kid Mode feature in addition to family safety. More about Kids Mode [here](https://go.microsoft.com/fwlink/?linkid=2146910)

## Policy updates

## New policies

Eight new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added:
-	[ApplicationGuardFavoritesSyncEnabled](/DeployEdge/microsoft-edge-policies#applicationguardfavoritessyncenabled) - Application Guard Favorites Sync Enabled
- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) Application Guard Traffic Identification
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) Explicitly allowed network ports
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) Allow importing of startup page settings
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) Let users snip a Math problem and get the solution with a step-by-step explanation in Microsoft Edge
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) Allow Microsoft News content on the new tab page
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) Allow quick links on the new tab page
-	[FetchKeepaliveDurationSecondsOnShutdown](/DeployEdge/microsoft-edge-policies#fetchkeepalivedurationsecondsonshutdown)- Fetch keepalive duration on shutdown
-	[ManagedConfigurationPerOrigin](/DeployEdge/microsoft-edge-policies#managedconfigurationperorigin) - Sets managed configuration values for websites to specific origins
-	[PrintRasterizationMode](/DeployEdge/microsoft-edge-policies#printrasterizationmode) - Print Rasterization Mode
-	[QuickViewOfficeFilesEnabled](/DeployEdge/microsoft-edge-policies#quickviewofficefilesenabled) - Manage QuickView Office files capability in Microsoft Edge
-	[SSLErrorOverrideAllowedForOrigins](/DeployEdge/microsoft-edge-policies#sslerroroverrideallowedfororigins) - Allow users to proceed from the HTTPS warning page for specific origins
-	[WindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#windowocclusionenabled) - Enable Window Occlusion
-	[WindowsHelloForHTTPAuthEnabled](/DeployEdge/microsoft-edge-policies#windowshelloforhttpauthenabled) - Windows Hello For HTTP Auth Enabled

## Deprecated policies

- [ProactiveAuthEnabled](/DeployEdge/microsoft-edge-policies#proactiveauthenabled) Enable Proactive Authentication
-	[NativeWindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - Enable Native Window Occlusion
-	[SSLVersionMin](/DeployEdge/microsoft-edge-policies#sslversionmin)- Minimum TLS version enabled

## Version 89.0.774.77: April 14

> [!Important]
>This update contains a fix for  [CVE-2021-21206](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21206) and [CVE-2021-21220](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21220) which has been reported by the Chromium team as having an exploit in the wild.  For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#april-14-2021).

## Version 89.0.774.76: April 12

Fixed various bugs and performance issues.

## Version 89.0.774.75: April 8

Fixed various bugs and performance issues.

## Version 89.0.774.68: April 1

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#april-1-2021).

## Version 89.0.774.63: March 25

Fixed various bugs and performance issues.

## Version 89.0.774.57: March 18

Fixed various bugs and performance issues.

## Version 89.0.774.54: March 13

> [!IMPORTANT]
> This update contains [CVE-2021-21193](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21193) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#march-13-2021).

## Version 89.0.774.50: March 10

Fixed various bugs and performance issues.

## Version 89.0.774.48: March 8

Fixed various bugs and performance issues.

<!-- begin major 89 -->

## Version

> [!IMPORTANT]
> This update contains [CVE-2021-21166](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21166) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#march-4-2021).

### Resolved issues

- **Taskbar and Start menu shortcut updates and fixes:**
  - Right-clicking the Microsoft Edge shortcut in the Start menu will now properly show the option to unpin Microsoft Edge from the taskbar when it’s pinned.
  - Start layouts that include a [taskbar configuration](/windows/configuration/configure-windows-10-taskbar) to pin Microsoft Edge to the taskbar will no longer result in a second Microsoft Edge shortcut getting pinned to the taskbar.
  - Organizations using Windows Roaming Profiles will no longer see a blank white icon in place of the Microsoft Edge icon on the taskbar when their users log on to Windows.

### Feature updates

- **Kiosk mode enables additional lockdown capabilities**. Starting with Microsoft Edge version 89, we have added additional lockdown capabilities within kiosk mode to enable customers to get the job done in a productive and more secure experience. [Learn more](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **The Enterprise Mode Site List Manager tool will be available in the browser through the *edge://compat* page**. You can use this tool to create, edit and export your site list XML for Internet Explorer mode on Microsoft Edge. You can enable access to this tool as needed through group policy. [Learn More](./edge-ie-mode-site-list-manager.md).

- **Improve browser performance with sleeping tabs**. Sleeping tabs improves browser performance by putting inactive tabs to sleep to free up system resources like memory and CPU so active tabs or other applications can use them. Users can prevent sites from going to sleep and configure the length of time before an inactive tab goes to sleep. To keep users in their flow, there are also [heuristics](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) to prevent certain sites from going to sleep, such as intranet sites. This feature can be managed with group policies.

- **Reset your Microsoft Edge sync data in the cloud manually**. We are introducing a way to reset your Microsoft Edge sync data from within the product. This ensures that your data is cleared from Microsoft services, as well as resolving certain product issues that previously required a support ticket.

- **Intelligent enablement of Single sign-on (SSO) for all Windows Azure Active Directory (Azure AD) accounts for users with a single non-Azure AD Microsoft Edge profile**.  Automatically turn this setting on for users that might benefit the most from this feature. If a user has only one Microsoft Edge profile (and it’s not Azure AD or Kids Mode), the setting will be automatically turned on when Microsoft Edge launches. This auto-toggle will also automatically turn off if a user later chooses to sign into a different Microsoft Edge profile with an Azure AD account. Users can manually update their preferences for this feature in **Settings > Profiles >Profile Preferences > Allow single sign-on for work or school sites using this profile**.

- **Improvements to text selection experience within PDF documents**. Users will begin to get a smoother and more consistent text selection experience across PDF documents opened in Microsoft Edge starting with version 89.

- **Date of birth field now supported in autofill**. Today Microsoft Edge helps you save time and effort while filling out forms and creating accounts online by auto filling your data like addresses, names, phone numbers, etc. Starting with Microsoft Edge version 89, we are adding support for another field that you can have saved and auto-filled - date of birth. You can view, edit and delete this information anytime in your profile settings.

### Policy updates

#### New policies

Seven new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added.

- [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime) - Browsing Data Lifetime Settings
- [MAMEnabled](./microsoft-edge-policies.md#mamenabled) - Mobile App Management Enabled
- [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages) - Define an ordered list of preferred languages that websites should display in if the site supports the language
- [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled) - Allow recommendations and promotional notifications from Edge
- [PrintingAllowedBackgroundGraphicsModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes) - Restrict background graphics printing mode
- [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault) - Default background graphics printing mode
- [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist) - Block smart actions  for a list of services

#### Obsoleted policies

The following policies are obsoleted.

- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) - Use a default referrer policy of no-referrer-when-downgrade
- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - Enable usage and crash-related data reporting
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - Send site information to improve Microsoft services

<!-- end major 89 -->

## Version 88.0.705.81: February 25

Fixed various bugs and performance issues.

## Version 88.0.705.74: February 17

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#february-17-2021).

## Version 88.0.705.68: February 11

Fixed various bugs and performance issues.

## Version 88.0.705.63: February 5

> [!IMPORTANT]
> This update contains [CVE-2021-21148](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21148) which has been reported by the Chromium team as having an exploit in the wild.

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#february-5-2021).

## Version 88.0.705.62: February 4

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#february-4-2021).

Fixed various bugs and performance issues.

## Version 88.0.705.56: January 28

Fixed various bugs and performance issues.

## Version 88.0.705.53: January 26

Fixed various bugs and performance issues.

## Version 88.0.705.50: January 21

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#january-21-2021).

<!--- begin major 88  --->
### Feature updates

- **Deprecations:**

  - Deprecate support for FTP protocol. Support for the legacy FTP protocol has been removed from Microsoft Edge. Attempting to navigate to an FTP link will result in the browser directing the Operating System to open an external application to handle the FTP link. Alternatively, IT administrators can configure Microsoft Edge to use IE Mode for sites that rely on the FTP protocol.
  - Adobe Flash support will be removed. Starting with Microsoft Edge Beta version 88, Adobe Flash capability and support will be removed. Learn more: [Update on Adobe Flash Player End of Support - Microsoft Edge Blog (windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Authentication:**

  - Single Sign On (SSO) now available for Azure Active Directory (Azure AD) accounts and Microsoft Account (MSA) on down-level Windows. A user signed in on Microsoft Edge on down-level Microsoft Windows (7, 8.1) will now get automatically signed into websites that are configured to allow single sign on with Work and Microsoft accounts (e.g., bing.com, office.com, msn.com, outlook.com).<br>Note: A user may have to sign out and then sign back in if they'd signed into Microsoft Edge in a version prior to Microsoft Edge 88 to leverage this feature.
  
  - Single sign-on (SSO) to work sites using any Windows Azure Active Directory (Azure AD) accounts on system in non-Azure AD Microsoft Edge profiles. This feature can be enabled for any profile that isn’t signed-in with a work/school account and is not guest or in-private and allows the use of any signed-in work/school account on operating system with that profile. This feature can be configured in **Settings** > **Profiles** > **Profile Preferences** > **Allow single sign-on for work or school sites using this profile**.
  
    > [!NOTE]
    > "Single sign-on (SSO) for all Windows accounts using the Microsoft Edge profile" is an update to the January 21 release notes.

- **Kiosk mode option to end session**. The "End session" button is now available in a kiosk mode public browsing experience. This feature ensures that browser data and settings are deleted when Microsoft Edge is closed. Learn more about kiosk mode features and roadmap, [Configure Microsoft Edge kiosk mode](./microsoft-edge-configure-kiosk-mode.md).

- **Security and Privacy:**

  - Alerts are generated if a user's password is found in an online leak. User passwords are checked against a repository of known-breached credentials and sends the user an alert if a match is found. To ensure security and privacy, user passwords are hashed and encrypted when they're checked against the database of leaked credentials.
  - Automatically upgrade mixed content. Secure pages delivered over HTTPS may contain references images that are served over non-secure HTTP. To improve privacy and security in Microsoft Edge 88, those images will be retrieved over HTTPS instead. If the image is not available over HTTPS, it will not be loaded.
  - View site permissions by site and by recent activity. Starting with Microsoft Edge 88, users will be able to manage site permissions more easily. They will be able to view permissions by web site rather than just permission type. Additionally, we’ve added a recent activity section that will show a user all the recent changes to their site permissions.
  - Increased controls for browser cookies. Starting with Microsoft Edge 88, users can delete third party cookies without affecting first party cookies. Users will also be able to filter their cookies by first or third party and sort by name, number of cookies, and the amount of data stored and last modified.

- **Passwords:**

  - Password Generator. Microsoft Edge offers a built-in strong password generator that you can use when signing up for a new account or when changing an existing password. Just look for the browser-suggested password drop down in the password field and when selected, it will automatically save to the browser and sync across devices for easy future use.
  - Password Monitor. When any of your passwords saved to the browser matches with those seen in the list of leaked credentials, Microsoft Edge will notify you and prompt you to update your password. Password Monitor scans for matches on your behalf and is on by default.
  - Edit Password. You can now edit your saved passwords directly in Microsoft Edge Settings. Any time a password has been updated outside of Microsoft Edge, it’s easy to replace the saved older password with the new one by editing the saved entry in Settings. 

- **Improve Microsoft Edge startup speed with startup boost**. To improve Microsoft Edge startup speed, we’ve developed a feature named startup boost. Startup boost makes Microsoft Edge launch faster by enabling Microsoft Edge to run in the background. Note: This feature is limited to a randomly selected group of users who have enabled experimentation. These users are giving feedback to the feature team.

- **Productivity:**

  - Improve productivity and multi-tasking with vertical tabs. As the number of horizontal tabs grows, site titles start to get cut off and tab controls are lost as each tab shrinks. This interrupts user workflow as they spend more time finding, switching, and managing their tabs and less time on the task at hand. Vertical tabs let users move their tabs to the side, where vertically aligned icons and longer site titles make it easier to quickly scan, identify and switch to the tab they want to open.
  - Auto filling the date of birth field. Microsoft Edge already helps save time and effort while filling out forms and creating accounts online by auto filling user data such as addresses, names, phone numbers, etc. Microsoft Edge now supports the date of birth field which users can save and auto fill. A user can view, edit and delete this information anytime in their profile settings.
  - Improvements to Recently closed in History. Recently closed now keeps the last 25 tabs and windows from any past browsing session rather than just the previous session. Users can select Recently closed in the new History experience to see all the tabs that were open.
  - “Your day at a glance” feature enabled by default. Starting with Microsoft Edge version 88, information workers can benefit from intelligent productivity features on their New tab page (NTP). Microsoft Edge 87 users will also experience these features within 2 weeks after Microsoft Edge 88 release. We offer users signed in with their work or school account personalized and relevant content powered by their M365 Graph. Users can quickly scan their “Your day at a glance” modules to easily track their meetings and recent work as well as quickly launch the applications they want to use.

- **History and open tabs sync**. History and open tabs sync is now available for users to enjoy. Enabling these features will help users pick up where they left off by making their browsing history and open tabs available on all their syncing devices. We've updated sync and browser history policies, so now users are connected and productive across any devices by using Microsoft Edge. [Learn more](https://blogs.windows.com/windowsexperience/2021/01/21/this-year-lets-resolve-to-make-the-most-of-our-time-online-and-better-protect-ourselves-from-online-threats/).

- **PDF:**

  - PDF document display in book view (two page). Starting with Microsoft Edge version 88, users can view PDF documents in a single page or in the two page book view. To change the view, click the **Page View** button in the toolbar.
  - Anchored text notes support for PDF files. Starting with Microsoft Edge version 87, users can add typed text notes on any piece of text in PDF files.

- **Fonts:**

  - Browser icons are updated to the Fluent design system. As part of our continued work around Fluent Design in the browser, we've made changes to closer align icons to the new Microsoft icon system. These changes will impact many of our high-touch user interfaces, including tabs, address bar, as well as navigational and wayfinding icons found in our various menus.
  - Improved font rendering. Text rendering is improved for better clarity and to reduce blurriness.

### Policy updates

#### New policies

Eighteen new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added.

- [BasicAuthOverHttpEnabled](./microsoft-edge-policies.md#basicauthoverhttpenabled) - Allow Basic authentication for HTTP.
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
- [TargetBlankImpliesNoOpener](./microsoft-edge-policies.md#targetblankimpliesnoopener) - Do not set window.opener for links targeting _blank.
- [UpdatePolicyOverride](./microsoft-edge-policies.md#updatepolicyoverride) - Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.
- [VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) - Configures availability of a vertical layout for tabs on the side of the browser.
- [WebRtcAllowLegacyTLSProtocols](./microsoft-edge-policies.md#webrtcallowlegacytlsprotocols) - Allow legacy TLS/DTLS downgrade in WebRTC.
- [WebWidgetAllowed](./microsoft-edge-policies.md#webwidgetallowed) - Enable the Web widget.
- [WebWidgetIsEnabledOnStartup](./microsoft-edge-policies.md#webwidgetisenabledonstartup) - Allow the Web widget at Windows startup.

#### Deprecated Policies

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) - Enable Proactive Authentication.
- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist) - Configure proxy bypass rules.
- [ProxyMode](./microsoft-edge-policies.md#proxymode) - Configure proxy server settings.
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl) - Set the proxy .pac file URL.
- [ProxyServer](./microsoft-edge-policies.md#proxyserver) - Configure address or URL of proxy server.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) - Allow WebDriver to Override Incompatible Policies.

### Obsoleted Policies

- [AllowPopupsDuringPageUnload](./microsoft-edge-policies.md#allowpopupsduringpageunload) - Allows a page to show popups during its unloading.
- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting) - Default Adobe Flash setting.
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls) - Allow the Adobe Flash plug-in on specific sites.
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls) - Block the Adobe Flash plug-in on specific sites.
- [RunAllFlashInAllowMode](./microsoft-edge-policies.md#runallflashinallowmode) - Extend Adobe Flash content setting to all content.
<!--- end major 88  --->
## Version 87.0.664.75: January 7

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#january-7-2021).

## Version 87.0.664.66: December 17

Fixed various bugs and performance issues.

## Version 87.0.664.60: December 10

Fixed various bugs and performance issues.

## Version 87.0.664.57: December 7

Fixed various bugs and performance issues. Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#december-7-2020).

## Version 87.0.664.55: December 3

Fixed various bugs and performance issues. The following feature was updated for this release.

- **Shopping is enabled by default**. Starting with Microsoft Edge version 87, enterprise users can benefit from shopping in Microsoft Edge. With Shopping features, Microsoft Edge helps users find coupons and better prices while shopping online. (The coupon experience was released with Stable version 87.0.664.41). The price comparison experience is now available with this update. This feature can be configured using the [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) policy. See our [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) and [Learn More](/microsoft-edge/privacy-whitepaper#shopping) about Microsoft Shopping.

## Version 87.0.664.52: November 30

Fixed various bugs and performance issues.

## Version 87.0.664.47: November 23

Fixed various bugs and performance issues.

<!-- begin major 87 --->
## Version 87.0.664.41: November 19

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#november-19-2020).

### Feature updates

- **Automatic redirection for incompatible sites from Internet Explorer to Microsoft Edge**. Starting with the Microsoft Edge 87 Stable update, public websites that show an incompatibility message on Internet Explorer will be automatically redirected to Microsoft Edge. To learn more and to configure this experience, see [Redirecting incompatible sites](./edge-learnmore-neededge.md).

- **Kiosk mode privacy features enabled**. Starting with Microsoft Edge version 87, kiosk mode features that will help enterprises around the privacy of user data will be enabled. These features will enable experiences such as clear the user data on exit, delete downloaded files and to reset the configured start experience after a specified amount of idle time. Learn more about how to [Configure Microsoft Edge kiosk mode](./microsoft-edge-configure-kiosk-mode.md)

- **Shopping features enabled by default**. Starting with Microsoft Edge version 87 enterprise users can also benefit from shopping in Edge. With Shopping features, Microsoft Edge helps users to find coupons and better prices while shopping online. Coupon experience is available with this update and price comparison will be released in upcoming updates for Microsoft Edge 87. This feature can be configured through [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) policy. See our [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) and [Learn More](/microsoft-edge/privacy-whitepaper#shopping) about Microsoft Shopping.

- **ClickOnce deployment enabled by default**. ClickOnce is enabled by default in Microsoft Edge 87, which reduces the barriers for enterprises to deploy software and better align with Microsoft Edge Legacy browser behavior. Starting in Microsoft Edge 87, the ClickOnceEnabled policy's "Not configured" state will reflect the new default ClickOnce state of Enabled (as compared to the previous default state of Disabled).

- **The enterprise new tab page (NTP) integrates productivity with customizable, work-relevant feed content**. The enterprise NTP blends the Office 365 productivity page we offer to users signed in with their work or school account with personalized, work-relevant company and industry feeds that are organized in a single page. Users will be able to recognize the familiar Office 365 content and Microsoft Search for Business powered by Bing. In addition, they can easily customize "My Feed" by choosing the most relevant content to them from the available content and modules for their organization. IT Administrators can control the News feed settings for their  organization, including the selected industry for the Edge new tab page by going to Microsoft 365 admin center. [Learn more](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/)

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
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) - Shopping in Microsoft Edge enabled.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](./microsoft-edge-policies.md#hideinternetexplorerredirectuxforincompatiblesitesenabled) - Hide the one-time redirection dialog and the banner on Microsoft Edge.
- [KioskAddressBarEditingEnabled](./microsoft-edge-policies.md#kioskaddressbareditingenabled) - Configure address bar editing for kiosk mode public browsing experience.
- [KioskDeleteDownloadsOnExit](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) - Delete files downloaded as part of kiosk session when Microsoft Edge closes.
- [PasswordRevealEnabled](./microsoft-edge-policies.md#passwordrevealenabled) - Enable Password reveal button.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerpreventbhoinstall) - Prevent install of the browser helper object (BHO) to redirect incompatible sites from Internet Explorer to Microsoft Edge.
- [RedirectSitesFromInternetExplorerRedirectMode](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerredirectmode) - Redirect incompatible sites from Internet Explorer to Microsoft Edge.
- [SpeechRecognitionEnabled](./microsoft-edge-policies.md#speechrecognitionenabled) - Configure Speech Recognition.
- [WebCaptureEnabled](./microsoft-edge-policies.md#webcaptureenabled) - Enable web capture feature in Microsoft Edge.

#### Deprecated Policy

[NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype) - Configure the Microsoft Edge new tab page experience.

#### Obsoleted Policy

[EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures) - Re-enable deprecated web platform features for a limited time.

<!-- end major 87 -->

## Version 86.0.622.69: November 13

> [!IMPORTANT]
> This update contains [CVE-2020-16013](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16013) and [CVE-2020-16017](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16017), that have been reported by the Chromium team as having an exploit in the wild.

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#november-13-2020).

## Version 86.0.622.68: November 11

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#november-11-2020)

## Version 86.0.622.63: November 4

> [!IMPORTANT]
> This update contains [CVE-2020-16009](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16009), that has been reported by the Chromium team as having an exploit in the wild.

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#november-4-2020).

## Version 86.0.622.61: November 2

Fixed various bugs and performance issues.

## Version 86.0.622.58: October 29

Fixed various bugs and performance issues.

## Version 86.0.622.56: October 27

Fixed various bugs and performance issues.

## Version 86.0.622.51: October 22

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#october-22-2020)

## Version 86.0.622.48: October 20

Fixed various bugs and performance issues.

## Version 86.0.622.43: October 15

Fixed various bugs and performance issues.

## Version 86.0.622.38: October 9

Security updates are listed [here](./microsoft-edge-relnotes-security.md#october-9-2020)

### Feature updates

* **Roll back to previous Microsoft Edge version.** The rollback feature lets administrators revert to a known good version of Microsoft Edge if there's an issue in the latest version of Microsoft Edge. **Note:** Stable version 86.0.622.38 is the first version you can roll back to, which means that Stable version 87 is the first version ready to rollback from. [Learn more](edge-learnmore-rollback.md).

* **Enforce enabling Sync by default across the enterprise.**  Administrators can enable synchronization for Azure Active Directory (Azure AD) accounts by default with the [ForceSync](./microsoft-edge-policies.md#forcesync) policy.

* **Automatic profile switching on Windows 7 and 8.1.** The automatic profile switching currently available in Microsoft Edge on Windows 10 is extended to downlevel Windows (Windows 7 and 8.1). For more information, see the [automatic profile switching](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) blog post.

* **SameSite=Lax Cookies By Default**. To improve web security and privacy, cookies will now default to [SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite) handling by default. This means that cookies will only be sent in a first-party context and will be omitted for requests sent to third-parties. This change can cause compatibility impact on websites that require cookies for third-party resources to function correctly. To permit such cookies, web developers can mark cookies which should be set from and sent to third-party contexts by adding explicit `SameSite=none` and `Secure` attributes when the cookie is set. Enterprises that wish to exempt certain sites from this change can do so using the [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) policy, or can opt-out of the change across all sites using the [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled) policy.

* **Remove the HTML5 Application Cache API.**  Beginning with Microsoft Edge version 86, the legacy Application Cache API that enables offline use of web pages is being removed from Microsoft Edge. Web Developers should review the [WebDev documentation](https://web.dev/appcache-removal/) for information on replacing  the Application Cache API with Service Workers.  Important: You can request an [AppCache OriginTrial Token](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) that allows sites to continue to use the deprecated Application Cache API until Microsoft Edge version 90.

* **Privacy and Security:**

  * Replace [MetricsReportingEnabled](/DeployEdge/microsoft-edge-policies#metricsreportingenabled) and [SendSiteInformationToImproveServices](/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) policies for downlevel Windows and macOS. These policies are deprecated in Microsoft Edge version 86 and will become obsolete in Microsoft Edge version 89.<br>
These policies are replaced by [Allow Telemetry](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) on Windows 10, and the new [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) policy for all other platforms. This will let users manage the diagnostic data that gets sent to Microsoft for Windows 7, 8, 8.1 and macOS.
  * Secure DNS (DNS-over-HTTPS) support.  Beginning with Microsoft Edge version 86, settings to control Secure DNS on un-managed devices is available. These settings aren't accessible to users on managed devices, but IT admins can enable or disable Secure DNS using the [dnsoverhttpsmode](./microsoft-edge-policies.md#dnsoverhttpsmode) group policy.

* **Internet Explorer mode:** Let users use the Microsoft Edge User Interface (UI) to test sites in Internet Explorer mode. Beginning with Microsoft Edge version 86, administrators can enable a UI option for their users to load a tab in Internet Explorer mode for testing purposes or as a stopgap until sites are added to the site list XML.

* **PDF updates:**

  * Table of contents for PDF Documents. Beginning with version 86, Microsoft Edge has added support for table of contents that lets users easily navigate through PDF documents.
  * Access all PDF functionalities on small form factor screens. Access all the capabilities of the Microsoft Edge PDF reader on devices with small screen sizes.
  * Pen support for highlighter on PDF files. With this update, users can use their digital pen to directly highlight text on PDF files, in the same way they would with a physical highlighter and paper.
  * Improved PDF scrolling. You will now be able to experience stutter free scrolling while navigating through long PDF documents.

* **Users will see auto complete suggestions when they start typing a search query on the Microsoft Edge Add-ons website.** Auto complete will help users quickly complete their search query without having to type the entire string. This will be helpful because users won't have to remember correct spellings and they can choose from the available options that are displayed.

* **Add a custom image to the New Tab Page (NTP) using a group policy.** Beginning with Microsoft Edge version 86 the NTP has an option to replace the default image with a custom user-supplied image. The ability to manage the properties of this image is also supported by the group policy.

* **Match customized keyboard shortcuts to VS Code.** Microsoft Edge DevTools now supports customizing keyboard shortcuts in the DevTools to match with your editor/IDE. (In Microsoft Edge 84, we added the ability to match DevTools keyboard shortcuts to VS Code).

* **Delete downloads from disk using download manager.** Users are now able to delete their downloaded files from their disk without leaving the browser. The new Delete downloads functionality exists within the context menu of downloads shelf or the downloads page.

### Policy updates

#### New policies

Twenty-three new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [CollectionsServicesAndExportsBlockList](./microsoft-edge-policies.md#collectionsservicesandexportsblocklist) - Block access to a specified list of services and export targets in Collections.
- [DefaultFileSystemReadGuardSetting](./microsoft-edge-policies.md#defaultfilesystemreadguardsetting) - Control use of the File System API for reading.
- [DefaultFileSystemWriteGuardSetting](./microsoft-edge-policies.md#defaultfilesystemwriteguardsetting) - Control use of the File System API for writing.
- [DefaultSensorsSetting](./microsoft-edge-policies.md#defaultsensorssetting) - Default sensors setting.
- [DefaultSerialGuardSetting](./microsoft-edge-policies.md#defaultserialguardsetting) - Control use of the Serial API.
- [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) - Send required and optional diagnostic data about browser usage.
- [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed) - Allow access to the Enterprise Mode Site List Manager tool.
- [FileSystemReadAskForUrls](./microsoft-edge-policies.md#filesystemreadaskforurls) - Allow read access via the File System API on these sites.
- [FileSystemReadBlockedForUrls](./microsoft-edge-policies.md#filesystemreadblockedforurls) - Block read access via the File System API on these sites.
- [FileSystemWriteAskForUrls](./microsoft-edge-policies.md#filesystemwriteaskforurls) - Allow write access to files and directories on these sites.
- [FileSystemWriteBlockedForUrls](./microsoft-edge-policies.md#filesystemwriteblockedforurls) - Block write access to files and directories on these sites.
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
- [UserAgentClientHintsEnabled](./microsoft-edge-policies.md#useragentclienthintsenabled) - Enable the User-Agent Client Hints feature.
- [UserDataSnapshotRetentionLimit](./microsoft-edge-policies.md#userdatasnapshotretentionlimit) - Limits the number of user data snapshots retained for use in case of emergency rollback.

#### Deprecated Policies

- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - Enable usage and crash-related data reporting.
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - Send site information to improve Microsoft services.

#### Obsoleted Policy

[TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled) - Enable a TLS 1.3 security feature for local trust anchors.

## Version 85.0.564.70: October 6

Fixed various bugs and performance issues.

## Version 85.0.564.68: October 1

Fixed various bugs and performance issues.

## Version 85.0.564.63: September 23

Security updates are listed [here](./microsoft-edge-relnotes-security.md#september-23-2020)

## Version 85.0.564.51: September 9

Security updates are listed [here](./microsoft-edge-relnotes-security.md#september-9-2020)

## Version 85.0.564.44: August 31

Fixed various bugs and performance issues.

<!-- 85.0.564.41: August 27 -->

## Version 85.0.564.41: August 27

Security updates are listed [here](./microsoft-edge-relnotes-security.md#august-27-2020)

### Feature updates

- **On-premises synchronization of Favorites and Settings**. Now you can synchronize browser favorites and settings between Active Directory profiles within your own environment without the need for cloud sync.

- **Microsoft Edge group policy support for trusting site + app combos to launch without a confirmation prompt.**. Group policy support added that lets administrators add site + app combos that are trusted to launch without the confirmation prompt. This adds the ability for administrators to configure trusted protocol/origin combinations (such as Microsoft 365 apps) for their end-users to suppress the confirmation prompt when navigating to a URL that contains an app protocol.

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
- [EnableSha1ForLocalAnchors](./microsoft-edge-policies.md#enablesha1forlocalanchors) - Allow certificates signed using SHA-1 when issued by local trust anchors.
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](./microsoft-edge-policies.md#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains.
- [IntensiveWakeUpThrottlingEnabled](./microsoft-edge-policies.md#intensivewakeupthrottlingenabled) - Control the IntensiveWakeUpThrottling feature.
- [NewTabPagePrerenderEnabled](./microsoft-edge-policies.md#newtabpageprerenderenabled) - Enable preload of the new tab page for faster rendering.
- [NewTabPageSearchBox](./microsoft-edge-policies.md#newtabpagesearchbox) - Configure the new tab page search box experience.
- [PasswordMonitorAllowed](./microsoft-edge-policies.md#passwordmonitorallowed) - Allow users to be alerted if their passwords are found to be unsafe.
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled) - Enable using roaming copies for Microsoft Edge profile data.
- [RoamingProfileLocation](./microsoft-edge-policies.md#roamingprofilelocation) - Set the roaming profile directory.
- [TLSCsipherSuiteDenyList](./microsoft-edge-policies.md#tlsciphersuitedenylist) - Specify the TLS cipher suites to disable.

#### Obsoleted policies

- [EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) - Enable Domain Actions Download from Microsoft.
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) - Re-enable Web Components v0 API until M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies)- Allow WebDriver to Override Incompatible Policies.

## Version 84.0.522.63: August 20

Security updates are listed [here](./microsoft-edge-relnotes-security.md#august-20-2020).

## Version 84.0.522.61: August 17

Fixed various bugs and performance issues.

## Version 84.0.522.59: August 11

Security updates are listed [here](./microsoft-edge-relnotes-security.md#august-11-2020)

## Version 84.0.522.58: August 10

Fixed various bugs and performance issues.

## Version 84.0.522.52: August 1

Fixed various bugs and performance issues.

## Version 84.0.522.50: July 31

Fixed various bugs and performance issues.

## Version 84.0.522.49: July 29

Security updates are listed [here](./microsoft-edge-relnotes-security.md#july-29-2020)

## Version 84.0.522.48: July 28

Fixed various bugs and performance issues.

## Version 84.0.522.44: July 23

Fixed various bugs and performance issues.

## Version 84.0.522.40: July 16

Security updates are listed [here](./microsoft-edge-relnotes-security.md#july-16-2020)

### Feature updates

- This version of Microsoft Edge provides improved site list download times for Internet Explorer mode. We've reduced download delay for the Internet Explorer mode site list to 0 seconds (down from a 60-second wait) in the absence of a cached site list. We've also added group policy support for cases when Internet Explorer mode home page navigations need to be delayed until the site list is downloaded. For more information, see the [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload) policy.

- Microsoft Edge now allows users to sign-into the browser when it's "run as administrator" on Windows 10. This will help customers running Microsoft Edge on Windows server or in remote-desktop and sandbox scenarios.

- Microsoft Edge now provides full mouse support when in full screen mode. Now you can use your mouse to access tabs, the address bar, and other items without having to exit full screen mode.

- Online purchase improvement. Add custom nicknames to saved debit or credit cards. Now you can distinguish and differentiate your credit cards when making online purchases. Nicknaming your debit or credit cards lets you choose the correct card when using autofill to select a payment method.

- TLS/1.0 and TLS/1.1 are disabled by default.  The [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin) policy permits re-enabling of TLS/1.0 and TLS/1.1. This policy will remain available until at least Microsoft Edge version 88. For more information, see [Site compatibility-impacting changes coming to Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

- Collections improvements:

  - A note capability is added that lets you add a note or comment to an item in a collection. Notes are grouped together and stay attached to an item even if you sort the items in a collection. To try this new feature, right-click on an item and select "Add note".
  - You can change the background color of notes in collections. You can use color coding to help you organize information and increase productivity.
  - There are noticeable performance improvements, which lets you export your collections to  Excel in less time than in previous versions of Microsoft Edge.

- Additional Microsoft Edge API support:

  - The Storage Access API is enabled for experimentation. This feature is enabled for home users and Enterprise users with the [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol) policy set to "Full". This feature will be enabled by default for all users in Microsoft Edge Stable Channel version 85.
  
    As privacy is becoming increasingly important to users, requests for stricter browser defaults and user opt-in settings like blocking all third-party storage access are increasingly common. While these settings help improve privacy and block unwanted access by unknown or untrusted parties, they can have unwanted side effects such as blocking access to content the user may want to view (for example, social media and embedded media content.)

    The Storage Access API allows access to first-party storage in a third-party context when a user provides a direct intent to allow storage that would otherwise be blocked by the browser's current configuration. For more information, see [Storage Access API](https://www.chromestatus.com/feature/5612590694662144).

  - The Native File System API, which means you can give sites permissions to edit files or folders via the Native File System API.

- PDF improvements:

  - Read Aloud for PDF lets users listen to PDF content while carrying out other tasks that may be important for them. It also helps audio visual learners focus on reading the content, making learning easier.
  - PDF file editing is improved. Now you can save an edit made to a PDF back to the file instead of saving a copy each time you edit the PDF.

- Microsoft Edge now enables Translation in the Immersive Reader. When a user opens the Immersive Reader view, they get the option to translate the page to their desired language.

- Several DevTools updates, including support for customizing keyboard shortcuts to match VS Code and viewing the DevTools in high contrast.  For more details, see [What's New In DevTools (Microsoft Edge 84)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/05/devtools).

### Policy updates

#### New policies

Seven new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [AppCacheForceEnabled](./microsoft-edge-policies.md#appcacheforceenabled) - Allows the AppCache feature to be re-enabled, even if it's turned off by default.
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy) - Configure the settings for the Application Guard Container Proxy.
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload) - Require that the Enterprise Mode Site List is available before tab navigation.
- [WinHttpProxyResolverEnabled](./microsoft-edge-policies.md#winhttpproxyresolverenabled) - Use the Windows proxy resolver.
- [InternetExplorerIntegrationEnhancedHangDetection](./microsoft-edge-policies.md#internetexplorerintegrationenhancedhangdetection) - Configure enhanced hang detection for Internet Explorer mode.
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - To reduce CPU and power consumption Microsoft Edge will detect when a window is covered by other windows, and will suspend work painting pixels.
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout) - Set a timeout for delay of tab navigation for the Enterprise Mode Site List.

#### Deprecated policies

- [AllowSyncXHRInPageDismissal](./microsoft-edge-policies.md#allowsyncxhrinpagedismissal) - Allow pages to send synchronous XHR requests during page dismissal.
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) - Determines whether the built-in certificate verifier will be used to verify server certificates.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled) - Enable stricter treatment for mixed content.

#### Obsoleted policy

[ForceNetworkInProcess](./microsoft-edge-policies.md#forcenetworkinprocess) - Force networking code to run in the browser process.

<!-- End 84 -->
## Version 83.0.478.64: July 13

Fixed various bugs and performance issues.

## Version 83.0.478.61: July 7

Fixed various bugs and performance issues.

## Version 83.0.478.58: June 30

Fixed various bugs and performance issues.

## Version 83.0.478.56: June 24

Fixed various bugs and performance issues.

Security updates are listed [here](./microsoft-edge-relnotes-security.md#june-24-2020)

## Version 83.0.478.54: June 17

Security updates are listed [here](./microsoft-edge-relnotes-security.md#june-17-2020)

## Version 83.0.478.50: June 15

Fixed various bugs and performance issues.

## Version 83.0.478.45: June 4

Security updates are listed [here](./microsoft-edge-relnotes-security.md#june-4-2020)

## Version 83.0.478.44: June 1

Fixed various bugs and performance issues.

## Version 83.0.478.37: May 21

Security updates are listed [here](./microsoft-edge-relnotes-security.md#may-21-2020)

### Feature updates

- Microsoft Edge updates will now roll out gradually. Going forward, updates for Microsoft Edge will be rolled out to our users over a period of a few days. This enables us to protect more of you from accidental buggy updates, which improves your update experience. As a user you will continue to get seamless auto-updates. If your organization isn't enrolled for auto-updates you won't be affected by this change. To learn more, see the [progressive rollouts article](microsoft-edge-update-progressive-rollout.md).
- Microsoft Defender SmartScreen improvements: Made several improvements to the Microsoft Defender SmartScreen service, such as improved protection from malicious sites that redirect when loading, and top-level frame blocking, which completely replaces malicious sites with the Microsoft Defender SmartScreen safety page. The top-level frame blocking prevents audio and other media from the malicious site from playing which gives an easier and less confusing experience.

- In response to user feedback, users can now exempt certain cookies from automatically clearing when the browser closes. This option is helpful if there's a site that users don't want to be signed out of, but still want to have all the other cookies cleared when the browser closes. To use this feature, go to *edge://settings/clearBrowsingDataOnClose* and enable the "Cookies and other site data" toggle.

- Automatic Profile Switching is now available to help you get to your work content more easily across profiles. If you use multiple profiles at work, you can check it out by navigating to a site requiring authentication from your work or school account while on your personal profile. When we detect this, you will receive a prompt to switch to your work profile to access that site without having to authenticate to it. When you choose the work profile you want to switch to, the website will simply open in your work profile. This profile switching capability will help you keep your work and personal data separate and help you get to your work content more effortlessly. If you don't want the feature to prompt you to switch profiles, you can choose the don't ask me again option and it will get out of your way.

- Collections feature improvements:
  - You can use drag and drop to add an item to a collection without opening the collection. During the drag and drop you can also choose a location in the collection list where you want to put the item.
  - You can add multiple items to a collection instead of adding one item at a time. To add multiple items, select the items and then drag them to a collection. Or you can select the items, right-click and then pick the collection where you want the items.

- You can add all the tabs in an Edge window into a new collection without adding them individually. To do this, right-click on any tab and choose "Add all tabs to a new collection".

- Extension sync is now available. You can now sync your extensions across all your devices! Extensions from both the Microsoft and Chrome Stores will sync with Microsoft Edge. To use this feature: Click the ellipses (**…**) on the menu bar, select **Settings**. Under Your profile, click **Sync** to see the Sync options. Under **Profiles/Sync** use the toggle to enable Extensions. You can use the [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) group policy to disable syncing of extensions.

- Improved the message on the Downloads management page for insecure downloads that have been blocked.

- Immersive Reader improvements:
  - Added support for Adverbs in the Parts of Speech experience we have in Immersive Reader. While reading an article within the Immersive Reader, open the Grammar Tools and switch on Adverbs within Parts of Speech to highlight all the adverbs on the page.
  - Added the ability to select any content on a webpage and open it in Immersive Reader. This ability enables users to use the Immersive Reader and all the Learning Tools, such as Line Focus and Read Aloud, across all websites.

- Link doctor provides host correction and a search query to the users when they mistype a URL. For example: <br>
A user mistypes "powerbi as "powerbbi".com. Link doctor will suggest "powerbi".com as a correction and create a link to search for "powerbbi" in case the user is looking for something different.

- Allow users to save their decision to launch an external protocol for a specific site. Users can configure the [ExternalProtocolDialogShowAlwaysOpenCheckbox](/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox) policy to enable or disable this feature.

- Users can set Microsoft Edge as their default browser directly from Microsoft Edge **Settings**. This makes it easier for users to change their default browser, within the context of the browser itself, instead of having to search through the operating system settings. To use this feature, go to *edge://settings/defaultBrowser* and click **Make default**.

- Several DevTools updates, including new remote debugging support, UI improvements, and more. For more details, see [What's New In DevTools (Microsoft Edge 83)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

- MCAS (Microsoft Cloud Access Security) warn scenario is now available. This enables admins to set up warn, a new category of MCAS blocks, where the user can override a MCAS block page. MDATP E5 blocks are natively integrated with SmartScreen blocks in Microsoft Edge for a seamless experience. This experience allows for a full page red block with the message "This website is blocked by your organization", instead of just a toast notification.

- Disallow synchronous XmlHttpRequest in page dismissal. Sending of synchronous XmlHttpRequests during unload of a webpage will be removed. This change improves browser performance and reliability, but may impact web applications that have not yet been updated to use more modern web APIs, including sendBeacon and fetch. The Group Policy to disable this change and permit synchronous XHR during page dismissal will be available until Microsoft Edge 88. For more information, see [Site compatibility-impacting changes coming to Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

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

<!-- end 83 -->

## Version 81.0.416.77: May 18

Fixed various bugs and performance issues.

## Version 81.0.416.72: May 7

Security updates are listed [here](./microsoft-edge-relnotes-security.md#may-7-2020)

## Version 81.0.416.68: April 29

Security updates are listed [here](./microsoft-edge-relnotes-security.md#april-29-2020)

## Version 81.0.416.64: April 23

Security updates are listed [here](./microsoft-edge-relnotes-security.md#april-23-2020)

## Version 81.0.416.58: April 17

Security updates are listed [here](./microsoft-edge-relnotes-security.md#april-17-2020)

## Version 81.0.416.53: April 13

Security updates are listed [here](./microsoft-edge-relnotes-security.md#april-13-2020)

### Feature updates

- Added support for Windows Information Protection (WIP), which helps enterprises protect sensitive data from unauthorized disclosure. [Learn More](./microsoft-edge-security-windows-information-protection.md).

- Collections is now available. To get started, click the Collections icon next to the address bar. This action opens the Collections pane where you can create, edit, and view Collections. We designed Collections based on what you do on the web. If you're a shopper, a traveler, a teacher, or a student, Collections can help. [Learn more](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97).

- Allow the removal (Hide from toolbar) of the Collections button from the Microsoft Edge toolbar for consistency.

- On-prem Active Directory account auto sign in will only be targeted to organizations that turn it on.  If users were already signed in with an on-prem AD account, they will be able to sign out of it. Users will only be automatically signed in with the primary account on their operating system if it's a Microsoft account or an Azure Active Directory account. Admins can enable auto sign in with an on-prem AD account using the ConfigureOnPremisesAccountAutoSignIn policy.

- Application Guard. Extensions support now available in the container.

- Added a message to inform users that Internet Explorer isn't installed when they navigate to a page that's configured to open in Internet Explorer mode.

- Updated the 3D View tool in Microsoft Edge DevTools with a new feature to help debug z-index stacking context. 3D View shows a representation of the DOM (Document Object Model) depth using color and stacking, and the z-Index view helps you isolate the different stacking contexts of your page. [Learn more](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/).

- The F12 Dev tools are localized in 10 new languages, so they will match the language used in the rest of the browser. [Learn more](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/).

- Added support for Dolby Vision playback. On Dolby Vision-enabled Windows 10 Build 17134 (April 2018 Update), websites can show Dolby vision content. See how to enable Dolby Vision content from [Netflix](https://help.netflix.com/en/node/42384).

- Microsoft Edge can now identify and remove duplicate favorites and merge folders with the same name. To access the tool, click the star on the browser's toolbar and select "Remove duplicate favorites".  You can that confirm changes and any updates to your favorites will be synced across devices.

- We heard from users it can be difficult to distinguish a normal browsing window in dark theme from an InPrivate window since both window frames are dark. The new solid InPrivate blue pill in the top right corner helps reassure users they are browsing InPrivate.

- Open external links in the correct browser profile. Select a default profile for links opened for external apps to open in from *edge://settings/multiProfileSettings*.

- Added a warning that alerts users who sign into a browser profile with an account after being previously signed in with another account. This warning will help prevent unintentional data merging.

- If you have payment cards saved in your Microsoft account, you can use them in Microsoft Edge while filling out payment forms. The cards in your Microsoft account will sync across desktop devices and the full details will be shared with the website after two-factor authentication (CVC code and your Microsoft identity.) For further convenience, you can choose to securely save a copy of the card on the device during authentication.

- Line Focus is designed for users who like to focus on a limited part of the content as they read. It lets users keep the focus on one, three, or five lines at a time and dims out the rest of the page to let users read without distraction. Users can scroll using touch or arrow keys and the focus shifts accordingly.

- Microsoft Edge is now integrated with Windows Speller on Windows platforms 8.1 and above. This integration provides greater language support, with access to more language dictionaries and the ability to use Windows custom dictionaries. There's no further action needed from the users when a language has been added in the OS language settings. Also, a language spellcheck toggle is enabled in Microsoft Edge settings.

- When PDF documents are opened using Microsoft Edge, users will now be able to create highlights, change color, and delete highlights. This feature helps in referencing important parts of the document later, and for collaboration.

- When loading long PDF documents that have been optimized for web, the pages being viewed by the user will be loaded faster, parallelly, while the rest of the document is loading.

- Now it's easier to start the Immersive Reader for a website by just pressing the F9 key.

- Now it's easier to start Read Aloud by using a keyboard shortcut (Ctrl + Shift + U).

- Added an MSI command line parameter that lets you suppress Desktop icon creation when you install Microsoft Edge. The following example shows how to use this new parameter: <br>
`MicrosoftEdgeEnterpriseX64.msi DONOTCREATEDESKTOPSHORTCUT=true`<br>
There will be a group policy to support this functionality in an upcoming release.

### Policy updates

#### New policies

11 new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled) - Enable Ambient Authentication for InPrivate and Guest profiles. 
- [AudioSandboxEnabled](./microsoft-edge-policies.md#audiosandboxenabled) - Allow the audio sandbox to run.
- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) - Use a default referrer policy of no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](./microsoft-edge-policies.md#globallyscopehttpauthcacheenabled) - Enable globally scoped HTTP auth cache.
- [ImportExtensions](./microsoft-edge-policies.md#importextensions) - Allow importing of extensions.
- [ImportCookies](./microsoft-edge-policies.md#importcookies) - Allow importing of Cookies.
- [ImportShortcuts](./microsoft-edge-policies.md#importshortcuts) - Allow importing of shortcuts.
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect) - Specify how "in-page" navigations to unconfigured sites behave when started from Internet Explorer mode pages.
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled) - Enable stricter treatment for mixed content.
- [TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled) - Enable a TLS 1.3 security feature for local trust anchors.
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin) - Configure automatic sign in with an Active Directory domain account when there is no Azure AD domain account.

#### Policy name and caption changes

The policy `OmniboxMSBProviderEnabled` is changed to [AddressBarMicrosoftSearchInBingProviderEnabled](//DeployEdge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled) - The caption for the policy is "Enable Microsoft Search in Bing suggestions in the address bar".

#### Deprecated policies

The following policies continue to work in this release. They will become "obsolete" in a future release.

- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) - Re-enable Web Components v0 API until M84.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) - Allow WebDriver to Override Incompatible.

#### Resolved issues

- Fixed an issue where IE mode on Microsoft Edge caused an ongoing download dialog to show even after the file was downloaded.
- Fixed an issue where Microsoft Edge was dropping session cookies when a page already in IE mode triggered to open a new IE mode tab.

## Version 80.0.361.111: April 7

Fixed various bugs and performance issues.

## Version 80.0.361.109: April 1

Security updates are listed [here](./microsoft-edge-relnotes-security.md#april-1-2020)

## Version 80.0.361.69: March 19

Security updates are listed [here](./microsoft-edge-relnotes-security.md#march-19-2020)

## Version 80.0.361.66: March 4

Security updates are listed [here](./microsoft-edge-relnotes-security.md#march-4-2020)

## Version 80.0.361.62: February 25

Security updates are listed [here](./microsoft-edge-relnotes-security.md#february-25-2020)

## Version 80.0.361.57: February 20

Security updates are listed [here](./microsoft-edge-relnotes-security.md#february-20-2020)

## Version 80.0.361.56: February 19

Fixed various bugs and performance issues.

## Version 80.0.361.54: February 14

### Resolved issues

- Fixed an issue where Password, Payment, and Cookies fail to get imported in Microsoft Edge.

## Version 80.0.361.50: February 11

Fixed various bugs and performances fixes.

## Version 80.0.361.48: February 7

Security updates are listed [here](./microsoft-edge-relnotes-security.md#february-7-2020)

### Feature updates

- Added SmartScreen protection from downloading potentially unwanted apps. [Learn more](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus)
- Added support for Dolby Vision playback.
- Enabled users of Windows Mixed Reality to view 360° videos on VR headsets.
- Added an option to Reading View to increase text spacing.
- Added support for erasing link using the Surface Pen eraser.
- Added support for using the arrow keys and spacebar to draw on feedback screenshots in editor mode.
- Improved the reliability of screenshots so they stop appearing all black when submitting feedback.
- Added dark theme support to the local new tab page that is shown when the device isn't connected to the internet.
- Added the ability for websites that are installed as apps to be restored when a browser session is restored after an update, crash, and so on.
- Added dark theme support to PDF UI when the browser is managed by Group Policy.
- Updated Adobe Flash to version 32.0.0.321. [Learn more](https://helpx.adobe.com/flash-player/release-note/fp_32_air_32_release_notes.html)

### Policy updates

#### New policies

16 new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [AlternateErrorPagesEnabled](./microsoft-edge-policies.md#alternateerrorpagesenabled) - Suggest similar pages when a webpage can't be found.
- [DefaultInsecureContentSetting](./microsoft-edge-policies.md#defaultinsecurecontentsetting)  - Control use of insecure content exceptions.
- [DNSInterceptionChecksEnabled](./microsoft-edge-policies.md#dnsinterceptionchecksenabled) - DNS interception checks enabled.
- [HideFirstRunExperience](./microsoft-edge-policies.md#hidefirstrunexperience) - Hide the First-run experience and splash screen.
- [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) - Allow insecure content on specified sites.
- [InsecureContentBlockedForUrls](./microsoft-edge-policies.md#insecurecontentblockedforurls) - Block insecure content on specified sites.
- [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled) - Enable default legacy SameSite cookie behavior setting.
- [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) - Revert to legacy SameSite behavior for cookies on specified sites.
- [PaymentMethodQueryEnabled](./microsoft-edge-policies.md#paymentmethodqueryenabled) - Allow websites to query for available payment methods.
- [PersonalizationReportingEnabled](./microsoft-edge-policies.md#personalizationreportingenabled) - Allow personalization of ads, search, and news by sending browsing history to Microsoft.
- [PinningWizardAllowed](./microsoft-edge-policies.md#pinningwizardallowed) - Allow Pin to taskbar wizard.
- [SmartScreenPuaEnabled](./microsoft-edge-policies.md#smartscreenpuaenabled) - Configure Microsoft Defender SmartScreen to block potentially unwanted apps.
- [TotalMemoryLimitMb](./microsoft-edge-policies.md#totalmemorylimitmb) - Set limit on megabytes of memory a single Microsoft Edge instance can use.
- [WebAppInstallForceList](./microsoft-edge-policies.md#webappinstallforcelist) - Configure list of force-installed Web Apps.
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) - Re-enable Web Components v0 API until M84.
- [WebRtcLocalIpsAllowedUrls](./microsoft-edge-policies.md#webrtclocalipsallowedurls) - Manage exposure of local IP addresses by WebRTC.

#### Deprecated policies

The following policy was deprecated.

- [NewTabPageCompanyLogo](./microsoft-edge-policies.md#newtabpagecompanylogo) - Set new tab page company logo.

### Resolved issues

- Fixed an issue where audio isn't working in Citrix environment.
- Fixed an issue where Microsoft Edge and legacy Microsoft Edge side-by-side experience results in broken legacy links and crashes.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)