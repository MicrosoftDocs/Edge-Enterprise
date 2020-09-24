---
title: "Microsoft Edge Browser Policy Documentation"
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 09/24/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom:
description: "Windows and Mac documentation for all policies supported by the Microsoft Edge Browser"
---

# Microsoft Edge - 策略
最新版本的 Microsoft Edge 包括以下策略。你可以使用这些策略配置 Microsoft Edge 在组织中的运行方式。

有关用于控制 Microsoft Edge 的更新方式和时间的其他策略，请查看 [Microsoft Edge 更新策略引用](microsoft-edge-update-policies.md)。

你可以下载 [Microsoft 安全合规性工具包](https://www.microsoft.com/download/details.aspx?id=55319)，以获取建议的 Microsoft Edge 安全配置基准设置。有关更多信息，请参阅 [Microsoft 安全基准博客](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)。

> [!注意]
> 本文适用于 Microsoft Edge 版本 77 或更高版本。

## 可用策略
这些表列出了此版本的 Microsoft Edge 中提供的所有与浏览器相关的组策略。使用表中的链接获取有关特定策略的详细信息。

|||
|-|-|
|[Cast](#cast)|[HTTP 身份验证](#http-身份验证)|
|[Smartscreen 设置](#smartscreen-设置)|[代理服务器](#代理服务器)|
|[内容设置](#内容设置)|[启动、主页和新选项卡页](#启动、主页和新选项卡页)|
|[密码管理器和保护](#密码管理器和保护)|[应用程序防护设置](#应用程序防护设置)|
|[打印](#打印)|[扩展](#扩展)|
|[本机消息](#本机消息)|[默认的搜索提供程序](#默认的搜索提供程序)|
|[Additional](#additional)|

### [*Cast*](#cast-policies)
|策略名称|描述|
|-|-|
|[EnableMediaRouter](#enablemediarouter)|启用 Google Cast|
|[ShowCastIconInToolbar](#showcasticonintoolbar)|在工具栏中显示投放图标|
### [*HTTP 身份验证*](#http-身份验证-policies)
|策略名称|描述|
|-|-|
|[AllowCrossOriginAuthPrompt](#allowcrossoriginauthprompt)|允许跨源 HTTP 基本身份验证提示|
|[AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)|指定 Microsoft Edge 可以将用户凭据委派给的服务器列表|
|[AuthSchemes](#authschemes)|支持的身份验证方案|
|[AuthServerAllowlist](#authserverallowlist)|配置允许的身份验证服务器列表|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|协商 Kerberos 身份验证时禁用 CNAME 查找|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|在 Kerberos SPN 中包含非标准端口|
|[NtlmV2Enabled](#ntlmv2enabled)|控制是否启用 NTLMv2 身份验证|
### [*Smartscreen 设置*](#smartscreen-设置-policies)
|策略名称|描述|
|-|-|
|[PreventSmartScreenPromptOverride](#preventsmartscreenpromptoverride)|阻止绕过 Microsoft Defender SmartScreen 对站点的提示|
|[PreventSmartScreenPromptOverrideForFiles](#preventsmartscreenpromptoverrideforfiles)|阻止绕过有关下载的 Microsoft Defender SmartScreen 警告|
|[SmartScreenAllowListDomains](#smartscreenallowlistdomains)|配置 Microsoft Defender SmartScreen 将不会为其触发警告的域的列表|
|[SmartScreenEnabled](#smartscreenenabled)|配置 Microsoft Defender SmartScreen|
|[SmartScreenForTrustedDownloadsEnabled](#smartscreenfortrusteddownloadsenabled)|强制对来自受信任源的下载执行 Microsoft Defender SmartScreen 检查|
|[SmartScreenPuaEnabled](#smartscreenpuaenabled)|配置 Microsoft Defender SmartScreen 以阻止可能不需要的应用|
### [*代理服务器*](#代理服务器-policies)
|策略名称|描述|
|-|-|
|[ProxyBypassList](#proxybypasslist)|配置代理绕过规则|
|[ProxyMode](#proxymode)|配置代理服务器设置|
|[ProxyPacUrl](#proxypacurl)|设置代理 .pac 文件的 URL|
|[ProxyServer](#proxyserver)|配置代理服务器的地址或 URL|
|[ProxySettings](#proxysettings)|代理服务器设置|
### [*内容设置*](#内容设置-policies)
|策略名称|描述|
|-|-|
|[AutoSelectCertificateForUrls](#autoselectcertificateforurls)|自动为这些站点选择客户端证书|
|[CookiesAllowedForUrls](#cookiesallowedforurls)|在特定站点上允许 Cookie|
|[CookiesBlockedForUrls](#cookiesblockedforurls)|在特定站点上阻止 Cookie|
|[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)|将特定网站的 Cookie 限制为当前会话|
|[DefaultCookiesSetting](#defaultcookiessetting)|配置 Cookie|
|[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)|控制用于读取的文件系统 API 的使用|
|[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)|控制用于编写的文件系统 API 的使用|
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|默认地理位置设置|
|[DefaultImagesSetting](#defaultimagessetting)|默认图像设置|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|控制不安全内容例外的使用|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|默认 JavaScript 设置|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|默认通知设置|
|[DefaultPluginsSetting](#defaultpluginssetting)|默认 Adobe Flash 设置|
|[DefaultPopupsSetting](#defaultpopupssetting)|默认的弹出窗口设置|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|控制 Web 蓝牙 API 的使用|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|控制 WebUSB API 的使用|
|[FileSystemReadAskForUrls](#filesystemreadaskforurls)|在这些网站上允许通过文件系统 API 进行读取访问|
|[FileSystemReadBlockedForUrls](#filesystemreadblockedforurls)|在这些网站上禁止通过文件系统 API 进行读取访问|
|[FileSystemWriteAskForUrls](#filesystemwriteaskforurls)|在这些网站上允许对文件和目录的写入访问|
|[FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls)|在这些网站上阻止对文件和目录的写入访问|
|[ImagesAllowedForUrls](#imagesallowedforurls)|允许使用这些站点上的图像|
|[ImagesBlockedForUrls](#imagesblockedforurls)|在特定站点上阻止图像|
|[InsecureContentAllowedForUrls](#insecurecontentallowedforurls)|对指定站点允许不安全内容|
|[InsecureContentBlockedForUrls](#insecurecontentblockedforurls)|对指定站点阻止不安全内容|
|[JavaScriptAllowedForUrls](#javascriptallowedforurls)|在特定站点上允许 JavaScript|
|[JavaScriptBlockedForUrls](#javascriptblockedforurls)|在特定站点上阻止 JavaScript|
|[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)|启用默认的旧 SameSite cookie 行为设置|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist)|针对指定站点上的 cookie 恢复为旧 SameSite 行为|
|[NotificationsAllowedForUrls](#notificationsallowedforurls)|在特定站点上允许通知|
|[NotificationsBlockedForUrls](#notificationsblockedforurls)|在特定站点上阻止通知|
|[PluginsAllowedForUrls](#pluginsallowedforurls)|允许对特定站点使用 Adobe Flash 插件|
|[PluginsBlockedForUrls](#pluginsblockedforurls)|阻止特定站点上的 Adobe Flash 插件|
|[PopupsAllowedForUrls](#popupsallowedforurls)|在特定站点上允许弹出窗口|
|[PopupsBlockedForUrls](#popupsblockedforurls)|在特定站点上阻止弹出窗口|
|[RegisteredProtocolHandlers](#registeredprotocolhandlers)|注册协议处理程序|
|[SpotlightExperiencesAndRecommendationsEnabled](#spotlightexperiencesandrecommendationsenabled)|选择用户是否可以接收 Microsoft 服务的自定义背景图像和文本、建议、通知、
和提示|
|[WebUsbAllowDevicesForUrls](#webusballowdevicesforurls)|授予特定站点访问权限以连接到特定 USB 设备|
|[WebUsbAskForUrls](#webusbaskforurls)|在特定站点上允许 WebUSB|
|[WebUsbBlockedForUrls](#webusbblockedforurls)|在特定站点上阻止 WebUSB|
### [*启动、主页和新选项卡页*](#启动、主页和新选项卡页-policies)
|策略名称|描述|
|-|-|
|[HomepageIsNewTabPage](#homepageisnewtabpage)|将新标签页设置为主页|
|[HomepageLocation](#homepagelocation)|配置主页 URL|
|[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)|配置允许用于新选项卡页面布局的背景类型|
|[NewTabPageCompanyLogo](#newtabpagecompanylogo)|设置新的选项卡页公司徽标 (过时)|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|从新选项卡页中隐藏默认的热门站点|
|[NewTabPageLocation](#newtabpagelocation)|配置新的选项卡页 URL|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|设置新标签页快速链接|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|启用新标签页的预加载以提高呈现速度|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|配置 Microsoft Edge 新标签页体验|
|[RestoreOnStartup](#restoreonstartup)|要在启动时执行的操作|
|[RestoreOnStartupURLs](#restoreonstartupurls)|浏览器启动时打开的站点|
|[ShowHomeButton](#showhomebutton)|在工具栏上显示“主页”按钮|
### [*密码管理器和保护*](#密码管理器和保护-policies)
|策略名称|描述|
|-|-|
|[PasswordManagerEnabled](#passwordmanagerenabled)|启用将密码保存到密码管理器|
|[PasswordMonitorAllowed](#passwordmonitorallowed)|如果发现用户的密码不安全，则向用户发出警报|
|[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)|配置更改密码 URL|
|[PasswordProtectionLoginURLs](#passwordprotectionloginurls)|配置密码保护服务应捕获密码加盐哈希的企业登录 URL 列表|
|[PasswordProtectionWarningTrigger](#passwordprotectionwarningtrigger)|配置密码保护警告触发器|
### [*应用程序防护设置*](#应用程序防护设置-policies)
|策略名称|描述|
|-|-|
|[ApplicationGuardContainerProxy](#applicationguardcontainerproxy)|应用程序防护容器代理|
### [*打印*](#打印-policies)
|策略名称|描述|
|-|-|
|[DefaultPrinterSelection](#defaultprinterselection)|默认打印机选择规则|
|[PrintHeaderFooter](#printheaderfooter)|打印页眉和页脚|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|将系统的默认打印机设置为默认打印机|
|[PrintingEnabled](#printingenabled)|启用打印|
|[PrintingPaperSizeDefault](#printingpapersizedefault)|默认打印页面大小|
|[UseSystemPrintDialog](#usesystemprintdialog)|使用系统打印对话框打印|
### [*扩展*](#扩展-policies)
|策略名称|描述|
|-|-|
|[ExtensionAllowedTypes](#extensionallowedtypes)|配置允许的扩展类型|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|允许安装特定扩展|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|控制哪些扩展不能安装|
|[ExtensionInstallForcelist](#extensioninstallforcelist)|控制无提示安装的扩展|
|[ExtensionInstallSources](#extensioninstallsources)|配置扩展和用户脚本安装源|
|[ExtensionSettings](#extensionsettings)|配置扩展管理设置|
### [*本机消息*](#本机消息-policies)
|策略名称|描述|
|-|-|
|[NativeMessagingAllowlist](#nativemessagingallowlist)|控制用户可以使用的本机消息传递主机|
|[NativeMessagingBlocklist](#nativemessagingblocklist)|配置本机消息传递阻止名单|
|[NativeMessagingUserLevelHosts](#nativemessaginguserlevelhosts)|允许用户级本机消息传递主机(安装时不带管理员权限)|
### [*默认的搜索提供程序*](#默认的搜索提供程序-policies)
|策略名称|描述|
|-|-|
|[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)|启用默认搜索提供程序|
|[DefaultSearchProviderEncodings](#defaultsearchproviderencodings)|默认的搜索提供程序编码|
|[DefaultSearchProviderImageURL](#defaultsearchproviderimageurl)|为默认搜索提供程序指定“按图像搜索”功能|
|[DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams)|使用 POST 的图像 URL 的参数|
|[DefaultSearchProviderKeyword](#defaultsearchproviderkeyword)|默认的搜索提供程序关键字|
|[DefaultSearchProviderName](#defaultsearchprovidername)|默认的搜索提供程序名称|
|[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)|默认的搜索提供程序搜索 URL|
|[DefaultSearchProviderSuggestURL](#defaultsearchprovidersuggesturl)|建议的默认搜索提供程序 URL|
|[NewTabPageSearchBox](#newtabpagesearchbox)|配置新的选项卡页搜索框体验|
### [*Additional*](#additional-policies)
|策略名称|描述|
|-|-|
|[AddressBarMicrosoftSearchInBingProviderEnabled](#addressbarmicrosoftsearchinbingproviderenabled)|在地址栏中启用必应中的 Microsoft 搜索建议|
|[AdsSettingForIntrusiveAdsSites](#adssettingforintrusiveadssites)|具有干扰性广告的站点的广告设置|
|[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory)|启用删除浏览器和下载历史记录|
|[AllowFileSelectionDialogs](#allowfileselectiondialogs)|允许文件选择对话框|
|[AllowPopupsDuringPageUnload](#allowpopupsduringpageunload)|允许页面在卸载期间显示弹出窗口|
|[AllowSurfGame](#allowsurfgame)|允许冲浪游戏|
|[AllowSyncXHRInPageDismissal](#allowsyncxhrinpagedismissal)|允许页面在关闭过程中发送同步 XHR 请求 (已弃用)|
|[AllowTokenBindingForUrls](#allowtokenbindingforurls)|配置 Microsoft Edge 将尝试为其建立令牌绑定的网站列表。|
|[AllowTrackingForUrls](#allowtrackingforurls)|为特定站点配置跟踪保护例外|
|[AlternateErrorPagesEnabled](#alternateerrorpagesenabled)|找不到网页时建议类似的页面|
|[AlwaysOpenPdfExternally](#alwaysopenpdfexternally)|始终在外部打开 PDF 文件|
|[AmbientAuthenticationInPrivateModesEnabled](#ambientauthenticationinprivatemodesenabled)|针对 InPrivate 和来宾用户配置启用环境身份验证|
|[AppCacheForceEnabled](#appcacheforceenabled)|允许重新启用 AppCache 功能，即使它默认处于关闭状态|
|[ApplicationLocaleValue](#applicationlocalevalue)|设置应用程序的区域设置|
|[AudioCaptureAllowed](#audiocaptureallowed)|允许或阻止音频捕获|
|[AudioCaptureAllowedUrls](#audiocaptureallowedurls)|无需请求许可即可访问音频捕获设备的站点|
|[AudioSandboxEnabled](#audiosandboxenabled)|允许音频沙盒运行|
|[AutoImportAtFirstRun](#autoimportatfirstrun)|首次运行时自动导入其他浏览器的数据和设置|
|[AutoLaunchProtocolsFromOrigins](#autolaunchprotocolsfromorigins)|定义可以在不提示用户的情况下从列出的源启动外部应用程序的协议列表|
|[AutoOpenAllowedForURLs](#autoopenallowedforurls)|AutoOpenFileTypes 可应用的 URL|
|[AutoOpenFileTypes](#autoopenfiletypes)|应在下载时自动打开的文件类型列表|
|[AutofillAddressEnabled](#autofilladdressenabled)|启用地址自动填充|
|[AutofillCreditCardEnabled](#autofillcreditcardenabled)|启用信用卡的自动填充功能|
|[AutoplayAllowed](#autoplayallowed)|允许网站自动播放媒体|
|[BackgroundModeEnabled](#backgroundmodeenabled)|Microsoft Edge 关闭后，继续运行后台应用|
|[BackgroundTemplateListUpdatesEnabled](#backgroundtemplatelistupdatesenabled)|对集锦和其他使用模板的功能的可用模板列表启用后台更新|
|[BingAdsSuppression](#bingadssuppression)|阻止必应搜索结果中的所有广告|
|[BlockThirdPartyCookies](#blockthirdpartycookies)|阻止第三方 Cookie|
|[BrowserAddProfileEnabled](#browseraddprofileenabled)|从“标识”浮出菜单或“设置”页面启用用户配置创建|
|[BrowserGuestModeEnabled](#browserguestmodeenabled)|启用来宾模式|
|[BrowserNetworkTimeQueriesEnabled](#browsernetworktimequeriesenabled)|允许查询浏览器网络时间服务|
|[BrowserSignin](#browsersignin)|浏览器登录设置|
|[BuiltInDnsClientEnabled](#builtindnsclientenabled)|使用内置 DNS 客户端|
|[BuiltinCertificateVerifierEnabled](#builtincertificateverifierenabled)|确定是否将使用内置证书验证器验证服务器证书 (已弃用)|
|[CertificateTransparencyEnforcementDisabledForCas](#certificatetransparencyenforcementdisabledforcas)|对 subjectPublicKeyInfo 哈希列表禁用强制证书透明度|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](#certificatetransparencyenforcementdisabledforlegacycas)|对列出的旧证书颁发机构禁用证书透明度强制|
|[CertificateTransparencyEnforcementDisabledForUrls](#certificatetransparencyenforcementdisabledforurls)|对特定 URL 禁用强制证书透明度|
|[ClearBrowsingDataOnExit](#clearbrowsingdataonexit)|Microsoft Edge 关闭时清除浏览数据|
|[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)|Microsoft Edge 关闭时清除缓存的图像和文件|
|[ClickOnceEnabled](#clickonceenabled)|允许用户使用 ClickOnce 协议打开文件|
|[CollectionsServicesAndExportsBlockList](#collectionsservicesandexportsblocklist)|阻止访问集锦中指定的服务列表和导出目标|
|[CommandLineFlagSecurityWarningsEnabled](#commandlineflagsecuritywarningsenabled)|为命令行标志启用安全警告|
|[ComponentUpdatesEnabled](#componentupdatesenabled)|在 Microsoft Edge 中启用组件更新|
|[ConfigureDoNotTrack](#configuredonottrack)|配置“禁止跟踪”|
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|配置用 Active Directory 域帐户(如果没有 Azure AD 域帐户)进行的自动登录|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|配置在线文本到语音转换|
|[ConfigureShare](#configureshare)|配置共享体验|
|[CustomHelpLink](#customhelplink)|指定自定义帮助链接|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|已启用 DNS 拦截检查|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|将 Microsoft Edge 设置为默认浏览器|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|允许默认搜索提供程序上下文菜单搜索访问|
|[DefaultSensorsSetting](#defaultsensorssetting)|默认传感器设置|
|[DefaultSerialGuardSetting](#defaultserialguardsetting)|控制串行 API 的使用|
|[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)|要求在选项卡导航之前企业模式站点列表可用|
|[DeleteDataOnMigration](#deletedataonmigration)|迁移时删除旧浏览器数据|
|[DeveloperToolsAvailability](#developertoolsavailability)|控制可以使用开发人员工具的位置|
|[DiagnosticData](#diagnosticdata)|发送有关浏览器使用情况的必需和可选诊断数据|
|[DirectInvokeEnabled](#directinvokeenabled)|允许用户使用 DirectInvoke 协议打开文件|
|[Disable3DAPIs](#disable3dapis)|禁用对 3D 图形 API 的支持|
|[DisableScreenshots](#disablescreenshots)|禁用进行屏幕截图|
|[DiskCacheDir](#diskcachedir)|设置磁盘缓存目录|
|[DiskCacheSize](#diskcachesize)|设置磁盘缓存大小(字节)|
|[DnsOverHttpsMode](#dnsoverhttpsmode)|控制 DNS-over-HTTPS 的模式|
|[DnsOverHttpsTemplates](#dnsoverhttpstemplates)|指定所需的 IP-HTTPS DNS 解析程序的 URI 模板|
|[DownloadDirectory](#downloaddirectory)|设置下载目录|
|[DownloadRestrictions](#downloadrestrictions)|允许使用下载限制|
|[EdgeCollectionsEnabled](#edgecollectionsenabled)|启用集锦功能|
|[EditFavoritesEnabled](#editfavoritesenabled)|允许用户编辑收藏夹|
|[EnableDeprecatedWebPlatformFeatures](#enabledeprecatedwebplatformfeatures)|在有限的时间内重新启用弃用的 Web 平台功能|
|[EnableDomainActionsDownload](#enabledomainactionsdownload)|启用从 Microsoft 进行域操作下载 (过时)|
|[EnableOnlineRevocationChecks](#enableonlinerevocationchecks)|启用联机 OCSP/CRL 检查|
|[EnableSha1ForLocalAnchors](#enablesha1forlocalanchors)|由本地信任锚颁发时，允许使用 SHA-1 签名的证书 (已弃用)|
|[EnterpriseHardwarePlatformAPIEnabled](#enterprisehardwareplatformapienabled)|允许托管扩展使用企业硬件平台 API|
|[EnterpriseModeSiteListManagerAllowed](#enterprisemodesitelistmanagerallowed)|允许访问 Enterprise Mode Site List Manager 工具|
|[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](#exemptdomainfiletypepairsfromfiletypedownloadwarnings)|对域上的指定文件类型禁用基于下载文件类型扩展名的警告|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|控制与实验和配置服务的通信|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox)|在外部协议对话框中显示“始终打开”复选框|
|[FamilySafetySettingsEnabled](#familysafetysettingsenabled)|允许用户配置“Family Safety”|
|[FavoritesBarEnabled](#favoritesbarenabled)|启用收藏夹栏|
|[ForceBingSafeSearch](#forcebingsafesearch)|强制执行必应安全搜索|
|[ForceCertificatePromptsOnMultipleMatches](#forcecertificatepromptsonmultiplematches)|配置当使用 "AutoSelectCertificateForUrls" 配置的站点拥有多个证书匹配项时，Microsoft Edge 是否应自动选择证书|
|[ForceEphemeralProfiles](#forceephemeralprofiles)|启用临时用户配置|
|[ForceGoogleSafeSearch](#forcegooglesafesearch)|强制执行 Google 安全搜索|
|[ForceLegacyDefaultReferrerPolicy](#forcelegacydefaultreferrerpolicy)|使用 no-referrer-when-downgrade 的默认引用站点策略 (已弃用)|
|[ForceNetworkInProcess](#forcenetworkinprocess)|强制网络代码在浏览器进程中运行 (过时)|
|[ForceSync](#forcesync)|强制同步浏览器数据，但不显示同步许可提示|
|[ForceYouTubeRestrict](#forceyoutuberestrict)|实施最小 YouTube 受限模式|
|[FullscreenAllowed](#fullscreenallowed)|允许全屏模式|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|启用全局范围的 HTTP 身份验证缓存|
|[GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar)|强制进行直接 Intranet 站点导航而不是在地址栏中对单个词条进行搜索|
|[HSTSPolicyBypassList](#hstspolicybypasslist)|配置将绕过 HSTS 策略检查的名称列表|
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|使用硬件加速(如可用)|
|[HideFirstRunExperience](#hidefirstrunexperience)|隐藏首次运行体验和初始屏幕|
|[ImportAutofillFormData](#importautofillformdata)|允许导入自动填充表单数据|
|[ImportBrowserSettings](#importbrowsersettings)|允许导入浏览器设置|
|[ImportCookies](#importcookies)|允许导入 Cookie|
|[ImportExtensions](#importextensions)|允许导入扩展|
|[ImportFavorites](#importfavorites)|允许导入收藏夹|
|[ImportHistory](#importhistory)|允许导入浏览历史记录|
|[ImportHomepage](#importhomepage)|允许导入主页设置|
|[ImportOpenTabs](#importopentabs)|允许导入打开的标签页|
|[ImportPaymentInfo](#importpaymentinfo)|允许导入付款信息|
|[ImportSavedPasswords](#importsavedpasswords)|允许导入保存的密码|
|[ImportSearchEngine](#importsearchengine)|允许导入搜索引擎设置|
|[ImportShortcuts](#importshortcuts)|允许导入快捷方式|
|[InPrivateModeAvailability](#inprivatemodeavailability)|配置 InPrivate 模式可用性|
|[InsecureFormsWarningsEnabled](#insecureformswarningsenabled)|为不安全的表单启用警告|
|[IntensiveWakeUpThrottlingEnabled](#intensivewakeupthrottlingenabled)|控制 IntensiveWakeUpThrottling 功能|
|[InternetExplorerIntegrationEnhancedHangDetection](#internetexplorerintegrationenhancedhangdetection)|为 Internet Explorer 模式配置增强型挂起检测|
|[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)|配置 Internet Explorer 集成|
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|配置企业模式站点列表|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|指定从 Internet Explorer 模式页面启动时，到未配置站点的“页面内”导航的行为方式|
|[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed)|允许 Internet Explorer 模式测试|
|[IsolateOrigins](#isolateorigins)|对特定来源启用站点隔离|
|[LocalProvidersEnabled](#localprovidersenabled)|允许来自本地提供商的建议|
|[ManagedFavorites](#managedfavorites)|配置收藏夹|
|[ManagedSearchEngines](#managedsearchengines)|管理搜索引擎|
|[MaxConnectionsPerProxy](#maxconnectionsperproxy)|到代理服务器的最大并发连接数|
|[MediaRouterCastAllowAllIPs](#mediaroutercastallowallips)|允许 Google Cast 连接到所有 IP 地址上的强制转换设备|
|[MetricsReportingEnabled](#metricsreportingenabled)|启用使用情况和崩溃相关的数据报告 (已弃用)|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|启用本机窗口封闭|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|为企业模式站点列表的选项卡导航设置延迟超时|
|[NetworkPredictionOptions](#networkpredictionoptions)|启用网络预测|
|[NonRemovableProfileEnabled](#nonremovableprofileenabled)|配置用户是否始终具有使用其工作或学校帐户自动登录的默认用户配置|
|[OverrideSecurityRestrictionsOnInsecureOrigin](#overridesecurityrestrictionsoninsecureorigin)|控制针对不安全源的安全限制的适用范围|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|允许网站查询可用的付款方式|
|[PersonalizationReportingEnabled](#personalizationreportingenabled)|允许向 Microsoft 发送浏览历史记录以对广告、搜索和新闻进行个性化设置|
|[PinningWizardAllowed](#pinningwizardallowed)|允许使用“固定到任务栏”向导|
|[ProactiveAuthEnabled](#proactiveauthenabled)|启用主动身份验证|
|[PromotionalTabsEnabled](#promotionaltabsenabled)|启用完整标签页促销内容|
|[PromptForDownloadLocation](#promptfordownloadlocation)|询问所下载文件的保存位置|
|[QuicAllowed](#quicallowed)|允许 QUIC 协议|
|[RelaunchNotification](#relaunchnotification)|通知用户推荐或需要对挂起的更新重启浏览器|
|[RelaunchNotificationPeriod](#relaunchnotificationperiod)|设置更新通知的时间段|
|[RendererCodeIntegrityEnabled](#renderercodeintegrityenabled)|启用呈现器代码完整性|
|[RequireOnlineRevocationChecksForLocalAnchors](#requireonlinerevocationchecksforlocalanchors)|指定本地信任密钥是否需要联机 OCSP/CRL 检查|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|启用使用 Web 服务解决导航错误|
|[RestrictSigninToPattern](#restrictsignintopattern)|限制哪些帐户可用作 Microsoft Edge 主帐户|
|[RoamingProfileLocation](#roamingprofilelocation)|设置漫游用户配置目录|
|[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)|启用对 Microsoft Edge 用户配置数据使用漫游副本|
|[RunAllFlashInAllowMode](#runallflashinallowmode)|将 Adobe Flash 内容设置扩展到所有内容|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|允许用户从 HTTPS 警告页继续|
|[SSLVersionMin](#sslversionmin)|已启用的最低 TLS 版本|
|[SaveCookiesOnExit](#savecookiesonexit)|当 Microsoft Edge 关闭时保存 Cookie|
|[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)|禁用保存浏览器历史记录|
|[ScreenCaptureAllowed](#screencaptureallowed)|允许或拒绝屏幕捕获|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|启用滚动到 URL 片段中的指定文本|
|[SearchSuggestEnabled](#searchsuggestenabled)|启用搜索建议|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|无需许可即可使用直接安全密钥证明的网站或域|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|将所有 Intranet 站点发送到 Internet Explorer|
|[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)|发送站点信息来改进 Microsoft 服务 (已弃用)|
|[SensorsAllowedForUrls](#sensorsallowedforurls)|允许访问特定网站上的传感器|
|[SensorsBlockedForUrls](#sensorsblockedforurls)|阻止访问特定网站上的传感器|
|[SerialAskForUrls](#serialaskforurls)|在特定网站上允许串行 API|
|[SerialBlockedForUrls](#serialblockedforurls)|在特定网站上阻止串行 API|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|在收藏夹栏中显示 Microsoft Office 快捷方式 (已弃用)|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|启用签名 HTTP Exchange (SXG) 支持|
|[SitePerProcess](#siteperprocess)|为每个站点启用站点隔离|
|[SpellcheckEnabled](#spellcheckenabled)|启用拼写检查|
|[SpellcheckLanguage](#spellchecklanguage)|启用特定拼写检查语言|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|强制禁用拼写检查功能的语言|
|[StricterMixedContentTreatmentEnabled](#strictermixedcontenttreatmentenabled)|针对混合内容启用更严格的处理 (已弃用)|
|[SuppressUnsupportedOSWarning](#suppressunsupportedoswarning)|禁止不支持的操作系统警告|
|[SyncDisabled](#syncdisabled)|使用 Microsoft 同步服务禁用数据同步|
|[SyncTypesListDisabled](#synctypeslistdisabled)|配置从同步中排除的类型列表|
|[TLS13HardeningForLocalAnchorsEnabled](#tls13hardeningforlocalanchorsenabled)|对本地信任密钥启用 TLS 1.3 安全功能。 (过时)|
|[TLSCipherSuiteDenyList](#tlsciphersuitedenylist)|指定要禁用的 TLS 密码套件|
|[TabFreezingEnabled](#tabfreezingenabled)|允许冻结后台标签页|
|[TaskManagerEndProcessEnabled](#taskmanagerendprocessenabled)|启用在浏览器任务管理器中结束进程|
|[TotalMemoryLimitMb](#totalmemorylimitmb)|设置单个 Microsoft Edge 实例可以使用的内存限制(MB)。|
|[TrackingPrevention](#trackingprevention)|阻止跟踪用户的 Web 浏览活动|
|[TranslateEnabled](#translateenabled)|启用翻译|
|[URLAllowlist](#urlallowlist)|定义允许的 URL 列表|
|[URLBlocklist](#urlblocklist)|阻止访问 URL 列表|
|[UserAgentClientHintsEnabled](#useragentclienthintsenabled)|启用用户代理客户端提示功能 (已弃用)|
|[UserDataDir](#userdatadir)|设置用户数据目录|
|[UserDataSnapshotRetentionLimit](#userdatasnapshotretentionlimit)|限制保留的用于紧急回退的用户数据快照的数量|
|[UserFeedbackAllowed](#userfeedbackallowed)|允许用户反馈|
|[VideoCaptureAllowed](#videocaptureallowed)|允许或阻止视频捕获|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|无需请求许可即可访问视频捕获设备的站点|
|[WPADQuickCheckEnabled](#wpadquickcheckenabled)|设置 WPAD 优化|
|[WebAppInstallForceList](#webappinstallforcelist)|配置强制安装的 Web 应用列表|
|[WebComponentsV0Enabled](#webcomponentsv0enabled)|在 M84 之前重新启用 Web 组件 v0 API (过时)|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|允许 WebDriver 覆盖不兼容的策略 (过时)|
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|管理 WebRTC 的本地 IP 地址公开|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|限制 WebRTC 的本地 IP 地址公开|
|[WebRtcUdpPortRange](#webrtcudpportrange)|限制 WebRTC 使用的本地 UDP 端口的范围|
|[WinHttpProxyResolverEnabled](#winhttpproxyresolverenabled)|使用 Windows 代理解析程序 (已弃用)|




  ## Cast policies

  [返回顶部](#microsoft-edge---策略)

  ### EnableMediaRouter
  #### 启用 Google Cast
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  启用此策略以启用 Google Cast。用户将能够从应用程序菜单、页面上下文菜单、启用强制转换的网站上的媒体控件以及（如果显示）强制转换工具栏图标启动它。

         停用此策略可停用 Google Cast。

         默认情况下，Google Cast 已启用。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: EnableMediaRouter
  - GP 名称: 启用 Google Cast
  - GP 路径 (强制): 管理模板/Microsoft Edge/Cast
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: EnableMediaRouter
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: EnableMediaRouter
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ShowCastIconInToolbar
  #### 在工具栏中显示投放图标
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  将此策略设置为 true 可在工具栏或溢出菜单上显示“强制转换”工具栏图标。用户将无法将其删除。

如果未配置或禁用此策略，则用户可以使用其上下文菜单来固定或删除图标。

如果已将 [EnableMediaRouter](#enablemediarouter) 策略设置为 false，则会忽略此策略，并且不显示该工具栏图标。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ShowCastIconInToolbar
  - GP 名称: 在工具栏中显示投放图标
  - GP 路径 (强制): 管理模板/Microsoft Edge/Cast
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ShowCastIconInToolbar
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: ShowCastIconInToolbar
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ## HTTP 身份验证 policies

  [返回顶部](#microsoft-edge---策略)

  ### AllowCrossOriginAuthPrompt
  #### 允许跨源 HTTP 基本身份验证提示
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  控制页面上的第三方子内容是否可以打开 HTTP 基本身份验证对话框。

通常，此项作为钓鱼防御功能处于禁用状态。如果未配置此策略，则会禁用该策略，并且第三方子内容无法打开 HTTP 基本身份验对话框。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AllowCrossOriginAuthPrompt
  - GP 名称: 允许跨源 HTTP 基本身份验证提示
  - GP 路径 (强制): 管理模板/Microsoft Edge/HTTP 身份验证
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AllowCrossOriginAuthPrompt
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: AllowCrossOriginAuthPrompt
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AuthNegotiateDelegateAllowlist
  #### 指定 Microsoft Edge 可以将用户凭据委派给的服务器列表
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  配置 Microsoft Edge 可委派的服务器列表。

请用逗号分隔多个服务器名称。允许使用通配符(*)。

如果你未配置此策略，则 Microsoft Edge 将不会委派用户凭据，即使检测到服务器为 Intranet 服务器也不例外。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AuthNegotiateDelegateAllowlist
  - GP 名称: 指定 Microsoft Edge 可以将用户凭据委派给的服务器列表
  - GP 路径 (强制): 管理模板/Microsoft Edge/HTTP 身份验证
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AuthNegotiateDelegateAllowlist
  - 值类型: REG_SZ
  ##### 示例值:
```
"contoso.com"
```


  #### Mac 信息和设置
  - 首选项密钥名称: AuthNegotiateDelegateAllowlist
  - 示例值:
``` xml
<string>contoso.com</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AuthSchemes
  #### 支持的身份验证方案
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定受支持的 HTTP 身份验证方案。

可用于配置该策略的值: "basic"、"digest"、"ntlm" 和 "negotiate"。用逗号分隔多个值。

如果未配置此策略，则会使用所有四个方案。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AuthSchemes
  - GP 名称: 支持的身份验证方案
  - GP 路径 (强制): 管理模板/Microsoft Edge/HTTP 身份验证
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AuthSchemes
  - 值类型: REG_SZ
  ##### 示例值:
```
"basic,digest,ntlm,negotiate"
```


  #### Mac 信息和设置
  - 首选项密钥名称: AuthSchemes
  - 示例值:
``` xml
<string>basic,digest,ntlm,negotiate</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AuthServerAllowlist
  #### 配置允许的身份验证服务器列表
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定为集成身份验证启用的服务器。仅当 Microsoft Edge 从代理或此列表中的服务器收到身份验证质询时，才启用集成身份验证。

用逗号分隔多个服务器名称。允许使用通配符(*)。

如果未配置此策略，则 Microsoft Edge 尝试检测服务器是否位于 Intranet 上 - 直到那时，它才将响应 IWA 请求。如果服务器在 Internet 上，Microsoft Edge 会忽略来自该服务器的 IWA 请求。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AuthServerAllowlist
  - GP 名称: 配置允许的身份验证服务器列表
  - GP 路径 (强制): 管理模板/Microsoft Edge/HTTP 身份验证
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AuthServerAllowlist
  - 值类型: REG_SZ
  ##### 示例值:
```
"*contoso.com,contoso.com"
```


  #### Mac 信息和设置
  - 首选项密钥名称: AuthServerAllowlist
  - 示例值:
``` xml
<string>*contoso.com,contoso.com</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DisableAuthNegotiateCnameLookup
  #### 协商 Kerberos 身份验证时禁用 CNAME 查找
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  确定生成的 Kerberos SPN 是否基于规范的 DNS 名称(CNAME)或输入的原始名称。

如果启用此策略，将跳过 CNAME 查找，使用服务器名称(作为输入)。

如果禁用或未配置此策略，则使用服务器的规范名称。这通过 CNAME 查找来确定。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DisableAuthNegotiateCnameLookup
  - GP 名称: 协商 Kerberos 身份验证时禁用 CNAME 查找
  - GP 路径 (强制): 管理模板/Microsoft Edge/HTTP 身份验证
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DisableAuthNegotiateCnameLookup
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: DisableAuthNegotiateCnameLookup
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### EnableAuthNegotiatePort
  #### 在 Kerberos SPN 中包含非标准端口
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定生成的 Kerberos SPN 是否应包括非标准端口。

如果启用此策略，并且用户在 URL 中包含非标准端口(非 80 或 443 的端口)，则该端口包含在生成的 Kerberos SPN 中。

如果不配置或禁用此策略，生成的 Kerberos SPN 在任何情况下都不包含端口。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: EnableAuthNegotiatePort
  - GP 名称: 在 Kerberos SPN 中包含非标准端口
  - GP 路径 (强制): 管理模板/Microsoft Edge/HTTP 身份验证
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: EnableAuthNegotiatePort
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: EnableAuthNegotiatePort
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### NtlmV2Enabled
  #### 控制是否启用 NTLMv2 身份验证
  
  
  #### 支持的版本:
  - 在 macOS 自 77 或之后

  #### 描述
  控制是否启用 NTLMv2。

所有最新版本的 Samba 和 Windows 服务器都支持 NTLMv2。你应该只禁用 NTLMv2 来解决向后兼容性问题，因为它会降低身份验证的安全性。

如果未配置此策略，则默认情况下会启用 NTLMv2。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  

  #### Mac 信息和设置
  - 首选项密钥名称: NtlmV2Enabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ## Smartscreen 设置 policies

  [返回顶部](#microsoft-edge---策略)

  ### PreventSmartScreenPromptOverride
  #### 阻止绕过 Microsoft Defender SmartScreen 对站点的提示
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  此策略让你确定用户是否可以覆盖有关潜在恶意网站的 Microsoft Defender SmartScreen 警告。

如果启用此设置，则用户无法忽略 Microsoft Defender SmartScreen 警告，并且会阻止用户继续访问该站点。

如果禁用或未配置此设置，则用户可以忽略 Microsoft Defender SmartScreen 警告并继续访问该站点。

此策略仅适用于已加入 Microsoft Active Directory 域的 Windows 实例、为进行设备管理而注册的 Windows 10 专业版或企业版实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PreventSmartScreenPromptOverride
  - GP 名称: 阻止绕过 Microsoft Defender SmartScreen 对站点的提示
  - GP 路径 (强制): 管理模板/Microsoft Edge/Smartscreen 设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: PreventSmartScreenPromptOverride
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: PreventSmartScreenPromptOverride
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### PreventSmartScreenPromptOverrideForFiles
  #### 阻止绕过有关下载的 Microsoft Defender SmartScreen 警告
  
  
  #### 支持的版本:
  - 在 Windows 自 77 或之后
  - 在 macOS 自 79 或之后

  #### 描述
  此策略让你确定用户是否可以覆盖有关未验证下载的 Microsoft Defender SmartScreen 警告。

如果启用此策略，组织中的用户无法忽略 Microsoft Defender SmartScreen 警告，并且用户无法完成未验证的下载。

如果禁用或未配置此策略，用户可以忽略 Microsoft Defender SmartScreen 警告并完成未验证的下载。

此策略仅适用于已加入 Microsoft Active Directory 域的 Windows 实例、为进行设备管理而注册的 Windows 10 专业版或企业版实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PreventSmartScreenPromptOverrideForFiles
  - GP 名称: 阻止绕过有关下载的 Microsoft Defender SmartScreen 警告
  - GP 路径 (强制): 管理模板/Microsoft Edge/Smartscreen 设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: PreventSmartScreenPromptOverrideForFiles
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: PreventSmartScreenPromptOverrideForFiles
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SmartScreenAllowListDomains
  #### 配置 Microsoft Defender SmartScreen 将不会为其触发警告的域的列表
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  配置 Microsoft Defender SmartScreen 受信任的域列表。这意味着:
如果源 URL 与这些域匹配，Microsoft Defender SmartScreen 不会检查可能的恶意资源，例如钓鱼软件和其他恶意软件。
Microsoft Defender SmartScreen 下载保护服务不会检查在这些域上托管的下载。

如果启用此策略，Microsoft Defender SmartScreen 将信任这些域。
如果禁用或未设置此策略，默认的 Microsoft Defender SmartScreen 保护将适用于所有资源。

此策略仅适用于已加入 Microsoft Active Directory 域的 Windows 实例、为进行设备管理而注册的 Windows 10 专业版或企业版实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例。
另请注意，如果你的组织已启用 Microsoft Defender 高级威胁防护，则此策略不适用。你必须在 Microsoft Defender 安全中心中配置允许和阻止名单。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SmartScreenAllowListDomains
  - GP 名称: 配置 Microsoft Defender SmartScreen 将不会为其触发警告的域的列表
  - GP 路径 (强制): 管理模板/Microsoft Edge/Smartscreen 设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\2 = "myuniversity.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: SmartScreenAllowListDomains
  - 示例值:
``` xml
<array>
  <string>mydomain.com</string>
  <string>myuniversity.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SmartScreenEnabled
  #### 配置 Microsoft Defender SmartScreen
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  此策略设置允许你配置是否开启 Microsoft Defender SmartScreen。Microsoft Defender SmartScreen 提供警告消息，以帮助保护用户免受潜在的钓鱼诈骗和恶意软件的侵害。默认情况下，Microsoft Defender SmartScreen 处于开启状态。

如果启用此设置，则将开启 Microsoft Defender SmartScreen。

如果禁用此设置，则将关闭 Microsoft Defender SmartScreen。

如果未配置此设置，则用户可以选择是否使用 Microsoft Defender SmartScreen。

此策略仅适用于已加入 Microsoft Active Directory 域的 Windows 实例、为设备管理注册的 Windows 10 专业版或企业版实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SmartScreenEnabled
  - GP 名称: 配置 Microsoft Defender SmartScreen
  - GP 路径 (强制): 管理模板/Microsoft Edge/Smartscreen 设置
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/Smartscreen 设置
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: SmartScreenEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: SmartScreenEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SmartScreenForTrustedDownloadsEnabled
  #### 强制对来自受信任源的下载执行 Microsoft Defender SmartScreen 检查
  
  
  #### 支持的版本:
  - 在 Windows 自 78 或之后

  #### 描述
  此策略设置允许你配置 Microsoft Defender SmartScreen 是否检查来自受信任源的下载内容的声誉。

如果启用或未配置此设置，则无论来源如何，Microsoft Defender SmartScreen 都将检查下载内容的声誉。

如果禁用此设置，则从受信任源下载时，Microsoft Defender SmartScreen 不会检查下载内容的声誉。

此策略仅适用于已加入 Microsoft Active Directory 域的 Windows 实例、为设备管理注册的 Windows 10 专业版或企业版实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SmartScreenForTrustedDownloadsEnabled
  - GP 名称: 强制对来自受信任源的下载执行 Microsoft Defender SmartScreen 检查
  - GP 路径 (强制): 管理模板/Microsoft Edge/Smartscreen 设置
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/Smartscreen 设置
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: SmartScreenForTrustedDownloadsEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  

  [返回顶部](#microsoft-edge---策略)

  ### SmartScreenPuaEnabled
  #### 配置 Microsoft Defender SmartScreen 以阻止可能不需要的应用
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 80

  #### 描述
  此策略设置允许你配置是否使用 Microsoft Defender SmartScreen 开启对可能不需要的应用的阻止功能。使用 Microsoft Defender SmartScreen 阻止可能不需要的应用可提供警告消息，以帮助保护用户防范广告程序、挖矿病毒、捆绑软件和其他由网站托管的信誉度较低的应用。默认关闭使用 Microsoft Defender SmartScreen 阻止可能不需要的应用。

如果启用此设置，则会开启使用 Microsoft Defender SmartScreen 阻止可能不需要的应用。

如果禁用此设置，则会关闭使用 Microsoft Defender SmartScreen 阻止可能不需要的应用。

如果未配置此设置，则用户可以选择是否使用 Microsoft Defender SmartScreen 阻止可能不需要的应用。

此策略仅适用于已加入 Microsoft Active Directory 域的 Windows 实例、为设备管理注册的 Windows 10 专业版或企业版实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SmartScreenPuaEnabled
  - GP 名称: 配置 Microsoft Defender SmartScreen 以阻止可能不需要的应用
  - GP 路径 (强制): 管理模板/Microsoft Edge/Smartscreen 设置
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/Smartscreen 设置
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: SmartScreenPuaEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: SmartScreenPuaEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ## 代理服务器 policies

  [返回顶部](#microsoft-edge---策略)

  ### ProxyBypassList
  #### 配置代理绕过规则
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  定义 Microsoft Edge 将会为其绕过任何代理的主机列表。

仅当在 [ProxyMode](#proxymode) 策略中选择“使用固定代理服务器”时才应用此策略。如果已选择任何其他模式来配置代理策略，请不要启用或配置此策略。

如果启用此策略，则可以创建主机列表，使 Microsoft Edge 不对这些主机使用代理。

如果未配置此策略，则不会创建 Microsoft Edge 为其绕过代理的主机列表。如果已指定任何其他代理策略设置方法，请不要配置此策略。

有关更详细的示例，请转到 [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ProxyBypassList
  - GP 名称: 配置代理绕过规则
  - GP 路径 (强制): 管理模板/Microsoft Edge/代理服务器
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ProxyBypassList
  - 值类型: REG_SZ
  ##### 示例值:
```
"https://www.contoso.com, https://www.fabrikam.com"
```


  #### Mac 信息和设置
  - 首选项密钥名称: ProxyBypassList
  - 示例值:
``` xml
<string>https://www.contoso.com, https://www.fabrikam.com</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ProxyMode
  #### 配置代理服务器设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定 Microsoft Edge 所使用的代理服务器设置。如果启用此策略，则用户将无法更改代理设置。

如果选择从不使用代理服务器并且始终直接连接，则会忽略所有其他选项。

如果选择使用系统代理设置，则会忽略所有其他选项。

如果选择自动检测代理服务器，则会忽略所有其他选项。

如果选择固定服务器代理模式，则可以在 [ProxyServer](#proxyserver) 和“以逗号分隔的代理跳过规则列表”中指定更多选项。

如果选择使用 .pac 代理脚本，则必须在“指向代理 .pac 文件的 URL”中指定指向脚本的 URL。

有关详细示例，请转到 [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)。

如果启用此策略，则 Microsoft Edge 将忽略从命令行指定的所有代理相关选项。

如果未配置此策略，则用户可以选择自己的代理设置。

策略选项映射：

* ProxyDisabled (direct) = 从不使用代理

* ProxyAutoDetect (auto_detect) = 自动检测代理设置

* ProxyPacScript (pac_script) = 使用 .pac 代理脚本

* ProxyFixedServers (fixed_servers) = 使用固定的代理服务器

* ProxyUseSystem (system) = 使用系统代理设置

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ProxyMode
  - GP 名称: 配置代理服务器设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/代理服务器
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ProxyMode
  - 值类型: REG_SZ
  ##### 示例值:
```
"direct"
```


  #### Mac 信息和设置
  - 首选项密钥名称: ProxyMode
  - 示例值:
``` xml
<string>direct</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ProxyPacUrl
  #### 设置代理 .pac 文件的 URL
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定代理自动配置(PAC)文件的 URL。

仅当你在 [ProxyMode](#proxymode) 策略中选择了“使用 .pac 代理脚本”时才会应用此策略。如果你选择了任何其他模式来配置代理策略，请不要启用或配置此策略。

如果启用此策略，则可以指定 PAC 文件的 URL，该文件定义浏览器如何自动选择适当的代理服务器来获取特定网站。

如果禁用或未配置此策略，则不会指定 PAC 文件。如果已指定任何其他代理策略设置方法，请不要配置此策略。

有关详细示例，请参阅 [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ProxyPacUrl
  - GP 名称: 设置代理 .pac 文件的 URL
  - GP 路径 (强制): 管理模板/Microsoft Edge/代理服务器
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ProxyPacUrl
  - 值类型: REG_SZ
  ##### 示例值:
```
"https://internal.contoso.com/example.pac"
```


  #### Mac 信息和设置
  - 首选项密钥名称: ProxyPacUrl
  - 示例值:
``` xml
<string>https://internal.contoso.com/example.pac</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ProxyServer
  #### 配置代理服务器的地址或 URL
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定代理服务器的 URL。

仅当你在 [ProxyMode](#proxymode) 策略中选择了“使用固定代理服务器”时才会应用此策略。如果选择了任何其他模式来配置代理策略，请不要启用或配置此策略。

如果启用此策略，则此策略配置的代理服务器将用于所有 URL。

如果禁用或未配置此策略，则用户可以在处于此代理模式时选择自己的代理设置。如果已指定任何其他代理策略设置方法，请不要配置此策略。

有关更多选项和详细示例，请参阅 [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ProxyServer
  - GP 名称: 配置代理服务器的地址或 URL
  - GP 路径 (强制): 管理模板/Microsoft Edge/代理服务器
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ProxyServer
  - 值类型: REG_SZ
  ##### 示例值:
```
"123.123.123.123:8080"
```


  #### Mac 信息和设置
  - 首选项密钥名称: ProxyServer
  - 示例值:
``` xml
<string>123.123.123.123:8080</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ProxySettings
  #### 代理服务器设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  配置 Microsoft Edge 的代理设置。

如果启用此策略，则 Microsoft Edge 会忽略从命令行指定的所有代理相关选项。

如果未配置此策略，则用户可以选择自己的代理设置。

此策略将替代以下各个策略:

[ProxyMode](#proxymode)
[ProxyPacUrl](#proxypacurl)
[ProxyServer](#proxyserver)
[ProxyBypassList](#proxybypasslist)

使用 ProxyMode 字段可以指定 Microsoft Edge 所使用的代理服务器，并阻止用户更改代理设置。

ProxyPacUrl 字段是指向代理 .pac 文件的 URL。

ProxyServer 字段是代理服务器的 URL。

ProxyBypassList 字段是 Microsoft Edge 绕过的代理主机列表。

如果选择 "direct" 值作为 [ProxyMode](#proxymode)，则将永远不会使用代理并且会忽略所有其他字段。

如果选择 "system" 值作为 [ProxyMode](#proxymode)，则使用系统的代理并忽略所有其他字段。

如果选择 "auto_detect" 值作为 [ProxyMode](#proxymode)，则会忽略所有其他字段。

如果选择 "fixed_server" 值作为 [ProxyMode](#proxymode)，则将使用 [ProxyServer](#proxyserver) 和 [ProxyBypassList](#proxybypasslist) 字段。

如果选择 "pac_script" 值作为 [ProxyMode](#proxymode)，则将使用 [ProxyPacUrl](#proxypacurl) 和 [ProxyBypassList](#proxybypasslist) 字段。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字典

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ProxySettings
  - GP 名称: 代理服务器设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/代理服务器
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ProxySettings
  - 值类型: REG_SZ
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {
  "ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", 
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  #### Mac 信息和设置
  - 首选项密钥名称: ProxySettings
  - 示例值:
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
  

  [返回顶部](#microsoft-edge---策略)

  ## 内容设置 policies

  [返回顶部](#microsoft-edge---策略)

  ### AutoSelectCertificateForUrls
  #### 自动为这些站点选择客户端证书
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  根据 URL 模式指定站点列表，当这些站点请求客户端证书时，Microsoft Edge 应自动为其选择。

该值必须是字符串化的 JSON 词典数组。每个词典的形式必须为 { "pattern": "$URL_PATTERN", "filter" : $FILTER }，其中 $URL_PATTERN 为内容设置模式。$FILTER 限制浏览器可自动从中选择的客户端证书。只能选择与服务器的证书请求匹配的证书，而与筛选器无关。例如，如果 $FILTER 的形式为 { "ISSUER": { "CN": "$ISSUER_CN" } }，则只能额外选择由具有 CommonName $ISSUER_CN 的证书所颁发的客户端证书。如果 $FILTER 包含 "ISSUER" 和 "SUBJECT" 部分，则客户端证书必须同时满足两个条件才能被选择。如果 $FILTER 指定了组织("O")，则证书必须至少具有一个与指定值匹配的组织才能被选择。如果 $FILTER 指定了组织单位("OU")，则证书必须至少具有一个与指定值匹配的组织单位才能被选择。如果 $FILTER 为空词典 {}，则不会对客户端证书选择产生额外限制。

如果未配置此策略，则不会对任何站点执行自动选择。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AutoSelectCertificateForUrls
  - GP 名称: 自动为这些站点选择客户端证书
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls\1 = "{\"pattern\":\"https://www.contoso.com\",\"filter\":{\"ISSUER\":{\"CN\":\"certificate issuer name\", \"L\": \"certificate issuer location\", \"O\": \"certificate issuer org\", \"OU\": \"certificate issuer org unit\"}, \"SUBJECT\":{\"CN\":\"certificate subject name\", \"L\": \"certificate subject location\", \"O\": \"certificate subject org\", \"OU\": \"certificate subject org unit\"}}}"

```


  #### Mac 信息和设置
  - 首选项密钥名称: AutoSelectCertificateForUrls
  - 示例值:
``` xml
<array>
  <string>{"pattern":"https://www.contoso.com","filter":{"ISSUER":{"CN":"certificate issuer name", "L": "certificate issuer location", "O": "certificate issuer org", "OU": "certificate issuer org unit"}, "SUBJECT":{"CN":"certificate subject name", "L": "certificate subject location", "O": "certificate subject org", "OU": "certificate subject org unit"}}}</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### CookiesAllowedForUrls
  #### 在特定站点上允许 Cookie
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  根据 URL 模式定义允许设置 Cookie 的站点列表。

如果未配置此策略，则对所有站点使用 [DefaultCookiesSetting](#defaultcookiessetting) 策略(如果已设置)或用户个人配置中的全局默认值。

有关详细信息，请参阅 [CookiesBlockedForUrls](#cookiesblockedforurls) 和 [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) 策略。

请注意，这三个策略之间不能设置冲突的 URL 模式:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- CookiesAllowedForUrls

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

若要排除 cookie 以防退出时被删除，请配置 [SaveCookiesOnExit](#savecookiesonexit) 策略。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: CookiesAllowedForUrls
  - GP 名称: 在特定站点上允许 Cookie
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: CookiesAllowedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### CookiesBlockedForUrls
  #### 在特定站点上阻止 Cookie
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  根据 URL 模式定义无法设置 Cookie 的站点列表。

如果未配置此策略，则对所有站点使用 [DefaultCookiesSetting](#defaultcookiessetting) 策略(如果已设置)或用户个人配置中的全局默认值。

有关详细信息，请参阅 [CookiesAllowedForUrls](#cookiesallowedforurls) 和 [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) 策略。

请注意，这三个策略之间不能设置冲突的 URL 模式:

- CookiesBlockedForUrls

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: CookiesBlockedForUrls
  - GP 名称: 在特定站点上阻止 Cookie
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: CookiesBlockedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### CookiesSessionOnlyForUrls
  #### 将特定网站的 Cookie 限制为当前会话
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  当会话结束时(窗口关闭时)，由与定义的 URL 模式匹配的网站所创建的 Cookie 将被删除。

与模式不匹配的网站所创建的 Cookie 由 [DefaultCookiesSetting](#defaultcookiessetting) 策略(如果已设置)或用户个人配置所控制。如果未配置此策略，那么这也是默认行为。

如果 Microsoft Edge 在后台模式下运行，则在最后一个窗口关闭时，会话可能不会关闭，这意味着窗口关闭时不会清除 Cookie。有关配置 Microsoft Edge 在后台模式下运行时所发生情况的信息，请参阅 [BackgroundModeEnabled](#backgroundmodeenabled) 策略。

你还可以使用 [CookiesAllowedForUrls](#cookiesallowedforurls) 和 [CookiesBlockedForUrls](#cookiesblockedforurls) 策略控制哪些网站可以创建 Cookie。

请注意，三个策略之间不能设置冲突的 URL 模式:

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- CookiesSessionOnlyForUrls

如果你设置 [RestoreOnStartup](#restoreonstartup) 策略以从以前的会话中恢复 URL，则会忽略此策略，并且会永久为那些站点存储 Cookie。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: CookiesSessionOnlyForUrls
  - GP 名称: 将特定网站的 Cookie 限制为当前会话
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: CookiesSessionOnlyForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultCookiesSetting
  #### 配置 Cookie
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  控制网站是否可以在用户的设备上创建 Cookie。此策略要求全部应用或者全部不应用 - 你可以允许所有网站创建 Cookie，或者不允许任何网站创建 Cookie。无法使用此策略启用来自特定网站的 Cookie。

将该策略设置为“SessionOnly”可在会话关闭时清除 Cookie。如果 Microsoft Edge 在后台模式下运行，则在最后一个窗口关闭时，会话可能不会关闭，这意味着窗口关闭时不会清除 Cookie。有关配置 Microsoft Edge 在后台模式下运行时所发生情况的信息，请参阅 [BackgroundModeEnabled](#backgroundmodeenabled) 策略。

如果未配置此策略，将使用默认的“AllowCookies”，并且用户可以在 Microsoft Edge 的“设置”中更改此设置。(如果不希望用户能够更改此设置，请设置该策略。)

策略选项映射：

* AllowCookies (1) = 允许所有站点创建 Cookie

* BlockCookies (2) = 不允许任何站点创建 Cookie

* SessionOnly (4) = 在会话持续时间内保留 cookie，[SaveCookiesOnExit](#savecookiesonexit) 中列出的内容除外

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultCookiesSetting
  - GP 名称: 配置 Cookie
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DefaultCookiesSetting
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultCookiesSetting
  - 示例值:
``` xml
<integer>1</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultFileSystemReadGuardSetting
  #### 控制用于读取的文件系统 API 的使用
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  如果将此策略设置为 3，则网站可以使用文件系统 API 请求对主机操作系统的文件系统进行读取访问。如果将此策略设置为 2，则拒绝访问。

如果未设置此策略，则网站可以请求访问。用户可以更改此设置。

策略选项映射：

* BlockFileSystemRead (2) = 不允许任何网站通过文件系统 API 请求对文件和目录的读取访问权限

* AskFileSystemRead (3) = 允许网站通过文件系统 API 要求用户授予对文件和目录的读取访问权限

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultFileSystemReadGuardSetting
  - GP 名称: 控制用于读取的文件系统 API 的使用
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DefaultFileSystemReadGuardSetting
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultFileSystemReadGuardSetting
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultFileSystemWriteGuardSetting
  #### 控制用于编写的文件系统 API 的使用
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  如果将此策略设置为 3，则网站可以使用文件系统 API 请求对主机操作系统的文件系统进行写入访问。如果将此策略设置为 2，则拒绝访问。

如果未设置此策略，则网站可以请求访问。用户可以更改此设置。

策略选项映射：

* BlockFileSystemWrite (2) = 不允许任何网站请求对文件和目录的写入访问权限

* AskFileSystemWrite (3) = 允许网站要求用户授予对文件和目录的写入访问权限

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultFileSystemWriteGuardSetting
  - GP 名称: 控制用于编写的文件系统 API 的使用
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DefaultFileSystemWriteGuardSetting
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultFileSystemWriteGuardSetting
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultGeolocationSetting
  #### 默认地理位置设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  设置网站是否可以跟踪用户的物理位置。你可以默认允许跟踪(“AllowGeolocation”)，默认拒绝跟踪(“BlockGeolocation”)，或者在每次网站请求用户位置时询问用户(“AskGeolocation”)。

如果未配置此策略，将使用“AskGeolocation”策略，并且用户可以更改此设置。

策略选项映射：

* AllowGeolocation (1) = 允许站点跟踪用户的实际位置

* BlockGeolocation (2) = 不允许任何站点跟踪用户的物理位置

* AskGeolocation (3) = 每当站点要跟踪用户的实际位置时都进行询问

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultGeolocationSetting
  - GP 名称: 默认地理位置设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DefaultGeolocationSetting
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultGeolocationSetting
  - 示例值:
``` xml
<integer>1</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultImagesSetting
  #### 默认图像设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  设置网站是否可以显示图像。可以对所有站点允许(“AllowImages”)或阻止(“BlockImages”)图像。

如果未配置此策略，默认情况下允许显示图像，而且用户可以更改此设置。

策略选项映射：

* AllowImages (1) = 允许所有站点显示所有图像

* BlockImages (2) = 不允许任何站点显示图像

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultImagesSetting
  - GP 名称: 默认图像设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DefaultImagesSetting
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultImagesSetting
  - 示例值:
``` xml
<integer>1</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultInsecureContentSetting
  #### 控制不安全内容例外的使用
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 80

  #### 描述
  允许你设置用户是否可以添加例外以允许特定站点显示混合内容。

针对特定 URL 模式，可使用 [InsecureContentAllowedForUrls](#insecurecontentallowedforurls) 和 [InsecureContentBlockedForUrls](#insecurecontentblockedforurls) 策略替代此策略。

如果未设置此策略，则将允许用户添加例外以允许可阻止混合内容并禁止自动升级可选择阻止的混合内容。

策略选项映射：

* BlockInsecureContent (2) = 不允许任何站点加载混合内容

* AllowExceptionsInsecureContent (3) = 允许用户添加例外以允许混合内容

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultInsecureContentSetting
  - GP 名称: 控制不安全内容例外的使用
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DefaultInsecureContentSetting
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultInsecureContentSetting
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultJavaScriptSetting
  #### 默认 JavaScript 设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  设置网站是否可以运行 JavaScript。可以对所有站点允许(“AllowJavaScript”)或阻止(“BlockJavaScript”)。

如果未配置此策略，所有站点默认都可以运行 JavaScript，而且用户可以更改此设置。

策略选项映射：

* AllowJavaScript (1) = 允许所有站点运行 JavaScript

* BlockJavaScript (2) = 不允许任何站点运行 JavaScript

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultJavaScriptSetting
  - GP 名称: 默认 JavaScript 设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DefaultJavaScriptSetting
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultJavaScriptSetting
  - 示例值:
``` xml
<integer>1</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultNotificationsSetting
  #### 默认通知设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  设置网站是否可以显示桌面通知。你可以默认允许通知(“AllowNotifications'”)，默认拒绝通知(“BlockNotifications”)，或者在每次网站要显示通知时询问用户(“AskNotifications”)。

如果未配置此策略，则默认允许通知，而且用户可以更改此设置。

策略选项映射：

* AllowNotifications (1) = 允许站点显示桌面通知

* BlockNotifications (2) = 不允许任何站点显示桌面通知

* AskNotifications (3) = 每次站点要显示桌面通知时都询问

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultNotificationsSetting
  - GP 名称: 默认通知设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DefaultNotificationsSetting
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultNotificationsSetting
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultPluginsSetting
  #### 默认 Adobe Flash 设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  [PluginsAllowedForUrls](#pluginsallowedforurls) and [PluginsBlockedForUrls](#pluginsblockedforurls) are checked first, then this policy. The options are 'ClickToPlay' and 'BlockPlugins'. If you set this policy to 'BlockPlugins', this plugin is denied for all websites. 'ClickToPlay' lets the Flash plugin run, but users click the placeholder to start it.

If you don't configure this policy, the user can change this setting manually.

Note: Automatic playback is only for domains explicitly listed in the [PluginsAllowedForUrls](#pluginsallowedforurls) policy. To turn automatic playback on for all sites, add http://* and https://* to the allowed list of URLs.

策略选项映射：

* BlockPlugins (2) = 阻止 Adobe Flash 插件

* ClickToPlay (3) = 单击以播放

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultPluginsSetting
  - GP 名称: 默认 Adobe Flash 设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DefaultPluginsSetting
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultPluginsSetting
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultPopupsSetting
  #### 默认的弹出窗口设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  设置网站是否可显示弹出窗口。可以对所有站点允许(“AllowPopups”)或阻止(“BlockPopups”)。

如果未配置此策略，则默认阻止弹出窗口，而且用户可以更改此设置。

策略选项映射：

* AllowPopups (1) = 允许所有站点显示弹出窗口

* BlockPopups (2) = 不允许任何站点显示弹出窗口

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultPopupsSetting
  - GP 名称: 默认的弹出窗口设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DefaultPopupsSetting
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultPopupsSetting
  - 示例值:
``` xml
<integer>1</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultWebBluetoothGuardSetting
  #### 控制 Web 蓝牙 API 的使用
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  控制网站是否可以访问附近的蓝牙设备。你可以完全阻止访问或要求站点在每次要访问蓝牙设备时都询问用户。

如果不配置此策略，则使用默认值(“AskWebBluetooth”，表示每次都询问用户)，用户可以更改此值。

策略选项映射：

* BlockWebBluetooth (2) = 不允许任何站点通过 Web 蓝牙 API 请求对蓝牙设备的访问

* AskWebBluetooth (3) = 允许站点请求用户授予对附近蓝牙设备的访问权限

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultWebBluetoothGuardSetting
  - GP 名称: 控制 Web 蓝牙 API 的使用
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DefaultWebBluetoothGuardSetting
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultWebBluetoothGuardSetting
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultWebUsbGuardSetting
  #### 控制 WebUSB API 的使用
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  设置网站是否可以访问连接的 USB 设备。你可以完全阻止访问，或让网站在每次希望访问连接的 USB 时询问用户。

你可以对特定的 URL 模式覆盖此策略，方法是使用 [WebUsbAskForUrls](#webusbaskforurls) 和 [WebUsbBlockedForUrls](#webusbblockedforurls) 策略。

如果未配置此策略，默认情况下站点可以询问用户是否可以访问连接的 USB 设备(“AskWebUsb”)，并且用户可以更改此设置。

策略选项映射：

* BlockWebUsb (2) = 不允许任何站点通过 WebUSB API 请求对 USB 设备的访问

* AskWebUsb (3) = 允许站点请求用户授予对已连接 USB 设备的访问权限

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultWebUsbGuardSetting
  - GP 名称: 控制 WebUSB API 的使用
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DefaultWebUsbGuardSetting
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultWebUsbGuardSetting
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### FileSystemReadAskForUrls
  #### 在这些网站上允许通过文件系统 API 进行读取访问
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  如果设置该策略，则可以列出 URL 模式，指定哪些网站可以通过文件系统 API 要求用户授予他们对主机操作系统的文件系统中的文件或目录的读取访问权限。

如果未设置此策略，[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) 适用于所有网站(如果已设置)。否则，用户的个人设置将适用。

URL 式不能与 [FileSystemReadBlockedForUrls](#filesystemreadblockedforurls) 冲突。如果 URL 与两者都匹配，则这两个策略都不优先。

有关有效 url 模式的详细信息，请参阅 https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: FileSystemReadAskForUrls
  - GP 名称: 在这些网站上允许通过文件系统 API 进行读取访问
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\2 = "[*.]example.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: FileSystemReadAskForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### FileSystemReadBlockedForUrls
  #### 在这些网站上禁止通过文件系统 API 进行读取访问
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  如果设置此策略，则可以列出 URL 模式，指定哪些网站可以通过文件系统 API 要求用户授予他们对主机操作系统的文件系统中的文件或目录的读取访问权限。

如果未设置此策略，[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) 适用于所有网站(如果已设置)。否则，用户的个人设置将适用。

URL 式不能与 [FileSystemReadAskForUrls](#filesystemreadaskforurls) 冲突。如果 URL 与两者都匹配，则这两个策略都不优先。

有关有效 url 模式的详细信息，请参阅 https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: FileSystemReadBlockedForUrls
  - GP 名称: 在这些网站上禁止通过文件系统 API 进行读取访问
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\2 = "[*.]example.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: FileSystemReadBlockedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### FileSystemWriteAskForUrls
  #### 在这些网站上允许对文件和目录的写入访问
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  如果设置此策略，则可以列出 URL 模式，指定哪些网站可以要求用户授予他们对主机操作系统的文件系统中的文件或目录的写入访问权限。

如果未设置此策略，[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) 将应用于所有网站(如果已设置)。否则，用户的个人设置将适用。

URL 式不能与 [FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls) 冲突。如果 URL 与两者都匹配，则这两个策略都不优先。

有关有效 url 模式的详细信息，请参阅 https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: FileSystemWriteAskForUrls
  - GP 名称: 在这些网站上允许对文件和目录的写入访问
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\2 = "[*.]example.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: FileSystemWriteAskForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### FileSystemWriteBlockedForUrls
  #### 在这些网站上阻止对文件和目录的写入访问
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  如果设置此策略，则可以列出 URL 模式，指定哪些网站不能要求用户授予他们对主机操作系统的文件系统中的文件或目录的写入访问权限。

如果未设置此策略，[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) 将应用于所有网站(如果已设置)。否则，用户的个人设置将适用。

URL 式不能与 [FileSystemWriteAskForUrls](#filesystemwriteaskforurls) 冲突。如果 URL 与两者都匹配，则这两个策略都不优先。

有关有效 url 模式的详细信息，请参阅 https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: FileSystemWriteBlockedForUrls
  - GP 名称: 在这些网站上阻止对文件和目录的写入访问
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\2 = "[*.]example.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: FileSystemWriteBlockedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ImagesAllowedForUrls
  #### 允许使用这些站点上的图像
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  根据 URL 模式定义可显示图像的站点列表。

如果未配置此策略，则对所有站点使用 [DefaultImagesSetting](#defaultimagessetting) 策略(如果已设置)或用户个人配置中的全局默认值。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ImagesAllowedForUrls
  - GP 名称: 允许使用这些站点上的图像
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: ImagesAllowedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ImagesBlockedForUrls
  #### 在特定站点上阻止图像
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  根据 URL 模式定义不允许其显示图像的站点列表。

如果未配置此策略，则对所有站点使用 [DefaultImagesSetting](#defaultimagessetting) 策略(如果已设置)或用户个人配置中的全局默认值。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ImagesBlockedForUrls
  - GP 名称: 在特定站点上阻止图像
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: ImagesBlockedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### InsecureContentAllowedForUrls
  #### 对指定站点允许不安全内容
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 80

  #### 描述
  创建 URL 模式列表，以指定可以显示不安全混合内容(即 HTTPS 站点上的 HTTP 内容)的站点。

如果未配置此策略，可阻止的混合内容将被阻止，而可选择阻止的混合内容将得以升级。但是，用户可以设置例外，允许特定站点显示不安全的混合内容。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: InsecureContentAllowedForUrls
  - GP 名称: 对指定站点允许不安全内容
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\2 = "[*.]example.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: InsecureContentAllowedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### InsecureContentBlockedForUrls
  #### 对指定站点阻止不安全内容
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 80

  #### 描述
  创建 URL 模式列表，以指定不允许显示可阻止的(即活动的)混合内容(即 HTTPS 站点上的 HTTP 内容)的站点，以及将对其禁用可选择阻止的混合内容升级的站点。

如果未配置此策略，可阻止的混合内容将被阻止，而可选择阻止的混合内容将得以升级。但是，用户可以设置例外，允许特定站点显示不安全的混合内容。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: InsecureContentBlockedForUrls
  - GP 名称: 对指定站点阻止不安全内容
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\2 = "[*.]example.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: InsecureContentBlockedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### JavaScriptAllowedForUrls
  #### 在特定站点上允许 JavaScript
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  根据 URL 模式定义允许运行 JavaScript 的站点列表。

如果未配置此策略，则对所有站点使用 [DefaultJavaScriptSetting](#defaultjavascriptsetting) 策略(如果已设置)或用户个人配置中的全局默认值。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: JavaScriptAllowedForUrls
  - GP 名称: 在特定站点上允许 JavaScript
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: JavaScriptAllowedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### JavaScriptBlockedForUrls
  #### 在特定站点上阻止 JavaScript
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  根据 URL 模式定义不允许其运行 JavaScript 的站点列表。

如果未配置此策略，则对所有站点使用 [DefaultJavaScriptSetting](#defaultjavascriptsetting) 策略(如果已设置)或用户个人配置中的全局默认值。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: JavaScriptBlockedForUrls
  - GP 名称: 在特定站点上阻止 JavaScript
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: JavaScriptBlockedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### LegacySameSiteCookieBehaviorEnabled
  #### 启用默认的旧 SameSite cookie 行为设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 80

  #### 描述
  允许你将所有 cookie 恢复为旧的 SameSite 行为。如果恢复为旧行为，则会导致未指定 SameSite 属性的 cookie 被视为“SameSite=None”，并且会删除对于“SameSite=None”cookie 的具有“Secure”属性的要求。

如果未设置此策略，则未指定 SameSite 属性的 cookie 的默认行为将取决于 SameSite-by-default 功能的其他配置源。可以通过现场试用或通过在 edge://flags 中启用 same-site-by-default-cookies 标志来设置此功能。

策略选项映射：

* DefaultToLegacySameSiteCookieBehavior (1) = 针对所有站点上的 cookie 都恢复为旧 SameSite 行为

* DefaultToSameSiteByDefaultCookieBehavior (2) = 针对所有站点上的 cookie 都使用 SameSite-by-default 行为

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: LegacySameSiteCookieBehaviorEnabled
  - GP 名称: 启用默认的旧 SameSite cookie 行为设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: LegacySameSiteCookieBehaviorEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: LegacySameSiteCookieBehaviorEnabled
  - 示例值:
``` xml
<integer>1</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### LegacySameSiteCookieBehaviorEnabledForDomainList
  #### 针对指定站点上的 cookie 恢复为旧 SameSite 行为
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 80

  #### 描述
  为域匹配指定模式而设置的 cookie 将恢复为旧的 SameSite 行为。

如果恢复为旧行为，则会导致未指定 SameSite 属性的 cookie 被视为 "SameSite=None"，并且会删除对于 "SameSite=None" cookie 的具有 "Secure" 属性的要求。

如果未设置此策略，则将使用全局默认值。全局默认值还将用于你所指定模式未涵盖的域中的 cookie。

可以使用 [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) 策略来配置全局默认值。如果未设置 [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)，则将转向其他配置源来获取全局默认值。

请注意，你在此策略中列出的模式被视为域，而不是 URL，因此，你不应指定方案或端口。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: LegacySameSiteCookieBehaviorEnabledForDomainList
  - GP 名称: 针对指定站点上的 cookie 恢复为旧 SameSite 行为
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\1 = "www.example.com"
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\2 = "[*.]example.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: LegacySameSiteCookieBehaviorEnabledForDomainList
  - 示例值:
``` xml
<array>
  <string>www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### NotificationsAllowedForUrls
  #### 在特定站点上允许通知
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  可用于创建 URL 模式的列表，以便指定允许显示通知的站点。

如果未设置此策略，则将对所有站点使用全局默认值。此默认值将来自 [DefaultNotificationsSetting](#defaultnotificationssetting) 策略(如果已设置)或用户的个人配置。有关有效 URL 模式的详细信息，请参阅 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: NotificationsAllowedForUrls
  - GP 名称: 在特定站点上允许通知
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: NotificationsAllowedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### NotificationsBlockedForUrls
  #### 在特定站点上阻止通知
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  可用于创建 URL 模式的列表，以便指定不允许显示通知的站点。

如果未设置此策略，则将对所有站点使用全局默认值。此默认值将来自 [DefaultNotificationsSetting](#defaultnotificationssetting) 策略(如果已设置)或用户的个人配置。有关有效 URL 模式的详细信息，请参阅 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: NotificationsBlockedForUrls
  - GP 名称: 在特定站点上阻止通知
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: NotificationsBlockedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### PluginsAllowedForUrls
  #### 允许对特定站点使用 Adobe Flash 插件
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  根据 URL 模式定义可运行 Adobe Flash 插件的网站列表。

如果未配置此策略，则对所有用户使用 [DefaultPluginsSetting](#defaultpluginssetting) 策略的全局默认值(如果已设置)或用户的个人配置。

有关有效 URL 模式的详细信息，请参阅 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。但是，从 M85 开始，此策略不再支持主机中带有“* 和“[*.]”通配符的模式。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PluginsAllowedForUrls
  - GP 名称: 允许对特定站点使用 Adobe Flash 插件
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\2 = "http://contoso.edu:8080"

```


  #### Mac 信息和设置
  - 首选项密钥名称: PluginsAllowedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### PluginsBlockedForUrls
  #### 阻止特定站点上的 Adobe Flash 插件
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  根据 URL 模式定义阻止运行 Adobe Flash 的网站列表。

如果未配置此策略，则对所有用户使用 [DefaultPluginsSetting](#defaultpluginssetting) 策略的全局默认值(如果已设置)或用户的个人配置。

有关有效 URL 模式的详细信息，请参阅 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。但是，从 M85 开始，此策略不再支持主机中带有“* 和“[*.]”通配符的模式。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PluginsBlockedForUrls
  - GP 名称: 阻止特定站点上的 Adobe Flash 插件
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\2 = "http://contoso.edu:8080"

```


  #### Mac 信息和设置
  - 首选项密钥名称: PluginsBlockedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### PopupsAllowedForUrls
  #### 在特定站点上允许弹出窗口
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  根据 URL 模式定义可打开弹出窗口的站点列表。

如果未配置此策略，则对所有站点使用 [DefaultPopupsSetting](#defaultpopupssetting) 策略(如果已设置)或用户个人配置中的全局默认值。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PopupsAllowedForUrls
  - GP 名称: 在特定站点上允许弹出窗口
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: PopupsAllowedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### PopupsBlockedForUrls
  #### 在特定站点上阻止弹出窗口
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  根据 URL 模式定义被阻止打开弹出窗口的站点列表。

如果未配置此策略，则对所有站点使用 [DefaultPopupsSetting](#defaultpopupssetting) 策略(如果已设置)或用户个人配置中的全局默认值。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PopupsBlockedForUrls
  - GP 名称: 在特定站点上阻止弹出窗口
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: PopupsBlockedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### RegisteredProtocolHandlers
  #### 注册协议处理程序
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  设置此策略(仅推荐)以注册协议处理程序列表。此列表与用户注册的列表进行合并，并且都可使用。

要注册协议处理程序，请执行以下操作:

- 将协议属性设置为方案(例如 "mailto")
- 将 URL 属性设置为处理“协议”字段中指定方案的应用程序的 URL 属性。该模式可以包括已处理的 URL 所替换的“%s”占位符。

用户不能删除此策略注册的协议处理程序。但是，他们可以安装一个新的默认协议处理程序来替代现有的协议处理程序。

  #### 支持的功能:
  - 可以为必填字段: 否
  - 可以推荐: 是
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字典

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: RegisteredProtocolHandlers
  - GP 名称: 注册协议处理程序
  - GP 路径 (强制): 不适用
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/内容设置
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): 不适用
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: RegisteredProtocolHandlers
  - 值类型: REG_SZ
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [
  {
    "default": true, 
    "protocol": "mailto", 
    "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"
  }
]
```


  #### Mac 信息和设置
  - 首选项密钥名称: RegisteredProtocolHandlers
  - 示例值:
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
  

  [返回顶部](#microsoft-edge---策略)

  ### SpotlightExperiencesAndRecommendationsEnabled
  #### 选择用户是否可以接收 Microsoft 服务的自定义背景图像和文本、建议、通知、
和提示
  
  
  #### 支持的版本:
  - 在 Windows 自 86 或之后

  #### 描述
  选择用户是否可以接收 Microsoft 服务的自定义背景图片和文本、建议、通知和提示。

如果启用或未配置此设置，则将打开聚焦体验和建议。

如果禁用此设置，则聚焦体验和建议将关闭。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SpotlightExperiencesAndRecommendationsEnabled
  - GP 名称: 选择用户是否可以接收 Microsoft 服务的自定义背景图像和文本、建议、通知、
和提示
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: SpotlightExperiencesAndRecommendationsEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  

  [返回顶部](#microsoft-edge---策略)

  ### WebUsbAllowDevicesForUrls
  #### 授予特定站点访问权限以连接到特定 USB 设备
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许你设置 URL 列表，指定为哪些站点自动授予具有给定供应商和产品 ID 的 USB 设备的访问权限。为了使策略有效，列表中的每个项目都必须包含设备和 URL。设备中的每个项目都可以包含供应商 ID 和产品 ID 字段。任何被省略的 ID 均视为通配符，但有一个例外: 必须同时指定供应商 ID，才能指定产品 ID，否则策略将无效并被忽略。

USB 权限模型使用请求站点的 URL (“请求 URL”)和顶级框架网站的 URL (“嵌入 URL”)为请求 URL 授予 USB 设备的访问权限。当请求的网站加载到 iframe 中时，请求 URL 可能不同于嵌入 URL。因此，"urls" 字段最多可包含两个以逗号分隔的 URL 字符串，以便分别指定请求和嵌入 URL。如果仅指定了一个 URL，则当请求站点的 URL 与此 URL 匹配时，将向相应的 USB 设备授予访问权限，而无论嵌入状态如何。"urls" 中的 URL 必须是有效的 URL，否则将忽略该策略。

如果未设置此策略，则将对所有站点使用 [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) 策略(如果已设置)或用户个人配置中的全局默认值。

此策略中的 URL 模式不应与通过 [WebUsbBlockedForUrls](#webusbblockedforurls) 配置的 URL 冲突。如果存在冲突，此策略将优先于 [WebUsbBlockedForUrls](#webusbblockedforurls) 和 [WebUsbAskForUrls](#webusbaskforurls)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字典

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: WebUsbAllowDevicesForUrls
  - GP 名称: 授予特定站点访问权限以连接到特定 USB 设备
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: WebUsbAllowDevicesForUrls
  - 值类型: REG_SZ
  ##### 示例值:
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


  #### Mac 信息和设置
  - 首选项密钥名称: WebUsbAllowDevicesForUrls
  - 示例值:
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
  

  [返回顶部](#microsoft-edge---策略)

  ### WebUsbAskForUrls
  #### 在特定站点上允许 WebUSB
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  根据 URL 模式定义可以请求用户提供 USB 设备访问权限的站点列表。

如果未配置此策略，则对所有站点使用 [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) 策略(如果已设置)或用户个人配置中的全局默认值。

此策略中定义的 URL 模式不能与 [WebUsbBlockedForUrls](#webusbblockedforurls) 策略中配置的 URL 模式冲突 - 不能同时允许和阻止 URL。有关有效 URL 模式的详细信息，请参阅 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: WebUsbAskForUrls
  - GP 名称: 在特定站点上允许 WebUSB
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: WebUsbAskForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### WebUsbBlockedForUrls
  #### 在特定站点上阻止 WebUSB
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  根据 URL 模式定义无法请求用户授予 USB 设备访问权限的站点列表。

如果未配置此策略，则对所有站点使用 [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) 策略(如果已设置)或用户个人配置中的全局默认值。

此策略中的 URL 模式不能与 [WebUsbAskForUrls](#webusbaskforurls) 策略中配置的 URL 模式冲突。不能同时允许和阻止 URL。有关有效 URL 模式的详细信息，请参阅 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: WebUsbBlockedForUrls
  - GP 名称: 在特定站点上阻止 WebUSB
  - GP 路径 (强制): 管理模板/Microsoft Edge/内容设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: WebUsbBlockedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ## 启动、主页和新选项卡页 policies

  [返回顶部](#microsoft-edge---策略)

  ### HomepageIsNewTabPage
  #### 将新标签页设置为主页
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  在 Microsoft Edge 中配置默认主页。你可以将主页设置为你指定的 URL 或新标签页。

如果启用此策略，则新标签页将始终用作主页，并且会忽略主页 URL 位置。

如果禁用此策略，则用户的主页不能是新标签页，除非 URL 设置为 "edge://newtab"。

如果未配置，则用户可以选择新标签页是否是其主页。

此策略仅适用于已加入 Microsoft Active Directory 域的 Windows 实例、为设备管理注册的 Windows 10 专业版或企业版实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: HomepageIsNewTabPage
  - GP 名称: 将新标签页设置为主页
  - GP 路径 (强制): 管理模板/Microsoft Edge/启动、主页和新选项卡页
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/启动、主页和新选项卡页
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: HomepageIsNewTabPage
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: HomepageIsNewTabPage
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### HomepageLocation
  #### 配置主页 URL
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  在 Microsoft Edge 中配置默认主页 URL。

主页是通过主页按钮打开的页面。启动时打开的页面由 [RestoreOnStartup](#restoreonstartup) 策略进行控制。

你可以在此处设置 URL 或设置主页以打开新标签页。如果选择打开新标签页，则此策略不会生效。

如果启用此策略，则用户无法更改其主页 URL，但可以选择使用新标签页作为主页。

如果禁用或未配置此策略，则只要未启用 [HomepageIsNewTabPage](#homepageisnewtabpage) 策略，用户就可以自行选择主页。

此策略仅适用于已加入 Microsoft Active Directory 域的 Windows 实例、为设备管理注册的 Windows 10 专业版或企业版实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: HomepageLocation
  - GP 名称: 配置主页 URL
  - GP 路径 (强制): 管理模板/Microsoft Edge/启动、主页和新选项卡页
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/启动、主页和新选项卡页
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: HomepageLocation
  - 值类型: REG_SZ
  ##### 示例值:
```
"https://www.contoso.com"
```


  #### Mac 信息和设置
  - 首选项密钥名称: HomepageLocation
  - 示例值:
``` xml
<string>https://www.contoso.com</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### NewTabPageAllowedBackgroundTypes
  #### 配置允许用于新选项卡页面布局的背景类型
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  你可以在 Microsoft Edge 中配置新选项卡页面布局上允许使用的背景图像类型。

如果未配置此策略，则会启用新选项卡页上的所有背景图像类型。

策略选项映射：

* DisableImageOfTheDay (1) = 禁用每日背景图像类型

* DisableCustomImage (2) = 禁用自定义背景图像类型

* DisableAll (3) = 禁用所有背景图像类型

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: NewTabPageAllowedBackgroundTypes
  - GP 名称: 配置允许用于新选项卡页面布局的背景类型
  - GP 路径 (强制): 管理模板/Microsoft Edge/启动、主页和新选项卡页
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: NewTabPageAllowedBackgroundTypes
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: NewTabPageAllowedBackgroundTypes
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### NewTabPageCompanyLogo
  #### 设置新的选项卡页公司徽标 (过时)
  
  >过时: 此策略已过时，在 Microsoft Edge 85 之后无法使用。
  #### 支持的版本:
  - 在 Windows 后，在 macOS 和 79 上 85

  #### 描述
  由于操作要求发生变化，此策略无法按预期发挥作用。因此，它已过时，不应使用。

指定要在 Microsoft Edge 中的新选项卡页上使用的公司徽标。

此策略应配置为以 JSON 格式表示徽标的字符串。例如: { "default_logo": { "url": "https://www.contoso.com/logo.png", "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29" }, "light_logo": { "url": "https://www.contoso.com/light_logo.png", "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737" } }

你可以通过指定 URL 来配置此策略，Microsoft Edge 可以通过此 URL 下载徽标以及用于验证下载完整性的加密哈希(SHA-256)。徽标必须采用 PNG 或 SVG 格式，并且文件大小不得超过 16 MB。下载并缓存徽标后，只要 URL 或哈希发生更改，就会重新下载徽标。此 URL 必须可访问，并且无需进行任何身份验证。

"default_logo" 是必需的，将在没有背景图像时使用。如果提供了 "light_logo"，则将在用户的新选项卡页具有背景图像时使用。我们建议使用具有左对齐且垂直居中的透明背景的水平徽标。徽标的最小高度应为 32 像素，纵横比为 1:1 到 4:1。"default_logo" 应与黑/白背景具有适当的对比度，而 "light_logo" 应与背景图像具有适当的对比度。

如果启用此策略，则 Microsoft Edge 将下载指定的徽标并在新选项卡页上显示此徽标。用户不能覆盖或隐藏徽标。

如果禁用或未配置此策略，则 Microsoft Edge 将不在新选项卡页上显示公司徽标或 Microsoft 徽标。

有关确定 SHA-256 哈希的帮助，请参阅 https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/get-filehash。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字典

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: NewTabPageCompanyLogo
  - GP 名称: 设置新的选项卡页公司徽标 (过时)
  - GP 路径 (强制): 管理模板/Microsoft Edge/启动、主页和新选项卡页
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: NewTabPageCompanyLogo
  - 值类型: REG_SZ
  ##### 示例值:
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


  #### Mac 信息和设置
  - 首选项密钥名称: NewTabPageCompanyLogo
  - 示例值:
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
  

  [返回顶部](#microsoft-edge---策略)

  ### NewTabPageHideDefaultTopSites
  #### 从新选项卡页中隐藏默认的热门站点
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  在 Microsoft Edge 中的新标签页中隐藏默认热门站点。

如果将此策略设置为 True，则默认热门站点磁贴将隐藏。

如果将此策略设置为 False 或未配置此策略，则默认热门站点磁贴将保持可见。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: NewTabPageHideDefaultTopSites
  - GP 名称: 从新选项卡页中隐藏默认的热门站点
  - GP 路径 (强制): 管理模板/Microsoft Edge/启动、主页和新选项卡页
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: NewTabPageHideDefaultTopSites
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: NewTabPageHideDefaultTopSites
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### NewTabPageLocation
  #### 配置新的选项卡页 URL
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  为新标签页配置默认 URL。

此策略可决定创建新标签页时(包括打开新窗口时)打开的页面。如果启动页面设置为打开新标签页，则此策略也会影响启动页面。

此策略无法决定启动时打开哪个页面；启动时打开哪个页面由 [RestoreOnStartup](#restoreonstartup) 策略控制。如果主页设置为打开新标签页，则它也不会影响主页。

如果未配置此策略，则使用默认的新标签页。

如果配置此策略*以及* [NewTabPageSetFeedType](#newtabpagesetfeedtype) 策略，则此策略优先。

如果提供的 URL 无效，新标签页将打开 about://blank。

此策略仅适用于已加入 Microsoft Active Directory 域的 Windows 实例、为设备管理注册的 Windows 10 专业版或企业版实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: NewTabPageLocation
  - GP 名称: 配置新的选项卡页 URL
  - GP 路径 (强制): 管理模板/Microsoft Edge/启动、主页和新选项卡页
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/启动、主页和新选项卡页
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: NewTabPageLocation
  - 值类型: REG_SZ
  ##### 示例值:
```
"https://www.fabrikam.com"
```


  #### Mac 信息和设置
  - 首选项密钥名称: NewTabPageLocation
  - 示例值:
``` xml
<string>https://www.fabrikam.com</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### NewTabPageManagedQuickLinks
  #### 设置新标签页快速链接
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 79

  #### 描述
  默认情况下，Microsoft Edge 在新标签页上显示快速链接，包括用户添加的快捷方式和基于浏览历史记录的热门站点。使用此策略，可以在新标签页上配置最多三个快速链接磁贴，以 JSON 对象的形式表示:

[ { "url": "https://www.contoso.com", "title": "Contoso Portal", "pinned": true/false }, ... ]

"URL" 字段为必填字段；“标题”和“已固定”为可选字段。如果未提供“标题”，则将 URL 用作默认标题。如果未提供“已固定”，则默认值为 false。

Microsoft Edge 按所列顺序从左到右显示这些项，并将所有已固定的磁贴排在未固定的磁贴之前。

如果此策略设置为强制执行，则会忽略“已固定”字段，并固定所有磁贴。用户无法删除磁贴，磁贴将始终显示在快速链接列表的前面。

如果此策略设置为推荐，则已固定的磁贴将保留在列表中，但用户可以编辑和删除它们。未固定的快速链接磁贴的使用方式与默认的热门站点类似，如果用户访问其他网站次数更多，则会将其从列表中清除。通过此策略将未固定的链接应用到现有浏览器用户配置时，链接可能根本不会显示，具体取决于它们在用户的浏览历史记录中的排名情况。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字典

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: NewTabPageManagedQuickLinks
  - GP 名称: 设置新标签页快速链接
  - GP 路径 (强制): 管理模板/Microsoft Edge/启动、主页和新选项卡页
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/启动、主页和新选项卡页
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: NewTabPageManagedQuickLinks
  - 值类型: REG_SZ
  ##### 示例值:
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


  #### Mac 信息和设置
  - 首选项密钥名称: NewTabPageManagedQuickLinks
  - 示例值:
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
  

  [返回顶部](#microsoft-edge---策略)

  ### NewTabPagePrerenderEnabled
  #### 启用新标签页的预加载以提高呈现速度
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 85

  #### 描述
  如果配置此策略，则会启用预加载“新建”选项卡页面，并且用户无法更改此设置。如果未配置此策略，则将启用预加载，并且用户可以更改此设置。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: NewTabPagePrerenderEnabled
  - GP 名称: 启用新标签页的预加载以提高呈现速度
  - GP 路径 (强制): 管理模板/Microsoft Edge/启动、主页和新选项卡页
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/启动、主页和新选项卡页
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: NewTabPagePrerenderEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: NewTabPagePrerenderEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### NewTabPageSetFeedType
  #### 配置 Microsoft Edge 新标签页体验
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 79

  #### 描述
  允许你为新标签页选择 Microsoft 资讯或是 Office 365 信息提要体验。

将此策略设置为“News”时，用户将在新标签页上获得 Microsoft 资讯信息提要体验。

将此策略设置为“Office”时，通过 Azure Active Directory 登录浏览器的用户将在新标签页上获得 Office 365 信息提要体验。

如果禁用或未配置此策略:

- 通过 Azure Active Directory 登录浏览器的用户将获得 Office 365 新标签页信息提要体验，以及标准的新标签页信息提要体验。

- 未通过 Azure Active Directory 登录浏览器的用户将获得标准的新标签页体验。

如果配置此策略 *以及* [NewTabPageLocation](#newtabpagelocation) 策略，则 [NewTabPageLocation](#newtabpagelocation) 优先。

默认设置: 已禁用或未配置。

策略选项映射：

* News (0) = Microsoft 资讯信息提要体验

* Office (1) = Office 365 信息提要体验

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: NewTabPageSetFeedType
  - GP 名称: 配置 Microsoft Edge 新标签页体验
  - GP 路径 (强制): 管理模板/Microsoft Edge/启动、主页和新选项卡页
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/启动、主页和新选项卡页
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: NewTabPageSetFeedType
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: NewTabPageSetFeedType
  - 示例值:
``` xml
<integer>0</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### RestoreOnStartup
  #### 要在启动时执行的操作
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定 Microsoft Edge 在启动时的行为方式。

如果希望在启动时始终打开新标签页，请选择“RestoreOnStartupIsNewTabPage”。

如果要重新打开上次 Microsoft Edge 关闭时打开的 URL，请选择“RestoreOnStartupIsLastSession”。浏览会话将按原样还原。请注意，此选项将禁用某些依赖会话或在退出时执行操作的设置(如“退出时清除浏览数据”或仅限于会话的 cookie)。

如果要打开一组特定的 URL，请选择“RestoreOnStartupIsURLs”。

禁用此设置相当于未配置此设置。用户将能够在 Microsoft Edge 中对其进行更改。

此策略仅适用于已加入 Microsoft Active Directory 域的 Windows 实例、为设备管理注册的 Windows 10 专业版或企业版实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例。

策略选项映射：

* RestoreOnStartupIsNewTabPage (5) = 打开新标签页

* RestoreOnStartupIsLastSession (1) = 还原上一个会话

* RestoreOnStartupIsURLs (4) = 打开 URL 列表

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: RestoreOnStartup
  - GP 名称: 要在启动时执行的操作
  - GP 路径 (强制): 管理模板/Microsoft Edge/启动、主页和新选项卡页
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/启动、主页和新选项卡页
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: RestoreOnStartup
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000004
```


  #### Mac 信息和设置
  - 首选项密钥名称: RestoreOnStartup
  - 示例值:
``` xml
<integer>4</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### RestoreOnStartupURLs
  #### 浏览器启动时打开的站点
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定要在浏览器启动时自动打开的网站的列表。如果未配置此策略，则在启动时不打开任何站点。

此策略仅在将 [RestoreOnStartup](#restoreonstartup) 策略设置为“打开 URL 列表”(4)时有效。

此策略仅适用于已加入 Microsoft Active Directory 域的 Windows 实例、为设备管理注册的 Windows 10 专业版或企业版实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: RestoreOnStartupURLs
  - GP 名称: 浏览器启动时打开的站点
  - GP 路径 (强制): 管理模板/Microsoft Edge/启动、主页和新选项卡页
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/启动、主页和新选项卡页
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐\RestoreOnStartupURLs
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\1 = "https://contoso.com"
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\2 = "https://www.fabrikam.com"

```


  #### Mac 信息和设置
  - 首选项密钥名称: RestoreOnStartupURLs
  - 示例值:
``` xml
<array>
  <string>https://contoso.com</string>
  <string>https://www.fabrikam.com</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ShowHomeButton
  #### 在工具栏上显示“主页”按钮
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  在 Microsoft Edge 的工具栏上显示主页按钮。

启用此策略可始终显示主页按钮。禁用此策略将从不显示此按钮。

如果未配置此策略，则用户可以选择是否显示主页按钮。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ShowHomeButton
  - GP 名称: 在工具栏上显示“主页”按钮
  - GP 路径 (强制): 管理模板/Microsoft Edge/启动、主页和新选项卡页
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/启动、主页和新选项卡页
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: ShowHomeButton
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ShowHomeButton
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ## 密码管理器和保护 policies

  [返回顶部](#microsoft-edge---策略)

  ### PasswordManagerEnabled
  #### 启用将密码保存到密码管理器
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  启用 Microsoft Edge 以保存用户密码。

如果启用此策略，则用户可以保存其在 Microsoft Edge 中的密码。他们下次访问站点时，Microsoft Edge 将自动输入密码。

如果禁用此策略，则用户将无法保存新的密码，但仍可使用以前保存的密码。

如果启用或禁用此策略，则用户不能在 Microsoft Edge 中更改或覆盖它。如果未配置此策略，则用户可以保存密码，也可以关闭此功能。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PasswordManagerEnabled
  - GP 名称: 启用将密码保存到密码管理器
  - GP 路径 (强制): 管理模板/Microsoft Edge/密码管理器和保护
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/密码管理器和保护
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: PasswordManagerEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: PasswordManagerEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### PasswordMonitorAllowed
  #### 如果发现用户的密码不安全，则向用户发出警报
  
  
  #### 支持的版本:
  - 在 Windows 自 85 或之后

  #### 描述
  允许 Microsoft Edge 监视用户密码。

如果你启用此策略，并且用户同意启用该策略，则如果发现存储在 Microsoft Edge 中的任何密码不安全，则会向用户发出警报。Microsoft Edge 将显示警报，并且此信息也将在“设置”>“密码”>“密码监视器”中提供。

如果禁用此策略，则不会要求用户授予启用此功能的权限。他们的密码不会被扫描，也不会收到警报。

如果启用或未配置该策略，则用户可以打开或关闭此功能。

若要了解有关 Microsoft Edge 如何找到不安全密码的详细信息，请参阅 [https://go.microsoft.com/fwlink/?linkid=2133833](https://go.microsoft.com/fwlink/?linkid=2133833)

其他指南:

可以将此政策设置为“推荐”和“强制”两种，但是带有重要标注。

强制启用: 鉴于个人用户同意是为给定用户启用此功能的前提，因此此策略没有强制启用设置。如果将该策略设置为强制启用，则“设置”中的 UI 不会更改，并且以下错误消息将显示在 edge://policy 中

示例错误状态消息:“此策略值将被忽略，因为密码监视器器需要个人用户同意才能打开它。你可以要求组织中的用户转至“设置”>“用户配置”>“密码”并打开功能。”

建议启用: 如果将策略设置为建议启用，则“设置”中的用户界面将保持“关闭”状态，但旁边会出现一个公文包图标，并在悬停时显示此说明:“你的组织建议为此设置指定一个特定值，而你选择了其他值”

强制和建议禁用: 这两种状态都将正常工作，并向用户显示常用标题。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PasswordMonitorAllowed
  - GP 名称: 如果发现用户的密码不安全，则向用户发出警报
  - GP 路径 (强制): 管理模板/Microsoft Edge/密码管理器和保护
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/密码管理器和保护
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: PasswordMonitorAllowed
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  

  [返回顶部](#microsoft-edge---策略)

  ### PasswordProtectionChangePasswordURL
  #### 配置更改密码 URL
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  配置更改密码 URL (仅限 HTTP 和 HTTPS 方案)。

密码保护服务会将用户定向到此 URL，以便用户在浏览器中看到警告后更改其密码。

如果启用此策略，则密码保护服务会将用户定向到此 URL 以便其更改密码。

如果禁用或未配置此策略，则密码保护服务不会将用户重定向到更改密码 URL。

此策略仅适用于已加入 Microsoft Active Directory 域的 Windows 实例、为设备管理注册的 Windows 10 专业版或企业版实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PasswordProtectionChangePasswordURL
  - GP 名称: 配置更改密码 URL
  - GP 路径 (强制): 管理模板/Microsoft Edge/密码管理器和保护
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: PasswordProtectionChangePasswordURL
  - 值类型: REG_SZ
  ##### 示例值:
```
"https://contoso.com/change_password.html"
```


  #### Mac 信息和设置
  - 首选项密钥名称: PasswordProtectionChangePasswordURL
  - 示例值:
``` xml
<string>https://contoso.com/change_password.html</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### PasswordProtectionLoginURLs
  #### 配置密码保护服务应捕获密码加盐哈希的企业登录 URL 列表
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  配置企业登录 URL 列表（仅限 HTTP 和 HTTPS 方案），其中 Microsoft Edge 应捕获密码盐渍哈希并将其用于密码重用检测。

如果启用此策略，则密码保护服务将捕获已定义 URL 上的密码指纹。

如果禁用或未配置此策略，则不会捕获密码指纹。

此策略仅适用于已加入 Microsoft Active Directory 域的 Windows 实例、为设备管理注册的 Windows 10 专业版或企业版实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PasswordProtectionLoginURLs
  - GP 名称: 配置密码保护服务应捕获密码加盐哈希的企业登录 URL 列表
  - GP 路径 (强制): 管理模板/Microsoft Edge/密码管理器和保护
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\1 = "https://contoso.com/login.html"
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\2 = "https://login.contoso.com"

```


  #### Mac 信息和设置
  - 首选项密钥名称: PasswordProtectionLoginURLs
  - 示例值:
``` xml
<array>
  <string>https://contoso.com/login.html</string>
  <string>https://login.contoso.com</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### PasswordProtectionWarningTrigger
  #### 配置密码保护警告触发器
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许你控制何时触发密码保护警告。用户在潜在可疑站点上重复使用受保护的密码时，密码保护功能会提醒用户。

你可以使用 [PasswordProtectionLoginURLs](#passwordprotectionloginurls) 和 [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl) 策略来配置要保护的密码。

例外: [PasswordProtectionLoginURLs](#passwordprotectionloginurls) 和 [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl) 中所列站点以及 [SmartScreenAllowListDomains](#smartscreenallowlistdomains) 中所列站点的密码不会触发密码保护警告。

如果设置为“PasswordProtectionWarningOff”，则不会显示密码保护警告。

如果设置为“PasswordProtectionWarningOnPasswordReuse”，则当用户在未列入允许列表的站点上重复使用受保护的密码时，会显示密码保护警告。

如果禁用或未配置此策略，则不显示警告触发器。

策略选项映射：

* PasswordProtectionWarningOff (0) = 密码保护警告处于关闭状态

* PasswordProtectionWarningOnPasswordReuse (1) = 密码重用将触发密码保护警告

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PasswordProtectionWarningTrigger
  - GP 名称: 配置密码保护警告触发器
  - GP 路径 (强制): 管理模板/Microsoft Edge/密码管理器和保护
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: PasswordProtectionWarningTrigger
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: PasswordProtectionWarningTrigger
  - 示例值:
``` xml
<integer>1</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ## 应用程序防护设置 policies

  [返回顶部](#microsoft-edge---策略)

  ### ApplicationGuardContainerProxy
  #### 应用程序防护容器代理
  
  
  #### 支持的版本:
  - 在 Windows 自 84 或之后

  #### 描述
  配置 Microsoft Edge 应用程序防护的代理设置。
 如果启用此策略，Microsoft Edge 应用程序防护会忽略代理配置的其他来源。

如果未配置此策略，Microsoft Edge 应用程序防护将使用主机的代理配置。

此策略不会影响应用程序防护(主机)外部的 Microsoft Edge 代理配置。

在 ProxyMode 字段中，可指定 Microsoft Edge 应用程序防护使用的代理服务器。

ProxyPacUrl 字段是指向代理 .pac 文件的 URL。

ProxyServer 字段是代理服务器的 URL。

如果选择“direct”值作为“ProxyMode”，则所有其他字段都将被忽略。

如果选择“auto_detect”值作为“ProxyMode”，则所有其他字段都将被忽略。

如果选择“fixed_servers”值作为“ProxyMode”，则将使用“ProxyServer”字段。

如果选择“pac_script”值作为“ProxyMode”，则将使用“ProxyPacUrl”字段。

有关通过双重代理确定应用程序防护流量的更多信息，请访问 [https://go.microsoft.com/fwlink/?linkid=2134653](https://go.microsoft.com/fwlink/?linkid=2134653)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字典

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ApplicationGuardContainerProxy
  - GP 名称: 应用程序防护容器代理
  - GP 路径 (强制): 管理模板/Microsoft Edge/应用程序防护设置
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ApplicationGuardContainerProxy
  - 值类型: REG_SZ
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  

  [返回顶部](#microsoft-edge---策略)

  ## 打印 policies

  [返回顶部](#microsoft-edge---策略)

  ### DefaultPrinterSelection
  #### 默认打印机选择规则
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  替代 Microsoft Edge 默认打印机选择规则。此策略确定在 Microsoft Edge 中选择默认打印机的规则，用户首次尝试打印页面时需要进行此操作。

设置此策略后，Microsoft Edge 会尝试查找与所有指定属性都匹配的打印机，并将其用作默认打印机。如果有多台打印机符合条件，则使用第一台匹配的打印机。

如果未配置此策略或在超时期限内未找到匹配的打印机，则打印机默认为内置 PDF 打印机，如果 PDF 打印机不可用，则默认为没有打印机。

该值被解析为 JSON 对象，遵循以下架构: { "type": "object", "properties": { "idPattern": { "description": "Regular expression to match printer id.", "type": "string" }, "namePattern": { "description": "Regular expression to match printer display name.", "type": "string" } } }

省略字段意味着所有值都匹配；例如，如果未指定连接，则“打印预览”将开始发现各种本地打印机。正则表达式模式必须遵循 JavaScript RegExp 语法，并且匹配项区分大小写。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultPrinterSelection
  - GP 名称: 默认打印机选择规则
  - GP 路径 (强制): 管理模板/Microsoft Edge/打印
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DefaultPrinterSelection
  - 值类型: REG_SZ
  ##### 示例值:
```
"{ \"idPattern\": \".*public\", \"namePattern\": \".*Color\" }"
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultPrinterSelection
  - 示例值:
``` xml
<string>{ "idPattern": ".*public", "namePattern": ".*Color" }</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### PrintHeaderFooter
  #### 打印页眉和页脚
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  在打印对话框中强制开启或关闭“页眉和页脚”。

如果未配置此策略，则用户可以决定是否打印页眉和页脚。

如果禁用此策略，则用户无法打印页眉和页脚。

如果启用此策略，则用户始终打印页眉和页脚。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PrintHeaderFooter
  - GP 名称: 打印页眉和页脚
  - GP 路径 (强制): 管理模板/Microsoft Edge/打印
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/打印
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: PrintHeaderFooter
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: PrintHeaderFooter
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### PrintPreviewUseSystemDefaultPrinter
  #### 将系统的默认打印机设置为默认打印机
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  告诉 Microsoft Edge 使用系统默认打印机作为“打印预览”中的默认选项，而不是使用最近使用过的打印机。

如果禁用或未配置此策略，则“打印预览”使用最近使用过的打印机作为默认目标选项。

如果启用此策略，则“打印预览”使用 OS 系统默认打印机作为默认目标选项。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PrintPreviewUseSystemDefaultPrinter
  - GP 名称: 将系统的默认打印机设置为默认打印机
  - GP 路径 (强制): 管理模板/Microsoft Edge/打印
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/打印
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: PrintPreviewUseSystemDefaultPrinter
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: PrintPreviewUseSystemDefaultPrinter
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### PrintingEnabled
  #### 启用打印
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许在 Microsoft Edge 中进行打印，并阻止用户更改此设置。

如果启用此策略或未配置此策略，则用户可以打印。

如果禁用此策略，则用户无法通过 Microsoft Edge 进行打印。在扳手菜单、扩展、JavaScript 应用程序等位置中禁用了打印。用户仍然可以通过打印时绕过 Microsoft Edge 的插件进行打印。例如，某些 Adobe Flash 应用程序的上下文菜单中具有打印选项，此策略未涵盖此选项。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PrintingEnabled
  - GP 名称: 启用打印
  - GP 路径 (强制): 管理模板/Microsoft Edge/打印
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: PrintingEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: PrintingEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### PrintingPaperSizeDefault
  #### 默认打印页面大小
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  覆盖默认打印页面大小。

如果列表中没有所需的纸张尺寸，name 应包含其中一种列出的格式或“自定义”格式。如果提供了“自定义”值，则应指定 custom_size 属性。它描述了所需的高度和宽度(以千分尺为单位)。否则不应指定 custom_size 属性。违反这些规则的策略将被忽略。

如果页面大小在用户选择的打印机上不可用，则忽略此策略。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字典

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PrintingPaperSizeDefault
  - GP 名称: 默认打印页面大小
  - GP 路径 (强制): 管理模板/Microsoft Edge/打印
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: PrintingPaperSizeDefault
  - 值类型: REG_SZ
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\PrintingPaperSizeDefault = {
  "custom_size": {
    "height": 297000, 
    "width": 210000
  }, 
  "name": "custom"
}
```


  #### Mac 信息和设置
  - 首选项密钥名称: PrintingPaperSizeDefault
  - 示例值:
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
  

  [返回顶部](#microsoft-edge---策略)

  ### UseSystemPrintDialog
  #### 使用系统打印对话框打印
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  显示系统打印对话框而不是打印预览。

如果启用此策略，那么当用户打印页面时，Microsoft Edge 将打开系统打印对话框而不是内置打印预览。

如果未配置或禁用此策略，则打印命令会触发 Microsoft Edge 打印预览屏幕。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: UseSystemPrintDialog
  - GP 名称: 使用系统打印对话框打印
  - GP 路径 (强制): 管理模板/Microsoft Edge/打印
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: UseSystemPrintDialog
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: UseSystemPrintDialog
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ## 扩展 policies

  [返回顶部](#microsoft-edge---策略)

  ### ExtensionAllowedTypes
  #### 配置允许的扩展类型
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  控制可以安装哪些扩展类型并限制运行时访问。

此设置定义允许的扩展类型以及它们可以与之交互的主机。值是一个字符串列表，每个字符串都应为以下其中一项: "extension"、"theme"、"user_script" 和 "hosted_app"。有关这些类型的详细信息，请参阅 Microsoft Edge 扩展文档。

请注意，此策略还影响将要使用 [ExtensionInstallForcelist](#extensioninstallforcelist) 策略强制安装的扩展。

如果启用此策略，则仅安装与列表中的类型匹配的扩展。

如果未配置此策略，则不会强制实施针对可接受扩展类型的限制。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ExtensionAllowedTypes
  - GP 名称: 配置允许的扩展类型
  - GP 路径 (强制): 管理模板/Microsoft Edge/扩展
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes\1 = "hosted_app"

```


  #### Mac 信息和设置
  - 首选项密钥名称: ExtensionAllowedTypes
  - 示例值:
``` xml
<array>
  <string>hosted_app</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ExtensionInstallAllowlist
  #### 允许安装特定扩展
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  默认情况下允许所有扩展。但是，如果通过将 "ExtensionInstallBlockList" 策略设置为 "*" 来阻止所有扩展，则用户只能安装此策略中定义的扩展。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ExtensionInstallAllowlist
  - GP 名称: 允许安装特定扩展
  - GP 路径 (强制): 管理模板/Microsoft Edge/扩展
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\2 = "extension_id2"

```


  #### Mac 信息和设置
  - 首选项密钥名称: ExtensionInstallAllowlist
  - 示例值:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ExtensionInstallBlocklist
  #### 控制哪些扩展不能安装
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  列出用户不能在 Microsoft Edge 中安装的特定扩展。部署此策略时，此列表中以前安装的任何扩展都将被禁用，并且用户将无法启用它们。如果从被阻止的扩展列表中删除某个项目，该扩展将在以前安装的任何位置自动重新启用。

使用 "*" 可阻止允许列表中未明确列出的所有扩展。

如果未配置此策略，则用户可以在 Microsoft Edge 中安装任何扩展。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ExtensionInstallBlocklist
  - GP 名称: 控制哪些扩展不能安装
  - GP 路径 (强制): 管理模板/Microsoft Edge/扩展
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\2 = "extension_id2"

```


  #### Mac 信息和设置
  - 首选项密钥名称: ExtensionInstallBlocklist
  - 示例值:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ExtensionInstallForcelist
  #### 控制无提示安装的扩展
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定静默安装、无需用户交互以及用户无法卸载或禁用(“强制安装”)的扩展。系统会隐式授予扩展请求的所有权限，包括将来版本的扩展所请求的任何附加权限，无需用户进行交互。此外，系统还会为 enterprise.deviceAttributes 和 enterprise.platformKeys 扩展 API 授予权限。(这两个 API 仅对强制安装的扩展可用。)

此策略优先于可能存在冲突的 [ExtensionInstallBlocklist](#extensioninstallblocklist) 策略。当你从强制安装列表中取消某个扩展时，Microsoft Edge 将自动卸载该扩展。

对于非以下任一项的实例，强制安装仅限于 Microsoft Edge 加载项网站中列出的应用和扩展: 已加入 Microsoft Active Directory 域的 Windows 实例或已注册用于设备管理的 Windows 10 专业版或企业版实例，以及通过 MDM 管理或通过 MCX 加入域的 macOS 实例。

请注意，用户可以使用开发人员工具(可能会显示扩展功能异常)修改任何扩展的源代码。如果你担心这一点，请设置 [DeveloperToolsAvailability](#developertoolsavailability) 策略。

使用以下格式将扩展添加到列表中:

[extensionID];[updateURL]

- extensionID - 开发人员模式下在 edge://extensions 上找到的 32 个字母的字符串。

- updateURL (可选)是应用或扩展的更新清单 XML 文档的地址，如 [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043) 中所述。如果要从 Chrome Web Store 安装扩展，请提供 Chrome Web Store 更新 URL: https://clients2.google.com/service/update2/crx。请注意，此策略中设置的更新 URL 仅用于初始安装；此扩展的后续更新使用扩展清单中指示的更新 URL。如果未设置 updateURL，则假定扩展位于 Microsoft Store 中，并使用以下更新 URL (https://edge.microsoft.com/extensionwebstorebase/v1/crx)。

例如，gggmmkjegpiggikcnhidnjjhmicpibll;https://edge.microsoft.com/extensionwebstorebase/v1/crx 从 Microsoft Store“更新”URL 安装 Microsoft Online 应用。有关托管扩展的详细信息，请参阅: [https://go.microsoft.com/fwlink/?linkid=2095044](https://go.microsoft.com/fwlink/?linkid=2095044)。

如果未配置此策略，则不会自动安装扩展，并且用户可以卸载 Microsoft Edge 中的任何扩展。

请注意，此策略不适用于 InPrivate 模式。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ExtensionInstallForcelist
  - GP 名称: 控制无提示安装的扩展
  - GP 路径 (强制): 管理模板/Microsoft Edge/扩展
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\1 = "gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\2 = "abcdefghijklmnopabcdefghijklmnop"

```


  #### Mac 信息和设置
  - 首选项密钥名称: ExtensionInstallForcelist
  - 示例值:
``` xml
<array>
  <string>gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx</string>
  <string>abcdefghijklmnopabcdefghijklmnop</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ExtensionInstallSources
  #### 配置扩展和用户脚本安装源
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  定义可以安装扩展和主题的 URL。

默认情况下，用户必须为要安装的每个扩展或脚本下载 *.crx 文件，然后将其拖到 Microsoft Edge 设置页面上。此策略允许特定 URL 针对用户使用/安装扩展或脚本。

此列表中的每个项目都是扩展样式匹配模式(请参阅 [https://go.microsoft.com/fwlink/?linkid=2095039](https://go.microsoft.com/fwlink/?linkid=2095039))。用户可以从任何与此列表中的项匹配的 URL 轻松安装项目。这些模式必须允许 *.crx 文件的位置，以及从中开始下载的页面(也就是引用站点)。

[ExtensionInstallBlocklist](#extensioninstallblocklist) 策略优先于此策略。阻止名单中的任何扩展都不会安装，即使来自此列表中的站点也不例外。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ExtensionInstallSources
  - GP 名称: 配置扩展和用户脚本安装源
  - GP 路径 (强制): 管理模板/Microsoft Edge/扩展
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources\1 = "https://corp.contoso.com/*"

```


  #### Mac 信息和设置
  - 首选项密钥名称: ExtensionInstallSources
  - 示例值:
``` xml
<array>
  <string>https://corp.contoso.com/*</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ExtensionSettings
  #### 配置扩展管理设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  配置 Microsoft Edge 的扩展管理设置。

此策略控制多个设置，包括任何现有扩展相关策略所控制的设置。如果同时设置了此策略和任何旧策略，则此策略将替代旧策略。

此策略会将扩展 ID 或更新 URL 映射到其配置。对于扩展 ID，此配置仅应用于指定的扩展。请设置特殊 ID "*" 的默认配置，以应用于此策略中未明确列出的所有扩展。对于更新 URL，此配置将应用于在此扩展的清单中明确声明的更新 URL 的所有扩展，如 [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043) 中所述。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字典

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ExtensionSettings
  - GP 名称: 配置扩展管理设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/扩展
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ExtensionSettings
  - 值类型: REG_SZ
  ##### 示例值:
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


  #### Mac 信息和设置
  - 首选项密钥名称: ExtensionSettings
  - 示例值:
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
  

  [返回顶部](#microsoft-edge---策略)

  ## 本机消息 policies

  [返回顶部](#microsoft-edge---策略)

  ### NativeMessagingAllowlist
  #### 控制用户可以使用的本机消息传递主机
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  列出用户可以在 Microsoft Edge 中使用的特定本地消息传递主机。

默认情况下，允许使用所有本地消息传递主机。如果将 [NativeMessagingBlocklist](#nativemessagingblocklist) 策略设置为 *，则将阻止所有本地消息传递主机，并且仅加载此处列出的本地消息传递主机。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: NativeMessagingAllowlist
  - GP 名称: 控制用户可以使用的本机消息传递主机
  - GP 路径 (强制): 管理模板/Microsoft Edge/本机消息
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\2 = "com.native.messaging.host.name2"

```


  #### Mac 信息和设置
  - 首选项密钥名称: NativeMessagingAllowlist
  - 示例值:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### NativeMessagingBlocklist
  #### 配置本机消息传递阻止名单
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定不应使用的本机消息传递主机。

使用 "*" 阻止所有本机消息传递主机，除非允许列表中明确列出了它们。

如果未配置此策略，则 Microsoft Edge 将加载所有已安装的本机消息传递主机。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: NativeMessagingBlocklist
  - GP 名称: 配置本机消息传递阻止名单
  - GP 路径 (强制): 管理模板/Microsoft Edge/本机消息
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\2 = "com.native.messaging.host.name2"

```


  #### Mac 信息和设置
  - 首选项密钥名称: NativeMessagingBlocklist
  - 示例值:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### NativeMessagingUserLevelHosts
  #### 允许用户级本机消息传递主机(安装时不带管理员权限)
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  启用本机消息传递主机的用户级别安装。

如果禁用此策略，则 Microsoft Edge 将只使用在系统级别安装的本机消息传递主机。

默认情况下，如果未配置此策略，则 Microsoft Edge 将允许使用用户级别的本机消息传递主机。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: NativeMessagingUserLevelHosts
  - GP 名称: 允许用户级本机消息传递主机(安装时不带管理员权限)
  - GP 路径 (强制): 管理模板/Microsoft Edge/本机消息
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: NativeMessagingUserLevelHosts
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: NativeMessagingUserLevelHosts
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ## 默认的搜索提供程序 policies

  [返回顶部](#microsoft-edge---策略)

  ### DefaultSearchProviderEnabled
  #### 启用默认搜索提供程序
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  启用使用默认搜索提供程序的功能。

如果启用此策略，用户可通过在地址栏中键入来搜索术语(只要键入的不是 URL)。

通过启用其余默认搜索策略，你可以指定要使用的默认搜索提供程序。如果留空(未配置)或配置不正确，用户可以选择默认提供程序。

如果禁用此策略，用户不能从地址栏中搜索。

如果启用或禁用此策略，则用户无法更改或覆盖它。

如果未配置此策略，将启用默认搜索提供程序，用户可以选择默认搜索提供程序并设置搜索提供程序列表。

此策略仅适用于加入到 Microsoft Active Directory 域的 Windows 实例，注册用于设备管理的 Windows 10 专业版或企业版实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例。

从 Microsoft Edge 84 开始，可以将此策略设置为推荐策略。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultSearchProviderEnabled
  - GP 名称: 启用默认搜索提供程序
  - GP 路径 (强制): 管理模板/Microsoft Edge/默认的搜索提供程序
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/默认的搜索提供程序
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: DefaultSearchProviderEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultSearchProviderEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultSearchProviderEncodings
  #### 默认的搜索提供程序编码
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定搜索提供程序支持的字符编码。编码是代码页名称，例如 UTF-8、GB2312 和 ISO-8859-1。将按照提供的顺序尝试它们。

此策略是可选的。如果未配置，则使用默认值 UTF-8。

此策略仅在启用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 策略时应用。

从 Microsoft Edge 84 开始，可以将此策略设置为推荐策略。如果用户已设置了默认搜索提供程序，则此建议策略配置的默认搜索提供程序将不会添加到用户可从中选择的搜索提供程序列表中。如果这是所需的行为，请使用 [ManagedSearchEngines](#managedsearchengines) 策略。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultSearchProviderEncodings
  - GP 名称: 默认的搜索提供程序编码
  - GP 路径 (强制): 管理模板/Microsoft Edge/默认的搜索提供程序
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/默认的搜索提供程序
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐\DefaultSearchProviderEncodings
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\1 = "UTF-8"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\2 = "UTF-16"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\3 = "GB2312"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\4 = "ISO-8859-1"

```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultSearchProviderEncodings
  - 示例值:
``` xml
<array>
  <string>UTF-8</string>
  <string>UTF-16</string>
  <string>GB2312</string>
  <string>ISO-8859-1</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultSearchProviderImageURL
  #### 为默认搜索提供程序指定“按图像搜索”功能
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定用于图像搜索的搜索引擎 URL。使用 GET 方法发送搜索请求。

此策略是可选的。如果未配置此策略，则图像搜索不可用。

必应的图像搜索 URL 可以指定为:
“{bing:baseURL}images/detail/search?iss=sbiupload&FORM=ANCMS1#enterInsights”。

Google 的图像搜索 URL 可以指定为:“{google:baseURL}searchbyimage/upload”。

请参阅 [DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams) 策略，以完成图像搜索配置。

此策略仅在启用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 策略时应用。

从 Microsoft Edge 84 开始，可以将此策略设置为推荐策略。如果用户已设置了默认搜索提供程序，则此建议策略配置的默认搜索提供程序将不会添加到用户可从中选择的搜索提供程序列表中。如果这是所需的行为，请使用 [ManagedSearchEngines](#managedsearchengines) 策略。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultSearchProviderImageURL
  - GP 名称: 为默认搜索提供程序指定“按图像搜索”功能
  - GP 路径 (强制): 管理模板/Microsoft Edge/默认的搜索提供程序
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/默认的搜索提供程序
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: DefaultSearchProviderImageURL
  - 值类型: REG_SZ
  ##### 示例值:
```
"https://search.contoso.com/searchbyimage/upload"
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultSearchProviderImageURL
  - 示例值:
``` xml
<string>https://search.contoso.com/searchbyimage/upload</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultSearchProviderImageURLPostParams
  #### 使用 POST 的图像 URL 的参数
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  如果启用此策略，它将指定在执行使用 POST 的图像搜索时使用的参数。该策略包含以逗号分隔的名称/值对。如果值为模板参数(例如前面示例中的 {imageThumbnail})，它将替换为实际图像缩略图数据。此策略仅在启用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 策略时应用。

必应的图像搜索 URL 发布参数可以指定为:
“imageBin={google:imageThumbnailBase64}”。

Google 的图像搜索 URL Post 参数可以指定为:
“encoded_image={google:imageThumbnail},image_url={google:imageURL},sbisrc={google:imageSearchSource},original_width={google:imageOriginalWidth},original_height={google:imageOriginalHeight}”

如果未设置此策略，则会使用 GET 方法发送图像搜索请求。

从 Microsoft Edge 84 开始，可以将此策略设置为推荐策略。如果用户已设置了默认搜索提供程序，则此建议策略配置的默认搜索提供程序将不会添加到用户可从中选择的搜索提供程序列表中。如果这是所需的行为，请使用 [ManagedSearchEngines](#managedsearchengines) 策略。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultSearchProviderImageURLPostParams
  - GP 名称: 使用 POST 的图像 URL 的参数
  - GP 路径 (强制): 管理模板/Microsoft Edge/默认的搜索提供程序
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/默认的搜索提供程序
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: DefaultSearchProviderImageURLPostParams
  - 值类型: REG_SZ
  ##### 示例值:
```
"content={imageThumbnail},url={imageURL},sbisrc={SearchSource}"
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultSearchProviderImageURLPostParams
  - 示例值:
``` xml
<string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultSearchProviderKeyword
  #### 默认的搜索提供程序关键字
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定关键字，它是在地址栏中用于触发搜索此提供程序的快捷方式。

此策略是可选的。如果未配置此策略，则不会有关键字激活搜索提供程序。

仅当启用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 策略时，才应用此策略。

从 Microsoft Edge 84 开始，你可以将此策略设置为建议的策略。如果用户已设置默认搜索提供程序，则此建议策略配置的默认搜索提供程序将不会添加到用户可以从中选择的搜索提供程序列表中。如果这是所需的行为，请使用 [ManagedSearchEngines](#managedsearchengines) 策略。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultSearchProviderKeyword
  - GP 名称: 默认的搜索提供程序关键字
  - GP 路径 (强制): 管理模板/Microsoft Edge/默认的搜索提供程序
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/默认的搜索提供程序
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: DefaultSearchProviderKeyword
  - 值类型: REG_SZ
  ##### 示例值:
```
"mis"
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultSearchProviderKeyword
  - 示例值:
``` xml
<string>mis</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultSearchProviderName
  #### 默认的搜索提供程序名称
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定默认搜索提供程序的名称。

如果启用此策略，请设置默认搜索提供程序的名称。

如果未启用此策略或将其留空，则将使用由搜索 URL 指定的主机名称。

“DefaultSearchProviderName”应设置为组织批准的已加密搜索提供程序，并与在 DTBC-0008 中设置的已加密搜索提供程序相对应。此策略仅在启用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 策略时应用。

从 Microsoft Edge 84 开始，可以将此策略设置为推荐策略。如果用户已设置了默认搜索提供程序，则此建议策略配置的默认搜索提供程序将不会添加到用户可从中选择的搜索提供程序列表中。如果这是所需的行为，请使用 [ManagedSearchEngines](#managedsearchengines) 策略。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultSearchProviderName
  - GP 名称: 默认的搜索提供程序名称
  - GP 路径 (强制): 管理模板/Microsoft Edge/默认的搜索提供程序
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/默认的搜索提供程序
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: DefaultSearchProviderName
  - 值类型: REG_SZ
  ##### 示例值:
```
"My Intranet Search"
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultSearchProviderName
  - 示例值:
``` xml
<string>My Intranet Search</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultSearchProviderSearchURL
  #### 默认的搜索提供程序搜索 URL
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定用于默认搜索的搜索引擎 URL。该 URL 包含字符串“{searchTerms}”，该字符串将在查询时替换为用户搜索的术语。

必应的搜索 URL 可以指定为:

“{bing:baseURL}search?q={searchTerms}”。

Google 的搜索 URL 可以指定为:“{google:baseURL}search?q={searchTerms}&{google:RLZ}{google:originalQueryForSuggestion}{google:assistedQueryStats}{google:searchFieldtrialParameter}{google:searchClient}{google:sourceId}ie={inputEncoding}”。

此策略在启用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 策略时是必需的；如果未启用后者策略，则此策略将被忽略。

从 Microsoft Edge 84 开始，可以将此策略设置为推荐策略。如果用户已设置了默认搜索提供程序，则此建议策略配置的默认搜索提供程序将不会添加到用户可从中选择的搜索提供程序列表中。如果这是所需的行为，请使用 [ManagedSearchEngines](#managedsearchengines) 策略。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultSearchProviderSearchURL
  - GP 名称: 默认的搜索提供程序搜索 URL
  - GP 路径 (强制): 管理模板/Microsoft Edge/默认的搜索提供程序
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/默认的搜索提供程序
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: DefaultSearchProviderSearchURL
  - 值类型: REG_SZ
  ##### 示例值:
```
"https://search.contoso.com/search?q={searchTerms}"
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultSearchProviderSearchURL
  - 示例值:
``` xml
<string>https://search.contoso.com/search?q={searchTerms}</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultSearchProviderSuggestURL
  #### 建议的默认搜索提供程序 URL
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定用于提供搜索建议的搜索引擎 URL。该 URL 包含字符串“{searchTerms}”，该字符串在查询时被用户实时输入的文本所替换。

此策略是可选的。如果未配置此策略，用户将看不到搜索建议，而将看到来自浏览历史记录和收藏夹的建议。

必应的建议 URL 可以指定为:

“{bing:baseURL}qbox?query={searchTerms}”。

Google 的建议 URL 可以指定为:“{google:baseURL}complete/search?output=chrome&q={searchTerms}”。

此策略仅在启用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 策略时应用。

从 Microsoft Edge 84 开始，可以将此策略设置为推荐策略。如果用户已设置了默认搜索提供程序，则此建议策略配置的默认搜索提供程序将不会添加到用户可从中选择的搜索提供程序列表中。如果这是所需的行为，请使用 [ManagedSearchEngines](#managedsearchengines) 策略。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultSearchProviderSuggestURL
  - GP 名称: 建议的默认搜索提供程序 URL
  - GP 路径 (强制): 管理模板/Microsoft Edge/默认的搜索提供程序
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/默认的搜索提供程序
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: DefaultSearchProviderSuggestURL
  - 值类型: REG_SZ
  ##### 示例值:
```
"https://search.contoso.com/suggest?q={searchTerms}"
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultSearchProviderSuggestURL
  - 示例值:
``` xml
<string>https://search.contoso.com/suggest?q={searchTerms}</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### NewTabPageSearchBox
  #### 配置新的选项卡页搜索框体验
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 85

  #### 描述
  你可以配置新选项卡页搜索框，以使用“搜索框(推荐)”或“地址栏”在新选项卡上搜索。只有当你通过设置以下两个策略将搜索引擎设置为除必应以外的值时，此策略才起作用: [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)。

 如果禁用或未配置此策略，并且:

- 如果地址栏默认搜索引擎为必应，则新选项卡页将使用搜索框在新选项卡上搜索。
- 如果地址栏默认搜索引擎不是必应，则在新选项卡上搜索时，用户还可以获得一个附加选项(使用“地址栏”)。


如果启用此策略并将其设置为:

-“搜索框(推荐)”(“bing”)，则新选项卡页将使用搜索框在新选项卡上搜索。
-“地址栏”(“redirect”)，新选项卡页搜索框使用地址栏在新选项卡上搜索。

策略选项映射：

* bing (bing) = 搜索框(推荐)

* redirect (redirect) = 地址栏

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: NewTabPageSearchBox
  - GP 名称: 配置新的选项卡页搜索框体验
  - GP 路径 (强制): 管理模板/Microsoft Edge/默认的搜索提供程序
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/默认的搜索提供程序
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: NewTabPageSearchBox
  - 值类型: REG_SZ
  ##### 示例值:
```
"bing"
```


  #### Mac 信息和设置
  - 首选项密钥名称: NewTabPageSearchBox
  - 示例值:
``` xml
<string>bing</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ## Additional policies

  [返回顶部](#microsoft-edge---策略)

  ### AddressBarMicrosoftSearchInBingProviderEnabled
  #### 在地址栏中启用必应中的 Microsoft 搜索建议
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 81

  #### 描述
  启用以下功能: 当用户在地址栏中键入搜索字符串时，在地址栏建议列表中显示相关的必应中的 Microsoft 搜索建议。如果启用或未配置此策略，则用户可以在 Microsoft Edge 地址栏建议列表中查看由必应中的 Microsoft 搜索支持的内部结果。要查看必应中的 Microsoft 搜索结果，用户必须通过组织的 Azure AD 帐户登录到 Microsoft Edge。
如果禁用此策略，则用户无法在 Microsoft Edge 地址栏建议列表中查看内部结果。
如果已启用强制使用默认搜索提供程序的策略集([DefaultSearchProviderEnabled](#defaultsearchproviderenabled)、[DefaultSearchProviderName](#defaultsearchprovidername) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl))，并且指定的搜索提供程序不是必应，则此策略不适用，且地址栏的建议列表中不会显示必应中的 Microsoft 搜索建议。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AddressBarMicrosoftSearchInBingProviderEnabled
  - GP 名称: 在地址栏中启用必应中的 Microsoft 搜索建议
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AddressBarMicrosoftSearchInBingProviderEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: AddressBarMicrosoftSearchInBingProviderEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AdsSettingForIntrusiveAdsSites
  #### 具有干扰性广告的站点的广告设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 78

  #### 描述
  控制是否在具有入侵广告的网站上阻止广告。

策略选项映射：

* AllowAds (1) = 在所有站点上允许广告

* BlockAds (2) = 在具有干扰性广告的站点上阻止广告。（默认值）

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AdsSettingForIntrusiveAdsSites
  - GP 名称: 具有干扰性广告的站点的广告设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AdsSettingForIntrusiveAdsSites
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: AdsSettingForIntrusiveAdsSites
  - 示例值:
``` xml
<integer>1</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AllowDeletingBrowserHistory
  #### 启用删除浏览器和下载历史记录
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  启用浏览器历史记录和下载历史记录删除，并防止用户更改此设置。

请注意，即使禁用此策略，也不能保证会保留浏览和下载历史记录: 用户可以直接编辑或删除历史记录数据库文件，浏览器本身可能会(根据过期期限)随时删除或存档任何或所有历史记录项目。

如果启用或未配置此策略，则用户可以删除浏览和下载历史记录。

如果禁用此策略，则用户无法删除浏览和下载历史记录。

如果启用此策略，则不要启用 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 策略，因为它们都会执行数据删除。如果二者都启用，则 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 策略优先并且会在 Microsoft Edge 关闭时删除所有数据，无论你如何配置此策略都是如此。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AllowDeletingBrowserHistory
  - GP 名称: 启用删除浏览器和下载历史记录
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AllowDeletingBrowserHistory
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: AllowDeletingBrowserHistory
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AllowFileSelectionDialogs
  #### 允许文件选择对话框
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许 Microsoft Edge 显示文件选择对话框，从而允许访问本地文件。

如果启用或未配置此策略，则用户可以正常打开文件选择对话框。

如果禁用此策略，那么每当用户执行触发文件选择对话框的操作(如导入收藏夹、上传文件或保存链接)时，就会显示一条消息，并且会假定用户在文件选择对话框中单击了“取消”。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AllowFileSelectionDialogs
  - GP 名称: 允许文件选择对话框
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AllowFileSelectionDialogs
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: AllowFileSelectionDialogs
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AllowPopupsDuringPageUnload
  #### 允许页面在卸载期间显示弹出窗口
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 78

  #### 描述
  通过此策略，管理员可以指定页面在卸载时是否可以显示弹出窗口。

如果将策略设置为“启用”，则将允许页面在卸载时显示弹出窗口。

如果将策略设置为“禁用”或未设置，则将不允许页面在卸载时显示弹出窗口。此策略基于规范: (https://html.spec.whatwg.org/#apis-for-creating-and-navigating-browsing-contexts-by-name)。

此策略将在未来删除。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AllowPopupsDuringPageUnload
  - GP 名称: 允许页面在卸载期间显示弹出窗口
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AllowPopupsDuringPageUnload
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: AllowPopupsDuringPageUnload
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AllowSurfGame
  #### 允许冲浪游戏
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 83

  #### 描述
  如果禁用此策略，则当设备处于离线状态或者用户导航到 edge://surf 时，用户将无法玩冲浪游戏。

如果启用或未配置此策略，用户可以玩冲浪游戏。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AllowSurfGame
  - GP 名称: 允许冲浪游戏
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AllowSurfGame
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: AllowSurfGame
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AllowSyncXHRInPageDismissal
  #### 允许页面在关闭过程中发送同步 XHR 请求 (已弃用)
  >已弃用: 此策略已弃用。目前仍受支持，但将在未来版本中弃用。
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 79

  #### 描述
  此策略已弃用，因为它旨在仅作为一种短期机制，让企业在发现它与不允许在页面关闭过程中同步 XHR 请求的更改不兼容时，有更多时间更新其 Web 内容。它将无法在 Microsoft Edge 版本 88 中正常使用。

此策略让你可以指定页面是否可以在页面关闭过程中发送同步 XHR 请求。

如果启用此策略，则页面可以在页面关闭过程中发送同步 XHR 请求。

如果禁用此策略或未配置此策略，则不允许页面在页面关闭过程中发送同步 XHR 请求。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AllowSyncXHRInPageDismissal
  - GP 名称: 允许页面在关闭过程中发送同步 XHR 请求 (已弃用)
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AllowSyncXHRInPageDismissal
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: AllowSyncXHRInPageDismissal
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AllowTokenBindingForUrls
  #### 配置 Microsoft Edge 将尝试为其建立令牌绑定的网站列表。
  
  
  #### 支持的版本:
  - 在 Windows 自 83 或之后

  #### 描述
  配置浏览器将尝试通过其执行令牌绑定协议的网站的 URL 模式列表。
对于此列表中的域，浏览器将在 TLS 握手中发送令牌绑定 ClientHello (请参阅 https://tools.ietf.org/html/rfc8472)。
如果服务器通过有效的 ServerHello 响应进行响应，则浏览器将在后续的 https 请求中创建并发送令牌绑定消息。有关详细信息，请参阅 https://tools.ietf.org/html/rfc8471。

如果此列表为空，则将禁用令牌绑定。

此策略仅在具有虚拟安全模式功能的 Windows 10 设备上可用。

从 Microsoft Edge 86 开始，此策略不再支持动态刷新。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AllowTokenBindingForUrls
  - GP 名称: 配置 Microsoft Edge 将尝试为其建立令牌绑定的网站列表。
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\2 = "[*.]mydomain2.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\3 = "[*.].mydomain2.com"

```


  

  [返回顶部](#microsoft-edge---策略)

  ### AllowTrackingForUrls
  #### 为特定站点配置跟踪保护例外
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 78

  #### 描述
  配置从跟踪保护中排除的 URL 模式的列表。

如果配置此策略，则会从跟踪保护中排除配置的 URL 模式列表。

如果未配置此策略，则将对所有站点使用“阻止跟踪用户的 Web 浏览活动”策略中的全局默认值(如果已设置)或用户个人配置。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AllowTrackingForUrls
  - GP 名称: 为特定站点配置跟踪保护例外
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: AllowTrackingForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AlternateErrorPagesEnabled
  #### 找不到网页时建议类似的页面
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 80

  #### 描述
  允许 Microsoft Edge 发出 Web 服务连接以针对 DNS 错误等连接问题生成 URL 和搜索建议。

如果启用此策略，则 Web 服务用于针对网络错误生成 URL 和搜索建议。

如果禁用此策略，则不会调用 Web 服务，并显示标准错误页面。

如果未配置此策略，则 Microsoft Edge 会遵守在 edge://settings/privacy 的“服务”下设置的用户首选项。
具体来说，存在用户可以打开或关闭的**找不到网页时建议类似的页面**切换开关。请注意，如果启用了此策略(AlternateErrorPagesEnabled)，则会打开“找不到网页时建议类似的页面”设置，但是用户无法使用切换开关来更改此设置。如果禁用此策略，则会关闭“找不到网页时建议类似的页面”设置，并且用户无法使用切换开关来更改此设置。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AlternateErrorPagesEnabled
  - GP 名称: 找不到网页时建议类似的页面
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: AlternateErrorPagesEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: AlternateErrorPagesEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AlwaysOpenPdfExternally
  #### 始终在外部打开 PDF 文件
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  在 Microsoft Edge 中禁用内部 PDF 查看器。

如果启用此策略，Microsoft Edge 会将 PDF 文件视为下载内容，并允许用户使用默认应用程序打开它们。

如果未配置此策略或禁用此策略，则 Microsoft Edge 将打开 PDF 文件(除非用户禁用此文件)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AlwaysOpenPdfExternally
  - GP 名称: 始终在外部打开 PDF 文件
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AlwaysOpenPdfExternally
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: AlwaysOpenPdfExternally
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AmbientAuthenticationInPrivateModesEnabled
  #### 针对 InPrivate 和来宾用户配置启用环境身份验证
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 81

  #### 描述
  配置此策略以允许/禁止在 Microsoft Edge 中针对 InPrivate 和来宾用户配置进行环境身份验证。

环境身份验证是未通过 NTLM/Kerberos/协商质询/响应方案提供显式凭据时使用默认凭据进行的 http 身份验证。

如果将策略设置为“RegularOnly”，则仅允许定期会话进行环境身份验证。将不允许 InPrivate 和来宾会话进行环境身份验证。

如果将策略设置为“InPrivateAndRegular”，则允许 InPrivate 和定期会话进行环境身份验证。将不允许来宾会话进行环境身份验证。

如果将策略设置为“GuestAndRegular”，则允许来宾和定期会话进行环境身份验证。将不允许 InPrivate 会话进行环境身份验证

如果将策略设置为“All”，则将允许所有会话进行环境身份验证。

请注意，始终允许对定期用户配置进行环境身份验证。

在 Microsoft Edge 版本 81 及更高版本中，如果策略保留为未设置，则仅在定期会话中启用环境身份验证。

策略选项映射：

* RegularOnly (0) = 仅在定期会话中启用环境身份验证

* InPrivateAndRegular (1) = 在 InPrivate 和定期会话中启用环境身份验证

* GuestAndRegular (2) = 在来宾和定期会话中启用环境身份验证

* All (3) = 在定期 InPrivate 和来宾会话中启用环境身份验证

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AmbientAuthenticationInPrivateModesEnabled
  - GP 名称: 针对 InPrivate 和来宾用户配置启用环境身份验证
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AmbientAuthenticationInPrivateModesEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: AmbientAuthenticationInPrivateModesEnabled
  - 示例值:
``` xml
<integer>0</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AppCacheForceEnabled
  #### 允许重新启用 AppCache 功能，即使它默认处于关闭状态
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 84

  #### 描述
  如果将此策略设置为 true，AppCache 将启用，即使 Microsoft Edge 中的 AppCache 默认情况下不可用。

如果将此策略设置为 false 或未设置，AppCache 将遵循 Microsoft Edge 的默认设置。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AppCacheForceEnabled
  - GP 名称: 允许重新启用 AppCache 功能，即使它默认处于关闭状态
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AppCacheForceEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: AppCacheForceEnabled
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ApplicationLocaleValue
  #### 设置应用程序的区域设置
  
  
  #### 支持的版本:
  - 在 Windows 自 77 或之后

  #### 描述
  在 Microsoft Edge 中配置应用程序区域设置，并阻止用户更改区域设置。

如果启用此策略，则 Microsoft Edge 使用指定的区域设置。如果不支持配置的区域设置，则改用 "en-US"。

如果禁用或未配置此设置，则 Microsoft Edge 使用用户指定的首选区域设置(如果已配置)或回退区域设置 "en-US"。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ApplicationLocaleValue
  - GP 名称: 设置应用程序的区域设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: ApplicationLocaleValue
  - 值类型: REG_SZ
  ##### 示例值:
```
"en"
```


  

  [返回顶部](#microsoft-edge---策略)

  ### AudioCaptureAllowed
  #### 允许或阻止音频捕获
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许你设置是否提示用户为网站授予其音频捕获设备的访问权限。此策略适用于除 [AudioCaptureAllowedUrls](#audiocaptureallowedurls) 列表中配置的 URL 以外的所有 URL。

如果启用或未配置此策略(默认设置)，则会提示用户提供音频捕获访问权限，但这不适用于 [AudioCaptureAllowedUrls](#audiocaptureallowedurls) 列表中的 URL。这些列出的 URL 已被授予访问权限，但未给出任何提示。

如果禁用此策略，则不会提示用户，并且只有 [AudioCaptureAllowedUrls](#audiocaptureallowedurls) 中配置的 URL 才能访问音频捕获。

此策略会影响所有类型的音频输入，而不仅仅是内置麦克风。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AudioCaptureAllowed
  - GP 名称: 允许或阻止音频捕获
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AudioCaptureAllowed
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: AudioCaptureAllowed
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AudioCaptureAllowedUrls
  #### 无需请求许可即可访问音频捕获设备的站点
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  根据 URL 模式指定无需用户许可即可使用音频捕获设备的网站。该列表中的模式将与请求 URL 的安全来源进行匹配。如果匹配，站点将自动获得音频捕获设备的访问权限。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AudioCaptureAllowedUrls
  - GP 名称: 无需请求许可即可访问音频捕获设备的站点
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Mac 信息和设置
  - 首选项密钥名称: AudioCaptureAllowedUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AudioSandboxEnabled
  #### 允许音频沙盒运行
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 81

  #### 描述
  此策略控制音频进程沙盒。

如果启用此策略，则音频进程将在沙盒化环境中运行。

如果禁用此策略，则音频进程将在非沙盒化环境中运行，WebRTC 音频处理模块将在呈现器进程中运行。
这会使用户面临与在非沙盒化环境中运行音频子系统相关的安全风险。

如果未配置此策略，则将使用音频沙盒的默认配置，这可能会因平台而异。

此策略旨在使企业能够灵活地禁用音频沙盒(如果他们使用干扰沙盒的安全软件设置)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AudioSandboxEnabled
  - GP 名称: 允许音频沙盒运行
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AudioSandboxEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: AudioSandboxEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AutoImportAtFirstRun
  #### 首次运行时自动导入其他浏览器的数据和设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  如果启用此策略，则在首次运行时会无提示地自动导入指定浏览器中的所有受支持的数据类型和设置。在首次运行体验期间，将跳过导入部分。

无论此策略的值如何，来自旧版 Microsoft Edge 的浏览器数据始终会在首次运行时无提示地进行迁移。

如果此策略设置为“FromDefaultBrowser”，则将导入与托管设备上的默认浏览器相对应的数据类型。

如果指定为此策略值的浏览器在托管设备中不存在，则 Microsoft Edge 只是跳过导入，而不向用户发送任何通知。

如果将此策略设置为“DisabledAutoImport”，则会完全跳过首次运行体验的导入部分，并且 Microsoft Edge 不会自动导入浏览器数据和设置。

如果此策略设置为值“FromInternetExplorer”，则会从 Internet Explorer 导入以下数据类型:
1. 收藏夹或书签
2. 保存的密码
3. 搜索引擎
4. 浏览历史记录
5. 主页

如果此策略设置为值“FromGoogleChrome”，则会从 Google Chrome 导入以下数据类型:
1. 收藏夹
2. 保存的密码
3. 地址及更多
4. 付款信息
5. 浏览历史记录
6. 设置
7. 固定和打开的选项卡
8. 扩展
9. Cookie

注意: 要更详细地了解从 Google Chrome 导入的内容，请参阅 [https://go.microsoft.com/fwlink/?linkid=2120835](https://go.microsoft.com/fwlink/?linkid=2120835)

如果此策略设置为值 Safari (3)，则用户数据不再导入到 Microsoft Edge 中。这是由于 Mac 上“完全磁盘访问”的工作方式所致。
在 macOS Mojave 及更高版本上，不再可能自动和无人值守地将 Safari 数据导入 Microsoft Edge。

从 Microsoft Edge 版本 83 开始，如果此策略设置为值 Mozilla Firefox (5)，则会从 Mozilla Firefox 导入以下数据类型:
1. 收藏夹或书签
2. 保存的密码
3. 地址及更多
4. 浏览历史记录

如果要限制托管设备上特定数据类型的导入，则可以将此策略与其他策略(如 [ImportAutofillFormData](#importautofillformdata)、[ImportBrowserSettings](#importbrowsersettings)、[ImportFavorites](#importfavorites) 等)结合使用。

策略选项映射：

* FromDefaultBrowser (0) = 自动从默认浏览器导入所有受支持的数据类型和设置

* FromInternetExplorer (1) = 自动从 Internet Explorer 导入所有受支持的数据类型和设置

* FromGoogleChrome (2) = 自动从 Google Chrome 中导入所有受支持的数据类型和设置

* FromSafari (3) = 自动从 Safari 中导入所有受支持的数据类型和设置

* DisabledAutoImport (4) = 禁用自动导入，跳过首次运行体验的导入部分

* FromMozillaFirefox (5) = 自动从 Mozilla Firefox 中导入所有受支持的数据类型和设置

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AutoImportAtFirstRun
  - GP 名称: 首次运行时自动导入其他浏览器的数据和设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AutoImportAtFirstRun
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: AutoImportAtFirstRun
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AutoLaunchProtocolsFromOrigins
  #### 定义可以在不提示用户的情况下从列出的源启动外部应用程序的协议列表
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 85

  #### 描述
  允许设置协议列表并为每个协议设置一个关联的允许源模式列表，该列表可以在不提示用户的情况下启动外部应用程序。在列出协议时不应包含尾部分隔符。例如，请列出 "skype"，而不是 "skype:" 或 "skype://"。

如果配置了此策略，则只有在以下条件下，才允许协议在不通过策略提示的情况下启动外部应用程序:

- 该协议已列出

- 尝试启动协议的网站源与该协议的 allowed_origins 列表中的一个源模式相匹配。

如果其中任一条件为 false，策略都不会省略外部协议启动提示。

如果未配置此策略，则在没有提示的情况下不能启动任何协议。除非将 [ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox) 策略设置为“已禁用”，否则用户可以根据协议/站点选择不显示提示。此策略对用户设置的每协议/每站点的提示豁免没有影响。

源匹配模式使用与 [URLBlocklist](#urlblocklist) 策略类似的格式，相关介绍，请访问 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

但是，此策略的源匹配模式不能包含 "/path" 或 "@query" 元素。任何包含 "/path" 或 "@query" 元素的模式都将被忽略。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字典

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AutoLaunchProtocolsFromOrigins
  - GP 名称: 定义可以在不提示用户的情况下从列出的源启动外部应用程序的协议列表
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AutoLaunchProtocolsFromOrigins
  - 值类型: REG_SZ
  ##### 示例值:
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


  #### Mac 信息和设置
  - 首选项密钥名称: AutoLaunchProtocolsFromOrigins
  - 示例值:
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
  

  [返回顶部](#microsoft-edge---策略)

  ### AutoOpenAllowedForURLs
  #### AutoOpenFileTypes 可应用的 URL
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 85

  #### 描述
  [AutoOpenFileTypes](#autoopenfiletypes) 将应用于的 URL 列表。此策略不会影响用户通过下载架设置的自动打开值...> “始终打开这种类型的文件”菜单条目。

如果在此策略中设置 URL，则只有当 URL 是此设置的一部分并且文件类型在 [AutoOpenFileTypes](#autoopenfiletypes) 中列出时，文件才会按策略自动打开。如果任一条件为 false，则下载不会按策略自动打开。

如果未设置此策略，文件类型为 [AutoOpenFileTypes](#autoopenfiletypes) 的所有下载将自动打开。

必须根据 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) 设置 URL 模式的格式。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AutoOpenAllowedForURLs
  - GP 名称: AutoOpenFileTypes 可应用的 URL
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\1 = "example.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\5 = ".exact.hostname.com"

```


  #### Mac 信息和设置
  - 首选项密钥名称: AutoOpenAllowedForURLs
  - 示例值:
``` xml
<array>
  <string>example.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AutoOpenFileTypes
  #### 应在下载时自动打开的文件类型列表
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 85

  #### 描述
  此策略设置应在下载时自动打开的文件类型列表。注意: 列出文件类型时不应包含前导分隔符，因此应列出“txt”而不是“.txt”。

默认情况下，这些文件类型将在所有 URL 上自动打开。你可以使用 [AutoOpenAllowedForURLs](#autoopenallowedforurls) 策略来限制将对其自动打开这些文件类型的 URL。

具有应自动打开的类型的文件仍将受启用的 Microsoft Defender SmartScreen 检查约束，如果未通过检查，则这些文件不会打开。

用户已指定为自动打开的类型在下载时将继续打开。用户将继续能够指定要自动打开的其他文件类型。

如果未设置此策略，则只有用户已指定为自动打开的文件类型将在下载时自动打开。

为使此策略应用于 Windows 设备，设备必须加入 Microsoft Active Directory 域，注册了设备管理的 Windows 10 专业版或企业版实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AutoOpenFileTypes
  - GP 名称: 应在下载时自动打开的文件类型列表
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\1 = "exe"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\2 = "txt"

```


  #### Mac 信息和设置
  - 首选项密钥名称: AutoOpenFileTypes
  - 示例值:
``` xml
<array>
  <string>exe</string>
  <string>txt</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AutofillAddressEnabled
  #### 启用地址自动填充
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  启用自动填充功能，并允许用户使用以前存储的信息在 Web 窗体中自动完成地址信息。

如果禁用此策略，自动填充不会建议或填充地址信息，也不会保存用户在浏览 Web 时可能提交的其他地址信息。

如果启用或未配置此策略，则用户可以在用户界面中控制地址自动填充。

请注意，如果禁用此策略，则还会停止除付款和密码窗体之外的所有其他 Web 窗体的所有活动。不再保存任何条目，Microsoft Edge 不会建议或自动填充任何以前的条目。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AutofillAddressEnabled
  - GP 名称: 启用地址自动填充
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: AutofillAddressEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: AutofillAddressEnabled
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AutofillCreditCardEnabled
  #### 启用信用卡的自动填充功能
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  启用 Microsoft Edge 的自动填充功能，并允许用户使用以前存储的信息在 Web 窗体中自动填写信用卡信息。

如果禁用此策略，则自动填充绝对不会建议或填充信用卡信息，也不会保存用户在浏览 Web 时可能提交的其他信用卡信息。

如果启用或未配置此策略，则用户可以控制信用卡信息的自动填充。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AutofillCreditCardEnabled
  - GP 名称: 启用信用卡的自动填充功能
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: AutofillCreditCardEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: AutofillCreditCardEnabled
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### AutoplayAllowed
  #### 允许网站自动播放媒体
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 78

  #### 描述
  此策略为网站设置媒体自动播放策略。

默认设置“未配置”遵循当前媒体自动播放设置，并允许用户配置其自动播放设置。

如果设置为“已启用”，则会将媒体自动播放设置为“允许”。允许所有网站自动播放媒体。用户无法覆盖此策略。

如果设置为“已禁用”，则会将媒体自动播放设置为“阻止”。不允许任何网站自动播放媒体。用户无法覆盖此策略。

需要关闭并重新打开标签页才能使此策略生效。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: AutoplayAllowed
  - GP 名称: 允许网站自动播放媒体
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: AutoplayAllowed
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: AutoplayAllowed
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### BackgroundModeEnabled
  #### Microsoft Edge 关闭后，继续运行后台应用
  
  
  #### 支持的版本:
  - 在 Windows 自 77 或之后

  #### 描述
  允许 Microsoft Edge 进程在操作系统登录时启动，并在最后一个浏览器窗口关闭后继续运行。在此场景中，后台应用和当前浏览会话保持活动状态，包括任何会话 cookie。打开的后台进程会在系统托盘中显示一个图标，并且始终可以从系统托盘中将其关闭。

如果启用此策略，则将开启后台模式。

如果禁用此策略，则将关闭后台模式。

如果未配置此策略，则将先关闭后台模式，并且用户可以在 edge://settings/system 中配置其行为。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: BackgroundModeEnabled
  - GP 名称: Microsoft Edge 关闭后，继续运行后台应用
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: BackgroundModeEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  

  [返回顶部](#microsoft-edge---策略)

  ### BackgroundTemplateListUpdatesEnabled
  #### 对集锦和其他使用模板的功能的可用模板列表启用后台更新
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 79

  #### 描述
  允许你对集锦和其他使用模板的功能的可用模板列表启用或禁用后台更新。模板用于在将页面保存到集锦时从网页中提取丰富的元数据。

如果启用此设置或未配置此设置，则将在后台每隔 24 小时从 Microsoft 服务下载可用模板的列表。

如果禁用此设置，则将按需下载可用模板的列表。此类型的下载可能会导致集锦和其他功能的性能受到细微影响。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: BackgroundTemplateListUpdatesEnabled
  - GP 名称: 对集锦和其他使用模板的功能的可用模板列表启用后台更新
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: BackgroundTemplateListUpdatesEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: BackgroundTemplateListUpdatesEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### BingAdsSuppression
  #### 阻止必应搜索结果中的所有广告
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 83

  #### 描述
  在 Bing.com 上实现无广告搜索体验

如果启用此策略，则用户可以在 bing.com 上搜索并获得无广告搜索体验。同时，安全搜索设置将设置为“严格”，并且用户无法进行更改。

 如果未配置此策略，则默认体验将在 bing.com 上的搜索结果中显示广告。安全搜索将设置为“中等”，并且用户可以进行更改。

 此策略仅适用于被 Microsoft 标识为 EDU 租户的 K-12 SKU。

 请参阅 [https://go.microsoft.com/fwlink/?linkid=2119711](https://go.microsoft.com/fwlink/?linkid=2119711) 以了解有关此策略的详细信息，或者如果以下情况适用于你:

 * 你拥有 EDU 租户，但策略不起作用。

 * 你的 IP 已列入核准清单，因为它具有无广告搜索体验。

 * 你正在体验旧版 Microsoft Edge 的无广告搜索体验，并且想要升级到 Microsoft Edge 的新版本。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: BingAdsSuppression
  - GP 名称: 阻止必应搜索结果中的所有广告
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: BingAdsSuppression
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: BingAdsSuppression
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### BlockThirdPartyCookies
  #### 阻止第三方 Cookie
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  阻止不是来自地址栏中的域的网页元素设置 Cookie。

如果启用此策略，则不是来自地址栏中的域的网页元素无法设置 Cookie。

如果禁用此策略，则来自地址栏以外的域的网页元素可以设置 Cookie。

如果未配置此策略，则启用第三方 Cookie，但用户可以更改此设置。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: BlockThirdPartyCookies
  - GP 名称: 阻止第三方 Cookie
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: BlockThirdPartyCookies
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: BlockThirdPartyCookies
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### BrowserAddProfileEnabled
  #### 从“标识”浮出菜单或“设置”页面启用用户配置创建
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许用户使用**添加用户配置**选项创建新用户配置。
如果启用或未配置此策略，则 Microsoft Edge 允许用户使用“标识”浮出控件菜单或“设置”页上的**添加用户配置**创建新用户配置。

如果禁用此策略，则用户无法从“标识”浮出控件菜单或“设置”页中添加新用户配置。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: BrowserAddProfileEnabled
  - GP 名称: 从“标识”浮出菜单或“设置”页面启用用户配置创建
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: BrowserAddProfileEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: BrowserAddProfileEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### BrowserGuestModeEnabled
  #### 启用来宾模式
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  启用此选项可允许在 Microsoft Edge 中使用来宾用户配置。在来宾用户配置中，浏览器不会从现有用户配置中导入浏览数据，并且在关闭所有来宾用户配置后，它会删除浏览数据。

如果启用或未配置此策略，则 Microsoft Edge 允许用户在来宾用户配置中浏览。

如果禁用此策略，则 Microsoft Edge 不允许用户在来宾用户配置中浏览。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: BrowserGuestModeEnabled
  - GP 名称: 启用来宾模式
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: BrowserGuestModeEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: BrowserGuestModeEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### BrowserNetworkTimeQueriesEnabled
  #### 允许查询浏览器网络时间服务
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  阻止 Microsoft Edge 偶尔向浏览器网络时间服务发送查询以检索准确的时间戳。

如果禁用此策略，则 Microsoft Edge 将停止向浏览器网络时间服务发送查询。

如果启用或未配置此策略，则 Microsoft Edge 会偶尔向浏览器网络时间服务发送查询。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: BrowserNetworkTimeQueriesEnabled
  - GP 名称: 允许查询浏览器网络时间服务
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: BrowserNetworkTimeQueriesEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: BrowserNetworkTimeQueriesEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### BrowserSignin
  #### 浏览器登录设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定用户是否可以使用其帐户登录 Microsoft Edge 并使用与帐户相关的服务，例如同步和单一登录。若要控制同步的可用性，请改用 [SyncDisabled](#syncdisabled) 策略。

如果将此策略设置为“Disable”，请确保将 [NonRemovableProfileEnabled](#nonremovableprofileenabled) 策略也设置为“已禁用”，因为 [NonRemovableProfileEnabled](#nonremovableprofileenabled) 会禁止创建自动登录浏览器用户配置。如果同时设置了这两个策略，则 Microsoft Edge 将使用“禁用浏览器登录”策略，其行为方式等同于将 [NonRemovableProfileEnabled](#nonremovableprofileenabled) 设置为“已禁用”。

如果将此策略设置为“Enable”，则用户可以登录浏览器。登录浏览器并不意味着默认情况下打开同步；用户必须单独选择使用此功能。

如果将此策略设置为“Force”，则用户必须登录用户配置才能使用浏览器。默认情况下，这将允许用户选择是否要同步到他们的帐户，除非由域管理员或通过 [SyncDisabled](#syncdisabled) 策略禁用了同步。[BrowserGuestModeEnabled](#browserguestmodeenabled) 策略的默认值被设置为 false。

如果未配置此策略，则用户可以确定是否要启用浏览器登录选项并在合适时使用它。

策略选项映射：

* Disable (0) = 禁用浏览器登录

* Enable (1) = 启用浏览器登录

* Force (2) = 强制用户通过登录使用浏览器

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: BrowserSignin
  - GP 名称: 浏览器登录设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: BrowserSignin
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: BrowserSignin
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### BuiltInDnsClientEnabled
  #### 使用内置 DNS 客户端
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  控制是否使用内置 DNS 客户端。

这不会对使用哪个 DNS 服务器有影响；只影响用于与它们通信的软件堆栈。例如，如果操作系统配置为使用企业 DNS 服务器，则内置 DNS 客户端将使用该服务器。但是，内置 DNS 客户端可能会使用更新型的 DNS 相关协议(例如 DNS-over-TLS)以不同方式对服务器进行寻址。

如果启用此策略，则使用内置 DNS 客户端(如果可用)。

如果禁用此策略，则从不使用客户端。

如果未配置此策略，则默认情况下在 MacOS 上启用内置 DNS 客户端，用户可通过编辑 edge://flags 或指定命令行标志，对是否使用内置 DNS 客户端进行更改。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: BuiltInDnsClientEnabled
  - GP 名称: 使用内置 DNS 客户端
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: BuiltInDnsClientEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: BuiltInDnsClientEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### BuiltinCertificateVerifierEnabled
  #### 确定是否将使用内置证书验证器验证服务器证书 (已弃用)
  >已弃用: 此策略已弃用。目前仍受支持，但将在未来版本中弃用。
  
  #### 支持的版本:
  - 在 macOS 自 83 或之后

  #### 描述
  此策略已弃用，因为它旨在仅作为一种短期机制，如果发现企业与内置证书验证程序不兼容，则可以让他们有更多时间更新环境并报告问题。

当计划删除对 Mac 操作系统 X 上的旧版证书验证程序的支持时，它将无法在 Microsoft Edge 版本 87 中正常使用。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  

  #### Mac 信息和设置
  - 首选项密钥名称: BuiltinCertificateVerifierEnabled
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### CertificateTransparencyEnforcementDisabledForCas
  #### 对 subjectPublicKeyInfo 哈希列表禁用强制证书透明度
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  对列出的 subjectPublicKeyInfo 哈希禁用强制的证书透明度要求。

此策略允许你对包含具有指定 subjectPublicKeyInfo 哈希之一的证书的证书链禁用证书透明度公开要求。这允许证书继续用于企业主机，否则这些证书因未被适当公开而不受信任。

为了在设置此策略时禁用强制证书透明度，必须满足以下条件集之一:
1. 哈希具有服务器证书的 subjectPublicKeyInfo。
2. 哈希具有出现在证书链中的 CA 证书的 subjectPublicKeyInfo，该 CA 证书通过 X.509v3 nameConstraints 扩展进行约束，permittedSubtrees 中包含一个或多个 directoryName nameConstraints，且 directoryName 包含一个 organizationName 属性。
3. 哈希具有出现在证书链中的 CA 证书的 subjectPublicKeyInfo，该 CA 证书在证书使用者中有一个或多个 organizationName 属性，并且服务器的证书包含相同数量的 organizationName 属性，顺序相同，并且具有逐字节相同的值。

指定 subjectPublicKeyInfo 哈希的方式是: 拼接哈希算法名称、"/" 字符和用于指定证书的 DER 编码 subjectPublicKeyInfo 的哈希算法的 Base64 编码。该 Base64 编码与 SPKI 指纹的格式相同，如 RFC 7469 第 2.4 节所定义。无法识别的哈希算法将被忽略。目前唯一支持的哈希算法是 "sha256"。

如果禁用或未配置此策略，则任何需要通过证书透明度公开的证书，如果没有根据证书透明度策略公开，将被视为不受信任。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: CertificateTransparencyEnforcementDisabledForCas
  - GP 名称: 对 subjectPublicKeyInfo 哈希列表禁用强制证书透明度
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\2 = "sha256//////////////////////w=="

```


  #### Mac 信息和设置
  - 首选项密钥名称: CertificateTransparencyEnforcementDisabledForCas
  - 示例值:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### CertificateTransparencyEnforcementDisabledForLegacyCas
  #### 对列出的旧证书颁发机构禁用证书透明度强制
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  针对旧证书颁发机构(Ca)列表禁用实施证书透明度要求。

此策略允许你对包含具有所指定 subjectPublicKeyInfo 哈希之一的证书的证书链禁用证书透明度公开要求。这样，你可以使用原来因未被正确公开但却继续用于企业主机而不受信任的证书。

为了禁用证书透明度实施要求，必须将哈希设置为出现在 CA 证书中并且被识别为旧证书颁发机构(CA)的 subjectPublicKeyInfo。旧 CA 是默认情况下已被 Microsoft Edge 所支持的一个或多个操作系统公开信任的 CA。

通过连接哈希算法名称、"/" 字符和对指定证书的 DER 编码 subjectPublicKeyInfo 应用的哈希算法的 Base64 编码，可以指定 subjectPublicKeyInfo 哈希。此 Base64 编码与 SPKI 指纹的格式相同，如 RFC 7469 第 2.4 节中所定义。无法识别的哈希算法会被忽略。目前唯一支持的哈希算法是 "sha256"。

如果未配置此策略，则任何需要通过证书透明度公开的证书在未根据证书透明度策略公开的情况下，都将被视为不受信任。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: CertificateTransparencyEnforcementDisabledForLegacyCas
  - GP 名称: 对列出的旧证书颁发机构禁用证书透明度强制
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\2 = "sha256//////////////////////w=="

```


  #### Mac 信息和设置
  - 首选项密钥名称: CertificateTransparencyEnforcementDisabledForLegacyCas
  - 示例值:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### CertificateTransparencyEnforcementDisabledForUrls
  #### 对特定 URL 禁用强制证书透明度
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  为列出的 URL 禁用强制执行证书透明度要求。

此策略允许你不通过证书透明度公开指定 URL 中的主机名证书。这样，你可以使用原来因未被正确公开而不受信任的证书，但这却更难检测到为那些主机误颁发的证书。

根据 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) 形成 URL 模式。由于证书对给定主机名有效，而与方案、端口或路径无关，因此仅考虑了 URL 的主机名部分。不支持使用通配符主机。

如果未配置此策略，则任何应通过证书透明度公开的证书在未公开的情况下，都会被视为不受信任。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: CertificateTransparencyEnforcementDisabledForUrls
  - GP 名称: 对特定 URL 禁用强制证书透明度
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\2 = ".contoso.com"

```


  #### Mac 信息和设置
  - 首选项密钥名称: CertificateTransparencyEnforcementDisabledForUrls
  - 示例值:
``` xml
<array>
  <string>contoso.com</string>
  <string>.contoso.com</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ClearBrowsingDataOnExit
  #### Microsoft Edge 关闭时清除浏览数据
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 78

  #### 描述
  Microsoft Edge 关闭时不会默认清除浏览数据。浏览数据包括在表单、密码甚至是所访问网站中输入的信息。

如果启用此策略，则每次 Microsoft Edge 关闭时都会删除所有浏览数据。请注意，如果启用此策略，它将优先于你配置 [DefaultCookiesSetting](#defaultcookiessetting) 的方式

如果禁用或未配置此策略，则用户可以在“设置”中配置“清除浏览数据”选项。

如果启用此策略，请不要配置 [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) 或 [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit) 策略，因为它们都会执行数据删除。如果同时配置了上述策略和此策略，则会在 Microsoft Edge 关闭时删除所有数据，无论你如何配置 [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) 或 [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)。

若要排除 cookie 以防退出时被删除，请配置 [SaveCookiesOnExit](#savecookiesonexit) 策略。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ClearBrowsingDataOnExit
  - GP 名称: Microsoft Edge 关闭时清除浏览数据
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: ClearBrowsingDataOnExit
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ClearBrowsingDataOnExit
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ClearCachedImagesAndFilesOnExit
  #### Microsoft Edge 关闭时清除缓存的图像和文件
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 83

  #### 描述
  Microsoft Edge 关闭时不会默认清除缓存的图像和文件。

如果启用此策略，则会在每次 Microsoft Edge 关闭时删除缓存的图像和文件。

如果禁用此策略，则用户无法在 edge://settings/clearBrowsingDataOnClose 中配置缓存的图像和文件选项。

如果未配置此策略，则用户可以选择是否在退出时清除缓存的图像和文件。

如果禁用此策略，则不要启用 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 策略，因为它们都涉及删除数据。如果同时配置这两者，则 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 策略将优先并在 Microsoft Edge 关闭时删除所有数据，而无论你是如何配置 [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit) 的。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ClearCachedImagesAndFilesOnExit
  - GP 名称: Microsoft Edge 关闭时清除缓存的图像和文件
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: ClearCachedImagesAndFilesOnExit
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ClearCachedImagesAndFilesOnExit
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ClickOnceEnabled
  #### 允许用户使用 ClickOnce 协议打开文件
  
  
  #### 支持的版本:
  - 在 Windows 自 78 或之后

  #### 描述
  允许用户使用 ClickOnce 协议打开文件。通过 ClickOnce 协议，网站可以请求浏览器使用用户的计算机或设备上的 ClickOnce 文件处理程序打开特定 URL 中的文件。

如果启用此策略，则用户可以使用 ClickOnce 协议打开文件。此策略将替代 edge://flags/ 页面中用户的 ClickOnce 设置。

如果禁用此策略，则用户无法使用 ClickOnce 协议打开文件。文件将通过浏览器保存到文件系统。此策略将替代 edge://flags/ 页面中用户的 ClickOnce 设置。

如果未配置此策略，则默认情况下，Microsoft Edge 版本在 Microsoft Edge 87 之前的用户无法使用 ClickOnce 协议打开文件。但是，他们可以选择允许将 ClickOnce 协议与 edge://flags/ 页面搭配使用。默认情况下，具有 Microsoft Edge 版本 87 和更高版本的用户可以使用 ClickOnce 协议打开文件，但可以选择使用 edge://flags/ 页面禁用 ClickOnce 协议。

禁用 ClickOnce 可能会阻止 ClickOnce 应用程序(.application 文件)正常启动。

有关 ClickOnce 的详细信息，请参阅 [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) 和 [https://go.microsoft.com/fwlink/?linkid=2099880](https://go.microsoft.com/fwlink/?linkid=2099880)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ClickOnceEnabled
  - GP 名称: 允许用户使用 ClickOnce 协议打开文件
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ClickOnceEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  

  [返回顶部](#microsoft-edge---策略)

  ### CollectionsServicesAndExportsBlockList
  #### 阻止访问集锦中指定的服务列表和导出目标
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  在 Microsoft Edge 的集锦功能中列出用户无法访问的特定服务和导出目标。这包括显示来自必应的其他数据以及将集锦导出到 Microsoft 产品或外部合作伙伴。

如果启用此策略，则与给定列表匹配的服务和导出目标将被阻止。

如果未配置此政策，则不对可接受的服务和导出目标实施任何限制。

策略选项映射：

* pinterest_suggestions (pinterest_suggestions) = Pinterest 建议

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: CollectionsServicesAndExportsBlockList
  - GP 名称: 阻止访问集锦中指定的服务列表和导出目标
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\1 = "pinterest_suggestions"

```


  #### Mac 信息和设置
  - 首选项密钥名称: CollectionsServicesAndExportsBlockList
  - 示例值:
``` xml
<array>
  <string>pinterest_suggestions</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### CommandLineFlagSecurityWarningsEnabled
  #### 为命令行标志启用安全警告
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 78

  #### 描述
  如果禁用，则使用具有潜在危险的命令行标志启动 Microsoft Edge 时，此策略会阻止出现安全警告。

如果启用或取消设置，则使用这些命令行标志启动 Microsoft Edge 时，会显示安全警告。

例如，--disable-gpu-sandbox 标志将生成以下警告: 你使用的是不受支持的命令行标志: --disable-gpu-sandbox。这会带来稳定性和安全风险。

此策略仅适用于已加入 Microsoft Active Directory 域的 Windows 实例、为设备管理注册的 Windows 10 专业版(或企业版)实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: CommandLineFlagSecurityWarningsEnabled
  - GP 名称: 为命令行标志启用安全警告
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: CommandLineFlagSecurityWarningsEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: CommandLineFlagSecurityWarningsEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ComponentUpdatesEnabled
  #### 在 Microsoft Edge 中启用组件更新
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  如果启用或未配置此策略，则会在 Microsoft Edge 中启用组件更新。

如果禁用此策略或将其设置为 false，则将对 Microsoft Edge 中的所有组件禁用组件更新。

但是，某些组件不受此策略控制。这包括任何不含可执行代码的组件、不会明显改变浏览器行为的组件，或对安全性至关重要的组件。即，即使禁用此策略，也仍会应用被视为“对安全至关重要”的更新。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ComponentUpdatesEnabled
  - GP 名称: 在 Microsoft Edge 中启用组件更新
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ComponentUpdatesEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ComponentUpdatesEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ConfigureDoNotTrack
  #### 配置“禁止跟踪”
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定是否向请求跟踪信息的网站发送“禁止跟踪”请求。“禁止跟踪”请求让你访问的网站知道你不希望你的浏览活动被跟踪。默认情况下，Microsoft Edge 不会发送“禁止跟踪”请求，但用户可以打开此功能来发送它们。

如果启用此策略，则将始终向请求跟踪信息的网站发送“禁止跟踪”请求。

如果禁用此策略，则从不会发送请求。

如果未配置此策略，则用户可以选择是否发送这些请求。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ConfigureDoNotTrack
  - GP 名称: 配置“禁止跟踪”
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ConfigureDoNotTrack
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: ConfigureDoNotTrack
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ConfigureOnPremisesAccountAutoSignIn
  #### 配置用 Active Directory 域帐户(如果没有 Azure AD 域帐户)进行的自动登录
  
  
  #### 支持的版本:
  - 在 Windows 自 81 或之后

  #### 描述
  如果你的用户计算机加入了域并且你的环境未进行混合联接，则启用使用 Active Directory 帐户自动登录。如果希望用户使用其 Azure Active Directory 帐户自动登录，请以 Azure AD 联接方式(请参阅 [https://go.microsoft.com/fwlink/?linkid=2118197](https://go.microsoft.com/fwlink/?linkid=2118197) 以获取更多信息)或混合联接方式(请参阅 [https://go.microsoft.com/fwlink/?linkid=2118365](https://go.microsoft.com/fwlink/?linkid=2118365) 以获取更多信息)联接环境。

如果已经将 [BrowserSignin](#browsersignin) 策略配置为“已禁用”，则此策略将不会生效。

如果启用此策略并将其设置为“SignInAndMakeDomainAccountNonRemovable”，则 Microsoft Edge 将使计算机加入到域中的用户使用其 Active Directory 帐户自动登录。

如果将此策略设置为“Disabled”或未设置此策略，则 Microsoft Edge 将不会使计算机加入到域中的用户使用其 Active Directory 帐户自动登录。

策略选项映射：

* Disabled (0) = 已禁用

* SignInAndMakeDomainAccountNonRemovable (1) = 登录并将域帐户设为无法删除

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ConfigureOnPremisesAccountAutoSignIn
  - GP 名称: 配置用 Active Directory 域帐户(如果没有 Azure AD 域帐户)进行的自动登录
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ConfigureOnPremisesAccountAutoSignIn
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  

  [返回顶部](#microsoft-edge---策略)

  ### ConfigureOnlineTextToSpeech
  #### 配置在线文本到语音转换
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  设置浏览器是否可以利用在线文本到语音转换的语音字体，这是 Azure 认知服务的一部分。这些语音字体比预先安装的系统语音字体质量更高。

如果启用或未配置此策略，则使用 SpeechSynthesis API 的基于 Web 的应用程序可以使用在线文本到语音转换的语音字体。

如果禁用此策略，则语音字体不可用。

可在此处了解有关此功能的详细信息:
SpeechSynthesis API: [https://go.microsoft.com/fwlink/?linkid=2110038](https://go.microsoft.com/fwlink/?linkid=2110038)
认知服务: [https://go.microsoft.com/fwlink/?linkid=2110141](https://go.microsoft.com/fwlink/?linkid=2110141)

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ConfigureOnlineTextToSpeech
  - GP 名称: 配置在线文本到语音转换
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ConfigureOnlineTextToSpeech
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ConfigureOnlineTextToSpeech
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ConfigureShare
  #### 配置共享体验
  
  
  #### 支持的版本:
  - 在 Windows 自 83 或之后

  #### 描述
  如果将此策略设置为“ShareAllowed”(默认值)，用户能够在 Microsoft Edge 中从“设置及更多”菜单访问 Windows 10“共享”体验，以便与系统上的其他应用共享。

如果将此策略设置为“ShareDisallowed”，则用户无法访问 Windows 10“共享”体验。如果“共享”按钮位于工具栏上，则它也会隐藏。

策略选项映射：

* ShareAllowed (0) = 允许使用共享体验

* ShareDisallowed (1) = 不允许使用共享体验

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ConfigureShare
  - GP 名称: 配置共享体验
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ConfigureShare
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  

  [返回顶部](#microsoft-edge---策略)

  ### CustomHelpLink
  #### 指定自定义帮助链接
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 79

  #### 描述
  指定 "帮助" 菜单或 F1 键的链接。

如果启用此策略，则管理员可以指定 "帮助" 菜单或 F1 键的链接。

如果禁用或不配置此策略，将使用 "帮助" 菜单或 F1 键的默认链接。

此策略仅适用于已加入到 Microsoft Active Directory 域的 Windows 实例、为设备管理注册的 Windows 10 专业版或企业版实例，或者是通过 MDM 管理或通过 MCX 加入到域的 macOS 实例。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: CustomHelpLink
  - GP 名称: 指定自定义帮助链接
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: CustomHelpLink
  - 值类型: REG_SZ
  ##### 示例值:
```
"https://go.microsoft.com/fwlink/?linkid=2080734"
```


  #### Mac 信息和设置
  - 首选项密钥名称: CustomHelpLink
  - 示例值:
``` xml
<string>https://go.microsoft.com/fwlink/?linkid=2080734</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DNSInterceptionChecksEnabled
  #### 已启用 DNS 拦截检查
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 80

  #### 描述
  此策略配置可用于禁用 DNS 拦截检查的本地交换机。这些检查意图了解浏览器是否在重定向未知主机名的代理后面。

在已知网络配置的企业环境中，可能不需要此检测。可以禁用它，以避免在启动时以及在每次 DNS 配置更改时出现额外的 DNS 和 HTTP 流量。

如果启用或未设置此策略，则会执行 DNS 拦截检查。

如果禁用此策略，则不会执行 DNS 拦截检查。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DNSInterceptionChecksEnabled
  - GP 名称: 已启用 DNS 拦截检查
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DNSInterceptionChecksEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: DNSInterceptionChecksEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultBrowserSettingEnabled
  #### 将 Microsoft Edge 设置为默认浏览器
  
  
  #### 支持的版本:
  - 由于 Windows 7 或更高版本，macOS 和 77

  #### 描述
  如果将此策略设置为 True，则 Microsoft Edge 在启动时会始终检查它是否是默认浏览器，并且如有可能，会自动进行注册。

如果将此策略设置为 False，Microsoft Edge 将停止检查其是否为默认设置，并关闭用户对此选项的控制。

如果未设置此策略，则 Microsoft Edge 允许用户控制它是否为默认设置，如果不是，则控制是否应显示用户通知。

Windows 管理员注意事项: 此策略仅适用于运行 Windows 7 的电脑。对于较高版本的 Windows，必须部署“默认应用程序关联”文件，使 Microsoft Edge 成为 https 和 http 协议(以及 FTP 协议和文件格式(可选)，如 .html、.htm、.pdf、.svg、.webp)的处理程序。有关详细信息，请访问 [https://go.microsoft.com/fwlink/?linkid=2094932](https://go.microsoft.com/fwlink/?linkid=2094932)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultBrowserSettingEnabled
  - GP 名称: 将 Microsoft Edge 设置为默认浏览器
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DefaultBrowserSettingEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultBrowserSettingEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultSearchProviderContextMenuAccessAllowed
  #### 允许默认搜索提供程序上下文菜单搜索访问
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 85

  #### 描述
  允许在上下文菜单上使用默认搜索提供程序。

如果将此策略设置为已禁用，则依赖于默认搜索提供程序和边栏搜索的搜索上下文菜单项将不可用，

如果将此策略设置为已启用或未设置，则默认搜索提供程序和边栏搜索的上下文菜单项将可用。

仅当已启用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 策略时才会应用该策略值，否则不适用。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultSearchProviderContextMenuAccessAllowed
  - GP 名称: 允许默认搜索提供程序上下文菜单搜索访问
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DefaultSearchProviderContextMenuAccessAllowed
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultSearchProviderContextMenuAccessAllowed
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultSensorsSetting
  #### 默认传感器设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  设置网站是否可以访问和使用诸如运动和光线传感器之类的传感器。你可以完全阻止或允许网站访问传感器。

将策略设置为 1 可允许网站访问和使用传感器。将策略设置为 2 会拒绝访问传感器。

可使用 [SensorsAllowedForUrls](#sensorsallowedforurls) 和 [SensorsBlockedForUrls](#sensorsblockedforurls) 策略覆盖特定 URL 模式的此策略。

如果未配置此策略，网站可以访问和使用传感器，用户可以更改此设置。这是 [SensorsAllowedForUrls](#sensorsallowedforurls) 和 [SensorsBlockedForUrls](#sensorsblockedforurls) 的全局默认值。

策略选项映射：

* AllowSensors (1) = 允许网站访问传感器

* BlockSensors (2) = 不允许任何网站访问传感器

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultSensorsSetting
  - GP 名称: 默认传感器设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DefaultSensorsSetting
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultSensorsSetting
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DefaultSerialGuardSetting
  #### 控制串行 API 的使用
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  设置网站是否可以访问串行端口。你可以完全阻止访问，也可以在每次网站想要访问串行端口时询问用户。

将该策略设置为 3 将使网站请求访问串行端口。将该策略设置为 2 将拒绝访问串行端口。

可以使用 [SerialAskForUrls](#serialaskforurls) 和 [SerialBlockedForUrls](#serialblockedforurls) 策略针对特定 URL 模式覆盖此策略。

如果未配置此策略，默认情况下，网站可以询问用户是否可以访问串行端口，并且用户可以更改此设置。

策略选项映射：

* BlockSerial (2) = 不允许任何网站通过串行 API 请求对串行端口的访问

* AskSerial (3) = 允许网站请求访问串行端口的用户权限

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DefaultSerialGuardSetting
  - GP 名称: 控制串行 API 的使用
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DefaultSerialGuardSetting
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: DefaultSerialGuardSetting
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DelayNavigationsForInitialSiteListDownload
  #### 要求在选项卡导航之前企业模式站点列表可用
  
  
  #### 支持的版本:
  - 在 Windows 自 84 或之后

  #### 描述
  允许你指定 Microsoft Edge 选项卡是否等待浏览，直到浏览器下载了初始企业模式站点列表。此设置适用于浏览器主页应在 Internet Explorer 模式下加载的情形，在启用 IE 模式后首次运行浏览器时，执行此操作非常重要。如果不存在这种情况，建议不要启用此设置，因为它可能会对加载主页的性能产生负面影响。仅当 Microsoft Edge 没有缓存的企业模式站点列表时(例如，在启用 IE 模式后浏览器首次运行时)，此设置才适用。

此设置可与以下各项结合使用:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) 设置为“IEMode”
以及
列表中至少有一个条目的 [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) 策略。

可以使用 [NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout) 策略配置此策略的超时行为。

如果将此策略设置为“All”，则当 Microsoft Edge 没有企业模式站点列表的缓存版本时，选项卡会延迟导航，直到浏览器下载了站点列表。配置为通过站点列表在 Internet Explorer 模式下打开的站点将以 Internet Explorer 模式加载，即使在浏览器的初始导航期间也是如此。不能配置为在 Internet Explorer 中打开的站点(例如，使用 http:、https:、file: 或 ftp: 以外的其他方案的任何站点)不会延迟浏览，会立即在 Edge 模式下加载。

如果将此策略设置为“None”或未配置，则当 Microsoft Edge 没有企业模式站点列表的缓存版本时，选项卡将立即导航，而不会等待浏览器下载企业模式站点列表。配置为通过站点列表在 Internet Explorer 模式下打开的站点将在 Microsoft Edge 模式下打开，直到浏览器完成下载企业模式站点列表。

策略选项映射：

* None (0) = 无

* All (1) = 所有符合条件的导航

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DelayNavigationsForInitialSiteListDownload
  - GP 名称: 要求在选项卡导航之前企业模式站点列表可用
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DelayNavigationsForInitialSiteListDownload
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  

  [返回顶部](#microsoft-edge---策略)

  ### DeleteDataOnMigration
  #### 迁移时删除旧浏览器数据
  
  
  #### 支持的版本:
  - 在 Windows 自 83 或之后

  #### 描述
  此策略确定迁移到 Microsoft Edge 版本 81 或更高版本后，是否删除旧版 Microsoft Edge 中的用户浏览数据。

如果将此策略设置为“已启用”，则迁移到 Microsoft Edge 版本 81 或更高版本后，旧版 Microsoft Edge 中的所有浏览数据都将被删除。必须在迁移到 Microsoft Edge 版本 81 或更高版本之前设置此策略，这样才能对现有浏览数据产生影响。

如果将此策略设置为“已禁用”，或者未配置此策略，则在迁移到 Microsoft Edge 版本 83 或更高版本后，不会删除用户浏览数据。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DeleteDataOnMigration
  - GP 名称: 迁移时删除旧浏览器数据
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DeleteDataOnMigration
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  

  [返回顶部](#microsoft-edge---策略)

  ### DeveloperToolsAvailability
  #### 控制可以使用开发人员工具的位置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  控制可以使用开发人员工具的位置。

如果将此策略设置为“DeveloperToolsDisallowedForForceInstalledExtensions”(默认值)，则用户通常可以访问开发人员工具和 JavaScript 控制台，但不能在按企业策略安装的扩展环境中访问。

如果将此策略设置为“DeveloperToolsAllowed”，则用户可以在所有环境中访问开发人员工具和 JavaScript 控制台，还能在按企业策略安装的扩展中访问。

如果将此策略设置为“DeveloperToolsDisallowed”，则用户无法访问开发人员工具或检查网站元素。用于打开开发人员工具或 JavaScript 控制台的键盘快捷方式和菜单或上下文菜单条目处于禁用状态。

策略选项映射：

* DeveloperToolsDisallowedForForceInstalledExtensions (0) = 在按企业策略安装的扩展上阻止开发人员工具，允许在其他上下文中使用

* DeveloperToolsAllowed (1) = 允许使用开发人员工具

* DeveloperToolsDisallowed (2) = 不允许使用开发人员工具

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DeveloperToolsAvailability
  - GP 名称: 控制可以使用开发人员工具的位置
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DeveloperToolsAvailability
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: DeveloperToolsAvailability
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DiagnosticData
  #### 发送有关浏览器使用情况的必需和可选诊断数据
  
  
  #### 支持的版本:
  - 由于 Windows 7 或更高版本，macOS 和 86

  #### 描述
  此策略控制向 Microsoft 发送有关浏览器使用情况的必需和可选诊断数据。

收集必要的诊断数据以确保 Microsoft Edge 安全、最新并按预期运行。

可选诊断数据包括有关使用浏览器的方式、访问的网站以及为改进产品和服务而向 Microsoft 发送的崩溃报告的数据。

此策略在 Windows 10 设备上不受支持。若要在 Windows 10 上控制此数据收集，IT 管理员必须使用 Windows 诊断数据组策略。此策略将为“允许遥测”或“允许诊断数据”，具体取决于 Windows 版本。详细了解 Windows 10 诊断数据收集: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

使用以下设置之一来配置此策略:

“Off”会关闭必需和可选诊断数据收集。不建议使用此选项。

必需数据(1)会发送必需的诊断数据，但会关闭可选诊断数据收集。Microsoft Edge 将发送必需的诊断数据以确保 Microsoft Edge 安全、最新并按预期运行。

“可选数据”将发送可选诊断数据，其中包括有关浏览器使用情况、访问的网站以及为改进产品和服务而向 Microsoft 发送的崩溃报告的数据。

在 Windows 7/macOS 上，此策略控制向 Microsoft 发送必需和可选数据。

 如果你未配置此策略或禁用它，则 Microsoft Edge 将默认为用户的首选项。

策略选项映射：

* Off (0) = 关闭(不推荐)

* RequiredData (1) = 必需数据

* OptionalData (2) = 可选数据

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DiagnosticData
  - GP 名称: 发送有关浏览器使用情况的必需和可选诊断数据
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DiagnosticData
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: DiagnosticData
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DirectInvokeEnabled
  #### 允许用户使用 DirectInvoke 协议打开文件
  
  
  #### 支持的版本:
  - 在 Windows 自 78 或之后

  #### 描述
  允许用户使用 DirectInvoke 协议打开文件。DirectInvoke 协议允许网站使用用户的计算机或设备上的特定文件处理程序请求浏览器打开特定 URL 中的文件。

如果启用或未配置此策略，则用户可以使用 DirectInvoke 协议打开文件。

如果禁用此策略，则用户无法使用 DirectInvoke 协议打开文件。文件将被保存到文件系统中。

注意：禁用 DirectInvoke 可能会阻止某些 Microsoft Office SharePoint Online 功能按预期方式工作。

有关 DirectInvoke 的详细信息，请参阅 [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) 和 [https://go.microsoft.com/fwlink/?linkid=2099871](https://go.microsoft.com/fwlink/?linkid=2099871)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DirectInvokeEnabled
  - GP 名称: 允许用户使用 DirectInvoke 协议打开文件
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DirectInvokeEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  

  [返回顶部](#microsoft-edge---策略)

  ### Disable3DAPIs
  #### 禁用对 3D 图形 API 的支持
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  防止网页访问图形处理单元(GPU)。具体而言，网页不能访问 WebGL API 并且插件不能使用 Pepper 3D API。

如果未配置或禁用此策略，则可能会允许网页使用 WebGL API 并允许插件使用 Pepper 3D API。默认情况下，Microsoft Edge 可能仍需要传递命令行参数才能使用这些 API。

如果 [HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled) 策略设置为 false，则 [Disable3DAPIs](#disable3dapis) 策略的设置会被忽略 - 这等同于将 [Disable3DAPIs](#disable3dapis) 策略设置为 true。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: Disable3DAPIs
  - GP 名称: 禁用对 3D 图形 API 的支持
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: Disable3DAPIs
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: Disable3DAPIs
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DisableScreenshots
  #### 禁用进行屏幕截图
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  控制用户是否可以截取浏览器页面的屏幕截图。

如果启用，则用户无法使用键盘快捷方式或扩展 API 截取屏幕截图。

如果禁用或不配置此策略，则用户可以截取屏幕截图。

请注意，此策略控制从浏览器本身内部截取的屏幕截图。即使启用此策略，用户或许仍可以在浏览器之外使用某些方法（例如使用操作系统功能或其他应用程序）截取屏幕截图。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DisableScreenshots
  - GP 名称: 禁用进行屏幕截图
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DisableScreenshots
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: DisableScreenshots
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DiskCacheDir
  #### 设置磁盘缓存目录
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  配置用于存储缓存文件的目录。

如果启用此策略，那么无论用户是否已指定 "--disk-cache-dir" 标志，Microsoft Edge 都将使用提供的目录。为避免数据丢失或其他意外错误，请不要将此策略配置为使用卷的根目录或用于其他用途的目录，因为 Microsoft Edge 会管理其内容。

有关在指定目录和路径时可以使用的变量列表，请参阅 [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041)。

如果你未配置此策略，则使用默认缓存目录，用户可以使用 "--disk-cache-dir" 命令行标志替代该默认值。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DiskCacheDir
  - GP 名称: 设置磁盘缓存目录
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DiskCacheDir
  - 值类型: REG_SZ
  ##### 示例值:
```
"${user_home}/Edge_cache"
```


  #### Mac 信息和设置
  - 首选项密钥名称: DiskCacheDir
  - 示例值:
``` xml
<string>${user_home}/Edge_cache</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DiskCacheSize
  #### 设置磁盘缓存大小(字节)
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  配置用于在磁盘上存储文件的缓存的大小(以字节为单位)。

如果启用此策略，那么无论用户是否指定了 "--disk-cache-size" 标志，Microsoft Edge 都会使用提供的缓存大小。此策略中指定的值不是严格界限，而是针对缓存系统的建议；低于几兆字节的任何值都太小，将被舍入为合理的最小值。

如果将此策略的值设置为 0，则将使用默认缓存大小，而且用户无法更改它。

如果未配置此策略，则将使用默认大小，但用户可以使用 "--disk-cache-size" 标志替代它。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DiskCacheSize
  - GP 名称: 设置磁盘缓存大小(字节)
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DiskCacheSize
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x06400000
```


  #### Mac 信息和设置
  - 首选项密钥名称: DiskCacheSize
  - 示例值:
``` xml
<integer>104857600</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DnsOverHttpsMode
  #### 控制 DNS-over-HTTPS 的模式
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 83

  #### 描述
  控制 DNS-over-HTTPS 解析程序的模式。请注意，此策略将仅为每个查询设置默认模式。对于特殊类型的查询（例如，请求解析 DNS-over-HTTPS  服务器主机名的请求），可以覆盖此模式。

"off" 模式将禁用 DNS-over-HTTPS。

如果 DNS-over-HTTPS 服务器可用，则 "automatic" 模式将首先发送 DNS-over-HTTPS 查询，并且可能会回退到因错误而发送不安全的查询。

"secure" 模式将仅发送 DNS-over-HTTPS 查询，将无法解决错误。

 如果您未配置此策略，则浏览器可能会将 DNS-over-HTTPS 请求发送到与用户配置的系统解析程序关联的解析程序。

策略选项映射：

* off (off) = 禁用 DNS-over-HTTPS

* automatic (automatic) = 启用具有不安全回退功能的 DNS-over-HTTPS

* secure (secure) = 启用不带不安全回退功能的 DNS-over-HTTPS

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DnsOverHttpsMode
  - GP 名称: 控制 DNS-over-HTTPS 的模式
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DnsOverHttpsMode
  - 值类型: REG_SZ
  ##### 示例值:
```
"off"
```


  #### Mac 信息和设置
  - 首选项密钥名称: DnsOverHttpsMode
  - 示例值:
``` xml
<string>off</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DnsOverHttpsTemplates
  #### 指定所需的 IP-HTTPS DNS 解析程序的 URI 模板
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 83

  #### 描述
  所需的 DNS-over-HTTPS 解析程序的 URI 模板。若要指定多个 DNS-over-HTTPS 解析程序，请用空格分隔相应的 URI 模板。

如果已将 [DnsOverHttpsMode](#dnsoverhttpsmode) 设置为 "secure"，则必须设置此策略并且它不能为空。

如果已将 [DnsOverHttpsMode](#dnsoverhttpsmode) 设置为 "automatic" 并且已设置此策略，则将使用指定的 URI 模板。如果未设置此策略，则将使用硬编码映射来尝试将用户当前的 DNS 解析程序升级到由同一提供商运营的 DoH 解析程序。

如果 URI 模板包含 dns 变量，则对解析程序的请求将使用 GET；否则，请求将使用 POST。

将忽略格式不正确的模板。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DnsOverHttpsTemplates
  - GP 名称: 指定所需的 IP-HTTPS DNS 解析程序的 URI 模板
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: DnsOverHttpsTemplates
  - 值类型: REG_SZ
  ##### 示例值:
```
"https://dns.example.net/dns-query{?dns}"
```


  #### Mac 信息和设置
  - 首选项密钥名称: DnsOverHttpsTemplates
  - 示例值:
``` xml
<string>https://dns.example.net/dns-query{?dns}</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DownloadDirectory
  #### 设置下载目录
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  配置下载文件时要使用的目录。

如果启用此策略，Microsoft Edge 将使用提供的目录，无论用户是已指定目录还是选择每次都提示提供下载位置。有关可以使用的变量列表，请参阅 [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041)。

如果禁用或未配置此策略，则使用默认下载目录，但用户可以更改它。

如果设置了无效路径，Microsoft Edge 将默认使用用户的默认下载目录。

如果路径指定的文件夹不存在，则下载将触发提示，询问用户他们想要保存下载的位置。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DownloadDirectory
  - GP 名称: 设置下载目录
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: DownloadDirectory
  - 值类型: REG_SZ
  ##### 示例值:
```
"\n      Linux-based OSes (including Mac): /home/${user_name}/Downloads\n      Windows: C:\\Users\\${user_name}\\Downloads"
```


  #### Mac 信息和设置
  - 首选项密钥名称: DownloadDirectory
  - 示例值:
``` xml
<string>
      Linux-based OSes (including Mac): /home/${user_name}/Downloads
      Windows: C:\Users\${user_name}\Downloads</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### DownloadRestrictions
  #### 允许使用下载限制
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  配置 Microsoft Edge 完全阻止的下载类型，不让用户覆盖安全决策。

设置“BlockDangerousDownloads”可以允许所有下载，但带有 Microsoft Defender SmartScreen 警告的下载除外。

设置“BlockPotentiallyDangerousDownloads”可以允许所有下载，但带有 Microsoft Defender SmartScreen 潜在危险或不需要的下载警告的下载除外。

设置“BlockAllDownloads”可以阻止所有下载。

如果未配置此策略或者设置“DefaultDownloadSecurity”选项，则下载将根据 Microsoft Defender SmartScreen 的分析结果受到普通安全限制。

请注意，这些限制适用于网页内容下载以及“下载链接...”上下文菜单选项。这些限制不适用于保存或下载当前显示的页面，也不适用于打印选项中的“另存为 PDF”选项。

有关 Microsoft Defender SmartScreen 的详细信息，请参阅 [https://go.microsoft.com/fwlink/?linkid=2094934](https://go.microsoft.com/fwlink/?linkid=2094934)。

策略选项映射：

* DefaultDownloadSecurity (0) = 无特殊限制

* BlockDangerousDownloads (1) = 阻止危险的下载

* BlockPotentiallyDangerousDownloads (2) = 阻止可能导致危险或不需要的下载

* BlockAllDownloads (3) = 阻止所有下载

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: DownloadRestrictions
  - GP 名称: 允许使用下载限制
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: DownloadRestrictions
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: DownloadRestrictions
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### EdgeCollectionsEnabled
  #### 启用集锦功能
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 78

  #### 描述
  使你能够支持用户访问集锦功能，利用此功能，他们可以通过 Office 集成更高效地收集、组织、共享和导出内容。

如果启用或未配置此策略，则用户可以在 Microsoft Edge 中访问和使集锦功能。

如果禁用此策略，则用户无法在 Microsoft Edge 中访问和使集锦。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: EdgeCollectionsEnabled
  - GP 名称: 启用集锦功能
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: EdgeCollectionsEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: EdgeCollectionsEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### EditFavoritesEnabled
  #### 允许用户编辑收藏夹
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  启用此策略可让用户添加、删除和修改收藏夹。如果未配置此策略，则这是默认行为。

禁用此策略可阻止用户添加、删除或修改收藏夹。他们仍可使用现有收藏夹。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: EditFavoritesEnabled
  - GP 名称: 允许用户编辑收藏夹
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: EditFavoritesEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: EditFavoritesEnabled
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### EnableDeprecatedWebPlatformFeatures
  #### 在有限的时间内重新启用弃用的 Web 平台功能
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定要暂时重新启用的弃用 Web 平台功能列表。

此策略允许你在有限的时间内重新启用弃用的 Web 平台功能。这些功能由字符串标签标识。

如果不配置此策略，或者列表为空，或者某个功能不能与某一受支持的字符串标签匹配，则所有弃用的 Web 平台功能将仍是禁用的。

虽然上述平台支持此策略，但它启用的功能可能并不在所有这些平台上都可用。并非所有弃用的 Web 平台功能都可以重新启用。只有下面明确列出的功能才能重新启用，并且只能在有限的时间内重新启用，具体取决于每项功能。你可以查看 https://bit.ly/blinkintents 了解网站平台功能变化背后的意图。

字符串标记的常规格式为 [DeprecatedFeatureName] _EffectiveUntil [yyyymmdd]。

策略选项映射：

* ExampleDeprecatedFeature (ExampleDeprecatedFeature_EffectiveUntil20080902) = 启用 ExampleDeprecatedFeature API 直至 2008 年 9 月 2 日

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: EnableDeprecatedWebPlatformFeatures
  - GP 名称: 在有限的时间内重新启用弃用的 Web 平台功能
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures\1 = "ExampleDeprecatedFeature_EffectiveUntil20080902"

```


  #### Mac 信息和设置
  - 首选项密钥名称: EnableDeprecatedWebPlatformFeatures
  - 示例值:
``` xml
<array>
  <string>ExampleDeprecatedFeature_EffectiveUntil20080902</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### EnableDomainActionsDownload
  #### 启用从 Microsoft 进行域操作下载 (过时)
  
  >过时: 此策略已过时，在 Microsoft Edge 84 之后无法使用。
  #### 支持的版本:
  - 在 Windows 后，在 macOS 和 77 上 84

  #### 描述
  该政策无效，因为应避免发生冲突的状态。此策略用于启用/禁用域操作列表的下载，不过它并不会始终实现所需状态。处理下载的试验和配置服务使用自己的策略配置从服务下载的内容。请改用 [ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol) 策略。

在 Microsoft Edge 中，域操作表示一系列兼容性功能，这些功能可帮助浏览器在 Web 上正常工作。

出于兼容性原因，Microsoft 会保留针对某些域采取的操作的列表。例如，如果某个网站由于 Microsoft Edge 上的新用户代理字符串而中断，则浏览器可能会覆盖该网站上的用户代理字符串。在 Microsoft 尝试与站点所有者一起解决问题时，所有这些操作都是临时性操作。

当浏览器启动后，浏览器会定期与包含最新待执行兼容性操作列表的试验和配置服务联系。此列表在第一次被检索后保存在本地，以便后续请求仅在服务器的副本发生更改时才会更新列表。

如果启用此策略，将继续通过试验和配置服务下载域操作列表。

如果禁用此策略，则不再通过试验和配置服务下载域操作列表。

如果未配置此策略，则将继续通过试验和配置服务下载域操作列表。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: EnableDomainActionsDownload
  - GP 名称: 启用从 Microsoft 进行域操作下载 (过时)
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: EnableDomainActionsDownload
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: EnableDomainActionsDownload
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### EnableOnlineRevocationChecks
  #### 启用联机 OCSP/CRL 检查
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  联机吊销检查并不具备显著的安全优势，并且默认情况下将其禁用。

如果启用此策略，则 Microsoft Edge 将执行软失败的联机 OCSP/CRL 检查。“软失败”是指如果无法访问吊销服务器，则该证书将被视为有效。

如果禁用或未配置此策略，则 Microsoft Edge 不会执行联机吊销检查。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: EnableOnlineRevocationChecks
  - GP 名称: 启用联机 OCSP/CRL 检查
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: EnableOnlineRevocationChecks
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: EnableOnlineRevocationChecks
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### EnableSha1ForLocalAnchors
  #### 由本地信任锚颁发时，允许使用 SHA-1 签名的证书 (已弃用)
  >已弃用: 此策略已弃用。目前仍受支持，但将在未来版本中弃用。
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 85

  #### 描述
  启用此设置后，只要证书链接到本地安装的根证书且有效，则 Microsoft Edge 允许受 SHA-1 签名证书保护的连接。

请注意，此策略取决于允许 SHA-1 签名的操作系统(OS)证书验证堆栈。如果操作系统更新更改了处理 SHA-1 证书的操作系统，则此策略可能不再有效。此外，此策略旨在用作临时解决方法，让企业有更多时间迁离 SHA-1。我们将在 2021 年年中发布的 Microsoft Edge 92 中删除此策略。

如果你未设置此策略或将其设置为 false，或者将 SHA-1 证书链接到了公开信任的根证书，则 Microsoft Edge 将不允许使用 SHA-1 签名的证书。

此策略仅在已加入 Microsoft Active Directory 域的 Windows 实例、为设备管理注册的 Windows 10 专业版或企业版实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例上可用。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: EnableSha1ForLocalAnchors
  - GP 名称: 由本地信任锚颁发时，允许使用 SHA-1 签名的证书 (已弃用)
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: EnableSha1ForLocalAnchors
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: EnableSha1ForLocalAnchors
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### EnterpriseHardwarePlatformAPIEnabled
  #### 允许托管扩展使用企业硬件平台 API
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 78

  #### 描述
  如果将此策略设置为“已启用”，则允许通过企业策略安装的扩展使用企业硬件平台 API。
如果此策略设置为“已禁用”，或者未设置此策略，则不允许扩展使用企业硬件平台 API。
此策略也适用于组件扩展。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: EnterpriseHardwarePlatformAPIEnabled
  - GP 名称: 允许托管扩展使用企业硬件平台 API
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: EnterpriseHardwarePlatformAPIEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: EnterpriseHardwarePlatformAPIEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### EnterpriseModeSiteListManagerAllowed
  #### 允许访问 Enterprise Mode Site List Manager 工具
  
  
  #### 支持的版本:
  - 在 Windows 自 86 或之后

  #### 描述
  允许你设置用户是否可以使用 Enterprise Mode Site List Manager。

如果启用此策略，则用户可以在 edge://compat 页面上看到 Enterprise Mode Site List Manager 导航按钮，导航至该工具并使用它。

如果禁用或未配置此策略，则用户将看不到 Enterprise Mode Site List Manager 导航按钮，也将无法使用它。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: EnterpriseModeSiteListManagerAllowed
  - GP 名称: 允许访问 Enterprise Mode Site List Manager 工具
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: EnterpriseModeSiteListManagerAllowed
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  

  [返回顶部](#microsoft-edge---策略)

  ### ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  #### 对域上的指定文件类型禁用基于下载文件类型扩展名的警告
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 85

  #### 描述
  你可以启用此策略来创建文件类型扩展名的字典，其相应的域列表将免于基于文件类型扩展名的下载警告。这使企业管理员可以阻止与列出的域关联的文件的基于文件扩展名的下载警告。例如，如果“jnlp”扩展名与“website1.com”关联，则用户从“website1.com”下载“jnlp”文件时不会看到警告，但从“website2.com”下载“jnlp”文件时会看到下载警告。

具有为此策略标识的域指定的文件类型扩展名的文件仍将受到基于非文件类型扩展名的安全警告，例如混合内容下载警告和 Microsoft Defender SmartScreen 警告。

如果你禁用或未配置此策略，则触发基于扩展名的下载警告的文件类型将向用户显示警告。

如果启用此策略：

* URL 模式应根据 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) 设置格式。
* 输入的文件扩展名必须使用小写 ASCII。 列出文件类型扩展名时，不应包括前导分隔符，因此应使用列表“jnlp”代替“.jnlp”。

示例：

以下示例值将防止 *.contoso.com 域在 swf、exe 和 jnlp扩展名上出现基于文件类型扩展名的下载警告。 它将在其他任何域上为用户显示 exe 和 jnlp 文件基于文件扩展名的下载警告，而不显示 swf 文件。

[
  { "file_extension": "jnlp", "domains": ["contoso.com"] },
  { "file_extension": "exe", "domains": ["contoso.com"] },
  { "file_extension": "swf", "domains": ["*"] }
]

请注意，尽管前面的示例显示了针对所有域的“swf”文件的基于文件类型扩展名的下载警告的抑制，但是出于安全考虑，建议不要针对所有危险文件类型扩展名对所有域应用此类警告的抑制。 在示例中仅显示了这样做的能力。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - GP 名称: 对域上的指定文件类型禁用基于下载文件类型扩展名的警告
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\1 = {"domains": ["https://contoso.com", "contoso2.com"], "file_extension": "jnlp"}
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\2 = {"domains": ["*"], "file_extension": "swf"}

```


  #### Mac 信息和设置
  - 首选项密钥名称: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - 示例值:
``` xml
<array>
  <string>{'domains': ['https://contoso.com', 'contoso2.com'], 'file_extension': 'jnlp'}</string>
  <string>{'domains': ['*'], 'file_extension': 'swf'}</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ExperimentationAndConfigurationServiceControl
  #### 控制与实验和配置服务的通信
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  Microsoft Edge 使用试验和配置服务来部署试验和配置有效负载。

试验有效负载由一系列 Microsoft 为测试和反馈而启用的处于早期开发阶段的功能组成。

配置有效负载由一系列 Microsoft 希望部署到 Microsoft Edge 以优化用户体验的设置组成。例如，配置有效负载可以指定 Microsoft Edge 将请求发送到试验和配置服务以检索最新有效负载的频率。

此外，配置有效负载还可以包含由于兼容性原因而要对特定域执行的操作的列表。例如，如果某个网站由于 Microsoft Edge 上的新用户代理字符串而中断，则浏览器可能会覆盖该网站上的用户代理字符串。在 Microsoft 尝试与站点所有者一起解决问题时，所有这些操作都是临时性操作。

如果将此策略设置为“FullMode”，则将从试验和配置服务下载完整有效负载，包括试验有效负载和配置有效负载。

如果将此策略设置为“ConfigurationsOnlyMode”，则仅提供配置有效负载。

如果将此策略设置为“RestrictedMode”，则与试验和配置服务的通信将完全停止。

如果未配置此策略，则位于稳定通道和测试通道的托管设备上的行为与“ConfigurationsOnlyMode”相同。

如果未配置此策略，则非托管设备上的行为与“FullMode”相同。

策略选项映射：

* FullMode (2) = 检索配置和试验

* ConfigurationsOnlyMode (1) = 仅检索配置

* RestrictedMode (0) = 禁止与实验和配置服务通信

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ExperimentationAndConfigurationServiceControl
  - GP 名称: 控制与实验和配置服务的通信
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ExperimentationAndConfigurationServiceControl
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: ExperimentationAndConfigurationServiceControl
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ExternalProtocolDialogShowAlwaysOpenCheckbox
  #### 在外部协议对话框中显示“始终打开”复选框
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 79

  #### 描述
  此策略控制“始终允许该站点打开此类型的链接”复选框是否在外部协议启动确认提示上显示。此策略仅适用于 https:// links。

 如果启用此策略，则显示外部协议确认提示时，用户可以选择“始终允许”以跳过此站点上该协议将来的所有确认提示。

 如果禁用此策略，则不会显示“始终允许”复选框。每次调用外部协议时，系统都将提示用户进行确认。

 在 Microsoft Edge 83之前，如果未配置此策略，则不会显示“始终允许”复选框。每次调用外部协议时，都会提示用户进行确认。

 在 Microsoft Edge 83上，如果未配置此策略，则复选框的可见性由 edge://flags 中的“启用记住协议启动提示首选项”标志控制

从 Microsoft Edge 84开始，如果未配置此策略，则在显示外部协议确认提示时，用户可以选择“始终允许”以跳过以后在此站点上对该协议进行的所有确认提示。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - GP 名称: 在外部协议对话框中显示“始终打开”复选框
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### FamilySafetySettingsEnabled
  #### 允许用户配置“Family Safety”
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 83

  #### 描述
  此策略在“设置”中禁用并完全隐藏“Family Safety”页面。也将阻止导航到 edge://settings/familysafety。“Family Safety”页面描述了家庭组可以使用的具体功能以及如何加入家庭组。请在此处了解有关家庭安全的更多信息: ([https://go.microsoft.com/fwlink/?linkid=2098432](https://go.microsoft.com/fwlink/?linkid=2098432))。

如果启用或未配置此策略，则将显示“Family Safety”页面。

如果禁用此策略，则不会显示“Family Safety”页面。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: FamilySafetySettingsEnabled
  - GP 名称: 允许用户配置“Family Safety”
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: FamilySafetySettingsEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: FamilySafetySettingsEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### FavoritesBarEnabled
  #### 启用收藏夹栏
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  启用或禁用收藏夹栏。

如果启用此策略，则用户将看到收藏夹栏。

如果禁用此策略，则用户将看不到收藏夹栏。

如果未配置此策略，则用户可以决定是否使用收藏夹栏。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: FavoritesBarEnabled
  - GP 名称: 启用收藏夹栏
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: FavoritesBarEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: FavoritesBarEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ForceBingSafeSearch
  #### 强制执行必应安全搜索
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  确保必应 Web 搜索中的查询是在将安全搜索设置为指定值后完成的。用户无法更改此设置。

如果将此策略配置为“BingSafeSearchNoRestrictionsMode”，则必应搜索中的安全搜索将恢复为 bing.com 值。

如果将此策略配置为“BingSafeSearchModerateMode”，则在安全搜索中使用适中的设置。适中的设置会从搜索结果中筛选成人视频和图像，但不筛选文本。

如果将此策略配置为“BingSafeSearchStrictMode”，则使用安全搜索中的严格设置。严格设置会筛选成人文本、图像和视频。

如果禁用此策略或者未对其进行配置，则不会强制在必应搜索中执行安全搜索，用户可以在 bing.com 上设置他们想要的值。

策略选项映射：

* BingSafeSearchNoRestrictionsMode (0) = 不在必应中配置搜索限制

* BingSafeSearchModerateMode (1) = 在必应中配置适中的搜索限制

* BingSafeSearchStrictMode (2) = 在必应中配置严格的搜索限制

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ForceBingSafeSearch
  - GP 名称: 强制执行必应安全搜索
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ForceBingSafeSearch
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: ForceBingSafeSearch
  - 示例值:
``` xml
<integer>0</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ForceCertificatePromptsOnMultipleMatches
  #### 配置当使用 "AutoSelectCertificateForUrls" 配置的站点拥有多个证书匹配项时，Microsoft Edge 是否应自动选择证书
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 81

  #### 描述
  当有多个可用证书并且站点配置有 [AutoSelectCertificateForUrls](#autoselectcertificateforurls) 时，切换是否提示用户选择证书。如果未为站点配置 [AutoSelectCertificateForUrls](#autoselectcertificateforurls)，将始终提示用户选择证书。

如果将此策略设置为 True，Microsoft Edge 将提示用户为 [AutoSelectCertificateForUrls](#autoselectcertificateforurls) 中定义的列表上的站点选择证书，前提是如果且仅当存在多个证书。

如果将此策略设置为 False 或未配置此策略，则即使有多个证书匹配项，Microsoft Edge 也将自动选择证书。将不会提示用户为 [AutoSelectCertificateForUrls](#autoselectcertificateforurls) 中定义的列表上的站点选择证书。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ForceCertificatePromptsOnMultipleMatches
  - GP 名称: 配置当使用 "AutoSelectCertificateForUrls" 配置的站点拥有多个证书匹配项时，Microsoft Edge 是否应自动选择证书
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ForceCertificatePromptsOnMultipleMatches
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ForceCertificatePromptsOnMultipleMatches
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ForceEphemeralProfiles
  #### 启用临时用户配置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  控制是否将用户用户配置切换到临时模式。临时用户配置在会话开始时创建，在会话结束时被删除，并且与用户的原始用户配置相关联。

如果启用此策略，则用户配置将在临时模式下运行。这样，用户就可以在自己的设备上工作，而无需将浏览数据保存到这些设备。如果将此策略启用为 OS 策略（例如，通过使用 Windows 上的 GPO），则该策略将应用于系统上的每个用户配置。

如果禁用或未配置此策略，则用户在登录到浏览器时将获取常规用户配置。

在临时模式下，用户配置数据仅在用户会话期间保存在磁盘上。浏览器关闭后，浏览器历史记录、扩展及其数据、Cookie 等 Web 数据和 Web 数据库等功能不会保存。这不会阻碍用户将任何数据手动下载到磁盘，也不会阻止用户保存或打印页面。如果用户启用了同步，则所有数据将与常规用户配置一样保留在其同步帐户中。用户也可以在临时模式下使用 InPrivate 浏览，除非你明确禁用此功能。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ForceEphemeralProfiles
  - GP 名称: 启用临时用户配置
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ForceEphemeralProfiles
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ForceEphemeralProfiles
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ForceGoogleSafeSearch
  #### 强制执行 Google 安全搜索
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  强制执行 Google Web 搜索中的查询并将安全搜索设置为活动，以及阻止用户更改此设置。

如果启用此策略，Google 搜索中的安全搜索将始终处于活动状态。

如果禁用或未配置此策略，将不执行 Google 搜索中的安全搜索。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ForceGoogleSafeSearch
  - GP 名称: 强制执行 Google 安全搜索
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ForceGoogleSafeSearch
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: ForceGoogleSafeSearch
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ForceLegacyDefaultReferrerPolicy
  #### 使用 no-referrer-when-downgrade 的默认引用站点策略 (已弃用)
  >已弃用: 此策略已弃用。目前仍受支持，但将在未来版本中弃用。
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 81

  #### 描述
  此策略已弃用，因为它旨在仅作为一种短期机制，让企业在发现它与当前默认应用站点策略不兼容时，有更多时间更新其 Web 内容。它将无法在 Microsoft Edge 版本 86 中正常工作。

通过逐步推出，Microsoft Edge 的默认引用站点策略正在加强安全性，其 no-referr-when-downgrade 当前值会变为更安全的 strict-origin-when-cross-origin。

在推出之前，此企业策略将无效。推出后，如果启用此企业策略，则 Microsoft Edge 的默认引用站点策略将设置为之前的值 no-referrer-when-downgrade。

此企业策略默认处于禁用状态。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ForceLegacyDefaultReferrerPolicy
  - GP 名称: 使用 no-referrer-when-downgrade 的默认引用站点策略 (已弃用)
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ForceLegacyDefaultReferrerPolicy
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: ForceLegacyDefaultReferrerPolicy
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ForceNetworkInProcess
  #### 强制网络代码在浏览器进程中运行 (过时)
  
  >过时: 此策略已过时，在 Microsoft Edge 83 之后无法使用。
  #### 支持的版本:
  - 在 Windows 从 78 到 83

  #### 描述
  此策略无效，因为它旨在仅作为一种短期机制，为企业提供更多时间来迁移到不依赖于挂钩网络 API 的第三方软件。建议使用代理服务器，而不是 LSP 和 Win32 API 修补程序。

此策略强制网络代码在浏览器进程中运行。

此策略默认禁用。如果启用，则在对网络进程进行沙盒处理时，用户会遇到安全问题。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ForceNetworkInProcess
  - GP 名称: 强制网络代码在浏览器进程中运行 (过时)
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ForceNetworkInProcess
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  

  [返回顶部](#microsoft-edge---策略)

  ### ForceSync
  #### 强制同步浏览器数据，但不显示同步许可提示
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  在 Microsoft Edge 中强制进行数据同步。此策略还可以防止用户关闭同步。

如果未配置此策略，则用户将可以打开或关闭同步。如果启用此策略，则用户将无法关闭同步。

为使此策略按预期工作，
[BrowserSignin](#browsersignin) 策略必须未配置或必须设置为启用。如果将 [ForceSync](#forcesync) 设置为禁用，则 [BrowserSignin](#browsersignin) 将不起作用。

[SyncDisabled](#syncdisabled) 不得配置或必须设置为 False。如果将其设置为 True，则 [ForceSync](#forcesync) 不会生效。

0 = 不自动开始同步并显示同步许可(默认)
1 = 强制为 Azure AD/Azure AD 降级的用户配置文件启用同步，并且不显示同步许可提示

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ForceSync
  - GP 名称: 强制同步浏览器数据，但不显示同步许可提示
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ForceSync
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ForceSync
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ForceYouTubeRestrict
  #### 实施最小 YouTube 受限模式
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  在 YouTube 上实施最小受限模式，并阻止用户选取较低的限制模式。

设置为“Strict”以在 YouTube 上实施严格受限模式。

 设置为“Moderate”以强制用户在 YouTube 上仅使用中等受限模式和严格受限模式。用户不能禁用限制模式。

设置为“Off”或不配置此策略，则不会在 YouTube 上实施受限模式。YouTube 策略等外部策略可能仍然会实施限制模式。

策略选项映射：

* Off (0) = 不在 YouTube 上实施最小受限模式

* Moderate (1) = 在 YouTube 上至少强制中等受限模式

* Strict (2) = 对 YouTube 强制严格受限模式

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ForceYouTubeRestrict
  - GP 名称: 实施最小 YouTube 受限模式
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ForceYouTubeRestrict
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: ForceYouTubeRestrict
  - 示例值:
``` xml
<integer>0</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### FullscreenAllowed
  #### 允许全屏模式
  
  
  #### 支持的版本:
  - 在 Windows 自 77 或之后

  #### 描述
  设置全屏模式的可用性 - 整个 Microsoft Edge UI 处于隐藏状态，只有 Web 内容可见。

如果启用或未配置此策略，则具有适当权限的用户、应用和扩展可以进入全屏模式。

如果禁用此策略，则用户、应用和扩展将无法进入全屏模式。

在禁用全屏模式时，无法使用命令行在展台模式下打开 Microsoft Edge。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: FullscreenAllowed
  - GP 名称: 允许全屏模式
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: FullscreenAllowed
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  

  [返回顶部](#microsoft-edge---策略)

  ### GloballyScopeHTTPAuthCacheEnabled
  #### 启用全局范围的 HTTP 身份验证缓存
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 81

  #### 描述
  此策略使用 HTTP 服务器身份验证凭据为每个用户配置缓存配置单个全局设置。

如果禁用或未设置此策略，则浏览器将使用默认的跨站点身份验证行为，自版本 80 开始，此操作通过顶级站点审查 HTTP 服务器身份验证凭据。因此，如果两个站点使用来自同一身份验证域的资源，则需要在两个站点的上下文中独立提供凭据。缓存的代理凭据将在各个站点之间重用。

如果启用此策略，则在一个站点的上下文中输入的 HTTP 身份验证凭据将自动用于另一个站点的上下文中。

启用此策略会使站点面临某些类型的跨站点攻击，并且通过使用 URL 中嵌入的凭据将条目添加到 HTTP 身份验证缓存中，甚至可以在没有 Cookie 的情况下也可以跨站点跟踪用户。

此策略旨在根据传统行为使企业能够更新其登录程序，并且以后将被删除。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: GloballyScopeHTTPAuthCacheEnabled
  - GP 名称: 启用全局范围的 HTTP 身份验证缓存
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: GloballyScopeHTTPAuthCacheEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: GloballyScopeHTTPAuthCacheEnabled
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### GoToIntranetSiteForSingleWordEntryInAddressBar
  #### 强制进行直接 Intranet 站点导航而不是在地址栏中对单个词条进行搜索
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 78

  #### 描述
  如果启用此策略，在地址栏中输入不含标点的单个字词文本后，则地址栏建议列表中的第一项自动建议结果将导航到 Intranet 站点。

键入不含标点的单个字词后，将导航到与输入的文本匹配的 Intranet 站点。

如果启用此策略，在此文本为不含标点的单个字词的情况下，地址栏建议列表中的第二项自动建议结果将按照所输入内容精确进行 Web 搜索。除非还启用了可阻止 Web 搜索的策略，否则将使用默认搜索提供程序。

启用此策略可达到两种效果:

针对通常解析为历史项目的单个字词查询的站点导航将不再发生。相反，浏览器将尝试导航到组织的 Intranet 中可能不存在的内部站点。这将导致出现 404 错误。

热门的单个字词搜索词将需要手动选择搜索建议，才能正确执行搜索。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: GoToIntranetSiteForSingleWordEntryInAddressBar
  - GP 名称: 强制进行直接 Intranet 站点导航而不是在地址栏中对单个词条进行搜索
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: GoToIntranetSiteForSingleWordEntryInAddressBar
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: GoToIntranetSiteForSingleWordEntryInAddressBar
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### HSTSPolicyBypassList
  #### 配置将绕过 HSTS 策略检查的名称列表
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 79

  #### 描述
  此列表中指定的主机名将不接受 HSTS 策略检查，该检查可能会将请求从 "http://" 升级到 "https://"。此策略仅允许使用单一标签主机名。主机名必须规范化。任何 IDN 都必须转换为其 A 标签格式，并且所有 ASCII 字母都必须小写。此策略仅适用于指定的特定主机名；它不适用于列表中名称的子域。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: HSTSPolicyBypassList
  - GP 名称: 配置将绕过 HSTS 策略检查的名称列表
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList\1 = "meet"

```


  #### Mac 信息和设置
  - 首选项密钥名称: HSTSPolicyBypassList
  - 示例值:
``` xml
<array>
  <string>meet</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### HardwareAccelerationModeEnabled
  #### 使用硬件加速(如可用)
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定要使用硬件加速(如果可用)。如果启用或未配置此策略，将启用硬件加速，除非已显式阻止 GPU 功能。

如果禁用此策略，将禁用硬件加速。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: HardwareAccelerationModeEnabled
  - GP 名称: 使用硬件加速(如可用)
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: HardwareAccelerationModeEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: HardwareAccelerationModeEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### HideFirstRunExperience
  #### 隐藏首次运行体验和初始屏幕
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 80

  #### 描述
  如果启用此策略，则当用户第一次运行 Microsoft Edge 时，不会向用户显示首次运行体验和初始屏幕。

对于首次运行体验中显示的配置选项，浏览器将默认使用以下设置:

- 在新标签页上，源类型将设置为“MSN 资讯”，布局将设置为“灵感”。

- 如果 Windows 帐户是 Azure AD 或 MSA 类型，则用户仍将自动登录到 Microsoft Edge。

- 默认情况下不会启用同步，并且用户将可以通过同步设置打开同步。

如果禁用或未配置此策略，则会显示首次运行体验和初始屏幕。

注意: 也可以使用其他特定策略管理首次运行体验中向用户显示的特定配置选项。可以将 HideFirstRunExperience 策略与这些策略结合使用，以在托管设备上配置特定的浏览器体验。其中一些其他策略包括:

-[AutoImportAtFirstRun](#autoimportatfirstrun)

-[NewTabPageLocation](#newtabpagelocation)

-[NewTabPageSetFeedType](#newtabpagesetfeedtype)

-[SyncDisabled](#syncdisabled)

-[BrowserSignin](#browsersignin)

-[NonRemovableProfileEnabled](#nonremovableprofileenabled)

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: HideFirstRunExperience
  - GP 名称: 隐藏首次运行体验和初始屏幕
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: HideFirstRunExperience
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: HideFirstRunExperience
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ImportAutofillFormData
  #### 允许导入自动填充表单数据
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许用户将其他浏览器中的自动填充表单数据导入 Microsoft Edge。

如果启用此策略，则会自动选择用于手动导入自动填充数据的选项。

如果禁用此策略，则首次运行时不会导入自动填充表单数据，并且用户无法手动导入它。

如果未配置此策略，则会在首次运行时导入自动填充数据，并且用户可以选择是否在以后的浏览会话期间手动导入此数据。

你可以将此策略设置为建议。这意味着 Microsoft Edge 会在首次运行时导入自动填充数据，但用户可以在手动导入期间选择或清除**自动填充数据**选项。

**注意**: 此策略目前管理从 Google Chrome (Windows 7、8 和 10 以及 macOS 上)和 Mozilla Firefox (Windows 7、8 和 10 以及 macOS 上)浏览器中的导入。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ImportAutofillFormData
  - GP 名称: 允许导入自动填充表单数据
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: ImportAutofillFormData
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ImportAutofillFormData
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ImportBrowserSettings
  #### 允许导入浏览器设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 78

  #### 描述
  允许用户将其他浏览器中的浏览器设置导入 Microsoft Edge。

如果启用此策略，则**导入浏览器数据**中的**浏览器设置**复选框会自动选中。

如果禁用此策略，则首次运行时不会导入浏览器设置，并且用户无法手动导入它们。

如果未配置此策略，则会在首次运行时导入浏览器设置，并且用户可以选择是否在以后的浏览会话期间手动导入此设置。

你也可以将此策略设置为建议。这意味着 Microsoft Edge 会在首次运行时导入设置，但用户可以在手动导入期间选择或清除**浏览器设置**选项。

**注意**: 此策略目前管理从 Google Chrome (Windows 7、8 和 10 以及 macOS 上)中的导入。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ImportBrowserSettings
  - GP 名称: 允许导入浏览器设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: ImportBrowserSettings
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ImportBrowserSettings
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ImportCookies
  #### 允许导入 Cookie
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 81

  #### 描述
  允许用户将其他浏览器中的 Cookie 导入 Microsoft Edge。

如果禁用此策略，则首次运行时不会导入 Cookie。

如果未配置此策略，则会在首次运行时导入 Cookie。

你也可以将此策略设置为建议。这意味着 Microsoft Edge 会在首次运行时导入 Cookie。

**注意**: 此策略目前管理从 Google Chrome 进行的导入(在 Windows 7、8、10 和 macOS 上)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ImportCookies
  - GP 名称: 允许导入 Cookie
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: ImportCookies
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ImportCookies
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ImportExtensions
  #### 允许导入扩展
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 81

  #### 描述
  允许用户将其他浏览器中的扩展导入 Microsoft Edge。

如果启用此策略，则会在**导入浏览器数据**对话框中自动选中**扩展**复选框。

如果禁用此策略，则首次运行时不会导入扩展，并且用户无法手动导入它们。

如果未配置此策略，则会在首次运行时导入扩展，并且用户可以选择是否在以后的浏览会话期间手动导入它们。

你还可以将此策略设置为建议。这意味着 Microsoft Edge 会在首次运行时导入扩展，但用户可以在手动导入期间选择或清除**收藏夹**选项。

**注意**: 此策略目前仅支持从 Google Chrome 进行导入(在 Windows 7、8、10 和 macOS 上)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ImportExtensions
  - GP 名称: 允许导入扩展
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: ImportExtensions
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ImportExtensions
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ImportFavorites
  #### 允许导入收藏夹
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许用户将其他浏览器中的收藏夹导入 Microsoft Edge。

如果启用此策略，则会在**导入浏览器数据**对话框中自动选中**收藏夹**复选框。

如果禁用此策略，则首次运行时不会导入收藏夹，并且用户无法手动导入收藏夹。

如果未配置此策略，则会在首次运行时导入收藏夹，并且用户可以选择是否在以后的浏览会话期间手动导入它们。

你还可以将此策略设置为建议。这意味着 Microsoft Edge 会在首次运行时导入收藏夹，但用户可以在手动导入期间选择或清除**收藏夹**选项。

**注意**: 此策略目前管理从 Internet Explorer (Windows 7、8 和 10 上)、Google Chrome (Windows 7、8 和 10 以及 macOS 上)、Mozilla Firefox (Windows 7、8 和 10 以及 macOS 上)和 Apple Safari (macOS) 浏览器中的导入。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ImportFavorites
  - GP 名称: 允许导入收藏夹
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: ImportFavorites
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ImportFavorites
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ImportHistory
  #### 允许导入浏览历史记录
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许用户将其他浏览器中的浏览历史记录导入 Microsoft Edge。

如果启用此策略，则会在**导入浏览器数据**对话框中自动选中**浏览历史记录**复选框。

如果禁用此策略，则首次运行时不会导入浏览历史记录数据，并且用户无法手动导入此数据。

如果未配置此策略，则会在首次运行时导入浏览历史记录数据，并且用户可以选择是否在以后的浏览会话期间手动导入它们。

你还可以将此策略设置为建议。这意味着 Microsoft Edge 会在首次运行时导入浏览历史记录，但用户可以在手动导入期间选择或清除**历史记录**选项。

**注意**: 此策略目前管理从 Internet Explorer (Windows 7、8 和 10 上)、Google Chrome (Windows 7、8 和 10 以及 macOS 上)、Mozilla Firefox (Windows 7、8 和 10 以及 macOS 上)和 Apple Safari (macOS) 浏览器中的导入。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ImportHistory
  - GP 名称: 允许导入浏览历史记录
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: ImportHistory
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ImportHistory
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ImportHomepage
  #### 允许导入主页设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许用户将其他浏览器中的主页设置导入 Microsoft Edge。

如果启用此策略，则会自动选择用于手动导入主页设置的选项。

如果禁用此策略，则首次运行时不会导入主页设置，并且用户无法手动导入它。

如果未配置此策略，则会在首次运行时导入主页设置，并且用户可以选择是否在以后的浏览会话期间手动导入此数据。

你可以将此策略设置为建议。这意味着 Microsoft Edge 会在首次运行时导入主页设置，但用户可以在手动导入期间选择或清除**主页**选项。

**注意**: 此策略目前管理从(Windows 7、8 和 10 上) Internet Explorer 中的导入。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ImportHomepage
  - GP 名称: 允许导入主页设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ImportHomepage
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ImportHomepage
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ImportOpenTabs
  #### 允许导入打开的标签页
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 79

  #### 描述
  允许用户将其他浏览器中打开和固定的标签页导入 Microsoft Edge。

如果启用此策略，则会在**导入浏览器数据**对话框中自动选中**打开的标签页**复选框。

如果禁用此策略，则首次运行时不会导入打开的标签页，并且用户无法手动导入它们。

如果未配置此策略，则会在首次运行时导入打开的标签页，并且用户可以选择是否在以后的浏览会话期间手动导入它们。

你还可以将此策略设置为建议。这意味着 Microsoft Edge 会在首次运行时导入打开的标签页，但用户可以在手动导入期间选择或清除**打开的标签页**选项。

**注意**: 此策略目前仅支持从(Windows 7、8、10 和 macOS 上) Google Chrome 中的导入。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ImportOpenTabs
  - GP 名称: 允许导入打开的标签页
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: ImportOpenTabs
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ImportOpenTabs
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ImportPaymentInfo
  #### 允许导入付款信息
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许用户将其他浏览器中的付款信息导入 Microsoft Edge。

如果启用此策略，则会在**导入浏览器数据**对话框中自动选中**付款信息**复选框。

如果禁用此策略，则首次运行时不会导入付款信息，并且用户无法手动导入它。

如果未配置此策略，则会在首次运行时导入付款信息，并且用户可以选择是否在以后的浏览会话期间手动导入此信息。

你还可以将此策略设置为建议。这意味着 Microsoft Edge 会在首次运行时导入付款信息，但用户可以在手动导入期间选择或清除**付款信息**选项。

**注意**: 此策略目前管理从 Google Chrome (Windows 7、8 、10 和 macOS 上)中的导入。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ImportPaymentInfo
  - GP 名称: 允许导入付款信息
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: ImportPaymentInfo
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ImportPaymentInfo
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ImportSavedPasswords
  #### 允许导入保存的密码
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许用户将其他浏览器中保存的密码导入 Microsoft Edge。

如果启用此策略，则会自动选择用于手动导入已保存密码的选项。

如果禁用此策略，则首次运行时不会导入保存的密码，并且用户无法手动导入它们。

如果未配置此策略，则会在首次运行时导入密码，并且用户可以选择是否在以后的浏览会话期间手动导入它们。

你可以将此策略设置为建议。这意味着 Microsoft Edge 会在首次运行时导入密码，但用户可以在手动导入期间选择或清除**密码**选项。

**注意**: 此策略目前管理从 Internet Explorer (Windows 7、8 和 10 上)、Google Chrome (Windows 7、8 和 10 以及 macOS 上)和 Mozilla Firefox (Windows 7、8 和 10 以及 macOS 上)浏览器中的导入。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ImportSavedPasswords
  - GP 名称: 允许导入保存的密码
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: ImportSavedPasswords
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ImportSavedPasswords
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ImportSearchEngine
  #### 允许导入搜索引擎设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许用户将其他浏览器中的搜索引擎设置导入 Microsoft Edge。

如果启用此策略，则会自动选择用于导入搜索引擎设置的选项。

如果禁用此策略，则首次运行时不会导入搜索引擎设置，并且用户无法手动导入它们。

如果未配置此策略，则会在首次运行时导入搜索引擎设置，并且用户可以选择是否在以后的浏览会话期间手动导入此数据。

你可以将此策略设置为建议。这意味着 Microsoft Edge 会在首次运行时导入搜索引擎设置，但用户可以在手动导入期间选择或清除**搜索引擎**选项。

**注意**: 此策略目前管理从 Internet Explorer (Windows 7、8 和 10 上)中的导入。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ImportSearchEngine
  - GP 名称: 允许导入搜索引擎设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: ImportSearchEngine
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ImportSearchEngine
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ImportShortcuts
  #### 允许导入快捷方式
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 81

  #### 描述
  允许用户从另一个浏览器将快捷方式导入到Microsoft Edge 中。

如果禁用此策略，则不会在首次运行时导入快捷方式。

如果未配置此策略，则在首次运行时会导入快捷方式。

也可以将此策略设置为建议。这意味着 Microsoft Edge 在首次运行时会导入快捷方式。

**注意**: 此策略当前管理从 Google Chrome 进行的导入(在 Windows 7、8 和 10 以及 macOS 上)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ImportShortcuts
  - GP 名称: 允许导入快捷方式
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: ImportShortcuts
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ImportShortcuts
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### InPrivateModeAvailability
  #### 配置 InPrivate 模式可用性
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定用户是否可以在 Microsoft Edge 中以 InPrivate 模式打开页面。

如果未配置此策略或将其设置为“Enabled”，则用户可以在 InPrivate 模式下打开页面。

将此策略设置为“Disabled”可以阻止用户使用 InPrivate 模式。

将此策略设置为“Forced”可以始终使用 InPrivate 模式。

策略选项映射：

* Enabled (0) = InPrivate 模式可用

* Disabled (1) = InPrivate 模式已禁用

* Forced (2) = 强制的 InPrivate 模式

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: InPrivateModeAvailability
  - GP 名称: 配置 InPrivate 模式可用性
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: InPrivateModeAvailability
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: InPrivateModeAvailability
  - 示例值:
``` xml
<integer>1</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### InsecureFormsWarningsEnabled
  #### 为不安全的表单启用警告
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  此策略控制对浏览器中安全(HTTPS)网站内嵌入的不安全表单(通过 HTTP 提交的表单)的处理。
如果启用或未设置此策略，则在提交不安全的表单时将显示完整页面警告。此外，当表单字段处于焦点时，它们旁边将显示一个警告气泡，并且将对这些表单禁用自动填充。
如果禁用此策略，则不会对不安全的表单显示警告，并且自动填充将正常工作。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: InsecureFormsWarningsEnabled
  - GP 名称: 为不安全的表单启用警告
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: InsecureFormsWarningsEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: InsecureFormsWarningsEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### IntensiveWakeUpThrottlingEnabled
  #### 控制 IntensiveWakeUpThrottling 功能
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 85

  #### 描述
  启用后，IntensiveWakeUpThrottling 功能会导致后台选项卡中的 Javascript 计时器受到严重限制和合并，当页面在后台 5 分钟或更长时间后，计时器每分钟运行不超过一次。

这是一个符合 Web 标准的功能，但可能会导致某些网站上的功能中断，最长可延迟一分钟。但是，启用后可显著节省 CPU 和电池开销。有关更多详细信息，请参阅 https://bit.ly/30b1XR4。

如果启用此策略，则将强制启用该功能，用户将无法覆盖此设置。
如果禁用此策略，则将强制禁用该功能。用户将无法覆盖此设置。
如果未配置此策略，则该功能将由其自身的内部逻辑控制。用户可以手动配置此设置。

请注意，策略是按呈现器进程应用的，策略设置的最新值将在呈现器进程启动时有效。需要完全重新启动，以确保所有加载的选项卡都收到一致的策略设置。使用此策略的不同值运行进程没有什么害处。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: IntensiveWakeUpThrottlingEnabled
  - GP 名称: 控制 IntensiveWakeUpThrottling 功能
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: IntensiveWakeUpThrottlingEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: IntensiveWakeUpThrottlingEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### InternetExplorerIntegrationEnhancedHangDetection
  #### 为 Internet Explorer 模式配置增强型挂起检测
  
  
  #### 支持的版本:
  - 在 Windows 自 84 或之后

  #### 描述
  增强型挂起检测可在 Internet Explorer 模式下检测挂起的网页，这种检测方法比独立 Internet Explorer 使用的方法更精细。检测到挂起的网页时，浏览器将应用缓解措施，防止浏览器的其余部分挂起。

通过此设置，可以配置使用增强型挂起检测，以防遇到任何网站的不兼容问题。建议仅在 Internet Explorer 模式下看到“(网站)未响应”之类的通知时，才禁用此策略，而不要在独立 Internet Explorer 中禁用。

此设置可与以下各项结合使用:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) 设置为“IEMode”
以及
列表中至少有一个条目的 [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) 策略。

如果将此策略设置为“Enabled”或不对其进行配置，则在 Internet Explorer 模式下运行的网站将使用增强型挂起检测。

如果将此策略设置为“Disabled”，则将禁用增强型挂起检测，因此用户将获得基本 Internet Explorer 挂起检测行为。

若要了解有关 Internet Explorer 模式的详细信息，请参阅 [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

策略选项映射：

* Disabled (0) = 已禁用增强型挂起检测

* Enabled (1) = 已启用增强型挂起检测

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: InternetExplorerIntegrationEnhancedHangDetection
  - GP 名称: 为 Internet Explorer 模式配置增强型挂起检测
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: InternetExplorerIntegrationEnhancedHangDetection
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  

  [返回顶部](#microsoft-edge---策略)

  ### InternetExplorerIntegrationLevel
  #### 配置 Internet Explorer 集成
  
  
  #### 支持的版本:
  - 在 Windows 自 77 或之后

  #### 描述
  有关为 Internet Explorer 模式配置最佳体验的指南，请参阅 [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

策略选项映射：

* None (0) = 无

* IEMode (1) = Internet Explorer 模式

* NeedIE (2) = Internet Explorer 11

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: InternetExplorerIntegrationLevel
  - GP 名称: 配置 Internet Explorer 集成
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: InternetExplorerIntegrationLevel
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  

  [返回顶部](#microsoft-edge---策略)

  ### InternetExplorerIntegrationSiteList
  #### 配置企业模式站点列表
  
  
  #### 支持的版本:
  - 在 Windows 自 78 或之后

  #### 描述
  有关为 Internet Explorer 模式配置最佳体验的指南，请参阅 [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: InternetExplorerIntegrationSiteList
  - GP 名称: 配置企业模式站点列表
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: InternetExplorerIntegrationSiteList
  - 值类型: REG_SZ
  ##### 示例值:
```
"https://internal.contoso.com/sitelist.xml"
```


  

  [返回顶部](#microsoft-edge---策略)

  ### InternetExplorerIntegrationSiteRedirect
  #### 指定从 Internet Explorer 模式页面启动时，到未配置站点的“页面内”导航的行为方式
  
  
  #### 支持的版本:
  - 在 Windows 自 81 或之后

  #### 描述
  从当前页面上的链接、脚本或表单中启动“页面内”导航。它也可以是上次“页面内”导航尝试的服务器端重定向。反过来，用户可以使用多种浏览器控件来启动独立于当前页面的非“页面内”导航，例如地址栏、“后退”按钮或收藏夹链接。

通过此设置，你可以指定从以 Internet Explorer 模式加载的页面导航到未配置站点(即未在企业模式站点列表中配置的站点)时是切换回 Microsoft Edge 还是保持 Internet Explorer 模式。

此设置可与以下各项结合使用:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) 设置为“IEMode”
以及
列表中至少有一个条目的 [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) 策略。

如果禁用或未配置此策略，则只有配置为以 Internet Explorer 模式打开的站点才会在该模式下打开。任何未配置为以 Internet Explorer 模式打开的站点都将重定向回 Microsoft Edge。

如果将此策略设置为“Default”，则只有配置为以 Internet Explorer 模式打开的站点才会在该模式下打开。任何未配置为以 Internet Explorer 模式打开的站点都将重定向回 Microsoft Edge。

如果将此策略设置为“AutomaticNavigationsOnly”，则会获得默认体验，只不过所有到未配置站点的自动导航(如 302 重定向)都将保持 Internet Explorer 模式。

如果将此策略设置为“AllInPageNavigations”，则所有从以 IE 模式加载的页面到未配置站点的导航都将保持 Internet Explorer 模式(最不推荐)。

要了解有关 Internet Explorer 模式的详细信息，请访问 [https://go.microsoft.com/fwlink/?linkid=2105106](https://go.microsoft.com/fwlink/?linkid=2105106)

策略选项映射：

* Default (0) = 默认值

* AutomaticNavigationsOnly (1) = 仅在 Internet Explorer 模式下保留自动导航

* AllInPageNavigations (2) = 在 Internet Explorer 模式下保留所有“页面内”导航

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: InternetExplorerIntegrationSiteRedirect
  - GP 名称: 指定从 Internet Explorer 模式页面启动时，到未配置站点的“页面内”导航的行为方式
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: InternetExplorerIntegrationSiteRedirect
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  

  [返回顶部](#microsoft-edge---策略)

  ### InternetExplorerIntegrationTestingAllowed
  #### 允许 Internet Explorer 模式测试
  
  
  #### 支持的版本:
  - 在 Windows 自 86 或之后

  #### 描述
  此策略取代了 ie-mode-test 标志策略。它使用户可以从 UI 菜单选项中打开 IE 模式选项卡。

此设置与以下各项结合使用
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) 设置为“IEMode”
和
[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) 策略，其中列表至少包含一个条目。

如果启用此策略，则用户可以从 UI 选项打开 IE 模式选项卡，然后将当前网站导航到 IE 模式网站。

如果禁用此策略，用户将无法直接在菜单中看到 UI 选项。

如果未配置此策略，则可以手动设置 ie-mode-test 标志。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: InternetExplorerIntegrationTestingAllowed
  - GP 名称: 允许 Internet Explorer 模式测试
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: InternetExplorerIntegrationTestingAllowed
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  

  [返回顶部](#microsoft-edge---策略)

  ### IsolateOrigins
  #### 对特定来源启用站点隔离
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定要在自身进程中隔离运行的来源。
该策略还隔离由子域命名的来源 - 例如，指定 https://contoso.com/ 将导致 https://foo.contoso.com/ 作为 https://contoso.com/ 站点的一部分被隔离。
如果启用此策略，每个以逗号分隔的列表中指定的来源将在其自身进程中运行。
如果禁用此策略，将同时禁用 [IsolateOrigins](#isolateorigins) 和 [SitePerProcess](#siteperprocess) 功能。用户仍然可以通过命令行标志手动启用 [IsolateOrigins](#isolateorigins) 策略。
如果未配置此策略，则用户可以更改此设置。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: IsolateOrigins
  - GP 名称: 对特定来源启用站点隔离
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: IsolateOrigins
  - 值类型: REG_SZ
  ##### 示例值:
```
"https://contoso.com/,https://fabrikam.com/"
```


  #### Mac 信息和设置
  - 首选项密钥名称: IsolateOrigins
  - 示例值:
``` xml
<string>https://contoso.com/,https://fabrikam.com/</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### LocalProvidersEnabled
  #### 允许来自本地提供商的建议
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 83

  #### 描述
  允许在 Microsoft Edge 地址栏和自动建议列表中的设备上提供建议，如收藏夹和浏览历史记录。

     如果启用此策略，将使用来自本地提供商的建议。

如果禁用此策略，则从不使用来自本地提供商的建议。本地历史记录和本地收藏夹建议将不会显示。

     如果未配置此策略，则允许本地提供商提出建议，用户可以使用“设置”切换进行更改。

     请注意，如果已应用禁用此功能的策略，则某些功能可能不可用。例如，如果启用 [SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled) 策略，浏览历史记录建议将不可用。

     此策略需要浏览器重新启动才能完成应用。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: LocalProvidersEnabled
  - GP 名称: 允许来自本地提供商的建议
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: LocalProvidersEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: LocalProvidersEnabled
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ManagedFavorites
  #### 配置收藏夹
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  配置托管收藏夹列表。

此策略会创建收藏夹列表。每个收藏夹都包含 "name"和 "url" 关键值，这些关键值表示收藏夹的名称和目标地址。你可以通过定义不带 "url" 关键值但带有附加 "children" 关键值的收藏夹来配置子文件夹，此 "children" 关键值包含上面定义的收藏夹列表(其中一些可能还是文件夹)。Microsoft Edge 会修改不完整的 URL，就好像它们是通过地址栏提交的一样，例如 "microsoft.com" 会变为 "https://microsoft.com/"。

这些收藏夹放在用户无法修改的文件夹中(但用户可以选择在收藏夹栏中将其隐藏)。默认情况下，文件夹名称为“托管收藏夹”，但是，通过向收藏夹列表添加一个包含 "toplevel_name" 关键值并且以所需文件夹名称为值的词典，你可以更改此名称。

托管收藏夹未同步到用户帐户，无法通过扩展进行修改。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字典

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ManagedFavorites
  - GP 名称: 配置收藏夹
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ManagedFavorites
  - 值类型: REG_SZ
  ##### 示例值:
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


  #### Mac 信息和设置
  - 首选项密钥名称: ManagedFavorites
  - 示例值:
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
  

  [返回顶部](#microsoft-edge---策略)

  ### ManagedSearchEngines
  #### 管理搜索引擎
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许你配置一个可列出最多 10 个搜索引擎的列表，其中一个搜索引擎必须标记为默认搜索引擎。
不需要指定编码。从 Microsoft Edge 80 开始，suggest_url 和 image_search_url 参数是可选参数。从 Microsoft Edge 80 开始，可以使用可选参数 image_search_post_params (包含以逗号分隔的名称/值对)。

从 Microsoft Edge 83 开始，你可以使用 allow_search_engine_discovery 可选参数启用搜索引擎发现。此参数必须是列表中的第一项。如果未指定 allow_search_engine_discovery，则默认情况下禁用搜索引擎发现。从 Microsoft Edge 84 开始，你可以将此策略设置为推荐策略，以允许搜索提供程序发现。无需添加 allow_search_engine_discovery 可选参数。

如果启用此策略，用户将无法在列表中添加、删除或更改任何搜索引擎。用户可以将其默认搜索引擎设置为列表中的任何搜索引擎。

如果禁用或未配置此策略，则用户可以根据需要修改搜索引擎列表。

如果设置了 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 策略，则将忽略此策略 (ManagedSearchEngines)。用户必须重启浏览器才能完成应用此策略。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字典

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ManagedSearchEngines
  - GP 名称: 管理搜索引擎
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: ManagedSearchEngines
  - 值类型: REG_SZ
  ##### 示例值:
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


  #### Mac 信息和设置
  - 首选项密钥名称: ManagedSearchEngines
  - 示例值:
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
  

  [返回顶部](#microsoft-edge---策略)

  ### MaxConnectionsPerProxy
  #### 到代理服务器的最大并发连接数
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定与代理服务器的最大同时连接数。

有些代理服务器不能处理每个客户端的大量并发连接，你可以通过将此策略设置为较低的值来解决这个问题。

此策略的值应小于 100 并大于 6。默认值为 32。

已知一些网络应用程序会消耗很多挂起的 GET 的连接，如果这类 Web 应用打开太多，将最大连接降低到 32 以下可能会导致浏览器网络挂起。

如果未配置此策略，将使用默认值(32)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: MaxConnectionsPerProxy
  - GP 名称: 到代理服务器的最大并发连接数
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: MaxConnectionsPerProxy
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000020
```


  #### Mac 信息和设置
  - 首选项密钥名称: MaxConnectionsPerProxy
  - 示例值:
``` xml
<integer>32</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### MediaRouterCastAllowAllIPs
  #### 允许 Google Cast 连接到所有 IP 地址上的强制转换设备
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  启用此策略可让 Google Cast 连接到所有 IP 地址上的强制转换设备，而不仅仅是 RFC1918/RFC4193 专用地址。

禁用此策略以限制 Google Cast 连接到 RFC1918/RFC4193 专用地址上的强制转换设备。

如果未配置此策略，则 Google Cast 仅会连接到 RFC1918/RFC4193 专用地址上的强制转换设备，除非你启用 CastAllowAllIPs 功能。

如果禁用了 [EnableMediaRouter](#enablemediarouter) 策略，则此策略不起作用。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: MediaRouterCastAllowAllIPs
  - GP 名称: 允许 Google Cast 连接到所有 IP 地址上的强制转换设备
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: MediaRouterCastAllowAllIPs
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: MediaRouterCastAllowAllIPs
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### MetricsReportingEnabled
  #### 启用使用情况和崩溃相关的数据报告 (已弃用)
  >已弃用: 此策略已弃用。目前仍受支持，但将在未来版本中弃用。
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  此策略已被弃用。它目前受支持，但在 Microsoft Edge 89 中将不再使用。对于 Windows 7、Windows 8 和 macOS，此策略将替换为新策略: [DiagnosticData](#diagnosticdata)。在 Win 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569))上，此策略将替换为“允许遥测”。

通过此策略，可向 Microsoft 报告与 Microsoft Edge 的使用情况和故障相关的数据。

启用此策略可将与使用情况和故障相关的数据发送给 Microsoft。禁用此策略则不会将数据发送给 Microsoft。在这两种情况下，用户都不能更改或替代设置。

对于 Windows 10，如果未配置此策略，Microsoft Edge 将默认为 Windows 诊断数据设置。如果启用此策略，Microsoft Edge 将仅在“Windows 诊断数据设置”设置为“增强”或“全部”时发送使用情况数据。如果禁用此策略，Microsoft Edge 将不会发送使用情况数据，而是根据 Windows 诊断数据设置发送故障相关数据。访问 [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)，了解有关 Windows 诊断数据设置的详细信息

对于 Windows 7、8 和 macOS，此策略控制使用情况和故障相关数据的发送。如果未配置此策略，Microsoft Edge 将默认为用户的首选项。

若要启用此策略，必须将 [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) 设置为“已启用”，如果未配置或已禁用 [MetricsReportingEnabled](#metricsreportingenabled) 或 [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)，则系统不会将此数据发送给 Microsoft。

此策略仅适用于已加入 Microsoft Active Directory 域的 Windows 实例、为设备管理注册的 Windows 10 专业版或企业版实例，或通过 MDM 管理或通过 MCX 加入域的 macOS 实例。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: MetricsReportingEnabled
  - GP 名称: 启用使用情况和崩溃相关的数据报告 (已弃用)
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: MetricsReportingEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: MetricsReportingEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### NativeWindowOcclusionEnabled
  #### 启用本机窗口封闭
  
  
  #### 支持的版本:
  - 在 Windows 自 84 或之后

  #### 描述
  在 Microsoft Edge 中启用本机窗口封闭。

如果启用此设置，为减少 CPU 和功耗，Microsoft Edge 将检测窗口何时被其他窗口覆盖，并且将暂停工作绘制像素。

如果禁用此设置，Microsoft Edge 将不会检测窗口何时被其他窗口覆盖。

如果未设置此策略，则将启用窗口隐藏检测。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: NativeWindowOcclusionEnabled
  - GP 名称: 启用本机窗口封闭
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: NativeWindowOcclusionEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  

  [返回顶部](#microsoft-edge---策略)

  ### NavigationDelayForInitialSiteListDownloadTimeout
  #### 为企业模式站点列表的选项卡导航设置延迟超时
  
  
  #### 支持的版本:
  - 在 Windows 自 84 或之后

  #### 描述
  允许你以秒为单位设置一个超时值，以便 Microsoft Edge 选项卡等待导航，直到浏览器下载了初始企业模式站点列表。

此设置可与以下各项结合使用:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) 设置为“IEMode”
以及
列表中至少有一个条目的 [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) 策略
以及
[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload) 设置为“所有符合条件的导航”(1)。

选项卡等待企业模式站点列表下载的时间不会超过此超时值。如果超时过期后浏览器尚未完成下载企业模式站点列表，则 Microsoft Edge 选项卡仍将继续导航。超时值不应大于 20 秒且不应少于 1 秒。

如果将此策略中的超时设置为大于默认值 2 秒的值，则 2 秒后将向用户显示一个信息栏。该信息栏包含一个按钮，允许用户退出等待企业模式站点列表下载完成。

如果未配置此策略，则使用默认超时 2 秒。此默认值将来可能会更改。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: NavigationDelayForInitialSiteListDownloadTimeout
  - GP 名称: 为企业模式站点列表的选项卡导航设置延迟超时
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: NavigationDelayForInitialSiteListDownloadTimeout
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x0000000a
```


  

  [返回顶部](#microsoft-edge---策略)

  ### NetworkPredictionOptions
  #### 启用网络预测
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  启用网络预测，并阻止用户更改此设置。

此策略控制 DNS 预取、TCP 和 SSL 预连接及网页的预呈现。

如果未配置此策略，则启用网络预测，但用户可以更改此项设置。

策略选项映射：

* NetworkPredictionAlways (0) = 预测任何网络连接上的网络操作

* NetworkPredictionWifiOnly (1) = 不支持，如果使用此值，它将被视为已设置“预测任何网络连接上的网络操作”(0)

* NetworkPredictionNever (2) = 不要对任何网络连接预测网络操作

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: NetworkPredictionOptions
  - GP 名称: 启用网络预测
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: NetworkPredictionOptions
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: NetworkPredictionOptions
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### NonRemovableProfileEnabled
  #### 配置用户是否始终具有使用其工作或学校帐户自动登录的默认用户配置
  
  
  #### 支持的版本:
  - 在 Windows 自 78 或之后

  #### 描述
  此策略确定用户是否可以删除通过用户工作或学校帐户自动登录的 Microsoft Edge 用户配置。

如果启用此策略，则将使用用户的工作或学校帐户在 Windows 上创建不可删除的用户配置。此用户配置无法注销或删除。

如果禁用或未配置此策略，则用户可以注销或删除 Windows 中通过用户的工作或学校帐户自动登录的用户配置。

如果要配置浏览器登录，请使用 [BrowserSignin](#browsersignin) 策略。

     此策略仅适用于已加入 Microsoft Active Directory 域的 Windows 实例、为设备管理注册的 Windows 10 专业版(或企业版)实例，

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: NonRemovableProfileEnabled
  - GP 名称: 配置用户是否始终具有使用其工作或学校帐户自动登录的默认用户配置
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: NonRemovableProfileEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  

  [返回顶部](#microsoft-edge---策略)

  ### OverrideSecurityRestrictionsOnInsecureOrigin
  #### 控制针对不安全源的安全限制的适用范围
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定来源(URL)或主机名模式(如 "*.contoso.com")的列表，对于这些模式，针对不安全来源的安全限制不适用。

此策略让你可以针对无法部署 TLS 或为内部 Web 开发设置暂存服务器的旧版应用程序指定允许的来源，以便开发人员可以测试需要安全上下文的功能，而不必在暂存服务器上部署 TLS。此策略还可防止来源在多功能地址栏中被标记为“不安全”。

在此策略中设置 URL 列表的效果与将命令行标志 "--unsafely-treat-insecure-origin-as-secure" 设置为相同 URL 的逗号分隔列表的效果相同。如果启用此策略，它将覆盖命令行标志。

有关安全上下文的详细信息，请参阅 https://www.w3.org/TR/secure-contexts/。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: OverrideSecurityRestrictionsOnInsecureOrigin
  - GP 名称: 控制针对不安全源的安全限制的适用范围
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\1 = "http://testserver.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\2 = "*.contoso.com"

```


  #### Mac 信息和设置
  - 首选项密钥名称: OverrideSecurityRestrictionsOnInsecureOrigin
  - 示例值:
``` xml
<array>
  <string>http://testserver.contoso.com/</string>
  <string>*.contoso.com</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### PaymentMethodQueryEnabled
  #### 允许网站查询可用的付款方式
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 80

  #### 描述
  允许你设置网站能否检查用户是否已保存付款方式。

如果禁用此策略，则使用 PaymentRequest.canMakePayment 或 PaymentRequest.hasEnrolledInstrument API 的网站将收到没有可用支付方式的通知。

如果启用此策略或未设置此策略，则网站可以检查用户是否保存了付款方式。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PaymentMethodQueryEnabled
  - GP 名称: 允许网站查询可用的付款方式
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: PaymentMethodQueryEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: PaymentMethodQueryEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### PersonalizationReportingEnabled
  #### 允许向 Microsoft 发送浏览历史记录以对广告、搜索和新闻进行个性化设置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 80

  #### 描述
  此策略阻止 Microsoft 收集用户的 Microsoft Edge 浏览历史记录以用于提供个性化广告、搜索、新闻和其他 Microsoft 服务。

此设置仅适用于具有 Microsoft 帐户的用户。此设置不适用于子帐户或企业帐户。

如果禁用此策略，则用户无法更改或替代此设置。如果启用或未配置此策略，则 Microsoft Edge 将默认使用用户的首选项。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PersonalizationReportingEnabled
  - GP 名称: 允许向 Microsoft 发送浏览历史记录以对广告、搜索和新闻进行个性化设置
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: PersonalizationReportingEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: PersonalizationReportingEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### PinningWizardAllowed
  #### 允许使用“固定到任务栏”向导
  
  
  #### 支持的版本:
  - 在 Windows 自 80 或之后

  #### 描述
  Microsoft Edge 使用“固定到任务栏”向导来帮助用户将建议的站点固定到任务栏。默认情况下，“固定到任务栏”向导功能处于启用状态，用户可以通过“设置及更多”菜单使用此功能。

如果启用或未配置此策略，则用户可以从“设置及更多”菜单中调用“固定到任务栏”向导。也可以通过协议启动来调用该向导。

如果禁用此策略，则“固定到任务栏”向导在菜单中被禁用，并且无法通过协议启动来调用。

用于启用或禁用“固定到任务栏”向导的用户设置不可用。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PinningWizardAllowed
  - GP 名称: 允许使用“固定到任务栏”向导
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: PinningWizardAllowed
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  

  [返回顶部](#microsoft-edge---策略)

  ### ProactiveAuthEnabled
  #### 启用主动身份验证
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许你配置是否开启主动身份验证。

如果启用此策略，Microsoft Edge 会尝试使用 Microsoft 服务主动验证登录用户的身份。Microsoft Edge 将定期通过联机服务检查更新的清单，该清单包含管理如何执行此操作的配置。

如果禁用此策略，则 Microsoft Edge 不会尝试使用 Microsoft 服务对已登录用户进行主动身份验证。Microsoft Edge 不再通过联机服务检查更新的清单，该清单包含用于执行此操作的配置。

如果未配置此策略，则会开启主动身份验证。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ProactiveAuthEnabled
  - GP 名称: 启用主动身份验证
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ProactiveAuthEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ProactiveAuthEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### PromotionalTabsEnabled
  #### 启用完整标签页促销内容
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  控制完整标签页的宣传内容或教育内容的呈现。此设置控制欢迎页面的呈现，以帮助用户登录 Microsoft Edge、选择其默认浏览器或了解产品功能。

如果启用此策略(将其设置为 true)或未对其进行配置，则 Microsoft Edge 可能会向用户显示完整标签页内容以提供产品信息。

如果禁用(设置为 false)此策略，则 Microsoft Edge 无法向用户显示完整标签页内容。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PromotionalTabsEnabled
  - GP 名称: 启用完整标签页促销内容
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: PromotionalTabsEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: PromotionalTabsEnabled
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### PromptForDownloadLocation
  #### 询问所下载文件的保存位置
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  设置下载文件前是否询问文件保存位置。

如果启用此策略，系统将在下载前询问用户每个文件的保存位置；如果不进行配置，文件会自动保存到默认位置，而不会询问用户。

如果未配置此策略，用户将能够更改此设置。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: PromptForDownloadLocation
  - GP 名称: 询问所下载文件的保存位置
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: PromptForDownloadLocation
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: PromptForDownloadLocation
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### QuicAllowed
  #### 允许 QUIC 协议
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许在 Microsoft Edge 中使用 QUIC 协议。

如果启用此策略或未配置此策略，则允许使用 QUIC 协议。

如果禁用此策略，则会阻止 QUIC 协议。

QUIC 是一种传输层网络协议，可以提高当前使用 TCP 的 Web 应用程序的性能。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: QuicAllowed
  - GP 名称: 允许 QUIC 协议
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: QuicAllowed
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: QuicAllowed
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### RelaunchNotification
  #### 通知用户推荐或需要对挂起的更新重启浏览器
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  通知用户需要重启 Microsoft Edge 以应用待处理的更新。

如果未配置此策略，Microsoft Edge 会在顶部菜单栏的最右侧添加一个回收站图标，提示用户重启浏览器以应用更新。

如果启用此策略并将其设置为“Recommended”，则定期警告会提示用户系统建议重启。用户可以消除此警告并推迟重启。

如果将该策略设置为“Required”，则定期警告会提示用户: 当通知期过后，浏览器将立即自动重启。默认期限为七天。你可以使用 [RelaunchNotificationPeriod](#relaunchnotificationperiod) 策略配置此期限。

当浏览器重启时，将还原用户的会话。

策略选项映射：

* Recommended (1) = 推荐 - 向用户显示重复提示，指示建议重启

* Required (2) = 需要 - 向用户显示重复提示，指示需要重启

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: RelaunchNotification
  - GP 名称: 通知用户推荐或需要对挂起的更新重启浏览器
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: RelaunchNotification
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: RelaunchNotification
  - 示例值:
``` xml
<integer>1</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### RelaunchNotificationPeriod
  #### 设置更新通知的时间段
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许设置时间段（以毫秒为单位），在该时间段内，将通知用户必须重新启动Microsoft Edge才能应用挂起的更新。

在此时间段内，将反复通知用户需要更新。在 Microsoft Edge 中，应用程序菜单更改，以指示通知时间过去三分之一后，需要重新启动。通知时间过去三分之二后，此通知将更改颜色，而整个通知时间结束后再次更改。[RelaunchNotification](#relaunchnotification) 策略所启用的附加通知采用此相同的计划。

如果未设置，则使用默认时间段 604800000 毫秒（一周）。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: RelaunchNotificationPeriod
  - GP 名称: 设置更新通知的时间段
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: RelaunchNotificationPeriod
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x240c8400
```


  #### Mac 信息和设置
  - 首选项密钥名称: RelaunchNotificationPeriod
  - 示例值:
``` xml
<integer>604800000</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### RendererCodeIntegrityEnabled
  #### 启用呈现器代码完整性
  
  
  #### 支持的版本:
  - 在 Windows 自 78 或之后

  #### 描述
  如果启用或未设置此策略，则会启用呈现器代码完整性。仅当必须在 Microsoft Edge 的呈现器进程中运行的第三方软件存在兼容性问题时，才应禁用此策略。

禁用此策略对 Microsoft Edge 的安全和稳定性有不利影响，因为 Microsoft Edge 的呈现器进程内部可能因此允许加载未知和可能有害的代码。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: RendererCodeIntegrityEnabled
  - GP 名称: 启用呈现器代码完整性
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: RendererCodeIntegrityEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  

  [返回顶部](#microsoft-edge---策略)

  ### RequireOnlineRevocationChecksForLocalAnchors
  #### 指定本地信任密钥是否需要联机 OCSP/CRL 检查
  
  
  #### 支持的版本:
  - 在 Windows 自 77 或之后

  #### 描述
  控制是否需要进行在线吊销检查(OCSP/CRL 检查)。如果 Microsoft Edge 无法获取吊销状态信息，则会将这些证书视为已吊销(“硬故障”)。

如果启用此策略，则 Microsoft Edge 始终对成功验证并由本地安装的 CA 证书签名的服务器证书执行吊销检查。

如果未配置或禁用此策略，则 Microsoft Edge 将使用现有的在线吊销检查设置。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: RequireOnlineRevocationChecksForLocalAnchors
  - GP 名称: 指定本地信任密钥是否需要联机 OCSP/CRL 检查
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: RequireOnlineRevocationChecksForLocalAnchors
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  

  [返回顶部](#microsoft-edge---策略)

  ### ResolveNavigationErrorsUseWebService
  #### 启用使用 Web 服务解决导航错误
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许 Microsoft Edge 发布到 Web 服务的无数据连接，以便在旅馆和机场 WLAN 等情况下探测网络的连接性。

如果启用此策略，则使用 Web 服务进行网络连接测试。

如果禁用此策略，则 Microsoft Edge 使用本机 API 尝试解决网络连接和导航问题。

**注意**: 除在 Windows 8 和更高版本的 Windows 上外，Microsoft Edge *始终*使用本机 API 解决连接问题。

如果未配置此策略，则 Microsoft Edge 会采用位于 edge://settings/privacy 的“服务”下设置的用户首选项。
具体来说，用户可以打开或关闭名为**使用 Web 服务帮助解决导航错误**的切换开关。请注意，如果已启用此策略(ResolveNavigationErrorsUseWebService)，则**使用 Web 服务帮助解决导航错误**设置处于开启状态，但用户无法使用该切换开关来更改此设置。如果已禁用此策略，则**使用 Web 服务帮助解决导航错误**设置处于关闭状态，用户无法使用该切换开关更改此设置。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ResolveNavigationErrorsUseWebService
  - GP 名称: 启用使用 Web 服务解决导航错误
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: ResolveNavigationErrorsUseWebService
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: ResolveNavigationErrorsUseWebService
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### RestrictSigninToPattern
  #### 限制哪些帐户可用作 Microsoft Edge 主帐户
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  确定可以在 Microsoft Edge 中将哪些帐户设置为浏览器主帐户(在同步选择加入流程中选择的帐户)。

如果用户尝试使用与此模式不匹配的用户名配置浏览器主帐户，则他们将被阻止，并会收到相应的错误消息。你可以使用该模式的 Perl 样式正则表达式将此策略配置为匹配多个帐户。请注意，模式匹配区分大小写。有关所使用的正则表达式规则的详细信息，请参阅 https://go.microsoft.com/fwlink/p/?linkid=2133903。

如果未配置此策略或将其留空，则用户可以在 Microsoft Edge 中将任何帐户设置为浏览器主帐户。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: RestrictSigninToPattern
  - GP 名称: 限制哪些帐户可用作 Microsoft Edge 主帐户
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: RestrictSigninToPattern
  - 值类型: REG_SZ
  ##### 示例值:
```
".*@contoso.com"
```


  #### Mac 信息和设置
  - 首选项密钥名称: RestrictSigninToPattern
  - 示例值:
``` xml
<string>.*@contoso.com</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### RoamingProfileLocation
  #### 设置漫游用户配置目录
  
  
  #### 支持的版本:
  - 在 Windows 自 85 或之后

  #### 描述
  配置用于存储用户配置漫游副本的目录。

如果启用此策略，那么只要你还启用了 [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) 策略，Microsoft Edge 就会使用提供的目录存储用户配置的漫游副本。如果禁用 [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) 策略或未对其进行配置，则不会使用此策略中存储的值。

请参阅 [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) 以获取可以使用的变量列表。

如果未配置此策略，则使用默认漫游用户配置路径。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: RoamingProfileLocation
  - GP 名称: 设置漫游用户配置目录
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: RoamingProfileLocation
  - 值类型: REG_SZ
  ##### 示例值:
```
"${roaming_app_data}\\edge-profile"
```


  

  [返回顶部](#microsoft-edge---策略)

  ### RoamingProfileSupportEnabled
  #### 启用对 Microsoft Edge 用户配置数据使用漫游副本
  
  
  #### 支持的版本:
  - 在 Windows 自 85 或之后

  #### 描述
  启用此策略可在 Windows 上使用漫游用户配置。存储在 Microsoft Edge 用户配置中的设置(收藏夹和首选项)也将保存到一个文件中，该文件存储在漫游用户的用户配置文件夹中(或管理员通过 [RoamingProfileLocation](#roamingprofilelocation) 策略指定的位置)。

如果禁用或未配置此策略，则仅使用常规的本地用户配置。

[SyncDisabled](#syncdisabled) 策略将禁用所有数据同步，覆盖该策略。

有关使用漫游用户用户配置的详细信息，请参阅 https://docs.microsoft.com/windows-server/storage/folder-redirection/deploy-roaming-user-profiles。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: RoamingProfileSupportEnabled
  - GP 名称: 启用对 Microsoft Edge 用户配置数据使用漫游副本
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: RoamingProfileSupportEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  

  [返回顶部](#microsoft-edge---策略)

  ### RunAllFlashInAllowMode
  #### 将 Adobe Flash 内容设置扩展到所有内容
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  如果启用此策略，则将运行嵌入在网站中的所有 Adobe Flash 内容，前提是此类网站已由用户或通过企业策略在内容设置中设置为允许运行 Adobe Flash。内容包括其他来源中的内容和/或较小内容。

若要控制允许哪些网站运行 Adobe Flash，请参阅 [DefaultPluginsSetting](#defaultpluginssetting)、[PluginsAllowedForUrls](#pluginsallowedforurls) 和 [PluginsBlockedForUrls](#pluginsblockedforurls) 策略中的规范。

如果禁用或未配置此策略，则可能会阻止其他来源(来自未在上述三个策略中指定的站点)的 Adobe Flash 内容或较小内容。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: RunAllFlashInAllowMode
  - GP 名称: 将 Adobe Flash 内容设置扩展到所有内容
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: RunAllFlashInAllowMode
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: RunAllFlashInAllowMode
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SSLErrorOverrideAllowed
  #### 允许用户从 HTTPS 警告页继续
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  当用户访问具有 SSL 错误的站点时，Microsoft Edge 会显示警告页面。

如果启用或未配置(默认)此策略，则用户能够以单击方式浏览这些警告页面。

如果禁用此策略，则会阻止用户以单击方式浏览任何警告页面。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SSLErrorOverrideAllowed
  - GP 名称: 允许用户从 HTTPS 警告页继续
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: SSLErrorOverrideAllowed
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: SSLErrorOverrideAllowed
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SSLVersionMin
  #### 已启用的最低 TLS 版本
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  设置受支持的最低 SSL 版本。如果未配置此策略，则 Microsoft Edge 会使用默认的最低版本，即 TLS 1.0。

如果启用此策略，则可以将最低版本设置为以下值之一:“TLSv1”、“TLSv1.1”或“TLSv1.2”。设置后，Microsoft Edge 不会使用低于指定版本的任何 SSL/TLS 版本。任何无法识别的值都会被忽略。

策略选项映射：

* TLSv1 (tls1) = TLS 1.0

* TLSv1.1 (tls1.1) = TLS 1.1

* TLSv1.2 (tls1.2) = TLS 1.2

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SSLVersionMin
  - GP 名称: 已启用的最低 TLS 版本
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: SSLVersionMin
  - 值类型: REG_SZ
  ##### 示例值:
```
"tls1"
```


  #### Mac 信息和设置
  - 首选项密钥名称: SSLVersionMin
  - 示例值:
``` xml
<string>tls1</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SaveCookiesOnExit
  #### 当 Microsoft Edge 关闭时保存 Cookie
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  如果启用此策略，则当浏览器关闭时，指定的 Cookie 集将免于删除。此策略仅在以下情况下有效:
- 已在“设置”/“隐私和服务”/“关闭时清除浏览数据”中配置“Cookie 和其他网站数据”切换，或者
- 已启用策略 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 或
- 已将策略 [DefaultCookiesSetting](#defaultcookiessetting) 设置为“在会话期间保留 Cookie”。

你可以根据 URL 模式定义网站列表，它将在各个会话之间保留 Cookie。

注意：用户仍可以编辑 Cookie 网站列表以添加或删除 URL。但是，他们不能删除已由管理员添加的 URL。

如果你启用此策略，则关闭浏览器时不会清除 Cookie 列表。

如果你禁用或未配置此策略，则将使用用户的个人配置。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SaveCookiesOnExit
  - GP 名称: 当 Microsoft Edge 关闭时保存 Cookie
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: SaveCookiesOnExit
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SavingBrowserHistoryDisabled
  #### 禁用保存浏览器历史记录
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  禁用保存浏览器历史记录，并阻止用户更改此设置。

如果启用此策略，浏览历史记录将不会保存。这还将禁用标签页同步。

如果禁用或未配置此策略，浏览历史记录将被保存。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SavingBrowserHistoryDisabled
  - GP 名称: 禁用保存浏览器历史记录
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: SavingBrowserHistoryDisabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: SavingBrowserHistoryDisabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ScreenCaptureAllowed
  #### 允许或拒绝屏幕捕获
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 83

  #### 描述
  如果启用此策略，或者未配置此策略，则网页可以使用屏幕共享 API（如 getDisplayMedia() 或桌面捕获扩展 API）进行屏幕捕获。
如果禁用此策略，则对屏幕共享 API 的调用将失败。例如，如果你使用的是基于 Web 的联机会议，则视频或屏幕共享将无法工作。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ScreenCaptureAllowed
  - GP 名称: 允许或拒绝屏幕捕获
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ScreenCaptureAllowed
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: ScreenCaptureAllowed
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ScrollToTextFragmentEnabled
  #### 启用滚动到 URL 片段中的指定文本
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 83

  #### 描述
  此功能允许超链接和地址栏 URL 导航以网页上的特定文本为目标，网页完成加载后将滚动到该文本。

如果启用或未配置此策略，则将允许网页通过 URL 滚动至特定文本片段。

如果禁用此策略，则不允许网页通过 URL 滚动到特定文本片段。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ScrollToTextFragmentEnabled
  - GP 名称: 启用滚动到 URL 片段中的指定文本
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ScrollToTextFragmentEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: ScrollToTextFragmentEnabled
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SearchSuggestEnabled
  #### 启用搜索建议
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  在 Microsoft Edge 的地址栏和自动建议列表中启用 Web 搜索建议，并阻止用户更改此策略。

如果启用此策略，将使用 Web 搜索建议。

如果禁用此策略，则永远不会使用 Web 搜索建议，但仍会显示本地历史记录和本地收藏夹建议。如果禁用此策略，则键入的字符和访问的 URL 不会包含在发送给 Microsoft 的遥测信息中。

如果未设置此策略，则会启用搜索建议，但用户可以对其进行更改。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SearchSuggestEnabled
  - GP 名称: 启用搜索建议
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: SearchSuggestEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: SearchSuggestEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SecurityKeyPermitAttestation
  #### 无需许可即可使用直接安全密钥证明的网站或域
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  指定当请求来自安全密钥的证明证书时不需要显式用户许可的网站和域。此外，向安全密钥发送一个信号，指示它可以使用单独的证明。如果不这样做，每次站点请求安全密钥证明时都会提示用户。

网站(如 https://contoso.com/some/path)仅作为 U2F appID 匹配。域(如 contoso.com)仅作为 webauthn RP ID 匹配。对于指定站点，要涵盖 U2F 和 webauthn API，需要列出 appID URL 和域。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SecurityKeyPermitAttestation
  - GP 名称: 无需许可即可使用直接安全密钥证明的网站或域
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation\1 = "https://contoso.com"

```


  #### Mac 信息和设置
  - 首选项密钥名称: SecurityKeyPermitAttestation
  - 示例值:
``` xml
<array>
  <string>https://contoso.com</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SendIntranetToInternetExplorer
  #### 将所有 Intranet 站点发送到 Internet Explorer
  
  
  #### 支持的版本:
  - 在 Windows 自 77 或之后

  #### 描述
  有关为 Internet Explorer 模式配置最佳体验的指南，请参阅 [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SendIntranetToInternetExplorer
  - GP 名称: 将所有 Intranet 站点发送到 Internet Explorer
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: SendIntranetToInternetExplorer
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  

  [返回顶部](#microsoft-edge---策略)

  ### SendSiteInfoToImproveServices
  #### 发送站点信息来改进 Microsoft 服务 (已弃用)
  >已弃用: 此策略已弃用。目前仍受支持，但将在未来版本中弃用。
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  此策略已被弃用。它目前受支持，但在 Microsoft Edge 89 中将不再使用。对于 Windows 7、Windows 8 和 macOS，此策略将替换为新策略: [DiagnosticData](#diagnosticdata)。在 Win 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569))上，此策略将替换为“允许遥测”。

此策略允许向 Microsoft 发送有关在 Microsoft Edge 中访问的网站的信息，以改进搜索等服务。

启用此策略会向 Microsoft 发送有关在 Microsoft Edge 中访问的网站的信息。禁用此策略不会向 Microsoft 发送有关在 Microsoft Edge 中访问的网站的信息。在这两种情况下，用户都不能更改或覆盖设置。

在 Windows 10 上，如果你未配置此策略，Microsoft Edge 将默认为 Windows 诊断数据设置。如果已启用此策略，Microsoft Edge 将仅发送有关在 Microsoft Edge 中访问的网站的信息(如果将 Windows 诊断数据设置设为“全部”)。如果已禁用此策略，Microsoft Edge 不会发送有关访问的网站的信息。详细了解 Windows 诊断数据设置: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

在 Windows 7、windows 8 和 macOS 上，此策略控制发送有关访问的网站的信息。如果你未配置此策略，Microsoft Edge 将默认为用户的首选项。

若要启用此策略，必须将 [MetricsReportingEnabled](#metricsreportingenabled) 设置为“已启用”。如果未配置或已禁用 [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) 或 [MetricsReportingEnabled](#metricsreportingenabled)，则系统不会将此数据发送给 Microsoft。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SendSiteInfoToImproveServices
  - GP 名称: 发送站点信息来改进 Microsoft 服务 (已弃用)
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: SendSiteInfoToImproveServices
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: SendSiteInfoToImproveServices
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SensorsAllowedForUrls
  #### 允许访问特定网站上的传感器
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  根据 URL 模式定义一个网站列表，这些网站可以访问和使用诸如运动和光线传感器之类的传感器。

如果不配置此策略，则所有网站都将使用来自 [DefaultSensorsSetting](#defaultsensorssetting) 策略(如果已设置)的全局默认值或用户的个人配置。

对于与此策略不匹配的 URL 模式，将使用以下优先顺序: [SensorsBlockedForUrls](#sensorsblockedforurls)策略(如果存在匹配项)、[DefaultSensorsSetting](#defaultsensorssetting) 策略(如果已设置)或用户的个人设置。

此策略中定义的 URL 模式不能与 [SensorsBlockedForUrls](#sensorsblockedforurls) 策略中配置的 URL 模式冲突。您无法允许和阻止 URL。

有关有效 URL 模式的详细信息，请参见 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SensorsAllowedForUrls
  - GP 名称: 允许访问特定网站上的传感器
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: SensorsAllowedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SensorsBlockedForUrls
  #### 阻止访问特定网站上的传感器
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  根据 URL 模式定义一个网站列表，这些网站可以访问诸如运动和光线传感器之类的传感器。

如果不配置此策略，则所有网站都将使用来自 [DefaultSensorsSetting](#defaultsensorssetting) 策略(如果已设置)的全局默认值或用户的个人配置。

对于与此策略不匹配的 URL 模式，将使用以下优先顺序: [SensorsAllowedForUrls](#sensorsallowedforurls)策略(如果存在匹配项)、[DefaultSensorsSetting](#defaultsensorssetting) 策略(如果已设置)或用户的个人设置。

此策略中定义的 URL 模式不能与 [SensorsAllowedForUrls](#sensorsallowedforurls) 策略中配置的 URL 模式冲突。您无法允许和阻止 URL。

有关有效 URL 模式的详细信息，请参见 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SensorsBlockedForUrls
  - GP 名称: 阻止访问特定网站上的传感器
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: SensorsBlockedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SerialAskForUrls
  #### 在特定网站上允许串行 API
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  根据 URL 模式定义不能要求用户授予其串行端口访问权限的网站列表。

如果不配置此策略，则所有网站都将使用来自 [DefaultSerialGuardSetting](#defaultserialguardsetting) 策略(如果已设置)的全局默认值或用户的个人配置。

对于与此策略不匹配的 URL 模式，将使用以下优先顺序: [SerialBlockedForUrls](#serialblockedforurls)策略(如果存在匹配项)、[DefaultSerialGuardSetting](#defaultserialguardsetting) 策略(如果已设置)或用户的个人设置。

此策略中定义的 URL 模式不能与 [SerialBlockedForUrls](#serialblockedforurls) 策略中配置的 URL 模式冲突。您无法允许和阻止 URL。

有关有效 URL 模式的详细信息，请参见 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SerialAskForUrls
  - GP 名称: 在特定网站上允许串行 API
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: SerialAskForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SerialBlockedForUrls
  #### 在特定网站上阻止串行 API
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  根据 URL 模式定义不能要求用户授予其串行端口访问权限的网站列表。

如果不配置此策略，则所有网站都将使用来自 [DefaultSerialGuardSetting](#defaultserialguardsetting) 策略(如果已设置)的全局默认值或用户的个人配置。

对于与此策略不匹配的 URL 模式，将使用以下优先顺序: [SerialAskForUrls](#serialaskforurls)策略(如果存在匹配项)、[DefaultSerialGuardSetting](#defaultserialguardsetting) 策略(如果已设置)或用户的个人设置。

此策略中的 URL 模式不能与 [SerialAskForUrls](#serialaskforurls) 策略中配置的 URL 模式冲突。您无法允许和阻止 URL。

有关有效 URL 模式的详细信息，请参见 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SerialBlockedForUrls
  - GP 名称: 在特定网站上阻止串行 API
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 信息和设置
  - 首选项密钥名称: SerialBlockedForUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### ShowOfficeShortcutInFavoritesBar
  #### 在收藏夹栏中显示 Microsoft Office 快捷方式 (已弃用)
  >已弃用: 此策略已弃用。目前仍受支持，但将在未来版本中弃用。
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  此策略由于操作要求发生变化而未能按预期工作。因此，它已被弃用，不应使用。

指定是否在收藏夹栏中包括 Office.com 的快捷方式。对于登录 Microsoft Edge 的用户，该快捷方式会将用户转到其 Microsoft Office 应用和文档中。
  如果启用或未配置此策略，用户可以通过在收藏夹栏上下文中更改切换来选择是否显示快捷方式。
  如果禁用此策略，则不会显示快捷方式。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: ShowOfficeShortcutInFavoritesBar
  - GP 名称: 在收藏夹栏中显示 Microsoft Office 快捷方式 (已弃用)
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: ShowOfficeShortcutInFavoritesBar
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: ShowOfficeShortcutInFavoritesBar
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SignedHTTPExchangeEnabled
  #### 启用签名 HTTP Exchange (SXG) 支持
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 78

  #### 描述
  启用对已签名 HTTP Exchange (SXG)的支持。

如果未设置或未启用此策略，则 Microsoft Edge 将接受作为已签名 HTTP Exchange 提供的 Web 内容。

如果将此策略设置为“已禁用”，则无法加载已签名 HTTP Exchange。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SignedHTTPExchangeEnabled
  - GP 名称: 启用签名 HTTP Exchange (SXG) 支持
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: SignedHTTPExchangeEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: SignedHTTPExchangeEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SitePerProcess
  #### 为每个站点启用站点隔离
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  [SitePerProcess](#siteperprocess) 策略可用于阻止用户选择不采取隔离所有站点这一默认行为。请注意，你还可以使用 [IsolateOrigins](#isolateorigins) 策略隔离其他更细粒度的来源。
如果启用此策略，则用户只能选择采取默认行为，即每个站点在自身进程中运行。
如果禁用或未配置此策略，则用户可以选择不采取站点隔离。(例如，通过在 edge://flags 中使用“禁用站点隔离”项来实现)。禁用或未配置此策略不会导致站点隔离关闭。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SitePerProcess
  - GP 名称: 为每个站点启用站点隔离
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: SitePerProcess
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: SitePerProcess
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SpellcheckEnabled
  #### 启用拼写检查
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  如果启用或未配置此策略，则用户可以使用拼写检查。

如果禁用此策略，则用户不能使用拼写检查，并且 [SpellcheckLanguage](#spellchecklanguage) 和 [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) 策略也将被禁用。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SpellcheckEnabled
  - GP 名称: 启用拼写检查
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: SpellcheckEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: SpellcheckEnabled
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SpellcheckLanguage
  #### 启用特定拼写检查语言
  
  
  #### 支持的版本:
  - 在 Windows 自 77 或之后

  #### 描述
  启用不同的语言以进行拼写检查。任何所指定的无法识别的语言都将被忽略。

如果启用此策略，则会对指定的语言以及用户启用的任何语言启用拼写检查。

如果未配置或禁用此策略，则用户的拼写检查首选项没有变化。

如果禁用 [SpellcheckEnabled](#spellcheckenabled) 策略，则此策略将不起作用。

如果 [SpellcheckLanguage](#spellchecklanguage) 和 [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) 策略中都包含某种语言，则将启用该拼写检查语言。

支持的语言包括: af、bg、ca、cs、cy、da、de、el、en-AU、en-CA、en-GB、en-US、es、es-419、es-AR、es-ES、es-MX、es-US、et、fa、fo、fr、he、hi、hr、hu、id、it、ko、lt、lv、nb、nl、pl、pt-BR、pt-PT、ro、ru、sh、sk、sl、sq、sr、sv、ta、tg、tr、uk、vi。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SpellcheckLanguage
  - GP 名称: 启用特定拼写检查语言
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\2 = "es"

```


  

  [返回顶部](#microsoft-edge---策略)

  ### SpellcheckLanguageBlocklist
  #### 强制禁用拼写检查功能的语言
  
  
  #### 支持的版本:
  - 在 Windows 自 78 或之后

  #### 描述
  强制禁用拼写检查语言。该列表中无法识别的语言将被忽略。

如果启用此策略，将对指定语言禁用拼写检查。用户仍然可以对不在列表中的语言启用或禁用拼写检查。

如果未设置或禁用此策略，则用户的拼写检查首选项将不会更改。

如果 [SpellcheckEnabled](#spellcheckenabled) 策略设置为“已禁用”，则此策略将不起作用。

如果在 [SpellcheckLanguage](#spellchecklanguage) 和 [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) 策略中都包含某种语言，则将启用该拼写检查语言。

当前支持的语言包括: af、bg、ca、cs、da、de、el、en-AU、en-CA、en-GB、en-US、es、es-419、es-AR、es-ES、es-MX、es-US、et、fa、fo、fr、he、hi、hr、hu、id、it、ko、lt、lv、nb、nl、pl、pt-BR、pt-PT、ro、ru、sh、sk、sl、sq、sr、sv、ta、tg、tr、uk、vi。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SpellcheckLanguageBlocklist
  - GP 名称: 强制禁用拼写检查功能的语言
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\2 = "es"

```


  

  [返回顶部](#microsoft-edge---策略)

  ### StricterMixedContentTreatmentEnabled
  #### 针对混合内容启用更严格的处理 (已弃用)
  >已弃用: 此策略已弃用。目前仍受支持，但将在未来版本中弃用。
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 81

  #### 描述
  此策略已弃用，因为它旨在仅作为一种短期机制，让企业在发现它与更严格的混合内容处理不兼容时，有更多时间更新其 Web 内容。它将无法在 Microsoft Edge 版本 85 中正常使用。

此策略控制浏览器中的混合内容 (HTTPS 站点中的 HTTP 内容) 的处理。

如果将此策略设置为“true”或未设置，则音频和视频混合内容将自动升级到 HTTPS (即，URL 将被重写为 HTTPS; 如果资源在 HTTPS 上不可用，则无回退)，并且图像混合内容的 URL 栏中将显示“不安全”警告。

如果将策略设置为“false”，将禁用音频和视频的自动升级，并且不会针对图像显示警告。

此策略不会影响音频、视频和图像以外的其他混合内容类型。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: StricterMixedContentTreatmentEnabled
  - GP 名称: 针对混合内容启用更严格的处理 (已弃用)
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: StricterMixedContentTreatmentEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: StricterMixedContentTreatmentEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SuppressUnsupportedOSWarning
  #### 禁止不支持的操作系统警告
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  取消当 Microsoft Edge 运行于不再受支持的计算机或操作系统上时显示的警告。

如果此策略为 False 或未设置，则将在此类不受支持的计算机或操作系统上显示警告。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SuppressUnsupportedOSWarning
  - GP 名称: 禁止不支持的操作系统警告
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: SuppressUnsupportedOSWarning
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: SuppressUnsupportedOSWarning
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SyncDisabled
  #### 使用 Microsoft 同步服务禁用数据同步
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  在 Microsoft Edge 中禁用数据同步。此策略还会阻止弹出关于同意进行同步的提示。

如果未设置此策略或未按照建议应用此策略，则用户将可以打开或关闭同步。如果作为强制性策略应用此策略，则用户将无法打开同步。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SyncDisabled
  - GP 名称: 使用 Microsoft 同步服务禁用数据同步
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: SyncDisabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: SyncDisabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### SyncTypesListDisabled
  #### 配置从同步中排除的类型列表
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 83

  #### 描述
  如果启用此策略，则所有指定的数据类型都将从同步中排除。此策略可用于限制上传到 Microsoft Edge 同步服务的数据类型。

你可以为此策略提供以下数据类型之一：“集锦夹”、“设置”、“密码”、“addressesAndMore”、“扩展”、“历史记录”、“openTabs”和“集合”。请注意，这些数据类型名称区分大小写。

用户将无法覆盖禁用的数据类型。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: SyncTypesListDisabled
  - GP 名称: 配置从同步中排除的类型列表
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled\1 = "favorites"

```


  #### Mac 信息和设置
  - 首选项密钥名称: SyncTypesListDisabled
  - 示例值:
``` xml
<array>
  <string>favorites</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### TLS13HardeningForLocalAnchorsEnabled
  #### 对本地信任密钥启用 TLS 1.3 安全功能。 (过时)
  
  >过时: 此策略已过时，在 Microsoft Edge 85 之后无法使用。
  #### 支持的版本:
  - 在 Windows 后，在 macOS 和 81 上 85

  #### 描述
  此策略仅为短期机制，旨在为企业提供更多时间升级受影响的代理。因此，目前已不再工作。

此策略控制 TLS 1.3 中的安全功能，该功能可保护连接免遭降级攻击。它向后兼容，不会影响与兼容的 TLS 1.2 服务器或代理的连接。但是，某些较旧版本的拦截 TLS 代理有实现缺陷，导致它们不兼容。

如果启用此策略或不对其进行设置，Microsoft Edge 将为所有连接启用这些安全保护。

如果禁用此策略，Microsoft Edge 会针对通过本地安装的 CA 证书进行身份验证的连接禁用这些安全保护。对于通过公共信任的 CA 证书进行身份验证的连接，将始终启用这些保护。

此策略可用于测试任何受影响的代理并对其进行升级。受影响的代理预期会导致连接失败，错误代码为“ERR_TLS13_DOWNGRADE_DETECTED”。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: TLS13HardeningForLocalAnchorsEnabled
  - GP 名称: 对本地信任密钥启用 TLS 1.3 安全功能。 (过时)
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: TLS13HardeningForLocalAnchorsEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: TLS13HardeningForLocalAnchorsEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### TLSCipherSuiteDenyList
  #### 指定要禁用的 TLS 密码套件
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 85

  #### 描述
  配置为 TLS 连接禁用的密码套件的列表。

 如果配置此策略，则不会在建立 TLS 连接时使用配置的密码套件列表。

 如果未配置此策略，则浏览器将选择要使用的 TLS 密码套件。

要禁用的密码套件值被指定为 16 位十六进制值。这些值由 Internet 分配的号码颁发机构（IANA）注册表指定。

 TLS 1.3 需要 TLS 1.3 密码套件 TLS_AES_128_GCM_SHA256（0x1301），并且无法通过此策略禁用。

 此策略不会影响基于QUIC的连接。可以通过 [QuicAllowed](#quicallowed) 策略关闭 QUIC。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: TLSCipherSuiteDenyList
  - GP 名称: 指定要禁用的 TLS 密码套件
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\1 = "0x1303"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\2 = "0xcca8"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\3 = "0xcca9"

```


  #### Mac 信息和设置
  - 首选项密钥名称: TLSCipherSuiteDenyList
  - 示例值:
``` xml
<array>
  <string>0x1303</string>
  <string>0xcca8</string>
  <string>0xcca9</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### TabFreezingEnabled
  #### 允许冻结后台标签页
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 79

  #### 描述
  控制 Microsoft Edge 是否可以将后台中的标签页至少冻结 5 分钟。

标签页冻结可减少 CPU、电池和内存的使用量。Microsoft Edge 使用试探法来避免冻结在后台执行有用工作(例如显示通知、播放声音和流式传输视频)的标签页。

如果启用此策略或未配置此策略，则后台中已至少存在 5 分钟的标签页可能会被冻结。

如果禁用此策略，则不会冻结任何标签页。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: TabFreezingEnabled
  - GP 名称: 允许冻结后台标签页
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: TabFreezingEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: TabFreezingEnabled
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### TaskManagerEndProcessEnabled
  #### 启用在浏览器任务管理器中结束进程
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  如果启用或未配置此策略，用户可以在浏览器任务管理器中结束进程。如果禁用此策略，用户将无法结束进程，并且浏览器任务管理器中的“结束进程”按钮将被禁用。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: TaskManagerEndProcessEnabled
  - GP 名称: 启用在浏览器任务管理器中结束进程
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: TaskManagerEndProcessEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: TaskManagerEndProcessEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### TotalMemoryLimitMb
  #### 设置单个 Microsoft Edge 实例可以使用的内存限制(MB)。
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 80

  #### 描述
  配置在标签页开始被放弃以节省内存之前，单个 Microsoft Edge 实例可以使用的内存量。将释放该标签页所使用的内存，并且当切换到该标签页时，必须对其重新加载。

如果启用此策略，则当超出限制时，浏览器将开始放弃标签页以节省内存。但不能保证浏览器始终在限制下运行。低于 1024 的任何值都将舍入为 1024。

如果未设置此策略，则在检测到计算机上的物理内存较少时，浏览器将仅尝试节省内存。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: TotalMemoryLimitMb
  - GP 名称: 设置单个 Microsoft Edge 实例可以使用的内存限制(MB)。
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: TotalMemoryLimitMb
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000800
```


  #### Mac 信息和设置
  - 首选项密钥名称: TotalMemoryLimitMb
  - 示例值:
``` xml
<integer>2048</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### TrackingPrevention
  #### 阻止跟踪用户的 Web 浏览活动
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 78

  #### 描述
  允许决定是否阻止网站跟踪用户的 Web 浏览活动。

如果禁用或不配置此策略，则用户可以设置自己的跟踪保护的级别。

策略选项映射：

* TrackingPreventionOff (0) = 关(无跟踪保护)

* TrackingPreventionBasic (1) = 基本（阻止有害的跟踪器，内容和广告将被个性化）

* TrackingPreventionBalanced (2) = 平衡(阻止有害跟踪器以及来自用户尚未访问的站点的跟踪器；内容和广告的个性化程度将较低)

* TrackingPreventionStrict (3) = 严格(阻止有害的跟踪器以及来自所有站点的大多数跟踪器；内容和广告将具有最低的个性化程度。站点的某些部分可能不起作用)

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: TrackingPrevention
  - GP 名称: 阻止跟踪用户的 Web 浏览活动
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: TrackingPrevention
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000002
```


  #### Mac 信息和设置
  - 首选项密钥名称: TrackingPrevention
  - 示例值:
``` xml
<integer>2</integer>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### TranslateEnabled
  #### 启用翻译
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  在 Microsoft Edge 上启用集成式 Microsoft 翻译服务。

如果启用此策略，则 Microsoft Edge 会在适当的情况下显示集成式翻译浮出控件，以及右键单击上下文菜单中的翻译选项，来为用户提供翻译功能。

禁用此策略可以禁用所有内置翻译功能。

如果未配置此策略，则用户可以选择是否使用翻译功能。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 是
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: TranslateEnabled
  - GP 名称: 启用翻译
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 管理模板/Microsoft Edge - 默认设置（用户可以覆盖）/
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): SOFTWARE\Policies\Microsoft\Edge\推荐
  - 值名称: TranslateEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: TranslateEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### URLAllowlist
  #### 定义允许的 URL 列表
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许访问列出的 URL，作为 URL 阻止名单的例外。

根据 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) 设置 URL 模式的格式。

可以使用此策略对限制性阻止名单设置例外。例如，可以在阻止名单中包含 "*" 以阻止所有请求，然后使用此策略允许访问受限制的 URL 列表。可以使用此策略对某些方案、其他域的子域、端口或特定路径设置例外。

最具体的筛选器会确定是阻止还是允许 URL。允许列表优先于阻止名单。

此策略不得超过 1000 个条目；后续条目将被忽略。

此策略还允许浏览器自动调用注册为“tel:”或“ssh:”等协议的协议处理程序的外部应用程序。

如果未配置此策略，则 [URLBlocklist](#urlblocklist) 策略中的阻止名单没有例外。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: URLAllowlist
  - GP 名称: 定义允许的 URL 列表
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\URLAllowlist
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\5 = ".exact.hostname.com"

```


  #### Mac 信息和设置
  - 首选项密钥名称: URLAllowlist
  - 示例值:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### URLBlocklist
  #### 阻止访问 URL 列表
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  根据 URL 模式定义被阻止的站点列表(你的用户无法加载它们)。

根据 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) 设置 URL 模式格式。

你可以在 [URLAllowlist](#urlallowlist) 策略中定义例外。这些策略不得超过 1000 个条目；后续条目将被忽略。

请注意，不建议阻止内部 "edge://*" URL - 这可能会导致意外错误。

此策略不会阻止页面通过 JavaScript 动态更新。例如，如果你阻止 "contoso.com/abc"，那么只要页面不刷新，用户或许仍然可以访问 "contoso.com" 并单击链接来访问 "contoso.com/abc"。

如果你未配置此策略，则不会阻止任何 URL。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: URLBlocklist
  - GP 名称: 阻止访问 URL 列表
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\URLBlocklist
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
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


  #### Mac 信息和设置
  - 首选项密钥名称: URLBlocklist
  - 示例值:
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
  

  [返回顶部](#microsoft-edge---策略)

  ### UserAgentClientHintsEnabled
  #### 启用用户代理客户端提示功能 (已弃用)
  >已弃用: 此策略已弃用。目前仍受支持，但将在未来版本中弃用。
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 86

  #### 描述
  已弃用此策略，因为它仅为短期机制，旨在为企业提供更多时间升级其 Web 内容(如果发现与“用户代理客户端提示”功能不兼容的话)。它将无法在 Microsoft Edge 版本 89 中起作用。

启用此策略时，“用户代理客户端提示”功能会发送粒度请求标题，提供与用户浏览器相关的信息(例如，浏览器版本)和环境(例如，系统体系结构)。

此策略虽然是累加功能，但新标题可能破坏某些限制请求可能包含的字符的网站。

如果启用或未配置此策略，将启用“用户代理客户端提示”功能。如果禁用此策略，则此功能不可用。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: UserAgentClientHintsEnabled
  - GP 名称: 启用用户代理客户端提示功能 (已弃用)
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: UserAgentClientHintsEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: UserAgentClientHintsEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### UserDataDir
  #### 设置用户数据目录
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  设置用于存储用户数据的目录。

如果启用此策略，那么无论用户是否已设置了 "--user-data-dir" 命令行标志，Microsoft Edge 都会使用指定的目录。

如果未启用此策略，则使用默认用户配置路径，但用户可以使用 "--user-data-dir" 标志覆盖它。用户可以在用户配置路径下的 edge://version/ 中找到该用户配置的目录。

为避免数据丢失或其他错误，请不要将此策略配置为卷的根目录或用于其他用途的目录，因为 Microsoft Edge 会管理其内容。

有关可以使用的变量列表，请参阅 [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041)。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: UserDataDir
  - GP 名称: 设置用户数据目录
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: UserDataDir
  - 值类型: REG_SZ
  ##### 示例值:
```
"${users}/${user_name}/Edge"
```


  #### Mac 信息和设置
  - 首选项密钥名称: UserDataDir
  - 示例值:
``` xml
<string>${users}/${user_name}/Edge</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### UserDataSnapshotRetentionLimit
  #### 限制保留的用于紧急回退的用户数据快照的数量
  
  
  #### 支持的版本:
  - 在 Windows 自 86 或之后

  #### 描述
  在每个主要版本更新之后，Microsoft Edge 将创建用户部分浏览数据的快照，以便在以后遇到需要临时回退版本的紧急情况时使用。如果对用户具有相应快照的版本执行临时回退，则会还原快照中的数据。这可让用户保留书签和自动填充数据等设置。

如果不设置此策略，则会使用 3 个快照的默认值。

如果你设置了此策略，则会根据需要删除旧快照以遵守你设置的限制。如果将此策略设置为 0，则不会使用任何快照。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 整数

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: UserDataSnapshotRetentionLimit
  - GP 名称: 限制保留的用于紧急回退的用户数据快照的数量
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: UserDataSnapshotRetentionLimit
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000003
```


  

  [返回顶部](#microsoft-edge---策略)

  ### UserFeedbackAllowed
  #### 允许用户反馈
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  Microsoft Edge 使用 Microsoft Edge 反馈功能(默认情况下已启用)来允许用户发送反馈、建议或客户调查，以及报告任何浏览器问题。另外，默认情况下，用户不能禁用(关闭) Microsoft Edge 反馈功能。

如果启用或未配置此策略，则用户可以调用 Microsoft Edge 反馈。

如果禁用此策略，则用户不能调用 Microsoft Edge 反馈。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: UserFeedbackAllowed
  - GP 名称: 允许用户反馈
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: UserFeedbackAllowed
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: UserFeedbackAllowed
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### VideoCaptureAllowed
  #### 允许或阻止视频捕获
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  控制站点是否可以捕获视频。

如果已启用或未配置(默认)，则将询问用户有关所有站点的视频捕获访问权限的信息，但在 [VideoCaptureAllowedUrls](#videocaptureallowedurls) 策略列表中配置了 URL 的站点除外，这些站点将被授予访问权限而不进行提示。

如果禁用此策略，则不会提示用户，且视频捕获仅适用于 [VideoCaptureAllowedUrls](#videocaptureallowedurls) 策略中配置的 URL。

此策略影响所有类型的视频输入，而不只是内置摄像头。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: VideoCaptureAllowed
  - GP 名称: 允许或阻止视频捕获
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: VideoCaptureAllowed
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000000
```


  #### Mac 信息和设置
  - 首选项密钥名称: VideoCaptureAllowed
  - 示例值:
``` xml
<false/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### VideoCaptureAllowedUrls
  #### 无需请求许可即可访问视频捕获设备的站点
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  根据 URL 模式指定无需用户许可即可使用视频捕获设备的网站。该列表中的模式将与请求 URL 的安全来源进行匹配。如果匹配，站点将自动获得视频捕获设备的访问权限。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: VideoCaptureAllowedUrls
  - GP 名称: 无需请求许可即可访问视频捕获设备的站点
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Mac 信息和设置
  - 首选项密钥名称: VideoCaptureAllowedUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### WPADQuickCheckEnabled
  #### 设置 WPAD 优化
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许你在 Microsoft Edge 中关闭 WPAD (Web 代理自动发现)优化。

如果禁用此策略，则会禁用 WPAD 优化，这会使浏览器等待基于 DNS 的 WPAD 服务器更长时间。

如果启用或未配置此策略，则会启用 WPAD 优化。

无论是否或如何启用此策略，用户都无法更改 WPAD 优化设置。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: WPADQuickCheckEnabled
  - GP 名称: 设置 WPAD 优化
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: WPADQuickCheckEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: WPADQuickCheckEnabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### WebAppInstallForceList
  #### 配置强制安装的 Web 应用列表
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 80

  #### 描述
  指定静默安装、无需用户交互、用户无法卸载或禁用的网站列表。

该策略的每个列表项都是一个具有以下成员的对象:
  - "url"，这是必需的。"url" 应为要安装的 Web 应用的 URL。

可选成员的值包括:
  - "launch_container" 应为 "window" 或 "tab"，以指示安装 Web 应用后如何将其打开。
  - 如果应在 Windows 上创建桌面快捷方式，则 "create_desktop_shortcut" 应为 true。

如果省略 "default_launch_container"，则默认情况下将在标签页中打开应用。无论 "default_launch_container" 的值如何，用户都可以更改将在其中打开该应用的容器。如果省略 "create_desktop_shortcuts"，将不会创建桌面快捷方式。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 是

  #### 数据类型:
  - 字典

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: WebAppInstallForceList
  - GP 名称: 配置强制安装的 Web 应用列表
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: WebAppInstallForceList
  - 值类型: REG_SZ
  ##### 示例值:
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


  #### Mac 信息和设置
  - 首选项密钥名称: WebAppInstallForceList
  - 示例值:
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
  

  [返回顶部](#microsoft-edge---策略)

  ### WebComponentsV0Enabled
  #### 在 M84 之前重新启用 Web 组件 v0 API (过时)
  
  >过时: 此策略已过时，在 Microsoft Edge 84 之后无法使用。
  #### 支持的版本:
  - 在 Windows 后，在 macOS 和 80 上 84

  #### 描述
  此策略不起作用，因为此策略允许在 Microsoft Edge 版本 85 之前选择性地重新启用这些功能。Web 组件 v0 API (影子 DOM v0、自定义元素 v0 和 HTML 导入)已于 2018 年弃用，默认情况下，自 Microsoft Edge 版本 80 开始禁用。

如果将此策略设置为“True”，则将对所有站点启用 Web 组件 v0 功能。

如果将此策略设置为“False”或未设置此策略，自 Microsoft Edge 版本 80 开始，默认将禁用 Web 组件 v0 功能。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: WebComponentsV0Enabled
  - GP 名称: 在 M84 之前重新启用 Web 组件 v0 API (过时)
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: WebComponentsV0Enabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: WebComponentsV0Enabled
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### WebDriverOverridesIncompatiblePolicies
  #### 允许 WebDriver 覆盖不兼容的策略 (过时)
  
  >过时: 此策略已过时，在 Microsoft Edge 84 之后无法使用。
  #### 支持的版本:
  - 在 Windows 后，在 macOS 和 77 上 84

  #### 描述
  此策略不起作用，因为 WebDriver 现在与所有现有策略兼容。

此策略允许使用 WebDriver 功能的用户覆盖
可能干扰该其运行的策略。

目前此策略禁用 [SitePerProcess](#siteperprocess) 和 [IsolateOrigins](#isolateorigins) 策略。

如果启用该策略，WebDriver 将能够覆盖不兼容的
策略。
如果禁用或未配置此策略，则 WebDriver 将无法
覆盖不兼容的策略。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: WebDriverOverridesIncompatiblePolicies
  - GP 名称: 允许 WebDriver 覆盖不兼容的策略 (过时)
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: WebDriverOverridesIncompatiblePolicies
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  #### Mac 信息和设置
  - 首选项密钥名称: WebDriverOverridesIncompatiblePolicies
  - 示例值:
``` xml
<true/>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### WebRtcLocalIpsAllowedUrls
  #### 管理 WebRTC 的本地 IP 地址公开
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 80

  #### 描述
  指定本地 IP 地址应由 WebRTC 公开的源(URL)或主机名模式(如 "*contoso.com*")的列表。

如果启用此策略并设置源(URL)或主机名模式列表，那么当启用 edge://flags/#enable-webrtc-hide-local-ips-with-mdns 时，对于与列表中的模式匹配的情况，WebRTC 将公开本地 IP 地址。

如果禁用或未配置此策略，并且启用了 edge://flags/#enable-webrtc-hide-local-ips-with-mdns，则 WebRTC 将不会公开本地 IP 地址。本地 IP 地址用 mDNS 主机名隐藏。

如果启用、禁用或未配置此策略，并且禁用了 edge://flags/#enable-webrtc-hide-local-ips-with-mdns，则 WebRTC 将公开本地 IP 地址。

请注意，此策略会削弱管理员可能需要的本地 IP 地址保护。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串列表

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: WebRtcLocalIpsAllowedUrls
  - GP 名称: 管理 WebRTC 的本地 IP 地址公开
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls
  - 路径 (推荐): 不适用
  - 值名称: 1, 2, 3, ...
  - 值类型: REG_SZ 列表
  ##### 示例值:
```
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\2 = "*contoso.com*"

```


  #### Mac 信息和设置
  - 首选项密钥名称: WebRtcLocalIpsAllowedUrls
  - 示例值:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>*contoso.com*</string>
</array>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### WebRtcLocalhostIpHandling
  #### 限制 WebRTC 的本地 IP 地址公开
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  允许你设置 WebRTC 是否公开用户的本地 IP 地址。

如果将此策略设置为“AllowAllInterfaces”或“AllowPublicAndPrivateInterfaces”，则 WebRTC 将公开本地 IP 地址。

如果将此策略设置为“AllowPublicInterfaceOnly”或“DisableNonProxiedUdp”，则 WebRTC 不会公开本地 IP 地址。

如果未设置此策略，或者如果禁用它，则 WebRTC 将公开本地 IP 地址。

策略选项映射：

* AllowAllInterfaces (default) = 允许使用所有接口。这会公开本地 IP 地址

* AllowPublicAndPrivateInterfaces (default_public_and_private_interfaces) = 允许通过 http 默认路由使用公共和专用接口。这会公开本地 IP 地址

* AllowPublicInterfaceOnly (default_public_interface_only) = 允许通过 http 默认路由使用公共接口。这不会公开本地 IP 地址

* DisableNonProxiedUdp (disable_non_proxied_udp) = 除非代理服务器支持 UDP，否则，请使用 TCP。这不会公开本地 IP 地址

配置此策略时，请使用上述信息。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: WebRtcLocalhostIpHandling
  - GP 名称: 限制 WebRTC 的本地 IP 地址公开
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: WebRtcLocalhostIpHandling
  - 值类型: REG_SZ
  ##### 示例值:
```
"default"
```


  #### Mac 信息和设置
  - 首选项密钥名称: WebRtcLocalhostIpHandling
  - 示例值:
``` xml
<string>default</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### WebRtcUdpPortRange
  #### 限制 WebRTC 使用的本地 UDP 端口的范围
  
  
  #### 支持的版本:
  - 由于 Windows 或更高版本，macOS 和 77

  #### 描述
  将 WebRTC 使用的 UDP 端口范围限制在指定的端口间隔(包括终结点)。

通过配置此策略，可以指定 Webrtc 可以使用的本地 UDP 端口的范围。

如果不配置此策略或将其设置为空字符串或无效端口范围，WebRTC 可以使用任何可用的本地 UDP 端口。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 字符串

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: WebRtcUdpPortRange
  - GP 名称: 限制 WebRTC 使用的本地 UDP 端口的范围
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: WebRtcUdpPortRange
  - 值类型: REG_SZ
  ##### 示例值:
```
"10000-11999"
```


  #### Mac 信息和设置
  - 首选项密钥名称: WebRtcUdpPortRange
  - 示例值:
``` xml
<string>10000-11999</string>
```
  

  [返回顶部](#microsoft-edge---策略)

  ### WinHttpProxyResolverEnabled
  #### 使用 Windows 代理解析程序 (已弃用)
  >已弃用: 此策略已弃用。目前仍受支持，但将在未来版本中弃用。
  
  #### 支持的版本:
  - 在 Windows 自 84 或之后

  #### 描述
  此策略已弃用。在将来的版本中，它将被类似功能取代，请参阅 https://crbug.com/1032820。

使用 Windows 解析所有浏览器网络的代理，而不是 Microsoft Edge 中内置的代理解析程序。Windows 代理解析程序可启用诸如 DirectAccess/NRPT 之类的 Windows 代理功能。

此策略附带了 https://crbug.com/644030 描述的问题，它会导致 Windows 代码提取和执行 PAC 文件，包括通过 [ProxyPacUrl](#proxypacurl) 策略设置的 PAC 文件。由于 PAC 文件的网络提取是通过 Windows 而不是 Microsoft Edge 代码执行的，因此诸如 [DnsOverHttpsMode](#dnsoverhttpsmode) 之类的网络策略不适用于 PAC 文件的网络提取。

如果启用此策略，则将使用 Windows 代理解析程序。

如果禁用或未配置此策略，则将使用 Microsoft Edge 代理解析程序。

  #### 支持的功能:
  - 可以为必填字段: 是
  - 可以推荐: 否
  - 动态策略刷新: 否 - 需要重启浏览器

  #### 数据类型:
  - 布尔

  #### Windows 信息和设置
  ##### 组策略(ADMX)信息
  - GP 唯一名称: WinHttpProxyResolverEnabled
  - GP 名称: 使用 Windows 代理解析程序 (已弃用)
  - GP 路径 (强制): 管理模板/Microsoft Edge/
  - GP 路径 (推荐): 不适用
  - GP ADMX 文件名: MSEdge.admx
  ##### Windows 注册表设置
  - 路径 (强制): SOFTWARE\Policies\Microsoft\Edge
  - 路径 (推荐): 不适用
  - 值名称: WinHttpProxyResolverEnabled
  - 值类型: REG_DWORD
  ##### 示例值:
```
0x00000001
```


  

  [返回顶部](#microsoft-edge---策略)


## 另请参阅
- [正在配置 Microsoft Edge](configure-microsoft-edge.md)
- [Microsoft Edge 企业登陆页](https://aka.ms/EdgeEnterprise)
- [Microsoft 安全基准博客](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)