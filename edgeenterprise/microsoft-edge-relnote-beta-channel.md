---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 08/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Microsoft Edge release notes for Beta Channel"
---

# Release notes for Microsoft Edge Beta Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Beta Channel. Archived versions of these release notes are available [here](microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> Microsoft Edge Web Platform constantly evolves to improve user experience, security, and privacy. To learn more, see [Site compatibility-impacting changes coming to Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## Version 93.0.961.11: August 3

### Feature updates

- **Initial Preferences in Microsoft Edge.**  Starting with Microsoft Edge version 93, deploying Microsoft Edge to your enterprise will become easier with the addition of Initial Preferences.

- **IE mode on Microsoft Edge will support "nomerge" behavior.**  Starting with Microsoft Edge version 93, IE mode on Microsoft Edge will support _nomerge_. For an end user, when a new browser window is launched from an IE mode application, it will be in a separate session, similar to the behavior in IE11. You will need to adjust your site list to configure sites that need to prevent session sharing. Behind the scenes, for each window of Microsoft Edge, the first time an IE mode tab is visited within that window, if it is one of the designated “nomerge” sites, that window is locked into a different “nomerge” IE session from all other Microsoft Edge windows at least until the last IE mode tab is closed in that window. Learn more [here](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--nomerge--option-that-was-supported-in-internet-explorer-11-).

- **Tab Groups.**  The ability to categorize tabs into user-defined groups helps you more effectively find, switch, and manage tabs across multiple workstreams. To enable this, we are turning on tab grouping beginning with Microsoft Edge version 93.

- **Hide the title bar while using Vertical Tabs.**  Get the extra few pixels back by hiding the browser's title bar, while in Vertical Tabs. Starting with Microsoft Edge version 93, you can go to edge://settings/appearance and under the Customize Toolbar section select the option to hide the title bar while in Vertical Tab mode.

- **Video Picture in Picture (PiP) from hover toolbar.**  Starting with Microsoft Edge version 93, it will become even easier to enter Picture in Picture (PiP) mode. When you hover over a supported video, a toolbar will appear that allows you to view that video in a PiP window.  Note: this is currently available for Microsoft Edge users on macOS.  Check back shortly as we continue our rollout to Windows users.

- **Removal of 3DES in TLS.**  Starting with Microsoft Edge version 93, support for the TLS_RSA_WITH_3DES_EDE_CBC_SHA cipher suite will be removed. This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, navigate to the [Chrome Platform Status entry](https://chromestatus.com/feature/6678134168485888). Additionally, in Microsoft Edge version 93, the [TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled) policy will be available to support scenarios that need to preserve compatibility with outdated servers. This compatibility policy will become obsolete and stop working in Microsoft Edge version 95. Ensure that you update affected servers before then.

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
Enterprise administrators may opt out of this behavior one of these two policies:
    - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains
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

<!-- begin major 89 -->

<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
