---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 09/08/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Microsoft Edge release notes for Beta Channel"
---

# Release notes for Microsoft Edge Beta Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Beta Channel.

> [!IMPORTANT]
> Please see this [update on Microsoft Edge channel releases](https://blogs.windows.com/msedgedev/2020/03/20/update-stable-channel-releases/).

## Version 86.0.622.xx: September 9

### Feature updates

* **Internet Explorer mode:**

   * Let users use the Microsoft Edge User Interface (UI) to test sites in Internet Explorer mode. Beginning with Microsoft Edge version 86, administrators can enable a UI option for their users to load a tab in Internet Explorer mode for testing purposes or as a stopgap until sites are added to the site list XML.
   * Let users provide feedback on sites that require IE mode. Users can send feedback to you using a Microsoft Edge UI option. You can configure this UI option to be visible through group policy and choose how you want to receive this information (via email or with a custom form).

* **Delete downloads from disk using download manager.** Users are now able to delete their downloaded files from their disk without leaving the browser. The new Delete downloads functionality exists within the context menu of downloads shelf or the downloads page.

* **Roll back to previous Microsoft Edge version.** The rollback feature lets administrators revert to a known good version of Microsoft Edge if there's an issue in the latest version of Microsoft Edge.
[Learn more](edge-learnmore-rollback.md) .

* **Kiosk mode privacy features enabled.** Beginning with Microsoft Edge version 86 we are enabling kiosk mode features that will help enterprises with the privacy of user data. These features will enable experiences such as: clear the user data on exit, delete the downloaded files, and to reset the configured start experience after a specified amount of idle time. Kiosk mode is an ongoing investment.

* **Enforce enabling Sync by default across the enterprise.**  Administrators can enable synchronization for Azure Active Directory (Azure AD) accounts by default with the [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync) policy.

* **PDF updates:**

  * Table of contents for PDF Documents. Beginning with version 86, Microsoft Edge has added support for table of contents that lets users easily navigate through PDF documents.
  * Access all PDF functionalities on small form factor screens. Access all the capabilities of the Microsoft Edge PDF reader on devices with small screen sizes.
  * Pen support for highlighter on PDF files. With this update, users can use their digital pen to directly highlight text on PDF files, in the same way they would with a physical highlighter and paper.
  * Improved PDF scrolling. You will now be able to experience stutter free scrolling while navigating through long PDF documents.

* **Automatic profile switching on Windows 7, 8, and 8.1.** The automatic profile switching currently available in Microsoft Edge on Windows 10 is extended to downlevel Windows (Windows 7, 8,and  8.1). For more information, see the [automatic profile switching](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) blog post.

* **Users will see auto complete suggestions when they start typing a search query on the Microsoft Edge Add-ons website.** Auto complete will help users quickly complete their search query without having to type the entire string. This will be helpful because users won't have to remember correct spellings and they can choose from the available options that are displayed.

* **Remove the HTML5 Application Cache API.**  Beginning with Microsoft Edge version 86, the legacy Application Cache API that enables offline use of web pages is being removed from Microsoft Edge. Web Developers should review the [WebDev documentation](https://web.dev/appcache-removal/) for information on replacing  the Application Cache API with Service Workers.  Important: You can request an [AppCache OriginTrial Token](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) that allows sites to continue to use the deprecated Application Cache API until Microsoft Edge version 90.

* **Security:**

  * Secure DNS (DNS-over-HTTPS) Support.  Beginning with Microsoft Edge version 86, settings to control Secure DNS on un-managed devices is available. These settings aren't accessible to users on managed devices, but IT admins can enable or disable Secure DNS using the [dnsoverhttpsmode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#dnsoverhttpsmode) group policy.
  * Microsoft Edge alerts you if your passwords are found in an online leak. Microsoft Edge checks your passwords against a repository of known-breached credentials and alerts you if a match is found.

* **Add a custom image to the New Tab Page (NTP) using a group policy.** Beginning with Microsoft Edge version 86 the NTP has an option to replace the default image with a custom user-supplied image. The ability to manage the properties of this image is also supported by the group policy.

* **Match customized keyboard shortcuts to VS Code.** Microsoft Edge DevTools now supports customizing keyboard shortcuts in the DevTools to match with your editor/IDE. (In Microsoft Edge 84, we added the ability to match DevTools keyboard shortcuts to VS Code).

* **Replace [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) and [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) policies for downlevel Windows and macOS.** These policies are deprecated in Microsoft Edge version 86 and will become obsolete in Microsoft Edge version 89.<br>
These policies are replaced by [Allow Telemetry](https://go.microsoft.com/fwlink/?linkid=2099569) on Windows 10, and the new [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) policy for all other platforms. This will let users manage the diagnostic data that gets sent to Microsoft for Windows 7, 8, 8.1 and macOS.

### Policy updates

#### New policies

Nineteen new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [CollectionsServicesAndExportsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#collectionsservicesandexportsblocklist) - Block access to a specified list of services and export targets in Collections.
- [DefaultSensorsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsensorssetting) - Default sensors setting.
- [DefaultSerialGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultserialguardsetting) - Control use of the Serial API.
- [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) -  Send required and optional diagnostic data about browser usage.
- [EnterpriseModeSiteListManagerAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed) - Allow access to the Enterprise Mode Site List Manager tool.
- [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync) - Force synchronization of browser data and do not show the sync consent prompt.
- [InsecureFormsWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecureformswarningsenabled) - Enable warnings for insecure forms.
- [InternetExplorerIntegrationTestingAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) - Allow Internet Explorer mode testing.
- [SpotlightExperiencesAndRecommendationsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#spotlightexperiencesandrecommendationsenabled) - Choose whether users can receive customized background images and text, suggestions, notifications, and tips for Microsoft services.
- [NewTabPageAllowedBackgroundTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpageallowedbackgroundtypes) - Configure the background types allowed for the new tab page layout.
- [SaveCookiesOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#savecookiesonexit) - Save cookies when Microsoft Edge closes.
- [SensorsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsallowedforurls) - Allow access to sensors on specific sites.
- [SensorsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsblockedforurls) - Block access to sensors on specific sites.
- [SerialAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialaskforurls) - Allow the Serial API on specific sites.
- [SerialBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialblockedforurls) - Block the Serial API on specific sites.
- [URLBlocklist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlblocklist) - Block access to a list of URLs.
- [URLAllowlist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlallowlist) - Define a list of allowed URLs.
- [UserAgentClientHintsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) - Enable the User-Agent Client Hints feature.
- [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#userdatasnapshotretentionlimit) - Limits the number of user data snapshots retained for use in case of emergency rollback.

#### Deprecated Policies

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - Enable usage and crash-related data reporting.
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - Send site information to improve Microsoft services.

#### Obsoleted Policy

[TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled) - Enable a TLS 1.3 security feature for local trust anchors.

#### Policy caption changed

[NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - Enable Native Window Occlusion.

#### Policy description changed

- [AdsSettingForIntrusiveAdsSites](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#adssettingforintrusiveadssites)
- [AllowTokenBindingForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowtokenbindingforurls)
- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled)
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy)
- [AutoImportAtFirstRun](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoimportatfirstrun)
- [AutoOpenFileTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenfiletypes)
- [BrowserSignin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#browsersignin)
- [ClearBrowsingDataOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clearbrowsingdataonexit) 
- [ClickOnceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clickonceenabled)
- [CommandLineFlagSecurityWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#commandlineflagsecuritywarningsenabled)
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin)
- [ConfigureShare](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureshare)
- [CookiesAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#cookiesallowedforurls)
- [CustomHelpLink](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#customhelplink)
- [DefaultCookiesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultcookiessetting)
- [DefaultGeolocationSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultgeolocationsetting)
- [DefaultImagesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultimagessetting)
- [DefaultInsecureContentSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultinsecurecontentsetting)
- [DefaultJavaScriptSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultjavascriptsetting)
- [DefaultNotificationsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultnotificationssetting)
- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting)
- [DefaultPopupsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpopupssetting)
- [DefaultSearchProviderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsearchproviderenabled)
- [DefaultWebBluetoothGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebbluetoothguardsetting)
- [DefaultWebUsbGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebusbguardsetting)
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload)
- [DeveloperToolsAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#developertoolsavailability)
- [EnableSha1ForLocalAnchors](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors)
- [DownloadRestrictions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#downloadrestrictions)
- [EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures)
- [WinHttpProxyResolverEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#winhttpproxyresolverenabled)
- [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol)
- [ExternalProtocolDialogShowAlwaysOpenCheckbox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox)
- [ExtensionInstallForcelist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)
- [ForceBingSafeSearch](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcebingsafesearch)
- [ForceYouTubeRestrict](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forceyoutuberestrict)
- [HomepageIsNewTabPage](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepageisnewtabpage)
- [HomepageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepagelocation)
- [InPrivateModeAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#inprivatemodeavailability)
- [InternetExplorerIntegrationEnhancedHangDetection](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationenhancedhangdetection)
- [InternetExplorerIntegrationLevel](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect)
- [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled)
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled)
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout)
- [NetworkPredictionOptions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#networkpredictionoptions)
- [NewTabPageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagelocation)
- [NewTabPageSearchBox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesearchbox)
- [NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype)
- [NonRemovableProfileEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nonremovableprofileenabled)
- [PasswordProtectionWarningTrigger](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionwarningtrigger)
- [PasswordProtectionLoginURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionloginurls)
- [PasswordProtectionChangePasswordURL](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionchangepasswordurl)
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls)
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls)
- [PreventSmartScreenPromptOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverride)
- [PreventSmartScreenPromptOverrideForFiles](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverrideforfiles)
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode)
- [RegisteredProtocolHandlers](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#registeredprotocolhandlers)
- [RelaunchNotification](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#relaunchnotification)
- [RestoreOnStartup](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartup)
- [RestoreOnStartupURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartupurls)
- [RestrictSigninToPattern](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restrictsignintopattern)
- [SSLVersionMin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sslversionmin)
- [SmartScreenAllowListDomains](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenallowlistdomains)
- [SmartScreenEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenenabled)
- [SmartScreenForTrustedDownloadsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenfortrusteddownloadsenabled)
- [SmartScreenPuaEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled)
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled)
- [TrackingPrevention](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#trackingprevention)
- [WebRtcLocalhostIpHandling](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtclocalhostiphandling)

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

<!--- BEGIN 85 ---->
## Version 85.0.564.18: July 28

### Feature updates

- **On-premises synchronization of Favorites and Settings**. Now you synchronize browser favorites and settings between Active Directory profiles within your own environment without the need for cloud sync.

- **Microsoft Edge group policy support for trusting site + app combos to launch without a confirmation prompt.** Group policy support added that lets administrators add site + app combos that are trusted to launch without the confirmation prompt. This adds the ability for administrators to configure trusted protocol/origin combinations (such as Microsoft 365 apps) for their end-users to suppress the confirmation prompt when navigating to a URL that contains an app protocol.

- **PDF Highlighter tool**. This tool can be added to the toolbar for PDFs to easily highlight important text.

- **The Storage Access API is available**. The Storage Access API allows access to first-party storage in a third-party context when a user has provided a direct intent to allow storage that would otherwise be blocked by the browser's current configuration. For more information, see [Storage Access API](https://www.chromestatus.com/feature/5612590694662144).

- **Send to OneNote is available for Microsoft Edge Collections**. Everyone's excited to be able to send the information they've gathered in Collections to OneNote, where they can append it to a larger project and collaborate with others! And even more importantly, in Microsoft Edge 85, you'll be able send content to *Office for Mac* products (Word, Excel, and OneNote) for both MSA and Azure Active Directory.

- **DevTools updates**. For details about the following updates, see [What's New In DevTools (Microsoft Edge 85)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools).

   - Microsoft Edge DevTools supports Surface Duo emulation. The Microsoft Edge DevTools can emulate the Surface Duo so you can test how your web content will look on dual-screen devices. To turn on this experiment in DevTools, enter Device Mode by pressing Ctrl+Shift+M on Windows or Command+Shift+M on macOS, and then select Surface Duo from the device drop-down list.
   - Microsoft Edge DevTools lets you match keyboard shortcuts to VS Code. The Microsoft Edge DevTools supports customizing keyboard shortcuts in the DevTools to match your editor/IDE. In Microsoft Edge 85, we are adding the ability to match DevTools keyboard shortcuts to VS Code. This change will help increase productively across VS Code and DevTools.

### Policy updates

#### New policies

Thirteen new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [AutoLaunchProtocolsFromOrigins](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autolaunchprotocolsfromorigins) - Define a list of protocols that can launch an external application from listed origins without prompting the user.
- [AutoOpenAllowedForURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenallowedforurls) - URLs where AutoOpenFileTypes can apply.
- [AutoOpenFileTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenfiletypes) - List of file types that should be automatically opened on download.
- [DefaultSearchProviderContextMenuAccessAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsearchprovidercontextmenuaccessallowed) - Allow default search provider context menu search access.
- [EnableSha1ForLocalAnchors](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) - Allow certificates signed using SHA-1 when issued by local trust anchors.
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains.
- [IntensiveWakeUpThrottlingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#intensivewakeupthrottlingenabled) - Control the IntensiveWakeUpThrottling feature.
- [NewTabPagePrerenderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpageprerenderenabled) - Enable preload of the new tab page for faster rendering.
- [NewTabPageSearchBox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesearchbox) - Configure the new tab page search box experience.
- [PasswordMonitorAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordmonitorallowed) - Allow users to be alerted if their passwords are found to be unsafe.
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled) - Enable using roaming copies for Microsoft Edge profile data.
- [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation) - Set the roaming profile directory.
- [TLSCipherSuiteDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tlsciphersuitedenylist) - Specify the TLS cipher suites to disable.

#### Obsoleted policies

- [EnableDomainActionsDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledomainactionsdownload) - Enable Domain Actions Download from Microsoft.
- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) - Re-enable Web Components v0 API until M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies)- Allow WebDriver to Override Incompatible Policies.

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

- This version of Microsoft Edge provides improved site list download times for Internet Explorer mode.  We've reduced download delay for the Internet Explorer mode site list to 0 seconds (down from a 60-second wait) in the absence of a cached site list. We've also added group policy support for cases when Internet Explorer mode home page navigations need to be delayed until the site list is downloaded. For more information, see the [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload) policy.

- Microsoft Edge now allows users to sign-into the browser when it's "run as administrator" on Windows 10. This will help customers running Microsoft Edge on Windows server or in remote-desktop and sandbox scenarios.

- Microsoft Edge now provides full mouse support when in full screen mode. Now you can use your mouse to access tabs, the address bar, and other items without having to exit full screen mode.

- Online purchase improvement. Add custom nicknames to saved debit or credit cards. Now you can distinguish and differentiate your credit cards when making online purchases. Nicknaming your debit or credit cards lets you choose the correct card when using autofill to select a payment method.

- TLS/1.0 and TLS/1.1 are disabled by default. To help discover impacted sites, you can set the *edge://flags/#display-legacy-tls-warnings* flag to cause Microsoft Edge to display a non-blocking "Not Secure" notice when loading pages that require legacy TLS protocols. The [SSLVersionMin](https://docs.microsoft.com/deployedge/microsoft-edge-policies#sslversionmin) policy permits re-enabling of TLS/1.0 and TLS/1.1. This policy will remain available until at least Microsoft Edge version 88. For more information, see [Site compatibility-impacting changes coming to Microsoft Edge](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes).

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

- [AppCacheForceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#appcacheforceenabled) - Allows the AppCache feature to be re-enabled, even if it's turned off by default.
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy) - Application Guard Container Proxy.
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload) - Require that the Enterprise Mode Site List is available before tab navigation.
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - Enable Hiding of Native Windows.
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout) - Set a timeout for delay of tab navigation for the Enterprise Mode Site List.

#### Deprecated policies

- [AllowSyncXHRInPageDismissal](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsyncxhrinpagedismissal) - Allow pages to send synchronous XHR requests during page dismissal.
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) - Determines whether the built-in certificate verifier will be used to verify server certificates.
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled) - Enable stricter treatment for mixed content.

#### Obsoleted policy

[ForceNetworkInProcess](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcenetworkinprocess) - Force networking code to run in the browser process.

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

- Extension sync is now available. You can now sync your extensions across all your devices! Extensions from both the Microsoft and Chrome Stores will sync with Microsoft Edge. To use this feature: Click the ellipses (**…**) on the menu bar, select **Settings**. Under Your profile, click **Sync** to see the Sync options. Under **Profiles/Sync** use the toggle to enable Extensions. You can use the [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) group policy to disable syncing of extensions.

- Improved the message on the Downloads management page for insecure downloads that have been blocked.

- Immersive Reader improvements:
  - Added support for Adverbs in the Parts of Speech experience we have in Immersive Reader. While reading an article within the Immersive Reader, open the Grammar Tools and switch on Adverbs within Parts of Speech to highlight all the adverbs on the page.
  - Added the ability to select any content on a webpage and open it in Immersive Reader. This ability enables users to use the Immersive Reader and all the Learning Tools, such as Line Focus and Read Aloud, across all websites.

- Link doctor provides host correction and a search query to the users when they mistype a URL. For example: <br>
A user mistypes "powerbi as "powerbbi".com. Link doctor will suggest "powerbi".com as a correction and create a link to search for "powerbbi" in case the user is looking for something different.

- Allow users to save their decision to launch an external protocol for a specific site. Users can configure the [ExternalProtocolDialogShowAlwaysOpenCheckbox]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox) policy to enable or disable this feature.

- Users can set Microsoft Edge as their default browser directly from Microsoft Edge **Settings**. This capability makes it easier for users to change their default browser, within the context of the browser itself, instead of having to search through the operating system settings. To use this feature, go to *edge://settings/defaultBrowser* and click **Make default**.

- Several DevTools updates, including new remote debugging support, UI improvements, and more. For more information, see [What's New In DevTools (Microsoft Edge 83)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools).

### Policy updates

#### New policies

15 new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [AllowSurfGame](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsurfgame) - Allow surf game.
- [AllowTokenBindingForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowtokenbindingforurls) - Configure the list of sites for which Microsoft Edge will attempt to establish a Token Binding with.
- [BingAdsSuppression](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#bingadssuppression) - Block all ads on Bing search results.
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) - Determines whether the built-in certificate verifier will be used to verify server certificates.
- [ClearCachedImagesAndFilesOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clearcachedimagesandfilesonexit) - Clear cached images and files when Microsoft Edge closes.
- [ConfigureShare](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureshare) - Configure the Share experience.
- [DeleteDataOnMigration](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#deletedataonmigration) - Delete old browser data on migration.
- [DnsOverHttpsMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsoverhttpsmode) - Control the mode of DNS-over-HTTPS.
- [DnsOverHttpsTemplates](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsoverhttpstemplates) - Specify URI template of desired DNS-over-HTTPS resolver.
- [FamilySafetySettingsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#familysafetysettingsenabled) - Allow users to configure Family safety.
- [LocalProvidersEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#localprovidersenabled) - Allow suggestions from local providers.
- [ScrollToTextFragmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#scrolltotextfragmentenabled) - Enable scrolling to text specified in URL fragments.
- [ScreenCaptureAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#screencaptureallowed) - Allow or deny screen capture.
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) - Configure the list of types that are excluded from synchronization.
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - Enable Hiding of Native Windows.

#### Deprecated policy

The following policy will continue to work in this release. It will become "obsolete" in a future release.

[EnableDomainActionsDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledomainactionsdownload) Enable Domain Actions Download from Microsoft

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

- On-prem Active Directory account auto sign in will only be targeted to organizations that turn it on.  If users were already signed in with an on-prem AD account, they will now be able to sign out of it. Now, users will only be automatically signed in with the primary account on their operating system if it is an MSA or an Azure AD account. Admins can enable auto sign in with an on-prem AD account using the ConfigureOnPremisesAccountAutoSignIn policy.

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

- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled) - Enable Ambient Authentication for InPrivate and Guest profiles. 
- [AudioSandboxEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#audiosandboxenabled) - Allow the audio sandbox to run.
- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy) - Use a default referrer policy of no-referrer-when-downgrade.
- [GloballyScopeHTTPAuthCacheEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#globallyscopehttpauthcacheenabled) - Enable globally scoped HTTP auth cache.
- [ImportExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importextensions) - Allow importing of extensions.
- [ImportCookies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importcookies) - Allow importing of Cookies.
- [ImportShortcuts](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importshortcuts) - Allow importing of shortcuts.
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect) - Specify how "in-page" navigations to unconfigured sites behave when started from Internet Explorer mode pages.
- [OmniboxMSBProviderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#omniboxmsbproviderenabled) - Enable Microsoft Search for Business provider in omnibox. 
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled) - Enable stricter treatment for mixed content.
- [TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled) - Enable a TLS 1.3 security feature for local trust anchors.
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin) - Configure automatic sign in with an Active Directory domain account when there is no Azure AD domain account.

#### Deprecated policies

The following policies continue to work in this release. They will become "obsolete" in a future release.

- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) - Re-enable Web Components v0 API until M84.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) - Allow WebDriver to Override Incompatible.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
