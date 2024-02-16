---
title: "Policy filters for the Enterprise personal browser"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 08/25/2023
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Policies that only apply to the work browser profile."
---

# Policy filters for the Enterprise personal browser

The Enterprise personal browser (MSA profile) is a lightly managed profile on managed devices that will automatically inherit admin policies from the Work browser (Microsoft Entra profile) for the following categories:
- Security
- Data Compliance
- Microsoft Edge Update

The work browser policies in the following section aren't available for the Enterprise personal browser (MSA profile).

## Work browser policies

The following policies only apply to the Microsoft Edge work browser profile.

| Policy Name | Caption |
|:-|:-|
|[AddressBarMicrosoftSearchInBingProviderEnabled](/deployedge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled)|Enable Microsoft Search in Bing suggestions in the address bar|
|[AdsSettingForIntrusiveAdsSites](/deployedge/microsoft-edge-policies#adssettingforintrusiveadssites)|Ads setting for sites with intrusive ads|
|[AdsTransparencyEnabled](/deployedge/microsoft-edge-policies#adstransparencyenabled)|Configure if the ads transparency feature is enabled|
|[AllowDeletingBrowserHistory](/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory)|Enable deleting browser and download history|
|[AllowGamesMenu](/deployedge/microsoft-edge-policies#allowgamesmenu)|Allow users to access the games menu (deprecated)|
|[AllowSurfGame](/deployedge/microsoft-edge-policies#allowsurfgame)|Allow surf game|
|[AllowTrackingForUrls](/deployedge/microsoft-edge-policies#allowtrackingforurls)|Configure tracking prevention exceptions for specific sites|
|[AllowedDomainsForApps](/deployedge/microsoft-edge-policies#alloweddomainsforapps)|Define domains allowed to access Google Workspace|
|[AlternateErrorPagesEnabled](/deployedge/microsoft-edge-policies#alternateerrorpagesenabled)|Suggest similar pages when a webpage can't be found|
|[AlwaysOpenPdfExternally](/deployedge/microsoft-edge-policies#alwaysopenpdfexternally)|Always open PDF files externally|
|[AutofillAddressEnabled](/deployedge/microsoft-edge-policies#autofilladdressenabled)|Enable AutoFill for addresses|
|[AutofillCreditCardEnabled](/deployedge/microsoft-edge-policies#autofillcreditcardenabled)|Enable AutoFill for payment instruments|
|[AutofillMembershipsEnabled](/deployedge/microsoft-edge-policies#autofillmembershipsenabled)|Save and fill memberships|
|[AutomaticDownloadsAllowedForUrls](/deployedge/microsoft-edge-policies#automaticdownloadsallowedforurls)|Allow multiple automatic downloads in quick succession on specific sites|
|[AutoplayAllowed](/deployedge/microsoft-edge-policies#autoplayallowed)|Allow media autoplay for websites|
|[AutoplayAllowlist](/deployedge/microsoft-edge-policies#autoplayallowlist)|Allow media autoplay on specific sites|
|[BlockExternalExtensions](/deployedge/microsoft-edge-policies#blockexternalextensions)|Blocks external extensions from being installed|
|[BrowserNetworkTimeQueriesEnabled](/deployedge/microsoft-edge-policies#browsernetworktimequeriesenabled)|Allow queries to a Browser Network Time service|
|[ClipboardAllowedForUrls](/deployedge/microsoft-edge-policies#clipboardallowedforurls)|Allow clipboard use on specific sites|
|[CollectionsServicesAndExportsBlockList](/deployedge/microsoft-edge-policies#collectionsservicesandexportsblocklist)|Block access to a specified list of services and export targets in Collections|
|[ComposeInlineEnabled](/deployedge/microsoft-edge-policies#composeinlineenabled)|Compose is enabled for writing on the web|
|[ConfigureDoNotTrack](/deployedge/microsoft-edge-policies#configuredonottrack)|Configure Do Not Track|
|[ConfigureFriendlyURLFormat](/deployedge/microsoft-edge-policies#configurefriendlyurlformat)|Configure the default paste format of URLs copied from Microsoft Edge, and determine if additional formats will be available to users|
|[ConfigureKeyboardShortcuts](/deployedge/microsoft-edge-policies#configurekeyboardshortcuts)|Configure the list of commands for which to disable keyboard shortcuts|
|[ConfigureOnlineTextToSpeech](/deployedge/microsoft-edge-policies#configureonlinetexttospeech)|Configure Online Text To Speech|
|[ConfigureShare](/deployedge/microsoft-edge-policies#configureshare)|Configure the Share experience|
|[ControlDefaultStateOfAllowExtensionFromOtherStoresSettingEnabled](/deployedge/microsoft-edge-policies#controldefaultstateofallowextensionfromotherstoressettingenabled)|Configure default state of Allow extensions from other stores setting|
|[CryptoWalletEnabled](/deployedge/microsoft-edge-policies#cryptowalletenabled)|Enable CryptoWallet feature|
|[CustomHelpLink](/deployedge/microsoft-edge-policies#customhelplink)|Specify custom help link|
|[DefaultAutomaticDownloadsSetting](/deployedge/microsoft-edge-policies#defaultautomaticdownloadssetting)|Default automatic downloads setting|
|[DefaultImagesSetting](/deployedge/microsoft-edge-policies#defaultimagessetting)|Default images setting|
|[DefaultInsecureContentSetting](/deployedge/microsoft-edge-policies#defaultinsecurecontentsetting)|Control use of insecure content exceptions|
|[DefaultJavaScriptJitSetting](/deployedge/microsoft-edge-policies#defaultjavascriptjitsetting)|Control use of JavaScript JIT|
|[DefaultJavaScriptSetting](/deployedge/microsoft-edge-policies#defaultjavascriptsetting)|Default JavaScript setting|
|[DefaultNotificationsSetting](/deployedge/microsoft-edge-policies#defaultnotificationssetting)|Default notification setting|
|[DefaultPopupsSetting](/deployedge/microsoft-edge-policies#defaultpopupssetting)|Default pop-up window setting|
|[DefaultPrinterSelection](/deployedge/microsoft-edge-policies#defaultprinterselection)|Default printer selection rules|
|[DefaultSearchProviderContextMenuAccessAllowed](/deployedge/microsoft-edge-policies#defaultsearchprovidercontextmenuaccessallowed)|Allow default search provider context menu search access|
|[DefaultSearchProviderEnabled](/deployedge/microsoft-edge-policies#defaultsearchproviderenabled)|Enable the default search provider|
|[DefaultSearchProviderEncodings](/deployedge/microsoft-edge-policies#defaultsearchproviderencodings)|Default search provider encodings|
|[DefaultSearchProviderImageURL](/deployedge/microsoft-edge-policies#defaultsearchproviderimageurl)|Specifies the search-by-image feature for the default search provider|
|[DefaultSearchProviderImageURLPostParams](/deployedge/microsoft-edge-policies#defaultsearchproviderimageurlpostparams)|Parameters for an image URL that uses POST|
|[DefaultSearchProviderKeyword](/deployedge/microsoft-edge-policies#defaultsearchproviderkeyword)|Default search provider keyword|
|[DefaultSearchProviderName](/deployedge/microsoft-edge-policies#defaultsearchprovidername)|Default search provider name|
|[DefaultSearchProviderSearchURL](/deployedge/microsoft-edge-policies#defaultsearchprovidersearchurl)|Default search provider search URL|
|[DefaultSearchProviderSuggestURL](/deployedge/microsoft-edge-policies#defaultsearchprovidersuggesturl)|Default search provider URL for suggestions|
|[DefinePreferredLanguages](/deployedge/microsoft-edge-policies#definepreferredlanguages)|Define an ordered list of preferred languages that websites should display in if the site supports the language|
|[DelayNavigationsForInitialSiteListDownload](/deployedge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload)|Require that the Enterprise Mode Site List is available before tab navigation|
|[DeveloperToolsAvailability](/deployedge/microsoft-edge-policies#developertoolsavailability)|Control where developer tools can be used|
|[Disable3DAPIs](/deployedge/microsoft-edge-policies#disable3dapis)|Disable support for 3D graphics APIs|
|[DiscoverPageContextEnabled](/deployedge/microsoft-edge-policies#discoverpagecontextenabled)|Enable Discover access to page contents for Microsoft Entra profiles|
|[DoNotSilentlyBlockProtocolsFromOrigins](/deployedge/microsoft-edge-policies#donotsilentlyblockprotocolsfromorigins)|Define a list of protocols that can not be silently blocked by anti-flood protection|
|[DoubleClickCloseTabEnabled](/deployedge/microsoft-edge-policies#doubleclickclosetabenabled)|Double Click feature in Microsoft Edge enabled (only available in China)|
|[DownloadDirectory](/deployedge/microsoft-edge-policies#downloaddirectory)|Set download directory|
|[DownloadRestrictions](/deployedge/microsoft-edge-policies#downloadrestrictions)|Allow download restrictions|
|[EdgeAssetDeliveryServiceEnabled](/deployedge/microsoft-edge-policies#edgeassetdeliveryserviceenabled)|Allow features to download assets from the Asset Delivery Service|
|[EdgeCollectionsEnabled](/deployedge/microsoft-edge-policies#edgecollectionsenabled)|Enable the Collections feature|
|[EdgeEDropEnabled](/deployedge/microsoft-edge-policies#edgeedropenabled)|Enable Drop feature in Microsoft Edge|
|[EdgeEnhanceImagesEnabled](/deployedge/microsoft-edge-policies#edgeenhanceimagesenabled)|Enhance images enabled|
|[EdgeFollowEnabled](/deployedge/microsoft-edge-policies#edgefollowenabled)|Enable Follow service in Microsoft Edge|
|[EdgeShoppingAssistantEnabled](/deployedge/microsoft-edge-policies#edgeshoppingassistantenabled)|Shopping in Microsoft Edge Enabled|
|[EdgeWalletCheckoutEnabled](/deployedge/microsoft-edge-policies#edgewalletcheckoutenabled)|Enable Wallet Checkout feature|
|[EdgeWorkspacesEnabled](/deployedge/microsoft-edge-policies#edgeworkspacesenabled)|Enable Workspaces|
|[EditFavoritesEnabled](/deployedge/microsoft-edge-policies#editfavoritesenabled)|Allows users to edit favorites|
|[EnableMediaRouter](/deployedge/microsoft-edge-policies#enablemediarouter)|Enable Google Cast|
|[EnterpriseHardwarePlatformAPIEnabled](/deployedge/microsoft-edge-policies#enterprisehardwareplatformapienabled)|Allow managed extensions to use the Enterprise Hardware Platform API|
|[EnterpriseModeSiteListManagerAllowed](/deployedge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed)|Allow access to the Enterprise Mode Site List Manager tool|
|[EventPathEnabled](/deployedge/microsoft-edge-policies#eventpathenabled)|Re-enable the Event.path API until Microsoft Edge version 115 (obsolete)|
|[ExtensionAllowedTypes](/deployedge/microsoft-edge-policies#extensionallowedtypes)|Configure allowed extension types|
|[ExtensionInstallAllowlist](/deployedge/microsoft-edge-policies#extensioninstallallowlist)|Allow specific extensions to be installed|
|[ExtensionInstallBlocklist](/deployedge/microsoft-edge-policies#extensioninstallblocklist)|Control which extensions cannot be installed|
|[ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings)|Configure extension management settings|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](/deployedge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox)|Show an "Always open" checkbox in external protocol dialog|
|[FavoritesBarEnabled](/deployedge/microsoft-edge-policies#favoritesbarenabled)|Enable favorites bar|
|[FetchKeepaliveDurationSecondsOnShutdown](/deployedge/microsoft-edge-policies#fetchkeepalivedurationsecondsonshutdown)|Fetch keepalive duration on shutdown|
|[ForceEphemeralProfiles](/deployedge/microsoft-edge-policies#forceephemeralprofiles)|Enable use of ephemeral profiles|
|[ForceMajorVersionToMinorPositionInUserAgent](/deployedge/microsoft-edge-policies#forcemajorversiontominorpositioninuseragent)|Enable or disable freezing the User-Agent string at major version 99|
|[ForceSync](/deployedge/microsoft-edge-policies#forcesync)|Force synchronization of browser data and do not show the sync consent prompt|
|[ForceSyncTypes](/deployedge/microsoft-edge-policies#forcesynctypes)|Configure the list of types that are included for synchronization|
|[ForceYouTubeRestrict](/deployedge/microsoft-edge-policies#forceyoutuberestrict)|Force minimum YouTube Restricted Mode|
|[FullscreenAllowed](/deployedge/microsoft-edge-policies#fullscreenallowed)|Allow full screen mode|
|[GloballyScopeHTTPAuthCacheEnabled](/deployedge/microsoft-edge-policies#globallyscopehttpauthcacheenabled)|Enable globally scoped HTTP auth cache|
|[HomepageIsNewTabPage](/deployedge/microsoft-edge-policies#homepageisnewtabpage)|Set the new tab page as the home page|
|[HomepageLocation](/deployedge/microsoft-edge-policies#homepagelocation)|Configure the home page URL|
|[HubsSidebarEnabled](/deployedge/microsoft-edge-policies#hubssidebarenabled)|Show Hubs Sidebar|
|[ImagesAllowedForUrls](/deployedge/microsoft-edge-policies#imagesallowedforurls)|Allow images on these sites|
|[ImagesBlockedForUrls](/deployedge/microsoft-edge-policies#imagesblockedforurls)|Block images on specific sites|
|[ImmersiveReaderGrammarToolsEnabled](/deployedge/microsoft-edge-policies#immersivereadergrammartoolsenabled)|Enable Grammar Tools feature within Immersive Reader in Microsoft Edge|
|[ImmersiveReaderPictureDictionaryEnabled](/deployedge/microsoft-edge-policies#immersivereaderpicturedictionaryenabled)|Enable Picture Dictionary feature within Immersive Reader in Microsoft Edge|
|[ImportAutofillFormData](/deployedge/microsoft-edge-policies#importautofillformdata)|Allow importing of autofill form data|
|[ImportBrowserSettings](/deployedge/microsoft-edge-policies#importbrowsersettings)|Allow importing of browser settings|
|[ImportCookies](/deployedge/microsoft-edge-policies#importcookies)|Allow importing of Cookies|
|[ImportExtensions](/deployedge/microsoft-edge-policies#importextensions)|Allow importing of extensions|
|[ImportFavorites](/deployedge/microsoft-edge-policies#importfavorites)|Allow importing of favorites|
|[ImportHistory](/deployedge/microsoft-edge-policies#importhistory)|Allow importing of browsing history|
|[ImportHomepage](/deployedge/microsoft-edge-policies#importhomepage)|Allow importing of home page settings|
|[ImportOnEachLaunch](/deployedge/microsoft-edge-policies#importoneachlaunch)|Allow import of data from other browsers on each Microsoft Edge launch|
|[ImportOpenTabs](/deployedge/microsoft-edge-policies#importopentabs)|Allow importing of open tabs|
|[ImportPaymentInfo](/deployedge/microsoft-edge-policies#importpaymentinfo)|Allow importing of payment info|
|[ImportSavedPasswords](/deployedge/microsoft-edge-policies#importsavedpasswords)|Allow importing of saved passwords|
|[ImportSearchEngine](/deployedge/microsoft-edge-policies#importsearchengine)|Allow importing of search engine settings|
|[ImportShortcuts](/deployedge/microsoft-edge-policies#importshortcuts)|Allow importing of shortcuts|
|[ImportStartupPageSettings](/deployedge/microsoft-edge-policies#importstartuppagesettings)|Allow importing of startup page settings|
|[InsecureContentAllowedForUrls](/deployedge/microsoft-edge-policies#insecurecontentallowedforurls)|Allow insecure content on specified sites|
|[InsecureContentBlockedForUrls](/deployedge/microsoft-edge-policies#insecurecontentblockedforurls)|Block insecure content on specified sites|
|[InsecureFormsWarningsEnabled](/deployedge/microsoft-edge-policies#insecureformswarningsenabled)|Enable warnings for insecure forms|
|[JavaScriptAllowedForUrls](/deployedge/microsoft-edge-policies#javascriptallowedforurls)|Allow JavaScript on specific sites|
|[JavaScriptBlockedForUrls](/deployedge/microsoft-edge-policies#javascriptblockedforurls)|Block JavaScript on specific sites|
|[JavaScriptJitAllowedForSites](/deployedge/microsoft-edge-policies#javascriptjitallowedforsites)|Allow JavaScript to use JIT on these sites|
|[JavaScriptJitBlockedForSites](/deployedge/microsoft-edge-policies#javascriptjitblockedforsites)|Block JavaScript from using JIT on these sites|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist)|Revert to legacy SameSite behavior for cookies on specified sites|
|[LinkedAccountEnabled](/deployedge/microsoft-edge-policies#linkedaccountenabled)|Enable the linked account feature|
|[LiveCaptionsAllowed](/deployedge/microsoft-edge-policies#livecaptionsallowed)|Live captions allowed|
|[LocalBrowserDataShareEnabled](/deployedge/microsoft-edge-policies#localbrowserdatashareenabled)|Enable Windows to search local Microsoft Edge browsing data|
|[LocalProvidersEnabled](/deployedge/microsoft-edge-policies#localprovidersenabled)|Allow suggestions from local providers|
|[ManagedConfigurationPerOrigin](/deployedge/microsoft-edge-policies#managedconfigurationperorigin)|Sets managed configuration values for websites to specific origins|
|[ManagedFavorites](/deployedge/microsoft-edge-policies#managedfavorites)|Configure favorites|
|[ManagedSearchEngines](/deployedge/microsoft-edge-policies#managedsearchengines)|Manage Search Engines|
|[MicrosoftEdgeInsiderPromotionEnabled](/deployedge/microsoft-edge-policies#microsoftedgeinsiderpromotionenabled)|Microsoft Edge Insider Promotion Enabled|
|[MicrosoftEditorProofingEnabled](/deployedge/microsoft-edge-policies#microsofteditorproofingenabled)|Spell checking provided by Microsoft Editor|
|[MicrosoftEditorSynonymsEnabled](/deployedge/microsoft-edge-policies#microsofteditorsynonymsenabled)|Synonyms are provided when using Microsoft Editor spell checker|
|[MicrosoftOfficeMenuEnabled](/deployedge/microsoft-edge-policies#microsoftofficemenuenabled)|Allow users to access the Microsoft Office menu (deprecated)|
|[MouseGestureEnabled](/deployedge/microsoft-edge-policies#mousegestureenabled)|Mouse Gesture Enabled|
|[NativeMessagingAllowlist](/deployedge/microsoft-edge-policies#nativemessagingallowlist)|Control which native messaging hosts users can use|
|[NativeMessagingBlocklist](/deployedge/microsoft-edge-policies#nativemessagingblocklist)|Configure native messaging block list|
|[NativeMessagingUserLevelHosts](/deployedge/microsoft-edge-policies#nativemessaginguserlevelhosts)|Allow user-level native messaging hosts (installed without admin permissions)|
|[NavigationDelayForInitialSiteListDownloadTimeout](/deployedge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout)|Set a timeout for delay of tab navigation for the Enterprise Mode Site List|
|[NetworkPredictionOptions](/deployedge/microsoft-edge-policies#networkpredictionoptions)|Enable network prediction|
|[NewPDFReaderEnabled](/deployedge/microsoft-edge-policies#newpdfreaderenabled)|Microsoft Edge built-in PDF reader powered by Adobe Acrobat enabled|
|[NewTabPageAllowedBackgroundTypes](/deployedge/microsoft-edge-policies#newtabpageallowedbackgroundtypes)|Configure the background types allowed for the new tab page layout|
|[NewTabPageAppLauncherEnabled](/deployedge/microsoft-edge-policies#newtabpageapplauncherenabled)|Hide App Launcher on Microsoft Edge new tab page|
|[NewTabPageContentEnabled](/deployedge/microsoft-edge-policies#newtabpagecontentenabled)|Allow Microsoft News content on the new tab page|
|[NewTabPageHideDefaultTopSites](/deployedge/microsoft-edge-policies#newtabpagehidedefaulttopsites)|Hide the default top sites from the new tab page|
|[NewTabPageLocation](/deployedge/microsoft-edge-policies#newtabpagelocation)|Configure the new tab page URL|
|[NewTabPageManagedQuickLinks](/deployedge/microsoft-edge-policies#newtabpagemanagedquicklinks)|Set new tab page quick links|
|[NewTabPagePrerenderEnabled](/deployedge/microsoft-edge-policies#newtabpageprerenderenabled)|Enable preload of the new tab page for faster rendering|
|[NewTabPageQuickLinksEnabled](/deployedge/microsoft-edge-policies#newtabpagequicklinksenabled)|Allow quick links on the new tab page|
|[NewTabPageSearchBox](/deployedge/microsoft-edge-policies#newtabpagesearchbox)|Configure the new tab page search box experience|
|[NotificationsAllowedForUrls](/deployedge/microsoft-edge-policies#notificationsallowedforurls)|Allow notifications on specific sites|
|[NotificationsBlockedForUrls](/deployedge/microsoft-edge-policies#notificationsblockedforurls)|Block notifications on specific sites|
|[OriginAgentClusterDefaultEnabled](/deployedge/microsoft-edge-policies#originagentclusterdefaultenabled)|Origin-keyed agent clustering enabled by default|
|[PDFSecureMode](/deployedge/microsoft-edge-policies#pdfsecuremode)|Secure mode and Certificate-based Digital Signature validation in native PDF reader|
|[PDFXFAEnabled](/deployedge/microsoft-edge-policies#pdfxfaenabled)|XFA support in native PDF reader enabled|
|[PasswordGeneratorEnabled](/deployedge/microsoft-edge-policies#passwordgeneratorenabled)|Allow users to get a strong password suggestion whenever they are creating an account online|
|[PasswordManagerBlocklist](/deployedge/microsoft-edge-policies#passwordmanagerblocklist)|Configure the list of domains for which the password manager UI (Save and Fill) will be disabled|
|[PasswordManagerEnabled](/deployedge/microsoft-edge-policies#passwordmanagerenabled)|Enable saving passwords to the password manager|
|[PasswordManagerRestrictLengthEnabled](/deployedge/microsoft-edge-policies#passwordmanagerrestrictlengthenabled)|Restrict the length of passwords that can be saved in the Password Manager|
|[PasswordMonitorAllowed](/deployedge/microsoft-edge-policies#passwordmonitorallowed)|Allow users to be alerted if their passwords are found to be unsafe|
|[PasswordProtectionChangePasswordURL](/deployedge/microsoft-edge-policies#passwordprotectionchangepasswordurl)|Configure the change password URL|
|[PasswordProtectionLoginURLs](/deployedge/microsoft-edge-policies#passwordprotectionloginurls)|Configure the list of enterprise login URLs where the password protection service should capture salted hashes of a password|
|[PasswordProtectionWarningTrigger](/deployedge/microsoft-edge-policies#passwordprotectionwarningtrigger)|Configure password protection warning trigger|
|[PasswordRevealEnabled](/deployedge/microsoft-edge-policies#passwordrevealenabled)|Enable Password reveal button|
|[PaymentMethodQueryEnabled](/deployedge/microsoft-edge-policies#paymentmethodqueryenabled)|Allow websites to query for available payment methods|
|[PerformanceDetectorEnabled](/deployedge/microsoft-edge-policies#performancedetectorenabled)|Performance Detector Enabled|
|[PinBrowserEssentialsToolbarButton](/deployedge/microsoft-edge-policies#pinbrowseressentialstoolbarbutton)|Pin browser essentials toolbar button|
|[PopupsAllowedForUrls](/deployedge/microsoft-edge-policies#popupsallowedforurls)|Allow pop-up windows on specific sites|
|[PopupsBlockedForUrls](/deployedge/microsoft-edge-policies#popupsblockedforurls)|Block pop-up windows on specific sites|
|[PrimaryPasswordSetting](/deployedge/microsoft-edge-policies#primarypasswordsetting)|Configures a setting that asks users to enter their device password while using password autofill|
|[PrintPdfAsImageDefault](/deployedge/microsoft-edge-policies#printpdfasimagedefault)|Print PDF as Image Default|
|[PrintPostScriptMode](/deployedge/microsoft-edge-policies#printpostscriptmode)|Print PostScript Mode|
|[PrintPreviewStickySettings](/deployedge/microsoft-edge-policies#printpreviewstickysettings)|Configure the sticky print preview settings|
|[PrintPreviewUseSystemDefaultPrinter](/deployedge/microsoft-edge-policies#printpreviewusesystemdefaultprinter)|Set the system default printer as the default printer|
|[PrintRasterizationMode](/deployedge/microsoft-edge-policies#printrasterizationmode)|Print Rasterization Mode|
|[PrintRasterizePdfDpi](/deployedge/microsoft-edge-policies#printrasterizepdfdpi)|Print Rasterize PDF DPI|
|[PrintStickySettings](/deployedge/microsoft-edge-policies#printstickysettings)|Print preview sticky settings|
|[PrinterTypeDenyList](/deployedge/microsoft-edge-policies#printertypedenylist)|Disable printer types on the deny list|
|[PrintingAllowedBackgroundGraphicsModes](/deployedge/microsoft-edge-policies#printingallowedbackgroundgraphicsmodes)|Restrict background graphics printing mode|
|[PrintingBackgroundGraphicsDefault](/deployedge/microsoft-edge-policies#printingbackgroundgraphicsdefault)|Default background graphics printing mode|
|[PrintingEnabled](/deployedge/microsoft-edge-policies#printingenabled)|Enable printing|
|[PrintingPaperSizeDefault](/deployedge/microsoft-edge-policies#printingpapersizedefault)|Default printing page size|
|[PrintingWebpageLayout](/deployedge/microsoft-edge-policies#printingwebpagelayout)|Sets layout for printing|
|[PromptForDownloadLocation](/deployedge/microsoft-edge-policies#promptfordownloadlocation)|Ask where to save downloaded files|
|[PromptOnMultipleMatchingCertificates](/deployedge/microsoft-edge-policies#promptonmultiplematchingcertificates)|Prompt the user to select a certificate when multiple certificates match|
|[ProxyBypassList](/deployedge/microsoft-edge-policies#proxybypasslist)|Configure proxy bypass rules (deprecated)|
|[ProxyMode](/deployedge/microsoft-edge-policies#proxymode)|Configure proxy server settings (deprecated)|
|[ProxyPacUrl](/deployedge/microsoft-edge-policies#proxypacurl)|Set the proxy .pac file URL (deprecated)|
|[ProxyServer](/deployedge/microsoft-edge-policies#proxyserver)|Configure address or URL of proxy server (deprecated)|
|[QuickSearchShowMiniMenu](/deployedge/microsoft-edge-policies#quicksearchshowminimenu)|Enables Microsoft Edge mini menu|
|[QuickViewOfficeFilesEnabled](/deployedge/microsoft-edge-policies#quickviewofficefilesenabled)|Manage QuickView Office files capability in Microsoft Edge|
|[ReadAloudEnabled](/deployedge/microsoft-edge-policies#readaloudenabled)|Enable Read Aloud feature in Microsoft Edge|
|[RegisteredProtocolHandlers](/deployedge/microsoft-edge-policies#registeredprotocolhandlers)|Register protocol handlers|
|[RelatedMatchesCloudServiceEnabled](/deployedge/microsoft-edge-policies#relatedmatchescloudserviceenabled)|Configure Related Matches in Find on Page|
|[ResolveNavigationErrorsUseWebService](/deployedge/microsoft-edge-policies#resolvenavigationerrorsusewebservice)|Enable resolution of navigation errors using a web service|
|[RestoreOnStartup](/deployedge/microsoft-edge-policies#restoreonstartup)|Action to take on startup|
|[RestoreOnStartupURLs](/deployedge/microsoft-edge-policies#restoreonstartupurls)|Sites to open when the browser starts|
|[RestoreOnStartupUserURLsEnabled](/deployedge/microsoft-edge-policies#restoreonstartupuserurlsenabled)|Allow users to add and remove their own sites during startup when the RestoreOnStartupURLs policy is configured|
|[RestorePdfView](/deployedge/microsoft-edge-policies#restorepdfview)|Restore PDF view|
|[SSLErrorOverrideAllowed](/deployedge/microsoft-edge-policies#sslerroroverrideallowed)|Allow users to proceed from the HTTPS warning page|
|[SSLErrorOverrideAllowedForOrigins](/deployedge/microsoft-edge-policies#sslerroroverrideallowedfororigins)|Allow users to proceed from the HTTPS warning page for specific origins|
|[SameOriginTabCaptureAllowedByOrigins](/deployedge/microsoft-edge-policies#sameorigintabcaptureallowedbyorigins)|Allow Same Origin Tab capture by these origins|
|[ScreenCaptureAllowed](/deployedge/microsoft-edge-policies#screencaptureallowed)|Allow or deny screen capture|
|[ScreenCaptureAllowedByOrigins](/deployedge/microsoft-edge-policies#screencaptureallowedbyorigins)|Allow Desktop, Window, and Tab capture by these origins|
|[ScrollToTextFragmentEnabled](/deployedge/microsoft-edge-policies#scrolltotextfragmentenabled)|Enable scrolling to text specified in URL fragments|
|[SearchFiltersEnabled](/deployedge/microsoft-edge-policies#searchfiltersenabled)|Search Filters Enabled|
|[SearchForImageEnabled](/deployedge/microsoft-edge-policies#searchforimageenabled)|Search for image enabled|
|[SearchInSidebarEnabled](/deployedge/microsoft-edge-policies#searchinsidebarenabled)|Search in Sidebar enabled|
|[SearchSuggestEnabled](/deployedge/microsoft-edge-policies#searchsuggestenabled)|Enable search suggestions|
|[SecurityKeyPermitAttestation](/deployedge/microsoft-edge-policies#securitykeypermitattestation)|Websites or domains that don't need permission to use direct Security Key attestation|
|[SendIntranetToInternetExplorer](/deployedge/microsoft-edge-policies#sendintranettointernetexplorer)|Send all intranet sites to Internet Explorer|
|[SensorsAllowedForUrls](/deployedge/microsoft-edge-policies#sensorsallowedforurls)|Allow access to sensors on specific sites|
|[SensorsBlockedForUrls](/deployedge/microsoft-edge-policies#sensorsblockedforurls)|Block access to sensors on specific sites|
|[SerialAskForUrls](/deployedge/microsoft-edge-policies#serialaskforurls)|Allow the Serial API on specific sites|
|[SerialBlockedForUrls](/deployedge/microsoft-edge-policies#serialblockedforurls)|Block the Serial API on specific sites|
|[ShowAcrobatSubscriptionButton](/deployedge/microsoft-edge-policies#showacrobatsubscriptionbutton)|Shows button on native PDF viewer in Microsoft Edge that allows users to sign up for Adobe Acrobat subscription|
|[ShowCastIconInToolbar](/deployedge/microsoft-edge-policies#showcasticonintoolbar)|Show the cast icon in the toolbar|
|[ShowDownloadsToolbarButton](/deployedge/microsoft-edge-policies#showdownloadstoolbarbutton)|Show Downloads button on the toolbar|
|[ShowHomeButton](/deployedge/microsoft-edge-policies#showhomebutton)|Show Home button on toolbar|
|[ShowMicrosoftRewards](/deployedge/microsoft-edge-policies#showmicrosoftrewards)|Show Microsoft Rewards experiences|
|[ShowOfficeShortcutInFavoritesBar](/deployedge/microsoft-edge-policies#showofficeshortcutinfavoritesbar)|Show Microsoft Office shortcut in favorites bar (deprecated)|
|[ShowPDFDefaultRecommendationsEnabled](/deployedge/microsoft-edge-policies#showpdfdefaultrecommendationsenabled)|Allow notifications to set Microsoft Edge as default PDF reader|
|[ShowRecommendationsEnabled](/deployedge/microsoft-edge-policies#showrecommendationsenabled)|Allow feature recommendations and browser assistance notifications from Microsoft Edge|
|[SignedHTTPExchangeEnabled](/deployedge/microsoft-edge-policies#signedhttpexchangeenabled)|Enable Signed HTTP Exchange (SXG) support|
|[SleepingTabsBlockedForUrls](/deployedge/microsoft-edge-policies#sleepingtabsblockedforurls)|Block sleeping tabs on specific sites|
|[SleepingTabsEnabled](/deployedge/microsoft-edge-policies#sleepingtabsenabled)|Configure sleeping tabs|
|[SleepingTabsTimeout](/deployedge/microsoft-edge-policies#sleepingtabstimeout)|Set the background tab inactivity timeout for sleeping tabs|
|[SmartActionsBlockList](/deployedge/microsoft-edge-policies#smartactionsblocklist)|Block smart actions for a list of services|
|[SpeechRecognitionEnabled](/deployedge/microsoft-edge-policies#speechrecognitionenabled)|Configure Speech Recognition|
|[SpellcheckEnabled](/deployedge/microsoft-edge-policies#spellcheckenabled)|Enable spellcheck|
|[SpellcheckLanguage](/deployedge/microsoft-edge-policies#spellchecklanguage)|Enable specific spellcheck languages|
|[SpellcheckLanguageBlocklist](/deployedge/microsoft-edge-policies#spellchecklanguageblocklist)|Force disable spellcheck languages|
|[SyncDisabled](/deployedge/microsoft-edge-policies#syncdisabled)|Disable synchronization of data using Microsoft sync services|
|[TabCaptureAllowedByOrigins](/deployedge/microsoft-edge-policies#tabcaptureallowedbyorigins)|Allow Tab capture by these origins|
|[TabServicesEnabled](/deployedge/microsoft-edge-policies#tabservicesenabled)|Tab Services enabled|
|[TextPredictionEnabled](/deployedge/microsoft-edge-policies#textpredictionenabled)|Text prediction enabled by default|
|[TrackingPrevention](/deployedge/microsoft-edge-policies#trackingprevention)|Block tracking of users' web-browsing activity|
|[TranslateEnabled](/deployedge/microsoft-edge-policies#translateenabled)|Enable Translate|
|[URLAllowlist](/deployedge/microsoft-edge-policies#urlallowlist)|Define a list of allowed URLs|
|[URLBlocklist](/deployedge/microsoft-edge-policies#urlblocklist)|Block access to a list of URLs|
|[UnthrottledNestedTimeoutEnabled](/deployedge/microsoft-edge-policies#unthrottlednestedtimeoutenabled)|JavaScript setTimeout will not be clamped until a higher nesting threshold is set (deprecated)|
|[UserAgentReduction](/deployedge/microsoft-edge-policies#useragentreduction)|Enable or disable the User-Agent Reduction|
|[VerticalTabsAllowed](/deployedge/microsoft-edge-policies#verticaltabsallowed)|Configures availability of a vertical layout for tabs on the side of the browser|
|[VideoCaptureAllowed](/deployedge/microsoft-edge-policies#videocaptureallowed)|Allow or block video capture|
|[VideoCaptureAllowedUrls](/deployedge/microsoft-edge-policies#videocaptureallowedurls)|Sites that can access video capture devices without requesting permission|
|[VisualSearchEnabled](/deployedge/microsoft-edge-policies#visualsearchenabled)|Visual search enabled|
|[WalletDonationEnabled](/deployedge/microsoft-edge-policies#walletdonationenabled)|Wallet Donation Enabled|
|[WebAppInstallForceList](/deployedge/microsoft-edge-policies#webappinstallforcelist)|Configure list of force-installed Web Apps|
|[WebHidAskForUrls](/deployedge/microsoft-edge-policies#webhidaskforurls)|Allow the WebHID API on these sites|
|[WebHidBlockedForUrls](/deployedge/microsoft-edge-policies#webhidblockedforurls)|Block the WebHID API on these sites|
|[WebRtcLocalIpsAllowedUrls](/deployedge/microsoft-edge-policies#webrtclocalipsallowedurls)|Manage exposure of local IP addressess by WebRTC|
|[WebRtcLocalhostIpHandling](/deployedge/microsoft-edge-policies#webrtclocalhostiphandling)|Restrict exposure of local IP address by WebRTC|
|[WebRtcUdpPortRange](/deployedge/microsoft-edge-policies#webrtcudpportrange)|Restrict the range of local UDP ports used by WebRTC|
|[WebSQLAccess](/deployedge/microsoft-edge-policies#websqlaccess)|Force WebSQL to be enabled|
|[WebSelectEnabled](/deployedge/microsoft-edge-policies#webselectenabled)|Web Select Enabled (deprecated)|
|[WorkspacesNavigationSettings](/deployedge/microsoft-edge-policies#workspacesnavigationsettings)|Configure navigation settings per groups of URLs in Microsoft Edge Workspaces|

## See also

- [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business)
