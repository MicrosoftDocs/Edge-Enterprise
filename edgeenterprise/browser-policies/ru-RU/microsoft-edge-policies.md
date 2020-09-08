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

# Microsoft Edge: политики
Последняя версия Microsoft Edge включает в себя указанные далее политики. Их можно использовать для настройки работы Microsoft Edge в вашей организации.

Чтобы узнать о дополнительных политиках для определения способа и времени обновления Microsoft Edge, перейдите сюда: [Ссылка на политику обновления Microsoft Edge](microsoft-edge-update-policies.md)

Вы можете загрузить [Набор средств соответствия требованиям Microsoft Security](https://www.microsoft.com/download/details.aspx?id=55319), чтобы получить информацию о рекомендованных настройках базовых шаблонов конфигурации безопасности для Microsoft Edge. Дополнительные сведения см. в [Блог базовых планов безопасности Microsoft Security](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)

> [!ПРИМЕЧАНИЕ]
> Эта статья относится к Microsoft Edge версии 77 или более поздней.

## Доступные политики
В этих таблицах перечислены все связанные с браузером групповые политики, доступные в данном выпуске Microsoft Edge. Используйте ссылки из таблицы для получения дополнительных сведений о конкретных политиках.

|||
|-|-|
|[Cast](#cast)|[Диспетчер паролей и защита](#диспетчер-паролей-и-защита)|
|[Запуск, домашняя страница и страница новой вкладки](#запуск-домашняя-страница-и-страница-новой-вкладки)|[Настройки Application Guard](#настройки-application-guard)|
|[Настройки SmartScreen](#настройки-smartscreen)|[Настройки содержимого](#настройки-содержимого)|
|[Печать](#печать)|[Проверка подлинности HTTP](#проверка-подлинности-http)|
|[Прокси-сервер](#прокси-сервер)|[Расширения](#расширения)|
|[Служба поиска по умолчанию](#служба-поиска-по-умолчанию)|[Собственный обмен сообщениями](#собственный-обмен-сообщениями)|
|[Additional](#additional)|

### [*Cast*](#cast-policies)
|Имя политики|Заголовок|
|-|-|
|[EnableMediaRouter](#enablemediarouter)|Включить Google Cast|
|[ShowCastIconInToolbar](#showcasticonintoolbar)|Показать на панели инструментов значок передачи на другие устройства|
### [*Диспетчер паролей и защита*](#диспетчер-паролей-и-защита-policies)
|Имя политики|Заголовок|
|-|-|
|[PasswordManagerEnabled](#passwordmanagerenabled)|Включить сохранение паролей в диспетчер паролей|
|[PasswordMonitorAllowed](#passwordmonitorallowed)|Разрешить уведомлять пользователей, если их пароли признаны небезопасными|
|[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)|Настройка URL-адреса изменения пароля|
|[PasswordProtectionLoginURLs](#passwordprotectionloginurls)|Настройте список URL-адресов для входа в систему, где служба защиты паролей должна записывать хэши пароля|
|[PasswordProtectionWarningTrigger](#passwordprotectionwarningtrigger)|Настройка триггера предупреждения защиты паролей|
### [*Запуск&comma; домашняя страница и страница новой вкладки*](#запуск-домашняя-страница-и-страница-новой-вкладки-policies)
|Имя политики|Заголовок|
|-|-|
|[HomepageIsNewTabPage](#homepageisnewtabpage)|Назначить страницу новой вкладки домашней страницей|
|[HomepageLocation](#homepagelocation)|Настроить URL-адрес домашней страницы|
|[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)|Настройка фоновых типов, разрешенных для макета страницы новой вкладки|
|[NewTabPageCompanyLogo](#newtabpagecompanylogo)|Настройка логотипа компании на странице новой вкладки (не рекомендуется)|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|Скрыть популярные сайты по умолчанию со страницы новой вкладки|
|[NewTabPageLocation](#newtabpagelocation)|Настроить URL-адрес страницы новой вкладки|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|Настройка быстрых ссылок для страницы новой вкладки|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|Включение предварительной загрузки новой вкладки для ускорения отрисовки|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|Настройка интерфейса страницы новой вкладки Microsoft Edge|
|[RestoreOnStartup](#restoreonstartup)|Действие, выполняемое при запуске|
|[RestoreOnStartupURLs](#restoreonstartupurls)|Сайты, которые открываются при запуске браузера|
|[ShowHomeButton](#showhomebutton)|Показать кнопку домашней страницы на панели инструментов|
### [*Настройки Application Guard*](#настройки-application-guard-policies)
|Имя политики|Заголовок|
|-|-|
|[ApplicationGuardContainerProxy](#applicationguardcontainerproxy)|Прокси-сервер контейнера Application Guard|
### [*Настройки SmartScreen*](#настройки-smartscreen-policies)
|Имя политики|Заголовок|
|-|-|
|[PreventSmartScreenPromptOverride](#preventsmartscreenpromptoverride)|Запретить игнорирование сообщений фильтра SmartScreen в Microsoft Defender о сайтах|
|[PreventSmartScreenPromptOverrideForFiles](#preventsmartscreenpromptoverrideforfiles)|Запретить обход предупреждений о загрузках, отправляемых фильтром SmartScreen в Microsoft Defender|
|[SmartScreenAllowListDomains](#smartscreenallowlistdomains)|Настроить список доменов, для которых фильтр SmartScreen в Microsoft Defender не будет отправлять предупреждения|
|[SmartScreenEnabled](#smartscreenenabled)|Настроить фильтр SmartScreen в Microsoft Defender|
|[SmartScreenForTrustedDownloadsEnabled](#smartscreenfortrusteddownloadsenabled)|Принудительная проверка загрузок из надежных источников с помощью фильтра SmartScreen в Microsoft Defender|
|[SmartScreenPuaEnabled](#smartscreenpuaenabled)|Настроить фильтр SmartScreen в Microsoft Defender на блокировку потенциально нежелательных приложений|
### [*Настройки содержимого*](#настройки-содержимого-policies)
|Имя политики|Заголовок|
|-|-|
|[AutoSelectCertificateForUrls](#autoselectcertificateforurls)|Автоматический выбор сертификатов клиентов для этих узлов|
|[CookiesAllowedForUrls](#cookiesallowedforurls)|Разрешить использование файлов cookie на определенных сайтах|
|[CookiesBlockedForUrls](#cookiesblockedforurls)|Блокировать файлы cookie на определенных сайтах|
|[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)|Ограничить файлы cookie от определенных веб-сайтов для текущего сеанса|
|[DefaultCookiesSetting](#defaultcookiessetting)|Настройка файлов cookie|
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|Настройка географического положения по умолчанию|
|[DefaultImagesSetting](#defaultimagessetting)|Настройка изображений по умолчанию|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|Контролировать использование исключений для небезопасного содержимого|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|Настройка скриптов JavaScript по умолчанию|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|Настройка уведомлений по умолчанию|
|[DefaultPluginsSetting](#defaultpluginssetting)|Настройки Adobe Flash по умолчанию|
|[DefaultPopupsSetting](#defaultpopupssetting)|Настройка всплывающего окна по умолчанию|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|Управление использованием веб-API Bluetooth|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|Управление использованием API WebUSB|
|[ImagesAllowedForUrls](#imagesallowedforurls)|Разрешить изображения на этих сайтах|
|[ImagesBlockedForUrls](#imagesblockedforurls)|Блокировать изображения на определенных сайтах|
|[InsecureContentAllowedForUrls](#insecurecontentallowedforurls)|Разрешить небезопасное содержимое на указанных сайтах|
|[InsecureContentBlockedForUrls](#insecurecontentblockedforurls)|Блокировать небезопасное содержимое на указанных сайтах|
|[JavaScriptAllowedForUrls](#javascriptallowedforurls)|Разрешить скрипты JavaScript на определенных сайтах|
|[JavaScriptBlockedForUrls](#javascriptblockedforurls)|Блокировать скрипты JavaScript на определенных сайтах|
|[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)|Включить стандартную устаревшую настройку поведения файлов cookie SameSite|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist)|Вернуться к устаревшему поведению для файлов cookie SameSite на указанных сайтах|
|[NotificationsAllowedForUrls](#notificationsallowedforurls)|Разрешить уведомления на определенных сайтах|
|[NotificationsBlockedForUrls](#notificationsblockedforurls)|Блокировать уведомления на определенных сайтах|
|[PluginsAllowedForUrls](#pluginsallowedforurls)|Разрешить подключаемый модуль Adobe Flash на определенных сайтах|
|[PluginsBlockedForUrls](#pluginsblockedforurls)|Блокировать подключаемый модуль Adobe Flash на определенных сайтах|
|[PopupsAllowedForUrls](#popupsallowedforurls)|Разрешить всплывающие окна на определенных сайтах|
|[PopupsBlockedForUrls](#popupsblockedforurls)|Блокировать всплывающие окна на определенных сайтах|
|[RegisteredProtocolHandlers](#registeredprotocolhandlers)|Регистрация обработчиков протоколов|
|[SpotlightExperiencesAndRecommendationsEnabled](#spotlightexperiencesandrecommendationsenabled)|Choose whether users can receive customized background images and text, suggestions, notifications,
and tips for Microsoft services|
|[WebUsbAllowDevicesForUrls](#webusballowdevicesforurls)|Разрешить для определенных сайтов доступ к определенным USB-устройствам|
|[WebUsbAskForUrls](#webusbaskforurls)|Разрешить WebUSB на определенных сайтах|
|[WebUsbBlockedForUrls](#webusbblockedforurls)|Блокировать WebUSB на определенных сайтах|
### [*Печать*](#печать-policies)
|Имя политики|Заголовок|
|-|-|
|[DefaultPrinterSelection](#defaultprinterselection)|Правила выбора принтера по умолчанию|
|[PrintHeaderFooter](#printheaderfooter)|Печать колонтитулов|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|Задать системный принтер по умолчанию в качестве принтера по умолчанию|
|[PrintingEnabled](#printingenabled)|Включить печать|
|[UseSystemPrintDialog](#usesystemprintdialog)|Печать с помощью системного диалогового окна печати|
### [*Проверка подлинности HTTP*](#проверка-подлинности-http-policies)
|Имя политики|Заголовок|
|-|-|
|[AllowCrossOriginAuthPrompt](#allowcrossoriginauthprompt)|Разрешить запросы обычной проверки подлинности HTTP независимо от источника|
|[AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)|Список серверов, которым Microsoft Edge может передавать учетные данные пользователя|
|[AuthSchemes](#authschemes)|Поддерживаемые схемы проверки подлинности|
|[AuthServerAllowlist](#authserverallowlist)|Настройка списка разрешенных серверов проверки подлинности|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|Отключить поиск CNAME при согласовании проверки подлинности Kerberos|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|Включить нестандартный порт в SPN Kerberos|
|[NtlmV2Enabled](#ntlmv2enabled)|Управление включением и отключением проверки подлинности NTLMv2|
### [*Прокси-сервер*](#прокси-сервер-policies)
|Имя политики|Заголовок|
|-|-|
|[ProxyBypassList](#proxybypasslist)|Настройка правил обхода прокси-сервера|
|[ProxyMode](#proxymode)|Настройки прокси-сервера|
|[ProxyPacUrl](#proxypacurl)|Настроить URL-адрес PAC-файла прокси-сервера|
|[ProxyServer](#proxyserver)|Настройка адреса или URL-адреса прокси-сервера|
|[ProxySettings](#proxysettings)|Настройки прокси-сервера|
### [*Расширения*](#расширения-policies)
|Имя политики|Заголовок|
|-|-|
|[ExtensionAllowedTypes](#extensionallowedtypes)|Настройка разрешенных типов расширений|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|Разрешить установку определенных расширений|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|Управление расширениями, которые нельзя устанавливать|
|[ExtensionInstallForcelist](#extensioninstallforcelist)|Определение автоматически устанавливаемых расширений|
|[ExtensionInstallSources](#extensioninstallsources)|Настройка источников установки расширений и пользовательских скриптов|
|[ExtensionSettings](#extensionsettings)|Настройки управления расширениями|
### [*Служба поиска по умолчанию*](#служба-поиска-по-умолчанию-policies)
|Имя политики|Заголовок|
|-|-|
|[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)|Включить службу поиска по умолчанию|
|[DefaultSearchProviderEncodings](#defaultsearchproviderencodings)|Кодировки службы поиска по умолчанию|
|[DefaultSearchProviderImageURL](#defaultsearchproviderimageurl)|Определяет функцию поиска по изображению для системы поиска по умолчанию|
|[DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams)|Параметры для URL-адреса изображения при использовании метода POST|
|[DefaultSearchProviderKeyword](#defaultsearchproviderkeyword)|Ключевое слово службы поиска по умолчанию|
|[DefaultSearchProviderName](#defaultsearchprovidername)|Имя службы поиска по умолчанию|
|[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)|Поисковый URL-адрес службы поиска по умолчанию|
|[DefaultSearchProviderSuggestURL](#defaultsearchprovidersuggesturl)|URL-адреса службы поиска по умолчанию для предложений|
|[NewTabPageSearchBox](#newtabpagesearchbox)|Настройка функции поиска на странице новой вкладки|
### [*Собственный обмен сообщениями*](#собственный-обмен-сообщениями-policies)
|Имя политики|Заголовок|
|-|-|
|[NativeMessagingAllowlist](#nativemessagingallowlist)|Управление узлами собственного обмена сообщениями, которые могут использовать пользователи|
|[NativeMessagingBlocklist](#nativemessagingblocklist)|Настроить список блокировки для собственного обмена сообщениями|
|[NativeMessagingUserLevelHosts](#nativemessaginguserlevelhosts)|Разрешить узлы собственного обмена сообщениями на уровне пользователя (установленные без разрешений администратора)|
### [*Additional*](#additional-policies)
|Имя политики|Заголовок|
|-|-|
|[AddressBarMicrosoftSearchInBingProviderEnabled](#addressbarmicrosoftsearchinbingproviderenabled)|Включать варианты поисковых запросов поиска (Майкрософт) в Bing в адресную строку|
|[AdsSettingForIntrusiveAdsSites](#adssettingforintrusiveadssites)|Настройка рекламы для сайтов с навязчивой рекламой|
|[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory)|Включить удаление журнала браузера и журнала загрузок|
|[AllowFileSelectionDialogs](#allowfileselectiondialogs)|Разрешить диалоговые окна выбора файлов|
|[AllowPopupsDuringPageUnload](#allowpopupsduringpageunload)|Позволяет странице отображать всплывающие окна во время ее выгрузки|
|[AllowSurfGame](#allowsurfgame)|Разрешить игру "Серфинг"|
|[AllowSyncXHRInPageDismissal](#allowsyncxhrinpagedismissal)|Разрешить отправку синхронных запросов XHR при закрытии страницы (не рекомендуется)|
|[AllowTokenBindingForUrls](#allowtokenbindingforurls)|Настройте список сайтов, для которых Microsoft Edge попытается создать привязку маркера.|
|[AllowTrackingForUrls](#allowtrackingforurls)|Настроить исключения из блокировки отслеживания для определенных сайтов|
|[AlternateErrorPagesEnabled](#alternateerrorpagesenabled)|Предлагать похожие страницы, если не удается найти веб-страницу|
|[AlwaysOpenPdfExternally](#alwaysopenpdfexternally)|Всегда открывать PDF-файлы извне|
|[AmbientAuthenticationInPrivateModesEnabled](#ambientauthenticationinprivatemodesenabled)|Включить проверку подлинности в среде для профилей InPrivate и гостевых профилей|
|[AppCacheForceEnabled](#appcacheforceenabled)|Разрешает повторное включение функции AppCache, даже если она отключена по умолчанию|
|[ApplicationLocaleValue](#applicationlocalevalue)|Настроить язык приложения|
|[AudioCaptureAllowed](#audiocaptureallowed)|Разрешить или запретить запись звука|
|[AudioCaptureAllowedUrls](#audiocaptureallowedurls)|Сайты, которые могут получать доступ к устройствам записи звука без запроса разрешения|
|[AudioSandboxEnabled](#audiosandboxenabled)|Разрешить запуск аудиопесочницы|
|[AutoImportAtFirstRun](#autoimportatfirstrun)|Автоматически импортировать данные и настройки другого браузера при первом запуске|
|[AutoLaunchProtocolsFromOrigins](#autolaunchprotocolsfromorigins)|Определение списка протоколов, которые могут запускать внешнее приложение из указанных источников без запроса к пользователю|
|[AutoOpenAllowedForURLs](#autoopenallowedforurls)|URL-адреса, по которым можно применять AutoOpenFileTypes|
|[AutoOpenFileTypes](#autoopenfiletypes)|Список типов файлов, которые должны открываться автоматически при скачивании|
|[AutofillAddressEnabled](#autofilladdressenabled)|Включить автозаполнение для адресов|
|[AutofillCreditCardEnabled](#autofillcreditcardenabled)|Включить автозаполнение для кредитных карт|
|[AutoplayAllowed](#autoplayallowed)|Разрешить автозапуск мультимедиа для веб-сайтов|
|[BackgroundModeEnabled](#backgroundmodeenabled)|Разрешить фоновым приложениям продолжать работу после закрытия Microsoft Edge|
|[BackgroundTemplateListUpdatesEnabled](#backgroundtemplatelistupdatesenabled)|Включение фонового обновления списка доступных шаблонов для коллекций и других функций, использующих шаблоны|
|[BingAdsSuppression](#bingadssuppression)|Блокировка всей рекламы в результатах поиска Bing|
|[BlockThirdPartyCookies](#blockthirdpartycookies)|Блокировать сторонние файлы cookie|
|[BrowserAddProfileEnabled](#browseraddprofileenabled)|Разрешить создание профиля во всплывающем меню "Удостоверение" или на странице "Настройки"|
|[BrowserGuestModeEnabled](#browserguestmodeenabled)|Включить режим гостя|
|[BrowserNetworkTimeQueriesEnabled](#browsernetworktimequeriesenabled)|Разрешить запросы к сетевой службе времени браузера|
|[BrowserSignin](#browsersignin)|Настройки входа браузера|
|[BuiltInDnsClientEnabled](#builtindnsclientenabled)|Использовать встроенный DNS-клиент|
|[BuiltinCertificateVerifierEnabled](#builtincertificateverifierenabled)|Определяет, будет ли использоваться встроенное средство проверки сертификата для проверки сертификатов сервера (не рекомендуется)|
|[CertificateTransparencyEnforcementDisabledForCas](#certificatetransparencyenforcementdisabledforcas)|Отключить обязательную проверку прозрачности сертификатов для списка хэш-значений subjectPublicKeyInfo|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](#certificatetransparencyenforcementdisabledforlegacycas)|Отключить обязательную проверку прозрачности сертификатов для списка устаревших центров сертификации|
|[CertificateTransparencyEnforcementDisabledForUrls](#certificatetransparencyenforcementdisabledforurls)|Отключить обязательную проверку прозрачности сертификатов для определенных URL-адресов|
|[ClearBrowsingDataOnExit](#clearbrowsingdataonexit)|Удалять данные о просмотре веб-страниц при закрытии Microsoft Edge|
|[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)|Удалять кэшированные изображения и файлы при закрытии Microsoft Edge|
|[ClickOnceEnabled](#clickonceenabled)|Разрешить пользователям открыть файлы с помощью протокола ClickOnce|
|[CollectionsServicesAndExportsBlockList](#collectionsservicesandexportsblocklist)|Блокировка доступа к указанному списку служб и целям экспорта в коллекциях|
|[CommandLineFlagSecurityWarningsEnabled](#commandlineflagsecuritywarningsenabled)|Включить предупреждения системы безопасности для флагов командной строки|
|[ComponentUpdatesEnabled](#componentupdatesenabled)|Включить обновления компонентов в Microsoft Edge|
|[ConfigureDoNotTrack](#configuredonottrack)|Настроить запросы "Не отслеживать"|
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|Настройка автоматического входа с использованием учетной записи домена Active Directory при отсутствии учетной записи домена Azure AD|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|Настройка преобразования текста в речь в сети|
|[ConfigureShare](#configureshare)|Настроить функцию предоставления общего доступа|
|[CustomHelpLink](#customhelplink)|Указание настраиваемой ссылки для справки|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|Проверки перехвата DNS включены|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|Назначить Microsoft Edge стандартным браузером|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|Разрешить поиск в контекстном меню службы поиска по умолчанию|
|[DefaultSensorsSetting](#defaultsensorssetting)|Default sensors setting|
|[DefaultSerialGuardSetting](#defaultserialguardsetting)|Управлять использованием API Serial|
|[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)|Требуется доступность списка сайтов в режиме предприятия перед переходом на вкладку|
|[DeleteDataOnMigration](#deletedataonmigration)|Удалить старые данные браузера при переносе|
|[DeveloperToolsAvailability](#developertoolsavailability)|Определение места использования средств разработчика|
|[DiagnosticData](#diagnosticdata)|Отправлять обязательные и необязательные диагностические данные об использовании браузера|
|[DirectInvokeEnabled](#directinvokeenabled)|Разрешить пользователям открыть файлы с помощью протокола DirectInvoke|
|[Disable3DAPIs](#disable3dapis)|Отключить поддержку API трехмерной графики|
|[DisableScreenshots](#disablescreenshots)|Отключить создание снимков экрана|
|[DiskCacheDir](#diskcachedir)|Задать каталог кэша на диске|
|[DiskCacheSize](#diskcachesize)|Задать размер кэша диска (в байтах)|
|[DnsOverHttpsMode](#dnsoverhttpsmode)|Управление режимом DNS через HTTPS|
|[DnsOverHttpsTemplates](#dnsoverhttpstemplates)|Укажите шаблон URI для нужного сопоставителя DNS поверх HTTPS|
|[DownloadDirectory](#downloaddirectory)|Настроить каталог загрузки|
|[DownloadRestrictions](#downloadrestrictions)|Разрешить ограничения загрузки|
|[EdgeCollectionsEnabled](#edgecollectionsenabled)|Включить функцию "Коллекции"|
|[EditFavoritesEnabled](#editfavoritesenabled)|Позволяет пользователям редактировать "Избранное"|
|[EnableDeprecatedWebPlatformFeatures](#enabledeprecatedwebplatformfeatures)|Повторно включить устаревшие функции веб-платформы на ограниченное время|
|[EnableDomainActionsDownload](#enabledomainactionsdownload)|Включить загрузку действий домена с серверов корпорации Майкрософт (устарела)|
|[EnableOnlineRevocationChecks](#enableonlinerevocationchecks)|Включить проверки OCSP/CRL в сети|
|[EnableSha1ForLocalAnchors](#enablesha1forlocalanchors)|Разрешить сертификаты, подписанные с помощью алгоритма SHA-1, если они выданы локальными якорями доверия (не рекомендуется)|
|[EnterpriseHardwarePlatformAPIEnabled](#enterprisehardwareplatformapienabled)|Разрешить управляемым расширениям использовать API платформы оборудования предприятия|
|[EnterpriseModeSiteListManagerAllowed](#enterprisemodesitelistmanagerallowed)|Разрешить доступ к средству Enterprise Mode Site List Manager|
|[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](#exemptdomainfiletypepairsfromfiletypedownloadwarnings)|Отключить предупреждения о загрузке на основе расширений типов файлов для указанных типов файлов в доменах|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|Управление связью со службой "Эксперименты и конфигурация"|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox)|Отображать флажок "Всегда открывать" в диалоговом окне внешнего протокола|
|[FamilySafetySettingsEnabled](#familysafetysettingsenabled)|Разрешить пользователям настраивать функцию Family Safety|
|[FavoritesBarEnabled](#favoritesbarenabled)|Включить панель "Избранное"|
|[ForceBingSafeSearch](#forcebingsafesearch)|Принудительно применить функцию "Безопасный поиск Bing"|
|[ForceCertificatePromptsOnMultipleMatches](#forcecertificatepromptsonmultiplematches)|Укажите, должен ли Microsoft Edge автоматически выбирать сертификат при обнаружении нескольких совпадений сертификатов для сайта, настроенного с помощью политики "AutoSelectCertificateForUrls"|
|[ForceEphemeralProfiles](#forceephemeralprofiles)|Разрешить использование временных профилей|
|[ForceGoogleSafeSearch](#forcegooglesafesearch)|Принудительно применить функцию "Безопасный поиск Google"|
|[ForceLegacyDefaultReferrerPolicy](#forcelegacydefaultreferrerpolicy)|Использовать стандартную политику источника ссылки "нет источника ссылки при понижении версии". (не рекомендуется)|
|[ForceNetworkInProcess](#forcenetworkinprocess)|Принудительно выполнять сетевой код в процессе браузера (устарела)|
|[ForceSync](#forcesync)|Force synchronization of browser data and do not show the sync consent prompt|
|[ForceYouTubeRestrict](#forceyoutuberestrict)|Принудительное применение минимального режима ограниченного доступа на YouTube|
|[FullscreenAllowed](#fullscreenallowed)|Разрешить работу в полноэкранном режиме|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|Включить кэш проверки подлинности HTTP глобальной области|
|[GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar)|При вводе одного слова в адресной строке не выполнять поиск, а перенаправлять пользователя на сайт интрасети.|
|[HSTSPolicyBypassList](#hstspolicybypasslist)|Настройка списка имен, которые будут обходить проверку политики HSTS|
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|Использовать аппаратное ускорение, если доступно|
|[HideFirstRunExperience](#hidefirstrunexperience)|Скрыть интерфейс первого запуска и экран-заставку|
|[ImportAutofillFormData](#importautofillformdata)|Разрешить импорт данных автозаполнения формы|
|[ImportBrowserSettings](#importbrowsersettings)|Разрешить импорт настроек браузера|
|[ImportCookies](#importcookies)|Разрешение импорта файлов cookie|
|[ImportExtensions](#importextensions)|Разрешение импорта расширений|
|[ImportFavorites](#importfavorites)|Разрешить импорт избранного|
|[ImportHistory](#importhistory)|Разрешить импорт журнала браузера|
|[ImportHomepage](#importhomepage)|Разрешить импорт настроек домашней страницы|
|[ImportOpenTabs](#importopentabs)|Разрешение импорта открытых вкладок|
|[ImportPaymentInfo](#importpaymentinfo)|Разрешить импорт платежных данных|
|[ImportSavedPasswords](#importsavedpasswords)|Разрешить импорт сохраненных паролей|
|[ImportSearchEngine](#importsearchengine)|Разрешить импортировать настройки поисковой системы|
|[ImportShortcuts](#importshortcuts)|Разрешить импорт ярлыков|
|[InPrivateModeAvailability](#inprivatemodeavailability)|Настроить доступность режима InPrivate|
|[InsecureFormsWarningsEnabled](#insecureformswarningsenabled)|Enable warnings for insecure forms|
|[IntensiveWakeUpThrottlingEnabled](#intensivewakeupthrottlingenabled)|Управление функцией IntensiveWakeUpThrottling|
|[InternetExplorerIntegrationEnhancedHangDetection](#internetexplorerintegrationenhancedhangdetection)|Настройка расширенного определения зависания для режима Internet Explorer|
|[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)|Настройка интеграции с Internet Explorer|
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|Настроить список сайтов для режима предприятия|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|Укажите способ обработки переходов "на странице" для ненастроенных сайтов, выполненных со страниц в режиме Internet Explorer|
|[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed)|Allow Internet Explorer mode testing|
|[IsolateOrigins](#isolateorigins)|Включить изоляцию сайта для определенных источников|
|[LocalProvidersEnabled](#localprovidersenabled)|Разрешить предложения локальных поставщиков|
|[ManagedFavorites](#managedfavorites)|Настроить "Избранное"|
|[ManagedSearchEngines](#managedsearchengines)|Управление поисковыми системами|
|[MaxConnectionsPerProxy](#maxconnectionsperproxy)|Максимальное число одновременных подключений к прокси-серверу|
|[MediaRouterCastAllowAllIPs](#mediaroutercastallowallips)|Разрешить Google Cast подключаться к устройствам передачи с любыми IP-адресами|
|[MetricsReportingEnabled](#metricsreportingenabled)|Включить отправку отчетов об использовании и данных, относящихся к сбою (не рекомендуется)|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|Включить закрытие собственныых окон|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|Установка времени ожидания для задержки перехода на вкладку для списка сайтов в режиме предприятия|
|[NetworkPredictionOptions](#networkpredictionoptions)|Включить прогнозирование сети|
|[NonRemovableProfileEnabled](#nonremovableprofileenabled)|Настройка постоянного автоматического входа пользователя в стандартный профиль на основе рабочей или учебной учетной записи|
|[OverrideSecurityRestrictionsOnInsecureOrigin](#overridesecurityrestrictionsoninsecureorigin)|Управление применением ограничений доступа к небезопасным источникам|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|Разрешить веб-сайтам запрашивать информацию о наличии доступных методов оплаты|
|[PersonalizationReportingEnabled](#personalizationreportingenabled)|Разрешить персонализацию рекламы, результатов поиска и новостей путем отправки журнала браузера в корпорацию Майкрософт|
|[PinningWizardAllowed](#pinningwizardallowed)|Разрешить использование мастера закрепления на панели задач|
|[ProactiveAuthEnabled](#proactiveauthenabled)|Включить упреждающую проверку подлинности|
|[PromotionalTabsEnabled](#promotionaltabsenabled)|Включить отображение полноширинной вкладки с рекламным содержимым|
|[PromptForDownloadLocation](#promptfordownloadlocation)|Спрашивать, куда сохранять загруженные файлы|
|[QuicAllowed](#quicallowed)|Разрешить протокол QUIC|
|[RelaunchNotification](#relaunchnotification)|Уведомлять пользователя о том, что рекомендуется или требуется перезапустить браузер для ожидающих обновлений|
|[RelaunchNotificationPeriod](#relaunchnotificationperiod)|Задать период времени для уведомлений об обновлении|
|[RendererCodeIntegrityEnabled](#renderercodeintegrityenabled)|Включить целостность кода визуализации|
|[RequireOnlineRevocationChecksForLocalAnchors](#requireonlinerevocationchecksforlocalanchors)|Укажите, требуются ли проверки OCSP и списка отзыва сертификатов через Интернет для локальных якорей доверия|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|Включить устранение ошибок навигации с помощью веб-службы|
|[RestrictSigninToPattern](#restrictsignintopattern)|Ограничить учетные записи, которые могут использоваться в качестве основных в Microsoft Edge|
|[RoamingProfileLocation](#roamingprofilelocation)|Задать каталог для перемещаемого профиля|
|[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)|Разрешить использование перемещаемых копий для данных профиля Microsoft Edge|
|[RunAllFlashInAllowMode](#runallflashinallowmode)|Расширить настройку содержимого Adobe Flash на все содержимое|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|Разрешить пользователям продолжать работу со страницы предупреждения HTTPS|
|[SSLVersionMin](#sslversionmin)|Включена минимальная версия протокола TLS|
|[SaveCookiesOnExit](#savecookiesonexit)|Сохранять файлы cookie при закрытии Microsoft Edge|
|[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)|Отключить сохранение журнала браузера|
|[ScreenCaptureAllowed](#screencaptureallowed)|Разрешите или запретите снимок экрана|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|Разрешить прокрутку до текста, указанного в фрагментах URL-адреса|
|[SearchSuggestEnabled](#searchsuggestenabled)|Включить варианты поиска|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|Веб-сайты и домены, которые не требуют разрешения на использование прямой аттестации ключа безопасности|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|Отправка всех сайтов интрасети в Internet Explorer|
|[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)|Отправлять сведения о сайте для улучшения служб Майкрософт (не рекомендуется)|
|[SensorsAllowedForUrls](#sensorsallowedforurls)|Allow access to sensors on specific sites|
|[SensorsBlockedForUrls](#sensorsblockedforurls)|Block access to sensors on specific sites|
|[SerialAskForUrls](#serialaskforurls)|Разрешить API Serial на определенных сайтах|
|[SerialBlockedForUrls](#serialblockedforurls)|Блокировать API Serial на определенных сайтах|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|Показать ярлык Microsoft Office на панели "Избранное"|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|Включить поддержку подписи HTTP exchange (SXG)|
|[SitePerProcess](#siteperprocess)|Включить изоляцию для каждого сайта|
|[SpellcheckEnabled](#spellcheckenabled)|Включить проверку орфографии|
|[SpellcheckLanguage](#spellchecklanguage)|Включить конкретные языки проверки орфографии|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|Принудительное отключение языков проверки орфографии|
|[StricterMixedContentTreatmentEnabled](#strictermixedcontenttreatmentenabled)|Включить более строгую обработку для смешанного содержимого (не рекомендуется)|
|[SuppressUnsupportedOSWarning](#suppressunsupportedoswarning)|Отключить предупреждение о неподдерживаемой ОС|
|[SyncDisabled](#syncdisabled)|Отключить синхронизацию данных с помощью служб синхронизации Майкрософт|
|[SyncTypesListDisabled](#synctypeslistdisabled)|Настройка списка типов, исключенных из синхронизации|
|[TLS13HardeningForLocalAnchorsEnabled](#tls13hardeningforlocalanchorsenabled)|Включить функцию безопасности TLS 1.3 для локальных якорей доверия. (устарела)|
|[TLSCipherSuiteDenyList](#tlsciphersuitedenylist)|Укажите комплекты шифров TLS для отключения|
|[TabFreezingEnabled](#tabfreezingenabled)|Разрешить блокировку работы фоновых вкладок|
|[TaskManagerEndProcessEnabled](#taskmanagerendprocessenabled)|Включить завершение процессов в диспетчере задач браузера|
|[TotalMemoryLimitMb](#totalmemorylimitmb)|Установка ограничения объема памяти (в мегабайтах), который может использовать один экземпляр Microsoft Edge.|
|[TrackingPrevention](#trackingprevention)|Блокировка отслеживания просмотренных веб-страниц|
|[TranslateEnabled](#translateenabled)|Включить перевод|
|[URLAllowlist](#urlallowlist)|Определить список разрешенных URL-адресов|
|[URLBlocklist](#urlblocklist)|Запретить доступ к списку URL-адресов|
|[UserAgentClientHintsEnabled](#useragentclienthintsenabled)|Включение функции подсказок клиента агента-пользователя (не рекомендуется)|
|[UserDataDir](#userdatadir)|Задать каталог данных пользователя|
|[UserDataSnapshotRetentionLimit](#userdatasnapshotretentionlimit)|Ограничивает количество снимков данных пользователя, сохраняемых для использования в случае экстренного отката|
|[UserFeedbackAllowed](#userfeedbackallowed)|Разрешить отзывы пользователей|
|[VideoCaptureAllowed](#videocaptureallowed)|Разрешить или запретить запись видео|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|Сайты, которые могут получать доступ к устройствам записи видео без запроса разрешения|
|[WPADQuickCheckEnabled](#wpadquickcheckenabled)|Настроить оптимизацию WPAD|
|[WebAppInstallForceList](#webappinstallforcelist)|Настройка списка принудительно установленных веб-приложений|
|[WebComponentsV0Enabled](#webcomponentsv0enabled)|Повторно включить API веб-компонентов v0 до версии M84 (устарела)|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|Разрешить WebDriver переопределять несовместимые политики (устарела)|
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|Управление раскрытием локальных IP-адресов с помощью WebRTC|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|Ограничить раскрытие локального IP-адреса с помощью WebRTC|
|[WebRtcUdpPortRange](#webrtcudpportrange)|Ограничить диапазон локальных UDP-портов, используемых WebRTC|
|[WinHttpProxyResolverEnabled](#winhttpproxyresolverenabled)|Использование сопоставителя прокси-серверов Windows (не рекомендуется)|




  ## Cast policies

  [В начало](#microsoft-edge:-политики)

  ### EnableMediaRouter
  #### Включить Google Cast
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Включите этот параметр политики, чтобы активировать Google Cast. Пользователи смогут запустить эту функцию из меню приложения, контекстных меню страницы, с помощью элементов управления мультимедиа на веб-сайтах с поддержкой Cast и с помощью значка компонента Cast (если отображается) на панели инструментов.

Отключите этот параметр политики, чтобы отключить Google Cast.

По умолчанию функция Google Cast активирована.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: EnableMediaRouter
  - Имя групповой политики: Включить Google Cast
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Cast
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: EnableMediaRouter
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: EnableMediaRouter
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ShowCastIconInToolbar
  #### Показать на панели инструментов значок передачи на другие устройства
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Когда этот параметр политики включен, на панели инструментов или в меню переполнения отображается значок панели инструментов "Передача на другие устройства" и пользователи не могут его удалить.

Если этот параметр политики выключен или не настроен, пользователи могут закрепить или удалить значок с помощью контекстного меню.

Если при этом для параметра [EnableMediaRouter](#enablemediarouter) установлено значение false, данный параметр политики игнорируется и значок панели инструментов не отображается.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ShowCastIconInToolbar
  - Имя групповой политики: Показать на панели инструментов значок передачи на другие устройства
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Cast
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ShowCastIconInToolbar
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ShowCastIconInToolbar
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ## Диспетчер паролей и защита policies

  [В начало](#microsoft-edge:-политики)

  ### PasswordManagerEnabled
  #### Включить сохранение паролей в диспетчер паролей
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Сохранение паролей пользователя в Microsoft Edge.

Если этот параметр политики включен, пользователи могут сохранять свои пароли в Microsoft Edge. При последующих посещениях сайта Microsoft Edge автоматически вводит пароль.

Если этот параметр политики отключен, пользователи не могут сохранять новые пароли, но могут использовать ранее сохраненные пароли.

Если включить или отключить этот параметр политики, пользователи не смогут изменить или переопределить его в Microsoft Edge. Если этот параметр не задан, пользователи могут сохранять пароли, а также могут отключить эту функцию.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PasswordManagerEnabled
  - Имя групповой политики: Включить сохранение паролей в диспетчер паролей
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Диспетчер паролей и защита
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Диспетчер паролей и защита
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: PasswordManagerEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: PasswordManagerEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### PasswordMonitorAllowed
  #### Разрешить уведомлять пользователей, если их пароли признаны небезопасными
  
  
  #### Поддерживаемые версии:
  - На Windows с 85 или более поздней версии

  #### Описание
  Разрешить Microsoft Edge отслеживать пароли пользователей.

Если вы включите эту политику и пользователь согласится на ее включение, он будет получать оповещение, если какой-либо из его паролей, хранящихся в Microsoft Edge, будет признан небезопасным. Оповещение появится в Microsoft Edge. Кроме того, эти сведения будут доступны в разделе "Параметры > Пароли > Мониторинг паролей".

Если вы отключите эту политику, у пользователей не будет запрашиваться разрешение на включение этой возможности и им не будет отправляться оповещение. Их пароли не будут сканироваться.

Если вы включите или не настроите политику, пользователи смогут включить или отключить эту возможность.

Дополнительные сведения о том, как Microsoft Edge находит небезопасные пароли см. на странице [https://go.microsoft.com/fwlink/?linkid=2133833](https://go.microsoft.com/fwlink/?linkid=2133833)

Дополнительные инструкции:

Эту политику можно настроить как рекомендуемой, так и обязательной, но с важным оповещением.

Включен параметр "Обязательно": с учетом того, что согласие отдельного пользователя является предварительным условием включения этой возможности для конкретного пользователя, у этой политики нет параметра обязательного включения. Если политика настроена на обязательное включение, пользовательский интерфейс в параметрах не изменится и отобразится следующее сообщение об ошибке на странице edge://policy

Пример сообщения о состоянии ошибки: "Это значение политики пропускается, так как мониторинг паролей требует согласия отдельного пользователя для ее включения. Вы можете попросить пользователей в вашей организации открыть "Параметры" > "Профиль" > "Пароль" и включить функцию".

Включен параметр "Рекомендуется": если политика настроена на рекомендуемое включение, пользовательский интерфейс в параметрах останется в состоянии "Откл", но рядом с ним будет отображаться значок портфеля со следующим описанием, выводимым при наведении курсора: "Ваша организация рекомендует определенное значение для этого параметра, но вы выбрали другое значение"

Параметры "Обязательно" и "Рекомендуется" отключены: оба состояния будут работать стандартным образом с отображением обычных подписей для пользователей.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PasswordMonitorAllowed
  - Имя групповой политики: Разрешить уведомлять пользователей, если их пароли признаны небезопасными
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Диспетчер паролей и защита
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Диспетчер паролей и защита
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: PasswordMonitorAllowed
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  

  [В начало](#microsoft-edge:-политики)

  ### PasswordProtectionChangePasswordURL
  #### Настройка URL-адреса изменения пароля
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Настройка URL-адреса для смены пароля (только схемы HTTP и HTTPS).

Служба защиты паролей будет отправлять пользователей на этот URL-адрес для смены пароля после появления предупреждения в браузере.

Если эта политика включена, служба защиты паролей отправляет пользователей на данный URL-адрес для смены пароля.

Если эта политика отключена или не настроена, служба защиты паролей не перенаправляет пользователей на URL-адрес для смены пароля.

Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PasswordProtectionChangePasswordURL
  - Имя групповой политики: Настройка URL-адреса изменения пароля
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Диспетчер паролей и защита
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: PasswordProtectionChangePasswordURL
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"https://contoso.com/change_password.html"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: PasswordProtectionChangePasswordURL
  - Пример значения:
``` xml
<string>https://contoso.com/change_password.html</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### PasswordProtectionLoginURLs
  #### Настройте список URL-адресов для входа в систему, где служба защиты паролей должна записывать хэши пароля
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Настройка списка корпоративных URL-адресов для входа (только схемы HTTP и HTTPS), где Microsoft Edge должен захватывать "соленые" хэши паролей и использовать их для обнаружения повторного использования пароля.

Если вы включите эту политику, эта служба защиты паролей фиксирует "отпечатки пальцев" паролей на определенных URL-адресах.

Если вы отключите эту политику или не настроите ее, "отпечатки пальцев" паролей не будут фиксироваться.

Эта политика доступна только для экземпляров Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PasswordProtectionLoginURLs
  - Имя групповой политики: Настройте список URL-адресов для входа в систему, где служба защиты паролей должна записывать хэши пароля
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Диспетчер паролей и защита
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\1 = "https://contoso.com/login.html"
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\2 = "https://login.contoso.com"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: PasswordProtectionLoginURLs
  - Пример значения:
``` xml
<array>
  <string>https://contoso.com/login.html</string>
  <string>https://login.contoso.com</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### PasswordProtectionWarningTrigger
  #### Настройка триггера предупреждения защиты паролей
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Разрешает управлять вызовом предупреждения о защите пароля. Защита пароля предупреждает пользователей, когда они повторно используют свой защищенный пароль на потенциально подозрительных сайтах.

Можно использовать политики [PasswordProtectionLoginURLs](#passwordprotectionloginurls) и [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl) для настройки паролей, которые необходимо защищать.

Исключения: пароли для сайтов, перечисленных в политиках [PasswordProtectionLoginURLs](#passwordprotectionloginurls) и [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl), а также для сайтов, указанных в [SmartScreenAllowListDomains](#smartscreenallowlistdomains), не будут отображать предупреждения защиты паролей.

Задайте значение 'PasswordProtectionWarningOff', чтобы не отображать предупреждения защиты паролей.

Задайте значение 'PasswordProtectionWarningOnPasswordReuse', чтобы отображать предупреждения защиты паролей, когда пользователь повторно использует свой защищенный пароль на сайтах, не внесенных в список разрешенных.

Если отключить или не настроить эту политику, триггер предупреждения защиты паролей не отображается.

Сопоставление параметров политики:

* PasswordProtectionWarningOff (0) = Предупреждение о защите паролем отключено

* PasswordProtectionWarningOnPasswordReuse (1) = Предупреждение о защите паролем вызывается повторным использованием пароля

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PasswordProtectionWarningTrigger
  - Имя групповой политики: Настройка триггера предупреждения защиты паролей
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Диспетчер паролей и защита
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: PasswordProtectionWarningTrigger
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: PasswordProtectionWarningTrigger
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ## Запуск&comma; домашняя страница и страница новой вкладки policies

  [В начало](#microsoft-edge:-политики)

  ### HomepageIsNewTabPage
  #### Назначить страницу новой вкладки домашней страницей
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Настройка стандартной домашней страницы в Microsoft Edge. В качестве домашней страницы можно задать определенный URL-адрес или новую вкладку.

Если эта политика включена, в новой вкладке всегда открывается домашняя страница, а URL-адрес домашней страницы игнорируется.

Если эта политика выключена, домашняя страница пользователя не может открываться в новой вкладке, если только в качестве URL-адреса не указано edge://newtab.

Если эта политика не настроена, пользователи могут выбирать, будет ли новая вкладка открываться на их домашней странице.

Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: HomepageIsNewTabPage
  - Имя групповой политики: Назначить страницу новой вкладки домашней страницей
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Запуск, домашняя страница и страница новой вкладки
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Запуск, домашняя страница и страница новой вкладки
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: HomepageIsNewTabPage
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: HomepageIsNewTabPage
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### HomepageLocation
  #### Настроить URL-адрес домашней страницы
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определение URL-адреса стандартной домашней страницы в Microsoft Edge.

Домашняя страница — это страница, которая открывается при нажатии кнопки "Домашняя страница". Страницы, открываемые при запуске, определяются политиками [RestoreOnStartup](#restoreonstartup).

Можно задать URL-адрес здесь или настроить открытие домашней страницы при открытии новой вкладки. Если настроено открытие новой вкладки, этот параметр политики не будет действовать.

Если включить эту политику, пользователи не смогут изменить URL-адрес своей домашней страницы, но смогут использовать страницу новой вкладки в качестве домашней.

Если отключить или не настроить эту политику, пользователи смогут выбирать домашнюю страницу по своему усмотрению, пока не будет включена политика [HomepageIsNewTabPage](#homepageisnewtabpage).

Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: HomepageLocation
  - Имя групповой политики: Настроить URL-адрес домашней страницы
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Запуск, домашняя страница и страница новой вкладки
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Запуск, домашняя страница и страница новой вкладки
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: HomepageLocation
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"https://www.contoso.com"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: HomepageLocation
  - Пример значения:
``` xml
<string>https://www.contoso.com</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### NewTabPageAllowedBackgroundTypes
  #### Настройка фоновых типов, разрешенных для макета страницы новой вкладки
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 86 или более поздней версии

  #### Описание
  Вы можете выбрать разрешенные типы фонового изображения на макете новой вкладки в Microsoft Edge.

Если не настроить этот параметр политики, на новой вкладке будут включены все типы фоновых изображений.

Сопоставление параметров политики:

* DisableImageOfTheDay (1) = Отключить ежедневное фоновое изображение

* DisableCustomImage (2) = Отключить настраиваемое фоновое изображение

* DisableAll (3) = Отключить все типы фоновых изображений

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: NewTabPageAllowedBackgroundTypes
  - Имя групповой политики: Настройка фоновых типов, разрешенных для макета страницы новой вкладки
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Запуск, домашняя страница и страница новой вкладки
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: NewTabPageAllowedBackgroundTypes
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000002
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: NewTabPageAllowedBackgroundTypes
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### NewTabPageCompanyLogo
  #### Настройка логотипа компании на странице новой вкладки (не рекомендуется)
  >УСТАРЕЛО. Эта политика устарела. В настоящее время она поддерживается, но станет устаревшей в будущем выпуске.
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 79 или более поздней версии

  #### Описание
  Применение этой политики не рекомендуется, поскольку она работает неправильно. Она не будет работать в Microsoft Edge версии 86.

Определяет логотип компании, который будет использоваться на странице новой вкладки в Microsoft Edge.

Этот параметр политики должен быть настроен в виде строки, которая выражает логотип в формате JSON. Пример: { "default_logo": { "url": "https://www.contoso.com/logo.png", "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29" }, "light_logo": { "url": "https://www.contoso.com/light_logo.png", "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737" } }

Этот параметр политики настраивается путем указания URL-адреса, с которого Microsoft Edge может загрузить требуемый логотип, и хэша шифрования (SHA-256), который используется для проверки целостности загрузки. Логотип должен быть сохранен в формате PNG или SVG, а размер файла логотипа не должен превышать 16 МБ. Логотип загружается и хэшируется, и будет повторно загружаться при каждом изменении URL-адреса или хэша. URL-адрес должен быть доступен без какой-либо проверки подлинности.

Элемент "default_logo" является обязательным. Он будет использоваться в случае отсутствия фонового изображения. Если предоставлен элемент "light_logo", он будет использоваться в случаях, когда у страницы новой вкладки пользователя есть фоновое изображение. Рекомендуется использовать горизонтальный логотип с прозрачным фоном, выровненный по левому краю и отцентрированный по вертикали. Высота логотипа должна составлять не меньше 32 пикселей, а соотношение сторон от 1:1 до 4:1. Элемент "default_logo" должен быть достаточно контрастным на черном/белом фоне, а элемент "light_logo" должен выглядеть достаточно контрастным на фоновом изображении.

Если этот параметр политики включен, Microsoft Edge загружает и отображает указанный логотип на странице новой вкладки. Пользователи не могут скрыть или переопределить его.

Если отключить или не настроить этот параметр политики, Microsoft Edge не будет отображать логотип на странице новой вкладки или будет отображать логотип Microsoft.

Справку по определению хэша SHA-256 см. на странице https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/get-filehash.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Словарь

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: NewTabPageCompanyLogo
  - Имя групповой политики: Настройка логотипа компании на странице новой вкладки (не рекомендуется)
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Запуск, домашняя страница и страница новой вкладки
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: NewTabPageCompanyLogo
  - Тип значения: REG_SZ
  ##### Пример значения:
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


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: NewTabPageCompanyLogo
  - Пример значения:
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
  

  [В начало](#microsoft-edge:-политики)

  ### NewTabPageHideDefaultTopSites
  #### Скрыть популярные сайты по умолчанию со страницы новой вкладки
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Удаление стандартных популярных сайтов со страницы новой вкладки в Microsoft Edge.

Если для этого параметра задано значение true, стандартные плитки популярных сайтов скрыты.

Если для этого параметра задано значение false или он не настроен, стандартные плитки популярных сайтов отображаются.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: NewTabPageHideDefaultTopSites
  - Имя групповой политики: Скрыть популярные сайты по умолчанию со страницы новой вкладки
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Запуск, домашняя страница и страница новой вкладки
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: NewTabPageHideDefaultTopSites
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: NewTabPageHideDefaultTopSites
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### NewTabPageLocation
  #### Настроить URL-адрес страницы новой вкладки
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Настройка URL-адреса по умолчанию для новой вкладки.

Эта политика определяет страницу, открываемую при создании новой вкладки (в том числе при открытии новых окон). Она также влияет на стартовую страницу, если она настроена открываться в новой вкладке.

Эта политика не определяет, какие страницы открывать при запуске; за это отвечает политика [RestoreOnStartup](#restoreonstartup). Она также не влияет на домашнюю страницу, если она настроена открываться в новой вкладке.

Если не настроить эту политику, будет использоваться новая вкладка по умолчанию.

Если настроить эту политику *и* политику [NewTabPageSetFeedType](#newtabpagesetfeedtype), эта политика будет иметь приоритет.

Если указан недействительный URL-адрес, в новых вкладках будет открываться страница about://blank.

Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: NewTabPageLocation
  - Имя групповой политики: Настроить URL-адрес страницы новой вкладки
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Запуск, домашняя страница и страница новой вкладки
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Запуск, домашняя страница и страница новой вкладки
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: NewTabPageLocation
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"https://www.fabrikam.com"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: NewTabPageLocation
  - Пример значения:
``` xml
<string>https://www.fabrikam.com</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### NewTabPageManagedQuickLinks
  #### Настройка быстрых ссылок для страницы новой вкладки
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 79 или более поздней версии

  #### Описание
  По умолчанию в качестве быстрых ссылок на странице новой вкладки Microsoft Edge отображаются добавленные пользователем ярлыки и популярные сайты из журнала браузера. С помощью этого параметра политики можно настроить до трех плиток быстрых ссылок на странице новой вкладки в виде объектов JSON:

[ { "url": "https://www.contoso.com", "title": "Contoso Portal", "pinned": true/false }, ... ]

Поле "url" — обязательное, "title" и "pinned" — необязательные. Если в поле "title" не задано значение, по умолчанию используется URL-адрес. Если в поле "pinned" не задано значение, по умолчанию используется значение false.

Microsoft Edge отображает плитки в указанном порядке (слева направо), при этом все закрепленные плитки предшествуют незакрепленным.

Если этот параметр политики является обязательным, поле "pinned" будет пропущено и все плитки будут закреплены. Пользователь не сможет удалить плитки. Они всегда будут отображаться в передней части списка быстрых ссылок.

Если политика задана как рекомендуемая, закрепленные плитки останутся в списке, но пользователь сможет изменять и удалять их. Незакрепленные плитки быстрых ссылок, как и стандартные популярные сайты, сдвигаются вниз по списку, если другие веб-сайты используются чаще. Когда незакрепленные ссылки применяются с помощью этого параметра политики к существующему профилю браузера, они могут не появиться, если имеют более низкий приоритет, чем другие ссылки из журнала браузера данного пользователя.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Словарь

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: NewTabPageManagedQuickLinks
  - Имя групповой политики: Настройка быстрых ссылок для страницы новой вкладки
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Запуск, домашняя страница и страница новой вкладки
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Запуск, домашняя страница и страница новой вкладки
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: NewTabPageManagedQuickLinks
  - Тип значения: REG_SZ
  ##### Пример значения:
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


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: NewTabPageManagedQuickLinks
  - Пример значения:
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
  

  [В начало](#microsoft-edge:-политики)

  ### NewTabPagePrerenderEnabled
  #### Включение предварительной загрузки новой вкладки для ускорения отрисовки
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 85 или более поздней версии

  #### Описание
  Если эта политика настроена, то включена предварительная загрузка страницы новой вкладки, и пользователи не могут изменить этот параметр. Если эта политика не настроена, то предварительная загрузка включена, но пользователи могут изменить этот параметр.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: NewTabPagePrerenderEnabled
  - Имя групповой политики: Включение предварительной загрузки новой вкладки для ускорения отрисовки
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Запуск, домашняя страница и страница новой вкладки
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Запуск, домашняя страница и страница новой вкладки
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: NewTabPagePrerenderEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: NewTabPagePrerenderEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### NewTabPageSetFeedType
  #### Настройка интерфейса страницы новой вкладки Microsoft Edge
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 79 или более поздней версии

  #### Описание
  Позволяет выбрать интерфейс веб-канала Microsoft News или Office 365 на странице новой вкладки.

Если для этой политики выбрано значение 'News', для пользователей будет отображаться интерфейс веб-канала Microsoft News на странице новой вкладки.

Если для этой политики выбрано значение 'Office', пользователи со входом в Azure Active Directory с помощью браузера будут видеть интерфейс веб-канала Office 365 на странице новой вкладки.

Если отключить или не настроить эту политику:

— Пользователям со входом в Azure Active Directory с помощью браузера будет предлагаться интерфейс веб-канала Office 365 на странице новой вкладки, а также стандартный интерфейс веб-канала на странице новой вкладки.

— Пользователям без входа в Azure Active Directory с помощью браузера будет отображаться стандартный интерфейс веб-канала на странице новой вкладки.

Если настроить эту политику и политику [NewTabPageLocation](#newtabpagelocation), преимущество будет иметь [NewTabPageLocation](#newtabpagelocation).

По умолчанию: отключено или не настроено.

Сопоставление параметров политики:

* News (0) = Интерфейс веб-канала Microsoft News

* Office (1) = Интерфейс веб-канала Office 365

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: NewTabPageSetFeedType
  - Имя групповой политики: Настройка интерфейса страницы новой вкладки Microsoft Edge
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Запуск, домашняя страница и страница новой вкладки
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Запуск, домашняя страница и страница новой вкладки
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: NewTabPageSetFeedType
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: NewTabPageSetFeedType
  - Пример значения:
``` xml
<integer>0</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### RestoreOnStartup
  #### Действие, выполняемое при запуске
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Указание действий Microsoft Edge при запуске.

Если необходимо, чтобы при запуске всегда открывалась новая вкладка, выберите пункт 'RestoreOnStartupIsNewTabPage'.

Если необходимо открывать URL-адреса, которые были открыты перед последним закрытием Microsoft Edge, выберите пункт 'RestoreOnStartupIsLastSession'. Сеанс просмотра будет восстановлен в том состоянии, в котором он был на момент закрытия. Обратите внимание: этот параметр отключает некоторые настройки, которые зависят от сеансов или задают действия при выходе (например, удаление данных о просмотре веб-страниц при выходе или использование файлов cookie только во время сеанса).

Если необходимо открывать определенный набор URL-адресов, выберите пункт 'RestoreOnStartupIsURLs'.

Если этот параметр отключить, результат будет тот же, что и при ненастроенном параметре. Пользователи могут изменить его в Microsoft Edge.

Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

Сопоставление параметров политики:

* RestoreOnStartupIsNewTabPage (5) = Открыть новую вкладку

* RestoreOnStartupIsLastSession (1) = Восстановить последний сеанс

* RestoreOnStartupIsURLs (4) = Открыть список URL-адресов

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: RestoreOnStartup
  - Имя групповой политики: Действие, выполняемое при запуске
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Запуск, домашняя страница и страница новой вкладки
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Запуск, домашняя страница и страница новой вкладки
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: RestoreOnStartup
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000004
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: RestoreOnStartup
  - Пример значения:
``` xml
<integer>4</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### RestoreOnStartupURLs
  #### Сайты, которые открываются при запуске браузера
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Укажите список веб-сайтов, которые будут открываться автоматически при запуске браузера. Если не настроить эту политику, при запуске не будет открываться ни один сайт.

Этот политика работает, только если для политики [RestoreOnStartup](#restoreonstartup) также указано "Открывать URL-адреса из списка" (4).

Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: RestoreOnStartupURLs
  - Имя групповой политики: Сайты, которые открываются при запуске браузера
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Запуск, домашняя страница и страница новой вкладки
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Запуск, домашняя страница и страница новой вкладки
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано\RestoreOnStartupURLs
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\1 = "https://contoso.com"
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\2 = "https://www.fabrikam.com"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: RestoreOnStartupURLs
  - Пример значения:
``` xml
<array>
  <string>https://contoso.com</string>
  <string>https://www.fabrikam.com</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ShowHomeButton
  #### Показать кнопку домашней страницы на панели инструментов
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Отображение кнопки домашней страницы на панели инструментов Microsoft Edge.

Если этот параметр включен, кнопка домашней страницы всегда отображается. Если этот параметр выключен, кнопка никогда не отображается.

Если данный параметр не настроен, пользователи могут самостоятельно отобразить или скрыть эту кнопку.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ShowHomeButton
  - Имя групповой политики: Показать кнопку домашней страницы на панели инструментов
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Запуск, домашняя страница и страница новой вкладки
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Запуск, домашняя страница и страница новой вкладки
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: ShowHomeButton
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ShowHomeButton
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ## Настройки Application Guard policies

  [В начало](#microsoft-edge:-политики)

  ### ApplicationGuardContainerProxy
  #### Прокси-сервер контейнера Application Guard
  
  
  #### Поддерживаемые версии:
  - На Windows с 84 или более поздней версии

  #### Описание
  Настройка прокси-сервера для Microsoft Edge Application Guard.
Если эта политика включена, Microsoft Edge Application Guard не будет учитывать другие источники конфигураций прокси-серверов.

Если вы не настроите эту политику, Microsoft Edge Application Guard будет использовать настройку прокси-сервера узла.

Эта политика не влияет на настройку прокси-сервера для Microsoft Edge за пределами Application Guard (на узле).

Поле ProxyMode позволяет выбрать прокси-сервер, используемый в Microsoft Edge Application Guard.

Поле ProxyPacUrl является URL-адресом PAC-файла прокси.

Поле ProxyServer является URL-адресом прокси-сервера.

Если выбрать значение 'direct' для 'ProxyMode', все остальные поля будут игнорироваться.

Если выбрать значение 'auto_detect' для 'ProxyMode', все остальные поля будут игнорироваться.

Если выбрать значение 'fixed_servers' для 'ProxyMode', используется поле 'ProxyServer'.

Если выбрать значение 'pac_script' для 'ProxyMode', используется поле 'ProxyPacUrl'.

Дополнительные сведения об идентификации трафика Application Guard через двойной прокси-сервер см. на странице [https://go.microsoft.com/fwlink/?linkid=2134653](https://go.microsoft.com/fwlink/?linkid=2134653).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Словарь

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ApplicationGuardContainerProxy
  - Имя групповой политики: Прокси-сервер контейнера Application Guard
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки Application Guard
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ApplicationGuardContainerProxy
  - Тип значения: REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  

  [В начало](#microsoft-edge:-политики)

  ## Настройки SmartScreen policies

  [В начало](#microsoft-edge:-политики)

  ### PreventSmartScreenPromptOverride
  #### Запретить игнорирование сообщений фильтра SmartScreen в Microsoft Defender о сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Эта политика позволяет определить, могут ли пользователи переопределять предупреждения фильтра SmartScreen в Microsoft Defender о потенциально вредоносных веб-сайтах.

Если эта политика включена, пользователи в вашей организации не смогут игнорировать предупреждения фильтра SmartScreen в Microsoft Defender и не смогут продолжать работу с сайтом.

Если отключить или не настроить эту политику, пользователи смогут игнорировать предупреждения фильтра SmartScreen в Microsoft Defender и продолжать работу с сайтом.

Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PreventSmartScreenPromptOverride
  - Имя групповой политики: Запретить игнорирование сообщений фильтра SmartScreen в Microsoft Defender о сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки SmartScreen
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: PreventSmartScreenPromptOverride
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: PreventSmartScreenPromptOverride
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### PreventSmartScreenPromptOverrideForFiles
  #### Запретить обход предупреждений о загрузках, отправляемых фильтром SmartScreen в Microsoft Defender
  
  
  #### Поддерживаемые версии:
  - На Windows с 77 или более поздней версии
  - На macOS с 79 или более поздней версии

  #### Описание
  Эта политика позволяет определить, могут ли пользователи переопределять предупреждения фильтра SmartScreen в Microsoft Defender о непроверенных скачиваниях.

Если эта политика включена, пользователи в вашей организации не смогут игнорировать предупреждения фильтра SmartScreen в Microsoft Defender и скачивать непроверенные файлы.

Если отключить или не настроить эту политику, пользователи смогут игнорировать предупреждения фильтра SmartScreen в Microsoft Defender и скачивать непроверенные файлы.

Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PreventSmartScreenPromptOverrideForFiles
  - Имя групповой политики: Запретить обход предупреждений о загрузках, отправляемых фильтром SmartScreen в Microsoft Defender
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки SmartScreen
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: PreventSmartScreenPromptOverrideForFiles
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: PreventSmartScreenPromptOverrideForFiles
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SmartScreenAllowListDomains
  #### Настроить список доменов, для которых фильтр SmartScreen в Microsoft Defender не будет отправлять предупреждения
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Настройка списка доменов, которым доверяет фильтр SmartScreen в Microsoft Defender. Это означает следующее.
Фильтр SmartScreen в Microsoft Defender не будет проверять потенциально вредоносные ресурсы (например, программы для фишинга и другое вредоносное ПО), если URL-адреса источников совпадают с этими доменами.
Служба защиты загрузок фильтра SmartScreen в Microsoft Defender не будет проверять загружаемые файлы, размещенные в этих доменах.

Если включить эту политику, фильтр SmartScreen в Microsoft Defender будет доверять этим доменам.
Если отключить или не настроить эту политику, ко всем ресурсам будет применяться стандартная защита фильтра SmartScreen в Microsoft Defender.

Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.
Также обратите внимание: эта политика не применяется, если ваша организация включила функцию Advanced Threat Protection в Microsoft Defender. В этом случае следует настроить списки разрешенных и блокируемых URL-адресов в Центре безопасности в Microsoft Defender.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SmartScreenAllowListDomains
  - Имя групповой политики: Настроить список доменов, для которых фильтр SmartScreen в Microsoft Defender не будет отправлять предупреждения
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки SmartScreen
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\2 = "myuniversity.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SmartScreenAllowListDomains
  - Пример значения:
``` xml
<array>
  <string>mydomain.com</string>
  <string>myuniversity.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SmartScreenEnabled
  #### Настроить фильтр SmartScreen в Microsoft Defender
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  С помощью этой политики можно настроить порядок включения фильтра SmartScreen в Microsoft Defender. Этот фильтр выводит предупреждающие сообщения, которые помогают защищать пользователей от возможного фишинга и вредоносных программ. Фильтр SmartScreen в Microsoft Defender по умолчанию включен.

Если эта политика включена, фильтр SmartScreen в Microsoft Defender включен.

Если эта политика отключена, фильтр SmartScreen в Microsoft Defender выключен.

Если эта политика не настроена, пользователи могут выбирать, нужно ли использовать фильтр SmartScreen в Microsoft Defender.

Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SmartScreenEnabled
  - Имя групповой политики: Настроить фильтр SmartScreen в Microsoft Defender
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки SmartScreen
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Настройки SmartScreen
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: SmartScreenEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SmartScreenEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SmartScreenForTrustedDownloadsEnabled
  #### Принудительная проверка загрузок из надежных источников с помощью фильтра SmartScreen в Microsoft Defender
  
  
  #### Поддерживаемые версии:
  - На Windows с 78 или более поздней версии

  #### Описание
  Эта политика позволяет указать, будет ли фильтр SmartScreen в Microsoft Defender проверять репутацию загрузки из надежного источника.

Если эта политика включена или не настроена, фильтр SmartScreen в Microsoft Defender проверяет репутацию загрузки независимо от источника.

Если эта политика выключена, фильтр SmartScreen в Microsoft Defender не проверяет репутацию загрузки, если она выполняется из надежного источника.

Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, либо в экземплярах Windows 10 Pro или Windows 10 Корпоративная, зарегистрированных для управления устройствами.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SmartScreenForTrustedDownloadsEnabled
  - Имя групповой политики: Принудительная проверка загрузок из надежных источников с помощью фильтра SmartScreen в Microsoft Defender
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки SmartScreen
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Настройки SmartScreen
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: SmartScreenForTrustedDownloadsEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  

  [В начало](#microsoft-edge:-политики)

  ### SmartScreenPuaEnabled
  #### Настроить фильтр SmartScreen в Microsoft Defender на блокировку потенциально нежелательных приложений
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 80 или более поздней версии

  #### Описание
  С помощью этой политики вы можете настроить, нужно ли включать блокировку потенциально нежелательных приложений с помощью фильтра SmartScreen в Microsoft Defender. Функция блокировки потенциально нежелательных приложений с помощью фильтра SmartScreen в Microsoft Defender выводит предупреждающие сообщения, которые помогают защищать пользователей от программ для показа рекламы, коин-майнеров, пакетных программ и других приложений с низкой репутацией, размещенных на веб-сайтах. Блокировка потенциально нежелательных приложений с помощью фильтра SmartScreen в Microsoft Defender по умолчанию выключена.

Если политика включена, блокировка потенциально нежелательных приложений с помощью фильтра SmartScreen в Microsoft Defender включена.

Если политика отключена, блокировка потенциально нежелательных приложений с помощью фильтра SmartScreen в Microsoft Defender выключена.

Если политика не настроена, пользователи могут выбирать, нужно ли использовать блокировку потенциально нежелательных приложений с помощью фильтра SmartScreen в Microsoft Defender.

Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SmartScreenPuaEnabled
  - Имя групповой политики: Настроить фильтр SmartScreen в Microsoft Defender на блокировку потенциально нежелательных приложений
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки SmartScreen
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Настройки SmartScreen
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: SmartScreenPuaEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SmartScreenPuaEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ## Настройки содержимого policies

  [В начало](#microsoft-edge:-политики)

  ### AutoSelectCertificateForUrls
  #### Автоматический выбор сертификатов клиентов для этих узлов
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Список сайтов (на основе шаблонов URL-адресов), для которых Microsoft Edge автоматически выбирает сертификат клиента при соответствующем запросе от сайта.

Это значение должно быть массивом в виде преобразованных в строку словарей JSON. Форма каждого словаря имеет следующий вид { "pattern": "$URL_PATTERN", "filter" : $FILTER }, где $URL_PATTERN является шаблоном параметра содержимого. $FILTER ограничивает сертификаты клиента, из которых браузер может автоматически выбирать. Независимо от фильтра, можно использовать только сертификаты, которые соответствуют запросу сертификата от сервера. Например, если $FILTER имеет форму { "ISSUER": { "CN": "$ISSUER_CN" } }, дополнительно могут использоваться только сертификаты клиента, изданные сертификатом с параметром CommonName $ISSUER_CN. Если $FILTER содержит раздел "ISSUER" и "SUBJECT", может быть выбран только сертификат клиента, отвечающий обоим условиям. Если $FILTER определяет организацию ("O"), сертификат должен содержать минимум одну организацию, соответствующую указанному значению. Если $FILTER определяет подразделение организации ("OU"), сертификат должен содержать минимум одно подразделение организации, соответствующее указанному значению. Если $FILTER является пустым словарем {}, выбор сертификатов клиента дополнительно не ограничивается.

Если не настроить эту политику, автоматический выбор не выполняется ни для каких сайтов.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AutoSelectCertificateForUrls
  - Имя групповой политики: Автоматический выбор сертификатов клиентов для этих узлов
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls\1 = "{\"pattern\":\"https://www.contoso.com\",\"filter\":{\"ISSUER\":{\"CN\":\"certificate issuer name\", \"L\": \"certificate issuer location\", \"O\": \"certificate issuer org\", \"OU\": \"certificate issuer org unit\"}, \"SUBJECT\":{\"CN\":\"certificate subject name\", \"L\": \"certificate subject location\", \"O\": \"certificate subject org\", \"OU\": \"certificate subject org unit\"}}}"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AutoSelectCertificateForUrls
  - Пример значения:
``` xml
<array>
  <string>{"pattern":"https://www.contoso.com","filter":{"ISSUER":{"CN":"certificate issuer name", "L": "certificate issuer location", "O": "certificate issuer org", "OU": "certificate issuer org unit"}, "SUBJECT":{"CN":"certificate subject name", "L": "certificate subject location", "O": "certificate subject org", "OU": "certificate subject org unit"}}}</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### CookiesAllowedForUrls
  #### Разрешить использование файлов cookie на определенных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  На основе шаблона URL-адресов определите список сайтов, для которых разрешается установка файлов cookie.

Если эта политика не настроена, то для всех сайтов будут использоваться глобальные установки по умолчанию из политики [DefaultCookiesSetting](#defaultcookiessetting) (если она настроена) или личные настройки пользователя.

Дополнительные сведения см. в политиках [CookiesBlockedForUrls](#cookiesblockedforurls) и [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls).

Обратите внимание на недопустимость конфликтов в наборе шаблонов URL-адресов между этими тремя политиками:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- CookiesAllowedForUrls

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

Чтобы не допустить удаления файлов cookie при выходе, настройте политику [SaveCookiesOnExit](#savecookiesonexit).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: CookiesAllowedForUrls
  - Имя групповой политики: Разрешить использование файлов cookie на определенных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: CookiesAllowedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### CookiesBlockedForUrls
  #### Блокировать файлы cookie на определенных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  На основании шаблонов URL-адресов определите список сайтов, которым запрещено устанавливать файлы cookie.

Если не настроить эту политику, для всех сайтов будет использоваться глобальное значение по умолчанию из политики [DefaultCookiesSetting](#defaultcookiessetting) (если задано) или персональной конфигурации пользователя.

Дополнительные сведения см. в политиках [CookiesAllowedForUrls](#cookiesallowedforurls) и [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls).

Обратите внимание, что не должно быть конфликтующих шаблонов URL-адресов в следующих трех политиках:

- CookiesBlockedForUrls

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: CookiesBlockedForUrls
  - Имя групповой политики: Блокировать файлы cookie на определенных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: CookiesBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### CookiesSessionOnlyForUrls
  #### Ограничить файлы cookie от определенных веб-сайтов для текущего сеанса
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  По завершении сеанса (когда закрывается окно) удаляются файлы cookie, созданные веб-сайтами, которые соответствуют определенному вами шаблону URL-адреса.

Файлы cookie, созданные веб-сайтами, которые не соответствуют шаблону, подпадают под действие политики [DefaultCookiesSetting](#defaultcookiessetting) (если она настроена) или персональных настроек пользователя. Этот сценарий также выполняется по умолчанию, если эта политика не настроена.

Если Microsoft Edge работает в фоновом режиме, сеанс может не завершиться после закрытия последнего окна, и в этом случае файлы cookie не будут удалены, когда закроется окно. См. политику [BackgroundModeEnabled](#backgroundmodeenabled), чтобы узнать, какие настройки доступны для фонового режима работы Microsoft Edge.

Вы также можете использовать политики [CookiesAllowedForUrls](#cookiesallowedforurls) и [CookiesBlockedForUrls](#cookiesblockedforurls) для управления веб-сайтами, которым разрешено создавать файлы cookie.

Обратите внимание: в следующих трех политиках не должно быть конфликтующих шаблонов URL-адресов:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- CookiesSessionOnlyForUrls

Если настроить в политике [RestoreOnStartup](#restoreonstartup) восстановление URL-адресов из предыдущих сеансов, эта политика будет игнорироваться и файлы cookie соответствующих сайтов будут храниться постоянно.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: CookiesSessionOnlyForUrls
  - Имя групповой политики: Ограничить файлы cookie от определенных веб-сайтов для текущего сеанса
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: CookiesSessionOnlyForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultCookiesSetting
  #### Настройка файлов cookie
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Создание файлов cookie веб-сайтами на устройстве пользователя. Эта политика работает по принципу "все или ничего": можно разрешить всем сайтам создавать файлы cookie или запретить всем сайтам создавать файлы cookie. С помощью этой настройки невозможно разрешить создание файлов cookie только определенным сайтам.

Если параметру политики присвоено значение 'SessionOnly', файлы cookie удаляются по завершении сеанса. Если Microsoft Edge работает в фоновом режиме, сеанс может не завершиться после закрытия последнего окна, и в этом случае файлы cookie не будут удалены, когда закроется окно. См. политику [BackgroundModeEnabled](#backgroundmodeenabled), чтобы узнать, какие настройки доступны для фонового режима работы Microsoft Edge.

Когда эта политика не настроена, используется стандартное значение 'AllowCookies' и пользователи могут изменить это в разделе настроек Microsoft Edge. (Если вы не хотите разрешать пользователям изменять эту настройку, настройте эту политику).

Сопоставление параметров политики:

* AllowCookies (1) = Разрешить всем сайтам создавать файлы cookie

* BlockCookies (2) = Запретить всем сайтам создавать файлы cookie

* SessionOnly (4) = Сохранять все файлы cookie, кроме перечисленных в [SaveCookiesOnExit](#savecookiesonexit), в течение сеанса

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultCookiesSetting
  - Имя групповой политики: Настройка файлов cookie
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DefaultCookiesSetting
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultCookiesSetting
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultGeolocationSetting
  #### Настройка географического положения по умолчанию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Укажите, могут ли сайты отслеживать физическое местоположение пользователей. Можно разрешить отслеживание по умолчанию ('AllowGeolocation'), запретить его по умолчанию ('BlockGeolocation') или спрашивать пользователя каждый раз, когда веб-сайт запрашивает его местоположение ('AskGeolocation').

Если вы не настроите эту политику, используется 'AskGeolocation', и пользователь может ее изменить.

Сопоставление параметров политики:

* AllowGeolocation (1) = Разрешить сайтам отслеживать физическое местоположение пользователей

* BlockGeolocation (2) = Запретить всем сайтам отслеживать физическое местоположение пользователя

* AskGeolocation (3) = Спрашивать каждый раз, когда сайт хочет отслеживать физическое местоположение пользователей

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultGeolocationSetting
  - Имя групповой политики: Настройка географического положения по умолчанию
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DefaultGeolocationSetting
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultGeolocationSetting
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultImagesSetting
  #### Настройка изображений по умолчанию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Эта политика позволяет разрешить или запретить использование изображений на веб-сайтах. Можно либо разрешить изображения на всех сайтах ('AllowImages'), либо заблокировать их на всех сайтах ('BlockImages').

Если эта политика не настроена, изображения разрешены по умолчанию и пользователь может изменить данную настройку.

Сопоставление параметров политики:

* AllowImages (1) = Разрешить всем сайтам отображать все изображения

* BlockImages (2) = Запретить всем сайтам показывать изображения

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultImagesSetting
  - Имя групповой политики: Настройка изображений по умолчанию
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DefaultImagesSetting
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultImagesSetting
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultInsecureContentSetting
  #### Контролировать использование исключений для небезопасного содержимого
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 80 или более поздней версии

  #### Описание
  Эта политика позволяет разрешить или запретить пользователям добавлять исключения, разрешающие использование смешанного содержимого на определенных сайтах.

Эта политика может быть переопределена конкретными шаблонами URL-адресов при использовании политик [InsecureContentAllowedForUrls](#insecurecontentallowedforurls) и [InsecureContentBlockedForUrls](#insecurecontentblockedforurls).

Если оставить эту политику ненастроенной, пользователи смогут добавлять исключения, чтобы разрешить использование блокируемого смешанного содержимого и запретить автоматическое обновление смешанного содержимого, блокируемого по необходимости.

Сопоставление параметров политики:

* BlockInsecureContent (2) = Не разрешать сайтам загружать смешанное содержимое

* AllowExceptionsInsecureContent (3) = Разрешить пользователям добавлять исключения, чтобы разрешать смешанное содержимое

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultInsecureContentSetting
  - Имя групповой политики: Контролировать использование исключений для небезопасного содержимого
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DefaultInsecureContentSetting
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000002
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultInsecureContentSetting
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultJavaScriptSetting
  #### Настройка скриптов JavaScript по умолчанию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Эта настройка политики позволяет разрешить или запретить выполнение сценариев JavaScript на веб-сайтах. Можно либо разрешить сценарии JavaScript на всех сайтах ('AllowJavaScript'), либо заблокировать их на всех сайтах ('BlockJavaScript').

Если эта настройка политики не изменена, на всех сайтах можно запускать сценарии JavaScript по умолчанию и пользователь может изменить данную настройку.

Сопоставление параметров политики:

* AllowJavaScript (1) = Разрешить всем сайтам запускать скрипты JavaScript

* BlockJavaScript (2) = Запретить всем сайтам запускать скрипты JavaScript

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultJavaScriptSetting
  - Имя групповой политики: Настройка скриптов JavaScript по умолчанию
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DefaultJavaScriptSetting
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultJavaScriptSetting
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultNotificationsSetting
  #### Настройка уведомлений по умолчанию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Эта политика позволяет указать, могут ли веб-сайты отображать уведомления на рабочем столе. Можно либо разрешить это делать по умолчанию ('AllowNotifications'), либо запретить это делать по умолчанию ('BlockNotifications'), либо каждый раз запрашивать у пользователя соответствующее разрешение ('AskNotifications').

Если эта политика не настроена, уведомления разрешены по умолчанию и пользователь может изменить данную настройку.

Сопоставление параметров политики:

* AllowNotifications (1) = Разрешить сайтам отображать уведомления на рабочем столе

* BlockNotifications (2) = Запретить всем сайтам показывать уведомления на рабочем столе

* AskNotifications (3) = Спрашивать каждый раз, когда сайт хочет отображать уведомления на рабочем столе

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultNotificationsSetting
  - Имя групповой политики: Настройка уведомлений по умолчанию
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DefaultNotificationsSetting
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000002
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultNotificationsSetting
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultPluginsSetting
  #### Настройки Adobe Flash по умолчанию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Сначала проверяются [PluginsAllowedForUrls](#pluginsallowedforurls) и [PluginsBlockedForUrls](#pluginsblockedforurls), а затем эта политика. Возможные значения: "ClickToPlay" и "BlockPlugins". Если присвоить этому параметру политики значение "BlockPlugins", этот подключаемый модуль определяется для всех веб-сайтов. "ClickToPlay" позволяет запустить подключаемый модуль Flash, но пользователи нажимают заполнитель для его запуска.

Если данный параметр политики не задан, он будет использовать BlockPlugins, и пользователи смогут изменять его.

Примечание. автоматическое воспроизведение можно только для доменов, явно перечисленных в политике [PluginsAllowedForUrls](#pluginsallowedforurls). Чтобы включить автоматическое воспроизведение для всех сайтов, добавьте http://* и https://* в список разрешенных URL-адресов.

Сопоставление параметров политики:

* BlockPlugins (2) = Блокировать подключаемый модуль Adobe Flash

* ClickToPlay (3) = Щелкните, чтобы воспроизвести

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultPluginsSetting
  - Имя групповой политики: Настройки Adobe Flash по умолчанию
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DefaultPluginsSetting
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000002
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultPluginsSetting
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultPopupsSetting
  #### Настройка всплывающего окна по умолчанию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Эта политика позволяет разрешить или запретить всплывающие окна на сайтах. Можно либо разрешить всплывающие окна на всех сайтах ('AllowPopups'), либо заблокировать их на всех сайтах ('BlockPopups').

Если эта политика не настроена, всплывающие окна блокируются по умолчанию и пользователь может изменить эту настройку.

Сопоставление параметров политики:

* AllowPopups (1) = Разрешить всем сайтам показывать всплывающие окна

* BlockPopups (2) = Запретить всем сайтам отображать всплывающие окна

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultPopupsSetting
  - Имя групповой политики: Настройка всплывающего окна по умолчанию
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DefaultPopupsSetting
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultPopupsSetting
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultWebBluetoothGuardSetting
  #### Управление использованием веб-API Bluetooth
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Управление доступом веб-сайтов к находящимся рядом устройствам Bluetooth. Можно полностью заблокировать доступ или обязать сайт запрашивать у пользователя разрешение при каждой попытке получить доступ к устройству Bluetooth.

Если не настроить этот параметр политики, используется значение по умолчанию ('AskWebBluetooth', что означает каждый раз спрашивать у пользователя) и пользователи могут его изменять.

Сопоставление параметров политики:

* BlockWebBluetooth (2) = Запретить всем сайтам запрашивать доступ к устройствам Bluetooth через веб-API Bluetooth

* AskWebBluetooth (3) = Разрешить сайтам отправлять пользователю запрос на предоставление доступа к устройствам Bluetooth поблизости

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultWebBluetoothGuardSetting
  - Имя групповой политики: Управление использованием веб-API Bluetooth
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DefaultWebBluetoothGuardSetting
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000002
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultWebBluetoothGuardSetting
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultWebUsbGuardSetting
  #### Управление использованием API WebUSB
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Укажите, могут ли сайты получать доступ к подключенным USB-устройствам. Можно либо полностью заблокировать доступ, либо каждый раз запрашивать у пользователя соответствующее разрешение.

Эту политику можно переопределить для конкретных шаблонов URL-адресов с помощью политик [WebUsbAskForUrls](#webusbaskforurls) и [WebUsbBlockedForUrls](#webusbblockedforurls).

Если эта политика не настроена, сайты могут запрашивать у пользователя доступ к подключенным USB-устройствам ('AskWebUsb') по умолчанию, при этом пользователи могут изменить данную настройку.

Сопоставление параметров политики:

* BlockWebUsb (2) = Запретить всем сайтам запрашивать доступ к USB-устройствам через API WebUSB

* AskWebUsb (3) = Разрешить сайтам запрашивать у пользователя разрешение на доступ к подключенному USB-устройству

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultWebUsbGuardSetting
  - Имя групповой политики: Управление использованием API WebUSB
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DefaultWebUsbGuardSetting
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000002
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultWebUsbGuardSetting
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ImagesAllowedForUrls
  #### Разрешить изображения на этих сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  На основании шаблонов URL-адресов определите список сайтов, которые могут отображать изображения.

Если не настроить эту политику, для всех сайтов будет использоваться глобальное значение по умолчанию из политики [DefaultImagesSetting](#defaultimagessetting) (если задано) или персональной конфигурации пользователя.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ImagesAllowedForUrls
  - Имя групповой политики: Разрешить изображения на этих сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ImagesAllowedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ImagesBlockedForUrls
  #### Блокировать изображения на определенных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  На основании шаблонов URL-адресов определите список сайтов, которым запрещено отображать изображения.

Если не настроить эту политику, для всех сайтов будет использоваться глобальное значение по умолчанию из политики [DefaultImagesSetting](#defaultimagessetting) (если задано) или персональной конфигурации пользователя.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ImagesBlockedForUrls
  - Имя групповой политики: Блокировать изображения на определенных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ImagesBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### InsecureContentAllowedForUrls
  #### Разрешить небезопасное содержимое на указанных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 80 или более поздней версии

  #### Описание
  Задайте список шаблонов URL-адресов, чтобы указать сайты, которым разрешено отображать небезопасное смешанное содержимое (т. е. HTTP-содержимое на HTTPS-сайтах).

Если не настроить эту политику, блокируемое смешанное содержимое блокируется, а смешанное содержимое, блокируемое по необходимости, обновляется. Несмотря на это, пользователи могут задать исключения, чтобы разрешить для определенных сайтов небезопасное смешанное содержимое.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: InsecureContentAllowedForUrls
  - Имя групповой политики: Разрешить небезопасное содержимое на указанных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\2 = "[*.]example.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: InsecureContentAllowedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### InsecureContentBlockedForUrls
  #### Блокировать небезопасное содержимое на указанных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 80 или более поздней версии

  #### Описание
  Задайте список шаблонов URL-адресов, чтобы указать сайты, которым запрещено отображать блокируемое (т. е. активное) смешанное содержимое (например, содержимое HTTP на сайтах HTTPS) и для которых отключено обновление смешанного содержимого, блокируемого по необходимости.

Если не настроить эту политику, блокируемое смешанное содержимое будет блокироваться, смешанное содержимое, блокируемое по необходимости, будет обновляться, но пользователи смогут устанавливать исключения, чтобы разрешить небезопасное смешанное содержимое для определенных сайтов.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: InsecureContentBlockedForUrls
  - Имя групповой политики: Блокировать небезопасное содержимое на указанных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\2 = "[*.]example.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: InsecureContentBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### JavaScriptAllowedForUrls
  #### Разрешить скрипты JavaScript на определенных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  На основании шаблонов URL-адресов определите список сайтов, которым разрешено запускать скрипты JavaScript.

Если не настроить эту политику, для всех сайтов будет использоваться глобальное значение по умолчанию из политики [DefaultJavaScriptSetting](#defaultjavascriptsetting) (если задано) или персональной конфигурации пользователя.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: JavaScriptAllowedForUrls
  - Имя групповой политики: Разрешить скрипты JavaScript на определенных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: JavaScriptAllowedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### JavaScriptBlockedForUrls
  #### Блокировать скрипты JavaScript на определенных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  На основании шаблонов URL-адресов определите список сайтов, которым запрещено запускать скрипты JavaScript.

Если не настроить эту политику, для всех сайтов будет использоваться глобальное значение по умолчанию из политики [DefaultJavaScriptSetting](#defaultjavascriptsetting) (если задано) или персональной конфигурации пользователя.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: JavaScriptBlockedForUrls
  - Имя групповой политики: Блокировать скрипты JavaScript на определенных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: JavaScriptBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### LegacySameSiteCookieBehaviorEnabled
  #### Включить стандартную устаревшую настройку поведения файлов cookie SameSite
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 80 или более поздней версии

  #### Описание
  Позволяет вернуть устаревшее поведение SameSite для всех файлов cookie. Возврат к устаревшему поведению приведет к тому, что файлы cookie, которые не определяют атрибут SameSite, будут обрабатываться, как если бы они были "SameSite=None". Также будет удалено требование для файлов cookie "SameSite=None" нести атрибут "Secure".

Если не настроить эту политику, стандартное поведение для файлов cookie, которые не определяют атрибут SameSite, будет зависеть от других источников конфигурации для функции SameSite-by-default. Эту функцию можно настроить с помощью испытания на практике или включения флага same-site-by-default-cookies в разделе edge://flags.

Сопоставление параметров политики:

* DefaultToLegacySameSiteCookieBehavior (1) = Вернуться к устаревшему поведению SameSite для файлов cookie на всех сайтах

* DefaultToSameSiteByDefaultCookieBehavior (2) = Использовать поведение SameSite-by-default для файлов cookie на всех сайтах

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: LegacySameSiteCookieBehaviorEnabled
  - Имя групповой политики: Включить стандартную устаревшую настройку поведения файлов cookie SameSite
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: LegacySameSiteCookieBehaviorEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: LegacySameSiteCookieBehaviorEnabled
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### LegacySameSiteCookieBehaviorEnabledForDomainList
  #### Вернуться к устаревшему поведению для файлов cookie SameSite на указанных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 80 или более поздней версии

  #### Описание
  Для файлов cookie, установленных для доменов, соответствующих указанным шаблонам, будет возвращено устаревшее поведение SameSite.

Возврат к устаревшему поведению приведет к тому, что файлы cookie, которые не определяют атрибут SameSite, будут обрабатываться, как если бы они были "SameSite=None". Также будет удалено требование для файлов cookie "SameSite=None" нести атрибут "Secure".

Если не настроить эту политику, будет использоваться глобальное значение по умолчанию. Глобальное значение по умолчанию также будет использоваться для файлов cookie в доменах, которые не соответствуют шаблонам, указанным вами.

Глобальное значение по умолчанию можно настроить с помощью политики [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled). Если не настроить политику [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled), глобальное значение по умолчанию будет определяться другими источниками конфигурации.

Обратите внимание, что указанные вами в этой политике шаблоны обрабатываются как домены, а не URL-адреса, поэтому вы не можете указать схему или порт.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Имя групповой политики: Вернуться к устаревшему поведению для файлов cookie SameSite на указанных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\1 = "www.example.com"
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\2 = "[*.]example.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: LegacySameSiteCookieBehaviorEnabledForDomainList
  - Пример значения:
``` xml
<array>
  <string>www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### NotificationsAllowedForUrls
  #### Разрешить уведомления на определенных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Позволяет создать список шаблонов URL-адресов для указания сайтов, которым разрешено отображать уведомления.

Если вы не настроите эту политику, глобальное значение, используемое по умолчанию, будет применяться для всех сайтов. Это используемое по умолчанию значение берется из политики [DefaultNotificationsSetting](#defaultnotificationssetting), если она настроена, или из личной конфигурации пользователя. Подробную информацию о допустимых шаблонах URL-адресов см. на странице [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: NotificationsAllowedForUrls
  - Имя групповой политики: Разрешить уведомления на определенных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: NotificationsAllowedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### NotificationsBlockedForUrls
  #### Блокировать уведомления на определенных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Позволяет создать список шаблонов URL-адресов для указания сайтов, которым не разрешено отображать уведомления.

Если вы не настроите эту политику, глобальное значение, используемое по умолчанию, будет применяться для всех сайтов. Это используемое по умолчанию значение берется из политики [DefaultNotificationsSetting](#defaultnotificationssetting), если она настроена, или из личной конфигурации пользователя. Подробную информацию о допустимых шаблонах URL-адресов см. на странице [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: NotificationsBlockedForUrls
  - Имя групповой политики: Блокировать уведомления на определенных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: NotificationsBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### PluginsAllowedForUrls
  #### Разрешить подключаемый модуль Adobe Flash на определенных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определение списка сайтов, на которых возможен запуск подключаемого модуля Adobe Flash, на основе шаблонов URL-адресов.

Если эта политика не настроена, для всех сайтов используется глобальное значение по умолчанию из политики [DefaultPluginsSetting](#defaultpluginssetting) (если она настроена) или личные настройки пользователя.

Подробную информацию о допустимых шаблонах URL-адресов см. [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Однако начиная с M85 шаблоны с подстановочными знаками "*" и "[*.]" в адресе узла в этой политике больше не поддерживаются.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PluginsAllowedForUrls
  - Имя групповой политики: Разрешить подключаемый модуль Adobe Flash на определенных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\2 = "http://contoso.edu:8080"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: PluginsAllowedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### PluginsBlockedForUrls
  #### Блокировать подключаемый модуль Adobe Flash на определенных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определение списка сайтов, на которых заблокирован запуск Adobe Flash, на основе шаблонов URL-адресов.

Если эта политика не настроена, для всех сайтов используется глобальное значение по умолчанию из политики [DefaultPluginsSetting](#defaultpluginssetting) (если она настроена) или личные настройки пользователя.

Подробную информацию о допустимых шаблонах URL-адресов см. [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Однако начиная с M85 шаблоны с подстановочными знаками "*" и "[*.]" в адресе узла в этой политике больше не поддерживаются.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PluginsBlockedForUrls
  - Имя групповой политики: Блокировать подключаемый модуль Adobe Flash на определенных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\2 = "http://contoso.edu:8080"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: PluginsBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### PopupsAllowedForUrls
  #### Разрешить всплывающие окна на определенных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  На основании шаблонов URL-адресов определите список сайтов, которым разрешено открыть всплывающие окна.

Если не настроить эту политику, для всех сайтов будет использоваться глобальное значение по умолчанию из политики [DefaultPopupsSetting](#defaultpopupssetting) (если задано) или персональной конфигурации пользователя.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PopupsAllowedForUrls
  - Имя групповой политики: Разрешить всплывающие окна на определенных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: PopupsAllowedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### PopupsBlockedForUrls
  #### Блокировать всплывающие окна на определенных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  На основании шаблонов URL-адресов определите список сайтов, которым запрещено открывать всплывающие окна.

Если не настроить эту политику, для всех сайтов будет использоваться глобальное значение по умолчанию из политики [DefaultPopupsSetting](#defaultpopupssetting) (если задано) или персональной конфигурации пользователя.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PopupsBlockedForUrls
  - Имя групповой политики: Блокировать всплывающие окна на определенных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: PopupsBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### RegisteredProtocolHandlers
  #### Регистрация обработчиков протоколов
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Эта политика (только рекомендательного характера) задается для регистрации списка обработчиков протоколов. Этот список объединяется с другими такими списками, зарегистрированными пользователем, и все они доступны для использования.

Чтобы зарегистрировать обработчик протокола:

- В свойстве "Протокол" укажите соответствующую схему (например, "mailto").
- В свойстве "URL-адрес" укажите значение свойства "URL-адрес" приложения, ответственного за обработку схемы, которая указана в свойстве "Протокол". Шаблон может содержать заполнитель "%s", который заменяется обрабатываемым URL-адресом.

Пользователи не могут удалить обработчик протокола, зарегистрированный с помощью этой политики, но могут установить новый обработчик протокола по умолчанию и тем самым переопределить существующие обработчики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Нет
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Словарь

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: RegisteredProtocolHandlers
  - Имя групповой политики: Регистрация обработчиков протоколов
  - Путь групповой политики (Обязательно): Н/Д
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Настройки содержимого
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): Н/Д
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: RegisteredProtocolHandlers
  - Тип значения: REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [
  {
    "default": true, 
    "protocol": "mailto", 
    "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"
  }
]
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: RegisteredProtocolHandlers
  - Пример значения:
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
  

  [В начало](#microsoft-edge:-политики)

  ### SpotlightExperiencesAndRecommendationsEnabled
  #### Choose whether users can receive customized background images and text, suggestions, notifications,
and tips for Microsoft services
  
  
  #### Поддерживаемые версии:
  - На Windows с 86 или более поздней версии

  #### Описание
  Choose whether users can receive customized background images and text, suggestions, notifications, and tips for Microsoft services.

If you enable or don't configure this setting, spotlight experiences and recommendations are turned on.

If you disable this setting, spotlight experiences and recommendations are turned off.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SpotlightExperiencesAndRecommendationsEnabled
  - Имя групповой политики: Choose whether users can receive customized background images and text, suggestions, notifications,
and tips for Microsoft services
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: SpotlightExperiencesAndRecommendationsEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  

  [В начало](#microsoft-edge:-политики)

  ### WebUsbAllowDevicesForUrls
  #### Разрешить для определенных сайтов доступ к определенным USB-устройствам
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Позволяет задать список URL-адресов, определяющий сайты, которые могут автоматически получать разрешение на доступ к USB-устройству с заданными идентификатором поставщика и кодом продукта. Каждый элемент в списке должен содержать и устройства и URL-адреса, чтобы политика была действительной. Каждый элемент в устройствах может содержать поле идентификатора поставщика и кода продукта. Каждый пропущенный идентификатор обрабатывается как подстановочный знак с одним исключением: код продукта не может быть указан без указания идентификатора поставщика. В противном случае данная политика не будет действительной и будет игнорироваться.

В модели разрешения USB используется URL-адрес запрашивающего сайта ("запрашивающий URL-адрес") и URL-адрес сайта кадра верхнего уровня ("URL-адрес внедрения"), чтобы предоставить запрашивающему URL-адресу доступ к USB-устройству. Запрашивающий URL-адрес может отличаться от URL-адреса внедрения, когда запрашивающий сайт загружен в интернет-кадр. Из-за этого поле "urls" может содержать до двух строк URL-адресов, разделенных запятой, — для запрашивающего URL-адреса и URL-адреса внедрения соответственно. Если указан только один URL-адрес, доступ к соответствующим USB-устройствам предоставляется в тех случаях, когда URL-адрес запрашивающего сайта совпадает с этим URL-адресом независимо от наличия внедрения. URL-адреса в поле "urls" должны быть допустимыми URL-адресами, иначе эта политика будет игнорироваться.

Если не настроить эту политику, для всех сайтов будет использоваться глобальное значение по умолчанию из политики [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (если настроена) или персональной конфигурации пользователя.

Шаблоны URL-адресов в этой политике не должны конфликтовать с шаблонами, настроенными в политике [WebUsbBlockedForUrls](#webusbblockedforurls). В случае конфликта шаблонов эта политика имеет преимущественную силу по сравнению с политиками [WebUsbBlockedForUrls](#webusbblockedforurls) и [WebUsbAskForUrls](#webusbaskforurls).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Словарь

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: WebUsbAllowDevicesForUrls
  - Имя групповой политики: Разрешить для определенных сайтов доступ к определенным USB-устройствам
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: WebUsbAllowDevicesForUrls
  - Тип значения: REG_SZ
  ##### Пример значения:
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


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: WebUsbAllowDevicesForUrls
  - Пример значения:
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
  

  [В начало](#microsoft-edge:-политики)

  ### WebUsbAskForUrls
  #### Разрешить WebUSB на определенных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  На основании шаблонов URL-адресов определите список сайтов, которые могут отправлять пользователю запрос на доступ к USB-устройству.

Если не настроить эту политику, для всех сайтов будет использоваться глобальное значение по умолчанию из политики [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (если задано) или личной конфигурации пользователя.

Определенные в этой политике шаблоны URL-адресов не должны конфликтовать с шаблонами, настроенными в политике [WebUsbBlockedForUrls](#webusbblockedforurls). Нельзя одновременно разрешить и блокировать URL-адрес. Подробную информацию о допустимых шаблонах URL-адресов см. на странице [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: WebUsbAskForUrls
  - Имя групповой политики: Разрешить WebUSB на определенных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: WebUsbAskForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### WebUsbBlockedForUrls
  #### Блокировать WebUSB на определенных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  На основании шаблонов URL-адресов определите список сайтов, которые не могут отправлять пользователю запрос на доступ к USB-устройству.

Если не настроить эту политику, для всех сайтов будет использоваться глобальное значение по умолчанию из политики [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) (если задано) или личной конфигурации пользователя.

Определенные в этой политике шаблоны URL-адресов не должны конфликтовать с шаблонами, настроенными в политике [WebUsbAskForUrls](#webusbaskforurls). Нельзя одновременно разрешить и блокировать URL-адрес. Подробную информацию о допустимых шаблонах URL-адресов см. на странице [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: WebUsbBlockedForUrls
  - Имя групповой политики: Блокировать WebUSB на определенных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Настройки содержимого
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: WebUsbBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ## Печать policies

  [В начало](#microsoft-edge:-политики)

  ### DefaultPrinterSelection
  #### Правила выбора принтера по умолчанию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Переопределение правил выбора стандартного принтера в браузере Microsoft Edge. Этот параметр политики определяет правила выбора стандартного принтера в Microsoft Edge. Такой выбор происходит, когда пользователь в первый раз пытается напечатать страницу.

Если этот параметр политики задан, Microsoft Edge находит принтер, который соответствует всем указанным атрибутам, и использует его в качестве стандартного. При наличии нескольких принтеров, которые соответствуют критериям, используется первый подходящий принтер.

Если этот параметр политики не настроен или соответствующие критериям принтеры не найдены в течение заданного времени, стандартным назначается встроенный PDF-принтер или, если PDF-принтер недоступен, не назначается ни один принтер.

Это значение анализируется как объект JSON, соответствующий следующей схеме: { "type": "object", "properties": { "idPattern": { "description": "Regular expression to match printer id.", "type": "string" }, "namePattern": { "description": "Regular expression to match printer display name.", "type": "string" } } }

Пропуск поля означает, что все значения подходят. Например, если не указать подключение, функция предварительного просмотра начинает поиск всех типов локальных принтеров. Шаблоны регулярных выражений должны соответствовать синтаксису JavaScript RegExp. Совпадения определяются с учетом регистра.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultPrinterSelection
  - Имя групповой политики: Правила выбора принтера по умолчанию
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Печать
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DefaultPrinterSelection
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"{ \"idPattern\": \".*public\", \"namePattern\": \".*Color\" }"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultPrinterSelection
  - Пример значения:
``` xml
<string>{ "idPattern": ".*public", "namePattern": ".*Color" }</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### PrintHeaderFooter
  #### Печать колонтитулов
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Принудительное включение или отключение колонтитулов в диалоговом окне печати.

Если не настроить этот параметр политики, пользователи смогут включать и отключать печать колонтитулов.

Если этот параметр политики отключен, пользователи не смогут печатать колонтитулы.

Если данный параметр политики включен, пользователи всегда будут печатать верхние и нижние колонтитулы.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PrintHeaderFooter
  - Имя групповой политики: Печать колонтитулов
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Печать
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Печать
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: PrintHeaderFooter
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: PrintHeaderFooter
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### PrintPreviewUseSystemDefaultPrinter
  #### Задать системный принтер по умолчанию в качестве принтера по умолчанию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Назначение стандартного системного принтера в качестве стандартного принтера для предварительного просмотра в Microsoft Edge вместо последнего использованного принтера.

Если этот параметр отключен или не настроен, последний использованный принтер используется в качестве стандартного в режиме предварительного просмотра.

Если этот параметр политики включен, в режиме предварительного просмотра по умолчанию используется стандартный принтер операционной системы.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PrintPreviewUseSystemDefaultPrinter
  - Имя групповой политики: Задать системный принтер по умолчанию в качестве принтера по умолчанию
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Печать
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Печать
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: PrintPreviewUseSystemDefaultPrinter
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: PrintPreviewUseSystemDefaultPrinter
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### PrintingEnabled
  #### Включить печать
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Включение печати в Microsoft Edge без возможности для пользователей изменять эту настройку.

Если эта политика включена или не настроена, пользователи могут печатать.

Если эта политика отключена, пользователи не могут печатать из Microsoft Edge. Печать будет отключена в меню "гаечный ключ", расширениях, приложениях JavaScript и других элементах. Пользователи по-прежнему смогут печатать из подключаемых модулей, которые обходят Microsoft Edge во время печати. Например, некоторые приложения Adobe Flash будут иметь в своем контекстном меню команду печати, на которую не распространяется эта политика.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PrintingEnabled
  - Имя групповой политики: Включить печать
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Печать
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: PrintingEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: PrintingEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### UseSystemPrintDialog
  #### Печать с помощью системного диалогового окна печати
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Вывод системного диалогового окна печати вместо окна предварительного просмотра.

Если этот параметр включен, Microsoft Edge открывает системное диалоговое окно печати вместо собственного окна предварительного просмотра, когда пользователь пытается выполнить печать.

Если этот параметр выключен или не настроен, при выборе команды печати открывается окно предварительного просмотра Microsoft Edge.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: UseSystemPrintDialog
  - Имя групповой политики: Печать с помощью системного диалогового окна печати
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Печать
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: UseSystemPrintDialog
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: UseSystemPrintDialog
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ## Проверка подлинности HTTP policies

  [В начало](#microsoft-edge:-политики)

  ### AllowCrossOriginAuthPrompt
  #### Разрешить запросы обычной проверки подлинности HTTP независимо от источника
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определяет для стороннего вложенного содержимого на странице возможность открыть диалоговое окно для обычной проверки подлинности HTTP.

Обычно эта возможность отключена для защиты от фишинга. Если не настроить этот параметр политики, он будет отключен и стороннее вложенное содержимое не сможет открыть диалоговое окно обычной проверки подлинности HTTP.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AllowCrossOriginAuthPrompt
  - Имя групповой политики: Разрешить запросы обычной проверки подлинности HTTP независимо от источника
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Проверка подлинности HTTP
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AllowCrossOriginAuthPrompt
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AllowCrossOriginAuthPrompt
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AuthNegotiateDelegateAllowlist
  #### Список серверов, которым Microsoft Edge может передавать учетные данные пользователя
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Настройка списка серверов, которым Microsoft Edge может передавать данные.

Можно указать несколько имен серверов через запятую. Допускаются подстановочные знаки (*).

Если не настроить этот параметр политики, Microsoft Edge не будет передавать учетные данные пользователя, даже если сервер определен как входящий в интрасеть.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AuthNegotiateDelegateAllowlist
  - Имя групповой политики: Список серверов, которым Microsoft Edge может передавать учетные данные пользователя
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Проверка подлинности HTTP
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AuthNegotiateDelegateAllowlist
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"contoso.com"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AuthNegotiateDelegateAllowlist
  - Пример значения:
``` xml
<string>contoso.com</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AuthSchemes
  #### Поддерживаемые схемы проверки подлинности
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определяет поддерживаемые схемы проверки подлинности HTTP.

Политики можно настроить с помощью следующих значений: "basic", "digest", "ntlm" и "negotiate". Несколько значений следует разделять запятыми.

Если не настроить этот параметр политики, используются все четыре схемы.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AuthSchemes
  - Имя групповой политики: Поддерживаемые схемы проверки подлинности
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Проверка подлинности HTTP
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AuthSchemes
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"basic,digest,ntlm,negotiate"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AuthSchemes
  - Пример значения:
``` xml
<string>basic,digest,ntlm,negotiate</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AuthServerAllowlist
  #### Настройка списка разрешенных серверов проверки подлинности
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определение серверов, для которых необходимо включить встроенную проверку подлинности. Встроенная проверка подлинности включается только в том случае, если Microsoft Edge получает запрос проверки подлинности от прокси-сервера или от указанного здесь сервера.

Для разделения нескольких имен серверов используйте запятые. Допускаются подстановочные знаки (*).

Если этот параметр политики не настроен, Microsoft Edge пытается определить, находится ли сервер в интрасети — только в этом случае он будет отвечать на запросы IWA. Если сервер подключен к Интернету, Microsoft Edge будет игнорировать его запросы IWA.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AuthServerAllowlist
  - Имя групповой политики: Настройка списка разрешенных серверов проверки подлинности
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Проверка подлинности HTTP
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AuthServerAllowlist
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"*contoso.com,contoso.com"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AuthServerAllowlist
  - Пример значения:
``` xml
<string>*contoso.com,contoso.com</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DisableAuthNegotiateCnameLookup
  #### Отключить поиск CNAME при согласовании проверки подлинности Kerberos
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определяется основа для создания SPN Kerberos — каноническое имя DNS (CNAME) или исходное введенное имя.

Если этот параметр включен, поиск CNAME пропускается и используется имя сервера (введенное).

Если этот параметр выключен или не настроен, используется каноническое имя сервера, определяемое с помощью поиска CNAME.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DisableAuthNegotiateCnameLookup
  - Имя групповой политики: Отключить поиск CNAME при согласовании проверки подлинности Kerberos
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Проверка подлинности HTTP
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DisableAuthNegotiateCnameLookup
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DisableAuthNegotiateCnameLookup
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### EnableAuthNegotiatePort
  #### Включить нестандартный порт в SPN Kerberos
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определяет, должен ли созданный SPN Kerberos включать нестандартный порт.

Если данный параметр политики включен, и пользователь включает в URL-адрес нестандартный порт (не порт 80 или 443), этот порт включается в созданный SPN Kerberos.

Если не настроить или отключить этот параметр политики, созданный SPN Kerberos не будет включать порт в любом случае.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: EnableAuthNegotiatePort
  - Имя групповой политики: Включить нестандартный порт в SPN Kerberos
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Проверка подлинности HTTP
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: EnableAuthNegotiatePort
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: EnableAuthNegotiatePort
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### NtlmV2Enabled
  #### Управление включением и отключением проверки подлинности NTLMv2
  
  
  #### Поддерживаемые версии:
  - На macOS с 77 или более поздней версии

  #### Описание
  Определяет, включен ли NTLMv2.

Все последние версии серверов Samba и Windows поддерживают NTLMv2. Отключать NTLMv2 следует только для устранения проблем с обратной совместимостью, так как это снизит безопасность проверки подлинности.

Если этот параметр политики не настроен, NTLMv2 включен по умолчанию.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  

  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: NtlmV2Enabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ## Прокси-сервер policies

  [В начало](#microsoft-edge:-политики)

  ### ProxyBypassList
  #### Настройка правил обхода прокси-сервера
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определение списка узлов, для которых Microsoft Edge обходит все прокси-серверы.

Эта политика применяется, только если вы выбрали значение "Использовать фиксированные прокси-серверы" для настройки [ProxyMode](#proxymode). Не включайте или не настраивайте эту политику, если вы выбрали другой режим настройки прокси-сервера.

Когда эта политика включен, вы можете создать список узлов, для которых Microsoft Edge не будет использовать прокси-сервер.

Когда эта политика не настроен, списки узлов, для которых Microsoft Edge обходит прокси-сервер, не создаются. Оставьте эту политику ненастроенной, если вы указали какой-либо другой способ настройки прокси-сервера.

Более подробные примеры см. на странице [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ProxyBypassList
  - Имя групповой политики: Настройка правил обхода прокси-сервера
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Прокси-сервер
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ProxyBypassList
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"https://www.contoso.com, https://www.fabrikam.com"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ProxyBypassList
  - Пример значения:
``` xml
<string>https://www.contoso.com, https://www.fabrikam.com</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ProxyMode
  #### Настройки прокси-сервера
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Выбор настроек прокси-сервера для Microsoft Edge. Если включить эту политику, пользователи не смогут изменить настройки прокси-сервера.

Если вы решите никогда не использовать прокси-сервер и всегда подключаться напрямую, все другие варианты будут игнорироваться.

Если задать использование системных настроек прокси-сервера, все другие варианты будут игнорироваться.

Если задать автоматическое определение прокси-сервера, все другие варианты будут игнорироваться.

Если выбрать режим фиксированных прокси-серверов, можно задать дополнительные параметры в настройках [ProxyServer](#proxyserver) и "Разделенный запятыми список правил обхода прокси-сервера".

Если задать использование сценария прокси-сервера (.pac), необходимо указать URL-адрес сценария в настройке "URL-адрес PAC-файла прокси-сервера".

Более подробные примеры см. на странице [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

Если эта политика включена, Microsoft Edge игнорирует все связанные с прокси-сервером настройки, указанные из командной строки.

Если не настроить эту политику, пользователи смогут выбрать свои настройки прокси-сервера.

Сопоставление параметров политики:

* ProxyDisabled (direct) = Никогда не использовать прокси-сервер

* ProxyAutoDetect (auto_detect) = Автоматическое определение настроек прокси-сервера

* ProxyPacScript (pac_script) = Использовать файл сценария (.pac) прокси-сервера

* ProxyFixedServers (fixed_servers) = Использовать фиксированные прокси-серверы

* ProxyUseSystem (system) = Использовать системные настройки прокси-сервера

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ProxyMode
  - Имя групповой политики: Настройки прокси-сервера
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Прокси-сервер
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ProxyMode
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"direct"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ProxyMode
  - Пример значения:
``` xml
<string>direct</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ProxyPacUrl
  #### Настроить URL-адрес PAC-файла прокси-сервера
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определение URL-адреса для PAC-файла автоматической настройки прокси-сервера.

Эта настройка политики применяется только в том случае, если в политике [ProxyMode](#proxymode) выбран вариант "Использовать файл сценария (.pac) прокси-сервера". Если для настройки прокси-сервера выбран другой режим, не включайте и не настраивайте эту политику.

Если эта настройка политики включена, можно указать URL-адрес для PAC-файла, который будет определять, как браузер автоматически выбирает подходящий прокси-сервер для доступа к определенному веб-сайту.

Если отключить или не настроить эту политику, PAC-файл не задается. Оставьте эту политику ненастроенной, если вы выбрали другой режим настройки прокси-сервера.

Более подробные примеры см. на странице [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ProxyPacUrl
  - Имя групповой политики: Настроить URL-адрес PAC-файла прокси-сервера
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Прокси-сервер
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ProxyPacUrl
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"https://internal.contoso.com/example.pac"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ProxyPacUrl
  - Пример значения:
``` xml
<string>https://internal.contoso.com/example.pac</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ProxyServer
  #### Настройка адреса или URL-адреса прокси-сервера
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определение URL-адреса прокси-сервера.

Эта политика применяется только в том случае, если в настройке [ProxyMode](#proxymode) выбран вариант "Использовать фиксированные прокси-серверы". Если выбран другой режим настройки прокси-сервера, не включайте и не настраивайте эту политику.

Если эта политика включена, заданный в нем прокси-сервер будет использоваться для всех URL-адресов.

Если отключить или не настроить эту политику, пользователи смогут выбрать свои настройки прокси-сервера в данном режиме. Оставьте эту ненастроенной, если вы выбрали другой режим настройки прокси-сервера.

Другие варианты и подробные примеры см. на странице [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ProxyServer
  - Имя групповой политики: Настройка адреса или URL-адреса прокси-сервера
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Прокси-сервер
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ProxyServer
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"123.123.123.123:8080"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ProxyServer
  - Пример значения:
``` xml
<string>123.123.123.123:8080</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ProxySettings
  #### Настройки прокси-сервера
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Настройки прокси-сервера для Microsoft Edge.

Если включить эту политику, Microsoft Edge будет игнорировать все связанные с прокси-сервером настройки, заданные из командной строки.

Если не настроить эту политику, пользователи смогут выбирать настройки прокси-сервера по своему усмотрению.

Эта политика переопределяет перечисленные ниже отдельные политики:

[ProxyMode](#proxymode)
[ProxyPacUrl](#proxypacurl)
[ProxyServer](#proxyserver)
[ProxyBypassList](#proxybypasslist)

В поле ProxyMode можно указать прокси-сервер, который будет использоваться браузером Microsoft Edge, и пользователи не смогут изменить эту настройку.

Поле ProxyPacUrl является URL-адресом PAC-файла прокси-сервера.

В поле ProxyServer указан URL-адрес прокси-сервера.

В поле ProxyBypassList указан список узлов прокси-сервера, которые Microsoft Edge будет обходить.

Если для настройки ProxyMode выбрать значение direct, прокси-сервер никогда не будет использоваться и все остальные поля будут игнорироваться.

Если для настройки ProxyMode выбрать значение system, будет использоваться системный прокси-сервер и все остальные поля будут игнорироваться.

Если для настройки ProxyMode выбрать значение auto_detect, все остальные поля будут игнорироваться.

Если для настройки ProxyMode выбрать значение fixed_server, будут использоваться поля ProxyServer и ProxyBypassList.

Если для настройки ProxyMode выбрать значение pac_script, будут использоваться поля ProxyPacUrl и ProxyBypassList.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Словарь

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ProxySettings
  - Имя групповой политики: Настройки прокси-сервера
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Прокси-сервер
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ProxySettings
  - Тип значения: REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {
  "ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", 
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ProxySettings
  - Пример значения:
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
  

  [В начало](#microsoft-edge:-политики)

  ## Расширения policies

  [В начало](#microsoft-edge:-политики)

  ### ExtensionAllowedTypes
  #### Настройка разрешенных типов расширений
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определение типов расширений, которые можно устанавливать, и ограничение доступа к среде выполнения.

Этот параметр определяет разрешенные типы расширений и узлы, с которыми они могут взаимодействовать. Для этого задается список строк, каждая из которых должна представлять собой одно из следующих значений: "extension", "theme", "user_script" и "hosted_app". Дополнительные сведения об этих типах см. в документации по расширениям Microsoft Edge.

Обратите внимание: этот параметр также влияет на расширения, которые устанавливаются автоматически с помощью политики [ExtensionInstallForcelist](#extensioninstallforcelist).

Если эта политика включена, разрешено устанавливать только расширения, которые соответствуют какому-либо типу из списка.

Если не настроить эту политику, ограничения относительно типов разрешений не будут применяться принудительно.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ExtensionAllowedTypes
  - Имя групповой политики: Настройка разрешенных типов расширений
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Расширения
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes\1 = "hosted_app"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ExtensionAllowedTypes
  - Пример значения:
``` xml
<array>
  <string>hosted_app</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ExtensionInstallAllowlist
  #### Разрешить установку определенных расширений
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  По умолчанию разрешены все расширения. Тем не менее, если вы заблокируете все расширения, задав для политики "ExtensionInstallBlockList" значение "*", пользователи смогут устанавливать только расширения, определенные в этой политике.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ExtensionInstallAllowlist
  - Имя групповой политики: Разрешить установку определенных расширений
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Расширения
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\2 = "extension_id2"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ExtensionInstallAllowlist
  - Пример значения:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ExtensionInstallBlocklist
  #### Управление расширениями, которые нельзя устанавливать
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определение списка конкретных расширений, которые пользователи НЕ могут устанавливать в Microsoft Edge. При развертывании этого параметра все установленные ранее расширения из данного списка отключаются и пользователь не может их включить. Если удалить расширение из списка заблокированных, оно будет автоматически повторно включено в том месте, где было установлено ранее.

Используйте "*" для блокировки всех расширений, не указанных явным образом в списке разрешенных.

Если этот параметр не настроен, пользователи могут установить любое расширение в Microsoft Edge.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ExtensionInstallBlocklist
  - Имя групповой политики: Управление расширениями, которые нельзя устанавливать
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Расширения
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\2 = "extension_id2"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ExtensionInstallBlocklist
  - Пример значения:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ExtensionInstallForcelist
  #### Определение автоматически устанавливаемых расширений
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определяет расширения, которые устанавливаются автоматически (без участия пользователя) и которые пользователи не могут удалить или отключить ("принудительно устанавливаемые"). Все разрешения, запрашиваемые расширениями, предоставляются неявным образом (без участия пользователя), включая любые дополнительные разрешения, запрашиваемые последующими версиями расширения. Кроме того, разрешения предоставляются для API расширения enterprise.deviceAttributes и enterprise.platformKeys. (Эти два API доступны только принудительно устанавливаемым расширениям.)

Эта политика имеет приоритет над потенциально конфликтующей с ней политикой [ExtensionInstallBlocklist](#extensioninstallblocklist). После удаления расширения из списка принудительно устанавливаемых Microsoft Edge его автоматически удаляет.

Принудительная установка ограничена только приложениями и расширениями, перечисленными на веб-сайте надстроек Microsoft Edge, для экземпляров, не являющихся следующими: экземпляры Windows, присоединенные к домену Microsoft Active Directory, либо экземпляры Windows 10 Pro и Windows Корпоративная, зарегистрированные для управления устройствами, а также экземпляры macOS, управляемые посредством MDM или присоединенные к домену через MCX.

Обратите внимание, что пользователи могут с помощью средств разработчика изменить исходный код любого расширения, потенциально превратив его в неработоспособное. Чтобы предотвратить это, настройте политику [DeveloperToolsAvailability](#developertoolsavailability).

Чтобы добавить расширение в список, используйте следующий формат.

[extensionID];[updateURL]

- extensionID — строка из 32 букв, представленная в разделе edge://extensions в режиме разработчика.

- updateURL (необязательно) — адрес XML-документа манифеста обновления для приложения или расширения (описано на странице [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043)). Если вы хотите установить расширение из интернет-магазина Chrome, укажите URL-адрес обновления интернет-магазина Chrome (https://clients2.google.com/service/update2/crx). Обратите внимание, что URL-адрес обновления, настроенный в этой политике, используется только для первичной установки; при последующих обновлениях расширения используется URL-адрес обновления, указанный в манифесте расширения. Если вы не настроите URL-адрес обновления, будет считаться, что расширение размещается в Microsoft Store, и будет применяться следующий URL-адрес обновления: https://edge.microsoft.com/extensionwebstorebase/v1/crx.

Например, адрес gggmmkjegpiggikcnhidnjjhmicpibll;https://edge.microsoft.com/extensionwebstorebase/v1/crx используется для установки приложения Microsoft Online с URL-адреса обновления, относящегося к Microsoft Store. Дополнительные сведения о размещении расширений см. на странице [https://go.microsoft.com/fwlink/?linkid=2095044](https://go.microsoft.com/fwlink/?linkid=2095044).

Если эта политика не настроена, никакие расширения не устанавливаются автоматически и пользователи могут удалить любое расширение в Microsoft Edge.

Обратите внимание, что эта политика не применяется в режиме InPrivate.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ExtensionInstallForcelist
  - Имя групповой политики: Определение автоматически устанавливаемых расширений
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Расширения
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\1 = "gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\2 = "abcdefghijklmnopabcdefghijklmnop"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ExtensionInstallForcelist
  - Пример значения:
``` xml
<array>
  <string>gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx</string>
  <string>abcdefghijklmnopabcdefghijklmnop</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ExtensionInstallSources
  #### Настройка источников установки расширений и пользовательских скриптов
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определение URL-адресов, с которых могут устанавливаться расширения и темы.

По умолчанию пользователи должны загрузить файл *.crx для каждого расширения или скрипта, который они хотят установить, а затем перетащить его на страницу настроек Microsoft Edge. Эта политика разрешает конкретным URL-адресам выполнять установку расширения или скрипта для пользователя.

Каждый элемент в этом списке представляет собой шаблон сопоставления стиля расширения (см. страницу [https://go.microsoft.com/fwlink/?linkid=2095039](https://go.microsoft.com/fwlink/?linkid=2095039)). Пользователи могут легко устанавливать элементы с любого URL-адреса, внесенного в этот список. Расположение файла *.crx и страница, с которой начинается загрузка (другими словами, источник ссылки), должны быть разрешены этими шаблонами.

Политика [ExtensionInstallBlocklist](#extensioninstallblocklist) имеет более высокий приоритет, чем эта политика. Ни одно расширение, внесенное в список блокировки, не будет установлено, даже если оно расположено на сайте, заданном в этой политике.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ExtensionInstallSources
  - Имя групповой политики: Настройка источников установки расширений и пользовательских скриптов
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Расширения
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources\1 = "https://corp.contoso.com/*"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ExtensionInstallSources
  - Пример значения:
``` xml
<array>
  <string>https://corp.contoso.com/*</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ExtensionSettings
  #### Настройки управления расширениями
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Настройки управления расширениями для Microsoft Edge.

Эта политика определяет множество настроек, включая настройки, управляемые любыми текущими политиками, связанными с расширениями. Она также переопределяет все устаревшие политики, если они еще настроены.

Эта политика сопоставляет идентификатор расширения или URL-адрес обновления со своей настройкой. При использовании идентификатора расширения настройка применяется только к указанному расширению. Используйте стандартную настройку для специального идентификатора "*", чтобы применить ее ко всем расширениям, которые конкретно не указаны в этой политике. При использовании URL-адреса обновления настройка применяется ко всем расширениям с точным URL-адресом обновления, указанном в манифесте этого расширения, как описано на странице [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Словарь

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ExtensionSettings
  - Имя групповой политики: Настройки управления расширениями
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Расширения
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ExtensionSettings
  - Тип значения: REG_SZ
  ##### Пример значения:
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


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ExtensionSettings
  - Пример значения:
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
  

  [В начало](#microsoft-edge:-политики)

  ## Служба поиска по умолчанию policies

  [В начало](#microsoft-edge:-политики)

  ### DefaultSearchProviderEnabled
  #### Включить службу поиска по умолчанию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Включение возможности использования поисковой системы по умолчанию.

Если эта политика включена, пользователи смогут выполнять поиск по условию, введенному в адресную строку (при условии, что это не URL-адрес).

Вы можете указать службу поиска по умолчанию, включив остальные политики поиска по умолчанию. Если оставить эти параметры пустыми (не настроенными) или настроенными неправильно, пользователь сможет выбрать поисковую систему по умолчанию.

Если эта политика отключена, пользователи не смогут выполнять поиск из адресной строки.

Если эта политика включена или отключена, пользователи не смогут переопределить ее.

Если не настроить эту политику, будет включено задание службы поиска по умолчанию, при этом пользователь сможет выбрать службу поиска по умолчанию и настроить список служб поиска.

Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

Начиная с версии Microsoft Edge 84, можно настроить эту политику в качестве рекомендуемой.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultSearchProviderEnabled
  - Имя групповой политики: Включить службу поиска по умолчанию
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Служба поиска по умолчанию
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Служба поиска по умолчанию
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: DefaultSearchProviderEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultSearchProviderEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultSearchProviderEncodings
  #### Кодировки службы поиска по умолчанию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Укажите кодировки, поддерживаемые службой поиска. Кодировки — это имена кодовых страниц, например UTF-8, GB2312 и ISO-8859-1. Они будут применяться в указанном порядке.

Это необязательная политика. Если она не задана, по умолчанию используется UTF-8.

Эта политика применяется только в том случае, если включены политики [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) и [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

С версии Microsoft Edge 84 можно настроить эту политику в качестве рекомендуемой. Если пользователь уже установил службу поиска по умолчанию, то служба поиска, настроенная рекомендуемой политикой, не будет добавлена в список служб поиска, из которого пользователь может выбирать. Если это требуемое поведение, используйте политику [ManagedSearchEngines](#managedsearchengines).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultSearchProviderEncodings
  - Имя групповой политики: Кодировки службы поиска по умолчанию
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Служба поиска по умолчанию
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Служба поиска по умолчанию
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано\DefaultSearchProviderEncodings
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\1 = "UTF-8"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\2 = "UTF-16"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\3 = "GB2312"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\4 = "ISO-8859-1"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultSearchProviderEncodings
  - Пример значения:
``` xml
<array>
  <string>UTF-8</string>
  <string>UTF-16</string>
  <string>GB2312</string>
  <string>ISO-8859-1</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultSearchProviderImageURL
  #### Определяет функцию поиска по изображению для системы поиска по умолчанию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Задает URL-адрес, используемый поисковой системой для нахождения изображений. Запросы поиска отправляются с помощью метода GET.

 Это необязательная политика. Если ее не настроить, поиск изображений выполняться не будет.

 Для Bing укажите такой URL-адрес поиска изображений:
 "{bing:baseURL}images/detail/search?iss=sbiupload&FORM=ANCMS1#enterInsights".

Для Google укажите такой URL-адрес поиска изображений: "{google:baseURL}searchbyimage/upload" .

 Для завершения настройки поиска изображений используйте политику [DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams).

 Эта политика применяется только в тех случаях, когда включены политики [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) и [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

 С версии Microsoft Edge 84 можно настроить эту политику в качестве рекомендуемой. Если пользователь уже установил службу поиска по умолчанию, то служба поиска, настроенная рекомендуемой политикой, не будет добавлена в список служб поиска, из которого пользователь может выбирать. Если это требуемое поведение, используйте политику [ManagedSearchEngines](#managedsearchengines).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultSearchProviderImageURL
  - Имя групповой политики: Определяет функцию поиска по изображению для системы поиска по умолчанию
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Служба поиска по умолчанию
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Служба поиска по умолчанию
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: DefaultSearchProviderImageURL
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"https://search.contoso.com/searchbyimage/upload"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultSearchProviderImageURL
  - Пример значения:
``` xml
<string>https://search.contoso.com/searchbyimage/upload</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultSearchProviderImageURLPostParams
  #### Параметры для URL-адреса изображения при использовании метода POST
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Если эта политика включена, она определяет параметры для поиска изображений с использованием метода POST. Здесь указываются пары имен/значений через запятую. Если в качестве значения используется шаблонный параметр (как {imageThumbnail} в предыдущем примере), он заменяется реальными данными эскиза изображения. Эта политика применяется только в тех случаях, когда включены политики [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) и [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

 Для Bing укажите следующие параметры метода POST для URL-адреса поиска изображений:
 "imageBin={google:imageThumbnailBase64}".

 Для Google укажите следующие параметры метода POST для URL-адреса поиска изображений:
 "coded_image={google:imageThumbnail},image_url={google:imageURL},sbisrc={google:imageSearchSource},original_width={google:imageOriginalWidth},original_height={google:imageOriginalHeight}".

 Если эта политика не настроена, для запросов поиска изображений используется метод GET.

С версии Microsoft Edge 84 можно задать эту политику в качестве рекомендуемой. Если пользователь уже установил службу поиска по умолчанию, то служба поиска, настроенная рекомендуемой политикой, не будет добавлена в список служб поиска, из которого пользователь может выбирать. Если это требуемое поведение, используйте политику [ManagedSearchEngines](#managedsearchengines).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultSearchProviderImageURLPostParams
  - Имя групповой политики: Параметры для URL-адреса изображения при использовании метода POST
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Служба поиска по умолчанию
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Служба поиска по умолчанию
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: DefaultSearchProviderImageURLPostParams
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"content={imageThumbnail},url={imageURL},sbisrc={SearchSource}"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultSearchProviderImageURLPostParams
  - Пример значения:
``` xml
<string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultSearchProviderKeyword
  #### Ключевое слово службы поиска по умолчанию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Указывает ключевое слово, которое является ярлыком, используемым в адресной строке для запуска поиска этого поставщика.

Этот параметр является необязательным. Если не настроить его, ключевое слово не активирует службу поиска.

Эта политика применяется только при включении политик [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) и [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

С версии Microsoft Edge 84 можно задать эту политику в качестве рекомендуемой. Если пользователь уже установил службу поиска по умолчанию, то служба поиска, настроенная рекомендуемой политикой, не будет добавлена в список служб поиска, из которого пользователь может выбирать. Если это требуемое поведение, используйте политику [ManagedSearchEngines](#managedsearchengines).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultSearchProviderKeyword
  - Имя групповой политики: Ключевое слово службы поиска по умолчанию
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Служба поиска по умолчанию
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Служба поиска по умолчанию
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: DefaultSearchProviderKeyword
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"mis"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultSearchProviderKeyword
  - Пример значения:
``` xml
<string>mis</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultSearchProviderName
  #### Имя службы поиска по умолчанию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Задает имя службы поиска по умолчанию.

Если эта политика включена, задается имя службы поиска, используемой по умолчанию.

Если эта политика не включена или не задана, используется имя узла, указанное в URL-адресе поиска.

В параметре [DefaultSearchProviderName](#defaultsearchprovidername) должна быть задана утвержденная организацией зашифрованная служба поиска, соответствующая зашифрованной службе поиска, заданной в DTBC-0008. Эта политика применяется только в том случае, если включены политики [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) и [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

С версии Microsoft Edge 84 можно настроить эту политику в качестве рекомендуемой. Если пользователь уже установил службу поиска по умолчанию, то служба поиска, настроенная рекомендуемой политикой, не будет добавлена в список служб поиска, из которого пользователь может выбирать. Если это требуемое поведение, используйте политику [ManagedSearchEngines](#managedsearchengines).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultSearchProviderName
  - Имя групповой политики: Имя службы поиска по умолчанию
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Служба поиска по умолчанию
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Служба поиска по умолчанию
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: DefaultSearchProviderName
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"My Intranet Search"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultSearchProviderName
  - Пример значения:
``` xml
<string>My Intranet Search</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultSearchProviderSearchURL
  #### Поисковый URL-адрес службы поиска по умолчанию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Задает URL-адрес поисковой системы, используемой для поиска по умолчанию. URL-адрес содержит строку "{searchTerms}", которая во время выполнения запроса заменяется терминами поиска пользователя.

Укажите URL-адрес для поиска в Bing так:

"{bing:baseURL}search?q={searchTerms}".

Укажите URL-адрес для поиска в Google так: "{google:baseURL}search?q={searchTerms}&{google:RLZ}{google:originalQueryForSuggestion}{google:assistedQueryStats}{google:searchFieldtrialParameter}{google:searchClient}{google:sourceId}ie={inputEncoding}".

Данная политика является обязательной, если включена политика [DefaultSearchProviderEnabled](#defaultsearchproviderenabled). Если эта политика не включена, данная политика игнорируется.

С версии Microsoft Edge 84 можно настроить эту политику в качестве рекомендуемой. Если пользователь уже установил службу поиска по умолчанию, то служба поиска, настроенная рекомендуемой политикой, не будет добавлена в список служб поиска, из которого пользователь может выбирать. Если это требуемое поведение, используйте политику [ManagedSearchEngines](#managedsearchengines).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultSearchProviderSearchURL
  - Имя групповой политики: Поисковый URL-адрес службы поиска по умолчанию
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Служба поиска по умолчанию
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Служба поиска по умолчанию
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: DefaultSearchProviderSearchURL
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"https://search.contoso.com/search?q={searchTerms}"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultSearchProviderSearchURL
  - Пример значения:
``` xml
<string>https://search.contoso.com/search?q={searchTerms}</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultSearchProviderSuggestURL
  #### URL-адреса службы поиска по умолчанию для предложений
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Задает URL-адрес поисковой системы, применяемой для предоставления вариантов поисковых запросов. Этот URL-адрес содержит строку "{searchTerms}", которая заменяется во время запроса текстом, уже введенным пользователем.

Это необязательная политика. Если ее не настроить, пользователи не будут видеть варианты поисковых запросов; они будут видеть варианты из своего журнала браузера и избранного.

URL-адрес вариантов поисковых запросов для Bing может быть определен так:

"{bing:baseURL}qbox?query={searchTerms}".

URL-адрес вариантов поисковых запросов для Google может быть определен так: "{google:baseURL}complete/search?output=chrome&q={searchTerms}".

Эта политика применяется только в тех случаях, когда включены политики [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) и [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

С версии Microsoft Edge 84 можно настроить эту политику в качестве рекомендуемой. Если пользователь уже установил службу поиска по умолчанию, то служба поиска, настроенная рекомендуемой политикой, не будет добавлена в список служб поиска, из которого пользователь может выбирать. Если это требуемое поведение, используйте политику [ManagedSearchEngines](#managedsearchengines).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultSearchProviderSuggestURL
  - Имя групповой политики: URL-адреса службы поиска по умолчанию для предложений
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Служба поиска по умолчанию
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Служба поиска по умолчанию
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: DefaultSearchProviderSuggestURL
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"https://search.contoso.com/suggest?q={searchTerms}"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultSearchProviderSuggestURL
  - Пример значения:
``` xml
<string>https://search.contoso.com/suggest?q={searchTerms}</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### NewTabPageSearchBox
  #### Настройка функции поиска на странице новой вкладки
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 85 или более поздней версии

  #### Описание
  Для поля поиска на странице новой вкладки можно задать значение "поле поиска (рекомендуется)" или "адресная строка", чтобы выполнять поиск на новых вкладках. Эта политика работает, только если задать для поисковой системы значение, отличное от Bing, и настроить следующие два параметра: [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) и [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl).

 Если отключить или не настроить эту политику и:

— Если поисковая система по умолчанию, указанная в адресной строке, — Bing, на странице новой вкладки используется поле поиска для поиска на новых вкладках.
— Если поисковая система по умолчанию, указанная в адресной строке, не Bing, пользователям предлагается дополнительный выбор (использовать адресную строку) при поиске на новых вкладках.


Если включить эту политику и задать для нее значение:

— "поле поиска (рекомендуется)" ('bing'), для поиска на новых вкладках будет использоваться поле поиска.
— "адресная строка" ('redirect'), для поиска на новых вкладках будет использоваться адресная строка.

Сопоставление параметров политики:

* bing (bing) = Окно поиска (рекомендуется)

* redirect (redirect) = Адресная строка

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: NewTabPageSearchBox
  - Имя групповой политики: Настройка функции поиска на странице новой вкладки
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Служба поиска по умолчанию
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/Служба поиска по умолчанию
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: NewTabPageSearchBox
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"bing"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: NewTabPageSearchBox
  - Пример значения:
``` xml
<string>bing</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ## Собственный обмен сообщениями policies

  [В начало](#microsoft-edge:-политики)

  ### NativeMessagingAllowlist
  #### Управление узлами собственного обмена сообщениями, которые могут использовать пользователи
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определение списка конкретных узлов собственного обмена сообщениями, доступных для использования в Microsoft Edge.

По умолчанию разрешены все узлы собственного обмена сообщениями. Если для параметра политики [NativeMessagingBlocklist](#nativemessagingblocklist) задано значение "*", блокируются все узлы собственного обмена сообщениями и загружаются только перечисленные здесь узлы.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: NativeMessagingAllowlist
  - Имя групповой политики: Управление узлами собственного обмена сообщениями, которые могут использовать пользователи
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Собственный обмен сообщениями
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\2 = "com.native.messaging.host.name2"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: NativeMessagingAllowlist
  - Пример значения:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### NativeMessagingBlocklist
  #### Настроить список блокировки для собственного обмена сообщениями
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определение запрещенных узлов собственного обмена сообщениями.

Символ "*" позволяет заблокировать все узлы собственного обмена сообщениями, не указанные явным образом в списке разрешенных узлов.

Если не настроить этот параметр политики, Microsoft Edge будет загружать все установленные узлы собственного обмена сообщениями.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: NativeMessagingBlocklist
  - Имя групповой политики: Настроить список блокировки для собственного обмена сообщениями
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Собственный обмен сообщениями
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\2 = "com.native.messaging.host.name2"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: NativeMessagingBlocklist
  - Пример значения:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### NativeMessagingUserLevelHosts
  #### Разрешить узлы собственного обмена сообщениями на уровне пользователя (установленные без разрешений администратора)
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Установка узлов собственного обмена сообщениями на уровне пользователя.

Если данный параметр политики отключен, Microsoft Edge использует только узлы собственного обмена сообщениями, установленные на уровне системы.

Если этот параметр политики не настроен, в Microsoft Edge по умолчанию разрешается использование узлов собственного обмена сообщениями на уровне пользователя.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: NativeMessagingUserLevelHosts
  - Имя групповой политики: Разрешить узлы собственного обмена сообщениями на уровне пользователя (установленные без разрешений администратора)
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/Собственный обмен сообщениями
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: NativeMessagingUserLevelHosts
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: NativeMessagingUserLevelHosts
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ## Additional policies

  [В начало](#microsoft-edge:-политики)

  ### AddressBarMicrosoftSearchInBingProviderEnabled
  #### Включать варианты поисковых запросов поиска (Майкрософт) в Bing в адресную строку
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 81 или более поздней версии

  #### Описание
  Включает отображение актуальных вариантов поисковых запросов поиска (Майкрософт) в Bing в список вариантов поисковых запросов в адресной строке, когда пользователь вводит поисковый запрос в эту адресную строку. Если этот параметр политики включен или не настроен, пользователи смогут видеть внутренние результаты, предоставленные поиском (Майкрософт) в Bing, в списке вариантов поиска в адресной строке Microsoft Edge. Чтобы результаты, предоставленные поиском (Майкрософт) в Bing отображались, пользователь должен выполнить вход в Microsoft Edge с помощью учетной записи Azure AD для соответствующей организации.
Если этот параметр политики отключен, пользователи не смогут видеть внутренние результаты в списке вариантов поиска в адресной строке Microsoft Edge.
Если администратор включил набор политик, предусматривающих принудительное назначение службы поиска по умолчанию ([DefaultSearchProviderEnabled](#defaultsearchproviderenabled), [DefaultSearchProviderName](#defaultsearchprovidername) и [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)), и Bing не является указанной службой поиска, эту политику применить невозможно, и варианты поисковых запросов поиска (Майкрософт) в Bing в списке вариантов поиска в адресной строке не будут отображаться.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AddressBarMicrosoftSearchInBingProviderEnabled
  - Имя групповой политики: Включать варианты поисковых запросов поиска (Майкрософт) в Bing в адресную строку
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AddressBarMicrosoftSearchInBingProviderEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AddressBarMicrosoftSearchInBingProviderEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AdsSettingForIntrusiveAdsSites
  #### Настройка рекламы для сайтов с навязчивой рекламой
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 78 или более поздней версии

  #### Описание
  Определяет, блокировать ли рекламу на сайтах с навязчивой рекламой.

Сопоставление параметров политики:

* AllowAds (1) = Разрешить рекламу на всех сайтах

* BlockAds (2) = Блокировка рекламы на сайтах с навязчивой рекламой. (Значение по умолчанию)

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AdsSettingForIntrusiveAdsSites
  - Имя групповой политики: Настройка рекламы для сайтов с навязчивой рекламой
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AdsSettingForIntrusiveAdsSites
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AdsSettingForIntrusiveAdsSites
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AllowDeletingBrowserHistory
  #### Включить удаление журнала браузера и журнала загрузок
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Удаление журнала браузера и журнала скачиваний без возможности для пользователей изменять эту настройку.

Обратите внимание: даже если эта политика отключена, журнал браузера и журнал скачиваний не обязательно будут сохраняться, так как пользователи могут изменить или удалить файлы базы данных журнала, а сам браузер может в любое время удалить (на основании срока действия) или заархивировать некоторые или все элементы журнала.

Если эта политика включена или не настроена, пользователи могут удалять журнал браузера и журнал скачиваний.

Если эта политика отключена, пользователи не могут удалять журнал браузера и журнал скачиваний.

Если эта политика включена, не включайте политику [ClearBrowsingDataOnExit](#clearbrowsingdataonexit), так как обе эти политики связаны с удалением данных. В противном случае политика [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) будет иметь приоритет и все данные будут удаляться при закрытии Microsoft Edge независимо от настройки этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AllowDeletingBrowserHistory
  - Имя групповой политики: Включить удаление журнала браузера и журнала загрузок
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AllowDeletingBrowserHistory
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AllowDeletingBrowserHistory
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AllowFileSelectionDialogs
  #### Разрешить диалоговые окна выбора файлов
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Доступ к локальным файлам через диалоговые окна выбора файлов в Microsoft Edge.

Если включить или не настроить этот параметр политики, пользователи смогут открыть диалоговые окна выбора файлов в обычном режиме.

Если отключить этот параметр политики, при каждом действии пользователя, запускающем диалоговое окно выбора файлов (например, импорт избранного, загрузка файлов или сохранение ссылок), выводится сообщение и пользователь должен нажать кнопку "Отмена" в диалоговом окне выбора файлов.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AllowFileSelectionDialogs
  - Имя групповой политики: Разрешить диалоговые окна выбора файлов
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AllowFileSelectionDialogs
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AllowFileSelectionDialogs
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AllowPopupsDuringPageUnload
  #### Позволяет странице отображать всплывающие окна во время ее выгрузки
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 78 или более поздней версии

  #### Описание
  Эта политика позволяет администратору указать, что страница может отображать всплывающие окна во время ее выгрузки.

Если этот параметр политики включен, страницам разрешено отображать всплывающие окна во время выгрузки.

Если этот параметр политики отключен или не определен, страницы не смогут отображать всплывающие окна во время выгрузки. Это относится к следующей спецификации: (https://html.spec.whatwg.org/#apis-for-creating-and-navigating-browsing-contexts-by-name).

Эта политика будет удалена в будущем.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AllowPopupsDuringPageUnload
  - Имя групповой политики: Позволяет странице отображать всплывающие окна во время ее выгрузки
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AllowPopupsDuringPageUnload
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AllowPopupsDuringPageUnload
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AllowSurfGame
  #### Разрешить игру "Серфинг"
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 83 или более поздней версии

  #### Описание
  Если этот параметр политики отключен, пользователи не смогут играть в игру "Серфинг", когда устройство находится не в сети или когда пользователь переходит на страницу edge://surf.

Если этот параметр политики включен или не настроен, пользователи смогут играть в игру "Серфинг".

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AllowSurfGame
  - Имя групповой политики: Разрешить игру "Серфинг"
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AllowSurfGame
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AllowSurfGame
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AllowSyncXHRInPageDismissal
  #### Разрешить отправку синхронных запросов XHR при закрытии страницы (не рекомендуется)
  >УСТАРЕЛО. Эта политика устарела. В настоящее время она поддерживается, но станет устаревшей в будущем выпуске.
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 79 или более поздней версии

  #### Описание
  Применение этой политики не рекомендуется. Она предназначена для использования только в качестве краткосрочного механизма, чтобы дать предприятиям больше времени для обновления своего веб-контента, если окажется, что он несовместим с изменением, запрещающим синхронные запросы XHR во время закрытия страницы. Она не будет работать в Microsoft Edge версии 88.

Эта политика позволяет вам указать, что страница может отправлять синхронные запросы XHR во время закрытия страницы.

Если эта политика включена, страницы могут отправлять синхронные запросы XHR во время закрытия страницы.

Если эта политика отключена или не настроена, страницам не разрешается отправлять синхронные запросы XHR во время закрытия страницы.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AllowSyncXHRInPageDismissal
  - Имя групповой политики: Разрешить отправку синхронных запросов XHR при закрытии страницы (не рекомендуется)
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AllowSyncXHRInPageDismissal
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AllowSyncXHRInPageDismissal
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AllowTokenBindingForUrls
  #### Настройте список сайтов, для которых Microsoft Edge попытается создать привязку маркера.
  
  
  #### Поддерживаемые версии:
  - На Windows с 83 или более поздней версии

  #### Описание
  Настройте список шаблонов URL-адресов для сайтов, для которых браузер попытается выполнить протокол привязки маркера.
Для доменов в этом списке браузер будет отправлять ClientHello привязки маркера в рукопожатии TLS (см. https://tools.ietf.org/html/rfc8472).
Если сервер отвечает допустимым ответом ServerHello, браузер создает и отправляет сообщения привязки маркера в последующих HTTPS-запросах. Дополнительные сведения см. на странице https://tools.ietf.org/html/rfc8471.

Если этот список пуст, привязка маркера будет отключена.

Эта политика доступна только на устройствах с Windows 10 с возможностью виртуального безопасного режима.

Начиная с версии Microsoft Edge 86, эта политика больше не поддерживает динамическое обновление.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AllowTokenBindingForUrls
  - Имя групповой политики: Настройте список сайтов, для которых Microsoft Edge попытается создать привязку маркера.
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\2 = "[*.]mydomain2.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\3 = "[*.].mydomain2.com"

```


  

  [В начало](#microsoft-edge:-политики)

  ### AllowTrackingForUrls
  #### Настроить исключения из блокировки отслеживания для определенных сайтов
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 78 или более поздней версии

  #### Описание
  Настройка списка шаблонов URL-адресов, исключаемых из блокировки отслеживания.

Если этот параметр политики настроен, список заданных шаблонов URL-адресов исключается из блокировки отслеживания.

Если этот параметр политики не настроен, для всех сайтов используется глобальное стандартное значение параметра "Блокировка отслеживания просмотренных веб-страниц" (если установлено) или персональная настройка пользователя.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AllowTrackingForUrls
  - Имя групповой политики: Настроить исключения из блокировки отслеживания для определенных сайтов
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AllowTrackingForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AlternateErrorPagesEnabled
  #### Предлагать похожие страницы, если не удается найти веб-страницу
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 80 или более поздней версии

  #### Описание
  Подключение Microsoft Edge к веб-службе для создания URL-адреса и поиска вариантов решения проблем совместимости, например ошибок DNS.

Если эта политика включена, веб-служба используется для создания URL-адреса и поиска вариантов решения ошибок сети.

Если эта политика отключена, вызовы к веб-службе не выполняются и отображается стандартная страница ошибки.

Если не настроить эту политику, Microsoft Edge использует настройки пользователя, установленные в разделе "Службы" по адресу edge://settings/privacy.
А именно: в этом разделе есть переключатель **Предлагать похожие страницы, если не удается найти страницу**, который пользователь может включить или отключить. Обратите внимание, что если эта политика включена (AlternateErrorPagesEnabled), настройка "Предлагать похожие страницы, если не удается найти страницу" будет включена, но пользователь не сможет изменить эту настройку с помощью данного переключателя. Если отключить эту политику, настройка "Предлагать похожие страницы, если не удается найти страницу" будет отключена и пользователь не сможет изменить эту настройку с помощью данного переключателя.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AlternateErrorPagesEnabled
  - Имя групповой политики: Предлагать похожие страницы, если не удается найти веб-страницу
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: AlternateErrorPagesEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AlternateErrorPagesEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AlwaysOpenPdfExternally
  #### Всегда открывать PDF-файлы извне
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Отключение встроенного средства просмотра PDF-файлов в Microsoft Edge.

Если данный параметр политики включен, Microsoft Edge рассматривает PDF-файлы как загрузки и пользователи могут открыть их с помощью стандартного приложения.

Если не настроить этот параметр политики или отключить его, Microsoft Edge будет открывать PDF-файлы (если пользователь не отключит эту функцию).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AlwaysOpenPdfExternally
  - Имя групповой политики: Всегда открывать PDF-файлы извне
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AlwaysOpenPdfExternally
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AlwaysOpenPdfExternally
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AmbientAuthenticationInPrivateModesEnabled
  #### Включить проверку подлинности в среде для профилей InPrivate и гостевых профилей
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 81 или более поздней версии

  #### Описание
  Настройте этот параметр политики, чтобы разрешить или запретить внешнюю проверку подлинности для профилей InPrivate и гостевых профилей в Microsoft Edge.

Внешняя проверка подлинности — это http-проверка подлинности с учетными данными по умолчанию, когда явные учетные данные не предоставляются через схемы NTLM/Kerberos/Согласование запроса/ответ.

Если параметру политики присвоено значение 'RegularOnly', внешняя проверка подлинности разрешена только для обычных сеансов. Сеансам InPrivate и гостевым сеансам будет запрещено проводить внешнюю проверку подлинности.

Если параметру политики присвоено значение 'InPrivateAndRegular', внешняя проверка подлинности разрешена для сеансов InPrivate и обычных сеансов. Гостевым сеансам будет запрещено проводить внешнюю проверку подлинности.

Если параметру политики присвоено значение 'GuestAndRegular', запрос проверки подлинности разрешен для гостевых и обычных сеансов. Сеансам InPrivate будет запрещено проводить внешнюю проверку подлинности

Если параметру политики присвоено значение 'All', внешняя проверка подлинности разрешена для всех сеансов.

Обратите внимание, что внешняя проверка подлинности всегда разрешена на обычных профилях.

Если не настроить этот параметр политики в Microsoft Edge версии 81 и более поздней, внешняя проверка подлинности будет включена только в обычных сеансах.

Сопоставление параметров политики:

* RegularOnly (0) = Включить внешнюю проверку подлинности только в обычных сеансах

* InPrivateAndRegular (1) = Включить внешнюю проверку подлинности в сеансах InPrivate и обычных сеансах

* GuestAndRegular (2) = Включить внешнюю проверку подлинности в гостевых и обычных сеансах

* All (3) = Включить внешнюю проверку подлинности в обычных, гостевых сеансах и сеансах InPrivate

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AmbientAuthenticationInPrivateModesEnabled
  - Имя групповой политики: Включить проверку подлинности в среде для профилей InPrivate и гостевых профилей
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AmbientAuthenticationInPrivateModesEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AmbientAuthenticationInPrivateModesEnabled
  - Пример значения:
``` xml
<integer>0</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AppCacheForceEnabled
  #### Разрешает повторное включение функции AppCache, даже если она отключена по умолчанию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 84 или более поздней версии

  #### Описание
  Если для этого параметра политики задано значение «истина», AppCache включен, даже если AppCache в Microsoft Edge недоступен по умолчанию.

Если для этого параметра политики задано значение «ложь», или ничего не задано, AppCache будет функционировать в соответствии со стандартными настройками Microsoft Edge.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AppCacheForceEnabled
  - Имя групповой политики: Разрешает повторное включение функции AppCache, даже если она отключена по умолчанию
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AppCacheForceEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AppCacheForceEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ApplicationLocaleValue
  #### Настроить язык приложения
  
  
  #### Поддерживаемые версии:
  - На Windows с 77 или более поздней версии

  #### Описание
  Определение языкового стандарта приложения в Microsoft Edge без возможности для пользователей изменять этоу настройку.

Если эта политика включена, Microsoft Edge использует указанный языковой стандарт. Если настроенный языковой стандарт не поддерживается, вместо него используется "en-US".

Если отключить или не настроить эту политику, Microsoft Edge использует указанный пользователем предпочтительный языковой стандарт (если настроен) или базовый языковой стандарт "en-US".

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ApplicationLocaleValue
  - Имя групповой политики: Настроить язык приложения
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: ApplicationLocaleValue
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"en"
```


  

  [В начало](#microsoft-edge:-политики)

  ### AudioCaptureAllowed
  #### Разрешить или запретить запись звука
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Позволяет указать, будет ли пользователь получать от веб-сайта запрос на предоставление доступа к устройству записи звука. Эта политика применяется ко всем URL-адресам, кроме внесенных в список [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Если эта политика включена или не настроена (по умолчанию), пользователь получает запрос на доступ к аудиозаписи (кроме URL-адресов в списке [AudioCaptureAllowedUrls](#audiocaptureallowedurls)). Внесенным в список URL-адресам предоставляется доступ без запроса.

Если отключить эту политику, пользователь не будет получать запрос, а аудиозапись будет доступна только для URL-адресов, настроенных в списке [AudioCaptureAllowedUrls](#audiocaptureallowedurls).

Эта политика затрагивает все типы устройств ввода аудиоданных, а не только встроенный микрофон.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AudioCaptureAllowed
  - Имя групповой политики: Разрешить или запретить запись звука
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AudioCaptureAllowed
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AudioCaptureAllowed
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AudioCaptureAllowedUrls
  #### Сайты, которые могут получать доступ к устройствам записи звука без запроса разрешения
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  На основании шаблонов URL-адресов укажите веб-сайты, которые могут использовать устройства записи звука, без запроса разрешения пользователя. Шаблоны в этом списке сопоставляются с источником безопасности запрашивающего URL-адреса. Если они совпадают, сайту автоматически предоставляется доступ к устройствам записи звука.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AudioCaptureAllowedUrls
  - Имя групповой политики: Сайты, которые могут получать доступ к устройствам записи звука без запроса разрешения
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AudioCaptureAllowedUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AudioSandboxEnabled
  #### Разрешить запуск аудиопесочницы
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 81 или более поздней версии

  #### Описание
  Эта политика управляет песочницей аудиопроцесса.

Если включить этот параметр политики, аудиопроцесс будет запускаться в песочнице.

Если отключить этот параметр политики, аудиопроцесс будет запускаться вне песочницы, и модуль обработки аудио WebRTC будет запускаться в процессе обработчика.
Это создает угрозу для безопасности пользователей, связанную с запуском аудиоподсистем вне изолированной среды.

Если не настроить эту политику, будет использоваться стандартная конфигурация для аудиопесочницы, которая может отличаться в зависимости от платформы.

Цель этой политики — обеспечить для организаций возможность отключения аудиопесочницы, если они используют настройки программ обеспечения безопасности, которые мешают работе этой песочницы.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AudioSandboxEnabled
  - Имя групповой политики: Разрешить запуск аудиопесочницы
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AudioSandboxEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AudioSandboxEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AutoImportAtFirstRun
  #### Автоматически импортировать данные и настройки другого браузера при первом запуске
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Если включить эту политику, все поддерживаемые типы данных и настройки из указанного браузера будут автоматически импортированы при первом запуске без уведомления пользователя. Также при первом запуске пропускается раздел импорта.

Данные браузера из устаревшей версии Microsoft Edge всегда переносятся без уведомления при первом запуске вне зависимости от значения этой политики.

Если для этой политики установлено значение 'FromDefaultBrowser', импортируются типы данных, соответствующие браузеру по умолчанию на управляемом устройстве.

Если браузер, указанный в качестве значения этой политики, отсутствует на управляемом устройстве, Microsoft Edge пропустит импорт, не уведомляя пользователя.

Если для этой политики установлено значение 'DisabledAutoImport', раздел импорта при первом запуске полностью пропускается и Microsoft Edge не импортирует автоматически данные браузера и настройки.

Если для этой политики установлено значение 'FromInternetExplorer', следующие типы данных будут импортированы из Internet Explorer:
1. Избранное или закладки
2. Сохраненные пароли
3. Поисковые системы
4. Журнал браузера
5. Домашняя страница

Если для этой политики установлено значение 'FromGoogleChrome', следующие типы данных будут импортированы из Google Chrome:
1. Избранное
2. Сохраненные пароли
3. Адреса и прочее
4. Данные платежей
5. Журнал браузера
6. Настройки
7. Закрепленные и открытые вкладки
8. Расширения
9. Файлы cookie

Примечание. Дополнительные сведения о данных, импортируемых из Google Chrome, см. по адресу [https://go.microsoft.com/fwlink/?linkid=2120835](https://go.microsoft.com/fwlink/?linkid=2120835)

Если для этой политики установлено значение 'FromSafari', данные пользователя больше не будут импортироваться в Microsoft Edge. Причина заключается в принципе работы Full Disk Access на компьютере Mac.
На компьютерах с версией macOS Mojave или выше нет возможности автоматически и без уведомлений импортировать данные Safari в Microsoft Edge.

Начиная с Microsoft Edge версии 83, если для этой политики установлено значение 'FromMozillaFirefox', следующие типы данных будут импортированы из Mozilla Firefox:
1. Избранное или закладки
2. Сохраненные пароли
3. Адреса и прочее
4. Журнал браузера

Если нужно отключить импорт определенных типов данных на управляемые устройства, можно использовать эту политику вместе с другими политиками, например [ImportAutofillFormData](#importautofillformdata), [ImportBrowserSettings](#importbrowsersettings), [ImportFavorites](#importfavorites) и т. д.

Сопоставление параметров политики:

* FromDefaultBrowser (0) = Автоматически импортирует все поддерживаемые типы данных и настройки из используемого по умолчанию браузера

* FromInternetExplorer (1) = Автоматически импортирует все поддерживаемые типы данных и настройки из Internet Explorer

* FromGoogleChrome (2) = Автоматически импортирует все поддерживаемые типы данных и настройки из Google Chrome

* FromSafari (3) = Автоматически импортирует все поддерживаемые типы данных и настройки из Safari

* DisabledAutoImport (4) = Отключает автоматический импорт, пропускает раздел импорта при первом запуске

* FromMozillaFirefox (5) = Автоматический импорт всех поддерживаемых типов данных и настроек из Mozilla Firefox

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AutoImportAtFirstRun
  - Имя групповой политики: Автоматически импортировать данные и настройки другого браузера при первом запуске
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AutoImportAtFirstRun
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000002
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AutoImportAtFirstRun
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AutoLaunchProtocolsFromOrigins
  #### Определение списка протоколов, которые могут запускать внешнее приложение из указанных источников без запроса к пользователю
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 85 или более поздней версии

  #### Описание
  Позволяет настроить список протоколов, а для каждого протокола — соответствующий список разрешенных шаблонов источников, которые могут запускать внешнее приложение без запроса к пользователю. При перечислении протоколов не следует включать конечный разделитель. Например, указывайте "skype" вместо "skype:" или "skype://".

Если настроить эту политику, протоколу будет разрешено запускать внешнее приложение без запроса политикой только в том случае, если:

– протокол указан в списке

– источник сайта, пытающегося запустить протокол, совпадает с одним из шаблонов источников в списке allowed_origins этого протокола.

Если любое из условий не соблюдается, запрос на запуск внешнего протокола не будет проигнорирован политикой.

Если не настроить эту политику, протоколы не смогут запускаться без запроса. Пользователи могут отказаться от запросов для отдельных протоколов или отдельных сайтов, если политике [ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox) не присвоено значение "Отключено". Эта политика не влияет на исключения из запросов для отдельных протоколов и отдельных сайтов, установленные пользователями.

Шаблоны с совпадающими источниками используют аналогичный формат для политики [URLBlocklist](#urlblocklist), задокументированный на странице [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Однако шаблоны с совпадающими источниками для этой политики не могут содержать элементы "/path" или "@query". Любой шаблон, содержащий элемент "/path" или "@query", будет игнорироваться.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Словарь

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AutoLaunchProtocolsFromOrigins
  - Имя групповой политики: Определение списка протоколов, которые могут запускать внешнее приложение из указанных источников без запроса к пользователю
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AutoLaunchProtocolsFromOrigins
  - Тип значения: REG_SZ
  ##### Пример значения:
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


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AutoLaunchProtocolsFromOrigins
  - Пример значения:
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
  

  [В начало](#microsoft-edge:-политики)

  ### AutoOpenAllowedForURLs
  #### URL-адреса, по которым можно применять AutoOpenFileTypes
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 85 или более поздней версии

  #### Описание
  Перечень URL-адресов, к которым будет применяться [AutoOpenFileTypes](#autoopenfiletypes). Эта политика не влияет на значения автоматического открытия, заданные пользователями с помощью полки загрузки … > пункт меню "Всегда открывать файлы этого типа".

Если задать URL-адреса для этой политики, она будет автоматически открывать файлы, только если URL-адрес настроен и тип файла указан в [AutoOpenFileTypes](#autoopenfiletypes). Если какое-либо из этих условий не выполняется, загрузки не будут открываться автоматически.

Если не настроить эту политику, все загруженные файлы, тип которых указан в [AutoOpenFileTypes](#autoopenfiletypes), будут открываться автоматически.

Шаблон URL-адреса должен быть отформатирован в соответствии с [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AutoOpenAllowedForURLs
  - Имя групповой политики: URL-адреса, по которым можно применять AutoOpenFileTypes
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\1 = "example.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\5 = ".exact.hostname.com"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AutoOpenAllowedForURLs
  - Пример значения:
``` xml
<array>
  <string>example.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AutoOpenFileTypes
  #### Список типов файлов, которые должны открываться автоматически при скачивании
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 85 или более поздней версии

  #### Описание
  Эта политика определяет список типов файлов, которые должны открываться автоматически при скачивании. Примечание. При перечислении типов файлов разделитель в начале не включается, т.е. вместо ".txt" следует указать "txt".

По умолчанию эти типы файлов будут открываться автоматически по всем URL-адресам. Политику [AutoOpenAllowedForURLs](#autoopenallowedforurls) можно использовать для ограничения списка URL-адресов, по которым эти типы файлов будут открываться автоматически.

Файлы, которые должны открываться автоматически, подлежат проверке включенным фильтром SmartScreen в Microsoft Defender и не откроются, если не пройдут эту проверку.

Типы файлов, для которых пользователь уже настроил автоматическое открытие, продолжат открываться автоматически при скачивании. Пользователь может настроить автоматическое открытие и для других типов файлов.

Если не настроить эту политику, при скачивании будут открываться автоматически только те типы файлов, для которых пользователь уже настроил автоматическое открытие.

Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AutoOpenFileTypes
  - Имя групповой политики: Список типов файлов, которые должны открываться автоматически при скачивании
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\1 = "exe"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\2 = "txt"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AutoOpenFileTypes
  - Пример значения:
``` xml
<array>
  <string>exe</string>
  <string>txt</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AutofillAddressEnabled
  #### Включить автозаполнение для адресов
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Включение функции автозаполнения для автоматического ввода сохраненных адресов в веб-формах.

Если этот параметр политики отключен, функция автозаполнения никогда не предлагает и не вводит информацию об адресах, а также не сохраняет дополнительные сведения об адресе, которые пользователь может отправить при просмотре веб-страниц.

Если этот параметр включен или не настроен, пользователи могут управлять функцией автозаполнения адресов в пользовательском интерфейсе.

Примечание. Отключив этот параметр политики, вы также остановите все действия для любых веб-форм, за исключением форм оплаты и паролей. Дальнейшие записи не будут сохраняться, и Microsoft Edge не будет предлагать или автоматически вводить какие-либо предыдущие записи.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AutofillAddressEnabled
  - Имя групповой политики: Включить автозаполнение для адресов
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: AutofillAddressEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AutofillAddressEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AutofillCreditCardEnabled
  #### Включить автозаполнение для кредитных карт
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Включение функции автозаполнения в Microsoft Edge, которая автоматически вносит данные кредитных карт в веб-формы, используя ранее сохраненные сведения.

Если этот параметр политики отключен, функция автозаполнения никогда не предлагает и не вносит данные кредитных карт, а также не сохраняет дополнительные сведения о кредитной карте, которые пользователи могут отправлять при просмотре веб-страниц.

Если этот параметр политики включен или не настроен, пользователи могут управлять функцией автозаполнения в отношении сведений о кредитных картах.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AutofillCreditCardEnabled
  - Имя групповой политики: Включить автозаполнение для кредитных карт
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: AutofillCreditCardEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AutofillCreditCardEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### AutoplayAllowed
  #### Разрешить автозапуск мультимедиа для веб-сайтов
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 78 или более поздней версии

  #### Описание
  Определение правил автозапуска мультимедиа для веб-сайтов.

Если выбран стандартный вариант "Не настроено", соблюдаются текущие настройки автозапуска мультимедиа, которые пользователь может изменить.

Если выбран вариант "Включено", для автозапуска устанавливается значение "Разрешить". Всем сайтам будет разрешено автоматически запускать мультимедиа, и пользователи не смогут переопределить эту политику.

Если выбран вариант "Выключено", для автозапуска устанавливается значение "Запретить". Всем сайтам будет запрещено автоматически запускать мультимедиа, и пользователи не смогут переопределить эту политику.

Чтобы политика вступила в силу, необходимо закрыть и снова открыть вкладку.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: AutoplayAllowed
  - Имя групповой политики: Разрешить автозапуск мультимедиа для веб-сайтов
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: AutoplayAllowed
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: AutoplayAllowed
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### BackgroundModeEnabled
  #### Разрешить фоновым приложениям продолжать работу после закрытия Microsoft Edge
  
  
  #### Поддерживаемые версии:
  - На Windows с 77 или более поздней версии

  #### Описание
  Процессы Microsoft Edge запускаются при входе в ОС и продолжают работу после закрытия последнего окна браузера. В этом сценарии фоновые приложения и текущий сеанс браузера остаются активными, включая все файлы cookie сеанса. На панели задач отображается значок выполняемого фонового процесса, с помощью которого этот процесс можно в любой момент остановить.

Если эта настройка политики включена, фоновый режим включен.

Если эта настройка политики отключена, фоновый режим отключен.

Если эта настройка политики не настроена, фоновый режим изначально отключен и пользователи могут управлять им в разделе edge://settings/system.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: BackgroundModeEnabled
  - Имя групповой политики: Разрешить фоновым приложениям продолжать работу после закрытия Microsoft Edge
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: BackgroundModeEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  

  [В начало](#microsoft-edge:-политики)

  ### BackgroundTemplateListUpdatesEnabled
  #### Включение фонового обновления списка доступных шаблонов для коллекций и других функций, использующих шаблоны
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 79 или более поздней версии

  #### Описание
  Включение или отключение фонового обновления списка доступных шаблонов для коллекций и других функций, использующих шаблоны. Шаблоны используются для извлечения многоформатных метаданных из веб-страницы при сохранении страницы в коллекции.

Если этот параметр включен или не настроен, список доступных шаблонов будет загружаться в фоновом режиме из службы Майкрософт каждые 24 часа.

Если этот параметр отключен, список доступных шаблонов будет загружаться по требованию. Этот тип загрузки может привести к снижению производительности коллекций и других функций.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: BackgroundTemplateListUpdatesEnabled
  - Имя групповой политики: Включение фонового обновления списка доступных шаблонов для коллекций и других функций, использующих шаблоны
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: BackgroundTemplateListUpdatesEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: BackgroundTemplateListUpdatesEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### BingAdsSuppression
  #### Блокировка всей рекламы в результатах поиска Bing
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 83 или более поздней версии

  #### Описание
  Включает поиск без рекламы в поисковой системе Bing.com

Если включить эту политику, пользователь сможет пользоваться поиском на bing.com без рекламы. Одновременно для настройки "Безопасный поиск" устанавливается значение "Строгий", которое не может быть изменено пользователем.

Если не настраивать эту политику, по умолчанию результаты поиска на bing.com будут содержать рекламу. Для настройки "Безопасный поиск" по умолчанию будет установлено значение "Умеренный", которое может быть изменено пользователем.

Эта политика доступна только для SKU учебных заведений категории K-12, определенных корпорацией Майкрософт в качестве клиентов EDU (образовательных учреждений).

Перейдите по адресу [https://go.microsoft.com/fwlink/?linkid=2119711](https://go.microsoft.com/fwlink/?linkid=2119711) для получения дополнительных сведений об этой политике или в одном из следующих случаев:

* Если у вас есть клиент EDU, но эта политика не работает.

* Ваш IP-адрес был включен в список разрешений для поиска без рекламы.

* Вы пользовались поиском без рекламы в устаревшей версии Microsoft Edge и хотели бы перейти на новую версию Microsoft Edge.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: BingAdsSuppression
  - Имя групповой политики: Блокировка всей рекламы в результатах поиска Bing
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: BingAdsSuppression
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: BingAdsSuppression
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### BlockThirdPartyCookies
  #### Блокировать сторонние файлы cookie
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Блокировать задание файлов cookie элементами веб-страницы, не принадлежащими домену, который указан в адресной строке.

Если эта политика включена, элементы веб-страницы, которые не принадлежат домену, указанному в адресной строке, не могут задавать файлы cookie

Если эта политика отключена, элементы веб-страницы из доменов, не относящихся к домену, указанному в адресной строке, могут задавать файлы cookie.

Если не настроить эту политику, будут включены сторонние файлы cookie, но пользователи смогут изменить эту настройку.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: BlockThirdPartyCookies
  - Имя групповой политики: Блокировать сторонние файлы cookie
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: BlockThirdPartyCookies
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: BlockThirdPartyCookies
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### BrowserAddProfileEnabled
  #### Разрешить создание профиля во всплывающем меню "Удостоверение" или на странице "Настройки"
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Создание новых профилей с помощью команды **Добавить профиль**.
Если эта политика включена или не настроена, в Microsoft Edge можно создавать новые профили с помощью команды **Добавить профиль** во всплывающем меню "Удостоверение" или на странице "Настройки".

Если эта политика отключена, пользователи не могут добавлять новые профили во всплывающем меню "Удостоверение" или на странице "Настройки".

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: BrowserAddProfileEnabled
  - Имя групповой политики: Разрешить создание профиля во всплывающем меню "Удостоверение" или на странице "Настройки"
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: BrowserAddProfileEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: BrowserAddProfileEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### BrowserGuestModeEnabled
  #### Включить режим гостя
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Использование гостевых профилей в Microsoft Edge. При использовании такого профиля браузер не импортирует данные о просмотре веб-страниц из имеющихся профилей и удаляет эти данные после закрытия всех гостевых профилей.

Если этот параметр политики включен или не настроен, пользователи могут просматривать веб-страницы в Microsoft Edge в гостевых профилях.

Если этот параметр политики отключен, пользователи не могут просматривать веб-страницы в Microsoft Edge в гостевых профилях.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: BrowserGuestModeEnabled
  - Имя групповой политики: Включить режим гостя
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: BrowserGuestModeEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: BrowserGuestModeEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### BrowserNetworkTimeQueriesEnabled
  #### Разрешить запросы к сетевой службе времени браузера
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Запрет периодической отправки запросов из Microsoft Edge в сетевую службу времени браузера для получения точной метки времени.

Если отключить этот параметр политики, Microsoft Edge прекратит отправку запросов в сетевую службу времени браузера.

Если этот параметр включен или не настроен, Microsoft Edge периодически отправляет запросы в сетевую службу времени браузера.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: BrowserNetworkTimeQueriesEnabled
  - Имя групповой политики: Разрешить запросы к сетевой службе времени браузера
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: BrowserNetworkTimeQueriesEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: BrowserNetworkTimeQueriesEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### BrowserSignin
  #### Настройки входа браузера
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Использование учетной записи пользователя и связанных служб (например, синхронизации и единого входа) в Microsoft Edge. Для определения доступности синхронизации используйте политику [SyncDisabled](#syncdisabled).

Если для данного параметра задано значение 'Disable', убедитесь, что политика [NonRemovableProfileEnabled](#nonremovableprofileenabled)также отключена, поскольку [NonRemovableProfileEnabled](#nonremovableprofileenabled) отключает создание профиля браузера, в который выполняется автоматический вход. Если обе политики настроены, Microsoft Edge будет использовать политику "Запретить вход в браузер" и работать так, как если бы политика [NonRemovableProfileEnabled](#nonremovableprofileenabled) была отключена.

Если для этого параметра задано значение 'Enable', пользователи могут входить в браузер. Вход в браузер не означает, что синхронизация включается по умолчанию; пользователь должен отдельно включить эту функцию.

Если для этого параметра задано значение 'Force', пользователи должны войти в свой профиль, чтобы использовать браузер. По умолчанию пользователи в этом случае могут выбирать, хотят ли они выполнять синхронизацию для учетной записи, если синхронизация не отключена администратором домена или политикой [SyncDisabled](#syncdisabled). Значение по умолчанию параметра [BrowserGuestModeEnabled](#browserguestmodeenabled) — false.

Если этот параметр не настроен, пользователи могут включить параметр входа в браузер и использовать его по своему усмотрению.

Сопоставление параметров политики:

* Disable (0) = Отключить вход в браузер

* Enable (1) = Включить вход с помощью браузера

* Force (2) = Требовать от пользователей выполнять вход для использования браузера

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: BrowserSignin
  - Имя групповой политики: Настройки входа браузера
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: BrowserSignin
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000002
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: BrowserSignin
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### BuiltInDnsClientEnabled
  #### Использовать встроенный DNS-клиент
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определяет, нужно ли использовать встроенный DNS-клиент.

Это влияет не на то, какие DNS-серверы используются, а на комплекс программного обеспечения, используемый для обмена данными с ними. Например, если операционная система настроена на использование корпоративного DNS-сервера, во встроенном DNS-клиенте будет применяться тот же сервер. Тем не менее есть вероятность, что DNS-клиент будет обращаться к серверам по-разному, используя более современные протоколы для DNS, такие как DNS-over-TLS.

Если включить эту политику, встроенный DNS-клиент используется (при наличии).

Если отключить эту политику, такой клиент никогда не используется.

Если не настроить эту политику, встроенный DNS-клиент включен по умолчанию в MacOS и пользователи могут изменять то, нужно ли его применять, — для этого они должны отредактировать параметр в расположении edge://flags или указать флаг командной строки.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: BuiltInDnsClientEnabled
  - Имя групповой политики: Использовать встроенный DNS-клиент
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: BuiltInDnsClientEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: BuiltInDnsClientEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### BuiltinCertificateVerifierEnabled
  #### Определяет, будет ли использоваться встроенное средство проверки сертификата для проверки сертификатов сервера (не рекомендуется)
  >УСТАРЕЛО. Эта политика устарела. В настоящее время она поддерживается, но станет устаревшей в будущем выпуске.
  
  #### Поддерживаемые версии:
  - На macOS с 83 или более поздней версии

  #### Описание
  Применение этой политики не рекомендуется. Она предназначена для использования только в качестве краткосрочного механизма, чтобы дать предприятиям больше времени для обновления своих сред и сообщать о проблемах, если выясняется, что они несовместимы со встроенным средством проверки сертификатов.

Она не будет работать в Microsoft Edge версии 87, когда планируется удалить поддержку прежнего средства проверки сертификатов в Mac OS X.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  

  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: BuiltinCertificateVerifierEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### CertificateTransparencyEnforcementDisabledForCas
  #### Отключить обязательную проверку прозрачности сертификатов для списка хэш-значений subjectPublicKeyInfo
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Отключает принудительное применение требований к прозрачности сертификата для списка хэш-данных subjectPublicKeyInfo.

Этот параметр политики разрешает отключать требования к публикации с помощью функции прозрачности сертификата для цепочек сертификатов, которые содержат сертификаты с одним из указанных хэшей subjectPublicKeyInfo. Этот параметр разрешает и дальше использовать для узлов предприятия сертификаты, которые считались бы в противном случае недоверенными, так как они не были правильно опубликованы.

Чтобы отключить принудительное применение прозрачности сертификата, когда задан этот параметр политики, должен выполняться один из следующих наборов условий.
1. Хэш включен в сведения subjectPublicKeyInfo сертификата сервера.
2. Хэш включен в сведения subjectPublicKeyInfo, содержащиеся в сертификате ЦС в цепочке сертификатов; этот сертификат ЦС ограничен через расширение X.509v3 nameConstraints; один или несколько атрибутов directoryName nameConstraints присутствуют в permittedSubtrees; directoryName содержит атрибут organizationName.
3. Хэш включен в сведения subjectPublicKeyInfo, содержащиеся в сертификате ЦС цепочки сертификатов; этот сертификат ЦС содержит один или несколько атрибутов organizationName в поле субъекта сертификата; сертификат сервера содержит то же количество атрибутов organizationName с одинаковыми значениями по байтам и в том же порядке.

Хэш subjectPublicKeyInfo задается путем объединения имени алгоритма хэша, символа "/" и кодировки Base64 этого алгоритма хэша, примененной к сведениям subjectPublicKeyInfo в DER-кодировке в указанном сертификате. Кодировка Base64 имеет тот же формат, что и SPKI Fingerprint в соответствии с разделом 2.4 RFC 7469. Нераспознанные алгоритмы хэша игнорируются. Единственным поддерживаемым алгоритмом хэша в настоящее время является "sha256".

Если этот параметр политики отключен или не задан, любой сертификат, который должен быть опубликован с помощью функции прозрачности сертификата, будет считаться недоверенным, если он не опубликован в соответствии с политикой прозрачности сертификата.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: CertificateTransparencyEnforcementDisabledForCas
  - Имя групповой политики: Отключить обязательную проверку прозрачности сертификатов для списка хэш-значений subjectPublicKeyInfo
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\2 = "sha256//////////////////////w=="

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: CertificateTransparencyEnforcementDisabledForCas
  - Пример значения:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### CertificateTransparencyEnforcementDisabledForLegacyCas
  #### Отключить обязательную проверку прозрачности сертификатов для списка устаревших центров сертификации
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Отключение принудительного применения политики прозрачности сертификатов для списка устаревших центров сертификации (ЦС).

Этот параметр политики позволяет отключить требования к прозрачной отправке сертификатов для цепочек, содержащих сертификаты с одним из указанных хэшей subjectPublicKeyInfo. Благодаря этому для корпоративных узлов продолжают использоваться сертификаты, которые иначе считались бы недоверенными из-за неправильной отправки.

Чтобы отключить принудительное применение политики прозрачности сертификатов, необходимо присвоить хэшу значение subjectPublicKeyInfo, которое отображается в сертификате ЦС и распознается как устаревший Центр сертификации (ЦС). Устаревший ЦС — это общедоступный ЦС, которому по умолчанию доверяли одна или несколько операционных систем, совместимых с Microsoft Edge.

Хэш subjectPublicKeyInfo указывается путем объединения имени хэш-алгоритма, символа "/" и кодировки Base64 этого хэш-алгоритма, применяемого к значению subjectPublicKeyInfo в кодировке DER для указанного сертификата. Данная кодировка Base64 представляет тот же формат, что и отпечаток SPKI, согласно RFC 7469, раздел 2.4. Нераспознанные хэш-алгоритмы игнорируются. Единственным поддерживаемым хэш-алгоритмом в данный момент является "sha256".

Когда этот параметр не настроен, любой сертификат, который должен быть отправлен с применением политики прозрачности сертификатов, считается недоверенным, если он не был отправлен в соответствии с этой политикой.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Имя групповой политики: Отключить обязательную проверку прозрачности сертификатов для списка устаревших центров сертификации
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\2 = "sha256//////////////////////w=="

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: CertificateTransparencyEnforcementDisabledForLegacyCas
  - Пример значения:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### CertificateTransparencyEnforcementDisabledForUrls
  #### Отключить обязательную проверку прозрачности сертификатов для определенных URL-адресов
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Отключение принудительного применения политики прозрачности сертификатов для заданных URL-адресов.

Этот параметр политики позволяет не передавать сертификаты для имен узлов на указанных URL-адресах с применением политики прозрачности сертификатов. Это означает, что вы можете использовать сертификаты, которые в противном случае считались бы недоверенными из-за неправильной передачи, однако при этом усложняется определение неправильно изданных сертификатов для таких узлов.

Сформируйте шаблон URL-адреса в соответствии с рекомендациями, изложенными на странице [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322). Так как сертификаты являются действительными для заданного имени узла независимо от схемы, порта или пути, в URL-адресе учитывается только часть имени узла. Узлы с подстановочными знаками не поддерживаются.

Когда этот параметр политики не настроен, любой сертификат, который должен быть передан с применением политики прозрачности сертификатов, считается недоверенным, если он не был передан.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: CertificateTransparencyEnforcementDisabledForUrls
  - Имя групповой политики: Отключить обязательную проверку прозрачности сертификатов для определенных URL-адресов
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\2 = ".contoso.com"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: CertificateTransparencyEnforcementDisabledForUrls
  - Пример значения:
``` xml
<array>
  <string>contoso.com</string>
  <string>.contoso.com</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ClearBrowsingDataOnExit
  #### Удалять данные о просмотре веб-страниц при закрытии Microsoft Edge
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 78 или более поздней версии

  #### Описание
  Microsoft Edge по умолчанию не удаляет при закрытии данные о просмотре веб-страниц. Данные о просмотре веб-страниц включают введенную в формы информацию, пароли и сведения о посещенных веб-сайтах.

При включении этой политики все данные о просмотре веб-страниц будут удаляться при каждом закрытии Microsoft Edge. Обратите внимание: включение этой политики имеет приоритет над вашими настройками [DefaultCookiesSetting](#defaultcookiessetting)

Если эта политика отключена или не настроена, пользователи могут настроить режим очистки данных о просмотре веб-страниц в разделе "Настройки".

При включении этой политики не настраивайте политику [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) или [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit), поскольку они касаются режима удаления данных о просмотре веб-страниц. Если вы настроили предыдущие политики и эту политику, все данные о просмотре веб-страниц будут удаляться при закрытии Microsoft Edge вне зависимости от настройки [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) или [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

Чтобы не допустить удаления файлов cookie при выходе, настройте политику [SaveCookiesOnExit](#savecookiesonexit).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ClearBrowsingDataOnExit
  - Имя групповой политики: Удалять данные о просмотре веб-страниц при закрытии Microsoft Edge
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: ClearBrowsingDataOnExit
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ClearBrowsingDataOnExit
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ClearCachedImagesAndFilesOnExit
  #### Удалять кэшированные изображения и файлы при закрытии Microsoft Edge
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 83 или более поздней версии

  #### Описание
  Microsoft Edge не удаляет по умолчанию кэшированные изображения и файлы при закрытии.

Если эта политика включена, кэшированные изображения и файлы будут удаляться каждый раз при закрытии Microsoft Edge.

Если эта политика отключена, пользователи не могут настраивать параметр кэшированных изображений и файлов в разделе edge://settings/clearBrowsingDataOnClose.

Если не настроить эту политику, пользователи могут решить, необходимо ли удалять кэшированные изображения и файлы при выходе.

Если эта политика отключена, не включайте политику [ClearBrowsingDataOnExit](#clearbrowsingdataonexit), поскольку они оба используются для удаления данных. Если настроить обе эти политики, политика [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) будет иметь приоритет и все данные будут удаляться при закрытии Microsoft Edge независимо от настройки [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ClearCachedImagesAndFilesOnExit
  - Имя групповой политики: Удалять кэшированные изображения и файлы при закрытии Microsoft Edge
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: ClearCachedImagesAndFilesOnExit
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ClearCachedImagesAndFilesOnExit
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ClickOnceEnabled
  #### Разрешить пользователям открыть файлы с помощью протокола ClickOnce
  
  
  #### Поддерживаемые версии:
  - На Windows с 78 или более поздней версии

  #### Описание
  Разрешить пользователям открывать файлы с помощью протокола ClickOnce. Протокол ClickOnce позволяет веб-сайтам запрашивать открытие файлов с определенного URL-адреса в браузере с помощью обработчика файлов ClickOnce на компьютере или другом устройстве пользователя.

Если эта политика включена, пользователи могут открывать файлы с помощью протокола ClickOnce. Эта политика переопределяет настройку ClickOnce, заданную пользователем на странице edge://flags/.

Если эта политика отключена, пользователи не могут открыть файлы с помощью протокола ClickOnce. В этом случае файл сохраняется в файловой системе через браузер. Эта политика переопределяет настройку ClickOnce, заданную пользователем на странице edge://flags/.

Если эта политика не настроена, пользователи с Microsoft Edge версии ниже Microsoft Edge 87 по умолчанию не могут открывать файлы с помощью протокола ClickOnce. Однако они могут включить протокол ClickOnce на странице edge://flags/. Пользователи с Microsoft Edge версии 87 или более поздней по умолчанию могут открывать файлы с помощью протокола ClickOnce. Однако они могут отключить протокол ClickOnce на странице edge://flags/.

Отключение ClickOnce может препятствовать нормальному запуску приложений ClickOnce (файлов с расширением ".application").

Дополнительные сведения о ClickOnce см. на страницах [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) и [https://go.microsoft.com/fwlink/?linkid=2099880](https://go.microsoft.com/fwlink/?linkid=2099880).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ClickOnceEnabled
  - Имя групповой политики: Разрешить пользователям открыть файлы с помощью протокола ClickOnce
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ClickOnceEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  

  [В начало](#microsoft-edge:-политики)

  ### CollectionsServicesAndExportsBlockList
  #### Блокировка доступа к указанному списку служб и целям экспорта в коллекциях
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 86 или более поздней версии

  #### Описание
  Перечислите конкретные службы и цели экспорта, которые недоступны пользователям в функции коллекций в Microsoft Edge. Это включает отображение дополнительных данных из Bing и экспорт коллекций в продукты Майкрософт или для внешних партнеров.

Если эта политика включена, службы и цели экспорта, соответствующие указанному списку, блокируются.

Если не настроить эту политику, к приемлемым службам и целям экспорта не будут применяться никакие ограничения.

Сопоставление параметров политики:

* pinterest_suggestions (pinterest_suggestions) = Рекомендации Pinterest

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: CollectionsServicesAndExportsBlockList
  - Имя групповой политики: Блокировка доступа к указанному списку служб и целям экспорта в коллекциях
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\1 = "pinterest_suggestions"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: CollectionsServicesAndExportsBlockList
  - Пример значения:
``` xml
<array>
  <string>pinterest_suggestions</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### CommandLineFlagSecurityWarningsEnabled
  #### Включить предупреждения системы безопасности для флагов командной строки
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 78 или более поздней версии

  #### Описание
  Если эта политика отключена, при запуске Microsoft Edge с флагами потенциально опасных элементов командной строки предупреждения системы безопасности не отображаются.

Если эта политика включена или не настроена, при запуске Microsoft Edge с такими флагами командной строки предупреждения системы безопасности отображаются.

Например, флаг "--disable-gpu-sandbox" вызывает такое предупреждение: "Вы используете неподдерживаемый флаг командной строки: --disable-gpu-sandbox. Это создает угрозу стабильности и безопасности".

Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: CommandLineFlagSecurityWarningsEnabled
  - Имя групповой политики: Включить предупреждения системы безопасности для флагов командной строки
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: CommandLineFlagSecurityWarningsEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: CommandLineFlagSecurityWarningsEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ComponentUpdatesEnabled
  #### Включить обновления компонентов в Microsoft Edge
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Если включить или не настроить этот параметр политики, в Microsoft Edge будет выполняться обновление компонентов.

Если отключить этот параметр политики или задать для него значение false, обновление будет отключено для всех компонентов в Microsoft Edge.

Из этого параметра, однако, исключены некоторые компоненты, например все компоненты, которые не содержат исполняемый код, не имеют существенного влияния на поведение браузера или имеют важное значение для безопасности. Это означает, что обновления, которые считаются "критически важными для безопасности", будут применяться, даже если данный параметр будет отключен.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ComponentUpdatesEnabled
  - Имя групповой политики: Включить обновления компонентов в Microsoft Edge
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ComponentUpdatesEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ComponentUpdatesEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ConfigureDoNotTrack
  #### Настроить запросы "Не отслеживать"
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Настройка запросов "Не отслеживать" для веб-сайтов, запрашивающих данные отслеживания. Запросы "Не отслеживать" сообщают веб-сайтам, которые вы посещаете, о том, что вы не хотите, чтобы ваши действия в сети отслеживались. По умолчанию Microsoft Edge не отправляет запросы "Не отслеживать", но пользователи могут включить данную функцию для отправки таких запросов.

Если этот параметр политики включен, запросы "Не отслеживать" всегда отправляются на веб-сайты, запрашивающие данные отслеживания.

Если отключить этот параметр политики, запросы не будут отправляться.

Если не настроить этот параметр политики, пользователи смогут разрешить или запретить отправку таких запросов.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ConfigureDoNotTrack
  - Имя групповой политики: Настроить запросы "Не отслеживать"
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ConfigureDoNotTrack
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ConfigureDoNotTrack
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ConfigureOnPremisesAccountAutoSignIn
  #### Настройка автоматического входа с использованием учетной записи домена Active Directory при отсутствии учетной записи домена Azure AD
  
  
  #### Поддерживаемые версии:
  - На Windows с 81 или более поздней версии

  #### Описание
  Разрешите автоматический вход с помощью учетных записей Active Directory, если компьютеры ваших пользователей присоединены к домену и ваша среда не включена в гибридную систему. Если вы хотите, чтобы пользователи автоматически входили в свои учетные записи Azure Active Directory, присоедините свою среду к Azure AD (см. подробные сведения на странице [https://go.microsoft.com/fwlink/?linkid=2118197](https://go.microsoft.com/fwlink/?linkid=2118197)) или к гибридной системе (см. подробные сведения на странице [https://go.microsoft.com/fwlink/?linkid=2118365](https://go.microsoft.com/fwlink/?linkid=2118365)).

Если политика [BrowserSignin](#browsersignin) отключена, данная политика не будет действовать.

Если данная политика включена и для нее выбран вариант 'SignInAndMakeDomainAccountNonRemovable', в Microsoft Edge будет автоматически выполняться вход в учетные записи Active Directory на компьютерах, присоединенных к домену.

Если для этого параметра задано значение 'Disabled' или эта политика не настроена, в Microsoft Edge не будет автоматически выполняться вход в учетные записи Active Directory на компьютерах, присоединенных к домену.

Сопоставление параметров политики:

* Disabled (0) = Отключено

* SignInAndMakeDomainAccountNonRemovable (1) = Вход и запрет на удаление учетной записи домена

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ConfigureOnPremisesAccountAutoSignIn
  - Имя групповой политики: Настройка автоматического входа с использованием учетной записи домена Active Directory при отсутствии учетной записи домена Azure AD
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ConfigureOnPremisesAccountAutoSignIn
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  

  [В начало](#microsoft-edge:-политики)

  ### ConfigureOnlineTextToSpeech
  #### Настройка преобразования текста в речь в сети
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Этот параметр политики позволяет указать, можно ли в браузере использовать голоса веб-службы преобразования текста в речь (в рамках Azure Cognitive Services). Эти голоса имеют более высокое качество, чем предустановленные в системе голоса.

Если этот параметр политики включен или не настроен, веб-приложения, использующие API SpeechSynthesis, могут использовать голоса веб-службы преобразования текста в речь.

Если этот параметр политики выключен, такие голоса недоступны.

Ниже указано, где можно узнать больше об этой функции.
API SpeechSynthesis: [https://go.microsoft.com/fwlink/?linkid=2110038](https://go.microsoft.com/fwlink/?linkid=2110038)
Службы Cognitive Services: [https://go.microsoft.com/fwlink/?linkid=2110141](https://go.microsoft.com/fwlink/?linkid=2110141)

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ConfigureOnlineTextToSpeech
  - Имя групповой политики: Настройка преобразования текста в речь в сети
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ConfigureOnlineTextToSpeech
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ConfigureOnlineTextToSpeech
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ConfigureShare
  #### Настроить функцию предоставления общего доступа
  
  
  #### Поддерживаемые версии:
  - На Windows с 83 или более поздней версии

  #### Описание
  Если для этой политики задано значение 'ShareAllowed (по умолчанию), пользователи смогут получать доступ к функции общего доступа Windows 10 из меню "Настройки" и "Дополнительно" в Microsoft Edge, чтобы предоставить общий доступ другим приложениям в системе.

Если присвоить этому параметру политики значение 'ShareDisallowed', пользователи не смогут получить доступ к функции "Общий доступ к Windows 10". Если кнопка "Поделиться" находится на панели инструментов, она также будет скрыта.

Сопоставление параметров политики:

* ShareAllowed (0) = Разрешить использование функции общего доступа

* ShareDisallowed (1) = Запретить использование функции общего доступа

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ConfigureShare
  - Имя групповой политики: Настроить функцию предоставления общего доступа
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ConfigureShare
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  

  [В начало](#microsoft-edge:-политики)

  ### CustomHelpLink
  #### Указание настраиваемой ссылки для справки
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 79 или более поздней версии

  #### Описание
  Указание ссылки на меню "Справка" или клавиши F1.

Если эта политика включена, администратор может указать ссылку на меню "Справка" или клавишу F1.

Если эта политика отключена или не настроена, будет использоваться заданная по умолчанию ссылка на меню "Справка" или клавиша F1.

Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: CustomHelpLink
  - Имя групповой политики: Указание настраиваемой ссылки для справки
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: CustomHelpLink
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"https://go.microsoft.com/fwlink/?linkid=2080734"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: CustomHelpLink
  - Пример значения:
``` xml
<string>https://go.microsoft.com/fwlink/?linkid=2080734</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DNSInterceptionChecksEnabled
  #### Проверки перехвата DNS включены
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 80 или более поздней версии

  #### Описание
  Эта политика настраивает локальный переключатель, который можно использовать для отключения проверок перехвата DNS. Эти проверки пытаются обнаружить, находится ли браузер за прокси-сервером, который перенаправляет неизвестные имена узлов.

Это обнаружение может быть не нужно в корпоративной среде, в которой известна конфигурация сети. Его можно отключить, чтобы избежать дополнительного трафика DNS и HTTP при запуске и каждом изменении конфигурации DNS.

Если этот параметр политики включен или не настроен, проверки перехвата DNS будут выполняться.

Если этот параметр политики отключен, проверки перехвата DNS не будут выполняться.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DNSInterceptionChecksEnabled
  - Имя групповой политики: Проверки перехвата DNS включены
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DNSInterceptionChecksEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DNSInterceptionChecksEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultBrowserSettingEnabled
  #### Назначить Microsoft Edge стандартным браузером
  
  
  #### Поддерживаемые версии:
  - На Windows 7 и macOS с 77 или более поздней версии

  #### Описание
  Когда для этой политики задан параметр "Истина", Microsoft Edge при запуске всегда проверяет, является ли он браузером по умолчанию, и, если возможно, автоматически регистрирует себя.

Если этой политике задан параметр "Ложь", Microsoft Edge не проверяет, используется ли он по умолчанию, и выключает управление этим параметром со стороны пользователя.

Если эта политика не установлена, Microsoft Edge позволяет пользователю контролировать, используется ли он по умолчанию, и если это не так, то для пользователя выводится сообщение.

Примечание для администраторов Windows. Эта политика работает только на компьютерах с Windows 7. Для более поздних версий Windows необходимо развернуть файл "сопоставления приложений по умолчанию", который назначает Microsoft Edge обработчиком протоколов https и http (и, дополнительно, протокола ftp и таких форматов файлов, как .html, .htm, .pdf, .svg и .webp). Подробнее см. на странице [https://go.microsoft.com/fwlink/?linkid=2094932](https://go.microsoft.com/fwlink/?linkid=2094932).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultBrowserSettingEnabled
  - Имя групповой политики: Назначить Microsoft Edge стандартным браузером
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DefaultBrowserSettingEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultBrowserSettingEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultSearchProviderContextMenuAccessAllowed
  #### Разрешить поиск в контекстном меню службы поиска по умолчанию
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 85 или более поздней версии

  #### Описание
  Позволяет использовать службу поиска по умолчанию в контекстном меню.

Если отключить этот параметр политики, элемент поиска в контекстном меню, который использует службу поиска по умолчанию и поиск на боковой панели, будет недоступен.

Если включить этот параметр политики или не настроить его, элемент контекстного меню для службы поиска по умолчанию и поиска на боковой панели будет доступен.

Значение политики применяется, только когда политика [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) включена.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultSearchProviderContextMenuAccessAllowed
  - Имя групповой политики: Разрешить поиск в контекстном меню службы поиска по умолчанию
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DefaultSearchProviderContextMenuAccessAllowed
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultSearchProviderContextMenuAccessAllowed
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultSensorsSetting
  #### Default sensors setting
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 86 или более поздней версии

  #### Описание
  Set whether websites can access and use sensors such as motion and light sensors. You can completely block or allow websites to get access to sensors.

Setting the policy to 1 lets websites access and use sensors. Setting the policy to 2 denies acess to sensors.

You can override this policy for specific URL patterns by using the [SensorsAllowedForUrls](#sensorsallowedforurls) and [SensorsBlockedForUrls](#sensorsblockedforurls) policies.

If you don't configure this policy, websites can access and use sensors, and users can change this setting. This is the global default for [SensorsAllowedForUrls](#sensorsallowedforurls) and [SensorsBlockedForUrls](#sensorsblockedforurls).

Сопоставление параметров политики:

* AllowSensors (1) = Allow sites to access sensors

* BlockSensors (2) = Do not allow any site to access sensors

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultSensorsSetting
  - Имя групповой политики: Default sensors setting
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DefaultSensorsSetting
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000002
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultSensorsSetting
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DefaultSerialGuardSetting
  #### Управлять использованием API Serial
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 86 или более поздней версии

  #### Описание
  Укажите, могут ли сайты получать доступ к последовательным портам. Вы можете либо полностью заблокировать доступ, либо каждый раз запрашивать у пользователя разрешение, когда веб-сайт пытается получить доступ к последовательному порту.

Присвоение этой политике значения "3" позволяет веб-сайтам запрашивать доступ к последовательным портам. Присвоение этой политике значения "2" запрещает доступ к последовательным портам.

Вы можете переопределить эту политику для конкретных шаблонов URL-адресов с помощью политик [SerialAskForUrls](#serialaskforurls) и [SerialBlockedForUrls](#serialblockedforurls).

Если эта политика не настроена, по умолчанию сайты могут запрашивать у пользователя доступ к последовательному порту, при этом пользователи могут изменить эту настройку.

Сопоставление параметров политики:

* BlockSerial (2) = Запретить всем сайтам запрашивать доступ к последовательным портам через API Serial

* AskSerial (3) = Разрешить сайтам запрашивать разрешение пользователя на доступ к последовательному порту

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DefaultSerialGuardSetting
  - Имя групповой политики: Управлять использованием API Serial
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DefaultSerialGuardSetting
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000002
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DefaultSerialGuardSetting
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DelayNavigationsForInitialSiteListDownload
  #### Требуется доступность списка сайтов в режиме предприятия перед переходом на вкладку
  
  
  #### Поддерживаемые версии:
  - На Windows с 84 или более поздней версии

  #### Описание
  Позволяет вам указать, выполняется ли ожидание перехода по вкладкам Microsoft Edge до загрузки браузером исходного списка сайтов в режиме предприятия. Этот параметр предназначен для сценария, в котором начальная страница браузера должна загружать режим Internet Explorer, и важно выполнить это действие при первом запуске браузера после включения режима IE. Если этот сценарий не существует, рекомендуется не включать этот параметр, так как он может отрицательно повлиять на скорость загрузки начальной страницы. Параметр применяется только в том случае, если в Microsoft Edge отсутствует кэшированный список сайтов в режиме предприятия, например при первом запуске браузера после включения режима IE.

Этот параметр работает совместно с:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) с присвоенным значением 'IEMode'
и
политикой [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist), когда в списке есть хотя бы одна запись.

Поведение при истечении времени ожидания этой политики можно настроить с помощью политики [NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout).

Если вы присвоите этой политике значение 'All', когда у Microsoft Edge нет кэшированной версии списка сайтов в режиме предприятия, вкладки задерживают переход, пока браузер не скачает список сайтов. Сайты, настроенные на открытие в режиме Internet Explorer с помощью списка сайтов, загружаются в режиме Internet Explorer даже при исходной навигации браузера. Сайты, которые невозможно настроить на открытие в Internet Explorer, например сайты со схемой, отличной от http:, https:, file: или ftp:, не задерживают переход и загружаются сразу в режиме Microsoft Edge.

Если вы присвоите этой политике значение 'None' или не настроите ее, когда у Microsoft Edge нет кэшированной версии списка сайтов в режиме предприятия, переход по вкладкам выполняется сразу, без ожидания загрузки браузером списка сайтов в режиме предприятия. Сайты, настроенные на открытие в режиме Internet Explorer с помощью списка сайтов, открываются в режиме Microsoft Edge, пока браузер не завершит скачивание списка сайтов в режиме предприятия.

Сопоставление параметров политики:

* None (0) = Нет

* All (1) = Все допустимые переходы

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DelayNavigationsForInitialSiteListDownload
  - Имя групповой политики: Требуется доступность списка сайтов в режиме предприятия перед переходом на вкладку
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DelayNavigationsForInitialSiteListDownload
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  

  [В начало](#microsoft-edge:-политики)

  ### DeleteDataOnMigration
  #### Удалить старые данные браузера при переносе
  
  
  #### Поддерживаемые версии:
  - На Windows с 83 или более поздней версии

  #### Описание
  Эта политика управляет удалением пользовательских данных браузера из устаревшей версии Microsoft Edge после перехода на Microsoft Edge версии 81 или более поздней.

Если установить для этой политики параметр "Включено", все данные браузера из устаревшей версии Microsoft Edge будут удалены после перехода на Microsoft Edge версии 81 или более поздней. Эту политику необходимо настроить до перехода на Microsoft Edge версии 81 или более поздней, иначе политика не повлияет на существующие данные браузера.

Если установить для этой политики параметр "Отключено" или не настраивать эту политику, пользовательские данные браузера не будут удалены после перехода на Microsoft Edge версии 83 или более поздней.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DeleteDataOnMigration
  - Имя групповой политики: Удалить старые данные браузера при переносе
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DeleteDataOnMigration
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  

  [В начало](#microsoft-edge:-политики)

  ### DeveloperToolsAvailability
  #### Определение места использования средств разработчика
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определяет место, в котором можно использовать средства разработчика.

Если задать этому параметру политики значение 'DeveloperToolsDisallowedForForceInstalledExtensions' (по умолчанию), пользователи смогут получать доступ к средствам разработчика и консоли JavaScript в общем, но не в контексте расширений, установленных политикой предприятия.

Если присвоить этому параметру политики значение 'DeveloperToolsAllowed', пользователи смогут получать доступ к средствам разработчика и консоли JavaScript во всех контекстах, включая расширения, установленные политикой предприятия.

Если присвоить этому параметру политики значение 'DeveloperToolsDisallowed', пользователи не смогут получать доступ к средствам разработчика или проверять элементы веб-сайтов. Сочетания клавиш и пункты меню или контекстных меню, которые открывают средства разработчика, или консоль JavaScript будут отключены.

Сопоставление параметров политики:

* DeveloperToolsDisallowedForForceInstalledExtensions (0) = Блокировать средства разработчика в расширениях, установленных политикой предприятия, разрешать в других контекстах

* DeveloperToolsAllowed (1) = Разрешить использование средств разработчика

* DeveloperToolsDisallowed (2) = Запретить использование средств разработчика

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DeveloperToolsAvailability
  - Имя групповой политики: Определение места использования средств разработчика
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DeveloperToolsAvailability
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000002
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DeveloperToolsAvailability
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DiagnosticData
  #### Отправлять обязательные и необязательные диагностические данные об использовании браузера
  
  
  #### Поддерживаемые версии:
  - На Windows 7 и macOS с 86 или более поздней версии

  #### Описание
  Эта политика управляет отправкой обязательных и необязательных диагностических данных об использовании браузера в Майкрософт.

Обязательные диагностические данные собираются для защиты, обеспечения актуальности и правильной работы Microsoft Edge.

Необязательные диагностические данные включают данные об использовании браузера, посещаемых веб-сайтах, а также отчеты о сбоях, чтобы помочь в улучшении продуктов и служб Майкрософт.

Эта политика не поддерживается на устройствах с Windows 10. Чтобы управлять сбором этих данных в Windows 10, ИТ-администраторы должны использовать групповую политику диагностических данных Windows. Эта политика называется "Разрешить телеметрию" или "Разрешить диагностические данные" в зависимости от версии Windows. Подробнее о сборе диагностических данных Windows 10: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

Используйте один из следующих параметров для настройки этой политики:

"Off" — отключает сбор обязательных и необязательных диагностических данных. Не рекомендуется использовать этот параметр.

"RequiredData" — отправляет обязательные диагностические данные, но отключает сбор необязательных диагностических данных. Microsoft Edge отправляет обязательные диагностические данные для защиты, обеспечения актуальности и правильной работы Microsoft Edge.

"OptionalData" — отправляет необязательные диагностические данные, включающие данные об использовании браузера, посещенных веб-сайтах, отчеты о сбоях, для улучшения продуктов и служб Майкрософт.

В Windows 7/macOS эта политика управляет отправкой обязательных и необязательных данных в Майкрософт.

Если эта политика не настроена или отключена, Microsoft Edge будет по умолчанию использовать параметры пользователя.

Сопоставление параметров политики:

* Off (0) = Отключено (не рекомендуется)

* RequiredData (1) = Обязательные данные

* OptionalData (2) = Необязательные данные

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DiagnosticData
  - Имя групповой политики: Отправлять обязательные и необязательные диагностические данные об использовании браузера
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DiagnosticData
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000002
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DiagnosticData
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DirectInvokeEnabled
  #### Разрешить пользователям открыть файлы с помощью протокола DirectInvoke
  
  
  #### Поддерживаемые версии:
  - На Windows с 78 или более поздней версии

  #### Описание
  Разрешить пользователям открыть файлы с помощью протокола DirectInvoke. Протокол DirectInvoke позволяет веб-сайтам запрашивать открытие файлов в браузере с определенного URL-адреса с помощью специального обработчика файлов на компьютере или другом устройстве пользователя.

Если этот параметр политики включен или не настроен, пользователи могут открыть файлы с помощью протокола DirectInvoke.

Если данный параметр политики отключен, пользователи не могут открыть файлы с помощью протокола DirectInvoke. В этом случае файл сохраняется в файловой системе.

Примечание. Запрет DirectInvoke может привести к неправильной работе некоторых компонентов Microsoft Office SharePoint Online.

Дополнительные сведения о DirectInvoke см. на страницах [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) и [https://go.microsoft.com/fwlink/?linkid=2099871](https://go.microsoft.com/fwlink/?linkid=2099871).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DirectInvokeEnabled
  - Имя групповой политики: Разрешить пользователям открыть файлы с помощью протокола DirectInvoke
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DirectInvokeEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  

  [В начало](#microsoft-edge:-политики)

  ### Disable3DAPIs
  #### Отключить поддержку API трехмерной графики
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Запрет доступа веб-страниц к графическому процессору (GPU), а именно: веб-страницы не могут получать доступ к API WebGL, а подключаемые модули не могут использовать API Pepper 3D.

Если не настроить или отключить эту политику, веб-страницы потенциально могут использовать API WebGL, а подключаемые модули — API Pepper 3D. Возможно, в Microsoft Edge по умолчанию по-прежнему будет требоваться передача аргументов командной строки для использования этих API.

Если политике [HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled) присвоено значение false, настройка Disable3DAPIs не учитывается — как и при присвоении настройке Disable3DAPIs значения true.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: Disable3DAPIs
  - Имя групповой политики: Отключить поддержку API трехмерной графики
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: Disable3DAPIs
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: Disable3DAPIs
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DisableScreenshots
  #### Отключить создание снимков экрана
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определяет, могут ли пользователи делать снимки экрана страницы браузера.

Если этот параметр включен, пользователь не может делать снимки экрана с помощью сочетания клавиш или API расширения.

Если отключить или не настроить этот параметр политики, пользователи смогут делать снимки экрана.

Обратите внимание, что этот параметр политики управляет снимками экрана, которые делаются из самого браузера. Даже если данный параметр политики включен, пользователи по-прежнему смогут делать снимки экрана с помощью любого метода вне браузера (например, с помощью функции операционной системы или другого приложения).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DisableScreenshots
  - Имя групповой политики: Отключить создание снимков экрана
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DisableScreenshots
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DisableScreenshots
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DiskCacheDir
  #### Задать каталог кэша на диске
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Выбор каталога для сохранения кэшированных файлов.

Если включить этот параметр политики, Microsoft Edge будет использовать заданный каталог независимо от того, указал ли пользователь флаг "--disk-cache-dir". Чтобы избежать потери данных или других непредвиденных ошибок, не задавайте в этом параметре политики корневой каталог тома или каталог, который используется для других целей, так как Microsoft Edge управляет его содержимым.

Список переменных, которые можно использовать при определении каталогов и путей, см. на странице [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

Если не настроить этот параметр политики, будет использоваться стандартный каталог кэша и пользователь сможет переопределить это стандартное значение с помощью флага командной строки "--disk-cache-dir".

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DiskCacheDir
  - Имя групповой политики: Задать каталог кэша на диске
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DiskCacheDir
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"${user_home}/Edge_cache"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DiskCacheDir
  - Пример значения:
``` xml
<string>${user_home}/Edge_cache</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DiskCacheSize
  #### Задать размер кэша диска (в байтах)
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определение размера кэша (в байтах) для хранения файлов на диске.

Если этот параметр политики включен, в Microsoft Edge используется указанный размер кэша независимо от того, указал ли пользователь флаг "--disk-cache-size". Указанное в этом параметре значение является не жестким, а скорее рекомендованным ограничением для системы кэширования. Любое значение меньше нескольких мегабайт считается слишком маленьким и будет округлено до разумного минимума.

Если для данного параметра политики выбрано значение 0, используется стандартный размер кэша и пользователи не могут изменить эту настройку.

Если не настроить этот параметр политики, используется стандартный размер, но пользователи могут изменить его с помощью флага "--disk-cache-size".

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DiskCacheSize
  - Имя групповой политики: Задать размер кэша диска (в байтах)
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DiskCacheSize
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x06400000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DiskCacheSize
  - Пример значения:
``` xml
<integer>104857600</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DnsOverHttpsMode
  #### Управление режимом DNS через HTTPS
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 83 или более поздней версии

  #### Описание
  Управление режимом сопоставителя DNS через HTTPS. Обратите внимание, что эта политика только устанавливает режим по умолчанию для каждого запроса. Режим может быть переопределен для определенных типов запросов, например запросов на сопоставление имени узла сервера DNS через HTTPS.

В режиме "off" DNS через HTTPS отключается.

В режиме "automatic" сначала отправляются запросы DNS через HTTPS, если сервер DNS через HTTPS доступен, но в случае ошибок могут отправляться небезопасные запросы.

В режиме "secure" отправляются только запросы DNS через HTTPS, а в случае ошибок сопоставление не будет выполнено.

Если не настроить эту политику, браузер может отправлять запросы DNS через HTTPS сопоставителю, связанному с системным сопоставителем, который настроен пользователем.

Сопоставление параметров политики:

* off (off) = Отключить DNS через HTTPS

* automatic (automatic) = Включить DNS через HTTPS с небезопасным резервным переходом

* secure (secure) = Включить DNS через HTTPS без небезопасного резервного перехода

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DnsOverHttpsMode
  - Имя групповой политики: Управление режимом DNS через HTTPS
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DnsOverHttpsMode
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"off"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DnsOverHttpsMode
  - Пример значения:
``` xml
<string>off</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DnsOverHttpsTemplates
  #### Укажите шаблон URI для нужного сопоставителя DNS поверх HTTPS
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 83 или более поздней версии

  #### Описание
  Шаблон URI нужного сопоставителя DNS через HTTPS. Чтобы указать несколько сопоставителей DNS через HTTPS, разделите соответствующие шаблоны URI пробелами.

Если установить для [DnsOverHttpsMode](#dnsoverhttpsmode) значение "secure", эта политика должна быть настроена и не может быть пустой.

Если установить для [DnsOverHttpsMode](#dnsoverhttpsmode) значение "automatic" и настроить эту политику, будут использоваться указанные шаблоны URI. Если не настраивать эту политику, будут использованы жестко заданные сопоставления, чтобы попытаться обновить текущий сопоставитель DNS пользователя до сопоставителя DNS через HTTPS этого же поставщика.

Если шаблон URI содержит переменную dns, запросы к сопоставителю будут использовать GET; в противном случае запросы будут использовать POST.

Шаблоны с неверным форматом будут пропущены.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DnsOverHttpsTemplates
  - Имя групповой политики: Укажите шаблон URI для нужного сопоставителя DNS поверх HTTPS
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: DnsOverHttpsTemplates
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"https://dns.example.net/dns-query{?dns}"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DnsOverHttpsTemplates
  - Пример значения:
``` xml
<string>https://dns.example.net/dns-query{?dns}</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DownloadDirectory
  #### Настроить каталог загрузки
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определение каталога для загрузки файлов.

Если включить эту политику, Microsoft Edge будет использовать заданный каталог независимо от того, указал пользователь такой каталог или настроил вывод запроса о расположении при каждой загрузке. Список переменных, которые можно использовать, см. на странице [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

Если отключить или не настроить эту политику, будет использоваться стандартный каталог и пользователь сможет изменить его.

Если задан недопустимый путь, Microsoft Edge по умолчанию использует стандартный каталог для загрузки, указанный пользователем.

Если задан путь к несуществующей папке, при загрузке появляется сообщение с вопросом о том, хочет ли пользователь сохранить загружаемые файлы.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DownloadDirectory
  - Имя групповой политики: Настроить каталог загрузки
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: DownloadDirectory
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"\n      Linux-based OSes (including Mac): /home/${user_name}/Downloads\n      Windows: C:\\Users\\${user_name}\\Downloads"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DownloadDirectory
  - Пример значения:
``` xml
<string>
      Linux-based OSes (including Mac): /home/${user_name}/Downloads
      Windows: C:\Users\${user_name}\Downloads</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### DownloadRestrictions
  #### Разрешить ограничения загрузки
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определение типа загрузок, которые Microsoft Edge полностью блокирует, без возможности для пользователей переопределять этот параметр безопасности.

Задайте значение 'BlockDangerousDownloads', чтобы разрешить все загрузки, кроме тех, которые сопровождаются предупреждениями фильтра SmartScreen в Microsoft Defender.

Задайте значение 'BlockPotentiallyDangerousDownloads', чтобы разрешить все загрузки, кроме тех, которые сопровождаются предупреждениями фильтра SmartScreen в Microsoft Defender о потенциально опасной или нежелательной загрузке.

Задайте значение 'BlockAllDownloads', чтобы блокировать все загрузки.

Если не настроить этот параметр политики или выбрать для него значение 'DefaultDownloadSecurity', загрузки будут подпадать под обычные защитные ограничения на основе результатов анализа фильтра SmartScreen в Microsoft Defender.

Обратите внимание: эти ограничения применяются при загрузках из содержимого веб-страницы, а также из пункта контекстного меню "ссылка для загрузки…". Эти ограничения не применяются при сохранении или загрузке страницы, отображаемой в данный момент, а также не применяются к пункту меню печати "Сохранить как PDF".

Дополнительные сведения о фильтре SmartScreen в Microsoft Defender см. на странице [https://go.microsoft.com/fwlink/?linkid=2094934](https://go.microsoft.com/fwlink/?linkid=2094934).

Сопоставление параметров политики:

* DefaultDownloadSecurity (0) = Нет специальных ограничений

* BlockDangerousDownloads (1) = Блокировать опасные загрузки

* BlockPotentiallyDangerousDownloads (2) = Блокировать потенциально опасные или нежелательные загрузки

* BlockAllDownloads (3) = Блокировать все загрузки

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: DownloadRestrictions
  - Имя групповой политики: Разрешить ограничения загрузки
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: DownloadRestrictions
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000002
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: DownloadRestrictions
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### EdgeCollectionsEnabled
  #### Включить функцию "Коллекции"
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 78 или более поздней версии

  #### Описание
  Настройка доступа к функции "Коллекции" для более эффективного сбора, упорядочивания, передачи и экспорта содержимого, в том числе с помощью встроенных инструментов Office.

Если включить или не настроить этот параметр политики, пользователи смогут получать доступ к функции "Коллекции" и использовать ее в Microsoft Edge.

Если данный параметр политики отключен, пользователи не могут получать доступ к функции "Коллекции" в Microsoft Edge.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: EdgeCollectionsEnabled
  - Имя групповой политики: Включить функцию "Коллекции"
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: EdgeCollectionsEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: EdgeCollectionsEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### EditFavoritesEnabled
  #### Позволяет пользователям редактировать "Избранное"
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Включите эту политику, чтобы разрешить пользователям добавлять, удалять и изменять избранное. Это поведение по умолчанию, если параметр политики не настроен.

Отключите эту политику, чтобы запретить пользователям добавлять, удалять или изменять избранное. Они по-прежнему смогут использовать существующее избранное.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: EditFavoritesEnabled
  - Имя групповой политики: Позволяет пользователям редактировать "Избранное"
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: EditFavoritesEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: EditFavoritesEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### EnableDeprecatedWebPlatformFeatures
  #### Повторно включить устаревшие функции веб-платформы на ограниченное время
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Укажите список устаревших функций веб-платформы, которые необходимо временно повторно включить.

Этот параметр политики позволяет повторно включить устаревшие функции веб-платформы на ограниченное время. Функции определяются тегом строки.

Если не настроить этот параметр политики, если список будет пустым или если функция не соответствует одному из поддерживаемых тегов строки, все устаревшие функции веб-платформы будут отключены.

Этот параметр политики поддерживается на вышеуказанных платформах, но функция, которую он включает, может быть недоступна на всех этих платформах. Не все устаревшие функции веб-платформы можно включить повторно. Только явно указанные ниже функции можно включить повторно и только на ограниченный период времени, который зависит от функции. Вы можете увидеть, как меняется назначение функции веб-платформы, на странице https://bit.ly/blinkintents.

Общий формат тега строки: [DeprecatedFeatureName]_EffectiveUntil[yyyymmdd].

Сопоставление параметров политики:

* ExampleDeprecatedFeature (ExampleDeprecatedFeature_EffectiveUntil20080902) = Включить API ExampleDeprecatedFeature до 02.09.2008

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: EnableDeprecatedWebPlatformFeatures
  - Имя групповой политики: Повторно включить устаревшие функции веб-платформы на ограниченное время
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures\1 = "ExampleDeprecatedFeature_EffectiveUntil20080902"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: EnableDeprecatedWebPlatformFeatures
  - Пример значения:
``` xml
<array>
  <string>ExampleDeprecatedFeature_EffectiveUntil20080902</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### EnableDomainActionsDownload
  #### Включить загрузку действий домена с серверов корпорации Майкрософт (устарела)
  
  >УСТАРЕВШАЯ: эта политика устарела. Она не действует в версиях Microsoft Edge, следующих за версией 84.
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 до 84

  #### Описание
  Эта политика не работает, так как следует избегать конфликтующих состояний. Она использовалась для включения и отключения загрузки списка действий домена, но не всегда достигала желаемого состояния. Служба "Эксперименты и конфигурация", которая обрабатывает загрузку, имеет собственную политику для настройки загружаемого содержимого из службы. Используйте вместо нее политику [ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol).

Действия домена в Microsoft Edge представляют собой ряд функций обеспечения совместимости, которые помогают браузеру правильно работать в Интернете.

Майкрософт сохраняет список действий, которые необходимо выполнить на некоторых доменах, в целях обеспечения совместимости. Например, браузер может переопределить строку "Агент пользователя" на веб-сайте, если этот веб-сайт не работает из-за новой строки "Агент пользователя" в Microsoft Edge. Каждое из этих действий применяется в течение ограниченного времени, пока Майкрософт пытается устранить проблему с владельцем сайта.

При запуске и периодически после него браузер будет подключаться к службе "Эксперименты и конфигурация", которая содержит наиболее актуальный список необходимых действий для обеспечения совместимости. Этот список сохраняется локально после первого получения, и последующие запросы только обновляют его, если серверная копия изменяется.

Если этот параметр политики включен, список действий домена и дальше будет загружаться из службы "Эксперименты и конфигурация".

Если этот параметр политики отключен, список действий домена больше не будет загружаться из службы "Эксперименты и конфигурация".

Если не настроить этот параметр политики, список действий домена и дальше будет загружаться из службы "Эксперименты и конфигурация".

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: EnableDomainActionsDownload
  - Имя групповой политики: Включить загрузку действий домена с серверов корпорации Майкрософт (устарела)
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: EnableDomainActionsDownload
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: EnableDomainActionsDownload
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### EnableOnlineRevocationChecks
  #### Включить проверки OCSP/CRL в сети
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Проверки отзыва через Интернет не обеспечивают существенного выигрыша в безопасности и по умолчанию отключены.

Если данный параметр политики включен, Microsoft Edge будет выполнять проверки OCSP/CRL через Интернет ("несерьезный сбой"). "Несерьезный сбой" означает, что если сервер отзыва сертификатов недоступен, сертификат считается действительным.

Если этот параметр политики отключен или не настроен, Microsoft Edge не будет выполнять проверки отзыва сертификатов через Интернет.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: EnableOnlineRevocationChecks
  - Имя групповой политики: Включить проверки OCSP/CRL в сети
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: EnableOnlineRevocationChecks
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: EnableOnlineRevocationChecks
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### EnableSha1ForLocalAnchors
  #### Разрешить сертификаты, подписанные с помощью алгоритма SHA-1, если они выданы локальными якорями доверия (не рекомендуется)
  >УСТАРЕЛО. Эта политика устарела. В настоящее время она поддерживается, но станет устаревшей в будущем выпуске.
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 85 или более поздней версии

  #### Описание
  Если этот параметр включен, Microsoft Edge допускает подключения, защищенные сертификатами, подписанными с использованием алгоритма SHA-1, если сертификат связан с локально установленным корневым сертификатом и действителен.

Обратите внимание: работа этой политики зависит от того, допускает ли стек проверки сертификатов операционной системы (ОС) алгоритм подписи SHA-1. Если при обновлении ОС изменится порядок обработки сертификатов SHA-1, эта политика может перестать работать.  Кроме того, эта политика предназначена для использования в качестве временного решения, предоставляющего компаниям больше времени на переход с SHA-1. Она будет удалена в браузере Microsoft Edge 92, который будет выпущен в середине 2021 года.

Если не настроить эту политику либо задать для нее значение false или если сертификат SHA-1 связан с общедоступным доверенным корневым сертификатом, Microsoft Edge не разрешит использовать сертификаты, подписанные с использованием алгоритма подписи SHA-1.

Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: EnableSha1ForLocalAnchors
  - Имя групповой политики: Разрешить сертификаты, подписанные с помощью алгоритма SHA-1, если они выданы локальными якорями доверия (не рекомендуется)
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: EnableSha1ForLocalAnchors
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: EnableSha1ForLocalAnchors
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### EnterpriseHardwarePlatformAPIEnabled
  #### Разрешить управляемым расширениям использовать API платформы оборудования предприятия
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 78 или более поздней версии

  #### Описание
  Если этот параметр политики включен, расширениям, установленным на основе корпоративной политики, разрешается использовать API платформы оборудования предприятия.
Если этот параметр политики отключен или не настроен, ни одному расширению не разрешается использовать API платформы оборудования предприятия.
Этот параметр политики также применяется для расширений компонентов.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: EnterpriseHardwarePlatformAPIEnabled
  - Имя групповой политики: Разрешить управляемым расширениям использовать API платформы оборудования предприятия
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: EnterpriseHardwarePlatformAPIEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: EnterpriseHardwarePlatformAPIEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### EnterpriseModeSiteListManagerAllowed
  #### Разрешить доступ к средству Enterprise Mode Site List Manager
  
  
  #### Поддерживаемые версии:
  - На Windows с 86 или более поздней версии

  #### Описание
  Позволяет указать, доступно ли средство Enterprise Mode Site List Manager для пользователей.

Если включить этот параметр политики, пользователи будут видеть кнопку навигации Enterprise Mode Site List Manager на странице edge://compat и смогут перейти к средству и воспользоваться им.

Если отключить этот параметр политики или не настроить его, пользователи не будут видеть кнопку навигации средства и не смогут воспользоваться им.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: EnterpriseModeSiteListManagerAllowed
  - Имя групповой политики: Разрешить доступ к средству Enterprise Mode Site List Manager
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: EnterpriseModeSiteListManagerAllowed
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  

  [В начало](#microsoft-edge:-политики)

  ### ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  #### Отключить предупреждения о загрузке на основе расширений типов файлов для указанных типов файлов в доменах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 85 или более поздней версии

  #### Описание
  Вы можете включить эту политику, чтобы создать словарь расширений типов файлов с соответствующим списком доменов, которые будут исключены из предупреждений о загрузке на основе расширений типов файлов. Это позволяет администраторам предприятия блокировать предупреждения о загрузке на основе расширений типов файлов для файлов, связанных с указанным доменом. Например, если расширение "jnlp" связано с "website1.com", пользователи не будут видеть предупреждение при загрузке файлов "jnlp" из "website1.com", но увидят его при загрузке файлов "jnlp" из "website2.com".

Для файлов с расширениями типов файлов, указанными для доменов, которые определяются этой политикой, также предоставляются предупреждения системы безопасности, не основанные на расширениях типов файлов, например предупреждения о загрузке смешанного контента и предупреждения фильтра SmartScreen в Microsoft Defender.

Если отключить этот параметр политики или не настроить его, то для типов файлов, которые активируют предупреждения о загрузке на основе расширений, предупреждения будут отображаться.

Если включить этот параметр политики:

* Шаблон URL-адреса должен быть отформатирован в соответствии с [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).
* Введенное расширение типа файла должно быть представлено символами ASCII нижнего регистра. Начальный разделитель не следует включать при указании расширения типа файла, т. е. вместо ".jnlp" нужно указать "jnlp".

Например:

Следующий пример значения блокирует предупреждения о загрузке на основе расширений типов файлов для расширений swf, exe и jnlp в доменах *.contoso.com. В любом другом домене для пользователя отображается предупреждение о загрузке на основе расширений типов файлов для файлов exe и jnlp, но не для swf.

[
{ "file_extension": "jnlp", "domains": ["contoso.com"] },
{ "file_extension": "exe", "domains": ["contoso.com"] },
{ "file_extension": "swf", "domains": ["*"] }
]

Обратите внимание, что в предшествующем примере показано подавление предупреждений на основе расширений типов файлов для файлов swf во всех доменах. Применение подавления таких предупреждений во всех доменах для любого опасного расширения типа файла не рекомендуется по соображениям безопасности. В примере просто показано наличие такой возможности.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Имя групповой политики: Отключить предупреждения о загрузке на основе расширений типов файлов для указанных типов файлов в доменах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\1 = {"domains": ["https://contoso.com", "contoso2.com"], "file_extension": "jnlp"}
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\2 = {"domains": ["*"], "file_extension": "swf"}

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - Пример значения:
``` xml
<array>
  <string>{'domains': ['https://contoso.com', 'contoso2.com'], 'file_extension': 'jnlp'}</string>
  <string>{'domains': ['*'], 'file_extension': 'swf'}</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ExperimentationAndConfigurationServiceControl
  #### Управление связью со службой "Эксперименты и конфигурация"
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  В Microsoft Edge для развертывания полезных данных экспериментов и конфигураций используется служба "Эксперименты и конфигурация".

Полезные данные экспериментов представляют собой список средств разработки, которые корпорация Майкрософт предоставляет для тестирования и обратной связи.

Полезные данные конфигурации представляют собой список настроек, которые Майкрософт хочет реализовать в Microsoft Edge для оптимизации взаимодействия с пользователем. Например, полезные данные конфигурации могут сообщать о том, как часто Microsoft Edge отправляет запросы в службу "Эксперименты и конфигурация" для получения последних полезных данных.

Кроме того, полезные данные конфигурации также могут содержать список действий, которые необходимо выполнить с определенными доменами по причинам совместимости. Например, браузер может переопределить строку "Агент пользователя" на веб-сайте, если этот веб-сайт не работает из-за новой строки "Агент пользователя" в Microsoft Edge. Каждое из этих действий применяется в течение ограниченного времени, пока Майкрософт пытается устранить проблему с владельцем сайта.

Если для этой политики задан режим 'FullMode', из службы "Эксперименты и конфигурация" загружаются все полезные данные, относящиеся как к экспериментам, так и к конфигурации.

Если для этой политики задан режим 'ConfigurationsOnlyMode', загружаются только полезные данные конфигурации.

Если для этой политики задан режим 'RestrictedMode', обмен данными со службой "Эксперименты и конфигурация" полностью прекращается.

Если не настроить эту политику, на управляемом устройстве в каналах Stable и Beta выполняется тот же сценарий, что и при режиме 'ConfigurationsOnlyMode'.

Если не настроить эту политику, на неуправляемом устройстве выполняется тот же сценарий, что и при режиме 'FullMode'.

Сопоставление параметров политики:

* FullMode (2) = Получать конфигурации и эксперименты

* ConfigurationsOnlyMode (1) = Получать только конфигурации

* RestrictedMode (0) = Отключить связь со службой "Эксперименты и конфигурация"

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ExperimentationAndConfigurationServiceControl
  - Имя групповой политики: Управление связью со службой "Эксперименты и конфигурация"
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ExperimentationAndConfigurationServiceControl
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000002
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ExperimentationAndConfigurationServiceControl
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ExternalProtocolDialogShowAlwaysOpenCheckbox
  #### Отображать флажок "Всегда открывать" в диалоговом окне внешнего протокола
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 79 или более поздней версии

  #### Описание
  Эта политика управляет отображением флажка «Всегда разрешать этому сайту открывать ссылки этого типа» во всех запросах на подтверждение запуска внешних протоколов. Она применяется только к ссылкам https://.

 Если включить эту политику, при появлении запроса на подтверждение внешнего протокола пользователь может выбрать «Всегда разрешать», чтобы пропустить все дальнейшие запросы на подтверждение этого протокола на этом сайте.

 Если отключить эту политику, флажок «Всегда разрешать» не будет отображаться. Пользователь будет получать запрос на подтверждение при каждом вызове внешнего протокола.

 Если не настроить эту политику в версиях Microsoft Edge до 83, флажок «Всегда разрешать» не будет отображаться. Пользователь будет получать запрос на подтверждение при каждом вызове внешнего протокола.

 Если не настроить эту политику в Microsoft Edge версии 83, управление настройкой отображения этого флажка будет доступно через флажок «Включить запоминание настроек запроса на подтверждение запуска протокола» на странице edge://flags

Начиная с Microsoft Edge версии 84, если не установить эту политику, то при появлении запроса на подтверждение внешнего протокола пользователь может выбрать «Всегда разрешать», чтобы пропустить все дальнейшие запросы на подтверждение этого протокола на этом сайте.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Имя групповой политики: Отображать флажок "Всегда открывать" в диалоговом окне внешнего протокола
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### FamilySafetySettingsEnabled
  #### Разрешить пользователям настраивать функцию Family Safety
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 83 или более поздней версии

  #### Описание
  Эта политика отключает и полностью скрывает страницу Family Safety в настройках. Переход на страницу edge://settings/familysafety также будет заблокирован. Страница Family Safety описывает функции, доступные для группы семьи и способы присоединиться к группе семьи. Дополнительные сведения о Family Safety: ([https://go.microsoft.com/fwlink/?linkid=2098432](https://go.microsoft.com/fwlink/?linkid=2098432)).

Если эта политика включена или не настроена, страница Family Safety будет отображаться.

Если эта политика отключена, страница Family Safety не будет отображаться.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: FamilySafetySettingsEnabled
  - Имя групповой политики: Разрешить пользователям настраивать функцию Family Safety
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: FamilySafetySettingsEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: FamilySafetySettingsEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### FavoritesBarEnabled
  #### Включить панель "Избранное"
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Включает или выключает панель избранного.

Если данный параметр политики включен, пользователи будут видеть панель избранного.

Если этот параметр политики отключен, пользователи не смогут видеть панель избранного.

Если этот параметр политики не настроен, пользователи смогут решить, использовать панель избранного или нет.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: FavoritesBarEnabled
  - Имя групповой политики: Включить панель "Избранное"
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: FavoritesBarEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: FavoritesBarEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ForceBingSafeSearch
  #### Принудительно применить функцию "Безопасный поиск Bing"
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Эта политика обеспечивает выполнение запросов веб-поиска в Bing с помощью функции "Безопасный поиск", которой задано определенное значение. Пользователи не могут изменить эту настройку.

Если задать этой политике значение 'BingSafeSearchNoRestrictionsMode', функция "Безопасного поиска" в Bing применяет значение bing.com.

Если задать этой политике значение 'BingSafeSearchModerateMode', для функции "Безопасный поиск" будет использоваться умеренное значение политики. Умеренное значение отфильтровывает из результатов поиска видео и изображения для взрослых, но не текст.

Если задать этой политике значение 'BingSafeSearchStrictMode', для функции "Безопасный поиск" будет использоваться строгое значение. Строгое значение отфильтровывает текст, изображения и видео для взрослых.

Если отключить или не настроить эту политику, функция "Безопасного поиска" в Bing не применяется принудительно, и пользователи могут задать этой настройке нужное им значение на bing.com.

Сопоставление параметров политики:

* BingSafeSearchNoRestrictionsMode (0) = Не задавать ограничения поиска в Bing

* BingSafeSearchModerateMode (1) = Настроить умеренные ограничения поиска в Bing

* BingSafeSearchStrictMode (2) = Настроить строгие ограничения поиска в Bing

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ForceBingSafeSearch
  - Имя групповой политики: Принудительно применить функцию "Безопасный поиск Bing"
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ForceBingSafeSearch
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ForceBingSafeSearch
  - Пример значения:
``` xml
<integer>0</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ForceCertificatePromptsOnMultipleMatches
  #### Укажите, должен ли Microsoft Edge автоматически выбирать сертификат при обнаружении нескольких совпадений сертификатов для сайта, настроенного с помощью политики "AutoSelectCertificateForUrls"
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 81 или более поздней версии

  #### Описание
  Включает или отключает для пользователей запрос на выбор сертификата, если доступно несколько сертификатов и для сайта настроена политика [AutoSelectCertificateForUrls](#autoselectcertificateforurls). Если не настроить политику [AutoSelectCertificateForUrls](#autoselectcertificateforurls) для сайта, для пользователей всегда будет отображаться запрос на выбор сертификата.

Если для этой политики задано значение True, Microsoft Edge будет отображать для пользователя запрос на выбор сертификата для сайтов в списке, определенном в политике [AutoSelectCertificateForUrls](#autoselectcertificateforurls), если и только если имеется больше одного сертификата.

Если для этой политики задано значение False или она не настроена, Microsoft Edge будет автоматически выбирать сертификат, даже если имеется несколько совпадений для сертификата. Для пользователя не будет отображаться запрос на выбор сертификата для сайтов в списке, определенном в политике [AutoSelectCertificateForUrls](#autoselectcertificateforurls).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ForceCertificatePromptsOnMultipleMatches
  - Имя групповой политики: Укажите, должен ли Microsoft Edge автоматически выбирать сертификат при обнаружении нескольких совпадений сертификатов для сайта, настроенного с помощью политики "AutoSelectCertificateForUrls"
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ForceCertificatePromptsOnMultipleMatches
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ForceCertificatePromptsOnMultipleMatches
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ForceEphemeralProfiles
  #### Разрешить использование временных профилей
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Этот параметр политики контролирует переключение профилей пользователя во временный режим. Временный профиль создается, когда начинается сеанс, и удаляется после его завершения, при этом он привязывается к исходному профилю пользователя.

Если данный параметр политики включен, профили работают во временном режиме. Это позволяет пользователям работать на собственных устройствах, не сохраняя на этих устройствах данные о просмотре веб-страниц. Если данный параметр политики включен как политика операционной системы (например, с помощью объекта групповой политики в Windows), он применяется к каждому профилю в системе.

Если этот параметр отключен или не настроен, пользователи работают в своих обычных профилях после входа в браузер.

Во временном режиме данные профиля сохраняются на диске только на время сеанса пользователя. Такие элементы, как журнал браузера, расширения и их данные, веб-данные (например, файлы cookie и веб-базы данных), не сохраняются после закрытия браузера. Это не мешает пользователю загружать данные на диск вручную, сохранять страницы или печатать их. Если пользователь включил синхронизацию, все данные будут оставаться в его синхронизируемой учетной записи, как и в случае с обычными профилями. Пользователи могут также использовать просмотр InPrivate во временном режиме, если вы не выключили эту функцию явным образом.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ForceEphemeralProfiles
  - Имя групповой политики: Разрешить использование временных профилей
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ForceEphemeralProfiles
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ForceEphemeralProfiles
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ForceGoogleSafeSearch
  #### Принудительно применить функцию "Безопасный поиск Google"
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Принудительно применяется активная функция "Безопасный поиск" для выполнения запросов в веб-поиске Google, и пользователям запрещается изменять эту настройку.

Если эта политика включена, функция "Безопасный поиск" в поиске Google всегда активна.

Если эта политика отключена или не настроена, функция "Безопасный поиск" в поиске Google не применяется принудительно.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ForceGoogleSafeSearch
  - Имя групповой политики: Принудительно применить функцию "Безопасный поиск Google"
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ForceGoogleSafeSearch
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ForceGoogleSafeSearch
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ForceLegacyDefaultReferrerPolicy
  #### Использовать стандартную политику источника ссылки "нет источника ссылки при понижении версии". (не рекомендуется)
  >УСТАРЕЛО. Эта политика устарела. В настоящее время она поддерживается, но станет устаревшей в будущем выпуске.
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 81 или более поздней версии

  #### Описание
  Применение этой политики не рекомендуется. Она предназначена для использования только в качестве краткосрочного механизма, чтобы дать предприятиям больше времени для обновления своего веб-контента, если окажется, что он несовместим с текущей политикой источника ссылки по умолчанию. Она не будет работать в Microsoft Edge версии 86.

 Политика источника ссылки по умолчанию в Microsoft Edge усиливается с ее нынешнего значения "no-referrer-when-downgrade" до более безопасного "strict-origin-when-cross-origin" путем постепенного развертывания.

До развертывания эта политика предприятия не будет иметь никакого действия. После развертывания, когда эта политика предприятия включена, для политики источника ссылки Microsoft Edge по умолчанию будет установлено прежнее значение.

Эта политика предприятия по умолчанию отключена.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ForceLegacyDefaultReferrerPolicy
  - Имя групповой политики: Использовать стандартную политику источника ссылки "нет источника ссылки при понижении версии". (не рекомендуется)
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ForceLegacyDefaultReferrerPolicy
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ForceLegacyDefaultReferrerPolicy
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ForceNetworkInProcess
  #### Принудительно выполнять сетевой код в процессе браузера (устарела)
  
  >УСТАРЕВШАЯ: эта политика устарела. Она не действует в версиях Microsoft Edge, следующих за версией 83.
  #### Поддерживаемые версии:
  - На Windows с 78 до 83

  #### Описание
  Эта политика не работает, так как она была предназначена только для краткосрочного механизма, чтобы дать предприятиям больше времени для перехода на стороннее программное обеспечение, не зависящее от перехвата сетевых API. Рекомендуются прокси-серверы поверх LSP и патчей Win32 API.

Эта политика заставляет сетевой код запускаться в процессе браузера.

Эта политика по умолчанию отключена. Если она включена, пользователи уязвимы для проблем безопасности, когда сетевой процесс изолирован.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ForceNetworkInProcess
  - Имя групповой политики: Принудительно выполнять сетевой код в процессе браузера (устарела)
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ForceNetworkInProcess
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  

  [В начало](#microsoft-edge:-политики)

  ### ForceSync
  #### Force synchronization of browser data and do not show the sync consent prompt
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 86 или более поздней версии

  #### Описание
  Forces data synchronization in Microsoft Edge. This policy also prevents the user from turning sync off.

If you don't configure this policy, users will be able to turn sync on or off. If you enable this policy, users will not be able to turn sync off.

For this policy to work as intended,
[BrowserSignin](#browsersignin) policy must not be configured, or must be set to enabled. If [ForceSync](#forcesync) is set to disabled, then [BrowserSignin](#browsersignin) will not take affect.

[SyncDisabled](#syncdisabled) must not be configured or must be set to False. If this is set to True, [ForceSync](#forcesync) will not take affect.

0 = Do not automatically start sync and show the sync consent (default)
1 = Force sync to be turned on for Azure AD/Azure AD-Degraded user profile and do not show the sync consent prompt

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ForceSync
  - Имя групповой политики: Force synchronization of browser data and do not show the sync consent prompt
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ForceSync
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ForceSync
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ForceYouTubeRestrict
  #### Принудительное применение минимального режима ограниченного доступа на YouTube
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Принудительно применяет минимальный режим ограниченного доступа на YouTube и запрещает пользователям выбор менее ограниченного режима.

Задайте значение 'Strict', чтобы принудительно применить режим строгого ограничения доступа на YouTube.

Задайте значение 'Moderate', чтобы принудительно применить к пользователю режим умеренного ограничения доступа и режим строгого ограничения доступа на YouTube. Пользователи не смогут отключить ограниченный режим.

Задайте значение 'Off' или не настраивайте эту политику, чтобы не применять принудительно режим ограничения на YouTube. Внешние политики (например, политики YouTube) по-прежнему могут принудительно применять режим ограниченного доступа.

Сопоставление параметров политики:

* Off (0) = Не применять принудительно режим ограниченного доступа на YouTube

* Moderate (1) = Применять принудительно минимум режим умеренного ограничения доступа на YouTube

* Strict (2) = Принудительно применять режим строгого ограничения доступа для YouTube

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ForceYouTubeRestrict
  - Имя групповой политики: Принудительное применение минимального режима ограниченного доступа на YouTube
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ForceYouTubeRestrict
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ForceYouTubeRestrict
  - Пример значения:
``` xml
<integer>0</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### FullscreenAllowed
  #### Разрешить работу в полноэкранном режиме
  
  
  #### Поддерживаемые версии:
  - На Windows с 77 или более поздней версии

  #### Описание
  Доступ к полноэкранному режиму, при котором скрываются все пользовательские элементы интерфейса Microsoft Edge и отображается только веб-содержимое.

Если этот параметр политики включен или не настроен, пользователи, приложения и расширения с соответствующими разрешениями могут включать полноэкранный режим.

Если этот параметр политики отключен, пользователи, приложения и расширения не могут включать полноэкранный режим.

Когда доступ к полноэкранному режиму отключен, Microsoft Edge нельзя открыть в режиме киоска с помощью командной строки.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: FullscreenAllowed
  - Имя групповой политики: Разрешить работу в полноэкранном режиме
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: FullscreenAllowed
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  

  [В начало](#microsoft-edge:-политики)

  ### GloballyScopeHTTPAuthCacheEnabled
  #### Включить кэш проверки подлинности HTTP глобальной области
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 81 или более поздней версии

  #### Описание
  Настройка одного глобального кэша для каждого профиля с учетными данными проверки подлинности HTTP.

Если отключить или не настроить этот параметр политики, браузер будет использовать стандартное поведение межсайтовой проверки подлинности, которое на момент версии 80 состоит в том, чтобы определить диапазон учетных данных проверки подлинности сервера HTTP сайтом верхнего уровня. Таким образом, если два сайта используют ресурсы из одного домена проверки подлинности, учетные данные должны предоставляться независимо в контексте обоих сайтов. Кэшированные учетные данные прокси-сервера будут повторно использоваться на разных сайтах.

Если включить этот параметр политики, учетные данные проверки подлинности HTTP, введенные в контекст одного сайта, будут автоматически использованы в контексте другого сайта.

При включении этого параметра политики сайты остаются открытыми для некоторых типов межсайтовых атак. Он также позволяет отследить пользователей на сайтах даже без использования файлов cookie, путем добавления записей в кэш проверки подлинности HTTP с помощью учетных данных, встроенных в URL-адреса.

Цель этой политики — дать возможность организациям, зависящим от устаревшего поведения, шанс обновить свои процедуры входа. Эта политика в будущем будет удалена.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: GloballyScopeHTTPAuthCacheEnabled
  - Имя групповой политики: Включить кэш проверки подлинности HTTP глобальной области
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: GloballyScopeHTTPAuthCacheEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: GloballyScopeHTTPAuthCacheEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### GoToIntranetSiteForSingleWordEntryInAddressBar
  #### При вводе одного слова в адресной строке не выполнять поиск, а перенаправлять пользователя на сайт интрасети.
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 78 или более поздней версии

  #### Описание
  Когда данный параметр политики включен и в адресной строке вводится одно слово без знаков препинания, первый из автоматически предлагаемых вариантов в адресной строке направляет пользователя на сайты интрасети.

По умолчанию при вводе одного слова без знаков препинания выполняется переход на сайт интрасети, соответствующий введенному тексту.

Когда этот параметр включен, второй из автоматически предлагаемых вариантов в адресной строке запускает поиск в Интернете в точном соответствии с введенным текстовым запросом, если этот запрос представляет собой одно слово без знаков препинания. Если параллельно не включен параметр, запрещающий поиск в Интернете, используется стандартная служба поиска.

Включение данного параметра политики приводит к следующим двум результатам.

 В ответ на поисковый запрос в виде одного слова (который в обычной ситуации был бы сопоставлен с одним из элементов журнала) больше не будет выполняться переход к сайтам. Вместо этого браузер будет пытаться перейти к внутренним сайтам, которых может не быть в интрасети организации. В этом случае будет возникать ошибка 404.

Для правильного поиска по популярным поисковым запросам в виде одного слова необходимо будет вручную выбирать один из автоматически предлагаемых вариантов.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Имя групповой политики: При вводе одного слова в адресной строке не выполнять поиск, а перенаправлять пользователя на сайт интрасети.
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: GoToIntranetSiteForSingleWordEntryInAddressBar
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### HSTSPolicyBypassList
  #### Настройка списка имен, которые будут обходить проверку политики HSTS
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 79 или более поздней версии

  #### Описание
  Имена узлов, указанные в этом списке, будут исключены из проверки политики HSTS, применение которой может повышать запросы с "http://" на "https://". В этой политике допускается применение только однокомпонентных имен узлов. Имена узлов должны быть каноническими. Любые IDN должны быть преобразованы в формат A-Label, а все буквы в формате ASCII должны быть строчными. Эта политика применяется только к указанным именам узлов и не применяется к поддоменам имен в списке.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: HSTSPolicyBypassList
  - Имя групповой политики: Настройка списка имен, которые будут обходить проверку политики HSTS
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList\1 = "meet"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: HSTSPolicyBypassList
  - Пример значения:
``` xml
<array>
  <string>meet</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### HardwareAccelerationModeEnabled
  #### Использовать аппаратное ускорение, если доступно
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Настройте использование аппаратного ускорения, если оно доступно. Если этот параметр политики включен или не настроен, аппаратное ускорение будет включено, если функция графического процессора не заблокирована явным образом.

Если этот параметр политики отключен, аппаратное ускорение будет отключено.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: HardwareAccelerationModeEnabled
  - Имя групповой политики: Использовать аппаратное ускорение, если доступно
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: HardwareAccelerationModeEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: HardwareAccelerationModeEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### HideFirstRunExperience
  #### Скрыть интерфейс первого запуска и экран-заставку
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 80 или более поздней версии

  #### Описание
  Если эта политика включена, интерфейс первого запуска и экран-заставка не будут отображаться пользователям при запуске Microsoft Edge первый раз.

Для настроек конфигурации, отображаемых в интерфейсе первого запуска, браузер присвоит следующие стандартные значения:

-На странице новой вкладки, тип веб канала – MSN Новости, макет – "Для вдохновения".

-Для пользователя по-прежнему будет выполняться автоматический вход в Microsoft Edge, если учетная запись Windows принадлежит типу Azure AD или MSA.

-Синхронизация не будет включена по умолчанию, и пользователи будут иметь возможность включить синхронизацию в соответствующих настройках.

Если эта политика отключена или не настроена, интерфейс первого запуска и экран-заставка будут отображаться.

Примечание. Определенными настройками конфигурации, которые отображаются для пользователя во время первого запуска, также можно управлять с помощью других специальных политик. Вы можете использовать политику HideFirstRunExperience в комбинации с этими политиками, чтобы настроить определенный интерфейс браузера на своих управляемых устройствах. Некоторые другие политики:

-[AutoImportAtFirstRun](#autoimportatfirstrun)

-[NewTabPageLocation](#newtabpagelocation)

-[NewTabPageSetFeedType](#newtabpagesetfeedtype)

-[SyncDisabled](#syncdisabled)

-[BrowserSignin](#browsersignin)

-[NonRemovableProfileEnabled](#nonremovableprofileenabled)

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: HideFirstRunExperience
  - Имя групповой политики: Скрыть интерфейс первого запуска и экран-заставку
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: HideFirstRunExperience
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: HideFirstRunExperience
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ImportAutofillFormData
  #### Разрешить импорт данных автозаполнения формы
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Разрешает пользователям импортировать данные автозаполнения форм из другого браузера в Microsoft Edge.

Если включить эту политику, автоматически устанавливается флажок импорта данных автозаполнения вручную.

Если отключить эту политику, данные автозаполнения не импортируются при первом запуске, а пользователи не могут выбрать импорт этих данных вручную в дальнейших сеансах использования браузера.

Если не настраивать эту политику, данные автозаполнения импортируются при первом запуске, а пользователи могут выбрать импорт этих данных вручную в дальнейших сеансах использования браузера.

Также можно включить эту политику в качестве рекомендации. Это означает, что Microsoft Edge импортирует данные автозаполнения при первом запуске, но пользователи могут установить или снять флажок **данные автозаполнения** при импорте вручную.

**Примечание**. Эта политика в настоящее время управляет импортом из браузеров Google Chrome (в Windows 7, 8, 10 и macOS) и Mozilla Firefox (в Windows 7, 8, 10 и macOS).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ImportAutofillFormData
  - Имя групповой политики: Разрешить импорт данных автозаполнения формы
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: ImportAutofillFormData
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ImportAutofillFormData
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ImportBrowserSettings
  #### Разрешить импорт настроек браузера
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 78 или более поздней версии

  #### Описание
  Импорт настроек браузера в Microsoft Edge из другого браузера.

Если эта политика включена, в диалоговом окне **Импорт данных браузера** автоматически устанавливается флажок **Настройки браузера**.

Если эта политика отключена, настройки браузера не импортируются при первом запуске и пользователи не могут импортировать их вручную.

Если не настроить эту политику, настройки браузера импортируются при первом запуске и пользователи могут решить, импортировать ли их вручную во время следующих сеансов браузера.

Эту политику можно задать как рекомендуемую. Это означает, что Microsoft Edge импортирует настройки при первом запуске, но пользователи могут выбрать или отменить параметр **настройки браузера** во время импорта вручную.

**Примечание**. Эта политика в настоящее время управляет импортом из Google Chrome (в Windows 7, 8, 10 и в macOS).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ImportBrowserSettings
  - Имя групповой политики: Разрешить импорт настроек браузера
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: ImportBrowserSettings
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ImportBrowserSettings
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ImportCookies
  #### Разрешение импорта файлов cookie
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 81 или более поздней версии

  #### Описание
  Импорт файлов cookie в Microsoft Edge из другого браузера.

Если эта политика отключена, файлы cookie не импортируются при первом запуске.

Если эта политика не настроена, файлы cookie импортируются при первом запуске.

Вы также можете задать эту политику как рекомендуемую. Это означает, что Microsoft Edge импортирует файлы cookie при первом запуске.

**Примечание**. Эта политика в настоящее время управляет импортом из Google Chrome (в Windows 7, 8, 10 и в macOS).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ImportCookies
  - Имя групповой политики: Разрешение импорта файлов cookie
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: ImportCookies
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ImportCookies
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ImportExtensions
  #### Разрешение импорта расширений
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 81 или более поздней версии

  #### Описание
  Пользователям разрешается импортировать в Microsoft Edge расширения из другого браузера.

Если включить эту политику, в диалоговом окне **Импорт данных браузера** автоматически устанавливается флажок **Расширения**.

Если отключить эту политику, расширения не импортируются при первом запуске и пользователи не могут импортировать их вручную.

Если не настроить эту политику, расширения импортируются при первом запуске и во время следующих сеансов просмотра веб-страниц пользователи могут решить, нужно ли импортировать расширения вручную.

Эту политику также можно задать как рекомендацию. В таком случае браузер Microsoft Edge импортирует расширения при первом запуске, но во время ручного импорта пользователи могут установить или снять флажок **избранное**.

**Примечание**. Сейчас эта политика применяется только в случае импорта из Google Chrome (в Windows 7, 8, 10 и macOS).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ImportExtensions
  - Имя групповой политики: Разрешение импорта расширений
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: ImportExtensions
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ImportExtensions
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ImportFavorites
  #### Разрешить импорт избранного
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Импорт избранного в Microsoft Edge из другого браузера.

Если включить эту политику, флажок **Избранное** автоматически устанавливается в диалоговом окне **Импорт данных браузера**.

Если отключить эту политику, данные избранного не импортируются при первом запуске, а пользователи не могут импортировать их вручную.

Если не настраивать эту политику, данные избранного импортируются при первом запуске, а пользователи могут выбрать импорт этих данных вручную в дальнейших сеансах использования браузера.

Также можно включить эту политику в качестве рекомендации. Это означает, что Microsoft Edge импортирует данные избранного при первом запуске, но пользователи могут установить или снять флажок **избранное** при импорте вручную.

**Примечание**. Эта политика в настоящее время управляет импортом из браузеров Internet Explorer (в Windows 7, 8, 10), Google Chrome (в Windows 7, 8, 10 и macOS), Mozilla Firefox (в Windows 7, 8, 10 и macOS) и Apple Safari (macOS).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ImportFavorites
  - Имя групповой политики: Разрешить импорт избранного
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: ImportFavorites
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ImportFavorites
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ImportHistory
  #### Разрешить импорт журнала браузера
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Импорт журнала браузера в Microsoft Edge из другого браузера.

Если включить эту политику, флажок **Журнал браузера** автоматически устанавливается в диалоговом окне **Импорт данных браузера**.

Если отключить эту политику, данные журнала браузера не импортируются при первом запуске, а пользователи не смогут импортировать эти данные вручную.

Если не настраивать эту политику, данные журнала браузера импортируются при первом запуске, а пользователи могут выбрать импорт этих данных вручную в дальнейших сеансах использования браузера.

Также можно включить эту политику в качестве рекомендации. Это означает, что Microsoft Edge импортирует журнал браузера при первом запуске, но пользователи могут установить или снять флажок **журнал** при импорте вручную.

**Примечание**. Эта политика в настоящее время управляет импортом из браузеров Internet Explorer (в Windows 7, 8, 10), Google Chrome (в Windows 7, 8, 10 и macOS), Mozilla Firefox (в Windows 7, 8, 10 и macOS) и Apple Safari (macOS).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ImportHistory
  - Имя групповой политики: Разрешить импорт журнала браузера
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: ImportHistory
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ImportHistory
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ImportHomepage
  #### Разрешить импорт настроек домашней страницы
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Импорт домашней страницы в Microsoft Edge из другого браузера.

Если эта политика включена, автоматически разрешается импорт домашней страницы вручную.

Если эта политика отключена, домашняя страница не импортируется при первом запуске и пользователи не могут импортировать ее вручную.

Если эта политика не настроена, домашняя страница импортируется при первом запуске и пользователи могут решить, импортировать ли ее вручную во время следующих сеансов браузера.

Эту политику можно задать как рекомендуемую. Это означает, что Microsoft Edge импортирует домашнюю страницу при первом запуске, но пользователи могут выбрать или отменить параметр **домашняя страница** во время импорта вручную.

**Примечание**. Эта политика в настоящее время управляет импортом из Internet Explorer (в Windows 7, 8 и 10).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ImportHomepage
  - Имя групповой политики: Разрешить импорт настроек домашней страницы
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ImportHomepage
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ImportHomepage
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ImportOpenTabs
  #### Разрешение импорта открытых вкладок
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 79 или более поздней версии

  #### Описание
  Пользователям разрешается импортировать в Microsoft Edge открытые и закрепленные вкладки из другого браузера.

Если включить эту политику, в диалоговом окне **Импорт данных браузера** автоматически устанавливается флажок **Открытые вкладки**.

Если отключить эту политику, открытые вкладки не импортируются при первом запуске и пользователи не могут импортировать их вручную.

Если не настроить эту политику, открытые вкладки импортируются при первом запуске и во время следующих сеансов просмотра веб-страниц пользователи могут решить, нужно ли импортировать вкладки вручную.

Эту политику также можно задать как рекомендацию. В таком случае браузер Microsoft Edge импортирует открытые вкладки при первом запуске, но во время ручного импорта пользователи могут установить или снять флажок **Открытые вкладки**.

**Примечание**. Сейчас эта политика поддерживает только импорт из Google Chrome (в Windows 7, 8, 10 и macOS).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ImportOpenTabs
  - Имя групповой политики: Разрешение импорта открытых вкладок
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: ImportOpenTabs
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ImportOpenTabs
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ImportPaymentInfo
  #### Разрешить импорт платежных данных
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Импорт платежной информации в Microsoft Edge из другого браузера.

Если этот параметр политики включен, в диалоговом окне **Импорт данных браузера** автоматически устанавливается флажок **платежная информация**.

Если этот параметр политики отключен, платежная информация не импортируется при первом запуске и пользователи не могут импортировать ее вручную.

Если не настроить этот параметр политики, платежная информация импортируется при первом запуске и пользователи могут решить, импортировать ли ее вручную во время следующих сеансов браузера.

Этот параметр политики можно задать как рекомендуемый. Это означает, что Microsoft Edge импортирует платежную информацию при первом запуске, но пользователи могут выбрать или отменить параметр **платежная информация** во время импорта вручную.

**Примечание**. Этот параметр политики в настоящее время управляет импортом из Google Chrome (в Windows 7, 8, 10 и в macOS).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ImportPaymentInfo
  - Имя групповой политики: Разрешить импорт платежных данных
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: ImportPaymentInfo
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ImportPaymentInfo
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ImportSavedPasswords
  #### Разрешить импорт сохраненных паролей
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Разрешает пользователям импортировать сохраненные пароли из другого браузера в Microsoft Edge.

Если включить эту политику, автоматически устанавливается флажок импорта сохраненных паролей вручную.

Если отключить эту политику, сохраненные пароли не импортируются при первом запуске, а пользователи не могут выбрать импорт этих данных вручную в дальнейших сеансах использования браузера.

Если не настраивать эту политику, пароли импортируются при первом запуске, а пользователи не могут выбрать импорт этих данных вручную в дальнейших сеансах использования браузера.

Также можно включить эту политику в качестве рекомендации. Это означает, что Microsoft Edge импортирует данные пароли при первом запуске, но пользователи могут установить или снять флажок **пароли** при импорте вручную.

**Примечание**. Эта политика в настоящее время управляет импортом из Internet Explorer (в Windows 7, 8, 10), Google Chrome (в Windows 7, 8, 10 и macOS) и Mozilla Firefox (в Windows 7, 8, 10 и macOS).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ImportSavedPasswords
  - Имя групповой политики: Разрешить импорт сохраненных паролей
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: ImportSavedPasswords
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ImportSavedPasswords
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ImportSearchEngine
  #### Разрешить импортировать настройки поисковой системы
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Импорт настроек поисковой системы в Microsoft Edge из другого браузера.

Если эта политика включена, автоматически разрешается импорт настроек поисковой системы.

Если эта политика отключена, настройки поисковой системы не импортируются при первом запуске и пользователи не могут импортировать их вручную.

Если эта политика не настроена, настройки поисковой системы импортируются при первом запуске и пользователи могут решить, импортировать ли их вручную во время следующих сеансов браузера.

Эту политику можно задать как рекомендуемую. Это означает, что Microsoft Edge импортирует настройки поисковой системы при первом запуске, но пользователи могут выбрать или отменить параметр **поисковая система** во время импорта вручную.

**Примечание**. Эта политика в настоящее время управляет импортом из Internet Explorer (в Windows 7, 8 и 10).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ImportSearchEngine
  - Имя групповой политики: Разрешить импортировать настройки поисковой системы
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: ImportSearchEngine
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ImportSearchEngine
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ImportShortcuts
  #### Разрешить импорт ярлыков
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 81 или более поздней версии

  #### Описание
  Импорт ярлыков в Microsoft Edge из другого браузера.

Если отключить эту политику, ярлыки не импортируются при первом запуске.

Если не настраивать эту политику, ярлыки импортируются при первом запуске.

Также можно включить эту политику в качестве рекомендации. Это означает, что Microsoft Edge импортирует ярлыки при первом запуске.

**Примечание**. Эта политика в настоящее время управляет импортом из Google Chrome (в Windows 7, 8, 10 и в macOS).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ImportShortcuts
  - Имя групповой политики: Разрешить импорт ярлыков
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: ImportShortcuts
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ImportShortcuts
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### InPrivateModeAvailability
  #### Настроить доступность режима InPrivate
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определяет, есть ли у пользователя доступ к страницам в режиме InPrivate в Microsoft Edge.

Если не настроить этот параметр политики или присвоить ему значение 'Enabled', пользователи смогут открывать страницы в режиме InPrivate.

Если присвоить параметру значение 'Disabled', пользователи не смогут использовать режим InPrivate.

Если присвоить параметру значение 'Forced', режим InPrivate будет использоваться всегда.

Сопоставление параметров политики:

* Enabled (0) = Режим InPrivate доступен

* Disabled (1) = Режим InPrivate отключен

* Forced (2) = Принудительное использование режима InPrivate

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: InPrivateModeAvailability
  - Имя групповой политики: Настроить доступность режима InPrivate
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: InPrivateModeAvailability
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: InPrivateModeAvailability
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### InsecureFormsWarningsEnabled
  #### Enable warnings for insecure forms
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 86 или более поздней версии

  #### Описание
  This policy controls the handling of insecure forms (forms submitted over HTTP) embedded in secure (HTTPS) sites in the browser.
If you enable this policy or don't set it, a full page warning will be shown when an insecure form is submitted. Additionally, a warning bubble will be shown next to the form fields when they are focused, and autofill will be disabled for those forms.
If you disable this policy, warnings will not be shown for insecure forms, and autofill will work normally.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: InsecureFormsWarningsEnabled
  - Имя групповой политики: Enable warnings for insecure forms
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: InsecureFormsWarningsEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: InsecureFormsWarningsEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### IntensiveWakeUpThrottlingEnabled
  #### Управление функцией IntensiveWakeUpThrottling
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 85 или более поздней версии

  #### Описание
  Включение функции IntensiveWakeUpThrottling приводит к агрессивному регулированию и объединению таймеров JavaScript во вкладках на заднем плане. Она запускается не чаще одного раза в минуту после нахождения страницы на заднем плане в течение 5 минут или более.

Это функция, соответствующая веб-стандартам, но она может нарушить функциональность некоторых веб-сайтов, вызывая задержку определенных действий на срок до минуты. Однако при ее включении достигается значительная экономия ресурсов ЦП и батареи. Дополнительные сведения см. на странице https://bit.ly/30b1XR4.

Если включить эту политику, функция будет принудительно запущена, и пользователи не смогут переопределить этот параметр.
Если отключить эту политику, функция будет принудительно остановлена, и пользователи не смогут переопределить этот параметр.
Если не настроить эту политику, функция будет управляться собственной внутренней логикой. Пользователи смогут вручную настроить этот параметр.

Обратите внимание, что политика применяется для каждого процесса обработчика, а когда запускается процесс обработчика, применяется самое последнее значение параметра политики. Чтобы все загруженные вкладки получили согласованный параметр политики, требуется полная перезагрузка. Работа процессов с разными значениями этой политики не оказывает никакого вреда.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: IntensiveWakeUpThrottlingEnabled
  - Имя групповой политики: Управление функцией IntensiveWakeUpThrottling
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: IntensiveWakeUpThrottlingEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: IntensiveWakeUpThrottlingEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### InternetExplorerIntegrationEnhancedHangDetection
  #### Настройка расширенного определения зависания для режима Internet Explorer
  
  
  #### Поддерживаемые версии:
  - На Windows с 84 или более поздней версии

  #### Описание
  Расширенная функция обнаружения зависаний — это более детальный подход к обнаружению зависших веб-страниц в режиме Internet Explorer, чем тот, что используется в отдельном приложении Internet Explorer. При обнаружении зависшей страницы браузер применяет меры предотвращения зависания всего браузера.

Этот параметр позволяет настроить использование расширенной функции обнаружения зависаний в случае возникновения проблем несовместимости с любым веб-сайтом. Мы рекомендуем отключать эту политику только в том случае, когда сообщения типа "(веб-сайт) не отвечает" появляются в режиме Internet Explorer, но не в отдельном приложении Internet Explorer.

Эта настройка работает в сочетании со следующими параметрами политики:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) с присвоенным значением 'IEMode'
и
политикой [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist), в которой список содержит хотя бы одну запись.

Если для этой политики задано значение 'Enabled' или она не настроена, при работе с веб-сайтами в режиме Internet Explorer применяется расширенная функция обнаружения зависаний.

Если для этой политики задано значение 'Disabled', расширенная функция обнаружения зависаний не применяется и работает стандартный для Internet Explorer порядок обнаружения зависаний.

Подробнее о режиме Internet Explorer см. на странице [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Сопоставление параметров политики:

* Disabled (0) = Расширенное обнаружение зависания отключено

* Enabled (1) = Расширенное обнаружение зависания

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: InternetExplorerIntegrationEnhancedHangDetection
  - Имя групповой политики: Настройка расширенного определения зависания для режима Internet Explorer
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: InternetExplorerIntegrationEnhancedHangDetection
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  

  [В начало](#microsoft-edge:-политики)

  ### InternetExplorerIntegrationLevel
  #### Настройка интеграции с Internet Explorer
  
  
  #### Поддерживаемые версии:
  - На Windows с 77 или более поздней версии

  #### Описание
  Инструкции по настройке оптимального интерфейса режима Internet Explorer см. на странице [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

Сопоставление параметров политики:

* None (0) = Нет

* IEMode (1) = Режим Internet Explorer

* NeedIE (2) = Internet Explorer 11

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: InternetExplorerIntegrationLevel
  - Имя групповой политики: Настройка интеграции с Internet Explorer
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: InternetExplorerIntegrationLevel
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  

  [В начало](#microsoft-edge:-политики)

  ### InternetExplorerIntegrationSiteList
  #### Настроить список сайтов для режима предприятия
  
  
  #### Поддерживаемые версии:
  - На Windows с 78 или более поздней версии

  #### Описание
  Инструкции по настройке оптимального интерфейса режима Internet Explorer см. на странице [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: InternetExplorerIntegrationSiteList
  - Имя групповой политики: Настроить список сайтов для режима предприятия
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: InternetExplorerIntegrationSiteList
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"https://internal.contoso.com/sitelist.xml"
```


  

  [В начало](#microsoft-edge:-политики)

  ### InternetExplorerIntegrationSiteRedirect
  #### Укажите способ обработки переходов "на странице" для ненастроенных сайтов, выполненных со страниц в режиме Internet Explorer
  
  
  #### Поддерживаемые версии:
  - На Windows с 81 или более поздней версии

  #### Описание
  Переход "на странице" запускается из ссылки, сценария или формы на текущей странице. Он также может быть выполнен в виде перенаправления на стороне сервера для предыдущей попытки перехода "на странице". И наоборот, пользователь может независимо от текущей страницы несколькими способами инициировать переход, отличный от перехода "на странице", с помощью элементов управления браузера. Например, он может воспользоваться адресной строкой, кнопкой "Назад" или ссылкой из избранного.

Эта настройка позволяет указать, будут ли переходы на ненастроенные сайты (сайты, которые не настроены в Списке сайтов в режиме предприятия) со страниц, загруженных в режиме Internet Explorer, переключаться в режим Microsoft Edge или оставаться в режиме Internet Explorer.

Эта настройка работает в связке с:
политикой [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel), для которой установлено значение 'IEMode',
и
политикой [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist), в которой список содержит хотя бы одну запись.

Если отключить или не настроить эту политику, в режиме Internet Explorer будут открываться только сайты, настроенные для открытия в этом режиме. Любые сайты, не настроенные для открытия в режиме Internet Explorer, будут перенаправлены обратно в Microsoft Edge.

Если для этого параметра задано значение 'Default', в режиме Internet Explorer будут открываться только сайты, настроенные для открытия в этом режиме. Любые сайты, не настроенные для открытия в режиме Internet Explorer, будут перенаправлены обратно в Microsoft Edge.

Если для этого параметра задано значение 'AutomaticNavigationsOnly', для всех переходов будут настройки по умолчанию, кроме автоматических переходов на ненастроенные сайты (например, перенаправления по состоянию 302), которые будут выполняться в режиме Internet Explorer.

 Если для этого параметра задано значение 'AllInPageNavigations', все переходы на ненастроенные сайты со страниц, загруженных в режиме Internet Explorer, будут выполняться в режиме Internet Explorer (не рекомендуется).

Дополнительные сведения о режиме Internet Explorer см. на странице [https://go.microsoft.com/fwlink/?linkid=2105106](https://go.microsoft.com/fwlink/?linkid=2105106)

Сопоставление параметров политики:

* Default (0) = По умолчанию

* AutomaticNavigationsOnly (1) = Выполнять в режиме Internet Explorer только автоматические переходы

* AllInPageNavigations (2) = Выполнять в режиме Internet Explorer все переходы "на странице"

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: InternetExplorerIntegrationSiteRedirect
  - Имя групповой политики: Укажите способ обработки переходов "на странице" для ненастроенных сайтов, выполненных со страниц в режиме Internet Explorer
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: InternetExplorerIntegrationSiteRedirect
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  

  [В начало](#microsoft-edge:-политики)

  ### InternetExplorerIntegrationTestingAllowed
  #### Allow Internet Explorer mode testing
  
  
  #### Поддерживаемые версии:
  - На Windows с 86 или более поздней версии

  #### Описание
  This policy is a replacement for the ie-mode-test flag policy. It lets users open an IE mode tab from the UI menu option.

This setting works in conjunction with:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) is set to 'IEMode'
and
[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) policy where the list has at least one entry.

If you enable this policy, users can open IE mode tab from the UI option and navigate current site to an IE mode site.

If you disable this policy, users can't see the UI option in the menu directly.

If you don't configure this policy, you can set up the ie-mode-test flag manually.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: InternetExplorerIntegrationTestingAllowed
  - Имя групповой политики: Allow Internet Explorer mode testing
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: InternetExplorerIntegrationTestingAllowed
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  

  [В начало](#microsoft-edge:-политики)

  ### IsolateOrigins
  #### Включить изоляцию сайта для определенных источников
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Укажите источники для выполнения в режиме изоляции, в собственном процессе.
Эта политика также изолирует источники, названные дочерними доменами (например, если указать https://contoso.com/, то https://foo.contoso.com/ будет изолирован как часть сайта https://contoso.com/).
Если эта политика включена, каждый из названных источников в списке, который разделяется запятыми, будет выполняться в отдельном процессе.
Если эта политика отключена, функции [IsolateOrigins](#isolateorigins) и [SitePerProcess](#siteperprocess) будут отключены. Пользователи по-прежнему смогут включить политику [IsolateOrigins](#isolateorigins) вручную с помощью флага командной строки.
Если эта политика не настроена, пользователь сможет изменить его значение.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: IsolateOrigins
  - Имя групповой политики: Включить изоляцию сайта для определенных источников
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: IsolateOrigins
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"https://contoso.com/,https://fabrikam.com/"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: IsolateOrigins
  - Пример значения:
``` xml
<string>https://contoso.com/,https://fabrikam.com/</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### LocalProvidersEnabled
  #### Разрешить предложения локальных поставщиков
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 83 или более поздней версии

  #### Описание
  Разрешить предложения поставщиков предложений на устройстве (локальных поставщиков), например "Избранное" и "Журнал браузера", в адресной строке и списке автоматических предложений Microsoft Edge.

Если включить эту политику, используются предложения локальных поставщиков.

Если отключить эту политику, предложения локальных поставщиков не будут использоваться, предложения на основе локального журнала и избранного не будут отображаться.

Если не настраивать эту политику, предложения локальных поставщиков будут разрешены, но пользователь может изменить эту настройку, переключив соответствующий настройку.

Обратите внимание, что некоторые функции могут быть недоступными, если применена политика для отключения этой функции. Например, если включить политику [SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled), предложения из "Журнала браузера" будут недоступны.

Чтобы завершить применения этой политики, необходимо перезапустить браузер.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: LocalProvidersEnabled
  - Имя групповой политики: Разрешить предложения локальных поставщиков
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: LocalProvidersEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: LocalProvidersEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ManagedFavorites
  #### Настроить "Избранное"
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Настройка списка управляемых элементов избранного.

Этот параметр политики определяет список элементов избранного. Каждый такой элемент содержит разделы "name" и "url", в которых указаны его название и целевой адрес. Можно настроить вложенную папку, определив элементы избранного без раздела "url", но с дополнительным разделом "children", который будет содержать список элементов избранного, как описано выше (некоторые элементы могут представлять собой папки). Microsoft Edge завершает неполные URL-адреса так, как если бы они были введены через адресную строку, например "microsoft.com" станет "https://microsoft.com/".

Эти элементы избранного размещаются в папке, которую не может изменить пользователь (но пользователь может скрыть ее на панели избранного). По умолчанию эта папка называется "Управляемое избранное", но вы можете изменить это название, добавив в список элементов избранного словарь, содержащий раздел "toplevel_name", и указав необходимое имя папки в качестве значения.

Управляемое избранное не синхронизируется с учетной записью пользователя и не может быть изменено расширениями.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Словарь

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ManagedFavorites
  - Имя групповой политики: Настроить "Избранное"
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ManagedFavorites
  - Тип значения: REG_SZ
  ##### Пример значения:
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


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ManagedFavorites
  - Пример значения:
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
  

  [В начало](#microsoft-edge:-политики)

  ### ManagedSearchEngines
  #### Управление поисковыми системами
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Дает возможность настроить список, включающий до 10 поисковых систем, одна из которых должна быть выбрана в качестве поисковой системы по умолчанию.
Нет необходимости указывать кодировку. С версии Microsoft Edge 80 параметры suggest_url и image_search_url являются необязательными. Необязательный параметр image_search_post_params (состоит из разделенных запятыми пар имен и значений) доступен в версии Microsoft Edge 80 и более поздних версиях.

С версии Microsoft Edge 83 можно включить обнаружение поисковых систем с помощью необязательного параметра allow_search_engine_discovery. Этот параметр должен быть первым в списке. Если параметр allow_search_engine_discovery не указан, обнаружение поисковых систем будет отключено по умолчанию. С версии Microsoft Edge 84 можно настроить эту политику в качестве рекомендуемой, чтобы разрешить обнаружение служб поиска. Вам не требуется добавлять необязательный параметр allow_search_engine_discovery.

Если включить эту политику, пользователи не смогут добавлять, удалять или изменять поисковые системы, указанные в списке. Пользователи могут выбрать одну из поисковых систем в списке в качестве поисковой системы по умолчанию.

Если отключить или не настраивать эту политику, пользователи смогут изменять список поисковых систем произвольным образом.

Если задана политика [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl), эта политика (ManagedSearchEngines) игнорируется. Чтобы завершить применение этой политики, пользователь должен перезапустить браузер.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Словарь

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ManagedSearchEngines
  - Имя групповой политики: Управление поисковыми системами
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: ManagedSearchEngines
  - Тип значения: REG_SZ
  ##### Пример значения:
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


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ManagedSearchEngines
  - Пример значения:
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
  

  [В начало](#microsoft-edge:-политики)

  ### MaxConnectionsPerProxy
  #### Максимальное число одновременных подключений к прокси-серверу
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Задает максимальное число одновременных подключений к прокси-серверу.

Некоторые прокси-серверы не могут обрабатывать большое количество одновременных подключений для каждого клиента. Это можно решить, задав данной настройке политики меньшее значение.

Значение этой настройки политики должно быть меньше 100 и больше 6. Значение по умолчанию — 32 подключения.

Известно, что некоторые веб-приложения используют большое число подключений с зависшими запросами GET. Уменьшение максимального числа подключений ниже 32 может привести к зависанию сети браузера, если открыто слишком много веб-приложений этого вида.

Если эта политика не настроена, используется значение по умолчанию (32).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: MaxConnectionsPerProxy
  - Имя групповой политики: Максимальное число одновременных подключений к прокси-серверу
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: MaxConnectionsPerProxy
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000020
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: MaxConnectionsPerProxy
  - Пример значения:
``` xml
<integer>32</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### MediaRouterCastAllowAllIPs
  #### Разрешить Google Cast подключаться к устройствам передачи с любыми IP-адресами
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Включите этот параметр политики, чтобы разрешить Google Cast подключаться к устройствам передачи с любыми IP-адресами, а не только частными адресами RFC1918/RFC4193.

Отключите этот параметр политики, чтобы разрешить Google Cast подключаться только к устройствам передачи с частными адресами RFC1918/RFC4193.

Если этот параметр политики не настроен, Google Cast подключается только к устройствам передачи с частными адресами RFC1918/RFC4193 (если не включена функция CastAllowAllIPs).

Если политика [EnableMediaRouter](#enablemediarouter) отключена, эта политика не действует.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: MediaRouterCastAllowAllIPs
  - Имя групповой политики: Разрешить Google Cast подключаться к устройствам передачи с любыми IP-адресами
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: MediaRouterCastAllowAllIPs
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: MediaRouterCastAllowAllIPs
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### MetricsReportingEnabled
  #### Включить отправку отчетов об использовании и данных, относящихся к сбою (не рекомендуется)
  >УСТАРЕЛО. Эта политика устарела. В настоящее время она поддерживается, но станет устаревшей в будущем выпуске.
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Это нерекомендуемая политика. В настоящее время она поддерживается, но перестанет поддерживаться в Microsoft Edge 89. Эта политика заменяется новой политикой [DiagnosticData](#diagnosticdata) в Windows 7, Windows 8 и macOS. Эта политика заменяется политикой "Разрешить телеметрию" в Windows 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

Эта политика разрешает отправку корпорации Майкрософт отчетов об использовании и сбоях, касающихся Microsoft Edge.

Включите эту политику, чтобы разрешить отправку корпорации Майкрософт отчетов об использовании и сбоях. Отключите эту политику, чтобы запретить отправку данных корпорации Майкрософт. В обоих случаях пользователи не смогут изменить или переопределить эту настройку.

В Windows 10, если вы не настроите эту политику, Microsoft Edge будет по умолчанию использовать настройку диагностических данных Windows. Если включить эту политику, Microsoft Edge будет отправлять данные об использовании, только если для параметра диагностических данных Windows установлено значение "Расширенные" или "Полные". Если отключить эту политику, Microsoft Edge не будет отправлять данные об использовании. Данные о сбоях будут отправляться на основании параметра диагностических данных Windows. Дополнительные сведения о параметре диагностических данных Windows см. на странице [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

В Windows 7, Windows 8 и macOS эта политика управляет отправкой данных об использовании и сбоях. Если эта политика не настроена, Microsoft Edge будет по умолчанию использовать параметры пользователя.

Чтобы включить эту политику, параметру [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) требуется присвоить значение "Включено". Если политике [MetricsReportingEnabled](#metricsreportingenabled) или [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) присвоено значение "Не настроено" или "Отключено", эти данные не отправляются в корпорацию Майкрософт.

  Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: MetricsReportingEnabled
  - Имя групповой политики: Включить отправку отчетов об использовании и данных, относящихся к сбою (не рекомендуется)
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: MetricsReportingEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: MetricsReportingEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### NativeWindowOcclusionEnabled
  #### Включить закрытие собственныых окон
  
  
  #### Поддерживаемые версии:
  - На Windows с 84 или более поздней версии

  #### Описание
  Включает обнаружение перекрытия собственного окна в Microsoft Edge.

Если этот параметр включен, для снижения нагрузки на ЦП и энергопотребления Microsoft Edge будет определять, когда окно перекрывается другими окнами, и приостанавливать работу по отрисовке пикселей.

Если этот параметр отключен, Microsoft Edge не будет определять, когда окно перекрывается другими окнами.

Если эта политика не настроена, обнаружение скрытия окна будет включено.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: NativeWindowOcclusionEnabled
  - Имя групповой политики: Включить закрытие собственныых окон
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: NativeWindowOcclusionEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  

  [В начало](#microsoft-edge:-политики)

  ### NavigationDelayForInitialSiteListDownloadTimeout
  #### Установка времени ожидания для задержки перехода на вкладку для списка сайтов в режиме предприятия
  
  
  #### Поддерживаемые версии:
  - На Windows с 84 или более поздней версии

  #### Описание
  Позволяет вам установить время ожидания в секундах для вкладок Microsoft Edge, ожидающих перехода, пока браузер скачивает исходный список сайтов, открываемых в режиме предприятия.

Этот параметр работает совместно с:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) с присвоенным значением 'IEMode'
и
политикой [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist), когда в списке есть хотя бы одна запись,
и
[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload) с присвоенным значением "Все допустимые переходы" (1).

Время ожидания вкладок не будет превышать время скачивания списка сайтов, открываемых в режиме предприятия. Если браузер не завершил скачивание списка сайтов, открываемых в режиме предприятия, до истечения времени ожидания, переход по вкладкам Microsoft Edge продолжится. Значение времени ожидания не должно превышать 20 секунд и не должно быть меньше 1 секунды.

Если вы настроите для времени ожидания в этой политике значение, превышающее стандартные 2 секунды, для пользователя отобразится панель информации по прошествии 2 секунд. Панель информации содержит кнопку, позволяющую пользователям покинуть режим ожидания скачивания списка сайтов, открываемых в режиме предприятия.

Если вы не настроите эту политику, будет применено стандартное время ожидания в 2 секунды. Это стандартное значение может измениться в будущем.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: NavigationDelayForInitialSiteListDownloadTimeout
  - Имя групповой политики: Установка времени ожидания для задержки перехода на вкладку для списка сайтов в режиме предприятия
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: NavigationDelayForInitialSiteListDownloadTimeout
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x0000000a
```


  

  [В начало](#microsoft-edge:-политики)

  ### NetworkPredictionOptions
  #### Включить прогнозирование сети
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Включает прогнозирование сети и запрещает пользователям изменять эту настройку.

Это позволяет контролировать предварительную загрузку DNS, предварительное TCP- и SSL-соединение, а также предварительную обработку веб-страниц.

Если эта политика не настроена, прогнозирование сети включено, но пользователь может изменить это значение.

Сопоставление параметров политики:

* NetworkPredictionAlways (0) = Прогнозировать действия сети для любого сетевого подключения

* NetworkPredictionWifiOnly (1) = Не поддерживается; если применено это значение, оно будет обрабатываться как настроенный параметр "Прогнозировать действия сети для любого сетевого подключения" (0)

* NetworkPredictionNever (2) = Не прогнозировать действия сети для каких-либо сетевых подключений

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: NetworkPredictionOptions
  - Имя групповой политики: Включить прогнозирование сети
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: NetworkPredictionOptions
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000002
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: NetworkPredictionOptions
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### NonRemovableProfileEnabled
  #### Настройка постоянного автоматического входа пользователя в стандартный профиль на основе рабочей или учебной учетной записи
  
  
  #### Поддерживаемые версии:
  - На Windows с 78 или более поздней версии

  #### Описание
  Эта политика определяет, может ли пользователь удалить профиль Microsoft Edge, в который выполняется автоматический вход на основе рабочей или учебной учетной записи пользователя.

Если эта политика включена, будет создан неудаляемый профиль на основе рабочей или учебной учетной записи пользователя в Windows. Пользователь не сможет выйти из этого профиля или удалить его.

Если эта политика отключена или не настроена, пользователь может выйти из профиля, в который выполняется автоматический вход на основе рабочей или учебной учетной записи пользователя в Windows, или удалить его.

Если необходимо настроить вход в браузер, используйте политику [BrowserSignin](#browsersignin).

  Эта политика доступна только в экземплярах Windows, подключенных к домену Microsoft Active Directory, экземплярах Windows 10 Pro и Windows 10 Корпоративная, зарегистрированных для управления устройствами, а также в экземплярах macOS, управляемых посредством MDM или подключенных к домену через MCX.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: NonRemovableProfileEnabled
  - Имя групповой политики: Настройка постоянного автоматического входа пользователя в стандартный профиль на основе рабочей или учебной учетной записи
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: NonRemovableProfileEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  

  [В начало](#microsoft-edge:-политики)

  ### OverrideSecurityRestrictionsOnInsecureOrigin
  #### Управление применением ограничений доступа к небезопасным источникам
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Эта политика позволяет указать список источников (URL-адреса) или шаблонов имен узлов (например, "*.contoso.com"), к которым не применяются ограничения, связанные с небезопасными источниками.

Вы можете указать разрешенные источники устаревших приложений, которые не позволяют развернуть TLS или настроить сервер промежуточного хранения для внутренней веб-разработки, чтобы разработчики могли тестировать функции, требующие безопасного контекста, не разворачивая TLS на сервере промежуточного хранения. Эта политика также запрещает отображать для источников отметку "Небезопасно" в адресной строке omnibox.

Список URL-адресов в этом параметре политики имеет тот же эффект, что и список тех же URL-адресов через запятую, указанный для флага командной строки "--unsafely-treat-insecure-origin-as-secure". Если этот параметр политики включен, он переопределяет флаг командной строки.

Подробные сведения о безопасных контекстах см. здесь: https://www.w3.org/TR/secure-contexts/.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: OverrideSecurityRestrictionsOnInsecureOrigin
  - Имя групповой политики: Управление применением ограничений доступа к небезопасным источникам
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\1 = "http://testserver.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\2 = "*.contoso.com"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: OverrideSecurityRestrictionsOnInsecureOrigin
  - Пример значения:
``` xml
<array>
  <string>http://testserver.contoso.com/</string>
  <string>*.contoso.com</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### PaymentMethodQueryEnabled
  #### Разрешить веб-сайтам запрашивать информацию о наличии доступных методов оплаты
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 80 или более поздней версии

  #### Описание
  Позволяет задать, могут ли веб-сайты проверять наличие у пользователя сохраненных методов оплаты.

Если отключить эту политику, то веб-сайты, на которых используется API PaymentRequest.canMakePayment или PaymentRequest.hasEnrolledInstrument, информируются об отсутствии методов оплаты.

Если включить или не задать эту политику, то веб-сайты могут проверять наличие у пользователя сохраненных методов оплаты.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PaymentMethodQueryEnabled
  - Имя групповой политики: Разрешить веб-сайтам запрашивать информацию о наличии доступных методов оплаты
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: PaymentMethodQueryEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: PaymentMethodQueryEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### PersonalizationReportingEnabled
  #### Разрешить персонализацию рекламы, результатов поиска и новостей путем отправки журнала браузера в корпорацию Майкрософт
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 80 или более поздней версии

  #### Описание
  Эта политика запрещает корпорации Майкрософт получать журнал браузера Microsoft Edge для персонализации рекламы, результатов поиска, новостей и других данных в рамках служб Майкрософт.

Этот параметр доступен только для пользователей с учетной записью Майкрософт, однако недоступен для учетных записей детей и предприятий.

Если эта политика отключена, пользователи не могут изменить или переопределить этот параметр. Если эта политика включена или не настроена, Microsoft Edge по умолчанию использует настройки пользователя.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PersonalizationReportingEnabled
  - Имя групповой политики: Разрешить персонализацию рекламы, результатов поиска и новостей путем отправки журнала браузера в корпорацию Майкрософт
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: PersonalizationReportingEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: PersonalizationReportingEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### PinningWizardAllowed
  #### Разрешить использование мастера закрепления на панели задач
  
  
  #### Поддерживаемые версии:
  - На Windows с 80 или более поздней версии

  #### Описание
  Мастер закрепления на панели задач в Microsoft Edge позволяет закреплять предлагаемые сайты на панели задач. Этот мастер включен по умолчанию и доступен для пользователей в разделе настроек и меню дополнительных параметров.

Если эта политика включена или не настроена, пользователи могут вызывать мастер закрепления с помощью раздела настроек или меню дополнительных параметров. Его также можно вызвать путем запуска протокола.

Если эта политика отключена, мастер закрепления недоступен в меню и его нельзя вызвать путем запуска протокола.

Настройки пользователя для включения и отключения мастера закрепления недоступны.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PinningWizardAllowed
  - Имя групповой политики: Разрешить использование мастера закрепления на панели задач
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: PinningWizardAllowed
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  

  [В начало](#microsoft-edge:-политики)

  ### ProactiveAuthEnabled
  #### Включить упреждающую проверку подлинности
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Включение или отключение упреждающей проверки подлинности.

Если этот параметр политики включен, Microsoft Edge с помощью служб Майкрософт выполняет упреждающую проверку подлинности пользователей, которые входят в систему. При этом Microsoft Edge периодически связывается с веб-службой, чтобы получить обновленный манифест, содержащий настройки для такой проверки подлинности.

Если этот параметр политики отключен, Microsoft Edge не пытается с помощью служб Майкрософт выполнять упреждающую проверку подлинности пользователей, которые входят в систему. Также Microsoft Edge не связывается с веб-службой, чтобы получить обновленный манифест, содержащий настройки для такой проверки подлинности.

Если не настроить этот параметр политики, упреждающая проверка подлинности будет включена.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ProactiveAuthEnabled
  - Имя групповой политики: Включить упреждающую проверку подлинности
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ProactiveAuthEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ProactiveAuthEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### PromotionalTabsEnabled
  #### Включить отображение полноширинной вкладки с рекламным содержимым
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Настройка представления рекламного или учебного содержимого на всей вкладке. Эта политика позволяет настроить вид страниц приветствия, на которых пользователи могут входить в Microsoft Edge, выбирать стандартный браузер или получать информацию о возможностях продукта.

Если эта политика включена (присвоено значение true) или не настроена, Microsoft Edge может отображать содержимое на всей вкладке, чтобы сообщить сведения о продукте.

Если эта политика отключена (присвоено значение false), Microsoft Edge не может отображать содержимое на всей вкладке.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PromotionalTabsEnabled
  - Имя групповой политики: Включить отображение полноширинной вкладки с рекламным содержимым
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: PromotionalTabsEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: PromotionalTabsEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### PromptForDownloadLocation
  #### Спрашивать, куда сохранять загруженные файлы
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Эта политика позволяет указать, необходимо ли спрашивать пользователя о месте сохранения файла перед загрузкой.

Если эта политика включена, перед каждой загрузкой система просит пользователя указать, где сохранить файл. Если эта политика не настроена, файлы автоматически сохраняются в папку, используемую по умолчанию, без запроса к пользователю.

Если эта политика не настроена, пользователь может изменить данную настройку.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: PromptForDownloadLocation
  - Имя групповой политики: Спрашивать, куда сохранять загруженные файлы
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: PromptForDownloadLocation
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: PromptForDownloadLocation
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### QuicAllowed
  #### Разрешить протокол QUIC
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Использование протокола QUIC в Microsoft Edge.

Если этот параметр политики включен или не настроен, протокол QUIC разрешен.

Если этот параметр политики отключен, протокол QUIC блокируется.

QUIC — это сетевой протокол транспортного уровня, который может повысить производительность веб-приложений, использующих подключение по протоколу TCP.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: QuicAllowed
  - Имя групповой политики: Разрешить протокол QUIC
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: QuicAllowed
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: QuicAllowed
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### RelaunchNotification
  #### Уведомлять пользователя о том, что рекомендуется или требуется перезапустить браузер для ожидающих обновлений
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Уведомление пользователей о необходимости перезапуска Microsoft Edge для применения отложенных обновлений.

Если этот параметр политики не настроен, Microsoft Edge добавляет значок перезапуска в дальнем правом углу верхней строки меню, чтобы уведомить пользователя о необходимости перезагрузить браузер для применения обновления.

Если этот параметр политики включен и ему присвоено значение 'Recommended', повторяющееся предупреждение сообщает пользователям, что рекомендуется выполнить перезапуск. Пользователь сможет закрыть это предупреждение и отложить перезапуск.

Если параметру политики присвоено значение 'Required', повторяющееся предупреждение сообщает пользователям о том, что браузер будет автоматически перезапущен по истечении периода предупреждения, который по умолчанию составляет 7 дней. Этот период можно изменить с помощью параметра политики [RelaunchNotificationPeriod](#relaunchnotificationperiod).

Сеанс пользователя будет восстановлен после перезапуска браузера.

Сопоставление параметров политики:

* Recommended (1) = Рекомендуется – Периодически показывать пользователю сообщение о том, что рекомендуется выполнить перезапуск

* Required (2) = Обязательно – Периодически показывать пользователю сообщение о том, что требуется выполнить перезапуск

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: RelaunchNotification
  - Имя групповой политики: Уведомлять пользователя о том, что рекомендуется или требуется перезапустить браузер для ожидающих обновлений
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: RelaunchNotification
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: RelaunchNotification
  - Пример значения:
``` xml
<integer>1</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### RelaunchNotificationPeriod
  #### Задать период времени для уведомлений об обновлении
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Позволяет задать период времени (в миллисекундах), по истечении которого пользователей уведомляют, что Microsoft Edge необходимо перезапустить, чтобы применить отложенное обновление.

В течение этого периода времени пользователь будет повторно уведомлен о необходимости обновления. В Microsoft Edge меню приложения меняется, чтобы указать, что требуется перезагрузка после того, как прошла треть периода уведомления. Цвет уведомления меняется после того, как пройдет две трети периода уведомлений, и во второй раз после истечения полного периода уведомления. Дополнительные уведомления, включенные политикой [RelaunchNotification](#relaunchnotification), следуют тому же алгоритму.

Если этот параметр не задан, используется стандартный период в 604 800 000 миллисекунд (одна неделя).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: RelaunchNotificationPeriod
  - Имя групповой политики: Задать период времени для уведомлений об обновлении
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: RelaunchNotificationPeriod
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x240c8400
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: RelaunchNotificationPeriod
  - Пример значения:
``` xml
<integer>604800000</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### RendererCodeIntegrityEnabled
  #### Включить целостность кода визуализации
  
  
  #### Поддерживаемые версии:
  - На Windows с 78 или более поздней версии

  #### Описание
  Если этот параметр политики включен или не задан, целостность кода визуализации включена. Эту политику следует отключать только в случае обнаружения проблем совместимости с программным обеспечением сторонних производителей, которое должно выполняться в процессах визуализации Microsoft Edge.

Отключение этой политики может негативно повлиять на безопасность и стабильность Microsoft Edge в связи с тем, что неизвестному и потенциально злонамеренному коду будет разрешено загружаться в процессы визуализации Microsoft Edge.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: RendererCodeIntegrityEnabled
  - Имя групповой политики: Включить целостность кода визуализации
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: RendererCodeIntegrityEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  

  [В начало](#microsoft-edge:-политики)

  ### RequireOnlineRevocationChecksForLocalAnchors
  #### Укажите, требуются ли проверки OCSP и списка отзыва сертификатов через Интернет для локальных якорей доверия
  
  
  #### Поддерживаемые версии:
  - На Windows с 77 или более поздней версии

  #### Описание
  Настройки обязательных проверок отзыва сертификатов через Интернет (проверки списка отзыва сертификатов или OCSP). Если Microsoft Edge не может получить информацию о состоянии отзыва, соответствующие сертификаты считаются отозванными ("серьезный сбой").

Если этот параметр политики включен, Microsoft Edge всегда выполняет проверку отзыва для сертификатов сервера, которые были успешно проверены и подписаны сертификатами локально установленных ЦС.

Если не настроить или отключить эту политику, Microsoft Edge будет использовать существующие настройки проверки отзыва сертификатов через Интернет.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: RequireOnlineRevocationChecksForLocalAnchors
  - Имя групповой политики: Укажите, требуются ли проверки OCSP и списка отзыва сертификатов через Интернет для локальных якорей доверия
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: RequireOnlineRevocationChecksForLocalAnchors
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  

  [В начало](#microsoft-edge:-политики)

  ### ResolveNavigationErrorsUseWebService
  #### Включить устранение ошибок навигации с помощью веб-службы
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Подключение Microsoft Edge к веб-службе без использования данных для проверки подключения к сетям Wi-Fi в аэропортах, гостиницах и т. п.

Если эта политика включена, для проверки подключения к сети используется веб-служба.

Если эта политика отключена, Microsoft Edge использует собственные API, чтобы попытаться решить проблемы подключения к сети и навигации.

**Примечание**. За исключением Windows 8 и более поздних версий, Microsoft Edge *всегда* использует собственные API для решения проблем с подключением.

Если эта политика не настроена, Microsoft Edge применяет настройки пользователя, указанные в разделе "Службы" на странице edge://settings/privacy.
В частности, там находится переключатель **Использовать веб-службу для решения проблем с навигацией**, который пользователь может включить или выключить. Обратите внимание: если данная политика (ResolveNavigationErrorsUseWebService) включена, настройка **Использовать веб-службу для решения проблем с навигацией** будет включена, но пользователь не сможет изменить его с помощью этого переключателя. Если отключить эту политику, настройка **Использовать веб-службу для решения проблем с навигацией** будет отключен и пользователь не сможет изменить его с помощью этого переключателя.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ResolveNavigationErrorsUseWebService
  - Имя групповой политики: Включить устранение ошибок навигации с помощью веб-службы
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: ResolveNavigationErrorsUseWebService
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ResolveNavigationErrorsUseWebService
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### RestrictSigninToPattern
  #### Ограничить учетные записи, которые могут использоваться в качестве основных в Microsoft Edge
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определяет, какие учетные записи можно задать в качестве основных учетных записей браузера в Microsoft Edge (учетная запись, выбранная в процессе синхронизации).

Если пользователь попытается настроить учетную запись в браузере, не соответствующую этому шаблону, он будет заблокирован и получит соответствующее сообщение об ошибке. Эту политику можно настроить в соответствии с несколькими учетными записями, используя регулярное выражение стиля Perl для шаблона. Обратите внимание, что в совпадениях с шаблоном учитывается регистр. Дополнительные сведения об используемых правилах регулярных выражений см. в статье https://go.microsoft.com/fwlink/p/?linkid=2133903.

Если не настроить эту политику или оставить ее пустой, пользователи смогут установить любую учетную запись в качестве основной учетной записи браузера в Microsoft Edge.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: RestrictSigninToPattern
  - Имя групповой политики: Ограничить учетные записи, которые могут использоваться в качестве основных в Microsoft Edge
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: RestrictSigninToPattern
  - Тип значения: REG_SZ
  ##### Пример значения:
```
".*@contoso.com"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: RestrictSigninToPattern
  - Пример значения:
``` xml
<string>.*@contoso.com</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### RoamingProfileLocation
  #### Задать каталог для перемещаемого профиля
  
  
  #### Поддерживаемые версии:
  - На Windows с 85 или более поздней версии

  #### Описание
  Настраивает каталог, который используется для сохранения перемещаемой копии профилей.

Если включить этот параметр политики, Microsoft Edge будет использовать указанный каталог для хранения перемещаемой копии профилей, если вы также включили политику [RoamingProfileSupportEnabled](#roamingprofilesupportenabled). Если отключить политику [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) или не настроить ее, значение, сохраненное в этой политике, не будет использоваться.

Список переменных, которые можно использовать, см. на странице [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

Если не настроить эту политику, будет использоваться путь к перемещаемому профилю по умолчанию.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: RoamingProfileLocation
  - Имя групповой политики: Задать каталог для перемещаемого профиля
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: RoamingProfileLocation
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"${roaming_app_data}\\edge-profile"
```


  

  [В начало](#microsoft-edge:-политики)

  ### RoamingProfileSupportEnabled
  #### Разрешить использование перемещаемых копий для данных профиля Microsoft Edge
  
  
  #### Поддерживаемые версии:
  - На Windows с 85 или более поздней версии

  #### Описание
  Включите эту политику, чтобы использовать перемещаемые профили в Windows. Параметры, сохраненные в профилях Microsoft Edge (избранное и настройки), также сохраняются в файл, хранящийся в папке перемещаемого профиля пользователя (или в расположении, указанном администратором с помощью политики [RoamingProfileLocation](#roamingprofilelocation)).

Если отключить этот параметр политики или не настроить его, будут использоваться только обычные локальные профили.

Политика [SyncDisabled](#syncdisabled) отключает синхронизацию всех данных, переопределяя политику.

Дополнительные сведения об использовании перемещаемых профилей пользователей см. на странице https://docs.microsoft.com/windows-server/storage/folder-redirection/deploy-roaming-user-profiles.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: RoamingProfileSupportEnabled
  - Имя групповой политики: Разрешить использование перемещаемых копий для данных профиля Microsoft Edge
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: RoamingProfileSupportEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  

  [В начало](#microsoft-edge:-политики)

  ### RunAllFlashInAllowMode
  #### Расширить настройку содержимого Adobe Flash на все содержимое
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Если эта политика включен, все содержимое Adobe Flash, внедренное в веб-сайты, на которых разрешен Adobe Flash в настройках содержимого (политикой пользователя или предприятия), будет запускаться. Это относится ко всему содержимому из других источников и/или небольшому содержимому.

Сведения об управлении веб-сайтами, которым разрешено запускать Adobe Flash, см. в спецификациях для политик [DefaultPluginsSetting](#defaultpluginssetting), [PluginsAllowedForUrls](#pluginsallowedforurls) и [PluginsBlockedForUrls](#pluginsblockedforurls).

Если эта политика отключена или не задана, содержимое Adobe Flash из других источников (с сайтов, которые не указаны в перечисленных выше политиках) или небольшое содержимое будет заблокировано.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: RunAllFlashInAllowMode
  - Имя групповой политики: Расширить настройку содержимого Adobe Flash на все содержимое
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: RunAllFlashInAllowMode
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: RunAllFlashInAllowMode
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SSLErrorOverrideAllowed
  #### Разрешить пользователям продолжать работу со страницы предупреждения HTTPS
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Microsoft Edge отображает страницу предупреждения, когда пользователь переходит на сайты, содержащие ошибки SSL.

Если включить или не настроить (по умолчанию) этот параметр политики, пользователи смогут пропускать такие страницы предупреждений.

Если отключить этот параметр политики, пользователям будет запрещено пропускать страницы предупреждений.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SSLErrorOverrideAllowed
  - Имя групповой политики: Разрешить пользователям продолжать работу со страницы предупреждения HTTPS
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: SSLErrorOverrideAllowed
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SSLErrorOverrideAllowed
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SSLVersionMin
  #### Включена минимальная версия протокола TLS
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определение минимальной поддерживаемой версии SSL. Если этот параметр не настроен, в Microsoft Edge используется минимальная версия по умолчанию — TLS 1.0.

Если этот параметр включен, можно выбрать один из следующих вариантов минимальной версии:'TLSv1', 'TLSv1.1' или 'TLSv1.2'. Если этот параметр настроен, Microsoft Edge не использует версии SSL/TLS ниже заданной. Все нераспознанные значения игнорируются.

Сопоставление параметров политики:

* TLSv1 (tls1) = TLS 1.0

* TLSv1.1 (tls1.1) = TLS 1.1

* TLSv1.2 (tls1.2) = TLS 1.2

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SSLVersionMin
  - Имя групповой политики: Включена минимальная версия протокола TLS
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: SSLVersionMin
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"tls1"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SSLVersionMin
  - Пример значения:
``` xml
<string>tls1</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SaveCookiesOnExit
  #### Сохранять файлы cookie при закрытии Microsoft Edge
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 86 или более поздней версии

  #### Описание
  Если эта политика включена, указанный набор файлов cookie исключается из удаления при закрытии браузера. Эта политика действует только в следующих случаях:
— Настроен переключатель "Файлы cookie и другие данные сайтов" в разделе "Настройки/Конфиденциальность и службы/Удалять данные браузера при выходе" или
— Включена политика [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) или
— Политике [DefaultCookiesSetting](#defaultcookiessetting) присвоено значение "Сохранять файлы cookie в течение сеанса".

Вы можете определить список сайтов на основе шаблонов URL-адресов, которые будут сохранять свои файлы cookie в сеансах.

Примечание. Пользователи по-прежнему могут изменять список сайтов с файлами cookie, чтобы добавлять или удалять URL-адреса. Но они не могут удалять URL-адреса, добавленные администратором.

Если включить эту политику, список файлов cookie не будет очищаться при закрытии браузера.

Если эта политика отключена или не настроена, применяется личная настройка пользователя.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SaveCookiesOnExit
  - Имя групповой политики: Сохранять файлы cookie при закрытии Microsoft Edge
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SaveCookiesOnExit
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SavingBrowserHistoryDisabled
  #### Отключить сохранение журнала браузера
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Отключает сохранение журнала браузера и запрещает пользователям изменять эту настройку.

Если эта политика включена, журнал браузера не будет сохраняться. Это действие также отключает синхронизацию вкладок.

Если эта политика отключен или не настроен, журнал браузера сохраняется.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SavingBrowserHistoryDisabled
  - Имя групповой политики: Отключить сохранение журнала браузера
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: SavingBrowserHistoryDisabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SavingBrowserHistoryDisabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ScreenCaptureAllowed
  #### Разрешите или запретите снимок экрана
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 83 или более поздней версии

  #### Описание
  Если эта политика включена или не настроена, веб-страница может использовать API демонстрации экрана (например, getDisplayMedia() или API расширения захвата рабочего стола) для снимков экрана.
Если эта политика отключена, вызовы API демонстрации экрана будут завершаться сбоем. Например, если вы используете собрание по сети, видео или демонстрация экрана не будут работать.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ScreenCaptureAllowed
  - Имя групповой политики: Разрешите или запретите снимок экрана
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ScreenCaptureAllowed
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ScreenCaptureAllowed
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ScrollToTextFragmentEnabled
  #### Разрешить прокрутку до текста, указанного в фрагментах URL-адреса
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 83 или более поздней версии

  #### Описание
  Эта функция позволяет переходам по гиперссылкам и URL-адресам в адресной строке искать определенный текст на веб-странице, к которому будет прокручиваться эта веб-страница после завершения загрузки.

Если включить или не настроить эту политику, прокрутка веб-страницы до определенных фрагментов текста через URL-адрес будет включена.

Если отключить эту политику, прокрутка веб-страницы до определенных фрагментов текста через URL-адрес будет отключена.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ScrollToTextFragmentEnabled
  - Имя групповой политики: Разрешить прокрутку до текста, указанного в фрагментах URL-адреса
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ScrollToTextFragmentEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ScrollToTextFragmentEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SearchSuggestEnabled
  #### Включить варианты поиска
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Использование вариантов запросов для веб-поиска в адресной строке и списке автозаполнения Microsoft Edge без возможности для пользователей изменять этот параметр.

Если данный параметр политики включен, предлагаются варианты запросов для веб-поиска.

Если этот параметр политики отключен, варианты запросов для веб-поиска никогда не предлагаются, однако варианты из локального журнала и избранного будут отображаться. Если этот параметр политики отключен, ни введенные символы, ни посещенные URL-адреса не будут включены в телеметрию, отправляемую в корпорацию Майкрософт.

Если этот параметр политики не задан, варианты поисковых запросов будут предлагаться, но пользователь сможет изменить эту настройку.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SearchSuggestEnabled
  - Имя групповой политики: Включить варианты поиска
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: SearchSuggestEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SearchSuggestEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SecurityKeyPermitAttestation
  #### Веб-сайты и домены, которые не требуют разрешения на использование прямой аттестации ключа безопасности
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определяет веб-сайты и домены, которые не требуют явного разрешения пользователя, когда запрашиваются сертификаты аттестации от ключей безопасности. Кроме того, ключу безопасности отправляется сигнал, указывающий, что он может использовать индивидуальную аттестацию. Без этого пользователи каждый раз получают запрос на аттестацию ключей безопасности.

Сайты (например, https://contoso.com/some/path) сопоставляются только как идентификаторы appID U2F. Домены (например, contoso.com) сопоставляются только как идентификаторы webauthn RP. Чтобы охватить API U2F и webauthn для данного сайта, необходимо указать URL-адрес и домен appID.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SecurityKeyPermitAttestation
  - Имя групповой политики: Веб-сайты и домены, которые не требуют разрешения на использование прямой аттестации ключа безопасности
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation\1 = "https://contoso.com"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SecurityKeyPermitAttestation
  - Пример значения:
``` xml
<array>
  <string>https://contoso.com</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SendIntranetToInternetExplorer
  #### Отправка всех сайтов интрасети в Internet Explorer
  
  
  #### Поддерживаемые версии:
  - На Windows с 77 или более поздней версии

  #### Описание
  Инструкции по настройке оптимального интерфейса режима Internet Explorer см. на странице [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SendIntranetToInternetExplorer
  - Имя групповой политики: Отправка всех сайтов интрасети в Internet Explorer
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: SendIntranetToInternetExplorer
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  

  [В начало](#microsoft-edge:-политики)

  ### SendSiteInfoToImproveServices
  #### Отправлять сведения о сайте для улучшения служб Майкрософт (не рекомендуется)
  >УСТАРЕЛО. Эта политика устарела. В настоящее время она поддерживается, но станет устаревшей в будущем выпуске.
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Эта политика устарела. В настоящее время она поддерживается, но перестанет поддерживаться в Microsoft Edge 89. Эта политика заменяется новой политикой: [DiagnosticData](#diagnosticdata) для Windows 7, Windows 8 и macOS. Эта политика заменяется политикой "Разрешить телеметрию" в Windows 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)).

Эта политика позволяет отправлять информацию о веб-сайтах, посещенных в Microsoft Edge, в Майкрософт для улучшения таких служб, как поиск.

Включите эту политику, чтобы отправлять информацию о веб-сайтах, посещенных в Microsoft Edge, в Майкрософт. Отключите эту политику, чтобы не отправлять информацию о веб-сайтах, посещенных в Microsoft Edge, в Майкрософт. В обоих случаях пользователи не могут изменить или переопределить настройку.

В Windows 10, если вы не настроите эту политику, Microsoft Edge по умолчанию применяет настройку диагностических данных Windows. Если эта политика включена, Microsoft Edge будет отправлять информацию о веб-сайтах, посещенных в Microsoft Edge, только если для параметра диагностических данных Windows установлено значение "Полные". Если эта политика отключена, Microsoft Edge не будет отправлять информацию о посещенных веб-сайтах. Подробнее о параметрах диагностических данных Windows: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

В Windows 7, Windows 8 и macOS эта политика управляет отправкой информации о посещенных веб-сайтах. Если эта политика не настроена, Microsoft Edge будет по умолчанию использовать параметры пользователя.

Чтобы включить эту политику, параметру [MetricsReportingEnabled](#metricsreportingenabled) требуется присвоить значение "Включено". Если политике [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) или [MetricsReportingEnabled](#metricsreportingenabled) присвоено значение "Не настроено" или "Отключено", эти данные не отправляются в корпорацию Майкрософт.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SendSiteInfoToImproveServices
  - Имя групповой политики: Отправлять сведения о сайте для улучшения служб Майкрософт (не рекомендуется)
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: SendSiteInfoToImproveServices
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SendSiteInfoToImproveServices
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SensorsAllowedForUrls
  #### Allow access to sensors on specific sites
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 86 или более поздней версии

  #### Описание
  Define a list of sites, based on URL patterns, that can access and use sensors such as motion and light sensors.

If you don't configure this policy, the global default value from the [DefaultSensorsSetting](#defaultsensorssetting) policy (if set) or the user's personal configuration is used for all sites.

For URL patterns that don't match this policy, the following order of precedence is used: The [SensorsBlockedForUrls](#sensorsblockedforurls) policy (if there is a match), the [DefaultSensorsSetting](#defaultsensorssetting) policy (if set), or the user's personal settings.

The URL patterns defined in this policy can't conflict with those configured in the [SensorsBlockedForUrls](#sensorsblockedforurls) policy. You can't allow and block a URL.

For detailed information about valid URL patterns, please see [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SensorsAllowedForUrls
  - Имя групповой политики: Allow access to sensors on specific sites
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SensorsAllowedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SensorsBlockedForUrls
  #### Block access to sensors on specific sites
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 86 или более поздней версии

  #### Описание
  Define a list of sites, based on URL patterns, that can't access sensors such as motion and light sensors.

If you don't configure this policy, the global default value from the [DefaultSensorsSetting](#defaultsensorssetting) policy (if set) or the user's personal configuration is used for all sites.

For URL patterns that don't match this policy, the following order of precedence is used: The [SensorsAllowedForUrls](#sensorsallowedforurls) policy (if there is a match), the [DefaultSensorsSetting](#defaultsensorssetting) policy (if set), or the user's personal settings.

The URL patterns defined in this policy can't conflict with those configured in the [SensorsAllowedForUrls](#sensorsallowedforurls) policy. You can't allow and block a URL.

For detailed information about valid URL patterns, please see [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SensorsBlockedForUrls
  - Имя групповой политики: Block access to sensors on specific sites
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SensorsBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SerialAskForUrls
  #### Разрешить API Serial на определенных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 86 или более поздней версии

  #### Описание
  На основании шаблонов URL-адресов определите список сайтов, которые могут запрашивать у пользователя доступ к последовательному порту.

Если не настроить эту политику, для всех сайтов будет использоваться стандартное глобальное значение из политики [DefaultSerialGuardSetting](#defaultserialguardsetting) (если настроена) или личная конфигурация пользователя.

Для шаблонов URL-адресов, не соответствующих этой политике, используется следующий порядок приоритета: политика [SerialBlockedForUrls](#serialblockedforurls) (если существует совпадение), политика [DefaultSerialGuardSetting](#defaultserialguardsetting) (если настроена) или личные параметры пользователя.

Шаблоны URL-адресов, определенные в этой политике, не могут конфликтовать с настроенными в политике [SerialBlockedForUrls](#serialblockedforurls). Вы не можете разрешить и заблокировать URL-адрес.

Подробные сведения о допустимых шаблонах URL-адресов см. на странице [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SerialAskForUrls
  - Имя групповой политики: Разрешить API Serial на определенных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SerialAskForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SerialBlockedForUrls
  #### Блокировать API Serial на определенных сайтах
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 86 или более поздней версии

  #### Описание
  На основании шаблонов URL-адресов определите список сайтов, которые не могут запрашивать у пользователя предоставление доступа к последовательному порту.

Если не настроить эту политику, для всех сайтов будет использоваться стандартное глобальное значение из политики [DefaultSerialGuardSetting](#defaultserialguardsetting) (если настроена) или личная конфигурация пользователя.

Для шаблонов URL-адресов, не соответствующих этой политике, используется следующий порядок приоритета: политика [SerialAskForUrls](#serialaskforurls) (если существует совпадение), политика [DefaultSerialGuardSetting](#defaultserialguardsetting) (если настроена) или личные параметры пользователя.

Шаблоны URL-адресов в этой политике не могут конфликтовать с настроенными в политике [SerialAskForUrls](#serialaskforurls). Вы не можете разрешить и заблокировать URL-адрес.

Подробные сведения о допустимых шаблонах URL-адресов см. на странице [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SerialBlockedForUrls
  - Имя групповой политики: Блокировать API Serial на определенных сайтах
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SerialBlockedForUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### ShowOfficeShortcutInFavoritesBar
  #### Показать ярлык Microsoft Office на панели "Избранное"
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Отображение ярлыка для Office.com на панели "Избранное". Пользователи, выполнившие вход в Microsoft Edge, могут через этот ярлык переходить к документам и приложениям Microsoft Office.

Если этот параметр политики включен или не настроен, пользователи могут отобразить или скрыть этот ярлык, изменив положение переключателя в контекстном меню панели избранного.

Если этот параметр политики отключен, ярлык не отображается.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: ShowOfficeShortcutInFavoritesBar
  - Имя групповой политики: Показать ярлык Microsoft Office на панели "Избранное"
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: ShowOfficeShortcutInFavoritesBar
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: ShowOfficeShortcutInFavoritesBar
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SignedHTTPExchangeEnabled
  #### Включить поддержку подписи HTTP exchange (SXG)
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 78 или более поздней версии

  #### Описание
  Поддержка подписанных пакетов обмена по HTTP (SXG).

Если этот параметр политики не задан или включен, Microsoft Edge принимает веб-содержимое, представленное в виде подписанных пакетов обмена по HTTP.

Если этот параметр политики отключен, подписанные пакеты обмена по HTTP не загружаются.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SignedHTTPExchangeEnabled
  - Имя групповой политики: Включить поддержку подписи HTTP exchange (SXG)
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: SignedHTTPExchangeEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SignedHTTPExchangeEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SitePerProcess
  #### Включить изоляцию для каждого сайта
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Политика SitePerProcess позволяет запретить пользователям блокировать стандартные настройки, касающиеся изоляции всех сайтов. Обратите внимание: вы также можете использовать политику [IsolateOrigins](#isolateorigins), чтобы изолировать дополнительные, более точно выбранные источники.
Если данный параметр включен, пользователи не могут отключать стандартные настройки, при которых каждый сайт выполняет собственный процесс.
Если данный параметр выключен или не настроен, пользователи могут отключать изоляцию сайтов. (Например, с помощью записи "Отключить изоляцию сайта" в edge://flags.) Если выключить или не настроить данный параметр, это не приведет к выключению функции "Изоляция сайта".

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SitePerProcess
  - Имя групповой политики: Включить изоляцию для каждого сайта
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: SitePerProcess
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SitePerProcess
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SpellcheckEnabled
  #### Включить проверку орфографии
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Если включить или не настроить эту политику, пользователи смогут использовать проверку орфографии.

Если отключить этот параметр политики, пользователи не смогут использовать проверку орфографии и политики [SpellcheckLanguage](#spellchecklanguage) и [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) также будут отключены.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SpellcheckEnabled
  - Имя групповой политики: Включить проверку орфографии
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: SpellcheckEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SpellcheckEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SpellcheckLanguage
  #### Включить конкретные языки проверки орфографии
  
  
  #### Поддерживаемые версии:
  - На Windows с 77 или более поздней версии

  #### Описание
  Проверка орфографии для разных языков. Любой выбранный язык, который не распознается, игнорируется.

Если данный параметр политики включен, проверка орфографии разрешена для указанных языков, а также всех языков, заданных пользователем.

Если не настроить или отключить этот параметр политики, пользовательские настройки проверки орфографии не меняются.

Если политика [SpellcheckEnabled](#spellcheckenabled) отключена, эта политика не будет действовать.

Если один и тот же язык указан и в политике SpellcheckLanguage и в политике [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist), проверка орфографии для него будет разрешена.

Поддерживаемые языки: af, bg, ca, cs, cy, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SpellcheckLanguage
  - Имя групповой политики: Включить конкретные языки проверки орфографии
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\2 = "es"

```


  

  [В начало](#microsoft-edge:-политики)

  ### SpellcheckLanguageBlocklist
  #### Принудительное отключение языков проверки орфографии
  
  
  #### Поддерживаемые версии:
  - На Windows с 78 или более поздней версии

  #### Описание
  Принудительное отключение проверки орфографии для языков. Нераспознанные языки из этого списка пропускаются.

Если этот параметр политики включен, проверка орфографии отключается для указанных языков. Пользователь при этом может включить или выключить проверку орфографии для языков, не включенных в список.

Если этот параметр политики выключен или не настроен, пользовательские настройки проверки орфографии остаются без изменений.

Если параметр [SpellcheckEnabled](#spellcheckenabled) выключен, данный параметр политики не действует.

Если один и тот же язык указан и в политике [SpellcheckLanguage](#spellchecklanguage), и в политике SpellcheckLanguageBlocklist, проверка орфографии для него будет разрешена.

В настоящее время поддерживаются следующие языки: af, bg, ca, cs, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SpellcheckLanguageBlocklist
  - Имя групповой политики: Принудительное отключение языков проверки орфографии
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\2 = "es"

```


  

  [В начало](#microsoft-edge:-политики)

  ### StricterMixedContentTreatmentEnabled
  #### Включить более строгую обработку для смешанного содержимого (не рекомендуется)
  >УСТАРЕЛО. Эта политика устарела. В настоящее время она поддерживается, но станет устаревшей в будущем выпуске.
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 81 или более поздней версии

  #### Описание
  Применение этой политики не рекомендуется. Она предназначена для использования только в качестве краткосрочного механизма, чтобы дать предприятиям больше времени на обновление своего веб-контента, если окажется, что он несовместим с более строгими требованиями обработки смешанного контента. Она не будет работать в Microsoft Edge версии 85.

Эта политика управляет обработкой смешанного контента (контент HTTP на сайтах HTTPS) в браузере.

Если для этой политики задано значение true или она не настроена, смешанный контент из аудио- и видеофайлов будет автоматически обновлен до HTTPS (т. е. URL-адрес будет переписан в формате HTTPS без резерва, если ресурс недоступен по протоколу HTTPS) и в строке URL-адреса для смешанного контента изображений будет отображаться предупреждение "Не защищено".

Если задать значение политики как false, то автоматическое обновление для аудио- и видеофайлов будет отключено, а для изображений не будет выводится предупреждение.

Эта политика не влияет на другие типы смешанного контента, кроме аудио, видео и изображений.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: StricterMixedContentTreatmentEnabled
  - Имя групповой политики: Включить более строгую обработку для смешанного содержимого (не рекомендуется)
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: StricterMixedContentTreatmentEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: StricterMixedContentTreatmentEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SuppressUnsupportedOSWarning
  #### Отключить предупреждение о неподдерживаемой ОС
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Предупреждение, которое появляется при работе Microsoft Edge на компьютере или в операционной системе с прекратившейся поддержкой, подавляется.

Если политике присвоено значение false или она не задана, предупреждения появляются на таких неподдерживаемых компьютерах или в таких неподдерживаемых операционных системах.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SuppressUnsupportedOSWarning
  - Имя групповой политики: Отключить предупреждение о неподдерживаемой ОС
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: SuppressUnsupportedOSWarning
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SuppressUnsupportedOSWarning
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SyncDisabled
  #### Отключить синхронизацию данных с помощью служб синхронизации Майкрософт
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Отключает синхронизацию данных в Microsoft Edge. Этот параметр политики также запрещает отображение запроса на подтверждение синхронизации.

Если не настроить эту политику или применить ее как рекомендованную, пользователи смогут включать и выключать синхронизацию. Если эта политика применена как обязательная, пользователи не смогут включить синхронизацию.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SyncDisabled
  - Имя групповой политики: Отключить синхронизацию данных с помощью служб синхронизации Майкрософт
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: SyncDisabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SyncDisabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### SyncTypesListDisabled
  #### Настройка списка типов, исключенных из синхронизации
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 83 или более поздней версии

  #### Описание
  Если включить эту политику, все указанные типы данных будут исключены из синхронизации. С помощью этой политики можно ограничить тип данных, отправляемых в службу синхронизации Microsoft Edge.

Для этой политики можно выбрать один из следующих типов данных: "favorites", "settings", "passwords", "addressesAndMore", "extensions", "history", "openTabs" и "collections". Обратите внимание, что эти названия типов данных указываются с учетом регистра.

Пользователи не смогут переопределить отключенные типы данных.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: SyncTypesListDisabled
  - Имя групповой политики: Настройка списка типов, исключенных из синхронизации
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled\1 = "favorites"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: SyncTypesListDisabled
  - Пример значения:
``` xml
<array>
  <string>favorites</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### TLS13HardeningForLocalAnchorsEnabled
  #### Включить функцию безопасности TLS 1.3 для локальных якорей доверия. (устарела)
  
  >УСТАРЕВШАЯ: эта политика устарела. Она не действует в версиях Microsoft Edge, следующих за версией 85.
  #### Поддерживаемые версии:
  - На Windows и macOS с 81 до 85

  #### Описание
  Эта политика не работает, так как она была предназначена только для краткосрочного механизма, чтобы дать предприятиям больше времени для обновления затронутых прокси-серверов.

Эта политика управляет функцией безопасности TLS 1.3, защищающей подключения от атак через понижение версии. Эта политика поддерживает обратную совместимость и не повлияет на подключения к серверам и прокси-серверам, поддерживающим TLS 1.2. Тем не менее, в более старых версиях некоторых прокси-серверов с перехватом TLS есть ошибка реализации, из-за которой они несовместимы.

Если включить эту политику или не настраивать ее, Microsoft Edge включит защиту для всех подключений.

Если отключить эту политику, Microsoft Edge отключит эту защиту для подключений, проверка подлинности которых выполнена с помощью сертификатов ЦС, установленных локально. Эта защита всегда включена для подключений, проверка подлинности которых выполнена с помощью общедоступных доверенных сертификатов ЦС.

Эту политику можно использовать для тестирования всех затронутых прокси-серверов и их обновления. Затронутые прокси-серверы будут выдавать ошибки подключения с кодом ошибки ERR_TLS13_DOWNGRADE_DETECTED.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: TLS13HardeningForLocalAnchorsEnabled
  - Имя групповой политики: Включить функцию безопасности TLS 1.3 для локальных якорей доверия. (устарела)
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: TLS13HardeningForLocalAnchorsEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: TLS13HardeningForLocalAnchorsEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### TLSCipherSuiteDenyList
  #### Укажите комплекты шифров TLS для отключения
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 85 или более поздней версии

  #### Описание
  Настройте список комплектов шифров, которые отключены для TLS-подключений.

Если вы настроите эту политику, при создании TLS-подключений не будет использоваться список настроенных комплектов шифров.

Если вы не настроите эту политику, браузер выберет комплекты шифров TLS для использования.

Значения комплектов шифров, подлежащие отключению, указываются как 16-разрядные шестнадцатеричные значения. Значения назначаются регистратором IANA (полномочный орган по цифровым адресам в Интернете).

Для TLS 1.3 требуется комплект шифров TLS_AES_128_GCM_SHA256 (0x1301), который не может быть отключен этой политикой.

Эта политика не влияет на подключения QUIC. QUIC можно отключить с помощью политики [QuicAllowed](#quicallowed).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: TLSCipherSuiteDenyList
  - Имя групповой политики: Укажите комплекты шифров TLS для отключения
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\1 = "0x1303"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\2 = "0xcca8"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\3 = "0xcca9"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: TLSCipherSuiteDenyList
  - Пример значения:
``` xml
<array>
  <string>0x1303</string>
  <string>0xcca8</string>
  <string>0xcca9</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### TabFreezingEnabled
  #### Разрешить блокировку работы фоновых вкладок
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 79 или более поздней версии

  #### Описание
  Определяет, может ли Microsoft Edge блокировать работу вкладок, которые находятся в фоновом режиме не менее 5 минут.

Блокировка работы вкладок позволяет уменьшить использование ЦП, аккумулятора и памяти. Microsoft Edge использует эвристику, чтобы не блокировать работу вкладок, которые выполняют полезные процессы в фоновом режиме (например, отображают уведомления, воспроизводят звук и передают в потоковом режиме видео).

Если эта политика включена или не настроена, работа вкладок, которые находятся в фоновом режиме не менее 5 минут, может быть заблокирована.

Если эта политика отключена, работа вкладок не будет блокироваться.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: TabFreezingEnabled
  - Имя групповой политики: Разрешить блокировку работы фоновых вкладок
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: TabFreezingEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: TabFreezingEnabled
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### TaskManagerEndProcessEnabled
  #### Включить завершение процессов в диспетчере задач браузера
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Если включить или не настроить этот параметр политики, пользователи смогут завершать процессы в диспетчере задач браузера. Если отключить его, пользователи не смогут завершать процессы, и кнопка "Завершить процесс" будет отключена в диспетчере задач браузера.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: TaskManagerEndProcessEnabled
  - Имя групповой политики: Включить завершение процессов в диспетчере задач браузера
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: TaskManagerEndProcessEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: TaskManagerEndProcessEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### TotalMemoryLimitMb
  #### Установка ограничения объема памяти (в мегабайтах), который может использовать один экземпляр Microsoft Edge.
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 80 или более поздней версии

  #### Описание
  Задает объем памяти, который может использовать один экземпляр Microsoft Edge до того, как начнет сбрасывать вкладки, чтобы освободить память. Память, используемая вкладкой, будет освобождена. Вкладку необходимо будет перезагрузить при переключении на нее.

Если данный параметр политики включен, при достижении ограничения браузер начнет сбрасывать вкладки, чтобы освободить память. Тем не менее, нет гарантии того, что браузер всегда будет работать в соответствии с этим ограничением. Любое значение меньше 1024 округляется до 1024.

Если не настроить этот параметр политики, браузер будет пытаться сэкономить память только при обнаружении нехватки физической памяти компьютера.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: TotalMemoryLimitMb
  - Имя групповой политики: Установка ограничения объема памяти (в мегабайтах), который может использовать один экземпляр Microsoft Edge.
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: TotalMemoryLimitMb
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000800
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: TotalMemoryLimitMb
  - Пример значения:
``` xml
<integer>2048</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### TrackingPrevention
  #### Блокировка отслеживания просмотренных веб-страниц
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 78 или более поздней версии

  #### Описание
  Позволяет решить, следует ли блокировать на веб-сайте отслеживание действий пользователей в Интернете.

Если вы отключите или не настроите эту политику, пользователи смогут установить собственный уровень предотвращения отслеживания.

Сопоставление параметров политики:

* TrackingPreventionOff (0) = Выкл. (без блокировки отслеживания)

* TrackingPreventionBasic (1) = Базовый уровень (блокируются вредоносные средства отслеживания, при этом содержимое и рекламные объявления персонализируются)

* TrackingPreventionBalanced (2) = Уравновешенный уровень (блокируются вредоносные средства отслеживания, а также средства отслеживания на сайтах, которые пользователь не посещал, при этом содержимое и рекламные объявления персонализируются в меньшей мере)

* TrackingPreventionStrict (3) = Строгий уровень (блокируются вредоносные средства отслеживания, а также большинство остальных средств отслеживания на всех сайтах; при этом содержимое и рекламные объявления персонализируются в минимальной степени, а некоторые компоненты сайтов могут не работать)

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: TrackingPrevention
  - Имя групповой политики: Блокировка отслеживания просмотренных веб-страниц
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: TrackingPrevention
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000002
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: TrackingPrevention
  - Пример значения:
``` xml
<integer>2</integer>
```
  

  [В начало](#microsoft-edge:-политики)

  ### TranslateEnabled
  #### Включить перевод
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Включение встроенной службы перевода (Майкрософт) в Microsoft Edge.

Если данный параметр политики включен, Microsoft Edge предлагает пользователю функции перевода в собственном всплывающем меню (если доступно) и в контекстном меню правой кнопки мыши.

Если данный параметр политики отключен, все встроенные функции перевода выключены.

Если этот параметр политики не настроен, пользователи могут сами решить, использовать функции перевода или нет.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Да
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: TranslateEnabled
  - Имя групповой политики: Включить перевод
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Административные шаблоны/Microsoft Edge - Настройки по умолчанию (пользователи могут переопределять)/
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): SOFTWARE\Policies\Microsoft\Edge\Рекомендовано
  - Имя значения: TranslateEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: TranslateEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### URLAllowlist
  #### Определить список разрешенных URL-адресов
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Настройка списка разрешенных URL-адресов как исключений из списка заблокированных.

Используйте формат шаблона URL-адреса, описанный на странице [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Этот параметр политики можно использовать для создания исключений из ограничительных списков блокировки. Например, вы можете включить "*" в список заблокированных адресов, чтобы блокировать все запросы, а затем использовать этот параметр политики, чтобы разрешить доступ к ограниченному списку URL-адресов. С помощью этого параметра можно создавать исключения для различных схем, поддоменов других доменов, портов или конкретных путей.

Самый точный фильтр определяет, заблокирован или разрешен URL-адрес. Список разрешенных URL-адресов имеет более высокий приоритет, чем список заблокированных.

Этот параметр политики допускает максимум 1000 записей; последующие записи игнорируются.

Этот параметр политики также позволяет браузеру автоматически вызывать внешние приложения, зарегистрированные как обработчики таких протоколов, как "tel:" или "ssh:".

Если не настроить этот параметр, исключений из заблокированных адресов, заданных в политике [URLBlocklist](#urlblocklist), не будет.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: URLAllowlist
  - Имя групповой политики: Определить список разрешенных URL-адресов
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\URLAllowlist
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\5 = ".exact.hostname.com"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: URLAllowlist
  - Пример значения:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### URLBlocklist
  #### Запретить доступ к списку URL-адресов
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  На основании шаблонов URL-адресов определите список сайтов, которые блокируются (ваши пользователи не смогут загружать их).

Используйте формат шаблона URL-адреса, описанный на странице [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322).

Вы можете определить исключения в политике [URLAllowlist](#urlallowlist). Этики политики ограничены 1 000 записей; последующие записи игнорируются.

Обратите внимание, что блокировать внутренние URL-адреса "edge://*" не рекомендуется. Это может привести к непредвиденным ошибкам.

Эта политика не запрещает динамическое обновление страницы с помощью скриптов JavaScript. Например, если вы заблокируете "contoso.com/abc", пользователи по-прежнему смогут переходить на "contoso.com" и нажимать ссылку, чтобы перейти на страницу "contoso.com/abc", пока страница не обновится.

Если не настроить этот параметр политики, URL-адреса не будут блокироваться.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: URLBlocklist
  - Имя групповой политики: Запретить доступ к списку URL-адресов
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\URLBlocklist
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
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


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: URLBlocklist
  - Пример значения:
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
  

  [В начало](#microsoft-edge:-политики)

  ### UserAgentClientHintsEnabled
  #### Включение функции подсказок клиента агента-пользователя (не рекомендуется)
  >УСТАРЕЛО. Эта политика устарела. В настоящее время она поддерживается, но станет устаревшей в будущем выпуске.
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 86 или более поздней версии

  #### Описание
  Поддержка этой политики прекращена, так как она предназначена только для краткосрочного механизма, чтобы дать предприятиям больше времени для обновления своего веб-содержимого, несовместимого с функцией подсказок клиента агента-пользователя. Она не работает в Microsoft Edge версии 89.

Если она включена, функция подсказок клиента агента-пользователя отправляет заголовки фрагментарных запросов, предоставляющие сведения о пользовательском браузере (например, версию браузера) и среде (например, системную архитектуру).

Это аддитивная функция, но новые заголовки могут прерывать некоторые веб-сайты, которые ограничивают допустимые символы в запросах.

Если включить или не настроить эту политику, функция подсказок клиента агента-пользователя будет включена. Если отключить эту политику, эта функция будет недоступна.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: UserAgentClientHintsEnabled
  - Имя групповой политики: Включение функции подсказок клиента агента-пользователя (не рекомендуется)
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: UserAgentClientHintsEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: UserAgentClientHintsEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### UserDataDir
  #### Задать каталог данных пользователя
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Определение каталога для сохранения пользовательских данных.

Если включить этот параметр политики, Microsoft Edge будет использовать заданный каталог независимо от того, указал ли пользователь флаг командной строки "--user-data-dir".

Если не включить этот параметр политики, будет использоваться путь к профилю по умолчанию и пользователь сможет переопределить его с помощью флага "--user-data-dir". Каталог для профиля можно найти на странице edge://version/ в разделе пути к профилю.

Чтобы избежать потери данных или других ошибок, не настраивайте этот параметр политики для корневого каталога тома или для каталога, который используется для других целей, так как Microsoft Edge управляет его содержимым.

Список переменных, которые можно использовать, см. на странице [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041).

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: UserDataDir
  - Имя групповой политики: Задать каталог данных пользователя
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: UserDataDir
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"${users}/${user_name}/Edge"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: UserDataDir
  - Пример значения:
``` xml
<string>${users}/${user_name}/Edge</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### UserDataSnapshotRetentionLimit
  #### Ограничивает количество снимков данных пользователя, сохраняемых для использования в случае экстренного отката
  
  
  #### Поддерживаемые версии:
  - На Windows с 86 или более поздней версии

  #### Описание
  После каждого обновления основного номера версии Microsoft Edge создаст моментальный снимок компонентов данных браузера пользователя для использования в дальнейшем в случае экстренного реагирования, которое требует временного отката версии. При выполнении временного отката к версии, для которой у пользователя есть соответствующий снимок, данные на снимке будут восстановлены. Это позволяет пользователям сохранять такие параметры, как закладки и данные автозаполнения.

Если не настроить этот параметр политики, будет использоваться значение по умолчанию (3 моментальных снимка).

Если настроить этот параметр политики, старые снимки будут удалены в соответствии с заданным вами ограничением. Если для этого параметра политики задано значение 0, моментальные снимки не делаются.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Целое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: UserDataSnapshotRetentionLimit
  - Имя групповой политики: Ограничивает количество снимков данных пользователя, сохраняемых для использования в случае экстренного отката
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: UserDataSnapshotRetentionLimit
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000003
```


  

  [В начало](#microsoft-edge:-политики)

  ### UserFeedbackAllowed
  #### Разрешить отзывы пользователей
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  В Microsoft Edge доступна функция отправки отзывов об Edge (по умолчанию включена), с помощью которой пользователи могут отправлять отзывы, предложения или заполненные опросы клиентов и сообщать обо всех проблемах с браузером. По умолчанию пользователи не могут отключить функцию отзывов об Edge.

Если этот параметр включен или не настроен, пользователи могут вызвать функцию отзывов об Edge.

Если этот параметр политики отключен, пользователи не могут вызвать функцию отзывов об Edge.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: UserFeedbackAllowed
  - Имя групповой политики: Разрешить отзывы пользователей
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: UserFeedbackAllowed
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: UserFeedbackAllowed
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### VideoCaptureAllowed
  #### Разрешить или запретить запись видео
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Управление возможностью сайтов записывать видео.

Если этот параметр политики включен или не задан (по умолчанию), пользователь будет получать запрос на доступ к видеозаписи для всех сайтов за исключением сайтов с URL-адресами, настроенными в списке политики [VideoCaptureAllowedUrls](#videocaptureallowedurls), которым будет разрешен доступ без запроса.

Если этот параметр политики отключен, то пользователь не будет получать запрос и видеозапись будет доступна только для сайтов с URL-адресами, настроенными в политике [VideoCaptureAllowedUrls](#videocaptureallowedurls).

Этот параметр политики влияет на все типы входящих видеоданных, а не только на встроенную камеру.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: VideoCaptureAllowed
  - Имя групповой политики: Разрешить или запретить запись видео
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: VideoCaptureAllowed
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000000
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: VideoCaptureAllowed
  - Пример значения:
``` xml
<false/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### VideoCaptureAllowedUrls
  #### Сайты, которые могут получать доступ к устройствам записи видео без запроса разрешения
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  На основании шаблонов URL-адресов укажите веб-сайты, которые могут использовать устройства записи видео, без запроса разрешения пользователя. Шаблоны в этом списке сопоставляются с источником безопасности запрашивающего URL-адреса. Если они совпадают, сайту автоматически предоставляется доступ к устройствам записи видео.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: VideoCaptureAllowedUrls
  - Имя групповой политики: Сайты, которые могут получать доступ к устройствам записи видео без запроса разрешения
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: VideoCaptureAllowedUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### WPADQuickCheckEnabled
  #### Настроить оптимизацию WPAD
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Оптимизация WPAD (Web Proxy Auto-Discovery) в Microsoft Edge.

Если отключить эту политику, оптимизация WPAD будет отключена, из-за чего браузеру придется дольше ожидать отклика DNS-серверов WPAD.

Если включить или не настроить эту политику, оптимизация WPAD будет включена.

Независимо от того, включена ли эта политика и каким образом, пользователи не могут изменять настройку оптимизации WPAD.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: WPADQuickCheckEnabled
  - Имя групповой политики: Настроить оптимизацию WPAD
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: WPADQuickCheckEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: WPADQuickCheckEnabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### WebAppInstallForceList
  #### Настройка списка принудительно установленных веб-приложений
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 80 или более поздней версии

  #### Описание
  Здесь задается список веб-сайтов, которые устанавливаются автоматически (без участи пользователя) и которые пользователь не может удалить или отключить.

Каждый элемент списка является объектом с указанными далее членами:
  - "url", используется как обязательный член. "url" должен представлять собой URL-адрес веб-приложения, которое необходимо установить.

Дополнительные члены:
  - "launch_container" должен представлять собой параметр "window" или "tab", чтобы указать, как веб-приложение будет открыто после установки.
  - "create_desktop_shortcut" должен иметь значение "true", если требуется создать ярлык рабочего стола в Windows.

Если опустить параметр "default_launch_container", приложение по умолчанию будет открываться во вкладке. Независимо от значения параметра "default_launch_container", пользователи могут изменить контейнер, в котором будет открываться приложение. Если опустить параметр "create_desktop_shortcuts", ярлыки на рабочем столе не будут создаваться.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Да

  #### Тип данных:
  - Словарь

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: WebAppInstallForceList
  - Имя групповой политики: Настройка списка принудительно установленных веб-приложений
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: WebAppInstallForceList
  - Тип значения: REG_SZ
  ##### Пример значения:
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


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: WebAppInstallForceList
  - Пример значения:
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
  

  [В начало](#microsoft-edge:-политики)

  ### WebComponentsV0Enabled
  #### Повторно включить API веб-компонентов v0 до версии M84 (устарела)
  
  >УСТАРЕВШАЯ: эта политика устарела. Она не действует в версиях Microsoft Edge, следующих за версией 84.
  #### Поддерживаемые версии:
  - На Windows и macOS с 80 до 84

  #### Описание
  Эта политика не работает. Согласно этой политике, компоненты можно было выборочно включать повторно до Microsoft Edge версии 85. API веб-компонентов v0 (Shadow DOM v0, Custom Elements v0 и HTML импорт) с 2018 г. были переведены в статус нерекомендуемых и были отключены по умолчанию, начиная с Microsoft Edge версии 80.

Если для этой политики задано значение True, функции веб-компонентов v0 будут включены для всех сайтов.

Если для этой политики задано значение False или она не настроена, по умолчанию функции веб-компонентов v0 будут отключены, начиная с Microsoft Edge версии 80.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: WebComponentsV0Enabled
  - Имя групповой политики: Повторно включить API веб-компонентов v0 до версии M84 (устарела)
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: WebComponentsV0Enabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: WebComponentsV0Enabled
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### WebDriverOverridesIncompatiblePolicies
  #### Разрешить WebDriver переопределять несовместимые политики (устарела)
  
  >УСТАРЕВШАЯ: эта политика устарела. Она не действует в версиях Microsoft Edge, следующих за версией 84.
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 до 84

  #### Описание
  Эта политика не работает, поскольку WebDriver совместим со всеми существующими политиками.

Эта политика позволяет пользователям функции WebDriver переопределять
политики, способные помешать этой операции.

В настоящее время эта политика отключает политики [SitePerProcess](#siteperprocess) и [IsolateOrigins](#isolateorigins).

Если эта политика включена, WebDriver сможет переопределять несовместимые
политики.
Если эта политика отключена или не настроена, функции WebDriver не будет разрешено
переопределять несовместимые политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: WebDriverOverridesIncompatiblePolicies
  - Имя групповой политики: Разрешить WebDriver переопределять несовместимые политики (устарела)
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: WebDriverOverridesIncompatiblePolicies
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: WebDriverOverridesIncompatiblePolicies
  - Пример значения:
``` xml
<true/>
```
  

  [В начало](#microsoft-edge:-политики)

  ### WebRtcLocalIpsAllowedUrls
  #### Управление раскрытием локальных IP-адресов с помощью WebRTC
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 80 или более поздней версии

  #### Описание
  Этот параметр политики позволяет указать список источников (URL-адреса) или шаблонов имен узлов (например, "*.contoso.com*"), для которых локальный IP-адрес должен предоставляться WebRTC.

Если этот параметр политики включен и задан список источников (URL-адресов) или шаблонов имен узлов, то при включенном параметре edge://flags/#enable-webrtc-hide-local-ips-with-mdns, WebRTC предоставляет локальный IP-адрес для случаев, соответствующих шаблонам в списке.

Если этот параметр политики отключен или не настроен, а параметр edge://flags/#enable-webrtc-hide-local-ips-with-mdns включен, WebRTC не будет представлять локальные IP-адреса. Локальный IP-адрес будет скрыт с помощью имени узла mDNS.

Если включить, отключить или не настроить этот параметр политики и отключить параметр edge://flags/#enable-webrtc-hide-local-ips-with-mdns, WebRTC будет предоставлять локальные IP-адреса.

Обратите внимание, что эта политика ослабляет защиту локальных IP-адресов, которые могут потребоваться администраторам.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Список строк

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: WebRtcLocalIpsAllowedUrls
  - Имя групповой политики: Управление раскрытием локальных IP-адресов с помощью WebRTC
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls
  - Путь (Рекомендовано): Н/Д
  - Имя значения: 1, 2, 3, ...
  - Тип значения: Список REG_SZ
  ##### Пример значения:
```
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\2 = "*contoso.com*"

```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: WebRtcLocalIpsAllowedUrls
  - Пример значения:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>*contoso.com*</string>
</array>
```
  

  [В начало](#microsoft-edge:-политики)

  ### WebRtcLocalhostIpHandling
  #### Ограничить раскрытие локального IP-адреса с помощью WebRTC
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Позволяет указать, будет ли WebRTC предоставлять доступ к локальному IP-адресу пользователя.

Если для этого параметра задано значение "AllowAllInterfaces" или "AllowPublicAndPrivateInterfaces", WebRTC дает доступ к локальному IP-адресу.

Если для этого параметра задано значение "AllowPublicInterfaceOnly" или "DisableNonProxiedUdp", WebRTC не дает доступ к локальному IP-адресу.

Если не настроить эту политику или отключить ее, WebRTC дает доступ к локальному IP-адресу.

Сопоставление параметров политики:

* AllowAllInterfaces (default) = Разрешить все интерфейсы. Это значение предоставляет локальный IP-адрес

* AllowPublicAndPrivateInterfaces (default_public_and_private_interfaces) = Разрешить открытые и закрытые интерфейсы по маршруту HTTP по умолчанию. Это значение предоставляет локальный IP-адрес

* AllowPublicInterfaceOnly (default_public_interface_only) = Разрешить общий интерфейс по маршруту HTTP по умолчанию. Это значение не предоставляет локальный IP-адрес

* DisableNonProxiedUdp (disable_non_proxied_udp) = Использовать TCP, если прокси-сервер не поддерживает UDP. Это значение не предоставляет локальный IP-адрес

Используйте предоставленную выше информацию при настройке этой политики.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: WebRtcLocalhostIpHandling
  - Имя групповой политики: Ограничить раскрытие локального IP-адреса с помощью WebRTC
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: WebRtcLocalhostIpHandling
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"default"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: WebRtcLocalhostIpHandling
  - Пример значения:
``` xml
<string>default</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### WebRtcUdpPortRange
  #### Ограничить диапазон локальных UDP-портов, используемых WebRTC
  
  
  #### Поддерживаемые версии:
  - На Windows и macOS с 77 или более поздней версии

  #### Описание
  Эта политика ограничивает диапазон UDP-портов, используемый WebRTC, до заданного интервала портов (включая конечные точки).

Настраивая эту политику вы указываете диапазон локальных UDP-портов, которые может использовать WebRTC.

Если вы не настроите эту политику, а также если укажете для нее пустую строку или недопустимый диапазон портов, WebRTC сможет использовать любой доступный локальный порт UDP.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Строковое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: WebRtcUdpPortRange
  - Имя групповой политики: Ограничить диапазон локальных UDP-портов, используемых WebRTC
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: WebRtcUdpPortRange
  - Тип значения: REG_SZ
  ##### Пример значения:
```
"10000-11999"
```


  #### Сведения и настройки Mac
  - Имя предпочтительного ключа: WebRtcUdpPortRange
  - Пример значения:
``` xml
<string>10000-11999</string>
```
  

  [В начало](#microsoft-edge:-политики)

  ### WinHttpProxyResolverEnabled
  #### Использование сопоставителя прокси-серверов Windows (не рекомендуется)
  >УСТАРЕЛО. Эта политика устарела. В настоящее время она поддерживается, но станет устаревшей в будущем выпуске.
  
  #### Поддерживаемые версии:
  - На Windows с 84 или более поздней версии

  #### Описание
  Применение этой политики не рекомендуется. Она будет заменена аналогичным компонентом в будущих выпусках. см. https://crbug.com/644030.

Использование Windows для сопоставления прокси-серверов во всех сетевых подключениях браузера вместо средства сопоставления прокси-серверов, встроенного в Microsoft Edge. Средство сопоставления прокси-серверов Windows разрешает такие функции прокси-сервера Windows, как DirectAccess/NRPT.

В этой политике имеются проблемы, описанные в https://crbug.com/1032820. Она приводит к извлечению файлов сертификата атрибута привилегий (PAC) и их выполнению кодом Windows, включая PAC-файлы, заданные с помощью политики [ProxyPacUrl](#proxypacurl). Так как получение из сети PAC-файла производится через Windows, а не через код Microsoft Edge, то такие сетевые политики, как [DnsOverHttpsMode](#dnsoverhttpsmode), не будут применяться к получению из сети PAC-файла.

Если вы примените эту политику, то будет использоваться средство сопоставления прокси-серверов Windows.

Если отключить или не настраивать эту политику, то будет использоваться средство сопоставления прокси-серверов Microsoft Edge.

  #### Поддерживаемые функции:
  - Может быть обязательной: Да
  - Может быть рекомендованной: Нет
  - Динамическое обновление политики: Нет - Требуется перезапуск браузера

  #### Тип данных:
  - Логическое

  #### Настройки и сведения Windows
  ##### Сведения о групповой политике (ADMX)
  - Уникальное имя групповой политики: WinHttpProxyResolverEnabled
  - Имя групповой политики: Использование сопоставителя прокси-серверов Windows (не рекомендуется)
  - Путь групповой политики (Обязательно): Административные шаблоны/Microsoft Edge/
  - Путь групповой политики (Рекомендовано): Н/Д
  - Имя файла групповой политики ADMX: MSEdge.admx
  ##### Настройки реестра Windows
  - Путь (Обязательно): SOFTWARE\Policies\Microsoft\Edge
  - Путь (Рекомендовано): Н/Д
  - Имя значения: WinHttpProxyResolverEnabled
  - Тип значения: REG_DWORD
  ##### Пример значения:
```
0x00000001
```


  

  [В начало](#microsoft-edge:-политики)


## См. также
- [Настройка Microsoft Edge](configure-microsoft-edge.md)
- [Целевая страница предприятия в Microsoft Edge](https://aka.ms/EdgeEnterprise)
- [Блог базовых планов безопасности Microsoft Security](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)