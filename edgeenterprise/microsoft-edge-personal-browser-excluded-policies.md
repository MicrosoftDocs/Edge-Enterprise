---
title: "Policies that aren't applied to an Enterprise personal browser profile"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 07/25/2023
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Policies excluded from the Enterprise personal browser profile"
---

# Policies that aren't applied to an Enterprise personal browser profile

The following policies aren't applied to the personal browser profile.

## Policy table

| Policy Name | Caption |
|:-|:-|
|[AccessibilityImageLabelsEnabled](#accessibilityimagelabelsenabled)|Let screen reader users get image descriptions from Microsoft|
|[AddressBarEditingEnabled](#addressbareditingenabled)|Configure address bar editing|
|[AddressBarMicrosoftSearchInBingProviderEnabled](#addressbarmicrosoftsearchinbingproviderenabled)|Enable Microsoft Search in Bing suggestions in the address bar|
|[AdsSettingForIntrusiveAdsSites](#adssettingforintrusiveadssites)|Ads setting for sites with intrusive ads|
|[AdsTransparencyEnabled](#adstransparencyenabled)|Configure if the ads transparency feature is enabled|
|[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory)|Enable deleting browser and download history|
|[AllowGamesMenu](#allowgamesmenu)|Allow users to access the games menu (deprecated)|
|[AllowSurfGame](#allowsurfgame)|Allow surf game|
|[AllowTrackingForUrls](#allowtrackingforurls)|Configure tracking prevention exceptions for specific sites|
|[AllowedDomainsForApps](#alloweddomainsforapps)|Define domains allowed to access Google Workspace|
|[AlternateErrorPagesEnabled](#alternateerrorpagesenabled)|Suggest similar pages when a webpage can't be found|
|[AlwaysOpenPdfExternally](#alwaysopenpdfexternally)|Always open PDF files externally|
|[AskBeforeCloseEnabled](#askbeforecloseenabled)|Get user confirmation before closing a browser window with multiple tabs|
|[AudioCaptureAllowedUrls](#audiocaptureallowedurls)|Sites that can access audio capture devices without requesting permission|
|[AutoLaunchProtocolsComponentEnabled](#autolaunchprotocolscomponentenabled)|AutoLaunch Protocols Component Enabled|
|[AutoLaunchProtocolsFromOrigins](#autolaunchprotocolsfromorigins)|Define a list of protocols that can launch an external application from listed origins without prompting the user|
|[AutoOpenAllowedForURLs](#autoopenallowedforurls)|URLs where AutoOpenFileTypes can apply|
|[AutoOpenFileTypes](#autoopenfiletypes)|List of file types that should be automatically opened on download|
|[AutoSelectCertificateForUrls](#autoselectcertificateforurls)|Automatically select client certificates for these sites|
|[AutofillAddressEnabled](#autofilladdressenabled)|Enable AutoFill for addresses|
|[AutofillCreditCardEnabled](#autofillcreditcardenabled)|Enable AutoFill for payment instruments|
|[AutofillMembershipsEnabled](#autofillmembershipsenabled)|Save and fill memberships|
|[AutomaticDownloadsAllowedForUrls](#automaticdownloadsallowedforurls)|Allow multiple automatic downloads in quick succession on specific sites|
|[AutomaticDownloadsBlockedForUrls](#automaticdownloadsblockedforurls)|Block multiple automatic downloads in quick succession on specific sites|
|[AutomaticHttpsDefault](#automatichttpsdefault)|Configure Automatic HTTPS|
|[AutoplayAllowed](#autoplayallowed)|Allow media autoplay for websites|
|[AutoplayAllowlist](#autoplayallowlist)|Allow media autoplay on specific sites|
|[BackgroundTemplateListUpdatesEnabled](#backgroundtemplatelistupdatesenabled)|Enables background updates to the list of available templates for Collections and other features that use templates (deprecated)|
|[BlockExternalExtensions](#blockexternalextensions)|Blocks external extensions from being installed|
|[BrowserNetworkTimeQueriesEnabled](#browsernetworktimequeriesenabled)|Allow queries to a Browser Network Time service|
|[CORSNonWildcardRequestHeadersSupport](#corsnonwildcardrequestheaderssupport)|CORS non-wildcard request header support enabled|
|[ClipboardAllowedForUrls](#clipboardallowedforurls)|Allow clipboard use on specific sites|
|[ClipboardBlockedForUrls](#clipboardblockedforurls)|Block clipboard use on specific sites|
|[CollectionsServicesAndExportsBlockList](#collectionsservicesandexportsblocklist)|Block access to a specified list of services and export targets in Collections|
|[ComposeInlineEnabled](#composeinlineenabled)|Compose is enabled for writing on the web|
|[ConfigureDoNotTrack](#configuredonottrack)|Configure Do Not Track|
|[ConfigureFriendlyURLFormat](#configurefriendlyurlformat)|Configure the default paste format of URLs copied from Microsoft Edge, and determine if additional formats will be available to users|
|[ConfigureKeyboardShortcuts](#configurekeyboardshortcuts)|Configure the list of commands for which to disable keyboard shortcuts|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|Configure Online Text To Speech|
|[ConfigureShare](#configureshare)|Configure the Share experience|
|[ControlDefaultStateOfAllowExtensionFromOtherStoresSettingEnabled](#controldefaultstateofallowextensionfromotherstoressettingenabled)|Configure default state of Allow extensions from other stores setting|
|[CryptoWalletEnabled](#cryptowalletenabled)|Enable CryptoWallet feature|
|[CustomHelpLink](#customhelplink)|Specify custom help link|
|[DefaultAutomaticDownloadsSetting](#defaultautomaticdownloadssetting)|Default automatic downloads setting|
|[DefaultClipboardSetting](#defaultclipboardsetting)|Default clipboard site permission|
|[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)|Control use of the File System API for reading|
|[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)|Control use of the File System API for writing|
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|Default geolocation setting|
|[DefaultImagesSetting](#defaultimagessetting)|Default images setting|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|Control use of insecure content exceptions|
|[DefaultJavaScriptJitSetting](#defaultjavascriptjitsetting)|Control use of JavaScript JIT|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|Default JavaScript setting|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|Default notification setting|
|[DefaultPopupsSetting](#defaultpopupssetting)|Default pop-up window setting|
|[DefaultPrinterSelection](#defaultprinterselection)|Default printer selection rules|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|Allow default search provider context menu search access|
|[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)|Enable the default search provider|
|[DefaultSearchProviderEncodings](#defaultsearchproviderencodings)|Default search provider encodings|
|[DefaultSearchProviderImageURL](#defaultsearchproviderimageurl)|Specifies the search-by-image feature for the default search provider|
|[DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams)|Parameters for an image URL that uses POST|
|[DefaultSearchProviderKeyword](#defaultsearchproviderkeyword)|Default search provider keyword|
|[DefaultSearchProviderName](#defaultsearchprovidername)|Default search provider name|
|[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)|Default search provider search URL|
|[DefaultSearchProviderSuggestURL](#defaultsearchprovidersuggesturl)|Default search provider URL for suggestions|
|[DefaultSensorsSetting](#defaultsensorssetting)|Default sensors setting|
|[DefaultSerialGuardSetting](#defaultserialguardsetting)|Control use of the Serial API|
|[DefaultShareAdditionalOSRegionSetting](#defaultshareadditionalosregionsetting)|Set the default "share additional operating system region" setting|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|Control use of the Web Bluetooth API|
|[DefaultWebHidGuardSetting](#defaultwebhidguardsetting)|Control use of the WebHID API|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|Control use of the WebUSB API|
|[DefinePreferredLanguages](#definepreferredlanguages)|Define an ordered list of preferred languages that websites should display in if the site supports the language|
|[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)|Require that the Enterprise Mode Site List is available before tab navigation|
|[DeveloperToolsAvailability](#developertoolsavailability)|Control where developer tools can be used|
|[Disable3DAPIs](#disable3dapis)|Disable support for 3D graphics APIs|
|[DiscoverPageContextEnabled](#discoverpagecontextenabled)|Enable Discover access to page contents for AAD profiles|
|[DoNotSilentlyBlockProtocolsFromOrigins](#donotsilentlyblockprotocolsfromorigins)|Define a list of protocols that can not be silently blocked by anti-flood protection|
|[DoubleClickCloseTabEnabled](#doubleclickclosetabenabled)|Double Click feature in Microsoft Edge enabled (only available in China)|
|[DownloadDirectory](#downloaddirectory)|Set download directory|
|[DownloadRestrictions](#downloadrestrictions)|Allow download restrictions|
|[EdgeAssetDeliveryServiceEnabled](#edgeassetdeliveryserviceenabled)|Allow features to download assets from the Asset Delivery Service|
|[EdgeCollectionsEnabled](#edgecollectionsenabled)|Enable the Collections feature|
|[EdgeEDropEnabled](#edgeedropenabled)|Enable Drop feature in Microsoft Edge|
|[EdgeEnhanceImagesEnabled](#edgeenhanceimagesenabled)|Enhance images enabled|
|[EdgeFollowEnabled](#edgefollowenabled)|Enable Follow service in Microsoft Edge|
|[EdgeShoppingAssistantEnabled](#edgeshoppingassistantenabled)|Shopping in Microsoft Edge Enabled|
|[EdgeWalletCheckoutEnabled](#edgewalletcheckoutenabled)|Enable Wallet Checkout feature|
|[EdgeWorkspacesEnabled](#edgeworkspacesenabled)|Enable Workspaces|
|[EditFavoritesEnabled](#editfavoritesenabled)|Allows users to edit favorites|
|[EnableMediaRouter](#enablemediarouter)|Enable Google Cast|
|[EnterpriseHardwarePlatformAPIEnabled](#enterprisehardwareplatformapienabled)|Allow managed extensions to use the Enterprise Hardware Platform API|
|[EnterpriseModeSiteListManagerAllowed](#enterprisemodesitelistmanagerallowed)|Allow access to the Enterprise Mode Site List Manager tool|
|[EventPathEnabled](#eventpathenabled)|Re-enable the Event.path API until Microsoft Edge version 115 (obsolete)|
|[ExtensionAllowedTypes](#extensionallowedtypes)|Configure allowed extension types|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|Allow specific extensions to be installed|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|Control which extensions cannot be installed|
|[ExtensionSettings](#extensionsettings)|Configure extension management settings|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox)|Show an "Always open" checkbox in external protocol dialog|
|[FavoritesBarEnabled](#favoritesbarenabled)|Enable favorites bar|
|[FetchKeepaliveDurationSecondsOnShutdown](#fetchkeepalivedurationsecondsonshutdown)|Fetch keepalive duration on shutdown|
|[FileSystemReadAskForUrls](#filesystemreadaskforurls)|Allow read access via the File System API on these sites|
|[FileSystemReadBlockedForUrls](#filesystemreadblockedforurls)|Block read access via the File System API on these sites|
|[FileSystemWriteAskForUrls](#filesystemwriteaskforurls)|Allow write access to files and directories on these sites|
|[FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls)|Block write access to files and directories on these sites|
|[ForceBingSafeSearch](#forcebingsafesearch)|Enforce Bing SafeSearch|
|[ForceEphemeralProfiles](#forceephemeralprofiles)|Enable use of ephemeral profiles|
|[ForceGoogleSafeSearch](#forcegooglesafesearch)|Enforce Google SafeSearch|
|[ForceMajorVersionToMinorPositionInUserAgent](#forcemajorversiontominorpositioninuseragent)|Enable or disable freezing the User-Agent string at major version 99|
|[ForceSync](#forcesync)|Force synchronization of browser data and do not show the sync consent prompt|
|[ForceSyncTypes](#forcesynctypes)|Configure the list of types that are included for synchronization|
|[ForceYouTubeRestrict](#forceyoutuberestrict)|Force minimum YouTube Restricted Mode|
|[FullscreenAllowed](#fullscreenallowed)|Allow full screen mode|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|Enable globally scoped HTTP auth cache|
|[HomepageIsNewTabPage](#homepageisnewtabpage)|Set the new tab page as the home page|
|[HomepageLocation](#homepagelocation)|Configure the home page URL|
|[HubsSidebarEnabled](#hubssidebarenabled)|Show Hubs Sidebar|
|[ImagesAllowedForUrls](#imagesallowedforurls)|Allow images on these sites|
|[ImagesBlockedForUrls](#imagesblockedforurls)|Block images on specific sites|
|[ImmersiveReaderGrammarToolsEnabled](#immersivereadergrammartoolsenabled)|Enable Grammar Tools feature within Immersive Reader in Microsoft Edge|
|[ImmersiveReaderPictureDictionaryEnabled](#immersivereaderpicturedictionaryenabled)|Enable Picture Dictionary feature within Immersive Reader in Microsoft Edge|
|[ImportAutofillFormData](#importautofillformdata)|Allow importing of autofill form data|
|[ImportBrowserSettings](#importbrowsersettings)|Allow importing of browser settings|
|[ImportCookies](#importcookies)|Allow importing of Cookies|
|[ImportExtensions](#importextensions)|Allow importing of extensions|
|[ImportFavorites](#importfavorites)|Allow importing of favorites|
|[ImportHistory](#importhistory)|Allow importing of browsing history|
|[ImportHomepage](#importhomepage)|Allow importing of home page settings|
|[ImportOnEachLaunch](#importoneachlaunch)|Allow import of data from other browsers on each Microsoft Edge launch|
|[ImportOpenTabs](#importopentabs)|Allow importing of open tabs|
|[ImportPaymentInfo](#importpaymentinfo)|Allow importing of payment info|
|[ImportSavedPasswords](#importsavedpasswords)|Allow importing of saved passwords|
|[ImportSearchEngine](#importsearchengine)|Allow importing of search engine settings|
|[ImportShortcuts](#importshortcuts)|Allow importing of shortcuts|
|[ImportStartupPageSettings](#importstartuppagesettings)|Allow importing of startup page settings|
|[InsecureContentAllowedForUrls](#insecurecontentallowedforurls)|Allow insecure content on specified sites|
|[InsecureContentBlockedForUrls](#insecurecontentblockedforurls)|Block insecure content on specified sites|
|[InsecureFormsWarningsEnabled](#insecureformswarningsenabled)|Enable warnings for insecure forms|
|[InternetExplorerIntegrationAlwaysUseOSCapture](#internetexplorerintegrationalwaysuseoscapture)|Always use the OS capture engine to avoid issues with capturing Internet Explorer mode tabs|
|[InternetExplorerIntegrationAlwaysWaitForUnload](#internetexplorerintegrationalwayswaitforunload)|Wait for Internet Explorer mode tabs to completely unload before ending the browser session|
|[InternetExplorerIntegrationCloudNeutralSitesReporting](#internetexplorerintegrationcloudneutralsitesreporting)|Configure reporting of potentially misconfigured neutral site URLs to the M365 Admin Center Site Lists app|
|[InternetExplorerIntegrationCloudSiteList](#internetexplorerintegrationcloudsitelist)|Configure the Enterprise Mode Cloud Site List|
|[InternetExplorerIntegrationCloudUserSitesReporting](#internetexplorerintegrationcloudusersitesreporting)|Configure reporting of IE Mode user list entries to the M365 Admin Center Site Lists app|
|[InternetExplorerIntegrationComplexNavDataTypes](#internetexplorerintegrationcomplexnavdatatypes)|Configure whether form data and HTTP headers will be sent when entering or exiting Internet Explorer mode|
|[InternetExplorerIntegrationEnhancedHangDetection](#internetexplorerintegrationenhancedhangdetection)|Configure enhanced hang detection for Internet Explorer mode|
|[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)|Configure Internet Explorer integration|
|[InternetExplorerIntegrationLocalFileAllowed](#internetexplorerintegrationlocalfileallowed)|Allow launching of local files in Internet Explorer mode|
|[InternetExplorerIntegrationLocalFileExtensionAllowList](#internetexplorerintegrationlocalfileextensionallowlist)|Open local files in Internet Explorer mode file extension allow list|
|[InternetExplorerIntegrationLocalFileShowContextMenu](#internetexplorerintegrationlocalfileshowcontextmenu)|Show context menu to open a file:// link in Internet Explorer mode|
|[InternetExplorerIntegrationLocalMhtFileAllowed](#internetexplorerintegrationlocalmhtfileallowed)|Allow local MHTML files to open automatically in Internet Explorer mode|
|[InternetExplorerIntegrationReloadInIEModeAllowed](#internetexplorerintegrationreloadiniemodeallowed)|Allow unconfigured sites to be reloaded in Internet Explorer mode|
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|Configure the Enterprise Mode Site List|
|[InternetExplorerIntegrationSiteListRefreshInterval](#internetexplorerintegrationsitelistrefreshinterval)|Configure how frequently the Enterprise Mode Site List is refreshed|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|Specify how "in-page" navigations to unconfigured sites behave when started from Internet Explorer mode pages|
|[InternetExplorerIntegrationWindowOpenHeightAdjustment](#internetexplorerintegrationwindowopenheightadjustment)|Configure the pixel adjustment between window.open heights sourced from IE mode pages vs. Edge mode pages|
|[InternetExplorerIntegrationWindowOpenWidthAdjustment](#internetexplorerintegrationwindowopenwidthadjustment)|Configure the pixel adjustment between window.open widths sourced from IE mode pages vs. Edge mode pages|
|[InternetExplorerModeClearDataOnExitEnabled](#internetexplorermodecleardataonexitenabled)|Clear history for IE and IE mode every time you exit|
|[InternetExplorerModeEnableSavePageAs](#internetexplorermodeenablesavepageas)|Allow Save page as in Internet Explorer mode|
|[InternetExplorerModeTabInEdgeModeAllowed](#internetexplorermodetabinedgemodeallowed)|Allow sites configured for Internet Explorer mode to open in Microsoft Edge|
|[InternetExplorerModeToolbarButtonEnabled](#internetexplorermodetoolbarbuttonenabled)|Show the Reload in Internet Explorer mode button in the toolbar|
|[InternetExplorerZoomDisplay](#internetexplorerzoomdisplay)|Display zoom in IE Mode tabs with DPI Scale included like it is in Internet Explorer|
|[IntranetFileLinksEnabled](#intranetfilelinksenabled)|Allow intranet zone file URL links from Microsoft Edge to open in Windows File Explorer|
|[JavaScriptAllowedForUrls](#javascriptallowedforurls)|Allow JavaScript on specific sites|
|[JavaScriptBlockedForUrls](#javascriptblockedforurls)|Block JavaScript on specific sites|
|[JavaScriptJitAllowedForSites](#javascriptjitallowedforsites)|Allow JavaScript to use JIT on these sites|
|[JavaScriptJitBlockedForSites](#javascriptjitblockedforsites)|Block JavaScript from using JIT on these sites|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist)|Revert to legacy SameSite behavior for cookies on specified sites|
|[LinkedAccountEnabled](#linkedaccountenabled)|Enable the linked account feature|
|[LiveCaptionsAllowed](#livecaptionsallowed)|Live captions allowed|
|[LocalBrowserDataShareEnabled](#localbrowserdatashareenabled)|Enable Windows to search local Microsoft Edge browsing data|
|[LocalProvidersEnabled](#localprovidersenabled)|Allow suggestions from local providers|
|[ManagedConfigurationPerOrigin](#managedconfigurationperorigin)|Sets managed configuration values for websites to specific origins|
|[ManagedFavorites](#managedfavorites)|Configure favorites|
|[ManagedSearchEngines](#managedsearchengines)|Manage Search Engines|
|[MicrosoftEdgeInsiderPromotionEnabled](#microsoftedgeinsiderpromotionenabled)|Microsoft Edge Insider Promotion Enabled|
|[MicrosoftEditorProofingEnabled](#microsofteditorproofingenabled)|Spell checking provided by Microsoft Editor|
|[MicrosoftEditorSynonymsEnabled](#microsofteditorsynonymsenabled)|Synonyms are provided when using Microsoft Editor spell checker|
|[MicrosoftOfficeMenuEnabled](#microsoftofficemenuenabled)|Allow users to access the Microsoft Office menu (deprecated)|
|[MouseGestureEnabled](#mousegestureenabled)|Mouse Gesture Enabled|
|[NativeMessagingAllowlist](#nativemessagingallowlist)|Control which native messaging hosts users can use|
|[NativeMessagingBlocklist](#nativemessagingblocklist)|Configure native messaging block list|
|[NativeMessagingUserLevelHosts](#nativemessaginguserlevelhosts)|Allow user-level native messaging hosts (installed without admin permissions)|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|Set a timeout for delay of tab navigation for the Enterprise Mode Site List|
|[NetworkPredictionOptions](#networkpredictionoptions)|Enable network prediction|
|[NewPDFReaderEnabled](#newpdfreaderenabled)|Microsoft Edge built-in PDF reader powered by Adobe Acrobat enabled|
|[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)|Configure the background types allowed for the new tab page layout|
|[NewTabPageAppLauncherEnabled](#newtabpageapplauncherenabled)|Hide App Launcher on Microsoft Edge new tab page|
|[NewTabPageContentEnabled](#newtabpagecontentenabled)|Allow Microsoft News content on the new tab page|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|Hide the default top sites from the new tab page|
|[NewTabPageLocation](#newtabpagelocation)|Configure the new tab page URL|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|Set new tab page quick links|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|Enable preload of the new tab page for faster rendering|
|[NewTabPageQuickLinksEnabled](#newtabpagequicklinksenabled)|Allow quick links on the new tab page|
|[NewTabPageSearchBox](#newtabpagesearchbox)|Configure the new tab page search box experience|
|[NotificationsAllowedForUrls](#notificationsallowedforurls)|Allow notifications on specific sites|
|[NotificationsBlockedForUrls](#notificationsblockedforurls)|Block notifications on specific sites|
|[OriginAgentClusterDefaultEnabled](#originagentclusterdefaultenabled)|Origin-keyed agent clustering enabled by default|
|[PDFSecureMode](#pdfsecuremode)|Secure mode and Certificate-based Digital Signature validation in native PDF reader|
|[PDFXFAEnabled](#pdfxfaenabled)|XFA support in native PDF reader enabled|
|[PasswordGeneratorEnabled](#passwordgeneratorenabled)|Allow users to get a strong password suggestion whenever they are creating an account online|
|[PasswordManagerBlocklist](#passwordmanagerblocklist)|Configure the list of domains for which the password manager UI (Save and Fill) will be disabled|
|[PasswordManagerEnabled](#passwordmanagerenabled)|Enable saving passwords to the password manager|
|[PasswordManagerRestrictLengthEnabled](#passwordmanagerrestrictlengthenabled)|Restrict the length of passwords that can be saved in the Password Manager|
|[PasswordMonitorAllowed](#passwordmonitorallowed)|Allow users to be alerted if their passwords are found to be unsafe|
|[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)|Configure the change password URL|
|[PasswordProtectionLoginURLs](#passwordprotectionloginurls)|Configure the list of enterprise login URLs where the password protection service should capture salted hashes of a password|
|[PasswordProtectionWarningTrigger](#passwordprotectionwarningtrigger)|Configure password protection warning trigger|
|[PasswordRevealEnabled](#passwordrevealenabled)|Enable Password reveal button|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|Allow websites to query for available payment methods|
|[PerformanceDetectorEnabled](#performancedetectorenabled)|Performance Detector Enabled|
|[PinBrowserEssentialsToolbarButton](#pinbrowseressentialstoolbarbutton)|Pin browser essentials toolbar button|
|[PopupsAllowedForUrls](#popupsallowedforurls)|Allow pop-up windows on specific sites|
|[PopupsBlockedForUrls](#popupsblockedforurls)|Block pop-up windows on specific sites|
|[PrimaryPasswordSetting](#primarypasswordsetting)|Configures a setting that asks users to enter their device password while using password autofill|
|[PrintPdfAsImageDefault](#printpdfasimagedefault)|Print PDF as Image Default|
|[PrintPostScriptMode](#printpostscriptmode)|Print PostScript Mode|
|[PrintPreviewStickySettings](#printpreviewstickysettings)|Configure the sticky print preview settings|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|Set the system default printer as the default printer|
|[PrintRasterizationMode](#printrasterizationmode)|Print Rasterization Mode|
|[PrintRasterizePdfDpi](#printrasterizepdfdpi)|Print Rasterize PDF DPI|
|[PrintStickySettings](#printstickysettings)|Print preview sticky settings|
|[PrinterTypeDenyList](#printertypedenylist)|Disable printer types on the deny list|
|[PrintingAllowedBackgroundGraphicsModes](#printingallowedbackgroundgraphicsmodes)|Restrict background graphics printing mode|
|[PrintingBackgroundGraphicsDefault](#printingbackgroundgraphicsdefault)|Default background graphics printing mode|
|[PrintingEnabled](#printingenabled)|Enable printing|
|[PrintingPaperSizeDefault](#printingpapersizedefault)|Default printing page size|
|[PrintingWebpageLayout](#printingwebpagelayout)|Sets layout for printing|
|[PromptForDownloadLocation](#promptfordownloadlocation)|Ask where to save downloaded files|
|[PromptOnMultipleMatchingCertificates](#promptonmultiplematchingcertificates)|Prompt the user to select a certificate when multiple certificates match|
|[ProxyBypassList](#proxybypasslist)|Configure proxy bypass rules (deprecated)|
|[ProxyMode](#proxymode)|Configure proxy server settings (deprecated)|
|[ProxyPacUrl](#proxypacurl)|Set the proxy .pac file URL (deprecated)|
|[ProxyServer](#proxyserver)|Configure address or URL of proxy server (deprecated)|
|[QuickSearchShowMiniMenu](#quicksearchshowminimenu)|Enables Microsoft Edge mini menu|
|[QuickViewOfficeFilesEnabled](#quickviewofficefilesenabled)|Manage QuickView Office files capability in Microsoft Edge|
|[ReadAloudEnabled](#readaloudenabled)|Enable Read Aloud feature in Microsoft Edge|
|[RegisteredProtocolHandlers](#registeredprotocolhandlers)|Register protocol handlers|
|[RelatedMatchesCloudServiceEnabled](#relatedmatchescloudserviceenabled)|Configure Related Matches in Find on Page|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|Enable resolution of navigation errors using a web service|
|[RestoreOnStartup](#restoreonstartup)|Action to take on startup|
|[RestoreOnStartupURLs](#restoreonstartupurls)|Sites to open when the browser starts|
|[RestoreOnStartupUserURLsEnabled](#restoreonstartupuserurlsenabled)|Allow users to add and remove their own sites during startup when the RestoreOnStartupURLs policy is configured|
|[RestorePdfView](#restorepdfview)|Restore PDF view|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|Allow users to proceed from the HTTPS warning page|
|[SSLErrorOverrideAllowedForOrigins](#sslerroroverrideallowedfororigins)|Allow users to proceed from the HTTPS warning page for specific origins|
|[SameOriginTabCaptureAllowedByOrigins](#sameorigintabcaptureallowedbyorigins)|Allow Same Origin Tab capture by these origins|
|[ScreenCaptureAllowed](#screencaptureallowed)|Allow or deny screen capture|
|[ScreenCaptureAllowedByOrigins](#screencaptureallowedbyorigins)|Allow Desktop, Window, and Tab capture by these origins|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|Enable scrolling to text specified in URL fragments|
|[SearchFiltersEnabled](#searchfiltersenabled)|Search Filters Enabled|
|[SearchForImageEnabled](#searchforimageenabled)|Search for image enabled|
|[SearchInSidebarEnabled](#searchinsidebarenabled)|Search in Sidebar enabled|
|[SearchSuggestEnabled](#searchsuggestenabled)|Enable search suggestions|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|Websites or domains that don't need permission to use direct Security Key attestation|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|Send all intranet sites to Internet Explorer|
|[SensorsAllowedForUrls](#sensorsallowedforurls)|Allow access to sensors on specific sites|
|[SensorsBlockedForUrls](#sensorsblockedforurls)|Block access to sensors on specific sites|
|[SerialAskForUrls](#serialaskforurls)|Allow the Serial API on specific sites|
|[SerialBlockedForUrls](#serialblockedforurls)|Block the Serial API on specific sites|
|[ShowAcrobatSubscriptionButton](#showacrobatsubscriptionbutton)|Shows button on native PDF viewer in Microsoft Edge that allows users to sign up for Adobe Acrobat subscription|
|[ShowCastIconInToolbar](#showcasticonintoolbar)|Show the cast icon in the toolbar|
|[ShowDownloadsToolbarButton](#showdownloadstoolbarbutton)|Show Downloads button on the toolbar|
|[ShowHomeButton](#showhomebutton)|Show Home button on toolbar|
|[ShowMicrosoftRewards](#showmicrosoftrewards)|Show Microsoft Rewards experiences|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|Show Microsoft Office shortcut in favorites bar (deprecated)|
|[ShowPDFDefaultRecommendationsEnabled](#showpdfdefaultrecommendationsenabled)|Allow notifications to set Microsoft Edge as default PDF reader|
|[ShowRecommendationsEnabled](#showrecommendationsenabled)|Allow feature recommendations and browser assistance notifications from Microsoft Edge|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|Enable Signed HTTP Exchange (SXG) support|
|[SleepingTabsBlockedForUrls](#sleepingtabsblockedforurls)|Block sleeping tabs on specific sites|
|[SleepingTabsEnabled](#sleepingtabsenabled)|Configure sleeping tabs|
|[SleepingTabsTimeout](#sleepingtabstimeout)|Set the background tab inactivity timeout for sleeping tabs|
|[SmartActionsBlockList](#smartactionsblocklist)|Block smart actions for a list of services|
|[SpeechRecognitionEnabled](#speechrecognitionenabled)|Configure Speech Recognition|
|[SpellcheckEnabled](#spellcheckenabled)|Enable spellcheck|
|[SpellcheckLanguage](#spellchecklanguage)|Enable specific spellcheck languages|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|Force disable spellcheck languages|
|[SyncDisabled](#syncdisabled)|Disable synchronization of data using Microsoft sync services|
|[TabCaptureAllowedByOrigins](#tabcaptureallowedbyorigins)|Allow Tab capture by these origins|
|[TabServicesEnabled](#tabservicesenabled)|Tab Services enabled|
|[TextPredictionEnabled](#textpredictionenabled)|Text prediction enabled by default|
|[TrackingPrevention](#trackingprevention)|Block tracking of users' web-browsing activity|
|[TranslateEnabled](#translateenabled)|Enable Translate|
|[URLAllowlist](#urlallowlist)|Define a list of allowed URLs|
|[URLBlocklist](#urlblocklist)|Block access to a list of URLs|
|[UnthrottledNestedTimeoutEnabled](#unthrottlednestedtimeoutenabled)|JavaScript setTimeout will not be clamped until a higher nesting threshold is set (deprecated)|
|[UserAgentReduction](#useragentreduction)|Enable or disable the User-Agent Reduction|
|[VerticalTabsAllowed](#verticaltabsallowed)|Configures availability of a vertical layout for tabs on the side of the browser|
|[VideoCaptureAllowed](#videocaptureallowed)|Allow or block video capture|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|Sites that can access video capture devices without requesting permission|
|[VisualSearchEnabled](#visualsearchenabled)|Visual search enabled|
|[WalletDonationEnabled](#walletdonationenabled)|Wallet Donation Enabled|
|[WebAppInstallForceList](#webappinstallforcelist)|Configure list of force-installed Web Apps|
|[WebHidAskForUrls](#webhidaskforurls)|Allow the WebHID API on these sites|
|[WebHidBlockedForUrls](#webhidblockedforurls)|Block the WebHID API on these sites|
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|Manage exposure of local IP addressess by WebRTC|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|Restrict exposure of local IP address by WebRTC|
|[WebRtcUdpPortRange](#webrtcudpportrange)|Restrict the range of local UDP ports used by WebRTC|
|[WebSQLAccess](#websqlaccess)|Force WebSQL to be enabled|
|[WebSelectEnabled](#webselectenabled)|Web Select Enabled (deprecated)|
|[WebUsbAllowDevicesForUrls](#webusballowdevicesforurls)|Grant access to specific sites to connect to specific USB devices|
|[WebUsbAskForUrls](#webusbaskforurls)|Allow WebUSB on specific sites|
|[WebUsbBlockedForUrls](#webusbblockedforurls)|Block WebUSB on specific sites|
|[WindowCaptureAllowedByOrigins](#windowcaptureallowedbyorigins)|Allow Window and Tab capture by these origins|
|[WorkspacesNavigationSettings](#workspacesnavigationsettings)|Configure navigation settings per groups of URLs in Microsoft Edge Workspaces|

## See also

- [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business)
