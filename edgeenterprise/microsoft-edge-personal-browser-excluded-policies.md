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
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |






## See also

- [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business)

