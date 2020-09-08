---
title: "Microsoft Edge Browser Policy Documentation"
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 09/07/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom:
description: "Windows and Mac documentation for all policies supported by the Microsoft Edge Browser"
---

# Microsoft Edge – Richtlinien
Die neueste Version von Microsoft Edge umfasst die folgenden Richtlinien. Sie können diese Richtlinien verwenden, um festzulegen, wie Microsoft Edge in Ihrer Organisation ausgeführt wird.

Informationen zu zusätzlichen Richtlinien, mit denen gesteuert wird, wie und wann Microsoft Edge aktualisiert wird, finden Sie hier: [Microsoft Edge Update: Verweis auf Richtlinie](microsoft-edge-update-policies.md).

Sie können die [Kompatibilitäts-Toolkit für Microsoft Security](https://www.microsoft.com/download/details.aspx?id=55319) für die Konfiguration von empfohlenen Grundsicherheitseinstellungen für Microsoft Edge herunterladen. Weitere Informationen hierzu finden Sie unter [Blog zu Microsoft Security-Baselines](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines).

> [!HINWEIS]
> Dieser Artikel gilt für Microsoft Edge, Version 77 oder höher.

## Verfügbare Richtlinien
In diesen Tabellen werden alle browserbezogenen Gruppenrichtlinien aufgelistet, die in dieser Version von Microsoft Edge verfügbar sind. Unter den Links in der Tabelle finden Sie weitere Informationen zu bestimmten Richtlinien.

|||
|-|-|
|[Application Guard-Einstellungen](#application-guard-einstellungen)|[Cast](#cast)|
|[Drucken](#drucken)|[Erweiterungen](#erweiterungen)|
|[HTTP-Authentifizierung](#http-authentifizierung)|[Inhaltseinstellungen](#inhaltseinstellungen)|
|[Kennwort-Manager und -schutz](#kennwort-manager-und--schutz)|[Natives Messaging](#natives-messaging)|
|[Proxyserver](#proxyserver)|[SmartScreen-Einstellungen](#smartscreen-einstellungen)|
|[Standardsuchanbieter](#standardsuchanbieter)|[Start, Startseite und neue Tabseite](#start-startseite-und-neue-tabseite)|
|[Additional](#additional)|

### [*Application Guard-Einstellungen*](#application-guard-einstellungen-policies)
|Richtlinienname|Beschriftung|
|-|-|
|[ApplicationGuardContainerProxy](#applicationguardcontainerproxy)|Containerproxy von Application Guard|
### [*Cast*](#cast-policies)
|Richtlinienname|Beschriftung|
|-|-|
|[EnableMediaRouter](#enablemediarouter)|Google Cast aktivieren|
|[ShowCastIconInToolbar](#showcasticonintoolbar)|Wiedergabesymbol in der Symbolleiste anzeigen|
### [*Drucken*](#drucken-policies)
|Richtlinienname|Beschriftung|
|-|-|
|[DefaultPrinterSelection](#defaultprinterselection)|Standardmäßige Druckerauswahl-Regeln|
|[PrintHeaderFooter](#printheaderfooter)|Kopf- und Fußzeilen drucken|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|Den Systemstandarddrucker als Standarddrucker festlegen|
|[PrintingEnabled](#printingenabled)|Drucken ermöglichen|
|[UseSystemPrintDialog](#usesystemprintdialog)|Über Systemdruckdialogfeld drucken|
### [*Erweiterungen*](#erweiterungen-policies)
|Richtlinienname|Beschriftung|
|-|-|
|[ExtensionAllowedTypes](#extensionallowedtypes)|Zulässige Erweiterungstypen konfigurieren|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|Installation bestimmter Erweiterungen zulassen|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|Steuern, welche Erweiterungen nicht installiert werden können|
|[ExtensionInstallForcelist](#extensioninstallforcelist)|Steuern, welche Erweiterungen automatisch installiert werden|
|[ExtensionInstallSources](#extensioninstallsources)|Erweiterung und Benutzer-Skriptinstallationsquellen konfigurieren|
|[ExtensionSettings](#extensionsettings)|Einstellungen für Erweiterungsverwaltung konfigurieren|
### [*HTTP-Authentifizierung*](#http-authentifizierung-policies)
|Richtlinienname|Beschriftung|
|-|-|
|[AllowCrossOriginAuthPrompt](#allowcrossoriginauthprompt)|Übergreifende HTTP-Basic-Authentifizierungsaufforderungen zulassen|
|[AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)|Gibt eine Liste der Server an, an die Microsoft Edge Anmeldeinformationen von Benutzern delegieren kann|
|[AuthSchemes](#authschemes)|Unterstützte Authentifizierungsschemas|
|[AuthServerAllowlist](#authserverallowlist)|Liste der zugelassenen Authentifizierungsserver konfigurieren|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|CNAME-Lookup beim Aushandeln der Kerberos-Authentifizierung deaktivieren|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|Nicht standardmäßigen Port in Kerberos-SPN einschließen|
|[NtlmV2Enabled](#ntlmv2enabled)|Steuern, ob die NTLMv2-Authentifizierung aktiviert ist|
### [*Inhaltseinstellungen*](#inhaltseinstellungen-policies)
|Richtlinienname|Beschriftung|
|-|-|
|[AutoSelectCertificateForUrls](#autoselectcertificateforurls)|Clientzertifikate für diese Websites automatisch auswählen|
|[CookiesAllowedForUrls](#cookiesallowedforurls)|Cookies auf bestimmten Websites zulassen|
|[CookiesBlockedForUrls](#cookiesblockedforurls)|Cookies auf bestimmten Websites blockieren|
|[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)|Cookies von bestimmten Websites auf die aktuelle Sitzung beschränken|
|[DefaultCookiesSetting](#defaultcookiessetting)|Cookies konfigurieren|
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|Standardeinstellung für Geolocation|
|[DefaultImagesSetting](#defaultimagessetting)|Standardeinstellung für Bilder|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|Nutzung von Ausnahmen für unsicheren Inhalt steuern|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|Standard-JavaScript-Einstellung|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|Standard-Benachrichtigungseinstellung|
|[DefaultPluginsSetting](#defaultpluginssetting)|Standardeinstellung für Adobe Flash|
|[DefaultPopupsSetting](#defaultpopupssetting)|Standardeinstellung für Popupfenster|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|Verwendung der Web-Bluetooth-API steuern|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|Verwendung der WebUSB-API steuern|
|[ImagesAllowedForUrls](#imagesallowedforurls)|Bilder auf diesen Websites zulassen|
|[ImagesBlockedForUrls](#imagesblockedforurls)|Bilder auf bestimmten Websites blockieren|
|[InsecureContentAllowedForUrls](#insecurecontentallowedforurls)|Unsicheren Inhalt auf angegebenen Websites zulassen|
|[InsecureContentBlockedForUrls](#insecurecontentblockedforurls)|Unsicheren Inhalt auf angegebenen Websites blockieren|
|[JavaScriptAllowedForUrls](#javascriptallowedforurls)|JavaScript auf bestimmten Websites zulassen|
|[JavaScriptBlockedForUrls](#javascriptblockedforurls)|JavaScript auf bestimmten Websites blockieren|
|[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)|Einstellung des standardmäßigen Cookieverhaltens für die Vorgängerversion von SameSite|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist)|Auf das Verhalten der Vorgängerversion für SameSite für Cookies auf bestimmten Websites zurücksetzen|
|[NotificationsAllowedForUrls](#notificationsallowedforurls)|Benachrichtigungen auf bestimmten Websites zulassen|
|[NotificationsBlockedForUrls](#notificationsblockedforurls)|Benachrichtigungen auf bestimmten Websites blockieren|
|[PluginsAllowedForUrls](#pluginsallowedforurls)|Adobe Flash-Plug-In auf bestimmten Websites zulassen|
|[PluginsBlockedForUrls](#pluginsblockedforurls)|Adobe Flash-Plug-In auf bestimmten Websites blockieren|
|[PopupsAllowedForUrls](#popupsallowedforurls)|Popupfenster auf bestimmten Websites zulassen|
|[PopupsBlockedForUrls](#popupsblockedforurls)|Popupfenster auf bestimmten Websites blockieren|
|[RegisteredProtocolHandlers](#registeredprotocolhandlers)|Protokollhandler registrieren|
|[SpotlightExperiencesAndRecommendationsEnabled](#spotlightexperiencesandrecommendationsenabled)|Choose whether users can receive customized background images and text, suggestions, notifications,
and tips for Microsoft services|
|[WebUsbAllowDevicesForUrls](#webusballowdevicesforurls)|Gewährt bestimmten Websites Zugriff, damit eine Verbindung mit bestimmten USB-Geräten hergestellt werden kann.|
|[WebUsbAskForUrls](#webusbaskforurls)|WebUSB auf bestimmten Websites zulassen|
|[WebUsbBlockedForUrls](#webusbblockedforurls)|WebUSB auf bestimmten Websites blockieren|
### [*Kennwort-Manager und -schutz*](#kennwort-manager-und--schutz-policies)
|Richtlinienname|Beschriftung|
|-|-|
|[PasswordManagerEnabled](#passwordmanagerenabled)|Speichern von Kennwörtern im Kennwort-Manager ermöglichen|
|[PasswordMonitorAllowed](#passwordmonitorallowed)|Ermöglichen Sie Nutzern, benachrichtigt zu werden, wenn sich herausstellt, dass ihre Kennwörter unsicher sind|
|[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)|URL zum Ändern des Kennworts konfigurieren|
|[PasswordProtectionLoginURLs](#passwordprotectionloginurls)|Liste der Unternehmens-Anmelde-URLs konfigurieren, bei denen der Kennwortschutzdienst zufällig gewählte Zeichenfolgen des Kennworts aufzeichnen soll|
|[PasswordProtectionWarningTrigger](#passwordprotectionwarningtrigger)|Warnungstrigger für Kennwortschutz konfigurieren|
### [*Natives Messaging*](#natives-messaging-policies)
|Richtlinienname|Beschriftung|
|-|-|
|[NativeMessagingAllowlist](#nativemessagingallowlist)|Steuern, welche nativen Messaginghosts von Benutzern verwendet werden können|
|[NativeMessagingBlocklist](#nativemessagingblocklist)|Native Nachrichtensperrliste konfigurieren|
|[NativeMessagingUserLevelHosts](#nativemessaginguserlevelhosts)|Native Messaginghosts auf Benutzerebene zulassen (ohne Administratorberechtigungen installiert)|
### [*Proxyserver*](#proxyserver-policies)
|Richtlinienname|Beschriftung|
|-|-|
|[ProxyBypassList](#proxybypasslist)|Proxy-Umgehungsregeln konfigurieren|
|[ProxyMode](#proxymode)|Proxyservereinstellungen konfigurieren|
|[ProxyPacUrl](#proxypacurl)|Proxy-PAC-Datei-URL festlegen|
|[ProxyServer](#proxyserver)|Adresse oder URL des Proxyservers konfigurieren|
|[ProxySettings](#proxysettings)|Proxyeinstellungen|
### [*SmartScreen-Einstellungen*](#smartscreen-einstellungen-policies)
|Richtlinienname|Beschriftung|
|-|-|
|[PreventSmartScreenPromptOverride](#preventsmartscreenpromptoverride)|Umgehung der Microsoft Defender SmartScreen-Aufforderungen für Websites verhindern|
|[PreventSmartScreenPromptOverrideForFiles](#preventsmartscreenpromptoverrideforfiles)|Umgehung der Microsoft Defender SmartScreen-Warnungen für Downloads verhindern|
|[SmartScreenAllowListDomains](#smartscreenallowlistdomains)|Konfigurieren Sie die Liste der Domänen, für die Microsoft Defender SmartScreen keine Warnungen auslöst.|
|[SmartScreenEnabled](#smartscreenenabled)|Microsoft Defender SmartScreen konfigurieren|
|[SmartScreenForTrustedDownloadsEnabled](#smartscreenfortrusteddownloadsenabled)|Überprüfung von Downloads von vertrauenswürdigen Quellen durch Microsoft Defender SmartScreen erzwingen|
|[SmartScreenPuaEnabled](#smartscreenpuaenabled)|Microsoft Defender SmartScreen konfigurieren, um potenziell unerwünschte Apps zu blockieren|
### [*Standardsuchanbieter*](#standardsuchanbieter-policies)
|Richtlinienname|Beschriftung|
|-|-|
|[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)|Standardsuchanbieter aktivieren|
|[DefaultSearchProviderEncodings](#defaultsearchproviderencodings)|Standardsuchanbieter-Codierungen|
|[DefaultSearchProviderImageURL](#defaultsearchproviderimageurl)|Gibt das Bildsuchfeature für den standardmäßigen Suchanbieter an|
|[DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams)|Parameter für eine Bild-URL, die POST verwendet|
|[DefaultSearchProviderKeyword](#defaultsearchproviderkeyword)|Stichwort für Standardsuchanbieter|
|[DefaultSearchProviderName](#defaultsearchprovidername)|Standardsuchanbietername|
|[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)|Such-URL für den Standardsuchanbieter|
|[DefaultSearchProviderSuggestURL](#defaultsearchprovidersuggesturl)|Standard-Suchanbieter-URL für Vorschläge|
|[NewTabPageSearchBox](#newtabpagesearchbox)|Konfigurieren der Suchfeld-Oberfläche für die neue Registerkartenseite|
### [*Start&comma; Startseite und neue Tabseite*](#start-startseite-und-neue-tabseite-policies)
|Richtlinienname|Beschriftung|
|-|-|
|[HomepageIsNewTabPage](#homepageisnewtabpage)|Neue Tabseite als Startseite festlegen|
|[HomepageLocation](#homepagelocation)|Homepage-URL konfigurieren|
|[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)|Hintergrundtypen konfigurieren, die für das Seitenlayout des neuen Tabs zulässig sind|
|[NewTabPageCompanyLogo](#newtabpagecompanylogo)|Neues Firmenlogo auf der Registerkartenseite festlegen (veraltet)|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|Die Standardwebsites der obersten Ebene auf der neuen Tabseite ausblenden|
|[NewTabPageLocation](#newtabpagelocation)|URL für die neue Tabseite konfigurieren|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|Schnelllinks für neue Tabs festlegen|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|Im Voraus laden der neuen Registerkartenseite für schnelleres Rendern aktivieren|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|Funktion für neue Tabseiten in Microsoft Edge konfigurieren|
|[RestoreOnStartup](#restoreonstartup)|Aktion, die beim Start ausgeführt werden soll|
|[RestoreOnStartupURLs](#restoreonstartupurls)|Websites, die beim Start des Browsers geöffnet werden sollen|
|[ShowHomeButton](#showhomebutton)|Schaltfläche „Startseite“ auf Symbolleiste anzeigen|
### [*Additional*](#additional-policies)
|Richtlinienname|Beschriftung|
|-|-|
|[AddressBarMicrosoftSearchInBingProviderEnabled](#addressbarmicrosoftsearchinbingproviderenabled)|Vorschläge von „Microsoft Search in Bing“ in der Adressleiste aktivieren|
|[AdsSettingForIntrusiveAdsSites](#adssettingforintrusiveadssites)|Anzeigeneinstellung für Websites mit aufdringlichen Anzeigen|
|[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory)|Löschen des Browser- und Downloadverlaufs ermöglichen|
|[AllowFileSelectionDialogs](#allowfileselectiondialogs)|Dateiauswahl-Dialogfelder zulassen|
|[AllowPopupsDuringPageUnload](#allowpopupsduringpageunload)|Erlaubt einer Seite, Popups während des Entladens zu zeigen|
|[AllowSurfGame](#allowsurfgame)|Surf-Spiel zulassen|
|[AllowSyncXHRInPageDismissal](#allowsyncxhrinpagedismissal)|Zulassen, dass Seiten beim Schließen synchrone XHR-Anforderungen senden (veraltet)|
|[AllowTokenBindingForUrls](#allowtokenbindingforurls)|Konfigurieren Sie die Liste der Sites, für die Microsoft Edge versuchen wird, eine Tokenbindung herzustellen.|
|[AllowTrackingForUrls](#allowtrackingforurls)|Konfigurieren von Ausnahmen für die Tracking-Verhinderung für bestimmte Sites|
|[AlternateErrorPagesEnabled](#alternateerrorpagesenabled)|Ähnliche Seiten vorschlagen, wenn eine Webseite nicht gefunden wird|
|[AlwaysOpenPdfExternally](#alwaysopenpdfexternally)|PDF-Dateien immer extern öffnen|
|[AmbientAuthenticationInPrivateModesEnabled](#ambientauthenticationinprivatemodesenabled)|Umgebungsauthentifizierung für InPrivate- und Gastprofile aktivieren|
|[AppCacheForceEnabled](#appcacheforceenabled)|Ermöglichen, dass das AppCache-Feature erneut aktiviert werden kann, auch wenn dieses standardmäßig deaktiviert ist|
|[ApplicationLocaleValue](#applicationlocalevalue)|Anwendungsgebietsschema festlegen|
|[AudioCaptureAllowed](#audiocaptureallowed)|Audioaufnahme zulassen oder blockieren|
|[AudioCaptureAllowedUrls](#audiocaptureallowedurls)|Websites, die auf Audioaufnahmegeräte zugreifen können, ohne eine Berechtigung anzufordern|
|[AudioSandboxEnabled](#audiosandboxenabled)|Ausführung der Audiosandbox zulassen|
|[AutoImportAtFirstRun](#autoimportatfirstrun)|Daten und Einstellungen eines anderen Browsers bei der ersten Ausführung automatisch importieren|
|[AutoLaunchProtocolsFromOrigins](#autolaunchprotocolsfromorigins)|Definieren Sie eine Liste der Protokolle, über die eine externe Anwendung von den aufgeführten Ursprüngen aus ohne Rückfrage beim Benutzer gestartet werden kann.|
|[AutoOpenAllowedForURLs](#autoopenallowedforurls)|URLs, bei denen Richtlinie “AutoOpenFileTypes” gelten kann|
|[AutoOpenFileTypes](#autoopenfiletypes)|Liste der Dateitypen, die nach dem Download automatisch geöffnet werden sollen|
|[AutofillAddressEnabled](#autofilladdressenabled)|AutoAusfüllen für Adressen aktivieren|
|[AutofillCreditCardEnabled](#autofillcreditcardenabled)|AutoAusfüllen für Kreditkarten aktivieren|
|[AutoplayAllowed](#autoplayallowed)|Automatische Medienwiedergabe für Websites zulassen|
|[BackgroundModeEnabled](#backgroundmodeenabled)|Ausführen von Hintergrund-Apps fortsetzen, nachdem Microsoft Edge geschlossen wurde|
|[BackgroundTemplateListUpdatesEnabled](#backgroundtemplatelistupdatesenabled)|Ermöglicht für Sammlungen und andere Features, die Vorlagen verwenden, die Aktualisierung der Liste verfügbarer Vorlagen im Hintergrund.|
|[BingAdsSuppression](#bingadssuppression)|Alle Werbeanzeigen in Bing-Suchergebnissen blockieren|
|[BlockThirdPartyCookies](#blockthirdpartycookies)|Cookies von Drittanbietern blockieren|
|[BrowserAddProfileEnabled](#browseraddprofileenabled)|Profilerstellung über das Flyout-Menü „Identität” oder die Seite „Einstellungen” aktivieren|
|[BrowserGuestModeEnabled](#browserguestmodeenabled)|Gastmodus aktivieren|
|[BrowserNetworkTimeQueriesEnabled](#browsernetworktimequeriesenabled)|Abfragen bei einem Browser-Netzwerk-Zeitdienst zulassen|
|[BrowserSignin](#browsersignin)|Browser-Anmeldeeinstellungen|
|[BuiltInDnsClientEnabled](#builtindnsclientenabled)|Integrierten DNS-Client verwenden|
|[BuiltinCertificateVerifierEnabled](#builtincertificateverifierenabled)|Ermittelt, ob die integrierte Zertifikatsprüfung zum Bestätigen von Serverzertifikaten verwendet wird. (veraltet)|
|[CertificateTransparencyEnforcementDisabledForCas](#certificatetransparencyenforcementdisabledforcas)|Erzwingung der Zertifikattransparenz für eine Liste von subjectPublicKeyInfo-Hashes deaktivieren|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](#certificatetransparencyenforcementdisabledforlegacycas)|Erzwingung der Zertifikattransparenz für eine Liste der Legacy-Zertifizierungsstellen deaktivieren|
|[CertificateTransparencyEnforcementDisabledForUrls](#certificatetransparencyenforcementdisabledforurls)|Erzwingung der Zertifikattransparenz für bestimmte URLs deaktivieren|
|[ClearBrowsingDataOnExit](#clearbrowsingdataonexit)|Browserdaten löschen, wenn Microsoft Edge geschlossen wird|
|[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)|Löschen von zwischengespeicherten Bildern und Dateien nach dem Schließen von Microsoft Edge|
|[ClickOnceEnabled](#clickonceenabled)|Benutzern das Öffnen von Dateien unter Verwendung des ClickOnce-Protokolls ermöglichen|
|[CollectionsServicesAndExportsBlockList](#collectionsservicesandexportsblocklist)|Zugriff auf eine angegebene Liste von Diensten blockieren und Ziele in Sammlungen exportieren|
|[CommandLineFlagSecurityWarningsEnabled](#commandlineflagsecuritywarningsenabled)|Aktivieren von Sicherheitswarnungen für Befehlszeilenflags|
|[ComponentUpdatesEnabled](#componentupdatesenabled)|Komponentenupdates in Microsoft Edge aktivieren|
|[ConfigureDoNotTrack](#configuredonottrack)|Nicht verfolgen (Do not track) konfigurieren|
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|Automatische Anmeldung mit einem Active Directory-Domänenkonto konfigurieren, wenn kein Azure AD-Domänenkonto vorhanden ist|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|Online-Text-zu-Sprache konfigurieren|
|[ConfigureShare](#configureshare)|Freigabefunktion konfigurieren|
|[CustomHelpLink](#customhelplink)|Benutzerdefinierten Hilfelink angeben|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|Überprüfungen auf DNS-Abfangvorgänge aktiviert|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|Microsoft Edge als Standardbrowser festlegen|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|Standardsuchanbieter Zugriff auf die Suche im Kontextmenü gestatten|
|[DefaultSensorsSetting](#defaultsensorssetting)|Default sensors setting|
|[DefaultSerialGuardSetting](#defaultserialguardsetting)|Verwendung der API für den seriellen Anschluss steuern|
|[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)|Voraussetzen, dass die Website-Liste zum Unternehmensmodus vor der Registerkartennavigation verfügbar ist|
|[DeleteDataOnMigration](#deletedataonmigration)|Alte Browserdaten bei der Migration löschen|
|[DeveloperToolsAvailability](#developertoolsavailability)|Steuern, wo Entwicklungstools verwendet werden können|
|[DiagnosticData](#diagnosticdata)|Erforderliche und optionale Diagnosedaten über die Browsernutzung senden|
|[DirectInvokeEnabled](#directinvokeenabled)|Benutzern das Öffnen von Dateien unter Verwendung des DirectInvoke-Protokolls ermöglichen|
|[Disable3DAPIs](#disable3dapis)|Unterstützung für 3D-Grafik-APIs deaktivieren|
|[DisableScreenshots](#disablescreenshots)|Aufnahme von Screenshots deaktivieren|
|[DiskCacheDir](#diskcachedir)|Verzeichnis für Datenträgercache festlegen|
|[DiskCacheSize](#diskcachesize)|Größe des Datenträgercaches festlegen (in Bytes)|
|[DnsOverHttpsMode](#dnsoverhttpsmode)|Den Modus von DNS-over-HTTPS steuern|
|[DnsOverHttpsTemplates](#dnsoverhttpstemplates)|URI-Vorlage der gewünschten DNS-über-HTTPS-Auflösung angeben|
|[DownloadDirectory](#downloaddirectory)|Downloadverzeichnis festlegen|
|[DownloadRestrictions](#downloadrestrictions)|Download-Einschränkungen zulassen|
|[EdgeCollectionsEnabled](#edgecollectionsenabled)|Aktivieren der Sammlungsfunktion|
|[EditFavoritesEnabled](#editfavoritesenabled)|Ermöglicht Benutzern das Bearbeiten von Favoriten.|
|[EnableDeprecatedWebPlatformFeatures](#enabledeprecatedwebplatformfeatures)|Veraltete Webplattformfeatures vorübergehend wieder aktivieren|
|[EnableDomainActionsDownload](#enabledomainactionsdownload)|Herunterladen von Domänenaktionen von Microsoft aktivieren (veraltet)|
|[EnableOnlineRevocationChecks](#enableonlinerevocationchecks)|Onlineprüfungen für OCSP/Sperrlisten aktivieren|
|[EnableSha1ForLocalAnchors](#enablesha1forlocalanchors)|Mit SHA-1 signierte Zertifikate zulassen, wenn sie von lokalen Vertrauensanker ausgestellt worden sind. (veraltet)|
|[EnterpriseHardwarePlatformAPIEnabled](#enterprisehardwareplatformapienabled)|Ermöglichen der Verwendung der Enterprise Hardware Platform-API durch verwaltete Erweiterungen|
|[EnterpriseModeSiteListManagerAllowed](#enterprisemodesitelistmanagerallowed)|Zugriff auf das Tool “Enterprise Mode Site List Manager” zulassen|
|[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](#exemptdomainfiletypepairsfromfiletypedownloadwarnings)|Download der auf Dateityperweiterungen basierenden Warnungen für angegebene Dateitypen in Domänen deaktivieren|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|Steuern der Kommunikation mit dem Experimentier- und Konfigurationsdienst|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox)|Kontrollkästchen „Immer geöffnet“ im Dialogfeld für externe Protokolle anzeigen|
|[FamilySafetySettingsEnabled](#familysafetysettingsenabled)|Zulassen, dass Benutzer Family Safety konfigurieren|
|[FavoritesBarEnabled](#favoritesbarenabled)|Favoritenleiste aktivieren|
|[ForceBingSafeSearch](#forcebingsafesearch)|Bing SafeSearch erzwingen|
|[ForceCertificatePromptsOnMultipleMatches](#forcecertificatepromptsonmultiplematches)|Konfigurieren Sie, ob Microsoft Edge automatisch ein Zertifikat auswählen sollte, wenn mehrere Zertifikat Übereinstimmungen für eine Website vorhanden sind, die mit "AutoSelectCertificateForUrls" konfiguriert ist.|
|[ForceEphemeralProfiles](#forceephemeralprofiles)|Verwendung von kurzlebigen Profilen aktivieren|
|[ForceGoogleSafeSearch](#forcegooglesafesearch)|Google SafeSearch erzwingen|
|[ForceLegacyDefaultReferrerPolicy](#forcelegacydefaultreferrerpolicy)|Verwenden Sie eine Referrer-Standardrichtlinie vom Typ „no-referrer-when-downgrade“ (veraltet)|
|[ForceNetworkInProcess](#forcenetworkinprocess)|Ausführung von Netzwerkcode im Browserprozess erzwingen (veraltet)|
|[ForceSync](#forcesync)|Force synchronization of browser data and do not show the sync consent prompt|
|[ForceYouTubeRestrict](#forceyoutuberestrict)|Minimalen eingeschränkten Modus für YouTube erzwingen|
|[FullscreenAllowed](#fullscreenallowed)|Vollbildmodus zulassen|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|Globalen bereichsbezogenen HTTP-Authentifizierungscache aktivieren|
|[GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar)|Direkte Intranetsitenavigation erzwingen anstatt in der Adressleiste nach einzelnen Worteinträgen zu suchen|
|[HSTSPolicyBypassList](#hstspolicybypasslist)|Konfigurieren der Liste mit Namen, die die HSTS-Richtlinienprüfung umgehen|
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|Hardwarebeschleunigung verwenden (sofern verfügbar)|
|[HideFirstRunExperience](#hidefirstrunexperience)|„Eindruck beim ersten Ausführen“ und Begrüßungsbildschirm ausblenden|
|[ImportAutofillFormData](#importautofillformdata)|Importieren von AutoAusfüllen-Formulardaten zulassen|
|[ImportBrowserSettings](#importbrowsersettings)|Importieren von Browsereinstellungen zulassen|
|[ImportCookies](#importcookies)|Importieren von Cookies zulassen|
|[ImportExtensions](#importextensions)|Importieren von Erweiterungen zulassen|
|[ImportFavorites](#importfavorites)|Importieren von Favoriten zulassen|
|[ImportHistory](#importhistory)|Importieren des Browserverlaufs zulassen|
|[ImportHomepage](#importhomepage)|Importieren von Startseiteneinstellungen zulassen|
|[ImportOpenTabs](#importopentabs)|Importieren offener Tabs zulassen|
|[ImportPaymentInfo](#importpaymentinfo)|Import von Zahlungsinformationen zulassen|
|[ImportSavedPasswords](#importsavedpasswords)|Importieren gespeicherter Kennwörter zulassen|
|[ImportSearchEngine](#importsearchengine)|Importieren von Suchmaschineneinstellungen zulassen|
|[ImportShortcuts](#importshortcuts)|Importieren von Tastenkombinationen zulassen|
|[InPrivateModeAvailability](#inprivatemodeavailability)|Verfügbarkeit des InPrivate-Modus konfigurieren|
|[InsecureFormsWarningsEnabled](#insecureformswarningsenabled)|Warnungen für unsichere Formulare aktivieren|
|[IntensiveWakeUpThrottlingEnabled](#intensivewakeupthrottlingenabled)|Steuern des Features “IntensiveWakeUpThrottling”|
|[InternetExplorerIntegrationEnhancedHangDetection](#internetexplorerintegrationenhancedhangdetection)|Konfigurieren der erweiterten Erkennung hängender Webseiten für den Internet Explorer-Modus|
|[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)|Internet Explorer-Integration konfigurieren|
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|Enterprise Mode Site List konfigurieren|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|Angeben des Verhaltens von seiteninternen Navigationsvorgängen zu nicht konfigurierten Websites, wenn diese über Seiten im Internet Explorer-Modus gestartet werden|
|[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed)|Allow Internet Explorer mode testing|
|[IsolateOrigins](#isolateorigins)|Websiteisolation für bestimmte Ursprünge aktivieren|
|[LocalProvidersEnabled](#localprovidersenabled)|Vorschläge von lokalen Anbietern zulassen|
|[ManagedFavorites](#managedfavorites)|Favoriten konfigurieren|
|[ManagedSearchEngines](#managedsearchengines)|Suchmaschinen verwalten|
|[MaxConnectionsPerProxy](#maxconnectionsperproxy)|Maximale Anzahl gleichzeitiger Verbindungen mit dem Proxyserver|
|[MediaRouterCastAllowAllIPs](#mediaroutercastallowallips)|Google Cast erlauben, eine Verbindung mit CAST-Geräten auf allen IP-Adressen herzustellen|
|[MetricsReportingEnabled](#metricsreportingenabled)|Meldung von nutzungs- und absturzbezogenen Daten aktivieren (veraltet)|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|Aktivieren Sie die ursprüngliche Fensterschließung|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|Festlegen eines Timeouts für die Verzögerung der Registerkartennavigation für die Website-Liste zum Unternehmensmodus|
|[NetworkPredictionOptions](#networkpredictionoptions)|Netzwerkvorhersage aktivieren|
|[NonRemovableProfileEnabled](#nonremovableprofileenabled)|Konfigurieren, ob für einen Benutzer beim Anmelden mit dem Geschäfts-, Schul-oder Unikonto immer automatisch ein Standardprofil vorhanden ist.|
|[OverrideSecurityRestrictionsOnInsecureOrigin](#overridesecurityrestrictionsoninsecureorigin)|Steuert, wo Sicherheitseinschränkungen für unsichere Ursprünge gelten|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|Abfragemöglichkeiten für verfügbare Zahlungsmethoden durch Websites zulassen|
|[PersonalizationReportingEnabled](#personalizationreportingenabled)|Personalisierung von Anzeigen, Suche und News zulassen, indem Sie den Browserverlauf an Microsoft senden|
|[PinningWizardAllowed](#pinningwizardallowed)|Assistent für das Anheften an die Taskleiste zulassen|
|[ProactiveAuthEnabled](#proactiveauthenabled)|Proaktive Authentifizierung aktivieren|
|[PromotionalTabsEnabled](#promotionaltabsenabled)|Tabfüllende Werbeinhalte ermöglichen|
|[PromptForDownloadLocation](#promptfordownloadlocation)|Fragen, wo heruntergeladene Dateien gespeichert werden sollen|
|[QuicAllowed](#quicallowed)|QUIC-Protokoll zulassen|
|[RelaunchNotification](#relaunchnotification)|Einen Benutzer benachrichtigen, dass ein Neustart des Browsers für ausstehende Updates empfohlen wird oder erforderlich ist|
|[RelaunchNotificationPeriod](#relaunchnotificationperiod)|Zeitraum für Aktualisierungsbenachrichtigungen festlegen|
|[RendererCodeIntegrityEnabled](#renderercodeintegrityenabled)|Renderercodeintegrität aktivieren|
|[RequireOnlineRevocationChecksForLocalAnchors](#requireonlinerevocationchecksforlocalanchors)|Geben Sie an, ob für lokale Vertrauensanker Online-OCSP/CRL-Überprüfungen erforderlich sind.|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|Auflösung von Navigationsfehlern mithilfe eines Webdienstes aktivieren|
|[RestrictSigninToPattern](#restrictsignintopattern)|Beschränken der Konten, die als primäre Microsoft Edge-Konten verwendet werden können|
|[RoamingProfileLocation](#roamingprofilelocation)|Roamingprofilverzeichnis festlegen|
|[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)|Verwendung von Roamingkopien für Microsoft Edge-Profildaten ermöglichen|
|[RunAllFlashInAllowMode](#runallflashinallowmode)|Adobe Flash-Inhaltseinstellung auf alle Inhalte erweitern|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|Zulassen, dass Benutzer von der HTTPS-Warnungsseite aus fortfahren können|
|[SSLVersionMin](#sslversionmin)|Mindestversion von TLS aktiviert|
|[SaveCookiesOnExit](#savecookiesonexit)|Speichern von Cookies beim Schließen von Microsoft Edge|
|[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)|Speichern des Browserverlaufs deaktivieren|
|[ScreenCaptureAllowed](#screencaptureallowed)|Screenshots zulassen oder verweigern|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|Scrollen zu dem in URL-Fragmenten angegebenen Text aktivieren|
|[SearchSuggestEnabled](#searchsuggestenabled)|Suchvorschläge aktivieren|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|Websites oder Domänen, die keine Berechtigung zur Verwendung des direkten Sicherheitsschlüssel-Nachweises benötigen|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|Alle Intranetsites an Internet Explorer senden|
|[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)|Websiteinformationen zur Verbesserung von Microsoft-Diensten senden (veraltet)|
|[SensorsAllowedForUrls](#sensorsallowedforurls)|Zugriff auf Sensoren auf bestimmten Websites zulassen|
|[SensorsBlockedForUrls](#sensorsblockedforurls)|Zugriff auf Sensoren auf bestimmten Websites blockieren|
|[SerialAskForUrls](#serialaskforurls)|Die serielle API auf bestimmten Websites zulassen|
|[SerialBlockedForUrls](#serialblockedforurls)|Die serielle API auf bestimmten Websites blockieren|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|Microsoft Office-Verknüpfung in der Favoritenleiste anzeigen|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|Unterstützung des signierten HTTP-Austauschs (SXG) aktivieren|
|[SitePerProcess](#siteperprocess)|Websiteisolation für jede Website aktivieren|
|[SpellcheckEnabled](#spellcheckenabled)|Rechtschreibprüfung aktivieren|
|[SpellcheckLanguage](#spellchecklanguage)|Spezifische Sprachen für die Rechtschreibprüfung aktivieren|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|Deaktivierung von Sprachen für die Rechtschreibprüfung erzwingen|
|[StricterMixedContentTreatmentEnabled](#strictermixedcontenttreatmentenabled)|Strengere Behandlung für gemischte Inhalte aktivieren (veraltet)|
|[SuppressUnsupportedOSWarning](#suppressunsupportedoswarning)|Nicht unterstützte Betriebssystemwarnung unterdrücken|
|[SyncDisabled](#syncdisabled)|Synchronisierung von Daten mit Microsoft-Synchronisierungsdiensten deaktivieren|
|[SyncTypesListDisabled](#synctypeslistdisabled)|Konfigurieren der Liste der Typen, die von der Synchronisierung ausgeschlossen werden sollen|
|[TLS13HardeningForLocalAnchorsEnabled](#tls13hardeningforlocalanchorsenabled)|Aktivieren Sie ein TLS 1.3-Sicherheitsfeature für lokale Vertrauensanker. (veraltet)|
|[TLSCipherSuiteDenyList](#tlsciphersuitedenylist)|Geben Sie die zu deaktivierenden TLS-Verschlüsselungssuites an|
|[TabFreezingEnabled](#tabfreezingenabled)|Einfrieren von Hintergrundtabs zulassen|
|[TaskManagerEndProcessEnabled](#taskmanagerendprocessenabled)|Beenden von Prozessen im Browser-Task-Manager ermöglichen|
|[TotalMemoryLimitMb](#totalmemorylimitmb)|Dient zum Festlegen des Limits für den Arbeitsspeicher, der von einer einzelnen Microsoft Edge-Instanz beansprucht werden kann (in MB).|
|[TrackingPrevention](#trackingprevention)|Blockieren der Nachverfolgung der Webbrowsing-Aktivitäten von Benutzern|
|[TranslateEnabled](#translateenabled)|Übersetzung aktivieren|
|[URLAllowlist](#urlallowlist)|Liste zulässiger URLs definieren|
|[URLBlocklist](#urlblocklist)|Zugriff auf eine Liste von URLs blockieren|
|[UserAgentClientHintsEnabled](#useragentclienthintsenabled)|Aktivieren des Features “Client Hints des Benutzer-Agenten” (veraltet)|
|[UserDataDir](#userdatadir)|Benutzerdatenverzeichnis festlegen|
|[UserDataSnapshotRetentionLimit](#userdatasnapshotretentionlimit)|Beschränkt die Anzahl Momentaufnahmen von Benutzerdaten, die für den Fall eines Notfallrollbacks aufbewahrt werden.|
|[UserFeedbackAllowed](#userfeedbackallowed)|Benutzerfeedback zulassen|
|[VideoCaptureAllowed](#videocaptureallowed)|Videoaufnahme zulassen oder blockieren|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|Websites, die auf Videoaufnahmegeräte zugreifen können, ohne eine Berechtigung anzufordern|
|[WPADQuickCheckEnabled](#wpadquickcheckenabled)|WPAD-Optimierung festlegen|
|[WebAppInstallForceList](#webappinstallforcelist)|Liste der Web-Apps, deren Installation erzwungen wurde, konfigurieren|
|[WebComponentsV0Enabled](#webcomponentsv0enabled)|Aktivieren Sie die v0-API der Webkomponenten bis M84 erneut (veraltet)|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|Zulassen, dass WebDriver inkompatible Richtlinien außer Kraft setzt (veraltet)|
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|Verfügbarmachung von lokalen IP-Adressen durch WebRTC verwalten|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|Verfügbarmachung der lokalen IP-Adresse durch WebRTC beschränken|
|[WebRtcUdpPortRange](#webrtcudpportrange)|Bereich der lokalen, von WebRTC verwendeten UDP-Ports einschränken|
|[WinHttpProxyResolverEnabled](#winhttpproxyresolverenabled)|Verwenden von Windows-Proxy-Konfliktlöser (veraltet)|




  ## Application Guard-Einstellungen policies

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ApplicationGuardContainerProxy
  #### Containerproxy von Application Guard
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 84 oder höher

  #### Beschreibung
  Diese Richtlinie konfiguriert die Proxyeinstellungen für Microsoft Edge Application Guard.
Wenn Sie diese Richtlinie aktivieren, ignoriert Microsoft Edge Application Guard andere Proxykonfigurationen.

Wenn Sie diese Richtlinie nicht konfigurieren, verwendet Microsoft Edge Application Guard die Proxykonfiguration des Hosts.

Diese Richtlinie wirkt sich nicht auf die Proxykonfiguration von Microsoft Edge außerhalb von Application Guard (auf dem Host) aus.

Im ProxyMode-Feld können Sie den von Microsoft Edge Application Guard verwendeten Proxyserver angeben.

Das ProxyPacUrl-Feld ist eine URL zu einer .pac-Proxydatei.

Das ProxyServer-Feld ist eine URL für den Proxyserver.

Wenn Sie den Wert "Direct" für [ProxyMode](#proxymode) auswählen, werden alle anderen Felder ignoriert.

Wenn Sie den Wert "auto_detect" für [ProxyMode](#proxymode) auswählen, werden alle anderen Felder ignoriert.

Wenn Sie den Wert "fixed_servers" für [ProxyMode](#proxymode) auswählen, wird das Feld [ProxyServer](#proxyserver) verwendet.

Wenn Sie den Wert "pac_script" für [ProxyMode](#proxymode) auswählen, wird das Feld [ProxyPacUrl](#proxypacurl) verwendet.

         Weitere Informationen zum Identifizieren von Application Guard-Datenverkehr mithilfe dualer Proxyx finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2134653](https://go.microsoft.com/fwlink/?linkid=2134653).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Wörterbuch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ApplicationGuardContainerProxy
  - Gruppenrichtlinienname: Containerproxy von Application Guard
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Application Guard-Einstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ApplicationGuardContainerProxy
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ## Cast policies

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### EnableMediaRouter
  #### Google Cast aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Aktivieren Sie diese Richtlinie, um Google Cast zu aktivieren. Benutzer können es dann über das App-Menü, über Seitenkontextmenüs, Mediensteuerungen auf Cast-fähigen Websites und (falls angezeigt) über das Cast-Symbolleistensymbol starten.

Deaktivieren Sie diese Richtlinie, um Google Cast zu deaktivieren.

Google Cast ist standardmäßig aktiviert.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: EnableMediaRouter
  - Gruppenrichtlinienname: Google Cast aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Cast
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: EnableMediaRouter
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: EnableMediaRouter
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ShowCastIconInToolbar
  #### Wiedergabesymbol in der Symbolleiste anzeigen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Legen Sie diese Richtlinie auf true fest, um das Symbol der Cast-Symbolleiste in der Symbolleiste oder im Überlaufmenü anzuzeigen. Benutzer können es nicht entfernen.

Wenn Sie diese Richtlinie nicht konfigurieren oder deaktivieren, können Benutzer das Symbol über das Kontextmenü anheften oder entfernen.

Diese Richtlinie wird ignoriert und das Symbol wird in der Symbolleiste nicht angezeigt, wenn Sie auch die Richtlinie [EnableMediaRouter](#enablemediarouter) auf false festgelegt haben.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ShowCastIconInToolbar
  - Gruppenrichtlinienname: Wiedergabesymbol in der Symbolleiste anzeigen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Cast
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ShowCastIconInToolbar
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ShowCastIconInToolbar
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ## Drucken policies

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultPrinterSelection
  #### Standardmäßige Druckerauswahl-Regeln
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Überschreibt die Regeln für die Wahl des Standarddruckers von Microsoft Edge. Diese Richtlinie bestimmt die Regeln für die Wahl des Standarddruckers in Microsoft Edge, wenn ein Benutzer erstmals eine Seite drucken möchte.

Wenn diese Richtlinie festgelegt ist, versucht Microsoft Edge, einen Drucker zu finden, der über alle angegebenen Attribute verfügt, und verwendet diesen als Standarddrucker. Sollten die Kriterien von mehreren Druckern erfüllt werden, wird der erste passende Drucker verwendet.

Wenn Sie diese Richtlinie nicht konfigurieren oder bis zum Timeout keine passenden Drucker gefunden werden, wird als Standarddrucker entweder der integrierte PDF-Drucker (sofern vorhanden) oder kein Drucker verwendet.

Der Wert wird als JSON-Objekt nach dem folgenden Schema analysiert: { "type": "object", "properties": { "idPattern": { "description": "Regular expression to match printer id.", "type": "string" }, "namePattern": { "description": "Regular expression to match printer display name.", "type": "string" } } }

Wird ein Feld ausgelassen, bedeutet das, dass alle Werte geeignet sind. Wenn Sie also beispielsweise keine Konnektivität angeben, sucht die Druckvorschau nach allen Arten von lokalen Druckern. Muster für reguläre Ausdrücke müssen der JavaScript-RegExp-Syntax entsprechen, und beim Abgleich wird die Groß-/Kleinschreibung berücksichtigt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultPrinterSelection
  - Gruppenrichtlinienname: Standardmäßige Druckerauswahl-Regeln
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Drucken
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DefaultPrinterSelection
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"{ \"idPattern\": \".*public\", \"namePattern\": \".*Color\" }"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultPrinterSelection
  - Beispielwert:
``` xml
<string>{ "idPattern": ".*public", "namePattern": ".*Color" }</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PrintHeaderFooter
  #### Kopf- und Fußzeilen drucken
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Erzwingt die Aktivierung oder Deaktivierung von Kopf- und Fußzeilen im Druckdialogfeld.

Wenn Sie diese Richtlinie nicht konfigurieren, kann der Benutzer entscheiden, ob Kopf- und Fußzeilen gedruckt werden sollen.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer keine Kopf- und Fußzeilen drucken.

Wenn Sie diese Richtlinie aktivieren, werden Kopf- und Fußzeilen immer gedruckt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PrintHeaderFooter
  - Gruppenrichtlinienname: Kopf- und Fußzeilen drucken
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Drucken
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Drucken
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: PrintHeaderFooter
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: PrintHeaderFooter
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PrintPreviewUseSystemDefaultPrinter
  #### Den Systemstandarddrucker als Standarddrucker festlegen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Weist Microsoft Edge an, den Standarddrucker des Systems anstelle des zuletzt verwendeten Druckers als Standardoption in der Seitenansicht zu verwenden.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird in der Seitenansicht der zuletzt verwendete Drucker als Standardziel ausgewählt.

Wenn Sie diese Richtlinie aktivieren, verwendet die Seitenansicht den Standarddrucker des Betriebssystems als Standardziel.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PrintPreviewUseSystemDefaultPrinter
  - Gruppenrichtlinienname: Den Systemstandarddrucker als Standarddrucker festlegen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Drucken
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Drucken
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: PrintPreviewUseSystemDefaultPrinter
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: PrintPreviewUseSystemDefaultPrinter
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PrintingEnabled
  #### Drucken ermöglichen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Ermöglicht das Drucken in Microsoft Edge und verhindert, dass Benutzer diese Einstellung ändern.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer drucken.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer in Microsoft Edge nicht drucken. Das Drucken wird unter anderem im Schraubenschlüsselmenü, in Erweiterungen und in JavaScript-Anwendungen deaktiviert. Benutzer können weiterhin über Plug-Ins drucken, die Microsoft Edge beim Drucken umgehen. So verfügen beispielsweise bestimmte Adobe Flash-Anwendungen über eine Druckoption in ihrem Kontextmenü, was von dieser Richtlinie nicht abgedeckt wird.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PrintingEnabled
  - Gruppenrichtlinienname: Drucken ermöglichen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Drucken
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: PrintingEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: PrintingEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### UseSystemPrintDialog
  #### Über Systemdruckdialogfeld drucken
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Zeigt das Systemdruckdialogfeld anstelle der Druckvorschau an.

Wenn Sie diese Richtlinie aktivieren, öffnet Microsoft Edge das Systemdruckdialogfeld anstelle der integrierten Druckvorschau, wenn ein Benutzer eine Seite druckt.

Falls Sie diese Richtlinie nicht konfigurieren oder deaktivieren, lösen Druckbefehle den Druckvorschaubildschirm von Microsoft Edge aus.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: UseSystemPrintDialog
  - Gruppenrichtlinienname: Über Systemdruckdialogfeld drucken
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Drucken
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: UseSystemPrintDialog
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: UseSystemPrintDialog
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ## Erweiterungen policies

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ExtensionAllowedTypes
  #### Zulässige Erweiterungstypen konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Steuert, welche Erweiterungstypen installiert werden können, und begrenzt den Laufzeitzugriff.

Diese Einstellung definiert die zulässigen Arten von Erweiterungen und mit welchen Hosts sie interagieren können. Der Wert ist eine Liste dieser Zeichenfolgen: "extension", "theme", "user_script", and "hosted_app". Weitere Informationen zu diesen Typen finden Sie in der Dokumentation zu Microsoft Edge-Erweiterungen.

Beachten Sie, dass diese Richtlinie auch Erweiterungen betrifft, die mit [ExtensionInstallForcelist](#extensioninstallforcelist) zwangsinstalliert werden sollen.

Wenn Sie diese Richtlinie aktivieren, werden nur Erweiterungen installiert, die einem Typ in der Liste entsprechen.

Wenn Sie diese Richtlinie nicht konfigurieren, werden keine Einschränkungen für die zulässigen Erweiterungstypen erzwungen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ExtensionAllowedTypes
  - Gruppenrichtlinienname: Zulässige Erweiterungstypen konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Erweiterungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes\1 = "hosted_app"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ExtensionAllowedTypes
  - Beispielwert:
``` xml
<array>
  <string>hosted_app</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ExtensionInstallAllowlist
  #### Installation bestimmter Erweiterungen zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Standardmäßig sind alle Erweiterungen zugelassen. Wenn Sie jedoch alle Erweiterungen blockieren, indem Sie die Richtlinie "ExtensionInstallBlockList" auf "*" festlegen, können Benutzer nur Erweiterungen installieren, die in dieser Richtlinie definiert sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ExtensionInstallAllowlist
  - Gruppenrichtlinienname: Installation bestimmter Erweiterungen zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Erweiterungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\2 = "extension_id2"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ExtensionInstallAllowlist
  - Beispielwert:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ExtensionInstallBlocklist
  #### Steuern, welche Erweiterungen nicht installiert werden können
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Listet bestimmte Erweiterungen auf, die Benutzer NICHT in Microsoft Edge installieren können. Wenn Sie diese Richtlinie bereitstellen, werden sämtliche zuvor installierten Erweiterungen aus dieser Liste deaktiviert und können vom Benutzer nicht mehr aktiviert werden. Wenn Sie ein Element aus der Liste blockierter Erweiterungen entfernen, wird die entsprechende Erweiterung automatisch überall reaktiviert, wo sie zuvor installiert war.

Mit „*“ können Sie alle Erweiterungen blockieren, die nicht explizit in der Liste „Zulassen“ angegeben sind.

Wenn Sie diese Richtlinie nicht konfigurieren, können Benutzer beliebige Erweiterungen in Microsoft Edge installieren.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ExtensionInstallBlocklist
  - Gruppenrichtlinienname: Steuern, welche Erweiterungen nicht installiert werden können
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Erweiterungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\2 = "extension_id2"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ExtensionInstallBlocklist
  - Beispielwert:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ExtensionInstallForcelist
  #### Steuern, welche Erweiterungen automatisch installiert werden
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt Erweiterungen an, die ohne Benutzereingriff im Hintergrund installiert werden und die Benutzer nicht deinstallieren oder deaktivieren können ("Erzwungene Installation"). Alle von den Erweiterungen angeforderten Berechtigungen werden ohne Benutzereingriff implizit gewährt, einschließlich zusätzlicher Berechtigungen, die von zukünftigen Versionen der Erweiterung angefordert werden. Außerdem werden Berechtigungen für die enterprise.deviceAttributes- und enterprise.platformKeys-Erweiterungs-APIs gewährt. (Diese beiden APIs sind nur für Erweiterungen verfügbar, deren Installation erzwungen wurde.)

Diese Richtlinie hat Vorrang vor einer potenziell in Konflikt stehenden [ExtensionInstallBlocklist](#extensioninstallblocklist)-Richtlinie. Wenn Sie eine Erweiterung aus der Liste mit erzwungener Installation herausnehmen, wird sie automatisch von Microsoft Edge deinstalliert.

  Die erzwungene Installation ist auf Apps und Erweiterungen beschränkt, die auf der Microsoft Edge-Seite für Add-ons aufgelistet sind und nicht zu folgendem gehören: Windows-Instanzen, die mit einer Microsoft Active Directory-Domäne verbunden sind, oder Instanzen von Windows 10 Pro oder Enterprise, die für die Geräteverwaltung registriert sind, sowie Instanzen von macOS, die über MDM verwaltet werden oder über MCX mit einer Domäne verbunden sind.

  Beachten Sie, dass Benutzer den Quellcode einer beliebigen Erweiterung mithilfe von Entwicklertools ändern können, wodurch die Erweiterung möglicherweise nicht funktionsfähig ist. Wenn dies ein Problem ist, legen Sie die [DeveloperToolsAvailability](#developertoolsavailability)-Richtlinie fest.

  Verwenden Sie das folgende Format, um der Liste eine Erweiterung hinzuzufügen:

[extensionID];[updateURL]

– extensionID: Zeichenfolge mit 32 Zeichen, die im Entwicklermodus unter edge://extensions gefunden wurde.

  – updateURL (optional) ist die Adresse des XML-Dokuments zum Aktualisieren des Manifests für die App oder Erweiterung, wie unter [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043) beschrieben. Wenn Sie eine Erweiterung aus dem Chrome Web Store installieren möchten, stellen Sie die Chrome Web Store Update-URL bereit (https://clients2.google.com/service/update2/crx). Beachten Sie, dass die in dieser Richtlinie festgelegte Update-URL nur für die Erstinstallation verwendet wird. Wenn Sie die Update-URL nicht festlegen, wird davon ausgegangen, dass die Erweiterung im Microsoft Store gehostet ist und die folgende Update-URL verwendet: https://edge.microsoft.com/extensionwebstorebase/v1/crx.

  Beispiel: gggmmkjegpiggikcnhidnjjhmicpibll;https://edge.microsoft.com/extensionwebstorebase/v1/crx installiert die Microsoft Online-App unter der Microsoft Store-Update-URL. Weitere Informationen zum Hosten von Erweiterungen finden Sie unter: [https://go.microsoft.com/fwlink/?linkid=2095044](https://go.microsoft.com/fwlink/?linkid=2095044).

Wenn Sie diese Richtlinie nicht konfigurieren, werden keine Erweiterungen automatisch installiert, und Benutzer können alle Erweiterungen in Microsoft Edge deinstallieren.

  Beachten Sie, dass diese Richtlinie nicht für den InPrivate-Modus gilt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ExtensionInstallForcelist
  - Gruppenrichtlinienname: Steuern, welche Erweiterungen automatisch installiert werden
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Erweiterungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\1 = "gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\2 = "abcdefghijklmnopabcdefghijklmnop"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ExtensionInstallForcelist
  - Beispielwert:
``` xml
<array>
  <string>gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx</string>
  <string>abcdefghijklmnopabcdefghijklmnop</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ExtensionInstallSources
  #### Erweiterung und Benutzer-Skriptinstallationsquellen konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Definiert URLs, die Erweiterungen und Themen installieren können.

Standardmäßig müssen Benutzer für jede Erweiterung oder jedes Skript, das sie installieren möchten, eine *.crx-Datei herunterladen und diese dann auf die Microsoft Edge-Einstellungsseite ziehen. Diese Richtlinie ermöglicht es bestimmten URLs, die Erweiterung oder das Skript für den Benutzer zu installieren.

Jedes Element in dieser Liste ist ein erweiterungsartiges Zuordnungsmuster (siehe [https://go.microsoft.com/fwlink/?linkid=2095039](https://go.microsoft.com/fwlink/?linkid=2095039)). Benutzer können Elemente einfach von jeder URL installieren, die mit einem Element in dieser Liste übereinstimmt. Sowohl der Speicherort der *.crx-Datei als auch die Seite, von der aus der Download gestartet wird (d.h. der Referrer), müssen durch diese Muster erlaubt sein.

Die Richtlinie [ExtensionInstallBlocklist](#extensioninstallblocklist) hat Vorrang vor dieser Richtlinie. Alle Erweiterungen, die sich auf der Blockliste befinden, werden nicht installiert, auch wenn sie von einer Website auf dieser Liste stammen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ExtensionInstallSources
  - Gruppenrichtlinienname: Erweiterung und Benutzer-Skriptinstallationsquellen konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Erweiterungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources\1 = "https://corp.contoso.com/*"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ExtensionInstallSources
  - Beispielwert:
``` xml
<array>
  <string>https://corp.contoso.com/*</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ExtensionSettings
  #### Einstellungen für Erweiterungsverwaltung konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Konfiguriert die Einstellungen für die Erweiterungsverwaltung für Microsoft Edge.

Diese Richtlinie steuert mehrere Einstellungen, einschließlich Einstellungen, die durch vorhandene erweiterungsbezogene Richtlinien gesteuert werden. Diese Richtlinie setzt alle Vorgänger-Richtlinien außer Kraft, wenn beide Einstellungen festgelegt sind.

Mit dieser Richtlinie wird der Konfiguration eine Erweiterungs-ID oder eine Update-URL zugeordnet. Mit einer Erweiterungs-ID wird die Konfiguration nur auf die angegebene Erweiterung angewendet. Legen Sie eine Standardkonfiguration für die spezielle ID "*" fest, die auf alle Erweiterungen angewendet werden soll, die nicht speziell in dieser Richtlinie aufgeführt sind. Mit einer Update-URL wird die Konfiguration auf alle Erweiterungen mit der genauen Update-URL angewendet, die im Manifest dieser Erweiterung angegeben ist, wie unter [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043) beschrieben.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Wörterbuch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ExtensionSettings
  - Gruppenrichtlinienname: Einstellungen für Erweiterungsverwaltung konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Erweiterungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ExtensionSettings
  - Werttyp: REG_SZ
  ##### Beispielwert:
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


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ExtensionSettings
  - Beispielwert:
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
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ## HTTP-Authentifizierung policies

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AllowCrossOriginAuthPrompt
  #### Übergreifende HTTP-Basic-Authentifizierungsaufforderungen zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Steuert, ob untergeordnete Inhalte von Drittanbietern auf einer Seite ein Dialogfeld für die HTTP-Standardauthentifizierung öffnen können.

Dies ist normalerweise im Sinne der Phishing-Abwehr deaktiviert. Wenn Sie diese Richtlinie nicht konfigurieren, ist sie deaktiviert, und untergeordnete Inhalte von Drittanbietern können kein Dialogfeld für die HTTP-Standardauthentifizierung öffnen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AllowCrossOriginAuthPrompt
  - Gruppenrichtlinienname: Übergreifende HTTP-Basic-Authentifizierungsaufforderungen zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/HTTP-Authentifizierung
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AllowCrossOriginAuthPrompt
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AllowCrossOriginAuthPrompt
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AuthNegotiateDelegateAllowlist
  #### Gibt eine Liste der Server an, an die Microsoft Edge Anmeldeinformationen von Benutzern delegieren kann
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Konfigurieren Sie die Liste der Server, an die Microsoft Edge delegieren kann.

Trennen Sie mehrere Servernamen durch Kommas. Platzhalter (*) sind zulässig.

Wenn Sie diese Richtlinie nicht konfigurieren, wird Microsoft Edge keine Benutzeranmeldeinformationen delegieren, auch wenn ein Server als Intranet erkannt wird.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AuthNegotiateDelegateAllowlist
  - Gruppenrichtlinienname: Gibt eine Liste der Server an, an die Microsoft Edge Anmeldeinformationen von Benutzern delegieren kann
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/HTTP-Authentifizierung
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AuthNegotiateDelegateAllowlist
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"contoso.com"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AuthNegotiateDelegateAllowlist
  - Beispielwert:
``` xml
<string>contoso.com</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AuthSchemes
  #### Unterstützte Authentifizierungsschemas
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt an, welche HTTP-Authentifizierungsschemas unterstützt werden.

Sie können die Richtlinie mit folgenden Werten konfigurieren: „Basic“, „Digest“, „NTLM“ und „Negotiate“. Trennen Sie mehrere Werte durch Kommas.

Wenn Sie diese Richtlinie nicht konfigurieren, werden alle vier Schemas verwendet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AuthSchemes
  - Gruppenrichtlinienname: Unterstützte Authentifizierungsschemas
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/HTTP-Authentifizierung
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AuthSchemes
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"basic,digest,ntlm,negotiate"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AuthSchemes
  - Beispielwert:
``` xml
<string>basic,digest,ntlm,negotiate</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AuthServerAllowlist
  #### Liste der zugelassenen Authentifizierungsserver konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Legt fest, welche Server für die integrierte Authentifizierung aktiviert werden sollen. Die integrierte Authentifizierung ist nur aktiviert, wenn Microsoft Edge eine Anfrage zur Authentifizierung von einem Proxy oder einem Server in dieser Liste erhält.

Trennen Sie mehrere Servernamen durch Kommas. Platzhalter (*) sind zulässig.

Falls Sie diese Richtlinie nicht konfigurieren, versucht Microsoft Edge zu erkennen, ob sich ein Server im Intranet befindet, nur dann reagiert er auf IWA-Anfragen. Falls sich der Server im Internet befindet, werden IWA-Anfragen von ihm durch Microsoft Edge ignoriert.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AuthServerAllowlist
  - Gruppenrichtlinienname: Liste der zugelassenen Authentifizierungsserver konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/HTTP-Authentifizierung
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AuthServerAllowlist
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"*contoso.com,contoso.com"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AuthServerAllowlist
  - Beispielwert:
``` xml
<string>*contoso.com,contoso.com</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DisableAuthNegotiateCnameLookup
  #### CNAME-Lookup beim Aushandeln der Kerberos-Authentifizierung deaktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Bestimmt, ob der generierte Kerberos-SPN auf dem kanonischen DNS-Namen (CNAME) oder auf dem ursprünglichen eingegebenen Namen basiert.

Wenn Sie diese Richtlinie aktivieren, wird die CNAME-Suche übersprungen und der Servername (wie eingegeben) verwendet.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird der kanonische Name des Servers verwendet. Dieser wird durch die CNAME-Suche bestimmt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DisableAuthNegotiateCnameLookup
  - Gruppenrichtlinienname: CNAME-Lookup beim Aushandeln der Kerberos-Authentifizierung deaktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/HTTP-Authentifizierung
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DisableAuthNegotiateCnameLookup
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DisableAuthNegotiateCnameLookup
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### EnableAuthNegotiatePort
  #### Nicht standardmäßigen Port in Kerberos-SPN einschließen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt an, ob der generierte Kerberos-SPN einen nicht standardmäßigen Anschluss enthalten soll

Wenn Sie diese Richtlinie aktivieren und ein Benutzer einen nicht standardmäßigen Port (einen anderen Port als 80 oder 443) in einer URL enthält, ist dieser in den generierten Kerberos-SPN enthalten

Wenn Sie diese Richtlinie nicht konfigurieren oder deaktivieren, enthalten die generierten Kerberos-SPN in keinem Fall einen Port.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: EnableAuthNegotiatePort
  - Gruppenrichtlinienname: Nicht standardmäßigen Port in Kerberos-SPN einschließen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/HTTP-Authentifizierung
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: EnableAuthNegotiatePort
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: EnableAuthNegotiatePort
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NtlmV2Enabled
  #### Steuern, ob die NTLMv2-Authentifizierung aktiviert ist
  
  
  #### Unterstützte Versionen:
  - Unter macOS seit Version 77 oder höher

  #### Beschreibung
  Steuert, ob NTLMv2 aktiviert ist.

Alle neueren Versionen von Samba- und Windows-Servern unterstützen NTLMv2. Sie sollten NTLMv2 nur deaktivieren, um Probleme mit Rückwärtskompatibilität zu beheben, da dadurch die Sicherheit der Authentifizierung verringert wird.

Wenn Sie diese Richtlinie nicht konfigurieren, ist NTLMv2 standardmäßig aktiviert.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  

  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: NtlmV2Enabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ## Inhaltseinstellungen policies

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AutoSelectCertificateForUrls
  #### Clientzertifikate für diese Websites automatisch auswählen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Geben Sie eine Websiteliste auf der Grundlage von URL-Mustern an, für die Microsoft Edge automatisch ein Clientzertifikat auswählen soll, wenn von der Website eines angefordert wird.

Der Wert muss ein Zeichenfolgenarray mit JSON-Wörterbüchern sein. Die einzelnen Wörterbücher müssen jeweils das Format { "pattern": "$URL_PATTERN", "filter" : $FILTER } besitzen, wobei $URL_PATTERN ein Inhaltseinstellungsmuster ist. $FILTER schränkt ein, welche Clientzertifikate der Browser automatisch auswählen kann. Unabhängig von diesem Filter können nur Zertifikate verwendet werden, die der Zertifikatanforderung des Servers entsprechen. Beispiel: Wenn $FILTER das Format { "ISSUER": { "CN": "$ISSUER_CN" } } hat, können zusätzlich nur Clientzertifikate verwendet werden, die von einem Zertifikat mit dem allgemeinen Namen $ISSUER_CN ausgestellt wurden. Wenn $FILTER einen Abschnitt vom Typ "ISSUER" und einen Abschnitt vom Typ "SUBJECT" enthält, muss ein Clientzertifikat beide Bedingungen erfüllen, um ausgewählt werden zu können. Wenn $FILTER eine Organisation („O“) angibt, muss ein Zertifikat über mindestens eine Organisation verfügen, die dem angegebenen Wert entspricht, um ausgewählt werden zu können. Wenn $FILTER eine Organisationseinheit („OU“) angibt, muss ein Zertifikat über mindestens eine Organisationseinheit verfügen, die dem angegebenen Wert entspricht, um ausgewählt werden zu können. Wenn es sich bei $FILTER um das leere Wörterbuch {} handelt, wird die Clientzertifikatauswahl nicht weiter eingeschränkt.

Wenn Sie diese Richtlinie nicht konfigurieren, erfolgt keine automatische Auswahl für Websites.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AutoSelectCertificateForUrls
  - Gruppenrichtlinienname: Clientzertifikate für diese Websites automatisch auswählen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls\1 = "{\"pattern\":\"https://www.contoso.com\",\"filter\":{\"ISSUER\":{\"CN\":\"certificate issuer name\", \"L\": \"certificate issuer location\", \"O\": \"certificate issuer org\", \"OU\": \"certificate issuer org unit\"}, \"SUBJECT\":{\"CN\":\"certificate subject name\", \"L\": \"certificate subject location\", \"O\": \"certificate subject org\", \"OU\": \"certificate subject org unit\"}}}"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AutoSelectCertificateForUrls
  - Beispielwert:
``` xml
<array>
  <string>{"pattern":"https://www.contoso.com","filter":{"ISSUER":{"CN":"certificate issuer name", "L": "certificate issuer location", "O": "certificate issuer org", "OU": "certificate issuer org unit"}, "SUBJECT":{"CN":"certificate subject name", "L": "certificate subject location", "O": "certificate subject org", "OU": "certificate subject org unit"}}}</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### CookiesAllowedForUrls
  #### Cookies auf bestimmten Websites zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Definiert basierend auf URL-Mustern eine Liste von Sites, die Cookies setzen dürfen.

Wenn Sie diese Richtlinie nicht konfigurieren, wird für alle Sites der globale Standardwert (falls festgelegt) aus der Richtlinie [DefaultCookiesSetting](#defaultcookiessetting) oder die persönliche Konfiguration des Benutzers verwendet.

Weitere Informationen finden Sie in den Richtlinien [CookiesBlockedForUrls](#cookiesblockedforurls) und [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls).

Beachten Sie, dass es keine widersprüchlichen URL-Muster für die folgenden drei Richtlinien geben darf:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- CookiesAllowedForUrls

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

Um Cookies von der Löschung beim Beenden auszuschließen, konfigurieren Sie die Richtlinie [SaveCookiesOnExit](#savecookiesonexit).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: CookiesAllowedForUrls
  - Gruppenrichtlinienname: Cookies auf bestimmten Websites zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: CookiesAllowedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### CookiesBlockedForUrls
  #### Cookies auf bestimmten Websites blockieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Definiert basierend auf URL-Mustern eine Liste von Sites, die keine Cookies setzen dürfen.

Wenn Sie diese Richtlinie nicht konfigurieren, wird für alle Sites der globale Standardwert (falls festgelegt) aus der Richtlinie [DefaultCookiesSetting](#defaultcookiessetting) oder die persönliche Konfiguration des Benutzers verwendet.

Weitere Informationen finden Sie in den Richtlinien [CookiesAllowedForUrls](#cookiesallowedforurls) und [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls).

Beachten Sie, dass es keine widersprüchlichen URL-Muster für die folgenden drei Richtlinien geben darf:

- CookiesBlockedForUrls

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: CookiesBlockedForUrls
  - Gruppenrichtlinienname: Cookies auf bestimmten Websites blockieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: CookiesBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### CookiesSessionOnlyForUrls
  #### Cookies von bestimmten Websites auf die aktuelle Sitzung beschränken
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Cookies, die von Websites erstellt werden, die einem von Ihnen definierten URL-Muster entsprechen, werden nach Beendigung der Sitzung (wenn das Fenster geschlossen wird) gelöscht.

Cookies, die von Websites erstellt werden, die nicht mit dem Muster übereinstimmen, werden durch die Richtlinie [DefaultCookiesSetting](#defaultcookiessetting) (falls konfiguriert) oder durch die persönliche Konfiguration des Benutzers gesteuert. Dies ist auch das Standardverhalten, wenn Sie diese Richtlinie nicht konfigurieren.

Wenn Microsoft Edge im Hintergrundmodus läuft, wird die Sitzung möglicherweise nicht geschlossen, nachdem das letzte Fenster geschlossen wurde, was bedeutet, dass die Cookies beim Schließen des Fensters nicht gelöscht werden. In der Richtlinie [BackgroundModeEnabled](#backgroundmodeenabled) finden Sie Informationen über das Verhalten von Microsoft Edge im Hintergrundmodus.

Sie können auch die Richtlinien [CookiesAllowedForUrls](#cookiesallowedforurls) und [CookiesBlockedForUrls](#cookiesblockedforurls) verwenden, um zu steuern, welche Websites Cookies erstellen können.

Beachten Sie, dass es keine widersprüchlichen URL-Muster für die folgenden drei Richtlinien geben darf:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- CookiesSessionOnlyForUrls

Wenn Sie die Richtlinie [RestoreOnStartup](#restoreonstartup) zur Wiederherstellung von URLs aus früheren Sitzungen aktivieren, wird diese Richtlinie ignoriert, und Cookies werden für diese Seiten dauerhaft gespeichert.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: CookiesSessionOnlyForUrls
  - Gruppenrichtlinienname: Cookies von bestimmten Websites auf die aktuelle Sitzung beschränken
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: CookiesSessionOnlyForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultCookiesSetting
  #### Cookies konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Diese Richtlinie steuert, ob Websites Cookies auf dem Gerät des Benutzers erstellen können. Es kann entweder jede oder keine Website Cookies erstellen. Sie können diese Richtlinie nicht verwenden, um Cookies von bestimmten Websites zuzulassen.

Legen Sie die Richtlinie auf "SessionOnly" fest, um Cookies zu löschen, wenn die Sitzung geschlossen wird. Wird Microsoft Edge im Hintergrundmodus ausgeführt, wird die Sitzung möglicherweise nicht geschlossen, sobald das letzte Fenster geschlossen wird, was bedeutet, dass die Cookies nicht gelöscht werden, wenn das Fenster geschlossen wird. In der Richtlinie [BackgroundModeEnabled](#backgroundmodeenabled) finden Sie weitere Informationen über das Verhalten von Microsoft Edge im Hintergrundmodus.

Wenn Sie diese Richtlinie nicht konfigurieren, wird die Standardeinstellung “AllowCookies” verwendet, und Benutzer können diese Einstellung in den Microsoft Edge-Einstellungen ändern. (Wenn Sie nicht möchten, dass Benutzer diese Einstellung ändern können, legen Sie die Richtlinie fest.)

Zuordnung der Richtlinienoptionen:

* AllowCookies (1) = Cookieerstellung für alle Websites zulassen

* BlockCookies (2) = Nicht zulassen, dass Websites Cookies erstellen

* SessionOnly (4) = Cookies für die Dauer der Sitzung behalten, mit Ausnahme solcher, die unter [SaveCookiesOnExit](#savecookiesonexit) aufgeführt sind.

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultCookiesSetting
  - Gruppenrichtlinienname: Cookies konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DefaultCookiesSetting
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultCookiesSetting
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultGeolocationSetting
  #### Standardeinstellung für Geolocation
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Mit dieser Richtlinie legen Sie fest, ob Websites den physischen Standort von Benutzern nachverfolgen können. Sie können die Nachverfolgung standardmäßig zulassen ("AllowGeolocation"), standardmäßig verweigern ("BlockGeolocation") oder den Benutzer jedes Mal um Erlaubnis bitten, wenn eine Website nach seinen Standort nachverfolgen will ("AskGeolocation").

Wenn Sie diese Richtlinie nicht konfigurieren, wird "AskGeolocation" verwendet, und der Benutzer kann die Richtlinie ändern.

Zuordnung der Richtlinienoptionen:

* AllowGeolocation (1) = Websites erlauben, den physischen Standort der Benutzer nachzuverfolgen

* BlockGeolocation (2) = Nicht zulassen, dass Websites den physischen Standort von Benutzern nachverfolgen

* AskGeolocation (3) = Fragen, jedes Mal, wenn eine Website den physischen Standort nachverfolgen möchte

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultGeolocationSetting
  - Gruppenrichtlinienname: Standardeinstellung für Geolocation
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DefaultGeolocationSetting
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultGeolocationSetting
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultImagesSetting
  #### Standardeinstellung für Bilder
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Mit dieser Richtlinie legen Sie fest, ob Websites Bilder anzeigen dürfen. Sie können Bilder auf allen Websites zulassen (“AllowImages”) oder für alle Websites sperren (“BlockImages”).

Wenn Sie diese Richtlinie nicht konfigurieren, sind Bilder standardmäßig erlaubt, und der Benutzer kann diese Einstellung ändern.

Zuordnung der Richtlinienoptionen:

* AllowImages (1) = Allen Websites erlauben, alle Bilder anzuzeigen

* BlockImages (2) = Nicht zulassen, dass Websites Bilder anzeigen

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultImagesSetting
  - Gruppenrichtlinienname: Standardeinstellung für Bilder
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DefaultImagesSetting
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultImagesSetting
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultInsecureContentSetting
  #### Nutzung von Ausnahmen für unsicheren Inhalt steuern
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 80 oder höher

  #### Beschreibung
  Ermöglicht Ihnen das Festlegen, ob Benutzer Ausnahmen hinzufügen können, um gemischte Inhalte für bestimmte Websites zuzulassen.

Diese Richtlinie kann für bestimmte URL-Muster mit den Richtlinien [InsecureContentAllowedForUrls](#insecurecontentallowedforurls) und [InsecureContentBlockedForUrls](#insecurecontentblockedforurls) außer Kraft gesetzt werden.

Wenn diese Richtlinie nicht festgelegt ist, können Benutzer Ausnahmen hinzufügen, um blockierbare gemischte Inhalte zuzulassen, und automatische Upgrades für optional blockierbare gemischte Inhalte deaktivieren.

Zuordnung der Richtlinienoptionen:

* BlockInsecureContent (2) = Nicht zulassen, dass Websites gemischte Inhalte laden

* AllowExceptionsInsecureContent (3) = Benutzern das Hinzufügen von Ausnahmen ermöglichen, um gemischte Inhalte zuzulassen

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultInsecureContentSetting
  - Gruppenrichtlinienname: Nutzung von Ausnahmen für unsicheren Inhalt steuern
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DefaultInsecureContentSetting
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000002
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultInsecureContentSetting
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultJavaScriptSetting
  #### Standard-JavaScript-Einstellung
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Mit dieser Richtlinie legen Sie fest, ob Websites JavaScript ausführen dürfen. Sie können dies für alle Websites (“AllowJavaScript”) zulassen oder für alle Websites (“BlockJavaScript”) blockieren.

Falls Sie diese Richtlinie nicht konfigurieren, können alle Websites standardmäßig JavaScript ausführen, und der Benutzer kann diese Einstellung ändern.

Zuordnung der Richtlinienoptionen:

* AllowJavaScript (1) = Zulassen, dass alle Websites JavaScript ausführen

* BlockJavaScript (2) = Nicht zulassen, dass Websites JavaScript ausführen

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultJavaScriptSetting
  - Gruppenrichtlinienname: Standard-JavaScript-Einstellung
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DefaultJavaScriptSetting
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultJavaScriptSetting
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultNotificationsSetting
  #### Standard-Benachrichtigungseinstellung
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Mit dieser Richtlinie legen Sie fest, ob Websites Desktopbenachrichtigungen anzeigen dürfen. Sie können sie standardmäßig zulassen (“AllowNotifications”), sie standardmäßig verweigern (“BlockNotifications”) oder den Benutzer jedes Mal fragen lassen, wenn eine Website eine Benachrichtigung anzeigen möchte (“AskNotifications”).

Wenn Sie diese Richtlinie nicht konfigurieren, sind Benachrichtigungen standardmäßig zulässig, und der Benutzer kann diese Einstellung ändern.

Zuordnung der Richtlinienoptionen:

* AllowNotifications (1) = Zulassen, dass Websites Desktop-Benachrichtigungen anzeigen

* BlockNotifications (2) = Nicht zulassen, dass Websites Desktopbenachrichtigungen anzeigen

* AskNotifications (3) = Jedes Mal fragen, wenn eine Website Desktop-Benachrichtigungen anzeigen will

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultNotificationsSetting
  - Gruppenrichtlinienname: Standard-Benachrichtigungseinstellung
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DefaultNotificationsSetting
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000002
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultNotificationsSetting
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultPluginsSetting
  #### Standardeinstellung für Adobe Flash
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Zuerst werden [PluginsAllowedForUrls](#pluginsallowedforurls) und [PluginsBlockedForUrls](#pluginsblockedforurls) überprüft, dann diese Richtlinie. Es stehen die Optionen "ClickToPlay" und "BlockPlugins" zur Verfügung. Wenn Sie diese Richtlinie auf "BlockPlugins" festlegen, wird der Zugriff auf dieses Plug-In auf allen Websites verweigert. Mit "ClickToPlay" kann das Flash-Plug-in ausgeführt werden, Benutzer müssen aber auf den Platzhalter klicken, um es zu starten.

Wenn Sie diese Richtlinie nicht festlegen, verwendet Sie BlockPlugins, und Benutzer können diese Einstellung ändern.

Hinweis: Die automatische Wiedergabe steht nur für Domänen zur Verfügung, die explizit in der Richtlinie [PluginsAllowedForUrls](#pluginsallowedforurls) aufgelistet sind. Um die automatische Wiedergabe für alle Websites zu aktivieren, fügen Sie “http://*” und “https://*” zur Liste der zulässigen URLs hinzu.

Zuordnung der Richtlinienoptionen:

* BlockPlugins (2) = Adobe Flash-Plug-In blockieren

* ClickToPlay (3) = Zur Wiedergabe klicken

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultPluginsSetting
  - Gruppenrichtlinienname: Standardeinstellung für Adobe Flash
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DefaultPluginsSetting
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000002
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultPluginsSetting
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultPopupsSetting
  #### Standardeinstellung für Popupfenster
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Diese Richtlinie legt fest, ob Websites Popupfenster anzeigen dürfen. Sie können dies auf allen Websites zulassen (“AllowPopups”) oder blockieren (“BlockPopups”).

Wenn Sie diese Richtlinie nicht konfigurieren, werden Popupfenster standardmäßig blockiert, und Benutzer können diese Einstellung ändern.

Zuordnung der Richtlinienoptionen:

* AllowPopups (1) = Zulassen, dass Websites Einblendungen anzeigen

* BlockPopups (2) = Nicht zulassen, dass Websites Popups anzeigen

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultPopupsSetting
  - Gruppenrichtlinienname: Standardeinstellung für Popupfenster
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DefaultPopupsSetting
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultPopupsSetting
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultWebBluetoothGuardSetting
  #### Verwendung der Web-Bluetooth-API steuern
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Mit dieser Richtlinie steuern Sie, ob Websites auf Bluetooth-Geräte in der Nähe zugreifen können. Sie können den Zugriff vollständig blockieren oder so konfigurieren, dass die Website den Benutzer vor jedem Zugriff auf ein Bluetooth-Gerät fragen muss.

Wenn Sie diese Richtlinie nicht konfigurieren, wird der Standardwert  (“AskWebBluetooth”, d. h., Benutzer werden jedes Mal gefragt) verwendet, und Benutzer können ihn ändern.

Zuordnung der Richtlinienoptionen:

* BlockWebBluetooth (2) = Nicht zulassen, dass Websites über die Web-Bluetooth-API Zugriff auf Bluetooth-Geräte anfordern

* AskWebBluetooth (3) = Websites erlauben, beim Benutzer den Zugriff auf ein Bluetooth-Gerät in der Nähe anzufordern

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultWebBluetoothGuardSetting
  - Gruppenrichtlinienname: Verwendung der Web-Bluetooth-API steuern
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DefaultWebBluetoothGuardSetting
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000002
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultWebBluetoothGuardSetting
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultWebUsbGuardSetting
  #### Verwendung der WebUSB-API steuern
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  !Mit dieser Richtlinie legen Sie fest, ob Websites auf angeschlossene USB-Geräte zugreifen können. Sie können den Zugriff vollständig blockieren oder den Benutzer jedes Mal fragen, wenn eine Website Zugriff auf angeschlossene USB-Geräte erhalten möchte.

Sie können diese Richtlinie für bestimmte URL-Muster mi den Richtlinien “[WebUsbAskForUrls](#webusbaskforurls)” und “[WebUsbBlockedForUrls](#webusbblockedforurls)“ außer Kraft setzen.

Wenn Sie diese Richtlinie nicht konfigurieren, können Websites Benutzer fragen, ob sie standardmäßig auf die angeschlossenen USB-Geräte zugreifen können (“AskWebUsb”), und Benutzer können diese Einstellung ändern.

Zuordnung der Richtlinienoptionen:

* BlockWebUsb (2) = Nicht zulassen, dass Websites über die WebUSB-API Zugriff auf USB-Geräte anfordern

* AskWebUsb (3) = Websites erlauben, beim Benutzer den Zugriff auf ein verbundenes USB-Gerät anzufordern

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultWebUsbGuardSetting
  - Gruppenrichtlinienname: Verwendung der WebUSB-API steuern
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DefaultWebUsbGuardSetting
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000002
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultWebUsbGuardSetting
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ImagesAllowedForUrls
  #### Bilder auf diesen Websites zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Definiert basierend auf URL-Mustern eine Liste von Sites, die Bilder anzeigen dürfen.

Wenn Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der Richtlinie [DefaultImagesSetting](#defaultimagessetting) (sofern festgelegt) oder der persönlichen Konfiguration des Benutzers für alle Websites verwendet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ImagesAllowedForUrls
  - Gruppenrichtlinienname: Bilder auf diesen Websites zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ImagesAllowedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ImagesBlockedForUrls
  #### Bilder auf bestimmten Websites blockieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Definiert basierend auf URL-Mustern eine Liste von Sites, die Bilder anzeigen dürfen.

Wenn Sie diese Richtlinie nicht konfigurieren, wird für alle Sites der globale Standardwert (falls festgelegt) aus der Richtlinie [DefaultImagesSetting](#defaultimagessetting) oder die persönliche Konfiguration des Benutzers verwendet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ImagesBlockedForUrls
  - Gruppenrichtlinienname: Bilder auf bestimmten Websites blockieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ImagesBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### InsecureContentAllowedForUrls
  #### Unsicheren Inhalt auf angegebenen Websites zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 80 oder höher

  #### Beschreibung
  Erstellen Sie eine Liste mit URL-Mustern zum Angeben von Websites, die unsichere gemischte Inhalte (d. h. HTTP-Inhalte auf HTTPS-Websites) anzeigen können.

Wenn diese Richtlinie nicht konfiguriert ist, werden blockierbare gemischte Inhalte blockiert, und für optional blockierbare gemischte Inhalte wird ein Upgrade durchgeführt. Benutzer haben jedoch die Möglichkeit, für bestimmte Websites Ausnahmen zur Zulassung von unsicheren gemischten Inhalten festzulegen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: InsecureContentAllowedForUrls
  - Gruppenrichtlinienname: Unsicheren Inhalt auf angegebenen Websites zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\2 = "[*.]example.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: InsecureContentAllowedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### InsecureContentBlockedForUrls
  #### Unsicheren Inhalt auf angegebenen Websites blockieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 80 oder höher

  #### Beschreibung
  Erstellen Sie eine Liste mit URL-Mustern zum Angeben von Websites, für die die Anzeige von blockierbaren (d. h. aktiven) gemischten Inhalten (d. h. HTTP-Inhalte auf HTTPS-Websites) nicht zulässig ist und für die Upgrades für optional blockierbare gemischte Inhalte deaktiviert sind.

Wenn diese Richtlinie nicht konfiguriert ist, werden blockierbare gemischte Inhalte blockiert, und für optional blockierbare gemischte Inhalte wird ein Upgrade durchgeführt. Benutzer haben jedoch die Möglichkeit, für bestimmte Websites Ausnahmen zur Zulassung von unsicheren gemischten Inhalten festzulegen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: InsecureContentBlockedForUrls
  - Gruppenrichtlinienname: Unsicheren Inhalt auf angegebenen Websites blockieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\2 = "[*.]example.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: InsecureContentBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### JavaScriptAllowedForUrls
  #### JavaScript auf bestimmten Websites zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Definiert basierend auf URL-Mustern eine Liste von Sites, auf denen die Ausführung von JavaScript erlaubt ist.

Wenn Sie diese Richtlinie nicht konfigurieren, wird für alle Sites der globale Standardwert (falls festgelegt) aus der Richtlinie [DefaultJavaScriptSetting](#defaultjavascriptsetting) oder die persönliche Konfiguration des Benutzers verwendet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: JavaScriptAllowedForUrls
  - Gruppenrichtlinienname: JavaScript auf bestimmten Websites zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: JavaScriptAllowedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### JavaScriptBlockedForUrls
  #### JavaScript auf bestimmten Websites blockieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Definiert basierend auf URL-Mustern eine Liste von Sites, auf denen die Ausführung von JavaScript blockiert wird.

Wenn Sie diese Richtlinie nicht konfigurieren, wird für alle Sites der globale Standardwert (falls festgelegt) aus der Richtlinie [DefaultJavaScriptSetting](#defaultjavascriptsetting) oder die persönliche Konfiguration des Benutzers verwendet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: JavaScriptBlockedForUrls
  - Gruppenrichtlinienname: JavaScript auf bestimmten Websites blockieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: JavaScriptBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### LegacySameSiteCookieBehaviorEnabled
  #### Einstellung des standardmäßigen Cookieverhaltens für die Vorgängerversion von SameSite
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 80 oder höher

  #### Beschreibung
  Ermöglicht das Zurücksetzen aller Cookies auf das Verhalten der Vorgängerversion für SameSite. Das Zurücksetzen auf das Verhalten der Vorgängerversion bewirkt, dass Cookies, die kein “SameSite”-Attribut angeben, so behandelt werden, als ob sie “SameSite=None“ wären, und Cookies vom Typ “SameSite=None“ das Attribut “Secure“ nicht mehr enthalten müssen.

Wenn Sie diese Richtlinie nicht festlegen, hängt das Standardverhalten für Cookies, die kein “SameSite”-Attribut angeben, von anderen Konfigurationsquellen für die Funktion “SameSite-by-default” ab. Diese Funktion kann durch einen Feldtest oder durch Aktivieren des Flags “same-site-by-default-cookies” in “edge://flags“ festgelegt werden.

Zuordnung der Richtlinienoptionen:

* DefaultToLegacySameSiteCookieBehavior (1) = Auf das Verhalten der Vorgängerversion für SameSite für Cookies auf allen Websites zurücksetzen

* DefaultToSameSiteByDefaultCookieBehavior (2) = Verhalten für SameSite-by-default für Cookies auf allen Websites verwenden

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: LegacySameSiteCookieBehaviorEnabled
  - Gruppenrichtlinienname: Einstellung des standardmäßigen Cookieverhaltens für die Vorgängerversion von SameSite
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: LegacySameSiteCookieBehaviorEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: LegacySameSiteCookieBehaviorEnabled
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### LegacySameSiteCookieBehaviorEnabledForDomainList
  #### Auf das Verhalten der Vorgängerversion für SameSite für Cookies auf bestimmten Websites zurücksetzen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 80 oder höher

  #### Beschreibung
  Cookies, die für Domänen festgelegt sind, die bestimmten Mustern entsprechen, werden auf das Verhalten der Vorgängerversion von SameSite zurückgesetzt.

Das Zurücksetzen auf das Verhalten der Vorgängerversion bewirkt, dass Cookies, die kein SameSite-Attribut angeben, so behandelt werden, als ob sie „SameSite=None“, und Cookies vom Typ „SameSite=None“ müssen das Attribut „Secure“ nicht mehr enthalten.

Wenn Sie diese Richtlinie nicht festlegen, wird der globale Standardwert verwendet. Der globale Standard wird auch für Cookies in Domänen verwendet, die nicht durch die von Ihnen angegebenen Muster abgedeckt sind.

Der globale Standardwert kann mithilfe der Richtlinie [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) konfiguriert werden. Wenn [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) aufgehoben wird, wird der globale Standardwert auf andere Konfigurationsquellen zurückgesetzt.

Beachten Sie, dass Muster, die Sie in dieser Richtlinie auflisten, als Domänen und nicht als URLs behandelt werden, daher sollten Sie kein Schema und keinen Port angeben.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Gruppenrichtlinienname: Auf das Verhalten der Vorgängerversion für SameSite für Cookies auf bestimmten Websites zurücksetzen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\1 = "www.example.com"
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\2 = "[*.]example.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Beispielwert:
``` xml
<array>
  <string>www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NotificationsAllowedForUrls
  #### Benachrichtigungen auf bestimmten Websites zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Ermöglicht das Erstellen einer Liste von URL-Mustern, um Websites anzugeben, auf denen Benachrichtigungen angezeigt werden dürfen.

Wenn Sie diese Richtlinie nicht festlegen, wird der globale Standardwert für alle Sites verwendet. Dieser Standardwert stammt aus der [DefaultNotificationsSetting](#defaultnotificationssetting)-Richtlinie, falls festgelegt, oder aus der persönlichen Konfiguration des Nutzers. Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: NotificationsAllowedForUrls
  - Gruppenrichtlinienname: Benachrichtigungen auf bestimmten Websites zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: NotificationsAllowedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NotificationsBlockedForUrls
  #### Benachrichtigungen auf bestimmten Websites blockieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Ermöglicht das Erstellen einer Liste von URL-Mustern, um Websites anzugeben, auf denen keine Benachrichtigungen angezeigt werden dürfen.

Wenn Sie diese Richtlinie nicht festlegen, wird der globale Standardwert für alle Sites verwendet. Dieser Standardwert stammt aus der [DefaultNotificationsSetting](#defaultnotificationssetting)-Richtlinie, falls festgelegt, oder aus der persönlichen Konfiguration des Nutzers. Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: NotificationsBlockedForUrls
  - Gruppenrichtlinienname: Benachrichtigungen auf bestimmten Websites blockieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: NotificationsBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PluginsAllowedForUrls
  #### Adobe Flash-Plug-In auf bestimmten Websites zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Definieren Sie eine Liste von Websites basierend auf URL-Mustern, die das Adobe Flash-Plug-In ausführen können.

 Wenn Sie diese Richtlinie nicht konfigurieren, wird für alle Sites der globale Standardwert aus der [DefaultPluginsSetting](#defaultpluginssetting)-Richtlinie (falls festgelegt) oder die persönliche Konfiguration des Nutzers verwendet.

Ausführliche Informationen über gültige URL-Muster finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Ab M85 werden Platzhalter im Host mit „*“ und „[*.]“ am Anfang jedoch nicht mehr für diese Richtlinie unterstützt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PluginsAllowedForUrls
  - Gruppenrichtlinienname: Adobe Flash-Plug-In auf bestimmten Websites zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\2 = "http://contoso.edu:8080"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: PluginsAllowedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PluginsBlockedForUrls
  #### Adobe Flash-Plug-In auf bestimmten Websites blockieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Definieren Sie eine Liste von Websites basierend auf URL-Mustern, die zum Ausführen blockiert sind.Adobe Flash

 Wenn Sie diese Richtlinie nicht konfigurieren, wird für alle Sites der globale Standardwert aus der [DefaultPluginsSetting](#defaultpluginssetting)-Richtlinie (falls festgelegt) oder die persönliche Konfiguration des Nutzers verwendet.

Ausführliche Informationen über gültige URL-Muster finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Ab M85 werden Platzhalter im Host mit „*“ und „[*.]“ am Anfang jedoch nicht mehr für diese Richtlinie unterstützt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PluginsBlockedForUrls
  - Gruppenrichtlinienname: Adobe Flash-Plug-In auf bestimmten Websites blockieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\2 = "http://contoso.edu:8080"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: PluginsBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PopupsAllowedForUrls
  #### Popupfenster auf bestimmten Websites zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Definiert basierend auf URL-Mustern eine Liste von Sites, die Popup-Fenstern öffnen dürfen.

Wenn Sie diese Richtlinie nicht konfigurieren, wird für alle Sites der globale Standardwert (falls festgelegt) aus der Richtlinie [DefaultPopupsSetting](#defaultpopupssetting) oder die persönliche Konfiguration des Benutzers verwendet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PopupsAllowedForUrls
  - Gruppenrichtlinienname: Popupfenster auf bestimmten Websites zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: PopupsAllowedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PopupsBlockedForUrls
  #### Popupfenster auf bestimmten Websites blockieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Definiert basierend auf URL-Mustern eine Liste von Sites, auf denen das Öffnen von Popup-Fenstern blockiert wird.

Wenn Sie diese Richtlinie nicht konfigurieren, wird für alle Sites der globale Standardwert (falls festgelegt) aus der Richtlinie [DefaultPopupsSetting](#defaultpopupssetting) oder die persönliche Konfiguration des Benutzers verwendet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PopupsBlockedForUrls
  - Gruppenrichtlinienname: Popupfenster auf bestimmten Websites blockieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: PopupsBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### RegisteredProtocolHandlers
  #### Protokollhandler registrieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Legen Sie diese Richtlinie fest (nur empfohlen), um eine Liste der Protokollhandler zu registrieren. Diese Liste wird mit von Ihnen registrierten Benutzern zusammengeführt, und beide sind zur Verwendung verfügbar.

Um einen Protokollhandler zu registrieren:

– Legen Sie die Protokolleigenschaft für das Schema fest (z. B. „mailto“)
– Legen Sie die URL-Eigenschaft der Anwendung fest, das im Feld „Protokoll“ angegebenen Schema angegeben wird. Das Muster kann einen „%s“ Platzhalter enthalten, der die behandelte URL ersetzt.

Benutzer können einen durch diese Richtlinie registrierten Protokollhandler nicht entfernen. Sie können jedoch einen neuen Standard-Protokollhandler installieren, um die vorhandenen Protokollhandler außer Kraft zu setzen.

  #### Unterstützte Features:
  - Kann zwingend sein: Nein
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Wörterbuch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: RegisteredProtocolHandlers
  - Gruppenrichtlinienname: Protokollhandler registrieren
  - Gruppenrichtlinienpfad (Erforderlich): Nicht zutreffend
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Inhaltseinstellungen
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): Nicht zutreffend
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: RegisteredProtocolHandlers
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [
  {
    "default": true, 
    "protocol": "mailto", 
    "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"
  }
]
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: RegisteredProtocolHandlers
  - Beispielwert:
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
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SpotlightExperiencesAndRecommendationsEnabled
  #### Choose whether users can receive customized background images and text, suggestions, notifications,
and tips for Microsoft services
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 86 oder höher

  #### Beschreibung
  Choose whether users can receive customized background images and text, suggestions, notifications, and tips for Microsoft services.

If you enable or don't configure this setting, spotlight experiences and recommendations are turned on.

If you disable this setting, spotlight experiences and recommendations are turned off.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SpotlightExperiencesAndRecommendationsEnabled
  - Gruppenrichtlinienname: Choose whether users can receive customized background images and text, suggestions, notifications,
and tips for Microsoft services
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: SpotlightExperiencesAndRecommendationsEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### WebUsbAllowDevicesForUrls
  #### Gewährt bestimmten Websites Zugriff, damit eine Verbindung mit bestimmten USB-Geräten hergestellt werden kann.
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Ermöglicht es Ihnen, eine Liste von URLs anzugeben, die festlegen, welche Websites automatisch die Berechtigung zum Zugriff auf ein USB-Gerät mit den angegebenen Hersteller- und Produkt-IDs erhalten. Jedes Element in der Liste muss sowohl Geräte als auch URLs enthalten, damit die Richtlinie gültig ist. Jedes Element in Geräten kann eine Lieferanten-ID und ein Produkt-ID-Feld enthalten. Jede fehlende ID wird mit einer Ausnahme als Wildcard behandelt, und diese Ausnahme besteht darin, dass eine Produkt-ID nicht angegeben werden kann, ohne dass auch eine Lieferanten-ID angegeben wird. Andernfalls ist die Richtlinie nicht gültig und wird ignoriert.

Das USB-Berechtigungsmodell verwendet die URL der anfragenden Website ("anfragende URL") und die URL der obersten Frame-Site ("eingebettete URL"), um der anfragenden URL die Berechtigung zum Zugriff auf das USB-Gerät zu erteilen. Die anfragende URL kann sich von der einbettenden URL unterscheiden, wenn die anfragende Website in einem Iframe geladen wird. Daher kann das Feld "urls" bis zu zwei URL-Zeichenketten enthalten, die durch ein Komma getrennt sind, um die anfragende bzw. einbettende URL anzugeben. Ist nur eine URL angegeben, wird der Zugriff auf die entsprechenden USB-Geräte gewährt, wenn die URL der anfragenden Website unabhängig vom Einbettungsstatus mit dieser URL übereinstimmt. Die URLs in "urls" müssen gültige URLs sein, sonst wird die Richtlinie ignoriert.

Wenn diese Richtlinie nicht festgelegt ist, wird der globale Standardwert für alle Websites verwendet, entweder aus der Richtlinie [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (sofern festgelegt) oder aus der persönlichen Konfiguration des Benutzers.

Die URL-Muster in dieser Richtlinie dürfen nicht mit kollidieren, die in [WebUsbBlockedForUrls](#webusbblockedforurls) festgelegt sind. Wenn es zu einem Konflikt kommt, hat diese Richtlinie Vorrang vor [WebUsbBlockedForUrls](#webusbblockedforurls) und [WebUsbAskForUrls](#webusbaskforurls).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Wörterbuch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: WebUsbAllowDevicesForUrls
  - Gruppenrichtlinienname: Gewährt bestimmten Websites Zugriff, damit eine Verbindung mit bestimmten USB-Geräten hergestellt werden kann.
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: WebUsbAllowDevicesForUrls
  - Werttyp: REG_SZ
  ##### Beispielwert:
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


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: WebUsbAllowDevicesForUrls
  - Beispielwert:
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
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### WebUsbAskForUrls
  #### WebUSB auf bestimmten Websites zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Definieren Sie basierend auf URL-Mustern eine Liste von Websites, die den Nutzer zum Zugriff auf ein USB-Gerät auffordern können.

Wenn Sie diese Richtlinie nicht konfigurieren, wird für alle Sites der globale Standardwert aus der [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)-Richtlinie (falls festgelegt) oder die persönliche Konfiguration des Benutzers verwendet.

 Die in dieser Richtlinie definierten URL-Muster können nicht denen in der [WebUsbBlockedForUrls](#webusbblockedforurls)-Richtlinie konfigurierten widersprechen. Sie können eine URL nicht gleichzeitig zulassen und blockieren. Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: WebUsbAskForUrls
  - Gruppenrichtlinienname: WebUSB auf bestimmten Websites zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: WebUsbAskForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### WebUsbBlockedForUrls
  #### WebUSB auf bestimmten Websites blockieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Definieren Sie eine Liste von Websites basierend auf URL-Mustern, die den Nutzer nicht auffordern können, ihm Zugriff auf ein USB-Gerät zu gewähren.

 Wenn Sie diese Richtlinie nicht konfigurieren, wird für alle Sites der globale Standardwert aus der [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)-Richtlinie (falls festgelegt) oder die persönliche Konfiguration des Nutzers verwendet.

URL-Muster in dieser Richtlinie können nicht mit den in der [WebUsbAskForUrls](#webusbaskforurls)-Richtlinie konfigurierten Mustern in Konflikt stehen. Sie können eine URL nicht zulassen und gleichzeitig blockieren. Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: WebUsbBlockedForUrls
  - Gruppenrichtlinienname: WebUSB auf bestimmten Websites blockieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Inhaltseinstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: WebUsbBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ## Kennwort-Manager und -schutz policies

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PasswordManagerEnabled
  #### Speichern von Kennwörtern im Kennwort-Manager ermöglichen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Ermöglicht Microsoft Edge das Speichern von Benutzerkennwörtern.

Wenn Sie diese Richtlinie aktivieren, können Benutzer ihre Kennwörter in Microsoft Edge speichern. Beim nächsten Besuch der Website fügt Microsoft Edge das Kennwort automatisch ein.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer keine neuen Kennwörter speichern. Zuvor gespeicherte Kennwörter können jedoch weiterhin verwendet werden.

Wenn Sie diese Richtlinie aktivieren oder deaktivieren, kann sie von Benutzern in Microsoft Edge nicht geändert oder überschrieben werden. Wenn Sie die Richtlinie nicht konfigurieren, können Benutzer Kennwörter speichern und dieses Feature deaktivieren.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PasswordManagerEnabled
  - Gruppenrichtlinienname: Speichern von Kennwörtern im Kennwort-Manager ermöglichen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Kennwort-Manager und -schutz
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Kennwort-Manager und -schutz
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: PasswordManagerEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: PasswordManagerEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PasswordMonitorAllowed
  #### Ermöglichen Sie Nutzern, benachrichtigt zu werden, wenn sich herausstellt, dass ihre Kennwörter unsicher sind
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 85 oder höher

  #### Beschreibung
  Erlauben Sie Microsoft Edge, Nutzerkennwörter zu überwachen.

  Wenn Sie diese Richtlinie aktivieren und ein Benutzer der Aktivierung der Richtlinie zustimmt, wird der Benutzer benachrichtigt, wenn eines seiner in Microsoft Edge gespeicherten Kennwörter als unsicher eingestuft wird. Microsoft Edge zeigt eine Warnung an und diese Informationen sind auch in Einstellungen > Kennwörter > Kennwortüberwachung verfügbar.

 Wenn Sie diese Richtlinie deaktivieren, werden Benutzer nicht um Erlaubnis zum Aktivieren dieser Funktion aufgefordert. Ihre Passwörter werden nicht gescannt und sie werden auch nicht benachrichtigt.

Wenn Sie die Richtlinie aktivieren oder nicht konfigurieren, können Benutzer diese Funktion aktivieren oder deaktivieren.

  Weitere Informationen dazu, wie Microsoft Edge unsichere Kennwörter findet, finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2133833](https://go.microsoft.com/fwlink/?linkid=2133833)

  Zusätzliche Anleitung:

  Diese Richtlinie kann sowohl als empfohlen als auch als obligatorisch festgelegt werden, jedoch mit einem Hinweis auf ihre Wichtigkeit.

  „Obligatorisch“ aktiviert: Da die Zustimmung des Nutzers eine Voraussetzung für die Aktivierung dieser Funktion für einen Nutzer ist, ist für diese Richtlinie keine „Obligatorisch“ aktivierte Einstellung festgelegt. Wenn die Richtlinie auf „Obligatorisch“ aktiviert eingestellt ist, ändert sich die Benutzeroberfläche in den Einstellungen nicht und die folgende Fehlermeldung wird in Edge angezeigt: //policy

  Beispiel für eine Fehlerstatusmeldung: „Dieser Richtlinienwert wird ignoriert, da für die Aktivierung der Kennwortüberwachung die Zustimmung des  Nutzers erforderlich ist. Sie können Nutzer in Ihrer Organisation auffordern, zu Einstellungen > Profil > Kennwort zu wechseln und die Funktion zu aktivieren.“

 „Empfohlen“ aktiviert: Wenn die Richtlinie auf „Empfohlen“ aktiviert eingestellt ist, bleibt die Benutzeroberfläche in den Einstellungen im Status „Aus“. Daneben wird jedoch ein Aktentaschensymbol angezeigt, auf dem diese Beschreibung beim Hover angezeigt wird. „Ihre Organisation empfiehlt einen bestimmten Wert für diese Einstellung und Sie haben einen anderen Wert gewählt“

  „Obligatorisch“ und „Empfohlen“ deaktiviert: Beide Zustände funktionieren auf normale Weise, wobei den Nutzern die üblichen Texte angezeigt werden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PasswordMonitorAllowed
  - Gruppenrichtlinienname: Ermöglichen Sie Nutzern, benachrichtigt zu werden, wenn sich herausstellt, dass ihre Kennwörter unsicher sind
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Kennwort-Manager und -schutz
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Kennwort-Manager und -schutz
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: PasswordMonitorAllowed
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PasswordProtectionChangePasswordURL
  #### URL zum Ändern des Kennworts konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Konfiguriert die URL zum Ändern des Kennworts (nur HTTP- und HTTPS-Schemas).

  Der Kennwortschutzdienst leitet Benutzer an diese URL weiter, damit sie ihr Kennwort ändern können, nachdem eine Warnung im Browser angezeigt wurde.

  Wenn Sie diese Richtlinie aktivieren, leitet der Kennwortschutzdienst Benutzer an diese URL weiter, damit sie ihr Kennwort ändern können.

  Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden Benutzer nicht an eine URL für die Kennwortänderung weitergeleitet.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PasswordProtectionChangePasswordURL
  - Gruppenrichtlinienname: URL zum Ändern des Kennworts konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Kennwort-Manager und -schutz
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: PasswordProtectionChangePasswordURL
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"https://contoso.com/change_password.html"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: PasswordProtectionChangePasswordURL
  - Beispielwert:
``` xml
<string>https://contoso.com/change_password.html</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PasswordProtectionLoginURLs
  #### Liste der Unternehmens-Anmelde-URLs konfigurieren, bei denen der Kennwortschutzdienst zufällig gewählte Zeichenfolgen des Kennworts aufzeichnen soll
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Konfigurieren Sie die Liste der Unternehmens-Anmelde-URLs (nur HTTP- und HTTPS-Schemas), bei denen Microsoft Edge zufällig gewählte Zeichenfolgen von Kennwörtern erfassen und zur Kennwort-Wiederverwendungserkennung verwenden soll.

Wenn Sie diese Richtlinie aktivieren, erfasst der Kennwortschutzdienst Fingerabdrücke von Kennwörtern für die definierten URLs.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden keine Kennwortfingerabdrücke erfasst.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PasswordProtectionLoginURLs
  - Gruppenrichtlinienname: Liste der Unternehmens-Anmelde-URLs konfigurieren, bei denen der Kennwortschutzdienst zufällig gewählte Zeichenfolgen des Kennworts aufzeichnen soll
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Kennwort-Manager und -schutz
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\1 = "https://contoso.com/login.html"
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\2 = "https://login.contoso.com"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: PasswordProtectionLoginURLs
  - Beispielwert:
``` xml
<array>
  <string>https://contoso.com/login.html</string>
  <string>https://login.contoso.com</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PasswordProtectionWarningTrigger
  #### Warnungstrigger für Kennwortschutz konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Mit dieser Richtlinie steuern Sie, wann eine Warnung zum Kennwortschutz angezeigt werden soll. Der Kennwortschutz warnt Benutzer, wenn sie ihr geschütztes Passwort auf potenziell verdächtigen Websites wiederverwenden.

Sie können die Richtlinien “[PasswordProtectionLoginURLs](#passwordprotectionloginurls)” und “[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)“ verwenden, um zu konfigurieren, welche Kennwörter geschützt werden sollen.

Ausnahmen: Kennwörter, die in “[PasswordProtectionLoginURLs](#passwordprotectionloginurls)” und “[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)” aufgeführt sind, lösen keine Warnung für den Kennwortschutz aus. Das gilt auch für alle in “[SmartScreenAllowListDomains](#smartscreenallowlistdomains)“ angegebenen Sites.

Mit “PasswordProtectionWarningOff” werden keine Warnungen für den Kennwortschutz angezeigt.

Mit “PasswordProtectionWarningOnPasswordReuse” werden Warnungen für den Kennwortschutz angezeigt, wenn der Benutzer sein geschütztes Kennwort auf einer nicht auf einer Whitelist stehenden Website wiederverwendet.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird der Warnungstrigger nicht angezeigt.

Zuordnung der Richtlinienoptionen:

* PasswordProtectionWarningOff (0) = Kennwortschutzwarnung deaktiviert

* PasswordProtectionWarningOnPasswordReuse (1) = Eine Kennwortschutzwarnung wird ausgelöst, wenn das Kennwort wiederverwendet wird.

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PasswordProtectionWarningTrigger
  - Gruppenrichtlinienname: Warnungstrigger für Kennwortschutz konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Kennwort-Manager und -schutz
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: PasswordProtectionWarningTrigger
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: PasswordProtectionWarningTrigger
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ## Natives Messaging policies

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NativeMessagingAllowlist
  #### Steuern, welche nativen Messaginghosts von Benutzern verwendet werden können
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Listet bestimmte native Messaging-Hosts auf, die Benutzer in Microsoft Edge verwenden können.

Standardmäßig sind alle nativen Messaging-Hosts zugelassen. Wenn Sie die Richtlinie [NativeMessagingBlocklist](#nativemessagingblocklist) auf * setzen, werden alle nativen Messaging-Hosts blockiert und nur die hier aufgeführten nativen Messaging-Hosts geladen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: NativeMessagingAllowlist
  - Gruppenrichtlinienname: Steuern, welche nativen Messaginghosts von Benutzern verwendet werden können
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Natives Messaging
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\2 = "com.native.messaging.host.name2"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: NativeMessagingAllowlist
  - Beispielwert:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NativeMessagingBlocklist
  #### Native Nachrichtensperrliste konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt an, welche nativen Messaginghosts nicht verwendet werden sollen.

Verwenden Sie "*", um alle nativen Messaginghosts zu blockieren, sofern Sie nicht explizit in der Liste "Zulassen" aufgeführt sind.

Wenn Sie diese Richtlinie nicht konfigurieren, werden von Microsoft Edge alle installierten nativen Messaginghosts geladen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: NativeMessagingBlocklist
  - Gruppenrichtlinienname: Native Nachrichtensperrliste konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Natives Messaging
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\2 = "com.native.messaging.host.name2"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: NativeMessagingBlocklist
  - Beispielwert:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NativeMessagingUserLevelHosts
  #### Native Messaginghosts auf Benutzerebene zulassen (ohne Administratorberechtigungen installiert)
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Aktiviert die Installation von nativen Messaginghosts auf Benutzerebene.

Wenn sie diese Richtlinie deaktivieren, verwendet Microsoft Edge nur native Messaginghosts, die auf der Systemebene installiert sind.

Wenn sie diese Richtlinie nicht konfigurieren, wird von Microsoft Edge standardmäßig die Verwendung von nativen Messaginghosts auf Benutzerebene zugelassen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: NativeMessagingUserLevelHosts
  - Gruppenrichtlinienname: Native Messaginghosts auf Benutzerebene zulassen (ohne Administratorberechtigungen installiert)
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Natives Messaging
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: NativeMessagingUserLevelHosts
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: NativeMessagingUserLevelHosts
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ## Proxyserver policies

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ProxyBypassList
  #### Proxy-Umgehungsregeln konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Definiert eine Liste von Hosts, für die Microsoft Edge jeden Proxy umgeht.

Diese Richtlinie wird nur angewendet, wenn Sie 'Feste Proxy-Server verwenden' in der Richtlinie [ProxyMode](#proxymode) ausgewählt haben. Aktivieren oder konfigurieren Sie diese Richtlinie nicht, wenn Sie einen anderen Modus für die Konfiguration von Proxy-Richtlinien ausgewählt haben.

Wenn Sie diese Richtlinie aktivieren, können Sie eine Liste von Hosts erstellen, für die Microsoft Edge keinen Proxy verwendet.

Wenn Sie diese Richtlinie nicht konfigurieren, wird keine Liste der Hosts erstellt, für die Microsoft Edge einen Proxy umgeht. Konfigurieren Sie diese Richtlinie nicht, wenn Sie eine andere Methode zum Festlegen von Proxy-Richtlinien angegeben haben.

Detaillierte Beispiele finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ProxyBypassList
  - Gruppenrichtlinienname: Proxy-Umgehungsregeln konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Proxyserver
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ProxyBypassList
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"https://www.contoso.com, https://www.fabrikam.com"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ProxyBypassList
  - Beispielwert:
``` xml
<string>https://www.contoso.com, https://www.fabrikam.com</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ProxyMode
  #### Proxyservereinstellungen konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Diese Richtlinie gibt die Proxyservereinstellungen an, die von Microsoft Edge verwendet werden. Wenn Sie diese Richtlinie aktivieren, können Benutzer die Proxyeinstellungen nicht ändern.

Wenn Sie sich dafür entscheiden, niemals einen Proxyserver zu verwenden und sich immer direkt zu verbinden, werden alle anderen Optionen ignoriert.

Wenn Sie sich für die Verwendung von Systemproxyeinstellungen entscheiden, werden alle anderen Optionen ignoriert.

Wenn Sie die automatische Erkennung des Proxyservers wählen, werden alle anderen Optionen ignoriert.

Wenn Sie den festen Serverproxymodus wählen, können Sie weitere Optionen in [ProxyServer](#proxyserver) und “Kommagetrennte Liste der Proxy-Umgehungsregeln” angeben.

Wenn Sie sich für die Verwendung eines PAC-Proxyskripts entscheiden, müssen Sie die URL zum Skript unter “URL für eine proxy.pac-Datei” angeben.

Detaillierte Beispiele finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)

Wenn Sie diese Richtlinie aktivieren, ignoriert Microsoft Edge alle proxybezogenen Optionen, die über die Befehlszeile angegeben werden.

Wenn Sie diese Richtlinie nicht konfigurieren, können Benutzer die Proxyeinstellungen selbst auswählen.

Zuordnung der Richtlinienoptionen:

* ProxyDisabled (direct) = Niemals einen Proxy verwenden

* ProxyAutoDetect (auto_detect) = Proxyeinstellungen automatisch erkennen

* ProxyPacScript (pac_script) = PAC-Proxyskript verwenden

* ProxyFixedServers (fixed_servers) = Feste Proxyserver verwenden

* ProxyUseSystem (system) = Systemproxyeinstellungen verwenden

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ProxyMode
  - Gruppenrichtlinienname: Proxyservereinstellungen konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Proxyserver
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ProxyMode
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"direct"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ProxyMode
  - Beispielwert:
``` xml
<string>direct</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ProxyPacUrl
  #### Proxy-PAC-Datei-URL festlegen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt die URL für eine PAC-Datei (Proxy Auto-Config) an.

Diese Richtlinie wird nur angewendet, wenn Sie 'Ein PAC-Proxyskript verwenden' in der Richtlinie [ProxyMode](#proxymode) verwenden. Wenn Sie einen anderen Modus für die Konfiguration von Proxy-Richtlinien ausgewählt haben, aktivieren oder konfigurieren Sie diese Richtlinie nicht.

Wenn Sie diese Richtlinie aktivieren, können Sie die URL für eine PAC-Datei angeben, die definiert, wie der Browser automatisch den geeigneten Proxy-Server für den Abruf einer bestimmten Website auswählt.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird keine PAC-Datei angegeben. Konfigurieren Sie diese Richtlinie nicht, wenn Sie eine andere Methode zum Festlegen von Proxy-Richtlinien angegeben haben.

Detaillierte Beispiele finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ProxyPacUrl
  - Gruppenrichtlinienname: Proxy-PAC-Datei-URL festlegen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Proxyserver
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ProxyPacUrl
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"https://internal.contoso.com/example.pac"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ProxyPacUrl
  - Beispielwert:
``` xml
<string>https://internal.contoso.com/example.pac</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ProxyServer
  #### Adresse oder URL des Proxyservers konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt die URL für den Proxy-Server an.

Diese Richtlinie wird nur angewendet, wenn Sie 'Feste Proxy-Server verwenden' [ProxyMode](#proxymode) verwenden. Wenn Sie einen anderen Modus für die Konfiguration von Proxy-Richtlinien ausgewählt haben, aktivieren oder konfigurieren Sie diese Richtlinie nicht.

Wenn Sie diese Richtlinie aktivieren, wird der durch diese Richtlinie konfigurierte Proxy-Server für alle URLs verwendet.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, können Benutzer in diesem Proxy-Modus ihre eigenen Proxy-Einstellungen wählen. Konfigurieren Sie diese Richtlinie nicht, wenn Sie eine andere Methode zum Festlegen von Proxy-Richtlinien angegeben haben.

Weitere Optionen und detaillierte Beispiele finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ProxyServer
  - Gruppenrichtlinienname: Adresse oder URL des Proxyservers konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Proxyserver
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ProxyServer
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"123.123.123.123:8080"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ProxyServer
  - Beispielwert:
``` xml
<string>123.123.123.123:8080</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ProxySettings
  #### Proxyeinstellungen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Konfiguriert die Proxy-Einstellungen für Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, ignoriert Microsoft Edge alle proxybezogenen Optionen, die über die Befehlszeile angegeben werden.

Wenn Sie diese Richtlinie nicht konfigurieren, können Benutzer ihre eigenen Proxy-Einstellungen auswählen.

Diese Richtlinie hat Vorrang vor den folgenden Einzelrichtlinien:

[ProxyMode](#proxymode)
[ProxyPacUrl](#proxypacurl)
[ProxyServer](#proxyserver)
[ProxyBypassList](#proxybypasslist)

Im Feld ProxyMode können Sie den Proxy-Server angeben, der von Microsoft Edge verwendet wird, und verhindern, dass Benutzer Proxy-Einstellungen ändern.

Das Feld ProxyPacUrl enthält eine URL zu einer Proxy-PAC-Datei.

Das Feld ProxyServer enthält eine URL für den Proxy-Server.

Das Feld ProxyBypassList enthält eine Liste mit Proxy-Host, die Microsoft Edge umgeht.

Wenn Sie den Wert' direct' für 'ProxyMode' wählen, wird kein Proxy verwendet, und alle anderen Felder werden ignoriert.

Wenn Sie den Wert 'system' für 'ProxyMode' wählen, wird der Proxy des Systems verwendet, und alle anderen Felder werden ignoriert.

Wenn Sie den Wert 'auto_detect' für 'ProxyMode' wählen, werden alle anderen Felder ignoriert.

Wenn Sie den Wert 'fixed_server' für 'ProxyMode' wählen, werden die Felder 'ProxyServer' und ProxyBypassList' verwendet.

Wenn Sie den Wert 'pac_script' als 'ProxyMode' wählen, werden die Felder ProxyPacUrl' und ProxyBypassList' verwendet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Wörterbuch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ProxySettings
  - Gruppenrichtlinienname: Proxyeinstellungen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Proxyserver
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ProxySettings
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {
  "ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", 
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ProxySettings
  - Beispielwert:
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
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ## SmartScreen-Einstellungen policies

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PreventSmartScreenPromptOverride
  #### Umgehung der Microsoft Defender SmartScreen-Aufforderungen für Websites verhindern
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Mit dieser Richtlinieneinstellung können Sie festlegen, ob Benutzer die Microsoft Defender SmartScreen-Warnungen im Zusammenhang mit potenziell schädlichen Websites überschreiben können.

Wenn Sie diese Einstellung aktivieren, können Benutzer Microsoft Defender SmartScreen-Warnungen nicht ignorieren und die Website nicht besuchen.

Wenn Sie diese Einstellung deaktivieren oder nicht konfigurieren, können Benutzer Microsoft Defender SmartScreen-Warnungen ignorieren und die Website besuchen.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PreventSmartScreenPromptOverride
  - Gruppenrichtlinienname: Umgehung der Microsoft Defender SmartScreen-Aufforderungen für Websites verhindern
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/SmartScreen-Einstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: PreventSmartScreenPromptOverride
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: PreventSmartScreenPromptOverride
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PreventSmartScreenPromptOverrideForFiles
  #### Umgehung der Microsoft Defender SmartScreen-Warnungen für Downloads verhindern
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 77 oder höher
  - Unter macOS seit Version 79 oder höher

  #### Beschreibung
  Mit dieser Richtlinieneinstellung können Sie festlegen, ob Benutzer Microsoft Defender SmartScreen-Warnungen im Zusammenhang mit nicht verifizierten Downloads überschreiben können.

Wenn Sie diese Richtlinie aktivieren, können Benutzer in Ihrer Organisation Microsoft Defender SmartScreen-Warnungen nicht ignorieren und die nicht verifizierten Downloads nicht abschließen.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, können Benutzer Microsoft Defender SmartScreen-Warnungen ignorieren und nicht verifizierte Downloads durchführen.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PreventSmartScreenPromptOverrideForFiles
  - Gruppenrichtlinienname: Umgehung der Microsoft Defender SmartScreen-Warnungen für Downloads verhindern
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/SmartScreen-Einstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: PreventSmartScreenPromptOverrideForFiles
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: PreventSmartScreenPromptOverrideForFiles
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SmartScreenAllowListDomains
  #### Konfigurieren Sie die Liste der Domänen, für die Microsoft Defender SmartScreen keine Warnungen auslöst.
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Konfigurieren Sie die Liste der für Microsoft Defender SmartScreen vertrauenswürdigen Domänen. Das bedeutet:
Wenn die Quell-URLs diesen Domänen entsprechen, führt Microsoft Defender SmartScreen keine Prüfung auf potenziell schädliche Ressourcen wie Phishingsoftware und andere Schadsoftware durch.
Der Microsoft Defender SmartScreen-Downloadschutzdienst überprüft keine Downloads, die in diesen Domänen gehostet werden.

Wenn Sie diese Richtlinie aktivieren, vertraut Microsoft Defender SmartScreen diesen Domänen.
Wenn Sie diese Richtlinie deaktivieren oder nicht festlegen, wird auf alle Ressourcen der Microsoft Defender SmartScreen-Standardschutz angewendet.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.
Beachten Sie außerdem, dass diese Richtlinie nicht angewendet wird, wenn Ihre Organisation Microsoft Defender Advanced Threat Protection aktiviert hat. In diesem Fall müssen stattdessen die Listen “Zulassen” und “Blockieren” in Microsoft Defender Security Center konfiguriert werden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SmartScreenAllowListDomains
  - Gruppenrichtlinienname: Konfigurieren Sie die Liste der Domänen, für die Microsoft Defender SmartScreen keine Warnungen auslöst.
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/SmartScreen-Einstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\2 = "myuniversity.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SmartScreenAllowListDomains
  - Beispielwert:
``` xml
<array>
  <string>mydomain.com</string>
  <string>myuniversity.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SmartScreenEnabled
  #### Microsoft Defender SmartScreen konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Mit dieser Richtlinieneinstellung können Sie festlegen, ob Microsoft Defender SmartScreen aktiviert werden soll. Microsoft Defender SmartScreen gibt Warnmeldungen aus, um Ihre Benutzer vor potenziellen Phishing-Versuchen und vor potenzieller Schadsoftware zu schützen. Standardmäßig ist Microsoft Defender SmartScreen aktiviert.

Wenn Sie diese Einstellung aktivieren, wird Microsoft Defender SmartScreen aktiviert.

Wenn Sie diese Einstellung deaktivieren, wird Microsoft Defender SmartScreen deaktiviert.

  Wenn Sie diese Richtlinie nicht konfigurieren, können die Benutzer entscheiden, ob Sie Microsoft Defender SmartScreen nutzen wollen.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SmartScreenEnabled
  - Gruppenrichtlinienname: Microsoft Defender SmartScreen konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/SmartScreen-Einstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/SmartScreen-Einstellungen
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: SmartScreenEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SmartScreenEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SmartScreenForTrustedDownloadsEnabled
  #### Überprüfung von Downloads von vertrauenswürdigen Quellen durch Microsoft Defender SmartScreen erzwingen
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 78 oder höher

  #### Beschreibung
  Mit dieser Richtlinieneinstellung können Sie konfigurieren, ob Microsoft Defender SmartScreen die Downloadzuverlässigkeit einer vertrauenswürdigen Quelle überprüft.

  Wenn Sie diese Einstellung aktivieren oder nicht konfigurieren, überprüft Microsoft Defender SmartScreen die Downloadzuverlässigkeit unabhängig von der Quelle.

  Wenn Sie diese Einstellung deaktivieren, überprüft Microsoft Defender SmartScreen die Downloadzuverlässigkeit beim Herunterladen von einer zuverlässigen Quelle nicht.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SmartScreenForTrustedDownloadsEnabled
  - Gruppenrichtlinienname: Überprüfung von Downloads von vertrauenswürdigen Quellen durch Microsoft Defender SmartScreen erzwingen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/SmartScreen-Einstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/SmartScreen-Einstellungen
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: SmartScreenForTrustedDownloadsEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SmartScreenPuaEnabled
  #### Microsoft Defender SmartScreen konfigurieren, um potenziell unerwünschte Apps zu blockieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 80 oder höher

  #### Beschreibung
  Mit dieser Richtlinieneinstellung können Sie konfigurieren, ob die Blockierung potenziell unerwünschter Apps in Microsoft Defender SmartScreen aktiviert werden soll. Die Blockierung potenziell unerwünschter Apps in Microsoft Defender SmartScreen schützt Benutzer mithilfe von Warnmeldungen vor Adware, Coin Mining, Bundleware und anderen fragwürdigen Apps, die von Websites gehostet werden. Die Blockierung potenziell unerwünschter Apps in Microsoft Defender SmartScreen ist standardmäßig deaktiviert.

  Wenn Sie diese Einstellung aktivieren, wird die Blockierung potenziell unerwünschter Apps in Microsoft Defender SmartScreen aktiviert.

  Wenn Sie diese Einstellung deaktivieren, wird die Blockierung potenziell unerwünschter Apps in Microsoft Defender SmartScreen deaktiviert.

  Wenn Sie diese Einstellung nicht konfigurieren, können Benutzer wählen, ob Sie die Blockierung potenziell unerwünschter Apps in Microsoft Defender SmartScreen verwenden möchten.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SmartScreenPuaEnabled
  - Gruppenrichtlinienname: Microsoft Defender SmartScreen konfigurieren, um potenziell unerwünschte Apps zu blockieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/SmartScreen-Einstellungen
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/SmartScreen-Einstellungen
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: SmartScreenPuaEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SmartScreenPuaEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ## Standardsuchanbieter policies

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultSearchProviderEnabled
  #### Standardsuchanbieter aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Ermöglicht die Verwendung eines Standardsuchanbieters.

  Wenn Sie diese Richtlinie aktivieren, kann ein Benutzer nach einem Begriff suchen, indem er ihn in die Adressleiste eingibt (vorausgesetzt, bei der Eingabe handelt es sich nicht um eine URL)

  Sie können den zu verwendenden Standardsuchanbieter angeben, indem Sie die restlichen Standardsuchrichtlinien aktivieren. Wenn Sie diese leer lassen (also nicht konfigurieren), kann der Benutzer den Standardanbieter auswählen.

  Wenn Sie diese Richtlinie deaktivieren, kann der Benutzer nicht mithilfe der Adressleiste suchen.

  Wenn Sie diese Richtlinie aktivieren oder deaktivieren, kann sie von Benutzern nicht geändert oder überschrieben werden.

  Wenn Sie diese Richtlinie nicht konfigurieren, wird der Standardsuchanbieter aktiviert, und der Benutzer kann den Standardsuchanbieter auswählen und die Suchanbieterliste festlegen.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.

  Ab Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultSearchProviderEnabled
  - Gruppenrichtlinienname: Standardsuchanbieter aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Standardsuchanbieter
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Standardsuchanbieter
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: DefaultSearchProviderEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultSearchProviderEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultSearchProviderEncodings
  #### Standardsuchanbieter-Codierungen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt die vom Suchanbieter unterstützten Zeichenkodierungen an. Kodierungen sind Codepage-Namen wie UTF-8, GB2312 und ISO-8859-1. Sie werden in der angegebenen Reihenfolge ausprobiert.

Diese Richtlinie ist optional. Ist sie nicht konfiguriert, wird der Standard UTF-8 verwendet.

Diese Richtlinie wird nur angewendet, wenn Sie die Richtlinien [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) und [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) aktivieren.

Ab Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen. Wenn der Benutzer bereits einen standardmäßigen Suchanbieter festgelegt hat, wird der von dieser empfohlenen Richtlinie konfigurierte Standardsuchanbieter nicht zur Liste der Suchanbieter hinzugefügt, aus denen der Benutzer auswählen kann. Wenn dies das gewünschte Verhalten ist, verwenden Sie die Richtlinie [ManagedSearchEngines](#managedsearchengines).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultSearchProviderEncodings
  - Gruppenrichtlinienname: Standardsuchanbieter-Codierungen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Standardsuchanbieter
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Standardsuchanbieter
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen\DefaultSearchProviderEncodings
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\1 = "UTF-8"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\2 = "UTF-16"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\3 = "GB2312"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\4 = "ISO-8859-1"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultSearchProviderEncodings
  - Beispielwert:
``` xml
<array>
  <string>UTF-8</string>
  <string>UTF-16</string>
  <string>GB2312</string>
  <string>ISO-8859-1</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultSearchProviderImageURL
  #### Gibt das Bildsuchfeature für den standardmäßigen Suchanbieter an
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt die URL der Suchmaschine an, die für die Bildsuche verwendet wird. Suchanfragen werden mit der Methode GET gesendet.

Diese Richtlinie ist optional. Wenn Sie es nicht konfigurieren, ist die Bildsuche nicht verfügbar.

Geben Sie die URL der Bing-Bildsuche wie folgt an:
'{bing:baseURL}images/detail/search?iss=sbiupload&FORM=ANCMS1#enterInsights'.

Geben Sie die URL der Google-Bildsuche wie folgt an: '{google:baseURL}searchbyimage/upload'.

In der Richtlinie [DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams) finden Sie Informationen zum Konfigurieren der Bildsuche.

Diese Richtlinie wird nur angewendet, wenn Sie die Richtlinien [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) und [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) aktivieren.

Ab Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen. Wenn der Benutzer bereits einen standardmäßigen Suchanbieter festgelegt hat, wird der von dieser empfohlenen Richtlinie konfigurierte Standardsuchanbieter nicht zur Liste der Suchanbieter hinzugefügt, aus denen der Benutzer auswählen kann. Wenn dies das gewünschte Verhalten ist, verwenden Sie die Richtlinie [ManagedSearchEngines](#managedsearchengines).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultSearchProviderImageURL
  - Gruppenrichtlinienname: Gibt das Bildsuchfeature für den standardmäßigen Suchanbieter an
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Standardsuchanbieter
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Standardsuchanbieter
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: DefaultSearchProviderImageURL
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"https://search.contoso.com/searchbyimage/upload"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultSearchProviderImageURL
  - Beispielwert:
``` xml
<string>https://search.contoso.com/searchbyimage/upload</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultSearchProviderImageURLPostParams
  #### Parameter für eine Bild-URL, die POST verwendet
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Wenn Sie diese Richtlinie aktivieren, werden die Parameter angegeben, die bei der Durchführung einer Bildsuche mit POST verwendet werden. Die Richtlinie besteht aus durch Kommas getrennte Namen/Wertpaare. Wenn ein Wert ein Vorlagenparameter ist, wie im vorherigen Beispiel {imageThumbnail}, wird er durch echte Miniaturbilddaten ersetzt. Diese Richtlinie wird nur angewendet, wenn Sie die Richtlinien “[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)” und “[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)” aktivieren.

  Geben Sie die URL-Postparameter für die Bildsuche von Bing an als:
  'imageBin={google:imageThumbnailBase64}'.

  Geben Sie die URL-Postparameter für die Bildsuche von Google an als:
  'encoded_image={google:imageThumbnail},image_url={google:imageURL},sbisrc={google:imageSearchSource},original_width={google:imageOriginalWidth},original_height={google:imageOriginalHeight}'.

Wenn Sie diese Richtlinie nicht festlegen, werden Suchanforderungen für Bilder mithilfe der GET-Methode gesendet.

  Ab Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen. Wenn der Benutzer bereits einen standardmäßigen Suchanbieter festgelegt hat, wird der von dieser empfohlenen Richtlinie konfigurierte Standardsuchanbieter nicht zur Liste der Suchanbieter hinzugefügt, aus denen der Benutzer auswählen kann. Wenn dies das gewünschte Verhalten ist, verwenden Sie die Richtlinie “[ManagedSearchEngines](#managedsearchengines)”.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultSearchProviderImageURLPostParams
  - Gruppenrichtlinienname: Parameter für eine Bild-URL, die POST verwendet
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Standardsuchanbieter
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Standardsuchanbieter
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: DefaultSearchProviderImageURLPostParams
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"content={imageThumbnail},url={imageURL},sbisrc={SearchSource}"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultSearchProviderImageURLPostParams
  - Beispielwert:
``` xml
<string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultSearchProviderKeyword
  #### Stichwort für Standardsuchanbieter
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt das Schlüsselwort an, das die Verknüpfung in der Adressleiste ist, mit der die Suche nach diesem Anbieter ausgelöst wird.

       Diese Richtlinie ist optional. Wird sie nicht konfiguriert, aktiviert kein Schlüsselwort den Suchanbieter.

       Diese Richtlinie wird nur angewendet, wenn Sie die Richtlinien [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) und [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) aktivieren.

Ab Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen. Wenn der Benutzer bereits einen standardmäßigen Suchanbieter festgelegt hat, wird der von dieser empfohlenen Richtlinie konfigurierte Standardsuchanbieter nicht zur Liste der Suchanbieter hinzugefügt, aus denen der Benutzer auswählen kann. Wenn dies das gewünschte Verhalten ist, verwenden Sie die Richtlinie [ManagedSearchEngines](#managedsearchengines).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultSearchProviderKeyword
  - Gruppenrichtlinienname: Stichwort für Standardsuchanbieter
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Standardsuchanbieter
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Standardsuchanbieter
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: DefaultSearchProviderKeyword
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"mis"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultSearchProviderKeyword
  - Beispielwert:
``` xml
<string>mis</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultSearchProviderName
  #### Standardsuchanbietername
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt den Namen des Standardsuchanbieters an.

 Wenn Sie diese Richtlinie aktivieren, legen Sie den Namen des Standardsuchanbieters fest.

 Wenn Sie diese Richtlinie nicht aktivieren oder leer lassen, wird der in der Such-URL angegebene Hostname verwendet.

 'DefaultSearchProviderName' sollte auf einen vom Unternehmen zugelassenen verschlüsselten Suchanbieter festgelegt sein, der dem in DTBC-0008 eingestellten verschlüsselten Suchanbieter entspricht. Diese Richtlinie wird nur angewendet, wenn Sie die Richtlinien [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) und [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) aktivieren.

Ab Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen. Wenn der Benutzer bereits einen standardmäßigen Suchanbieter festgelegt hat, wird der von dieser empfohlenen Richtlinie konfigurierte Standardsuchanbieter nicht zur Liste der Suchanbieter hinzugefügt, aus denen der Benutzer auswählen kann. Wenn dies das gewünschte Verhalten ist, verwenden Sie die Richtlinie [ManagedSearchEngines](#managedsearchengines).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultSearchProviderName
  - Gruppenrichtlinienname: Standardsuchanbietername
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Standardsuchanbieter
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Standardsuchanbieter
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: DefaultSearchProviderName
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"My Intranet Search"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultSearchProviderName
  - Beispielwert:
``` xml
<string>My Intranet Search</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultSearchProviderSearchURL
  #### Such-URL für den Standardsuchanbieter
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt die URL der Suchmaschine an, die für eine Standardsuche verwendet wird. Die URL enthält die Zeichenfolge '{searchTerms}'', die bei der Abfrage durch die Begriffe ersetzt wird, nach denen der Benutzer sucht.

Geben Sie die Such-URL von Bing an als:

'{bing:baseURL}search?q={searchTerms}'.

Geben Sie die Such-URL von Google an als:: '{google:baseURL}search?q={searchTerms}&{google:RLZ}{google:originalQueryForSuggestion}{google:assistedQueryStats}{google:searchFieldtrialParameter}{google:searchClient}{google:sourceId}ie={inputEncoding}'.

Diese Richtlinie ist erforderlich, wenn Sie die Richtlinie [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) aktivieren. Wenn Sie diese Richtlinie nicht aktivieren, wird sie ignoriert.

Ab Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen. Wenn der Benutzer bereits einen standardmäßigen Suchanbieter festgelegt hat, wird der von dieser empfohlenen Richtlinie konfigurierte Standardsuchanbieter nicht zur Liste der Suchanbieter hinzugefügt, aus denen der Benutzer auswählen kann. Wenn dies das gewünschte Verhalten ist, verwenden Sie die Richtlinie [ManagedSearchEngines](#managedsearchengines).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultSearchProviderSearchURL
  - Gruppenrichtlinienname: Such-URL für den Standardsuchanbieter
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Standardsuchanbieter
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Standardsuchanbieter
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: DefaultSearchProviderSearchURL
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"https://search.contoso.com/search?q={searchTerms}"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultSearchProviderSearchURL
  - Beispielwert:
``` xml
<string>https://search.contoso.com/search?q={searchTerms}</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultSearchProviderSuggestURL
  #### Standard-Suchanbieter-URL für Vorschläge
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt die URL für die Suchmaschine an, die verwendet wird, um Suchvorschläge bereitzustellen. Die URL enthält die Zeichenfolge '{searchTerms}', die zur Abfragezeit durch den bisher vom Benutzer eingegebenen Text ersetzt wird.

 Diese Richtlinie ist optional. Wird sie nicht konfiguriert, werden den Benutzern keine Suchvorschläge angezeigt, sondern Vorschläge aus ihrem Browserverlauf und ihren Favoriten.

 Die von Bing vorgeschlagene URL kann wie folgt angegeben werden:

 '{bing:baseURL}qbox?query={searchTerms}'.

 Die von Google vorgeschlagene URL kann wie folgt angegeben werden: '{google:baseURL}complete/search?output=chrome&q={searchTerms}'.

 Diese Richtlinie wird nur angewendet, wenn Sie die Richtlinien [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) und [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) aktivieren.

Ab Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen. Wenn der Benutzer bereits einen standardmäßigen Suchanbieter festgelegt hat, wird der von dieser empfohlenen Richtlinie konfigurierte Standardsuchanbieter nicht zur Liste der Suchanbieter hinzugefügt, aus denen der Benutzer auswählen kann. Wenn dies das gewünschte Verhalten ist, verwenden Sie die Richtlinie [ManagedSearchEngines](#managedsearchengines).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultSearchProviderSuggestURL
  - Gruppenrichtlinienname: Standard-Suchanbieter-URL für Vorschläge
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Standardsuchanbieter
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Standardsuchanbieter
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: DefaultSearchProviderSuggestURL
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"https://search.contoso.com/suggest?q={searchTerms}"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultSearchProviderSuggestURL
  - Beispielwert:
``` xml
<string>https://search.contoso.com/suggest?q={searchTerms}</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NewTabPageSearchBox
  #### Konfigurieren der Suchfeld-Oberfläche für die neue Registerkartenseite
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 85 oder höher

  #### Beschreibung
  Sie können das Suchfeld für die neue Registerkartenseite konfigurieren, um "Suchfeld (empfohlen)" oder "Adressleiste" zu verwenden, um auf neuen Registerkarten zu suchen. Diese Richtlinie funktioniert nur, wenn Sie für die Suchmaschine einen anderen Wert als “Bing” angeben, indem Sie die folgenden zwei Richtlinien festlegen: “[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)” und “[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)”.

 Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren und:

– die Standardsuchmaschine der Adressleiste Bing ist, verwendet die neue Registerkartenseite das Suchfeld, um auf neuen Registerkarten zu suchen.
– die Standardsuchmaschine nicht Bing ist, wird den Benutzern eine zusätzliche Auswahl angeboten ("Adressleiste" verwenden), wenn Sie auf neuen Registerkarten suchen.


Wenn Sie diese Richtlinie aktivieren und festlegen auf:

– "Suchfeld (empfohlen)" (“Bing”), verwendet die neue Registerkartenseite das Suchfeld, um auf neuen Registerkarten zu suchen.
–"Adressleiste" ("umleiten"), verwendet das Suchfeld der neuen Registerkartenseite die Adressleiste, um auf neuen Registerkarten zu suchen.

Zuordnung der Richtlinienoptionen:

* bing (bing) = Suchfeld (Empfohlen)

* redirect (redirect) = Adressleiste

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: NewTabPageSearchBox
  - Gruppenrichtlinienname: Konfigurieren der Suchfeld-Oberfläche für die neue Registerkartenseite
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Standardsuchanbieter
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Standardsuchanbieter
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: NewTabPageSearchBox
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"bing"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: NewTabPageSearchBox
  - Beispielwert:
``` xml
<string>bing</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ## Start&comma; Startseite und neue Tabseite policies

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### HomepageIsNewTabPage
  #### Neue Tabseite als Startseite festlegen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Konfiguriert die Standard-Startseite in Microsoft Edge. Sie können die Startseite auf eine von Ihnen angegebene URL festlegen oder auf "Neue Tabseite".

  Wenn Sie diese Richtlinie aktivieren, wird die Seite “Neue Registerkarte“ immer als Startseite verwendet, und der URL-Pfad der Startseite wird ignoriert.

  Wenn Sie diese Richtlinie deaktivieren, kann die Startseite des Benutzers nicht die Seite “Neue Registerkarte“ sein, es sei denn, die URL ist auf “edge://newtab” festgelegt.

  Wenn die Richtlinie nicht konfiguriert ist, können Benutzer auswählen, ob die Seite “Neue Registerkarte” ihre Startseite sein soll.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: HomepageIsNewTabPage
  - Gruppenrichtlinienname: Neue Tabseite als Startseite festlegen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Start, Startseite und neue Tabseite
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Start, Startseite und neue Tabseite
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: HomepageIsNewTabPage
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: HomepageIsNewTabPage
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### HomepageLocation
  #### Homepage-URL konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Konfiguriert die standardmäßige URL der Homepage in Microsoft Edge.

  Die Startseite ist die Seite, die durch die gleichnamige Schaltfläche geöffnet wird. Die Seiten, die sich beim Start öffnen, werden durch die Richtlinien [RestoreOnStartup](#restoreonstartup) gesteuert.

  Sie können entweder eine URL hier eingeben oder die Startseite so einstellen, dass der neue Tab geöffnet wird. Wenn Sie die zweite Möglichkeit wählen, wird diese Richtlinie nicht wirksam.

  Wenn Sie diese Richtlinie aktivieren, können Benutzer ihre Homepage-URL nicht ändern, aber sie können den neuen Tab als Startseite verwenden.

  Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, können Benutzer ihre eigene Homepage wählen, solange die Richtlinie [HomepageIsNewTabPage](#homepageisnewtabpage) nicht aktiviert ist.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: HomepageLocation
  - Gruppenrichtlinienname: Homepage-URL konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Start, Startseite und neue Tabseite
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Start, Startseite und neue Tabseite
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: HomepageLocation
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"https://www.contoso.com"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: HomepageLocation
  - Beispielwert:
``` xml
<string>https://www.contoso.com</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NewTabPageAllowedBackgroundTypes
  #### Hintergrundtypen konfigurieren, die für das Seitenlayout des neuen Tabs zulässig sind
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 86 oder höher

  #### Beschreibung
  Sie können konfigurieren, welche Arten von Hintergrundbildern auf dem neuen Registerkartenlayout in Microsoft Edge zulässig sind.

Wenn Sie diese Richtlinie nicht konfigurieren, werden alle Hintergrundbildtypen auf der neuen Registerkarte aktiviert.

Zuordnung der Richtlinienoptionen:

* DisableImageOfTheDay (1) = Täglichen Hintergrundbildtyp deaktivieren

* DisableCustomImage (2) = Benutzerdefinierten Hintergrundbildtyp deaktivieren

* DisableAll (3) = Alle Hintergrundbildtypen deaktivieren

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: NewTabPageAllowedBackgroundTypes
  - Gruppenrichtlinienname: Hintergrundtypen konfigurieren, die für das Seitenlayout des neuen Tabs zulässig sind
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Start, Startseite und neue Tabseite
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: NewTabPageAllowedBackgroundTypes
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000002
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: NewTabPageAllowedBackgroundTypes
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NewTabPageCompanyLogo
  #### Neues Firmenlogo auf der Registerkartenseite festlegen (veraltet)
  >VERALTET: Diese Richtlinie ist veraltet. Sie wird gegenwärtig noch unterstützt, aber in einem zukünftigen Release ausgemustert.
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 79 oder höher

  #### Beschreibung
  Diese Richtlinie ist veraltet, da sie nicht wie erwartet funktioniert. Wir empfehlen Ihnen, sie nicht zu verwenden. Sie funktioniert in Microsoft Edge Version 86 nicht.

Gibt das Firmenlogo an, das auf der neuen Tabseite in Microsoft Edge verwendet werden soll.

Die Richtlinie muss als Zeichenfolge konfiguriert werden, die die Logos im JSON-Format ausdrückt. Beispiel: { "default_logo": { "url": "https://www.contoso.com/logo.png", "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29" }, "light_logo": { "url": "https://www.contoso.com/light_logo.png", "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737" } }

Sie konfigurieren diese Richtlinie durch Angeben der URL, von der Microsoft Edge das Logo und den zugehörigen kryptographischen Hash (SHA-256) herunterladen kann, der zur Überprüfung der Integrität des Downloads verwendet wird. Das Logo muss im PNG- oder SVG-Format vorliegen und darf maximal 16 MB groß sein. Das Logo wird heruntergeladen und zwischengespeichert, und es wird erneut heruntergeladen, wenn sich die URL oder der Hash ändern. Die URL muss ohne jegliche Authentifizierung zugänglich sein.

Die Datei “default_logo“ ist erforderlich und wird verwendet, wenn kein Hintergrundbild vorhanden ist. Wenn “light_logo“ angegeben ist, wird es verwendet, wenn die neue Registerkartenseite des Benutzers ein Hintergrundbild besitzt. Wir empfehlen ein horizontales Logo mit transparentem Hintergrund, das linksbündig ausgerichtet und vertikal zentriert ist. Das Logo muss eine Mindesthöhe von 32 Pixeln und ein Seitenverhältnis zwischen 1:1 und 4:1 aufweisen. “default_logo“ muss sich angemessen von einem weißen/schwarzen Hintergrund abheben, während sich “light_logo“ angemessen von einem Hintergrundbild abheben muss.

Wenn Sie diese Richtlinie aktivieren, lädt Microsoft Edge die angegebenen Logos herunter und zeigt sie auf der neuen Registerkartenseite an. Benutzer können die Logos nicht überschreiben oder ausblenden.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, zeigt Microsoft Edge auf der neuen Registerkartenseite entweder kein Firmenlogo oder ein Microsoft-Logo an.

Hilfe zum Ermitteln des SHA-256-Hash finden Sie unter “https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/get-filehash“.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Wörterbuch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: NewTabPageCompanyLogo
  - Gruppenrichtlinienname: Neues Firmenlogo auf der Registerkartenseite festlegen (veraltet)
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Start, Startseite und neue Tabseite
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: NewTabPageCompanyLogo
  - Werttyp: REG_SZ
  ##### Beispielwert:
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


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: NewTabPageCompanyLogo
  - Beispielwert:
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
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NewTabPageHideDefaultTopSites
  #### Die Standardwebsites der obersten Ebene auf der neuen Tabseite ausblenden
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Blendet die Standardwebsites auf der Tabseite "Neu" in Microsoft Edge aus.

Wenn Sie diese Richtlinie auf "true" festlegen, werden die Standardkacheln der Website der obersten Ebene ausgeblendet.

Wenn Sie diese Richtlinie auf "false" festlegen oder nicht konfigurieren, bleiben die Standardkacheln für die Website der obersten Ebene sichtbar.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: NewTabPageHideDefaultTopSites
  - Gruppenrichtlinienname: Die Standardwebsites der obersten Ebene auf der neuen Tabseite ausblenden
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Start, Startseite und neue Tabseite
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: NewTabPageHideDefaultTopSites
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: NewTabPageHideDefaultTopSites
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NewTabPageLocation
  #### URL für die neue Tabseite konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Konfiguriert die Standard-URL für die neue Registerkartenseite.

  Diese Richtlinie bestimmt die Seite, die geöffnet wird, wenn neue Registerkarten erstellt werden (auch wenn neue Fenster geöffnet werden). Sie wirkt sich auch auf die Startseite aus, wenn diese in der neuen Registerkarte geöffnet werden soll.

  Diese Richtlinie bestimmt nicht, welche Seite beim Start geöffnet wird. Dies wird durch die Richtlinie [RestoreOnStartup](#restoreonstartup) gesteuert. Sie wirkt sich auch nicht auf die Startseite aus, wenn diese in der neuen Registerkarte geöffnet werden soll.

  Wenn Sie diese Richtlinie nicht konfigurieren, wird die standardmäßige neue Registerkarte verwendet.

  Wenn Sie diese Richtlinie *und* die Richtlinie [NewTabPageSetFeedType](#newtabpagesetfeedtype) konfigurieren, hat diese Richtlinie Vorrang.

  Wenn eine ungültige URL angegeben ist, wird die neue Registerkarte “about://blank” geöffnet.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: NewTabPageLocation
  - Gruppenrichtlinienname: URL für die neue Tabseite konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Start, Startseite und neue Tabseite
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Start, Startseite und neue Tabseite
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: NewTabPageLocation
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"https://www.fabrikam.com"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: NewTabPageLocation
  - Beispielwert:
``` xml
<string>https://www.fabrikam.com</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NewTabPageManagedQuickLinks
  #### Schnelllinks für neue Tabs festlegen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 79 oder höher

  #### Beschreibung
  Microsoft Edge zeigt auf der neuen Tabseite standardmäßig Quicklinks aus von Benutzern hinzugefügten Verknüpfungen und zu den beliebtesten Websites basierend auf dem Browserverlauf an. Mit dieser Richtlinie können Sie auf der neuen Tabseite bis zu drei Quicklink-Kacheln konfigurieren, die als JSON-Objekt ausgedrückt werden:

[ { "url": "https://www.contoso.com", "title": "Contoso Portal", "pinned": true/false }, ... ]

Das Feld „url“ ist erforderlich; „title“ und „pinned“ sind optional. Wenn „title“ nicht angegeben ist, wird die URL als Standardtitel verwendet. Wenn „pinned“ nicht angegeben wird, ist der Standardwert „false“.

Microsoft Edge stellt diese in der aufgelisteten Reihenfolge von links nach rechts dar, wobei alle angehefteten Kacheln vor nicht angehefteten Kacheln angezeigt werden.

Wenn die Richtlinie als obligatorisch festgelegt ist, wird das Feld „pinned“ ignoriert, und alle Kacheln werden angeheftet. Die Kacheln können vom Benutzer nicht gelöscht werden und werden immer am Anfang der Quicklinks-Liste angezeigt.

Wenn die Richtlinie als empfohlen festgelegt ist, bleiben angeheftete Kacheln in der Liste, aber der Benutzer hat die Möglichkeit, sie zu bearbeiten und zu löschen. Nicht angeheftete Quicklink-Kacheln verhalten sich wie Standardwebsites der obersten Ebene und werden von der Liste gestrichen, wenn andere Websites häufiger besucht werden. Beim Anwenden von nicht angehefteten Links über diese Richtlinie auf ein vorhandenes Browserprofil werden die Links u. U. überhaupt nicht angezeigt, je nachdem, wie sie im Vergleich zum Browserverlauf des Benutzers eingestuft werden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Wörterbuch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: NewTabPageManagedQuickLinks
  - Gruppenrichtlinienname: Schnelllinks für neue Tabs festlegen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Start, Startseite und neue Tabseite
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Start, Startseite und neue Tabseite
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: NewTabPageManagedQuickLinks
  - Werttyp: REG_SZ
  ##### Beispielwert:
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


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: NewTabPageManagedQuickLinks
  - Beispielwert:
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
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NewTabPagePrerenderEnabled
  #### Im Voraus laden der neuen Registerkartenseite für schnelleres Rendern aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 85 oder höher

  #### Beschreibung
  Wenn Sie diese Richtlinie konfigurieren, wird die Seite "Neue Registerkarte" aktiviert, und Benutzer können diese Einstellung nicht ändern. Wenn Sie diese Richtlinie nicht konfigurieren, ist Vorabladen aktiviert, und Benutzer können diese Einstellung ändern.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: NewTabPagePrerenderEnabled
  - Gruppenrichtlinienname: Im Voraus laden der neuen Registerkartenseite für schnelleres Rendern aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Start, Startseite und neue Tabseite
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Start, Startseite und neue Tabseite
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: NewTabPagePrerenderEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: NewTabPagePrerenderEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NewTabPageSetFeedType
  #### Funktion für neue Tabseiten in Microsoft Edge konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 79 oder höher

  #### Beschreibung
  Diese Richtlinie gibt Ihnen die Möglichkeit, für die neue Tabseite zwischen Microsoft News- oder Office 365-Feed zu wählen.

Wenn Sie diese Richtlinie auf “News” festlegen, wird Benutzern auf der neuen Tabseite der Microsoft News-Feed angezeigt.

Wenn Sie diese Richtlinie auf den Office”Office”, wird Benutzern mit einer Azure Active Directory-Browseranmeldung der Office 365-Feed auf der neuen Tabseite angezeigt.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, gilt Folgendes:

– Benutzern mit Azure Active Directory-Browseranmeldung wird neben dem Standardfeed für neue Tabseiten auch der Office 365-Feed angeboten.

– Benutzern ohne Azure Active Directory-Browseranmeldung wird der Standardfeed für neue Tabseiten angezeigt.

Wenn Sie diese Richtlinie *und* die Richtlinie “[NewTabPageLocation](#newtabpagelocation)” konfigurieren, hat “[NewTabPageLocation](#newtabpagelocation)” Vorrang.

Standardeinstellung: Deaktiviert oder nicht konfiguriert.

Zuordnung der Richtlinienoptionen:

* News (0) = Microsoft News-Feedoberfläche

* Office (1) = Office 365-Feedoberfläche

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: NewTabPageSetFeedType
  - Gruppenrichtlinienname: Funktion für neue Tabseiten in Microsoft Edge konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Start, Startseite und neue Tabseite
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Start, Startseite und neue Tabseite
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: NewTabPageSetFeedType
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: NewTabPageSetFeedType
  - Beispielwert:
``` xml
<integer>0</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### RestoreOnStartup
  #### Aktion, die beim Start ausgeführt werden soll
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Mit dieser Richtlinie legen Sie fest, wie sich Microsoft Edge beim Starten verhält.

  Wenn Sie möchten, dass sich beim Start immer eine neue Registerkarte öffnet, wählen Sie  “RestoreOnStartupIsNewTabPage”.

  Wenn Sie möchten, dass die URLs, die beim letzten Schließen von Microsoft Edge geöffnet waren, wieder geöffnet werden, wählen Sie “RestoreOnStartupIsLastSession”. Die Browsersitzung wird so wiederhergestellt, wie sie war. Beachten Sie, dass diese Option einige Einstellungen deaktiviert, die auf Sitzungen basieren oder die Aktionen beim Beenden ausführen (z. B. das Löschen von Browserdaten beim Beenden oder von Sitzungscookies).

  Wenn Sie einen bestimmten Satz von URLs öffnen möchten, wählen Sie “RestoreOnStartupIsURLs”.

  Das Deaktivieren dieser Einstellung entspricht einer fehlenden Konfiguration. Die Benutzer können sie in Microsoft Edge ändern.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.

Zuordnung der Richtlinienoptionen:

* RestoreOnStartupIsNewTabPage (5) = Neuen Tab öffnen

* RestoreOnStartupIsLastSession (1) = Letzte Sitzung wiederherstellen

* RestoreOnStartupIsURLs (4) = Liste mit URLs öffnen

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: RestoreOnStartup
  - Gruppenrichtlinienname: Aktion, die beim Start ausgeführt werden soll
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Start, Startseite und neue Tabseite
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Start, Startseite und neue Tabseite
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: RestoreOnStartup
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000004
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: RestoreOnStartup
  - Beispielwert:
``` xml
<integer>4</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### RestoreOnStartupURLs
  #### Websites, die beim Start des Browsers geöffnet werden sollen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt eine Liste von Websites an, die beim Start des Browsers automatisch geöffnet werden sollen. Wenn Sie diese Richtlinie nicht konfigurieren, wird beim Start keine Website geöffnet.

Diese Richtlinie ist nur verfügbar nur, wenn Sie zudem die Richtlinie [RestoreOnStartup](#restoreonstartup) auf “URL-Liste öffnen” (4) festlegen.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: RestoreOnStartupURLs
  - Gruppenrichtlinienname: Websites, die beim Start des Browsers geöffnet werden sollen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Start, Startseite und neue Tabseite
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Start, Startseite und neue Tabseite
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen\RestoreOnStartupURLs
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\1 = "https://contoso.com"
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\2 = "https://www.fabrikam.com"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: RestoreOnStartupURLs
  - Beispielwert:
``` xml
<array>
  <string>https://contoso.com</string>
  <string>https://www.fabrikam.com</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ShowHomeButton
  #### Schaltfläche „Startseite“ auf Symbolleiste anzeigen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Zeigt die Schaltfläche „Start“ auf der Microsoft Edge-Symbolleiste an.

Aktivieren Sie diese Richtlinie, um die Schaltfläche „Start“ immer anzuzeigen. Deaktivieren Sie diese Option, um die Schaltfläche nie anzuzeigen.

Wenn Sie die Richtlinie nicht konfigurieren, können Benutzer auswählen, ob die Schaltfläche „Start“ angezeigt werden soll.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ShowHomeButton
  - Gruppenrichtlinienname: Schaltfläche „Startseite“ auf Symbolleiste anzeigen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/Start, Startseite und neue Tabseite
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/Start, Startseite und neue Tabseite
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: ShowHomeButton
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ShowHomeButton
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ## Additional policies

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AddressBarMicrosoftSearchInBingProviderEnabled
  #### Vorschläge von „Microsoft Search in Bing“ in der Adressleiste aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 81 oder höher

  #### Beschreibung
  Aktiviert die Anzeige relevanter Vorschläge von „Microsoft Search in Bing“ in der Vorschlagsliste der Adresszeile, wenn der Benutzer eine Suchzeichenfolge in der Adressleiste eingibt. Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, werden Benutzern unter Umständen von Microsoft Search in Bing unterstützte interne Ergebnisse in der Vorschlagsliste der Adressleiste von Microsoft Edge angezeigt. Zum Anzeigen von Ergebnissen von „Microsoft Search in Bing“ muss der Benutzer mit dem Azure AD-Konto der Organisation bei Microsoft Edge angemeldet sein.
Wenn Sie diese Richtlinie deaktivieren, werden Benutzern keine internen Ergebnisse in der Vorschlagsliste der Adressleiste von Microsoft Edge angezeigt.
Wenn Sie den Richtliniensatz zum Erzwingen eines Standardsuchanbieters ([DefaultSearchProviderEnabled](#defaultsearchproviderenabled), [DefaultSearchProviderName](#defaultsearchprovidername) und [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)) aktiviert haben und es sich beim angegebenen Suchanbieter nicht um Bing handelt, wird diese Richtlinie nicht angewendet, und in der Vorschlagsliste der Adressleiste werden keine Vorschläge von „Microsoft Search in Bing“ angezeigt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AddressBarMicrosoftSearchInBingProviderEnabled
  - Gruppenrichtlinienname: Vorschläge von „Microsoft Search in Bing“ in der Adressleiste aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AddressBarMicrosoftSearchInBingProviderEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AddressBarMicrosoftSearchInBingProviderEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AdsSettingForIntrusiveAdsSites
  #### Anzeigeneinstellung für Websites mit aufdringlichen Anzeigen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 78 oder höher

  #### Beschreibung
  Steuert, ob Anzeigen auf Websites mit aufdringlicher Werbung blockiert werden.

Zuordnung der Richtlinienoptionen:

* AllowAds (1) = Werbung auf allen Websites zulassen

* BlockAds (2) = Blockiert Werbung auf Websites mit aufdringlichen Werbeanzeigen. (Standardwert)

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AdsSettingForIntrusiveAdsSites
  - Gruppenrichtlinienname: Anzeigeneinstellung für Websites mit aufdringlichen Anzeigen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AdsSettingForIntrusiveAdsSites
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AdsSettingForIntrusiveAdsSites
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AllowDeletingBrowserHistory
  #### Löschen des Browser- und Downloadverlaufs ermöglichen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Ermöglicht das Löschen des Browser- und Downloadverlaufs und verhindert, dass Benutzer diese Einstellung ändern.

Hinweis: Auch wenn diese Richtlinie deaktiviert ist, ist nicht garantiert, dass Browser- und Downloadverlauf gespeichert werden: Benutzer können die Verlaufsdatenbankdateien direkt bearbeiten oder löschen, und der Browser kann beliebige oder alle Verlaufselemente jederzeit entfernen (basierend auf der Ablauffrist) oder archivieren.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer den Browser- und Downloadverlauf löschen.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer den Browser- und Downloadverlauf nicht löschen.

Wenn Sie diese Richtlinie aktivieren, achten Sie darauf, dass die Richtlinie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) nicht aktiviert ist, da beide dazu dienen, Daten zu löschen. Wenn Sie beide Richtlinien aktivieren, hat die Richtlinie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) Vorrang und löscht alle Daten, wenn Microsoft Edge geschlossen wird (unabhängig von der Konfiguration dieser Richtlinie).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AllowDeletingBrowserHistory
  - Gruppenrichtlinienname: Löschen des Browser- und Downloadverlaufs ermöglichen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AllowDeletingBrowserHistory
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AllowDeletingBrowserHistory
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AllowFileSelectionDialogs
  #### Dateiauswahl-Dialogfelder zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Lassen Sie den Zugriff auf lokale Dateien zu, indem Sie Microsoft Edge Dateiauswahl-Dialogfelder anzeigen lassen.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer Dateiauswahl-Dialogfelder normal öffnen.

Wenn Sie diese Richtlinie deaktivieren, wird immer dann eine Meldung angezeigt, wenn der Benutzer eine Aktion ausführt, die ein Dateiauswahl-Dialogfeld auslöst (z. B. das Importieren von Favoriten, das Hochladen von Dateien oder das Speichern von links). Es wird angenommen, dass der Benutzer im Dateiauswahl-Dialogfeld auf „Abbrechen” geklickt hat.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AllowFileSelectionDialogs
  - Gruppenrichtlinienname: Dateiauswahl-Dialogfelder zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AllowFileSelectionDialogs
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AllowFileSelectionDialogs
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AllowPopupsDuringPageUnload
  #### Erlaubt einer Seite, Popups während des Entladens zu zeigen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 78 oder höher

  #### Beschreibung
  Mit dieser Richtlinie kann ein Administrator angeben, dass beim Entladen einer Seite Popups angezeigt werden können.

Wenn die Richtlinie auf „aktiviert“ festgelegt ist, können Seiten Popups anzeigen, während sie entladen werden.

Wenn die Richtlinie auf „deaktiviert“ festgelegt oder nicht festgelegt ist, dürfen Seiten keine Popups anzeigen, während sie entladen werden. Dies entspricht der folgenden Spezifikation: (https://html.spec.whatwg.org/#apis-for-creating-and-navigating-browsing-contexts-by-name).

Diese Richtlinie wird künftig entfernt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AllowPopupsDuringPageUnload
  - Gruppenrichtlinienname: Erlaubt einer Seite, Popups während des Entladens zu zeigen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AllowPopupsDuringPageUnload
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AllowPopupsDuringPageUnload
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AllowSurfGame
  #### Surf-Spiel zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 83 oder höher

  #### Beschreibung
  Wenn Sie diese Richtlinie deaktivieren, können Benutzer das Surf-Spiel nicht spielen, wenn das Gerät offline ist oder der Benutzer zu „edge://surf“ navigiert.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer das Surf-Spiel spielen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AllowSurfGame
  - Gruppenrichtlinienname: Surf-Spiel zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AllowSurfGame
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AllowSurfGame
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AllowSyncXHRInPageDismissal
  #### Zulassen, dass Seiten beim Schließen synchrone XHR-Anforderungen senden (veraltet)
  >VERALTET: Diese Richtlinie ist veraltet. Sie wird gegenwärtig noch unterstützt, aber in einem zukünftigen Release ausgemustert.
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 79 oder höher

  #### Beschreibung
  Diese Richtlinie ist veraltet, da sie nur als kurzfristiger Mechanismus gedacht ist, um Unternehmen mehr Zeit für die Aktualisierung ihrer Webinhalte zu geben, wenn sich herausstellt, dass sie nicht mit der Änderung vereinbar sind, synchrone XHR-Anforderungen während des Schließens einer Seite nicht zuzulassen. Sie funktioniert in Microsoft Edge Version 88 nicht mehr.

 Mit dieser Richtlinie können Sie festlegen, dass eine Seite während des Schließens synchrone XHR-Anforderungen senden kann.

 Wenn Sie diese Richtlinie aktivieren, werden Seiten am Senden synchroner XHR-Anforderungen während des Schließens gehindert.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, können Seiten während des Schließens keine synchronen XHR-Anforderungen senden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AllowSyncXHRInPageDismissal
  - Gruppenrichtlinienname: Zulassen, dass Seiten beim Schließen synchrone XHR-Anforderungen senden (veraltet)
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AllowSyncXHRInPageDismissal
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AllowSyncXHRInPageDismissal
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AllowTokenBindingForUrls
  #### Konfigurieren Sie die Liste der Sites, für die Microsoft Edge versuchen wird, eine Tokenbindung herzustellen.
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 83 oder höher

  #### Beschreibung
  Konfigurieren Sie die Liste der URL-Muster für Websites, bei denen der Browser versucht, das Tokenbindungsprotokoll auszuführen.
 Bei den Domänen in dieser Liste sendet der Browser die Tokenbindungs-ClientHello im TLS-Handshake (siehe https://tools.ietf.org/html/rfc8472).
Wenn der Server mit einer gültigen ServerHello-Antwort antwortet, erstellt und sendet der Browser Tokenbindungsnachrichten in aufeinanderfolgenden HTTPS-Anforderungen. Weitere Informationen finden Sie unter https://tools.ietf.org/html/rfc8471.

Wenn diese Liste leer ist, wird die Tokenbindung deaktiviert.

Diese Richtlinie steht nur auf Windows 10-Geräten mit Funktionen für den virtuellen Secure-Modus zur Verfügung.

Ab Microsoft Edge 86 unterstützt diese Richtlinie nicht mehr das dynamische Aktualisieren.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AllowTokenBindingForUrls
  - Gruppenrichtlinienname: Konfigurieren Sie die Liste der Sites, für die Microsoft Edge versuchen wird, eine Tokenbindung herzustellen.
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\2 = "[*.]mydomain2.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\3 = "[*.].mydomain2.com"

```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AllowTrackingForUrls
  #### Konfigurieren von Ausnahmen für die Tracking-Verhinderung für bestimmte Sites
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 78 oder höher

  #### Beschreibung
  Konfigurieren Sie die Liste der URL-Muster, die von der nach Tracking-Verhinderung ausgeschlossen sind.

Wenn Sie diese Richtlinie konfigurieren, wird die Liste der konfigurierten URL-Muster von der nach Tracking-Verhinderung ausgeschlossen.

Wenn Sie diese Richtlinie nicht konfigurieren, wird der globale Standardwert aus der Richtlinie "Blockieren der Nachverfolgung der Webbrowsing-Aktivitäten von Benutzern" (falls festgelegt) oder die persönliche Konfiguration des Benutzers für alle Websites verwendet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AllowTrackingForUrls
  - Gruppenrichtlinienname: Konfigurieren von Ausnahmen für die Tracking-Verhinderung für bestimmte Sites
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AllowTrackingForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AlternateErrorPagesEnabled
  #### Ähnliche Seiten vorschlagen, wenn eine Webseite nicht gefunden wird
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 80 oder höher

  #### Beschreibung
  Erlaubt, dass Microsoft Edge eine Verbindung mit einem Webdienst herstellt, um bei Konnektivitätsproblemen (beispielsweise DNS-Fehler) URL- und Suchvorschläge zu generieren.

Wenn Sie diese Richtlinie aktivieren, wird ein Webdienst verwendet, um bei Netzwerkfehlern URL- und Suchvorschläge zu generieren.

Wenn Sie diese Richtlinie deaktivieren, wird der Webdienst nicht aufgerufen, und es wird eine Standardfehlerseite angezeigt.

Wenn Sie diese Richtlinie nicht konfigurieren, verwendet Microsoft Edge die Benutzereinstellung, die für Dienste unter edge://settings/privacy“ festgelegt ist.
Der Umschalter **Ähnliche Seiten vorschlagen, wenn eine Webseite nicht gefunden wird** kann vom Benutzer aktiviert oder deaktiviert werden. Hinweis: Wenn Sie diese Richtlinie (AlternateErrorPagesEnabled) aktiviert haben, ist die Einstellung “Ähnliche Seiten vorschlagen, wenn eine Webseite nicht gefunden wird” aktiviert und kann vom Benutzer nicht mithilfe des Umschalters geändert werden. Wenn Sie diese Richtlinie deaktivieren, ist die Einstellung “Ähnliche Seiten vorschlagen, wenn eine Webseite nicht gefunden wird“ aktiviert und kann vom Benutzer nicht mithilfe des Umschalters geändert werden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AlternateErrorPagesEnabled
  - Gruppenrichtlinienname: Ähnliche Seiten vorschlagen, wenn eine Webseite nicht gefunden wird
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: AlternateErrorPagesEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AlternateErrorPagesEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AlwaysOpenPdfExternally
  #### PDF-Dateien immer extern öffnen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Deaktiviert den internen PDF-Viewer in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, werden PDF-Dateien von Microsoft Edge als Downloads behandelt und können von den Benutzern mit der Standardanwendung geöffnet werden.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden PDF-Dateien von Microsoft Edge geöffnet (es sei denn, dies wird vom Benutzer deaktiviert).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AlwaysOpenPdfExternally
  - Gruppenrichtlinienname: PDF-Dateien immer extern öffnen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AlwaysOpenPdfExternally
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AlwaysOpenPdfExternally
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AmbientAuthenticationInPrivateModesEnabled
  #### Umgebungsauthentifizierung für InPrivate- und Gastprofile aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 81 oder höher

  #### Beschreibung
  Konfigurieren Sie diese Richtlinie, um die Umgebungsauthentifizierung für InPrivate- und Gastprofile in Microsoft Edge zuzulassen bzw. nicht zuzulassen.

Die Umgebungsauthentifizierung ist eine HTTP-Authentifizierung mit Standardanmeldeinformationen, wenn keine expliziten Anmeldeinformationen über NTLM/Kerberos/Negotiate-Herausforderung/Antwortschemas bereitgestellt werden.

Wenn Sie die Richtlinie auf “RegularOnly” festlegen, wird die Umgebungsauthentifizierung nur für reguläre Sitzungen zugelassen. Für InPrivate- und Gastsitzungen ist die Umgebungsauthentifizierung nicht zulässig.

Wenn Sie die Richtlinie auf “InPrivateAndRegular” festlegen, wird die Umgebungsauthentifizierung für InPrivate- und reguläre Sitzungen zugelassen. Für Gastsitzungen ist die Umgebungsauthentifizierung nicht zulässig.

Wenn Sie die Richtlinie auf “GuestAndRegular” festlegen, ist die Umgebungsauthentifizierung für Gastsitzungen und reguläre Sitzungen zulässig. Für InPrivate-Sitzungen ist die Umgebungsauthentifizierung nicht zulässig.

Wenn Sie die Richtlinie auf “All” festlegen, ist die Umgebungsauthentifizierung für alle Sitzungen zulässig.

Hinweis: In regulären Profilen ist die Umgebungsauthentifizierung immer zulässig.

Falls die Richtlinie ab Microsoft Edge Version 81 nicht festgelegt ist, ist die Umgebungsauthentifizierung nur in regulären Sitzungen zugelassen.

Zuordnung der Richtlinienoptionen:

* RegularOnly (0) = Umgebungsauthentifizierung nur in regulären Sitzungen aktivieren

* InPrivateAndRegular (1) = Umgebungsauthentifizierung in InPrivate-Sitzungen und regulären Sitzungen aktivieren

* GuestAndRegular (2) = Umgebungsauthentifizierung in Gastsitzungen und regulären Sitzungen aktivieren

* All (3) = Umgebungsauthentifizierung in regulären, InPrivate- und Gastsitzungen aktivieren

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AmbientAuthenticationInPrivateModesEnabled
  - Gruppenrichtlinienname: Umgebungsauthentifizierung für InPrivate- und Gastprofile aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AmbientAuthenticationInPrivateModesEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AmbientAuthenticationInPrivateModesEnabled
  - Beispielwert:
``` xml
<integer>0</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AppCacheForceEnabled
  #### Ermöglichen, dass das AppCache-Feature erneut aktiviert werden kann, auch wenn dieses standardmäßig deaktiviert ist
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 84 oder höher

  #### Beschreibung
  Wenn Sie diese Richtlinie auf „true“ setzen, ist AppCache aktiviert, auch wenn AppCache in Microsoft Edge standardmäßig nicht verfügbar ist.

Wenn Sie für diese Richtlinie „false“ oder keinen Wert festlegen, wird AppCache entsprechend den Standardeinstellungen von Microsoft Edge verwendet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AppCacheForceEnabled
  - Gruppenrichtlinienname: Ermöglichen, dass das AppCache-Feature erneut aktiviert werden kann, auch wenn dieses standardmäßig deaktiviert ist
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AppCacheForceEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AppCacheForceEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ApplicationLocaleValue
  #### Anwendungsgebietsschema festlegen
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 77 oder höher

  #### Beschreibung
  Konfiguriert das Anwendungsgebietsschema in Microsoft Edge und verhindert, dass Benutzer das Gebietsschema ändern.

Wenn Sie diese Richtlinie aktivieren, verwendet Microsoft Edge das angegebene Gebietsschema. Wenn das konfigurierte Gebietsschema nicht unterstützt wird, wird stattdessen "en-US" verwendet.

Wenn Sie diese Einstellung deaktivieren oder nicht konfigurieren, verwendet Microsoft Edge entweder das vom Benutzer angegebene bevorzugte Gebietsschema (falls konfiguriert) oder das Fallback-Gebietsschema "en-US".

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ApplicationLocaleValue
  - Gruppenrichtlinienname: Anwendungsgebietsschema festlegen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: ApplicationLocaleValue
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"en"
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AudioCaptureAllowed
  #### Audioaufnahme zulassen oder blockieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Hier können Sie einstellen, ob ein Benutzer aufgefordert wird, einer Website Zugriff auf sein Audioaufnahmegerät zu gewähren. Diese Richtlinie gilt für alle URLs mit Ausnahme derjenigen, die in der Liste [AudioCaptureAllowedUrls](#audiocaptureallowedurls) konfiguriert sind.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren (Standardeinstellung), wird der Benutzer mit Ausnahme der URLs in der Liste [AudioCaptureAllowedUrls](#audiocaptureallowedurls) aufgefordert. Diese aufgeführten URLs erhalten ohne Aufforderung Zugriff.

Wenn Sie diese Richtlinie deaktivieren, wird der Benutzer nicht aufgefordert, und Audioaufnahmen sind nur für die URLs möglich, die in [AudioCaptureAllowedUrls](#audiocaptureallowedurls) konfiguriert sind.

Diese Richtlinie betrifft alle Arten von Audioeingängen, nicht nur das eingebaute Mikrofon.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AudioCaptureAllowed
  - Gruppenrichtlinienname: Audioaufnahme zulassen oder blockieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AudioCaptureAllowed
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AudioCaptureAllowed
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AudioCaptureAllowedUrls
  #### Websites, die auf Audioaufnahmegeräte zugreifen können, ohne eine Berechtigung anzufordern
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Geben Sie Websites basierend auf URL-Mustern an, die Audioaufnahmegeräte verwenden können, ohne den Benutzer um Erlaubnis zu bitten. Muster in dieser Liste werden mit dem Sicherheitsursprung der anfordernden URL abgeglichen. Wenn sie übereinstimmen, wird der Website automatisch der Zugriff auf Audioaufnahmegeräte gewährt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AudioCaptureAllowedUrls
  - Gruppenrichtlinienname: Websites, die auf Audioaufnahmegeräte zugreifen können, ohne eine Berechtigung anzufordern
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AudioCaptureAllowedUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AudioSandboxEnabled
  #### Ausführung der Audiosandbox zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 81 oder höher

  #### Beschreibung
  Diese Richtlinie steuert die Audioprozess-Sandbox.

Wenn Sie diese Richtlinie aktivieren, wird der Audioprozess in einer Sandbox ausgeführt.

Wenn Sie diese Richtlinie deaktivieren, wird der Audioprozess nicht in einer Sandbox ausgeführt, und das WebRTC-Audioverarbeitungsmodul wird im Rendererprozess ausgeführt.
Dies setzt Benutzer Sicherheitsrisiken in Zusammenhang mit der Verwendung des Audiosubsystems außerhalb einer Sandbox aus.

Wenn Sie diese Richtlinie nicht konfigurieren, wird die Standardkonfiguration für die Audiosandbox verwendet, die je nach Plattform unterschiedlich sein kann.

Diese Richtlinie soll Unternehmen die Flexibilität geben, die Audiosandbox zu deaktivieren, wenn sie Setups mit Sicherheitssoftware verwenden, die mit der Sandbox interferieren.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AudioSandboxEnabled
  - Gruppenrichtlinienname: Ausführung der Audiosandbox zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AudioSandboxEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AudioSandboxEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AutoImportAtFirstRun
  #### Daten und Einstellungen eines anderen Browsers bei der ersten Ausführung automatisch importieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Wenn Sie diese Richtlinie aktivieren, werden bei der erstmaligen Ausführung alle unterstützten Datentypen und Einstellungen aus dem festgelegten Browser im Hintergrund importiert. Während der erstmaligen Ausführung wird außerdem der Importabschnitt übersprungen.

   Die Browserdaten aus Microsoft Edge-Vorgängerversionen werden ungeachtet des Werts der Richtlinie stets bei der ersten Ausführung im Hintergrund migriert.

   Wenn diese Richtlinie auf den Wert “FromDefaultBrowser” festgelegt wird, werden die Datentypen, die dem Standardbrowser entsprechen, auf das verwaltete Gerät importiert.

 Falls der Browser, der als Wert dieser Richtlinie festgelegt ist, auf dem verwalteten Gerät nicht vorhanden ist, überspringt “Microsoft Edge” den Import ohne Benachrichtigung an den Benutzer.

  Wenn Sie diese Richtlinie auf "DisabledAutoImport" festlegen, wird der Importabschnitt bei der ersten Ausführung vollständig übersprungen und “Microsoft Edge” importiert Browserdaten und Einstellungen nicht automatisch.

    Wenn diese Richtlinie auf den Wert “FromInternetExplorer” festgelegt ist, werden die folgenden Datentypen von Internet Explorer importiert:
   1. Favoriten oder Lesezeichen
   2. Gespeicherte Passwörter
   3. Suchmaschinen
  4. Browserverlauf
  5. Startseite

   Wenn diese Richtlinie auf den Wert “FromGoogleChrome” festgelegt ist, werden die folgenden Datentypen von Google Chrome importiert:
   1. Favoriten
  2. Gespeicherte Kennwörter
   3. Adressen und mehr
  4. Zahlungsinformationen
  5. Browserverlauf
  6. Einstellungen
7. Angeheftete und offene Tabs
   8. Erweiterungen
  9. Cookies

   Hinweis: Eine detailliertere Übersicht über die Importe aus Google Chrome finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2120835](https://go.microsoft.com/fwlink/?linkid=2120835)

  Falls diese Richtlinie auf den Wert “FromSafari” festgelegt ist, werden Benutzerdaten nicht mehr in Microsoft Edge importiert. Dies liegt an der Funktionsweise des Datenträgervollzugriffs unter macOS.
   Unter macOs Mojave und höher ist ein automatisierter und unbeaufsichtigter Import von Safari-Daten in Microsoft Edge nicht mehr möglich.

   Ab Microsoft Edge Version 83 werden, falls die Richtlinie auf den Wert “FromMozillaFirefox” festgelegt ist, die folgenden Daten aus Mozilla Firefox importiert:
    1. Favoriten oder Lesezeichen
   2. Gespeicherte Passwöerter
   3. Adressen und mehr
   4. Browserverlauf

   Falls Sie den Import spezifischer Datentypen auf den verwalteten Geräten einschränken möchten, können Sie diese Richtlinie zusammen mit anderen verwenden, zum Beispiel “[ImportAutofillFormData](#importautofillformdata)”, “[ImportBrowserSettings](#importbrowsersettings)”, “[ImportFavorites](#importfavorites)” usw.

Zuordnung der Richtlinienoptionen:

* FromDefaultBrowser (0) = Importiert automatisch alle unterstützten Datentypen und Einstellungen aus dem Standardbrowser.

* FromInternetExplorer (1) = Importiert automatisch alle unterstützten Datentypen und Einstellungen aus Internet Explorer.

* FromGoogleChrome (2) = Importiert automatisch alle unterstützten Datentypen und Einstellungen aus Google Chrome.

* FromSafari (3) = Importiert automatisch alle unterstützten Datentypen und Einstellungen aus Safari.

* DisabledAutoImport (4) = Deaktiviert den automatischen Import und überspringt den Importabschnitt der erstmaligen Ausführung.

* FromMozillaFirefox (5) = Importiert automatisch alle unterstützten Datentypen und Einstellungen aus Mozilla Firefox.

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AutoImportAtFirstRun
  - Gruppenrichtlinienname: Daten und Einstellungen eines anderen Browsers bei der ersten Ausführung automatisch importieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AutoImportAtFirstRun
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000002
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AutoImportAtFirstRun
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AutoLaunchProtocolsFromOrigins
  #### Definieren Sie eine Liste der Protokolle, über die eine externe Anwendung von den aufgeführten Ursprüngen aus ohne Rückfrage beim Benutzer gestartet werden kann.
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 85 oder höher

  #### Beschreibung
  Ermöglicht das Festlegen einer Liste von Protokollen, und für jedes Protokoll einer zugeordneten Liste zulässiger Ursprungsmuster, über die eine externe Anwendung ohne Rückfrage beim Benutzer gestartet werden kann. Das nachgestellte Trennzeichen sollte beim Aufführen des Protokolls nicht einbezogen werden. Listen Sie beispielsweise „skype“ anstelle von „skype:“ oder „skype://“ auf.

Wenn Sie diese Richtlinie konfigurieren, kann ein Protokoll eine externe Anwendung nur dann ohne Rückfrage starten, wenn:

- das Protokoll aufgelistet ist

- der Ursprung der Website, die versucht, das Protokoll zu starten, mit einem der Ursprungsmuster in der allowed_origins-Liste dieses Protokolls übereinstimmt.

Wenn eine der beiden Voraussetzungen nicht erfüllt ist, wird die Rückfrage für den externen Protokollstart von der Richtlinie nicht ausgelassen.

Wenn Sie diese Richtlinie nicht konfigurieren, können keine Protokolle ohne Rückfrage gestartet werden. Benutzer können die Rückfrage für einzelne Protokolle/Websites deaktivieren, es sei denn, die [ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox) Richtlinie ist auf „Deaktiviert“ festgelegt. Diese Richtlinie wirkt sich nicht auf von Benutzern festgelegte Rückfrageausnahmen für einzelne Protokolle/Websites aus.

Für die Ursprungsentsprechungsmuster wird ein ähnliches Format verwendet wie für die [URLBlocklist](#urlblocklist)-Richtlinie, die unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) dokumentiert sind.

Die Ursprungsentsprechungsmuster für diese Richtlinie dürfen jedoch keine „/path“- oder „@query“-Elemente enthalten. Jedes Muster, das ein „/path“- oder „@query“-Element  enthält, wird ignoriert.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Wörterbuch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AutoLaunchProtocolsFromOrigins
  - Gruppenrichtlinienname: Definieren Sie eine Liste der Protokolle, über die eine externe Anwendung von den aufgeführten Ursprüngen aus ohne Rückfrage beim Benutzer gestartet werden kann.
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AutoLaunchProtocolsFromOrigins
  - Werttyp: REG_SZ
  ##### Beispielwert:
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


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AutoLaunchProtocolsFromOrigins
  - Beispielwert:
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
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AutoOpenAllowedForURLs
  #### URLs, bei denen Richtlinie “AutoOpenFileTypes” gelten kann
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 85 oder höher

  #### Beschreibung
  Eine Liste der URLs, auf die die Richtlinie „[AutoOpenFileTypes](#autoopenfiletypes)‟ angewendet wird. Diese Richtlinie hat keine Auswirkungen auf Werte für automatisches Öffnen, die von Benutzern mithilfe des Download Shelf festgelegt worden sind … > Menüeintrag „Dateien dieses Typs immer öffnen‟.

Wenn Sie URLs in dieser Richtlinie festlegen, werden Dateien durch sie nur automatisch geöffnet, wenn die URL Teil dieser Liste ist und der Dateityp in „[AutoOpenFileTypes](#autoopenfiletypes)‟ aufgeführt ist. Wenn eine der beiden Bedingungen nicht zutrifft, wird der Download nicht automatisch auf Basis der Richtlinie geöffnet.

Wenn Sie diese Richtlinie nicht festlegen, werden alle Downloads, deren Dateityp sich in „[AutoOpenFileTypes](#autoopenfiletypes)‟ befindet, automatisch geöffnet.

Ein URL-Muster muss entsprechend den Vorgaben formatiert werden, die Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) finden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AutoOpenAllowedForURLs
  - Gruppenrichtlinienname: URLs, bei denen Richtlinie “AutoOpenFileTypes” gelten kann
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\1 = "example.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\5 = ".exact.hostname.com"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AutoOpenAllowedForURLs
  - Beispielwert:
``` xml
<array>
  <string>example.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AutoOpenFileTypes
  #### Liste der Dateitypen, die nach dem Download automatisch geöffnet werden sollen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 85 oder höher

  #### Beschreibung
  Diese Richtlinie legt eine Liste der Dateitypen fest, die nach dem Download automatisch geöffnet werden sollen. Hinweis: Das vorangestellte Trennzeichen muss beim Auflisten der Dateitypen weggelassen werden, also beispielsweise "txt" statt ".txt".

  Standardmäßig werden diese Dateitypen automatisch durch alle URLs geöffnet. Sie können die Richtlinie “[AutoOpenAllowedForURLs](#autoopenallowedforurls)” verwenden, um die URLs einzuschränken, durch die diese Dateitypen automatisch geöffnet werden.

  Dateitypen, die automatisch geöffnet werden sollen, werden trotzdem durch den aktivierten Microsoft Defender SmartScreen geprüft und nicht geöffnet, wenn die Prüfung fehlschlägt.

  Dateitypen, die ein Benutzer bereits für automatisches Öffnen festgelegt hat, werden nach dem Download auch weiterhin automatisch geöffnet. Der Benutzer kann weiterhin andere Dateitypen angeben, die automatisch geöffnet werden sollen.

  Wenn Sie diese Richtlinie nicht festlegen, werden nur die Dateitypen, die ein Benutzer für das automatische Öffnen festgelegt hat, nach dem Download automatisch geöffnet.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AutoOpenFileTypes
  - Gruppenrichtlinienname: Liste der Dateitypen, die nach dem Download automatisch geöffnet werden sollen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\1 = "exe"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\2 = "txt"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AutoOpenFileTypes
  - Beispielwert:
``` xml
<array>
  <string>exe</string>
  <string>txt</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AutofillAddressEnabled
  #### AutoAusfüllen für Adressen aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Aktiviert das AutoAusfüllen-Feature und ermöglicht Benutzern das automatische Vervollständigen von Adressinformationen in Webformularen mithilfe zuvor gespeicherter Informationen.

Wenn Sie diese Richtlinie deaktivieren, werden die Adressinformationen von AutoAusfüllen niemals vorgeschlagen oder ausgefüllt, und es werden auch keine weiteren Adressinformationen gespeichert, die der Benutzer beim Browsen im Web ggf. übermittelt.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer AutoAusfüllen für Adressen in der Benutzeroberfläche steuern.

Hinweis: Wenn Sie diese Richtlinie deaktivieren, werden dadurch auch sämtliche Aktivitäten für alle Webformulare (mit Ausnahme von Zahlungs- und Kennwortformularen) beendet. Es werden keine weiteren Einträge gespeichert, und von Microsoft Edge werden keine zuvor verwendeten Einträge vorgeschlagen oder automatisch ausgefüllt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AutofillAddressEnabled
  - Gruppenrichtlinienname: AutoAusfüllen für Adressen aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: AutofillAddressEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AutofillAddressEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AutofillCreditCardEnabled
  #### AutoAusfüllen für Kreditkarten aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Aktiviert das AutoAusfüllen-Feature von Microsoft Edge und ermöglicht Benutzern das automatische Ausfüllen von Kreditkarteninformationen in Webformularen mit zuvor gespeicherten Angaben.

Wenn Sie diese Richtlinie deaktivieren, werden von AutoAusfüllen keine Kreditkarteninformationen vorgeschlagen oder ausgefüllt, und es werden auch keine weiteren Kreditkarteninformationen gespeichert, die der Benutzer ggf. beim Surfen im Web übermittelt.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer das automatische Ausfüllen von Kreditkarteninformationen steuern.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AutofillCreditCardEnabled
  - Gruppenrichtlinienname: AutoAusfüllen für Kreditkarten aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: AutofillCreditCardEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AutofillCreditCardEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### AutoplayAllowed
  #### Automatische Medienwiedergabe für Websites zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 78 oder höher

  #### Beschreibung
  Diese Richtlinie steuert die automatische Medienwiedergabe für Websites.

Bei Verwendung der Standardeinstellung “Nicht konfiguriert“ werden die aktuellen Einstellungen für die automatische Medienwiedergabe verwendet, und Benutzer können die automatische Wiedergabe wie gewünscht konfigurieren.

Bei Verwendung der Einstellung “Aktiviert“ wird die automatische Medienwiedergabe auf “Zulassen“ festgelegt. In diesem Fall ist die automatische Medienwiedergabe auf allen Websites zulässig. Benutzer können diese Richtlinie nicht überschreiben.

Bei Verwendung der Einstellung “Deaktiviert“ wird die automatische Medienwiedergabe auf “Blockieren“ festgelegt. In diesem Fall ist die automatische Medienwiedergabe auf keinen Websites zulässig. Benutzer können diese Richtlinie nicht überschreiben.

Diese Richtlinie wird erst wirksam, nachdem eine Registerkarte geschlossen und erneut geöffnet wurde.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: AutoplayAllowed
  - Gruppenrichtlinienname: Automatische Medienwiedergabe für Websites zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: AutoplayAllowed
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: AutoplayAllowed
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### BackgroundModeEnabled
  #### Ausführen von Hintergrund-Apps fortsetzen, nachdem Microsoft Edge geschlossen wurde
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 77 oder höher

  #### Beschreibung
  Ermöglicht es Microsoft Edge-Prozessen, beim Einloggen in das Betriebssystem zu starten und nach dem Schließen des letzten Browserfensters weiter zu laufen. In diesem Szenario bleiben die Hintergrundanwendungen und die aktuelle Browsersitzung aktiv, einschließlich aller Sitzungs-Cookies. Ein offener Hintergrundprozess zeigt ein Symbol in der Taskleiste an und kann von dort aus immer geschlossen werden.

Wenn Sie diese Richtlinie aktivieren, wird der Hintergrundmodus eingeschaltet.

Wenn Sie diese Richtlinie deaktivieren, wird der Hintergrundmodus ausgeschaltet.

Wenn Sie diese Richtlinie nicht konfigurieren, wird der Hintergrundmodus zunächst deaktiviert, und der Benutzer kann dessen Verhalten in edge://settings/system konfigurieren.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: BackgroundModeEnabled
  - Gruppenrichtlinienname: Ausführen von Hintergrund-Apps fortsetzen, nachdem Microsoft Edge geschlossen wurde
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: BackgroundModeEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### BackgroundTemplateListUpdatesEnabled
  #### Ermöglicht für Sammlungen und andere Features, die Vorlagen verwenden, die Aktualisierung der Liste verfügbarer Vorlagen im Hintergrund.
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 79 oder höher

  #### Beschreibung
  Ermöglicht es Ihnen, für Sammlungen und andere Features, die Vorlagen verwenden, Hintergrundaktualisierungen der Liste mit den verfügbaren Vorlagen zu aktivieren oder zu deaktivieren. Vorlagen werden verwendet, um umfassende Metadaten aus einer Webseite zu extrahieren, wenn die Seite in einer Sammlung gespeichert wird.

Wenn Sie diese Einstellung aktivieren oder diese nicht konfiguriert ist, wird die Liste mit den verfügbaren Vorlagen alle 24 Stunden im Hintergrund von einem Microsoft-Dienst heruntergeladen.

Wenn Sie diese Einstellung deaktivieren, wird die Liste mit den verfügbaren Vorlagen bei Bedarf heruntergeladen. Diese Art von Download kann für Sammlungen und andere Features ggf. zu geringen Leistungseinbußen führen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: BackgroundTemplateListUpdatesEnabled
  - Gruppenrichtlinienname: Ermöglicht für Sammlungen und andere Features, die Vorlagen verwenden, die Aktualisierung der Liste verfügbarer Vorlagen im Hintergrund.
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: BackgroundTemplateListUpdatesEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: BackgroundTemplateListUpdatesEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### BingAdsSuppression
  #### Alle Werbeanzeigen in Bing-Suchergebnissen blockieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 83 oder höher

  #### Beschreibung
  Aktiviert eine anzeigenfreie Suchumgebung auf Bing.com.

Wenn Sie diese Richtlinie aktivieren, kann ein Benutzer auf Bing.com Suchen über eine anzeigenfreie Umgebung durchführen. Gleichzeitig wird die SafeSearch-Einstellung auf "Streng" festgelegt und kann vom Benutzer nicht geändert werden.

Wenn Sie diese Richtlinie nicht konfigurieren, werden in den Suchergebnissen auf Bing.com standardmäßig Anzeigen angezeigt. SafeSearch wird standardmäßig auf "Mittel" festgelegt und kann vom Benutzer geändert werden.

Diese Richtlinie ist nur für K-12-SKUs verfügbar, die von Microsoft als EDU-Mandanten bezeichnet werden.

Lesen Sie bitte [https://go.microsoft.com/fwlink/?linkid=2119711](https://go.microsoft.com/fwlink/?linkid=2119711), um weitere Informationen zu dieser Richtlinie zu erhalten, oder wenn die folgenden Szenarien für Sie zutreffen:

* Sie verfügen über einen EDU-Mandanten, die Richtlinie funktioniert aber nicht.

*Ihre IP wurde für das Aktivieren einer anzeigenfreien Suchoberfläche auf eine Whitelist gesetzt.

*Sie nutzten eine anzeigenfreie Suchumgebung in einer Microsoft Edge-Vorgängerversion und möchten ein Upgrade auf die neue Version von Microsoft Edge durchführen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: BingAdsSuppression
  - Gruppenrichtlinienname: Alle Werbeanzeigen in Bing-Suchergebnissen blockieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: BingAdsSuppression
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: BingAdsSuppression
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### BlockThirdPartyCookies
  #### Cookies von Drittanbietern blockieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Blockieren Sie das Festlegen von Cookies für Webseitenelemente, die nicht der Domäne in der Adressleiste angehören.

Wenn Sie diese Richtlinie aktivieren, können Webseitenelemente, die nicht der Domäne in der Adressleiste angehören, keine Cookies festlegen.

Wenn Sie diese Richtlinie deaktivieren, können Webseitenelemente, die Domänen angehören, die nicht in der Adressleiste enthalten sind, Cookies festlegen.

Wenn Sie diese Richtlinie nicht konfigurieren, sind Cookies von Drittanbietern aktiviert, aber Benutzer können diese Einstellung ändern.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: BlockThirdPartyCookies
  - Gruppenrichtlinienname: Cookies von Drittanbietern blockieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: BlockThirdPartyCookies
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: BlockThirdPartyCookies
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### BrowserAddProfileEnabled
  #### Profilerstellung über das Flyout-Menü „Identität” oder die Seite „Einstellungen” aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Ermöglicht Benutzern das Erstellen neuer Profile mithilfe der Option **Profil hinzufügen**.
Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer in Microsoft Edge die Option **Profil hinzufügen** im Flyoutmenü „Identität“ oder auf der Seite „Einstellungen“ verwenden, um neue Profile zu erstellen.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer keine neuen Profile über das Flyoutmenü „Identität“ oder die Seite „Einstellungen“ hinzufügen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: BrowserAddProfileEnabled
  - Gruppenrichtlinienname: Profilerstellung über das Flyout-Menü „Identität” oder die Seite „Einstellungen” aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: BrowserAddProfileEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: BrowserAddProfileEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### BrowserGuestModeEnabled
  #### Gastmodus aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Aktivieren Sie die Option, um die Verwendung von Gastprofilen in Microsoft Edge zu ermöglichen. In einem Gastprofil importiert der Browser keine Browserdaten aus vorhandenen Profilen und löscht die Browserdaten, wenn alle Gastprofile geschlossen werden.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, lässt Microsoft Edge das Surfen in Gastprofilen für Benutzer zu.

Wenn Sie diese Richtlinie deaktivieren, lässt Microsoft Edge das Surfen in Gastprofilen für Benutzer nicht zu.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: BrowserGuestModeEnabled
  - Gruppenrichtlinienname: Gastmodus aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: BrowserGuestModeEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: BrowserGuestModeEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### BrowserNetworkTimeQueriesEnabled
  #### Abfragen bei einem Browser-Netzwerk-Zeitdienst zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Verhindert, dass Microsoft Edge gelegentlich Abfragen an einen Browser-Netzwerkzeitdienst sendet, um einen genauen Zeitstempel abzurufen.

Wenn Sie diese Richtlinie deaktivieren, sendet Microsoft Edge keine Abfragen mehr an einen Browser-Netzwerkzeitdienst.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, sendet Microsoft Edge gelegentlich Abfragen an einen Browser-Netzwerkzeitdienst.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: BrowserNetworkTimeQueriesEnabled
  - Gruppenrichtlinienname: Abfragen bei einem Browser-Netzwerk-Zeitdienst zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: BrowserNetworkTimeQueriesEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: BrowserNetworkTimeQueriesEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### BrowserSignin
  #### Browser-Anmeldeeinstellungen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Mit dieser Richtlinie legen Sie fest, ob sich ein Benutzer mit seinem Konto bei Microsoft Edge anmelden und kontobezogene Dienste wie Synchronisieren und einmaliges Anmelden verwenden kann. Um die Verfügbarkeit der Synchronisierung zu steuern, verwenden Sie stattdessen die Richtlinie “[SyncDisabled](#syncdisabled)”.

Wenn Sie diese Richtlinie auf “Disable” festlegen, müssen Sie auch die Richtlinie “[NonRemovableProfileEnabled](#nonremovableprofileenabled)” deaktivieren, weil [NonRemovableProfileEnabled](#nonremovableprofileenabled) die Erstellung eines automatisch erstellten Browserprofils deaktiviert. Wenn beide Richtlinien aktiviert sind, verwendet Microsoft Edge die Einstellung “Browseranmeldung deaktivieren” und verhält sich so, als wäre [NonRemovableProfileEnabled](#nonremovableprofileenabled) deaktiviert.

Wenn Sie diese Richtlinie auf "Enable" setzen, können sich Benutzer im Browser anmelden. Die Anmeldung im Browser bedeutet nicht, dass die Synchronisierung standardmäßig aktiviert ist. Der Benutzer muss zusätzlich zustimmen, um dieses Feature nutzen zu können.

Wenn Sie diese Richtlinie auf "Force" festlegen, müssen sich Benutzer in einem Profil anmelden, um den Browser verwenden zu können. Der Benutzer kann somit standardmäßig zwischen der Synchronisierung mit seinem Konto (sofern sie nicht vom Domänenadministrator deaktiviert wurde) und der Richtlinie “[SyncDisabled](#syncdisabled)” wählen. Der Standardwert für die Richtlinie “[BrowserGuestModeEnabled](#browserguestmodeenabled)” ist “falsch”.

Wenn Sie diese Richtlinie nicht konfigurieren, kann der Benutzer entscheiden, ob er die Browseranmeldung aktivieren und nach eigenem Ermessen verwenden möchte.

Zuordnung der Richtlinienoptionen:

* Disable (0) = Browseranmeldung deaktivieren

* Enable (1) = Browseranmeldung ermöglichen

* Force (2) = Benutzeranmeldung für Browserverwendung erzwingen

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: BrowserSignin
  - Gruppenrichtlinienname: Browser-Anmeldeeinstellungen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: BrowserSignin
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000002
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: BrowserSignin
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### BuiltInDnsClientEnabled
  #### Integrierten DNS-Client verwenden
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Steuert, ob der integrierte DNS-Client verwendet werden soll.

Dies hat keinen Einfluss darauf, welche DNS-Server verwendet werden, sondern nur auf den Softwarestapel, der zur Kommunikation mit ihnen verwendet wird. Wenn das Betriebssystem beispielsweise für die Verwendung eines DNS-Unternehmensservers konfiguriert ist, wird dieser Server vom integrierten DNS-Client verwendet. Der integrierte DNS-Client kann Server jedoch auf unterschiedliche Weise adressieren, indem er modernere DNS-bezogene Protokolle wie DNS-over-TLS verwendet.

Wenn Sie diese Richtlinie aktivieren, wird der integrierte DNS-Client verwendet, sofern er verfügbar ist.

Wenn Sie diese Richtlinie deaktivieren, wird der Client nie verwendet.

Wenn Sie diese Richtlinie nicht konfigurieren, ist der integrierte DNS-Client unter MacOS standardmäßig aktiviert, und Benutzer können ändern, ob der integrierte DNS-Client verwendet wird, indem sie edge://flags bearbeiten oder ein Befehlszeilenflag angeben.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: BuiltInDnsClientEnabled
  - Gruppenrichtlinienname: Integrierten DNS-Client verwenden
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: BuiltInDnsClientEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: BuiltInDnsClientEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### BuiltinCertificateVerifierEnabled
  #### Ermittelt, ob die integrierte Zertifikatsprüfung zum Bestätigen von Serverzertifikaten verwendet wird. (veraltet)
  >VERALTET: Diese Richtlinie ist veraltet. Sie wird gegenwärtig noch unterstützt, aber in einem zukünftigen Release ausgemustert.
  
  #### Unterstützte Versionen:
  - Unter macOS seit Version 83 oder höher

  #### Beschreibung
  Diese Richtlinie ist veraltet, da sie nur als kurzfristiger Mechanismus dienen soll, um Unternehmen mehr Zeit zu geben, ihre Umgebungen zu aktualisieren und Probleme zu melden, wenn sich herausstellt, dass sie mit der integrierten Zertifikatsprüfung nicht kompatibel sind.

Dies funktioniert nicht in Microsoft Edge Version 87, wenn die Unterstützung für die Vorgänger-Zertifikatsprüfung unter Mac OS X entfernt werden soll.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  

  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: BuiltinCertificateVerifierEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### CertificateTransparencyEnforcementDisabledForCas
  #### Erzwingung der Zertifikattransparenz für eine Liste von subjectPublicKeyInfo-Hashes deaktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Deaktiviert die Erzwingung der Zertifikatstransparenzanforderungen für eine Liste von subjectPublicKeyInfo-Hashes.

Mit dieser Richtlinie können Sie die Offenlegungsanforderungen für die Zertifikatstransparenz für Zertifikatketten deaktivieren, die Zertifikate mit einem der angegebenen subjectPublicKeyInfo-Hashes enthalten. Auf diese Weise können Zertifikate, die ansonsten nicht vertrauenswürdig wären, weil sie nicht ordnungsgemäß öffentlich bekannt gegeben wurden, weiterhin für Enterprise-Hosts verwendet werden.

Um die Erzwingung der Zertifikatstransparenz zu deaktivieren, wenn diese Richtlinie festgelegt ist, muss eine der folgenden Bedingungen erfüllt sein:
1. Der Hash muss im subjectPublicKeyInfo-Element des Serverzertifikats enthalten sein.
2. Der Hash muss in einem subjectPublicKeyInfo-Element enthalten sein, das in einem Zertifizierungsstellenzertifikat in der Zertifikatkette enthalten ist, das Zertifizierungsstellenzertifikat muss durch die X.509v3-Erweiterung „nameConstraints“ beschränkt sein, „permittedSubtrees“ muss mindestens eine Namensbeschränkung vom Typ „directoryName“ enthalten, und „directoryName“ muss ein organizationName-Attribut enthalten.
3. Der Hash muss in einem subjectPublicKeyInfo-Element enthalten sein, das in einem Zertifizierungsstellenzertifikat in der Zertifikatkette enthalten ist, der Antragsteller des Zertifizierungsstellenzertifikats muss mindestens ein organizationName-Attribut enthalten, und das Zertifikat des Servers muss die gleiche Anzahl von organizationName-Attributen enthalten (in der gleichen Reihenfolge und Byte für Byte identisch).

Zur Angabe eines subjectPublicKeyInfo-Hashs werden der Name des Hashalgorithmus, das Zeichen „/“ und die Base64-Codierung des Hashalgorithmus verkettet, der auf das DER-codierte subjectPublicKeyInfo-Element des angegebenen Zertifikats angewendet wurde. Diese Base64-Codierung hat das gleiche Format wie ein SPKI-Fingerabdruck gemäß Definition in RFC 7469, Abschnitt 2.4. Nicht erkannte Hashalgorithmen werden ignoriert. Aktuell wird nur der Hashalgorithmus „sha256“ unterstützt.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden alle Zertifikate, die über Certificate Transparency offengelegt werden müssen, als nicht vertrauenswürdig behandelt, wenn sie nicht gemäß der Certificate Transparency-Richtlinie offengelegt werden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: CertificateTransparencyEnforcementDisabledForCas
  - Gruppenrichtlinienname: Erzwingung der Zertifikattransparenz für eine Liste von subjectPublicKeyInfo-Hashes deaktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\2 = "sha256//////////////////////w=="

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: CertificateTransparencyEnforcementDisabledForCas
  - Beispielwert:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### CertificateTransparencyEnforcementDisabledForLegacyCas
  #### Erzwingung der Zertifikattransparenz für eine Liste der Legacy-Zertifizierungsstellen deaktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Deaktiviert die Erzwingung der Zertifikattransparenz-Anforderungen für eine Liste der Legacy-Zertifizierungsstellen (Cas).

Mit dieser Richtlinie können Sie die Offenlegungsanforderungen für die Zertifikattransparenz für Zertifikatketten deaktivieren, die Zertifikate mit einem der angegebenen subjectPublicKeyInfo-Hashes enthalten. Dadurch können Zertifikate, die ansonsten nicht vertrauenswürdig wären, da Sie nicht ordnungsgemäß veröffentlicht wurden, weiterhin für Unternehmens-Hosts verwendet werden.

Damit die Erzwingung der Zertifikattransparenz deaktiviert werden kann, müssen Sie den Hash auf einen subjectPublicKeyInfo festlegen, der in einem Zertifizierungsstellenzertifikat angezeigt wird, das als eine Legacy-Zertifizierungsstelle (Certification Authority, CA) erkannt wird. Eine Legacy-CA ist eine CA, die standardmäßig von mindestens einem der von Microsoft Edge unterstützten Betriebssysteme als vertrauenswürdig eingestuft wurde.

Sie geben einen subjectPublicKeyInfo-Hash an, indem Sie den Hashalgorithmusnamen, das Zeichen "/" und die Base64-Codierung dieses Hashalgorithmus, die auf den DER-codierten subjectPublicKeyInfo des angegebenen Zertifikats angewendet wurde, verketten. Diese Base64-Codierung hat das gleiche Format wie ein SPKI-Fingerabdruck gemäß der Definition in RFC 7469, Abschnitt 2.4. Nicht erkannte Hashalgorithmen werden ignoriert. Der einzige unterstützte Hashalgorithmus ist zu diesem Zeitpunkt "sha256".

Wenn Sie diese Richtlinie nicht konfigurieren, wird jedes Zertifikat, das über die Zertifikattransparenz offengelegt werden muss, als nicht vertrauenswürdig eingestuft, wenn es nicht gemäß der Zertifikattransparenz-Richtlinie offengelegt wird.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Gruppenrichtlinienname: Erzwingung der Zertifikattransparenz für eine Liste der Legacy-Zertifizierungsstellen deaktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\2 = "sha256//////////////////////w=="

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Beispielwert:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### CertificateTransparencyEnforcementDisabledForUrls
  #### Erzwingung der Zertifikattransparenz für bestimmte URLs deaktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Deaktiviert die Erzwingung der Certificate Transparency-Anforderungen für die aufgeführten URLs.

Mit dieser Richtlinie können Sie die Offenlegung von Zertifikaten für die Hostnamen in den angegebenen URLs über Certificate Transparency verhindern. Dies ermöglicht die Verwendung von Zertifikaten, die andernfalls als nicht vertrauenswürdig eingestuft würden, da sie nicht ordnungsgemäß offengelegt wurden. Gleichzeitig wird jedoch die Erkennung nicht korrekt ausgestellter Zertifikate für diese Hosts erschwert.

Orientieren Sie sich bei Ihrem URL-Muster an „[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)“. Da Zertifikate für einen bestimmten Hostnamen gültig sind (unabhängig von Schema, Port oder Pfad), wird lediglich der Hostnamenteil der URL berücksichtigt. Platzhalterhosts werden nicht unterstützt.

Wenn Sie diese Richtlinie nicht konfigurieren, wird jedes Zertifikat, das über Certificate Transparency offengelegt werden muss, als nicht vertrauenswürdig behandelt, wenn es nicht offengelegt wird.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: CertificateTransparencyEnforcementDisabledForUrls
  - Gruppenrichtlinienname: Erzwingung der Zertifikattransparenz für bestimmte URLs deaktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\2 = ".contoso.com"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: CertificateTransparencyEnforcementDisabledForUrls
  - Beispielwert:
``` xml
<array>
  <string>contoso.com</string>
  <string>.contoso.com</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ClearBrowsingDataOnExit
  #### Browserdaten löschen, wenn Microsoft Edge geschlossen wird
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 78 oder höher

  #### Beschreibung
  Microsoft Edge löscht die Browserdaten beim Schließen nicht standardmäßig. Zu den Browserdaten zählen Informationen, die Sie in Formulare eingegeben haben, Passwörter und die besuchten Websites.

Wenn Sie diese Richtlinie aktivieren, werden alle Browserdaten gelöscht, wenn Sie Microsoft Edge schließen. Hinweis: Wenn diese Richtlinie aktiviert ist, hat sie Vorrang vor der Konfiguration von [DefaultCookiesSetting](#defaultcookiessetting)

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, können Benutzer die Option "Browserdaten löschen" in den Einstellungen konfigurieren.

Wenn Sie diese Richtlinie aktivieren, konfigurieren Sie nicht die Richtlinie [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) oder [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit), da beide Richtlinien das Löschen von Daten steuern. Wenn Sie beide sowie diese aktivieren, werden alle Daten gelöscht, wenn Microsoft Edge geschlossen wird, unabhängig davon, wie [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) oder [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit) konfiguriert ist.

Um Cookies von der Löschung beim Beenden auszuschließen, konfigurieren Sie die Richtlinie [SaveCookiesOnExit](#savecookiesonexit).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ClearBrowsingDataOnExit
  - Gruppenrichtlinienname: Browserdaten löschen, wenn Microsoft Edge geschlossen wird
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: ClearBrowsingDataOnExit
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ClearBrowsingDataOnExit
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ClearCachedImagesAndFilesOnExit
  #### Löschen von zwischengespeicherten Bildern und Dateien nach dem Schließen von Microsoft Edge
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 83 oder höher

  #### Beschreibung
  Microsoft Edge löscht beim Schließen keine zwischengespeicherten Bilder und Dateien.

Falls Sie diese Richtlinie aktivieren, werden zwischengespeicherte Bilder und Dateien jedes Mal gelöscht, wenn Microsoft Edge geschlossen wird.

Falls Sie diese Richtlinie deaktivieren, können Benutzer die Option „Zwischengespeicherte Bilder und Dateien“ in edge://settings/clearBrowsingDataOnClose nicht konfigurieren.

Falls Sie diese Richtlinie nicht konfigurieren, können Benutzer wählen, ob zwischengespeicherte Bilder und Dateien beim Beenden gelöscht werden.

Falls Sie diese Richtlinie deaktivieren, aktivieren Sie die Richtlinie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) nicht, da beide sich mit dem Löschen von Daten befassen. Falls Sie beide konfigurieren, erhält die Richtlinie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) Vorrang und löscht alle Daten, wenn Microsoft Edge geschlossen wird, ungeachtet Ihrer Konfiguration von [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ClearCachedImagesAndFilesOnExit
  - Gruppenrichtlinienname: Löschen von zwischengespeicherten Bildern und Dateien nach dem Schließen von Microsoft Edge
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: ClearCachedImagesAndFilesOnExit
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ClearCachedImagesAndFilesOnExit
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ClickOnceEnabled
  #### Benutzern das Öffnen von Dateien unter Verwendung des ClickOnce-Protokolls ermöglichen
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 78 oder höher

  #### Beschreibung
  Ermöglicht Benutzern das Öffnen von Dateien unter Verwendung des ClickOnce-Protokolls. Mit dem ClickOnce-Protokoll können Websites anfordern, dass der Browser Dateien von einer bestimmten URL öffnet und dabei den ClickOnce-Dateihandler auf dem Computer oder Gerät des Benutzers verwendet.

Wenn Sie diese Richtlinie aktivieren, können Benutzer Dateien unter Verwendung des ClickOnce-Protokolls öffnen. Diese Richtlinie überschreibt die ClickOnce-Einstellung des Benutzers auf der Seite edge://flags/“.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer keine Dateien unter Verwendung des ClickOnce-Protokolls öffnen. Die Datei wird stattdessen über den Browser im Dateisystem gespeichert. Diese Richtlinie überschreibt die ClickOnce-Einstellung des Benutzers auf der Seite edge://flags/“.

Wenn Sie diese Richtlinie nicht konfigurieren, können Benutzer mit der Version Microsoft Edge vor Microsoft Edge 87 standardmäßig keine Dateien unter Verwendung des ClickOnce-Protokolls öffnen. Diese Benutzer haben jedoch die Möglichkeit, die Verwendung des ClickOnce-Protokolls auf der Seite edge://flags/“ zu aktivieren. Benutzer mit Microsoft Edge Versionen 87 und später können unter Verwendung des ClickOnce-Protokolls standardmäßig Dateien öffnen, haben jedoc nicht die Option, das ClickOnce-Protokoll auf der Seite edge://flags/ zu deaktivieren.

Ist ClickOnce deaktiviert, können ClickOnce-Anwendungen (APPLICATION-Dateien) möglicherweise nicht ordnungsgemäß gestartet werden.

Weitere Informationen zu ClickOnce finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) and [https://go.microsoft.com/fwlink/?linkid=2099880](https://go.microsoft.com/fwlink/?linkid=2099880).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ClickOnceEnabled
  - Gruppenrichtlinienname: Benutzern das Öffnen von Dateien unter Verwendung des ClickOnce-Protokolls ermöglichen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ClickOnceEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### CollectionsServicesAndExportsBlockList
  #### Zugriff auf eine angegebene Liste von Diensten blockieren und Ziele in Sammlungen exportieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 86 oder höher

  #### Beschreibung
  Listet bestimmte Dienste und Exportziele auf, auf die Benutzer im Feature "Sammlungen" in Microsoft Edge nicht zugreifen können. Dies umfasst die Anzeige zusätzlicher Daten von Bing und das Exportieren von Sammlungen in Microsoft-Produkte oder zu externen Partnern.

Wenn Sie diese Richtlinie aktivieren, werden Dienste und Exportziele blockiert, die mit der angegebenen Liste übereinstimmen.

Wenn Sie diese Richtlinie nicht konfigurieren, werden keine Einschränkungen für die zulässigen Dienste und Exportziele erzwungen.

Zuordnung der Richtlinienoptionen:

* pinterest_suggestions (pinterest_suggestions) = Pinterest-Vorschläge

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: CollectionsServicesAndExportsBlockList
  - Gruppenrichtlinienname: Zugriff auf eine angegebene Liste von Diensten blockieren und Ziele in Sammlungen exportieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\1 = "pinterest_suggestions"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: CollectionsServicesAndExportsBlockList
  - Beispielwert:
``` xml
<array>
  <string>pinterest_suggestions</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### CommandLineFlagSecurityWarningsEnabled
  #### Aktivieren von Sicherheitswarnungen für Befehlszeilenflags
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 78 oder höher

  #### Beschreibung
  Wenn diese Richtlinie deaktiviert ist, wird verhindert, dass Sicherheitswarnungen angezeigt werden, wenn Microsoft Edge mit potenziell gefährlichen Befehlszeilenflags gestartet wird.

    Wenn diese Option aktiviert oder nicht festgelegt ist, werden Sicherheitswarnungen angezeigt, wenn diese Befehlszeilenflags zum Starten von Microsoft Edge verwendet werden.

    Beispielsweise generiert das Flag "--disable-gpu-sandbox" die folgende Warnung: “Sie verwenden ein nicht unterstütztes Befehlszeilenflag: --disable-gpu-sandbox. Dies stellt ein Stabilitäts- und Sicherheitsrisiko dar.”

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: CommandLineFlagSecurityWarningsEnabled
  - Gruppenrichtlinienname: Aktivieren von Sicherheitswarnungen für Befehlszeilenflags
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: CommandLineFlagSecurityWarningsEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: CommandLineFlagSecurityWarningsEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ComponentUpdatesEnabled
  #### Komponentenupdates in Microsoft Edge aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, werden Komponentenupdates in Microsoft Edge aktiviert.

Wenn Sie diese Richtlinie deaktivieren oder auf „false” festlegen, werden Komponentenupdates für alle Komponenten in Microsoft Edge deaktiviert.

Einige Komponenten sind jedoch von dieser Richtlinie ausgenommen. Dazu gehören alle Komponenten, die keinen ausführbaren Code enthalten, die das Verhalten des Browsers nicht wesentlich verändern oder die für die Sicherheit von entscheidender Bedeutung sind. Das heißt, Updates, die als „sicherheitskritisch” eingestuft sind, werden auch dann angewendet, wenn Sie diese Richtlinie deaktivieren.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ComponentUpdatesEnabled
  - Gruppenrichtlinienname: Komponentenupdates in Microsoft Edge aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ComponentUpdatesEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ComponentUpdatesEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ConfigureDoNotTrack
  #### Nicht verfolgen (Do not track) konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Geben Sie an, ob „Nicht verfolgen“-Anfragen an Websites gesendet werden sollen, die um Nachverfolgungsinformationen bitten. „Nicht verfolgen“-Anfragen informieren die von Ihnen besuchten Websites, dass Ihre Browseraktivitäten nicht nachverfolgt werden sollen. Standardmäßig sendet Microsoft Edge keine „Nicht verfolgen“-Anfragen, Benutzer können dieses Feature allerdings aktivieren, damit sie gesendet werden.

Wenn Sie diese Richtlinie aktivieren, werden „Nicht verfolgen“-Anfragen immer an Websites gesendet, die um Nachverfolgungsinformationen bitten.

Wenn Sie diese Richtlinie deaktivieren, werden nie Anfragen gesendet.

Wenn Sie diese Richtlinie nicht konfigurieren, können Benutzer auswählen, ob diese Anfragen gesendet werden sollen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ConfigureDoNotTrack
  - Gruppenrichtlinienname: Nicht verfolgen (Do not track) konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ConfigureDoNotTrack
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ConfigureDoNotTrack
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ConfigureOnPremisesAccountAutoSignIn
  #### Automatische Anmeldung mit einem Active Directory-Domänenkonto konfigurieren, wenn kein Azure AD-Domänenkonto vorhanden ist
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 81 oder höher

  #### Beschreibung
  Mit dieser Richtlinie ermöglichen Sie die Verwendung von Active Directory-Konten für die automatische Anmeldung, wenn die Computer Ihrer Benutzer in die Domäne eingebunden sind und Ihre Umgebung nicht hybrid eingebunden ist. Wenn Benutzer stattdessen automatisch mit ihren Azure Active Directory-Konten angemeldet werden sollen, führen Sie für Ihre Umgebung eine Azure AD-Einbindung (weitere Informationen unter [https://go.microsoft.com/fwlink/?linkid=2118197](https://go.microsoft.com/fwlink/?linkid=2118197)) bzw. eine Azure AD-Hybrideinbindung (weitere Informationen unter [https://go.microsoft.com/fwlink/?linkid=2118365](https://go.microsoft.com/fwlink/?linkid=2118365)) durch.

Wenn Sie die Richtlinie “[BrowserSignin](#browsersignin)” deaktiviert haben, hat sie keine Auswirkung.

Wenn Sie diese Richtlinie aktivieren und auf “'SignInAndMakeDomainAccountNonRemovable“ festlegen, werden Benutzer mit in die Domäne eingebundenen Computern von “Microsoft Edge” automatisch unter Verwendung ihrer Active Directory-Konten angemeldet.

Wenn Sie diese Richtlinie auf “Disabled“ festlegen oder nicht konfigurieren, meldet “Microsoft Edge” Benutzer mit in die Domäne eingebundenen Computern mit Active Directory-Konten nicht automatisch an.

Zuordnung der Richtlinienoptionen:

* Disabled (0) = Deaktiviert

* SignInAndMakeDomainAccountNonRemovable (1) = Anmelden und Domänenkonto als nicht entfernbar festlegen

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ConfigureOnPremisesAccountAutoSignIn
  - Gruppenrichtlinienname: Automatische Anmeldung mit einem Active Directory-Domänenkonto konfigurieren, wenn kein Azure AD-Domänenkonto vorhanden ist
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ConfigureOnPremisesAccountAutoSignIn
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ConfigureOnlineTextToSpeech
  #### Online-Text-zu-Sprache konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Legt fest, ob der Browser Online Text to Speech-Sprachfonts nutzen kann, die Teil der Azure Cognitive Services sind. Diese Sprachfonts sind qualitativ hochwertiger als die vorinstallierten Systemschriftarten.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können webbasierte Anwendungen, die die SpeechSynthesis-API einsetzen, Online Text to Speech-Sprachfonts verwenden.

Wenn Sie diese Richtlinie deaktivieren, sind die Sprachfonts nicht verfügbar.

Lesen Sie hier mehr über diese Funktion:
SpeechSynthesis API: [https://go.microsoft.com/fwlink/?linkid=2110038](https://go.microsoft.com/fwlink/?linkid=2110038)
Cognitive Services: [https://go.microsoft.com/fwlink/?linkid=2110141](https://go.microsoft.com/fwlink/?linkid=2110141)

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ConfigureOnlineTextToSpeech
  - Gruppenrichtlinienname: Online-Text-zu-Sprache konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ConfigureOnlineTextToSpeech
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ConfigureOnlineTextToSpeech
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ConfigureShare
  #### Freigabefunktion konfigurieren
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 83 oder höher

  #### Beschreibung
  Wenn Sie diese Richtlinie auf "ShareAllowed" (die Standardeinstellung) festlegen, können die Benutzer über das Menü “”Einstellungen und mehr” in Microsoft Edge auf die Windows 10-Freigabefunktion zugreifen, um anderen Apps im System die Freigabe zu ermöglichen.

Wenn Sie diese Richtlinie auf "ShareDisallowed" festlegen, können die Benutzer nicht auf die Windows 10-Freigabefunktion zugreifen. Wenn sich die Schaltfläche "Freigeben" auf der Symbolleiste befindet, wird Sie ebenfalls ausgeblendet.

Zuordnung der Richtlinienoptionen:

* ShareAllowed (0) = Verwendung der Freigabefunktion zulassen

* ShareDisallowed (1) = Verwendung der Freigabefunktion nicht zulassen

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ConfigureShare
  - Gruppenrichtlinienname: Freigabefunktion konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ConfigureShare
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### CustomHelpLink
  #### Benutzerdefinierten Hilfelink angeben
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 79 oder höher

  #### Beschreibung
  Gibt einen Link für das Hilfemenü oder die F1-Taste an.

Wenn Sie diese Richtlinie aktivieren, kann ein Administrator einen Link für das Hilfemenü oder die F1-Taste angeben.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird der Standard-Link für das Hilfemenü oder die F1-Taste verwendet.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: CustomHelpLink
  - Gruppenrichtlinienname: Benutzerdefinierten Hilfelink angeben
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: CustomHelpLink
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"https://go.microsoft.com/fwlink/?linkid=2080734"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: CustomHelpLink
  - Beispielwert:
``` xml
<string>https://go.microsoft.com/fwlink/?linkid=2080734</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DNSInterceptionChecksEnabled
  #### Überprüfungen auf DNS-Abfangvorgänge aktiviert
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 80 oder höher

  #### Beschreibung
  Mit dieser Richtlinie wird ein lokaler Switch konfiguriert, mit dem Überprüfungen auf DNS-Abfangvorgänge deaktiviert werden können. Mit diesen Überprüfungen soll ermittelt werden, ob sich der Browser hinter einem Proxy befindet, von dem unbekannte Hostnamen umgeleitet werden.

Diese Erkennung ist in einer Unternehmensumgebung, in der die Netzwerkkonfiguration bekannt ist, unter Umständen nicht erforderlich. Sie kann deaktiviert werden, um zu vermeiden, dass beim Starten und bei jeder Änderung der DNS-Konfiguration zusätzlicher DNS- und HTTP-Datenverkehr anfällt.

Wenn Sie diese Richtlinie aktivieren oder nicht festlegen, werden die Überprüfungen auf DNS-Abfangvorgänge durchgeführt.

Wenn Sie diese Richtlinie deaktivieren, werden die Überprüfungen auf DNS-Abfangvorgänge nicht durchgeführt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DNSInterceptionChecksEnabled
  - Gruppenrichtlinienname: Überprüfungen auf DNS-Abfangvorgänge aktiviert
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DNSInterceptionChecksEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DNSInterceptionChecksEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultBrowserSettingEnabled
  #### Microsoft Edge als Standardbrowser festlegen
  
  
  #### Unterstützte Versionen:
  - Bei Windows 7 und macOS seit 77 oder höher

  #### Beschreibung
  Wenn Sie diese Richtlinie auf “wahr” setzen, überprüft Microsoft Edge beim Start jedes Mal, ob es der Standardbrowser ist, und registriert sich automatisch.

Wenn Sie diese Richtlinie auf “falsch” setzen, prüft Microsoft Edge nie, ob es der Standardbrowser ist und deaktiviert die Benutzersteuerelemente für diese Option.

Wenn Sie diese Richtlinie nicht konfigurieren, erlaubt es Microsoft Edge dem Benutzer zu entscheiden, ob es der Standardbrowser sein soll und ob Benutzerbenachrichtigungen angezeigt werden sollen, wenn dies nicht der Fall ist.

Hinweis für Windows-Administratoren: Diese Richtlinie funktioniert nur für PCs mit Windows 7. Für spätere Windows-Versionen müssen Sie eine "Standardanwendungszuordnungsdatei" bereitstellen, die Microsoft Edge als den Handler für die https- und http-Protokolle (und optional das FTP-Protokoll und für Dateiformate wie .html, .htm, .pdf, .svg, .webp) festlegt. Weitere Informationen finden Sie unter "[https://go.microsoft.com/fwlink/?linkid=2094932](https://go.microsoft.com/fwlink/?linkid=2094932)".

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultBrowserSettingEnabled
  - Gruppenrichtlinienname: Microsoft Edge als Standardbrowser festlegen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DefaultBrowserSettingEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultBrowserSettingEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultSearchProviderContextMenuAccessAllowed
  #### Standardsuchanbieter Zugriff auf die Suche im Kontextmenü gestatten
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 85 oder höher

  #### Beschreibung
  Aktiviert die Verwendung eines Standardsuchanbieters im Kontextmenü.

Wenn Sie diese Richtlinie deaktivieren, wird das Kontextmenüelement “Suche”, das auf den Standardsuchanbieter zurückgreift, deaktiviert. Auch die Suche in der Randleiste ist nicht verfügbar.

Wenn Sie diese Richtlinie aktivieren oder nicht festgelegen, sind das Kontextmenüelementelement für den Standardsuchanbieter und die Suche in der Randleiste verfügbar.

Der Richtlinienwert wird nur angewendet, wenn die Richtlinie “[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)” aktiviert und nicht andernfalls anwendbar ist.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultSearchProviderContextMenuAccessAllowed
  - Gruppenrichtlinienname: Standardsuchanbieter Zugriff auf die Suche im Kontextmenü gestatten
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DefaultSearchProviderContextMenuAccessAllowed
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultSearchProviderContextMenuAccessAllowed
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultSensorsSetting
  #### Default sensors setting
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 86 oder höher

  #### Beschreibung
  Set whether websites can access and use sensors such as motion and light sensors. You can completely block or allow websites to get access to sensors.

Setting the policy to 1 lets websites access and use sensors. Setting the policy to 2 denies acess to sensors.

You can override this policy for specific URL patterns by using the [SensorsAllowedForUrls](#sensorsallowedforurls) and [SensorsBlockedForUrls](#sensorsblockedforurls) policies.

If you don't configure this policy, websites can access and use sensors, and users can change this setting. This is the global default for [SensorsAllowedForUrls](#sensorsallowedforurls) and [SensorsBlockedForUrls](#sensorsblockedforurls).

Zuordnung der Richtlinienoptionen:

* AllowSensors (1) = Allow sites to access sensors

* BlockSensors (2) = Do not allow any site to access sensors

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultSensorsSetting
  - Gruppenrichtlinienname: Default sensors setting
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DefaultSensorsSetting
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000002
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultSensorsSetting
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DefaultSerialGuardSetting
  #### Verwendung der API für den seriellen Anschluss steuern
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 86 oder höher

  #### Beschreibung
  Legt fest, ob Websites auf serielle Anschlüsse zugreifen können. Sie können den Zugriff vollständig blockieren oder den Benutzer jedes Mal fragen, wenn eine Website Zugriff auf einen seriellen Anschluss haben möchte.

Wenn Sie die Richtlinie auf 3 festlegen, können Websites den Zugriff auf serielle Anschlüsse anfordern. Durch Festlegen der Richtlinie auf 2 wird der Zugriff auf serielle Anschlüsse verweigert.

Sie können die Richtlinie für bestimmte URL-Muster mithilfe der Richtlinien [SerialAskForUrls](#serialaskforurls) und [SerialBlockedForUrls](#serialblockedforurls) außer Kraft setzen.

Wenn Sie diese Richtlinie nicht konfigurieren, können Websites Benutzer fragen, ob sie auf einen seriellen Anschluss zugreifen können und Benutzer können diese Einstellung ändern.

Zuordnung der Richtlinienoptionen:

* BlockSerial (2) = Keiner Website erlauben, dass Zugriff auf serielle Anschlüsse angefordert wird

* AskSerial (3) = Zulassen, dass Websites nach Benutzerberechtigung für den Zugriff auf einen seriellen Anschluss fragen

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DefaultSerialGuardSetting
  - Gruppenrichtlinienname: Verwendung der API für den seriellen Anschluss steuern
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DefaultSerialGuardSetting
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000002
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DefaultSerialGuardSetting
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DelayNavigationsForInitialSiteListDownload
  #### Voraussetzen, dass die Website-Liste zum Unternehmensmodus vor der Registerkartennavigation verfügbar ist
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 84 oder höher

  #### Beschreibung
  Diese Richtlinie ermöglicht es Ihnen anzugeben, ob Registerkarten von Microsoft Edge darauf warten, bis der Browser die anfängliche Website-Liste für den Unternehmensmodus heruntergeladen hat. Diese Einstellung ist für das Szenario vorgesehen, in dem die Startseite des Browsers im Internet Explorer-Modus geladen werden soll, und es ist wichtig, dass dies im Browser als Erstes ausgeführt wird, nachdem der IE-Modus aktiviert ist. Wenn dieses Szenario nicht vorhanden ist, empfiehlt es sich, diese Einstellung nicht zu aktivieren, da sich dies negativ auf die Ladeleistung der Startseite auswirken kann. Die Einstellung funktioniert nur, wenn bei der ersten Ausführung des Browsers, nachdem der IE-Modus aktiviert wurde, unter Microsoft Edge keine Website-Liste für den Unternehmensmodus zwischengespeichert ist.

Diese Einstellung funktioniert gemeinsam mit:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel), festgelegt auf den Modus “IEMode”
       und
       [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)-Richtlinie, bei der die Liste mindestens einen Eintrag enthält.

       Das Timeout-Verhalten dieser Richtlinie kann mithilfe der Richtlinie “[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)” konfiguriert werden.

       Wenn Sie diese Richtlinie auf “All” festlegen und “Microsoft Edge” nicht über eine zwischengespeicherte Version der Website-Liste für den Unternehmensmodus verfügt, verzögern Registerkarten die Navigation, bis der Browser die Website-Liste heruntergeladen hat. Websites, die so konfiguriert sind, dass sie über die Website-Liste im Internet Explorer-Modus geöffnet werden, werden auch während der anfänglichen Navigation im Browser im Internet Explorer-Modus geladen. Websites, die möglicherweise nicht konfiguriert werden können, um sie im Internet Explorer zu öffnen, z. B. jede-Website mit einem anderen Schema als “http:”, “https:”, “file:” oder “ftp:”, verzögern das Navigieren nicht und werden sofort im Edge-Modus geladen.

       Wenn Sie diese Richtlinie auf “None” setzen oder nicht konfigurieren, oder wenn “Microsoft Edge” nicht über eine zwischengespeicherte Version der-Website-Liste für den Unternehmensmodus verfügt, navigieren die Registerkarten sofort, und Sie müssen nicht warten, bis der Browser die Website-Liste für den Unternehmensmodus heruntergeladen hat. Websites, die so konfiguriert sind, dass sie über die Website-Liste im Internet Explorer-Modus geöffnet werden, werden im Microsoft Edge-Modus geöffnet, bis der Browser den Download der Website-Liste für den Unternehmensmodus abgeschlossen hat.

Zuordnung der Richtlinienoptionen:

* None (0) = Keine

* All (1) = Alle berechtigten Navigationselemente

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DelayNavigationsForInitialSiteListDownload
  - Gruppenrichtlinienname: Voraussetzen, dass die Website-Liste zum Unternehmensmodus vor der Registerkartennavigation verfügbar ist
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DelayNavigationsForInitialSiteListDownload
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DeleteDataOnMigration
  #### Alte Browserdaten bei der Migration löschen
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 83 oder höher

  #### Beschreibung
  Diese Richtlinie bestimmt, ob Benutzerbrowserdaten von Microsoft Edge-Vorgängerversionen nach der Migration zu Microsoft Edge Version 81 oder gelöscht werden.

Falls Sie diese Richtlinie auf "Aktiviert" setzen, werden alle Browserdaten von Microsoft Edge-Vorgängerversionen nach der Migration zu Microsoft Edge Version 81 oder höher gelöscht. Diese Richtlinie muss vor der Migration zu Microsoft Edge Version 81 oder höher festgelegt werden, damit sie sich auf vorhandene Browserdaten auswirkt.

Falls Sie diese Richtlinie auf "Deaktiviert" setzen oder die Richtlinie nicht konfiguriert ist, werden nach der Migration zu Microsoft Edge Version 83 oder höher keine Benutzerbrowserdaten gelöscht.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DeleteDataOnMigration
  - Gruppenrichtlinienname: Alte Browserdaten bei der Migration löschen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DeleteDataOnMigration
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DeveloperToolsAvailability
  #### Steuern, wo Entwicklungstools verwendet werden können
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Diese Richtlinie steuert, wo Entwicklertools verwendet werden können.

Wenn Sie diese Richtlinie auf "DeveloperToolsDisallowedForForceInstalledExtensions" (Standardeinstellung) festlegen, können Benutzer im Allgemeinen auf die Entwicklertools und die JavaScript-Konsole zugreifen, jedoch nicht im Kontext von Erweiterungen, die von der Unternehmensrichtlinie installiert werden.

Wenn Sie diese Richtlinie auf "DeveloperToolsAllowed" festlegen, können Benutzer in allen Kontexten, einschließlich der von der Unternehmensrichtlinie installierten Erweiterungen, auf die Entwicklertools und die JavaScript-Konsole zugreifen.

Wenn Sie diese Richtlinie auf "DeveloperToolsDisallowed" festlegen, können Benutzer nicht auf die Entwicklertools zugreifen oder Websiteelemente überprüfen. Tastenkombinationen und Menü- oder Kontextmenüeinträge, die die Entwicklertools oder die JavaScript-Konsole öffnen, sind deaktiviert.

Zuordnung der Richtlinienoptionen:

* DeveloperToolsDisallowedForForceInstalledExtensions (0) = Entwicklertools für Erweiterungen blockieren, die von der Unternehmensrichtlinie installiert werden, in anderen Kontexten zulassen

* DeveloperToolsAllowed (1) = Verwendung der Entwicklertools zulassen

* DeveloperToolsDisallowed (2) = Verwendung der Entwicklungstools nicht zulassen

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DeveloperToolsAvailability
  - Gruppenrichtlinienname: Steuern, wo Entwicklungstools verwendet werden können
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DeveloperToolsAvailability
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000002
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DeveloperToolsAvailability
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DiagnosticData
  #### Erforderliche und optionale Diagnosedaten über die Browsernutzung senden
  
  
  #### Unterstützte Versionen:
  - Bei Windows 7 und macOS seit 86 oder höher

  #### Beschreibung
  Mit dieser Richtlinie wird gesteuert, wie erforderliche und optionale Diagnosedaten zur Browsernutzung an Microsoft gesendet werden.

Erforderliche Diagnosedaten werden gesammelt, um Microsoft Edge sicher und auf dem neuesten Stand zu halten und für eine ordnungsgemäße Ausführung zu sorgen.

Optionale Diagnosedaten umfassen Daten darüber, wie Sie den Browser nutzen, von Ihnen besuchte Websites sowie Absturzberichte. Diese werden an Microsoft gesendet, um Produkte und Dienstleistungen zu verbessern.

Diese Richtlinie wird auf Windows 10-Geräten nicht unterstützt. Um diese Datensammlung unter Windows 10 zu steuern, müssen IT-Administratoren die Gruppenrichtlinie "Windows-Diagnosedaten" verwenden. Diese Richtlinie lautet je nach Windows-Version entweder "Telemetrie zulassen" oder "Diagnosedaten zulassen". Erfahren Sie mehr über die Windows 10 Diagnosedatensammlung unter: https://go.Microsoft.com/fwlink/?linkid=2099569

Verwenden Sie eine der folgenden Einstellungen, um diese Richtlinie zu konfigurieren:

"Off"      deaktiviert die erforderliche und optionale Sammlung von Diagnosedaten. Diese Option wird nicht empfohlen.

"Erforderliche Daten" sendet die erforderlichen Diagnosedaten, deaktiviert aber die Sammlung optionaler Diagnosedaten. Microsoft Edge sendet die erforderlichen Diagnosedaten, um sicherzustellen, dass Microsoft Edge immer sicher und auf dem neuesten Stand ist und ordnungsgemäß ausgeführt wird.

"Optionale Daten": Optionale Diagnosedaten werden gesendet. Dies umfasst Daten zur Browsernutzung und zu besuchten Websites sowie Absturzberichte. Dieser werden an Microsoft gesendet, um Produkte und Dienstleistungen zu verbessern.

Unter Windows 7/macOS werden mit dieser Richtlinie das Senden erforderlicher und optionaler Daten an Microsoft gesteuert.

Wenn Sie diese Richtlinie nicht konfigurieren oder deaktivieren, verwendet Microsoft Edge standardmäßig die Benutzereinstellungen.

Zuordnung der Richtlinienoptionen:

* Off (0) = Aus (nicht empfohlen)

* RequiredData (1) = Erforderliche Daten

* OptionalData (2) = Optionale Daten

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DiagnosticData
  - Gruppenrichtlinienname: Erforderliche und optionale Diagnosedaten über die Browsernutzung senden
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DiagnosticData
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000002
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DiagnosticData
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DirectInvokeEnabled
  #### Benutzern das Öffnen von Dateien unter Verwendung des DirectInvoke-Protokolls ermöglichen
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 78 oder höher

  #### Beschreibung
  Ermöglicht Benutzern das Öffnen von Dateien unter Verwendung des DirectInvoke-Protokolls. Mit dem DirectInvoke-Protokoll können Websites anfordern, dass der Browser Dateien von einer bestimmten URL öffnet und dabei einen spezifischen Dateihandler auf dem Computer oder Gerät des Benutzers verwendet.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer Dateien unter Verwendung des DirectInvoke-Protokolls öffnen.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer keine Dateien unter Verwendung des DirectInvoke-Protokolls öffnen. Die Datei wird stattdessen im Dateisystem gespeichert.

Hinweis: Wenn Sie DirectInvoke deaktivieren, funktionieren bestimmte Microsoft Office SharePoint Online-Features möglicherweise nicht wie erwartet.

Weitere Informationen zu DirectInvoke finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) und [https://go.microsoft.com/fwlink/?linkid=2099871](https://go.microsoft.com/fwlink/?linkid=2099871).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DirectInvokeEnabled
  - Gruppenrichtlinienname: Benutzern das Öffnen von Dateien unter Verwendung des DirectInvoke-Protokolls ermöglichen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DirectInvokeEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### Disable3DAPIs
  #### Unterstützung für 3D-Grafik-APIs deaktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Verhindern Sie, dass Webseiten auf die Grafikprozessoreinheit (GPU) zugreifen. Insbesondere können Webseiten nicht auf die WebGL-API zugreifen und Plug-Ins nicht auf die Pepper 3D-API.

Wenn Sie diese Richtlinie nicht konfigurieren oder deaktivieren, können Webseiten möglicherweise die WebGL-API und Plug-Ins die Pepper 3D-API verwenden. Microsoft Edge könnte standardmäßig weiterhin die Übergabe von Befehlszeilenargumenten erfordern, um diese APIs zu verwenden.

Wenn die Richtlinie [HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled) auf false festgelegt ist, wird die Einstellung für die Richtlinie 'Disable3DAPIs' ignoriert. Dies entspricht der Festlegung der Richtlinie 'Disable3DAPIs' auf true.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: Disable3DAPIs
  - Gruppenrichtlinienname: Unterstützung für 3D-Grafik-APIs deaktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: Disable3DAPIs
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: Disable3DAPIs
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DisableScreenshots
  #### Aufnahme von Screenshots deaktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Steuert, ob Benutzer Screenshots der Browserseite aufnehmen können.

Wenn diese Option aktiviert ist, können Benutzer keine Screenshots mithilfe von Tastenkombinationen oder Erweiterungs-APIs aufnehmen.

Wenn diese Richtlinie deaktiviert oder nicht konfiguriert wird, können Benutzer Screenshots aufnehmen.

Hinweis: Diese Richtlinie steuert Screenshots, die innerhalb des Browsers selbst erstellt wurden. Auch wenn Sie diese Richtlinie aktivieren, können Benutzer möglicherweise weiterhin Screenshots mit einer Methode außerhalb des Browsers (z. B. mit einem Betriebssystemfeature oder einer anderen Anwendung) aufnehmen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DisableScreenshots
  - Gruppenrichtlinienname: Aufnahme von Screenshots deaktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DisableScreenshots
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DisableScreenshots
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DiskCacheDir
  #### Verzeichnis für Datenträgercache festlegen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Konfiguriert das Verzeichnis, das zum Speichern von zwischengespeicherten Dateien verwendet werden soll.

Wenn Sie diese Richtlinie aktivieren, verwendet Microsoft Edge das angegebene Verzeichnis, unabhängig davon, ob der Benutzer das Kennzeichen "--disk-cache-dir" angegeben hat. Um Datenverlust oder andere unerwartete Fehler zu vermeiden, konfigurieren Sie diese Richtlinie nicht auf das Stammverzeichnis eines Volumes oder auf ein Verzeichnis, das für andere Zwecke verwendet wird, da Microsoft Edge dessen Inhalt verwaltet.

Eine Liste der Variablen, die Sie beim Angeben von Verzeichnissen und Pfaden verwenden können, finden Sie unter "[https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041)".

Wenn Sie diese Richtlinie nicht konfigurieren, wird das standardmäßige Cache-Verzeichnis verwendet, und Benutzer können diesen Standard mit dem Befehlszeilen-Kennzeichen "--disk-cache-dir" überschreiben.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DiskCacheDir
  - Gruppenrichtlinienname: Verzeichnis für Datenträgercache festlegen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DiskCacheDir
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"${user_home}/Edge_cache"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DiskCacheDir
  - Beispielwert:
``` xml
<string>${user_home}/Edge_cache</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DiskCacheSize
  #### Größe des Datenträgercaches festlegen (in Bytes)
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Konfiguriert die Cachegröße (in Bytes), die zum Speichern von Dateien auf dem Datenträger verwendet wird.

Wenn sie diese Richtlinie aktivieren, verwendet Microsoft Edge die bereitgestellte Cachegröße, unabhängig davon, ob der Benutzer das Kennzeichen "--disk-cache-size" angegeben hat. Der in dieser Richtlinie angegebene Wert ist keine harte Grenze, sondern eher ein Vorschlag für das Cachingsystem. Jeder beliebige Wert unter einigen Megabytes ist zu klein und wird auf ein angemessenes Minimum aufgerundet.

Wenn Sie den Wert dieser Richtlinie auf "0" festlegen, wird die Standardcachegröße verwendet, und die Benutzer können sie nicht ändern.

Wenn Sie diese Richtlinie nicht konfigurieren, wird die Standardgröße verwendet, aber die Benutzer können sie mit dem Kennzeichen "--cache-cache-size" außer Kraft setzen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DiskCacheSize
  - Gruppenrichtlinienname: Größe des Datenträgercaches festlegen (in Bytes)
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DiskCacheSize
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x06400000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DiskCacheSize
  - Beispielwert:
``` xml
<integer>104857600</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DnsOverHttpsMode
  #### Den Modus von DNS-over-HTTPS steuern
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 83 oder höher

  #### Beschreibung
  Steuerung des Modus des DNS-over-HTTPS-Resolvers. Beachten Sie, dass diese Richtlinie nur den Standardmodus für jede Abfrage festlegt. Der Modus kann für spezielle Abfragetypen außer Kraft gesetzt werden, wie beispielsweise Anforderungen, DNS-over-HTTPS-Server-Hostnamen aufzulösen.

Der "off"-Modus deaktiviert DNS-over-HTTPS.

Der "automatic"-Modus sendet erst DNS-over-HTTPS-Abfragen, falls ein DNS-over-HTTPS-Server verfügbar ist, und kann bei Fehlern auf den Versand ungesicherter Abfragen zurückfallen.

Der "secure"-Modus sendet ausschließlich DNS-over-HTTPS-Abfragen und bei Fehlern schlägt die Auflösung fehl.

Falls Sie diese Richtlinie nicht konfigurieren, sendet der Browser möglicherweise DNS-over-HTTPS-Abfragen an einen Resolver, der mit dem vom Benutzer konfigurierten Systemresolver verbunden ist.

Zuordnung der Richtlinienoptionen:

* off (off) = DNS-over-HTTPS abschalten

* automatic (automatic) = Aktivieren von DNS-over-HTTPS mit unsicherem Fallback

* secure (secure) = Aktivieren von DNS–over-HTTPS ohne unsicheres Fallback

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DnsOverHttpsMode
  - Gruppenrichtlinienname: Den Modus von DNS-over-HTTPS steuern
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DnsOverHttpsMode
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"off"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DnsOverHttpsMode
  - Beispielwert:
``` xml
<string>off</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DnsOverHttpsTemplates
  #### URI-Vorlage der gewünschten DNS-über-HTTPS-Auflösung angeben
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 83 oder höher

  #### Beschreibung
  Die URI-Vorlage des gewünschten DNS-over-HTTPS-Resolvers. Um mehrere DNS-over-HTTPS-Resolver anzugeben, trennen Sie die entsprechenden URI-Vorlagen durch Leerzeichen.

Wenn Sie den [DnsOverHttpsMode](#dnsoverhttpsmode) auf "secure" festlegen, muss diese Richtlinie festgelegt und darf nicht leer sein.

Wenn Sie den [DnsOverHttpsMode](#dnsoverhttpsmode) auf "automatic" festlegen, und diese Richtlinie festgelegt wird, werden die angegebenen URI-Vorlagen verwendet. Wenn Sie diese Richtlinie nicht festlegen, werden hartcodierte Zuordnungen verwendet, um ein Upgrade des aktuellen DNS-Resolvers des Benutzers auf einen DoH-Resolver zu versuchen, der vom selben Anbieter betrieben wird.

Wenn die URI-Vorlage eine dns-Variable enthält, verwenden Anforderungen an den Resolver GET, andernfalls verwenden Anforderungen POST.

Fehlerhaft formatierte Vorlagen werden ignoriert.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DnsOverHttpsTemplates
  - Gruppenrichtlinienname: URI-Vorlage der gewünschten DNS-über-HTTPS-Auflösung angeben
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: DnsOverHttpsTemplates
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"https://dns.example.net/dns-query{?dns}"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DnsOverHttpsTemplates
  - Beispielwert:
``` xml
<string>https://dns.example.net/dns-query{?dns}</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DownloadDirectory
  #### Downloadverzeichnis festlegen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Konfiguriert das Verzeichnis, das beim Herunterladen von Dateien verwendet werden soll.

Wenn Sie diese Richtlinie aktivieren, verwendet Microsoft Edge das angegebene Verzeichnis – unabhängig davon, ob der Benutzer ein Verzeichnis angegeben oder ausgewählt hat, dass er jedes Mal zur Angabe eines Downloadverzeichnisses aufgefordert werden möchte. Unter „[https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041)“ finden Sie eine Liste mit verwendbaren Variablen.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird das Standardverzeichnis für Downloads verwendet, und der Benutzer kann das Verzeichnis ändern.

Ist der festgelegte Pfad ungültig, verwendet Microsoft Edge das standardmäßige Downloadverzeichnis des Benutzers.

Ist der durch den Pfad angegebene Ordner nicht vorhanden, wird der Benutzer zur Angabe eines Speicherorts für den Download aufgefordert.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DownloadDirectory
  - Gruppenrichtlinienname: Downloadverzeichnis festlegen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: DownloadDirectory
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"\n      Linux-based OSes (including Mac): /home/${user_name}/Downloads\n      Windows: C:\\Users\\${user_name}\\Downloads"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DownloadDirectory
  - Beispielwert:
``` xml
<string>
      Linux-based OSes (including Mac): /home/${user_name}/Downloads
      Windows: C:\Users\${user_name}\Downloads</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### DownloadRestrictions
  #### Download-Einschränkungen zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Mit dieser Richtlinie konfigurieren Sie die Art der Downloads, die Microsoft Edge vollständig blockiert, ohne dass Benutzer die Sicherheitsentscheidung außer Kraft setzen können.

Legen Sie “BlockDangerousDownloads“ fest, um alle Downloads außer denjenigen zuzulassen, die Microsoft Defender SmartScreen-Warnungen aufweisen.

Legen Sie “BlockDangerousDownloads“ fest, um alle Downloads außer denjenigen zuzulassen, die Microsoft Defender SmartScreen-Warnungen vor potenziell gefährlichen Downloads aufweisen.

Legen Sie “BlockAllDownloads” fest, um alle Downloads zu blockieren.

Wenn Sie diese Richtlinie nicht konfigurieren oder die Option “DefaultDownloadSecurity” wählen, durchlaufen die Downloads die üblichen Sicherheitseinschränkungen basierend auf den Microsoft Defender SmartScreen-Analyseergebnissen.

Beachten Sie, dass diese Einschränkungen für Downloads von Webseiteninhalten sowie für die Kontextmenüoption “Link herunterladen …“ gelten. Diese Einschränkungen gelten weder für das Speichern oder Herunterladen der aktuell angezeigten Seite noch für die Option “Als PDF speichern“ in den Druckoptionen.

Weitere Informationen zu Microsoft Defender SmartScreen finden Sie unter “[https://go.microsoft.com/fwlink/?linkid=2094934](https://go.microsoft.com/fwlink/?linkid=2094934)“.

Zuordnung der Richtlinienoptionen:

* DefaultDownloadSecurity (0) = Keine besonderen Einschränkungen

* BlockDangerousDownloads (1) = Gefährliche Downloads blockieren

* BlockPotentiallyDangerousDownloads (2) = Blockieren potenziell gefährlicher oder unerwünschter Downloads

* BlockAllDownloads (3) = Alle Downloads blockieren

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: DownloadRestrictions
  - Gruppenrichtlinienname: Download-Einschränkungen zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: DownloadRestrictions
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000002
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: DownloadRestrictions
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### EdgeCollectionsEnabled
  #### Aktivieren der Sammlungsfunktion
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 78 oder höher

  #### Beschreibung
  Ermöglicht Benutzern den Zugriff auf die Sammlungsfunktion, mit der Inhalte effizienter und mit Office-Integration gesammelt, organisiert, freigegeben und exportiert werden können.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer auf die Sammlungsfunktion in Microsoft Edge zugreifen und diese verwenden.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer nicht auf die Sammlungsfunktion Microsoft Edge zugreifen und diese nicht verwenden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: EdgeCollectionsEnabled
  - Gruppenrichtlinienname: Aktivieren der Sammlungsfunktion
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: EdgeCollectionsEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: EdgeCollectionsEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### EditFavoritesEnabled
  #### Ermöglicht Benutzern das Bearbeiten von Favoriten.
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Aktivieren Sie diese Richtlinie, um Benutzern das Hinzufügen, Entfernen und Ändern von Favoriten zu ermöglichen. Dies ist das Standardverhalten, wenn Sie die Richtlinie nicht konfigurieren.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer keine Favoriten mehr hinzufügen, entfernen oder ändern. Bereits vorhandene Favoriten können weiterhin verwendet werden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: EditFavoritesEnabled
  - Gruppenrichtlinienname: Ermöglicht Benutzern das Bearbeiten von Favoriten.
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: EditFavoritesEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: EditFavoritesEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### EnableDeprecatedWebPlatformFeatures
  #### Veraltete Webplattformfeatures vorübergehend wieder aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Geben Sie eine Liste der veralteten Webplattformfeatures an, um sie vorübergehend wieder zu aktivieren.

Mit dieser Richtlinie können Sie veraltete Webplattformfeatures für einen begrenzten Zeitraum wieder aktivieren. Die Features werden anhand eines Zeichenfolgen-Tags gekennzeichnet.

Falls Sie diese Richtlinie nicht konfigurieren, wenn die Liste leer ist, oder falls ein Feature keinem der unterstützten Zeichenfolgen-Tags entspricht, bleiben alle veralteten Webplattformfeatures deaktiviert.

Auch wenn die Richtlinie selbst auf den obigen Plattformen unterstützt wird, ist das Feature, das sie aktiviert, möglicherweise nicht auf all diesen Plattformen verfügbar. Nicht alle veralteten Webplattformfeatures können erneut aktiviert werden. Nur die unten explizit aufgelisteten können erneut und nur für einen begrenzten Zeitraum aktiviert werden. Dies variiert je nach Feature. Sie können sich die Absicht hinter den Änderungen des Webplattformfeatures unter https://bit.ly/blinkintents ansehen.

Das allgemeine Format des Zeichenfolgen-Tags lautet [DeprecatedFeatureName]_EffectiveUntil[yyyymmdd].

Zuordnung der Richtlinienoptionen:

* ExampleDeprecatedFeature (ExampleDeprecatedFeature_EffectiveUntil20080902) = ExampleDeprecatedFeature-API bis einschließlich 02.09.2008 aktivieren

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: EnableDeprecatedWebPlatformFeatures
  - Gruppenrichtlinienname: Veraltete Webplattformfeatures vorübergehend wieder aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures\1 = "ExampleDeprecatedFeature_EffectiveUntil20080902"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: EnableDeprecatedWebPlatformFeatures
  - Beispielwert:
``` xml
<array>
  <string>ExampleDeprecatedFeature_EffectiveUntil20080902</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### EnableDomainActionsDownload
  #### Herunterladen von Domänenaktionen von Microsoft aktivieren (veraltet)
  
  >VERALTET: Diese Richtlinie ist veraltet und funktioniert nach Microsoft Edge Version 84 nicht mehr.
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77, bis 84

  #### Beschreibung
  Diese Richtlinie funktioniert nicht, weil in Konflikt stehende Zustände vermieden werden sollten. Diese Richtlinie verwendet wurde verwendet, um das Herunterladen der Liste der Domänenaktionen zu aktivieren/deaktivieren, erreichte aber nicht immer den gewünschten Zustand. Der Experimentier- und Konfigurationsdienst, der den Download durchführt, hat seine eigene Richtlinie, in der konfiguriert wird, was vom Dienst heruntergeladen wird. Verwenden Sie stattdessen die Richtlinie “[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)”.

In Microsoft Edge stellen Domänenaktionen eine Reihe von Kompatibilitätsfeatures dar, die dazu beitragen, dass der Browser im Web ordnungsgemäß funktioniert.

Microsoft verfügt über eine Liste mit Aktionen, die aus Kompatibilitätsgründen für bestimmte Domänen ausgeführt werden. So kann der Browser beispielsweise die Zeichenfolge des Benutzer-Agents auf einer Website ändern, wenn bei dieser Website aufgrund der neuen Zeichenfolge des Benutzer-Agents in Microsoft Edge Probleme auftreten. Jede dieser Aktionen ist als Übergangslösung gedacht, während Microsoft versucht, das Problem in Zusammenarbeit mit dem Websitebesitzer zu beheben.

Beim Start des Browsers (und danach in regelmäßigen Abständen) wird der Experimentier- und Konfigurationsdienst kontaktiert, auf dem sich die neueste Liste mit auszuführenden Kompatibilitätsaktionen befindet. Diese Liste wird nach dem erstmaligen Abruf lokal gespeichert und bei nachfolgenden Anforderungen nur noch aktualisiert, falls sich die Kopie auf dem Server geändert hat.

Wenn Sie diese Richtlinie aktivieren, wird die Liste mit Domänenaktionen weiterhin vom Experimentier- und Konfigurationsdienst heruntergeladen.

Wenn Sie diese Richtlinie deaktivieren, wird die Liste mit Domänenaktionen nicht mehr vom Experimentier- und Konfigurationsdienst heruntergeladen.

Wenn Sie diese Richtlinie nicht konfigurieren, wird die Liste mit Domänenaktionen weiterhin vom Experimentier- und Konfigurationsdienst heruntergeladen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: EnableDomainActionsDownload
  - Gruppenrichtlinienname: Herunterladen von Domänenaktionen von Microsoft aktivieren (veraltet)
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: EnableDomainActionsDownload
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: EnableDomainActionsDownload
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### EnableOnlineRevocationChecks
  #### Onlineprüfungen für OCSP/Sperrlisten aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Onlinesperrprüfungen bieten keinen wesentlichen Sicherheitsvorteil und sind standardmäßig deaktiviert.

Wenn Sie diese Richtlinie aktivieren, führt Microsoft Edge Onlineprüfungen für OCSP/Sperrlisten auf leichte Fehler durch. „Leichter Fehler“ bedeutet, dass das Zertifikat als gültig gilt, wenn der Sperrserver nicht erreicht werden kann.

Wenn Sie die Richtlinie deaktivieren oder nicht konfigurieren, führt Microsoft Edge keine Onlinesperrprüfungen durch.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: EnableOnlineRevocationChecks
  - Gruppenrichtlinienname: Onlineprüfungen für OCSP/Sperrlisten aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: EnableOnlineRevocationChecks
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: EnableOnlineRevocationChecks
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### EnableSha1ForLocalAnchors
  #### Mit SHA-1 signierte Zertifikate zulassen, wenn sie von lokalen Vertrauensanker ausgestellt worden sind. (veraltet)
  >VERALTET: Diese Richtlinie ist veraltet. Sie wird gegenwärtig noch unterstützt, aber in einem zukünftigen Release ausgemustert.
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 85 oder höher

  #### Beschreibung
  Wenn diese Einstellung aktiviert ist, lässt Microsoft Edge Verbindungen zu, die durch signierte SHA-1-Zertifikate gesichert sind, solange das Zertifikat mit einem lokal installierten Stammzertifikat verkettet und andernfalls gültig ist.

Beachten Sie, dass diese Richtlinie vom Zertifikatüberprüfungsstapel des Betriebssystems (BS) abhängt, der SHA-1-Signaturen zulässt. Wenn ein Betriebssystemupdate den Umgang des BS mit SHA-1-Zertifikaten ändert, hat diese Richtlinie möglicherweise keinen Effekt mehr.  Außerdem ist diese Richtlinie als vorübergehende Problemumgehung vorgesehen, um Unternehmen mehr Zeit für die Umstellung weg von SHA-1 zu bieten. Diese Richtlinie wird in Microsoft Edge 92 (Release Mitte 2021) entfernt.

Wenn Sie diese Richtlinie nicht oder auf "falsch" festlegen oder das SHA-1-Zertifikat mit einem öffentlich vertrauenswürdigen Stammzertifikat verkettet ist, lässt Microsoft Edge keine von SHA-1 signierte Zertifikate zu.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: EnableSha1ForLocalAnchors
  - Gruppenrichtlinienname: Mit SHA-1 signierte Zertifikate zulassen, wenn sie von lokalen Vertrauensanker ausgestellt worden sind. (veraltet)
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: EnableSha1ForLocalAnchors
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: EnableSha1ForLocalAnchors
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### EnterpriseHardwarePlatformAPIEnabled
  #### Ermöglichen der Verwendung der Enterprise Hardware Platform-API durch verwaltete Erweiterungen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 78 oder höher

  #### Beschreibung
  Wenn diese Richtlinie aktiviert ist, dürfen anhand der Unternehmensrichtlinie installierte Erweiterungen die Enterprise Hardware Platform-API verwenden.
Wenn diese Richtlinie deaktiviert oder nicht festgelegt ist, dürfen keine Erweiterungen die Enterprise Hardware Platform-API verwenden.
Diese Richtlinie gilt auch für Komponentenerweiterungen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: EnterpriseHardwarePlatformAPIEnabled
  - Gruppenrichtlinienname: Ermöglichen der Verwendung der Enterprise Hardware Platform-API durch verwaltete Erweiterungen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: EnterpriseHardwarePlatformAPIEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: EnterpriseHardwarePlatformAPIEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### EnterpriseModeSiteListManagerAllowed
  #### Zugriff auf das Tool “Enterprise Mode Site List Manager” zulassen
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 86 oder höher

  #### Beschreibung
  Hiermit können Sie festlegen, ob der Enterprise Mode Site List Manager für Benutzer verfügbar ist.

 Wenn Sie diese Richtlinie aktivieren, können Benutzer die Navigationsschaltfläche des Enterprise Mode Site List Manager-Tools auf der Seite "edge://compat page" sehen, das Tool aufrufen und es verwenden.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, können die Benutzer die Navigationsschaltfläche des Enterprise Mode Site List Manager-Tools nicht sehen und es auch nicht verwenden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: EnterpriseModeSiteListManagerAllowed
  - Gruppenrichtlinienname: Zugriff auf das Tool “Enterprise Mode Site List Manager” zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: EnterpriseModeSiteListManagerAllowed
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  #### Download der auf Dateityperweiterungen basierenden Warnungen für angegebene Dateitypen in Domänen deaktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 85 oder höher

  #### Beschreibung
  Sie können diese Richtlinie aktivieren, um ein Wörterbuch der Dateityperweiterungen mit einer entsprechenden Liste von Domänen zu erstellen, die von auf Dateityperweiterungen basierenden Downloadwarnungen ausgenommen werden. Dies gestattet Unternehmensadministratoren, Downloadwarnungen, die auf Dateierweiterungen für Dateien basieren, für Dateien zu blockieren, die einer aufgeführten Domäne zugeordnet sind. Wenn beispielsweise die Erweiterung "jnlp" mit "website1.com" verknüpft ist, wird Benutzern beim Herunterladen von "jnlp"-Dateien von "website1.com" keine Warnung angezeigt, beim Herunterladen von "website2.com" jedoch schon.

Dateien mit Dateityperweiterungen, die für Domänen angegeben sind, die von dieser Richtlinie identifiziert werden, unterliegen weiterhin Sicherheitswarnungen, die nicht auf Dateierweiterungen basieren, z. B Downloadwarnungen für gemischte Inhalte und Microsoft Defender SmartScreen-Warnungen.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden dem Benutzer für Dateitypen, die Downloadwarnungen basierend auf Dateierweiterungen auslösen, solche Warnungen angezeigt.

Wenn Sie diese Richtlinie aktivieren:

* Das URL-Muster sollte entsprechend den Hinweisen unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). formatiert sein.
* Die Dateityperweiterung muss als kleingeschriebener ASCII-Wert eingegeben werden. Das vorangestellte Trennzeichen muss beim Auflisten der Dateityperweiterung weggelassen werden, also sollte beispielsweise "jnlp" statt ". jnlp" in die Liste eingegeben werden.

Beispiel

Mit dem folgenden Beispielwert werden die auf dem Dateityp basierenden Downloadwarnungen für SWF-, EXE- und JNLP-Erweiterungen für *.contoso.com”-Domänen verhindert. Der Benutzer erhält bei jeder anderen Domäne eine auf Dateierweiterungen basierende Downloadwarnung für EXE- und JNLP-Dateien, nicht aber für SWF-Dateien.

[
  { "file_extension": "jnlp", "domains": ["contoso.com"] },
  { "file_extension": "exe", "domains": ["contoso.com"] },
  { "file_extension": "swf", "domains": ["*"] }
]

Beachten Sie, dass das vorherige Beispiel zeigt, wie auf Dateityperweiterungen basierende Downloadwarnungen für SWF-Dateien für alle Domänen unterdrückt werden können. Es ist aber aus Sicherheitsgründen nicht empfehlenswert, solche Warnungen für jede Art von gefährlichen Dateityperweiterungen für alle Domänen zu unterdrücken. Diese Möglichkeit wird im Beispiel lediglich zu Veranschaulichungszwecken gezeigt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Gruppenrichtlinienname: Download der auf Dateityperweiterungen basierenden Warnungen für angegebene Dateitypen in Domänen deaktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\1 = {"domains": ["https://contoso.com", "contoso2.com"], "file_extension": "jnlp"}
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\2 = {"domains": ["*"], "file_extension": "swf"}

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Beispielwert:
``` xml
<array>
  <string>{'domains': ['https://contoso.com', 'contoso2.com'], 'file_extension': 'jnlp'}</string>
  <string>{'domains': ['*'], 'file_extension': 'swf'}</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ExperimentationAndConfigurationServiceControl
  #### Steuern der Kommunikation mit dem Experimentier- und Konfigurationsdienst
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  In Microsoft Edge wird der Experimentier- und Konfigurationsdienst zum Bereitstellen der Experimentier- und Konfigurationsnutzlast verwendet.

Die Nutzlast für Experimente besteht aus einer Liste von frühzeitigen Entwicklungsfeatures, die Microsoft für Tests und Feedback aktiviert.

Die Konfigurationsnutzlast besteht aus einer Liste von Einstellungen, die Microsoft für Microsoft Edge bereitstellen möchte, um die Benutzerfreundlichkeit zu optimieren. Die Konfigurationsnutzlast kann z. B. angeben, wie oft Microsoft Edge Anforderungen an den Experimentier- und Konfigurationsdienst sendet, um die neueste Nutzlast abzurufen.

Zudem enthält die Konfigurationsnutzlast möglicherweise eine Liste von Aktionen, die aus Kompatibilitätsgründen an bestimmten Domänen ausgeführt werden müssen. So kann der Browser beispielsweise die Zeichenfolge des Benutzer-Agents auf einer Website ändern, wenn bei dieser Website aufgrund der neuen Zeichenfolge des Benutzer-Agents in Microsoft Edge Probleme auftreten. Jede dieser Aktionen ist als Übergangslösung gedacht, während Microsoft versucht, das Problem in Zusammenarbeit mit dem Websitebesitzer zu beheben.

Wenn Sie diese Richtlinie auf den Modus “FullMode” festlegen, wird die vollständige Nutzlast vom Experimentier- und Konfigurationsdienst heruntergeladen. Dazu gehört sowohl die Experimentier- als auch die Konfigurationsnutzlast.

Wenn Sie diese Richtlinie auf den Modus “ConfigurationsOnlyMode” festlegen, wird nur die Konfigurationsnutzlast übermittelt.

Wenn Sie diese Richtlinie auf “RestrictedMode” festlegen, wird die Kommunikation mit dem Experimentier- und Konfigurationsdienst vollständig beendet.

Wenn Sie diese Richtlinie nicht konfigurieren, ist das Verhalten auf einem verwalteten Gerät bei Beta- und Stable-Kanälen dasselbe wie im Modus “ConfigurationsOnlyMode”.

Wenn Sie diese Richtlinie nicht konfigurieren ist das Verhalten auf einem nicht verwalteten Gerät dasselbe wie im Modus “FullMode”.

Zuordnung der Richtlinienoptionen:

* FullMode (2) = Konfigurationen und Experimente abrufen

* ConfigurationsOnlyMode (1) = Nur Konfigurationen abrufen

* RestrictedMode (0) = Deaktivieren der Kommunikation mit dem Experimentier- und Konfigurationsdienst

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ExperimentationAndConfigurationServiceControl
  - Gruppenrichtlinienname: Steuern der Kommunikation mit dem Experimentier- und Konfigurationsdienst
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ExperimentationAndConfigurationServiceControl
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000002
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ExperimentationAndConfigurationServiceControl
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ExternalProtocolDialogShowAlwaysOpenCheckbox
  #### Kontrollkästchen „Immer geöffnet“ im Dialogfeld für externe Protokolle anzeigen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 79 oder höher

  #### Beschreibung
  Diese Richtlinie steuert, ob in Startbestätigungsaufforderungen externer Protokolle das Kontrollkästchen "Für diese Website das Öffnen solcher Links zulassen" angezeigt wird. Diese Richtlinie wirkt sich nur auf https://-Links aus.

 Wenn Sie diese Richtlinie aktivieren und eine Bestätigungsaufforderung für ein externes Protokoll angezeigt wird, kann der Benutzer "Immer zulassen" auswählen, um alle zukünftigen Bestätigungsaufforderungen für das Protokoll auf dieser Website zu überspringen.

 Wenn Sie diese Richtlinie deaktivieren, wird das Kontrollkästchen "Immer zulassen" nicht angezeigt. Der Benutzer wird jedes Mal zur Bestätigung aufgefordert, wenn ein externes Protokoll aufgerufen wird.

Vor Microsoft Edge 83, wenn Sie diese Richtlinie nicht konfigurieren, wird das Kontrollkästchen "immer zulassen" nicht angezeigt. Der Benutzer wird jedes Mal zur Bestätigung aufgefordert, wenn ein externes Protokoll aufgerufen wird.

In Microsoft Edge 83, wenn Sie diese Richtlinie nicht konfigurieren, wird die Sichtbarkeit des Kontrollkästchens durch die Kennzeichnung "Aktivieren des Speicherns von Präferenzen für die Protokollstartabfrage" in edge://flags gesteuert

Ab Microsoft Edge 84, wenn Sie diese Richtlinie nicht konfigurieren, kann der Benutzer beim Anzeigen einer Bestätigungsaufforderung für externes Protokoll "immer zulassen" auswählen, um alle zukünftigen Bestätigungsaufforderungen für das Protokoll auf dieser Website zu überspringen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Gruppenrichtlinienname: Kontrollkästchen „Immer geöffnet“ im Dialogfeld für externe Protokolle anzeigen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### FamilySafetySettingsEnabled
  #### Zulassen, dass Benutzer Family Safety konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 83 oder höher

  #### Beschreibung
  Durch diese Richt Linie wird die Seite "Family Safety" in den Einstellungen deaktiviert und voll ständig ausgeblendet. Die Navigation zu edge://settings/familysafety wird ebenfalls blockiert. Die Family Safety-Seite beschreibt, welche Funktionen für Familien Gruppen und für die Teilnahme an einer Familien Gruppe verfügbar sind. Weitere Informationen zur Family Safety hier: ([https://go.microsoft.com/fwlink/?linkid=2098432](https://go.microsoft.com/fwlink/?linkid=2098432)).

Wenn Sie diese Richt Linie aktivieren oder nicht konfigurieren, wird die Seite "Familien Sicherheit" angezeigt.

Wenn Sie diese Richt Linie deaktivieren, wird die Seite "Familien Sicherheit" nicht angezeigt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: FamilySafetySettingsEnabled
  - Gruppenrichtlinienname: Zulassen, dass Benutzer Family Safety konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: FamilySafetySettingsEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: FamilySafetySettingsEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### FavoritesBarEnabled
  #### Favoritenleiste aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Aktiviert oder deaktiviert die Favoritenleiste.

Wenn Sie diese Richtlinie aktivieren, wird den Benutzern die Favoritenleiste angezeigt.

Wenn Sie diese Richtlinie deaktivieren, wird den Benutzern die Favoritenleiste nicht angezeigt.

Wenn diese Richtlinie nicht konfiguriert ist, kann der Benutzer entscheiden, ob er die Favoritenleiste verwenden möchte.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: FavoritesBarEnabled
  - Gruppenrichtlinienname: Favoritenleiste aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: FavoritesBarEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: FavoritesBarEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ForceBingSafeSearch
  #### Bing SafeSearch erzwingen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Mit dieser Richtlinie sorgen Sie dafür, dass bei Abfragen in der Bing-Websuche der angegebene SafeSearch-Wert verwendet wird. Diese Einstellung kann von Benutzern nicht geändert werden.

Wenn Sie diese Richtlinie auf “BingSafeSearchNoRestrictionsMode” festlegen, wird für SafeSearch in der Bing-Suche der Wert von “bing.com“ verwendet.

Wenn Sie diese Richtlinie auf “BingSafeSearchModerateMode“ festlegen, wird in SafeSearch die moderate Einstellung verwendet. Bei dieser Einstellung werden nicht jugendfreie Videos und Bilder, aber keine Texte aus den Suchergebnissen herausgefiltert.

Wenn Sie diese Richtlinie auf “BingSafeSearchStrictMode” festlegen, wird in SafeSearch die strenge Einstellung verwendet. Bei dieser Einstellung werden nicht jugendfreie Texte, Bilder und Videos herausgefiltert.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird SafeSearch in der Bing-Suche nicht erzwungen, und Benutzer können den gewünschten Wert auf “bing.com“ selbst festlegen.

Zuordnung der Richtlinienoptionen:

* BingSafeSearchNoRestrictionsMode (0) = Keine Sucheinschränkungen in Bing konfigurieren

* BingSafeSearchModerateMode (1) = Moderate Sucheinschränkungen in Bing konfigurieren

* BingSafeSearchStrictMode (2) = Strenge Sucheinschränkungen in Bing konfigurieren

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ForceBingSafeSearch
  - Gruppenrichtlinienname: Bing SafeSearch erzwingen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ForceBingSafeSearch
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ForceBingSafeSearch
  - Beispielwert:
``` xml
<integer>0</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ForceCertificatePromptsOnMultipleMatches
  #### Konfigurieren Sie, ob Microsoft Edge automatisch ein Zertifikat auswählen sollte, wenn mehrere Zertifikat Übereinstimmungen für eine Website vorhanden sind, die mit "AutoSelectCertificateForUrls" konfiguriert ist.
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 81 oder höher

  #### Beschreibung
  Schaltet an, ob Benutzer zur Auswahl eines Zertifikats aufgefordert werden, wenn mehrere Zertifikate verfügbar sind und eine Website mit der [AutoSelectCertificateForUrls](#autoselectcertificateforurls). Wenn Sie [AutoSelectCertificateForUrls](#autoselectcertificateforurls) nicht für eine Website konfigurieren, wird der Benutzer immer aufgefordert, ein Zertifikat auszuwählen.

Wenn Sie diese Richt Linie auf "true" festlegen, fordert Microsoft Edge einen Benutzer auf, ein Zertifikat für Websites in der Liste auszuwählen, die in [AutoSelectCertificateForUrls](#autoselectcertificateforurls) definiert ist, und nur dann, wenn mehrere Zertifikate vorhanden sind.

Wenn Sie diese Richt Linie auf "false" festlegen oder nicht konfigurieren, wählt Microsoft Edge automatisch ein Zertifikat aus, auch wenn für ein Zertifikat mehrere überein Stimmungen vorhanden sind. Der Benutzer wird nicht aufgefordert, ein Zertifikat für Websites in der Liste auszuwählen, die in [AutoSelectCertificateForUrls](#autoselectcertificateforurls) definiert ist.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ForceCertificatePromptsOnMultipleMatches
  - Gruppenrichtlinienname: Konfigurieren Sie, ob Microsoft Edge automatisch ein Zertifikat auswählen sollte, wenn mehrere Zertifikat Übereinstimmungen für eine Website vorhanden sind, die mit "AutoSelectCertificateForUrls" konfiguriert ist.
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ForceCertificatePromptsOnMultipleMatches
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ForceCertificatePromptsOnMultipleMatches
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ForceEphemeralProfiles
  #### Verwendung von kurzlebigen Profilen aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Steuert, ob Benutzerprofile auf den kurzlebigen Modus umgestellt werden. Ein kurzlebiges Profil wird zu Beginn einer Sitzung erstellt und am Ende der Sitzung gelöscht und ist dem ursprünglichen Profil des Benutzers zugeordnet

Wenn Sie diese Richtlinie aktivieren, werden Profile im kurzlebigen Modus ausgeführt. Dadurch können Benutzer auf ihren eigenen Geräten arbeiten, ohne die Browserdaten auf diesen Geräten zu speichern. Wenn Sie diese Richtlinie als Betriebssystemrichtlinie aktivieren (beispielsweise per Gruppenrichtlinienobjekt unter Windows), gilt sie für jedes Profil im System.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, stehen Benutzern ihre regulären Profile zur Verfügung, wenn Sie sich beim Browser anmelden.

Im kurzlebigen Modus werden Profildaten nur für die Dauer der Benutzersitzung auf dem Datenträger gespeichert. Features wie Browserverlauf, Erweiterungen und deren Daten, Webdaten wie Cookies und Webdatenbanken werden nach dem Schließen des Browsers nicht gespeichert. Ein Benutzer kann jedoch weiterhin beliebige Daten manuell auf den Datenträger herunterladen sowie Seiten speichern oder ausdrucken. Bei Benutzern mit aktivierter Synchronisierung werden alle Daten genau wie bei regulären Profilen in ihren Synchronisierungskonten gespeichert. Benutzer können außerdem den InPrivate-Modus im kurzlebigen Modus verwenden, sofern Sie dies nicht explizit deaktivieren.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ForceEphemeralProfiles
  - Gruppenrichtlinienname: Verwendung von kurzlebigen Profilen aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ForceEphemeralProfiles
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ForceEphemeralProfiles
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ForceGoogleSafeSearch
  #### Google SafeSearch erzwingen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Erzwingt bei Abfragen in der Google Websuche, dass SafeSearch aktiviert wird, und verhindert, dass Benutzer diese Einstellung ändern.

Wenn Sie diese Richtlinie aktivieren, ist SafeSearch in der Google-Suche immer aktiv.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird SafeSearch in der Google-Suche nicht erzwungen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ForceGoogleSafeSearch
  - Gruppenrichtlinienname: Google SafeSearch erzwingen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ForceGoogleSafeSearch
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ForceGoogleSafeSearch
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ForceLegacyDefaultReferrerPolicy
  #### Verwenden Sie eine Referrer-Standardrichtlinie vom Typ „no-referrer-when-downgrade“ (veraltet)
  >VERALTET: Diese Richtlinie ist veraltet. Sie wird gegenwärtig noch unterstützt, aber in einem zukünftigen Release ausgemustert.
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 81 oder höher

  #### Beschreibung
  Diese Richtlinie ist veraltet, weil sie nur als kurzfristiger Mechanismus gedacht ist, um Unternehmen mehr Zeit zu geben, ihre Webinhalte zu aktualisieren, wenn sich herausstellt, dass sie nicht mit der aktuellen Standardverweiserrichtlinie vereinbar sind. Sie wird in Microsoft Edge Version 86 nicht mehr funktionieren.

Die Standardverweiserrichtlinie von Microsoft Edge wird durch ein schrittweises Rollout von ihrem derzeitigen Wert "no-Referrer-when-downgrade" auf die sicherere Richtlinie "strict-origin-when-cross-origin" umgestellt.

Vor dem Rollout hat diese Unternehmensrichtlinie keine Auswirkungen. Wenn diese Unternehmensrichtlinie nach dem Rollout aktiviert ist, wird die Standardverweiserrichtlinie von Microsoft Edge auf den alten Wert "no-referrer-when-downgrade" festgelegt.

Diese Unternehmensrichtlinie ist standardmäßig deaktiviert.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ForceLegacyDefaultReferrerPolicy
  - Gruppenrichtlinienname: Verwenden Sie eine Referrer-Standardrichtlinie vom Typ „no-referrer-when-downgrade“ (veraltet)
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ForceLegacyDefaultReferrerPolicy
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ForceLegacyDefaultReferrerPolicy
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ForceNetworkInProcess
  #### Ausführung von Netzwerkcode im Browserprozess erzwingen (veraltet)
  
  >VERALTET: Diese Richtlinie ist veraltet und funktioniert nach Microsoft Edge Version 83 nicht mehr.
  #### Unterstützte Versionen:
  - Unter Windows seit 78, bis 83

  #### Beschreibung
  Diese Richtlinie funktioniert nicht, da sie nur als kurzfristiger Mechanismus gedacht war, um Unternehmen mehr Zeit für die Migration zu Software von Drittanbietern zu geben, die nicht vom Hooking von Netzwerk-APIs abhängt. Proxyserver werden über LSPs und Win32-API-Patching empfohlen.

Diese Richtlinie erzwingt, dass Netzwerkcode im Browserprozess ausgeführt wird.

Diese Richtlinie ist standardmäßig deaktiviert. Wenn sie aktiviert ist, sind Benutzer anfällig für Sicherheitsprobleme, wenn der Netzwerkprozess in der Sandbox ausgeführt wird.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ForceNetworkInProcess
  - Gruppenrichtlinienname: Ausführung von Netzwerkcode im Browserprozess erzwingen (veraltet)
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ForceNetworkInProcess
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ForceSync
  #### Force synchronization of browser data and do not show the sync consent prompt
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 86 oder höher

  #### Beschreibung
  Forces data synchronization in Microsoft Edge. This policy also prevents the user from turning sync off.

If you don't configure this policy, users will be able to turn sync on or off. If you enable this policy, users will not be able to turn sync off.

For this policy to work as intended,
[BrowserSignin](#browsersignin) policy must not be configured, or must be set to enabled. If [ForceSync](#forcesync) is set to disabled, then [BrowserSignin](#browsersignin) will not take affect.

[SyncDisabled](#syncdisabled) must not be configured or must be set to False. If this is set to True, [ForceSync](#forcesync) will not take affect.

0 = Do not automatically start sync and show the sync consent (default)
1 = Force sync to be turned on for Azure AD/Azure AD-Degraded user profile and do not show the sync consent prompt

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ForceSync
  - Gruppenrichtlinienname: Force synchronization of browser data and do not show the sync consent prompt
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ForceSync
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ForceSync
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ForceYouTubeRestrict
  #### Minimalen eingeschränkten Modus für YouTube erzwingen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Mit dieser Richtlinie können Sie einen mindestens eingeschränkten Modus für YouTube erzwingen und verhindern, dass Benutzer einen weniger eingeschränkten auswählen.

Legen Sie diese Richtlinie auf StrictStreng“ fest, um den streng eingeschränkten Modus für YouTube zu erzwingen.

Legen Sie diese Richtlinie auf “Moderate” fest, um zu erzwingen, dass Benutzer nur den moderat eingeschränkten und den streng eingeschränkten Modus für YouTube verwenden können. Sie können den eingeschränkten Modus nicht deaktivieren.

Wenn Sie diese Richtlinie auf “Off” festlegen oder nicht konfigurieren, wird der eingeschränkte Modus für YouTube nicht erzwungen. Externe Richtlinien, wie zum Beispiel YouTube-Richtlinien, können den eingeschränkten Modus aber möglicherweise weiterhin erzwingen.

Zuordnung der Richtlinienoptionen:

* Off (0) = Eingeschränkten Modus für YouTube nicht erzwingen

* Moderate (1) = Mindestens moderaten eingeschränkten Modus für YouTube erzwingen

* Strict (2) = Strengen eingeschränkten Modus für YouTube erzwingen

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ForceYouTubeRestrict
  - Gruppenrichtlinienname: Minimalen eingeschränkten Modus für YouTube erzwingen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ForceYouTubeRestrict
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ForceYouTubeRestrict
  - Beispielwert:
``` xml
<integer>0</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### FullscreenAllowed
  #### Vollbildmodus zulassen
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 77 oder höher

  #### Beschreibung
  Legen Sie die Verfügbarkeit des Vollbildmodus fest. Die gesamte Microsoft Edge-Benutzeroberfläche ist ausgeblendet und nur Webinhalte sind sichtbar.

Falls Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer, Apps und Erweiterungen mit entsprechenden Berechtigungen den Vollbildmodus öffnen.

Falls Sie diese Richtlinie deaktivieren, können Benutzer, Apps und Erweiterungen den Vollbildmodus nicht öffnen.

Das Öffnen von Microsoft Edge im Kioskmodus mithilfe der Befehlszeile ist nicht verfügbar, wenn der Vollbildmodus deaktiviert ist.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: FullscreenAllowed
  - Gruppenrichtlinienname: Vollbildmodus zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: FullscreenAllowed
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### GloballyScopeHTTPAuthCacheEnabled
  #### Globalen bereichsbezogenen HTTP-Authentifizierungscache aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 81 oder höher

  #### Beschreibung
  Mit dieser Richtlinie wird ein einzelner globaler profilbezogener Cache mit Anmeldeinformationen für die HTTP-Serverauthentifizierung konfiguriert.

Wenn Sie diese Richtlinie deaktivieren oder nicht festlegen, verwendet der Browser das Standardverhalten der standortübergreifenden Authentifizierung, das ab Version 80 zum Definieren der Anmeldeinformationen für die HTTP-Serverauthentifizierung nach Website auf oberster Ebene verwendet wird. Wenn also zwei Websites Ressourcen aus derselben Authentifizierungsdomäne verwenden, müssen die Anmeldeinformationen unabhängig voneinander im Kontext beider Websites bereitgestellt werden. Zwischengespeicherte Proxyanmeldeinformationen werden standortübergreifend wiederverwendet.

Wenn Sie diese Richtlinie aktivieren, werden HTTP-Authentifizierungsanmeldeinformationen, die im Kontext einer Website eingegeben werden, automatisch im Kontext einer anderen Website verwendet.

Wenn Sie diese Richtlinie aktivieren, sind die Websites möglicherweise für einige Typen standortübergreifender Angriffe anfällig, und Benutzer können auch ohne Cookies über Websites hinweg verfolgt werden, indem dem HTTP-Authentifizierungscache Einträge unter Verwendung der in URLs eingebetteten Anmeldeinformationen hinzugefügt werden.

Diese Richtlinie soll Unternehmen abhängig vom Vorgängerverhalten die Möglichkeit geben, ihre Anmeldeverfahren zu aktualisieren und wird in Zukunft entfernt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: GloballyScopeHTTPAuthCacheEnabled
  - Gruppenrichtlinienname: Globalen bereichsbezogenen HTTP-Authentifizierungscache aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: GloballyScopeHTTPAuthCacheEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: GloballyScopeHTTPAuthCacheEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### GoToIntranetSiteForSingleWordEntryInAddressBar
  #### Direkte Intranetsitenavigation erzwingen anstatt in der Adressleiste nach einzelnen Worteinträgen zu suchen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 78 oder höher

  #### Beschreibung
  Wenn Sie diese Richtlinie aktivieren, wird beim obersten Ergebnis der automatischen Vorschläge in der Vorschlagsliste der Adressleiste zu Intranetsites navigiert, sofern auf der Adressleiste ein einzelnes Wort ohne Interpunktion eingegeben wurde.

Bei Eingabe eines einzelnen Worts ohne Interpunktion erfolgt standardmäßig eine Navigation zu einer Intranetsite, die dem eingegebenen Text entspricht.

Wenn Sie diese Richtlinie aktivieren, führt das zweite Ergebnis der automatischen Vorschläge in der Vorschlagsliste der Adressleiste zu einer exakt wie eingegebenen Websuche, vorausgesetzt, bei diesem Text handelt es sich um ein einzelnes Wort ohne Zeichensetzung. Der Standardsuchanbieter wird verwendet, es sein denn, es wurde auch eine Richtlinie zur Verhinderung der Websuche aktiviert.

Die Aktivierung dieser Richtlinie bewirkt Folgendes:

Bei Abfragen mit einem einzelnen Wort, die üblicherweise zu einem Verlaufselement aufgelöst würden, erfolgt keine Navigation zu Sites mehr. Stattdessen versucht der Browser, zu internen Sites zu navigieren, die im Intranet einer Organisation möglicherweise nicht vorhanden sind. Dies führt zu einem 404-Fehler.

Für beliebte Suchbegriffe, die aus einem Wort bestehen, müssen manuell Suchvorschläge ausgewählt werden, damit eine ordnungsgemäße Suche ausgeführt wird.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Gruppenrichtlinienname: Direkte Intranetsitenavigation erzwingen anstatt in der Adressleiste nach einzelnen Worteinträgen zu suchen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### HSTSPolicyBypassList
  #### Konfigurieren der Liste mit Namen, die die HSTS-Richtlinienprüfung umgehen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 79 oder höher

  #### Beschreibung
  Die in dieser Liste angegebenen Hostnamen werden von der HSTS-Richtlinienprüfung ausgenommen, die unter Umständen Anforderungen von „http://“ auf „https://“ aktualisiert. In dieser Richtlinie sind nur Hostnamen mit einzelner Bezeichnung zulässig. Hostnamen müssen vereinheitlicht werden. Alle IDNs müssen ins Format für A-Einträge konvertiert werden, und alle ASCII-Zeichen müssen in Kleinbuchstaben angegeben werden. Diese Richtlinie gilt nur für die angegebenen Hostnamen und nicht für Unterdomänen der Namen in der Liste.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: HSTSPolicyBypassList
  - Gruppenrichtlinienname: Konfigurieren der Liste mit Namen, die die HSTS-Richtlinienprüfung umgehen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList\1 = "meet"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: HSTSPolicyBypassList
  - Beispielwert:
``` xml
<array>
  <string>meet</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### HardwareAccelerationModeEnabled
  #### Hardwarebeschleunigung verwenden (sofern verfügbar)
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Geben Sie an, ob die Hardwarebeschleunigung verwendet werden soll, sofern sie verfügbar ist. Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, wird die Hardwarebeschleunigung aktiviert, solange kein GPU-Feature ausdrücklich blockiert wird.

Wenn Sie diese Richtlinie deaktivieren, wird die Hardwarebeschleunigung deaktiviert.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: HardwareAccelerationModeEnabled
  - Gruppenrichtlinienname: Hardwarebeschleunigung verwenden (sofern verfügbar)
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: HardwareAccelerationModeEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: HardwareAccelerationModeEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### HideFirstRunExperience
  #### „Eindruck beim ersten Ausführen“ und Begrüßungsbildschirm ausblenden
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 80 oder höher

  #### Beschreibung
  Bei Aktivierung dieser Richtlinie werden „Eindruck beim ersten Ausführen“ und der Begrüßungsbildschirm nicht für Benutzer angezeigt, wenn sie Microsoft Edge zum ersten Mal ausführen.

Für die unter „Eindruck beim ersten Ausführen“ angezeigten Konfigurationsoptionen wird im Browser standardmäßig Folgendes durchgeführt:

- Auf der Seite „Neuer Tab“ wird der Feedtyp auf „MSN Nachrichten“ und das Layout auf „Inspirierend“ festgelegt.

- Der Benutzer wird weiterhin automatisch bei Microsoft Edge angemeldet, wenn das Windows-Konto den Typ Azure AD oder MSA hat.

- Die Synchronisierung ist standardmäßig nicht aktiviert, aber die Benutzer können dies in den Synchronisierungseinstellungen einschalten.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden „Eindruck beim ersten Ausführen“ und der Begrüßungsbildschirm angezeigt.

Hinweis: Die spezifischen Konfigurationsoptionen, die dem Benutzer unter „Eindruck beim ersten Ausführen“ angezeigt werden, können auch mit anderen spezifischen Richtlinien verwaltet werden. Sie können die HideFirstRunExperience-Richtlinie zusammen mit diesen Richtlinien verwenden, um auf Ihren verwalteten Geräten eine spezifische Browseroberfläche zu konfigurieren. Beispiele für andere geeignete Richtlinien sind:

-[AutoImportAtFirstRun](#autoimportatfirstrun)

-[NewTabPageLocation](#newtabpagelocation)

-[NewTabPageSetFeedType](#newtabpagesetfeedtype)

-[SyncDisabled](#syncdisabled)

-[BrowserSignin](#browsersignin)

-[NonRemovableProfileEnabled](#nonremovableprofileenabled)

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: HideFirstRunExperience
  - Gruppenrichtlinienname: „Eindruck beim ersten Ausführen“ und Begrüßungsbildschirm ausblenden
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: HideFirstRunExperience
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: HideFirstRunExperience
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ImportAutofillFormData
  #### Importieren von AutoAusfüllen-Formulardaten zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Erlaubt Benutzern, Daten aus AutoAusfüllen-Formularen von einem anderen Browser in Microsoft Edge zu importieren.

  Wenn Sie diese Richtlinie aktivieren, wird automatisch die Option zum manuellen Importieren von AutoAusfüllen-Daten ausgewählt.

Wenn Sie diese Richtlinie deaktivieren, werden beim ersten Ausführen keine AutoAusfüllen-Daten importiert, und Benutzer können sie nicht manuell importieren.

  Wenn Sie diese Richtlinie nicht konfigurieren, werden AutoAusfüllen-Daten beim ersten Ausführen importiert, und Benutzer können auswählen, ob diese Daten bei späteren Browsersitzungen manuell importiert werden sollen.

  Sie können diese Richtlinie auch als Empfehlung festlegen. Das bedeutet, dass in Microsoft Edge AutoAusfüllen-Daten beim ersten Ausführen importiert werden, aber Benutzer die Option **AutoAusfüllen-Daten** beim manuellen Import auswählen oder deaktivieren können.

  **Hinweis**: Diese Richtlinie verwaltet derzeit den Import aus den Browsern Google Chrome (unter Windows 7, 8 und 10 sowie unter MacOS) und Mozilla Firefox (unter Windows 7, 8 und 10 sowie unter MacOS).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ImportAutofillFormData
  - Gruppenrichtlinienname: Importieren von AutoAusfüllen-Formulardaten zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: ImportAutofillFormData
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ImportAutofillFormData
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ImportBrowserSettings
  #### Importieren von Browsereinstellungen zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 78 oder höher

  #### Beschreibung
  Ermöglicht Benutzern das Importieren von Browsereinstellungen aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, ist das Kontrollkästchen **Browsereinstellungen** im Dialogfeld **Browserdaten importieren** automatisch aktiviert.

Wenn Sie diese Richtlinie deaktivieren, werden bei der ersten Ausführung keine Browsereinstellungen importiert, und Benutzer können sie auch nicht manuell importieren.

Wenn Sie diese Richtlinie nicht konfigurieren, werden Browsereinstellungen bei der ersten Ausführung importiert, und die Benutzer können bei späteren Browsersitzungen wählen, ob sie sie manuell importieren möchten.

Sie können diese Richtlinie auch als Empfehlung festlegen. Das bedeutet, dass Microsoft Edge die Einstellungen bei der ersten Ausführung importiert und Benutzer die Option **Browsereinstellungen** beim manuellen Importieren aktivieren oder deaktivieren können.

**Hinweis**: Mit dieser Richtlinie wird derzeit das Importieren von Google Chrome (unter Windows 7, 8, und 10 sowie unter macOS) verwaltet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ImportBrowserSettings
  - Gruppenrichtlinienname: Importieren von Browsereinstellungen zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: ImportBrowserSettings
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ImportBrowserSettings
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ImportCookies
  #### Importieren von Cookies zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 81 oder höher

  #### Beschreibung
  Ermöglicht Benutzern das Importieren von Cookies aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie deaktivieren, werden Cookies bei der ersten Ausführung nicht importiert.

Wenn Sie diese Richtlinie nicht konfigurieren, werden Cookies bei der ersten Ausführung importiert.

Sie können diese Richtlinie auch als Empfehlung festlegen. Das bedeutet, dass Cookies von Microsoft Edge bei der ersten Ausführung importiert werden.

**Hinweis**: Mit dieser Richtlinie wird derzeit der Import aus Google Chrome (unter Windows 7, 8 und 10 sowie macOS) verwaltet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ImportCookies
  - Gruppenrichtlinienname: Importieren von Cookies zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: ImportCookies
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ImportCookies
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ImportExtensions
  #### Importieren von Erweiterungen zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 81 oder höher

  #### Beschreibung
  Ermöglicht Benutzern das Importieren von Erweiterungen aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, ist das Kontrollkästchen **Erweiterungen** im Dialogfeld **Browserdaten importieren** automatisch aktiviert.

Wenn Sie diese Richtlinie deaktivieren, werden bei der ersten Ausführung keine Erweiterungen importiert, und Benutzer können sie auch nicht manuell importieren.

Wenn Sie diese Richtlinie nicht konfigurieren, werden Erweiterungen bei der ersten Ausführung importiert, und die Benutzer können bei späteren Browsersitzungen wählen, ob Sie sie manuell importieren möchten.

Sie können diese Richtlinie auch als Empfehlung festlegen. Das bedeutet, dass Microsoft Edge die Erweiterungen bei der ersten Ausführung importiert und Benutzer die Option **Favoriten** beim manuellen Importieren aktivieren oder deaktivieren können.

**Hinweis**: Mit dieser Richtlinie wird derzeit der Import aus Google Chrome (unter Windows 7, 8 und 10 sowie macOS) verwaltet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ImportExtensions
  - Gruppenrichtlinienname: Importieren von Erweiterungen zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: ImportExtensions
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ImportExtensions
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ImportFavorites
  #### Importieren von Favoriten zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Erlaubt Benutzern, Favoriten von einem anderen Browser in Microsoft Edge zu importieren.

  Wenn Sie diese Richtlinie aktivieren, wird automatisch das Kontrollkästchen **Favoriten** im Dialogfeld **Browserdaten importieren** ausgewählt.

Wenn Sie diese Richtlinie deaktivieren, werden die Favoriten beim ersten Ausführen nicht importiert, und Benutzer können sie nicht manuell importieren.

  Wenn Sie diese Richtlinie nicht konfigurieren, werden die Favoriten beim ersten Ausführen importiert, und Benutzer können entscheiden, ob sie bei späteren Browsersitzungen manuell importiert werden sollen.

  Sie können diese Richtlinie auch als Empfehlung festlegen. Das bedeutet, dass in Microsoft Edge Favoriten beim ersten Ausführen importiert werden, aber Benutzer die Option **Favoriten** beim manuellen Import auswählen oder deaktivieren können.

  **Hinweis**: Diese Richtlinie verwaltet derzeit den Import aus den Browsern Internet Explorer (unter Windows 7, 8 und 10), Google Chrome (unter Windows 7, 8 und 10 sowie unter MacOS), Mozilla Firefox (unter Windows 7, 8 und 10 sowie unter MacOS) und Apple Safari (unter MacOS).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ImportFavorites
  - Gruppenrichtlinienname: Importieren von Favoriten zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: ImportFavorites
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ImportFavorites
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ImportHistory
  #### Importieren des Browserverlaufs zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Erlaubt Benutzern, ihren Browserverlauf von einem anderen Browser in Microsoft Edge zu importieren.

  Wenn Sie diese Richtlinie aktivieren, wird das Kontrollkästchen **Browserverlauf** im Dialogfeld **Browserdaten importieren** automatisch ausgewählt.

Wenn Sie diese Richtlinie deaktivieren, wird der Browserverlauf beim ersten Ausführen nicht importiert, und Benutzer können sie nicht manuell importieren.

  Wenn Sie diese Richtlinie nicht konfigurieren, wird der Browserverlauf beim ersten Ausführen importiert, und Benutzer können auswählen, ob sie bei späteren Browsersitzungen manuell importiert werden sollen.

  Sie können diese Richtlinie auch als Empfehlung festlegen. Das bedeutet, dass der Browserverlauf beim ersten Ausführen in Microsoft Edge importiert wird, aber Benutzer die Option **Verlauf** beim manuellen Import auswählen oder deaktivieren können.

  **Hinweis**: Diese Richtlinie verwaltet derzeit den Import aus den Browsern Internet Explorer (unter Windows 7, 8 und 10), Google Chrome (unter Windows 7, 8 und 10 sowie unter MacOS), Mozilla Firefox (unter Windows 7, 8 und 10 sowie unter MacOS) und Apple Safari (MacOS).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ImportHistory
  - Gruppenrichtlinienname: Importieren des Browserverlaufs zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: ImportHistory
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ImportHistory
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ImportHomepage
  #### Importieren von Startseiteneinstellungen zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Ermöglicht Benutzern das Importieren ihrer Startseiteneinstellung aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, wird die Option zum manuellen Importieren der Startseiteneinstellung automatisch ausgewählt.

Wenn Sie diese Richtlinie deaktivieren, wird die Startseiteneinstellung bei der ersten Ausführung nicht importiert, und Benutzer können sie auch nicht manuell importieren.

Wenn Sie diese Richtlinie nicht konfigurieren, wird die Startseiteneinstellung bei der ersten Ausführung importiert, und die Benutzer können bei späteren Browsersitzungen wählen, ob sie sie manuell importieren möchten.

Sie können diese Richtlinie als Empfehlung festlegen. Das bedeutet, dass Microsoft Edge die Startseiteneinstellung bei der ersten Ausführung importiert und Benutzer die Option **Startseite** beim manuellen Importieren aktivieren oder deaktivieren können.

**Hinweis**: Mit dieser Richtlinie wird derzeit das Importieren aus Internet Explorer (unter Windows 7, 8 und 10) verwaltet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ImportHomepage
  - Gruppenrichtlinienname: Importieren von Startseiteneinstellungen zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ImportHomepage
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ImportHomepage
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ImportOpenTabs
  #### Importieren offener Tabs zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 79 oder höher

  #### Beschreibung
  Ermöglicht Benutzern das Importieren von Browsereinstellungen aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, ist das Kontrollkästchen **Browsereinstellungen** im Dialogfeld **Browserdaten importieren** automatisch aktiviert.

Wenn Sie diese Richtlinie deaktivieren, werden bei der ersten Ausführung keine Browsereinstellungen importiert, und Benutzer können sie auch nicht manuell importieren.

Wenn Sie diese Richtlinie nicht konfigurieren, werden Browsereinstellungen bei der ersten Ausführung importiert, und die Benutzer können bei späteren Browsersitzungen wählen, ob Sie sie manuell importieren möchten.

Sie können diese Richtlinie auch als Empfehlung festlegen. Das bedeutet, dass Microsoft Edge die Einstellungen bei der ersten Ausführung importiert und Benutzer die Option **Browsereinstellungen** beim manuellen Importieren aktivieren oder deaktivieren können.

**Hinweis**: Mit dieser Richtlinie wird derzeit das Importieren von Google Chrome (unter Windows 7, 8, und 10 sowie unter macOS) verwaltet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ImportOpenTabs
  - Gruppenrichtlinienname: Importieren offener Tabs zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: ImportOpenTabs
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ImportOpenTabs
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ImportPaymentInfo
  #### Import von Zahlungsinformationen zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Ermöglicht Benutzern das Importieren von Zahlungsinformationen aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, wird das Kontrollkästchen **Zahlungsinformationen** automatisch im Dialogfeld **Browserdaten importieren** aktiviert.

Wenn Sie diese Richtlinie deaktivieren, werden Zahlungsinformationen bei der erstmaligen Ausführung nicht importiert, und Benutzer können sie nicht manuell importieren.

Wenn Sie diese Richtlinie nicht konfigurieren, werden Zahlungsinformationen bei der erstmaligen Ausführung importiert, und die Benutzer können auswählen, ob sie bei späteren Browsersitzungen manuell importiert werden sollen.

Sie können diese Richtlinie auch als Empfehlung festlegen. Dies bedeutet, dass Microsoft Edge Zahlungsinformationen bei der erstmaligen Ausführung importiert, Benutzer die Option **Zahlungsinformationen** aber während des manuellen Imports aktivieren oder deaktivieren können.

**Hinweis:** Diese Richtlinie dient derzeit zum Verwalten des Imports aus Google Chrome (unter Windows 7, 8 und 10 sowie macOS).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ImportPaymentInfo
  - Gruppenrichtlinienname: Import von Zahlungsinformationen zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: ImportPaymentInfo
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ImportPaymentInfo
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ImportSavedPasswords
  #### Importieren gespeicherter Kennwörter zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Erlaubt Benutzern, gespeicherte Kennwörter von einem anderen Browser in Microsoft Edge zu importieren.

  Wenn Sie diese Richtlinie aktivieren, wird automatisch die Option zum manuellen Importieren gespeicherter Kennwörter ausgewählt.

Wenn Sie diese Richtlinie deaktivieren, werden gespeicherte Kennwörter beim ersten Ausführen nicht importiert, und Benutzer können sie nicht manuell importieren.

  Wenn Sie diese Richtlinie nicht konfigurieren, werden Kennwörter beim ersten Ausführen importiert, und Benutzer können auswählen, ob sie bei späteren Browsersitzungen manuell importiert werden sollen.

  Sie können diese Richtlinie auch als Empfehlung festlegen. Das bedeutet, dass in Microsoft Edge Kennwörter beim ersten Ausführen importiert werden, aber Benutzer die Option **Kennwörter** beim manuellen Import auswählen oder deaktivieren können.

  **Hinweis**: Diese Richtlinie verwaltet derzeit den Import aus den Browsern Internet Explorer (unter Windows 7, 8 und 10), Google Chrome (unter Windows 7, 8 und 10 sowie unter MacOS) und Mozilla Firefox (unter Windows 7, 8 und 10 sowie unter MacOS).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ImportSavedPasswords
  - Gruppenrichtlinienname: Importieren gespeicherter Kennwörter zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: ImportSavedPasswords
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ImportSavedPasswords
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ImportSearchEngine
  #### Importieren von Suchmaschineneinstellungen zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Ermöglicht Benutzern das Importieren von Suchmaschineneinstellungen aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, wird die Option zum Importieren von Suchmaschineneinstellungen automatisch ausgewählt.

Wenn Sie diese Richtlinie deaktivieren, werden bei der ersten Ausführung keine Suchmaschineneinstellungen importiert, und Benutzer können sie auch nicht manuell importieren.

Wenn Sie diese Richtlinie nicht konfigurieren, werden die Suchmaschineneinstellungen bei der ersten Ausführung importiert, und die Benutzer können bei späteren Browsersitzungen wählen, ob sie sie manuell importieren möchten.

Sie können diese Richtlinie als Empfehlung festlegen. Das bedeutet, dass Microsoft Edge die Suchmaschineneinstellungen bei der ersten Ausführung importiert und Benutzer die Option **Suchmaschine** beim manuellen Importieren aktivieren oder deaktivieren können.

**Hinweis**: Mit dieser Richtlinie wird derzeit das Importieren aus Internet Explorer (unter Windows 7, 8 und 10) verwaltet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ImportSearchEngine
  - Gruppenrichtlinienname: Importieren von Suchmaschineneinstellungen zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: ImportSearchEngine
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ImportSearchEngine
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ImportShortcuts
  #### Importieren von Tastenkombinationen zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 81 oder höher

  #### Beschreibung
  Ermöglicht Benutzern das Importieren von Tastenkombinationen aus einem anderen Browser in Microsoft Edge.

Wenn Sie diese Richtlinie deaktivieren, werden Tastenkombinationen bei der ersten Ausführung nicht importiert.

Wenn Sie diese Richtlinie nicht konfigurieren, werden Tastenkombinationen bei der ersten Ausführung importiert.

Sie können diese Richtlinie auch als Empfehlung festlegen. Dies bedeutet, dass Tastenkombinationen von Microsoft Edge bei der ersten Ausführung importiert werden.

**Hinweis**: Mit dieser Richtlinie wird derzeit der Import aus Google Chrome (unter Windows 7, 8 und 10 sowie macOS) unterstützt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ImportShortcuts
  - Gruppenrichtlinienname: Importieren von Tastenkombinationen zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: ImportShortcuts
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ImportShortcuts
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### InPrivateModeAvailability
  #### Verfügbarkeit des InPrivate-Modus konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Diese Richtlinie gibt an, ob der Benutzer Seiten im InPrivate-Modus in Microsoft Edge öffnen kann.

Wenn Sie diese Richtlinie nicht konfigurieren oder auf “Enabled” festlegen, können Benutzer Seiten im InPrivate-Modus öffnen.

Legen Sie diese Richtlinie auf “Disabled” fest, um Benutzer daran zu hindern, den InPrivate-Modus zu verwenden.

Legen Sie diese Richtlinie auf “Forced”, um immer den InPrivate-Modus zu verwenden.

Zuordnung der Richtlinienoptionen:

* Enabled (0) = InPrivate-Modus verfügbar

* Disabled (1) = InPrivate-Modus deaktiviert

* Forced (2) = InPrivate-Modus erzwungen

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: InPrivateModeAvailability
  - Gruppenrichtlinienname: Verfügbarkeit des InPrivate-Modus konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: InPrivateModeAvailability
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: InPrivateModeAvailability
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### InsecureFormsWarningsEnabled
  #### Warnungen für unsichere Formulare aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 86 oder höher

  #### Beschreibung
  This policy controls the handling of insecure forms (forms submitted over HTTP) embedded in secure (HTTPS) sites in the browser.
If you enable this policy or don't set it, a full page warning will be shown when an insecure form is submitted. Additionally, a warning bubble will be shown next to the form fields when they are focused, and autofill will be disabled for those forms.
If you disable this policy, warnings will not be shown for insecure forms, and autofill will work normally.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: InsecureFormsWarningsEnabled
  - Gruppenrichtlinienname: Warnungen für unsichere Formulare aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: InsecureFormsWarningsEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: InsecureFormsWarningsEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### IntensiveWakeUpThrottlingEnabled
  #### Steuern des Features “IntensiveWakeUpThrottling”
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 85 oder höher

  #### Beschreibung
  Wenn das Feature “IntensiveWakeUpThrottling” aktiviert ist, werden JavaScript-Timer auf Registerkarten im Hintergrund aggressiv gedrosselt und zusammengeführt, sodass sie nicht mehr als einmal pro Minute ausgeführt werden, nachdem eine Seite für fünf Minuten oder länger im Hintergrund ausgeführt wurde.

Dieses Feature ist konform mit Webstandards, kann jedoch die Funktionalität mancher Websites stören, indem bestimmte Aktionen bis zu eine Minute lang verzögert werden. Das Feature führt jedoch zu erheblichen CPU- und Akkueinsparungen, wenn es aktiviert ist. Weitere Details finden Sie unter https://bit.ly/30b1XR4.

Wenn Sie diese Richtlinie aktivieren, wird das Feature zwingend aktiviert, und die Benutzer können diese Einstellung nicht überschreiben.
Wenn Sie diese Richtlinie deaktivieren, wird das Feature zwingend deaktiviert, und Benutzer können diese Einstellung nicht überschreiben.
Wenn Sie diese Richtlinie nicht konfigurieren, wird die Funktion von einer eigenen internen Logik gesteuert. Benutzer können diese Einstellung manuell konfigurieren.

Beachten Sie, dass die Richtlinie per Renderer-Prozess angewendet wird, wobei der neueste Wert der Richtlinieneinstellung in Kraft tritt, wenn ein Renderer-Prozesses gestartet wird. Ein vollständiger Neustart ist erforderlich, um sicherzustellen, dass alle geladenen Registerkarten eine konsistente Richtlinieneinstellung erhalten. Es ist aber ungefährlich, die Prozesse mit unterschiedlichen Werten für diese Richtlinie auszuführen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: IntensiveWakeUpThrottlingEnabled
  - Gruppenrichtlinienname: Steuern des Features “IntensiveWakeUpThrottling”
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: IntensiveWakeUpThrottlingEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: IntensiveWakeUpThrottlingEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### InternetExplorerIntegrationEnhancedHangDetection
  #### Konfigurieren der erweiterten Erkennung hängender Webseiten für den Internet Explorer-Modus
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 84 oder höher

  #### Beschreibung
  Die erweiterte Erkennung nicht mehr reagierender Webseiten ist ein differenzierterer Ansatz zum Erkennen solcher Webseiten im Internet Explorer-Modus als die im Internet Explorer verwendete Option. Wenn eine nicht mehr reagierende Webseite erkannt wird, wendet der Browser eine Entschärfung an, um zu verhindern, dass der gesamte Browsers ebenfalls nicht mehr reagiert.

Diese Einstellung ermöglicht es Ihnen, die Verwendung der erweiterten Erkennung nicht mehr reagierender Webseiten für den Fall zu konfigurieren, dass Sie mit einer ihrer Websites Probleme mit fehlender Kompatibilität haben. Es wird empfohlen, diese Richtlinie nur zu deaktivieren, wenn Benachrichtigungen wie “(Website) reagiert nicht” im Internet Explorer-Modus, jedoch nicht im eigenständigen Internet Explorer angezeigt werden.

Diese Einstellung funktioniert in Verbindung mit:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) ist festgelegt auf "IEMode"
und
der Richtlinie “[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)”, wobei die Liste mindestens einen Eintrag enthält.

 Wenn Sie diese Richtlinie auf "Enabled" festgelegen oder nicht konfigurieren, wird für Websites, die im Internet Explorer-Modus ausgeführt werden, die erweiterte Erkennung nicht mehr reagierender Webseiten verwendet.

 Wenn Sie diese Richtlinie auf "Disabled" festgelegen, ist die Option zur erweiterten Erkennung nicht mehr reagierender Webseiten deaktiviert und die Benutzer arbeiten mit dem Standardverhalten des Internet Explorer zur Erkennung nicht mehr reagierender Webseiten.

Weitere Informationen zum Internet Explorer-Modus finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210).

Zuordnung der Richtlinienoptionen:

* Disabled (0) = Erweiterte Erkennung hängender Webseiten deaktiviert

* Enabled (1) = Erweiterte Erkennung hängender Webseiten aktiviert

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: InternetExplorerIntegrationEnhancedHangDetection
  - Gruppenrichtlinienname: Konfigurieren der erweiterten Erkennung hängender Webseiten für den Internet Explorer-Modus
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: InternetExplorerIntegrationEnhancedHangDetection
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### InternetExplorerIntegrationLevel
  #### Internet Explorer-Integration konfigurieren
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 77 oder höher

  #### Beschreibung
  Anleitungen zum Konfigurieren der optimalen Benutzeroberfläche für den Internet Explorer-Modus finden Sie unter "[https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)".

Zuordnung der Richtlinienoptionen:

* None (0) = Keine

* IEMode (1) = Internet Explorer-Modus

* NeedIE (2) = Internet Explorer 11

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: InternetExplorerIntegrationLevel
  - Gruppenrichtlinienname: Internet Explorer-Integration konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: InternetExplorerIntegrationLevel
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### InternetExplorerIntegrationSiteList
  #### Enterprise Mode Site List konfigurieren
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 78 oder höher

  #### Beschreibung
  Anleitungen zum Konfigurieren der optimalen Benutzeroberfläche für den Internet Explorer-Modus finden Sie unter "[https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)".

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: InternetExplorerIntegrationSiteList
  - Gruppenrichtlinienname: Enterprise Mode Site List konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: InternetExplorerIntegrationSiteList
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"https://internal.contoso.com/sitelist.xml"
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### InternetExplorerIntegrationSiteRedirect
  #### Angeben des Verhaltens von seiteninternen Navigationsvorgängen zu nicht konfigurierten Websites, wenn diese über Seiten im Internet Explorer-Modus gestartet werden
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 81 oder höher

  #### Beschreibung
  Eine “In-Page“-Navigation wird über einen Link, ein Skript oder ein Formular auf der aktuellen Seite gestartet. Es kann auch eine serverseitige Umleitung eines früheren “In-Page“-Navigationsversuchs sein. Umgekehrt kann ein Benutzer über die Browser-Steuerelemente eine Navigation starten, die nicht “in-page“ und unabhängig von der aktuellen Seite ist, beispielsweise über die Adressleiste, die Zurück-Taste oder einen Favoritenlink.

Mit dieser Einstellung können Sie festlegen, ob die Navigation von im Internet Explorer-Modus geladenen Seiten zu nicht konfigurierten Websites (die nicht in der Siteliste für den Enterprise-Modus konfiguriert sind) wieder zu Microsoft Edge zurückkehrt oder im Internet Explorer-Modus bleibt.

Diese Einstellung funktioniert in Verbindung mit:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) ist festgelegt auf “EIMode”
und
der Richtlinie “[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)”, wenn die Liste mindestens einen Eintrag enthält.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden in diesem Modus nur Websites geöffnet, die für das Öffnen im Internet Explorer-Modus konfiguriert sind. Jede Website, die nicht für das Öffnen im Internet Explorer-Modus konfiguriert ist, wird zurück zu Microsoft Edge umgeleitet.

Wenn Sie diese Richtlinie auf “Default” festlegen, werden in diesem Modus nur Websites geöffnet, die für das Öffnen im Internet Explorer-Modus konfiguriert sind. Jede Website, die nicht für das Öffnen im Internet Explorer-Modus konfiguriert ist, wird zurück zu Microsoft Edge umgeleitet.

Falls Sie diese Richtlinie auf “AutomaticNavigationsOnly” festlegen, erhalten Sie die Standarderfahrung mit der Ausnahme, dass alle automatischen Navigationen (z.B. 302-Umleitungen) zu nicht konfigurierten Websites im Internet Explorer-Modus verbleiben.

Falls Sie diese Richtlinie auf “AllInPageNavigations” festlegen, verbleiben alle Navigationen von Seiten, die im IE-Modus geladen wurden, auf nicht konfigurierten Websites im Internet Explorer-Modus (am wenigsten empfohlen).

Weitere Informationen zum Internet Explorer-Modus finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2105106](https://go.microsoft.com/fwlink/?linkid=2105106)

Zuordnung der Richtlinienoptionen:

* Default (0) = Standard

* AutomaticNavigationsOnly (1) = Nur automatische Navigation im Internet Explorer-Modus beibehalten

* AllInPageNavigations (2) = Gesamte seiteninterne Navigation im Internet Explorer-Modus beibehalten

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: InternetExplorerIntegrationSiteRedirect
  - Gruppenrichtlinienname: Angeben des Verhaltens von seiteninternen Navigationsvorgängen zu nicht konfigurierten Websites, wenn diese über Seiten im Internet Explorer-Modus gestartet werden
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: InternetExplorerIntegrationSiteRedirect
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### InternetExplorerIntegrationTestingAllowed
  #### Allow Internet Explorer mode testing
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 86 oder höher

  #### Beschreibung
  This policy is a replacement for the ie-mode-test flag policy. It lets users open an IE mode tab from the UI menu option.

This setting works in conjunction with:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) is set to 'IEMode'
and
[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) policy where the list has at least one entry.

If you enable this policy, users can open IE mode tab from the UI option and navigate current site to an IE mode site.

If you disable this policy, users can't see the UI option in the menu directly.

If you don't configure this policy, you can set up the ie-mode-test flag manually.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: InternetExplorerIntegrationTestingAllowed
  - Gruppenrichtlinienname: Allow Internet Explorer mode testing
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: InternetExplorerIntegrationTestingAllowed
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### IsolateOrigins
  #### Websiteisolation für bestimmte Ursprünge aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt Quellen an, die isoliert in einem eigenen Prozess ausgeführt werden sollen.
Diese Richtlinie isoliert auch Quellen, die von Subdomains benannt werden. Beispielsweise bewirkt die Angabe von https://contoso.com/, dass https://foo.contoso.com/ als Teil der Website https://contoso.com/ isoliert wird.
Wenn die Richtlinie aktiviert ist, wird jeder in einer kommagetrennten Liste stehenden Quellen in einem eigenen Prozess ausgeführt.
Wenn Sie diese Richtlinie deaktivieren, sind die Features 'IsolateOrigins' und 'SitePerProcess' deaktiviert. Benutzer können die Richtlinie 'IsolateOrigins' weiterhin manuell über Befehlszeilen-Flags aktivieren.
Wenn Sie die Richtlinie nicht konfigurieren, kann der Benutzer diese Einstellung ändern.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: IsolateOrigins
  - Gruppenrichtlinienname: Websiteisolation für bestimmte Ursprünge aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: IsolateOrigins
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"https://contoso.com/,https://fabrikam.com/"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: IsolateOrigins
  - Beispielwert:
``` xml
<string>https://contoso.com/,https://fabrikam.com/</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### LocalProvidersEnabled
  #### Vorschläge von lokalen Anbietern zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 83 oder höher

  #### Beschreibung
  Sie können Vorschläge von Vorschlagsanbietern auf dem Gerät (lokale Anbieter) zulassen, z. B. "Favoriten" und "Browserverlauf", in der Adressleiste und der Liste der automatischen Vorschläge von Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, werden Vorschläge von lokalen Anbietern verwendet.

 Wenn Sie diese Richtlinie deaktivieren, werden keine Vorschläge von lokalen Anbietern verwendet. Vorschläge für lokale Historie und lokale Favoriten werden nicht angezeigt.

 Wenn Sie diese Richtlinie nicht konfigurieren, sind Vorschläge von lokalen Anbietern zulässig, aber der Benutzer kann dies mithilfe der Umschaltfläche "Einstellungen" ändern.

 Bitte beachten Sie, dass einige Features möglicherweise nicht verfügbar sind, wenn eine Richtlinie zum Deaktivieren dieses Features angewendet wurde. Wenn Sie die [SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)-Richtlinie aktivieren, sind z.B. die Vorschläge zum Browserverlauf nicht verfügbar.

Für diese Richtlinie muss ein Neustart des Browsers ausgeführt werden, um die Anwendung abzuschließen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: LocalProvidersEnabled
  - Gruppenrichtlinienname: Vorschläge von lokalen Anbietern zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: LocalProvidersEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: LocalProvidersEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ManagedFavorites
  #### Favoriten konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Konfiguriert eine Liste verwalteter Favoriten.

Die Richtlinie erstellt eine Liste mit Favoriten. Jeder Favorit enthält die Schlüssel "Name" und "URL", die den Namen des Favoriten und sein Ziel enthalten. Sie können einen Unterordner konfigurieren, indem Sie einen Favoriten ohne einen "URL"-Schlüssel definieren, jedoch mit einem zusätzlichen "Children"-Schlüssel, der eine Liste der oben definierten Favoriten enthält (von denen einige möglicherweise wieder Ordner sind). Microsoft Edge ändert unvollständige URLs so, als ob sie über die Adressleiste eingegeben wurden, z. B. wird "microsoft.com" zu "https://microsoft.com/".

Diese Favoriten werden in einem Ordner abgelegt, der nicht vom Benutzer geändert werden kann (der Benutzer kann jedoch auswählen, dass er in der Favoritenleiste ausgeblendet werden soll). Standardmäßig lautet der Ordnername "Verwaltete Favoriten". Sie können ihn jedoch ändern, indem Sie der Liste der Favoriten ein Wörterbuch mit dem Schlüssel "toplevel_name" mit dem gewünschten Ordnernamen als Wert hinzufügen.

Verwaltete Favoriten werden nicht mit dem Benutzerkonto synchronisiert und können nicht durch Erweiterungen geändert werden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Wörterbuch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ManagedFavorites
  - Gruppenrichtlinienname: Favoriten konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ManagedFavorites
  - Werttyp: REG_SZ
  ##### Beispielwert:
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


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ManagedFavorites
  - Beispielwert:
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
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ManagedSearchEngines
  #### Suchmaschinen verwalten
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Hiermit können Sie eine Liste mit bis zu 10 Suchmaschinen konfigurieren, von denen eine als Standardsuchmaschine gekennzeichnet sein muss.
 Sie müssen für keine Suchmaschine die Codierung angeben. Ab Microsoft Edge 80 sind die Parameter „suggest_url“ und „image_search_url“ optional. Der optionale Parameter „image_search_post_params“ (besteht aus durch Trennzeichen getrennten Name/Wert-Paaren) ist ab Microsoft Edge 80 verfügbar.

 Ab Microsoft Edge 83 können Sie die Suchmaschinenerkennung mit dem optionalen Parameter „allow_search_engine_discovery“ aktivieren. Dieser Parameter muss das erste Element in der Liste sein. Falls „allow_search_engine_discovery“ nicht festgelegt ist, wird die Suchmaschinenerkennung standardmäßig deaktiviert. Ab Microsoft Edge 84 können Sie diese Richtlinie als empfohlene Richtlinie festlegen, um die Suchmaschinenerkennung zuzulassen. Sie müssen den optionalen Parameter „allow_search_engine_discovery“ nicht zulassen.

Wenn Sie diese Richtlinie aktivieren, können Benutzer in der Liste keine Suchmaschine hinzufügen, entfernen oder ändern. Benutzer können jede Suchmaschine in der Liste als ihre Standardsuchmaschine festlegen.

  Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, können Benutzer die Suchmaschinenliste nach Belieben ändern.

 Wenn die [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)-Richtlinie festgelegt ist, wird die Richtlinie (ManagedSearchEngines) ignoriert. Der Benutzer muss seinen Browser neu starten, um die Anwendung dieser Richtlinie abzuschließen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Wörterbuch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ManagedSearchEngines
  - Gruppenrichtlinienname: Suchmaschinen verwalten
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: ManagedSearchEngines
  - Werttyp: REG_SZ
  ##### Beispielwert:
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


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ManagedSearchEngines
  - Beispielwert:
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
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### MaxConnectionsPerProxy
  #### Maximale Anzahl gleichzeitiger Verbindungen mit dem Proxyserver
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt die maximale Anzahl gleichzeitiger Verbindungen mit dem Proxyserver an.

Einige Proxyserver können keine hohe Anzahl gleichzeitiger Verbindungen pro Client verarbeiten. Sie können dies lösen, indem Sie für diese Richtlinie einen niedrigeren Wert festlegen.

Der Wert dieser Richtlinie muss niedriger als 100 und höher als 6 sein. Der Standardwert ist 32.

Einige Webanwendungen sind dafür bekannt, viele Verbindungen mit hängenden GETs zu verbrauchen. Das Senken der maximalen Anzahl auf weniger als 32 kann dazu führen, dass sich das Browsernetzwerk aufhängt, wenn zu viele Web-Apps dieser Art geöffnet sind.

Wenn Sie diese Richtlinie nicht konfigurieren, wird der Standardwert (32) verwendet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: MaxConnectionsPerProxy
  - Gruppenrichtlinienname: Maximale Anzahl gleichzeitiger Verbindungen mit dem Proxyserver
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: MaxConnectionsPerProxy
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000020
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: MaxConnectionsPerProxy
  - Beispielwert:
``` xml
<integer>32</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### MediaRouterCastAllowAllIPs
  #### Google Cast erlauben, eine Verbindung mit CAST-Geräten auf allen IP-Adressen herzustellen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Aktivieren Sie diese Richtlinie, damit Google Cast eine Verbindung zu Cast-Geräten mit allen IP-Adressen herstellen kann, nicht nur mit privaten RFC1918/RFC4193-Adressen.

Deaktivieren Sie diese Richtlinie, um Google Cast auf Cast-Geräte mit privaten RFC1918/RFC4193-Adressen zu beschränken.

Wenn Sie diese Richtlinie nicht konfigurieren, verbindet sich Google Cast nur mit Cast-Geräten mit privaten RFC1918/RFC4193-Adressen, es sei denn, Sie aktivieren das CastAllowAllIPs-Feature.

Wenn die Richtlinie [EnableMediaRouter](#enablemediarouter) deaktiviert ist, hat diese Richtlinie keine Wirkung.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: MediaRouterCastAllowAllIPs
  - Gruppenrichtlinienname: Google Cast erlauben, eine Verbindung mit CAST-Geräten auf allen IP-Adressen herzustellen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: MediaRouterCastAllowAllIPs
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: MediaRouterCastAllowAllIPs
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### MetricsReportingEnabled
  #### Meldung von nutzungs- und absturzbezogenen Daten aktivieren (veraltet)
  >VERALTET: Diese Richtlinie ist veraltet. Sie wird gegenwärtig noch unterstützt, aber in einem zukünftigen Release ausgemustert.
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Diese Richtlinie ist veraltet. Sie wird im Augenblick noch unterstützt, ist in Microsoft Edge 89 aber veraltet. Sie wird durch eine neue Richtlinie ersetzt:  [DiagnosticData](#diagnosticdata) für Windows 7, Windows 8 und macOS. Auf Windows 10 wird sie durch “Telemetrie zulassen” ersetzt ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

Diese Richtlinie ermöglicht das Melden von Nutzungs- und absturzbezogenen Daten im Zusammenhang mit Microsoft Edge an Microsoft.

Aktivieren Sie diese Richtlinie, um Berichte mit Nutzungs- und absturzbezogenen Daten an Microsoft zu senden. Deaktivieren Sie diese Richtlinie, um die Daten nicht an Microsoft zu senden. In beiden Fällen kann die Einstellung nicht vom Benutzer geändert oder überschrieben werden.

Unter Windows 10 gilt: Wenn Sie diese Richtlinie nicht konfigurieren, verwendet Microsoft Edge standardmäßig die Einstellung für Windows-Diagnosedaten. Wenn Sie diese Richtlinie aktivieren, sendet Microsoft Edge nur dann Nutzungsdaten, wenn die Einstellung für Windows-Diagnosedaten auf “Erweitert“ oder “Vollständig“ festgelegt ist. Wenn Sie diese Richtlinie deaktivieren, sendet Microsoft Edge keine Nutzungsdaten. Absturzbezogene Daten werden auf der Grundlage der Einstellung für Windows-Diagnosedaten gesendet. Weitere Informationen zu Einstellungen für Windows-Diagnosedaten finden Sie hier: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

Unter Windows 7, Windows 8 und macOS gilt: Diese Richtlinie steuert das Senden von Nutzungs- und absturzbezogenen Daten. Wenn Sie diese Richtlinie nicht konfigurieren, verwendet Microsoft Edge standardmäßig die Einstellung des Benutzers.

Um diese Richtlinie zu aktivieren, muss [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) auf “Aktiviert” festgelegt werden. Wenn [MetricsReportingEnabled](#metricsreportingenabled) oder [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) nicht konfiguriert oder deaktiviert sind, werden keine Daten an Microsoft gesendet.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind. Sie ist außerdem für macOS-Instanzen verfügbar, die mithilfe des MDM verwaltet werden, oder via MCX mit einer Domäne verknüpft sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: MetricsReportingEnabled
  - Gruppenrichtlinienname: Meldung von nutzungs- und absturzbezogenen Daten aktivieren (veraltet)
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: MetricsReportingEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: MetricsReportingEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NativeWindowOcclusionEnabled
  #### Aktivieren Sie die ursprüngliche Fensterschließung
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 84 oder höher

  #### Beschreibung
  Aktiviert die Okklusion systemeigener Fenster in Microsoft Edge.

Wenn Sie diese Einstellung aktivieren, um CPU- und Energieverbrauch zu reduzieren, erkennt Microsoft Edge, wenn ein Fenster von anderen Fenstern verdeckt wird, und hält das Bemalen von Pixeln an.

Falls Sie diese Einstellung Microsoft Edge deaktivieren, wird nicht erkannt, wenn ein Fenster von anderen Fenstern verdeckt wird.

Falls diese Richtlinie nicht festgelegt bleibt, wird die Erkennung ausgeblendeter Fenster aktiviert.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: NativeWindowOcclusionEnabled
  - Gruppenrichtlinienname: Aktivieren Sie die ursprüngliche Fensterschließung
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: NativeWindowOcclusionEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NavigationDelayForInitialSiteListDownloadTimeout
  #### Festlegen eines Timeouts für die Verzögerung der Registerkartennavigation für die Website-Liste zum Unternehmensmodus
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 84 oder höher

  #### Beschreibung
  Diese Richtlinie ermöglicht es Ihnen, einen Timeout (in Sekunden) für Registerkarten in Microsoft Edge festzulegen, die auf die Navigation warten, bis der Browser die ursprüngliche Website-Liste für den Unternehmensmodus heruntergeladen hat.

Diese Einstellung funktioniert gemeinsam mit:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) festgelegt auf “IEMode”
und der
Richtlinie “[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)”, wobei die Liste mindestens einen Eintrag enthält
 und
[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload) auf “Alle berechtigten Navigationselemente“ (1) festgelegt ist.

 Registerkarten warten nicht länger als bis zum Timeout ab, bevor die Website-Liste für den Unternehmensmodus heruntergeladen wird. Sofern der Browser die Website-Liste für den Unternehmensmodus bei Ablauf des Timeouts noch nicht vollständig heruntergeladen hat, wird die Navigation von Microsoft Edge-Registerkarten trotzdem fortgesetzt. Der als Timeout festgelegte Wert darf nicht weniger als 1 Sekunde und nicht mehr als 2 Sekunden betragen.

 Wenn Sie den Timeout-Wert in dieser Richtlinie auf einen höheren als den Standardwert von 2 Sekunden festlegen, wird dem Benutzer nach 2 Sekunden eine Informationsleiste angezeigt. Sie beinhaltet eine Schaltfläche, die es ihm ermöglicht, das Warten auf den vollständigen Download der Website-Liste für den Unternehmensmodus abzubrechen.

Wenn Sie diese Richtlinie nicht konfigurieren, wird der Standardwert von 2 Sekunden für den Timeout verwendet. Zukünftige Änderungen dieses Standardwerts sind möglich.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: NavigationDelayForInitialSiteListDownloadTimeout
  - Gruppenrichtlinienname: Festlegen eines Timeouts für die Verzögerung der Registerkartennavigation für die Website-Liste zum Unternehmensmodus
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: NavigationDelayForInitialSiteListDownloadTimeout
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x0000000a
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NetworkPredictionOptions
  #### Netzwerkvorhersage aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Aktiviert die Netzwerkvorhersage und verhindert, dass Benutzer diese Einstellung ändern.

Diese Richtlinie steuert DNS-Vorabrufe, TCP- und SSL-Vorabverbindungen sowie das Prerendering von Webseiten.

Wenn Sie diese Richtlinie nicht konfigurieren, ist die Netzwerkvorhersage aktiviert, kann aber vom Benutzer geändert werden.

Zuordnung der Richtlinienoptionen:

* NetworkPredictionAlways (0) = Netzwerkaktionen für beliebige Netzwerkverbindung vorhersagen

* NetworkPredictionWifiOnly (1) = Nicht unter stützt. wenn dieser Wert verwendet wird, wird er behandelt, wenn "Netzwerk Aktionen für alle Netzwerk Verbindungen (0)" vorher gesagt wurde.

* NetworkPredictionNever (2) = Keine Netzwerkaktionen für Netzwerkverbindungen vorhersagen

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: NetworkPredictionOptions
  - Gruppenrichtlinienname: Netzwerkvorhersage aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: NetworkPredictionOptions
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000002
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: NetworkPredictionOptions
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### NonRemovableProfileEnabled
  #### Konfigurieren, ob für einen Benutzer beim Anmelden mit dem Geschäfts-, Schul-oder Unikonto immer automatisch ein Standardprofil vorhanden ist.
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 78 oder höher

  #### Beschreibung
  Mit dieser Richtlinie wird bestimmt, ob das Microsoft Edge-Profil, das für das Geschäfts-, Schul- oder Unikonto eines Benutzers automatisch angemeldet wird, entfernt werden kann.

Wenn Sie diese Richtlinie aktivieren, wird mit dem Geschäfts-, Schul- oder Unikonto des Benutzers unter Windows ein nicht entfernbares Profil erstellt. Dieses Profil kann nicht abgemeldet oder entfernt werden.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, kann das Profil, das für das Geschäfts-, Schul- oder Unikonto eines Benutzers unter Windows automatisch angemeldet wird, vom Benutzer abgemeldet oder entfernt werden.

Verwenden Sie die Richtlinie [BrowserSignin](#browsersignin), wenn Sie die Browseranmeldung konfigurieren möchten.

Diese Richtlinie ist nur für Windows-Instanzen verfügbar, die mit einer Microsoft Active Directory-Domäne, mit Windows 10 Pro- oder Enterprise-Instanzen verknüpft sind, die für die Geräteverwaltung registriert sind.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: NonRemovableProfileEnabled
  - Gruppenrichtlinienname: Konfigurieren, ob für einen Benutzer beim Anmelden mit dem Geschäfts-, Schul-oder Unikonto immer automatisch ein Standardprofil vorhanden ist.
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: NonRemovableProfileEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### OverrideSecurityRestrictionsOnInsecureOrigin
  #### Steuert, wo Sicherheitseinschränkungen für unsichere Ursprünge gelten
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt eine Liste mit Ursprüngen (URLs) oder Hostnamen-Mustern (z. B. „*.contoso.com“) an, für die keine Sicherheitseinschränkungen bei unsicheren Ursprüngen gelten.

Mit dieser Richtlinie können Sie die zulässigen Ursprünge für ältere Anwendungen angeben, die TLS nicht bereitstellen kann, oder einen Stagingserver für die interne Webentwicklung einrichten, sodass Entwickler Features testen können, die sichere Kontexte erfordern, ohne dass TLS auf dem Server bereitgestellt ist. Durch diese Richtlinie wird auch verhindert, dass der Ursprung in der Omnibox als „nicht sicher“ gekennzeichnet ist.

Das Festlegen einer Liste von URLs in dieser Richtlinie hat denselben Effekt wie das Festlegen des Befehlszeilenflags „--unsafely-treat-insecure-origin-as-secure“ in einer durch Kommas getrennte Liste derselben URLs. Wenn Sie diese Richtlinie aktivieren, wird das Befehlszeilenflag überschrieben.

Weitere Informationen zu sicheren Kontexten finden Sie unter https://www.w3.org/TR/secure-contexts/.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: OverrideSecurityRestrictionsOnInsecureOrigin
  - Gruppenrichtlinienname: Steuert, wo Sicherheitseinschränkungen für unsichere Ursprünge gelten
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\1 = "http://testserver.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\2 = "*.contoso.com"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: OverrideSecurityRestrictionsOnInsecureOrigin
  - Beispielwert:
``` xml
<array>
  <string>http://testserver.contoso.com/</string>
  <string>*.contoso.com</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PaymentMethodQueryEnabled
  #### Abfragemöglichkeiten für verfügbare Zahlungsmethoden durch Websites zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 80 oder höher

  #### Beschreibung
  Hiermit können Sie festlegen, ob Websites überprüfen können, ob der Benutzer Zahlungsmethoden gespeichert hat.

Wenn Sie diese Richtlinie deaktivieren, werden Websites, die die PaymentRequest.canMakePayment- oder PaymentRequest.hasEnrolledInstrument-API verwenden, informiert, dass keine Zahlungsmethoden verfügbar sind.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Websites überprüfen, ob der Benutzer Zahlungsmethoden gespeichert hat.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PaymentMethodQueryEnabled
  - Gruppenrichtlinienname: Abfragemöglichkeiten für verfügbare Zahlungsmethoden durch Websites zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: PaymentMethodQueryEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: PaymentMethodQueryEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PersonalizationReportingEnabled
  #### Personalisierung von Anzeigen, Suche und News zulassen, indem Sie den Browserverlauf an Microsoft senden
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 80 oder höher

  #### Beschreibung
  Mit dieser Richtlinie wird verhindert, dass Microsoft den Browserverlauf des Microsoft Edge-Browsers eines Benutzers erfasst, um Anzeigen, Suche, News und andere Microsoft-Dienste zu personalisieren.

Diese Einstellung ist nur für Benutzer mit einem Microsoft-Konto verfügbar. Sie ist nicht für untergeordnete Konten oder Unternehmenskonten verfügbar.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer die Einstellung nicht ändern oder außer Kraft setzen. Wenn diese Richtlinie aktiviert oder nicht konfiguriert ist, wird für Microsoft Edge standardmäßig die bevorzugte Einstellung des Benutzers verwendet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PersonalizationReportingEnabled
  - Gruppenrichtlinienname: Personalisierung von Anzeigen, Suche und News zulassen, indem Sie den Browserverlauf an Microsoft senden
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: PersonalizationReportingEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: PersonalizationReportingEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PinningWizardAllowed
  #### Assistent für das Anheften an die Taskleiste zulassen
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 80 oder höher

  #### Beschreibung
  Microsoft Edge verwendet den Assistenten für das Anheften an die Taskleiste, um Benutzer beim Anheften vorgeschlagener Websites an die Taskleiste zu unterstützen. Der Assistent für das Anheften an die Taskleiste ist standardmäßig aktiviert und kann vom Benutzer über das Menü „Einstellungen und mehr“ aufgerufen werden.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer den Assistenten für das Anheften an die Taskleiste über das Menü „Einstellungen und mehr“ aufrufen. Darüber hinaus kann der Assistent per Protokollstart aufgerufen werden.

Wenn Sie diese Richtlinie deaktivieren, ist der Assistent für das Anheften an die Taskleiste im Menü deaktiviert und kann auch nicht per Protokollstart aufgerufen werden.

Es stehen keine Benutzereinstellungen zum Aktivieren/Deaktivieren des Assistenten für das Anheften an die Taskleiste zur Verfügung.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PinningWizardAllowed
  - Gruppenrichtlinienname: Assistent für das Anheften an die Taskleiste zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: PinningWizardAllowed
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ProactiveAuthEnabled
  #### Proaktive Authentifizierung aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Hiermit können Sie konfigurieren, ob die proaktive Authentifizierung aktiviert werden soll.

Wenn sie diese Richtlinie aktivieren, versucht Microsoft Edge, den angemeldeten Benutzer proaktiv mit Microsoft-Diensten zu authentifizieren. Microsoft Edge sucht in regelmäßigen Abständen mit einem Onlinedienst ein aktualisiertes Manifest, das die Konfiguration enthält, in der die Vorgehensweise geregelt wird.

Wenn sie diese Richtlinie deaktivieren, versucht Microsoft Edge nicht, den angemeldeten Benutzer proaktiv mit Microsoft-Diensten zu authentifizieren. Microsoft Edge sucht dann nicht mehr mit einem Onlinedienst nach einem aktualisierten Manifest, das die entsprechende Konfiguration enthält.

Wenn Sie diese Richtlinie nicht konfigurieren, ist die proaktive Authentifizierung aktiviert.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ProactiveAuthEnabled
  - Gruppenrichtlinienname: Proaktive Authentifizierung aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ProactiveAuthEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ProactiveAuthEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PromotionalTabsEnabled
  #### Tabfüllende Werbeinhalte ermöglichen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Steuert die Darstellung von Werbe- oder informativen Inhalten für vollständige Tabs. Mit dieser Einstellung wird die Darstellung von Willkommensseiten gesteuert, über die Benutzer sich bei Microsoft Edge anmelden, den Standardbrowser auswählen oder Informationen zu Produktfeatures erhalten.

Wenn sie diese Richtlinie aktivieren (auf "wahr" festlegen) oder nicht konfigurieren, kann Microsoft Edge Benutzern vollständige Tabinhalte anzeigen, um Produktinformationen bereitzustellen.

Wenn Sie diese Richtlinie deaktivieren (auf "false" festlegen), kann Microsoft Edge keine vollständigen Tabinhalte für Benutzer anzeigen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PromotionalTabsEnabled
  - Gruppenrichtlinienname: Tabfüllende Werbeinhalte ermöglichen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: PromotionalTabsEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: PromotionalTabsEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### PromptForDownloadLocation
  #### Fragen, wo heruntergeladene Dateien gespeichert werden sollen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Legen Sie fest, ob vor dem Herunterladen gefragt wird, wo eine Datei gespeichert werden soll.

Wenn Sie diese Richtlinie aktivieren, wird der Benutzer vor dem Herunterladen gefragt, wo jede einzelne Datei gespeichert werden soll. Wenn Sie dies nicht konfigurieren, werden die Dateien automatisch am Standardspeicherort gespeichert, ohne dass der Benutzer gefragt wird.

Wenn Sie diese Richtlinie nicht konfigurieren, kann der Benutzer diese Einstellung ändern.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: PromptForDownloadLocation
  - Gruppenrichtlinienname: Fragen, wo heruntergeladene Dateien gespeichert werden sollen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: PromptForDownloadLocation
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: PromptForDownloadLocation
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### QuicAllowed
  #### QUIC-Protokoll zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Ermöglicht die Verwendung des QUIC-Protokolls in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, wird das QUIC-Protokoll zugelassen.

Wenn Sie diese Richtlinie deaktivieren, wird das QUIC-Protokoll blockiert.

QUIC ist ein Transportschicht-Netzwerkprotokoll, das die Leistung von Webanwendungen verbessern kann, die derzeit TCP verwenden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: QuicAllowed
  - Gruppenrichtlinienname: QUIC-Protokoll zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: QuicAllowed
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: QuicAllowed
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### RelaunchNotification
  #### Einen Benutzer benachrichtigen, dass ein Neustart des Browsers für ausstehende Updates empfohlen wird oder erforderlich ist
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Mit dieser Richtlinie benachrichtigen Sie Benutzer darüber, dass sie Microsoft Edge neu starten müssen, um ein ausstehendes Update vorzunehmen.

Wenn Sie diese Richtlinie nicht konfigurieren, fügt Microsoft Edge ein Wiederherstellungssymbol ganz rechts in der oberen Menüleiste ein, um den Benutzer aufzufordern, den Browser neu zu starten, damit das Update vorgenommen werden kann.

Wenn Sie diese Richtlinie aktivieren und auf “Recommended“ einstellen, werden die Benutzer durch eine wiederkehrende Warnung zu einem Neustart aufgefordert. Benutzer können diese Warnung ablehnen und den Neustart verschieben.

Wenn Sie die Richtlinie auf “Required” festlegen, informiert eine wiederkehrende Warnung die Benutzer darüber, dass der Browser automatisch neu gestartet wird, sobald der Benachrichtigungszeitraum abgelaufen ist. Der Standardzeitraum beträgt sieben Tage. Sie können diesen Zeitraum mithilfe der Richtlinie “[RelaunchNotificationPeriod](#relaunchnotificationperiod)” konfigurieren.

Die Sitzung des Benutzers wird beim Neustart des Browsers wiederhergestellt.

Zuordnung der Richtlinienoptionen:

* Recommended (1) = Empfohlen: Dem Benutzer eine wiederkehrende Eingabeaufforderung mit dem Hinweis anzeigen, dass ein Neustart empfohlen wird

* Required (2) = Erforderlich: Dem Benutzer eine wiederkehrende Eingabeaufforderung anzeigen, die angibt, dass ein Neustart erforderlich ist

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: RelaunchNotification
  - Gruppenrichtlinienname: Einen Benutzer benachrichtigen, dass ein Neustart des Browsers für ausstehende Updates empfohlen wird oder erforderlich ist
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: RelaunchNotification
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: RelaunchNotification
  - Beispielwert:
``` xml
<integer>1</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### RelaunchNotificationPeriod
  #### Zeitraum für Aktualisierungsbenachrichtigungen festlegen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Ermöglicht es Ihnen, einen Zeitraum in Millisekunden festzulegen, über den Benutzer benachrichtigt werden, dass Microsoft Edge neu gestartet werden muss, um eine ausstehende Aktualisierung anzuwenden.

Über diesen Zeitraum wird der Benutzer wiederholt informiert, dass eine Aktualisierung erforderlich ist. In Microsoft Edge wird das App-Menü geändert, um anzuzeigen, dass ein Neustart erforderlich ist, sobald ein Drittel des Benachrichtigungszeitraums abgelaufen ist. Diese Benachrichtigung ändert die Farbe, sobald zwei Drittel des Benachrichtigungszeitraums abgelaufen sind, und erneut, wenn der gesamte Benachrichtigungszeitraum abgelaufen ist. Die zusätzlichen Benachrichtigungen, die durch die [RelaunchNotification](#relaunchnotification)-Richtlinie aktiviert sind, folgen diesem Zeitplan.

Wenn nicht festgelegt, wird ein Standardzeitraum von 604800000 Millisekunden (eine Woche) verwendet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: RelaunchNotificationPeriod
  - Gruppenrichtlinienname: Zeitraum für Aktualisierungsbenachrichtigungen festlegen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: RelaunchNotificationPeriod
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x240c8400
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: RelaunchNotificationPeriod
  - Beispielwert:
``` xml
<integer>604800000</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### RendererCodeIntegrityEnabled
  #### Renderercodeintegrität aktivieren
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 78 oder höher

  #### Beschreibung
  Wenn diese Richtlinie aktiviert oder nicht definiert ist, wird die Renderercodeintegrität aktiviert. Diese Richtlinie sollte nur deaktiviert werden, wenn Kompatibilitätsprobleme mit Software von Drittanbietern auftreten, die innerhalb der Rendererprozesse von Microsoft Edge ausgeführt werden.

Das Deaktivieren dieser Richtlinie hat nachteilige Auswirkungen auf die Sicherheit und Stabilität von Microsoft Edge, da unbekannter und potentiell schädlicher Code innerhalb der Rendererprozesse von Microsoft Edge geladen werden kann.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: RendererCodeIntegrityEnabled
  - Gruppenrichtlinienname: Renderercodeintegrität aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: RendererCodeIntegrityEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### RequireOnlineRevocationChecksForLocalAnchors
  #### Geben Sie an, ob für lokale Vertrauensanker Online-OCSP/CRL-Überprüfungen erforderlich sind.
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 77 oder höher

  #### Beschreibung
  Steuern Sie, ob Online Sperrüberprüfungen (OCSP/Zertifikatsperrlisten-Überprüfungen) erforderlich sind. Wenn Microsoft Edge keine Sperrstatusinformationen erhalten kann, werden diese Zertifikate als gesperrt behandelt ("harter Fehler").

Wenn Sie diese Richtlinie aktivieren, führt Microsoft Edge immer eine Sperrüberprüfung für Serverzertifikate durch, die erfolgreich überprüft werden und durch lokal installierte Zertifizierungsstellenzertifikate signiert sind.

Wenn Sie diese Richtlinie nicht konfigurieren oder deaktivieren, verwendet Microsoft Edge die vorhandenen Einstellungen für die Online-Sperrüberprüfung.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: RequireOnlineRevocationChecksForLocalAnchors
  - Gruppenrichtlinienname: Geben Sie an, ob für lokale Vertrauensanker Online-OCSP/CRL-Überprüfungen erforderlich sind.
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: RequireOnlineRevocationChecksForLocalAnchors
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ResolveNavigationErrorsUseWebService
  #### Auflösung von Navigationsfehlern mithilfe eines Webdienstes aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Erlaubt Microsoft Edge, eine datenlose Verbindung zu einem Webservice herzustellen, um Netzwerke auf Konnektivität zu prüfen, beispielsweise die WLAN-Verbindung in Hotels und Flughäfen.

Wenn Sie diese Richtlinie aktivieren, wird ein Webservice für Tests der Netzwerkverbindung verwendet.

Wenn Sie diese Richtlinie deaktivieren, verwendet Microsoft Edge native APIs, um Probleme mit der Netzwerkverbindung und der Navigation zu beheben.

**Hinweis**: Mit Ausnahme von Windows 8 und späteren Versionen von Windows verwendet Microsoft Edge *immer* native APIs, um Verbindungsprobleme zu lösen.

Wenn Sie diese Richtlinie nicht konfigurieren, verwendet Microsoft Edge die Benutzereinstellung, die für Dienste unter edge://settings/privacy festgelegt ist.
Es gibt einen **Einen Webservice verwenden, um Navigationsfehler zu beheben**-Schalter, den der Benutzer ein- und ausschalten kann. Beachten Sie: Wenn Sie diese Richtlinie (ResolveNavigationErrorsUseWebService) aktiviert haben, ist die Einstellung **Einen Webservice verwenden, um Navigationsfehler zu beheben** aktiviert, aber der Benutzer kann die Einstellung nicht mit Hilfe des Umschalters ändern. Wenn Sie diese Richtlinie deaktiviert haben, wird die Einstellung **Einen Webservice verwenden, um Navigationsfehler zu beheben** deaktiviert, und der Benutzer kann die Einstellung nicht mit dem Umschalter ändern.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ResolveNavigationErrorsUseWebService
  - Gruppenrichtlinienname: Auflösung von Navigationsfehlern mithilfe eines Webdienstes aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: ResolveNavigationErrorsUseWebService
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ResolveNavigationErrorsUseWebService
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### RestrictSigninToPattern
  #### Beschränken der Konten, die als primäre Microsoft Edge-Konten verwendet werden können
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Mit dieser Richtlinie legen Sie fest, welche Konten in Microsoft Edge als primäre Browserkonten festgelegt werden können (das Konto, das während des Synchronisierungs-Opt-in-Flows ausgewählt wird).

Wenn ein Benutzer versucht, ein primäres Browserkonto mit einem Benutzernamen zu konfigurieren, der diesem Muster nicht entspricht, wird er blockiert und erhält eine entsprechende Fehlermeldung. Sie können diese Richtlinie so konfigurieren, dass Sie mehreren Konten entspricht. Verwenden Sie dazu einen regulären Ausdruck im Perl-Stil für das Muster. Beachten Sie, dass bei Musterübereinstimmungen zwischen Groß-/Kleinschreibung unterschieden wird. Weitere Informationen zu den Regeln für reguläre Ausdrücke, die verwendet werden können finden Sie unter https://go.Microsoft.com/fwlink/p/?linkid=2133903.

Wenn Sie diese Richtlinie nicht konfigurieren oder leer lassen, können Benutzer jedes Konto in Microsoft Edgeals primäres Browserkonto festlegen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: RestrictSigninToPattern
  - Gruppenrichtlinienname: Beschränken der Konten, die als primäre Microsoft Edge-Konten verwendet werden können
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: RestrictSigninToPattern
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
".*@contoso.com"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: RestrictSigninToPattern
  - Beispielwert:
``` xml
<string>.*@contoso.com</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### RoamingProfileLocation
  #### Roamingprofilverzeichnis festlegen
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 85 oder höher

  #### Beschreibung
  Konfiguriert das Verzeichnis, das zum Speichern der Roaming-Kopie von Profilen verwendet werden soll.

Wenn sie diese Richtlinie aktivieren, verwendet Microsoft Edge das angegebene Verzeichnis zum Speichern einer Roaming-Kopie der Profile, sofern Sie auch die Richtlinie "[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)" aktiviert haben. Wenn Sie die Richtlinie "[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)" deaktivieren oder nicht konfigurieren, wird der in dieser Richtlinie gespeicherte Wert nicht verwendet.

Eine Liste der Variablen, die Sie verwenden können, finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

Wenn Sie diese Richtlinie nicht konfigurieren, wird der standardmäßige Pfad des Roaming-Profils verwendet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: RoamingProfileLocation
  - Gruppenrichtlinienname: Roamingprofilverzeichnis festlegen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: RoamingProfileLocation
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"${roaming_app_data}\\edge-profile"
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### RoamingProfileSupportEnabled
  #### Verwendung von Roamingkopien für Microsoft Edge-Profildaten ermöglichen
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 85 oder höher

  #### Beschreibung
  Aktivieren Sie diese Richtlinie, um Roamingprofile für Windows zu verwenden. Die in Microsoft Edge-Profilen gespeicherten Einstellungen (Favoriten und Einstellungen) werden auch in einer Datei im Benutzerprofilordner „Roaming“ gespeichert (oder an dem Speicherort, den der Administrator mithilfe der Richtlinie [RoamingProfileLocation](#roamingprofilelocation) angegeben hat).

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, werden nur die regulären lokalen Profile verwendet.

Die Richtlinie [SyncDisabled](#syncdisabled) deaktiviert die gesamte Datensynchronisierung und setzt diese Richtlinie außer Kraft.

Weitere Informationen zur Verwendung von Roamingbenutzerprofilen finden Sie unter https://docs.microsoft.com/windows-server/storage/folder-redirection/deploy-roaming-user-profiles.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: RoamingProfileSupportEnabled
  - Gruppenrichtlinienname: Verwendung von Roamingkopien für Microsoft Edge-Profildaten ermöglichen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: RoamingProfileSupportEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### RunAllFlashInAllowMode
  #### Adobe Flash-Inhaltseinstellung auf alle Inhalte erweitern
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Wenn Sie diese Richtlinie aktivieren, werden alle Adobe Flash-Inhalte ausgeführt, die in Websites eingebettet sind, deren Inhaltseinstellungen (vom Benutzer oder über eine Unternehmensrichtlinie festgelegt)Adobe Flash zulassen. Dazu gehören auch Inhalte anderer Herkunft und/oder kleine Inhalte.

Informationen darüber, wie Sie steuern können, welche Websites Adobe Flash ausführen dürfen, finden Sie in den Spezifikationen der Richtlinien [DefaultPluginsSetting](#defaultpluginssetting), [PluginsAllowedForUrls](#pluginsallowedforurls) und [PluginsBlockedForUrls](#pluginsblockedforurls).

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, können Adobe Flash-Inhalte aus anderen Quellen (von Websites, die nicht in den drei oben genannten Richtlinien aufgeführt sind) oder kleine Inhalte blockiert werden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: RunAllFlashInAllowMode
  - Gruppenrichtlinienname: Adobe Flash-Inhaltseinstellung auf alle Inhalte erweitern
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: RunAllFlashInAllowMode
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: RunAllFlashInAllowMode
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SSLErrorOverrideAllowed
  #### Zulassen, dass Benutzer von der HTTPS-Warnungsseite aus fortfahren können
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Microsoft Edge zeigt eine Warnungsseite an, wenn Benutzer Websites mit SSL-Fehlern besuchen.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren (Standardeinstellung), können Benutzer durch diese Warnungsseiten klicken.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer sich nicht durch eine Warnungsseite klicken.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SSLErrorOverrideAllowed
  - Gruppenrichtlinienname: Zulassen, dass Benutzer von der HTTPS-Warnungsseite aus fortfahren können
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: SSLErrorOverrideAllowed
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SSLErrorOverrideAllowed
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SSLVersionMin
  #### Mindestversion von TLS aktiviert
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Legt die minimale unterstützte SSL-Version fest. Wenn Sie diese Richtlinie nicht konfigurieren, verwendet Microsoft Edge die standardmäßige Minimalversion TLS 1.0.

Wenn Sie diese Richtlinie aktivieren, können Sie die minimale Version auf einen der folgenden Werte festlegen: “TLSv1“, “TLSv1.1“ oder “TLSv1.2“. Wenn festgelegt, verwendet Microsoft Edge keine SSL/TLS-Version, die niedriger als die angegebene Version ist. Unbekannte Werte werden ignoriert.

Zuordnung der Richtlinienoptionen:

* TLSv1 (tls1) = TLS 1.0

* TLSv1.1 (tls1.1) = TLS 1.1

* TLSv1.2 (tls1.2) = TLS 1.2

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SSLVersionMin
  - Gruppenrichtlinienname: Mindestversion von TLS aktiviert
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: SSLVersionMin
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"tls1"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SSLVersionMin
  - Beispielwert:
``` xml
<string>tls1</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SaveCookiesOnExit
  #### Speichern von Cookies beim Schließen von Microsoft Edge
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 86 oder höher

  #### Beschreibung
  Wenn diese Richtlinie aktiviert ist, wird die angegebene Gruppe von Cookies beim Schließen des Browsers vom Löschvorgang ausgeschlossen. Diese Richtlinie wird nur wirksam, wenn:
–die Umschaltfläche "Cookies und andere Websitedaten" unter “Einstellungen/Datenschutz” und “Dienste/Löschen der Browserdaten beim Schließen” konfiguriert sind
  – die Richtlinie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) aktiviert ist, oder
 – die Richtlinie [DefaultCookiesSetting](#defaultcookiessetting) auf “Cookies für die Dauer der Sitzung beibehalten” konfiguriert ist.

 Sie können Sie eine Liste von Websites, die auf  URL-Mustern basiert, definieren, die Ihre Cookies über Sitzungen hinaus beibehalten.

 Hinweis: Benutzer können die Cookie-Übersicht weiterhin bearbeiten, um URLs hinzuzufügen oder zu entfernen. Sie können jedoch keine URLs entfernen, die von einem Administrator hinzugefügt wurden.

 Wenn Sie diese Richtlinie aktivieren, wird die Liste der Cookies nicht gelöscht, wenn der Browser geschlossen wird.

 Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird die persönliche Konfiguration des Benutzers verwendet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SaveCookiesOnExit
  - Gruppenrichtlinienname: Speichern von Cookies beim Schließen von Microsoft Edge
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SaveCookiesOnExit
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SavingBrowserHistoryDisabled
  #### Speichern des Browserverlaufs deaktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Deaktiviert das Speichern des Browserverlaufs und verhindert, dass Benutzer diese Einstellung ändern.

Wenn Sie diese Richtlinie aktivieren, wird der Browserverlauf nicht gespeichert, und auch die Tabsynchronisierung wird deaktiviert.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird der Browserverlauf gespeichert.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SavingBrowserHistoryDisabled
  - Gruppenrichtlinienname: Speichern des Browserverlaufs deaktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: SavingBrowserHistoryDisabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SavingBrowserHistoryDisabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ScreenCaptureAllowed
  #### Screenshots zulassen oder verweigern
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 83 oder höher

  #### Beschreibung
  Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, kann eine Webseite Bildschirmübertragungs-APIs (z. B. getDisplayMedia() oder die Desktoperfassungserweiterungs-API) für einen Screenshot verwenden.
Wenn Sie diese Richtlinie deaktivieren, schlagen Aufrufe von Bildschirmübertragungs-APIs fehl. Wenn Sie z. B. eine webbasierte Onlinebesprechung verwenden, funktioniert das Teilen von Videos oder die Bildschirmübertragung nicht.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ScreenCaptureAllowed
  - Gruppenrichtlinienname: Screenshots zulassen oder verweigern
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ScreenCaptureAllowed
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ScreenCaptureAllowed
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ScrollToTextFragmentEnabled
  #### Scrollen zu dem in URL-Fragmenten angegebenen Text aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 83 oder höher

  #### Beschreibung
  Dieses Feature erlaubt Link- und Adressleisten-URL-Navigationen, spezifischen Text auf einer Webseite zu adressieren, der nach dem Laden der Webseite gescrollt wird.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, wird das Scrollen auf Webseiten zu bestimmten Textstellen mithilfe einer URL aktiviert.

Wenn Sie diese Richtlinie deaktivieren, wird das Scrollen auf Webseiten zu bestimmten Textstellen mithilfe einer URL deaktiviert.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ScrollToTextFragmentEnabled
  - Gruppenrichtlinienname: Scrollen zu dem in URL-Fragmenten angegebenen Text aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ScrollToTextFragmentEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ScrollToTextFragmentEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SearchSuggestEnabled
  #### Suchvorschläge aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Aktiviert Websuchvorschläge auf der Adressleiste und in der Liste mit automatischen Vorschlägen von Microsoft Edge und verhindert, dass Benutzer diese Richtlinie ändern.

Wenn Sie diese Richtlinie aktivieren, werden Websuchvorschläge verwendet.

Wenn Sie diese Richtlinie deaktivieren, werden keine Websuchvorschläge verwendet. Vorschläge aus dem lokalen Verlauf und aus den lokalen Favoriten werden jedoch weiterhin angezeigt. Außerdem werden weder die eingegebenen Zeichen noch die besuchten URLs in die an Microsoft übermittelten Telemetriedaten eingeschlossen.

Wenn Sie diese Richtlinie nicht festlegen, sind Suchvorschläge aktiviert. Dies kann jedoch vom Benutzer geändert werden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SearchSuggestEnabled
  - Gruppenrichtlinienname: Suchvorschläge aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: SearchSuggestEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SearchSuggestEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SecurityKeyPermitAttestation
  #### Websites oder Domänen, die keine Berechtigung zur Verwendung des direkten Sicherheitsschlüssel-Nachweises benötigen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt Websites und Domänen an, die keine explizite Benutzerberechtigung benötigen, wenn Nachweiszertifikate von Sicherheitsschlüsseln angefordert werden. Zusätzlich wird ein Signal an den Sicherheitsschlüssel gesendet, das angibt, dass es einen individuellen Nachweis verwenden kann. Ohne dies werden Benutzer jedes Mal aufgefordert, wenn eine Website Nachweise für Sicherheitsschlüssel anfordert.

Websites (z. B. https://contoso.com/some/path) stimmen nur als U2F-appIDs überein. Domänen (z. B. contoso.com) stimmen nur mit den webauthn-RP-IDs überein. Sie müssen sowohl die appID-URL als auch die Domäne auflisten, um U2F- und webauthn-APIs für eine bestimmte Website zu erfassen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SecurityKeyPermitAttestation
  - Gruppenrichtlinienname: Websites oder Domänen, die keine Berechtigung zur Verwendung des direkten Sicherheitsschlüssel-Nachweises benötigen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation\1 = "https://contoso.com"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SecurityKeyPermitAttestation
  - Beispielwert:
``` xml
<array>
  <string>https://contoso.com</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SendIntranetToInternetExplorer
  #### Alle Intranetsites an Internet Explorer senden
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 77 oder höher

  #### Beschreibung
  Anleitungen zum Konfigurieren der optimalen Benutzeroberfläche für den Internet Explorer-Modus finden Sie unter "[https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)".

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SendIntranetToInternetExplorer
  - Gruppenrichtlinienname: Alle Intranetsites an Internet Explorer senden
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: SendIntranetToInternetExplorer
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SendSiteInfoToImproveServices
  #### Websiteinformationen zur Verbesserung von Microsoft-Diensten senden (veraltet)
  >VERALTET: Diese Richtlinie ist veraltet. Sie wird gegenwärtig noch unterstützt, aber in einem zukünftigen Release ausgemustert.
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Diese Richtlinie ist veraltet. Sie wird im Augenblick noch unterstützt, ist in Microsoft Edge 89 aber veraltet. Sie wird durch eine neue Richtlinie ersetzt:  [DiagnosticData](#diagnosticdata) für Windows 7, Windows 8 und macOS. Auf Windows 10 wird sie durch “Telemetrie zulassen” ersetzt ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

Diese Richtlinie ermöglicht das Senden von Informationen über in Microsoft Edge besuchte Websites an Microsoft, um Dienste wie die Suche zu verbessern.

Aktivieren Sie diese Richtlinie, um Informationen über in Microsoft Edge besuchte Websites an Microsoft zu senden. Deaktivieren Sie diese Richtlinie, um Informationen über in Microsoft Edge besuchte Websites nicht an Microsoft zu senden. In beiden Fällen kann die Einstellung nicht vom Benutzer geändert oder überschrieben werden.

Unter Windows 10 gilt: Wenn Sie diese Richtlinie nicht konfigurieren, verwendet Microsoft Edge standardmäßig die Einstellung für Windows-Diagnosedaten. Wenn Sie diese Richtlinie aktivieren, sendet Microsoft Edge nur dann Informationen über in Microsoft Edge besuchte Websites, wenn die Einstellung für Windows-Diagnosedaten auf “Vollständig“ festgelegt ist. Wenn Sie diese Richtlinie deaktivieren, sendet Microsoft Edge keine Informationen über besuchte Websites. Weitere Informationen zu Einstellungen für Windows-Diagnosedaten finden Sie hier: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

Unter Windows 7, Windows 8 und macOS gilt: Diese Richtlinie steuert das Senden von Informationen über besuchte Websites. Wenn Sie diese Richtlinie nicht konfigurieren, verwendet Microsoft Edge standardmäßig die Einstellung des Benutzers.

Um diese Richtlinie zu aktivieren, muss [MetricsReportingEnabled](#metricsreportingenabled) auf “Aktiviert” festgelegt werden. Wenn [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) oder [MetricsReportingEnabled](#metricsreportingenabled) nicht konfiguriert oder deaktiviert sind, werden keine Daten an Microsoft gesendet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SendSiteInfoToImproveServices
  - Gruppenrichtlinienname: Websiteinformationen zur Verbesserung von Microsoft-Diensten senden (veraltet)
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: SendSiteInfoToImproveServices
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SendSiteInfoToImproveServices
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SensorsAllowedForUrls
  #### Zugriff auf Sensoren auf bestimmten Websites zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 86 oder höher

  #### Beschreibung
  Define a list of sites, based on URL patterns, that can access and use sensors such as motion and light sensors.

If you don't configure this policy, the global default value from the [DefaultSensorsSetting](#defaultsensorssetting) policy (if set) or the user's personal configuration is used for all sites.

For URL patterns that don't match this policy, the following order of precedence is used: The [SensorsBlockedForUrls](#sensorsblockedforurls) policy (if there is a match), the [DefaultSensorsSetting](#defaultsensorssetting) policy (if set), or the user's personal settings.

The URL patterns defined in this policy can't conflict with those configured in the [SensorsBlockedForUrls](#sensorsblockedforurls) policy. You can't allow and block a URL.

For detailed information about valid URL patterns, please see [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SensorsAllowedForUrls
  - Gruppenrichtlinienname: Zugriff auf Sensoren auf bestimmten Websites zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SensorsAllowedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SensorsBlockedForUrls
  #### Zugriff auf Sensoren auf bestimmten Websites blockieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 86 oder höher

  #### Beschreibung
  Define a list of sites, based on URL patterns, that can't access sensors such as motion and light sensors.

If you don't configure this policy, the global default value from the [DefaultSensorsSetting](#defaultsensorssetting) policy (if set) or the user's personal configuration is used for all sites.

For URL patterns that don't match this policy, the following order of precedence is used: The [SensorsAllowedForUrls](#sensorsallowedforurls) policy (if there is a match), the [DefaultSensorsSetting](#defaultsensorssetting) policy (if set), or the user's personal settings.

The URL patterns defined in this policy can't conflict with those configured in the [SensorsAllowedForUrls](#sensorsallowedforurls) policy. You can't allow and block a URL.

For detailed information about valid URL patterns, please see [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SensorsBlockedForUrls
  - Gruppenrichtlinienname: Zugriff auf Sensoren auf bestimmten Websites blockieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SensorsBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SerialAskForUrls
  #### Die serielle API auf bestimmten Websites zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 86 oder höher

  #### Beschreibung
  Definiert eine auf URL-Mustern basierende Liste mit Websites, die vom Benutzer Zugriff auf einen seriellen Anschluss erbitten können.

Wenn Sie diese Richtlinie nicht konfigurieren, wird für alle Websites der globale Standardwert aus der Richtlinie [DefaultSerialGuardSetting](#defaultserialguardsetting) (falls festgelegt) oder die persönliche Konfiguration des Benutzers verwendet.

Für URL-Muster, die nicht mit dieser Richtlinie übereinstimmen, wird die Prioritätsreihenfolge verwendet: Richtlinie [SerialBlockedForUrls](#serialblockedforurls) (falls eine Übereinstimmung besteht), Richtlinie [DefaultSerialGuardSetting](#defaultserialguardsetting) (falls festgelegt) oder die persönlichen Einstellungen des Benutzers.

Die in dieser Richtlinie definierten URL-Muster dürfen nicht mit denen in der Richtlinie [SerialBlockedForUrls](#serialblockedforurls) konfigurierten in Konflikt stehen. Sie können eine URL nicht gleichzeitig zulassen und blockieren.

Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SerialAskForUrls
  - Gruppenrichtlinienname: Die serielle API auf bestimmten Websites zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SerialAskForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SerialBlockedForUrls
  #### Die serielle API auf bestimmten Websites blockieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 86 oder höher

  #### Beschreibung
  Definiert eine auf URL-Mustern basierende Liste mit Websites, die vom Benutzer keinen Zugriff auf einen seriellen Anschluss erbitten können.

Wenn Sie diese Richtlinie nicht konfigurieren, wird für alle Websites der globale Standardwert aus der Richtlinie [DefaultSerialGuardSetting](#defaultserialguardsetting) (falls festgelegt) oder die persönliche Konfiguration des Benutzers verwendet.

Für URL-Muster, die nicht mit dieser Richtlinie übereinstimmen, wird die Prioritätsreihenfolge verwendet: Richtlinie [SerialAskForUrls](#serialaskforurls) (falls eine Übereinstimmung besteht), Richtlinie [DefaultSerialGuardSetting](#defaultserialguardsetting) (falls festgelegt) oder die persönlichen Einstellungen des Benutzers.

Die URL-Muster in dieser Richtlinie dürfen nicht mit denen in der Richtlinie [SerialAskForUrls](#serialaskforurls) konfigurierten in Konflikt stehen. Sie können eine URL nicht gleichzeitig zulassen und blockieren.

Ausführliche Informationen zu gültigen URL-Mustern finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SerialBlockedForUrls
  - Gruppenrichtlinienname: Die serielle API auf bestimmten Websites blockieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SerialBlockedForUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### ShowOfficeShortcutInFavoritesBar
  #### Microsoft Office-Verknüpfung in der Favoritenleiste anzeigen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Gibt an, ob in der Favoritenleiste eine Verknüpfung mit Office.com eingefügt werden soll. Benutzer, die bei Microsoft Edge angemeldet sind, werden von der Verknüpfung zu ihren Microsoft Office-Apps und -Dokumenten weitergeleitet.

Wenn diese Richtlinie aktiviert oder nicht konfiguriert ist, können Benutzer im Kontextmenü der Favoritenleiste wählen, ob die Verknüpfung angezeigt werden soll.

Wenn die Richtlinie deaktiviert ist, wird die Verknüpfung nicht angezeigt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: ShowOfficeShortcutInFavoritesBar
  - Gruppenrichtlinienname: Microsoft Office-Verknüpfung in der Favoritenleiste anzeigen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: ShowOfficeShortcutInFavoritesBar
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: ShowOfficeShortcutInFavoritesBar
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SignedHTTPExchangeEnabled
  #### Unterstützung des signierten HTTP-Austauschs (SXG) aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 78 oder höher

  #### Beschreibung
  Aktivieren Sie die Unterstützung für Signed HTTP Exchange (SXG).

Wenn diese Richtlinie nicht festgelegt oder aktiviert ist, akzeptiert Microsoft Edge Webinhalte, die als Signed HTTP Exchanges bereitgestellt werden.

Wenn diese Richtlinie deaktiviert ist, können Signed HTTP Exchanges nicht geladen werden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SignedHTTPExchangeEnabled
  - Gruppenrichtlinienname: Unterstützung des signierten HTTP-Austauschs (SXG) aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: SignedHTTPExchangeEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SignedHTTPExchangeEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SitePerProcess
  #### Websiteisolation für jede Website aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Die Richtlinie ”SitePerProcess” kann verwendet werden, um zu verhindern, dass Benutzer das Standardverhalten der Isolierung aller Sites deaktivieren. Beachten Sie, dass Sie auch die Richtlinie “[IsolateOrigins](#isolateorigins)” verwenden können, um zusätzliche, differenziertere Ursprünge zu isolieren.
Wenn Sie diese Richtlinie aktivieren, können Benutzer das Standardverhalten, bei dem jede Website in ihrem eigenen Prozess ausgeführt wird, nicht abwählen.
Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, kann ein Benutzer die Isolierung der Website deaktivieren. (zum Beispiel durch Verwendung des Eintrags "Website-Isolierung deaktivieren" in edge://flags). Das Deaktivieren oder Nichtkonfigurieren der Richtlinie schaltet die Website-Isolierung nicht aus.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SitePerProcess
  - Gruppenrichtlinienname: Websiteisolation für jede Website aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: SitePerProcess
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SitePerProcess
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SpellcheckEnabled
  #### Rechtschreibprüfung aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, kann der Benutzer die Rechtschreibprüfung verwenden.

Wenn Sie diese Richtlinie deaktivieren, kann der Benutzer die Rechtschreibprüfung nicht verwenden und die Richtlinien [SpellcheckLanguage](#spellchecklanguage) und [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) sind ebenfalls deaktiviert.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SpellcheckEnabled
  - Gruppenrichtlinienname: Rechtschreibprüfung aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: SpellcheckEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SpellcheckEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SpellcheckLanguage
  #### Spezifische Sprachen für die Rechtschreibprüfung aktivieren
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 77 oder höher

  #### Beschreibung
  Aktiviert verschiedene Sprachen für die Rechtschreibprüfung. Jede angegebene Sprache, die nicht erkannt wird, wird ignoriert.

Wenn Sie diese Richtlinie aktivieren, wird die Rechtschreibprüfung für die angegebenen Sprachen aktiviert sowie für alle Sprachen, die der Benutzer aktiviert hat.

Wenn Sie diese Richtlinie nicht konfigurieren oder deaktivieren, werden die Einstellungen des Benutzers für die Rechtschreibprüfung nicht geändert.

Wenn die Richtlinie [SpellcheckEnabled](#spellcheckenabled) deaktiviert ist, hat diese Richtlinie keine Wirkung.

Wenn eine Sprache sowohl in der Richtlinie SpellcheckLanguage' als auch in der Richtlinie [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) angegeben ist, wird die Sprache der Rechtschreibprüfung aktiviert.

Die unterstützten Sprachen sind: af, bg, ca, cs, cy, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SpellcheckLanguage
  - Gruppenrichtlinienname: Spezifische Sprachen für die Rechtschreibprüfung aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\2 = "es"

```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SpellcheckLanguageBlocklist
  #### Deaktivierung von Sprachen für die Rechtschreibprüfung erzwingen
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 78 oder höher

  #### Beschreibung
  Deaktiviert zwangsweise die Rechtschreibprüfung für Sprachen. Nicht erkannte Sprachen in dieser Liste werden ignoriert.

Wenn Sie diese Richtlinie aktivieren, wird die Rechtschreibprüfung für die angegebenen Sprachen deaktiviert. Der Benutzer kann die Rechtschreibprüfung für Sprachen, die nicht in der Liste enthalten sind, weiterhin aktivieren oder deaktivieren.

Wenn Sie diese Richtlinie nicht festlegen oder deaktivieren, ändert sich nichts an den Einstellungen des Benutzers für die Rechtschreibprüfung.

Wenn die Richtlinie [SpellcheckEnabled](#spellcheckenabled) deaktiviert ist, hat diese Richtlinie keine Wirkung.

Wenn eine Sprache sowohl in der Richtlinie [SpellcheckLanguage](#spellchecklanguage) als auch in der Richtlinie 'SpellcheckLanguageBlocklist' enthalten ist, wird die Rechtschreibprüfung der Sprache aktiviert.

Die derzeit unterstützten Sprachen sind: af, bg, ca, cs, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SpellcheckLanguageBlocklist
  - Gruppenrichtlinienname: Deaktivierung von Sprachen für die Rechtschreibprüfung erzwingen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\2 = "es"

```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### StricterMixedContentTreatmentEnabled
  #### Strengere Behandlung für gemischte Inhalte aktivieren (veraltet)
  >VERALTET: Diese Richtlinie ist veraltet. Sie wird gegenwärtig noch unterstützt, aber in einem zukünftigen Release ausgemustert.
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 81 oder höher

  #### Beschreibung
  Diese Richtlinie ist veraltet, weil sie nur als kurzfristiger Mechanismus gedacht war, um Unternehmen mehr Zeit für die Aktualisierung ihrer Webinhalte zu geben, wenn sich bei ihnen herausstellt, dass eine strengere Behandlung gemischter Inhalte unvereinbar ist. Sie wird in Microsoft Edge Version 85 nicht mehr funktionieren.

Diese Richtlinie steuert die Behandlung gemischter Inhalte (HTTP-Inhalte in HTTPS-Sites) im Browser.

Wenn Sie diese Richtlinie auf "wahr" oder "nicht festgelegt" setzen, werden gemischte Audio- und Videoinhalte automatisch auf HTTPS aktualisiert (d. h. die URL wird als HTTPS ohne Fallback neu geschrieben, wenn die Ressource nicht über HTTPS verfügbar ist), und in der URL-Leiste für gemischte Bildinhalte wird die Warnung "Nicht sicher" angezeigt.

Wenn Sie die Richtlinie auf "falsch" festlegen, werden automatische Upgrades für Audio und Video deaktiviert, und für Bilder wird keine Warnung angezeigt.

Diese Richtlinie wirkt sich außer auf Audio, Video und Bilder nicht auf andere Arten gemischter Inhalte aus.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: StricterMixedContentTreatmentEnabled
  - Gruppenrichtlinienname: Strengere Behandlung für gemischte Inhalte aktivieren (veraltet)
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: StricterMixedContentTreatmentEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: StricterMixedContentTreatmentEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SuppressUnsupportedOSWarning
  #### Nicht unterstützte Betriebssystemwarnung unterdrücken
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Unterdrückt die Warnung, die angezeigt wird, wenn Microsoft Edge auf einem Computer oder Betriebssystem ausgeführt wird, der nicht mehr unterstützt wird.

Wenn diese Richtlinie deaktiviert oder nicht festgelegt ist, werden die Warnungen bei solchen nicht unterstützten Computern oder Betriebssystemen angezeigt.


  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SuppressUnsupportedOSWarning
  - Gruppenrichtlinienname: Nicht unterstützte Betriebssystemwarnung unterdrücken
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: SuppressUnsupportedOSWarning
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SuppressUnsupportedOSWarning
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SyncDisabled
  #### Synchronisierung von Daten mit Microsoft-Synchronisierungsdiensten deaktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Deaktiviert die Datensynchronisierung in Microsoft Edge. Diese Richtlinie verhindert außerdem, dass die Zustimmungsaufforderung für die Synchronisierung angezeigt wird.

Wenn Sie diese Richtlinie nicht festlegen oder nicht wie empfohlen anwenden, können Benutzer die Synchronisierung ein- oder ausschalten. Wenn Sie diese Richtlinie als erforderlich anwenden, können Benutzer die Synchronisierung nicht einschalten.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SyncDisabled
  - Gruppenrichtlinienname: Synchronisierung von Daten mit Microsoft-Synchronisierungsdiensten deaktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: SyncDisabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SyncDisabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### SyncTypesListDisabled
  #### Konfigurieren der Liste der Typen, die von der Synchronisierung ausgeschlossen werden sollen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 83 oder höher

  #### Beschreibung
  Wenn Sie diese Richtlinie aktivieren, werden alle angegebenen Datentypen von der Synchronisierung ausgeschlossen. Diese Richtlinie kann verwendet werden, um die Art der in den Microsoft EdgeSynchronisierungsdienst hochgeladenen Daten einzuschränken.

Sie können einen der folgenden Datentypen für diese Richtlinie bereitstellen: "Favoriten", "Einstellungen", "Kennwörter", "adressesAndMore", "Erweiterungen", "Verlauf" und "Sammlungen". Beachten Sie, dass bei diesen Datentypnamen Groß- und Kleinschreibung beachtet werden muss.

Benutzer können die deaktivierten Datentypen nicht überschreiben.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: SyncTypesListDisabled
  - Gruppenrichtlinienname: Konfigurieren der Liste der Typen, die von der Synchronisierung ausgeschlossen werden sollen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled\1 = "favorites"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: SyncTypesListDisabled
  - Beispielwert:
``` xml
<array>
  <string>favorites</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### TLS13HardeningForLocalAnchorsEnabled
  #### Aktivieren Sie ein TLS 1.3-Sicherheitsfeature für lokale Vertrauensanker. (veraltet)
  
  >VERALTET: Diese Richtlinie ist veraltet und funktioniert nach Microsoft Edge Version 85 nicht mehr.
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 81, bis 85

  #### Beschreibung
  Diese Richtlinie funktioniert nicht, da sie nur als kurzfristiger Mechanismus vorgesehen war, um Unternehmen mehr Zeit für ein Upgrade der betroffenen Proxys zu geben.

Mit dieser Richtlinie wird ein Sicherheitsfeature in TLS 1.3 gesteuert, mit dem Verbindungen vor Downgrade-Angriffen geschützt werden. Es besteht Abwärtskompatibilität, und Verbindungen mit konformen TLS 1.2-Servern oder -Proxys werden nicht beeinträchtigt. Ältere Versionen einiger Proxys, die TLS abfangen, verfügen aber über einen Implementierungsfehler, der zu Inkompatibilität führt.

Wenn Sie diese Richtlinie einschalten oder nicht festlegen, wird Microsoft Edge diesen Sicherheitsschutz für alle Verbindungen einschalten.

Wenn Sie diese Richtlinie ausschalten, wird Microsoft Edge diesen Sicherheitsschutz für Verbindungen, die anhand von lokal installierten Zertifizierungsstellenzertifikaten authentifiziert werden, abschalten. Dieser Schutz ist immer für Verbindungen aktiviert, die mit öffentlich vertrauenswürdigen Zertifizierungsstellenzertifikaten authentifiziert werden.

Diese Richtlinie kann verwendet werden, um anhand von Tests betroffene Proxys zu ermitteln und zu aktualisieren. Für betroffene Proxys ist zu erwarten, dass ein Verbindungsfehler mit dem Fehlercode ERR_TLS13_DOWNGRADE_DETECTED auftritt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: TLS13HardeningForLocalAnchorsEnabled
  - Gruppenrichtlinienname: Aktivieren Sie ein TLS 1.3-Sicherheitsfeature für lokale Vertrauensanker. (veraltet)
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: TLS13HardeningForLocalAnchorsEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: TLS13HardeningForLocalAnchorsEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### TLSCipherSuiteDenyList
  #### Geben Sie die zu deaktivierenden TLS-Verschlüsselungssuites an
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 85 oder höher

  #### Beschreibung
  Konfigurieren Sie die Liste der Verschlüsselungssuites, die für TLS-Verbindungen deaktiviert sind.

Wenn Sie diese Richtlinie konfigurieren, wird die Liste der konfigurierten Verschlüsselungssuites beim Aufbau von TLS-Verbindungen nicht verwendet.

Wenn Sie diese Richtlinie nicht konfigurieren, wählt der Browser aus, welche TLS-Verschlüsselungssuites verwendet werden sollen.

Zu deaktivierende Verschlüsselungssuite-Werte werden als hexadezimale 16-Bit-Werte angegeben. Die Werte werden von der Registrierung der Internet Assigned Numbers Authority (IANA) zugewiesen.

Die TLS 1.3-Verschlüsselungssuite TLS_AES_128_GCM_SHA256 (0x1301) ist für TLS 1.3 erforderlich und kann durch diese Richtlinie nicht deaktiviert werden.

Diese Richtlinie hat keinen Einfluss auf QUIC-basierte Verbindungen. QUIC kann über die Richtlinie  [QuicAllowed](#quicallowed) deaktiviert werden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: TLSCipherSuiteDenyList
  - Gruppenrichtlinienname: Geben Sie die zu deaktivierenden TLS-Verschlüsselungssuites an
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\1 = "0x1303"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\2 = "0xcca8"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\3 = "0xcca9"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: TLSCipherSuiteDenyList
  - Beispielwert:
``` xml
<array>
  <string>0x1303</string>
  <string>0xcca8</string>
  <string>0xcca9</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### TabFreezingEnabled
  #### Einfrieren von Hintergrundtabs zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 79 oder höher

  #### Beschreibung
  Hiermit können Sie steuern, ob mit Microsoft Edge das Einfrieren von Tabs möglich ist, die sich seit mindestens fünf Minuten im Hintergrund befinden.

Durch das Einfrieren von Tabs wird der Verbrauch von CPU-, Akku- und Arbeitsspeicherressourcen reduziert. Microsoft Edge nutzt Heuristik, um das Einfrieren von Tabs zu verhindern, auf denen im Hintergrund nützliche Vorgänge durchgeführt werden, z. B. Anzeigen von Benachrichtigungen, Wiedergeben von Sound und Streamen von Videos.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, werden Tabs eingefroren, die sich seit mindestens fünf Minuten im Hintergrund befinden.

Wenn Sie diese Richtlinie deaktivieren, werden keine Tabs eingefroren.


  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: TabFreezingEnabled
  - Gruppenrichtlinienname: Einfrieren von Hintergrundtabs zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: TabFreezingEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: TabFreezingEnabled
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### TaskManagerEndProcessEnabled
  #### Beenden von Prozessen im Browser-Task-Manager ermöglichen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer Prozesse im Browser-Task-Manager beenden. Wenn Sie die Richtlinie deaktivieren, können Benutzer keine Prozesse beenden, und die Schaltfläche „Prozess beenden“ ist im Browser-Task-Manager deaktiviert.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: TaskManagerEndProcessEnabled
  - Gruppenrichtlinienname: Beenden von Prozessen im Browser-Task-Manager ermöglichen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: TaskManagerEndProcessEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: TaskManagerEndProcessEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### TotalMemoryLimitMb
  #### Dient zum Festlegen des Limits für den Arbeitsspeicher, der von einer einzelnen Microsoft Edge-Instanz beansprucht werden kann (in MB).
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 80 oder höher

  #### Beschreibung
  Konfiguriert die Menge an Arbeitsspeicher, die von einer einzelnen Microsoft Edge-Instanz beansprucht werden kann, bevor Tabs verworfen werden, um Arbeitsspeicher zu sparen. Der von dem Tab beanspruchte Arbeitsspeicher wird freigegeben, und der Tab muss neu geladen werden, wenn erneut zu ihm gewechselt wird.

Wenn Sie diese Richtlinie aktivieren, werden Tabs bei Erreichen des Limits durch den Browser verworfen, um Arbeitsspeicher zu sparen. Es wird jedoch nicht garantiert, dass das Limit niemals überschritten wird. Werte unter 1.024 werden auf 1.024 aufgerundet.

Wenn Sie diese Richtlinie nicht festlegen, versucht der Browser nur dann Arbeitsspeicher zu sparen, wenn erkannt wurde, dass auf dem Computer nur noch wenig physischer Speicher zur Verfügung steht.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: TotalMemoryLimitMb
  - Gruppenrichtlinienname: Dient zum Festlegen des Limits für den Arbeitsspeicher, der von einer einzelnen Microsoft Edge-Instanz beansprucht werden kann (in MB).
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: TotalMemoryLimitMb
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000800
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: TotalMemoryLimitMb
  - Beispielwert:
``` xml
<integer>2048</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### TrackingPrevention
  #### Blockieren der Nachverfolgung der Webbrowsing-Aktivitäten von Benutzern
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 78 oder höher

  #### Beschreibung
  Mit dieser Richtlinie können Sie entscheiden, ob Websites davon abgehalten werden sollen, die Webbrowsingaktivitäten der Benutzer nachzuverfolgen.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, können Benutzer die Stufe der Vorbeugung vor Nachverfolgung selbst festlegen.

Zuordnung der Richtlinienoptionen:

* TrackingPreventionOff (0) = Aus (keine Tracking-Verhinderung)

* TrackingPreventionBasic (1) = Grundlegend (Blockiert schädliche Tracker, Inhalte und Anzeigen werden personalisiert.)

* TrackingPreventionBalanced (2) = Ausgeglichen (Blockiert schädliche Tracker und Tracker von Websites, die der Benutzer nicht besucht hat; Inhalte und Anzeigen werden weniger personalisiert.)

* TrackingPreventionStrict (3) = Streng (Blockiert schädliche Tracker und den Großteil der Tracker von allen Websites; Inhalte und Anzeigen weisen eine minimale Personalisierung auf; einige Teile von Websites funktionieren möglicherweise nicht.)

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: TrackingPrevention
  - Gruppenrichtlinienname: Blockieren der Nachverfolgung der Webbrowsing-Aktivitäten von Benutzern
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: TrackingPrevention
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000002
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: TrackingPrevention
  - Beispielwert:
``` xml
<integer>2</integer>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### TranslateEnabled
  #### Übersetzung aktivieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Aktiviert den integrierten Microsoft-Übersetzungsdienst in Microsoft Edge.

Wenn Sie diese Richtlinie aktivieren, bietet Microsoft Edge dem Benutzer eine Übersetzungsfunktion in Form eines integrierten Übersetzungs-Flyouts (sofern geeignet) sowie eine Übersetzungsoption im Rechtsklick-Kontextmenü.

Deaktivieren Sie diese Richtlinie, um sämtliche integrierten Übersetzungsfeatures zu deaktivieren.

Wenn Sie die Richtlinie nicht konfigurieren, können Benutzer wählen, ob sie die Übersetzungsfunktion verwenden möchten.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Ja
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: TranslateEnabled
  - Gruppenrichtlinienname: Übersetzung aktivieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Administrative Vorlagen/Microsoft Edge - Standardeinstellungen (können durch Benutzer überschrieben werden)/
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): SOFTWARE\Policies\Microsoft\Edge\Empfohlen
  - Wertname: TranslateEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: TranslateEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### URLAllowlist
  #### Liste zulässiger URLs definieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Ermöglicht Zugriff auf die aufgelisteten URLs als Ausnahmen von der URL-Blockierungsliste.

Formatieren Sie die URL-Muster gemäß [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Mit dieser Richtlinie können Sie Ausnahmen zu restriktiven Blockierungslisten öffnen. Sie können beispielsweise "*" in die Blockierungsliste aufnehmen, um alle Anfragen zu blockieren, und dann diese Richtlinie verwenden, um den Zugriff auf eine begrenzte Liste von URLs zu ermöglichen. Mit dieser Richtlinie können Sie Ausnahmen für bestimmte Systeme, Subdomänen anderer Domänen, Ports oder bestimmte Pfade öffnen.

Der spezifischste Filter bestimmt, ob eine URL blockiert oder erlaubt ist. Die zulässige Liste hat Vorrang vor der Blockierungsliste.

Diese Richtlinie ist auf 1.000 Einträge begrenzt; nachfolgende Einträge werden ignoriert.

Diese Richtlinie ermöglicht es dem Browser außerdem, automatisch externe Anwendungen aufzurufen, die als Protokollhandler für Protokolle wie “tel:” oder “ssh:” registriert sind.

Wenn Sie diese Richtlinie nicht konfigurieren, gibt es keine Ausnahmen von der Blockierungsliste in der Richtlinie [URLBlocklist](#urlblocklist).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: URLAllowlist
  - Gruppenrichtlinienname: Liste zulässiger URLs definieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\URLAllowlist
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\5 = ".exact.hostname.com"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: URLAllowlist
  - Beispielwert:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### URLBlocklist
  #### Zugriff auf eine Liste von URLs blockieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Definiert basierend auf URL-Mustern eine Liste von Sites, die blockiert sind (der Benutzer kann sie nicht laden).

Formatieren Sie die URL-Muster gemäß [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Sie können in der Richtlinie [URLAllowlist](#urlallowlist) Ausnahmen definieren. Diese Richtlinien sind auf 1000 Einträge begrenzt; nachfolgende Einträge werden ignoriert.

Beachten Sie: Das Blockieren von internen 'edge://*'-URLs wird nicht empfohlen, weil es zu unerwarteten Fehlern führen kann.

Diese Richtlinie verhindert nicht, dass die Seite dynamisch durch JavaScript aktualisiert wird. Wenn Sie beispielsweise 'contoso.com/abc' blockieren, können Benutzer möglicherweise immer noch 'contoso.com' besuchen und auf einen Link klicken, um 'contoso.com/abc' aufzurufen, solange die Seite nicht aktualisiert wird.

Wenn Sie diese Richtlinie nicht konfigurieren, werden keine URLs blockiert.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: URLBlocklist
  - Gruppenrichtlinienname: Zugriff auf eine Liste von URLs blockieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\URLBlocklist
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
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


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: URLBlocklist
  - Beispielwert:
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
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### UserAgentClientHintsEnabled
  #### Aktivieren des Features “Client Hints des Benutzer-Agenten” (veraltet)
  >VERALTET: Diese Richtlinie ist veraltet. Sie wird gegenwärtig noch unterstützt, aber in einem zukünftigen Release ausgemustert.
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 86 oder höher

  #### Beschreibung
  Diese Richtlinie ist veraltet, weil Sie nur als kurzfristiger Mechanismus vorgesehen war, um Unternehmen mehr Zeit zum Aktualisieren Ihrer Webinhalte zu verschaffen, sofern diese mit dem Feature “Client Hints des Benutzer-Agenten” nicht kompatibel waren. In Microsoft Edge Version 89 funktioniert diese Richtlinie nicht.

Wenn diese Richtlinie aktiviert ist, sendet das Feature “Client Hints des Benutzer-Agenten” präzise Anforderungsheader, die Informationen über den Benutzerbrowser (z. B. die Browserversion) und die Umgebung (z. B. die Systemarchitektur) bereitstellen.

Dies ist ein zusätzliches Feature. Die neuen Kopfzeilen können allerdings manche Websites unterbrechen, die die Zeichen einschränken, die Anforderungen enthalten dürfen.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, ist das Feature “Client Hints des Benutzer-Agenten” aktiviert. Wenn Sie diese Richtlinie deaktivieren, ist das Feature nicht verfügbar.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: UserAgentClientHintsEnabled
  - Gruppenrichtlinienname: Aktivieren des Features “Client Hints des Benutzer-Agenten” (veraltet)
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: UserAgentClientHintsEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: UserAgentClientHintsEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### UserDataDir
  #### Benutzerdatenverzeichnis festlegen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Konfiguriert das Verzeichnis, das zum Speichern von Benutzerdaten verwendet werden soll.

Wenn Sie diese Richtlinie aktivieren, verwendet Microsoft Edge das angegebene Verzeichnis, unabhängig davon, ob der Benutzer das Befehlszeilenflag '--user-data-dir' festgelegt hat.

Wenn Sie diese Richtlinie nicht aktivieren, wird der Standardprofilpfad verwendet, den der Benutzer jedoch mithilfe des Flags '--user-data-dir' überschreiben kann. Benutzer finden das Verzeichnis für das Profil unter edge://version/ unter Profilpfad.

Um Datenverlust oder andere unerwartete Fehler zu vermeiden, konfigurieren Sie diese Richtlinie nicht für das Stammverzeichnis eines Volumes oder für ein Verzeichnis, das für andere Zwecke verwendet wird, da Microsoft Edge dessen Inhalt verwaltet.

Eine Liste der Variablen, die verwendet werden können, finden Sie unter [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: UserDataDir
  - Gruppenrichtlinienname: Benutzerdatenverzeichnis festlegen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: UserDataDir
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"${users}/${user_name}/Edge"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: UserDataDir
  - Beispielwert:
``` xml
<string>${users}/${user_name}/Edge</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### UserDataSnapshotRetentionLimit
  #### Beschränkt die Anzahl Momentaufnahmen von Benutzerdaten, die für den Fall eines Notfallrollbacks aufbewahrt werden.
  
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 86 oder höher

  #### Beschreibung
  Bei jeder Hauptversionsaktualisierung wird von Microsoft Edge eine Momentaufnahme von Teilen der Browserdaten des Benutzers erstellt. Diese kann bei einem später auftretenden Notfall für ein temporäres Versionsrollback verwendet werden. Wenn ein temporäres Rollback für eine Version ausgeführt wird, für die ein Benutzer über eine entsprechende Momentaufnahme verfügt, werden die in der Momentaufnahme enthaltenen Daten wiederhergestellt. Dadurch behalten Benutzer Einstellungen wie Lesezeichen und AutoAusfüllen-Daten.

Wenn Sie diese Richtlinie nicht festlegen, wird der Standardwert von drei Momentaufnahmen verwendet.

Wenn Sie diese Richtlinie festlegen, werden alte Momentaufnahmen bei Bedarf gelöscht, um das von Ihnen festgelegte Limit einzuhalten. Wenn Sie diese Richtlinie auf 0 festlegen, werden keine Momentaufnahmen erstellt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Ganze Zahl

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: UserDataSnapshotRetentionLimit
  - Gruppenrichtlinienname: Beschränkt die Anzahl Momentaufnahmen von Benutzerdaten, die für den Fall eines Notfallrollbacks aufbewahrt werden.
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: UserDataSnapshotRetentionLimit
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000003
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### UserFeedbackAllowed
  #### Benutzerfeedback zulassen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Microsoft Edge verwendet das Edge-Feedbackfeature (standardmäßig aktiviert), um Benutzern das Übermitteln von Feedback, Vorschlägen oder Kundenumfragen sowie das Melden von Problemen mit dem Browser zu ermöglichen. Das Edge-Feedbackfeature kann standardmäßig nicht von Benutzern deaktiviert werden.

Wenn Sie diese Richtlinie aktivieren oder nicht konfigurieren, können Benutzer das Edge-Feedbackfeature aufrufen.

Wenn Sie diese Richtlinie deaktivieren, können Benutzer das Edge-Feedbackfeature nicht aufrufen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: UserFeedbackAllowed
  - Gruppenrichtlinienname: Benutzerfeedback zulassen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: UserFeedbackAllowed
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: UserFeedbackAllowed
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### VideoCaptureAllowed
  #### Videoaufnahme zulassen oder blockieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Legt fest, ob Sites Videos aufnehmen können.

Ist diese Richtlinie aktiviert oder nicht konfiguriert (Standard), wird der Benutzer für alle Websites vor der Videoaufzeichnung um Erlaubnis gefragt. Ausnahme: Für Sites mit URLs, die in der Liste der Richtlinie [VideoCaptureAllowedUrls](#videocaptureallowedurls) aufgeführt sind, wird der Zugriff ohne Nachfrage gewährt.

Wenn Sie diese Richtlinie deaktivieren, wird der Benutzer nicht gefragt, und eine Videoaufnahme ist nur für URLs möglich, die in der Richtlinie [VideoCaptureAllowedUrls](#videocaptureallowedurls) konfiguriert sind.

Diese Richtlinie betrifft alle Arten von Videoeingängen, nicht nur die eingebaute Kamera.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: VideoCaptureAllowed
  - Gruppenrichtlinienname: Videoaufnahme zulassen oder blockieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: VideoCaptureAllowed
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000000
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: VideoCaptureAllowed
  - Beispielwert:
``` xml
<false/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### VideoCaptureAllowedUrls
  #### Websites, die auf Videoaufnahmegeräte zugreifen können, ohne eine Berechtigung anzufordern
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Geben Sie Websites basierend auf URL-Mustern an, die Videoaufnahmegeräte verwenden können, ohne den Benutzer um Erlaubnis zu bitten. Muster in dieser Liste werden mit dem Sicherheitsursprung der anfordernden URL abgeglichen. Wenn sie übereinstimmen, wird der Website automatisch der Zugriff auf Videoaufnahmegeräte gewährt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: VideoCaptureAllowedUrls
  - Gruppenrichtlinienname: Websites, die auf Videoaufnahmegeräte zugreifen können, ohne eine Berechtigung anzufordern
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: VideoCaptureAllowedUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### WPADQuickCheckEnabled
  #### WPAD-Optimierung festlegen
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Ermöglicht das deaktivieren der WPAD-Optimierung (Web Proxy Auto-Discovery) in Microsoft Edge.

Wenn Sie diese Richtlinie deaktivieren, wird die WPAD-Optimierung deaktiviert. Dadurch muss der Browser länger auf DNS-basierte WPAD-Server warten.

Wenn Sie die Richtlinie aktivieren oder nicht konfigurieren, ist die WPAD-Optimierung aktiviert.

Unabhängig davon, ob oder wie diese Richtlinie aktiviert ist, kann die Einstellung für die WPAD-Optimierung nicht von Benutzern geändert werden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: WPADQuickCheckEnabled
  - Gruppenrichtlinienname: WPAD-Optimierung festlegen
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: WPADQuickCheckEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: WPADQuickCheckEnabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### WebAppInstallForceList
  #### Liste der Web-Apps, deren Installation erzwungen wurde, konfigurieren
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 80 oder höher

  #### Beschreibung
  Gibt eine Liste der Websites an, die ohne Benutzereingriff im Hintergrund installiert werden und vom Benutzer weder deinstalliert noch deaktiviert werden können.

Jedes Listenelement der Richtlinie ist ein Objekt mit den folgenden Mitgliedern:
  - „url“ (erforderlich). „url“ ist die URL der zu installierenden Web-App.

Werte für die optionalen Mitglieder sind:
  - „launch_container“ ist entweder „window“ oder „tabׅ“ und gibt an, wie die Web-App nach der Installation geöffnet wird.
  - „create_desktop_shortcut“ muss „true“ sein, wenn eine Desktopverknüpfung unter Windows erstellt werden soll.

Wenn „default_launch_container“ ausgelassen wird, wird die App standardmäßig in einer Registerkarte geöffnet. Unabhängig vom Wert von „default_launch_container“ können Benutzer den Container ändern, in dem die App geöffnet wird. Wenn „create_desktop_shortcuts“ ausgelassen wird, werden keine Desktopverknüpfungen erstellt.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Ja

  #### Datentyp:
  - Wörterbuch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: WebAppInstallForceList
  - Gruppenrichtlinienname: Liste der Web-Apps, deren Installation erzwungen wurde, konfigurieren
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: WebAppInstallForceList
  - Werttyp: REG_SZ
  ##### Beispielwert:
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


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: WebAppInstallForceList
  - Beispielwert:
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
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### WebComponentsV0Enabled
  #### Aktivieren Sie die v0-API der Webkomponenten bis M84 erneut (veraltet)
  
  >VERALTET: Diese Richtlinie ist veraltet und funktioniert nach Microsoft Edge Version 84 nicht mehr.
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 80, bis 84

  #### Beschreibung
  Diese Richtlinie ist veraltet, weil sie gestattet, dass diese Features bis zu Microsoft Edge Version 85 selektiv erneut aktiviert werden können. Die Webkomponenten v0-APIs (Shadow DOM v0, Custom Elements V0 und HTML Imports) wurden im Jahr 2018 verworfen und sind seit Microsoft Edge Version 80 standardmäßig deaktiviert.

Wenn Sie diese Richtlinie auf "wahr" festgelegen, werden die Webkomponenten "v0" für alle Websites aktiviert.

Wenn Sie diese Richtlinie auf "falsch" oder nicht festlegen, werden die Features der Webkomponenten v0 ab Microsoft Edge Version 80 standardmäßig deaktiviert.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: WebComponentsV0Enabled
  - Gruppenrichtlinienname: Aktivieren Sie die v0-API der Webkomponenten bis M84 erneut (veraltet)
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: WebComponentsV0Enabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: WebComponentsV0Enabled
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### WebDriverOverridesIncompatiblePolicies
  #### Zulassen, dass WebDriver inkompatible Richtlinien außer Kraft setzt (veraltet)
  
  >VERALTET: Diese Richtlinie ist veraltet und funktioniert nach Microsoft Edge Version 84 nicht mehr.
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77, bis 84

  #### Beschreibung
  Diese Richtlinie funktioniert nicht, da WebDriver jetzt mit allen bestehenden Richtlinien kompatibel ist.

       Diese Richtlinie ermöglicht Benutzern der WebDriver-Funktion, Richtlinien außer Kraft zu setzen
,      die den Betrieb von WebDriver stören können.

       Derzeit deaktiviert diese Richtlinie die Richtlinien [SitePerProcess](#siteperprocess) und [IsolateOrigins](#isolateorigins).

       Wenn die Richtlinie aktiviert ist, ist WebDriver in der Lage, inkompatible
Richtlinien außer Kraft zu setzen.
Wenn die Richtlinie deaktiviert oder nicht konfiguriert ist, kann WebDriver
inkompatible Richtlinien nicht außer Kraft setzen.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: WebDriverOverridesIncompatiblePolicies
  - Gruppenrichtlinienname: Zulassen, dass WebDriver inkompatible Richtlinien außer Kraft setzt (veraltet)
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: WebDriverOverridesIncompatiblePolicies
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: WebDriverOverridesIncompatiblePolicies
  - Beispielwert:
``` xml
<true/>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### WebRtcLocalIpsAllowedUrls
  #### Verfügbarmachung von lokalen IP-Adressen durch WebRTC verwalten
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 80 oder höher

  #### Beschreibung
  Gibt eine Liste mit Ursprüngen (URLs) oder Hostnamen-Mustern (z. B. „*contoso.com*“) an, für die lokale IP-Adressen durch WebRTC verfügbar gemacht werden sollen.

Wenn Sie diese Richtlinie aktivieren und eine Liste mit Ursprüngen (URLs) oder Hostnamen-Mustern festlegen, macht WebRTC die lokale IP-Adresse bei einer Übereinstimmung mit den Mustern in der Liste verfügbar, wenn edge://flags/#enable-webrtc-hide-local-ips-with-mdns aktiviert ist.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren und edge://flags/#enable-webrtc-hide-local-ips-with-mdns aktiviert ist, macht WebRTC die lokalen IP-Adressen nicht verfügbar. Die lokale IP-Adresse wird durch einen mDNS-Hostnamen verborgen.

Wenn Sie diese Richtlinie aktivieren, deaktivieren oder nicht konfigurieren und edge://flags/#enable-webrtc-hide-local-ips-with-mdns deaktiviert ist, macht WebRTC lokale IP-Adressen verfügbar.

Beachten Sie, dass diese Richtlinie den Schutz der lokalen IP-Adressen schwächt, der u. U. von Administratoren benötigt wird.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Liste der Zeichenfolgen

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: WebRtcLocalIpsAllowedUrls
  - Gruppenrichtlinienname: Verfügbarmachung von lokalen IP-Adressen durch WebRTC verwalten
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: 1, 2, 3, ...
  - Werttyp: Liste von REG_SZ
  ##### Beispielwert:
```
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\2 = "*contoso.com*"

```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: WebRtcLocalIpsAllowedUrls
  - Beispielwert:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>*contoso.com*</string>
</array>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### WebRtcLocalhostIpHandling
  #### Verfügbarmachung der lokalen IP-Adresse durch WebRTC beschränken
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Mit dieser Richtlinie können Sie festlegen, ob WebRTC die lokale IP-Adresse des Benutzers verfügbar macht.

Wenn Sie diese Richtlinie auf "AllowAllInterfaces" oder "AllowPublicAndPrivateInterfaces" festlegen, macht WebRTC die lokale IP-Adresse verfügbar.

Wenn Sie diese Richtlinie auf "AllowPublicInterfaceOnly" oder "DisableNonProxiedUdp" festlegen, macht WebRTC die lokale IP-Adresse nicht verfügbar.

Wenn Sie diese Richtlinie nicht festlegen oder sie deaktivieren, macht WebRTC die lokale IP-Adresse verfügbar.

Zuordnung der Richtlinienoptionen:

* AllowAllInterfaces (default) = Alle Schnittstellen zulassen. Dadurch wird die lokale IP-Adresse verfügbar gemacht.

* AllowPublicAndPrivateInterfaces (default_public_and_private_interfaces) = Öffentliche und private Schnittstellen über HTTP-Standardroute zulassen. Dadurch wird die lokale IP-Adresse verfügbar gemacht.

* AllowPublicInterfaceOnly (default_public_interface_only) = Öffentliche Schnittstelle über HTTP-Standardroute zulassen. Dadurch wird die lokale IP-Adresse nicht verfügbar gemacht.

* DisableNonProxiedUdp (disable_non_proxied_udp) = Verwenden Sie TCP, falls der Proxyserver UDP nicht unterstützt. Dadurch wird die lokale IP-Adresse nicht verfügbar gemacht.

Nutzen Sie die vorherigen Informationen zum Konfigurieren dieser Richtlinie.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: WebRtcLocalhostIpHandling
  - Gruppenrichtlinienname: Verfügbarmachung der lokalen IP-Adresse durch WebRTC beschränken
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: WebRtcLocalhostIpHandling
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"default"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: WebRtcLocalhostIpHandling
  - Beispielwert:
``` xml
<string>default</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### WebRtcUdpPortRange
  #### Bereich der lokalen, von WebRTC verwendeten UDP-Ports einschränken
  
  
  #### Unterstützte Versionen:
  - Bei Windows und macOS seit 77 oder höher

  #### Beschreibung
  Schränkt den von WebRTC verwendeten UDP-Portbereich auf ein angegebenes Portintervall (Endpunkte eingeschlossen) ein.

Wenn Sie diese Richtlinie konfigurieren, geben Sie den Bereich der lokalen UDP-Ports an, die von WebRTC verwendet werden können.

Wenn Sie diese Richtlinie nicht konfigurieren, oder wenn Sie sie auf eine leere Zeichenfolge oder einen ungültigen Portbereich festlegen, kann WebRTC einen beliebigen verfügbaren lokalen UDP-Port verwenden.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Zeichenfolge

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: WebRtcUdpPortRange
  - Gruppenrichtlinienname: Bereich der lokalen, von WebRTC verwendeten UDP-Ports einschränken
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: WebRtcUdpPortRange
  - Werttyp: REG_SZ
  ##### Beispielwert:
```
"10000-11999"
```


  #### Mac-Informationen und -Einstellungen
  - Gewünschter Schlüsselname: WebRtcUdpPortRange
  - Beispielwert:
``` xml
<string>10000-11999</string>
```
  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)

  ### WinHttpProxyResolverEnabled
  #### Verwenden von Windows-Proxy-Konfliktlöser (veraltet)
  >VERALTET: Diese Richtlinie ist veraltet. Sie wird gegenwärtig noch unterstützt, aber in einem zukünftigen Release ausgemustert.
  
  #### Unterstützte Versionen:
  - Unter Windows seit Version 84 oder höher

  #### Beschreibung
  Diese Richtlinie ist veraltet. Sie wird von einem ähnlichen Feature im Rahmen eines zukünftigen Releases ersetzt, vgl. https://crbug.com/1032820.

Verwenden Sie Windows anstelle des in Microsoft Edge integrierten Proxyresolvers, um Proxys für alle Browser-Netzwerke aufzulösen. Die Windows Proxy Auflösung ermöglicht Windows-Proxy Funktionen wie DirectAccess/NRPT.

Diese Richtlinie enthält die unter https://crbug.com/644030 beschriebenen Probleme. Sie führen dazu, dass PAC-Dateien von Windows-Code abgerufen und ausgeführt werden. Dies gilt auch für PAC-Dateien, die über die [ProxyPacUrl](#proxypacurl)-Richtlinie festgelegt wurden. Da das Netzwerk beim Abrufen von PAC-Dateien über Windows- statt überMicrosoft Edge-Code erfolgt, gelten Netzwerkrichtlinien wie [DnsOverHttpsMode](#dnsoverhttpsmode) nicht für Netzwerkabrufe für eine PAC-Datei.

Wenn Sie diese Richtlinie aktivieren, wird der Windows-Proxyresolver verwendet.

Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, wird der  Microsoft Edge-Proxyresolver verwendet.

  #### Unterstützte Features:
  - Kann zwingend sein: Ja
  - Kann empfohlen werden: Nein
  - Dynamische Richtlinienaktualisierung: Nein - Erfordert einen Neustart des Browsers

  #### Datentyp:
  - Boolesch

  #### Windows-Informationen und-Einstellungen
  ##### Informationen zur Gruppenrichtlinie (ADMX)
  - Eindeutiger Name der Gruppenrichtlinie: WinHttpProxyResolverEnabled
  - Gruppenrichtlinienname: Verwenden von Windows-Proxy-Konfliktlöser (veraltet)
  - Gruppenrichtlinienpfad (Erforderlich): Administrative Vorlagen/Microsoft Edge/
  - Gruppenrichtlinienpfad (Empfohlen): Nicht zutreffend
  - Name der ADMX-Datei der Gruppenrichtlinie: MSEdge.admx
  ##### Windows-Registrierungseinstellungen
  - Pfad (Erforderlich): SOFTWARE\Policies\Microsoft\Edge
  - Pfad (Empfohlen): Nicht zutreffend
  - Wertname: WinHttpProxyResolverEnabled
  - Werttyp: REG_DWORD
  ##### Beispielwert:
```
0x00000001
```


  

  [Zurück nach oben](#microsoft-edge-–-richtlinien)


## Siehe auch
- [Konfigurieren von Microsoft Edge](configure-microsoft-edge.md)
- [Microsoft Edge: Zielseite für Unternehmen](https://aka.ms/EdgeEnterprise)
- [Blog zu Microsoft Security-Baselines](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)