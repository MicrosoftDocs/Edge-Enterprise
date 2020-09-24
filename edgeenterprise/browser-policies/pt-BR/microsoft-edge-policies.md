---
title: "Microsoft Edge Browser Policy Documentation"
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 09/14/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom:
description: "Windows and Mac documentation for all policies supported by the Microsoft Edge Browser"
---

# Microsoft Edge - Políticas
A versão mais recente do Microsoft Edge inclui as seguintes políticas. Você pode usar essas políticas para configurar como o Microsoft Edge é executado em sua organização.

Para obter informações sobre um conjunto adicional de políticas usadas para controlar como e quando o Microsoft Edge é atualizado, confira [Referência de política de atualização do Microsoft Edge](microsoft-edge-update-policies.md).

Você pode fazer o download de [Kit de Ferramentas do Microsoft Security Compliance](https://www.microsoft.com/download/details.aspx?id=55319) para configurações de linha de base recomendadas da configuração de segurança do Microsoft Edge. Para mais informações, confira o [Blog das Linhas de Base de Segurança da Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines).

> [!OBSERVAÇÃO]
> Este artigo se aplica ao Microsoft Edge versão 77 ou posterior.

## Políticas disponíveis
Estas tabelas listam todas as políticas de grupo relacionadas ao navegador disponíveis nesta versão do Microsoft Edge. Use os links na tabela para obter mais detalhes sobre políticas específicas.

|||
|-|-|
|[Autenticação HTTP](#autenticação-http)|[Cast](#cast)|
|[Configurações de conteúdo](#configurações-de-conteúdo)|[Configurações do Application Guard](#configurações-do-application-guard)|
|[Configurações do SmartScreen](#configurações-do-smartscreen)|[Extensões](#extensões)|
|[Gerenciador de senhas e de proteção](#gerenciador-de-senhas-e-de-proteção)|[Impressão](#impressão)|
|[Inicialização, página inicial e página nova guia](#inicialização-página-inicial-e-página-nova-guia)|[Mensagens nativas](#mensagens-nativas)|
|[Provedor de pesquisa padrão](#provedor-de-pesquisa-padrão)|[Servidor proxy](#servidor-proxy)|
|[Additional](#additional)|

### [*Autenticação HTTP*](#autenticação-http-policies)
|Nome da Política|Legenda|
|-|-|
|[AllowCrossOriginAuthPrompt](#allowcrossoriginauthprompt)|Permitir solicitações de Autenticação Básica HTTP entre origens|
|[AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)|Especifica uma lista de servidores aos quais o Microsoft Edge pode delegar credenciais de usuário|
|[AuthSchemes](#authschemes)|Esquemas de autenticação com suporte|
|[AuthServerAllowlist](#authserverallowlist)|Configurar lista de servidores de autenticação permitidos|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|Desabilitar pesquisa CNAME ao negociar a autenticação Kerberos|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|Incluir porta não padrão no SPN do Kerberos|
|[NtlmV2Enabled](#ntlmv2enabled)|Controlar se a autenticação NTLMv2 está habilitada|
### [*Cast*](#cast-policies)
|Nome da Política|Legenda|
|-|-|
|[EnableMediaRouter](#enablemediarouter)|Habilitar Google Cast|
|[ShowCastIconInToolbar](#showcasticonintoolbar)|Mostrar o ícone de transmissão na barra de ferramentas|
### [*Configurações de conteúdo*](#configurações-de-conteúdo-policies)
|Nome da Política|Legenda|
|-|-|
|[AutoSelectCertificateForUrls](#autoselectcertificateforurls)|Selecionar automaticamente os certificados de cliente para estes sites|
|[CookiesAllowedForUrls](#cookiesallowedforurls)|Permitir cookies em sites específicos|
|[CookiesBlockedForUrls](#cookiesblockedforurls)|Bloquear cookies em sites específicos|
|[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)|Limitar cookies de sites específicos para a sessão atual|
|[DefaultCookiesSetting](#defaultcookiessetting)|Configurar cookies|
|[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)|Controlar o uso da API do Sistema de Arquivos para leitura|
|[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)|Controlar o uso da API do Sistema de Arquivos para escrita|
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|Configuração de geolocalização padrão|
|[DefaultImagesSetting](#defaultimagessetting)|Configuração de imagens padrão|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|Controlar uso de exceções de conteúdo não seguro|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|Configuração de JavaScript padrão|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|Configuração de notificação padrão|
|[DefaultPluginsSetting](#defaultpluginssetting)|Configuração padrão do Adobe Flash|
|[DefaultPopupsSetting](#defaultpopupssetting)|Configuração de janela pop-up padrão|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|Controlar o uso da API Web Bluetooth|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|Controlar o uso da API WebUSB|
|[FileSystemReadAskForUrls](#filesystemreadaskforurls)|Permitir acesso de leitura através da API do Sistema de Arquivos nesses sites|
|[FileSystemReadBlockedForUrls](#filesystemreadblockedforurls)|Bloquear o acesso de leitura pela API do Sistema de Arquivos nestes sites|
|[FileSystemWriteAskForUrls](#filesystemwriteaskforurls)|Permitir o acesso de gravação a arquivos e diretórios nesses sites|
|[FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls)|Bloquear o acesso de gravação a arquivos e diretórios nesses sites|
|[ImagesAllowedForUrls](#imagesallowedforurls)|Permitir imagens nestes sites|
|[ImagesBlockedForUrls](#imagesblockedforurls)|Bloquear imagens em sites específicos|
|[InsecureContentAllowedForUrls](#insecurecontentallowedforurls)|Permitir conteúdo não seguro em sites especificados|
|[InsecureContentBlockedForUrls](#insecurecontentblockedforurls)|Bloquear conteúdo não seguro em sites especificados|
|[JavaScriptAllowedForUrls](#javascriptallowedforurls)|Permitir JavaScript em sites específicos|
|[JavaScriptBlockedForUrls](#javascriptblockedforurls)|Bloquear o JavaScript em sites específicos|
|[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)|Habilitar a configuração do comportamento de cookies SameSite herdado padrão|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist)|Reverter para o comportamento SameSite herdado de cookies em sites especificados|
|[NotificationsAllowedForUrls](#notificationsallowedforurls)|Permitir notificações em sites específicos|
|[NotificationsBlockedForUrls](#notificationsblockedforurls)|Bloquear notificações em sites específicos|
|[PluginsAllowedForUrls](#pluginsallowedforurls)|Permitir o plug-in do Adobe Flash em sites específicos|
|[PluginsBlockedForUrls](#pluginsblockedforurls)|Bloquear o plug-in do Adobe Flash em sites específicos|
|[PopupsAllowedForUrls](#popupsallowedforurls)|Permitir janelas pop-up em sites específicos|
|[PopupsBlockedForUrls](#popupsblockedforurls)|Bloquear janelas pop-up em sites específicos|
|[RegisteredProtocolHandlers](#registeredprotocolhandlers)|Registrar manipuladores de protocolo|
|[SpotlightExperiencesAndRecommendationsEnabled](#spotlightexperiencesandrecommendationsenabled)|Escolha se os usuários podem receber imagens de plano de fundo personalizadas e textos, sugestões, notificações
e dicas para serviços Microsoft|
|[WebUsbAllowDevicesForUrls](#webusballowdevicesforurls)|Conceder acesso a sites específicos para se conectar a dispositivos USB específicos|
|[WebUsbAskForUrls](#webusbaskforurls)|Permitir WebUSB em sites específicos|
|[WebUsbBlockedForUrls](#webusbblockedforurls)|Bloquear WebUSB em sites específicos|
### [*Configurações do Application Guard*](#configurações-do-application-guard-policies)
|Nome da Política|Legenda|
|-|-|
|[ApplicationGuardContainerProxy](#applicationguardcontainerproxy)|Proxy do Contêiner do Application Guard|
### [*Configurações do SmartScreen*](#configurações-do-smartscreen-policies)
|Nome da Política|Legenda|
|-|-|
|[PreventSmartScreenPromptOverride](#preventsmartscreenpromptoverride)|Impedir que avisos do Microsoft Defender SmartScreen sejam ignorados para sites|
|[PreventSmartScreenPromptOverrideForFiles](#preventsmartscreenpromptoverrideforfiles)|Impedir que os avisos do Microsoft Defender SmartScreen sobre downloads sejam ignorados|
|[SmartScreenAllowListDomains](#smartscreenallowlistdomains)|Configurar a lista de domínios para os quais o Microsoft Defender SmartScreen não disparará avisos|
|[SmartScreenEnabled](#smartscreenenabled)|Configurar o Microsoft Defender SmartScreen|
|[SmartScreenForTrustedDownloadsEnabled](#smartscreenfortrusteddownloadsenabled)|Forçar verificações do Microsoft Defender SmartScreen em downloads de fontes confiáveis|
|[SmartScreenPuaEnabled](#smartscreenpuaenabled)|Configurar o Microsoft Defender SmartScreen para bloquear aplicativos potencialmente indesejados|
### [*Extensões*](#extensões-policies)
|Nome da Política|Legenda|
|-|-|
|[ExtensionAllowedTypes](#extensionallowedtypes)|Configurar tipos de extensão permitidos|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|Permitir que extensões específicas sejam instaladas|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|Controlar quais extensões não podem ser instaladas|
|[ExtensionInstallForcelist](#extensioninstallforcelist)|Controlar quais extensões são instaladas silenciosamente|
|[ExtensionInstallSources](#extensioninstallsources)|Configurar fontes de instalação de script de usuário e extensão|
|[ExtensionSettings](#extensionsettings)|Definir configurações de gerenciamento de extensões|
### [*Gerenciador de senhas e de proteção*](#gerenciador-de-senhas-e-de-proteção-policies)
|Nome da Política|Legenda|
|-|-|
|[PasswordManagerEnabled](#passwordmanagerenabled)|Habilitar salvamento de senhas no gerenciador de senhas|
|[PasswordMonitorAllowed](#passwordmonitorallowed)|Permitir que os usuários sejam alertados se as senhas deles não forem seguras|
|[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)|Configurar a URL de alteração de senha|
|[PasswordProtectionLoginURLs](#passwordprotectionloginurls)|Configurar a lista de URLs de logon corporativos onde o serviço de proteção por senha deve capturar os salted hashes de uma senha|
|[PasswordProtectionWarningTrigger](#passwordprotectionwarningtrigger)|Configurar gatilho de aviso de proteção de senha|
### [*Impressão*](#impressão-policies)
|Nome da Política|Legenda|
|-|-|
|[DefaultPrinterSelection](#defaultprinterselection)|Regras de seleção de impressora padrão|
|[PrintHeaderFooter](#printheaderfooter)|Imprimir cabeçalhos e rodapés|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|Definir a impressora padrão do sistema como a impressora padrão|
|[PrintingEnabled](#printingenabled)|Habilitar impressão|
|[PrintingPaperSizeDefault](#printingpapersizedefault)|Tamanho da página de impressão padrão|
|[UseSystemPrintDialog](#usesystemprintdialog)|Imprimir usando a caixa de diálogo de impressão do sistema|
### [*Inicialização&comma; página inicial e página nova guia*](#inicialização-página-inicial-e-página-nova-guia-policies)
|Nome da Política|Legenda|
|-|-|
|[HomepageIsNewTabPage](#homepageisnewtabpage)|Definir a página nova guia como a home page|
|[HomepageLocation](#homepagelocation)|Configurar a URL da home page|
|[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)|Configurar os tipos de plano de fundo permitidos para o novo layout de página de guia|
|[NewTabPageCompanyLogo](#newtabpagecompanylogo)|Definir o logotipo da empresa da página Nova guia (obsoleto)|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|Ocultar os sites principais padrão da página de nova guia|
|[NewTabPageLocation](#newtabpagelocation)|Configurar a URL da página de nova guia|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|Definir links rápidos da página de nova guia|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|Habilitar o pré-carregamento da página de nova guia para renderização mais rápida|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|Configurar a experiência de página de nova guia do Microsoft Edge|
|[RestoreOnStartup](#restoreonstartup)|Ação a ser executada na inicialização|
|[RestoreOnStartupURLs](#restoreonstartupurls)|Sites a serem abertos quando o navegador for iniciado|
|[ShowHomeButton](#showhomebutton)|Mostrar botão Início na barra de ferramentas|
### [*Mensagens nativas*](#mensagens-nativas-policies)
|Nome da Política|Legenda|
|-|-|
|[NativeMessagingAllowlist](#nativemessagingallowlist)|Controlar quais hosts de mensagens nativas os usuários podem usar|
|[NativeMessagingBlocklist](#nativemessagingblocklist)|Configurar lista de contatos bloqueados de mensagens nativas|
|[NativeMessagingUserLevelHosts](#nativemessaginguserlevelhosts)|Permitir hosts de mensagens nativas no nível de usuário (instalado sem permissões de administrador)|
### [*Provedor de pesquisa padrão*](#provedor-de-pesquisa-padrão-policies)
|Nome da Política|Legenda|
|-|-|
|[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)|Habilitar o provedor de pesquisa padrão|
|[DefaultSearchProviderEncodings](#defaultsearchproviderencodings)|Codificações do provedor de pesquisa padrão|
|[DefaultSearchProviderImageURL](#defaultsearchproviderimageurl)|Especifica o recurso de pesquisa por imagem para o provedor de pesquisa padrão|
|[DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams)|Parâmetros para uma URL de imagem que usa POST|
|[DefaultSearchProviderKeyword](#defaultsearchproviderkeyword)|Palavra-chave do provedor de pesquisa padrão|
|[DefaultSearchProviderName](#defaultsearchprovidername)|Nome do provedor de pesquisa padrão|
|[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)|URL de pesquisa do provedor de pesquisa padrão|
|[DefaultSearchProviderSuggestURL](#defaultsearchprovidersuggesturl)|URL do provedor de pesquisa padrão para sugestões|
|[NewTabPageSearchBox](#newtabpagesearchbox)|Configurar a nova experiência de caixa de pesquisa da página da guia|
### [*Servidor proxy*](#servidor-proxy-policies)
|Nome da Política|Legenda|
|-|-|
|[ProxyBypassList](#proxybypasslist)|Configurar regras para ignorar o proxy|
|[ProxyMode](#proxymode)|Definir configurações de servidor proxy|
|[ProxyPacUrl](#proxypacurl)|Definir a URL do arquivo .pac do proxy|
|[ProxyServer](#proxyserver)|Configurar o endereço ou a URL do servidor proxy|
|[ProxySettings](#proxysettings)|Configurações de proxy|
### [*Additional*](#additional-policies)
|Nome da Política|Legenda|
|-|-|
|[AddressBarMicrosoftSearchInBingProviderEnabled](#addressbarmicrosoftsearchinbingproviderenabled)|Habilitar sugestões da Pesquisa da Microsoft no Bing na barra de endereços|
|[AdsSettingForIntrusiveAdsSites](#adssettingforintrusiveadssites)|Configuração de anúncios para sites com anúncios intrusivos|
|[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory)|Habilitar a exclusão do navegador e do histórico de download|
|[AllowFileSelectionDialogs](#allowfileselectiondialogs)|Permitir caixas de diálogo de seleção de arquivos|
|[AllowPopupsDuringPageUnload](#allowpopupsduringpageunload)|Permite que uma página mostre pop-ups durante seu descarregamento|
|[AllowSurfGame](#allowsurfgame)|Permitir jogo de surfe|
|[AllowSyncXHRInPageDismissal](#allowsyncxhrinpagedismissal)|Permitir que as páginas enviem solicitações XHR síncronas durante o descarte de páginas (preterida)|
|[AllowTokenBindingForUrls](#allowtokenbindingforurls)|Configurar a lista de sites que o Microsoft Edge tentará estabelecer uma ligação de token com|
|[AllowTrackingForUrls](#allowtrackingforurls)|Configurar exceções de prevenção de rastreamento para sites específicos|
|[AlternateErrorPagesEnabled](#alternateerrorpagesenabled)|Sugerir páginas similares quando uma página da Web não for encontrada|
|[AlwaysOpenPdfExternally](#alwaysopenpdfexternally)|Sempre abrir arquivos PDF externamente|
|[AmbientAuthenticationInPrivateModesEnabled](#ambientauthenticationinprivatemodesenabled)|Habilitar a autenticação de ambiente para perfis InPrivate e Convidado|
|[AppCacheForceEnabled](#appcacheforceenabled)|Permite que o recurso AppCache seja reativado mesmo se estiver desativado por padrão|
|[ApplicationLocaleValue](#applicationlocalevalue)|Definir localidade do aplicativo|
|[AudioCaptureAllowed](#audiocaptureallowed)|Permitir ou bloquear captura de áudio|
|[AudioCaptureAllowedUrls](#audiocaptureallowedurls)|Sites podem acessar dispositivos de captura áudio sem solicitar permissão|
|[AudioSandboxEnabled](#audiosandboxenabled)|Permitir execução da área restrita de áudio|
|[AutoImportAtFirstRun](#autoimportatfirstrun)|Importar automaticamente os dados e as configurações de outro navegador na primeira execução|
|[AutoLaunchProtocolsFromOrigins](#autolaunchprotocolsfromorigins)|Define uma lista de protocolos que podem iniciar um aplicativo externo de origens listadas sem avisar ao usuário|
|[AutoOpenAllowedForURLs](#autoopenallowedforurls)|URLs em que AutoOpenFileTypes pode aplicar|
|[AutoOpenFileTypes](#autoopenfiletypes)|Lista dos tipos de arquivo que devem ser abertos automaticamente ao baixar|
|[AutofillAddressEnabled](#autofilladdressenabled)|Habilitar AutoPreenchimento para endereços|
|[AutofillCreditCardEnabled](#autofillcreditcardenabled)|Habilitar AutoPreenchimento para cartões de crédito|
|[AutoplayAllowed](#autoplayallowed)|Permitir reprodução automática de mídia para sites|
|[BackgroundModeEnabled](#backgroundmodeenabled)|Continuar executando apps em segundo plano depois que o Microsoft Edge for fechado|
|[BackgroundTemplateListUpdatesEnabled](#backgroundtemplatelistupdatesenabled)|Habilita atualizações em segundo plano na lista de modelos disponíveis para Coleções e outros recursos que usam modelos|
|[BingAdsSuppression](#bingadssuppression)|Bloquear todos os anúncios nos resultados de pesquisa do Bing|
|[BlockThirdPartyCookies](#blockthirdpartycookies)|Bloquear cookies de terceiros|
|[BrowserAddProfileEnabled](#browseraddprofileenabled)|Habilitar a criação de perfil no menu do submenu Identidade ou na página Configurações|
|[BrowserGuestModeEnabled](#browserguestmodeenabled)|Habilitar modo convidado|
|[BrowserNetworkTimeQueriesEnabled](#browsernetworktimequeriesenabled)|Permitir consultas a um serviço de Hora da Rede do Navegador|
|[BrowserSignin](#browsersignin)|Configurações de entrada do navegador|
|[BuiltInDnsClientEnabled](#builtindnsclientenabled)|Usar o cliente DNS interno|
|[BuiltinCertificateVerifierEnabled](#builtincertificateverifierenabled)|Determina se o verificador de certificado interno será usado para verificar os certificados do servidor (preterida)|
|[CertificateTransparencyEnforcementDisabledForCas](#certificatetransparencyenforcementdisabledforcas)|Desabilitar a imposição de Transparência de Certificado para uma lista de hashes de subjectPublicKeyInfo|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](#certificatetransparencyenforcementdisabledforlegacycas)|Desabilitar a imposição de Transparência de Certificado para uma lista de autoridades de certificação herdadas|
|[CertificateTransparencyEnforcementDisabledForUrls](#certificatetransparencyenforcementdisabledforurls)|Desabilitar a imposição de Transparência de Certificado para URLs específicas|
|[ClearBrowsingDataOnExit](#clearbrowsingdataonexit)|Limpar dados de navegação quando o Microsoft Edge for fechado|
|[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)|Limpar arquivos e imagens armazenados em cache quando Microsoft Edge for fechado|
|[CollectionsServicesAndExportsBlockList](#collectionsservicesandexportsblocklist)|Bloquear o acesso a uma lista especificada de serviços e exportar destinos em Coleções|
|[CommandLineFlagSecurityWarningsEnabled](#commandlineflagsecuritywarningsenabled)|Habilitar avisos de segurança para sinalizadores de linha de comando|
|[ComponentUpdatesEnabled](#componentupdatesenabled)|Habilitar atualizações de componentes no Microsoft Edge|
|[ConfigureDoNotTrack](#configuredonottrack)|Configurar Não Rastrear|
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|Configurar a entrada automática com uma conta de domínio do Active Directory quando não houver nenhuma conta de domínio do Azure AD|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|Configurar a conversão de texto em fala online|
|[ConfigureShare](#configureshare)|Configurar a Experiência de compartilhamento|
|[CustomHelpLink](#customhelplink)|Especificar link de ajuda personalizado|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|Verificações de interceptação de DNS habilitadas|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|Definir Microsoft Edge como navegador padrão|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|Permitir acesso de pesquisa do menu de contexto do provedor de pesquisa padrão|
|[DefaultSensorsSetting](#defaultsensorssetting)|Configuração de sensores padrão|
|[DefaultSerialGuardSetting](#defaultserialguardsetting)|Controlar o uso da API serial|
|[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)|Exigir que a Lista de Sites do Modo Empresarial esteja disponível antes da navegação na guia|
|[DeleteDataOnMigration](#deletedataonmigration)|Excluir dados antigos do navegador na migração|
|[DeveloperToolsAvailability](#developertoolsavailability)|Controlar onde as ferramentas de desenvolvedor podem ser usadas|
|[DiagnosticData](#diagnosticdata)|Enviar dados de diagnóstico necessários e opcionais sobre o uso do navegador|
|[DirectInvokeEnabled](#directinvokeenabled)|Permitir que os usuários abram arquivos usando o protocolo DirectInvoke|
|[Disable3DAPIs](#disable3dapis)|Desabilitar o suporte para APIs de gráficos 3D|
|[DisableScreenshots](#disablescreenshots)|Desabilitar as capturas de tela|
|[DiskCacheDir](#diskcachedir)|Definir diretório de cache de disco|
|[DiskCacheSize](#diskcachesize)|Definir o tamanho do cache de disco, em bytes|
|[DnsOverHttpsMode](#dnsoverhttpsmode)|Controle o modo DNS-over-HTTPS|
|[DnsOverHttpsTemplates](#dnsoverhttpstemplates)|Especificar modelo de URI do resolvedor DNS-over-HTTPS desejado|
|[DownloadDirectory](#downloaddirectory)|Definir diretório de download|
|[DownloadRestrictions](#downloadrestrictions)|Permitir restrições de download|
|[EdgeCollectionsEnabled](#edgecollectionsenabled)|Habilitar o recurso Coleções|
|[EditFavoritesEnabled](#editfavoritesenabled)|Permite que os usuários editem os favoritos|
|[EnableDeprecatedWebPlatformFeatures](#enabledeprecatedwebplatformfeatures)|Reabilitar os recursos preteridos da plataforma da Web por um tempo limitado|
|[EnableDomainActionsDownload](#enabledomainactionsdownload)|Habilitar o download de ações de domínio da Microsoft (obsoleto)|
|[EnableOnlineRevocationChecks](#enableonlinerevocationchecks)|Habilitar verificações de OCSP/CRL online|
|[EnableSha1ForLocalAnchors](#enablesha1forlocalanchors)|Permitir certificados assinados usando o SHA-1 quando emitidos por âncoras de confiança locais (preterida)|
|[EnterpriseHardwarePlatformAPIEnabled](#enterprisehardwareplatformapienabled)|Permitir que extensões gerenciadas usem a API da Plataforma de Hardware Corporativo|
|[EnterpriseModeSiteListManagerAllowed](#enterprisemodesitelistmanagerallowed)|Permitir o acesso à ferramenta Enterprise Mode Site List Manager|
|[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](#exemptdomainfiletypepairsfromfiletypedownloadwarnings)|Desabilitar o download de avisos baseados em extensão de tipo de arquivo para tipos de arquivo especificados em domínios|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|Controlar a comunicação com o Serviço de Configuração e Experimentação|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox)|Mostrar uma caixa de seleção "Sempre abrir" na caixa de diálogo de protocolo externo|
|[FamilySafetySettingsEnabled](#familysafetysettingsenabled)|Permitir que os usuários configurem o Family Safety|
|[FavoritesBarEnabled](#favoritesbarenabled)|Habilitar barra de favoritos|
|[ForceBingSafeSearch](#forcebingsafesearch)|Aplicar a Pesquisa Segura do Bing|
|[ForceCertificatePromptsOnMultipleMatches](#forcecertificatepromptsonmultiplematches)|Configure se o Microsoft Edge deve selecionar um certificado automaticamente quando houver várias correspondências de certificado para um site configurado com "AutoSelectCertificateForUrls"|
|[ForceEphemeralProfiles](#forceephemeralprofiles)|Habilitar o uso de perfis efêmeros|
|[ForceGoogleSafeSearch](#forcegooglesafesearch)|Forçar a Pesquisa Segura do Google|
|[ForceLegacyDefaultReferrerPolicy](#forcelegacydefaultreferrerpolicy)|Use a política referencial padrão de no-referrer-when-downgrade. (preterida)|
|[ForceNetworkInProcess](#forcenetworkinprocess)|Aplicar o código de rede a ser executado no processo do navegador (obsoleto)|
|[ForceSync](#forcesync)|Forçar a sincronização dos dados do navegador e não mostrar a solicitação de consentimento da sincronização|
|[ForceYouTubeRestrict](#forceyoutuberestrict)|Aplicar o modo restrito mínimo do YouTube|
|[FullscreenAllowed](#fullscreenallowed)|Permitir modo de tela inteira|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|Habilitar cache de autenticação HTTP com escopo global|
|[GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar)|Forçar a navegação direta em site da intranet, em vez de pesquisar em entradas de palavras únicas na Barra de Endereços|
|[HSTSPolicyBypassList](#hstspolicybypasslist)|Configurar a lista de nomes que ignorarão a verificação de política HSTS|
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|Usar aceleração de hardware quando disponível|
|[HideFirstRunExperience](#hidefirstrunexperience)|Ocultar a Experiência de primeira execução e a tela inicial|
|[ImportAutofillFormData](#importautofillformdata)|Permitir importação de dados de formulário de autopreenchimento|
|[ImportBrowserSettings](#importbrowsersettings)|Permitir a importação das configurações do navegador|
|[ImportCookies](#importcookies)|Permitir importação de Cookies|
|[ImportExtensions](#importextensions)|Permitir importação de extensões|
|[ImportFavorites](#importfavorites)|Permitir importação de favoritos|
|[ImportHistory](#importhistory)|Permitir a importação do histórico de navegação|
|[ImportHomepage](#importhomepage)|Permitir a importação das configurações da home page|
|[ImportOpenTabs](#importopentabs)|Permitir importação de guias abertas|
|[ImportPaymentInfo](#importpaymentinfo)|Permitir importação de informações de pagamento|
|[ImportSavedPasswords](#importsavedpasswords)|Permitir a importação de senhas salvas|
|[ImportSearchEngine](#importsearchengine)|Permitir importação das configurações do mecanismo de pesquisa|
|[ImportShortcuts](#importshortcuts)|Permitir importação de atalhos|
|[InPrivateModeAvailability](#inprivatemodeavailability)|Configurar a disponibilidade do modo InPrivate|
|[InsecureFormsWarningsEnabled](#insecureformswarningsenabled)|Habilitar avisos para formulários não seguros|
|[IntensiveWakeUpThrottlingEnabled](#intensivewakeupthrottlingenabled)|Controlar o recurso de IntensiveWakeUpThrottling|
|[InternetExplorerIntegrationEnhancedHangDetection](#internetexplorerintegrationenhancedhangdetection)|Configurar detecção de travamento aprimorada no modo Internet Explorer|
|[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)|Configurar a integração com o Internet Explorer|
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|Configurar a Lista de Sites do Modo Empresarial|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|Especificar como as navegações "em página" para sites não configurados se comportam ao iniciar em páginas do modo do Internet Explorer|
|[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed)|Permitir o teste do modo Internet Explorer|
|[IsolateOrigins](#isolateorigins)|Habilitar isolamento de site para origens específicas|
|[LocalProvidersEnabled](#localprovidersenabled)|Permitir sugestões de fornecedores locais|
|[ManagedFavorites](#managedfavorites)|Configurar favoritos|
|[ManagedSearchEngines](#managedsearchengines)|Gerenciar Mecanismos de Pesquisa|
|[MaxConnectionsPerProxy](#maxconnectionsperproxy)|Número máximo de conexões simultâneas com o servidor proxy|
|[MediaRouterCastAllowAllIPs](#mediaroutercastallowallips)|Permitir que o Google Cast se conecte a dispositivos Cast em todos os endereços IP|
|[MetricsReportingEnabled](#metricsreportingenabled)|Habilitar relatórios de dados relacionados a uso e falhas (preterida)|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|Habilitar Oclusão de Janela Nativa|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|Definir um tempo limite para o atraso da navegação de guia para a Lista de Sites do Modo Empresarial|
|[NetworkPredictionOptions](#networkpredictionoptions)|Habilitar previsão de rede|
|[NonRemovableProfileEnabled](#nonremovableprofileenabled)|Configurar se um usuário sempre tem um perfil padrão conectado automaticamente à sua conta corporativa ou de estudante|
|[OverrideSecurityRestrictionsOnInsecureOrigin](#overridesecurityrestrictionsoninsecureorigin)|Controlar onde se aplicam a restrições de segurança em origens não seguras|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|Permitir que sites consultem os métodos de pagamento disponíveis|
|[PersonalizationReportingEnabled](#personalizationreportingenabled)|Permitir personalização de anúncios, pesquisa e notícias enviando histórico de navegação à Microsoft|
|[PinningWizardAllowed](#pinningwizardallowed)|Permitir o Assistente para fixar na barra de tarefas|
|[ProactiveAuthEnabled](#proactiveauthenabled)|Habilitar a Autenticação Proativa|
|[PromotionalTabsEnabled](#promotionaltabsenabled)|Habilitar conteúdo promocional em toda a guia|
|[PromptForDownloadLocation](#promptfordownloadlocation)|Perguntar onde salvar os arquivos baixados|
|[QuicAllowed](#quicallowed)|Permitir o protocolo QUIC|
|[RelaunchNotification](#relaunchnotification)|Notificar um usuário de que uma reinicialização do navegador é recomendada ou necessária para atualizações pendentes|
|[RelaunchNotificationPeriod](#relaunchnotificationperiod)|Definir o período para notificações de atualização|
|[RendererCodeIntegrityEnabled](#renderercodeintegrityenabled)|Habilitar integridade do código do renderizador|
|[RequireOnlineRevocationChecksForLocalAnchors](#requireonlinerevocationchecksforlocalanchors)|Especificar se as verificações OCSP/CRL online são necessárias para âncoras de confiança locais|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|Habilitar a resolução de erros de navegação usando um serviço Web|
|[RestrictSigninToPattern](#restrictsignintopattern)|Restringir quais contas podem ser usadas como contas principais do Microsoft Edge|
|[RoamingProfileLocation](#roamingprofilelocation)|Definir o diretório de perfil de roaming|
|[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)|Habilitar o uso de cópias móveis para dados de perfil do Microsoft Edge|
|[RunAllFlashInAllowMode](#runallflashinallowmode)|Estender a configuração do conteúdo em Adobe Flash a todo o conteúdo|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|Permitir que os usuários continuem a partir da página de aviso HTTPS|
|[SSLVersionMin](#sslversionmin)|Versão mínima do TLS habilitada|
|[SaveCookiesOnExit](#savecookiesonexit)|Salvar cookies quando o Microsoft Edge fechar|
|[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)|Desabilitar o salvamento do histórico do navegador|
|[ScreenCaptureAllowed](#screencaptureallowed)|Permitir ou negar captura de tela|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|Ativar rolagem para textos especificados nos fragmentos da URL|
|[SearchSuggestEnabled](#searchsuggestenabled)|Habilitar sugestões de pesquisa|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|Sites ou domínios que não precisam de permissão para usar o atestado de Chave de Segurança direto|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|Enviar todos os sites da intranet para o Internet Explorer|
|[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)|Enviar informações do site para melhorar os serviços Microsoft (preterida)|
|[SensorsAllowedForUrls](#sensorsallowedforurls)|Permitir o acesso a sensores em sites específicos|
|[SensorsBlockedForUrls](#sensorsblockedforurls)|Bloquear o acesso a sensores em sites específicos|
|[SerialAskForUrls](#serialaskforurls)|Permitir a API serial em sites específicos|
|[SerialBlockedForUrls](#serialblockedforurls)|Bloquear a API serial em sites específicos|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|Mostrar o atalho do Microsoft Office na barra Favoritos|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|Habilitar o suporte para o Signed HTTP Exchange (SXG)|
|[SitePerProcess](#siteperprocess)|Habilitar isolamento de sites para todos os sites|
|[SpellcheckEnabled](#spellcheckenabled)|Habilitar verificação ortográfica|
|[SpellcheckLanguage](#spellchecklanguage)|Habilitar idiomas específicos da verificação ortográfica|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|Aplicar a desabilitação de verificação ortográfica dos idiomas|
|[StricterMixedContentTreatmentEnabled](#strictermixedcontenttreatmentenabled)|Habilitar tratamento mais rígido para conteúdo misto (preterida)|
|[SuppressUnsupportedOSWarning](#suppressunsupportedoswarning)|Suprimir o aviso do sistema operacional sem suporte|
|[SyncDisabled](#syncdisabled)|Desabilitar sincronização de dados usando os serviços de sincronização da Microsoft|
|[SyncTypesListDisabled](#synctypeslistdisabled)|Configure a lista de tipos excluídos da sincronização|
|[TLS13HardeningForLocalAnchorsEnabled](#tls13hardeningforlocalanchorsenabled)|Habilitar um recurso de segurança TLS 1.3 para âncoras de confiança locais. (obsoleto)|
|[TLSCipherSuiteDenyList](#tlsciphersuitedenylist)|Especificar os pacotes de cifra TLS para desabilitar|
|[TabFreezingEnabled](#tabfreezingenabled)|Permitir congelamento de guias em segundo plano|
|[TaskManagerEndProcessEnabled](#taskmanagerendprocessenabled)|Habilitar processos finais no gerenciador de tarefas do navegador|
|[TotalMemoryLimitMb](#totalmemorylimitmb)|Defina o limite em megabytes de memória que uma única instância do Microsoft Edge pode usar.|
|[TrackingPrevention](#trackingprevention)|Bloquear o rastreamento de atividades de navegação da Web dos usuários|
|[TranslateEnabled](#translateenabled)|Habilitar Traduzir|
|[URLAllowlist](#urlallowlist)|Definir uma lista de URLs permitidas|
|[URLBlocklist](#urlblocklist)|Bloquear o acesso a uma lista de URLs|
|[UserAgentClientHintsEnabled](#useragentclienthintsenabled)|Habilitar o recurso dicas de cliente Usuário-Agente (preterida)|
|[UserDataDir](#userdatadir)|Definir o diretório de dados do usuário|
|[UserDataSnapshotRetentionLimit](#userdatasnapshotretentionlimit)|Limita o número de instantâneos de dados do usuário retidos para uso em caso de reversão de emergência.|
|[UserFeedbackAllowed](#userfeedbackallowed)|Permitir comentários do usuário|
|[VideoCaptureAllowed](#videocaptureallowed)|Permitir ou bloquear captura de vídeo|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|Sites que podem acessar dispositivos de captura de vídeo sem solicitar permissão|
|[WPADQuickCheckEnabled](#wpadquickcheckenabled)|Definir otimização de WPAD|
|[WebAppInstallForceList](#webappinstallforcelist)|Configurar lista de Aplicativos Web instalados à força|
|[WebComponentsV0Enabled](#webcomponentsv0enabled)|Reabilitar a API do Web Components v0 até M84 (obsoleto)|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|Permitir que o WebDriver substitua políticas incompatíveis (obsoleto)|
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|Gerenciar a exposição de endereços IP locais pelo WebRTC|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|Restringir a exposição do endereço IP local pelo WebRTC|
|[WebRtcUdpPortRange](#webrtcudpportrange)|Restringir o intervalo de portas UDP locais usadas pelo WebRTC|
|[WinHttpProxyResolverEnabled](#winhttpproxyresolverenabled)|Use o resolvedor de proxy do Windows (preterida)|




  ## Autenticação HTTP policies

  [Voltar ao início](#microsoft-edge---políticas)

  ### AllowCrossOriginAuthPrompt
  #### Permitir solicitações de Autenticação Básica HTTP entre origens
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Controla se o subconteúdo de terceiros em uma página pode abrir uma caixa de diálogo de Autenticação Básica HTTP.

Normalmente, isso é desabilitado como uma defesa contra phishing. Se você não configurar esta política, ela será desabilitada e o subconteúdo de terceiros não poderá abrir uma caixa de diálogo de Autenticação Básica HTTP.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AllowCrossOriginAuthPrompt
  - Nome da GP: Permitir solicitações de Autenticação Básica HTTP entre origens
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Autenticação HTTP
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AllowCrossOriginAuthPrompt
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AllowCrossOriginAuthPrompt
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AuthNegotiateDelegateAllowlist
  #### Especifica uma lista de servidores aos quais o Microsoft Edge pode delegar credenciais de usuário
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Configura a lista de servidores que o Microsoft Edge pode delegar.

Separe vários nomes de servidor com vírgulas. Caracteres curinga (*) são permitidos.

Se você não configurar essa política, o Microsoft Edge não delegará credenciais de usuário, mesmo que um servidor seja detectado como Intranet.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AuthNegotiateDelegateAllowlist
  - Nome da GP: Especifica uma lista de servidores aos quais o Microsoft Edge pode delegar credenciais de usuário
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Autenticação HTTP
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AuthNegotiateDelegateAllowlist
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"contoso.com"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AuthNegotiateDelegateAllowlist
  - Exemplo de valor:
``` xml
<string>contoso.com</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AuthSchemes
  #### Esquemas de autenticação com suporte
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica os esquemas de autenticação HTTP que têm suporte.

Você pode configurar a política usando os valores: 'basic', 'digest', 'ntlm' e 'negotiate'. Separe vários valores por vírgulas.

Se você não configurar essa política, todos os quatro esquemas serão usados.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AuthSchemes
  - Nome da GP: Esquemas de autenticação com suporte
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Autenticação HTTP
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AuthSchemes
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"basic,digest,ntlm,negotiate"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AuthSchemes
  - Exemplo de valor:
``` xml
<string>basic,digest,ntlm,negotiate</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AuthServerAllowlist
  #### Configurar lista de servidores de autenticação permitidos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica quais servidores devem ser habilitados para a autenticação integrada. A autenticação integrada só é habilitada quando o Microsoft Edge recebe um desafio de autenticação de um proxy ou servidor na lista.

Separe vários nomes de servidor com vírgulas. São permitidos curingas (*).

Se você não configurar essa política, o Microsoft Edge tentará detectar se um servidor está na intranet. Somente depois disso, ele responderá às solicitações IWA. Se o servidor estiver na internet, as solicitações IWA provenientes dele serão ignoradas pelo Microsoft Edge.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AuthServerAllowlist
  - Nome da GP: Configurar lista de servidores de autenticação permitidos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Autenticação HTTP
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AuthServerAllowlist
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"*contoso.com,contoso.com"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AuthServerAllowlist
  - Exemplo de valor:
``` xml
<string>*contoso.com,contoso.com</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DisableAuthNegotiateCnameLookup
  #### Desabilitar pesquisa CNAME ao negociar a autenticação Kerberos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Determina se o SPN do Kerberos gerado é baseado no nome DNS canônico (CNAME) ou no nome original inserido.

Se você habilitar essa política, a pesquisa CNAME será ignorada e o nome do servidor será usado (conforme inserido).

Se você desabilitar essa política ou não a configurar, o nome canônico do servidor será usado. Isso é determinado via pesquisa CNAME.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DisableAuthNegotiateCnameLookup
  - Nome da GP: Desabilitar pesquisa CNAME ao negociar a autenticação Kerberos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Autenticação HTTP
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DisableAuthNegotiateCnameLookup
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DisableAuthNegotiateCnameLookup
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### EnableAuthNegotiatePort
  #### Incluir porta não padrão no SPN do Kerberos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica se o SPN do Kerberos gerado deve incluir uma porta não padrão.

Se essa política for habilitada e um usuário inclui uma porta não padrão (uma porta diferente de 80 ou 443) em uma URL, essa porta será incluída no SPN do Kerberos gerado.

Se você não configurar ou desabilitar essa política, o SPN do Kerberos gerado não incluirá uma porta em nenhum caso.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: EnableAuthNegotiatePort
  - Nome da GP: Incluir porta não padrão no SPN do Kerberos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Autenticação HTTP
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: EnableAuthNegotiatePort
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: EnableAuthNegotiatePort
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### NtlmV2Enabled
  #### Controlar se a autenticação NTLMv2 está habilitada
  
  
  #### Versões com suporte:
  - No macOS desde a versão 77 ou posterior

  #### Descrição
  Controla se o NTLMv2 está habilitado.

Todas as versões recentes dos servidores Samba e Windows oferecem suporte a NTLMv2. Você só deve desabilitar o NTLMv2 para resolver problemas de compatibilidade com versões anteriores, já que ele reduz a segurança da autenticação.

Se você não configurar esta política, o NTLMv2 estará habilitado por padrão.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  

  #### Informações e configurações do Mac
  - Nome da chave de preferência: NtlmV2Enabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ## Cast policies

  [Voltar ao início](#microsoft-edge---políticas)

  ### EnableMediaRouter
  #### Habilitar Google Cast
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Habilite essa política para habilitar o Google Cast. Os usuários poderão iniciá-lo por meio do menu do app, dos menus de contexto das páginas, dos controles de mídia em sites habilitados para o Cast e (se exibido) do ícone da barra de ferramentas do Cast.

Desabilite essa política para desativar o Google Cast.

Por padrão, o Google Cast é habilitado.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: EnableMediaRouter
  - Nome da GP: Habilitar Google Cast
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Cast
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: EnableMediaRouter
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: EnableMediaRouter
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ShowCastIconInToolbar
  #### Mostrar o ícone de transmissão na barra de ferramentas
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Defina essa política como true para mostrar o ícone da barra de ferramentas Transmitir na barra de ferramentas ou no Menu Estouro. Os usuários não poderão removê-lo.

Se você não definir essa política ou desativá-la, os usuários poderão fixar ou remover o ícone usando o menu contextual.

Se você definir também a política [EnableMediaRouter](#enablemediarouter) como false, essa política será ignorada e o ícone da barra de ferramentas não será mostrado.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ShowCastIconInToolbar
  - Nome da GP: Mostrar o ícone de transmissão na barra de ferramentas
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Cast
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ShowCastIconInToolbar
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ShowCastIconInToolbar
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ## Configurações de conteúdo policies

  [Voltar ao início](#microsoft-edge---políticas)

  ### AutoSelectCertificateForUrls
  #### Selecionar automaticamente os certificados de cliente para estes sites
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica uma lista de sites, com base nos padrões de URL, para os quais o Microsoft Edge deve selecionar automaticamente um certificado de cliente, se o site solicitar um.

O valor deve ser uma matriz de dicionários JSON de cadeias de caracteres. A forma de cada dicionário é { "pattern": "$URL_PATTERN", "filter" : $FILTER }, onde $URL_PATTERN é um padrão de configuração de conteúdo. $FILTER restringe os certificados de cliente que o navegador selecionará automaticamente. Independentemente do filtro, somente os certificados que correspondem à solicitação de certificado do servidor serão selecionados. Por exemplo, se $FILTER tiver a forma { "ISSUER": { "CN": "$ISSUER_CN" } }, serão selecionados apenas certificados de cliente emitidos por um certificado com o CommonName $ISSUER_CN. Se $FILTER contiver "ISSUER" e uma seção "SUBJECT", um certificado de cliente deverá atender às duas condições para ser selecionado. Se $FILTER especificar uma organização ("O"), um certificado deverá ter pelo menos uma organização que corresponda ao valor especificado para ser selecionado. Se $FILTER especificar uma unidade organizacional ("UO"), um certificado deverá ter pelo menos uma unidade organizacional que corresponda ao valor especificado para ser selecionado. Se $FILTER for um dicionário vazio {}, a seleção de certificados de cliente não será restrita.

Se você não configurar essa política, a seleção automática não será feita para os sites.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AutoSelectCertificateForUrls
  - Nome da GP: Selecionar automaticamente os certificados de cliente para estes sites
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls\1 = "{\"pattern\":\"https://www.contoso.com\",\"filter\":{\"ISSUER\":{\"CN\":\"certificate issuer name\", \"L\": \"certificate issuer location\", \"O\": \"certificate issuer org\", \"OU\": \"certificate issuer org unit\"}, \"SUBJECT\":{\"CN\":\"certificate subject name\", \"L\": \"certificate subject location\", \"O\": \"certificate subject org\", \"OU\": \"certificate subject org unit\"}}}"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AutoSelectCertificateForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>{"pattern":"https://www.contoso.com","filter":{"ISSUER":{"CN":"certificate issuer name", "L": "certificate issuer location", "O": "certificate issuer org", "OU": "certificate issuer org unit"}, "SUBJECT":{"CN":"certificate subject name", "L": "certificate subject location", "O": "certificate subject org", "OU": "certificate subject org unit"}}}</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### CookiesAllowedForUrls
  #### Permitir cookies em sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define uma lista de sites, com base em padrões de URL, que não podem definir cookies.

Se você não configurar esta política, será usado o valor padrão global da política [DefaultCookiesSetting](#defaultcookiessetting) (se definida) ou a configuração pessoal do usuário para todos os sites.

Confira as políticas [CookiesBlockedForUrls](#cookiesblockedforurls) e [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) para obter mais informações.

Observe que não pode haver padrões de URL em conflito definidos entre estas três políticas:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- CookiesAllowedForUrls

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

Para impedir a exclusão de cookies ao sair, configure a política [SaveCookiesOnExit](#savecookiesonexit).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: CookiesAllowedForUrls
  - Nome da GP: Permitir cookies em sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: CookiesAllowedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### CookiesBlockedForUrls
  #### Bloquear cookies em sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define uma lista de sites, com base em padrões de URL, que não podem definir cookies.

Se você não configurar esta política, será usado o valor padrão global da política [DefaultCookiesSetting](#defaultcookiessetting) (se definida) ou a configuração pessoal do usuário para todos os sites.

Consulte as políticas [CookiesAllowedForUrls](#cookiesallowedforurls) e [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) para obter mais informações.

Observe que não pode haver padrões de URL em conflito definidos entre estas três políticas:

- CookiesBlockedForUrls

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: CookiesBlockedForUrls
  - Nome da GP: Bloquear cookies em sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: CookiesBlockedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### CookiesSessionOnlyForUrls
  #### Limitar cookies de sites específicos para a sessão atual
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Os cookies criados por sites que correspondam a um padrão de URL que você definir serão excluídos quando a sessão for encerrada (quando a janela for fechada).

Os cookies criados por sites que não correspondam ao padrão serão controlados pela política [DefaultCookiesSetting](#defaultcookiessetting) (se definida) ou pela configuração pessoal do usuário. Esse também será o comportamento padrão se você não configurar esta política.

Se o Microsoft Edge estiver em execução em segundo plano, a sessão talvez não seja encerrada quando a última janela for fechada, o que significa que os cookies não serão limpos quando a janela for fechada. Consulte a política [BackgroundModeEnabled](#backgroundmodeenabled) para obter informações sobre como configurar o que acontece quando o Microsoft Edge é executado em segundo plano.

Você também pode usar as políticas [CookiesAllowedForUrls](#cookiesallowedforurls) e [CookiesBlockedForUrls](#cookiesblockedforurls) para controlar os sites que podem criar cookies.

Observe que não pode haver padrões de URL em conflito definidos entre estas três políticas:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- CookiesSessionOnlyForUrls

Se você definir a política [RestoreOnStartup](#restoreonstartup) para restaurar URLs de sessões anteriores, esta política será ignorada e os cookies serão armazenados permanentemente para esses sites.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: CookiesSessionOnlyForUrls
  - Nome da GP: Limitar cookies de sites específicos para a sessão atual
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: CookiesSessionOnlyForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultCookiesSetting
  #### Configurar cookies
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Controla se os sites podem criar cookies no dispositivo do usuário. Esta política é tudo ou nada: você pode permitir que todos os sites criem cookies ou que nenhum site crie cookies. Você não pode usar esta política para habilitar cookies de sites específicos.

Defina a política como "SessionOnly" para limpar cookies quando a sessão for encerrada. Se o Microsoft Edge estiver sendo executado em segundo plano, a sessão talvez não seja encerrada quando a última janela for fechada, o que significa que os cookies não serão limpos quando a janela for fechada. Consulte a política [BackgroundModeEnabled](#backgroundmodeenabled) para obter informações sobre como configurar o que acontece quando o Microsoft Edge é executado em segundo plano.

Se você não configurar esta política, será usado o padrão "AllowCookies", e os usuários poderão alterar isso nas Configurações do Microsoft Edge. (Se você não quiser que os usuários possam alterar essa configuração, defina a política.)

Mapeamento das opções da política:

* AllowCookies (1) = Permitir que todos os sites criem cookies

* BlockCookies (2) = Não deixe nenhum site criar cookies

* SessionOnly (4) = Mantenha os cookies durante a sessão, exceto os listados em [SaveCookiesOnExit](#savecookiesonexit)

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultCookiesSetting
  - Nome da GP: Configurar cookies
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DefaultCookiesSetting
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultCookiesSetting
  - Exemplo de valor:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultFileSystemReadGuardSetting
  #### Controlar o uso da API do Sistema de Arquivos para leitura
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Se você definir essa política como 3, os sites poderão solicitar acesso de leitura ao sistema de arquivos do sistema operacional do host usando a API do sistema de arquivos. Se você definir esta política como 2, o acesso será negado.

Se você não definir essa política, os sites poderão pedir acesso. Os usuários podem alterar essa configuração.

Mapeamento das opções da política:

* BlockFileSystemRead (2) = Não permitir que nenhum site solicite o acesso de leitura a arquivos e diretórios por meio da API do Sistema de Arquivos

* AskFileSystemRead (3) = Permitir que os sites peçam ao usuário para conceder acesso de leitura a arquivos e diretórios por meio da API do Sistema de Arquivos

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultFileSystemReadGuardSetting
  - Nome da GP: Controlar o uso da API do Sistema de Arquivos para leitura
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DefaultFileSystemReadGuardSetting
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultFileSystemReadGuardSetting
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultFileSystemWriteGuardSetting
  #### Controlar o uso da API do Sistema de Arquivos para escrita
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Se você definir essa política como 3, os sites poderão solicitar acesso de leitura ao sistema de arquivos do sistema operacional do host usando a API do sistema de arquivos. Se você definir esta política como 2, o acesso será negado.

Se você não definir essa política, os sites poderão pedir acesso. Os usuários podem alterar essa configuração.

Mapeamento das opções da política:

* BlockFileSystemWrite (2) = Não permitir que nenhum site solicite o acesso de gravação a arquivos e diretórios

* AskFileSystemWrite (3) = Permitir que os sites peçam ao usuário para conceder acesso de gravação a arquivos e diretórios

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultFileSystemWriteGuardSetting
  - Nome da GP: Controlar o uso da API do Sistema de Arquivos para escrita
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DefaultFileSystemWriteGuardSetting
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultFileSystemWriteGuardSetting
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultGeolocationSetting
  #### Configuração de geolocalização padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Defina se os sites podem controlar a localização geográfica dos usuários. Você pode permitir o controle por padrão ("AllowGeolocation"), o bloqueio por padrão ("BlockGeolocation") ou perguntar ao usuário toda vez que um site solicitar sua localização ("AskGeolocation").

se você não configurar essa política, "AskGeolocation" será usado e o usuário poderá alterá-la.

Mapeamento das opções da política:

* AllowGeolocation (1) = Permitir que sites rastreiem a localização física dos usuários

* BlockGeolocation (2) = Não permitir que nenhum site rastreie a localização física dos usuários

* AskGeolocation (3) = Perguntar sempre que um site desejar rastrear a localização física dos usuários

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultGeolocationSetting
  - Nome da GP: Configuração de geolocalização padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DefaultGeolocationSetting
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultGeolocationSetting
  - Exemplo de valor:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultImagesSetting
  #### Configuração de imagens padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define se os sites podem exibir imagens. Você pode permitir imagens em todos os sites ("AllowImages") ou bloqueá-las em todos os sites ("BlockImages").

Se você não configurar essa política, as imagens serão permitidas por padrão, e o usuário poderá alterar essa configuração.

Mapeamento das opções da política:

* AllowImages (1) = Permitir que todos os sites mostrem todas as imagens

* BlockImages (2) = Não permitir que nenhum site mostre imagens

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultImagesSetting
  - Nome da GP: Configuração de imagens padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DefaultImagesSetting
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultImagesSetting
  - Exemplo de valor:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultInsecureContentSetting
  #### Controlar uso de exceções de conteúdo não seguro
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 80 ou posterior

  #### Descrição
  Permite definir se os usuários podem adicionar exceções para permitir conteúdo misto para sites específicos.

Essa política pode ser substituída por padrões de URL específicos usando as políticas [InsecureContentAllowedForUrls](#insecurecontentallowedforurls) e [InsecureContentBlockedForUrls](#insecurecontentblockedforurls).

Se essa política não for definida, os usuários terão permissão para adicionar exceções para permitir conteúdo misto bloqueável e desabilitar upgrades automáticos de conteúdo misto opcionalmente bloqueável.

Mapeamento das opções da política:

* BlockInsecureContent (2) = Não permitir que nenhum site carregue conteúdo misto

* AllowExceptionsInsecureContent (3) = Permitir que os usuários adicionem exceções para permitir conteúdo misto

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultInsecureContentSetting
  - Nome da GP: Controlar uso de exceções de conteúdo não seguro
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DefaultInsecureContentSetting
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultInsecureContentSetting
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultJavaScriptSetting
  #### Configuração de JavaScript padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define se os sites podem executar o JavaScript. Você pode permitir a execução do JavaScript em todos os sites ("AllowJavaScript") ou bloquear a execução dele em todos os sites ("BlockJavaScript").

Se você não configurar essa política, todos os sites poderão executar o JavaScript por padrão e o usuário poderá alterar essa configuração.

Mapeamento das opções da política:

* AllowJavaScript (1) = Permitir que todos os sites executem JavaScript

* BlockJavaScript (2) = Não permitir que nenhum site execute JavaScript

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultJavaScriptSetting
  - Nome da GP: Configuração de JavaScript padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DefaultJavaScriptSetting
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultJavaScriptSetting
  - Exemplo de valor:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultNotificationsSetting
  #### Configuração de notificação padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define se os sites podem exibir notificações na área de trabalho. Você pode aceitá-las por padrão ("AllowNotifications"), recusá-las por padrão ("BlockNotifications") ou receber uma solicitação sempre que um site precisar mostrar uma notificação ("AskNotifications").

Se você não configurar essa política, as notificações serão aceitas por padrão e o usuário poderá alterar essa configuração.

Mapeamento das opções da política:

* AllowNotifications (1) = Permitir que sites mostrem notificações da área de trabalho

* BlockNotifications (2) = Não permitir que nenhum site mostre notificações na área de trabalho

* AskNotifications (3) = Perguntar sempre que um site desejar mostrar notificações da área de trabalho

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultNotificationsSetting
  - Nome da GP: Configuração de notificação padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DefaultNotificationsSetting
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultNotificationsSetting
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultPluginsSetting
  #### Configuração padrão do Adobe Flash
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  [PluginsAllowedForUrls](#pluginsallowedforurls) e [PluginsBlockedForUrls](#pluginsblockedforurls) são verificados primeiro e, em seguida, essa política. As opções são 'ClickToPlay' e 'BlockPlugins'. Se você definir esta política como 'BlockPlugins', este plug-in será negado para todos os sites. 'ClickToPlay' permite que o plug-in Flash seja executado, mas os usuários clicam no espaço reservado para iniciá-lo.

Se você não definir essa política, ela usará BlockPlugins e os usuários poderão alterar essa configuração.

 Observação: a reprodução automática é somente para domínios listados explicitamente na política de [PluginsAllowedForUrls](#pluginsallowedforurls) . Para ativar a reprodução automática para todos os sites, adicione http://* e https://* à lista de URLs permitidas.

Mapeamento das opções da política:

* BlockPlugins (2) = Bloquear o plug-in do Adobe Flash

* ClickToPlay (3) = Clicar para reproduzir

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultPluginsSetting
  - Nome da GP: Configuração padrão do Adobe Flash
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DefaultPluginsSetting
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultPluginsSetting
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultPopupsSetting
  #### Configuração de janela pop-up padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define se os sites poderão mostrar janelas pop-up. Você pode permiti-las em todos os sites ("AllowPopups") ou bloqueá-las em todos os sites ("BlockPopups").

Se você não configurar essa política, as janelas pop-up serão bloqueadas por padrão, e os usuários poderão alterar essa configuração.

Mapeamento das opções da política:

* AllowPopups (1) = Permitir que todos os sites mostrem pop-ups

* BlockPopups (2) = Não permitir que nenhum site mostre pop-ups

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultPopupsSetting
  - Nome da GP: Configuração de janela pop-up padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DefaultPopupsSetting
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultPopupsSetting
  - Exemplo de valor:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultWebBluetoothGuardSetting
  #### Controlar o uso da API Web Bluetooth
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Controla se os sites podem acessar dispositivos Bluetooth próximos. Você pode bloquear completamente o acesso ou exigir que o site pergunte ao usuário sempre que ele quiser acessar um dispositivo Bluetooth.

Se você não configurar esta política, será usado o valor padrão ("AskWebBluetooth", que significa que os usuários serão sempre perguntados) e os usuários poderão alterá-lo.

Mapeamento das opções da política:

* BlockWebBluetooth (2) = Não permitir que nenhum site solicite acesso a dispositivos Bluetooth por meio da API Bluetooth da Web

* AskWebBluetooth (3) = Permitir que sites peçam ao usuário para conceder acesso a um dispositivo Bluetooth próximo

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultWebBluetoothGuardSetting
  - Nome da GP: Controlar o uso da API Web Bluetooth
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DefaultWebBluetoothGuardSetting
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultWebBluetoothGuardSetting
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultWebUsbGuardSetting
  #### Controlar o uso da API WebUSB
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define se os sites podem acessar dispositivos USB conectados. Você pode bloquear totalmente o acesso ou perguntar ao usuário toda vez que um site precisar obter acesso a dispositivos USB conectados.

Você pode substituir essa política por padrões de URL específicos usando as políticas [WebUsbAskForUrls](#webusbaskforurls) e [WebUsbBlockedForUrls](#webusbblockedforurls).

Se você não definir essa política, os sites poderão solicitar aos usuários a permissão para acessar os dispositivos USB conectados ("AskWebUsb") por padrão, e os usuários poderão alterar essa configuração.

Mapeamento das opções da política:

* BlockWebUsb (2) = Não permitir que nenhum site solicite acesso a dispositivos USB por meio da API WebUSB

* AskWebUsb (3) = Permitir que os sites solicitem ao usuário que conceda acesso a um dispositivo USB conectado

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultWebUsbGuardSetting
  - Nome da GP: Controlar o uso da API WebUSB
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DefaultWebUsbGuardSetting
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultWebUsbGuardSetting
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### FileSystemReadAskForUrls
  #### Permitir acesso de leitura através da API do Sistema de Arquivos nesses sites
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  A configuração da política permite listar os padrões de URL que especificam quais sites podem fazer com que os usuários os concedas a eles o acesso de leitura a arquivos ou diretórios no sistema de arquivos do sistema operacional do host pela API do sistema de arquivos.

Deixando a política sem definição significa, [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) se aplica a todos os sites, se ela estiver definida. Caso contrário, as configurações pessoais dos usuários serão aplicadas. os padrões de URL do

não podem entrar em conflito com [FileSystemReadBlockedForUrls](#filesystemreadblockedforurls). Nenhuma política tem prioridade se uma URL corresponder a ambos.

Para obter informações detalhadas sobre os padrões de url válidos, confira https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: FileSystemReadAskForUrls
  - Nome da GP: Permitir acesso de leitura através da API do Sistema de Arquivos nesses sites
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\2 = "[*.]example.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: FileSystemReadAskForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### FileSystemReadBlockedForUrls
  #### Bloquear o acesso de leitura pela API do Sistema de Arquivos nestes sites
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Se você definir essa política, poderá listar os padrões de URL que especificam quais sites não podem solicitar que os usuários os concedas a eles o acesso de leitura a arquivos ou diretórios no sistema de arquivos do sistema operacional do host pela API do Sistema de Arquivos.

Se você não definir essa política, [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) será aplicada a todos os sites, se ela estiver definida. Caso contrário, as configurações pessoais dos usuários serão aplicadas.

Os padrões de URL do não podem entrar em conflito com [FileSystemReadAskForUrls](#filesystemreadaskforurls). Nenhuma política tem prioridade se uma URL corresponder a ambos.

Para obter informações detalhadas sobre os padrões de url válidos, confira https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: FileSystemReadBlockedForUrls
  - Nome da GP: Bloquear o acesso de leitura pela API do Sistema de Arquivos nestes sites
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\2 = "[*.]example.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: FileSystemReadBlockedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### FileSystemWriteAskForUrls
  #### Permitir o acesso de gravação a arquivos e diretórios nesses sites
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Se você definir essa política, poderá listar os padrões de URL que especificam quais sites podem solicitar aos usuários que lhes conceda acesso de gravação a arquivos ou diretórios no sistema de arquivos do sistema operacional do host.

Se você não definir essa política, [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) será aplicada a todos os sites, se ela estiver definida. Caso contrário, as configurações pessoais dos usuários serão aplicadas.

Os padrões de URL não podem entrar em conflito com [FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls). Nenhuma política terá precedência se uma URL corresponder com ambas.

Para obter informações detalhadas sobre padrões url válidos, consulte https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: FileSystemWriteAskForUrls
  - Nome da GP: Permitir o acesso de gravação a arquivos e diretórios nesses sites
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\2 = "[*.]example.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: FileSystemWriteAskForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### FileSystemWriteBlockedForUrls
  #### Bloquear o acesso de gravação a arquivos e diretórios nesses sites
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Se você definir essa política, poderá listar os padrões de URL que especificam quais sites não podem solicitar que os usuários os concedas a eles o acesso de gravação a arquivos ou diretórios no sistema de arquivos do sistema operacional do host.

Se você não definir essa política, [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) será aplicada a todos os sites, se ela estiver definida. Caso contrário, as configurações pessoais dos usuários serão aplicadas. Os padrões de URL do

não podem entrar em conflito com [FileSystemWriteAskForUrls](#filesystemwriteaskforurls). Nenhuma política tem prioridade se uma URL corresponder a ambos.

Para obter informações detalhadas sobre os padrões de url válidos, confira https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: FileSystemWriteBlockedForUrls
  - Nome da GP: Bloquear o acesso de gravação a arquivos e diretórios nesses sites
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\2 = "[*.]example.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: FileSystemWriteBlockedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ImagesAllowedForUrls
  #### Permitir imagens nestes sites
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Defina uma lista de sites com base nos padrões da URL que podem exibir imagens.

Se você não configurar esta política, o valor padrão global será usado em todos os sites da [DefaultImagesSetting](#defaultimagessetting) política (se definida) ou da configuração pessoal do usuário.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ImagesAllowedForUrls
  - Nome da GP: Permitir imagens nestes sites
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImagesAllowedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ImagesBlockedForUrls
  #### Bloquear imagens em sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Defina uma lista de sites com base nos padrões da URL que não têm permissão para exibir imagens.

Se você não configurar esta política, o valor padrão global da [DefaultImagesSetting](#defaultimagessetting) política (se definido) ou a configuração pessoal do usuário serão usados em todos os sites.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ImagesBlockedForUrls
  - Nome da GP: Bloquear imagens em sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImagesBlockedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### InsecureContentAllowedForUrls
  #### Permitir conteúdo não seguro em sites especificados
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 80 ou posterior

  #### Descrição
  Cria uma lista de padrões de URL para especificar sites que podem exibir conteúdo misto não seguro (ou seja, conteúdo HTTP em sites HTTPS).

Se você não configurar essa política, o conteúdo misto bloqueado será bloqueado e será feito upgrade do conteúdo misto que poderá ser bloqueado opcionalmente. Contudo, os usuários terão permissão para definir exceções a fim de permitir conteúdo misto não seguro para sites específicos.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: InsecureContentAllowedForUrls
  - Nome da GP: Permitir conteúdo não seguro em sites especificados
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\2 = "[*.]example.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: InsecureContentAllowedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### InsecureContentBlockedForUrls
  #### Bloquear conteúdo não seguro em sites especificados
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 80 ou posterior

  #### Descrição
  Cria uma lista de padrões de URL que especificam sites que têm permissão para exibir conteúdo misto (ou seja, ativo) bloqueável (ou seja, conteúdo HTTP em sites HTTPS) e para os quais a atualização do conteúdo misto opcionalmente bloqueável será desabilitada.

Se essa política não for definida, o conteúdo misto bloqueável será bloqueado e, opcionalmente, será feito upgrade no conteúdo misto bloqueável. Contudo, os usuários terão permissão para definir exceções a fim de permitir conteúdo misto não seguro para sites específicos.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: InsecureContentBlockedForUrls
  - Nome da GP: Bloquear conteúdo não seguro em sites especificados
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\2 = "[*.]example.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: InsecureContentBlockedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### JavaScriptAllowedForUrls
  #### Permitir JavaScript em sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Defina uma lista de sites com base nos padrões da URL com permissão para executar o JavaScript.

Se você não configurar esta política, o valor padrão global da [DefaultJavaScriptSetting](#defaultjavascriptsetting) política (se definido) ou a configuração pessoal do usuário serão usados em todos os sites.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: JavaScriptAllowedForUrls
  - Nome da GP: Permitir JavaScript em sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: JavaScriptAllowedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### JavaScriptBlockedForUrls
  #### Bloquear o JavaScript em sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define uma lista de sites, com base em padrões de URL, que não têm permissão para executar JavaScript.

Se você não configurar esta política, será usado o valor padrão global da política [DefaultJavaScriptSetting](#defaultjavascriptsetting) (se definida) ou a configuração de pessoal do usuário para todos os sites.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: JavaScriptBlockedForUrls
  - Nome da GP: Bloquear o JavaScript em sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: JavaScriptBlockedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### LegacySameSiteCookieBehaviorEnabled
  #### Habilitar a configuração do comportamento de cookies SameSite herdado padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 80 ou posterior

  #### Descrição
  Permite reverter todos os cookies para o comportamento SameSite herdado. A reversão para o comportamento herdado faz com que os cookies que não especificam o atributo SameSite sejam tratados como se fossem "SameSite=None" e remove o requisito para que os cookies "SameSite=None" contenham o atributo "Secure".

Se você não configurar esta política, o comportamento padrão para os cookies que não especificam um atributo SameSite dependerá de outras fontes de configuração do recurso SameSite-by-default. Este recurso pode ser configurado por uma avaliação de campo ou pela habilitação do sinalizador same-site-by-default-cookies em edge://flags.

Mapeamento das opções da política:

* DefaultToLegacySameSiteCookieBehavior (1) = Reverter para o comportamento SameSite herdado para cookies em todos os sites

* DefaultToSameSiteByDefaultCookieBehavior (2) = Usar o comportamento SameSite-by-default para cookies em todos os sites

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: LegacySameSiteCookieBehaviorEnabled
  - Nome da GP: Habilitar a configuração do comportamento de cookies SameSite herdado padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: LegacySameSiteCookieBehaviorEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: LegacySameSiteCookieBehaviorEnabled
  - Exemplo de valor:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### LegacySameSiteCookieBehaviorEnabledForDomainList
  #### Reverter para o comportamento SameSite herdado de cookies em sites especificados
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 80 ou posterior

  #### Descrição
  Os cookies configurados para padrões especificados de correspondência de domínios serão revertidos para o comportamento SameSite herdado.

Reverter para o comportamento herdado faz com que os cookies que não especificam um atributo SameSite sejam tratados como se fossem "SameSite=None" e remove o requisito para que os cookies "SameSite=None" contenham o atributo "Secure".

Se você não configurar esta política, o valor padrão global será usado. O padrão global também será usado para cookies em domínios não cobertos pelos padrões especificados.

O valor padrão global pode ser configurado usando a política [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled). Se [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) não estiver configurado, o valor padrão global será aquele usado em outras fontes de configuração.

Observe que os padrões listados nesta política são tratados como domínios, não URLs. Portanto, você não deve especificar um esquema ou porta.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Nome da GP: Reverter para o comportamento SameSite herdado de cookies em sites especificados
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\1 = "www.example.com"
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\2 = "[*.]example.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Exemplo de valor:
``` xml
<array>
  <string>www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### NotificationsAllowedForUrls
  #### Permitir notificações em sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite criar uma lista de padrões de URL para especificar sites que têm permissão para exibir notificações.

Se você não definir esta política, o valor padrão global será usado para todos os sites. Esse valor padrão será da política de [DefaultNotificationsSetting](#defaultnotificationssetting) se ela estiver definida ou da configuração pessoal do usuário. Para obter informações detalhadas sobre os padrões de URL válidos, confira  [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NotificationsAllowedForUrls
  - Nome da GP: Permitir notificações em sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NotificationsAllowedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### NotificationsBlockedForUrls
  #### Bloquear notificações em sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite criar uma lista de padrões de URL para especificar sites que não têm permissão para exibir notificações.

Se você não definir esta política, o valor padrão global será usado por todos os sites. Esse valor padrão será da política de [DefaultNotificationsSetting](#defaultnotificationssetting) se ela estiver definida ou da configuração pessoal do usuário. Para obter informações detalhadas sobre os padrões de URL válidos, confira [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NotificationsBlockedForUrls
  - Nome da GP: Bloquear notificações em sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NotificationsBlockedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PluginsAllowedForUrls
  #### Permitir o plug-in do Adobe Flash em sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define uma lista de sites, com base em padrões de URL que podem executar o plug-in Adobe Flash.

Se você não configurar essa política, o valor padrão global da política [DefaultPluginsSetting](#defaultpluginssetting) (se definido) ou da configuração pessoal do usuário será usado para todos os sites.

Para obter informações detalhadas sobre padrões de URL válidos, confira [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). No entanto, a partir de M85, padrões com caracteres curinga '*' e '[*.]'  no host não têm mais suporte para esta política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PluginsAllowedForUrls
  - Nome da GP: Permitir o plug-in do Adobe Flash em sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\2 = "http://contoso.edu:8080"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PluginsAllowedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PluginsBlockedForUrls
  #### Bloquear o plug-in do Adobe Flash em sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL que são impedidos de executar Adobe Flash.

Se você não configurar essa política, o valor padrão global da política [DefaultPluginsSetting](#defaultpluginssetting) (se definido) ou da configuração pessoal do usuário será usado para todos os sites.

Para obter informações detalhadas sobre padrões de URL válidos, confira [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). No entanto, a partir de M85, padrões com caracteres curinga '*' e '[*.]'  no host não têm mais suporte para esta política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PluginsBlockedForUrls
  - Nome da GP: Bloquear o plug-in do Adobe Flash em sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\2 = "http://contoso.edu:8080"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PluginsBlockedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PopupsAllowedForUrls
  #### Permitir janelas pop-up em sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define uma lista de sites, com base em padrões de URL, que podem abrir janelas pop-up.

Se você não configurar esta política, será usado o valor padrão global da política [DefaultPopupsSetting](#defaultpopupssetting) (se definida) ou a configuração pessoal do usuário para todos os sites.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PopupsAllowedForUrls
  - Nome da GP: Permitir janelas pop-up em sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PopupsAllowedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PopupsBlockedForUrls
  #### Bloquear janelas pop-up em sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define uma lista de sites, com base nos padrões de URL, que são impedidos de abrir janelas pop-up.

Se você não configurar esta política, será usado o valor padrão global da política [DefaultPopupsSetting](#defaultpopupssetting) (se definida) ou a configuração pessoal do usuário para todos os sites.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PopupsBlockedForUrls
  - Nome da GP: Bloquear janelas pop-up em sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PopupsBlockedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### RegisteredProtocolHandlers
  #### Registrar manipuladores de protocolo
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Defina esta política (recomendável apenas) para registrar uma lista de manipuladores de protocolo. Esta lista é mesclada com aquelas registradas pelo usuário e ambas estão disponíveis para uso.

Para registrar um manipulador de protocolo:

- Defina a propriedade de protocolo para o esquema (por exemplo, "mailto")
-Defina a propriedade URL para a propriedade URL do aplicativo que manipula o esquema especificado no campo "protocolo". O padrão pode incluir um "%s" placeholder que  a URL manipulada substitui.

Os usuários não podem remover um manipulador de protocolo registrado por essa política. No entanto, eles podem instalar um novo manipulador de protocolo padrão para substituir os manipuladores de protocolo existentes.

  #### Recursos com suporte:
  - Pode ser obrigatório: Não
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Dicionário

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: RegisteredProtocolHandlers
  - Nome da GP: Registrar manipuladores de protocolo
  - Caminho da GP (Obrigatório): N/A
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Configurações de conteúdo
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): N/A
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: RegisteredProtocolHandlers
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [
  {
    "default": true, 
    "protocol": "mailto", 
    "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"
  }
]
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: RegisteredProtocolHandlers
  - Exemplo de valor:
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
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SpotlightExperiencesAndRecommendationsEnabled
  #### Escolha se os usuários podem receber imagens de plano de fundo personalizadas e textos, sugestões, notificações
e dicas para serviços Microsoft
  
  
  #### Versões com suporte:
  - No Windows desde a versão 86 ou posterior

  #### Descrição
  Escolha se os usuários podem receber imagens de plano de fundo personalizadas e textos, sugestões, notificações e dicas para os serviços Microsoft.

Se você habilitar ou não definir essa configuração, as experiências e as recomendações de destaque serão ativadas.

Se você desabilitar essa configuração, as experiências e as recomendações de destaque serão desabilitadas.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SpotlightExperiencesAndRecommendationsEnabled
  - Nome da GP: Escolha se os usuários podem receber imagens de plano de fundo personalizadas e textos, sugestões, notificações
e dicas para serviços Microsoft
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: SpotlightExperiencesAndRecommendationsEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### WebUsbAllowDevicesForUrls
  #### Conceder acesso a sites específicos para se conectar a dispositivos USB específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite definir uma lista de URLs que especificam quais sites receberão automaticamente permissão para acessar um dispositivo USB com as IDs de fornecedor e de produto fornecidas. Cada item da lista deve conter tanto dispositivos quanto URLs para que a política seja válida. Cada item em dispositivos pode conter um campo de ID do fornecedor e de ID do produto (product ID). Qualquer ID omitida é tratada como curinga com uma exceção, e essa exceção é que não é possível especificar uma ID de produto sem que uma ID de fornecedor também seja especificada. Caso contrário, a política não será válida e será ignorada.

O modelo de permissão USB usa a URL do site solicitante ("URL de solicitação") e a URL do site do quadro de nível superior ("URL de inserção") para conceder permissão à URL de solicitação para acessar o dispositivo USB. A URL de solicitação pode ser diferente da URL de inserção quando o site solicitante é carregado em um iframe. Portanto, o campo "URLs" pode conter até duas cadeias de caracteres de URL delimitadas por uma vírgula para especificar as URLs de solicitação e de inserção, respectivamente. Se for especificada apenas uma URL, o acesso aos dispositivos USB correspondentes será concedido quando a URL do site solicitante corresponder a essa URL, independentemente do status de inserção. As URLs citadas em "urls" devem ser válidas, caso contrário, a política será ignorada.

Se essa política não for definida, o valor padrão global será usado para todos os sites da política [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting), se definida, ou da configuração pessoal do usuário.

Os padrões de URL nessa política não devem conflitar com os que foram configurados via [WebUsbBlockedForUrls](#webusbblockedforurls). Se houver um conflito, essa política terá precedência sobre [WebUsbBlockedForUrls](#webusbblockedforurls) e [WebUsbAskForUrls](#webusbaskforurls).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Dicionário

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: WebUsbAllowDevicesForUrls
  - Nome da GP: Conceder acesso a sites específicos para se conectar a dispositivos USB específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: WebUsbAllowDevicesForUrls
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
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


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebUsbAllowDevicesForUrls
  - Exemplo de valor:
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
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### WebUsbAskForUrls
  #### Permitir WebUSB em sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define uma lista de sites, com base em padrões de URL, que podem solicitar ao usuário acesso a um dispositivo USB.

Se você não configurar esta política, será usado o valor padrão global da política [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (se definida) ou a configuração pessoal do usuário para todos os sites.

Os padrões de URL definidos nesta política não podem entrar em conflito com aqueles configurados na política [WebUsbBlockedForUrls](#webusbblockedforurls). Você não pode permitir e bloquear uma URL ao mesmo tempo. Para obter informações detalhadas sobre os padrões de URL válidos, confira [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: WebUsbAskForUrls
  - Nome da GP: Permitir WebUSB em sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebUsbAskForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### WebUsbBlockedForUrls
  #### Bloquear WebUSB em sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define uma lista de sites, com base em padrões de URL, que não podem solicitar ao usuário que conceda a eles acesso a um dispositivo USB.

Se você não configurar esta política, será usado o valor padrão global da política [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (se definida) ou a configuração pessoal do usuário para todos os sites.

Os padrões de URL nesta política não podem entrar em conflito com aqueles configurados na política [WebUsbAskForUrls](#webusbaskforurls). Você não pode permitir e bloquear uma URL ao mesmo tempo. Para obter informações detalhadas sobre os padrões de URL válidos, confira [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: WebUsbBlockedForUrls
  - Nome da GP: Bloquear WebUSB em sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações de conteúdo
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebUsbBlockedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ## Configurações do Application Guard policies

  [Voltar ao início](#microsoft-edge---políticas)

  ### ApplicationGuardContainerProxy
  #### Proxy do Contêiner do Application Guard
  
  
  #### Versões com suporte:
  - No Windows desde a versão 84 ou posterior

  #### Descrição
  Define as configurações de proxy para o Microsoft Edge Application Guard.
se você habilitar essa política, o Microsoft Edge Application Guard ignorará outras fontes de configurações de proxy.

se você não configurar essa política, Microsoft Edge Application Guard usará a configuração de proxy do host.

essa política não afeta a configuração de proxy do Microsoft Edge fora do Application Guard (no host).

campo ProxyMode permite especificar o servidor proxy usado pelo Microsoft Edge Application Guard.

campo ProxyPacUrl é uma URL para um arquivo. PAC de proxy.

campo ProxyServer é uma URL para o servidor proxy.

se você escolher o valor "direto" como [ProxyMode](#proxymode), todos os outros campos serão ignorados.

se você escolher o valor de ' auto_detect ' como 'ProxyMode', todos os outros campos são ignorados.

se você escolher o valor de ' fixed_servers ' como 'ProxyMode', o campo 'ProxyServer' é usado.

se você escolher o valor de ' pac_script ' como 'ProxyMode', o campo 'ProxyPacUrl' é usado.

Para obter mais informações sobre como identificar o tráfego do Application Guard por meio de proxy duplo, acesse [https://go.microsoft.com/fwlink/?linkid=2134653](https://go.microsoft.com/fwlink/?linkid=2134653).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Dicionário

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ApplicationGuardContainerProxy
  - Nome da GP: Proxy do Contêiner do Application Guard
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações do Application Guard
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ApplicationGuardContainerProxy
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ## Configurações do SmartScreen policies

  [Voltar ao início](#microsoft-edge---políticas)

  ### PreventSmartScreenPromptOverride
  #### Impedir que avisos do Microsoft Defender SmartScreen sejam ignorados para sites
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Essa configuração de política permite que você decida se os usuários podem substituir os avisos do Microsoft Defender SmartScreen sobre sites potencialmente mal-intencionados.

Se você habilitar essa configuração, os usuários não poderão ignorar os avisos do Microsoft Defender SmartScreen e serão impedidos de continuar no site.

Se você desabilitar ou não definir essa configuração, os usuários poderão ignorar os avisos do Microsoft Defender SmartScreen e continuar no site.

Essa política está disponível somente em instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory instâncias do Windows 10 Pro ou Enterprise registradas para o gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou associadas a um domínio via MCX.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PreventSmartScreenPromptOverride
  - Nome da GP: Impedir que avisos do Microsoft Defender SmartScreen sejam ignorados para sites
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações do SmartScreen
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: PreventSmartScreenPromptOverride
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PreventSmartScreenPromptOverride
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PreventSmartScreenPromptOverrideForFiles
  #### Impedir que os avisos do Microsoft Defender SmartScreen sobre downloads sejam ignorados
  
  
  #### Versões com suporte:
  - No Windows desde a versão 77 ou posterior
  - No macOS desde a versão 79 ou posterior

  #### Descrição
  Essa política permite determinar se os usuários podem substituir os avisos do Microsoft Defender SmartScreen sobre downloads não verificados.

Se você habilitar essa política, os usuários de sua organização não poderão ignorar os avisos do Microsoft Defender SmartScreen, e eles serão impedidos de concluir os downloads não verificados.

Se você desabilitar ou não configurar essa política, os usuários poderão ignorar os avisos do Microsoft Defender SmartScreen e concluir downloads não verificados.

Essa política está disponível somente em instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, instâncias do Windows 10 Pro ou Enterprise registradas para o gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou associadas a um domínio via MCX.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PreventSmartScreenPromptOverrideForFiles
  - Nome da GP: Impedir que os avisos do Microsoft Defender SmartScreen sobre downloads sejam ignorados
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações do SmartScreen
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: PreventSmartScreenPromptOverrideForFiles
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PreventSmartScreenPromptOverrideForFiles
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SmartScreenAllowListDomains
  #### Configurar a lista de domínios para os quais o Microsoft Defender SmartScreen não disparará avisos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Configure a lista de domínios confiáveis do Microsoft Defender SmartScreen. Isso significa que:
o Microsoft Defender SmartScreen não verificará recursos potencialmente mal-intencionados, como software de phishing e outro malware se as URLs de origem coincidirem com esses domínios.
O serviço de proteção contra download do Microsoft Defender SmartScreen não verificará os downloads hospedados nesses domínios.

Se você habilitar essa política, o Microsoft Defender SmartScreen confiará nesses domínios.
Se você desabilitar ou não configurar essa política, a proteção padrão do Microsoft Defender SmartScreen será aplicada a todos os recursos.

Essa política está disponível somente em instâncias do Windows que façam parte de um domínio do Microsoft Active Directory, instâncias do Windows 10 Pro ou Enterprise registradas para o gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou associadas a um domínio via MCX.
Observe também que essa política não se aplica quando a organização habilita a Proteção Avançada contra Ameaças do Microsoft Defender. É necessário configurar suas listas de contatos bloqueados e permitidos na Central de Segurança do Microsoft Defender.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SmartScreenAllowListDomains
  - Nome da GP: Configurar a lista de domínios para os quais o Microsoft Defender SmartScreen não disparará avisos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações do SmartScreen
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\2 = "myuniversity.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SmartScreenAllowListDomains
  - Exemplo de valor:
``` xml
<array>
  <string>mydomain.com</string>
  <string>myuniversity.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SmartScreenEnabled
  #### Configurar o Microsoft Defender SmartScreen
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Essa configuração de política permite configurar a ativação do Microsoft Defender SmartScreen. O Microsoft Defender SmartScreen fornece mensagens de aviso para ajudar a proteger seus funcionários contra potenciais golpes de phishing e software mal-intencionado. Por padrão, o Microsoft Defender SmartScreen é ativado.

Se você habilitar essa configuração, o Microsoft Defender SmartScreen será ativado.

Se você desabilitar essa configuração, o Microsoft Defender SmartScreen será desativado.

Se você não definir essa configuração, os usuários poderão escolher se desejam usar o Microsoft Defender SmartScreen.

Essa política está disponível somente em instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, instâncias do Windows 10 Pro ou Enterprise registradas para o gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou associadas a um domínio via MCX..

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SmartScreenEnabled
  - Nome da GP: Configurar o Microsoft Defender SmartScreen
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações do SmartScreen
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Configurações do SmartScreen
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: SmartScreenEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SmartScreenEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SmartScreenForTrustedDownloadsEnabled
  #### Forçar verificações do Microsoft Defender SmartScreen em downloads de fontes confiáveis
  
  
  #### Versões com suporte:
  - No Windows desde a versão 78 ou posterior

  #### Descrição
  Essa configuração de política permite definir se o Microsoft Defender SmartScreen verificará a reputação de download de uma fonte confiável.

Se você habilitar ou não definir essa configuração, o Microsoft Defender SmartScreen verificará a reputação do download, independentemente da fonte.

Se você desabilitar essa configuração, o Microsoft Defender SmartScreen não verificará a reputação do download ao baixar de uma fonte confiável.

Essa política está disponível somente em instâncias do Windows que façam parte de um domínio do Microsoft Active Directory, instâncias do Windows 10 Pro ou Enterprise registradas para o gerenciamento de dispositivos.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SmartScreenForTrustedDownloadsEnabled
  - Nome da GP: Forçar verificações do Microsoft Defender SmartScreen em downloads de fontes confiáveis
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações do SmartScreen
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Configurações do SmartScreen
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: SmartScreenForTrustedDownloadsEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SmartScreenPuaEnabled
  #### Configurar o Microsoft Defender SmartScreen para bloquear aplicativos potencialmente indesejados
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 80 ou posterior

  #### Descrição
  Essa configuração de política permite definir a ativação do bloqueio de aplicativos potencialmente indesejados no Microsoft Defender SmartScreen. O bloqueio de aplicativos potencialmente indesejados no Microsoft Defender SmartScreen fornece mensagens de aviso para ajudar a proteger os usuários contra adware, mineradores de moeda, bundleware e outros aplicativos de baixa reputação que são hospedados por sites. O bloqueio de aplicativos potencialmente indesejados no Microsoft Defender SmartScreen está desativado por padrão.

Se você habilitar essa configuração, o bloqueio de aplicativos potencialmente indesejados no Microsoft Defender SmartScreen será ativado.

Se você desabilitar essa configuração, o bloqueio de aplicativos potencialmente indesejados no Microsoft Defender SmartScreen será desativado.

Se você não definir essa configuração, os usuários poderão escolher se desejam usar o bloqueio de aplicativos potencialmente indesejados no Microsoft Defender SmartScreen.

Essa política está disponível apenas em instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, instâncias do Windows 10 Pro ou Enterprise registradas para o gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou associadas a um domínio via MCX.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SmartScreenPuaEnabled
  - Nome da GP: Configurar o Microsoft Defender SmartScreen para bloquear aplicativos potencialmente indesejados
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Configurações do SmartScreen
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Configurações do SmartScreen
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: SmartScreenPuaEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SmartScreenPuaEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ## Extensões policies

  [Voltar ao início](#microsoft-edge---políticas)

  ### ExtensionAllowedTypes
  #### Configurar tipos de extensão permitidos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Controla quais tipos de extensão podem ser instalados e limita o acesso do tempo de execução.

Esta configuração define os tipos de extensão permitidos e com quais hosts eles podem interagir. O valor é uma lista de cadeias de caracteres, e cada uma delas deve ser uma das seguintes: "extension", "theme", "user_script" e "hosted_app". Consulte a documentação sobre extensões do Microsoft Edge para obter mais informações sobre esses tipos.

Observe que esta política também afeta as extensões a serem instaladas forçadamente pela política [ExtensionInstallForcelist](#extensioninstallforcelist).

Se você habilitar esta política, apenas as extensões que corresponderem a um tipo na lista serão instaladas.

Se você não configurar esta política, nenhuma restrição sobre os tipos de extensão aceitáveis será aplicada.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ExtensionAllowedTypes
  - Nome da GP: Configurar tipos de extensão permitidos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Extensões
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes\1 = "hosted_app"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExtensionAllowedTypes
  - Exemplo de valor:
``` xml
<array>
  <string>hosted_app</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ExtensionInstallAllowlist
  #### Permitir que extensões específicas sejam instaladas
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Por padrão, todas as extensões são permitidas. No entanto, se você bloquear todas as extensões definindo a política 'ExtensionInstallBlockList' como "*", os usuários só poderão instalar as extensões definidas nesta política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ExtensionInstallAllowlist
  - Nome da GP: Permitir que extensões específicas sejam instaladas
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Extensões
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\2 = "extension_id2"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExtensionInstallAllowlist
  - Exemplo de valor:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ExtensionInstallBlocklist
  #### Controlar quais extensões não podem ser instaladas
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Liste extensões específicas que os usuários NÃO podem instalar no Microsoft Edge. Quando você implanta essa política, todas as extensões nessa lista que foram instaladas anteriormente serão desabilitadas e o usuário não poderá habilitá-las. Se você remover um item da lista de extensões bloqueadas, essa extensão será reabilitada automaticamente em qualquer lugar onde tenha sido instalada anteriormente.

Use "*" para bloquear todas as extensões que não estão listadas explicitamente na lista de permissões.

Se você não configurar essa política, os usuários poderão instalar qualquer extensão no Microsoft Edge.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ExtensionInstallBlocklist
  - Nome da GP: Controlar quais extensões não podem ser instaladas
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Extensões
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\2 = "extension_id2"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExtensionInstallBlocklist
  - Exemplo de valor:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ExtensionInstallForcelist
  #### Controlar quais extensões são instaladas silenciosamente
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica as extensões instaladas silenciosamente, sem a interação do usuário e que os usuários não podem desinstalar ou desabilitar ("força-instalada"). Todas as permissões solicitadas pelas extensões são concedidas implicitamente, sem interação do usuário, incluindo quaisquer permissões adicionais solicitadas por versões futuras da extensão. Além disso, as permissões são concedidas para as APIs de extensão enterprise.deviceAttributes e enterprise.platformKeys extension. Essas duas APIs estão disponíveis apenas para extensões forçadas a serem instaladas.

Essa política tem precedência sobre uma política de [ExtensionInstallBlocklist](#extensioninstallblocklist) potencialmente conflitante. Quando você tira uma extensão da lista de força instalada, ela é desinstalada automaticamente pela Microsoft Edge.

Instalação forçada fica limitada a aplicativos e extensões listados no site Complementos do Microsoft Edge para instâncias que não são uma das seguintes opções: Instâncias do Windows que fazem parte de um domínio Microsoft Active Directory ou instâncias do Windows 10 pro ou Enterprise que se inscreveram para o gerenciamento de dispositivos e as instâncias do macOS gerenciadas via MDM ou associadas a um domínio por meio do MCX.

Observe que os usuários podem modificar o código-fonte de qualquer extensão usando as ferramentas de desenvolvedor, potencialmente processando a extensão Dysfunctional. Se isso for uma preocupação, defina o [DeveloperToolsAvailability](#developertoolsavailability) política.

Usar o formato a seguir para adicionar uma extensão à lista:

[extensionID];[updateURL]

- extensionId - a cadeia de caracteres de 32 encontrada em edge://extensions quando estiver no modo de desenvolvedor.

– updateURL (opcional) é o endereço do documento XML de atualização para o aplicativo ou extensão, conforme descrito em [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043). Se você deseja instalar uma extensão a partir da loja Web do Chrome, forneça a URL de atualização do Chrome Web Store, https://clients2.google.com/service/update2/crx. Observe que a URL de atualização definida nesta política só é usada para a instalação inicial. as atualizações subsequentes da extensão usam o URL de atualização indicado no manifesto da extensão. Se você não definir o updateURL, a extensão será considerada hospedada na Microsoft Store e a seguinte URL de atualização será usada (https://edge.microsoft.com/extensionwebstorebase/v1/crx).

por exemplo, gggmmkjegpiggikcnhidnjjhmicpibll;https://edge.microsoft.com/extensionwebstorebase/v1/crx instala o aplicativo Microsoft Online na URL "atualizar" da Microsoft Store. Para obter mais informações sobre as extensões de hospedagem, confira: [https://go.microsoft.com/fwlink/?linkid=2095044](https://go.microsoft.com/fwlink/?linkid=2095044).

Se você não configurar essa política, não serão instaladas extensões automaticamente, e os usuários poderão desinstalar qualquer extensão no Microsoft Edge.

Observe que essa política não se aplica ao modo InPrivate.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ExtensionInstallForcelist
  - Nome da GP: Controlar quais extensões são instaladas silenciosamente
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Extensões
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\1 = "gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\2 = "abcdefghijklmnopabcdefghijklmnop"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExtensionInstallForcelist
  - Exemplo de valor:
``` xml
<array>
  <string>gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx</string>
  <string>abcdefghijklmnopabcdefghijklmnop</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ExtensionInstallSources
  #### Configurar fontes de instalação de script de usuário e extensão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define URLs que podem instalar extensões e temas.

Por padrão, os usuários precisam baixar um arquivo *.crx para cada extensão ou script que desejam instalar e, em seguida, arrastá-lo para a página de configurações do Microsoft Edge. Esta política permite que URLs específicas instalem a extensão ou o script para o usuário.

Cada item da lista é um padrão de correspondência de estilo de extensão (consulte [https://go.microsoft.com/fwlink/?linkid=2095039](https://go.microsoft.com/fwlink/?linkid=2095039)). Os usuários poderão instalar facilmente itens de qualquer URL que corresponda a um item dessa lista. A localização do arquivo *.crx e a página a partir da qual o download é iniciado (ou seja, o referenciador) devem ser autorizadas por esses padrões.

A política [ExtensionInstallBlocklist](#extensioninstallblocklist) tem precedência sobre esta política. As extensões que estiverem na lista de contatos bloqueados não serão instaladas, mesmo que venham de um site dessa lista.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ExtensionInstallSources
  - Nome da GP: Configurar fontes de instalação de script de usuário e extensão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Extensões
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources\1 = "https://corp.contoso.com/*"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExtensionInstallSources
  - Exemplo de valor:
``` xml
<array>
  <string>https://corp.contoso.com/*</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ExtensionSettings
  #### Definir configurações de gerenciamento de extensões
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define as configurações de gerenciamento de extensão para o Microsoft Edge.

Esta política controla várias configurações, incluindo as configurações controladas por quaisquer políticas existentes relacionadas a extensões. Esta política substituirá qualquer política herdada se ambas forem definidas.

Esta política mapeia uma ID de extensão ou uma URL de atualização para a configuração dela. Com uma ID de extensão, a configuração é aplicada somente à extensão especificada. Defina uma configuração padrão para a ID especial "*", para aplicar a todas as extensões que não forem especificamente listadas nesta política. Com uma URL de atualização, a configuração é aplicada a todas as extensões com a URL de atualização exata declarada no manifesto dessa extensão, conforme descrito em [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Dicionário

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ExtensionSettings
  - Nome da GP: Definir configurações de gerenciamento de extensões
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Extensões
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ExtensionSettings
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
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


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExtensionSettings
  - Exemplo de valor:
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
  

  [Voltar ao início](#microsoft-edge---políticas)

  ## Gerenciador de senhas e de proteção policies

  [Voltar ao início](#microsoft-edge---políticas)

  ### PasswordManagerEnabled
  #### Habilitar salvamento de senhas no gerenciador de senhas
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Habilite o Microsoft Edge para salvar as senhas dos usuários.

Se você habilitar essa política, os usuários poderão salvar suas senhas no Microsoft Edge. Na próxima visita que fizerem ao site, o Microsoft Edge inserirá a senha automaticamente.

Se você desabilitar essa política, os usuários não poderão salvar novas senhas, mas ainda poderão usar senhas salvas anteriormente.

Se você habilitar ou desabilitar essa política, os usuários não poderão alterá-la ou substituí-la no Microsoft Edge. Se você não configurá-la, os usuários poderão salvar senhas, além de desabilitar esse recurso.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PasswordManagerEnabled
  - Nome da GP: Habilitar salvamento de senhas no gerenciador de senhas
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Gerenciador de senhas e de proteção
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Gerenciador de senhas e de proteção
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: PasswordManagerEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PasswordManagerEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PasswordMonitorAllowed
  #### Permitir que os usuários sejam alertados se as senhas deles não forem seguras
  
  
  #### Versões com suporte:
  - No Windows desde a versão 85 ou posterior

  #### Descrição
  Permitir que o Microsoft Edge monitore senhas de usuário.

Se você habilitar essa política e um usuário for importado para habilitar a política, o usuário será alertado se qualquer uma das suas senhas armazenadas em Microsoft Edge não for segura. Microsoft Edge mostrará um alerta e essas informações também estarão disponíveis em Configurações > senhas > Monitor de senha.

Se você desabilitar essa política, não será solicitada permissão aos usuários para habilitar esse recurso. As senhas não serão examinadas, e elas não serão alertadas.

Se você habilitar ou não configurar a política, os usuários poderão ativar ou desativar esse recurso.

Para saber mais sobre como o Microsoft Edge localiza senhas não seguras, consulte [https://go.microsoft.com/fwlink/?linkid=2133833](https://go.microsoft.com/fwlink/?linkid=2133833)

Diretrizes adicionais:

Essa política pode ser definida como recomendado e como obrigatória, mas com um texto explicativo importante.

Obrigatório habilitado: Considerando que o consentimento do usuário individual é uma pré-condição para habilitar esse recurso para um determinado usuário, essa política não tem uma configuração habilitada obrigatória. Se a política estiver definida como obrigatória habilitada, a interface do usuário em configurações não será alterada e a seguinte mensagem de erro será exibida no edge://policy

Exemplo de mensagem de estado de erro: "esse valor de política é ignorado porque o monitor de senha requer o consentimento do usuário individual para que ele seja ativado. Você pode solicitar que os usuários da sua organização acedam às configurações > Perfil > senha e ativar o recurso."

Recomendado habilitado: se a política estiver definida como habilitada, a interface do usuário em configurações permanecerá no estado "desativado", mas um ícone de porta-arquivos ficará visível ao lado desta descrição exibida ao focalizar-"sua organização recomenda um valor específico para essa configuração e você escolheu um valor diferente"

Obrigatório e recomendado desabilitado: ambos os Estados funcionarão da maneira normal, com as legendas usuais mostradas para os usuários.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PasswordMonitorAllowed
  - Nome da GP: Permitir que os usuários sejam alertados se as senhas deles não forem seguras
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Gerenciador de senhas e de proteção
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Gerenciador de senhas e de proteção
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: PasswordMonitorAllowed
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PasswordProtectionChangePasswordURL
  #### Configurar a URL de alteração de senha
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Configura a URL de alteração de senha (somente esquemas HTTP e HTTPS).

O serviço de proteção de senha enviará os usuários para essa URL para que alterem suas senhas depois de verem um aviso no navegador..

Se você habilitar essa política, o serviço de proteção de senha enviará os usuários para essa URL para que alterem suas senhas.

Se você desabilitar essa política ou não a configurar, o serviço de proteção de senha não redirecionará os usuários para uma URL de alteração de senha.

Essa política está disponível apenas em instâncias do Windows que façam parte de um domínio do Microsoft Active Directory, instâncias do Windows 10 Pro ou Enterprise registradas para o gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou associadas a um domínio via MCX.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PasswordProtectionChangePasswordURL
  - Nome da GP: Configurar a URL de alteração de senha
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Gerenciador de senhas e de proteção
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: PasswordProtectionChangePasswordURL
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"https://contoso.com/change_password.html"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PasswordProtectionChangePasswordURL
  - Exemplo de valor:
``` xml
<string>https://contoso.com/change_password.html</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PasswordProtectionLoginURLs
  #### Configurar a lista de URLs de logon corporativos onde o serviço de proteção por senha deve capturar os salted hashes de uma senha
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Configure a lista de URLs de logon corporativo (somente esquemas HTTP e HTTPS) em que Microsoft Edge devem capturar os salted hashes  das senhas e usá-lo para a detecção de reutilização de senha.

Se essa política estiver habilitada, o serviço de proteção por senha captura as impressões digitais das senhas nas URLs definidas.

Se você desabilitar essa política ou não a configurá-la, não serão capturadas impressões de senha.

Essa política estará disponível somente em instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, instâncias do Windows 10 Pro ou Enterprise que estejam inscritas no gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou associadas a um domínio via MCX.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PasswordProtectionLoginURLs
  - Nome da GP: Configurar a lista de URLs de logon corporativos onde o serviço de proteção por senha deve capturar os salted hashes de uma senha
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Gerenciador de senhas e de proteção
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\1 = "https://contoso.com/login.html"
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\2 = "https://login.contoso.com"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PasswordProtectionLoginURLs
  - Exemplo de valor:
``` xml
<array>
  <string>https://contoso.com/login.html</string>
  <string>https://login.contoso.com</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PasswordProtectionWarningTrigger
  #### Configurar gatilho de aviso de proteção de senha
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite que você controle o momento do disparo do aviso de proteção de senha. A proteção de senha alerta os usuários quando eles reutilizam senhas protegidas em sites potencialmente suspeitos.

Você pode usar as políticas [PasswordProtectionLoginURLs](#passwordprotectionloginurls) e [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl) para configurar as senhas que devem ser protegidas.

Isenções: senhas de sites listados nas políticas [PasswordProtectionLoginURLs](#passwordprotectionloginurls) e [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl), bem como aqueles listados nas políticas [SmartScreenAllowListDomains](#smartscreenallowlistdomains), não causarão o disparo do aviso de proteção de senha.

Defina "PasswordProtectionWarningOff" para não mostrar avisos de proteção de senha.

Defina "PasswordProtectionWarningOnPasswordReuse" para mostrar avisos de proteção de senha quando o usuário reutilizar senhas protegidas em sites listados como não permitidos.

Se você desabilitar ou não configurar essa política, o disparador de aviso não será mostrado.

Mapeamento das opções da política:

* PasswordProtectionWarningOff (0) = O aviso de proteção por senha está desativado

* PasswordProtectionWarningOnPasswordReuse (1) = O aviso de proteção por senha é acionado por reutilização de senha

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PasswordProtectionWarningTrigger
  - Nome da GP: Configurar gatilho de aviso de proteção de senha
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Gerenciador de senhas e de proteção
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: PasswordProtectionWarningTrigger
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PasswordProtectionWarningTrigger
  - Exemplo de valor:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ## Impressão policies

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultPrinterSelection
  #### Regras de seleção de impressora padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Substitui as regras de seleção de impressora padrão do Microsoft Edge. Essa política determina as regras para selecionar a impressora padrão no Microsoft Edge, o que acontece na primeira vez que um usuário tenta imprimir uma página.

Quando essa política é definida, o Microsoft Edge tenta encontrar uma impressora que corresponda a todos os atributos especificados, usando-a como impressora padrão. Se houver várias impressoras que atendem aos critérios, a primeira impressora correspondente será usada.

Se você não configurar essa política ou nenhuma impressora correspondente for encontrada dentro do tempo limite, a impressora usará como padrão a impressora PDF integrada ou nenhuma impressora, se a impressora PDF não estiver disponível.

O valor é analisado como um objeto JSON, em conformidade com o seguinte esquema: { "type": "object", "properties": { "idPattern": { "description": "Regular expression to match printer id.", "type": "string" }, "namePattern": { "description": "Regular expression to match printer display name.", "type": "string" } } }

A omissão de um campo significa que todos os valores são correspondentes; por exemplo, se você não especificar a conectividade, Visualizar Impressão começará a descobrir todos os tipos de impressoras locais. Os padrões de expressões regulares devem seguir a sintaxe JavaScript RegExp e as correspondências diferenciam maiúsculas de minúsculas.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultPrinterSelection
  - Nome da GP: Regras de seleção de impressora padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Impressão
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DefaultPrinterSelection
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"{ \"idPattern\": \".*public\", \"namePattern\": \".*Color\" }"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultPrinterSelection
  - Exemplo de valor:
``` xml
<string>{ "idPattern": ".*public", "namePattern": ".*Color" }</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PrintHeaderFooter
  #### Imprimir cabeçalhos e rodapés
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Aplique os cabeçalhos e rodapés para que sejam ativados ou desativados no diálogo de impressão.

Se você não configurar essa política, os usuários poderão decidir se serão impressos cabeçalhos e rodapés.

Se você desabilitar essa política, os usuários não poderão imprimir cabeçalhos e rodapés.

Se você habilitar essa política, os usuários sempre imprimirão cabeçalhos e rodapés.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PrintHeaderFooter
  - Nome da GP: Imprimir cabeçalhos e rodapés
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Impressão
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Impressão
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: PrintHeaderFooter
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PrintHeaderFooter
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PrintPreviewUseSystemDefaultPrinter
  #### Definir a impressora padrão do sistema como a impressora padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Informa ao Microsoft Edge para usar a impressora padrão do sistema como a opção padrão na Visualização de Impressão, em vez da impressora usada recentemente.

Se você desabilitar essa política ou não configurá-la, a Visualização de Impressão usará a impressora usada mais recentemente como a opção de destino padrão.

Se você habilitar essa política, a Visualização de Impressão usará a impressora padrão do sistema operacional como a opção de destino padrão.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PrintPreviewUseSystemDefaultPrinter
  - Nome da GP: Definir a impressora padrão do sistema como a impressora padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Impressão
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Impressão
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: PrintPreviewUseSystemDefaultPrinter
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PrintPreviewUseSystemDefaultPrinter
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PrintingEnabled
  #### Habilitar impressão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Habilita a impressão no Microsoft Edge e impede que os usuários alterem essa configuração.

Se você habilitar essa política ou não configurá-la, os usuários poderão imprimir.

Se você desabilitar essa política, os usuários não poderão imprimir usando o Microsoft Edge. A impressão está desabilitada no menu de ferramentas, extensões, aplicativos JavaScript e assim por diante. Os usuários ainda podem imprimir usando plug-ins que ignoram o Microsoft Edge durante a impressão. Por exemplo, alguns aplicativos Adobe Flash têm a opção de impressão em seu menu de contexto, o que não é coberto por essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PrintingEnabled
  - Nome da GP: Habilitar impressão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Impressão
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: PrintingEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PrintingEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PrintingPaperSizeDefault
  #### Tamanho da página de impressão padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Substituições do tamanho da página de impressão padrão.

name devem conter um dos formatos listados ou "personalizado" se o tamanho do papel necessário não estiver na lista. Se o valor "personalizado" for fornecido custom_size a propriedade deve ser especificada. Ela descreve a altura e a largura desejadas em micrometros. Caso contrário, a propriedade custom_size não deve ser especificada. As políticas que violem essas regras serão ignoradas.

Se o tamanho da página não estiver disponível na impressora escolhida pelo usuário essa política será ignorada.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Dicionário

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PrintingPaperSizeDefault
  - Nome da GP: Tamanho da página de impressão padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Impressão
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: PrintingPaperSizeDefault
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\PrintingPaperSizeDefault = {
  "custom_size": {
    "height": 297000, 
    "width": 210000
  }, 
  "name": "custom"
}
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PrintingPaperSizeDefault
  - Exemplo de valor:
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
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### UseSystemPrintDialog
  #### Imprimir usando a caixa de diálogo de impressão do sistema
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Mostra a caixa de diálogo de impressão do sistema, em vez da visualização de impressão.

Se você habilitar essa política, o Microsoft Edge abrirá a caixa de diálogo de impressão do sistema, em vez da visualização de impressão interna quando o usuário imprimir uma página.

Se você não configurar ou desabilitar essa política, os comandos de impressão acionarão a tela de visualização de impressão do Microsoft Edge.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: UseSystemPrintDialog
  - Nome da GP: Imprimir usando a caixa de diálogo de impressão do sistema
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Impressão
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: UseSystemPrintDialog
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: UseSystemPrintDialog
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ## Inicialização&comma; página inicial e página nova guia policies

  [Voltar ao início](#microsoft-edge---políticas)

  ### HomepageIsNewTabPage
  #### Definir a página nova guia como a home page
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Configura a home page padrão no Microsoft Edge. Você pode definir a home page como uma URL que você especificar ou como a página de nova guia.

Se você habilitar esta política, a página de nova guia será sempre usada para a home page, e a localização da URL da home page será ignorada.

Se você desabilitar esta política, a home page do usuário não poderá ser a página de nova guia, a menos que a URL seja definida como "edge://newtab".

Se ela não for configurada, os usuários poderão escolher se a página de nova guia é a sua home page.

Esta política está disponível apenas em instâncias do Windows que façam parte de um domínio do Microsoft Active Directory, instâncias do Windows 10 Pro ou Enterprise que estão registradas para o gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou associadas a um domínio via MCX..

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: HomepageIsNewTabPage
  - Nome da GP: Definir a página nova guia como a home page
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Inicialização, página inicial e página nova guia
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Inicialização, página inicial e página nova guia
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: HomepageIsNewTabPage
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: HomepageIsNewTabPage
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### HomepageLocation
  #### Configurar a URL da home page
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Configura a URL da home page padrão no Microsoft Edge.

A home page é a página aberta pelo botão Início. As páginas abertas na inicialização são controladas pelas políticas [RestoreOnStartup](#restoreonstartup).

Você pode definir uma URL aqui ou definir a home page para abrir a página de nova guia. Se você optar por abrir a página de nova guia, essa política não terá efeito.

Se você habilitar essa política, os usuários não poderão alterar a URL da home page, mas poderão optar por usar a página nova guia como home page.

Se você desabilitar ou não configurar essa política, os usuários poderão escolher sua própria home page, desde que a política [HomepageIsNewTabPage](#homepageisnewtabpage) não esteja habilitada.

Essa política está disponível somente em instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, em instâncias do Windows 10 Pro ou Enterprise registradas para o gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou associadas a um domínio via MCX..

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: HomepageLocation
  - Nome da GP: Configurar a URL da home page
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Inicialização, página inicial e página nova guia
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Inicialização, página inicial e página nova guia
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: HomepageLocation
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"https://www.contoso.com"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: HomepageLocation
  - Exemplo de valor:
``` xml
<string>https://www.contoso.com</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### NewTabPageAllowedBackgroundTypes
  #### Configurar os tipos de plano de fundo permitidos para o novo layout de página de guia
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Você pode configurar quais tipos de imagem de fundo são permitidas no layout da página nova guia no Microsoft Edge.

Se você não configurar essa política, todos os tipos de imagem de fundo na página nova guia serão habilitados.

Mapeamento das opções da política:

* DisableImageOfTheDay (1) = Desabilitar tipo de imagem de tela de fundo diária

* DisableCustomImage (2) = Desabilitar tipo de imagem de tela de fundo personalizada

* DisableAll (3) = Desabilitar todos os tipos de imagem de plano de fundo

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NewTabPageAllowedBackgroundTypes
  - Nome da GP: Configurar os tipos de plano de fundo permitidos para o novo layout de página de guia
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Inicialização, página inicial e página nova guia
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: NewTabPageAllowedBackgroundTypes
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NewTabPageAllowedBackgroundTypes
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### NewTabPageCompanyLogo
  #### Definir o logotipo da empresa da página Nova guia (obsoleto)
  
  >OBSOLETO: Essa política é obsoleta e não funciona após o Microsoft Edge 85.
  #### Versões com suporte:
  - No Windows e macOS desde 79, até 85

  #### Descrição
  Essa política não funcionou conforme o esperado devido a alterações nos requisitos operacionais. Portanto, ela é obsoleta e não deve ser usada.

Especifica o logotipo da empresa a ser usado na página nova guia no Microsoft Edge.

A política deve ser configurada como uma cadeia de caracteres que expressa o logotipo (s) no formato JSON. Por exemplo: { "default_logo": { "url": "https://www.contoso.com/logo.png", "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29" }, "light_logo": { "url": "https://www.contoso.com/light_logo.png", "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737" }}

Você configura essa política especificando a URL de onde Microsoft Edge pode baixar o logotipo e seu hash criptográfico (SHA-256), que é usado para verificar a integridade do download. O logotipo deve estar no formato PNG ou SVG, e o tamanho do arquivo não deve exceder 16 MB. O logotipo é baixado e armazenado em cache e será baixado sempre que a URL ou o hash for alterado. A URL deve estar acessível sem qualquer autenticação.

'default_logo' é necessário e será usado quando não houver nenhuma imagem de tela de fundo. Se 'light_logo' for fornecido, ele será usado quando a nova guia do usuário tiver uma imagem de tela de fundo. Recomendamos um logotipo horizontal com um plano de fundo transparente, alinhado à esquerda e centralizado verticalmente. O logotipo deve ter uma altura mínima de 32 pixels e uma taxa de proporção de 1:1 a 4:1. O 'default_logo' deve ter o contraste apropriado contra um plano de fundo branco ou preto, enquanto o 'light_logo' deve ter o contraste correto contra uma imagem de fundo.

se habilitar essa política, Microsoft Edge downloads e exibir os logotipos especificados na página nova guia. Os usuários não podem substituir nem ocultar os logotipos do.

Se você desabilitar ou não configurar essa política, Microsoft Edge não mostrará logotipo da empresa ou um logotipo da Microsoft na página nova guia.

Para obter ajuda na determinação do hash SHA-256, confira https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/get-filehash.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Dicionário

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NewTabPageCompanyLogo
  - Nome da GP: Definir o logotipo da empresa da página Nova guia (obsoleto)
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Inicialização, página inicial e página nova guia
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: NewTabPageCompanyLogo
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
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


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NewTabPageCompanyLogo
  - Exemplo de valor:
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
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### NewTabPageHideDefaultTopSites
  #### Ocultar os sites principais padrão da página de nova guia
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Oculta os sites principais padrão da página de nova guia no Microsoft Edge.

Se você definir essa política como true, os blocos do site principal padrão serão ocultos.

Se você definir essa política como false ou não configurá-la, os blocos dos sites principais padrão permanecerão visíveis.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NewTabPageHideDefaultTopSites
  - Nome da GP: Ocultar os sites principais padrão da página de nova guia
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Inicialização, página inicial e página nova guia
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: NewTabPageHideDefaultTopSites
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NewTabPageHideDefaultTopSites
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### NewTabPageLocation
  #### Configurar a URL da página de nova guia
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Configura a URL padrão para a página da nova guia.

Esta política determina a página que abrirá quando novas guias são criadas (inclusive quando novas janelas são abertas). Também afeta a página de inicialização se configurada para ser aberta na página da nova guia.

Esta política não determina qual página abrirá na inicialização. Isso é controlado pela política [RestoreOnStartup](#restoreonstartup). Também não afeta a página inicial se configurada para ser aberta na página da nova guia.

Se esta política não for configurada, a página da nova guia padrão será usada.

Se você configurar esta política *e* a política [NewTabPageSetFeedType](#newtabpagesetfeedtype), esta política terá prioridade.

Se uma URL inválida for fornecida, as novas guias abrirão about://blank.

Esta política está disponível somente em instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory em instâncias do Windows 10 Pro ou Enterprise registradas para o gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou associadas a um domínio via MCX..

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NewTabPageLocation
  - Nome da GP: Configurar a URL da página de nova guia
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Inicialização, página inicial e página nova guia
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Inicialização, página inicial e página nova guia
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: NewTabPageLocation
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"https://www.fabrikam.com"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NewTabPageLocation
  - Exemplo de valor:
``` xml
<string>https://www.fabrikam.com</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### NewTabPageManagedQuickLinks
  #### Definir links rápidos da página de nova guia
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 79 ou posterior

  #### Descrição
  Por padrão, o Microsoft Edge exibe links rápidos na página de nova guia de atalhos adicionados pelo usuário e sites principais com base no histórico de navegação. Com essa política, você pode configurar até três blocos de links rápidos na página da nova guia, expressos como um objeto JSON:

[ { "url": "https://www.contoso.com", "title": "Contoso Portal", "pinned": true/false }, ... ]

O campo "url" é obrigatório; "title" e "pinned" são opcionais. Se "title" não for preenchido, a URL será usada como o título padrão. Se "pinned" não for preenchido, o valor padrão será false.

O Microsoft Edge apresenta esses itens na ordem listada, da esquerda para a direita, com todos os blocos fixados exibidos à frente dos blocos não fixados.

Se a política estiver definida como obrigatória, o campo "pinned" será ignorado e todos os blocos serão fixados. Os blocos não poderão ser excluídos pelo usuário e sempre serão exibidos na frente da lista de links rápidos.

Se a política estiver definida como recomendada, os blocos fixados permanecerão na lista, mas o usuário poderá editá-los e excluí-los. Os blocos de links rápidos não fixados se comportam como sites principais padrão e são retirados da lista quando outros sites são visitados com mais frequência. Ao aplicar links não fixados por essa política a um perfil de navegador existente, os links podem não aparecer, dependendo de como são classificados em comparação ao histórico de navegação do usuário.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Dicionário

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NewTabPageManagedQuickLinks
  - Nome da GP: Definir links rápidos da página de nova guia
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Inicialização, página inicial e página nova guia
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Inicialização, página inicial e página nova guia
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: NewTabPageManagedQuickLinks
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
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


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NewTabPageManagedQuickLinks
  - Exemplo de valor:
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
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### NewTabPagePrerenderEnabled
  #### Habilitar o pré-carregamento da página de nova guia para renderização mais rápida
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 85 ou posterior

  #### Descrição
  Se você configurar essa política, o pré-carregamento da página Nova guia será habilitado e os usuários não poderão alterar essa configuração. Se você não configurar essa política, o pré-carregamento será habilitado e o usuário poderá alterar essa configuração.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NewTabPagePrerenderEnabled
  - Nome da GP: Habilitar o pré-carregamento da página de nova guia para renderização mais rápida
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Inicialização, página inicial e página nova guia
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Inicialização, página inicial e página nova guia
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: NewTabPagePrerenderEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NewTabPagePrerenderEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### NewTabPageSetFeedType
  #### Configurar a experiência de página de nova guia do Microsoft Edge
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 79 ou posterior

  #### Descrição
  Permite escolher a experiência de feed do Microsoft News ou do Office 365 para a página de nova guia.

Quando você definir essa política como "News", os usuários verão a experiência de feed do Microsoft News na página de nova guia.

Quando você definir essa política como "Office", os usuários com uma entrada do navegador do Azure Active Directory verão a experiência de feed do Office 365 na página de nova guia.

Se você desabilitar ou não configurar essa política:

- Os usuários com uma entrada do navegador do Azure Active Directory serão oferecidos a experiência de feed de página de nova guia do Office 365, bem como a experiência padrão de feed de página de nova guia.

- Os usuários sem uma entrada do navegador do Azure Active Directory verão a experiência padrão de página de nova guia.

Se você configurar essa política *e* a política [NewTabPageLocation](#newtabpagelocation), [NewTabPageLocation](#newtabpagelocation) terá prioridade.

Configuração padrão: desabilitada ou não configurada.

Mapeamento das opções da política:

* News (0) = Experiência de feed do Microsoft News

* Office (1) = Experiência de feed do Office 365

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NewTabPageSetFeedType
  - Nome da GP: Configurar a experiência de página de nova guia do Microsoft Edge
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Inicialização, página inicial e página nova guia
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Inicialização, página inicial e página nova guia
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: NewTabPageSetFeedType
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NewTabPageSetFeedType
  - Exemplo de valor:
``` xml
<integer>0</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### RestoreOnStartup
  #### Ação a ser executada na inicialização
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifique como o Microsoft Edge deve se comportar quando for iniciado.

Se você quiser que uma nova guia sempre abra na inicialização, escolha "RestoreOnStartupIsNewTabPage" .

Se você quiser reabrir URLs que estavam abertas na última vez em que o Microsoft Edge foi fechado, escolha "RestoreOnStartupIsLastSession". A sessão de navegação será restaurada como estava. Observe que essa opção desabilita algumas configurações que dependem de sessões ou que executem ações na saída (como Limpar dados de navegação ao sair ou cookies somente da sessão).

Se você deseja abrir um conjunto específico de URLs, escolha "RestoreOnStartupIsURLs".

Desabilitar essa configuração é o equivalente a deixá-la não configurada. Os usuários poderão alterá-la no Microsoft Edge.

Essa política está disponível apenas em instâncias do Windows que façam parte de um domínio do Microsoft Active Directory, Windows 10 Pro ou Enterprise registradas para o gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou associadas a um domínio via MCX.

Mapeamento das opções da política:

* RestoreOnStartupIsNewTabPage (5) = Abrir uma nova guia

* RestoreOnStartupIsLastSession (1) = Restaurar a última sessão

* RestoreOnStartupIsURLs (4) = Abrir uma lista de URLs

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: RestoreOnStartup
  - Nome da GP: Ação a ser executada na inicialização
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Inicialização, página inicial e página nova guia
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Inicialização, página inicial e página nova guia
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: RestoreOnStartup
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000004
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: RestoreOnStartup
  - Exemplo de valor:
``` xml
<integer>4</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### RestoreOnStartupURLs
  #### Sites a serem abertos quando o navegador for iniciado
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifique uma lista de sites para abrir automaticamente quando o navegador for iniciado. Se você não configurar esta política, nenhum site será aberto na inicialização.

   Esta política só funcionará se você também definir a [RestoreOnStartup](#restoreonstartup) política como "Abrir uma lista de URLs" (4).

Esta política só estará disponível em instâncias do Windows que fazem parte de um Microsoft Active Directory domínio, instâncias do Windows 10 Pro ou Enterprise que inscritas no gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou associadas a um domínio via MCX.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: RestoreOnStartupURLs
  - Nome da GP: Sites a serem abertos quando o navegador for iniciado
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Inicialização, página inicial e página nova guia
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Inicialização, página inicial e página nova guia
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações\RestoreOnStartupURLs
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\1 = "https://contoso.com"
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\2 = "https://www.fabrikam.com"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: RestoreOnStartupURLs
  - Exemplo de valor:
``` xml
<array>
  <string>https://contoso.com</string>
  <string>https://www.fabrikam.com</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ShowHomeButton
  #### Mostrar botão Início na barra de ferramentas
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Mostra o botão Início na barra de ferramentas do Microsoft Edge.

Habilite esta política para sempre mostrar o botão Início. Desabilite-a para nunca mostrar o botão.

Se você não configurar a política, os usuários poderão optar por mostrar o botão Início.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ShowHomeButton
  - Nome da GP: Mostrar botão Início na barra de ferramentas
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Inicialização, página inicial e página nova guia
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Inicialização, página inicial e página nova guia
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: ShowHomeButton
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ShowHomeButton
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ## Mensagens nativas policies

  [Voltar ao início](#microsoft-edge---políticas)

  ### NativeMessagingAllowlist
  #### Controlar quais hosts de mensagens nativas os usuários podem usar
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Liste os hosts de mensagens nativas específicos que os usuários podem usar no Microsoft Edge.

Por padrão, todos os hosts de mensagens nativas são permitidos. Se você definir a política [NativeMessagingBlocklist](#nativemessagingblocklist) como *, todos os hosts de mensagens nativas serão bloqueados, e somente hosts de mensagens nativos listados aqui serão carregados.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NativeMessagingAllowlist
  - Nome da GP: Controlar quais hosts de mensagens nativas os usuários podem usar
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Mensagens nativas
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\2 = "com.native.messaging.host.name2"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NativeMessagingAllowlist
  - Exemplo de valor:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### NativeMessagingBlocklist
  #### Configurar lista de contatos bloqueados de mensagens nativas
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica quais hosts de mensagens nativas não devem ser usados.

Use "*" para bloquear todos os hosts de mensagens nativas, a menos que estejam explicitamente listados na lista de permissões.

Se você não configurar essa política, o Microsoft Edge carregará todos os hosts de mensagens nativas instalados.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NativeMessagingBlocklist
  - Nome da GP: Configurar lista de contatos bloqueados de mensagens nativas
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Mensagens nativas
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\2 = "com.native.messaging.host.name2"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NativeMessagingBlocklist
  - Exemplo de valor:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### NativeMessagingUserLevelHosts
  #### Permitir hosts de mensagens nativas no nível de usuário (instalado sem permissões de administrador)
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite a instalação em nível de usuário de hosts de mensagens nativas.

Se você desabilitar essa política, o Microsoft Edge usará somente hosts de mensagens nativas instalados no nível do sistema.

Por padrão, se você não configurar essa política, o Microsoft Edge permitirá o uso de hosts de mensagens nativas no nível de usuário.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NativeMessagingUserLevelHosts
  - Nome da GP: Permitir hosts de mensagens nativas no nível de usuário (instalado sem permissões de administrador)
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Mensagens nativas
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: NativeMessagingUserLevelHosts
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NativeMessagingUserLevelHosts
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ## Provedor de pesquisa padrão policies

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultSearchProviderEnabled
  #### Habilitar o provedor de pesquisa padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite o uso de um provedor de pesquisa padrão.

Se você habilitar essa política, um usuário poderá pesquisar um termo digitando na barra de endereço (desde que o que ele digite não seja uma URL).

Você pode especificar o provedor de pesquisa padrão a ser usado, habilitando o restante das políticas de pesquisa padrão. Se estas forem deixadas vazias (não configuradas), o usuário poderá escolher o provedor padrão.

Se você desabilitar essa política, o usuário não poderá pesquisar na barra de endereço.

Se você habilitar ou desabilitar essa política, os usuários não poderão alterá-la ou substituí-la.

Se você não configurar essa política, o provedor de pesquisa padrão será habilitado e o usuário poderá escolher o provedor de pesquisa padrão e definir a lista de provedores de pesquisa.

Essa política está disponível apenas em instâncias do Windows que ingressaram em um domínio do Microsoft Active Directory em instâncias do Windows 10 Pro ou Enterprise registradas para o gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou associadas a um domínio via MCX..

A partir do Microsoft Edge 84, você pode definir esta política como uma política recomendada.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultSearchProviderEnabled
  - Nome da GP: Habilitar o provedor de pesquisa padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Provedor de pesquisa padrão
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: DefaultSearchProviderEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSearchProviderEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultSearchProviderEncodings
  #### Codificações do provedor de pesquisa padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica a codificação de caractere suportado pelo provedor de busca. Codificações são nomes da página de código como UTF-8, GB2312 e ISO-8859-1. Eles são testados na ordem fornecida.

Essa política é opcional. Se não for configurada, o padrão UTF-8 será usado.

Essa política será aplicada somente se você habilitar as políticas de [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir de Microsoft Edge 84, você pode definir essa política como uma política recomendada. Se o usuário já tiver definido um provedor de pesquisa padrão, o provedor de pesquisa padrão configurado por essa política recomendada não será adicionado à lista de provedores de pesquisa para a escolha do usuário. Se esse for o comportamento desejado, use a política de [ManagedSearchEngines](#managedsearchengines).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultSearchProviderEncodings
  - Nome da GP: Codificações do provedor de pesquisa padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Provedor de pesquisa padrão
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações\DefaultSearchProviderEncodings
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\1 = "UTF-8"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\2 = "UTF-16"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\3 = "GB2312"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\4 = "ISO-8859-1"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSearchProviderEncodings
  - Exemplo de valor:
``` xml
<array>
  <string>UTF-8</string>
  <string>UTF-16</string>
  <string>GB2312</string>
  <string>ISO-8859-1</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultSearchProviderImageURL
  #### Especifica o recurso de pesquisa por imagem para o provedor de pesquisa padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica a URL para o mecanismo de pesquisa usado na pesquisa de imagem. As solicitações de pesquisa são enviadas pelo método GET.

Essa política é opcional. Se você não configurá-la, a pesquisa de imagem não estará disponível.

Especifique a URL de Pesquisa de Imagem do Bing como:
 "{bing:baseURL}images/detail/search?iss=sbiupload&FORM=ANCMS1#enterInsights".

Especifique a URL de Pesquisa de Imagem do Google: "{google:baseURL}searchbyimage/upload".

Consulte a política de [DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams) para concluir a configuração da pesquisa de imagem.

Essa política é aplicada somente ao habilitar as políticas de [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir de Microsoft Edge 84, você pode definir esta política como política recomendada. Se o usuário já tiver definido um provedor de pesquisa padrão, o provedor de pesquisa padrão configurado por essa política recomendada não será adicionado à lista de provedores de pesquisa para a escolha do usuário. Se esse for o comportamento desejado, use a política de [ManagedSearchEngines](#managedsearchengines).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultSearchProviderImageURL
  - Nome da GP: Especifica o recurso de pesquisa por imagem para o provedor de pesquisa padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Provedor de pesquisa padrão
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: DefaultSearchProviderImageURL
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"https://search.contoso.com/searchbyimage/upload"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSearchProviderImageURL
  - Exemplo de valor:
``` xml
<string>https://search.contoso.com/searchbyimage/upload</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultSearchProviderImageURLPostParams
  #### Parâmetros para uma URL de imagem que usa POST
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Se habilitar esta política, ela especificará os parâmetros usados quando uma pesquisa de imagem que usa POST for realizada. A política consiste em partes de nome/valor separados por vírgula. Se um valor for um parâmetro de modelo, como {imageThumbnail} no exemplo anterior, ele será substituído por dados reais de miniatura da imagem. Esta política é aplicada somente ao habilitar as políticas de [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

Especifique os Parâmetros POST da URL de Pesquisa de Imagem do Bing como:
"imageBin={google:imageThumbnailBase64}".

Especifique os Parâmetros POST da URL de Pesquisa de Imagem do Google como:
"encoded_image={google:imageThumbnail},image_url={google:imageURL},sbisrc={google:imageSearchSource},original_width={google:imageOriginalWidth},original_height={google:imageOriginalHeight}".

Se não configurar esta política, as solicitações de pesquisa de imagem serão enviadas pelo método GET.

A partir de Microsoft Edge 84, você pode definir esta política como uma política recomendada. Se o usuário já tiver definido um provedor de pesquisa padrão, o provedor de pesquisa padrão configurado por esta política recomendada não será adicionado à lista de provedores de pesquisa para a escolha do usuário. Se esse for o comportamento desejado, use a política de [ManagedSearchEngines](#managedsearchengines).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultSearchProviderImageURLPostParams
  - Nome da GP: Parâmetros para uma URL de imagem que usa POST
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Provedor de pesquisa padrão
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: DefaultSearchProviderImageURLPostParams
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"content={imageThumbnail},url={imageURL},sbisrc={SearchSource}"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSearchProviderImageURLPostParams
  - Exemplo de valor:
``` xml
<string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultSearchProviderKeyword
  #### Palavra-chave do provedor de pesquisa padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica a palavra-chave, que é o atalho usado na barra de endereços para acionar a pesquisa deste provedor.

Essa política é opcional. Se não configurá-la, nenhuma palavra-chave ativará o provedor de pesquisa.

Essa política será aplicada somente se você habilitar as políticas[DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir de Microsoft Edge 84, você pode definir essa política como uma política recomendada. Se o usuário já tiver definido um provedor de pesquisa padrão, o provedor de pesquisa padrão configurado por essa política recomendada não será adicionado à lista de provedores de pesquisa para a escolha do usuário. Se esse for o comportamento desejado, use a política de [ManagedSearchEngines](#managedsearchengines).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultSearchProviderKeyword
  - Nome da GP: Palavra-chave do provedor de pesquisa padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Provedor de pesquisa padrão
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: DefaultSearchProviderKeyword
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"mis"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSearchProviderKeyword
  - Exemplo de valor:
``` xml
<string>mis</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultSearchProviderName
  #### Nome do provedor de pesquisa padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica o nome do provedor de pesquisa padrão.

Se você habilitar essa política, o nome do provedor de pesquisa padrão será definido.

Se você não habilitar essa política ou deixá-la vazia, o nome do host especificado pela URL de pesquisa será usado.

[DefaultSearchProviderName](#defaultsearchprovidername) deve ser definida como um provedor de pesquisa criptografado aprovado pela organização que corresponde ao provedor de pesquisa criptografado definido em DTBC-0008. Essa política é aplicada somente quando você habilita as políticas de [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir de Microsoft Edge 84, você pode definir esta política como uma política recomendada. Se o usuário já tiver definido um provedor de pesquisa padrão, o provedor de pesquisa padrão configurado por essa política recomendada não será adicionado à lista de provedores de pesquisa para a escolha do usuário. Se esse for o comportamento desejado, use a política de [ManagedSearchEngines](#managedsearchengines).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultSearchProviderName
  - Nome da GP: Nome do provedor de pesquisa padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Provedor de pesquisa padrão
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: DefaultSearchProviderName
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"My Intranet Search"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSearchProviderName
  - Exemplo de valor:
``` xml
<string>My Intranet Search</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultSearchProviderSearchURL
  #### URL de pesquisa do provedor de pesquisa padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica a URL do mecanismo de pesquisa usado para uma pesquisa padrão. A URL contém a cadeia de caracteres  "{searchTerms}", que é substituída no momento da consulta pelos termos que o usuário está pesquisando.

 Especifique a URL de pesquisa do Bing como:

 "{bing:baseURL}search?q={searchTerms}".

Especifique a URL de pesquisa do Google como: "{google:baseURL}search?q={searchTerms}&{google:RLZ}{google:originalQueryForSuggestion}{google:assistedQueryStats}{google:searchFieldtrialParameter}{google:searchClient}{google:sourceId}ie={inputEncoding}".

 Essa política é necessária ao ativar a política do[DefaultSearchProviderEnabled](#defaultsearchproviderenabled); se você não habilitar a última política, essa política será ignorada.

  A partir de Microsoft Edge 84, você pode definir esta política como política recomendada. Se o usuário já tiver definido um provedor de pesquisa padrão, o provedor de pesquisa padrão configurado por essa política recomendada não será adicionado à lista de provedores de pesquisa para a escolha do usuário. Se esse for o comportamento desejado, use a política de [ManagedSearchEngines](#managedsearchengines).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultSearchProviderSearchURL
  - Nome da GP: URL de pesquisa do provedor de pesquisa padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Provedor de pesquisa padrão
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: DefaultSearchProviderSearchURL
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"https://search.contoso.com/search?q={searchTerms}"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSearchProviderSearchURL
  - Exemplo de valor:
``` xml
<string>https://search.contoso.com/search?q={searchTerms}</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultSearchProviderSuggestURL
  #### URL do provedor de pesquisa padrão para sugestões
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica a URL do mecanismo de pesquisa usado para fornecer sugestões de pesquisa. A URL contém a cadeia de caracteres "{searchTerms}", que é substituída no momento da consulta pelo texto que o usuário inseriu até o momento.

Essa política é opcional. Se você não configurá-la, os usuários não verão sugestões de pesquisa. Eles verão sugestões do histórico de navegação e favoritos.

A URL de sugestão do Bing pode ser especificada como:

"{bing:baseURL}qbox?query={searchTerms}".

A URL de sugestão do Google pode ser especificada como: "{google:baseURL}complete/search?output=chrome&q={searchTerms}".

Essa política é aplicada somente quando você habilita as políticas [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

A partir de Microsoft Edge 84, você pode definir esta política como uma política recomendada. Se o usuário já tiver definido um provedor de pesquisa padrão, o provedor de pesquisa padrão configurado por essa política recomendada não será adicionado à lista de provedores de pesquisa para a escolha do usuário. Se esse for o comportamento desejado, use a política de [ManagedSearchEngines](#managedsearchengines).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultSearchProviderSuggestURL
  - Nome da GP: URL do provedor de pesquisa padrão para sugestões
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Provedor de pesquisa padrão
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: DefaultSearchProviderSuggestURL
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"https://search.contoso.com/suggest?q={searchTerms}"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSearchProviderSuggestURL
  - Exemplo de valor:
``` xml
<string>https://search.contoso.com/suggest?q={searchTerms}</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### NewTabPageSearchBox
  #### Configurar a nova experiência de caixa de pesquisa da página da guia
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 85 ou posterior

  #### Descrição
  Você pode configurar a caixa de pesquisa nova guia da página para usar "Caixa de pesquisa (Recomendada)" ou "Barra de endereços" para pesquisar em novas guias. Esta política só funcionará se você definir o mecanismo de pesquisa para um valor diferente do Bing, definindo as duas políticas a seguir: [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

  Se você desabilitar ou não configurar esta política e:

  - Se o mecanismo de pesquisa padrão da barra de endereços for Bing, a página nova guia usará a caixa de pesquisa para pesquisar em novas guias.
- Se o mecanismo de pesquisa padrão da barra de endereços não for Bing, os usuários receberão uma escolha adicional (use "Barra de endereços") ao pesquisar em novas guias.


  Se você habilitar essa política e defini-la como:

  - "Caixa de pesquisa (Recomendada)" ('Bing'), a página da nova guia usa a caixa de pesquisa para pesquisar em novas guias.
 - "Barra de endereços" ('redirecionar'), a caixa de pesquisa da nova guia usa a barra de endereços para pesquisar em novas guias.

Mapeamento das opções da política:

* bing (bing) = Caixa de pesquisa (recomendado)

* redirect (redirect) = Barra de endereços

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NewTabPageSearchBox
  - Nome da GP: Configurar a nova experiência de caixa de pesquisa da página da guia
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Provedor de pesquisa padrão
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/Provedor de pesquisa padrão
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: NewTabPageSearchBox
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"bing"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NewTabPageSearchBox
  - Exemplo de valor:
``` xml
<string>bing</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ## Servidor proxy policies

  [Voltar ao início](#microsoft-edge---políticas)

  ### ProxyBypassList
  #### Configurar regras para ignorar o proxy
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define uma lista de organizadores que Microsoft Edge ignoram qualquer proxy.

Esta política será aplicada apenas se você tiver selecionado “Usar servidores proxy fixos” na  [ProxyMode](#proxymode) política. Se você selecionou outro modo para configurar políticas de proxy, não ative ou configure esta política.

Se você habilitar esta política, poderá criar uma lista de organizadores que  Microsoft Edge usam um proxy.

Se você não configurar esta política, nenhuma lista de organizadores será criada que  Microsoft Edge ignorará um proxy. Deixe esta política desconfigurada se você especificou outro método para definir políticas de proxy.

Para obter mais exemplos detalhados, consulte: [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ProxyBypassList
  - Nome da GP: Configurar regras para ignorar o proxy
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Servidor proxy
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ProxyBypassList
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"https://www.contoso.com, https://www.fabrikam.com"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ProxyBypassList
  - Exemplo de valor:
``` xml
<string>https://www.contoso.com, https://www.fabrikam.com</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ProxyMode
  #### Definir configurações de servidor proxy
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifique as configurações do servidor proxy usadas pelo Microsoft Edge. Se você habilitar essa política, os usuários não podem alterar as configurações de proxy.

Se você optar por nunca usar um servidor proxy e sempre conectar-se diretamente, todas as outras opções serão ignoradas.

Se você optar por usar as configurações de proxy do sistema, todas as outras opções serão ignoradas.

Se você optar por detectar automaticamente o servidor proxy, todas as outras opções serão ignoradas.

Se você optar pelo modo fixo de servidor proxy, poderá especificar outras opções em [ProxyServer](#proxyserver) e "Lista separada por vírgulas de regras para ignorar o proxy".

Se você optar por usar um script de proxy do .pac, você deve especificar a URL para o script "URL para um arquivo .pac de proxy".

Para obter exemplos detalhados, vá para [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

Se você habilitar essa política, o Microsoft Edge ignorará todas as opções relacionadas ao proxy especificadas na linha de comando.

Se você não configurar essa política, os usuários poderão escolher suas próprias configurações de proxy.

Mapeamento das opções da política:

* ProxyDisabled (direct) = Nunca usar um proxy

* ProxyAutoDetect (auto_detect) = Detectar as configurações de proxy automaticamente

* ProxyPacScript (pac_script) = Usar um script de proxy do .pac

* ProxyFixedServers (fixed_servers) = Usar servidores proxy fixo

* ProxyUseSystem (system) = Usar configurações de proxy do sistema

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ProxyMode
  - Nome da GP: Definir configurações de servidor proxy
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Servidor proxy
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ProxyMode
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"direct"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ProxyMode
  - Exemplo de valor:
``` xml
<string>direct</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ProxyPacUrl
  #### Definir a URL do arquivo .pac do proxy
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica a URL de um arquivo de configuração automática do proxy (PAC).

Essa política será aplicada somente se você tiver selecionado "Usar um script de proxy .pac" na política [ProxyMode](#proxymode). Se você tiver selecionado qualquer outro modo para configurar as políticas de proxy, não habilite ou configure essa política.

Se você habilitar essa política, poderá especificar a URL de um arquivo PAC, que define como o navegador escolherá automaticamente o servidor proxy apropriado para buscar um site específico.

Se você desabilitar ou não configurar essa política, nenhum arquivo PAC será especificado. Deixe essa política não configurada se você tiver especificado qualquer outro método para definir políticas de proxy.

Para obter exemplos detalhados, consulte [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ProxyPacUrl
  - Nome da GP: Definir a URL do arquivo .pac do proxy
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Servidor proxy
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ProxyPacUrl
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"https://internal.contoso.com/example.pac"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ProxyPacUrl
  - Exemplo de valor:
``` xml
<string>https://internal.contoso.com/example.pac</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ProxyServer
  #### Configurar o endereço ou a URL do servidor proxy
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica a URL do servidor proxy.

   Esta política será aplicada apenas se você tiver selecionado a opção "Usar servidores de proxy fixos" na [ProxyMode](#proxymode) política. Se você tiver selecionado qualquer outro modo para configurar as políticas de proxy, não habilite ou configure esta política.

Se você habilitar esta política, o servidor proxy configurado por esta política será usado para todas as URLs.

Se você desabilitar ou não configurar esta política, os usuários poderão escolher suas próprias configurações de proxy enquanto estiverem neste modo de proxy. Deixe esta política desconfigurada se você tiver especificado qualquer outro método para a configuração das políticas de proxy.

Para obter mais opções e exemplos detalhados, consulte: [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ProxyServer
  - Nome da GP: Configurar o endereço ou a URL do servidor proxy
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Servidor proxy
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ProxyServer
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"123.123.123.123:8080"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ProxyServer
  - Exemplo de valor:
``` xml
<string>123.123.123.123:8080</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ProxySettings
  #### Configurações de proxy
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define as configurações de proxy para o Microsoft Edge.

Se você habilitar essa política, o Microsoft Edge ignorará todas as opções relacionadas ao proxy especificadas na linha de comando.

Se você não configurar essa política, os usuários poderão escolher suas próprias configurações de proxy.

Essa política substitui as seguintes políticas individuais:

[ProxyMode](#proxymode)
[ProxyPacUrl](#proxypacurl)
[ProxyServer](#proxyserver)
[ProxyBypassList](#proxybypasslist)

O campo ProxyMode permite especificar o servidor proxy usado pelo Microsoft Edge e impede que os usuários alterem as configurações do proxy.

O campo ProxyPacUrl é uma URL para um arquivo .pac do proxy.

O campo ProxyServer é uma URL do servidor proxy.

O campo ProxyBypassList é uma lista de hosts proxy que o Microsoft Edge ignora.

Se você escolher o valor "direct" como [ProxyMode](#proxymode), um proxy nunca será usado e todos os outros campos serão ignorados.

Se você escolher o valor "system" como [ProxyMode](#proxymode), o proxy do sistema será usado e todos os outros campos serão ignorados.

Se você escolher o valor "auto_detect" como [ProxyMode](#proxymode), todos os outros campos serão ignorados.

Se você escolher o valor "fixed_server" como [ProxyMode](#proxymode), os campos [ProxyServer](#proxyserver) e [ProxyBypassList](#proxybypasslist) serão usados.

Se você escolher o valor "pac_script" como [ProxyMode](#proxymode), os campos [ProxyPacUrl](#proxypacurl) e [ProxyBypassList](#proxybypasslist) serão usados.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Dicionário

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ProxySettings
  - Nome da GP: Configurações de proxy
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/Servidor proxy
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ProxySettings
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {
  "ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", 
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ProxySettings
  - Exemplo de valor:
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
  

  [Voltar ao início](#microsoft-edge---políticas)

  ## Additional policies

  [Voltar ao início](#microsoft-edge---políticas)

  ### AddressBarMicrosoftSearchInBingProviderEnabled
  #### Habilitar sugestões da Pesquisa da Microsoft no Bing na barra de endereços
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 81 ou posterior

  #### Descrição
  Habilita a exibição de sugestões relevantes da Pesquisa da Microsoft no Bing na lista de sugestões da barra de endereços quando o usuário digitar uma cadeia de caracteres de pesquisa na barra de endereços. Se você habilitar ou não configurar essa política, os usuários poderão ver resultados internos da plataforma de Pesquisa da Microsoft no Bing na lista de sugestões da barra de endereços do Microsoft Edge. Para ver os resultados da Pesquisa da Microsoft no Bing, o usuário deve entrar no Microsoft Edge com a conta do Azure AD para essa organização.
Se você desabilitar essa política, os usuários não poderão ver resultados internos na lista de sugestões da barra de endereços do Microsoft Edge.
Se você habilitou o conjunto de políticas que força um provedor de pesquisa padrão ([DefaultSearchProviderEnabled](#defaultsearchproviderenabled), [DefaultSearchProviderName](#defaultsearchprovidername) e [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)), e o provedor de pesquisa especificado não é o Bing, essa política não é aplicável e não haverá sugestões da Pesquisa da Microsoft no Bing na lista de sugestões da barra de endereços.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AddressBarMicrosoftSearchInBingProviderEnabled
  - Nome da GP: Habilitar sugestões da Pesquisa da Microsoft no Bing na barra de endereços
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AddressBarMicrosoftSearchInBingProviderEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AddressBarMicrosoftSearchInBingProviderEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AdsSettingForIntrusiveAdsSites
  #### Configuração de anúncios para sites com anúncios intrusivos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 78 ou posterior

  #### Descrição
  Controla se os anúncios estão bloqueados em sites com anúncios invasivos.

Mapeamento das opções da política:

* AllowAds (1) = Permitir anúncios em todos os sites

* BlockAds (2) = Bloquear anúncios em sites com anúncios intrusivos. (Valor padrão)

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AdsSettingForIntrusiveAdsSites
  - Nome da GP: Configuração de anúncios para sites com anúncios intrusivos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AdsSettingForIntrusiveAdsSites
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AdsSettingForIntrusiveAdsSites
  - Exemplo de valor:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AllowDeletingBrowserHistory
  #### Habilitar a exclusão do navegador e do histórico de download
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Habilita a exclusão do histórico do navegador e do histórico de downloads e impede que os usuários alterem essa configuração.

Observe que, mesmo com essa política desabilitada, a retenção do histórico de navegação e download não é garantida: os usuários podem editar ou excluir os arquivos do banco de dados do histórico diretamente, e o próprio navegador pode remover (com base no período de expiração) ou arquivar alguns ou todos itens de histórico a qualquer momento.

Se você habilitar essa política ou não configurá-la, os usuários poderão excluir o histórico de navegação e download.

Se você desabilitar essa política, os usuários não poderão excluir o histórico de navegação e download.

Se você habilitar essa política, não habilite a política [ClearBrowsingDataOnExit](#clearbrowsingdataonexit), pois ambas lidam com a exclusão de dados. Se você habilitar as duas, a política [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) terá precedência e excluirá todos os dados quando o Microsoft Edge for fechado, independentemente de como essa política estiver configurada.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AllowDeletingBrowserHistory
  - Nome da GP: Habilitar a exclusão do navegador e do histórico de download
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AllowDeletingBrowserHistory
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AllowDeletingBrowserHistory
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AllowFileSelectionDialogs
  #### Permitir caixas de diálogo de seleção de arquivos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Conceda acesso a arquivos locais permitindo que o Microsoft Edge exiba caixas de diálogo de seleção de arquivos

Se você habilitar ou não configurar essa política, os usuários poderão abrir caixas de diálogo de seleção de arquivos normalmente.

Se você desabilitar essa política, sempre que o usuário executar uma ação que dispare uma caixa de diálogo de seleção de arquivos (como importar favoritos, carregar arquivos ou salvar links), será exibida uma mensagem, e presume-se que o usuário clicou em Cancelar na caixa de diálogo de seleção de arquivos.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AllowFileSelectionDialogs
  - Nome da GP: Permitir caixas de diálogo de seleção de arquivos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AllowFileSelectionDialogs
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AllowFileSelectionDialogs
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AllowPopupsDuringPageUnload
  #### Permite que uma página mostre pop-ups durante seu descarregamento
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 78 ou posterior

  #### Descrição
  Essa política permite que um administrador especifique que uma página pode mostrar pop-ups durante seu descarregamento.

Quando a política está configurada como habilitada, as páginas podem mostrar pop-ups enquanto estão sendo descarregadas.

Quando a política está configurada como desabilitada ou não está configurada, as páginas não podem mostrar pop-ups enquanto estão sendo descarregadas, de acordo com a especificação: (https://html.spec.whatwg.org/#apis-for-creating-and-navigating-browsing-contexts-by-name).

Esta política será removida no futuro.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AllowPopupsDuringPageUnload
  - Nome da GP: Permite que uma página mostre pop-ups durante seu descarregamento
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AllowPopupsDuringPageUnload
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AllowPopupsDuringPageUnload
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AllowSurfGame
  #### Permitir jogo de surfe
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 83 ou posterior

  #### Descrição
  Se você desativar esta política, os usuários não poderão jogar o jogo de surf quando o dispositivo estiver off-line ou se o usuário navegar até a edge://surf.

Se você ativar ou não configurar esta política, os usuários poderão jogar o jogo de surf.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AllowSurfGame
  - Nome da GP: Permitir jogo de surfe
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AllowSurfGame
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AllowSurfGame
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AllowSyncXHRInPageDismissal
  #### Permitir que as páginas enviem solicitações XHR síncronas durante o descarte de páginas (preterida)
  >PRETERIDA: essa política foi preterida. No momento, ela tem suporte, mas ficará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - Em Windows e macOS desde 79 ou posterior

  #### Descrição
  Essa política foi preterida porque destina-se a ser um mecanismo de curto prazo para dar mais tempo para que as empresas atualizem o conteúdo da Web se e quando ela for incompatível com a alteração para não permitir solicitações XHR síncronas durante a descarte da página. Ele não funcionará na versão 88 do Microsoft Edge.

Essa política permite especificar que uma página pode enviar solicitações XHR síncronas durante a transmissão de página.

Se você habilitar essa política, as páginas poderão enviar solicitações XHR síncronas durante descarte de páginas.

Se você desabilitar essa política ou não configurar essa política, não será possível enviar solicitações de XHR síncronos durante a descarte de páginas.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AllowSyncXHRInPageDismissal
  - Nome da GP: Permitir que as páginas enviem solicitações XHR síncronas durante o descarte de páginas (preterida)
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AllowSyncXHRInPageDismissal
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AllowSyncXHRInPageDismissal
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AllowTokenBindingForUrls
  #### Configurar a lista de sites que o Microsoft Edge tentará estabelecer uma ligação de token com
  
  
  #### Versões com suporte:
  - No Windows desde a versão 83 ou posterior

  #### Descrição
  Configure a lista de padrões de URL para sites com os quais o navegador tentará executar o protocolo de Ligação de Token.
Para os domínios nesta lista, o navegador enviará a Ligação de Token ClientHello no handshake de TLS (confira https://tools.ietf.org/html/rfc8472).
Se o servidor responder com uma resposta ServerHello válida, o navegador criará e enviará mensagens de Ligação de Token nas solicitações https subsequentes. Confira https://tools.ietf.org/html/rfc8471 para obter mais informações.

Se esta lista estiver vazia, a Ligação de Token será desabilitada.

Esta política está disponível apenas em dispositivos Windows 10 com recurso Modo Seguro Virtual.

A partir do Microsoft Edge 86, essa política não oferece mais suporte à atualização dinâmica.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AllowTokenBindingForUrls
  - Nome da GP: Configurar a lista de sites que o Microsoft Edge tentará estabelecer uma ligação de token com
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\2 = "[*.]mydomain2.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\3 = "[*.].mydomain2.com"

```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AllowTrackingForUrls
  #### Configurar exceções de prevenção de rastreamento para sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 78 ou posterior

  #### Descrição
  Configure a lista de padrões de URL que são excluídos da prevenção de rastreamento.

Se você configurar essa política, a lista de padrões de URL configurados será excluída da prevenção de rastreamento.

Se você não configurar essa política, o valor padrão global da política "Bloquear rastreamento de usuários" (se definida), ou a configuração pessoal do usuário será usada para todos os sites.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AllowTrackingForUrls
  - Nome da GP: Configurar exceções de prevenção de rastreamento para sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AllowTrackingForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AlternateErrorPagesEnabled
  #### Sugerir páginas similares quando uma página da Web não for encontrada
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 80 ou posterior

  #### Descrição
  Permita que o Microsoft Edge emita uma conexão com um serviço Web para gerar sugestões de pesquisa e URL para problemas de conectividade, como erros de DNS.

Se você habilitar esta política, um serviço Web será usado para gerar sugestões de pesquisa e URL para erros de rede.

Se você desabilitar esta política, nenhuma chamada para o serviço Web será feita, e uma página de erro padrão será exibida.

Se você não configurar esta política, o Microsoft Edge respeitará a preferência do usuário definida em Serviços, em edge://settings/privacy.
Especificamente, há o botão de alternância “Sugerir páginas similares quando uma página da Web não for encontrada”, que o usuário pode ativar ou desativar. Observe que, se você habilitar esta política (AlternateErrorPagesEnabled), a configuração Sugerir páginas similares quando uma página da Web não for encontrada será ativada, mas o usuário não poderá alterar a configuração usando o botão de alternância. Se você desabilitar esta política, a configuração Sugerir páginas similares quando uma página da Web não for encontrada será desativada, e o usuário não poderá alterar a configuração usando o botão de alternância.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AlternateErrorPagesEnabled
  - Nome da GP: Sugerir páginas similares quando uma página da Web não for encontrada
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: AlternateErrorPagesEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AlternateErrorPagesEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AlwaysOpenPdfExternally
  #### Sempre abrir arquivos PDF externamente
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Desabilita o Visualizador de PDF interno no Microsoft Edge.

Se você habilitar essa política, o Microsoft Edge tratará arquivos PDF como downloads e permitirá que os usuários os abram com o aplicativo padrão.

Se você não configurar essa política ou desabilitá-la, o Microsoft Edge abrirá arquivos PDF (a menos que o usuário a desabilite).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AlwaysOpenPdfExternally
  - Nome da GP: Sempre abrir arquivos PDF externamente
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AlwaysOpenPdfExternally
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AlwaysOpenPdfExternally
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AmbientAuthenticationInPrivateModesEnabled
  #### Habilitar a autenticação de ambiente para perfis InPrivate e Convidado
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 81 ou posterior

  #### Descrição
  Configure essa política para permitir ou retirar a permissão para autenticação de ambiente para perfis InPrivate e Convidado no Microsoft Edge.

A Autenticação de Ambiente é a autenticação http com credenciais padrão quando credenciais explícitas não forem fornecidas via esquemas desafio/resposta NTLM/Kerberos/Negotiate.

Se você definir a política como "RegularOnly", ela permitirá a autenticação de ambiente apenas para sessões do tipo Regular. As sessões InPrivate e Convidado não terão permissão para realizar a autenticação de ambiente.

Se você definir a política como "InPrivateAndRegular", ela permitirá a autenticação de ambiente para sessões InPrivate e Regular. As sessões do tipo Convidado não terão permissão para realizar a autenticação de ambiente.

Se você definir a política como "GuestAndRegular", ela permitirá a autenticação de ambiente para sessões Convidado e Regular. As sessões InPrivate não terão permissão para realizar a autenticação de ambiente

Se você definir a política como "All", ela permitirá a autenticação de ambiente para todas as sessões.

Observe que a autenticação de ambiente é sempre permitida em perfis regulares.

No Microsoft Edge versão 81 e posterior, se a política não for definida, a autenticação de ambiente será habilitada apenas em sessões regulares.

Mapeamento das opções da política:

* RegularOnly (0) = Habilitar a autenticação de ambiente somente em sessões comuns

* InPrivateAndRegular (1) = Habilitar autenticação de ambiente em sessões comuns e InPrivate

* GuestAndRegular (2) = Habilitar autenticação de ambiente em sessões comuns e de convidado

* All (3) = Habilitar autenticação de ambiente em sessões comuns, InPrivate e de convidado

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AmbientAuthenticationInPrivateModesEnabled
  - Nome da GP: Habilitar a autenticação de ambiente para perfis InPrivate e Convidado
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AmbientAuthenticationInPrivateModesEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AmbientAuthenticationInPrivateModesEnabled
  - Exemplo de valor:
``` xml
<integer>0</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AppCacheForceEnabled
  #### Permite que o recurso AppCache seja reativado mesmo se estiver desativado por padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 84 ou posterior

  #### Descrição
  Se você definir esta política como verdadeira, o AppCache será ativado, mesmo quando o AppCache no Microsoft Edge não estiver disponível por padrão.

Se você definir esta política como falsa ou não, o AppCache seguirá os padrões do Microsoft Edge.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AppCacheForceEnabled
  - Nome da GP: Permite que o recurso AppCache seja reativado mesmo se estiver desativado por padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AppCacheForceEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AppCacheForceEnabled
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ApplicationLocaleValue
  #### Definir localidade do aplicativo
  
  
  #### Versões com suporte:
  - No Windows desde a versão 77 ou posterior

  #### Descrição
  Configura a localidade do aplicativo em Microsoft Edge e impede que os usuários a alterem.

Se você habilitar esta política, o Microsoft Edge usará a localidade especificada. Se a localidade configurada não tiver suporte, será usada a "en-US".

Se você desabilitar ou não definir esta configuração, o Microsoft Edge usará a localidade preferencial especificada pelo usuário (se configurada) ou a localidade de fallback "en-US".

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ApplicationLocaleValue
  - Nome da GP: Definir localidade do aplicativo
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: ApplicationLocaleValue
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"en"
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AudioCaptureAllowed
  #### Permitir ou bloquear captura de áudio
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite definir se o usuário será solicitado a conceder acesso a um site para seus dispositivos de captura de áudio. Esta política se aplica a todas as URLs, exceto aquelas configuradas na lista [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Se você habilitar ou não configurar esta política (configuração padrão), o usuário será solicitado a fornecer acesso de captura de áudio, exceto das URLs na lista [AudioCaptureAllowedUrls](#audiocaptureallowedurls). Essas URLs listadas terão acesso sem solicitação.

Se esta política for desabilitada, o usuário não será avisado, e a captura de áudio ficará acessível somente para as URLs configuradas em [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Esta política afeta todos os tipos de entradas de áudio, não apenas o microfone interno.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AudioCaptureAllowed
  - Nome da GP: Permitir ou bloquear captura de áudio
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AudioCaptureAllowed
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AudioCaptureAllowed
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AudioCaptureAllowedUrls
  #### Sites podem acessar dispositivos de captura áudio sem solicitar permissão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica sites, com base nos padrões de URL, que podem usar dispositivos de captura de áudio sem pedir permissão ao usuário. Padrões nesta lista são comparados com a origem de segurança da URL solicitante. Se forem correspondentes, o site terá acesso automaticamente aos dispositivos de captura de áudio.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AudioCaptureAllowedUrls
  - Nome da GP: Sites podem acessar dispositivos de captura áudio sem solicitar permissão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AudioCaptureAllowedUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AudioSandboxEnabled
  #### Permitir execução da área restrita de áudio
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 81 ou posterior

  #### Descrição
  Essa política controla a área restrita do processo de áudio.

Se você habilitar essa política, o processo de áudio será executado em área restrita.

Se você desabilitar essa política, o processo de áudio será executado em modo sem área restrita e o módulo de processamento de áudio WebRTC será executado no processo renderizador.
Isso deixa os usuários abertos a riscos de segurança relacionados à execução do subsistema de áudio sem área restrita.

Se você não configurar essa política, a configuração padrão da área restrita de áudio será usada, o que pode variar de acordo com a plataforma.

Essa política tem como objetivo proporcionar flexibilidade às empresas para desabilitar a área restrita de áudio se usarem configurações de software de segurança que interfiram na área restrita.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AudioSandboxEnabled
  - Nome da GP: Permitir execução da área restrita de áudio
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AudioSandboxEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AudioSandboxEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AutoImportAtFirstRun
  #### Importar automaticamente os dados e as configurações de outro navegador na primeira execução
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Se você habilitar esta política, todos os tipos de dados e configurações com suporte do navegador especificado serão importados silenciosa e automaticamente na primeira execução. Durante a tela de apresentação, a seção de importação também será ignorada.

 Os dados de navegador herdados do Microsoft Edge Sempre serão migrados silenciosamente na tela de apresentação, independentemente do valor desta política. Você pode usar os seguintes valores para esta política:

 Se esta política estiver definida como "FromDefaultBrowser" , os tipos de dados correspondentes ao navegador padrão no dispositivo gerenciado serão importados.

 Se o navegador especificado como o valor desta política não estiver presente no dispositivo gerenciado, Microsoft Edge simplesmente ignorará a importação sem nenhuma notificação ao usuário.

 Se você definir esta política como 'DisabledAutoImport', a seção de importação da tela de apresentação será ignorada completamente e o Microsoft Edge não importará os dados e as configurações do navegador automaticamente.

 Se esta política estiver definida como o valor de "FromInternetExplorer" , os seguintes tipos de dados serão importados do Internet Explorer:
 1. Favoritos ou marcadores
 2. Senhas salvas
 3. Mecanismos de pesquisa
 4. Histórico de navegação
 5. Página inicial

 Se esta política estiver definida como o valor de "FromGoogleChrome", os seguintes tipos de dados serão importados do Google Chrome:
 1. Favoritos
 2. Senhas salvas
 3. Endereços e mais
 4. Informações de pagamento
 5. Histórico de navegação
 6. Configurações
 7. Guias fixas e abertas
 8. Extensões
 9. Cookies

 Observação: Para mais detalhes sobre o que é importado do Google Chrome, confira [https://go.microsoft.com/fwlink/?linkid=2120835](https://go.microsoft.com/fwlink/?linkid=2120835)

 Se esta política estiver definida como o valor de "FromSafari", os dados do usuário não são mais importados para o Microsoft Edge. Isso se deve à maneira como o Acesso Total ao Disco funciona no Mac.
 No macOS Mojave e acima dele, não é mais possível ter importação automatizada e autônoma de dados do Safari para o Microsoft Edge.

A partir do Microsoft Edge versão 83, se esta política estiver definida como o valor de "FromMozillaFirefox", os seguintes tipos de dados serão importados do Mozilla Firefox:
 1. Favoritos ou marcadores
 2. Senhas salvas
 3. Endereços e mais
 4. Histórico de navegação

 Se você deseja impedir que tipos de dados específicos sejam importados nos dispositivos gerenciados, você pode usar esta política com outras políticas, como [ImportAutofillFormData](#importautofillformdata), [ImportBrowserSettings](#importbrowsersettings), [ImportFavorites](#importfavorites), e etc.

Mapeamento das opções da política:

* FromDefaultBrowser (0) = Importa automaticamente todos os tipos de dados e configurações com suporte do navegador padrão

* FromInternetExplorer (1) = Importa automaticamente todos os tipos de dados e configurações com suporte do Internet Explorer

* FromGoogleChrome (2) = Importa automaticamente todos os tipos de dados e configurações com suporte do Google Chrome

* FromSafari (3) = Importa automaticamente todos os tipos de dados e configurações com suporte do Safari

* DisabledAutoImport (4) = Desabilita a importação automática, e a seção de importação da experiência de primeira execução é ignorada

* FromMozillaFirefox (5) = Importa automaticamente todos os tipos de dados e configurações com suporte do Mozilla Firefox

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AutoImportAtFirstRun
  - Nome da GP: Importar automaticamente os dados e as configurações de outro navegador na primeira execução
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AutoImportAtFirstRun
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AutoImportAtFirstRun
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AutoLaunchProtocolsFromOrigins
  #### Define uma lista de protocolos que podem iniciar um aplicativo externo de origens listadas sem avisar ao usuário
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 85 ou posterior

  #### Descrição
  Permite que você defina uma lista de protocolos e, para cada protocolo, uma lista associada de padrões de origem permitidos, que pode iniciar um aplicativo externo sem avisar o usuário. O separador à direita não deve ser incluído ao listar o protocolo. Por exemplo, liste "skype" em vez de "Skype:" ou "skype://".

Se você configurar essa política, um protocolo só poderá iniciar um aplicativo externo sem solicitar uma política se:

- o protocolo está listado

- a origem do site que está tentando iniciar o protocolo corresponde a um dos padrões de origem na lista de allowed_origins do protocolo.

Se uma das duas condições for falsa, o prompt de inicialização do protocolo externo não será omitido pela política.

Se você não configurar essa política, nenhum protocolo poderá ser iniciado sem confirmação. Os usuários podem recusar solicitações por meio de um protocolo/por site, a menos que a política de  [ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox) seja definida como Desabilitada. Esta política não afeta as isenções de aviso por protocolo/por site definidas pelos usuários.

Os padrões correspondentes de origem usam um formato semelhante àqueles para a política de [URLBlocklist](#urlblocklist), que estão documentadas em [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

No entanto, padrões de correspondência de origem para esta política não podem conter elementos "/path" ou "@query". Qualquer padrão que contenha um elemento "/path" ou "@query" será ignorado.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Dicionário

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AutoLaunchProtocolsFromOrigins
  - Nome da GP: Define uma lista de protocolos que podem iniciar um aplicativo externo de origens listadas sem avisar ao usuário
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AutoLaunchProtocolsFromOrigins
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
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


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AutoLaunchProtocolsFromOrigins
  - Exemplo de valor:
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
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AutoOpenAllowedForURLs
  #### URLs em que AutoOpenFileTypes pode aplicar
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 85 ou posterior

  #### Descrição
  Uma lista de URLs às quais [AutoOpenFileTypes](#autoopenfiletypes) será aplicado. Esta política não afeta os valores abertos automaticamente configurados pelos usuários por meio da prateleira de download ... > a entrada de menu "sempre abrir arquivos deste tipo".

Se você definir URLs nesta política, os arquivos serão automaticamente abertos pela política se a URL fizer parte desse conjunto e o tipo de arquivo estiver listado em [AutoOpenFileTypes](#autoopenfiletypes). Se uma das duas condições for falsa, o download não abrirá automaticamente pela política.

Se você não definir essa política, todos os downloads nos quais o tipo de arquivo está em [AutoOpenFileTypes](#autoopenfiletypes) serão abertos automaticamente.

Um padrão de URL deve ser formatado de acordo com [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AutoOpenAllowedForURLs
  - Nome da GP: URLs em que AutoOpenFileTypes pode aplicar
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\1 = "example.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\5 = ".exact.hostname.com"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AutoOpenAllowedForURLs
  - Exemplo de valor:
``` xml
<array>
  <string>example.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AutoOpenFileTypes
  #### Lista dos tipos de arquivo que devem ser abertos automaticamente ao baixar
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 85 ou posterior

  #### Descrição
  Esta política define uma lista de tipos de arquivo que devem ser abertos automaticamente ao baixar. Observação: o separador à esquerda não deve ser incluído ao listar o tipo de arquivo, portanto, lista "txt" em vez de ".txt".

  Por padrão, esses tipos de arquivo serão abertos automaticamente em todas as URLs. Você pode usar a política de [AutoOpenAllowedForURLs](#autoopenallowedforurls) para restringir as URLs para as quais esses tipos de arquivo serão abertos automaticamente.

  Os arquivos com tipos que devem ser abertos automaticamente ainda estarão sujeitos às verificações do Microsoft Defender SmartScreen habilitadas e não serão abertos se as verificações falharem.

  Os tipos de arquivo que um usuário já especificou para serem abertos automaticamente continuarão a serem abertos quando forem baixados. O usuário continuará podendo especificar outros tipos de arquivo a serem abertos automaticamente.

  Se você não definir essa política, somente os tipos de arquivo que um usuário já especificou para ser abertos automaticamente serão abertos quando baixados.

Essa política está disponível somente em instâncias do Windows associadas a um domínio Microsoft Active Directory, instâncias do Windows 10 Pro ou Enterprise registradas para o gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou associadas a um domínio via MCX..

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AutoOpenFileTypes
  - Nome da GP: Lista dos tipos de arquivo que devem ser abertos automaticamente ao baixar
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\1 = "exe"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\2 = "txt"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AutoOpenFileTypes
  - Exemplo de valor:
``` xml
<array>
  <string>exe</string>
  <string>txt</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AutofillAddressEnabled
  #### Habilitar AutoPreenchimento para endereços
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Habilita o recurso AutoPreenchimento e permite que os usuários preencham automaticamente informações de endereço em formulários da Web usando informações armazenadas anteriormente.

Se você desabilitar essa política, o AutoPreenchimento nunca sugere ou preenche informações de endereço, nem salva informações adicionais de endereço que o usuário pode enviar ao navegar na Web.

Se você habilitar essa política ou não configurá-la, os usuários poderão controlar o AutoPreenchimento de endereços na interface do usuário.

Observe que, se você desabilitar essa política, também interromperá todas as atividades de todos os formulários da Web, exceto os formulários de pagamento e senha. Nenhuma outra entrada será salva e o Microsoft Edge não sugerirá nem preencherá as entradas anteriores.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AutofillAddressEnabled
  - Nome da GP: Habilitar AutoPreenchimento para endereços
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: AutofillAddressEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AutofillAddressEnabled
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AutofillCreditCardEnabled
  #### Habilitar AutoPreenchimento para cartões de crédito
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Habilita o recurso de AutoPreenchimento do Microsoft Edge e permite que os usuários completem automaticamente informações de cartão de crédito em formulários da Web usando informações armazenadas anteriormente.

Se você desabilitar essa política, o AutoPreenchimento nunca sugerirá ou preencherá informações de cartão de crédito, nem salvará informações adicionais de cartão de crédito que os usuários possam enviar enquanto navegam na Web.

Se você habilitar essa política ou não configurá-la, os usuários poderão controlar o AutoPreenchimento de cartões de crédito.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AutofillCreditCardEnabled
  - Nome da GP: Habilitar AutoPreenchimento para cartões de crédito
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: AutofillCreditCardEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AutofillCreditCardEnabled
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### AutoplayAllowed
  #### Permitir reprodução automática de mídia para sites
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 78 ou posterior

  #### Descrição
  Esta política define a política de reprodução automática de mídia para sites.

A configuração padrão, "Não configurada", respeita as configurações de reprodução automática de mídia atuais e permite que os usuários definam suas configurações de reprodução automática.

Configurar como "Habilitada" define a reprodução automática de mídia para "Permitir".  Todos os sites podem executar a reprodução automática de mídia. Os usuários não podem substituir esta política.

Configurar como "Desabilitada" define a reprodução automática de mídia para "Bloquear". Nenhum site tem permissão para executar a reprodução automática. Os usuários não podem substituir esta política.

Uma guia terá que ser fechada e reaberta para que esta política entre em vigor.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: AutoplayAllowed
  - Nome da GP: Permitir reprodução automática de mídia para sites
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: AutoplayAllowed
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: AutoplayAllowed
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### BackgroundModeEnabled
  #### Continuar executando apps em segundo plano depois que o Microsoft Edge for fechado
  
  
  #### Versões com suporte:
  - No Windows desde a versão 77 ou posterior

  #### Descrição
  Permite que os processos do Microsoft Edge sejam iniciados durante a conexão do SO e continuem em execução depois que a última janela do navegador for fechada. Nesse cenário, os aplicativos em segundo plano e a sessão de navegação atual permanecem ativos, incluindo quaisquer cookies de sessão. Um processo em segundo plano aberto exibe um ícone na bandeja do sistema e sempre pode ser fechado a partir desse local.

Se você habilitar essa política, o modo de segundo plano será ativado.

Se você desabilitar essa política, o modo de segundo plano será desativado.

Se você não configurar essa política, o modo de segundo plano será inicialmente desativado e o usuário poderá configurar seu comportamento em edge://settings/system.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: BackgroundModeEnabled
  - Nome da GP: Continuar executando apps em segundo plano depois que o Microsoft Edge for fechado
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: BackgroundModeEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### BackgroundTemplateListUpdatesEnabled
  #### Habilita atualizações em segundo plano na lista de modelos disponíveis para Coleções e outros recursos que usam modelos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 79 ou posterior

  #### Descrição
  Permite habilitar ou desabilitar atualizações em segundo plano na lista de modelos disponíveis para Coleções e outros recursos que usam modelos.  Os modelos são usados para extrair metadados sofisticados de uma página da Web quando a página é salva em uma coleção.

Se você habilitar essa configuração ou se a configuração não estiver definida, a lista de modelos disponíveis será baixada em segundo plano de um serviço Microsoft a cada 24 horas.

Se você desabilitar esta configuração, a lista de modelos disponíveis será baixada por demanda. Esse tipo de download pode resultar em pequenas penalidades de desempenho para Coleções e outros recursos.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: BackgroundTemplateListUpdatesEnabled
  - Nome da GP: Habilita atualizações em segundo plano na lista de modelos disponíveis para Coleções e outros recursos que usam modelos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: BackgroundTemplateListUpdatesEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: BackgroundTemplateListUpdatesEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### BingAdsSuppression
  #### Bloquear todos os anúncios nos resultados de pesquisa do Bing
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 83 ou posterior

  #### Descrição
  Habilita uma experiência de pesquisa sem anúncios no Bing.com

Se você habilitar esta política, um usuário poderá pesquisar no bing.com e ter uma experiência de pesquisa sem anúncios. Ao mesmo tempo, a configuração do SafeSearch será definida como 'Estrita' e não poderá ser alterada pelo usuário.

Se você não configurar esta política, a experiência padrão terá anúncios nos resultados da pesquisa em bing.com. O SafeSearch se encontra definido como 'Moderado' por padrão e isso pode ser alterado pelo usuário.

Esta política está disponível apenas para SKUs K-12 identificados como locatários EDU pela Microsoft.

Confira [https://go.microsoft.com/fwlink/?linkid=2119711](https://go.microsoft.com/fwlink/?linkid=2119711) para saber mais sobre esta política ou se os seguintes cenários se aplicam a você:

* Você tem um locatário EDU, mas a política não funciona.

* Seu IP foi incluído na lista de permissões por ter uma experiência de pesquisa sem anúncios.

* Você estava experimentando uma experiência de pesquisa sem anúncios no Microsoft Edge herdado e deseja atualizar para a nova versão do Microsoft Edge.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: BingAdsSuppression
  - Nome da GP: Bloquear todos os anúncios nos resultados de pesquisa do Bing
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: BingAdsSuppression
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: BingAdsSuppression
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### BlockThirdPartyCookies
  #### Bloquear cookies de terceiros
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Impede que os elementos de páginas da Web que não pertençam ao domínio indicado na barra de endereços definam cookies.

Se você habilitar esta política, os elementos de páginas da Web que não pertencerem ao domínio indicado na barra de endereços não poderão definir cookies

Se você desabilitar esta política, os elementos de páginas da Web de domínios não indicados na barra de endereços poderão definir cookies.

Se você não configurar esta política, os cookies de terceiros serão habilitados, mas os usuários poderão alterar essa configuração.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: BlockThirdPartyCookies
  - Nome da GP: Bloquear cookies de terceiros
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: BlockThirdPartyCookies
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: BlockThirdPartyCookies
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### BrowserAddProfileEnabled
  #### Habilitar a criação de perfil no menu do submenu Identidade ou na página Configurações
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite que os usuários criem novos perfis usando a opção **Adicionar perfil**.
Se você habilitar essa política ou não configurá-la, o Microsoft Edge permitirá que os usuários usem **Adicionar perfil** no menu de submenu Identidade ou na página Configurações para criar novos perfis.

Se você desabilitar essa política, os usuários não poderão adicionar novos perfis a partir do menu do submenu Identidade ou da página Configurações.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: BrowserAddProfileEnabled
  - Nome da GP: Habilitar a criação de perfil no menu do submenu Identidade ou na página Configurações
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: BrowserAddProfileEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: BrowserAddProfileEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### BrowserGuestModeEnabled
  #### Habilitar modo convidado
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Habilita a opção para permitir o uso de perfis de convidado no Microsoft Edge. Em um perfil de convidado, o navegador não importa os dados de navegação dos perfis existentes e exclui os dados de navegação quando todos os perfis de convidado são fechados.

Se você habilitar essa política ou não configurá-la, o Microsoft Edge permitirá que os usuários naveguem em perfis de convidado.

Se você desabilitar esta política, o Microsoft Edge não permitirá que os usuários naveguem em perfis de convidado.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: BrowserGuestModeEnabled
  - Nome da GP: Habilitar modo convidado
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: BrowserGuestModeEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: BrowserGuestModeEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### BrowserNetworkTimeQueriesEnabled
  #### Permitir consultas a um serviço de Hora da Rede do Navegador
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Impede que Microsoft Edge envie ocasionalmente consultas a um serviço de tempo de rede do navegador para recuperar um registro de carimbo de data/hora preciso.

Se você desabilitar essa política, o Microsoft Edge deixará de enviar consultas para um serviço de tempo de rede do navegador.

Se você habilitar essa política ou não configurá-la, o Microsoft Edge ocasionalmente enviará consultas para um serviço de tempo de rede do navegador.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: BrowserNetworkTimeQueriesEnabled
  - Nome da GP: Permitir consultas a um serviço de Hora da Rede do Navegador
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: BrowserNetworkTimeQueriesEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: BrowserNetworkTimeQueriesEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### BrowserSignin
  #### Configurações de entrada do navegador
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifique se um usuário pode entrar no Microsoft Edge com sua própria conta e usar serviços relacionados à conta, como sincronização e logon único. Para controlar a disponibilidade da sincronização, use a política [SyncDisabled](#syncdisabled).

 Se você definir essa política como "Disable", também defina a política [NonRemovableProfileEnabled](#nonremovableprofileenabled) como desabilitada porque [NonRemovableProfileEnabled](#nonremovableprofileenabled) desabilita a criação de um perfil de navegador conectado automaticamente. Se as duas políticas forem definidas, o Microsoft Edge usará a política "Desabilitar entrada no navegador" e se comportará como se [NonRemovableProfileEnabled](#nonremovableprofileenabled) estivesse definida como desabilitada.

 Se você definir essa política como "Enable",  os usuários poderão entrar no navegador. Entrar no navegador não significa que a sincronização será ativada por padrão; o usuário deverá aceitar separadamente para usar esse recurso.

 Se você definir essa política como "Force", os usuários deverão entrar em um perfil para usar o navegador. Por padrão, isso permitirá que o usuário escolha se quer sincronizar com a conta, a menos que a sincronização seja desabilitada pelo administrador do domínio ou com a política [SyncDisabled](#syncdisabled). O valor padrão da política [BrowserGuestModeEnabled](#browserguestmodeenabled) é definido como false.

Se você não configurar essa política, os usuários poderão decidir se desejam habilitar a opção de entrada no navegador e usá-la como quiserem.

Mapeamento das opções da política:

* Disable (0) = Desabilitar a entrada do navegador

* Enable (1) = Habilitar entrada do navegador

* Force (2) = Fazer com que os usuários entrem para usar o navegador

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: BrowserSignin
  - Nome da GP: Configurações de entrada do navegador
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: BrowserSignin
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: BrowserSignin
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### BuiltInDnsClientEnabled
  #### Usar o cliente DNS interno
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Controla se o cliente DNS interno deve ser usado.

Isso não afeta quais servidores DNS são usados, apenas a pilha de software usada para se comunicar com eles. Por exemplo, se o sistema operacional estiver configurado para usar um servidor DNS corporativo, esse mesmo servidor será usado pelo cliente DNS interno. No entanto, é possível que o cliente DNS interno atenda servidores de formas diferentes usando protocolos mais modernos relacionados ao DNS, como o DNS sobre TLS.

Se você habilitar essa política, o cliente DNS interno será usado, caso esteja disponível.

Se você desabilitar essa política, o cliente nunca será usado.

Se você não configurar essa política, o cliente DNS interno será habilitado por padrão no MacOS, e os usuários poderão alterar se desejam usar o cliente DNS interno editando edge://flags ou especificando um sinalizador de linha de comando.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: BuiltInDnsClientEnabled
  - Nome da GP: Usar o cliente DNS interno
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: BuiltInDnsClientEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: BuiltInDnsClientEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### BuiltinCertificateVerifierEnabled
  #### Determina se o verificador de certificado interno será usado para verificar os certificados do servidor (preterida)
  >PRETERIDA: essa política foi preterida. No momento, ela tem suporte, mas ficará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - No macOS desde a versão 83 ou posterior

  #### Descrição
  Essa política foi preterida porque destina-se apenas a servir como um mecanismo de curto prazo para dar mais tempo para que as empresas atualizem seus ambientes e relatarem problemas se estiverem incompatíveis com o verificador de certificados interno.

Não funcionará na versão 87 do Microsoft Edge para Mac OS, quando o suporte para o verificador de certificado herdado no Mac OS X está planejado para ser removido.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  

  #### Informações e configurações do Mac
  - Nome da chave de preferência: BuiltinCertificateVerifierEnabled
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### CertificateTransparencyEnforcementDisabledForCas
  #### Desabilitar a imposição de Transparência de Certificado para uma lista de hashes de subjectPublicKeyInfo
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Desabilita a imposição dos requisitos de Transparência de Certificado para uma lista de hashes subjectPublicKeyInfo.

Essa política permite desabilitar os requisitos de divulgação da Transparência de Certificado para cadeias de certificados que contenham certificados com um dos hashes subjectPublicKeyInfo especificados. Isso permite que certificados que de outra forma não seriam confiáveis, porque não foram divulgados publicamente da forma devida, continuem sendo usados para hosts Enterprise.

Para desabilitar a imposição da Transparência de Certificado quando essa política for definida, um dos seguintes conjuntos de condições deverá ser atendido:
1. O hash é do subjectPublicKeyInfo do certificado do servidor.
2. O hash é de um subjectPublicKeyInfo que aparece em um certificado da autoridade de certificação na cadeia de certificados, que é restrito pela extensão X.509v3 nameConstraints, um ou mais directoryName nameConstraints estão presentes nos permittedSubtrees e o directoryName contém um atributo organizationName.
3. O hash é de um subjectPublicKeyInfo que aparece em um certificado da autoridade de certificação na cadeia de certificados, o certificado de autoridade de certificação possui um ou mais atributos organizationName no certificado Subject e o certificado do servidor contém o mesmo número de atributos organizationName, na mesma ordem e com valores idênticos byte por byte.

Um hash subjectPublicKeyInfo é especificado concatenando o nome do algoritmo de hash, o caractere "/" e a codificação Base64 desse algoritmo de hash aplicado ao subjectPublicKeyInfo codificado por DER do certificado especificado. Essa codificação Base64 tem o mesmo formato de uma impressão digital SPKI, conforme definido na RFC 7469, seção 2.4. Algoritmos de hash não reconhecidos são ignorados. O único algoritmo de hash compatível neste momento é "sha256".

Se você desabilitar essa política ou não a configurar, todos os certificados que tiverem de ser divulgados por meio da Transparência de Certificado serão tratados como não confiáveis se não forem divulgados de acordo com a política Transparência de Certificado.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: CertificateTransparencyEnforcementDisabledForCas
  - Nome da GP: Desabilitar a imposição de Transparência de Certificado para uma lista de hashes de subjectPublicKeyInfo
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\2 = "sha256//////////////////////w=="

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: CertificateTransparencyEnforcementDisabledForCas
  - Exemplo de valor:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### CertificateTransparencyEnforcementDisabledForLegacyCas
  #### Desabilitar a imposição de Transparência de Certificado para uma lista de autoridades de certificação herdadas
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Desabilita a imposição de requisitos de Transparência de Certificado para uma lista de autoridades de certificação (ACs) herdadas.

Essa política permite desabilitar os requisitos de divulgação de transparência de certificado para cadeias de certificados que contenham certificados com um dos hashes subjectPublicKeyInfo especificados. Isso permite que os certificados, que de outra forma não seriam confiáveis por não terem sido divulgados publicamente da forma correta, continuem a ser usados para hosts corporativos.

Para que a imposição de Transparência de Certificado seja desabilitada, você deve definir o hash como um subjectPublicKeyInfo que seja exibido em um Certificado de Autoridade de Certificação reconhecido como uma AC (autoridade de certificação) herdada. Uma AC herdada é uma AC que foi publicamente considerada confiável por padrão por um ou mais sistemas operacionais compatíveis com o Microsoft Edge.

Você especifica um hash de subjectPublicKeyInfo concatenando o nome do algoritmo de hash, o caractere "/" e a codificação Base64 desse algoritmo de hash aplicado ao subjectPublicKeyInfo codificado por DER do certificado especificado. Essa codificação Base64 tem o mesmo formato que uma impressão digital SPKI, conforme definido no RFC 7469, Seção 2.4. Os algoritmos de hash não reconhecidos são ignorados. O único algoritmo de hash com suporte no momento é o "sha256".

Se você não configurar essa política, qualquer certificado que precise ser divulgado por meio da Transparência de Certificado será tratado como não confiável se não for divulgado de acordo com a política Transparência de Certificado.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Nome da GP: Desabilitar a imposição de Transparência de Certificado para uma lista de autoridades de certificação herdadas
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\2 = "sha256//////////////////////w=="

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Exemplo de valor:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### CertificateTransparencyEnforcementDisabledForUrls
  #### Desabilitar a imposição de Transparência de Certificado para URLs específicas
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Desabilita a aplicação dos requisitos de Transparência do Certificado para as URLs listadas.

Essa política permite que você não divulgue certificados para os nomes de host nas URLs especificadas por meio da Transparência do Certificado. Isso permite usar certificados que, de outra forma, não seriam confiáveis, porque não foram divulgados adequadamente, mas dificulta a detecção de certificados incorretos para esses hosts.

Forme seu padrão de URL de acordo com [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Como os certificados são válidos para um determinado nome de host, independentemente do esquema, porta ou caminho, apenas a parte do nome do host da URL é considerada. Hosts curinga não são compatíveis.

Se você não configurar essa política, qualquer certificado que deva ser divulgado por meio de Transparência do Certificado será tratado como não confiável se não for divulgado.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: CertificateTransparencyEnforcementDisabledForUrls
  - Nome da GP: Desabilitar a imposição de Transparência de Certificado para URLs específicas
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\2 = ".contoso.com"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: CertificateTransparencyEnforcementDisabledForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>contoso.com</string>
  <string>.contoso.com</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ClearBrowsingDataOnExit
  #### Limpar dados de navegação quando o Microsoft Edge for fechado
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 78 ou posterior

  #### Descrição
  Por padrão, o Microsoft Edge não limpa os dados de navegação quando é fechado. Os dados de navegação incluem informações fornecidas em formulários, senhas e até mesmo em sites visitados.

Se você habilitar essa política, todos os dados serão excluídos toda vez que o Microsoft Edge for fechado. Observe que se você habilitar essa política, ela terá precedência sobre a forma que você tiver configurado a política [DefaultCookiesSetting](#defaultcookiessetting)

Se você desabilitar ou não configurar essa política, os usuários poderão configurar a opção Limpar dados de navegação em Configurações.

Se você habilitar essa política, não configure a política [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) ou [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit), porque todas elas lidam com a exclusão de dados de navegação. Se você configurar as políticas anteriores e essa política, todos os dados de navegação serão excluídos quando o Microsoft Edge for fechado, independentemente de como você tenha configurado a política [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) ou [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

Para impedir a exclusão de cookies ao sair, configure a política [SaveCookiesOnExit](#savecookiesonexit).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ClearBrowsingDataOnExit
  - Nome da GP: Limpar dados de navegação quando o Microsoft Edge for fechado
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: ClearBrowsingDataOnExit
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ClearBrowsingDataOnExit
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ClearCachedImagesAndFilesOnExit
  #### Limpar arquivos e imagens armazenados em cache quando Microsoft Edge for fechado
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 83 ou posterior

  #### Descrição
  O Microsoft Edge não limpa arquivos e imagens em cache por padrão quando é fechado.

Se você habilitar essa política, os arquivos e as imagens em cache serão excluídas toda vez que o Microsoft Edge for fechado.

Se você desabilitar essa política, os usuários não poderão configurar a opção de arquivos e imagens em cache em edge://settings/clearBrowsingDataOnClose.

Se você não configurar essa política, os usuários podem optar por limpar os arquivos e as imagens em cache quando saírem do navegador.

Se você desabilitar essa política, não habilite a política [ClearBrowsingDataOnExit](#clearbrowsingdataonexit), porque as duas tratam da exclusão de dados. Se você configurar as duas, a política [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) prevalecerá e excluirá todos os dados quando o Microsoft Edge for fechado, independentemente de como você tenha configurado a política [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ClearCachedImagesAndFilesOnExit
  - Nome da GP: Limpar arquivos e imagens armazenados em cache quando Microsoft Edge for fechado
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: ClearCachedImagesAndFilesOnExit
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ClearCachedImagesAndFilesOnExit
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### CollectionsServicesAndExportsBlockList
  #### Bloquear o acesso a uma lista especificada de serviços e exportar destinos em Coleções
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Listar os serviços específicos e exportar os destinos que os usuários não podem acessar no recurso Coletas em Microsoft Edge. Isso inclui a exibição de dados adicionais do Bing e a exportação de coletas para produtos da Microsoft ou parceiros externos.

Se você habilitar essa política, os serviços e os destinos de exportação correspondentes à lista determinada serão bloqueados.

Se você não configurar essa política, nenhuma restrição aos serviços e destinos de exportação aceitáveis será imposta.

Mapeamento das opções da política:

* pinterest_suggestions (pinterest_suggestions) = Sugestões do Pinterest

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: CollectionsServicesAndExportsBlockList
  - Nome da GP: Bloquear o acesso a uma lista especificada de serviços e exportar destinos em Coleções
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\1 = "pinterest_suggestions"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: CollectionsServicesAndExportsBlockList
  - Exemplo de valor:
``` xml
<array>
  <string>pinterest_suggestions</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### CommandLineFlagSecurityWarningsEnabled
  #### Habilitar avisos de segurança para sinalizadores de linha de comando
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 78 ou posterior

  #### Descrição
  Se desabilitada, essa política impedirá que os avisos de segurança sejam exibidos quando o Microsoft Edge for iniciado com sinalizadores de linha de comando potencialmente perigosos.

Se habilitada ou indefinida, os avisos de segurança são exibidos quando esses sinalizadores de linha de comando são usados para iniciar o Microsoft Edge.

Por exemplo, o sinalizador --disable-gpu-sandbox gera este aviso: Você está usando um sinalizador de linha de comando sem suporte: --disable-gpu-sandbox. Isso representa riscos de estabilidade e segurança.

Essa política está disponível somente em instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, instâncias do Windows 10 Pro ou Enterprise registradas para o gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou associadas a um domínio via MCX.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: CommandLineFlagSecurityWarningsEnabled
  - Nome da GP: Habilitar avisos de segurança para sinalizadores de linha de comando
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: CommandLineFlagSecurityWarningsEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: CommandLineFlagSecurityWarningsEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ComponentUpdatesEnabled
  #### Habilitar atualizações de componentes no Microsoft Edge
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Se você habilitar ou não configurar essa política, as atualizações de componentes serão habilitadas no Microsoft Edge.

Se você desabilitar essa política ou defini-la como false, as atualizações de componentes serão desabilitadas para todos os componentes no Microsoft Edge.

No entanto, alguns componentes estão isentos dessa política. Isso inclui qualquer componente que não contenha código executável, que não altere significativamente o comportamento do navegador ou que seja crítico para a segurança. Ou seja, as atualizações consideradas "críticas para segurança" ainda serão aplicadas, mesmo que você desabilite essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ComponentUpdatesEnabled
  - Nome da GP: Habilitar atualizações de componentes no Microsoft Edge
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ComponentUpdatesEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ComponentUpdatesEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ConfigureDoNotTrack
  #### Configurar Não Rastrear
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica se deve-se enviar solicitações Não Rastrear a sites que pedem para rastrear informações. As solicitações Não Rastrear permitem que os sites que você visita saibam que você não deseja que sua atividade de navegação seja rastreada. Por padrão, o Microsoft Edge não envia solicitações Não Rastrear, mas os usuários podem ativar esse recurso para enviá-las.

Se você habilitar essa política, as solicitações Não Rastrear sempre serão enviadas a sites que solicitem rastrear informações.

Se essa política for desabilitada, as solicitações nunca serão enviadas.

Se você não configurar essa política, os usuários poderão optar por enviar ou não essas solicitações.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ConfigureDoNotTrack
  - Nome da GP: Configurar Não Rastrear
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ConfigureDoNotTrack
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ConfigureDoNotTrack
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ConfigureOnPremisesAccountAutoSignIn
  #### Configurar a entrada automática com uma conta de domínio do Active Directory quando não houver nenhuma conta de domínio do Azure AD
  
  
  #### Versões com suporte:
  - No Windows desde a versão 81 ou posterior

  #### Descrição
  Habilite o uso de contas do Active Directory para entrada automática se as máquinas dos usuários que fizerem parte do domínio e se o seu ambiente não for híbrido. Se você quiser que os usuários se conectem automaticamente com suas contas do Azure Active Directory, torne seu ambiente parte do Azure AD (Consulte [https://go.microsoft.com/fwlink/?linkid=2118197](https://go.microsoft.com/fwlink/?linkid=2118197) para obter mais informações) ou parte híbrida (Consulte [https://go.microsoft.com/fwlink/?linkid=2118365](https://go.microsoft.com/fwlink/?linkid=2118365) para obter mais informações).

Se você definiu a política [BrowserSignin](#browsersignin) como desabilitada, essa política não entrará em vigor.

Se você habilitar essa política e defini-la como "SignInAndMakeDomainAccountNonRemovable", o Microsoft Edge conectará automaticamente os usuários que estão em computadores associados a um domínio usando suas contas do Active Directory.

Se você definir essa política como "Disabled" ou não defini-la, Microsoft Edge não conectará automaticamente os usuários que estão em computadores associados a um domínio com contas do Active Directory.

Mapeamento das opções da política:

* Disabled (0) = Desabilitado

* SignInAndMakeDomainAccountNonRemovable (1) = Entrar e tornar a conta de domínio não removível

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ConfigureOnPremisesAccountAutoSignIn
  - Nome da GP: Configurar a entrada automática com uma conta de domínio do Active Directory quando não houver nenhuma conta de domínio do Azure AD
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ConfigureOnPremisesAccountAutoSignIn
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ConfigureOnlineTextToSpeech
  #### Configurar a conversão de texto em fala online
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Defina se o navegador pode aproveitar as fontes de voz para Conversão de Texto em Fala Online, parte dos Serviços Cognitivos do Azure. Essas fontes de voz são de maior qualidade do que as fontes de voz do sistema pré-instaladas.

Se você habilitar ou não configurar essa política, os aplicativos web que usam a API SpeechSynthesis poderão usar as fontes de voz para Conversão de Texto em Fala Online.

Se essa política for desabilitada, as fontes de voz não estarão disponíveis.

Leia mais sobre esse recurso aqui:
API SpeechSynthesis: [https://go.microsoft.com/fwlink/?linkid=2110038](https://go.microsoft.com/fwlink/?linkid=2110038)
Serviços Cognitivos: [https://go.microsoft.com/fwlink/?linkid=2110141](https://go.microsoft.com/fwlink/?linkid=2110141)

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ConfigureOnlineTextToSpeech
  - Nome da GP: Configurar a conversão de texto em fala online
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ConfigureOnlineTextToSpeech
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ConfigureOnlineTextToSpeech
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ConfigureShare
  #### Configurar a Experiência de compartilhamento
  
  
  #### Versões com suporte:
  - No Windows desde a versão 83 ou posterior

  #### Descrição
  Se você definir esta política como 'ShareAllowed'  (o padrão), os usuários poderão acessar a experiência de compartilhamento do Windows 10 no menu Configurações e mais Microsoft Edge para compartilhar com outros aplicativos no sistema.

Se você definir esta política como 'ShareDisallowed', os usuários não poderão acessar a experiência do Windows 10 Share. Se o botão Compartilhar estiver na barra de ferramentas, ele também ficará oculto.

Mapeamento das opções da política:

* ShareAllowed (0) = Permitir o uso da Experiência de compartilhamento

* ShareDisallowed (1) = Não permitir o uso da Experiência de compartilhamento

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ConfigureShare
  - Nome da GP: Configurar a Experiência de compartilhamento
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ConfigureShare
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### CustomHelpLink
  #### Especificar link de ajuda personalizado
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 79 ou posterior

  #### Descrição
  Especifique um link para o menu Ajuda ou para a tecla F1.

Se você habilitar essa política, um administrador poderá especificar um link para o menu Ajuda ou para a tecla F1.

Se você desabilitar ou não configurar essa política, o link padrão para o menu Ajuda ou para a tecla F1 será usado.

Essa política está disponível somente em instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, instâncias do Windows 10 Pro ou Enterprise registradas para gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou que ingressaram em um domínio via MCX.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: CustomHelpLink
  - Nome da GP: Especificar link de ajuda personalizado
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: CustomHelpLink
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"https://go.microsoft.com/fwlink/?linkid=2080734"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: CustomHelpLink
  - Exemplo de valor:
``` xml
<string>https://go.microsoft.com/fwlink/?linkid=2080734</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DNSInterceptionChecksEnabled
  #### Verificações de interceptação de DNS habilitadas
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 80 ou posterior

  #### Descrição
  Esta política configura um comutador local que pode ser usado para desabilitar verificações de interceptação de DNS. Essas verificações tentam descobrir se o navegador está atrás de um proxy que redireciona nomes de host desconhecidos.

Essa detecção pode não ser necessária em um ambiente empresarial no qual a configuração de rede é conhecida. Pode ser desabilitada para evitar tráfego de DNS e HTTP adicional na inicialização e em cada alteração de configuração de DNS.

Se você habilitar ou não configurar esta política, as verificações de interceptação de DNS serão executadas.

Se você desabilitar esta política, as verificações de interceptação de DNS não serão executadas.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DNSInterceptionChecksEnabled
  - Nome da GP: Verificações de interceptação de DNS habilitadas
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DNSInterceptionChecksEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DNSInterceptionChecksEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultBrowserSettingEnabled
  #### Definir Microsoft Edge como navegador padrão
  
  
  #### Versões com suporte:
  - Em Windows 7 e macOS desde 77 ou posterior

  #### Descrição
  Se você habilitar esta política como Verdadeira, o Microsoft Edge sempre verificará na inicialização se é o navegador padrão e automaticamente se registrará, se possível.

Se você definir esta política como Falsa, o Microsoft Edge será impedido de verificar se é o padrão e desativa os controles do usuário para esta opção.

Se você não definir esta política, o Microsoft Edge permitirá aos usuários controlar se é o padrão e, caso contrário, se as notificações do usuário devem ser exibidas.

Observação para administradores do Windows: esta política só funciona para computadores que executam o Windows 7. Para versões posteriores do Windows, você deve implantar um arquivo de "associações de aplicativos padrão" que torna o Microsoft Edge o manipulador para os protocolos HTTPS e HTTP (e, opcionalmente, o protocolo FTP e os formatos de arquivo, como .html, .htm, .pdf, .svg, .webp). Consulte [https://go.microsoft.com/fwlink/?linkid=2094932](https://go.microsoft.com/fwlink/?linkid=2094932) para obter mais informações.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultBrowserSettingEnabled
  - Nome da GP: Definir Microsoft Edge como navegador padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DefaultBrowserSettingEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultBrowserSettingEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultSearchProviderContextMenuAccessAllowed
  #### Permitir acesso de pesquisa do menu de contexto do provedor de pesquisa padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 85 ou posterior

  #### Descrição
  Habilita o uso de um provedor de pesquisa padrão no menu de contexto.

Se você definir esta política como desabilitada, o item menu de contexto de pesquisa que depende do seu provedor de pesquisa padrão e da pesquisa na barra lateral não estará disponível.

Se essa política estiver definida como habilitada ou não definida, o item menu de contexto para o provedor de pesquisa padrão e a pesquisa da barra lateral estarão disponíveis.

O valor da política somente é aplicado quando a política de [DefaultSearchProviderEnabled](#defaultsearchproviderenabled)  está habilitada e não é aplicável do contrário.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultSearchProviderContextMenuAccessAllowed
  - Nome da GP: Permitir acesso de pesquisa do menu de contexto do provedor de pesquisa padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DefaultSearchProviderContextMenuAccessAllowed
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSearchProviderContextMenuAccessAllowed
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultSensorsSetting
  #### Configuração de sensores padrão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Defina se os sites podem acessar e usar sensores como sensores de movimento e de luz. Você pode bloquear ou permitir que os sites tenham acesso a sensores.

A configuração da política como 1 permite que os sites acessem e usem sensores. Definir a política para 2 nega o acesso aos sensores.

Você pode substituir essa política por padrões de URL específicos, usando as políticas de [SensorsAllowedForUrls](#sensorsallowedforurls) e [SensorsBlockedForUrls](#sensorsblockedforurls).

Se você não configurar essa política, os sites podem acessar e usar sensores, e os usuários podem alterar essa configuração. Esse é o padrão global para [SensorsAllowedForUrls](#sensorsallowedforurls) e [SensorsBlockedForUrls](#sensorsblockedforurls).

Mapeamento das opções da política:

* AllowSensors (1) = Permitir que os sites acessem sensores

* BlockSensors (2) = Não permitir que todos os sites acessem sensores

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultSensorsSetting
  - Nome da GP: Configuração de sensores padrão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DefaultSensorsSetting
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSensorsSetting
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DefaultSerialGuardSetting
  #### Controlar o uso da API serial
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Define se os sites podem acessar portas seriais. Você pode bloquear completamente o acesso ou perguntar ao usuário toda vez que um site quiser obter acesso a uma porta serial.

A configuração da política como 3 permite que os sites solicitem acesso a portas seriais. A configuração da política como 2 nega acesso a portas seriais.

Você pode substituir essa política para padrões de URL específicos usando as políticas de [SerialAskForUrls](#serialaskforurls) e [SerialBlockedForUrls](#serialblockedforurls).

    Se você não configurar essa política, por padrão, os sites poderão perguntar aos usuários se eles podem acessar uma porta serial e se os usuários podem alterar essa configuração.

Mapeamento das opções da política:

* BlockSerial (2) = Não permitir que os sites solicitem acesso a portas seriais pela API serial

* AskSerial (3) = Permitir que os sites solicitem permissão do usuário para acessar uma porta serial

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DefaultSerialGuardSetting
  - Nome da GP: Controlar o uso da API serial
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DefaultSerialGuardSetting
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DefaultSerialGuardSetting
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DelayNavigationsForInitialSiteListDownload
  #### Exigir que a Lista de Sites do Modo Empresarial esteja disponível antes da navegação na guia
  
  
  #### Versões com suporte:
  - No Windows desde a versão 84 ou posterior

  #### Descrição
  Permite que você especifique se guias do Microsoft Edge aguardam para navegar até que o navegador baixe a Lista de Sites inicial do Modo Empresarial. Essa configuração destina-se ao cenário em que a home page do navegador deve ser carregada no modo Internet Explorer e é importante fazer isso no navegador pela primeira vez, após o modo IE estar habilitado. Se esse cenário não existir, recomendamos não habilitar essa configuração porque isso pode afetar negativamente o desempenho do carregamento da home page. A configuração se aplica somente quando o Microsoft Edge não tiver uma lista de sites do Modo Empresarial em cache, como no primeiro navegador executado após o modo IE estar habilitado.

       Essa configuração funciona em conjunto com o:
       [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) estar definido como "IEMode"
       e a política
       [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)onde a lista tem pelo menos uma entrada.

O comportamento de tempo limite desta política pode ser configurado com a política de [NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout).

       Se você definir essa política como All, quando Microsoft Edge não tiver uma versão em cache da lista de Sites do Modo Empresarial, as guias adiarão a navegação até que o navegador baixe a lista de sites. Os sites configurados para abrir no modo do Internet Explorer pela lista de sites serão carregados no modo do Internet Explorer, mesmo durante a navegação inicial do navegador. Os sites que provavelmente não conseguem ser configurados para abrir no Internet Explorer, como em qualquer site com um esquema diferente de http:, https:, arquivo: ou ftp: não atrasam a navegação e a carregam imediatamente no modo Edge.

        Se você definir essa política como "None" ou não a configurar, quando Microsoft Edge não tiver uma versão em cache da Lista de Sites do Modo Empresarial, as guias navegarão imediatamente e não esperará o navegador baixar a Lista de Sites do Modo Empresarial. Os sites configurados para abrir no modo do Internet Explorer pela lista de sites serão abertos no modo Microsoft Edge até que o navegador termine de baixar a lista de Sites do Modo Empresarial.

Mapeamento das opções da política:

* None (0) = Nenhum

* All (1) = Todas as navegações elegíveis

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DelayNavigationsForInitialSiteListDownload
  - Nome da GP: Exigir que a Lista de Sites do Modo Empresarial esteja disponível antes da navegação na guia
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DelayNavigationsForInitialSiteListDownload
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DeleteDataOnMigration
  #### Excluir dados antigos do navegador na migração
  
  
  #### Versões com suporte:
  - No Windows desde a versão 83 ou posterior

  #### Descrição
  Esta política determina se os dados de navegação do usuário da Versão Prévia do Microsoft Edge serão excluídos após a migração para o Microsoft Edge versão 81 ou posterior.

Se você definir esta política como "Habilitada", todos os dados de navegação da Versão Prévia do Microsoft Edge após a migração para o Microsoft Edge versão 81 ou posterior serão excluídos. Esta política deve ser definida antes da migração para o Microsoft Edge versão 81 ou posterior para que haja efeito sobre os dados de navegação existentes.

Se você definir esta política como "Desabilitada" ou se a política não estiver configurada, os dados de navegação do usuário não serão excluídos após a migração para o Microsoft Edge versão 83 ou posterior.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DeleteDataOnMigration
  - Nome da GP: Excluir dados antigos do navegador na migração
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DeleteDataOnMigration
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DeveloperToolsAvailability
  #### Controlar onde as ferramentas de desenvolvedor podem ser usadas
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Controla onde as ferramentas de desenvolvedor podem ser usadas.

Se você definir esta política como 'DeveloperToolsDisallowedForForceInstalledExtensions' (o padrão), os usuários poderão acessar as ferramentas de desenvolvedor e o console do JavaScript em geral, mas não no contexto de extensões instaladas pela política corporativa.

Se você definir esta política como 'DeveloperToolsAllowed', os usuários poderão acessar as ferramentas de desenvolvedor e o console do JavaScript em todos os contextos, incluindo as extensões instaladas pela política corporativa.

Se você definir esta política como 'DeveloperToolsDisallowed', os usuários não poderão acessar as ferramentas de desenvolvedor nem inspecionar elementos do site. Os atalhos de teclado e as entradas de menu ou menu de contexto que abrem as ferramentas de desenvolvedor ou o Console do JavaScript são desabilitadas.

Mapeamento das opções da política:

* DeveloperToolsDisallowedForForceInstalledExtensions (0) = Bloquear as ferramentas de desenvolvedor em extensões instaladas pela política corporativa e permitir em outros contextos

* DeveloperToolsAllowed (1) = Permitir o uso das ferramentas de desenvolvedor

* DeveloperToolsDisallowed (2) = Não permitir o uso das ferramentas de desenvolvedor

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DeveloperToolsAvailability
  - Nome da GP: Controlar onde as ferramentas de desenvolvedor podem ser usadas
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DeveloperToolsAvailability
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DeveloperToolsAvailability
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DiagnosticData
  #### Enviar dados de diagnóstico necessários e opcionais sobre o uso do navegador
  
  
  #### Versões com suporte:
  - Em Windows 7 e macOS desde 86 ou posterior

  #### Descrição
  Esta política controla o envio de dados de diagnóstico obrigatórios sobre o uso do navegador à Microsoft.

Dados de diagnóstico necessários são coletados para manter Microsoft Edge seguro, atualizado e em execução conforme o esperado.

Dados de diagnóstico opcionais incluem os dados sobre o uso do navegador, os sites visitados e relatórios de falha à Microsoft para melhorar o produto e o serviço.

Esta política não é compatível com dispositivos Windows 10. Para controlar essa coleta de dados no Windows 10, os administradores de TI devem usar a política de grupo de dados de diagnóstico do Windows. Essa política será “Permitir Telemetria” ou “Permitir Dados de Diagnóstico”, dependendo da versão do Windows. Saiba mais sobre a coleta de dados de diagnóstico no Windows 10: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

Use uma das configurações a seguir para definir essa política:

'Off' desativa a coleta de dados de diagnóstico obrigatória e opcional. Esta opção não é recomendada.

'RequiredData' envia os dados de diagnóstico obrigatórios mas desativa a coleta de dados de diagnóstico opcionais. Microsoft Edge enviará dados de diagnóstico obrigatórios para manter Microsoft Edge seguro, atualizado e em execução conforme o esperado.

'OptionalData' envia dados de diagnóstico opcionais que incluem dados sobre o uso do navegador, sites visitados e relatórios de falha enviados à Microsoft para melhorar o produto e o serviço.

No Windows 7/macOS, esta política controla o envio de dados obrigatórios e opcionais à Microsoft.

Se você não configurar esta política ou desabilitá-la, Microsoft Edge usará a preferência do usuário como padrão.

Mapeamento das opções da política:

* Off (0) = Desativado (Não recomendado)

* RequiredData (1) = Dados obrigatórios

* OptionalData (2) = Dados opcionais

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DiagnosticData
  - Nome da GP: Enviar dados de diagnóstico necessários e opcionais sobre o uso do navegador
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DiagnosticData
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DiagnosticData
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DirectInvokeEnabled
  #### Permitir que os usuários abram arquivos usando o protocolo DirectInvoke
  
  
  #### Versões com suporte:
  - No Windows desde a versão 78 ou posterior

  #### Descrição
  Permitir que os usuários abram arquivos usando o protocolo DirectInvoke. O protocolo DirectInvoke permite que os sites solicitem que o navegador abra arquivos de uma URL específica usando um manipulador de arquivo específico no computador ou dispositivo do usuário.

Se você habilitar ou não configurar essa política, os usuários poderão abrir arquivos usando o protocolo DirectInvoke.

Se você desabilitar essa política, os usuários não poderão abrir arquivos usando o protocolo DirectInvoke. Em vez disso, o arquivo será salvo no sistema de arquivos.

Observação: desabilitar o DirectInvoke pode impedir que certos recursos do Microsoft Office SharePoint Online funcionem conforme o esperado.

Para obter mais informações sobre o DirectInvoke, consulte [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) e [https://go.microsoft.com/fwlink/?linkid=2099871](https://go.microsoft.com/fwlink/?linkid=2099871).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DirectInvokeEnabled
  - Nome da GP: Permitir que os usuários abram arquivos usando o protocolo DirectInvoke
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DirectInvokeEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### Disable3DAPIs
  #### Desabilitar o suporte para APIs de gráficos 3D
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Impeça que páginas da Web acessem a unidade de processamento gráfico (GPU). Especificamente, as páginas da Web não podem acessar a API WebGL e os plug-ins não podem usar a API Pepper 3D.

Se você não configurar ou desabilitar essa política, ela permitirá que as páginas da Web usem a API WebGL e os plug-ins usem a API Pepper 3D. O Microsoft Edge pode, por padrão, ainda exigir que os argumentos da linha de comando sejam passados para usar essas APIs.

Se a política [HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled) estiver definida como false, a configuração da política [Disable3DAPIs](#disable3dapis) será ignorada. É o equivalente a definir a política [Disable3DAPIs](#disable3dapis) como true.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: Disable3DAPIs
  - Nome da GP: Desabilitar o suporte para APIs de gráficos 3D
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: Disable3DAPIs
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: Disable3DAPIs
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DisableScreenshots
  #### Desabilitar as capturas de tela
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Controla se os usuários podem tirar capturas de tela da página do navegador.

Se estiver habilitada, o usuário não poderá tirar capturas de tela usando atalhos do teclado ou APIs de extensão.

Se estiver desabilitada ou você não configurar a política, os usuários poderão tirar capturas de tela.

Observe que esta política controla as capturas de tela tiradas de dentro do próprio navegador. Mesmo se você habilitar esta política, os usuários ainda poderão tirar capturas de tela usando algum método fora do navegador (por exemplo, usando um recurso do sistema operacional ou outro aplicativo).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DisableScreenshots
  - Nome da GP: Desabilitar as capturas de tela
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DisableScreenshots
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DisableScreenshots
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DiskCacheDir
  #### Definir diretório de cache de disco
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Configura o diretório a ser usado para armazenar arquivos armazenados em cache.

Se você habilitar essa política, o Microsoft Edge usará o diretório fornecido, independentemente de o usuário ter especificado o sinalizador "--disk-cache-dir". Para evitar a perda de dados ou outros erros inesperados, não configure essa política para o diretório raiz de um volume ou para um diretório usado para outros fins, pois o Microsoft Edge gerenciará seu conteúdo.

Consulte [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) para obter uma lista de variáveis que você pode usar ao especificar diretórios e caminhos.

Se você não configurar essa política, o diretório de cache padrão será usado, e os usuários poderão substituir o padrão pelo sinalizador de linha de comando "--disk-cache-dir".

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DiskCacheDir
  - Nome da GP: Definir diretório de cache de disco
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DiskCacheDir
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"${user_home}/Edge_cache"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DiskCacheDir
  - Exemplo de valor:
``` xml
<string>${user_home}/Edge_cache</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DiskCacheSize
  #### Definir o tamanho do cache de disco, em bytes
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Configura o tamanho do cache, em bytes, usado para armazenar arquivos no disco.

Se você habilitar esta política, o Microsoft Edge usará o tamanho de cache fornecido, independentemente de o usuário ter especificado ou não o sinalizador "--disk-cache-size". O valor especificado nesta política não é um limite rígido, mas uma sugestão ao sistema de cache; qualquer valor abaixo de alguns megabytes é muito pequeno e será arredondado para um mínimo razoável.

Se você definir o valor desta política como 0, será usado o tamanho de cache padrão, e os usuários não poderão alterá-lo.

Se você não configurar esta política, será usado o tamanho padrão, mas os usuários poderão substituí-lo pelo sinalizador "--disk-cache-size".

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DiskCacheSize
  - Nome da GP: Definir o tamanho do cache de disco, em bytes
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DiskCacheSize
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x06400000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DiskCacheSize
  - Exemplo de valor:
``` xml
<integer>104857600</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DnsOverHttpsMode
  #### Controle o modo DNS-over-HTTPS
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 83 ou posterior

  #### Descrição
  Controle o modo de resolução DNS-over-HTTPS. Observe que essa política só definirá o modo padrão de cada consulta. O modo pode ser substituído por tipos especiais de consultas, como solicitações, para resolver um nome de host de servidor DNS-over-HTTPS.

O modo "off" desabilitará o DNS-over-HTTPS.

O modo "automatic" enviará consultas do DNS-over-HTTPS antes se um servidor DNS-over-HTTPS estiver disponível e puder alternar para o envio de consultas inseguros em caso de erro.

O modo "secure" só enviará consultas DNS-over-HTTPS e falhará ao resolver o erro.

Se você não configurar essa política, o navegador poderá enviar solicitações de DNS-over-HTTPS para um resolvedor associado ao resolvedor de sistema configurado do usuário.

Mapeamento das opções da política:

* off (off) = Desabilite o DNS-over-HTTPS

* automatic (automatic) = Habilite o DNS-over-HTTPS com falhas inseguras

* secure (secure) = Habilite o DNS-over-HTTPS sem falhas inseguras

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DnsOverHttpsMode
  - Nome da GP: Controle o modo DNS-over-HTTPS
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DnsOverHttpsMode
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"off"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DnsOverHttpsMode
  - Exemplo de valor:
``` xml
<string>off</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DnsOverHttpsTemplates
  #### Especificar modelo de URI do resolvedor DNS-over-HTTPS desejado
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 83 ou posterior

  #### Descrição
  O modelo de URI do resolvedor DNS-over-HTTPS desejado. Para especificar vários resolvedores DNS-over-HTTPS, separe os modelos de URI correspondentes por espaços.

Se você definir [DnsOverHttpsMode](#dnsoverhttpsmode) como "secure", essa política deverá ser definida e não poderá estar vazia.

 Se você definir [DnsOverHttpsMode](#dnsoverhttpsmode) como "automatic" e essa política for definida, os modelos de URI especificados serão usados. Se você não definir essa política, os mapeamentos codificados serão usados para tentar atualizar o resolver DNS atual do usuário como um resolvedor DoH operado pelo mesmo provedor.

 Se o modelo URI contiver uma variável dns, as solicitações para o solucionador usarão GET, caso contrário, elas usarão POST.

Os modelos formatados incorretamente serão ignorados.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DnsOverHttpsTemplates
  - Nome da GP: Especificar modelo de URI do resolvedor DNS-over-HTTPS desejado
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: DnsOverHttpsTemplates
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"https://dns.example.net/dns-query{?dns}"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DnsOverHttpsTemplates
  - Exemplo de valor:
``` xml
<string>https://dns.example.net/dns-query{?dns}</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DownloadDirectory
  #### Definir diretório de download
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Configura o diretório a ser usado ao baixar arquivos.

Se você habilitar essa política, o Microsoft Edge usará o diretório fornecido, independentemente de o usuário ter especificado um ou ter optado por ser solicitado a fornecer o local de download a cada vez. Consulte a lista de variáveis que podem ser usadas em [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

Se você desabilitar ou não configurar essa política, o diretório de download padrão será usado, e o usuário poderá alterá-lo.

Se um caminho inválido for definido, o Microsoft Edge usará como padrão o diretório de download padrão do usuário.

Se a pasta especificada pelo caminho não existir, o download iniciará um prompt que pergunta ao usuário onde ele deseja salvar o download.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DownloadDirectory
  - Nome da GP: Definir diretório de download
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: DownloadDirectory
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"\n      Linux-based OSes (including Mac): /home/${user_name}/Downloads\n      Windows: C:\\Users\\${user_name}\\Downloads"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DownloadDirectory
  - Exemplo de valor:
``` xml
<string>
      Linux-based OSes (including Mac): /home/${user_name}/Downloads
      Windows: C:\Users\${user_name}\Downloads</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### DownloadRestrictions
  #### Permitir restrições de download
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Configura o tipo de downloads que o Microsoft Edge bloqueia completamente, sem permitir que os usuários substituam a decisão de segurança.

Defina "BlockDangerousDownloads" para permitir todos os downloads, exceto os que contenham avisos do Microsoft Defender SmartScreen.

Defina "BlockPotentiallyDangerousDownloads" para permitir todos os downloads, exceto os que tenham avisos de downloads potencialmente perigosos ou indesejados do Microsoft Defender SmartScreen.

Defina "BlockAllDownloads" para bloquear todos os downloads.

Se você não configurar essa política ou definir a opção "DefaultDownloadSecurity",  os downloads passarão por restrições de segurança comuns com base nos resultados da análise do Microsoft Defender SmartScreen.

Observe que essas restrições são aplicáveis a downloads do conteúdo da página da Web, bem como à opção de menu de contexto "link de download...". Essas restrições não se aplicam ao salvamento ou ao download da página exibida no momento, nem se aplicam à opção Salvar como PDF nas opções de impressão.

Consulte [https://go.microsoft.com/fwlink/?linkid=2094934](https://go.microsoft.com/fwlink/?linkid=2094934) para obter mais informações sobre o Microsoft Defender SmartScreen.

Mapeamento das opções da política:

* DefaultDownloadSecurity (0) = Não há restrições especiais

* BlockDangerousDownloads (1) = Bloquear downloads perigosos

* BlockPotentiallyDangerousDownloads (2) = Bloquear downloads potencialmente perigosos ou indesejados

* BlockAllDownloads (3) = Bloquear todos os downloads

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: DownloadRestrictions
  - Nome da GP: Permitir restrições de download
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: DownloadRestrictions
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: DownloadRestrictions
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### EdgeCollectionsEnabled
  #### Habilitar o recurso Coleções
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 78 ou posterior

  #### Descrição
  Permite que os usuários acessem o recurso Coleções, onde eles podem coletar, organizar, compartilhar e exportar conteúdo de forma mais eficiente e com a integração do Office.

Se você habilitar ou não configurar essa política, os usuários poderão acessar e usar o recurso Coleções no Microsoft Edge.

Se você desabilitar essa política, os usuários não poderão acessar e usar Coleções no Microsoft Edge.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: EdgeCollectionsEnabled
  - Nome da GP: Habilitar o recurso Coleções
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: EdgeCollectionsEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: EdgeCollectionsEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### EditFavoritesEnabled
  #### Permite que os usuários editem os favoritos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Habilite essa política para permitir que os usuários adicionem, removam e modifiquem os favoritos. Esse é o comportamento padrão se você não configurar a política.

Desabilite essa política para impedir que os usuários adicionem, removam ou modifiquem os favoritos. Eles ainda poderão usar os favoritos existentes.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: EditFavoritesEnabled
  - Nome da GP: Permite que os usuários editem os favoritos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: EditFavoritesEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: EditFavoritesEnabled
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### EnableDeprecatedWebPlatformFeatures
  #### Reabilitar os recursos preteridos da plataforma da Web por um tempo limitado
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica uma lista de recursos da plataforma da Web preteridos que serão temporariamente habilitados novamente.

Essa política permite que você habilite novamente os recursos preteridos da plataforma da Web por tempo limitado. Os recursos são identificados por uma marca de cadeia de caracteres.

Se você não configurar essa política, se a lista estiver vazia ou se um recurso não corresponder a uma das marcas de cadeia de caracteres com suporte, todos os recursos da plataforma da Web preteridos permanecerão desabilitados.

Embora a política propriamente dita tenha suporte nas plataformas acima, o recurso que ela estiver habilitando talvez não esteja disponível em todas as plataformas. Nem todos os recursos da plataforma da Web preteridos podem ser habilitados novamente. Somente os explicitamente listados abaixo podem ser habilitados novamente e apenas por um período de tempo limitado, que difere por recurso. Você pode examinar o intuito subjacente às alterações de recurso da plataforma da Web em https://bit.ly/blinkintents.

O formato geral da marca da cadeia de caracteres é [DeprecatedFeatureName]_EffectiveUntil[yyyymmdd].

Mapeamento das opções da política:

* ExampleDeprecatedFeature (ExampleDeprecatedFeature_EffectiveUntil20080902) = Habilitar a API ExampleDeprecatedFeature até 2008/09/02

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: EnableDeprecatedWebPlatformFeatures
  - Nome da GP: Reabilitar os recursos preteridos da plataforma da Web por um tempo limitado
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures\1 = "ExampleDeprecatedFeature_EffectiveUntil20080902"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: EnableDeprecatedWebPlatformFeatures
  - Exemplo de valor:
``` xml
<array>
  <string>ExampleDeprecatedFeature_EffectiveUntil20080902</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### EnableDomainActionsDownload
  #### Habilitar o download de ações de domínio da Microsoft (obsoleto)
  
  >OBSOLETO: Essa política é obsoleta e não funciona após o Microsoft Edge 84.
  #### Versões com suporte:
  - No Windows e macOS desde 77, até 84

  #### Descrição
  Esta política não funciona porque estados conflitantes devem ser evitados. Esta política era usada para habilitar/desabilitar o download da lista de ações do domínio nem sempre ela atingia esse objetivo. O Serviço de Experimentação  e Configuração, que lida com o download, tem sua própria política para configurar o que deve ser baixado do serviço. No lugar, use a política [ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol).

 NoMicrosoft Edge, as Ações de Domínio representam uma série de recursos de compatibilidade que ajudam o navegador a funcionar corretamente na Web.

A Microsoft mantém uma lista de ações a seguir em alguns domínios por motivo de compatibilidade. Por exemplo, o navegador poderá substituir a cadeia de caracteres do Agente do Usuário em um site caso este não esteja funcionando devido a uma nova cadeia de caracteres do Agente de Usuário no Microsoft Edge. Cada uma dessas ações tem caráter temporário enquanto a Microsoft tenta resolver o problema com o proprietário do site.

Quando o navegador for iniciado e depois periodicamente, o navegador entrará em contato com o Serviço de Experimentação e Configuração que contém a lista de ações de compatibilidade mais recentes a serem executadas. Essa lista é salva no local depois de ser recuperada de forma que as solicitações posteriores atualizarão apenas a lista se a cópia do servidor for alterada.

Se você habilitar esta política, a lista de Ações de Domínio continuará a ser baixada do Serviço de Experimentação e Configuração.

Se você desabilitar esta política, a lista de Ações de Domínio não será mais baixada do Serviço de Experimentação e Configuração.

Se você não configurar esta política, a lista de Ações de Domínio continuará a ser baixada do Serviço de Experimentação e Configuração.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: EnableDomainActionsDownload
  - Nome da GP: Habilitar o download de ações de domínio da Microsoft (obsoleto)
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: EnableDomainActionsDownload
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: EnableDomainActionsDownload
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### EnableOnlineRevocationChecks
  #### Habilitar verificações de OCSP/CRL online
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  As verificações de revogação online não fornecem um benefício de segurança significativo e são desabilitadas por padrão.

Se você habilitar essa política, o Microsoft Edge executará verificações de OCSP/CRL online com falha leve. "Falha leve" significa que, se não for possível acessar o servidor de revogação, o certificado será considerado válido.

Se você desabilitar a política ou não configurá-la, o Microsoft Edge não executará verificações de revogação online.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: EnableOnlineRevocationChecks
  - Nome da GP: Habilitar verificações de OCSP/CRL online
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: EnableOnlineRevocationChecks
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: EnableOnlineRevocationChecks
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### EnableSha1ForLocalAnchors
  #### Permitir certificados assinados usando o SHA-1 quando emitidos por âncoras de confiança locais (preterida)
  >PRETERIDA: essa política foi preterida. No momento, ela tem suporte, mas ficará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - Em Windows e macOS desde 85 ou posterior

  #### Descrição
  Quando essa configuração estiver habilitada, o Microsoft Edge permitirá que as conexões sejam protegidas por certificados assinados por SHA-1, desde que as cadeias de certificados sejam um certificado raiz instalado localmente e sejam válidas.

Observe que essa política depende da pilha de verificação de certificados do sistema operacional (SO), permitindo assinaturas SHA-1. Se a atualização do sistema operacional alterar o gerenciamento do sistema operacional de certificados SHA-1, talvez essa política não tenha mais efeito.  Além disso, a política destina-se a uma solução alternativa temporária para dar mais tempo para que as empresas deixem de usar SHA-1. Essa política será removida no Microsoft Edge 92 que será lançado em meados de 2021.

Se você não definir essa política ou defini-la como falsa ou se o certificado SHA-1 se vincula a uma raiz de certificado confiável publicamente, Microsoft Edge não permitirá certificados assinados por SHA-1.

Essa política só estará disponível em instâncias do Windows que fazem parte de um domínio Microsoft Active Directory, instâncias do Windows 10 Pro ou Enterprise inscritas para gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou associadas a um domínio via MCX.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: EnableSha1ForLocalAnchors
  - Nome da GP: Permitir certificados assinados usando o SHA-1 quando emitidos por âncoras de confiança locais (preterida)
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: EnableSha1ForLocalAnchors
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: EnableSha1ForLocalAnchors
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### EnterpriseHardwarePlatformAPIEnabled
  #### Permitir que extensões gerenciadas usem a API da Plataforma de Hardware Corporativo
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 78 ou posterior

  #### Descrição
  Quando essa política estiver habilitada, as extensões instaladas pela política da empresa têm permissão para usar a API da Plataforma de Hardware Empresarial.
Quando essa política está definida como desabilitada ou não está definida, nenhuma extensão tem permissão para usar a API da Plataforma de Hardware Empresarial.
Essa política também se aplica às extensões de componente.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: EnterpriseHardwarePlatformAPIEnabled
  - Nome da GP: Permitir que extensões gerenciadas usem a API da Plataforma de Hardware Corporativo
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: EnterpriseHardwarePlatformAPIEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: EnterpriseHardwarePlatformAPIEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### EnterpriseModeSiteListManagerAllowed
  #### Permitir o acesso à ferramenta Enterprise Mode Site List Manager
  
  
  #### Versões com suporte:
  - No Windows desde a versão 86 ou posterior

  #### Descrição
  Permite definir se o Enterprise Mode Site List Manager está disponível para os usuários.

Se você habilitar essa política, os usuários poderão ver o botão de navegação Enterprise Mode Site List Manager na página edge://compat, navegar até a ferramenta e usá-la.

Se desabilitar ou não configurar essa política, os usuários não verão o botão de navegação Enterprise Mode Site List Manager e não poderão usá-lo.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: EnterpriseModeSiteListManagerAllowed
  - Nome da GP: Permitir o acesso à ferramenta Enterprise Mode Site List Manager
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: EnterpriseModeSiteListManagerAllowed
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  #### Desabilitar o download de avisos baseados em extensão de tipo de arquivo para tipos de arquivo especificados em domínios
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 85 ou posterior

  #### Descrição
  Você pode habilitar esta política para criar um dicionário de extensões de tipo de arquivo com uma lista correspondente de domínios que serão isentas de avisos de download com base na extensão de tipo de arquivo. Isso permite que os administradores corporativos bloqueiem avisos de download com base na extensão do tipo de arquivo para arquivos associados a um domínio listado. Por exemplo, se a extensão "jnlp" estiver associada a "website1.com", os usuários não verão um aviso ao baixar arquivos "jnlp" de "website1.com", mas receberão um aviso de download ao baixar arquivos "jnlp" de "website2.com".

Os arquivos com extensões de tipo de arquivo especificados para domínios identificados por essa política ainda estarão sujeitos a avisos de segurança baseados em extensão de tipo não arquivo, como avisos de download de conteúdo misto e avisos do Microsoft defender SmartScreen.

Se você desabilitar essa política ou não configurá-la, os tipos de arquivo que disparam avisos de download baseados em extensão mostrarão avisos ao usuário.

Se você habilitar essa política:

* O padrão de URL deve ser formatado de acordo com [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).
* A extensão de tipo de arquivo inserida deve estar em ASCII de maiúsculas e minúsculas. O separador à esquerda não deve ser incluído ao listar a extensão de tipo de arquivo, de modo que a lista "jnlp" deve ser usada em vez de ". jnlp".

Exemplo:

O valor do exemplo a seguir evitará avisos de download com base na extensão de tipo de arquivo nas extensões swf, exe e jnlp para domínios *.contoso.com. Ele mostrará ao usuário um aviso de download com base na extensão de tipo de arquivo em qualquer outro domínio para arquivos exe e jnlp, mas não para arquivos swf.

[
  { "file_extension": "jnlp", "domains": ["contoso.com"] },
  { "file_extension": "exe", "domains": ["contoso.com"] },
{ "file_extension": "swf", "domains": ["*"] }
]

Observe que, enquanto o exemplo anterior mostra a supressão de avisos de download baseados na extensão de tipo de arquivo para arquivos "swf" para todos os domínios, a aplicação de supressão de tais avisos para todos os domínios de qualquer extensão de tipo de arquivo perigosa não é recomendada devido a questões de segurança. Ele é mostrado no exemplo simplesmente para demonstrar a capacidade de fazer isso.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Nome da GP: Desabilitar o download de avisos baseados em extensão de tipo de arquivo para tipos de arquivo especificados em domínios
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\1 = {"domains": ["https://contoso.com", "contoso2.com"], "file_extension": "jnlp"}
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\2 = {"domains": ["*"], "file_extension": "swf"}

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Exemplo de valor:
``` xml
<array>
  <string>{'domains': ['https://contoso.com', 'contoso2.com'], 'file_extension': 'jnlp'}</string>
  <string>{'domains': ['*'], 'file_extension': 'swf'}</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ExperimentationAndConfigurationServiceControl
  #### Controlar a comunicação com o Serviço de Configuração e Experimentação
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  No Microsoft Edge, o Serviço de Configuração e Experimentação é usado para implantar a carga de Configuração e Experimentação.

A carga de Experimentação consiste em uma lista de recursos de desenvolvimento antecipados que a Microsoft está habilitando para testes e comentários.

A carga de configuração consiste em uma lista de configurações que a Microsoft deseja implantar no Microsoft Edge para otimizar a experiência do usuário. Por exemplo, a carga de configuração pode especificar a frequência com que o Microsoft Edge envia solicitações para o Serviço de Configuração e Experimentação para recuperar a carga mais recente.

Além disso, a carga de configuração também pode conter uma lista de ações a serem tomadas em alguns domínios por motivo de compatibilidade. Por exemplo, o navegador pode substituir a cadeia de caracteres do Agente de Usuário em um site caso este esteja quebrado devido a uma nova cadeia de caracteres de Agente de Usuário no Microsoft Edge. Cada uma dessas ações tem caráter temporário enquanto a Microsoft tenta resolver o problema com o proprietário do site.

Se você configurar essa política como o modo "FullMode", a carga total será baixada do Serviço de Configuração e Experimentação. Isso inclui as cargas de configuração e experimentação.

Se você configurar essa política como o modo "ConfigurationsOnlyMode", somente a carga de configuração será entregue.

Se você configurar essa política como "RestrictedMode", a comunicação com o Serviço de Configuração e Experimentação será interrompida completamente.

Se você não configurar essa política, em um dispositivo gerenciado nos canais Estável e Beta, o comportamento será o mesmo que o modo "ConfigurationsOnlyMode".

Se você não configurar essa política, em um dispositivo não gerenciado o comportamento será o mesmo que "FullMode".

Mapeamento das opções da política:

* FullMode (2) = Recuperar configurações e experimentos

* ConfigurationsOnlyMode (1) = Recuperar apenas configurações

* RestrictedMode (0) = Desabilitar a comunicação com o Serviço de Configuração e Experimentação

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ExperimentationAndConfigurationServiceControl
  - Nome da GP: Controlar a comunicação com o Serviço de Configuração e Experimentação
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ExperimentationAndConfigurationServiceControl
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExperimentationAndConfigurationServiceControl
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ExternalProtocolDialogShowAlwaysOpenCheckbox
  #### Mostrar uma caixa de seleção "Sempre abrir" na caixa de diálogo de protocolo externo
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 79 ou posterior

  #### Descrição
  Essa política controla se a caixa de seleção "Sempre permitir que este site abra links deste tipo" é mostrada em solicitações de inicialização do protocolo externo. Esta política só se aplica a links https://.

Se você habilitar essa política, quando uma solicitação de confirmação de protocolo externo for exibida, o usuário poderá selecionar "Sempre permitir" para ignorar todos os avisos de confirmação futuros do protocolo neste site.

Se desabilitar essa política, a caixa de seleção "Sempre permitir" não será exibida. O usuário será solicitado a fornecer uma confirmação sempre que um protocolo externo for chamado.

Antes de Microsoft Edge 83, se você não configurar essa política, a caixa de seleção "Sempre permitir" não será exibida. O usuário será solicitado a fornecer uma confirmação sempre que um protocolo externo for chamado.

Em Microsoft Edge 83, se você não configurar essa política, a visibilidade da caixa de seleção será controlada pelo sinalizador "Habilitar lembretes de aviso de inicialização de protocolo" no edge://flags

A partir de Microsoft Edge 84, se você não configurar essa política, quando uma solicitação de confirmação de protocolo externo for exibida, o usuário poderá selecionar "Sempre permitir" para ignorar todos os avisos de confirmação do protocolo neste site.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Nome da GP: Mostrar uma caixa de seleção "Sempre abrir" na caixa de diálogo de protocolo externo
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### FamilySafetySettingsEnabled
  #### Permitir que os usuários configurem o Family Safety
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 83 ou posterior

  #### Descrição
  Esta política desabilita e oculta completamente a Página de proteção da família em Configurações. A navegação para edge://settings/familysafety também será bloqueada. A Página de proteção da família descreve quais recursos estão disponíveis para grupos de família e como ingressar em um grupo de família. Saiba mais sobre a proteção da família aqui: ([https://go.microsoft.com/fwlink/?linkid=2098432](https://go.microsoft.com/fwlink/?linkid=2098432)).

Se você habilitar esta política ou não configurá-la, a página de proteção da família será mostrada.

Se esta diretiva for desabilitada, a página de proteção da família não será exibida.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: FamilySafetySettingsEnabled
  - Nome da GP: Permitir que os usuários configurem o Family Safety
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: FamilySafetySettingsEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: FamilySafetySettingsEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### FavoritesBarEnabled
  #### Habilitar barra de favoritos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Habilita ou desabilita a barra de favoritos.

Se você habilitar essa política, os usuários verão a barra de favoritos.

Se você desabilitar essa política, os usuários não verão a barra de favoritos.

Se essa política não estiver configurada, o usuário pode optar por usar a barra de favoritos ou não.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: FavoritesBarEnabled
  - Nome da GP: Habilitar barra de favoritos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: FavoritesBarEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: FavoritesBarEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ForceBingSafeSearch
  #### Aplicar a Pesquisa Segura do Bing
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Certifique-se de que as consultas de pesquisa na Web do Bing sejam feitas com a Pesquisa Segura configurada com o valor especificado. Os usuários não podem alterar essa configuração.

Se você configurar esta política como "BingSafeSearchNoRestrictionsMode", a Pesquisa Segura no Bing voltará para o valor de bing.com.

Se você configurar esta política como "BingSafeSearchModerateMode", a configuração moderada será usada na Pesquisa Segura. A configuração moderada filtra vídeos e imagens de teor adulto, mas não textos dos resultados da pesquisa.

Se você configurar esta política como "BingSafeSearchStrictMode", a configuração estrita será usada na Pesquisa Segura. A configuração estrita filtros de texto, imagens e vídeos.

Se você desabilitar esta política ou não configurá-la, a Pesquisa Segura no Bing não será imposta, e os usuários poderão definir o valor que desejarem em bing.com.

Mapeamento das opções da política:

* BingSafeSearchNoRestrictionsMode (0) = Não configurar restrições de pesquisa no Bing

* BingSafeSearchModerateMode (1) = Configurar restrições de pesquisa moderadas no Bing

* BingSafeSearchStrictMode (2) = Configurar restrições de pesquisa rigorosas no Bing

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ForceBingSafeSearch
  - Nome da GP: Aplicar a Pesquisa Segura do Bing
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ForceBingSafeSearch
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ForceBingSafeSearch
  - Exemplo de valor:
``` xml
<integer>0</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ForceCertificatePromptsOnMultipleMatches
  #### Configure se o Microsoft Edge deve selecionar um certificado automaticamente quando houver várias correspondências de certificado para um site configurado com "AutoSelectCertificateForUrls"
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 81 ou posterior

  #### Descrição
  Alterna se os usuários recebem solicitação para selecionar um certificado se houver vários certificados disponíveis e um site estiver configurado com [AutoSelectCertificateForUrls](#autoselectcertificateforurls). Se você não configurar [AutoSelectCertificateForUrls](#autoselectcertificateforurls) para um site, o usuário sempre receberá uma solicitação para selecionar um certificado.

Se você definir essa política como verdadeira, o Microsoft Edge solicitará que um usuário selecione um certificado para sites na lista definida em [AutoSelectCertificateForUrls](#autoselectcertificateforurls) se e somente se houver mais de um certificado.

Se você definir essa política como falsa ou não configurá-la, o Microsoft Edge selecionará automaticamente um certificado mesmo se houver várias correspondências para um certificado. O usuário não receberá uma solicitação para selecionar um certificado para sites na lista definida em [AutoSelectCertificateForUrls](#autoselectcertificateforurls).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ForceCertificatePromptsOnMultipleMatches
  - Nome da GP: Configure se o Microsoft Edge deve selecionar um certificado automaticamente quando houver várias correspondências de certificado para um site configurado com "AutoSelectCertificateForUrls"
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ForceCertificatePromptsOnMultipleMatches
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ForceCertificatePromptsOnMultipleMatches
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ForceEphemeralProfiles
  #### Habilitar o uso de perfis efêmeros
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Controla se os perfis de usuário são alternados para o modo efêmero. Um perfil efêmero é criado quando uma sessão é iniciada, é excluído quando a sessão é encerrada e é associado ao perfil original do usuário.

Se você habilitar essa política, os perfis serão executados no modo efêmero. Isso permite que os usuários trabalhem em seus próprios dispositivos sem salvar dados de navegação nesses dispositivos. Se você habilitar essa política como uma política do sistema operacional (usando o GPO no Windows, por exemplo), ela se aplicará a todos os perfis do sistema.

Se você desabilitar essa política ou não configurá-la, os usuários receberão seus perfis regulares quando entrarem no navegador.

No modo efêmero, os dados do perfil são salvos em disco apenas pela duração da sessão do usuário. Os recursos, como o histórico do navegador, as extensões e seus dados, dados da Web, como cookies e bancos de dados da Web, não são salvos depois que o navegador é fechado. Isso não impede que o usuário baixe manualmente os dados em disco ou salve páginas ou as imprima. Se o usuário tiver habilitado a sincronização, todos os dados serão preservados nas contas de sincronização da mesma forma que os perfis regulares. Os usuários também poderão usar a navegação InPrivate no modo efêmero, a menos que você desabilite isso explicitamente.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ForceEphemeralProfiles
  - Nome da GP: Habilitar o uso de perfis efêmeros
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ForceEphemeralProfiles
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ForceEphemeralProfiles
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ForceGoogleSafeSearch
  #### Forçar a Pesquisa Segura do Google
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Força a realização de consultas na Pesquisa do Google na Web com a Pesquisa Segura definida como ativa e impede que os usuários alterem essa configuração.

Se você habilitar essa política, a Pesquisa Segura na Pesquisa do Google sempre ficará ativa.

Se você desabilitar essa política ou não configurá-la, a Pesquisa Segura não será imposta na Pesquisa do Google.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ForceGoogleSafeSearch
  - Nome da GP: Forçar a Pesquisa Segura do Google
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ForceGoogleSafeSearch
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ForceGoogleSafeSearch
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ForceLegacyDefaultReferrerPolicy
  #### Use a política referencial padrão de no-referrer-when-downgrade. (preterida)
  >PRETERIDA: essa política foi preterida. No momento, ela tem suporte, mas ficará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - Em Windows e macOS desde 81 ou posterior

  #### Descrição
  Essa política foi preterida porque destina-se a ser um mecanismo de curto prazo para dar mais tempo para que as empresas atualizem o conteúdo da Web se e quando ela for incompatível com a política padrão de referência atual. Ele não funcionará na versão 86 do Microsoft Edge.

A política padrão de referência Microsoft Edge está sendo reforçada de seu valor atual de não referência quando faz o downgrade para a forma mais segura, origem estrita quando cruzada por meio de uma implantação gradual.

Antes da distribuição, essa política corporativa não terá efeito. Após a distribuição, quando essa política corporativa estiver habilitada, a política referencial padrão do Microsoft Edge será definida como seu valor anterior de não referência quando faz o downgrade.

Essa política corporativa está desabilitada por padrão.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ForceLegacyDefaultReferrerPolicy
  - Nome da GP: Use a política referencial padrão de no-referrer-when-downgrade. (preterida)
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ForceLegacyDefaultReferrerPolicy
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ForceLegacyDefaultReferrerPolicy
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ForceNetworkInProcess
  #### Aplicar o código de rede a ser executado no processo do navegador (obsoleto)
  
  >OBSOLETO: Essa política é obsoleta e não funciona após o Microsoft Edge 83.
  #### Versões com suporte:
  - No Windows desde 78, até 83

  #### Descrição
  Esta política não funciona porque era pra ser apenas um mecanismo de curto prazo para dar mais tempo para migrar para o software de terceiros que não dependa das APIs de rede. Os servidores proxy são recomendados em relação aos LSPs e ao patch da API do Win32.

Esta política força o código de rede a ser executado no processo do navegador.

Essa política está desabilitada por padrão. Se habilitada, os usuários poderão ter problemas de segurança quando o processo de rede estiver na área restrita.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ForceNetworkInProcess
  - Nome da GP: Aplicar o código de rede a ser executado no processo do navegador (obsoleto)
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ForceNetworkInProcess
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ForceSync
  #### Forçar a sincronização dos dados do navegador e não mostrar a solicitação de consentimento da sincronização
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Força a sincronização de dados no Microsoft Edge. Essa política também impede que o usuário desative a sincronização.

Se você não configurar essa política, os usuários poderão ativar ou desativar a sincronização. Se você habilitar essa política, os usuários não poderão desativar a sincronização.

Para essa política trabalhar conforme o esperado,
[BrowserSignin](#browsersignin) política não deve ser configurada ou deve ser definida como habilitada. Se [ForceSync](#forcesync) estiver definida como desabilitada, [BrowserSignin](#browsersignin) não terá efeito.

[SyncDisabled](#syncdisabled) Não deve ser configurado ou deve ser definido como falso. Se essa configuração estiver definida como verdadeiro, o [ForceSync](#forcesync) não terá efeito.

0 = não iniciar automaticamente a sincronização e mostrar o consentimento da sincronização (padrão)
1 = a sincronização forçada a ser habilitada para o perfil de usuário degradado do AD/Azure AD e não mostrar a solicitação de consentimento da sincronização

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ForceSync
  - Nome da GP: Forçar a sincronização dos dados do navegador e não mostrar a solicitação de consentimento da sincronização
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ForceSync
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ForceSync
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ForceYouTubeRestrict
  #### Aplicar o modo restrito mínimo do YouTube
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Aplica um modo restrito mínimo no YouTube e impede que os usuários escolham um modo menos restrito.

 Defina como "Strict"  para aplicar o modo restrito estrito no YouTube.

Defina como moderado "Moderate" para fazer com que o usuário use apenas o modo restrito moderado e o modo restrito estrito no YouTube. Eles não podem desabilitar o modo restrito.

 Defina como desativado "Off" ou não configure essa política para não aplicar o modo restrito no YouTube. Políticas externas, como políticas do YouTube, ainda podem aplicar o modo restrito.

Mapeamento das opções da política:

* Off (0) = Não aplicar o modo restrito no YouTube

* Moderate (1) = Aplicar pelo menos o modo restrito moderado no YouTube

* Strict (2) = Aplicar modo restrito estrito para o YouTube

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ForceYouTubeRestrict
  - Nome da GP: Aplicar o modo restrito mínimo do YouTube
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ForceYouTubeRestrict
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ForceYouTubeRestrict
  - Exemplo de valor:
``` xml
<integer>0</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### FullscreenAllowed
  #### Permitir modo de tela inteira
  
  
  #### Versões com suporte:
  - No Windows desde a versão 77 ou posterior

  #### Descrição
  Definir a disponibilidade do modo de tela inteira - toda a interface do usuário do Microsoft Edge está oculta e apenas o conteúdo da Web está visível.

Se você habilitar essa política ou não configurá-la, o usuário, os aplicativos e as extensões com as permissões apropriadas poderão entrar no modo tela inteira.

Se essa política for desabilitada, os usuários, os aplicativos e as extensões não poderão entrar no modo tela inteira.

Abrir o Microsoft Edge no modo de quiosque usando a linha de comando não está disponível quando o modo de tela inteira está desabilitado.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: FullscreenAllowed
  - Nome da GP: Permitir modo de tela inteira
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: FullscreenAllowed
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### GloballyScopeHTTPAuthCacheEnabled
  #### Habilitar cache de autenticação HTTP com escopo global
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 81 ou posterior

  #### Descrição
  Esta política configura um único cache global por perfil com credenciais de autenticação de servidor HTTP.

Se você desabilitar ou não configurar esta política, o navegador usará o comportamento padrão de autenticação entre sites, que, a partir da versão 80, será o escopo das credenciais de autenticação do servidor HTTP por site de nível superior. Portanto, se dois sites usarem recursos do mesmo domínio de autenticação, as credenciais deverão ser fornecidas de forma independente no contexto dos dois sites. As credenciais de proxy armazenadas em cache serão reutilizadas em todos os sites.

Se você habilitar esta política, as credenciais de autenticação HTTP inseridas no contexto de um site serão automaticamente usadas no contexto de outro site.

Habilitar esta política deixa os sites abertos para alguns tipos de ataques entre sites e permite que os usuários sejam rastreados entre sites, mesmo sem cookies, adicionando entradas ao cache de autenticação HTTP usando as credenciais inseridas em URLs.

Esta política tem o objetivo de dar às empresas dependentes do comportamento herdado a chance de atualizar seus procedimentos de logon, que serão removidos no futuro.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: GloballyScopeHTTPAuthCacheEnabled
  - Nome da GP: Habilitar cache de autenticação HTTP com escopo global
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: GloballyScopeHTTPAuthCacheEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: GloballyScopeHTTPAuthCacheEnabled
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### GoToIntranetSiteForSingleWordEntryInAddressBar
  #### Forçar a navegação direta em site da intranet, em vez de pesquisar em entradas de palavras únicas na Barra de Endereços
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 78 ou posterior

  #### Descrição
  Se você habilitar esta política, o primeiro resultado da sugestão automática na lista de sugestões da barra de endereços navegará para sites da intranet se o texto digitado na barra de endereços for uma única palavra sem pontuação.

A navegação padrão ao digitar uma única palavra sem pontuação realizará uma navegação para um site da intranet correspondente à palavra digitada.

Se você habilitar esta política, o segundo resultado da sugestão automática na lista de sugestões da barra de endereços realizará uma pesquisa na Web exatamente como foi digitado, contanto que esse texto seja uma única palavra sem pontuação. O provedor de pesquisa padrão será usado, a menos que uma política que impeça a pesquisa na Web também esteja habilitada.

Os dois efeitos da habilitação desta política são:

A navegação para sites em resposta a consultas com uma única palavra que normalmente se resolveriam em um item de histórico não acontecerá mais. Em vez disso, o navegador tentará navegar para sites internos que talvez nem existam na intranet de uma organização. Isso resultará no erro 404.

Termos de pesquisa comuns de uma única palavra exigirão a seleção manual de sugestões de pesquisa para conduzir uma pesquisa de forma adequada.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Nome da GP: Forçar a navegação direta em site da intranet, em vez de pesquisar em entradas de palavras únicas na Barra de Endereços
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### HSTSPolicyBypassList
  #### Configurar a lista de nomes que ignorarão a verificação de política HSTS
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 79 ou posterior

  #### Descrição
  Os nomes de host especificados nesta lista serão isentos da verificação de política HSTS que poderiam potencialmente atualizar solicitações de "http://" para "https://". Somente nomes de host de rótulo único são permitidos nesta política. Os nomes de host devem ser canônicos. Todos os IDNs devem ser convertidos em seu formato de rótulo A, e todas as letras ASCII devem ser minúsculas. Esta política aplica-se somente aos nomes de host específicos especificados; ela não se aplica aos subdomínios dos nomes na lista.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: HSTSPolicyBypassList
  - Nome da GP: Configurar a lista de nomes que ignorarão a verificação de política HSTS
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList\1 = "meet"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: HSTSPolicyBypassList
  - Exemplo de valor:
``` xml
<array>
  <string>meet</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### HardwareAccelerationModeEnabled
  #### Usar aceleração de hardware quando disponível
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifique para usar a aceleração de hardware, se ela estiver disponível. Se você habilitar essa política ou não configurá-la, a aceleração de hardware será habilitada, a menos que um recurso GPU esteja explicitamente bloqueado.

Se essa política for desabilitada, a aceleração de hardware será desabilitada.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: HardwareAccelerationModeEnabled
  - Nome da GP: Usar aceleração de hardware quando disponível
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: HardwareAccelerationModeEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: HardwareAccelerationModeEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### HideFirstRunExperience
  #### Ocultar a Experiência de primeira execução e a tela inicial
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 80 ou posterior

  #### Descrição
  Se você habilitar essa política, a Experiência de primeira execução e a tela inicial não serão mostradas aos usuários quando executarem o Microsoft Edge pela primeira vez.

Para as opções de configuração mostradas na Experiência de Primeira Execução, o navegador usará como padrão o seguinte:

-Na Página Nova Guia, o tipo de feed será definido como MSN Notícias e o layout como Inspiração.

-O usuário ainda será automaticamente conectado ao Microsoft Edge se a conta do Windows for do tipo Azure AD ou MSA.

-A sincronização não será habilitada por padrão, e os usuários poderão ativar a sincronização nas configurações de sincronização.

Se você desabilitar ou não configurar essa política, a Experiência de primeira execução e a Tela Inicial serão mostradas.

Observação: as opções de configuração específicas mostradas ao usuário na Experiência de Primeira Execução também podem ser gerenciadas usando outras políticas específicas. Você pode usar a política HideFirstRunExperience em combinação com essas políticas para configurar uma experiência de navegador específica em seus dispositivos gerenciados. Algumas dessas outras políticas são:

-[AutoImportAtFirstRun](#autoimportatfirstrun)

-[NewTabPageLocation](#newtabpagelocation)

-[NewTabPageSetFeedType](#newtabpagesetfeedtype)

-[SyncDisabled](#syncdisabled)

-[BrowserSignin](#browsersignin)

-[NonRemovableProfileEnabled](#nonremovableprofileenabled)

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: HideFirstRunExperience
  - Nome da GP: Ocultar a Experiência de primeira execução e a tela inicial
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: HideFirstRunExperience
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: HideFirstRunExperience
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ImportAutofillFormData
  #### Permitir importação de dados de formulário de autopreenchimento
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite que os usuários importem dados do formulário de AutoPreenchimento de outro navegador para o Microsoft Edge.

Se você habilitar esta política, a opção para importar dados de AutoPreenchimento manualmente será selecionada automaticamente.

Se você desabilitar esta política, os dados do formulário de AutoPreenchimento não serão importados na primeira execução e os usuários não poderão importá-los manualmente.

Se você não configurar esta política, os dados de AutoPreenchimento serão importados na primeira execução e os usuários poderão optar por importar esses dados manualmente durante as sessões de navegação posteriores.

Você pode definir esta política como uma recomendação. Isso significa que o Microsoft Edge importará os dados de AutoPreenchimento na primeira execução, mas os usuários podem selecionar ou limpar a opção **AutoPreenchimento de dados** durante a importação manual.

**Observação**: Atualmente, esta política gerencia a importação dos navegadores Google Chrome (no Windows 7, 8 e 10 e no macOS) e Mozilla Firefox (no Windows 7, 8 e 10 e no macOS).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ImportAutofillFormData
  - Nome da GP: Permitir importação de dados de formulário de autopreenchimento
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: ImportAutofillFormData
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportAutofillFormData
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ImportBrowserSettings
  #### Permitir a importação das configurações do navegador
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 78 ou posterior

  #### Descrição
  Permite que os usuários importem configurações de outro navegador para o Microsoft Edge.

Se você habilitar esta política, a caixa de seleção “Configurações do navegador” será marcada automaticamente na caixa de diálogo “Importar dados do navegador”.

Se você desabilitar esta política, as configurações do navegador não serão importadas na primeira execução, e os usuários não poderão importá-las manualmente.

Se você não configurar esta política, as configurações do navegador serão importadas na primeira execução, e os usuários poderão optar por importá-las manualmente durante sessões de navegação posteriores.

Você também pode definir esta política como uma recomendação. Isso significa que o Microsoft Edge importará as configurações na primeira execução, mas os usuários poderão marcar ou desmarcar a opção “configurações do navegador” durante a importação manual.

Observação: esta política atualmente gerencia a importação do Google Chrome (no Windows 7, 8 e 10 e no macOS).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ImportBrowserSettings
  - Nome da GP: Permitir a importação das configurações do navegador
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: ImportBrowserSettings
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportBrowserSettings
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ImportCookies
  #### Permitir importação de Cookies
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 81 ou posterior

  #### Descrição
  Permite que os usuários importem Cookies de outro navegador para o Microsoft Edge.

Se você desabilitar esta política, os Cookies não serão importados na primeira execução.

Se você não configurar esta política, os Cookies serão importados na primeira execução.

Você também pode definir esta política como uma recomendação. Isso significa que o Microsoft Edge importará Cookies na primeira execução.

Observação: no momento, esta política gerencia a importação do Google Chrome (no Windows 7, 8 e 10 e no macOS).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ImportCookies
  - Nome da GP: Permitir importação de Cookies
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: ImportCookies
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportCookies
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ImportExtensions
  #### Permitir importação de extensões
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 81 ou posterior

  #### Descrição
  Permite que os usuários importem extensões de outro navegador para o Microsoft Edge.

Se você habilitar esta política, a caixa de seleção **Extensões** será marcada automaticamente na caixa de diálogo **Importar dados do navegador**.

Se você desabilitar esta política, as extensões não serão importadas na primeira execução, e os usuários não poderão importá-las manualmente.

Se você não configurar esta política, as extensões serão importadas na primeira execução, e os usuários poderão optar por importá-las manualmente durante sessões de navegação posteriores.

Você também pode definir esta política como uma recomendação. Isso significa que o Microsoft Edge importará as extensões na primeira execução, mas os usuários poderão marcar ou desmarcar a opção **favoritos** durante a importação manual.

**Observação**: no momento, esta política gerencia a importação do Google Chrome (no Windows 7, 8 e 10 e no macOS).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ImportExtensions
  - Nome da GP: Permitir importação de extensões
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: ImportExtensions
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportExtensions
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ImportFavorites
  #### Permitir importação de favoritos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite que os usuários importem os favoritos de outro navegador para o Microsoft Edge.

Se você habilitar esta política, a caixa de seleção “Favoritos” será selecionada automaticamente na caixa de diálogo “Importar dados do navegador”.

Se você desabilitar esta política, os favoritos não serão importados na primeira execução, e os usuários não poderão importar esses dados manualmente.

Se você não configurar esta política, os favoritos serão importados na primeira execução, e os usuários poderão optar por importá-los manualmente durante as sessões de navegação posteriores.

Você também pode definir esta política como uma recomendação. Isso significa que o Microsoft Edge importa os favoritos na primeira execução, mas os usuários poderão marcar ou desmarcar a opção “Favoritos” durante a importação manual.

Observação: esta política gerencia atualmente a importação dos navegadores Internet Explorer (no Windows 7, 8 e 10), Google Chrome (no Windows 7, 8 e 10 e macOS), Mozilla Firefox (no Windows 7, 8 e 10 e macOS) e Apple Safari (macOS).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ImportFavorites
  - Nome da GP: Permitir importação de favoritos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: ImportFavorites
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportFavorites
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ImportHistory
  #### Permitir a importação do histórico de navegação
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite que os usuários importem o histórico de navegação de outro navegador para o Microsoft Edge.

Se você habilitar esta política, a caixa de seleção “Histórico de navegação” será selecionada automaticamente na caixa de diálogo **Importar dados do navegador**.

Se esta política for desabilitada, os dados do histórico de navegação não serão importados na primeira execução, e os usuários não poderão importar esses dados manualmente.

Se você não configurar esta política, os dados de histórico de navegação serão importados na primeira execução, e os usuários poderão optar por importá-los manualmente durante sessões de navegação posteriores.

Você também pode definir esta política como uma recomendação. Isso significa que o Microsoft Edge importa o histórico de navegação na primeira execução, mas os usuários poderão marcar ou desmarcar a opção “histórico” durante a importação manual.

Observação: atualmente, esta política gerencia a importação dos navegadores Internet Explorer (no Windows 7, 8 e 10), Google Chrome (no Windows 7, 8 e 10 e macOS), Mozilla Firefox (no Windows 7, 8 e 10 e macOS) e Apple Safari (macOS).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ImportHistory
  - Nome da GP: Permitir a importação do histórico de navegação
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: ImportHistory
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportHistory
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ImportHomepage
  #### Permitir a importação das configurações da home page
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite que os usuários importem a configuração da página inicial de outro navegador para o Microsoft Edge.

Se você habilitar esta política, a opção para importar manualmente a configuração da página inicial será selecionada automaticamente.

Se esta política for desabilitada, a configuração da página inicial não será importada na primeira execução, e os usuários não poderão importá-la manualmente.

Se você não configurar esta política, a configuração da página inicial será importada na primeira execução, e os usuários poderão optar por importar esses dados manualmente durante sessões de navegação posteriores.

Você pode definir esta política como uma recomendação. Isso significa que o Microsoft Edge importa a configuração da página inicial na primeira execução, mas os usuários poderão marcar ou desmarcar a opção “página inicial” durante a importação manual.

Observação: esta política atualmente gerencia a importação do Internet Explorer (no Windows 7, 8 e 10).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ImportHomepage
  - Nome da GP: Permitir a importação das configurações da home page
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ImportHomepage
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportHomepage
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ImportOpenTabs
  #### Permitir importação de guias abertas
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 79 ou posterior

  #### Descrição
  Permite que os usuários importem configurações de outro navegador para o Microsoft Edge.

Se você habilitar essa política, a caixa de seleção **Configurações do navegador** será marcada automaticamente na caixa de diálogo **Importar dados do navegador**.

Se você desabilitar essa política, as configurações do navegador não serão importadas na primeira execução, e os usuários não poderão importá-las manualmente.

Se você não configurar essa política, as configurações do navegador serão importadas na primeira execução, e os usuários poderão optar por importá-las manualmente durante sessões de navegação posteriores.

Você também pode definir essa política como uma recomendação. Isso significa que o Microsoft Edge importará as configurações na primeira execução, mas os usuários poderão marcar ou desmarcar a opção ** configurações do navegador** durante a importação manual.

**Observação**: essa política atualmente gerencia a importação do Google Chrome (no Windows 7, 8 e 10 e no macOS).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ImportOpenTabs
  - Nome da GP: Permitir importação de guias abertas
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: ImportOpenTabs
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportOpenTabs
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ImportPaymentInfo
  #### Permitir importação de informações de pagamento
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite que os usuários importem informações de pagamento de outro navegador para o Microsoft Edge.

Se você habilitar esta política, a caixa de seleção “informações de pagamento” será selecionada automaticamente na caixa de diálogo “Importar dados do navegador”.

Se esta política for desabilitada, as informações de pagamento não serão importadas na primeira execução, e os usuários não poderão importá-las manualmente.

Se você não configurar esta política, as informações de pagamento serão importadas na primeira execução, e os usuários poderão optar por importá-las manualmente durante sessões de navegação posteriores.

Você também pode definir esta política como uma recomendação. Isso significa que o Microsoft Edge importa informações de pagamento na primeira execução, mas os usuários poderão marcar ou desmarcar a opção “informações de pagamento” durante a importação manual.

Observação: esta política atualmente gerencia a importação do Google Chrome (no Windows 7, 8 e 10 e no macOS).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ImportPaymentInfo
  - Nome da GP: Permitir importação de informações de pagamento
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: ImportPaymentInfo
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportPaymentInfo
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ImportSavedPasswords
  #### Permitir a importação de senhas salvas
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite que os usuários importem senhas salvas de outro navegador para o Microsoft Edge.

Se você habilitar esta política, a opção de importar manualmente as senhas salvas será selecionada automaticamente.

Se você desabilitar esta política, as senhas salvas não serão importadas na primeira execução e os usuários não poderão importá-las manualmente.

Se você não configurar esta política, as senhas serão importadas na primeira execução e os usuários poderão optar por importá-las manualmente durante as sessões de navegação posteriores.

Você pode definir esta política como uma recomendação. Isso significa que o Microsoft Edge importa senhas na primeira execução, mas os usuários podem marcar ou desmarcar a opção **senhas** durante a importação manual.

**Observação**: Atualmente, esta política gerencia a importação a partir dos navegadores Internet Explorer (no Windows 7, 8 e 10), Google Chrome (no Windows 7, 8 e 10 e no macOS) e Mozilla Firefox (no Windows 7, 8 e 10 e no macOS).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ImportSavedPasswords
  - Nome da GP: Permitir a importação de senhas salvas
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: ImportSavedPasswords
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportSavedPasswords
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ImportSearchEngine
  #### Permitir importação das configurações do mecanismo de pesquisa
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite que os usuários importem as configurações do mecanismo de pesquisa de outro navegador para o Microsoft Edge.

Se você habilitar esta política, a opção para importar as configurações do mecanismo de pesquisa será selecionada automaticamente.

Se esta política for desabilitada, as configurações do mecanismo de pesquisa não serão importadas na primeira execução, e os usuários não poderão importá-las manualmente.

Se você não configurar esta política, as configurações do mecanismo de pesquisa serão importadas na primeira execução, e os usuários poderão optar por importar esses dados manualmente durante sessões de navegação posteriores.

Você pode definir esta política como uma recomendação. Isso significa que o Microsoft Edge importa as configurações do mecanismo de pesquisa na primeira execução, mas os usuários podem marcar ou desmarcar a opção “mecanismo de pesquisa” durante a importação manual.

Observação: esta política atualmente gerencia a importação do Internet Explorer (no Windows 7, 8 e 10).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ImportSearchEngine
  - Nome da GP: Permitir importação das configurações do mecanismo de pesquisa
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: ImportSearchEngine
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportSearchEngine
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ImportShortcuts
  #### Permitir importação de atalhos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 81 ou posterior

  #### Descrição
  Permite que os usuários importem Atalhos de outro navegador para o Microsoft Edge.

Se você desabilitar esta política, os Atalhos não serão importados na primeira execução.

Se você não configurar esta política, os Atalhos serão importados na primeira execução.

Você também pode definir esta política como recomendação. Isso significa que o Microsoft Edge importa os Atalhos na primeira execução.

Observação: esta política atualmente gerencia a importação do Google Chrome (no Windows 7, 8 e 10 e no macOS).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ImportShortcuts
  - Nome da GP: Permitir importação de atalhos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: ImportShortcuts
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ImportShortcuts
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### InPrivateModeAvailability
  #### Configurar a disponibilidade do modo InPrivate
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica se o usuário pode abrir páginas no modo InPrivate no Microsoft Edge.

Se você não configurar essa política ou defini-la como "Enabled", os usuários poderão abrir páginas no modo InPrivate.

Defina esta política como "Disabled" para impedir que os usuários usem o modo InPrivate.

Defina esta política como "Forced" para usar sempre o modo InPrivate.

Mapeamento das opções da política:

* Enabled (0) = Modo InPrivate disponível

* Disabled (1) = Modo InPrivate desabilitado

* Forced (2) = Modo InPrivate aplicado

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: InPrivateModeAvailability
  - Nome da GP: Configurar a disponibilidade do modo InPrivate
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: InPrivateModeAvailability
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: InPrivateModeAvailability
  - Exemplo de valor:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### InsecureFormsWarningsEnabled
  #### Habilitar avisos para formulários não seguros
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Essa política controla o tratamento de formulários inseguros (formulários enviados em HTTP) inseridos em sites seguros (HTTPS) no navegador. Se você habilitar essa política ou não a definir, um aviso de página inteira será mostrado quando um formulário não seguro for enviado.
Além disso, uma bolha de aviso será exibida ao lado dos campos de formulário quando eles forem prioritários, e o preenchimento automático será desabilitado para esses formulários.
Se você desabilitar essa política, os avisos não serão exibidos para os formulários inseguros, e o AutoPreenchimento funcionará normalmente.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: InsecureFormsWarningsEnabled
  - Nome da GP: Habilitar avisos para formulários não seguros
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: InsecureFormsWarningsEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: InsecureFormsWarningsEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### IntensiveWakeUpThrottlingEnabled
  #### Controlar o recurso de IntensiveWakeUpThrottling
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 85 ou posterior

  #### Descrição
  Quando habilitada, o recurso de IntensiveWakeUpThrottling faz com que os cronômetros de JavaScript nas guias de tela de fundo sejam regulados e agrupados agressivamente, executando não mais que uma vez por minuto depois que uma página tiver sido executada por 5 minutos ou mais.

Este é um recurso compatível com os padrões da web, mas ele pode dividir a funcionalidade em alguns sites, fazendo com que determinadas ações sejam atrasadas em até um minuto. No entanto, isso resulta em economias significativas de CPU e bateria quando habilitada. Consulte https://bit.ly/30b1XR4 para obter mais detalhes.

Se você habilitar essa política, o recurso será forçado a habilitar, e os usuários não poderão substituir essa configuração.
Se você desabilitar essa política, o recurso será forçado a desabilitar e os usuários não poderão substituir essa configuração.
          Se você não configurar essa política, o recurso será controlado por sua própria lógica interna. Os usuários podem definir essa configuração manualmente.

Observe que a política é aplicada por processo de renderização, com o valor mais recente da configuração de política em vigor quando um processo de processamento é iniciado. É necessária uma reinicialização completa para garantir que todas as guias carregadas recebam uma configuração de política consistente. É inofensiva para que processos sejam executados com valores diferentes desta política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: IntensiveWakeUpThrottlingEnabled
  - Nome da GP: Controlar o recurso de IntensiveWakeUpThrottling
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: IntensiveWakeUpThrottlingEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: IntensiveWakeUpThrottlingEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### InternetExplorerIntegrationEnhancedHangDetection
  #### Configurar detecção de travamento aprimorada no modo Internet Explorer
  
  
  #### Versões com suporte:
  - No Windows desde a versão 84 ou posterior

  #### Descrição
  A detecção avançada de bloqueio é uma abordagem mais detalhada para detectar páginas da Web travadas no modo Internet Explorer do que a usada pelo Internet Explorer autônomo. Quando uma página da Web travada é detectada, o navegador aplica uma mitigação para impedir que o restante do navegador trave.

  Essa configuração permite definir o uso da detecção de falha avançada caso tenha problemas incompatíveis com qualquer um dos seus sites. Recomendamos desabilitar esta política somente se surgir notificações como "(site) não está respondendo" no modo Internet Explorer, mas não no Internet Explorer autônomo.

 Essa configuração funciona em conjunto com:
 [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) definido como "IEMode"
 e
 a política[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) onde a lista tem pelo menos uma entrada.

 Se você definir esta política como "Enabled" ou não a configurar, os sites que estiverem executando no modo Internet Explorer usarão a detecção de falha avançada.

Se você definir esta política como "Disabled", a detecção de falha avançada será desabilitada, e os usuários receberão o comportamento de detecção básica do Internet Explorer.

 Para saber mais sobre o modo Internet Explorer, confira [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Mapeamento das opções da política:

* Disabled (0) = Detecção avançada de bloqueio desabilitada

* Enabled (1) = Detecção avançada de bloqueio habilitada

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: InternetExplorerIntegrationEnhancedHangDetection
  - Nome da GP: Configurar detecção de travamento aprimorada no modo Internet Explorer
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: InternetExplorerIntegrationEnhancedHangDetection
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### InternetExplorerIntegrationLevel
  #### Configurar a integração com o Internet Explorer
  
  
  #### Versões com suporte:
  - No Windows desde a versão 77 ou posterior

  #### Descrição
  Para obter orientações sobre como configurar a experiência ideal para o modo do Internet Explorer, consulte [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Mapeamento das opções da política:

* None (0) = Nenhum

* IEMode (1) = Modo Internet Explorer

* NeedIE (2) = Internet Explorer 11

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: InternetExplorerIntegrationLevel
  - Nome da GP: Configurar a integração com o Internet Explorer
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: InternetExplorerIntegrationLevel
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### InternetExplorerIntegrationSiteList
  #### Configurar a Lista de Sites do Modo Empresarial
  
  
  #### Versões com suporte:
  - No Windows desde a versão 78 ou posterior

  #### Descrição
  Para obter orientações sobre como configurar a experiência ideal para o modo do Internet Explorer, consulte [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: InternetExplorerIntegrationSiteList
  - Nome da GP: Configurar a Lista de Sites do Modo Empresarial
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: InternetExplorerIntegrationSiteList
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"https://internal.contoso.com/sitelist.xml"
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### InternetExplorerIntegrationSiteRedirect
  #### Especificar como as navegações "em página" para sites não configurados se comportam ao iniciar em páginas do modo do Internet Explorer
  
  
  #### Versões com suporte:
  - No Windows desde a versão 81 ou posterior

  #### Descrição
  Uma navegação "na página" é iniciada a partir de um link, um script ou um formulário na página atual. Também pode ser um redirecionamento do lado do servidor de uma tentativa de navegação "na página" anterior. Por outro lado, um usuário pode iniciar uma navegação que não seja "na página" e que seja independente da página atual de várias maneiras, usando os controles do navegador. Por exemplo, usando a barra de endereços, o botão Voltar ou um link favorito.

 Essa configuração permite especificar se as navegações de páginas carregadas no modo Internet Explorer para sites não configurados (que não estão configurados na Lista de Sites do Modo Empresarial) serão revertidas para o Microsoft Edge ou permanecerão no modo Internet Explorer.

 Essa configuração funciona em conjunto com:
 [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) está definida como "IEMode"
 e
 a política [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) em que a lista possui pelo menos uma entrada.

 Se você desabilitar ou não configurar esta política, somente os sites configurados para serem abertos no modo Internet Explorer serão abertos nesse modo. Os sites não configurados para abrir no modo Internet Explorer serão redirecionados de volta ao Microsoft Edge.

 Se você definir esta política como"Default", apenas sites configurados para abrir no modo Internet Explorer abrirão neste modo. Os sites não configurados para abrir no modo Internet Explorer serão redirecionados ao Microsoft Edge.

Se você definir esta política como AutomaticNavigationsOnly (valor 1), terá a experiência padrão exceto que todas as navegações automáticas (como redirecionamentos 302) para sites não configurados serão mantidas no modo Internet Explorer.

 Se você definir esta política como AllInPageNavigations (valor 2), todas as navegações de páginas carregadas no modo IE para sites não configurados serão mantidas no modo Internet Explorer (menos recomendado)

.        Para saber mais sobre o modo Internet Explorer, acesse [https://go.microsoft.com/fwlink/?linkid=2105106](https://go.microsoft.com/fwlink/?linkid=2105106)

Mapeamento das opções da política:

* Default (0) = Padrão

* AutomaticNavigationsOnly (1) = Manter somente as navegações automáticas no modo do Internet Explorer

* AllInPageNavigations (2) = Manter todas as navegações na página no modo do Internet Explorer

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: InternetExplorerIntegrationSiteRedirect
  - Nome da GP: Especificar como as navegações "em página" para sites não configurados se comportam ao iniciar em páginas do modo do Internet Explorer
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: InternetExplorerIntegrationSiteRedirect
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### InternetExplorerIntegrationTestingAllowed
  #### Permitir o teste do modo Internet Explorer
  
  
  #### Versões com suporte:
  - No Windows desde a versão 86 ou posterior

  #### Descrição
  Essa política é um substituto para a política de sinalizador do modo do IE. Permite que os usuários abram uma guia do modo IE na opção de menu UI.

Essa configuração funciona em conjunto com o:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) Está definida como ' IEMode '
e
[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) política onde a lista tem pelo menos uma entrada.

Se você habilitar essa política, os usuários poderão abrir a guia modo de exibição do IE da opção IU e navegar para o site atual para um site do IE.

Se você desabilitar essa política, os usuários não poderão ver a opção IU no menu diretamente.

Se você não configurar essa política, poderá configurar o sinalizador de teste do modo IE manualmente.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: InternetExplorerIntegrationTestingAllowed
  - Nome da GP: Permitir o teste do modo Internet Explorer
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: InternetExplorerIntegrationTestingAllowed
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### IsolateOrigins
  #### Habilitar isolamento de site para origens específicas
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica as origens para executar isoladamente, em seus próprios processos.
Essa política também isola origens indicadas por subdomínios. Por exemplo, especificar https://contoso.com/ causará o isolamento de https://foo.contoso.com/ como parte do site https://contoso.com/.
Se a política estiver habilitada, cada uma das origens indicadas em uma lista separada por vírgulas será executada em seu próprio processo.
Se essa política for desabilitada, os recursos [IsolateOrigins](#isolateorigins) e [SitePerProcess](#siteperprocess) serão desabilitados. Os usuários ainda podem habilitar a política [IsolateOrigins](#isolateorigins) manualmente, por meio de sinalizadores de linha de comando.
Se você não configurar a política, o usuário poderá alterar essa configuração.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: IsolateOrigins
  - Nome da GP: Habilitar isolamento de site para origens específicas
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: IsolateOrigins
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"https://contoso.com/,https://fabrikam.com/"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: IsolateOrigins
  - Exemplo de valor:
``` xml
<string>https://contoso.com/,https://fabrikam.com/</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### LocalProvidersEnabled
  #### Permitir sugestões de fornecedores locais
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 83 ou posterior

  #### Descrição
  Permita sugestões de provedores de sugestão no dispositivo (provedores locais), por exemplo, Favoritos e Histórico de Navegação, na Barra de Endereços e na Lista de Sugestão Automática do Microsoft Edge.

Se você habilitar esta política, serão usadas sugestões de provedores locais.

Se você desabilitar esta política, nunca serão usadas sugestões de provedores locais. O histórico local e as sugestões de favoritos locais não aparecerão.

Se você não configurar esta política, serão permitidas sugestões de provedores locais, mas o usuário poderá alterar isso usando a alternância de configurações.

Observe que alguns recursos podem não estar disponíveis se uma política para desabilitar esse recurso tiver sido aplicada. Por exemplo, as sugestões do Histórico de Navegação não estarão disponíveis se você habilitar a política [SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled).

Esta política requer a reinicialização do navegador para concluir a aplicação.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: LocalProvidersEnabled
  - Nome da GP: Permitir sugestões de fornecedores locais
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: LocalProvidersEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: LocalProvidersEnabled
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ManagedFavorites
  #### Configurar favoritos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Configura uma lista de favoritos gerenciados.

A política cria uma lista de favoritos. Cada favorito contém as chaves "name" e "url", que contêm o nome do favorito e seu destino. Você pode configurar uma subpasta definindo favoritos sem uma chave "url", mas com uma chave "children" adicional contendo uma lista de favoritos, conforme definido acima (alguns dos quais poderão ser pastas novamente). O Microsoft Edge corrige as URLs incompletas como se elas fossem enviadas pela Barra de Endereços, por exemplo, "microsoft.com" torna-se "https://microsoft.com/".

Esses favoritos são colocados em uma pasta que não pode ser modificada pelo usuário (mas o usuário pode ocultá-la da barra de favoritos). Por padrão, o nome da pasta é "Favoritos gerenciados", mas você pode alterá-la adicionando à lista de favoritos um dicionário contendo a chave "toplevel_name" com o nome de pasta desejado como o valor.

Os favoritos gerenciados não são sincronizados com a conta de usuário e não podem ser modificados por extensões.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Dicionário

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ManagedFavorites
  - Nome da GP: Configurar favoritos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ManagedFavorites
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
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


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ManagedFavorites
  - Exemplo de valor:
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
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ManagedSearchEngines
  #### Gerenciar Mecanismos de Pesquisa
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite configurar uma lista de até 10 mecanismos de pesquisa, um dos quais deve ser marcado como o mecanismo de pesquisa padrão.
Você não precisa especificar a codificação. A partir do Microsoft Edge 80, os parâmetros suggest_url e image_search_url são opcionais. O parâmetro opcional, image_search_post_params (consiste em pares de nome/valor separados por vírgula), está disponível a partir do Microsoft Edge 80.

A partir do Microsoft Edge 83, você pode ativar a descoberta do mecanismo de pesquisa com o parâmetro opcional allow_search_engine_discovery. Esse parâmetro deve ser o primeiro item da lista. Se allow_search_engine_discovery não for especificado, a descoberta do mecanismo de pesquisa será desativada por padrão. A partir do Microsoft Edge 84, você pode definir esta política como uma política recomendada para permitir a descoberta do provedor de pesquisa. Não é necessário adicionar o parâmetro opcional allow_search_engine_discovery.

Se você habilitar esta política, os usuários não poderão adicionar, remover ou alterar nenhum mecanismo de pesquisa da lista. Os usuários podem definir seu mecanismo de pesquisa padrão para qualquer mecanismo de pesquisa na lista.

Se você desabilitar ou não configurar esta política, os usuários poderão modificar a lista de mecanismos de pesquisa conforme desejado.

Se a política [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) for definida, esta política (ManagedSearchEngines) será ignorada. O usuário deve reiniciar o navegador para concluir a aplicação desta política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Dicionário

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ManagedSearchEngines
  - Nome da GP: Gerenciar Mecanismos de Pesquisa
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: ManagedSearchEngines
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
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


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ManagedSearchEngines
  - Exemplo de valor:
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
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### MaxConnectionsPerProxy
  #### Número máximo de conexões simultâneas com o servidor proxy
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica o número máximo de conexões simultâneas com o servidor proxy.

Alguns servidores proxy não podem manipular um alto número de conexões simultâneas por cliente. Você pode resolver isso configurando essa política como um valor menor.

O valor dessa política deve ser inferior a 100 e maior do que 6. O valor padrão é 32.

Alguns aplicativos Web são conhecidos por consumir muitas conexões com GETs pendentes. Reduzir o máximo de conexões abaixo 32 pode travar o navegador se vários desses aplicativos Web estiverem abertos.

Se você não configurar essa política, o valor padrão (32) será usado.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: MaxConnectionsPerProxy
  - Nome da GP: Número máximo de conexões simultâneas com o servidor proxy
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: MaxConnectionsPerProxy
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000020
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: MaxConnectionsPerProxy
  - Exemplo de valor:
``` xml
<integer>32</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### MediaRouterCastAllowAllIPs
  #### Permitir que o Google Cast se conecte a dispositivos Cast em todos os endereços IP
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Habilite essa política para permitir que o Google Cast conecte-se a dispositivos Cast em todos os endereços IP, e não apenas em endereços privados RFC1918/RFC4193.

Desabilite essa política para restringir o Google Cast a dispositivos Cast em endereços privados RFC1918/RFC4193.

Se você não configurar essa política, o Google Cast se conectará a dispositivos Cast somente em endereços privados RFC1918/RFC4193, a menos que você habilite o recurso CastAllowAllIPs.

Se a política [EnableMediaRouter](#enablemediarouter) estiver desabilitada, essa política não terá efeito.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: MediaRouterCastAllowAllIPs
  - Nome da GP: Permitir que o Google Cast se conecte a dispositivos Cast em todos os endereços IP
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: MediaRouterCastAllowAllIPs
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: MediaRouterCastAllowAllIPs
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### MetricsReportingEnabled
  #### Habilitar relatórios de dados relacionados a uso e falhas (preterida)
  >PRETERIDA: essa política foi preterida. No momento, ela tem suporte, mas ficará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Essa política foi preterida. Ela tem suporte no momento, mas se tornará obsoleta no Microsoft Edge 89. Essa política foi substituída pela nova política: [DiagnosticData](#diagnosticdata)no Windows 7, no Windows 8 e no macOS. Essa política foi substituída por Permitir Telemetria no Win 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

Essa política habilita o relatório de dados relacionados a uso e falhas sobre o Microsoft Edge à Microsoft.

Habilite essa política para enviar relatórios de dados relacionados a uso e falhas à Microsoft. Desabilite essa política para não enviar os dados à Microsoft. Em ambos os casos, os usuários não podem alterar ou substituir a configuração.

No Windows 10, se você não configurar essa política, o Microsoft Edge usará como padrão a configuração de dados de diagnóstico do Windows. Se você habilitar essa política, o Microsoft Edge enviará dados de uso somente se a configuração de dados de diagnóstico do Windows for Aprimorado ou Completo. Se você desabilitar essa política, o Microsoft Edge não enviará dados de uso. Os dados relacionados a falhas são baseados na configuração de dados de diagnóstico do Windows. Saiba mais sobre as configurações de dados de diagnóstico do Windows em [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

No Windows 7, Windows 8 e macOS, essa política controla o envio de dados relacionados a uso e falhas. Se essa política não for configurada, o Microsoft Edge usará como padrão a preferência do usuário.

 Para habilitar essa política [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) deve ser definido como habilitado. Se [MetricsReportingEnabled](#metricsreportingenabled) ou [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) estiverem Não Configurados ou estiverem Desabilitados, esses dados não serão enviados para  a Microsoft.

Essa política está disponível apenas em instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, instâncias do Windows 10 Pro ou Enterprise registradas para o gerenciamento de dispositivos ou instâncias do macOS que são gerenciadas via MDM ou associadas a um domínio via MCX.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: MetricsReportingEnabled
  - Nome da GP: Habilitar relatórios de dados relacionados a uso e falhas (preterida)
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: MetricsReportingEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: MetricsReportingEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### NativeWindowOcclusionEnabled
  #### Habilitar Oclusão de Janela Nativa
  
  
  #### Versões com suporte:
  - No Windows desde a versão 84 ou posterior

  #### Descrição
  Habilitar oclusão de janela nativa no Microsoft Edge.

Se você habilitar essa configuração, para reduzir o consumo de energia e CPU, o Microsoft Edge detectará quando uma janela é coberta por outras janelas e suspenderá os pixels da pintura do trabalho.

Se você desabilitar essa configuração, o Microsoft Edge não detectará quando uma janela é coberta por outras janelas.

Se essa política não for definida, a detecção de ocultar janelas será habilitada.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NativeWindowOcclusionEnabled
  - Nome da GP: Habilitar Oclusão de Janela Nativa
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: NativeWindowOcclusionEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### NavigationDelayForInitialSiteListDownloadTimeout
  #### Definir um tempo limite para o atraso da navegação de guia para a Lista de Sites do Modo Empresarial
  
  
  #### Versões com suporte:
  - No Windows desde a versão 84 ou posterior

  #### Descrição
  Permite que você defina um tempo limite, em segundos, para guias do Microsoft Edge aguardando para navegar até que o navegador baixe a Lista de Sites do Modo Empresarial inicial.

Essa configuração funciona em conjunto com o:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) está definido como "IEMode"
e política
[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist), onde a lista tem pelo menos uma entrada
 e
[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload) está definida como "Todas as navegações elegíveis" (1). As guias

não aguardam mais do que esse tempo limite para que a Lista de Sites do Modo Empresarial seja baixada. Se o navegador não tiver terminado de baixar a Lista de Sites do Modo Empresarial quando o tempo limite expirar, as guias Microsoft Edge continuarão a navegar. O valor do tempo limite não deve ser maior que 20 segundos e não ser menor que 1 segundo.

Se você definir o tempo limite nesta política como um valor maior que o padrão de 2 segundos, uma barra de informações será exibida para o usuário após 2 segundos. A barra de informações contém um botão que permite ao usuário parar de aguardar o download da Lista de Sites do Modo Empresarial para concluir.

Se você não configurar essa política, o tempo limite padrão de 2 segundos será utilizado. Esse padrão está sujeito a alterações futuras.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NavigationDelayForInitialSiteListDownloadTimeout
  - Nome da GP: Definir um tempo limite para o atraso da navegação de guia para a Lista de Sites do Modo Empresarial
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: NavigationDelayForInitialSiteListDownloadTimeout
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x0000000a
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### NetworkPredictionOptions
  #### Habilitar previsão de rede
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Habilita a previsão de rede e impede que os usuários alterem essa configuração.

Isso controla a pré-busca de DNS, a pré-conexão TCP e SSL e a pré-renderização de páginas da Web.

Se você não configurar essa política, a previsão de rede será habilitada, mas o usuário poderá alterá-la.

Mapeamento das opções da política:

* NetworkPredictionAlways (0) = Prever ações de rede em qualquer conexão de rede

* NetworkPredictionWifiOnly (1) = Não tem suporte, se esse valor for usado, ele será tratado como se 'Prever ações de rede em qualquer conexão de rede' (0) estivesse definido

* NetworkPredictionNever (2) = Não prever ações de rede em qualquer conexão de rede

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NetworkPredictionOptions
  - Nome da GP: Habilitar previsão de rede
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: NetworkPredictionOptions
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: NetworkPredictionOptions
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### NonRemovableProfileEnabled
  #### Configurar se um usuário sempre tem um perfil padrão conectado automaticamente à sua conta corporativa ou de estudante
  
  
  #### Versões com suporte:
  - No Windows desde a versão 78 ou posterior

  #### Descrição
  Essa política determina se usuário pode remover o perfil do Microsoft Edge conectado automaticamente com a conta corporativa ou de estudante.

Se você habilitar, um perfil não removível será criado com a conta corporativa ou de estudante do usuário no Windows. Esse perfil não pode ser desconectado nem removido.

Se você desabilitar ou não configurar essa política, o perfil conectado automaticamente com a conta corporativa ou de estudante de um usuário do Windows pode ser desconectado ou removido pelo usuário.

Se você quiser configurar a entrada do navegador, use a política [BrowserSignin](#browsersignin).

 Essa política está disponível somente em instâncias do Windows que fazem parte de um domínio do Microsoft Active Directory, instâncias do Windows 10 Pro ou Enterprise registradas para o gerenciamento de dispositivos.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: NonRemovableProfileEnabled
  - Nome da GP: Configurar se um usuário sempre tem um perfil padrão conectado automaticamente à sua conta corporativa ou de estudante
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: NonRemovableProfileEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### OverrideSecurityRestrictionsOnInsecureOrigin
  #### Controlar onde se aplicam a restrições de segurança em origens não seguras
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica uma lista de origens (URLs) ou padrões de nome de host (como "*.contoso.com") para que as restrições de segurança relativas às origens inseguras não se apliquem.

Essa política permite que você especifique as origens permitidas para aplicativos herdados que não é podem implantar o TLS nem configurar um servidor de preparo para desenvolvimento para a Web interno de forma que os desenvolvedores possam testar os recursos que exigem contextos seguros sem precisar implantar o TLS no servidor de preparo. Essa política também impede que a origem seja rotulada como "Não Segura" na omnibox.

A definição de uma lista de URLs nessa política terá o mesmo efeito que a configuração do sinalizador de linha de comando '--unsafely-treat-insecure-origin-as-secure' para uma lista separada por vírgulas das mesmas URLs. Se você habilitar essa política, ela substituirá o sinalizador de linha de comando.

Para obter mais informações sobre os contextos seguros, consulte https://www.w3.org/TR/secure-contexts/.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: OverrideSecurityRestrictionsOnInsecureOrigin
  - Nome da GP: Controlar onde se aplicam a restrições de segurança em origens não seguras
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\1 = "http://testserver.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\2 = "*.contoso.com"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: OverrideSecurityRestrictionsOnInsecureOrigin
  - Exemplo de valor:
``` xml
<array>
  <string>http://testserver.contoso.com/</string>
  <string>*.contoso.com</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PaymentMethodQueryEnabled
  #### Permitir que sites consultem os métodos de pagamento disponíveis
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 80 ou posterior

  #### Descrição
  Permite definir se os sites podem verificar se o usuário tem métodos de pagamento salvos.

Se você desabilitar essa política, os sites que usarem as APIs PaymentRequest.canMakePayment ou PaymentRequest.hasEnrolledInstrument serão informadas de que nenhum método de pagamento estará disponível.

Se você habilitar essa política ou não defini-la, os sites poderão verificar se o usuário tem métodos de pagamento salvos.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PaymentMethodQueryEnabled
  - Nome da GP: Permitir que sites consultem os métodos de pagamento disponíveis
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: PaymentMethodQueryEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PaymentMethodQueryEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PersonalizationReportingEnabled
  #### Permitir personalização de anúncios, pesquisa e notícias enviando histórico de navegação à Microsoft
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 80 ou posterior

  #### Descrição
  Esta política impede que a Microsoft colete o histórico de navegação do Microsoft Edge do usuário para ser usado para personalizar publicidade, pesquisa, notícias e outros serviços da Microsoft.

Esta configuração está disponível somente para usuários com uma conta Microsoft. Esta configuração não está disponível para contas de criança ou contas corporativas.

Se você desabilitar esta política, os usuários não poderão alterar ou substituir a configuração. Se esta política estiver habilitada ou não configurada, o Microsoft Edge usará a preferência do usuário como padrão.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PersonalizationReportingEnabled
  - Nome da GP: Permitir personalização de anúncios, pesquisa e notícias enviando histórico de navegação à Microsoft
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: PersonalizationReportingEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PersonalizationReportingEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PinningWizardAllowed
  #### Permitir o Assistente para fixar na barra de tarefas
  
  
  #### Versões com suporte:
  - No Windows desde a versão 80 ou posterior

  #### Descrição
  O Microsoft Edge usa o Assistente para fixar na barra de tarefas para ajudar os usuários a fixar sites sugeridos na barra de tarefas. O recurso Fixar na barra de tarefas é habilitado por padrão e pode ser acessado pelo usuário por meio do menu Configurações e mais.

Se você habilitar essa política ou não configurá-la, os usuários poderão chamar o Assistente para fixar na barra de tarefas no menu Configurações e mais. O Assistente também pode ser chamado por meio de uma inicialização de protocolo.

Se você desabilitar essa política, o Assistente para fixar na barra de tarefas será desabilitado no menu e não poderá ser chamado por meio de uma inicialização de protocolo.

As configurações do usuário para habilitar ou desabilitar o Assistente para fixar na barra de tarefas não estão disponíveis.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PinningWizardAllowed
  - Nome da GP: Permitir o Assistente para fixar na barra de tarefas
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: PinningWizardAllowed
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ProactiveAuthEnabled
  #### Habilitar a Autenticação Proativa
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite configurar se a Autenticação Proativa deve ser ativada.

Se você habilitar essa política, o Microsoft Edge tentará autenticar de forma proativa o usuário conectado com os serviços Microsoft. Em intervalos regulares, o Microsoft Edge verifica em um serviço online um manifesto atualizado com a configuração que rege como fazer isso.

Se você desabilitar essa política, o Microsoft Edge não tentará autenticar de forma proativa o usuário conectado com os serviços Microsoft. O Microsoft Edge não verifica mais em um serviço online se há um manifesto atualizado com a configuração para fazer isso.

Se você não configurar essa política, a Autenticação Proativa será ativada.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ProactiveAuthEnabled
  - Nome da GP: Habilitar a Autenticação Proativa
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ProactiveAuthEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ProactiveAuthEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PromotionalTabsEnabled
  #### Habilitar conteúdo promocional em toda a guia
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Controla a apresentação de conteúdo promocional ou educativo em uma guia inteira. Esta configuração controla a apresentação de páginas de boas-vindas que ajudam os usuários a entrar no Microsoft Edge, escolher o navegador padrão ou saber mais sobre os recursos do produto.

Se você habilitar esta política (defini-la como true) ou não a configurar, o Microsoft Edge poderá mostrar conteúdo em uma guia inteira aos usuários para fornecer informações sobre o produto.

Se você desabilitar (definir como false) esta política, o Microsoft Edge não poderá mostrar o conteúdo em uma guia inteira aos usuários.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PromotionalTabsEnabled
  - Nome da GP: Habilitar conteúdo promocional em toda a guia
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: PromotionalTabsEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PromotionalTabsEnabled
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### PromptForDownloadLocation
  #### Perguntar onde salvar os arquivos baixados
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define se deve-se perguntar onde salvar um arquivo antes de baixá-lo.

Se você habilitar essa política, será perguntado ao usuário onde salvar cada arquivo antes de baixar; se você não configurá-la, os arquivos serão salvos automaticamente no local padrão, sem perguntar ao usuário.

Se você não configurar essa política, o usuário poderá alterar essa configuração.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: PromptForDownloadLocation
  - Nome da GP: Perguntar onde salvar os arquivos baixados
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: PromptForDownloadLocation
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: PromptForDownloadLocation
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### QuicAllowed
  #### Permitir o protocolo QUIC
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite o uso do protocolo QUIC no Microsoft Edge.

Se você habilitar essa política ou não configurá-la, o protocolo QUIC será permitido.

Se essa política for desabilitada, o protocolo QUIC será bloqueado.

QUIC é um protocolo de rede de camada de transporte que pode melhorar o desempenho dos aplicativos Web que atualmente usam o TCP.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: QuicAllowed
  - Nome da GP: Permitir o protocolo QUIC
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: QuicAllowed
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: QuicAllowed
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### RelaunchNotification
  #### Notificar um usuário de que uma reinicialização do navegador é recomendada ou necessária para atualizações pendentes
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Notifique os usuários de que eles precisam reiniciar o Microsoft Edge para aplicar uma atualização pendente.

Se você não configurar essa política, o Microsoft Edge adicionará um ícone de reciclagem na extremidade direita da barra de menus superior para solicitar que os usuários reiniciem o navegador para aplicar a atualização.

Se você habilitar essa política e defini-la como "Recommended", um aviso recorrente indicará aos usuários que uma reinicialização é recomendada. Os usuários podem ignorar esse aviso e adiar a reinicialização.

Se você configurar a política como "Required",  um aviso recorrente indicará aos usuários que o navegador será reiniciado automaticamente assim que um período de notificação passar. O período padrão é de sete dias. Você pode configurar esse período com a política [RelaunchNotificationPeriod](#relaunchnotificationperiod).

A sessão do usuário é restaurada quando o navegador é reiniciado.

Mapeamento das opções da política:

* Recommended (1) = Recomendável - Mostrar um prompt recorrente para o usuário indicando a recomendação de uma reinicialização

* Required (2) = Obrigatório - Mostra um prompt recorrente para o usuário indicando que uma reinicialização é necessária

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: RelaunchNotification
  - Nome da GP: Notificar um usuário de que uma reinicialização do navegador é recomendada ou necessária para atualizações pendentes
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: RelaunchNotification
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: RelaunchNotification
  - Exemplo de valor:
``` xml
<integer>1</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### RelaunchNotificationPeriod
  #### Definir o período para notificações de atualização
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite definir o período de tempo em milissegundos, quando os usuários são notificados de que Microsoft Edge devem ser reiniciados para aplicar uma atualização pendente.

Durante este período de tempo, o usuário será reportado repetidamente da necessidade de uma atualização. O Microsoft Edge menu do aplicativo é alterado para indicar que um reinício é necessário quando uma terceira notificação passar o período. Essa notificação mudará de cor uma vez que dois terços do período de notificação passaram e novamente quando o período de notificação total tiver passado. As notificações adicionais habilitadas pela [RelaunchNotification](#relaunchnotification) política seguem a mesma programação.

Se não estiver definido, o período padrão de 604800000 de milissegundos (uma semana) será usado.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: RelaunchNotificationPeriod
  - Nome da GP: Definir o período para notificações de atualização
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: RelaunchNotificationPeriod
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x240c8400
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: RelaunchNotificationPeriod
  - Exemplo de valor:
``` xml
<integer>604800000</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### RendererCodeIntegrityEnabled
  #### Habilitar integridade do código do renderizador
  
  
  #### Versões com suporte:
  - No Windows desde a versão 78 ou posterior

  #### Descrição
  Se essa política for habilitada ou não for definida, a Integridade do Código do Renderizador será habilitada. Essa política deve ser desabilitada somente se forem encontrados problemas de compatibilidade com softwares de terceiros que devem ser executados nos processos de renderização do Microsoft Edge.

Desabilitar essa política tem um efeito prejudicial sobre a segurança e a estabilidade do Microsoft Edge, pois o código desconhecido e potencialmente hostil poderá ser carregado dentro dos processos de renderização do Microsoft Edge.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: RendererCodeIntegrityEnabled
  - Nome da GP: Habilitar integridade do código do renderizador
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: RendererCodeIntegrityEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### RequireOnlineRevocationChecksForLocalAnchors
  #### Especificar se as verificações OCSP/CRL online são necessárias para âncoras de confiança locais
  
  
  #### Versões com suporte:
  - No Windows desde a versão 77 ou posterior

  #### Descrição
  Controla se as verificações de revogação online (verificações OCSP/CRL) são necessárias. Se o Microsoft Edge não puder obter informações do status de revogação, esses certificados serão tratados como revogados ("falha irrecuperável").

Se você habilitar esta política, o Microsoft Edge sempre executará a verificação de revogação para certificados de servidores com validação bem-sucedida e assinados por certificados de Autoridade de Certificação instalados localmente.

Se você não configurar ou desabilitar esta política, o Microsoft Edge usará as configurações de revogação online existentes.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: RequireOnlineRevocationChecksForLocalAnchors
  - Nome da GP: Especificar se as verificações OCSP/CRL online são necessárias para âncoras de confiança locais
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: RequireOnlineRevocationChecksForLocalAnchors
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ResolveNavigationErrorsUseWebService
  #### Habilitar a resolução de erros de navegação usando um serviço Web
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permita que o Microsoft Edge emita uma conexão sem dados para um serviço Web para sondar redes em busca de conectividade em casos como o Wi-Fi em hotéis e aeroportos.

Se você habilitar essa política, um serviço Web será usado para testes de conectividade de rede.

Se você desabilitar essa política, o Microsoft Edge usará APIs nativas para tentar resolver os problemas de conectividade e de navegação de rede.

**Observação**: exceto no Windows 8 e em versões posteriores do Windows, o Microsoft Edge *sempre* usará APIs nativas para resolver problemas de conectividade.

Se você não configurar essa política, o Microsoft Edge respeitará a preferência do usuário definida em Serviços, em edge://settings/privacy.
Especificamente, há uma alternância **Usar um serviço Web para ajudar a resolver erros de navegação**, que o usuário pode ativar ou desativar. Esteja ciente de que, se essa política tiver sido habilitada (ResolveNavigationErrorsUseWebService), a configuração **Usar um serviço Web para ajudar a resolver erros de navegação** será ativada, mas o usuário não poderá alterá-la usando a alternância. Se você tiver desabilitado essa política, a configuração **Usar um serviço Web para ajudar a resolver erros de navegação** será desativada, e o usuário não poderá alterá-la usando a alternância.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ResolveNavigationErrorsUseWebService
  - Nome da GP: Habilitar a resolução de erros de navegação usando um serviço Web
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: ResolveNavigationErrorsUseWebService
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ResolveNavigationErrorsUseWebService
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### RestrictSigninToPattern
  #### Restringir quais contas podem ser usadas como contas principais do Microsoft Edge
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Determina quais contas podem ser definidas como contas principais do navegador no Microsoft Edge (a conta escolhida durante o fluxo de aceitação da sincronização).

Se um usuário tentar configurar uma conta primária do navegador com um nome de usuário que não corresponda a esse padrão, ele será bloqueado e receberá a mensagem de erro apropriada. Você pode configurar essa política para corresponder a várias contas usando uma expressão regular no estilo Perl para o padrão. Observe que as correspondências padrão diferenciam maiúsculas de minúsculas. Para obter mais informações sobre as regras de expressão regular usadas, consulte https://go.microsoft.com/fwlink/p/?linkid=2133903.

        Se você não configurar essa política ou deixá-la em branco, os usuários poderão definir qualquer conta como uma conta primária do navegador no Microsoft Edge.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: RestrictSigninToPattern
  - Nome da GP: Restringir quais contas podem ser usadas como contas principais do Microsoft Edge
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: RestrictSigninToPattern
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
".*@contoso.com"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: RestrictSigninToPattern
  - Exemplo de valor:
``` xml
<string>.*@contoso.com</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### RoamingProfileLocation
  #### Definir o diretório de perfil de roaming
  
  
  #### Versões com suporte:
  - No Windows desde a versão 85 ou posterior

  #### Descrição
  Configura o diretório a ser usado para armazenar a cópia de perfis de roaming.

Se você habilitar essa política, Microsoft Edge usa o diretório fornecido para armazenar uma cópia de roaming dos perfis, desde que você também tenha habilitado a política de [RoamingProfileSupportEnabled](#roamingprofilesupportenabled). Se você desabilitar a política de [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) ou não configurá-lo, o valor armazenado nesta política não será utilizado.

Consulte [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) para obter uma lista de variáveis que você pode usar.

Se você não configurar essa política, o caminho de perfil móvel padrão será usado.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: RoamingProfileLocation
  - Nome da GP: Definir o diretório de perfil de roaming
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: RoamingProfileLocation
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"${roaming_app_data}\\edge-profile"
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### RoamingProfileSupportEnabled
  #### Habilitar o uso de cópias móveis para dados de perfil do Microsoft Edge
  
  
  #### Versões com suporte:
  - No Windows desde a versão 85 ou posterior

  #### Descrição
  Habilite essa política para usar perfis móveis no Windows. As configurações armazenadas em perfis do Microsoft Edge (favoritos e preferências) também serão salvas em um arquivo armazenado na pasta de Perfil de usuário móvel (ou o local especificado pelo administrador pela política [RoamingProfileLocation](#roamingprofilelocation)).

Se você desabilitar essa política ou não a configurar, somente os perfis locais serão usados.

A política de [SyncDisabled](#syncdisabled) desabilita toda a sincronização de dados, substituindo a política.

Veja https://docs.microsoft.com/windows-server/storage/folder-redirection/deploy-roaming-user-profiles para saber mais sobre como usar perfis de usuários móveis.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: RoamingProfileSupportEnabled
  - Nome da GP: Habilitar o uso de cópias móveis para dados de perfil do Microsoft Edge
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: RoamingProfileSupportEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### RunAllFlashInAllowMode
  #### Estender a configuração do conteúdo em Adobe Flash a todo o conteúdo
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Se você habilitar essa política, todo o conteúdo Adobe Flash inserido em sites que estão configurados para permitir Adobe Flash nas configurações de conteúdo, pelo usuário ou pela política da empresa, será executado. Isso inclui o conteúdo de outras origens e/ou conteúdo pequeno.

Para controlar os sites que têm permissão para executar Adobe Flash, consulte as especificações nas políticas [DefaultPluginsSetting](#defaultpluginssetting), [PluginsAllowedForUrls](#pluginsallowedforurls) e [PluginsBlockedForUrls](#pluginsblockedforurls).

Se você desabilitar essa política ou não configurá-la, o conteúdo do Adobe Flash de outras origens (de sites que não são especificados nas três políticas mencionadas acima) ou conteúdo pequeno talvez seja bloqueado.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: RunAllFlashInAllowMode
  - Nome da GP: Estender a configuração do conteúdo em Adobe Flash a todo o conteúdo
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: RunAllFlashInAllowMode
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: RunAllFlashInAllowMode
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SSLErrorOverrideAllowed
  #### Permitir que os usuários continuem a partir da página de aviso HTTPS
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  O Microsoft Edge mostra uma página de aviso quando os usuários visitam sites que têm erros de SSL.

Se você habilitar ou não configurar (padrão) essa política, os usuários poderão clicar nessas páginas de aviso.

Se você desabilitar essa política, os usuários serão impedidos de clicar em qualquer página de aviso.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SSLErrorOverrideAllowed
  - Nome da GP: Permitir que os usuários continuem a partir da página de aviso HTTPS
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: SSLErrorOverrideAllowed
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SSLErrorOverrideAllowed
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SSLVersionMin
  #### Versão mínima do TLS habilitada
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define a versão mínima com suporte do SSL. Se você não definir essa política, o Microsoft Edge usará uma versão mínima do padrão, o TLS 1.0.

Se habilitar essa política, você poderá definir a versão mínima com um dos seguintes valores: "TLSv1", "TLSv1.1" or "TLSv1.2". Quando definida, o Microsoft Edge não usará uma versão do SSL/TLS menor do que a versão especificada. Os valores não reconhecidos serão ignorados.

Mapeamento das opções da política:

* TLSv1 (tls1) = TLS 1.0

* TLSv1.1 (tls1.1) = TLS 1.1

* TLSv1.2 (tls1.2) = TLS 1.2

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SSLVersionMin
  - Nome da GP: Versão mínima do TLS habilitada
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: SSLVersionMin
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"tls1"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SSLVersionMin
  - Exemplo de valor:
``` xml
<string>tls1</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SaveCookiesOnExit
  #### Salvar cookies quando o Microsoft Edge fechar
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Quando essa política estiver habilitada, o conjunto especificado de cookies estará isento da exclusão quando o navegador for fechado. Essa política só será eficaz quando:
- A opção "Cookies e outros dados do site" estiver configurada em Configurações/Privacidade e serviços/Limpar dados de navegação no fechamento ou
- A política [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) estiver habilitada ou
- A política[DefaultCookiesSetting](#defaultcookiessetting) estiver definida como "Manter cookies pela duração da sessão".

Você pode definir uma lista de sites, com base em padrões de URL, que terão seus cookies preservados entre as sessões.

 Observação: os usuários ainda podem editar a lista de sites de cookies para adicionar ou remover URLs. No entanto, eles não podem remover URLs adicionadas por um Administrador.

Se você habilitar essa política, a lista de cookies não será limpa quando o navegador for fechado.

 Se você desabilitar ou não configurar essa política, a configuração pessoal do usuário será usada.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SaveCookiesOnExit
  - Nome da GP: Salvar cookies quando o Microsoft Edge fechar
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SaveCookiesOnExit
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SavingBrowserHistoryDisabled
  #### Desabilitar o salvamento do histórico do navegador
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Desabilita o salvamento do histórico do navegador e impede que os usuários alterem essa configuração.

Se você habilitar essa política, o histórico de navegação não será salvo. Isso também desabilita a sincronização de guias.

Se você desabilitar essa política ou não configurá-la, o histórico de navegação será salvo.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SavingBrowserHistoryDisabled
  - Nome da GP: Desabilitar o salvamento do histórico do navegador
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: SavingBrowserHistoryDisabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SavingBrowserHistoryDisabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ScreenCaptureAllowed
  #### Permitir ou negar captura de tela
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 83 ou posterior

  #### Descrição
  Se você habilitar esta política ou não configurá-la, uma página da Web poderá usar APIs de compartilhamento de tela (por exemplo, getDisplayMedia() ou a API de extensão de Captura de Área de Trabalho) para uma captura de tela.
Se você desabilitar esta política, as chamadas para APIs de compartilhamento de tela falharão. Por exemplo, se você estiver usando uma reunião online baseada na Web, o compartilhamento de vídeo ou tela não funcionará.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ScreenCaptureAllowed
  - Nome da GP: Permitir ou negar captura de tela
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ScreenCaptureAllowed
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ScreenCaptureAllowed
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ScrollToTextFragmentEnabled
  #### Ativar rolagem para textos especificados nos fragmentos da URL
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 83 ou posterior

  #### Descrição
  Esse recurso permite que as navegações de URL de hiperlink e barra de endereço direcionem texto específico em uma página da Web, que será rolada para depois que a página da Web terminar de ser carregada.

Se você habilitar ou não configurar esta política, a rolagem de páginas da Web para fragmentos de texto específicos por meio de uma URL será habilitada.

Se você desabilitar esta política, a rolagem de páginas da Web para fragmentos de texto específicos por meio de uma URL será desabilitada.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ScrollToTextFragmentEnabled
  - Nome da GP: Ativar rolagem para textos especificados nos fragmentos da URL
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ScrollToTextFragmentEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ScrollToTextFragmentEnabled
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SearchSuggestEnabled
  #### Habilitar sugestões de pesquisa
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Habilita sugestões de pesquisa na Web na Barra de Endereço do Microsoft Edge e na Lista de Sugestão Automática e impede que os usuários alterem essa política.

Se você habilitar essa política, serão usadas sugestões de pesquisa da Web.

Se você desabilitar essa política, as sugestões de pesquisa da Web nunca serão usadas. Contudo, as sugestões do histórico local e dos favoritos locais ainda serão exibidas. Se você desabilitar essa política, nem os caracteres digitados, nem as URLs visitadas serão incluídos na telemetria para a Microsoft.

Se essa política não for definida, as sugestões de pesquisa serão habilitadas, mas o usuário poderá alterá-la.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SearchSuggestEnabled
  - Nome da GP: Habilitar sugestões de pesquisa
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: SearchSuggestEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SearchSuggestEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SecurityKeyPermitAttestation
  #### Sites ou domínios que não precisam de permissão para usar o atestado de Chave de Segurança direto
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica os sites e os domínios que não precisam de permissão explícita do usuário quando certificados de atestado de chaves de segurança são solicitados. Além disso, um sinal é enviado para a chave de segurança que indica que eles podem usar o atestado individual. Sem isso, os usuários serão avisados toda vez que um site solicitar o atestado de chaves de segurança.

Sites (como https://contoso.com/some/path) se correspondem apenas com appIDs U2F. Domínios (como contoso.com) se correspondem apenas com IDs RP webauthn. Para cobrir APIs U2F e webauthn para um determinado site, será necessário listar o domínio e a URL de appID.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SecurityKeyPermitAttestation
  - Nome da GP: Sites ou domínios que não precisam de permissão para usar o atestado de Chave de Segurança direto
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation\1 = "https://contoso.com"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SecurityKeyPermitAttestation
  - Exemplo de valor:
``` xml
<array>
  <string>https://contoso.com</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SendIntranetToInternetExplorer
  #### Enviar todos os sites da intranet para o Internet Explorer
  
  
  #### Versões com suporte:
  - No Windows desde a versão 77 ou posterior

  #### Descrição
  Para obter orientações sobre como configurar a experiência ideal para o modo do Internet Explorer, consulte [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SendIntranetToInternetExplorer
  - Nome da GP: Enviar todos os sites da intranet para o Internet Explorer
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: SendIntranetToInternetExplorer
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SendSiteInfoToImproveServices
  #### Enviar informações do site para melhorar os serviços Microsoft (preterida)
  >PRETERIDA: essa política foi preterida. No momento, ela tem suporte, mas ficará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Essa política foi preterida. Ela tem suporte no momento, mas se tornará obsoleta no Microsoft Edge 89. Essa política foi substituída pela nova política: [DiagnosticData](#diagnosticdata)no Windows 7, no Windows 8 e no macOS. Essa política foi substituída por Permitir Telemetria no Win 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

     Esta política permite o envio de informações sobre sites visitados no Microsoft Edge à Microsoft para melhorar serviços como pesquisa.

Habilite esta política para enviar informações sobre sites visitados no Microsoft Edge para a Microsoft. Desabilite essa política para não enviar informações sobre sites visitados no Microsoft Edge à Microsoft. Em ambos os casos, os usuários não podem alterar ou substituir a configuração.

     No Windows 10, se você não configurar essa política, o Microsoft Edge usará como padrão a configuração de dados de diagnóstico do Windows. Se essa política estiver habilitada, o Microsoft Edge enviará informações sobre sites visitados no Microsoft Edge somente se a configuração de dados de diagnóstico estiver configurada como Completa. Se essa política for desabilitada, o Microsoft Edge não enviará informações sobre sites visitados. Saiba mais sobre as configurações de dados de diagnóstico do Windows em [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

     No Windows 7, Windows 8 e macOS, essa política controla as informações sobre sites visitados. Se essa política não for configurada, o Microsoft Edge usará como padrão a preferência do usuário.

     Para habilitar essa política [MetricsReportingEnabled](#metricsreportingenabled) deve ser definido como habilitado. Se [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) ou [MetricsReportingEnabled](#metricsreportingenabled) estiverem Não Configurados ou estiverem Desabilitados, esses dados não serão enviados para  a Microsoft.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SendSiteInfoToImproveServices
  - Nome da GP: Enviar informações do site para melhorar os serviços Microsoft (preterida)
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: SendSiteInfoToImproveServices
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SendSiteInfoToImproveServices
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SensorsAllowedForUrls
  #### Permitir o acesso a sensores em sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Define uma lista de sites, com base em padrões de URL, que podem solicitar acesso do usuário a uma porta serial.

Se você não configurar essa política, o valor padrão global da política de  [DefaultSensorsSetting](#defaultsensorssetting) (se definido) ou da configuração pessoal do usuário será usado para todos os sites.

Para padrões de URL que não correspondem a essa política, a ordem de precedência a seguir é usada: a política de  [SensorsBlockedForUrls](#sensorsblockedforurls) (se houver uma correspondência), a política de [DefaultSensorsSetting](#defaultsensorssetting)  (se definida) ou as configurações pessoais do usuário.

Os padrões de URL definidos nesta política não podem entrar em conflito com aqueles configurados na política de  [SensorsBlockedForUrls](#sensorsblockedforurls). Você não pode permitir e bloquear uma URL.

Para obter informações detalhadas sobre padrões de URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SensorsAllowedForUrls
  - Nome da GP: Permitir o acesso a sensores em sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SensorsAllowedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SensorsBlockedForUrls
  #### Bloquear o acesso a sensores em sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Defina uma lista de sites, com base em padrões de URL, que não podem acessar sensores, como sensores de movimento e Light.

Se você não configurar essa política, o valor padrão global da política [DefaultSensorsSetting](#defaultsensorssetting) (se definida) ou a configuração pessoal do usuário será usada para todos os sites.

De padrões de URL que não correspondam a essa política, a seguinte ordem de precedência é usada: a política de [SensorsAllowedForUrls](#sensorsallowedforurls) (se houver uma correspondência), a política de [DefaultSensorsSetting](#defaultsensorssetting) (se definida) ou as configurações pessoais do usuário.

Os padrões de URL definidos nesta política não podem entrar em conflito com aqueles configurados na política de [SensorsAllowedForUrls](#sensorsallowedforurls). Você não pode permitir e bloquear uma URL.

Para obter informações detalhadas sobre os padrões de URL válidos, confira [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SensorsBlockedForUrls
  - Nome da GP: Bloquear o acesso a sensores em sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SensorsBlockedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SerialAskForUrls
  #### Permitir a API serial em sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Define uma lista de sites, com base em padrões de URL, que podem solicitar acesso do usuário a uma porta serial.

Se você não configurar essa política, o valor padrão global da política de  [DefaultSerialGuardSetting](#defaultserialguardsetting) (se definido) ou da configuração pessoal do usuário será usado para todos os sites.

Para padrões de URL que não correspondem a essa política, a ordem de precedência a seguir é usada: a política de  [SerialBlockedForUrls](#serialblockedforurls) (se houver uma correspondência), a política de [DefaultSerialGuardSetting](#defaultserialguardsetting)  (se definida) ou as configurações pessoais do usuário.

Os padrões de URL definidos nesta política não podem entrar em conflito com aqueles configurados na política de  [SerialBlockedForUrls](#serialblockedforurls). Você não pode permitir e bloquear uma URL.

Para obter informações detalhadas sobre padrões de URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SerialAskForUrls
  - Nome da GP: Permitir a API serial em sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SerialAskForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SerialBlockedForUrls
  #### Bloquear a API serial em sites específicos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Define uma lista de sites, com base em padrões de URL, que não podem pedir ao usuário que lhes conceda acesso a uma porta serial.

Se você não configurar essa política, o valor padrão global da política de [DefaultSerialGuardSetting](#defaultserialguardsetting)  (se definida) ou da configuração pessoal do usuário será usado para todos os sites.

Para padrões de URL que não correspondem a essa política, a ordem de precedência a seguir é usada: a política de [SerialAskForUrls](#serialaskforurls) (se houver uma correspondência), a política de [DefaultSerialGuardSetting](#defaultserialguardsetting) (se definida) ou as configurações pessoais do usuário.

Os padrões de URL nesta política não podem entrar em conflito com aqueles configurados na política de [SerialAskForUrls](#serialaskforurls). Você não pode permitir e bloquear uma URL..

Para obter informações detalhadas sobre padrões de URL válidos, consulte [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SerialBlockedForUrls
  - Nome da GP: Bloquear a API serial em sites específicos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SerialBlockedForUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### ShowOfficeShortcutInFavoritesBar
  #### Mostrar o atalho do Microsoft Office na barra Favoritos
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica se deve-se incluir um atalho para Office.com na barra de favoritos. Para usuários conectados ao Microsoft Edge, o atalho leva-os para seus documentos e aplicativos do Microsoft Office.

Se essa política estiver habilitada ou não estiver configurada, os usuários poderão optar por ver o atalho. Basta alterar a alternância no menu de contexto da barra de favoritos.

Se a política estiver desabilitada, o atalho não será mostrado.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: ShowOfficeShortcutInFavoritesBar
  - Nome da GP: Mostrar o atalho do Microsoft Office na barra Favoritos
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: ShowOfficeShortcutInFavoritesBar
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: ShowOfficeShortcutInFavoritesBar
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SignedHTTPExchangeEnabled
  #### Habilitar o suporte para o Signed HTTP Exchange (SXG)
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 78 ou posterior

  #### Descrição
  Habilite o suporte para o SXG (Signed HTTP Exchange).

Se essa política não for configurada ou for configurada como habilitada, o Microsoft Edge aceitará o conteúdo da Web fornecido como SXG.

Se essa política estiver configurada como desabilitada, o SXG não poderá ser carregado.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SignedHTTPExchangeEnabled
  - Nome da GP: Habilitar o suporte para o Signed HTTP Exchange (SXG)
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: SignedHTTPExchangeEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SignedHTTPExchangeEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SitePerProcess
  #### Habilitar isolamento de sites para todos os sites
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  A política [SitePerProcess](#siteperprocess) pode ser usada para impedir que os usuários recusem o comportamento padrão de isolamento de todos os sites. Observe que você também pode usar a política [IsolateOrigins](#isolateorigins) para isolar origens adicionais, mais refinadas.
Se você habilitar esta política, os usuários não poderão recusar o comportamento padrão em que cada site executa em seu próprio processo.
Se você desabilitar ou não configurar esta política, um usuário poderá recusar o isolamento de site.  (Por exemplo, usando a entrada “Desabilitar isolamento de site” em edge://flags.)  Desabilitar a política ou não configurar a política não desliga o Isolamento de Site.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SitePerProcess
  - Nome da GP: Habilitar isolamento de sites para todos os sites
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: SitePerProcess
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SitePerProcess
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SpellcheckEnabled
  #### Habilitar verificação ortográfica
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Se você habilitar ou não configurar essa política, o usuário poderá usar a verificação ortográfica.

Se você desabilitar essa política, o usuário não poderá usar a verificação ortográfica, e as políticas [SpellcheckLanguage](#spellchecklanguage) e [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) também serão desabilitadas.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SpellcheckEnabled
  - Nome da GP: Habilitar verificação ortográfica
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: SpellcheckEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SpellcheckEnabled
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SpellcheckLanguage
  #### Habilitar idiomas específicos da verificação ortográfica
  
  
  #### Versões com suporte:
  - No Windows desde a versão 77 ou posterior

  #### Descrição
  Habilita diferentes idiomas para verificação ortográfica. Qualquer idioma especificado que não for reconhecido será ignorado.

Se você habilitar essa política, a verificação ortográfica será habilitada para os idiomas especificados, bem como os idiomas que o usuário tiver habilitado.

Se você não configurar ou desabilitar essa política, não haverá nenhuma alteração nas preferências de verificação ortográfica do usuário.

Se a política [SpellcheckEnabled](#spellcheckenabled) estiver desabilitada, essa política não terá efeito.

Se um idioma for incluído nas políticas [SpellcheckLanguage](#spellchecklanguage) e [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist), o idioma da verificação ortográfica será habilitado.

Os idiomas com suporte são: af, bg, ca, cs, cy, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SpellcheckLanguage
  - Nome da GP: Habilitar idiomas específicos da verificação ortográfica
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\2 = "es"

```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SpellcheckLanguageBlocklist
  #### Aplicar a desabilitação de verificação ortográfica dos idiomas
  
  
  #### Versões com suporte:
  - No Windows desde a versão 78 ou posterior

  #### Descrição
  Force - desabilita os idiomas de verificação ortográfica. Os idiomas não reconhecidos nessa lista serão ignorados.

Se você habilitar essa política, a verificação ortográfica será desabilitada para os idiomas especificados. O usuário ainda poderá habilitar nem desabilitar a verificação ortográfica para os idiomas que não estão na lista.

Se você não configurar essa política ou desabilitá-la, não haverá alteração nas preferências de verificação ortográfica do usuário.

Se a política [SpellcheckEnabled](#spellcheckenabled) for desabilitada, ela não terá efeito.

Se um idioma estiver incluído nas políticas [SpellcheckLanguage](#spellchecklanguage) e [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist), o idioma de verificação ortográfica será habilitado.

Os idiomas atualmente com suporte são: af, bg, ca, cs, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SpellcheckLanguageBlocklist
  - Nome da GP: Aplicar a desabilitação de verificação ortográfica dos idiomas
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\2 = "es"

```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### StricterMixedContentTreatmentEnabled
  #### Habilitar tratamento mais rígido para conteúdo misto (preterida)
  >PRETERIDA: essa política foi preterida. No momento, ela tem suporte, mas ficará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - Em Windows e macOS desde 81 ou posterior

  #### Descrição
  Esta política foi preterida porque é um mecanismo de curto prazo para oferecer mais tempo para as empresas atualizarem o conteúdo da Web se e quando for incompatível com um tratamento de conteúdo misto mais estrito. Ela não funcionará na versão 85 do Microsoft Edge.

Esta política controla o tratamento de conteúdo misto (conteúdo HTTP em sites HTTPS) no navegador.

Se você definir esta política como Verdadeira ou não configurar, o conteúdo misto de áudio e vídeo será automaticamente atualizado para HTTPS (ou seja, a URL será regravada como HTTPS, sem um retorno se o recurso não estiver disponível em HTTPS) e um aviso "Não Seguro" será mostrado na barra de URLs para conteúdo misto de imagens.

Se você definir a política como Falsa, as atualizações automáticas serão desabilitadas para áudio e vídeo, e nenhum aviso será mostrado para imagens.

Esta política não afeta outros tipos de outros conteúdos mistos diferentes de áudio, vídeo e imagens.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: StricterMixedContentTreatmentEnabled
  - Nome da GP: Habilitar tratamento mais rígido para conteúdo misto (preterida)
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: StricterMixedContentTreatmentEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: StricterMixedContentTreatmentEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SuppressUnsupportedOSWarning
  #### Suprimir o aviso do sistema operacional sem suporte
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Suprime o aviso exibido quando o Microsoft Edge está em execução em um computador ou sistema operacional que não tem mais suporte.

Se essa política for false ou não for definida, os avisos serão exibidos nesses computadores ou sistemas operacionais que não têm suporte.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SuppressUnsupportedOSWarning
  - Nome da GP: Suprimir o aviso do sistema operacional sem suporte
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: SuppressUnsupportedOSWarning
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SuppressUnsupportedOSWarning
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SyncDisabled
  #### Desabilitar sincronização de dados usando os serviços de sincronização da Microsoft
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Desabilita a sincronização de dados no Microsoft Edge. Essa política também impede a exibição do prompt de consentimento de sincronização.

Se você não definir essa política ou aplicá-la como recomendado, os usuários poderão ativar ou desativar a sincronização. Se você aplicar essa política como obrigatória, os usuários não poderão ativar a sincronização.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SyncDisabled
  - Nome da GP: Desabilitar sincronização de dados usando os serviços de sincronização da Microsoft
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: SyncDisabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SyncDisabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### SyncTypesListDisabled
  #### Configure a lista de tipos excluídos da sincronização
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 83 ou posterior

  #### Descrição
  Se você habilitar esta política, todos os tipos de dados especificados serão excluídos da sincronização. Esta política pode ser usada para limitar o tipo de dados carregados para o serviço de sincronização do Microsoft Edge.

Você pode fornecer um dos seguintes tipos de dados para esta política: "favoritos", "configurações", "senhas", "addressesAndMore", "extensões", “histórico”, “openTabs” e "coleções". Observe que esses nomes de tipo de dados diferenciam maiúsculas de minúsculas.

Os usuários não poderão substituir os tipos de dados desabilitados.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: SyncTypesListDisabled
  - Nome da GP: Configure a lista de tipos excluídos da sincronização
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled\1 = "favorites"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: SyncTypesListDisabled
  - Exemplo de valor:
``` xml
<array>
  <string>favorites</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### TLS13HardeningForLocalAnchorsEnabled
  #### Habilitar um recurso de segurança TLS 1.3 para âncoras de confiança locais. (obsoleto)
  
  >OBSOLETO: Essa política é obsoleta e não funciona após o Microsoft Edge 85.
  #### Versões com suporte:
  - No Windows e macOS desde 81, até 85

  #### Descrição
  Essa política não funciona porque o destina-se a ser um mecanismo de curto prazo para dar mais tempo para que as empresas atualizem proxies afetados.

Essa política controla um recurso de segurança no TLS 1.3 que protege as conexões contra ataques de downgrade. Ele é compatível com versões anteriores do e não afetará as conexões com os servidores ou proxies TLS 1.2 compatíveis. No entanto, as versões mais antigas de alguns proxies de interceptação TLS têm uma falha de implementação, o que os torna incompatíveis.

Se você habilitar essa política ou não a definir, Microsoft Edge habilitará estas proteções de segurança para todas as conexões.

Se desabilitar essa política, Microsoft Edge desabilitará estas proteções de segurança para conexões autenticadas com certificados de autoridade de certificação instalados localmente. Essas proteções estão sempre ativadas para conexões autenticadas com certificados de autoridade de certificação de confiança pública.

Essa política pode ser usada para testar todos os proxies afetados e atualizá-los. Espera-se que os proxies afetados falhem nas conexões com um código de erro de ERR_TLS13_DOWNGRADE_DETECTED.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: TLS13HardeningForLocalAnchorsEnabled
  - Nome da GP: Habilitar um recurso de segurança TLS 1.3 para âncoras de confiança locais. (obsoleto)
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: TLS13HardeningForLocalAnchorsEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: TLS13HardeningForLocalAnchorsEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### TLSCipherSuiteDenyList
  #### Especificar os pacotes de cifra TLS para desabilitar
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 85 ou posterior

  #### Descrição
  Configure a lista de pacotes de codificação que estão desativados para conexões TLS.

Se configurar essa política, a lista de pacotes de cifra configurada não será usada para estabelecer conexões TLS.

Se você não configurar essa política, o navegador escolherá quais pacotes de codificação TLS devem ser usados.

Os valores de pacote de cifra a serem desabilitado são especificados como valores hexadecimais de 16 bits. Os valores são atribuídos pelo registro IANA (Autoridade de Números Atribuídos pela Internet).

O pacote TLS 1.3 Cipher TLS_AES_128_GCM_SHA256 (0x1301) é necessário para o TLS 1.3 e não pode ser desabilitado por esta política.

Esta política não afeta as conexões baseadas em QUIC. QUIC pode ser desabilitado por meio da política de [QuicAllowed](#quicallowed).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: TLSCipherSuiteDenyList
  - Nome da GP: Especificar os pacotes de cifra TLS para desabilitar
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\1 = "0x1303"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\2 = "0xcca8"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\3 = "0xcca9"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: TLSCipherSuiteDenyList
  - Exemplo de valor:
``` xml
<array>
  <string>0x1303</string>
  <string>0xcca8</string>
  <string>0xcca9</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### TabFreezingEnabled
  #### Permitir congelamento de guias em segundo plano
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 79 ou posterior

  #### Descrição
  Controla se o Microsoft Edge pode congelar guias que estão em segundo plano há pelo menos 5 minutos.

O congelamento de guias reduz o uso da CPU, da bateria e da memória. O Microsoft Edge usa heurística para evitar o congelamento de guias que fazem trabalho útil em segundo plano, como exibir notificações, reproduzir sons e transmitir vídeos.

Se você habilitar ou não configurar essa política, as guias que estiverem em segundo plano há pelo menos 5 minutos poderão ser congeladas.

Se você desabilitar essa política, nenhuma guia será congelada.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: TabFreezingEnabled
  - Nome da GP: Permitir congelamento de guias em segundo plano
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: TabFreezingEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: TabFreezingEnabled
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### TaskManagerEndProcessEnabled
  #### Habilitar processos finais no gerenciador de tarefas do navegador
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Se você habilitar ou não configurar essa política, os usuários poderão encerrar processos no gerenciador de tarefas do navegador. Se você desabilitá-la, os usuários não poderão encerrar processos e o botão Finalizar processo será desabilitado no gerenciador de tarefas do navegador.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: TaskManagerEndProcessEnabled
  - Nome da GP: Habilitar processos finais no gerenciador de tarefas do navegador
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: TaskManagerEndProcessEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: TaskManagerEndProcessEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### TotalMemoryLimitMb
  #### Defina o limite em megabytes de memória que uma única instância do Microsoft Edge pode usar.
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 80 ou posterior

  #### Descrição
  Configura a quantidade de memória que uma única instância do Microsoft Edge pode usar antes que as guias comecem a ser descartadas para economizar memória. A memória usada pela guia será liberada e a guia deverá ser recarregada quando o usuário alternar para ela.

Se você habilitar essa política, o navegador começará a descartar as guias para economizar memória quando a limitação for excedida. No entanto, não há garantia de que o navegador sempre funcionará sob o limite. Qualquer valor abaixo de 1024 será arredondado para 1024.

Se você não configurar essa política, o navegador só tentará economizar memória quando detectar que a quantidade de memória física no computador está baixa.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: TotalMemoryLimitMb
  - Nome da GP: Defina o limite em megabytes de memória que uma única instância do Microsoft Edge pode usar.
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: TotalMemoryLimitMb
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000800
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: TotalMemoryLimitMb
  - Exemplo de valor:
``` xml
<integer>2048</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### TrackingPrevention
  #### Bloquear o rastreamento de atividades de navegação da Web dos usuários
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 78 ou posterior

  #### Descrição
  Permite que você decida se deseja impedir que sites rastreiem a atividade de navegação na Web do usuário.

Se você desabilitar essa política ou não a configurar, os usuários poderão definir seu próprio nível de prevenção de rastreamento.

Mapeamento das opções da política:

* TrackingPreventionOff (0) = Desativado (sem prevenção de rastreamento)

* TrackingPreventionBasic (1) = Básico (bloqueia rastreadores, conteúdo e anúncios prejudiciais serão personalizados)

* TrackingPreventionBalanced (2) = Equilibrado (bloqueia rastreadores prejudiciais e rastreadores de sites que o usuário não visitou; o conteúdo e os anúncios serão menos personalizados)

* TrackingPreventionStrict (3) = Rigoroso (bloqueia rastreadores prejudiciais e a maioria dos rastreadores de todos os sites; conteúdo e anúncios terão personalização mínima. Algumas partes dos sites podem não funcionar)

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: TrackingPrevention
  - Nome da GP: Bloquear o rastreamento de atividades de navegação da Web dos usuários
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: TrackingPrevention
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000002
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: TrackingPrevention
  - Exemplo de valor:
``` xml
<integer>2</integer>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### TranslateEnabled
  #### Habilitar Traduzir
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Habilita o serviço de tradução integrado da Microsoft no Microsoft Edge.

Se você habilitar essa política, o Microsoft Edge oferecerá a funcionalidade de tradução ao usuário, mostrando um submenu integrado de tradução (quando apropriado) e uma opção de tradução no menu de contexto exibido quando você clica com o botão direito do mouse.

Desabilite essa política para desabilitar todos os recursos de tradução integrados.

Se você não configurar a política, os usuários poderão optar por usar a funcionalidade de tradução ou não.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Sim
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: TranslateEnabled
  - Nome da GP: Habilitar Traduzir
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): Modelos Administrativos/Microsoft Edge - Configurações Padrão (os usuários podem substituir)/
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): SOFTWARE\Policies\Microsoft\Edge\Recomendações
  - Nome do Valor: TranslateEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: TranslateEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### URLAllowlist
  #### Definir uma lista de URLs permitidas
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permita acesso às URLs listadas, como exceções à lista de URL bloqueadas.

  Formate o padrão de URL de acordo com [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  Você pode usar esta política para abrir exceções a listas de contatos bloqueados restritivas. Por exemplo, você pode incluir "*" na lista de contatos bloqueados para bloquear todas as solicitações e, em seguida, usar essa política para permitir o acesso a uma lista limitada de URLs. Você pode usar esta política para abrir exceções a determinados esquemas, subdomínios de outros domínios, portas ou caminhos específicos.

  O filtro mais específico determina se uma URL está bloqueada ou autorizada. A lista permitida tem precedência sobre a lista de contatos bloqueados.

  Esta política está limitada a 1000 entradas; as entradas subsequentes serão ignoradas.

  Esta política também permite que o navegador invoque automaticamente aplicativos externos registrados como manipuladores de protocolo para protocolos como “tel:” ou “ssh:”.

Se você não configurar esta política, não haverá exceções para a lista de contatos bloqueados na política [URLBlocklist](#urlblocklist).

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: URLAllowlist
  - Nome da GP: Definir uma lista de URLs permitidas
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\URLAllowlist
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\5 = ".exact.hostname.com"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: URLAllowlist
  - Exemplo de valor:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### URLBlocklist
  #### Bloquear o acesso a uma lista de URLs
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Define uma lista de sites, com base em padrões de URL, que são bloqueados (os usuários não podem carregá-los).

Formate o padrão de URL de acordo com [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Você pode definir exceções na política [URLAllowlist](#urlallowlist). Essas políticas limitam-se a 1000 entradas; as entradas subsequentes serão ignoradas.

Observe que não é recomendado bloquear URLs internas "edge://*", pois isso pode causar erros inesperados.

Esta política não impede que a página seja atualizada dinamicamente por meio do JavaScript. Por exemplo, se você bloquear "contoso.com/abc", os usuários ainda poderão visitar "contoso.com" e clicar em um link para visitar "contoso.com/abc", desde que a página não seja atualizada.

Se você não configurar esta política, nenhuma URL será bloqueada.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: URLBlocklist
  - Nome da GP: Bloquear o acesso a uma lista de URLs
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\URLBlocklist
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
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


  #### Informações e configurações do Mac
  - Nome da chave de preferência: URLBlocklist
  - Exemplo de valor:
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
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### UserAgentClientHintsEnabled
  #### Habilitar o recurso dicas de cliente Usuário-Agente (preterida)
  >PRETERIDA: essa política foi preterida. No momento, ela tem suporte, mas ficará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - Em Windows e macOS desde 86 ou posterior

  #### Descrição
  Essa política foi preterida porque destina-se a ser um mecanismo de curto prazo para dar mais tempo para que as empresas atualizem o conteúdo da Web se e quando ela for incompatível com o recurso de dicas de cliente do agente de usuário. Ele não funcionará no Microsoft Edge versão 89.

Quando o recurso de dicas do cliente do agente de usuário é enviado, o envia cabeçalhos de solicitação granulares que fornecem informações sobre o navegador do usuário (por exemplo, a versão do navegador) e o ambiente (por exemplo, a arquitetura do sistema).

Esse é um recurso aditivo, mas os novos cabeçalhos podem quebrar alguns sites que restringem os caracteres que as solicitações podem conter.

Se você habilitar ou não configurar essa política, o recurso dicas do cliente do agente de usuário será habilitado. Se você desabilitar essa política, esse recurso não estará disponível.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: UserAgentClientHintsEnabled
  - Nome da GP: Habilitar o recurso dicas de cliente Usuário-Agente (preterida)
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: UserAgentClientHintsEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: UserAgentClientHintsEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### UserDataDir
  #### Definir o diretório de dados do usuário
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Defina o diretório a ser usado para armazenar dados do usuário.

Se você habilitar essa política, o Microsoft Edge usará o diretório especificado, independentemente de o usuário ter definido o sinalizador de linha de comando "--user-data-dir".

Se você não habilitar essa política, o caminho de perfil padrão será usado, mas o usuário poderá substituí-lo usando o sinalizador "--user-data-dir". Os usuários podem encontrar o diretório do perfil em edge://version/ no caminho do perfil.

Para evitar a perda de dados ou outros erros, não configure essa política para o diretório raiz de um volume ou para um diretório usado para outros fins, pois o Microsoft Edge gerencia o conteúdo.

Confira [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) para obter uma lista de variáveis que podem ser usadas.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: UserDataDir
  - Nome da GP: Definir o diretório de dados do usuário
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: UserDataDir
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"${users}/${user_name}/Edge"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: UserDataDir
  - Exemplo de valor:
``` xml
<string>${users}/${user_name}/Edge</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### UserDataSnapshotRetentionLimit
  #### Limita o número de instantâneos de dados do usuário retidos para uso em caso de reversão de emergência.
  
  
  #### Versões com suporte:
  - No Windows desde a versão 86 ou posterior

  #### Descrição
  Após cada atualização principal de versão, o Microsoft Edge cria um instantâneo de partes dos dados de navegação do usuário para uso no caso de uma emergência posterior que exija uma reversão temporária da versão. Se uma reversão temporária for executada em uma versão que o usuário possui um instantâneo correspondente, os dados no instantâneo serão restaurados. Isso permite que os usuários mantenham configurações como marcadores e dados de preenchimento automático.

Se você não definir essa política, o valor padrão de 3 instantâneos será usado.

Se você definir essa política, os instantâneos antigos serão excluídos, conforme necessário, para respeitar o limite definido. Se você definir essa política como 0, nenhum instantâneo será criado.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Número inteiro

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: UserDataSnapshotRetentionLimit
  - Nome da GP: Limita o número de instantâneos de dados do usuário retidos para uso em caso de reversão de emergência.
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: UserDataSnapshotRetentionLimit
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000003
```


  

  [Voltar ao início](#microsoft-edge---políticas)

  ### UserFeedbackAllowed
  #### Permitir comentários do usuário
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  O Microsoft Edge usa o recurso de Comentários do Edge (habilitado por padrão) para permitir que os usuários enviem comentários, sugestões ou pesquisas de clientes e para relatar qualquer problema com o navegador. Além disso, por padrão, os usuários não podem desabilitar (desativar) o recurso Comentários do Edge.

Se você habilitar essa política ou não a configurar, os usuários poderão chamar Comentários do Edge.

Se você desabilitar essa política, os usuários não poderão chamar Comentários do Edge.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: UserFeedbackAllowed
  - Nome da GP: Permitir comentários do usuário
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: UserFeedbackAllowed
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: UserFeedbackAllowed
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### VideoCaptureAllowed
  #### Permitir ou bloquear captura de vídeo
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Controla se os sites podem capturar vídeo.

Se habilitada ou não configurada (padrão), o usuário será perguntado sobre o acesso de captura de vídeo para todos os sites, exceto aqueles com URLs configuradas na lista da política [VideoCaptureAllowedUrls](#videocaptureallowedurls), que terão o acesso concedido sem aviso.

Se você desabilitar esta política, o usuário não será avisado e a captura de vídeo estará disponível apenas para as URLs configuradas na política [VideoCaptureAllowedUrls](#videocaptureallowedurls).

Esta política afeta todos os tipos de entradas de vídeo, não apenas a câmera interna.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: VideoCaptureAllowed
  - Nome da GP: Permitir ou bloquear captura de vídeo
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: VideoCaptureAllowed
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000000
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: VideoCaptureAllowed
  - Exemplo de valor:
``` xml
<false/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### VideoCaptureAllowedUrls
  #### Sites que podem acessar dispositivos de captura de vídeo sem solicitar permissão
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Especifica sites, com base nos padrões de URL, que podem usar dispositivos de captura de vídeo sem pedir permissão ao usuário. Os padrões nessa lista são comparados com a origem de segurança da URL solicitante. Se forem iguais, o site automaticamente terá acesso aos dispositivos de captura de vídeo.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: VideoCaptureAllowedUrls
  - Nome da GP: Sites que podem acessar dispositivos de captura de vídeo sem solicitar permissão
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: VideoCaptureAllowedUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### WPADQuickCheckEnabled
  #### Definir otimização de WPAD
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite que você desative a otimização WPAD (Descoberta Automática de Proxy da Web) no Microsoft Edge.

Se você desabilitar esta política, a otimização de WPAD será desabilitada, o que faz o navegador aguardar mais tempo pelos servidores WPAD baseados em DNS.

Se você habilitar ou não configurar a política, a otimização WPAD será habilitada.

Independentemente de a política estar habilitada ou de como está habilitada, a configuração da otimização WPAD não pode ser alterada pelos usuários.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: WPADQuickCheckEnabled
  - Nome da GP: Definir otimização de WPAD
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: WPADQuickCheckEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WPADQuickCheckEnabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### WebAppInstallForceList
  #### Configurar lista de Aplicativos Web instalados à força
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 80 ou posterior

  #### Descrição
  Especifica uma lista de sites que estão instalados no modo silencioso, sem interação do usuário, e que não podem ser desinstalados nem desabilitados pelo usuário.

Cada item da lista da política é um objeto com os seguintes membros:
  - "url", que é obrigatório. "url" deve ser a URL do aplicativo web a ser instalado.

Os valores para os membros opcionais são:
  - "launch_container" deve ser "window" ou "tab" para indicar como o aplicativo Web será aberto depois de instalado.
  - "create_desktop_shortcut" deve ser true se um atalho da área de trabalho precisar ser criado no Windows.

Se "default_launch_container" for omitido, o aplicativo será aberto em uma guia por padrão. Independentemente do valor de "default_launch_container", os usuários poderão alterar o contêiner no qual o aplicativo será aberto. Se "create_desktop_shortcuts" for omitido, não serão criados atalhos da área de trabalho.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Sim

  #### Tipo de Dados:
  - Dicionário

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: WebAppInstallForceList
  - Nome da GP: Configurar lista de Aplicativos Web instalados à força
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: WebAppInstallForceList
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
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


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebAppInstallForceList
  - Exemplo de valor:
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
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### WebComponentsV0Enabled
  #### Reabilitar a API do Web Components v0 até M84 (obsoleto)
  
  >OBSOLETO: Essa política é obsoleta e não funciona após o Microsoft Edge 84.
  #### Versões com suporte:
  - No Windows e macOS desde 80, até 84

  #### Descrição
  Esta política não funciona porque esta política permitiu que esses recursos sejam habilitados novamente de modo seletivo até a versão 85 do Microsoft Edge. As APIs V0 dos Componentes Web (Shadow DOM V0, Elementos personalizados V0 e importações do HTML) ficaram obsoletas em 2018 e foram desabilitadas por padrão a partir da versão 80 do Microsoft Edge.

Se você configurar essa política como Verdadeira, os recursos dos Componentes Web v0 serão habilitados em todos os sites.

Se você definir essa política como Falsa ou não definir essa política, os recursos dos Componentes Web v0 serão desabilitados por padrão a partir da versão 80 do Microsoft Edge.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: WebComponentsV0Enabled
  - Nome da GP: Reabilitar a API do Web Components v0 até M84 (obsoleto)
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: WebComponentsV0Enabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebComponentsV0Enabled
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### WebDriverOverridesIncompatiblePolicies
  #### Permitir que o WebDriver substitua políticas incompatíveis (obsoleto)
  
  >OBSOLETO: Essa política é obsoleta e não funciona após o Microsoft Edge 84.
  #### Versões com suporte:
  - No Windows e macOS desde 77, até 84

  #### Descrição
  Esta política não funcionará porque o WebDriver agora é compatível com todas as políticas existentes.

     Esta política permite que os usuários do recurso WebDriver substituam políticas
que possam interferir em sua operação.

     Atualmente, esta política desativa as políticas [SitePerProcess](#siteperprocess) e [IsolateOrigins](#isolateorigins).

     Se a política estiver habilitada, o WebDriver poderá substituir políticas incompatíveis
.
     Se a política estiver desabilitada ou não configurada, o WebDriver não poderá
     substituir políticas incompatíveis.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: WebDriverOverridesIncompatiblePolicies
  - Nome da GP: Permitir que o WebDriver substitua políticas incompatíveis (obsoleto)
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: WebDriverOverridesIncompatiblePolicies
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebDriverOverridesIncompatiblePolicies
  - Exemplo de valor:
``` xml
<true/>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### WebRtcLocalIpsAllowedUrls
  #### Gerenciar a exposição de endereços IP locais pelo WebRTC
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 80 ou posterior

  #### Descrição
  Especifica uma lista de origens (URLs) ou padrões de nome de host (como "*contoso.com*") para os quais o endereço IP local deve ser exposto pelo WebRTC.

Se você habilitar essa política e definir uma lista de origens (URLs) ou padrões de nome de host, quando edge://flags/#enable-webrtc-hide-local-ips-with-mdns estiver habilitado, o WebRTC mostrará o endereço IP local para casos que corresponderem aos padrões na lista.

Se você desabilitar ou não configurar essa política e edge://flags/#enable-webrtc-hide-local-ips-with-mdns estiver habilitado, o WebRTC não mostrará os endereços IP locais. O endereço IP local é oculto por um nome de host mDNS.

Se você habilitar, desabilitar ou não configurar essa política e edge://flags/#enable-webrtc-hide-local-ips-with-mdns estiver desabilitado, o WebRTC mostrará endereços IP locais.

Observe que essa política enfraquece a proteção de endereços IP locais que podem ser necessária para os administradores.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Lista de cadeias de caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: WebRtcLocalIpsAllowedUrls
  - Nome da GP: Gerenciar a exposição de endereços IP locais pelo WebRTC
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls
  - Caminho (Recomendações): N/A
  - Nome do Valor: 1, 2, 3, ...
  - Tipo de Valor: lista de REG_SZ
  ##### Exemplo de valor:
```
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\2 = "*contoso.com*"

```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebRtcLocalIpsAllowedUrls
  - Exemplo de valor:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>*contoso.com*</string>
</array>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### WebRtcLocalhostIpHandling
  #### Restringir a exposição do endereço IP local pelo WebRTC
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Permite definir se o WebRTC expõe ou não o endereço IP local do usuário.

Se você definir essa política como "AllowAllInterfaces" ou "AllowPublicAndPrivateInterfaces", o WebRTC exporá o endereço IP local.

Se você definir essa política como "AllowPublicInterfaceOnly" ou "DisableNonProxiedUdp", o WebRTC não exporá o endereço IP local.

Se você não definir essa política, ou se desabilitá-la, WebRTC exporá o endereço IP local.

Mapeamento das opções da política:

* AllowAllInterfaces (default) = Permitir todas as interfaces. Isso expõe o endereço IP local

* AllowPublicAndPrivateInterfaces (default_public_and_private_interfaces) = Permitir interfaces públicas e privadas na rota padrão http. Isso expõe o endereço IP local

* AllowPublicInterfaceOnly (default_public_interface_only) = Permitir interface pública sobre rota padrão http. Isso não expõe o endereço IP local

* DisableNonProxiedUdp (disable_non_proxied_udp) = Usar TCP, salvo se o servidor proxy der suporte para UDP. Isso não expõe o endereço IP local

Use as informações anteriores ao configurar essa política.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: WebRtcLocalhostIpHandling
  - Nome da GP: Restringir a exposição do endereço IP local pelo WebRTC
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: WebRtcLocalhostIpHandling
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"default"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebRtcLocalhostIpHandling
  - Exemplo de valor:
``` xml
<string>default</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### WebRtcUdpPortRange
  #### Restringir o intervalo de portas UDP locais usadas pelo WebRTC
  
  
  #### Versões com suporte:
  - Em Windows e macOS desde 77 ou posterior

  #### Descrição
  Restringe o intervalo de portas UDP usado pelo WebRTC a um intervalo de portas especificado (pontos de extremidade incluídos).

Ao configurar essa política, você especifica o intervalo de portas UDP locais que o WebRTC pode usar.

Se você não configurar essa política, ou se defini-la como uma cadeia de caracteres vazia ou um intervalo de portas inválido, o WebRTC poderá usar qualquer porta UDP local disponível.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Cadeia de Caracteres

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: WebRtcUdpPortRange
  - Nome da GP: Restringir o intervalo de portas UDP locais usadas pelo WebRTC
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: WebRtcUdpPortRange
  - Tipo de Valor: REG_SZ
  ##### Exemplo de valor:
```
"10000-11999"
```


  #### Informações e configurações do Mac
  - Nome da chave de preferência: WebRtcUdpPortRange
  - Exemplo de valor:
``` xml
<string>10000-11999</string>
```
  

  [Voltar ao início](#microsoft-edge---políticas)

  ### WinHttpProxyResolverEnabled
  #### Use o resolvedor de proxy do Windows (preterida)
  >PRETERIDA: essa política foi preterida. No momento, ela tem suporte, mas ficará obsoleta em uma versão futura.
  
  #### Versões com suporte:
  - No Windows desde a versão 84 ou posterior

  #### Descrição
  Esta política foi preterida porque será substituída por um recurso semelhante em uma versão futura, confira https://crbug.com/1032820.

Use o Windows para resolver os proxies de todas as redes do navegador em vez do resolvedor de proxy incorporado em Microsoft Edge. O resolvedor de proxy do Windows habilita recursos de proxy do Windows, como o DirectAccess/NRPT.

Essa política vem com os problemas descritos em https://crbug.com/644030. Faz com que os arquivos PAC sejam buscados e executados pelo código do Windows, incluindo arquivos PAC definidos pela política [ProxyPacUrl](#proxypacurl). Como as buscas de rede do arquivo PAC acontecem pelo Windows, e não pelo código do Microsoft Edge, políticas de rede como [DnsOverHttpsMode](#dnsoverhttpsmode) não se aplicam às buscas de rede de um arquivo PAC.

Se você habilitar essa política, o resolvedor de proxy do Windows será usado.

Se você desabilitar ou não configurar essa política, o resolvedor de proxy do Microsoft Edge será usado.

  #### Recursos com suporte:
  - Pode ser obrigatório: Sim
  - Pode ser recomendado: Não
  - Atualização de política dinâmica: Não - Requer a reinicialização do navegador

  #### Tipo de Dados:
  - Booliano

  #### Informações e configurações do Windows
  ##### Informações da Política de Grupo (ADMX)
  - Nome exclusivo da GP: WinHttpProxyResolverEnabled
  - Nome da GP: Use o resolvedor de proxy do Windows (preterida)
  - Caminho da GP (Obrigatório): Modelos Administrativos/Microsoft Edge/
  - Caminho da GP (Recomendações): N/A
  - Nome do arquivo da GP ADMX: MSEdge.admx
  ##### Configurações do Registro do Windows
  - Caminho (Obrigatório): SOFTWARE\Policies\Microsoft\Edge
  - Caminho (Recomendações): N/A
  - Nome do Valor: WinHttpProxyResolverEnabled
  - Tipo de Valor: REG_DWORD
  ##### Exemplo de valor:
```
0x00000001
```


  

  [Voltar ao início](#microsoft-edge---políticas)


## Consulte também
- [Configurando o Microsoft Edge](configure-microsoft-edge.md)
- [Página inicial do Microsoft Edge Enterprise](https://aka.ms/EdgeEnterprise)
- [Blog das Linhas de Base de Segurança da Microsoft](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)