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

# Microsoft Edge - Stratégies
La dernière version de Microsoft Edge inclut les stratégies suivantes. Vous pouvez utiliser ces stratégies pour configurer l’exécution de Microsoft Edge au sein de votre organisation.

Pour plus d’informations sur un autre ensemble de stratégies utilisées pour contrôler la façon dont Microsoft Edge est mis à jour, consultez [Référence de la stratégie de mise à jour Microsoft Edge](microsoft-edge-update-policies.md).

Vous pouvez télécharger le [Kit de ressources Sécurité et conformité Microsoft](https://www.microsoft.com/download/details.aspx?id=55319) pour les paramètres de base de configuration de sécurité recommandés pour Microsoft Edge. Pour plus d’informations, voir le [Blog des Bases de référence de sécurité Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines).

> [!REMARQUE]
> Cet article s’applique à Microsoft Edge version 77 ou ultérieure.

## Stratégies disponibles
Ces tableaux répertorient toutes les stratégies de groupe liées au navigateur disponibles dans cette version de Microsoft Edge. Utilisez les liens de la table pour obtenir plus de détails sur les stratégies spécifiques.

|||
|-|-|
|[Authentification HTTP](#authentification-http)|[Cast](#cast)|
|[Démarrage, page d’accueil et page Nouvel onglet](#démarrage-page-d’accueil-et-page-nouvel-onglet)|[Extensions](#extensions)|
|[Gestionnaire de mot de passe et protection](#gestionnaire-de-mot-de-passe-et-protection)|[Impression](#impression)|
|[Messagerie native](#messagerie-native)|[Moteur de recherche par défaut](#moteur-de-recherche-par-défaut)|
|[Paramètres de SmartScreen](#paramètres-de-smartscreen)|[Paramètres de contenu](#paramètres-de-contenu)|
|[Paramètres d’Application Guard](#paramètres-d’application-guard)|[Serveur proxy](#serveur-proxy)|
|[Additional](#additional)|

### [*Authentification HTTP*](#authentification-http-policies)
|Nom de la stratégie|Sous-titre|
|-|-|
|[AllowCrossOriginAuthPrompt](#allowcrossoriginauthprompt)|Autoriser les invites d’authentification de base HTTP cross-origin|
|[AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)|Spécifie la liste des serveurs auxquels Microsoft Edge peut déléguer des identifiants utilisateur|
|[AuthSchemes](#authschemes)|Schémas d’authentification pris en charge|
|[AuthServerAllowlist](#authserverallowlist)|Configurer la liste des serveurs d’authentification autorisés|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|Désactiver la recherche CNAME lors de la négociation de l’authentification Kerberos|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|Inclure le port non standard dans Kerberos SPN|
|[NtlmV2Enabled](#ntlmv2enabled)|Contrôler si l’authentification NTLMv2 est activée|
### [*Cast*](#cast-policies)
|Nom de la stratégie|Sous-titre|
|-|-|
|[EnableMediaRouter](#enablemediarouter)|Activer Google Cast|
|[ShowCastIconInToolbar](#showcasticonintoolbar)|Afficher l’icône de diffusion dans la barre d’outils|
### [*Démarrage&comma; page d’accueil et page Nouvel onglet*](#démarrage-page-d’accueil-et-page-nouvel-onglet-policies)
|Nom de la stratégie|Sous-titre|
|-|-|
|[HomepageIsNewTabPage](#homepageisnewtabpage)|Définir la page Nouvel onglet comme page d’accueil|
|[HomepageLocation](#homepagelocation)|Configurer l’URL de la page d’accueil|
|[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)|Configurer les types d’arrière-plan autorisés pour la mise en page du nouvel onglet|
|[NewTabPageCompanyLogo](#newtabpagecompanylogo)|Définir un nouvel onglet pour le logo de l'entreprise (obsolète)|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|Masquer les sites populaires par défaut à partir du nouvel onglet|
|[NewTabPageLocation](#newtabpagelocation)|Configurer l’URL du nouvel onglet|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|Définir les liens rapides du nouvel onglet|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|Activer le préchargement de la page Nouvel onglet pour un rendu plus rapide|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|Configurer l’expérience de nouvel onglet Microsoft Edge|
|[RestoreOnStartup](#restoreonstartup)|Action à exécuter au démarrage|
|[RestoreOnStartupURLs](#restoreonstartupurls)|Sites à ouvrir au démarrage du navigateur|
|[ShowHomeButton](#showhomebutton)|Afficher le bouton Accueil sur la barre d’outils|
### [*Extensions*](#extensions-policies)
|Nom de la stratégie|Sous-titre|
|-|-|
|[ExtensionAllowedTypes](#extensionallowedtypes)|Configurer les types d’extensions autorisées|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|Autoriser l'installation d'extensions spécifiques|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|Contrôler les extensions impossibles à installer|
|[ExtensionInstallForcelist](#extensioninstallforcelist)|Contrôler les extensions qui sont installées en mode silencieux|
|[ExtensionInstallSources](#extensioninstallsources)|Configurer l’extension et les sources d’installation du script utilisateur|
|[ExtensionSettings](#extensionsettings)|Configurer les paramètres de gestion des extensions|
### [*Gestionnaire de mot de passe et protection*](#gestionnaire-de-mot-de-passe-et-protection-policies)
|Nom de la stratégie|Sous-titre|
|-|-|
|[PasswordManagerEnabled](#passwordmanagerenabled)|Activer l’enregistrement des mots de passe pour le Gestionnaire de mot de passe|
|[PasswordMonitorAllowed](#passwordmonitorallowed)|Autoriser les utilisateurs à être avertis si leur mot de passe est considéré comme non sécurisé|
|[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)|Configurer l’URL de modification du mot de passe|
|[PasswordProtectionLoginURLs](#passwordprotectionloginurls)|Configurer la liste des URL de connexion d’entreprise dans lesquelles le service de protection par mot de passe doit capturer les hachages salés d’un mot de passe|
|[PasswordProtectionWarningTrigger](#passwordprotectionwarningtrigger)|Configurer le déclencheur d'avertissement de protection par mot de passe|
### [*Impression*](#impression-policies)
|Nom de la stratégie|Sous-titre|
|-|-|
|[DefaultPrinterSelection](#defaultprinterselection)|Règles de sélection d’imprimante par défaut|
|[PrintHeaderFooter](#printheaderfooter)|Imprimer des en-têtes et des pieds de page|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|Définir l’imprimante système par défaut en tant qu’imprimante par défaut|
|[PrintingEnabled](#printingenabled)|Activer l’impression|
|[PrintingPaperSizeDefault](#printingpapersizedefault)|Taille de la page d’impression par défaut|
|[UseSystemPrintDialog](#usesystemprintdialog)|Imprimer à l’aide de la boîte de dialogue d’impression système|
### [*Messagerie native*](#messagerie-native-policies)
|Nom de la stratégie|Sous-titre|
|-|-|
|[NativeMessagingAllowlist](#nativemessagingallowlist)|Contrôle des hôtes de messagerie natifs pouvant être utilisés par les utilisateurs|
|[NativeMessagingBlocklist](#nativemessagingblocklist)|Configurer la liste rouge de messagerie native|
|[NativeMessagingUserLevelHosts](#nativemessaginguserlevelhosts)|Autoriser les hôtes de messagerie natifs au niveau de l’utilisateur (installés sans autorisation d’administrateur)|
### [*Moteur de recherche par défaut*](#moteur-de-recherche-par-défaut-policies)
|Nom de la stratégie|Sous-titre|
|-|-|
|[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)|Activer le moteur de recherche par défaut|
|[DefaultSearchProviderEncodings](#defaultsearchproviderencodings)|Encodages du moteur de recherche par défaut|
|[DefaultSearchProviderImageURL](#defaultsearchproviderimageurl)|Spécifie la fonction de recherche-par-image pour le moteur de recherche par défaut|
|[DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams)|Paramètres pour une URL d’image qui utilise POST|
|[DefaultSearchProviderKeyword](#defaultsearchproviderkeyword)|Mot clé du moteur de recherche par défaut|
|[DefaultSearchProviderName](#defaultsearchprovidername)|Nom du moteur de recherche par défaut|
|[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)|URL de recherche du moteur de recherche par défaut|
|[DefaultSearchProviderSuggestURL](#defaultsearchprovidersuggesturl)|URL du moteur de recherche par défaut pour les suggestions|
|[NewTabPageSearchBox](#newtabpagesearchbox)|Configurer l’expérience de la zone de recherche de la page nouvel onglet|
### [*Paramètres de SmartScreen*](#paramètres-de-smartscreen-policies)
|Nom de la stratégie|Sous-titre|
|-|-|
|[PreventSmartScreenPromptOverride](#preventsmartscreenpromptoverride)|Empêcher le contournement des avertissements de Microsoft Defender SmartScreen pour les sites|
|[PreventSmartScreenPromptOverrideForFiles](#preventsmartscreenpromptoverrideforfiles)|Empêcher le contournement des avertissements de Microsoft Defender SmartScreen concernant les téléchargements|
|[SmartScreenAllowListDomains](#smartscreenallowlistdomains)|Configurer la liste des domaines pour lesquels Microsoft Defender SmartScreen ne déclenche pas d'avertissement|
|[SmartScreenEnabled](#smartscreenenabled)|Configurer Microsoft Defender SmartScreen|
|[SmartScreenForTrustedDownloadsEnabled](#smartscreenfortrusteddownloadsenabled)|Forcer les vérifications de Microsoft Defender SmartScreen sur les téléchargements provenant de sources approuvées|
|[SmartScreenPuaEnabled](#smartscreenpuaenabled)|Configurer Microsoft Defender SmartScreen de manière à bloquer les applications potentiellement indésirables|
### [*Paramètres de contenu*](#paramètres-de-contenu-policies)
|Nom de la stratégie|Sous-titre|
|-|-|
|[AutoSelectCertificateForUrls](#autoselectcertificateforurls)|Sélectionner automatiquement des certificats clients pour ces sites|
|[CookiesAllowedForUrls](#cookiesallowedforurls)|Autoriser les cookies sur des sites spécifiques|
|[CookiesBlockedForUrls](#cookiesblockedforurls)|Bloquer les cookies sur des sites spécifiques|
|[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)|Limiter les cookies provenant de sites web spécifiques à la session active|
|[DefaultCookiesSetting](#defaultcookiessetting)|Configurer les cookies|
|[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)|Contrôler l’utilisation de l’API du système de fichiers pour la lecture|
|[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)|Contrôler l’utilisation de l’API du système de fichiers pour l’écriture|
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|Paramètre de géolocalisation par défaut|
|[DefaultImagesSetting](#defaultimagessetting)|Paramètres des images par défaut|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|Contrôler l’utilisation des exceptions de contenu non sécurisé|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|Paramètre par défaut de JavaScript|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|Paramètres de notification par défaut|
|[DefaultPluginsSetting](#defaultpluginssetting)|Paramètre Adobe Flash par défaut|
|[DefaultPopupsSetting](#defaultpopupssetting)|Paramètres de fenêtre contextuelle par défaut|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|Contrôler l’utilisation de l’API web Bluetooth|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|Contrôler l’utilisation de l’API WebUSB|
|[FileSystemReadAskForUrls](#filesystemreadaskforurls)|Autoriser l’accès en lecture via l’API du système de fichiers sur ces sites|
|[FileSystemReadBlockedForUrls](#filesystemreadblockedforurls)|Bloquer l’accès en lecture via l’API du système de fichiers sur ces sites|
|[FileSystemWriteAskForUrls](#filesystemwriteaskforurls)|Autoriser l’accès en écriture aux fichiers et aux répertoires sur ces sites|
|[FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls)|Bloquer l’accès en écriture aux fichiers et aux répertoires sur ces sites|
|[ImagesAllowedForUrls](#imagesallowedforurls)|Autoriser les images sur ces sites|
|[ImagesBlockedForUrls](#imagesblockedforurls)|Bloquer les images sur des sites spécifiques|
|[InsecureContentAllowedForUrls](#insecurecontentallowedforurls)|Autoriser le contenu non sécurisé sur les sites spécifiés|
|[InsecureContentBlockedForUrls](#insecurecontentblockedforurls)|Bloquer le contenu non sécurisé sur les sites spécifiés|
|[JavaScriptAllowedForUrls](#javascriptallowedforurls)|Autoriser JavaScript sur des sites spécifiques|
|[JavaScriptBlockedForUrls](#javascriptblockedforurls)|Bloquer JavaScript sur des sites spécifiques|
|[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)|Activer les paramètres de comportement de cookie SameSite hérité par défaut|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist)|Rétablir le comportement SameSite hérité des cookies sur les sites spécifiés|
|[NotificationsAllowedForUrls](#notificationsallowedforurls)|Autoriser les notifications sur des sites spécifiques|
|[NotificationsBlockedForUrls](#notificationsblockedforurls)|Bloquer les notifications sur des sites spécifiques|
|[PluginsAllowedForUrls](#pluginsallowedforurls)|Autoriser le plug-in Adobe Flash sur des sites spécifiques|
|[PluginsBlockedForUrls](#pluginsblockedforurls)|Bloquer le plug-in Adobe Flash sur des sites spécifiques|
|[PopupsAllowedForUrls](#popupsallowedforurls)|Autoriser les fenêtres contextuelles sur des sites spécifiques|
|[PopupsBlockedForUrls](#popupsblockedforurls)|Bloquer les fenêtres contextuelles sur des sites spécifiques|
|[RegisteredProtocolHandlers](#registeredprotocolhandlers)|Inscrire les gestionnaires de protocole|
|[SpotlightExperiencesAndRecommendationsEnabled](#spotlightexperiencesandrecommendationsenabled)|Déterminez si les utilisateurs peuvent recevoir des images d’arrière-plan et du texte personnalisés, des suggestions, des notifications
et des conseils pour les services Microsoft|
|[WebUsbAllowDevicesForUrls](#webusballowdevicesforurls)|Accorder l’accès à des sites spécifiques pour se connecter à des périphériques USB spécifiques|
|[WebUsbAskForUrls](#webusbaskforurls)|Autoriser WebUSB sur des sites spécifiques|
|[WebUsbBlockedForUrls](#webusbblockedforurls)|Bloquer WebUSB sur des sites spécifiques|
### [*Paramètres d’Application Guard*](#paramètres-d’application-guard-policies)
|Nom de la stratégie|Sous-titre|
|-|-|
|[ApplicationGuardContainerProxy](#applicationguardcontainerproxy)|Proxy de conteneur Application Guard|
### [*Serveur proxy*](#serveur-proxy-policies)
|Nom de la stratégie|Sous-titre|
|-|-|
|[ProxyBypassList](#proxybypasslist)|Configurer les règles de contournement du proxy|
|[ProxyMode](#proxymode)|Configurer les paramètres du serveur proxy|
|[ProxyPacUrl](#proxypacurl)|Définir l'URL du fichier .pac du proxy|
|[ProxyServer](#proxyserver)|Configurer l’adresse ou l’URL du serveur proxy|
|[ProxySettings](#proxysettings)|Paramètres du proxy|
### [*Additional*](#additional-policies)
|Nom de la stratégie|Sous-titre|
|-|-|
|[AddressBarMicrosoftSearchInBingProviderEnabled](#addressbarmicrosoftsearchinbingproviderenabled)|Activer les suggestions de Recherche Microsoft dans Bing dans la barre d’adresse|
|[AdsSettingForIntrusiveAdsSites](#adssettingforintrusiveadssites)|Paramètres des annonces pour les sites contenant des annonces gênantes|
|[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory)|Activer la suppression de l'historique du navigateur et des téléchargements|
|[AllowFileSelectionDialogs](#allowfileselectiondialogs)|Boîtes de dialogue Autoriser la sélection de fichiers|
|[AllowPopupsDuringPageUnload](#allowpopupsduringpageunload)|Autorise une page à afficher les fenêtres contextuelles pendant son déchargement|
|[AllowSurfGame](#allowsurfgame)|Autoriser le jeu du surf|
|[AllowSyncXHRInPageDismissal](#allowsyncxhrinpagedismissal)|Autoriser les pages à envoyer des demandes XHR synchrones lors de l’opération de rejet de page (déconseillé)|
|[AllowTokenBindingForUrls](#allowtokenbindingforurls)|Configurez la liste des sites avec lesquels Microsoft Edge va tenter d’établir une liaison de jeton|
|[AllowTrackingForUrls](#allowtrackingforurls)|Configurer les exceptions de prévention du suivi pour des sites spécifiques|
|[AlternateErrorPagesEnabled](#alternateerrorpagesenabled)|Suggérer des pages similaires lorsqu’une page web est introuvable|
|[AlwaysOpenPdfExternally](#alwaysopenpdfexternally)|Toujours ouvrir les fichiers PDF en externe|
|[AmbientAuthenticationInPrivateModesEnabled](#ambientauthenticationinprivatemodesenabled)|Activer l’authentification ambiante pour les profils Invité et InPrivate|
|[AppCacheForceEnabled](#appcacheforceenabled)|Permet de réactiver la fonctionnalité AppCache, même si elle est désactivée par défaut|
|[ApplicationLocaleValue](#applicationlocalevalue)|Définir les paramètres régionaux de l'application|
|[AudioCaptureAllowed](#audiocaptureallowed)|Autoriser ou bloquer la capture audio|
|[AudioCaptureAllowedUrls](#audiocaptureallowedurls)|Sites pouvant accéder aux appareils de capture audio sans demander l’autorisation|
|[AudioSandboxEnabled](#audiosandboxenabled)|Autoriser l’exécution du bac à sable audio|
|[AutoImportAtFirstRun](#autoimportatfirstrun)|Importer automatiquement les données et les paramètres d’un autre navigateur lors de la première exécution|
|[AutoLaunchProtocolsFromOrigins](#autolaunchprotocolsfromorigins)|Définir une liste de protocoles qui peuvent lancer une application externe à partir d’origines, sans inviter l’utilisateur|
|[AutoOpenAllowedForURLs](#autoopenallowedforurls)|URL où les types de fichiers AutoOpenFileTypes peuvent s’appliquer|
|[AutoOpenFileTypes](#autoopenfiletypes)|Liste des types de fichiers qui doivent être automatiquement ouverts lors du téléchargement|
|[AutofillAddressEnabled](#autofilladdressenabled)|Activer le remplissage auto pour les adresses|
|[AutofillCreditCardEnabled](#autofillcreditcardenabled)|Activer le Remplissage auto pour les cartes de crédit|
|[AutoplayAllowed](#autoplayallowed)|Autoriser la lecture automatique de média pour les sites web|
|[BackgroundModeEnabled](#backgroundmodeenabled)|Poursuivre l’exécution des applications en arrière-plan après la fermeture de Microsoft Edge|
|[BackgroundTemplateListUpdatesEnabled](#backgroundtemplatelistupdatesenabled)|Active les mises à jour en arrière-plan de la liste des modèles disponibles pour les collections et d’autres fonctionnalités utilisées par des modèles|
|[BingAdsSuppression](#bingadssuppression)|Bloquer toutes les publicités dans les résultats de recherche Bing|
|[BlockThirdPartyCookies](#blockthirdpartycookies)|Bloquer les cookies tiers|
|[BrowserAddProfileEnabled](#browseraddprofileenabled)|Activer la création de profil à partir du menu déroulant Identité ou de la page Paramètres|
|[BrowserGuestModeEnabled](#browserguestmodeenabled)|Activer le mode invité|
|[BrowserNetworkTimeQueriesEnabled](#browsernetworktimequeriesenabled)|Autoriser les requêtes auprès d'un service de temps réseau de navigateur|
|[BrowserSignin](#browsersignin)|Paramètres de connexion du navigateur|
|[BuiltInDnsClientEnabled](#builtindnsclientenabled)|Utiliser le client DNS intégré|
|[BuiltinCertificateVerifierEnabled](#builtincertificateverifierenabled)|Détermine si le vérificateur de certificat intégré est utilisé pour vérifier les certificats de serveur (déconseillé)|
|[CertificateTransparencyEnforcementDisabledForCas](#certificatetransparencyenforcementdisabledforcas)|Désactiver l'application transparence de certificat pour la liste des hachages subjectPublicKeyInfo|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](#certificatetransparencyenforcementdisabledforlegacycas)|Désactivez l’application de transparence de certificat pour obtenir la liste des autorités de certification héritées|
|[CertificateTransparencyEnforcementDisabledForUrls](#certificatetransparencyenforcementdisabledforurls)|Désactiver l'application de transparence de certificat pour des URL spécifiques|
|[ClearBrowsingDataOnExit](#clearbrowsingdataonexit)|Effacer les données de navigation à la fermeture de Microsoft Edge|
|[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)|Effacer les images et les fichiers mis en cache lorsque Microsoft Edge se ferme|
|[ClickOnceEnabled](#clickonceenabled)|Autoriser les utilisateurs à ouvrir des fichiers à l’aide du protocole ClickOnce|
|[CollectionsServicesAndExportsBlockList](#collectionsservicesandexportsblocklist)|Bloquer l’accès à une liste spécifiée de services et de cibles d’exportation dans Collections|
|[CommandLineFlagSecurityWarningsEnabled](#commandlineflagsecuritywarningsenabled)|Activer les avertissements de sécurité pour les indicateurs de ligne de commande|
|[ComponentUpdatesEnabled](#componentupdatesenabled)|Activer les mises à jour de composant dans Microsoft Edge|
|[ConfigureDoNotTrack](#configuredonottrack)|Configurer Ne pas me suivre|
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|Configurer la connexion automatique avec un compte de domaine Active Directory en l'absence de compte de domaine Azure AD|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|Configuration la conversion de texte par synthèse vocale en ligne|
|[ConfigureShare](#configureshare)|Configurer l’expérience de partage|
|[CustomHelpLink](#customhelplink)|Spécifier le lien d’aide personnalisé|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|Vérifications d’interception DNS activées|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|Définir Microsoft Edge comme navigateur par défaut|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|Autoriser l’accès de recherche au menu contextuel du fournisseur de recherche par défaut|
|[DefaultSensorsSetting](#defaultsensorssetting)|Paramètre des capteurs par défaut|
|[DefaultSerialGuardSetting](#defaultserialguardsetting)|Contrôler l’utilisation de l’API série|
|[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)|Exiger que la Liste des sites en Mode entreprise soit disponible avant la navigation d’onglets|
|[DeleteDataOnMigration](#deletedataonmigration)|Supprimer les anciennes données de navigateur lors de la migration|
|[DeveloperToolsAvailability](#developertoolsavailability)|Contrôler où les outils de développement peuvent être utilisés|
|[DiagnosticData](#diagnosticdata)|Envoyer les données de diagnostic obligatoires et facultatives à propos de l’utilisation du navigateur|
|[DirectInvokeEnabled](#directinvokeenabled)|Autoriser les utilisateurs à ouvrir des fichiers à l’aide du protocole DirectInvoke|
|[Disable3DAPIs](#disable3dapis)|Désactiver la prise en charge des API graphiques 3D|
|[DisableScreenshots](#disablescreenshots)|Désactiver la création de captures d’écran|
|[DiskCacheDir](#diskcachedir)|Définir le répertoire du cache du disque|
|[DiskCacheSize](#diskcachesize)|Définir la taille de cache du disque, en octets|
|[DnsOverHttpsMode](#dnsoverhttpsmode)|Contrôler le mode DNS-sur-HTTPs|
|[DnsOverHttpsTemplates](#dnsoverhttpstemplates)|Spécifier le modèle d’URI du programme de résolution DNS sur HTTPS souhaité|
|[DownloadDirectory](#downloaddirectory)|Définir le répertoire de téléchargement|
|[DownloadRestrictions](#downloadrestrictions)|Autoriser les restrictions de téléchargement|
|[EdgeCollectionsEnabled](#edgecollectionsenabled)|Activer la fonctionnalité Collections|
|[EditFavoritesEnabled](#editfavoritesenabled)|Autorise les utilisateurs à modifier les favoris|
|[EnableDeprecatedWebPlatformFeatures](#enabledeprecatedwebplatformfeatures)|Réactiver les fonctionnalités de plateforme web déconseillées pendant une durée limitée|
|[EnableDomainActionsDownload](#enabledomainactionsdownload)|Activer le téléchargement des actions de domaine à partir de Microsoft (obsolète)|
|[EnableOnlineRevocationChecks](#enableonlinerevocationchecks)|Activer les contrôles de protocole OCSP/liste de révocation de certificats en ligne|
|[EnableSha1ForLocalAnchors](#enablesha1forlocalanchors)|Autoriser les certificats signés avec SHA-1 lorsqu’ils sont émis par des ancres d’approbation locales (déconseillé)|
|[EnterpriseHardwarePlatformAPIEnabled](#enterprisehardwareplatformapienabled)|Autoriser les extensions managées de manière à utiliser l’API de plateforme de matériel d’entreprise|
|[EnterpriseModeSiteListManagerAllowed](#enterprisemodesitelistmanagerallowed)|Autoriser l’accès à l’outil Gestionnaire de liste de sites en mode entreprise|
|[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](#exemptdomainfiletypepairsfromfiletypedownloadwarnings)|Désactiver le téléchargement des avertissements basés sur l’extension de type de fichier pour les types de fichiers spécifiés sur les domaines|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|Contrôler la communication avec le service d’expérimentation et de configuration|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox)|Afficher la case à cocher « Toujours ouvrir » dans la boîte de dialogue de protocole externe|
|[FamilySafetySettingsEnabled](#familysafetysettingsenabled)|Autoriser les utilisateurs à configurer Family Safety|
|[FavoritesBarEnabled](#favoritesbarenabled)|Activer la barre des favoris|
|[ForceBingSafeSearch](#forcebingsafesearch)|Appliquer la recherche sécurisée Bing|
|[ForceCertificatePromptsOnMultipleMatches](#forcecertificatepromptsonmultiplematches)|Configurez si Microsoft Edge doit sélectionner automatiquement un certificat lorsqu’il existe plusieurs correspondances de certificats pour un site configuré avec "AutoSelectCertificateForUrls"|
|[ForceEphemeralProfiles](#forceephemeralprofiles)|Activer l’utilisation des profils éphémères|
|[ForceGoogleSafeSearch](#forcegooglesafesearch)|Appliquer Google SafeSearch|
|[ForceLegacyDefaultReferrerPolicy](#forcelegacydefaultreferrerpolicy)|Utilisez une stratégie de renvoi par défaut no-referrer-when-downgrade (déconseillé)|
|[ForceNetworkInProcess](#forcenetworkinprocess)|Forcer le code de mise en réseau à s’exécuter dans le processus du navigateur (obsolète)|
|[ForceSync](#forcesync)|Forcer la synchronisation des données du navigateur et ne pas afficher l’invite de consentement de synchronisation|
|[ForceYouTubeRestrict](#forceyoutuberestrict)|Forcer le mode Limité YouTube minimal|
|[FullscreenAllowed](#fullscreenallowed)|Autoriser le mode plein écran|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|Activer le cache d'autorisation HTTP globalement étendu|
|[GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar)|Force la navigation directe sur un site intranet au lieu de rechercher des entrées à mots uniques dans la barre d’adresses|
|[HSTSPolicyBypassList](#hstspolicybypasslist)|Configurez la liste des noms qui vont contourner la vérification de stratégie HSTS|
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|Utiliser l’accélération matérielle (si disponible)|
|[HideFirstRunExperience](#hidefirstrunexperience)|Masquer l’expérience de première exécution et l’écran de démarrage|
|[ImportAutofillFormData](#importautofillformdata)|Autoriser l’importation des données du formulaire de remplissage auto|
|[ImportBrowserSettings](#importbrowsersettings)|Autoriser l’importation des paramètres du navigateur|
|[ImportCookies](#importcookies)|Autoriser l’importation de cookies|
|[ImportExtensions](#importextensions)|Autoriser l’importation d'extensions|
|[ImportFavorites](#importfavorites)|Autoriser l’importation des favoris|
|[ImportHistory](#importhistory)|Autoriser l’importation de l’historique de navigation|
|[ImportHomepage](#importhomepage)|Autoriser l’importation des paramètres de la page d’accueil|
|[ImportOpenTabs](#importopentabs)|Autoriser l’importation des onglets ouverts|
|[ImportPaymentInfo](#importpaymentinfo)|Autoriser l’importation des infos de paiement|
|[ImportSavedPasswords](#importsavedpasswords)|Autoriser l’importation des mots de passe enregistrés|
|[ImportSearchEngine](#importsearchengine)|Autoriser l’importation des paramètres du moteur de recherche|
|[ImportShortcuts](#importshortcuts)|Autoriser l’importation des raccourcis|
|[InPrivateModeAvailability](#inprivatemodeavailability)|Configurer la disponibilité du mode InPrivate|
|[InsecureFormsWarningsEnabled](#insecureformswarningsenabled)|Activer les avertissements pour les formulaires non sécurisés|
|[IntensiveWakeUpThrottlingEnabled](#intensivewakeupthrottlingenabled)|Contrôler la fonctionnalité IntensiveWakeUpThrottling|
|[InternetExplorerIntegrationEnhancedHangDetection](#internetexplorerintegrationenhancedhangdetection)|Configurez la détection de blocage améliorée pour le mode Internet Explorer|
|[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)|Configurer l’intégration d’Internet Explorer|
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|Configurer la liste des sites en Mode entreprise|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|Spécifier le type de comportement des navigations « entre les pages » vers des sites non configurés lorsqu’elles commencent sur des pages en mode Internet Explorer|
|[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed)|Autoriser le test du mode Internet Explorer|
|[IsolateOrigins](#isolateorigins)|Activer l’isolation de site pour des origines spécifiques|
|[LocalProvidersEnabled](#localprovidersenabled)|Autoriser les suggestions des fournisseurs locaux|
|[ManagedFavorites](#managedfavorites)|Configurer les favoris|
|[ManagedSearchEngines](#managedsearchengines)|Gérer les moteurs de recherche|
|[MaxConnectionsPerProxy](#maxconnectionsperproxy)|Nombre maximal de connexions simultanées au serveur proxy|
|[MediaRouterCastAllowAllIPs](#mediaroutercastallowallips)|Autoriser Google Cast à se connecter aux appareils Cast sur toutes les adresses IP|
|[MetricsReportingEnabled](#metricsreportingenabled)|Activer l’utilisation et les rapports de données liées à l’incident (déconseillé)|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|Activer l’occlusion de fenêtre native|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|Définition d’un délai d’expiration pour la navigation d’onglets de la Liste des sites en Mode entreprise|
|[NetworkPredictionOptions](#networkpredictionoptions)|Activer la prédiction réseau|
|[NonRemovableProfileEnabled](#nonremovableprofileenabled)|Configurer si un utilisateur dispose toujours d’un profil par défaut connecté automatiquement avec son compte professionnel ou scolaire|
|[OverrideSecurityRestrictionsOnInsecureOrigin](#overridesecurityrestrictionsoninsecureorigin)|Contrôler l’application des restrictions de sécurité aux origines non sécurisées|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|Autoriser les sites Web à demander des modes de paiement disponibles|
|[PersonalizationReportingEnabled](#personalizationreportingenabled)|Autoriser la personnalisation des publicités, de la recherche et des actualités en envoyant un historique de navigation à Microsoft|
|[PinningWizardAllowed](#pinningwizardallowed)|Autoriser l’Assistant Épingler à la barre des tâches|
|[ProactiveAuthEnabled](#proactiveauthenabled)|Activer l’authentification proactive|
|[PromotionalTabsEnabled](#promotionaltabsenabled)|Autoriser le contenu promotionnel dans des onglets|
|[PromptForDownloadLocation](#promptfordownloadlocation)|Demander où enregistrer les fichiers téléchargés|
|[QuicAllowed](#quicallowed)|Autoriser le protocole QUIC|
|[RelaunchNotification](#relaunchnotification)|Avertir un utilisateur qu’un redémarrage du navigateur est recommandé ou requis pour les mises à jour en attente|
|[RelaunchNotificationPeriod](#relaunchnotificationperiod)|Définir la période pour les notifications de mise à jour|
|[RendererCodeIntegrityEnabled](#renderercodeintegrityenabled)|Activer l’intégrité du code de rendu|
|[RequireOnlineRevocationChecksForLocalAnchors](#requireonlinerevocationchecksforlocalanchors)|Spécifier si des vérifications OCSP/liste de révocation de certificats en ligne sont obligatoires pour les ancres d’approbation locales|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|Activer la résolution des erreurs de navigation à l'aide d'un service web|
|[RestrictSigninToPattern](#restrictsignintopattern)|Restreindre les comptes qui peuvent être utilisés en tant que comptes principaux Microsoft Edge|
|[RoamingProfileLocation](#roamingprofilelocation)|Définir le répertoire de profils itinérants|
|[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)|Activer l’utilisation des copies itinérantes pour les données de profil Microsoft Edge|
|[RunAllFlashInAllowMode](#runallflashinallowmode)|Étendre le paramètre de contenu d'Adobe Flash à l'ensemble du contenu|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|Autoriser les utilisateurs à continuer à partir de la page d’avertissement HTTPS|
|[SSLVersionMin](#sslversionmin)|Version TLS minimale activée|
|[SaveCookiesOnExit](#savecookiesonexit)|Enregistrer les cookies lorsque Microsoft Edge se ferme|
|[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)|Désactiver l’enregistrement de l’historique du navigateur|
|[ScreenCaptureAllowed](#screencaptureallowed)|Autoriser ou refuser la capture d’écran|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|Activer le défilement vers le texte spécifié dans les fragments d’URL|
|[SearchSuggestEnabled](#searchsuggestenabled)|Activer les suggestions de recherche|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|Sites web ou domaines qui ne nécessitent pas l'autorisation d'utiliser l’attestation de clé de sécurité directe|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|Envoyer tous les sites intranet vers Internet Explorer|
|[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)|Envoyer les informations de site pour améliorer les services Microsoft (déconseillé)|
|[SensorsAllowedForUrls](#sensorsallowedforurls)|Autoriser l’accès aux capteurs sur des sites spécifiques|
|[SensorsBlockedForUrls](#sensorsblockedforurls)|Bloquer l’accès aux capteurs sur des sites spécifiques|
|[SerialAskForUrls](#serialaskforurls)|Autoriser l’API série sur des sites spécifiques|
|[SerialBlockedForUrls](#serialblockedforurls)|Bloquer l’API série sur des sites spécifiques|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|Afficher les raccourcis Microsoft Office dans la barre des favoris|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|Activer la prise en charge de SXG (échange HTTP signé)|
|[SitePerProcess](#siteperprocess)|Activer l’isolation de site pour chaque site|
|[SpellcheckEnabled](#spellcheckenabled)|Activer la vérification orthographique|
|[SpellcheckLanguage](#spellchecklanguage)|Activer des langues de vérification orthographique spécifiques|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|Forcer la désactivation des langues de la vérification orthographique|
|[StricterMixedContentTreatmentEnabled](#strictermixedcontenttreatmentenabled)|Activer le traitement plus strict pour le contenu mixte (déconseillé)|
|[SuppressUnsupportedOSWarning](#suppressunsupportedoswarning)|Supprimer l’avertissement de système d’exploitation non pris en charge|
|[SyncDisabled](#syncdisabled)|Désactiver la synchronisation des données à l’aide des services de synchronisation Microsoft|
|[SyncTypesListDisabled](#synctypeslistdisabled)|Configuration de la liste des types exclus de la synchronisation|
|[TLS13HardeningForLocalAnchorsEnabled](#tls13hardeningforlocalanchorsenabled)|Activez une fonctionnalité de sécurité TLS 1.3 pour les ancres d’approbation locales. (obsolète)|
|[TLSCipherSuiteDenyList](#tlsciphersuitedenylist)|Spécifier les suites de chiffrement TLS à désactiver|
|[TabFreezingEnabled](#tabfreezingenabled)|Autoriser le gel des onglets d’arrière-plan|
|[TaskManagerEndProcessEnabled](#taskmanagerendprocessenabled)|Activer la fin des processus dans le gestionnaire des tâches du navigateur|
|[TotalMemoryLimitMb](#totalmemorylimitmb)|Définissez une limite de mémoire en méga-octets qu’une seule instance de Microsoft Edge peut utiliser.|
|[TrackingPrevention](#trackingprevention)|Bloquer le suivi de l’activité de navigation sur le Web des utilisateurs|
|[TranslateEnabled](#translateenabled)|Activer Traduire|
|[URLAllowlist](#urlallowlist)|Définir une liste d’URL autorisées|
|[URLBlocklist](#urlblocklist)|Bloquer l’accès à une liste d’URL|
|[UserAgentClientHintsEnabled](#useragentclienthintsenabled)|Activer la fonctionnalité Indications client de l’agent utilisateur (déconseillé)|
|[UserDataDir](#userdatadir)|Définir le répertoire des données utilisateur|
|[UserDataSnapshotRetentionLimit](#userdatasnapshotretentionlimit)|Limite le nombre d’instantanés de données utilisateur conservés pour une utilisation en cas d’annulation d’urgence|
|[UserFeedbackAllowed](#userfeedbackallowed)|Autoriser les commentaires des utilisateurs|
|[VideoCaptureAllowed](#videocaptureallowed)|Autoriser ou bloquer la capture vidéo|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|Sites pouvant accéder aux appareils de capture vidéo sans demander l’autorisation|
|[WPADQuickCheckEnabled](#wpadquickcheckenabled)|Définir l'optimisation WPAD|
|[WebAppInstallForceList](#webappinstallforcelist)|Configurer la liste des applications web installées de force|
|[WebComponentsV0Enabled](#webcomponentsv0enabled)|Réactivez l’API Web Components v0 jusqu’à M84 (obsolète)|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|Autoriser WebDriver à remplacer les stratégies incompatibles (obsolète)|
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|Gérer l’exposition des adresses IP locales par WebRTC|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|Limiter l’exposition de l’adresse IP locale par WebRTC|
|[WebRtcUdpPortRange](#webrtcudpportrange)|Limiter la plage de ports UDP locaux utilisés par WebRTC|
|[WinHttpProxyResolverEnabled](#winhttpproxyresolverenabled)|Utiliser le programme de résolution du proxy Windows (déconseillé)|




  ## Authentification HTTP policies

  [Revenir au début](#microsoft-edge---stratégies)

  ### AllowCrossOriginAuthPrompt
  #### Autoriser les invites d’authentification de base HTTP cross-origin
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Contrôle si le contenu secondaire tiers sur une page peut ouvrir une boîte de dialogue d’authentification de base HTTP.

En règle générale, cette option est désactivée pour une protection contre le hameçonnage. Si vous ne configurez pas cette stratégie, elle est désactivée et le contenu secondaire tiers ne peut pas ouvrir une boîte de dialogue d’authentification de base HTTP.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AllowCrossOriginAuthPrompt
  - Nom de la stratégie de groupe: Autoriser les invites d’authentification de base HTTP cross-origin
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Authentification HTTP
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AllowCrossOriginAuthPrompt
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AllowCrossOriginAuthPrompt
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AuthNegotiateDelegateAllowlist
  #### Spécifie la liste des serveurs auxquels Microsoft Edge peut déléguer des identifiants utilisateur
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Configurer la liste des serveurs auxquels Microsoft Edge peut déléguer.

	Séparez plusieurs noms de serveurs par des virgules. Les caractères génériques (*) sont autorisés.

	Si vous ne configurez pas cette stratégie, Microsoft Edge ne peut pas déléguer les informations d’identification de l’utilisateur, même si un serveur est détecté comme intranet.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AuthNegotiateDelegateAllowlist
  - Nom de la stratégie de groupe: Spécifie la liste des serveurs auxquels Microsoft Edge peut déléguer des identifiants utilisateur
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Authentification HTTP
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AuthNegotiateDelegateAllowlist
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"contoso.com"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AuthNegotiateDelegateAllowlist
  - Exemple de valeur :
``` xml
<string>contoso.com</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AuthSchemes
  #### Schémas d’authentification pris en charge
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifie les schémas d’authentification HTTP pris en charge.

Vous pouvez configurer la stratégie en utilisant les valeurs suivantes : « basic », « digest », « ntlm » et « negotiate ». Séparez plusieurs valeurs par des virgules.

Si vous ne configurez pas cette stratégie, les quatre modèles sont utilisés.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AuthSchemes
  - Nom de la stratégie de groupe: Schémas d’authentification pris en charge
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Authentification HTTP
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AuthSchemes
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"basic,digest,ntlm,negotiate"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AuthSchemes
  - Exemple de valeur :
``` xml
<string>basic,digest,ntlm,negotiate</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AuthServerAllowlist
  #### Configurer la liste des serveurs d’authentification autorisés
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifie les serveurs à activer pour l’authentification intégrée. L’authentification intégrée n’est activée que lorsque Microsoft Edge reçoit une demande d’authentification à partir d’un proxy ou d’un serveur de cette liste.

	Séparez les noms de serveurs multiples par des virgules. Les caractères génériques (*) sont autorisés.

	Si vous ne configurez pas cette stratégie, Microsoft Edge essaie de détecter si un serveur se trouve sur l’intranet. Ce n'est qu'à ce moment-là qu’il répond aux requêtes IWA. Si le serveur se trouve sur Internet, les requêtes IWA émanant de celui-ci sont ignorées par Microsoft Edge.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AuthServerAllowlist
  - Nom de la stratégie de groupe: Configurer la liste des serveurs d’authentification autorisés
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Authentification HTTP
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AuthServerAllowlist
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"*contoso.com,contoso.com"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AuthServerAllowlist
  - Exemple de valeur :
``` xml
<string>*contoso.com,contoso.com</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DisableAuthNegotiateCnameLookup
  #### Désactiver la recherche CNAME lors de la négociation de l’authentification Kerberos
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Détermine si le SPN Kerberos généré est basé sur le nom DNS canonique (CNAME) ou sur le nom d’origine entré.

Si vous activez cette stratégie, la recherche CNAME est ignorée et le nom du serveur (tel qu'il a été entré) est utilisé.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, le nom canonique du serveur est utilisé. Ceci est déterminé via une recherche CNAME.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DisableAuthNegotiateCnameLookup
  - Nom de la stratégie de groupe: Désactiver la recherche CNAME lors de la négociation de l’authentification Kerberos
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Authentification HTTP
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DisableAuthNegotiateCnameLookup
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DisableAuthNegotiateCnameLookup
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### EnableAuthNegotiatePort
  #### Inclure le port non standard dans Kerberos SPN
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifie si le SPN Kerberos généré doit inclure un port non standard.

Si vous activez cette stratégie et si un utilisateur inclut un port non standard (un port différent de 80 ou 443) dans une URL, ce port est inclus dans le SPN Kerberos généré.

Si vous ne configurez pas ou si vous désactivez cette stratégie, le SPN Kerberos généré n’inclut de port dans aucun cas.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: EnableAuthNegotiatePort
  - Nom de la stratégie de groupe: Inclure le port non standard dans Kerberos SPN
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Authentification HTTP
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: EnableAuthNegotiatePort
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: EnableAuthNegotiatePort
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### NtlmV2Enabled
  #### Contrôler si l’authentification NTLMv2 est activée
  
  
  #### Versions prises en charge :
  - Sur macOS depuis 77 ou ultérieur

  #### Description
  Contrôle si NTLMv2 est activée.

Toutes les versions récentes des serveurs Samba et Windows prennent en charge NTLMv2. Vous ne devez désactiver NTLMv2 que pour résoudre les problèmes de compatibilité descendante, car elle réduit la sécurité de l’authentification.

Si vous ne configurez pas cette stratégie, NTLMv2 est activé par défaut.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  

  #### Paramètres et informations Mac
  - Nom de la clé de préférence: NtlmV2Enabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ## Cast policies

  [Revenir au début](#microsoft-edge---stratégies)

  ### EnableMediaRouter
  #### Activer Google Cast
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Activez cette stratégie pour activer Google Cast. Les utilisateurs seront en mesure de le lancer à partir du menu de l'application, des menus contextuels de page, des contrôles de media sur les sites sur lesquels Cast est activé, et de l'icône de la barre d'outils Cast (le cas échéant).

Désactivez cette stratégie pour désactiver Google Cast.

Par défaut, Google Cast est activé.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: EnableMediaRouter
  - Nom de la stratégie de groupe: Activer Google Cast
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Cast
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: EnableMediaRouter
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: EnableMediaRouter
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ShowCastIconInToolbar
  #### Afficher l’icône de diffusion dans la barre d’outils
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez cette stratégie sur true pour afficher l’icône de la barre d’outils Diffuser dans la barre d’outils ou le menu de dépassement de capacité. Les utilisateurs ne peuvent pas la supprimer.

Si vous ne configurez pas cette stratégie ou si vous la désactivez, les utilisateurs peuvent épingler ou supprimer l’icône à l’aide de son menu contextuel.

Si vous avez également défini la stratégie [EnableMediaRouter](#enablemediarouter) sur false, cette stratégie est ignorée et l’icône de la barre d’outils n’est pas affichée.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ShowCastIconInToolbar
  - Nom de la stratégie de groupe: Afficher l’icône de diffusion dans la barre d’outils
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Cast
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ShowCastIconInToolbar
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ShowCastIconInToolbar
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ## Démarrage&comma; page d’accueil et page Nouvel onglet policies

  [Revenir au début](#microsoft-edge---stratégies)

  ### HomepageIsNewTabPage
  #### Définir la page Nouvel onglet comme page d’accueil
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Configurer la page d’accueil par défaut dans Microsoft Edge. Vous pouvez définir la page d’accueil sur une URL spécifiée ou sur la page Nouvel onglet.

Si vous activez cette stratégie, la page Nouvel onglet est toujours utilisée pour la page d’accueil et l’emplacement de l’URL de la page d’accueil est ignoré.

Si vous désactivez cette stratégie, la page d’accueil de l’utilisateur ne peut pas être la page Nouvel onglet, sauf si l’URL est définie sur « edge://newtab ».

Si elle n’est pas configurée, les utilisateurs peuvent choisir si la page Nouvel onglet est leur page d’accueil.

Cette stratégie n'est disponible que sur les instances de Windows jointes à un domaine Microsoft Active Directory, instances de Windows 10 Professionnel ou Entreprise inscrites pour la gestion des appareils, ou les instances macOS qui sont gérées via la gestion des périphériques mobiles ou qui sont jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: HomepageIsNewTabPage
  - Nom de la stratégie de groupe: Définir la page Nouvel onglet comme page d’accueil
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Démarrage, page d’accueil et page Nouvel onglet
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Démarrage, page d’accueil et page Nouvel onglet
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: HomepageIsNewTabPage
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: HomepageIsNewTabPage
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### HomepageLocation
  #### Configurer l’URL de la page d’accueil
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Configurez l’URL de la page d’accueil par défaut dans Microsoft Edge.

La page d’accueil est la page ouverte par le bouton Accueil. Les pages qui s’ouvrent au démarrage sont contrôlées par les stratégies [RestoreOnStartup](#restoreonstartup).

Vous pouvez définir une URL ici ou définir la page d’accueil de manière à ouvrir le nouvel onglet. Si vous choisissez d’ouvrir le nouvel onglet, cette stratégie n’est pas appliquée.

Si vous activez cette stratégie, les utilisateurs ne peuvent pas modifier l’URL de la page d’accueil, mais ils peuvent choisir d’utiliser le nouvel onglet comme page d’accueil.

Si vous désactivez ou ne configurez pas ce paramètre de stratégie, les utilisateurs peuvent choisir leur propre page d’accueil, tant que la stratégie [HomepageIsNewTabPage](#homepageisnewtabpage) n’est pas activée.

Cette stratégie n'est disponible que sur les instances de Windows jointes à un domaine Microsoft Active Directory, les instances de Windows 10 Professionnel ou Entreprise inscrites pour la gestion des appareils, ou les instances macOS qui sont gérées via la gestion des périphériques mobiles ou qui sont jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: HomepageLocation
  - Nom de la stratégie de groupe: Configurer l’URL de la page d’accueil
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Démarrage, page d’accueil et page Nouvel onglet
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Démarrage, page d’accueil et page Nouvel onglet
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: HomepageLocation
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"https://www.contoso.com"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: HomepageLocation
  - Exemple de valeur :
``` xml
<string>https://www.contoso.com</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### NewTabPageAllowedBackgroundTypes
  #### Configurer les types d’arrière-plan autorisés pour la mise en page du nouvel onglet
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Vous pouvez configurer les types d’image d’arrière-plan qui sont autorisés dans la nouvelle mise en page d’onglets dans Microsoft Edge.

Si vous ne configurez pas cette stratégie, tous les types d’image d’arrière-plan dans la page nouvel onglet sont activés.

Mappage des options de stratégie :

* DisableImageOfTheDay (1) = Désactiver les types d’images d’arrière-plan quotidien

* DisableCustomImage (2) = Désactiver le type d’image d’arrière-plan personnalisée

* DisableAll (3) = Désactiver tous les types d’images d’arrière-plan

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: NewTabPageAllowedBackgroundTypes
  - Nom de la stratégie de groupe: Configurer les types d’arrière-plan autorisés pour la mise en page du nouvel onglet
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Démarrage, page d’accueil et page Nouvel onglet
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: NewTabPageAllowedBackgroundTypes
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: NewTabPageAllowedBackgroundTypes
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### NewTabPageCompanyLogo
  #### Définir un nouvel onglet pour le logo de l'entreprise (obsolète)
  
  >OBSOLÈTE : cette stratégie est obsolète et ne fonctionne pas après Microsoft Edge85.
  #### Versions prises en charge :
  - Sur Windows et macOS depuis le 79, jusqu’au 85

  #### Description
  Cette stratégie ne fonctionnait comme prévu en raison de modifications apportées aux exigences opérationnelles. Elle est donc déconseillée et nous recommandons de ne pas l'utiliser.

Spécifie le logo de la société à utiliser sur le nouvel onglet dans Microsoft Edge.

La stratégie doit être configurée en tant que chaîne qui exprime le(s) logo(s) au format JSON. Par exemple : { "default_logo": { "url": "https://www.contoso.com/logo.png", "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29" }, "light_logo" : { "url": "https://www.contoso.com/light_logo.png", "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737" } }

Pour configurer cette stratégie, spécifiez l’URL à partir de laquelle Microsoft Edge peut télécharger le logo et son hachage de chiffrement (SHA-256), qui permet de vérifier l’intégrité du téléchargement. Le logo doit être au format PNG ou SVG et sa taille de fichier ne doit pas dépasser 16 Mo. Le logo est téléchargé et mis en cache. Il est téléchargé de nouveau lors de chaque modification de l’URL ou du hachage. L’URL doit être accessible sans authentification.

Le « default_logo » est obligatoire et est utilisé lorsqu’il n’y a pas d’image d’arrière-plan. Si « light_logo » est spécifié, il est utilisé lorsque le nouvel onglet de l’utilisateur a une image d’arrière-plan. Nous vous conseillons d’utiliser un logo horizontal avec un arrière-plan transparent aligné à gauche et centré verticalement. Le logo doit avoir une hauteur minimale de 32pixels et des proportions de 1:1 à 4:1. Le « default_logo » doit avoir un contraste approprié avec un arrière-plan blanc/noir, tandis que le « light_logo » doit avoir un contraste correct par rapport à une image d’arrière-plan.

Si vous activez cette stratégie, Microsoft Edge télécharge et affiche le(s) logo(s) spécifié(s) sur le nouvel onglet. Les utilisateurs ne peuvent pas remplacer ni masquer le(s) logo(s).

Si vous désactivez cette stratégie ou si vous ne la configurez pas, Microsoft Edge n’affiche pas de logo de la société ni de logo Microsoft sur le nouvel onglet.

Pour obtenir de l’aide sur la détermination du hachage SHA-256, voir https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/get-filehash.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Dictionnaire

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: NewTabPageCompanyLogo
  - Nom de la stratégie de groupe: Définir un nouvel onglet pour le logo de l'entreprise (obsolète)
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Démarrage, page d’accueil et page Nouvel onglet
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: NewTabPageCompanyLogo
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
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


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: NewTabPageCompanyLogo
  - Exemple de valeur :
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
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### NewTabPageHideDefaultTopSites
  #### Masquer les sites populaires par défaut à partir du nouvel onglet
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Masque les sites populaires par défaut à partir du nouvel onglet dans Microsoft Edge.

Si vous définissez cette stratégie sur true, les vignettes de site populaire par défaut sont masquées.

Si vous définissez cette stratégie sur false ou si vous ne la configurez pas, les vignettes de site populaire par défaut restent visibles.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: NewTabPageHideDefaultTopSites
  - Nom de la stratégie de groupe: Masquer les sites populaires par défaut à partir du nouvel onglet
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Démarrage, page d’accueil et page Nouvel onglet
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: NewTabPageHideDefaultTopSites
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: NewTabPageHideDefaultTopSites
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### NewTabPageLocation
  #### Configurer l’URL du nouvel onglet
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Configure l’URL par défaut du nouvel onglet.

 Cette stratégie détermine la page ouverte lors de la création d’onglets (notamment à l’ouverture de nouvelles fenêtres). Elle affecte également la page de démarrage si elle est définie de manière à s'ouvrir dans le nouvel onglet.

 Cette stratégie ne détermine pas la page qui s’ouvre au démarrage ; cela est contrôlé par la stratégie [RestoreOnStartup](#restoreonstartup). Elle n’affecte pas non plus la page d’accueil si celle-ci est définie de manière à s'ouvrir dans le nouvel onglet.licy. It also doesn't affect the home page if that's set to open to the new tab page.

 Si vous ne configurez pas cette stratégie, le nouvel onglet par défaut est utilisé.

 Si vous configurez cette stratégie *et* la stratégie [NewTabPageSetFeedType](#newtabpagesetfeedtype), cette stratégie est prioritaire.

Si une URL non valide est fournie, les nouveaux onglets ouvrent about://blank.

 Cette stratégie n’est disponible que sur les instances de Windows qui sont jointes à un domaine Microsoft Active Directory, les instances de Windows 10 Professionnel ou Entreprise qui sont inscrites pour la gestion des périphériques, ou les instances macOS qui sont gérées via la gestion des périphériques mobiles ou qui sont jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: NewTabPageLocation
  - Nom de la stratégie de groupe: Configurer l’URL du nouvel onglet
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Démarrage, page d’accueil et page Nouvel onglet
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Démarrage, page d’accueil et page Nouvel onglet
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: NewTabPageLocation
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"https://www.fabrikam.com"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: NewTabPageLocation
  - Exemple de valeur :
``` xml
<string>https://www.fabrikam.com</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### NewTabPageManagedQuickLinks
  #### Définir les liens rapides du nouvel onglet
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 79 ou version ultérieure

  #### Description
  Par défaut, Microsoft Edge affiche les liens rapides du nouvel onglet à partir des raccourcis ajoutés par l’utilisateur et des sites récurrents en fonction de l’historique de navigation. Grâce à cette stratégie, vous pouvez configurer jusqu’à 3 vignettes de liens rapides sur le nouvel onglet, exprimées sous forme d’objet JSON :

 [ { "url": "https://www.contoso.com", "title": "Contoso Portal", "pinned": true/false }, ... ]

Le champ « URL » est obligatoire ; les éléments « title » et « pinned » sont facultatifs. Si « title » n’est pas spécifié, l’URL est utilisée comme titre par défaut. Si « pinned » n’est pas spécifié, la valeur par défaut est « false ».

Microsoft Edge présente celles-ci dans l’ordre listé, de gauche à droite, en affichant les vignettes épinglées avant celles qui ne le sont pas.

Si la stratégie est définie comme obligatoire, le champ « pinned » est ignoré et toutes les vignettes sont épinglées. Les vignettes ne peuvent pas être supprimées par l’utilisateur et apparaissent toujours au début de la liste des liens rapides.

Lorsque la stratégie est recommandée, les vignettes épinglées sont conservées dans la liste, mais l’utilisateur peut les modifier et les supprimer. Les vignettes de lien rapide qui ne sont pas épinglées se comportent comme des sites récurrents par défaut et sont exclues de la liste si d’autres sites web sont visités plus fréquemment. Lorsque cette stratégie applique à un profil de navigateur existant des liens qui ne sont pas épinglés, il est possible que ces liens n’apparaissent pas, selon la façon dont ils sont classés par rapport à l’historique de navigation de l’utilisateur.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Dictionnaire

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: NewTabPageManagedQuickLinks
  - Nom de la stratégie de groupe: Définir les liens rapides du nouvel onglet
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Démarrage, page d’accueil et page Nouvel onglet
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Démarrage, page d’accueil et page Nouvel onglet
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: NewTabPageManagedQuickLinks
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
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


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: NewTabPageManagedQuickLinks
  - Exemple de valeur :
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
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### NewTabPagePrerenderEnabled
  #### Activer le préchargement de la page Nouvel onglet pour un rendu plus rapide
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 85 ou version ultérieure

  #### Description
  Si vous configurez cette stratégie, le préchargement de la page Nouvel onglet est activé et les utilisateurs ne peuvent pas modifier ce paramètre. Si vous ne configurez pas cette stratégie, le préchargement est désactivé et un utilisateur peut modifier ce paramètre.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: NewTabPagePrerenderEnabled
  - Nom de la stratégie de groupe: Activer le préchargement de la page Nouvel onglet pour un rendu plus rapide
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Démarrage, page d’accueil et page Nouvel onglet
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Démarrage, page d’accueil et page Nouvel onglet
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: NewTabPagePrerenderEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: NewTabPagePrerenderEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### NewTabPageSetFeedType
  #### Configurer l’expérience de nouvel onglet Microsoft Edge
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 79 ou version ultérieure

  #### Description
  Vous permet de choisir l’expérience de flux Microsoft News ou Office 365 pour le nouvel onglet.

Si vous définissez cette stratégie sur News, les utilisateurs voient l’expérience de flux Microsoft News sur la nouvelle page onglet.

Si vous définissez cette stratégie sur Office, les utilisateurs disposant d’une connexion au navigateur Azure Active Directory voient l’expérience de flux Office 365 sur le nouvel onglet.

Si vous désactivez cette stratégie ou si vous ne la configurez pas :

- Les utilisateurs disposant d’une connexion au navigateur Azure Active Directory se voient proposer l’expérience de flux de nouvel onglet Office 365, ainsi que l’expérience de flux de nouvel onglet standard.

-        Les utilisateurs sans connexion au navigateur Azure Active Directory voient l’expérience de nouvel onglet standard.

Si vous configurez cette stratégie *et* la stratégie [NewTabPageLocation](#newtabpagelocation), [NewTabPageLocation](#newtabpagelocation) est prioritaire.

Paramètre par défaut : désactivé ou non configuré.

Mappage des options de stratégie :

* News (0) = Expérience de flux Microsoft News

* Office (1) = Expérience de flux Office 365

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: NewTabPageSetFeedType
  - Nom de la stratégie de groupe: Configurer l’expérience de nouvel onglet Microsoft Edge
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Démarrage, page d’accueil et page Nouvel onglet
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Démarrage, page d’accueil et page Nouvel onglet
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: NewTabPageSetFeedType
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: NewTabPageSetFeedType
  - Exemple de valeur :
``` xml
<integer>0</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### RestoreOnStartup
  #### Action à exécuter au démarrage
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifiez la façon dont Microsoft Edge se comporte lorsqu’il démarre.

Si vous voulez qu'un nouvel onglet s'ouvre toujours au démarrage, sélectionnez « RestoreOnStartupIsNewTabPage ».

Si vous voulez rouvrir des URL ouvertes lors de la dernière fermeture de Microsoft Edge, sélectionnez « RestoreOnStartupIsLastSession ». La session de navigation est restaurée telle qu'elle était. Notez que cette option désactive certains paramètres qui s’appuient sur des sessions ou qui effectuent des actions à la fermeture (telles qu'effacer les données de navigation en quittant ou les cookies de session uniquement).

Si vous voulez ouvrir un ensemble spécifique d’URL, choisissez « RestoreOnStartupIsURLs » .

La désactivation de ce paramètre revient à le laisser non configuré. Les utilisateurs peuvent le modifier dans Microsoft Edge.

Cette stratégie n'est disponible que sur les instances de Windows jointes à un domaine Microsoft Active Directory, les instances de Windows 10 Professionnel ou Entreprise inscrites pour la gestion des appareils, ou les instances macOS qui sont gérées via la gestion des périphériques mobiles ou qui sont jointes à un domaine via MCX.

Mappage des options de stratégie :

* RestoreOnStartupIsNewTabPage (5) = Ouvrir un nouvel onglet

* RestoreOnStartupIsLastSession (1) = Restaurer la dernière session

* RestoreOnStartupIsURLs (4) = Ouvrir la liste des URL

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: RestoreOnStartup
  - Nom de la stratégie de groupe: Action à exécuter au démarrage
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Démarrage, page d’accueil et page Nouvel onglet
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Démarrage, page d’accueil et page Nouvel onglet
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: RestoreOnStartup
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000004
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: RestoreOnStartup
  - Exemple de valeur :
``` xml
<integer>4</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### RestoreOnStartupURLs
  #### Sites à ouvrir au démarrage du navigateur
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifiez la liste des sites web à ouvrir automatiquement au démarrage du navigateur. Si vous ne configurez pas cette stratégie, aucun site n’est ouvert au démarrage.

Cette stratégie ne fonctionne que si vous définissez également la stratégie [RestoreOnStartup](#restoreonstartup) pour « Ouvrir une liste d’URL » (4).

Cette stratégie n’est disponible que sur les instances de Windows qui sont jointes à un domaine Microsoft Active Directory, instances de Windows 10 Professionnel ou Entreprise inscrites pour la gestion des appareils, ou les instances macOS qui sont gérées via la gestion des périphériques mobiles ou qui sont jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: RestoreOnStartupURLs
  - Nom de la stratégie de groupe: Sites à ouvrir au démarrage du navigateur
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Démarrage, page d’accueil et page Nouvel onglet
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Démarrage, page d’accueil et page Nouvel onglet
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé\RestoreOnStartupURLs
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\1 = "https://contoso.com"
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\2 = "https://www.fabrikam.com"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: RestoreOnStartupURLs
  - Exemple de valeur :
``` xml
<array>
  <string>https://contoso.com</string>
  <string>https://www.fabrikam.com</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ShowHomeButton
  #### Afficher le bouton Accueil sur la barre d’outils
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Affiche le bouton Accueil dans la barre d'outils de Microsoft Edge.

	Activez cette stratégie pour toujours afficher le bouton Accueil. Désactivez-la pour ne jamais afficher le bouton.

	Si vous ne configurez pas la stratégie, les utilisateurs peuvent choisir s’il veulent afficher le bouton Accueil.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ShowHomeButton
  - Nom de la stratégie de groupe: Afficher le bouton Accueil sur la barre d’outils
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Démarrage, page d’accueil et page Nouvel onglet
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Démarrage, page d’accueil et page Nouvel onglet
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: ShowHomeButton
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ShowHomeButton
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ## Extensions policies

  [Revenir au début](#microsoft-edge---stratégies)

  ### ExtensionAllowedTypes
  #### Configurer les types d’extensions autorisées
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Détermine les types d’extensions qui peuvent être installés et limite l’accès au runtime.

Ce paramètre définit les types autorisés d'extensions et les hôtes avec lesquels elles peuvent interagir. La valeur est une liste de chaînes, dont chacune doit être l'une des valeurs suivantes : « extension », « theme », « user_script » et « hosted_app ». Voir la documentation sur les extensions de Microsoft Edge pour plus d’informations sur ces types.

Notez que cette stratégie affecte également les extensions à installer de force à l'aide de la stratégie [ExtensionInstallForcelist](#extensioninstallforcelist).

Si vous activez cette stratégie, seules les extensions qui correspondent à un type de la liste sont installées.

Si vous ne configurez pas cette stratégie, aucune restriction sur les types d’extensions acceptables n’est appliquée.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ExtensionAllowedTypes
  - Nom de la stratégie de groupe: Configurer les types d’extensions autorisées
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Extensions
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes\1 = "hosted_app"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ExtensionAllowedTypes
  - Exemple de valeur :
``` xml
<array>
  <string>hosted_app</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ExtensionInstallAllowlist
  #### Autoriser l'installation d'extensions spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Par défaut, toutes les extensions sont autorisées. Toutefois, si vous bloquez toutes les extensions en définissant la stratégie « ExtensionInstallBlockList » sur « * », les utilisateurs ne peuvent installer que les extensions définies dans cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ExtensionInstallAllowlist
  - Nom de la stratégie de groupe: Autoriser l'installation d'extensions spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Extensions
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\2 = "extension_id2"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ExtensionInstallAllowlist
  - Exemple de valeur :
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ExtensionInstallBlocklist
  #### Contrôler les extensions impossibles à installer
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Répertoriez des extensions spécifiques que les utilisateurs ne peuvent PAS installer dans Microsoft Edge. Lorsque vous déployez cette stratégie, toutes les extensions de cette liste qui ont été installées précédemment sont désactivées et l’utilisateur ne peut pas les activer. Si vous supprimez un élément de la liste des extensions bloquées, cette extension est automatiquement réactivée partout où elle a déjà été installée.

	Utilisez « * » pour bloquer toutes les extensions qui ne sont pas répertoriées de façon explicite dans la liste verte.

	Si vous ne configurez pas cette stratégie, les utilisateurs peuvent installer toutes les extensions de Microsoft Edge.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ExtensionInstallBlocklist
  - Nom de la stratégie de groupe: Contrôler les extensions impossibles à installer
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Extensions
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\2 = "extension_id2"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ExtensionInstallBlocklist
  - Exemple de valeur :
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ExtensionInstallForcelist
  #### Contrôler les extensions qui sont installées en mode silencieux
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifie les extensions installées en mode silencieux, sans intervention de l’utilisateur, et que les utilisateurs ne peuvent pas désinstaller ou désactiver («installées de force»). Toutes les autorisations demandées par les extensions sont implicitement accordées sans intervention de l’utilisateur, y compris les autorisations supplémentaires demandées par les futures versions de l’extension. En outre, les autorisations sont accordées pour les API d’extension enterprise.deviceAttributes et enterprise.platformKeys. (Ces deux API sont uniquement disponibles pour les extensions qui sont installées de force.)

Cette stratégie est prioritaire sur une stratégie [ExtensionInstallBlocklist](#extensioninstallblocklist) potentiellement en conflit. Lorsque vous enlevez une extension sur la liste des extensions installées de force, elle est automatiquement désinstallée par Microsoft Edge.

L'installation forcée est limitée aux applications et extensions listées sur le site web des modules complémentaires de Microsoft Edge pour les cas qui ne sont pas les suivants : les instances Windows qui sont jointes à un domaine Microsoft Active Directory, ou les instances Windows 10 Pro ou Enterprise qui se sont inscrites pour la gestion des appareils, et les instances MacOS qui sont gérées via MDM ou jointes à un domaine via MCX.

Notez que les utilisateurs peuvent modifier le code source de n’importe quelle extension à l’aide des outils de développement, ce qui risque d'engendrer des dysfonctionnements de l’extension. S’il s’agit d’un problème, définissez la stratégie [DeveloperToolsAvailability](#developertoolsavailability).

Utilisez le format suivant pour ajouter une extension à la liste:

[extensionID];[updateURL]

-extensionID: chaîne de 32 lettres trouvée dans edge://extensions en mode développeur.

- updateURL (facultatif) est l’adresse du document XML de manifeste de la mise à jour pour l’application ou l’extension, comme décrit dans [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043). Si vous voulez installer un extension depuis Chrome Web Store, fournissez l’URL de mise à jour Chrome Web Store https://clients2.google.com/service/update2/crx. Notez que l’URL de la mise à jour définie dans cette stratégie n'est utilisée que pour l’installation initiale; les mises à jour suivantes de l’extension utilisent l’URL de la mise à jour indiquée dans le manifeste de l’extension. Si vous ne définissez pas l’URL de mise à jour, l’extension est supposée être hébergée dans le Microsoft Store et l’URL de mise à jour suivante est utilisée (https://edge.microsoft.com/extensionwebstorebase/v1/crx).

 Par exemple, gggmmkjegpiggikcnhidnjjhmicpibll;https://edge.microsoft.com/extensionwebstorebase/v1/crx installe l’application Microsoft Online à partir de l’URL de «mise à jour» du Microsoft Store. Pour plus d’informations sur l’hébergement d’extensions, voir: [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043).

Si vous ne configurez pas cette stratégie, aucune extension n’est installée automatiquement et les utilisateurs peuvent désinstaller les extensions de Microsoft Edge.
Notez que cette stratégie ne s’applique pas au mode InPrivate.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ExtensionInstallForcelist
  - Nom de la stratégie de groupe: Contrôler les extensions qui sont installées en mode silencieux
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Extensions
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\1 = "gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\2 = "abcdefghijklmnopabcdefghijklmnop"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ExtensionInstallForcelist
  - Exemple de valeur :
``` xml
<array>
  <string>gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx</string>
  <string>abcdefghijklmnopabcdefghijklmnop</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ExtensionInstallSources
  #### Configurer l’extension et les sources d’installation du script utilisateur
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez les URL qui peuvent installer des extensions et des thèmes.

Par défaut, les utilisateurs doivent télécharger un fichier *.crx pour chaque extension ou script qu’ils souhaitent installer, puis le faire glisser sur la page Paramètres de Microsoft Edge. Cette stratégie permet aux URL spécifiques d’installer l’extension ou le script pour l’utilisateur.

Chaque élément de cette liste est un modèle de correspondance de type extension (voir [https://go.microsoft.com/fwlink/?linkid=2095039](https://go.microsoft.com/fwlink/?linkid=2095039)). Les utilisateurs peuvent facilement installer des éléments à partir de n’importe quelle URL qui correspond à un élément de cette liste. L’emplacement du fichier *.crx et la page depuis laquelle le téléchargement est lancé (en d’autres termes, le référent) doivent être autorisés par ces modèles.

La stratégie [ExtensionInstallBlocklist](#extensioninstallblocklist) est prioritaire sur cette stratégie. Les extensions de la liste rouge ne sont pas installées, même si elles proviennent d’un site de cette liste.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ExtensionInstallSources
  - Nom de la stratégie de groupe: Configurer l’extension et les sources d’installation du script utilisateur
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Extensions
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources\1 = "https://corp.contoso.com/*"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ExtensionInstallSources
  - Exemple de valeur :
``` xml
<array>
  <string>https://corp.contoso.com/*</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ExtensionSettings
  #### Configurer les paramètres de gestion des extensions
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Configurer les paramètres de gestion d’extension de Microsoft Edge.

	Cette stratégie contrôle plusieurs paramètres, y compris les paramètres contrôlés par des stratégies existantes relatives à l’extension. Cette stratégie remplace les stratégies héritées si les deux sont définies.

	Cette stratégie mappe un ID d’extension ou une URL de mise à jour avec sa configuration. Avec un ID d’extension, la configuration s’applique uniquement à l’extension spécifiée. Définissez une configuration par défaut pour l’ID spécial « * » à appliquer à toutes les extensions qui ne sont pas spécifiquement répertoriées dans cette stratégie. Avec une URL de mise à jour, la configuration s’applique à toutes les extensions avec l’URL de mise à jour exact indiqué dans le manifeste de cette extension, comme décrit dans [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Dictionnaire

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ExtensionSettings
  - Nom de la stratégie de groupe: Configurer les paramètres de gestion des extensions
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Extensions
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ExtensionSettings
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
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


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ExtensionSettings
  - Exemple de valeur :
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
  

  [Revenir au début](#microsoft-edge---stratégies)

  ## Gestionnaire de mot de passe et protection policies

  [Revenir au début](#microsoft-edge---stratégies)

  ### PasswordManagerEnabled
  #### Activer l’enregistrement des mots de passe pour le Gestionnaire de mot de passe
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Activez Microsoft Edge pour enregistrer les mots de passe utilisateur.

	Si vous activez cette stratégie, les utilisateurs peuvent enregistrer leurs mots de passe Microsoft Edge. Lors de leur prochaine visite du site, Microsoft Edge entre automatiquement le mot de passe.

	Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas enregistrer de nouveaux mots de passe, mais ils peuvent toujours utiliser les mots de passe enregistrés précédemment.

	Si vous activez ou désactivez cette stratégie, les utilisateurs ne peuvent pas la modifier ni la remplacer dans Microsoft Edge. Si vous ne la configurez pas, les utilisateurs peuvent enregistrer les mots de passe, ainsi que désactiver cette fonctionnalité.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PasswordManagerEnabled
  - Nom de la stratégie de groupe: Activer l’enregistrement des mots de passe pour le Gestionnaire de mot de passe
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Gestionnaire de mot de passe et protection
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Gestionnaire de mot de passe et protection
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: PasswordManagerEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PasswordManagerEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PasswordMonitorAllowed
  #### Autoriser les utilisateurs à être avertis si leur mot de passe est considéré comme non sécurisé
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 85 ou ultérieur

  #### Description
  Autoriser Microsoft Edge à surveiller les mots de passe des utilisateurs.

Si vous activez cette stratégie et qu’un utilisateur consent à activer la stratégie, l’utilisateur reçoit une alerte si l’un de ses mots de passe stockés dans Microsoft Edge est considéré comme non sécurisé. Microsoft Edge affiche une alerte. Ces informations sont également disponibles dans Paramètres > Mots de passe > Surveillance de mot de passe.

Si vous désactivez cette stratégie, les utilisateurs ne sont pas invités à autoriser l’activation de cette fonctionnalité. Les mots de passe ne seront pas analysés et ne seront pas non plus signalés.

Si vous activez ou ne configurez pas la stratégie, les utilisateurs peuvent activer ou désactiver cette fonctionnalité.

Si vous souhaitez en savoir plus sur la manière dont Microsoft Edge détermine que des mots de passe ne sont pas sécurisés, veuillez consulter [https://go.microsoft.com/fwlink/?linkid=2133833](https://go.microsoft.com/fwlink/?linkid=2133833)

Conseils supplémentaires :

Cette stratégie peut être configurée comme étant Recommandée et Obligatoire, mais avec une légende importante.

Obligatoire activé : étant donné que le consentement de l’utilisateur individuel est une condition préalable à l’activation de cette fonctionnalité pour un utilisateur donné, cette stratégie ne dispose pas de paramètre Obligatoire activé. Si la stratégie est configurée sur Obligatoire, l’interface utilisateur dans les Paramètres ne change pas et le message d’erreur suivant s’affiche dans edge://policy

Exemple de message d’état d’erreur : « Cette valeur de stratégie est ignorée parce que le Moniteur de mot de passe nécessite le consentement de l’utilisateur individuel pour qu’il soit activé. Vous pouvez demander aux utilisateurs au sein de votre organisation d’accéder à Paramètres > Profils > Mots de passe, puis d’activer la fonctionnalité. »

Recommandé activé : si la stratégie est configurée sur Recommandée activé, l’interface utilisateur dans les Paramètres demeure en mode « Désactivé », mais une icône porte-documents est affichée en regard de celle-ci avec cette description affichée par pointage – « Votre organisation recommande une valeur spécifique pour ce paramètre et vous avez choisi une autre valeur »

Obligatoire et Recommandée désactivé : ces deux états fonctionnent normalement, avec les légendes habituelles visibles par les utilisateurs.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PasswordMonitorAllowed
  - Nom de la stratégie de groupe: Autoriser les utilisateurs à être avertis si leur mot de passe est considéré comme non sécurisé
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Gestionnaire de mot de passe et protection
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Gestionnaire de mot de passe et protection
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: PasswordMonitorAllowed
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PasswordProtectionChangePasswordURL
  #### Configurer l’URL de modification du mot de passe
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Configure l’URL de modification du mot de passe (schémas HTTP et HTTPS uniquement).

Le service de protection par mot de passe redirige les utilisateurs vers cette URL pour modifier leur mot de passe après l'affichage d'un avertissement dans le navigateur.

Si vous activez cette stratégie, le service de protection par mot de passe redirige les utilisateurs vers cette URL pour modifier leur mot de passe.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, le service de protection par mot de passe ne redirige pas les utilisateurs vers une URL de modification du mot de passe.

Cette stratégie est disponible uniquement sur les instances de Windows jointes à un domaine Microsoft Active Directory, instances de Windows 10 Professionnel ou Entreprise inscrites pour la gestion des appareils, ou les instances macOS qui sont gérées via la gestion des périphériques mobiles ou qui sont jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PasswordProtectionChangePasswordURL
  - Nom de la stratégie de groupe: Configurer l’URL de modification du mot de passe
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Gestionnaire de mot de passe et protection
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: PasswordProtectionChangePasswordURL
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"https://contoso.com/change_password.html"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PasswordProtectionChangePasswordURL
  - Exemple de valeur :
``` xml
<string>https://contoso.com/change_password.html</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PasswordProtectionLoginURLs
  #### Configurer la liste des URL de connexion d’entreprise dans lesquelles le service de protection par mot de passe doit capturer les hachages salés d’un mot de passe
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Configurez la liste des URL de connexion d’entreprise (modèles HTTP et HTTPs uniquement) où Microsoft Edge doit capturer les hachages salés de mots de passe et les utiliser pour la détection de la réutilisation de mot de passe.

Si vous activez cette stratégie, le service de protection par mot de passe capture les empreintes de mots de passe dans les URL définies.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, aucune empreinte de mot de passe n’est capturée.

Cette stratégie est disponible uniquement sur les instances Windows qui sont jointes à un domaine de Microsoft Active Directory, des instances Windows 10 Professionnel ou Windows 10 Entreprise inscrites pour la gestion des périphériques, ou les instances macOS qui sont gérées via la gestion des données de référence ou qui sont jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PasswordProtectionLoginURLs
  - Nom de la stratégie de groupe: Configurer la liste des URL de connexion d’entreprise dans lesquelles le service de protection par mot de passe doit capturer les hachages salés d’un mot de passe
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Gestionnaire de mot de passe et protection
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\1 = "https://contoso.com/login.html"
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\2 = "https://login.contoso.com"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PasswordProtectionLoginURLs
  - Exemple de valeur :
``` xml
<array>
  <string>https://contoso.com/login.html</string>
  <string>https://login.contoso.com</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PasswordProtectionWarningTrigger
  #### Configurer le déclencheur d'avertissement de protection par mot de passe
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Vous permet de contrôler quand déclencher un avertissement de protection du mot de passe. La protection de mot de passe avertit les utilisateurs lorsqu'ils réutilisent leur mot de passe protégé sur des sites potentiellement suspects.

Vous pouvez utiliser les stratégies [PasswordProtectionLoginURLs](#passwordprotectionloginurls) et [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl) pour configurer les mots de passe à protéger.

  Exceptions : les mots de passe des sites listés dans [PasswordProtectionLoginURLs](#passwordprotectionloginurls) et [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl), ainsi que des sites listés dans [SmartScreenAllowListDomains](#smartscreenallowlistdomains) ne déclenchent pas d’avertissement de protection du mot de passe.

Définissez sur « PasswordProtectionWarningOff » pour ne pas afficher les avertissements de protection de mot de passe.

Définissez sur « PasswordProtectionWarningOnPasswordReuse » pour afficher les avertissements de protection de mot de passe lorsque l’utilisateur réutilise son mot de passe protégé sur un site non autorisé.

Si vous désactivez ou ne configurez pas cette stratégie, le déclencheur d’avertissement ne s'affiche pas.

Mappage des options de stratégie :

* PasswordProtectionWarningOff (0) = Avertissement relatif à la protection par mot de passe désactivé

* PasswordProtectionWarningOnPasswordReuse (1) = L'avertissement de protection de mot de passe est déclenché par la réutilisation du mot de passe

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PasswordProtectionWarningTrigger
  - Nom de la stratégie de groupe: Configurer le déclencheur d'avertissement de protection par mot de passe
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Gestionnaire de mot de passe et protection
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: PasswordProtectionWarningTrigger
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PasswordProtectionWarningTrigger
  - Exemple de valeur :
``` xml
<integer>1</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ## Impression policies

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultPrinterSelection
  #### Règles de sélection d’imprimante par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Remplace les règles de sélection d’imprimante par défaut de Microsoft Edge. Cette stratégie détermine les règles pour la sélection de l’imprimante par défaut dans Microsoft Edge qui doit être effectuée la première fois qu'un utilisateur essaie d’imprimer une page.

	Lorsque cette stratégie est définie, Microsoft Edge tente de trouver une imprimante qui correspond à tous les attributs spécifiés et l’utilise comme imprimante par défaut. Si plusieurs imprimantes remplissent les critères, la première imprimante correspondante est utilisée.

	Si vous ne configurez pas cette stratégie ou si aucune imprimante correspondante n'est détectée dans le délai imparti, l’imprimante est définie par défaut sur l’imprimante PDF intégrée ou sur aucune imprimante si l’imprimante PDF n’est pas disponible.

	La valeur est analysée en tant qu’objet JSON, conformément au schéma suivant : { "type": "object", "properties": { "idPattern": { "description": "Regular expression to match printer id.", "type": "string" }, "namePattern": { "description": "Regular expression to match printer display name.", "type": "string" } } }

	L'omission d'un champ signifie que toutes les valeurs correspondent ; par exemple, si vous ne spécifiez pas la connectivité, l'Aperçu avant impression démarre la découverte de tous les types d’imprimantes locales. Les modèles d’expressions régulières doivent respecter la syntaxe JavaScript RegExp et les correspondances respectent la casse.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultPrinterSelection
  - Nom de la stratégie de groupe: Règles de sélection d’imprimante par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Impression
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DefaultPrinterSelection
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"{ \"idPattern\": \".*public\", \"namePattern\": \".*Color\" }"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultPrinterSelection
  - Exemple de valeur :
``` xml
<string>{ "idPattern": ".*public", "namePattern": ".*Color" }</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PrintHeaderFooter
  #### Imprimer des en-têtes et des pieds de page
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Forcez l'activation ou la désactivation des « en-têtes et pieds de page » dans la boîte de dialogue d’impression.

Si vous ne configurez pas cette stratégie, les utilisateurs peuvent décider d’imprimer les en-têtes et pieds de page.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas imprimer les en-têtes et pieds de page.

Si vous activez cette stratégie, les utilisateurs peuvent toujours imprimer les en-têtes et pieds de page.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PrintHeaderFooter
  - Nom de la stratégie de groupe: Imprimer des en-têtes et des pieds de page
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Impression
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Impression
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: PrintHeaderFooter
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PrintHeaderFooter
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PrintPreviewUseSystemDefaultPrinter
  #### Définir l’imprimante système par défaut en tant qu’imprimante par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Indique à Microsoft Edge d'utiliser l’imprimante système par défaut en tant qu’option par défaut dans l’aperçu avant impression à la place de l’imprimante la plus récemment utilisée.

	Si vous désactivez cette stratégie ou si vous ne la configurez pas, l'aperçu avant impression utilise l’imprimante la plus récemment utilisée comme option de destination par défaut.

	Si vous activez cette stratégie, l'aperçu avant impression utilise l’imprimante par défaut du système d’exploitation comme option de destination par défaut.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PrintPreviewUseSystemDefaultPrinter
  - Nom de la stratégie de groupe: Définir l’imprimante système par défaut en tant qu’imprimante par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Impression
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Impression
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: PrintPreviewUseSystemDefaultPrinter
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PrintPreviewUseSystemDefaultPrinter
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PrintingEnabled
  #### Activer l’impression
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Active l’impression dans Microsoft Edge et empêche les utilisateurs de modifier ce paramètre.

	Si vous activez cette stratégie ou ne la configurez pas, les utilisateurs peuvent imprimer.

	Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas imprimer à partir de Microsoft Edge. L’impression est désactivée dans le menu clé, les extensions, les applications JavaScript, etc. Les utilisateurs peuvent toujours imprimer à partir de plug-ins qui n’utilisent pas Microsoft Edge lors de l’impression. Par exemple, certaines applications Adobe Flash présentent l'option d’impression dans leur menu contextuel, ce qui n’est pas couvert par cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PrintingEnabled
  - Nom de la stratégie de groupe: Activer l’impression
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Impression
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: PrintingEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PrintingEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PrintingPaperSizeDefault
  #### Taille de la page d’impression par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Remplace la taille de la page d’impression par défaut.

name doit contenir l’un des formats répertoriés ou « personnalisé » si la taille de papier requise ne figure pas dans la liste. Si la valeur « personnalisé » est indiquée, propriété custom_size doit être spécifiée. Il décrit la hauteur et la largeur souhaitées en micromètres. Sinon propriété custom_size ne doit pas être spécifiée. La stratégie qui viole ces règles est ignorée.

Si la taille de page n’est pas disponible sur l’imprimante choisie par l’utilisateur, cette stratégie est ignorée.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Dictionnaire

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PrintingPaperSizeDefault
  - Nom de la stratégie de groupe: Taille de la page d’impression par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Impression
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: PrintingPaperSizeDefault
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\PrintingPaperSizeDefault = {
  "custom_size": {
    "height": 297000, 
    "width": 210000
  }, 
  "name": "custom"
}
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PrintingPaperSizeDefault
  - Exemple de valeur :
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
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### UseSystemPrintDialog
  #### Imprimer à l’aide de la boîte de dialogue d’impression système
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Affiche la boîte de dialogue d’impression système au lieu de l’aperçu avant impression.

	Si vous activez cette stratégie, Microsoft Edge ouvre la boîte de dialogue d’impression système à la place de l’aperçu avant impression intégré lorsque l’utilisateur imprime une page.

	Si vous ne configurez pas ou si vous désactivez cette stratégie, les commandes d’impression déclenchent l'écran Aperçu avant impression de Microsoft Edge.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: UseSystemPrintDialog
  - Nom de la stratégie de groupe: Imprimer à l’aide de la boîte de dialogue d’impression système
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Impression
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: UseSystemPrintDialog
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: UseSystemPrintDialog
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ## Messagerie native policies

  [Revenir au début](#microsoft-edge---stratégies)

  ### NativeMessagingAllowlist
  #### Contrôle des hôtes de messagerie natifs pouvant être utilisés par les utilisateurs
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Listez les hôtes de messagerie natifs spécifiques que les utilisateurs peuvent utiliser dans Microsoft Edge.

Par défaut, tous les hôtes de messagerie natifs sont autorisés. Si vous définissez la stratégie [NativeMessagingBlocklist](#nativemessagingblocklist) sur *, tous les hôtes de messagerie natifs sont bloqués et seuls ceux qui sont répertoriés ici sont chargés.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: NativeMessagingAllowlist
  - Nom de la stratégie de groupe: Contrôle des hôtes de messagerie natifs pouvant être utilisés par les utilisateurs
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Messagerie native
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\2 = "com.native.messaging.host.name2"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: NativeMessagingAllowlist
  - Exemple de valeur :
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### NativeMessagingBlocklist
  #### Configurer la liste rouge de messagerie native
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifie les hôtes de messagerie natifs qui ne doivent pas être utilisés.

	Utilisez « * » pour bloquer tous les hôtes de messagerie natifs, à moins qu'ils ne soient explicitement répertoriés dans la liste verte.

	Si vous ne configurez pas cette stratégie, Microsoft Edge chargera tous les hôtes de messagerie natifs installés.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: NativeMessagingBlocklist
  - Nom de la stratégie de groupe: Configurer la liste rouge de messagerie native
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Messagerie native
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\2 = "com.native.messaging.host.name2"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: NativeMessagingBlocklist
  - Exemple de valeur :
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### NativeMessagingUserLevelHosts
  #### Autoriser les hôtes de messagerie natifs au niveau de l’utilisateur (installés sans autorisation d’administrateur)
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Permet l’installation d’hôtes de messagerie natifs au niveau utilisateur.

	Si vous désactivez cette stratégie, Microsoft Edge utilisera uniquement les hôtes de messagerie natifs installés au niveau système.

	Par défaut, si vous ne configurez pas cette stratégie, Microsoft Edge autorisera l'utilisation des hôtes de messagerie natifs au niveau utilisateur.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: NativeMessagingUserLevelHosts
  - Nom de la stratégie de groupe: Autoriser les hôtes de messagerie natifs au niveau de l’utilisateur (installés sans autorisation d’administrateur)
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Messagerie native
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: NativeMessagingUserLevelHosts
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: NativeMessagingUserLevelHosts
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ## Moteur de recherche par défaut policies

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultSearchProviderEnabled
  #### Activer le moteur de recherche par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Active l’utilisation d’un moteur de recherche par défaut.

Si vous activez cette stratégie, un utilisateur peut rechercher un terme en tapant dans la barre d'adresse (tant que ce qu'il tape n’est pas une URL).

Vous pouvez spécifier le moteur de recherche par défaut à utiliser en activant le reste des stratégies de recherche par défaut. Si elles restent vides (non configurées), l’utilisateur peut choisir le moteur par défaut.

Si vous désactivez cette stratégie, l’utilisateur ne peut pas rechercher à partir de la barre d'adresse.

Si vous activez ou désactivez cette stratégie, les utilisateurs ne peuvent pas la modifier ni la remplacer.

Si vous ne configurez pas cette stratégie, le moteur de recherche par défaut est activé, et l’utilisateur peut choisir le moteur de recherche par défaut et définir la liste des moteurs de recherche.

Cette stratégie est disponible uniquement sur les instances de Windows jointes à un domaine Microsoft Active Directory, les instances de Windows 10 Professionnel ou Entreprise inscrites pour la gestion des appareils, ou les instances macOS qui sont gérées via la gestion des périphériques mobiles ou qui sont jointes à un domaine via MCX.

À partir de Microsoft Edge version 84, vous pouvez définir cette stratégie en tant que stratégie recommandée.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultSearchProviderEnabled
  - Nom de la stratégie de groupe: Activer le moteur de recherche par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Moteur de recherche par défaut
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Moteur de recherche par défaut
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: DefaultSearchProviderEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultSearchProviderEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultSearchProviderEncodings
  #### Encodages du moteur de recherche par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifiez les encodages de caractères pris en charge par le moteur de recherche. Les encodages sont des noms de page de codes tels que UTF-8, GB2312 et ISO-8859-1. Ils sont testés dans l’ordre indiqué.

Cette stratégie est facultative. Si cette option n’est pas configurée, la valeur par défaut (UTF-8) est utilisée.

Cette stratégie est appliquée uniquement si vous activez les stratégies de [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) et de [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

À partir de Microsoft Edge 84, vous pouvez la spécifier comme stratégie recommandée. Si l’utilisateur a déjà défini un moteur de recherche par défaut, le moteur de recherche par défaut configuré par cette stratégie recommandée ne sera pas ajouté à la liste des fournisseurs de recherche parmi lesquels l’utilisateur peut faire son choix. S’il s’agit du comportement souhaité, utilisez la stratégie de [ManagedSearchEngines](#managedsearchengines).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultSearchProviderEncodings
  - Nom de la stratégie de groupe: Encodages du moteur de recherche par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Moteur de recherche par défaut
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Moteur de recherche par défaut
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé\DefaultSearchProviderEncodings
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\1 = "UTF-8"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\2 = "UTF-16"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\3 = "GB2312"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\4 = "ISO-8859-1"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultSearchProviderEncodings
  - Exemple de valeur :
``` xml
<array>
  <string>UTF-8</string>
  <string>UTF-16</string>
  <string>GB2312</string>
  <string>ISO-8859-1</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultSearchProviderImageURL
  #### Spécifie la fonction de recherche-par-image pour le moteur de recherche par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifie l’URL du moteur de recherche utilisé pour la recherche d’image. Les requêtes de recherche sont envoyées à l’aide de la méthode GET.

Cette stratégie est facultative. Si vous ne la configurez pas, la recherche d’image n’est pas disponible.

Spécifiez l’URL de recherche d’image de Bing :
{bing:baseURL}'images/detail/search?iss=sbiupload&FORM=ANCMS1#enterInsights'.

Spécifiez l’URL de recherche d’image de Google : '{google:baseURL}searchbyimage/upload'.

Consultez la stratégie [DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams) pour terminer la configuration de la recherche d’image.

Cette stratégie n'est appliquée que si vous activez les stratégies [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) et stratégies [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

À partir de Microsoft Edge 84, vous pouvez la spécifier comme stratégie recommandée. Si l’utilisateur a déjà défini un moteur de recherche par défaut, le moteur de recherche par défaut configuré par cette stratégie recommandée n’est pas ajoutée à la liste des fournisseurs de recherche à partir de laquelle l’utilisateur peut faire son choix. Si ceci représente le comportement souhaité, utilisez la stratégie [ManagedSearchEngines](#managedsearchengines).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultSearchProviderImageURL
  - Nom de la stratégie de groupe: Spécifie la fonction de recherche-par-image pour le moteur de recherche par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Moteur de recherche par défaut
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Moteur de recherche par défaut
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: DefaultSearchProviderImageURL
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"https://search.contoso.com/searchbyimage/upload"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultSearchProviderImageURL
  - Exemple de valeur :
``` xml
<string>https://search.contoso.com/searchbyimage/upload</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultSearchProviderImageURLPostParams
  #### Paramètres pour une URL d’image qui utilise POST
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Si vous activez cette stratégie, elle spécifie les paramètres utilisés lors de l’exécution d’une recherche d’image utilisant POST. La stratégie est constituée de paires nom/valeur séparées par des virgules. Si une valeur est un paramètre de modèle, tel que {imageThumbnail} dans l’exemple précédent, elle est remplacée par des données de miniatures d’image réelles. Cette stratégie n'est appliquée que si vous activez les stratégies [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) et [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

       Spécifiez les paramètres POST de l’URL de recherche d’image de Bing:
       'imageBin={google:imageThumbnailBase64}'.

       Spécifiez les paramètres POST de l'URL de recherche d’image Google:
       'encoded_image={google:imageThumbnail},image_url={google:imageURL},sbisrc={google:imageSearchSource},original_width={google:imageOriginalWidth},original_height={google:imageOriginalHeight}'.

       Si vous ne définissez pas cette stratégie, les demandes de recherche d’image sont envoyées à l’aide de la méthode GET.

À partir de Microsoft Edge version 84, vous pouvez définir cette stratégie en tant que stratégie recommandée. Si l’utilisateur a déjà défini un moteur de recherche par défaut, le moteur de recherche par défaut configuré par cette stratégie recommandée n’est pas ajoutée à la liste des fournisseurs de recherche à partir de laquelle l’utilisateur peut faire son choix. Si ceci représente le comportement souhaité, utilisez la stratégie [ManagedSearchEngines](#managedsearchengines).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultSearchProviderImageURLPostParams
  - Nom de la stratégie de groupe: Paramètres pour une URL d’image qui utilise POST
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Moteur de recherche par défaut
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Moteur de recherche par défaut
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: DefaultSearchProviderImageURLPostParams
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"content={imageThumbnail},url={imageURL},sbisrc={SearchSource}"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultSearchProviderImageURLPostParams
  - Exemple de valeur :
``` xml
<string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultSearchProviderKeyword
  #### Mot clé du moteur de recherche par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifie le mot clé, qui est le raccourci utilisé dans la barre d’adresses pour déclencher la recherche de ce fournisseur.

Cette stratégie est facultative. Si vous ne la configurez pas, aucun mot clé n’active le moteur de recherche.

Cette stratégie est appliquée uniquement si vous activez les stratégies de [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) et de [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

À partir de Microsoft Edge 84, vous pouvez la spécifier en tant que stratégie recommandée. Si l’utilisateur a déjà défini un moteur de recherche par défaut, le moteur de recherche par défaut configuré par cette stratégie recommandée n’est pas ajoutée à la liste des fournisseurs de recherche à partir de laquelle l’utilisateur peut faire son choix. Si ceci représente le comportement souhaité, utilisez la stratégie  [ManagedSearchEngines](#managedsearchengines).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultSearchProviderKeyword
  - Nom de la stratégie de groupe: Mot clé du moteur de recherche par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Moteur de recherche par défaut
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Moteur de recherche par défaut
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: DefaultSearchProviderKeyword
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"mis"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultSearchProviderKeyword
  - Exemple de valeur :
``` xml
<string>mis</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultSearchProviderName
  #### Nom du moteur de recherche par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifie le nom du moteur de recherche par défaut.

Si vous activez cette stratégie, vous définissez le nom du moteur de recherche par défaut.

Si vous n’activez pas cette stratégie ou si vous la laissez vide, le nom d’hôte spécifié par l’URL de recherche est utilisé.

« DefaultSearchProviderName » doit être défini sur un moteur de recherche chiffré approuvé par l’organisation qui correspond au moteur de recherche chiffré défini dans DTBC-0008. Cette stratégie est appliquée uniquement si vous activez les stratégies [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) et [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

À partir de Microsoft Edge version 84, vous pouvez définir cette stratégie en tant que stratégie recommandée. Si l’utilisateur a déjà défini un moteur de recherche par défaut, le moteur de recherche par défaut configuré par cette stratégie recommandée n’est pas ajoutée à la liste des fournisseurs de recherche à partir de laquelle l’utilisateur peut choisir. Si ceci représente le comportement souhaité, utilisez la stratégie [ManagedSearchEngines](#managedsearchengines).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultSearchProviderName
  - Nom de la stratégie de groupe: Nom du moteur de recherche par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Moteur de recherche par défaut
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Moteur de recherche par défaut
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: DefaultSearchProviderName
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"My Intranet Search"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultSearchProviderName
  - Exemple de valeur :
``` xml
<string>My Intranet Search</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultSearchProviderSearchURL
  #### URL de recherche du moteur de recherche par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifie l’URL du moteur de recherche utilisé pour une recherche par défaut. L’URL contient la chaîne « {searchTerms} », qui est remplacée au moment de la requête par les termes que l’utilisateur recherche.

Spécifiez l’URL de recherche de Bing sous la forme suivante :

« {bing:baseURL}search?q={searchTerms} ».

Spécifiez l’URL de recherche de Google sous la forme suivante : « {google:baseURL}search?q={searchTerms}&{google:RLZ}{google:originalQueryForSuggestion}{google:assistedQueryStats}{google:searchFieldtrialParameter}{google:searchClient}{google:sourceId}ie={inputEncoding} ».

Cette stratégie est obligatoire lorsque vous activez la stratégie [DefaultSearchProviderEnabled](#defaultsearchproviderenabled). Si vous n’activez pas cette dernière, cette stratégie est ignorée.

  À partir de Microsoft Edge 84, vous pouvez la spécifier comme stratégie recommandée. S i l’utilisateur a déjà défini un moteur de recherche par défaut, le moteur de recherche par défaut configuré par cette stratégie recommandée n’est pas ajoutée à la liste des fournisseurs de recherche à partir de laquelle l’utilisateur peut faire son choix. Si ceci représente le comportement souhaité, utilisez la stratégie [ManagedSearchEngines](#managedsearchengines).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultSearchProviderSearchURL
  - Nom de la stratégie de groupe: URL de recherche du moteur de recherche par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Moteur de recherche par défaut
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Moteur de recherche par défaut
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: DefaultSearchProviderSearchURL
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"https://search.contoso.com/search?q={searchTerms}"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultSearchProviderSearchURL
  - Exemple de valeur :
``` xml
<string>https://search.contoso.com/search?q={searchTerms}</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultSearchProviderSuggestURL
  #### URL du moteur de recherche par défaut pour les suggestions
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifie l’URL du moteur de recherche utilisé pour fournir des suggestions de recherche. L’URL contient la chaîne « {searchTerms} », qui est remplacée au moment de la requête par le texte que l’utilisateur a entré jusqu’à présent.

       Cette stratégie est facultative. Si vous ne la configurez pas, les utilisateurs ne verront pas les suggestions de recherche; ils verront les suggestions de l’historique de navigation et des favoris.

       L’URL de suggestion de Bing peut être spécifiée sous la forme :

       « {bing:baseURL}qbox?query={searchTerms} ».

       L’URL de suggestion de Google peut être spécifiée sous la forme : « {google:baseURL}complete/search?output=chrome&q={searchTerms} ».

       Cette stratégie est appliquée uniquement si vous activez les stratégies [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) et [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

À partir de Microsoft Edge version 84, vous pouvez définir cette stratégie en tant que stratégie recommandée. Si l’utilisateur a déjà défini un moteur de recherche par défaut, le moteur de recherche par défaut configuré par cette stratégie recommandée n’est pas ajoutée à la liste des fournisseurs de recherche à partir de laquelle l’utilisateur peut faire son choix. Si ceci représente le comportement souhaité, utilisez la stratégie [ManagedSearchEngines](#managedsearchengines).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultSearchProviderSuggestURL
  - Nom de la stratégie de groupe: URL du moteur de recherche par défaut pour les suggestions
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Moteur de recherche par défaut
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Moteur de recherche par défaut
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: DefaultSearchProviderSuggestURL
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"https://search.contoso.com/suggest?q={searchTerms}"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultSearchProviderSuggestURL
  - Exemple de valeur :
``` xml
<string>https://search.contoso.com/suggest?q={searchTerms}</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### NewTabPageSearchBox
  #### Configurer l’expérience de la zone de recherche de la page nouvel onglet
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 85 ou version ultérieure

  #### Description
  Vous pouvez configurer la zone de recherche de la nouvelle page d’onglet pour utiliser « Zone de recherche (recommandé) » ou « Barre d’adresse » pour effectuer une recherche dans les nouveaux onglets. Cette stratégie fonctionne uniquement si vous définissez le moteur de recherche sur une valeur autre que Bing en définissant les deux stratégies suivantes : [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) et [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

Si vous désactivez ou ne configurez pas cette stratégie :

        - Si le moteur de recherche par défaut de la barre d’adresse est Bing, la page nouvel onglet utilise la zone de recherche pour effectuer une recherche dans les nouveaux onglets.
        - Si le moteur de recherche par défaut de la barre d’adresse n’est pas Bing, les utilisateurs sont invités à choisir une option supplémentaire (utilisez la « barre d’adresse ») lors de la recherche dans les nouveaux onglets.


        Si vous activez cette stratégie et configurez-la sur :

        - « Zone de recherche (recommandé) » (« Bing »), la nouvelle page d’onglet utilise la zone de recherche pour effectuer une recherche dans les nouveaux onglets.
        - « Barre d’adresses » (« Redirect »), la zone de recherche de la nouvelle page de l’onglet utilise la barre d’adresse pour effectuer une recherche dans les nouveaux onglets.

Mappage des options de stratégie :

* bing (bing) = Zone de recherche (recommandé)

* redirect (redirect) = Barre d’adresse

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: NewTabPageSearchBox
  - Nom de la stratégie de groupe: Configurer l’expérience de la zone de recherche de la page nouvel onglet
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Moteur de recherche par défaut
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Moteur de recherche par défaut
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: NewTabPageSearchBox
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"bing"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: NewTabPageSearchBox
  - Exemple de valeur :
``` xml
<string>bing</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ## Paramètres de SmartScreen policies

  [Revenir au début](#microsoft-edge---stratégies)

  ### PreventSmartScreenPromptOverride
  #### Empêcher le contournement des avertissements de Microsoft Defender SmartScreen pour les sites
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Ce paramètre de stratégie vous permet de déterminer si les utilisateurs peuvent ignorer les avertissements de Microsoft Defender SmartScreen sur les sites web potentiellement malveillants.

Si vous activez ce paramètre, les utilisateurs ne peuvent pas ignorer les avertissements de Microsoft Defender SmartScreen et ils ne peuvent pas continuer sur le site.

Si vous désactivez ou ne configurez pas ce paramètre, les utilisateurs peuvent ignorer les avertissements de Microsoft Defender SmartScreen et accéder au site.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft Active Directory, les instances de Windows 10 Professionnel ou Entreprise qui sont inscrites pour la gestion des appareils, ou les instances macOS qui sont gérées via la gestion des périphériques mobiles ou qui sont jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PreventSmartScreenPromptOverride
  - Nom de la stratégie de groupe: Empêcher le contournement des avertissements de Microsoft Defender SmartScreen pour les sites
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de SmartScreen
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: PreventSmartScreenPromptOverride
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PreventSmartScreenPromptOverride
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PreventSmartScreenPromptOverrideForFiles
  #### Empêcher le contournement des avertissements de Microsoft Defender SmartScreen concernant les téléchargements
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 77 ou ultérieur
  - Sur macOS depuis 79 ou ultérieur

  #### Description
  Cette stratégie vous permet de déterminer si les utilisateurs peuvent ignorer les avertissements de Microsoft Defender SmartScreen à propos des téléchargements non vérifiés.

Si vous activez cette stratégie, les utilisateurs de votre organisation ne peuvent pas ignorer les avertissements de Microsoft Defender SmartScreen et ne peuvent pas terminer les téléchargements non vérifiés.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, les utilisateurs peuvent ignorer les avertissements de Microsoft Defender SmartScreen et effectuer des téléchargements non vérifiés.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft Active Directory ou sur les instances de Windows 10 Professionnel ou Entreprise qui sont inscrites pour la gestion des appareils, ou les instances macOS qui sont gérées via la gestion des périphériques mobiles ou qui sont jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PreventSmartScreenPromptOverrideForFiles
  - Nom de la stratégie de groupe: Empêcher le contournement des avertissements de Microsoft Defender SmartScreen concernant les téléchargements
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de SmartScreen
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: PreventSmartScreenPromptOverrideForFiles
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PreventSmartScreenPromptOverrideForFiles
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SmartScreenAllowListDomains
  #### Configurer la liste des domaines pour lesquels Microsoft Defender SmartScreen ne déclenche pas d'avertissement
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Configurez la liste des domaines approuvés par Microsoft Defender SmartScreen. Cela signifie :
Microsoft Defender SmartScreen ne recherche pas les ressources potentiellement malveillantes, telles que les logiciels d’hameçonnage et autres programmes malveillants, si les URL sources correspondent à ces domaines.
Le service de protection contre le téléchargement Microsoft Defender SmartScreen ne vérifie pas les téléchargements hébergés sur ces domaines.

Si vous activez cette stratégie, Microsoft Defender SmartScreen approuve ces domaines.
Si vous désactivez cette stratégie ou si vous ne la définissez pas, la protection Microsoft Defender SmartScreen par défaut est appliquée à toutes les ressources.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft Active Directory, dans les instances de Windows 10 Professionnel ou Entreprise qui sont inscrites pour la gestion des appareils, ou les instances macOS qui sont gérées via la gestion des périphériques mobiles ou qui sont jointes à un domaine via MCX.
Notez également que cette stratégie ne s’applique pas si votre organisation a activé Microsoft Defender - Protection avancée contre les menaces. Vous devez plutôt configurer vos listes verte et rouge dans le Centre de sécurité Microsoft Defender.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SmartScreenAllowListDomains
  - Nom de la stratégie de groupe: Configurer la liste des domaines pour lesquels Microsoft Defender SmartScreen ne déclenche pas d'avertissement
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de SmartScreen
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\2 = "myuniversity.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SmartScreenAllowListDomains
  - Exemple de valeur :
``` xml
<array>
  <string>mydomain.com</string>
  <string>myuniversity.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SmartScreenEnabled
  #### Configurer Microsoft Defender SmartScreen
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Ce paramètre de stratégie vous permet de configurer si vous souhaitez activer Microsoft Defender SmartScreen. Microsoft Defender SmartScreen renvoie des messages d’avertissement pour protéger vos utilisateurs contre d’éventuels courriers indésirables d’hameçonnage et logiciels malveillants. Par défaut, Microsoft Defender SmartScreen est activé.

Si vous activez ce paramètre, Microsoft Defender SmartScreen est activé.

Si vous désactivez ce paramètre, Microsoft Defender SmartScreen est désactivé.

Si vous ne configurez pas ce paramètre, les utilisateurs peuvent choisir d’utiliser ou non Microsoft Defender SmartScreen.

Cette stratégie n'est disponible que sur les instances de Windows jointes à un domaine Microsoft Active Directory, les instances de Windows 10 Professionnel ou Entreprise qui sont inscrites pour la gestion des appareils, ou les instances macOS qui sont gérées via la gestion des périphériques mobiles ou qui sont jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SmartScreenEnabled
  - Nom de la stratégie de groupe: Configurer Microsoft Defender SmartScreen
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de SmartScreen
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Paramètres de SmartScreen
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: SmartScreenEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SmartScreenEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SmartScreenForTrustedDownloadsEnabled
  #### Forcer les vérifications de Microsoft Defender SmartScreen sur les téléchargements provenant de sources approuvées
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 78 ou ultérieur

  #### Description
  Cette stratégie vous permet de configurer la vérification par Microsoft Defender SmartScreen de la réputation des téléchargements à partir d'une source approuvée.

Si vous activez ou ne configurez pas cette stratégie, Microsoft Defender SmartScreen vérifie la réputation des téléchargements, quelle qu'en soit la source.

Si vous désactivez cette stratégie, Microsoft Defender SmartScreen ne vérifie pas la réputation des téléchargements lors d'un téléchargement à partir d'une source approuvée.

Cette stratégie n’est disponible que sur les instances Windows qui sont jointes à un domaine Microsoft Active Directory, des instances Windows 10 Professionnel ou Entreprise qui sont inscrites pour la gestion des appareils.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SmartScreenForTrustedDownloadsEnabled
  - Nom de la stratégie de groupe: Forcer les vérifications de Microsoft Defender SmartScreen sur les téléchargements provenant de sources approuvées
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de SmartScreen
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Paramètres de SmartScreen
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: SmartScreenForTrustedDownloadsEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SmartScreenPuaEnabled
  #### Configurer Microsoft Defender SmartScreen de manière à bloquer les applications potentiellement indésirables
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 80 ou version ultérieure

  #### Description
  Ce paramètre de stratégie vous permet de configurer si vous souhaitez activer le blocage des applications potentiellement indésirables avec Microsoft Defender SmartScreen. Le blocage d’applications potentiellement indésirables avec Microsoft Defender SmartScreen fournit des messages d’avertissement pour protéger les utilisateurs des logiciels de publicité, des mineurs de cryptomonnaie, des bundleware et autres applications à faible réputation hébergées par des sites web. Le blocage d’applications potentiellement indésirables avec Microsoft Defender SmartScreen est désactivé par défaut.

Si vous activez ce paramètre, le blocage des applications potentiellement indésirables avec Microsoft Defender SmartScreen est activé.

Si vous désactivez ce paramètre, le blocage des applications potentiellement indésirables avec Microsoft Defender SmartScreen est désactivé.

Si vous ne configurez pas ce paramètre, les utilisateurs peuvent choisir s’ils souhaitent utiliser le blocage des applications potentiellement indésirables avec Microsoft Defender SmartScreen.

Cette stratégie est disponible uniquement sur les instances de Windows qui sont jointes à un domaine Microsoft Active Directory, les instances de Windows 10 Professionnel ou Entreprise qui sont inscrites pour la gestion des appareils, ou les instances macOS qui sont gérées via la gestion des périphériques mobiles ou qui sont jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SmartScreenPuaEnabled
  - Nom de la stratégie de groupe: Configurer Microsoft Defender SmartScreen de manière à bloquer les applications potentiellement indésirables
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de SmartScreen
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Paramètres de SmartScreen
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: SmartScreenPuaEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SmartScreenPuaEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ## Paramètres de contenu policies

  [Revenir au début](#microsoft-edge---stratégies)

  ### AutoSelectCertificateForUrls
  #### Sélectionner automatiquement des certificats clients pour ces sites
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifiez la liste des sites en fonction des modèles d’URL pour lesquels Microsoft Edge doit sélectionner automatiquement un certificat client si le site le demande.

La valeur doit être un tableau de dictionnaires JSON convertis en chaînes. La forme de chaque dictionnaire doit être { "pattern": "$URL_PATTERN", "filter" : $FILTER }, où $URL_PATTERN représente un modèle de paramètre de contenu. $FILTER restreint les certificats clients à partir desquels le navigateur va effectuer une sélection automatique. Quel que soit le filtre, seuls les certificats qui correspondent à la demande de certificat du serveur vont être sélectionnés. Par exemple, si $FILTER a la forme { "ISSUER": { "CN": "$ISSUER_CN" } }, seuls les certificats clients émis par un certificat présentant CommonName $ISSUER_CN peuvent en outre être sélectionnés. Si $FILTER contient une section "ISSUER" et une section "SUBJECT", un certificat client doit répondre à ces deux conditions pour être sélectionné. Si $FILTER indique une organisation (« O »), un certificat doit avoir au moins une organisation qui correspond à la valeur spécifiée pour être sélectionné. Si $FILTER indique une unité organisationnelle (« UO »), un certificat doit avoir au moins une unité organisationnelle qui correspond à la valeur spécifiée pour être sélectionné. Si $FILTER est le dictionnaire vide {}, la sélection des certificats clients n'est pas davantage restreinte.

Si vous ne configurez pas cette stratégie, la sélection automatique n'est effectuée pour aucun site.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AutoSelectCertificateForUrls
  - Nom de la stratégie de groupe: Sélectionner automatiquement des certificats clients pour ces sites
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls\1 = "{\"pattern\":\"https://www.contoso.com\",\"filter\":{\"ISSUER\":{\"CN\":\"certificate issuer name\", \"L\": \"certificate issuer location\", \"O\": \"certificate issuer org\", \"OU\": \"certificate issuer org unit\"}, \"SUBJECT\":{\"CN\":\"certificate subject name\", \"L\": \"certificate subject location\", \"O\": \"certificate subject org\", \"OU\": \"certificate subject org unit\"}}}"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AutoSelectCertificateForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>{"pattern":"https://www.contoso.com","filter":{"ISSUER":{"CN":"certificate issuer name", "L": "certificate issuer location", "O": "certificate issuer org", "OU": "certificate issuer org unit"}, "SUBJECT":{"CN":"certificate subject name", "L": "certificate subject location", "O": "certificate subject org", "OU": "certificate subject org unit"}}}</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### CookiesAllowedForUrls
  #### Autoriser les cookies sur des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez la liste des sites en fonction des modèles d’URL qui ne peuvent pas définir de cookies.

Si vous ne configurez pas cette stratégie, la valeur par défaut globale de la stratégie [DefaultCookiesSetting](#defaultcookiessetting) (si elle est définie) ou la configuration personnelle de l’utilisateur est utilisée pour tous les sites.

Pour plus d’informations, voir les stratégies [CookiesBlockedForUrls](#cookiesblockedforurls) et [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls).

Remarque : il ne peut pas y avoir de modèles d’URL en conflit définis entre ces trois stratégies :

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- CookiesAllowedForUrls

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

Pour empêcher la suppression des cookies à la fermeture, configurez la stratégie [SaveCookiesOnExit](#savecookiesonexit).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: CookiesAllowedForUrls
  - Nom de la stratégie de groupe: Autoriser les cookies sur des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: CookiesAllowedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### CookiesBlockedForUrls
  #### Bloquer les cookies sur des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez la liste des sites en fonction des modèles d’URL qui ne peuvent pas définir de cookies.

Si vous ne configurez pas cette de stratégie, la valeur par défaut globale de la stratégie [DefaultCookiesSetting](#defaultcookiessetting) (si elle est définie) ou de la configuration personnelle de l’utilisateur est utilisée pour tous les sites.

Voir les stratégies [CookiesAllowedForUrls](#cookiesallowedforurls) et [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) pour plus d’informations.

Remarque : il ne peut pas y avoir de modèles d’URL en conflit définis entre ces trois stratégies :

- CookiesBlockedForUrls

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: CookiesBlockedForUrls
  - Nom de la stratégie de groupe: Bloquer les cookies sur des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: CookiesBlockedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### CookiesSessionOnlyForUrls
  #### Limiter les cookies provenant de sites web spécifiques à la session active
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Les cookies créés par les sites web qui correspondent à un modèle d’URL que vous définissez sont supprimés à la fin de la session (lors de la fermeture de la fenêtre).

Les cookies créés par les sites web qui ne correspondent pas au modèle sont contrôlés par la stratégie [DefaultCookiesSetting](#defaultcookiessetting) (si elle est définie) ou par la configuration personnelle de l’utilisateur. Il s'agit également du comportement par défaut si vous ne configurez pas cette stratégie.

Si Microsoft Edge s’exécute en mode arrière-plan, la session peut ne pas se fermer à la fermeture de la dernière fenêtre, ce qui signifie que les cookies ne seront pas effacés à la fermeture de la fenêtre. Voir la stratégie [BackgroundModeEnabled](#backgroundmodeenabled) pour plus d’informations sur la configuration de ce qu'il se passe lorsque Microsoft Edge s’exécute en mode arrière-plan.

Vous pouvez également utiliser les stratégies [CookiesAllowedForUrls](#cookiesallowedforurls) et [CookiesBlockedForUrls](#cookiesblockedforurls) pour contrôler les sites web qui peuvent créer des cookies.

Remarque : il ne peut pas y avoir de modèles d’URL en conflit définis entre ces trois stratégies

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- CookiesSessionOnlyForUrls

Si vous définissez la stratégie [RestoreOnStartup](#restoreonstartup) de manière à restaurer les URL à partir des sessions précédentes, cette stratégie est ignorée et les cookies sont stockés définitivement pour ces sites.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: CookiesSessionOnlyForUrls
  - Nom de la stratégie de groupe: Limiter les cookies provenant de sites web spécifiques à la session active
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: CookiesSessionOnlyForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultCookiesSetting
  #### Configurer les cookies
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Contrôlez si des sites web peuvent créer des cookies sur l’appareil de l’utilisateur. Cette stratégie est tout ou rien : vous pouvez laisser tous les sites web créer des cookies ou aucun site web ne crée de cookies. Vous ne pouvez pas utiliser cette stratégie pour activer les cookies de sites web spécifiques.

Définissez la stratégie sur « SessionOnly » pour effacer les cookies à la fermeture de la session. Si Microsoft Edge est exécuté en mode arrière-plan, la session risque de ne pas se fermer à la fermeture de la dernière fenêtre, ce qui signifie que les cookies ne seront pas effacés à la fermeture de la fenêtre. Consultez la stratégie [BackgroundModeEnabled](#backgroundmodeenabled) pour plus d’informations sur la configuration de ce qu'il se passe lorsque Microsoft Edge s’exécute en mode arrière-plan.

Si vous ne configurez pas cette stratégie, la valeur par défaut « AllowCookies » est utilisée et les utilisateurs peuvent modifier ce paramètre dans les paramètres de Microsoft Edge. (Si vous ne voulez pas que les utilisateurs puissent modifier ce paramètre, définissez la stratégie.)

Mappage des options de stratégie :

* AllowCookies (1) = Autoriser tous les sites à créer des cookies

* BlockCookies (2) = N'autoriser aucun site à créer des cookies

* SessionOnly (4) = Conserver les cookies pendant toute la durée de la session, sauf ceux indiqués dans [SaveCookiesOnExit](#savecookiesonexit)

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultCookiesSetting
  - Nom de la stratégie de groupe: Configurer les cookies
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DefaultCookiesSetting
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultCookiesSetting
  - Exemple de valeur :
``` xml
<integer>1</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultFileSystemReadGuardSetting
  #### Contrôler l’utilisation de l’API du système de fichiers pour la lecture
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Si vous définissez cette stratégie sur 3, les sites web peuvent demander l’accès en lecture au système de fichiers du système d’exploitation hôte à l’aide de l’API du système de fichiers. Si vous définissez cette stratégie sur 2, l’accès est refusé.

Si vous ne définissez pas cette stratégie, les sites web peuvent demander l’accès. Les utilisateurs peuvent modifier ce paramètre.

Mappage des options de stratégie :

* BlockFileSystemRead (2) = Ne pas autoriser les sites à demander l’accès en lecture aux fichiers et aux répertoires via l’API du système de fichiers

* AskFileSystemRead (3) = Autoriser les sites à demander à l’utilisateur d’octroyer l’accès en lecture aux fichiers et aux répertoires via l’API du système de fichiers

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultFileSystemReadGuardSetting
  - Nom de la stratégie de groupe: Contrôler l’utilisation de l’API du système de fichiers pour la lecture
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DefaultFileSystemReadGuardSetting
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultFileSystemReadGuardSetting
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultFileSystemWriteGuardSetting
  #### Contrôler l’utilisation de l’API du système de fichiers pour l’écriture
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Si vous définissez cette stratégie sur 3, les sites web peuvent demander l’accès en écriture au système de fichiers du système d’exploitation hôte à l’aide de l’API du système de fichiers. Si vous définissez cette stratégie sur 2, l’accès est refusé.

Si vous ne définissez pas cette stratégie, les sites web peuvent demander l’accès. Les utilisateurs peuvent modifier ce paramètre.

Mappage des options de stratégie :

* BlockFileSystemWrite (2) = Ne pas autoriser les sites à demander l’accès en écriture aux fichiers et aux répertoires

* AskFileSystemWrite (3) = Autoriser les sites à demander à l’utilisateur d’accorder l’accès en écriture aux fichiers et aux répertoires

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultFileSystemWriteGuardSetting
  - Nom de la stratégie de groupe: Contrôler l’utilisation de l’API du système de fichiers pour l’écriture
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DefaultFileSystemWriteGuardSetting
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultFileSystemWriteGuardSetting
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultGeolocationSetting
  #### Paramètre de géolocalisation par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Indiquez si les sites web peuvent suivre les emplacements physiques des utilisateurs. Vous pouvez autoriser le suivi par défaut (« AllowGeolocation »), le refuser par défaut (« BlockGeolocation ») ou demander à l’utilisateur chaque fois qu’un site web demande son emplacement (« AskGeolocation »).

Si vous ne configurez pas cette stratégie, « AskGeolocation » est utilisé et l’utilisateur peut le modifier.

Mappage des options de stratégie :

* AllowGeolocation (1) = Autoriser les sites à effectuer le suivi de l’emplacement physique des utilisateurs

* BlockGeolocation (2) = N'autoriser aucun site à effectuer le suivi d’emplacement physique des utilisateurs

* AskGeolocation (3) = Demander chaque fois qu’un site souhaite suivre l’emplacement physique des utilisateurs

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultGeolocationSetting
  - Nom de la stratégie de groupe: Paramètre de géolocalisation par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DefaultGeolocationSetting
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultGeolocationSetting
  - Exemple de valeur :
``` xml
<integer>1</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultImagesSetting
  #### Paramètres des images par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez si les sites web peuvent afficher des images. Vous pouvez autoriser les images sur tous les sites (« AllowImages ») ou les bloquer sur tous les sites (« BlockImages »).

Si vous ne configurez pas cette stratégie, les images sont autorisées par défaut et l’utilisateur peut modifier ce paramètre.

Mappage des options de stratégie :

* AllowImages (1) = Autoriser tous les sites à afficher toutes les images

* BlockImages (2) = N'autoriser aucun site à afficher des images

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultImagesSetting
  - Nom de la stratégie de groupe: Paramètres des images par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DefaultImagesSetting
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultImagesSetting
  - Exemple de valeur :
``` xml
<integer>1</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultInsecureContentSetting
  #### Contrôler l’utilisation des exceptions de contenu non sécurisé
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 80 ou version ultérieure

  #### Description
  Vous permet de définir si les utilisateurs peuvent ajouter des exceptions pour autoriser le contenu mixte pour des sites spécifiques.

Cette stratégie peut être remplacée pour des modèles d’URL spécifiques à l’aide des stratégies[InsecureContentAllowedForUrls](#insecurecontentallowedforurls) et [InsecureContentBlockedForUrls](#insecurecontentblockedforurls).

Si cette stratégie n’est pas définie, les utilisateurs sont autorisés à ajouter des exceptions pour permettre le contenu mixte pouvant être bloqué et désactiver les mises à jour automatiques pour le contenu mixte pouvant facultativement être bloqué.

Mappage des options de stratégie :

* BlockInsecureContent (2) = Empêcher les sites de charger du contenu mixte

* AllowExceptionsInsecureContent (3) = Autoriser les utilisateurs à ajouter des exceptions pour autoriser un contenu mixte

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultInsecureContentSetting
  - Nom de la stratégie de groupe: Contrôler l’utilisation des exceptions de contenu non sécurisé
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DefaultInsecureContentSetting
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultInsecureContentSetting
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultJavaScriptSetting
  #### Paramètre par défaut de JavaScript
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez si les sites web peuvent exécuter JavaScript. Vous pouvez l'autoriser pour tous les sites (« AllowJavaScript ») ou le bloquer pour tous les sites (« BlockJavaScript »).

Si vous ne configurez pas cette stratégie, tous les sites peuvent exécuter JavaScript par défaut et l’utilisateur peut modifier ce paramètre.

Mappage des options de stratégie :

* AllowJavaScript (1) = Autoriser tous les sites à exécuter JavaScript

* BlockJavaScript (2) = N'autoriser aucun site à exécuter JavaScript

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultJavaScriptSetting
  - Nom de la stratégie de groupe: Paramètre par défaut de JavaScript
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DefaultJavaScriptSetting
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultJavaScriptSetting
  - Exemple de valeur :
``` xml
<integer>1</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultNotificationsSetting
  #### Paramètres de notification par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez si les sites web peuvent afficher les notifications de bureau. Vous pouvez les autoriser par défaut (« AllowNotifications »), les refuser par défaut v ou demander que l’utilisateur reçoive une demande chaque fois qu’un site web veut afficher une notification (« AskNotifications »).

Si vous ne configurez pas cette stratégie, les notifications sont autorisées par défaut et l’utilisateur peut modifier ce paramètre.

Mappage des options de stratégie :

* AllowNotifications (1) = Autoriser les sites à afficher les notifications de l'appareil de bureau

* BlockNotifications (2) = N'autoriser aucun site à afficher les notifications du bureau

* AskNotifications (3) = Demander chaque fois qu’un site souhaite afficher les notifications de l'appareil de bureau

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultNotificationsSetting
  - Nom de la stratégie de groupe: Paramètres de notification par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DefaultNotificationsSetting
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultNotificationsSetting
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultPluginsSetting
  #### Paramètre Adobe Flash par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  [PluginsAllowedForUrls](#pluginsallowedforurls) et [PluginsBlockedForUrls](#pluginsblockedforurls) sont examinées en premier, puis cette stratégie. Les options sont « ClickToPlay » et « BlockPlugins ». Si vous configurez cette stratégie sur « BlockPlugins », ce plug-in est refusé pour tous les sites web. « ClickToPlay » permet au plug-in Flash de s'exécuter, mais les utilisateurs cliquent sur l’espace réservé pour le démarrer.

Si vous ne définissez pas cette stratégie, elle utilise BlockPlugins et les utilisateurs peuvent modifier ce paramètre.

Remarque : la lecture automatique est réservée aux domaines répertoriés explicitement dans la stratégie [PluginsAllowedForUrls](#pluginsallowedforurls). Pour activer la lecture automatique pour tous les sites, ajoutez http://* et https://* à la liste d’URL autorisée.

Mappage des options de stratégie :

* BlockPlugins (2) = Bloquer le plug-in Adobe Flash

* ClickToPlay (3) = Cliquer pour lire

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultPluginsSetting
  - Nom de la stratégie de groupe: Paramètre Adobe Flash par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DefaultPluginsSetting
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultPluginsSetting
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultPopupsSetting
  #### Paramètres de fenêtre contextuelle par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez si les sites web peuvent afficher des fenêtres contextuelles. Vous pouvez les autoriser sur tous les sites web (« AllowPopups ») ou les bloquer sur tous les sites (« BlockPopups »).

Si vous ne configurez pas cette stratégie, des fenêtres contextuelles sont bloquées par défaut et les utilisateurs peuvent modifier ce paramètre.

Mappage des options de stratégie :

* AllowPopups (1) = Autoriser tous les sites à afficher les fenêtres contextuelles

* BlockPopups (2) = Ne pas autoriser les sites à afficher les fenêtres contextuelles

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultPopupsSetting
  - Nom de la stratégie de groupe: Paramètres de fenêtre contextuelle par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DefaultPopupsSetting
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultPopupsSetting
  - Exemple de valeur :
``` xml
<integer>1</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultWebBluetoothGuardSetting
  #### Contrôler l’utilisation de l’API web Bluetooth
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Contrôler si les sites web peuvent accéder aux appareils Bluetooth à proximité. Vous pouvez complètement bloquer l’accès ou exiger que le site demande à l’utilisateur à chaque fois qu’il souhaite accéder à un appareil Bluetooth.

Si vous ne configurez pas cette stratégie, la valeur par défaut ('AskWebBluetooth', qui signifie que les utilisateurs sont invités à chaque fois) est utilisée et les utilisateurs peuvent la modifier.

Mappage des options de stratégie :

* BlockWebBluetooth (2) = N'autoriser aucun site à demander l’accès à des appareils Bluetooth via l’API Bluetooth web

* AskWebBluetooth (3) = Autoriser les sites à demander à l’utilisateur de leur accorder l’accès à un appareil Bluetooth à proximité

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultWebBluetoothGuardSetting
  - Nom de la stratégie de groupe: Contrôler l’utilisation de l’API web Bluetooth
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DefaultWebBluetoothGuardSetting
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultWebBluetoothGuardSetting
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultWebUsbGuardSetting
  #### Contrôler l’utilisation de l’API WebUSB
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez si les sites web peuvent accéder aux périphériques USB connectés. Vous pouvez entièrement bloquer l’accès ou demander à l’utilisateur chaque fois qu’un site web veut accéder aux périphériques USB connectés.

Vous pouvez remplacer cette stratégie pour les modèles d’URL spécifiques à l’aide des [WebUsbAskForUrls](#webusbaskforurls) et stratégies [WebUsbBlockedForUrls](#webusbblockedforurls).

Si vous ne configurez pas cette stratégie, les sites peuvent demander aux utilisateurs s'ils peuvent accéder à des périphériques USB connectés ('AskWebUsb') par défaut et les utilisateurs peuvent modifier ce paramètre.

Mappage des options de stratégie :

* BlockWebUsb (2) = N'autoriser aucun site à demander l’accès aux appareils USB via l’API WebUSB

* AskWebUsb (3) = Autoriser les sites à demander à l’utilisateur d' accorder l’accès à un périphérique USB connecté

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultWebUsbGuardSetting
  - Nom de la stratégie de groupe: Contrôler l’utilisation de l’API WebUSB
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DefaultWebUsbGuardSetting
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultWebUsbGuardSetting
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### FileSystemReadAskForUrls
  #### Autoriser l’accès en lecture via l’API du système de fichiers sur ces sites
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  La configuration de cette stratégie vous permet de répertorier les modèles d’URL qui spécifient les sites qui peuvent demander aux utilisateurs de leur accorder l’accès en lecture aux fichiers ou aux répertoires du système de fichiers du système d’exploitation hôte via l’API du système de fichiers.

Si vous laissez la stratégie non définie, cela signifie que [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) s’applique à tous les sites, s’il est défini. Si ce n’est pas le cas, les paramètres personnels des utilisateurs s’appliquent.

Les modèles d’URL ne peuvent pas entrer en conflit avec [FileSystemReadBlockedForUrls](#filesystemreadblockedforurls). Aucune des stratégies n’est prioritaire si une URL correspond aux deux.

Pour obtenir des informations détaillées sur les modèles de url valides, consultez https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: FileSystemReadAskForUrls
  - Nom de la stratégie de groupe: Autoriser l’accès en lecture via l’API du système de fichiers sur ces sites
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\2 = "[*.]example.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: FileSystemReadAskForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### FileSystemReadBlockedForUrls
  #### Bloquer l’accès en lecture via l’API du système de fichiers sur ces sites
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Si vous définissez cette stratégie, vous pouvez répertorier les modèles d’URL qui spécifient les sites qui ne peuvent pas demander aux utilisateurs de leur accorder l’accès en lecture aux fichiers ou aux répertoires du système de fichiers du système d’exploitation hôte via l’API du système de fichiers.

Si vous ne définissez pas cette stratégie, [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) s’applique à tous les sites, s’il est défini. Si ce n’est pas le cas, les paramètres personnels des utilisateurs s’appliquent.

Les modèles d’URL ne peuvent pas entrer en conflit avec [FileSystemReadAskForUrls](#filesystemreadaskforurls). Aucune des stratégies n’est prioritaire si une URL correspond aux deux.

Pour obtenir des informations détaillées sur les modèles de url valides, consultez https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: FileSystemReadBlockedForUrls
  - Nom de la stratégie de groupe: Bloquer l’accès en lecture via l’API du système de fichiers sur ces sites
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\2 = "[*.]example.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: FileSystemReadBlockedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### FileSystemWriteAskForUrls
  #### Autoriser l’accès en écriture aux fichiers et aux répertoires sur ces sites
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Si vous définissez cette stratégie, vous pouvez répertorier les modèles d’URL qui spécifient les sites qui peuvent demander aux utilisateurs de leur accorder l’accès en écriture aux fichiers ou aux répertoires du système de fichiers du système d’exploitation hôte.

     Si vous ne définissez pas cette stratégie, [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) s’applique à tous les sites, s’il est défini. Si ce n’est pas le cas, les paramètres personnels des utilisateurs s’appliquent.

     Les modèles d’URL ne peuvent pas entrer en conflit avec [FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls). Aucune des stratégies n’est prioritaire si une URL correspond aux deux.
url      Pour obtenir des informations détaillées sur les modèles de
valides, consultez https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: FileSystemWriteAskForUrls
  - Nom de la stratégie de groupe: Autoriser l’accès en écriture aux fichiers et aux répertoires sur ces sites
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\2 = "[*.]example.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: FileSystemWriteAskForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### FileSystemWriteBlockedForUrls
  #### Bloquer l’accès en écriture aux fichiers et aux répertoires sur ces sites
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Si vous définissez cette stratégie, vous pouvez répertorier les modèles d’URL qui spécifient les sites qui ne peuvent pas demander aux utilisateurs de leur accorder l’accès en écriture aux fichiers ou aux répertoires du système de fichiers du système d’exploitation hôte.

     Si vous ne définissez pas cette stratégie, [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) s’applique à tous les sites, s’il est défini. Si ce n’est pas le cas, les paramètres personnels des utilisateurs s’appliquent.

     Les modèles d’URL ne peuvent pas entrer en conflit avec [FileSystemWriteAskForUrls](#filesystemwriteaskforurls). Aucune des stratégies n’est prioritaire si une URL correspond aux deux.
url      Pour obtenir des informations détaillées sur les modèles de
valides, consultez https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: FileSystemWriteBlockedForUrls
  - Nom de la stratégie de groupe: Bloquer l’accès en écriture aux fichiers et aux répertoires sur ces sites
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\2 = "[*.]example.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: FileSystemWriteBlockedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ImagesAllowedForUrls
  #### Autoriser les images sur ces sites
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez une liste de sites basée sur des modèles d’URL, qui peuvent afficher des images.

Si vous ne configurez pas cette stratégie, la valeur par défaut globale est utilisée pour tous les sites à partir de la stratégie [DefaultImagesSetting](#defaultimagessetting) (si elle est définie) ou de la configuration personnelle de l’utilisateur.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ImagesAllowedForUrls
  - Nom de la stratégie de groupe: Autoriser les images sur ces sites
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ImagesAllowedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ImagesBlockedForUrls
  #### Bloquer les images sur des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez une liste de sites basée sur des modèles d’URL, qui ne sont pas autorisés à afficher des images.

Si vous ne configurez pas cette stratégie, la valeur par défaut globale de la stratégie [DefaultImagesSetting](#defaultimagessetting) (si elle est définie) ou de la configuration personnelle de l’utilisateur est utilisée pour tous les sites.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ImagesBlockedForUrls
  - Nom de la stratégie de groupe: Bloquer les images sur des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ImagesBlockedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### InsecureContentAllowedForUrls
  #### Autoriser le contenu non sécurisé sur les sites spécifiés
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 80 ou version ultérieure

  #### Description
  Créez la liste de modèles d’URL pour spécifier les sites qui peuvent afficher du contenu mixte non sécurisé (contenu HTTP sur les sites HTTPS).

Si vous ne configurez pas cette stratégie, le contenu mixte pouvant être bloqué le sera bloqué et le contenu mixte pouvant facultativement être bloqué sera mis à jour. Toutefois, les utilisateurs seront autorisés à définir des exceptions pour autoriser du contenu mixte non sécurisé pour des sites spécifiques.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: InsecureContentAllowedForUrls
  - Nom de la stratégie de groupe: Autoriser le contenu non sécurisé sur les sites spécifiés
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\2 = "[*.]example.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: InsecureContentAllowedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### InsecureContentBlockedForUrls
  #### Bloquer le contenu non sécurisé sur les sites spécifiés
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 80 ou version ultérieure

  #### Description
  Créez la liste des modèles d’URL pour spécifier les sites qui ne sont pas autorisés à afficher du contenu mixte pouvant être bloqué (c'est-à-dire actif) (contenu HTTP sur des sites HTTPS) et pour lesquels les mises à jour du contenu mixte pouvant facultativement être bloqué vont être désactivées.

Si vous ne configurez pas cette stratégie, le contenu mixte pouvant être bloqué le sera et le contenu mixte pouvant facultativement être bloqué sera mis à jour. Toutefois, les utilisateurs seront autorisés à définir des exceptions pour autoriser le contenu mixte non sécurisé pour des sites spécifiques.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: InsecureContentBlockedForUrls
  - Nom de la stratégie de groupe: Bloquer le contenu non sécurisé sur les sites spécifiés
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\2 = "[*.]example.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: InsecureContentBlockedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### JavaScriptAllowedForUrls
  #### Autoriser JavaScript sur des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez la liste des sites en fonction des modèles d’URL, qui sont autorisés à exécuter JavaScript.

Si vous ne configurez pas cette stratégie, la valeur par défaut globale de la stratégie [DefaultJavaScriptSetting](#defaultjavascriptsetting) (si elle est définie) ou de la configuration personnelle de l’utilisateur est utilisée pour tous les sites.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: JavaScriptAllowedForUrls
  - Nom de la stratégie de groupe: Autoriser JavaScript sur des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: JavaScriptAllowedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### JavaScriptBlockedForUrls
  #### Bloquer JavaScript sur des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez une liste de sites basée sur des modèles d’URL, qui ne sont pas autorisés à exécuter JavaScript.

Si vous ne configurez pas cette stratégie, la valeur par défaut globale de la stratégie [DefaultJavaScriptSetting](#defaultjavascriptsetting) (si elle est définie) ou de la configuration personnelle de l’utilisateur est utilisée pour tous les sites.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: JavaScriptBlockedForUrls
  - Nom de la stratégie de groupe: Bloquer JavaScript sur des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: JavaScriptBlockedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### LegacySameSiteCookieBehaviorEnabled
  #### Activer les paramètres de comportement de cookie SameSite hérité par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 80 ou version ultérieure

  #### Description
  Vous permet de rétablir tous les cookies au comportement SameSite hérité. Le rétablissement du comportement hérité entraîne le traitement des cookies qui ne spécifient pas d'attribut SameSite comme s’ils étaient « SameSite=None » et supprime la condition requise pour que les cookies « SameSite=None » transportent l’attribut « Secure ».

Si vous ne définissez pas cette stratégie, le comportement par défaut des cookies qui ne spécifient pas d'attribut SameSite dépendra d’autres sources de configuration pour la fonctionnalité SameSite-by-default. Cette fonctionnalité peut être définie par une période d’évaluation de champ ou par l’activation de l’indicateur same-site-by-default-cookies dans edge://flags.

Mappage des options de stratégie :

* DefaultToLegacySameSiteCookieBehavior (1) = Rétablir le comportement SameSite hérité pour les cookies sur tous les sites

* DefaultToSameSiteByDefaultCookieBehavior (2) = Utiliser le comportement SameSite-by-default pour les cookies sur tous les sites

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: LegacySameSiteCookieBehaviorEnabled
  - Nom de la stratégie de groupe: Activer les paramètres de comportement de cookie SameSite hérité par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: LegacySameSiteCookieBehaviorEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: LegacySameSiteCookieBehaviorEnabled
  - Exemple de valeur :
``` xml
<integer>1</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### LegacySameSiteCookieBehaviorEnabledForDomainList
  #### Rétablir le comportement SameSite hérité des cookies sur les sites spécifiés
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 80 ou version ultérieure

  #### Description
  Les cookies définis pour les modèles spécifiés correspondant au domaine sont rétablis vers l’ancien comportement SameSite.

Le rétablissement du comportement hérité entraîne le traitement des cookies qui ne spécifient pas d'attribut SameSite comme s’ils étaient « SameSite=None » et supprime la condition requise pour que les cookies « SameSite=None » transportent l’attribut « Secure ».

Si vous ne définissez pas cette stratégie, la valeur par défaut globale est utilisée. La valeur par défaut globale est également utilisée pour les cookies sur les domaines non couverts par les modèles que vous spécifiez.

La valeur par défaut globale peut être configurée à l’aide de la stratégie [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled). Si [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) n’est pas défini, la valeur par défaut globale est rétablie à d'autres sources de configuration.

Notez que les modèles que vous répertoriez dans cette stratégie sont traités comme des domaines et non des URL. Vous ne devez donc pas spécifier de modèle ni de port.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Nom de la stratégie de groupe: Rétablir le comportement SameSite hérité des cookies sur les sites spécifiés
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\1 = "www.example.com"
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\2 = "[*.]example.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Exemple de valeur :
``` xml
<array>
  <string>www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### NotificationsAllowedForUrls
  #### Autoriser les notifications sur des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Vous permet de créer une liste de modèles d’URL pour spécifier les sites qui sont autorisés à afficher les notifications.

Si vous ne configurez pas cette stratégie, la valeur globale par défaut est utilisée pour tous les sites. Cette valeur par défaut est comprise dans la stratégie [DefaultNotificationsSetting](#defaultnotificationssetting) si elle est définie ou dans la configuration personnelle de l’utilisateur. Pour plus d’informations sur les modèles d’URL valides, consultez [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: NotificationsAllowedForUrls
  - Nom de la stratégie de groupe: Autoriser les notifications sur des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: NotificationsAllowedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### NotificationsBlockedForUrls
  #### Bloquer les notifications sur des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Vous permet de créer une liste de modèles d’URL pour spécifier les sites qui ne sont pas autorisés à afficher les notifications.

Si vous ne configurez pas cette stratégie, la valeur globale par défaut est utilisée pour tous les sites. Cette valeur par défaut est comprise dans la stratégie [DefaultNotificationsSetting](#defaultnotificationssetting) si elle est définie ou dans la configuration personnelle de l’utilisateur. Pour plus d’informations sur les modèles d’URL valides, consultez [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: NotificationsBlockedForUrls
  - Nom de la stratégie de groupe: Bloquer les notifications sur des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: NotificationsBlockedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PluginsAllowedForUrls
  #### Autoriser le plug-in Adobe Flash sur des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez la liste des sites, en fonction des modèles d'URL, qui peuvent exécuter le plug-in Adobe Flash.

Si vous ne configurez pas cette stratégie, la valeur globale par défaut de la stratégie [DefaultPluginsSetting](#defaultpluginssetting) (si elle est définie) ou de la configuration personnelle de l’utilisateur est utilisée pour tous les sites.

Si vous souhaitez obtenir des informations détaillées sur les modèles d’URL valides, consultez [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Toutefois, à partir de M85, les modèles contenant les caractères génériques « * » et « [*.] » dans l’hôte ne sont plus pris en charge pour cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PluginsAllowedForUrls
  - Nom de la stratégie de groupe: Autoriser le plug-in Adobe Flash sur des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\2 = "http://contoso.edu:8080"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PluginsAllowedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PluginsBlockedForUrls
  #### Bloquer le plug-in Adobe Flash sur des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez la liste des sites, en fonction des modèles d'URL, qui ne peuvent pas exécuter Adobe Flash.

Si vous ne configurez pas cette stratégie, la valeur globale par défaut de la stratégie [DefaultPluginsSetting](#defaultpluginssetting) (si elle est définie) ou de la configuration personnelle de l’utilisateur est utilisée pour tous les sites.

Si vous souhaitez obtenir des informations détaillées sur les modèles d’URL valides, consultez [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Toutefois, à partir de M85, les modèles contenant les caractères génériques « * » et « [*.] » dans l’hôte ne sont plus pris en charge pour cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PluginsBlockedForUrls
  - Nom de la stratégie de groupe: Bloquer le plug-in Adobe Flash sur des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\2 = "http://contoso.edu:8080"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PluginsBlockedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PopupsAllowedForUrls
  #### Autoriser les fenêtres contextuelles sur des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez une liste de sites basée sur des modèles d’URL, qui peuvent ouvrir des fenêtres contextuelles.

Si vous ne configurez pas cette stratégie, la valeur par défaut globale de la stratégie [DefaultPopupsSetting](#defaultpopupssetting) (si elle est définie) ou de la configuration personnelle de l’utilisateur est utilisée pour tous les sites.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PopupsAllowedForUrls
  - Nom de la stratégie de groupe: Autoriser les fenêtres contextuelles sur des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PopupsAllowedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PopupsBlockedForUrls
  #### Bloquer les fenêtres contextuelles sur des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez une liste de sites basée sur des modèles d’URL, qui ne peuvent pas ouvrir des fenêtres contextuelles.

Si vous ne configurez pas cette stratégie, la valeur par défaut globale de valeur de la stratégie [DefaultPopupsSetting](#defaultpopupssetting) (si elle est définie) ou de la configuration personnelle de l’utilisateur est utilisée pour tous les sites.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PopupsBlockedForUrls
  - Nom de la stratégie de groupe: Bloquer les fenêtres contextuelles sur des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PopupsBlockedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### RegisteredProtocolHandlers
  #### Inscrire les gestionnaires de protocole
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Configurez cette stratégie (recommandé uniquement) pour inscrire une liste de gestionnaires de protocoles. Cette liste est fusionnée avec celles inscrites par l’utilisateur et elles sont toutes utilisables.

Pour inscrire un gestionnaire de protocole :

-Définir la propriété du protocole sur le modèle (par exemple, « mailto »)
-Définir la propriété URL de l’application qui gère le schéma spécifié dans le champ « protocole ». Le modèle peut inclure un espace réservé « %s », lequel est remplacé par l’URL gérée.

Les utilisateurs ne peuvent pas supprimer un gestionnaire de protocole inscrit par cette stratégie. Ils peuvent toutefois installer un nouveau gestionnaire de protocole par défaut pour remplacer les gestionnaires de protocoles existants.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Non
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Dictionnaire

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: RegisteredProtocolHandlers
  - Nom de la stratégie de groupe: Inscrire les gestionnaires de protocole
  - Chemin d'accès à la stratégie de groupe (Obligatoire): N/A
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/Paramètres de contenu
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): N/A
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: RegisteredProtocolHandlers
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [
  {
    "default": true, 
    "protocol": "mailto", 
    "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"
  }
]
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: RegisteredProtocolHandlers
  - Exemple de valeur :
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
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SpotlightExperiencesAndRecommendationsEnabled
  #### Déterminez si les utilisateurs peuvent recevoir des images d’arrière-plan et du texte personnalisés, des suggestions, des notifications
et des conseils pour les services Microsoft
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 86 ou ultérieur

  #### Description
  Déterminez si les utilisateurs peuvent recevoir des images d’arrière-plan et du texte personnalisés, des suggestions, des notifications et des conseils pour les services Microsoft.

              Si vous activez ce paramètre ou ne le configurez pas, les expériences et recommandations à la une sont activées.

Si vous désactivez ce paramètre, les expériences et recommandations à la une sont désactivées.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SpotlightExperiencesAndRecommendationsEnabled
  - Nom de la stratégie de groupe: Déterminez si les utilisateurs peuvent recevoir des images d’arrière-plan et du texte personnalisés, des suggestions, des notifications
et des conseils pour les services Microsoft
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: SpotlightExperiencesAndRecommendationsEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### WebUsbAllowDevicesForUrls
  #### Accorder l’accès à des sites spécifiques pour se connecter à des périphériques USB spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Permet de définir la liste des URL indiquant les sites qui sont automatiquement autorisés à accéder à un périphérique USB avec les ID produit et fournisseur spécifiés. Chaque élément de la liste doit contenir à la fois les appareils et les URL pour que la stratégie soit valide. Chaque élément des appareils peut contenir un champ d’ID fournisseur et produit. Tout ID omis est traité comme un caractère générique avec une exception et cette exception indique qu’un ID produit ne peut pas être spécifié sans qu’un ID fournisseur soit également spécifié. Sinon, la stratégie n'est pas valide et est ignorée.

Le modèle d’autorisation USB utilise l’URL du site demandeur (« URL de demande ») et l’URL du site de cadre de niveau supérieur (« URL d’incorporation ») pour accorder l’autorisation à l’URL de demande d’accéder au périphérique USB. L’URL de demande peut être différente de l’URL d’incorporation si le site demandeur est chargé dans un IFRAME. Par conséquent, le champ « URL » peut contenir jusqu’à deux chaînes d’URL séparées par une virgule pour spécifier respectivement l’URL de demande et l’URL d’incorporation. Si une seule URL est spécifiée, l’accès aux périphériques USB correspondants est accordé si l’URL du site demandeur correspond à cette URL, quel que soit le statut d’incorporation. Les URL dans « URL » doivent être des URL valides, sinon la stratégie est ignorée.

Si cette stratégie n’est pas définie, la valeur par défaut globale est utilisée pour tous les sites à partir de la stratégie [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) si elle est définie, ou de la configuration personnelle de l’utilisateur.

Les modèles d’URL de cette stratégie ne doivent pas entrer en conflit avec ceux configurés via [WebUsbBlockedForUrls](#webusbblockedforurls). En cas de conflit, cette stratégie est prioritaire sur les stratégies [WebUsbBlockedForUrls](#webusbblockedforurls) et [WebUsbAskForUrls](#webusbaskforurls).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Dictionnaire

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: WebUsbAllowDevicesForUrls
  - Nom de la stratégie de groupe: Accorder l’accès à des sites spécifiques pour se connecter à des périphériques USB spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: WebUsbAllowDevicesForUrls
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
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


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: WebUsbAllowDevicesForUrls
  - Exemple de valeur :
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
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### WebUsbAskForUrls
  #### Autoriser WebUSB sur des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez la liste des sites en fonction des modèles d'URL, qui peuvent demander à l’utilisateur l’accès à un appareil USB.

Si vous ne configurez pas cette stratégie, la valeur par défaut globale de valeur de la stratégie [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (si elle est définie) ou de la configuration personnelle de l’utilisateur est utilisée pour tous les sites.

Les modèles d’URL définis dans cette stratégie ne peuvent pas entrer en conflit avec ceux configurés dans la stratégie [WebUsbBlockedForUrls](#webusbblockedforurls) : vous ne pouvez pas à la fois autoriser et bloquer une URL. Si vous souhaitez en savoir plus sur les modèles d’URL valides, veuillez consulter [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: WebUsbAskForUrls
  - Nom de la stratégie de groupe: Autoriser WebUSB sur des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: WebUsbAskForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### WebUsbBlockedForUrls
  #### Bloquer WebUSB sur des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez la liste des sites en fonction des modèles d'URL qui ne peuvent pas demander à l’utilisateur de leur accorder l’accès à un appareil USB.

Si vous ne configurez pas cette stratégie, la valeur par défaut globale de valeur de la stratégie [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (si elle est définie) ou de la configuration personnelle de l’utilisateur est utilisée pour tous les sites.

Les modèles d’URL dans cette stratégie ne peuvent pas entrer en conflit avec ceux configurés dans la stratégie [WebUsbAskForUrls](#webusbaskforurls). Vous ne pouvez pas à la fois autoriser et bloquer une URL. Si vous souhaitez en savoir plus sur les modèles d’URL valides, voir [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: WebUsbBlockedForUrls
  - Nom de la stratégie de groupe: Bloquer WebUSB sur des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres de contenu
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: WebUsbBlockedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ## Paramètres d’Application Guard policies

  [Revenir au début](#microsoft-edge---stratégies)

  ### ApplicationGuardContainerProxy
  #### Proxy de conteneur Application Guard
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 84 ou ultérieur

  #### Description
  Configure les paramètres de proxy pour Microsoft Edge Application Guard.
          Si vous activez cette stratégie, Microsoft Edge Application Guard ignore les autres sources de configuration proxy.

         Si vous ne configurez pas cette stratégie, Microsoft Edge Application Guard utilise la configuration proxy de l’hôte.

         Cette stratégie n’affecte pas la configuration proxy de Microsoft Edge en dehors d’application Guard (sur l’hôte).

         Le champ ProxyMode vous permet de spécifier le serveur proxy utilisé par Microsoft Edge Application Guard.

         Le champ ProxyPacUrl est une URL vers un fichier proxy. PAC.

Le champ ProxyServer est une URL pour le serveur proxy.

Si vous choisissez la valeur « directe » comme « ProxyMode », tous les autres champs sont ignorés.

         Si vous choisissez la valeur « auto_detect » comme «ProxyMode», tous les autres champs sont ignorés.

         Si vous choisissez la valeur « fixed_servers » comme «ProxyMode», le champ «ProxyServer» est utilisé.

Si vous choisissez la valeur « pac_script » comme «ProxyMode», le champ «ProxyPacUrl» est utilisé.

         Pour plus d'informations sur l'identification du trafic d'Application Guard via un double proxy, consultez le site [https://go.microsoft.com/fwlink/?linkid=2134653](https://go.microsoft.com/fwlink/?linkid=2134653).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Dictionnaire

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ApplicationGuardContainerProxy
  - Nom de la stratégie de groupe: Proxy de conteneur Application Guard
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Paramètres d’Application Guard
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ApplicationGuardContainerProxy
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ## Serveur proxy policies

  [Revenir au début](#microsoft-edge---stratégies)

  ### ProxyBypassList
  #### Configurer les règles de contournement du proxy
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définit une liste d’hôtes pour lesquels Microsoft Edge contourne un proxy.

Cette stratégie est appliquée uniquement si vous avez sélectionné « Utiliser des serveurs de proxy fixes » dans la stratégie [ProxyMode](#proxymode). Si vous avez sélectionné un autre mode de configuration des stratégies de proxy, n’activez pas cette stratégie ou ne la configurez pas.

Si vous activez cette stratégie, vous pouvez créer une liste d’hôtes pour lesquels Microsoft Edge n’utilise pas de proxy.

Si vous ne configurez pas cette stratégie, aucune liste d’hôtes n’est créée pour laquelle Microsoft Edge contourne un proxy. Ne configurez pas cette stratégie si vous avez spécifié une autre méthode de définition des stratégies de proxy.

Pour obtenir des exemples plus détaillés, rendez-vous sur [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ProxyBypassList
  - Nom de la stratégie de groupe: Configurer les règles de contournement du proxy
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Serveur proxy
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ProxyBypassList
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"https://www.contoso.com, https://www.fabrikam.com"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ProxyBypassList
  - Exemple de valeur :
``` xml
<string>https://www.contoso.com, https://www.fabrikam.com</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ProxyMode
  #### Configurer les paramètres du serveur proxy
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifiez les paramètres de serveur proxy utilisés par Microsoft Edge. Si vous activez cette stratégie, les utilisateurs ne peuvent pas modifier les paramètres de proxy.

Si vous choisissez de ne jamais utiliser de serveur proxy et de toujours vous connecter directement, toutes les autres options sont ignorées.

Si vous choisissez d’utiliser les paramètres de proxy système, toutes les autres options sont ignorées.

Si vous choisissez de détecter automatiquement le serveur proxy, toutes les autres options sont ignorées.

Si vous choisissez le mode proxy de serveur fixe, vous pouvez spécifier des options supplémentaires dans [ProxyServer](#proxyserver) et « Liste séparée par des virgules des règles de contournement de proxy ».

Si vous choisissez d’utiliser un script de proxy .pac, vous devez spécifier l’URL du script dans « URL vers le fichier .pac du proxy ».

Pour obtenir des exemples détaillés, accédez à [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

Si vous activez cette stratégie, Microsoft Edge ignore toutes les options liées au proxy spécifiées à partir de la ligne de commande.

Si vous ne configurez pas cette stratégie, les utilisateurs peuvent choisir leurs propres paramètres de proxy.

Mappage des options de stratégie :

* ProxyDisabled (direct) = Ne jamais utiliser un proxy

* ProxyAutoDetect (auto_detect) = Détection automatique des paramètres de proxy

* ProxyPacScript (pac_script) = Utiliser un script de proxy .pac

* ProxyFixedServers (fixed_servers) = Utiliser des serveurs de proxy fixes

* ProxyUseSystem (system) = Utiliser les paramètres proxy du système

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ProxyMode
  - Nom de la stratégie de groupe: Configurer les paramètres du serveur proxy
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Serveur proxy
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ProxyMode
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"direct"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ProxyMode
  - Exemple de valeur :
``` xml
<string>direct</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ProxyPacUrl
  #### Définir l'URL du fichier .pac du proxy
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifie l’URL d’un fichier de configuration automatique de proxy (PAC).

Cette stratégie est appliquée uniquement si vous avez sélectionné « Utiliser un script de proxy .pac » dans la stratégie e [ProxyMode](#proxymode). Si vous avez sélectionné un autre mode de configuration des stratégies de proxy, n’activez ou ne configurez pas cette stratégie.

Si vous activez cette stratégie, vous pouvez spécifier l’URL d’un fichier PAC, qui définit la manière dont le navigateur choisit automatiquement le serveur proxy approprié pour l’extraction d’un site web particulier.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, aucun fichier PAC n’est spécifié. Ne configurez pas cette stratégie si vous avez spécifié une autre méthode pour la définition des stratégies de proxy.

Pour obtenir des exemples détaillés, voir [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ProxyPacUrl
  - Nom de la stratégie de groupe: Définir l'URL du fichier .pac du proxy
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Serveur proxy
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ProxyPacUrl
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"https://internal.contoso.com/example.pac"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ProxyPacUrl
  - Exemple de valeur :
``` xml
<string>https://internal.contoso.com/example.pac</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ProxyServer
  #### Configurer l’adresse ou l’URL du serveur proxy
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifie l’URL du serveur proxy.

Cette stratégie est appliquée uniquement si vous avez sélectionné « Utiliser des serveurs de proxy fixes » dans la stratégie [ProxyMode](#proxymode). Si vous avez sélectionné un autre mode de configuration des stratégies de proxy, n’activez pas cette stratégie ou ne la configurez pas.

Si vous activez cette stratégie, le serveur proxy configuré par cette stratégie est utilisé pour toutes les URL.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, les utilisateurs peuvent choisir leurs propres paramètres de proxy lorsqu’ils sont en mode proxy. Ne configurez pas cette stratégie si vous avez spécifié une autre méthode de configuration des stratégies de proxy.

Pour obtenir plus d’options et des exemples détaillés, rendez-vous sur [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ProxyServer
  - Nom de la stratégie de groupe: Configurer l’adresse ou l’URL du serveur proxy
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Serveur proxy
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ProxyServer
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"123.123.123.123:8080"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ProxyServer
  - Exemple de valeur :
``` xml
<string>123.123.123.123:8080</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ProxySettings
  #### Paramètres du proxy
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Configure les paramètres de proxy pour Microsoft Edge.

Si vous activez cette stratégie, Microsoft Edge ignore toutes les options liées au proxy spécifiées à partir de la ligne de commande.

Si vous ne configurez pas cette stratégie, les utilisateurs peuvent choisir leurs propres paramètres de proxy.

Cette stratégie remplace les stratégies individuelles suivantes :

[ProxyMode](#proxymode)
[ProxyPacUrl](#proxypacurl)
[ProxyServer](#proxyserver)
[ProxyBypassList](#proxybypasslist)

Le champ ProxyMode vous permet de spécifier le serveur proxy utilisé par Microsoft Edge et empêche les utilisateurs de modifier les paramètres de proxy.

Le champ ProxyPacUrl est une URL vers un fichier .pac de proxy.

Le champ ProxyServer est une URL pour le serveur proxy.

Le champ ProxyBypassList est une liste des hôtes proxy contournés par Microsoft Edge.

Si vous choisissez la valeur « direct » pour « ProxyMode », un proxy n’est jamais utilisé et tous les autres champs sont ignorés.

Si vous choisissez la valeur « system » pour « ProxyMode », le proxy du système est utilisé et tous les autres champs sont ignorés.

Si vous choisissez la valeur « auto_detect » pour « ProxyMode », tous les autres champs sont ignorés.

Si vous choisissez la valeur « fixed_server » pour « ProxyMode », les champs « ProxyServer » et « ProxyBypassList » sont utilisés.

Si vous choisissez la valeur « pac_script » pour « ProxyMode », les champs « ProxyPacUrl » et « ProxyBypassList » sont utilisés.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Dictionnaire

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ProxySettings
  - Nom de la stratégie de groupe: Paramètres du proxy
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/Serveur proxy
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ProxySettings
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {
  "ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", 
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ProxySettings
  - Exemple de valeur :
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
  

  [Revenir au début](#microsoft-edge---stratégies)

  ## Additional policies

  [Revenir au début](#microsoft-edge---stratégies)

  ### AddressBarMicrosoftSearchInBingProviderEnabled
  #### Activer les suggestions de Recherche Microsoft dans Bing dans la barre d’adresse
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 81 ou version ultérieure

  #### Description
  Permet d’afficher les suggestions de Recherche Microsoft dans Bing appropriées dans la liste de suggestions de la barre d’adresse lorsque l’utilisateur tape une chaîne de recherche dans la barre d’adresse. Si vous activez cette stratégie ou si vous ne la configurez pas, les utilisateurs peuvent voir les résultats internes obtenus par Recherche Microsoft dans Bing dans la liste de suggestions de la barre d’adresse de Microsoft Edge. Pour afficher les résultats de Recherche Microsoft dans Bing, l’utilisateur doit être connecté à Microsoft Edge avec son compte Azure AD pour cette organisation.
Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas voir les résultats internes dans la liste de suggestions de la barre d’adresse de Microsoft Edge.
Si vous avez activé l’ensemble de stratégies qui force un moteur de recherche par défaut ([DefaultSearchProviderEnabled](#defaultsearchproviderenabled), [DefaultSearchProviderName](#defaultsearchprovidername) et [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)), et si le moteur de recherche spécifié n’est pas Bing, cette stratégie n’est pas applicable et aucune suggestion de Recherche Microsoft dans Bing n’apparaît dans la liste de suggestions de la barre d’adresse.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AddressBarMicrosoftSearchInBingProviderEnabled
  - Nom de la stratégie de groupe: Activer les suggestions de Recherche Microsoft dans Bing dans la barre d’adresse
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AddressBarMicrosoftSearchInBingProviderEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AddressBarMicrosoftSearchInBingProviderEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AdsSettingForIntrusiveAdsSites
  #### Paramètres des annonces pour les sites contenant des annonces gênantes
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 78 ou version ultérieure

  #### Description
  Détermine si les publicités sont bloquées sur des sites avec des publicités intrusives.

Mappage des options de stratégie :

* AllowAds (1) = Autoriser les annonces sur tous les sites

* BlockAds (2) = Bloquez les publicités sur les sites contenant des annonces gênantes (valeur par défaut).

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AdsSettingForIntrusiveAdsSites
  - Nom de la stratégie de groupe: Paramètres des annonces pour les sites contenant des annonces gênantes
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AdsSettingForIntrusiveAdsSites
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AdsSettingForIntrusiveAdsSites
  - Exemple de valeur :
``` xml
<integer>1</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AllowDeletingBrowserHistory
  #### Activer la suppression de l'historique du navigateur et des téléchargements
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Permet de supprimer l’historique du navigateur et l'historique de téléchargement, et empêche les utilisateurs de modifier ce paramètre.

Notez que même si cette stratégie est désactivée, il n'est pas garanti que l’historique de navigation et de téléchargement sont conservés : les utilisateurs peuvent modifier ou supprimer directement les fichiers de base de données de l’historique, et le navigateur peut supprimer (en se basant sur la période d’expiration) ou archiver tout ou partie des éléments de l’historique à tout moment.

Si vous activez cette stratégie ou si vous ne la configurez pas, les utilisateurs peuvent supprimer l’historique de navigation et de téléchargement.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas supprimer l'historique de navigation et de téléchargement.

Si vous activez cette stratégie, n’activez pas la stratégie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit), car toutes deux concernent la suppression de données. Si vous les activez toutes les deux, la stratégie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) est prioritaire et supprime toutes les données à la fermeture de Microsoft Edge, quelle que soit la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AllowDeletingBrowserHistory
  - Nom de la stratégie de groupe: Activer la suppression de l'historique du navigateur et des téléchargements
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AllowDeletingBrowserHistory
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AllowDeletingBrowserHistory
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AllowFileSelectionDialogs
  #### Boîtes de dialogue Autoriser la sélection de fichiers
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Autoriser l’accès aux fichiers locaux en autorisant Microsoft Edge à afficher les boîtes de dialogue de sélection de fichier.

	Si vous activez ou ne configurez pas cette stratégie, les utilisateurs peuvent ouvrir des boîtes de dialogue de sélection de fichier comme d’habitude.

	Si vous désactivez cette stratégie, chaque fois que l’utilisateur effectue une action qui déclenche une boîte de dialogue de sélection de fichier (par exemple, l’importation des favoris, le téléchargement de fichiers ou l’enregistrement de liens), un message s’affiche et l’utilisateur est supposé avoir cliqué sur Annuler dans la boîte de dialogue de sélection de fichier.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AllowFileSelectionDialogs
  - Nom de la stratégie de groupe: Boîtes de dialogue Autoriser la sélection de fichiers
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AllowFileSelectionDialogs
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AllowFileSelectionDialogs
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AllowPopupsDuringPageUnload
  #### Autorise une page à afficher les fenêtres contextuelles pendant son déchargement
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 78 ou version ultérieure

  #### Description
  Cette stratégie permet à un administrateur de spécifier qu’une page peut afficher des fenêtres contextuelles pendant le déchargement.

Lorsque la stratégie est activée, les pages sont autorisées à afficher des fenêtres contextuelles pendant leur déchargement.

Lorsque la stratégie est définie sur désactivé ou non défini, les pages ne sont pas autorisées à afficher des fenêtres contextuelles pendant leur déchargement. Ceci est conforme à la spécification : (https://html.spec.whatwg.org/#apis-for-creating-and-navigating-browsing-contexts-by-name).

Cette stratégie sera supprimée à l'avenir.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AllowPopupsDuringPageUnload
  - Nom de la stratégie de groupe: Autorise une page à afficher les fenêtres contextuelles pendant son déchargement
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AllowPopupsDuringPageUnload
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AllowPopupsDuringPageUnload
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AllowSurfGame
  #### Autoriser le jeu du surf
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 83 ou version ultérieure

  #### Description
  Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas jouer au jeu du surf lorsque l’appareil est hors connexion ou si l’utilisateur accède à edge://surf.

Si vous activez cette stratégie ou si vous ne la configurez pas, les utilisateurs peuvent jouer au jeu du surf.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AllowSurfGame
  - Nom de la stratégie de groupe: Autoriser le jeu du surf
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AllowSurfGame
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AllowSurfGame
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AllowSyncXHRInPageDismissal
  #### Autoriser les pages à envoyer des demandes XHR synchrones lors de l’opération de rejet de page (déconseillé)
  >DÉCONSEILLÉ : cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 79 ou version ultérieure

  #### Description
  Cette stratégie est déconseillée car elle n'est qu'un mécanisme à court terme qui permet aux entreprises de mettre à jour le contenu de leur site web si et quand il s'avère incompatible avec la modification qui consiste à refuser les demandes de RXH synchrones lors du renvoi d'une page. Elle ne fonctionnera pas dans Microsoft Edge version 88.

Cette stratégie vous permet de spécifier qu’une page peut envoyer des demandes XHR synchrones lors d’un renvoi de page.

Si vous activez cette stratégie, les pages peuvent envoyer des demandes XHR synchrones pendant un renvoi de page.

Si vous désactivez cette stratégie ou ne configurez pas cette stratégie, les pages ne sont pas autorisées à envoyer des demandes XHR synchrones pendant le renvoi de la page.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AllowSyncXHRInPageDismissal
  - Nom de la stratégie de groupe: Autoriser les pages à envoyer des demandes XHR synchrones lors de l’opération de rejet de page (déconseillé)
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AllowSyncXHRInPageDismissal
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AllowSyncXHRInPageDismissal
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AllowTokenBindingForUrls
  #### Configurez la liste des sites avec lesquels Microsoft Edge va tenter d’établir une liaison de jeton
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 83 ou ultérieur

  #### Description
  Configurez la liste des modèles d’URL des sites avec lesquels le navigateur essaiera d’effectuer le protocole de liaison de jetons.
Pour les domaines de cette liste, le navigateur envoie la liaison de jetons ClientHello dans la négociation TLS (voir https://tools.ietf.org/html/rfc8472).
Si le serveur répond par une réponse ServerHello valide, le navigateur crée et envoie des messages de liaison de jetons sur les futures demandes HTTPS. Pour plus d’informations, voir https://tools.ietf.org/html/rfc8471.

Si cette liste est vide, la liaison de jetons est désactivée.

Cette stratégie est disponible uniquement sur les appareils Windows 10 disposant d’une fonctionnalité de Mode sécurisé virtuel.

À partir de Microsoft Edge 86, cette stratégie ne prend plus en charge l’actualisation dynamique.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AllowTokenBindingForUrls
  - Nom de la stratégie de groupe: Configurez la liste des sites avec lesquels Microsoft Edge va tenter d’établir une liaison de jeton
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\2 = "[*.]mydomain2.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\3 = "[*.].mydomain2.com"

```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AllowTrackingForUrls
  #### Configurer les exceptions de prévention du suivi pour des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 78 ou version ultérieure

  #### Description
  Configurez la liste des modèles d'URL qui sont exclus de la prévention du suivi.

	Si vous configurez cette stratégie, la liste des modèles d'URL configurés est exclue de la prévention du suivi.

	Si vous ne configurez pas cette stratégie, la valeur globale par défaut provenant de la stratégie « Bloquer le suivi des activités de navigation des utilisateurs » (si définie) ou la configuration personnelle de l'utilisateur est utilisée pour tous les sites.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AllowTrackingForUrls
  - Nom de la stratégie de groupe: Configurer les exceptions de prévention du suivi pour des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AllowTrackingForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AlternateErrorPagesEnabled
  #### Suggérer des pages similaires lorsqu’une page web est introuvable
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 80 ou version ultérieure

  #### Description
  Autorisez Microsoft Edge à émettre une connexion à un service web pour générer des suggestions d’URL et de recherche pour des problèmes de connectivité, tels que des erreurs DNS.

Si vous activez cette stratégie, un service web permet de générer des suggestions d’URL et de recherche pour les erreurs réseau.

Si vous désactivez cette stratégie, aucun appel au service web n’est effectué et une page d’erreur standard est affichée.

Si vous ne configurez pas cette stratégie, Microsoft Edge respecte la préférence de l’utilisateur définie sous Services sur edge://settings/privacy.
Plus précisément, la présence du bouton bascule **Suggérer des pages similaires lorsqu’une page web est introuvable** permet à l’utilisateur d’activer ou de désactiver cette fonction. Notez que si vous avez activé cette stratégie (AlternateErrorPagesEnabled), le paramètre Suggérer des pages similaires lorsqu’une page web est introuvable est activé, mais l’utilisateur ne peut pas modifier le paramètre à l’aide du bouton bascule. Si vous désactivez cette stratégie, le paramètre Suggérer des pages similaires lorsqu’une page web est introuvable est désactivé et l’utilisateur ne peut pas modifier le paramètre à l’aide du bouton bascule.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AlternateErrorPagesEnabled
  - Nom de la stratégie de groupe: Suggérer des pages similaires lorsqu’une page web est introuvable
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: AlternateErrorPagesEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AlternateErrorPagesEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AlwaysOpenPdfExternally
  #### Toujours ouvrir les fichiers PDF en externe
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Désactive la visionneuse PDF interne dans Microsoft Edge.

	Si vous activez cette stratégie, Microsoft Edge traite les fichiers PDF comme des téléchargements et permet aux utilisateurs de les ouvrir avec l’application par défaut.

	Si vous ne configurez cette stratégie ou si vous la désactivez, Microsoft Edge ouvre les fichiers PDF (sauf si l’utilisateur désactive cette stratégie).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AlwaysOpenPdfExternally
  - Nom de la stratégie de groupe: Toujours ouvrir les fichiers PDF en externe
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AlwaysOpenPdfExternally
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AlwaysOpenPdfExternally
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AmbientAuthenticationInPrivateModesEnabled
  #### Activer l’authentification ambiante pour les profils Invité et InPrivate
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 81 ou version ultérieure

  #### Description
  Configurez cette stratégie pour autoriser/refuser l’authentification ambiante pour les profils InPrivate et Invité dans Microsoft Edge.

L’authentification ambiante est une authentification HTTP avec des informations d’identification par défaut lorsque les informations d’identification explicites ne sont pas fournies via les schémas de test/réponse NTLM/Kerberos/Negotiate.

Si vous définissez la stratégie sur RegularOnly, elle autorise l’authentification ambiante uniquement pour les sessions normales. Les sessions InPrivate et Invité ne sont pas autorisées à s’authentifier de manière ambiante.

Si vous définissez la stratégie sur InPrivateAndRegular, elle autorise l’authentification ambiante pour les sessions InPrivate et normale. Les sessions Invité ne seront pas autorisées à s’authentifier de manière ambiante.

Si vous définissez la stratégie sur GuestAndRegular, elle autorise l’authentification ambiante pour les sessions Invité et normale. Les sessions InPrivate ne seront pas autorisées à s’authentifier de manière ambiante

Si vous définissez la stratégie sur All, elle autorise l’authentification ambiante pour toutes les sessions.

Notez que l’authentification ambiante est toujours autorisée sur les profils normaux.

Dans Microsoft Edge version 81 et ultérieure, si la stratégie n’est pas définie, l’authentification ambiante est activée uniquement dans les sessions normales.

Mappage des options de stratégie :

* RegularOnly (0) = Activer l’authentification ambiante dans les sessions standard uniquement

* InPrivateAndRegular (1) = Activer l’authentification ambiante dans les sessions InPrivate et classiques

* GuestAndRegular (2) = Activer l’authentification ambiante dans les sessions invité et normales

* All (3) = Activer l’authentification ambiante dans les sessions standard, InPrivate et invité

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AmbientAuthenticationInPrivateModesEnabled
  - Nom de la stratégie de groupe: Activer l’authentification ambiante pour les profils Invité et InPrivate
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AmbientAuthenticationInPrivateModesEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AmbientAuthenticationInPrivateModesEnabled
  - Exemple de valeur :
``` xml
<integer>0</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AppCacheForceEnabled
  #### Permet de réactiver la fonctionnalité AppCache, même si elle est désactivée par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 84 ou version ultérieure

  #### Description
  Si vous définissez cette stratégie sur True, AppCache est activé, même lorsque AppCache dans Microsoft Edge n’est pas disponible par défaut.

Si vous affectez la valeur False à cette stratégie, ou si vous ne la définissez pas, AppCache suit les valeurs par défaut de Microsoft Edge.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AppCacheForceEnabled
  - Nom de la stratégie de groupe: Permet de réactiver la fonctionnalité AppCache, même si elle est désactivée par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AppCacheForceEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AppCacheForceEnabled
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ApplicationLocaleValue
  #### Définir les paramètres régionaux de l'application
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 77 ou ultérieur

  #### Description
  Configure les paramètres régionaux de l'application dans Microsoft Edge et empêche les utilisateurs de modifier les paramètres régionaux.

	Si vous activez cette stratégie, Microsoft Edge utilise les paramètres régionaux spécifiés. Si le paramètre régional configuré n’est pas pris en charge, « en-US » est utilisé à la place.

	Si vous désactivez ou ne configurez pas ce paramètre, Microsoft Edge utilise les paramètres régionaux par défaut spécifiés par l’utilisateur (si configurés) ou le paramètre régional « en-US » de secours.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ApplicationLocaleValue
  - Nom de la stratégie de groupe: Définir les paramètres régionaux de l'application
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: ApplicationLocaleValue
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"en"
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AudioCaptureAllowed
  #### Autoriser ou bloquer la capture audio
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Permet de définir si un utilisateur est invité à autoriser un site web à accéder à son appareil de capture audio. Cette stratégie s’applique à toutes les URL, à l’exception de celles qui sont configurées dans la liste [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Si vous activez cette stratégie ou ne la configurez pas (le paramètre par défaut), l’utilisateur est invité à accorder l’accès aux captures audio, à l’exception des URL de la liste [AudioCaptureAllowedUrls](#audiocaptureallowedurls). Ces URL répertoriées bénéficient d'un accès sans invite.

Si vous désactivez cette stratégie, l’utilisateur n’est pas invité et la capture audio n'est accessible que pour les URL configurées dans [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Cette stratégie affecte tous les types d’entrées audio, pas uniquement le microphone intégré.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AudioCaptureAllowed
  - Nom de la stratégie de groupe: Autoriser ou bloquer la capture audio
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AudioCaptureAllowed
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AudioCaptureAllowed
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AudioCaptureAllowedUrls
  #### Sites pouvant accéder aux appareils de capture audio sans demander l’autorisation
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifiez les sites web, en fonction de modèles d’URL, qui peuvent utiliser des appareils de capture audio sans demander l’autorisation de l'utilisateur. Les modèles de cette liste sont comparés à l’origine de sécurité de l’URL d'incorporation. S'ils correspondent, le site reçoit automatiquement l’accès à des appareils de capture audio.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AudioCaptureAllowedUrls
  - Nom de la stratégie de groupe: Sites pouvant accéder aux appareils de capture audio sans demander l’autorisation
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AudioCaptureAllowedUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AudioSandboxEnabled
  #### Autoriser l’exécution du bac à sable audio
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 81 ou version ultérieure

  #### Description
  Cette stratégie contrôle le bac à sable du processus audio.

Si vous activez cette stratégie, le processus audio s’exécute en mode bac à sable.

Si vous désactivez cette stratégie, le processus audio ne s’exécute pas en mode bac à sable, et le module de traitement audio WebRTC s’exécute lors du processus du convertisseur.
Cela rend les utilisateurs ouverts aux risques de sécurité liés à l’exécution du sous-système audio sans bac à sable.

Si vous ne configurez pas cette stratégie, la configuration par défaut pour le bac à sable audio est utilisée, ce qui peut varier en fonction de la plateforme.

Cette stratégie est destinée à offrir aux entreprises de la souplesse pour désactiver le sandbox audio s’ils utilisent des configurations de logiciels de sécurité qui interfèrent avec le bac à sable.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AudioSandboxEnabled
  - Nom de la stratégie de groupe: Autoriser l’exécution du bac à sable audio
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AudioSandboxEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AudioSandboxEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AutoImportAtFirstRun
  #### Importer automatiquement les données et les paramètres d’un autre navigateur lors de la première exécution
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Si vous activez cette stratégie, tous les types de données et paramètres pris en charge par le navigateur spécifié seront importés automatiquement et silencieusement lors de la première exécution. Lors de la première exécution, la section d'importation sera également ignorée.

  Les données du navigateur Microsoft Edge Legacy seront toujours migrées silencieusement lors de la première exécution, quelle que soit la valeur de cette stratégie.

  Si cette politique est définie sur « FromDefaultBrowser », les types de données correspondant au navigateur par défaut sur le périphérique géré seront importés.

  Si le navigateur spécifié comme valeur de cette stratégie n'est pas présent sur l'appareil géré, Microsoft Edgeignore simplement l'importation sans notification à l'utilisateur.

  Si vous définissez cette stratégie sur « DisabledAutoImport », la section d'importation de la première expérience est entièrement ignorée et Microsoft Edge n'importe pas automatiquement les données et les paramètres du navigateur.

  Si cette stratégie est définie sur la valeur « FromInternetExplorer », les types de données suivants seront importés à partir d'Internet Explorer :
 1. Favoris ou signets
 2. Mots de passe enregistrés
  3. Moteurs de recherche
   4. Historique de navigation
  5. Page d'accueil

  Si cette stratégie est définie sur la valeur « FromGoogleChrome », les types de données suivants seront importés de Google Chrome :
1. Favoris
 2. Mots de passe enregistrés
  3. Adresses et autres
  4. Informations sur les paiements
 5. Historique de navigation
  6. Paramètres
 7. Onglets épinglés et ouverts
 8. Extensions
 9. Cookies

Remarque : Pour plus de détails sur ce qui est importé de Google Chrome, veuillez consulter le site [https://go.microsoft.com/fwlink/?linkid=2120835](https://go.microsoft.com/fwlink/?linkid=2120835).

 Si cette politique est définie sur la valeur « FromSafari », les données de l'utilisateur ne sont plus importées dans Microsoft Edge. Cela est dû à la façon dont le Full Disk Access fonctionne sur Mac.
 Sur MacOS Mojave et supérieur, il n'est plus possible d'avoir une importation automatisée et sans surveillance des données de Safari dans Microsoft Edge.

  À partir de la version 83 de Microsoft Edge, si cette stratégie est définie sur la valeur « FromMozillaFirefox », les types de données suivants seront importés de Mozilla Firefox :
 1. Favoris ou signets
  2. Mots de passe enregistrés
  3. Adresses et autres
  4. Historique de navigation

  Si vous souhaitez empêcher l'importation de certains types de données sur les périphériques gérés, vous pouvez utiliser cette politique avec d'autres politiques telles que [ImportAutofillFormData](#importautofillformdata), [ImportBrowserSettings](#importbrowsersettings), [ImportFavorites](#importfavorites), etc.

Mappage des options de stratégie :

* FromDefaultBrowser (0) = Importe automatiquement tous les types de données et les paramètres pris en charge à partir du navigateur par défaut

* FromInternetExplorer (1) = Importe automatiquement tous les types de données et les paramètres pris en charge à partir d’Internet Explorer

* FromGoogleChrome (2) = Importe automatiquement tous les types de données et les paramètres pris en charge à partir de Google Chrome

* FromSafari (3) = Importe automatiquement tous les types de données et les paramètres pris en charge à partir de Safari

* DisabledAutoImport (4) = Désactive l’importation automatique et la section d’importation de l’expérience de première exécution est ignorée

* FromMozillaFirefox (5) = Importe automatiquement tous les types de données et les paramètres pris en charge à partir de Mozilla Firefox

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AutoImportAtFirstRun
  - Nom de la stratégie de groupe: Importer automatiquement les données et les paramètres d’un autre navigateur lors de la première exécution
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AutoImportAtFirstRun
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AutoImportAtFirstRun
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AutoLaunchProtocolsFromOrigins
  #### Définir une liste de protocoles qui peuvent lancer une application externe à partir d’origines, sans inviter l’utilisateur
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 85 ou version ultérieure

  #### Description
  Permet de définir une liste de protocoles et, pour chaque protocole, une liste associée de modèles d’origine autorisée. Cette liste peut lancer une application externe sans inviter l’utilisateur. Le séparateur de fin ne doit pas être inclus lorsque vous répertoriez le protocole. Par exemple, indiquez « Skype » au lieu de « Skype : » ou « skype:// ».

Si vous configurez cette stratégie, un protocole n’est autorisé à lancer une application externe qu’à l’invite de stratégie si :

- le protocole est répertorié

- l’origine du site qui tente de lancer le protocole correspond à l’un des modèles d’origine dans la liste allowed_origins de ce protocole.

Si l’une ou l’autre condition est fausse, l’invite de lancement du protocole externe ne sera pas omise par la stratégie.

Si vous ne configurez pas cette stratégie, vous ne pouvez pas lancer de protocoles sans invite. Les utilisateurs peuvent désactiver les invites sur une base par protocole ou par site, sauf si la stratégie [ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox) est désactivée. Cette stratégie n’a aucun impact sur les exemptions d’invite par protocole ou par site définis par les utilisateurs.

Les modèles de correspondance d’origine utilisent un format similaire à celui de la stratégie de [URLBlocklist](#urlblocklist), documentée sur https://go.microsoft.com/fwlink/ ?linkid=2095322.

Toutefois, les modèles de correspondance d’origine pour cette stratégie ne peuvent pas contenir d’éléments « /path » ou « @query ». Tout modèle contenant un élément "/path" ou "@query" sera ignoré.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Dictionnaire

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AutoLaunchProtocolsFromOrigins
  - Nom de la stratégie de groupe: Définir une liste de protocoles qui peuvent lancer une application externe à partir d’origines, sans inviter l’utilisateur
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AutoLaunchProtocolsFromOrigins
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
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


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AutoLaunchProtocolsFromOrigins
  - Exemple de valeur :
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
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AutoOpenAllowedForURLs
  #### URL où les types de fichiers AutoOpenFileTypes peuvent s’appliquer
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 85 ou version ultérieure

  #### Description
  Liste d’URL auxquelles [AutoOpenFileTypes](#autoopenfiletypes) s’applique. Cette stratégie n’a aucun impact sur les valeurs ouvertes automatiquement définies par les utilisateurs via l’étagère de téléchargement... > Entrée de menu « Toujours ouvrir les fichiers de ce type ».

Si vous définissez des URL dans cette stratégie, les fichiers s’ouvrent automatiquement uniquement par stratégie quand l’URL fait partie de ce groupe et le type de fichier est répertorié dans [AutoOpenFileTypes](#autoopenfiletypes). Si l’une ou l’autre condition est fausse, le téléchargement ne s’ouvre pas automatiquement par stratégie.

Si vous ne définissez cette stratégie, tous les téléchargements où se trouve le type de fichier dans [AutoOpenFileTypes](#autoopenfiletypes) s’ouvrent automatiquement.

       Un modèle d’URL doit être mis en forme conformément à [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AutoOpenAllowedForURLs
  - Nom de la stratégie de groupe: URL où les types de fichiers AutoOpenFileTypes peuvent s’appliquer
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\1 = "example.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\5 = ".exact.hostname.com"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AutoOpenAllowedForURLs
  - Exemple de valeur :
``` xml
<array>
  <string>example.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AutoOpenFileTypes
  #### Liste des types de fichiers qui doivent être automatiquement ouverts lors du téléchargement
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 85 ou version ultérieure

  #### Description
  Cette stratégie définit la liste des types de fichiers qui doivent être automatiquement ouverts lors du téléchargement. Remarque : le séparateur principal ne doit pas être inclus lorsque vous répertoriez le type de fichier. par conséquent, il vous suffit de répertorier « txt » au lieu de « .txt ».

Par défaut, ces types de fichiers sont automatiquement ouverts sur toutes les URL. Vous pouvez utiliser la stratégie [AutoOpenAllowedForURLs](#autoopenallowedforurls) pour restreindre les URL pour lesquelles ces types de fichiers seront ouverts automatiquement.

Les fichiers dont le type doit être ouvert automatiquement restent soumis aux vérifications Microsoft Defender SmartScreen activées et ne s’ouvrent pas si ces vérifications ne donnent pas satisfaction.

Les types de fichiers qu’un utilisateur a déjà spécifiés pour qu’ils s’ouvrent automatiquement continuera à le faire lors du téléchargement. L’utilisateur pourra toujours spécifier d’autres types de fichiers à ouvrir automatiquement.

Si vous ne configurez pas cette stratégie, seuls les types de fichiers qu’un utilisateur a déjà spécifié pour être automatiquement ouverts le sont lors du téléchargement.

Pour que cette stratégie soit appliquée sur les appareils Windows, celui-ci doit être joint à un domaine de Microsoft Active Directory, ou être une instance de Windows 10 professionnel ou entreprise inscrite pour la gestion des appareils.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AutoOpenFileTypes
  - Nom de la stratégie de groupe: Liste des types de fichiers qui doivent être automatiquement ouverts lors du téléchargement
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\1 = "exe"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\2 = "txt"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AutoOpenFileTypes
  - Exemple de valeur :
``` xml
<array>
  <string>exe</string>
  <string>txt</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AutofillAddressEnabled
  #### Activer le remplissage auto pour les adresses
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Active la fonctionnalité Remplissage auto et permet aux utilisateurs de remplir automatiquement les informations d'adresse dans les formulaires web en utilisant les informations stockées précédemment.

	Si vous désactivez cette stratégie, la fonctionnalité Remplissage auto ne suggère jamais ni ne renseigne les informations d’adresse, et n’enregistre pas les informations d’adresse supplémentaires que l’utilisateur peut envoyer lors de la navigation sur le web.

	Si vous activez cette stratégie ou ne la configurez pas, les utilisateurs contrôlent le Remplissage auto pour les adresses dans l’interface utilisateur.

	Notez que si vous désactivez cette stratégie, vous arrêtez également toutes les activités pour tous les formulaires web, à l’exception des formulaires de paiement et de mot de passe. Aucune entrée supplémentaire n’est enregistrée et Microsoft Edge ne suggère pas ou ne remplit pas automatiquement les entrées précédentes.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AutofillAddressEnabled
  - Nom de la stratégie de groupe: Activer le remplissage auto pour les adresses
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: AutofillAddressEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AutofillAddressEnabled
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AutofillCreditCardEnabled
  #### Activer le Remplissage auto pour les cartes de crédit
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Active la fonctionnalité Remplissage auto de Microsoft Edge et permet aux utilisateurs d'utiliser la saisie automatique pour les informations de carte de crédit dans les formulaires web en utilisant les informations stockées précédemment.

	Si vous désactivez cette stratégie, la fonctionnalité Remplissage auto ne suggère jamais ou ne remplit jamais les informations de carte de crédit, et n'enregistre pas les informations de carte de crédit supplémentaires que les utilisateurs peuvent envoyer lors de la navigation sur le web.

	Si vous activez cette stratégie ou ne la configurez pas, les utilisateurs contrôlent la fonctionnalité Remplissage auto pour les cartes de crédit.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AutofillCreditCardEnabled
  - Nom de la stratégie de groupe: Activer le Remplissage auto pour les cartes de crédit
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: AutofillCreditCardEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AutofillCreditCardEnabled
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### AutoplayAllowed
  #### Autoriser la lecture automatique de média pour les sites web
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 78 ou version ultérieure

  #### Description
  Cette stratégie définit la stratégie de lecture automatique de médias pour les sites web.

Le paramètre par défaut, « Non configuré », respecte les paramètres actuels de lecture automatique de médias et permet aux utilisateurs de configurer leurs paramètres de lecture automatique.

Le paramètre « Activé » définit la lecture automatique de médias sur « Autoriser ». Tous les sites web sont autorisés à lire les médias par lecture automatique. Les utilisateurs ne peuvent pas remplacer cette stratégie

.      Le paramètre « Désactivé » définit la lecture automatique de médias sur « Bloquer ». Aucun site web n’est autorisé à procéder à la lecture automatique des médias. Les utilisateurs ne peuvent pas remplacer cette stratégie.

Un onglet doit être fermé et rouvert pour que cette stratégie prenne effet.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: AutoplayAllowed
  - Nom de la stratégie de groupe: Autoriser la lecture automatique de média pour les sites web
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: AutoplayAllowed
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: AutoplayAllowed
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### BackgroundModeEnabled
  #### Poursuivre l’exécution des applications en arrière-plan après la fermeture de Microsoft Edge
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 77 ou ultérieur

  #### Description
  Permet aux processus de Microsoft Edge de démarrer lors de la connexion du système d’exploitation et de continuer à s’exécuter après la fermeture de la dernière fenêtre du navigateur. Dans ce scénario, les applications en arrière-plan et la session de navigation actuelle restent actives, y compris les cookies de la session. Un processus ouvert en arrière-plan affiche une icône dans la barre d’état système et peut toujours être fermé à partir de cet emplacement.

	Si vous activez cette stratégie, le mode arrière-plan est activé.

	Si vous désactivez cette stratégie, le mode arrière-plan est désactivé.

	Si vous ne configurez pas cette stratégie, le mode arrière-plan est désactivé et l’utilisateur peut configurer son comportement dans edge://settings/system.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: BackgroundModeEnabled
  - Nom de la stratégie de groupe: Poursuivre l’exécution des applications en arrière-plan après la fermeture de Microsoft Edge
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: BackgroundModeEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### BackgroundTemplateListUpdatesEnabled
  #### Active les mises à jour en arrière-plan de la liste des modèles disponibles pour les collections et d’autres fonctionnalités utilisées par des modèles
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 79 ou version ultérieure

  #### Description
  Vous permet d’activer ou de désactiver les mises à jour en arrière-plan pour la liste des modèles disponibles pour les collections et d’autres fonctionnalités qui utilisent des modèles. Les modèles permettent d'extraire des métadonnées enrichies d’une page web lorsque la page est enregistrée dans une collection.

Si vous activez ce paramètre ou si le paramètre n’est pas configuré, la liste des modèles disponibles est téléchargée en arrière-plan à partir d’un service Microsoft toutes les 24 heures.

Si vous désactivez ce paramètre, la liste des modèles disponibles est téléchargée à la demande. Ce type de téléchargement peut entraîner de légères altérations des performances pour les collections et d’autres fonctionnalités.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: BackgroundTemplateListUpdatesEnabled
  - Nom de la stratégie de groupe: Active les mises à jour en arrière-plan de la liste des modèles disponibles pour les collections et d’autres fonctionnalités utilisées par des modèles
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: BackgroundTemplateListUpdatesEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: BackgroundTemplateListUpdatesEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### BingAdsSuppression
  #### Bloquer toutes les publicités dans les résultats de recherche Bing
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 83 ou version ultérieure

  #### Description
  Autorise une expérience de recherche sans publicités sur Bing.com

        Si vous activez cette stratégie, un utilisateur peut effectuer une recherche sur bing.com et bénéficier d’une expérience de recherche sans publicités. En même temps, le paramètre SafeSearch est défini sur « Strict » et ne peut pas être modifié par l’utilisateur.

       Si vous ne configurez pas cette stratégie, l’expérience par défaut affiche les publicités dans les résultats de la recherche sur bing.com. Par défaut, SafeSearch est défini sur « Modéré » et peut être modifié par l’utilisateur.

       Cette stratégie est disponible uniquement pour les SKU K-12 qui sont identifiées comme clients EDU par Microsoft.

       Veuillez consulter https://go.microsoft.com/fwlink/ ?linkid=2119711 pour en savoir plus sur cette stratégie ou si les scénarios suivants vous concernent :

* Vous avez un client EDU, mais la stratégie ne fonctionne pas.

       * Votre adresse IP a été mise en liste verte pour obtenir une expérience de recherche sans publicités.

*        Vous avez expérimenté une expérience de recherche sans publicités sur Microsoft Edge hérité et souhaitez effectuer une mise à niveau vers la nouvelle version de Microsoft Edge.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: BingAdsSuppression
  - Nom de la stratégie de groupe: Bloquer toutes les publicités dans les résultats de recherche Bing
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: BingAdsSuppression
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: BingAdsSuppression
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### BlockThirdPartyCookies
  #### Bloquer les cookies tiers
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Empêcher les éléments de page web qui ne proviennent pas du domaine qui se trouve dans la barre d’adresses de définir des cookies.

Si vous activez cette stratégie, les éléments de page web qui ne proviennent pas du domaine qui se trouve dans la barre d’adresses ne peuvent pas définir de cookies

Si vous désactivez cette stratégie, les éléments de page web provenant de domaines autres que ceux figurant dans la barre d’adresses peuvent définir des cookies.

Si vous ne configurez pas cette stratégie, des cookies tiers sont activés, mais les utilisateurs peuvent modifier ce paramètre.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: BlockThirdPartyCookies
  - Nom de la stratégie de groupe: Bloquer les cookies tiers
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: BlockThirdPartyCookies
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: BlockThirdPartyCookies
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### BrowserAddProfileEnabled
  #### Activer la création de profil à partir du menu déroulant Identité ou de la page Paramètres
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Autorise les utilisateurs de créer des profils à l’aide de l’option **Ajouter un profil**.
Si vous activez cette stratégie ou ne la configurez pas, Microsoft Edge autorise les utilisateurs à utiliser **Ajouter un profil** dans le menu déroulant Identité ou sur la page Paramètres pour créer des profils.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas ajouter de profils à partir du menu déroulant Identité ou de la page Paramètres.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: BrowserAddProfileEnabled
  - Nom de la stratégie de groupe: Activer la création de profil à partir du menu déroulant Identité ou de la page Paramètres
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: BrowserAddProfileEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: BrowserAddProfileEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### BrowserGuestModeEnabled
  #### Activer le mode invité
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Activez l’option autorisant l’utilisation de profils Invité dans Microsoft Edge. Dans un profil Invité, le navigateur n’importe pas les données de navigation à partir des profils existants et supprime les données de navigation lorsque tous les profils Invité sont fermés.

Si vous activez cette stratégie ou ne la configurez pas, Microsoft Edge permet aux utilisateurs de parcourir les profils Invité.

Si vous désactivez cette stratégie, Microsoft Edge n’autorise pas les utilisateurs à parcourir les profils Invité.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: BrowserGuestModeEnabled
  - Nom de la stratégie de groupe: Activer le mode invité
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: BrowserGuestModeEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: BrowserGuestModeEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### BrowserNetworkTimeQueriesEnabled
  #### Autoriser les requêtes auprès d'un service de temps réseau de navigateur
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Empêche Microsoft Edge de parfois envoyer des requêtes à un service de temps réseau du navigateur pour récupérer un horodatage précis.

	Si vous désactivez cette stratégie, Microsoft Edge arrête d’envoyer des requêtes à un service de temps réseau du navigateur.

	Si vous activez cette stratégie ou si vous ne la configurez pas, Microsoft Edge envoie parfois des requêtes à un service de temps réseau du navigateur.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: BrowserNetworkTimeQueriesEnabled
  - Nom de la stratégie de groupe: Autoriser les requêtes auprès d'un service de temps réseau de navigateur
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: BrowserNetworkTimeQueriesEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: BrowserNetworkTimeQueriesEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### BrowserSignin
  #### Paramètres de connexion du navigateur
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifiez si un utilisateur peut se connecter à Microsoft Edge avec son compte et utiliser les services liés au compte, tels que la synchronisation et l'authentification unique. Pour contrôler la disponibilité de la synchronisation, utilisez plutôt la stratégie [SyncDisabled](#syncdisabled).

Si vous définissez cette stratégie sur « Disable », vérifiez que vous désactivez également la stratégie[NonRemovableProfileEnabled](#nonremovableprofileenabled), car [NonRemovableProfileEnabled](#nonremovableprofileenabled) désactive la création d'un profil de navigateur automatiquement connecté. Si les deux stratégies sont définies, Microsoft Edge utilise la stratégie « Désactiver la connexion au navigateur » et se comporte comme si [NonRemovableProfileEnabled](#nonremovableprofileenabled) était désactivé.

Si vous définissez cette stratégie sur « Enable », les utilisateurs peuvent se connecter au navigateur. La connexion au navigateur ne signifie pas que la synchronisation est activée par défaut ; l’utilisateur doit accepter séparément l'utilisation de cette fonctionnalité.

Si vous définissez cette stratégie sur « Force » (2), les utilisateurs doivent se connecter à un profil pour utiliser le navigateur. Par défaut, cela permet à l'utilisateur de choisir s'il veut synchroniser avec son compte, sauf si la synchronisation est désactivée par l’administrateur de domaine ou avec la stratégie [SyncDisabled](#syncdisabled). La valeur par défaut de la stratégie [BrowserGuestModeEnabled](#browserguestmodeenabled) est définie sur false.

Si vous ne configurez pas cette stratégie, les utilisateurs peuvent décider s’ils souhaitent activer l’option de connexion au navigateur et l’utiliser au mieux.

Mappage des options de stratégie :

* Disable (0) = Désactiver la connexion au navigateur

* Enable (1) = Activer la connexion dans l’Explorateur

* Force (2) = Forcer les utilisateurs à se connecter pour utiliser le navigateur

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: BrowserSignin
  - Nom de la stratégie de groupe: Paramètres de connexion du navigateur
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: BrowserSignin
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: BrowserSignin
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### BuiltInDnsClientEnabled
  #### Utiliser le client DNS intégré
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Contrôle si le client DNS intégré doit être utilisé.

Cela n’affecte pas les serveurs DNS utilisés ; uniquement la pile logicielle permettant de communiquer avec eux. Par exemple, si le système d’exploitation est configuré de manière à utiliser un serveur DNS d’entreprise, ce même serveur est utilisé par le client DNS intégré. Il est toutefois possible que le client DNS intégré adresse les serveurs de différentes manières en utilisant des protocoles plus modernes liés à DNS, tels que DNS-over-TLS.

Si vous activez cette stratégie, le client DNS intégré est utilisé, s’il est disponible.

Si vous désactivez cette stratégie, le client n’est jamais utilisé.

Si vous ne configurez pas cette stratégie, le client DNS intégré est activé par défaut sur MacOS et les utilisateurs peuvent choisir d’utiliser le client DNS intégré en modifiant edge://flags ou en spécifiant un indicateur de ligne de commande.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: BuiltInDnsClientEnabled
  - Nom de la stratégie de groupe: Utiliser le client DNS intégré
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: BuiltInDnsClientEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: BuiltInDnsClientEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### BuiltinCertificateVerifierEnabled
  #### Détermine si le vérificateur de certificat intégré est utilisé pour vérifier les certificats de serveur (déconseillé)
  >DÉCONSEILLÉ : cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge :
  - Sur macOS depuis 83 ou ultérieur

  #### Description
  Cette stratégie est déconseillée, car elle est conçue comme un mécanisme à court terme destiné à offrir aux entreprises davantage de temps pour mettre à jour leurs environnements incompatibles avec le vérificateur de certificats intégré et signaler les problèmes détectés.

Elle ne fonctionnera plus dans Microsoft Edge version 87 lorsque l’arrêt de la prise en charge du vérificateur de certificat hérité sur Mac OS X est prévue.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  

  #### Paramètres et informations Mac
  - Nom de la clé de préférence: BuiltinCertificateVerifierEnabled
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### CertificateTransparencyEnforcementDisabledForCas
  #### Désactiver l'application transparence de certificat pour la liste des hachages subjectPublicKeyInfo
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Désactive l’application des exigences de transparence du certificat pour obtenir la liste des hachages subjectPublicKeyInfo.

Cette stratégie vous permet de désactiver les exigences de divulgation de transparence de certificat pour les chaînes de certificat qui contiennent des certificats avec l’un des hachages subjectPublicKeyInfo spécifiés. Ceci autorise les certificats qui ne seraient pas approuvés dans le cas contraire, car ils n'ont pas été divulgués publiquement correctement, à continuer à être utilisés pour les hôtes Entreprise.

Pour désactiver l'application de la transparence du certificat lorsque cette stratégie est définie, l'un des ensembles de conditions suivants doit être rempli :
1. Le hachage est celui de subjectPublicKeyInfo du certificat serveur.
2. Le hachage est celui d’un subjectPublicKeyInfo qui s’affiche dans un certificat d’autorité de certification dans la chaîne de certificats, que le certificat d’autorité de certification est limité via l’extension nameConstraints X.509v3, au moins un nameConstraints est présent dans le permittedSubtrees et le directoryName contient un attribut organizationName.
3. Le hachage est celui d’un subjectPublicKeyInfo qui s’affiche dans un certificat d’autorité de certification dans la chaîne de certificats, que le certificat d’autorité de certification a au moins un attribut organizationName dans le sujet du certificat et le certificat du serveur contient le même nombre d'attributs organizationName, dans le même ordre et avec les valeurs identiques (octet pour octet).

Un hachage subjectPublicKeyInfo est spécifié par la concaténation du nom d’algorithme de hachage, le caractère « / » et l’encodage Base64 de cet algorithme de hachage appliqué à la subjectPublicKeyInfo codée DER du certificat spécifié. Cet encodage Base64 est le même format qu’une empreinte digitale SPKI, telle que définie dans la RFC 7469, section 2.4. Les algorithmes de hachage non reconnus sont ignorés. Le seul algorithme de hachage pris en charge pour l’instant est « sha256 ».

Si vous désactivez ou ne configurez pas cette stratégie, tous les certificats obligatoires pour être divulgués via la transparence des certificats sont considérés comme non approuvés s'ils ne sont pas transmis conformément à la stratégie de transparence du certificat.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: CertificateTransparencyEnforcementDisabledForCas
  - Nom de la stratégie de groupe: Désactiver l'application transparence de certificat pour la liste des hachages subjectPublicKeyInfo
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\2 = "sha256//////////////////////w=="

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: CertificateTransparencyEnforcementDisabledForCas
  - Exemple de valeur :
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### CertificateTransparencyEnforcementDisabledForLegacyCas
  #### Désactivez l’application de transparence de certificat pour obtenir la liste des autorités de certification héritées
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Désactive l’application des exigences de transparence de certificat pour une liste d’autorités de certification (AC) héritées.

	Cette stratégie vous permet de désactiver les exigences de divulgation de transparence de certificat pour les chaînes de certificat qui contiennent des certificats avec l’un des hachages subjectPublicKeyInfo spécifiés. Ainsi, les certificats qui ne seraient pas approuvés en temps normal, car ils n’ont pas été correctement divulgués publiquement, continuent à être utilisés pour les hôtes de l’entreprise.

	Pour pouvoir désactiver l'application de la transparence de certificat, vous devez définir le hachage sur un subjectPublicKeyInfo apparaissant dans un certificat d’autorité de certification qui n’est reconnu comme une autorité de certification (AC) héritée. Une autorité de certification héritée est une autorité de certification qui a été approuvée publiquement par défaut par un ou plusieurs systèmes d’exploitation pris en charge par Microsoft Edge.

	Pour spécifier un hachage subjectPublicKeyInfo, concaténez le nom de l’algorithme de hachage, le caractère « / » et l’encodage Base64 de cet algorithme de hachage appliqué à la subjectPublicKeyInfo codée DER du certificat spécifié. Cet encodage Base64 est le même format qu’une empreinte digitale SPKI, tel que défini dans RFC 7469, Section 2.4. Les algorithmes de hachage non reconnus sont ignorés. Le seul algorithme de hachage pris en charge pour l’instant est « sha256 ».

	Si vous ne configurez pas cette stratégie, tous les certificats qui doivent être divulgués via la transparence des certificats sont considérés comme non approuvés s'ils ne sont pas divulgués conformément à la stratégie de transparence de certificat.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Nom de la stratégie de groupe: Désactivez l’application de transparence de certificat pour obtenir la liste des autorités de certification héritées
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\2 = "sha256//////////////////////w=="

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Exemple de valeur :
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### CertificateTransparencyEnforcementDisabledForUrls
  #### Désactiver l'application de transparence de certificat pour des URL spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Désactive l’application des exigences de transparence de certificat pour les URL répertoriées.

	Cette stratégie vous permet de ne pas divulguer les certificats pour les noms d’hôte dans les URL spécifiées via la transparence du certificat. Cela vous permet d’utiliser les certificats qui ne seraient pas approuvés, car ils n’ont pas été correctement publiés, mais elle complique la détection des certificats mal utilisés pour ces hôtes.

	Formez le modèle d’URL de la façon suivante : [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Étant donné que les certificats sont valides pour un nom d’hôte donné, indépendamment du schéma, port ou chemin d’accès, seule une partie du nom d’hôte de l’URL est prise en compte. Les hôtes de caractères génériques ne sont pas pris en charge.

	Si vous ne configurez pas cette stratégie, tous les certificats qui doivent être transmis via la transparence du certificat sont considérés comme non approuvés s’ils ne sont pas divulgués.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: CertificateTransparencyEnforcementDisabledForUrls
  - Nom de la stratégie de groupe: Désactiver l'application de transparence de certificat pour des URL spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\2 = ".contoso.com"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: CertificateTransparencyEnforcementDisabledForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>contoso.com</string>
  <string>.contoso.com</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ClearBrowsingDataOnExit
  #### Effacer les données de navigation à la fermeture de Microsoft Edge
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 78 ou version ultérieure

  #### Description
  Microsoft Edge n’efface pas les données de navigation par défaut à sa fermeture. Les données de navigation incluent les informations entrées dans les formulaires, les mots de passe et même les sites web visités.

Si vous activez cette stratégie, toutes les données de navigation sont supprimées à chaque fermeture de Microsoft Edge. Notez que si vous activez cette stratégie, elle a la priorité sur la configuration de [DefaultCookiesSetting](#defaultcookiessetting)

Si vous désactivez ou omettez de configurer cette stratégie, les utilisateurs peuvent configurer l’option Effacer les données de navigation dans les Paramètres.

Si vous activez cette stratégie, n’activez pas la stratégie [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) ou [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit), car toutes deux concernent la suppression des données de navigation. Si vous configurez les stratégies précédentes et cette stratégie, toutes les données de navigation sont supprimées à la fermeture de Microsoft Edge, quelle que soit la configuration de l’option [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) ou [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

Pour empêcher la suppression des cookies à la fermeture, configurez la stratégie [SaveCookiesOnExit](#savecookiesonexit).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ClearBrowsingDataOnExit
  - Nom de la stratégie de groupe: Effacer les données de navigation à la fermeture de Microsoft Edge
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: ClearBrowsingDataOnExit
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ClearBrowsingDataOnExit
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ClearCachedImagesAndFilesOnExit
  #### Effacer les images et les fichiers mis en cache lorsque Microsoft Edge se ferme
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 83 ou version ultérieure

  #### Description
  Microsoft Edge n’efface pas les images et les fichiers mis en cache par défaut lorsqu’il se ferme.

Si vous activez cette stratégie, les images et les fichiers mis en cache sont supprimés à chaque fermeture de Microsoft Edge.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas configurer l’option des images et fichiers mis en cache dans edge://settings/clearBrowsingDataOnClose.

Si vous ne configurez pas cette stratégie, les utilisateurs peuvent choisir si les images et les fichiers mis en cache sont effacés à la fermeture.

Si vous désactivez cette stratégie, n’activez pas la stratégie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit), car elles traitent toutes deux de la suppression de données. Si vous configurez les deux, la stratégie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) est prioritaire et supprime toutes les données à la fermeture de Microsoft Edge, quelle que soit la configuration de [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ClearCachedImagesAndFilesOnExit
  - Nom de la stratégie de groupe: Effacer les images et les fichiers mis en cache lorsque Microsoft Edge se ferme
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: ClearCachedImagesAndFilesOnExit
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ClearCachedImagesAndFilesOnExit
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ClickOnceEnabled
  #### Autoriser les utilisateurs à ouvrir des fichiers à l’aide du protocole ClickOnce
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 78 ou ultérieur

  #### Description
  Autoriser les utilisateurs à ouvrir des fichiers à l’aide du protocole ClickOnce. Le protocole ClickOnce permet aux sites web de demander que le navigateur ouvre les fichiers d’une URL spécifique à l’aide du gestionnaire de fichiers ClickOnce sur l’ordinateur ou l’appareil de l’utilisateur.

Si vous activez cette stratégie, les utilisateurs peuvent ouvrir des fichiers à l’aide du protocole ClickOnce. Cette stratégie remplace le paramètre ClickOnce de l’utilisateur sur la page edge://flags/.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas ouvrir de fichiers à l’aide du protocole ClickOnce. Au lieu de cela, le fichier est enregistré dans le système de fichiers utilisant le navigateur. Cette stratégie remplace le paramètre ClickOnce de l’utilisateur sur la page edge://flags/.

Si vous ne configurez pas cette stratégie, les utilisateurs disposant de versions Microsoft Edge antérieures à Microsoft Edge 87 ne peuvent pas ouvrir de fichiers à l’aide du protocole ClickOnce par défaut. Les utilisateurs ont toutefois la possibilité d’activer l’utilisation du protocole ClickOnce avec la page edge://flags/. Les utilisateurs disposant des versions Microsoft Edge 87 et ultérieures peuvent ouvrir des fichiers à l’aide du protocole ClickOnce par défaut et ont la possibilité de désactiver le protocole ClickOnce avec la page edge://flags/.

 La désactivation de ClickOnce peut empêcher le lancement correct d’applications ClickOnce (fichiers .application).

Si vous souhaitez obtenir plus d’informations sur ClickOnce, voir [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) and [https://go.microsoft.com/fwlink/?linkid=2099880](https://go.microsoft.com/fwlink/?linkid=2099880).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ClickOnceEnabled
  - Nom de la stratégie de groupe: Autoriser les utilisateurs à ouvrir des fichiers à l’aide du protocole ClickOnce
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ClickOnceEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### CollectionsServicesAndExportsBlockList
  #### Bloquer l’accès à une liste spécifiée de services et de cibles d’exportation dans Collections
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Répertoriez les services spécifiques et les cibles d’exportation auxquelles les utilisateurs ne peuvent pas accéder dans la fonctionnalité Collections dans Microsoft Edge. Ceci inclut l’affichage de données supplémentaires à partir de Bing et l’exportation de collections vers des produits Microsoft ou des partenaires externes.

Si vous activez cette stratégie, les services et les cibles d’exportation qui correspondent à la liste spécifiée sont bloqués.

Si vous ne configurez pas cette stratégie, aucune restriction sur les services et les cibles d’exportation acceptables n’est appliquée.

Mappage des options de stratégie :

* pinterest_suggestions (pinterest_suggestions) = Suggestions de Pinterest

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: CollectionsServicesAndExportsBlockList
  - Nom de la stratégie de groupe: Bloquer l’accès à une liste spécifiée de services et de cibles d’exportation dans Collections
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\1 = "pinterest_suggestions"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: CollectionsServicesAndExportsBlockList
  - Exemple de valeur :
``` xml
<array>
  <string>pinterest_suggestions</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### CommandLineFlagSecurityWarningsEnabled
  #### Activer les avertissements de sécurité pour les indicateurs de ligne de commande
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 78 ou version ultérieure

  #### Description
  Si cette stratégie est désactivée, elle empêche l'apparition des avertissements de sécurité lorsque Microsoft Edge est lancé avec des indicateurs de ligne de commande potentiellement dangereux.

Si elle est activée ou non configurée, les avertissements de sécurité s'affichent lorsque ces indicateurs de ligne de commande sont utilisés pour lancer Microsoft Edge.

Par exemple, l'indicateur « --disable-gpu-sandbox » génère l'avertissement suivant :  Vous utilisez un indicateur de ligne de commande non pris en charge : « --disable-gpu-sandbox ». Cela implique des risques de sécurité et de stabilité.

Sur Windows, cette stratégie est uniquement disponible sur les instances jointes au domaine Microsoft Active Directory, ou sur Windows 10 Professionnel ou Enterprise sur les instances engagées dans la gestion d'un appareil, ou les instances macOS qui sont gérées via la gestion des périphériques mobiles ou qui sont jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: CommandLineFlagSecurityWarningsEnabled
  - Nom de la stratégie de groupe: Activer les avertissements de sécurité pour les indicateurs de ligne de commande
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: CommandLineFlagSecurityWarningsEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: CommandLineFlagSecurityWarningsEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ComponentUpdatesEnabled
  #### Activer les mises à jour de composant dans Microsoft Edge
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Si vous activez ou ne configurez pas cette stratégie, les mises à jour de composant sont activées dans Microsoft Edge.

	Si vous désactivez cette stratégie ou la définissez sur « false », les mises à jour de composant sont désactivées pour tous les composants dans Microsoft Edge.

	Toutefois, certains composants ne sont pas concernés par cette stratégie, notamment les composants ne contenant pas de code exécutable, ceux qui n'affectent pas de manière importante le comportement du navigateur ou encore ceux qui sont importants pour la sécurité. En d'autres termes, les mises à jour considérées comme « importante pour la sécurité » sont toujours appliquées même si vous désactivez la stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ComponentUpdatesEnabled
  - Nom de la stratégie de groupe: Activer les mises à jour de composant dans Microsoft Edge
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ComponentUpdatesEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ComponentUpdatesEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ConfigureDoNotTrack
  #### Configurer Ne pas me suivre
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifiez s’il faut envoyer des requêtes Ne pas me suivre aux sites web qui demandent des infos de suivi. Les requêtes Ne pas me suivre autorisent les sites web que vous visitez à savoir que vous ne souhaitez pas que votre activité de navigation soit suivie. Par défaut, Microsoft Edge n’envoie pas de requête Ne pas me suivre, mais les utilisateurs peuvent activer cette fonctionnalité pour les envoyer.

	Si vous activez cette stratégie, les requêtes Ne pas me suivre sont toujours envoyées aux sites web qui demandent des infos de suivi.

	Si vous désactivez cette stratégie, les requêtes ne sont jamais envoyées.

	Si vous ne configurez pas cette stratégie, les utilisateurs peuvent décider d’envoyer ces requêtes.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ConfigureDoNotTrack
  - Nom de la stratégie de groupe: Configurer Ne pas me suivre
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ConfigureDoNotTrack
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ConfigureDoNotTrack
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ConfigureOnPremisesAccountAutoSignIn
  #### Configurer la connexion automatique avec un compte de domaine Active Directory en l'absence de compte de domaine Azure AD
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 81 ou ultérieur

  #### Description
  Activez l’utilisation des comptes Active Directory pour la connexion automatique si les ordinateurs de vos utilisateurs sont joints au domaine et si votre environnement n’est pas joint de façon hybride. Si vous voulez que les utilisateurs soient connectés automatiquement avec leur compte Azure Active Directory, créez une jonction Azure AD (voir [https://go.microsoft.com/fwlink/?linkid=2118197](https://go.microsoft.com/fwlink/?linkid=2118197) pour plus d’informations) ou une jonction hybride (voir [https://go.microsoft.com/fwlink/?linkid=2118365](https://go.microsoft.com/fwlink/?linkid=2118365) pour plus d’informations) pour votre environnement.

Si vous avez configuré la stratégie [BrowserSignin](#browsersignin) sur désactivé, cette stratégie n’a aucun effet.

Si vous activez cette stratégie et la définissez sur « Se connecter et empêcher de supprimer le compte du domaine », Microsoft Edge connecte automatiquement les utilisateurs qui se trouvent sur des ordinateurs joints au domaine à l’aide de leur compte Active Directory.

Si vous définissez cette stratégie sur « Disabled » ou si vous ne la définissez pas, Microsoft Edge ne connecte pas automatiquement les utilisateurs qui se trouvent sur des ordinateurs joints au domaine joint avec un compte Active Directory.

Mappage des options de stratégie :

* Disabled (0) = Désactivé

* SignInAndMakeDomainAccountNonRemovable (1) = Se connecter et empêcher de supprimer le compte de domaine

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ConfigureOnPremisesAccountAutoSignIn
  - Nom de la stratégie de groupe: Configurer la connexion automatique avec un compte de domaine Active Directory en l'absence de compte de domaine Azure AD
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ConfigureOnPremisesAccountAutoSignIn
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ConfigureOnlineTextToSpeech
  #### Configuration la conversion de texte par synthèse vocale en ligne
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez si le navigateur peut tirer profit des polices de la voix de la conversion de texte en ligne en voix dans le cadre d'Azure Cognitive Services. Ces polices de la voix sont d'une qualité supérieure à celle des polices de la voix système préinstallées.

Si vous activez ou ne configurez pas cette stratégie, les applications web qui utilisent l’API SpeechSynthesis peuvent utiliser les polices de la voix de la conversion de texte en ligne en voix.

Si vous désactivez cette stratégie, les polices de la voix ne sont pas disponibles.

Pour en savoir plus sur cette fonctionnalité :
API SpeechSynthesis : [https://go.microsoft.com/fwlink/?linkid=2110038](https://go.microsoft.com/fwlink/?linkid=2110038)
Cognitive Services : [https://go.microsoft.com/fwlink/?linkid=2110141](https://go.microsoft.com/fwlink/?linkid=2110141)

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ConfigureOnlineTextToSpeech
  - Nom de la stratégie de groupe: Configuration la conversion de texte par synthèse vocale en ligne
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ConfigureOnlineTextToSpeech
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ConfigureOnlineTextToSpeech
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ConfigureShare
  #### Configurer l’expérience de partage
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 83 ou ultérieur

  #### Description
  Si vous définissez cette stratégie sur « ShareAllowed » (valeur par défaut), les utilisateurs pourront accéder à l’expérience de partage de Windows 10 à partir du menu Paramètres et Plus dans Microsoft Edge à partager avec d’autres applications sur le système.

Si vous définissez cette stratégie sur « ShareDisallowed », les utilisateurs ne pourront pas accéder à l’expérience de partage Windows 10. Si le bouton partager se trouve dans la barre d’outils, il sera également masqué.

Mappage des options de stratégie :

* ShareAllowed (0) = Autoriser l’utilisation de l’expérience de partage

* ShareDisallowed (1) = Ne pas autoriser l’utilisation de l’expérience de partage

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ConfigureShare
  - Nom de la stratégie de groupe: Configurer l’expérience de partage
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ConfigureShare
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### CustomHelpLink
  #### Spécifier le lien d’aide personnalisé
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 79 ou version ultérieure

  #### Description
  Spécifiez un lien pour le menu Aide ou la touche F1.

Si vous activez cette stratégie, un administrateur peut spécifier un lien pour le menu Aide ou la touche F1.

Si vous désactivez ou ne configurez pas cette stratégie, le lien par défaut du menu Aide ou de la touche F1 est utilisé.

Cette stratégie est disponible uniquement sur les instances Windows qui sont jointes à un domaine de Microsoft Active Directory, Windows 10 professionnel ou les instances d’entreprise qui sont inscrites à la gestion des appareils, ou les instances macOS qui sont gérées via la gestion des périphériques mobiles ou qui sont jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: CustomHelpLink
  - Nom de la stratégie de groupe: Spécifier le lien d’aide personnalisé
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: CustomHelpLink
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"https://go.microsoft.com/fwlink/?linkid=2080734"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: CustomHelpLink
  - Exemple de valeur :
``` xml
<string>https://go.microsoft.com/fwlink/?linkid=2080734</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DNSInterceptionChecksEnabled
  #### Vérifications d’interception DNS activées
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 80 ou version ultérieure

  #### Description
  Cette stratégie configure un commutateur local qui peut permettre de désactiver les vérifications d’interception DNS. Ces vérifications essaient de déterminer si le navigateur se situe derrière un proxy qui redirige des noms d’hôtes inconnus.

Cette détection n’est peut-être pas nécessaire dans un environnement d’entreprise dans lequel la configuration réseau est connue. Elle peut être désactivée afin d’éviter tout trafic DNS et HTTP supplémentaire au démarrage et lors de chaque modification de la configuration DNS.

Si vous activez ou ne définissez pas cette stratégie, les vérifications d’interception DNS sont effectuées.

Si vous désactivez cette stratégie, les vérifications d’interception DNS ne sont pas effectuées.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DNSInterceptionChecksEnabled
  - Nom de la stratégie de groupe: Vérifications d’interception DNS activées
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DNSInterceptionChecksEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DNSInterceptionChecksEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultBrowserSettingEnabled
  #### Définir Microsoft Edge comme navigateur par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows 7 et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Si vous définissez cette stratégie sur True, Microsoft Edge vérifie toujours s’il s’agit du navigateur par défaut au démarrage et s’inscrit automatiquement, si possible.

Si vous définissez cette stratégie sur False, Microsoft Edge n’effectue pas de vérification s’il s’agit du navigateur par défaut et désactive les contrôles utilisateur pour définir cette option.

Si vous ne configurez pas cette stratégie, Microsoft Edge permet à l’utilisateur de contrôler s’il s'agit du navigateur par défaut et d’afficher les notifications utilisateur lorsque ce n'est pas le cas.

Remarque à l’attention des administrateurs Windows : cette stratégie ne fonctionne que pour les PC exécutant Windows 7. Pour les versions ultérieures de Windows, vous devez déployer un fichier « associations d’applications par défaut » qui fait de Microsoft Edge le gestionnaire pour les protocoles HTTPS et HTTP (et, éventuellement, le protocole FTP et les formats de fichier, tels que .html, .htm, .pdf, .svg, .webp). Voir [https://go.microsoft.com/fwlink/?linkid=2094932](https://go.microsoft.com/fwlink/?linkid=2094932) pour plus d’informations.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultBrowserSettingEnabled
  - Nom de la stratégie de groupe: Définir Microsoft Edge comme navigateur par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DefaultBrowserSettingEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultBrowserSettingEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultSearchProviderContextMenuAccessAllowed
  #### Autoriser l’accès de recherche au menu contextuel du fournisseur de recherche par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 85 ou version ultérieure

  #### Description
  Active l’utilisation d’un moteur de recherche par défaut dans le menu contextuel.

Si vous configurez cette stratégie sur désactivé, l’élément de menu contextuel de recherche qui s’appuie sur votre moteur de recherche par défaut et la recherche dans la barre latérale ne sera pas disponible.

Si cette stratégie est configurée sur activée ou non définie, l’élément de menu contextuel pour votre moteur de recherche par défaut et la recherche dans la barre latérale sont disponibles.

La valeur de la stratégie est appliquée uniquement lorsque la stratégie de [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) est activée et ne s’applique pas dans le cas contraire.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultSearchProviderContextMenuAccessAllowed
  - Nom de la stratégie de groupe: Autoriser l’accès de recherche au menu contextuel du fournisseur de recherche par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DefaultSearchProviderContextMenuAccessAllowed
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultSearchProviderContextMenuAccessAllowed
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultSensorsSetting
  #### Paramètre des capteurs par défaut
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Déterminez si les sites web peuvent accéder et utiliser des capteurs comme les capteurs de mouvement et de luminosité. Vous pouvez bloquer ou autoriser complètement l’accès aux capteurs pour les sites web.

Définir la stratégie sur 1 permet aux sites web d’accéder aux capteurs et de les utiliser. Définir la stratégie sur 2 refuse l’autorisation aux capteurs.

Vous pouvez remplacer cette stratégie pour des modèles d’URL spécifiques en utilisant les stratégies [SensorsAllowedForUrls](#sensorsallowedforurls) et [SensorsBlockedForUrls](#sensorsblockedforurls).

Si vous ne configurez pas cette stratégie, les sites web peuvent accéder aux capteurs et les utiliser, et les utilisateurs peuvent modifier ce paramètre. Il s’agit de la valeur par défaut globale pour [SensorsAllowedForUrls](#sensorsallowedforurls) et [SensorsBlockedForUrls](#sensorsblockedforurls).

Mappage des options de stratégie :

* AllowSensors (1) = Autoriser les sites à accéder aux capteurs

* BlockSensors (2) = Ne pas autoriser les sites à accéder aux capteurs

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultSensorsSetting
  - Nom de la stratégie de groupe: Paramètre des capteurs par défaut
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DefaultSensorsSetting
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultSensorsSetting
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DefaultSerialGuardSetting
  #### Contrôler l’utilisation de l’API série
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Définissez si les sites Web peuvent accéder aux ports série. Vous pouvez totalement bloquer l’accès ou demander à l’utilisateur chaque fois qu’un site Web souhaite accéder à un port série.

La définition de la stratégie sur 3 permet aux sites Web de demander l’accès aux ports série. La définition de la stratégie sur 2 refuse l’accès aux ports série.

Vous pouvez remplacer cette stratégie pour des modèles d’URL spécifiques à l’aide des stratégies [SerialAskForUrls](#serialaskforurls) et [SerialBlockedForUrls](#serialblockedforurls).

Si vous ne configurez pas cette stratégie, par défaut, les sites Web peuvent demander aux utilisateurs s’ils peuvent accéder à un port série, et les utilisateurs peuvent modifier ce paramètre.

Mappage des options de stratégie :

* BlockSerial (2) = N'autoriser aucun site à demander l’accès aux ports série via l’API série

* AskSerial (3) = Autoriser les sites à demander des autorisations d’accès utilisateur à un port série

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DefaultSerialGuardSetting
  - Nom de la stratégie de groupe: Contrôler l’utilisation de l’API série
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DefaultSerialGuardSetting
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DefaultSerialGuardSetting
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DelayNavigationsForInitialSiteListDownload
  #### Exiger que la Liste des sites en Mode entreprise soit disponible avant la navigation d’onglets
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 84 ou ultérieur

  #### Description
  Vous permet de spécifier si les onglets de Microsoft Edge sont en attente jusqu’à ce que le navigateur ait téléchargé la Liste des sites en Mode entreprise initiale. Ce paramètre est destiné au scénario dans lequel la page d’accueil du navigateur doit être chargée en mode Internet Explorer. Il est important que cette action s’effectue lors de la première exécution du navigateur lorsque le mode IE est activé. Si ce scénario est inexistant, nous vous recommandons de ne pas activer ce paramètre, car cela peut avoir une incidence négative sur les performances de chargement de la page d’accueil. Le paramètre s’applique uniquement lorsque Microsoft Edge ne dispose pas d’aucune Liste des sites en Mode entreprise mise en cache, par exemple, lors de la première exécution du navigateur lorsque le mode IE est activé.

Ce paramètre fonctionne en association avec :
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) est défini sur « Mode Internet Explorer »
et
la stratégie [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) dans laquelle la liste comporte au moins une entrée.

 Le comportement d’expiration de cette stratégie peut être configuré avec la stratégie [NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout).

 Si vous avez attribué la valeur « All » à cette stratégie, lorsque Microsoft Edge ne dispose pas de version mise en cache de la Liste des sites en Mode entreprise, les onglets retardent la navigation jusqu’à ce que le navigateur ait téléchargé la liste des sites. Les sites configurés pour s’ouvrir en mode Internet Explorer par le biais de la liste des sites se chargent en mode Internet Explorer, même pendant la navigation initiale du navigateur. Les sites qui ne peuvent pas être configurés pour s’ouvrir dans Internet Explorer, par exemple, les sites dont le modèle n’est pas http:, https:, fichier: ou ftp: ne retardent pas la navigation et le chargement immédiatement en mode Edge.

 Si vous définissez cette stratégie sur la valeur « None » ou si vous ne la configurez pas, lorsque Microsoft Edge ne dispose pas de version mise en cache de la Liste des sites en Mode entreprise, les onglets naviguent immédiatement et n’attendent pas que le navigateur télécharge la Liste des sites en Mode entreprise. Les sites configurés pour s’ouvrir en mode Internet Explorer par le biais de la liste des sites s’ouvrent en mode Microsoft Edge jusqu’à ce que le navigateur ait terminé de télécharger la Liste des sites en Mode entreprise.

Mappage des options de stratégie :

* None (0) = Aucun(e)

* All (1) = Toutes les navigations éligibles

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DelayNavigationsForInitialSiteListDownload
  - Nom de la stratégie de groupe: Exiger que la Liste des sites en Mode entreprise soit disponible avant la navigation d’onglets
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DelayNavigationsForInitialSiteListDownload
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DeleteDataOnMigration
  #### Supprimer les anciennes données de navigateur lors de la migration
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 83 ou ultérieur

  #### Description
  Cette stratégie détermine si les données de navigation utilisateur de Microsoft Edge hérité seront supprimées après la migration vers Microsoft Edge version 81 ou ultérieure.

Si vous définissez cette stratégie sur « Activé », toutes les données de navigation provenant de Microsoft Edge hérité après la migration vers la version 81 de Microsoft Edge ou ultérieure seront supprimées. Cette stratégie doit être définie avant d’effectuer la migration vers Microsoft Edge version 81 ou ultérieure pour avoir un quelconque effet sur les données de navigation existantes.

Si vous définissez cette stratégie sur « Désactivé » ou si la stratégie n’est pas configurée, les données de navigation utilisateur ne sont pas supprimées après la migration vers Microsoft Edge version 83 ou ultérieure.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DeleteDataOnMigration
  - Nom de la stratégie de groupe: Supprimer les anciennes données de navigateur lors de la migration
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DeleteDataOnMigration
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DeveloperToolsAvailability
  #### Contrôler où les outils de développement peuvent être utilisés
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Contrôler l’emplacement où les outils de développement peuvent être utilisés.

Si vous définissez cette stratégie sur « DeveloperToolsDisallowedForForceInstalledExtensions » (valeur par défaut), les utilisateurs peuvent accéder aux outils de développement et à la console JavaScript en général, mais pas dans le contexte des extensions installées par la stratégie d’entreprise.

Si vous définissez cette stratégie sur « DeveloperToolsAllowed » , les utilisateurs peuvent accéder aux outils de développement et à la console JavaScript dans tous les contextes, y compris les extensions installées par la stratégie d’entreprise.

Si vous définissez cette stratégie sur « DeveloperToolsDisallowed », les utilisateurs ne peuvent pas accéder aux outils de développement ni inspecter les éléments du site web. Les raccourcis clavier et les entrées de menu ou de menu contextuel qui ouvrent les outils de développement ou la console JavaScript sont désactivées.

Mappage des options de stratégie :

* DeveloperToolsDisallowedForForceInstalledExtensions (0) = Bloquer les outils de développement sur les extensions installées par la stratégie d’entreprise, autoriser dans d’autres contextes

* DeveloperToolsAllowed (1) = Autoriser l'utilisation d'outils de développement

* DeveloperToolsDisallowed (2) = Ne pas autoriser l’utilisation des outils de développement

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DeveloperToolsAvailability
  - Nom de la stratégie de groupe: Contrôler où les outils de développement peuvent être utilisés
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DeveloperToolsAvailability
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DeveloperToolsAvailability
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DiagnosticData
  #### Envoyer les données de diagnostic obligatoires et facultatives à propos de l’utilisation du navigateur
  
  
  #### Versions prises en charge :
  - Sur Windows 7 et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Cette stratégie contrôle l’envoi des données de diagnostic obligatoires et facultatives sur l’utilisation du navigateur par Microsoft.

 Les données de diagnostic obligatoires sont collectées, conservées Microsoft Edge en toute sécurité, mises à jour et exécutées comme prévu.

 Les données de diagnostic facultatives incluent des données sur la façon dont vous utilisez le navigateur, les sites web que vous visitez et les rapports de blocage envoyés à Microsoft pour améliorer les produits et services.

 Cette stratégie n’est pas prise en charge sur les appareils Windows 10. Pour contrôler cette collecte de données sur Windows 10, les administrateurs informatiques doivent utiliser la stratégie de groupe données de diagnostic de Windows. Selon la version de Windows, cette stratégie est soit « Autoriser la télémétrie », soit « Autoriser les données de diagnostic ». En savoir plus sur la collecte de données de diagnostic dans Windows 10 : [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

Utilisez l’un des paramètres suivants pour configurer cette stratégie :

 « Off » désactive les collections de données de diagnostic obligatoires et facultatives.

 « RequiredData » envoie les données de diagnostic obligatoires, mais désactive la collecte de données de diagnostic facultatives. Microsoft Edge enverra les données de diagnostic obligatoires pour assurer la sécurité, la mise à jour et l’exécution de Microsoft Edge comme prévu.

 « OptionalData » envoie des données de diagnostic facultatives qui incluent des données sur l’utilisation des navigateurs, les sites web visités et les rapports de blocage envoyés à Microsoft pour améliorer les produits et services.

 Sur Windows 7/macOS, cette stratégie contrôle l’envoi des données obligatoires et facultatives à Microsoft.

 Si vous ne configurez pas cette stratégie ou si vous la désactivez, Microsoft Edge prendra par défaut la préférence de l’utilisateur.

Mappage des options de stratégie :

* Off (0) = Faible (non recommandé)

* RequiredData (1) = Données requises

* OptionalData (2) = Données facultatives

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DiagnosticData
  - Nom de la stratégie de groupe: Envoyer les données de diagnostic obligatoires et facultatives à propos de l’utilisation du navigateur
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DiagnosticData
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DiagnosticData
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DirectInvokeEnabled
  #### Autoriser les utilisateurs à ouvrir des fichiers à l’aide du protocole DirectInvoke
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 78 ou ultérieur

  #### Description
  Autorisez les utilisateurs à ouvrir des fichiers à l’aide du protocole DirectInvoke. Le protocole DirectInvoke permet aux sites web de demander que le navigateur ouvre les fichiers d’une URL spécifique à l’aide d’un gestionnaire de fichiers spécifique sur l’ordinateur ou l’appareil de l’utilisateur.

Si vous activez ou ne configurez pas cette stratégie, les utilisateurs peuvent ouvrir des fichiers à l’aide du protocole DirectInvoke.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas ouvrir de fichiers à l’aide du protocole DirectInvoke. Au lieu de cela, le fichier est enregistré dans le système de fichiers.

Remarque : la désactivation de DirectInvoke peut empêcher certaines fonctionnalités de Microsoft Office SharePoint Online de s’utiliser comme prévu.

Pour plus d’informations sur DirectInvoke, voir [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) et [https://go.microsoft.com/fwlink/?linkid=2099871](https://go.microsoft.com/fwlink/?linkid=2099871).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DirectInvokeEnabled
  - Nom de la stratégie de groupe: Autoriser les utilisateurs à ouvrir des fichiers à l’aide du protocole DirectInvoke
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DirectInvokeEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### Disable3DAPIs
  #### Désactiver la prise en charge des API graphiques 3D
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Empêchez les pages web d’accéder à l’unité centrale graphique (GPU). En particulier, les pages web ne peuvent pas accéder à l’API WebGL et les plug-ins ne peuvent pas utiliser l’API Pepper 3D.

Si vous ne configurez pas ou ne désactivez pas cette stratégie, les pages web peuvent utiliser l’API WebGL et les plug-ins peuvent utiliser l’API Pepper 3D. Microsoft Edge peut, par défaut, toujours exiger la transmission d'arguments de ligne de commande pour pouvoir utiliser ces API.

Si la stratégie [HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled) est définie sur false, le paramètre de la stratégie « Disable3DAPIs » est ignoré, ce qui revient à définir la stratégie « Disable3DAPIs » sur true.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: Disable3DAPIs
  - Nom de la stratégie de groupe: Désactiver la prise en charge des API graphiques 3D
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: Disable3DAPIs
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: Disable3DAPIs
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DisableScreenshots
  #### Désactiver la création de captures d’écran
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Contrôle si les utilisateurs peuvent prendre des captures d’écran de la page du navigateur.

Si cette option est activée, l’utilisateur ne peut pas prendre de captures d’écran à l’aide des raccourcis clavier ou des API d’extension.

Si cette option est désactivée ou si vous ne configurez pas cette stratégie, les utilisateurs peuvent prendre des captures d’écran.

Veuillez noter que cette stratégie contrôle les captures d’écran prises dans le navigateur proprement dit. Même si vous activez cette stratégie, les utilisateurs peuvent toujours prendre des captures d’écran en utilisant une méthode en dehors du navigateur (comme l’utilisation d’une fonctionnalité du système d’exploitation ou d’une autre application).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DisableScreenshots
  - Nom de la stratégie de groupe: Désactiver la création de captures d’écran
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DisableScreenshots
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DisableScreenshots
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DiskCacheDir
  #### Définir le répertoire du cache du disque
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Configure le répertoire à utiliser pour stocker les fichiers mis en cache.

	Si vous activez cette stratégie, Microsoft Edge utilise le répertoire spécifié, peu importe si l’utilisateur a spécifié l'indicateur « --disk-cache-dir ». Pour éviter toute perte de données ou d’autres erreurs inattendues, ne configurez pas cette stratégie au répertoire racine d’un volume ni dans un répertoire utilisé à d’autres fins, car Microsoft Edge gère son contenu.

	Voir [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) pour obtenir la liste des variables, que vous pouvez utiliser lorsque vous spécifiez les répertoires et les chemins d’accès.

	Si vous ne configurez pas ce paramètre de stratégie, le répertoire de cache par défaut est utilisé et les utilisateurs peuvent remplacer cette valeur par défaut par l'indicateur de ligne de commande « --disk-cache-dir ».

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DiskCacheDir
  - Nom de la stratégie de groupe: Définir le répertoire du cache du disque
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DiskCacheDir
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"${user_home}/Edge_cache"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DiskCacheDir
  - Exemple de valeur :
``` xml
<string>${user_home}/Edge_cache</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DiskCacheSize
  #### Définir la taille de cache du disque, en octets
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Configurer la taille du cache, en octets, utilisé pour stocker des fichiers sur le disque.

	Si vous activez cette stratégie, Microsoft Edge utilise la taille du cache indiquée, peu importe si l’utilisateur a spécifié l'indicateur « --disk-cache-size ». La valeur spécifiée dans cette stratégie n’est pas une délimitation fixe, mais plutôt une suggestion de système de mise en cache. Toute valeur inférieure à quelques mégaoctets est trop faible et sera arrondie au minimum raisonnable.

	Si vous définissez la valeur de cette stratégie sur 0, la taille de cache par défaut est utilisée et les utilisateurs ne peuvent pas la modifier.

	Si vous ne configurez pas cette stratégie, la taille par défaut est utilisée, mais les utilisateurs peuvent la remplacer par l'indicateur « --disk-cache-size ».

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DiskCacheSize
  - Nom de la stratégie de groupe: Définir la taille de cache du disque, en octets
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DiskCacheSize
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x06400000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DiskCacheSize
  - Exemple de valeur :
``` xml
<integer>104857600</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DnsOverHttpsMode
  #### Contrôler le mode DNS-sur-HTTPs
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 83 ou version ultérieure

  #### Description
  Contrôlez le mode du résolveur DNS-sur-HTTPS. Notez que cette stratégie ne définira que le mode par défaut pour chaque requête. Ce mode peut être modifié pour des types de requêtes particuliers, comme les demandes de résolution d'un nom d'hôte de serveur DNS-sur-HTTPS.

Le"off" mode désactivera le DNS-sur-HTTPS.

 Le "automatic" mode enverra d'abord des requêtes DNS-sur-HTTPS si un serveur DNS-sur-HTTPS est disponible et peut se rabattre sur l'envoi de requêtes non sécurisées en cas d'erreur.

 Le "secure" mode n'envoie que des requêtes DNS sur HTTPS et ne résout pas les erreurs.

 Si vous ne configurez pas cette politique, le navigateur peut envoyer des requêtes DNS-sur-HTTPS à un résolveur associé au résolveur système configuré par l'utilisateur.

Mappage des options de stratégie :

* off (off) = Désactiver DNS-sur-HTTPs

* automatic (automatic) = Activer DNS-sur-HTTPs avec un secours non sécurisé

* secure (secure) = Activer DNS-sur-HTTPs sans aucun secours non sécurisé

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DnsOverHttpsMode
  - Nom de la stratégie de groupe: Contrôler le mode DNS-sur-HTTPs
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DnsOverHttpsMode
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"off"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DnsOverHttpsMode
  - Exemple de valeur :
``` xml
<string>off</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DnsOverHttpsTemplates
  #### Spécifier le modèle d’URI du programme de résolution DNS sur HTTPS souhaité
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 83 ou version ultérieure

  #### Description
  Modèle d’URI du programme de résolution DNS-sur-HTTPS souhaité. Pour spécifier plusieurs programmes de résolution DNS-sur-HTTPS, séparez les modèles d’URI correspondants par des espaces.

Si vous définissez [DnsOverHttpsMode](#dnsoverhttpsmode) sur "secure", cette stratégie doit être définie et ne pas être vide.

Si vous définissez [DnsOverHttpsMode](#dnsoverhttpsmode) sur "automatic" et que cette stratégie est définie, les modèles d’URI spécifiés seront utilisés. Si vous ne définissez pas cette stratégie, les mappages codés en dur seront utilisés pour tenter de mettre à niveau le programme de résolution DNS actuel de l’utilisateur vers un programme de résolution DoH géré par le même fournisseur.

Si le modèle d’URI contient une variable dns, les demandes adressées au programme de résolution utilisent GET. Sinon, les demandes utiliseront POST.

Les modèles au format incorrect seront ignorés.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DnsOverHttpsTemplates
  - Nom de la stratégie de groupe: Spécifier le modèle d’URI du programme de résolution DNS sur HTTPS souhaité
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: DnsOverHttpsTemplates
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"https://dns.example.net/dns-query{?dns}"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DnsOverHttpsTemplates
  - Exemple de valeur :
``` xml
<string>https://dns.example.net/dns-query{?dns}</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DownloadDirectory
  #### Définir le répertoire de téléchargement
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Configure le répertoire à utiliser lors du téléchargement des fichiers.

Si vous activez cette stratégie, Microsoft Edge utilise le répertoire indiqué, peu importe que l’utilisateur en ait spécifié un ou non, ou qu'il ait choisi d'être invité à sélectionner l'emplacement de téléchargement à chaque fois. Voir [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) pour obtenir la liste des variables pouvant être utilisées.

Si vous désactivez ou ne configurez pas cette stratégie, le répertoire de téléchargement par défaut est utilisé et l’utilisateur peut le modifier.

Si un chemin d’accès non valide est défini, Microsoft Edge utilise par défaut le répertoire de téléchargement par défaut de l’utilisateur.

Si le dossier spécifié par le chemin d'accès n’existe pas, le téléchargement déclenche une invite demandant à l’utilisateur où il souhaite enregistrer son téléchargement.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DownloadDirectory
  - Nom de la stratégie de groupe: Définir le répertoire de téléchargement
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: DownloadDirectory
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"\n      Linux-based OSes (including Mac): /home/${user_name}/Downloads\n      Windows: C:\\Users\\${user_name}\\Downloads"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DownloadDirectory
  - Exemple de valeur :
``` xml
<string>
      Linux-based OSes (including Mac): /home/${user_name}/Downloads
      Windows: C:\Users\${user_name}\Downloads</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### DownloadRestrictions
  #### Autoriser les restrictions de téléchargement
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Configure le type de téléchargements que Microsoft Edge bloque complètement, sans laisser les utilisateurs passer outre la décision de sécurité.

Définissez « Bloquer les téléchargements dangereux » pour autoriser tous les téléchargements, à l'exception de ceux qui comportent des avertissements Microsoft Defender SmartScreen.

  Définissez « Bloquer les téléchargements potentiellement dangereux » pour autoriser tous les téléchargements, à l'exception de ceux qui comportent des avertissements Microsoft Defender SmartScreen concernant des téléchargements potentiellement dangereux ou indésirables.

  Définissez « BlockAllDownloads » pour bloquer tous les téléchargements.

  Si vous ne configurez pas cette stratégie ou ne définissez pas l'option « DefaultDownloadSecurity », les téléchargements sont soumis aux restrictions de sécurité habituelles basées sur les résultats d'analyse de Microsoft Defender SmartScreen.

  Notez que ces restrictions s'appliquent aux téléchargements à partir du contenu des pages web, ainsi qu'à l'option de menu contextuel « lien de téléchargement...». Ces restrictions ne s'appliquent pas à l'enregistrement ou au téléchargement de la page actuellement affichée, ni à l'option « Enregistrer en PDF » des options d'impression.

  Voir [https://go.microsoft.com/fwlink/?linkid=2094934](https://go.microsoft.com/fwlink/?linkid=2094934) pour plus d'informations sur Microsoft Defender SmartScreen.

Mappage des options de stratégie :

* DefaultDownloadSecurity (0) = Aucune restriction particulière

* BlockDangerousDownloads (1) = Bloquer les téléchargements dangereux

* BlockPotentiallyDangerousDownloads (2) = Bloquer les téléchargements potentiellement dangereux ou indésirables

* BlockAllDownloads (3) = Bloquer tous les téléchargements

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: DownloadRestrictions
  - Nom de la stratégie de groupe: Autoriser les restrictions de téléchargement
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: DownloadRestrictions
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: DownloadRestrictions
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### EdgeCollectionsEnabled
  #### Activer la fonctionnalité Collections
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 78 ou version ultérieure

  #### Description
  Vous permet d'autoriser les utilisateurs à accéder à la fonctionnalité Collections afin de pouvoir collecter, organiser, partager et exporter du contenu de manière plus efficace et avec l'intégration d'Office.

Si vous activez ou ne configurez pas cette stratégie, les utilisateurs peuvent accéder à la fonctionnalité Collections et l'utiliser dans Microsoft Edge.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas accéder à la fonctionnalité Collections et ne peuvent pas l'utiliser dans Microsoft Edge.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: EdgeCollectionsEnabled
  - Nom de la stratégie de groupe: Activer la fonctionnalité Collections
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: EdgeCollectionsEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: EdgeCollectionsEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### EditFavoritesEnabled
  #### Autorise les utilisateurs à modifier les favoris
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Activez cette stratégie pour permettre aux utilisateurs d’ajouter, de supprimer et de modifier des favoris. Il s'agit du comportement par défaut si vous ne configurez pas la stratégie.

Désactivez cette stratégie pour empêcher les utilisateurs d’ajouter, de supprimer et de modifier des favoris. Ils peuvent toujours utiliser des favoris existants.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: EditFavoritesEnabled
  - Nom de la stratégie de groupe: Autorise les utilisateurs à modifier les favoris
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: EditFavoritesEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: EditFavoritesEnabled
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### EnableDeprecatedWebPlatformFeatures
  #### Réactiver les fonctionnalités de plateforme web déconseillées pendant une durée limitée
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifiez la liste des fonctionnalités de plateforme web déconseillées à réactiver temporairement.

Cette stratégie vous permet de réactiver des fonctionnalités de plateforme web déconseillées pendant une durée limitée. Les fonctionnalités sont identifiées par une balise de chaîne.

Si vous ne configurez pas cette stratégie, si la liste est vide ou si une fonctionnalité ne correspond pas à l'une des balises de chaîne prises en charge, toutes les fonctionnalités de plateforme web déconseillées restent désactivées.

Alors que la stratégie proprement dite est prise en charge sur les plateformes ci-dessus, la fonctionnalité qu'elle active n’est peut-être pas disponible sur toutes ces plateformes. Toutes les fonctionnalités de plateforme web déconseillées ne peuvent pas être réactivées. Seules celles qui sont explicitement répertoriées ci-dessous peuvent être réactivées et uniquement pendant une durée limitée, qui diffère selon la fonctionnalité. Vous pouvez consulter l’intention des modifications des fonctionnalités de plateforme web à l'adresse https://bit.ly/blinkintents.

Le format général de la balise de chaîne est [DeprecatedFeatureName]_EffectiveUntil[yyyymmdd].

Mappage des options de stratégie :

* ExampleDeprecatedFeature (ExampleDeprecatedFeature_EffectiveUntil20080902) = Activer l'API ExampleDeprecatedFeature par le biais de 2008/09/02

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: EnableDeprecatedWebPlatformFeatures
  - Nom de la stratégie de groupe: Réactiver les fonctionnalités de plateforme web déconseillées pendant une durée limitée
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures\1 = "ExampleDeprecatedFeature_EffectiveUntil20080902"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: EnableDeprecatedWebPlatformFeatures
  - Exemple de valeur :
``` xml
<array>
  <string>ExampleDeprecatedFeature_EffectiveUntil20080902</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### EnableDomainActionsDownload
  #### Activer le téléchargement des actions de domaine à partir de Microsoft (obsolète)
  
  >OBSOLÈTE : cette stratégie est obsolète et ne fonctionne pas après Microsoft Edge84.
  #### Versions prises en charge :
  - Sur Windows et macOS depuis le 77, jusqu’au 84

  #### Description
  Cette stratégie ne fonctionne pas, car des états en conflit doivent être évités. Cette stratégie était utilisée pour activer/désactiver le téléchargement de la liste des actions de domaine, mais elle n'atteignait pas toujours l'état souhaité. Le service Expérimentation et configuration, qui gère le téléchargement, possède sa propre stratégie pour configurer ce qui est téléchargé à partir du service. Utilisez plutôt la stratégie [ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol).

Dans Microsoft Edge, les actions de domaine représentent une série de fonctionnalités de compatibilité permettant au navigateur de fonctionner correctement sur le web.

Microsoft conserve la liste des actions à entreprendre sur certains domaines pour des raisons de compatibilité. Par exemple, le navigateur peut remplacer la chaîne Agent utilisateur sur un site web si ce site web a été bloqué en raison de la nouvelle chaîne Agent utilisateur dans Microsoft Edge. Chacune de ces actions est destinée à être temporaire, tandis que Microsoft tente de résoudre le problème avec le propriétaire du site.

Au démarrage du navigateur, puis régulièrement par la suite, le navigateur va contacter le service Expérimentation et configuration, qui contient la liste la plus à jour des actions de compatibilité a exécuter. Cette liste est enregistrée localement une fois qu’elle a été récupérée afin que les demandes ultérieures ne mettent à jour que la liste si la copie du serveur a été modifiée.

Si vous activez cette stratégie, la liste des actions de domaine continue à être téléchargée à partir du service Expérimentation et configuration.

Si vous désactivez cette stratégie, la liste des actions de domaine n’est plus téléchargée à partir du service de Expérimentation et configuration.

Si vous ne configurez pas cette stratégie, la liste des actions de domaine continue à être téléchargée à partir du service Expérimentation et configuration.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: EnableDomainActionsDownload
  - Nom de la stratégie de groupe: Activer le téléchargement des actions de domaine à partir de Microsoft (obsolète)
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: EnableDomainActionsDownload
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: EnableDomainActionsDownload
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### EnableOnlineRevocationChecks
  #### Activer les contrôles de protocole OCSP/liste de révocation de certificats en ligne
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Les vérifications de révocation en ligne ne fournissent pas un avantage de sécurité significatif et sont désactivées par défaut.

Si vous activez cette stratégie, Microsoft Edge effectue des vérifications OCSP/de liste de révocation de certificats en ligne d'erreur irrécupérable. « Erreur irrécupérable » signifie que si le serveur de révocation est inaccessible, le certificat est considéré comme valide.

Si vous désactivez la stratégie ou si vous ne la configurez pas, Microsoft Edge n’effectue pas de vérifications de révocation en ligne.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: EnableOnlineRevocationChecks
  - Nom de la stratégie de groupe: Activer les contrôles de protocole OCSP/liste de révocation de certificats en ligne
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: EnableOnlineRevocationChecks
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: EnableOnlineRevocationChecks
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### EnableSha1ForLocalAnchors
  #### Autoriser les certificats signés avec SHA-1 lorsqu’ils sont émis par des ancres d’approbation locales (déconseillé)
  >DÉCONSEILLÉ : cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 85 ou version ultérieure

  #### Description
  Lorsque ce paramètre est activé, Microsoft Edge autorise les connexions sécurisées par des certificats signés SHA-1 tant que le certificat est chaîné à un certificat racine installé localement et est valide.

Notez que cette stratégie dépend de la pile de vérification des certificats du système d’exploitation (OS) permettant d’autoriser les signatures SHA-1. Si une mise à jour du système d’exploitation modifie le traitement par le système d’exploitation des certificats SHA-1, cette stratégie risque de ne plus être appliquée.  De plus, cette stratégie est prévue comme une solution de contournement temporaire pour offrir aux entreprises davantage de temps pour quitter SHA-1. Cette stratégie sera supprimée dans Microsoft Edge 92 qui sera publiée au milieu de 2021.

      Si vous ne configurez pas cette stratégie ou si vous la configurez sur false, ou si le certificat SHA-1 est chaîné à un certificat racine approuvé publiquement, Microsoft Edge n’autorisera pas les certificats signés par SHA-1.

       Cette stratégie est uniquement disponible sur les instances Windows qui sont jointes à un domaine Microsoft Active Directory ou aux instances Windows 10 Professionnel ou Entreprise inscrites pour la gestion des appareils, ou les instances macOS qui sont gérées via la gestion des périphériques mobiles ou qui sont jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: EnableSha1ForLocalAnchors
  - Nom de la stratégie de groupe: Autoriser les certificats signés avec SHA-1 lorsqu’ils sont émis par des ancres d’approbation locales (déconseillé)
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: EnableSha1ForLocalAnchors
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: EnableSha1ForLocalAnchors
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### EnterpriseHardwarePlatformAPIEnabled
  #### Autoriser les extensions managées de manière à utiliser l’API de plateforme de matériel d’entreprise
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 78 ou version ultérieure

  #### Description
  Si cette stratégie est activée, les extensions installées par la stratégie d’entreprise sont autorisées à utiliser l’API de plateforme de matériel d’entreprise.
	Si vous désactivez cette stratégie ou ne la configurez pas, aucune extension n’est autorisée à utiliser l’API de plateforme de matériel d’entreprise.
	Cette stratégie s’applique également aux extensions de composant.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: EnterpriseHardwarePlatformAPIEnabled
  - Nom de la stratégie de groupe: Autoriser les extensions managées de manière à utiliser l’API de plateforme de matériel d’entreprise
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: EnterpriseHardwarePlatformAPIEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: EnterpriseHardwarePlatformAPIEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### EnterpriseModeSiteListManagerAllowed
  #### Autoriser l’accès à l’outil Gestionnaire de liste de sites en mode entreprise
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 86 ou ultérieur

  #### Description
  Vous permet de déterminer si le Gestionnaire de liste de sites en mode entreprise est disponible pour les utilisateurs.

Si vous activez cette stratégie, les utilisateurs peuvent voir le bouton de navigation de l’outil Gestionnaire de liste de sites en mode entreprise dans la page edge://compat. Accédez à l’outil et utilisez-le.

 Si vous désactivez ou si vous ne configurez pas cette stratégie, les utilisateurs ne peuvent pas voir le bouton de navigation du Gestionnaire de liste de sites en mode entreprise et ne peuvent pas utiliser l’outil.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: EnterpriseModeSiteListManagerAllowed
  - Nom de la stratégie de groupe: Autoriser l’accès à l’outil Gestionnaire de liste de sites en mode entreprise
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: EnterpriseModeSiteListManagerAllowed
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  #### Désactiver le téléchargement des avertissements basés sur l’extension de type de fichier pour les types de fichiers spécifiés sur les domaines
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 85 ou version ultérieure

  #### Description
  Vous pouvez activer cette stratégie pour créer un dictionnaire des extensions de type de fichier avec une liste correspondante de domaines qui seront exemptés des avertissements de téléchargement basé sur l’extension de type de fichier. Cela permet aux administrateurs d’entreprise de bloquer les avertissements de téléchargement basés sur l’extension de type de fichier pour les fichiers associés à un domaine répertorié. Par exemple, si l’extension « jnlp » est associée à « website1.com », les utilisateurs ne verront pas d’avertissement lors du téléchargement de fichiers « JNLP » à partir de « website1.com », mais verront un avertissement de téléchargement lors du téléchargement de fichiers « jnlp » à partir de « website2.com ».

Les fichiers avec l’extension de type de fichier spécifiée pour les domaines identifiés par cette stratégie seront toujours soumis à des avertissements de sécurité basés sur l’extension de type non-fichier, tels que des avertissements de téléchargement de contenu mixte et des avertissements de Microsoft Defender SmartScreen.

Si vous désactivez ce paramètre de stratégie ou si vous ne le configurez pas, les types de fichiers qui déclenchent des avertissements de téléchargement basé sur les extensions affichent des avertissements à l’utilisateur.

Si vous activez ce paramètre de stratégie :

* Le modèle d’URL doit être mis en forme selon [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).
  * L’extension de type de fichier entrée doit être en minuscules ASCII. Le séparateur de début ne doit pas être inclus dans la liste des extensions de type de fichier, de sorte que la liste « jnlp » doit être utilisée à la place de « .jnlp ».

 Exemple :

 L’exemple de valeur suivant empêche l’extension de type fichier des avertissements de téléchargement basés sur les extensions swf, exe et jnlp pour les domaines *. contoso.com. Il indiquera à l’utilisateur un avertissement de téléchargement basé sur une extension de type de fichier sur tout autre domaine pour les fichiers exe et jnlp, mais pas pour les fichiers swf.

 [
    { "file_extension": "jnlp", "domains": ["contoso.com"] },
    { "file_extension": "exe", "domains": ["contoso.com"] },
   { "file_extension": "swf", "domains": ["*"] }
   ]

 Notez que, bien que l’exemple précédent montre la suppression des avertissements de téléchargement basé sur le type d’extension pour les fichiers « swf » de tous les domaines, l’application de la suppression de ceux-ci n’est pas recommandé pour des raisons de sécurité. Elle n’est affichée dans l’exemple que pour démontrer que vous avez la possibilité de le faire.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Nom de la stratégie de groupe: Désactiver le téléchargement des avertissements basés sur l’extension de type de fichier pour les types de fichiers spécifiés sur les domaines
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\1 = {"domains": ["https://contoso.com", "contoso2.com"], "file_extension": "jnlp"}
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\2 = {"domains": ["*"], "file_extension": "swf"}

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Exemple de valeur :
``` xml
<array>
  <string>{'domains': ['https://contoso.com', 'contoso2.com'], 'file_extension': 'jnlp'}</string>
  <string>{'domains': ['*'], 'file_extension': 'swf'}</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ExperimentationAndConfigurationServiceControl
  #### Contrôler la communication avec le service d’expérimentation et de configuration
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Dans Microsoft Edge, le service Expérimentation et configuration permet de déployer la charge utile d’expérimentation et de configuration.

La charge utile de l’expérimentation consiste en une liste des fonctionnalités à un stade précoce de développement qui sont activées par Microsoft à des fins de test et de commentaires.

La charge utile de la configuration consiste en une liste de paramètres que Microsoft souhaite déployer pour Microsoft Edge afin d'optimiser l’expérience utilisateur. Par exemple, la charge utile de la configuration peut spécifier la fréquence à laquelle Microsoft Edge envoie des demandes au service Expérimentation et configuration pour récupérer la charge utile la plus récente.

En outre, la charge utile de la configuration peut également contenir la liste des actions à exécuter sur certains domaines pour des raisons de compatibilité. Par exemple, le navigateur peut remplacer la chaîne Agent utilisateur sur un site web si ce site web est bloqué en raison de la nouvelle chaîne Agent utilisateur dans Microsoft Edge. Chacune de ces actions est destinée à être temporaire, tandis que Microsoft tente de résoudre le problème avec le propriétaire du site.

Si vous définissez cette stratégie sur « FullMode», la charge utile complète est téléchargée à partir du service Expérimentation et configuration. Cela inclut les charges utiles de l’expérimentation et celles de la configuration.

Si vous définissez cette stratégie sur le mode « Configurations uniquement », seule la charge utile de la configuration est livrée.

Si vous définissez cette stratégie sur « RestrictedMode », la communication avec le service Expérimentation et configuration est complètement arrêtée.

Si vous ne configurez pas cette stratégie, sur un appareil géré sur des canaux stables et bêta, le comportement est le même que« ConfigurationsOnlyMode ».

Si vous ne configurez pas cette stratégie, sur un appareil non géré, le comportement est identique au « FullMode »

Mappage des options de stratégie :

* FullMode (2) = Récupérer les configurations et les expérimentations

* ConfigurationsOnlyMode (1) = Récupérer les configurations uniquement

* RestrictedMode (0) = Désactiver la communication avec le service d’expérimentation et de configuration

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ExperimentationAndConfigurationServiceControl
  - Nom de la stratégie de groupe: Contrôler la communication avec le service d’expérimentation et de configuration
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ExperimentationAndConfigurationServiceControl
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ExperimentationAndConfigurationServiceControl
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ExternalProtocolDialogShowAlwaysOpenCheckbox
  #### Afficher la case à cocher « Toujours ouvrir » dans la boîte de dialogue de protocole externe
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 79 ou version ultérieure

  #### Description
  Cette stratégie contrôle si la case à cocher « Toujours autoriser ce site à ouvrir les liens de ce type » s’affiche dans les invites de confirmation de lancement de protocole externe. Cette stratégie s’applique uniquement aux liens https://.

 Si vous activez cette stratégie, lorsqu’une invite de confirmation de protocole externe s’affiche, l’utilisateur peut sélectionner l’option « Toujours autoriser » pour ignorer toutes les invites de confirmation ultérieures pour le protocole sur ce site.

Si vous désactivez cette stratégie, la case à cocher « Toujours autoriser » ne s’affiche pas. L’utilisateur est invité à confirmer chaque fois qu’un protocole externe est appelé.

 Avant Microsoft Edge 83, Si vous ne configurez pas cette stratégie, la case à cocher « Toujours autoriser » ne s’affiche pas. L’utilisateur est invité à confirmer chaque fois qu’un protocole externe est appelé.

 Sur Microsoft Edge 83, si vous ne configurez pas cette stratégie, la visibilité de la case à cocher est contrôlée par l’indicateur « Activer le protocole de mémorisation des préférences de lancement de protocole » dans edge://flags

 À partir de Microsoft Edge 84, si vous ne configurez pas cette stratégie, lorsqu’une invite de confirmation de protocole externe s’affiche, l’utilisateur peut sélectionner l’option « Toujours autoriser » pour ignorer toutes les invites de confirmation ultérieures pour le protocole sur ce site.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Nom de la stratégie de groupe: Afficher la case à cocher « Toujours ouvrir » dans la boîte de dialogue de protocole externe
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### FamilySafetySettingsEnabled
  #### Autoriser les utilisateurs à configurer Family Safety
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 83 ou version ultérieure

  #### Description
  Cette stratégie désactive et masque complètement la page contrôle parental dans paramètres. La navigation vers edge://settings/familysafety sera également bloquée. La page contrôle parental décrit les fonctionnalités disponibles pour les groupes familiaux et la manière de rejoindre un groupe familial. En savoir plus sur le contrôle parental ici : ([https://go.microsoft.com/fwlink/?linkid=2098432](https://go.microsoft.com/fwlink/?linkid=2098432)).

Si vous activez ce paramètre de stratégie ou si vous ne le configurez pas, la page contrôle parental s’affiche.

Si vous désactivez cette stratégie, la page contrôle parental ne s’affiche pas.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: FamilySafetySettingsEnabled
  - Nom de la stratégie de groupe: Autoriser les utilisateurs à configurer Family Safety
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: FamilySafetySettingsEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: FamilySafetySettingsEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### FavoritesBarEnabled
  #### Activer la barre des favoris
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Active ou désactive la barre des favoris.

Si vous activez cette stratégie, les utilisateurs voient la barre des favoris.

Si vous désactivez cette stratégie, les utilisateurs ne voient pas la barre des favoris.

Si cette stratégie n’est pas configurée, l’utilisateur peut décider d’utiliser la barre des favoris ou non.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: FavoritesBarEnabled
  - Nom de la stratégie de groupe: Activer la barre des favoris
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: FavoritesBarEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: FavoritesBarEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ForceBingSafeSearch
  #### Appliquer la recherche sécurisée Bing
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Assurez-vous que les requêtes de recherche sur le web Bing sont effectuées avec la recherche sécurisée définie sur la valeur spécifiée. Les utilisateurs ne peuvent pas modifier ce paramètre.

Si vous configurez cette stratégie sur « BingSafeSearchNoRestrictionsMode », la recherche sécurisée de Recherche Bing revient à la valeur bing.com.

Si vous configurez cette stratégie sur « BingSafeSearchModerateMode », le paramètre modéré est utilisé dans la recherche sécurisée. Le paramètre modéré filtre les vidéos pour adultes et les images, mais pas le texte, des résultats de recherche.

Si vous configurez cette stratégie sur « BingSafeSearchStrictMode », le paramètre strict de la recherche sécurisée est utilisé. Le paramètre strict filtre le texte, les images et les vidéos pour adultes.

Si vous désactivez cette stratégie ou ne la configurez pas, la recherche sécurisée de Recherche Bing n’est pas appliquée et les utilisateurs peuvent définir la valeur de leur choix sur bing.com.

Mappage des options de stratégie :

* BingSafeSearchNoRestrictionsMode (0) = Ne pas configurer de restrictions de recherche dans Bing

* BingSafeSearchModerateMode (1) = Configurer des restrictions de recherche modérées dans Bing

* BingSafeSearchStrictMode (2) = Configurer des restrictions de recherche strictes dans Bing

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ForceBingSafeSearch
  - Nom de la stratégie de groupe: Appliquer la recherche sécurisée Bing
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ForceBingSafeSearch
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ForceBingSafeSearch
  - Exemple de valeur :
``` xml
<integer>0</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ForceCertificatePromptsOnMultipleMatches
  #### Configurez si Microsoft Edge doit sélectionner automatiquement un certificat lorsqu’il existe plusieurs correspondances de certificats pour un site configuré avec "AutoSelectCertificateForUrls"
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 81 ou version ultérieure

  #### Description
  Indique si les utilisateurs sont invités à sélectionner un certificat si plusieurs certificats sont disponibles et qu’un site est configuré avec [AutoSelectCertificateForUrls](#autoselectcertificateforurls). Si vous ne configurez pas [AutoSelectCertificateForUrls](#autoselectcertificateforurls) pour un site, l’utilisateur est toujours invité à sélectionner un certificat.

Si vous définissez cette stratégie sur True, Microsoft Edge invite un utilisateur à sélectionner un certificat pour les sites de la liste définie dans [AutoSelectCertificateForUrls](#autoselectcertificateforurls) si et seulement s’il y a plusieurs certificats.

Si vous définissez cette stratégie sur False ou si vous ne la configurez pas, Microsoft Edge sélectionne automatiquement un certificat, même s’il existe plusieurs correspondances pour un certificat. L’utilisateur n'est pas invité à sélectionner un certificat pour les sites de la liste définie dans [AutoSelectCertificateForUrls](#autoselectcertificateforurls).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ForceCertificatePromptsOnMultipleMatches
  - Nom de la stratégie de groupe: Configurez si Microsoft Edge doit sélectionner automatiquement un certificat lorsqu’il existe plusieurs correspondances de certificats pour un site configuré avec "AutoSelectCertificateForUrls"
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ForceCertificatePromptsOnMultipleMatches
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ForceCertificatePromptsOnMultipleMatches
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ForceEphemeralProfiles
  #### Activer l’utilisation des profils éphémères
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Contrôle si les profils utilisateur sont basculés en mode éphémère. Un profil éphémère est créé au début d'une session, supprimé à la fin de la session et associé au profil d’origine de l’utilisateur.

Si vous activez cette stratégie, les profils s’exécutent en mode éphémère. Cela permet aux utilisateurs de travailler à partir de leurs propres appareils sans enregistrer les données de navigation sur ces appareils. Si vous activez cette stratégie en tant que stratégie de système d'exploitation (en utilisant le GPO sous Windows, par exemple), elle s’applique à chaque profil du système.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, les utilisateurs obtiennent leur profil normal lorsqu’ils se connectent au navigateur.

En mode éphémère, les données de profil ne sont enregistrées sur le disque que pour la durée de la session utilisateur. Les fonctionnalités, telles que l’historique du navigateur, les extensions et leurs données, les données web, telles que les cookies et les bases de données web, ne sont pas enregistrées après la fermeture du navigateur. Ceci n’empêche pas les utilisateurs de télécharger manuellement des données sur le disque, ni d’enregistrer des pages ou de les imprimer. Si l’utilisateur a activé la synchronisation, toutes les données sont conservées dans leurs comptes de synchronisation, comme avec les profils normaux. Les utilisateurs peuvent également utiliser la navigation InPrivate en mode éphémère, sauf si vous désactivez explicitement cette option.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ForceEphemeralProfiles
  - Nom de la stratégie de groupe: Activer l’utilisation des profils éphémères
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ForceEphemeralProfiles
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ForceEphemeralProfiles
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ForceGoogleSafeSearch
  #### Appliquer Google SafeSearch
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Force l'exécution des requêtes Recherche Web Google avec la fonctionnalité SafeSearch activée et empêche les utilisateurs de modifier ce paramètre.

Si vous activez cette stratégie, la fonctionnalité SafeSearch de Recherche Google est toujours active.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, la fonctionnalité SafeSearch de Recherche Google n’est pas appliquée.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ForceGoogleSafeSearch
  - Nom de la stratégie de groupe: Appliquer Google SafeSearch
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ForceGoogleSafeSearch
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ForceGoogleSafeSearch
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ForceLegacyDefaultReferrerPolicy
  #### Utilisez une stratégie de renvoi par défaut no-referrer-when-downgrade (déconseillé)
  >DÉCONSEILLÉ : cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 81 ou version ultérieure

  #### Description
  Cette stratégie n’est plus utilisée, car elle est conçue comme un mécanisme à court terme destiné à offrir aux entreprises davantage de temps pour mettre à jour leur contenu web incompatible avec la stratégie de référent par défaut actuelle. Elle ne fonctionnera pas dans Microsoft Edge version 86.

La stratégie de référent par défaut de Microsoft Edge est renforcée en remplaçant sa valeur actuelle no-referrer-when-downgrade par la valeur plus sécurisée strict-origin-when-cross-origin dans le cadre d’un déploiement progressif.

 Avant le déploiement, cette stratégie d’entreprise n’aura aucun effet. Une fois la stratégie activée, la stratégie de référent par défaut de Microsoft Edge sera définie sur son ancienne valeur (no-referrer-when-downgrade).

Cette stratégie d’entreprise est désactivée par défaut.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ForceLegacyDefaultReferrerPolicy
  - Nom de la stratégie de groupe: Utilisez une stratégie de renvoi par défaut no-referrer-when-downgrade (déconseillé)
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ForceLegacyDefaultReferrerPolicy
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ForceLegacyDefaultReferrerPolicy
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ForceNetworkInProcess
  #### Forcer le code de mise en réseau à s’exécuter dans le processus du navigateur (obsolète)
  
  >OBSOLÈTE : cette stratégie est obsolète et ne fonctionne pas après Microsoft Edge83.
  #### Versions prises en charge :
  - Sur Windows depuis 78, jusqu’à 83

  #### Description
  Cette stratégie ne fonctionne pas parce qu’elle n’était destinée qu’à être un mécanisme à court terme pour offrir aux entreprises davantage de temps pour la migration vers des logiciels tiers qui ne dépendent pas de l’accrochage des API réseau. Les serveurs proxy sont recommandés pour les LSP et la mise à jour de l’API Win32.

Cette stratégie force l’exécution du code réseau dans le processus de navigateur.

Cette stratégie est désactivée par défaut. Si cette option est activée, les utilisateurs sont ouverts aux problèmes de sécurité lorsque le processus de mise en réseau est en mode sandbox.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ForceNetworkInProcess
  - Nom de la stratégie de groupe: Forcer le code de mise en réseau à s’exécuter dans le processus du navigateur (obsolète)
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ForceNetworkInProcess
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ForceSync
  #### Forcer la synchronisation des données du navigateur et ne pas afficher l’invite de consentement de synchronisation
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Force la synchronisation des données dans Microsoft Edge. Cette stratégie empêche également l’utilisateur de désactiver la synchronisation.

Si vous ne configurez pas cette stratégie, les utilisateurs peuvent activer ou désactiver la synchronisation. Si vous activez cette stratégie, les utilisateurs ne peuvent pas désactiver la synchronisation.

Pour que cette stratégie fonctionne correctement, la stratégie
[BrowserSignin](#browsersignin) ne doit pas être configurée, ou doit être activée. Si [ForceSync](#forcesync) est désactivée, [BrowserSignin](#browsersignin) ne sera pas prise en compte.

[SyncDisabled](#syncdisabled) ne doit pas être configurée ou doit être définie sur False. Si elle est définie sur True, [ForceSync](#forcesync) ne sera pas prise en compte.

0 = ne pas démarrer automatiquement la synchronisation et afficher le consentement de synchronisation (par défaut)
1 = forcer la synchronisation pour Azure AD/Azure AD-dégradation du profil utilisateur et ne pas afficher l’invite de consentement de synchronisation

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ForceSync
  - Nom de la stratégie de groupe: Forcer la synchronisation des données du navigateur et ne pas afficher l’invite de consentement de synchronisation
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ForceSync
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ForceSync
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ForceYouTubeRestrict
  #### Forcer le mode Limité YouTube minimal
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Applique un mode Limité minimal à YouTube et empêche les utilisateurs de sélectionner un mode limité inférieur.

Définissez sur Strict pour appliquer le mode Limité strict à YouTube.

Définissez sur Modéré Moderate pour autoriser l’utilisateur à n’utiliser que les modes Limité modéré et Limité strict à YouTube. Il ne peut pas désactiver le mode Limité.

Définissez sur Off ou ne configurez pas cette stratégie pour ne pas appliquer le mode Limité à YouTube. Les stratégies externes, telles que les stratégies YouTube, peuvent encore appliquer le mode Limité.

Mappage des options de stratégie :

* Off (0) = Ne pas appliquer le mode Limité à YouTube

* Moderate (1) = Appliquer au moins le mode Limité modéré à YouTube

* Strict (2) = Appliquer le mode Limité strict pour YouTube

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ForceYouTubeRestrict
  - Nom de la stratégie de groupe: Forcer le mode Limité YouTube minimal
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ForceYouTubeRestrict
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ForceYouTubeRestrict
  - Exemple de valeur :
``` xml
<integer>0</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### FullscreenAllowed
  #### Autoriser le mode plein écran
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 77 ou ultérieur

  #### Description
  Définissez la disponibilité du mode plein écran : la totalité de l'IU Microsoft Edge est masquée et seul le contenu web est visible.

	Si vous activez cette stratégie ou si vous ne la configurez pas, l’utilisateur, les applications et les extensions avec les autorisations appropriées peuvent passer en mode plein écran.

	Si vous désactivez cette stratégie, les utilisateurs, les applications et les extensions ne peuvent pas passer en mode plein écran.

	L’ouverture de Microsoft Edge en mode plein écran à l’aide de la ligne de commande n’est pas disponible lorsque le mode plein écran est désactivé.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: FullscreenAllowed
  - Nom de la stratégie de groupe: Autoriser le mode plein écran
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: FullscreenAllowed
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### GloballyScopeHTTPAuthCacheEnabled
  #### Activer le cache d'autorisation HTTP globalement étendu
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 81 ou version ultérieure

  #### Description
  Cette stratégie configure un cache global unique par profil avec les informations d’identification du serveur HTTP.

Si vous désactivez ce paramètre de stratégie ou si vous ne le configurez pas, le navigateur utilise le comportement par défaut de l’authentification inter-site, qui, à partir de la version 80, comprendra toutes les informations d’authentification du serveur HTTP en commençant par le site de meilleur niveau. Par conséquent, si deux sites utilisent des ressources provenant du même domaine d’authentification, les informations d’identification devront être renseignées indépendamment dans le contexte des deux sites. Les informations d’identification du proxy mis en cache seront réutilisées sur les sites.

Si vous activez ce paramètre, les informations d’authentification HTTP de stratégie entrées dans le contexte d’un site sont automatiquement utilisées dans le contexte d’un autre site.

L’activation de cette stratégie laisse les sites ouverts à certains types d’attaques inter-site et permet d’effectuer le suivi des utilisateurs sur les sites, même sans cookies, en ajoutant des entrées au cache d'authentification HTTP à l’aide d’informations d’identification incorporées dans les URL.

Cette stratégie est destinée à fournir aux entreprises, en fonction du comportement hérité, une possibilité de mettre à jour leurs procédures de connexion et elle sera supprimée à l’avenir.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: GloballyScopeHTTPAuthCacheEnabled
  - Nom de la stratégie de groupe: Activer le cache d'autorisation HTTP globalement étendu
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: GloballyScopeHTTPAuthCacheEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: GloballyScopeHTTPAuthCacheEnabled
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### GoToIntranetSiteForSingleWordEntryInAddressBar
  #### Force la navigation directe sur un site intranet au lieu de rechercher des entrées à mots uniques dans la barre d’adresses
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 78 ou version ultérieure

  #### Description
  Si vous activez cette stratégie, le premier résultat de la suggestion automatique dans la liste de suggestions de la barre d’adresses navigue vers les sites intranet si le texte entré dans la barre d’adresses est un mot unique sans ponctuation.

La navigation par défaut lors de la saisie d’un mot unique sans ponctuation effectue une navigation vers un site intranet correspondant au texte entré.

Si vous activez cette stratégie, le deuxième résultat de la suggestion automatique dans la liste de suggestions de la barre d’adresses mène à une recherche sur le web exactement telle qu’elle a été entrée, à condition que ce texte ne comporte qu’un seul mot sans ponctuation. Le moteur de recherche par défaut est utilisé, sauf si une stratégie empêchant la recherche sur le web a également été activée.

L'activation de cette stratégie peut avoir deux effets :

La navigation vers les sites en réponse à des requêtes avec un seul mot se concentrant sur un seul élément de l'historique n'apparaît plus. Au lieu de cela, le navigateur tente de naviguer vers des sites internes qui n'existent peut-être plus dans le réseau intranet d'une organisation. Cette action génère une erreur 404

.      Les termes de recherche populaires à mot unique nécessitent une sélection manuelle des suggestions de recherche pour mener une recherche de manière correcte.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Nom de la stratégie de groupe: Force la navigation directe sur un site intranet au lieu de rechercher des entrées à mots uniques dans la barre d’adresses
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### HSTSPolicyBypassList
  #### Configurez la liste des noms qui vont contourner la vérification de stratégie HSTS
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 79 ou version ultérieure

  #### Description
  Les noms d’hôte spécifiés dans cette liste seront dispensés de la vérification de stratégie HSTS qui pourrait éventuellement mettre à niveau les demandes de « http:// » vers « https:// ». Seuls les noms d’hôte en une seule partie sont autorisés dans cette stratégie. Les noms d’hôte doivent être au format canonique. Toutes les IDN doivent être convertis au format d'étiquette A et toutes les lettres ASCII doivent être en minuscule. Cette stratégie ne s’applique qu’aux noms d’hôte spécifiques indiqués ; elle ne s’applique pas aux sous-domaines des noms de la liste.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: HSTSPolicyBypassList
  - Nom de la stratégie de groupe: Configurez la liste des noms qui vont contourner la vérification de stratégie HSTS
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList\1 = "meet"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: HSTSPolicyBypassList
  - Exemple de valeur :
``` xml
<array>
  <string>meet</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### HardwareAccelerationModeEnabled
  #### Utiliser l’accélération matérielle (si disponible)
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifiez s'il convient d'utiliser l’accélération matérielle, si elle est disponible. Si vous activez cette stratégie ou si vous ne la configurez pas, l’accélération matérielle est activée, sauf si une fonctionnalité GPU est explicitement bloquée.

Si vous désactivez cette stratégie, l’accélération matérielle est désactivée.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: HardwareAccelerationModeEnabled
  - Nom de la stratégie de groupe: Utiliser l’accélération matérielle (si disponible)
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: HardwareAccelerationModeEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: HardwareAccelerationModeEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### HideFirstRunExperience
  #### Masquer l’expérience de première exécution et l’écran de démarrage
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 80 ou version ultérieure

  #### Description
  Si vous activez cette stratégie, l’expérience de première exécution et l’écran de démarrage ne sont pas affichés aux utilisateurs lorsqu’ils exécutent Microsoft Edge pour la première fois.

Pour les options de configuration affichées dans l’expérience de première exécution, le navigateur prend par défaut les valeurs suivantes :

- Sous le nouvel onglet, le type de flux est défini sur MSN Actualité et la mise en page sur Source d'inspiration.

- L’utilisateur est toujours connecté automatiquement à Microsoft Edge si le compte Windows est de type Azure AD ou MSA.

- La synchronisation n'est pas activée par défaut et les utilisateurs peuvent activer la synchronisation à partir des paramètres de synchronisation.

 Si vous désactivez cette stratégie ou si vous ne la configurez pas, l’expérience de première exécution et l’écran de démarrage s’affichent.

Remarque : les options de configuration spécifiques qui s’affichent à l’utilisateur lors de l'expérience de première utilisation peuvent également être gérées à l’aide d’autres stratégies spécifiques. Vous pouvez utiliser la stratégie HideFirstRunExperience en association avec ces stratégies pour configurer une expérience de navigateur spécifique sur vos appareils gérés. Voici quelques-unes de ces autres stratégies :

- [AutoImportAtFirstRun](#autoimportatfirstrun)

- [NewTabPageLocation](#newtabpagelocation)

- [NewTabPageSetFeedType](#newtabpagesetfeedtype)

- [SyncDisabled](#syncdisabled)

- [BrowserSignin](#browsersignin)

- [NonRemovableProfileEnabled](#nonremovableprofileenabled)

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: HideFirstRunExperience
  - Nom de la stratégie de groupe: Masquer l’expérience de première exécution et l’écran de démarrage
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: HideFirstRunExperience
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: HideFirstRunExperience
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ImportAutofillFormData
  #### Autoriser l’importation des données du formulaire de remplissage auto
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Permet aux utilisateurs d’importer des données de formulaire de remplissage auto à partir d’un autre navigateur dans Microsoft Edge.

	Si vous activez cette stratégie, l’option d’importation manuelle des données de remplissage auto est automatiquement sélectionnée.

	Si vous désactivez cette stratégie, les données de remplissage auto ne sont pas importées lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement.

Si vous ne configurez pas cette stratégie, les données de remplissage auto sont importées lors de la première exécution et les utilisateurs peuvent choisir d’importer ou non ces données manuellement lors des sessions de navigation ultérieures.

	Vous pouvez définir cette stratégie comme une recommandation. Cela signifie que Microsoft Edge importe les données de remplissage auto lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou désactiver l’option **données de remplissage auto** pendant l’importation manuelle.

**Remarque** : cette stratégie gère actuellement l’importation à partir des navigateurs de Google Chrome (sous Windows 7, 8 et 10 et sous macOS) et de Mozilla Firefox (sur Windows 7, 8 et 10 et sur macOS).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ImportAutofillFormData
  - Nom de la stratégie de groupe: Autoriser l’importation des données du formulaire de remplissage auto
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: ImportAutofillFormData
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ImportAutofillFormData
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ImportBrowserSettings
  #### Autoriser l’importation des paramètres du navigateur
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 78 ou version ultérieure

  #### Description
  Permet aux utilisateurs d’importer les paramètres du navigateur à partir d’un autre navigateur dans Microsoft Edge.

Si vous activez cette stratégie, la case **Paramètres du navigateur** est automatiquement cochée dans la boîte de dialogue **Importer des données du navigateur**.

Si vous désactivez cette stratégie, les paramètres du navigateur ne sont pas importés lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement.

Si vous ne configurez pas cette stratégie, les paramètres du navigateur sont importés lors de la première exécution et les utilisateurs peuvent choisir s’ils souhaitent les importer manuellement lors des sessions de navigation ultérieures.

Vous pouvez également définir cette stratégie comme une recommandation. Cela signifie que Microsoft Edge importe les paramètres lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou désactiver l’option **Paramètres du navigateur** pendant l’importation manuelle.

**Remarque** : cette stratégie gère actuellement l’importation de Google Chrome (sous Windows 7, 8 et 10 et sous macOS).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ImportBrowserSettings
  - Nom de la stratégie de groupe: Autoriser l’importation des paramètres du navigateur
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: ImportBrowserSettings
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ImportBrowserSettings
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ImportCookies
  #### Autoriser l’importation de cookies
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 81 ou version ultérieure

  #### Description
  Permet aux utilisateurs d’importer des cookies à partir d’un autre navigateur dans Microsoft Edge.

Si vous désactivez cette stratégie, les cookies ne sont pas importés lors de la première exécution.

Si vous ne configurez pas cette stratégie, les cookies sont importés lors de la première exécution.

Vous pouvez également définir cette stratégie comme une recommandation. Cela signifie que Microsoft Edge importe les cookies lors de la première exécution.

**Remarque** : cette stratégie gère actuellement l’importation depuis Google Chrome (sous Windows 7, 8 et 10, et sous macOS).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ImportCookies
  - Nom de la stratégie de groupe: Autoriser l’importation de cookies
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: ImportCookies
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ImportCookies
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ImportExtensions
  #### Autoriser l’importation d'extensions
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 81 ou version ultérieure

  #### Description
  Permet aux utilisateurs d’importer des extensions à partir d’un autre navigateur dans Microsoft Edge.

Si vous activez cette stratégie, la case **Extensions** est automatiquement cochée dans la boîte de dialogue **Importer des données du navigateur**.

Si vous désactivez cette stratégie, les extensions ne sont pas importées lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement.

Si vous ne configurez pas cette stratégie, les extensions sont importées lors de la première exécution et les utilisateurs peuvent choisir s’ils souhaitent les importer manuellement lors des sessions de navigation ultérieures.

Vous pouvez également définir cette stratégie comme une recommandation. Cela signifie que Microsoft Edge importe les extensions lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou désactiver l’option **favoris** pendant l’importation manuelle.

**Remarque** : cette stratégie ne prend actuellement en charge que l’importation à partir de Google Chrome (sous Windows 7, 8 et 10, et sous macOS).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ImportExtensions
  - Nom de la stratégie de groupe: Autoriser l’importation d'extensions
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: ImportExtensions
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ImportExtensions
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ImportFavorites
  #### Autoriser l’importation des favoris
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Permet aux utilisateurs d’importer les favoris à partir d’un autre navigateur dans Microsoft Edge.

Si vous activez cette stratégie, la case à cocher **Favoris** est automatiquement activée dans la boîte de dialogue **Importer des données du navigateur**.

Si vous désactivez cette stratégie, les favoris ne sont pas importés lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement.

Si vous ne configurez pas cette stratégie, les favoris sont importés lors de la première exécution et les utilisateurs peuvent décider de les importer manuellement lors des sessions de navigation ultérieures.

Vous pouvez également définir cette stratégie comme une recommandation. Cela signifie que Microsoft Edge importe les favoris lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou désactiver l’option **Favoris** pendant l’importation manuelle.

**Remarque** : cette stratégie gère actuellement l’importation à partir des navigateurs Internet Explorer (sous Windows 7, 8 et 10), de Google Chrome (sous Windows 7, 8 et 10, et sur macOS), Mozilla Firefox (sous Windows 7, 8 et 10 et macOS) et Apple Safari (sous macOS).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ImportFavorites
  - Nom de la stratégie de groupe: Autoriser l’importation des favoris
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: ImportFavorites
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ImportFavorites
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ImportHistory
  #### Autoriser l’importation de l’historique de navigation
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Permet aux utilisateurs d’importer leur historique de navigation à partir d’un autre navigateur dans Microsoft Edge.

Si vous activez cette stratégie, la case à cocher **Historique de navigation** est automatiquement activée dans la boîte de dialogue **Importer des données du navigateur**.

Si vous désactivez cette stratégie, les données de l’historique de navigation ne sont pas importées lors de la première exécution et les utilisateurs ne peuvent pas importer ces données manuellement.

Si vous ne configurez pas cette stratégie, les données de l’historique de navigation sont importées lors de la première exécution et les utilisateurs peuvent décider de les importer manuellement lors des sessions de navigation ultérieures.

Vous pouvez également définir cette stratégie comme une recommandation. Cela signifie que Microsoft Edge importe l’historique de navigation lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou désactiver l’option **Historique** pendant l’importation manuelle.

**Remarque** : cette stratégie gère actuellement l’importation à partir des navigateurs Internet Explorer (sous Windows 7, 8 et 10), de Google Chrome (sous Windows 7, 8 et 10, et sur macOS), Mozilla Firefox (sous Windows 7, 8 et 10 et macOS) et Apple Safari (macOS).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ImportHistory
  - Nom de la stratégie de groupe: Autoriser l’importation de l’historique de navigation
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: ImportHistory
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ImportHistory
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ImportHomepage
  #### Autoriser l’importation des paramètres de la page d’accueil
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Permet aux utilisateurs d’importer leur paramètre de page d’accueil à partir d’un autre navigateur dans Microsoft Edge.

Si vous activez cette stratégie, l’option d’importation manuelle du paramètre de page d’accueil est automatiquement sélectionnée.

Si vous désactivez cette stratégie, le paramètre de la page d’accueil n’est pas importé lors de la première exécution et les utilisateurs ne peuvent pas l’importer manuellement.

Si vous ne configurez pas cette stratégie, la page d’accueil est importée lors de la première exécution et les utilisateurs peuvent choisir d’importer ou non ces données manuellement lors des sessions de navigation ultérieures.

Vous pouvez définir cette stratégie comme une recommandation. Cela signifie que Microsoft Edge importe le paramètre de page d’accueil lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou désactiver l’option **page d’accueil** pendant l’importation manuelle.

**Remarque** : cette stratégie gère actuellement l’importation à partir d’Internet Explorer (sous Windows 7, 8 et 10).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ImportHomepage
  - Nom de la stratégie de groupe: Autoriser l’importation des paramètres de la page d’accueil
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ImportHomepage
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ImportHomepage
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ImportOpenTabs
  #### Autoriser l’importation des onglets ouverts
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 79 ou version ultérieure

  #### Description
  Permet aux utilisateurs d’importer les onglets ouverts et épinglés à partir d’un autre navigateur dans Microsoft Edge.

Si vous activez cette stratégie, la case **Onglets ouverts** est automatiquement cochée dans la boîte de dialogue **Importer des données du navigateur**.

Si vous désactivez cette stratégie, les onglets ouverts ne sont pas importés lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement.

Si vous ne configurez pas cette stratégie, les onglets ouverts sont importés lors de la première exécution et les utilisateurs peuvent choisir s’ils souhaitent les importer manuellement lors des sessions de navigation ultérieures.

Vous pouvez également définir cette stratégie comme une recommandation. Cela signifie que Microsoft Edge importe les onglets ouverts lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou désactiver l’option **Onglets ouverts** pendant l’importation manuelle.

**Remarque** : cette stratégie ne prend actuellement en charge que l’importation à partir de Google Chrome (sous Windows 7, 8 et 10 et sous macOS).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ImportOpenTabs
  - Nom de la stratégie de groupe: Autoriser l’importation des onglets ouverts
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: ImportOpenTabs
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ImportOpenTabs
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ImportPaymentInfo
  #### Autoriser l’importation des infos de paiement
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Autorise les utilisateurs à importer des infos de paiement à partir d’un autre navigateur dans Microsoft Edge.

Si vous activez cette stratégie, la case à cocher **infos de paiement * * est automatiquement activée dans la boîte de dialogue **Importer les données du navigateur**.

Si vous désactivez cette stratégie, les infos de paiement ne sont pas importées lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement.

Si vous ne configurez pas cette stratégie, les infos de paiement sont importées lors de la première exécution et les utilisateurs peuvent décider de les importer manuellement lors des sessions de navigation ultérieures.

Vous pouvez également définir cette stratégie comme une recommandation. Cela signifie que Microsoft Edge importe les infos de paiement lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou désélectionner l’option **infos de paiement** pendant l’importation manuelle.

**Remarque :** cette stratégie gère actuellement l’importation à partir de Google Chrome (sous Windows 7, 8 et 10 et sous macOS).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ImportPaymentInfo
  - Nom de la stratégie de groupe: Autoriser l’importation des infos de paiement
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: ImportPaymentInfo
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ImportPaymentInfo
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ImportSavedPasswords
  #### Autoriser l’importation des mots de passe enregistrés
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Permet aux utilisateurs d’importer les mots de passe enregistrés à partir d’un autre navigateur dans Microsoft Edge.

	Si vous activez cette stratégie, l’option d’importation manuelle des mots de passe enregistrés est automatiquement sélectionnée.

	Si vous désactivez cette stratégie, les mots de passe enregistrés ne sont pas importés lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement.

	Si vous ne configurez pas cette stratégie, les mots de passe sont importés lors de la première exécution et les utilisateurs peuvent choisir s’ils souhaitent les importer manuellement lors des sessions de navigation ultérieures.

	Vous pouvez définir cette stratégie comme une recommandation. Cela signifie que Microsoft Edge importe les mots de passe lors de la première exécution, mais les utilisateurs peuvent activer ou désactiver l’option **mots de passe** pendant l’importation manuelle.

	**Remarque** : Cette stratégie gère actuellement l’importation à partir des navigateurs d’Internet Explorer (sous Windows 7, 8 et 10), de Google Chrome (sous Windows 7, 8 et 10 et sur macOS) et de Mozilla Firefox (sur Windows 7,8 et 10 et sur macOS).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ImportSavedPasswords
  - Nom de la stratégie de groupe: Autoriser l’importation des mots de passe enregistrés
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: ImportSavedPasswords
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ImportSavedPasswords
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ImportSearchEngine
  #### Autoriser l’importation des paramètres du moteur de recherche
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Permet aux utilisateurs d’importer les paramètres du moteur de recherche à partir d’un autre navigateur dans Microsoft Edge.

Si vous activez cette stratégie, l’option permettant d’importer les paramètres du moteur de recherche est automatiquement sélectionnée.

Si vous désactivez cette stratégie, les paramètres du moteur de recherche ne sont pas importés lors de la première exécution et les utilisateurs ne peuvent pas les importer manuellement.

Si vous ne configurez pas cette stratégie, les paramètres du moteur de recherche sont importés lors de la première exécution et les utilisateurs peuvent choisir d’importer ou non ces données manuellement lors des sessions de navigation ultérieures.

	Vous pouvez définir cette stratégie comme une recommandation. Cela signifie que Microsoft Edge importe les paramètres du moteur de recherche lors de la première exécution, mais que les utilisateurs peuvent sélectionner ou désactiver l’option **moteur de recherche** pendant l’importation manuelle.

**Remarque** : cette stratégie gère actuellement l’importation à partir d’Internet Explorer (sous Windows 7, 8 et 10).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ImportSearchEngine
  - Nom de la stratégie de groupe: Autoriser l’importation des paramètres du moteur de recherche
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: ImportSearchEngine
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ImportSearchEngine
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ImportShortcuts
  #### Autoriser l’importation des raccourcis
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 81 ou version ultérieure

  #### Description
  Permet aux utilisateurs d’importer les raccourcis à partir d’un autre navigateur dans Microsoft Edge.

Si vous désactivez cette stratégie, les raccourcis ne sont pas importés lors de la première exécution

.        Si vous ne configurez pas cette stratégie, les raccourcis sont importés lors de la première exécution.

Vous pouvez également définir cette stratégie comme une recommandation. Cela signifie que Microsoft Edge importe les raccourcis lors de la première exécution.

**Remarque** : cette stratégie gère actuellement l’importation depuis Google Chrome (sous Windows 7, 8 et 10 et sous macOS).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ImportShortcuts
  - Nom de la stratégie de groupe: Autoriser l’importation des raccourcis
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: ImportShortcuts
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ImportShortcuts
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### InPrivateModeAvailability
  #### Configurer la disponibilité du mode InPrivate
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifie si l’utilisateur peut ouvrir des pages en mode InPrivate dans Microsoft Edge.

Si vous ne configurez cette stratégie ou si vous la définissez sur « Enabled », les utilisateurs peuvent ouvrir des pages en mode InPrivate.

 Définissez cette stratégie sur « Disabled » pour empêcher les utilisateurs d’utiliser le mode InPrivate.

 Définissez cette stratégie sur « Forced » pour toujours utiliser le mode InPrivate.

Mappage des options de stratégie :

* Enabled (0) = Mode InPrivate disponible

* Disabled (1) = Mode InPrivate désactivé

* Forced (2) = Mode InPrivate forcé

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: InPrivateModeAvailability
  - Nom de la stratégie de groupe: Configurer la disponibilité du mode InPrivate
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: InPrivateModeAvailability
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: InPrivateModeAvailability
  - Exemple de valeur :
``` xml
<integer>1</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### InsecureFormsWarningsEnabled
  #### Activer les avertissements pour les formulaires non sécurisés
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Cette stratégie contrôle la gestion des formulaires non sécurisés (formulaires envoyés via HTTP), incorporés dans des sites sécurisés (HTTPs) dans le navigateur.
Si vous activez cette stratégie ou si vous ne la définissez pas, un avertissement s’affiche sur la page entière lorsqu’un formulaire non sécurisé est envoyé. De plus, une bulle d’avertissement s’affiche en regard des champs de formulaire lorsqu’ils sont sélectionnés, et la saisie automatique est désactivée pour ces formulaires.
Si vous désactivez cette stratégie, les avertissements ne s’affichent pas pour les formulaires non sécurisés et la saisie automatique fonctionne normalement.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: InsecureFormsWarningsEnabled
  - Nom de la stratégie de groupe: Activer les avertissements pour les formulaires non sécurisés
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: InsecureFormsWarningsEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: InsecureFormsWarningsEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### IntensiveWakeUpThrottlingEnabled
  #### Contrôler la fonctionnalité IntensiveWakeUpThrottling
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 85 ou version ultérieure

  #### Description
  Lorsque la fonctionnalité de IntensiveWakeUpThrottling est activée, les chronométrages JavaScript dans les onglets d’arrière-plan sont considérablement accélérés et fusionnés, et ne s’exécutent pas plus d’une fois par minute après qu’une page ait été mise en page en arrière-plan pendant 5 minutes ou plus.

Il s’agit d’une fonctionnalité conforme aux normes web, mais elle risque de rompre la fonctionnalité de certains sites web en forçant certaines actions à être différées de quelques minutes. Cependant, l’utilisation de la CPU et de la batterie entraîne une économie considérable. Pour plus d’informations, consultez https://bit.ly/30b1XR4.

  Si vous activez cette stratégie, la fonctionnalité est activée et les utilisateurs ne peuvent pas modifier ce paramètre.
  Si vous désactivez cette stratégie, la fonctionnalité sera désactivée et les utilisateurs ne pourront pas modifier ce paramètre.
  Si vous ne configurez pas cette stratégie, la fonctionnalité est contrôlée par sa propre logique interne. Les utilisateurs peuvent configurer manuellement ce paramètre.

  Notez que la stratégie est appliquée par processus de rendu, avec la valeur la plus récente du paramètre de stratégie en vigueur au démarrage du processus de rendu. Un redémarrage complet est nécessaire pour s’assurer que tous les onglets chargés reçoivent un paramètre de stratégie cohérent. Il est inoffensif pour les processus qui s’exécutent avec différentes valeurs de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: IntensiveWakeUpThrottlingEnabled
  - Nom de la stratégie de groupe: Contrôler la fonctionnalité IntensiveWakeUpThrottling
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: IntensiveWakeUpThrottlingEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: IntensiveWakeUpThrottlingEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### InternetExplorerIntegrationEnhancedHangDetection
  #### Configurez la détection de blocage améliorée pour le mode Internet Explorer
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 84 ou ultérieur

  #### Description
  La détection de blocage améliorée est une approche plus granulaire de la détection de pages web bloquées en mode Internet Explorer, comparée à celle utiliser par la version autonome d’Internet Explorer. Lorsqu’une page web suspendue est détectée, le navigateur applique une atténuation pour empêcher le blocage du reste du navigateur.

Ce paramètre vous permet de configurer l’utilisation de la détection de blocage améliorée au cas où vous rencontriez des problèmes incompatibles avec l’un de vos sites web. Il est recommandé de désactiver cette stratégie uniquement si les notifications telles que « (le site web) ne répond pas » s’affiche en mode Internet Explorer, mais pas dans la version autonome d’Internet Explorer.

Ce paramètre fonctionne conjointement avec :
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) qui est défini sur « IEMode »
et
la stratégie[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) dans laquelle la liste comporte au moins une entrée.

Si vous définissez cette stratégie sur « Enabled » ou si vous ne la configurez pas, les sites web en mode Internet Explorer utilisent la détection de blocage améliorée.

Si vous avez défini cette stratégie sur « Disabled », la détection de blocage améliorée est désactivée et les utilisateurs obtiendront le comportement de détection de blocage d’Internet Explorer.

Si vous souhaitez en savoir plus sur le mode Internet Explorer, rendez-vous sur [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Mappage des options de stratégie :

* Disabled (0) = Détection de blocage améliorée désactivée

* Enabled (1) = Détection de blocage améliorée activée

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: InternetExplorerIntegrationEnhancedHangDetection
  - Nom de la stratégie de groupe: Configurez la détection de blocage améliorée pour le mode Internet Explorer
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: InternetExplorerIntegrationEnhancedHangDetection
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### InternetExplorerIntegrationLevel
  #### Configurer l’intégration d’Internet Explorer
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 77 ou ultérieur

  #### Description
  Pour obtenir des instructions sur la configuration optimale de l’expérience pour Internet Explorer, consultez [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Mappage des options de stratégie :

* None (0) = Aucun(e)

* IEMode (1) = Mode Internet Explorer

* NeedIE (2) = Internet Explorer 11

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: InternetExplorerIntegrationLevel
  - Nom de la stratégie de groupe: Configurer l’intégration d’Internet Explorer
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: InternetExplorerIntegrationLevel
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### InternetExplorerIntegrationSiteList
  #### Configurer la liste des sites en Mode entreprise
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 78 ou ultérieur

  #### Description
  Pour obtenir des instructions sur la configuration optimale de l’expérience pour Internet Explorer, consultez [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: InternetExplorerIntegrationSiteList
  - Nom de la stratégie de groupe: Configurer la liste des sites en Mode entreprise
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: InternetExplorerIntegrationSiteList
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"https://internal.contoso.com/sitelist.xml"
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### InternetExplorerIntegrationSiteRedirect
  #### Spécifier le type de comportement des navigations « entre les pages » vers des sites non configurés lorsqu’elles commencent sur des pages en mode Internet Explorer
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 81 ou ultérieur

  #### Description
  Une navigation « entre les pages » est lancée à partir d’un lien, d’un script ou d’un formulaire de la page active. Il peut également s’agir d’une redirection côté serveur d’une tentative de navigation « entre les pages » précédente. Inversement, un utilisateur peut démarrer une navigation qui n’est pas « entre les pages » et qui est indépendante de la page active de plusieurs façons en utilisant les contrôles du navigateur. Par exemple, à l’aide de la barre d’adresse, du bouton Retour ou d’un lien favori.

Ce paramètre vous permet de spécifier si les navigations à partir de pages chargées en mode Internet Explorer sur des sites non configurés (qui ne sont pas configurés dans la liste de sites en mode Entreprise) basculent vers Microsoft Edge ou restent en mode Internet Explorer.

Ce paramètre fonctionne conjointement avec :
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) est défini sur « mode Internet Explorer »
et
la stratégie[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) dans laquelle la liste comporte au moins une entrée.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, seuls les sites configurés pour s’ouvrir en mode Internet Explorer s’ouvrent dans ce mode. Les sites non configurés pour être ouverts en mode Internet Explorer sont redirigés vers Microsoft Edge.

Si vous définissez cette stratégie sur Default, seuls les sites configurés pour s’ouvrir en mode Internet Explorer s’ouvrent dans ce mode. Les sites non configurés pour être ouverts en mode Internet Explorer sont redirigés vers Microsoft Edge.

Si vous définissez cette stratégie sur « AutomaticNavigationsOnly », vous obtenez l'expérience par défaut, sauf que toutes les navigations automatiques (telles que les redirections 302) vers des sites non configurés restent en mode Internet Explorer.

Si vous définissez cette stratégie sur « AllInPageNavigations », toutes les navigations à partir des pages chargées en mode IE vers des sites non configurés restent en mode Internet Explorer (le moins recommandé).

Pour en savoir plus sur le mode Internet Explorer, voir [https://go.microsoft.com/fwlink/?linkid=2105106](https://go.microsoft.com/fwlink/?linkid=2105106)

Mappage des options de stratégie :

* Default (0) = Par défaut

* AutomaticNavigationsOnly (1) = Conserver uniquement les navigations automatiques en mode Internet Explorer

* AllInPageNavigations (2) = Conserver toutes les navigations entre les pages en mode Internet Explorer

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: InternetExplorerIntegrationSiteRedirect
  - Nom de la stratégie de groupe: Spécifier le type de comportement des navigations « entre les pages » vers des sites non configurés lorsqu’elles commencent sur des pages en mode Internet Explorer
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: InternetExplorerIntegrationSiteRedirect
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### InternetExplorerIntegrationTestingAllowed
  #### Autoriser le test du mode Internet Explorer
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 86 ou ultérieur

  #### Description
  Cette stratégie remplace la stratégie d’indicateur de test en mode Internet Explorer. Elle permet aux utilisateurs d’ouvrir un onglet mode Internet Explorer à partir de l’option de menu de l’interface utilisateur.

Ce paramètre fonctionne conjointement avec :
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) est définie sur « IEMode »
et
[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) la stratégie  pour laquelle la liste comporte au moins une entrée.

Si vous activez cette stratégie, les utilisateurs peuvent ouvrir l’onglet mode Internet Explorer à partir de l’option d’interface utilisateur et naviguer dans le site actif vers un site en mode IE.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas afficher l’option interface utilisateur directement dans le menu.

Si vous ne configurez pas cette stratégie, vous pouvez définir manuellement l’indicateur de test de mode Internet Explorer.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: InternetExplorerIntegrationTestingAllowed
  - Nom de la stratégie de groupe: Autoriser le test du mode Internet Explorer
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: InternetExplorerIntegrationTestingAllowed
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### IsolateOrigins
  #### Activer l’isolation de site pour des origines spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifiez les origines à exécuter dans une isolation, dans leur propre processus.
Cette stratégie isole également les origines nommées par sous-domaine. Par exemple, la définition de https://contoso.com/ provoque l'isolation de https://foo.contoso.com/ dans le cadre du site https://contoso.com/.
Si la stratégie est activée, chacune des origines nommées dans une liste séparée par des virgules s’exécute dans son propre processus.
Si vous désactivez cette stratégie, les fonctionnalités « IsolateOrigins » et « SitePerProcess » sont désactivées. Les utilisateurs peuvent toujours activer la stratégie « IsolateOrigins » manuellement, via les indicateurs de ligne de commande.
Si vous ne configurez pas la stratégie, l’utilisateur peut modifier ce paramètre.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: IsolateOrigins
  - Nom de la stratégie de groupe: Activer l’isolation de site pour des origines spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: IsolateOrigins
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"https://contoso.com/,https://fabrikam.com/"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: IsolateOrigins
  - Exemple de valeur :
``` xml
<string>https://contoso.com/,https://fabrikam.com/</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### LocalProvidersEnabled
  #### Autoriser les suggestions des fournisseurs locaux
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 83 ou version ultérieure

  #### Description
  Autorisez les suggestions des fournisseurs de suggestion sur l’appareil (fournisseurs locaux), par exemple, les favoris et l’historique de navigation, dans la barre d’adresse et dans la liste de suggestions automatiques de Microsoft Edge.

Si vous activez cette stratégie, les suggestions des fournisseurs locaux sont utilisées.

Si vous désactivez cette stratégie, les suggestions des fournisseurs locaux ne sont jamais utilisées. L’historique et les suggestions de favoris locaux n’apparaissent pas.

Si vous ne configurez pas cette stratégie, les suggestions des fournisseurs locaux sont autorisées, mais l’utilisateur peut modifier ce paramètre à l’aide du bouton bascule.

Notez que certaines fonctionnalités peuvent ne pas être disponibles si une stratégie de désactivation de cette fonctionnalité a été appliquée. Par exemple, les suggestions d’historique de navigation ne sont pas disponibles si vous activez la stratégie [SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled).

Cette stratégie nécessite un redémarrage du navigateur pour finaliser l’application.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: LocalProvidersEnabled
  - Nom de la stratégie de groupe: Autoriser les suggestions des fournisseurs locaux
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: LocalProvidersEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: LocalProvidersEnabled
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ManagedFavorites
  #### Configurer les favoris
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Configurer une liste de favoris gérés.

	La stratégie crée une liste de favoris. Chaque favori contient les clés « nom » et « URL », qui contiennent le nom du favori et sa cible. Vous pouvez configurer un sous-dossier en définissant un favori sans clé « URL », mais avec une clé supplémentaire « enfants » qui contient une liste de favoris définie ci-dessus (certains peuvent être de nouveau des dossiers). Microsoft Edge modifie les URL incomplètes comme si elles étaient envoyées par le biais de la barre d'adresses, par exemple, « microsoft.com » devient « https://microsoft.com/ ».

	Ces favoris sont placés dans un dossier qui ne peut pas être modifié par l’utilisateur (mais l’utilisateur peut choisir de le masquer dans la barre des favoris). Par défaut, le nom du dossier est « Favoris gérés », mais vous pouvez le modifier en ajoutant à la liste des favoris un dictionnaire contenant la clé « toplevel_name » avec le nom de dossier souhaité comme valeur.

	Les favoris gérés ne sont pas synchronisés avec le compte d’utilisateur et ne peuvent pas être modifiés par des extensions.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Dictionnaire

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ManagedFavorites
  - Nom de la stratégie de groupe: Configurer les favoris
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ManagedFavorites
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
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


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ManagedFavorites
  - Exemple de valeur :
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
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ManagedSearchEngines
  #### Gérer les moteurs de recherche
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Il vous permet de configurer une liste de 10moteurs de recherche maximum, dont l’un d’entre eux doit être défini comme moteur de recherche par défaut.
Il n’est pas nécessaire de spécifier le codage. À partir de Microsoft Edge80, les paramètres suggest_url et image_search_url sont facultatifs. Le paramètre facultatif, image_search_post_params (qui est constitué de paires de noms/valeurs séparées par des virgules) est disponible à partir de Microsoft Edge 80.

À partir de Microsoft Edge 83, vous pouvez activer la découverte de moteur de recherche avec le paramètre facultatif allow_search_engine_discovery. Ce paramètre doit être le premier élément de la liste. Si allow_search_engine_discovery n'est pas spécifié, la découverte de moteur de recherche est désactivée par défaut. À partir de Microsoft Edge 84, vous pouvez définir cette stratégie comme une stratégie recommandée pour permettre la découverte de fournisseurs de services de recherche. Vous n'avez pas besoin d'ajouter le paramètre optionnel allow_search_engine_discovery

Si vous activez cette stratégie, les utilisateurs ne peuvent pas ajouter, supprimer ou modifier un moteur de recherche dans la liste. Les utilisateurs peuvent définir n’importe quel moteur de recherche dans la liste en tant que moteur de recherche par défaut.

Si vous désactivez ou ne configurez pas cette stratégie, les utilisateurs peuvent modifier la liste des moteurs de recherche s'ils le souhaitent.

Si la stratégie [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) est définie, cette stratégie (ManagedSearchEngines) est ignorée. L’utilisateur doit redémarrer son navigateur pour que l’application de cette stratégie soit prise en compte.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Dictionnaire

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ManagedSearchEngines
  - Nom de la stratégie de groupe: Gérer les moteurs de recherche
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: ManagedSearchEngines
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
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


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ManagedSearchEngines
  - Exemple de valeur :
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
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### MaxConnectionsPerProxy
  #### Nombre maximal de connexions simultanées au serveur proxy
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifie le nombre maximal de connexions simultanées au serveur proxy.

Certains serveurs proxy ne peuvent pas gérer un nombre élevé de connexions simultanées par client. Vous pouvez résoudre ce problème en définissant cette stratégie sur une valeur inférieure.

La valeur de cette stratégie doit être inférieure à 100 et supérieure à 6. La valeur par défaut est 32.

Certaines applications web sont connues pour consommer de nombreuses connexions lors du blocage d'opérations GET. Diminuer le nombre maximal de connexions à une valeur inférieure à 32 peut bloquer les réseaux du navigateur en cas d'ouverture d'un trop grand nombre de ce type d’applications web.

Si vous ne configurez pas cette stratégie, la valeur par défaut (32) est utilisée.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: MaxConnectionsPerProxy
  - Nom de la stratégie de groupe: Nombre maximal de connexions simultanées au serveur proxy
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: MaxConnectionsPerProxy
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000020
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: MaxConnectionsPerProxy
  - Exemple de valeur :
``` xml
<integer>32</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### MediaRouterCastAllowAllIPs
  #### Autoriser Google Cast à se connecter aux appareils Cast sur toutes les adresses IP
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Activez cette stratégie pour permettre à Google Cast de se connecter à tous les appareils Cast sur toutes les adresses IP, sans se limiter aux adresses privées RFC1918/RFC4193.

Désactivez cette stratégie pour limiter Google Cast aux appareils Cast sur les adresses privées RFC1918/RFC4193.

Si vous ne configurez pas cette stratégie, Google Cast se connecte aux appareils Cast uniquement sur les adresses privées RFC1918/RFC4193, à moins que vous n'activiez la fonctionnalité CastAllowAllIPs.

Si la stratégie [EnableMediaRouter](#enablemediarouter) est désactivée, cette stratégie n'a aucun effet.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: MediaRouterCastAllowAllIPs
  - Nom de la stratégie de groupe: Autoriser Google Cast à se connecter aux appareils Cast sur toutes les adresses IP
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: MediaRouterCastAllowAllIPs
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: MediaRouterCastAllowAllIPs
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### MetricsReportingEnabled
  #### Activer l’utilisation et les rapports de données liées à l’incident (déconseillé)
  >DÉCONSEILLÉ : cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans Microsoft Edge 89. Cette stratégie est remplacée par la nouvelle stratégie : [DiagnosticData](#diagnosticdata)pour Windows 7, Windows 8 et macOS. Cette stratégie est remplacée par la fonctionnalité de télémétrie sur Win 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

Cette stratégie permet de signaler les informations d’utilisation et de blocage relatives à Microsoft Edge à Microsoft.

Activer cette stratégie pour envoyer des rapports sur l’utilisation et les données liées à un blocage à Microsoft. Désactiver cette stratégie pour ne pas envoyer les données à Microsoft. Dans les deux cas, les utilisateurs ne peuvent pas modifier le paramètre ou le remplacer.

Sur Windows 10, si vous ne configurez pas cette stratégie, Microsoft Edge est configuré par défaut sur les données de diagnostic de Windows. Si vous activez cette stratégie, Microsoft Edge enverra uniquement les données d’utilisation si le paramètre de données de diagnostic Windows est défini sur Amélioré ou Complet. Si vous désactivez cette stratégie, Microsoft Edge n’enverra pas les données d’utilisation. Les données liées au blocage sont envoyées sur la base du paramètre de données de diagnostic Windows. En savoir plus sur les paramètres des données de diagnostic Windows sur [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

Sur Windows 7, Windows 8 et macOS, cette stratégie contrôle l’envoi des données d’utilisation et de blocage. Si vous ne configurez pas cette stratégie, Microsoft Edge aura par défaut la préférence de l’utilisateur.

Pour activer cette stratégie,[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) doit être configuré sur Activée. Si [MetricsReportingEnabled](#metricsreportingenabled) ou [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) n’est pas configuré ou désactivé, ces données ne sont pas envoyées à Microsoft.

Cette stratégie est disponible uniquement sur les instances Windows qui sont jointes à un domaine de Microsoft Active Directory, Windows 10 professionnel ou les instances d’entreprise qui sont inscrites à la gestion des appareils, ou les instances macOS qui sont gérées via la gestion des périphériques mobiles ou qui sont jointes à un domaine via MCX.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: MetricsReportingEnabled
  - Nom de la stratégie de groupe: Activer l’utilisation et les rapports de données liées à l’incident (déconseillé)
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: MetricsReportingEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: MetricsReportingEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### NativeWindowOcclusionEnabled
  #### Activer l’occlusion de fenêtre native
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 84 ou ultérieur

  #### Description
  Active l’occlusion de fenêtres natives dans Microsoft Edge.

Si vous activez ce paramètre, Microsoft Edge détecte la dissimulation d’une fenêtre par d’autres fenêtres et suspend la tâche de remplissage de pixels afin de réduire la consommation du processeur et d’énergie.

Si vous désactivez ce paramètre, Microsoft Edge ne détecte pas la dissimulation d’une fenêtres par d’autres fenêtres.

Si cette stratégie n’est pas configurée, la détection de fenêtre masquée est activée.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: NativeWindowOcclusionEnabled
  - Nom de la stratégie de groupe: Activer l’occlusion de fenêtre native
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: NativeWindowOcclusionEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### NavigationDelayForInitialSiteListDownloadTimeout
  #### Définition d’un délai d’expiration pour la navigation d’onglets de la Liste des sites en Mode entreprise
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 84 ou ultérieur

  #### Description
  Vous permet de spécifier un délai d’expiration (en secondes) pour les onglets Microsoft Edge en attente de navigation jusqu’à ce que le navigateur ait téléchargé la Liste des sites en Mode entreprise initiale.

Ce paramètre fonctionne en association avec:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) est défini sur « Mode Internet Explorer »
et
la stratégie de [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) dans laquelle la liste comporte au moins une entrée
 et
[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload) a la valeur «Toutes les navigations éligibles» (1).

 Les onglets n’attendent pas au-delà de ce délai d’expiration pour le téléchargement de la Liste des sites en Mode entreprise. Si le navigateur n’a pas terminé le téléchargement de la Liste des sites en Mode entreprise à l’expiration du délai d’expiration, les onglets de Microsoft Edge continuent leur navigation. La valeur du délai d’expiration ne doit pas excéder 20 secondes et être inférieure à 1 seconde.

 Si vous avez défini le délai d’expiration dans cette stratégie sur une valeur supérieure à la valeur par défaut de 2 secondes, une barre d’informations s’affiche à l’utilisateur après 2 secondes. La barre d’informations contient un bouton permettant à l’utilisateur d’arrêter d’attendre l’exécution du téléchargement de la Liste des sites en Mode entreprise.

 Si vous ne configurez pas cette stratégie, le délai d’expiration par défaut de 2 secondes est utilisé. Cette valeur par défaut est susceptible d’être modifiée à l’avenir.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: NavigationDelayForInitialSiteListDownloadTimeout
  - Nom de la stratégie de groupe: Définition d’un délai d’expiration pour la navigation d’onglets de la Liste des sites en Mode entreprise
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: NavigationDelayForInitialSiteListDownloadTimeout
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x0000000a
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### NetworkPredictionOptions
  #### Activer la prédiction réseau
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Active les prédictions réseau et empêche les utilisateurs de modifier ce paramètre.

Contrôle la prérécupération DNS, la préconnexion TCP et SSL et le prérendu des pages web.

Si vous ne configurez pas cette stratégie, les prédictions réseau sont activées, mais l’utilisateur peut modifier ce comportement.

Mappage des options de stratégie :

* NetworkPredictionAlways (0) = Prévoir des actions réseau sur une connexion réseau

* NetworkPredictionWifiOnly (1) = Non pris en charge, si cette valeur est utilisée, elle est traitée comme si « Prédire les actions réseau sur n'importe quelle connexion réseau » (0) était configuré

* NetworkPredictionNever (2) = Ne pas prédire les actions de réseau sur n’importe quelle connexion réseau

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: NetworkPredictionOptions
  - Nom de la stratégie de groupe: Activer la prédiction réseau
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: NetworkPredictionOptions
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: NetworkPredictionOptions
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### NonRemovableProfileEnabled
  #### Configurer si un utilisateur dispose toujours d’un profil par défaut connecté automatiquement avec son compte professionnel ou scolaire
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 78 ou ultérieur

  #### Description
  Cette stratégie détermine si un utilisateur peut supprimer le profil Microsoft Edge connecté automatiquement dans le compte professionnel ou scolaire d’un utilisateur.

Si vous activez cette stratégie, un profil impossible à supprimer est créé avec le compte professionnel ou scolaire de l’utilisateur sous Windows. Ce profil ne peut pas être déconnecté ni supprimé.

Si vous désactivez cette stratégie ou ne la configurez pas, le profil connecté automatiquement avec le compte professionnel ou scolaire d’un utilisateur sous Windows peut être déconnecté ou supprimé par l’utilisateur.

Si vous souhaitez configurer la connexion du navigateur, utilisez la stratégie [BrowserSignin](#browsersignin).

 Cette stratégie est disponible uniquement sur les instances Windows qui sont jointes à un domaine Microsoft Active Directory, Windows 10 professionnel ou les instances d’entreprise inscrites à la gestion des appareils..

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: NonRemovableProfileEnabled
  - Nom de la stratégie de groupe: Configurer si un utilisateur dispose toujours d’un profil par défaut connecté automatiquement avec son compte professionnel ou scolaire
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: NonRemovableProfileEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### OverrideSecurityRestrictionsOnInsecureOrigin
  #### Contrôler l’application des restrictions de sécurité aux origines non sécurisées
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifie la liste des origines (URL) ou des modèles de nom d’hôte (tels que « *.contoso.com ») pour lesquels des restrictions de sécurité ne s’appliquent pas.

Cette stratégie vous permet de spécifier des origines autorisées pour les applications héritées qui ne peuvent pas déployer TLS ni définir de serveur de gestion intermédiaire pour le développement web interne afin que les développeurs puissent tester les fonctions nécessitant des contextes de sécurité sans devoir déployer TLS sur le serveur de gestion intermédiaire. Cette stratégie empêche également l’origine d'être étiquetée « Non sécurisé » dans l’omnibox.

La définition d’une liste d’URL dans cette stratégie a le même effet que la définition de l’indicateur de ligne de commande « --unsafely-treat-insecure-origin-as-secure » dans une liste d'URL identiques séparées par des virgules. Si vous activez cette stratégie, elle remplace l’indicateur de ligne de commande.

Cette stratégie remplace la stratégie « UnsafelyTreatInsecureOriginAsSecure », le cas échéant.

Pour plus d’informations sur les contextes de sécurité, voir https://www.w3.org/TR/secure-contexts/.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: OverrideSecurityRestrictionsOnInsecureOrigin
  - Nom de la stratégie de groupe: Contrôler l’application des restrictions de sécurité aux origines non sécurisées
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\1 = "http://testserver.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\2 = "*.contoso.com"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: OverrideSecurityRestrictionsOnInsecureOrigin
  - Exemple de valeur :
``` xml
<array>
  <string>http://testserver.contoso.com/</string>
  <string>*.contoso.com</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PaymentMethodQueryEnabled
  #### Autoriser les sites Web à demander des modes de paiement disponibles
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 80 ou version ultérieure

  #### Description
  Permet de déterminer si les sites Web peuvent vérifier si l’utilisateur a enregistré des modes de paiement.

Si vous désactivez cette stratégie, les sites Web qui utilisent les API PaymentRequest.canMakePayment ou PaymentRequest.hasEnrolledInstrument seront informés qu’aucun mode de paiement n’est disponible.

Si vous activez cette stratégie ou si vous ne la définissez pas, les sites Web peuvent vérifier si les modes de paiement de l’utilisateur sont enregistrés.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PaymentMethodQueryEnabled
  - Nom de la stratégie de groupe: Autoriser les sites Web à demander des modes de paiement disponibles
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: PaymentMethodQueryEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PaymentMethodQueryEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PersonalizationReportingEnabled
  #### Autoriser la personnalisation des publicités, de la recherche et des actualités en envoyant un historique de navigation à Microsoft
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 80 ou version ultérieure

  #### Description
  Cette stratégie empêche Microsoft de collecter l’historique de navigation Microsoft Edge d'un utilisateur pour personnaliser la publicité, la recherche, les actualités et d’autres services Microsoft.

Ce paramètre n'est disponible que pour les utilisateurs disposant d’un compte Microsoft. Ce paramètre n’est pas disponible pour les comptes enfants ou les comptes d’entreprise.

Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas modifier ou remplacer le paramètre. Si vous activez cette stratégie ou si vous ne la configurez pas, Microsoft Edge sera par défaut la préférence de l’utilisateur.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PersonalizationReportingEnabled
  - Nom de la stratégie de groupe: Autoriser la personnalisation des publicités, de la recherche et des actualités en envoyant un historique de navigation à Microsoft
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: PersonalizationReportingEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PersonalizationReportingEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PinningWizardAllowed
  #### Autoriser l’Assistant Épingler à la barre des tâches
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 80 ou ultérieur

  #### Description
  Microsoft Edge utilise l’Assistant Épingler à la barre des tâches pour aider les utilisateurs à épingler les sites suggérés dans la barre des tâches. La fonctionnalité d'Assistant Épingler à la barre des tâches est activée par défaut et accessible par l’utilisateur via le menu Paramètres et plus.

Si vous activez cette stratégie ou si vous ne la configurez pas, les utilisateurs peuvent appeler l’Assistant Épingler à la barre des tâches à partir du menu Paramètres et plus. L’Assistant peut également être appelé via le lancement d'un protocole.

Si vous désactivez cette stratégie, l’Assistant Épingler à la barre des tâches est désactivé dans le menu et ne peut pas être appelé via le lancement d'un protocole.

Les paramètres utilisateur permettant d'activer ou de désactiver l’Assistant Épingler à la barre des tâches ne sont pas disponibles.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PinningWizardAllowed
  - Nom de la stratégie de groupe: Autoriser l’Assistant Épingler à la barre des tâches
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: PinningWizardAllowed
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ProactiveAuthEnabled
  #### Activer l’authentification proactive
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Vous permet de configurer l'activation et la désactivation de l'Authentification proactive.

	Si vous activez cette stratégie, Microsoft Edge tente d'authentifier de manière proactive l'utilisateur connecté aux services Microsoft. À intervalles réguliers, Microsoft Edge recherche sur le service en ligne un manifeste mis à jour contenant la configuration régissant ce comportement.

	Si vous désactivez cette stratégie, Microsoft Edge ne tente pas d'authentifier de manière proactive l'utilisateur connecté aux services Microsoft. Microsoft Edge ne recherche pas sur le service en ligne un manifeste mis à jour contenant la configuration régissant ce comportement.

	Si vous ne configurez pas cette stratégie, l'authentification proactive est activée.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ProactiveAuthEnabled
  - Nom de la stratégie de groupe: Activer l’authentification proactive
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ProactiveAuthEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ProactiveAuthEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PromotionalTabsEnabled
  #### Autoriser le contenu promotionnel dans des onglets
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Contrôler la présentation de contenu pédagogique ou promotionnel dans des onglets. Ce paramètre contrôle la présentation des pages d’accueil qui aident les utilisateurs à se connecter à Microsoft Edge, à choisir leur navigateur par défaut ou à en savoir plus sur les fonctionnalités du produit.

	Si vous activez cette stratégie (définie sur true) ou si vous ne la configurez pas, Microsoft Edge peut afficher le contenu dans des onglets pour fournir des informations sur le produit.

	Si vous désactivez (définissez sur false) cette stratégie, Microsoft Edge ne peut pas afficher le contenu dans des onglets aux utilisateurs.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PromotionalTabsEnabled
  - Nom de la stratégie de groupe: Autoriser le contenu promotionnel dans des onglets
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: PromotionalTabsEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PromotionalTabsEnabled
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### PromptForDownloadLocation
  #### Demander où enregistrer les fichiers téléchargés
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez s’il faut demander où enregistrer un fichier avant de le télécharger.

Si vous activez cette stratégie, l’utilisateur est invité à indiquer l'emplacement d’enregistrement de chaque fichier avant le téléchargement. Si vous ne la configurez pas, les fichiers sont enregistrés automatiquement à l’emplacement par défaut, sans demander à l’utilisateur.

Si vous ne configurez pas cette stratégie, l’utilisateur peut modifier ce paramètre.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: PromptForDownloadLocation
  - Nom de la stratégie de groupe: Demander où enregistrer les fichiers téléchargés
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: PromptForDownloadLocation
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: PromptForDownloadLocation
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### QuicAllowed
  #### Autoriser le protocole QUIC
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Permet d’utiliser le protocole QUIC Microsoft Edge.

	Si vous activez cette stratégie ou ne la configurez pas, le protocole QUIC est autorisé.

	Si vous désactivez cette stratégie, le protocole QUIC est bloqué.

	QUIC est un protocole réseau de couche transport qui peut améliorer les performances des applications web qui utilisent TCP.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: QuicAllowed
  - Nom de la stratégie de groupe: Autoriser le protocole QUIC
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: QuicAllowed
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: QuicAllowed
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### RelaunchNotification
  #### Avertir un utilisateur qu’un redémarrage du navigateur est recommandé ou requis pour les mises à jour en attente
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Avertissez les utilisateurs qu’ils doivent redémarrer Microsoft Edge pour appliquer une mise à jour en attente.

Si vous ne configurez pas cette stratégie, Microsoft Edge ajoute une icône de recyclage à l’extrême droite de la barre de menus supérieure pour inviter les utilisateurs à redémarrer le navigateur afin d'appliquer la mise à jour.

Si vous activez cette stratégie et la définissez sur « Recommended », un avertissement périodique informe les utilisateurs qu’un redémarrage est recommandé. Les utilisateurs peuvent ignorer cet avertissement et reporter le redémarrage.

Si vous définissez la stratégie sur « Required » (2), un avertissement périodique informe les utilisateurs que le navigateur sera redémarré automatiquement dès qu’une période de notification est passée. La période par défaut est de sept jours. Vous pouvez configurer cette période avec la stratégie [RelaunchNotificationPeriod](#relaunchnotificationperiod).

La session de l'utilisateur est restaurée au redémarrage du navigateur.

Mappage des options de stratégie :

* Recommended (1) = Recommandé - Afficher une invite périodique à l’utilisateur pour indiquer qu’un redémarrage est recommandé

* Required (2) = Obligatoire - Afficher une invite périodique à l’utilisateur indiquant qu’un redémarrage est nécessaire

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: RelaunchNotification
  - Nom de la stratégie de groupe: Avertir un utilisateur qu’un redémarrage du navigateur est recommandé ou requis pour les mises à jour en attente
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: RelaunchNotification
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: RelaunchNotification
  - Exemple de valeur :
``` xml
<integer>1</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### RelaunchNotificationPeriod
  #### Définir la période pour les notifications de mise à jour
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Vous permet de définir la période de temps, en millisecondes, pendant laquelle les utilisateurs sont avertis que Microsoft Edge doit être relancé pour appliquer une mise à jour en attente.

Au cours de cette période, l’utilisateur sera informé à plusieurs reprises de la nécessité d’une mise à jour. Dans Microsoft Edge le menu de l’application change pour indiquer qu’un redémarrage est nécessaire dès qu’un tiers de la période de notification est écoulé. Cette notification change de couleur une fois que les deux tiers de la période de notification est passée, puis à nouveau lorsque la période de notification complète est passée. Les notifications supplémentaires activées par la stratégie de [RelaunchNotification](#relaunchnotification) suivent le même Planning.

Si cette valeur n’est pas définie, la période par défaut de 604,8 millions millisecondes (une semaine) est utilisée.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: RelaunchNotificationPeriod
  - Nom de la stratégie de groupe: Définir la période pour les notifications de mise à jour
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: RelaunchNotificationPeriod
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x240c8400
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: RelaunchNotificationPeriod
  - Exemple de valeur :
``` xml
<integer>604800000</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### RendererCodeIntegrityEnabled
  #### Activer l’intégrité du code de rendu
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 78 ou ultérieur

  #### Description
  Si cette stratégie est activée ou si elle est laissée non définie, l’intégrité du code de rendu est activée. Cette stratégie ne doit être désactivée que si des problèmes de compatibilité sont rencontrés avec des logiciels tiers qui doivent s’exécuter dans les processus de rendu de Microsoft Edge.

La désactivation de cette stratégie a un effet néfaste sur la sécurité et la stabilité de Microsoft Edge, car le code inconnu et potentiellement hostile est autorisé à se charger dans les processus de rendu de Microsoft Edge.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: RendererCodeIntegrityEnabled
  - Nom de la stratégie de groupe: Activer l’intégrité du code de rendu
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: RendererCodeIntegrityEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### RequireOnlineRevocationChecksForLocalAnchors
  #### Spécifier si des vérifications OCSP/liste de révocation de certificats en ligne sont obligatoires pour les ancres d’approbation locales
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 77 ou ultérieur

  #### Description
  Contrôler si des vérifications de révocation en ligne (vérifications OCSP/liste de révocation de certificats) sont nécessaires. Si Microsoft Edge ne peut pas obtenir d'informations sur le statut de révocation, ces certificats sont considérés comme révoqués (« erreur irrécupérable »).

	Si vous activez cette stratégie, Microsoft Edge exécute toujours la vérification de révocation des certificats de serveur qui ont été validés et sont signés par les certificats d'autorité de certification installés localement.

	Si vous ne configurez pas ou si vous désactivez cette stratégie, Microsoft Edge utilise les paramètres de vérification de révocation en ligne existants.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: RequireOnlineRevocationChecksForLocalAnchors
  - Nom de la stratégie de groupe: Spécifier si des vérifications OCSP/liste de révocation de certificats en ligne sont obligatoires pour les ancres d’approbation locales
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: RequireOnlineRevocationChecksForLocalAnchors
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ResolveNavigationErrorsUseWebService
  #### Activer la résolution des erreurs de navigation à l'aide d'un service web
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Autorise Microsoft Edge à émettre une connexion sans donnée vers un service web pour sonder les réseaux afin de détecter la connectivité, par exemple dans le cas du réseau Wi-Fi d'un hôtel ou d'un aéroport.

Si vous activez cette stratégie, un service web est utilisé pour les tests de connectivité.

Si vous désactivez cette stratégie, Microsoft Edge utilise les API natives pour tenter de résoudre les problèmes de connectivité au réseau et de navigation.

**Remarque** : sauf dans le cas de Windows 8 ou des versions ultérieures de Windows, Microsoft Edge utilise *toujours* les API natives pour résoudre les problèmes de connectivité.

Si vous ne configurez pas cette stratégie, Microsoft Edge respecte la préférence de l'utilisateur, définie sous la section Services à l'adresse edge://settings/privacy.
De manière spécifique, il existe un bouton bascule **Utiliser un service web pour résoudre les erreurs de navigation** qui peut être activé ou désactivé par l'utilisateur. Sachez que si vous avez activé cette stratégie (ResolveNavigationErrorsUseWebService), le bouton bascule **Utiliser un service web pour résoudre les erreurs de navigation** est activé, mais l'utilisateur n'est pas en mesure de modifier ce paramètre en utilisant le bouton bascule. Si vous avez désactivé cette stratégie, le paramètre the **Utiliser un service web pour résoudre les erreurs de navigation** est désactivé et l'utilisateur n'est pas en mesure de modifier ce paramètre en utilisant le bouton bascule.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ResolveNavigationErrorsUseWebService
  - Nom de la stratégie de groupe: Activer la résolution des erreurs de navigation à l'aide d'un service web
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: ResolveNavigationErrorsUseWebService
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ResolveNavigationErrorsUseWebService
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### RestrictSigninToPattern
  #### Restreindre les comptes qui peuvent être utilisés en tant que comptes principaux Microsoft Edge
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Détermine quels comptes peuvent être définis comme comptes principaux de navigateur dans Microsoft Edge (le compte choisi lors du flux d’abonnement à la synchronisation).

Si un utilisateur tente de configurer un compte principal de navigateur avec un nom d’utilisateur qui ne correspond pas à ce modèle, il est bloqué et le message d’erreur approprié s’affiche. Vous pouvez configurer cette stratégie pour qu’elle corresponde à plusieurs comptes à l’aide d’une expression régulière de style Perl pour le modèle. Notez que les correspondances de modèle respectent la casse. Pour plus d’informations sur les règles d’expression régulière utilisées, consultez https://go.microsoft.com/fwlink/p/ ?linkid=2133903.

  Si vous ne configurez pas cette stratégie ou laissez cette zone vide, les utilisateurs peuvent définir un compte comme compte principal de navigateur dans Microsoft Edge.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: RestrictSigninToPattern
  - Nom de la stratégie de groupe: Restreindre les comptes qui peuvent être utilisés en tant que comptes principaux Microsoft Edge
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: RestrictSigninToPattern
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
".*@contoso.com"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: RestrictSigninToPattern
  - Exemple de valeur :
``` xml
<string>.*@contoso.com</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### RoamingProfileLocation
  #### Définir le répertoire de profils itinérants
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 85 ou ultérieur

  #### Description
  Configurer le répertoire à utiliser pour stocker la copie itinérante des profils.

Si vous activez cette stratégie, Microsoft Edge utilise le répertoire fourni pour stocker une copie itinérante des profils tant que vous avez également activé la stratégie [RoamingProfileSupportEnabled](#roamingprofilesupportenabled). Si vous désactivez la stratégie [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) ou si vous ne la configurez pas, la valeur stockée dans cette stratégie n’est pas utilisée.

Voir [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) pour obtenir la liste des variables que vous pouvez utiliser.

Si vous ne configurez pas cette stratégie, le chemin d’accès du profil itinérant par défaut est utilisé.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: RoamingProfileLocation
  - Nom de la stratégie de groupe: Définir le répertoire de profils itinérants
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: RoamingProfileLocation
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"${roaming_app_data}\\edge-profile"
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### RoamingProfileSupportEnabled
  #### Activer l’utilisation des copies itinérantes pour les données de profil Microsoft Edge
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 85 ou ultérieur

  #### Description
  Activez cette stratégie pour utiliser des profils itinérants sous Windows. Les paramètres stockés dans les profils Microsoft Edge (favoris, données de Remplissage auto et mots de passe) sont également enregistrés dans un fichier stocké dans le dossier de profil utilisateur itinérant (ou dans l’emplacement spécifié par l’administrateur via la stratégie [RoamingProfileLocation](#roamingprofilelocation)).

Si vous désactivez cette stratégie ou ne la configurez pas, seuls les profils locaux habituels sont utilisés.

La stratégie [SyncDisabled](#syncdisabled) désactive l’ensemble de la synchronisation des données et remplace la stratégie.

Voir https://docs.microsoft.com/windows-server/storage/folder-redirection/deploy-roaming-user-profiles pour plus d’informations sur l’utilisation des profils utilisateur itinérants.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: RoamingProfileSupportEnabled
  - Nom de la stratégie de groupe: Activer l’utilisation des copies itinérantes pour les données de profil Microsoft Edge
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: RoamingProfileSupportEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### RunAllFlashInAllowMode
  #### Étendre le paramètre de contenu d'Adobe Flash à l'ensemble du contenu
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Si vous activez cette stratégie, la totalité du contenu Adobe Flash incorporé dans les sites web définis de manière à autoriser Adobe Flash dans les paramètres de contenu, que ce soit par l’utilisateur ou par la stratégie d’entreprise, est exécutée. Ceci inclut le contenu provenant d’autres origines et/ou du contenu de petite taille.

Pour contrôler les sites web autorisés à exécuter Adobe Flash, consultez les spécifications dans les stratégies [DefaultPluginsSetting](#defaultpluginssetting), [PluginsAllowedForUrls](#pluginsallowedforurls) et [PluginsBlockedForUrls](#pluginsblockedforurls).

Si vous désactivez cette stratégie ou si vous ne la configurez pas, le contenu Adobe Flash provenant d’autres origines (provenant de sites qui ne sont pas spécifiés dans les trois stratégies mentionnées ci-dessus) ou le contenu de petite taille risque d'être bloqué.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: RunAllFlashInAllowMode
  - Nom de la stratégie de groupe: Étendre le paramètre de contenu d'Adobe Flash à l'ensemble du contenu
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: RunAllFlashInAllowMode
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: RunAllFlashInAllowMode
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SSLErrorOverrideAllowed
  #### Autoriser les utilisateurs à continuer à partir de la page d’avertissement HTTPS
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Microsoft Edge affiche une page d’avertissement lorsque les utilisateurs visitent des sites présentant des erreurs SSL.

	Si vous activez cette stratégie ou ne la configurez pas (par défaut), les utilisateurs peuvent cliquer sur ces pages d’avertissement.

	Si vous désactivez cette stratégie, les utilisateurs ne peuvent cliquer sur aucune page d’avertissement.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SSLErrorOverrideAllowed
  - Nom de la stratégie de groupe: Autoriser les utilisateurs à continuer à partir de la page d’avertissement HTTPS
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: SSLErrorOverrideAllowed
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SSLErrorOverrideAllowed
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SSLVersionMin
  #### Version TLS minimale activée
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définit la version minimale prise en charge de SSL. Si vous ne configurez pas cette stratégie, Microsoft Edge utilise une version minimale par défaut, TLS 1.0.

Si vous activez cette stratégie, vous pouvez définir la version minimale sur l’une des valeurs suivantes : « TLSv1 », « TLSv1.1 » ou « TLSv1.2 ». Si elle est définie, Microsoft Edge n’utilise pas une version de SSL/TLS inférieure à la version spécifiée. Une valeur non reconnue est ignorée.

Mappage des options de stratégie :

* TLSv1 (tls1) = TLS 1.0

* TLSv1.1 (tls1.1) = TLS 1.1

* TLSv1.2 (tls1.2) = TLS 1.2

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SSLVersionMin
  - Nom de la stratégie de groupe: Version TLS minimale activée
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: SSLVersionMin
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"tls1"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SSLVersionMin
  - Exemple de valeur :
``` xml
<string>tls1</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SaveCookiesOnExit
  #### Enregistrer les cookies lorsque Microsoft Edge se ferme
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Lorsque cette stratégie est activée, le groupe de cookies spécifié est exempté de la suppression lorsque le navigateur se ferme. Cette stratégie ne s’applique que lorsque :
- Le basculement « Cookies et autres données du site » est configuré dans Paramètres/Confidentialité et services/Effacer les données de navigation à la fermeture ou
- La stratégie [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) est activée ou
- La stratégie [DefaultCookiesSetting](#defaultcookiessetting) est définie sur « Conserver les cookies pendant toute la durée de la session ».

Vous pouvez définir une liste de sites, sur la base des modèles d’URL, dont les cookies sont conservés entre les sessions.

Remarque : les utilisateurs peuvent encore modifier la liste des sites de cookies pour ajouter ou supprimer des URL. Toutefois, il ne peut pas supprimer les URL qui ont été ajoutées par un administrateur.

Si vous activez cette stratégie, la liste de cookies ne sera pas supprimée lorsque le navigateur se ferme.

Si vous désactivez ou ne configurez pas cette stratégie, la configuration personnelle de l’utilisateur est utilisée.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SaveCookiesOnExit
  - Nom de la stratégie de groupe: Enregistrer les cookies lorsque Microsoft Edge se ferme
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SaveCookiesOnExit
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SavingBrowserHistoryDisabled
  #### Désactiver l’enregistrement de l’historique du navigateur
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Désactive l’enregistrement de l’historique du navigateur et empêche les utilisateurs de modifier ce paramètre.

Si vous activez cette stratégie, l’historique de navigation n'est pas enregistré. Ce paramètre désactive également la synchronisation des onglets.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, l’historique de navigation est enregistré.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SavingBrowserHistoryDisabled
  - Nom de la stratégie de groupe: Désactiver l’enregistrement de l’historique du navigateur
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: SavingBrowserHistoryDisabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SavingBrowserHistoryDisabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ScreenCaptureAllowed
  #### Autoriser ou refuser la capture d’écran
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 83 ou version ultérieure

  #### Description
  Si vous activez cette stratégie ou si vous ne la configurez pas, une page web peut utiliser les API de partage d’écran (par exemple, getDisplayMedia() ou l’API d’extension Capture de bureau) pour une capture d’écran.
Si vous désactivez cette stratégie, les appels vers les API de partage d’écran vont échouer. Par exemple, si vous utilisez une réunion en ligne basée sur le web, le partage d’écran ou de vidéo sera défaillant.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ScreenCaptureAllowed
  - Nom de la stratégie de groupe: Autoriser ou refuser la capture d’écran
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ScreenCaptureAllowed
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ScreenCaptureAllowed
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ScrollToTextFragmentEnabled
  #### Activer le défilement vers le texte spécifié dans les fragments d’URL
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 83 ou version ultérieure

  #### Description
  Cette fonctionnalité permet aux navigations par lien hypertexte et par URL de la barre d’adresse de cibler du texte spécifique sur une page web qui fera l’objet d’un défilement vers le bas une fois qu'elle aura été chargée.

Si vous activez cette stratégie ou si vous ne la configurez pas, le défilement des pages web vers des fragments de texte spécifiques via une URL est activé.

Si vous désactivez cette stratégie, le défilement des pages web vers des fragments de texte spécifiques via une URL est désactivé.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ScrollToTextFragmentEnabled
  - Nom de la stratégie de groupe: Activer le défilement vers le texte spécifié dans les fragments d’URL
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ScrollToTextFragmentEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ScrollToTextFragmentEnabled
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SearchSuggestEnabled
  #### Activer les suggestions de recherche
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Active les suggestions de recherche sur le web dans la barre d’adresses et liste de suggestions automatiques de Microsoft Edge et empêche les utilisateurs de modifier cette stratégie.

	Si vous activez cette stratégie, les suggestions de recherche sur le web sont utilisées.

	Si vous désactivez cette stratégie, les suggestions de recherche sur le web ne sont jamais utilisées, mais l'historique local et les suggestions de favoris locaux apparaissent toujours. Si vous désactivez cette stratégie, ni les caractères tapés, ni les URL consultées ne sont inclus dans les données de télémétrie destinées à Microsoft.

	Si cette stratégie reste non définie, les suggestions de recherche sont activées, mais l’utilisateur peut modifier ce paramètre.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SearchSuggestEnabled
  - Nom de la stratégie de groupe: Activer les suggestions de recherche
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: SearchSuggestEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SearchSuggestEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SecurityKeyPermitAttestation
  #### Sites web ou domaines qui ne nécessitent pas l'autorisation d'utiliser l’attestation de clé de sécurité directe
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifie les sites web et les domaines qui ne nécessitent pas d’autorisation utilisateur explicite lorsque des certificats d’attestation provenant des clés de sécurité sont obligatoires. En outre, un signal est envoyé à la clé de sécurité indiquant qu’elle peut utiliser l’attestation individuelle. Sans cela, les utilisateurs sont invités chaque fois qu’un site demande une attestation de clés de sécurité.

Les sites (par exemple, https://contoso.com/some/path) ne correspondent qu'en tant qu’appID U2F. Les domaines (par exemple, contoso.com) ne correspondent qu'en tant qu'ID RP webauthn. Pour couvrir à la fois les API U2F et webauthn pour un site donné, vous devez répertorier les domaines et URL appID.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SecurityKeyPermitAttestation
  - Nom de la stratégie de groupe: Sites web ou domaines qui ne nécessitent pas l'autorisation d'utiliser l’attestation de clé de sécurité directe
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation\1 = "https://contoso.com"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SecurityKeyPermitAttestation
  - Exemple de valeur :
``` xml
<array>
  <string>https://contoso.com</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SendIntranetToInternetExplorer
  #### Envoyer tous les sites intranet vers Internet Explorer
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 77 ou ultérieur

  #### Description
  Pour obtenir des instructions sur la configuration optimale de l’expérience pour Internet Explorer, consultez [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SendIntranetToInternetExplorer
  - Nom de la stratégie de groupe: Envoyer tous les sites intranet vers Internet Explorer
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: SendIntranetToInternetExplorer
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SendSiteInfoToImproveServices
  #### Envoyer les informations de site pour améliorer les services Microsoft (déconseillé)
  >DÉCONSEILLÉ : cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans Microsoft Edge 89. Cette stratégie est remplacée par la nouvelle stratégie : [DiagnosticData](#diagnosticdata)pour Windows 7, Windows 8 et macOS. Cette stratégie est remplacée par la fonctionnalité de télémétrie sur Win 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

     Cette stratégie active l’envoi d’informations sur les sites web visités dans Microsoft Edge à Microsoft pour améliorer les services tels que la recherche.

     Activer cette stratégie pour envoyer des informations sur les sites web visités dans Microsoft Edge à Microsoft. Désactiver cette stratégie pour ne pas envoyer d’informations sur les sites web visités dans Microsoft Edge à Microsoft. Dans les deux cas, les utilisateurs ne peuvent pas modifier le paramètre ou le remplacer.

     Sur Windows 10, si vous ne configurez pas cette stratégie, Microsoft Edge est configuré par défaut sur les données de diagnostic de Windows. Si cette stratégie est activée Microsoft Edge enverra uniquement les informations relatives aux sites web visités dans Microsoft Edge si le paramètre de données de diagnostic Windows est défini sur Complet. Si cette stratégie est désactivée Microsoft Edge n’enverra pas d’informations sur les sites web visités. En savoir plus sur les paramètres des données de diagnostic Windows : [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

     Sur Windows 7, Windows 8 et macOS cette stratégie contrôle l’envoi d’informations sur les sites web visités. Si vous ne configurez pas cette stratégie, Microsoft Edge aura par défaut la préférence de l’utilisateur.

pour activer cette stratégie, [MetricsReportingEnabled](#metricsreportingenabled) doit être configuré sur Activé. Si [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) ou [MetricsReportingEnabled](#metricsreportingenabled) n’est pas configuré ou désactivé, ces données ne sont pas envoyées à Microsoft.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SendSiteInfoToImproveServices
  - Nom de la stratégie de groupe: Envoyer les informations de site pour améliorer les services Microsoft (déconseillé)
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: SendSiteInfoToImproveServices
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SendSiteInfoToImproveServices
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SensorsAllowedForUrls
  #### Autoriser l’accès aux capteurs sur des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Définissez une liste de sites, basée sur des modèles d’URL, qui peuvent accéder et utiliser des capteurs comme les capteurs de mouvement et de luminosité.

Si vous ne configurez pas cette stratégie, la valeur par défaut globale de la stratégie [DefaultSensorsSetting](#defaultsensorssetting) (si elle est définie) ou de la configuration personnelle de l’utilisateur est utilisée pour tous les sites.

Pour les modèles d’URL qui ne correspondent pas à cette stratégie, l’ordre de priorité suivant est utilisé : la stratégie [SensorsBlockedForUrls](#sensorsblockedforurls) (s’il existe une correspondance), la stratégie [DefaultSensorsSetting](#defaultsensorssetting) (si elle est définie) ou les paramètres personnels de l’utilisateur.

Les modèles d’URL définis dans cette stratégie ne peuvent pas entrer en conflit avec ceux configurés dans la stratégie [SensorsBlockedForUrls](#sensorsblockedforurls). Vous ne pouvez pas autoriser et bloquer une URL.

Pour obtenir des informations détaillées sur les modèles d’URL valides, rendez-vous à l’adresse [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SensorsAllowedForUrls
  - Nom de la stratégie de groupe: Autoriser l’accès aux capteurs sur des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SensorsAllowedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SensorsBlockedForUrls
  #### Bloquer l’accès aux capteurs sur des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Définissez une liste de sites, basée sur des modèles d’URL, qui ne peuvent pas accéder aux capteurs tels que les capteurs de mouvement et de luminosité.

Si vous ne configurez pas cette stratégie, la valeur par défaut globale de la stratégie [DefaultSensorsSetting](#defaultsensorssetting) (si elle est définie) ou de la configuration personnelle de l’utilisateur est utilisée pour tous les sites.

      Pour les modèles d’URL qui ne correspondent pas à cette stratégie, l’ordre de priorité suivant est utilisé : la stratégie [SensorsAllowedForUrls](#sensorsallowedforurls) (s’il existe une correspondance), la stratégie [DefaultSensorsSetting](#defaultsensorssetting) (si elle est définie) ou les paramètres personnels de l’utilisateur.

Les modèles d’URL définis dans cette stratégie ne peuvent pas entrer en conflit avec ceux configurés dans la stratégie [SensorsAllowedForUrls](#sensorsallowedforurls). Vous ne pouvez pas autoriser et bloquer une URL.

Pour obtenir des informations détaillées sur les modèles d’URL valides, voir [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SensorsBlockedForUrls
  - Nom de la stratégie de groupe: Bloquer l’accès aux capteurs sur des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SensorsBlockedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SerialAskForUrls
  #### Autoriser l’API série sur des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Définissez une liste de sites basée sur des modèles d’URL, qui peuvent inviter l’utilisateur à accéder à un port série.

Si vous ne configurez pas cette stratégie, la valeur par défaut globale de la stratégie [DefaultSerialGuardSetting](#defaultserialguardsetting) (si elle est définie) ou de la configuration personnelle de l’utilisateur est utilisée pour tous les sites.

Pour les modèles d’URL qui ne correspondent pas à cette stratégie, l’ordre de priorité suivant est utilisé: la stratégie [SerialBlockedForUrls](#serialblockedforurls) (s’il existe une correspondance), la stratégie [DefaultSerialGuardSetting](#defaultserialguardsetting) (si elle est définie) ou les paramètres personnels de l’utilisateur.

Les modèles d’URL définis dans stratégie ne peuvent pas entrer en conflit avec ceux configurés dans la stratégie [SerialBlockedForUrls](#serialblockedforurls). Vous ne pouvez pas autoriser et bloquer une URL.

Pour obtenir des informations détaillées sur les modèles d’URL valides, voir [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SerialAskForUrls
  - Nom de la stratégie de groupe: Autoriser l’API série sur des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SerialAskForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SerialBlockedForUrls
  #### Bloquer l’API série sur des sites spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Définissez une liste de sites basée sur des modèles d’URL, qui ne peut pas demander à l’utilisateur de lui accorder l’accès à un port série.

Si vous ne configurez pas cette stratégie, la valeur par défaut globale de la stratégie [DefaultSerialGuardSetting](#defaultserialguardsetting) (si elle est définie) ou de la configuration personnelle de l’utilisateur est utilisée pour tous les sites.

Pour les modèles d’URL qui ne correspondent pas à cette stratégie, l’ordre de priorité suivant est utilisé: la stratégie [SerialAskForUrls](#serialaskforurls) (s’il existe une correspondance), la stratégie [DefaultSerialGuardSetting](#defaultserialguardsetting) (si elle est définie) ou les paramètres personnels de l’utilisateur.

Les modèles d’URL de cette stratégie ne peuvent pas entrer en conflit avec ceux configurés dans la stratégie [SerialAskForUrls](#serialaskforurls). Vous ne pouvez pas autoriser et bloquer une URL.

Pour obtenir des informations détaillées sur les modèles d’URL valides, voir [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SerialBlockedForUrls
  - Nom de la stratégie de groupe: Bloquer l’API série sur des sites spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SerialBlockedForUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### ShowOfficeShortcutInFavoritesBar
  #### Afficher les raccourcis Microsoft Office dans la barre des favoris
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifie s’il faut inclure un raccourci vers Office.com dans la barre des favoris. Pour les utilisateurs connectés à Microsoft Edge, le raccourci dirige les utilisateurs vers leurs applications et documents Microsoft Office.

	Si cette stratégie est activée ou si vous ne la configurez pas, les utilisateurs peuvent choisir d'afficher le raccourci en modifiant le bouton bascule dans le menu contextuel de la barre des favoris.

	Si vous désactivez cette stratégie, le raccourci n'est pas affiché.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: ShowOfficeShortcutInFavoritesBar
  - Nom de la stratégie de groupe: Afficher les raccourcis Microsoft Office dans la barre des favoris
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: ShowOfficeShortcutInFavoritesBar
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: ShowOfficeShortcutInFavoritesBar
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SignedHTTPExchangeEnabled
  #### Activer la prise en charge de SXG (échange HTTP signé)
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 78 ou version ultérieure

  #### Description
  Activer le support pour Signed HTTP Exchange (SXG).

Si cette stratégie n'est pas définie ou activée, Microsoft Edge accepte les contenus web servis en tant que Signed HTTP Exchanges.

Si cette stratégie est désactivée, Signed HTTP Exchanges ne peut pas être chargé.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SignedHTTPExchangeEnabled
  - Nom de la stratégie de groupe: Activer la prise en charge de SXG (échange HTTP signé)
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: SignedHTTPExchangeEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SignedHTTPExchangeEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SitePerProcess
  #### Activer l’isolation de site pour chaque site
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  La stratégie « SitePerProcess » peut également être utilisée pour empêcher les utilisateurs de refuser le comportement par défaut visant à isoler tous les sites. Notez que vous pouvez également utiliser la stratégie [IsolateOrigins](#isolateorigins) pour isoler des origines supplémentaires et plus fines.
Si vous activez cette stratégie, les utilisateurs ne peuvent pas refuser le comportement par défaut selon lequel chaque site exécute son propre processus.
Si vous désactivez ou ne configurez pas cette stratégie, les utilisateurs peuvent refuser l'isolation du site. (Par exemple, en utilisant l'entrée « Disable site isolation » dans edge://flags.) La désactivation ou non-configuration de cette stratégie n'aura pas pour effet la désactivation de l'isolation du site.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SitePerProcess
  - Nom de la stratégie de groupe: Activer l’isolation de site pour chaque site
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: SitePerProcess
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SitePerProcess
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SpellcheckEnabled
  #### Activer la vérification orthographique
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Si vous activez cette stratégie ou si vous ne la configurez pas, l’utilisateur peut utiliser le vérificateur orthographique.

Si vous désactivez cette stratégie, l’utilisateur ne peut pas utiliser le vérificateur orthographique et les stratégies [SpellcheckLanguage](#spellchecklanguage) et [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) sont également désactivées.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SpellcheckEnabled
  - Nom de la stratégie de groupe: Activer la vérification orthographique
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: SpellcheckEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SpellcheckEnabled
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SpellcheckLanguage
  #### Activer des langues de vérification orthographique spécifiques
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 77 ou ultérieur

  #### Description
  Active des langues différentes pour le vérificateur orthographique. Les langues spécifiées qui ne sont pas reconnues sont ignorées.

Si vous activez cette stratégie, le vérificateur orthographique est activé pour les langues spécifiées, ainsi que les langues que l’utilisateur a activées.

Si vous ne configurez pas ou si vous désactivez cette stratégie, aucune modification n'est apportée aux préférences de vérificateur orthographique de l’utilisateur.

Si la stratégie [SpellcheckEnabled](#spellcheckenabled) est désactivée, cette stratégie n’aura aucun effet.

Si une langue est incluse dans les deux stratégies « SpellcheckLanguage » et [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist), la langue du vérificateur orthographique est activée.

Les langues prises en charge sont les suivantes : af, bg, ca, cs, cy, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SpellcheckLanguage
  - Nom de la stratégie de groupe: Activer des langues de vérification orthographique spécifiques
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\2 = "es"

```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SpellcheckLanguageBlocklist
  #### Forcer la désactivation des langues de la vérification orthographique
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 78 ou ultérieur

  #### Description
  Désactive de force les langues du vérificateur orthographique. Les langues non reconnues dans cette liste seront ignorées.

Si vous activez cette stratégie, le vérificateur orthographique est désactivé pour les langues spécifiées. L’utilisateur peut toujours activer ou désactiver le vérificateur orthographique pour les langues qui ne sont pas dans la liste.

Si vous ne définissez pas cette stratégie ou si vous la désactivez, les préférences de vérificateur orthographique de l’utilisateur ne sont pas modifiées.

Si la stratégie [SpellcheckEnabled](#spellcheckenabled) est désactivée, cette stratégie n’a aucun effet.

Si une langue est incluse dans les stratégies [SpellcheckLanguage](#spellchecklanguage) et « SpellcheckLanguageBlocklist », la langue du vérificateur orthographique est activée.

Les langues actuellement prises en charge sont les suivantes : af, bg, ca, cs, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SpellcheckLanguageBlocklist
  - Nom de la stratégie de groupe: Forcer la désactivation des langues de la vérification orthographique
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\2 = "es"

```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### StricterMixedContentTreatmentEnabled
  #### Activer le traitement plus strict pour le contenu mixte (déconseillé)
  >DÉCONSEILLÉ : cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 81 ou version ultérieure

  #### Description
  Cette stratégie n’est plus utilisée, car elle est conçue comme un mécanisme à court terme destiné à offrir aux entreprises davantage de temps pour mettre à jour leur contenu web incompatible avec le traitement plus strict du contenu mixte. Elle ne fonctionnera pas dans Microsoft Edge version 85.

Cette stratégie contrôle le traitement du contenu mixte (contenu HTTP dans les sites HTTPS) dans le navigateur.

Si vous définissez cette stratégie sur True ou omettez de la définir, le contenu mixte audio et vidéo sera automatiquement mis à jour vers HTTPS (autrement dit, l’URL sera réécrite en HTTPS, sans solution de secours si la ressource n’est pas disponible via HTTPS) et un avertissement de page non sécurisée s’affichera dans la barre d’URL pour le contenu mixte de type image.

Si vous définissez la stratégie sur False, les mises à jour automatiques seront désactivées pour le contenu audio et vidéo, et aucun avertissement ne s’affichera pour les images.

Cette stratégie n’affecte pas les types de contenu mixte autres que les contenus audio et vidéo, et les images.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: StricterMixedContentTreatmentEnabled
  - Nom de la stratégie de groupe: Activer le traitement plus strict pour le contenu mixte (déconseillé)
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: StricterMixedContentTreatmentEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: StricterMixedContentTreatmentEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SuppressUnsupportedOSWarning
  #### Supprimer l’avertissement de système d’exploitation non pris en charge
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Supprime l’avertissement qui s’affiche lorsque Microsoft Edge est exécuté sur un ordinateur ou un système d’exploitation qui n’est plus pris en charge.

Si cette stratégie est false ou non définie, les avertissements s’affichent sur des ordinateurs ou des systèmes d’exploitation non pris en charge.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SuppressUnsupportedOSWarning
  - Nom de la stratégie de groupe: Supprimer l’avertissement de système d’exploitation non pris en charge
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: SuppressUnsupportedOSWarning
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SuppressUnsupportedOSWarning
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SyncDisabled
  #### Désactiver la synchronisation des données à l’aide des services de synchronisation Microsoft
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Désactive la synchronisation des données dans Microsoft Edge. Cette stratégie empêche également l’affichage de l’invite d'accord de synchronisation.

Si vous ne définissez pas cette stratégie ou si vous l’appliquez en tant que recommandation, les utilisateurs peuvent activer ou désactiver la synchronisation. Si vous appliquez cette stratégie comme obligatoire, les utilisateurs ne peuvent pas activer la synchronisation.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SyncDisabled
  - Nom de la stratégie de groupe: Désactiver la synchronisation des données à l’aide des services de synchronisation Microsoft
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: SyncDisabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SyncDisabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### SyncTypesListDisabled
  #### Configuration de la liste des types exclus de la synchronisation
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 83 ou version ultérieure

  #### Description
  Si vous activez cette stratégie, tous les types de données spécifiés seront exclus de la synchronisation. Cette stratégie permet de limiter le type de données téléchargées vers le Microsoft Edgeservice de synchronisation.

Vous pouvez fournir l’un des types de données suivants pour cette stratégie : « favoris », « paramètres », « mots de passe », « addressesAndMore », « extensions », « historique », « openTabs » et « collections ». Notez que le noms de ces types de données respectent la casse.

Les utilisateurs ne peuvent pas remplacer les types de données désactivés.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: SyncTypesListDisabled
  - Nom de la stratégie de groupe: Configuration de la liste des types exclus de la synchronisation
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled\1 = "favorites"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: SyncTypesListDisabled
  - Exemple de valeur :
``` xml
<array>
  <string>favorites</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### TLS13HardeningForLocalAnchorsEnabled
  #### Activez une fonctionnalité de sécurité TLS 1.3 pour les ancres d’approbation locales. (obsolète)
  
  >OBSOLÈTE : cette stratégie est obsolète et ne fonctionne pas après Microsoft Edge85.
  #### Versions prises en charge :
  - Sur Windows et macOS depuis le 81, jusqu’au 85

  #### Description
  Cette stratégie ne fonctionne pas, car elle est uniquement destinée à être un mécanisme à court terme pour accorder davantage de temps aux entreprises pour mettre à niveau les proxys concernées.

Cette stratégie contrôle une fonctionnalité de sécurité dans TLS 1.3 qui protège les connexions contre les attaques de rétrogradation. Elle offre une compatibilité descendante et n’affecte pas les connexions aux serveurs ou proxys TLS 1.2 conformes. Toutefois, les anciennes versions de certains proxys d’interception de TLS présentent un défaut d’implémentation qui les rend incompatibles.

Si vous activez cette stratégie ou si vous ne la définissez pas, Microsoft Edge active ces protections de sécurité pour toutes les connexions.

Si vous désactivez cette stratégie, Microsoft Edge désactive ces protections de sécurité pour les connexions authentifiées avec des certificats d’autorité de certification installés localement. Ces protections sont toujours activées pour les connexions authentifiées à l’aide de certificats d’autorité de certification publiquement approuvés.

Cette stratégie peut être utilisée pour tester les proxys concernés et les mettre à niveau. Les proxys concernés sont censés échouer à la connexion avec le code d’erreur ERR_TLS13_DOWNGRADE_DETECTED.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: TLS13HardeningForLocalAnchorsEnabled
  - Nom de la stratégie de groupe: Activez une fonctionnalité de sécurité TLS 1.3 pour les ancres d’approbation locales. (obsolète)
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: TLS13HardeningForLocalAnchorsEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: TLS13HardeningForLocalAnchorsEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### TLSCipherSuiteDenyList
  #### Spécifier les suites de chiffrement TLS à désactiver
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 85 ou version ultérieure

  #### Description
  Configurez la liste des suites de chiffrement désactivées pour les connexions TLS.

Si vous configurez cette stratégie, la liste des suites de chiffrement configurées ne sera pas utilisée lors de l’établissement de connexions TLS.

Si vous ne configurez pas cette stratégie, le navigateur choisit les suites de chiffrement TLS à utiliser.

Les valeurs de la suite de chiffrement à désactiver sont indiquées en tant que valeurs hexadécimales 16 bits. Les valeurs sont attribuées par le registre de l’organisme IANA (Internet Assigned Numbers Authority).

 La suite de chiffrement TLS 1.3 TLS_AES_128_GCM_SHA256 (0x1301) est exigée pour TLS 1.3 et ne peut pas être désactivée par cette stratégie.

 Cette stratégie n’affecte pas les connexions se basant sur QUIC. Le protocole QUIC peut être désactivé par le biais de la stratégie de [QuicAllowed](#quicallowed).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: TLSCipherSuiteDenyList
  - Nom de la stratégie de groupe: Spécifier les suites de chiffrement TLS à désactiver
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\1 = "0x1303"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\2 = "0xcca8"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\3 = "0xcca9"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: TLSCipherSuiteDenyList
  - Exemple de valeur :
``` xml
<array>
  <string>0x1303</string>
  <string>0xcca8</string>
  <string>0xcca9</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### TabFreezingEnabled
  #### Autoriser le gel des onglets d’arrière-plan
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 79 ou version ultérieure

  #### Description
  Contrôle si Microsoft Edge peut figer des onglets qui se trouvent en arrière-plan pendant au moins 5 minutes.

Le gel des onglets réduit l’utilisation de l’UC, de la batterie et de la mémoire. Microsoft Edge utilise l'heuristique pour éviter de figer des onglets qui permettent de travailler en arrière-plan, comme les notifications d’affichage, la lecture du son et la diffusion en continu de vidéo.

Si vous activez cette stratégie ou si vous ne la configurez pas, les onglets qui se trouvent à l’arrière-plan pendant au moins 5 minutes peuvent être figés.

Si vous désactivez cette stratégie, aucun onglet n’est figé.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: TabFreezingEnabled
  - Nom de la stratégie de groupe: Autoriser le gel des onglets d’arrière-plan
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: TabFreezingEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: TabFreezingEnabled
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### TaskManagerEndProcessEnabled
  #### Activer la fin des processus dans le gestionnaire des tâches du navigateur
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Si vous activez ou ne configurez pas cette stratégie, les utilisateurs peuvent arrêter les processus dans le Gestionnaire des tâches du navigateur. Si vous la désactivez, les utilisateurs ne peuvent pas arrêter les processus et le bouton Arrêter le processus est désactivé dans le Gestionnaire des tâches du navigateur.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: TaskManagerEndProcessEnabled
  - Nom de la stratégie de groupe: Activer la fin des processus dans le gestionnaire des tâches du navigateur
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: TaskManagerEndProcessEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: TaskManagerEndProcessEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### TotalMemoryLimitMb
  #### Définissez une limite de mémoire en méga-octets qu’une seule instance de Microsoft Edge peut utiliser.
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 80 ou version ultérieure

  #### Description
  Configure la quantité de mémoire qu’une seule instance de Microsoft Edge peut utiliser avant que les onglets soient supprimés pour économiser de la mémoire. La mémoire utilisée par l’onglet sera libérée et l’onglet devra être rechargé lorsque l'utilisateur souhaitera y accéder.

Si vous activez cette stratégie, le navigateur commence à supprimer des onglets pour économiser de la mémoire lorsque la limite est dépassée. Toutefois, il n’y a aucune garantie que le navigateur s’exécute toujours dans la limite. Toute valeur inférieure à 1 024 est arrondie à 1 024.

Si vous ne définissez pas cette stratégie, le navigateur n'essaie d’enregistrer la mémoire que lorsqu’il détecte que la quantité de mémoire physique sur son ordinateur est faible.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: TotalMemoryLimitMb
  - Nom de la stratégie de groupe: Définissez une limite de mémoire en méga-octets qu’une seule instance de Microsoft Edge peut utiliser.
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: TotalMemoryLimitMb
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000800
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: TotalMemoryLimitMb
  - Exemple de valeur :
``` xml
<integer>2048</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### TrackingPrevention
  #### Bloquer le suivi de l’activité de navigation sur le Web des utilisateurs
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 78 ou version ultérieure

  #### Description
  Vous permet de décider de bloquer ou non les sites web de suivi de l’activité de navigation sur le web des utilisateurs.

Si vous désactivez ou ne configurez pas cette stratégie, les utilisateurs peuvent définir leur propre niveau de prévention de la surveillance.

Mappage des options de stratégie :

* TrackingPreventionOff (0) = Désactivé (aucune prévention du suivi)

* TrackingPreventionBasic (1) = De base (bloque les dispositifs de suivi malveillants, le contenu et les publicités sont personnalisés)

* TrackingPreventionBalanced (2) = Équilibré (bloque les dispositifs de suivi malveillants et les dispositifs de suivi des sites que l'utilisateur n'a pas visités ; le contenu et les publicités sont moins personnalisés)

* TrackingPreventionStrict (3) = Strict (bloque les dispositifs de suivi malveillants et la majorité des dispositifs de suivi de tous les sites ; le contenu et les publicités ont une personnalisation minimale. Certaines parties des sites peuvent ne pas fonctionner)

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: TrackingPrevention
  - Nom de la stratégie de groupe: Bloquer le suivi de l’activité de navigation sur le Web des utilisateurs
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: TrackingPrevention
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000002
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: TrackingPrevention
  - Exemple de valeur :
``` xml
<integer>2</integer>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### TranslateEnabled
  #### Activer Traduire
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Active le service de traduction Microsoft intégré à Microsoft Edge.

	Si vous activez cette stratégie, Microsoft Edge offre des fonctionnalités de traduction à l’utilisateur en affichant un menu volant de traduction intégré le cas échéant, et une option de traduction dans le menu contextuel.

	Désactivez cette stratégie pour désactiver toutes les fonctionnalités de traduction intégrée.

	Si vous ne configurez pas la stratégie, les utilisateurs peuvent choisir d'utiliser la fonctionnalité de traduction ou non.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Oui
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: TranslateEnabled
  - Nom de la stratégie de groupe: Activer Traduire
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): Modèles d’administration/Microsoft Edge - Paramètres par défaut (les utilisateurs peuvent les modifier)/
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): SOFTWARE\Policies\Microsoft\Edge\Recommandé
  - Nom de la valeur: TranslateEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: TranslateEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### URLAllowlist
  #### Définir une liste d’URL autorisées
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Autorisez l’accès aux URL répertoriées en tant qu’exceptions à la liste rouge des URL.

Mettez en forme le modèle d’URL conformément à [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Vous pouvez utiliser cette stratégie pour ouvrir des exceptions aux listes rouges restrictives. Par exemple, vous pouvez inclure « * » dans la liste rouge pour bloquer toutes les requêtes, puis utiliser cette stratégie pour autoriser l’accès à une liste limitée d’URL. Vous pouvez utiliser cette stratégie pour ouvrir des exceptions pour certains schémas, sous-domaines d’autres domaines, ports ou chemins d’accès spécifiques.

Le filtre plus spécifique détermine si une URL est bloquée ou autorisée. La liste verte est prioritaire sur la liste rouge.

Cette stratégie est limitée à 1 000 entrées ; les entrées suivantes sont ignorées.

Cette stratégie permet également au navigateur d’appeler des applications externes enregistrées en tant que gestionnaires de protocoles pour des protocoles tels que « tel: » ou « ssh: ».

Si vous ne configurez pas cette stratégie, il n’y a aucune exception à la liste rouge dans la [URLBlocklist](#urlblocklist)stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: URLAllowlist
  - Nom de la stratégie de groupe: Définir une liste d’URL autorisées
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\URLAllowlist
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\5 = ".exact.hostname.com"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: URLAllowlist
  - Exemple de valeur :
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### URLBlocklist
  #### Bloquer l’accès à une liste d’URL
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Définissez la liste des sites en fonction des modèles d’URL qui sont bloqués (les utilisateurs ne peuvent pas les charger).

Mettez en forme le modèle d’URL conformément à [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Vous pouvez définir des exceptions dans la stratégie [URLAllowlist](#urlallowlist). Ces stratégies sont limitées à 1 000 entrées ; les entrées suivantes sont ignorées.

Notez qu'il est déconseillé de bloquer les URL internes « edge://* » : cela peut entraîner des erreurs inattendues.

Cette stratégie n’empêche pas la mise à jour dynamique de la page par le biais de JavaScript. Par exemple, si vous bloquez « contoso.com/abc », les utilisateurs pourront toujours visiter « contoso.com » et cliquer sur un lien pour accéder à « contoso.com/abc » tant que la page n’a pas été actualisée.

Si vous ne configurez pas cette stratégie, aucune URL n’est bloquée.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: URLBlocklist
  - Nom de la stratégie de groupe: Bloquer l’accès à une liste d’URL
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\URLBlocklist
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
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


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: URLBlocklist
  - Exemple de valeur :
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
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### UserAgentClientHintsEnabled
  #### Activer la fonctionnalité Indications client de l’agent utilisateur (déconseillé)
  >DÉCONSEILLÉ : cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 86 ou version ultérieure

  #### Description
  Cette stratégie est déconseillée, car elle est uniquement destinée à être un mécanisme à court terme pour accorder davantage de temps aux entreprises pour mettre à jour leur contenu web si et quand il est détecté comme étant incompatible avec la fonctionnalité Indicateurs client de l’agent utilisateur. Elle ne fonctionnera pas dans version Microsoft Edge 89.

Une fois activée, la fonctionnalité Indicateurs client de l’agent utilisateur envoie des en-têtes de requête granulaires fournissant des informations sur le navigateur de l’utilisateur (par exemple, la version du navigateur) et l’environnement (par exemple, l’architecture système).

Il s’agit d’une fonctionnalité supplémentaire, mais les nouveaux en-têtes peuvent désactiver certains sites web qui limitent les caractères que les requêtes peuvent contenir.

Si vous activez ou ne configurez pas cette stratégie, la fonctionnalité Indicateurs client de l’agent utilisateur est activée. Si vous désactivez cette stratégie, cette fonctionnalité n’est pas disponible.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: UserAgentClientHintsEnabled
  - Nom de la stratégie de groupe: Activer la fonctionnalité Indications client de l’agent utilisateur (déconseillé)
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: UserAgentClientHintsEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: UserAgentClientHintsEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### UserDataDir
  #### Définir le répertoire des données utilisateur
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Configurer le répertoire à utiliser pour le stockage des données utilisateur.

Si vous activez cette stratégie, Microsoft Edge utilise le répertoire spécifié, peu importe si l’utilisateur a spécifié l’indicateur de ligne de commande « --user-data-dir ».

Si vous ne configurez pas cette stratégie, le chemin d’accès du profil par défaut est utilisé et l’utilisateur peut le remplacer par l'indicateur de ligne de commande « --user-data-dir ». Le répertoire du profil est accessible par l’utilisateur dans le chemin d'accès du profil edge://version/.

Pour éviter toute perte de données ou d’autres erreurs inattendues, ne configurez pas cette stratégie sur le répertoire racine d’un volume ni sur un répertoire utilisé à d’autres fins, car Microsoft Edge gère son contenu.

Pour obtenir une liste des variables utilisables, veuillez consulter la page [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: UserDataDir
  - Nom de la stratégie de groupe: Définir le répertoire des données utilisateur
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: UserDataDir
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"${users}/${user_name}/Edge"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: UserDataDir
  - Exemple de valeur :
``` xml
<string>${users}/${user_name}/Edge</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### UserDataSnapshotRetentionLimit
  #### Limite le nombre d’instantanés de données utilisateur conservés pour une utilisation en cas d’annulation d’urgence
  
  
  #### Versions prises en charge :
  - Sur Windows depuis 86 ou ultérieur

  #### Description
  À l’issue de chaque mise à jour de version majeure, Microsoft Edge crée un instantané des parties des données de navigation de l’utilisateur à utiliser en cas d’urgence ultérieure nécessitant une restauration de version temporaire. Si une restauration temporaire est effectuée sur une version pour laquelle un utilisateur dispose d’un instantané correspondant, les données de l’instantané sont restaurées. Ainsi, les utilisateurs peuvent conserver les paramètres tels que les signets et les données de remplissage automatique.

Si vous ne configurez pas cette stratégie, la valeur par défaut, 3 instantanés, est utilisée.

Si vous configurez cette stratégie, les anciens instantanés sont supprimés si nécessaire pour respecter la limite que vous avez définie. Si vous configurez cette stratégie sur 0, aucun snapshot n’est pris.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Entier

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: UserDataSnapshotRetentionLimit
  - Nom de la stratégie de groupe: Limite le nombre d’instantanés de données utilisateur conservés pour une utilisation en cas d’annulation d’urgence
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: UserDataSnapshotRetentionLimit
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000003
```


  

  [Revenir au début](#microsoft-edge---stratégies)

  ### UserFeedbackAllowed
  #### Autoriser les commentaires des utilisateurs
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Microsoft Edge utilise la fonctionnalité de commentaires Edge (activée par défaut) pour permettre aux utilisateurs d’envoyer des commentaires, des suggestions ou des enquêtes client et de signaler des problèmes liés au navigateur. En outre, par défaut, les utilisateurs ne peuvent pas désactiver la fonctionnalité de commentaires Edge.

	Si vous activez cette stratégie ou ne la configurez pas, les utilisateurs peuvent appeler des commentaires Edge.

	Si vous désactivez cette stratégie, les utilisateurs ne peuvent pas invoquer les commentaires Edge.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: UserFeedbackAllowed
  - Nom de la stratégie de groupe: Autoriser les commentaires des utilisateurs
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: UserFeedbackAllowed
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: UserFeedbackAllowed
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### VideoCaptureAllowed
  #### Autoriser ou bloquer la capture vidéo
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Contrôle si les sites peuvent effectuer des captures vidéo.

Si cette option est activée ou n'est pas configurée (par défaut), l’utilisateur est invité à accorder l’accès de capture vidéo à tous les sites, à l’exception de ceux dont les URL configurées dans la liste de la stratégie [VideoCaptureAllowedUrls](#videocaptureallowedurls), qui bénéficient d'une autorisation d'accès sans invite.

Si vous désactivez cette stratégie, l’utilisateur ne reçoit pas d'invitation et les captures vidéo ne sont disponibles que pour les URL configurées dans la stratégie [VideoCaptureAllowedUrls](#videocaptureallowedurls).

Cette stratégie affecte tous les types d’entrées vidéo, pas seulement la caméra intégrée.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: VideoCaptureAllowed
  - Nom de la stratégie de groupe: Autoriser ou bloquer la capture vidéo
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: VideoCaptureAllowed
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000000
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: VideoCaptureAllowed
  - Exemple de valeur :
``` xml
<false/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### VideoCaptureAllowedUrls
  #### Sites pouvant accéder aux appareils de capture vidéo sans demander l’autorisation
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Spécifiez les sites web, en fonction de modèles d’URL, qui peuvent utiliser des appareils de capture vidéo sans demander l’autorisation de l'utilisateur. Les modèles de cette liste sont comparés à l’origine de sécurité de l’URL d'incorporation. S'ils correspondent, le site reçoit automatiquement l’accès à des appareils de capture vidéo.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: VideoCaptureAllowedUrls
  - Nom de la stratégie de groupe: Sites pouvant accéder aux appareils de capture vidéo sans demander l’autorisation
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: VideoCaptureAllowedUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### WPADQuickCheckEnabled
  #### Définir l'optimisation WPAD
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Vous autorise à désactiver l’optimisation WPAD (Découverte automatique de proxy web) dans Microsoft Edge.

	Si vous désactivez cette stratégie, l’optimisation WPAD est désactivée, ce qui fait patienter le navigateur plus longtemps que les serveurs WPAD basés sur DNS.

	Si vous activez ou ne configurez pas la stratégie, l’optimisation WPAD est activée.

	Indépendamment de l'activation ou non de cette stratégie, le paramètre d’optimisation WPAD ne peut pas être modifié par les utilisateurs.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: WPADQuickCheckEnabled
  - Nom de la stratégie de groupe: Définir l'optimisation WPAD
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: WPADQuickCheckEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: WPADQuickCheckEnabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### WebAppInstallForceList
  #### Configurer la liste des applications web installées de force
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 80 ou version ultérieure

  #### Description
  Spécifie la liste des sites web qui sont installés en mode silencieux, sans interaction de l’utilisateur, et qui ne peuvent pas être désinstallés ou désactivés par l’utilisateur.

Chaque élément de la liste de la stratégie est un objet avec les membres suivants :
  -« URL », qui est obligatoire. « URL » doit être l’URL de l’application web à installer.

Les valeurs des membres facultatifs sont les suivantes :
  -« launch_container » doit avoir la valeur « window » ou « tab » pour indiquer comment l’application web sera ouverte après son installation.
  -« create_desktop_shortcut » doit avoir la valeur true si un raccourci de Bureau doit être créé sur Windows.

Si « default_launch_container » est omis, l’application s’ouvre par défaut dans un onglet. Quelle que soit la valeur de « default_launch_container », les utilisateurs peuvent modifier le conteneur dans lequel l’application s'ouvre. Si « create_desktop_shortcuts » est omis, aucun raccourci de Bureau n'est créé.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Oui

  #### Type de données:
  - Dictionnaire

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: WebAppInstallForceList
  - Nom de la stratégie de groupe: Configurer la liste des applications web installées de force
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: WebAppInstallForceList
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
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


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: WebAppInstallForceList
  - Exemple de valeur :
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
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### WebComponentsV0Enabled
  #### Réactivez l’API Web Components v0 jusqu’à M84 (obsolète)
  
  >OBSOLÈTE : cette stratégie est obsolète et ne fonctionne pas après Microsoft Edge84.
  #### Versions prises en charge :
  - Sur Windows et macOS depuis le 80, jusqu’au 84

  #### Description
  Cette stratégie ne fonctionne pas car elle a autorisé ces fonctionnalités à être activées de nouveau de façon sélective jusqu’à Microsoft Edge version 85.Les composants web des API v0 (Shadow DOM v0, Custom Elements v0 et HTML Imports) ont été déconseillés en 2018 et ont été désactivés par défaut à partir de Microsoft Edge version 80.

Si vous définissez cette stratégie sur True, les fonctionnalités de composants web v0 seront activées pour tous les sites.

Si vous affectez la valeur False à cette stratégie ou si vous ne définissez pas cette stratégie, les fonctionnalités de l’option v0 du composant web sont désactivées par défaut, à partir de M80.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: WebComponentsV0Enabled
  - Nom de la stratégie de groupe: Réactivez l’API Web Components v0 jusqu’à M84 (obsolète)
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: WebComponentsV0Enabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: WebComponentsV0Enabled
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### WebDriverOverridesIncompatiblePolicies
  #### Autoriser WebDriver à remplacer les stratégies incompatibles (obsolète)
  
  >OBSOLÈTE : cette stratégie est obsolète et ne fonctionne pas après Microsoft Edge84.
  #### Versions prises en charge :
  - Sur Windows et macOS depuis le 77, jusqu’au 84

  #### Description
  Cette stratégie ne fonctionne plus car WebDriver est désormais compatible avec l’ensemble des stratégies existantes

  Cette stratégie permet aux utilisateurs de la fonctionnalité WebDriver de remplacer
 des stratégies pouvant interférer avec son fonctionnement.

 Actuellement, cette stratégie désactive les stratégies [SitePerProcess](#siteperprocess) et [IsolateOrigins](#isolateorigins).

 Si la stratégie est activée, WebDriver peut remplacer les stratégies
incompatibles.
  Si la stratégie est désactivée ou n’est pas configurée, WebDriver n'est pas autorisé
 à remplacer les stratégies incompatibles.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: WebDriverOverridesIncompatiblePolicies
  - Nom de la stratégie de groupe: Autoriser WebDriver à remplacer les stratégies incompatibles (obsolète)
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: WebDriverOverridesIncompatiblePolicies
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: WebDriverOverridesIncompatiblePolicies
  - Exemple de valeur :
``` xml
<true/>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### WebRtcLocalIpsAllowedUrls
  #### Gérer l’exposition des adresses IP locales par WebRTC
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 80 ou version ultérieure

  #### Description
  Spécifie une liste d’origines (URL) ou de modèles de noms d’hôte (par exemple, « *contoso.com * ») pour laquelle l’adresse IP locale doit être exposée par WebRTC.

Si vous activez cette stratégie et définissez une liste d’origines (URL) ou des modèles de noms d’hôte, lorsque edge://flags/#enable-webrtc-hide-local-ips-with-mdns est activé, WebRTC expose l’adresse IP locale pour les cas qui correspondent aux modèles dans la liste.

Si vous désactivez cette stratégie ou si vous ne la configurez pas, et si edge://flags/#enable-webrtc-hide-local-ips-with-mdns est activé, WebRTC n’expose pas les adresses IP locales. L’adresse IP locale est cachée avec un nom d’hôte mDNS.

Si vous activez, désactivez ou ne configurez pas cette stratégie, et si edge://flags/#enable-webrtc-hide-local-ips-with-mdns est désactivé, WebRTC expose les adresses IP locales.

Veuillez noter que cette stratégie affaiblit la protection des adresses IP locales qui peuvent être nécessaires aux administrateurs.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Liste de chaînes

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: WebRtcLocalIpsAllowedUrls
  - Nom de la stratégie de groupe: Gérer l’exposition des adresses IP locales par WebRTC
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls
  - Chemin (Recommandé): N/A
  - Nom de la valeur: 1, 2, 3, ...
  - Type de la valeur: liste de REG_SZ
  ##### Exemple de valeur :
```
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\2 = "*contoso.com*"

```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: WebRtcLocalIpsAllowedUrls
  - Exemple de valeur :
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>*contoso.com*</string>
</array>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### WebRtcLocalhostIpHandling
  #### Limiter l’exposition de l’adresse IP locale par WebRTC
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Vous permet de déterminer si WebRTC expose l’adresse IP locale de l’utilisateur.

Si vous avez attribué la valeur « AllowAllInterfaces » ou « AllowPublicAndPrivateInterfaces » à cette stratégie, WebRTC présente l’adresse IP locale.

  Si vous avez attribué la valeur « AllowPublicInterfaceOnly » ou « DisableNonProxiedUdp » à cette stratégie, WebRTC n’expose pas l’adresse IP locale.

 Si vous ne configurez pas cette stratégie, ou si vous la désactivez, WebRTC expose l’adresse IP locale.

Mappage des options de stratégie :

* AllowAllInterfaces (default) = Autorisez toutes les interfaces. Ceci expose l’adresse IP locale

* AllowPublicAndPrivateInterfaces (default_public_and_private_interfaces) = Autoriser les interfaces publiques et privées sur l’itinéraire http par défaut. Ceci expose l’adresse IP locale

* AllowPublicInterfaceOnly (default_public_interface_only) = Autoriser l’interface publique sur l’itinéraire http par défaut. Ceci n’expose pas l’adresse IP locale

* DisableNonProxiedUdp (disable_non_proxied_udp) = Utiliser TCP, sauf si le serveur proxy prend en charge UDP. Ceci n’expose pas l’adresse IP locale

Utilisez les informations ci-dessus lors de la configuration de cette stratégie.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: WebRtcLocalhostIpHandling
  - Nom de la stratégie de groupe: Limiter l’exposition de l’adresse IP locale par WebRTC
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: WebRtcLocalhostIpHandling
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"default"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: WebRtcLocalhostIpHandling
  - Exemple de valeur :
``` xml
<string>default</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### WebRtcUdpPortRange
  #### Limiter la plage de ports UDP locaux utilisés par WebRTC
  
  
  #### Versions prises en charge :
  - Sur Windows et macOS dans la mesure où 77 ou version ultérieure

  #### Description
  Limite la plage de ports UDP utilisée par WebRTC à un intervalle de ports spécifié (points de terminaison inclus).

En configurant cette stratégie, vous spécifiez la plage de ports UDP locaux que WebRTC peut utiliser.

Si vous ne configurez pas cette stratégie ou si vous définissez une chaîne vide ou une plage de ports non valide, WebRTC peut utiliser n’importe quel port UDP local disponible.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Chaîne

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: WebRtcUdpPortRange
  - Nom de la stratégie de groupe: Limiter la plage de ports UDP locaux utilisés par WebRTC
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: WebRtcUdpPortRange
  - Type de la valeur: REG_SZ
  ##### Exemple de valeur :
```
"10000-11999"
```


  #### Paramètres et informations Mac
  - Nom de la clé de préférence: WebRtcUdpPortRange
  - Exemple de valeur :
``` xml
<string>10000-11999</string>
```
  

  [Revenir au début](#microsoft-edge---stratégies)

  ### WinHttpProxyResolverEnabled
  #### Utiliser le programme de résolution du proxy Windows (déconseillé)
  >DÉCONSEILLÉ : cette stratégie est déconseillée. Elle est actuellement prise en charge, mais deviendra obsolète dans une prochaine version.
  
  #### Versions prises en charge :
  - Sur Windows depuis 84 ou ultérieur

  #### Description
  Cette stratégie est déconseillée, car elle sera remplacée par une fonctionnalité similaire dans une prochaine version. Consultez https://crbug.com/644030.

Utilisez Windows pour résoudre les proxys pour tout le réseau de navigateur, au lieu du programme de résolution proxy intégré à Microsoft Edge. Le programme de résolution de proxy Windows active les fonctionnalités de proxy Windows telles que DirectAccess/NRPT.

Cette stratégie inclut les problèmes décrits par https://crbug.com/1032820. Elle entraîne l’extraction et l’exécution des fichiers PAC par le code Windows, y compris les fichiers PAC définis par l’intermédiaire de la stratégie [ProxyPacUrl](#proxypacurl). Étant donné que les récupérations de réseau pour le fichier PAC se produisent par le biais de Windows au lieu du code Microsoft Edge, les stratégies réseau telles que [DnsOverHttpsMode](#dnsoverhttpsmode) ne s’appliquent pas aux récupérations de réseau pour un fichier PAC.

Si vous activez cette stratégie, le programme de résolution de proxy Windows est utilisé.

Si vous désactivez ou omettez de configurer cette stratégie, le programme de résolution de proxy Microsoft Edge est utilisé.

  #### Fonctionnalités prises en charge :
  - Peut être obligatoire: Oui
  - Peut être recommandé(e): Non
  - Actualisation de la stratégie dynamique: Non - Nécessite le redémarrage du navigateur

  #### Type de données:
  - Booléen

  #### Informations et paramètres Windows
  ##### Informations sur la stratégie de groupe (ADMX)
  - Nom unique de stratégie de groupe: WinHttpProxyResolverEnabled
  - Nom de la stratégie de groupe: Utiliser le programme de résolution du proxy Windows (déconseillé)
  - Chemin d'accès à la stratégie de groupe (Obligatoire): Modèles d’administration/Microsoft Edge/
  - Chemin d'accès à la stratégie de groupe (Recommandé): N/A
  - Nom du fichier ADMX de stratégie de groupe: MSEdge.admx
  ##### Paramètres du Registre Windows
  - Chemin (Obligatoire): SOFTWARE\Policies\Microsoft\Edge
  - Chemin (Recommandé): N/A
  - Nom de la valeur: WinHttpProxyResolverEnabled
  - Type de la valeur: REG_DWORD
  ##### Exemple de valeur :
```
0x00000001
```


  

  [Revenir au début](#microsoft-edge---stratégies)


## Voir aussi
- [Configuration de Microsoft Edge](configure-microsoft-edge.md)
- [Page d’arrivée de Microsoft Edge Entreprise](https://aka.ms/EdgeEnterprise)
- [Blog des Bases de référence de sécurité Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)