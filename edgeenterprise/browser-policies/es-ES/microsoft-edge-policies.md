---
title: "Microsoft Edge Browser Policy Documentation"
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 09/28/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom:
description: "Windows and Mac documentation for all policies supported by the Microsoft Edge Browser"
---

# Microsoft Edge: directivas
La versión más reciente de Microsoft Edge incluye las siguientes directivas. Puedes usar estas directivas para configurar cómo se ejecuta Microsoft Edge en la organización.

Para más información sobre un conjunto adicional de directivas usadas para controlar cómo y cuándo se actualiza Microsoft Edge, consulta [Referencia de la directiva de Microsoft Edge Update](microsoft-edge-update-policies.md).

Puedes descargar el [Kit de herramientas del cumplimiento de la seguridad de Microsoft](https://www.microsoft.com/download/details.aspx?id=55319) para obtener la configuración de seguridad recomendada para Microsoft Edge. Para más información, consulta [Blog de bases de referencia de seguridad de Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines).

> [!NOTA]
> Este artículo se aplica a Microsoft Edge versión 77 o posterior.

## Directivas disponibles
En estas tablas se muestra una lista de todas las directivas de grupo relacionadas con el explorador disponibles en esta versión de Microsoft Edge. Utilice los vínculos de la tabla para obtener más detalles sobre directivas específicas.

|||
|-|-|
|[Administrador de contraseñas y protección](#administrador-de-contraseñas-y-protección)|[Autenticación HTTP](#autenticación-http)|
|[Cast](#cast)|[Configuración de Protección de aplicaciones](#configuración-de-protección-de-aplicaciones)|
|[Configuración de SmartScreen](#configuración-de-smartscreen)|[Configuración de contenido](#configuración-de-contenido)|
|[Configuración del modo de pantalla completa](#configuración-del-modo-de-pantalla-completa)|[Extensiones](#extensiones)|
|[Imprimir](#imprimir)|[Inicio, página principal y página de la nueva pestaña](#inicio-página-principal-y-página-de-la-nueva-pestaña)|
|[Mensajería nativa](#mensajería-nativa)|[Proveedor de búsquedas predeterminado](#proveedor-de-búsquedas-predeterminado)|
|[Servidor proxy](#servidor-proxy)|[Additional](#additional)|


### [*Administrador de contraseñas y protección*](#administrador-de-contraseñas-y-protección-policies)
|Nombre de directiva|Título|
|-|-|
|[PasswordManagerEnabled](#passwordmanagerenabled)|Habilitar guardar contraseñas en el administrador de contraseñas|
|[PasswordMonitorAllowed](#passwordmonitorallowed)|Permitir que los usuarios sean alertados si sus contraseñas se encuentran inseguras|
|[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)|Configurar la URL de cambio de contraseña|
|[PasswordProtectionLoginURLs](#passwordprotectionloginurls)|Configura la lista de direcciones URL de inicio de sesión de la empresa donde el servicio de protección con contraseña debería capturar códigos hash con sal de una contraseña|
|[PasswordProtectionWarningTrigger](#passwordprotectionwarningtrigger)|Configurar desencadenador de advertencia de protección de contraseñas|
### [*Autenticación HTTP*](#autenticación-http-policies)
|Nombre de directiva|Título|
|-|-|
|[AllowCrossOriginAuthPrompt](#allowcrossoriginauthprompt)|Allow cross-origin HTTP Authentication prompts|
|[AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)|Especifica una lista de servidores a los que Microsoft Edge puede delegar credenciales de usuario|
|[AuthSchemes](#authschemes)|Esquemas de autenticación admitidos|
|[AuthServerAllowlist](#authserverallowlist)|Configurar lista de servidores de autenticación permitidos|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|Deshabilitar búsqueda de CNAME al negociar la autenticación Kerberos|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|Incluir el puerto no estándar en Kerberos SPN|
|[NtlmV2Enabled](#ntlmv2enabled)|Controlar si la autenticación NTLMv2 está habilitada|
### [*Cast*](#cast-policies)
|Nombre de directiva|Título|
|-|-|
|[EnableMediaRouter](#enablemediarouter)|Habilitar Google Cast|
|[ShowCastIconInToolbar](#showcasticonintoolbar)|Mostrar el icono de transmisión en la barra de herramientas|
### [*Configuración de Protección de aplicaciones*](#configuración-de-protección-de-aplicaciones-policies)
|Nombre de directiva|Título|
|-|-|
|[ApplicationGuardContainerProxy](#applicationguardcontainerproxy)|Servicio de contenedor de Protección de aplicaciones|
### [*Configuración de SmartScreen*](#configuración-de-smartscreen-policies)
|Nombre de directiva|Título|
|-|-|
|[PreventSmartScreenPromptOverride](#preventsmartscreenpromptoverride)|Impedir que se pasen por alto de Sm los avisos de SmartScreen de Microsoft Defender para sitios|
|[PreventSmartScreenPromptOverrideForFiles](#preventsmartscreenpromptoverrideforfiles)|Impedir que se omitan las advertencias de SmartScreen de Microsoft Defender sobre las descargas|
|[SmartScreenAllowListDomains](#smartscreenallowlistdomains)|Configurar la lista de dominios para los que SmartScreen de Microsoft Defender no desencadenará advertencias|
|[SmartScreenEnabled](#smartscreenenabled)|Configurar SmartScreen de Microsoft Defender|
|[SmartScreenForTrustedDownloadsEnabled](#smartscreenfortrusteddownloadsenabled)|Forzar las comprobaciones de SmartScreen de Microsoft Defender en las descargas de fuentes de confianza|
|[SmartScreenPuaEnabled](#smartscreenpuaenabled)|Configurar SmartScreen de Microsoft Defender para bloquear aplicaciones potencialmente no deseadas|
### [*Configuración de contenido*](#configuración-de-contenido-policies)
|Nombre de directiva|Título|
|-|-|
|[AutoSelectCertificateForUrls](#autoselectcertificateforurls)|Seleccionar automáticamente certificados de cliente para estos sitios|
|[CookiesAllowedForUrls](#cookiesallowedforurls)|Permitir cookies en sitios específicos|
|[CookiesBlockedForUrls](#cookiesblockedforurls)|Bloquear cookies en sitios específicos|
|[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)|Limitar las cookies de sitios web específicos a la sesión actual|
|[DefaultCookiesSetting](#defaultcookiessetting)|Configurar cookies|
|[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)|Controlar el uso de la API del sistema de archivos para leer|
|[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)|Controlar el uso de la API del sistema de archivos para escribir|
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|Configuración de geolocalización predeterminada|
|[DefaultImagesSetting](#defaultimagessetting)|Configuración predeterminada de imágenes|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|Controlar el uso de excepciones de contenido no seguro|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|Configuración predeterminada de JavaScript|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|Configuración de notificaciones predeterminada|
|[DefaultPluginsSetting](#defaultpluginssetting)|Configuración de Adobe Flash predeterminada|
|[DefaultPopupsSetting](#defaultpopupssetting)|Configuración de ventana emergente predeterminada|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|Controlar el uso de la API Web Bluetooth|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|Controlar el uso de la API WebUSB|
|[FileSystemReadAskForUrls](#filesystemreadaskforurls)|Permitir el acceso de lectura mediante la API del sistema de archivos en estos sitios|
|[FileSystemReadBlockedForUrls](#filesystemreadblockedforurls)|Bloquear el acceso de lectura mediante la API del sistema de archivos en estos sitios|
|[FileSystemWriteAskForUrls](#filesystemwriteaskforurls)|Permitir el acceso de escritura de archivos y directorios en estos sitios|
|[FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls)|Bloquear el acceso de escritura de archivos y directorios en estos sitios|
|[ImagesAllowedForUrls](#imagesallowedforurls)|Permitir imágenes en estos sitios|
|[ImagesBlockedForUrls](#imagesblockedforurls)|Bloquear imágenes en sitios específicos|
|[InsecureContentAllowedForUrls](#insecurecontentallowedforurls)|Permitir contenido no seguro en sitios especificados|
|[InsecureContentBlockedForUrls](#insecurecontentblockedforurls)|Bloquear contenido no seguro en sitios especificados|
|[JavaScriptAllowedForUrls](#javascriptallowedforurls)|Permitir JavaScript en sitios específicos|
|[JavaScriptBlockedForUrls](#javascriptblockedforurls)|Bloquear JavaScript en sitios específicos|
|[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)|Habilitar la configuración del comportamiento de cookies de SameSite heredadas predefinido|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist)|Revertir al comportamiento de SameSite heredado para cookies en sitios especificados|
|[NotificationsAllowedForUrls](#notificationsallowedforurls)|Permitir notificaciones en sitios específicos|
|[NotificationsBlockedForUrls](#notificationsblockedforurls)|Bloquear notificaciones en sitios específicos|
|[PluginsAllowedForUrls](#pluginsallowedforurls)|Permitir el complemento de Adobe Flash en sitios específicos|
|[PluginsBlockedForUrls](#pluginsblockedforurls)|Bloquear el complemento de Adobe Flash en sitios específicos|
|[PopupsAllowedForUrls](#popupsallowedforurls)|Permitir ventanas emergentes en sitios específicos|
|[PopupsBlockedForUrls](#popupsblockedforurls)|Bloquear ventanas emergentes en sitios específicos|
|[RegisteredProtocolHandlers](#registeredprotocolhandlers)|Registrar controladores de protocolo|
|[SpotlightExperiencesAndRecommendationsEnabled](#spotlightexperiencesandrecommendationsenabled)|Elige si los usuarios pueden recibir imágenes de fondo personalizadas y texto, sugerencias, notificaciones
y consejos para los servicios Microsoft|
|[WebUsbAllowDevicesForUrls](#webusballowdevicesforurls)|Conceder acceso a sitios específicos para conectarse a dispositivos USB específicos|
|[WebUsbAskForUrls](#webusbaskforurls)|Permitir WebUSB en sitios específicos|
|[WebUsbBlockedForUrls](#webusbblockedforurls)|Bloquear WebUSB en sitios específicos|
### [*Configuración del modo de pantalla completa*](#configuración-del-modo-de-pantalla-completa-policies)
|Nombre de directiva|Título|
|-|-|
|[KioskDeleteDownloadsOnExit](#kioskdeletedownloadsonexit)|Eliminar archivos descargados como parte de la sesión de quiosco cuando se cierra Microsoft Edge|
### [*Extensiones*](#extensiones-policies)
|Nombre de directiva|Título|
|-|-|
|[ExtensionAllowedTypes](#extensionallowedtypes)|Configurar tipos de extensiones permitidos|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|Permitir la instalación de extensiones específicas|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|Controlar las extensiones que no se pueden instalar|
|[ExtensionInstallForcelist](#extensioninstallforcelist)|Controlar las extensiones que se instalan en modo silencioso|
|[ExtensionInstallSources](#extensioninstallsources)|Configurar extensión y orígenes de instalación de script de usuario|
|[ExtensionSettings](#extensionsettings)|Configurar ajustes de administración de extensiones|
### [*Imprimir*](#imprimir-policies)
|Nombre de directiva|Título|
|-|-|
|[DefaultPrinterSelection](#defaultprinterselection)|Reglas de selección de impresora predeterminada|
|[PrintHeaderFooter](#printheaderfooter)|Imprimir encabezados y pies de página|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|Establecer la impresora predeterminada del sistema como la impresora predeterminada|
|[PrintingEnabled](#printingenabled)|Habilitar la impresión|
|[PrintingPaperSizeDefault](#printingpapersizedefault)|Tamaño de página de impresión predeterminado|
|[UseSystemPrintDialog](#usesystemprintdialog)|Imprimir usando el cuadro de diálogo de impresión|
### [*Inicio&comma; página principal y página de la nueva pestaña*](#inicio-página-principal-y-página-de-la-nueva-pestaña-policies)
|Nombre de directiva|Título|
|-|-|
|[HomepageIsNewTabPage](#homepageisnewtabpage)|Establecer la página de la nueva pestaña como página principal|
|[HomepageLocation](#homepagelocation)|Configurar la dirección URL de la página principal|
|[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)|Configurar los tipos de fondo permitidos para el nuevo diseño de página de pestañas|
|[NewTabPageCompanyLogo](#newtabpagecompanylogo)|Establecer el logotipo de la empresa en la nueva ficha (obsoleto)|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|Ocultar los sitios principales predeterminados de la página de la nueva pestaña|
|[NewTabPageLocation](#newtabpagelocation)|Configurar la dirección URL de la página de la nueva pestaña|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|Establecer vínculos rápidos a la página de la nueva pestaña|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|Habilitar la carga previa de la página de nueva pestaña para una representación más rápida|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|Configurar la experiencia de página de la nueva pestaña de Microsoft Edge|
|[RestoreOnStartup](#restoreonstartup)|Acción que se realizará al inicio|
|[RestoreOnStartupURLs](#restoreonstartupurls)|Sitios que se abrirán cuando se inicia el explorador|
|[ShowHomeButton](#showhomebutton)|Mostrar el botón Inicio en la barra de herramientas|
### [*Mensajería nativa*](#mensajería-nativa-policies)
|Nombre de directiva|Título|
|-|-|
|[NativeMessagingAllowlist](#nativemessagingallowlist)|Controlar qué hosts de mensajería nativos pueden usar los usuarios|
|[NativeMessagingBlocklist](#nativemessagingblocklist)|Configurar la lista de bloqueados de mensajes nativa|
|[NativeMessagingUserLevelHosts](#nativemessaginguserlevelhosts)|Permitir hosts de mensajería nativos de nivel de usuario (instalados sin permisos del administrador)|
### [*Proveedor de búsquedas predeterminado*](#proveedor-de-búsquedas-predeterminado-policies)
|Nombre de directiva|Título|
|-|-|
|[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)|Habilitar el proveedor de búsquedas predeterminado|
|[DefaultSearchProviderEncodings](#defaultsearchproviderencodings)|Codificaciones del proveedor de búsquedas predeterminado|
|[DefaultSearchProviderImageURL](#defaultsearchproviderimageurl)|Especifica la característica de búsqueda por imagen para el proveedor de búsquedas predeterminado|
|[DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams)|Parámetros para una dirección URL de imagen que usa POST|
|[DefaultSearchProviderKeyword](#defaultsearchproviderkeyword)|Palabra clave del proveedor de búsquedas predeterminado|
|[DefaultSearchProviderName](#defaultsearchprovidername)|Nombre del proveedor de búsquedas predeterminado|
|[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)|URL de búsqueda del proveedor de búsquedas predeterminado|
|[DefaultSearchProviderSuggestURL](#defaultsearchprovidersuggesturl)|URL del proveedor de búsqueda predeterminado para obtener sugerencias|
|[NewTabPageSearchBox](#newtabpagesearchbox)|Configurar la nueva experiencia del cuadro de búsqueda de página de pestañas|
### [*Servidor proxy*](#servidor-proxy-policies)
|Nombre de directiva|Título|
|-|-|
|[ProxyBypassList](#proxybypasslist)|Configurar reglas de omisión de proxy|
|[ProxyMode](#proxymode)|Configurar ajustes del servidor proxy|
|[ProxyPacUrl](#proxypacurl)|Establecer la dirección URL del archivo .pac del proxy|
|[ProxyServer](#proxyserver)|Configurar dirección o URL del servidor proxy|
|[ProxySettings](#proxysettings)|Configuración del proxy|
### [*Additional*](#additional-policies)
|Nombre de directiva|Título|
|-|-|
|[AddressBarMicrosoftSearchInBingProviderEnabled](#addressbarmicrosoftsearchinbingproviderenabled)|Habilitar la Búsqueda de Microsoft en las sugerencias de Bing en la barra de direcciones|
|[AdsSettingForIntrusiveAdsSites](#adssettingforintrusiveadssites)|Configuración de anuncios para sitios con anuncios intrusivos|
|[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory)|Habilitar la eliminación del explorador y el historial de descarga|
|[AllowFileSelectionDialogs](#allowfileselectiondialogs)|Permitir cuadros de diálogo de selección de archivos|
|[AllowPopupsDuringPageUnload](#allowpopupsduringpageunload)|Permite que una página muestre elementos emergentes durante su descarga|
|[AllowSurfGame](#allowsurfgame)|Permitir el juego de surf|
|[AllowSyncXHRInPageDismissal](#allowsyncxhrinpagedismissal)|Permitir que las páginas envíen solicitudes sincrónicas de XHR durante el descarte de páginas (en desuso)|
|[AllowTokenBindingForUrls](#allowtokenbindingforurls)|Configure la lista de sitios con los que Microsoft Edge intentará establecer un enlace de token.|
|[AllowTrackingForUrls](#allowtrackingforurls)|Configurar excepciones de prevención de seguimiento para sitios específicos|
|[AlternateErrorPagesEnabled](#alternateerrorpagesenabled)|Sugerir páginas similares cuando no se puede encontrar una página web|
|[AlwaysOpenPdfExternally](#alwaysopenpdfexternally)|Abrir siempre archivos PDF externamente|
|[AmbientAuthenticationInPrivateModesEnabled](#ambientauthenticationinprivatemodesenabled)|Habilitar la autenticación de ambiente para perfiles de invitados e InPrivate|
|[AppCacheForceEnabled](#appcacheforceenabled)|Permite que se vuelva a activar la función de AppCache, incluso si está desactivada de forma predeterminada.|
|[ApplicationLocaleValue](#applicationlocalevalue)|Establecer la configuración regional de aplicación|
|[AudioCaptureAllowed](#audiocaptureallowed)|Permitir o bloquear la captura de audio|
|[AudioCaptureAllowedUrls](#audiocaptureallowedurls)|Sitios que pueden acceder a dispositivos de captura de audio sin solicitar permiso|
|[AudioSandboxEnabled](#audiosandboxenabled)|Permitir la ejecución del espacio aislado de audio|
|[AutoImportAtFirstRun](#autoimportatfirstrun)|Importar automáticamente los datos y la configuración de otro explorador la primera vez que se ejecute|
|[AutoLaunchProtocolsFromOrigins](#autolaunchprotocolsfromorigins)|Defina una lista de protocolos que pueden iniciar una aplicación externa desde los orígenes enumerados sin preguntar al usuario|
|[AutoOpenAllowedForURLs](#autoopenallowedforurls)|URL donde se puede aplicar AutoOpenFileTypes|
|[AutoOpenFileTypes](#autoopenfiletypes)|Lista de tipos de archivo que se deben abrir automáticamente al descargarse|
|[AutofillAddressEnabled](#autofilladdressenabled)|Habilitar Autorrellenar para direcciones|
|[AutofillCreditCardEnabled](#autofillcreditcardenabled)|Habilitar Autorrellenar para tarjetas de crédito|
|[AutoplayAllowed](#autoplayallowed)|Permitir la reproducción automática de multimedia para sitios web|
|[BackgroundModeEnabled](#backgroundmodeenabled)|Continúa con la ejecución de aplicaciones en segundo plano después de cerrar Microsoft Edge|
|[BackgroundTemplateListUpdatesEnabled](#backgroundtemplatelistupdatesenabled)|Habilita actualizaciones en segundo plano para la lista de plantillas disponibles para Colecciones y otras características que usan plantillas.|
|[BingAdsSuppression](#bingadssuppression)|Bloquear todos los anuncios en los resultados de búsqueda de Bing|
|[BlockThirdPartyCookies](#blockthirdpartycookies)|Bloquear cookies de terceros|
|[BrowserAddProfileEnabled](#browseraddprofileenabled)|Habilitar la creación de perfiles desde el menú desplegable Identidad o la página de configuración|
|[BrowserGuestModeEnabled](#browserguestmodeenabled)|Habilitar el modo Invitado|
|[BrowserNetworkTimeQueriesEnabled](#browsernetworktimequeriesenabled)|Permitir consultas a un servicio de hora de red de explorador|
|[BrowserSignin](#browsersignin)|Configuración de inicio de sesión del explorador|
|[BuiltInDnsClientEnabled](#builtindnsclientenabled)|Usar el cliente DNS integrado|
|[BuiltinCertificateVerifierEnabled](#builtincertificateverifierenabled)|Determina si se usará el comprobador de certificados integrado para comprobar los certificados de servidor (en desuso)|
|[CertificateTransparencyEnforcementDisabledForCas](#certificatetransparencyenforcementdisabledforcas)|Deshabilitar el cumplimiento de la transparencia de certificados para obtener una lista de hashes subjectPublicKeyInfo|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](#certificatetransparencyenforcementdisabledforlegacycas)|Deshabilitar la aplicación de la transparencia de certificados para una lista de entidades de certificación heredadas|
|[CertificateTransparencyEnforcementDisabledForUrls](#certificatetransparencyenforcementdisabledforurls)|Deshabilitar el cumplimiento de transparencia de certificados para direcciones URL específicas|
|[ClearBrowsingDataOnExit](#clearbrowsingdataonexit)|Borrar los datos de exploración al cerrar Microsoft Edge|
|[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)|Borrar archivos e imágenes en caché al cerrar Microsoft Edge|
|[ClickOnceEnabled](#clickonceenabled)|Permitir a los usuarios abrir archivos con el protocolo ClickOnce|
|[CollectionsServicesAndExportsBlockList](#collectionsservicesandexportsblocklist)|Bloquear el acceso a una lista específica de servicios y destinos de exportación en colecciones|
|[CommandLineFlagSecurityWarningsEnabled](#commandlineflagsecuritywarningsenabled)|Habilitar advertencias de seguridad para marcadores de la línea de comandos|
|[ComponentUpdatesEnabled](#componentupdatesenabled)|Habilitar actualizaciones de componentes en Microsoft Edge|
|[ConfigureDoNotTrack](#configuredonottrack)|Configurar No realizar seguimiento|
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|Configurar el inicio de sesión automático con una cuenta de dominio de Active Directory cuando no hay ninguna cuenta de dominio de Azure AD|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|Configurar texto a voz en línea|
|[ConfigureShare](#configureshare)|Configurar la experiencia de uso compartido|
|[CustomHelpLink](#customhelplink)|Especificar vínculo de ayuda personalizado|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|Comprobaciones de interceptación de DNS habilitadas|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|Establecer Microsoft Edge como el explorador predeterminado|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|Permitir acceso de búsqueda al menú contextual de proveedor de búsqueda predeterminado|
|[DefaultSensorsSetting](#defaultsensorssetting)|Configuración de sensores predeterminada|
|[DefaultSerialGuardSetting](#defaultserialguardsetting)|Controlar el uso de la API serie|
|[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)|Requerir que la lista de sitios del modo empresarial esté disponible antes que la exploración con tabulador.|
|[DeleteDataOnMigration](#deletedataonmigration)|Eliminar los datos antiguos del explorador durante la migración|
|[DeveloperToolsAvailability](#developertoolsavailability)|Controlar dónde se pueden usar las herramientas de desarrollo|
|[DiagnosticData](#diagnosticdata)|Enviar datos de diagnóstico necesarios y opcionales sobre el uso del explorador|
|[DirectInvokeEnabled](#directinvokeenabled)|Permitir a los usuarios abrir archivos con el protocolo DirectInvoke|
|[Disable3DAPIs](#disable3dapis)|Deshabilitar el soporte de las API de gráficos 3D|
|[DisableScreenshots](#disablescreenshots)|Deshabilitar la captura de pantalla|
|[DiskCacheDir](#diskcachedir)|Establecer el directorio de memoria caché del disco|
|[DiskCacheSize](#diskcachesize)|Establecer tamaño de caché de disco, en bytes|
|[DnsOverHttpsMode](#dnsoverhttpsmode)|Controlar el modo de DNS mediante HTTPS|
|[DnsOverHttpsTemplates](#dnsoverhttpstemplates)|Especificar la plantilla URI de la resolución de DNS mediante HTTPS que se prefiera|
|[DownloadDirectory](#downloaddirectory)|Establecer el directorio de descarga|
|[DownloadRestrictions](#downloadrestrictions)|Permitir restricciones de descarga|
|[EdgeCollectionsEnabled](#edgecollectionsenabled)|Habilitar la característica Colecciones|
|[EditFavoritesEnabled](#editfavoritesenabled)|Permite a los usuarios editar los favoritos|
|[EnableDeprecatedWebPlatformFeatures](#enabledeprecatedwebplatformfeatures)|Volver a habilitar las características de la plataforma web en desuso durante un tiempo limitado|
|[EnableDomainActionsDownload](#enabledomainactionsdownload)|Habilitar la descarga de acciones de dominio desde Microsoft (obsoleto)|
|[EnableOnlineRevocationChecks](#enableonlinerevocationchecks)|Habilitar comprobaciones de CRL/OCSP en línea|
|[EnableSha1ForLocalAnchors](#enablesha1forlocalanchors)|Permitir certificados firmados con SHA-1 al emitirlos por anclajes de veracidad local (en desuso)|
|[EnterpriseHardwarePlatformAPIEnabled](#enterprisehardwareplatformapienabled)|Permitir que las extensiones administradas usen la API de la plataforma de hardware empresarial|
|[EnterpriseModeSiteListManagerAllowed](#enterprisemodesitelistmanagerallowed)|Permitir el acceso a la herramienta Enterprise Mode Site List Manager|
|[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](#exemptdomainfiletypepairsfromfiletypedownloadwarnings)|Deshabilitar las advertencias basadas en la extensión de tipo de archivo de descarga para los tipos de archivo especificados en dominios|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|Controlar la comunicación con el servicio de configuración y experimentación|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox)|Mostrar una casilla "Abrir siempre" en el diálogo de protocolo externo|
|[FamilySafetySettingsEnabled](#familysafetysettingsenabled)|Permitir a los usuarios configurar Family Safety|
|[FavoritesBarEnabled](#favoritesbarenabled)|Habilitar barra de favoritos|
|[ForceBingSafeSearch](#forcebingsafesearch)|Aplicar Búsqueda segura de Bing|
|[ForceCertificatePromptsOnMultipleMatches](#forcecertificatepromptsonmultiplematches)|Configura si Microsoft Edge debe seleccionar automáticamente un certificado cuando haya varias coincidencias de certificados para un sitio configurado con "AutoSelectCertificateForUrls"|
|[ForceEphemeralProfiles](#forceephemeralprofiles)|Habilitar el uso de perfiles efímeros|
|[ForceGoogleSafeSearch](#forcegooglesafesearch)|Aplicar la Búsqueda segura de Google|
|[ForceLegacyDefaultReferrerPolicy](#forcelegacydefaultreferrerpolicy)|Use una directiva de referencia predeterminada de sin origen de referencia al degradar (en desuso)|
|[ForceNetworkInProcess](#forcenetworkinprocess)|Forzar el código de red para que se ejecute en el proceso del explorador (obsoleto)|
|[ForceSync](#forcesync)|Forzar la sincronización de los datos del explorador y no mostrar la solicitud de consentimiento de sincronización|
|[ForceYouTubeRestrict](#forceyoutuberestrict)|Forzar el modo Restringido mínimo en YouTube|
|[FullscreenAllowed](#fullscreenallowed)|Permitir modo de pantalla completa|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|Habilitar la caché de autenticación HTTP de ámbito global|
|[GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar)|Fuerce la navegación directa en el sitio de intranet en lugar de buscar entradas de una única palabra en la barra de direcciones.|
|[HSTSPolicyBypassList](#hstspolicybypasslist)|Configurar la lista de nombres que omitirán la comprobación de directiva de HSTS|
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|Usar aceleración de hardware cuando esté disponible|
|[HideFirstRunExperience](#hidefirstrunexperience)|Ocultar la experiencia de primera ejecución y la pantalla de presentación|
|[ImportAutofillFormData](#importautofillformdata)|Permitir la importación de datos de Autorrellenar del formulario|
|[ImportBrowserSettings](#importbrowsersettings)|Permitir la importación de la configuración del explorador|
|[ImportCookies](#importcookies)|Permitir la importación de cookies|
|[ImportExtensions](#importextensions)|Permitir la importación de extensiones|
|[ImportFavorites](#importfavorites)|Permitir la importación de favoritos|
|[ImportHistory](#importhistory)|Permitir la importación del historial de exploración|
|[ImportHomepage](#importhomepage)|Permitir la importación de la configuración de la página principal|
|[ImportOpenTabs](#importopentabs)|Permitir la importación de pestañas abiertas|
|[ImportPaymentInfo](#importpaymentinfo)|Permitir la importación de información de pago|
|[ImportSavedPasswords](#importsavedpasswords)|Permitir la importación de contraseñas guardadas|
|[ImportSearchEngine](#importsearchengine)|Permitir la importación de la configuración del motor de búsqueda|
|[ImportShortcuts](#importshortcuts)|Permitir la importación de accesos directos|
|[InPrivateModeAvailability](#inprivatemodeavailability)|Configurar la disponibilidad del modo InPrivate|
|[InsecureFormsWarningsEnabled](#insecureformswarningsenabled)|Habilitar advertencias para formularios no seguros|
|[IntensiveWakeUpThrottlingEnabled](#intensivewakeupthrottlingenabled)|Controle la característica IntensiveWakeUpThrottling|
|[InternetExplorerIntegrationEnhancedHangDetection](#internetexplorerintegrationenhancedhangdetection)|Configure la detección de bloqueos mejorada para el modo de Internet Explorer|
|[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)|Configurar la integración de Internet Explorer|
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|Configurar la lista de sitios del modo de empresa|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|Especificar cómo se comportan las exploraciones "en la página" para sitios no configurados cuando se inician desde páginas en el modo de Internet Explorer|
|[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed)|Permitir prueba de modo de Internet Explorer|
|[IsolateOrigins](#isolateorigins)|Habilitar el aislamiento de sitios para orígenes específicos|
|[LocalProvidersEnabled](#localprovidersenabled)|Permitir sugerencias de proveedores locales|
|[ManagedFavorites](#managedfavorites)|Configurar favoritos|
|[ManagedSearchEngines](#managedsearchengines)|Administrar motores de búsqueda|
|[MaxConnectionsPerProxy](#maxconnectionsperproxy)|Número máximo de conexiones simultáneas al servidor proxy|
|[MediaRouterCastAllowAllIPs](#mediaroutercastallowallips)|Permitir que Google Cast se conecte con dispositivos de Cast en todas las direcciones IP|
|[MetricsReportingEnabled](#metricsreportingenabled)|Habilitar el uso y los informes de datos relacionados con el bloqueo (en desuso)|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|Habilitar la oclusión de ventana nativa|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|Establece un tiempo de espera de retardo en la navegación por la etiqueta de la Lista de sitios de Modo de empresa|
|[NetworkPredictionOptions](#networkpredictionoptions)|Habilitar la predicción de red|
|[NonRemovableProfileEnabled](#nonremovableprofileenabled)|Configurar si un usuario siempre tiene un perfil predeterminado con sesión iniciada automáticamente con su cuenta profesional o educativa|
|[OverrideSecurityRestrictionsOnInsecureOrigin](#overridesecurityrestrictionsoninsecureorigin)|Controlar dónde se aplican restricciones de seguridad en los orígenes no seguros|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|Permitir que los sitios web consulten los métodos de pago disponibles|
|[PersonalizationReportingEnabled](#personalizationreportingenabled)|Permitir la personalización de anuncios, búsquedas y noticias mediante el envío del historial de exploración a Microsoft|
|[PinningWizardAllowed](#pinningwizardallowed)|Permitir el asistente de Anclar a la barra de tareas|
|[ProactiveAuthEnabled](#proactiveauthenabled)|Habilitar autenticación proactiva|
|[PromotionalTabsEnabled](#promotionaltabsenabled)|Habilitar el contenido promocional en toda la pestaña|
|[PromptForDownloadLocation](#promptfordownloadlocation)|Preguntar dónde guardar los archivos descargados|
|[QuicAllowed](#quicallowed)|Permitir protocolo QUIC|
|[RelaunchNotification](#relaunchnotification)|Notificar al usuario que se recomienda o se requiere reiniciar el explorador para las actualizaciones pendientes|
|[RelaunchNotificationPeriod](#relaunchnotificationperiod)|Establecer el período de tiempo para las notificaciones de actualización|
|[RendererCodeIntegrityEnabled](#renderercodeintegrityenabled)|Habilitar la integridad del código del procesador|
|[RequireOnlineRevocationChecksForLocalAnchors](#requireonlinerevocationchecksforlocalanchors)|Especificar si las comprobaciones CRL/OCSP en línea son obligatorias para los delimitadores locales de confianza|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|Habilitar la resolución de errores de navegación mediante un servicio web|
|[RestrictSigninToPattern](#restrictsignintopattern)|Restringir las cuentas que pueden usarse como cuentas principales de Microsoft Edge|
|[RoamingProfileLocation](#roamingprofilelocation)|Establecer el directorio de perfiles de itinerancia|
|[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)|Habilitar el uso de copias de itinerancia para los datos de perfil de Microsoft Edge|
|[RunAllFlashInAllowMode](#runallflashinallowmode)|Extender la configuración de contenidos de Adobe Flash a todos los contenido|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|Permitir que los usuarios continúen desde la página de advertencia de HTTPS|
|[SSLVersionMin](#sslversionmin)|Versión mínima de TLS habilitada|
|[SaveCookiesOnExit](#savecookiesonexit)|Guardar cookies cuando se cierre Microsoft Edge|
|[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)|Deshabilitar guardar el historial del explorador|
|[ScreenCaptureAllowed](#screencaptureallowed)|Permitir o denegar captura de pantalla|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|Habilitar el desplazamiento del texto especificado en los segmentos de la dirección URL|
|[SearchSuggestEnabled](#searchsuggestenabled)|Habilitar sugerencias de búsqueda|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|Sitios web o dominios que no necesitan permiso para usar la atestación de clave de seguridad directa|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|Enviar todos los sitios de la intranet a Internet Explorer|
|[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)|Enviar información del sitio para mejorar los servicios Microsoft (en desuso)|
|[SensorsAllowedForUrls](#sensorsallowedforurls)|Permitir el acceso a sensores en sitios específicos|
|[SensorsBlockedForUrls](#sensorsblockedforurls)|Bloquear el acceso a los sensores en sitios específicos|
|[SerialAskForUrls](#serialaskforurls)|Permitir la API serie en sitios específicos|
|[SerialBlockedForUrls](#serialblockedforurls)|Bloquear la API serie en sitios específicos|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|Mostrar el acceso directo de Microsoft Office en la barra de favoritos (en desuso)|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|Habilitar la compatibilidad con Exchange firmado de HTTP (SXG)|
|[SitePerProcess](#siteperprocess)|Habilitar el aislamiento de sitios para cada sitio|
|[SpellcheckEnabled](#spellcheckenabled)|Habilitar corrector ortográfico|
|[SpellcheckLanguage](#spellchecklanguage)|Habilitar los idiomas de corrección ortográfica específicos|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|Forzar deshabilitar idiomas de corrección ortográfica|
|[StricterMixedContentTreatmentEnabled](#strictermixedcontenttreatmentenabled)|Habilitar el tratamiento más estricto para el contenido mixto (en desuso)|
|[SuppressUnsupportedOSWarning](#suppressunsupportedoswarning)|Suprimir la advertencia de sistema operativo no compatible|
|[SyncDisabled](#syncdisabled)|Deshabilitar la sincronización de datos mediante los servicios de sincronización de Microsoft|
|[SyncTypesListDisabled](#synctypeslistdisabled)|Configurar la lista de tipos que están excluidos de la sincronización|
|[TLS13HardeningForLocalAnchorsEnabled](#tls13hardeningforlocalanchorsenabled)|Habilite una característica de seguridad de TLS 1.3 para anclajes locales de confianza. (obsoleto)|
|[TLSCipherSuiteDenyList](#tlsciphersuitedenylist)|Especificar los conjuntos de cifrado TLS para deshabilitar|
|[TabFreezingEnabled](#tabfreezingenabled)|Permitir la inmovilización de pestañas en segundo plano|
|[TaskManagerEndProcessEnabled](#taskmanagerendprocessenabled)|Habilitar finalizar procesos en el Administrador de tareas del explorador|
|[TotalMemoryLimitMb](#totalmemorylimitmb)|Establezca el límite de megabytes de memoria que puede usar una única instancia de Microsoft Edge.|
|[TrackingPrevention](#trackingprevention)|Bloquear el seguimiento de la actividad de exploración web de los usuarios|
|[TranslateEnabled](#translateenabled)|Habilitar Traducir|
|[URLAllowlist](#urlallowlist)|Definir una lista de direcciones URL permitidas|
|[URLBlocklist](#urlblocklist)|Bloquear el acceso a una lista de direcciones URL|
|[UserAgentClientHintsEnabled](#useragentclienthintsenabled)|Habilitar la característica de sugerencias del cliente del agente de usuario (en desuso)|
|[UserDataDir](#userdatadir)|Establecer el directorio de datos de usuario|
|[UserDataSnapshotRetentionLimit](#userdatasnapshotretentionlimit)|Limita el número de instantáneas de datos de usuario que se conservan para su uso en caso de reversión de emergencia|
|[UserFeedbackAllowed](#userfeedbackallowed)|Permitir comentarios del usuario|
|[VideoCaptureAllowed](#videocaptureallowed)|Permitir o bloquear la captura de vídeo|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|Sitios que pueden acceder a dispositivos de captura de vídeo sin solicitar permiso|
|[WPADQuickCheckEnabled](#wpadquickcheckenabled)|Establecer la optimización de WPAD|
|[WebAppInstallForceList](#webappinstallforcelist)|Configurar la lista de aplicaciones web instaladas por la fuerza|
|[WebComponentsV0Enabled](#webcomponentsv0enabled)|Vuelva a habilitar la API de Web Components v0 hasta M84 (obsoleto)|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|Permitir que WebDriver invalide las directivas incompatibles (obsoleto)|
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|Administrar la exposición de direcciones IP locales por WebRTC|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|Restringir la exposición de la dirección IP local por WebRTC|
|[WebRtcUdpPortRange](#webrtcudpportrange)|Restringir el intervalo de puertos UDP locales usados por WebRTC|
|[WinHttpProxyResolverEnabled](#winhttpproxyresolverenabled)|Usar resolución de proxy de Windows (en desuso)|




  ## Administrador de contraseñas y protección policies

  [Volver al principio](#microsoft-edge:-directivas)

  ### PasswordManagerEnabled
  #### Habilitar guardar contraseñas en el administrador de contraseñas
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Habilitar Microsoft Edge para guardar las contraseñas de usuario.

Si se habilita esta directiva, los usuarios pueden guardar sus contraseñas en Microsoft Edge. La próxima vez que visiten el sitio, Microsoft Edge introducirá automáticamente la contraseña.

Si se deshabilita esta directiva, los usuarios no pueden guardar nuevas contraseñas, pero pueden usar contraseñas guardadas con anterioridad.

Si se habilita o se deshabilita esta directiva, los usuarios no pueden cambiarla ni reemplazarla en Microsoft Edge. Si no se configura, los usuarios podrán guardar sus contraseñas y desactivar esta característica.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PasswordManagerEnabled
  - Nombre de la directiva de grupos: Habilitar guardar contraseñas en el administrador de contraseñas
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Administrador de contraseñas y protección
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Administrador de contraseñas y protección
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: PasswordManagerEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PasswordManagerEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PasswordMonitorAllowed
  #### Permitir que los usuarios sean alertados si sus contraseñas se encuentran inseguras
  
  
  #### Versiones admitidas:
  - En Windows desde 85 o posterior

  #### Descripción
  PermiteMicrosoft Edge controlar las contraseñas de los usuarios.

         Si habilita esta política y un usuario procede a habilitarla, el usuario recibirá una alerta si alguna de sus contraseñas almacenadas Microsoft Edgese encuentra insegura.Microsoft Edge mostrará una alerta y esta información también estará disponible en Configuración > Contraseñas > Monitor de contraseñas.

         Si se deshabilita esta directiva, no se pedirá permiso a los usuarios para activar esta función. Sus contraseñas no serán escaneadas y tampoco recibirán alertas.

         Si habilita o no configura la política, los usuarios pueden activar o desactivar esta función.

         Para obtener más información sobre cómo Microsoft Edge encuentra contraseñas inseguras, vea [https://go.microsoft.com/fwlink/?linkid=2133833](https://go.microsoft.com/fwlink/?linkid=2133833)

Directrices adicionales:

Esta directiva puede establecerse tanto como recomendada como obligatoria, aunque con una llamada importante.

         Habilitada como obligatoria: dado que el consentimiento del usuario individual es una condición previa para habilitar esta característica para un usuario determinado, esta directiva no tiene una configuración de habilitación obligatoria. Si la directiva se establece como Obligatoria habilitada, la interfaz de usuario en Configuración no cambiará y se mostrará el siguiente mensaje de error en el mensaje de estado de error de Edge://directiva

Ejemplo de estado de error: "Este valor de política se ignora porque el monitor de contraseñas requiere el consentimiento del usuario individual para ser activado. Puede pedir a los usuarios de su organización que vayan a Configuración > Perfil > Contraseña y activen la función".

         Habilitada como recomendada: si la directiva se establece como "Recomendada habilitada", la interfaz de usuario de Configuración permanecerá en estado "Desactivada", pero se hará visible un icono de un maletín junto a ella con esta descripción que se muestra al pasar el ratón por encima: "Su organización recomienda un valor específico para esta configuración y has elegido un valor diferente"

   Obligatorio y Recomendado deshabilitado: estos dos estados funcionarán de manera normal, con los subtítulos habituales que se muestran a los usuarios.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PasswordMonitorAllowed
  - Nombre de la directiva de grupos: Permitir que los usuarios sean alertados si sus contraseñas se encuentran inseguras
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Administrador de contraseñas y protección
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Administrador de contraseñas y protección
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: PasswordMonitorAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PasswordProtectionChangePasswordURL
  #### Configurar la URL de cambio de contraseña
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Configurar la URL de cambio de contraseña (solo para esquemas HTTP y HTTPS).

El servicio de protección de contraseñas enviará a los usuarios a esta URL para cambiar su contraseña después de ver una advertencia en el explorador.

Si habilita esta directiva, el servicio de protección de contraseñas enviará a los usuarios a esta URL para cambiar su contraseña.

Si deshabilita esta directiva o no la configura, el servicio de protección de contraseñas no redirigirá a los usuarios a una URL de cambio de contraseña.

Esta directiva solo está disponible en las instancias de Windows que estén unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise que estén inscritas para la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PasswordProtectionChangePasswordURL
  - Nombre de la directiva de grupos: Configurar la URL de cambio de contraseña
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Administrador de contraseñas y protección
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: PasswordProtectionChangePasswordURL
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"https://contoso.com/change_password.html"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PasswordProtectionChangePasswordURL
  - Valor de ejemplo:
``` xml
<string>https://contoso.com/change_password.html</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PasswordProtectionLoginURLs
  #### Configura la lista de direcciones URL de inicio de sesión de la empresa donde el servicio de protección con contraseña debería capturar códigos hash con sal de una contraseña
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Configure la lista de direcciones URL de inicio de sesión de la empresa (solo para esquemas HTTP y HTTPS) donde Microsoft Edge debería capturar los códigos hash con sal de las contraseñas y usarlos para la detección de reutilización de contraseñas.

Si habilita esta directiva, el servicio de protección con contraseña captura huellas digitales de las contraseñas en las direcciones URL definidas.

Si deshabilita esta directiva o no la configura, no se capturará ninguna huella digital de contraseña.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise que estén inscritas para la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PasswordProtectionLoginURLs
  - Nombre de la directiva de grupos: Configura la lista de direcciones URL de inicio de sesión de la empresa donde el servicio de protección con contraseña debería capturar códigos hash con sal de una contraseña
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Administrador de contraseñas y protección
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\1 = "https://contoso.com/login.html"
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\2 = "https://login.contoso.com"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PasswordProtectionLoginURLs
  - Valor de ejemplo:
``` xml
<array>
  <string>https://contoso.com/login.html</string>
  <string>https://login.contoso.com</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PasswordProtectionWarningTrigger
  #### Configurar desencadenador de advertencia de protección de contraseñas
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite controlar cuándo se debe desencadenar la advertencia de protección con contraseña. La protección con contraseña alerta a los usuarios cuando reutilizan su contraseña protegida en sitios potencialmente sospechosos.

Se pueden usar las directivas [PasswordProtectionLoginURLs](#passwordprotectionloginurls) y [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl) para configurar las contraseñas que se van a proteger.

Exenciones: las contraseñas de los sitios que aparecen en [PasswordProtectionLoginURLs](#passwordprotectionloginurls) y [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl), así como las de los sitios que aparecen en [SmartScreenAllowListDomains](#smartscreenallowlistdomains), no desencadenarán una advertencia de protección con contraseña.

Se debe establecer en 'PasswordProtectionWarningOff' para no mostrar advertencias de protección con contraseña.

Se debe establecer en 'PasswordProtectionWarningOnPasswordReuse'  para mostrar advertencias de protección con contraseña cuando el usuario reutiliza su contraseña protegida en un sitio no perteneciente a la lista de permitidos.

Si se deshabilita o no se configura esta directiva, no se mostrará el desencadenador de advertencia.

Asignación de opciones de directiva:

* PasswordProtectionWarningOff (0) = La advertencia de protección de contraseña está desactivada

* PasswordProtectionWarningOnPasswordReuse (1) = La advertencia de protección de contraseña está desencadenada por la reutilización de contraseñas

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PasswordProtectionWarningTrigger
  - Nombre de la directiva de grupos: Configurar desencadenador de advertencia de protección de contraseñas
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Administrador de contraseñas y protección
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: PasswordProtectionWarningTrigger
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PasswordProtectionWarningTrigger
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ## Autenticación HTTP policies

  [Volver al principio](#microsoft-edge:-directivas)

  ### AllowCrossOriginAuthPrompt
  #### Allow cross-origin HTTP Authentication prompts
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Controla si las imágenes de terceros de una página pueden mostrar un mensaje de autenticación.

Normalmente, esto se deshabilita como una defensa de suplantación de identidad. Si no se configura esta Directiva, se deshabilita y las imágenes de terceros no pueden mostrar un mensaje de autenticación.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AllowCrossOriginAuthPrompt
  - Nombre de la directiva de grupos: Allow cross-origin HTTP Authentication prompts
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Autenticación HTTP
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AllowCrossOriginAuthPrompt
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AllowCrossOriginAuthPrompt
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AuthNegotiateDelegateAllowlist
  #### Especifica una lista de servidores a los que Microsoft Edge puede delegar credenciales de usuario
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Configure la lista de servidores en los que puede delegar Microsoft Edge.

Separe los nombres de los distintos servidores con comas. Se permiten caracteres comodín (*).

Si no se configura esta directiva, Microsoft Edge no delegará las credenciales de usuario aunque se detecte un servidor como Intranet.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AuthNegotiateDelegateAllowlist
  - Nombre de la directiva de grupos: Especifica una lista de servidores a los que Microsoft Edge puede delegar credenciales de usuario
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Autenticación HTTP
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AuthNegotiateDelegateAllowlist
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"contoso.com"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AuthNegotiateDelegateAllowlist
  - Valor de ejemplo:
``` xml
<string>contoso.com</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AuthSchemes
  #### Esquemas de autenticación admitidos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica los esquemas de autenticación HTTP que se admiten.

Puede configurarse la directiva usando estos valores: 'basic', 'digest', 'ntlm' y 'negotiate'. Los valores múltiples deben estar separados por comas.

Si no se configura esta directiva, se usan los cuatro esquemas.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AuthSchemes
  - Nombre de la directiva de grupos: Esquemas de autenticación admitidos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Autenticación HTTP
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AuthSchemes
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"basic,digest,ntlm,negotiate"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AuthSchemes
  - Valor de ejemplo:
``` xml
<string>basic,digest,ntlm,negotiate</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AuthServerAllowlist
  #### Configurar lista de servidores de autenticación permitidos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica los servidores que se habilitarán para la autenticación integrada. La autenticación integrada solo se habilita cuando Microsoft Edge recibe un desafío de autenticación de un proxy o de un servidor en esta lista.

Separe los nombres de varios servidores con comas. Se permiten caracteres comodín (*).

Si no se configura esta directiva, Microsoft Edge intenta detectar si un servidor se encuentra en la intranet; solo entonces responderá a las solicitudes de IWA. Si el servidor está en Internet, Microsoft Edge omitirá las solicitudes de IWA.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AuthServerAllowlist
  - Nombre de la directiva de grupos: Configurar lista de servidores de autenticación permitidos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Autenticación HTTP
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AuthServerAllowlist
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"*contoso.com,contoso.com"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AuthServerAllowlist
  - Valor de ejemplo:
``` xml
<string>*contoso.com,contoso.com</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DisableAuthNegotiateCnameLookup
  #### Deshabilitar búsqueda de CNAME al negociar la autenticación Kerberos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Determina si el SPN de Kerberos generado se basa en el nombre DNS canónico (CNAME) o en el nombre original especificado.

Si se habilita esta directiva, se omitirá la búsqueda CNAME y se usará el nombre del servidor (como se indicó).

Si se deshabilita esta directiva o no se configura, se usará el nombre canónico del servidor. Esto se determina a través de la búsqueda CNAME.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DisableAuthNegotiateCnameLookup
  - Nombre de la directiva de grupos: Deshabilitar búsqueda de CNAME al negociar la autenticación Kerberos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Autenticación HTTP
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DisableAuthNegotiateCnameLookup
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DisableAuthNegotiateCnameLookup
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### EnableAuthNegotiatePort
  #### Incluir el puerto no estándar en Kerberos SPN
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica si el SPN Kerberos generado debe incluir un puerto no estándar.

Si se habilita esta directiva y un usuario incluye un puerto no estándar (es decir, un puerto distinto de 80 o 443) en una dirección URL, el puerto está incluido en el SPN Kerberos generado.

Si no se configura o se deshabilita esta directiva, el SPN Kerberos generado no incluirá un puerto en ningún caso.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: EnableAuthNegotiatePort
  - Nombre de la directiva de grupos: Incluir el puerto no estándar en Kerberos SPN
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Autenticación HTTP
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: EnableAuthNegotiatePort
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: EnableAuthNegotiatePort
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### NtlmV2Enabled
  #### Controlar si la autenticación NTLMv2 está habilitada
  
  
  #### Versiones admitidas:
  - En macOS desde 77 o posterior

  #### Descripción
  Controla si NTLMv2 está habilitado.

Todas las versiones recientes de los servidores Samba y Windows son compatibles con NTLMv2. Solo debe deshabilitar NTLMv2 para solucionar problemas con la compatibilidad con versiones anteriores, ya que reduce la seguridad de la autenticación.

Si no configura esta directiva, NTLMv2 estará habilitado de manera predeterminada.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  

  #### Información y configuración de Mac
  - Nombre de clave de preferencia: NtlmV2Enabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ## Cast policies

  [Volver al principio](#microsoft-edge:-directivas)

  ### EnableMediaRouter
  #### Habilitar Google Cast
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Habilitar esta directiva para habilitar Google Cast. Los usuarios podrán iniciarla desde el menú de aplicaciones, los menús contextuales de página, los controles de multimedia en sitios web habilitados para Cast y (si se muestra) el icono de la barra de herramientas de Cast.

Deshabilita esta directiva para deshabilitar Google Cast.

Google Cast está habilitado de forma predeterminada.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: EnableMediaRouter
  - Nombre de la directiva de grupos: Habilitar Google Cast
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Cast
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: EnableMediaRouter
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: EnableMediaRouter
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ShowCastIconInToolbar
  #### Mostrar el icono de transmisión en la barra de herramientas
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Establezca esta directiva en true para mostrar el icono de la barra de herramientas de conversión en la barra de herramientas o en el menú de desbordamiento. Los usuarios no podrán quitarlo.

Si no se configura esta directiva o se deshabilita, los usuarios podrán anclar o quitar el icono mediante su menú contextual.

Si también ha establecido la directiva [EnableMediaRouter](#enablemediarouter) en false, se omitirá esta directiva y no se mostrará el icono de la barra de herramientas.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ShowCastIconInToolbar
  - Nombre de la directiva de grupos: Mostrar el icono de transmisión en la barra de herramientas
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Cast
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ShowCastIconInToolbar
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ShowCastIconInToolbar
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ## Configuración de Protección de aplicaciones policies

  [Volver al principio](#microsoft-edge:-directivas)

  ### ApplicationGuardContainerProxy
  #### Servicio de contenedor de Protección de aplicaciones
  
  
  #### Versiones admitidas:
  - En Windows desde 84 o posterior

  #### Descripción
  Configura las opciones del servidor proxy para Protección de aplicaciones de Microsoft Edge.
Si habilitas esta directiva, Protección de aplicaciones de Microsoft Edge  pasará por alto otros orígenes de configuraciones de proxy.

Si no configuras esta directiva, Protección de aplicaciones de Microsoft Edge usará la configuración de proxy del host.

Esta directiva no afecta a la configuración de proxy de Microsoft Edge fuera de Protección de aplicaciones (en el host).

El campo ProxyMode te permite especificar el servidor proxy usado por Protección de aplicaciones de Microsoft Edge.

El campo ProxyPacUrl es la dirección URL de un archivo proxy. pac.

El campo ProxyServer es una dirección URL del servidor proxy.

Si eliges el valor 'direct' como 'ProxyMode', los demás campos se omiten.

Si eliges el valor 'auto_detect' como 'ProxyMode', los demás campos se omiten.

Si eliges el valor 'fixed_servers' como 'ProxyMode', se usará el campo 'ProxyServer'.

Si eliges el valor 'pac_script' como 'ProxyMode', se usará el campo 'ProxyPacUrl'.

Para más información sobre como identificar el tráfico de Protección de aplicaciones mediante proxy dual, visita [https://go.microsoft.com/fwlink/?linkid=2134653](https://go.microsoft.com/fwlink/?linkid=2134653).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Diccionario

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ApplicationGuardContainerProxy
  - Nombre de la directiva de grupos: Servicio de contenedor de Protección de aplicaciones
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de Protección de aplicaciones
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ApplicationGuardContainerProxy
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ## Configuración de SmartScreen policies

  [Volver al principio](#microsoft-edge:-directivas)

  ### PreventSmartScreenPromptOverride
  #### Impedir que se pasen por alto de Sm los avisos de SmartScreen de Microsoft Defender para sitios
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Esta configuración de directiva permite decidir si los usuarios pueden invalidar las advertencias de SmartScreen de Microsoft Defender sobre sitios web potencialmente malintencionados.

Si habilita esta configuración, los usuarios no podrán ignorar las advertencias de SmartScreen de Microsoft Defender y se les impedirá ir al sitio.

Si deshabilita o no establece esta configuración, los usuarios podrán ignorar las advertencias de SmartScreen de Microsoft Defender e ir al sitio.

Esta directiva solo está disponible en las instancias de Windows que estén unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise que estén inscritas para la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PreventSmartScreenPromptOverride
  - Nombre de la directiva de grupos: Impedir que se pasen por alto de Sm los avisos de SmartScreen de Microsoft Defender para sitios
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de SmartScreen
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: PreventSmartScreenPromptOverride
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PreventSmartScreenPromptOverride
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PreventSmartScreenPromptOverrideForFiles
  #### Impedir que se omitan las advertencias de SmartScreen de Microsoft Defender sobre las descargas
  
  
  #### Versiones admitidas:
  - En Windows desde 77 o posterior
  - En macOS desde 79 o posterior

  #### Descripción
  Esta directiva permite determinar si los usuarios pueden invalidar las advertencias de SmartScreen de Microsoft Defender sobre descargas no comprobadas.

Si habilita esta directiva, los usuarios de la organización no podrán ignorar las advertencias de SmartScreen de Microsoft Defender y se les impedirá completar las descargas no comprobadas.

Si deshabilita o no configura esta directiva, los usuarios podrán ignorar las advertencias de SmartScreen de Microsoft Defender y realizar descargas no comprobadas.

Esta directiva solo está disponible en las instancias de Windows que estén unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise que estén inscritas para la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PreventSmartScreenPromptOverrideForFiles
  - Nombre de la directiva de grupos: Impedir que se omitan las advertencias de SmartScreen de Microsoft Defender sobre las descargas
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de SmartScreen
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: PreventSmartScreenPromptOverrideForFiles
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PreventSmartScreenPromptOverrideForFiles
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SmartScreenAllowListDomains
  #### Configurar la lista de dominios para los que SmartScreen de Microsoft Defender no desencadenará advertencias
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Configurar la lista de dominios de confianza de SmartScreen de Microsoft Defender. Esto significa que:
SmartScreen de Microsoft Defender no comprobará recursos potencialmente malintencionados como software de suplantación de identidad (phishing) y otro malware si las direcciones URL de origen coinciden con estos dominios.
El servicio de protección de descargas de SmartScreen de Microsoft Defender no comprobará las descargas hospedadas en estos dominios.

Si habilita esta directiva, SmartScreen de Microsoft Defender confiará en estos dominios.
Si deshabilita o no establece esta directiva, la protección de SmartScreen de Microsoft Defender predeterminada se aplicará a todos los recursos.

Esta directiva solo está disponible en las instancias de Windows que estén unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise que estén inscritas para la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX.
Tenga en cuenta también que esta directiva no se aplicará si su organización ha habilitado la Protección contra amenazas avanzada de Microsoft Defender. En su lugar, debe configurar las listas de permitidos y bloqueados en el Centro de seguridad de Microsoft Defender.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SmartScreenAllowListDomains
  - Nombre de la directiva de grupos: Configurar la lista de dominios para los que SmartScreen de Microsoft Defender no desencadenará advertencias
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de SmartScreen
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\2 = "myuniversity.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SmartScreenAllowListDomains
  - Valor de ejemplo:
``` xml
<array>
  <string>mydomain.com</string>
  <string>myuniversity.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SmartScreenEnabled
  #### Configurar SmartScreen de Microsoft Defender
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Esta configuración de directiva permite configurar si se debe activar SmartScreen de Microsoft Defender. SmartScreen de Microsoft Defender proporciona mensajes de advertencia que ayudan a proteger a los usuarios contra posibles estafas de suplantación de identidad (phishing) y software malintencionado. De manera predeterminada, SmartScreen de Microsoft Defender está activado.

Si habilita esta configuración, SmartScreen de Microsoft Defender se activará.

Si deshabilita esta configuración, SmartScreen de Microsoft Defender se desactivará.

Si no establece esta configuración, los usuarios podrán elegir si desean usar SmartScreen de Microsoft Defender.

Esta directiva solo está disponible en las instancias de Windows que estén unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise que estén inscritas para la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SmartScreenEnabled
  - Nombre de la directiva de grupos: Configurar SmartScreen de Microsoft Defender
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de SmartScreen
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Configuración de SmartScreen
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: SmartScreenEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SmartScreenEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SmartScreenForTrustedDownloadsEnabled
  #### Forzar las comprobaciones de SmartScreen de Microsoft Defender en las descargas de fuentes de confianza
  
  
  #### Versiones admitidas:
  - En Windows desde 78 o posterior

  #### Descripción
  Esta configuración de directiva permite configurar si las comprobaciones de SmartScreen de Microsoft Defender descargan la reputación de un origen de confianza.

Si habilita o no establece esta configuración, SmartScreen de Microsoft Defender comprobará la reputación de la descarga independientemente del origen.

Si deshabilita esta configuración, SmartScreen de Microsoft Defender no comprobará la reputación de la descarga desde un origen de confianza.

Esta directiva solo está disponible en las instancias de Windows que están unidas a un dominio de Microsoft Active Directory, e instancias de Windows 10 Pro o Enterprise que estén inscritas para la administración de dispositivos.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SmartScreenForTrustedDownloadsEnabled
  - Nombre de la directiva de grupos: Forzar las comprobaciones de SmartScreen de Microsoft Defender en las descargas de fuentes de confianza
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de SmartScreen
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Configuración de SmartScreen
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: SmartScreenForTrustedDownloadsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SmartScreenPuaEnabled
  #### Configurar SmartScreen de Microsoft Defender para bloquear aplicaciones potencialmente no deseadas
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 80 o posterior

  #### Descripción
  Esta configuración de directiva permite establecer si se debe activar el bloqueo de aplicaciones potencialmente no deseadas en SmartScreen de Microsoft Defender. El bloqueo de aplicaciones potencialmente no deseadas en SmartScreen de Microsoft Defender proporciona mensajes de advertencia que ayudan a proteger a los usuarios contra adware, extractores de moneda, bundleware y otras aplicaciones de baja reputación que se hospedan en sitios web. El bloqueo de aplicaciones potencialmente no deseadas en SmartScreen de Microsoft Defender está desactivado de manera predeterminada.

Si habilita esta configuración, se activará el bloqueo de aplicaciones potencialmente no deseadas en SmartScreen de Microsoft Defender.

Si deshabilita esta configuración, se desactivará el bloqueo de aplicaciones potencialmente no deseadas en SmartScreen de Microsoft Defender.

Si no establece esta configuración, los usuarios podrán elegir si quieren usar el bloqueo de aplicaciones potencialmente no deseadas en SmartScreen de Microsoft Defender.

Esta directiva solo está disponible en las instancias de Windows que estén unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise que estén inscritas para la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SmartScreenPuaEnabled
  - Nombre de la directiva de grupos: Configurar SmartScreen de Microsoft Defender para bloquear aplicaciones potencialmente no deseadas
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de SmartScreen
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Configuración de SmartScreen
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: SmartScreenPuaEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SmartScreenPuaEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ## Configuración de contenido policies

  [Volver al principio](#microsoft-edge:-directivas)

  ### AutoSelectCertificateForUrls
  #### Seleccionar automáticamente certificados de cliente para estos sitios
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Setting the policy lets you make a list of URL patterns that specify sites for which Microsoft Edge can automatically select a client certificate. The value is an array of stringified JSON dictionaries, each with the form { "pattern": "$URL_PATTERN", "filter" : $FILTER }, where $URL_PATTERN is a content setting pattern. $FILTER restricts the client certificates the browser automatically selects from. Independent of the filter, only certificates that match the server's certificate request are selected.

Examples for the usage of the $FILTER section:

* When $FILTER is set to { "ISSUER": { "CN": "$ISSUER_CN" } }, only client certificates issued by a certificate with the CommonName $ISSUER_CN are selected.

* When $FILTER contains both the "ISSUER" and the "SUBJECT" sections, only client certificates that satisfy both conditions are selected.

* When $FILTER contains a "SUBJECT" section with the "O" value, a certificate needs at least one organization matching the specified value to be selected.

* When $FILTER contains a "SUBJECT" section with a "OU" value, a certificate needs at least one organizational unit matching the specified value to be selected.

* When $FILTER is set to {}, the selection of client certificates is not additionally restricted. Note that filters provided by the web server still apply.

If you leave the policy unset, there's no autoselection for any site.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AutoSelectCertificateForUrls
  - Nombre de la directiva de grupos: Seleccionar automáticamente certificados de cliente para estos sitios
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls\1 = "{\"pattern\":\"https://www.contoso.com\",\"filter\":{\"ISSUER\":{\"CN\":\"certificate issuer name\", \"L\": \"certificate issuer location\", \"O\": \"certificate issuer org\", \"OU\": \"certificate issuer org unit\"}, \"SUBJECT\":{\"CN\":\"certificate subject name\", \"L\": \"certificate subject location\", \"O\": \"certificate subject org\", \"OU\": \"certificate subject org unit\"}}}"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AutoSelectCertificateForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>{"pattern":"https://www.contoso.com","filter":{"ISSUER":{"CN":"certificate issuer name", "L": "certificate issuer location", "O": "certificate issuer org", "OU": "certificate issuer org unit"}, "SUBJECT":{"CN":"certificate subject name", "L": "certificate subject location", "O": "certificate subject org", "OU": "certificate subject org unit"}}}</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### CookiesAllowedForUrls
  #### Permitir cookies en sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Definir una lista de sitios, según los patrones de URL, con autorización para establecer cookies.

Si no se configura esta directiva, se usará el valor predeterminado global de la directiva [DefaultCookiesSetting](#defaultcookiessetting) (si se ha establecido) o de la configuración personal del usuario en todos los sitios.

Consulte las directivas [CookiesBlockedForUrls](#cookiesblockedforurls) y [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) para obtener más información.

Tenga en cuenta que no puede haber patrones de direcciones URL en conflicto establecidos entre estas tres directivas:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- CookiesAllowedForUrls

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

Para excluir cookies para que no se eliminen al salir, configure la directiva [SaveCookiesOnExit](#savecookiesonexit).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: CookiesAllowedForUrls
  - Nombre de la directiva de grupos: Permitir cookies en sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: CookiesAllowedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### CookiesBlockedForUrls
  #### Bloquear cookies en sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Defina una lista de sitios, según los patrones de URL, sin autorización para establecer cookies.

Si no se configura esta directiva, se usará el valor predeterminado global de la directiva [DefaultCookiesSetting](#defaultcookiessetting) (si se ha establecido) o de la configuración personal del usuario en todos los sitios.

Consulte las directivas [CookiesAllowedForUrls](#cookiesallowedforurls) y [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) para obtener más información.

Tenga en cuenta que no puede haber patrones de direcciones URL en conflicto establecidos entre estas tres directivas:

- CookiesBlockedForUrls

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: CookiesBlockedForUrls
  - Nombre de la directiva de grupos: Bloquear cookies en sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: CookiesBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### CookiesSessionOnlyForUrls
  #### Limitar las cookies de sitios web específicos a la sesión actual
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Las cookies creadas por sitios web que coinciden con un patrón de dirección URL que se defina se eliminan cuando finaliza la sesión (cuando se cierra la ventana).

Las cookies creadas por sitios web que no coinciden con el patrón están controladas por la directiva [DefaultCookiesSetting](#defaultcookiessetting) (si se ha establecido) o por la configuración personal del usuario. Este también es el comportamiento predeterminado si no configura esta directiva.

Si Microsoft Edge se ejecuta en modo de segundo plano, la sesión podría no cerrarse cuando se cierre la última ventana, lo que significa que las cookies no se borrarán cuando se cierre la ventana. Consulte la directiva [BackgroundModeEnabled](#backgroundmodeenabled) para obtener información sobre cómo configurar lo que sucede cuando Microsoft Edge se ejecuta en modo de segundo plano.

También puede usar las directivas [CookiesAllowedForUrls](#cookiesallowedforurls) y [CookiesBlockedForUrls](#cookiesblockedforurls) para controlar qué sitios web pueden crear cookies.

Tenga en cuenta que no puede haber patrones de direcciones URL en conflicto establecidos entre estas tres directivas:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- CookiesSessionOnlyForUrls

Si se establece la directiva [RestoreOnStartup](#restoreonstartup) para restaurar las direcciones URL de sesiones anteriores, esta directiva se ignorará y las cookies se almacenarán permanentemente para esos sitios.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: CookiesSessionOnlyForUrls
  - Nombre de la directiva de grupos: Limitar las cookies de sitios web específicos a la sesión actual
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: CookiesSessionOnlyForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultCookiesSetting
  #### Configurar cookies
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Controla si los sitios web pueden crear cookies en el dispositivo del usuario. Esta directiva es una cuestión de todo o nada: puedes permitir que todos los sitios web creen cookies o que ningún sitio web cree cookies. No puede usarse esta directiva para habilitar las cookies de sitios web específicos.

Establece la directiva en 'SessionOnly' para borrar las cookies cuando se cierre la sesión. Si Microsoft Edge se está ejecutando en modo de segundo plano, es posible que la sesión no se cierre al cerrar la última ventana, lo que significa que las cookies no se borrarán cuando se cierre la ventana. Consulta la directiva [BackgroundModeEnabled](#backgroundmodeenabled) para obtener información acerca de cómo configurar lo que ocurre cuando Microsoft Edge se ejecuta en modo en segundo plano.

Si no se configura esta directiva, se usará el valor predeterminado 'AllowCookies' (1) y los usuarios podrán cambiar este ajuste en la configuración de Microsoft Edge. (Si no quieres que los usuarios puedan cambiar esta configuración, establece la directiva).

Asignación de opciones de directiva:

* AllowCookies (1) = Permitir que todos los sitios creen cookies

* BlockCookies (2) = No permitir que ningún sitio cree cookies

* SessionOnly (4) = Conservar las cookies durante la sesión, excepto las que aparecen en [SaveCookiesOnExit](#savecookiesonexit)

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultCookiesSetting
  - Nombre de la directiva de grupos: Configurar cookies
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DefaultCookiesSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultCookiesSetting
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultFileSystemReadGuardSetting
  #### Controlar el uso de la API del sistema de archivos para leer
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Si establece esta directiva en 3, los sitios web pueden solicitar acceso de lectura al sistema de archivos del sistema operativo host mediante la API del sistema de archivos. Si establece esta directiva en 2, se deniega el acceso.

Si no establece esta directiva, los sitios web pueden pedir acceso. Los usuarios pueden cambiar esta configuración.

Asignación de opciones de directiva:

* BlockFileSystemRead (2) = No permitir que ningún sitio solicite acceso de lectura de archivos y directorios mediante la API del sistema de archivos

* AskFileSystemRead (3) = Permitir que los sitios soliciten al usuario que conceda acceso de lectura de archivos y directorios mediante la API del sistema de archivos

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultFileSystemReadGuardSetting
  - Nombre de la directiva de grupos: Controlar el uso de la API del sistema de archivos para leer
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DefaultFileSystemReadGuardSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultFileSystemReadGuardSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultFileSystemWriteGuardSetting
  #### Controlar el uso de la API del sistema de archivos para escribir
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Si establece esta directiva en 3, los sitios web pueden solicitar acceso de escritura al sistema de archivos del sistema operativo host mediante la API del sistema de archivos. Si establece esta directiva en 2, se deniega el acceso.

Si no establece esta directiva, los sitios web pueden pedir acceso. Los usuarios pueden cambiar esta configuración.

Asignación de opciones de directiva:

* BlockFileSystemWrite (2) = No permitir que ningún sitio solicite acceso de escritura de archivos y directorios

* AskFileSystemWrite (3) = Permitir que los sitios soliciten al usuario que conceda acceso de escritura de los archivos y directorios

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultFileSystemWriteGuardSetting
  - Nombre de la directiva de grupos: Controlar el uso de la API del sistema de archivos para escribir
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DefaultFileSystemWriteGuardSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultFileSystemWriteGuardSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultGeolocationSetting
  #### Configuración de geolocalización predeterminada
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Establece si los sitios web pueden realizar un seguimiento de la ubicación física de los usuarios. Puedes permitir el seguimiento de manera predeterminada ('AllowGeolocation'), denegarlo de manera predeterminada ('BlockGeolocation') o preguntar al usuario cada vez que un sitio web solicite su ubicación ('AskGeolocation').

Si no se configura esta directiva, se usa 'AskGeolocation' y el usuario puede cambiarla.

Asignación de opciones de directiva:

* AllowGeolocation (1) = Permitir que los sitios realicen un seguimiento de la ubicación física de los usuarios

* BlockGeolocation (2) = No permitir que ningún sitio realice un seguimiento de la ubicación física de los usuarios

* AskGeolocation (3) = Preguntar cuando un sitio quiera realizar un seguimiento de la ubicación física de los usuarios

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultGeolocationSetting
  - Nombre de la directiva de grupos: Configuración de geolocalización predeterminada
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DefaultGeolocationSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultGeolocationSetting
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultImagesSetting
  #### Configuración predeterminada de imágenes
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Establece si los sitios web pueden mostrar imágenes. Se pueden permitir imágenes en todos los sitios ('AllowImages') o bloquearlas en todos los sitios ('BlockImages').

Si no se configura esta directiva, se permiten imágenes de manera predeterminada y el usuario puede cambiar esta configuración.

Asignación de opciones de directiva:

* AllowImages (1) = Permitir que todos los sitios muestren todas las imágenes

* BlockImages (2) = No permitir que ningún sitio muestre imágenes

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultImagesSetting
  - Nombre de la directiva de grupos: Configuración predeterminada de imágenes
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DefaultImagesSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultImagesSetting
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultInsecureContentSetting
  #### Controlar el uso de excepciones de contenido no seguro
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 80 o posterior

  #### Descripción
  Le permite establecer si los usuarios pueden agregar excepciones para permitir contenido mixto en sitios específicos.

Esta directiva se puede reemplazar para patrones de direcciones URL específicas mediante las the [InsecureContentAllowedForUrls](#insecurecontentallowedforurls) y [InsecureContentBlockedForUrls](#insecurecontentblockedforurls).

Si no se establece esta directiva, los usuarios podrán agregar excepciones para permitir contenido mixto que se pueda bloquear y desactivar las actualizaciones automáticas para contenido mixto que se pueda bloquear.

Asignación de opciones de directiva:

* BlockInsecureContent (2) = No permitir que ningún sitio cargue contenido mixto

* AllowExceptionsInsecureContent (3) = Permitir que los usuarios añadan excepciones para permitir el contenido mixto

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultInsecureContentSetting
  - Nombre de la directiva de grupos: Controlar el uso de excepciones de contenido no seguro
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DefaultInsecureContentSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultInsecureContentSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultJavaScriptSetting
  #### Configuración predeterminada de JavaScript
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Establece si los sitios web pueden ejecutar JavaScript. Puede permitirse para todos los sitios ('AllowJavaScript') o bloquearse para todos los sitios ('BlockJavaScript').

Si no se configura esta directiva, todos los sitios pueden ejecutar JavaScript de manera predeterminada y el usuario puede cambiar esta configuración.

Asignación de opciones de directiva:

* AllowJavaScript (1) = Permitir que todos los sitios ejecuten JavaScript

* BlockJavaScript (2) = No permitir que ningún sitio ejecute JavaScript

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultJavaScriptSetting
  - Nombre de la directiva de grupos: Configuración predeterminada de JavaScript
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DefaultJavaScriptSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultJavaScriptSetting
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultNotificationsSetting
  #### Configuración de notificaciones predeterminada
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Establece si los sitios web pueden mostrar notificaciones de escritorio. Puedes permitirlos de manera predeterminada ('AllowNotifications'), denegarlos de manera predeterminada ('BlockNotifications') o preguntarle al usuario cada vez que un sitio web quiera mostrar una notificación ('AskNotifications').

Si no se configura esta directiva, se permitirán las notificaciones de manera predeterminada y el usuario podrá cambiar esta configuración.

Asignación de opciones de directiva:

* AllowNotifications (1) = Permitir que los sitios muestren notificaciones de escritorio

* BlockNotifications (2) = No permitir que ningún sitio muestre notificaciones de escritorio

* AskNotifications (3) = Preguntar siempre que un sitio desee mostrar notificaciones de escritorio

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultNotificationsSetting
  - Nombre de la directiva de grupos: Configuración de notificaciones predeterminada
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DefaultNotificationsSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultNotificationsSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultPluginsSetting
  #### Configuración de Adobe Flash predeterminada
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  [PluginsAllowedForUrls](#pluginsallowedforurls) y [PluginsBlockedForUrls](#pluginsblockedforurls) se comprueban primero y después, esta directiva. Las opciones son "ClickToPlay" y "BlockPlugins". Si establece esta directiva en "BlockPlugins", este complemento será denegado para todos los sitios web. "ClickToPlay" permite ejecutar el complemento Flash, pero los usuarios deben hacer clic en el marcador de posición para iniciarlo.

Si no define esta directiva, el usuario podrá cambiar esta configuración manualmente.

Nota: La reproducción automática es solo para los dominios enumerados explícitamente en la directiva [PluginsAllowedForUrls](#pluginsallowedforurls). Para activar la reproducción automática en todos los sitios, añada http://* y https://* a la lista de direcciones URL permitidas.

Asignación de opciones de directiva:

* BlockPlugins (2) = Bloquear el complemento de Adobe Flash

* ClickToPlay (3) = Haga clic para reproducir

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultPluginsSetting
  - Nombre de la directiva de grupos: Configuración de Adobe Flash predeterminada
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DefaultPluginsSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultPluginsSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultPopupsSetting
  #### Configuración de ventana emergente predeterminada
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Establece si los sitios web pueden mostrar ventanas emergentes. Pueden permitirse en todos los sitios web ('AllowPopups') o bloquearse en todos los sitios ('BlockPopups')

Si no se configura esta directiva, las ventanas emergentes se bloquearán de manera predeterminada y los usuarios podrán cambiar esta configuración.

Asignación de opciones de directiva:

* AllowPopups (1) = Permitir que todos los sitios muestren elementos emergentes

* BlockPopups (2) = No permitir que ningún sitio muestre elementos emergentes

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultPopupsSetting
  - Nombre de la directiva de grupos: Configuración de ventana emergente predeterminada
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DefaultPopupsSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultPopupsSetting
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultWebBluetoothGuardSetting
  #### Controlar el uso de la API Web Bluetooth
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Controla si los sitios web pueden acceder a dispositivos Bluetooth cercanos. Puedes bloquear completamente el acceso o requerir que el sitio pregunte al usuario cada vez que quiera obtener acceso a un dispositivo Bluetooth.

Si no configuras esta directiva, se usará el valor predeterminado ('AskWebBluetooth', lo que significa que se pregunta a los usuarios cada vez) y los usuarios podrán cambiarlo.

Asignación de opciones de directiva:

* BlockWebBluetooth (2) = No permitir que ningún sitio solicite acceso a dispositivos Bluetooth a través de la API web de Bluetooth

* AskWebBluetooth (3) = Permitir que los sitios soliciten al usuario que conceda acceso a un dispositivo Bluetooth cercano

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultWebBluetoothGuardSetting
  - Nombre de la directiva de grupos: Controlar el uso de la API Web Bluetooth
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DefaultWebBluetoothGuardSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultWebBluetoothGuardSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultWebUsbGuardSetting
  #### Controlar el uso de la API WebUSB
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Establece si los sitios web pueden tener acceso a dispositivos USB conectados. Puedes bloquear completamente el acceso o preguntar al usuario cada vez que un sitio web quiera obtener acceso a dispositivos USB conectados.

Puedes invalidar esta directiva para patrones de dirección URL específicos mediante las directivas [WebUsbAskForUrls](#webusbaskforurls) y [WebUsbBlockedForUrls](#webusbblockedforurls).

Si no configuras esta directiva, los sitios pueden preguntar a los usuarios si pueden obtener acceso a los dispositivos USB conectados ('AskWebUsb') de manera predeterminada y los usuarios pueden cambiar esta configuración.

Asignación de opciones de directiva:

* BlockWebUsb (2) = No permitir que ningún sitio solicite acceso a los dispositivos USB a través de la API WebUSB

* AskWebUsb (3) = Permitir que los sitios soliciten al usuario que conceda acceso a un dispositivo USB conectado

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultWebUsbGuardSetting
  - Nombre de la directiva de grupos: Controlar el uso de la API WebUSB
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DefaultWebUsbGuardSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultWebUsbGuardSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### FileSystemReadAskForUrls
  #### Permitir el acceso de lectura mediante la API del sistema de archivos en estos sitios
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Establecer la directiva le permite enumerar los patrones de dirección URL que especifican qué sitios pueden pedir a los usurarios la concesión de acceso de lectura de archivos o directorios del sistema de archivos del sistema operativo host mediante la API del sistema de archivos.

Si no establece esta directiva, [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) se aplica a todos los sitios, si se ha establecido. Si no, se aplica la configuración personal de los usuarios.

Los patrones de dirección URL no pueden entrar en conflicto con [FileSystemReadBlockedForUrls](#filesystemreadblockedforurls). Ninguna directiva tiene prioridad si una dirección URL coincide con ambos.

Para obtener información detallada sobre patrones de url válidos, consulte https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: FileSystemReadAskForUrls
  - Nombre de la directiva de grupos: Permitir el acceso de lectura mediante la API del sistema de archivos en estos sitios
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\2 = "[*.]example.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: FileSystemReadAskForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### FileSystemReadBlockedForUrls
  #### Bloquear el acceso de lectura mediante la API del sistema de archivos en estos sitios
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Si establece esta directiva, puede enumerar los patrones de dirección URL que especifican qué sitios no pueden pedir a los usurarios la concesión de acceso de lectura de archivos o directorios del sistema de archivos del sistema operativo host mediante la API del sistema de archivos.

Si no establece esta directiva, [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) se aplica a todos los sitios, si se ha establecido. Si no, se aplica la configuración personal de los usuarios.

Los patrones de dirección URL no pueden entrar en conflicto con [FileSystemReadAskForUrls](#filesystemreadaskforurls). Ninguna directiva tiene prioridad si una dirección URL coincide con ambos.

Para obtener información detallada sobre patrones de url válidos, consulte https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: FileSystemReadBlockedForUrls
  - Nombre de la directiva de grupos: Bloquear el acceso de lectura mediante la API del sistema de archivos en estos sitios
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\2 = "[*.]example.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: FileSystemReadBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### FileSystemWriteAskForUrls
  #### Permitir el acceso de escritura de archivos y directorios en estos sitios
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Si establece esta directiva, puede enumerar los patrones de dirección URL que especifican qué sitios pueden pedir a los usurarios la concesión de acceso de escritura de archivos o directorios del sistema de archivos del sistema operativo host.

Si no establece esta directiva, [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) se aplica a todos los sitios, si se ha establecido. Si no, se aplica la configuración personal de los usuarios.

Los patrones de dirección URL no pueden entrar en conflicto con [FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls). Ninguna directiva tiene prioridad si una dirección URL coincide con ambos.

Para obtener información detallada sobre patrones de url válidos, consulte https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: FileSystemWriteAskForUrls
  - Nombre de la directiva de grupos: Permitir el acceso de escritura de archivos y directorios en estos sitios
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\2 = "[*.]example.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: FileSystemWriteAskForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### FileSystemWriteBlockedForUrls
  #### Bloquear el acceso de escritura de archivos y directorios en estos sitios
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Si establece esta directiva, puede enumerar los patrones de dirección URL que especifican qué sitios no pueden pedir a los usurarios la concesión de acceso de escritura de archivos o directorios del sistema de archivos del sistema operativo host.

Si no establece esta directiva, [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) se aplica a todos los sitios, si se ha establecido. Si no, se aplica la configuración personal de los usuarios.

Los patrones de dirección URL no pueden entrar en conflicto con [FileSystemWriteAskForUrls](#filesystemwriteaskforurls). Ninguna directiva tiene prioridad si una dirección URL coincide con ambos.

Para obtener información detallada sobre patrones de url válidos, consulte https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: FileSystemWriteBlockedForUrls
  - Nombre de la directiva de grupos: Bloquear el acceso de escritura de archivos y directorios en estos sitios
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\2 = "[*.]example.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: FileSystemWriteBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ImagesAllowedForUrls
  #### Permitir imágenes en estos sitios
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Definir una lista de sitios, según los patrones de URL, que puedan mostrar imágenes.

Si no se configura esta directiva, se usará el valor predeterminado global en todos los sitios, ya sea de la directiva [DefaultImagesSetting](#defaultimagessetting) (si se ha establecido) o de la configuración personal del usuario.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ImagesAllowedForUrls
  - Nombre de la directiva de grupos: Permitir imágenes en estos sitios
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ImagesAllowedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ImagesBlockedForUrls
  #### Bloquear imágenes en sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Definir una lista de sitios, según los patrones de URL, que no puedan mostrar imágenes.

Si no se configura esta directiva, se usará el valor predeterminado global de la directiva [DefaultImagesSetting](#defaultimagessetting) (si se ha establecido) o de la configuración personal del usuario en todos los sitios.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ImagesBlockedForUrls
  - Nombre de la directiva de grupos: Bloquear imágenes en sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ImagesBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### InsecureContentAllowedForUrls
  #### Permitir contenido no seguro en sitios especificados
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 80 o posterior

  #### Descripción
  Cree una lista de patrones de direcciones URL para especificar sitios que pueden mostrar contenido mixto no seguro (es decir, contenido HTTP en sitios HTTPS).

Si no se configura esta directiva, el contenido mixto que se puede bloquear se bloqueará y se actualizará el contenido mixto con opción de bloqueo. Sin embargo, a los usuarios se les permitirá establecer excepciones para permitir contenido mixto no seguro para sitios específicos.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: InsecureContentAllowedForUrls
  - Nombre de la directiva de grupos: Permitir contenido no seguro en sitios especificados
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\2 = "[*.]example.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: InsecureContentAllowedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### InsecureContentBlockedForUrls
  #### Bloquear contenido no seguro en sitios especificados
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 80 o posterior

  #### Descripción
  Cree una lista de patrones de direcciones URL para especificar sitios que no pueden mostrar contenido mixto (es decir, contenido HTTP en sitios HTTPS) que se puede bloquear (es decir, activo) y para los que se desactivarán las actualizaciones de contenido mixto con opción de bloqueo.

Si no se establece esta directiva, se bloqueará el contenido mixto que se puede bloquear y se actualizará el contenido mixto con opción de bloqueo, y se permitirá que los usuarios establezcan excepciones para permitir contenido mixto no seguro en sitios específicos.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: InsecureContentBlockedForUrls
  - Nombre de la directiva de grupos: Bloquear contenido no seguro en sitios especificados
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\2 = "[*.]example.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: InsecureContentBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### JavaScriptAllowedForUrls
  #### Permitir JavaScript en sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Defina una lista de sitios, según los patrones de URL, que tienen permiso para ejecutar JavaScript.

Si no se configura esta directiva, se usará el valor predeterminado global de la directiva [DefaultJavaScriptSetting](#defaultjavascriptsetting) (si se ha establecido) o de la configuración personal del usuario en todos los sitios.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: JavaScriptAllowedForUrls
  - Nombre de la directiva de grupos: Permitir JavaScript en sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: JavaScriptAllowedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### JavaScriptBlockedForUrls
  #### Bloquear JavaScript en sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Defina una lista de sitios, según los patrones de URL, que no tienen permiso para ejecutar JavaScript.

Si no se configura esta directiva, se usará el valor predeterminado global de la directiva [DefaultJavaScriptSetting](#defaultjavascriptsetting) (si se ha establecido) o de la configuración personal del usuario en todos los sitios.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: JavaScriptBlockedForUrls
  - Nombre de la directiva de grupos: Bloquear JavaScript en sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: JavaScriptBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### LegacySameSiteCookieBehaviorEnabled
  #### Habilitar la configuración del comportamiento de cookies de SameSite heredadas predefinido
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 80 o posterior

  #### Descripción
  Lets you revert all cookies to legacy SameSite behavior. Reverting to legacy behavior causes cookies that don't specify a SameSite attribute to be treated as if they were "SameSite=None", removes the requirement for "SameSite=None" cookies to carry the "Secure" attribute, and skips the scheme comparison when evaluating if two sites are same-site.

If you don't set this policy, the default SameSite behavior for cookies will depend on other configuration sources for the SameSite-by-default feature, the Cookies-without-SameSite-must-be-secure feature, and the Schemeful Same-Site feature. These features can also be configured by a field trial or the same-site-by-default-cookies flag, the cookies-without-same-site-must-be-secure flag, or the schemeful-same-site flag in edge://flags.

Asignación de opciones de directiva:

* DefaultToLegacySameSiteCookieBehavior (1) = Revertir al comportamiento de SameSite heredado para las cookies en todos los sitios

* DefaultToSameSiteByDefaultCookieBehavior (2) = Usar el comportamiento de SameSite-by-default para las cookies en todos los sitios

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: LegacySameSiteCookieBehaviorEnabled
  - Nombre de la directiva de grupos: Habilitar la configuración del comportamiento de cookies de SameSite heredadas predefinido
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: LegacySameSiteCookieBehaviorEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: LegacySameSiteCookieBehaviorEnabled
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### LegacySameSiteCookieBehaviorEnabledForDomainList
  #### Revertir al comportamiento de SameSite heredado para cookies en sitios especificados
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 80 o posterior

  #### Descripción
  Cookies set for domains match specified patterns will revert to legacy SameSite behavior.

Reverting to legacy behavior causes cookies that don't specify a SameSite attribute to be treated as if they were "SameSite=None", removes the requirement for "SameSite=None" cookies to carry the "Secure" attribute, and skips the scheme comparison when evaluating if two sites are same-site.

If you don't set this policy, the global default value will be used. The global default will also be used for cookies on domains not covered by the patterns you specify.

The global default value can be configured using the [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) policy. If [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) is unset, the global default value falls back to other configuration sources.

Note that patterns you list in this policy are treated as domains, not URLs, so you should not specify a scheme or port.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Nombre de la directiva de grupos: Revertir al comportamiento de SameSite heredado para cookies en sitios especificados
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\1 = "www.example.com"
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\2 = "[*.]example.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Valor de ejemplo:
``` xml
<array>
  <string>www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### NotificationsAllowedForUrls
  #### Permitir notificaciones en sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite crear una lista de patrones de dirección URL para especificar los sitios a los que se permite mostrar notificaciones.

Si no establece esta directiva, se utilizará el valor predeterminado global para todos los sitios. Este valor predeterminado será de la directiva [DefaultNotificationsSetting](#defaultnotificationssetting) si está establecida o de la configuración personal del usuario. Para obtener información detallada sobre los patrones de url válidos, consulta [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: NotificationsAllowedForUrls
  - Nombre de la directiva de grupos: Permitir notificaciones en sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: NotificationsAllowedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### NotificationsBlockedForUrls
  #### Bloquear notificaciones en sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite crear una lista de patrones de dirección URL para especificar sitios a los que no se permite mostrar las notificaciones.

si no define esta Directiva, el valor predeterminado global se usará para todos los sitios de. Este valor predeterminado será de la Directiva de [DefaultNotificationsSetting](#defaultnotificationssetting) si está configurada o de la configuración personal del usuario. Para obtener información detallada sobre los patrones de dirección URL válidos, vea [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: NotificationsBlockedForUrls
  - Nombre de la directiva de grupos: Bloquear notificaciones en sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: NotificationsBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PluginsAllowedForUrls
  #### Permitir el complemento de Adobe Flash en sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Define una lista de sitios, basada en modelos de URL, que pueda ejecutar el complemento Adobe Flash.

Si no configuras esta directiva, el valor predeterminado global de la directiva [DefaultPluginsSetting](#defaultpluginssetting) (si está configurado) o la configuración personal del usuario se usa para todos los sitios.

Para información detallada sobre patrones de URL válidos, consulta [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Sin embargo, a partir de M85, los modelos con caracteres comodín '*' y '[*.]' en el host ya no son admitidos por esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PluginsAllowedForUrls
  - Nombre de la directiva de grupos: Permitir el complemento de Adobe Flash en sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\2 = "http://contoso.edu:8080"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PluginsAllowedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PluginsBlockedForUrls
  #### Bloquear el complemento de Adobe Flash en sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Define una lista de sitios, basada en modelos de URL, que tengan bloqueada la ejecución de Adobe Flash.

Si no configuras esta directiva, el valor predeterminado global de la directiva [DefaultPluginsSetting](#defaultpluginssetting) (si está configurado) o la configuración personal del usuario se usa para todos los sitios.

Para información detallada sobre patrones de URL válidos, consulta [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Sin embargo, a partir de M85, los modelos con caracteres comodín '*' y '[*.]' en el host ya no son admitidos por esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PluginsBlockedForUrls
  - Nombre de la directiva de grupos: Bloquear el complemento de Adobe Flash en sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\2 = "http://contoso.edu:8080"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PluginsBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PopupsAllowedForUrls
  #### Permitir ventanas emergentes en sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Definir una lista de sitios, según los patrones de URL, que puedan abrir ventanas emergentes.

Si no se configura esta directiva, se usará el valor predeterminado global de la directiva [DefaultPopupsSetting](#defaultpopupssetting) (si se ha establecido) o de la configuración personal del usuario en todos los sitios.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PopupsAllowedForUrls
  - Nombre de la directiva de grupos: Permitir ventanas emergentes en sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PopupsAllowedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PopupsBlockedForUrls
  #### Bloquear ventanas emergentes en sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Defina una lista de sitios, según los patrones de URL, que estén bloqueados y no puedan abrir ventanas emergentes.

Si no se configura esta directiva, se usará el valor predeterminado global de la directiva [DefaultPopupsSetting](#defaultpopupssetting) (si se ha establecido) o de la configuración personal del usuario en todos los sitios.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PopupsBlockedForUrls
  - Nombre de la directiva de grupos: Bloquear ventanas emergentes en sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PopupsBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### RegisteredProtocolHandlers
  #### Registrar controladores de protocolo
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Establece esta directiva (solo recomendado) para registrar una lista de controladores de protocolo. Esta lista se combina con la registrada por el usuario y ambas se pueden usar.

Para registrar un controlador de protocolo:

- Establece la propiedad de protocolo en el esquema (por ejemplo, "mailto")
- Establece la propiedad URL en la propiedad URL de la aplicación que controla el esquema especificado en el campo "protocolo". El patrón puede incluir un marcador de posición "%s" , que reemplaza la dirección URL tratada.

Los usuarios no pueden quitar un controlador de protocolo registrado por esta directiva. Sin embargo, pueden instalar un controlador de protocolo predeterminado nuevo para reemplazar los controladores de protocolo existentes.

  #### Características admitidas:
  - Puede ser obligatorio: No
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Diccionario

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: RegisteredProtocolHandlers
  - Nombre de la directiva de grupos: Registrar controladores de protocolo
  - Ruta de acceso de GP (Obligatorio): N/D
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Configuración de contenido
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): N/D
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: RegisteredProtocolHandlers
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [
  {
    "default": true, 
    "protocol": "mailto", 
    "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"
  }
]
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: RegisteredProtocolHandlers
  - Valor de ejemplo:
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
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SpotlightExperiencesAndRecommendationsEnabled
  #### Elige si los usuarios pueden recibir imágenes de fondo personalizadas y texto, sugerencias, notificaciones
y consejos para los servicios Microsoft
  
  
  #### Versiones admitidas:
  - En Windows desde 86 o posterior

  #### Descripción
  Elige si los usuarios pueden recibir imágenes de fondo personalizadas, texto, sugerencias, notificaciones y consejos para los servicios Microsoft.

Si habilitas o no estableces esta configuración, se activan las experiencias de destacados y las recomendaciones.

Si deshabilitas esta configuración, se desactivan las experiencias de destacados y las recomendaciones.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SpotlightExperiencesAndRecommendationsEnabled
  - Nombre de la directiva de grupos: Elige si los usuarios pueden recibir imágenes de fondo personalizadas y texto, sugerencias, notificaciones
y consejos para los servicios Microsoft
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: SpotlightExperiencesAndRecommendationsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### WebUsbAllowDevicesForUrls
  #### Conceder acceso a sitios específicos para conectarse a dispositivos USB específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite establecer una lista de direcciones URL que especifican los sitios a los que se concederá automáticamente permiso de acceso a un dispositivo USB con los id. del producto especificados. Cada elemento de la lista debe contener tanto dispositivos como direcciones URL para que la directiva sea válida. Cada elemento de los dispositivos puede contener un campo de id. de proveedor y id. del producto. Cualquier identificador que se omita se tratará como un comodín con una excepción y esa excepción es que no se puede especificar un id. del producto sin que también se especifique un id. de proveedor. De lo contrario, la directiva no será válida y se omitirá.

El modelo de permisos de USB usa la dirección URL del sitio que hace la solicitud ("URL de solicitud") y la dirección URL del sitio de marco de nivel superior ("URL de inserción") para conceder permiso de acceso a la dirección URL solicitante al dispositivo USB. La dirección URL solicitante puede ser distinta de la URL de inserción cuando el sitio solicitante se carga en un IFrame. Por este motivo, el campo "direcciones URL" puede contener dos cadenas URL, delimitadas por una coma, para especificar la dirección URL de solicitud e incrustación respectivamente. Si solo se especifica una dirección URL, se concederá el acceso a los dispositivos USB correspondientes cuando la dirección URL del sitio solicitante coincide con esta dirección URL, independientemente del estado de la incrustación. Por lo tanto, el campo "urls" puede contener hasta dos cadenas de direcciones URL delimitadas por una coma para especificar la dirección URL de solicitud e incrustación, respectivamente. Si solo se especifica una dirección URL, se concederá acceso a los dispositivos USB correspondientes cuando la dirección URL del sitio solicitante coincida con esta dirección URL, independientemente del estado de la incrustación. Las direcciones URL en "urls" deben ser direcciones URL válidas; de lo contrario, se omitirá la directiva.

Si no se establece esta directiva, se usará el valor predeterminado global para todos los sitios de la directiva [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting), si está establecida, o de la configuración personal del usuario si no lo está.

Los modelos de dirección URL de esta directiva no deben entrar en conflicto con los configurados a través de [WebUsbBlockedForUrls](#webusbblockedforurls). Si hay un conflicto, esta directiva tendrá prioridad sobre [WebUsbBlockedForUrls](#webusbblockedforurls) y [WebUsbAskForUrls](#webusbaskforurls).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Diccionario

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: WebUsbAllowDevicesForUrls
  - Nombre de la directiva de grupos: Conceder acceso a sitios específicos para conectarse a dispositivos USB específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: WebUsbAllowDevicesForUrls
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
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


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: WebUsbAllowDevicesForUrls
  - Valor de ejemplo:
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
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### WebUsbAskForUrls
  #### Permitir WebUSB en sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Define una lista de sitios, basada en patrones de URL, que pueden pedir al usuario acceso a un dispositivo USB

.          Si no configura esta directiva, se utiliza el valor predeterminado global de la directiva [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (si está establecido) o la configuración personal del usuario para todos los sitios.

Los patrones de URL definidos en esta directiva no pueden entrar en conflicto con los configurados en la directiva [WebUsbBlockedForUrls](#webusbblockedforurls); no se puede permitir ni bloquear una URL. Para obtener información detallada sobre los patrones de URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: WebUsbAskForUrls
  - Nombre de la directiva de grupos: Permitir WebUSB en sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: WebUsbAskForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### WebUsbBlockedForUrls
  #### Bloquear WebUSB en sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Define una lista de sitios, basada en patrones de URL, que pueden pedir al usuario acceso a un dispositivo USB.

Si no configura esta directiva, se utiliza el valor predeterminado global de la directiva [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (si está establecido) o la configuración personal del usuario para todos los sitios.

Los patrones de URL definidos en esta directiva no pueden entrar en conflicto con los configurados en la directiva [WebUsbAskForUrls](#webusbaskforurls). No puede permitir ni bloquear una URL. Para obtener información detallada sobre los patrones de URL válidos, vea [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: WebUsbBlockedForUrls
  - Nombre de la directiva de grupos: Bloquear WebUSB en sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración de contenido
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: WebUsbBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ## Configuración del modo de pantalla completa policies

  [Volver al principio](#microsoft-edge:-directivas)

  ### KioskDeleteDownloadsOnExit
  #### Eliminar archivos descargados como parte de la sesión de quiosco cuando se cierra Microsoft Edge
  
  
  #### Versiones admitidas:
  - En Windows desde 87 o posterior

  #### Descripción
  Nota: esta directiva solo se admite cuando se inicia Microsoft Edge con el parámetro de línea de comandos "--edge-kiosk-type".

Si habilitas esta directiva, los archivos descargados como parte de la sesión de quiosco se eliminan cada vez que se cierra Microsoft Edge.

Si deshabilitas esta directiva o no la configuras, los archivos descargados como parte de la sesión de quiosco no se eliminan cuando se cierra Microsoft Edge.

Para obtener información detallada sobre la configuración del modo quiosco, consulta [https://go.microsoft.com/fwlink/?linkid=2137578](https://go.microsoft.com/fwlink/?linkid=2137578).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: KioskDeleteDownloadsOnExit
  - Nombre de la directiva de grupos: Eliminar archivos descargados como parte de la sesión de quiosco cuando se cierra Microsoft Edge
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Configuración del modo de pantalla completa
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: KioskDeleteDownloadsOnExit
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ## Extensiones policies

  [Volver al principio](#microsoft-edge:-directivas)

  ### ExtensionAllowedTypes
  #### Configurar tipos de extensiones permitidos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Controla los tipos de extensión que se pueden instalar y limita el acceso en tiempo de ejecución.

Esta configuración define los tipos permitidos de extensiones y los hosts con los que pueden interactuar. El valor es una lista de cadenas, cada una de las cuales debe ser uno de los siguientes valores: "extensión", "theme", "user_script" y "hosted_app". Consulte la documentación de extensiones de Microsoft Edge para obtener más información sobre estos tipos.

Tenga en cuenta que esta directiva también afecta a que se fuerce la instalación de las extensiones mediante la directiva [ExtensionInstallForcelist](#extensioninstallforcelist).

Si se habilita esta directiva, se instalan solo las extensiones que coinciden con un tipo en la lista.

Si no se configura esta directiva, no se aplicarán restricciones en los tipos de extensión aceptables.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ExtensionAllowedTypes
  - Nombre de la directiva de grupos: Configurar tipos de extensiones permitidos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Extensiones
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes\1 = "hosted_app"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ExtensionAllowedTypes
  - Valor de ejemplo:
``` xml
<array>
  <string>hosted_app</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ExtensionInstallAllowlist
  #### Permitir la instalación de extensiones específicas
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  De manera predeterminada, se permiten todas las extensiones. Sin embargo, si bloquea todas las extensiones al establecer la directiva 'ExtensionInstallBlockList' en "*", los usuarios solo podrán instalar las extensiones definidas en esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ExtensionInstallAllowlist
  - Nombre de la directiva de grupos: Permitir la instalación de extensiones específicas
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Extensiones
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\2 = "extension_id2"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ExtensionInstallAllowlist
  - Valor de ejemplo:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ExtensionInstallBlocklist
  #### Controlar las extensiones que no se pueden instalar
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Lista de extensiones específicas que los usuarios NO pueden instalar en Microsoft Edge. Al implementar esta directiva, se deshabilitarán las extensiones de esta lista que se instalaron anteriormente y el usuario no podrá activarlos. Si se quita un elemento de la lista de extensiones bloqueadas, esta extensión se volverá a activar automáticamente en cualquier lugar en el que se instaló anteriormente.

Use "*" para bloquear todas las extensiones que no aparecen explícitamente en la lista de permitidos.

Si no se configura esta directiva, los usuarios pueden instalar cualquier extensión en Microsoft Edge.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ExtensionInstallBlocklist
  - Nombre de la directiva de grupos: Controlar las extensiones que no se pueden instalar
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Extensiones
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\2 = "extension_id2"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ExtensionInstallBlocklist
  - Valor de ejemplo:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ExtensionInstallForcelist
  #### Controlar las extensiones que se instalan en modo silencioso
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica extensiones que se instalan silenciosamente, sin interacción del usuario y que los usuarios no puedan desinstalar ni deshabilitar ("instalación forzada"). Todos los permisos solicitados por las extensiones se conceden de forma implícita, sin la interacción del usuario, incluidos los permisos adicionales solicitados por las versiones futuras de la extensión. Además, se conceden permisos para las API de las extensiones enterprise.deviceAttributes y enterprise.platformKeys (estas dos API solo están disponibles para extensiones que con instalación forzada).

Esta directiva tiene prioridad sobre una directiva [ExtensionInstallBlocklist](#extensioninstallblocklist) potencialmente conflictiva. Cuando quita una extensión de la lista de instalaciones forzadas, Microsoft Edge la desinstalará automáticamente.

La instalación forzada está limitada a aplicaciones y extensiones de la lista del sitio web de complementos de Microsoft Edge para las instancias siguientes: instancias de Windows que no estén unidas a un dominio de Microsoft Active Directory o instancias de Windows 10 Pro o Empresa que no estén inscritas en administración de dispositivos e instancias de macOS que no estén administradas mediante MDM o unidas a un dominio mediante MCX.

Tenga en cuenta que los usuarios pueden modificar el código fuente de cualquier extensión mediante las Herramientas de desarrollo, lo que podría representar la extensión como disfuncional. Si esto es un problema, establezca la directiva [DeveloperToolsAvailability](#developertoolsavailability).

Use el siguiente formato para agregar una extensión a la lista:

[extensionID];[updateURL]

- extensionID - la cadena de 32 letras que se encuentra en edge://extensions en el modo de desarrollador.

- updateURL (opcional) es la dirección del documento XML del manifiesto de actualización para la aplicación o extensión, como se describe en  [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043). Si desea instalar la extensión desde Chrome Web Store, proporcione la URL de actualización de Chrome Web Store, https://clients2.google.com/service/update2/crx. Tenga en cuenta que la dirección URL de actualización establecida en esta directiva solo se usa para la instalación inicial; las actualizaciones subsiguientes de la extensión usan la dirección URL de actualización indicada en el manifiesto de la extensión. Si no establece la URL de actualización, se asume que la extensión está hospedada en Microsoft Store y se usa la siguiente URL de actualización (https://edge.microsoft.com/extensionwebstorebase/v1/crx).

Por ejemplo, gggmmkjegpiggikcnhidnjjhmicpibll;https://edge.microsoft.com/extensionwebstorebase/v1/crx instala la aplicación Microsoft Online desde la dirección URL de "actualización" de Microsoft Store. Para obtener más información acerca de las extensiones de hospedaje, consulte: [https://go.microsoft.com/fwlink/?linkid=2095044](https://go.microsoft.com/fwlink/?linkid=2095044).

Si no se configura esta directiva, no se instalarán extensiones automáticamente y los usuarios podrán desinstalar cualquier extensión en Microsoft Edge.

Tenga en cuenta que esta directiva no se aplica al modo de InPrivate.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ExtensionInstallForcelist
  - Nombre de la directiva de grupos: Controlar las extensiones que se instalan en modo silencioso
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Extensiones
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\1 = "gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\2 = "abcdefghijklmnopabcdefghijklmnop"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ExtensionInstallForcelist
  - Valor de ejemplo:
``` xml
<array>
  <string>gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx</string>
  <string>abcdefghijklmnopabcdefghijklmnop</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ExtensionInstallSources
  #### Configurar extensión y orígenes de instalación de script de usuario
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Defina las URL que pueden instalar extensiones y temas.

De manera predeterminada, los usuarios tienen que descargar un archivo *.crx para cada extensión o script que deseen instalar y, a continuación, arrastrarlo a la página de configuración de Microsoft Edge. Esta directiva permite que las URL específicas instalen la extensión o script para el usuario.

Cada elemento de esta lista es un patrón de coincidencia de estilo de extensión (consulte [https://go.microsoft.com/fwlink/?linkid=2095039](https://go.microsoft.com/fwlink/?linkid=2095039)). Los usuarios pueden instalar fácilmente elementos de cualquier URL que coincida con un elemento de esta lista. Estos patrones deben permitir tanto la ubicación del archivo *.crx como la página en la que se inicie la descarga (es decir, la dirección de referencia).

La directiva [ExtensionInstallBlocklist](#extensioninstallblocklist) tiene prioridad sobre esta directiva. Las extensiones que se encuentren en la lista de bloqueados no se instalarán, aunque provengan de un sitio de la lista.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ExtensionInstallSources
  - Nombre de la directiva de grupos: Configurar extensión y orígenes de instalación de script de usuario
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Extensiones
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources\1 = "https://corp.contoso.com/*"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ExtensionInstallSources
  - Valor de ejemplo:
``` xml
<array>
  <string>https://corp.contoso.com/*</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ExtensionSettings
  #### Configurar ajustes de administración de extensiones
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Configura los ajustes de administración de extensiones para Microsoft Edge.

Esta directiva controla múltiples ajustes, incluidos los ajustes controlados por cualquier directiva existente relacionada con las extensiones. Esta directiva invalida cualquier directiva heredada si se establecen ambas.

Esta directiva asigna un id. de extensión o una URL de actualización a su configuración. Con un id. de extensión, la configuración se aplica solo a la extensión especificada. Establezca una configuración predeterminada para el id. especial "*", que se aplicará a todas las extensiones que no se indiquen específicamente en esta directiva. Con una URL de actualización, la configuración se aplica a todas las extensiones con la URL de actualización exacta establecida en el manifiesto de esta extensión, como se describe en [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Diccionario

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ExtensionSettings
  - Nombre de la directiva de grupos: Configurar ajustes de administración de extensiones
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Extensiones
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ExtensionSettings
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
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


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ExtensionSettings
  - Valor de ejemplo:
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
  

  [Volver al principio](#microsoft-edge:-directivas)

  ## Imprimir policies

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultPrinterSelection
  #### Reglas de selección de impresora predeterminada
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Invalida las reglas de selección de la impresora predeterminada de Microsoft Edge. Esta directiva determina las reglas para seleccionar la impresora predeterminada en Microsoft Edge, que ocurre la primera vez que un usuario intenta imprimir una página.

Cuando se establece esta directiva, Microsoft Edge intenta buscar una impresora que coincida con todos los atributos especificados y la usa como impresora predeterminada. Si hay varias impresoras que cumplan los criterios, se usará la primera impresora que coincida.

Si no se configura esta directiva o no se encuentra ninguna impresora coincidente en el tiempo de espera, la impresora será de manera predeterminada la impresora PDF integrada o ninguna impresora, si la impresora PDF no está disponible.

El valor se analiza como un objeto JSON, según el esquema siguiente: { "type": "object", "properties": { "idPattern": { "description": "Regular expression to match printer id.", "type": "string" }, "namePattern": { "description": "Regular expression to match printer display name.", "type": "string" } } }

Si se omite un campo, coincidirán todos los valores; por ejemplo, si no se especifica ninguna conectividad, la Vista previa de impresión empezará a detectar todas las impresoras locales. Los patrones de expresiones regulares deben seguir la sintaxis de JavaScript RegExp y las coincidencias distinguirán mayúsculas de minúsculas.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultPrinterSelection
  - Nombre de la directiva de grupos: Reglas de selección de impresora predeterminada
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Imprimir
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DefaultPrinterSelection
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"{ \"idPattern\": \".*public\", \"namePattern\": \".*Color\" }"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultPrinterSelection
  - Valor de ejemplo:
``` xml
<string>{ "idPattern": ".*public", "namePattern": ".*Color" }</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PrintHeaderFooter
  #### Imprimir encabezados y pies de página
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Haz que los "encabezados y pies de página" estén activados o desactivados en el cuadro de diálogo de impresión.

Si no configuras esta directiva, los usuarios podrán decidir si quieren imprimir los encabezados y pies de página.

Si deshabilitas esta directiva, los usuarios no podrán imprimir encabezados y pies de página.

Si habilitas esta directiva, los usuarios podrán imprimir siempre encabezados y pies de página.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PrintHeaderFooter
  - Nombre de la directiva de grupos: Imprimir encabezados y pies de página
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Imprimir
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Imprimir
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: PrintHeaderFooter
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PrintHeaderFooter
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PrintPreviewUseSystemDefaultPrinter
  #### Establecer la impresora predeterminada del sistema como la impresora predeterminada
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Insta a Microsoft Edge a usar la impresora predeterminada del sistema como la opción predeterminada en la vista previa de impresión en lugar de la impresora utilizada recientemente.

Si se deshabilita esta directiva o no se configura, la vista previa de impresión usará la impresora utilizada recientemente como la opción de destino predeterminada.

Si se habilita esta directiva, la vista previa de impresión usará la impresora predeterminada del sistema de SO como la opción de destino predeterminada.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PrintPreviewUseSystemDefaultPrinter
  - Nombre de la directiva de grupos: Establecer la impresora predeterminada del sistema como la impresora predeterminada
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Imprimir
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Imprimir
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: PrintPreviewUseSystemDefaultPrinter
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PrintPreviewUseSystemDefaultPrinter
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PrintingEnabled
  #### Habilitar la impresión
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Habilita la impresión en Microsoft Edge e impide que los usuarios cambien esta configuración.

Si se habilita esta directiva o no se configura, los usuarios podrán imprimir.

Si se deshabilita esta directiva, los usuarios no podrán imprimir desde Microsoft Edge. La impresión está deshabilitada en el menú de llave, las extensiones, las aplicaciones de JavaScript, etc. Los usuarios podrán seguir imprimiendo desde los complementos que omitan Microsoft Edge durante la impresión. Por ejemplo, determinadas aplicaciones de Adobe Flash tienen la opción de imprimir en el menú contextual, que no está cubierto por esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PrintingEnabled
  - Nombre de la directiva de grupos: Habilitar la impresión
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Imprimir
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: PrintingEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PrintingEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PrintingPaperSizeDefault
  #### Tamaño de página de impresión predeterminado
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Invalida el tamaño de página de impresión predeterminado.

name debe contener uno de los formatos de la lista o el valor "personalizado" si el tamaño de papel requerido no está en la lista. Si se proporciona el valor "personalizado", se debe especificar la propiedad custom_size. Describe la altura y anchura deseadas en micras. De lo contrario, no se debe especificar la propiedad custom_size. Se ignoran las directivas que violan estas reglas.

Si el tamaño de página no está disponible en la impresora elegida por el usuario, se ignora esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Diccionario

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PrintingPaperSizeDefault
  - Nombre de la directiva de grupos: Tamaño de página de impresión predeterminado
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Imprimir
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: PrintingPaperSizeDefault
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\PrintingPaperSizeDefault = {
  "custom_size": {
    "height": 297000, 
    "width": 210000
  }, 
  "name": "custom"
}
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PrintingPaperSizeDefault
  - Valor de ejemplo:
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
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### UseSystemPrintDialog
  #### Imprimir usando el cuadro de diálogo de impresión
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Muestra el cuadro de diálogo de impresión del sistema en lugar de la vista previa de impresión.

Si se habilita esta directiva, Microsoft Edge abrirá el cuadro de diálogo de impresión del sistema en lugar de la vista previa de impresión integrada cuando un usuario imprime una página.

Si no se configura o si se deshabilita esta directiva, los comandos de impresión desencadenan la pantalla de vista previa de impresión de Microsoft Edge.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: UseSystemPrintDialog
  - Nombre de la directiva de grupos: Imprimir usando el cuadro de diálogo de impresión
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Imprimir
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: UseSystemPrintDialog
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: UseSystemPrintDialog
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ## Inicio&comma; página principal y página de la nueva pestaña policies

  [Volver al principio](#microsoft-edge:-directivas)

  ### HomepageIsNewTabPage
  #### Establecer la página de la nueva pestaña como página principal
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Configurar la página principal predeterminada en Microsoft Edge. Puede establecer la página principal a la URL que especifique o a la página de nueva pestaña.

Si habilita esta directiva, siempre se usará la página de nueva pestaña para la página principal y se omitirá la ubicación de la URL de la página principal.

Si deshabilita esta directiva, la página principal del usuario no podrá ser la página de nueva pestaña, a menos que la URL se establezca en 'edge://newtab'.

Si no se configura, los usuarios podrán elegir si la página de nueva pestaña será o no la página principal.

Esta directiva solo está disponible en las instancias de Windows que estén unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise que estén inscritas para la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: HomepageIsNewTabPage
  - Nombre de la directiva de grupos: Establecer la página de la nueva pestaña como página principal
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de la nueva pestaña
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Inicio, página principal y página de la nueva pestaña
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: HomepageIsNewTabPage
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: HomepageIsNewTabPage
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### HomepageLocation
  #### Configurar la dirección URL de la página principal
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Configurar la URL de la página principal predeterminada en Microsoft Edge.

La página principal es la página que abre el botón Inicio. Las páginas que se abren al inicio se controlan mediante las directivas [RestoreOnStartup](#restoreonstartup).

Puede establecer una dirección URL aquí o establecer la página principal para abrir la página de nueva pestaña. Si selecciona abrir la página de nueva pestaña, esta directiva no surtirá efecto.

Si habilita esta directiva, los usuarios no podrán cambiar la dirección URL de la página principal, pero podrán elegir usar la página de nueva pestaña como página principal.

Si deshabilita o no configura esta directiva, los usuarios podrán elegir su propia página principal, siempre y cuando la directiva [HomepageIsNewTabPage](#homepageisnewtabpage) no esté habilitada.

Esta directiva solo está disponible en las instancias de Windows que estén unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise que estén inscritas para la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: HomepageLocation
  - Nombre de la directiva de grupos: Configurar la dirección URL de la página principal
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de la nueva pestaña
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Inicio, página principal y página de la nueva pestaña
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: HomepageLocation
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"https://www.contoso.com"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: HomepageLocation
  - Valor de ejemplo:
``` xml
<string>https://www.contoso.com</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### NewTabPageAllowedBackgroundTypes
  #### Configurar los tipos de fondo permitidos para el nuevo diseño de página de pestañas
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Puedes configurar qué tipos de imagen de fondo están permitidos en el nuevo diseño de página de pestaña en Microsoft Edge.

Si no configuras esta directiva, todos los tipos de imagen de fondo en la nueva página de pestaña se habilitan.

Asignación de opciones de directiva:

* DisableImageOfTheDay (1) = Deshabilitar el tipo de imagen de fondo diario

* DisableCustomImage (2) = Deshabilitar el tipo de imagen de fondo personalizado

* DisableAll (3) = Deshabilitar todos los tipos de imágenes de fondo

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: NewTabPageAllowedBackgroundTypes
  - Nombre de la directiva de grupos: Configurar los tipos de fondo permitidos para el nuevo diseño de página de pestañas
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de la nueva pestaña
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: NewTabPageAllowedBackgroundTypes
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: NewTabPageAllowedBackgroundTypes
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### NewTabPageCompanyLogo
  #### Establecer el logotipo de la empresa en la nueva ficha (obsoleto)
  
  >OBSOLETO: Esta directiva es obsoleta y no funciona después de la versión 85 de Microsoft Edge.
  #### Versiones admitidas:
  - En Windows y macOS desde 79, hasta 85

  #### Descripción
  Esta directiva no ha funcionado según lo esperado debido a cambios en los requisitos operativos. Por lo tanto, está en desuso.

     Especifica el logotipo de la empresa que se usará en la página de la nueva pestaña en Microsoft Edge.

     La directiva se debe configurar como una cadena que expresa los logotipos en formato JSON. Por ejemplo: { "default_logo": { "url": "https://www.contoso.com/logo.png", "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29" }, "light_logo": { "url": "https://www.contoso.com/light_logo.png", "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737" } }

     Para configurar esta directiva, debes especificar la dirección URL desde la que Microsoft Edge puede descargar el logotipo y su hash de cifrado (SHA-256), que se usa para comprobar la integridad de la descarga. El logotipo debe estar en formato PNG o SVG y el tamaño de archivo no debe superar los 16 MB. El logotipo se descarga y se almacena en la caché, y se volverá a descargar cada vez que cambie la dirección URL o el hash. La dirección URL debe ser accesible sin ninguna autenticación.

     El "default_logo'' es necesario y se usará cuando no haya ninguna imagen de fondo. Si se proporciona el ''light_logo'', se usará cuando la página de la nueva pestaña del usuario tenga una imagen de fondo. Recomendamos usar un logotipo horizontal con un fondo transparente que esté alineado a la izquierda y centrado verticalmente. El logotipo debe tener una altura mínima de 32 píxeles y una relación de aspecto de 1:1 a 4:1. El "default_logo" debe tener un contraste adecuado con un fondo blanco o negro, mientras que el "light_logo" debe tener un contraste adecuado con una imagen de fondo.

     Si habilitas esta directiva, Microsoft Edge se descargará y mostrará los logotipos especificados en la página de la nueva pestaña. Los usuarios no pueden invalidar ni ocultar los logotipos.

     Si deshabilitas o no configuras esta directiva, Microsoft Edge no mostrará ningún logotipo de la empresa ni de Microsoft en la página de la nueva pestaña.

     Si necesitas ayuda para determinar el hash SHA-256, consulta https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/get-filehash.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Diccionario

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: NewTabPageCompanyLogo
  - Nombre de la directiva de grupos: Establecer el logotipo de la empresa en la nueva ficha (obsoleto)
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de la nueva pestaña
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: NewTabPageCompanyLogo
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
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


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: NewTabPageCompanyLogo
  - Valor de ejemplo:
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
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### NewTabPageHideDefaultTopSites
  #### Ocultar los sitios principales predeterminados de la página de la nueva pestaña
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Oculta los sitios principales predeterminados de la página de la nueva pestaña en Microsoft Edge.

Si se establece esta directiva como true, se ocultarán los iconos de los sitios principales predeterminados.

Si se establece esta directiva como false o no se configura, los iconos de los sitios principales predeterminados permanecerán visibles.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: NewTabPageHideDefaultTopSites
  - Nombre de la directiva de grupos: Ocultar los sitios principales predeterminados de la página de la nueva pestaña
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de la nueva pestaña
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: NewTabPageHideDefaultTopSites
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: NewTabPageHideDefaultTopSites
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### NewTabPageLocation
  #### Configurar la dirección URL de la página de la nueva pestaña
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Configurar la dirección URL predeterminada para la página de nueva pestaña.

Esta directiva determina la página que se abre cuando se crean nuevas pestañas (también cuando se abren nuevas ventanas). Asimismo, afecta a la página de inicio si está configurada para abrirse en la página de nueva pestaña.

Esta directiva no determina qué página se abre en el inicio; ya que eso está controlado por la directiva [RestoreOnStartup](#restoreonstartup). Tampoco afecta a la página de inicio si está configurada para abrirse en la página de nueva pestaña.

Si no configura esta directiva, se usará la página de nueva pestaña predeterminada.

Si configura esta directiva *y* la directiva [NewTabPageSetFeedType](#newtabpagesetfeedtype), esta directiva tendrá prioridad.

Si se proporciona una dirección URL no válida, las nuevas pestañas abrirán about://blank.

Esta directiva solo está disponible en las instancias de Windows que estén unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: NewTabPageLocation
  - Nombre de la directiva de grupos: Configurar la dirección URL de la página de la nueva pestaña
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de la nueva pestaña
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Inicio, página principal y página de la nueva pestaña
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: NewTabPageLocation
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"https://www.fabrikam.com"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: NewTabPageLocation
  - Valor de ejemplo:
``` xml
<string>https://www.fabrikam.com</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### NewTabPageManagedQuickLinks
  #### Establecer vínculos rápidos a la página de la nueva pestaña
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 79 o posterior

  #### Descripción
  De manera predeterminada, Microsoft Edge muestra vínculos rápidos en la página de la nueva pestaña de los accesos directos agregados por el usuario y los sitios principales basados en el historial de exploración. Con esta directiva, puede configurar hasta tres iconos de vínculos rápidos en la página de la nueva pestaña, expresados como un objeto JSON:

[ { "url": "https://www.contoso.com", "title": "Contoso Portal", "pinned": true/false }, ... ]

El campo 'url' es obligatorio; 'title' y 'pinned' son opcionales. Si no se proporciona 'title', se usará la dirección URL como título predeterminado. Si no se proporciona 'pinned', el valor predeterminado será false.

Microsoft Edge los muestra en el orden en que aparecen en la lista, de izquierda a derecha, y todos los iconos anclados se muestran por delante de los iconos no anclados.

Si la directiva está establecida como obligatoria, se omitirá el campo 'pinned' y se anclarán todos los iconos. El usuario no puede eliminar los iconos y siempre aparecerán al principio de la lista de vínculos rápidos.

Si la directiva está establecida como se recomienda, los iconos anclados permanecerán en la lista, pero el usuario podrá editarlos y eliminarlos. Los iconos de vínculos rápidos que no están anclados se comportarán como los sitios principales predeterminados y se quitarán de la lista si otros sitios web se visitan con más frecuencia. Al aplicar vínculos no anclados mediante esta directiva a un perfil de explorador existente, es posible que los vínculos no aparezcan, en función de cómo se clasifiquen en comparación con el historial de exploración del usuario.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Diccionario

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: NewTabPageManagedQuickLinks
  - Nombre de la directiva de grupos: Establecer vínculos rápidos a la página de la nueva pestaña
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de la nueva pestaña
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Inicio, página principal y página de la nueva pestaña
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: NewTabPageManagedQuickLinks
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
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


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: NewTabPageManagedQuickLinks
  - Valor de ejemplo:
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
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### NewTabPagePrerenderEnabled
  #### Habilitar la carga previa de la página de nueva pestaña para una representación más rápida
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 85 o posterior

  #### Descripción
  Si configuras esta directiva, se habilitará la carga previa de la página de Nueva pestaña y los usuarios no podrán cambiar esta configuración. Si no configuras esta directiva, se habilitará la carga previa y los usuarios podrán cambiar esta configuración.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: NewTabPagePrerenderEnabled
  - Nombre de la directiva de grupos: Habilitar la carga previa de la página de nueva pestaña para una representación más rápida
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de la nueva pestaña
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Inicio, página principal y página de la nueva pestaña
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: NewTabPagePrerenderEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: NewTabPagePrerenderEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### NewTabPageSetFeedType
  #### Configurar la experiencia de página de la nueva pestaña de Microsoft Edge
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 79 o posterior

  #### Descripción
  Te permite elegir la experiencia de la fuente de Office 365 o Microsoft News para la página de la nueva pestaña.

Al establecer esta directiva en  'News', los usuarios verán la experiencia de la fuente de Microsoft News en la página de la nueva pestaña.

Al establecer esta directiva en  'Office', los usuarios con un inicio de sesión en el explorador de Azure Active Directory verán la experiencia de la fuente de Office 365 en la página de la nueva pestaña.

Si deshabilitas o no configuras esta directiva:

- A los usuarios con un inicio de sesión del explorador de Azure Active Directory se le ofrecerá la experiencia de la fuente de la página de nueva pestaña de Office 365, así como la experiencia estándar de la fuente de la página de nueva pestaña.

- Los usuarios que no tengan un inicio de sesión en el explorador de Azure Active Directory verán la experiencia estándar de la página de nueva pestaña.

Si configuras esta directiva *y* la directiva [NewTabPageLocation](#newtabpagelocation), [NewTabPageLocation](#newtabpagelocation) tiene prioridad.

Configuración predeterminada: deshabilitada o no configurada.

Asignación de opciones de directiva:

* News (0) = Experiencia de la fuente de Microsoft News

* Office (1) = Experiencia de la fuente de Office 365

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: NewTabPageSetFeedType
  - Nombre de la directiva de grupos: Configurar la experiencia de página de la nueva pestaña de Microsoft Edge
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de la nueva pestaña
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Inicio, página principal y página de la nueva pestaña
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: NewTabPageSetFeedType
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: NewTabPageSetFeedType
  - Valor de ejemplo:
``` xml
<integer>0</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### RestoreOnStartup
  #### Acción que se realizará al inicio
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especificar cómo se comporta Microsoft Edge cuando se inicia.

Si quiere que siempre se abra una nueva pestaña en el inicio, elija 'RestoreOnStartupIsNewTabPage'.

Si quiere volver a abrir las direcciones URL que estaban abiertas la última vez que se cerró Microsoft Edge, elija 'RestoreOnStartupIsLastSession'. Se restaurará la sesión de exploración tal como estaba. Tenga en cuenta que esta opción deshabilita algunas opciones de configuración que se basan en sesiones o que realizan acciones al salir (por ejemplo, Borrar datos de exploración al salir o cookies de solo sesión).

Si quiere abrir un conjunto específico de direcciones URL, elija 'RestoreOnStartupIsURLs'.

Deshabilitar esta configuración es equivalente a dejarla sin configurar. Los usuarios podrán cambiarla en Microsoft Edge.

Esta directiva solo está disponible en las instancias de Windows que estén unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise inscritas para la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX

Asignación de opciones de directiva:

* RestoreOnStartupIsNewTabPage (5) = Abrir una nueva pestaña

* RestoreOnStartupIsLastSession (1) = Restaurar la última sesión

* RestoreOnStartupIsURLs (4) = Abrir una lista de direcciones URL

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: RestoreOnStartup
  - Nombre de la directiva de grupos: Acción que se realizará al inicio
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de la nueva pestaña
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Inicio, página principal y página de la nueva pestaña
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: RestoreOnStartup
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000004
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: RestoreOnStartup
  - Valor de ejemplo:
``` xml
<integer>4</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### RestoreOnStartupURLs
  #### Sitios que se abrirán cuando se inicia el explorador
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especificar una lista de sitios web que se abran automáticamente cuando se inicia el explorador. Si no configura esta directiva, no se abrirá ningún sitio en el inicio.

Esta directiva solo funciona si establece también la directiva [RestoreOnStartup](#restoreonstartup) en 'Abrir una lista de direcciones URL' (4).

Esta directiva solo está disponible en las instancias de Windows que estén unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise que estén inscritas en la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: RestoreOnStartupURLs
  - Nombre de la directiva de grupos: Sitios que se abrirán cuando se inicia el explorador
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de la nueva pestaña
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Inicio, página principal y página de la nueva pestaña
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada\RestoreOnStartupURLs
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\1 = "https://contoso.com"
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\2 = "https://www.fabrikam.com"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: RestoreOnStartupURLs
  - Valor de ejemplo:
``` xml
<array>
  <string>https://contoso.com</string>
  <string>https://www.fabrikam.com</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ShowHomeButton
  #### Mostrar el botón Inicio en la barra de herramientas
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Muestra el botón Inicio en la barra de herramientas de Microsoft Edge.

Habilite esta directiva para mostrar siempre el botón Inicio. Deshabilítela para no mostrar el botón.

Si no se establece la directiva, los usuarios pueden elegir si quieren mostrar el botón Inicio.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ShowHomeButton
  - Nombre de la directiva de grupos: Mostrar el botón Inicio en la barra de herramientas
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Inicio, página principal y página de la nueva pestaña
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Inicio, página principal y página de la nueva pestaña
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: ShowHomeButton
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ShowHomeButton
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ## Mensajería nativa policies

  [Volver al principio](#microsoft-edge:-directivas)

  ### NativeMessagingAllowlist
  #### Controlar qué hosts de mensajería nativos pueden usar los usuarios
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica los hosts de mensajes nativos que los usuarios pueden usar en Microsoft Edge.

De manera predeterminada, se permiten todos los hosts de mensajes nativos. Si se configura la directiva [NativeMessagingBlocklist](#nativemessagingblocklist) a *, se bloquearán todos los hosts de mensajes nativos y solo se cargarán los hosts de mensajes nativos de aquí.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: NativeMessagingAllowlist
  - Nombre de la directiva de grupos: Controlar qué hosts de mensajería nativos pueden usar los usuarios
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Mensajería nativa
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\2 = "com.native.messaging.host.name2"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: NativeMessagingAllowlist
  - Valor de ejemplo:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### NativeMessagingBlocklist
  #### Configurar la lista de bloqueados de mensajes nativa
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica qué hosts de mensajes nativos no deben usarse.

Use '*' para bloquear todos los hosts de mensajes nativos a menos que aparezcan explícitamente en la lista de permitidos.

Si no se configura esta directiva, Microsoft Edge cargará todos los hosts de mensajes nativos instalados.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: NativeMessagingBlocklist
  - Nombre de la directiva de grupos: Configurar la lista de bloqueados de mensajes nativa
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Mensajería nativa
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\2 = "com.native.messaging.host.name2"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: NativeMessagingBlocklist
  - Valor de ejemplo:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### NativeMessagingUserLevelHosts
  #### Permitir hosts de mensajería nativos de nivel de usuario (instalados sin permisos del administrador)
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite la instalación de nivel de usuario de los hosts de mensajes nativos.

Si se deshabilita esta directiva, Microsoft Edge solo usará hosts de mensajes nativos instalados en el nivel de sistema.

De manera predeterminada, si no se configura esta directiva, Microsoft Edge permitirá el uso de hosts de mensajes nativos de nivel de usuario.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: NativeMessagingUserLevelHosts
  - Nombre de la directiva de grupos: Permitir hosts de mensajería nativos de nivel de usuario (instalados sin permisos del administrador)
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Mensajería nativa
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: NativeMessagingUserLevelHosts
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: NativeMessagingUserLevelHosts
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ## Proveedor de búsquedas predeterminado policies

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultSearchProviderEnabled
  #### Habilitar el proveedor de búsquedas predeterminado
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Habilitar el uso de un proveedor de búsqueda predeterminado.

Si habilita esta directiva, un usuario puede buscar un término al escribir en la barra de direcciones (siempre y cuando no se escriba una dirección URL).

Puede especificar el proveedor de búsqueda predeterminado habilitando el resto de las directivas de búsqueda predeterminadas. Si éstas se dejan en blanco (sin configurar) o se configuran de forma incorrecta, el usuario puede elegir el proveedor predeterminado.

Si deshabilita esta directiva, el usuario no puede buscar desde la barra de direcciones.

Si habilita o deshabilita esta directiva, los usuarios no podrán cambiarla o reemplazarla.

Si no configura esta directiva, el proveedor de búsquedas predeterminado estará habilitado y el usuario podrá elegirlo y establecer la lista de proveedores de búsqueda.

Esta directiva solo está disponible en las instancias de Windows que estén unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise que estén inscritas para la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX.

A partir de Microsoft Edge 84, puede establecer esta directiva como una directiva recomendada.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultSearchProviderEnabled
  - Nombre de la directiva de grupos: Habilitar el proveedor de búsquedas predeterminado
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Proveedor de búsquedas predeterminado
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Proveedor de búsquedas predeterminado
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: DefaultSearchProviderEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultSearchProviderEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultSearchProviderEncodings
  #### Codificaciones del proveedor de búsquedas predeterminado
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica las codificaciones de caracteres que admite el proveedor de búsqueda. Las codificaciones son nombres de páginas de códigos como UTF-8, GB2312 y ISO-8859-1. Se prueban en el orden indicado.

Esta directiva es opcional. Si no se configura, se usa la codificación predeterminada, UTF-8.

Esta directiva solo se aplica si se habilitan las directivas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) y [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)

A partir del Microsoft Edge 84, puedes establecer esta directiva como una directiva recomendada. Si el usuario ya ha establecido un proveedor de búsqueda predeterminado, el proveedor de búsqueda predeterminado configurado por esta directiva recomendada no se agregará a la lista de proveedores de búsqueda entre los que el usuario puede elegir. Si este es el comportamiento deseado, usa la directiva [ManagedSearchEngines](#managedsearchengines).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultSearchProviderEncodings
  - Nombre de la directiva de grupos: Codificaciones del proveedor de búsquedas predeterminado
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Proveedor de búsquedas predeterminado
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Proveedor de búsquedas predeterminado
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada\DefaultSearchProviderEncodings
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\1 = "UTF-8"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\2 = "UTF-16"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\3 = "GB2312"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\4 = "ISO-8859-1"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultSearchProviderEncodings
  - Valor de ejemplo:
``` xml
<array>
  <string>UTF-8</string>
  <string>UTF-16</string>
  <string>GB2312</string>
  <string>ISO-8859-1</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultSearchProviderImageURL
  #### Especifica la característica de búsqueda por imagen para el proveedor de búsquedas predeterminado
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica la dirección URL del motor de búsqueda que se usa para la búsqueda de imágenes. Se envían las solicitudes de búsqueda mediante el método GET.

Esta directiva es opcional. Si no se configura, la búsqueda de imágenes no está disponible.

Especifica la dirección URL de búsqueda de imágenes de Bing como:
'{bing:baseURL}images/detail/search?iss=sbiupload&FORM=ANCMS1#enterInsights'.

Especifica la dirección URL de búsqueda de imágenes de Google como: '{google:baseURL}searchbyimage/upload'.

Consulta la directiva [DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams) para finalizar la configuración de la búsqueda de imágenes.

Esta directiva se aplica solo si se habilitan las directivas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) y [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir de Microsoft Edge 84, puedes establecer esta directiva como directiva recomendada.  Si el usuario ya ha establecido un proveedor de búsqueda predeterminado, el proveedor de búsqueda predeterminado configurado por esta directiva recomendada no se agregará a la lista de proveedores de búsqueda entre los que el usuario puede elegir. Si este es el comportamiento deseado, usa la directiva [ManagedSearchEngines](#managedsearchengines).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultSearchProviderImageURL
  - Nombre de la directiva de grupos: Especifica la característica de búsqueda por imagen para el proveedor de búsquedas predeterminado
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Proveedor de búsquedas predeterminado
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Proveedor de búsquedas predeterminado
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: DefaultSearchProviderImageURL
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"https://search.contoso.com/searchbyimage/upload"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultSearchProviderImageURL
  - Valor de ejemplo:
``` xml
<string>https://search.contoso.com/searchbyimage/upload</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultSearchProviderImageURLPostParams
  #### Parámetros para una dirección URL de imagen que usa POST
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Si se habilita esta directiva, se especifican los parámetros usados cuando se realiza una búsqueda de imagen que use POST. La directiva consiste en pares de nombre/valor separados por comas. Si un valor es un parámetro de plantilla, como {imageThumbnail} en el ejemplo anterior, se reemplaza con los datos de miniaturas de imagen reales. Esta directiva se aplica solo si se habilitan las directivas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) y [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

Especifica los parámetros de POST de la dirección URL de la búsqueda de imágenes de Bing como:
'imageBin={google:imageThumbnailBase64}'.

Especifica los parámetros de POST de la dirección URL de la búsqueda de imagen de Google como:
'encoded_image={google:imageThumbnail},image_url={google:imageURL},sbisrc={google:imageSearchSource},original_width={google:imageOriginalWidth},original_height={google:imageOriginalHeight}'.

Si no se configura esta directiva, se envían las solicitudes de búsqueda de imágenes con el método GET.

A partir de Microsoft Edge 84, puedes establecer esta directiva como directiva recomendada. Si el usuario ya ha establecido un proveedor de búsqueda predeterminado, el proveedor de búsqueda predeterminado configurado por esta directiva recomendada no se agregará a la lista de proveedores de búsqueda entre los que el usuario puede elegir. Si este es el comportamiento deseado, usa la directiva [ManagedSearchEngines](#managedsearchengines).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultSearchProviderImageURLPostParams
  - Nombre de la directiva de grupos: Parámetros para una dirección URL de imagen que usa POST
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Proveedor de búsquedas predeterminado
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Proveedor de búsquedas predeterminado
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: DefaultSearchProviderImageURLPostParams
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"content={imageThumbnail},url={imageURL},sbisrc={SearchSource}"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultSearchProviderImageURLPostParams
  - Valor de ejemplo:
``` xml
<string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultSearchProviderKeyword
  #### Palabra clave del proveedor de búsquedas predeterminado
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica la palabra clave, que es el acceso directo que se usa en la barra de direcciones para desencadenar la búsqueda de este proveedor.

Esta directiva es opcional. Si no la configuras, ninguna palabra clave activa el proveedor de búsqueda.

Esta directiva solo se aplica si se habilitan las directivas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) y [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir del Microsoft Edge 84, puedes establecer esta directiva como una directiva recomendada. Si el usuario ya ha establecido un proveedor de búsqueda predeterminado, el proveedor de búsqueda predeterminado configurado por esta directiva recomendada no se agregará a la lista de proveedores de búsqueda entre los que el usuario puede elegir. Si este es el comportamiento deseado, usa la directiva [ManagedSearchEngines](#managedsearchengines).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultSearchProviderKeyword
  - Nombre de la directiva de grupos: Palabra clave del proveedor de búsquedas predeterminado
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Proveedor de búsquedas predeterminado
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Proveedor de búsquedas predeterminado
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: DefaultSearchProviderKeyword
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"mis"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultSearchProviderKeyword
  - Valor de ejemplo:
``` xml
<string>mis</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultSearchProviderName
  #### Nombre del proveedor de búsquedas predeterminado
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica el nombre del proveedor de búsqueda predeterminado.

Si se habilita esta directiva, se establecerá el nombre del proveedor de búsqueda predeterminado.

Si no se habilita esta directiva o si se deja en blanco, se usará el nombre de host especificado por la dirección URL de búsqueda.

Debe establecerse 'DefaultSearchProviderName' como un proveedor de búsqueda cifrada aprobado por la organización que se corresponda con el proveedor de búsqueda cifrada establecido en DTBC-0008. Esta directiva solo se aplica si se habilitan las directivas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) y [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir de Microsoft Edge 84, puedes establecer esta directiva como directiva recomendada.  Si el usuario ya ha establecido un proveedor de búsqueda predeterminado, el proveedor de búsqueda predeterminado configurado por esta directiva recomendada no se agregará a la lista de proveedores de búsqueda entre los que el usuario puede elegir. Si este es el comportamiento deseado, usa la directiva [ManagedSearchEngines](#managedsearchengines).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultSearchProviderName
  - Nombre de la directiva de grupos: Nombre del proveedor de búsquedas predeterminado
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Proveedor de búsquedas predeterminado
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Proveedor de búsquedas predeterminado
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: DefaultSearchProviderName
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"My Intranet Search"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultSearchProviderName
  - Valor de ejemplo:
``` xml
<string>My Intranet Search</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultSearchProviderSearchURL
  #### URL de búsqueda del proveedor de búsquedas predeterminado
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica la dirección URL del motor de búsqueda que se usa para una búsqueda predeterminada. La dirección URL contiene la cadena '{searchTerms}', que se reemplaza en el momento de la consulta por los términos que está buscando el usuario.

Especifica la dirección URL de Bing como:

'{bing:baseURL}search?q={searchTerms}'.

Especifica la dirección URL de Google como: '{google:baseURL}search?q={searchTerms}&{google:RLZ}{google:originalQueryForSuggestion}{google:assistedQueryStats}{google:searchFieldtrialParameter}{google:searchClient}{google:sourceId}ie={inputEncoding}'.

Esta directiva es necesaria cuando se habilita la directiva [DefaultSearchProviderEnabled](#defaultsearchproviderenabled); si dicha directiva no se habilita, se ignorará esta directiva.

A partir de Microsoft Edge 84, puedes establecer esta directiva como directiva recomendada.  Si el usuario ya ha establecido un proveedor de búsqueda predeterminado, el proveedor de búsqueda predeterminado configurado por esta directiva recomendada no se agregará a la lista de proveedores de búsqueda entre los que el usuario puede elegir. Si este es el comportamiento deseado, usa la directiva [ManagedSearchEngines](#managedsearchengines).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultSearchProviderSearchURL
  - Nombre de la directiva de grupos: URL de búsqueda del proveedor de búsquedas predeterminado
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Proveedor de búsquedas predeterminado
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Proveedor de búsquedas predeterminado
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: DefaultSearchProviderSearchURL
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"https://search.contoso.com/search?q={searchTerms}"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultSearchProviderSearchURL
  - Valor de ejemplo:
``` xml
<string>https://search.contoso.com/search?q={searchTerms}</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultSearchProviderSuggestURL
  #### URL del proveedor de búsqueda predeterminado para obtener sugerencias
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica la dirección URL del motor de búsqueda usado para proporcionar sugerencias de búsqueda. La dirección URL contiene la cadena '{searchTerms}', que se reemplaza en el momento de la consulta por el texto que el usuario ha escrito hasta ese momento.

Esta directiva es opcional. Si no se configura, los usuarios no verán las sugerencias de búsqueda; verán sugerencias de su historial de exploración y favoritos.

La dirección URL sugerida de Bing se puede especificar como:

'{bing:baseURL}qbox?query={searchTerms}'.

La dirección URL sugerida de Google se puede especificar como: '{google:baseURL}complete/search?output=chrome&q={searchTerms}'.

Esta directiva solo se aplica si se habilitan las directivas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) y [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir de Microsoft Edge 84, puedes establecer esta directiva como directiva recomendada. Si el usuario ya ha establecido un proveedor de búsqueda predeterminado, el proveedor de búsqueda predeterminado configurado por esta directiva recomendada no se agregará a la lista de proveedores de búsqueda entre los que el usuario puede elegir. Si este es el comportamiento deseado, usa la directiva [ManagedSearchEngines](#managedsearchengines).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultSearchProviderSuggestURL
  - Nombre de la directiva de grupos: URL del proveedor de búsqueda predeterminado para obtener sugerencias
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Proveedor de búsquedas predeterminado
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Proveedor de búsquedas predeterminado
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: DefaultSearchProviderSuggestURL
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"https://search.contoso.com/suggest?q={searchTerms}"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultSearchProviderSuggestURL
  - Valor de ejemplo:
``` xml
<string>https://search.contoso.com/suggest?q={searchTerms}</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### NewTabPageSearchBox
  #### Configurar la nueva experiencia del cuadro de búsqueda de página de pestañas
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 85 o posterior

  #### Descripción
  Puedes configurar el cuadro de búsqueda de la página de nueva pestaña para que use "Cuadro de búsqueda (recomendado)" o "Barra de direcciones" para buscar en nuevas pestañas. Esta directiva solo funciona si configuras el motor de búsqueda en un valor distinto de Bing al establecer las dos directivas siguientes: [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) y [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

 Si deshabilitas o no configuras esta directiva y:

- si el motor de búsqueda predeterminado de la barra de direcciones es Bing, en la página de nueva pestaña se usa el cuadro de búsqueda para buscar en nuevas pestañas.
- si el motor de búsqueda predeterminado de la barra de direcciones no es Bing, se ofrece a los usuarios una opción adicional (usar 'Barra de direcciones') al buscar en nuevas pestañas.


Si habilitas esta directiva y la configuras como:

- "Cuadro de búsqueda (recomendado)" ('bing'), la página de nueva pestaña usa el cuadro de búsqueda para buscar en nuevas pestañas.
- "Barra de direcciones" ('redirect'), el cuadro de búsqueda de la página de nueva pestaña usa la barra de direcciones para buscar en pestañas nuevas.

Asignación de opciones de directiva:

* bing (bing) = Cuadro de búsqueda (recomendado)

* redirect (redirect) = Barra de direcciones

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: NewTabPageSearchBox
  - Nombre de la directiva de grupos: Configurar la nueva experiencia del cuadro de búsqueda de página de pestañas
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Proveedor de búsquedas predeterminado
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/Proveedor de búsquedas predeterminado
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: NewTabPageSearchBox
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"bing"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: NewTabPageSearchBox
  - Valor de ejemplo:
``` xml
<string>bing</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ## Servidor proxy policies

  [Volver al principio](#microsoft-edge:-directivas)

  ### ProxyBypassList
  #### Configurar reglas de omisión de proxy
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Define una lista de hosts para los que Microsoft Edge omite cualquier proxy.

Esta directiva se aplica solo si se ha seleccionado 'Usar servidores proxy fijos' en la directiva [ProxyMode](#proxymode). Si se ha seleccionado cualquier otro modo para la configuración de directivas de proxy, no debe habilitar ni configurar esta directiva.

Si se habilita esta directiva, puede crear una lista de hosts para los que Microsoft Edge no usa un proxy.

Si no se configura esta directiva, no se crea ninguna lista de hosts para los que Microsoft Edge omite un proxy. Deje esta directiva sin configurar si se ha especificado algún otro método para establecer las directivas de proxy.

Para obtener ejemplos más detallados, visite [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ProxyBypassList
  - Nombre de la directiva de grupos: Configurar reglas de omisión de proxy
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Servidor proxy
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ProxyBypassList
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"https://www.contoso.com, https://www.fabrikam.com"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ProxyBypassList
  - Valor de ejemplo:
``` xml
<string>https://www.contoso.com, https://www.fabrikam.com</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ProxyMode
  #### Configurar ajustes del servidor proxy
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica la configuración del servidor proxy usada por Microsoft Edge. Si se habilita esta directiva, los usuarios no pueden cambiar la configuración del proxy.

Si se elige no usar nunca un servidor proxy y conectarse siempre directamente, se omitirán todas las demás opciones.

Si se elige usar la configuración del proxy del sistema, se omitirán todas las demás opciones.

Si se elige detectar automáticamente el servidor proxy, se omitirán todas las demás opciones.

Si se elige el modo de proxy de servidor fijo, se pueden especificar más opciones en [ProxyServer](#proxyserver) y 'Lista de reglas de omisión de proxy separadas por comas'.

Si se elige usar un script de proxy .pac, se debe especificar la dirección URL al script en 'Dirección URL a un archivo .pac de proxy'.

Para obtener ejemplos detallados, vaya a [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

Si se habilita esta directiva, Microsoft Edge omitirá todas las opciones relacionadas con el proxy especificadas desde la línea de comandos.

Si no se configura esta directiva, los usuarios podrán elegir su propia configuración del proxy.

Asignación de opciones de directiva:

* ProxyDisabled (direct) = No utilizar nunca un proxy

* ProxyAutoDetect (auto_detect) = Detectar automáticamente configuración del proxy

* ProxyPacScript (pac_script) = Usar un script de proxy .pac

* ProxyFixedServers (fixed_servers) = Usar servidores proxy fijos

* ProxyUseSystem (system) = Usar la configuración de proxy del sistema

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ProxyMode
  - Nombre de la directiva de grupos: Configurar ajustes del servidor proxy
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Servidor proxy
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ProxyMode
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"direct"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ProxyMode
  - Valor de ejemplo:
``` xml
<string>direct</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ProxyPacUrl
  #### Establecer la dirección URL del archivo .pac del proxy
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica la dirección URL de un archivo de configuración automática de proxy (PAC).

Esta directiva solo se aplica si se ha seleccionado 'Usar un script de proxy .pac' en la directiva [ProxyMode](#proxymode). Si se selecciona cualquier otro modo para configurar directivas de proxy, no debe habilitar ni configurar esta directiva.

Si se habilita esta directiva, puede especificarse la dirección URL de un archivo PAC, que define el modo en que el explorador elige automáticamente el servidor proxy adecuado para obtener un sitio web determinado.

Si se deshabilita o no se configura esta directiva, no se especifica ningún archivo PAC. Deje esta directiva sin configurar si ha especificado otro método para establecer directivas de proxy.

Para obtener ejemplos detallados, consulte [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ProxyPacUrl
  - Nombre de la directiva de grupos: Establecer la dirección URL del archivo .pac del proxy
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Servidor proxy
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ProxyPacUrl
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"https://internal.contoso.com/example.pac"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ProxyPacUrl
  - Valor de ejemplo:
``` xml
<string>https://internal.contoso.com/example.pac</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ProxyServer
  #### Configurar dirección o URL del servidor proxy
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica la dirección URL del servidor proxy.

Esta directiva solo se aplica si se ha seleccionado 'Usar servidores proxy fijos' en la directiva [ProxyMode](#proxymode). Si se selecciona cualquier otro modo para configurar directivas de proxy, no habilite ni configure esta directiva.

Si se habilita esta directiva, se usará el servidor proxy configurado por esta directiva para todas las direcciones URL.

Si se deshabilita o no se configura esta directiva, los usuarios podrán elegir su propia configuración de proxy en este modo de proxy. Deje esta directiva sin configurar si ha especificado otro método para establecer directivas de proxy.

Para obtener más opciones y ejemplos detallados, consulte [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ProxyServer
  - Nombre de la directiva de grupos: Configurar dirección o URL del servidor proxy
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Servidor proxy
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ProxyServer
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"123.123.123.123:8080"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ProxyServer
  - Valor de ejemplo:
``` xml
<string>123.123.123.123:8080</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ProxySettings
  #### Configuración del proxy
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Configura las opciones de proxy para Microsoft Edge.

Si se habilita esta directiva, Microsoft Edge pasa por alto todas las opciones relacionadas con el proxy especificadas desde la línea de comandos.

Si no se configura esta directiva, los usuarios pueden elegir su propia configuración de proxy.

Esta directiva invalidará las siguientes directivas individuales:

[ProxyMode](#proxymode)
[ProxyPacUrl](#proxypacurl)
[ProxyServer](#proxyserver)
[ProxyBypassList](#proxybypasslist)

El campo ProxyMode permite especificar el servidor proxy usado por Microsoft Edge e impide que los usuarios cambien la configuración de proxy.

El campo ProxyPacUrl es una dirección URL a un archivo .pac de proxy.

El campo ProxyServer es una dirección URL para el servidor proxy.

El campo ProxyBypassList es una lista de hosts del proxy que Microsoft Edge omite.

Si elige el valor 'direct' como 'ProxyMode', no se usará nunca un proxy y se ignorarán todos los demás campos.

Si elige el valor 'system' como 'ProxyMode', se usará el proxy del sistema y se ignorarán todos los demás campos.

Si elige el valor 'auto_detect' como 'ProxyMode', se ignorarán todos los demás campos.

Si elige el valor 'fixed_server' como 'ProxyMode', se usarán los campos 'ProxyServer' y 'ProxyBypassList'.

Si elige el valor 'pac_script' como 'ProxyMode', se usarán los campos 'ProxyPacUrl' y 'ProxyBypassList'.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Diccionario

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ProxySettings
  - Nombre de la directiva de grupos: Configuración del proxy
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/Servidor proxy
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ProxySettings
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {
  "ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", 
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ProxySettings
  - Valor de ejemplo:
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
  

  [Volver al principio](#microsoft-edge:-directivas)

  ## Additional policies

  [Volver al principio](#microsoft-edge:-directivas)

  ### AddressBarMicrosoftSearchInBingProviderEnabled
  #### Habilitar la Búsqueda de Microsoft en las sugerencias de Bing en la barra de direcciones
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 81 o posterior

  #### Descripción
  Habilita la visualización de sugerencias relevantes de la Búsqueda de Microsoft en Bing en la lista de sugerencias de la barra de direcciones cuando el usuario escribe una cadena de búsqueda en la barra de direcciones. Si se habilita o no se configura esta directiva, los usuarios podrán ver los resultados internos con tecnología de Búsqueda de Microsoft en Bing en la lista de sugerencias de la barra de direcciones de Microsoft Edge. Para ver los resultados de la Búsqueda de Microsoft en Bing, el usuario debe iniciar sesión en Microsoft Edge con su cuenta de Azure AD para esa organización.
Si se deshabilita esta directiva, los usuarios no podrán ver los resultados internos en la lista de sugerencias de la barra de direcciones de Microsoft Edge.
Si ha habilitado el conjunto de directivas que aplica un proveedor de búsquedas predeterminado ([DefaultSearchProviderEnabled](#defaultsearchproviderenabled), [DefaultSearchProviderName](#defaultsearchprovidername) y [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)) y el proveedor de búsquedas especificado no es Bing, esta directiva no será aplicable y no habrá ninguna sugerencia en la Búsqueda de Microsoft en Bing en la lista de sugerencias de la barra de direcciones.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AddressBarMicrosoftSearchInBingProviderEnabled
  - Nombre de la directiva de grupos: Habilitar la Búsqueda de Microsoft en las sugerencias de Bing en la barra de direcciones
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AddressBarMicrosoftSearchInBingProviderEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AddressBarMicrosoftSearchInBingProviderEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AdsSettingForIntrusiveAdsSites
  #### Configuración de anuncios para sitios con anuncios intrusivos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 78 o posterior

  #### Descripción
  Controla si se bloquean anuncios en sitios con anuncios intrusivos.

Asignación de opciones de directiva:

* AllowAds (1) = Permitir anuncios en todos los sitios

* BlockAds (2) = Bloquee los anuncios en sitios con anuncios intrusivos. (Valor predeterminado)

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AdsSettingForIntrusiveAdsSites
  - Nombre de la directiva de grupos: Configuración de anuncios para sitios con anuncios intrusivos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AdsSettingForIntrusiveAdsSites
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AdsSettingForIntrusiveAdsSites
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AllowDeletingBrowserHistory
  #### Habilitar la eliminación del explorador y el historial de descarga
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite eliminar el historial del explorador y el historial de descarga e impide que los usuarios cambien esta configuración.

Tenga en cuenta que, incluso con esta directiva deshabilitada, no se garantiza que se conserven los historiales de exploración y de descarga: los usuarios pueden editar o eliminar los archivos de la base de datos del historial directamente y el mismo explorador puede quitar (en función del período de expiración) o archivar alguno o todos los elementos del historial en cualquier momento.

Si se habilita esta directiva o no se configura, los usuarios podrán eliminar los historiales de exploración y de descarga.

Si se deshabilita esta directiva, los usuarios no podrán eliminar los historiales de exploración y de descarga.

Si se habilita esta directiva, no habilite la directiva [ClearBrowsingDataOnExit](#clearbrowsingdataonexit), ya que ambas se ocupan de la eliminación de datos. Si se habilitan las dos, la directiva [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) tendrá prioridad y se eliminarán todos los datos al cerrar Microsoft Edge, independientemente de cómo se configure esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AllowDeletingBrowserHistory
  - Nombre de la directiva de grupos: Habilitar la eliminación del explorador y el historial de descarga
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AllowDeletingBrowserHistory
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AllowDeletingBrowserHistory
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AllowFileSelectionDialogs
  #### Permitir cuadros de diálogo de selección de archivos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permitir el acceso a los archivos locales al permitir que Microsoft Edge muestre cuadros de diálogo de selección de archivos.

Si se habilita o no se configura esta directiva, los usuarios podrán abrir cuadros de diálogo de selección de archivos de la forma habitual.

Si se deshabilita esta directiva, cada vez que el usuario realice una acción que desencadene un cuadro de diálogo de selección de archivos (como importar favoritos, cargar archivos o guardar vínculos), aparecerá un mensaje en su lugar y se asumirá que el usuario ha hecho clic en Cancelar en el cuadro de diálogo de selección de archivos.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AllowFileSelectionDialogs
  - Nombre de la directiva de grupos: Permitir cuadros de diálogo de selección de archivos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AllowFileSelectionDialogs
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AllowFileSelectionDialogs
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AllowPopupsDuringPageUnload
  #### Permite que una página muestre elementos emergentes durante su descarga
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 78 o posterior

  #### Descripción
  Esta directiva permite que un administrador especifique que una página pueda mostrar elementos emergentes durante su descarga.

Cuando se establece la directiva en habilitada, las páginas pueden mostrar elementos emergentes mientras se descargan.

Cuando la directiva se establece en deshabilitada o no establecida, las páginas no pueden mostrar elementos emergentes mientras se descargan. Esto se debe a las especificaciones: (https://html.spec.whatwg.org/#apis-for-creating-and-navigating-browsing-contexts-by-name).

Esta directiva se quitará en el futuro.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AllowPopupsDuringPageUnload
  - Nombre de la directiva de grupos: Permite que una página muestre elementos emergentes durante su descarga
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AllowPopupsDuringPageUnload
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AllowPopupsDuringPageUnload
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AllowSurfGame
  #### Permitir el juego de surf
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 83 o posterior

  #### Descripción
  Si deshabilita esta directiva, los usuarios no podrán jugar al juego de surf cuando el dispositivo esté sin conexión o si el usuario navega a edge://surf.

Si se habilita o no se configura esta directiva, los usuarios podrán jugar al juego de surf.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AllowSurfGame
  - Nombre de la directiva de grupos: Permitir el juego de surf
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AllowSurfGame
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AllowSurfGame
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AllowSyncXHRInPageDismissal
  #### Permitir que las páginas envíen solicitudes sincrónicas de XHR durante el descarte de páginas (en desuso)
  >EN DESUSO: esta directiva está en desuso. Actualmente se admite pero será obsoleta en una versión futura.
  
  #### Versiones admitidas:
  - En Windows y macOS desde 79 o posterior

  #### Descripción
  Esta directiva está obsoleta porque sólo pretende ser un mecanismo a corto plazo para dar a las empresas más tiempo para actualizar el contenido de su web si resulta ser incompatible con el cambio de rechazar las solicitudes de XHR sincrónico durante el descarte de la página. No funcionará en la versión 88 de Microsoft Edge.

  Esta directiva permite especificar que una página pueda enviar solicitudes XHR sincrónicas durante el descarte de páginas.

Si habilitas esta directiva, las páginas podrán enviar solicitudes XHR síncronas durante el descarte de páginas.

 Si desactivas esta directiva o no la configuras, las páginas no podrán enviar solicitudes de XHR sincrónicas durante el descarte de páginas.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AllowSyncXHRInPageDismissal
  - Nombre de la directiva de grupos: Permitir que las páginas envíen solicitudes sincrónicas de XHR durante el descarte de páginas (en desuso)
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AllowSyncXHRInPageDismissal
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AllowSyncXHRInPageDismissal
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AllowTokenBindingForUrls
  #### Configure la lista de sitios con los que Microsoft Edge intentará establecer un enlace de token.
  
  
  #### Versiones admitidas:
  - En Windows desde 83 o posterior

  #### Descripción
  Configura la lista de patrones de URL para los sitios con los que el explorador intentará ejecutar en el protocolo de enlace de tokens.
 Para los dominios de esta lista, el explorador enviará el enlace de token ClientHello en el protocolo de enlace TLS (consulta https://tools.ietf.org/html/rfc8472).
 Si el servidor responde con una respuesta ServerHello válida, el explorador crea y envía mensajes de enlace de tokens en las siguientes solicitudes https. Para más información, consulta https://tools.ietf.org/html/rfc8471.

 Si esta lista está vacía, se deshabilitará el enlace de tokens.

Esta directiva solo está disponible en los dispositivos con Windows 10 con capacidad en modo de seguridad virtual.

 A partir de Microsoft Edge 86, esta directiva dejará de ser compatible con la actualización dinámica.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AllowTokenBindingForUrls
  - Nombre de la directiva de grupos: Configure la lista de sitios con los que Microsoft Edge intentará establecer un enlace de token.
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\2 = "[*.]mydomain2.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\3 = "[*.].mydomain2.com"

```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AllowTrackingForUrls
  #### Configurar excepciones de prevención de seguimiento para sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 78 o posterior

  #### Descripción
  Configurar la lista de patrones de direcciones URL que están excluidos de la prevención de seguimiento.

Si se configura esta directiva, la lista de patrones de direcciones URL configurados se excluirá de la prevención de seguimiento.

Si no se configura esta directiva, se usará el valor predeterminado global de la directiva "Bloquear el seguimiento de la actividad de exploración web de los usuarios" (si se ha establecido) o de la configuración personal del usuario para todos los sitios.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AllowTrackingForUrls
  - Nombre de la directiva de grupos: Configurar excepciones de prevención de seguimiento para sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AllowTrackingForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AlternateErrorPagesEnabled
  #### Sugerir páginas similares cuando no se puede encontrar una página web
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 80 o posterior

  #### Descripción
  Permitir que Microsoft Edge emita una conexión a un servicio web para generar sugerencias de direcciones URL y de búsqueda para problemas de conectividad, como errores de DNS.

Si se habilita esta directiva, se usará un servicio web para generar sugerencias de direcciones URL y de búsqueda para errores de red.

Si se deshabilita esta directiva, no se realizará ninguna llamada al servicio web y se mostrará una página de error estándar.

Si no se configura esta directiva, Microsoft Edge respeta la preferencia de usuario que se establece en Servicios en edge://settings/privacy.
En concreto, hay un una tecla de alternancia **Sugerir páginas similares cuando no se encuentra una página web**, que el usuario puede activar o desactivar. Ten en cuenta que si has habilitado esta directiva (AlternateErrorPagesEnabled), la opción Sugerir páginas similares cuando no se encuentra una página web está activada, pero el usuario no puede cambiar la configuración mediante el botón de alternancia. Si se deshabilita esta directiva, la opción Sugerir páginas similares cuando no se encuentra una página web está desactivada y el usuario no puede cambiar la configuración mediante el botón de alternancia.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AlternateErrorPagesEnabled
  - Nombre de la directiva de grupos: Sugerir páginas similares cuando no se puede encontrar una página web
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: AlternateErrorPagesEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AlternateErrorPagesEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AlwaysOpenPdfExternally
  #### Abrir siempre archivos PDF externamente
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Deshabilita el visor de PDF interno en Microsoft Edge.

Si se habilita esta directiva, Microsoft Edge trata los archivos PDF como descargas y permite a los usuarios abrirlos con la aplicación predeterminada.

Si no se configura esta directiva o se deshabilita, Microsoft Edge abrirá los archivos PDF (a menos que el usuario la deshabilite).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AlwaysOpenPdfExternally
  - Nombre de la directiva de grupos: Abrir siempre archivos PDF externamente
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AlwaysOpenPdfExternally
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AlwaysOpenPdfExternally
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AmbientAuthenticationInPrivateModesEnabled
  #### Habilitar la autenticación de ambiente para perfiles de invitados e InPrivate
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 81 o posterior

  #### Descripción
  Configura esta directiva para permitir o denegar la autenticación del ambiente para perfiles de invitados e InPrivate en Microsoft Edge.

La autenticación del ambiente es la autenticación HTTP con credenciales predeterminadas cuando no se proporcionan credenciales explícitas a través de esquemas de desafío o respuesta de NTLM/Kerberos/Negotiate.

Si se establece la directiva en 'RegularOnly', solo se permite la autenticación del ambiente para sesiones regulares. Las sesiones de invitado e InPrivate no podrán autenticarse de forma ambiental.

Si se establece la directiva en 'InPrivateAndRegular', se permite la autenticación del ambiente para las sesiones regulares y de InPrivate. No se permitirá la autenticación ambiental para las sesiones de invitado.

Si se establece la directiva en 'GuestAndRegular', se permite la autenticación del ambiente para sesiones regulares y de invitado. Las sesiones de InPrivate no podrán autenticarse de forma ambiental

Si se establece la directiva en 'All', se permite la autenticación del ambiente para todas las sesiones.

Ten en cuenta que siempre se permite la autenticación del ambiente en los perfiles regulares.

En Microsoft Edge, versión 81 y versiones posteriores, si la directiva no está establecida, la autenticación del ambiente se habilitará solo en sesiones regulares.

Asignación de opciones de directiva:

* RegularOnly (0) = Habilitar la autenticación de ambiente solo en sesiones normales

* InPrivateAndRegular (1) = Habilitar la autenticación de ambiente en sesiones normales e InPrivate

* GuestAndRegular (2) = Habilitar la autenticación de ambiente en las sesiones normales y de invitado

* All (3) = Habilitar la autenticación de ambiente en sesiones normales, de invitado e InPrivate

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AmbientAuthenticationInPrivateModesEnabled
  - Nombre de la directiva de grupos: Habilitar la autenticación de ambiente para perfiles de invitados e InPrivate
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AmbientAuthenticationInPrivateModesEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AmbientAuthenticationInPrivateModesEnabled
  - Valor de ejemplo:
``` xml
<integer>0</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AppCacheForceEnabled
  #### Permite que se vuelva a activar la función de AppCache, incluso si está desactivada de forma predeterminada.
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 84 o posterior

  #### Descripción
  Si establece esta directiva como verdadera, se habilitará el AppCache e incluso cuando AppCache no esté disponible de forma predeterminada en Microsoft Edge.

.      Si establece esta directiva como falsa o no la establece, AppCache seguirá los valores predeterminados de Microsoft Edge.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AppCacheForceEnabled
  - Nombre de la directiva de grupos: Permite que se vuelva a activar la función de AppCache, incluso si está desactivada de forma predeterminada.
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AppCacheForceEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AppCacheForceEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ApplicationLocaleValue
  #### Establecer la configuración regional de aplicación
  
  
  #### Versiones admitidas:
  - En Windows desde 77 o posterior

  #### Descripción
  Establece la configuración regional de la aplicación en Microsoft Edge e impide que los usuarios cambien la configuración regional.

Si se habilita esta directiva, Microsoft Edge usará la configuración regional especificada. Si no se admite la configuración regional configurada, se usará 'en-US' en su lugar.

Si se deshabilita o no se configuran estos ajustes, Microsoft Edge usará la configuración regional preferida especificada por el usuario (si está configurada) o la configuración regional de reserva 'en-US'.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ApplicationLocaleValue
  - Nombre de la directiva de grupos: Establecer la configuración regional de aplicación
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: ApplicationLocaleValue
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"en"
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AudioCaptureAllowed
  #### Permitir o bloquear la captura de audio
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite establecer si se solicita a un usuario que conceda acceso a un sitio web a su dispositivo de captura de audio. Esta directiva se aplica a todas las direcciones URL, excepto las configuradas en la lista [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Si se habilita o no se configura esta directiva (configuración predeterminada), se le pedirá al usuario acceso de captura de audio, excepto para las direcciones URL de la lista [AudioCaptureAllowedUrls](#audiocaptureallowedurls). A estas URL de la lista se les concede acceso sin pedir confirmación.

Si se deshabilita esta directiva, no se solicitará la intervención del usuario y solo se podrá tener acceso a la captura de audio en las direcciones URL configuradas en [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Esta directiva afecta a todos los tipos de entradas de audio, no solo al micrófono integrado.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AudioCaptureAllowed
  - Nombre de la directiva de grupos: Permitir o bloquear la captura de audio
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AudioCaptureAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AudioCaptureAllowed
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AudioCaptureAllowedUrls
  #### Sitios que pueden acceder a dispositivos de captura de audio sin solicitar permiso
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especificar los sitios web, según los patrones de la dirección URL, que pueden usar dispositivos de captura de audio sin pedirle permiso al usuario. Los patrones de esta lista se comparan con el origen de la seguridad de la URL de la solicitud. Si coinciden, se concederá automáticamente acceso a los dispositivos de captura de audio.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AudioCaptureAllowedUrls
  - Nombre de la directiva de grupos: Sitios que pueden acceder a dispositivos de captura de audio sin solicitar permiso
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AudioCaptureAllowedUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AudioSandboxEnabled
  #### Permitir la ejecución del espacio aislado de audio
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 81 o posterior

  #### Descripción
  Esta directiva controla el espacio aislado del proceso de audio.

Si se habilita esta directiva, el proceso de audio se ejecutará en un espacio aislado.

Si se deshabilita esta directiva, el proceso de audio se ejecutará sin espacio aislado y el módulo de procesamiento de audio WebRTC se ejecutará en el proceso de representador.
Esto deja los usuarios abiertos a riesgos de seguridad relacionados con la ejecución del subsistema de audio sin espacio aislado.

Si no se configura esta directiva, se usará la configuración predeterminada del espacio aislado de audio, que puede ser diferente según la plataforma.

Esta directiva está pensada para proporcionar flexibilidad a las empresas para deshabilitar el espacio aislado de audio si usan configuraciones de software de seguridad que interfieran con el espacio aislado.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AudioSandboxEnabled
  - Nombre de la directiva de grupos: Permitir la ejecución del espacio aislado de audio
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AudioSandboxEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AudioSandboxEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AutoImportAtFirstRun
  #### Importar automáticamente los datos y la configuración de otro explorador la primera vez que se ejecute
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Si habilitas esta directiva, todos los tipos de datos y configuraciones compatibles del navegador especificado se importarán silenciosa y automáticamente en la primera ejecución. Durante la primera experiencia de ejecución, también se omitirá la sección de importación.

Los datos del explorador de Microsoft Edge (versión heredada) siempre se migrarán silenciosamente durante la primera ejecución, independientemente del valor de esta directiva.

Si se establece esta directiva en 'FromDefaultBrowser', se importarán los tipos de datos correspondientes al navegador predeterminado en el dispositivo administrado.

Si el explorador especificado como el valor de esta directiva no está presente en el dispositivo administrado, Microsoft Edge simplemente omitirá la importación sin que se notifique al usuario.

Si se establece esta directiva en 'DisabledAutoImport', la sección de importación de la experiencia de primera ejecución se omite completamente y Microsoft Edge no importa los datos ni la configuración del explorador automáticamente.

Si esta directiva se establece en el valor 'FromInternetExplorer', se importarán los siguientes tipos de datos de Internet Explorer:
1. Favoritos o marcadores
2. Contraseñas guardadas
3. Motores de búsqueda
4. Historial de exploración
5. Página principal

Si esta directiva se establece en el valor 'FromGoogleChrome', se importarán los siguientes tipos de datos de Google Chrome:
1. Favoritos
2. Contraseñas guardadas
3. Direcciones y más
4. Información de pago
5. Historial de exploración
6. Configuración
7. Pestañas ancladas y abiertas
8. Extensiones
9. Cookies

Nota: Para obtener más detalles de lo que se importa de Google Chrome consulta [https://go.microsoft.com/fwlink/?linkid=2120835](https://go.microsoft.com/fwlink/?linkid=2120835)

Si esta directiva se establece en el valor 'FromSafari', los datos del usuario ya no se importarán a Microsoft Edge. Esto se debe a la forma en que el acceso total al disco funciona en Mac.
En macOS Mojave y versiones posteriores, ya no es posible la importación automática y desatendida de datos de Safari a Microsoft Edge.

A partir de Microsoft Edge, versión 83, si esta directiva se establece en el valor 'FromMozillaFirefox' se importarán los siguientes tipos de datos de Mozilla Firefox:
1. Favoritos o marcadores
2. Contraseñas guardadas
3. Direcciones y más
4. Historial de exploración

Si quieres restringir tipos de datos específicos de la importación en los dispositivos administrados, puedes usar esta directiva con otras directivas, como [ImportAutofillFormData](#importautofillformdata), [ImportBrowserSettings](#importbrowsersettings), [ImportFavorites](#importfavorites), etc.

Asignación de opciones de directiva:

* FromDefaultBrowser (0) = Importa automáticamente todos los tipos de datos y configuraciones compatibles del explorador predeterminado

* FromInternetExplorer (1) = Importa automáticamente todos los tipos de datos y configuraciones compatibles de Internet Explorer

* FromGoogleChrome (2) = Importa automáticamente todos los tipos de datos y configuraciones compatibles de Google Chrome

* FromSafari (3) = Importa automáticamente todos los tipos de datos y configuraciones compatibles de Safari

* DisabledAutoImport (4) = Deshabilita la importación automática y se omite la sección de importación de la experiencia de primera ejecución

* FromMozillaFirefox (5) = Importe automáticamente todos los tipos de datos y configuraciones soportadas de Mozilla Firefox

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AutoImportAtFirstRun
  - Nombre de la directiva de grupos: Importar automáticamente los datos y la configuración de otro explorador la primera vez que se ejecute
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AutoImportAtFirstRun
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AutoImportAtFirstRun
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AutoLaunchProtocolsFromOrigins
  #### Defina una lista de protocolos que pueden iniciar una aplicación externa desde los orígenes enumerados sin preguntar al usuario
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 85 o posterior

  #### Descripción
  Permite configurar una lista de protocolos y, para cada protocolo, una lista asociada de patrones de origen permitidos que pueden iniciar una aplicación externa sin tener que preguntar al usuario. El separador final no se debe incluir cuando se enumera el protocolo. Por ejemplo, incluye "skype" en lugar de "skype:" o "skype://".

Si configuras esta directiva, solo se permitirá que un protocolo inicie una aplicación externa sin tener que la directiva pregunte si:

- el protocolo se muestra

- el origen del sitio que intenta iniciar el protocolo coincide con uno de los patrones de origen de esa lista de allowed_origins del protocolo.

Si cualquiera de las condiciones es false, el mensaje de inicio del protocolo externo no se omitirá por directiva.

Si no configuras esta directiva, no se podrán iniciar protocolos sin pedir confirmación. Los usuarios pueden optar por no recibir mensajes en función de cada protocolo o sitio, salvo que la directiva [ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox) se configure como deshabilitada. Esta Directiva no afecta a las exenciones de mensaje por protocolo/por sitio establecidas por los usuarios.

Los modelos de coincidencia de origen usan un formato similar a los de la directiva [URLBlocklist](#urlblocklist), que se describen en [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Sin embargo, los patrones de coincidencia de origen para esta directiva no pueden contener elementos "/path" o "@query". Cualquier patrón que contenga un elemento "/path" o "@query" se omitirá.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Diccionario

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AutoLaunchProtocolsFromOrigins
  - Nombre de la directiva de grupos: Defina una lista de protocolos que pueden iniciar una aplicación externa desde los orígenes enumerados sin preguntar al usuario
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AutoLaunchProtocolsFromOrigins
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
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


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AutoLaunchProtocolsFromOrigins
  - Valor de ejemplo:
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
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AutoOpenAllowedForURLs
  #### URL donde se puede aplicar AutoOpenFileTypes
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 85 o posterior

  #### Descripción
  Una lista de direcciones URL a las que se aplicará [AutoOpenFileTypes](#autoopenfiletypes). Esta directiva no tiene ningún impacto en los valores abiertos automáticamente establecidos por los usuarios a través del estante de descarga... > Entrada de menú "Abrir siempre archivos de este tipo".

Si configuras las direcciones URL en esta directiva, los archivos solo se abrirán automáticamente por la directiva si la URL forma parte de este conjunto y el tipo de archivo aparece en [AutoOpenFileTypes](#autoopenfiletypes). Si cualquiera de las condiciones es falsa, la descarga no se abrirá automáticamente por la directiva.

Si no configuras esta directiva, todas las descargas donde se encuentre el tipo de archivo en [AutoOpenFileTypes](#autoopenfiletypes) se abrirán automáticamente.

Un patrón de URL debe tener un formato de acuerdo con [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AutoOpenAllowedForURLs
  - Nombre de la directiva de grupos: URL donde se puede aplicar AutoOpenFileTypes
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\1 = "example.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\5 = ".exact.hostname.com"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AutoOpenAllowedForURLs
  - Valor de ejemplo:
``` xml
<array>
  <string>example.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AutoOpenFileTypes
  #### Lista de tipos de archivo que se deben abrir automáticamente al descargarse
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 85 o posterior

  #### Descripción
  Esta directiva establece una lista de los tipos de archivo que deberían abrirse automáticamente en la descarga. Nota: el separador principal no debe incluirse al enumerar el tipo de archivo, por lo que debe incluir "txt" en lugar de ".txt".

De forma predeterminada, estos tipos de archivos se abrirán automáticamente en todas las URL. Puede usar la directiva [AutoOpenAllowedForURLs](#autoopenallowedforurls) para restringir las URL para las que se abrirán automáticamente estos tipos de archivos.

Los archivos cuyos tipos deberían abrirse automáticamente estarán sujetos a las comprobaciones habilitadas de SmartScreen de Microsoft Defender y no se abrirán si fallan esas comprobaciones.

Los tipos de archivo que un usuario ya ha especificado para abrirse automáticamente continuarán haciéndolo cuando se descarguen. El usuario continuará pudiendo especificar otros tipos de archivos que se abrirán automáticamente.

Si no establece esta directiva, solo los tipos de archivos que un usuario ya ha especificado para que se abran automáticamente lo harán cuando se descarguen.

Esta directiva solo está disponible en instancias de Windows que estén unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise que estén inscritas para la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AutoOpenFileTypes
  - Nombre de la directiva de grupos: Lista de tipos de archivo que se deben abrir automáticamente al descargarse
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\1 = "exe"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\2 = "txt"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AutoOpenFileTypes
  - Valor de ejemplo:
``` xml
<array>
  <string>exe</string>
  <string>txt</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AutofillAddressEnabled
  #### Habilitar Autorrellenar para direcciones
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Habilita la característica de Autorrellenar y permite a los usuarios rellenar automáticamente la información de dirección en formularios web con información previamente almacenada.

Si se deshabilita esta directiva, Autorrellenar nunca sugiere o escribe información sobre la dirección ni guarda información adicional sobre la dirección que el usuario podría enviar durante la exploración web.

Si se habilita esta directiva o no se configura, los usuarios pueden controlar Autorrellenar para direcciones en la interfaz de usuario.

Tenga en cuenta que si se deshabilita esta directiva, también se detendrán todas las actividades de todos los formularios web, excepto los formularios de pago y contraseña. No se guardarán más entradas y Microsoft Edge no sugerirá ni rellenará automáticamente las entradas anteriores.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AutofillAddressEnabled
  - Nombre de la directiva de grupos: Habilitar Autorrellenar para direcciones
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: AutofillAddressEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AutofillAddressEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AutofillCreditCardEnabled
  #### Habilitar Autorrellenar para tarjetas de crédito
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Habilita la característica Autorrellenar de Microsoft Edge y permite a los usuarios rellenar de forma automática la información de tarjetas de crédito en formularios web con la información almacenada anteriormente.

Si se deshabilita esta directiva, Autorrellenar nunca sugerirá ni rellenará la información de tarjetas de crédito y tampoco guardará la información adicional de estas que los usuarios podrían enviar al explorar la web.

Si se habilita o no se configura esta directiva, los usuarios pueden controlar la característica Autorrellenar para tarjetas de crédito.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AutofillCreditCardEnabled
  - Nombre de la directiva de grupos: Habilitar Autorrellenar para tarjetas de crédito
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: AutofillCreditCardEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AutofillCreditCardEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### AutoplayAllowed
  #### Permitir la reproducción automática de multimedia para sitios web
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 78 o posterior

  #### Descripción
  Esta directiva establece la directiva de reproducción automática de multimedia para sitios web.

La configuración predeterminada, "No configurado" respeta la configuración actual de reproducción automática de multimedia y permite a los usuarios configurar su configuración de reproducción automática.

Al establecer la opción "Habilitado", la reproducción automática de multimedia se establece en "Permitir".  Todos los sitios web tienen permiso para reproducir contenido multimedia. Los usuarios no pueden invalidar esta directiva.

Si se establece la opción "Deshabilitado", la reproducción automática de multimedia se establece en "Bloquear".  Ningún sitio web tiene permiso para reproducir contenido multimedia. Los usuarios no pueden invalidar esta directiva.

Es necesario cerrar una pestaña y volver a abrirla para que esta directiva surta efecto.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: AutoplayAllowed
  - Nombre de la directiva de grupos: Permitir la reproducción automática de multimedia para sitios web
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: AutoplayAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: AutoplayAllowed
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### BackgroundModeEnabled
  #### Continúa con la ejecución de aplicaciones en segundo plano después de cerrar Microsoft Edge
  
  
  #### Versiones admitidas:
  - En Windows desde 77 o posterior

  #### Descripción
  Permite que los procesos de Microsoft Edge comiencen con el inicio de sesión del sistema operativo y sigan ejecutándose cuando se cierre la última ventana del navegador. En este escenario, las aplicaciones en segundo plano y la sesión de exploración actual permanecen activas, incluidas las cookies de la sesión. Un proceso abierto en segundo plano muestra un icono en la bandeja del sistema y siempre se puede cerrar desde allí.

Si se habilita esta directiva, se activará el modo de segundo plano.

Si se deshabilita esta directiva, se desactivará el modo de segundo plano.

Si no se configura esta directiva, el modo de segundo plano estará desactivado inicialmente y el usuario puede configurar su comportamiento en edge://settings/system.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: BackgroundModeEnabled
  - Nombre de la directiva de grupos: Continúa con la ejecución de aplicaciones en segundo plano después de cerrar Microsoft Edge
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: BackgroundModeEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### BackgroundTemplateListUpdatesEnabled
  #### Habilita actualizaciones en segundo plano para la lista de plantillas disponibles para Colecciones y otras características que usan plantillas.
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 79 o posterior

  #### Descripción
  Permite habilitar o deshabilitar las actualizaciones en segundo plano de la lista de plantillas disponibles para Colecciones y otras características que usan plantillas. Las plantillas se usan para extraer metadatos enriquecidos de una página web cuando la página se guarda en una colección.

Si habilita esta configuración o si la configuración no está configurada, la lista de plantillas disponibles se descargará en segundo plano desde un servicio Microsoft cada 24 horas.

Si deshabilita esta configuración, la lista de plantillas disponibles se descargará a petición. Este tipo de descarga puede dar lugar a pequeñas penalizaciones de rendimiento para Colecciones y otras características.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: BackgroundTemplateListUpdatesEnabled
  - Nombre de la directiva de grupos: Habilita actualizaciones en segundo plano para la lista de plantillas disponibles para Colecciones y otras características que usan plantillas.
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: BackgroundTemplateListUpdatesEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: BackgroundTemplateListUpdatesEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### BingAdsSuppression
  #### Bloquear todos los anuncios en los resultados de búsqueda de Bing
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 83 o posterior

  #### Descripción
  Habilita una experiencia de búsqueda sin anuncios en Bing.com

Si habilita esta directiva, un usuario puede buscar en bing.com y tener una experiencia de búsqueda sin anuncios. Al mismo tiempo, la configuración de Búsqueda segura se establecerá en "estricto" y el usuario no podrá cambiarlo.

Si no configura esta directiva, la experiencia predeterminada tendrá anuncios en los resultados de la búsqueda en bing.com. Búsqueda segura se establecerá en "moderado" de forma predeterminada y el usuario podrá cambiarlo.

Esta directiva solo está disponible para las SKU de la K-12 que Microsoft identificó como espacios empresariales de EDU.

Consulte [https://go.microsoft.com/fwlink/?linkid=2119711](https://go.microsoft.com/fwlink/?linkid=2119711) para obtener más información sobre esta directiva o si se aplican los siguientes escenarios en su caso:

* Tiene un espacio empresarial de EDU, pero la directiva no funciona.

* Agregó la IP a la lista de permitidos para tener una experiencia de búsqueda sin anuncios.

* Estaba experimentando una experiencia de búsqueda sin anuncios en Microsoft Edge (versión heredada) y quiere actualizar a la nueva versión de Microsoft Edge.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: BingAdsSuppression
  - Nombre de la directiva de grupos: Bloquear todos los anuncios en los resultados de búsqueda de Bing
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: BingAdsSuppression
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: BingAdsSuppression
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### BlockThirdPartyCookies
  #### Bloquear cookies de terceros
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Bloquee los elementos de la página web que no pertenezcan al dominio que se encuentra en la barra de direcciones del establecimiento de cookies.

Si habilita esta directiva, los elementos de la página web que no pertenecen al dominio que se encuentra en la barra de direcciones no podrán establecer cookies

Si deshabilita esta directiva, los elementos de la página web de otros dominios que no se encuentran en la barra de direcciones podrán establecer cookies.

Si no configura esta directiva, las cookies de terceros están habilitadas, pero los usuarios podrán cambiar esta configuración.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: BlockThirdPartyCookies
  - Nombre de la directiva de grupos: Bloquear cookies de terceros
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: BlockThirdPartyCookies
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: BlockThirdPartyCookies
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### BrowserAddProfileEnabled
  #### Habilitar la creación de perfiles desde el menú desplegable Identidad o la página de configuración
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permitir a los usuarios crear nuevos perfiles mediante la opción **Agregar perfil**.
Si se habilita esta directiva o no se configura, Microsoft Edge permite a los usuarios usar **Agregar perfil** en el menú flotante de identidad o en la página de configuración para crear nuevos perfiles.

Si se deshabilita esta directiva, los usuarios no podrán agregar nuevos perfiles desde el menú flotante de identidad o desde la página de configuración.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: BrowserAddProfileEnabled
  - Nombre de la directiva de grupos: Habilitar la creación de perfiles desde el menú desplegable Identidad o la página de configuración
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: BrowserAddProfileEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: BrowserAddProfileEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### BrowserGuestModeEnabled
  #### Habilitar el modo Invitado
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Habilita la opción de permitir el uso de perfiles de invitados en Microsoft Edge. En un perfil de invitado, el explorador no importa los datos de exploración de los perfiles existentes y elimina los datos de exploración cuando se cierran todos los perfiles de invitados.

Si se habilita esta directiva o no se configura, Microsoft Edge permite a los usuarios examinar los perfiles de invitados.

Si se deshabilita esta directiva, Microsoft Edge no permite a los usuarios examinar los perfiles de invitados.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: BrowserGuestModeEnabled
  - Nombre de la directiva de grupos: Habilitar el modo Invitado
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: BrowserGuestModeEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: BrowserGuestModeEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### BrowserNetworkTimeQueriesEnabled
  #### Permitir consultas a un servicio de hora de red de explorador
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Impide que Microsoft Edge envíe consultas ocasionalmente a un servicio de hora de la red de explorador para recuperar una marca de tiempo precisa.

Si se deshabilita esta directiva, Microsoft Edge dejará de enviar consultas a un servicio de hora de la red de explorador.

Si se habilita esta directiva o no se configura, Microsoft Edge enviará consultas ocasionalmente a un servicio de hora de la red de explorador.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: BrowserNetworkTimeQueriesEnabled
  - Nombre de la directiva de grupos: Permitir consultas a un servicio de hora de red de explorador
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: BrowserNetworkTimeQueriesEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: BrowserNetworkTimeQueriesEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### BrowserSignin
  #### Configuración de inicio de sesión del explorador
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica si un usuario puede iniciar sesión en Microsoft Edge con su cuenta y usar los servicios relacionados con la cuenta, como sincronizar e inicio de sesión único. Para controlar la disponibilidad de la sincronización, usa la directiva [SyncDisabled](#syncdisabled) en su lugar.

Si se establece esta directiva en 'Disable', asegúrate de que también estableces la directiva [NonRemovableProfileEnabled](#nonremovableprofileenabled) en Deshabilitado porque [NonRemovableProfileEnabled](#nonremovableprofileenabled) deshabilita la creación de un perfil del explorador con sesión iniciada automáticamente. Si se establecen las dos directivas, Microsoft Edge usará la directiva 'Deshabilitar el inicio de sesión del explorador' y se comportará como si [NonRemovableProfileEnabled](#nonremovableprofileenabled) estuviese establecida en Deshabilitado.

Si se establece esta directiva en 'Enable', los usuarios podrán iniciar sesión en el explorador. Iniciar sesión en el explorador no significa que la sincronización esté activada de manera predeterminada; el usuario debe decidir participar por separado para usar esta característica.

Si se establece esta directiva en 'Force', los usuarios deberán iniciar sesión en un perfil para usar el explorador. De manera predeterminada, esto permitirá al usuario elegir si quiere sincronizar con su cuenta, a menos que el administrador del dominio o la directiva [SyncDisabled](#syncdisabled) deshabiliten la sincronización. El valor predeterminado de la directiva [BrowserGuestModeEnabled](#browserguestmodeenabled) se ha establecido en false.

Si no se configura esta directiva, los usuarios podrán decidir si quieren habilitar la opción de inicio de sesión del explorador y usarla como consideren adecuado.

Asignación de opciones de directiva:

* Disable (0) = Deshabilitar inicio de sesión del explorador

* Enable (1) = Habilitar el inicio de sesión del explorador

* Force (2) = Forzar el inicio de sesión para usar el explorador

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: BrowserSignin
  - Nombre de la directiva de grupos: Configuración de inicio de sesión del explorador
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: BrowserSignin
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: BrowserSignin
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### BuiltInDnsClientEnabled
  #### Usar el cliente DNS integrado
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Controla si se debe usar el cliente DNS integrado.

Esto no afecta a los servidores DNS que se usan; solo a la pila de software que se usa para comunicarse con ellos. Por ejemplo, si el sistema operativo está configurado para usar un servidor DNS de la empresa, el cliente DNS integrado usará ese mismo servidor. Sin embargo, es posible que el cliente DNS integrado vaya a los servidores de distintas formas usando protocolos más modernos relacionados con DNS, como por ejemplo DNS sobre TLS.

Si se habilita esta directiva, se usará el cliente DNS integrado si está disponible.

Si se deshabilita esta directiva, el cliente no se usará nunca.

Si no se configura esta directiva, el cliente DNS integrado se habilitará de manera predeterminada en MacOS y los usuarios podrán cambiar si usan el cliente DNS integrado editando edge://flags o especificando una marca de línea de comandos.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: BuiltInDnsClientEnabled
  - Nombre de la directiva de grupos: Usar el cliente DNS integrado
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: BuiltInDnsClientEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: BuiltInDnsClientEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### BuiltinCertificateVerifierEnabled
  #### Determina si se usará el comprobador de certificados integrado para comprobar los certificados de servidor (en desuso)
  >EN DESUSO: esta directiva está en desuso. Actualmente se admite pero será obsoleta en una versión futura.
  
  #### Versiones admitidas:
  - En macOS desde 83 o posterior

  #### Descripción
  Esta directiva es obsoleta porque tiene por objeto servir únicamente como mecanismo a corto plazo para dar a las empresas más tiempo para actualizar sus entornos e informar de los problemas si se comprueba que son incompatibles con el verificador de certificados incorporado.

No funcionará en la versión 87 de Microsoft Edge, para la que está previsto que se elimine el soporte para el verificador de certificados heredados en Mac OS X.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  

  #### Información y configuración de Mac
  - Nombre de clave de preferencia: BuiltinCertificateVerifierEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### CertificateTransparencyEnforcementDisabledForCas
  #### Deshabilitar el cumplimiento de la transparencia de certificados para obtener una lista de hashes subjectPublicKeyInfo
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Deshabilita la aplicación de los requisitos de transparencia de certificado para una lista de hash de subjectPublicKeyInfo.

Esta directiva te permite deshabilitar los requisitos de divulgación de la transparencia de certificados para cadenas de certificados que contienen certificados con uno de los hash de subjectPublicKeyInfo especificados. Esto permite que los certificados que, de lo contrario, no serían de confianza porque no se habían divulgado correctamente, se puedan usar en los hosts de Enterprise.

Para deshabilitar la aplicación de la transparencia de certificados cuando se establece esta directiva, se debe cumplir uno de los siguientes conjuntos de condiciones:
1. El hash es de la subjectPublicKeyInfo del certificado del servidor.
2. El hash es de una subjectPublicKeyInfo que aparece en un Certificado CA de la cadena de certificados, este Certificado CA está restringido mediante la extensión nameConstraints X.509v3, uno o varios nameConstraints de directoryName están presentes en los permittedSubtrees y el directoryName contiene un atributo de organizationName.
3. El hash es de una subjectPublicKeyInfo que aparece en un Certificado CA de la cadena de certificados, el Certificado CA tiene uno o más atributos de organizationName en el asunto del certificado y el certificado del servidor contiene el mismo número de atributos de organizationName, en el mismo orden y con valores idénticos byte por byte.

Un hash de subjectPublicKeyInfo se especifica concatenando el nombre del algoritmo hash, el carácter "/" y la codificación Base64 de dicho algoritmo hash aplicado a la subjectPublicKeyInfo codificada con DER del certificado especificado. Esta codificación Base64 tiene el mismo formato que una huella digital SPKI, como se define en la sección 2.4 de RFC 7469. Los algoritmos hash no reconocidos se omiten. El único algoritmo hash admitido en este momento es "SHA256".

Si se deshabilita esta directiva o no se configura, cualquier certificado que deba ser divulgado a través de la transparencia del certificado se tratará como de no confianza si no se divulga de acuerdo con la directiva de transparencia del certificado.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: CertificateTransparencyEnforcementDisabledForCas
  - Nombre de la directiva de grupos: Deshabilitar el cumplimiento de la transparencia de certificados para obtener una lista de hashes subjectPublicKeyInfo
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\2 = "sha256//////////////////////w=="

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: CertificateTransparencyEnforcementDisabledForCas
  - Valor de ejemplo:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### CertificateTransparencyEnforcementDisabledForLegacyCas
  #### Deshabilitar la aplicación de la transparencia de certificados para una lista de entidades de certificación heredadas
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Deshabilita la aplicación de los requisitos de transparencia de certificado para una lista de entidades de certificación (CA) heredadas.

Esta directiva permite deshabilitar los requisitos de divulgación de la transparencia de certificados para cadenas de certificados que contienen certificados con uno de los hash de subjectPublicKeyInfo especificados. Esto permite que los certificados que de otro modo no eran de confianza debido a que no se divulgaran correctamente, sigan usándose para los hosts de la empresa.

Para que la aplicación de la transparencia se deshabilite, debe establecer el algoritmo hash en un subjectPublicKeyInfo que aparezca en un Certificado CA reconocido como una entidad de certificación (CA) heredada. Una CA heredada es una CA de confianza pública de forma predeterminada por parte de uno o varios sistemas operativos compatibles con Microsoft Edge.

Puede especificar un hash subjectPublicKeyInfo concatenando el nombre del algoritmo hash, el carácter "/" y la codificación Base64 de ese algoritmo hash aplicado a la subjectPublicKeyInfo codificada con DER del certificado especificado. Esta codificación Base64 tiene el mismo formato que una huella digital SPKI, como se define en la sección 2,4 de RFC 7469. Se omiten los algoritmos hash no reconocidos. El único algoritmo hash admitido en este momento es "SHA256".

Si no se configuras esta directiva, todos los certificados que se deban divulgar a través de la transparencia de certificados se tratarán como no de confianza si no se divulgan según la directiva de transparencia de certificados.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Nombre de la directiva de grupos: Deshabilitar la aplicación de la transparencia de certificados para una lista de entidades de certificación heredadas
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\2 = "sha256//////////////////////w=="

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Valor de ejemplo:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### CertificateTransparencyEnforcementDisabledForUrls
  #### Deshabilitar el cumplimiento de transparencia de certificados para direcciones URL específicas
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Se deshabilitan los requisitos de transparencia de certificado para las direcciones URL que aparecen en la lista.

Esta directiva te permite no divulgar certificados para los nombres de host en la dirección URL a través de la transparencia del certificado. Esto te permitirá usar certificados que, de lo contrario, no serían de confianza, debido a que no se divulgaron públicamente de manera correcta, pero resulta más difícil de detectar los certificados que no se emitieron correctamente para estos hosts.

Forma el patrón de las direcciones URL según [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Como los certificados son válidos para un nombre de host determinado, independientemente del esquema, el puerto o la ruta de acceso, solo se tendrá en cuenta la parte del nombre de host de la dirección URL. No se admiten hosts comodín.

Si no configuras esta directiva, todos los certificados que deberían divulgarse a través de la transparencia del certificado se tratarán como no de confianza si no se divulgan.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: CertificateTransparencyEnforcementDisabledForUrls
  - Nombre de la directiva de grupos: Deshabilitar el cumplimiento de transparencia de certificados para direcciones URL específicas
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\2 = ".contoso.com"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: CertificateTransparencyEnforcementDisabledForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>contoso.com</string>
  <string>.contoso.com</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ClearBrowsingDataOnExit
  #### Borrar los datos de exploración al cerrar Microsoft Edge
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 78 o posterior

  #### Descripción
  Microsoft Edge no borra los datos de exploración de manera predeterminada cuando se cierra. Los datos de exploración incluyen información escrita en formularios, contraseñas e incluso los sitios web visitados.

Si se habilita esta directiva, todos los datos de exploración se eliminan cada vez que se cierra Microsoft Edge. Tenga en cuenta que si se habilita esta directiva, esta tendrá prioridad sobre cómo se ha configurado [DefaultCookiesSetting](#defaultcookiessetting)

Si esta directiva se deshabilita o no se configura, los usuarios podrán configurar la opción Borrar los datos de exploración en Configuración.

Si se habilita esta directiva, no configure la directiva [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) ni la directiva [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit),  ya que ambas se ocupan de eliminar los datos de exploración. Si se configuran las directivas anteriores y esta directiva, se eliminarán todos los datos de exploración cuando se cierre Microsoft Edge, independientemente de cómo se haya configurado [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) o [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

Para excluir cookies para que no se eliminen al salir, configure la directiva [SaveCookiesOnExit](#savecookiesonexit).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ClearBrowsingDataOnExit
  - Nombre de la directiva de grupos: Borrar los datos de exploración al cerrar Microsoft Edge
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: ClearBrowsingDataOnExit
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ClearBrowsingDataOnExit
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ClearCachedImagesAndFilesOnExit
  #### Borrar archivos e imágenes en caché al cerrar Microsoft Edge
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 83 o posterior

  #### Descripción
  Microsoft Edge no borra los archivos y las imágenes en caché de forma predeterminada cuando se cierra.

Si se habilita esta directiva, se eliminarán las imágenes y los archivos almacenados en caché cada vez que se cierre Microsoft Edge.

Si se deshabilita esta directiva, los usuarios no pueden configurar la opción de imágenes y archivos en caché en edge://settings/clearBrowsingDataOnClose.

Si no se configura esta directiva, los usuarios pueden elegir si se borran los archivos y las imágenes en caché al salir.

Si deshabilita esta directiva, no habilite la directiva [ClearBrowsingDataOnExit](#clearbrowsingdataonexit), ya que ambas se ocupan de eliminar datos. Si configura las dos, la directiva [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) tiene prioridad y elimina todos los datos cuando Microsoft Edge se cierra, independientemente de cómo se haya configurado [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ClearCachedImagesAndFilesOnExit
  - Nombre de la directiva de grupos: Borrar archivos e imágenes en caché al cerrar Microsoft Edge
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: ClearCachedImagesAndFilesOnExit
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ClearCachedImagesAndFilesOnExit
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ClickOnceEnabled
  #### Permitir a los usuarios abrir archivos con el protocolo ClickOnce
  
  
  #### Versiones admitidas:
  - En Windows desde 78 o posterior

  #### Descripción
  Permitir a los usuarios abrir archivos con el protocolo ClickOnce. El protocolo ClickOnce permite a los sitios web solicitar que el explorador abra archivos de una dirección URL específica mediante el controlador de archivos de ClickOnce del equipo o dispositivo del usuario.

Si se habilita esta directiva, los usuarios pueden abrir archivos con el protocolo ClickOnce. Esta directiva invalida la configuración de ClickOnce del usuario en la página edge://flags/.

Si se deshabilita esta directiva, los usuarios no podrán abrir archivos con el protocolo ClickOnce. En su lugar, el archivo se guardará en el sistema de archivos usando el explorador. Esta directiva invalida la configuración de ClickOnce del usuario en la página edge://flags/.

Si no se configura esta directiva, los usuarios con versiones de Microsoft Edge anteriores a Microsoft Edge 87 no podrán abrir archivos con el protocolo ClickOnce de manera predeterminada. No obstante, tienen la opción de habilitar el uso del protocolo ClickOnce usando la página edge://flags/. Los usuarios con las versiones 87 y posteriores de Microsoft Edge pueden abrir archivos con el protocolo ClickOnce de forma predeterminada, pero tienen la opción de deshabilitar el protocolo ClickOnce en la página edge://flags/.

     La deshabilitación de ClickOnce puede impedir que las aplicaciones ClickOnce (.application files) se inicien correctamente.

Para obtener más información sobre ClickOnce, consulte [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) and [https://go.microsoft.com/fwlink/?linkid=2099880](https://go.microsoft.com/fwlink/?linkid=2099880).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ClickOnceEnabled
  - Nombre de la directiva de grupos: Permitir a los usuarios abrir archivos con el protocolo ClickOnce
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ClickOnceEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### CollectionsServicesAndExportsBlockList
  #### Bloquear el acceso a una lista específica de servicios y destinos de exportación en colecciones
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Mostrar servicios específicos y destinos de exportación a los que los usuarios no pueden obtener acceso en la característica de Colecciones en Microsoft Edge. Esto incluye mostrar datos adicionales de Bing y exportar colecciones a productos de Microsoft o socios externos.

Si habilitas esta directiva, los servicios y destinos de exportación que coincidan con la lista determinada estarán bloqueados.

     Si no configuras esta directiva, no se aplican restricciones en los servicios aceptables y los objetivos de exportación.

Asignación de opciones de directiva:

* pinterest_suggestions (pinterest_suggestions) = Sugerencias de Pinterest

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: CollectionsServicesAndExportsBlockList
  - Nombre de la directiva de grupos: Bloquear el acceso a una lista específica de servicios y destinos de exportación en colecciones
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\1 = "pinterest_suggestions"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: CollectionsServicesAndExportsBlockList
  - Valor de ejemplo:
``` xml
<array>
  <string>pinterest_suggestions</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### CommandLineFlagSecurityWarningsEnabled
  #### Habilitar advertencias de seguridad para marcadores de la línea de comandos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 78 o posterior

  #### Descripción
  Si se deshabilita, esta directiva impide que las advertencias de seguridad aparezcan cuando Microsoft Edge se inicie con marcas de línea de comandos potencialmente peligrosas.

Si se habilita o no se establece esta opción, se muestran advertencias de seguridad cuando se usan estas marcas de línea de comandos para iniciar Microsoft Edge.

Por ejemplo, la marca--disable-gpu-sandbox genera esta advertencia: Está usando una marca de línea de comandos no admitida: --disable-gpu-sandbox. Esto supone un riesgo de seguridad y de estabilidad.

Esta directiva solo está disponible en las instancias de Windows que están unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise que están inscritas para la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: CommandLineFlagSecurityWarningsEnabled
  - Nombre de la directiva de grupos: Habilitar advertencias de seguridad para marcadores de la línea de comandos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: CommandLineFlagSecurityWarningsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: CommandLineFlagSecurityWarningsEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ComponentUpdatesEnabled
  #### Habilitar actualizaciones de componentes en Microsoft Edge
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Si se habilita o no se configura esta directiva, las actualizaciones de componentes estarán habilitadas en Microsoft Edge.

Si se deshabilita esta directiva o se establece en false, se deshabilitarán las actualizaciones de componentes para todos los componentes de Microsoft Edge.

Sin embargo, algunos componentes están exentos de esta directiva. Esto incluye todos los componentes que no contengan código ejecutable, que no modifica significativamente el comportamiento del explorador o que es crítico para la seguridad. Es decir, las actualizaciones que se consideran "críticas para la seguridad" se siguen aplicando incluso si se deshabilita esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ComponentUpdatesEnabled
  - Nombre de la directiva de grupos: Habilitar actualizaciones de componentes en Microsoft Edge
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ComponentUpdatesEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ComponentUpdatesEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ConfigureDoNotTrack
  #### Configurar No realizar seguimiento
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifique si quiere enviar solicitudes de No realizar seguimiento a sitios web que pidan información de seguimiento. Las solicitudes de No realizar seguimiento permiten que los sitios web que visite sepan que no quiere que se realice un seguimiento de su actividad de exploración. De manera predeterminada, Microsoft Edge no enviará solicitudes de No realizar seguimiento, pero los usuarios pueden activar esta característica para enviarlas.

Si se habilita esta directiva, siempre se enviarán solicitudes de No realizar seguimiento a los sitios web que pidan información de seguimiento.

Si se deshabilita esta directiva, nunca se enviarán solicitudes.

Si no se configura esta directiva, los usuarios podrán elegir si quieren enviar estas solicitudes.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ConfigureDoNotTrack
  - Nombre de la directiva de grupos: Configurar No realizar seguimiento
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ConfigureDoNotTrack
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ConfigureDoNotTrack
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ConfigureOnPremisesAccountAutoSignIn
  #### Configurar el inicio de sesión automático con una cuenta de dominio de Active Directory cuando no hay ninguna cuenta de dominio de Azure AD
  
  
  #### Versiones admitidas:
  - En Windows desde 81 o posterior

  #### Descripción
  Habilita el uso de cuentas de Active Directory para el inicio de sesión automático si las máquinas de los usuarios están unidas a un dominio y el ambiente no está unido a híbrido. Si quieres que los usuarios inicien sesión automáticamente con sus cuentas de Azure Active Directory, une tu ambiente a Azure AD (consulta [https://go.microsoft.com/fwlink/?linkid=2118197](https://go.microsoft.com/fwlink/?linkid=2118197) para obtener más información) o a híbrido (consulta [https://go.microsoft.com/fwlink/?linkid=2118365](https://go.microsoft.com/fwlink/?linkid=2118365) para más información).

Si has configurado la directiva [BrowserSignin](#browsersignin) en deshabilitada, esta directiva no tendrá ningún efecto.

Si se habilita esta directiva y se establece en 'SignInAndMakeDomainAccountNonRemovable', Microsoft Edge iniciará sesión automáticamente para los usuarios que estén en máquinas unidas a un dominio mediante sus cuentas de Active Directory.

Si se establece esta directiva en 'Disabled' o no se configura, Microsoft Edge no iniciará sesión automáticamente para los usuarios que estén en máquinas unidas a un dominio con cuentas de Active Directory.

Asignación de opciones de directiva:

* Disabled (0) = Deshabilitado

* SignInAndMakeDomainAccountNonRemovable (1) = Iniciar sesión y hacer que la cuenta de dominio no sea extraíble

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ConfigureOnPremisesAccountAutoSignIn
  - Nombre de la directiva de grupos: Configurar el inicio de sesión automático con una cuenta de dominio de Active Directory cuando no hay ninguna cuenta de dominio de Azure AD
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ConfigureOnPremisesAccountAutoSignIn
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ConfigureOnlineTextToSpeech
  #### Configurar texto a voz en línea
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Establecer si el explorador puede sacar provecho de las fuentes de voz de Texto a voz en línea, parte de Azure Cognitive Services. Estas fuentes de voz son de mejor calidad que las fuentes de voz del sistema instaladas previamente.

Si se habilita o no se configura esta directiva, las aplicaciones basadas en web que usan la API SpeechSynthesis podrán usar las fuentes de voz de Texto a voz en línea.

Si se deshabilita esta directiva, las fuentes de voz no estarán disponibles.

Obtenga más información acerca de esta característica aquí:
SpeechSynthesis API: [https://go.microsoft.com/fwlink/?linkid=2110038](https://go.microsoft.com/fwlink/?linkid=2110038)
Cognitive Services: [https://go.microsoft.com/fwlink/?linkid=2110141](https://go.microsoft.com/fwlink/?linkid=2110141)

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ConfigureOnlineTextToSpeech
  - Nombre de la directiva de grupos: Configurar texto a voz en línea
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ConfigureOnlineTextToSpeech
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ConfigureOnlineTextToSpeech
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ConfigureShare
  #### Configurar la experiencia de uso compartido
  
  
  #### Versiones admitidas:
  - En Windows desde 83 o posterior

  #### Descripción
  Si estableces esta directiva en 'ShareAllowed' (el valor predeterminado), los usuarios podrán acceder a la experiencia de uso compartido de Windows 10 desde el menú configuración y más en Microsoft Edge para compartirlo con otras aplicaciones del sistema.

Si estableces esta directiva en 'ShareDisallowed', los usuarios no podrán tener acceso a la experiencia de uso compartido de Windows 10. Si el botón Compartir se encuentra en la barra de herramientas, también se ocultará.

Asignación de opciones de directiva:

* ShareAllowed (0) = Permitir el uso de la experiencia de uso compartido

* ShareDisallowed (1) = No permitir el uso de la experiencia de uso compartido

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ConfigureShare
  - Nombre de la directiva de grupos: Configurar la experiencia de uso compartido
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ConfigureShare
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### CustomHelpLink
  #### Especificar vínculo de ayuda personalizado
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 79 o posterior

  #### Descripción
  Especificar un vínculo para el menú Ayuda o la tecla F1.

Si habilita esta directiva, un administrador puede especificar un vínculo para el menú Ayuda o la tecla F1.

Si deshabilita o no configura esta directiva, se usará el vínculo predeterminado para el menú Ayuda o la tecla F1.

Esta directiva solo está disponible en las instancias de Windows que estén unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise que estén inscritas en la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: CustomHelpLink
  - Nombre de la directiva de grupos: Especificar vínculo de ayuda personalizado
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: CustomHelpLink
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"https://go.microsoft.com/fwlink/?linkid=2080734"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: CustomHelpLink
  - Valor de ejemplo:
``` xml
<string>https://go.microsoft.com/fwlink/?linkid=2080734</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DNSInterceptionChecksEnabled
  #### Comprobaciones de interceptación de DNS habilitadas
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 80 o posterior

  #### Descripción
  Esta directiva configura un conmutador local que se puede usar para deshabilitar las comprobaciones de interceptación de DNS. Estas comprobaciones intentan detectar si el explorador está detrás de un proxy que redirige nombres de host desconocidos.

Es posible que esta detección no sea necesaria en un entorno empresarial donde se conozca la configuración de red. Se puede deshabilitar para evitar tráfico DNS y HTTP adicional en el inicio y en cada cambio de configuración de DNS.

Si se habilita o no se establece esta directiva, se realizarán las comprobaciones de interceptación de DNS.

Si se deshabilita esta directiva, no se realizarán las comprobaciones de interceptación de DNS.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DNSInterceptionChecksEnabled
  - Nombre de la directiva de grupos: Comprobaciones de interceptación de DNS habilitadas
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DNSInterceptionChecksEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DNSInterceptionChecksEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultBrowserSettingEnabled
  #### Establecer Microsoft Edge como el explorador predeterminado
  
  
  #### Versiones admitidas:
  - En Windows 7 y macOS desde 77 o posterior

  #### Descripción
  Si estableces esta directiva en True Microsoft Edge comprueba siempre si es el navegador predeterminado en el inicio y, si es posible, se registra automáticamente.

Si estableces esta directiva en False, se impedirá que Microsoft Edge compruebe en ningún momento si es el valor predeterminado y se desactivarán los controles de usuario para esta opción.

Si no estableces esta directiva, Microsoft Edge permite a los usuarios controlar si es la opción predeterminada y, en caso contrario, si las notificaciones de usuario deberían aparecer.

Nota para administradores de Windows: esta directiva solo funciona para los equipos PC que ejecutan Windows 7. Para las versiones posteriores de Windows, es necesario implementar un archivo de "asociaciones de aplicaciones predeterminadas" que convierte a Microsoft Edge en el controlador para los protocolos https y http (y, opcionalmente, el protocolo ftp y formatos de archivo como .html, .htm, .pdf, .svg, .webp). Para más información, consulta [https://go.microsoft.com/fwlink/?linkid=2094932](https://go.microsoft.com/fwlink/?linkid=2094932).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultBrowserSettingEnabled
  - Nombre de la directiva de grupos: Establecer Microsoft Edge como el explorador predeterminado
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DefaultBrowserSettingEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultBrowserSettingEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultSearchProviderContextMenuAccessAllowed
  #### Permitir acceso de búsqueda al menú contextual de proveedor de búsqueda predeterminado
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 85 o posterior

  #### Descripción
  Permite el uso de un proveedor de búsquedas predeterminado en el menú contextual.

Si se establece esta directiva en deshabilitado, el elemento de menú de contexto de búsqueda que se basa en el proveedor de búsqueda predeterminado y la búsqueda en la barra lateral no estarán disponibles.

Si esta directiva está configurada como habilitada o no establecida, el elemento de menú de contexto para el proveedor de búsqueda predeterminado y la búsqueda de la barra lateral estarán disponibles.

El valor de la directiva solo se aplica cuando se habilita la directiva [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) y no se aplica en caso contrario.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultSearchProviderContextMenuAccessAllowed
  - Nombre de la directiva de grupos: Permitir acceso de búsqueda al menú contextual de proveedor de búsqueda predeterminado
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DefaultSearchProviderContextMenuAccessAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultSearchProviderContextMenuAccessAllowed
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultSensorsSetting
  #### Configuración de sensores predeterminada
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Establece si los sitios web pueden obtener acceso y usar sensores, como sensores de luz y movimiento. Puedes bloquear o permitir por completo que los sitios web puedan obtener acceso a los sensores.

Establecer la directiva en 1 permite a los sitios web acceder a los sensores y usarlos. Si se establece la directiva en 2, se deniega el acceso a los sensores.

Puedes invalidar esta directiva para patrones de direcciones URL específicos mediante las directivas [SensorsAllowedForUrls](#sensorsallowedforurls) y [SensorsBlockedForUrls](#sensorsblockedforurls).

Si no configuras esta directiva, los sitios web pueden tener acceso a los sensores y usarlos, y los usuarios pueden cambiar esta configuración. Este es el valor predeterminado global para [SensorsAllowedForUrls](#sensorsallowedforurls) y [SensorsBlockedForUrls](#sensorsblockedforurls).

Asignación de opciones de directiva:

* AllowSensors (1) = Permitir que los sitios accedan a los sensores

* BlockSensors (2) = No permitir que ningún sitio obtenga acceso a los sensores

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultSensorsSetting
  - Nombre de la directiva de grupos: Configuración de sensores predeterminada
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DefaultSensorsSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultSensorsSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DefaultSerialGuardSetting
  #### Controlar el uso de la API serie
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Establece si los sitios web pueden tener acceso a los puertos serie. Puede bloquear completamente el acceso o preguntar al usuario cada vez que un sitio web quiera obtener acceso a un puerto serie.

Establecer la directiva en 3 permite que los sitios web soliciten acceso a los puertos serie. Establecer la directiva en 2 deniega el acceso a los puertos serie.

Puede invalidar esta directiva para patrones de direcciones URL específicos mediante las Directivas [SerialAskForUrls](#serialaskforurls) y[SerialBlockedForUrls](#serialblockedforurls).

Si no configura esta directiva, de forma predeterminada, los sitios web pueden preguntar a los usuarios si pueden obtener acceso a un puerto serie y los usuarios pueden cambiar esta configuración.

Asignación de opciones de directiva:

* BlockSerial (2) = No permitir que ningún sitio solicite acceso a los puertos serie a través de la API serie

* AskSerial (3) = Permitir que los sitios soliciten permisos de usuario para tener acceso a un puerto serie

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DefaultSerialGuardSetting
  - Nombre de la directiva de grupos: Controlar el uso de la API serie
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DefaultSerialGuardSetting
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DefaultSerialGuardSetting
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DelayNavigationsForInitialSiteListDownload
  #### Requerir que la lista de sitios del modo empresarial esté disponible antes que la exploración con tabulador.
  
  
  #### Versiones admitidas:
  - En Windows desde 84 o posterior

  #### Descripción
  Te permite especificar si las pestañas de Microsoft Edge esperan a que el explorador descargue la Lista de sitios inicial de Modo de empresa para navegar. Esta configuración está pensada para el escenario en el que la página principal del explorador se debe cargar en el modo de Internet Explorer y es importante que se realice en la primera ejecución del explorador después de habilitar el modo IE. Si este escenario no existe, te recomendamos que no habilites esta opción, ya que puede afectar negativamente al rendimiento de carga de la página principal. La configuración solo se aplica cuando Microsoft Edge no tiene una Lista de sitios en Modo de empresa almacenada en la caché, como en el caso de la primera ejecución después de habilitar el modo IE.

  Esta configuración funciona conjuntamente con lo siguiente:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) está establecido en 'IEMode'
 y
la directiva [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) en la que la lista tiene al menos una entrada.

  El comportamiento del tiempo de espera de esta directiva se puede configurar con la directiva [NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout).

  Si configuras esta directiva en 'All', cuando Microsoft Edge no tenga una versión en caché de la Lista de sitios del Modo de empresa, las pestañas no navegarán hasta que el explorador descargue la Lista de sitios. Los sitios configurados para abrirse en modo de Internet Explorer en la Lista de sitios se cargarán en el modo de Internet Explorer, incluso durante la navegación inicial del explorador. Los sitios que no puedan configurarse para abrirse en Internet Explorer, como cualquier sitio con un esquema distinto de http:, https:, file: o ftp: no navegarán con retraso y se cargarán inmediatamente en modo Edge.

  Si se establece esta directiva en 'None' o no se configura, cuando Microsoft Edge no tenga una versión en caché de la Lista de sitios de Modo de empresa, las pestañas navegarán inmediatamente y no esperarán a que el explorador descargue la Lista de sitios de Modo de empresa. Los sitios configurados para abrirse en el modo de Internet Explorer en la Lista de sitios se abrirán en el modo de Microsoft Edge hasta que el explorador termine de descargar la Lista de sitios de Modo de empresa.

Asignación de opciones de directiva:

* None (0) = Ninguno

* All (1) = Todas las exploraciones aptas

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DelayNavigationsForInitialSiteListDownload
  - Nombre de la directiva de grupos: Requerir que la lista de sitios del modo empresarial esté disponible antes que la exploración con tabulador.
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DelayNavigationsForInitialSiteListDownload
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DeleteDataOnMigration
  #### Eliminar los datos antiguos del explorador durante la migración
  
  
  #### Versiones admitidas:
  - En Windows desde 83 o posterior

  #### Descripción
  Esta directiva determina si los datos de navegación del usuario de Microsoft Edge El legado será eliminado después de migrar al Microsoft Edge versión 81 o posterior

Si establece esta directiva en "Activado", todos los datos de navegación de Microsoft Edge El legado después de migrar a la Microsoft EdgeEl legado después de migrar a la versión 81 o posterior será eliminado. Esta directiva debe establecerse antes de migrar a la Microsoft Edge versión 81 o posterior para tener algún efecto en los datos de navegación existentes.

Si configura esta directiva en "Desactivado", o la directiva no está configurada, los datos de navegación del usuario no se eliminan después de migrar a laMicrosoft Edge versión 83 o posterior.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DeleteDataOnMigration
  - Nombre de la directiva de grupos: Eliminar los datos antiguos del explorador durante la migración
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DeleteDataOnMigration
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DeveloperToolsAvailability
  #### Controlar dónde se pueden usar las herramientas de desarrollo
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Controla dónde se pueden usar las herramientas de desarrollo.

Si estableces esta directiva en 'DeveloperToolsDisallowedForForceInstalledExtensions' (valor predeterminado), los usuarios podrán acceder a las herramientas de desarrollo y la consola de JavaScript en general, pero no en el contexto de extensiones instaladas por la directiva de empresa.

Si estableces esta directiva en 'DeveloperToolsAllowed', los usuarios podrán acceder a las herramientas de desarrollo y la consola de JavaScript en todos los contextos, incluidas las extensiones instaladas por la directiva de empresa.

Si estableces esta directiva en 'DeveloperToolsDisallowed', los usuarios no podrán acceder a las herramientas de desarrollo ni inspeccionar los elementos del sitio web. Los métodos abreviados de teclado y las entradas de menú o de menú contextual que abren las herramientas de desarrollo o la consola de JavaScript se deshabilitarán.

Asignación de opciones de directiva:

* DeveloperToolsDisallowedForForceInstalledExtensions (0) = Bloquear las herramientas de desarrollo en extensiones instaladas por la directiva de empresa, permitir en otros contextos

* DeveloperToolsAllowed (1) = Permitir el uso de las herramientas de desarrollo

* DeveloperToolsDisallowed (2) = No permitir el uso de las herramientas de desarrollador

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DeveloperToolsAvailability
  - Nombre de la directiva de grupos: Controlar dónde se pueden usar las herramientas de desarrollo
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DeveloperToolsAvailability
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DeveloperToolsAvailability
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DiagnosticData
  #### Enviar datos de diagnóstico necesarios y opcionales sobre el uso del explorador
  
  
  #### Versiones admitidas:
  - En Windows 7 y macOS desde 86 o posterior

  #### Descripción
  Esta directiva controla el envío de datos de diagnóstico requeridos y opcionales sobre el uso del navegador a Microsoft.

 Los datos de diagnóstico requeridos se recopilan para mantener Microsoft Edge seguro, actualizado y funcionando según lo esperado.

 Los datos de diagnóstico opcionales incluyen datos sobre cómo usas el navegador, los sitios web que visitas y los informes de bloqueos a Microsoft para mejorar los productos y servicios.

 Esta directiva no es compatible con dispositivos con Windows 10. Para controlar esta recopilación de datos en Windows 10, los administradores de tecnologías de la información deben usar la directiva de grupo de datos de diagnóstico de Windows. Esta directiva será 'Permitir telemetría' o 'Permitir datos de diagnóstico', según la versión de Windows. Más información sobre la recopilación de datos de diagnóstico de Windows 10: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

 Usa una de las siguientes opciones para configurar esta directiva:

 'Off' desactiva la recopilación de datos de diagnóstico requeridos y opcionales, esta opción no está recomendada.

 'RequiredData' envía los datos de diagnóstico requeridos pero desactiva la recopilación de datos de diagnóstico opcionales. Microsoft Edge  enviará los datos de diagnóstico requeridos para mantener Microsoft Edge seguro, actualizado y con el rendimiento esperado.

  'OptionalData' envía datos de diagnóstico opcionales que incluyen datos sobre el uso del navegador, sitios web que se visitan, informes de bloqueos enviados a Microsoft para mejorar el producto y el servicio.

  En Windows 7 o macOS, esta directiva controla el envío de datos requeridos y opcionales a Microsoft.

Si no configuras esta directiva o la deshabilitas, Microsoft Edge usará la preferencia del usuario de forma predeterminada.

Asignación de opciones de directiva:

* Off (0) = Desactivado (no recomendado)

* RequiredData (1) = Datos de diagnóstico requeridos

* OptionalData (2) = Datos de diagnóstico opcionales

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DiagnosticData
  - Nombre de la directiva de grupos: Enviar datos de diagnóstico necesarios y opcionales sobre el uso del explorador
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DiagnosticData
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DiagnosticData
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DirectInvokeEnabled
  #### Permitir a los usuarios abrir archivos con el protocolo DirectInvoke
  
  
  #### Versiones admitidas:
  - En Windows desde 78 o posterior

  #### Descripción
  Permitir a los usuarios abrir archivos con el protocolo DirectInvoke. El protocolo DirectInvoke permite a los sitios web solicitar que el explorador abra archivos de una dirección URL específica mediante un controlador de archivos específico en el equipo o dispositivo del usuario.

Si habilitas o no configuras esta Directiva, los usuarios podrán abrir archivos con el protocolo DirectInvoke.

Si deshabilita esta Directiva, los usuarios no podrán abrir archivos con el protocolo DirectInvoke. En su lugar, el archivo se guardará en el sistema de archivos.

Nota: Si deshabilita DirectInvoke, es posible que algunas características de Microsoft Office SharePoint Online no funcionen según lo esperado.

Para obtener más información acerca de DirectInvoke, consulte [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) y [https://go.microsoft.com/fwlink/?linkid=2099871](https://go.microsoft.com/fwlink/?linkid=2099871).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DirectInvokeEnabled
  - Nombre de la directiva de grupos: Permitir a los usuarios abrir archivos con el protocolo DirectInvoke
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DirectInvokeEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### Disable3DAPIs
  #### Deshabilitar el soporte de las API de gráficos 3D
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Impedir que las páginas web tengan acceso a la unidad de procesamiento gráfico (GPU). Más concretamente, las páginas web no podrán obtener acceso a la API WebGL y los complementos no podrán usar la API 3D Pepper.

Si no se configura ni se deshabilita esta directiva, podría permitir que las páginas web usen la API WebGL y complementos para usar la API 3D Pepper. Microsoft Edge, de manera predeterminada, aún pueden necesitar los argumentos de línea de comandos que se pasarán para poder usar estas API.

Si la directiva [HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled) está establecida en false, se omitirá la configuración de la directiva 'Disable3DAPIs': es el equivalente a establecer la directiva 'Disable3DAPIs' en true.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: Disable3DAPIs
  - Nombre de la directiva de grupos: Deshabilitar el soporte de las API de gráficos 3D
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: Disable3DAPIs
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: Disable3DAPIs
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DisableScreenshots
  #### Deshabilitar la captura de pantalla
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Controla si los usuarios pueden tomar capturas de pantalla de la página del explorador.

Si habilita esta opción, el usuario no podrá tomar capturas de pantalla mediante los métodos abreviados de teclado o las API de extensión.

Si deshabilita o no configura esta directiva, los usuarios podrán tomar capturas de pantalla.

Tenga en cuenta que esta directiva controla las capturas de pantalla que se toman desde el propio explorador. Aunque habilite esta directiva, los usuarios aún podrán tomar capturas de pantalla con algún método fuera del explorador (por ejemplo, mediante una función del sistema operativo u otra aplicación).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DisableScreenshots
  - Nombre de la directiva de grupos: Deshabilitar la captura de pantalla
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DisableScreenshots
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DisableScreenshots
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DiskCacheDir
  #### Establecer el directorio de memoria caché del disco
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Configura el directorio que se va a usar para almacenar archivos en caché.

Si se habilita esta directiva, Microsoft Edge usará el directorio proporcionado independientemente de si el usuario ha especificado la marca '--disk-cache-dir'. Para evitar la pérdida de datos u otros errores inesperados, no configure esta directiva en el directorio raíz de un volumen o en un directorio usado para otros fines, ya que Microsoft Edge administra su contenido.

Consulte [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) para obtener una lista de las variables que puede usar al especificar directorios y rutas.

Si no se configura esta directiva, se usará el directorio de caché predeterminado y los usuarios podrán invalidarlo con la marca de línea de comandos '--disk-cache-dir'.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DiskCacheDir
  - Nombre de la directiva de grupos: Establecer el directorio de memoria caché del disco
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DiskCacheDir
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"${user_home}/Edge_cache"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DiskCacheDir
  - Valor de ejemplo:
``` xml
<string>${user_home}/Edge_cache</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DiskCacheSize
  #### Establecer tamaño de caché de disco, en bytes
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Configura el tamaño de la memoria caché, en bytes, que se usa para almacenar archivos en el disco.

Si habilita esta directiva, Microsoft Edge usará el tamaño de la memoria caché proporcionado independientemente de si el usuario ha especificado la marca '--disk-cache-size'. El valor especificado en esta directiva no es un límite estricto, sino una sugerencia para el sistema de almacenamiento en caché; cualquier valor de menos de unos pocos megabytes será demasiado pequeño y se redondeará hasta un mínimo razonable.

Si se establece el valor de esta directiva en 0, se usará el tamaño de memoria caché predeterminado y los usuarios no podrán cambiarlo.

Si no se configura esta directiva, se usará el tamaño predeterminado, pero los usuarios podrán invalidarlo con la marca '--disk-cache-size'.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DiskCacheSize
  - Nombre de la directiva de grupos: Establecer tamaño de caché de disco, en bytes
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DiskCacheSize
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x06400000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DiskCacheSize
  - Valor de ejemplo:
``` xml
<integer>104857600</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DnsOverHttpsMode
  #### Controlar el modo de DNS mediante HTTPS
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 83 o posterior

  #### Descripción
  Controla el modo de la resolución DNS mediante HTTPS. Ten en cuenta que esta directiva solo establecerá el modo predeterminado para cada consulta. El modo se puede reemplazar para los tipos de consultas especiales como las solicitudes para resolver un nombre de host de servidor DNS mediante HTTPS.

El modo "off" deshabilitará DNS mediante HTTPS.

El modo "automatic" enviará en primer lugar consultas de DNS mediante HTTPS si un servidor DNS mediante HTTPS está disponible y es posible que recurra a enviar consultas no seguras por error.

El modo "secure" solo enviará consultas DNS sobre HTTPS y no podrá solucionar el error.

Si no configuras esta directiva, es posible que el explorador envíe solicitudes DNS sobre HTTPS a una resolución asociada a la resolución del sistema configurada por el usuario.

Asignación de opciones de directiva:

* off (off) = Deshabilitar DNS mediante HTTPS

* automatic (automatic) = Habilitar DNS mediante HTTPS con reserva no segura

* secure (secure) = Habilitar DNS mediante HTTPS sin reserva no segura

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DnsOverHttpsMode
  - Nombre de la directiva de grupos: Controlar el modo de DNS mediante HTTPS
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DnsOverHttpsMode
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"off"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DnsOverHttpsMode
  - Valor de ejemplo:
``` xml
<string>off</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DnsOverHttpsTemplates
  #### Especificar la plantilla URI de la resolución de DNS mediante HTTPS que se prefiera
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 83 o posterior

  #### Descripción
  La plantilla URI de la resolución de DNS mediante HTTPS deseada. Para especificar varias resoluciones de DNS mediante HTTPS, separa las plantillas URI correspondientes con espacios.

 Si estableces [DnsOverHttpsMode](#dnsoverhttpsmode) en "secure", esta directiva debe establecerse y no puede estar vacía.

 Si estableces [DnsOverHttpsMode](#dnsoverhttpsmode) en "automatic" y se establece esta directiva, se usarán las plantillas URI especificadas. Si no establece esta directiva, se usarán las asignaciones codificadas para intentar actualizar la resolución de DNS actual del usuario a una resolución de DoH operada por el mismo proveedor.

 Si la plantilla URI contiene una variable dns, las solicitudes a la resolución usarán GET; en caso contrario, las solicitudes usarán POST.

Se pasarán por alto las plantillas con formato incorrecto.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DnsOverHttpsTemplates
  - Nombre de la directiva de grupos: Especificar la plantilla URI de la resolución de DNS mediante HTTPS que se prefiera
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: DnsOverHttpsTemplates
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"https://dns.example.net/dns-query{?dns}"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DnsOverHttpsTemplates
  - Valor de ejemplo:
``` xml
<string>https://dns.example.net/dns-query{?dns}</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DownloadDirectory
  #### Establecer el directorio de descarga
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Configura el directorio que se va a usar al descargar archivos.

Si se habilita esta directiva, Microsoft Edge usa el directorio proporcionado, independientemente de si el usuario ha especificado uno o si ha elegido que se le pregunte la ubicación de descarga cada vez. Consulte [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) para obtener una lista de las variables que se pueden usar.

Si se deshabilita o no se configura esta directiva, se usará el directorio de descargas predeterminado y el usuario podrá cambiarlo.

Si se establece una ruta de acceso no válida, Microsoft Edge usará de forma predeterminada el directorio de descargas predeterminado del usuario.

Si la carpeta especificada por la ruta de acceso no existe, la descarga desencadenará un aviso que le preguntará al usuario dónde quiere guardar su descarga.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DownloadDirectory
  - Nombre de la directiva de grupos: Establecer el directorio de descarga
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: DownloadDirectory
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"\n      Linux-based OSes (including Mac): /home/${user_name}/Downloads\n      Windows: C:\\Users\\${user_name}\\Downloads"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DownloadDirectory
  - Valor de ejemplo:
``` xml
<string>
      Linux-based OSes (including Mac): /home/${user_name}/Downloads
      Windows: C:\Users\${user_name}\Downloads</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### DownloadRestrictions
  #### Permitir restricciones de descarga
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Configura el tipo de descargas que Microsoft Edge bloquea por completo, sin permitir que los usuarios anulen la decisión de seguridad.

Establece 'BlockDangerousDownloads' para permitir todas las descargas excepto las que tienen advertencias de SmartScreen de Microsoft Defender.

Establece 'BlockPotentiallyDangerousDownloads' para permitir todas las descargas, excepto las que tienen advertencias de SmartScreen de Microsoft Defender sobre descargas potencialmente peligrosas o no deseadas.

Establece 'BlockAllDownloads' para bloquear todas las descargas.

Si no se configura esta directiva o no se establece la opción 'DefaultDownloadSecurity', las descargas pasarán por las restricciones de seguridad habituales basadas en los resultados del análisis de SmartScreen de Microsoft Defender.

Ten en cuenta que estas restricciones se aplican a las descargas desde el contenido de la página web, así como a la opción del menú contextual 'descargar vínculo...'. Estas restricciones no se aplican a guardar o descargar la página que se muestra actualmente, ni tampoco a la opción Guardar como PDF de las opciones de impresión.

Consulta [https://go.microsoft.com/fwlink/?linkid=2094934](https://go.microsoft.com/fwlink/?linkid=2094934) para más información.

Asignación de opciones de directiva:

* DefaultDownloadSecurity (0) = No hay restricciones especiales

* BlockDangerousDownloads (1) = Bloquear descargas peligrosas

* BlockPotentiallyDangerousDownloads (2) = Bloquear descargas potencialmente peligrosas o no deseadas

* BlockAllDownloads (3) = Bloquear todas las descargas

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: DownloadRestrictions
  - Nombre de la directiva de grupos: Permitir restricciones de descarga
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: DownloadRestrictions
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: DownloadRestrictions
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### EdgeCollectionsEnabled
  #### Habilitar la característica Colecciones
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 78 o posterior

  #### Descripción
  Permite que los usuarios tengan acceso a la característica Colecciones, donde pueden recopilar, organizar, compartir y exportar contenido de forma más eficaz y con la integración de Office.

Si se habilita o no se configura esta directiva, los usuarios podrán acceder y usar la característica Colecciones en Microsoft Edge.

Si se deshabilita esta directiva, los usuarios no podrán obtener acceso ni usar Colecciones en Microsoft Edge.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: EdgeCollectionsEnabled
  - Nombre de la directiva de grupos: Habilitar la característica Colecciones
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: EdgeCollectionsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: EdgeCollectionsEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### EditFavoritesEnabled
  #### Permite a los usuarios editar los favoritos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Habilita esta directiva para permitir que los usuarios agreguen, quiten y modifiquen favoritos. Este es el comportamiento predeterminado si no se configura la directiva.

Deshabilita esta directiva para impedir que los usuarios agreguen, quiten o modifiquen favoritos. Pueden seguir usando favoritos existentes.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: EditFavoritesEnabled
  - Nombre de la directiva de grupos: Permite a los usuarios editar los favoritos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: EditFavoritesEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: EditFavoritesEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### EnableDeprecatedWebPlatformFeatures
  #### Volver a habilitar las características de la plataforma web en desuso durante un tiempo limitado
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica una lista de características de la plataforma web en desuso para volver a habilitarlas temporalmente.

Esta directiva permite volver a habilitar las características de la plataforma web en desuso durante un tiempo limitado. Las características se identifican mediante una etiqueta de cadena.

Si no se configura esta directiva, si la lista está vacía o si una característica no coincide con una de las etiquetas de cadena compatibles, todas las características de la plataforma web en desuso permanecerán deshabilitadas.

Aunque la propia directiva se admite en las plataformas anteriores, es posible que la característica que se está habilitando no esté disponible en todas las plataformas. No todas las características de la plataforma web en desuso se pueden volver a habilitar. Solo aquellas que se indican explícitamente a continuación pueden volver a habilitarse y solo durante un período de tiempo limitado, que es diferente en función de la característica. Puedes revisar la finalidad de los cambios de la característica de la plataforma web en https://bit.ly/blinkintents.

El formato habitual de la etiqueta de cadena es [DeprecatedFeatureName]_EffectiveUntil[yyyymmdd].

Asignación de opciones de directiva:

* ExampleDeprecatedFeature (ExampleDeprecatedFeature_EffectiveUntil20080902) = Habilitar API de ExampleDeprecatedFeature a través de 2008/09/02

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: EnableDeprecatedWebPlatformFeatures
  - Nombre de la directiva de grupos: Volver a habilitar las características de la plataforma web en desuso durante un tiempo limitado
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures\1 = "ExampleDeprecatedFeature_EffectiveUntil20080902"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: EnableDeprecatedWebPlatformFeatures
  - Valor de ejemplo:
``` xml
<array>
  <string>ExampleDeprecatedFeature_EffectiveUntil20080902</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### EnableDomainActionsDownload
  #### Habilitar la descarga de acciones de dominio desde Microsoft (obsoleto)
  
  >OBSOLETO: Esta directiva es obsoleta y no funciona después de la versión 84 de Microsoft Edge.
  #### Versiones admitidas:
  - En Windows y macOS desde 77, hasta 84

  #### Descripción
  Esta directiva no funciona porque se deberían evitar los estados en conflicto. Esta directiva se usaba para habilitar o deshabilitar la descarga de la lista de acciones de dominio, pero no siempre se lograba el estado deseado. El servicio de configuración y experimentación, que se ocupa de la descarga, cuenta con su propia directiva para configurar lo que se descarga del servicio. En lugar de esta, usa la directiva [ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol).

En Microsoft Edge, las acciones de dominio representan una serie de características de compatibilidad que ayudan al explorador a funcionar correctamente en la web.

Microsoft guarda una lista de acciones que se deben realizar en determinados dominios por motivos de compatibilidad. Por ejemplo, el explorador puede invalidar la cadena de agente de usuario en un sitio web si ese sitio web está roto debido a la cadena de agente de usuario en Microsoft Edge. Se supone que cada una de estas acciones es temporal mientras Microsoft intenta resolver el problema con el propietario del sitio.

Cuando se inicia el explorador, y después periódicamente, el explorador se pondrá en contacto con el servicio de configuración y experimentación de Microsoft que contiene la lista de acciones de compatibilidad que se deben realizar más reciente. Esta lista se guardará localmente después de recuperarla por primera vez, de modo que las solicitudes posteriores solo actualizarán la lista si ha cambiado la copia del servidor.

Si se habilita esta directiva, la lista de acciones del dominio seguirá descargándose desde el servicio de configuración y experimentación.

Si se deshabilita esta directiva, la lista de acciones del dominio no volverá a descargarse desde el servicio de configuración y experimentación.

Si no se configura esta directiva, las lista de acciones del dominio seguirán descargándose desde el servicio de configuración y experimentación.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: EnableDomainActionsDownload
  - Nombre de la directiva de grupos: Habilitar la descarga de acciones de dominio desde Microsoft (obsoleto)
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: EnableDomainActionsDownload
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: EnableDomainActionsDownload
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### EnableOnlineRevocationChecks
  #### Habilitar comprobaciones de CRL/OCSP en línea
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Las comprobaciones de revocación en línea no ofrecen una ventaja de seguridad significativa y están deshabilitadas de manera predeterminada.

Si se habilita esta directiva, Microsoft Edge llevará a cabo comprobaciones de errores recuperables de OCSP/CRL en línea. "Error recuperable" significa que si no se puede establecer contacto con el servidor de revocación, el certificado se considerará válido.

Si se deshabilita la directiva o no se configura, Microsoft Edge no llevará a cabo comprobaciones de revocación en línea.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: EnableOnlineRevocationChecks
  - Nombre de la directiva de grupos: Habilitar comprobaciones de CRL/OCSP en línea
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: EnableOnlineRevocationChecks
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: EnableOnlineRevocationChecks
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### EnableSha1ForLocalAnchors
  #### Permitir certificados firmados con SHA-1 al emitirlos por anclajes de veracidad local (en desuso)
  >EN DESUSO: esta directiva está en desuso. Actualmente se admite pero será obsoleta en una versión futura.
  
  #### Versiones admitidas:
  - En Windows y macOS desde 85 o posterior

  #### Descripción
  Cuando habilita esta configuración, Microsoft Edge permite conexiones protegidas por certificados firmados con SHA-1 siempre y cuando el certificado se encadene a un certificado de raíz instalado de forma local y sea válido.

Tenga en cuenta que esta directiva depende de que la pila de comprobación del certificado del sistema operativo (SO) permita firmas SHA-1. Si una actualización del sistema operativo cambia el tratamiento de los certificados SHA-1, es posible que esta directiva ya no tenga efecto.  Además, esta directiva está pensada como una solución temporal para dar más tiempo a las empresas para cambiarse de SHA-1. Esta directiva se quitará en Microsoft Edge 92, que se publicará a mediados de 2021.

Si no establece esta directiva o la configura como falsa, o si el certificado SHA-1 se encadena a una raíz de certificado de confianza pública, Microsoft Edge no admitirá certificados firmados por SHA-1.

Esta directiva solo está disponible en las instancias de Windows unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise inscritas para la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: EnableSha1ForLocalAnchors
  - Nombre de la directiva de grupos: Permitir certificados firmados con SHA-1 al emitirlos por anclajes de veracidad local (en desuso)
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: EnableSha1ForLocalAnchors
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: EnableSha1ForLocalAnchors
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### EnterpriseHardwarePlatformAPIEnabled
  #### Permitir que las extensiones administradas usen la API de la plataforma de hardware empresarial
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 78 o posterior

  #### Descripción
  Cuando esta directiva está establecida en habilitada, las extensiones instaladas por la directiva empresarial podrán usar la API de plataforma de hardware de la empresa.
Cuando esta directiva está establecida en deshabilitada o no está configurada, no se permite que las extensiones usen la API de plataforma de hardware de la empresa.
Esta directiva también se aplica a las extensiones del componente.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: EnterpriseHardwarePlatformAPIEnabled
  - Nombre de la directiva de grupos: Permitir que las extensiones administradas usen la API de la plataforma de hardware empresarial
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: EnterpriseHardwarePlatformAPIEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: EnterpriseHardwarePlatformAPIEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### EnterpriseModeSiteListManagerAllowed
  #### Permitir el acceso a la herramienta Enterprise Mode Site List Manager
  
  
  #### Versiones admitidas:
  - En Windows desde 86 o posterior

  #### Descripción
  Permite establecer si Enterprise Mode Site List Manager está disponible para los usuarios.

Si habilitas esta directiva, los usuarios podrán ver el botón de navegación de Enterprise Mode Site List Manager en la página edge://compat, navegar a la herramienta y usarla.

Si deshabilitas esta directiva o no la configuras, los usuarios no verán el botón de navegación de Enterprise Mode Site List Manager y no podrán usarla.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: EnterpriseModeSiteListManagerAllowed
  - Nombre de la directiva de grupos: Permitir el acceso a la herramienta Enterprise Mode Site List Manager
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: EnterpriseModeSiteListManagerAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  #### Deshabilitar las advertencias basadas en la extensión de tipo de archivo de descarga para los tipos de archivo especificados en dominios
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 85 o posterior

  #### Descripción
  Puedes habilitar esta directiva para crear un diccionario de extensiones de tipo de archivo con una lista correspondiente de dominios que se excluirán de las advertencias de descarga basadas en la extensión de tipo de archivo. Esto permite que los administradores de empresa bloqueen las advertencias de descarga basadas en extensiones de tipo de archivo para los archivos asociados a un dominio de la lista. Por ejemplo, si la extensión "jnlp" está asociada a "website1.com", los usuarios no verán ninguna advertencia al descargar archivos "jnlp" de "website1.com", pero verán una advertencia de descarga cuando descarguen archivos "jnlp" de "website2.com".

Los archivos con extensiones de tipo de archivo especificados para los dominios identificados por esta directiva seguirán estando sujetos a las advertencias de seguridad no basadas en extensiones de tipo de archivo, como las advertencias de descarga de contenido mixto y las advertencias de SmartScreen de Microsoft Defender.

Si deshabilitas esta Directiva o no la configuras, los tipos de archivo que desencadenan advertencias de descarga basadas en extensión mostrarán advertencias al usuario.

Si habilitas esta directiva:

* Se debe dar formato al patrón de dirección URL según [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).
* La extensión de tipo de archivo especificada debe estar en minúsculas ASCII. El separador principal  no debe incluirse al enumerar la extensión del tipo de archivo, por lo que se debe usar la lista "jnlp" en lugar de ".jnlp".

Ejemplo:

El siguiente valor de ejemplo impediría advertencias de descarga basadas en extensiones de tipo de archivo en las extensiones swf, exe y jnlp para los dominios *.contoso.com. Mostrará al usuario una advertencia de descarga basada en extensión de tipo de archivo en cualquier otro dominio para archivos exe y jnlp, pero no para archivos swf.

[
  { "file_extension": "jnlp", "domains": ["contoso.com"] },
  { "file_extension": "exe", "domains": ["contoso.com"] },
  { "file_extension": "swf", "domains": ["*"] }
]

Ten en cuenta que, aunque el ejemplo anterior muestra la supresión de advertencias de descarga basadas en la extensión de tipo de archivo para los archivos "swf" de todos los dominios, no se recomienda la supresión de avisos de este tipo para todos los dominios para cualquier extensión de tipo de archivo peligroso por motivos de seguridad. Se muestra en el ejemplo simplemente para demostrar la posibilidad de hacerlo.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Nombre de la directiva de grupos: Deshabilitar las advertencias basadas en la extensión de tipo de archivo de descarga para los tipos de archivo especificados en dominios
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\1 = {"domains": ["https://contoso.com", "contoso2.com"], "file_extension": "jnlp"}
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\2 = {"domains": ["*"], "file_extension": "swf"}

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Valor de ejemplo:
``` xml
<array>
  <string>{'domains': ['https://contoso.com', 'contoso2.com'], 'file_extension': 'jnlp'}</string>
  <string>{'domains': ['*'], 'file_extension': 'swf'}</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ExperimentationAndConfigurationServiceControl
  #### Controlar la comunicación con el servicio de configuración y experimentación
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  En Microsoft Edge, el servicio de configuración y experimentación se usa para implementar la carga de experimentación y configuración.

La carga de experimentación consiste en una lista de las características de desarrollo anticipadas que Microsoft está habilitando para pruebas y comentarios.

La carga de configuración consiste en una lista de opciones que Microsoft desea implementar en Microsoft Edge para optimizar la experiencia del usuario. Por ejemplo, la carga de configuración puede especificar la frecuencia con la que Microsoft Edge envía solicitudes al servicio de experimentación y configuración para recuperar la carga más reciente.

Además, la carga de configuración puede contener una lista de acciones que se deben realizar en determinados dominios por motivos de compatibilidad. Por ejemplo, el explorador puede invalidar la cadena de agente de usuario en un sitio web si ese sitio web está roto debido a la nueva cadena de agente de usuario en Microsoft Edge. Se supone que cada una de estas acciones es temporal mientras Microsoft intenta resolver el problema con el propietario del sitio.

Si se establece esta directiva en el modo 'FullMode', la carga completa se descarga del servicio de configuración y experimentación. Esto incluye las cargas de experimentación y configuración.

Si se establece esta directiva en 'ConfigurationsOnlyMode', solo se entrega la carga de configuración.

Si se establece esta directiva en 'RestrictedMode', la comunicación con el servicio de configuración y experimentación se detiene por completo.

Si no se configura esta directiva, en un dispositivo administrado en los canales Estable y Beta, el comportamiento es el mismo que para 'ConfigurationsOnlyMode'.

Si no se configura esta directiva, en un dispositivo no administrado, el comportamiento es el mismo que para 'FullMode'.

Asignación de opciones de directiva:

* FullMode (2) = Recuperar configuraciones y experimentos

* ConfigurationsOnlyMode (1) = Recuperar solo configuraciones

* RestrictedMode (0) = Deshabilitar la comunicación con el servicio de configuración y experimentación

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ExperimentationAndConfigurationServiceControl
  - Nombre de la directiva de grupos: Controlar la comunicación con el servicio de configuración y experimentación
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ExperimentationAndConfigurationServiceControl
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ExperimentationAndConfigurationServiceControl
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ExternalProtocolDialogShowAlwaysOpenCheckbox
  #### Mostrar una casilla "Abrir siempre" en el diálogo de protocolo externo
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 79 o posterior

  #### Descripción
  Esta directiva controla si la casilla "Permitir siempre que este sitio abra vínculos de este tipo" se muestra en las solicitudes de confirmación de inicio del protocolo externo. Esta directiva solo se aplica a vínculos https://.

Si habilitas esta directiva, cuando se muestra una solicitud de confirmación del protocolo externo, el usuario puede seleccionar "Permitir siempre" para omitir todas las solicitudes de confirmación en el futuro para el protocolo de este sitio.

Si deshabilitas esta directiva, no se mostrará la casilla "Permitir siempre". Se solicitará la confirmación del usuario cada vez que se invoque un protocolo externo.

Antes de Microsoft Edge 83, si no configuras esta directiva, la casilla "Permitir siempre" no se muestra. Se solicitará confirmación al usuario cada vez que se invoque un protocolo externo.

En Microsoft Edge 83. Si no configuras esta directiva, la visibilidad de las casillas de verificación se controla mediante el indicador "Habilitar el recuerdo de las preferencias de solicitud de inicio de protocolo", en edge://flags

A partir de Microsoft Edge 84, si no configuras esta directiva, cuando se muestra un mensaje de confirmación de protocolo externo, el usuario puede seleccionar "Permitir siempre" para omitir futuras solicitudes de confirmación para el protocolo en este sitio.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Nombre de la directiva de grupos: Mostrar una casilla "Abrir siempre" en el diálogo de protocolo externo
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### FamilySafetySettingsEnabled
  #### Permitir a los usuarios configurar Family Safety
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 83 o posterior

  #### Descripción
  Esta directiva deshabilita y oculta por completo la página de Protección infantil en Configuración. La navegación a edge://settings/familysafety también será bloqueada. La página de protección infantil indica las características disponibles para los grupos familiares y también cómo unirse a un grupo familiar. Más información sobre Protección infantil aquí: ([https://go.microsoft.com/fwlink/?linkid=2098432](https://go.microsoft.com/fwlink/?linkid=2098432)).

Si habilita esta directiva o no la configura, se mostrará la página de Protección infantil.

Si deshabilita esta directiva, no se mostrará la página de Protección infantil.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: FamilySafetySettingsEnabled
  - Nombre de la directiva de grupos: Permitir a los usuarios configurar Family Safety
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: FamilySafetySettingsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: FamilySafetySettingsEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### FavoritesBarEnabled
  #### Habilitar barra de favoritos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Habilita o deshabilita la barra de favoritos.

Si se habilita esta directiva, los usuarios verán la barra de favoritos.

Si se deshabilita esta directiva, los usuarios no verán la barra de favoritos.

Si no se configura esta directiva, el usuario puede decidir usar la barra de favoritos o no.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: FavoritesBarEnabled
  - Nombre de la directiva de grupos: Habilitar barra de favoritos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: FavoritesBarEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: FavoritesBarEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ForceBingSafeSearch
  #### Aplicar Búsqueda segura de Bing
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Asegúrate de que las consultas en Bing Web Search se realicen con Búsqueda segura establecida en el valor especificado. Los usuarios no pueden cambiar esta configuración.

Si configuras esta directiva en 'BingSafeSearchNoRestrictionsMode', Búsqueda segura en Bing Search revertirá al valor bing.com.

Si se establece esta directiva en 'BingSafeSearchModerateMode', se usará la configuración moderada en Búsqueda segura. La configuración moderada filtra los vídeos e imágenes para adultos, pero no el texto de los resultados de la búsqueda.

Si se establece esta directiva en 'BingSafeSearchStrictMode', se usará la configuración estricta en Búsqueda segura. La opción estricta filtra el texto, las imágenes y los vídeos para adultos.

Si se deshabilita esta directiva o no se configura, Búsqueda segura en Bing Search no se aplicará y los usuarios podrán establecer el valor que deseen en bing.com.

Asignación de opciones de directiva:

* BingSafeSearchNoRestrictionsMode (0) = No configurar restricciones de búsqueda en Bing

* BingSafeSearchModerateMode (1) = Configurar las restricciones de búsqueda moderadas en Bing

* BingSafeSearchStrictMode (2) = Configurar restricciones de búsqueda estrictas en Bing

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ForceBingSafeSearch
  - Nombre de la directiva de grupos: Aplicar Búsqueda segura de Bing
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ForceBingSafeSearch
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ForceBingSafeSearch
  - Valor de ejemplo:
``` xml
<integer>0</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ForceCertificatePromptsOnMultipleMatches
  #### Configura si Microsoft Edge debe seleccionar automáticamente un certificado cuando haya varias coincidencias de certificados para un sitio configurado con "AutoSelectCertificateForUrls"
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 81 o posterior

  #### Descripción
  Alterna si se pide a los usuarios que seleccionen un certificado si hay varios certificados disponibles y un sitio está configurado con[AutoSelectCertificateForUrls](#autoselectcertificateforurls). Si no se configura [AutoSelectCertificateForUrls](#autoselectcertificateforurls) para un sitio, siempre se le pedirá al usuario que seleccione un certificado.

Si estableces esta directiva en true, Microsoft Edge solicitará al usuario que seleccione un certificado para los sitios de la lista definida en[AutoSelectCertificateForUrls](#autoselectcertificateforurls) solo si hay más de un certificado.

Si estableces esta directiva en false o no la configuras, Microsoft Edge seleccionará automáticamente un certificado aunque haya varias coincidencias para un certificado. No se pedirá al usuario que seleccione un certificado para los sitios de la lista definida en [AutoSelectCertificateForUrls](#autoselectcertificateforurls).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ForceCertificatePromptsOnMultipleMatches
  - Nombre de la directiva de grupos: Configura si Microsoft Edge debe seleccionar automáticamente un certificado cuando haya varias coincidencias de certificados para un sitio configurado con "AutoSelectCertificateForUrls"
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ForceCertificatePromptsOnMultipleMatches
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ForceCertificatePromptsOnMultipleMatches
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ForceEphemeralProfiles
  #### Habilitar el uso de perfiles efímeros
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Controla si los perfiles de usuario se cambian a modo efímero. Los perfiles efímeros se crean cuando se inicia una sesión, se eliminan cuando finaliza la sesión y se asocian con el perfil original del usuario.

Si se habilita esta directiva, los perfiles se ejecutarán en modo efímero. Esto permite a los usuarios trabajar desde sus propios dispositivos sin guardar los datos de exploración en esos dispositivos. Si se habilita esta directiva como una directiva del sistema operativo (por ejemplo, mediante un GPO en Windows), se aplicará a todos los perfiles del sistema.

Si se deshabilita esta directiva o no se configura, los usuarios reciben sus perfiles normales cuando inician sesión en el explorador.

En modo efímero, los datos de perfil se guardan en el disco solo durante la sesión de usuario. Las características como el historial del explorador, las extensiones y sus datos, los datos web como las cookies y las bases de datos web no se guardarán después de cerrar el explorador. Esto no impide que un usuario descargue manualmente datos en el disco, o que guarde páginas o las imprima. Si el usuario ha habilitado la sincronización, todos los datos se conservan en sus cuentas de sincronización al igual que con los perfiles normales. Los usuarios también pueden usar la exploración de InPrivate en modo efímero a menos que se deshabilite explícitamente.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ForceEphemeralProfiles
  - Nombre de la directiva de grupos: Habilitar el uso de perfiles efímeros
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ForceEphemeralProfiles
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ForceEphemeralProfiles
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ForceGoogleSafeSearch
  #### Aplicar la Búsqueda segura de Google
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Exige que las consultas en Google Web Search se realicen con la Búsqueda segura establecida como activa e impide que los usuarios cambien esta configuración.

Si se habilita esta directiva, la Búsqueda segura en Google Search siempre estará activa.

Si se deshabilita esta directiva o no se configura, no se exigirá la Búsqueda segura en la búsqueda de Google.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ForceGoogleSafeSearch
  - Nombre de la directiva de grupos: Aplicar la Búsqueda segura de Google
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ForceGoogleSafeSearch
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ForceGoogleSafeSearch
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ForceLegacyDefaultReferrerPolicy
  #### Use una directiva de referencia predeterminada de sin origen de referencia al degradar (en desuso)
  >EN DESUSO: esta directiva está en desuso. Actualmente se admite pero será obsoleta en una versión futura.
  
  #### Versiones admitidas:
  - En Windows y macOS desde 81 o posterior

  #### Descripción
  This policy is deprecated because it's only intended to be a short-term mechanism to give enterprises more time to update their web content if and when it's found to be incompatible with the current default referrer policy. It won't work in Microsoft Edge version 88.

Microsoft Edge's default referrer policy is being strengthened from its current value of no-referrer-when-downgrade to the more secure strict-origin-when-cross-origin through a gradual rollout.

Before the rollout, this enterprise policy will have no effect. After the rollout, when this enterprise policy is enabled, Microsoft Edge's default referrer policy will be set to its old value of no-referrer-when-downgrade.

This enterprise policy is disabled by default.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ForceLegacyDefaultReferrerPolicy
  - Nombre de la directiva de grupos: Use una directiva de referencia predeterminada de sin origen de referencia al degradar (en desuso)
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ForceLegacyDefaultReferrerPolicy
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ForceLegacyDefaultReferrerPolicy
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ForceNetworkInProcess
  #### Forzar el código de red para que se ejecute en el proceso del explorador (obsoleto)
  
  >OBSOLETO: Esta directiva es obsoleta y no funciona después de la versión 83 de Microsoft Edge.
  #### Versiones admitidas:
  - En Windows desde 78, hasta 83

  #### Descripción
  Esta directiva no funciona porque solo pretendía ser un mecanismo a corto plazo para dar a las empresas más tiempo para migrar al software de terceros que no depende de la conexión de las API de redes. Se recomiendan los servidores proxy sobre los LSP y el parcheo de la API de Win32.

Esta directiva obliga a que el código de red se ejecute en el proceso del navegador.

Esta directiva está desactivada de forma predeterminada. Si está activada, los usuarios pueden tener problemas de seguridad cuando el proceso de red está en un espacio aislado.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ForceNetworkInProcess
  - Nombre de la directiva de grupos: Forzar el código de red para que se ejecute en el proceso del explorador (obsoleto)
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ForceNetworkInProcess
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ForceSync
  #### Forzar la sincronización de los datos del explorador y no mostrar la solicitud de consentimiento de sincronización
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Fuerza la sincronización de datos en Microsoft Edge. Esta directiva también impide que el usuario desactive la sincronización.

Si no configuras esta directiva, los usuarios podrán activar o desactivar la sincronización. Si habilitas esta directiva, los usuarios no podrán desactivar la sincronización.

Para que esta directiva funcione según lo previsto,
la directiva [BrowserSignin](#browsersignin) no debe estar configurada o debe establecerse como habilitada. Si [BrowserSignin](#browsersignin) se establece en deshabilitado, [ForceSync](#forcesync) no tendrá efecto.

No se debe configurar [SyncDisabled](#syncdisabled) o debe establecerse como False. Si se establece en True, [ForceSync](#forcesync) no tendrá efecto.

0 = No iniciar automáticamente la sincronización y mostrar el consentimiento de sincronización (predeterminado)
1 = Forzar la sincronización para que se active para el perfil de usuario degradado de Azure AD/Azure AD y no mostrar el aviso de consentimiento de la sincronización

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ForceSync
  - Nombre de la directiva de grupos: Forzar la sincronización de los datos del explorador y no mostrar la solicitud de consentimiento de sincronización
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ForceSync
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ForceSync
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ForceYouTubeRestrict
  #### Forzar el modo Restringido mínimo en YouTube
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Fuerza un Modo restringido mínimo en YouTube e impide que los usuarios seleccionen un modo menos restringido.

Establecer en 'Strict' para forzar el Modo restringido estricto en YouTube.

Establecer en 'Moderate'  para forzar que el usuario use solo el Modo restringido moderado y el Modo restringido estricto en YouTube. No pueden deshabilitar el modo restringido.

Establecer en 'Off'  o no configurar esta directiva para no forzar el Modo restringido en YouTube. Las directivas externas como las directivas de YouTube podrán forzar el Modo restringido.

Asignación de opciones de directiva:

* Off (0) = No forzar el modo Restringido en YouTube

* Moderate (1) = Aplicar el modo restringido moderado al menos en YouTube

* Strict (2) = Forzar modo restringido Strict para YouTube

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ForceYouTubeRestrict
  - Nombre de la directiva de grupos: Forzar el modo Restringido mínimo en YouTube
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ForceYouTubeRestrict
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ForceYouTubeRestrict
  - Valor de ejemplo:
``` xml
<integer>0</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### FullscreenAllowed
  #### Permitir modo de pantalla completa
  
  
  #### Versiones admitidas:
  - En Windows desde 77 o posterior

  #### Descripción
  Establecer la disponibilidad del modo de pantalla completa: toda la UI de Microsoft Edge está oculta y solo está visible el contenido web.

Si se habilita esta directiva o no se configura, el usuario, las aplicaciones y las extensiones con los permisos apropiados pueden pasar al modo de pantalla completa.

Si se deshabilita esta directiva, los usuarios, las aplicaciones y las extensiones no podrán pasar al modo de pantalla completa.

Cuando se deshabilita el modo de pantalla completa, no se puede abrir Microsoft Edge en modo de pantalla completa usando la línea de comandos.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: FullscreenAllowed
  - Nombre de la directiva de grupos: Permitir modo de pantalla completa
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: FullscreenAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### GloballyScopeHTTPAuthCacheEnabled
  #### Habilitar la caché de autenticación HTTP de ámbito global
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 81 o posterior

  #### Descripción
  Esta directiva configura una única memoria caché por perfil global con credenciales de autenticación de servidor HTTP.

Si se deshabilita o no se establece esta directiva, el explorador usará el comportamiento predeterminado de la autenticación entre sitios que, a partir de la versión 80, será el ámbito de las credenciales de autenticación del servidor HTTP por sitio de nivel superior. Por lo tanto, si dos sitios usan recursos del mismo dominio de autenticación, las credenciales se deberán proporcionar de forma independiente en el contexto de ambos sitios. Las credenciales de proxy en caché se reutilizarán en los sitios.

Si se habilita esta directiva, las credenciales de autenticación HTTP introducidas en el contexto de un sitio se usarán automáticamente en el contexto de otro sitio.

Si se habilita esta directiva, los sitios se abrirán para algunos tipos de ataques entre sitios y se permitirá el seguimiento de los usuarios en todos los sitios, incluso sin cookies, agregando entradas a la memoria caché de autenticación HTTP con credenciales insertadas en direcciones URL.

Esta directiva está pensada para proporcionar a las empresas en función del comportamiento heredado una oportunidad para actualizar los procedimientos de inicio de sesión y se quitarán en el futuro.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: GloballyScopeHTTPAuthCacheEnabled
  - Nombre de la directiva de grupos: Habilitar la caché de autenticación HTTP de ámbito global
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: GloballyScopeHTTPAuthCacheEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: GloballyScopeHTTPAuthCacheEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### GoToIntranetSiteForSingleWordEntryInAddressBar
  #### Fuerce la navegación directa en el sitio de intranet en lugar de buscar entradas de una única palabra en la barra de direcciones.
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 78 o posterior

  #### Descripción
  Si se habilita esta directiva, el resultado principal de sugerencia automática en la lista de sugerencias de la barra de direcciones navegará a sitios de intranet si el texto escrito en la barra de direcciones es una sola palabra sin puntuación.

La navegación predeterminada cuando se escribe una sola palabra sin puntuación llevará a cabo una navegación a un sitio de intranet que coincida con el texto escrito.

Si se habilita esta directiva, el segundo resultado de las sugerencias automáticas en la lista de sugerencias de la barra de direcciones llevará a cabo una búsqueda web tal como se ha introducido, siempre y cuando el texto sea una sola palabra sin puntuación. Se usará el proveedor de búsquedas predeterminado a menos que también esté habilitada una directiva que impida la búsqueda web.

Habilitar esta directiva tiene dos efectos:

Ya no tendrá lugar la navegación a sitios en respuesta a consultas de una sola palabra que normalmente se resolverían a un elemento del historial. En su lugar, el explorador intentará navegar a sitios internos que puede que no existan en la intranet de la organización. Esto provocará un error 404.

Los términos de búsqueda populares de una sola palabra requerirán la selección manual de sugerencias de búsqueda para llevar a cabo una búsqueda correctamente.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Nombre de la directiva de grupos: Fuerce la navegación directa en el sitio de intranet en lugar de buscar entradas de una única palabra en la barra de direcciones.
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### HSTSPolicyBypassList
  #### Configurar la lista de nombres que omitirán la comprobación de directiva de HSTS
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 79 o posterior

  #### Descripción
  Los nombres de host especificados en esta lista se excluirán de la comprobación de directiva HSTS que podría actualizar las solicitudes de "http://" a "https://". Solo se permiten nombres de host de una sola etiqueta en esta directiva. Los nombres de host deben tener un formato canónico. Cualquier IDN debe convertirse a su formato de etiqueta A y todas las letras ASCII deben estar en minúsculas. Esta directiva solo se aplica a los nombres de host específicos especificados; no se aplica a los subdominios de los nombres de la lista.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: HSTSPolicyBypassList
  - Nombre de la directiva de grupos: Configurar la lista de nombres que omitirán la comprobación de directiva de HSTS
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList\1 = "meet"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: HSTSPolicyBypassList
  - Valor de ejemplo:
``` xml
<array>
  <string>meet</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### HardwareAccelerationModeEnabled
  #### Usar aceleración de hardware cuando esté disponible
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especificar si se usa la aceleración de hardware, si está disponible. Si se habilita esta directiva o no se configura, se habilitará la aceleración de hardware, a menos que se haya bloqueado explícitamente una característica de GPU.

Si deshabilita esta directiva, se deshabilitará la aceleración de hardware.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: HardwareAccelerationModeEnabled
  - Nombre de la directiva de grupos: Usar aceleración de hardware cuando esté disponible
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: HardwareAccelerationModeEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: HardwareAccelerationModeEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### HideFirstRunExperience
  #### Ocultar la experiencia de primera ejecución y la pantalla de presentación
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 80 o posterior

  #### Descripción
  Si habilitas esta directiva, ni la experiencia de primera ejecución ni la pantalla de presentación se mostrarán a los usuarios cuando ejecuten Microsoft Edge por primera vez.

Para las opciones de configuración que se muestran en la experiencia de primera ejecución, el explorador estará establecido así de manera predeterminada:

- En la página de la nueva pestaña, el tipo de fuente se establecerá en MSN Noticias y el diseño en Inspiradores.

- El usuario seguirá iniciando sesión automáticamente en Microsoft Edge si la cuenta de Windows es del tipo Azure AD o MSA:

- La sincronización no se habilitará de forma predeterminada y se pedirá a los usuarios que elijan si quieren sincronizar al iniciar el navegador. Puedes usar la directiva [ForceSync](#forcesync) o [SyncDisabled](#syncdisabled) para configurar la sincronización y la solicitud de consentimiento de sincronización.

Si se deshabilita o no se configura esta directiva, se mostrará la experiencia de primera ejecución y la pantalla de presentación.

Nota: Las opciones de configuración específicas que se muestran al usuario en la experiencia de primera ejecución también se pueden administrar mediante otras directivas específicas. Puedes usar la directiva HideFirstRunExperience junto con estas directivas para configurar una experiencia de explorador específica en los dispositivos administrados. Algunas de estas directivas son:

-[AutoImportAtFirstRun](#autoimportatfirstrun)

-[NewTabPageLocation](#newtabpagelocation)

-[NewTabPageSetFeedType](#newtabpagesetfeedtype)

-[ForceSync](#forcesync)

-[SyncDisabled](#syncdisabled)

-[BrowserSignin](#browsersignin)

-[NonRemovableProfileEnabled](#nonremovableprofileenabled)

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: HideFirstRunExperience
  - Nombre de la directiva de grupos: Ocultar la experiencia de primera ejecución y la pantalla de presentación
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: HideFirstRunExperience
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: HideFirstRunExperience
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ImportAutofillFormData
  #### Permitir la importación de datos de Autorrellenar del formulario
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite a los usuarios importar datos de formulario de autorrellenar desde otro explorador a Microsoft Edge.

Si se habilita esta directiva, se selecciona automáticamente la opción para importar manualmente los datos de autorrellenar.

Si se deshabilita esta directiva, los datos de formulario de autorrellenar no se importarán en la primera ejecución y los usuarios no podrán importarlos manualmente.

Si no se configura esta directiva, se importarán los datos de autorrellenar en la primera ejecución y los usuarios podrán elegir si quieren importar estos datos manualmente durante las sesiones de exploración posteriores.

Puede establecerse esta directiva como una recomendación. Esto significa que Microsoft Edge importará datos de autorrellenar en la primera ejecución, pero los usuarios podrán seleccionar o borrar la opción **datos de autorrellenar** durante la importación manual.

**Nota**: Esta directiva actualmente administra la importación de Google Chrome (en Windows 7, 8 y 10 y en macOS), y Mozilla Firefox (en Windows 7, 8, y 10 y en macOS).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ImportAutofillFormData
  - Nombre de la directiva de grupos: Permitir la importación de datos de Autorrellenar del formulario
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: ImportAutofillFormData
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ImportAutofillFormData
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ImportBrowserSettings
  #### Permitir la importación de la configuración del explorador
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 78 o posterior

  #### Descripción
  Permite a los usuarios importar la configuración del motor de búsqueda de otro explorador a Microsoft Edge.

Si se habilita esta directiva, se seleccionará automáticamente la casilla de verificación **Configuración del explorador** en el cuadro de diálogo **Importar datos del explorador**.

Si se deshabilita esta directiva, la configuración del explorador no se importará en la primera ejecución y los usuarios no podrán importarla manualmente.

Si no se configura esta directiva, la configuración del explorador se importará en la primera ejecución y los usuarios podrán elegir si importar estos datos manualmente durante las sesiones de exploración posteriores.

También puede establecerse esta directiva como una recomendación. Esto significa que Microsoft Edge importa la configuración del motor de búsqueda en la primera ejecución, pero los usuarios pueden seleccionar o borrar la opción **configuración del explorador** durante la importación manual.

**Nota**: Esta directiva administra actualmente la importación de Google Chrome (en Windows 7, 8 y 10 y en macOS).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ImportBrowserSettings
  - Nombre de la directiva de grupos: Permitir la importación de la configuración del explorador
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: ImportBrowserSettings
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ImportBrowserSettings
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ImportCookies
  #### Permitir la importación de cookies
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 81 o posterior

  #### Descripción
  Permite a los usuarios importar cookies de otro explorador a Microsoft Edge.

Si se habilita esta directiva, las cookies no se importarán en la primera ejecución.

Si no se configura esta directiva, las cookies se importarán en la primera ejecución.

También puede establecerse esta directiva como una recomendación. Esto significa que Microsoft Edge importa las cookies en la primera ejecución.

**Nota**: Esta directiva administra actualmente la importación de Google Chrome (en Windows 7, 8 y 10 y en macOS).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ImportCookies
  - Nombre de la directiva de grupos: Permitir la importación de cookies
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: ImportCookies
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ImportCookies
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ImportExtensions
  #### Permitir la importación de extensiones
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 81 o posterior

  #### Descripción
  Permite a los usuarios importar extensiones desde otro explorador a Microsoft Edge.

Si se habilita esta directiva, se activará automáticamente la casilla **Pestañas abiertas** en el cuadro de diálogo **Importar datos del navegador**.

Si se deshabilita esta directiva, las extensiones no se importarán en la primera ejecución y los usuarios no podrán importarlas manualmente.

Si no se configura esta directiva, las extensiones se importarán en la primera ejecución y los usuarios podrán elegir si importarlas manualmente durante las sesiones de exploración posteriores.

También se puede establecer esta directiva como recomendación. Esto significa que Microsoft Edge importa las extensiones en la primera ejecución, pero los usuarios pueden activar o desactivar la opción **favoritos** durante la importación manual.

**Nota:** Esta directiva solo admite actualmente la importación desde Google Chrome (en Windows 7, 8 y 10 y en macOS).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ImportExtensions
  - Nombre de la directiva de grupos: Permitir la importación de extensiones
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: ImportExtensions
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ImportExtensions
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ImportFavorites
  #### Permitir la importación de favoritos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite a los usuarios importar favoritos de otro explorador en Microsoft Edge.

Si habilitas esta directiva, la casilla **favoritos** se activará automáticamente en el cuadro de diálogo **Importar datos del explorador**.

Si deshabilitas esta directiva, los favoritos no se importarán en la primera ejecución y los usuarios no podrán importarlos manualmente.

Si no configuras esta directiva, los favoritos se importan en la primera ejecución y los usuarios podrán elegir si quieren importarlos manualmente durante las sesiones de exploración posteriores.

También puedes establecer esta directiva como recomendación. Esto significa que Microsoft Edge importa los favoritos en la primera ejecución, pero los usuarios podrán seleccionar o borrar la opción **favoritos** durante la importación manual.

**Nota**: Esta directiva administra actualmente la importación desde los exploradores de Internet Explorer (en Windows 7, 8 y 10), Google Chrome (en Windows 7, 8 y 10 y en macOS), Mozilla Firefox (en Windows 7, 8 y 10 y en MacOs) y Apple Safari (en macOS).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ImportFavorites
  - Nombre de la directiva de grupos: Permitir la importación de favoritos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: ImportFavorites
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ImportFavorites
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ImportHistory
  #### Permitir la importación del historial de exploración
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite a los usuarios importar su historial de exploración desde otro explorador a Microsoft Edge.

Si se habilita esta directiva, se seleccionará automáticamente la casilla **Historial de exploración** en el cuadro de diálogo **Importar datos del explorador**.

Si se deshabilita esta directiva, los datos del historial de exploración no se importarán en la primera ejecución y los usuarios no podrán importar los datos manualmente.

Si no se configura esta directiva, los datos del historial de exploración se importarán en la primera ejecución y los usuarios podrán elegir si quieren importarlos manualmente durante las sesiones de exploración posteriores.

También puede establecerse esta directiva como recomendación. Esto significa que Microsoft Edge importa el historial de exploración en la primera ejecución, pero los usuarios podrán seleccionar o borrar la opción **historial** durante la importación manual.

**Nota**: Esta directiva administra actualmente la importación desde los exploradores de Internet Explorer (en Windows 7, 8 y 10), Google Chrome (en Windows 7, 8 y 10 y en macOS), Mozilla Firefox (en Windows 7, 8 y 10 y en MacOs) y Apple Safari (macOS).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ImportHistory
  - Nombre de la directiva de grupos: Permitir la importación del historial de exploración
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: ImportHistory
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ImportHistory
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ImportHomepage
  #### Permitir la importación de la configuración de la página principal
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite a los usuarios importar la configuración de la página principal de otro explorador a Microsoft Edge.

Si se habilita esta directiva, se seleccionará automáticamente la opción para importar manualmente la configuración de la página principal.

Si se deshabilita esta directiva, la configuración de la página principal no se importará en la primera ejecución y los usuarios no podrán importarla manualmente.

Si no se configura esta directiva, la configuración de la página principal se importará en la primera ejecución y los usuarios podrán elegir si importar estos datos manualmente durante las sesiones de exploración posteriores.

Puede establecerse esta directiva como una recomendación. Esto significa que Microsoft Edge importa la configuración de la página principal en la primera ejecución, pero los usuarios pueden seleccionar o borrar la opción **página principal** durante la importación manual.

**Nota**: Esta directiva administra actualmente la importación desde Internet Explorer (en Windows 7, 8 y 10).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ImportHomepage
  - Nombre de la directiva de grupos: Permitir la importación de la configuración de la página principal
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ImportHomepage
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ImportHomepage
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ImportOpenTabs
  #### Permitir la importación de pestañas abiertas
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 79 o posterior

  #### Descripción
  Permite a los usuarios importar pestañas abiertas y ancladas desde otro explorador a Microsoft Edge.

Si se habilita esta directiva, se activará automáticamente la casilla **Pestañas abiertas** en el cuadro de diálogo **Importar datos del navegador**.

Si se deshabilita esta directiva, las pestañas abiertas no se importarán en la primera ejecución y los usuarios no podrán importarla manualmente.

Si no se configura esta directiva, las pestañas abiertas se importarán en la primera ejecución y los usuarios podrán elegir si importarla manualmente durante las sesiones de exploración posteriores.

También se puede establecer esta directiva como recomendación. Esto significa que Microsoft Edge importa las pestañas abiertas en la primera ejecución, pero los usuarios pueden activar o desactivar la opción **Pestañas abiertas** durante la importación manual.

**Nota:** Esta directiva solo admite actualmente la importación desde Google Chrome (en Windows 7, 8 y 10 y en macOS).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ImportOpenTabs
  - Nombre de la directiva de grupos: Permitir la importación de pestañas abiertas
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: ImportOpenTabs
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ImportOpenTabs
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ImportPaymentInfo
  #### Permitir la importación de información de pago
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite a los usuarios importar la información de pago desde otro explorador a Microsoft Edge.

Si se habilita esta directiva, se activará automáticamente la casilla **información de pago** en el cuadro de diálogo **Importar datos del navegador**.

Si se deshabilita esta directiva, la información de pago no se importará en la primera ejecución y los usuarios no podrán importarla manualmente.

Si no se configura esta directiva, la información de pago se importará en la primera ejecución y los usuarios podrán elegir si importarla manualmente durante las sesiones de exploración posteriores.

También se puede establecer esta directiva como recomendación. Esto significa que Microsoft Edge importa la información de pago en la primera ejecución, pero los usuarios pueden activar o desactivar la opción **información de pago** durante la importación manual.

**Nota:** Esta directiva administra actualmente la importación de Google Chrome (en Windows 7, 8 y 10 y en macOS).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ImportPaymentInfo
  - Nombre de la directiva de grupos: Permitir la importación de información de pago
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: ImportPaymentInfo
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ImportPaymentInfo
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ImportSavedPasswords
  #### Permitir la importación de contraseñas guardadas
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite que los usuarios importen las contraseñas guardadas desde otro explorador a Microsoft Edge.

Si se habilita esta directiva, la opción de importar automáticamente las contraseñas guardadas se selecciona automáticamente.

Si se deshabilita esta directiva, las contraseñas guardadas no se importan en la primera ejecución y los usuarios no podrán importarlas de forma manual.

Si no se configura esta directiva, las contraseñas se importarán en la primera ejecución y los usuarios podrán optar por importarlas manualmente durante las sesiones de exploración posteriores.

Puede establecerse esta directiva como una recomendación. Esto significa que Microsoft Edge importa contraseñas en la primera ejecución, pero los usuarios podrán seleccionar o borrar la opción **contraseñas** durante la importación manual.

**Nota**: Esta directiva administra actualmente las importaciones desde exploradores de Internet Explorer (en Windows 7, 8 y 10), Google Chrome (en Windows 7, 8 y 10 y en macOS) y Mozilla Firefox (en Windows 7, 8, y 10 y en macOS).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ImportSavedPasswords
  - Nombre de la directiva de grupos: Permitir la importación de contraseñas guardadas
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: ImportSavedPasswords
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ImportSavedPasswords
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ImportSearchEngine
  #### Permitir la importación de la configuración del motor de búsqueda
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite a los usuarios importar la configuración del motor de búsqueda de otro explorador a Microsoft Edge.

Si se habilita esta directiva, se seleccionará automáticamente la opción para importar la configuración del motor de búsqueda.

Si se deshabilita esta directiva, la configuración de los motores de búsqueda no se importará en la primera ejecución y los usuarios no podrán importarlos manualmente.

Si no se configura esta directiva, la configuración del motor de búsqueda se importará en la primera ejecución y los usuarios podrán elegir si importar estos datos manualmente durante las sesiones de exploración posteriores.

Puede establecerse esta directiva como una recomendación. Esto significa que Microsoft Edge importa la configuración del motor de búsqueda en la primera ejecución, pero los usuarios pueden seleccionar o borrar la opción **motor de búsqueda** durante la importación manual.

**Nota**: Esta directiva administra actualmente la importación desde Internet Explorer (en Windows 7, 8 y 10).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ImportSearchEngine
  - Nombre de la directiva de grupos: Permitir la importación de la configuración del motor de búsqueda
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: ImportSearchEngine
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ImportSearchEngine
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ImportShortcuts
  #### Permitir la importación de accesos directos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 81 o posterior

  #### Descripción
  Permite a los usuarios importar accesos directos de otro explorador a Microsoft Edge.

Si se habilita esta directiva, los accesos directos no se importarán en la primera ejecución.

Si no se configura esta directiva, los accesos directos se importarán en la primera ejecución.

También puede establecerse esta directiva como una recomendación. Esto significa que Microsoft Edge importa los accesos directos en la primera ejecución.

**Nota**: Esta directiva administra actualmente la importación de Google Chrome (en Windows 7, 8 y 10 y en macOS).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ImportShortcuts
  - Nombre de la directiva de grupos: Permitir la importación de accesos directos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: ImportShortcuts
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ImportShortcuts
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### InPrivateModeAvailability
  #### Configurar la disponibilidad del modo InPrivate
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica si el usuario puede abrir páginas en modo InPrivate en Microsoft Edge.

Si no se configura esta directiva o se establece en 'Enabled', los usuarios podrán abrir páginas en modo InPrivate.

Establece esta directiva en 'Disabled' para impedir que los usuarios utilicen el modo InPrivate.

Establece esta directiva en 'Forced' para usar siempre el modo InPrivate.

Asignación de opciones de directiva:

* Enabled (0) = Modo InPrivate disponible

* Disabled (1) = Modo InPrivate deshabilitado

* Forced (2) = Modo InPrivate forzado

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: InPrivateModeAvailability
  - Nombre de la directiva de grupos: Configurar la disponibilidad del modo InPrivate
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: InPrivateModeAvailability
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: InPrivateModeAvailability
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### InsecureFormsWarningsEnabled
  #### Habilitar advertencias para formularios no seguros
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Esta directiva controla la administración de formularios no seguros (formularios enviados a través de HTTP) insertados en sitios seguros (HTTPS) en el explorador.
Si habilitas esta directiva o no la estableces, se mostrará una advertencia de página completa cuando se envíe un formulario no seguro. Además, se mostrará un globo de advertencia junto a los campos del formulario cuando tengan el foco y autorrellenar se deshabilitará para esos formularios.
Si deshabilitas esta directiva, no se mostrarán advertencias para formularios no seguros y autorrellenar funcionará con normalidad.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: InsecureFormsWarningsEnabled
  - Nombre de la directiva de grupos: Habilitar advertencias para formularios no seguros
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: InsecureFormsWarningsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: InsecureFormsWarningsEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### IntensiveWakeUpThrottlingEnabled
  #### Controle la característica IntensiveWakeUpThrottling
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 85 o posterior

  #### Descripción
  Cuando se habilita la característica IntensiveWakeUpThrottling, los temporizadores de JavaScript en las pestañas de fondo se limitan y fusionan de forma agresiva, y no se ejecutan más de una vez por minuto después de que se haya colocado en segundo plano una página durante 5 minutos o más.

Esta es una característica compatible con estándares web, pero puede romper la funcionalidad en algunos sitios web causando que algunas acciones se retrasen hasta un minuto. Sin embargo, si se habilita, se producen ahorros significativos de CPU y batería. Para más información, consulte https://bit.ly/30b1XR4.

Si habilita esta directiva, la característica se habilitará y los usuarios no podrán reemplazar esta configuración.
Si deshabilita esta directiva, la característica se deshabilitará y los usuarios no podrán reemplazar esta configuración.
Si no configura esta directiva, la característica se controlará con su propia lógica interna. Los usuarios pueden configurar manualmente esta opción.

Tenga en cuenta que la directiva se aplica por cada proceso del representación, con el valor más reciente de la configuración de directiva vigente cuando se inicia un proceso del representación. Se debe reiniciar completamente para garantizar que todas las pestañas cargadas tengan una configuración de directiva coherente. Tener procesos que se ejecuten con diferentes valores de esta directiva no supone ningún inconveniente.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: IntensiveWakeUpThrottlingEnabled
  - Nombre de la directiva de grupos: Controle la característica IntensiveWakeUpThrottling
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: IntensiveWakeUpThrottlingEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: IntensiveWakeUpThrottlingEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### InternetExplorerIntegrationEnhancedHangDetection
  #### Configure la detección de bloqueos mejorada para el modo de Internet Explorer
  
  
  #### Versiones admitidas:
  - En Windows desde 84 o posterior

  #### Descripción
  La detección de bloqueo mejorada es un enfoque más específico para detectar páginas web bloqueadas en el modo de Internet Explorer que el que usa Internet Explorer independiente. Cuando se detecta una página web bloqueada, el explorador aplicará una mitigación para evitar que el resto del navegador se bloquee.

    Esta configuración te permite configurar el uso de la detección de bloqueo mejorada en caso de que encuentre problemas incompatibles con cualquiera de los sitios web. Recomendamos deshabilitar esta directiva solo si aparecen notificaciones como "(el sitio web) no responde" en el modo de Internet Explorer, pero no en Internet Explorer independiente.

    Esta configuración funciona conjuntamente con:
    [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) está configurado en 'IEMode'
    y
    la directiva [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) en la que la lista tiene al menos una entrada.

    Si estableces esta directiva en 'Enabled' o no la configuras, los sitios web que se ejecuten en modo de Internet Explorer usarán la detección de bloqueo mejorada.

    Si estableces esta directiva en 'Disabled', la detección de bloqueo mejorada se deshabilita, y los usuarios tendrán el comportamiento de detección de bloqueo de Internet Explorer básico.

Para más información sobre el modo de Internet Explorer, consulta [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Asignación de opciones de directiva:

* Disabled (0) = Detección de bloqueo mejorada deshabilitada

* Enabled (1) = Detección de bloqueo mejorada habilitada

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: InternetExplorerIntegrationEnhancedHangDetection
  - Nombre de la directiva de grupos: Configure la detección de bloqueos mejorada para el modo de Internet Explorer
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: InternetExplorerIntegrationEnhancedHangDetection
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### InternetExplorerIntegrationLevel
  #### Configurar la integración de Internet Explorer
  
  
  #### Versiones admitidas:
  - En Windows desde 77 o posterior

  #### Descripción
  Para obtener instrucciones sobre cómo configurar la experiencia óptima para el modo de Internet Explorer, consulte [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Asignación de opciones de directiva:

* None (0) = Ninguno

* IEMode (1) = Modo de Internet Explorer

* NeedIE (2) = Internet Explorer 11

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: InternetExplorerIntegrationLevel
  - Nombre de la directiva de grupos: Configurar la integración de Internet Explorer
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: InternetExplorerIntegrationLevel
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### InternetExplorerIntegrationSiteList
  #### Configurar la lista de sitios del modo de empresa
  
  
  #### Versiones admitidas:
  - En Windows desde 78 o posterior

  #### Descripción
  Para obtener instrucciones sobre cómo configurar la experiencia óptima para el modo de Internet Explorer, consulte [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: InternetExplorerIntegrationSiteList
  - Nombre de la directiva de grupos: Configurar la lista de sitios del modo de empresa
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: InternetExplorerIntegrationSiteList
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"https://internal.contoso.com/sitelist.xml"
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### InternetExplorerIntegrationSiteRedirect
  #### Especificar cómo se comportan las exploraciones "en la página" para sitios no configurados cuando se inician desde páginas en el modo de Internet Explorer
  
  
  #### Versiones admitidas:
  - En Windows desde 81 o posterior

  #### Descripción
  La navegación "en la página" se inicia desde un vínculo, un script o un formulario de la página actual. También puede ser un redireccionamiento del lado del servidor de un intento de navegación anterior "en la página". Por el contrario, un usuario puede iniciar una navegación que no está "en la página", independiente de la página actual, utilizando los controles del explorador. Por ejemplo, usando la barra de direcciones, el botón atrás o un vínculo favorito.

Esta opción permite especificar si las navegaciones desde páginas cargadas en el modo de Internet Explorer a sitios sin configurar (no configurados en la lista de sitios del modo de empresa) cambiarán a Microsoft Edge o permanecerán en el modo de Internet Explorer.

Esta configuración funciona junto con:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) está establecido en 'IEMode'
y
la directiva [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) donde la lista tenga al menos una entrada.

Si deshabilitas o no configuras esta directiva, solo se abrirán en ese modo los sitios configurados para abrirse en el modo de Internet Explorer. Cualquier sitio que no esté configurado para abrirse en el modo de Internet Explorer se redirigirá de nuevo a Microsoft Edge.

Si estableces esta directiva en 'Default', solo los sitios configurados para abrirse en el modo de Internet Explorer se abrirán en ese modo. Los sitios no configurados para abrirse en el modo de Internet Explorer se redirigirán de nuevo a Microsoft Edge.

Si estableces esta directiva en 'AutomaticNavigationsOnly', tendrás la experiencia predeterminada, salvo que todas las navegaciones automáticas (como redirecciones 302) a sitios no configurados se mantendrán en el modo de Internet Explorer.

Si estableces esta directiva en 'AllInPageNavigations', todas las navegaciones de páginas cargadas en el modo IE a sitios no configurados se mantendrán en el modo de Internet Explorer (opción menos recomendada).

Para más información sobre el modo de Internet Explorer, consulta [https://go.microsoft.com/fwlink/?linkid=2105106](https://go.microsoft.com/fwlink/?linkid=2105106)

Asignación de opciones de directiva:

* Default (0) = Predeterminado

* AutomaticNavigationsOnly (1) = Mantener solo las exploraciones automáticas en el modo de Internet Explorer

* AllInPageNavigations (2) = Mantener todas las navegaciones en la página en el modo de Internet Explorer

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: InternetExplorerIntegrationSiteRedirect
  - Nombre de la directiva de grupos: Especificar cómo se comportan las exploraciones "en la página" para sitios no configurados cuando se inician desde páginas en el modo de Internet Explorer
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: InternetExplorerIntegrationSiteRedirect
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### InternetExplorerIntegrationTestingAllowed
  #### Permitir prueba de modo de Internet Explorer
  
  
  #### Versiones admitidas:
  - En Windows desde 86 o posterior

  #### Descripción
  Esta directiva sustituye a la directiva de marca de ie-mode-test. Permite a los usuarios abrir una pestaña en modo de IE desde la opción de menú de la interfaz de usuario.

Esta configuración funciona junto con:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) está establecido en 'IEMode'
y
la directiva [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) en la que la lista tiene al menos una entrada.

Si habilitas esta directiva, los usuarios pueden abrir la pestaña en modo IE desde la opción de la interfaz de usuario y navegar por el sitio actual a un sitio en modo IE.

Si deshabilitas esta directiva, los usuarios no podrán ver la opción de la interfaz de usuario en el menú directamente.

Si no configuras esta directiva, puedes configurar manualmente la marca de ie-mode-test.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: InternetExplorerIntegrationTestingAllowed
  - Nombre de la directiva de grupos: Permitir prueba de modo de Internet Explorer
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: InternetExplorerIntegrationTestingAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### IsolateOrigins
  #### Habilitar el aislamiento de sitios para orígenes específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especificar los orígenes para ejecutar en aislamiento, en su propio proceso.

Esta directiva también aísla los orígenes denominados subdominios; por ejemplo, si se especifica https://contoso.com/ provocará que https://foo.contoso.com/ se aísle como parte del sitio https://contoso.com/.

Si la directiva está habilitada, cada uno de los orígenes en una lista separada por comas se ejecutará en su propio proceso.

Si se deshabilita esta directiva, se deshabilitarán las características 'IsolateOrigins' y 'SitePerProcess'. Los usuarios podrán habilitar la directiva 'IsolateOrigins' manualmente, mediante los marcadores de la línea de comandos.

Si no se establece la directiva, el usuario podrá cambiar esta configuración.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: IsolateOrigins
  - Nombre de la directiva de grupos: Habilitar el aislamiento de sitios para orígenes específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: IsolateOrigins
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"https://contoso.com/,https://fabrikam.com/"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: IsolateOrigins
  - Valor de ejemplo:
``` xml
<string>https://contoso.com/,https://fabrikam.com/</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### LocalProvidersEnabled
  #### Permitir sugerencias de proveedores locales
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 83 o posterior

  #### Descripción
  Permitir sugerencias de proveedores de sugerencias en el dispositivo (proveedores locales), por ejemplo, Favoritos e Historial de exploración, en la barra de direcciones de Microsoft Edgey en la lista de sugerencias automáticas.

Si habilita esta directiva, se usarán sugerencias de proveedores locales.

Si deshabilita esta directiva, las sugerencias de proveedores locales nunca se usarán. No se mostrarán sugerencias del historial local y favoritos locales.

Si no configura esta directiva, se permitirán sugerencias de proveedores locales, pero el usuario podrá cambiar esta opción con el botón de la configuración.

Tenga en cuenta que es posible que algunas características no estén disponibles si se ha aplicado una directiva para deshabilitar esta característica. Por ejemplo, las sugerencias de Historial de exploración no estarán disponibles si habilita la directiva [SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled).

Esta directiva requiere reiniciar el explorador para finalizar su aplicación.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: LocalProvidersEnabled
  - Nombre de la directiva de grupos: Permitir sugerencias de proveedores locales
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: LocalProvidersEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: LocalProvidersEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ManagedFavorites
  #### Configurar favoritos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Configura una lista de favoritos administrados.

La directiva crea una lista de favoritos. Cada favorito contiene las claves "name" y "url", que contienen el nombre del favorito y su destino. Puede configurar una subcarpeta mediante la definición de favoritos sin una clave "url", sino con una clave "children" adicional que contiene una lista de favoritos como se define anteriormente (algunos de los cuales pueden volver a ser carpetas). Microsoft Edge modifica las URL incompletas como si se enviaran a través de la barra de direcciones, por ejemplo "microsoft.com" se convierte en "https://microsoft.com/".

Estos favoritos se colocan en una carpeta que el usuario no puede modificar (pero el usuario puede elegir ocultarlo en la barra de favoritos). De manera predeterminada, el nombre de la carpeta será "Favoritos administrados", pero puede cambiarlo si agrega a la lista de favoritos un diccionario que contenga la clave "toplevel_name" con el nombre de la carpeta deseada como valor.

Los favoritos administrados no se sincronizan con la cuenta de usuario y las extensiones no pueden modificarlos.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Diccionario

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ManagedFavorites
  - Nombre de la directiva de grupos: Configurar favoritos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ManagedFavorites
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
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


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ManagedFavorites
  - Valor de ejemplo:
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
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ManagedSearchEngines
  #### Administrar motores de búsqueda
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite configurar una lista de hasta 10 motores de búsqueda, uno de los cuales debe marcarse como el motor de búsqueda predeterminado.
No es necesario especificar la codificación. A partir de Microsoft Edge 80, los parámetros suggest_url e image_search_url son opcionales. El parámetro opcional image_search_post_params (consiste en pares de valores o nombres separados por comas) está disponible a partir de Microsoft Edge 80.

A partir de Microsoft Edge 83, se puede habilitar la detección del motor de búsqueda con el parámetro opcional allow_search_engine_discovery. Este parámetro debe ser el primer elemento de la lista. Si allow_search_engine_discovery no está especificado, la detección del motor de búsqueda se deshabilitará de manera predeterminada. A partir de Microsoft Edge 84,se puede establecer esta directiva como directiva recomendada para permitir la detección del proveedor de búsqueda. No es necesario agregar el parámetro opcional allow_search_engine_discovery.

Si se habilita esta directiva, los usuarios no podrán agregar, quitar ni cambiar ningún motor de búsqueda en la lista. Los usuarios pueden establecer su motor de búsqueda predeterminado en cualquier motor de búsqueda de la lista.

Si se deshabilita o no se configura esta directiva, los usuarios podrán modificar la lista de motores de búsqueda como prefieran.

Si se establece la directiva [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl), se omitirá esta directiva (ManagedSearchEngines). El usuario debe reiniciar el explorador para terminar de aplicar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Diccionario

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ManagedSearchEngines
  - Nombre de la directiva de grupos: Administrar motores de búsqueda
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: ManagedSearchEngines
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
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


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ManagedSearchEngines
  - Valor de ejemplo:
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
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### MaxConnectionsPerProxy
  #### Número máximo de conexiones simultáneas al servidor proxy
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica el número máximo de conexiones simultáneas al servidor proxy.

Algunos servidores proxy no pueden controlar un gran número de conexiones simultáneas por cliente; esto se puede solucionar estableciendo esta directiva en un valor menor.

El valor de esta directiva debe ser inferior a 100 y superior a 6. El valor predeterminado es 32.

Se sabe que algunas aplicaciones web consumen muchas conexiones con GET que no responden, reducir el número máximo de conexiones por debajo de 32 puede provocar que las redes del explorador no respondan si hay demasiadas aplicaciones web de este tipo abiertas.

Si no se configura esta directiva, se usa el valor predeterminado (32).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: MaxConnectionsPerProxy
  - Nombre de la directiva de grupos: Número máximo de conexiones simultáneas al servidor proxy
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: MaxConnectionsPerProxy
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000020
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: MaxConnectionsPerProxy
  - Valor de ejemplo:
``` xml
<integer>32</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### MediaRouterCastAllowAllIPs
  #### Permitir que Google Cast se conecte con dispositivos de Cast en todas las direcciones IP
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Habilite esta directiva para permitir que Google Cast se conecte a dispositivos de Cast en todas las direcciones IP, no solo direcciones privadas de RFC1918/RFC4193.

Deshabilite esta directiva para restringir Google Cast a los dispositivos de Cast en direcciones privadas de RFC1918/RFC4193.

Si no se configura esta directiva, Google Cast se conectará a dispositivos de Cast solo en direcciones privadas de RFC1918/RFC4193, a menos que se habilite la característica CastAllowAllIPs.

Si la directiva [EnableMediaRouter](#enablemediarouter) está deshabilitada, esta directiva no tiene ningún efecto.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: MediaRouterCastAllowAllIPs
  - Nombre de la directiva de grupos: Permitir que Google Cast se conecte con dispositivos de Cast en todas las direcciones IP
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: MediaRouterCastAllowAllIPs
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: MediaRouterCastAllowAllIPs
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### MetricsReportingEnabled
  #### Habilitar el uso y los informes de datos relacionados con el bloqueo (en desuso)
  >EN DESUSO: esta directiva está en desuso. Actualmente se admite pero será obsoleta en una versión futura.
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Esta directiva está en desuso. Se admite actualmente, pero quedará obsoleta en Microsoft Edge 89 y se reemplaza por la nueva:   [DiagnosticData](#diagnosticdata)para Windows 7, Windows 8 y macOS. Esta directiva se reemplaza por Permitir telemetría en Win 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

      Esta directiva permite informar a Microsoft sobre el uso y los datos relacionados con bloqueos de Microsoft Edge.

     Habilite esta directiva para enviar informes de uso y datos relacionados con bloqueos a Microsoft. Deshabilite esta directiva para no enviar los datos a Microsoft. En ambos casos, los usuarios no pueden cambiar ni reemplazar la configuración.

     En Windows 10, si no configura esta directiva, Microsoft Edge usará de forma predeterminada la configuración de datos de diagnóstico de Windows. Si habilita esta directiva, Microsoft Edge solo enviará datos de uso si la configuración de Datos de diagnóstico de Windows está establecida en Mejorado o Completo. Si deshabilita esta directiva, Microsoft Edge no enviará datos de uso. Los datos relacionados con bloqueos se envían en función de la configuración de Datos de diagnóstico de Windows. Más información sobre la configuración de Datos de diagnóstico de Windows en [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

     En Windows 7, Windows 8 y macOS, esta directiva controla el envío de datos relacionados con el uso y el bloqueo. Si no configura esta directiva, Microsoft Edge usará de forma predeterminada la preferencia del usuario.

      Para habilitar esta directiva, [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) debe establecerse en Habilitado. Si [MetricsReportingEnabled](#metricsreportingenabled) o [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) no se configuran o se deshabilitan, estos datos no se enviarán a Microsoft.

Esta directiva solo está disponible en instancias de Windows que estén unidas a un dominio de Microsoft Active Directory, instancias de Windows 10 Pro o Enterprise que estén inscritas para la administración de dispositivos, o bien instancias de macOS que sean administradas mediante MDM o estén unidas a un dominio mediante MCX.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: MetricsReportingEnabled
  - Nombre de la directiva de grupos: Habilitar el uso y los informes de datos relacionados con el bloqueo (en desuso)
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: MetricsReportingEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: MetricsReportingEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### NativeWindowOcclusionEnabled
  #### Habilitar la oclusión de ventana nativa
  
  
  #### Versiones admitidas:
  - En Windows desde 84 o posterior

  #### Descripción
  Habilita la oclusión de ventanas nativas en Microsoft Edge.

Si se habilita esta opción Microsoft Edge detectará si hay alguna ventana cubierta por otras ventanas y suspenderá el trabajo de pintado de píxeles.

Si se deshabilita esta opción, Microsoft Edge no detectará si hay alguna ventana cubierta por otras ventanas.

Si no se configura esta directiva, se habilitará la detección de ocultamiento de ventanas.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: NativeWindowOcclusionEnabled
  - Nombre de la directiva de grupos: Habilitar la oclusión de ventana nativa
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: NativeWindowOcclusionEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### NavigationDelayForInitialSiteListDownloadTimeout
  #### Establece un tiempo de espera de retardo en la navegación por la etiqueta de la Lista de sitios de Modo de empresa
  
  
  #### Versiones admitidas:
  - En Windows desde 84 o posterior

  #### Descripción
  Permite establecer un tiempo de espera en segundos para pestañas de Microsoft Edge que esperan para navegar hasta que el explorador descargue la Lista de sitios de Modo de Empresa inicial.

Esta configuración funciona conjuntamente con lo siguiente:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) está establecido en 'IEMode'
y
la directiva [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) en la que la lista tiene al menos una entrada
y
[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload) está establecido como "Todas las exploraciones aptas" (1).

Las pestañas no esperarán más de este tiempo de espera a que se descargue la Lista de sitios de Modo de Empresa. Si el explorador no ha terminado de descargar la Lista de sitios de Modo de Empresa cuando se agote el tiempo de espera, las pestañas de Microsoft Edge continuarán navegando de todos modos. El valor del tiempo de espera no debe ser mayor que 20 segundos y no puede ser menor que 1 segundo.

Si se define el tiempo de espera en esta directiva en un valor mayor que el predeterminado de 2 segundos, se muestra una barra de información al usuario después de 2 segundos. La barra de información contiene un botón que permite al usuario elegir dejar de esperar a que se complete la descarga de la Lista de sitios de Modo de Empresa.

Si no se configura esta directiva, se usa el tiempo de espera predeterminado de 2 segundos. Este valor predeterminado está sujeto a cambios en el futuro.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: NavigationDelayForInitialSiteListDownloadTimeout
  - Nombre de la directiva de grupos: Establece un tiempo de espera de retardo en la navegación por la etiqueta de la Lista de sitios de Modo de empresa
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: NavigationDelayForInitialSiteListDownloadTimeout
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x0000000a
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### NetworkPredictionOptions
  #### Habilitar la predicción de red
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Habilita la predicción de red e impide que los usuarios cambien esta configuración.

Esto controla la captura previa de DNS, la conexión previa de TCP y SSL, y la representación previa de páginas web.

Si no se configura esta directiva, la predicción de red estará habilitada pero el usuario podrá cambiarla.

Asignación de opciones de directiva:

* NetworkPredictionAlways (0) = Predecir las acciones de la red en cualquier conexión de red

* NetworkPredictionWifiOnly (1) = No admitido, si se usa este valor, se tratará como si se hubiera definido "Predecir las acciones de red en cualquier conexión de red" (0).

* NetworkPredictionNever (2) = No predecir las acciones de la red en ninguna conexión de red

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: NetworkPredictionOptions
  - Nombre de la directiva de grupos: Habilitar la predicción de red
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: NetworkPredictionOptions
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: NetworkPredictionOptions
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### NonRemovableProfileEnabled
  #### Configurar si un usuario siempre tiene un perfil predeterminado con sesión iniciada automáticamente con su cuenta profesional o educativa
  
  
  #### Versiones admitidas:
  - En Windows desde 78 o posterior

  #### Descripción
  Esta directiva determina si un usuario puede quitar el perfil de Microsoft Edge que inició sesión automáticamente con una cuenta profesional o educativa de un usuario.

Si habilita esta directiva, se creará un perfil no extraíble con la cuenta profesional o educativa del usuario en Windows. No se puede cerrar la sesión de este perfil ni quitarlo.

Si deshabilita o no configura esta directiva, el usuario puede cerrar la sesión o quitar el perfil que ha iniciado sesión automáticamente con la cuenta profesional o educativa en Windows.

Si quiere configurar el inicio de sesión del explorador, use la directiva [BrowserSignin](#browsersignin).

Esta directiva solo está disponible en las instancias de Windows que estén unidas a un dominio de Microsoft Active Directory e instancias de Windows 10 Pro o Enterprise que estén inscritas para la administración de dispositivos.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: NonRemovableProfileEnabled
  - Nombre de la directiva de grupos: Configurar si un usuario siempre tiene un perfil predeterminado con sesión iniciada automáticamente con su cuenta profesional o educativa
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: NonRemovableProfileEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### OverrideSecurityRestrictionsOnInsecureOrigin
  #### Controlar dónde se aplican restricciones de seguridad en los orígenes no seguros
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica una lista de orígenes (URL) o patrones de nombre de host (como "*.contoso.com") en los que no se aplican restricciones de seguridad en los orígenes no seguros.

Esta directiva permite especificar orígenes permitidos para las aplicaciones heredadas que no pueden implementar TLS o configurar un servidor de almacenamiento provisional para el desarrollo web interno de modo que los desarrolladores puedan probar las características que requieren contextos seguros sin tener que implementar TLS en el servidor de almacenamiento provisional. Esta directiva también impide que el origen esté etiquetado como "No seguro" en el multicuadro.

Establecer una lista de direcciones URL en esta directiva tiene el mismo efecto que establecer la marca de línea de comandos '--unsafely-treat-insecure-origin-as-secure' en una lista separada por comas de las mismas direcciones URL. Si se habilita esta directiva, se invalidará la marca de línea de comandos.

Para obtener más información acerca de los contextos de seguridad, consulta https://www.w3.org/TR/secure-contexts/.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: OverrideSecurityRestrictionsOnInsecureOrigin
  - Nombre de la directiva de grupos: Controlar dónde se aplican restricciones de seguridad en los orígenes no seguros
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\1 = "http://testserver.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\2 = "*.contoso.com"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: OverrideSecurityRestrictionsOnInsecureOrigin
  - Valor de ejemplo:
``` xml
<array>
  <string>http://testserver.contoso.com/</string>
  <string>*.contoso.com</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PaymentMethodQueryEnabled
  #### Permitir que los sitios web consulten los métodos de pago disponibles
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 80 o posterior

  #### Descripción
  Te permite establecer si los sitios web pueden comprobar si el usuario tiene métodos de pago guardados

Si deshabilitas esta directiva, se informará a los sitios web que usan la API PaymentRequest.canMakePayment o PaymentRequest.hasEnrolledInstrument de que no hay métodos de pago disponibles.

Si habilitas esta directiva o no la estableces, los sitios web podrán comprobar si el usuario tiene métodos de pago guardados.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PaymentMethodQueryEnabled
  - Nombre de la directiva de grupos: Permitir que los sitios web consulten los métodos de pago disponibles
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: PaymentMethodQueryEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PaymentMethodQueryEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PersonalizationReportingEnabled
  #### Permitir la personalización de anuncios, búsquedas y noticias mediante el envío del historial de exploración a Microsoft
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 80 o posterior

  #### Descripción
  Esta directiva impide que Microsoft recopile el historial de exploración de Microsoft Edge de un usuario que se usará para personalizar la publicidad, la búsqueda, las noticias y otros servicios Microsoft.

Esta opción solo está disponible para los usuarios que tengan una cuenta de Microsoft. Esta opción no está disponible para cuentas de menores o cuentas de empresa.

Si se deshabilita esta directiva, los usuarios no podrán cambiar ni reemplazar la configuración. Si se habilita o no se configura esta directiva, Microsoft Edge usará de forma predeterminada la preferencia del usuario.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PersonalizationReportingEnabled
  - Nombre de la directiva de grupos: Permitir la personalización de anuncios, búsquedas y noticias mediante el envío del historial de exploración a Microsoft
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: PersonalizationReportingEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PersonalizationReportingEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PinningWizardAllowed
  #### Permitir el asistente de Anclar a la barra de tareas
  
  
  #### Versiones admitidas:
  - En Windows desde 80 o posterior

  #### Descripción
  Microsoft Edge usa el asistente de Anclar a la barra de tareas para ayudar a los usuarios a anclar sitios sugeridos a la barra de tareas. La característica Anclar a la barra de tareas está habilitada de forma predeterminada y el usuario puede acceder a ella a través del menú Configuración y más.


Si se habilita esta directiva o no se configura, los usuarios podrán llamar al asistente Anclar a la barra de tareas desde el menú Configuración y más. También se puede llamar al asistente a través de un inicio de protocolo.

Si deshabilita esta directiva, el asistente de Anclar a la barra de tareas estará deshabilitado en el menú y no se podrá llamar a través de un inicio de protocolo.

La configuración del usuario para habilitar o deshabilitar el asistente de Anclar a la barra de tareas no está disponible.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PinningWizardAllowed
  - Nombre de la directiva de grupos: Permitir el asistente de Anclar a la barra de tareas
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: PinningWizardAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ProactiveAuthEnabled
  #### Habilitar autenticación proactiva
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite configurar si se debe activar la autenticación proactiva.

Si se habilita esta directiva, Microsoft Edge intentará autenticar proactivamente el usuario que inició sesión con los servicios Microsoft. A intervalos regulares, Microsoft Edge realiza comprobaciones con un servicio en línea para obtener un manifiesto actualizado que contenga la configuración que rige cómo hacerlo.

Si se deshabilita esta directiva, Microsoft Edge no intentará autenticar proactivamente el usuario que ha iniciado sesión con los servicios Microsoft. Microsoft Edge ya no realizará comprobaciones con un servicio en línea para obtener un manifiesto actualizado que contenga la configuración para hacerlo.

Si no se configura esta directiva, se activará la autenticación proactiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ProactiveAuthEnabled
  - Nombre de la directiva de grupos: Habilitar autenticación proactiva
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ProactiveAuthEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ProactiveAuthEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PromotionalTabsEnabled
  #### Habilitar el contenido promocional en toda la pestaña
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Controle la presentación de contenido educativo o promocional de pestaña completa. Esta configuración controla la presentación de las páginas principales que ayudan a los usuarios a iniciar sesión en Microsoft Edge, elegir su explorador predeterminado o descubrir características del producto.

Si se habilita esta directiva (si se establece en true) o si no se configura, Microsoft Edge podrá mostrar contenido de pestaña completa a los usuarios para proporcionar información acerca del producto.

Si se deshabilita esta directiva (si se establece en false), Microsoft Edge no podrá mostrar contenido de pestaña completa a los usuarios.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PromotionalTabsEnabled
  - Nombre de la directiva de grupos: Habilitar el contenido promocional en toda la pestaña
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: PromotionalTabsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PromotionalTabsEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### PromptForDownloadLocation
  #### Preguntar dónde guardar los archivos descargados
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Establecer si se debe preguntar dónde guardar un archivo antes de descargarlo.

Si se habilita esta directiva, se le preguntará al usuario dónde quiere guardar cada archivo antes de descargarlo; si no se configura, los archivos se guardan automáticamente en la ubicación predeterminada, sin preguntarle al usuario.

Si no se configura esta directiva, el usuario podrá cambiar esta configuración.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: PromptForDownloadLocation
  - Nombre de la directiva de grupos: Preguntar dónde guardar los archivos descargados
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: PromptForDownloadLocation
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: PromptForDownloadLocation
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### QuicAllowed
  #### Permitir protocolo QUIC
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite el uso del protocolo QUIC en Microsoft Edge.

Si se habilita esta directiva o no se configura, se permitirá el protocolo QUIC.

Si se deshabilita esta directiva, se bloqueará el protocolo QUIC.

QUIC es un protocolo de red de capa de transporte que puede mejorar el rendimiento de las aplicaciones web que usan actualmente TCP.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: QuicAllowed
  - Nombre de la directiva de grupos: Permitir protocolo QUIC
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: QuicAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: QuicAllowed
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### RelaunchNotification
  #### Notificar al usuario que se recomienda o se requiere reiniciar el explorador para las actualizaciones pendientes
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Notifica a los usuarios que deben reiniciar Microsoft Edge para aplicar una actualización pendiente.

Si no se configura esta directiva, Microsoft Edge agrega un icono de reciclaje en el extremo derecho de la barra de menús superior para pedir a los usuarios que reinicien el explorador y aplicar la actualización.

Si se habilita esta directiva y se establece con el valor 'Recommended', una advertencia periódica indicará a los usuarios que se recomienda reiniciar el explorador. Los usuarios pueden descartar esta advertencia y aplazar el reinicio.

Si se establece la directiva en 'Required', una advertencia periódica indicará a los usuarios que el explorador se reiniciará automáticamente tras un período de notificación. El período predeterminado es de siete días. Se puede configurar este período con la directiva [RelaunchNotificationPeriod](#relaunchnotificationperiod).

La sesión del usuario se restaurará cuando se reinicie el explorador.

Asignación de opciones de directiva:

* Recommended (1) = Recomendado: mostrar un aviso periódico al usuario que indique que se recomienda reiniciar

* Required (2) = Requerido: mostrar un aviso periódico al usuario para indicar que es necesario reiniciar

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: RelaunchNotification
  - Nombre de la directiva de grupos: Notificar al usuario que se recomienda o se requiere reiniciar el explorador para las actualizaciones pendientes
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: RelaunchNotification
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: RelaunchNotification
  - Valor de ejemplo:
``` xml
<integer>1</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### RelaunchNotificationPeriod
  #### Establecer el período de tiempo para las notificaciones de actualización
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite establecer el período de tiempo, en milisegundos, en el que se notifica a los usuarios que el Microsoft Edge debe volver a iniciarse para aplicar una actualización pendiente.

Durante este período de tiempo, se le informará repetidamente al usuario sobre la necesidad de una actualización. En Microsoft Edge el menú de la aplicación cambia para indicar que se necesita un reinicio cuando se pasa un tercio del período de notificación. Esta notificación cambia de color tan pronto como se transfieren los dos tercios del período de notificación y una vez que ha transcurrido el período de notificación completo. Las notificaciones adicionales habilitadas por la directiva [RelaunchNotification](#relaunchnotification) siguen la misma programación.

Si no se establece, se usa el período predeterminado de 604,8 millones de milisegundos (una semana).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: RelaunchNotificationPeriod
  - Nombre de la directiva de grupos: Establecer el período de tiempo para las notificaciones de actualización
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: RelaunchNotificationPeriod
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x240c8400
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: RelaunchNotificationPeriod
  - Valor de ejemplo:
``` xml
<integer>604800000</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### RendererCodeIntegrityEnabled
  #### Habilitar la integridad del código del procesador
  
  
  #### Versiones admitidas:
  - En Windows desde 78 o posterior

  #### Descripción
  Si se habilita o se deja esta directiva sin establecer, se habilita la integridad del código de representador. Esta directiva solo se debe deshabilitar si se encuentran problemas de compatibilidad con el software de terceros que deben ejecutarse dentro de los procesos del representador de Microsoft Edge.

La deshabilitación de esta directiva tiene un efecto perjudicial en la estabilidad y la seguridad de Microsoft Edge porque se permitirá que el código desconocido y potencialmente hostil se cargue dentro de los procesadores del representador de Microsoft Edge.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: RendererCodeIntegrityEnabled
  - Nombre de la directiva de grupos: Habilitar la integridad del código del procesador
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: RendererCodeIntegrityEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### RequireOnlineRevocationChecksForLocalAnchors
  #### Especificar si las comprobaciones CRL/OCSP en línea son obligatorias para los delimitadores locales de confianza
  
  
  #### Versiones admitidas:
  - En Windows desde 77 o posterior

  #### Descripción
  Controle si las comprobaciones de revocación en línea (comprobaciones OCSP/CRL) son obligatorias. Si Microsoft Edge no puede obtener información de estado de revocación, estos certificados se tratan como revocados ("error no recuperable").

Si se habilita esta directiva, Microsoft Edge siempre realizará la comprobación de revocación de los certificados de servidor que se validan correctamente y están firmados por certificados de entidad de certificación instalados localmente.

Si no se configura o si se deshabilita esta directiva, Microsoft Edge usará la configuración de comprobación de revocación en línea existente.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: RequireOnlineRevocationChecksForLocalAnchors
  - Nombre de la directiva de grupos: Especificar si las comprobaciones CRL/OCSP en línea son obligatorias para los delimitadores locales de confianza
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: RequireOnlineRevocationChecksForLocalAnchors
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ResolveNavigationErrorsUseWebService
  #### Habilitar la resolución de errores de navegación mediante un servicio web
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permitir que Microsoft Edge emita una conexión sin datos a un servicio web para sondear las redes para la conectividad en casos como la Wi-Fi de hoteles y aeropuertos.

Si se habilita esta directiva, se usará un servicio web para las pruebas de conectividad de red.

Si se deshabilita esta directiva, Microsoft Edge usará las API nativas para intentar resolver los problemas de navegación y conectividad de red.

**Nota**: Excepto en Windows 8 y versiones posteriores de Windows, Microsoft Edge *siempre* usa API nativas para resolver problemas de conectividad.

Si no se configura esta directiva, Microsoft Edge respeta la preferencia del usuario que está establecida en Servicios en edge://settings/privacy.
En concreto, hay un botón de alternancia, **Usar un servicio web para ayudar a resolver errores de navegación**, que el usuario puede activar o desactivar. Tenga en cuenta que si está habilitada esta directiva (ResolveNavigationErrorsUseWebService), la configuración **Usar un servicio web para ayudar a resolver errores de navegación** estará activada, pero el usuario no podrá cambiar la configuración mediante el botón de alternancia. Si se deshabilita esta directiva, la configuración **Usar un servicio web para ayudar a resolver errores de navegación** estará desactivada y el usuario no podrá cambiar la configuración mediante el botón de alternancia.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ResolveNavigationErrorsUseWebService
  - Nombre de la directiva de grupos: Habilitar la resolución de errores de navegación mediante un servicio web
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: ResolveNavigationErrorsUseWebService
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ResolveNavigationErrorsUseWebService
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### RestrictSigninToPattern
  #### Restringir las cuentas que pueden usarse como cuentas principales de Microsoft Edge
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Determina qué cuentas se pueden establecer como cuentas primarias de explorador en Microsoft Edge (la cuenta que se elige durante el flujo de participación en la sincronización).

Si un usuario intenta configurar una cuenta principal del explorador con un nombre de usuario que no coincide con este patrón, se bloqueará y aparecerá el mensaje de error correspondiente. Puedes configurar esta directiva para que coincida con varias cuentas mediante una expresión regular de estilo Perl para el patrón. Ten en cuenta que las coincidencias de patrón distinguen mayúsculas de minúsculas. Para más información sobre las reglas de expresión regular que se usan, consulta https://go.microsoft.com/fwlink/p/?linkid=2133903.

Si no se configura esta directiva o se deja en blanco, los usuarios podrán establecer cualquiera de las cuentas como cuenta principal del explorador en Microsoft Edge.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: RestrictSigninToPattern
  - Nombre de la directiva de grupos: Restringir las cuentas que pueden usarse como cuentas principales de Microsoft Edge
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: RestrictSigninToPattern
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
".*@contoso.com"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: RestrictSigninToPattern
  - Valor de ejemplo:
``` xml
<string>.*@contoso.com</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### RoamingProfileLocation
  #### Establecer el directorio de perfiles de itinerancia
  
  
  #### Versiones admitidas:
  - En Windows desde 85 o posterior

  #### Descripción
  Configura el directorio que se va a usar para almacenar la copia de perfiles de itinerancia.

Si habilitas esta directiva, Microsoft Edge usará el directorio proporcionado para almacenar una copia de los perfiles de itinerancia, siempre y cuando también se haya habilitado la directiva [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) Si deshabilitas la directiva [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) o no la configuras, no se usará el valor almacenado en esta directiva.

Consulta [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) para ver una lista de las variables que puedes usar.

Si no configuras esta directiva, se usará la ruta de acceso del perfil de itinerancia predeterminada.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: RoamingProfileLocation
  - Nombre de la directiva de grupos: Establecer el directorio de perfiles de itinerancia
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: RoamingProfileLocation
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"${roaming_app_data}\\edge-profile"
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### RoamingProfileSupportEnabled
  #### Habilitar el uso de copias de itinerancia para los datos de perfil de Microsoft Edge
  
  
  #### Versiones admitidas:
  - En Windows desde 85 o posterior

  #### Descripción
  Habilita esta directiva para usar perfiles de itinerancia en Windows. La configuración almacenada en los perfiles de Microsoft Edge (favoritos y preferencias) también se guarda en un archivo que se almacena en la carpeta de Perfil de usuario de itinerancia (o la ubicación especificada por el administrador a través de la directiva [RoamingProfileLocation](#roamingprofilelocation)).

Si se deshabilita o no se configura esta directiva, se usan los perfiles locales habituales.

La directiva [SyncDisabled](#syncdisabled) deshabilita toda la sincronización de datos, lo que invalida la directiva.

Consulta https://docs.microsoft.com/windows-server/storage/folder-redirection/deploy-roaming-user-profiles para más información sobre el uso de perfiles de usuario de itinerancia.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: RoamingProfileSupportEnabled
  - Nombre de la directiva de grupos: Habilitar el uso de copias de itinerancia para los datos de perfil de Microsoft Edge
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: RoamingProfileSupportEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### RunAllFlashInAllowMode
  #### Extender la configuración de contenidos de Adobe Flash a todos los contenido
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Si se habilita esta directiva, se ejecutarán todos los contenidos de Adobe Flash incorporados en sitios web que están establecidos para permitir Adobe Flash en la configuración de contenido (ya sea por parte del usuario o de la directiva de empresa). Esto incluye contenidos de otros orígenes o contenidos pequeños.

Para controlar los sitios web que pueden ejecutar Adobe Flash, consulta las especificaciones de las directivas [DefaultPluginsSetting](#defaultpluginssetting), [PluginsAllowedForUrls](#pluginsallowedforurls) y [PluginsBlockedForUrls](#pluginsblockedforurls).

Si se deshabilita esta directiva o no se configura, los contenidos de Adobe Flash de otros orígenes (de sitios que no están especificados en las directivas de las tres políticas mencionadas antes) o los contenidos pequeños podrían estar bloqueados.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: RunAllFlashInAllowMode
  - Nombre de la directiva de grupos: Extender la configuración de contenidos de Adobe Flash a todos los contenido
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: RunAllFlashInAllowMode
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: RunAllFlashInAllowMode
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SSLErrorOverrideAllowed
  #### Permitir que los usuarios continúen desde la página de advertencia de HTTPS
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Microsoft Edge muestra una página de advertencia cuando los usuarios visitan sitios que presentan errores SSL.

Si se habilita o no se configura (valor predeterminado) esta directiva, los usuarios podrán hacer clic en estas páginas de advertencia.

Si se deshabilita esta directiva, los usuarios no podrán hacer clic en ninguna página de advertencia.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SSLErrorOverrideAllowed
  - Nombre de la directiva de grupos: Permitir que los usuarios continúen desde la página de advertencia de HTTPS
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: SSLErrorOverrideAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SSLErrorOverrideAllowed
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SSLVersionMin
  #### Versión mínima de TLS habilitada
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Sets the minimum supported version of TLS. If you don't configure this policy, Microsoft Edge uses a default minimum version, TLS 1.0.

If you enable this policy, Microsoft Edge won't use any version of SSL/TLS lower than the specified version. Any unrecognized value is ignored.

Asignación de opciones de directiva:

* TLSv1 (tls1) = TLS 1.0

* TLSv1.1 (tls1.1) = TLS 1.1

* TLSv1.2 (tls1.2) = TLS 1.2

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SSLVersionMin
  - Nombre de la directiva de grupos: Versión mínima de TLS habilitada
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: SSLVersionMin
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"tls1"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SSLVersionMin
  - Valor de ejemplo:
``` xml
<string>tls1</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SaveCookiesOnExit
  #### Guardar cookies cuando se cierre Microsoft Edge
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Cuando esta directiva está habilitada, el conjunto de cookies no se eliminará cuando se cierre el explorador. Esta directiva solo surte efecto cuando:
- El conmutador 'Cookies y otros datos del sitio' está configurado en Configuración/Privacidad y servicios/Borrar datos de navegación al cerrar o
- La directiva [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) está habilitada o
- La directiva [DefaultCookiesSetting](#defaultcookiessetting) está configurada en 'Guardar cookies durante la sesión'.

Puedes definir una lista de sitios, basada en modelos de URL, que conservará tus cookies en las sesiones.

Nota: los usuarios aún pueden editar la lista de sitios de cookies para agregar o eliminar URL. Sin embargo, no pueden eliminar las URL que haya agregado un administrador.

Si habilitas esta directiva, la lista de cookies no se borrará cuando se cierre el navegador.

Si deshabilitas o no configuras esta directiva, se utiliza la configuración personal del usuario.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SaveCookiesOnExit
  - Nombre de la directiva de grupos: Guardar cookies cuando se cierre Microsoft Edge
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SaveCookiesOnExit
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SavingBrowserHistoryDisabled
  #### Deshabilitar guardar el historial del explorador
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Deshabilita guardar el historial del explorador e impide que los usuarios cambien esta configuración.

Si se habilita esta directiva, el historial de exploración no se guardará. Esto también deshabilita la sincronización de pestañas.

Si se deshabilita esta directiva o no se configura, se guardará el historial de exploración.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SavingBrowserHistoryDisabled
  - Nombre de la directiva de grupos: Deshabilitar guardar el historial del explorador
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: SavingBrowserHistoryDisabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SavingBrowserHistoryDisabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ScreenCaptureAllowed
  #### Permitir o denegar captura de pantalla
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 83 o posterior

  #### Descripción
  Si habilita esta directiva, o no la configura, una página web puede utilizar las APIs de compartición de pantalla (por ejemplo, getDisplayMedia() o la API de extensión de Desktop Capture) para una captura de pantalla.
Si deshabilita esta directiva, las llamadas a las API de pantalla compartida fallarán. Por ejemplo, si utiliza una reunión en línea basada en la web, el vídeo o la pantalla compartida no funcionarán.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ScreenCaptureAllowed
  - Nombre de la directiva de grupos: Permitir o denegar captura de pantalla
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ScreenCaptureAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ScreenCaptureAllowed
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ScrollToTextFragmentEnabled
  #### Habilitar el desplazamiento del texto especificado en los segmentos de la dirección URL
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 83 o posterior

  #### Descripción
  Esta característica permite que las navegaciones de direcciones URL de hipervínculo y la barra de direcciones destinen texto específico en una página web, que se desplazará después de que termine de cargarse la Página Web.

Si habilitas o no configuras esta directiva, se habilitará la opción de desplazar la página web a fragmentos de texto específicos a través de una dirección URL.

Si deshabilitas esta Directiva, se deshabilitará la opción de desplazamiento de la página web a fragmentos de texto específicos a través de una dirección URL.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ScrollToTextFragmentEnabled
  - Nombre de la directiva de grupos: Habilitar el desplazamiento del texto especificado en los segmentos de la dirección URL
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ScrollToTextFragmentEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ScrollToTextFragmentEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SearchSuggestEnabled
  #### Habilitar sugerencias de búsqueda
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Habilita las sugerencias de búsqueda web en la lista de sugerencias automáticas y la barra de direcciones de Microsoft Edge e impide que los usuarios cambien esta directiva.

Si se habilita esta directiva, se usarán las sugerencias de búsqueda web.

Si se deshabilita esta directiva, las sugerencias de búsqueda web no se usarán nunca, pero seguirán apareciendo las sugerencias de favoritos e historial locales. Si se deshabilita esta directiva, no se incluirán en telemetría a Microsoft ni los caracteres escritos ni las direcciones URL visitadas.

Si esta directiva se deja no establecida, las sugerencias de búsqueda estarán habilitadas, pero el usuario podrá modificarlas.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SearchSuggestEnabled
  - Nombre de la directiva de grupos: Habilitar sugerencias de búsqueda
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: SearchSuggestEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SearchSuggestEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SecurityKeyPermitAttestation
  #### Sitios web o dominios que no necesitan permiso para usar la atestación de clave de seguridad directa
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica los sitios web y dominios que no necesitan permiso explícito del usuario cuando se solicitan certificados de atestación de claves de seguridad. Además, se envía una señal a la clave de seguridad que indica que puede usar la atestación individual. Sin esto, se le preguntará a los usuarios cada vez que un sitio solicite la atestación de claves de seguridad.

Los sitios (por ejemplo, https://contoso.com/some/path) solo coinciden como U2F AppIDs. Los dominios (por ejemplo, contoso.com) solo coinciden como id. de webauthn RP. Para que tanto las API de U2F y de webauthn estén cubiertas en un sitio determinado, tienes que indicar el dominio y la dirección URL de appID.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SecurityKeyPermitAttestation
  - Nombre de la directiva de grupos: Sitios web o dominios que no necesitan permiso para usar la atestación de clave de seguridad directa
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation\1 = "https://contoso.com"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SecurityKeyPermitAttestation
  - Valor de ejemplo:
``` xml
<array>
  <string>https://contoso.com</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SendIntranetToInternetExplorer
  #### Enviar todos los sitios de la intranet a Internet Explorer
  
  
  #### Versiones admitidas:
  - En Windows desde 77 o posterior

  #### Descripción
  Para obtener instrucciones sobre cómo configurar la experiencia óptima para el modo de Internet Explorer, consulte [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SendIntranetToInternetExplorer
  - Nombre de la directiva de grupos: Enviar todos los sitios de la intranet a Internet Explorer
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: SendIntranetToInternetExplorer
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SendSiteInfoToImproveServices
  #### Enviar información del sitio para mejorar los servicios Microsoft (en desuso)
  >EN DESUSO: esta directiva está en desuso. Actualmente se admite pero será obsoleta en una versión futura.
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Esta directiva está en desuso. Actualmente, se admite pero quedará obsoleta en Microsoft Edge 89. Esta directiva se reemplaza por la nueva directiva:   [DiagnosticData](#diagnosticdata)para Windows 7, Windows 8 y macOS. Esta directiva se reemplaza por Permitir telemetría en Win 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

 Esta directiva permite enviar información acerca de los sitios web que visitas en Microsoft Edge a Microsoft para mejorar servicios como la búsqueda.

Habilita esta directiva para enviar información acerca de los sitios web que visitaste en Microsoft Edge a Microsoft. Deshabilita esta directiva para no enviar información acerca de los sitios web visitados en Microsoft Edge a Microsoft. En ambos casos, los usuarios no pueden cambiar o invalidar la configuración.

 En Windows 10, si no configuras esta directiva, Microsoft Edge usará de forma predeterminada la configuración de los datos de diagnóstico de Windows. Si esta directiva está habilitada, Microsoft Edge solo enviará información sobre los sitios web que visites en Microsoft Edge si la configuración de Datos de diagnóstico de Windows está establecida en Completo. Si se deshabilita esta directiva, Microsoft Edge no enviará información acerca de los sitios web visitados. Más información sobre la configuración de Datos de diagnóstico de Windows: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

 En Windows 7, Windows 8 y macOS esta directiva controla el envío de información sobre los sitios web visitados. Si no configuras esta directiva, Microsoft Edge usará de forma predeterminada las preferencias del usuario.

 Para habilitar esta directiva, [MetricsReportingEnabled](#metricsreportingenabled) debe establecerse en Habilitado. Si [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) o [MetricsReportingEnabled](#metricsreportingenabled) no se configuran o se deshabilitan, estos datos no se enviarán a Microsoft.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SendSiteInfoToImproveServices
  - Nombre de la directiva de grupos: Enviar información del sitio para mejorar los servicios Microsoft (en desuso)
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: SendSiteInfoToImproveServices
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SendSiteInfoToImproveServices
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SensorsAllowedForUrls
  #### Permitir el acceso a sensores en sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Define una lista de sitios, según los patrones de dirección URL, que pueden acceder a los sensores, como los sensores de movimiento y luz, y usarlos.

Si no configuras esta directiva, el valor predeterminado global de la directiva [DefaultSensorsSetting](#defaultsensorssetting) (si se ha establecido) o de la configuración personal del usuario se usa para todos los sitios.

Para patrones de direcciones URL que no coinciden con esta directiva, se usa el siguiente orden de prioridad: la directiva [SensorsBlockedForUrls](#sensorsblockedforurls) (si hay una coincidencia), la directiva [DefaultSensorsSetting](#defaultsensorssetting) (si está establecida) o la configuración personal del usuario.

Los patrones de dirección URL definidos en esta directiva no pueden entrar en conflicto con los configurados en la directiva [SensorsBlockedForUrls](#sensorsblockedforurls). No se puede permitir y bloquear una dirección URL.

Para obtener información detallada sobre los patrones de direcciones URL válidos, consulta [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SensorsAllowedForUrls
  - Nombre de la directiva de grupos: Permitir el acceso a sensores en sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SensorsAllowedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SensorsBlockedForUrls
  #### Bloquear el acceso a los sensores en sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Define una lista de sitios, según los patrones de dirección URL, que no pueden acceder a los sensores, como los sensores de movimiento y luz.

Si no configuras esta directiva, el valor predeterminado global de la directiva [DefaultSensorsSetting](#defaultsensorssetting) (si se ha establecido) o de la configuración personal del usuario se usa para todos los sitios.

Para patrones de direcciones URL que no coinciden con esta directiva, se usa el siguiente orden de prioridad: la directiva [SensorsAllowedForUrls](#sensorsallowedforurls) (si hay una coincidencia), la directiva [DefaultSensorsSetting](#defaultsensorssetting) (si está establecida) o la configuración personal del usuario.

Los patrones de dirección URL definidos en esta directiva no pueden entrar en conflicto con los configurados en la directiva [SensorsAllowedForUrls](#sensorsallowedforurls). No se puede permitir y bloquear una dirección URL.

Para obtener información detallada sobre los patrones de direcciones URL válidos, consulta [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SensorsBlockedForUrls
  - Nombre de la directiva de grupos: Bloquear el acceso a los sensores en sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SensorsBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SerialAskForUrls
  #### Permitir la API serie en sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Defina una lista de sitios, según los patrones de dirección URL, que pueden pedir al usuario acceso a un puerto serie.

Si no configura esta Directiva, el valor predeterminado global de la Directiva de [DefaultSerialGuardSetting](#defaultserialguardsetting) (si se ha establecido) o de la configuración personal del usuario se usa para todos los sitios.

Para patrones de direcciones URL que no coinciden con esta Directiva, se usa el siguiente orden de prioridad: la Directiva de [SerialBlockedForUrls](#serialblockedforurls) (si hay una coincidencia), la Directiva de [DefaultSerialGuardSetting](#defaultserialguardsetting) (si está establecida) o la configuración personal del usuario.

Los patrones de dirección URL definidos en esta Directiva no pueden entrar en conflicto con los configurados en la Directiva de [SerialBlockedForUrls](#serialblockedforurls). No se puede permitir ni bloquear una dirección URL.

Para obtener información detallada sobre los patrones de direcciones URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SerialAskForUrls
  - Nombre de la directiva de grupos: Permitir la API serie en sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SerialAskForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SerialBlockedForUrls
  #### Bloquear la API serie en sitios específicos
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Defina una lista de sitios, según los patrones de dirección URL, que no puedan pedir al usuario que les conceda acceso a un puerto serie.

Si no configura esta Directiva, el valor predeterminado global de la Directiva de [DefaultSerialGuardSetting](#defaultserialguardsetting) (si se ha establecido) o de la configuración personal del usuario se usa para todos los sitios.

Para patrones de direcciones URL que no coinciden con esta Directiva, se usa el siguiente orden de prioridad: la Directiva de [SerialAskForUrls](#serialaskforurls) (si hay una coincidencia), la Directiva de [DefaultSerialGuardSetting](#defaultserialguardsetting) (si está establecida) o la configuración personal del usuario.

Los patrones de dirección URL de esta Directiva no pueden entrar en conflicto con los configurados en la Directiva de [SerialAskForUrls](#serialaskforurls). No se puede permitir ni bloquear una dirección URL.

Para obtener información detallada sobre los patrones de direcciones URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SerialBlockedForUrls
  - Nombre de la directiva de grupos: Bloquear la API serie en sitios específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SerialBlockedForUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### ShowOfficeShortcutInFavoritesBar
  #### Mostrar el acceso directo de Microsoft Office en la barra de favoritos (en desuso)
  >EN DESUSO: esta directiva está en desuso. Actualmente se admite pero será obsoleta en una versión futura.
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Esta directiva no funcionó según lo esperado debido a cambios en los requisitos operativos. Por lo tanto, está en desuso y no debe usarse.

Especifica si se incluye un acceso directo a Office.com en la barra de favoritos. Para los usuarios que han iniciado sesión en Microsoft Edge, el acceso directo lleva a los usuarios a sus documentos y aplicaciones de Microsoft Office.
  Si habilitas o no configuras esta directiva, los usuarios pueden elegir si quieren ver el acceso directo cambiando el botón de alternancia en el menú contextual de la barra de favoritos.
  Si deshabilitas esta directiva, no se muestra el acceso directo.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: ShowOfficeShortcutInFavoritesBar
  - Nombre de la directiva de grupos: Mostrar el acceso directo de Microsoft Office en la barra de favoritos (en desuso)
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: ShowOfficeShortcutInFavoritesBar
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: ShowOfficeShortcutInFavoritesBar
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SignedHTTPExchangeEnabled
  #### Habilitar la compatibilidad con Exchange firmado de HTTP (SXG)
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 78 o posterior

  #### Descripción
  Habilitar la compatibilidad con HTTP de Exchange firmado (SXG).

Si no se configura o no se habilita esta directiva, Microsoft Edge aceptará contenido web servidos como HTTP de Exchange firmados.

Si esta directiva se establece en deshabilitada, no se cargarán los HTTP de Exchange firmados.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SignedHTTPExchangeEnabled
  - Nombre de la directiva de grupos: Habilitar la compatibilidad con Exchange firmado de HTTP (SXG)
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: SignedHTTPExchangeEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SignedHTTPExchangeEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SitePerProcess
  #### Habilitar el aislamiento de sitios para cada sitio
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  La directiva [SitePerProcess](#siteperprocess) se puede usar para impedir que los usuarios opten por el comportamiento predeterminado de aislar todos los sitios. Ten en cuenta que también puedes usar la directiva [IsolateOrigins](#isolateorigins) para aislar orígenes adicionales y más específicos.

Si se habilita esta directiva, los usuarios no pueden optar por el comportamiento predeterminado en el que cada sitio se ejecuta en su propio proceso.

Si se deshabilita o no se configura esta directiva, un usuario puede optar por el aislamiento del sitio. (Por ejemplo, con la entrada "Deshabilitar aislamiento de sitio" en edge://flags.) Si se deshabilita o no se configura la directiva, no se desactivará el aislamiento del sitio.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SitePerProcess
  - Nombre de la directiva de grupos: Habilitar el aislamiento de sitios para cada sitio
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: SitePerProcess
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SitePerProcess
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SpellcheckEnabled
  #### Habilitar corrector ortográfico
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Si se habilita o no se configura esta directiva, el usuario puede usar el corrector ortográfico.

Si se deshabilita esta directiva, el usuario no puede usar el corrector ortográfico y también se deshabilitan las directivas [SpellcheckLanguage](#spellchecklanguage) y [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SpellcheckEnabled
  - Nombre de la directiva de grupos: Habilitar corrector ortográfico
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: SpellcheckEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SpellcheckEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SpellcheckLanguage
  #### Habilitar los idiomas de corrección ortográfica específicos
  
  
  #### Versiones admitidas:
  - En Windows desde 77 o posterior

  #### Descripción
  Habilita diferentes idiomas para la corrección ortográfica. Se omitirá cualquier idioma que especifique que no se reconozca.

Si se habilita esta directiva, la corrección ortográfica se habilitará para los idiomas especificados, así como para los idiomas que el usuario haya habilitado.

Si no se configura o si se deshabilita esta directiva, no habrá ningún cambio en las preferencias de corrección ortográfica del usuario.

Si la directiva [SpellcheckEnabled](#spellcheckenabled) está deshabilitada, esta directiva no tendrá efecto.

Si un idioma está incluido en la directiva 'SpellcheckLanguage' y en la directiva [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist), el idioma de corrección ortográfica estará habilitado.

Los idiomas compatibles son: af, bg, ca, cs, cy, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SpellcheckLanguage
  - Nombre de la directiva de grupos: Habilitar los idiomas de corrección ortográfica específicos
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\2 = "es"

```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SpellcheckLanguageBlocklist
  #### Forzar deshabilitar idiomas de corrección ortográfica
  
  
  #### Versiones admitidas:
  - En Windows desde 78 o posterior

  #### Descripción
  Fuerza la deshabilitación de idiomas para la revisión ortográfica. Se omitirán los idiomas no reconocidos de la lista.

Si se habilita esta directiva, se deshabilitará la revisión ortográfica para los idiomas especificados. El usuario puede seguir habilitando o deshabilitando la revisión ortográfica para los idiomas que no estén en la lista.

Si no se establece esta directiva o se deshabilita, no se cambiarán las preferencias de revisión ortográfica del usuario.

Si la directiva [SpellcheckEnabled](#spellcheckenabled) está establecida en deshabilitada, esta directiva no tendrá ningún efecto.

Si un idioma se incluye en las directivas [SpellcheckLanguage](#spellchecklanguage) y 'SpellcheckLanguageBlocklist', se habilitará el idioma para la corrección ortográfica.

Los idiomas admitidos actualmente son: af, bg, ca, cs, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SpellcheckLanguageBlocklist
  - Nombre de la directiva de grupos: Forzar deshabilitar idiomas de corrección ortográfica
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\2 = "es"

```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### StricterMixedContentTreatmentEnabled
  #### Habilitar el tratamiento más estricto para el contenido mixto (en desuso)
  >EN DESUSO: esta directiva está en desuso. Actualmente se admite pero será obsoleta en una versión futura.
  
  #### Versiones admitidas:
  - En Windows y macOS desde 81 o posterior

  #### Descripción
  Esta directiva está en desuso, ya que solo se pensó como un mecanismo a corto plazo para ofrecer a las empresas más tiempo para actualizar el contenido web en caso de que se compruebe que no es compatible con el tratamiento de contenido mixto más estricto. No funcionará para Microsoft Edge en la versión 85.

 Esta directiva controla el tratamiento para contenido mixto (contenido HTTP en sitios HTTPS) en el explorador.

Si estableces esta directiva en "true" o no la configuras, el contenido de audio y vídeo mixto se actualizará automáticamente a HTTPS (es decir, la dirección URL se reescribirá como HTTPS, sin una opción de reserva si el recurso no está disponible a través de HTTPS) y en la barra URL se mostrará un mensaje de advertencia de "No seguro" para el contenido mixto.

Si estableces la directiva en "false", se deshabilitarán las actualizaciones automáticas para el audio y el vídeo, y no se mostrará ninguna advertencia para las imágenes.

Esta directiva no afecta a otros tipos de contenido mixto excepto el audio, el vídeo y las imágenes.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: StricterMixedContentTreatmentEnabled
  - Nombre de la directiva de grupos: Habilitar el tratamiento más estricto para el contenido mixto (en desuso)
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: StricterMixedContentTreatmentEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: StricterMixedContentTreatmentEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SuppressUnsupportedOSWarning
  #### Suprimir la advertencia de sistema operativo no compatible
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Suprime la advertencia que aparece cuando Microsoft Edge se está ejecutando en un equipo o un sistema operativo que ya no se admite.

Si esta directiva es falsa o no se establece, las advertencias aparecerán en estos equipos o sistemas operativos no compatibles.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SuppressUnsupportedOSWarning
  - Nombre de la directiva de grupos: Suprimir la advertencia de sistema operativo no compatible
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: SuppressUnsupportedOSWarning
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SuppressUnsupportedOSWarning
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SyncDisabled
  #### Deshabilitar la sincronización de datos mediante los servicios de sincronización de Microsoft
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Deshabilita la sincronización de datos en Microsoft Edge. Esta directiva también impide que aparezca la pregunta de consentimiento de sincronización.

Si no se establece esta directiva o no se aplica de la forma recomendada, los usuarios podrán activar o desactivar la sincronización. Si se aplica esta directiva como obligatoria, los usuarios no podrán activar la sincronización.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SyncDisabled
  - Nombre de la directiva de grupos: Deshabilitar la sincronización de datos mediante los servicios de sincronización de Microsoft
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: SyncDisabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SyncDisabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### SyncTypesListDisabled
  #### Configurar la lista de tipos que están excluidos de la sincronización
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 83 o posterior

  #### Descripción
  Si habilita esta directiva, todos los tipos de datos especificados se excluirán de la sincronización. Esta directiva se puede usar para restringir el tipo de datos que se cargan al servicio de sincronización de Microsoft Edge.

Puede proporcionar uno de los siguientes tipos de datos para esta directiva: "favoritos", "configuración", "contraseñas", "direccionesYMás", "extensiones", "historial", "pestañasAbiertas" y "colecciones". Tenga en cuenta que estos nombres de tipo de datos distinguen entre mayúsculas y minúsculas.

Los usuarios no podrán invalidar los tipos de datos deshabilitados.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: SyncTypesListDisabled
  - Nombre de la directiva de grupos: Configurar la lista de tipos que están excluidos de la sincronización
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled\1 = "favorites"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: SyncTypesListDisabled
  - Valor de ejemplo:
``` xml
<array>
  <string>favorites</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### TLS13HardeningForLocalAnchorsEnabled
  #### Habilite una característica de seguridad de TLS 1.3 para anclajes locales de confianza. (obsoleto)
  
  >OBSOLETO: Esta directiva es obsoleta y no funciona después de la versión 85 de Microsoft Edge.
  #### Versiones admitidas:
  - En Windows y macOS desde 81, hasta 85

  #### Descripción
  Esta directiva no funciona porque solo tenía la intención de ser un mecanismo a corto plazo para dar a las empresas más tiempo para actualizar los proxies afectados.

Esta directiva controla una característica de seguridad en TLS 1.3 que protege las conexiones contra ataques de degradación. Es compatible con versiones anteriores y no afectará a las conexiones a servidores o servidores proxy TLS 1.2 compatibles. Sin embargo, las versiones anteriores de algunos servidores proxy de interceptación de TLS tienen un error de implementación, lo que hace que sean incompatibles.

Si se habilita esta directiva,  Microsoft Edgehabilitará estas protecciones de seguridad para todas las conexiones.

Si se deshabilita esta directiva o no se configura, Microsoft Edge deshabilitará estas protecciones de seguridad para las conexiones autenticadas con certificados de entidad de certificación instalados localmente. Estas protecciones siempre están habilitadas para las conexiones autenticadas con certificados de entidad de certificación de confianza pública.

Esta directiva puede usarse para probar cualquier proxy afectado y actualizarlo. Se espera que los servidores proxy afectados den error en las conexiones con el código de error ERR_TLS13_DOWNGRADE_DETECTED.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: TLS13HardeningForLocalAnchorsEnabled
  - Nombre de la directiva de grupos: Habilite una característica de seguridad de TLS 1.3 para anclajes locales de confianza. (obsoleto)
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: TLS13HardeningForLocalAnchorsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: TLS13HardeningForLocalAnchorsEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### TLSCipherSuiteDenyList
  #### Especificar los conjuntos de cifrado TLS para deshabilitar
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 85 o posterior

  #### Descripción
  Configure la lista de conjuntos de cifrado que están deshabilitados para las conexiones TLS.

Si configura esta directiva, no se usará la lista de conjuntos de cifrado configurados al establecer conexiones TLS.

Si no configura esta directiva, el explorador elegirá los conjuntos de cifrado de TLS que se usarán.

Los valores del conjunto de cifrado que se va a deshabilitar se especifican como valores hexadecimales de 16 bits. Los valores los asigna el registro de la autoridad de números asignados de Internet (IANA).

El conjunto de cifrado de TLS 1.3 TLS_AES_128_GCM_SHA256 (0x1301) es necesario para TLS 1.3 y esta directiva no puede deshabilitarlo.

Esta directiva no afecta a las conexiones basadas en QUIC. Puede desactivar QUIC con la directiva [QuicAllowed](#quicallowed).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: TLSCipherSuiteDenyList
  - Nombre de la directiva de grupos: Especificar los conjuntos de cifrado TLS para deshabilitar
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\1 = "0x1303"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\2 = "0xcca8"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\3 = "0xcca9"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: TLSCipherSuiteDenyList
  - Valor de ejemplo:
``` xml
<array>
  <string>0x1303</string>
  <string>0xcca8</string>
  <string>0xcca9</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### TabFreezingEnabled
  #### Permitir la inmovilización de pestañas en segundo plano
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 79 o posterior

  #### Descripción
  Controla si Microsoft Edge puede inmovilizar las pestañas que están en segundo plano durante al menos 5 minutos.

La inmovilización de pestañas reduce el uso de la CPU, la batería y la memoria. Microsoft Edge usa heurística para evitar inmovilizar las pestañas que realizan trabajo útil en segundo plano, como mostrar notificaciones, reproducir sonido y transmitir vídeo.

Si se habilita o no se configura esta directiva, es posible que las pestañas que han estado en segundo plano durante al menos 5 minutos estén inmovilizadas.

Si se deshabilita esta directiva, no se inmovilizará ninguna pestaña.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: TabFreezingEnabled
  - Nombre de la directiva de grupos: Permitir la inmovilización de pestañas en segundo plano
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: TabFreezingEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: TabFreezingEnabled
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### TaskManagerEndProcessEnabled
  #### Habilitar finalizar procesos en el Administrador de tareas del explorador
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Si se habilita o no se configura esta directiva, los usuarios pueden finalizar procesos en el Administrador de tareas del explorador. Si se deshabilita, los usuarios no pueden finalizar los procesos y el botón de Finalizar proceso estará deshabilitado en el Administrador de tareas del explorador.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: TaskManagerEndProcessEnabled
  - Nombre de la directiva de grupos: Habilitar finalizar procesos en el Administrador de tareas del explorador
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: TaskManagerEndProcessEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: TaskManagerEndProcessEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### TotalMemoryLimitMb
  #### Establezca el límite de megabytes de memoria que puede usar una única instancia de Microsoft Edge.
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 80 o posterior

  #### Descripción
  Configura la cantidad de memoria que puede usar una única instancia de Microsoft Edge antes de que las pestañas empiecen a descartarse para ahorrar memoria. La memoria usada por la pestaña se liberará y será necesario volver a cargar la pestaña cuando se cambie a la misma.

Si se habilita esta directiva, el explorador empezará a descartar las pestañas para ahorrar memoria una vez que se supere el límite. Sin embargo, no hay ninguna garantía de que el explorador siempre se esté ejecutando bajo el límite. Cualquier valor por debajo de 1024 se redondeará a 1024.

Si no se establece esta directiva, el explorador solo intentará ahorrar memoria cuando detecte que la cantidad de memoria física de su máquina es baja.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: TotalMemoryLimitMb
  - Nombre de la directiva de grupos: Establezca el límite de megabytes de memoria que puede usar una única instancia de Microsoft Edge.
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: TotalMemoryLimitMb
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000800
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: TotalMemoryLimitMb
  - Valor de ejemplo:
``` xml
<integer>2048</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### TrackingPrevention
  #### Bloquear el seguimiento de la actividad de exploración web de los usuarios
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 78 o posterior

  #### Descripción
  Te permite decidir si quieres impedir que los sitios web realicen un seguimiento de la actividad de los usuarios.

Si deshabilitas esta directiva o no la configuras, los usuarios podrán establecer su propio nivel de prevención de seguimiento.

Asignación de opciones de directiva:

* TrackingPreventionOff (0) = Desactivado (sin prevención de seguimiento)

* TrackingPreventionBasic (1) = Básico (bloquea los rastreadores dañinos, el contenido y los anuncios se personalizarán)

* TrackingPreventionBalanced (2) = Equilibrado (bloquea los rastreadores y rastreadores dañinos del usuario de los sitios que no ha visitado; el contenido y los anuncios serán menos personalizados).

* TrackingPreventionStrict (3) = Estricto (bloquea los rastreadores dañinos y la mayoría de los rastreadores de todos los sitios; el contenido y los anuncios tendrán una personalización mínima. Es posible que algunas partes de los sitios no funcionen)

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: TrackingPrevention
  - Nombre de la directiva de grupos: Bloquear el seguimiento de la actividad de exploración web de los usuarios
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: TrackingPrevention
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000002
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: TrackingPrevention
  - Valor de ejemplo:
``` xml
<integer>2</integer>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### TranslateEnabled
  #### Habilitar Traducir
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Habilita el servicio de traducción de Microsoft integrado en Microsoft Edge.

Si se habilita esta directiva, Microsoft Edge ofrece funcionalidad de traducción al usuario mostrando un control flotante de traducción integrado (cuando corresponda) y una opción de traducción en el menú contextual.

Deshabilite esta directiva para deshabilitar todas las características de traducción integradas.

Si no se establece la directiva, los usuarios podrán elegir si quieren usar la funcionalidad de traducción o no.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: Sí
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: TranslateEnabled
  - Nombre de la directiva de grupos: Habilitar Traducir
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): Plantillas administrativas/Microsoft Edge - Configuración predeterminada (los usuarios pueden cambiarla)/
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): SOFTWARE\Policies\Microsoft\Edge\Recomendada
  - Nombre del valor: TranslateEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: TranslateEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### URLAllowlist
  #### Definir una lista de direcciones URL permitidas
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permita el acceso a las direcciones URL enumeradas, como excepciones a la lista de direcciones URL bloqueadas.

Formatee el patrón de dirección URL según [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Puede usar esta directiva para abrir excepciones a listas de bloqueadas restrictivas. Por ejemplo, puede incluir "*" en la lista de bloqueo para bloquear todas las solicitudes y luego usar esta directiva para permitir el acceso a una lista limitada de direcciones URL. Puede usar esta directiva para abrir excepciones a ciertos esquemas, subdominios de otros dominios, puertos o rutas específicas.

El filtro más específico determina si una dirección URL está bloqueada o permitida. La lista de permitidos tiene prioridad sobre la lista de bloqueos.

Esta directiva está limitada a 1000 entradas; las entradas posteriores se ignorarán.

Esta directiva también permite que el navegador invoque automáticamente las aplicaciones externas registradas como controladores de protocolo para protocolos como "tel:" o "ssh:".

Si no se configura esta directiva, no hay excepciones a la lista de bloqueo de la [URLBlocklist](#urlblocklist) directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: URLAllowlist
  - Nombre de la directiva de grupos: Definir una lista de direcciones URL permitidas
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\URLAllowlist
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\5 = ".exact.hostname.com"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: URLAllowlist
  - Valor de ejemplo:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### URLBlocklist
  #### Bloquear el acceso a una lista de direcciones URL
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Defina una lista de sitios, según los patrones de URL, que están bloqueados (los usuarios no pueden cargarlos).

Formatee el patrón de dirección URL según [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Puede definir excepciones en la directiva [URLAllowlist](#urlallowlist). Estas directivas están limitadas a 1000 entradas; las entradas posteriores se omitirán.

Tenga en cuenta que no se recomienda bloquear las URL 'edge://*' internas, ya que esto podría provocar errores inesperados.

Esta directiva no impide que la página se actualice dinámicamente a través de JavaScript. Por ejemplo, si bloquea 'contoso.com/abc', los usuarios aún podrán visitar 'contoso.com' y hacer clic en un vínculo para visitar 'contoso.com/abc', siempre y cuando la página no se actualice.

Si no configura esta directiva, no se bloqueará ninguna URL.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: URLBlocklist
  - Nombre de la directiva de grupos: Bloquear el acceso a una lista de direcciones URL
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\URLBlocklist
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
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


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: URLBlocklist
  - Valor de ejemplo:
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
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### UserAgentClientHintsEnabled
  #### Habilitar la característica de sugerencias del cliente del agente de usuario (en desuso)
  >EN DESUSO: esta directiva está en desuso. Actualmente se admite pero será obsoleta en una versión futura.
  
  #### Versiones admitidas:
  - En Windows y macOS desde 86 o posterior

  #### Descripción
  Esta directiva está en desuso, ya que solo se ha diseñado para ser un mecanismo a corto plazo con el fin de que las empresas puedan actualizar su contenido web en caso de que se detecte que no es compatible con la característica de sugerencias del cliente del agente de usuario. No funcionará en la versión 89 de Microsoft Edge.

Cuando está habilitada, la característica de sugerencias de usuario agente de cliente envía encabezados de solicitud granulares que proporcionan información sobre el explorador del usuario (por ejemplo, la versión del explorador) y el entorno (por ejemplo, la arquitectura del sistema).

Esta es una característica adicional, pero los nuevos encabezados pueden romper algunos sitios web que restringen los caracteres que pueden contener las solicitudes.

Si habilita o no configura esta directiva, se habilitará la característica de sugerencias de usuario agente de cliente. Si deshabilita esta directiva, esta característica no estará disponible.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: UserAgentClientHintsEnabled
  - Nombre de la directiva de grupos: Habilitar la característica de sugerencias del cliente del agente de usuario (en desuso)
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: UserAgentClientHintsEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: UserAgentClientHintsEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### UserDataDir
  #### Establecer el directorio de datos de usuario
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Establecer el directorio que se va a usar para almacenar los datos del usuario.

Si se habilita esta directiva, Microsoft Edge usará el directorio especificado independientemente de si el usuario ha establecido la marca de línea de comandos '--user-data-dir'.

Si no se habilita esta directiva, se usará la ruta de acceso del perfil, pero el usuario podrá anularla usando la marca '--user-data-dir'. Los usuarios podrán encontrar el directorio para el perfil en edge://version/ en la ruta de acceso del perfil.

Para evitar la pérdida de datos u otros errores, no se debe configurar esta directiva en el directorio raíz de un volumen o en un directorio usado para otros fines, ya que Microsoft Edge administra su contenido.

Consulte [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) para ver una lista de variables que se pueden usar.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: UserDataDir
  - Nombre de la directiva de grupos: Establecer el directorio de datos de usuario
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: UserDataDir
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"${users}/${user_name}/Edge"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: UserDataDir
  - Valor de ejemplo:
``` xml
<string>${users}/${user_name}/Edge</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### UserDataSnapshotRetentionLimit
  #### Limita el número de instantáneas de datos de usuario que se conservan para su uso en caso de reversión de emergencia
  
  
  #### Versiones admitidas:
  - En Windows desde 86 o posterior

  #### Descripción
  Después de cada actualización de versión principal, Microsoft Edge creará una instantánea de partes de los datos de navegación del usuario para usar en caso de una emergencia posterior que requiera una reversión temporal de la versión. Si se realiza una reversión temporal a una versión para la que un usuario tiene una instantánea correspondiente, se restauran los datos de la instantánea. Esto permite a los usuarios mantener configuraciones como marcadores y datos de autocompletar.

Si no se establece esta directiva, se usa el valor predeterminado de 3 instantáneas.

Si se establece esta directiva, instantáneas antiguas se eliminan según sea necesario para respetar el límite establecido. Si se configura esta directiva en 0, no se toman instantáneas.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Entero

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: UserDataSnapshotRetentionLimit
  - Nombre de la directiva de grupos: Limita el número de instantáneas de datos de usuario que se conservan para su uso en caso de reversión de emergencia
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: UserDataSnapshotRetentionLimit
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000003
```


  

  [Volver al principio](#microsoft-edge:-directivas)

  ### UserFeedbackAllowed
  #### Permitir comentarios del usuario
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Microsoft Edge usa la característica Comentarios de Edge (habilitada de manera predeterminada) para permitir que los usuarios envíen comentarios, sugerencias o encuestas sobre los clientes y para informar de problemas con el explorador. Además, de manera predeterminada, los usuarios no pueden deshabilitar (desactivar) la característica Comentarios de Edge.

Si se habilita esta directiva o no se configura, los usuarios podrán invocar Comentarios de Edge.

Si se deshabilita esta directiva, los usuarios no podrán invocar Comentarios de Edge.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: UserFeedbackAllowed
  - Nombre de la directiva de grupos: Permitir comentarios del usuario
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: UserFeedbackAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: UserFeedbackAllowed
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### VideoCaptureAllowed
  #### Permitir o bloquear la captura de vídeo
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Controle si los sitios pueden capturar vídeo.

Si se habilita o no se configura (valor predeterminado), se preguntará al usuario acerca del acceso de la captura de vídeo para todos los sitios excepto para los que tengan URL configuradas en la lista de directivas [VideoCaptureAllowedUrls](#videocaptureallowedurls), a los que se les concederá acceso sin preguntar.

Si deshabilita esta directiva, no se preguntará al usuario y la captura de vídeo solo estará disponible para las URL configuradas en la directiva [VideoCaptureAllowedUrls](#videocaptureallowedurls).

Esta directiva afecta a todos los tipos de entradas de vídeo, no solo a la cámara integrada.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: VideoCaptureAllowed
  - Nombre de la directiva de grupos: Permitir o bloquear la captura de vídeo
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: VideoCaptureAllowed
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000000
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: VideoCaptureAllowed
  - Valor de ejemplo:
``` xml
<false/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### VideoCaptureAllowedUrls
  #### Sitios que pueden acceder a dispositivos de captura de vídeo sin solicitar permiso
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Especifica los sitios web, según los patrones de dirección URL, que pueden usar dispositivos de captura de vídeo sin pedirle permiso al usuario. Los patrones de esta lista se comparan con el origen de la seguridad de la dirección URL de la solicitud. Si coinciden, el sitio tendrá acceso automáticamente a los dispositivos de captura de vídeo.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: VideoCaptureAllowedUrls
  - Nombre de la directiva de grupos: Sitios que pueden acceder a dispositivos de captura de vídeo sin solicitar permiso
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: VideoCaptureAllowedUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### WPADQuickCheckEnabled
  #### Establecer la optimización de WPAD
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Le permite desconectar la optimización de WPAD (detección automática de proxy web) en Microsoft Edge.

Si se deshabilita esta directiva, la optimización de WPAD se deshabilitará, lo que hará que el explorador tenga que esperar más tiempo a los servidores de WPAD basados en DNS.

Si se habilita o no se configura la directiva, la optimización de WPAD se habilitará.

Independientemente de cómo se habilite esta directiva y de si está o no habilitada, los usuarios no podrán cambiar la configuración de optimización de WPAD.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: WPADQuickCheckEnabled
  - Nombre de la directiva de grupos: Establecer la optimización de WPAD
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: WPADQuickCheckEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: WPADQuickCheckEnabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### WebAppInstallForceList
  #### Configurar la lista de aplicaciones web instaladas por la fuerza
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 80 o posterior

  #### Descripción
  Configura esta directiva para especificar una lista de aplicaciones web que se instalan silenciosamente, sin interacción del usuario y que los usuarios no pueden desinstalar ni desactivar.

Cada elemento de lista de la directiva es un objeto con un miembro obligatorio: url (la dirección URL de la aplicación web que se va a instalar) y 2 miembros opcionales: default_launch_container (especifica el modo de ventana con el que se abre la aplicación web: una nueva pestaña es el valor predeterminado) y create_desktop_shortcut (verdadero si quiere crear Linux y accesos directos del escritorio de Windows).

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: Sí

  #### Tipo de datos:
  - Diccionario

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: WebAppInstallForceList
  - Nombre de la directiva de grupos: Configurar la lista de aplicaciones web instaladas por la fuerza
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: WebAppInstallForceList
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
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


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: WebAppInstallForceList
  - Valor de ejemplo:
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
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### WebComponentsV0Enabled
  #### Vuelva a habilitar la API de Web Components v0 hasta M84 (obsoleto)
  
  >OBSOLETO: Esta directiva es obsoleta y no funciona después de la versión 84 de Microsoft Edge.
  #### Versiones admitidas:
  - En Windows y macOS desde 80, hasta 84

  #### Descripción
  Esta directiva no funcionará porque permitía que estas características se reactivaran selectivamente hasta la versión 85 de Microsoft Edge. Las API de Web Components v0 (Shadow DOM v0, Custom Elements v0, e importaciones de HTML) fueron desactivadas en 2018, y han sido desactivadas de forma predeterminada en la versión 80 de Microsoft Edge.

Si estableces esta configuración de directiva como verdadera, se habilitarán las características de Web Components v0 en todos los sitios.

Si estableces esta directiva como falsa o no la estableces, las características de Web Components v0 se deshabilitarán de forma predeterminada, a partir de la versión 80 de Microsoft Edge.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: WebComponentsV0Enabled
  - Nombre de la directiva de grupos: Vuelva a habilitar la API de Web Components v0 hasta M84 (obsoleto)
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: WebComponentsV0Enabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: WebComponentsV0Enabled
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### WebDriverOverridesIncompatiblePolicies
  #### Permitir que WebDriver invalide las directivas incompatibles (obsoleto)
  
  >OBSOLETO: Esta directiva es obsoleta y no funciona después de la versión 84 de Microsoft Edge.
  #### Versiones admitidas:
  - En Windows y macOS desde 77, hasta 84

  #### Descripción
  Esta directiva no funciona porque WebDriver es ahora compatible con todas las directivas existentes.

    Esta directiva permite a los usuarios de la característica WebDriver reemplazar las directivas de
    que pueden interferir con su operación.

    Actualmente, esta directiva deshabilita las directivas [SitePerProcess](#siteperprocess) y [IsolateOrigins](#isolateorigins).

    Si la directiva está habilitada, WebDriver podrá reemplazar las directivas
no compatibles.
    Si la directiva está deshabilitada o no está configurada, no se permitirá que WebDriver
    reemplace directivas incompatibles.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: WebDriverOverridesIncompatiblePolicies
  - Nombre de la directiva de grupos: Permitir que WebDriver invalide las directivas incompatibles (obsoleto)
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: WebDriverOverridesIncompatiblePolicies
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: WebDriverOverridesIncompatiblePolicies
  - Valor de ejemplo:
``` xml
<true/>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### WebRtcLocalIpsAllowedUrls
  #### Administrar la exposición de direcciones IP locales por WebRTC
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 80 o posterior

  #### Descripción
  Especifica una lista de orígenes (URL) o patrones de nombre de host (como "*contoso.com*") para los que WebRTC debe exponer la dirección IP local.

Si se habilita esta directiva y se establece una lista de orígenes (URL) o patrones de nombre de host, cuando se habilite edge://flags/#enable-webrtc-hide-local-ips-with-mdns, WebRTC expondrá la dirección IP local para los casos que coincidan con los patrones de la lista.

Si se deshabilita o no se configura esta directiva y edge://flags/#enable-webrtc-hide-local-ips-with-mdns está habilitado, WebRTC no expondrá direcciones IP locales. La dirección IP local se oculta con un nombre de host mDNS.

Si se habilita, se deshabilita o no se configura esta directiva, y edge://flags/#enable-webrtc-hide-local-ips-with-mdns está deshabilitado, WebRTC expondrá las direcciones IP locales.

Tenga en cuenta que esta directiva debilita la protección de las direcciones IP locales que pueden necesitar los administradores.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Lista de cadenas

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: WebRtcLocalIpsAllowedUrls
  - Nombre de la directiva de grupos: Administrar la exposición de direcciones IP locales por WebRTC
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: 1, 2, 3, ...
  - Tipo de valor: lista de REG_SZ
  ##### Valor de ejemplo:
```
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\2 = "*contoso.com*"

```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: WebRtcLocalIpsAllowedUrls
  - Valor de ejemplo:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>*contoso.com*</string>
</array>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### WebRtcLocalhostIpHandling
  #### Restringir la exposición de la dirección IP local por WebRTC
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Permite establecer si WebRTC expone la dirección IP local del usuario.

Si se establece esta directiva en "AllowAllInterfaces" o "AllowPublicAndPrivateInterfaces", WebRTC expone la dirección IP local.

Si se establece esta directiva en "AllowPublicInterfaceOnly" o "DisableNonProxiedUdp", WebRTC no expone la dirección IP local.

Si no se establece esta directiva o si se deshabilita, WebRTC expone la dirección IP local.

Asignación de opciones de directiva:

* AllowAllInterfaces (default) = Permitir todas las interfaces. Esto expone la dirección IP local

* AllowPublicAndPrivateInterfaces (default_public_and_private_interfaces) = Permitir interfaces públicas y privadas sobre la ruta predeterminada http. Esto expone la dirección IP local

* AllowPublicInterfaceOnly (default_public_interface_only) = Permitir la interfaz pública a través de la ruta predeterminada http. Esto no expone la dirección IP local

* DisableNonProxiedUdp (disable_non_proxied_udp) = Usar TCP a menos que el servidor proxy sea compatible con UDP. Esto no expone la dirección IP local

Usa la información anterior al configurar esta directiva.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: WebRtcLocalhostIpHandling
  - Nombre de la directiva de grupos: Restringir la exposición de la dirección IP local por WebRTC
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: WebRtcLocalhostIpHandling
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"default"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: WebRtcLocalhostIpHandling
  - Valor de ejemplo:
``` xml
<string>default</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### WebRtcUdpPortRange
  #### Restringir el intervalo de puertos UDP locales usados por WebRTC
  
  
  #### Versiones admitidas:
  - En Windows y macOS desde 77 o posterior

  #### Descripción
  Restringe el intervalo de puertos UDP usado por WebRTC a un intervalo de puertos especificado (puntos de conexión incluidos).

Mediante la configuración de esta directiva, debes especificar el intervalo de puertos UDP locales que WebRTC puede usar.

Si no se configura esta directiva o si se establece en una cadena vacía o en un intervalo de puertos no válido, WebRTC puede usar cualquier puerto UDP local disponible.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Cadena

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: WebRtcUdpPortRange
  - Nombre de la directiva de grupos: Restringir el intervalo de puertos UDP locales usados por WebRTC
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: WebRtcUdpPortRange
  - Tipo de valor: REG_SZ
  ##### Valor de ejemplo:
```
"10000-11999"
```


  #### Información y configuración de Mac
  - Nombre de clave de preferencia: WebRtcUdpPortRange
  - Valor de ejemplo:
``` xml
<string>10000-11999</string>
```
  

  [Volver al principio](#microsoft-edge:-directivas)

  ### WinHttpProxyResolverEnabled
  #### Usar resolución de proxy de Windows (en desuso)
  >EN DESUSO: esta directiva está en desuso. Actualmente se admite pero será obsoleta en una versión futura.
  
  #### Versiones admitidas:
  - En Windows desde 84 o posterior

  #### Descripción
  Esta directiva está en desuso porque será reemplazada por una característica similar en una versión futura, consulte https://crbug.com/1032820.

Utilice Windows para solucionar proxies para todas las redes de navegadores en lugar del solucionador de proxy integrado en Microsoft Edge. El solucionador de proxy de Windows admite característica de proxy de Windows como DirectAccess/NRPT.

Esta directiva viene con los problemas descritos por https://crbug.com/644030. Lo que causa que los archivos PAC sean recuperados y ejecutados por el código de Windows, incluidos los archivos PAC configurados por la directiva [ProxyPacUrl](#proxypacurl). Como las búsquedas en red para el archivo PAC ocurren por Windows en lugar del código de Microsoft Edge, las directivas de red como [DnsOverHttpsMode](#dnsoverhttpsmode) no se aplicarán a las búsquedas de red para un archivo PAC.

Si habilita esta directiva, se usará la resolución del proxy de Windows.

Si deshabilita o no configura esta directiva, se usará la resolución de proxy de Microsoft Edge.

  #### Características admitidas:
  - Puede ser obligatorio: Sí
  - Se puede recomendar: No
  - Actualización de directiva dinámica: No - Requiere reiniciar el explorador

  #### Tipo de datos:
  - Booleano

  #### Información y configuración de Windows
  ##### Información de la directiva de grupos (ADMX)
  - Nombre único de la directiva de grupos: WinHttpProxyResolverEnabled
  - Nombre de la directiva de grupos: Usar resolución de proxy de Windows (en desuso)
  - Ruta de acceso de GP (Obligatorio): Plantillas administrativas/Microsoft Edge/
  - Ruta de acceso de GP (Recomendada): N/D
  - Nombre del archivo ADMX de GP: MSEdge.admx
  ##### Configuración del registro de Windows
  - Ruta de acceso (Obligatorio): SOFTWARE\Policies\Microsoft\Edge
  - Ruta de acceso (Recomendada): N/D
  - Nombre del valor: WinHttpProxyResolverEnabled
  - Tipo de valor: REG_DWORD
  ##### Valor de ejemplo:
```
0x00000001
```


  

  [Volver al principio](#microsoft-edge:-directivas)


## Vea también
- [Configurando Microsoft Edge](configure-microsoft-edge.md)
- [Página de aterrizaje de Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Blog de bases de referencia de seguridad de Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)