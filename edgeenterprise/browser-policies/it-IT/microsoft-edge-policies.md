---
title: "Microsoft Edge Browser Policy Documentation"
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 09/11/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom:
description: "Windows and Mac documentation for all policies supported by the Microsoft Edge Browser"
---

# Microsoft Edge - Criteri
L'ultima versione di Microsoft Edge include i criteri seguenti. Puoi utilizzare questi criteri per configurare il modo in cui Microsoft Edge viene eseguito nell'organizzazione.

Per informazioni su un set aggiuntivo di criteri utilizzati per controllare come e quando Microsoft Edge viene aggiornato, vedi [Riferimento ai criteri di aggiornamento di Microsoft Edge](microsoft-edge-update-policies.md)

Puoi scaricare [Toolkit di conformità di Microsoft Security](https://www.microsoft.com/download/details.aspx?id=55319) per le impostazioni iniziali di configurazione della sicurezza consigliate per Microsoft Edge. Per altre informazioni, vedi [Blog sulle linee di base di Microsoft Security](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)

> [!NOTA]
> Questo articolo si applica a Microsoft Edge versione 77 o successiva.

## Criteri disponibili
Queste tabelle elencano tutti i criteri di gruppo correlati al browser disponibili in questa versione di Microsoft Edge. Utilizza i collegamenti nella tabella per ottenere altri dettagli sui criteri specifici.

|||
|-|-|
|[Autenticazione HTTP](#autenticazione-http)|[Avvio, pagina iniziale e nuova scheda](#avvio-pagina-iniziale-e-nuova-scheda)|
|[Cast](#cast)|[Estensioni](#estensioni)|
|[Impostazioni SmartScreen](#impostazioni-smartscreen)|[Impostazioni dei contenuti](#impostazioni-dei-contenuti)|
|[Impostazioni di Application Guard](#impostazioni-di-application-guard)|[Messaggi nativi](#messaggi-nativi)|
|[Protezione e gestione password](#protezione-e-gestione-password)|[Provider di ricerca predefinito](#provider-di-ricerca-predefinito)|
|[Server proxy](#server-proxy)|[Stampa](#stampa)|
|[Additional](#additional)|

### [*Autenticazione HTTP*](#autenticazione-http-policies)
|Nome criteri|Sottotitolo|
|-|-|
|[AllowCrossOriginAuthPrompt](#allowcrossoriginauthprompt)|Consenti le richieste di autenticazione di base HTTP tra le origini|
|[AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)|Specifica un elenco di server a cui Microsoft Edge può delegare le credenziali dell'utente|
|[AuthSchemes](#authschemes)|Schemi di autenticazione supportati|
|[AuthServerAllowlist](#authserverallowlist)|Configura l'elenco dei server di autenticazione consentiti|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|Disabilita la ricerca CNAME durante la negoziazione dell'autenticazione Kerberos|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|Includi la porta non standard in SPN Kerberos|
|[NtlmV2Enabled](#ntlmv2enabled)|Controlla se è abilitata l'autenticazione NTLMv2|
### [*Avvio&comma; pagina iniziale e nuova scheda*](#avvio-pagina-iniziale-e-nuova-scheda-policies)
|Nome criteri|Sottotitolo|
|-|-|
|[HomepageIsNewTabPage](#homepageisnewtabpage)|Imposta la nuova scheda come home page|
|[HomepageLocation](#homepagelocation)|Configura l'URL della home page|
|[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)|Configura i tipi di sfondo consentiti per il nuovo layout di pagina della nuova scheda|
|[NewTabPageCompanyLogo](#newtabpagecompanylogo)|Imposta logo aziendale nuova scheda (obsoleto)|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|Nascondi i siti principali predefiniti dalla nuova scheda|
|[NewTabPageLocation](#newtabpagelocation)|Configura l'URL della nuova scheda|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|Imposta collegamenti rapidi per la nuova scheda|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|Attiva precaricamento della nuova scheda per il rendering più veloce|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|Configura l'esperienza della nuova scheda di Microsoft Edge|
|[RestoreOnStartup](#restoreonstartup)|Azione da eseguire all'avvio|
|[RestoreOnStartupURLs](#restoreonstartupurls)|Siti da aprire quando si avvia il browser|
|[ShowHomeButton](#showhomebutton)|Mostra pulsante Home sulla barra degli strumenti|
### [*Cast*](#cast-policies)
|Nome criteri|Sottotitolo|
|-|-|
|[EnableMediaRouter](#enablemediarouter)|Abilita Google Cast|
|[ShowCastIconInToolbar](#showcasticonintoolbar)|Mostra l'icona cast nella barra degli strumenti|
### [*Estensioni*](#estensioni-policies)
|Nome criteri|Sottotitolo|
|-|-|
|[ExtensionAllowedTypes](#extensionallowedtypes)|Configura i tipi di estensione consentiti|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|Consenti l'installazione di estensioni specifiche|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|Controlla le estensioni che non possono essere installate|
|[ExtensionInstallForcelist](#extensioninstallforcelist)|Controlla quali estensioni vengono installate automaticamente|
|[ExtensionInstallSources](#extensioninstallsources)|Configura le origini di installazione degli script degli utenti e delle estensioni|
|[ExtensionSettings](#extensionsettings)|Configura le impostazioni di gestione delle estensioni|
### [*Impostazioni SmartScreen*](#impostazioni-smartscreen-policies)
|Nome criteri|Sottotitolo|
|-|-|
|[PreventSmartScreenPromptOverride](#preventsmartscreenpromptoverride)|Impedisci di ignorare i prompt di Microsoft Defender SmartScreen per i siti|
|[PreventSmartScreenPromptOverrideForFiles](#preventsmartscreenpromptoverrideforfiles)|Impedisci di ignorare gli avvisi di Microsoft Defender SmartScreen relativi ai download|
|[SmartScreenAllowListDomains](#smartscreenallowlistdomains)|Configura l'elenco dei domini per cui Microsoft Defender SmartScreen non attiva gli avvisi|
|[SmartScreenEnabled](#smartscreenenabled)|Configura Microsoft Defender SmartScreen|
|[SmartScreenForTrustedDownloadsEnabled](#smartscreenfortrusteddownloadsenabled)|Forza i controlli Microsoft Defender SmartScreen per i download da origini attendibili|
|[SmartScreenPuaEnabled](#smartscreenpuaenabled)|Configura Microsoft Defender SmartScreen per bloccare le app potenzialmente indesiderate|
### [*Impostazioni dei contenuti*](#impostazioni-dei-contenuti-policies)
|Nome criteri|Sottotitolo|
|-|-|
|[AutoSelectCertificateForUrls](#autoselectcertificateforurls)|Seleziona automaticamente i certificati client per questi siti|
|[CookiesAllowedForUrls](#cookiesallowedforurls)|Consenti i cookie per siti specifici|
|[CookiesBlockedForUrls](#cookiesblockedforurls)|Blocca i cookie per siti specifici|
|[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)|Limita i cookie provenienti da siti Web specifici per la sessione corrente|
|[DefaultCookiesSetting](#defaultcookiessetting)|Configura i cookie|
|[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)|Controlla l'uso dell'API file System per la lettura|
|[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)|Controlla l'uso dell'API file System per la scrittura|
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|Impostazione predefinita per la georilevazione|
|[DefaultImagesSetting](#defaultimagessetting)|Impostazione predefinita per le immagini|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|Controlla l'uso di eccezioni di contenuto non sicuro|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|Impostazione predefinita per JavaScript|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|Impostazione predefinita per la notifica|
|[DefaultPluginsSetting](#defaultpluginssetting)|Impostazione predefinita per Adobe Flash|
|[DefaultPopupsSetting](#defaultpopupssetting)|Impostazione predefinita per la finestra popup|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|Controlla l'uso dell'API Web Bluetooth|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|Controlla l'uso dell'API WebUSB|
|[FileSystemReadAskForUrls](#filesystemreadaskforurls)|Consenti accesso in lettura tramite l'API file System in questi siti|
|[FileSystemReadBlockedForUrls](#filesystemreadblockedforurls)|Blocca accesso in lettura tramite l'API del file System in questi siti|
|[FileSystemWriteAskForUrls](#filesystemwriteaskforurls)|Consenti accesso in scrittura ai file e alle directory in questi siti|
|[FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls)|Blocca accesso in scrittura a file e directory in questi siti|
|[ImagesAllowedForUrls](#imagesallowedforurls)|Consenti le immagini per questi siti|
|[ImagesBlockedForUrls](#imagesblockedforurls)|Blocca le immagini per siti specifici|
|[InsecureContentAllowedForUrls](#insecurecontentallowedforurls)|Consenti contenuto non sicuro nei siti specificati|
|[InsecureContentBlockedForUrls](#insecurecontentblockedforurls)|Blocca contenuto non sicuro nei siti specificati|
|[JavaScriptAllowedForUrls](#javascriptallowedforurls)|Consenti JavaScript per siti specifici|
|[JavaScriptBlockedForUrls](#javascriptblockedforurls)|Blocca JavaScript per siti specifici|
|[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)|Abilita impostazione predefinita del comportamento dei cookie SameSite|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist)|Ripristina il comportamento SameSite legacy per i cookie nei siti specificati|
|[NotificationsAllowedForUrls](#notificationsallowedforurls)|Consenti le notifiche per siti specifici|
|[NotificationsBlockedForUrls](#notificationsblockedforurls)|Blocca le notifiche per siti specifici|
|[PluginsAllowedForUrls](#pluginsallowedforurls)|Consenti il plug-in Adobe Flash per siti specifici|
|[PluginsBlockedForUrls](#pluginsblockedforurls)|Blocca il plug-in Adobe Flash per siti specifici|
|[PopupsAllowedForUrls](#popupsallowedforurls)|Consenti le finestre popup per siti specifici|
|[PopupsBlockedForUrls](#popupsblockedforurls)|Blocca le finestre popup per siti specifici|
|[RegisteredProtocolHandlers](#registeredprotocolhandlers)|Registra gestori di protocollo|
|[SpotlightExperiencesAndRecommendationsEnabled](#spotlightexperiencesandrecommendationsenabled)|Scegli se gli utenti possono ricevere testo e immagini di sfondo personalizzati, suggerimenti, notifiche
e suggerimenti per i servizi Microsoft|
|[WebUsbAllowDevicesForUrls](#webusballowdevicesforurls)|Concedi l'accesso a siti specifici per la connessione a dispositivi USB specifici|
|[WebUsbAskForUrls](#webusbaskforurls)|Consenti WebUSB per siti specifici|
|[WebUsbBlockedForUrls](#webusbblockedforurls)|Blocca WebUSB per siti specifici|
### [*Impostazioni di Application Guard*](#impostazioni-di-application-guard-policies)
|Nome criteri|Sottotitolo|
|-|-|
|[ApplicationGuardContainerProxy](#applicationguardcontainerproxy)|Proxy contenitore Application Guard|
### [*Messaggi nativi*](#messaggi-nativi-policies)
|Nome criteri|Sottotitolo|
|-|-|
|[NativeMessagingAllowlist](#nativemessagingallowlist)|Controlla quali host di messaggistica nativa possono essere utilizzati dagli utenti|
|[NativeMessagingBlocklist](#nativemessagingblocklist)|Configura l'elenco degli host di messaggistica nativa bloccati|
|[NativeMessagingUserLevelHosts](#nativemessaginguserlevelhosts)|Consenti host di messaggistica nativa a livello di utente (installati senza autorizzazioni di amministratore)|
### [*Protezione e gestione password*](#protezione-e-gestione-password-policies)
|Nome criteri|Sottotitolo|
|-|-|
|[PasswordManagerEnabled](#passwordmanagerenabled)|Abilita salvataggio password nella gestione delle password|
|[PasswordMonitorAllowed](#passwordmonitorallowed)|Consenti l’invio di avvisi agli utenti se le password non sono più sicure|
|[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)|Configura l'URL di modifica password|
|[PasswordProtectionLoginURLs](#passwordprotectionloginurls)|Configura l'elenco degli URL di accesso aziendali in cui il servizio di protezione password deve acquisire gli hash con salting di una password|
|[PasswordProtectionWarningTrigger](#passwordprotectionwarningtrigger)|Configura il trigger di avviso di protezione password|
### [*Provider di ricerca predefinito*](#provider-di-ricerca-predefinito-policies)
|Nome criteri|Sottotitolo|
|-|-|
|[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)|Abilita il provider di ricerca predefinito|
|[DefaultSearchProviderEncodings](#defaultsearchproviderencodings)|Codifiche del provider di ricerca predefinito|
|[DefaultSearchProviderImageURL](#defaultsearchproviderimageurl)|Specifica la funzionalità di ricerca per immagini per il provider di ricerca predefinito|
|[DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams)|Parametri per l'URL di un'immagine che utilizza POST|
|[DefaultSearchProviderKeyword](#defaultsearchproviderkeyword)|Parola chiave del provider di ricerca predefinito|
|[DefaultSearchProviderName](#defaultsearchprovidername)|Nome del provider di ricerca predefinito|
|[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)|URL di ricerca del provider di ricerca predefinito|
|[DefaultSearchProviderSuggestURL](#defaultsearchprovidersuggesturl)|URL del provider di ricerca predefinito per i suggerimenti|
|[NewTabPageSearchBox](#newtabpagesearchbox)|Configura l'esperienza della casella di ricerca della nuova scheda|
### [*Server proxy*](#server-proxy-policies)
|Nome criteri|Sottotitolo|
|-|-|
|[ProxyBypassList](#proxybypasslist)|Configura le regole di bypass proxy|
|[ProxyMode](#proxymode)|Configura le impostazioni del server proxy|
|[ProxyPacUrl](#proxypacurl)|Imposta l'URL del file .pac del proxy|
|[ProxyServer](#proxyserver)|Configura l'indirizzo o l'URL del server proxy|
|[ProxySettings](#proxysettings)|Impostazioni proxy|
### [*Stampa*](#stampa-policies)
|Nome criteri|Sottotitolo|
|-|-|
|[DefaultPrinterSelection](#defaultprinterselection)|Regole di selezione della stampante predefinita|
|[PrintHeaderFooter](#printheaderfooter)|Stampa intestazioni e piè di pagina|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|Imposta stampante predefinita del sistema come stampante predefinita|
|[PrintingEnabled](#printingenabled)|Abilita stampa|
|[PrintingPaperSizeDefault](#printingpapersizedefault)|Dimensioni predefinite pagina di stampa|
|[UseSystemPrintDialog](#usesystemprintdialog)|Stampa utilizzando la finestra di dialogo Stampa del sistema|
### [*Additional*](#additional-policies)
|Nome criteri|Sottotitolo|
|-|-|
|[AddressBarMicrosoftSearchInBingProviderEnabled](#addressbarmicrosoftsearchinbingproviderenabled)|Abilita i suggerimenti di Microsoft Search in Bing nella barra degli indirizzi|
|[AdsSettingForIntrusiveAdsSites](#adssettingforintrusiveadssites)|Impostazione degli annunci per i siti con annunci intrusivi|
|[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory)|Abilita eliminazione cronologia del browser e download|
|[AllowFileSelectionDialogs](#allowfileselectiondialogs)|Consenti le finestre di dialogo di selezione file|
|[AllowPopupsDuringPageUnload](#allowpopupsduringpageunload)|Consente a una pagina di visualizzare i popup durante lo scaricamento|
|[AllowSurfGame](#allowsurfgame)|Consenti gioco di surf|
|[AllowSyncXHRInPageDismissal](#allowsyncxhrinpagedismissal)|Consenti alle pagine di inviare richieste XHR sincrone durante la chiusura della pagina (deprecato)|
|[AllowTokenBindingForUrls](#allowtokenbindingforurls)|Configurare l'elenco dei siti con cui Microsoft Edge tenterà di stabilire un binding di token.|
|[AllowTrackingForUrls](#allowtrackingforurls)|Configura le eccezioni di prevenzione del monitoraggio per siti specifici|
|[AlternateErrorPagesEnabled](#alternateerrorpagesenabled)|Suggerisci pagine simili quando non è possibile trovare una pagina|
|[AlwaysOpenPdfExternally](#alwaysopenpdfexternally)|Apri sempre i file PDF esternamente|
|[AmbientAuthenticationInPrivateModesEnabled](#ambientauthenticationinprivatemodesenabled)|Abilita autenticazione ambiente per i profili InPrivate e guest|
|[AppCacheForceEnabled](#appcacheforceenabled)|Consente di riabilitare la funzionalità AppCache, anche se è disattivata per impostazione predefinita|
|[ApplicationLocaleValue](#applicationlocalevalue)|Specifica le impostazioni locali dell'applicazione|
|[AudioCaptureAllowed](#audiocaptureallowed)|Consenti o blocca l'acquisizione audio|
|[AudioCaptureAllowedUrls](#audiocaptureallowedurls)|Siti che possono accedere ai dispositivi di acquisizione audio senza richiedere l'autorizzazione|
|[AudioSandboxEnabled](#audiosandboxenabled)|Consenti l'esecuzione della sandbox audio|
|[AutoImportAtFirstRun](#autoimportatfirstrun)|Importa automaticamente i dati e le impostazioni di un altro browser alla prima esecuzione|
|[AutoLaunchProtocolsFromOrigins](#autolaunchprotocolsfromorigins)|Definisci un elenco di protocolli in grado di avviare un'applicazione esterna dalle origini elencate senza richiedere all'utente|
|[AutoOpenAllowedForURLs](#autoopenallowedforurls)|URL in cui è possibile applicare AutoOpenFileTypes|
|[AutoOpenFileTypes](#autoopenfiletypes)|Elenco dei tipi di file che dovrebbero aprirsi automaticamente al download|
|[AutofillAddressEnabled](#autofilladdressenabled)|Abilita riempimento automatico per gli indirizzi|
|[AutofillCreditCardEnabled](#autofillcreditcardenabled)|Abilita riempimento automatico per le carte di credito|
|[AutoplayAllowed](#autoplayallowed)|Consenti AutoPlay di supporti per siti Web|
|[BackgroundModeEnabled](#backgroundmodeenabled)|Continua a eseguire le app in background dopo che Microsoft Edge viene chiuso|
|[BackgroundTemplateListUpdatesEnabled](#backgroundtemplatelistupdatesenabled)|Abilita gli aggiornamenti in background all'elenco di modelli disponibili per le raccolte e le altre funzionalità che utilizzano i modelli.|
|[BingAdsSuppression](#bingadssuppression)|Blocca tutti gli annunci nei risultati della ricerca con Bing|
|[BlockThirdPartyCookies](#blockthirdpartycookies)|Blocca i cookie di terze parti|
|[BrowserAddProfileEnabled](#browseraddprofileenabled)|Abilita la creazione del profilo dal menu a comparsa Identità o dalla pagina Impostazioni|
|[BrowserGuestModeEnabled](#browserguestmodeenabled)|Abilita modalità guest|
|[BrowserNetworkTimeQueriesEnabled](#browsernetworktimequeriesenabled)|Consenti le query a un servizio di ora di rete del browser|
|[BrowserSignin](#browsersignin)|Impostazioni di accesso del browser|
|[BuiltInDnsClientEnabled](#builtindnsclientenabled)|Utilizza il client DNS predefinito|
|[BuiltinCertificateVerifierEnabled](#builtincertificateverifierenabled)|Determina se il certificato predefinito Verifier verrà utilizzato per verificare i certificati del server (deprecato)|
|[CertificateTransparencyEnforcementDisabledForCas](#certificatetransparencyenforcementdisabledforcas)|Disabilita l'applicazione della trasparenza dei certificati per un elenco di hash subjectPublicKeyInfo|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](#certificatetransparencyenforcementdisabledforlegacycas)|Disabilita l'applicazione della trasparenza dei certificati per un elenco di autorità di certificazione legacy|
|[CertificateTransparencyEnforcementDisabledForUrls](#certificatetransparencyenforcementdisabledforurls)|Disabilita l'applicazione della trasparenza dei certificati per URL specifici|
|[ClearBrowsingDataOnExit](#clearbrowsingdataonexit)|Cancella i dati di navigazione quando Microsoft Edge viene chiuso|
|[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)|Cancella immagini e file memorizzati nella cache quando Microsoft Edge viene chiuso|
|[ClickOnceEnabled](#clickonceenabled)|Consenti agli utenti di aprire file tramite il protocollo ClickOnce|
|[CollectionsServicesAndExportsBlockList](#collectionsservicesandexportsblocklist)|Blocca l'accesso a un elenco di servizi specifici ed esporta destinazioni in Raccolte|
|[CommandLineFlagSecurityWarningsEnabled](#commandlineflagsecuritywarningsenabled)|Abilita gli avvisi di sicurezza per i flag della riga di comando|
|[ComponentUpdatesEnabled](#componentupdatesenabled)|Abilita gli aggiornamenti dei componenti in Microsoft Edge|
|[ConfigureDoNotTrack](#configuredonottrack)|Configura Non tenere traccia|
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|Configura l'accesso automatico con un account di dominio di Active Directory quando non è disponibile un account di dominio di Azure AD|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|Configura la sintesi vocale online|
|[ConfigureShare](#configureshare)|Configura l'esperienza di condivisione|
|[CustomHelpLink](#customhelplink)|Specifica il collegamento della Guida personalizzato|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|Controlli intercettazione DNS abilitati|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|Imposta Microsoft Edge come browser predefinito|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|Consenti accesso predefinito al menu di scelta rapida del provider di ricerca|
|[DefaultSensorsSetting](#defaultsensorssetting)|Impostazione predefinite dei sensori|
|[DefaultSerialGuardSetting](#defaultserialguardsetting)|Controlla l'uso dell'API seriale|
|[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)|È necessario che l'elenco dei siti in modalità Enterprise sia disponibile prima dell'esplorazione nella scheda|
|[DeleteDataOnMigration](#deletedataonmigration)|Elimina i dati del browser datati durante la migrazione|
|[DeveloperToolsAvailability](#developertoolsavailability)|Controlla dove possono essere utilizzati gli strumenti di sviluppo|
|[DiagnosticData](#diagnosticdata)|Invia dati di diagnostica obbligatori e facoltativi sull’uso del browser|
|[DirectInvokeEnabled](#directinvokeenabled)|Consenti agli utenti di aprire file tramite il protocollo DirectInvoke|
|[Disable3DAPIs](#disable3dapis)|Disabilita il supporto per le API di grafica 3D|
|[DisableScreenshots](#disablescreenshots)|Disabilita l'acquisizione di screenshot|
|[DiskCacheDir](#diskcachedir)|Imposta directory cache disco|
|[DiskCacheSize](#diskcachesize)|Imposta le dimensioni della cache disco, in byte|
|[DnsOverHttpsMode](#dnsoverhttpsmode)|Controlla la modalità di DNS su HTTPS|
|[DnsOverHttpsTemplates](#dnsoverhttpstemplates)|Specificare il modello URI del resolver DNS-over-HTTPS desiderato|
|[DownloadDirectory](#downloaddirectory)|Imposta directory di download|
|[DownloadRestrictions](#downloadrestrictions)|Consenti le restrizioni di download|
|[EdgeCollectionsEnabled](#edgecollectionsenabled)|Abilita la funzionalità Raccolte|
|[EditFavoritesEnabled](#editfavoritesenabled)|Consente agli utenti di modificare i Preferiti|
|[EnableDeprecatedWebPlatformFeatures](#enabledeprecatedwebplatformfeatures)|Riattiva le funzionalità della piattaforma Web deprecate per un periodo di tempo limitato|
|[EnableDomainActionsDownload](#enabledomainactionsdownload)|Abilita download azioni di dominio da Microsoft (obsoleto)|
|[EnableOnlineRevocationChecks](#enableonlinerevocationchecks)|Abilita i controlli CRL/OCSP online|
|[EnableSha1ForLocalAnchors](#enablesha1forlocalanchors)|Consenti certificati firmati con SHA-1 quando vengono emessi da Trust Anchor locali (deprecato)|
|[EnterpriseHardwarePlatformAPIEnabled](#enterprisehardwareplatformapienabled)|Consenti alle estensioni gestite di utilizzare l'API della piattaforma hardware aziendale|
|[EnterpriseModeSiteListManagerAllowed](#enterprisemodesitelistmanagerallowed)|Consenti l'accesso allo strumento Enterprise Mode Site List Manager|
|[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](#exemptdomainfiletypepairsfromfiletypedownloadwarnings)|Disabilita il download degli avvisi basati sull'estensione del tipo di file per i tipi di file specificati nei domini|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|Controlla le comunicazioni con il servizio di sperimentazione e configurazione|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox)|Mostra una casella di controllo "Sempre aperto" nella finestra di dialogo del protocollo esterno.|
|[FamilySafetySettingsEnabled](#familysafetysettingsenabled)|Consenti agli utenti di configurare Family Safety|
|[FavoritesBarEnabled](#favoritesbarenabled)|Abilita barra Preferiti|
|[ForceBingSafeSearch](#forcebingsafesearch)|Applica Ricerca sicura Bing|
|[ForceCertificatePromptsOnMultipleMatches](#forcecertificatepromptsonmultiplematches)|Configura se Microsoft Edge deve selezionare automaticamente un certificato quando esistono più corrispondenze di certificati per un sito configurato con "AutoSelectCertificateForUrls"|
|[ForceEphemeralProfiles](#forceephemeralprofiles)|Abilita l'uso di profili temporanei|
|[ForceGoogleSafeSearch](#forcegooglesafesearch)|Applica Google SafeSearch|
|[ForceLegacyDefaultReferrerPolicy](#forcelegacydefaultreferrerpolicy)|Utilizza un criterio referrer predefinito di no-referrer-when-downgrade (deprecato)|
|[ForceNetworkInProcess](#forcenetworkinprocess)|Forza codice di rete da eseguire nel processo del browser (obsoleto)|
|[ForceSync](#forcesync)|Forza la sincronizzazione dei dati del browser e non mostrare la richiesta di consenso alla sincronizzazione|
|[ForceYouTubeRestrict](#forceyoutuberestrict)|Forza modalità con restrizioni YouTube minima|
|[FullscreenAllowed](#fullscreenallowed)|Consenti la modalità a schermo intero|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|Abilita cache di autenticazione HTTP con ambito globale|
|[GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar)|Forza l'esplorazione diretta del sito Intranet anziché cercare le singole parole immesse nella barra degli indirizzi|
|[HSTSPolicyBypassList](#hstspolicybypasslist)|Configura l'elenco dei nomi che ignoreranno il controllo dei criteri HSTS|
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|Utilizza l'accelerazione hardware se disponibile|
|[HideFirstRunExperience](#hidefirstrunexperience)|Nascondi la First Run Experience e la schermata iniziale|
|[ImportAutofillFormData](#importautofillformdata)|Consenti l'importazione dei dati del modulo di riempimento automatico|
|[ImportBrowserSettings](#importbrowsersettings)|Consenti l'importazione delle impostazioni del browser|
|[ImportCookies](#importcookies)|Consenti l'importazione dei cookie|
|[ImportExtensions](#importextensions)|Consenti l'importazione delle estensioni|
|[ImportFavorites](#importfavorites)|Consenti l'importazione dei preferiti|
|[ImportHistory](#importhistory)|Consenti l'importazione della cronologia esplorazioni|
|[ImportHomepage](#importhomepage)|Consenti l'importazione delle impostazioni della home page|
|[ImportOpenTabs](#importopentabs)|Consenti l'importazione delle schede aperte|
|[ImportPaymentInfo](#importpaymentinfo)|Consenti importazione delle info di pagamento|
|[ImportSavedPasswords](#importsavedpasswords)|Consenti l'importazione delle password salvate|
|[ImportSearchEngine](#importsearchengine)|Consenti l'importazione delle impostazioni del motore di ricerca|
|[ImportShortcuts](#importshortcuts)|Consenti l'importazione dei collegamenti|
|[InPrivateModeAvailability](#inprivatemodeavailability)|Configura la disponibilità della modalità InPrivate|
|[InsecureFormsWarningsEnabled](#insecureformswarningsenabled)|Abilita avvisi per moduli non sicuri|
|[IntensiveWakeUpThrottlingEnabled](#intensivewakeupthrottlingenabled)|Controlla la funzionalità IntensiveWakeUpThrottling|
|[InternetExplorerIntegrationEnhancedHangDetection](#internetexplorerintegrationenhancedhangdetection)|Configura il rilevamento avanzato di blocchi per la modalità di Internet Explorer|
|[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)|Configura l'integrazione di Internet Explorer|
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|Configura l'elenco dei siti in modalità Enterprise|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|Specifica il comportamento della modalità di spostamento dei siti non configurati "nella pagina" quando avviati dalle pagine in modalità Internet Explorer|
|[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed)|Consenti il test della modalità Internet Explorer|
|[IsolateOrigins](#isolateorigins)|Abilita l'isolamento del sito per origini specifiche|
|[LocalProvidersEnabled](#localprovidersenabled)|Consenti suggerimenti dei provider locali|
|[ManagedFavorites](#managedfavorites)|Configura i preferiti|
|[ManagedSearchEngines](#managedsearchengines)|Gestisci motori di ricerca|
|[MaxConnectionsPerProxy](#maxconnectionsperproxy)|Numero massimo di connessioni simultanee al server proxy|
|[MediaRouterCastAllowAllIPs](#mediaroutercastallowallips)|Consenti a Google Cast di connettersi ai dispositivi Cast su tutti gli indirizzi IP|
|[MetricsReportingEnabled](#metricsreportingenabled)|Abilita creazione di report sui dati di utilizzo e relativi all'arresto anomalo del sistema (deprecato)|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|Attiva occlusione finestra nativa|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|Imposta un timeout per ritardare l'esplorazione della scheda per l'elenco dei siti in modalità Enterprise.|
|[NetworkPredictionOptions](#networkpredictionoptions)|Abilita completamento rete|
|[NonRemovableProfileEnabled](#nonremovableprofileenabled)|Configura se effettuare automaticamente l’accesso del profilo predefinito dell’utente con l’account aziendale o dell'istituto di istruzione|
|[OverrideSecurityRestrictionsOnInsecureOrigin](#overridesecurityrestrictionsoninsecureorigin)|Controlla dove vengono applicate le restrizioni di sicurezza alle origini non sicure|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|Consenti ai siti Web di richiedere metodi di pagamento disponibili|
|[PersonalizationReportingEnabled](#personalizationreportingenabled)|Consenti personalizzazione di annunci, ricerca e notizie inviando la cronologia esplorazioni a Microsoft|
|[PinningWizardAllowed](#pinningwizardallowed)|Procedura guidata Aggiungi a barra delle applicazioni|
|[ProactiveAuthEnabled](#proactiveauthenabled)|Abilita l'autenticazione proattiva|
|[PromotionalTabsEnabled](#promotionaltabsenabled)|Abilitare il contenuto promozionale della scheda completa|
|[PromptForDownloadLocation](#promptfordownloadlocation)|Richiedi la posizione in cui salvare i file scaricati|
|[QuicAllowed](#quicallowed)|Consenti il protocollo QUIC|
|[RelaunchNotification](#relaunchnotification)|Notifica a un utente che è consigliato o obbligatorio eseguire un riavvio del browser per gli aggiornamenti in sospeso|
|[RelaunchNotificationPeriod](#relaunchnotificationperiod)|Imposta il periodo di tempo per le notifiche di aggiornamento|
|[RendererCodeIntegrityEnabled](#renderercodeintegrityenabled)|Abilita l'integrità del codice di rendering|
|[RequireOnlineRevocationChecksForLocalAnchors](#requireonlinerevocationchecksforlocalanchors)|Specifica se i controlli CRL/OCSP online sono necessari per i trust anchor locali|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|Abilita la risoluzione degli errori di navigazione tramite un servizio Web|
|[RestrictSigninToPattern](#restrictsignintopattern)|Limita gli account che possono essere utilizzati come account principali di Microsoft Edge|
|[RoamingProfileLocation](#roamingprofilelocation)|Imposta la directory del profilo mobile|
|[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)|Abilita l'utilizzo di copie roaming per i dati del profilo di Microsoft Edge|
|[RunAllFlashInAllowMode](#runallflashinallowmode)|Estendi l'impostazione dei contenuti Adobe Flash a tutti i contenuti|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|Consenti agli utenti di continuare dalla pagina di avviso HTTPS|
|[SSLVersionMin](#sslversionmin)|Versione TLS minima abilitata|
|[SaveCookiesOnExit](#savecookiesonexit)|Salvare i cookie alla chiusura di Microsoft Edge|
|[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)|Disabilita il salvataggio della cronologia del browser|
|[ScreenCaptureAllowed](#screencaptureallowed)|Consentire o negare l'acquisizione dello schermo|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|Abilita scorrimento verso il testo specificato nei frammenti di URL|
|[SearchSuggestEnabled](#searchsuggestenabled)|Abilita suggerimenti di ricerca|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|Siti Web o i domini che non richiedono l'autorizzazione per utilizzare l'attestazione per la chiave di sicurezza diretta|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|Invia tutti i siti Intranet a Internet Explorer|
|[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)|Invia informazioni sul sito per migliorare i servizi Microsoft (deprecato)|
|[SensorsAllowedForUrls](#sensorsallowedforurls)|Consenti l'accesso ai sensori su siti specifici|
|[SensorsBlockedForUrls](#sensorsblockedforurls)|Blocca l'accesso ai sensori su siti specifici|
|[SerialAskForUrls](#serialaskforurls)|Consenti l'API Serial su siti specifici|
|[SerialBlockedForUrls](#serialblockedforurls)|Blocca l'API Serial su siti specifici|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|Mostra collegamento Microsoft Office sulla barra Preferiti|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|Abilita supporto Signed HTTP Exchange (SXG)|
|[SitePerProcess](#siteperprocess)|Abilita l'isolamento per ogni sito|
|[SpellcheckEnabled](#spellcheckenabled)|Abilita controllo ortografia|
|[SpellcheckLanguage](#spellchecklanguage)|Attiva lingua specifica per controllo ortografia|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|Forza disattivazione lingue per controllo ortografico|
|[StricterMixedContentTreatmentEnabled](#strictermixedcontenttreatmentenabled)|Abilita trattamento più rigoroso per il contenuto misto (deprecato)|
|[SuppressUnsupportedOSWarning](#suppressunsupportedoswarning)|Elimina l'avviso di sistema operativo non supportato|
|[SyncDisabled](#syncdisabled)|Disabilita la sincronizzazione dei dati mediante i servizi di sincronizzazione Microsoft|
|[SyncTypesListDisabled](#synctypeslistdisabled)|Configura l'elenco di caratteri esclusi dalla sincronizzazione|
|[TLS13HardeningForLocalAnchorsEnabled](#tls13hardeningforlocalanchorsenabled)|Abilita una funzionalità di sicurezza TLS 1.3 per i trust anchor locali. (obsoleto)|
|[TLSCipherSuiteDenyList](#tlsciphersuitedenylist)|Specifica i pacchetti di crittografia TLS da disabilitare|
|[TabFreezingEnabled](#tabfreezingenabled)|Consenti blocco delle schede in background|
|[TaskManagerEndProcessEnabled](#taskmanagerendprocessenabled)|Abilita l'interruzione dei processi in Gestione attività del browser|
|[TotalMemoryLimitMb](#totalmemorylimitmb)|Imposta in megabyte il limite di memoria che può essere utilizzata da un'unica istanza di Microsoft Edge.|
|[TrackingPrevention](#trackingprevention)|Blocca il rilevamento dell'attività di esplorazione Web degli utenti|
|[TranslateEnabled](#translateenabled)|Abilita traduzione|
|[URLAllowlist](#urlallowlist)|Definisci un elenco di URL consentiti|
|[URLBlocklist](#urlblocklist)|Blocca l'accesso a un elenco di URL|
|[UserAgentClientHintsEnabled](#useragentclienthintsenabled)|Abilita la funzionalità User-Agent Client Hints (deprecato)|
|[UserDataDir](#userdatadir)|Imposta la directory dei dati dell'utente|
|[UserDataSnapshotRetentionLimit](#userdatasnapshotretentionlimit)|Limita il numero di snapshot dei dati utente conservati per l'utilizzo in caso di rollback di emergenza|
|[UserFeedbackAllowed](#userfeedbackallowed)|Consenti feedback utente|
|[VideoCaptureAllowed](#videocaptureallowed)|Consenti o blocca l'acquisizione video|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|Siti che possono accedere ai dispositivi di acquisizione video senza richiedere l'autorizzazione|
|[WPADQuickCheckEnabled](#wpadquickcheckenabled)|Imposta ottimizzazione WPAD|
|[WebAppInstallForceList](#webappinstallforcelist)|Configura l'elenco delle app Web con installazione forzata|
|[WebComponentsV0Enabled](#webcomponentsv0enabled)|Riabilita l'API dei componenti Web v0 fino alla versione M84 (obsoleto)|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|Consenti a WebDriver di sostituire i criteri non compatibili (obsoleto)|
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|Gestisci l'esposizione degli indirizzi IP locali da WebRTC|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|Limita l'esposizione dell'indirizzo IP locale da WebRTC|
|[WebRtcUdpPortRange](#webrtcudpportrange)|Limita l'intervallo di porte UDP locali utilizzato da WebRTC|
|[WinHttpProxyResolverEnabled](#winhttpproxyresolverenabled)|Usa resolver proxy di Windows (deprecato)|




  ## Autenticazione HTTP policies

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AllowCrossOriginAuthPrompt
  #### Consenti le richieste di autenticazione di base HTTP tra le origini
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Controlla se i contenuti secondari di terze parti in una pagina possono aprire una finestra di dialogo di autenticazione di base HTTP.

In genere, questi criteri sono disabilitati per difesa dal phishing. Se non configuri questi criteri, sono disabilitati e i contenuti secondari di terze parti non possono aprire una finestra di dialogo di autenticazione di base HTTP.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AllowCrossOriginAuthPrompt
  - Nome GP: Consenti le richieste di autenticazione di base HTTP tra le origini
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Autenticazione HTTP
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AllowCrossOriginAuthPrompt
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AllowCrossOriginAuthPrompt
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AuthNegotiateDelegateAllowlist
  #### Specifica un elenco di server a cui Microsoft Edge può delegare le credenziali dell'utente
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Configura l'elenco dei server a cui è possibile delegare Microsoft Edge.

Separa più nomi di server con una virgola. I caratteri jolly (*) sono consentiti.

Se non configuri questi criteri Microsoft Edge non delega le credenziali dell'utente anche se un server viene rilevato come Intranet.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AuthNegotiateDelegateAllowlist
  - Nome GP: Specifica un elenco di server a cui Microsoft Edge può delegare le credenziali dell'utente
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Autenticazione HTTP
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AuthNegotiateDelegateAllowlist
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"contoso.com"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AuthNegotiateDelegateAllowlist
  - Valore di esempio:
``` xml
<string>contoso.com</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AuthSchemes
  #### Schemi di autenticazione supportati
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica quali schemi di autenticazione HTTP sono supportati.

Puoi configurare i criteri utilizzando questi valori: 'basic', 'digest', 'ntlm' e 'negotiate'. Separa più valori con virgole.

Se non configuri questi criteri, verranno utilizzati tutti gli schemi.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AuthSchemes
  - Nome GP: Schemi di autenticazione supportati
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Autenticazione HTTP
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AuthSchemes
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"basic,digest,ntlm,negotiate"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AuthSchemes
  - Valore di esempio:
``` xml
<string>basic,digest,ntlm,negotiate</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AuthServerAllowlist
  #### Configura l'elenco dei server di autenticazione consentiti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica quali server abilitare per l'autenticazione integrata. L'autenticazione integrata viene abilitata solo quando Microsoft Edge riceve una richiesta di autenticazione da un proxy o da un server presente in questo elenco.

Separa più nomi server con le virgole. Sono consentiti i caratteri jolly (*).

Se non configuri questi criteri, Microsoft Edge tenta di rilevare se un server si trova nella rete Intranet: solo allora risponde alle richieste di autenticazione integrata di Windows. Se il server è su Internet, le richieste di autenticazione integrata di Windows vengono ignorate da Microsoft Edge.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AuthServerAllowlist
  - Nome GP: Configura l'elenco dei server di autenticazione consentiti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Autenticazione HTTP
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AuthServerAllowlist
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"*contoso.com,contoso.com"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AuthServerAllowlist
  - Valore di esempio:
``` xml
<string>*contoso.com,contoso.com</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DisableAuthNegotiateCnameLookup
  #### Disabilita la ricerca CNAME durante la negoziazione dell'autenticazione Kerberos
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Determina se l'SPN Kerberos generato è basato sul nome canonico DNS (CNAME) o sul nome originale immesso.

Se abiliti questi criteri, la ricerca CNAME viene ignorata e il nome del server verrà utilizzato (come immesso).

Se disabiliti o non configuri questi criteri, il nome canonico del server verrà utilizzato e sarà determinato mediante una ricerca CNAME.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DisableAuthNegotiateCnameLookup
  - Nome GP: Disabilita la ricerca CNAME durante la negoziazione dell'autenticazione Kerberos
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Autenticazione HTTP
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DisableAuthNegotiateCnameLookup
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DisableAuthNegotiateCnameLookup
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### EnableAuthNegotiatePort
  #### Includi la porta non standard in SPN Kerberos
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica se l'SPN Kerberos generato deve includere una porta non standard.

Se abiliti questi criteri e un utente include una porta non standard (una porta diversa da 80 o 443) in un URL, tale porta è inclusa nell'SPN Kerberos generato.

Se non configuri o disabiliti questi criteri, l'SPN Kerberos generato non includerà una porta in ogni caso.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: EnableAuthNegotiatePort
  - Nome GP: Includi la porta non standard in SPN Kerberos
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Autenticazione HTTP
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: EnableAuthNegotiatePort
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: EnableAuthNegotiatePort
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NtlmV2Enabled
  #### Controlla se è abilitata l'autenticazione NTLMv2
  
  
  #### Versioni supportate:
  - Su macOS dal 77 o successiva

  #### Descrizione
  Controlla se NTLMv2 è abilitato.

Tutte le versioni recenti dei server Samba e Windows supportano NTLMv2. Disattiva NTLMv2 solo per risolvere i problemi di compatibilità con le versioni precedenti in quanto riduce la sicurezza dell'autenticazione.

Se non configuri questi criteri, NTLMv2 è abilitato per impostazione predefinita.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  

  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: NtlmV2Enabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ## Avvio&comma; pagina iniziale e nuova scheda policies

  [Torna all'inizio](#microsoft-edge---criteri)

  ### HomepageIsNewTabPage
  #### Imposta la nuova scheda come home page
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Configura la home page predefinita in Microsoft Edge. Puoi impostare come home page un URL specificato o una nuova scheda.

Se abiliti questo criterio, la nuova scheda verrà sempre utilizzata per la home page e la posizione dell'URL della home page verrà ignorata.

Se disabiliti questo criterio, la home page dell'utente non potrà essere la pagina della nuova scheda, a meno che l'URL non sia impostato su "edge://newtab".

Se non configuri questo criterio, gli utenti potranno scegliere se la home page sarà la nuova scheda.

Questo criterio è disponibile solo per le istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: HomepageIsNewTabPage
  - Nome GP: Imposta la nuova scheda come home page
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Avvio, pagina iniziale e nuova scheda
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Avvio, pagina iniziale e nuova scheda
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: HomepageIsNewTabPage
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: HomepageIsNewTabPage
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### HomepageLocation
  #### Configura l'URL della home page
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Configura l'URL predefinito della home page in Microsoft Edge.

La home page è la pagina che viene aperta dal pulsante Home. Le pagine che vengono aperte all'avvio sono controllate dai criteri [RestoreOnStartup](#restoreonstartup).

Puoi impostare un URL qui oppure impostare la home page in modo che si apra una nuova scheda. Se scegli di aprire una nuova scheda, il criterio non avrà effetto.

Se abiliti questo criterio, gli utenti non potranno modificare l'URL della home page, ma potranno scegliere di utilizzare una nuova scheda come home page.

Se disabiliti o non configuri questo criterio, gli utenti potranno scegliere la propria home page, a condizione che il criterio [HomepageIsNewTabPage](#homepageisnewtabpage) non sia abilitato.

Questo criterio è disponibile solo per le istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: HomepageLocation
  - Nome GP: Configura l'URL della home page
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Avvio, pagina iniziale e nuova scheda
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Avvio, pagina iniziale e nuova scheda
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: HomepageLocation
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"https://www.contoso.com"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: HomepageLocation
  - Valore di esempio:
``` xml
<string>https://www.contoso.com</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NewTabPageAllowedBackgroundTypes
  #### Configura i tipi di sfondo consentiti per il nuovo layout di pagina della nuova scheda
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Puoi configurare i tipi di immagine di sfondo consentiti nel layout di pagina nuova scheda in Microsoft Edge.

Se non configuri questo criterio, sono abilitati tutti i tipi di immagine di sfondo.

Mappatura opzioni criteri:

* DisableImageOfTheDay (1) = Disabilita immagini di sfondo giornaliere

* DisableCustomImage (2) = Disabilita immagini di sfondo personalizzate

* DisableAll (3) = Disabilita tutti i tipi di immagine di sfondo

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: NewTabPageAllowedBackgroundTypes
  - Nome GP: Configura i tipi di sfondo consentiti per il nuovo layout di pagina della nuova scheda
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Avvio, pagina iniziale e nuova scheda
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: NewTabPageAllowedBackgroundTypes
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: NewTabPageAllowedBackgroundTypes
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NewTabPageCompanyLogo
  #### Imposta logo aziendale nuova scheda (obsoleto)
  
  >OBSOLETO: questo criterio è obsoleto e non funziona nelle versioni di Microsoft Edge successive alla versione 85.
  #### Versioni supportate:
  - Su Windows e macOS dal 79, fino al 85

  #### Descrizione
  Questo criterio non ha funzionato come previsto a causa di modifiche apportate ai requisiti operativi. Di conseguenza è obsoleto e non deve essere usato .

     Specifica il logo aziendale da utilizzare nella nuova scheda in Microsoft Edge.

     I criteri devono essere configurati come stringa che esprime il logo o i loghi in formato JSON. Ad esempio: { "default_logo": { "url": "https://www.contoso.com/logo.png", "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29" }, "light_logo": { "url": "https://www.contoso.com/light_logo.png", "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737" } }

     Per configurare questi criteri, specifica l'URL da cui Microsoft Edge può scaricare il logo e l'hash di crittografia (Agente integrità sistema-256) utilizzato per verificare l'integrità del download. Il logo deve essere in formato PNG o SVG e le dimensioni del file non devono superare i 16 MB. Il logo viene scaricato e memorizzato nella cache e verrà riscaricato ogni volta che l'URL o l'hash viene modificato. L'URL deve essere accessibile senza alcuna autenticazione.        .

     Il valore "default_logo" è obbligatorio e viene utilizzato quando non c'è un'immagine di sfondo. Se fornito, "light_logo" viene utilizzato quando la nuova scheda dell'utente ha un'immagine di sfondo. È consigliabile utilizzare un logo orizzontale con uno sfondo trasparente allineato a sinistra e centrato verticalmente. Il logo deve avere un'altezza minima di 32 pixel e proporzioni da 1:1 a 4:1. "default_logo" deve avere un contrasto corretto rispetto a uno sfondo bianco/nero mentre "light_logo" deve avere un contrasto corretto rispetto all'immagine di sfondo.

Se abiliti questi criteri, Microsoft Edgescarica e mostra i logo specificati nella nuova scheda. Gli utenti non possono ignorare o nascondere il logo

Se disabiliti o non configuri questi criteri, Microsoft Edgenon viene visualizzato alcun logo aziendale o Microsoft nella nuova scheda.

Per informazioni sulla determinazione dell'hash Agente integrità sistema-256, vedi https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/get-filehash.e/microsoft.powershell.utility/get-filehash.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Dizionario

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: NewTabPageCompanyLogo
  - Nome GP: Imposta logo aziendale nuova scheda (obsoleto)
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Avvio, pagina iniziale e nuova scheda
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: NewTabPageCompanyLogo
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\NewTabPageCompanyLogo = {
  "default_logo": {
    "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29", 
    "url": "https://www.contoso.com/logo.png"
  }, 
  "light_logo": {
    "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737", 
    "url": "https://www.contoso.com/light_logo.png"
  }
}
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: NewTabPageCompanyLogo
  - Valore di esempio:
``` xml
<key>NewTabPageCompanyLogo</key>
<dict>
  <key>default_logo</key>
  <dict>
    <key>hash</key>
    <string>cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29</string>
    <key>url</key>
    <string>https://www.contoso.com/logo.png</string>
  </dict>
  <key>light_logo</key>
  <dict>
    <key>hash</key>
    <string>517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737</string>
    <key>url</key>
    <string>https://www.contoso.com/light_logo.png</string>
  </dict>
</dict>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NewTabPageHideDefaultTopSites
  #### Nascondi i siti principali predefiniti dalla nuova scheda
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Nasconde i siti principali predefiniti dalla nuova scheda in Microsoft Edge.

Se imposti questi criteri su true, i riquadri predefiniti sulla parte superiore del sito vengono nascosti.

Se imposti questi criteri su false o non li configuri, i riquadri predefiniti sulla parte superiore del sito rimangono visibili.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: NewTabPageHideDefaultTopSites
  - Nome GP: Nascondi i siti principali predefiniti dalla nuova scheda
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Avvio, pagina iniziale e nuova scheda
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: NewTabPageHideDefaultTopSites
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: NewTabPageHideDefaultTopSites
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NewTabPageLocation
  #### Configura l'URL della nuova scheda
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Configura l'URL predefinito per la nuova scheda.

Questo criterio determina la pagina che viene aperta quando vengono create nuove schede (inclusa l'apertura di nuove finestre). Influisce anche sulla pagina di avvio se è impostata per l'apertura nella nuova scheda.

Questo criterio non determina la pagina che viene aperta all'avvio controllata dal criterio [RestoreOnStartup](#restoreonstartup) e non interessa la home page se è impostata per l'apertura nella nuova scheda.

Se non configuri questo criterio, viene utilizzata la nuova scheda predefinita.

Se configuri questo criterio *e* il criterio [NewTabPageSetFeedType](#newtabpagesetfeedtype), questo criterio ha la precedenza.

Se viene specificato un URL non valido, le nuove schede vengono aperte con about://blank.

Questo criterio è disponibile solo nelle istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: NewTabPageLocation
  - Nome GP: Configura l'URL della nuova scheda
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Avvio, pagina iniziale e nuova scheda
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Avvio, pagina iniziale e nuova scheda
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: NewTabPageLocation
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"https://www.fabrikam.com"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: NewTabPageLocation
  - Valore di esempio:
``` xml
<string>https://www.fabrikam.com</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NewTabPageManagedQuickLinks
  #### Imposta collegamenti rapidi per la nuova scheda
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 79 o in seguito

  #### Descrizione
  Per impostazione predefinita, Microsoft Edge mostra i collegamenti rapidi nella nuova pagina della scheda dai collegamenti aggiunti dall'utente e i siti principali in base alla cronologia delle esplorazioni. Con questo criterio, puoi configurare fino a tre riquadri di collegamento rapido nella nuova pagina della scheda, espressa come oggetto JSON:

[ { "url": "https://www.contoso.com", "title": "Contoso Portal", "pinned": true/false }, ... ]

Il campo 'URL' è obbligatorio. 'title' e 'pinned' sono facoltativi. Se 'title' non è specificato, l'URL viene utilizzato come titolo predefinito. Se 'pinned' non è specificato, il valore predefinito è false.

Microsoft Edge li presenta nell'ordine elencato, da sinistra a destra, con tutti i riquadri bloccati prima dei riquadri non bloccati.

Se il criterio è impostato come obbligatorio, il campo 'pinned' verrà ignorato e tutti i riquadri verranno bloccati. I riquadri non possono essere eliminati dall'utente e verranno sempre visualizzati nella prima parte dell'elenco dei collegamenti rapidi.

Se il criterio è impostato come consigliato, i riquadri bloccati rimarranno nell'elenco, ma l'utente potrà modificarli ed eliminarli. I riquadri dei collegamenti rapidi che non sono bloccati si comportano come i siti principali predefiniti e vengono spostati fuori dall'elenco se altri siti Web vengono visitati più di frequente. Quando si applicano collegamenti non bloccati tramite questo criterio a un profilo del browser esistente, i collegamenti potrebbero non essere visualizzati, a seconda del livello di classificazione rispetto alla cronologia delle esplorazioni dell'utente.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Dizionario

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: NewTabPageManagedQuickLinks
  - Nome GP: Imposta collegamenti rapidi per la nuova scheda
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Avvio, pagina iniziale e nuova scheda
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Avvio, pagina iniziale e nuova scheda
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: NewTabPageManagedQuickLinks
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\NewTabPageManagedQuickLinks = [
  {
    "pinned": true, 
    "title": "Contoso Portal", 
    "url": "https://contoso.com"
  }, 
  {
    "title": "Fabrikam", 
    "url": "https://fabrikam.com"
  }
]
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: NewTabPageManagedQuickLinks
  - Valore di esempio:
``` xml
<key>NewTabPageManagedQuickLinks</key>
<array>
  <dict>
    <key>pinned</key>
    <true/>
    <key>title</key>
    <string>Contoso Portal</string>
    <key>url</key>
    <string>https://contoso.com</string>
  </dict>
  <dict>
    <key>title</key>
    <string>Fabrikam</string>
    <key>url</key>
    <string>https://fabrikam.com</string>
  </dict>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NewTabPagePrerenderEnabled
  #### Attiva precaricamento della nuova scheda per il rendering più veloce
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 85 o in seguito

  #### Descrizione
  Se configuri questo criterio, il precaricamento della pagina Nuova scheda sarà abilitato e gli utenti non potranno modificare questa impostazione. Se non configuri questo criterio, il precaricamento sarà abilitato e un utente può modificare questa impostazione.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: NewTabPagePrerenderEnabled
  - Nome GP: Attiva precaricamento della nuova scheda per il rendering più veloce
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Avvio, pagina iniziale e nuova scheda
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Avvio, pagina iniziale e nuova scheda
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: NewTabPagePrerenderEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: NewTabPagePrerenderEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NewTabPageSetFeedType
  #### Configura l'esperienza della nuova scheda di Microsoft Edge
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 79 o in seguito

  #### Descrizione
  Consente di scegliere l'esperienza di feed di Microsoft News o Office 365 per la nuova scheda.

       Quando imposti questi criteri su ’’News’’, gli utenti visualizzeranno l'esperienza di feed di Microsoft News nella nuova scheda.

      Quando imposti questi criteri su ’’Office’’, gli utenti con accesso browser Azure Active Directory vedranno l’esperienza del feed di Office 365 nella nuova scheda.

      Se disabiliti o non configuri questi criteri:

       - Agli utenti con un accesso browser Azure Active Directory verrà offerta l'esperienza di feed su nuova scheda di Office 365, oltre all'esperienza di feed su nuova scheda standard.

      - Agli utenti che non dispongono di un accesso browser Azure Active Directory vedranno l'esperienza su nuova scheda standard.

       Se configuri questi criteri *e* i criteri [NewTabPageLocation](#newtabpagelocation),  [NewTabPageLocation](#newtabpagelocation) ha la precedenza.

       Impostazione predefinita: disabilitati o non configurati.

Mappatura opzioni criteri:

* News (0) = Esperienza di feed di Microsoft News

* Office (1) = Esperienza di feed di Office 365

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: NewTabPageSetFeedType
  - Nome GP: Configura l'esperienza della nuova scheda di Microsoft Edge
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Avvio, pagina iniziale e nuova scheda
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Avvio, pagina iniziale e nuova scheda
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: NewTabPageSetFeedType
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: NewTabPageSetFeedType
  - Valore di esempio:
``` xml
<integer>0</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### RestoreOnStartup
  #### Azione da eseguire all'avvio
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica come Microsoft Edge deve comportarsi all'avvio.

Se vuoi che all'avvio si apra sempre una nuova scheda, seleziona "RestoreOnStartupIsNewTabPage".

Se vuoi riaprire gli URL che erano aperti l'ultima volta che Microsoft Edge è stato chiuso, seleziona "RestoreOnStartupIsLastSession". La sessione di esplorazione precedente verrà ripristinata. Tieni presente che questa opzione disabilita alcune impostazioni che si basano su sessioni o che eseguono azioni in uscita (ad esempio cancellare i dati di navigazione all'uscita o i cookie della sola sessione).

Se vuoi aprire un set specifico di URL, seleziona "Ripristina all’avvio è un URL" (4).

La disattivazione di questa impostazione equivale a lasciarla non configurata. Gli utenti possono modificarla in Microsoft Edge.

Questo criterio è disponibile solo per le istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.

Mappatura opzioni criteri:

* RestoreOnStartupIsNewTabPage (5) = Apri in una nuova scheda

* RestoreOnStartupIsLastSession (1) = Ripristina l'ultima sessione

* RestoreOnStartupIsURLs (4) = Apri un elenco di URL

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: RestoreOnStartup
  - Nome GP: Azione da eseguire all'avvio
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Avvio, pagina iniziale e nuova scheda
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Avvio, pagina iniziale e nuova scheda
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: RestoreOnStartup
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000004
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: RestoreOnStartup
  - Valore di esempio:
``` xml
<integer>4</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### RestoreOnStartupURLs
  #### Siti da aprire quando si avvia il browser
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica un elenco di siti Web da aprire automaticamente quando viene avviato il browser. Se non configuri questo criterio, all'avvio non verrà aperto alcun sito.

Questo criterio funziona solo se hai impostato anche il criterio [RestoreOnStartup](#restoreonstartup) su "Apri un elenco di URL" (4).

Questo criterio è disponibile solo nelle istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: RestoreOnStartupURLs
  - Nome GP: Siti da aprire quando si avvia il browser
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Avvio, pagina iniziale e nuova scheda
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Avvio, pagina iniziale e nuova scheda
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati\RestoreOnStartupURLs
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\1 = "https://contoso.com"
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\2 = "https://www.fabrikam.com"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: RestoreOnStartupURLs
  - Valore di esempio:
``` xml
<array>
  <string>https://contoso.com</string>
  <string>https://www.fabrikam.com</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ShowHomeButton
  #### Mostra pulsante Home sulla barra degli strumenti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Mostra il pulsante Home nella barra degli strumenti di Microsoft Edge.

Abilita questi criteri per visualizzare sempre il pulsante Home. Disabilitali in modo da non visualizzare mai il pulsante.

Se non configuri i criteri, gli utenti possono scegliere se visualizzare il pulsante Home.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ShowHomeButton
  - Nome GP: Mostra pulsante Home sulla barra degli strumenti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Avvio, pagina iniziale e nuova scheda
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Avvio, pagina iniziale e nuova scheda
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: ShowHomeButton
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ShowHomeButton
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ## Cast policies

  [Torna all'inizio](#microsoft-edge---criteri)

  ### EnableMediaRouter
  #### Abilita Google Cast
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Abilita questi criteri per attivare Google Cast. Gli utenti saranno in grado di avviarla dal menu app, dai menu di scelta rapida della pagina, dai controlli multimediali nei siti Web abilitati per Cast e (se visualizzata) dall'icona sulla barra degli strumenti di Cast.

Disabilita questi criteri per disabilitare Google Cast.

Per impostazione predefinita, Google Cast è abilitata.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: EnableMediaRouter
  - Nome GP: Abilita Google Cast
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Cast
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: EnableMediaRouter
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: EnableMediaRouter
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ShowCastIconInToolbar
  #### Mostra l'icona cast nella barra degli strumenti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Imposta questi criteri su true per visualizzare l'icona Cast nella barra degli strumenti o nel menu extra. Gli utenti non sono in grado di rimuoverla.

Se non configuri o disabiliti questi criteri, gli utenti possono aggiungere o rimuovere l'icona utilizzando il menu contestuale.

Se hai impostato i criteri [EnableMediaRouter](#enablemediarouter) su false, questi criteri vengono ignorati e l'icona della barra degli strumenti non viene visualizzata.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ShowCastIconInToolbar
  - Nome GP: Mostra l'icona cast nella barra degli strumenti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Cast
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ShowCastIconInToolbar
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ShowCastIconInToolbar
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ## Estensioni policies

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ExtensionAllowedTypes
  #### Configura i tipi di estensione consentiti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Controlla quali tipi di estensioni possono essere installati e limita l'accesso del runtime.

Questa impostazione definisce i tipi di estensioni consentiti e gli host con cui possono interagire. Il valore è un elenco di stringhe, ognuna delle quali deve essere una delle seguenti: "extension", "theme", "user_script" e "hosted_app". Per ulteriori informazioni su questi tipi, vedi la documentazione delle estensioni Microsoft Edge.

Tieni presente che questi criteri influiscono anche sulle estensioni con installazione forzata tramite i criteri [ExtensionInstallForcelist](#extensioninstallforcelist).

Se abiliti questi criteri, vengono installate solo le estensioni corrispondenti a un tipo nell'elenco.

Se non configuri questa impostazione dei criteri, non vengono applicate restrizioni per i tipi di estensioni accettabili.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ExtensionAllowedTypes
  - Nome GP: Configura i tipi di estensione consentiti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Estensioni
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes\1 = "hosted_app"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ExtensionAllowedTypes
  - Valore di esempio:
``` xml
<array>
  <string>hosted_app</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ExtensionInstallAllowlist
  #### Consenti l'installazione di estensioni specifiche
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Per impostazione predefinita sono consentite tutte le estensioni. Tuttavia, se blocchi tutte le estensioni impostando i criteri "ExtensionInstallBlockList" su "*" gli utenti potranno installare solo le estensioni definite in questi criteri.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ExtensionInstallAllowlist
  - Nome GP: Consenti l'installazione di estensioni specifiche
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Estensioni
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\2 = "extension_id2"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ExtensionInstallAllowlist
  - Valore di esempio:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ExtensionInstallBlocklist
  #### Controlla le estensioni che non possono essere installate
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Elenca estensioni specifiche che gli utenti NON possono installare in Microsoft Edge. Quando distribuisci questi criteri, tutte le estensioni in questo elenco installate in precedenza vengono disabilitate e l'utente non può più abilitarle. Se rimuovi una voce dall'elenco delle estensioni bloccate, tale estensione viene riabilitata automaticamente laddove era installata in precedenza.

Utilizza "*" per bloccare tutte le estensioni che non sono elencate in modo esplicito nell'elenco Consenti.

Se non configuri questi criteri, gli utenti possono installare le estensioni in Microsoft Edge.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ExtensionInstallBlocklist
  - Nome GP: Controlla le estensioni che non possono essere installate
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Estensioni
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\2 = "extension_id2"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ExtensionInstallBlocklist
  - Valore di esempio:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ExtensionInstallForcelist
  #### Controlla quali estensioni vengono installate automaticamente
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica le estensioni installate automaticamente, senza interazione da parte dell'utente e impossibili da installare o disabilitare ("con installazione forzata"). Tutte le autorizzazioni richieste dalle estensioni sono implicitamente concesse, senza interazione da parte dell'utente, incluse le autorizzazioni aggiuntive richieste dalle versioni future dell'estensione. Inoltre, sono concesse le autorizzazioni per le API delle estensioni enterprise.deviceAttributes ed enterprise.platformKeys. Queste due API sono disponibili solo per le estensioni con installazione forzata.

 Questo criterio ha priorità rispetto a un eventuale criterio [ExtensionInstallBlocklist](#extensioninstallblocklist) in conflitto. Quando rimuovi un'estensione dall'elenco delle estensioni con installazione forzata, questa viene disinstallata automaticamente da Microsoft Edge.

 L'installazione forzata è limitata alle app e alle estensioni elencate nel sito Web dei componenti aggiuntivi di Microsoft Ege per le istanze diverse dalle seguenti: istanze di Windows aggiunte a un dominio di Microsoft Active Directory, istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, e istanze di macOS gestite tramite MDM o unite a un dominio tramite MCX.

Tieni presente che gli utenti possono modificare il codice sorgente delle estensioni utilizzando gli strumenti di sviluppo, causando potenzialmente un funzionamento anomalo dell'estensione. Se questo è un problema, imposta il criterio [DeveloperToolsAvailability](#developertoolsavailability).

 Per aggiungere un'estensione all'elenco, usa il formato seguente:

 [extensionID];[updateURL]

 - extensionID - la stringa di 32 lettere trovata su edge://estensioni in modalità sviluppatore.

 - updateURL (facoltativo) è l'indirizzo del documento XML del manifesto di aggiornamento per l'app o estensione, come descritto in [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043). Se vuoi installare un'estensione dal Chrome Web Store, fornisci l'URL aggiornato del Chrome Web Store: https://clients2.google.com/service/update2/crx. Tieni presente che l'URL di aggiornamento impostato in questo criterio viene usato solo per l'installazione iniziale; gli aggiornamenti successivi dell'estensione usano l'URL aggiornamento indicato nel manifesto dell'estensione. Se non imposti l'URL di aggiornamento, si presume che l'estensione sia ospitata in Microsoft Store e viene usato l'URL di aggiornamento seguente (https://edge.microsoft.com/extensionwebstorebase/v1/crx).

 Ad esempio, gggmmkjegpiggikcnhidnjjhmicpibll;https://edge.microsoft.com/extensionwebstorebase/v1/crx installa l'app Microsoft Online dall'URL di aggiornamento di Microsoft Store. Per ulteriori informazioni sull'hosting delle estensioni, vedi: [https://go.microsoft.com/fwlink/?linkid=2095044](https://go.microsoft.com/fwlink/?linkid=2095044).

 Se non configuri questo criterio, nessuna estensione viene installata automaticamente e puoi disinstallare le estensioni in Microsoft Edge.

 Tieni presente che questo criterio non si applica alla modalità InPrivate.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ExtensionInstallForcelist
  - Nome GP: Controlla quali estensioni vengono installate automaticamente
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Estensioni
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\1 = "gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\2 = "abcdefghijklmnopabcdefghijklmnop"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ExtensionInstallForcelist
  - Valore di esempio:
``` xml
<array>
  <string>gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx</string>
  <string>abcdefghijklmnopabcdefghijklmnop</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ExtensionInstallSources
  #### Configura le origini di installazione degli script degli utenti e delle estensioni
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Definisci gli URL che possono installare estensioni e temi.

Per impostazione predefinita, gli utenti devono scaricare un file *.crx per ogni estensione o script che vogliono installare, quindi devono trascinarlo sulla pagina delle impostazioni di Microsoft Edge. Questi criteri consentono a URL specifici di installare l'estensione o lo script per l'utente.

Ogni voce di questo elenco è un modello di corrispondenza a livello di estensione (vedi [https://go.microsoft.com/fwlink/?linkid=2095039](https://go.microsoft.com/fwlink/?linkid=2095039)). Gli utenti possono facilmente installare elementi da qualsiasi URL corrispondente a una voce di questo elenco. La posizione del file *.crx e la pagina da cui viene avviato il download (in altre parole, il referrer) devono essere consentiti da questi modelli.

I criteri [ExtensionInstallBlocklist](#extensioninstallblocklist) sono prioritari rispetto a questi criteri. Le estensioni presenti nell'elenco Blocca non vengono installate, anche se provengono da un sito presente in questo elenco.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ExtensionInstallSources
  - Nome GP: Configura le origini di installazione degli script degli utenti e delle estensioni
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Estensioni
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources\1 = "https://corp.contoso.com/*"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ExtensionInstallSources
  - Valore di esempio:
``` xml
<array>
  <string>https://corp.contoso.com/*</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ExtensionSettings
  #### Configura le impostazioni di gestione delle estensioni
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Configura le impostazioni di gestione delle estensioni per Microsoft Edge.

Questi criteri gestiscono diverse impostazioni, incluse quelle controllate dai criteri correlati alle estensioni. Questi criteri sostituiscono i criteri legacy, se entrambi impostati.

Questi criteri eseguono il mapping di un ID estensione o un URL di aggiornamento alla configurazione. Con l'ID estensione, la configurazione viene applicata solo all'estensione specificata. Imposta una configurazione predefinita per l'ID speciale "*", da applicare a tutte le estensioni specificatamente elencate in questi criteri. Con un URL di aggiornamento, la configurazione viene applicata a tutte le estensioni con l'URL di aggiornamento esatto specificato nel manifesto dell'estensione, come descritto in [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Dizionario

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ExtensionSettings
  - Nome GP: Configura le impostazioni di gestione delle estensioni
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Estensioni
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ExtensionSettings
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings = {
  "*": {
    "allowed_types": [
      "hosted_app"
    ], 
    "blocked_install_message": "Custom error message.", 
    "blocked_permissions": [
      "downloads", 
      "bookmarks"
    ], 
    "install_sources": [
      "https://company-intranet/apps"
    ], 
    "installation_mode": "blocked", 
    "runtime_allowed_hosts": [
      "*://good.contoso.com"
    ], 
    "runtime_blocked_hosts": [
      "*://*.contoso.com"
    ]
  }, 
  "abcdefghijklmnopabcdefghijklmnop": {
    "blocked_permissions": [
      "history"
    ], 
    "installation_mode": "allowed", 
    "minimum_version_required": "1.0.1"
  }, 
  "bcdefghijklmnopabcdefghijklmnopa": {
    "allowed_permissions": [
      "downloads"
    ], 
    "installation_mode": "force_installed", 
    "runtime_allowed_hosts": [
      "*://good.contoso.com"
    ], 
    "runtime_blocked_hosts": [
      "*://*.contoso.com"
    ], 
    "update_url": "https://contoso.com/update_url"
  }, 
  "cdefghijklmnopabcdefghijklmnopab": {
    "blocked_install_message": "Custom error message.", 
    "installation_mode": "blocked"
  }, 
  "defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd": {
    "blocked_install_message": "Custom error message.", 
    "installation_mode": "blocked"
  }, 
  "fghijklmnopabcdefghijklmnopabcde": {
    "blocked_install_message": "Custom removal message.", 
    "installation_mode": "removed"
  }, 
  "update_url:https://www.contoso.com/update.xml": {
    "allowed_permissions": [
      "downloads"
    ], 
    "blocked_permissions": [
      "wallpaper"
    ], 
    "installation_mode": "allowed"
  }
}
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ExtensionSettings
  - Valore di esempio:
``` xml
<key>ExtensionSettings</key>
<dict>
  <key>*</key>
  <dict>
    <key>allowed_types</key>
    <array>
      <string>hosted_app</string>
    </array>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>blocked_permissions</key>
    <array>
      <string>downloads</string>
      <string>bookmarks</string>
    </array>
    <key>install_sources</key>
    <array>
      <string>https://company-intranet/apps</string>
    </array>
    <key>installation_mode</key>
    <string>blocked</string>
    <key>runtime_allowed_hosts</key>
    <array>
      <string>*://good.contoso.com</string>
    </array>
    <key>runtime_blocked_hosts</key>
    <array>
      <string>*://*.contoso.com</string>
    </array>
  </dict>
  <key>abcdefghijklmnopabcdefghijklmnop</key>
  <dict>
    <key>blocked_permissions</key>
    <array>
      <string>history</string>
    </array>
    <key>installation_mode</key>
    <string>allowed</string>
    <key>minimum_version_required</key>
    <string>1.0.1</string>
  </dict>
  <key>bcdefghijklmnopabcdefghijklmnopa</key>
  <dict>
    <key>allowed_permissions</key>
    <array>
      <string>downloads</string>
    </array>
    <key>installation_mode</key>
    <string>force_installed</string>
    <key>runtime_allowed_hosts</key>
    <array>
      <string>*://good.contoso.com</string>
    </array>
    <key>runtime_blocked_hosts</key>
    <array>
      <string>*://*.contoso.com</string>
    </array>
    <key>update_url</key>
    <string>https://contoso.com/update_url</string>
  </dict>
  <key>cdefghijklmnopabcdefghijklmnopab</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>installation_mode</key>
    <string>blocked</string>
  </dict>
  <key>defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>installation_mode</key>
    <string>blocked</string>
  </dict>
  <key>fghijklmnopabcdefghijklmnopabcde</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom removal message.</string>
    <key>installation_mode</key>
    <string>removed</string>
  </dict>
  <key>update_url:https://www.contoso.com/update.xml</key>
  <dict>
    <key>allowed_permissions</key>
    <array>
      <string>downloads</string>
    </array>
    <key>blocked_permissions</key>
    <array>
      <string>wallpaper</string>
    </array>
    <key>installation_mode</key>
    <string>allowed</string>
  </dict>
</dict>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ## Impostazioni SmartScreen policies

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PreventSmartScreenPromptOverride
  #### Impedisci di ignorare i prompt di Microsoft Defender SmartScreen per i siti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Questa impostazione dei criteri consente di decidere se gli utenti possono eseguire l'override degli avvisi di Microsoft Defender SmartScreen sui siti Web potenzialmente dannosi.

Se abiliti questa impostazione, gli utenti non potranno ignorare gli avvisi di Microsoft Defender SmartScreen e non potranno visitare il sito.

Se disabiliti o non configuri questa impostazione, gli utenti potranno ignorare gli avvisi di Microsoft Defender SmartScreen e andare al sito.

Questo criterio è disponibile solo per le istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PreventSmartScreenPromptOverride
  - Nome GP: Impedisci di ignorare i prompt di Microsoft Defender SmartScreen per i siti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni SmartScreen
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: PreventSmartScreenPromptOverride
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PreventSmartScreenPromptOverride
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PreventSmartScreenPromptOverrideForFiles
  #### Impedisci di ignorare gli avvisi di Microsoft Defender SmartScreen relativi ai download
  
  
  #### Versioni supportate:
  - Su Windows dal 77 o successiva
  - Su macOS dal 79 o successiva

  #### Descrizione
  Questo criterio consente di determinare se gli utenti possono eseguire l'override degli avvisi di Microsoft Defender SmartScreen sui download non verificati.

Se abiliti questo criterio, gli utenti dell'organizzazione non potranno ignorare gli avvisi di Microsoft Defender SmartScreen e non potranno completare i download non verificati.

Se disabiliti o non configuri questo criterio, gli utenti potranno eseguire l'override degli avvisi di Microsoft Defender SmartScreen e completare i download non verificati.

Questo criterio è disponibile solo nelle istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PreventSmartScreenPromptOverrideForFiles
  - Nome GP: Impedisci di ignorare gli avvisi di Microsoft Defender SmartScreen relativi ai download
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni SmartScreen
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: PreventSmartScreenPromptOverrideForFiles
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PreventSmartScreenPromptOverrideForFiles
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SmartScreenAllowListDomains
  #### Configura l'elenco dei domini per cui Microsoft Defender SmartScreen non attiva gli avvisi
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Configura l'elenco dei domini attendibili di Microsoft Defender SmartScreen. Ciò significa che:
Microsoft Defender SmartScreen non verificherà la presenza di risorse potenzialmente dannose come il software di phishing e altri malware se gli URL di origine corrispondono a questi domini.
Il servizio di protezione download di Microsoft Defender SmartScreen non verificherà i download ospitati in questi domini.

Se abiliti questi criteri, Microsoft Defender SmartScreen considererà attendibili questi domini.
Se disabiliti o non imposti questi criteri, la protezione Microsoft Defender SmartScreen predefinita viene applicata a tutte le risorse.

Questo criterio è disponibile solo per le istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.
Tieni inoltre presente che questo criterio non si applica se l'organizzazione ha abilitato Microsoft Defender Advanced Threat Protection. In questo caso, devi configurare gli elenchi Consenti e Blocca in Microsoft Defender Security Center.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SmartScreenAllowListDomains
  - Nome GP: Configura l'elenco dei domini per cui Microsoft Defender SmartScreen non attiva gli avvisi
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni SmartScreen
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\2 = "myuniversity.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SmartScreenAllowListDomains
  - Valore di esempio:
``` xml
<array>
  <string>mydomain.com</string>
  <string>myuniversity.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SmartScreenEnabled
  #### Configura Microsoft Defender SmartScreen
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Questa impostazione dei criteri consente di abilitare Microsoft Defender SmartScreen. Microsoft Defender SmartScreen fornisce messaggi di avviso che contribuiscono a proteggere gli utenti da tentativi di phishing e software dannosi. Per impostazione predefinita, Microsoft Defender SmartScreen è abilitato.

Se abiliti questa impostazione, Microsoft Defender SmartScreen sarà attivato.

Se disabiliti questa impostazione, Microsoft Defender SmartScreen sarà disattivato.

Se non configuri questa impostazione, gli utenti potranno scegliere se usare Microsoft Defender SmartScreen.

Questo criterio è disponibile solo per le istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SmartScreenEnabled
  - Nome GP: Configura Microsoft Defender SmartScreen
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni SmartScreen
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Impostazioni SmartScreen
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: SmartScreenEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SmartScreenEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SmartScreenForTrustedDownloadsEnabled
  #### Forza i controlli Microsoft Defender SmartScreen per i download da origini attendibili
  
  
  #### Versioni supportate:
  - Su Windows dal 78 o successiva

  #### Descrizione
  Questa impostazione dei criteri consente di specificare se Microsoft Defender SmartScreen controlla la reputazione del download da una fonte attendibile.

Se abiliti o non configuri questa impostazione, Microsoft Defender SmartScreen controllerà la reputazione del download indipendentemente dalla fonte.

Se disabiliti questa impostazione, Microsoft Defender SmartScreen non controllerà la reputazione del download durante il download da una fonte attendibile.

Questo criterio è disponibile solo per le istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SmartScreenForTrustedDownloadsEnabled
  - Nome GP: Forza i controlli Microsoft Defender SmartScreen per i download da origini attendibili
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni SmartScreen
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Impostazioni SmartScreen
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: SmartScreenForTrustedDownloadsEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SmartScreenPuaEnabled
  #### Configura Microsoft Defender SmartScreen per bloccare le app potenzialmente indesiderate
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 80 o in seguito

  #### Descrizione
  Questa impostazione dei criteri consente di configurare se abilitare il blocco per le app potenzialmente indesiderate in Microsoft Defender SmartScreen. Il blocco di app potenzialmente indesiderate di Microsoft Defender SmartScreen fornisce messaggi di avviso per proteggere gli utenti da adware, coin miner, bundleware e altre app di scarsa reputazione ospitate da siti Web. Il blocco di app potenzialmente indesiderate in Microsoft Defender SmartScreen è disattivato per impostazione predefinita.

Se abiliti questa impostazione, il blocco di app potenzialmente indesiderate in Microsoft Defender SmartScreen verrà attivato.

Se disabiliti questa impostazione, il blocco di app potenzialmente indesiderate in Microsoft Defender SmartScreen verrà disattivato.

Se non configuri questa impostazione, gli utenti potranno scegliere se usare il blocco di app potenzialmente indesiderate in Microsoft Defender SmartScreen.

Questo criterio è disponibile solo per le istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SmartScreenPuaEnabled
  - Nome GP: Configura Microsoft Defender SmartScreen per bloccare le app potenzialmente indesiderate
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni SmartScreen
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Impostazioni SmartScreen
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: SmartScreenPuaEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SmartScreenPuaEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ## Impostazioni dei contenuti policies

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AutoSelectCertificateForUrls
  #### Seleziona automaticamente i certificati client per questi siti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica un elenco di siti, in base ai modelli di URL, per cui Microsoft Edge deve selezionare automaticamente un certificato client, se il sito ne richiede uno.

Il valore deve essere una matrice di dizionari JSON sotto forma di stringa. Il modulo per ogni dizionario è { "pattern": "$URL_PATTERN", "filter" : $FILTER }, dove $URL_PATTERN è un modello di impostazione di contenuto. $FILTER limita i certificati client che il browser può selezionare automaticamente. Indipendente del filtro, solo i certificati che corrispondono alla richiesta di certificato del server possono essere utilizzati. Ad esempio, se $FILTER ha il formato { "ISSUER": { "CN": "$ISSUER_CN" } }, possono essere utilizzati solo i certificati client emessi da un certificato con CommonName $ISSUER_CN. Se $FILTER contiene una sezione "ISSUER" e una sezione "SUBJECT" un certificato client deve soddisfare entrambe le condizioni per essere selezionato. Se $FILTER specifica un'organizzazione ("O"), un certificato deve avere almeno un'organizzazione che corrisponde al valore specificato. Se $FILTER specifica un'unità organizzativa ("OU"), un certificato deve avere almeno una unità organizzativa che corrisponde al valore specificato. Se $FILTER corrisponde al dizionario vuoto {}, la selezione dei certificati client non prevede restrizioni aggiuntive.

Se non configuri questi criteri, la selezione automatica non è prevista per nessun sito.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AutoSelectCertificateForUrls
  - Nome GP: Seleziona automaticamente i certificati client per questi siti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls\1 = "{\"pattern\":\"https://www.contoso.com\",\"filter\":{\"ISSUER\":{\"CN\":\"certificate issuer name\", \"L\": \"certificate issuer location\", \"O\": \"certificate issuer org\", \"OU\": \"certificate issuer org unit\"}, \"SUBJECT\":{\"CN\":\"certificate subject name\", \"L\": \"certificate subject location\", \"O\": \"certificate subject org\", \"OU\": \"certificate subject org unit\"}}}"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AutoSelectCertificateForUrls
  - Valore di esempio:
``` xml
<array>
  <string>{"pattern":"https://www.contoso.com","filter":{"ISSUER":{"CN":"certificate issuer name", "L": "certificate issuer location", "O": "certificate issuer org", "OU": "certificate issuer org unit"}, "SUBJECT":{"CN":"certificate subject name", "L": "certificate subject location", "O": "certificate subject org", "OU": "certificate subject org unit"}}}</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### CookiesAllowedForUrls
  #### Consenti i cookie per siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Definisci un elenco di siti basati sui modelli di URL che non possono impostare i cookie.

Se non configuri questi criteri, per tutti i siti viene utilizzato il valore predefinito globale dei criteri [DefaultCookiesSetting](#defaultcookiessetting) (se impostati) o la configurazione personale dell'utente.

Per ulteriori informazioni, vedi i criteri [CookiesBlockedForUrls](#cookiesblockedforurls) e [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls).

Tieni presente che non ci possono essere modelli di URL in conflitto tra questi tre criteri:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- CookiesAllowedForUrls

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

Per evitare che i cookie vengano eliminati alla chiusura, configura il criterio [SaveCookiesOnExit](#savecookiesonexit).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: CookiesAllowedForUrls
  - Nome GP: Consenti i cookie per siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: CookiesAllowedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### CookiesBlockedForUrls
  #### Blocca i cookie per siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Definisci un elenco di siti basati sui modelli di URL che non possono impostare i cookie.

Se non configuri questi criteri, per tutti i siti viene utilizzato il valore predefinito globale dei criteri [DefaultCookiesSetting](#defaultcookiessetting) (se impostati) o la configurazione personale dell'utente.

Per ulteriori informazioni, vedi i criteri [CookiesAllowedForUrls](#cookiesallowedforurls) e [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls).

Tieni presente che non ci possono essere modelli di URL in conflitto tra questi tre criteri:

CookiesBlockedForUrls

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: CookiesBlockedForUrls
  - Nome GP: Blocca i cookie per siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: CookiesBlockedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### CookiesSessionOnlyForUrls
  #### Limita i cookie provenienti da siti Web specifici per la sessione corrente
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  I cookie creati da siti Web che corrispondono a un modello di URL definito vengono cancellati al termine della sessione (quando viene chiusa la finestra).

I cookie creati da siti Web che non corrispondono al modello sono controllati dai criteri [DefaultCookiesSetting](#defaultcookiessetting) (se impostati) o dalla configurazione personale dell'utente. Questo è il comportamento predefinito se non configuri questi criteri.

Se Microsoft Edge è in esecuzione in background, la sessione potrebbe non chiudersi quando viene chiusa l'ultima finestra, il che significa che i cookie non vengono cancellati alla chiusura della finestra. Vedi i criteri [BackgroundModeEnabled](#backgroundmodeenabled) per informazioni sulla configurazione delle azioni quando Microsoft Edge è in esecuzione in background.

Inoltre puoi utilizzare i criteri [CookiesAllowedForUrls](#cookiesallowedforurls) e [CookiesBlockedForUrls](#cookiesblockedforurls) per controllare quali siti Web possono creare cookie.

Tieni presente che non ci possono essere modelli di URL in conflitto tra questi tre criteri:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- CookiesSessionOnlyForUrls

Se imposti i criteri [RestoreOnStartup](#restoreonstartup) per il ripristino degli URL delle sessioni precedenti, questi criteri vengono ignorati e i cookie sono archiviati in modo permanente per i siti.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: CookiesSessionOnlyForUrls
  - Nome GP: Limita i cookie provenienti da siti Web specifici per la sessione corrente
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: CookiesSessionOnlyForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultCookiesSetting
  #### Configura i cookie
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Controlla se i siti web possono creare cookie sul dispositivo dell'utente. Questi criteri sono per tutti i siti o per nessuno di essi: puoi consentire a tutti i siti Web di creare cookie oppure nessun sito Web crea cookie. Non puoi utilizzare questi criteri per abilitare i cookie di siti Web specifici.

Imposta i criteri su "SessionOnly" per cancellare i cookie quando la sessione viene chiusa. Se Microsoft Edge è in esecuzione in background, la sessione potrebbe non chiudersi quando l'ultima finestra viene chiusa, il che significa che i cookie non vengono cancellati quando viene chiusa la finestra. Vedi i criteri [BackgroundModeEnabled](#backgroundmodeenabled) per informazioni sulla configurazione delle operazioni quando Microsoft Edge è in esecuzione in background.

Se non configuri questi criteri, vengono usati i criteri predefiniti "AllowCookies" e gli utenti possono cambiare questo valore nelle impostazioni di Microsoft Edge. Se non desideri che gli utenti possano modificare questa impostazione, è necessario impostare i criteri.

Mappatura opzioni criteri:

* AllowCookies (1) = Consenti a tutti i siti di creare cookie

* BlockCookies (2) = Non consentire a nessun sito di creare cookie

* SessionOnly (4) = Mantenere i cookie per tutta la durata della sessione, ad eccezione di quelli elencati in [SaveCookiesOnExit](#savecookiesonexit)

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultCookiesSetting
  - Nome GP: Configura i cookie
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DefaultCookiesSetting
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultCookiesSetting
  - Valore di esempio:
``` xml
<integer>1</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultFileSystemReadGuardSetting
  #### Controlla l'uso dell'API file System per la lettura
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Se si imposta questo criterio su 3, i siti Web potranno chiedere l'accesso in lettura al file System del sistema operativo host mediante l'API del file System. Se imposti questi criteri su 2, l'accesso è negato.

Se non si imposta questo criterio, i siti Web potranno chiedere l'accesso. Gli utenti possono modificare questa impostazione.

Mappatura opzioni criteri:

* BlockFileSystemRead (2) = Non consentire ad alcun sito di richiedere l'accesso in lettura ai file e alle directory tramite l'API del file System

* AskFileSystemRead (3) = Consenti ai siti di chiedere all'utente di concedere l'accesso in lettura ai file e alle directory tramite l'API del file System

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultFileSystemReadGuardSetting
  - Nome GP: Controlla l'uso dell'API file System per la lettura
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DefaultFileSystemReadGuardSetting
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultFileSystemReadGuardSetting
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultFileSystemWriteGuardSetting
  #### Controlla l'uso dell'API file System per la scrittura
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Se si imposta questo criterio su 3, i siti Web potranno chiedere l'accesso in scrittura al file System del sistema operativo host mediante l'API del file System. Se imposti questi criteri su 2, l'accesso è negato.

Se non si imposta questo criterio, i siti Web potranno chiedere l'accesso. Gli utenti possono modificare questa impostazione.

Mappatura opzioni criteri:

* BlockFileSystemWrite (2) = Non consentire ad alcun sito di richiedere l'accesso in scrittura a file e directory

* AskFileSystemWrite (3) = Consenti ai siti di chiedere all'utente di concedere l'accesso in scrittura ai file e alle directory

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultFileSystemWriteGuardSetting
  - Nome GP: Controlla l'uso dell'API file System per la scrittura
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DefaultFileSystemWriteGuardSetting
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultFileSystemWriteGuardSetting
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultGeolocationSetting
  #### Impostazione predefinita per la georilevazione
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specificare se i siti Web possono tenere traccia delle posizioni fisiche degli utenti. Per impostazione predefinita, è possibile consentire la verifica ('Consenti geolocalizzazione'), negarla per impostazione predefinita ('Blocca geolocalizzazione') o chiedere all'utente ogni volta che un sito Web richiede la posizione ('Chiedi geolocalizzazione').

Se il criterio non viene configurato, verrà usato 'AskGeolocation' con la possibilità per l’utente di modificarlo.

Mappatura opzioni criteri:

* AllowGeolocation (1) = Consenti ai siti di tenere traccia della posizione fisica degli utenti

* BlockGeolocation (2) = Non consentire ad alcun sito di rilevare la posizione fisica degli utenti

* AskGeolocation (3) = Chiedi conferma ogni volta che un sito tenta di tracciare la posizione fisica degli utenti

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultGeolocationSetting
  - Nome GP: Impostazione predefinita per la georilevazione
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DefaultGeolocationSetting
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultGeolocationSetting
  - Valore di esempio:
``` xml
<integer>1</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultImagesSetting
  #### Impostazione predefinita per le immagini
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica se i siti Web possono visualizzare immagini. Puoi consentire immagini in tutti i siti ('Consenti immagini')  o bloccarle in tutti i siti ('Blocca immagini').

Se non configuri questi criteri, le immagini sono consentite per impostazione predefinita e l'utente può modificare questa impostazione.

Mappatura opzioni criteri:

* AllowImages (1) = Consenti la visualizzazione di tutte le immagini per tutti i siti

* BlockImages (2) = Non consentire ad alcun sito di mostrare le immagini

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultImagesSetting
  - Nome GP: Impostazione predefinita per le immagini
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DefaultImagesSetting
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultImagesSetting
  - Valore di esempio:
``` xml
<integer>1</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultInsecureContentSetting
  #### Controlla l'uso di eccezioni di contenuto non sicuro
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 80 o in seguito

  #### Descrizione
  Consente di specificare se gli utenti possono aggiungere eccezioni per consentire contenuti misti per siti specifici.

Questi criteri possono essere sovrascritti per specifici modelli di URL utilizzando i criteri [InsecureContentAllowedForUrls](#insecurecontentallowedforurls) and [InsecureContentBlockedForUrls](#insecurecontentblockedforurls).

Se questi criteri non vengono impostati, gli utenti potranno aggiungere eccezioni per consentire il contenuto misto bloccabile e disabilitare gli aggiornamenti automatici del contenuto misto bloccabile facoltativamente.

Mappatura opzioni criteri:

* BlockInsecureContent (2) = Non consentire a nessun sito di caricare contenuti misti

* AllowExceptionsInsecureContent (3) = Consenti agli utenti di aggiungere eccezioni per consentire contenuti misti

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultInsecureContentSetting
  - Nome GP: Controlla l'uso di eccezioni di contenuto non sicuro
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DefaultInsecureContentSetting
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultInsecureContentSetting
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultJavaScriptSetting
  #### Impostazione predefinita per JavaScript
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica se i siti Web possono eseguire JavaScript. Puoi consentirlo per tutti i siti (‘Consenti Java script’) o bloccarlo per tutti i siti (‘Blocca Java script’).

Se non configuri questi criteri, tutti i siti possono eseguire JavaScript per impostazione predefinita e l'utente potrà modificare questa impostazione.

Mappatura opzioni criteri:

* AllowJavaScript (1) = Consenti l'esecuzione di JavaScript per tutti i siti

* BlockJavaScript (2) = Non consentire ad alcun sito di eseguire JavaScript

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultJavaScriptSetting
  - Nome GP: Impostazione predefinita per JavaScript
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DefaultJavaScriptSetting
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultJavaScriptSetting
  - Valore di esempio:
``` xml
<integer>1</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultNotificationsSetting
  #### Impostazione predefinita per la notifica
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica se i siti Web possono visualizzare notifiche sul desktop. Puoi consentirle per impostazione predefinita (‘Consenti notifiche’), rifiutarle per impostazione predefinita (‘Blocca notifiche’) oppure fare in modo che all'utente venga richiesto ogni volta che un sito Web sta tentando di visualizzare una notifica (‘Chiedi notifiche’).

Se non configuri questi criteri, le notifiche sono consentite per impostazione predefinita e l'utente potrà modificare questa impostazione.

Mappatura opzioni criteri:

* AllowNotifications (1) = Consenti ai siti di visualizzare le notifiche desktop

* BlockNotifications (2) = Non consentire ad alcun sito di mostrare notifiche sul desktop

* AskNotifications (3) = Chiedi conferma ogni volta che un sito tenta di visualizzare le notifiche desktop

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultNotificationsSetting
  - Nome GP: Impostazione predefinita per la notifica
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DefaultNotificationsSetting
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultNotificationsSetting
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultPluginsSetting
  #### Impostazione predefinita per Adobe Flash
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  [PluginsAllowedForUrls](#pluginsallowedforurls) e [PluginsBlockedForUrls](#pluginsblockedforurls) vengono controllati prima, quindi viene creato questo criterio. Le opzioni sono "ClickToPlay" e "BlockPlugins". Se imposti questo criterio su "BlockPlugins", questo plug-in viene negato a tutti i siti web. "ClickToPlay" consente l'esecuzione del plug-in Flash, ma gli utenti fanno clic sul segnaposto per avviarlo.

Se non imposti questo criterio, utilizza BlockPlugins e gli utenti possono modificare questa impostazione.

Nota: la riproduzione automatica vale solo per i domini esplicitamente elencati nel criterio [PluginsAllowedForUrls](#pluginsallowedforurls). Per attivare la riproduzione automatica per tutti i siti, aggiungi http://* and https://* all'elenco di URL consentiti.

Mappatura opzioni criteri:

* BlockPlugins (2) = Blocca il plug-in Adobe Flash

* ClickToPlay (3) = Fai clic per riprodurre

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultPluginsSetting
  - Nome GP: Impostazione predefinita per Adobe Flash
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DefaultPluginsSetting
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultPluginsSetting
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultPopupsSetting
  #### Impostazione predefinita per la finestra popup
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica se i siti Web possono visualizzare finestre popup. Puoi consentirle su tutti i siti Web (‘Consenti Popup’) o bloccarle su tutti i siti (‘Blocca Popup’).

Se non configuri questi criteri, le finestre popup sono bloccate per impostazione predefinita e gli utenti possono modificare questa impostazione.

Mappatura opzioni criteri:

* AllowPopups (1) = Consenti la visualizzazione dei popup per tutti i siti

* BlockPopups (2) = Non consentire ad alcun sito di mostrare i popup

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultPopupsSetting
  - Nome GP: Impostazione predefinita per la finestra popup
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DefaultPopupsSetting
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultPopupsSetting
  - Valore di esempio:
``` xml
<integer>1</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultWebBluetoothGuardSetting
  #### Controlla l'uso dell'API Web Bluetooth
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Controlla se i siti Web possono accedere ai dispositivi Bluetooth nelle vicinanze. Puoi totalmente bloccare l'accesso o fare in modo che il sito visualizzi una richiesta per l'utente ogni volta che vuole accedere a un dispositivo Bluetooth.

Se non configuri questi criteri, viene usato il valore predefinito ('Chiedi Bluetooth Web', ossia viene visualizzata ogni volta la richiesta per gli utenti) e gli utenti possono modificare il valore.

Mappatura opzioni criteri:

* BlockWebBluetooth (2) = Non consentire ad alcun sito di richiedere l'accesso ai dispositivi Bluetooth tramite l'API Bluetooth su Web

* AskWebBluetooth (3) = Consenti ai siti di chiedere all'utente di concedere l'accesso a un dispositivo Bluetooth nelle vicinanze

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultWebBluetoothGuardSetting
  - Nome GP: Controlla l'uso dell'API Web Bluetooth
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DefaultWebBluetoothGuardSetting
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultWebBluetoothGuardSetting
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultWebUsbGuardSetting
  #### Controlla l'uso dell'API WebUSB
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica se i siti Web possono accedere a dispositivi USB connessi. Puoi bloccare completamente l'accesso o chiedere all'utente ogni volta che un sito Web sta tentando di accedere ai dispositivi USB connessi.

Puoi eseguire l'override di questi criteri per modelli di URL specifici tramite i criteri [WebUsbAskForUrls](#webusbaskforurls) e [WebUsbBlockedForUrls](#webusbblockedforurls).

Se non configuri questi criteri, i siti possono chiedere agli utenti se possono accedere ai dispositivi USB connessi ('Chiedi USB Web') per impostazione predefinita e gli utenti possono modificare questa impostazione.

Mappatura opzioni criteri:

* BlockWebUsb (2) = Non consentire ad alcun sito di richiedere l'accesso ai dispositivi USB tramite l'API WebUSB

* AskWebUsb (3) = Consenti ai siti di chiedere all'utente di concedere l'accesso a un dispositivo USB connesso

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultWebUsbGuardSetting
  - Nome GP: Controlla l'uso dell'API WebUSB
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DefaultWebUsbGuardSetting
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultWebUsbGuardSetting
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### FileSystemReadAskForUrls
  #### Consenti accesso in lettura tramite l'API file System in questi siti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  L'impostazione dei criteri consente di elencare i modelli di URL che specificano quali siti possono chiedere agli utenti di concedere l'accesso in lettura ai file o alle directory del file System del sistema operativo host tramite l'API del file System.

Se si esce dall'impostazione dei criteri, [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)applicabile per tutti i siti, se è impostata. Se non si applicano le impostazioni personali degli utenti.

I modelli di URL non possono essere in conflitto con [FileSystemReadBlockedForUrls](#filesystemreadblockedforurls). Nessun criterio ha la precedenza se un URL corrisponde a entrambi.

Per informazioni dettagliate sui modelli url validi, vedere https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: FileSystemReadAskForUrls
  - Nome GP: Consenti accesso in lettura tramite l'API file System in questi siti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\2 = "[*.]example.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: FileSystemReadAskForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### FileSystemReadBlockedForUrls
  #### Blocca accesso in lettura tramite l'API del file System in questi siti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Se si imposta questo criterio, è possibile elencare i modelli di URL che specificano quali siti non possono chiedere agli utenti di concedere l'accesso in lettura ai file o alle directory del file System del sistema operativo host tramite l'API del file System.

Se non imposti questi criteri, [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)si applica a tutti i siti, se è impostato. Se non si applicano le impostazioni personali degli utenti.

I modelli di URL non possono essere in conflitto con.[FileSystemReadAskForUrls](#filesystemreadaskforurls) Nessun criterio ha la precedenza se un URL corrisponde a entrambi.

Per informazioni dettagliate sui modelli url validi, vedere https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: FileSystemReadBlockedForUrls
  - Nome GP: Blocca accesso in lettura tramite l'API del file System in questi siti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\2 = "[*.]example.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: FileSystemReadBlockedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### FileSystemWriteAskForUrls
  #### Consenti accesso in scrittura ai file e alle directory in questi siti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Se si imposta questo criterio, è possibile elencare i modelli di URL che specificano quali siti possono chiedere agli utenti di concedere l'accesso in scrittura ai file o alle directory nel file System del sistema operativo host.

Se non imposti questi criteri,[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)si applica a tutti i siti, se è impostato. Se non si applicano le impostazioni personali degli utenti

i modelli di URL non possono essere in conflitto con [FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls) Nessun criterio ha la precedenza se un URL corrisponde a entrambi

Per informazioni dettagliate sui modelli url validi, vedere https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: FileSystemWriteAskForUrls
  - Nome GP: Consenti accesso in scrittura ai file e alle directory in questi siti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\2 = "[*.]example.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: FileSystemWriteAskForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### FileSystemWriteBlockedForUrls
  #### Blocca accesso in scrittura a file e directory in questi siti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Se si imposta questo criterio, è possibile elencare i modelli di URL che specificano i siti che non possono chiedere agli utenti di concedere l'accesso in scrittura ai file o alle directory nel file System del sistema operativo host.

Se non imposti questi criteri,.[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)si applica a tutti i siti, se è impostato. Se non si applicano le impostazioni personali degli utenti

I modelli di URL non possono essere in conflitto con.[FileSystemWriteAskForUrls](#filesystemwriteaskforurls)Nessun criterio ha la precedenza se un URL corrisponde a entrambi.

Per informazioni dettagliate sui modelli urlvalidi, vedere https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: FileSystemWriteBlockedForUrls
  - Nome GP: Blocca accesso in scrittura a file e directory in questi siti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\2 = "[*.]example.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: FileSystemWriteBlockedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ImagesAllowedForUrls
  #### Consenti le immagini per questi siti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Definisci un elenco di siti basati sui modelli di URL che possono visualizzare le immagini.

Se non configuri questi criteri, per tutti i siti viene utilizzato il valore predefinito globale dei criteri [DefaultImagesSetting](#defaultimagessetting) (se impostati) o la configurazione personale dell'utente.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ImagesAllowedForUrls
  - Nome GP: Consenti le immagini per questi siti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ImagesAllowedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ImagesBlockedForUrls
  #### Blocca le immagini per siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Definisci un elenco di siti basati sui modelli di URL a cui non è consentito visualizzare le immagini.

Se non configuri questi criteri, per tutti i siti viene utilizzato il valore predefinito globale dei criteri [DefaultImagesSetting](#defaultimagessetting) (se impostati) o la configurazione personale dell'utente.


  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ImagesBlockedForUrls
  - Nome GP: Blocca le immagini per siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ImagesBlockedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### InsecureContentAllowedForUrls
  #### Consenti contenuto non sicuro nei siti specificati
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 80 o in seguito

  #### Descrizione
  Crea un elenco di modelli di URL per specificare i siti che possono visualizzare contenuti misti non sicuri (ovvero il contenuto HTTP nei siti HTTPS).

Se non si configurano questi criteri, i contenuti misti bloccabili verranno bloccati e verranno aggiornati i contenuti misti bloccabili facoltativamente. Tuttavia, gli utenti potranno impostare eccezioni per consentire i contenuti misti non sicuri per siti specifici.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: InsecureContentAllowedForUrls
  - Nome GP: Consenti contenuto non sicuro nei siti specificati
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\2 = "[*.]example.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: InsecureContentAllowedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### InsecureContentBlockedForUrls
  #### Blocca contenuto non sicuro nei siti specificati
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 80 o in seguito

  #### Descrizione
  Crea un elenco di modelli di URL per specificare i siti a cui non è consentito visualizzare contenuti misti (attivi) bloccabili (ad esempio, contenuto HTTP nei siti HTTPS) e per i quali gli aggiornamenti di contenuto misto bloccabile facoltativamente verranno disabilitati.

Se non si configurano questi criteri, i contenuti misti bloccabili verranno bloccati e verrà aggiornato il contenuto misto bloccabile facoltativamente. Tuttavia, gli utenti potranno impostare eccezioni per consentirne l'impostazione per siti specifici.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: InsecureContentBlockedForUrls
  - Nome GP: Blocca contenuto non sicuro nei siti specificati
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\2 = "[*.]example.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: InsecureContentBlockedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### JavaScriptAllowedForUrls
  #### Consenti JavaScript per siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Definisci un elenco di siti basati sui modelli di URL che sono autorizzati a eseguire JavaScript.

Se non configuri questi criteri, per tutti i siti viene utilizzato il valore predefinito globale dei criteri [DefaultJavaScriptSetting](#defaultjavascriptsetting) (se impostati) o la configurazione personale dell'utente.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: JavaScriptAllowedForUrls
  - Nome GP: Consenti JavaScript per siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: JavaScriptAllowedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### JavaScriptBlockedForUrls
  #### Blocca JavaScript per siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Definisci un elenco di siti basati sui modelli di URL per cui non è consentita l'esecuzione di JavaScript.

Se non configuri questi criteri, per tutti i siti viene utilizzato il valore predefinito globale dei criteri [DefaultJavaScriptSetting](#defaultjavascriptsetting) (se impostati) o la configurazione personale dell'utente.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: JavaScriptBlockedForUrls
  - Nome GP: Blocca JavaScript per siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: JavaScriptBlockedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### LegacySameSiteCookieBehaviorEnabled
  #### Abilita impostazione predefinita del comportamento dei cookie SameSite
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 80 o in seguito

  #### Descrizione
  Consente di ripristinare tutti i cookie sul comportamento SameSite legacy. Se si ripristina il comportamento legacy, i cookie che non specificano un attributo SameSite vengono considerati come se fossero "SameSite=None" e viene rimosso il requisito per cui i cookie "SameSite=None" devono includere l'attributo "Secure".

Se non imposti questi criteri, il comportamento predefinito per i cookie che non specificano un attributo SameSite dipenderà da altre origini di configurazione per la funzionalità SameSite-by-default. Questa funzionalità può essere impostata da una versione di valutazione sul campo o abilitando il flag same-site-by-default-cookies in edge://flags.

Mappatura opzioni criteri:

* DefaultToLegacySameSiteCookieBehavior (1) = Ripristina il comportamento SameSite legacy per i cookie in tutti i siti

* DefaultToSameSiteByDefaultCookieBehavior (2) = Utilizza il comportamento SameSite-by-default per i cookie in tutti i siti

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: LegacySameSiteCookieBehaviorEnabled
  - Nome GP: Abilita impostazione predefinita del comportamento dei cookie SameSite
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: LegacySameSiteCookieBehaviorEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: LegacySameSiteCookieBehaviorEnabled
  - Valore di esempio:
``` xml
<integer>1</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### LegacySameSiteCookieBehaviorEnabledForDomainList
  #### Ripristina il comportamento SameSite legacy per i cookie nei siti specificati
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 80 o in seguito

  #### Descrizione
  I cookie impostati per i domini che corrispondono a modelli specificati verranno ripristinati sul comportamento SameSite legacy.

Se si ripristina il comportamento legacy, i cookie che non specificano un attributo SameSite verranno considerati come se fossero da considerare come se fossero "SameSite=None" e verrà rimosso il requisito per cui i cookie "SameSite=None" devono includere l'attributo "Secure".

Se non si impostano questi criteri, verrà utilizzato il valore predefinito globale. Verrà utilizzato il valore predefinito globale anche per i cookie nei domini non coperti dai modelli specificati.

È possibile configurare il valore predefinito globale utilizzando i criteri [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled). se i criteri [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) non sono impostati, il valore predefinito globale tornerà su altre origini di configurazione.

Tieni presente che i modelli elencati in questi criteri vengono considerati come domini, non URL, pertanto non devi specificare uno schema o una porta.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Nome GP: Ripristina il comportamento SameSite legacy per i cookie nei siti specificati
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\1 = "www.example.com"
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\2 = "[*.]example.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Valore di esempio:
``` xml
<array>
  <string>www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NotificationsAllowedForUrls
  #### Consenti le notifiche per siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Ti consente di creare un elenco di modelli di URL per specificare i siti ai quali è consentito visualizzare le notifiche.

Se non imposti questo criterio, verrà utilizzato il valore predefinito globale per tutti i siti. Questo valore predefinito deriverà dal criterio [DefaultNotificationsSetting](#defaultnotificationssetting) se è impostato o dalla configurazione personale dell'utente. Per informazioni dettagliate sui modelli di URL validi, consulta [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: NotificationsAllowedForUrls
  - Nome GP: Consenti le notifiche per siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: NotificationsAllowedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NotificationsBlockedForUrls
  #### Blocca le notifiche per siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Ti consente di creare un elenco di modelli di URL per specificare i siti ai quali non è consentito visualizzare le notifiche.

Se non imposti questo criterio, verrà utilizzato il valore predefinito globale per tutti i siti. Questo valore predefinito deriverà dal criterio [DefaultNotificationsSetting](#defaultnotificationssetting) se è impostato o dalla configurazione personale dell'utente. Per informazioni dettagliate sui modelli di URL validi, consulta [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: NotificationsBlockedForUrls
  - Nome GP: Blocca le notifiche per siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: NotificationsBlockedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PluginsAllowedForUrls
  #### Consenti il plug-in Adobe Flash per siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Definisci un elenco di siti, basato su modelli di URL, che possono eseguire il plug-inAdobe Flash.

Se non configuri questo criterio, per tutti i siti viene usato il valore predefinito globale del criterio [DefaultPluginsSetting](#defaultpluginssetting) (se impostato) o la configurazione personale dell'utente.

Per informazioni dettagliate sui modelli di URL validi, vedi  [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Tuttavia, a partire da M85, i modelli con caratteri jolly '*' e '[*.]' nell'host non sono più supportati per questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PluginsAllowedForUrls
  - Nome GP: Consenti il plug-in Adobe Flash per siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\2 = "http://contoso.edu:8080"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PluginsAllowedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PluginsBlockedForUrls
  #### Blocca il plug-in Adobe Flash per siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Definisci un elenco di siti, basato su modelli di URL, che non possono eseguire Adobe Flash.

Se non configuri questo criterio, per tutti i siti viene usato il valore predefinito globale del criterio [DefaultPluginsSetting](#defaultpluginssetting) (se impostato) o la configurazione personale dell'utente.

Per informazioni dettagliate sui modelli di URL validi, vedi [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Tuttavia, a partire da M85, i modelli con caratteri jolly '*' e '[*.]' nell'host non sono più supportati per questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PluginsBlockedForUrls
  - Nome GP: Blocca il plug-in Adobe Flash per siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\2 = "http://contoso.edu:8080"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PluginsBlockedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PopupsAllowedForUrls
  #### Consenti le finestre popup per siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Definisci un elenco di siti basati sui modelli di URL che possono aprire le finestre popup.

Se non configuri questi criteri, per tutti i siti viene utilizzato il valore predefinito globale dei criteri [DefaultPopupsSetting](#defaultpopupssetting) (se impostati) o la configurazione personale dell'utente.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PopupsAllowedForUrls
  - Nome GP: Consenti le finestre popup per siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PopupsAllowedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PopupsBlockedForUrls
  #### Blocca le finestre popup per siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Definisci un elenco di siti basati sui modelli di URL per cui è impedita l'apertura delle finestre popup.

Se non configuri questi criteri, per tutti i siti viene utilizzato il valore predefinito globale dei criteri [DefaultPopupsSetting](#defaultpopupssetting) (se impostati) o la configurazione personale dell'utente.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PopupsBlockedForUrls
  - Nome GP: Blocca le finestre popup per siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PopupsBlockedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### RegisteredProtocolHandlers
  #### Registra gestori di protocollo
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Imposta questo criterio (solo consigliato) per registrare un elenco di gestori di protocollo. Questo elenco viene unito a quelli registrati dall'utente ed entrambi sono disponibili per l'uso.

Per registrare un gestore di protocollo:

- Imposta la proprietà del protocollo sullo schema (ad esempio "mailto")
- Imposta la proprietà URL sulla proprietà URL dell'applicazione che gestisce lo schema specificato nel campo "protocollo". Il modello può includere un segnaposto "%s", che sostituisce l'URL gestito.

Gli utenti non possono rimuovere un gestore di protocollo registrato da questo criterio. Tuttavia, possono installare un nuovo gestore di protocollo predefinito per sovrascrivere i gestori di protocollo esistenti.

  #### Funzionalità supportate:
  - Può essere obbligatorio: No
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Dizionario

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: RegisteredProtocolHandlers
  - Nome GP: Registra gestori di protocollo
  - Percorso GP (Obbligatorio): N/D
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Impostazioni dei contenuti
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): N/D
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: RegisteredProtocolHandlers
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [
  {
    "default": true, 
    "protocol": "mailto", 
    "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"
  }
]
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: RegisteredProtocolHandlers
  - Valore di esempio:
``` xml
<key>RegisteredProtocolHandlers</key>
<array>
  <dict>
    <key>default</key>
    <true/>
    <key>protocol</key>
    <string>mailto</string>
    <key>url</key>
    <string>https://mail.contoso.com/mail/?extsrc=mailto&url=%s</string>
  </dict>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SpotlightExperiencesAndRecommendationsEnabled
  #### Scegli se gli utenti possono ricevere testo e immagini di sfondo personalizzati, suggerimenti, notifiche
e suggerimenti per i servizi Microsoft
  
  
  #### Versioni supportate:
  - Su Windows dal 86 o successiva

  #### Descrizione
  Scegli se gli utenti possono ricevere immagini di sfondo e testo personalizzati, suggerimenti, notifiche e suggerimenti per i servizi Microsoft.

 Se abiliti o non configuri questa impostazione, vengono attivati i consigli e le esperienze in primo piano.

Se disattivi questa impostazione, le esperienze in evidenza e i consigli vengono disattivati.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SpotlightExperiencesAndRecommendationsEnabled
  - Nome GP: Scegli se gli utenti possono ricevere testo e immagini di sfondo personalizzati, suggerimenti, notifiche
e suggerimenti per i servizi Microsoft
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: SpotlightExperiencesAndRecommendationsEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### WebUsbAllowDevicesForUrls
  #### Concedi l'accesso a siti specifici per la connessione a dispositivi USB specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente di impostare un elenco di URL che specifica a quali siti viene automaticamente concessa l'autorizzazione per accedere a un dispositivo USB con il fornitore e gli ID di prodotto specificati. Ogni voce dell'elenco deve contenere sia i dispositivi che gli URL affinché i criteri siano validi. Ogni elemento nei dispositivi può contenere un campo ID fornitore e ID prodotto. Qualsiasi ID omesso viene considerato un carattere jolly con un'eccezione e tale eccezione indica che non è possibile specificare un ID prodotto senza specificare anche un ID fornitore. In caso contrario, i criteri non sono validi e vengono ignorati.

Il modello di autorizzazione USB utilizza l'URL del sito richiedente ("URL richiedente") e l'URL del sito frame principale ("URL di incorporamento") per concedere l'autorizzazione all'URL che richiede l'accesso al dispositivo USB. L'URL richiedente può essere diverso dall'URL di incorporamento quando il sito richiedente viene caricato in un iFrame. Pertanto, il campo "URL" può contenere fino a due stringhe di URL delimitate da una virgola per specificare rispettivamente l'URL richiedente e di incorporamento. Se viene specificato un solo URL, l'accesso ai dispositivi USB corrispondenti viene concesso quando l'URL del sito richiedente corrisponde a questo URL indipendentemente dallo stato di incorporamento. Gli URL in "URL" devono essere validi, in caso contrario i criteri vengono ignorati.

Se questi criteri non vengono impostati, per tutti i siti verrà utilizzato il valore predefinito globale dei criteri [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) se impostati o in caso contrario la configurazione personale dell'utente.

I modelli di URL in questi criteri non devono essere in conflitto con quelli configurati tramite [WebUsbBlockedForUrls](#webusbblockedforurls). In caso di conflitto, questi criteri sono prioritari rispetto a [WebUsbBlockedForUrls](#webusbblockedforurls) e [WebUsbAskForUrls](#webusbaskforurls).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Dizionario

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: WebUsbAllowDevicesForUrls
  - Nome GP: Concedi l'accesso a siti specifici per la connessione a dispositivi USB specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: WebUsbAllowDevicesForUrls
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAllowDevicesForUrls = [
  {
    "devices": [
      {
        "product_id": 5678, 
        "vendor_id": 1234
      }
    ], 
    "urls": [
      "https://contoso.com", 
      "https://fabrikam.com"
    ]
  }
]
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: WebUsbAllowDevicesForUrls
  - Valore di esempio:
``` xml
<key>WebUsbAllowDevicesForUrls</key>
<array>
  <dict>
    <key>devices</key>
    <array>
      <dict>
        <key>product_id</key>
        <integer>5678</integer>
        <key>vendor_id</key>
        <integer>1234</integer>
      </dict>
    </array>
    <key>urls</key>
    <array>
      <string>https://contoso.com</string>
      <string>https://fabrikam.com</string>
    </array>
  </dict>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### WebUsbAskForUrls
  #### Consenti WebUSB per siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Definisci un elenco di siti basati sui modelli di URL che possono richiedere all'utente l'accesso a un dispositivo USB.

Se non configuri questi criteri, per tutti i siti viene utilizzato il valore predefinito globale dei criteri [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (se impostati) o la configurazione personale dell'utente.

I modelli di URL definiti in questi criteri non possono essere in conflitto con quelli configurati in [WebUsbBlockedForUrls](#webusbblockedforurls) in quanto non è possibile contemporaneamente consentire e bloccare un URL.  Per informazioni dettagliate su modelli di URL validi, vedi [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: WebUsbAskForUrls
  - Nome GP: Consenti WebUSB per siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: WebUsbAskForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### WebUsbBlockedForUrls
  #### Blocca WebUSB per siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Definisci un elenco di siti basati sui modelli di URL che non possono richiedere all'utente di concedere l'accesso a un dispositivo USB.

Se non configuri questi criteri, per tutti i siti viene utilizzato il valore predefinito globale dei criteri [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (se impostati) o la configurazione personale dell'utente.

I modelli di URL in questi criteri non possono essere in conflitto con quelli configurati in [WebUsbAskForUrls](#webusbaskforurls) in quanto non è possibile contemporaneamente consentire e bloccare un URL.  Per informazioni dettagliate su modelli di URL validi, vedi [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: WebUsbBlockedForUrls
  - Nome GP: Blocca WebUSB per siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni dei contenuti
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: WebUsbBlockedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ## Impostazioni di Application Guard policies

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ApplicationGuardContainerProxy
  #### Proxy contenitore Application Guard
  
  
  #### Versioni supportate:
  - Su Windows dal 84 o successiva

  #### Descrizione
  Configura le impostazioni proxy per Microsoft Edge Application Guard.
         Se abiliti questo criterio, Microsoft Edge Application Guard ignora altre origini di configurazioni proxy.

         Se non configuri questo criterio, Microsoft Edge Application Guard userà la configurazione proxy dell'host.

         Questo criterio non influisce sulla configurazione proxy di Microsoft Edge all'esterno di Application Guard (sull'host).

         Il campo ProxyMode consente di specificare il server proxy usato da Microsoft Edge Application Guard.

         Il campo ProxyPacUrl è un URL di un file proxy con estensione .pac.

         Il campo ProxyServer è un URL per il server proxy.

         Se scegli il valore 'diretto' come 'ProxyMode', tutti gli altri campi vengono ignorati.

         Se scegli il valore 'auto_detect' come 'ProxyMode', tutti gli altri campi vengono ignorati.

         Se scegli il valore 'fixed_servers' come 'ProxyMode', viene usato il campo 'ProxyServer'.

         Se scegli il valore 'pac_script' come 'ProxyMode', viene usato il campo 'ProxyPacUrl'.

Per maggiori informazioni sull’identificazione del traffico Application Guard tramite dual proxy, visita il sito [https://go.microsoft.com/fwlink/?linkid=2134653](https://go.microsoft.com/fwlink/?linkid=2134653).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Dizionario

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ApplicationGuardContainerProxy
  - Nome GP: Proxy contenitore Application Guard
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Impostazioni di Application Guard
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ApplicationGuardContainerProxy
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ## Messaggi nativi policies

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NativeMessagingAllowlist
  #### Controlla quali host di messaggistica nativa possono essere utilizzati dagli utenti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Elenca gli host di messaggistica nativa specifici che gli utenti possono utilizzare in Microsoft Edge.

Per impostazione predefinita, sono consentiti tutti gli host di messaggistica nativa. Se imposti i criteri [NativeMessagingBlocklist](#nativemessagingblocklist) su *, tutti gli host di messaggistica nativa sono bloccati e vengono caricati solo gli host di messaggistica nativa presenti nell'elenco.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: NativeMessagingAllowlist
  - Nome GP: Controlla quali host di messaggistica nativa possono essere utilizzati dagli utenti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Messaggi nativi
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\2 = "com.native.messaging.host.name2"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: NativeMessagingAllowlist
  - Valore di esempio:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NativeMessagingBlocklist
  #### Configura l'elenco degli host di messaggistica nativa bloccati
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica gli host di messaggistica nativa che non devono essere utilizzati.

Utilizza "*" per bloccare tutti gli host di messaggistica nativa, a meno che non siano elencati in modo esplicito nell'elenco Consenti.

Se non configuri questi criteri, Microsoft Edge carica tutti gli host di messaggistica nativa installati.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: NativeMessagingBlocklist
  - Nome GP: Configura l'elenco degli host di messaggistica nativa bloccati
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Messaggi nativi
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\2 = "com.native.messaging.host.name2"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: NativeMessagingBlocklist
  - Valore di esempio:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NativeMessagingUserLevelHosts
  #### Consenti host di messaggistica nativa a livello di utente (installati senza autorizzazioni di amministratore)
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Abilita l'installazione a livello di utente di host di messaggistica nativa.

Se disabiliti questi criteri, Microsoft Edge utilizza solo gli host di messaggistica nativa installati a livello di sistema.

Per impostazione predefinita, se non configuri questi criteri, Microsoft Edge consente l'utilizzo di host di messaggistica nativa a livello di utente.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: NativeMessagingUserLevelHosts
  - Nome GP: Consenti host di messaggistica nativa a livello di utente (installati senza autorizzazioni di amministratore)
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Messaggi nativi
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: NativeMessagingUserLevelHosts
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: NativeMessagingUserLevelHosts
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ## Protezione e gestione password policies

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PasswordManagerEnabled
  #### Abilita salvataggio password nella gestione delle password
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Abilita Microsoft Edge per salvare le password degli utenti.

Se abiliti questi criteri, gli utenti possono salvare le password in Microsoft Edge. La prossima volta che accedono al sito, Microsoft Edge immette automaticamente la password.

Se disabiliti questi criteri, gli utenti non possono salvare le nuove password, ma possono comunque utilizzare le password salvate in precedenza.

Se abiliti o disabiliti questi criteri, gli utenti non possono modificare o sostituire la password in Microsoft Edge. Se non vengono configurati, gli utenti possono salvare le password, nonché disattivare questa funzionalità.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PasswordManagerEnabled
  - Nome GP: Abilita salvataggio password nella gestione delle password
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Protezione e gestione password
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Protezione e gestione password
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: PasswordManagerEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PasswordManagerEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PasswordMonitorAllowed
  #### Consenti l’invio di avvisi agli utenti se le password non sono più sicure
  
  
  #### Versioni supportate:
  - Su Windows dal 85 o successiva

  #### Descrizione
  Consenti a Microsoft Edge di monitorare le password degli utenti.

Se abiliti questo criterio e un utente ne accetta l’abilitazione, l’utente riceverà un avviso se una o più password archiviate in Microsoft Edge non sono più sicure. Microsoft Edge mostrerà un avviso e queste informazioni saranno disponibili anche in Impostazioni > Password > Monitoraggio password.

Se disabiliti il criterio, agli utenti non verrà chiesta l’autorizzazione per abilitare questa funzionalità. Le loro password non verranno analizzate e non riceveranno avvisi.

Se abiliti o non configuri il criterio, gli utenti possono attivare o disattivare questa funzionalità.

Per maggiori informazioni su come Microsoft Edge rileva le password non sicure, vedi [https://go.microsoft.com/fwlink/?linkid=2133833](https://go.microsoft.com/fwlink/?linkid=2133833)

Informazioni aggiuntive:

È possibile impostare questo criterio come consigliato o obbligatorio, ma con un callout importante.

Abilitazione obbligatoria: poiché l’autorizzazione dei singoli utenti è una condizione preliminare per l’abilitazione di questa funzionalità per un determinato utente, questo criterio non prevede un’impostazione di abilitazione obbligatoria. Se il criterio è impostato su abilitazione obbligatoria, l’interfaccia utente in Impostazioni non cambierà e verrà visualizzato il seguente messaggio in edge://policy

Esempio di messaggio di stato dell’errore: "Questo valore del criterio è ignorato perché l’attivazione di Monitoraggio password richiede il consenso dei singoli utenti. Puoi chiedere agli utenti dell’organizzazione di passare a Impostazioni > Profilo > Password e attivare la funzionalità."

Abilitazione consigliata: se il criterio è impostato su abilitazione consigliata, l’interfaccia utente in Impostazioni rimarrà in stato “Disattivato”, ma sarà visibile l’icona sincronia il cui testo verrà visualizzato al passaggio del mouse: "La tua organizzazione consiglia un valore specifico per questa impostazione e hai scelto un valore diverso"

Disabilitazione obbligatoria e consigliata: questi stati funzioneranno in maniera normale, e agli utenti verranno mostrati i sottotitoli soliti.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PasswordMonitorAllowed
  - Nome GP: Consenti l’invio di avvisi agli utenti se le password non sono più sicure
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Protezione e gestione password
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Protezione e gestione password
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: PasswordMonitorAllowed
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PasswordProtectionChangePasswordURL
  #### Configura l'URL di modifica password
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Configura l'URL per la modifica della password (solo schemi HTTP e HTTPS).

Il servizio password di protezione reindirizza gli utenti a questo URL per modificare la password a seguito dell'avviso visualizzato nel browser.

Se abiliti questo criterio, il servizio password di protezione reindirizzerà gli utenti a questo URL per modificare la password.

Se disabiliti o non configuri questo criterio, il servizio password di protezione non reindirizzerà gli utenti a un URL per modificare la password.

Questo criterio è disponibile solo per le istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PasswordProtectionChangePasswordURL
  - Nome GP: Configura l'URL di modifica password
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Protezione e gestione password
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: PasswordProtectionChangePasswordURL
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"https://contoso.com/change_password.html"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PasswordProtectionChangePasswordURL
  - Valore di esempio:
``` xml
<string>https://contoso.com/change_password.html</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PasswordProtectionLoginURLs
  #### Configura l'elenco degli URL di accesso aziendali in cui il servizio di protezione password deve acquisire gli hash con salting di una password
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Configura l'elenco degli URL di accesso aziendali (solo schemi HTTP e HTTPS) in cui Microsoft Edge deve acquisire gli hash salati delle password e usarli per il rilevamento delle password riutilizzate.

Se abiliti questo criterio, il servizio password di protezione acquisisce le impronte digitali delle password negli URL definiti.

Se disabiliti questo criterio o non lo configuri, le impronte digitali delle password non vengono acquisite.

Questo criterio è disponibile solo nelle istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PasswordProtectionLoginURLs
  - Nome GP: Configura l'elenco degli URL di accesso aziendali in cui il servizio di protezione password deve acquisire gli hash con salting di una password
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Protezione e gestione password
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\1 = "https://contoso.com/login.html"
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\2 = "https://login.contoso.com"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PasswordProtectionLoginURLs
  - Valore di esempio:
``` xml
<array>
  <string>https://contoso.com/login.html</string>
  <string>https://login.contoso.com</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PasswordProtectionWarningTrigger
  #### Configura il trigger di avviso di protezione password
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente di controllare quando attivare l'avviso di protezione password. La protezione password avvisa gli utenti quando riutilizzano la propria password protetta su siti potenzialmente sospetti.

Puoi utilizzare i criteri [PasswordProtectionLoginURLs](#passwordprotectionloginurls) e [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)  per configurare la password da proteggere.

Esenzioni: le password per i siti elencati in [PasswordProtectionLoginURLs](#passwordprotectionloginurls) e [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl), nonché per i siti elencati in [SmartScreenAllowListDomains](#smartscreenallowlistdomains), non attivano un avviso di protezione della password.

Imposta su "PasswordProtectionWarningOff" per non visualizzare avvisi della protezione password.

Imposta su "PasswordProtectionWarningOnPasswordReuse" per visualizzare gli avvisi della protezione password quando l'utente riutilizza la propria password protetta su un sito non autorizzato.

Se disabiliti o non configuri questi criteri, il trigger di avviso non viene visualizzato.

Mappatura opzioni criteri:

* PasswordProtectionWarningOff (0) = L'avviso di protezione della password è disattivato

* PasswordProtectionWarningOnPasswordReuse (1) = L'avviso di protezione delle password viene attivato dal riutilizzo delle password

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PasswordProtectionWarningTrigger
  - Nome GP: Configura il trigger di avviso di protezione password
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Protezione e gestione password
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: PasswordProtectionWarningTrigger
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PasswordProtectionWarningTrigger
  - Valore di esempio:
``` xml
<integer>1</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ## Provider di ricerca predefinito policies

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultSearchProviderEnabled
  #### Abilita il provider di ricerca predefinito
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente l'uso di un provider di ricerca predefinito.

Se abiliti questo criterio, gli utenti potranno cercare un termine digitandolo nella barra degli indirizzi (purché non stia digitando un URL).

Puoi specificare il provider di ricerca predefinito da utilizzare abilitando il resto dei criteri di ricerca predefiniti. Se questi criteri vengono lasciati vuoti (non configurati), gli utenti potranno scegliere il provider predefinito.

Se disabiliti questo criterio, gli utenti non potranno eseguire la ricerca dalla barra degli indirizzi.

Se abiliti o disabiliti questo criterio, gli utenti non potranno modificarli o eseguirne l'override.

Se non configuri questo criterio, il provider di ricerca predefinito sarà abilitato e gli utenti potranno scegliere il provider di ricerca predefinito e impostare l'elenco di provider di ricerca.

Questo criterio è disponibile solo per le istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.

A partire da Microsoft Edge 84, puoi impostarlo come criterio consigliato.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultSearchProviderEnabled
  - Nome GP: Abilita il provider di ricerca predefinito
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Provider di ricerca predefinito
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Provider di ricerca predefinito
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: DefaultSearchProviderEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultSearchProviderEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultSearchProviderEncodings
  #### Codifiche del provider di ricerca predefinito
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica le codifiche dei caratteri supportate dal provider di ricerca. Le codifiche sono nomi di tabella codici, come UTF-8, GB2312 e ISO-8859-1. Vengono provate nell'ordine indicato.

Questo criterio è facoltativo. Se non configurato, verrà utilizzata l'impostazione predefinita UTF-8.

Questo criterio viene applicato solo se abiliti i criteri [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partire da Microsoft Edge 84, puoi impostarlo come criterio consigliato. Se l’utente ha già impostato un provider di ricerca predefinito, il provider di ricerca predefinito configurato da questo criterio consigliato non verrà aggiunto all’elenco dei provider di ricerca tra cui l’utente può scegliere. Se si tratta del comportamento desiderato, usa il criterio [ManagedSearchEngines](#managedsearchengines).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultSearchProviderEncodings
  - Nome GP: Codifiche del provider di ricerca predefinito
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Provider di ricerca predefinito
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Provider di ricerca predefinito
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati\DefaultSearchProviderEncodings
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\1 = "UTF-8"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\2 = "UTF-16"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\3 = "GB2312"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\4 = "ISO-8859-1"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultSearchProviderEncodings
  - Valore di esempio:
``` xml
<array>
  <string>UTF-8</string>
  <string>UTF-16</string>
  <string>GB2312</string>
  <string>ISO-8859-1</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultSearchProviderImageURL
  #### Specifica la funzionalità di ricerca per immagini per il provider di ricerca predefinito
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica l'URL per il motore di ricerca utilizzato per la ricerca dell'immagine. Le richieste di ricerca vengono inviate tramite il metodo GET.

Questo criterio è facoltativo. Se non lo configuri, la ricerca di immagini non è disponibile.

Specifica l'URL di ricerca dell'immagine di Bing come:
"{bing:baseURL}images/detail/search?iss=sbiupload&FORM=ANCMS1#enterInsights".

Specifica l'URL di ricerca dell'immagine di Google come: "{google:baseURL}searchbyimage/upload".

Vedi il criterio [DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams) per finire la configurazione della ricerca dell'immagine.

Questo criterio è applicato solo se abiliti anche i criteri [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partire da Microsoft Edge 84, puoi impostarlo come criterio consigliato. Se l’utente ha già impostato un provider di ricerca predefinito, il provider di ricerca predefinito configurato da questo criterio consigliato non verrà aggiunto all’elenco dei provider di ricerca tra cui l’utente può scegliere. Se si tratta del comportamento desiderato, usa il criterio [ManagedSearchEngines](#managedsearchengines).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultSearchProviderImageURL
  - Nome GP: Specifica la funzionalità di ricerca per immagini per il provider di ricerca predefinito
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Provider di ricerca predefinito
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Provider di ricerca predefinito
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: DefaultSearchProviderImageURL
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"https://search.contoso.com/searchbyimage/upload"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultSearchProviderImageURL
  - Valore di esempio:
``` xml
<string>https://search.contoso.com/searchbyimage/upload</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultSearchProviderImageURLPostParams
  #### Parametri per l'URL di un'immagine che utilizza POST
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Se abiliti questo criterio, vengono specificati i parametri utilizzati quando si esegue la ricerca di immagini con POST. Il criterio consiste in coppie nome/valore delimitate da virgole. Se un valore è un parametro di modello, come {imageThumbnail} nel precedente esempio, verrà sostituito con i dati dell'anteprima dell'immagine reale. Questo criterio viene applicato solo se abiliti i criteri [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

Specifica i parametri di pubblicazione dell'URL di ricerca immagini di Bing come:
"imageBin={google:imageThumbnailBase64}".

Specifica i parametri di pubblicazione dell'URL di ricerca dell'immagine di Google come:
"encoded_image={google:imageThumbnail},image_url={google:imageURL},sbisrc={google:imageSearchSource},original_width={google:imageOriginalWidth},original_height={google:imageOriginalHeight}".

Se non imposti questo criterio, le richieste di ricerca dell'immagine vengono inviate tramite il metodo GET.

A partire da Microsoft Edge 84, puoi impostarlo come criterio consigliato. Se l’utente ha già impostato un provider di ricerca predefinito, il provider di ricerca predefinito configurato da questo criterio consigliato non verrà aggiunto all’elenco dei provider di ricerca tra cui l’utente può scegliere. Se si tratta del comportamento desiderato, usa il criterio [ManagedSearchEngines](#managedsearchengines).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultSearchProviderImageURLPostParams
  - Nome GP: Parametri per l'URL di un'immagine che utilizza POST
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Provider di ricerca predefinito
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Provider di ricerca predefinito
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: DefaultSearchProviderImageURLPostParams
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"content={imageThumbnail},url={imageURL},sbisrc={SearchSource}"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultSearchProviderImageURLPostParams
  - Valore di esempio:
``` xml
<string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultSearchProviderKeyword
  #### Parola chiave del provider di ricerca predefinito
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica la parola chiave, che è il collegamento utilizzato nella barra degli indirizzi per attivare la ricerca per questo provider.

Questo criterio è facoltativo. Se non lo configuri, nessuna parola chiave attiverà il provider di ricerca.

Questo criterio viene applicato solo se abiliti i criteri [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partire da Microsoft Edge 84, puoi impostarlo come criterio consigliato. Se l’utente ha già impostato un provider di ricerca predefinito, il provider di ricerca predefinito configurato da questo criterio consigliato non verrà aggiunto all’elenco dei provider di ricerca tra cui l’utente può scegliere. Se si tratta del comportamento desiderato, usa il criterio [ManagedSearchEngines](#managedsearchengines).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultSearchProviderKeyword
  - Nome GP: Parola chiave del provider di ricerca predefinito
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Provider di ricerca predefinito
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Provider di ricerca predefinito
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: DefaultSearchProviderKeyword
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"mis"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultSearchProviderKeyword
  - Valore di esempio:
``` xml
<string>mis</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultSearchProviderName
  #### Nome del provider di ricerca predefinito
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica il nome del provider di ricerca predefinito.

Se abiliti questo criterio, verrà impostato il nome del provider di ricerca predefinito.

Se non abiliti questo criterio o lo lasci vuoto, verrà utilizzato il nome host specificato dall'URL di ricerca.

[DefaultSearchProviderName](#defaultsearchprovidername) deve essere impostato su un provider di ricerca crittografato approvato dall'organizzazione che corrisponde al provider di ricerca crittografato impostato in DTBC-0008. Questo criterio viene applicato solo se abiliti i criteri [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partire da Microsoft Edge 84, puoi impostarlo come criterio consigliato. Se l’utente ha già impostato un provider di ricerca predefinito, il provider di ricerca predefinito configurato da questo criterio consigliato non verrà aggiunto all’elenco dei provider di ricerca tra cui l’utente può scegliere. Se si tratta del comportamento desiderato, usa il criterio [ManagedSearchEngines](#managedsearchengines).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultSearchProviderName
  - Nome GP: Nome del provider di ricerca predefinito
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Provider di ricerca predefinito
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Provider di ricerca predefinito
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: DefaultSearchProviderName
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"My Intranet Search"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultSearchProviderName
  - Valore di esempio:
``` xml
<string>My Intranet Search</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultSearchProviderSearchURL
  #### URL di ricerca del provider di ricerca predefinito
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica l'URL del motore di ricerca utilizzato per una ricerca predefinita. L'URL contiene la stringa '{searchTerms}', che viene sostituita in fase di query con i termini che l'utente sta cercando.

Specifica l'URL di ricerca di Bing come:

'{bing:baseURL}search?q={searchTerms}'.

Specifica l'URL di ricerca Google come: '{google:baseURL}search?q={searchTerms}&{google:RLZ}{google:originalQueryForSuggestion}{google:assistedQueryStats}{google:searchFieldtrialParameter}{google:searchClient}{google:sourceId}ie={inputEncoding}'.

Questo criterio è obbligatorio quando abiliti i criteri [DefaultSearchProviderEnabled](#defaultsearchproviderenabled); se non abiliti quest’ultimo, questo criterio viene ignorato.

A partire da Microsoft Edge 84, puoi impostarlo come criterio consigliato. Se l’utente ha già impostato un provider di ricerca predefinito, il provider di ricerca predefinito configurato da questo criterio consigliato non verrà aggiunto all’elenco dei provider di ricerca tra cui l’utente può scegliere. Se si tratta del comportamento desiderato, usa il criterio [ManagedSearchEngines](#managedsearchengines).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultSearchProviderSearchURL
  - Nome GP: URL di ricerca del provider di ricerca predefinito
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Provider di ricerca predefinito
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Provider di ricerca predefinito
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: DefaultSearchProviderSearchURL
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"https://search.contoso.com/search?q={searchTerms}"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultSearchProviderSearchURL
  - Valore di esempio:
``` xml
<string>https://search.contoso.com/search?q={searchTerms}</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultSearchProviderSuggestURL
  #### URL del provider di ricerca predefinito per i suggerimenti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica l'URL del motore di ricerca utilizzato per fornire suggerimenti per la ricerca. L'URL contiene la stringa "{searchTerms}", che viene sostituita in fase di query con il testo che l'utente ha immesso finora.

Questo criterio è facoltativo. Se non lo configuri, gli utenti non visualizzeranno i suggerimenti di ricerca; i suggerimenti verranno visualizzati dalla loro cronologia esplorazione e dai preferiti.

L'URL per i suggerimenti di Bing può essere specificato come:

"{bing:baseURL}qbox?query={searchTerms}".

L'URL per i suggerimenti di Google può essere specificato come: "{google:baseURL}complete/search?output=chrome&q={searchTerms}".

Questo criterio viee applicato solo se abiliti i criteri [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partire da Microsoft Edge 84, puoi impostarlo come criterio consigliato. Se l’utente ha già impostato un provider di ricerca predefinito, il provider di ricerca predefinito configurato da questo criterio consigliato non verrà aggiunto all’elenco dei provider di ricerca tra cui l’utente può scegliere. Se si tratta del comportamento desiderato, usa il criterio [ManagedSearchEngines](#managedsearchengines).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultSearchProviderSuggestURL
  - Nome GP: URL del provider di ricerca predefinito per i suggerimenti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Provider di ricerca predefinito
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Provider di ricerca predefinito
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: DefaultSearchProviderSuggestURL
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"https://search.contoso.com/suggest?q={searchTerms}"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultSearchProviderSuggestURL
  - Valore di esempio:
``` xml
<string>https://search.contoso.com/suggest?q={searchTerms}</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NewTabPageSearchBox
  #### Configura l'esperienza della casella di ricerca della nuova scheda
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 85 o in seguito

  #### Descrizione
  Puoi configurare la casella di ricerca della nuova scheda per utilizzare "Casella di ricerca (consigliata)" o "Barra degli indirizzi" per cercare nuove schede. Questo criterio funziona solo se imposti il motore di ricerca su un valore diverso da Bing impostando le seguenti due politiche: [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

Se disabiliti o non configuri questo criterio e:

- Se il motore di ricerca predefinito della barra degli indirizzi è Bing, la nuova scheda utilizza la casella di ricerca per cercare nuove schede.
 - Se il motore di ricerca predefinito della barra degli indirizzi non è Bing, agli utenti viene offerta una scelta aggiuntiva (utilizzare "Barra degli indirizzi") durante la ricerca in nuove schede.


 Se abiliti questo criterio e lo imposti su:

 - "Casella di ricerca (consigliata)" ('bing'), la nuova scheda utilizza la casella di ricerca per cercare nuove schede.
 - "Barra degli indirizzi" ("reindirizzamento"), la casella di ricerca della nuova scheda utilizza la barra degli indirizzi per cercare nuove schede.

Mappatura opzioni criteri:

* bing (bing) = Casella di ricerca (scelta consigliata)

* redirect (redirect) = Barra degli indirizzi

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: NewTabPageSearchBox
  - Nome GP: Configura l'esperienza della casella di ricerca della nuova scheda
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Provider di ricerca predefinito
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Provider di ricerca predefinito
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: NewTabPageSearchBox
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"bing"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: NewTabPageSearchBox
  - Valore di esempio:
``` xml
<string>bing</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ## Server proxy policies

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ProxyBypassList
  #### Configura le regole di bypass proxy
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Definisce un elenco di host per cui Microsoft Edge ignora qualsiasi proxy.

Questi criteri vengono applicati solo se hai selezionato "Utilizza server proxy fissi" nei criteri [ProxyMode](#proxymode). Se hai selezionato altre modalità per la configurazione dei criteri del proxy, non abilitare o configurare questi criteri.

Se abiliti questi criteri, puoi creare un elenco di host per cui Microsoft Edge non utilizza un proxy.

Se non configuri questi criteri, non viene creato alcun elenco di host per cui Microsoft Edge ignora un proxy. Lascia non configurati questi criteri se hai specificato un altro metodo per l'impostazione dei criteri del proxy.

Per esempi più dettagliati, vai a [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ProxyBypassList
  - Nome GP: Configura le regole di bypass proxy
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Server proxy
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ProxyBypassList
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"https://www.contoso.com, https://www.fabrikam.com"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ProxyBypassList
  - Valore di esempio:
``` xml
<string>https://www.contoso.com, https://www.fabrikam.com</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ProxyMode
  #### Configura le impostazioni del server proxy
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica le impostazioni del server proxy utilizzate da Microsoft Edge. Se abiliti questi criteri, gli utenti non possono modificare le impostazioni del proxy.

Se scegli di non utilizzare mai un server proxy e di utilizzare sempre la connessione diretta, tutte le altre opzioni vengono ignorate.

Se scegli di utilizzare le impostazioni del proxy del sistema, tutte le altre opzioni vengono ignorate.

Se scegli di rilevare automaticamente il server proxy, tutte le altre opzioni vengono ignorate.

Se scegli una modalità del server proxy fissa, puoi specificare altre opzioni in "[ProxyServer](#proxyserver)" e in "Elenco delle regole di bypass proxy separate da virgole".

Se scegli di utilizzare uno script proxy .pac, devi specificare l'URL dello script in "URL di un file proxy con estensione .pac".

Per esempi dettagliati, visita [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

Se abiliti questi criteri, Microsoft Edge ignora tutte le opzioni relative al proxy specificate dalla riga di comando.

Se non configuri questi criteri, gli utenti possono scegliere le proprie impostazioni del proxy.

Mappatura opzioni criteri:

* ProxyDisabled (direct) = Non usare mai un proxy

* ProxyAutoDetect (auto_detect) = Rileva automaticamente le impostazioni del proxy

* ProxyPacScript (pac_script) = Utilizza uno script proxy .pac

* ProxyFixedServers (fixed_servers) = Utilizza server proxy fissi

* ProxyUseSystem (system) = Utilizza Impostazioni proxy del sistema

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ProxyMode
  - Nome GP: Configura le impostazioni del server proxy
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Server proxy
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ProxyMode
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"direct"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ProxyMode
  - Valore di esempio:
``` xml
<string>direct</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ProxyPacUrl
  #### Imposta l'URL del file .pac del proxy
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica l'URL di un file di configurazione automatica del proxy (PAC).

Questi criteri vengono applicati solo hai selezionato "Utilizza uno script proxy .pac" nei criteri [ProxyMode](#proxymode). Se hai selezionato altre modalità per la configurazione dei criteri del proxy, non abilitare o configurare questi criteri.

Se abiliti questi criteri, puoi specificare l'URL di un file PAC che definisca il modo in cui il browser sceglie automaticamente il server proxy appropriato per il recupero di un determinato sito Web.

Se disabiliti o non configuri questi criteri, non è specificato alcun file PAC. Lascia non configurati questi criteri se hai specificato un altro metodo per l'impostazione dei criteri del proxy.

Per esempi dettagliati, vedi [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ProxyPacUrl
  - Nome GP: Imposta l'URL del file .pac del proxy
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Server proxy
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ProxyPacUrl
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"https://internal.contoso.com/example.pac"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ProxyPacUrl
  - Valore di esempio:
``` xml
<string>https://internal.contoso.com/example.pac</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ProxyServer
  #### Configura l'indirizzo o l'URL del server proxy
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica l'URL del server proxy.

Questi criteri vengono applicati solo se hai selezionato "Utilizza server proxy fissi" nei criteri [ProxyMode](#proxymode). Se hai selezionato altre modalità per la configurazione dei criteri del proxy, non abilitare o configurare questi criteri.

Se abiliti questi criteri, il server proxy configurato da questi criteri viene utilizzato per tutti gli URL.

Se disabiliti o non configuri questi criteri, gli utenti possono scegliere le proprie impostazioni del proxy in questa modalità proxy. Lascia non configurati questi criteri se hai specificato un altro metodo per l'impostazione dei criteri del proxy.

Per altre opzioni ed esempi dettagliati, vedi [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ProxyServer
  - Nome GP: Configura l'indirizzo o l'URL del server proxy
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Server proxy
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ProxyServer
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"123.123.123.123:8080"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ProxyServer
  - Valore di esempio:
``` xml
<string>123.123.123.123:8080</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ProxySettings
  #### Impostazioni proxy
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Configura le impostazioni del proxy per Microsoft Edge.

Se abiliti questi criteri, Microsoft Edge ignora tutte le opzioni relative al proxy specificate dalla riga di comando.

Se non configuri questi criteri, gli utenti possono scegliere le proprie impostazioni del proxy.

Questi criteri sostituiscono i singoli criteri seguenti:

[ProxyMode](#proxymode)
[ProxyPacUrl](#proxypacurl)
[ProxyServer](#proxyserver)
[ProxyBypassList](#proxybypasslist)

Il campo ProxyMode consente di specificare il server proxy utilizzato da Microsoft Edge e impedisce agli utenti di modificare le impostazioni del proxy.

Il campo ProxyPacUrl  è l'URL di un file .pac del proxy.

Il campo ProxyServer è l'URL del server proxy.

Il campo ProxyBypassList è un elenco di host proxy che vengono ignorati da Microsoft Edge.

Se scegli il valore "direct" come [ProxyMode](#proxymode), non viene mai usato un proxy e tutti gli altri campi vengono ignorati.

Se scegli il valore "system" come [ProxyMode](#proxymode), viene utilizzato il proxy del sistema e tutti gli altri campi vengono ignorati.

Se scegli il valore "auto_detect" come [ProxyMode](#proxymode), tutti gli altri campi vengono ignorati.

Se scegli il valore "fixed_server" come [ProxyMode](#proxymode), vengono utilizzati i campi [ProxyServer](#proxyserver) e [ProxyBypassList](#proxybypasslist).

Se scegli il valore "pac_script" come [ProxyMode](#proxymode), vengono utilizzati i campi "'ProxyPacUrl" e [ProxyBypassList](#proxybypasslist).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Dizionario

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ProxySettings
  - Nome GP: Impostazioni proxy
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Server proxy
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ProxySettings
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {
  "ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", 
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ProxySettings
  - Valore di esempio:
``` xml
<key>ProxySettings</key>
<dict>
  <key>ProxyBypassList</key>
  <string>https://www.example1.com,https://www.example2.com,https://internalsite/</string>
  <key>ProxyMode</key>
  <string>direct</string>
  <key>ProxyPacUrl</key>
  <string>https://internal.site/example.pac</string>
  <key>ProxyServer</key>
  <string>123.123.123.123:8080</string>
</dict>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ## Stampa policies

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultPrinterSelection
  #### Regole di selezione della stampante predefinita
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Sostituisce le regole di selezione della stampante predefinita di Microsoft Edge. Questi criteri determinano le regole per la selezione della stampante predefinita in Microsoft Edge che viene effettuata la prima volta che un utente tenta di stampare una pagina.

Quando questi criteri sono impostati, Microsoft Edge tenta di trovare una stampante che corrisponda a tutti gli attributi specificati e la utilizza come stampante predefinita. Se sono presenti più stampanti che soddisfano i criteri, viene utilizzata la prima stampante corrispondente.

Se non configuri questi criteri o nessuna stampante corrispondente viene trovata entro il timeout, l'impostazione predefinita è la stampante PDF incorporata o nessuna stampante, se la stampante PDF non è disponibile.

Il valore viene analizzato come un oggetto JSON, in base allo schema seguente: { "type": "object", "properties": { "idPattern": { "description": "Regular expression to match printer id.", "type": "string" }, "namePattern": { "description": "Regular expression to match printer display name.", "type": "string" } } }

L'omissione di un campo indica che tutti i valori corrispondono. Se ad esempio non specifichi la connettività, Anteprima di stampa inizia a cercare tutti i tipi di stampanti locali. I modelli di espressione regolare devono seguire la sintassi RegExp JavaScript e le corrispondenze rispettano la differenza tra maiuscolo e minuscolo.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultPrinterSelection
  - Nome GP: Regole di selezione della stampante predefinita
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Stampa
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DefaultPrinterSelection
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"{ \"idPattern\": \".*public\", \"namePattern\": \".*Color\" }"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultPrinterSelection
  - Valore di esempio:
``` xml
<string>{ "idPattern": ".*public", "namePattern": ".*Color" }</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PrintHeaderFooter
  #### Stampa intestazioni e piè di pagina
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Forza l'attivazione o la disattivazione di 'intestazioni e piè di pagina' nella finestra di dialogo di stampa.

Se non configuri questi criteri, gli utenti possono decidere se stampare intestazioni e piè di pagina.

Se disabiliti questi criteri, gli utenti non possono stampare intestazioni e piè di pagina.

Se abiliti questi criteri, gli utenti stampano sempre intestazioni e piè di pagina.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PrintHeaderFooter
  - Nome GP: Stampa intestazioni e piè di pagina
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Stampa
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Stampa
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: PrintHeaderFooter
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PrintHeaderFooter
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PrintPreviewUseSystemDefaultPrinter
  #### Imposta stampante predefinita del sistema come stampante predefinita
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Indica a Microsoft Edge di utilizzare la stampante predefinita di sistema come opzione predefinita nella finestra Anteprima di stampa anziché la stampante utilizzata più di recente.

Se disabiliti o non configuri questi criteri, Anteprima di stampa utilizza la stampante utilizzata più di recente come scelta di destinazione predefinita.

Se abiliti questi criteri, Anteprima di stampa utilizza la stampante predefinita del sistema operativo come scelta di destinazione predefinita.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PrintPreviewUseSystemDefaultPrinter
  - Nome GP: Imposta stampante predefinita del sistema come stampante predefinita
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Stampa
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/Stampa
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: PrintPreviewUseSystemDefaultPrinter
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PrintPreviewUseSystemDefaultPrinter
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PrintingEnabled
  #### Abilita stampa
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Abilita la stampa in Microsoft Edge e impedisce agli utenti di modificare questa impostazione.

Se abiliti o non configuri questi criteri, gli utenti possono stampare.

Se disabiliti questi criteri, gli utenti non possono stampare da Microsoft Edge. La stampa è disabilitata nel menu chiave inglese, nelle estensioni, nelle applicazioni JavaScript e così via. Gli utenti possono comunque stampare dai plug-in che ignorano Microsoft Edge durante la stampa. Ad esempio, alcune applicazioni Adobe Flash hanno l'opzione di stampa nel menu di scelta rapida, che non è coperto da questi criteri.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PrintingEnabled
  - Nome GP: Abilita stampa
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Stampa
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: PrintingEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PrintingEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PrintingPaperSizeDefault
  #### Dimensioni predefinite pagina di stampa
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Sostituisce le dimensioni predefinite della pagina di stampa..

name  deve contenere uno dei formati elencati o "Custom" se la dimensione dei fogli richiesti non è inclusa nell'elenco. Se è specificato il valore ' Custom ' custom_size è necessario specificare la proprietà. Descrive l'altezza e la larghezza desiderate in micrometri. Non specificare diversamentecustom_size proprietà. Criteri che violano queste regole vengono ignorati.

Se la dimensione della pagina non è disponibile nella stampante scelta dall'utente, questo criterio verrà ignorato.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Dizionario

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PrintingPaperSizeDefault
  - Nome GP: Dimensioni predefinite pagina di stampa
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Stampa
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: PrintingPaperSizeDefault
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\PrintingPaperSizeDefault = {
  "custom_size": {
    "height": 297000, 
    "width": 210000
  }, 
  "name": "custom"
}
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PrintingPaperSizeDefault
  - Valore di esempio:
``` xml
<key>PrintingPaperSizeDefault</key>
<dict>
  <key>custom_size</key>
  <dict>
    <key>height</key>
    <integer>297000</integer>
    <key>width</key>
    <integer>210000</integer>
  </dict>
  <key>name</key>
  <string>custom</string>
</dict>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### UseSystemPrintDialog
  #### Stampa utilizzando la finestra di dialogo Stampa del sistema
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Mostra la finestra di dialogo di stampa del sistema anziché l'anteprima di stampa.

Se abiliti questi criteri, Microsoft Edge apre la finestra di dialogo di stampa del sistema anziché l'anteprima di stampa incorporata quando un utente stampa una pagina.

Se non configuri questi criteri, i comandi di stampa attivano la schermata di anteprima di stampa di Microsoft Edge.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: UseSystemPrintDialog
  - Nome GP: Stampa utilizzando la finestra di dialogo Stampa del sistema
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/Stampa
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: UseSystemPrintDialog
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: UseSystemPrintDialog
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ## Additional policies

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AddressBarMicrosoftSearchInBingProviderEnabled
  #### Abilita i suggerimenti di Microsoft Search in Bing nella barra degli indirizzi
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 81 o in seguito

  #### Descrizione
  Abili la visualizzazione dei suggerimenti pertinenti di Microsoft Search in Bing nell'elenco dei suggerimenti della barra degli indirizzi quando l'utente vi digita una stringa di ricerca. Se abiliti o non configuri questi criteri, gli utenti possono visualizzare i risultati interni generati da Microsoft Search in Bing nell'elenco dei suggerimenti della barra degli indirizzi di Microsoft Edge. Per visualizzare i risultati di Microsoft Search in Bing, l'utente deve aver effettuato l'accesso a Microsoft Edge con il suo account Azure AD per tale organizzazione.
Se disabiliti questi criteri, gli utenti non possono visualizzare i risultati interni nell'elenco dei suggerimenti della barra degli indirizzi di Microsoft Edge.
Se hai abilitato il set di criteri che forza un provider di ricerca predefinito ([DefaultSearchProviderEnabled](#defaultsearchproviderenabled), [DefaultSearchProviderName](#defaultsearchprovidername) and [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)) e il provider di ricerca specificato non è Bing, questi criteri non sono applicabili e i suggerimenti di Microsoft Search in Bing non saranno inclusi nell'elenco dei suggerimenti della barra degli indirizzi.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AddressBarMicrosoftSearchInBingProviderEnabled
  - Nome GP: Abilita i suggerimenti di Microsoft Search in Bing nella barra degli indirizzi
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AddressBarMicrosoftSearchInBingProviderEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AddressBarMicrosoftSearchInBingProviderEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AdsSettingForIntrusiveAdsSites
  #### Impostazione degli annunci per i siti con annunci intrusivi
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 78 o in seguito

  #### Descrizione
  Verifica se gli annunci sono bloccati nei siti con annunci intrusivi.

Mappatura opzioni criteri:

* AllowAds (1) = Consenti gli annunci per tutti i siti

* BlockAds (2) = Blocca gli annunci per i siti con annunci intrusivi (valore predefinito)

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AdsSettingForIntrusiveAdsSites
  - Nome GP: Impostazione degli annunci per i siti con annunci intrusivi
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AdsSettingForIntrusiveAdsSites
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AdsSettingForIntrusiveAdsSites
  - Valore di esempio:
``` xml
<integer>1</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AllowDeletingBrowserHistory
  #### Abilita eliminazione cronologia del browser e download
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente l'eliminazione della cronologia del browser e della cronologia di download e impedisce agli utenti di modificare questa impostazione.

Tieni presente che anche con questi criteri disabilitati, non viene garantito il mantenimento della cronologia esplorazioni e download: gli utenti possono modificare o eliminare direttamente i file del database della cronologia e il browser stesso potrebbe rimuovere (in base alla scadenza) o archiviare alcuni o tutti gli elementi della cronologia in qualsiasi momento.

Se abiliti o non configuri questi criteri, gli utenti possono eliminare la cronologia esplorazioni e download.

Se disabiliti o non configuri questi criteri, gli utenti non possono eliminare la cronologia esplorazioni e download.

Se abiliti questi criteri, non abilitare i criteri [ClearBrowsingDataOnExit](#clearbrowsingdataonexit), poiché entrambi vengono utilizzati per l'eliminazione dei dati. Se abiliti entrambi, i criteri [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) sono prioritari e tutti i dati vengono eliminati quando Microsoft Edge viene chiuso, indipendentemente dalla configurazione di questi criteri.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AllowDeletingBrowserHistory
  - Nome GP: Abilita eliminazione cronologia del browser e download
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AllowDeletingBrowserHistory
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AllowDeletingBrowserHistory
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AllowFileSelectionDialogs
  #### Consenti le finestre di dialogo di selezione file
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consenti l'accesso ai file locali permettendo a Microsoft Edge di visualizzare le finestre di dialogo di selezione file.

Se abiliti o non configuri questi criteri, gli utenti possono aprire le finestre di dialogo di selezione file come di consueto.

Se disabiliti questi criteri, ogni volta che l'utente esegue un'azione che attiva una finestra di selezione file (come l'importazione di preferiti, il caricamento di file o il salvataggio di collegamenti), viene visualizzato un messaggio e si presume che l'utente abbia fatto clic su Annulla nella finestra di dialogo di selezione file.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AllowFileSelectionDialogs
  - Nome GP: Consenti le finestre di dialogo di selezione file
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AllowFileSelectionDialogs
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AllowFileSelectionDialogs
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AllowPopupsDuringPageUnload
  #### Consente a una pagina di visualizzare i popup durante lo scaricamento
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 78 o in seguito

  #### Descrizione
  Questo criterio consente ad un amministratore di indicare che una pagina può visulizzare i popup durante lo scaricamento.

Quando i criteri sono abilitati, alle pagine viene consentito di mostrare i popup mentre si scaricano.

Quando i criteri sono disabilitati o non sono impostati, alle pagine non è consentito di mostrare i popup mentre vengono scaricati. Ciò avviene grazie alla specifica: (https://html.spec.whatwg.org/#apis-for-creating-and-navigating-browsing-contexts-by-name).

Questi criteri verranno rimossi in futuro.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AllowPopupsDuringPageUnload
  - Nome GP: Consente a una pagina di visualizzare i popup durante lo scaricamento
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AllowPopupsDuringPageUnload
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AllowPopupsDuringPageUnload
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AllowSurfGame
  #### Consenti gioco di surf
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 83 o in seguito

  #### Descrizione
  Se disabiliti questi criteri, gli utenti non potranno riprodurre il gioco di surf quando il dispositivo è offline o se l'utente passa a edge://surf.

Se abiliti o non configuri questi criteri, gli utenti possono riprodurre il gioco di surf.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AllowSurfGame
  - Nome GP: Consenti gioco di surf
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AllowSurfGame
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AllowSurfGame
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AllowSyncXHRInPageDismissal
  #### Consenti alle pagine di inviare richieste XHR sincrone durante la chiusura della pagina (deprecato)
  >DEPRECAtO: questi criteri sono deprecati. Sono attualmente supportati ma diventeranno obsoleti in una versione futura.
  
  #### Versioni supportate:
  - Su Windows e macOS dal 79 o in seguito

  #### Descrizione
  Questi criteri sono deprecati perché sono intesi solo come meccanismo a breve termine per dare alle aziende più tempo per aggiornare il loro contenuto Web se e quando si ritiene che sia incompatibile con la modifica per impedire richieste XHR sincrone durante l'eliminazione della pagina. Non funzionerà in Microsoft Edge dalla versione 88.

Questi criteri consentono di specificare che una pagina può inviare richieste XHR sincrone durante l'eliminazione della pagina.

Se abiliti questi criteri, le pagine possono inviare richieste XHR sincrone durante l'eliminazione della pagina.

Se disabiliti o non configuri questi criteri, le pagine non possono inviare richieste XHR sincrone durante l'eliminazione della pagina.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AllowSyncXHRInPageDismissal
  - Nome GP: Consenti alle pagine di inviare richieste XHR sincrone durante la chiusura della pagina (deprecato)
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AllowSyncXHRInPageDismissal
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AllowSyncXHRInPageDismissal
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AllowTokenBindingForUrls
  #### Configurare l'elenco dei siti con cui Microsoft Edge tenterà di stabilire un binding di token.
  
  
  #### Versioni supportate:
  - Su Windows dal 83 o successiva

  #### Descrizione
  Configura l'elenco di modelli URL per i siti con cui il browser tenterà di eseguire il protocollo di binding token.
Per i domini nell'elenco, il browser invierà il ClientHello del binding token nell'handshake TLS (vedi https://tools.ietf.org/html/rfc8472).
Se il server risponde con una risposta ServerHello valida, il browser creerà e invierà i messaggi di binding token sulle successive richieste https. Vedi https://tools.ietf.org/html/rfc8471 per ulteriori informazioni.

Se l'elenco è vuoto, il binding token verrà disabilitato.

Questo criterio è disponibile solo sui dispositivi Windows 10 con la funzionalità di modalità protetta virtuale.

A partire da Microsoft Edge 86, questo criterio non supporterà più l'aggiornamento dinamico.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AllowTokenBindingForUrls
  - Nome GP: Configurare l'elenco dei siti con cui Microsoft Edge tenterà di stabilire un binding di token.
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\2 = "[*.]mydomain2.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\3 = "[*.].mydomain2.com"

```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AllowTrackingForUrls
  #### Configura le eccezioni di prevenzione del monitoraggio per siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 78 o in seguito

  #### Descrizione
  Configura l'elenco dei modelli di URL esclusi dalla prevenzione del monitoraggio.

Se configuri questi criteri, l'elenco dei modelli di URL configurati viene escluso dalla prevenzione del monitoraggio.

Se non configuri questi criteri, per tutti i siti viene utilizzato il valore predefinito globale dei criteri "Blocca il rilevamento dell'attività di esplorazione Web degli utenti" (se impostati) o la configurazione personale dell'utente.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AllowTrackingForUrls
  - Nome GP: Configura le eccezioni di prevenzione del monitoraggio per siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AllowTrackingForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AlternateErrorPagesEnabled
  #### Suggerisci pagine simili quando non è possibile trovare una pagina
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 80 o in seguito

  #### Descrizione
  Consenti a Microsoft Edge di stabilire una connessione a un servizio Web per generare URL e cercare suggerimenti per problemi di connettività quali errori DNS.

Se abiliti questi criteri, un servizio Web viene utilizzato per generare URL e cercare suggerimenti per gli errori di rete.

Se disabiliti questi criteri, nessuna chiamata al servizio Web viene effettuata e viene visualizzata una pagina di errore standard.

Se non configuri questi criteri, Microsoft Edge rispetta la preferenza dell'utente impostata in Servizi su edge://settings/privacy.
In particolare, l'utente può attivare o disattivare l'interruttore **Suggerisci pagine simili quando non è possibile trovare una pagina Web**. Se hai abilitato questi criteri (AlternateErrorPagesEnabled), tale opzione è attivata, ma l'utente non può modificare l'impostazione utilizzando l'interruttore. Se disabiliti questi criteri, l'impostazione è disattivata e l'utente non può modificare l'impostazione utilizzando l'interruttore.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AlternateErrorPagesEnabled
  - Nome GP: Suggerisci pagine simili quando non è possibile trovare una pagina
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: AlternateErrorPagesEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AlternateErrorPagesEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AlwaysOpenPdfExternally
  #### Apri sempre i file PDF esternamente
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Disabilita il visualizzatore PDF interno in Microsoft Edge.

Se abiliti questi criteri Microsoft Edge considera i file PDF come download e consente agli utenti di aprirli con l'applicazione predefinita.

Se non configuri o disabiliti questi criteri, Microsoft Edge apre i file PDF (a meno che l'utente non li disabiliti).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AlwaysOpenPdfExternally
  - Nome GP: Apri sempre i file PDF esternamente
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AlwaysOpenPdfExternally
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AlwaysOpenPdfExternally
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AmbientAuthenticationInPrivateModesEnabled
  #### Abilita autenticazione ambiente per i profili InPrivate e guest
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 81 o in seguito

  #### Descrizione
  Configura questi criteri per consentire/non consentire l'autenticazione dell'ambiente per i profili InPrivate e Guest in Microsoft Edge.

L'autenticazione dell'ambiente è l'autenticazione HTTP con le credenziali predefinite quando le credenziali esplicite non vengono fornite tramite NTLM/Kerberos/richiesta di negoziazione/schema di risposta.

Se imposti i criteri su ‘RegularOnly’, l'autenticazione dell'ambiente viene consentita solo per le sessioni normali. Le sessioni InPrivate e Guest non saranno in grado di eseguire l'autenticazione dell'ambiente.

Se imposti i criteri su ‘InPrivateAndRegular’, l'autenticazione dell'ambiente viene consentita per le sessioni InPrivate e normali. Le sessioni Guest non saranno in grado di eseguire l'autenticazione dell'ambiente.

Se imposti i criteri su ‘GuestAndRegular’, l'autenticazione dell'ambiente è consentita per le sessioni Guest e normali. Le sessioni InPrivate non saranno in grado di eseguire l'autenticazione dell'ambiente

Se imposti i criteri su ‘All’, l'autenticazione dell'ambiente sarà consentita per tutte le sessioni.

Tieni presente che l'autenticazione dell'ambiente è sempre consentita sui profili normali.

In Microsoft Edge versione 81 e successive, se i criteri sono lasciati non impostati, l'autenticazione dell'ambiente verrà abilitata solo in sessioni normali.

Mappatura opzioni criteri:

* RegularOnly (0) = Abilita l'autenticazione ambiente solo nelle sessioni normali.

* InPrivateAndRegular (1) = Abilita autenticazione ambiente nelle sessioni InPrivate e nomali

* GuestAndRegular (2) = Abilita autenticazione ambiente in sessioni guest e normali

* All (3) = Abilita autenticazione ambiente in sessioni normali, InPrivate e guest

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AmbientAuthenticationInPrivateModesEnabled
  - Nome GP: Abilita autenticazione ambiente per i profili InPrivate e guest
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AmbientAuthenticationInPrivateModesEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AmbientAuthenticationInPrivateModesEnabled
  - Valore di esempio:
``` xml
<integer>0</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AppCacheForceEnabled
  #### Consente di riabilitare la funzionalità AppCache, anche se è disattivata per impostazione predefinita
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 84 o in seguito

  #### Descrizione
  Se imposti questo criterio su true, AppCache è abilitata, anche quando AppCache in Microsoft Edge non è disponibile per impostazione predefinita.

Se imposti questo criterio su false, o non lo imposti, AppCache seguirà le impostazioni predefinite di Microsoft Edge.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AppCacheForceEnabled
  - Nome GP: Consente di riabilitare la funzionalità AppCache, anche se è disattivata per impostazione predefinita
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AppCacheForceEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AppCacheForceEnabled
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ApplicationLocaleValue
  #### Specifica le impostazioni locali dell'applicazione
  
  
  #### Versioni supportate:
  - Su Windows dal 77 o successiva

  #### Descrizione
  Configura le impostazioni locali dell'applicazione in Microsoft Edge e impedisce agli utenti di modificarle.

Se abiliti questo criterio, Microsoft Edge utilizza le impostazioni locali specificate. Se le impostazioni locali configurate non sono supportate, viene utilizzato "en-US".

Se disabiliti o non configuri questa impostazione, Microsoft Edge utilizza le impostazioni locali preferite specificate dall'utente (se configurate) o le impostazioni locali di fallback "en-US".

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ApplicationLocaleValue
  - Nome GP: Specifica le impostazioni locali dell'applicazione
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: ApplicationLocaleValue
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"en"
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AudioCaptureAllowed
  #### Consenti o blocca l'acquisizione audio
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente di specificare se a un utente viene richiesto di concedere un accesso tramite sito Web al dispositivo di acquisizione audio. Questi criteri si applicano a tutti gli URL ad eccezione di quelli configurati nell'elenco [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Se abiliti o non configuri questi criteri (impostazione predefinita), all'utente verrà richiesto l'accesso all'acquisizione audio tranne dagli URL inclusi nell'elenco [AudioCaptureAllowedUrls](#audiocaptureallowedurls). A questi URL elencati viene concesso l'accesso senza richiedere conferma.

Se disabiliti questi criteri, all'utente non viene inviata la richiesta e l'acquisizione audio sarà accessibile solo agli URL configurati in [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Questi criteri interessano tutti i tipi di input audio, non solo il microfono incorporato.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AudioCaptureAllowed
  - Nome GP: Consenti o blocca l'acquisizione audio
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AudioCaptureAllowed
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AudioCaptureAllowed
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AudioCaptureAllowedUrls
  #### Siti che possono accedere ai dispositivi di acquisizione audio senza richiedere l'autorizzazione
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica i siti Web, in base agli schemi URL, che possono utilizzare dispositivi di acquisizione audio senza richiedere l'autorizzazione all'utente. I modelli in questo elenco vengono messi a confronto con l'origine di sicurezza dell'URL di richiesta. Se corrispondono, al sito viene automaticamente consentito l'accesso ai dispositivi di acquisizione audio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AudioCaptureAllowedUrls
  - Nome GP: Siti che possono accedere ai dispositivi di acquisizione audio senza richiedere l'autorizzazione
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AudioCaptureAllowedUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AudioSandboxEnabled
  #### Consenti l'esecuzione della sandbox audio
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 81 o in seguito

  #### Descrizione
  Questi criteri controllano la sandbox del processo audio.

Se abiliti questi criteri, il processo audio verrà eseguito in modalità sandbox.

Se disabiliti questa impostazione dei criteri, il processo audio non verrà eseguito in modalità sandbox e il modulo di elaborazione audio WebRTC verrà eseguito nel processo di rendering.
In questo modo gli utenti sono esposti a rischi di sicurezza correlati all'esecuzione del sottosistema audio non in modalità sandbox.

Se non configuri questi criteri, verrà utilizzata la configurazione predefinita per la sandbox audio, che potrebbe variare in base alla piattaforma.

Questi criteri sono destinati a concedere alle aziende la possibilità di disabilitare la sandbox audio se usano le configurazioni del software di sicurezza che interferiscono con la sandbox.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AudioSandboxEnabled
  - Nome GP: Consenti l'esecuzione della sandbox audio
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AudioSandboxEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AudioSandboxEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AutoImportAtFirstRun
  #### Importa automaticamente i dati e le impostazioni di un altro browser alla prima esecuzione
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Se abiliti questi criteri, tutti i tipi di dati e le impostazioni supportati dal browser specificato verranno importati automaticamente alla prima esecuzione. Durante il completamento dell'installazione, anche la sezione di importazione verrà ignorata.

I dati del browser da Microsoft Edge Legacy verranno sempre migrati automaticamente alla prima esecuzione, indipendentemente dal valore di questi criteri.

       Se questi criteri sono impostati su  'Da browser predefinito', i tipi di dati corrispondenti al browser predefinito sul dispositivo gestito verranno importati.

 Se il browser specificato come valore di questo criterio non è presente nel dispositivo gestito, Microsoft Edge ignorerà semplicemente l'importazione senza alcuna notifica per l'utente.

 Se imposti questi criteri su 'Importazione automatica disabilitata', la sezione di importazione del completamento dell'installazione viene ignorata completamente e Microsoft Edge non importa automaticamente i dati e le impostazioni del browser.

 Se questi criteri vengono impostati sul valore di Internet Explorer, i seguenti tipi di dati verranno importati da Internet Explorer:
 1. Preferiti o segnalibri
 2. Password salvate
 3. Motori di ricerca
 4. Cronologia esplorazioni
 5. Home page

Se questi criteri vengono impostati sul valore di Google Chrome, i seguenti tipi di dati verranno importati da Google Chrome:
 1. Preferiti
2. Password salvate
 3. Indirizzi e altro
 4. Info di pagamento
 5. Cronologia esplorazioni
 6. Impostazioni
 7. Schede aggiunte e aperte
 8. Estensioni
 9. Cookie

 Nota: per uno sguardo approfondito su quanto viene importato da Google Chrome, vedi [https://go.microsoft.com/fwlink/?linkid=2120835](https://go.microsoft.com/fwlink/?linkid=2120835)

 Se questi criteri sono impostati sul valore di Safari, i dati dell'utente non vengono più importati in Microsoft Edge. Ciò è dovuto al modo in cui funziona l'accesso completo al disco sul Mac.
 Da macOS Mojave in avanti, non è più possibile importare automaticamente e senza supervisione i dati di Safari in Microsoft Edge.

A partire dalla versione 83 di Microsoft Edge, se questi criteri vengono impostati sul valore di Mozilla Firefox, i seguenti tipi di dati verranno importati da Mozilla Firefox:
 1. Preferiti o segnalibri
 2. Password salvate
 3. Indirizzi e altro
 4. Cronologia esplorazioni

 Se vuoi limitare i tipi di dati specifici da importare nei dispositivi gestiti, puoi usare questi criteri con altri criteri, ad esempio [ImportAutofillFormData](#importautofillformdata), [ImportBrowserSettings](#importbrowsersettings), [ImportFavorites](#importfavorites), e così via.

Mappatura opzioni criteri:

* FromDefaultBrowser (0) = Importa automaticamente tutti i tipi di dati e le impostazioni supportati dal browser supportato

* FromInternetExplorer (1) = Importa automaticamente tutti i tipi di dati e le impostazioni supportati da Internet Explorer

* FromGoogleChrome (2) = Importa automaticamente tutti i tipi di dati e le impostazioni supportati da Google Chrome

* FromSafari (3) = Importa automaticamente tutti i tipi di dati e le impostazioni supportati da Safari

* DisabledAutoImport (4) = Disabilita l'importazione automatica e la sezione di importazione dell'esperienza di prima esecuzione viene ignorata

* FromMozillaFirefox (5) = Importa automaticamente tutti i tipi di dati e le impostazioni supportati da Mozilla Firefox

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AutoImportAtFirstRun
  - Nome GP: Importa automaticamente i dati e le impostazioni di un altro browser alla prima esecuzione
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AutoImportAtFirstRun
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AutoImportAtFirstRun
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AutoLaunchProtocolsFromOrigins
  #### Definisci un elenco di protocolli in grado di avviare un'applicazione esterna dalle origini elencate senza richiedere all'utente
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 85 o in seguito

  #### Descrizione
  Consente di impostare un elenco di protocolli e, per ciascun protocollo, un elenco associato di modelli di origine consentiti, in grado di avviare un'applicazione esterna senza richiedere all'utente. Il separatore finale non deve essere incluso quando si elenca il protocollo. Ad esempio, elenca "skype" anziché "skype:" o "skype://".

Se configuri questo criterio, un protocollo sarà autorizzato ad avviare un'applicazione esterna senza richiedere il criterio se:

- il protocollo è elencato

- l'origine del sito che tenta di avviare il protocollo corrisponde a uno dei modelli di origine nell'elenco origini_consentite di tale protocollo.

Se una delle condizioni è false, la richiesta di avvio del protocollo esterno non verrà omessa dal criterio.

Se non configuri questo criterio, nessun protocollo può essere avviato senza un prompt. Gli utenti possono annullare la richiesta in base al protocollo/sito, a meno che il criterio [ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox) non sia impostato su Disabilitato. Questo criterio non ha alcun impatto sulle esenzioni di prompt in base al protocollo/sito impostate dagli utenti.

I modelli di corrispondenza dell'origine utilizzano un formato simile a quelli per il criterio [URLBlocklist](#urlblocklist), che sono documentati all'indirizzo [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Tuttavia, i modelli di corrispondenza dell'origine per questo criterio non possono contenere elementi "/path" o "@query". Qualsiasi modello che contenga un elemento "/path" o "@query" verrà ignorato.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Dizionario

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AutoLaunchProtocolsFromOrigins
  - Nome GP: Definisci un elenco di protocolli in grado di avviare un'applicazione esterna dalle origini elencate senza richiedere all'utente
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AutoLaunchProtocolsFromOrigins
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\AutoLaunchProtocolsFromOrigins = [
  {
    "allowed_origins": [
      "example.com", 
      "http://www.example.com:8080"
    ], 
    "protocol": "spotify"
  }, 
  {
    "allowed_origins": [
      "https://example.com", 
      "https://.mail.example.com"
    ], 
    "protocol": "teams"
  }, 
  {
    "allowed_origins": [
      "*"
    ], 
    "protocol": "outlook"
  }
]
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AutoLaunchProtocolsFromOrigins
  - Valore di esempio:
``` xml
<key>AutoLaunchProtocolsFromOrigins</key>
<array>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>example.com</string>
      <string>http://www.example.com:8080</string>
    </array>
    <key>protocol</key>
    <string>spotify</string>
  </dict>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>https://example.com</string>
      <string>https://.mail.example.com</string>
    </array>
    <key>protocol</key>
    <string>teams</string>
  </dict>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>*</string>
    </array>
    <key>protocol</key>
    <string>outlook</string>
  </dict>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AutoOpenAllowedForURLs
  #### URL in cui è possibile applicare AutoOpenFileTypes
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 85 o in seguito

  #### Descrizione
  Un elenco di URL a cui verrà applicato [AutoOpenFileTypes](#autoopenfiletypes). Questo criterio non ha alcun impatto sui valori di apertura automatica impostati dagli utenti tramite la voce di menu  ... > "Apri sempre file di questo tipo" di Download Shelf.

Se imposti gli URL in questo criterio, i file si apriranno automaticamente per criterio solo se l'URL fa parte di questa serie e il tipo di file è indicato in [AutoOpenFileTypes](#autoopenfiletypes). Se una delle condizioni è falsa, il download non si aprirà automaticamente per criterio.

Se non imposti questo criterio, tutti i download in cui il tipo di file è in [AutoOpenFileTypes](#autoopenfiletypes) si apriranno automaticamente.

Un modello di URL deve essere formattato secondo quando indicato all'indirizzo https://go.microsoft.com/fwlink /? linkid = 2.095.322.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AutoOpenAllowedForURLs
  - Nome GP: URL in cui è possibile applicare AutoOpenFileTypes
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\1 = "example.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\5 = ".exact.hostname.com"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AutoOpenAllowedForURLs
  - Valore di esempio:
``` xml
<array>
  <string>example.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AutoOpenFileTypes
  #### Elenco dei tipi di file che dovrebbero aprirsi automaticamente al download
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 85 o in seguito

  #### Descrizione
  Questo criterio imposta un elenco di tipi di file che dovrebbero essere aperti automaticamente al download. Nota: il separatore principale non deve essere incluso quando elenchi i tipi di file, quindi indica "txt" anziché ".txt".

Per impostazione predefinita, questi tipi di file verranno aperti automaticamente su tutti gli URL. Puoi utilizzare il criterio [AutoOpenAllowedForURLs](#autoopenallowedforurls) per limitare gli URL per i quali questi tipi di file verranno aperti automaticamente.

I tipi di file che devono essere aperti automaticamente saranno comunque soggetti ai controlli abilitati di Microsoft Defender SmartScreen e non verranno aperti se non superano tali controlli.

I tipi di file che un utente ha già specificato di aprire automaticamente continueranno ad aprirsi quando vengono scaricati. L'utente potrà ancora specificare altri tipi di file da aprire automaticamente.

Se non imposti questo criterio, solo i tipi di file che un utente ha già specificato di aprire automaticamente si apriranno al download.

Questo criterio è disponibile solo per le istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AutoOpenFileTypes
  - Nome GP: Elenco dei tipi di file che dovrebbero aprirsi automaticamente al download
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\1 = "exe"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\2 = "txt"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AutoOpenFileTypes
  - Valore di esempio:
``` xml
<array>
  <string>exe</string>
  <string>txt</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AutofillAddressEnabled
  #### Abilita riempimento automatico per gli indirizzi
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Abilita la funzionalità di riempimento automatico e consente agli utenti di completare automaticamente le informazioni sull'indirizzo nei moduli Web utilizzando informazioni archiviate in precedenza.

Se disabiliti questi criteri, il riempimento automatico non suggerisce né compila le informazioni sull'indirizzo, né salva altre informazioni sull'indirizzo che l'utente potrebbe inviare durante l'esplorazione del Web.

Se abiliti o non configuri questi criteri, gli utenti possono controllare il riempimento automatico degli indirizzi nell'interfaccia utente.

Tieni presente che se disabiliti questi criteri interrompi anche tutte le attività per tutti i moduli Web, ad eccezione dei moduli di pagamento e password. Non vengono salvate altre voci e Microsoft Edge non suggerisce né compila automaticamente le voci precedenti.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AutofillAddressEnabled
  - Nome GP: Abilita riempimento automatico per gli indirizzi
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: AutofillAddressEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AutofillAddressEnabled
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AutofillCreditCardEnabled
  #### Abilita riempimento automatico per le carte di credito
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Abilita la funzionalità Riempimento automatico di Microsoft Edge e consente agli utenti di completare automaticamente le informazioni della carta di credito nei moduli Web utilizzando le informazioni archiviate in precedenza.

Se disabiliti questi criteri, il riempimento automatico non suggerisce né compila mai le informazioni della carta di credito e non vengono salvate le informazioni aggiuntive della carta di credito che gli utenti potrebbero inviare durante l'esplorazione del Web.

Se abiliti o non configuri questi criteri, gli utenti possono controllare il riempimento automatico per le carte di credito.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AutofillCreditCardEnabled
  - Nome GP: Abilita riempimento automatico per le carte di credito
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: AutofillCreditCardEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AutofillCreditCardEnabled
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### AutoplayAllowed
  #### Consenti AutoPlay di supporti per siti Web
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 78 o in seguito

  #### Descrizione
  Questo criterio consente di impostare il criterio AutoPlay dei supporti per i siti Web.

L'impostazione predefinita, "Non configurato", rispetta le impostazioni di AutoPlay dei supporti correnti e consente agli utenti di configurare le impostazioni di AutoPlay.

La selezione di "Abilitato" imposta la riproduzione automatica dei supporti su "Consenti".  Tutti i siti Web sono autorizzati a eseguire la riproduzione automatica dei supporti. Gli utenti non possono ignorare questo criterio.

La selezione di "Disabilitato" imposta la riproduzione automatica su "Blocco".  Nessun sito Web è autorizzato a eseguire la riproduzione automatica dei supporti. Gli utenti non possono ignorare questo criterio.

Per rendere effettive le modifiche, è necessario chiudere e riaprire una scheda.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: AutoplayAllowed
  - Nome GP: Consenti AutoPlay di supporti per siti Web
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: AutoplayAllowed
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: AutoplayAllowed
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### BackgroundModeEnabled
  #### Continua a eseguire le app in background dopo che Microsoft Edge viene chiuso
  
  
  #### Versioni supportate:
  - Su Windows dal 77 o successiva

  #### Descrizione
  Consente ai processi di Microsoft Edge di essere avviati su un accesso del sistema operativo e di essere mantenuti in esecuzione quando viene chiusa l'ultima finestra del browser. In questo scenario, le app in background e la sessione di esplorazione corrente rimangono attive, inclusi i cookie di sessione. Un processo in background aperto visualizza un'icona sulla barra delle applicazioni e può sempre essere chiuso da lì.

Se abiliti questi criteri, la modalità in background è attivata.

Se disabiliti questi criteri, la modalità in background è disattivata.

Se non configuri questi criteri, la modalità in background è inizialmente disattivata e l'utente può configurarne il comportamento in edge://settings/system.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: BackgroundModeEnabled
  - Nome GP: Continua a eseguire le app in background dopo che Microsoft Edge viene chiuso
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: BackgroundModeEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### BackgroundTemplateListUpdatesEnabled
  #### Abilita gli aggiornamenti in background all'elenco di modelli disponibili per le raccolte e le altre funzionalità che utilizzano i modelli.
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 79 o in seguito

  #### Descrizione
  Consente di abilitare o disabilitare gli aggiornamenti in background per l'elenco dei modelli disponibili per le raccolte e altre caratteristiche che utilizzano modelli.  I modelli vengono utilizzati per estrarre i metadati avanzati da una pagina Web quando la pagina viene salvata in una raccolta.

Se abiliti questa impostazione o l'impostazione non è configurata, l'elenco dei modelli disponibili verrà scaricato in background da un servizio Microsoft ogni 24 ore.

Se si disabilita questa impostazione, l'elenco dei modelli disponibili verrà scaricato su richiesta. Questo tipo di download potrebbe causare piccole prestazioni per le raccolte e altre caratteristiche.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: BackgroundTemplateListUpdatesEnabled
  - Nome GP: Abilita gli aggiornamenti in background all'elenco di modelli disponibili per le raccolte e le altre funzionalità che utilizzano i modelli.
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: BackgroundTemplateListUpdatesEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: BackgroundTemplateListUpdatesEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### BingAdsSuppression
  #### Blocca tutti gli annunci nei risultati della ricerca con Bing
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 83 o in seguito

  #### Descrizione
  Abilita un'esperienza di ricerca senza pubblicità su Bing.com

Se abiliti questi criteri, l'utente può eseguire una ricerca in bing.com e vivere un'esperienza di ricerca senza pubblicità. Contemporaneamente, l'impostazione Ricerca sicura verrà impostata su 'Completa' e non potrà essere cambiata dall'utente.

Se non configuri questi criteri, l'esperienza predefinita presenterà annunci nei risultati della ricerca in bing.com. Ricerca sicura sarà impostato su 'Media' per impostazione predefinita e potrà essere modificata dall'utente.

Questi criteri sono disponibili solo per gli SKU della scuola primaria e secondaria di primo grado identificati come tenant EDU da Microsoft.

Fai riferimento a [https://go.microsoft.com/fwlink/?linkid=2119711](https://go.microsoft.com/fwlink/?linkid=2119711) per altre informazioni su questo criterio o se si applicano gli scenari seguenti:

* Hai un tenant EDU, ma il criterio non funziona.

* Hai fatto inserire il tuo indirizzo IP tra quelli consentiti per un'esperienza di ricerca senza pubblicità.

* Hai vissuto un'esperienza di ricerca senza pubblicità in Microsoft Edge Legacy e vuoi eseguire l'aggiornamento alla nuova versione di Microsoft Edge.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: BingAdsSuppression
  - Nome GP: Blocca tutti gli annunci nei risultati della ricerca con Bing
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: BingAdsSuppression
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: BingAdsSuppression
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### BlockThirdPartyCookies
  #### Blocca i cookie di terze parti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Blocca l'impostazione dei cookie per gli elementi delle pagine Web che non provengono dal dominio presente nella barra degli indirizzi.

Se abiliti questi criteri, gli elementi della pagina Web che non provengono dal dominio presente nella barra degli indirizzi non possono impostare i cookie.

Se disabiliti questi criteri, gli elementi della pagina Web che non provengono dal dominio presente nella barra degli indirizzi possono impostare i cookie.

Se non configuri questi criteri, sono abilitati i cookie di terze parti, ma gli utenti possono modificare l'impostazione.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: BlockThirdPartyCookies
  - Nome GP: Blocca i cookie di terze parti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: BlockThirdPartyCookies
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: BlockThirdPartyCookies
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### BrowserAddProfileEnabled
  #### Abilita la creazione del profilo dal menu a comparsa Identità o dalla pagina Impostazioni
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente agli utenti di creare nuovi profili usando l'opzione **Aggiungi profilo**.
Se abiliti o non configuri questo criterio, Microsoft Edge consente agli utenti di utilizzare l'opzione **Aggiungi profilo** dal menu a comparsa Identità o dalla pagina Impostazioni per creare nuovi profili.

Se disabiliti questo criterio, gli utenti non possono aggiungere nuovi profili dal menu a comparsa Identità o dalla pagina Impostazioni.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: BrowserAddProfileEnabled
  - Nome GP: Abilita la creazione del profilo dal menu a comparsa Identità o dalla pagina Impostazioni
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: BrowserAddProfileEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: BrowserAddProfileEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### BrowserGuestModeEnabled
  #### Abilita modalità guest
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Abilita l'opzione per consentire l'uso di profili guest in Microsoft Edge. In un profilo guest, il browser non importa i dati di esplorazione dai profili esistenti e li elimina quando tutti i profili guest vengono chiusi.

Se abiliti o non configuri questo criterio, Microsoft Edge consente agli utenti di esplorare con i profili guest.

Se disabiliti questo criterio, Microsoft Edge non consente agli utenti di esplorare con i profili guest.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: BrowserGuestModeEnabled
  - Nome GP: Abilita modalità guest
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: BrowserGuestModeEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: BrowserGuestModeEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### BrowserNetworkTimeQueriesEnabled
  #### Consenti le query a un servizio di ora di rete del browser
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Impedisce a Microsoft Edge di inviare occasionalmente query a un servizio ora di rete del browser per recuperare un timestamp accurato.

Se disabiliti questi criteri, Microsoft Edge interrompe l'invio di query a un servizio ora di rete del browser.

Se abiliti o non configuri questi criteri, Microsoft Edge invia occasionalmente le query a un servizio ora di rete del browser.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: BrowserNetworkTimeQueriesEnabled
  - Nome GP: Consenti le query a un servizio di ora di rete del browser
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: BrowserNetworkTimeQueriesEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: BrowserNetworkTimeQueriesEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### BrowserSignin
  #### Impostazioni di accesso del browser
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica se un utente può accedere a Microsoft Edge con il proprio account e utilizzare servizi correlati all'account, come la sincronizzazione e Single Sign-On. Per controllare la disponibilità della sincronizzazione, utilizza invece i criteri [SyncDisabled](#syncdisabled).

Se imposti questi criteri su 'Disable', assicurati di impostare anche i criteri [NonRemovableProfileEnabled](#nonremovableprofileenabled) su disabilitato perché [NonRemovableProfileEnabled](#nonremovableprofileenabled) disabilita la creazione di un profilo browser con accesso automatico. Se sono impostati entrambi i criteri,  Microsoft Edge utilizzerà i criteri 'Disabilita accesso al browser' e agisci come se [NonRemovableProfileEnabled](#nonremovableprofileenabled) siano impostati su disabilitato.

 Se imposti questi criteri su 'Enable', gli utenti possono accedere al browser. L'accesso al browser non significa che la sincronizzazione sia attivata per impostazione predefinita e per utilizzare questa funzionalità, l'utente deve fornire il consenso esplicito separatamente.

Se imposti questi criteri su 'Force', gli utenti devono accedere a un profilo per utilizzare il browser. Per impostazione predefinita, questa opzione consente all'utente di scegliere se desidera eseguire la sincronizzazione con il proprio account, a meno che la sincronizzazione non sia stata disabilitata dall'amministratore del dominio o con i criteri [SyncDisabled](#syncdisabled). Il valore predefinito dei criteri [BrowserGuestModeEnabled](#browserguestmodeenabled) è impostato su false.

Se non configuri questa impostazione, gli utenti possono decidere se desiderano abilitare l'opzione di accesso al browser e usarla in modo appropriato.

Mappatura opzioni criteri:

* Disable (0) = Disabilita l'accesso del browser

* Enable (1) = Abilita accesso browser

* Force (2) = Imponi agli utenti di accedere per utilizzare il browser

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: BrowserSignin
  - Nome GP: Impostazioni di accesso del browser
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: BrowserSignin
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: BrowserSignin
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### BuiltInDnsClientEnabled
  #### Utilizza il client DNS predefinito
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Determina se utilizzare il client DNS predefinito.

Non influisce sulla scelta dei server DNS utilizzati, ma solo sullo stack del software utilizzato per comunicare con loro. Ad esempio, se il sistema operativo è configurato per l'utilizzo di un server DNS aziendale, lo stesso server verrà utilizzato dal client DNS predefinito. È tuttavia possibile che il client DNS predefinito affronti i server in diversi modi utilizzando protocolli più moderni correlati a DNS, come DNS-over-TLS.

Se abiliti questo criterio, verrà utilizzato il client DNS predefinito, se disponibile.

Se disabiliti questo criterio, il client non verrà mai utilizzato.

Se non configuri questo criterio, il client DNS predefinito è abilitato per impostazione predefinita in MacOS e gli utenti possono scegliere se usare il client DNS predefinito modificando edge://flags o specificando un flag della riga di comando.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: BuiltInDnsClientEnabled
  - Nome GP: Utilizza il client DNS predefinito
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: BuiltInDnsClientEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: BuiltInDnsClientEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### BuiltinCertificateVerifierEnabled
  #### Determina se il certificato predefinito Verifier verrà utilizzato per verificare i certificati del server (deprecato)
  >DEPRECAtO: questi criteri sono deprecati. Sono attualmente supportati ma diventeranno obsoleti in una versione futura.
  
  #### Versioni supportate:
  - Su macOS dal 83 o successiva

  #### Descrizione
  Questi criteri sono deprecati perché sono intesi solo come meccanismo a breve termine per dare alle aziende più tempo per aggiornare i loro ambienti e segnalare problemi se ritieni che sia incompatibile con la verifica di certificati predefiniti.

Non funzionerà in Microsoft Edge per Mac OS X versione 87, quando è pianificata la rimozione del supporto per la verifica di certificati legacy su Mac OS X.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  

  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: BuiltinCertificateVerifierEnabled
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### CertificateTransparencyEnforcementDisabledForCas
  #### Disabilita l'applicazione della trasparenza dei certificati per un elenco di hash subjectPublicKeyInfo
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Disabilita l'applicazione dei requisiti di trasparenza dei certificati per un elenco di hash subjectPublicKeyInfo.

Questi criteri consentono di disabilitare i requisiti di divulgazione di trasparenza dei certificati per le catene di certificati che contengono certificati con uno degli hash subjectPublicKeyInfo specificati. In tal modo i certificati che altrimenti non sarebbero attendibili perché non divulgati pubblicamente, continuano ad essere utilizzati per gli host aziendali.

Affinché l'applicazione della trasparenza dei certificati venga disabilitata quando questi criteri sono impostati, è necessario soddisfare una delle seguenti condizioni:
1. L'hash è di un subjectPublicKeyInfo del certificato del server.
2. L'hash è di un subjectPublicKeyInfo presente in un certificato della CA nella catena di certificati e tale certificato della CA è vincolato tramite l'estensione nameConstraints X.509v3, uno o più nameConstraints directoryName sono presenti in permittedSubtrees e directoryName contiene un attributo organizationName.
3. L'hash è di un subjectPublicKeyInfo che viene visualizzato in un certificato della CA nella catena di certificati, il certificato della CA include uno o più attributi organizationName nell'oggetto del certificato e il certificato del server contiene lo stesso numero di attributi organizationName, nello stesso ordine e con gli stessi valori byte per byte.

Specifica l'hash subjectPublicKeyInfo concatenando il nome dell'algoritmo di hash, il carattere "/" e la codifica Base64 dell'algoritmo di hash applicato a subjectPublicKeyInfo con codifica DER del certificato specificato. Questa codifica Base64 ha lo stesso formato di un'impronta digitale SPKI, come definito nella RFC 7469, Sezione 2.4. Gli algoritmi di hash non riconosciuti vengono ignorati. L'unico algoritmo di hash supportato in questo momento è "sha256".

Se non configuri questi criteri, qualsiasi certificato che deve essere divulgato con trasparenza dei certificati è considerato non attendibile se non viene divulgato in base ai criteri di trasparenza dei certificati.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: CertificateTransparencyEnforcementDisabledForCas
  - Nome GP: Disabilita l'applicazione della trasparenza dei certificati per un elenco di hash subjectPublicKeyInfo
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\2 = "sha256//////////////////////w=="

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: CertificateTransparencyEnforcementDisabledForCas
  - Valore di esempio:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### CertificateTransparencyEnforcementDisabledForLegacyCas
  #### Disabilita l'applicazione della trasparenza dei certificati per un elenco di autorità di certificazione legacy
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Disabilita l'applicazione dei requisiti di trasparenza dei certificati per un elenco di autorità di certificazione (CA) legacy.

Questi criteri consentono di disabilitare i requisiti di divulgazione di trasparenza dei certificati per le catene che contengono certificati con un hash subjectPublicKeyInfo specificato. In tal modo i certificati che altrimenti non sarebbero attendibili perché non correttamente divulgati pubblicamente, continuano ad essere utilizzati per gli host aziendali.

Per disabilitare l'applicazione della trasparenza dei certificati, devi impostare l'hash su un subjectPublicKeyInfo specificato in un certificato della CA riconosciuto come autorità di certificazione (CA) legacy. Una CA legacy è un'autorità di certificazione che è stata pubblicamente attendibile per impostazione predefinita per uno o più sistemi operativi supportati da Microsoft Edge.

Specifica l'hash subjectPublicKeyInfo concatenando il nome dell'algoritmo di hash, il carattere "/" e la codifica Base64 dell'algoritmo di hash applicato a subjectPublicKeyInfo con codifica DER del certificato specificato. Questa codifica Base64 ha lo stesso formato di un'impronta digitale SPKI, come definito nella RFC 7469, Sezione 2.4. Gli algoritmi di hash non riconosciuti vengono ignorati. L'unico algoritmo di hash supportato in questo momento è "sha256".

Se non configuri questi criteri, qualsiasi certificato che deve essere divulgato con trasparenza dei certificati è considerato non attendibile se non viene divulgato in base ai criteri di trasparenza dei certificati.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Nome GP: Disabilita l'applicazione della trasparenza dei certificati per un elenco di autorità di certificazione legacy
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\2 = "sha256//////////////////////w=="

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Valore di esempio:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### CertificateTransparencyEnforcementDisabledForUrls
  #### Disabilita l'applicazione della trasparenza dei certificati per URL specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Disabilita l'applicazione dei requisiti di trasparenza dei certificati per gli URL elencati.

Questi criteri consentono di non divulgare i certificati per i nomi host negli URL specificati tramite la trasparenza dei certificati. Consente di utilizzare certificati che sarebbero altrimenti non attendibili, in quanto non erano stati correttamente divulgati, ma rende più difficile rilevare i certificati rilasciati erroneamente per tali host.

Crea il modello di URL in base al formato [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Poiché i certificati sono validi per un nome host specificato, indipendentemente dallo schema, dalla porta o dal percorso, solo la parte del nome host dell'URL viene considerata. Gli host con caratteri jolly non sono supportati.

Se non configuri questi criteri, tutti i certificati che devono essere divulgati tramite trasparenza dei certificati vengono considerati non attendibili se non vengono divulgati.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: CertificateTransparencyEnforcementDisabledForUrls
  - Nome GP: Disabilita l'applicazione della trasparenza dei certificati per URL specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\2 = ".contoso.com"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: CertificateTransparencyEnforcementDisabledForUrls
  - Valore di esempio:
``` xml
<array>
  <string>contoso.com</string>
  <string>.contoso.com</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ClearBrowsingDataOnExit
  #### Cancella i dati di navigazione quando Microsoft Edge viene chiuso
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 78 o in seguito

  #### Descrizione
  Microsoft Edge per impostazione predefinita non cancella i dati di navigazione quando viene chiuso. I dati di navigazione includono le informazioni inserite nei moduli, le password e persino i siti Web visitati.

Se abiliti questi criteri, tutti i dati di navigazione vengono eliminati ogni volta che Microsoft Edge viene chiuso. Tieni presente che se abiliti questi criteri, avranno la precedenza sulla modalità di configurazione di [DefaultCookiesSetting](#defaultcookiessetting)

Se disabiliti o non configuri questi criteri, gli utenti possono configurare l'opzione Cancella i dati delle esplorazioni in Impostazioni.

Se abiliti questi criteri, non abilitare i criteri [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) o [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit) perché entrambi si occupano dell'eliminazione dei dati. Se li abiliti entrambi, questi criteri sono prioritari e pertanto tutti i dati vengono cancellati quando Microsoft Edge viene chiuso, indipendentemente da come hai configurato [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) o [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)..

Per evitare che i cookie vengano eliminati alla chiusura, configura il criterio [SaveCookiesOnExit](#savecookiesonexit).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ClearBrowsingDataOnExit
  - Nome GP: Cancella i dati di navigazione quando Microsoft Edge viene chiuso
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: ClearBrowsingDataOnExit
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ClearBrowsingDataOnExit
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ClearCachedImagesAndFilesOnExit
  #### Cancella immagini e file memorizzati nella cache quando Microsoft Edge viene chiuso
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 83 o in seguito

  #### Descrizione
  Microsoft Edge non cancella le immagini e i file memorizzati nella cache per impostazione predefinita alla chiusura.

Se abiliti questi criteri, le immagini e i file memorizzati nella cache verranno eliminati ogni volta che Microsoft Edge verrà chiuso.

Se disabiliti questi criteri, gli utenti non potranno configurare le immagini e i file memorizzati nella cache in edge://settings/clearBrowsingDataOnClose.

Se non configuri questi criteri, gli utenti possono scegliere se le immagini e i file memorizzati nella cache devono essere cancellati alla chiusura.

Se disabiliti questi criteri, non abilitare i criteri [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) perché riguardano entrambi l'eliminazione dei dati. Se li configuri entrambi, i criteri [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) hanno la precedenza ed eliminano tutti i dati quando Microsoft Edge viene chiuso, indipendentemente dal modo in cui hai configurato [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ClearCachedImagesAndFilesOnExit
  - Nome GP: Cancella immagini e file memorizzati nella cache quando Microsoft Edge viene chiuso
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: ClearCachedImagesAndFilesOnExit
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ClearCachedImagesAndFilesOnExit
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ClickOnceEnabled
  #### Consenti agli utenti di aprire file tramite il protocollo ClickOnce
  
  
  #### Versioni supportate:
  - Su Windows dal 78 o successiva

  #### Descrizione
  Consenti agli utenti di aprire i file utilizzando il protocollo ClickOnce. Il protocollo ClickOnce permette ai siti Web di richiedere che il browser apra i file da un URL specifico utilizzando il gestore di file ClickOnce nel computer o nel dispositivo dell'utente.

Se abiliti questi criteri, gli utenti possono aprire i file utilizzando il protocollo ClickOnce. Questi criteri sostituiscono l'impostazione ClickOnce dell'utente nella pagina edge://flags/.

Se disabiliti questi criteri, gli utenti non possono aprire i file con il protocollo ClickOnce. Il file verrà invece salvato nel file system utilizzando il browser. Questi criteri sostituiscono l'impostazione ClickOnce dell'utente nella pagina edge://flags/.

Se non configuri questi criteri, gli utenti con versioni di Microsoft Edge precedenti a Microsoft Edge 87 non possono aprire i file utilizzando il protocollo ClickOnce per impostazione predefinita. Tuttavia, hanno l'opzione per abilitare l'uso del protocollo ClickOnce con la pagina edge://flags/. Gli utenti con Microsoft Edge versione 87 e successive possono aprire i file utilizzando il protocollo ClickOnce per impostazione predefinita, ma hanno la possibilità di disabilitare il protocollo ClickOnce con la pagina edge://flags/.

La disabilitazione di ClickOnce può impedire l'avvio corretto delle applicazioni ClickOnce (file .application).

Per ulteriori informazioni su ClickOnce, vedi [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) e [https://go.microsoft.com/fwlink/?linkid=2099880](https://go.microsoft.com/fwlink/?linkid=2099880).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ClickOnceEnabled
  - Nome GP: Consenti agli utenti di aprire file tramite il protocollo ClickOnce
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ClickOnceEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### CollectionsServicesAndExportsBlockList
  #### Blocca l'accesso a un elenco di servizi specifici ed esporta destinazioni in Raccolte
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Elenca servizi specifici ed esporta destinazioni cui gli utenti non possono accedere nella funzionalità Raccolte in Microsoft Edge. Include la visualizzazione di dati aggiuntivi di Bing e l'esportazione di raccolte in prodotti Microsoft o partner esterni.

Se abiliti questo criterio, i servizi e le destinazioni di esportazione corrispondenti all'elenco specificato saranno bloccati.

Se non configuri questa impostazione dei criteri, non verranno applicate restrizioni per i servizi accettabili e le destinazioni di esportazione.

Mappatura opzioni criteri:

* pinterest_suggestions (pinterest_suggestions) = Suggerimenti Pinterest

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: CollectionsServicesAndExportsBlockList
  - Nome GP: Blocca l'accesso a un elenco di servizi specifici ed esporta destinazioni in Raccolte
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\1 = "pinterest_suggestions"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: CollectionsServicesAndExportsBlockList
  - Valore di esempio:
``` xml
<array>
  <string>pinterest_suggestions</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### CommandLineFlagSecurityWarningsEnabled
  #### Abilita gli avvisi di sicurezza per i flag della riga di comando
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 78 o in seguito

  #### Descrizione
  Se disabilitato, questo criterio impedisce la visualizzazione degli avvisi di sicurezza quando Microsoft Edge verrà avviato con flag della riga di comando potenzialmente pericolosi.

Se abilitato o non impostato, gli avvisi di sicurezza verranno visualizzati quando questi flag della riga di comando vengono utilizzati per avviare Microsoft Edge.

Ad esempio, il flag --disable-gpu-sandbox genera questo avviso: Stai utilizzando un flag della riga di comando non supportato--disable-gpu-sandbox. Questa azione comporta rischi di stabilità e sicurezza.

Questo criterio è disponibile solo per le istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: CommandLineFlagSecurityWarningsEnabled
  - Nome GP: Abilita gli avvisi di sicurezza per i flag della riga di comando
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: CommandLineFlagSecurityWarningsEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: CommandLineFlagSecurityWarningsEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ComponentUpdatesEnabled
  #### Abilita gli aggiornamenti dei componenti in Microsoft Edge
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Se abiliti o non configuri questi criteri, gli aggiornamenti dei componenti sono abilitati in Microsoft Edge.

Se questi criteri vengono disabilitati o impostati su false, gli aggiornamenti dei componenti sono disabilitati per tutti i componenti in Microsoft Edge.

Alcuni componenti non sono tuttavia interessati da questi criteri, incluso qualsiasi componente che non contenga codice eseguibile, che non alteri in modo significativo il comportamento del browser o che sia fondamentale per la sicurezza. Gli aggiornamenti che sono considerati "critici per la sicurezza" vengono comunque applicati anche se disabiliti questi criteri.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ComponentUpdatesEnabled
  - Nome GP: Abilita gli aggiornamenti dei componenti in Microsoft Edge
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ComponentUpdatesEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ComponentUpdatesEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ConfigureDoNotTrack
  #### Configura Non tenere traccia
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica se inviare richieste Non tenere traccia ai siti Web che richiedono info di registrazione. Le richieste Non tenere traccia consentono ai siti Web visitati di sapere se non vuoi che la tua attività di esplorazione vena registrata. Per impostazione predefinita, Microsoft Edge non invia nessuna richiesta Non tenere traccia, ma gli utenti possono attivare questa funzionalità per inviarle.

Se abiliti questi criteri, le richieste Non tenere traccia vengono sempre inviate ai siti Web che richiedono info di registrazione.

Se disabiliti questi criteri, le richieste non vengono mai inviate.

Se non configuri questi criteri, gli utenti possono scegliere se inviare le richieste.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ConfigureDoNotTrack
  - Nome GP: Configura Non tenere traccia
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ConfigureDoNotTrack
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ConfigureDoNotTrack
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ConfigureOnPremisesAccountAutoSignIn
  #### Configura l'accesso automatico con un account di dominio di Active Directory quando non è disponibile un account di dominio di Azure AD
  
  
  #### Versioni supportate:
  - Su Windows dal 81 o successiva

  #### Descrizione
  Abilita l'uso degli account Active Directory per l'accesso automatico se i computer degli utenti sono aggiunti a un dominio e l'ambiente non è aggiunto a un dominio ibrido. Se desideri che gli utenti accedano invece automaticamente con i loro account Azure Active Directory, esegui aggiungi al dominio Azure AD (vedi [https://go.microsoft.com/fwlink/?linkid=2118197](https://go.microsoft.com/fwlink/?linkid=2118197) per altre informazioni) o alla distribuzione ibrida (vedere [https://go.microsoft.com/fwlink/?linkid=2118365](https://go.microsoft.com/fwlink/?linkid=2118365) per ulteriori informazioni) il tuo ambiente.

Se hai configurato i criteri [BrowserSignin](#browsersignin) come disabilitati, questi criteri non avranno effetto.

Se abiliti questi criteri e li imposti su "Accedi e rendi account di dominio non rimovibile", Microsoft Edge eseguirà automaticamente l'accesso degli utenti nei computer aggiunti al dominio tramite i relativi account di Active Directory.

Se imposti questi criteri su "Disabled" o non li imposti,  Microsoft Edge non eseguirà automaticamente l'accesso degli utenti su computer aggiunti a un dominio con account Active Directory.

Mappatura opzioni criteri:

* Disabled (0) = Disabilitato

* SignInAndMakeDomainAccountNonRemovable (1) = Accedi e rendi account di dominio non rimovibile

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ConfigureOnPremisesAccountAutoSignIn
  - Nome GP: Configura l'accesso automatico con un account di dominio di Active Directory quando non è disponibile un account di dominio di Azure AD
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ConfigureOnPremisesAccountAutoSignIn
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ConfigureOnlineTextToSpeech
  #### Configura la sintesi vocale online
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica se il browser può sfruttare i caratteri voce di Sintesi vocale online, parte di Servizi cognitivi di Azure. Questi caratteri voce sono di qualità superiore rispetto ai caratteri voce di sistema preinstallati.

Se abiliti o non configuri questi criteri, le applicazioni basate sul Web che utilizzano l'API SpeechSynthesis possono utilizzare i caratteri voce di Sintesi vocale online.

Se disabiliti questi criteri, i caratteri voce non sono disponibili.

Leggi altre informazioni su questa funzionalità in:
API SpeechSynthesis: [https://go.microsoft.com/fwlink/?linkid=2110038](https://go.microsoft.com/fwlink/?linkid=2110038)
Servizi cognitivi: [https://go.microsoft.com/fwlink/?linkid=2110141](https://go.microsoft.com/fwlink/?linkid=2110141)

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ConfigureOnlineTextToSpeech
  - Nome GP: Configura la sintesi vocale online
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ConfigureOnlineTextToSpeech
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ConfigureOnlineTextToSpeech
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ConfigureShare
  #### Configura l'esperienza di condivisione
  
  
  #### Versioni supportate:
  - Su Windows dal 83 o successiva

  #### Descrizione
  Se imposti questi criteri su "ShareAllowed" (il valore predefinito), gli utenti potranno accedere all'esperienza di condivisione di Windows 10 dal menu Impostazioni e altro in Microsoft Edge per condividere con altre app nel sistema.

Se imposti questi criteri su "ShareDisallowed", gli utenti non potranno accedere all'esperienza di condivisione di Windows 10. Se il pulsante Condividi è sulla barra degli strumenti, anche questo verrà nascosto.

Mappatura opzioni criteri:

* ShareAllowed (0) = Consenti l'uso dell'esperienza di condivisione

* ShareDisallowed (1) = Non consentire l'utilizzo dell'esperienza di condivisione

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ConfigureShare
  - Nome GP: Configura l'esperienza di condivisione
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ConfigureShare
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### CustomHelpLink
  #### Specifica il collegamento della Guida personalizzato
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 79 o in seguito

  #### Descrizione
  Specifica un collegamento per il menu ? o il tasto F1.

Se abiliti questo criterio, un amministratore potrà specificare un collegamento per il menu? o il tasto F1.

Se si disabiliti o non configuri questo criterio, verrà utilizzato il collegamento predefinito per il menu ? o il tasto F1.

Questo criterio è disponibile solo per le istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: CustomHelpLink
  - Nome GP: Specifica il collegamento della Guida personalizzato
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: CustomHelpLink
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"https://go.microsoft.com/fwlink/?linkid=2080734"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: CustomHelpLink
  - Valore di esempio:
``` xml
<string>https://go.microsoft.com/fwlink/?linkid=2080734</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DNSInterceptionChecksEnabled
  #### Controlli intercettazione DNS abilitati
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 80 o in seguito

  #### Descrizione
  Questi criteri configurano un opzione locale che può essere utilizzata per disabilitare i controlli di intercettazione DNS. Questi controlli tentano di individuare se il browser si trova dietro un proxy che reindirizza nomi host sconosciuti.

Questo rilevamento potrebbe non essere necessario in un ambiente aziendale in cui è nota la configurazione di rete. Può essere disabilitato per evitare traffico DNS e HTTP aggiuntivo all'avvio e a ogni modifica della configurazione DNS.

Se abiliti o non imposti questi criteri, verranno eseguiti i controlli di intercettazione DNS.

Se disabiliti questa impostazione dei criteri, i controlli di intercettazione DNS non verranno eseguiti.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DNSInterceptionChecksEnabled
  - Nome GP: Controlli intercettazione DNS abilitati
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DNSInterceptionChecksEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DNSInterceptionChecksEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultBrowserSettingEnabled
  #### Imposta Microsoft Edge come browser predefinito
  
  
  #### Versioni supportate:
  - Su Windows 7 e macOS dal 77 o in seguito

  #### Descrizione
  Se imposti questo criterio su True, Microsoft Edgecontrollerà sempre se si tratta del browser predefinito all'avvio e, se possibile, si registrerà automaticamente.

Se imposti questo criterio su False, a Microsoft Edgeviene impedito di verificare se è l'impostazione predefinita e disattiverà i controlli utente per questa opzione.

Se non imposti questo criterio, Microsoft Edgeconsentirà agli utenti di controllare se è l'impostazione predefinita e, in caso contrario, se devono essere visualizzate le notifiche degli utenti.

Nota per gli amministratori di Windows: questi criteri funzionano solo per i PC con Windows 7. Per le versioni successive di Windows è necessario distribuire un file di "associazioni di applicazioni predefinite" che consente a Microsoft Edge di gestire i protocolli HTTPS e HTTP (e facoltativamente il protocollo ftp e i formati di file quali .html, .htm, .pdf, .svg, .webp). Per ulteriori informazioni, vedi [https://go.microsoft.com/fwlink/?linkid=2094932](https://go.microsoft.com/fwlink/?linkid=2094932).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultBrowserSettingEnabled
  - Nome GP: Imposta Microsoft Edge come browser predefinito
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DefaultBrowserSettingEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultBrowserSettingEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultSearchProviderContextMenuAccessAllowed
  #### Consenti accesso predefinito al menu di scelta rapida del provider di ricerca
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 85 o in seguito

  #### Descrizione
  Consente l'uso di un provider di ricerca predefinito nel menu di scelta rapida.

Se imposti questo criterio su disabilitato, la voce di ricerca del menu di scelta rapida basata sul provider di ricerca predefinito e la ricerca della barra laterale non saranno disponibili.

Se questo criterio è abilitato o non impostato, la voce del menu di scelta rapida per il provider di ricerca predefinito e la ricerca nella barra laterale saranno disponibili.

Il valore dei criteri viene applicato solo quando il criterio [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) è abilitato e non è applicabile in caso contrario.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultSearchProviderContextMenuAccessAllowed
  - Nome GP: Consenti accesso predefinito al menu di scelta rapida del provider di ricerca
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DefaultSearchProviderContextMenuAccessAllowed
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultSearchProviderContextMenuAccessAllowed
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultSensorsSetting
  #### Impostazione predefinite dei sensori
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Imposta se i siti Web possono accedere e utilizzare sensori come i sensori di movimento e di luce. Puoi bloccare completamente o consentire ai siti Web di accedere ai sensori.

Impostando il criterio su 1 si consente ai siti Web di accedere e utilizzare i sensori. Impostando il criterio su 2 si nega l'accesso ai sensori.

 Puoi sostituire questo criterio per pattern URL specifici utilizzando i criteri [SensorsAllowedForUrls](#sensorsallowedforurls) e [SensorsBlockedForUrls](#sensorsblockedforurls).

 Se non configuri questo criterio, i siti Web possono accedere e utilizzare i sensori e gli utenti possono modificare questa impostazione. Questa è l'impostazione predefinita globale per [SensorsAllowedForUrls](#sensorsallowedforurls) e [SensorsBlockedForUrls](#sensorsblockedforurls).

Mappatura opzioni criteri:

* AllowSensors (1) = Consenti ai siti di accedere ai sensori

* BlockSensors (2) = Non consentire l'accesso ai sensori a nessun sito

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultSensorsSetting
  - Nome GP: Impostazione predefinite dei sensori
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DefaultSensorsSetting
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultSensorsSetting
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DefaultSerialGuardSetting
  #### Controlla l'uso dell'API seriale
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Specifica se i siti Web possono accedere alle porte seriali. È possibile bloccare completamente l'accesso o chiedere all'utente ogni volta che un sito Web vuole ottenere l'accesso a una porta seriale.

Impostando il criterio su 3 si consente ai siti Web di richiedere l'accesso alle porte seriali. Impostando il criterio su 2 si nega l'accesso alle porte seriali.

È possibile eseguire l'override di questo criterio per specifici schemi di URL usando i criteri [SerialAskForUrls](#serialaskforurls) e [SerialBlockedForUrls](#serialblockedforurls).

Se non configuri questo criterio, per impostazione predefinita i siti Web possono chiedere agli utenti se possono accedere a una porta seriale e gli utenti possono modificare questa impostazione.

Mappatura opzioni criteri:

* BlockSerial (2) = Non consentire ad alcun sito di richiedere l'accesso alle porte seriali tramite l'API seriale

* AskSerial (3) = Consenti ai siti di chiedere l'autorizzazione dell'utente per accedere a una porta seriale

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DefaultSerialGuardSetting
  - Nome GP: Controlla l'uso dell'API seriale
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DefaultSerialGuardSetting
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DefaultSerialGuardSetting
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DelayNavigationsForInitialSiteListDownload
  #### È necessario che l'elenco dei siti in modalità Enterprise sia disponibile prima dell'esplorazione nella scheda
  
  
  #### Versioni supportate:
  - Su Windows dal 84 o successiva

  #### Descrizione
  Consente di specificare se le schede di Microsoft Edge attendono di essere disponibili per l'esplorazione finché il browser non ha scaricato l'elenco dei siti in modalità Enterprise iniziale. Questa impostazione è destinata allo scenario in cui la home page del browser deve essere caricata in modalità Internet Explorer ed è importante farlo alla prima esecuzione del browser dopo l'attivazione della modalità IE. Se questo scenario non esiste, consigliamo di non abilitare questa impostazione perché può influire negativamente sulle prestazioni del caricamento della home page. L'impostazione si applica solo quando Microsoft Edge non dispone di un Elenco siti in modalità Enterprise memorizzato nella cache, ad esempio alla prima esecuzione del browser dopo l'attivazione della modalità IE.

       Questa impostazione funziona insieme a:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) è impostato in "modalità Internet Explorer"
       e sul criterio
[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) in cui l'elenco contiene almeno una voce.

       Il comportamento di timeout di questo criterio può essere configurato con il criterio [NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout).

       Se imposti questo criterio su All, quando Microsoft Edge non ha una versione memorizzata nella cache dell'elenco dei siti in modalità Enterprise, le schede ritardano l'esplorazione fino a quando il browser non ha scaricato l'elenco dei siti. I siti configurati per l'apertura in modalità Internet Explorer dall'elenco dei siti verranno caricati in modalità Internet Explorer, anche durante l'esplorazione iniziale del browser. I siti che non possono essere configurati per l'apertura in Internet Explorer, come qualsiasi sito con uno schema diverso da http:, https:, file: o ftp: non ritardano l'esplorazione e si caricano immediatamente in modalità Edge.

       Se imposti questo criterio su “None” o non lo configuri, quandoMicrosoft Edge non dispone di una versione memorizzata nella cache dell'elenco dei siti in modalità Enterprise, le schede sono immediatamente disponibili per l'esplorazione e non attendono che il browser scarichi l'elenco dei siti in modalità Enterprise. I siti configurati per l'apertura in modalità Internet Explorer dall'elenco dei siti si apriranno in modalità Microsoft Edge fino a quando il browser non avrà completato il download dell'elenco dei siti in modalità Enterprise.

Mappatura opzioni criteri:

* None (0) = Nessuno

* All (1) = Tutte le esplorazioni disponibili

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DelayNavigationsForInitialSiteListDownload
  - Nome GP: È necessario che l'elenco dei siti in modalità Enterprise sia disponibile prima dell'esplorazione nella scheda
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DelayNavigationsForInitialSiteListDownload
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DeleteDataOnMigration
  #### Elimina i dati del browser datati durante la migrazione
  
  
  #### Versioni supportate:
  - Su Windows dal 83 o successiva

  #### Descrizione
  Questi criteri determinano se i dati di esplorazione degli utenti da Microsoft Edge Legacy verranno eliminati dopo la migrazione a Microsoft Edge versione 81 o successiva.

Se imposti questi criteri su "Abilitato", tutti i dati di esplorazione da Microsoft Edge Legacy dopo la migrazione a Microsoft Edge versione 81 o successiva verranno eliminati. È necessario impostare questi criteri prima di eseguire la migrazione a Microsoft Edge versione 81 o successiva per avere effetto sui dati di esplorazione esistenti.

Se imposti questi criteri su "Disabilitato" o i criteri non vengono configurati, i dati di esplorazione degli utenti non vengono eliminati dopo la migrazione a Microsoft Edge versione 83 o successiva.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DeleteDataOnMigration
  - Nome GP: Elimina i dati del browser datati durante la migrazione
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DeleteDataOnMigration
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DeveloperToolsAvailability
  #### Controlla dove possono essere utilizzati gli strumenti di sviluppo
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Controlla dove possono essere utilizzati gli strumenti di sviluppo.

Se imposti questi criteri su "DeveloperToolsDisallowedForForceInstalledExtensions" (predefinito), gli utenti possono accedere agli strumenti di sviluppo e alla console JavaScript in generale, ma non nel contesto delle estensioni installate dai criteri aziendali.

Se imposti questi criteri su "DeveloperToolsAllowed", gli utenti possono accedere agli strumenti di sviluppo e alla console JavaScript in tutti i contesti, incluse le estensioni installate dai criteri aziendali.

Se imposti questi criteri su "DeveloperToolsDisallowed", gli utenti non possono accedere agli strumenti di sviluppo o ispezionare gli elementi del sito Web. I tasti di scelta rapida e le voci dei menu o dei menu contestuali che aprono gli strumenti di sviluppo o la console JavaScript sono disabilitati.

Mappatura opzioni criteri:

* DeveloperToolsDisallowedForForceInstalledExtensions (0) = Blocca gli strumenti di sviluppo per le estensioni installate dai criteri aziendali, consenti in altri contesti

* DeveloperToolsAllowed (1) = Consenti l'uso degli strumenti di sviluppo

* DeveloperToolsDisallowed (2) = Non consentire l'utilizzo degli strumenti di sviluppo

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DeveloperToolsAvailability
  - Nome GP: Controlla dove possono essere utilizzati gli strumenti di sviluppo
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DeveloperToolsAvailability
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DeveloperToolsAvailability
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DiagnosticData
  #### Invia dati di diagnostica obbligatori e facoltativi sull’uso del browser
  
  
  #### Versioni supportate:
  - Su Windows 7 e macOS dal 86 o in seguito

  #### Descrizione
  Questo criterio controlla l'invio dei dati di diagnostica obbligatori e facoltativi relativi all'utilizzo del browser a Microsoft.

I dati di diagnostica obbligatori vengono raccolti per mantenere Microsoft Edge sicuro, aggiornato e garantire le prestazioni previste.

I dati di diagnostica facoltativi includono i dati sull'utilizzo del browser, i siti Web visitati e i report sugli arresti anomali, inviati a Microsoft per il miglioramento di prodotti e servizi.

Questo criterio non è supportato nei dispositivi Windows 10. Per controllare questa raccolta di dati in Windows 10, gli amministratori IT devono usare i criteri di gruppo per i dati di diagnostica di Windows. Questo criterio può essere "Consenti telemetria" o "Consenti dati di diagnostica", in base alla versione di Windows. Altre informazioni sulla raccolta di dati di diagnostica per Windows 10: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

Usa una delle impostazioni seguenti per configurare il criterio:

'Off' disattiva la raccolta dei dati di diagnostica obbligatori e facoltativi. Questa opzione non è consigliabile.

'RequiredData' invia i dati di diagnostica obbligatori, ma disattiva la raccolta dei dati di diagnostica facoltativi. Microsoft Edge invierà i dati di diagnostica obbligatori per mantenere Microsoft Edge sicuro, aggiornato e garantire le prestazioni previste.

'OptionalData' invia i dati di diagnostica facoltativi, che includono dati sull'utilizzo del browser, i siti Web visitati e i report sugli arresti anomali, inviati a Microsoft per il miglioramento di prodotti e servizi.

In Windows 7/macOS, questo criterio controlla l'invio dei dati obbligatori e facoltativi a Microsoft.

Se non configuri questo criterio o lo disabiliti, Microsoft Edge userà per impostazione predefinita le preferenze dell'utente.

Mappatura opzioni criteri:

* Off (0) = Disattivato (non consigliato)

* RequiredData (1) = Dati obbligatori

* OptionalData (2) = Dati facoltativi

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DiagnosticData
  - Nome GP: Invia dati di diagnostica obbligatori e facoltativi sull’uso del browser
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DiagnosticData
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DiagnosticData
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DirectInvokeEnabled
  #### Consenti agli utenti di aprire file tramite il protocollo DirectInvoke
  
  
  #### Versioni supportate:
  - Su Windows dal 78 o successiva

  #### Descrizione
  Consenti agli utenti di aprire i file tramite il protocollo DirectInvoke. Il protocollo DirectInvoke consente ai siti Web di richiedere che il browser apra i file da un URL specifico utilizzando un gestore di file specifico nel computer o nel dispositivo dell'utente.

Se abiliti o non configuri questi criteri, gli utenti possono aprire i file usando il protocollo DirectInvoke.

Se disabiliti questi criteri, gli utenti non possono aprire i file tramite il protocollo DirectInvoke. I file vengono invece salvati nel file system.

Nota: la disabilitazione di DirectInvoke può impedire il funzionamento previsto di determinate funzionalità di Microsoft Office SharePoint Online.

Per ulteriori informazioni su DirectInvoke, vedi [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) e [https://go.microsoft.com/fwlink/?linkid=2099871](https://go.microsoft.com/fwlink/?linkid=2099871).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DirectInvokeEnabled
  - Nome GP: Consenti agli utenti di aprire file tramite il protocollo DirectInvoke
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DirectInvokeEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### Disable3DAPIs
  #### Disabilita il supporto per le API di grafica 3D
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Impedisci alle pagine Web di accedere all'unità di elaborazione grafica (GPU). In particolare, le pagine Web non possono accedere all'API WebGL e i plug-in non possono utilizzare l'API 3D Pepper.

Se non configuri o disabiliti questi criteri, le pagine Web possono potenzialmente utilizzare l'API WebGL e i plug-in possono utilizzare l'API 3D Pepper. Microsoft Edge potrebbe comunque richiedere, per impostazione predefinita, il passaggio degli argomenti della riga di comando per poter utilizzare le API.

Se i criteri [HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled) sono impostati su false, l'impostazione dei criteri "'Disable3DAPIs" viene ignorata: ciò equivale all'impostazione dei criteri [Disable3DAPIs](#disable3dapis) su true.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: Disable3DAPIs
  - Nome GP: Disabilita il supporto per le API di grafica 3D
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: Disable3DAPIs
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: Disable3DAPIs
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DisableScreenshots
  #### Disabilita l'acquisizione di screenshot
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Controlla se gli utenti possono acquisire screenshot della pagina del browser.

Se abiliti questi criteri, l'utente non può acquisire screenshot utilizzando i tasti di scelta rapida o le API di estensione.

Se disabiliti o non configuri questi criteri, gli utenti possono acquisire screenshot.

Tieni presente che questi criteri controllano gli screenshot acquisiti dal browser. Anche se abiliti questi criteri, gli utenti potrebbero comunque essere in grado di acquisire schermate usando un metodo diverso dal browser (ad esempio una funzione del sistema operativo o un'altra applicazione).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DisableScreenshots
  - Nome GP: Disabilita l'acquisizione di screenshot
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DisableScreenshots
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DisableScreenshots
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DiskCacheDir
  #### Imposta directory cache disco
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Configura la directory da utilizzare per archiviare i file memorizzati nella cache.

Se abiliti questi criteri, Microsoft Edge utilizza la directory specificata indipendentemente dal flag "--disk-cache-dir" eventualmente specificato dall'utente. Per evitare la perdita di dati o altri errori imprevisti, non configurare questi criteri per la directory radice di un volume o una directory utilizzata per altri scopi, perché Microsoft Edge ne gestisce il contenuto.

Visita la pagina [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) per un elenco di variabili da utilizzare quando specifichi le directory e i percorsi.

Se non configuri questi criteri, viene utilizzata la directory della cache predefinita e gli utenti possono sostituire tale impostazione predefinita con il flag della riga di comando "--disk-cache-dir".

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DiskCacheDir
  - Nome GP: Imposta directory cache disco
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DiskCacheDir
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"${user_home}/Edge_cache"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DiskCacheDir
  - Valore di esempio:
``` xml
<string>${user_home}/Edge_cache</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DiskCacheSize
  #### Imposta le dimensioni della cache disco, in byte
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Configura le dimensioni in byte della cache utilizzata per archiviare i file sul disco.

Se abiliti questi criteri, Microsoft Edge utilizza le dimensioni della cache specificate, indipendentemente dal flag "--disk-cache-size" eventualmente specificato dall'utente. Il valore specificato nei criteri non è un limite rigido, piuttosto un suggerimento per il sistema di memorizzazione nella cache. Se un valore è troppo basso perché inferiore di pochi MB, viene arrotondato al minimo ragionevole.

Se imposti questi criteri su 0, vengono utilizzate le dimensioni predefinite della cache e gli utenti non possono modificare l'impostazione.

Se non configuri questi criteri, viene utilizzata la dimensione predefinita, ma gli utenti possono sostituirla usando il flag "--disk-cache-size".

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DiskCacheSize
  - Nome GP: Imposta le dimensioni della cache disco, in byte
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DiskCacheSize
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x06400000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DiskCacheSize
  - Valore di esempio:
``` xml
<integer>104857600</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DnsOverHttpsMode
  #### Controlla la modalità di DNS su HTTPS
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 83 o in seguito

  #### Descrizione
  Controlla la modalità del resolver DNS su HTTPS. Questo criterio imposta solo la modalità predefinita per ogni query. È possibile eseguire l'override della modalità per tipi di query speciali, ad esempio le richieste di risoluzione di un nome host di server DNS su HTTPS.

Con la modalità "off" DNS su HTTPS verrà disabilitato.

Con la modalità "automatic" le query DNS su HTTPS verranno inviate per prime se è disponibile un server DNS su HTTPS ed è possibile che venga eseguito il fallback all'invio di query non sicure in caso di errore.

Con la modalità "secure" verranno inviate solo query DNS su HTTPS e che non verranno risolte in caso di errore.

Se questo criterio non viene configurato, il browser potrebbe inviare richieste DNS su HTTPS a un resolver associato al resolver di sistema configurato dell'utente.

Mappatura opzioni criteri:

* off (off) = Disabilita DNS su HTTPS

* automatic (automatic) = Abilita DNS su HTTPS con fallback non sicuro

* secure (secure) = Abilita DNS su HTTPS senza fallback non sicuro

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DnsOverHttpsMode
  - Nome GP: Controlla la modalità di DNS su HTTPS
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DnsOverHttpsMode
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"off"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DnsOverHttpsMode
  - Valore di esempio:
``` xml
<string>off</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DnsOverHttpsTemplates
  #### Specificare il modello URI del resolver DNS-over-HTTPS desiderato
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 83 o in seguito

  #### Descrizione
  Modello di URI del resolver DNS su HTTPS desiderato. Per specificare più resolver DNS su HTTPS, separa con uno spazio i modelli di URI corrispondenti.

Se imposti [DnsOverHttpsMode](#dnsoverhttpsmode) su "secure", questo criterio deve essere impostato e non può essere vuoto.

Se imposti [DnsOverHttpsMode](#dnsoverhttpsmode) su "automatic" e questo criterio è impostato, verranno usati i modelli di URI specificati. Se non imposti questo criterio, verranno usati i mapping hardcoded per provare ad aggiornare il resolver DNS corrente dell'utente in un resolver DNS su HTTPS DoH gestito dallo stesso provider.

Se il modello di URI contiene una variabile dns, nelle richieste al resolver verrà usato GET; in caso contrario verrà usato POST.

I modelli formattati in modo errato verranno ignorati.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DnsOverHttpsTemplates
  - Nome GP: Specificare il modello URI del resolver DNS-over-HTTPS desiderato
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: DnsOverHttpsTemplates
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"https://dns.example.net/dns-query{?dns}"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DnsOverHttpsTemplates
  - Valore di esempio:
``` xml
<string>https://dns.example.net/dns-query{?dns}</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DownloadDirectory
  #### Imposta directory di download
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Configura la directory da utilizzare per il download dei file.

Se abiliti questi criteri, Microsoft Edge utilizza la directory specificata indipendentemente dal fatto che l'utente ne abbia specificata una o che abbia scelto di ricevere ogni volta una richiesta di conferma per il percorso di download. Vedi [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) per un elenco delle variabili che possono essere utilizzate.

Se disabiliti o non configuri questo criterio, viene utilizzata la directory di download predefinita e l'utente può modificarla.

Se è impostato un percorso non valido, Microsoft Edge utilizzerà per impostazione predefinita la directory di download predefinita dell'utente.

Se la cartella specificata dal percorso non esiste, il download attiverà un prompt con cui viene richiesto all'utente dove desidera salvare il download.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DownloadDirectory
  - Nome GP: Imposta directory di download
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: DownloadDirectory
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"\n      Linux-based OSes (including Mac): /home/${user_name}/Downloads\n      Windows: C:\\Users\\${user_name}\\Downloads"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DownloadDirectory
  - Valore di esempio:
``` xml
<string>
      Linux-based OSes (including Mac): /home/${user_name}/Downloads
      Windows: C:\Users\${user_name}\Downloads</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### DownloadRestrictions
  #### Consenti le restrizioni di download
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Configura il tipo di download che Microsoft Edge blocca completamente, senza consentire agli utenti di ignorare la decisione sulla sicurezza.

Imposta "Blocca download pericolosi" per consentire tutti i download ad eccezione di quelli che contengono avvisi di Microsoft Defender SmartScreen.

Imposta "Blocca download potenzialmente pericolosi" per consentire tutti i download ad eccezione di quelli che includono avvisi di Microsoft Defender SmartScreen per i download potenzialmente pericolosi o indesiderati.

Imposta "Blocca tutti i download" per bloccare tutti i download.

Se non configuri questi criteri o imposti l'opzione "Sicurezza download predefinita", i download passano attraverso le consuete restrizioni di sicurezza basate sui risultati dell'analisi di Microsoft Defender SmartScreen.

Tieni presente che queste restrizioni si applicano ai download di contenuti della pagina Web, nonché all'opzione di menu di scelta rapida "Collegamento di download...". Queste restrizioni non si applicano al salvataggio o al download della pagina attualmente visualizzata e non si applicano all'opzione Salva come PDF delle opzioni di stampa.

Per ulteriori informazioni su Microsoft Defender SmartScreen, vedi [https://go.microsoft.com/fwlink/?linkid=2094934](https://go.microsoft.com/fwlink/?linkid=2094934).

Mappatura opzioni criteri:

* DefaultDownloadSecurity (0) = Nessuna restrizione speciale

* BlockDangerousDownloads (1) = Blocca i download pericolosi

* BlockPotentiallyDangerousDownloads (2) = Blocca i download potenzialmente pericolosi o indesiderati

* BlockAllDownloads (3) = Blocca tutti i download

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: DownloadRestrictions
  - Nome GP: Consenti le restrizioni di download
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: DownloadRestrictions
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: DownloadRestrictions
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### EdgeCollectionsEnabled
  #### Abilita la funzionalità Raccolte
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 78 o in seguito

  #### Descrizione
  Consente di autorizzare l'accesso degli utenti alla funzionalità Raccolte con cui possono raccogliere, organizzare, condividere ed esportare i contenuti in modo più efficiente e con l'integrazione di Office.

Se abiliti o non configuri questi criteri, gli utenti possono accedere e usare la funzionalità Raccolte in Microsoft Edge.

Se disabiliti questi criteri, gli utenti non possono accedere e usare la funzionalità Raccolte in Microsoft Edge.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: EdgeCollectionsEnabled
  - Nome GP: Abilita la funzionalità Raccolte
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: EdgeCollectionsEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: EdgeCollectionsEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### EditFavoritesEnabled
  #### Consente agli utenti di modificare i Preferiti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Abilita questi criteri per consentire agli utenti di aggiungere, rimuovere e modificare i preferiti. Questo è il comportamento predefinito se non configuri i criteri.

Disabilita questi criteri per impedire agli utenti di aggiungere, rimuovere o modificare i preferiti. I preferiti esistenti possono comunque essere utilizzati.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: EditFavoritesEnabled
  - Nome GP: Consente agli utenti di modificare i Preferiti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: EditFavoritesEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: EditFavoritesEnabled
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### EnableDeprecatedWebPlatformFeatures
  #### Riattiva le funzionalità della piattaforma Web deprecate per un periodo di tempo limitato
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica un elenco delle funzionalità deprecate della piattaforma Web da riabilitare temporaneamente.

Questi criteri consentono di abilitare di nuovo le funzionalità deprecate della piattaforma Web per un periodo di tempo limitato. Le funzionalità sono identificate da un tag di stringa.

Se non configuri questi criteri, se l'elenco è vuoto oppure se una funzionalità non corrisponde a uno dei tag stringa supportati, tutte le funzionalità deprecate della piattaforma Web rimangono disabilitate.

Sebbene i criteri stessi siano supportati sulle piattaforme illustrate sopra, la funzionalità che si sta abilitando potrebbe non essere disponibile su tutte le piattaforme. Non tutte le funzionalità deprecate della piattaforma Web possono essere nuovamente abilitate. Solo quelle elencate in modo esplicito di seguito possono essere abilitate nuovamente e solo per un periodo di tempo limitato, che differisce a seconda della funzionalità. Puoi rivedere lo scopo dietro le modifiche della funzionalità della piattaforma Web su https://bit.ly/blinkintents.

Il formato generico del tag stringa è [DeprecatedFeatureName]_EffectiveUntil[yyyymmdd].

Mappatura opzioni criteri:

* ExampleDeprecatedFeature (ExampleDeprecatedFeature_EffectiveUntil20080902) = Abilita API ExampleDeprecatedFeature tramite 2008/09/02

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: EnableDeprecatedWebPlatformFeatures
  - Nome GP: Riattiva le funzionalità della piattaforma Web deprecate per un periodo di tempo limitato
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures\1 = "ExampleDeprecatedFeature_EffectiveUntil20080902"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: EnableDeprecatedWebPlatformFeatures
  - Valore di esempio:
``` xml
<array>
  <string>ExampleDeprecatedFeature_EffectiveUntil20080902</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### EnableDomainActionsDownload
  #### Abilita download azioni di dominio da Microsoft (obsoleto)
  
  >OBSOLETO: questo criterio è obsoleto e non funziona nelle versioni di Microsoft Edge successive alla versione 84.
  #### Versioni supportate:
  - Su Windows e macOS dal 77, fino al 84

  #### Descrizione
  Questo criterio non funziona perché è necessario evitare stati conflittuali. Sebbene questi criteri venissero utilizzati per abilitare/disabilitare il download dell'elenco di azioni di dominio, non sempre veniva raggiunto lo stato desiderato. Il servizio di sperimentazione e configurazione che gestisce il download dispone di criteri propri per configurare cosa viene scaricato dal servizio. Utilizza invece i criteri [ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol).

In Microsoft Edge, le azioni di dominio rappresentano una serie di funzionalità di compatibilità che contribuiscono al funzionamento corretto del browser sul Web.

Microsoft conserva un elenco di azioni da intraprendere su alcuni dominii per motivi di compatibilità. Ad esempio, il browser potrebbe ignorare la stringa Agente utente su un sito Web se tale sito Web è danneggiato a causa della nuova stringa Agente utente su Microsoft Edge. Ognuna di queste azioni è destinata a essere temporanea mentre Microsoft tenta di risolvere il problema con il proprietario del sito.

Quando il browser viene avviato la prima volta e periodicamente in momenti successivi, contatterà il servizio di sperimentazione e configurazione che contiene l'elenco più aggiornato delle azioni di compatibilità da eseguire. Questo elenco viene salvato in locale dopo che è stato prima recuperato in modo che le richieste successive aggiorneranno l'elenco solo se la copia sul server è cambiata.

Se abiliti questi criteri, l'elenco di azioni di dominio continuerà ad essere scaricato dal servizio di sperimentazione e configurazione.

Se disabiliti questi criteri, l'elenco delle azioni di dominio non verrà più scaricato dal servizio di sperimentazione e configurazione.

Se non configuri questi criteri, l'elenco delle azioni di dominio continuerà ad essere scaricato dal servizio di sperimentazione e configurazione.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: EnableDomainActionsDownload
  - Nome GP: Abilita download azioni di dominio da Microsoft (obsoleto)
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: EnableDomainActionsDownload
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: EnableDomainActionsDownload
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### EnableOnlineRevocationChecks
  #### Abilita i controlli CRL/OCSP online
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  I controlli sulle revoche online non forniscono un notevole vantaggio per la sicurezza e sono disabilitati per impostazione predefinita.

Se abiliti questi criteri, Microsoft Edge esegue i controlli CRL/OCSP online per gli errori non bloccanti. Per "errori non bloccanti" si intendono quelli per cui non è possibile raggiungere il server di revoca, il certificato verrà considerato valido.

Se disabiliti o non configuri questi criteri, Microsoft Edge non esegue i controlli sulle revoche online.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: EnableOnlineRevocationChecks
  - Nome GP: Abilita i controlli CRL/OCSP online
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: EnableOnlineRevocationChecks
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: EnableOnlineRevocationChecks
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### EnableSha1ForLocalAnchors
  #### Consenti certificati firmati con SHA-1 quando vengono emessi da Trust Anchor locali (deprecato)
  >DEPRECAtO: questi criteri sono deprecati. Sono attualmente supportati ma diventeranno obsoleti in una versione futura.
  
  #### Versioni supportate:
  - Su Windows e macOS dal 85 o in seguito

  #### Descrizione
  Se questa impostazione è abilitata, Microsoft Edge consente connessioni protette dai certificati firmati SHA-1 purché il certificato sia associato a un certificato radice installato localmente e sia valido.

 Tieni presente che questo criterio è applicabile se lo stack di verifica del certificato del sistema operativo consente le firme SHA-1. Se un aggiornamento del sistema operativo modifica la gestione da parte del sistema operativo dei certificati SHA-1, questo criterio potrebbe non avere effetto. Inoltre, questo criterio è inteso come soluzione alternativa temporanea che consente alle aziende di avere più tempo per non ricorrere più a SHA-1. Questo criterio verrà eliminato in Microsoft Edge 92, che verrà rilasciato a metà del 2021.

 Se non imposti questo criterio, lo imposti su falso oppure se il certificato SHA-1 è associato a un certificato radice attendibile, Microsoft Edge non consentirà certificati firmati da SHA-1.

Questo criterio è disponibile solo per le istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: EnableSha1ForLocalAnchors
  - Nome GP: Consenti certificati firmati con SHA-1 quando vengono emessi da Trust Anchor locali (deprecato)
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: EnableSha1ForLocalAnchors
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: EnableSha1ForLocalAnchors
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### EnterpriseHardwarePlatformAPIEnabled
  #### Consenti alle estensioni gestite di utilizzare l'API della piattaforma hardware aziendale
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 78 o in seguito

  #### Descrizione
  Quando questi criteri sono abilitati, le estensioni installate dai criteri dell'azienda sono autorizzate a utilizzare l'API della piattaforma hardware aziendale.
Quando questi criteri sono disabilitati o non impostati, nessuna estensione è autorizzata a utilizzare l'API della piattaforma hardware aziendale.
Questi criteri si applicano anche alle estensioni dei componenti.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: EnterpriseHardwarePlatformAPIEnabled
  - Nome GP: Consenti alle estensioni gestite di utilizzare l'API della piattaforma hardware aziendale
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: EnterpriseHardwarePlatformAPIEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: EnterpriseHardwarePlatformAPIEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### EnterpriseModeSiteListManagerAllowed
  #### Consenti l'accesso allo strumento Enterprise Mode Site List Manager
  
  
  #### Versioni supportate:
  - Su Windows dal 86 o successiva

  #### Descrizione
  Consente di specificare se Enterprise Mode Site List Manager è disponibile per gli utenti.

Se abiliti questi criteri, gli utenti potranno visualizzare il pulsante di spostamento di Enterprise Mode Site List Manager in edge://compat, passare allo strumento e utilizzarlo.

Se disabiliti o non configuri questi criteri, gli utenti non potranno visualizzare il pulsante di spostamento di Enterprise Mode Site List Manager e non potranno utilizzarlo.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: EnterpriseModeSiteListManagerAllowed
  - Nome GP: Consenti l'accesso allo strumento Enterprise Mode Site List Manager
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: EnterpriseModeSiteListManagerAllowed
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  #### Disabilita il download degli avvisi basati sull'estensione del tipo di file per i tipi di file specificati nei domini
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 85 o in seguito

  #### Descrizione
  Puoi abilitare questo criterio per creare un dizionario di estensioni di tipi di file con un elenco corrispondente di domini che non saranno interessati dagli avvisi di download basati sull’estensione del tipo di file. In questo modo, gli amministratore dell’organizzazione possono bloccare gli avvisi di download basati sull’estensione del tipo di file per file associati a un dominio elencato. Ad esempio, se l’estensione "jnlp" è associata a "website1.com", gli utenti non vedranno un avviso quando scaricheranno i file "jnlp" da "website1.com", ma vedranno un avviso di download quando scaricheranno i file "jnlp" da "website2.com".

I file con le estensioni dei tipi di file specificate per i domini identificati da questo criterio saranno comunque soggetti agli avvisi di sicurezza non basati sull’estensione del tipo di file, ad esempio avvisi di download di contenuto misto e avvisi di Microsoft Defender SmartScreen.

Se disabiliti questo criterio o non lo configuri, i tipi di file che scatenano gli avvisi di download basati sull’estensione mostreranno avvisi all’utente.

Se abiliti questo criterio:

*Il formato dell’URL deve seguire questo modello: [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).
*L’estensione di tipo di file immessa deve essere in caratteri ASCII in minuscolo. Il separatore principale non va incluso quando si elenca l’estensione del tipo di file, per cui va usato "jnlp" e non ".jnlp".

Esempio:

Il valore dell’esempio seguente evita gli avvisi di download basati sull’estensione del tipo di file per le estensioni swf, exe e jnlp per i domini *.contoso.com. Mostrerà all’utente un avviso di download basato sull’estensione del tipo di file su qualsiasi altro dominio per i file exe e jnlp, ma non per i file swf.

[
  { "file_extension": "jnlp", "domains": ["contoso.com"] },
  { "file_extension": "exe", "domains": ["contoso.com"] },
  { "file_extension": "swf", "domains": ["*"] }
]

È importante notare che, anche se l’esempio precedente mostra l’omissione degli avvisi di download basati sull’estensione di tipo di file per i file "swf" per tutti i domini, omettere tali avvisi per tutti i domini per estensioni di tipi di file pericolose è sconsigliata a causa di problemi di sicurezza. Viene mostrato nell’esempio semplicemente per dimostrare la possibilità di farlo.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Nome GP: Disabilita il download degli avvisi basati sull'estensione del tipo di file per i tipi di file specificati nei domini
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\1 = {"domains": ["https://contoso.com", "contoso2.com"], "file_extension": "jnlp"}
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\2 = {"domains": ["*"], "file_extension": "swf"}

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Valore di esempio:
``` xml
<array>
  <string>{'domains': ['https://contoso.com', 'contoso2.com'], 'file_extension': 'jnlp'}</string>
  <string>{'domains': ['*'], 'file_extension': 'swf'}</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ExperimentationAndConfigurationServiceControl
  #### Controlla le comunicazioni con il servizio di sperimentazione e configurazione
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  In Microsoft Edge, il servizio di sperimentazione e configurazione viene utilizzato per distribuire il payload di sperimentazione e configurazione.

Il payload di sperimentazione è costituito dall'elenco delle prime funzionalità di sviluppo che Microsoft abilita per il testing e il feedback.

Il payload di configurazione è costituito dall'elenco delle impostazioni che Microsoft desidera distribuire in Microsoft Edge per ottimizzare l'esperienza utente. Ad esempio, il payload di configurazione può specificare la frequenza con cui Microsoft Edge invia le richieste al servizio di sperimentazione e configurazione per recuperare il payload più recente.

Inoltre, il payload di configurazione potrebbe anche contenere un elenco di azioni da intraprendere su alcuni domini per motivi di compatibilità. Ad esempio, il browser potrebbe ignorare la stringa Agente utente su un sito Web se tale sito Web è danneggaiato a causa della nuova stringa Agente utente su Microsoft Edge. Ognuna di queste azioni è destinata ad essere temporanea mentre Microsoft tenta di risolvere il problema con il proprietario del sito.

Se imposti questi criteri sulla modalità "Modalità estesa", viene scaricato il payload completo dal servizio di sperimentazione e configurazione, ossia il payload di entrambe sperimentazione e configurazione.

Se imposti questi criteri sulla modalità "Solo configurazioni", viene recuperato solo il payload di configurazione.

Se imposti questi criteri su "Modalità con restrizioni", le comunicazioni con il servizio di sperimentazione e configurazione vengono completamente interrotte.

Se non configuri questi criteri, in un dispositivo gestito nei canali Stable e Beta, il comportamento è quello della "Modalità solo configurazioni".

Se non configuri questi criteri, il comportamento è quello della “Modalità estesa”.

Mappatura opzioni criteri:

* FullMode (2) = Recupera configurazioni ed esperimenti

* ConfigurationsOnlyMode (1) = Recupera solo configurazioni

* RestrictedMode (0) = Disabilita le comunicazioni con il servizio di sperimentazione e configurazione

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ExperimentationAndConfigurationServiceControl
  - Nome GP: Controlla le comunicazioni con il servizio di sperimentazione e configurazione
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ExperimentationAndConfigurationServiceControl
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ExperimentationAndConfigurationServiceControl
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ExternalProtocolDialogShowAlwaysOpenCheckbox
  #### Mostra una casella di controllo "Sempre aperto" nella finestra di dialogo del protocollo esterno.
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 79 o in seguito

  #### Descrizione
  Questo criterio controlla se la casella di controllo "Consenti sempre a questo sito di aprire collegamenti di questo tipo" è visualizzata nelle richieste di conferma dell'avvio del protocollo esterno. Questo criterio è valido solo sui link https://

Se abiliti questo criterio, quando viene visualizzata una richiesta di conferma del protocollo esterno, l'utente può selezionare "Consenti sempre" per ignorare tutte le future richieste di conferma del protocollo su questo sito.

Se disabiliti questo criterio, la casella di controllo "Consenti sempre" non viene visualizzata. All'utente verrà richiesta la conferma ogni volta che viene invocato un protocollo esterno.

Nelle versioni precedenti a Microsoft Edge 83, se non configuri questo criterio, la casella di controllo "Consenti sempre" non viene visualizzata. All'utente verrà richiesta la conferma ogni volta che viene invocato un protocollo esterno.

In Microsoft Edge 83, se non configuri questo criterio, la visibilità della casella di controllo dipende dal contrassegno "Abilita il promemoria per i preferiti che richiedono l'avvio del protocollo" in edge://flags

A partire da Microsoft Edge 84, Se non configuri questo criterio, quando viene visualizzata una richiesta di conferma del protocollo esterno, l'utente può selezionare "Consenti sempre" per ignorare tutte le future richieste di conferma del protocollo su questo sito.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Nome GP: Mostra una casella di controllo "Sempre aperto" nella finestra di dialogo del protocollo esterno.
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### FamilySafetySettingsEnabled
  #### Consenti agli utenti di configurare Family Safety
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 83 o in seguito

  #### Descrizione
  Questi criteri disabilitano e nascondono completamente la pagina di Family Safety in Impostazioni. Anche l'esplorazione su edge://settings/familysafety verrà bloccata. La pagina di Family Safety descrive le funzionalità disponibili per i gruppi di famiglia e la modalità di partecipazione a un gruppo familiare. Altre informazioni su Family Safety sono disponibili qui: ([https://go.microsoft.com/fwlink/?linkid=2098432](https://go.microsoft.com/fwlink/?linkid=2098432)).

Se abiliti o non configuri questi criteri, la pagina di Family Safety verrà visualizzata.

Se disabiliti questi criteri, la pagina di Family Safety non verrà visualizzata.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: FamilySafetySettingsEnabled
  - Nome GP: Consenti agli utenti di configurare Family Safety
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: FamilySafetySettingsEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: FamilySafetySettingsEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### FavoritesBarEnabled
  #### Abilita barra Preferiti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Attiva o disattiva la barra Preferiti.

Se abiliti questi criteri, gli utenti visualizzeranno la barra Preferiti.

Se disabiliti questi criteri, gli utenti non visualizzeranno la barra Preferiti.

Se questo criterio non è configurato, l'utente potrà decidere se utilizzare o meno la barra Preferiti.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: FavoritesBarEnabled
  - Nome GP: Abilita barra Preferiti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: FavoritesBarEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: FavoritesBarEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ForceBingSafeSearch
  #### Applica Ricerca sicura Bing
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Verifica che le query in Ricerca Web Bing vengano eseguite con Ricerca sicura impostata sul valore specificato. Gli utenti non possono modificare questa impostazione.

Se imposti questi criteri su "Modalità nessuna restrizione Ricerca sicura in Bing", Ricerca sicura in Ricerca Bing torna al valore bing.com.

Se imposti questi criteri su "Modalità moderata Ricerca sicura in Bing", viene utilizzata l'impostazione Media in Ricerca sicura. L'impostazione Media filtra video e immagini per adulti, ma non il testo dai risultati di ricerca.

Se imposti questi criteri su "Modalità restrttiva Ricerca sicura in Bing", viene utilizzata l'impostazione della modalità Strict di Ricerca sicura. L'impostazione Strict filtra testo, immagini e video per adulti.

Se disabiliti o non configuri questa impostazione, Ricerca sicura in Ricerca Bing non viene applicata e gli utenti possono impostare il valore che desiderano su bing.com.

Mappatura opzioni criteri:

* BingSafeSearchNoRestrictionsMode (0) = Non configurare le restrizioni di ricerca in Bing

* BingSafeSearchModerateMode (1) = Configura restrizioni di ricerca moderate in Bing

* BingSafeSearchStrictMode (2) = Configura restrizioni di ricerca strict in Bing

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ForceBingSafeSearch
  - Nome GP: Applica Ricerca sicura Bing
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ForceBingSafeSearch
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ForceBingSafeSearch
  - Valore di esempio:
``` xml
<integer>0</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ForceCertificatePromptsOnMultipleMatches
  #### Configura se Microsoft Edge deve selezionare automaticamente un certificato quando esistono più corrispondenze di certificati per un sito configurato con "AutoSelectCertificateForUrls"
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 81 o in seguito

  #### Descrizione
  Indica se agli utenti viene chiesto di selezionare un certificato se sono disponibili più certificati e un sito è configurato con [AutoSelectCertificateForUrls](#autoselectcertificateforurls). Se non configuri [AutoSelectCertificateForUrls](#autoselectcertificateforurls) per un sito, all'utente verrà sempre chiesto di selezionare un certificato.

Se imposti questi criteri su True, Microsoft Edge richiederà all'utente di selezionare un certificato per i siti nell'elenco definito in [AutoSelectCertificateForUrls](#autoselectcertificateforurls) se e solo se sono presenti più certificati.

Se imposti questi criteri su False o non li configuri, Microsoft Edge selezionerà automaticamente un certificato anche se sono presenti più corrispondenze per un certificato. All'utente non verrà richiesto di selezionare un certificato per i siti nell'elenco definito in [AutoSelectCertificateForUrls](#autoselectcertificateforurls).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ForceCertificatePromptsOnMultipleMatches
  - Nome GP: Configura se Microsoft Edge deve selezionare automaticamente un certificato quando esistono più corrispondenze di certificati per un sito configurato con "AutoSelectCertificateForUrls"
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ForceCertificatePromptsOnMultipleMatches
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ForceCertificatePromptsOnMultipleMatches
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ForceEphemeralProfiles
  #### Abilita l'uso di profili temporanei
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Controlla se i profili utente vengono passati alla modalità temporanea. Un profilo temporaneo viene creato quando una sessione inizia, viene eliminato quando la sessione finisce e viene associato al profilo originale dell'utente.

Se abiliti questo criterio, i profili vengono eseguiti in modalità temporanea. Ciò consente agli utenti di lavorare con i propri dispositivi senza salvare i dati delle esplorazioni nei dispositivi stessi. Se abiliti questo criterio per il sistema operativo (ad esempio utilizzando Oggetto Criteri di gruppo in Windows) viene applicato a tutti i profili nel sistema.

Se disabiliti questo criterio o non lo configuri, gli utenti usano i profili normali quando accedono con il browser.

In modalità temporanea, i dati dei profili vengono salvati sul disco solo per la durata della sessione dell’utente. Le funzionalità come la cronologia del browser, le estensioni e i relativi dati, i dati Web come i cookie e i database Web non vengono salvati quando si chiude il browser. L’utente può comunque scaricare manualmente i dati su disco, salvare le pagine o stamparle. Se l'utente ha abilitato la sincronizzazione, tutti i dati vengono conservati nei relativi account di sincronizzazione come per i profili normali. Gli utenti possono inoltre usare la funzionalità InPrivate Browsing in modalità temporanea a meno che non venga esplicitamente disabilitata.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ForceEphemeralProfiles
  - Nome GP: Abilita l'uso di profili temporanei
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ForceEphemeralProfiles
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ForceEphemeralProfiles
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ForceGoogleSafeSearch
  #### Applica Google SafeSearch
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Forza l'esecuzione delle query nella ricerca Web di Google con SafeSearch impostata come attiva e impedisce agli utenti di modificare questa impostazione.

Se abiliti questi criteri, SafeSearch è sempre attiva nella ricerca di Google.

Se disabiliti o non configuri questi criteri, SafeSearch non è attiva nella ricerca di Google.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ForceGoogleSafeSearch
  - Nome GP: Applica Google SafeSearch
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ForceGoogleSafeSearch
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ForceGoogleSafeSearch
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ForceLegacyDefaultReferrerPolicy
  #### Utilizza un criterio referrer predefinito di no-referrer-when-downgrade (deprecato)
  >DEPRECAtO: questi criteri sono deprecati. Sono attualmente supportati ma diventeranno obsoleti in una versione futura.
  
  #### Versioni supportate:
  - Su Windows e macOS dal 81 o in seguito

  #### Descrizione
  Questi criteri sono deprecati perché sono intesi solo come meccanismo a breve termine per dare alle aziende più tempo per aggiornare il loro contenuto Web se e quando si ritiene che sia compatibile con gli attuali criteri di riferimento predefiniti. Non funzionerà in Microsoft Edge dalla versione 86.

I criteri di riferimento predefiniti di Microsoft Edge vengono rafforzati dal valore corrente di no-referrer-when-downgrade al più sicuro strict-origin-when-cross-origin tramite un'implementazione graduale.

Prima dell'implementazione, i criteri dell'organizzazione non avranno alcun effetto. Dopo l'implementazione, quando questi criteri dell'organizzazione sono abilitati, i criteri di riferimento predefiniti di Microsoft Edge verranno impostati sul relativo valore precedente di no-referrer-when-downgrade.

Questi criteri dell'organizzazione sono disabilitati per impostazione predefinita.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ForceLegacyDefaultReferrerPolicy
  - Nome GP: Utilizza un criterio referrer predefinito di no-referrer-when-downgrade (deprecato)
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ForceLegacyDefaultReferrerPolicy
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ForceLegacyDefaultReferrerPolicy
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ForceNetworkInProcess
  #### Forza codice di rete da eseguire nel processo del browser (obsoleto)
  
  >OBSOLETO: questo criterio è obsoleto e non funziona nelle versioni di Microsoft Edge successive alla versione 83.
  #### Versioni supportate:
  - Su Windows dal 78, fino al 83

  #### Descrizione
  Questi criteri non funzionano perché erano intesi solo come meccanismo a breve termine per dare alle aziende più tempo per eseguire la migrazione a un software di terze parti che non dipende dall'esecuzione dell'hook delle API di rete. I server proxy sono consigliati su LSP e patch API Win32.

Questi criteri forzano l'esecuzione del codice di rete nel processo del browser.

Questi criteri sono disabilitati per impostazione predefinita. Se abilitati, gli utenti sono esposti a problemi di sicurezza quando il processo di rete è in modalità sandbox.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ForceNetworkInProcess
  - Nome GP: Forza codice di rete da eseguire nel processo del browser (obsoleto)
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ForceNetworkInProcess
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ForceSync
  #### Forza la sincronizzazione dei dati del browser e non mostrare la richiesta di consenso alla sincronizzazione
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Forza la sincronizzazione dei dati in Microsoft Edge. Questo criterio impedisce inoltre all'utente di disattivare la sincronizzazione.

Se non configuri questo criterio, gli utenti potranno attivare o disattivare la sincronizzazione. Se abiliti questo criterio, gli utenti non saranno in grado di disattivare la sincronizzazione.

Affinché questo criterio funzioni come previsto,
[BrowserSignin](#browsersignin) il criterio non deve essere configurato o deve essere impostato su abilitato. Se [ForceSync](#forcesync) è impostato su disabilitato, [BrowserSignin](#browsersignin) non avrà effetto.

[SyncDisabled](#syncdisabled) non deve essere configurato o deve essere impostato su False. Se è impostato su True, [ForceSync](#forcesync) non avrà effetto.

0 = Non avviare automaticamente la sincronizzazione e mostrare il consenso alla sincronizzazione (impostazione predefinita)
1 = Forza l'attivazione della sincronizzazione per il profilo utente degradato di Azure AD/Azure AD e non mostrare la richiesta di consenso alla sincronizzazione

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ForceSync
  - Nome GP: Forza la sincronizzazione dei dati del browser e non mostrare la richiesta di consenso alla sincronizzazione
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ForceSync
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ForceSync
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ForceYouTubeRestrict
  #### Forza modalità con restrizioni YouTube minima
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Applica una modalità con restrizioni minima su YouTube e impedisce agli utenti di selezionare una modalità con meno restrizioni.

Imposta su 'Strict' per applicare la modalità Strict con restrizioni su YouTube.

Imposta su 'Moderate' per imporre all'utente di utilizzare solo la modalità Media con restrizioni e la modalità Strict con restrizioni su YouTube. Non è possibile disabilitare la modalità con restrizioni.

 Imposta su 'Off' o non configurare questi criteri per non applicare la modalità con restrizioni su YouTube. Criteri esterni, ad esempio i criteri di YouTube potrebbero imporre comunque la modalità con restrizioni.

Mappatura opzioni criteri:

* Off (0) = Non applicare la modalità con restrizioni su YouTube

* Moderate (1) = Applica almeno una modalità di restrizione media su YouTube

* Strict (2) = Attiva la modalità Strict con restrizioni per YouTube

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ForceYouTubeRestrict
  - Nome GP: Forza modalità con restrizioni YouTube minima
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ForceYouTubeRestrict
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ForceYouTubeRestrict
  - Valore di esempio:
``` xml
<integer>0</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### FullscreenAllowed
  #### Consenti la modalità a schermo intero
  
  
  #### Versioni supportate:
  - Su Windows dal 77 o successiva

  #### Descrizione
  Imposta la disponibilità della modalità a schermo intero: l'intera interfaccia utente di Microsoft Edge è nascosta e solo il contenuto Web è visibile.

Se abiliti o non configuri questi criteri, l'utente, le app e le estensioni con le autorizzazioni appropriate possono accedere alla modalità a schermo intero.

Se disabiliti questi criteri, gli utenti, le app e le estensioni non possono accedere alla modalità a schermo intero.

L'apertura di Microsoft Edge in modalità tutto schermo tramite la riga di comando non è disponibile quando la modalità a schermo intero è disabilitata.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: FullscreenAllowed
  - Nome GP: Consenti la modalità a schermo intero
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: FullscreenAllowed
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### GloballyScopeHTTPAuthCacheEnabled
  #### Abilita cache di autenticazione HTTP con ambito globale
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 81 o in seguito

  #### Descrizione
  Questo criterio configura una singola cache per profilo globale con credenziali di autenticazione del server HTTP.

Se disabiliti o non imposti questi criteri, il browser utilizzerà il comportamento predefinito dell'autenticazione tra siti che, a partire dalla versione 80, sarà l'ambito delle credenziali di autenticazione del server HTTP per il sito principale. Se due siti utilizzano risorse appartenenti allo stesso dominio di autenticazione, sarà necessario fornire le credenziali indipendentemente nel contesto di entrambi i siti. Le credenziali proxy memorizzate nella cache verranno riutilizzate tra siti.

Se abiliti questa impostazione, le credenziali di autenticazione HTTP dei criteri immesse nel contesto di un sito verranno utilizzate automaticamente nel contesto di un altro sito.

L'abilitazione di questi criteri lascia i siti esposti ad alcuni tipi di attacchi tra siti e consente di registrare gli utenti nei siti anche senza cookie aggiungendo voci alla cache di autenticazione HTTP utilizzando le credenziali incorporate negli URL.

Questi criteri sono destinati a fornire alle aziende in base al comportamento legacy la possibilità di aggiornare le procedure di accesso e verranno rimossi in futuro.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: GloballyScopeHTTPAuthCacheEnabled
  - Nome GP: Abilita cache di autenticazione HTTP con ambito globale
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: GloballyScopeHTTPAuthCacheEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: GloballyScopeHTTPAuthCacheEnabled
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### GoToIntranetSiteForSingleWordEntryInAddressBar
  #### Forza l'esplorazione diretta del sito Intranet anziché cercare le singole parole immesse nella barra degli indirizzi
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 78 o in seguito

  #### Descrizione
  Se abiliti questi criteri, il primo risultato del suggerimento automatico dell'elenco dei suggerimenti della barra degli indirizzi passa al sito Intranet se il testo immesso nella barra degli indirizzi è una singola parola senza punteggiatura.

La navigazione predefinita quando si digita una singola parola senza punteggiatura conduce a un sito Intranet corrispondente al testo inserito.

Se abiliti questi criteri, il secondo suggerimento automatico dell'elenco dei suggerimenti della barra degli indirizzi eseguirà una ricerca Web del termine esattamente come è stato immesso, a condizione che il testo sia una singola parola senza punteggiatura. Verrà utilizzato il provider di ricerca predefinito a meno che non siano abilitati anche criteri per impedire la ricerca Web.

Gli effetti dell'abilitazione di questi criteri sono due:

non verrà più eseguita la navigazione ai siti in risposta alle query a parola singola che normalmente si risolvono in un elemento della cronologia. Al contrario, il browser tenterà di accedere a siti interni che potrebbero non esistere nella rete Intranet di un'organizzazione. Viene restituito un errore 404.

I termini di ricerca popolari a parola singola richiedono la selezione manuale dei suggerimenti di ricerca per condurre correttamente una ricerca.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Nome GP: Forza l'esplorazione diretta del sito Intranet anziché cercare le singole parole immesse nella barra degli indirizzi
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### HSTSPolicyBypassList
  #### Configura l'elenco dei nomi che ignoreranno il controllo dei criteri HSTS
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 79 o in seguito

  #### Descrizione
  I nomi host specificati in questo elenco saranno esenti dal controllo dei criteri HSTS che potrebbe potenzialmente aggiornare le richieste da "http://" a "https://". In questo criterio sono consentiti solo nomi host con etichetta singola. I nomi host devono essere in forma canonica. Qualsiasi IDN deve essere convertito nel formato A-Label e tutte le lettere ASCII devono essere minuscole. Questo criterio si applica solo a specifici nomi host specificati e non si applica ai sottodomini dei nomi nell'elenco.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: HSTSPolicyBypassList
  - Nome GP: Configura l'elenco dei nomi che ignoreranno il controllo dei criteri HSTS
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList\1 = "meet"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: HSTSPolicyBypassList
  - Valore di esempio:
``` xml
<array>
  <string>meet</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### HardwareAccelerationModeEnabled
  #### Utilizza l'accelerazione hardware se disponibile
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica l'utilizzo dell'accelerazione hardware, se disponibile. Se abiliti o non configuri questo criteri, l'accelerazione hardware è abilitata a meno che una funzionalità GPU non sia bloccata in modo esplicito.

Se disabiliti questi criteri, l'accelerazione hardware è disabilitata.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: HardwareAccelerationModeEnabled
  - Nome GP: Utilizza l'accelerazione hardware se disponibile
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: HardwareAccelerationModeEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: HardwareAccelerationModeEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### HideFirstRunExperience
  #### Nascondi la First Run Experience e la schermata iniziale
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 80 o in seguito

  #### Descrizione
  Se abiliti questi criteri, l'esperienza di prima esecuzione e la schermata iniziale non verranno mostrati agli utenti quando eseguono Microsoft Edge per la prima volta.

Per le opzioni di configurazione visualizzate nella prima esperienza di avvio, il browser utilizzerà le impostazioni predefinite seguenti:

-Nella pagina nuova scheda il tipo di feed verrà impostato su MSN Notizie e il layout su Di ispirazione.

-L'utente continuerà a essere connesso automaticamente a Microsoft Edge se l'account di Windows è di tipo AAD o MSA.

La sincronizzazione non verrà abilitata per impostazione predefinita e gli utenti saranno in grado di attivare la sincronizzazione dalle impostazioni di sincronizzazione.

Se disabiliti o non configuri questi criteri, verrà visualizzata la prima esperienza e la schermata iniziale.

Nota: le opzioni di configurazione specifiche visualizzate all'utente nella prima esperienza di avvio possono essere gestite anche utilizzando altri criteri specifici. È possibile utilizzare il criterio HideFirstRunExperience in combinazione con questi criteri per configurare un'esperienza browser specifica nei dispositivi gestiti. Alcuni di questi altri criteri sono:

-[AutoImportAtFirstRun](#autoimportatfirstrun)

-[NewTabPageLocation](#newtabpagelocation)

-[NewTabPageSetFeedType](#newtabpagesetfeedtype)

-[SyncDisabled](#syncdisabled)

-[BrowserSignin](#browsersignin)

-[NonRemovableProfileEnabled](#nonremovableprofileenabled)

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: HideFirstRunExperience
  - Nome GP: Nascondi la First Run Experience e la schermata iniziale
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: HideFirstRunExperience
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: HideFirstRunExperience
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ImportAutofillFormData
  #### Consenti l'importazione dei dati del modulo di riempimento automatico
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente agli utenti di importare i dati del modulo di riempimento automatico da un altro browser in Microsoft Edge.

Se abiliti questi criteri, l'opzione per l'importazione manuale dei dati di riempimento automatico è selezionata automaticamente.

Se disabiliti questi criteri, i dati del modulo di riempimento automatico non vengono importati alla prima esecuzione e gli utenti non possono importarli manualmente.

Se non configuri questi criteri, i dati di riempimento automatico vengono importati alla prima esecuzione e gli utenti possono scegliere se importare manualmente questi dati durante le sessioni di esplorazione successive.

Puoi impostare questi criteri come suggerimento. Ciò significa che Microsoft Edge importa i dati di riempimento automatico alla prima esecuzione, ma gli utenti possono selezionare o deselezionare l'opzione **Dati riempimento automatico** durante l'importazione manuale.

**Nota**: questi criteri gestiscono attualmente l'importazione dai browser Google Chrome (in Windows 7, 8 e 10 e macOS) e Mozilla Firefox (in Windows 7, 8 e 10 e macOS).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ImportAutofillFormData
  - Nome GP: Consenti l'importazione dei dati del modulo di riempimento automatico
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: ImportAutofillFormData
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ImportAutofillFormData
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ImportBrowserSettings
  #### Consenti l'importazione delle impostazioni del browser
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 78 o in seguito

  #### Descrizione
  Consente agli utenti di importare le impostazioni del browser da un altro browser in Microsoft Edge.

Se abiliti questi criteri, la casella di controllo **impostazioni browser** viene selezionata automaticamente nella finestra di dialogo **Importa dati del browser**.

Se disabiliti questi criteri, le impostazioni del browser non vengono importate alla prima operazione e gli utenti non possono importarle manualmente.

Se non configuri questi criteri, le impostazioni del browser vengono importate alla prima operazione e gli utenti possono scegliere se importarle manualmente durante le sessioni di esplorazione successive.

Puoi inoltre impostare questi criteri come suggerimento. Questo significa che Microsoft Edge importa le impostazioni alla prima operazione, ma gli utenti possono selezionare o deselezionare l'opzione **impostazioni del browser** durante l'importazione manuale.

**Nota**: questi criteri gestiscono attualmente l'importazione di Google Chrome (in Windows 7, 8 e 10 e su macOS).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ImportBrowserSettings
  - Nome GP: Consenti l'importazione delle impostazioni del browser
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: ImportBrowserSettings
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ImportBrowserSettings
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ImportCookies
  #### Consenti l'importazione dei cookie
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 81 o in seguito

  #### Descrizione
  Consente agli utenti di importare i cookie da un altro browser in Microsoft Edge.

Se disabiliti questi criteri, i cookie non vengono importati alla prima esecuzione.

Se non configuri questi criteri, i cookie vengono importati alla prima esecuzione.

Puoi inoltre impostare questi criteri come suggerimento. Questo significa che Microsoft Edge importa i cookie alla prima esecuzione.

**Nota**: questi criteri gestiscono attualmente l'importazione da Google Chrome (in Windows 7, 8 e 10 e su macOS).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ImportCookies
  - Nome GP: Consenti l'importazione dei cookie
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: ImportCookies
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ImportCookies
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ImportExtensions
  #### Consenti l'importazione delle estensioni
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 81 o in seguito

  #### Descrizione
  Consenti agli utenti di importare le estensioni da un altro browser in Microsoft Edge.

Se abiliti questi criteri, la casella di controllo **Estensioni** è selezionata automaticamente nella finestra di dialogo **Importa dati del browser**.

Se disabiliti questi criteri, le estensioni non vengono importate alla prima esecuzione e gli utenti non possono importarle manualmente.

Se non configuri questi criteri, le estensioni vengono importate alla prima esecuzione e gli utenti possono scegliere se importarle manualmente durante le sessioni di esplorazione successive.

Puoi inoltre impostare questi criteri come suggerimento. Questo significa che Microsoft Edge importa le estensioni alla prima esecuzione, ma gli utenti possono selezionare o deselezionare l'opzione **Preferiti** durante l'importazione manuale.

**Nota**: questi criteri gestiscono attualmente l'importazione di Google Chrome (in Windows 7, 8 e 10 e su macOS).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ImportExtensions
  - Nome GP: Consenti l'importazione delle estensioni
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: ImportExtensions
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ImportExtensions
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ImportFavorites
  #### Consenti l'importazione dei preferiti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente agli utenti di importare i preferiti da un altro browser in Microsoft Edge.

Se abiliti questi criteri, la casella di controllo **Preferiti** è selezionata automaticamente nella finestra di dialogo **Importa dati del browser**.

Se disabiliti questi criteri, i preferiti non vengono importati alla prima esecuzione e gli utenti non possono importarli manualmente.

Se non configuri questi criteri, i preferiti vengono importati alla prima esecuzione e gli utenti possono scegliere se importarli manualmente durante le sessioni di esplorazione successive.

Puoi inoltre impostare questi criteri come suggerimento. Questo significa che Microsoft Edge importa i preferiti alla prima esecuzione, ma gli utenti possono selezionare o deselezionare l'opzione **preferiti** durante l'importazione manuale.

**Nota**: questi criteri gestiscono attualmente l'importazione dai browser Internet Explorer (in Windows 7, 8 e 10), Google Chrome (in Windows 7, 8 e 10 e macOS), Mozilla Firefox (in Windows 7, 8 e 10 e macOS) e Apple Safari (in macOS).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ImportFavorites
  - Nome GP: Consenti l'importazione dei preferiti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: ImportFavorites
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ImportFavorites
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ImportHistory
  #### Consenti l'importazione della cronologia esplorazioni
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente agli utenti di importare la cronologia esplorazioni da un altro browser in Microsoft Edge.

Se abiliti questi criteri, la casella di controllo **Cronologia esplorazioni** viene selezionata automaticamente nella finestra di dialogo **Importa dati del browser**.

Se disabiliti questi criteri, i dati relativi alla cronologia esplorazioni non vengono importati alla prima esecuzione e gli utenti non possono importare manualmente questi dati.

Se non configuri questi criteri, i dati relativi alla cronologia esplorazioni vengono importati alla prima esecuzione e gli utenti possono scegliere se importarli manualmente durante le sessioni di esplorazione successive.

Puoi inoltre impostare questi criteri come suggerimento. Questo significa che Microsoft Edge importa la cronologia esplorazioni alla prima esecuzione, ma gli utenti possono selezionare o deselezionare l'opzione **cronologia** durante l'importazione manuale.

**Nota**: questi criteri gestiscono attualmente l'importazione dai browser Internet Explorer (in Windows 7, 8 e 10), Google Chrome (in Windows 7, 8 e 10 e macOS), Mozilla Firefox (in Windows 7, 8 e 10 e macOS) e Apple Safari (macOS).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ImportHistory
  - Nome GP: Consenti l'importazione della cronologia esplorazioni
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: ImportHistory
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ImportHistory
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ImportHomepage
  #### Consenti l'importazione delle impostazioni della home page
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente agli utenti di importare l'impostazione della home page da un altro browser in Microsoft Edge.

Se abiliti questi criteri, l'opzione per importare manualmente l'impostazione della home page è selezionata automaticamente.

Se disabiliti questi criteri, l'impostazione della home page non viene importata alla prima esecuzione e gli utenti non possono importarla manualmente.

Se non configuri questi criteri, l'impostazione della home page viene importata alla prima esecuzione e gli utenti possono scegliere se importare manualmente questi dati durante le sessioni di esplorazione successive.

Puoi impostare questi criteri come suggerimento. Questo significa che Microsoft Edge importa l'impostazione della home page alla prima esecuzione, ma gli utenti possono selezionare o deselezionare l'opzione **home page** durante l'importazione manuale.

**Nota**: questi criteri gestiscono attualmente l'importazione da Internet Explorer (in Windows 7, 8 e 10).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ImportHomepage
  - Nome GP: Consenti l'importazione delle impostazioni della home page
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ImportHomepage
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ImportHomepage
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ImportOpenTabs
  #### Consenti l'importazione delle schede aperte
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 79 o in seguito

  #### Descrizione
  Consenti agli utenti di importare le schede aperte e bloccate da un altro browser in Microsoft Edge.

Se abiliti questi criteri, la casella di controllo **Schede aperte** è selezionata automaticamente nella finestra di dialogo **Importa dati del browser**.

Se disabiliti questi criteri, le schede aperte non vengono importate alla prima esecuzione e gli utenti non possono importarle manualmente.

Se non configuri questi criteri, le schede aperte vengono importate alla prima esecuzione e gli utenti possono scegliere se importarle manualmente durante le sessioni di esplorazione successive.

Puoi inoltre impostare questi criteri come suggerimento. Questo significa che Microsoft Edge importa le schede aperte alla prima esecuzione, ma gli utenti possono selezionare o deselezionare l'opzione **Schede aperte** durante l'importazione manuale.

**Nota**: questi criteri gestiscono attualmente l'importazione di Google Chrome (in Windows 7, 8 e 10 e su macOS).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ImportOpenTabs
  - Nome GP: Consenti l'importazione delle schede aperte
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: ImportOpenTabs
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ImportOpenTabs
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ImportPaymentInfo
  #### Consenti importazione delle info di pagamento
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente agli utenti di importare le info di pagamento da un altro browser in Microsoft Edge.

Se abiliti questi criteri, la casella di controllo **Info di pagamento** è selezionata automaticamente nella finestra di dialogo **Importa dati del browser**.

Se disabiliti questi criteri, le info di pagamento non vengono importate alla prima esecuzione e gli utenti non possono importarle manualmente.

Se non configuri questi criteri, le info di pagamento vengono importate alla prima esecuzione e gli utenti possono scegliere se importare manualmente questi dati durante le sessioni di esplorazione successive.

Puoi anche impostare questi criteri come suggerimento. Ciò significa che Microsoft Edge importa le info di pagamento alla prima esecuzione, ma gli utenti possono selezionare o deselezionare l'opzione **Info di pagamento** durante l'importazione manuale.

**Nota**: questi criteri gestiscono attualmente l'importazione da Google Chrome (in Windows 7, 8 e 10 e macOS).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ImportPaymentInfo
  - Nome GP: Consenti importazione delle info di pagamento
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: ImportPaymentInfo
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ImportPaymentInfo
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ImportSavedPasswords
  #### Consenti l'importazione delle password salvate
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente agli utenti di importare le password salvate da un altro browser in Microsoft Edge.

Se abiliti questi criteri, l'opzione per importare manualmente le password salvate è selezionata automaticamente.

Se disabiliti questi criteri, le password salvate non vengono importate alla prima esecuzione e gli utenti non possono importarle manualmente.

Se non configuri questi criteri, le password vengono importate alla prima esecuzione e gli utenti possono scegliere se importarle manualmente durante le sessioni di esplorazione successive.

Puoi impostare questi criteri come suggerimento. Questo significa che Microsoft Edge importa le password alla prima esecuzione, ma gli utenti possono selezionare o deselezionare l'opzione **password** durante l'importazione manuale.

**Nota**: questi criteri gestiscono attualmente l'importazione dai browser Internet Explorer (in Windows 7, 8 e 10), Google Chrome (in Windows 7, 8 e 10 e macOS) e Mozilla Firefox (in Windows 7, 8 e 10 e macOS).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ImportSavedPasswords
  - Nome GP: Consenti l'importazione delle password salvate
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: ImportSavedPasswords
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ImportSavedPasswords
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ImportSearchEngine
  #### Consenti l'importazione delle impostazioni del motore di ricerca
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente agli utenti di importare le impostazioni del motore di ricerca da un altro browser in Microsoft Edge.

Se abiliti questi criteri, l'opzione per l'importazione delle impostazioni del motore di ricerca viene selezionata automaticamente.

Se disabiliti questi criteri, le impostazioni del motore di ricerca non vengono importate alla prima esecuzione e gli utenti non possono importarle manualmente.

Se non configuri questi criteri, le impostazioni del motore di ricerca vengono importate alla prima esecuzione e gli utenti possono scegliere se importare manualmente questi dati durante le sessioni di esplorazione successive.

Puoi impostare questi criteri come suggerimento. Questo significa che Microsoft Edge importa le impostazioni del motore di ricerca alla prima esecuzione, ma gli utenti possono selezionare o deselezionare l'opzione **motore di ricerca** durante l'importazione manuale.

**Nota**: questi criteri gestiscono attualmente l'importazione da Internet Explorer (in Windows 7, 8 e 10).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ImportSearchEngine
  - Nome GP: Consenti l'importazione delle impostazioni del motore di ricerca
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: ImportSearchEngine
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ImportSearchEngine
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ImportShortcuts
  #### Consenti l'importazione dei collegamenti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 81 o in seguito

  #### Descrizione
  Consenti agli utenti di importare i collegamenti da un altro browser in Microsoft Edge.

Se disabiliti questi criteri, i collegamenti non vengono importati alla prima esecuzione.

Se non configuri questi criteri, i collegamenti vengono importati alla prima esecuzione.

Puoi inoltre impostare questi criteri come suggerimento. Questo significa che Microsoft Edge importa i collegamenti alla prima esecuzione.

**Nota**: questi criteri gestiscono attualmente l'importazione da Google Chrome (in Windows 7, 8 e 10 e su macOS).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ImportShortcuts
  - Nome GP: Consenti l'importazione dei collegamenti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: ImportShortcuts
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ImportShortcuts
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### InPrivateModeAvailability
  #### Configura la disponibilità della modalità InPrivate
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica se l'utente può aprire le pagine in modalità InPrivate in Microsoft Edge.

Se non configuri questi criteri o li imposti su "Enabled", gli utenti possono aprire le pagine in modalità InPrivate.

Imposta questi criteri su "Disabled" per arrestare l'utilizzo della modalità InPrivate da parte degli utenti.

Imposta questi criteri su "Forced" per utilizzare sempre la modalità InPrivate.

Mappatura opzioni criteri:

* Enabled (0) = Modalità InPrivate disponibile

* Disabled (1) = Modalità InPrivate disabilitata

* Forced (2) = Modalità InPrivate forzata

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: InPrivateModeAvailability
  - Nome GP: Configura la disponibilità della modalità InPrivate
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: InPrivateModeAvailability
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: InPrivateModeAvailability
  - Valore di esempio:
``` xml
<integer>1</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### InsecureFormsWarningsEnabled
  #### Abilita avvisi per moduli non sicuri
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Questo criterio controlla la gestione dei moduli non sicuri (moduli inviati tramite HTTP) incorporati in siti protetti (HTTPS) nel browser.
Se abiliti questo criterio o non lo imposti, verrà visualizzato un avviso a pagina intera quando viene inviato un modulo non sicuro. Inoltre, verrà visualizzato un avviso accanto ai campi del modulo quando sono attivi e la compilazione automatica verrà disabilitata per tali moduli.
Se disabiliti questo criterio, gli avvisi non verranno visualizzati per i moduli non protetti e la compilazione automatica funzionerà normalmente.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: InsecureFormsWarningsEnabled
  - Nome GP: Abilita avvisi per moduli non sicuri
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: InsecureFormsWarningsEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: InsecureFormsWarningsEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### IntensiveWakeUpThrottlingEnabled
  #### Controlla la funzionalità IntensiveWakeUpThrottling
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 85 o in seguito

  #### Descrizione
  Se abilitata, la funzionalità IntensiveWakeUpThrottling fa sì che i timer Javascript nelle schede in background vengano rallentati e coalizzati in modo aggressivo, in esecuzione non più di una volta al minuto dopo che una pagina è stata messa in background per 5 minuti o più.

Questa è una funzionalità conforme agli standard Web, ma potrebbe interrompere la funzionalità su alcuni siti Web causando un ritardo di alcune azioni di un minuto. Tuttavia, comporta un notevole risparmio di CPU e batteria quando abilitato. Consulta https://bit.ly/30b1XR4 per ulteriori dettagli.

Se attivi questo criterio, la funzionalità verrà abilitata forzatamente e gli utenti non saranno in grado di ignorare questa impostazione.
Se disabiliti questo criterio, la funzionalità verrà disabilitata forzatamente e gli utenti non saranno in grado di ignorare questa impostazione.
Se non configuri questo criterio, la funzionalità sarà controllata dalla propria logica interna. Gli utenti possono configurare manualmente questa impostazione.

Tieni presente che il criterio viene applicato per processo di rendering, con il valore più recente dell'impostazione del criterio in vigore all'avvio di un processo di rendering. È necessario un riavvio completo per garantire che tutte le schede caricate ricevano un'impostazione dei criteri coerente. Non è importante che i processi vengano eseguiti con valori diversi da questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: IntensiveWakeUpThrottlingEnabled
  - Nome GP: Controlla la funzionalità IntensiveWakeUpThrottling
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: IntensiveWakeUpThrottlingEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: IntensiveWakeUpThrottlingEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### InternetExplorerIntegrationEnhancedHangDetection
  #### Configura il rilevamento avanzato di blocchi per la modalità di Internet Explorer
  
  
  #### Versioni supportate:
  - Su Windows dal 84 o successiva

  #### Descrizione
  Il rilevamento dei blocchi avanzato è un approccio più granulare al rilevamento di pagine Web bloccate in modalità Internet Explorer rispetto a quello che utilizza Internet Explorer autonomo. Quando viene rilevata una pagina Web bloccata, il browser applica una mitigazione per impedire il blocco del resto del browser.

      Questa impostazione ti consente di configurare l'uso del rilevamento avanzato del blocco in caso di problemi incompatibili con uno dei tuoi siti Web. Ti consigliamo di disabilitare questo criterio solo se visualizzi notifiche come "(sito Web) non risponde" in modalità Internet Explorer ma non in Internet Explorer autonomo.

      Questa impostazione funziona in combinazione con:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) è impostato su "modalità Internet Explorer"
      e il criterio
[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) in cui l'elenco ha almeno una voce.

      Se imposti questo criterio su “Enabled” o non lo configuri, i siti Web in esecuzione in modalità Internet Explorer utilizzeranno il rilevamento avanzato dei blocchi.

      Se imposti questo criterio su "Disabled", il rilevamento avanzato dei blocchi è disabilitato e gli utenti otterranno il comportamento di base del rilevamento dei blocchi di Internet Explorer.

Per altre informazioni sulla modalità Internet Explorer, vai all'indirizzo [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Mappatura opzioni criteri:

* Disabled (0) = Rilevamento avanzato blocchi disabilitato

* Enabled (1) = Rilevamento avanzato blocchi abilitato

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: InternetExplorerIntegrationEnhancedHangDetection
  - Nome GP: Configura il rilevamento avanzato di blocchi per la modalità di Internet Explorer
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: InternetExplorerIntegrationEnhancedHangDetection
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### InternetExplorerIntegrationLevel
  #### Configura l'integrazione di Internet Explorer
  
  
  #### Versioni supportate:
  - Su Windows dal 77 o successiva

  #### Descrizione
  Per informazioni sulla configurazione dell'esperienza ottimale per la modalità Internet Explorer, vedi [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Mappatura opzioni criteri:

* None (0) = Nessuno

* IEMode (1) = Modalità Internet Explorer

* NeedIE (2) = Internet Explorer 11

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: InternetExplorerIntegrationLevel
  - Nome GP: Configura l'integrazione di Internet Explorer
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: InternetExplorerIntegrationLevel
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### InternetExplorerIntegrationSiteList
  #### Configura l'elenco dei siti in modalità Enterprise
  
  
  #### Versioni supportate:
  - Su Windows dal 78 o successiva

  #### Descrizione
  Per informazioni sulla configurazione dell'esperienza ottimale per la modalità Internet Explorer, vedi [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: InternetExplorerIntegrationSiteList
  - Nome GP: Configura l'elenco dei siti in modalità Enterprise
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: InternetExplorerIntegrationSiteList
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"https://internal.contoso.com/sitelist.xml"
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### InternetExplorerIntegrationSiteRedirect
  #### Specifica il comportamento della modalità di spostamento dei siti non configurati "nella pagina" quando avviati dalle pagine in modalità Internet Explorer
  
  
  #### Versioni supportate:
  - Su Windows dal 81 o successiva

  #### Descrizione
  Lo spostamento "nella pagina" viene avviato da un collegamento, uno script o un modulo nella pagina corrente. Può anche essere un reindirizzamento lato server di un precedente tentativo di spostamento nella pagina. Al contrario, un utente può avviare uno spostamento che non è "nella pagina" indipendentemente dalla pagina corrente in diversi modi utilizzando i controlli del browser. Ad esempio, utilizzando la barra degli indirizzi, il pulsante Indietro o un collegamento preferito.

 Questa impostazione consente di specificare se gli spostamenti dalle pagine caricate in modalità Internet Explorer in siti non configurati (non configurati nell'elenco dei siti in modalità Enterprise) tornano su Microsoft Edge o rimangono in modalità Internet Explorer.

 Questa impostazione funziona in combinazione con:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) impostata su "modalità Internet Explorer"
 e
[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) in cui l'elenco contiene almeno una voce.

 Se disabiliti o non configuri questi criteri, in tale modalità verranno aperti solo i siti configurati per l'apertura in modalità Internet Explorer. Qualsiasi sito non configurato per l'apertura in modalità Internet Explorer verrà reindirizzato a Microsoft Edge.

Con Default si apriranno solo i siti configurati per l'apertura in modalità Internet Explorer. Qualsiasi sito non configurato per l'apertura in modalità Internet Explorer verrà reindirizzato a Microsoft Edge.

 Con Mantieni solo gli spostamenti automatici in modalità Internet Explorer, otterrai l'esperienza predefinita, ad eccezione del fatto che tutti gli spostamenti automatici (ad esempio, 302 reindirizzamenti) in siti non configurati verranno mantenuti in modalità Internet Explorer.

 Con Mantieni tutti gli spostamenti nella pagina in modalità Internet Explorer (scelta non consigliata), tutti gli spostamenti dalle pagine caricate in modalità IE in siti non configurati vengono mantenuti in modalità Internet Explorer.

   Per altre informazioni sulla modalità Internet Explorer, vedi [https://go.microsoft.com/fwlink/?linkid=2105106](https://go.microsoft.com/fwlink/?linkid=2105106)

Mappatura opzioni criteri:

* Default (0) = Predefinito

* AutomaticNavigationsOnly (1) = Mantieni solo gli spostamenti automatici in modalità Internet Explorer

* AllInPageNavigations (2) = Mantieni tutti gli spostamenti nella pagina in modalità Internet Explorer

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: InternetExplorerIntegrationSiteRedirect
  - Nome GP: Specifica il comportamento della modalità di spostamento dei siti non configurati "nella pagina" quando avviati dalle pagine in modalità Internet Explorer
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: InternetExplorerIntegrationSiteRedirect
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### InternetExplorerIntegrationTestingAllowed
  #### Consenti il test della modalità Internet Explorer
  
  
  #### Versioni supportate:
  - Su Windows dal 86 o successiva

  #### Descrizione
  Questo criterio è una sostituzione del criterio ie-mode-test flag. Consente agli utenti di aprire una scheda della modalità IE dall'opzione di menu dell'interfaccia utente.

Questa impostazione funziona insieme a:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) è impostato su "IEMode"
e il criterio
[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) in cui l'elenco contiene almeno una voce.

Se abiliti questo criterio, gli utenti possono aprire la scheda della modalità IE dall'opzione dell'interfaccia utente e navigare nel sito corrente in un sito in modalità IE.

Se disabiliti questo criterio, gli utenti non possono vedere direttamente l'opzione dell'interfaccia utente nel menu.

Se non configuri questo criterio, puoi impostare manualmente il contrassegno ie-mode-test.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: InternetExplorerIntegrationTestingAllowed
  - Nome GP: Consenti il test della modalità Internet Explorer
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: InternetExplorerIntegrationTestingAllowed
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### IsolateOrigins
  #### Abilita l'isolamento del sito per origini specifiche
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica l'esecuzione delle origini in isolamento nel proprio processo.
Questi criteri isolano inoltre le origini denominate da sottodomini, ad esempio specificando che https://contoso.com/ comporterà l'isolamento di https://foo.contoso.com/ come parte del sito https://contoso.com/.
Se i criteri sono abilitati, ciascuna delle origini denominate in un elenco delimitato da virgole verrà eseguita nel proprio processo.
Se disabiliti questi criteri, le funzionalità [IsolateOrigins](#isolateorigins) and [SitePerProcess](#siteperprocess) sono disabilitate. Gli utenti possono comunque abilitare i criteri [IsolateOrigins](#isolateorigins) manualmente, tramite i flag della riga di comando.
Se non configuri i criteri, l'utente può modificare questa impostazione.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: IsolateOrigins
  - Nome GP: Abilita l'isolamento del sito per origini specifiche
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: IsolateOrigins
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"https://contoso.com/,https://fabrikam.com/"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: IsolateOrigins
  - Valore di esempio:
``` xml
<string>https://contoso.com/,https://fabrikam.com/</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### LocalProvidersEnabled
  #### Consenti suggerimenti dei provider locali
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 83 o in seguito

  #### Descrizione
  Consente la visualizzazione dei suggerimenti dei provider di suggerimenti nel dispositivo (provider locali), ad esempio Preferiti e Cronologia esplorazioni, nell'elenco dei suggerimenti automatici e nella barra degli indirizzi di Microsoft Edge.

Se abiliti questo criterio, verranno usati i suggerimenti dei provider locali.

Se disabiliti questo criterio, i suggerimenti dei provider locali non verranno mai usati. I suggerimenti per la cronologia e i preferiti locali non verranno visualizzati.

Se non configuri questo criterio, i suggerimenti dei provider locali sono consentiti, ma l'utente può modificare questo comportamento con l'interruttore delle impostazioni.

Tieni presente che alcune funzionalità potrebbero non essere disponibili se è stato applicato un criterio per disabilitare questa funzionalità. Ad esempio, i suggerimenti di Cronologia esplorazioni non saranno disponibili se abiliti il criterio [SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled).

Per completare l'applicazione di questo criterio, è necessario riavviare il browser.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: LocalProvidersEnabled
  - Nome GP: Consenti suggerimenti dei provider locali
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: LocalProvidersEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: LocalProvidersEnabled
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ManagedFavorites
  #### Configura i preferiti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Configura un elenco di preferiti gestiti.

I criteri creano un elenco di preferiti. Ogni preferito contiene le chiavi "name" e "url" che contengono il nome e la destinazione del preferito. Puoi configurare una sottocartella definendo un preferito senza una chiave "url" ma con un ulteriore chiave "children" che contiene un elenco di preferiti come definito sopra (alcuni dei quali potrebbero essere di nuovo cartelle). Microsoft Edge modifica gli URL incompleti come se fossero stati inviati tramite la barra degli indirizzi, ad esempio "microsoft.com" diventa "https://microsoft.com/".

Questi preferiti sono inseriti in una cartella che non può essere modificata dall'utente (ma l'utente può scegliere di nasconderla dalla barra dei preferiti). Per impostazione predefinita, il nome della cartella è "Preferiti gestiti", ma è possibile modificarlo aggiungendo all'elenco dei preferiti un dizionario contenente la chiave "toplevel_name" con il nome della cartella desiderata come valore.

I preferiti gestiti non vengono sincronizzati con l'account utente e non possono essere modificati dalle estensioni.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Dizionario

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ManagedFavorites
  - Nome GP: Configura i preferiti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ManagedFavorites
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\ManagedFavorites = [
  {
    "toplevel_name": "My managed favorites folder"
  }, 
  {
    "name": "Microsoft", 
    "url": "microsoft.com"
  }, 
  {
    "name": "Bing", 
    "url": "bing.com"
  }, 
  {
    "children": [
      {
        "name": "Microsoft Edge Insiders", 
        "url": "www.microsoftedgeinsider.com"
      }, 
      {
        "name": "Microsoft Edge", 
        "url": "www.microsoft.com/windows/microsoft-edge"
      }
    ], 
    "name": "Microsoft Edge links"
  }
]
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ManagedFavorites
  - Valore di esempio:
``` xml
<key>ManagedFavorites</key>
<array>
  <dict>
    <key>toplevel_name</key>
    <string>My managed favorites folder</string>
  </dict>
  <dict>
    <key>name</key>
    <string>Microsoft</string>
    <key>url</key>
    <string>microsoft.com</string>
  </dict>
  <dict>
    <key>name</key>
    <string>Bing</string>
    <key>url</key>
    <string>bing.com</string>
  </dict>
  <dict>
    <key>children</key>
    <array>
      <dict>
        <key>name</key>
        <string>Microsoft Edge Insiders</string>
        <key>url</key>
        <string>www.microsoftedgeinsider.com</string>
      </dict>
      <dict>
        <key>name</key>
        <string>Microsoft Edge</string>
        <key>url</key>
        <string>www.microsoft.com/windows/microsoft-edge</string>
      </dict>
    </array>
    <key>name</key>
    <string>Microsoft Edge links</string>
  </dict>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ManagedSearchEngines
  #### Gestisci motori di ricerca
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente di configurare un elenco di un massimo di 10 motori di ricerca, uno dei quali deve essere contrassegnato come motore di ricerca predefinito.
Non è necessario specificare la codifica per un motore di ricerca. A partire da Microsoft Edge 80, i parametri suggest_url e image_search_url consigliati sono facoltativi. Il parametro facoltativo, image_search_post_params (consiste in coppie di nome/valore separate da virgole) è disponibile a partire da Microsoft Edge 80.

A partire da Microsoft Edge 83, puoi abilitare l'individuazione del motore di ricerca con il parametro opzionale allow_search_engine_discovery. Questo parametro deve essere la prima voce in elenco. Se allow_search_engine_discovery non è specificato, l'individuazione del motore di ricerca verrà disabilitata per impostazione predefinita. A partire da Microsoft Edge 84, puoi impostare questo criterio come consigliato per consentire l'individuazione da parte dei motori di ricerca. Non è necessario aggiungere il parametro facoltativo allow_search_engine_discovery.

Se abiliti questi criteri, gli utenti non possono aggiungere, rimuovere o modificare alcun motore di ricerca nell'elenco. Gli utenti possono impostare il motore di ricerca predefinito su qualsiasi motore di ricerca nell'elenco.

Se disabiliti o non configuri questi criteri, gli utenti possono modificare l'elenco dei motori di ricerca come desiderano.

Se i criteri [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) sono impostati, questi criteri (ManagedSearchEngines) vengono ignorati. L'utente deve riavviare il browser per completare l'applicazione dei criteri.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Dizionario

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ManagedSearchEngines
  - Nome GP: Gestisci motori di ricerca
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: ManagedSearchEngines
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\ManagedSearchEngines = [
  {
    "allow_search_engine_discovery": true
  }, 
  {
    "is_default": true, 
    "keyword": "example1.com", 
    "name": "Example1", 
    "search_url": "https://www.example1.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example1.com/qbox?query={searchTerms}"
  }, 
  {
    "image_search_post_params": "content={imageThumbnail},url={imageURL},sbisrc={SearchSource}", 
    "image_search_url": "https://www.example2.com/images/detail/search?iss=sbiupload", 
    "keyword": "example2.com", 
    "name": "Example2", 
    "search_url": "https://www.example2.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example2.com/qbox?query={searchTerms}"
  }, 
  {
    "encoding": "UTF-8", 
    "image_search_url": "https://www.example3.com/images/detail/search?iss=sbiupload", 
    "keyword": "example3.com", 
    "name": "Example3", 
    "search_url": "https://www.example3.com/search?q={searchTerms}", 
    "suggest_url": "https://www.example3.com/qbox?query={searchTerms}"
  }, 
  {
    "keyword": "example4.com", 
    "name": "Example4", 
    "search_url": "https://www.example4.com/search?q={searchTerms}"
  }
]
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ManagedSearchEngines
  - Valore di esempio:
``` xml
<key>ManagedSearchEngines</key>
<array>
  <dict>
    <key>allow_search_engine_discovery</key>
    <true/>
  </dict>
  <dict>
    <key>is_default</key>
    <true/>
    <key>keyword</key>
    <string>example1.com</string>
    <key>name</key>
    <string>Example1</string>
    <key>search_url</key>
    <string>https://www.example1.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example1.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>image_search_post_params</key>
    <string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
    <key>image_search_url</key>
    <string>https://www.example2.com/images/detail/search?iss=sbiupload</string>
    <key>keyword</key>
    <string>example2.com</string>
    <key>name</key>
    <string>Example2</string>
    <key>search_url</key>
    <string>https://www.example2.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example2.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>encoding</key>
    <string>UTF-8</string>
    <key>image_search_url</key>
    <string>https://www.example3.com/images/detail/search?iss=sbiupload</string>
    <key>keyword</key>
    <string>example3.com</string>
    <key>name</key>
    <string>Example3</string>
    <key>search_url</key>
    <string>https://www.example3.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example3.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>keyword</key>
    <string>example4.com</string>
    <key>name</key>
    <string>Example4</string>
    <key>search_url</key>
    <string>https://www.example4.com/search?q={searchTerms}</string>
  </dict>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### MaxConnectionsPerProxy
  #### Numero massimo di connessioni simultanee al server proxy
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica il numero massimo di connessioni simultanee al server proxy.

Alcuni server proxy non possono gestire un numero elevato di connessioni simultanee per client, ma puoi risolvere il problema impostando questi criteri su un valore inferiore.

Il valore di questi criteri deve essere inferiore a 100 e superiore a 6. Il valore predefinito è 32.

Alcune app sono note per l'utilizzo di un numero eccessivo di connessioni con GET bloccato: la riduzione del numero massimo di connessioni a meno di 32 potrebbe comportare il blocco del collegamento di rete del browser se un numero eccessivo di questo tipo di app Web vengono aperte.

Se non configuri questi criteri, viene utilizzato il valore predefinito (32).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: MaxConnectionsPerProxy
  - Nome GP: Numero massimo di connessioni simultanee al server proxy
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: MaxConnectionsPerProxy
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000020
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: MaxConnectionsPerProxy
  - Valore di esempio:
``` xml
<integer>32</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### MediaRouterCastAllowAllIPs
  #### Consenti a Google Cast di connettersi ai dispositivi Cast su tutti gli indirizzi IP
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Abilita questi criteri per consentire a Google Cast di connettersi a dispositivi Cast su tutti gli indirizzi IP, non solo gli indirizzi privati RFC1918/RFC4193.

Disabilita questi criteri per limitare Google Cast ai dispositivi Cast sugli indirizzi privati RFC1918/RFC4193.

Se non configuri questi criteri, Google Cast si connette ai dispositivi Cast solo sugli indirizzi privati RFC1918/RFC4193, a meno che non abiliti la funzionalità CastAllowAllIPs.

Se i criteri [EnableMediaRouter](#enablemediarouter) sono disabilitati, questi criteri non hanno effetto.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: MediaRouterCastAllowAllIPs
  - Nome GP: Consenti a Google Cast di connettersi ai dispositivi Cast su tutti gli indirizzi IP
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: MediaRouterCastAllowAllIPs
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: MediaRouterCastAllowAllIPs
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### MetricsReportingEnabled
  #### Abilita creazione di report sui dati di utilizzo e relativi all'arresto anomalo del sistema (deprecato)
  >DEPRECAtO: questi criteri sono deprecati. Sono attualmente supportati ma diventeranno obsoleti in una versione futura.
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Questo criterio è deprecato. È attualmente supportato ma diventerà obsoleto in Microsoft Edge 89. Questo criterio è sostituito dal nuovo criterio:  [DiagnosticData](#diagnosticdata)per Windows 7, Windows 8 e macOS. Questo criterio è sostituito da Consenti telemetria in Windows 10 (https://docs.microsoft.com/it-it/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

Questo criterio abilita l'invio di report sui dati relativi all'utilizzo e agli arresti anomali di Microsoft Edge a Microsoft.

Abilita questo criterio per inviare report sui dati relativi all'utilizzo e agli arresti anomali a Microsoft. Disabilita questo criterio per non inviare i dati a Microsoft. In entrambi i casi, gli utenti non possono modificare o eseguire l'override dell'impostazione.

In Windows 10, se non configuri questo criterio Microsoft Edge verrà impostato automaticamente sull'impostazione dei dati di diagnostica di Windows. Se abiliti questo criterio, Microsoft Edge invierà i dati di utilizzo solo se l'impostazione dei dati di diagnostica di Windows è configurata su Avanzato o Completo. Se disabiliti questo criterio, Microsoft Edge non invierà i dati di utilizzo. I dati relativi agli arresti anomali vengono inviati in base all'impostazione dei dati di diagnostica di Windows. Altre informazioni sui dati di diagnostica di Windows sono disponibili nella pagina https://docs.microsoft.com/it-it/windows/privacy/configure-windows-diagnostic-data-in-your-organization

In Windows 7, Windows 8 e macOS, questo criterio controlla l'invio di dati relativi all'utilizzo e agli arresti anomali. Se non configuri questo criterio, Microsoft Edge userà per impostazione predefinita le preferenze dell'utente.

Per abilitare questo criterio,[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) deve essere abilitato. Se [MetricsReportingEnabled](#metricsreportingenabled) o [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) non sono configurati o sono disabilitati, questi dati non verranno inviati a Microsoft.

Questo criterio è disponibile solo per le istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi, oppure di istanze macOS gestite tramite MDM o che fanno parte di un dominio tramite MCX.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: MetricsReportingEnabled
  - Nome GP: Abilita creazione di report sui dati di utilizzo e relativi all'arresto anomalo del sistema (deprecato)
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: MetricsReportingEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: MetricsReportingEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NativeWindowOcclusionEnabled
  #### Attiva occlusione finestra nativa
  
  
  #### Versioni supportate:
  - Su Windows dal 84 o successiva

  #### Descrizione
  Abilita l'occlusione di finestre native in Microsoft Edge.

Se abiliti questa impostazione, per ridurre l'utilizzo di CPU e il consumo di energia Microsoft Edge rileverà quando una finestra è coperta da altre finestre e sospenderà i pixel di disegno del lavoro.

Se disabiliti questa impostazione Microsoft Edge non rileverà quando una finestra è coperta da altre finestre.

Se questi criteri non vengono impostati, il rilevamento dell'occultamento delle finestre verrà abilitato.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: NativeWindowOcclusionEnabled
  - Nome GP: Attiva occlusione finestra nativa
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: NativeWindowOcclusionEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NavigationDelayForInitialSiteListDownloadTimeout
  #### Imposta un timeout per ritardare l'esplorazione della scheda per l'elenco dei siti in modalità Enterprise.
  
  
  #### Versioni supportate:
  - Su Windows dal 84 o successiva

  #### Descrizione
  Ti consente di impostare un timeout, in secondi per le schede di Microsoft Edge in attesa di essere disponibili per l'esplorazione fino a quando il browser non ha scaricato l'elenco dei siti in modalità Enterprise iniziale.

 Questa impostazione funziona insieme a:
 [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) è impostato su "modalità Internet Explorer"
 e sul criterio
[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) in cui l'elenco ha almeno una voce
 e
[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)è impostato su "Tutte le esplorazioni disponibili" (1).

 Le schede non attenderanno più a lungo di questo timeout per il download dell'elenco di siti in modalità Enterprise. Se il browser non ha completato il download dell'elenco dei siti in modalità Enterprise alla scadenza del timeout, le schede di Microsoft Edge continueranno comunque a essere disponibili per l'esplorazione. Il valore del timeout non deve superare i 20 secondi e non deve essere inferiore di 1 secondo.

 Se imposti il timeout in questo criterio su un valore superiore al valore predefinito di 2 secondi, dopo 2 secondi viene mostrata una barra delle informazioni all'utente. La barra delle informazioni contiene un pulsante che consente all'utente di scegliere di terminare l'attesa del completamento del download dell'elenco dei siti in modalità Enterprise.

 Se non configuri questo criterio, viene utilizzato il timeout predefinito di 2 secondi. Questa impostazione predefinita è soggetta a modifiche in futuro.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: NavigationDelayForInitialSiteListDownloadTimeout
  - Nome GP: Imposta un timeout per ritardare l'esplorazione della scheda per l'elenco dei siti in modalità Enterprise.
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: NavigationDelayForInitialSiteListDownloadTimeout
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x0000000a
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NetworkPredictionOptions
  #### Abilita completamento rete
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Abilita la previsione della rete e impedisce agli utenti di modificare questa impostazione.

Controlla la prelettura DNS, la preconnessione TCP e SSL e il rendering preliminare di pagine Web.

Se non configuri questi criteri, la previsione della rete è abilitata ma l'utente può modificarla.

Mappatura opzioni criteri:

* NetworkPredictionAlways (0) = Prevedi azioni di rete su qualsiasi connessione di rete

* NetworkPredictionWifiOnly (1) = Non supportato, se viene utilizzato questo valore verrà trattato come se fosse impostato "Prevedi azioni di rete su qualsiasi connessione di rete" (0)

* NetworkPredictionNever (2) = Non prevedere azioni di rete su qualsiasi connessione di rete

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: NetworkPredictionOptions
  - Nome GP: Abilita completamento rete
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: NetworkPredictionOptions
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: NetworkPredictionOptions
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### NonRemovableProfileEnabled
  #### Configura se effettuare automaticamente l’accesso del profilo predefinito dell’utente con l’account aziendale o dell'istituto di istruzione
  
  
  #### Versioni supportate:
  - Su Windows dal 78 o successiva

  #### Descrizione
  Questo criterio determina se gli utenti possono rimuovere il profilo di Microsoft Edge che ha effettuato automaticamente l'accesso con un account aziendale o dell'istituto di istruzione.

Se abiliti questo criterio, verrà creato un profilo non rimovibile con l'account aziendale o dell'istituto di istruzione su Windows. Questo profilo non può essere disconnesso o rimosso.

Se disabiliti o non configuri questo criterio, il profilo che ha effettuato automaticamente l'accesso con un account aziendale o dell'istituto di istruzione su Windows potrà venire disconnesso o rimosso dagli utenti.

Se vuoi configurare l'accesso al browser, utilizza il criterio [BrowserSignin](#browsersignin).

Questo criterio è disponibile solo per le istanze di Windows che fanno parte di un dominio Microsoft Active Directory, nelle istanze di Windows 10 Pro o Enterprise registrate per la gestione dei dispositivi.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: NonRemovableProfileEnabled
  - Nome GP: Configura se effettuare automaticamente l’accesso del profilo predefinito dell’utente con l’account aziendale o dell'istituto di istruzione
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: NonRemovableProfileEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### OverrideSecurityRestrictionsOnInsecureOrigin
  #### Controlla dove vengono applicate le restrizioni di sicurezza alle origini non sicure
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica un elenco di origini (URL) o modelli di nome host (ad esempio "*.contoso.com") per cui non si applicano restrizioni di sicurezza per le origini non sicure.

Questi criteri consentono di specificare le origini consentite per le applicazioni legacy che non possono distribuire TLS o impostare un server di gestione temporanea per lo sviluppo Web interno in modo che gli sviluppatori possano testare le funzionalità che richiedono contesti protetti senza la necessità di eseguire la distribuzione di TLS nel server di gestione temporanea. Questi criteri impediscono inoltre all'origine di essere etichettata come "Non protetta" nell'omnibox.

L'impostazione di un elenco di URL in questi criteri ha lo stesso effetto dell'impostazione del flag della riga di comando "--unsafely-treat-insecure-origin-as-secure" su un elenco delimitato da virgole degli stessi URL. Se abiliti questi criteri, viene eseguito l'override del flag della riga di comando.

Per ulteriori informazioni sui contesti protetti, vedi https://www.w3.org/TR/secure-contexts/.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: OverrideSecurityRestrictionsOnInsecureOrigin
  - Nome GP: Controlla dove vengono applicate le restrizioni di sicurezza alle origini non sicure
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\1 = "http://testserver.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\2 = "*.contoso.com"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: OverrideSecurityRestrictionsOnInsecureOrigin
  - Valore di esempio:
``` xml
<array>
  <string>http://testserver.contoso.com/</string>
  <string>*.contoso.com</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PaymentMethodQueryEnabled
  #### Consenti ai siti Web di richiedere metodi di pagamento disponibili
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 80 o in seguito

  #### Descrizione
  Ti consente di specificare se i siti Web possono verificare se l'utente dispone di metodi di pagamento salvati.

Se disabiliti questi criteri, i siti Web che usano l'API PaymentRequest.canMakePayment o PaymentRequest.hasEnrolledInstrument verranno informati che non esistono metodi di pagamento disponibili.

Se abiliti questi criteri o non li configuri, i siti Web possono verificare se l'utente dispone di metodi di pagamento salvati.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PaymentMethodQueryEnabled
  - Nome GP: Consenti ai siti Web di richiedere metodi di pagamento disponibili
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: PaymentMethodQueryEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PaymentMethodQueryEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PersonalizationReportingEnabled
  #### Consenti personalizzazione di annunci, ricerca e notizie inviando la cronologia esplorazioni a Microsoft
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 80 o in seguito

  #### Descrizione
  Questi criteri impediscono a Microsoft di raccogliere la cronologia di esplorazione di Microsoft Edge da usare per personalizzare la pubblicità, la ricerca, le notizie e altri servizi Microsoft.

Questa impostazione è disponibile solo per gli utenti con un account Microsoft. Questa impostazione non è disponibile per gli account figlio o per gli account aziendali.

Se disabiliti questa impostazione dei criteri, gli utenti non potranno modificare o ignorare l'impostazione. Se questi criteri sono abilitati o non configurati, Microsoft Edge verrà utilizzato come preferenza dell'utente.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PersonalizationReportingEnabled
  - Nome GP: Consenti personalizzazione di annunci, ricerca e notizie inviando la cronologia esplorazioni a Microsoft
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: PersonalizationReportingEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PersonalizationReportingEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PinningWizardAllowed
  #### Procedura guidata Aggiungi a barra delle applicazioni
  
  
  #### Versioni supportate:
  - Su Windows dal 80 o successiva

  #### Descrizione
  Microsoft Edge utilizza la procedura guidata Aggiungi a barra delle applicazioni per aiutare gli utenti ad aggiungere i siti suggeriti alla barra delle applicazioni. La funzionalità di procedura guidata Aggiungi alla barra delle applicazioni è abilitata per impostazione predefinita e accessibile per gli utenti dal menu Impostazioni e altro.

Se abiliti o non configuri questi criteri, gli utenti possono richiamare la procedura guidata Aggiungi a barra delle applicazioni dal menu Impostazioni e altro. La procedura guidata può essere richiamata inoltre tramite un avvio del protocollo.

Se disabiliti questi criteri, la procedura guidata Aggiungi a barra delle applicazioni è disabilitata nel menu e non può essere richiamata tramite un avvio del protocollo.

Le impostazioni utente per abilitare o disabilitare la procedura guidata Aggiungi a barra delle applicazioni non sono disponibili.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PinningWizardAllowed
  - Nome GP: Procedura guidata Aggiungi a barra delle applicazioni
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: PinningWizardAllowed
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ProactiveAuthEnabled
  #### Abilita l'autenticazione proattiva
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente di configurare se attivare l'autenticazione proattiva.

Se abiliti questi criteri, Microsoft Edge tenta di autenticare in modo proattivo l'utente connesso ai servizi Microsoft. Microsoft Edge verifica a intervalli regolari un servizio online per la presenza di un manifesto aggiornato contenente la configurazione che determina come eseguire questa operazione.

Se disabiliti questi criteri, Microsoft Edge non tenta di autenticare in modo proattivo l'utente connesso ai servizi Microsoft. Microsoft Edge non esegue più la verifica di un servizio online per la presenza di un manifesto aggiornato contenente la configurazione per questa operazione.

Se non configuri questi criteri, l'autenticazione proattiva è attivata.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ProactiveAuthEnabled
  - Nome GP: Abilita l'autenticazione proattiva
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ProactiveAuthEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ProactiveAuthEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PromotionalTabsEnabled
  #### Abilitare il contenuto promozionale della scheda completa
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Controlla la presentazione dei contenuti promozionali o formativi a scheda intera. Questa impostazione controlla la presentazione delle pagine di benvenuto che consentono agli utenti di accedere a Microsoft Edge, scegliere il browser predefinito o visualizzare informazioni sulle caratteristiche del prodotto.

Se abiliti questi criteri (true) o non li configuri, Microsoft Edge può visualizzare i contenuti a scheda intera agli utenti per fornire informazioni sul prodotto.

Se disabiliti questa impostazione (false), Microsoft Edge non mostra agli utenti i contenuti a scheda intera.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PromotionalTabsEnabled
  - Nome GP: Abilitare il contenuto promozionale della scheda completa
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: PromotionalTabsEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PromotionalTabsEnabled
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### PromptForDownloadLocation
  #### Richiedi la posizione in cui salvare i file scaricati
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica se chiedere la posizione in cui salvare il file prima di scaricarlo.

Se abiliti questi criteri, viene richiesta all'utente la posizione in cui salvare i file prima del download; se non li configuri, i file vengono salvati automaticamente nel percorso predefinito, senza chiedere all'utente.

Se non configuri questi criteri, l'utente sarà in grado di modificare questa impostazione.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: PromptForDownloadLocation
  - Nome GP: Richiedi la posizione in cui salvare i file scaricati
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: PromptForDownloadLocation
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: PromptForDownloadLocation
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### QuicAllowed
  #### Consenti il protocollo QUIC
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente di utilizzare il protocollo QUIC in Microsoft Edge.

Se abiliti o non configuri questi criteri, il protocollo QUIC è consentito.

Se disabiliti questi criteri, il protocollo QUIC è bloccato.

QUIC è un protocollo di rete a livello trasporto che consente di migliorare le prestazioni delle applicazioni Web che attualmente utilizzano TCP.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: QuicAllowed
  - Nome GP: Consenti il protocollo QUIC
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: QuicAllowed
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: QuicAllowed
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### RelaunchNotification
  #### Notifica a un utente che è consigliato o obbligatorio eseguire un riavvio del browser per gli aggiornamenti in sospeso
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Avvisa gli utenti che è necessario riavviare Microsoft Edge per applicare un aggiornamento in sospeso.

Se non configuri questi criteri, Microsoft Edge informa l'utente che è necessario riavviare il browser aggiungendo un'icona Cestino al menu.

Se abiliti questi criteri e li imposti su "Recommended", un avviso ricorrente indica agli utenti che è consigliabile riavviare il computer. L'utente può ignorare questo avviso e rimandare il riavvio.

Se imposti i criteri su "Required", un avviso ricorrente indica agli utenti che il browser viene riavviato automaticamente non appena trascorre il periodo di notifica. Il periodo predefinito è di sette giorni. Puoi configurare questo periodo con i [RelaunchNotificationPeriod](#relaunchnotificationperiod)criteri

La sessione dell'utente viene ripristinata quando si riavvia il browser.

Mappatura opzioni criteri:

* Recommended (1) = Consigliato - Visualizza un prompt ricorrente all'utente che indica che è consigliabile riavviare il sistema

* Required (2) = Obbligatorio - Visualizza un prompt ricorrente all'utente che indica che è obbligatorio riavviare il sistema

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: RelaunchNotification
  - Nome GP: Notifica a un utente che è consigliato o obbligatorio eseguire un riavvio del browser per gli aggiornamenti in sospeso
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: RelaunchNotification
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: RelaunchNotification
  - Valore di esempio:
``` xml
<integer>1</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### RelaunchNotificationPeriod
  #### Imposta il periodo di tempo per le notifiche di aggiornamento
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente di impostare l'intervallo di tempo, in millisecondi, per il quale gli utenti vengono informati che è necessario riavviare Microsoft Edge per applicare un aggiornamento in sospeso.

In questo periodo di tempo, l'utente verrà ripetutamente informato delle necessità di un aggiornamento. In Microsoft Edge, il menu dell'app cambia per indicare che è necessario un riavvio una volta che viene superato un terzo del periodo di notifica. Questa notifica cambia colore quando passano due terzi del periodo di notifica, per cambiare di nuovo una volta che tutto il periodo di notifica è trascorso. Le notifiche aggiuntive abilitate dal criterio [RelaunchNotification](#relaunchnotification) seguono la stessa programmazione.

Se non impostato, viene usato il periodo predefinito di 604.800.000 millisecondi (una settimana).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: RelaunchNotificationPeriod
  - Nome GP: Imposta il periodo di tempo per le notifiche di aggiornamento
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: RelaunchNotificationPeriod
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x240c8400
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: RelaunchNotificationPeriod
  - Valore di esempio:
``` xml
<integer>604800000</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### RendererCodeIntegrityEnabled
  #### Abilita l'integrità del codice di rendering
  
  
  #### Versioni supportate:
  - Su Windows dal 78 o successiva

  #### Descrizione
  Se questi criteri sono abilitati o non impostati, l'integrità del codice di rendering è abilitata. Questi criteri devono essere disabilitati solo se si rilevano problemi di compatibilità con software di terze parti che deve essere utilizzato all'interno ei processi di rendering di Microsoft Edge.

La disabilitazione di questi criteri ha un effetto negativo sulla sicurezza e sulla stabilità di Microsoft Edge perché il codice sconosciuto e potenzialmente ostile può essere caricato all'interno dei processi di rendering di Microsoft Edge.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: RendererCodeIntegrityEnabled
  - Nome GP: Abilita l'integrità del codice di rendering
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: RendererCodeIntegrityEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### RequireOnlineRevocationChecksForLocalAnchors
  #### Specifica se i controlli CRL/OCSP online sono necessari per i trust anchor locali
  
  
  #### Versioni supportate:
  - Su Windows dal 77 o successiva

  #### Descrizione
  Controlla se sono necessarie le verifiche delle revoche online (controlli CRL/OCSP). Se Microsoft Edge non ottiene le informazioni sullo stato di revoca, questi certificati vengono considerati come revocati ("errore bloccante").

Se abiliti questi criteri, Microsoft Edge esegue sempre il controllo della revoca dei certificati del server che vengono convalidati correttamente e quelli firmati da certificati della CA installati localmente.

Se non configuri o disabiliti questi criteri, Microsoft Edge utilizza le impostazioni di controllo della revoca online esistenti.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: RequireOnlineRevocationChecksForLocalAnchors
  - Nome GP: Specifica se i controlli CRL/OCSP online sono necessari per i trust anchor locali
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: RequireOnlineRevocationChecksForLocalAnchors
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ResolveNavigationErrorsUseWebService
  #### Abilita la risoluzione degli errori di navigazione tramite un servizio Web
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consenti a Microsoft Edge di stabilire una connessione dataless a un servizio Web per eseguire il probe delle reti per la connettività, ad esempio per il Wi-Fi in aeroporto e in hotel.

Se abiliti questi criteri, viene utilizzato un servizio Web per i test della connettività di rete.

Se disabiliti questi criteri, Microsoft Edge utilizza le API native per provare a risolvere i problemi di connettività di rete e di navigazione.

**Nota**: ad eccezione di Windows 8 e versioni successive di Windows, Microsoft Edge utilizza *sempre* le API native per risolvere i problemi di connettività.

Se non configuri questi criteri, Microsoft Edge rispetta le preferenze dell'utente impostate in Servizi in edge://settings/privacy.

In particolare, è disponibile un interruttore **Utilizza un servizio Web per aiutare a risolvere gli errori di navigazione** che l'utente può attivare o disattivare. Tieni presente che se hai abilitato questi criteri (ResolveNavigationErrorsUseWebService), l'impostazione **Utilizza un servizio Web per aiutare a risolvere gli errori di navigazione** è attivata, ma l'utente non può modificarla utilizzando l'interruttore. Se hai disabilitato questi criteri, l'impostazione **Utilizza un servizio Web per aiutare a risolvere gli errori di navigazione** è disattivata e l'utente non può modificarla utilizzando l'interruttore.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ResolveNavigationErrorsUseWebService
  - Nome GP: Abilita la risoluzione degli errori di navigazione tramite un servizio Web
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: ResolveNavigationErrorsUseWebService
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ResolveNavigationErrorsUseWebService
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### RestrictSigninToPattern
  #### Limita gli account che possono essere utilizzati come account principali di Microsoft Edge
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente di stabilire quali account possono essere impostati come account principali del browser in Microsoft Edge, ossia l'account scelto durante il flusso esplicito di sincronizzazione.

 Se un utente prova a configurare un account primario del browser con un nome utente che non corrisponde a questo modello, viene bloccato e viene visualizzato il messaggio di errore appropriato. È possibile configurare questo criterio in modo che corrisponda a più account con un'espressione regolare in stile Perl per il modello. Si noti che i criteri distinguono maiuscole e minuscole. Per altre informazioni sulle regole di espressioni regolari usate, fare riferimento a https://go.microsoft.com/fwlink/p/?linkid=2133903.

Se il criterio non viene configurato o lasciato vuoto, gli utenti possono impostare qualsiasi account come account primario del browser in Microsoft Edge.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: RestrictSigninToPattern
  - Nome GP: Limita gli account che possono essere utilizzati come account principali di Microsoft Edge
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: RestrictSigninToPattern
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
".*@contoso.com"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: RestrictSigninToPattern
  - Valore di esempio:
``` xml
<string>.*@contoso.com</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### RoamingProfileLocation
  #### Imposta la directory del profilo mobile
  
  
  #### Versioni supportate:
  - Su Windows dal 85 o successiva

  #### Descrizione
  Configura la directory da utilizzare per memorizzare la copia di roaming dei profili.

Se abiliti questi criteri, Microsoft Edge usa la directory specificata per memorizzare una copia di roaming dei profili, a condizione che siano abilitati anche i criteri [RoamingProfileSupportEnabled](#roamingprofilesupportenabled). Se disabiliti o non configuri i criteri [RoamingProfileSupportEnabled](#roamingprofilesupportenabled), il valore specificato in questi criteri non viene utilizzato.

Per l'elenco delle variabili che puoi usare, vedi [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

Se non configuri questi criteri, viene utilizzato il percorso predefinito del profilo di roaming.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: RoamingProfileLocation
  - Nome GP: Imposta la directory del profilo mobile
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: RoamingProfileLocation
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"${roaming_app_data}\\edge-profile"
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### RoamingProfileSupportEnabled
  #### Abilita l'utilizzo di copie roaming per i dati del profilo di Microsoft Edge
  
  
  #### Versioni supportate:
  - Su Windows dal 85 o successiva

  #### Descrizione
  Abilita questi criteri per utilizzare profili di roaming in Windows. Le impostazioni archiviate nei profili Microsoft Edge (preferiti e preferenze) vengono salvate anche in un file archiviato nella cartella del profilo utente mobile (o nel percorso specificato dall'amministratore tramite i criteri [RoamingProfileLocation](#roamingprofilelocation)).

   Se disabiliti o non configuri questi criteri, vengono utilizzati solo i profili locali normali

I criteri [SyncDisabled](#syncdisabled) disattivano la sincronizzazione dei dati, eseguendo l'override dei criteri.

   Vedi https://docs.microsoft.com/windows-server/storage/folder-redirection/deploy-roaming-user-profiles per ulteriori informazioni sull'utilizzo dei profili utente mobili.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: RoamingProfileSupportEnabled
  - Nome GP: Abilita l'utilizzo di copie roaming per i dati del profilo di Microsoft Edge
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: RoamingProfileSupportEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### RunAllFlashInAllowMode
  #### Estendi l'impostazione dei contenuti Adobe Flash a tutti i contenuti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Se abiliti questi criteri, vengono eseguiti tutti i contenuti Adobe Flash incorporati in siti Web che sono impostati per consentire Adobe Flash nelle impostazioni dei contenuti, dall'utente o dai criteri aziendali. Sono inclusi i contenuti di altre origini e/o di piccole dimensioni.

Per controllare i siti Web che possono eseguire Adobe Flash, vedi le specifiche nei criteri [DefaultPluginsSetting](#defaultpluginssetting), [PluginsAllowedForUrls](#pluginsallowedforurls), and [PluginsBlockedForUrls](#pluginsblockedforurls).

Se disabiliti o non configuri questi criteri, i contenuti Adobe Flash da altre origini (dai siti che non sono specificati nei tre criteri indicati in precedenza) o di piccole dimensioni potrebbero essere bloccati.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: RunAllFlashInAllowMode
  - Nome GP: Estendi l'impostazione dei contenuti Adobe Flash a tutti i contenuti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: RunAllFlashInAllowMode
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: RunAllFlashInAllowMode
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SSLErrorOverrideAllowed
  #### Consenti agli utenti di continuare dalla pagina di avviso HTTPS
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Microsoft Edge mostra una pagina di avviso quando gli utenti visitano i siti che presentano errori SSL.

Se abiliti o non configuri (predefinito) questi criteri, gli utenti possono fare clic su queste pagine di avviso.

Se disabiliti questi criteri, agli utenti viene impedito di fare clic su una pagina di avviso.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SSLErrorOverrideAllowed
  - Nome GP: Consenti agli utenti di continuare dalla pagina di avviso HTTPS
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: SSLErrorOverrideAllowed
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SSLErrorOverrideAllowed
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SSLVersionMin
  #### Versione TLS minima abilitata
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Imposta la versione minima supportata del protocollo SSL. Se non configuri questi criteri, Microsoft Edge utilizza una versione minima predefinita, TLS 1.0.

Se abiliti questi criteri, puoi impostare la versione minima su uno dei valori seguenti: "TLSv1", "TLSv1.1" o "TLSv1.2". Se impostati, Microsoft Edge non utilizza una versione di SSL/TLS inferiore a quella specificata. Qualsiasi valore non riconosciuto viene ignorato.

Mappatura opzioni criteri:

* TLSv1 (tls1) = TLS 1.0

* TLSv1.1 (tls1.1) = TLS 1.1

* TLSv1.2 (tls1.2) = TLS 1.2

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SSLVersionMin
  - Nome GP: Versione TLS minima abilitata
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: SSLVersionMin
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"tls1"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SSLVersionMin
  - Valore di esempio:
``` xml
<string>tls1</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SaveCookiesOnExit
  #### Salvare i cookie alla chiusura di Microsoft Edge
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Quando questo criterio è abilitato, alla chiusura del browser il set di cookie specificato è escluso dall'eliminazione. Questo criterio è valido solo quando:
- L'interruttore 'Cookie e altri dati del sito' è configurato in Impostazioni/Privacy e servizi/Cancella i dati di navigazione alla chiusura o
- Il criterio [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) è abilitato o
- Il criterio [DefaultCookiesSetting](#defaultcookiessetting) è impostato su 'Mantieni cookie per la durata della sessione'.

È possibile definire un elenco di siti, basato su modelli di URL, per cui i cookie verranno mantenuti da una sessione all'altra.

Nota: gli utenti possono comunque modificare l'elenco di siti dei cookie in modo da aggiungere o rimuovere URL. Non possono tuttavia rimuovere gli URL aggiunti da un amministratore.

Se abiliti questo criterio, l'elenco dei cookie non verrà cancellato alla chiusura del browser.

Se disabiliti o non configuri questo criterio, viene usata la configurazione personale dell'utente.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SaveCookiesOnExit
  - Nome GP: Salvare i cookie alla chiusura di Microsoft Edge
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SaveCookiesOnExit
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SavingBrowserHistoryDisabled
  #### Disabilita il salvataggio della cronologia del browser
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Disabilita il salvataggio della cronologia del browser e impedisce agli utenti di modificare questa impostazione.

Se abiliti questi criteri la cronologia esplorazioni non verrà salvata. Disabilita inoltre la sincronizzazione della scheda.

Se disabiliti o non configuri questi criteri, la cronologia esplorazioni verrà salvata.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SavingBrowserHistoryDisabled
  - Nome GP: Disabilita il salvataggio della cronologia del browser
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: SavingBrowserHistoryDisabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SavingBrowserHistoryDisabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ScreenCaptureAllowed
  #### Consentire o negare l'acquisizione dello schermo
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 83 o in seguito

  #### Descrizione
  Se si abilita questo criterio o non lo si configura, una pagina Web può utilizzare le API di condivisione dello schermo (ad esempio getDisplayMedia) o l'API di estensione di acquisizione del desktop) per uno screenshot.
Se si disabilita questo criterio, le chiamate alle API di condivisione dello schermo non andranno a buon fine. Ad esempio, se si utilizza una riunione online basata sul Web, la condivisione del video o dello schermo non funzionerà.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ScreenCaptureAllowed
  - Nome GP: Consentire o negare l'acquisizione dello schermo
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ScreenCaptureAllowed
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ScreenCaptureAllowed
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ScrollToTextFragmentEnabled
  #### Abilita scorrimento verso il testo specificato nei frammenti di URL
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 83 o in seguito

  #### Descrizione
  Questa funzionalità consente alle esplorazioni tramite URL della barra degli indirizzi e collegamento ipertestuale di puntare del testo specifico di destinazione in una pagina Web, che sarà possibile scorrere al termine del caricamento della pagina Web.

Se abiliti o non configuri questo criterio, lo scorrimento della pagina Web verso frammenti di testo specifici tramite un URL sarà abilitato.

Se disabiliti questo criterio, lo scorrimento della pagina Web verso frammenti di testo specifici tramite un URL verrà disabilitato.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ScrollToTextFragmentEnabled
  - Nome GP: Abilita scorrimento verso il testo specificato nei frammenti di URL
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ScrollToTextFragmentEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ScrollToTextFragmentEnabled
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SearchSuggestEnabled
  #### Abilita suggerimenti di ricerca
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Abilita i suggerimenti di ricerca Web nell'elenco dei suggerimenti automatici e nella barra degli indirizzi di Microsoft Edge e impedisce agli utenti di modificare questi criteri.

Se abiliti questi criteri, i suggerimenti di ricerca Web vengono utilizzati.

Se disabiliti questi criteri, i suggerimenti di ricerca Web non vengono mai utilizzati, tuttavia vengono comunque visualizzati i suggerimenti della cronologia e dei preferiti locali. Se disabiliti questi criteri, né i caratteri digitati né gli URL visitati vengono inclusi nella telemetria in Microsoft.

Se questi criteri vengono lasciati non impostati, i suggerimenti di ricerca sono abilitati ma l'utente può modificare tale impostazione.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SearchSuggestEnabled
  - Nome GP: Abilita suggerimenti di ricerca
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: SearchSuggestEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SearchSuggestEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SecurityKeyPermitAttestation
  #### Siti Web o i domini che non richiedono l'autorizzazione per utilizzare l'attestazione per la chiave di sicurezza diretta
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica i siti Web e i domini che non richiedono l'autorizzazione esplicita dell'utente quando vengono richiesti i certificati di attestazione dalle chiavi di sicurezza. Inoltre, alla chiave di sicurezza viene inviato un segnale che indica che è possibile utilizzare un'unica attestazione. Senza questa impostazione, agli utenti viene inviata una richiesta ogni volta che un sito richiede l'attestazione delle chiavi di sicurezza.

I siti (ad esempio https://contoso.com/some/path) corrispondono solo come U2F appID. I domini (ad esempio, contoso.com) corrispondono solo come ID RP webauthn. Per coprire entrambi U2F e le API webauthn per un determinato sito, devi elencare il dominio e l'URL appID.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SecurityKeyPermitAttestation
  - Nome GP: Siti Web o i domini che non richiedono l'autorizzazione per utilizzare l'attestazione per la chiave di sicurezza diretta
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation\1 = "https://contoso.com"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SecurityKeyPermitAttestation
  - Valore di esempio:
``` xml
<array>
  <string>https://contoso.com</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SendIntranetToInternetExplorer
  #### Invia tutti i siti Intranet a Internet Explorer
  
  
  #### Versioni supportate:
  - Su Windows dal 77 o successiva

  #### Descrizione
  Per informazioni sulla configurazione dell'esperienza ottimale per la modalità Internet Explorer, vedi [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SendIntranetToInternetExplorer
  - Nome GP: Invia tutti i siti Intranet a Internet Explorer
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: SendIntranetToInternetExplorer
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SendSiteInfoToImproveServices
  #### Invia informazioni sul sito per migliorare i servizi Microsoft (deprecato)
  >DEPRECAtO: questi criteri sono deprecati. Sono attualmente supportati ma diventeranno obsoleti in una versione futura.
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Questo criterio è deprecato. È attualmente supportato, ma diventerà obsoleto in Microsoft Edge 89. Questo criterio è sostituito dal nuovo criterio:  [DiagnosticData](#diagnosticdata)per Windows 7, Windows 8 e macOS. Questo criterio è sostituito da Consenti telemetria in Windows 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

 Questo criterio abilita l'invio di informazioni sui siti Web visitati in Microsoft Edge a Microsoft per migliorare i servizi come la ricerca.

 Abilita questo criterio per inviare info sui siti Web visitati in Microsoft Edge a Microsoft. Disabilita questo criterio per non inviare info sui siti Web visitati in Microsoft Edge a Microsoft. In entrambi i casi, gli utenti non possono modificare o sostituire l'impostazione.

 In Windows 10, se non configuri questo criterio, Microsoft Edge userà l'impostazione dei dati di diagnostica di Windows. Se questo criterio è abilitato, Microsoft Edge invierà informazioni sui siti Web visitati in Microsoft Edge solo se l'impostazione dei dati di diagnostica di Windows è configurata su completi. Se questo criterio è disabilitato, Microsoft Edge non invierà info sui siti Web visitati. Altre informazioni sui dati di diagnostica di Windows sono disponibili in [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

In Windows 7, Windows 8 e macOS, questo criterio controlla l'invio di info sui siti Web visitati. Se non configuri questo criterio, Microsoft Edge userà per impostazione predefinita le preferenze dell'utente.

 Per abilitare questo criterio, [MetricsReportingEnabled](#metricsreportingenabled) deve essere abilitato. Se [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) o [MetricsReportingEnabled](#metricsreportingenabled) non è configurato o è disabilitato, questi dati non verranno inviati a Microsoft.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SendSiteInfoToImproveServices
  - Nome GP: Invia informazioni sul sito per migliorare i servizi Microsoft (deprecato)
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: SendSiteInfoToImproveServices
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SendSiteInfoToImproveServices
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SensorsAllowedForUrls
  #### Consenti l'accesso ai sensori su siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Definisci un elenco di siti, secondo gli schemi di URL, che possono accedere e utilizzare sensori come i sensori di movimento e di luce

Se non configuri questa impostazione del criterio, per tutti i siti viene utilizzato il valore predefinito globale del criterio [DefaultSensorsSetting](#defaultsensorssetting) (se impostato) o la configurazione personale dell'utente.

Per gli schemi di URL che non corrispondono a questo criterio, viene utilizzato l'ordine di precedenza seguente: il criterio [SensorsBlockedForUrls](#sensorsblockedforurls) (se c’è una corrispondenza), il criterio [DefaultSensorsSetting](#defaultsensorssetting) (se impostato) o le impostazioni personali dell'utente.

Gli schemi di URL definiti in questo criterio non possono essere in conflitto con quelli configurati nel criterio [SensorsBlockedForUrls](#sensorsblockedforurls). Non è possibile contemporaneamente consentire e bloccare un URL.

Per informazioni dettagliate sugli schemi di URL validi, consulta [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SensorsAllowedForUrls
  - Nome GP: Consenti l'accesso ai sensori su siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SensorsAllowedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SensorsBlockedForUrls
  #### Blocca l'accesso ai sensori su siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Definisci un elenco di siti, secondo gli schemi di URL, che non possono accedere a sensori come i sensori di movimento e di luce

Se non configuri questa impostazione del criterio, per tutti i siti viene utilizzato il valore predefinito globale del criterio [DefaultSensorsSetting](#defaultsensorssetting) (se impostato) o la configurazione personale dell'utente.

Per gli schemi di URL che non corrispondono a questo criterio, viene utilizzato l'ordine di precedenza seguente: il criterio [SensorsAllowedForUrls](#sensorsallowedforurls) (se c’è una corrispondenza), il criterio [DefaultSensorsSetting](#defaultsensorssetting) (se impostato) o le impostazioni personali dell'utente.

Gli schemi di URL definiti in questo criterio non possono essere in conflitto con quelli configurati nel criterio [SensorsAllowedForUrls](#sensorsallowedforurls). Non è possibile contemporaneamente consentire e bloccare un URL.

Per informazioni dettagliate sugli schemi di URL validi, consulta [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SensorsBlockedForUrls
  - Nome GP: Blocca l'accesso ai sensori su siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SensorsBlockedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SerialAskForUrls
  #### Consenti l'API Serial su siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Definisci un elenco di siti, secondo gli schemi di URL, che possono chiedere all'utente di accedere a una porta seriale.

Se non configuri questa impostazione del criterio, per tutti i siti viene utilizzato il valore predefinito globale del criterio [DefaultSerialGuardSetting](#defaultserialguardsetting) (se impostato) o la configurazione personale dell'utente.

Per gli schemi di URL che non corrispondono a questo criterio, viene utilizzato l'ordine di precedenza seguente: il criterio [SerialBlockedForUrls](#serialblockedforurls) (se c’è una corrispondenza), il criterio [DefaultSerialGuardSetting](#defaultserialguardsetting) (se impostato) o le impostazioni personali dell'utente.

Gli schemi di URL definiti in questo criterio non possono essere in conflitto con quelli configurati nel criterio [SerialBlockedForUrls](#serialblockedforurls). Non è possibile contemporaneamente consentire e bloccare un URL.

Per informazioni dettagliate sugli schemi di URL validi, consulta [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SerialAskForUrls
  - Nome GP: Consenti l'API Serial su siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SerialAskForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SerialBlockedForUrls
  #### Blocca l'API Serial su siti specifici
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Definisci un elenco di siti, secondo gli schemi di URL, che non possono chiedere all'utente di concedere l'accesso a una porta seriale.

Se non configuri questa impostazione del criterio, per tutti i siti viene utilizzato il valore predefinito globale del criterio [DefaultSerialGuardSetting](#defaultserialguardsetting) (se impostato) o la configurazione personale dell'utente.

Per gli schemi di URL che non corrispondono a questo criterio, viene utilizzato l'ordine di precedenza seguente: il criterio [SerialAskForUrls](#serialaskforurls) (se c’è una corrispondenza), il criterio [DefaultSerialGuardSetting](#defaultserialguardsetting) (se impostato) o le impostazioni personali dell'utente.

Gli schemi di URL in questo criterio non possono essere in conflitto con quelli configurati nel criterio [SerialAskForUrls](#serialaskforurls). Non è possibile contemporaneamente consentire e bloccare un URL.

Per informazioni dettagliate sugli schemi di URL validi, consulta [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SerialBlockedForUrls
  - Nome GP: Blocca l'API Serial su siti specifici
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SerialBlockedForUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### ShowOfficeShortcutInFavoritesBar
  #### Mostra collegamento Microsoft Office sulla barra Preferiti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica se includere un collegamento a Office.com nella barra Preferiti. Per gli utenti che hanno effettuato l'accesso a Microsoft Edge il collegamento indirizza gli utenti verso le app e i documenti di Microsoft Office.

Se questi criteri sono abilitati o non configurati, gli utenti possono scegliere se visualizzare il collegamento modificando l'interruttore nel menu di scelta rapida della barra Preferiti.

Se i criteri sono disabilitati, il collegamento non viene visualizzato.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: ShowOfficeShortcutInFavoritesBar
  - Nome GP: Mostra collegamento Microsoft Office sulla barra Preferiti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: ShowOfficeShortcutInFavoritesBar
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: ShowOfficeShortcutInFavoritesBar
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SignedHTTPExchangeEnabled
  #### Abilita supporto Signed HTTP Exchange (SXG)
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 78 o in seguito

  #### Descrizione
  Abilita il supporto Signed HTTP Exchange (SXG).

Se questi criteri non sono impostati o abilitati, Microsoft Edge accetta i contenuti Web serviti come Signed HTTP Exchange.

Se questi criteri sono disabilitati, non è possibile caricare Signed HTTP Exchange.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SignedHTTPExchangeEnabled
  - Nome GP: Abilita supporto Signed HTTP Exchange (SXG)
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: SignedHTTPExchangeEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SignedHTTPExchangeEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SitePerProcess
  #### Abilita l'isolamento per ogni sito
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  È possibile utilizzare i criteri [SitePerProcess](#siteperprocess) per impedire agli utenti di rifiutare esplicitamente il comportamento predefinito dell'isolamento di tutti i siti. Tieni presente che è inoltre possibile utilizzare i criteri [IsolateOrigins](#isolateorigins) per isolare altre origini in modo più dettagliato.
Se abiliti questi criteri, gli utenti non potranno rifiutare esplicitamente il comportamento predefinito per cui ogni sito viene eseguito nel proprio processo.
Se disabiliti o non configuri questi criteri, un utente può rifiutare esplicitamente l'isolamento del sito, ad esempio utilizzando la voce "Disabilita isolamento sito" in edge://flags. Se disabiliti o non configuri i criteri, l'isolamento del sito non viene disattivato.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SitePerProcess
  - Nome GP: Abilita l'isolamento per ogni sito
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: SitePerProcess
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SitePerProcess
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SpellcheckEnabled
  #### Abilita controllo ortografia
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Se abiliti o non configuri questi criteri, l'utente può utilizzare il controllo ortografico.

Se disabiliti questi criteri, l'utente non può utilizzare il controllo ortografico e anche i criteri [SpellcheckLanguage](#spellchecklanguage) e [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) sono disabilitati.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SpellcheckEnabled
  - Nome GP: Abilita controllo ortografia
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: SpellcheckEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SpellcheckEnabled
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SpellcheckLanguage
  #### Attiva lingua specifica per controllo ortografia
  
  
  #### Versioni supportate:
  - Su Windows dal 77 o successiva

  #### Descrizione
  Abilita diverse lingue per il controllo ortografico. Qualsiasi lingua specificata che non viene riconosciuta viene ignorata.

Se abiliti questi criteri, il controllo ortografico è abilitato per le lingue specificate, nonché per tutte le lingue abilitate dall'utente.

Se non configuri o disabiliti questi criteri, nessuna modifica viene apportata alle preferenze del controllo ortografico dell'utente.

Se i criteri [SpellcheckEnabled](#spellcheckenabled) sono disabilitati, non hanno effetto.

Se una lingua è inclusa in entrambi i criteri [SpellcheckLanguage](#spellchecklanguage) e [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist), la lingua del controllo ortografico viene abilitata.

Le lingue supportate sono: af, bg, ca, cs, cy, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SpellcheckLanguage
  - Nome GP: Attiva lingua specifica per controllo ortografia
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\2 = "es"

```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SpellcheckLanguageBlocklist
  #### Forza disattivazione lingue per controllo ortografico
  
  
  #### Versioni supportate:
  - Su Windows dal 78 o successiva

  #### Descrizione
  Forza la disabilitazione delle lingue del controllo ortografico. Le lingue non riconosciute in questo elenco vengono ignorate.

Se abiliti questi criteri, il controllo ortografico è disabilitato per le lingue specificate. L'utente può comunque abilitare o disabilitare il controllo ortografico per le lingue non incluse nell'elenco.

Se non imposti o disabiliti questi criteri, nessuna modifica viene apportata alle preferenze del controllo ortografico dell'utente.

Se i criteri [SpellcheckEnabled](#spellcheckenabled) sono disabilitati, non hanno effetto.

Se una lingua è inclusa in entrambi i criteri [SpellcheckLanguage](#spellchecklanguage) and the 'SpellcheckLanguageBlocklist, la lingua del controllo ortografico viene abilitata.

Le lingue attualmente supportate sono: af, bg, ca, cs, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SpellcheckLanguageBlocklist
  - Nome GP: Forza disattivazione lingue per controllo ortografico
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\2 = "es"

```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### StricterMixedContentTreatmentEnabled
  #### Abilita trattamento più rigoroso per il contenuto misto (deprecato)
  >DEPRECAtO: questi criteri sono deprecati. Sono attualmente supportati ma diventeranno obsoleti in una versione futura.
  
  #### Versioni supportate:
  - Su Windows e macOS dal 81 o in seguito

  #### Descrizione
  Questo criterio è deprecato perché è inteso solo come un meccanismo a breve termine per dare alle aziende più tempo per aggiornare il loro contenuto Web se e quando si ritiene che sia incompatibile con un trattamento di contenuto misto più rigoroso. Non funzionerà in Microsoft Edge dalla versione 85.

Questo criterio controlla il trattamento per il contenuto misto (contenuto HTTP nei siti HTTPS) nel browser.

Se imposti questo criterio su true o not set, il contenuto misto audio e video verrà automaticamente aggiornato a HTTPS (ovvero, l'URL verrà riscritto come HTTPS, senza fallback se la risorsa non è disponibile su HTTPS) e un avviso "Non sicuro" verrà visualizzato nella barra degli URL per i contenuti misti di immagini.

Se imposti il criterio su false, gli aggiornamenti automatici verranno disabilitati per audio e video e non verrà mostrato alcun avviso per le immagini.

Questo criterio non influisce su altri tipi di contenuti misti diversi da audio, video e immagini.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: StricterMixedContentTreatmentEnabled
  - Nome GP: Abilita trattamento più rigoroso per il contenuto misto (deprecato)
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: StricterMixedContentTreatmentEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: StricterMixedContentTreatmentEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SuppressUnsupportedOSWarning
  #### Elimina l'avviso di sistema operativo non supportato
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Elimina l'avviso visualizzato quando Microsoft Edge è in esecuzione in un computer o in un sistema operativo che non è più supportato.

Se questo criterio è falso o non impostato, gli avvisi verranno visualizzati in tali computer o sistemi operativi non supportati.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SuppressUnsupportedOSWarning
  - Nome GP: Elimina l'avviso di sistema operativo non supportato
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: SuppressUnsupportedOSWarning
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SuppressUnsupportedOSWarning
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SyncDisabled
  #### Disabilita la sincronizzazione dei dati mediante i servizi di sincronizzazione Microsoft
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Disabilita la sincronizzazione dei dati in Microsoft Edge. Questi criteri impediscono, inoltre, la visualizzazione della richiesta di consenso alla sincronizzazione.

Se non imposti questi criteri o non li applichi come consigliato, gli utenti potranno attivare o disattivare la sincronizzazione. Se l'applicazione di questi criteri viene resa obbligatoria, gli utenti non saranno in grado di abilitare la sincronizzazione.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SyncDisabled
  - Nome GP: Disabilita la sincronizzazione dei dati mediante i servizi di sincronizzazione Microsoft
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: SyncDisabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SyncDisabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### SyncTypesListDisabled
  #### Configura l'elenco di caratteri esclusi dalla sincronizzazione
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 83 o in seguito

  #### Descrizione
  Abilitando questo criterio, tutti i tipi di dati specificati verranno esclusi dalla sincronizzazione. Questo criterio può essere usato per limitare il tipo di dati caricati nel servizio di sincronizzazione di Microsoft Edge.

È possibile specificare uno dei tipi di dati seguenti per questo criterio: favorites", "settings", "passwords", "addressesAndMore", "extensions", "history", "openTabs" e "collections. I nomi dei tipi di dati fanno distinzione tra maiuscole e minuscole.

Gli utenti non potranno eseguire l'override dei tipi di dati disabilitati.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: SyncTypesListDisabled
  - Nome GP: Configura l'elenco di caratteri esclusi dalla sincronizzazione
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled\1 = "favorites"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: SyncTypesListDisabled
  - Valore di esempio:
``` xml
<array>
  <string>favorites</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### TLS13HardeningForLocalAnchorsEnabled
  #### Abilita una funzionalità di sicurezza TLS 1.3 per i trust anchor locali. (obsoleto)
  
  >OBSOLETO: questo criterio è obsoleto e non funziona nelle versioni di Microsoft Edge successive alla versione 85.
  #### Versioni supportate:
  - Su Windows e macOS dal 81, fino al 85

  #### Descrizione
  Questo criterio non funziona perché era inteso solo come meccanismo a breve termine per dare alle aziende più tempo per aggiornare i proxy interessati.

Questo criterio controlla una funzionalità di sicurezza in TLS 1.3 che protegge le connessioni dagli attacchi di tipo downgrade. È compatibile con le versioni precedenti e non influirà sulle connessioni a server o proxy TLS 1.2 compatibili. Tuttavia, le versioni precedenti di alcuni proxy di intercettazione TLS presentano un difetto di implementazione che ne causa l'incompatibilità.

Se abiliti questo criterio o non lo imposti, Microsoft Edge abiliterà queste protezioni di sicurezza per tutte le connessioni.

Se disabiliti questo criterio, Microsoft Edge disabiliterà queste protezioni di sicurezza per le connessioni autenticate con certificati CA installati in locale. Queste protezioni sono sempre abilitate per le connessioni autenticate con certificati CA pubblicamente attendibili.

È possibile usare questo criterio per testare eventuali proxy interessati e aggiornarli. Le connessioni sui proxy interessati non riescono e viene restituito un codice di errore ERR_TLS13_DOWNGRADE_DETECTED.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: TLS13HardeningForLocalAnchorsEnabled
  - Nome GP: Abilita una funzionalità di sicurezza TLS 1.3 per i trust anchor locali. (obsoleto)
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: TLS13HardeningForLocalAnchorsEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: TLS13HardeningForLocalAnchorsEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### TLSCipherSuiteDenyList
  #### Specifica i pacchetti di crittografia TLS da disabilitare
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 85 o in seguito

  #### Descrizione
  Configura l'elenco dei pacchetti di crittografia che sono disabilitati per le connessioni TLS.

Se configuri questo criterio, l'elenco di pacchetti di crittografia configurati non sarà usato quando si stabiliscono connessioni TLS.

Se non configuri questo criterio, il browser sceglierà quali pacchetti di crittografia TLS usare.

I valori dei pacchetti di crittografia da disabilitare sono specificati come valori esadecimali a 16 bit. I valori sono assegnati dal Registro di sistema di IANA (Internet Assigned Numbers Authority).

Il pacchetto di crittografia TLS 1.3 TLS_AES_128_GCM_SHA256 (0x1301) è necessario per TLS 1.3 e non può essere disabilitato da questo criterio.

Questo criterio non influisce sulle connessioni basate su QUIC. È possibile disattivare QUIC tramite il criterio [QuicAllowed](#quicallowed).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: TLSCipherSuiteDenyList
  - Nome GP: Specifica i pacchetti di crittografia TLS da disabilitare
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\1 = "0x1303"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\2 = "0xcca8"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\3 = "0xcca9"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: TLSCipherSuiteDenyList
  - Valore di esempio:
``` xml
<array>
  <string>0x1303</string>
  <string>0xcca8</string>
  <string>0xcca9</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### TabFreezingEnabled
  #### Consenti blocco delle schede in background
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 79 o in seguito

  #### Descrizione
  Controlla se Microsoft Edge è in grado di bloccare le schede in background per almeno 5 minuti.

Il blocco delle schede riduce l'uso della CPU, della batteria e della memoria. Microsoft Edge utilizza l'euristica per evitare di bloccare le schede che svolgono funzioni utili in background, ad esempio notifiche di visualizzazione, riproduzione audio e riproduzione in streaming di video.

Se abiliti questi criteri o non li configuri, le schede in background per almeno 5 minuti potrebbero essere bloccate.

Se disabiliti questi criteri, nessuna scheda verrà bloccata.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: TabFreezingEnabled
  - Nome GP: Consenti blocco delle schede in background
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: TabFreezingEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: TabFreezingEnabled
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### TaskManagerEndProcessEnabled
  #### Abilita l'interruzione dei processi in Gestione attività del browser
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Se abiliti o non configuri questi criteri, gli utenti possono terminare i processi in Gestione attività del browser. Se li disabiliti, gli utenti non possono terminare i processi e pulsante Termina processo è disabilitato in Gestione attività del browser.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: TaskManagerEndProcessEnabled
  - Nome GP: Abilita l'interruzione dei processi in Gestione attività del browser
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: TaskManagerEndProcessEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: TaskManagerEndProcessEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### TotalMemoryLimitMb
  #### Imposta in megabyte il limite di memoria che può essere utilizzata da un'unica istanza di Microsoft Edge.
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 80 o in seguito

  #### Descrizione
  Configura la quantità di memoria che una singola istanza di Microsoft Edge può utilizzare prima che le schede inizino a essere rimosse per risparmiare memoria. La memoria utilizzata dalla scheda verrà liberata e sarà necessario ricaricare la scheda in caso di commutazione.

Se abiliti questi criteri, il browser inizierà a rimuovere le schede per risparmiare memoria dopo che il limite è stato superato. Tuttavia, non vi è alcuna garanzia il browser sia sempre in esecuzione nei limiti. Qualsiasi valore inferiore a 1024 verrà arrotondato a 1024.

Se non imposti questi criteri, il browser tenterà di risparmiare memoria solo quando viene rilevato che la quantità di memoria fisica del computer è insufficiente.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: TotalMemoryLimitMb
  - Nome GP: Imposta in megabyte il limite di memoria che può essere utilizzata da un'unica istanza di Microsoft Edge.
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: TotalMemoryLimitMb
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000800
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: TotalMemoryLimitMb
  - Valore di esempio:
``` xml
<integer>2048</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### TrackingPrevention
  #### Blocca il rilevamento dell'attività di esplorazione Web degli utenti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 78 o in seguito

  #### Descrizione
  Consente di decidere se impedire ai siti Web di tenere traccia delle attività di navigazione Web degli utenti.

Se si disabilita questo criterio o non lo si configura, gli utenti possono impostare il proprio livello di prevenzione della verifica.

Mappatura opzioni criteri:

* TrackingPreventionOff (0) = Disattivato (nessuna prevenzione del monitoraggio)

* TrackingPreventionBasic (1) = Di base (blocca i tracker dannosi, il contenuto e gli annunci saranno personalizzati)

* TrackingPreventionBalanced (2) = Bilanciato (blocca i tracker dannosi e i tracker dei siti non visitati dall'utente; il contenuto e gli annunci saranno meno personalizzati)

* TrackingPreventionStrict (3) = Rigido (blocca i tracker dannosi e la maggior parte dei tracker da tutti i siti; il contenuto e gli annunci avranno una personalizzazione minima. Alcune parti di siti potrebbero non funzionare).

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: TrackingPrevention
  - Nome GP: Blocca il rilevamento dell'attività di esplorazione Web degli utenti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: TrackingPrevention
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000002
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: TrackingPrevention
  - Valore di esempio:
``` xml
<integer>2</integer>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### TranslateEnabled
  #### Abilita traduzione
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Abilita il servizio di traduzione Microsoft integrato in Microsoft Edge.

Se abiliti questi criteri, Microsoft Edge offre funzionalità di traduzione all'utente visualizzando un riquadro a comparsa di traduzione integrato (ove appropriato) e l'opzione di traduzione nel menu di scelta rapida del pulsante destro del mouse.

Disabilita questi criteri per disabilitare tutte le funzionalità di traduzione predefinite.

Se non configuri i criteri, gli utenti possono scegliere se utilizzare o meno la funzionalità di traduzione.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: Sì
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: TranslateEnabled
  - Nome GP: Abilita traduzione
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): Modelli amministrativi/Microsoft Edge - Impostazioni predefinite (sostituibili dagli utenti)/
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): SOFTWARE\Policies\Microsoft\Edge\Consigliati
  - Nome valore: TranslateEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: TranslateEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### URLAllowlist
  #### Definisci un elenco di URL consentiti
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consenti l'accesso agli URL nell'elenco, come eccezioni all'elenco degli URL bloccati.

Usa il formato di modello di URL indicato in [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) format.

Puoi utilizzare questo criterio per aprire eccezioni per gli elenchi Blocca. Ad esempio, puoi includere "*" nell'elenco Blocca per bloccare tutte le richieste e quindi utilizzare questo criterio per consentire l'accesso a un elenco limitato di URL. Puoi usare questo criterio per aprire eccezioni a determinati schemi, sottodomini di altri domini, porte o percorsi specifici.

Il filtro più specifico determina se un URL è bloccato o consentito. L'elenco Consenti è prioritario rispetto all'elenco Blocca.

Questo criterio è limitato a 1.000 voci, le voci successive vengono ignorate.

Questo criterio consente anche al browser di richiamare automaticamente applicazioni esterne registrate come gestori protocollo per protocolli come "tel:" o "ssh:".

Se non configuri questo criterio, non saranno presenti eccezioni all'elenco Blocca nel criterio [URLBlocklist](#urlblocklist).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: URLAllowlist
  - Nome GP: Definisci un elenco di URL consentiti
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\URLAllowlist
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\5 = ".exact.hostname.com"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: URLAllowlist
  - Valore di esempio:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### URLBlocklist
  #### Blocca l'accesso a un elenco di URL
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Definisci un elenco di siti basati sui modelli di URL che sono bloccati (gli utenti non possono caricarli).

Usa il formato di modello di URL indicato in [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Puoi definire le eccezioni nei criteri [URLAllowlist](#urlallowlist). Questi criteri sono limitati a 1000 voci. Le voci successive vengono ignorate.

Tieni presente che non è consigliato bloccare gli URL interni "edge://*" in quanto possono verificarsi errori imprevisti.

Questi criteri non impediscono l'aggiornamento dinamico della pagina tramite JavaScript. Ad esempio, se blocchi "contoso.com/abc", gli utenti potrebbero comunque essere in grado di visitare "contoso.com" e fare clic su un collegamento per aprire "contoso.com/abc" fintanto che la pagina non viene aggiornata.

Se non configuri questi criteri, nessun URL è bloccato.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: URLBlocklist
  - Nome GP: Blocca l'accesso a un elenco di URL
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\URLBlocklist
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\3 = "hosting.com/bad_path"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\5 = ".exact.hostname.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\6 = "file://*"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\7 = "custom_scheme:*"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\8 = "*"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: URLBlocklist
  - Valore di esempio:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/bad_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
  <string>file://*</string>
  <string>custom_scheme:*</string>
  <string>*</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### UserAgentClientHintsEnabled
  #### Abilita la funzionalità User-Agent Client Hints (deprecato)
  >DEPRECAtO: questi criteri sono deprecati. Sono attualmente supportati ma diventeranno obsoleti in una versione futura.
  
  #### Versioni supportate:
  - Su Windows e macOS dal 86 o in seguito

  #### Descrizione
  Questo criterio è deprecato perché è inteso solo come meccanismo a breve termine per dare alle aziende più tempo per aggiornare il contenuto Web se e quando viene rilevato che è incompatibile con la funzionalità User-Agent Client Hints. Non funzionerà in Microsoft Edge versione 89.

Se abilitata, la funzionalità User-Agent Client Hints invia intestazioni di richiesta granulari che forniscono informazioni sul browser dell'utente, ad esempio la versione del browser, e sull'ambiente, ad esempio l'architettura di sistema.

Questa è una funzionalità additiva, ma le nuove intestazioni potrebbero compromettere il funzionamento di alcuni siti Web che limitano i caratteri che le richieste possono contenere.

Se abiliti o non configuri questo criterio, la funzionalità User-Agent Client Hints sarà abilitata. Se disabiliti questo criterio, la funzionalità non sarà disponibile.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: UserAgentClientHintsEnabled
  - Nome GP: Abilita la funzionalità User-Agent Client Hints (deprecato)
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: UserAgentClientHintsEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: UserAgentClientHintsEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### UserDataDir
  #### Imposta la directory dei dati dell'utente
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Imposta la directory da utilizzare per l'archiviazione dei dati dell'utente.

Se abiliti questo criterio, Microsoft Edge utilizza la directory specificata indipendentemente dal fatto che l'utente abbia impostato il flag della riga di comando "--user-data-dir".

Se non abiliti questo criterio, viene utilizzato il percorso del profilo predefinito, ma l'utente può sostituirlo utilizzando il flag "--user-data-dir". Gli utenti possono trovare la directory per il profilo in edge://version/ nel percorso del profilo.

Per evitare la perdita di dati o altri errori, non configurare questo criterio con la directory radice di un volume o con una directory utilizzata per altri scopi, perché Microsoft Edge ne gestisce il contenuto.

Per un elenco di variabili che è possibile utilizzare, vedi [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: UserDataDir
  - Nome GP: Imposta la directory dei dati dell'utente
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: UserDataDir
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"${users}/${user_name}/Edge"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: UserDataDir
  - Valore di esempio:
``` xml
<string>${users}/${user_name}/Edge</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### UserDataSnapshotRetentionLimit
  #### Limita il numero di snapshot dei dati utente conservati per l'utilizzo in caso di rollback di emergenza
  
  
  #### Versioni supportate:
  - Su Windows dal 86 o successiva

  #### Descrizione
  Dopo ogni aggiornamento della versione principale, Microsoft Edge creerà uno snapshot di parti dei dati di navigazione dell'utente da utilizzare in caso di un'emergenza successiva che richiede un rollback temporaneo della versione. Se viene eseguito un rollback temporaneo su una versione per la quale un utente dispone di uno snapshot corrispondente, i dati nello snapshot vengono ripristinati. Ciò consente agli utenti di mantenere impostazioni come segnalibri e dati di riempimento automatico.

Se non imposti questo criterio, viene utilizzato il valore predefinito di 3 snapshot.

Se imposti questo criterio, gli snapshot precedenti vengono eliminati secondo necessità per rispettare il limite impostato. Se imposti questo criterio su 0, non vengono acquisiti snapshot.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Numero intero

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: UserDataSnapshotRetentionLimit
  - Nome GP: Limita il numero di snapshot dei dati utente conservati per l'utilizzo in caso di rollback di emergenza
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: UserDataSnapshotRetentionLimit
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000003
```


  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### UserFeedbackAllowed
  #### Consenti feedback utente
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Microsoft Edge utilizza la funzionalità Feedback di Edge (abilitata per impostazione predefinita) per consentire agli utenti di inviare feedback, suggerimenti o sondaggi del cliente e segnalare problemi con il browser. Inoltre, per impostazione predefinita, gli utenti non possono disabilitare (disattivare) la funzionalità Feedback di Edge.

Se abiliti o non configuri questi criteri, gli utenti possono richiamare Feedback di Edge.

Se disabiliti questi criteri, gli utenti non possono richiamare Feedback di Edge.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: UserFeedbackAllowed
  - Nome GP: Consenti feedback utente
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: UserFeedbackAllowed
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: UserFeedbackAllowed
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### VideoCaptureAllowed
  #### Consenti o blocca l'acquisizione video
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Controlla se i siti possono acquisire video.

Se abiliti o non configuri (predefinito) questi criteri, all'utente viene richiesto di confermare l'accesso all'acquisizione video per tutti i siti, ad eccezione di quelli con gli URL configurati nell'elenco dei criteri [VideoCaptureAllowedUrls](#videocaptureallowedurls), a cui verrà concesso l'accesso senza chiedere conferma.

Se disabiliti questi criteri, non viene visualizzata alcuna richiesta per l'utente e l'acquisizione video è disponibile solo per gli URL configurati nei criteri [VideoCaptureAllowedUrls](#videocaptureallowedurls).

Questi criteri interessano tutti i tipi di input video e non solo la videocamera integrata.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: VideoCaptureAllowed
  - Nome GP: Consenti o blocca l'acquisizione video
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: VideoCaptureAllowed
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000000
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: VideoCaptureAllowed
  - Valore di esempio:
``` xml
<false/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### VideoCaptureAllowedUrls
  #### Siti che possono accedere ai dispositivi di acquisizione video senza richiedere l'autorizzazione
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Specifica i siti Web, in base agli schemi URL, che possono utilizzare dispositivi di acquisizione video senza richiedere l'autorizzazione all'utente. I modelli in questo elenco vengono messi a confronto con l'origine di sicurezza dell'URL di richiesta. Se corrispondono, al sito viene automaticamente consentito l'accesso ai dispositivi di acquisizione video.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: VideoCaptureAllowedUrls
  - Nome GP: Siti che possono accedere ai dispositivi di acquisizione video senza richiedere l'autorizzazione
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: VideoCaptureAllowedUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### WPADQuickCheckEnabled
  #### Imposta ottimizzazione WPAD
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente di disattivare l'ottimizzazione WPAD (Web Proxy Auto-Discovery) in Microsoft Edge.

Se disabiliti questi criteri, l'ottimizzazione WPAD è disabilitata e pertanto l'attesa del browser per i server WPAD basati su DNS è più lunga.

Se abiliti o non configuri i criteri, l'ottimizzazione WPAD è abilitata.

Indipendentemente dall'abilitazione o meno di questi criteri, l'impostazione dell'ottimizzazione WPAD non può essere modificata dagli utenti.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: WPADQuickCheckEnabled
  - Nome GP: Imposta ottimizzazione WPAD
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: WPADQuickCheckEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: WPADQuickCheckEnabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### WebAppInstallForceList
  #### Configura l'elenco delle app Web con installazione forzata
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 80 o in seguito

  #### Descrizione
  Specifica un elenco di siti Web installati automaticamente, senza interazione dell'utente, che non possono essere disinstallati o disattivati dall'utente.

Ogni voce di elenco dei criteri è un oggetto con i seguenti membri:
  -"url", che è obbligatorio. "url" deve essere l'URL dell'app Web da installare.

I valori dei membri facoltativi sono:
  -"launch_container" deve essere "window" o "tab" per indicare come verrà aperta l'app Web dopo l'installazione.
  -"create_desktop_shortcut" deve essere true se è necessario creare un collegamento sul desktop in Windows.

Se "default_launch_container" viene omesso, l'app verrà aperta in una scheda per impostazione predefinita. Indipendentemente dal valore di "default_launch_container", gli utenti possono modificare il contenitore in cui si aprirà l'app. Se "create_desktop_shortcuts" viene omesso, non verranno creati collegamenti sul desktop.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: Sì

  #### Tipo di dati:
  - Dizionario

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: WebAppInstallForceList
  - Nome GP: Configura l'elenco delle app Web con installazione forzata
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: WebAppInstallForceList
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\WebAppInstallForceList = [
  {
    "create_desktop_shortcut": true, 
    "default_launch_container": "window", 
    "url": "https://www.contoso.com/maps"
  }, 
  {
    "default_launch_container": "tab", 
    "url": "https://app.contoso.edu"
  }
]
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: WebAppInstallForceList
  - Valore di esempio:
``` xml
<key>WebAppInstallForceList</key>
<array>
  <dict>
    <key>create_desktop_shortcut</key>
    <true/>
    <key>default_launch_container</key>
    <string>window</string>
    <key>url</key>
    <string>https://www.contoso.com/maps</string>
  </dict>
  <dict>
    <key>default_launch_container</key>
    <string>tab</string>
    <key>url</key>
    <string>https://app.contoso.edu</string>
  </dict>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### WebComponentsV0Enabled
  #### Riabilita l'API dei componenti Web v0 fino alla versione M84 (obsoleto)
  
  >OBSOLETO: questo criterio è obsoleto e non funziona nelle versioni di Microsoft Edge successive alla versione 84.
  #### Versioni supportate:
  - Su Windows e macOS dal 80, fino al 84

  #### Descrizione
  Questo criterio non funziona perché ha consentito di riattivare selettivamente queste funzionalità fino a Microsoft Edge versione 85. Le API Web Components v0 (Shadow DOM v0, Custom Elements v0 e HTML Imports) sono state deprecate nel 2018 e sono state disabilitate per impostazione predefinita a partire da Microsoft Edge versione 80.

Se imposti questo criterio su True, le funzionalità di Web Components v0 saranno abilitate per tutti i siti.

Se imposti questo criterio su False o non imposti questo criterio, le funzionalità di Web Components v0 verranno disabilitate per impostazione predefinita, a partire da Microsoft Edge versione 80.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: WebComponentsV0Enabled
  - Nome GP: Riabilita l'API dei componenti Web v0 fino alla versione M84 (obsoleto)
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: WebComponentsV0Enabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: WebComponentsV0Enabled
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### WebDriverOverridesIncompatiblePolicies
  #### Consenti a WebDriver di sostituire i criteri non compatibili (obsoleto)
  
  >OBSOLETO: questo criterio è obsoleto e non funziona nelle versioni di Microsoft Edge successive alla versione 84.
  #### Versioni supportate:
  - Su Windows e macOS dal 77, fino al 84

  #### Descrizione
  Questi criteri non funzioneranno, in quanto WebDriver è ora compatibile con tutti i criteri esistenti.

     Questi criteri consentono agli utenti della funzionalità WebDriver di sovrascrivere
i criteri che possono interferire con il suo funzionamento.

     Attualmente questi criteri disabilitano i criteri [SitePerProcess](#siteperprocess) e [IsolateOrigins](#isolateorigins).

     Se i criteri sono abilitati, WebDriver sarà in grado di sovrascrivere i criteri
     incompatibili.
     Se i criteri sono disabilitati o non configurati, a WebDriver non sarà consentito
     di sovrascrivere i criteri incompatibili.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: WebDriverOverridesIncompatiblePolicies
  - Nome GP: Consenti a WebDriver di sostituire i criteri non compatibili (obsoleto)
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: WebDriverOverridesIncompatiblePolicies
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: WebDriverOverridesIncompatiblePolicies
  - Valore di esempio:
``` xml
<true/>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### WebRtcLocalIpsAllowedUrls
  #### Gestisci l'esposizione degli indirizzi IP locali da WebRTC
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 80 o in seguito

  #### Descrizione
  Specifica un elenco di origini (URL) o modelli di nome host (ad esempio "*contoso.com*") per cui l'indirizzo IP locale deve essere esposto da WebRTC.

Se abiliti questi criteri e imposti un elenco di origini (URL) o modelli di nomi host, quando edge://flags/#enable-webrtc-hide-local-ips-with-mdns è abilitato, WebRTC esporrà l'indirizzo IP locale per i casi che corrispondono a modelli nell'elenco.

Se disabiliti o non configuri questi criteri e edge://flags/#enable-webrtc-hide-local-ips-with-mdns è abilitato, WebRTC non esporrà gli indirizzi IP locali. L'indirizzo IP locale è nascosto con un nome host mDNS.

Se abiliti, disabiliti o non configuri questi criteri e edge://flags/#enable-webrtc-hide-local-ips-with-mdns è disabilitato, WebRTC esporrà gli indirizzi IP locali.

Tieni presente che questi criteri indeboliscono la protezione degli indirizzi IP locali che potrebbero essere necessari per gli amministratori.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Elenco di stringhe

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: WebRtcLocalIpsAllowedUrls
  - Nome GP: Gestisci l'esposizione degli indirizzi IP locali da WebRTC
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls
  - Percorso (Consigliati): N/D
  - Nome valore: 1, 2, 3, ...
  - Tipo di valore: elenco di REG_SZ
  ##### Valore di esempio:
```
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\2 = "*contoso.com*"

```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: WebRtcLocalIpsAllowedUrls
  - Valore di esempio:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>*contoso.com*</string>
</array>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### WebRtcLocalhostIpHandling
  #### Limita l'esposizione dell'indirizzo IP locale da WebRTC
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Consente di specificare se WebRTC espone o meno l'indirizzo IP locale dell'utente.

       Se si imposta questo criterio su "Consenti tutte le interfacce" o su "Consenti interfacce pubbliche e private", WebRTC espone l'indirizzo IP locale.

se si impostano i criteri come "Consenti solo interfaccia pubblica" o "Disabilita UDP non trasmesso tramite proxy", WebRTC non esporrà l'indirizzo IP locale.

      Se non si impostano questi criteri o se si disabilitano, WebRTC espone l'indirizzo IP locale.

Mappatura opzioni criteri:

* AllowAllInterfaces (default) = Consenti tutte le interfacce. Viene esposto l'indirizzo IP localhost

* AllowPublicAndPrivateInterfaces (default_public_and_private_interfaces) = Consenti le interfacce pubbliche e private sulla route HTTP predefinita. Viene esposto l'indirizzo IP localhost

* AllowPublicInterfaceOnly (default_public_interface_only) = Consenti interfaccia pubblica sulla route http predefinita. Non viene esposto l'indirizzo IP localhost.

* DisableNonProxiedUdp (disable_non_proxied_udp) = Utilizza TCP a meno che il server proxy non supporti UDP. L'indirizzo IP localhost non viene esposto

Utilizzare le informazioni precedenti durante la configurazione di questo criterio.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: WebRtcLocalhostIpHandling
  - Nome GP: Limita l'esposizione dell'indirizzo IP locale da WebRTC
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: WebRtcLocalhostIpHandling
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"default"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: WebRtcLocalhostIpHandling
  - Valore di esempio:
``` xml
<string>default</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### WebRtcUdpPortRange
  #### Limita l'intervallo di porte UDP locali utilizzato da WebRTC
  
  
  #### Versioni supportate:
  - Su Windows e macOS dal 77 o in seguito

  #### Descrizione
  Limita l'intervallo di porte UDP utilizzato dal WebRTC a un intervallo di porta specificato (inclusi gli endpoint).
Mediante la configurazione di questi criteri, specifichi l'intervallo delle porte UDP locali che WebRTC può utilizzare.

Se non configuri questi criteri o li imposti su una stringa vuota o un intervallo di porte non valido, WebRTC può utilizzare qualsiasi porta UDP locale disponibile.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Stringa

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: WebRtcUdpPortRange
  - Nome GP: Limita l'intervallo di porte UDP locali utilizzato da WebRTC
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: WebRtcUdpPortRange
  - Tipo di valore: REG_SZ
  ##### Valore di esempio:
```
"10000-11999"
```


  #### Informazioni e impostazioni per Mac
  - Nome chiave preferenza: WebRtcUdpPortRange
  - Valore di esempio:
``` xml
<string>10000-11999</string>
```
  

  [Torna all'inizio](#microsoft-edge---criteri)

  ### WinHttpProxyResolverEnabled
  #### Usa resolver proxy di Windows (deprecato)
  >DEPRECAtO: questi criteri sono deprecati. Sono attualmente supportati ma diventeranno obsoleti in una versione futura.
  
  #### Versioni supportate:
  - Su Windows dal 84 o successiva

  #### Descrizione
  Questo criterio è deprecato. Verrà sostituito da una funzionalità simile in un release futuro, vedi https://crbug.com/1032820.

Usa Windows per risolvere i proxy per tutte le reti del browser e non il resolver proxy incorporato in Microsoft Edge. Il resolver proxy di Windows abilita funzionalità proxy di Windows quali DirectAccess/NRPT.

Questo criterio include i problemi descritti da https://crbug.com/644030. Fa sì che i file PAC vengano recuperati ed eseguiti dal codice di Windows, inclusi i file PAC impostati tramite il criterio [ProxyPacUrl](#proxypacurl). Poiché i recuperi di rete per il file PAC si verificano tramite Windows e non tramite il codice Microsoft Edge, i criteri di rete, ad esempio [DnsOverHttpsMode](#dnsoverhttpsmode), non verranno applicati ai recuperi di rete per un file PAC.

   Se abiliti questo criterio, verrà utilizzato il resolver proxy di Windows.

Se disabiliti o non configuri questo criterio, verrà utilizzato il resolver proxy di Microsoft Edge.

  #### Funzionalità supportate:
  - Può essere obbligatorio: Sì
  - Può essere consigliato: No
  - Aggiornamento criteri dinamici: No - Richiede il riavvio del browser

  #### Tipo di dati:
  - Booleano

  #### Informazioni e impostazioni di Windows
  ##### Info su Criteri di gruppo (ADMX)
  - Nome univoco GP: WinHttpProxyResolverEnabled
  - Nome GP: Usa resolver proxy di Windows (deprecato)
  - Percorso GP (Obbligatorio): Modelli amministrativi/Microsoft Edge/
  - Percorso GP (Consigliati): N/D
  - Nome file ADMX GP: MSEdge.admx
  ##### Impostazioni Registro di sistema di Windows
  - Percorso (Obbligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Percorso (Consigliati): N/D
  - Nome valore: WinHttpProxyResolverEnabled
  - Tipo di valore: REG_DWORD
  ##### Valore di esempio:
```
0x00000001
```


  

  [Torna all'inizio](#microsoft-edge---criteri)


## Vedi anche
- [Configurazione di Microsoft Edge in corso](configure-microsoft-edge.md)
- [Pagina di destinazione di Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Blog sulle linee di base di Microsoft Security](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)