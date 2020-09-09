---
title: "Microsoft Edge Browser Policy Documentation"
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 09/08/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom:
description: "Windows and Mac documentation for all policies supported by the Microsoft Edge Browser"
---

# Microsoft Edge - 정책
최신 버전의 Microsoft Edge에는 다음과 같은 정책이 포함되어 있습니다. 이러한 정책을 사용하여 조직에서 Microsoft Edge가 실행되는 방식을 구성할 수 있습니다.

Microsoft Edge가 업데이트되는 방법과 시기를 제어하는 데 사용되는 추가 정책 집합에 대한 정보는 [Microsoft Edge 업데이트 정책 참조](microsoft-edge-update-policies.md)을 확인하세요.

Microsoft Edge에 대한 권장 보안 구성 기준 설정에 대 해 [Microsoft 보안 준수 도구 키트](https://www.microsoft.com/download/details.aspx?id=55319)을(를) 다운로드할 수 있습니다. 자세한 내용은 [Microsoft 보안 기준 블로그](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)을(를) 참조하세요.

> [!참고]
> 이 문서는 Microsoft Edge 버전 77 이상에 적용됩니다.

## 사용 가능한 정책
이 표에는이 Microsoft Edge 릴리스에서 사용할 수 있는 모든 브라우저 관련 그룹 정책이 나열 되어 있습니다. 특정 정책에 대 한 자세한 내용을 보려면 테이블에 있는 링크를 사용 하십시오.

|||
|-|-|
|[Application Guard 설정](#application-guard-설정)|[Cast](#cast)|
|[HTTP 인증](#http-인증)|[SmartScreen 설정](#smartscreen-설정)|
|[기본 검색 공급자](#기본-검색-공급자)|[기본 메시지](#기본-메시지)|
|[시작, 홈 페이지 및 새 탭 페이지](#시작-홈-페이지-및-새-탭-페이지)|[암호 관리자 및 보호](#암호-관리자-및-보호)|
|[인쇄 중](#인쇄-중)|[콘텐츠 설정](#콘텐츠-설정)|
|[프록시 서버](#프록시-서버)|[확장](#확장)|
|[Additional](#additional)|

### [*Application Guard 설정*](#application-guard-설정-policies)
|정책 이름|설명|
|-|-|
|[ApplicationGuardContainerProxy](#applicationguardcontainerproxy)|Application Guard 컨테이너 프록시|
### [*Cast*](#cast-policies)
|정책 이름|설명|
|-|-|
|[EnableMediaRouter](#enablemediarouter)|Google Cast 사용|
|[ShowCastIconInToolbar](#showcasticonintoolbar)|도구 모음에서 캐스트 아이콘 표시|
### [*HTTP 인증*](#http-인증-policies)
|정책 이름|설명|
|-|-|
|[AllowCrossOriginAuthPrompt](#allowcrossoriginauthprompt)|원본 간 HTTP 기본 인증 메시지 표시 허용|
|[AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)|Microsoft Edge가 사용자 자격 증명을 위임할 수 있는 서버 목록을 지정합니다.|
|[AuthSchemes](#authschemes)|지원되는 인증 방식|
|[AuthServerAllowlist](#authserverallowlist)|허용된 인증 서버의 목록 구성|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|Kerberos 인증을 협상할 때 CNAME 조회 사용 안 함|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|Kerberos SPN에 비표준 포트 포함|
|[NtlmV2Enabled](#ntlmv2enabled)|NTLMv2 인증을 사용할지 여부 제어|
### [*SmartScreen 설정*](#smartscreen-설정-policies)
|정책 이름|설명|
|-|-|
|[PreventSmartScreenPromptOverride](#preventsmartscreenpromptoverride)|사이트에 대한 Microsoft Defender SmartScreen 프롬프트 무시 허용 안 함|
|[PreventSmartScreenPromptOverrideForFiles](#preventsmartscreenpromptoverrideforfiles)|다운로드에 대한 Microsoft Defender SmartScreen 경고 무시 허용 안 함|
|[SmartScreenAllowListDomains](#smartscreenallowlistdomains)|Microsoft Defender SmartScreen이 경고를 트리거하지 않는 도메인 목록 구성|
|[SmartScreenEnabled](#smartscreenenabled)|Microsoft Defender SmartScreen 구성|
|[SmartScreenForTrustedDownloadsEnabled](#smartscreenfortrusteddownloadsenabled)|신뢰할 수 있는 원본의 다운로드에 대한 Microsoft Defender SmartScreen 검사 강제 적용|
|[SmartScreenPuaEnabled](#smartscreenpuaenabled)|사용자 동의 없이 설치된 앱을 차단하도록 Microsoft Defender SmartScreen 구성|
### [*기본 검색 공급자*](#기본-검색-공급자-policies)
|정책 이름|설명|
|-|-|
|[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)|기본 검색 공급자 사용|
|[DefaultSearchProviderEncodings](#defaultsearchproviderencodings)|기본 검색 공급자 인코딩|
|[DefaultSearchProviderImageURL](#defaultsearchproviderimageurl)|기본 검색 공급자에 대한 이미지로 검색하기 기능을 지정합니다.|
|[DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams)|POST를 사용하는 이미지 URL에 대한 매개 변수|
|[DefaultSearchProviderKeyword](#defaultsearchproviderkeyword)|기본 검색 공급자 키워드|
|[DefaultSearchProviderName](#defaultsearchprovidername)|기본 검색 공급자 이름|
|[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)|기본 검색 공급자 검색 URL|
|[DefaultSearchProviderSuggestURL](#defaultsearchprovidersuggesturl)|제안에 대한 기본 검색 공급자 URL|
|[NewTabPageSearchBox](#newtabpagesearchbox)|새 탭 페이지 검색 상자 환경 구성|
### [*기본 메시지*](#기본-메시지-policies)
|정책 이름|설명|
|-|-|
|[NativeMessagingAllowlist](#nativemessagingallowlist)|사용자가 사용할 수 있는 기본 메시징 호스트 제어|
|[NativeMessagingBlocklist](#nativemessagingblocklist)|기본 메시지 차단 목록 구성|
|[NativeMessagingUserLevelHosts](#nativemessaginguserlevelhosts)|사용자 수준 기본 메시징 호스트 허용(관리자 권한 없이 설치됨)|
### [*시작&comma; 홈 페이지 및 새 탭 페이지*](#시작-홈-페이지-및-새-탭-페이지-policies)
|정책 이름|설명|
|-|-|
|[HomepageIsNewTabPage](#homepageisnewtabpage)|새 탭 페이지를 홈 페이지로 설정|
|[HomepageLocation](#homepagelocation)|홈 페이지 URL 구성|
|[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)|새 탭 페이지 레이아웃에 허용되는 배경 종류 구성|
|[NewTabPageCompanyLogo](#newtabpagecompanylogo)|새 탭 페이지 회사 로고 설정 (사용하지 않음)|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|새 탭 페이지에서 기본 상위 사이트 숨기기|
|[NewTabPageLocation](#newtabpagelocation)|새 탭 페이지 URL 구성|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|새 탭 페이지 빠른 연결 설정|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|더 빠른 렌더링을 위해 새 탭 페이지를 미리 로드할 수 있습니다.|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|Microsoft Edge 새 탭 페이지 환경 구성|
|[RestoreOnStartup](#restoreonstartup)|시작 시 수행할 작업|
|[RestoreOnStartupURLs](#restoreonstartupurls)|브라우저가 시작될 때 열 사이트|
|[ShowHomeButton](#showhomebutton)|도구 모음에 홈 버튼 표시|
### [*암호 관리자 및 보호*](#암호-관리자-및-보호-policies)
|정책 이름|설명|
|-|-|
|[PasswordManagerEnabled](#passwordmanagerenabled)|암호 관리자에 암호 저장 사용|
|[PasswordMonitorAllowed](#passwordmonitorallowed)|사용자의 암호가 안전하지 않은 경우 사용자에게 알림이 표시되도록 허용|
|[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)|암호 변경 URL 구성|
|[PasswordProtectionLoginURLs](#passwordprotectionloginurls)|암호 보호 서비스가 암호의 솔티드 해시를 캡처해야 하는 엔터프라이즈 로그인 URL 목록 구성|
|[PasswordProtectionWarningTrigger](#passwordprotectionwarningtrigger)|암호 보호 경고 트리거 구성|
### [*인쇄 중*](#인쇄-중-policies)
|정책 이름|설명|
|-|-|
|[DefaultPrinterSelection](#defaultprinterselection)|기본 프린터 선택 규칙|
|[PrintHeaderFooter](#printheaderfooter)|머리글 및 바닥글 인쇄|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|시스템 기본 프린터를 기본 프린터로 설정|
|[PrintingEnabled](#printingenabled)|인쇄 사용|
|[PrintingPaperSizeDefault](#printingpapersizedefault)|기본 인쇄 페이지 크기|
|[UseSystemPrintDialog](#usesystemprintdialog)|시스템 대화 상자를 사용하여 인쇄|
### [*콘텐츠 설정*](#콘텐츠-설정-policies)
|정책 이름|설명|
|-|-|
|[AutoSelectCertificateForUrls](#autoselectcertificateforurls)|이 사이트에 대한 클라이언트 인증서 자동 선택|
|[CookiesAllowedForUrls](#cookiesallowedforurls)|특정 사이트에서 쿠키 허용|
|[CookiesBlockedForUrls](#cookiesblockedforurls)|특정 사이트에서 쿠키 차단|
|[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)|특정 웹 사이트의 쿠키를 현재 세션으로 제한|
|[DefaultCookiesSetting](#defaultcookiessetting)|쿠키 구성|
|[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)|읽기용 파일 시스템 API의 사용 제어|
|[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)|쓰기용 파일 시스템 API의 사용 제어|
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|기본 지리적 위치 설정|
|[DefaultImagesSetting](#defaultimagessetting)|기본 이미지 설정|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|안전하지 않은 콘텐츠 예외 사용 제어|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|기본 JavaScript 설정|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|기본 알림 설정|
|[DefaultPluginsSetting](#defaultpluginssetting)|기본 Adobe Flash 설정|
|[DefaultPopupsSetting](#defaultpopupssetting)|기본 팝업 창 설정|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|Bluetooth 웹 API의 사용 제어|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|WebUSB API의 사용 제어|
|[FileSystemReadAskForUrls](#filesystemreadaskforurls)|이 사이트에서 파일 시스템 API를 통한 읽기 권한 허용|
|[FileSystemReadBlockedForUrls](#filesystemreadblockedforurls)|이 사이트에서 파일 시스템 API를 통한 읽기 권한 차단|
|[FileSystemWriteAskForUrls](#filesystemwriteaskforurls)|이 사이트의 파일 및 디렉터리에 대한 쓰기 권한 허용|
|[FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls)|이 사이트의 파일 및 디렉터리에 대한 쓰기 권한 차단|
|[ImagesAllowedForUrls](#imagesallowedforurls)|이 사이트의 이미지 허용|
|[ImagesBlockedForUrls](#imagesblockedforurls)|특정 사이트에서 이미지 차단|
|[InsecureContentAllowedForUrls](#insecurecontentallowedforurls)|지정된 사이트에서 안전하지 않은 콘텐츠 허용|
|[InsecureContentBlockedForUrls](#insecurecontentblockedforurls)|지정된 사이트에서 안전하지 않은 콘텐츠 차단|
|[JavaScriptAllowedForUrls](#javascriptallowedforurls)|특정 사이트에서 JavaScript 허용|
|[JavaScriptBlockedForUrls](#javascriptblockedforurls)|특정 사이트에서 JavaScript 차단|
|[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)|기본 레거시 SameSite 쿠키 동작 설정 사용|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist)|지정된 사이트의 쿠키에 대해 레거시 SameSite 동작으로 되돌리기|
|[NotificationsAllowedForUrls](#notificationsallowedforurls)|특정 사이트에서 알림 허용|
|[NotificationsBlockedForUrls](#notificationsblockedforurls)|특정 사이트에서 알림 차단|
|[PluginsAllowedForUrls](#pluginsallowedforurls)|특정 사이트에서 Adobe Flash 플러그 인 허용|
|[PluginsBlockedForUrls](#pluginsblockedforurls)|특정 사이트에서 Adobe Flash 플러그 인 차단|
|[PopupsAllowedForUrls](#popupsallowedforurls)|특정 사이트에서 팝업 창 허용|
|[PopupsBlockedForUrls](#popupsblockedforurls)|특정 사이트에서 팝업 창 차단|
|[RegisteredProtocolHandlers](#registeredprotocolhandlers)|프로토콜 처리기 등록|
|[SpotlightExperiencesAndRecommendationsEnabled](#spotlightexperiencesandrecommendationsenabled)|사용자가 사용자 정의 된 배경 이미지와 텍스트, 제안, 알림,
및 Microsoft 서비스에 대한 팁을 받을 수 있는지 여부를 선택합니다.|
|[WebUsbAllowDevicesForUrls](#webusballowdevicesforurls)|특정 USB 장치에 연결하기 위해 특정 사이트에 대한 액세스 권한 부여|
|[WebUsbAskForUrls](#webusbaskforurls)|특정 사이트에서 WebUSB 허용|
|[WebUsbBlockedForUrls](#webusbblockedforurls)|특정 사이트에서 WebUSB 차단|
### [*프록시 서버*](#프록시-서버-policies)
|정책 이름|설명|
|-|-|
|[ProxyBypassList](#proxybypasslist)|프록시 바이패스 규칙 구성|
|[ProxyMode](#proxymode)|프록시 서버 설정 구성|
|[ProxyPacUrl](#proxypacurl)|프록시.pac 파일 URL 설정|
|[ProxyServer](#proxyserver)|프록시 서버의 주소 또는 URL 구성|
|[ProxySettings](#proxysettings)|프록시 설정|
### [*확장*](#확장-policies)
|정책 이름|설명|
|-|-|
|[ExtensionAllowedTypes](#extensionallowedtypes)|허용된 확장 유형 구성|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|특정 확장 설치 허용|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|설치될 수 없는 확장 제어|
|[ExtensionInstallForcelist](#extensioninstallforcelist)|자동으로 설치되는 확장 제어|
|[ExtensionInstallSources](#extensioninstallsources)|확장 및 사용자 스크립트 설치 원본 구성|
|[ExtensionSettings](#extensionsettings)|확장 관리 설정 구성|
### [*Additional*](#additional-policies)
|정책 이름|설명|
|-|-|
|[AddressBarMicrosoftSearchInBingProviderEnabled](#addressbarmicrosoftsearchinbingproviderenabled)|주소 표시줄의 Bing 추천에서 Microsoft Search 사용|
|[AdsSettingForIntrusiveAdsSites](#adssettingforintrusiveadssites)|침입적인 광고가 있는 사이트에 대한 광고 설정|
|[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory)|브라우저 및 다운로드 기록 삭제 사용|
|[AllowFileSelectionDialogs](#allowfileselectiondialogs)|파일 선택 대화 상자 허용|
|[AllowPopupsDuringPageUnload](#allowpopupsduringpageunload)|언로드하는 동안 페이지에서 팝업을 표시하도록 허용|
|[AllowSurfGame](#allowsurfgame)|서핑 게임 허용|
|[AllowSyncXHRInPageDismissal](#allowsyncxhrinpagedismissal)|페이지 해제 중에 페이지에서 동기 XHR 요청을 보내도록 허용 (사용되지 않음)|
|[AllowTokenBindingForUrls](#allowtokenbindingforurls)|Microsoft Edge에서 토큰 바인딩을 설정하려고 하는 사이트 목록을 구성합니다.|
|[AllowTrackingForUrls](#allowtrackingforurls)|특정 사이트에 대한 추적 방지 예외 구성|
|[AlternateErrorPagesEnabled](#alternateerrorpagesenabled)|웹 페이지를 찾을 수 없을 때 비슷한 페이지 추천|
|[AlwaysOpenPdfExternally](#alwaysopenpdfexternally)|항상 외부에서 PDF 파일 열기|
|[AmbientAuthenticationInPrivateModesEnabled](#ambientauthenticationinprivatemodesenabled)|InPrivate 및 게스트 프로필에 대해 앰비언트 인증 사용|
|[AppCacheForceEnabled](#appcacheforceenabled)|AppCache 기능이 기본적으로 해제되어 있더라도 다시 사용할 수 있도록 허용|
|[ApplicationLocaleValue](#applicationlocalevalue)|응용 프로그램 로캘 설정|
|[AudioCaptureAllowed](#audiocaptureallowed)|오디오 캡처 허용 또는 차단|
|[AudioCaptureAllowedUrls](#audiocaptureallowedurls)|사용 권한을 요청하지 않고 오디오 캡처 장치에 액세스할 수 있는 사이트|
|[AudioSandboxEnabled](#audiosandboxenabled)|오디오 샌드박스 실행 허용|
|[AutoImportAtFirstRun](#autoimportatfirstrun)|처음 실행 시 다른 브라우저의 데이터 및 설정 자동으로 가져오기|
|[AutoLaunchProtocolsFromOrigins](#autolaunchprotocolsfromorigins)|사용자에게 묻지 않고 목록에 있는 원본에서 외부 응용 프로그램을 실행할 수 있는 프로토콜 목록을 정의합니다.|
|[AutoOpenAllowedForURLs](#autoopenallowedforurls)|AutoOpenFileType을 적용할 수 있는 URL입니다.|
|[AutoOpenFileTypes](#autoopenfiletypes)|다운로드 시 자동으로 열어야 하는 파일 형식 목록입니다.|
|[AutofillAddressEnabled](#autofilladdressenabled)|주소 정보 자동 채우기 사용|
|[AutofillCreditCardEnabled](#autofillcreditcardenabled)|신용 카드 정보 자동 채우기 사용|
|[AutoplayAllowed](#autoplayallowed)|웹 사이트에 미디어 자동 재생 허용|
|[BackgroundModeEnabled](#backgroundmodeenabled)|Microsoft Edge가 닫힌 후 백그라운드 앱 계속 실행|
|[BackgroundTemplateListUpdatesEnabled](#backgroundtemplatelistupdatesenabled)|컬렉션 및 템플릿을 사용하는 기타 기능의 사용 가능한 템플릿 목록에 대한 백그라운드 업데이트를 사용하도록 설정합니다.|
|[BingAdsSuppression](#bingadssuppression)|Bing 검색 결과에서 모든 광고 차단|
|[BlockThirdPartyCookies](#blockthirdpartycookies)|타사 쿠키 차단|
|[BrowserAddProfileEnabled](#browseraddprofileenabled)|ID 플라이아웃 메뉴 또는 설정 페이지에서 프로필 만들기 사용|
|[BrowserGuestModeEnabled](#browserguestmodeenabled)|게스트 모드 사용|
|[BrowserNetworkTimeQueriesEnabled](#browsernetworktimequeriesenabled)|브라우저 네트워크 시간 서비스에 대한 쿼리 허용|
|[BrowserSignin](#browsersignin)|브라우저 로그인 설정|
|[BuiltInDnsClientEnabled](#builtindnsclientenabled)|기본 제공 DNS 클라이언트 사용|
|[BuiltinCertificateVerifierEnabled](#builtincertificateverifierenabled)|서버 인증서를 확인 하는 데 기본 제공 인증서 검증 도구를 사용할지 여부를 결정 합니다. (사용되지 않음)|
|[CertificateTransparencyEnforcementDisabledForCas](#certificatetransparencyenforcementdisabledforcas)|subjectPublicKeyInfo 해시 목록에 대한 인증서 투명성 적용 사용 안 함|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](#certificatetransparencyenforcementdisabledforlegacycas)|레거시 인증 기관 목록에 대 한 인증서 투명도 적용 사용 안 함|
|[CertificateTransparencyEnforcementDisabledForUrls](#certificatetransparencyenforcementdisabledforurls)|특정 URL에 대한 인증서 투명성 적용 사용 안 함|
|[ClearBrowsingDataOnExit](#clearbrowsingdataonexit)|Microsoft Edge가 닫힐 때 검색 데이터 지우기|
|[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)|Microsoft Edge 닫을 때 캐시 된 이미지 및 파일을 지웁니다.|
|[ClickOnceEnabled](#clickonceenabled)|사용자가 ClickOnce 프로토콜을 사용하여 파일을 열 수 있도록 허용|
|[CollectionsServicesAndExportsBlockList](#collectionsservicesandexportsblocklist)|지정된 서비스 목록에 대한 액세스 차단 및 컬렉션에서 대상 내보내기|
|[CommandLineFlagSecurityWarningsEnabled](#commandlineflagsecuritywarningsenabled)|명령줄 플래그에 대한 보안 경고 사용|
|[ComponentUpdatesEnabled](#componentupdatesenabled)|Microsoft Edge에서 구성 요소 업데이트 사용|
|[ConfigureDoNotTrack](#configuredonottrack)|추적 안 함 구성|
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|Azure AD 도메인 계정이 없을 때 Active Directory 도메인 계정으로 자동 로그인 구성|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|온라인 텍스트 음성 변환 구성|
|[ConfigureShare](#configureshare)|공유 환경 구성|
|[CustomHelpLink](#customhelplink)|사용자 지정 도움말 링크 지정|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|DNS 가로채기 검사 사용|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|Microsoft Edge를 기본 브라우저로 설정|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|기본 검색 공급자 컨텍스트 메뉴 검색 허용|
|[DefaultSensorsSetting](#defaultsensorssetting)|기본 센서 설정|
|[DefaultSerialGuardSetting](#defaultserialguardsetting)|직렬 API의 사용 제어|
|[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)|탭 탐색 이전에 엔터프라이즈 모드 사이트 목록을 사용할 수 있어야 합니다.|
|[DeleteDataOnMigration](#deletedataonmigration)|마이그레이션 시 이전 브라우저 데이터 삭제|
|[DeveloperToolsAvailability](#developertoolsavailability)|개발자 도구를 사용할 수 있는 위치 제어|
|[DiagnosticData](#diagnosticdata)|브라우저 사용 현황에 대한 필수 및 선택적인 진단 데이터 보내기|
|[DirectInvokeEnabled](#directinvokeenabled)|사용자가 DirectInvoke 프로토콜을 사용하여 파일을 열 수 있도록 허용|
|[Disable3DAPIs](#disable3dapis)|3D 그래픽 API에 대한 지원 사용 안 함|
|[DisableScreenshots](#disablescreenshots)|스크린샷 찍기 사용 안 함|
|[DiskCacheDir](#diskcachedir)|디스크 캐시 디렉터리 설정|
|[DiskCacheSize](#diskcachesize)|디스크 캐시 크기를 바이트 단위로 설정|
|[DnsOverHttpsMode](#dnsoverhttpsmode)|DNS-over-HTTPS 모드 제어|
|[DnsOverHttpsTemplates](#dnsoverhttpstemplates)|원하는 DNS over HTTPS 확인 프로그램의 URI 템플릿을 지정합니다.|
|[DownloadDirectory](#downloaddirectory)|다운로드 디렉터리 설정|
|[DownloadRestrictions](#downloadrestrictions)|다운로드 제한 허용|
|[EdgeCollectionsEnabled](#edgecollectionsenabled)|컬렉션 기능 사용|
|[EditFavoritesEnabled](#editfavoritesenabled)|사용자가 즐겨찾기를 편집할 수 있도록 허용|
|[EnableDeprecatedWebPlatformFeatures](#enabledeprecatedwebplatformfeatures)|제한된 기간 동안 사용되지 않은 웹 플랫폼 기능 다시 사용|
|[EnableDomainActionsDownload](#enabledomainactionsdownload)|Microsoft에서 도메인 작업 다운로드 사용 (사용하지 않음)|
|[EnableOnlineRevocationChecks](#enableonlinerevocationchecks)|온라인 OCSP/CRL 검사 사용|
|[EnableSha1ForLocalAnchors](#enablesha1forlocalanchors)|로컬 신뢰 앵커로 발급될 때 SHA-1을 사용하여 서명된 인증서 허용 (사용되지 않음)|
|[EnterpriseHardwarePlatformAPIEnabled](#enterprisehardwareplatformapienabled)|관리되는 확장에서 엔터프라이즈 하드웨어 플랫폼 API를 사용하도록 허용|
|[EnterpriseModeSiteListManagerAllowed](#enterprisemodesitelistmanagerallowed)|엔터프라이즈 모드 사이트 목록 관리자 도구에 대한 액세스 허용|
|[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](#exemptdomainfiletypepairsfromfiletypedownloadwarnings)|도메인에서 지정된 파일 형식에 대해 다운로드 파일 형식 확장명 기반의 경고를 사용 안 함|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|실험 및 구성 서비스와의 통신 제어|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox)|외부 프로토콜 대화 상자에 "항상 열기" 확인란을 표시합니다.|
|[FamilySafetySettingsEnabled](#familysafetysettingsenabled)|사용자가 Family Safety를 구성할 수 있도록 허용|
|[FavoritesBarEnabled](#favoritesbarenabled)|즐겨찾기 모음 사용|
|[ForceBingSafeSearch](#forcebingsafesearch)|Bing 유해 정보 차단 적용|
|[ForceCertificatePromptsOnMultipleMatches](#forcecertificatepromptsonmultiplematches)|"AutoSelectCertificateForUrls" 을 사용 하 여 구성 된 사이트에 대해 일치 하는 인증서가 여러 개 있는 경우 Microsoft Edge에서 인증서를 자동으로 선택 해야 하는지 여부를 구성 합니다|
|[ForceEphemeralProfiles](#forceephemeralprofiles)|임시 프로필 사용 설정|
|[ForceGoogleSafeSearch](#forcegooglesafesearch)|Google 유해 정보 차단 적용|
|[ForceLegacyDefaultReferrerPolicy](#forcelegacydefaultreferrerpolicy)|다운그레이드 시 참조 페이지 없음'의 기본 참조 페이지 정책을 사용합니다 (사용되지 않음)|
|[ForceNetworkInProcess](#forcenetworkinprocess)|네트워킹 코드가 브라우저 프로세스에서 실행되도록 강제 (사용하지 않음)|
|[ForceSync](#forcesync)|브라우저 데이터를 강제로 동기화하고 동기화 동의 프롬프트를 표시하지 않음|
|[ForceYouTubeRestrict](#forceyoutuberestrict)|최소 YouTube 제한 모드 강제 적용|
|[FullscreenAllowed](#fullscreenallowed)|전체 화면 모드 허용|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|전역 범위의 HTTP 인증 캐시 사용|
|[GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar)|주소 표시줄에서 단일 단어 항목을 검색하는 대신 직접 인트라넷 사이트 탐색을 강제합니다.|
|[HSTSPolicyBypassList](#hstspolicybypasslist)|HSTS 정책 확인을 무시할 이름 목록 구성|
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|가능한 경우 하드웨어 가속 사용|
|[HideFirstRunExperience](#hidefirstrunexperience)|첫 실행 경험 및 시작 화면 숨기기|
|[ImportAutofillFormData](#importautofillformdata)|자동 채우기 양식 데이터 가져오기 허용|
|[ImportBrowserSettings](#importbrowsersettings)|브라우저 설정 가져오기 허용|
|[ImportCookies](#importcookies)|쿠키 가져오기 허용|
|[ImportExtensions](#importextensions)|확장 가져오기 허용|
|[ImportFavorites](#importfavorites)|즐겨찾기 가져오기 허용|
|[ImportHistory](#importhistory)|검색 기록 가져오기 허용|
|[ImportHomepage](#importhomepage)|홈 페이지 설정 가져오기 허용|
|[ImportOpenTabs](#importopentabs)|열린 탭 가져오기 허용|
|[ImportPaymentInfo](#importpaymentinfo)|결제 정보 가져오기 허용|
|[ImportSavedPasswords](#importsavedpasswords)|저장된 암호 가져오기 허용|
|[ImportSearchEngine](#importsearchengine)|검색 엔진 설정 가져오기 허용|
|[ImportShortcuts](#importshortcuts)|바로 가기 가져오기 허용|
|[InPrivateModeAvailability](#inprivatemodeavailability)|InPrivate 모드 가용성 구성|
|[InsecureFormsWarningsEnabled](#insecureformswarningsenabled)|안전하지 않은 양식에 대한 경고 사용|
|[IntensiveWakeUpThrottlingEnabled](#intensivewakeupthrottlingenabled)|IntensiveWakeUpThrottling 기능 제어|
|[InternetExplorerIntegrationEnhancedHangDetection](#internetexplorerintegrationenhancedhangdetection)|Internet Explorer 모드에 대한 향상된 정지 감지 구성|
|[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)|Internet Explorer 통합 구성|
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|엔터프라이즈 모드 사이트 목록 구성|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|Internet Explorer 모드 페이지에서 시작할 때 구성되지 않은 사이트에 대한 "페이지 내" 탐색 작동 방식 지정|
|[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed)|Internet Explorer 모드 테스트 허용|
|[IsolateOrigins](#isolateorigins)|특정 원본에 대해 사이트 격리 사용|
|[LocalProvidersEnabled](#localprovidersenabled)|현지 공급자의 제안 허용|
|[ManagedFavorites](#managedfavorites)|즐겨찾기 구성|
|[ManagedSearchEngines](#managedsearchengines)|검색 엔진 관리|
|[MaxConnectionsPerProxy](#maxconnectionsperproxy)|프록시 서버에 대 한 동시 연결의 최대 수|
|[MediaRouterCastAllowAllIPs](#mediaroutercastallowallips)|Google Cast가 모든 IP 주소의 캐스트 장치에 연결하도록 허용|
|[MetricsReportingEnabled](#metricsreportingenabled)|사용 현황 및 크래시 관련 데이터 보고 사용 (사용되지 않음)|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|기본 창 Occlusion 사용|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|엔터프라이즈 모드 사이트 목록에 대한 탭 탐색 지연 시간 설정|
|[NetworkPredictionOptions](#networkpredictionoptions)|네트워크 예측 사용|
|[NonRemovableProfileEnabled](#nonremovableprofileenabled)|사용자가 회사 또는 학교 계정으로 자동으로 로그인한 기본 프로필을 항상 가지고 있는지 여부를 구성합니다.|
|[OverrideSecurityRestrictionsOnInsecureOrigin](#overridesecurityrestrictionsoninsecureorigin)|안전하지 않은 원본에 대한 보안 제한이 적용되는 위치 제어|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|웹 사이트에서 사용 가능한 결제 방법을 쿼리할 수 있도록 허용|
|[PersonalizationReportingEnabled](#personalizationreportingenabled)|검색 기록을 Microsoft에 보내 광고, 검색 및 뉴스의 개인 설정 허용|
|[PinningWizardAllowed](#pinningwizardallowed)|작업 표시줄에 고정 마법사 허용|
|[ProactiveAuthEnabled](#proactiveauthenabled)|사전 인증 사용|
|[PromotionalTabsEnabled](#promotionaltabsenabled)|전체 탭 프로모션 콘텐츠 사용|
|[PromptForDownloadLocation](#promptfordownloadlocation)|다운로드한 파일을 저장할 위치 묻기|
|[QuicAllowed](#quicallowed)|QUIC 프로토콜 허용|
|[RelaunchNotification](#relaunchnotification)|보류 중인 업데이트에 대해 브라우저 다시 시작이 권장되거나 필요함을 사용자에게 알림|
|[RelaunchNotificationPeriod](#relaunchnotificationperiod)|업데이트 알림 기간 설정|
|[RendererCodeIntegrityEnabled](#renderercodeintegrityenabled)|렌더러 코드 무결성 사용|
|[RequireOnlineRevocationChecksForLocalAnchors](#requireonlinerevocationchecksforlocalanchors)|온라인 OCSP/CRL 검사가 로컬 트러스트 앵커에 필요한지 여부를 지정합니다.|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|웹 서비스를 사용하여 탐색 오류 해결 사용|
|[RestrictSigninToPattern](#restrictsignintopattern)|Microsoft Edge 기본 계정으로 사용할 수 있는 계정 제한|
|[RoamingProfileLocation](#roamingprofilelocation)|로밍 프로필 디렉토리 설정|
|[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)|Microsoft Edge 프로필 데이터에 대한 로밍 복사본 사용 설정|
|[RunAllFlashInAllowMode](#runallflashinallowmode)|Adobe Flash 콘텐츠 설정을 모든 콘텐츠로 확장|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|HTTPS 경고 페이지에서 사용자가 작업을 계속할 수 있도록 허용|
|[SSLVersionMin](#sslversionmin)|최소 TLS 버전 사용|
|[SaveCookiesOnExit](#savecookiesonexit)|Microsoft Edge 종료 시 쿠키를 저장합니다.|
|[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)|브라우저 기록 저장 사용 안 함|
|[ScreenCaptureAllowed](#screencaptureallowed)|화면 캡처 허용 또는 거부|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|URL 조각에 지정된 텍스트로의 스크롤 사용|
|[SearchSuggestEnabled](#searchsuggestenabled)|검색 제안 사용|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|직접 보안 키 증명 사용 권한이 필요하지 않은 웹 사이트 또는 도메인|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|모든 인트라넷 사이트를 Internet Explorer로 보내기|
|[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)|Microsoft 서비스 개선을 위해 사이트 정보 보내기 (사용되지 않음)|
|[SensorsAllowedForUrls](#sensorsallowedforurls)|특정 사이트의 센서에 대한 액세스 허용|
|[SensorsBlockedForUrls](#sensorsblockedforurls)|특정 사이트의 센서에 대한 액세스 차단|
|[SerialAskForUrls](#serialaskforurls)|특정 사이트에서 직렬 API 허용|
|[SerialBlockedForUrls](#serialblockedforurls)|특정 사이트에서 직렬 API 차단|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|즐겨 찾기 모음에 Microsoft Office 바로 가기 표시|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|서명된 HTTP 교환(SXG) 지원 사용|
|[SitePerProcess](#siteperprocess)|모든 사이트에 대해 사이트 격리 사용|
|[SpellcheckEnabled](#spellcheckenabled)|맞춤법 검사 사용|
|[SpellcheckLanguage](#spellchecklanguage)|특정 맞춤법 검사 언어 사용|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|맞춤법 검사 언어 강제 사용 안 함|
|[StricterMixedContentTreatmentEnabled](#strictermixedcontenttreatmentenabled)|혼합 콘텐츠에 대해 보다 엄격한 처리 가능 (사용되지 않음)|
|[SuppressUnsupportedOSWarning](#suppressunsupportedoswarning)|지원 되지 않는 OS 경고 표시 안 함|
|[SyncDisabled](#syncdisabled)|Microsoft 동기화 서비스를 사용한 데이터의 동기화 사용 안 함|
|[SyncTypesListDisabled](#synctypeslistdisabled)|동기화에서 제외되는 형식 목록 구성하기|
|[TLS13HardeningForLocalAnchorsEnabled](#tls13hardeningforlocalanchorsenabled)|로컬 트러스트 앵커에 대해 TLS 1.3 보안 기능을 사용하도록 설정합니다. (사용하지 않음)|
|[TLSCipherSuiteDenyList](#tlsciphersuitedenylist)|비활성화할 TLS 암호 그룹 지정|
|[TabFreezingEnabled](#tabfreezingenabled)|배경 탭의 고정 허용|
|[TaskManagerEndProcessEnabled](#taskmanagerendprocessenabled)|브라우저 작업 관리자에서 종료 프로세스 사용|
|[TotalMemoryLimitMb](#totalmemorylimitmb)|단일 Microsoft Edge 인스턴스에서 사용할 수 있는 메모리 크기(MB)를 설정합니다.|
|[TrackingPrevention](#trackingprevention)|사용자의 웹 검색 활동 추적 차단|
|[TranslateEnabled](#translateenabled)|번역 사용|
|[URLAllowlist](#urlallowlist)|허용된 URL 목록을 정의|
|[URLBlocklist](#urlblocklist)|URL 목록에 대한 액세스 차단|
|[UserAgentClientHintsEnabled](#useragentclienthintsenabled)|사용자 에이전트 클라이언트 힌트 기능 사용 (사용되지 않음)|
|[UserDataDir](#userdatadir)|사용자 데이터 디렉터리 설정|
|[UserDataSnapshotRetentionLimit](#userdatasnapshotretentionlimit)|비상 롤백이 있을 경우 사용하기 위해 보존된 사용자 데이터 스냅숏 수를 제한합니다.|
|[UserFeedbackAllowed](#userfeedbackallowed)|사용자 피드백 허용|
|[VideoCaptureAllowed](#videocaptureallowed)|비디오 캡처 허용 또는 차단|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|권한을 요청하지 않고 비디오 캡처 장치에 액세스할 수 있는 사이트|
|[WPADQuickCheckEnabled](#wpadquickcheckenabled)|WPAD 최적화 설정|
|[WebAppInstallForceList](#webappinstallforcelist)|강제 설치된 Web Apps 목록 구성|
|[WebComponentsV0Enabled](#webcomponentsv0enabled)|M84이 될 때까지 웹 구성 요소 v0 API 다시 사용 (사용하지 않음)|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|WebDriver가 호환되지 않는 정책을 재정의하도록 허용 (사용하지 않음)|
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|WebRTC에 의한 로컬 IP 주소 노출 관리|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|WebRTC에 의한 로컬 IP 주소 노출 제한|
|[WebRtcUdpPortRange](#webrtcudpportrange)|WebRTC에서 사용하는 로컬 UDP 포트 범위 제한|
|[WinHttpProxyResolverEnabled](#winhttpproxyresolverenabled)|Windows 프록시 해결 프로그램 사용 (사용되지 않음)|




  ## Application Guard 설정 policies

  [맨 위로 이동](#microsoft-edge---정책)

  ### ApplicationGuardContainerProxy
  #### Application Guard 컨테이너 프록시
  
  
  #### 지원되는 버전:
  - Windows 84 이상부터

  #### 설명
  Microsoft Edge Application Guard에 대한 프록시 설정을 구성합니다.
         이 정책을 사용하면 Microsoft Edge Application Guard가 다른 프록시 구성 소스를 무시합니다.

         이 정책을 구성하지 않으면 Microsoft Edge Application Guard는 호스트의 프록시 구성을 사용합니다.

         이 정책은 Application Guard(호스트)를 벗어나는 Microsoft Edge의 프록시 구성에 영향을 미치지 않습니다.

ProxyMode 필드에서 Microsoft Edge Application Guard에서 사용하는 프록시 서버를 지정할 수 있습니다.

ProxyPacUrl 필드는 프록시 .pac 파일의 URL입니다.

ProxyServer 필드는 프록시 서버의 URL입니다.

         '직접' 값을 'ProxyMode'(으)로 선택하면 다른 모든 필드는 무시됩니다.

         'auto_detect' 값을 'ProxyMode'(으)로 선택하면 다른 모든 필드는 무시됩니다.

         'fixed_servers' 값을 'ProxyMode'(으)로 선택하면 'ProxyServer' 필드가 사용됩니다.

         'pac_script' 값을 'ProxyMode'(으)로 선택하면 'ProxyPacUrl' 필드가 사용됩니다.

이중 프록시를 통해 Application Guard 트래픽을 식별하는 방법에 대한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2134653](https://go.microsoft.com/fwlink/?linkid=2134653)을 방문하시기 바랍니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 사전

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ApplicationGuardContainerProxy
  - GP 이름: Application Guard 컨테이너 프록시
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/Application Guard 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ApplicationGuardContainerProxy
  - 값 형식: REG_SZ
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ## Cast policies

  [맨 위로 이동](#microsoft-edge---정책)

  ### EnableMediaRouter
  #### Google Cast 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  이 정책을 사용하면 Google Cast를 사용하도록 설정할 수 있습니다. 사용자는 앱 메뉴, 페이지 상황에 맞는 메뉴, 캐스트 사용 웹 사이트의 미디어 컨트롤 및 캐스트 도구 모음 아이콘(표시되는 경우)에서 이를 시작할 수 있습니다.

Google 캐스트를 사용하지 않으려면 이 정책을 사용하지 않도록 설정하세요.

기본적으로 Google 캐스트를 사용하도록 설정되어 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: EnableMediaRouter
  - GP 이름: Google Cast 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/Cast
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: EnableMediaRouter
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: EnableMediaRouter
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ShowCastIconInToolbar
  #### 도구 모음에서 캐스트 아이콘 표시
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  도구 모음이나 오버플로 메뉴에 캐스트 도구 모음 아이콘을 표시하려면 이 정책을 true로 설정합니다. 사용자는 이 정책을 제거할 수 없습니다.

이 정책을 구성하지 않거나 사용하지 않도록 설정 하는 경우 사용자는 상황에 맞는 메뉴를 사용하여 아이콘을 고정하거나 제거할 수 있습니다.

[EnableMediaRouter](#enablemediarouter) 정책을 false로 설정하면 이 정책은 무시되고 도구 모음 아이콘은 표시되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ShowCastIconInToolbar
  - GP 이름: 도구 모음에서 캐스트 아이콘 표시
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/Cast
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ShowCastIconInToolbar
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ShowCastIconInToolbar
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ## HTTP 인증 policies

  [맨 위로 이동](#microsoft-edge---정책)

  ### AllowCrossOriginAuthPrompt
  #### 원본 간 HTTP 기본 인증 메시지 표시 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  페이지의 타사 하위 콘텐츠가 HTTP 기본 인증 대화 상자를 열 수 있는지 여부를 제어합니다.

일반적으로 피싱 방어는 사용하지 않도록 설정되어 있습니다. 이 정책을 구성하지 않는 경우 사용하지 않도록 설정되고 타사 하위 콘텐츠는 HTTP 기본 인증 대화 상자를 열 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AllowCrossOriginAuthPrompt
  - GP 이름: 원본 간 HTTP 기본 인증 메시지 표시 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/HTTP 인증
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AllowCrossOriginAuthPrompt
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AllowCrossOriginAuthPrompt
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AuthNegotiateDelegateAllowlist
  #### Microsoft Edge가 사용자 자격 증명을 위임할 수 있는 서버 목록을 지정합니다.
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge가 위임할 수 있는 서버 목록을 구성합니다.

여러 개의 서버 이름을 쉼표로 구분합니다. 와일드카드(*)는 허용됩니다.

이 정책을 구성하지 않으면 서버가 인트라넷으로 검색된 경우에도 Microsoft Edge는 사용자 자격 증명을 위임하지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AuthNegotiateDelegateAllowlist
  - GP 이름: Microsoft Edge가 사용자 자격 증명을 위임할 수 있는 서버 목록을 지정합니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/HTTP 인증
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AuthNegotiateDelegateAllowlist
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"contoso.com"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AuthNegotiateDelegateAllowlist
  - 예제 값:
``` xml
<string>contoso.com</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AuthSchemes
  #### 지원되는 인증 방식
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  지원되는 HTTP 인증 체계를 지정합니다.

'기본', '다이제스트', 'ntlm'및 '협상'과 같은 값을 사용하여 정책을 구성 할 수 있습니다. 값이 여러 개라면 쉼표로 구분하세요.

이 정책을 구성하지 않으면 네 가지 구성이 모두 사용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AuthSchemes
  - GP 이름: 지원되는 인증 방식
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/HTTP 인증
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AuthSchemes
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"basic,digest,ntlm,negotiate"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AuthSchemes
  - 예제 값:
``` xml
<string>basic,digest,ntlm,negotiate</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AuthServerAllowlist
  #### 허용된 인증 서버의 목록 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  통합 인증을 위해 사용할 서버를 지정합니다. 통합 인증은 Microsoft Edge가 프록시 또는 이 목록의 서버로부터 인증 질문을 받는 경우에만 활성화됩니다.

여러 서버 이름은 쉼표로 구분합니다. 와일드 카드(*)를 사용할 수 있습니다.

이 정책을 구성하지 않으면 Microsoft Edge에서 서버가 인트라넷에 있는지 검색하려고 하고, 그런 다음에만 IWA 요청에 응답합니다. 서버가 인터넷에 연결되어 있으면 Microsoft Edge에 의해 IWA 요청이 무시됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AuthServerAllowlist
  - GP 이름: 허용된 인증 서버의 목록 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/HTTP 인증
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AuthServerAllowlist
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"*contoso.com,contoso.com"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AuthServerAllowlist
  - 예제 값:
``` xml
<string>*contoso.com,contoso.com</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DisableAuthNegotiateCnameLookup
  #### Kerberos 인증을 협상할 때 CNAME 조회 사용 안 함
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  생성된 Kerberos SPN이 정식 DNS 이름(CNAME)을 기반으로 하는지 아니면 원래 원본 이름에 기반으로 하는지 여부를 결정합니다.

이 정책을 사용하면 CNAME 조회를 건너뛰고 입력한 대로 서버 이름이 사용됩니다.

이 정책 설정을 사용하지 않거나 구성하지 않으면 서버의 정식 이름이 사용됩니다. CNAME 조회를 통해 결정 됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DisableAuthNegotiateCnameLookup
  - GP 이름: Kerberos 인증을 협상할 때 CNAME 조회 사용 안 함
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/HTTP 인증
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DisableAuthNegotiateCnameLookup
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DisableAuthNegotiateCnameLookup
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### EnableAuthNegotiatePort
  #### Kerberos SPN에 비표준 포트 포함
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  생성 된 Kerberos SPN에 비표준 포트가 포함되어야 하는지 여부를 지정합니다.

이 정책을 사용하고 사용자가 URL에 비표준 포트 (80 또는 443 이외의 포트)를 포함하면 해당 포트가 생성 된 Kerberos SPN에 포함됩니다.

이 정책을 구성하거나 사용하지 않으면 생성된 Kerberos SPN에는 어떤 경우에도 포트가 포함되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: EnableAuthNegotiatePort
  - GP 이름: Kerberos SPN에 비표준 포트 포함
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/HTTP 인증
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: EnableAuthNegotiatePort
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: EnableAuthNegotiatePort
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### NtlmV2Enabled
  #### NTLMv2 인증을 사용할지 여부 제어
  
  
  #### 지원되는 버전:
  - macOS 77 이상부터

  #### 설명
  NTLMv2를 사용할지 여부를 제어합니다.

모든 최신 버전의 삼바 및 Windows 서버는 NTLMv2 지원합니다. NTLMv2를 사용하지 않도록 설정하면 인증 보안이 약화되기 때문에 이전 버전과의 호환성 문제를 해결하기 위해서만 NTLMv2를 사용하지 않도록 설정해야 합니다.

이 정책을 구성하지 않으면 NTLMv2는 기본적으로 사용하도록 설정됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  

  #### Mac 정보 및 설정
  - 기본 설정 키 이름: NtlmV2Enabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ## SmartScreen 설정 policies

  [맨 위로 이동](#microsoft-edge---정책)

  ### PreventSmartScreenPromptOverride
  #### 사이트에 대한 Microsoft Defender SmartScreen 프롬프트 무시 허용 안 함
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  이 정책 설정을 통해 사용자가 잠재적 악성 웹 사이트에 대한 Microsoft Defender SmartScreen 경고를 무시할 수 있는지 여부를 결정할 수 있습니다.

이 설정을 사용하면 사용자가 Microsoft Defender SmartScreen 경고를 무시할 수 없으며 해당 사이트를 계속 사용할 수 없습니다.

이 설정을 사용하지 않거나 구성하지 않으면 사용자가 Microsoft Defender SmartScreen 경고를 무시하고 해당 사이트를 계속 사용할 수 있습니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PreventSmartScreenPromptOverride
  - GP 이름: 사이트에 대한 Microsoft Defender SmartScreen 프롬프트 무시 허용 안 함
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/SmartScreen 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: PreventSmartScreenPromptOverride
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PreventSmartScreenPromptOverride
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PreventSmartScreenPromptOverrideForFiles
  #### 다운로드에 대한 Microsoft Defender SmartScreen 경고 무시 허용 안 함
  
  
  #### 지원되는 버전:
  - Windows 77 이상부터
  - macOS 79 이상부터

  #### 설명
  이 정책을 통해 사용자가 확인되지 않은 다운로드에 대한 Microsoft Defender SmartScreen 경고를 무시할 수 있는지 여부를 결정할 수 있습니다.

이 정책을 사용하면 조직의 사용자가 Microsoft Defender SmartScreen 경고를 무시할 수 없으며 확인되지 않은 다운로드를 완료할 수 없습니다.

이 정책을 사용하지 않거나 구성하지 않으면 사용자가 Microsoft Defender SmartScreen 경고를 무시하고 확인되지 않은 다운로드를 완료할 수 있습니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PreventSmartScreenPromptOverrideForFiles
  - GP 이름: 다운로드에 대한 Microsoft Defender SmartScreen 경고 무시 허용 안 함
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/SmartScreen 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: PreventSmartScreenPromptOverrideForFiles
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PreventSmartScreenPromptOverrideForFiles
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SmartScreenAllowListDomains
  #### Microsoft Defender SmartScreen이 경고를 트리거하지 않는 도메인 목록 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Defender SmartScreen에서 트러스트된 도메인 목록을 구성합니다. 즉,
원본 URL이 이 도메인과 일치하는 경우 Microsoft Defender SmartScreen은 피싱 소프트웨어 및 기타 맬웨어와 같은 잠재적 악성 리소스를 확인하지 않습니다.
Microsoft Defender SmartScreen 다운로드 보호 서비스는 해당 도메인에서 호스팅되는 다운로드를 확인하지 않습니다.

이 정책을 사용하면 Microsoft Defender SmartScreen에서 이러한 도메인을 신뢰합니다.
이 정책을 사용하지 않거나 설정하지 않으면 기본 Microsoft Defender SmartScreen 보호가 모든 리소스에 적용됩니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.
또한, 조직에서 Microsoft Defender Advanced Threat Protection을 사용하도록 설정한 경우에는 이 정책이 적용되지 않습니다. Microsoft Defender 보안 센터에서 허용 및 차단 목록을 구성해야 합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SmartScreenAllowListDomains
  - GP 이름: Microsoft Defender SmartScreen이 경고를 트리거하지 않는 도메인 목록 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/SmartScreen 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\2 = "myuniversity.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SmartScreenAllowListDomains
  - 예제 값:
``` xml
<array>
  <string>mydomain.com</string>
  <string>myuniversity.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SmartScreenEnabled
  #### Microsoft Defender SmartScreen 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  이 정책 설정을 통해 Microsoft Defender SmartScreen을 활성화할지 여부를 구성할 수 있습니다. Microsoft Defender SmartScreen은 피싱 사기 및 악성 소프트웨어로부터 사용자를 보호하는데 도움이 되는 경고 메시지를 제공합니다 기본적으로 Microsoft Defender SmartScreen은 켜져 있습니다.

이 설정을 사용하면 Microsoft Defender SmartScreen이 켜집니다.

이 설정을 사용하지 않으면 Microsoft Defender SmartScreen이 꺼집니다.

이 설정을 구성하지 않으면 사용자가 Microsoft Defender SmartScreen을 사용할지 여부를 선택할 수 있습니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SmartScreenEnabled
  - GP 이름: Microsoft Defender SmartScreen 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/SmartScreen 설정
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/SmartScreen 설정
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: SmartScreenEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SmartScreenEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SmartScreenForTrustedDownloadsEnabled
  #### 신뢰할 수 있는 원본의 다운로드에 대한 Microsoft Defender SmartScreen 검사 강제 적용
  
  
  #### 지원되는 버전:
  - Windows 78 이상부터

  #### 설명
  이 정책 설정을 통해 Microsoft Defender SmartScreen이 신뢰할 수 있는 원본의 다운로드 신뢰도를 확인할 지 여부를 구성할 수 있습니다.

이 설정을 사용하거나 구성하지 않으면 Microsoft Defender SmartScreen이 원본에 관계 없이 다운로드의 신뢰도를 확인합니다.

이 설정을 사용하지 않으면 Microsoft Defender SmartScreen이 신뢰할 수 있는 원본에서 다운로드할 때 다운로드의 신뢰도를 확인하지 않습니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스에서만 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SmartScreenForTrustedDownloadsEnabled
  - GP 이름: 신뢰할 수 있는 원본의 다운로드에 대한 Microsoft Defender SmartScreen 검사 강제 적용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/SmartScreen 설정
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/SmartScreen 설정
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: SmartScreenForTrustedDownloadsEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SmartScreenPuaEnabled
  #### 사용자 동의 없이 설치된 앱을 차단하도록 Microsoft Defender SmartScreen 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 80 이상

  #### 설명
  이 정책 설정을 통해 Microsoft Defender SmartScreen을 사용한 사용자 동의 없이 설치된 앱의 차단을 활성화할지 여부를 구성할 수 있습니다. Microsoft Defender SmartScreen을 사용한 사용자 동의 없이 설치된 앱 차단은 웹 사이트에서 호스트하는 애드웨어, 코인 마이너, 번들웨어 및 기타 낮은 평판의 앱으로부터 사용자를 보호하는 데 도움이 되는 경고 메시지를 제공합니다. Microsoft Defender SmartScreen을 사용한 사용자 동의 없이 설치된 앱 차단은 기본적으로 비활성화되어 있습니다.

이 설정을 사용하면 Microsoft Defender SmartScreen을 사용한 사용자 동의 없이 설치된 앱 차단이 활성화됩니다.

이 설정을 사용하지 않으면 Microsoft Defender SmartScreen을 사용한 사용자 동의 없이 설치된 앱 차단이 비활성화됩니다.

이 설정을 구성하지 않으면 사용자가 Microsoft Defender SmartScreen을 사용한 사용자 동의 없이 설치된 앱 차단을 사용할지 여부를 선택할 수 있습니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SmartScreenPuaEnabled
  - GP 이름: 사용자 동의 없이 설치된 앱을 차단하도록 Microsoft Defender SmartScreen 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/SmartScreen 설정
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/SmartScreen 설정
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: SmartScreenPuaEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SmartScreenPuaEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ## 기본 검색 공급자 policies

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultSearchProviderEnabled
  #### 기본 검색 공급자 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  기본 검색 공급자를 사용하도록 설정합니다.

이 정책을 사용하면(입력한 내용이 URL이 아닌 경우에 한하여) 사용자는 주소 표시줄에 검색어를 입력하여 검색할 수 있습니다.

기본 검색 정책의 나머지 부분을 사용하도록 설정하여 사용할 기본 검색 공급자를 지정할 수 있습니다. 해당 항목을 비워두거나(구성되지 않음) 잘못 구성되어 있으면 사용자는 기본 공급자를 선택할 수 있습니다.

이 정책을 사용하지 않으면 사용자는 주소 표시줄에서 검색할 수 없습니다.

이 정책을 사용하거나 사용하지 않도록 설정하면 사용자는 변경하거나 재정의할 수 없습니다.

이 정책을 구성하지 않으면 기본 검색 공급자를 사용하도록 설정되며 사용자는 기본 검색 공급자를 선택하고 검색 공급자 목록을 설정할 수 있습니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.

Microsoft Edge 84부터 이 정책을 권장 정책으로 설정할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultSearchProviderEnabled
  - GP 이름: 기본 검색 공급자 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/기본 검색 공급자
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/기본 검색 공급자
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: DefaultSearchProviderEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultSearchProviderEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultSearchProviderEncodings
  #### 기본 검색 공급자 인코딩
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  검색 공급자가 지원하는 문자 인코딩을 지정합니다. 인코딩은 UTF-8, GB2312 및 ISO-8859-1과 같은 코드 페이지 이름입니다. 해당 순서대로 시도됩니다.

이 정책은 선택 사항입니다. 구성되지 않은 경우 기본값인 UTF-8이 사용됩니다.

이 정책은 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 및 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 정책을 사용하는 경우에만 적용됩니다.

Microsoft Edge 84부터 이 정책을 권장 정책으로 설정할 수 있습니다. 사용자가 이미 기본 검색 공급자를 설정한 경우 이 권장 정책에서 구성한 기본 검색 공급자는 사용자가 선택할 수 있는 검색 공급자 목록에 추가되지 않습니다. 원하는 동작인 경우 [ManagedSearchEngines](#managedsearchengines) 정책을 사용하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultSearchProviderEncodings
  - GP 이름: 기본 검색 공급자 인코딩
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/기본 검색 공급자
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/기본 검색 공급자
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤\DefaultSearchProviderEncodings
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\1 = "UTF-8"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\2 = "UTF-16"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\3 = "GB2312"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\4 = "ISO-8859-1"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultSearchProviderEncodings
  - 예제 값:
``` xml
<array>
  <string>UTF-8</string>
  <string>UTF-16</string>
  <string>GB2312</string>
  <string>ISO-8859-1</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultSearchProviderImageURL
  #### 기본 검색 공급자에 대한 이미지로 검색하기 기능을 지정합니다.
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  이미지 검색에 사용되는 검색 엔진의 URL을 지정합니다. 검색 요청은 GET 메서드를 사용하여 전송됩니다.

이 정책은 선택 사항입니다. 구성하지 않으면 이미지 검색을 사용할 수 없습니다.

Bing의 이미지 검색 URL을 다음과 같이 지정합니다.
'{bing:baseURL}images/detail/search?iss=sbiupload&FORM=ANCMS1#enterInsights'.

Google의 이미지 검색 URL을 다음과 같이 지정합니다. '{google:baseURL}searchbyimage/upload'.

이미지 검색 구성을 완료하려면 [DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams) 정책을 참조하세요.

이 정책은 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 및 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 정책을 사용하는 경우에만 적용됩니다.

Microsoft Edge 84부터 이 정책을 권장 정책으로 설정할 수 있습니다. 사용자가 이미 기본 검색 공급자를 설정한 경우 이 권장 정책에서 구성한 기본 검색 공급자는 사용자가 선택할 수 있는 검색 공급자 목록에 추가되지 않습니다. 원하는 동작인 경우 [ManagedSearchEngines](#managedsearchengines) 정책을 사용하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultSearchProviderImageURL
  - GP 이름: 기본 검색 공급자에 대한 이미지로 검색하기 기능을 지정합니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/기본 검색 공급자
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/기본 검색 공급자
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: DefaultSearchProviderImageURL
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"https://search.contoso.com/searchbyimage/upload"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultSearchProviderImageURL
  - 예제 값:
``` xml
<string>https://search.contoso.com/searchbyimage/upload</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultSearchProviderImageURLPostParams
  #### POST를 사용하는 이미지 URL에 대한 매개 변수
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  이 정책을 사용하면 POST를 사용하는 이미지 검색을 수행할 때 사용되는 매개 변수가 지정됩니다. 이 정책은 쉼표로 구분된 이름/값 쌍으로 구성됩니다. 앞의 예제에서 {imageThumbnail}와(과) 같이 값이 템플릿 매개 변수인 경우 실제 이미지 축소판 그림 데이터로 바뀝니다. 이 정책은 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 및 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 정책을 사용하는 경우에만 적용됩니다.

Bing의 이미지 검색 URL 게시 매개 변수를 다음과 같이 지정합니다.
'imageBin={google:imageThumbnailBase64}'.

Google의 이미지 검색 URL 게시 매개 변수를 다음과 같이 지정합니다.
'encoded_image={google:imageThumbnail},image_url={google:imageURL},sbisrc={google:imageSearchSource},original_width={google:imageOriginalWidth},original_height={google:imageOriginalHeight}'.

이 정책을 설정하지 않으면 이미지 검색 요청이 GET 메서드를 사용하여 전송됩니다.

Microsoft Edge 84부터 이 정책을 권장 정책으로 설정할 수 있습니다. 사용자가 이미 기본 검색 공급자를 설정한 경우 이 권장 정책에서 구성한 기본 검색 공급자는 사용자가 선택할 수 있는 검색 공급자 목록에 추가되지 않습니다. 원하는 동작인 경우 [ManagedSearchEngines](#managedsearchengines) 정책을 사용하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultSearchProviderImageURLPostParams
  - GP 이름: POST를 사용하는 이미지 URL에 대한 매개 변수
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/기본 검색 공급자
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/기본 검색 공급자
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: DefaultSearchProviderImageURLPostParams
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"content={imageThumbnail},url={imageURL},sbisrc={SearchSource}"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultSearchProviderImageURLPostParams
  - 예제 값:
``` xml
<string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultSearchProviderKeyword
  #### 기본 검색 공급자 키워드
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  주소 표시줄에서 해당 공급자에 대한 검색을 트리거하는데 사용되는 바로 가기인 키워드를 지정합니다.

이 정책은 선택 사항입니다. 구성하지 않으면 키워드가 검색 공급자를 활성화하지 않습니다.

이 정책은 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 및 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 정책을 사용하는 경우에만 적용됩니다.

Microsoft Edge 84부터 이 정책을 권장 정책으로 설정할 수 있습니다. 사용자가 이미 기본 검색 공급자를 설정한 경우 이 권장 정책에서 구성한 기본 검색 공급자는 사용자가 선택할 수 있는 검색 공급자 목록에 추가되지 않습니다. 원하는 동작인 경우 [ManagedSearchEngines](#managedsearchengines) 정책을 사용하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultSearchProviderKeyword
  - GP 이름: 기본 검색 공급자 키워드
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/기본 검색 공급자
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/기본 검색 공급자
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: DefaultSearchProviderKeyword
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"mis"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultSearchProviderKeyword
  - 예제 값:
``` xml
<string>mis</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultSearchProviderName
  #### 기본 검색 공급자 이름
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  기본 검색 공급자의 이름을 지정합니다.

이 정책을 사용하면 기본 검색 공급자의 이름을 설정할 수 있습니다.

이 정책을 사용하지 않거나 비워두면 검색 URL로 지정된 호스트 이름이 사용됩니다.

'DefaultSearchProviderName'은 DTBC-0008에 설정된 암호화된 검색 공급자에 해당하는, 조직에서 승인한 암호화된 검색 공급자로 설정되어야 합니다. 이 정책은 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 및 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 정책을 사용하는 경우에만 적용됩니다.

Microsoft Edge 84부터 이 정책을 권장 정책으로 설정할 수 있습니다. 사용자가 이미 기본 검색 공급자를 설정한 경우 이 권장 정책에서 구성한 기본 검색 공급자는 사용자가 선택할 수 있는 검색 공급자 목록에 추가되지 않습니다. 원하는 동작인 경우 [ManagedSearchEngines](#managedsearchengines) 정책을 사용하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultSearchProviderName
  - GP 이름: 기본 검색 공급자 이름
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/기본 검색 공급자
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/기본 검색 공급자
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: DefaultSearchProviderName
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"My Intranet Search"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultSearchProviderName
  - 예제 값:
``` xml
<string>My Intranet Search</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultSearchProviderSearchURL
  #### 기본 검색 공급자 검색 URL
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  기본 검색에 사용되는 검색 엔진의 URL을 지정합니다. URL에는 '{searchTerms}' 문자열이 포함되어 있으며 쿼리 시에 사용자가 검색하는 용어로 바뀝니다.

Bing의 검색 URL은 다음과 같이 지정합니다.

'{bing:baseURL}search?q={searchTerms}'.

Google의 검색 URL은 다음과 같이 지정합니다, '{google:baseURL}search?q={searchTerms}&{google:RLZ}{google:originalQueryForSuggestion}{google:assistedQueryStats}{google:searchFieldtrialParameter}{google:searchClient}{google:sourceId}ie={inputEncoding}'.

이 정책은 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 정책을 사용하는 경우에만 필요합니다. 후자의 정책을 사용하지 않으면 이 정책은 무시됩니다.

Microsoft Edge 84부터 이 정책을 권장 정책으로 설정할 수 있습니다. 사용자가 이미 기본 검색 공급자를 설정한 경우 이 권장 정책에서 구성한 기본 검색 공급자는 사용자가 선택할 수 있는 검색 공급자 목록에 추가되지 않습니다. 원하는 동작인 경우 [ManagedSearchEngines](#managedsearchengines) 정책을 사용하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultSearchProviderSearchURL
  - GP 이름: 기본 검색 공급자 검색 URL
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/기본 검색 공급자
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/기본 검색 공급자
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: DefaultSearchProviderSearchURL
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"https://search.contoso.com/search?q={searchTerms}"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultSearchProviderSearchURL
  - 예제 값:
``` xml
<string>https://search.contoso.com/search?q={searchTerms}</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultSearchProviderSuggestURL
  #### 제안에 대한 기본 검색 공급자 URL
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  검색 제안을 제공하는 데 사용되는 검색 엔진의 URL을 지정합니다. URL에는 문자열 '{searchTerms}'이(가) 포함되어 있으며 쿼리 시에 사용자가 지금까지 입력한 텍스트로 바뀝니다.

이 정책은 선택 사항입니다. 구성하지 않으면 사용자에게 검색 제안이 표시되지 않습니다. 검색 기록 및 즐겨찾기에서 제안 사항이 표시됩니다.

Bing의 제안 URL은 다음과 같이 지정될 수 있습니다.

'{bing:baseURL}qbox?query={searchTerms}'.

Google의 제안 URL은 다음과 같이 지정될 수 있습니다: '{google:baseURL}complete/search?output=chrome&q={searchTerms}'.

이 정책은 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 및 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 정책을 사용하는 경우에만 적용됩니다.

Microsoft Edge 84부터 이 정책을 권장 정책으로 설정할 수 있습니다. 사용자가 이미 기본 검색 공급자를 설정한 경우 이 권장 정책에서 구성한 기본 검색 공급자는 사용자가 선택할 수 있는 검색 공급자 목록에 추가되지 않습니다. 원하는 동작인 경우 [ManagedSearchEngines](#managedsearchengines) 정책을 사용하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultSearchProviderSuggestURL
  - GP 이름: 제안에 대한 기본 검색 공급자 URL
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/기본 검색 공급자
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/기본 검색 공급자
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: DefaultSearchProviderSuggestURL
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"https://search.contoso.com/suggest?q={searchTerms}"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultSearchProviderSuggestURL
  - 예제 값:
``` xml
<string>https://search.contoso.com/suggest?q={searchTerms}</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### NewTabPageSearchBox
  #### 새 탭 페이지 검색 상자 환경 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 85 이상

  #### 설명
  검색 상자(권장) 또는 "주소 표시줄"을 사용하여 새 탭에서 검색하도록 새 탭 페이지 검색 상자를 구성할 수 있습니다. 이 정책은 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 및 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)의 두 가지 정책을 설정하여 검색 엔진을 빙 이외의 값으로 설정한 경우에만 작동합니다.

      이 정책을 사용하지 않도록 설정하거나 구성하지 않는 경우:

- 주소 표시줄 기본 검색 엔진이 Bing인 경우 새 탭 페이지는 검색 상자를 사용하여 새 탭을 검색합니다.
- 주소 표시줄 기본 검색 엔진이 Bing이 아닌 경우 새 탭에서 검색할 때 사용자에게 추가 선택권이 제공됩니다("주소 표시줄" 사용).


이 정책을 사용하도록 설정하고 다음

- "검색 상자(권장)"로 설정하면 새 탭 페이지는 검색 상자를 사용하여 새 탭을 검색합니다.
- "주소 표시줄"('redirect'), 새 탭 페이지 검색 상자는 주소 표시줄을 사용하여 새 탭을 검색합니다.

정책 옵션 매핑:

* bing (bing) = 검색 상자(권장)

* redirect (redirect) = 주소 표시줄

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: NewTabPageSearchBox
  - GP 이름: 새 탭 페이지 검색 상자 환경 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/기본 검색 공급자
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/기본 검색 공급자
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: NewTabPageSearchBox
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"bing"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: NewTabPageSearchBox
  - 예제 값:
``` xml
<string>bing</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ## 기본 메시지 policies

  [맨 위로 이동](#microsoft-edge---정책)

  ### NativeMessagingAllowlist
  #### 사용자가 사용할 수 있는 기본 메시징 호스트 제어
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용자가 Microsoft Edge에서 사용할 수 있는 특정 기본 메시징 호스트를 나열합니다.

기본적으로 모든 기본 메시징 호스트가 허용됩니다. [NativeMessagingBlocklist](#nativemessagingblocklist) 정책을 *로 설정하면 모든 기본 메시징 호스트가 차단되며 여기에 나열된 기본 메시징 호스트만 로드됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: NativeMessagingAllowlist
  - GP 이름: 사용자가 사용할 수 있는 기본 메시징 호스트 제어
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/기본 메시지
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\2 = "com.native.messaging.host.name2"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: NativeMessagingAllowlist
  - 예제 값:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### NativeMessagingBlocklist
  #### 기본 메시지 차단 목록 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용할 수 없는 기본 메시징 호스트를 지정합니다.

허용 목록에 명시적으로 나열되어 있지 않는 한 '*'를 사용하여 모든 기본 메시징 호스트를 차단합니다.

이 정책을 구성하지 않으면 Microsoft Edge 는 설치된 모든 기본 메시징 호스트를 로드합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: NativeMessagingBlocklist
  - GP 이름: 기본 메시지 차단 목록 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/기본 메시지
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\2 = "com.native.messaging.host.name2"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: NativeMessagingBlocklist
  - 예제 값:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### NativeMessagingUserLevelHosts
  #### 사용자 수준 기본 메시징 호스트 허용(관리자 권한 없이 설치됨)
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  기본 메시징 호스트의 사용자 수준 설치를 사용하도록 설정합니다.

이 정책을 사용하지 않으면 Microsoft Edge는 시스템 수준에 설치된 기본 메시징 호스트만 사용합니다.

기본적으로 이 정책을 구성하지 않으면 Microsoft Edge는 사용자 수준 기본 메시징 호스트의 사용을 허용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: NativeMessagingUserLevelHosts
  - GP 이름: 사용자 수준 기본 메시징 호스트 허용(관리자 권한 없이 설치됨)
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/기본 메시지
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: NativeMessagingUserLevelHosts
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: NativeMessagingUserLevelHosts
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ## 시작&comma; 홈 페이지 및 새 탭 페이지 policies

  [맨 위로 이동](#microsoft-edge---정책)

  ### HomepageIsNewTabPage
  #### 새 탭 페이지를 홈 페이지로 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge에서 기본 홈 페이지를 구성합니다. 지정한 URL 또는 새 탭 페이지를 홈 페이지를 설정할 수 있습니다.

이 정책을 사용하면 항상 새 탭 페이지가 홈 페이지에 사용되며 홈 페이지 URL 위치는 무시됩니다.

이 정책을 사용하지 않으면 'edge://newtab'으로 설정되어 있지 않는 한 사용자의 홈 페이지 URL는 새 탭 페이지가 될 수 없습니다.

구성하지 않으면 사용자는 새 탭 페이지가 자신의 홈 페이지인지 여부를 선택할 수 있습니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: HomepageIsNewTabPage
  - GP 이름: 새 탭 페이지를 홈 페이지로 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/시작, 홈 페이지 및 새 탭 페이지
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/시작, 홈 페이지 및 새 탭 페이지
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: HomepageIsNewTabPage
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: HomepageIsNewTabPage
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### HomepageLocation
  #### 홈 페이지 URL 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge에서 기본 홈 페이지 URL을 구성합니다.

홈 페이지는 홈 단추에 의해 열리는 페이지입니다. 시작 시 열리는 페이지는 [RestoreOnStartup](#restoreonstartup) 정책에 의해 제어됩니다.

여기에서 URL을 설정하거나 새 탭 페이지를 열도록 홈 페이지를 설정할 수 있습니다. 새 탭 페이지를 열도록 선택하면 이 정책이 적용되지 않습니다.

이 정책을 사용하면 사용자가 홈 페이지 URL을 변경할 수 없지만 새 탭 페이지를 홈 페이지로 사용하도록 선택할 수 있습니다.

이 정책을 사용하지 않거나 구성하지 않으면 [HomepageIsNewTabPage](#homepageisnewtabpage) 정책이 사용하지 않도록 설정된 경우에 한해 사용자가 자신의 홈 페이지를 선택할 수 있습니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: HomepageLocation
  - GP 이름: 홈 페이지 URL 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/시작, 홈 페이지 및 새 탭 페이지
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/시작, 홈 페이지 및 새 탭 페이지
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: HomepageLocation
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"https://www.contoso.com"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: HomepageLocation
  - 예제 값:
``` xml
<string>https://www.contoso.com</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### NewTabPageAllowedBackgroundTypes
  #### 새 탭 페이지 레이아웃에 허용되는 배경 종류 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  Microsoft Edge의 새 탭 페이지 레이아웃에서 허용되는 배경 이미지 유형을 구성할 수 있습니다.

이 정책을 구성하지 않으면 새 탭 페이지의 모든 배경 이미지 유형이 사용하도록 설정됩니다.

정책 옵션 매핑:

* DisableImageOfTheDay (1) = 일상 배경 이미지 종류 이용 안 함

* DisableCustomImage (2) = 사용자 지정 배경 이미지 종류 이용 안 함

* DisableAll (3) = 배경 이미지 종류 모두 이용 안 함

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: NewTabPageAllowedBackgroundTypes
  - GP 이름: 새 탭 페이지 레이아웃에 허용되는 배경 종류 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/시작, 홈 페이지 및 새 탭 페이지
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: NewTabPageAllowedBackgroundTypes
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: NewTabPageAllowedBackgroundTypes
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### NewTabPageCompanyLogo
  #### 새 탭 페이지 회사 로고 설정 (사용하지 않음)
  
  >사용되지 않음: 이 정책은 사용되지 않으며 Microsoft Edge 85 이후에는 작동되지 않습니다.
  #### 지원되는 버전:
  - Windows macOS 79 이후 85

  #### 설명
  이 정책은 운영 요구 사항의 변경으로 인해 예상대로 작동하지 않았습니다. 따라서 더 이상 사용되지 않으며 사용해서는 안됩니다.

Microsoft Edge의 새 탭 페이지에서 사용할 회사 로고를 지정합니다.

정책은 로고를 표현하는 문자열로 구성되어야 합니다(s) JSON 형식으로. 예: { "default_logo": { "url": "https://www.contoso.com/logo.png", "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29" }, "light_logo": { "url": "https://www.contoso.com/light_logo.png", "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737" }}

Microsoft Edge이 로고를 다운로드할 수 있는 URL과 해당 암호화 해시(SHA-256)를 지정하여 이 정책을 구성하며 이 작업은 다운로드의 무결성을 확인하는 데 사용됩니다. 로고는 PNG 또는 SVG 형식이어야 하며 파일 크기는 16MB를 초과할 수 없습니다. 로고는 다운로드 및 캐시되며 URL 또는 해시가 변경될 때마다 다시 다운로드됩니다. URL은 인증없이 액세스할 수 있어야 합니다.

   'default_logo'는 필수 항목이며 배경 이미지가 없을 때 사용됩니다. 'light_logo'가 제공되면 사용자의 새 탭 페이지에 배경 이미지가있을 때 사용됩니다. 투명한 배경이 왼쪽에 정렬되고 세로로 가운데에 배치된 가로 로고를 사용하는 것이 좋습니다. 로고는 최소 높이가 32픽셀이고 가로 세로 비율이 1:1 ~ 4:1이어야 합니다. 'default_logo'는 흰색/검은색 배경과 적절한 대비를 가져야 하며 'light_logo'는 배경 이미지와 적절한 대비를 가져야 합니다.

이 정책을 사용하면 Microsoft Edge이(가) 지정된 로고를 다운로드하여 새 탭 페이지에서 표시합니다(s). 사용자는 로고를 무시하거나 숨길 수 없습니다.

이 정책을 사용 중지하거나 구성하지 않을 경우 Microsoft Edge의 새 탭 페이지에 회사 로고나 Microsoft 로고가 표시되지 않습니다.

SHA-256 해시 결정에 대한 도움말은 https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/get-filehash를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 사전

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: NewTabPageCompanyLogo
  - GP 이름: 새 탭 페이지 회사 로고 설정 (사용하지 않음)
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/시작, 홈 페이지 및 새 탭 페이지
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: NewTabPageCompanyLogo
  - 값 형식: REG_SZ
  ##### 예제 값:
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


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: NewTabPageCompanyLogo
  - 예제 값:
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
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### NewTabPageHideDefaultTopSites
  #### 새 탭 페이지에서 기본 상위 사이트 숨기기
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge의 새 탭 페이지에서 기본 상위 사이트를 숨깁니다.

이 정책을 true로 설정하면 기본 상위 사이트 타일이 숨겨집니다.

이 정책을 false로 설정하거나 구성하지 않으면 기본 상위 사이트 타일이 계속 표시됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: NewTabPageHideDefaultTopSites
  - GP 이름: 새 탭 페이지에서 기본 상위 사이트 숨기기
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/시작, 홈 페이지 및 새 탭 페이지
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: NewTabPageHideDefaultTopSites
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: NewTabPageHideDefaultTopSites
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### NewTabPageLocation
  #### 새 탭 페이지 URL 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  새 탭 페이지에 대한 기본 URL을 구성합니다.

이 정책은 새 탭을 만들 때(새 창을 열 때도 포함) 열리는 페이지를 결정합니다. 새 탭 페이지로 열리도록 설정된 경우 시작 페이지에도 영향을 미칩니다.

이 정책은 시작할 때 열리는 페이지를 결정하지 않습니다. 이는 [RestoreOnStartup](#restoreonstartup) 정책에 의해 제어됩니다. 새 탭 페이지로 열리도록 설정되어 있는 경우에도 홈 페이지에 영향을 주지 않습니다.

이 정책을 구성하지 않으면 기본 새 탭 페이지가 사용됩니다.

이 정책 *및* [NewTabPageSetFeedType](#newtabpagesetfeedtype) 정책을 구성하면 이 정책이 우선합니다.

잘못된 URL을 제공하면 새 탭에서 about://blank로 열립니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: NewTabPageLocation
  - GP 이름: 새 탭 페이지 URL 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/시작, 홈 페이지 및 새 탭 페이지
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/시작, 홈 페이지 및 새 탭 페이지
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: NewTabPageLocation
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"https://www.fabrikam.com"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: NewTabPageLocation
  - 예제 값:
``` xml
<string>https://www.fabrikam.com</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### NewTabPageManagedQuickLinks
  #### 새 탭 페이지 빠른 연결 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 79 이상

  #### 설명
  기본적으로 Microsoft Edge는 검색 기록을 기반으로 사용자가 추가한 바로 가기 및 상위 사이트의 새 탭 페이지에 빠른 링크를 표시합니다. 이 정책을 사용하여 새 탭 페이지에서 JSON 개체로 표시되는 빠른 링크 타일을 3개까지 구성할 수 있습니다.

[ { "url": "https://www.contoso.com", "title": "Contoso Portal", "pinned": true/false }, ... ]

'url' 필드는 필수입니다. 'title' 및 'pinned'는 선택 사항입니다. 'title'이 제공되지 않으면 URL이 기본 제목으로 사용됩니다. 'pinned'가 제공되지 않으면 기본값은 false입니다.

Microsoft Edge는 고정된 모든 타일이 고정되지 않은 타일보다 먼저 표시되는 순서대로 왼쪽에서 오른쪽으로 나열됩니다.

'pinned' 필드가 무시되고 모든 타일이 고정됩니다. 타일은 사용자가 삭제할 수 없으며 항상 빠른 링크 목록 맨 앞에 표시됩니다.

정책을 권장 사항으로 설정하면 고정된 타일은 목록에 남아 있지만 사용자는 이를 편집하고 삭제할 수 있습니다. 고정되지 않은 빠른 링크 타일은 기본 상위 사이트처럼 작동하며 다른 웹 사이트를 더 자주 방문하는 경우 목록에서 제거됩니다. 이 정책을 통해 고정되지 않은 링크를 기존 브라우저 프로필에 적용할 경우 해당 링크는 사용자의 검색 기록과 비교하여 순위에 따라 전혀 표시되지 않을 수도 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 사전

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: NewTabPageManagedQuickLinks
  - GP 이름: 새 탭 페이지 빠른 연결 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/시작, 홈 페이지 및 새 탭 페이지
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/시작, 홈 페이지 및 새 탭 페이지
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: NewTabPageManagedQuickLinks
  - 값 형식: REG_SZ
  ##### 예제 값:
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


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: NewTabPageManagedQuickLinks
  - 예제 값:
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
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### NewTabPagePrerenderEnabled
  #### 더 빠른 렌더링을 위해 새 탭 페이지를 미리 로드할 수 있습니다.
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 85 이상

  #### 설명
  이 정책을 구성하는 경우 새 탭 페이지를 미리 로드할 수 있으며, 사용자는 이 설정을 변경할 수 없습니다. 이 정책을 구성하지 않으면 미리 로드를 사용할 수 있고, 사용자가 이 설정을 변경할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: NewTabPagePrerenderEnabled
  - GP 이름: 더 빠른 렌더링을 위해 새 탭 페이지를 미리 로드할 수 있습니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/시작, 홈 페이지 및 새 탭 페이지
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/시작, 홈 페이지 및 새 탭 페이지
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: NewTabPagePrerenderEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: NewTabPagePrerenderEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### NewTabPageSetFeedType
  #### Microsoft Edge 새 탭 페이지 환경 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 79 이상

  #### 설명
  새 탭 페이지에 대한 Microsoft 뉴스 또는 Office 365 피드 환경을 선택할 수 있습니다.

     이 정책을 'News'(으)로 설정하면 사용자는 새 탭 페이지에서 Microsoft 뉴스 피드 환경을 볼 수 있습니다.

     이 정책을 'Office'(으)로 설정하면 Azure Active Directory 브라우저 로그인이 있는 사용자는 새 탭 페이지에서 Office 365 피드 환경을 볼 수 있습니다.

     이 정책을 사용하지 않거나 구성하지 않는 경우:

- 브라우저 로그인이 Azure Active Directory인 사용자는 Office 365 new 탭 페이지 피드 환경 및 표준 새 탭 페이지 피드 환경을 제공합니다.

      Azure Active Directory 브라우저 로그인이 없는 사용자는 표준 새 탭 페이지 경험을 볼 수 있습니다.

이 정책을 *및* 구성하면 [NewTabPageLocation](#newtabpagelocation) 정책 [NewTabPageLocation](#newtabpagelocation)이(가) 우선합니다.

기본 설정은 다음과 같습니다.  사용할 수 없거나 구성되지 않았습니다.

정책 옵션 매핑:

* News (0) = Microsoft 뉴스 피드 환경

* Office (1) = Office 365 피드 환경

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: NewTabPageSetFeedType
  - GP 이름: Microsoft Edge 새 탭 페이지 환경 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/시작, 홈 페이지 및 새 탭 페이지
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/시작, 홈 페이지 및 새 탭 페이지
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: NewTabPageSetFeedType
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: NewTabPageSetFeedType
  - 예제 값:
``` xml
<integer>0</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### RestoreOnStartup
  #### 시작 시 수행할 작업
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  시작 시 Microsoft Edge의 동작 방식을 지정합니다.

시작 시 항상 새 탭이 열리도록 하려면 'RestoreOnStartupIsNewTabPage’를 선택하세요.

Microsoft Edge가 마지막으로 닫혔을 때 열려 있던 URL을 다시 열려면 'RestoreOnStartupIsLastSession을 선택하세요. 검색 세션이 그대로 복원됩니다. 이 옵션은 세션에 의존하거나 종료 시 작업을 수행하는 일부 설정(예: 종료 시 검색 데이터 지우기 또는 세션 전용 쿠키)을 사용 중지합니다.

특정 URL 집합을 열려면 'URL 목록 열기'(4)를 선택하세요.

이 설정을 사용하지 않으면 구성되지 않은 상태로 유지되는 것과 같습니다. 사용자는 Microsoft Edge에서 변경할 수 있습니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.

정책 옵션 매핑:

* RestoreOnStartupIsNewTabPage (5) = 새 탭 열기

* RestoreOnStartupIsLastSession (1) = 마지막 세션 복원

* RestoreOnStartupIsURLs (4) = URL 목록 열기

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: RestoreOnStartup
  - GP 이름: 시작 시 수행할 작업
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/시작, 홈 페이지 및 새 탭 페이지
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/시작, 홈 페이지 및 새 탭 페이지
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: RestoreOnStartup
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000004
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: RestoreOnStartup
  - 예제 값:
``` xml
<integer>4</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### RestoreOnStartupURLs
  #### 브라우저가 시작될 때 열 사이트
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  브라우저가 시작될 때 자동으로 열 웹 사이트 목록을 지정합니다. 이 정책을 구성하지 않으면 시작할 때 어떤 사이트도 열리지 않습니다.

이 정책은 [RestoreOnStartup](#restoreonstartup) 정책을 'URL 목록 열기'(4)로 설정한 경우에만 작동합니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: RestoreOnStartupURLs
  - GP 이름: 브라우저가 시작될 때 열 사이트
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/시작, 홈 페이지 및 새 탭 페이지
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/시작, 홈 페이지 및 새 탭 페이지
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤\RestoreOnStartupURLs
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\1 = "https://contoso.com"
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\2 = "https://www.fabrikam.com"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: RestoreOnStartupURLs
  - 예제 값:
``` xml
<array>
  <string>https://contoso.com</string>
  <string>https://www.fabrikam.com</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ShowHomeButton
  #### 도구 모음에 홈 버튼 표시
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge의 도구 모음에 홈 버튼을 표시합니다.

항상 홈 버튼을 표시하려면 이 정책을 사용합니다. 버튼을 표시하지 않으려면 사용하지 않도록 설정화합니다.

정책을 구성하지 않으면 사용자가 홈 버튼을 표시할지 여부를 선택할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ShowHomeButton
  - GP 이름: 도구 모음에 홈 버튼 표시
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/시작, 홈 페이지 및 새 탭 페이지
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/시작, 홈 페이지 및 새 탭 페이지
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: ShowHomeButton
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ShowHomeButton
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ## 암호 관리자 및 보호 policies

  [맨 위로 이동](#microsoft-edge---정책)

  ### PasswordManagerEnabled
  #### 암호 관리자에 암호 저장 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge에서 사용자 암호를 저장하도록 설정합니다.

이 정책을 사용하면 사용자가 Microsoft Edge에서 암호를 저장할 수 있습니다. 다음에 사이트를 방문하면 Microsoft Edge에서 자동으로 암호를 입력합니다.

이 정책을 사용하지 않으면 사용자가 새 암호를 저장할 수 없지만 이전에 저장된 암호를 계속 사용할 수 있습니다.

이 정책을 사용하거나 사용하지 않도록 설정하면 Microsoft Edge에서 사용자가 변경하거나 재정의할 수 없습니다. 구성하지 않으면 사용자가 암호를 저장할 수 있을 뿐만 아니라 이 기능을 끌 수도 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PasswordManagerEnabled
  - GP 이름: 암호 관리자에 암호 저장 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/암호 관리자 및 보호
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/암호 관리자 및 보호
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: PasswordManagerEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PasswordManagerEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PasswordMonitorAllowed
  #### 사용자의 암호가 안전하지 않은 경우 사용자에게 알림이 표시되도록 허용
  
  
  #### 지원되는 버전:
  - Windows 85 이상부터

  #### 설명
  Microsoft Edge에서 사용자 암호를 모니터링하도록 허용합니다.

이 정책을 사용하도록 설정하고 사용자가 정책 사용에 동의하면 Microsoft Edge에 저장된 암호가 안전하지 않은 경우 사용자에게 알림이 표시됩니다. Microsoft Edge에서 알림이 표시되고, 이 정보를 설정 > 암호 > 암호 모니터에서도 볼 수 있습니다.

이 정책을 사용하지 않으면 사용자에게 이 기능을 사용하도록 설정할 권한이 있는지 묻는 메시지가 표시되지 않고, 해당 암호를 검사하지 않으며 사용자에게 알림이 표시되지도 않습니다.

정책을 사용하도록 설정하거나 구성하지 않은 경우 사용자가 이 기능을 켜거나 끌 수 있습니다.

Microsoft Edge에서 안전하지 않은 암호를 찾는 방법에 대한 자세한 내용은 다음을 참조하세요. [https://go.microsoft.com/fwlink/?linkid=2133833](https://go.microsoft.com/fwlink/?linkid=2133833)

추가 가이드:

이 정책은 중요 설명선을 사용하긴 하지만 필수 항목뿐만 아니라 권장 항목으로도 모두 설정 가능합니다.

필수 사용: 특정 사용자에 대해 이 기능을 사용하도록 설정하려면 개별 사용자의 동의가 전제 조건임을 고려하면 이 정책에는 필수 사용 설정이 없습니다. 정책을 필수 사용으로 설정하면 설정의 UI가 변경되지 않고 edge://policy에서 다음 오류 메시지가 표시됩니다.

오류 메시지 내용 예: "암호 모니터에서 개별 사용자가 동의해야 하므로 이 정책 값은 무시됩니다. 조직의 사용자에게 설정 > 프로필 > 암호로 이동해 기능을 켜도록 요청할 수 있습니다."

권장 사용: 정책을 권장 사용으로 설정하면 설정의 UI가 '꺼짐' 상태로 유지되지만 이 설명이 표시된 상태에서 마우스를 가져가면 그 옆에 서류 가방 아이콘이 보입니다. - "조직에서 이 설정에 대한 특정 값을 권장하고 사용자는 다른 값을 선택했습니다"

필수 및 권장 사용 안 함: 이러한 두 가지 상태가 모두 정상 작동하고 일반적인 캡션이 사용자에게 표시됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PasswordMonitorAllowed
  - GP 이름: 사용자의 암호가 안전하지 않은 경우 사용자에게 알림이 표시되도록 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/암호 관리자 및 보호
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/암호 관리자 및 보호
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: PasswordMonitorAllowed
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PasswordProtectionChangePasswordURL
  #### 암호 변경 URL 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  암호 변경 URL을 구성합니다(HTTP 및 HTTPS 스키마만 해당).

암호 보호 서비스는 브라우저에서 경고를 표시한 후 사용자를 이 URL로 보내 암호를 변경합니다.

이 정책을 사용하면 암호 보호 서비스가 비밀번호를 변경하기 위해 사용자를 이 URL로 보냅니다.

이 정책을 사용하지 않거나 구성하지 않으면 암호 보호 서비스가 사용자를 암호 변경 URL로 리디렉션하지 않습니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PasswordProtectionChangePasswordURL
  - GP 이름: 암호 변경 URL 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/암호 관리자 및 보호
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: PasswordProtectionChangePasswordURL
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"https://contoso.com/change_password.html"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PasswordProtectionChangePasswordURL
  - 예제 값:
``` xml
<string>https://contoso.com/change_password.html</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PasswordProtectionLoginURLs
  #### 암호 보호 서비스가 암호의 솔티드 해시를 캡처해야 하는 엔터프라이즈 로그인 URL 목록 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge가 암호의 salted 해시를 캡처하여 암호 재사용 감지에 사용해야 하는 엔터프라이즈 로그인 URL 목록을 구성합니다(HTTP 및 HTTPS 스키마만 해당).

이 정책을 사용하면 암호 보호 서비스가 정의된 URL의 암호 지문을 캡처합니다.

이 정책을 사용하지 않거나 구성하지 않으면 암호 지문을 캡처하지 않습니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PasswordProtectionLoginURLs
  - GP 이름: 암호 보호 서비스가 암호의 솔티드 해시를 캡처해야 하는 엔터프라이즈 로그인 URL 목록 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/암호 관리자 및 보호
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\1 = "https://contoso.com/login.html"
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\2 = "https://login.contoso.com"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PasswordProtectionLoginURLs
  - 예제 값:
``` xml
<array>
  <string>https://contoso.com/login.html</string>
  <string>https://login.contoso.com</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PasswordProtectionWarningTrigger
  #### 암호 보호 경고 트리거 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  암호 보호 경고를 트리거할 시기를 제어할 수 있습니다. 암호 보호는 잠재적으로 의심스러운 사이트에서 보호된 암호를 재사용할 때 사용자에게 경고합니다.

[PasswordProtectionLoginURLs](#passwordprotectionloginurls) 및 [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl) 정책을 사용하여 보호할 암호를 구성할 수 있습니다.

예외: [PasswordProtectionLoginURLs](#passwordprotectionloginurls) 및 [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)에 나열된 사이트와 [SmartScreenAllowListDomains](#smartscreenallowlistdomains)에 나열된 사이트에 대한 암호는 암호 보호 경고를 트리거하지 않습니다.

암호 보호 경고s를 표시하지 않으려면 'PasswordProtectionWarningOff'로 설정합니다.

사용자가 목록에 없는 사이트에서 보호된 암호를 다시 사용할 때 암호 보호 경고를 표시하려면 'PasswordProtectionWarningOnPasswordReuse'로 설정합니다.

이 정책을 사용하지 않도록 설정하거나 구성하지 않으면 경고 트리거가 표시되지 않습니다.

정책 옵션 매핑:

* PasswordProtectionWarningOff (0) = 암호 보호 경고가 꺼져 있습니다.

* PasswordProtectionWarningOnPasswordReuse (1) = 암호 다시 사용에 의해 암호 보호 경고가 트리거됨

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PasswordProtectionWarningTrigger
  - GP 이름: 암호 보호 경고 트리거 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/암호 관리자 및 보호
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: PasswordProtectionWarningTrigger
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PasswordProtectionWarningTrigger
  - 예제 값:
``` xml
<integer>1</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ## 인쇄 중 policies

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultPrinterSelection
  #### 기본 프린터 선택 규칙
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge 기본 프린터 선택 규칙을 재정의합니다. 이 정책은 Microsoft Edge에서 사용자가 페이지를 처음 인쇄하려고 할 때 발생하는 기본 프린터를 선택하는 규칙을 결정합니다.

이 정책을 설정하면 Microsoft Edge는 지정된 모든 특성과 일치하는 프린터를 찾으려고 시도하고 기본 프린터로 사용합니다. 기준을 충족하는 프린터가 여러 개인 경우에는 일치하는 첫 번째 프린터가 사용됩니다.

이 정책을 구성하지 않거나 제한 시간 내에 일치하는 프린터가 발견되지 않으면 기본 제공 PDF 프린터 또는 프린터 없음(PDF 프린터를 사용할 수 없는 경우)이 프린터의 기본값으로 설정됩니다.

값은 다음과 같은 스키마를 준수하는 JSON 개체로 구문 분석됩니다. - { "type": "object", "properties": { "idPattern": { "description": "Regular expression to match printer id.", "type": "string" }, "namePattern": { "description": "Regular expression to match printer display name.", "type": "string" } } }

필드를 생략하면 모든 값이 일치함을 의미합니다. 예를 들어 연결을 지정하지 않으면 인쇄 미리 보기가 모든 종류의 로컬 프린터를 검색하기 시작합니다. 정규식 패턴은 JavaScript RegExp 구문을 따라야 하며 일치하는 항목은 대/소문자를 구분합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultPrinterSelection
  - GP 이름: 기본 프린터 선택 규칙
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/인쇄 중
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DefaultPrinterSelection
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"{ \"idPattern\": \".*public\", \"namePattern\": \".*Color\" }"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultPrinterSelection
  - 예제 값:
``` xml
<string>{ "idPattern": ".*public", "namePattern": ".*Color" }</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PrintHeaderFooter
  #### 머리글 및 바닥글 인쇄
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  인쇄 대화 상자에서 '머리글 및 바닥글'을 강제로 켜거나 끌 수 있습니다.

이 정책을 구성하지 않으면 사용자가 머리글 및 바닥글을 인쇄할지 여부를 결정할 수 있습니다.

이 정책을 사용하지 않으면 사용자가 머리글 및 바닥글을 인쇄할 수 없습니다.

이 정책을 사용하면 사용자가 머리글 및 바닥글을 항상 인쇄합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PrintHeaderFooter
  - GP 이름: 머리글 및 바닥글 인쇄
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/인쇄 중
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/인쇄 중
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: PrintHeaderFooter
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PrintHeaderFooter
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PrintPreviewUseSystemDefaultPrinter
  #### 시스템 기본 프린터를 기본 프린터로 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge가 가장 최근에 사용한 프린터 대신 인쇄 미리보기에서 시스템 기본 프린터를 기본 선택으로 사용하도록 지시합니다.

이 정책을 사용하지 않거나 구성하지 않으면 인쇄 미리보기에서 가장 최근에 사용한 프린터를 기본값으로 사용합니다.

이 정책을 사용하면 인쇄 미리보기에서 OS 시스템 기본 프린터를 기본 대상으로 선택합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PrintPreviewUseSystemDefaultPrinter
  - GP 이름: 시스템 기본 프린터를 기본 프린터로 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/인쇄 중
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/인쇄 중
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: PrintPreviewUseSystemDefaultPrinter
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PrintPreviewUseSystemDefaultPrinter
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PrintingEnabled
  #### 인쇄 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge에서 인쇄를 사용하도록 설정하고 사용자가 이 설정을 변경할 수 없게 합니다.

이 정책을 사용하거나 구성하지 않으면 사용자가 인쇄할 수 있습니다.

이 정책을 사용하지 않으면 사용자가 Microsoft Edge에서 인쇄를 할 수 없습니다. 공구 모양 메뉴, 확장, JavaScript 응용 프로그램 등에서 인쇄 기능을 사용할 수 없습니다. 사용자는 인쇄하는 동안 Microsoft Edge를 무시하는 플러그 인에서 계속 인쇄할 수 있습니다. 예를 들어 특정 Adobe Flash 응용 프로그램은 상황에 맞는 메뉴에 이 정책에서 다루지 않는 인쇄 옵션이 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PrintingEnabled
  - GP 이름: 인쇄 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/인쇄 중
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: PrintingEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PrintingEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PrintingPaperSizeDefault
  #### 기본 인쇄 페이지 크기
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  기본 인쇄 페이지 크기를 재정의합니다.

name은 나열된 형식 중 하나를 포함하거나 필요한 용지 크기가 목록에 없는 경우 'custom’을 포함해야 합니다. 'custom' 값을 제공하는 경우 custom_size 속성을 지정해야 합니다. 이는 원하는 높이와 너비(마이크로미터)를 설명합니다. 그렇지 않으면 custom_size 속성을 지정하면 안 됩니다. 이 규칙을 위반하는 정책은 무시됩니다.

사용자가 선택한 프린터에서 해당 페이지 크기를 사용할 수 없으면 이 정책이 무시됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 사전

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PrintingPaperSizeDefault
  - GP 이름: 기본 인쇄 페이지 크기
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/인쇄 중
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: PrintingPaperSizeDefault
  - 값 형식: REG_SZ
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\PrintingPaperSizeDefault = {
  "custom_size": {
    "height": 297000, 
    "width": 210000
  }, 
  "name": "custom"
}
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PrintingPaperSizeDefault
  - 예제 값:
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
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### UseSystemPrintDialog
  #### 시스템 대화 상자를 사용하여 인쇄
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  인쇄 미리보기 대신 시스템 인쇄 대화 상자를 표시합니다.

이 정책을 사용하면 Microsoft Edge는 사용자가 페이지를 인쇄할 때 기본 제공되는 인쇄 미리 보기 대신 시스템 인쇄 대화 상자를 엽니다.

이 정책을 구성하지 않거나 사용하지 않으면 인쇄 명령이 Microsoft Edge 인쇄 미리 보기 화면을 트리거합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: UseSystemPrintDialog
  - GP 이름: 시스템 대화 상자를 사용하여 인쇄
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/인쇄 중
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: UseSystemPrintDialog
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: UseSystemPrintDialog
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ## 콘텐츠 설정 policies

  [맨 위로 이동](#microsoft-edge---정책)

  ### AutoSelectCertificateForUrls
  #### 이 사이트에 대한 클라이언트 인증서 자동 선택
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사이트에서 요청할 경우 Microsoft Edge가 자동으로 클라이언트 인증서를 선택해야 하는 URL 패턴에 따라 사이트 목록을 지정합니다.

값은 문자열로 묶은 JSON 사전의 배열이어야 합니다. 각 사전의 형식은 { "pattern": "$URL_PATTERN", "filter" : $FILTER } 이어야 합니다. 여기서 $URL_PATTERN은 콘텐츠 설정 패턴입니다. $FILTER는 브라우저가 자동으로 선택할 수 있는 클라이언트 인증서를 제한합니다. 필터와는 별도로 서버의 인증서 요청과 일치하는 인증서만 선택됩니다. 예를 들어 $FILTER형식이 { "ISSUER": { "CN": "$ISSUER_CN" } }이면 CommonName $ISSUER_CN이 있는 인증서에서 발급한 클라이언트 인증서만 선택됩니다. $FILTER에 "ISSUER" 및 "SUBJECT" 섹션이 포함되어 있으면 클라이언트 인증서가 두 조건을 모두 충족해야 선택됩니다. $FILTER가 조직("O")을 지정하면 인증서에 지정된 값과 일치하는 조직이 하나 이상 있어야 합니다. $FILTER가 조직 단위("OU")를 지정하면 인증서에 지정된 값과 일치하는 조직 단위가 하나 이상 있어야 합니다. $FILTER가 빈 사전 {}이면 클라이언트 인증서 선택이 추가로 제한되지 않습니다.

이 정책을 구성하지 않으면 모든 사이트에 대해 자동 선택이 수행되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AutoSelectCertificateForUrls
  - GP 이름: 이 사이트에 대한 클라이언트 인증서 자동 선택
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls\1 = "{\"pattern\":\"https://www.contoso.com\",\"filter\":{\"ISSUER\":{\"CN\":\"certificate issuer name\", \"L\": \"certificate issuer location\", \"O\": \"certificate issuer org\", \"OU\": \"certificate issuer org unit\"}, \"SUBJECT\":{\"CN\":\"certificate subject name\", \"L\": \"certificate subject location\", \"O\": \"certificate subject org\", \"OU\": \"certificate subject org unit\"}}}"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AutoSelectCertificateForUrls
  - 예제 값:
``` xml
<array>
  <string>{"pattern":"https://www.contoso.com","filter":{"ISSUER":{"CN":"certificate issuer name", "L": "certificate issuer location", "O": "certificate issuer org", "OU": "certificate issuer org unit"}, "SUBJECT":{"CN":"certificate subject name", "L": "certificate subject location", "O": "certificate subject org", "OU": "certificate subject org unit"}}}</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### CookiesAllowedForUrls
  #### 특정 사이트에서 쿠키 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  URL 패턴을 기반으로 쿠키를 설정하도록 허용하는 사이트 목록을 정의합니다.

이 정책을 구성하지 않으면 [DefaultCookiesSetting](#defaultcookiessetting) 정책(설정된 경우) 또는 사용자의 개인 구성의 전역 기본값이 모든 사이트에 사용됩니다.

자세한 내용은 [CookiesBlockedForUrls](#cookiesblockedforurls) 및 [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) 정책을 참조하세요.

다음 세 가지 정책 사이에는 충돌하는 URL 패턴이 설정될 수 없다는 점에 유의하세요.

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- CookiesAllowedForUrls

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

종료 시 쿠키를 삭제하지 않으려면 [SaveCookiesOnExit](#savecookiesonexit) 정책을 구성하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: CookiesAllowedForUrls
  - GP 이름: 특정 사이트에서 쿠키 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: CookiesAllowedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### CookiesBlockedForUrls
  #### 특정 사이트에서 쿠키 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  URL 패턴을 기반으로, 쿠키를 설정할 수 없는 사이트 목록을 정의합니다.

이 정책을 구성하지 않으면 [DefaultCookiesSetting](#defaultcookiessetting) 정책(설정된 경우) 또는 사용자의 개인 구성에 있는 전역 기본값이 모든 사이트에 사용됩니다.

자세한 내용은 [CookiesAllowedForUrls](#cookiesallowedforurls) 및 '[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) 정책을 참조하세요.

참고: 다음 세 가지 정책 사이에는 충돌하는 URL 패턴이 설정될 수 없습니다.

- CookiesBlockedForUrls

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: CookiesBlockedForUrls
  - GP 이름: 특정 사이트에서 쿠키 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: CookiesBlockedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### CookiesSessionOnlyForUrls
  #### 특정 웹 사이트의 쿠키를 현재 세션으로 제한
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  세션이 종료될 때(창이 닫힐 때) 정의한 URL 패턴과 일치하는 웹 사이트에서 만든 쿠키는 삭제됩니다.

패턴과 일치하지 않는 웹 사이트에서 만든 [DefaultCookiesSetting](#defaultcookiessetting) 정책(설정된 경우) 또는 사용자의 개인 구성에 의해 제어됩니다. 이 정책을 구성하지 경우의 기본 동작이기도 합니다.

Microsoft Edge가 백그라운드 모드에서 실행되고 있는 경우 마지막 창이 닫힐 때 세션이 닫히지 않을 수 있습니다. 즉, 창이 닫힐 때 쿠키가 지워지지 않습니다. Microsoft Edge가 백그라운드 모드에서 실행될 때 수행되는 작업을 구성하는 방법에 대한 자세한 내용은 [BackgroundModeEnabled](#backgroundmodeenabled) 정책을 참조하세요.

[CookiesAllowedForUrls](#cookiesallowedforurls) 및 [CookiesBlockedForUrls](#cookiesblockedforurls) 정책을 사용하여 쿠키를 만들 수 있는 웹 사이트를 제어할 수도 있습니다.

참고: 다음 세 가지 정책 사이에 충돌하는 URL 패턴이 설정되어 있으면 안 됩니다.

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- CookiesSessionOnlyForUrls

If you set the [RestoreOnStartup](#restoreonstartup) 정책을 설정하여 이전 세션의 URL을 복원하면 이 정책은 무시되며 해당 사이트에 대한 쿠키가 영구적으로 저장됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: CookiesSessionOnlyForUrls
  - GP 이름: 특정 웹 사이트의 쿠키를 현재 세션으로 제한
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: CookiesSessionOnlyForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultCookiesSetting
  #### 쿠키 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  웹 사이트가 사용자 장치에 쿠키를 만들 수 있는지 여부를 제어합니다. 이 정책은 모두 또는 아무것도 아닙니다. 모든 웹 사이트에서 쿠키를 만들거나 웹 사이트에서 쿠키를 만들 수 없습니다. 이 정책을 사용하여 특정 웹 사이트의 쿠키를 실행할 수 없습니다.

 정책을 '세션'으로 설정합니다.세션이 종료될 때 쿠키를 지웁니다. Microsoft Edge이(가) 백그라운드 모드로 실행되고 있는 경우 마지막 창이 닫힐 때 세션이 닫히지 않을 수 있습니다. 즉, 창이 닫힐 때 쿠키가 지워지지 않습니다. Microsoft Edge이(가) 백그라운드 모드에서 실행될 때 수행되는 작업을 구성하는 방법에 대한 자세한 내용은 [BackgroundModeEnabled](#backgroundmodeenabled) 정책을 참조합니다.

이 정책을 구성하지 않으면 기본 'AllowCookies'가 사용되며 사용자는 Microsoft Edge 설정에서 이 설정을 변경할 수 있습니다. 사용자가 이 설정을 변경할 수 없도록 하려면 정책을 설정합니다.

정책 옵션 매핑:

* AllowCookies (1) = 모든 사이트에서 쿠키를 만들도록 허용

* BlockCookies (2) = 모든 사이트에서 쿠키를 만들도록 허용하지 않음

* SessionOnly (4) = [SaveCookiesOnExit](#savecookiesonexit)에 나열된 항목을 제외하고 세션 기간에 대한 쿠키를 유지합니다.

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultCookiesSetting
  - GP 이름: 쿠키 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DefaultCookiesSetting
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultCookiesSetting
  - 예제 값:
``` xml
<integer>1</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultFileSystemReadGuardSetting
  #### 읽기용 파일 시스템 API의 사용 제어
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  이 정책을 3으로 설정하면 웹 사이트에서 파일 시스템 API를 사용하여 호스트 운영 체제의 파일 시스템에 대한 읽기 권한을 요청할 수 있습니다. 이 정책을 2로 설정하면 액세스가 거부됩니다.

이 정책을 설정하지 않으면 웹 사이트에서 액세스를 요청할 수 있습니다. 사용자는 이 설정을 변경할 수 있습니다.

정책 옵션 매핑:

* BlockFileSystemRead (2) = 사이트에서 파일 시스템 API를 통해 파일 및 디렉터리에 대한 읽기 권한을 요청하는 것을 허용 안 함

* AskFileSystemRead (3) = 사이트에서 사용자에게 파일 시스템 API를 통해 파일 및 디렉터리에 대한 읽기 권한을 부여하도록 요청하는 것을 허용

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultFileSystemReadGuardSetting
  - GP 이름: 읽기용 파일 시스템 API의 사용 제어
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DefaultFileSystemReadGuardSetting
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultFileSystemReadGuardSetting
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultFileSystemWriteGuardSetting
  #### 쓰기용 파일 시스템 API의 사용 제어
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  이 정책을 3으로 설정하면 웹 사이트에서 파일 시스템 API를 사용하여 호스트 운영 체제의 파일 시스템에 대한 쓰기 권한을 요청할 수 있습니다. 이 정책을 2로 설정하면 액세스가 거부됩니다.

이 정책을 설정하지 않으면 웹 사이트에서 액세스를 요청할 수 있습니다. 사용자는 이 설정을 변경할 수 있습니다.

정책 옵션 매핑:

* BlockFileSystemWrite (2) = 사이트에서 파일 및 디렉터리에 대한 쓰기 권한을 요청하는 것을 허용 안 함

* AskFileSystemWrite (3) = 사이트에서 사용자에게 파일 및 디렉터리에 대한 쓰기 권한을 부여하도록 요청하는 것을 허용

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultFileSystemWriteGuardSetting
  - GP 이름: 쓰기용 파일 시스템 API의 사용 제어
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DefaultFileSystemWriteGuardSetting
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultFileSystemWriteGuardSetting
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultGeolocationSetting
  #### 기본 지리적 위치 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  웹 사이트가 사용자의 실제 위치를 추적할 수 있는지 여부를 설정합니다. 기본적으로 추적('AllowGeolocation')을 허용하거나, 기본적으로 추적을 거부('BlockGeolocation')하거나, 웹 사이트가 위치를 요청할 때마다 사용자에게 요청할 수 있습니다('AskGeolocation').

이 정책을 구성하지 않으면 'AskGeolocation'이 사용되고 사용자가 변경할 수 있습니다.

정책 옵션 매핑:

* AllowGeolocation (1) = 사이트에서 사용자의 실제 위치를 추적하도록 허용

* BlockGeolocation (2) = 모든 사이트에서 사용자의 실제 위치를 추적하는 것을 허용 안 함

* AskGeolocation (3) = 사이트에서 사용자의 실제 위치를 추적하려고 할 때마다 묻기

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultGeolocationSetting
  - GP 이름: 기본 지리적 위치 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DefaultGeolocationSetting
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultGeolocationSetting
  - 예제 값:
``` xml
<integer>1</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultImagesSetting
  #### 기본 이미지 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  웹 사이트에서 이미지를 표시할 수 있는지 여부를 설정합니다. 모든 사이트에서 이미지를 허용하거나('AllowImages') 모든 사이트에서 차단할 수 있습니다('BlockImages').

이 정책을 구성하지 않으면 이미지가 기본적으로 허용되며 사용자가 이 설정을 변경할 수 있습니다.

정책 옵션 매핑:

* AllowImages (1) = 모든 사이트에서 모든 이미지를 표시하도록 허용

* BlockImages (2) = 모든 사이트에서 이미지를 표시하는 것을 허용 안 함

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultImagesSetting
  - GP 이름: 기본 이미지 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DefaultImagesSetting
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultImagesSetting
  - 예제 값:
``` xml
<integer>1</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultInsecureContentSetting
  #### 안전하지 않은 콘텐츠 예외 사용 제어
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 80 이상

  #### 설명
  사용자가 예외를 추가하여 특정 사이트에 대한 혼합 콘텐츠를 허용할 수 있는지 여부를 설정할 수 있습니다.

이 정책은 [InsecureContentAllowedForUrls](#insecurecontentallowedforurls) 및 [InsecureContentBlockedForUrls](#insecurecontentblockedforurls) 정책을 사용하여 특정 URL 패턴에 대해 이 정책을 재정의할 수 있습니다.

정책을 설정하지 않으면 사용자는 차단 가능한 혼합 콘텐츠를 허용하고 선택적으로 차단 가능한 혼합 콘텐츠에 대한 자동 업그레이드를 사용하지 않도록 설정하는 예외를 추가할 수 있습니다.

정책 옵션 매핑:

* BlockInsecureContent (2) = 모든 사이트에서 혼합 컨텐츠를 로드하는 것을 허용 안 함

* AllowExceptionsInsecureContent (3) = 사용자가 혼합 콘텐츠를 허용하는 예외를 추가할 수 있도록 허용

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultInsecureContentSetting
  - GP 이름: 안전하지 않은 콘텐츠 예외 사용 제어
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DefaultInsecureContentSetting
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultInsecureContentSetting
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultJavaScriptSetting
  #### 기본 JavaScript 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  웹 사이트에서 JavaScript를 실행할 수 있는지 여부를 설정합니다. 모든 사이트에 대해 허용('AllowJavaScript')하거나 모든 사이트에 대해 차단('BlockJavaScript')할 수 있습니다.

이 정책을 구성하지 않으면 모든 사이트에서 기본적으로 JavaScript를 실행할 수 있으며 사용자가 이 설정을 변경할 수 있습니다.

정책 옵션 매핑:

* AllowJavaScript (1) = 모든 사이트에서 JavaScript 실행 허용

* BlockJavaScript (2) = 모든 사이트에 JavaScript 실행 허용 안 함

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultJavaScriptSetting
  - GP 이름: 기본 JavaScript 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DefaultJavaScriptSetting
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultJavaScriptSetting
  - 예제 값:
``` xml
<integer>1</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultNotificationsSetting
  #### 기본 알림 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  웹 사이트에서 데스크톱 알림을 표시할 수 있는지 여부를 설정합니다. 기본적으로 허용('AllowNotification')'을 허용하거나, 기본적으로 거부('BlockNotification')하거나, 웹 사이트에서 알림을 표시하려는 경우('AskNotification')를 사용자에게 묻도록 할 수 있습니다.

이 정책을 구성하지 않으면 기본적으로 알림이 허용되며 사용자가 이 설정을 변경할 수 있습니다.

정책 옵션 매핑:

* AllowNotifications (1) = 사이트에서 데스크톱 알림을 표시하도록 허용

* BlockNotifications (2) = 모든 사이트에서 바탕 화면 알림을 표시하는 것을 허용 안 함

* AskNotifications (3) = 사이트에서 데스크톱 알림을 표시하려고 할 때마다 묻기

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultNotificationsSetting
  - GP 이름: 기본 알림 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DefaultNotificationsSetting
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultNotificationsSetting
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultPluginsSetting
  #### 기본 Adobe Flash 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  [PluginsAllowedForUrls](#pluginsallowedforurls) 및 [PluginsBlockedForUrls](#pluginsblockedforurls)을(를) 먼저 확인한 다음 이 정책을 확인합니다. 옵션은 'ClickToPlay' 및 'BlockPlugins'입니다. 이 정책을 'BlockPlugins'로 설정하면 모든 웹 사이트에서 이 플러그인이 거부됩니다. 'ClickToPlay'는 Flash 플러그인이 실행되도록 허용하지만 사용자는 자리 표시자를 눌러 플러그인을 시작합니다.

이 정책을 설정하지 않으면 BlockPlugins 정책을 사용하고 사용자가 이 설정을 변경할 수 있습니다.

참고: 자동 재생은 [PluginsAllowedForUrls](#pluginsallowedforurls) 정책에 명시적으로 나열된 도메인에 대해서만 가능합니다. 모든 사이트에 대해 자동 재생을 설정하려면 허용된 URL 목록에 http://* 및 https://*를 추가합니다.

정책 옵션 매핑:

* BlockPlugins (2) = Adobe Flash 플러그 인 차단

* ClickToPlay (3) = 클릭하여 재생

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultPluginsSetting
  - GP 이름: 기본 Adobe Flash 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DefaultPluginsSetting
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultPluginsSetting
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultPopupsSetting
  #### 기본 팝업 창 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  웹 사이트에서 팝업 창을 표시할 수 있는지 여부를 설정합니다. 모든 웹 사이트('팝업 허용')에서 허용하거나 모든 사이트에서 차단('BlockPopups')할 수 있습니다.

이 정책을 구성하지 않으면 팝업 창이 기본적으로 차단되며 사용자가 이 설정을 변경할 수 있습니다.

정책 옵션 매핑:

* AllowPopups (1) = 모든 사이트에서 팝업 표시 허용

* BlockPopups (2) = 모든 사이트에서 팝업 표시 허용 안 함

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultPopupsSetting
  - GP 이름: 기본 팝업 창 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DefaultPopupsSetting
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultPopupsSetting
  - 예제 값:
``` xml
<integer>1</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultWebBluetoothGuardSetting
  #### Bluetooth 웹 API의 사용 제어
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  웹 사이트가 근처의 Bluetooth 장치에 액세스할 수 있는지 여부를 제어합니다. 액세스를 완전히 차단하거나 사이트에서 Bluetooth 장치에 액세스할 때마다 사용자에게 요청하도록 요구할 수 있습니다.

이 정책을 구성하지 않으면 기본값('AskWebBluetooth(매번 사용자에게 물어본다는 의미))이 사용되고 사용자가 변경할 수 있습니다.

정책 옵션 매핑:

* BlockWebBluetooth (2) = 모든 사이트에서 웹 Bluetooth API를 통해 Bluetooth 장치에 대한 액세스를 요청하는 것을 허용 안 함

* AskWebBluetooth (3) = 사이트에서 근처의 Bluetooth 장치에 대한 액세스 권한을 사용자에게 요청하는 것을 허용

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultWebBluetoothGuardSetting
  - GP 이름: Bluetooth 웹 API의 사용 제어
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DefaultWebBluetoothGuardSetting
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultWebBluetoothGuardSetting
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultWebUsbGuardSetting
  #### WebUSB API의 사용 제어
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  웹 사이트가 연결된 USB 장치에 액세스할 수 있는지 여부를 설정합니다. 웹 사이트에서 연결된 USB 장치에 액세스할 때마다 액세스를 완전히 차단하거나 사용자에게 요청할 수 있습니다.

      특정 URL 패턴에 대해 [WebUsbAskForUrls](#webusbaskforurls) 및 [WebUsbBlockedForUrls](#webusbblockedforurls) 정책을 사용하여 이 정책을 재정의할 수 있습니다.

이 정책을 구성하지 않으면 사이트에서 기본적으로 연결된 USB 디바이스('AskWebUb')에 액세스할 수 있는지 여부를 사용자에게 묻고 사용자가 이 설정을 변경할 수 있습니다.

정책 옵션 매핑:

* BlockWebUsb (2) = 모든 사이트에서 WebUSB API를 통해 USB 장치에 대한 액세스를 요청하는 것을 허용 안 함

* AskWebUsb (3) = 사이트에서 연결된 USB 장치에 대한 액세스 권한을 사용자에게 요청하는 것을 허용

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultWebUsbGuardSetting
  - GP 이름: WebUSB API의 사용 제어
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DefaultWebUsbGuardSetting
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultWebUsbGuardSetting
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### FileSystemReadAskForUrls
  #### 이 사이트에서 파일 시스템 API를 통한 읽기 권한 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  이 정책을 설정하면 사용자에게 파일 시스템 API를 통해 호스트 운영 체제의 파일이나 디렉터리에 대한 읽기 권한을 부여하도록 요청할 수 있는 사이트를 지정하는 URL 패턴을 나열할 수 있습니다.

이 정책을 설정하지 않으면 설정된 경우 모든 사이트에 [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)이 적용됩니다. 그렇지 않으면 사용자의 개인 설정이 적용됩니다.

URL 패턴은 [FileSystemReadBlockedForUrls](#filesystemreadblockedforurls)와 충돌할 수 없습니다. URL이 둘 다와 일치하면 두 정책 모두 우선하지 않습니다.

유효한 url 패턴에 대한 자세한 내용은 https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: FileSystemReadAskForUrls
  - GP 이름: 이 사이트에서 파일 시스템 API를 통한 읽기 권한 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\2 = "[*.]example.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: FileSystemReadAskForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### FileSystemReadBlockedForUrls
  #### 이 사이트에서 파일 시스템 API를 통한 읽기 권한 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  이 정책을 설정하면 사용자에게 파일 시스템 API를 통해 호스트 운영 체제의 파일이나 디렉터리에 대한 읽기 권한을 부여하도록 요청할 수 없는 사이트를 지정하는 URL 패턴을 나열할 수 있습니다.

이 정책을 설정하지 않으면 설정된 경우 모든 사이트에 [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)이 적용됩니다. 그렇지 않으면 사용자의 개인 설정이 적용됩니다.

URL 패턴은 [FileSystemReadAskForUrls](#filesystemreadaskforurls)와 충돌할 수 없습니다. URL이 둘 다와 일치하면 두 정책 모두 우선하지 않습니다.

유효한 url 패턴에 대한 자세한 내용은 https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: FileSystemReadBlockedForUrls
  - GP 이름: 이 사이트에서 파일 시스템 API를 통한 읽기 권한 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\2 = "[*.]example.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: FileSystemReadBlockedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### FileSystemWriteAskForUrls
  #### 이 사이트의 파일 및 디렉터리에 대한 쓰기 권한 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  이 정책을 설정하면 사용자에게 호스트 운영 체제의 파일 시스템에 있는 파일이나 디렉터리에 대한 쓰기 권한을 부여하도록 요청할 수 있는 사이트를 지정하는 URL 패턴을 나열할 수 있습니다.

이 정책을 설정하지 않으면 설정된 경우 모든 사이트에 [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)이 적용됩니다. 그렇지 않으면 사용자의 개인 설정이 적용됩니다.

URL 패턴은 [FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls)와 충돌할 수 없습니다. URL이 둘 다와 일치하면 두 정책 모두 우선하지 않습니다.

유효한 url 패턴에 대한 자세한 내용은 https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: FileSystemWriteAskForUrls
  - GP 이름: 이 사이트의 파일 및 디렉터리에 대한 쓰기 권한 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\2 = "[*.]example.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: FileSystemWriteAskForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### FileSystemWriteBlockedForUrls
  #### 이 사이트의 파일 및 디렉터리에 대한 쓰기 권한 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  이 정책을 설정하면 사용자에게 호스트 운영 체제의 파일 시스템에 있는 파일이나 디렉터리에 대한 쓰기 권한을 부여하도록 요청할 수 없는 사이트를 지정하는 URL 패턴을 나열할 수 있습니다.

이 정책을 설정하지 않으면 설정된 경우 모든 사이트에 [DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)이 적용됩니다. 그렇지 않으면 사용자의 개인 설정이 적용됩니다.

URL 패턴은 [FileSystemWriteAskForUrls](#filesystemwriteaskforurls)와 충돌할 수 없습니다. URL이 둘 다와 일치하면 두 정책 모두 우선하지 않습니다.

유효한 url 패턴에 대한 자세한 내용은 https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: FileSystemWriteBlockedForUrls
  - GP 이름: 이 사이트의 파일 및 디렉터리에 대한 쓰기 권한 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\2 = "[*.]example.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: FileSystemWriteBlockedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ImagesAllowedForUrls
  #### 이 사이트의 이미지 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  URL 패턴을 기반으로, 이미지를 표시할 수 있는 사이트 목록을 정의합니다.

이 정책을 구성하지 않으면 [DefaultImagesSetting](#defaultimagessetting) 정책(설정된 경우) 또는 사용자의 개인 구성에 있는 전역 기본값이 모든 사이트에 사용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ImagesAllowedForUrls
  - GP 이름: 이 사이트의 이미지 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ImagesAllowedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ImagesBlockedForUrls
  #### 특정 사이트에서 이미지 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  URL 패턴을 기반으로, 이미지 표시가 허용되지 않는 사이트 목록을 정의합니다.

이 정책을 구성하지 않으면 [DefaultImagesSetting](#defaultimagessetting) 정책(경우 설정) 또는 사용자의 개인 구성에 있는 전역 기본값이 모든 사이트에 사용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ImagesBlockedForUrls
  - GP 이름: 특정 사이트에서 이미지 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ImagesBlockedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### InsecureContentAllowedForUrls
  #### 지정된 사이트에서 안전하지 않은 콘텐츠 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 80 이상

  #### 설명
  안전하지 않은 혼합 콘텐츠(즉, HTTPS 사이트의 HTTP 콘텐츠)를 표시할 수 있는 사이트를 지정하는 URL 패턴 목록을 만듭니다.

이 정책을 구성하지 않으면 차단 가능한 혼합 콘텐츠가 차단되고 선택적으로 차단 가능한 혼합 콘텐츠가 업그레이드되지만, 사용자는 특정 사이트에 대해 안전하지 않은 혼합 콘텐츠를 허용하도록 예외를 설정할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: InsecureContentAllowedForUrls
  - GP 이름: 지정된 사이트에서 안전하지 않은 콘텐츠 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\2 = "[*.]example.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: InsecureContentAllowedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### InsecureContentBlockedForUrls
  #### 지정된 사이트에서 안전하지 않은 콘텐츠 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 80 이상

  #### 설명
  차단 가능한(활성) 혼합 콘텐츠(즉, HTTPS 사이트의 HTTP 콘텐츠)를 표시할 수 없고 선택적으로 차단 가능한 혼합 콘텐츠 업그레이드를 사용하지 않도록 설정할 사이트를 지정하는 URL 패턴 목록을 만듭니다.

이 정책을 구성하지 않으면 차단 가능한 혼합 콘텐츠가 차단되고 선택적으로 차단 가능한 혼합 콘텐츠가 업그레이드되지만, 사용자는 특정 사이트에 대해 안전하지 않은 혼합 콘텐츠를 허용하도록 예외를 설정할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: InsecureContentBlockedForUrls
  - GP 이름: 지정된 사이트에서 안전하지 않은 콘텐츠 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\2 = "[*.]example.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: InsecureContentBlockedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### JavaScriptAllowedForUrls
  #### 특정 사이트에서 JavaScript 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  URL 패턴을 기반으로, JavaScript 실행이 허용되는 사이트 목록을 정의합니다.

이 정책을 구성하지 [DefaultJavaScriptSetting](#defaultjavascriptsetting) 정책(설정된 경우) 또는 사용자의 개인 구성에 있는 전역 기본값이 모든 사이트에 사용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: JavaScriptAllowedForUrls
  - GP 이름: 특정 사이트에서 JavaScript 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: JavaScriptAllowedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### JavaScriptBlockedForUrls
  #### 특정 사이트에서 JavaScript 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  URL 패턴을 기반으로, JavaScript 실행이 허용되지 않는 사이트 목록을 정의합니다.

이 정책을 구성하지 않으면 [DefaultJavaScriptSetting](#defaultjavascriptsetting) 정책(설정된 경우) 또는 사용자의 개인 구성에 있는 전역 기본값이 모든 사이트에 사용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: JavaScriptBlockedForUrls
  - GP 이름: 특정 사이트에서 JavaScript 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: JavaScriptBlockedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### LegacySameSiteCookieBehaviorEnabled
  #### 기본 레거시 SameSite 쿠키 동작 설정 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 80 이상

  #### 설명
  모든 쿠키를 기존 SameSite 동작으로 되돌릴 수 있습니다. 레거시 동작으로 되돌리면 SameSite 속성을 지정하지 않은 쿠키가 "SameSite=None"인 것처럼 처리되고 "SameSite=None" 쿠키가 "Secure" 특성을 운반할 필요가 없습니다.

이 정책을 설정하지 않으면 SameSite 특성을 지정하지 않은 쿠키의 기본 동작이 SameSite-by-default 기능에 대한 다른 구성 소스에 종속됩니다. 이 기능은 현장 평가판 또는 edge://flags에서 same-site-by-default-cookies 플래그를 사용하도록 설정하여 설정할 수 있습니다.

정책 옵션 매핑:

* DefaultToLegacySameSiteCookieBehavior (1) = 모든 사이트의 쿠키에 대해 레거시 SameSite 동작으로 되돌리기

* DefaultToSameSiteByDefaultCookieBehavior (2) = 모든 사이트의 쿠키에 대해 SameSite-by-default 동작 사용

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: LegacySameSiteCookieBehaviorEnabled
  - GP 이름: 기본 레거시 SameSite 쿠키 동작 설정 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: LegacySameSiteCookieBehaviorEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: LegacySameSiteCookieBehaviorEnabled
  - 예제 값:
``` xml
<integer>1</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### LegacySameSiteCookieBehaviorEnabledForDomainList
  #### 지정된 사이트의 쿠키에 대해 레거시 SameSite 동작으로 되돌리기
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 80 이상

  #### 설명
  지정된 패턴과 일치하는 도메인에 대해 설정된 쿠키는 레거시 SameSite 동작으로 되돌아갑니다.

레거시 동작으로 되돌리면 SameSite 특성을 지정하지 않는 쿠키가 "SameSite=None"처럼 처리되고 "Secure" 특성을 실행하는 "SameSite=None" 쿠키에 대한 요구 사항이 제거됩니다.

이 정책을 설정하지 않으면 전역 기본값이 사용됩니다. 전역 기본값은 지정한 패턴이 적용되지 않는 도메인의 쿠키에도 사용됩니다.

전역 기본값은 [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) 정책을 사용하여 구성할 수 있습니다. [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)이(가) 설정되지 않은 경우 전역 기본값은 다른 구성 원본으로 돌아갑니다.

이 정책에 나열되는 패턴은 URL이 아닌 도메인으로 간주되므로 스키마나 포트를 지정하지 않아야 합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: LegacySameSiteCookieBehaviorEnabledForDomainList
  - GP 이름: 지정된 사이트의 쿠키에 대해 레거시 SameSite 동작으로 되돌리기
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\1 = "www.example.com"
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\2 = "[*.]example.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: LegacySameSiteCookieBehaviorEnabledForDomainList
  - 예제 값:
``` xml
<array>
  <string>www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### NotificationsAllowedForUrls
  #### 특정 사이트에서 알림 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사이트에서 알림이 표시되도록 지정하기 위해 URL 패턴 목록 작성을 허용합니다.

이 정책을 설정하지 않으면 모든 사이트에 전체 기본값이 사용됩니다. 이 기본값은 정책이 설정된 경우 [DefaultNotificationsSetting](#defaultnotificationssetting) 정책이나 사용자 개인 구성의 설정에 해당합니다. 유효한 URL 패턴에 대한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: NotificationsAllowedForUrls
  - GP 이름: 특정 사이트에서 알림 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: NotificationsAllowedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### NotificationsBlockedForUrls
  #### 특정 사이트에서 알림 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사이트에서 알림이 표시되지 않도록 지정하기 위해 URL 패턴 목록 작성을 허용합니다.

이 정책을 설정하지 않으면 모든 사이트에 전체 기본값이 사용됩니다. 이 기본값은 정책이 설정된 경우 [DefaultNotificationsSetting](#defaultnotificationssetting) 정책이나 사용자 개인 구성의 설정에 해당합니다. 유효한 URL 패턴에 대한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: NotificationsBlockedForUrls
  - GP 이름: 특정 사이트에서 알림 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: NotificationsBlockedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PluginsAllowedForUrls
  #### 특정 사이트에서 Adobe Flash 플러그 인 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  URL 패턴을 기반으로 Adobe Flash 플러그 인을 실행할 수 있는 사이트 목록을 정의합니다.

이 정책을 구성하지 않으면 [DefaultPluginsSetting](#defaultpluginssetting) 정책(설정된 경우) 또는 사용자의 개인 구성의 전역 기본값이 모든 사이트에 사용됩니다.

유효한 URL 패턴에 대한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)를 참조하세요. 그러나 M85에서 시작하는 경우 호스트에 ‘*’ 및 ‘[*.]’ 와일드카드를 사용하는 패턴은 더 이상 이 정책에서 지원되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PluginsAllowedForUrls
  - GP 이름: 특정 사이트에서 Adobe Flash 플러그 인 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\2 = "http://contoso.edu:8080"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PluginsAllowedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PluginsBlockedForUrls
  #### 특정 사이트에서 Adobe Flash 플러그 인 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  URL 패턴을 기반으로 Adobe Flash의 실행을 차단하는 사이트 목록을 정의합니다.

이 정책을 구성하지 않으면 [DefaultPluginsSetting](#defaultpluginssetting) 정책(설정된 경우) 또는 사용자의 개인 구성의 전역 기본값이 모든 사이트에 사용됩니다.

유효한 URL 패턴에 대한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)를 참조하세요. 그러나 M85에서 시작하는 경우 호스트에 ‘*’ 및 ‘[*.]’ 와일드카드를 사용하는 패턴은 더 이상 이 정책에서 지원되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PluginsBlockedForUrls
  - GP 이름: 특정 사이트에서 Adobe Flash 플러그 인 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\2 = "http://contoso.edu:8080"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PluginsBlockedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PopupsAllowedForUrls
  #### 특정 사이트에서 팝업 창 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  URL 패턴을 기반으로, 팝업 창을 열 수 있는 사이트 목록을 정의합니다.

이 정책을 구성하지 않으면 '[DefaultPopupsSetting](#defaultpopupssetting) 정책(설정된 경우) 또는 사용자의 개인 구성에 있는 전역 기본값이 모든 사이트에 사용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PopupsAllowedForUrls
  - GP 이름: 특정 사이트에서 팝업 창 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PopupsAllowedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PopupsBlockedForUrls
  #### 특정 사이트에서 팝업 창 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  URL 패턴을 기반으로, 팝업 창 열기가 차단되는 사이트 목록을 정의합니다.

이 정책을 구성하지 않으면 [DefaultPopupsSetting](#defaultpopupssetting) 정책(설정된 경우) 또는 사용자의 개인 구성에 있는 전역 기본값이 모든 사이트에 사용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PopupsBlockedForUrls
  - GP 이름: 특정 사이트에서 팝업 창 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PopupsBlockedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### RegisteredProtocolHandlers
  #### 프로토콜 처리기 등록
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  이 정책(권장)을 설정하여 프로토콜 처리기 목록을 등록합니다. 이 목록은 사용자가 등록한 이름과 병합되며, 두 경우 모두 사용할 수 있습니다.

 프로토콜 처리기를 등록하려면

- 프로토콜 속성을 구성표로 설정(예: "mailto")
- URL 속성을 "프로토콜" 필드에 지정된 구성표를 처리하는 응용 프로그램의 URL 속성으로 설정합니다. 이 패턴에는 처리된 URL을 대체하는 "%s" 자리 표시자가 포함될 수 있습니다.

사용자는 이 정책에서 등록한 프로토콜 처리기를 제거할 수 없지만, 새 기본 프로토콜 처리기를 설치하여 기존 프로토콜 처리기를 재정의할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 아니요
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 사전

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: RegisteredProtocolHandlers
  - GP 이름: 프로토콜 처리기 등록
  - GP 경로 (필수): 해당 없음
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/콘텐츠 설정
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): 해당 없음
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: RegisteredProtocolHandlers
  - 값 형식: REG_SZ
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [
  {
    "default": true, 
    "protocol": "mailto", 
    "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"
  }
]
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: RegisteredProtocolHandlers
  - 예제 값:
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
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SpotlightExperiencesAndRecommendationsEnabled
  #### 사용자가 사용자 정의 된 배경 이미지와 텍스트, 제안, 알림,
및 Microsoft 서비스에 대한 팁을 받을 수 있는지 여부를 선택합니다.
  
  
  #### 지원되는 버전:
  - Windows 86 이상부터

  #### 설명
  사용자가 Microsoft 서비스에 대한 맞춤 배경 이미지와 텍스트, 제안, 알림 및 팁을 받을 수 있는지 여부를 선택합니다.

이 설정을 사용하거나 구성하지 않으면 스포트라이트 환경 및 권장 사항이 사용 설정됩니다.

이 설정을 비활성화하면 스포트라이트 경험과 추천이 꺼집니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SpotlightExperiencesAndRecommendationsEnabled
  - GP 이름: 사용자가 사용자 정의 된 배경 이미지와 텍스트, 제안, 알림,
및 Microsoft 서비스에 대한 팁을 받을 수 있는지 여부를 선택합니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: SpotlightExperiencesAndRecommendationsEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### WebUsbAllowDevicesForUrls
  #### 특정 USB 장치에 연결하기 위해 특정 사이트에 대한 액세스 권한 부여
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  지정된 공급 업체 및 제품 Id를 사용하여 USB 장치에 대한 액세스 권한이 자동으로 부여되는 사이트를 지정하는 url 목록을 설정할 수 있습니다. 이 정책이 유효하려면 목록의 각 항목에 장치와 url이 모두 포함되어야 합니다. 장치의 각 항목에는 공급 업체 ID와 제품 ID 필드가 포함될 수 있습니다. 생략된 ID는 예외를 포함하여 와일드 카드로 처리되며,이 예외는 공급 업체 ID도 지정하지 않으면 제품 ID를 지정할 수 없다는 것을 의미합니다. 그렇지 않으면 정책이 유효하지 않으며 무시됩니다.

USB 권한 모델은 요청하는 사이트의 URL ("URL 요청")과 최상위 프레임 사이트의 URL ("포함 URL")을 사용하여 USB 장치에 액세스하는 데 필요한 URL을 요청합니다. 요청하는 사이트가 iframe에 로드될 때 요청하는 url이 포함 URL과 다를 수 있습니다. 따라서 "url" 필드에는 쉼표로 구분된 최대 2 개의 URL 문자열을 포함하여 각각 요청 및 포함 URL을 지정할 수 있습니다. URL을 하나만 지정하면 요청 사이트의 URL이 포함 상태에 관계 없이 이 URL과 일치하는 경우 해당 USB 장치에 대 한 액세스가 허용됩니다. "Url"의 Url은 유효한 Url 이어야 하며, 그렇지 않으면 정책이 무시됩니다.

이 정책을 설정하지 않으면 [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) 정책 (설정된 경우) 또는 사용자의 개인 구성에 모든 사이트에 대한 전역 기본값이 사용됩니다.

이 정책의 URL 패턴은 [WebUsbBlockedForUrls](#webusbblockedforurls)를 통해 구성된 것과 충돌하지 않아야 합니다. 충돌하는 경우 이 정책은 [WebUsbBlockedForUrls](#webusbblockedforurls) 및 [WebUsbAskForUrls](#webusbaskforurls)보다 우선시 됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 사전

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: WebUsbAllowDevicesForUrls
  - GP 이름: 특정 USB 장치에 연결하기 위해 특정 사이트에 대한 액세스 권한 부여
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: WebUsbAllowDevicesForUrls
  - 값 형식: REG_SZ
  ##### 예제 값:
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


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: WebUsbAllowDevicesForUrls
  - 예제 값:
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
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### WebUsbAskForUrls
  #### 특정 사이트에서 WebUSB 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  URL 패턴을 기반으로, 사용자에게 USB 장치에 대한 액세스를 요청할 수 있는 사이트 목록을 정의합니다.

이 정책을 구성하지 않으면 [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) 정책(설정된 경우) 또는 사용자의 개인 구성에 있는 전역 기본값이 모든 사이트에 사용됩니다.

이 정책에 정의된 URL 패턴은 [WebUsbBlockedForUrls](#webusbblockedforurls) 정책에 구성된 URL 패턴과 충돌하지 않습니다. - URL 허용 및 차단을 모두 할 수 없습니다. 유효한 URL 패턴에 대한 자세한 정보는 다음을 참조하세요. [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: WebUsbAskForUrls
  - GP 이름: 특정 사이트에서 WebUSB 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: WebUsbAskForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### WebUsbBlockedForUrls
  #### 특정 사이트에서 WebUSB 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  URL 패턴을 기반으로, 사용자에게 USB 장치에 대한 액세스를 허가하도록 요청할 수 없는 사이트 목록을 정의합니다.

이 정책을 구성하지 않으면 [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) 정책(설정된 경우) 또는 사용자의 개인 구성에 있는 전역 기본값이 모든 사이트에 사용됩니다.

이 정책의 URL 패턴은 [WebUsbAskForUrls](#webusbaskforurls) 정책에 구성된 URL 패턴과 충돌하지 않습니다. URL을 허용하거나 차단할 수 없습니다. 유효한 URL 패턴에 대한 자세한 정보는 다음을 참조하세요. [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: WebUsbBlockedForUrls
  - GP 이름: 특정 사이트에서 WebUSB 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/콘텐츠 설정
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: WebUsbBlockedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ## 프록시 서버 policies

  [맨 위로 이동](#microsoft-edge---정책)

  ### ProxyBypassList
  #### 프록시 바이패스 규칙 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge에서 프록시를 무시하는 호스트 목록을 정의합니다.

이 정책은 [ProxyMode](#proxymode) 정책에서 '고정 프록시 서버 사용'을 선택한 경우에만 적용됩니다. 프록시 정책을 구성하기 위해 다른 모드를 선택한 경우에는 이 정책을 사용하거나 구성하지 마세요.

이 정책을 사용하면 Microsoft Edge에서 프록시를 사용하지 않는 호스트 목록을 만들 수 있습니다.

이 정책을 구성하지 않으면 Microsoft Edge에서 프록시를 무시하는 호스트 목록이 만들어지지 않습니다. 프록시 정책을 설정하기 위한 다른 방법을 지정한 경우에는 이 정책을 구성하지 마세요.

자세한 예제는 [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ProxyBypassList
  - GP 이름: 프록시 바이패스 규칙 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/프록시 서버
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ProxyBypassList
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"https://www.contoso.com, https://www.fabrikam.com"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ProxyBypassList
  - 예제 값:
``` xml
<string>https://www.contoso.com, https://www.fabrikam.com</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ProxyMode
  #### 프록시 서버 설정 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge에서 사용하는 프록시 서버 설정을 지정합니다. 이 정책을 사용하면 사용자가 프록시 설정을 변경할 수 없습니다.

프록시 서버를 사용하지 않고 항상 직접 연결하도록 선택하면 다른 모든 옵션은 무시됩니다.

시스템 프록시 설정을 사용하도록 선택하면 다른 모든 옵션이 무시됩니다.

프록시 서버 자동 검색을 선택하면 다른 모든 옵션은 무시됩니다.

고정 서버 프록시 모드를 선택하면 [ProxyServer](#proxyserver) 및 '쉼표로 구분된 프록시 바이패스 규칙 목록'에서 추가 옵션을 지정할 수 있습니다.

.pac 프록시 스크립트를 사용하려면 '프록시 .pac 파일의 URL'에 스크립트의 URL을 지정해야 합니다.

자세한 예제는 [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)을 참조하세요.

이 정책을 사용하면 Microsoft Edge가 명령줄에서 지정한 모든 프록시 관련 옵션을 무시합니다.

이 정책을 구성하지 않으면 사용자가 자신의 프록시 설정을 선택할 수 있습니다.

정책 옵션 매핑:

* ProxyDisabled (direct) = 프록시 사용 안 함

* ProxyAutoDetect (auto_detect) = 프록시 설정 자동 검색

* ProxyPacScript (pac_script) = .pac 프록시 스크립트를 사용

* ProxyFixedServers (fixed_servers) = 고정된 프록시 서버 사용

* ProxyUseSystem (system) = 시스템 프록시 설정 사용

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ProxyMode
  - GP 이름: 프록시 서버 설정 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/프록시 서버
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ProxyMode
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"direct"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ProxyMode
  - 예제 값:
``` xml
<string>direct</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ProxyPacUrl
  #### 프록시.pac 파일 URL 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  프록시 자동 구성(PAC) 파일의 URL을 지정합니다.

이 정책은 [ProxyMode](#proxymode) 정책에서 '.pac 프록시 스크립트 사용'을 선택한 경우에만 적용됩니다. 프록시 정책을 구성하기 위해 다른 모드를 선택한 경우에는 이 정책을 사용하거나 구성하지 마세요.

이 정책을 사용하면 특정 웹 사이트를 가져오는 데 적합한 프록시 서버를 브라우저에서 자동으로 선택하는 방법을 정의하는 PAC 파일의 URL을 지정할 수 있습니다.

이 정책을 사용하지 않거나 구성하지 않으면 PAC 파일이 지정되지 않습니다. 프록시 정책을 설정하기 위한 다른 방법을 지정한 경우에는 이 정책을 구성하지 마세요.

자세한 예제는 [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)을 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ProxyPacUrl
  - GP 이름: 프록시.pac 파일 URL 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/프록시 서버
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ProxyPacUrl
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"https://internal.contoso.com/example.pac"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ProxyPacUrl
  - 예제 값:
``` xml
<string>https://internal.contoso.com/example.pac</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ProxyServer
  #### 프록시 서버의 주소 또는 URL 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  프록시 서버의 URL을 지정합니다.

이 정책은 [ProxyMode](#proxymode) 정책에서 '고정 프록시 서버 사용'을 선택한 경우에만 적용됩니다. 프록시 정책을 구성하기 위해 다른 모드를 선택한 경우에는 이 정책을 사용하거나 구성하지 마세요.

이 정책을 사용하면 이 정책으로 구성된 프록시 서버가 모든 URL에 사용됩니다.

이 정책을 사용하지 않거나 구성하지 않으면 이 프록시 모드에 있는 동안 사용자가 자신의 프록시 설정을 선택할 수 있습니다. 프록시 정책을 설정하기 위한 다른 방법을 지정한 경우에는 이 정책을 구성하지 마세요.

추가 옵션 및 자세한 예제는 [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)을 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ProxyServer
  - GP 이름: 프록시 서버의 주소 또는 URL 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/프록시 서버
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ProxyServer
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"123.123.123.123:8080"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ProxyServer
  - 예제 값:
``` xml
<string>123.123.123.123:8080</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ProxySettings
  #### 프록시 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge에 대한 프록시 설정을 구성합니다.

이 정책을 구성하면 Microsoft Edge는 명령줄에서 지정한 모든 프록시 관련 옵션을 무시합니다

이 정책을 구성하지 않으면 사용자가 자신의 프록시 설정을 변경할 수 있습니다.

이 정책은 다음 개별 정책을 재정의합니다.

[ProxyMode](#proxymode)
[ProxyPacUrl](#proxypacurl)
[ProxyServer](#proxyserver)
[ProxyBypassList](#proxybypasslist)

ProxyMode필드를 통해 Microsoft Edge에서 사용하는 프록시 서버를 지정할 수 있으며 사용자가 프록시 설정을 변경하지 못하게 할 수 있습니다.

ProxyPacUrl 필드는 프록시 .pac 파일의 URL입니다.

ProxyServer 필드는 프록시 서버의 URL입니다.

ProxyBypassList필드는 Microsoft Edge에서 무시할 프록시 호스트의 목록입니다.

'direct' 값을 'ProxyMode'로 선택하면 프록시가 사용되지 않으며 다른 모든 필드는 무시됩니다.

'system' 값을 'ProxyMode'로 선택하면 시스템의 프록시가 사용되고 다른 모든 필드는 무시됩니다.

'auto_detect' 값을 'ProxyMode'로 선택하면 다른 모든 필드는 무시됩니다.

'fixed_server' 값을 'ProxyMode'로 선택하면 'ProxyServer' 및 'ProxyBypassList' 필드가 사용됩니다.

'pac_script' 값을 'ProxyMode'로 선택하면 'ProxyPacUrl' 및 'ProxyBypassList' 필드가 사용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 사전

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ProxySettings
  - GP 이름: 프록시 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/프록시 서버
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ProxySettings
  - 값 형식: REG_SZ
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {
  "ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", 
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ProxySettings
  - 예제 값:
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
  

  [맨 위로 이동](#microsoft-edge---정책)

  ## 확장 policies

  [맨 위로 이동](#microsoft-edge---정책)

  ### ExtensionAllowedTypes
  #### 허용된 확장 유형 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  설치할 수 있는 확장 유형을 제어하고 런타임 액세스를 제한합니다.

이 설정은 허용되는 확장 유형과 상호 작용할 수 있는 호스트를 정의합니다. 값은 문자열 목록이며 각 문자열은 "extension", "theme", "user_script" 및 "hosted_app" 중 하나여야 합니다. 이러한 유형에 대한 자세한 내용은 Microsoft Edge 확장 문서를 참조하세요.

이 정책은 [ExtensionInstallForcelist](#extensioninstallforcelist) 정책을 사용하여 강제 설치할 확장에 영향을 줍니다.

이 정책을 사용하면 목록의 유형과 일치하는 확장만 설치됩니다.

이 정책을 구성하지 않으면 허용되는 extension 유형에 대한 제한이 적용되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ExtensionAllowedTypes
  - GP 이름: 허용된 확장 유형 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/확장
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes\1 = "hosted_app"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ExtensionAllowedTypes
  - 예제 값:
``` xml
<array>
  <string>hosted_app</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ExtensionInstallAllowlist
  #### 특정 확장 설치 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  기본적으로 모든 확장이 허용됩니다. 그러나 'ExtensionInstallBlockList'정책을 "*"로 설정하여 모든 확장을 차단하는 경우 사용자는 이 정책에 정의된 확장만 설치할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ExtensionInstallAllowlist
  - GP 이름: 특정 확장 설치 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/확장
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\2 = "extension_id2"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ExtensionInstallAllowlist
  - 예제 값:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ExtensionInstallBlocklist
  #### 설치될 수 없는 확장 제어
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용자가 Microsoft Edge에 설치할 수 없는 특정 확장을 나열합니다. 이 정책을 배포하면 이전에 설치된 이 목록의 확장을 사용할 수 없게 되며 사용자는 이러한 확장을 사용하도록 설정할 수 없습니다. 차단된 확장 목록에서 항목을 제거하면 해당 확장은 이전에 설치된 모든 위치에서 자동으로 다시 사용하도록 설정됩니다.

"*"를 사용하여 허용 목록에 명시적으로 나열되지 않은 모든 확장을 차단합니다.

이 정책을 구성하지 않으면 사용자가 Microsoft Edge에 확장을 설치할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ExtensionInstallBlocklist
  - GP 이름: 설치될 수 없는 확장 제어
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/확장
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\2 = "extension_id2"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ExtensionInstallBlocklist
  - 예제 값:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ExtensionInstallForcelist
  #### 자동으로 설치되는 확장 제어
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용자 개입 없이 자동으로 설치되고 사용자가 제거하거나 사용하지 않도록 설정할 수 없는("강제 설치") 확장을 지정합니다. 향후 버전의 확장에서 요청할 추가 사용 권한을 포함하여 확장에서 요청한 모든 사용 권한은 사용자 개입 없이 암시적으로 부여됩니다. 그에 더해 enterprise.deviceAttributes 및 enterprise.platformKeys 확장 API에 대한 사용 권한이 부여됩니다. (해당 두 API는 강제 설치되는 확장에서만 사용할 수 있습니다.)

해당 정책은 잠재적으로 충돌하는 [ExtensionInstallBlocklist](#extensioninstallblocklist) 정책보다 우선합니다. 강제 설치 목록에서 확장을 제거하면 Microsoft Edge에 의해 자동으로 제거됩니다.

Microsoft Active Directory 도메인에 가입되어 있는 Windows 인스턴스, Windows 10 Pro, 장치 관리에 등록되어 있는 Enterprise 인스턴스, MDM을 통해 관리되거나 MCX를 통해 도메인에 가입되어 있는 macOS 인스턴스 중 하나에 해당하지 않는 인스턴스의 경우 강제 설치는 Microsoft Edge 추가 기능 웹 사이트에서 나열된 앱 및 확장에 제한됩니다.

사용자는 개발자 도구를 사용하여 확장의 소스 코드를 수정할 수 있으므로 확장 기능이 제대로 렌더링되지 않을 수 있습니다. 해당 사항이 우려되는 경우 [DeveloperToolsAvailability](#developertoolsavailability) 정책을 설정하세요.

확장을 목록에 추가하려면 다음 형식을 사용하세요.

[extensionID];[updateURL]

- extensionID - 개발자 모드인 경우 edge://extensions에 있는 32자 문자열입니다.

- updateURL(선택 사항)은 [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043)에 설명된 대로 앱 또는 확장에 대한 업데이트 매니페스트 XML 문서의 주소입니다. Chrome 웹 스토어에서 확장을 설치하려면 Chrome 웹 스토어 업데이트 URL, https://clients2.google.com/service/update2/crx를 제공합니다. 해당 정책에 설정된 업데이트 URL은 초기 설치에만 사용됩니다. 이후 확장의 업데이트는 확장의 매니페스트에 표시된 업데이트 URL을 사용합니다. updateURL을 설정하지 않으면 확장은 Microsoft Store에서 호스트된 것으로 간주되고 다음 업데이트 URL(https://edge.microsoft.com/extensionwebstorebase/v1/crx)이 사용됩니다.

예를 들어, gggmmkjegpiggikcnhidnjjhmicpibll;https://edge.microsoft.com/extensionwebstorebase/v1/crx는 Microsoft Store "업데이트" URL에서 Microsoft Online 앱을 설치합니다. 확장 호스팅에 대한 자세한 내용은 다음을 참조하세요. [https://go.microsoft.com/fwlink/?linkid=2095044](https://go.microsoft.com/fwlink/?linkid=2095044).

이 정책을 구성하지 않으면 확장이 자동으로 설치되지 않으며 사용자는 Microsoft Edge에서 확장을 제거할 수 있습니다..

해당 정책은 InPrivate 모드에는 적용되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ExtensionInstallForcelist
  - GP 이름: 자동으로 설치되는 확장 제어
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/확장
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\1 = "gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\2 = "abcdefghijklmnopabcdefghijklmnop"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ExtensionInstallForcelist
  - 예제 값:
``` xml
<array>
  <string>gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx</string>
  <string>abcdefghijklmnopabcdefghijklmnop</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ExtensionInstallSources
  #### 확장 및 사용자 스크립트 설치 원본 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  확장 및 테마를 설치할 수 있는 URL을 정의합니다.

기본적으로 사용자는 설치하려는 각 확장 또는 스크립트에 대한 *.crx 파일을 다운로드한 다음 Microsoft Edge 설정 페이지로 파일을 끌어와야 합니다. 이 정책을 통해 특정 URL에서 사용자를 위해 확장 또는 스크립트를 설치할 수 있습니다.

이 목록의 각 항목은 확장 스타일 일치 패턴입니다([https://go.microsoft.com/fwlink/?linkid=2095039](https://go.microsoft.com/fwlink/?linkid=2095039) 참조). 사용자는 이 목록의 항목과 일치하는 모든 URL에서 항목을 쉽게 설치할 수 있습니다. *.crx 파일의 위치 및 다운로드가 시작되는 페이지(즉, 참조 페이지)는 이 패턴에 의해 허용되어야 합니다.

[ExtensionInstallBlocklist](#extensioninstallblocklist) 정책이 이 정책보다 우선합니다. 차단 목록에 있는 모든 확장은 이 목록의 사이트가 출처인 경우에도 설치되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ExtensionInstallSources
  - GP 이름: 확장 및 사용자 스크립트 설치 원본 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/확장
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources\1 = "https://corp.contoso.com/*"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ExtensionInstallSources
  - 예제 값:
``` xml
<array>
  <string>https://corp.contoso.com/*</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ExtensionSettings
  #### 확장 관리 설정 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge에 대한 확장 관리 설정을 구성합니다.

이 정책은 기존의 확장 관련 정책에 의해 제어되는 설정을 포함하여 여러 설정을 제어합니다. 두 가지 모두가 설정된 경우 이 정책은 기존 정책보다 우선합니다.

이 정책은 확장 ID 또는 업데이트 URL을 해당 구성에 매핑합니다. 확장 ID를 사용하면 구성은 지정된 확장에만 적용됩니다. 특수 ID "*"에 대한 기본 구성을 설정하여 이 정책에 특별히 나열되지 않은 모든 확장에 적용합니다. 업데이트 URL을 사용하면 [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043)에서 설명한 대로 이 확장의 매니페스트에 명시된 정확한 업데이트 URL을 가진 모든 확장에 구성이 적용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 사전

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ExtensionSettings
  - GP 이름: 확장 관리 설정 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/확장
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ExtensionSettings
  - 값 형식: REG_SZ
  ##### 예제 값:
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


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ExtensionSettings
  - 예제 값:
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
  

  [맨 위로 이동](#microsoft-edge---정책)

  ## Additional policies

  [맨 위로 이동](#microsoft-edge---정책)

  ### AddressBarMicrosoftSearchInBingProviderEnabled
  #### 주소 표시줄의 Bing 추천에서 Microsoft Search 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 81 이상

  #### 설명
  사용자가 주소 표시줄에 검색 문자열을 입력할 때 주소 표시줄의 추천 목록에 있는 Bing 추천에서 관련 Microsoft Search의 표시를 활성화합니다. 이 정책을 활성화하거나 구성하지 않으면 사용자는 Microsoft Edge 주소 표시줄 추천 목록의 Bing에서 Microsoft Search를 통해 제공되는 내부 결과를 볼 수 있습니다. Bing에서 Microsoft Search 결과를 보려면 사용자가 해당 조직용 Azure AD 계정을 사용하여 Microsoft Edge에 로그인되어 있어야 합니다.
이 정책을 비활성화하면 사용자는 Microsoft Edge 주소 표시줄 추천 목록에서 내부 결과를 볼 수 없습니다.
기본 검색 공급자([DefaultSearchProviderEnabled](#defaultsearchproviderenabled), [DefaultSearchProviderName](#defaultsearchprovidername) 및 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl))를 강제로 적용하는 정책 집합을 활성화한 경우, 지정된 검색 공급자가 Bing이 아니면 이 정책이 적용되지 않으며, 주소 표시줄의 추천 목록에 Bing의 Microsoft Search 추천이 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AddressBarMicrosoftSearchInBingProviderEnabled
  - GP 이름: 주소 표시줄의 Bing 추천에서 Microsoft Search 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AddressBarMicrosoftSearchInBingProviderEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AddressBarMicrosoftSearchInBingProviderEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AdsSettingForIntrusiveAdsSites
  #### 침입적인 광고가 있는 사이트에 대한 광고 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 78 이상

  #### 설명
  방해가 되는 광고가 있는 사이트에서 광고를 차단할지 여부를 제어

정책 옵션 매핑:

* AllowAds (1) = 모든 사이트에서 광고 허용

* BlockAds (2) = 침입적인 광고가 있는 사이트에서 광고를 차단합니다. (기본값)

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AdsSettingForIntrusiveAdsSites
  - GP 이름: 침입적인 광고가 있는 사이트에 대한 광고 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AdsSettingForIntrusiveAdsSites
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AdsSettingForIntrusiveAdsSites
  - 예제 값:
``` xml
<integer>1</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AllowDeletingBrowserHistory
  #### 브라우저 및 다운로드 기록 삭제 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  브라우저 기록 및 다운로드 기록을 삭제하고 사용자가 이 설정을 변경할 수 없도록 합니다.

참고: 이 정책을 사용하지 않도록 설정해도 검색 및 다운로드 기록은 유지되지 않을 수 있습니다. 즉, 사용자가 기록 데이터베이스 파일을 직접 편집하거나 삭제할 수 있으며 브라우저 자체에서 언제든지 일부 또는 전체 기록을 만료 기간에 따라 제거하거나 보관할 수 있습니다.

이 정책을 사용하거나 구성하지 않으면 사용자가 검색 및 다운로드 기록을 삭제할 수 있습니다.

이 정책을 사용하지 않으면 사용자가 검색 및 다운로드 기록을 삭제할 수 없습니다.

이 정책을 사용하도록 설정하는 경우에는 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 정책을 사용하도록 설정하지 마세요. 둘 다 사용하도록 설정하는 경우에는 이 정책이 어떻게 구성되는지에 관계 없이 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 정책이 우선하고 Microsoft Edge가 닫힐 때 모든 데이터가 삭제됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AllowDeletingBrowserHistory
  - GP 이름: 브라우저 및 다운로드 기록 삭제 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AllowDeletingBrowserHistory
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AllowDeletingBrowserHistory
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AllowFileSelectionDialogs
  #### 파일 선택 대화 상자 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge에서 파일 선택 대화 상자를 표시하여 로컬 파일에 대한 액세스를 허용합니다.

이 정책을 사용하거나 구성하지 않으면 사용자가 파일 선택 대화 상자를 정상적으로 열 수 있습니다.

이 정책을 사용하지 않으면 사용자가 파일 선택 대화 상자(예: 즐겨찾기 가져 오기, 파일 업로드, 링크 저장 등)를 트리거하는 작업을 수행할 때마다 대신 메시지가 표시되고 사용자가 파일 선택 대화 상자에서 [취소]를 클릭한 것으로 간주됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AllowFileSelectionDialogs
  - GP 이름: 파일 선택 대화 상자 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AllowFileSelectionDialogs
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AllowFileSelectionDialogs
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AllowPopupsDuringPageUnload
  #### 언로드하는 동안 페이지에서 팝업을 표시하도록 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 78 이상

  #### 설명
  이 정책을 통해 관리자는 페이지를 언로드하는 동안 팝업을 표시할 수 있도록 지정할 수 있습니다.

정책을 사용하도록 설정하면 페이지를 언로드하는 동안 팝업을 표시할 수 있습니다.

 정책을 사용 안 함 또는 설정 해제로 설정하면 페이지가 언로드되는 동안 팝업을 표시할 수 없습니다. 이는 사양(https://html.spec.whatwg.org/#apis-for-creating-and-navigating-browsing-contexts-by-name)에 따라 다릅니다.

 이 정책은 향후에 제거될 예정입니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AllowPopupsDuringPageUnload
  - GP 이름: 언로드하는 동안 페이지에서 팝업을 표시하도록 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AllowPopupsDuringPageUnload
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AllowPopupsDuringPageUnload
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AllowSurfGame
  #### 서핑 게임 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 83 이상

  #### 설명
  이 정책을 사용하지 않으면 장치가 오프라인일 때 또는 사용자가 edge://surf로 이동한 경우에는 사용자가 서핑 게임을 플레이할 수 없습니다.

이 정책을 사용하도록 설정하거나 구성하지 않으면 사용자가 서핑 게임을 플레이할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AllowSurfGame
  - GP 이름: 서핑 게임 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AllowSurfGame
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AllowSurfGame
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AllowSyncXHRInPageDismissal
  #### 페이지 해제 중에 페이지에서 동기 XHR 요청을 보내도록 허용 (사용되지 않음)
  >사용되지 않음: 이 정책은 더 이상 사용되지 않습니다. 현재 지원되고 있으나 향후 릴리스에서는 사용되지 않을 예정입니다.
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 79 이상

  #### 설명
  이 정책은 페이지 해제 중에 동기 XHR 요청을 허용하지 않는 변경 사항과 호환되지 않는 것으로 판명된 경우, 기업이 웹 컨텐츠를 업데이트할 시간을 더 많이 제공하기 위한 단기 메커니즘일 뿐이므로 더 이상 사용되지 않습니다. Microsoft Edge 버전 88에서는 작동하지 않습니다.

이 정책을 사용하면 페이지 해제 중에 페이지가 동기 XHR 요청을 보낼 수 있도록 지정할 수 있습니다.

이 정책을 사용하면 페이지를 닫는 동안 페이지가 동기 XHR 요청을 보낼 수 있습니다.

이 정책을 사용하지 않도록 설정하거나 구성하지 않으면 페이지 해제를 진행하는 동안 페이지에서 동기 XHR 요청을 보낼 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AllowSyncXHRInPageDismissal
  - GP 이름: 페이지 해제 중에 페이지에서 동기 XHR 요청을 보내도록 허용 (사용되지 않음)
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AllowSyncXHRInPageDismissal
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AllowSyncXHRInPageDismissal
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AllowTokenBindingForUrls
  #### Microsoft Edge에서 토큰 바인딩을 설정하려고 하는 사이트 목록을 구성합니다.
  
  
  #### 지원되는 버전:
  - Windows 83 이상부터

  #### 설명
  브라우저에서 토큰 바인딩 프로토콜을 수행 하려고 시도하는 사이트에 대한 URL 패턴 목록을 구성합니다.
이 목록의 도메인에 대해 브라우저는 TLS 핸드셰이크에 토큰 바인딩 ClientHello를 전송합니다(자세한 내용은 https://tools.ietf.org/html/rfc8472를 참조하세요).
서버가 유효한 ServerHello 응답을 사용하여 응답 하는 경우 브라우저가 다음 https 요청에서 토큰 바인딩 메시지를 만들고 보냅니다. 자세한 정보는 https://tools.ietf.org/html/rfc8471을 참조하세요.

이 목록이 비어있으면 토큰 바인딩을 사용할 수 없게 됩니다.

이 정책은 가상 보안 모드 기능이 있는 Windows 10 장치에서만 사용할 수 있습니다.

Microsoft Edge 86부터, 이 정책은 동적 새로 고침을 더 이상 지원하지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AllowTokenBindingForUrls
  - GP 이름: Microsoft Edge에서 토큰 바인딩을 설정하려고 하는 사이트 목록을 구성합니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\2 = "[*.]mydomain2.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\3 = "[*.].mydomain2.com"

```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AllowTrackingForUrls
  #### 특정 사이트에 대한 추적 방지 예외 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 78 이상

  #### 설명
  추적 방지에서 제외되는 URL 패턴의 목록을 구성합니다.

이 정책을 구성하는 경우 구성된 URL 패턴 목록은 추적 방지에서 제외됩니다.

이 정책을 구성하지 않는 경우 "사용자의 웹 검색 활동 추적 차단" 정책(설정된 경우)의 전역 기본값 또는 사용자의 개인 구성이 모든 사이트에 사용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AllowTrackingForUrls
  - GP 이름: 특정 사이트에 대한 추적 방지 예외 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AllowTrackingForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AlternateErrorPagesEnabled
  #### 웹 페이지를 찾을 수 없을 때 비슷한 페이지 추천
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 80 이상

  #### 설명
  Microsoft Edge에서 웹 서비스에 대한 연결을 발급하여 URL을 생성 하 고 DNS 오류와 같은 연결 문제에 대한 검색할 수 있도록 허용합니다.

이 정책을 사용하면 웹 서비스는 URL을 생성하고 네트워크 오류에 대한 제안을 검색하는 데 사용됩니다.

이 정책을 사용하지 않으면 웹 서비스를 호출하지 않고 표준 오류 페이지가 표시됩니다.

이 정책을 구성하지 않으면 Microsoft Edge는 edge://settings/privacy의 서비스에서 설정한 사용자 기본 설정을 유지합니다.
특히, 사용자가 켜거나 끌 수 있는 **웹 페이지를 찾을 수 없을 때 비슷한 페이지 추천** 토글이 있습니다. 이 정책(AlternateErrorPagesEnabled)을 사용하면 웹 페이지를 찾을 수 없는 경우 비슷한 페이지 추천 설정이 켜져 있지만 사용자는 토글을 사용하여 설정을 변경할 수 없습니다. 이 정책을 사용하지 않으면 웹 페이지를 찾을 수 없을 때 비슷한 페이지 추천 설정이 꺼지고 사용자가 토글을 사용하여 설정을 변경할 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AlternateErrorPagesEnabled
  - GP 이름: 웹 페이지를 찾을 수 없을 때 비슷한 페이지 추천
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: AlternateErrorPagesEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AlternateErrorPagesEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AlwaysOpenPdfExternally
  #### 항상 외부에서 PDF 파일 열기
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge에서 내부 PDF 뷰어를 사용하지 않도록 설정합니다.

이 정책을 사용하면 Microsoft Edge에서 PDF 파일을 다운로드 파일로 취급하고 사용자가 기본 응용 프로그램을 사용하여 해당 파일을 열 수 있습니다.

이 정책을 구성하지 않거나 사용하지 않도록 설정하면 Microsoft Edge에서 PDF 파일을 엽니다(사용자가 사용하지 않도록 설정하지 않는 한).

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AlwaysOpenPdfExternally
  - GP 이름: 항상 외부에서 PDF 파일 열기
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AlwaysOpenPdfExternally
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AlwaysOpenPdfExternally
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AmbientAuthenticationInPrivateModesEnabled
  #### InPrivate 및 게스트 프로필에 대해 앰비언트 인증 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 81 이상

  #### 설명
  Microsoft Edge에서 InPrivate 및 Guest 프로파일에 대한 외부 인증을 허용/허용하지 않도록 이 정책을 구성합니다.

NTLM/Kerberos/협상 대상 질문/응답 체계를 통해 명시적 자격 증명이 제공되지 않는 경우 주변 인증은 기본 자격 증명이 포함된 http 인증입니다.

정책을 'RegularOnly'로 설정하면 일반 세션에 대해서만 주변 인증을 허용합니다. InPrivate 및 Guest 세션은 주변 인증이 허용되지 않습니다.

정책을 'InPrivateAndRegular'로 설정하면 InPrivate 및 일반 세션에 대해 주변 인증을 수행할 수 있습니다. 게스트 세션은 주변 인증이 허용되지 않습니다.

정책을 'GuestAndRegular'로 설정하면 게스트 및 일반 세션에 대해 외부 인증을 수행할 수 있습니다. InPrivate 세션은 주변 인증을 허용하지 않습니다

정책을 'All'로 설정하면 모든 세션에 대해 주변 인증을 허용합니다.

주변 인증은 항상 일반 프로필에서 허용됩니다.

Microsoft Edge 버전 81 이상에서 정책을 설정하지 않은 경우 일반 세션에서만 외부 인증이 사용됩니다.

정책 옵션 매핑:

* RegularOnly (0) = 일반 세션에서만 앰비언트 인증 사용

* InPrivateAndRegular (1) = InPrivate 및 일반 세션에서 앰비언트 인증 사용

* GuestAndRegular (2) = 게스트 및 일반 세션에서 앰비언트 인증 사용

* All (3) = 일반, InPrivate 및 게스트 세션에서 앰비언트 인증을 사용하도록 설정합니다.

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AmbientAuthenticationInPrivateModesEnabled
  - GP 이름: InPrivate 및 게스트 프로필에 대해 앰비언트 인증 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AmbientAuthenticationInPrivateModesEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AmbientAuthenticationInPrivateModesEnabled
  - 예제 값:
``` xml
<integer>0</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AppCacheForceEnabled
  #### AppCache 기능이 기본적으로 해제되어 있더라도 다시 사용할 수 있도록 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 84 이상

  #### 설명
  이 정책을 true로 설정하면 Microsoft Edge의 AppCache를 기본적으로 사용할 수 없는 경우에도 AppCache가 활성화됩니다.

이 정책을 false로 설정하거나 설정하지 않으면 AppCache는 Microsoft Edge의 기본값을 따릅니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AppCacheForceEnabled
  - GP 이름: AppCache 기능이 기본적으로 해제되어 있더라도 다시 사용할 수 있도록 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AppCacheForceEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AppCacheForceEnabled
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ApplicationLocaleValue
  #### 응용 프로그램 로캘 설정
  
  
  #### 지원되는 버전:
  - Windows 77 이상부터

  #### 설명
  Microsoft Edge에서 응용 프로그램 로캘을 구성하고 사용자가 로캘을 변경하지 못하도록 합니다.

이 정책을 사용하면 Microsoft Edge가 지정된 로캘을 사용합니다. 구성된 로캘이 지원되지 않으면 'en-US'가 대신 사용됩니다.

이 설정을 사용하지 않거나 구성하지 않으면 Microsoft Edge는 사용자가 지정한 기본 설정 로캘(구성된 경우) 또는 대체 로캘 'en-US'를 사용합니다

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ApplicationLocaleValue
  - GP 이름: 응용 프로그램 로캘 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: ApplicationLocaleValue
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"en"
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AudioCaptureAllowed
  #### 오디오 캡처 허용 또는 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용자에게 해당 오디오 캡처 장치에 대한 액세스 권한을 부여하라는 메시지를 표시할지 여부를 설정하도록 허용합니다. 이 정책은 [AudioCaptureAllowedUrls](#audiocaptureallowedurls) 목록에 구성된 URL을 제외한 모든 URL에 적용됩니다.

이 정책을 사용하거나 구성하지 않으면(기본 설정) [AudioCaptureAllowedUrls](#audiocaptureallowedurls) 목록의 URL을 제외하고 오디오 캡처 액세스를 묻는 프롬프트가 표시됩니다. 나열된 URL은 메시지를 표시하지 않고 액세스 권한이 부여됩니다.

이 정책을 사용하지 않으면 사용자에게 메시지가 표시되지 않고 [AudioCaptureAllowedUrls](#audiocaptureallowedurls)에 구성된 URL에서만 오디오 캡처에 액세스할 수 있습니다.

이 정책은 내장 마이크뿐만 아니라 모든 유형의 오디오 입력에 영향을 줍니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AudioCaptureAllowed
  - GP 이름: 오디오 캡처 허용 또는 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AudioCaptureAllowed
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AudioCaptureAllowed
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AudioCaptureAllowedUrls
  #### 사용 권한을 요청하지 않고 오디오 캡처 장치에 액세스할 수 있는 사이트
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  URL 패턴을 기반으로 사용자에게 사용 권한 요청을 하지 않고 오디오 캡처 장치를 사용할 수 있는 웹 사이트를 지정합니다. 이 목록의 패턴은 요청 URL의 보안 시작과 비교됩니다. 일치할 경우 사이트에 오디오 캡처 장치에 대한 액세스 사용 권한이 자동으로 부여됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AudioCaptureAllowedUrls
  - GP 이름: 사용 권한을 요청하지 않고 오디오 캡처 장치에 액세스할 수 있는 사이트
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AudioCaptureAllowedUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AudioSandboxEnabled
  #### 오디오 샌드박스 실행 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 81 이상

  #### 설명
  이 정책은 오디오 프로세스 샌드박스를 제어합니다.

이 정책을 사용하면 오디오 프로세스가 샌드박스로 실행됩니다.

이 정책을 사용하지 않으면 오디오 프로세스가 샌드박스로 실행되지 않고 WebRTC 오디오 처리 모듈이 렌더러 프로세스에서 실행됩니다.
이렇게 하면 사용자가 오디오 하위 시스템이 샌드박스로 실행되지 않는 것과 관련된 보안 위험에 노출됩니다.

이 정책을 구성하지 않으면 오디오 샌드박스의 기본 구성이 사용되며, 이는 플랫폼에 따라 다를 수 있습니다.

이 정책은 사용자가 샌드박스를 방해하는 보안 소프트웨어 설정을 사용하는 경우에 오디오 샌드박스를 사용하지 않도록 설정할 수 있는 엔터프라이즈 유연성을 제공하기 위한 것입니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AudioSandboxEnabled
  - GP 이름: 오디오 샌드박스 실행 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AudioSandboxEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AudioSandboxEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AutoImportAtFirstRun
  #### 처음 실행 시 다른 브라우저의 데이터 및 설정 자동으로 가져오기
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  이 정책을 실행하면 지정된 브라우저에서 지원되는 모든 데이터 유형 및 설정이 처음 실행 시 자동으로 가져오기됩니다. 처음 실행 환경에서는 가져오기 섹션도 건너뜁니다.

      Microsoft Edge 레거시의 브라우저 데이터는 이 정책의 값에 관계없이 항상 처음 실행 시 자동으로 마이그레이션됩니다.

이 정책을 'FromDefaultBrowser'로 설정하면 관리되는 디바이스의 기본 브라우저에 해당하는 데이터 유형을 가져옵니다.

      이 정책 값으로 지정된 브라우저가 관리되는 디바이스에 없는 경우 Microsoft Edge은(는) 사용자에게 알리지 않고 가져오기를 건너뜁니다.

      이 정책을 '사용 안 함'으로 설정한 경우입니다.AutoImport'는 처음 실행 환경의 가져오기 섹션을 완전히 건너뛰고 Microsoft Edge이(가) 브라우저 데이터 및 설정을 자동으로 가져오지 않습니다.

      이 정책을 'FromInternetExplorer' 값으로 설정하면 Internet Explorer에서 다음 데이터 유형을 가져옵니다.
1. 즐겨찾기 또는 책갈피
2. 저장된 암호
3. 검색 엔진
4. 검색 기록
5. 홈페이지

      이 정책을 'FromGoogleChrome' 값으로 설정하면 Google Chrome에서 다음 데이터 유형을 가져옵니다.
      1. 즐겨찾기
      2. 저장된 암호
      3. 주소 등
     4. 결제 정보
     5. 검색 기록
      6. 설정
      7. 고정 및 열기 탭
      8. 확장
      9. 쿠키

      참고: Google Chrome에서 가져온 항목에 대한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2120835](https://go.microsoft.com/fwlink/?linkid=2120835)을 참조하십시오

      이 정책을 'FromSafari' 값으로 설정하면 사용자 데이터를 더 이상 Microsoft Edge로 가져오지 않습니다. 이는 Mac에서 전체 디스크 액세스가 작동하는 방식 때문입니다.
      MacOS Mojave 이상에서는 더 이상 Safari 데이터를 자동으로 Microsoft Edge로 가져올 수 없습니다.

      Microsoft Edge 버전 83부터 이 정책을 'FromMozillaFirefox' 값으로 설정하면 Mozilla Firefox에서 다음과 같은 데이터 유형을 가져옵니다
      1. 즐겨찾기 또는 책갈피
      2. 저장된 암호
      3. 주소 등
      4. 검색 기록

특정 데이터 유형을 관리 디바이스로 가져오는 것을 제한하려면 이 정책을 [ImportAutofillFormData](#importautofillformdata), [ImportBrowserSettings](#importbrowsersettings), [ImportFavorites](#importfavorites) 등의 다른 정책과 함께 사용할 수 있습니다.

정책 옵션 매핑:

* FromDefaultBrowser (0) = 기본 브라우저에서 지원되는 모든 데이터 형식 및 설정을 자동으로 가져오기

* FromInternetExplorer (1) = Internet Explorer에서 지원되는 모든 데이터 형식 및 설정을 자동으로 가져오기

* FromGoogleChrome (2) = Google Chrome에서 지원되는 모든 데이터 형식 및 설정을 자동으로 가져오기

* FromSafari (3) = Safari에서 지원되는 모든 데이터 형식 및 설정을 자동으로 가져오기

* DisabledAutoImport (4) = 자동 가져오기를 사용하지 않고, 첫 실행 경험의 가져오기 섹션을 건너뜀

* FromMozillaFirefox (5) = Mozilla Firefox에서 지원되는 모든 데이터 형식 및 설정을 자동으로 가져오기

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AutoImportAtFirstRun
  - GP 이름: 처음 실행 시 다른 브라우저의 데이터 및 설정 자동으로 가져오기
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AutoImportAtFirstRun
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AutoImportAtFirstRun
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AutoLaunchProtocolsFromOrigins
  #### 사용자에게 묻지 않고 목록에 있는 원본에서 외부 응용 프로그램을 실행할 수 있는 프로토콜 목록을 정의합니다.
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 85 이상

  #### 설명
  사용자는 프로토콜 목록과 각 프로토콜에 대해 사용자에게 묻지 않고 외부 응용 프로그램을 실행할 수 있는 허용되는 원본 패턴과 관련된 목록을 설정할 수 있습니다. 프로토콜을 나열하는 경우 후행 구분 기호를 포함하면 안 됩니다. 예를 들어 "skype:" 또는 "skype://" 대신 "skype"를 나열해야 합니다.

이 정책을 구성하는 경우 정책에서 묻지 않고 외부 응용 프로그램의 실행만 허용됩니다. 다음의 조건이 있습니다.

-프로토콜이 목록에 나열됩니다.

- 프로토콜을 실행하려는 사이트의 원본이 해당 프로토콜의 allowed_origins 목록에 있는 원본 패턴 중 하나와 일치합니다.

두 조건 중 하나가 거짓이면 외부 프로토콜 시작 프롬프트는 정책에서 생략되지 않습니다.

이 정책을 구성하지 않으면 프롬프트 없이 시작할 수 있는 프로토콜은 없습니다. 사용자는 [ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox) 정책이 사용 안 함으로 설정되어 있지 않으면 프로토콜별/사이트별 프롬프트에서 옵트아웃될 수 있습니다. 이 정책은 사용자가 설정하는 프로토콜별/사이트별 프롬프트 예외에 영향을 주지 않습니다.

원본 일치 패턴은 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)에서 기록된 [URLBlocklist](#urlblocklist) 정책에 대한 패턴과 유사한 형식을 사용합니다.

그러나 이 정책에 대한 원본 일치 패턴에는 "/path" 또는 "@query" 요소가 포함될 수 없습니다. "/Path" 또는 "@query" 요소가 포함된 모든 패턴은 무시됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 사전

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AutoLaunchProtocolsFromOrigins
  - GP 이름: 사용자에게 묻지 않고 목록에 있는 원본에서 외부 응용 프로그램을 실행할 수 있는 프로토콜 목록을 정의합니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AutoLaunchProtocolsFromOrigins
  - 값 형식: REG_SZ
  ##### 예제 값:
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


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AutoLaunchProtocolsFromOrigins
  - 예제 값:
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
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AutoOpenAllowedForURLs
  #### AutoOpenFileType을 적용할 수 있는 URL입니다.
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 85 이상

  #### 설명
  [AutoOpenFileTypes](#autoopenfiletypes)이(가) 적용될 URL 목록입니다. 이 정책은 다운로드 쉘프를 통해 사용자가 설정한 자동 열기 값에 영향을 미치지 않습니다. > "항상 이 유형의 파일을 엽니다" 메뉴 항목.

이 정책에서 URL을 설정하는 경우 URL이 이 집합의 일부이고 파일 유형이 [AutoOpenFileTypes](#autoopenfiletypes)에 나열된 경우에만 정책에 의해 파일이 자동으로 열립니다. 두 조건 중 하나가 잘못된 경우 정책에서 다운로드가 자동으로 열리지 않습니다.

이 정책을 설정하지 않으면 [AutoOpenFileTypes](#autoopenfiletypes)의 파일 형식이 있는 모든 다운로드가 자동으로 열립니다.

URL 패턴은 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)에 따라 포맷해야 합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AutoOpenAllowedForURLs
  - GP 이름: AutoOpenFileType을 적용할 수 있는 URL입니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\1 = "example.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\5 = ".exact.hostname.com"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AutoOpenAllowedForURLs
  - 예제 값:
``` xml
<array>
  <string>example.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AutoOpenFileTypes
  #### 다운로드 시 자동으로 열어야 하는 파일 형식 목록입니다.
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 85 이상

  #### 설명
  이 정책은 다운로드 시 자동으로 열어야 하는 파일 형식 목록을 설정합니다. 참고: 파일 형식을 나열할 때 선행 구분 기호를 포함하면 안 되므로 ".txt" 대신 "txt"를 나열합니다.

기본적으로 이러한 파일 형식은 모든 URL에서 자동으로 열립니다. [AutoOpenAllowedForURLs](#autoopenallowedforurls) 정책을 사용하여 이러한 파일 형식을 자동으로 열 URL을 제한할 수 있습니다.

자동으로 열어야 하는 유형의 파일은 여전히 활성화된 Microsoft Defender SmartScreen 확인의 적용을 받으며 이러한 확인에 실패할 경우 열리지 않습니다.

사용자가 자동으로 열도록 이미 지정한 파일 형식은 다운로드 시 계속 자동으로 열립니다. 사용자는 자동으로 열 수 있는 다른 파일 형식을 계속 지정할 수 있습니다.

이 정책을 설정하지 않으면 사용자가 자동으로 열도록 이미 지정한 파일 형식만 다운로드 시 자동으로 열립니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AutoOpenFileTypes
  - GP 이름: 다운로드 시 자동으로 열어야 하는 파일 형식 목록입니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\1 = "exe"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\2 = "txt"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AutoOpenFileTypes
  - 예제 값:
``` xml
<array>
  <string>exe</string>
  <string>txt</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AutofillAddressEnabled
  #### 주소 정보 자동 채우기 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  자동 채우기 기능을 사용하도록 설정하고 사용자가 이전에 저장된 정보를 사용하여 웹 양식에 주소 정보를 자동으로 완성하도록 허용합니다.

이 정책을 사용하지 않으면 자동 채우기 기능이 주소 정보를 제안하거나 채우지 않으며 사용자가 웹을 탐색할 때 제출할 수 있는 추가 주소 정보도 저장하지 않습니다.

이 정책을 사용하거나 구성하지 않으면 사용자는 사용자 인터페이스의 주소에 대한 자동 채우기를 제어할 수 있습니다.

참고: 이 정책을 사용하지 않으면 지불 및 암호 양식을 제외한 모든 웹 양식의 모든 활동도 중지됩니다. 더 이상 항목이 저장되지 않으며 Microsoft Edge는 이전 항목을 제안하거나 자동으로 채우지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AutofillAddressEnabled
  - GP 이름: 주소 정보 자동 채우기 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: AutofillAddressEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AutofillAddressEnabled
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AutofillCreditCardEnabled
  #### 신용 카드 정보 자동 채우기 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge의 자동 채우기 기능을 사용하도록 설정하고 사용자가 이전에 저장된 정보를 사용하여 웹 양식에 신용 카드 정보를 자동으로 완성할 수 있게 합니다.

이 정책을 사용하지 않으면 자동 채우기에서 신용 카드 정보를 제안하거나 채우지 않으며 사용자가 웹을 검색하는 동안 제출할 수 있는 추가 신용 카드 정보를 저장하지 않습니다.

이 정책을 사용하거나 구성하지 않으면 사용자가 신용 카드 정보 자동 채우기를 제어할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AutofillCreditCardEnabled
  - GP 이름: 신용 카드 정보 자동 채우기 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: AutofillCreditCardEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AutofillCreditCardEnabled
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### AutoplayAllowed
  #### 웹 사이트에 미디어 자동 재생 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 78 이상

  #### 설명
  이 정책은 웹 사이트에 대한 미디어 자동 재생 정책을 설정합니다.

기본 설정인 "구성되지 않음"은 현재 미디어 자동 실행 설정을 고려하며 사용자가 자동 실행 설정을 구성할 수 있도록 합니다..

"사용"으로 설정하면 미디어 자동 실행이 "허용"으로 설정됩니다. 모든 웹 사이트는 자동으로 미디어를 재생할 수 있습니다. 사용자가 이 정책을 무시할 수 없습니다..

"사용 안 함"으로 설정하면 미디어 자동 실행이 "차단"으로 설정됩니다. 미디어에 자동 실행을 허용하는 웹 사이트가 없습니다. 사용자가 이 정책을 무시할 수 없습니다.

이 정책이 적용되려면 탭을 닫았다가 다시 열어야 합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: AutoplayAllowed
  - GP 이름: 웹 사이트에 미디어 자동 재생 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: AutoplayAllowed
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: AutoplayAllowed
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### BackgroundModeEnabled
  #### Microsoft Edge가 닫힌 후 백그라운드 앱 계속 실행
  
  
  #### 지원되는 버전:
  - Windows 77 이상부터

  #### 설명
  OS 로그인 시 Microsoft Edge 프로세스가 시작되고 마지막 브라우저 창이 닫힌 후 계속 실행되도록 허용합니다. 이 시나리오에서는 백그라운드 앱과 현재 검색 세션이 세션 쿠키를 포함하여 활성 상태로 유지됩니다. 열려 있는 백그라운드 프로세스는 시스템 트레이에 아이콘을 표시하며 거기에서 언제든지 닫을 수 있습니다.

이 정책을 사용하면 백그라운드 모드가 켜집니다.

이 정책을 사용하지 않으면 백그라운드 모드가 꺼집니다.

이 정책을 구성하지 않으면 초기에 백그라운드 모드가 꺼지고 사용자가 edge://settings/system에서 동작을 구성할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: BackgroundModeEnabled
  - GP 이름: Microsoft Edge가 닫힌 후 백그라운드 앱 계속 실행
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: BackgroundModeEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### BackgroundTemplateListUpdatesEnabled
  #### 컬렉션 및 템플릿을 사용하는 기타 기능의 사용 가능한 템플릿 목록에 대한 백그라운드 업데이트를 사용하도록 설정합니다.
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 79 이상

  #### 설명
  컬렉션 템플릿을 사용하는 기타 기능에 사용 가능한 템플릿 목록에 대한 백그라운드 업데이트를 사용하거나 사용하지 않도록 설정할 수 있습니다. 템플릿은 페이지가 컬렉션에 저장되어 있을 때 웹 페이지에서 서식 있는 메타데이터를 추출하는 데 사용됩니다.

이 설정을 사용하거나 설정을 구성하지 않으면 사용 가능한 템플릿 목록이 24시간마다 Microsoft 서비스에서 백그라운드로 다운로드됩니다.

이 설정을 사용하지 않으면 필요할 때 사용 가능한 템플릿 목록이 다운로드됩니다. 이러한 유형의 다운로드는 컬렉션 및 기타 기능에 대한 성능 저하를 일으킬 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: BackgroundTemplateListUpdatesEnabled
  - GP 이름: 컬렉션 및 템플릿을 사용하는 기타 기능의 사용 가능한 템플릿 목록에 대한 백그라운드 업데이트를 사용하도록 설정합니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: BackgroundTemplateListUpdatesEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: BackgroundTemplateListUpdatesEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### BingAdsSuppression
  #### Bing 검색 결과에서 모든 광고 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 83 이상

  #### 설명
  Bing.com에서 광고 없는 검색 환경을 설정합니다.

이 정책을 사용하면 사용자가 bing.com에서 광고 없는 검색 환경에서 검색할 수 있습니다. 동시에 SafeSearch 설정은 '엄격함'으로 설정되고 사용자가 변경할 수 없습니다.

이 정책을 구성하지 않으면 기본 환경은 bing.com에서 검색 결과에 광고를 포함합니다. SafeSearch는 기본적으로 '보통'으로 설정되며 사용자가 변경할 수 있습니다.

이 정책은 Microsoft에서 교육용 테넌트로 식별된 초등 및 중등 교육 SKU에서만 사용할 수 있습니다.

이 정책에 대한 자세한 내용을 알아보려고 하거나 다음 시나리오가 적용되는 경우 [https://go.microsoft.com/fwlink/?linkid=2119711](https://go.microsoft.com/fwlink/?linkid=2119711)을 참조하세요.

* EDU 테넌트가 있지만, 정책이 작동하지 않습니다.

* 광고 없는 검색 환경을 위해 IP를 목록에 올렸습니다.

* Microsoft Edge 레거시에서 광고 없는 검색 환경을 경험했으며 새 버전의 Microsoft Edge로 업그레이드하려고 합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: BingAdsSuppression
  - GP 이름: Bing 검색 결과에서 모든 광고 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: BingAdsSuppression
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: BingAdsSuppression
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### BlockThirdPartyCookies
  #### 타사 쿠키 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  주소 표시줄에 있는도메인에서 비롯되지 않은 웹 페이지 요소가 쿠키를 설정하지 못하도록 차단합니다.

이 정책을 사용하면 주소 표시줄에 있는도메인에서 비롯되지 않은 웹 페이지 요소가 쿠키를 설정할 수 없습니다.

이 정책을 사용하지 않으면 주소 표시줄 이외의도메인에 있는 웹 페이지 요소에서 쿠키를 설정할 수 있습니다.

이 정책을 구성하지 않으면 타사 쿠키가 사용하도록 설정되지만 사용자가 이 설정을 변경할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: BlockThirdPartyCookies
  - GP 이름: 타사 쿠키 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: BlockThirdPartyCookies
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: BlockThirdPartyCookies
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### BrowserAddProfileEnabled
  #### ID 플라이아웃 메뉴 또는 설정 페이지에서 프로필 만들기 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  **프로필 추가** 옵션을 사용하여 새 프로필을 만들 수 있도록 허용합니다.
이 정책을 사용하거나 구성하지 않으면 Microsoft Edge에서 사용자가 ID 플라이아웃 메뉴 또는 설정 페이지에서 **프로필 추가**를 사용하여 새 프로필을 만들 수 있습니다.

이 정책을 사용하지 않으면 사용자가 ID 플라이아웃 메뉴 또는 설정 페이지에서 새 프로필을 추가할 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: BrowserAddProfileEnabled
  - GP 이름: ID 플라이아웃 메뉴 또는 설정 페이지에서 프로필 만들기 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: BrowserAddProfileEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: BrowserAddProfileEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### BrowserGuestModeEnabled
  #### 게스트 모드 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge에서 게스트 프로필을 사용하도록 허용하는 옵션을 사용합니다. 게스트 프로필의 경우, 브라우저는 기존 프로필에서 검색 데이터를 가져오지 않으며 모든 게스트 프로필이 닫힐 때 검색 데이터를 삭제합니다.

이 정책 설정을 사용하거나 구성하지 않으면 Microsoft Edge에서 사용자가 게스트 프로필을 탐색할 수 있도록 허용합니다.

이 정책을 사용하지 않으면 Microsoft Edge에서 사용자가 게스트 프로필을 탐색할 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: BrowserGuestModeEnabled
  - GP 이름: 게스트 모드 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: BrowserGuestModeEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: BrowserGuestModeEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### BrowserNetworkTimeQueriesEnabled
  #### 브라우저 네트워크 시간 서비스에 대한 쿼리 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  정확한 타임스탬프를 검색하기 위해 Microsoft Edge에서 때때로 브라우저 네트워크 시간 서비스에 쿼리를 보낼 수 없게 합니다.

이 정책을 사용하지 않으면 Microsoft Edge에서 브라우저 네트워크 시간 서비스에 쿼리를 보내는 것이 중지됩니다.

이 정책을 사용하거나 구성하지 않으면 Microsoft Edge에서 때때로 브라우저 네트워크 시간 서비스에 쿼리를 보냅니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: BrowserNetworkTimeQueriesEnabled
  - GP 이름: 브라우저 네트워크 시간 서비스에 대한 쿼리 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: BrowserNetworkTimeQueriesEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: BrowserNetworkTimeQueriesEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### BrowserSignin
  #### 브라우저 로그인 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용자가 자신의 계정으로 Microsoft Edge에 로그인하고 동기화 및 Single Sign On과 같은 계정 관련 서비스를 사용할 수 있는지 여부를 지정합니다. 동기화의 가용성을 제어하려면 대신 [SyncDisabled](#syncdisabled) 정책을 사용합니다.

이 정책을 'Disable'으(로) 설정한 경우 [NonRemovableProfileEnabled](#nonremovableprofileenabled)이(가) 브라우저 프로파일에서 자동으로 서명된 정책을 생성하지 않도록 설정하므로 [NonRemovableProfileEnabled](#nonremovableprofileenabled) 정책도 사용하지 않도록 설정해야 합니다. 두 정책이 모두 설정된 경우 Microsoft Edge은(는) '브라우저 로그인 사용 안 함' 정책을 사용하고 [NonRemovableProfileEnabled](#nonremovableprofileenabled)이(가) 사용 안 함으로 설정된 것처럼 작동합니다.

      이 정책을 'Enable'으(로) 설정하면 사용자가 브라우저에 로그인할 수 있습니다. 브라우저에 로그인한다고 해서 동기화가 기본적으로 설정되어 있는 것은 아닙니다. 이 기능을 사용하려면 사용자가 별도로 선택해야 합니다.

      이 정책을 'Force'(으)로 설정하면 사용자가 브라우저를 사용하려면 프로파일에 로그인해야 합니다. 기본적으로 도메인 관리자 또는 [SyncDisabled](#syncdisabled) 정책에서 동기화를 사용하지 않도록 설정하지 않은 경우 사용자가 계정에 동기화할지 여부를 선택할 수 있습니다. [BrowserGuestModeEnabled](#browserguestmodeenabled) 정책의 기본값은 false로 설정됩니다.

이 정책을 구성하지 않으면 사용자가 브라우저 로그인 옵션을 사용하도록 설정할지 여부를 결정하고 적합하다고 판단되는 대로 사용할 수 있습니다.

정책 옵션 매핑:

* Disable (0) = 브라우저 로그인 사용 안 함

* Enable (1) = 브라우저 로그인 사용

* Force (2) = 사용자가 브라우저를 사용하려면 로그인하도록 강제

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: BrowserSignin
  - GP 이름: 브라우저 로그인 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: BrowserSignin
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: BrowserSignin
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### BuiltInDnsClientEnabled
  #### 기본 제공 DNS 클라이언트 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  기본 제공 DNS 클라이언트를 사용할지 여부를 제어합니다.

사용되는 DNS 서버에는 영향을 주지 않으며, 해당 서버와 통신하는 데 사용되는 소프트웨어 스택에만 영향을 줍니다. 예를 들어 운영 체제가 엔터프라이즈 DNS 서버를 사용하도록 구성된 경우 기본 제공 DNS 클라이언트가 동일한 서버를 사용합니다. 그러나 기본 제공 DNS 클라이언트는 DNS-over-TLS와 같은 최신 DNS 관련 프로토콜을 사용하여 서버를 다양한 방식으로 처리할 수 있습니다.

이 정책을 사용하면 기본 제공 DNS 클라이언트가 사용됩니다(사용 가능한 경우).

이 정책을 사용하지 않으면 클라이언트가 사용되지 않습니다.

이 정책을 구성하지 않으면 기본 제공 DNS 클라이언트가 MacOS에서 기본적으로 사용되며 사용자는 edge://flags를 편집하거나 명령줄 플래그를 지정하여 기본 제공 DNS 클라이언트를 사용할지 여부를 변경할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: BuiltInDnsClientEnabled
  - GP 이름: 기본 제공 DNS 클라이언트 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: BuiltInDnsClientEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: BuiltInDnsClientEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### BuiltinCertificateVerifierEnabled
  #### 서버 인증서를 확인 하는 데 기본 제공 인증서 검증 도구를 사용할지 여부를 결정 합니다. (사용되지 않음)
  >사용되지 않음: 이 정책은 더 이상 사용되지 않습니다. 현재 지원되고 있으나 향후 릴리스에서는 사용되지 않을 예정입니다.
  
  #### 지원되는 버전:
  - macOS 83 이상부터

  #### 설명
  이 정책은 회사에서 기본 제공 인증서 검증기와 호환되지 않는 경우 환경을 업데이트하고 문제를 보고하는 데 더 많은 시간을 제공하기 위한 단기간 메커니즘만으로 서비스를 제공할 목적을 가지고 있으므로 사용되지 않습니다.

Mac OS X에 대한 레거시 인증서 검증기에 대한 지원이 제거될 예정인 경우, Microsoft Edge 버전 87에서 작동하지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  

  #### Mac 정보 및 설정
  - 기본 설정 키 이름: BuiltinCertificateVerifierEnabled
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### CertificateTransparencyEnforcementDisabledForCas
  #### subjectPublicKeyInfo 해시 목록에 대한 인증서 투명성 적용 사용 안 함
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  subjectPublicKeyInfo 해시 목록에 대한 인증서 투명성 요구 사항의 적용을 사용하지 않도록 설정합니다.

이 정책은 지정된 subjectPublicKeyInfo 해시 중 하나를 사용하여 인증서를 포함하는 인증서 체인에 대한 인증서 투명성 공개 요구 사항을 사용하지 않도록 설정할 수 있습니다. 제대로 공개되지 않았기 때문에 이 정책을 사용하지 않으면 신뢰할 수 없는 것이 되는 인증서가 엔터프라이즈 호스트에 계속 사용될 수 있습니다.

이 정책을 설정할 때 인증서 투명성 적용을 사용하지 않으려면 다음 조건 집합 중 하나가 충족되어야 합니다.
1. 해시는 서버 인증서의 subjectPublicKeyInfo입니다.
2. 해시는 인증서 체인에 있는 CA 인증서에 표시되는 subjectPublicKeyInfo의 해시이며, 해당 CA 인증서는 X.509v3 nameConstraints 확장을 통해 제한되며, 하나 이상의 directoryName nameConstraints가 permittedSubtrees에 있고 directoryName에 organizationName 특성이 포함되어 있습니다.
3. 해시는 인증서 체인에 있는 CA 인증서에 표시되는 subjectPublicKeyInfo의 해시이며, CA 인증서에는 인증서 Subject에 하나 이상의 organizationName 특성이 있으며, 서버의 인증서에는 동일한 순서로 바이트 단위의 동일한 값인 동일한 수의 organizationName 특성이 포함되어 있습니다.

해시 알고리즘 이름, "/" 문자 및 지정된 인증서의 DER로 인코딩된 subjectPublicKeyInfo에 적용된 해당 해시 알고리즘의 Base64 인코딩을 연결하여 subjectPublicKeyInfo 해시를 지정합니다. 이 Base64 인코딩은 RFC 7469, 섹션 2.4에 정의된 SPKI 지문과 동일한 형식입니다. 인식할 수 없는 해시 알고리즘은 무시됩니다. 현재 지원되는 유일한 해시 알고리즘은 "sha256"입니다.

이 정책을 사용하지 않거나 구성하지 않으면 인증서 투명성 정책에 따라 공개되지 않으면 인증서 투명성을 통해 공개해야 하는 인증서는 신뢰할 수 없는 것으로 처리됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: CertificateTransparencyEnforcementDisabledForCas
  - GP 이름: subjectPublicKeyInfo 해시 목록에 대한 인증서 투명성 적용 사용 안 함
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\2 = "sha256//////////////////////w=="

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: CertificateTransparencyEnforcementDisabledForCas
  - 예제 값:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### CertificateTransparencyEnforcementDisabledForLegacyCas
  #### 레거시 인증 기관 목록에 대 한 인증서 투명도 적용 사용 안 함
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  레거시 CA(인증 기관) 목록에 대한 인증서 투명성 요구 사항의 적용을 사용하지 않도록 설정합니다.

이 정책을 사용하면 지정된 subjectPublicKeyInfo 해시 중 하나를 사용하여 인증서를 포함하는 인증서 체인에 대한 인증서 투명성 공개 요구 사항을 사용하지 않도록 설정할 수 있습니다. 적절하게 공개되지 않았기 때문에 이 정책을 사용하지 않으면 신뢰할 수 없는 것이 되는 인증서가 엔터프라이즈 호스트에 계속 사용됩니다.

인증서 투명성 적용을 사용하지 않으려면 레거시 CA(인증 기관)로 인식되는 CA 인증서에 표시되는 subjectPublicKeyInfo 해시를 설정해야 합니다. 레거시 CA는 Microsoft Edge에서 지원하는 하나 이상의 운영 체제에서 기본값으로 공개적으로 신뢰할 수 있는 CA입니다.

해시 알고리즘 이름, "/" 문자 및 지정된 인증서의 DER로 인코딩된 subjectPublicKeyInfo에 적용된 해당 해시 알고리즘의 Base64 인코딩을 연결하여 subjectPublicKeyInfo 해시를 지정합니다. 이 Base64 인코딩은 RFC 7469, 섹션 2.4에 정의된 SPKI 지문과 동일한 형식입니다. 인식할 수 없는 해시 알고리즘은 무시됩니다. 현재 지원되는 유일한 해시 알고리즘은 "sha256"입니다.

이 정책을 구성하지 않으면, 인증서 투명성을 통해 공개해야 하는 인증서는 인증서 투명성 정책에 따라 공개되지 않으면 신뢰할 수 없는 것으로 인증서는 처리됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: CertificateTransparencyEnforcementDisabledForLegacyCas
  - GP 이름: 레거시 인증 기관 목록에 대 한 인증서 투명도 적용 사용 안 함
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\2 = "sha256//////////////////////w=="

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: CertificateTransparencyEnforcementDisabledForLegacyCas
  - 예제 값:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### CertificateTransparencyEnforcementDisabledForUrls
  #### 특정 URL에 대한 인증서 투명성 적용 사용 안 함
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  나열된 URL에 대해 강제 인증서 투명성 요구 사항을 사용하지 않도록 설정합니다.

이 정책을 사용하면 인증서 투명성을 통해 지정한 URL의 호스트 이름에 대한 인증서를 공개하지 않을 수 있습니다. 따라서 적절하게 공개되지 않았기 때문에 이 정책을 사용하지 않으면 신뢰할 수 없는 것이 되는 인증서를 사용할 수 있지만 해당 호스트에 대해 잘못 발급된 인증서를 검색하기가 더 어려워집니다.

[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)에 따라 URL 패턴을 구성합니다. 인증서는 구성표, 포트 또는 경로와 관계없이 지정된 호스트 이름에 대해 유효하기 때문에 URL의 호스트 이름 부분만 고려됩니다. 와일드카드 호스트는 지원되지 않습니다.

이 정책을 구성하지 않으면 인증서 투명성을 통해 공개해야 하는 공개되지 않은 경우 신뢰할 수 없는 것으로 처리됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: CertificateTransparencyEnforcementDisabledForUrls
  - GP 이름: 특정 URL에 대한 인증서 투명성 적용 사용 안 함
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\2 = ".contoso.com"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: CertificateTransparencyEnforcementDisabledForUrls
  - 예제 값:
``` xml
<array>
  <string>contoso.com</string>
  <string>.contoso.com</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ClearBrowsingDataOnExit
  #### Microsoft Edge가 닫힐 때 검색 데이터 지우기
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 78 이상

  #### 설명
  Microsoft Edge은(는) 닫힐 때 기본적으로 검색 데이터를 지우지 않습니다. 검색 데이터에는 양식에 입력한 정보, 암호와 방문한 웹 사이트도 포함됩니다.

이 정책을 사용하면 Microsoft Edge이(가) 닫힐 때마다 모든 검색 데이터가 삭제됩니다. 이 정책을 사용하면 사용자가 구성한 방식보다 우선합니다.[DefaultCookiesSetting](#defaultcookiessetting)

이 정책을 사용하지 않도록 설정하거나 구성하지 않으면 사용자가 설정에서 검색 데이터 지우기 옵션을 구성할 수 있습니다.

이 정책을 사용하는 경우 [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) 또는 [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit) 정책은 모두 검색 데이터의 삭제를 다루므로 구성하지 마세요. 선행 정책 및 이 정책을 구성하는 경우 사용자가 [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) 또는 [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)을(를) 구성한 방식에 상관 없이 Microsoft Edge이(가) 닫힐 때 모든 검색 데이터가 삭제됩니다.

종료 시 쿠키를 삭제하지 않으려면 [SaveCookiesOnExit](#savecookiesonexit) 정책을 구성하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ClearBrowsingDataOnExit
  - GP 이름: Microsoft Edge가 닫힐 때 검색 데이터 지우기
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: ClearBrowsingDataOnExit
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ClearBrowsingDataOnExit
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ClearCachedImagesAndFilesOnExit
  #### Microsoft Edge 닫을 때 캐시 된 이미지 및 파일을 지웁니다.
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 83 이상

  #### 설명
  Microsoft Edge 이 닫힐 때 기본적으로 캐시 된 이미지와 파일을 지우지 않습니다.

이 정책을 사용 하면 Microsoft Edge 닫힐 때마다 캐시 된 이미지와 파일이 삭제 됩니다 .

이 정책을 사용 하지 않으면 사용자가 edge://settings/clearBrowsingDataOnClose에서 캐시 된 이미지 및 파일 옵션을 구성할 수 없습니다.

이 정책을 구성 하지 않으면 사용자가 종료 시 캐시 된 이미지와 파일을 지울 것인지 여부를 선택할 수 있습니다.

이 정책을 사용 하지 않도록 설정 하는 경우 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 정책이 데이터 삭제를 처리 하기 때문에이 정책을 사용 하지 마십시오. 둘 다 구성 하는 경우 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 정책이 우선 하며[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit) 구성한 방식에 관계 없이 Microsoft Edge 닫을 때 모든 데이터를 삭제 합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ClearCachedImagesAndFilesOnExit
  - GP 이름: Microsoft Edge 닫을 때 캐시 된 이미지 및 파일을 지웁니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: ClearCachedImagesAndFilesOnExit
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ClearCachedImagesAndFilesOnExit
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ClickOnceEnabled
  #### 사용자가 ClickOnce 프로토콜을 사용하여 파일을 열 수 있도록 허용
  
  
  #### 지원되는 버전:
  - Windows 78 이상부터

  #### 설명
  사용자가 ClickOnce 프로토콜을 사용하여 파일을 열 수 있도록 허용 합니다. ClickOnce 프로토콜을 사용하면 웹 사이트에서 사용자의 컴퓨터나 장치에 있는 ClickOnce 파일 처리기를 사용하여 특정 URL의 파일을 브라우저에서 열도록 요청할 수 있습니다.

이 정책을 사용하면 사용자는 ClickOnce 프로토콜을 사용하여 파일을 열 수 있습니다. 이 정책은 edge://flags/ 페이지에 있는 사용자의 ClickOnce 설정보다 우선시 됩니다.

이 정책을 사용하지 않으면 사용자가 ClickOnce 프로토콜을 사용하 여 파일을 열 수 없습니다. 대신 파일은 브라우저를 사용하여 파일 시스템에 저장됩니다. 이 정책은 edge://flags/ 페이지에 있는 사용자의 ClickOnce 설정보다 우선시 됩니다.

이 정책을 구성하지 않으면 Microsoft Edge 87 이전의 Microsoft Edge 버전을 사용하는 사용자는 기본적으로 ClickOnce 프로토콜을 사용하여 파일을 열 수 없습니다. 그러나 해당 사용자는 edge://flags/ 페이지에서 ClickOnce 프로토콜을 사용할 수 있도록 설정하는 옵션을 사용할 수 있습니다. Microsoft Edge 버전 87 이상을 사용하는 사용자는 기본적으로 ClickOnce 프로토콜을 사용하여 파일을 열 수 있지만 edge://flags/ 페이지에서 ClickOnce 프로토콜을 사용하지 않도록 선택할 수 있습니다.

ClickOnce를 사용하지 않도록 설정하면 ClickOnce 응용 프로그램(.application 파일)이 제대로 시작되지 않을 수 있습니다.

ClickOnce에 대한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) 및 [https://go.microsoft.com/fwlink/?linkid=2099880](https://go.microsoft.com/fwlink/?linkid=2099880)를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ClickOnceEnabled
  - GP 이름: 사용자가 ClickOnce 프로토콜을 사용하여 파일을 열 수 있도록 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ClickOnceEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### CollectionsServicesAndExportsBlockList
  #### 지정된 서비스 목록에 대한 액세스 차단 및 컬렉션에서 대상 내보내기
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  Microsoft Edge의 모음 기능에서 사용자가 액세스할 수 없는 특정 서비스 및 내보내기 대상을 나열합니다. 여기에는 Bing에서 추가 데이터를 표시하고 Microsoft 제품 또는 외부 파트너에게 컬렉션을 내보내는 작업이 포함됩니다.

이 정책을 사용하면 지정된 목록과 일치하는 서비스 및 내보내기 대상이 차단됩니다.

이 정책을 구성하지 않으면 허용 가능한 서비스 및 내보내기 대상에 대한 제한 사항이 적용되지 않습니다.

정책 옵션 매핑:

* pinterest_suggestions (pinterest_suggestions) = Pinterest 제안

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: CollectionsServicesAndExportsBlockList
  - GP 이름: 지정된 서비스 목록에 대한 액세스 차단 및 컬렉션에서 대상 내보내기
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\1 = "pinterest_suggestions"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: CollectionsServicesAndExportsBlockList
  - 예제 값:
``` xml
<array>
  <string>pinterest_suggestions</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### CommandLineFlagSecurityWarningsEnabled
  #### 명령줄 플래그에 대한 보안 경고 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 78 이상

  #### 설명
  이 정책을 사용하지 않으면 잠재적으로 위험한 명령줄 플래그를 사용하여 Microsoft Edge를 시작할 보안 경고가 표시되지 않습니다.

사용하거나 설정하지 않으면 이러한 명령줄 플래그를 사용하여 Microsoft Edge를 시작할 때 보안 경고가 표시됩니다.

예를 들어, --disable-gpu-sandbox 플래그는 다음 경고를 생성합니다. 지원되지 않는 명령줄 플래그(--disable-gpu-sandbox)를 사용하고 있습니다. 이 플래그는 안전성과 보안 위험을 초래합니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: CommandLineFlagSecurityWarningsEnabled
  - GP 이름: 명령줄 플래그에 대한 보안 경고 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: CommandLineFlagSecurityWarningsEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: CommandLineFlagSecurityWarningsEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ComponentUpdatesEnabled
  #### Microsoft Edge에서 구성 요소 업데이트 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  이 정책을 사용하거나 구성하지 않으면 Microsoft Edge에서 구성 요소 업데이트를 사용할 수 있습니다.

이 정책을 사용하지 않거나 false로 설정하면 Microsoft Edge의 모든 구성 요소에 대해 구성 요소 업데이트를 사용할 수 없습니다.

그러나 일부 구성 요소는 이 정책에서 제외됩니다. 여기에는 실행 코드를 포함하지 않거나 브라우저의 동작이 크게 변경되지 않거나 보안을 위해 중요한 구성 요소가 포함됩니다. 즉, "보안을 위해 중요한" 업데이트라고 간주되는 업데이트는 이 정책을 사용하지 않도록 설정한 경우에도 계속 적용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ComponentUpdatesEnabled
  - GP 이름: Microsoft Edge에서 구성 요소 업데이트 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ComponentUpdatesEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ComponentUpdatesEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ConfigureDoNotTrack
  #### 추적 안 함 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  추적 정보를 요청하는 웹 사이트에 추적 안 함 요청을 보낼지 여부를 지정합니다. 추적 안 함 요청은 사용자가 방문하는 웹 사이트에 사용자의 검색 활동을 추적하지 못하도록 한다는 것을 알려줍니다. 기본적으로 Microsoft Edge는 추적 안 함 요청을 보내지 않지만 사용자는 이 기능을 사용하여 보낼 수 있습니다.

이 정책을 사용하면 항상 추적 안 함 요청이 추적 정보를 요청하는 웹 사이트로 전송됩니다.

이 정책을 사용하지 않으면 요청이 전송되지 않습니다.

이 정책을 구성하지 않으면 사용자가 이러한 요청을 보낼지 여부를 선택할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ConfigureDoNotTrack
  - GP 이름: 추적 안 함 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ConfigureDoNotTrack
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ConfigureDoNotTrack
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ConfigureOnPremisesAccountAutoSignIn
  #### Azure AD 도메인 계정이 없을 때 Active Directory 도메인 계정으로 자동 로그인 구성
  
  
  #### 지원되는 버전:
  - Windows 81 이상부터

  #### 설명
  사용자의 컴퓨터가 도메인에 가입되어 있고 환경이 하이브리드에 가입되어 있지 않은 경우 Active Directory 계정을 사용하여 자동 로그인할 수 있습니다. 사용자가 Azure Active Directory 계정으로 자동 로그인하려면 사용자 환경에 Azure AD 가입([https://go.microsoft.com/fwlink/?linkid=2118197](https://go.microsoft.com/fwlink/?linkid=2118197) 참조) 또는 하이브리드 가입(자세한 정보는 [https://go.microsoft.com/fwlink/?linkid=2118365](https://go.microsoft.com/fwlink/?linkid=2118365) 참조)을 하십시오.

[BrowserSignin](#browsersignin) 정책을 사용하지 않도록 구성한 경우 이 정책이 적용되지 않습니다.

이 정책을 사용하도록 설정하고 'SignInAndMakeDomainAccountNonRemovable'로 설정하면 Microsoft Edge이(가) Active Directory 계정을 사용하여 도메인 가입 시스템에 있는 사용자를 자동으로 로그인합니다.

이 정책을 'Disabled'(으)로 설정하거나 설정하지 않으면 Microsoft Edge이(가) Active Directory 계정이 있는 도메인에 가입한 시스템에 있는 사용자를 자동으로 로그인하지 않습니다.

정책 옵션 매핑:

* Disabled (0) = 사용 안 함

* SignInAndMakeDomainAccountNonRemovable (1) = 로그인하여 도메인 계정을 제거할 수 없도록 설정

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ConfigureOnPremisesAccountAutoSignIn
  - GP 이름: Azure AD 도메인 계정이 없을 때 Active Directory 도메인 계정으로 자동 로그인 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ConfigureOnPremisesAccountAutoSignIn
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ConfigureOnlineTextToSpeech
  #### 온라인 텍스트 음성 변환 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Azure인식 서비스의 한 부분인 브라우저에서 온라인 텍스트 음성 변환 글꼴을 활용할 수 있는지 여부를 설정합니다.

이 정책을 사용하거나 구성하지 않으면 SpeechSynthesis API를 사용하는 웹 기반 응용 프로그램에서 온라인 텍스트 음성 변환 글꼴을 사용할 수 있습니다.

사이 정책을 사용하지 않으면 음성 글꼴을 사용할 수 없습니다.

이 기능에 대한 자세한 내용은 다음을 참조하세요:
SpeechSynthesis API: [https://go.microsoft.com/fwlink/?linkid=2110038](https://go.microsoft.com/fwlink/?linkid=2110038)
인식 서비스: [https://go.microsoft.com/fwlink/?linkid=2110141](https://go.microsoft.com/fwlink/?linkid=2110141)

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ConfigureOnlineTextToSpeech
  - GP 이름: 온라인 텍스트 음성 변환 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ConfigureOnlineTextToSpeech
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ConfigureOnlineTextToSpeech
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ConfigureShare
  #### 공유 환경 구성
  
  
  #### 지원되는 버전:
  - Windows 83 이상부터

  #### 설명
  이 정책을 '공유 허용됨'(기본값)으로 설정하면 사용자는 Microsoft Edge의 설정 및 추가 메뉴에서 WIndows 10 공유 환경에 액세스하여 시스템의 다른 앱과 공유할 수 있습니다.

이 정책을 'ShareDisabled'로 설정하면 사용자가 Windows 10 공유 환경에 액세스할 수 없습니다. Share(공유) 버튼이 도구 모음에 있으면 해당 버튼도 숨겨집니다.

정책 옵션 매핑:

* ShareAllowed (0) = 공유 환경 사용 허용

* ShareDisallowed (1) = 공유 환경 사용 허용 안 함

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ConfigureShare
  - GP 이름: 공유 환경 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ConfigureShare
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### CustomHelpLink
  #### 사용자 지정 도움말 링크 지정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 79 이상

  #### 설명
  도움말 메뉴 또는 F1 키에 대한 링크를 지정합니다.

이 정책을 사용하면 관리자가 도움말 메뉴 또는 F1 키에 대한 링크를 지정할 수 있습니다.

이 정책을 사용하지 않거나 구성하지 않으면 도움말 메뉴 또는 F1 키에 대한 기본 링크가 사용됩니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: CustomHelpLink
  - GP 이름: 사용자 지정 도움말 링크 지정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: CustomHelpLink
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"https://go.microsoft.com/fwlink/?linkid=2080734"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: CustomHelpLink
  - 예제 값:
``` xml
<string>https://go.microsoft.com/fwlink/?linkid=2080734</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DNSInterceptionChecksEnabled
  #### DNS 가로채기 검사 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 80 이상

  #### 설명
  정책은 DNS 가로채기 검사를 사용하지 않도록 설정하는 데 사용할 수 있는 로컬 스위치를 구성합니다. 이 검사는 브라우저가 알 수 없는 호스트 이름을 리디렉션하는 프록시 뒤에 있는지 확인합니다.

네트워크 구성이 알려진 엔터프라이즈 환경에서는 이 검색이 필요하지 않을 수 있습니다. 시작 시 추가 DNS 및 HTTP 트래픽과 각 DNS 구성 변경을 피하기 위해 사용하지 않도록 설정할 수 있습니다.

이 정책을 사용하지 않거나 설정하지 않으면 DNS 가로채기 검사가 수행됩니다.

이 정책을 사용하지 않으면 이 정책에서는 DNS 가로채기 검사가 수행되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DNSInterceptionChecksEnabled
  - GP 이름: DNS 가로채기 검사 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DNSInterceptionChecksEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DNSInterceptionChecksEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultBrowserSettingEnabled
  #### Microsoft Edge를 기본 브라우저로 설정
  
  
  #### 지원되는 버전:
  - Windows 7 및 macOS 이후 77 이상

  #### 설명
  이 정책을 True로 설정하면 Microsoft Edge는 시작할 때 항상 기본 브라우저인지 여부를 확인하고, 가능한 경우 자동으로 자체 등록합니다.

이 정책을 False로 설정하면 Microsoft Edge는 기본값인지 확인하지 않으며 이 옵션을 설정할 수 있는 사용자 컨트롤을 끕니다.

이 정책을 구성하지 않으면 Microsoft Edge를 통해 사용자가 기본 브라우저인지 여부와 그렇지 않을 경우 사용자 알림을 표시할지 여부를 제어할 수 있습니다.

Windows 관리자 참고 사항: 이 정책은 Windows 7을 실행하는 PC에서만 작동합니다. 이후 버전의 Windows에서는 Microsoft Edge를 https 및 http 프로토콜(및 선택적으로 .html, .htm, .pdf, .svg, .webp와 같은 ftp 프로토콜 및 파일 형식)에 대한 처리기로 만드는 "기본 응용 프로그램 연결" 파일을 배포해야 합니다. 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2094932](https://go.microsoft.com/fwlink/?linkid=2094932)를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultBrowserSettingEnabled
  - GP 이름: Microsoft Edge를 기본 브라우저로 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DefaultBrowserSettingEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultBrowserSettingEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultSearchProviderContextMenuAccessAllowed
  #### 기본 검색 공급자 컨텍스트 메뉴 검색 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 85 이상

  #### 설명
  컨텍스트 메뉴에서 기본 검색 공급자를 사용할 수 있습니다.

이 정책을 사용하지 않도록 설정하면 기본 검색 공급자 및 사이드바 검색에 의존하는 검색 컨텍스트 메뉴 항목을 사용할 수 없습니다.

이 정책을 사용하도록 설정했거나 설정하지 않은 경우 기본 검색 공급자 및 사이드바 검색에 대한 컨텍스트 메뉴 항목을 사용할 수 있습니다.

정책 값은 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 정책이 활성화된 경우에만 적용되며, 그렇지 않은 경우에는 적용되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultSearchProviderContextMenuAccessAllowed
  - GP 이름: 기본 검색 공급자 컨텍스트 메뉴 검색 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DefaultSearchProviderContextMenuAccessAllowed
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultSearchProviderContextMenuAccessAllowed
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultSensorsSetting
  #### 기본 센서 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  웹 사이트가 모션 및 광 센서와 같은 센서에 액세스하고 사용할 수 있는지 여부를 설정합니다. 웹 사이트에서 센서에 대한 액세스를 완전히 차단하거나 허용할 수 있습니다.

정책을 1로 설정하면 웹 사이트에서 센서에 액세스하고 사용할 수 있습니다. 정책을 2로 설정하면 센서에 대한 액세스가 거부됩니다.

[SensorsAllowedForUrls](#sensorsallowedforurls) 및 [SensorsBlockedForUrls](#sensorsblockedforurls) 정책을 사용하여 특정 URL 패턴에 대해 이 정책을 재정의 할 수 있습니다.

이를 구성하지 않는 경우 정책에 따라 웹 사이트에서 센서에 액세스하고 사용할 수 있으며 사용자는 이 설정을 변경할 수 있습니다. 이 설정은 [SensorsAllowedForUrls](#sensorsallowedforurls) 및 [SensorsBlockedForUrls](#sensorsblockedforurls)의 전역 기본값입니다.

정책 옵션 매핑:

* AllowSensors (1) = 사이트에서 센서에 액세스하도록 허용

* BlockSensors (2) = 어떤 사이트도 센서에 액세스하도록 허용하지 않습니다.

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultSensorsSetting
  - GP 이름: 기본 센서 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DefaultSensorsSetting
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultSensorsSetting
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DefaultSerialGuardSetting
  #### 직렬 API의 사용 제어
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  웹 사이트에서 직렬 포트에 액세스할 수 있는지 여부를 설정합니다. 웹 사이트에서 직렬 포트에 액세스하려고 할 때마다 액세스를 완전히 차단하거나 사용자에게 요청할 수 있습니다.

정책을 3으로 설정하면 웹 사이트에서 직렬 포트에 대한 액세스를 요청할 수 있습니다. 이 정책을 2로 설정하면 직렬 포트에 대한 액세스를 거부합니다.

[SerialAskForUrls](#serialaskforurls) 및 [SerialBlockedForUrls](#serialblockedforurls) 정책을 사용하여 특정 URL 패턴에 대해 해당 정책을 재정의할 수 있습니다.

이 정책을 구성하지 않으면 기본적으로 웹 사이트에서 직렬 포트에 액세스할 수 있는지와 사용자가 해당 설정을 변경할 수 있는지 여부를 사용자에게 요청할 수 있습니다.

정책 옵션 매핑:

* BlockSerial (2) = 모든 사이트에서 직렬 API를 통해 직렬 포트에 대한 액세스 권한을 요청할 수 없도록 허용

* AskSerial (3) = 사이트에서 직렬 포트에 액세스할 수 있는 사용자 권한을 요청할 수 있도록 허용

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DefaultSerialGuardSetting
  - GP 이름: 직렬 API의 사용 제어
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DefaultSerialGuardSetting
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DefaultSerialGuardSetting
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DelayNavigationsForInitialSiteListDownload
  #### 탭 탐색 이전에 엔터프라이즈 모드 사이트 목록을 사용할 수 있어야 합니다.
  
  
  #### 지원되는 버전:
  - Windows 84 이상부터

  #### 설명
  브라우저가 초기 엔터프라이즈 모드 사이트 목록을 다운로드할 때까지 Microsoft Edge 탭 탐색 대기 여부를 지정할 수 있습니다. 해당 설정은 브라우저 홈 페이지를 Internet Explorer 모드로 로드해야 하는 시나리오용으로 설정되었으며 처음으로 브라우저를 실행하기 전에 IE 모드를 설정하는 것이 중요합니다. 해당 시나리오가 없는 경우 홈 페이지를 로드하는 성능을 저하시킬 수 있기 때문에 해당 설정을 사용하지 않는 것이 좋습니다. 해당 설정은 브라우저를 처음 실행하기 전에 IE 모드를 설정해야 하는 경우와 같이 Microsoft Edge에 캐싱된 엔터프라이즈 모드 사이트 목록이 없는 경우에만 적용됩니다.

해당 설정은
와 함께 작동하며        [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)은 "IE 모드" (1)
및
목록에 항목이 한 개 이상 있는[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) 정책으로 설정됩니다.

[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout) 정책을 사용하여 해당 정책의 시간 제한 동작을 구성할 수 있습니다.

해당 정책을 All(으)로 설정하는 경우 Microsoft Edge에 엔터프라이즈 모드 사이트 목록의 캐시 버전이 없으면 브라우저가 사이트 목록을 다운로드할 때까지 탭은 탐색을 지연합니다. 사이트 목록을 통해 Internet Explorer 모드에서 열리도록 구성된 사이트는 브라우저를 처음 탐색하는 중에도 Internet Explorer 모드로 로드됩니다. Http:, https:, file:, ftp: 외의 다른 체계가 있는 사이트와 같이 Internet Explorer에서 열리도록 구성될 수 없는 사이트는 Edge 모드에서 즉시 탐색 및 로드를 지연시키지 않아야 합니다.

해당 정책을 None(으)로 설정하거나 구성하지 않는 경우 Microsoft Edge에 엔터프라이즈 모드 사이트 목록의 캐시된 버전이 없으면 탭에서 즉시 탐색하고 브라우저의 엔터프라이즈 모드 사이트 목록 다운로드 작업을 대기하지 않습니다. 사이트 목록에서 Internet Explorer 모드로 열도록 구성된 사이트는 브라우저에서 엔터프라이즈 모드 사이트 목록의 다운로드를 완료할 때까지 Microsoft Edge 모드로 열립니다.

정책 옵션 매핑:

* None (0) = 없음

* All (1) = 모든 적격 탐색

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DelayNavigationsForInitialSiteListDownload
  - GP 이름: 탭 탐색 이전에 엔터프라이즈 모드 사이트 목록을 사용할 수 있어야 합니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DelayNavigationsForInitialSiteListDownload
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DeleteDataOnMigration
  #### 마이그레이션 시 이전 브라우저 데이터 삭제
  
  
  #### 지원되는 버전:
  - Windows 83 이상부터

  #### 설명
  이 정책은 Microsoft Edge 버전 81 이상으로 마이그레이션한 후 Microsoft Edge 레거시에서 사용자 검색 데이터를 삭제할지 여부를 결정합니다.

이 정책을 "사용"으로 설정한 경우 Microsoft Edge 버전 81 이상으로 마이그레이션한 후 Microsoft Edge 레거시에서 모든 검색 데이터가 삭제됩니다. 기존 검색 데이터에 영향을 미치려면 Microsoft Edge 버전 81 이상으로 마이그레이션하기 전에 이 정책을 설정해야 합니다.

이 정책을 "사용 안 함"으로 설정하거나 정책을 구성하지 않은 경우 Microsoft Edge 버전 83 이상으로 마이그레이션한 후에 사용자 검색 데이터가 삭제되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DeleteDataOnMigration
  - GP 이름: 마이그레이션 시 이전 브라우저 데이터 삭제
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DeleteDataOnMigration
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DeveloperToolsAvailability
  #### 개발자 도구를 사용할 수 있는 위치 제어
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  개발자 도구를 사용할 수 있는 위치를 제어합니다.

이 정책을 'DeveloperToolsDisallowedForForceInstalledExtensions'(0, 기본값)로 설정하면 사용자가 개발자 도구와 JavaScript 콘솔에 일반적으로 액세스할 수 있지만 엔터프라이즈 정책에 의해 설치된 확장의 컨텍스트에서는 액세스할 수 없습니다.

이 정책을 'DeveloperToolsAllowed'(1)로 설정하면 사용자가 엔터프라이즈 정책에 의해 설치된 확장을 포함하여 모든 컨텍스트에서 개발자 도구와 JavaScript 콘솔에 액세스할 수 있습니다.

이 정책을 'DeveloperToolsDisallowed'(2)로 설정하면 사용자가 개발자 도구에 액세스하거나 웹 사이트 요소를 검사할 수 없습니다. 개발자 도구나 JavaScript 콘솔을 여는 바로 가기 키와 메뉴 또는 상황에 맞는 메뉴 항목을 사용할 수 없습니다.

정책 옵션 매핑:

* DeveloperToolsDisallowedForForceInstalledExtensions (0) = 엔터프라이즈 정책에 의해 설치된 확장에서 개발자 도구 차단, 다른 컨텍스트에서는 허용

* DeveloperToolsAllowed (1) = 개발자 도구 사용 허용

* DeveloperToolsDisallowed (2) = 개발자 도구 사용 허용 안 함

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DeveloperToolsAvailability
  - GP 이름: 개발자 도구를 사용할 수 있는 위치 제어
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DeveloperToolsAvailability
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DeveloperToolsAvailability
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DiagnosticData
  #### 브라우저 사용 현황에 대한 필수 및 선택적인 진단 데이터 보내기
  
  
  #### 지원되는 버전:
  - Windows 7 및 macOS 이후 86 이상

  #### 설명
  이 정책은 브라우저 사용에 대해 필요한 선택적 진단 데이터를 Microsoft에 전송하는 작업을 제어합니다.

필수 진단 데이터를 수집하여 Microsoft Edge을(를) 정상적으로 수행할 수 있도록 안전하고 최신 상태로 유지하세요.

선택적 진단 데이터에는 브라우저, 방문 웹 사이트, 제품 및 서비스 개선을 위한 Microsoft의 충돌 보고서를 사용하는 방법에 대한 데이터가 포함됩니다.

이 정책은 Windows 10 장치에서 지원되지 않습니다. Windows 10에서 이 데이터 수집을 제어하려면 IT 관리자가 Windows 진단 데이터 그룹 정책을 사용해야 합니다. 이 정책은 Windows 버전에 따라 '원격 분석 허용' 또는 '진단 데이터 허용'이 될 수 있습니다. Windows 10 진단 데이터 수집에 대한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)를 참조하세요.

다음 설정 중 하나를 사용하여 이 정책을 구성하려면 다음을 수행하세요.

'Off'은(는) 필수 및 선택적 진단 데이터 수집을 끕니다. 이 옵션은 권장되지 않습니다.

‘RequiredData’는 필수 진단 데이터를 전송하지만 선택적 진단 데이터 수집을 끕니다. Microsoft Edge에서 필수 진단 데이터를 전송하여 Microsoft Edge을(를) 정상적으로 수행할 수 있도록 안전하고 최신 상태로 유지하세요.

‘OptionalData’는 브라우저 사용 현황, 방문 웹 사이트, 제품 및 서비스 개선을 위해 Microsoft에 전송된 충돌 보고서에 대한 데이터가 포함되어 있는 선택적 진단 데이터를 전송합니다.

Windows 7/MacOS에서 이 정책은 Microsoft로의 필수 및 선택적 데이터의 전송을 제어합니다.

이 정책을 구성하지 않거나 사용하지 않도록 설정하면 Microsoft Edge은(는) 기본적으로 사용자의 기본 설정이됩니다.

정책 옵션 매핑:

* Off (0) = 꺼짐(권장하지 않음)

* RequiredData (1) = 필수 데이터

* OptionalData (2) = 선택적 데이터

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DiagnosticData
  - GP 이름: 브라우저 사용 현황에 대한 필수 및 선택적인 진단 데이터 보내기
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DiagnosticData
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DiagnosticData
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DirectInvokeEnabled
  #### 사용자가 DirectInvoke 프로토콜을 사용하여 파일을 열 수 있도록 허용
  
  
  #### 지원되는 버전:
  - Windows 78 이상부터

  #### 설명
  사용자가 DirectInvoke 프로토콜을 사용하여 파일을 열 수 있도록 허용합니다. DirectInvoke 프로토콜은 웹 사이트에서 사용자의 컴퓨터나 장치에 있는 특정 파일 처리기를 사용하여 특정 URL의 파일을 브라우저에서 열도록 요청할 수 있습니다.

이 정책을 사용하거나 구성하지 않으면 사용자는 DirectInvoke 프로토콜을 사용하여 파일을 열 수 있습니다.

이 정책을 사용하지 않으면 사용자는 DirectInvoke 프로토콜을 사용하여 파일을 열 수 없습니다. 대신 파일은 파일 시스템에 저장됩니다.

참고: DirectInvoke를 사용하지 않도록 설정하면 특정 Microsoft SharePoint Online 기능이 예상대로 작동하지 않을 수 있습니다.

DirectInvoke에 대한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) 및 [https://go.microsoft.com/fwlink/?linkid=2099871](https://go.microsoft.com/fwlink/?linkid=2099871)를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DirectInvokeEnabled
  - GP 이름: 사용자가 DirectInvoke 프로토콜을 사용하여 파일을 열 수 있도록 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DirectInvokeEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### Disable3DAPIs
  #### 3D 그래픽 API에 대한 지원 사용 안 함
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  웹 페이지가 GPU(그래픽 처리 장치)에 액세스하지 못하도록 합니다. 특히 웹 페이지가 WebGL API에 액세스할 수 없으며 플러그 인은 Pepper 3D API를 사용할 수 없습니다.

이 정책을 구성하지 않거나 사용하지 않도록 설정하면 잠재적으로 웹 페이지가 WebGL API를 사용하고 플러그 인은 Pepper 3D API를 사용할 수 있습니다. Microsoft Edge는 기본적으로 이러한 API를 사용하기 위해 전달할 명령줄 인수가 여전히 필요합니다.

[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled) 정책이 false로 설정되면 'Disable3DAPIs' 정책에 대한 설정은 무시됩니다. 'Disable3DAPIs'정책을 true로 설정하는 것과 같습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: Disable3DAPIs
  - GP 이름: 3D 그래픽 API에 대한 지원 사용 안 함
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: Disable3DAPIs
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: Disable3DAPIs
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DisableScreenshots
  #### 스크린샷 찍기 사용 안 함
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용자가 브라우저 페이지의 스크린샷을 찍을 수 있는지 여부를 제어합니다.

이 정책을 사용하면 사용자가 바로 가기 키 또는 확장 API를 사용하여 스크린샷을 찍을 수 없습니다.

이 정책을 사용하지 않거나 구성하지 않으면 사용자가 스크린샷을 찍을 수 있습니다.

참고: 이 정책은 브라우저 자체에서 찍은 스크린샷을 제어합니다. 이 정책을 사용하도록 설정하는 경우에도 사용자는 운영 체제 기능이나 다른 응용 프로그램 사용하는 등의 일부 브라우저 외부의 방법을 사용하여 계속 스크린샷을 찍을 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DisableScreenshots
  - GP 이름: 스크린샷 찍기 사용 안 함
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DisableScreenshots
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DisableScreenshots
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DiskCacheDir
  #### 디스크 캐시 디렉터리 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  캐시된 파일을 저장하는 데 사용할 디렉터리를 구성합니다.

이 정책을 사용하면 Microsoft Edge 는 사용자가 '--disk-cache-dir' 플래그를 지정했는지 여부에 관계 없이 제공된 디렉터리를 사용합니다. Microsoft Edge에서 콘텐츠를 관리하므로 데이터 손실이나 기타 예기치 않은 오류가 발생하지 않도록 하려면 볼륨의 루트 디렉터리 또는 다른 목적으로 사용되는 디렉터리에 이 정책을 구성하지 마세요.

디렉터리 및 경로를 지정할 때 사용할 수 있는 변수 목록은 [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041)을 참조하세요.

이 정책을 구성하지 않으면 기본 캐시 디렉터리가 사용되며 사용자가 '--disk-cache-dir' 명령줄 플래그를 사용하여 해당 기본값을 재정의할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DiskCacheDir
  - GP 이름: 디스크 캐시 디렉터리 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DiskCacheDir
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"${user_home}/Edge_cache"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DiskCacheDir
  - 예제 값:
``` xml
<string>${user_home}/Edge_cache</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DiskCacheSize
  #### 디스크 캐시 크기를 바이트 단위로 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  디스크에 파일을 저장하는 데 사용되는 캐시 크기(바이트)를 구성합니다.

이 정책을 사용하면 Microsoft Edge는 사용자가 '--disk-cache-size' 플래그를 지정했는지 여부에 관계 없이 제공된 캐시 크기를 사용합니다. 이 정책에 지정된 값은 하드 경계가 아니라 캐싱 시스템에 대한 제안 사항입니다. 메가바이트 이하의 값은 너무 작아서 합리적인 최소값으로 반올림됩니다.

이 정책의 값을 0으로 설정하면 기본 캐시 크기가 사용되며 사용자가 변경할 수 없습니다.

이 정책을 구성하지 않으면 기본 크기가 사용되지만 사용자가 '--disk-cache-size' 플래그를 사용하여 재정의할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DiskCacheSize
  - GP 이름: 디스크 캐시 크기를 바이트 단위로 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DiskCacheSize
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x06400000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DiskCacheSize
  - 예제 값:
``` xml
<integer>104857600</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DnsOverHttpsMode
  #### DNS-over-HTTPS 모드 제어
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 83 이상

  #### 설명
  DNS over-HTTPS 해결 프로그램의 모드를 제어합니다. 이 정책에서는 각 쿼리의 기본 모드만 설정합니다. 이 모드는 DNS를 통한 HTTP 서버 호스트 이름을 확인하는 요청과 같은 특별한 유형의 쿼리를 재정의할 수 있습니다.

 "off" 모드를 DNS over-HTTPS를 사용할 수 없게 됩니다.

"automatic" 모드인 경우에는 DNS를 통한 HTTPS 서버를 사용할 수 있는 경우에는 먼저 DNS over HTTPS 쿼리를 전송하고 오류가 발생 하는 경우 안전하지 않은 쿼리를 보낼 수 있습니다.

 "secure" 모드는 DNS를 통해 HTTPS 쿼리만 보낼 뿐이며 오류 발생 시 해결되지 않습니다.

이 정책을 구성하지 않으면 브라우저가 사용자가 구성한 시스템 해결 프로그램에 연결된 해결 프로그램에 대한 DNS over HTTPS 요청을 보낼 수 있습니다.

정책 옵션 매핑:

* off (off) = DNS-over-HTTPS 설정 해제

* automatic (automatic) = 안전하지 않은 폴백으로 DNS-over-HTTPS 사용

* secure (secure) = 안전하지 않은 폴백 없이 DNS-over-HTTPS 사용

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DnsOverHttpsMode
  - GP 이름: DNS-over-HTTPS 모드 제어
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DnsOverHttpsMode
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"off"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DnsOverHttpsMode
  - 예제 값:
``` xml
<string>off</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DnsOverHttpsTemplates
  #### 원하는 DNS over HTTPS 확인 프로그램의 URI 템플릿을 지정합니다.
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 83 이상

  #### 설명
  원하는 DNS-over-HTTPS 확인자의 URI 템플릿입니다. 여러 DNS-over-HTTPS 확인자를 지정하려면 해당 URI 템플릿을 공백으로 구분합니다.

[DnsOverHttpsMode](#dnsoverhttpsmode)를 "secure"로 설정하면 이 정책이 설정되어야 하며 비워 둘 수 없습니다.

[DnsOverHttpsMode](#dnsoverhttpsmode)를 "automatic"(으)로 설정하고 이 정책이 설정되면 지정된 URI 템플릿이 사용됩니다. 이 정책을 설정하지 않으면 하드 코드된 매핑을 사용하여 사용자의 현재 DNS 확인자를 동일한 공급자가 운영하는 DoH 확인자로 업그레이드하려고 시도합니다.

URI 템플릿에 dns 변수가 포함되어 있으면 요청은 확인자에 대해 GET을 사용합니다. 그렇지 않으면 요청은 POST를 사용합니다.

잘못된 형식의 템플릿은 무시됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DnsOverHttpsTemplates
  - GP 이름: 원하는 DNS over HTTPS 확인 프로그램의 URI 템플릿을 지정합니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: DnsOverHttpsTemplates
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"https://dns.example.net/dns-query{?dns}"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DnsOverHttpsTemplates
  - 예제 값:
``` xml
<string>https://dns.example.net/dns-query{?dns}</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DownloadDirectory
  #### 다운로드 디렉터리 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  파일을 다운로드할 때 사용할 디렉터리를 구성합니다.

이 정책을 활성화하면 Microsoft Edge는 사용자가 디렉터리를 지정했는지 아니면 매번 다운로드 위치를 묻는 메시지가 표시되도록 선택했는지에 관계없이 제공된 디렉터리를 사용합니다. 사용할 수 있는 변수 목록은 [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041)을 참조하세요.

이 정책을 비활성화하거나 구성하지 않으면 기본 다운로드 디렉터리가 사용되며 사용자가 이를 변경할 수 있습니다.

잘못된 경로를 설정하면 Microsoft Edge에서 사용자의 기본 다운로드 디렉터리가 사용됩니다.

경로에 지정된 폴더가 존재하지 않는 경우, 다운로드할 때 사용자에게 다운로드를 저장할 위치를 묻는 메시지가 표시됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DownloadDirectory
  - GP 이름: 다운로드 디렉터리 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: DownloadDirectory
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"\n      Linux-based OSes (including Mac): /home/${user_name}/Downloads\n      Windows: C:\\Users\\${user_name}\\Downloads"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DownloadDirectory
  - 예제 값:
``` xml
<string>
      Linux-based OSes (including Mac): /home/${user_name}/Downloads
      Windows: C:\Users\${user_name}\Downloads</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### DownloadRestrictions
  #### 다운로드 제한 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용자가 보안 결정을 재정의하지 않고 Microsoft Edge에서 완전히 차단하는 다운로드 유형을 구성합니다.

Microsoft Defender SmartScreen 경고를 포함하는 다운로드를 제외한 모든 다운로드를 허용하도록 'BlockDangerousDownloads'를 설정합니다.

위험하거나 원하지 않는 다운로드에 대한 Microsoft Defender SmartScreen 경고를 포함하는 다운로드를 제외한 모든 다운로드를 허용하도록 'BlockPotentiallyDangerousDownloads'를 설정합니다.

모든 다운로드를 차단하려면 'BlockAllDownloads'를 설정합니다.

이 정책을 구성하지 않거나 'DefaultDownloadSecurity' 옵션을 설정하지 않으면 다운로드에 Microsoft Defender SmartScreen 분석 결과에 따라 일반적인 보안 제한이 적용됩니다.

이러한 제한은 '다운로드 링크...' 상황에 맞는 메뉴 옵션뿐만 아니라 웹 페이지 컨텐츠에서 다운로드하는 경우에도 적용됩니다. 이러한 제한사항은 현재 표시된 페이지를 저장하거나 다운로드할 때 적용되지 않으며 인쇄 옵션에서 PDF로 저장 옵션에도 적용되지 않습니다.

Microsoft Defender SmartScreen에 대한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2094934](https://go.microsoft.com/fwlink/?linkid=2094934)를 참조합니다.

정책 옵션 매핑:

* DefaultDownloadSecurity (0) = 특별한 제한 없음

* BlockDangerousDownloads (1) = 위험한 다운로드 차단

* BlockPotentiallyDangerousDownloads (2) = 잠재적으로 위험하거나 원치 않는 다운로드 차단

* BlockAllDownloads (3) = 모든 다운로드 차단

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: DownloadRestrictions
  - GP 이름: 다운로드 제한 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: DownloadRestrictions
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: DownloadRestrictions
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### EdgeCollectionsEnabled
  #### 컬렉션 기능 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 78 이상

  #### 설명
  사용자가 Office 통합으로 콘텐츠를 보다 효율적으로 수집하고 구성하고 공유하고 내보낼 수 있는 컬렉션 기능에 액세스하도록 허용할 수 있습니다.

이 정책을 사용하거나 구성하지 않으면 사용자가 Microsoft Edge에서 컬렉션 기능에 액세스하여 사용할 수 있습니다.

이 정책을 사용하지 않으면 사용자가 Microsoft Edge에서 컬렉션에 액세스하여 사용할 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: EdgeCollectionsEnabled
  - GP 이름: 컬렉션 기능 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: EdgeCollectionsEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: EdgeCollectionsEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### EditFavoritesEnabled
  #### 사용자가 즐겨찾기를 편집할 수 있도록 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  이 정책을 사용하도록 설정하면 사용자가 즐겨찾기를 추가, 제거 및 수정할 수 있습니다. 정책을 구성하지 않으면 이것이 기본 동작입니다.

이 정책을 사용하지 않도록 설정하면 사용자가 즐겨찾기를 추가, 제거 또는 수정할 수 없도록 중지합니다. 기존 즐겨찾기는 계속 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: EditFavoritesEnabled
  - GP 이름: 사용자가 즐겨찾기를 편집할 수 있도록 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: EditFavoritesEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: EditFavoritesEnabled
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### EnableDeprecatedWebPlatformFeatures
  #### 제한된 기간 동안 사용되지 않은 웹 플랫폼 기능 다시 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  일시적으로 다시 사용하도록 사용 중단된 기능을 일시적으로 다시 사용할 수 있게 웹 플랫폼 기능 목록을 지정합니다.

이 정책을 사용하면 제한된 기간 동안 사용 중단된 웹 플랫폼 기능을 다시 활성화할 수 있습니다.기능은 문자열 태그로 식별됩니다.

이 정책을 구성하지 않은 경우, 목록이 비어 있거나 또는 기능이 지원되는 문자열 태그 중 하나와 일치하지 않는 경우, 사용 중단된 웹 플랫폼 기능이 모두 사용 중지된 상태로 유지됩니다.

위의 플랫폼에서는 정책 자체가 지원되지만 모든 플랫폼에서 사용할 수는 없습니다. 사용 중단된 모든 웹 플랫폼 기능을 다시 사용할 수 있는 것은 아닙니다. 명시적으로 아래에 나열 된 기능만이, 기능에 따라 다른 제한된 시간동안 사용할 수 있습니다.https://bit.ly/blinkintents에서 웹 플랫폼 기능 변경의 의도를 검토 할 수 있습니다.

문자열 태그의 일반적인 형식은 [DeprecatedFeatureName]_EffectiveUntil[yyyymmdd]입니다.

정책 옵션 매핑:

* ExampleDeprecatedFeature (ExampleDeprecatedFeature_EffectiveUntil20080902) = 2008/09/02까지 ExampleDeprecatedFeature API 사용

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: EnableDeprecatedWebPlatformFeatures
  - GP 이름: 제한된 기간 동안 사용되지 않은 웹 플랫폼 기능 다시 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures\1 = "ExampleDeprecatedFeature_EffectiveUntil20080902"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: EnableDeprecatedWebPlatformFeatures
  - 예제 값:
``` xml
<array>
  <string>ExampleDeprecatedFeature_EffectiveUntil20080902</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### EnableDomainActionsDownload
  #### Microsoft에서 도메인 작업 다운로드 사용 (사용하지 않음)
  
  >사용되지 않음: 이 정책은 사용되지 않으며 Microsoft Edge 84 이후에는 작동되지 않습니다.
  #### 지원되는 버전:
  - Windows macOS 77 이후 84

  #### 설명
  충돌하는 상태를 방지해야 하므로 이 정책은 작동하지 않습니다. 이 정책은 도메인 작업 목록의 다운로드를 사용하거나 사용하지 않도록 설정하는 데 사용되었지만 항상 원하는 상태를 달성하지는 않았습니다. 다운로드를 처리하는 실험 및 구성 서비스에는 서비스에서 다운로드할 내용을 구성하는 데 필요한 고유한 정책이 있습니다. 대신 [ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol) 정책을 사용합니다.

 Microsoft Edge에서 도메인 작업은 브라우저가 웹에서 제대로 작동하는 데 도움이 되는 일련의 호환 기능을 나타냅니다.

 Microsoft는 일부 도메인에서 호환성 문제를 해결할 수 있는 조치 목록을 유지합니다. 예를 들어 해당 웹 사이트가 Microsoft Edge의 새 사용자 에이전트 문자열 때문에 깨지는 경우 브라우저가 웹 사이트의 사용자 에이전트 문자열을 재정의할 수 있습니다. 이러한 각 작업은 임시 이며, Microsoft에서는 사이트 소유자와 관련된 문제를 해결하려고 노력합니다.

브라우저가 처음 시작할 때에 그리고 나서 그 후에는 주기적으로 브라우저에서 수행할 호환성 작업의 최신 목록이 포함된 실험 및 구성 서비스에 문의합니다. 이 목록은 처음 검색된 후 로컬에 저장되기 때문에 이후의 요청은 서버 복사가 변경된 경우에만 목록을 업데이트 합니다.

 이 정책을 사용하면 도메인 작업 목록은 실험 및 구성 서비스에서 계속 다운로드됩니다.

 이 정책을 사용하지 않도록 설정하면 계속해 서 도메인 작업 목록이 실험 및 구성 서비스에서 다운로드 되지 않습니다.

 이 정책을 구성하지 않으면 실험 및 구성 서비스에서 도메인 작업 목록이 계속 다운로드됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: EnableDomainActionsDownload
  - GP 이름: Microsoft에서 도메인 작업 다운로드 사용 (사용하지 않음)
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: EnableDomainActionsDownload
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: EnableDomainActionsDownload
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### EnableOnlineRevocationChecks
  #### 온라인 OCSP/CRL 검사 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  온라인 해지 확인은 보안에 큰 이점을 제공하지 않으며 기본적으로 사용하지 않도록 설정되어 있습니다.

이 정책을 사용하면 Microsoft Edge가 소프트 오류, 온라인 OCSP/CRL 검사를 수행합니다. "소프트 오류"는 해지 서버에 연결할 수 없는 경우 인증서가 유효한 것으로 간주된다는 것을 의미합니다.

이 정책을 사용하지 않거나 구성하지 않으면 Microsoft Edge는 온라인 해지 검사를 수행하지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: EnableOnlineRevocationChecks
  - GP 이름: 온라인 OCSP/CRL 검사 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: EnableOnlineRevocationChecks
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: EnableOnlineRevocationChecks
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### EnableSha1ForLocalAnchors
  #### 로컬 신뢰 앵커로 발급될 때 SHA-1을 사용하여 서명된 인증서 허용 (사용되지 않음)
  >사용되지 않음: 이 정책은 더 이상 사용되지 않습니다. 현재 지원되고 있으나 향후 릴리스에서는 사용되지 않을 예정입니다.
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 85 이상

  #### 설명
  이 설정을 사용하면 인증서 체인이 로컬에 설치된 루트 인증서에 연결되고, 그 외 유효하지 않은 경우 Microsoft Edge는 SHA-1 서명된 인증서에 의해 보안된 연결을 허용합니다.

이 정책은 SHA-1 서명을 허용하는 운영 체제(OS) 인증서 확인 스택에 따라 달라집니다. OS 업데이트가 SHA-1 인증서의 OS 처리를 변경하면 이 정책은 더 이상 적용되지 않을 수 있습니다. 또한 이 정책은 기업이 SHA-1에서 벗어나는 데 더 많은 시간을 할애하기 위한 임시 해결책으로 사용됩니다. 이 정책은 2021년 중반에 발표되는 Microsoft Edge 92에서 제거됩니다.

이 정책을 설정하지 않거나, false로 설정하거나, SHA-1 인증서 체인을 공개적으로 신뢰할 수 있는 인증서 루트로 설정하지 않으면, Microsoft Edge는 SHA-1에 의해 서명된 인증서를 허용하지 않습니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: EnableSha1ForLocalAnchors
  - GP 이름: 로컬 신뢰 앵커로 발급될 때 SHA-1을 사용하여 서명된 인증서 허용 (사용되지 않음)
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: EnableSha1ForLocalAnchors
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: EnableSha1ForLocalAnchors
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### EnterpriseHardwarePlatformAPIEnabled
  #### 관리되는 확장에서 엔터프라이즈 하드웨어 플랫폼 API를 사용하도록 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 78 이상

  #### 설명
  이 정책을 사용하도록 설정하면 엔터프라이즈 정책에 의해 설치된 확장에서 엔터프라이즈 하드웨어 플랫폼 API를 사용할 수 있습니다.
이 정책을 사용하지 않도록 설정하거나 설정하지 않으면 확장이 엔터프라이즈 하드웨어 플랫폼 API를 사용할 수 없습니다.
이 정책은 구성 요소 확장에도 적용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: EnterpriseHardwarePlatformAPIEnabled
  - GP 이름: 관리되는 확장에서 엔터프라이즈 하드웨어 플랫폼 API를 사용하도록 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: EnterpriseHardwarePlatformAPIEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: EnterpriseHardwarePlatformAPIEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### EnterpriseModeSiteListManagerAllowed
  #### 엔터프라이즈 모드 사이트 목록 관리자 도구에 대한 액세스 허용
  
  
  #### 지원되는 버전:
  - Windows 86 이상부터

  #### 설명
  사용자가 엔터프라이즈 모드 사이트 목록 관리자를 사용할 수 있는지를 설정할 수 있습니다.

이 정책을 사용하도록 설정하면 사용자가 edge://compat 페이지에서 엔터프라이즈 모드 사이트 목록 관리자 도구의 탐색 단추를 볼 수 있습니다. 도구를 탐색하여 사용하세요.

이 정책을 사용하지 않거나 구성하지 않으하면 엔터프라이즈 모드 사이트 목록 관리자 탐색 단추를 볼 수 없고 사용할 수도 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: EnterpriseModeSiteListManagerAllowed
  - GP 이름: 엔터프라이즈 모드 사이트 목록 관리자 도구에 대한 액세스 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: EnterpriseModeSiteListManagerAllowed
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  #### 도메인에서 지정된 파일 형식에 대해 다운로드 파일 형식 확장명 기반의 경고를 사용 안 함
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 85 이상

  #### 설명
  이 정책을 사용하도록 설정하여 파일 형식 확장명 기반의 다운로드 경고에서 제외할 도메인의 해당 목록을 사용하여 파일 형식 확장명 사전을 만들 수 있습니다. 이렇게 하면 목록에 있는 도메인과 연결된 파일에 대한 파일 형식 확장명 기반 다운로드 경고를 차단할 수 있습니다. 예를 들어 "jnlp" 확장명이 "website1.com"와 연결되어 있는 경우, "website1.com"에서 "jnlp" 파일을 다운로드할 때 사용자에게 경고가 표시되지 않지만 "website2.com"에서 "jnlp" 파일을 다운로드할 때는 다운로드 경고가 표시됩니다.

이 정책으로 식별된 도메인에 대해 지정된 파일 형식 확장명이 있는 파일은 혼합된 콘텐츠 다운로드 경고 및 Microsoft Defender SmartScreen 경고와 같은 파일 형식 확장명 기반 외의 보안 경고는 여전히 적용을 받습니다.

이 정책을 사용하지 않도록 설정하거나 구성하지 않으면 확장 기반 다운로드 경고를 트리거하는 파일 형식이 사용자에게 경고를 표시합니다.

이 정책을 사용하도록 설정하려면 다음에 유의합니다.

*URL 패턴은 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)에 따라서 형식을 지정해야 합니다.
       * 파일 형식 확장명은 소문자 ASCII로 입력해야 합니다. 파일 형식 확장명을 나열할 때 선행 구분 기호를 포함하지 않아야 합니다. 따라서 ".jnlp" 대신 "jnlp" 목록을 사용해야 합니다.

예:

다음의 예시 값은 *.contoso.com 도메인에 대해 swf, exe 및 jnlp 확장명에 대해 파일 확장명 기반의 다운로드 경고를 차단합니다. exe 및 jnlp 파일에 대한 다른 도메인에 대한 파일 형식 확장명 기반 다운로드 경고는 표시하지만 swf 파일에 대해서는 표시하지 않습니다.

[
{ "file_extension": "jnlp", "domains": ["contoso.com"] },
{ "file_extension": "exe", "domains": ["contoso.com"] },
{ "file_extension": "swf", "domains": ["*"] }
  ]

앞의 예시는 모든 도메인에 대해 "swf" 파일에 대한 파일 형식 확장명 기반의 다운로드 경고의 차단을 보여주지만, 모든 도메인에 대해 모든 위험한 파일 형식 확장자에 이러한 경고의 차단은 보안 문제로 인해 적용하지 않는 것이 좋습니다. 이 예제는 단지 이러한 기능의 수행을 보여주기 위한 예제입니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - GP 이름: 도메인에서 지정된 파일 형식에 대해 다운로드 파일 형식 확장명 기반의 경고를 사용 안 함
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\1 = {"domains": ["https://contoso.com", "contoso2.com"], "file_extension": "jnlp"}
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\2 = {"domains": ["*"], "file_extension": "swf"}

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - 예제 값:
``` xml
<array>
  <string>{'domains': ['https://contoso.com', 'contoso2.com'], 'file_extension': 'jnlp'}</string>
  <string>{'domains': ['*'], 'file_extension': 'swf'}</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ExperimentationAndConfigurationServiceControl
  #### 실험 및 구성 서비스와의 통신 제어
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge에서 실험 및 구성 서비스는 실험 및 구성 페이로드 배포에 사용됩니다.

실험 페이로드에는 Microsoft에서 테스트 및 피드백을 위해 사용하도록 설정한 초기 개발 기능 목록이 포함되어 있습니다.

구성 페이로드는 사용자 환경을 최적화하기 위해 Microsoft에서 Microsoft Edge에 배포하려는 설정 목록으로 구성됩니다. 예를 들어 구성 페이로드는 Microsoft Edge이(가) 최신 페이로드를 검색하기 위해 실험 및 구성 서비스에 요청을 보내는 빈도를 지정할 수 있습니다.

  또한, 구성 페이로드에는 호환성을 위해 특정 도메인에 대해 수행할 작업 목록이 포함될 수도 있습니다. 예를 들어 의 새 사용자 에이전트 문자열로 인해 웹 사이트가 손상된 경우 브라우저가 웹 사이트의 사용자 에이전트 문자열을 재정의할 수 있습니다.Microsoft Edge    Microsoft가 사이트 소유자와 문제를 해결하는 동안 이러한 각 작업은 일시적입니다.

   이 정책을 'FullMode'로 설정하면 실험 및 구성 서비스에서 전체 페이로드가 다운로드됩니다. 여기에는 실험 및 구성 페이로드가 모두 포함됩니다.

   이 정책을 'ConfigurationsOnlyMode'로 설정하면 구성 페이로드만 전송됩니다.

   이 정책을 '제한 모드'로 설정하면 실험 및 구성 서비스와의 통신이 완전히 중지됩니다.

   이 정책을 구성하지 않으면 안정 및 베타 채널의 관리되는 디바이스에서 동작이 'ConfigurationsOnlyMode'와 동일합니다.

이 정책을 구성하지 않으면 관리되지 않는 디바이스에서 동작이 'FullMode'와 동일합니다.

정책 옵션 매핑:

* FullMode (2) = 구성 및 실험 검색

* ConfigurationsOnlyMode (1) = 구성만 검색

* RestrictedMode (0) = 실험 및 구성 서비스와의 통신을 사용하지 않도록 설정

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ExperimentationAndConfigurationServiceControl
  - GP 이름: 실험 및 구성 서비스와의 통신 제어
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ExperimentationAndConfigurationServiceControl
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ExperimentationAndConfigurationServiceControl
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ExternalProtocolDialogShowAlwaysOpenCheckbox
  #### 외부 프로토콜 대화 상자에 "항상 열기" 확인란을 표시합니다.
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 79 이상

  #### 설명
  이 정책은 "이 사이트에서 이 형식의 링크를 항상 열 수 있도록 허용" 확인란이 외부 프로토콜 시작 확인 프롬프트에 표시되는지 여부를 제어합니다.

이 정책을 사용하도록 설정하면 외부 프로토콜 확인 프롬프트가 표시될 때 사용자는 "항상 허용"을 선택하여 이 사이트의 프로토콜에 대한 이후의 모든 확인 메시지를 건너뛸 수 있습니다.

이 정책을 비활성화하면 "항상 허용" 확인란이 표시되지 않습니다. 외부 프로토콜이 호출될 때마다 확인 메시지가 사용자에게 표시됩니다.

Microsoft Edge 83 이전에 이 정책을 구성하지 않으면 "항상 허용" 확인란이 표시되지 않습니다. 외부 프로토콜이 호출될 때마다 사용자에게 확인 메시지가 표시됩니다.

Microsoft Edge 83에서 이 정책을 구성하지 않으면 확인란의 표시는 edge://flags에서 “프로토콜 시작 프롬프트 기본 설정 기억 사용” 플래그로 컨트롤됩니다.

Microsoft Edge 84를 기준으로 이 정책을 구성하지 않는면 외부 프로토콜 확인 프롬프트가 표시될 때 사용자는 “항상 허용”을 선택하여 해당 사이트의 프로토콜에 대한 이후의 모든 확인 메시지를 건너뛸 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - GP 이름: 외부 프로토콜 대화 상자에 "항상 열기" 확인란을 표시합니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### FamilySafetySettingsEnabled
  #### 사용자가 Family Safety를 구성할 수 있도록 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 83 이상

  #### 설명
  이 정책은 설정에서 Family Safety 페이지를 사용하지 않도록 설정하고 완전히 숨깁니다. edge://settings/familysafety로의 탐색도 차단됩니다. Family Safety 페이지에는 가족 그룹에서 사용할 수 있는 기능과 가족 그룹에 참가하는 방법이 설명되어 있습니다. 가족 보호에 대한 자세한 정보는 여기([https://go.microsoft.com/fwlink/?linkid=2098432](https://go.microsoft.com/fwlink/?linkid=2098432))를 참조하세요.

이 정책 설정을 사용하도록 설정하거나 구성하지 않으면 Family Safety 페이지가 표시됩니다.

이 정책을 사용하지 않으면 Family Safety 페이지가 표시되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: FamilySafetySettingsEnabled
  - GP 이름: 사용자가 Family Safety를 구성할 수 있도록 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: FamilySafetySettingsEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: FamilySafetySettingsEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### FavoritesBarEnabled
  #### 즐겨찾기 모음 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  즐겨찾기 모음을 사용하거나 사용하지 않도록 설정합니다.

이 정책을 사용하면 즐겨찾기 모음이 표시됩니다.

이 정책을 사용하지 않으면 즐겨찾기 모음이 표시되지 않습니다.

이 정책이 구성되어 있지 않으면 사용자가 즐겨찾기 모음을 사용할지 여부를 결정할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: FavoritesBarEnabled
  - GP 이름: 즐겨찾기 모음 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: FavoritesBarEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: FavoritesBarEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ForceBingSafeSearch
  #### Bing 유해 정보 차단 적용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Bing 웹 검색의 쿼리가 지정된 값으로 설정된 SafeSearch로 수행되는지 확인합니다. 사용자는 이 설정을 변경할 수 없습니다.

이 정책을 'BingSafeSearchNoRestrictions'로 구성하면 다음과 같습니다.Mode'의 SafeSearch in Bing 검색은 bing.com 값으로 돌아갑니다.

이 정책을 'BingSafeSearchModerateMode'로 구성하면 SafeSearch에서 중간 설정이 사용됩니다. 보통 설정은 성인 비디오 및 이미지를 필터링하지만 검색 결과의 텍스트는 필터링하지 않습니다.

이 정책을 'BingSafeSearchStrictMode'로 구성하는 경우 SafeSearch의 엄격한 설정이 사용됩니다. 엄격한 설정은 성인 텍스트, 이미지 및 비디오를 필터링합니다.

이 정책을 사용하지 않도록 설정하거나 구성하지 않으면 Bing 검색의 SafeSearch가 시행되지 않으며 사용자는 bing.com에서 원하는 값을 설정할 수 있습니다.

정책 옵션 매핑:

* BingSafeSearchNoRestrictionsMode (0) = Bing에서 검색 제한 구성 안 함

* BingSafeSearchModerateMode (1) = Bing에서 보통 검색 제한 구성

* BingSafeSearchStrictMode (2) = Bing에서 엄격한 검색 제한 구성

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ForceBingSafeSearch
  - GP 이름: Bing 유해 정보 차단 적용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ForceBingSafeSearch
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ForceBingSafeSearch
  - 예제 값:
``` xml
<integer>0</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ForceCertificatePromptsOnMultipleMatches
  #### "AutoSelectCertificateForUrls" 을 사용 하 여 구성 된 사이트에 대해 일치 하는 인증서가 여러 개 있는 경우 Microsoft Edge에서 인증서를 자동으로 선택 해야 하는지 여부를 구성 합니다
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 81 이상

  #### 설명
  사용 가능한 인증서가 여러 개 있고 사이트가 [AutoSelectCertificateForUrls](#autoselectcertificateforurls) 으로 구성 된 경우 사용자에 게 인증서를 선택 하 라는 메시지가 표시 되는지 여부를 전환 합니다. 사이트에 대 한 [AutoSelectCertificateForUrls](#autoselectcertificateforurls) 구성 하지 않으면 사용자에 게 인증서를 선택 하 라는 메시지가 항상 표시 됩니다.

이 정책을 True로 설정 하면 Microsoft Edge에서 사용자에 게 [AutoSelectCertificateForUrls](#autoselectcertificateforurls) 에 정의 된 사이트에 대 한 인증서를 선택 하 라는 메시지를 표시 합니다 .이 경우에는 두 개 이상의 인증서가 있는 경우에만 해당 됩니다.

이 정책을 False로 설정 하거나 구성 하지 않으면 인증서와 일치 하는 항목이 여러 개인 경우에도 Microsoft Edge에서 인증서를 자동으로 선택 합니다. [AutoSelectCertificateForUrls](#autoselectcertificateforurls) 에 정의 된 목록에서 사이트에 대 한 인증서를 선택 하 라는 메시지가 표시 되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ForceCertificatePromptsOnMultipleMatches
  - GP 이름: "AutoSelectCertificateForUrls" 을 사용 하 여 구성 된 사이트에 대해 일치 하는 인증서가 여러 개 있는 경우 Microsoft Edge에서 인증서를 자동으로 선택 해야 하는지 여부를 구성 합니다
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ForceCertificatePromptsOnMultipleMatches
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ForceCertificatePromptsOnMultipleMatches
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ForceEphemeralProfiles
  #### 임시 프로필 사용 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용자 프로필이 임시 모드로 전환되는지 여부를 제어합니다. 임시 프로필은 세션이 시작될 때 만들어지고 세션이 끝날 때 삭제되며 사용자의 원래 프로필과 연결됩니다.

이 정책을 사용하면 프로필이 임시 모드로 실행됩니다. 이를 통해 사용자는 검색 데이터를 해당 장치에 저장하지 않고도 자신의 장치에서 작업할 수 있습니다. Windows에서 GPO를 사용하여 OS 정책으로 이 정책을 사용하면 시스템의 모든 프로필에 이 정책이 적용됩니다.

이 정책을 사용하지 않거나 구성하지 않으면 사용자가 브라우저에 로그인할 때 일반 프로필을 가져옵니다.

임시 모드에서는 프로필 데이터가 사용자 세션 동안에만 디스크에 저장됩니다. 브라우저 기록, 확장 및 해당 데이터, 쿠키와 같은 웹 데이터, 웹 데이터베이스 등의 기능은 브라우저를 닫은 후에 저장되지 않습니다. 이 경우 사용자가 수동으로 디스크에 데이터를 다운로드하거나 페이지를 저장하거나 인쇄하는 것을 막지 않습니다. 사용자가 동기화를 사용하도록 설정하면 일반 프로필과 마찬가지로 모든 데이터가 동기화 계정에 보존됩니다. 명시적으로 사용하지 않도록 설정하지 않는 한 사용자는 임시 모드에서 InPrivate 브라우징을 사용할 수도 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ForceEphemeralProfiles
  - GP 이름: 임시 프로필 사용 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ForceEphemeralProfiles
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ForceEphemeralProfiles
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ForceGoogleSafeSearch
  #### Google 유해 정보 차단 적용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  유해 정보 차단이 활성으로 설정된 상태에서 수행되도록 Google 웹 검색의 쿼리를 강제로 적용하고 사용자가 이 설정을 변경하지 못하도록 합니다.

이 정책을 사용하면 Google 검색에서 유해 정보 차단이 항상 활성 상태입니다.

이 정책을 사용하지 않거나 구성하지 않으면 유해 정보 차단이 Google 검색에 적용되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ForceGoogleSafeSearch
  - GP 이름: Google 유해 정보 차단 적용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ForceGoogleSafeSearch
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ForceGoogleSafeSearch
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ForceLegacyDefaultReferrerPolicy
  #### 다운그레이드 시 참조 페이지 없음'의 기본 참조 페이지 정책을 사용합니다 (사용되지 않음)
  >사용되지 않음: 이 정책은 더 이상 사용되지 않습니다. 현재 지원되고 있으나 향후 릴리스에서는 사용되지 않을 예정입니다.
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 81 이상

  #### 설명
  이 정책은 현재 기본 참조 페이지 정책과 호환되지 않는 경우 웹 컨텐츠를 업데이트할 수 있는 시간을 기업에 제공하기 위한 단기적인 목적의 메커니즘일 뿐이므로 더 이상 사용되지 않습니다. 이 정책은 Microsoft Edge버전 86부터 작동하지 않습니다.

 Microsoft Edge의 기본 참조 페이지 정책은 현재 값(다운그레이드 시 참조 페이지 없음)에서 점진적 롤아웃을 통해 보다 안전한 정책(교차 원본의 경우 엄격한 출처)으로 강화되고 있습니다.

롤아웃 전에는 이 엔터프라이즈 정책이 적용되지 않습니다. 롤아웃 후 이 엔터프라이즈 정책이 사용하도록 설정되면 Microsoft Edge의 기본 참조 페이지 정책이 이전 값(다운그레이드 시 참조 페이지 없음)으로 설정됩니다.

이 엔터프라이즈 정책은 기본적으로 사용하지 않도록 설정됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ForceLegacyDefaultReferrerPolicy
  - GP 이름: 다운그레이드 시 참조 페이지 없음'의 기본 참조 페이지 정책을 사용합니다 (사용되지 않음)
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ForceLegacyDefaultReferrerPolicy
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ForceLegacyDefaultReferrerPolicy
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ForceNetworkInProcess
  #### 네트워킹 코드가 브라우저 프로세스에서 실행되도록 강제 (사용하지 않음)
  
  >사용되지 않음: 이 정책은 사용되지 않으며 Microsoft Edge 83 이후에는 작동되지 않습니다.
  #### 지원되는 버전:
  - Windows 78부터 83까지

  #### 설명
  해당 정책은 회사가 네트워킹 API 연결 여부에 의존하지 않는 타사 소프트웨어로 마이그레이션할 수 있도록 시간을 더 주기 위한 단기적 메커니즘이므로 효과가 없습니다. 프록시 서버는 LSP 및 Win32 API 패치 보다는 좋습니다.

해당 정책을 적용하면 네트워킹 코드가 브라우저 프로세스에서 실행됩니다.

해당 정책은 기본적으로 사용하지 않도록 설정됩니다. 해당 정책을 사용하도록 설정하면 사용자에게는 네트워킹 프로세스가 샌드박싱될 때 보안 문제가 발생합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ForceNetworkInProcess
  - GP 이름: 네트워킹 코드가 브라우저 프로세스에서 실행되도록 강제 (사용하지 않음)
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ForceNetworkInProcess
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ForceSync
  #### 브라우저 데이터를 강제로 동기화하고 동기화 동의 프롬프트를 표시하지 않음
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  Microsoft Edge에서 데이터 동기화를 강제합니다. 또한 이 정책은 사용자가 동기화를 끄는 것을 방지합니다.

이 정책을 구성하지 않으면 사용자가 동기화를 켜거나 끌 수 있습니다. 이 정책을 사용하면 사용자가 동기화를 사용 중지할 수 없습니다.

이 정책이 의도대로 작동하려면
[BrowserSignin](#browsersignin) 정책을 구성하지 않거나 사용하도록 설정해야합니다. [ForceSync](#forcesync)을(를) 사용 안함으로 설정하면 [BrowserSignin](#browsersignin)이 적용되지 않습니다.

[SyncDisabled](#syncdisabled)을 구성하지 않거나 False로 설정해야 합니다. True로 설정하면 [ForceSync](#forcesync)이(가) 적용되지 않습니다.

0 = 자동으로 동기화를 시작하지 않고 동기화 동의 표시 (기본값)
1 = Azure AD에 대해 강제로 동기화 설정/Azure AD-Degraded 사용자 프로필 및 동기화 동의 프롬프트를 표시하지 않음

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ForceSync
  - GP 이름: 브라우저 데이터를 강제로 동기화하고 동기화 동의 프롬프트를 표시하지 않음
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ForceSync
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ForceSync
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ForceYouTubeRestrict
  #### 최소 YouTube 제한 모드 강제 적용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  YouTube에서 최소 제한 모드를 적용하고 사용자가 덜 제한된 모드를 선택하지 못하도록 합니다.

YouTube에서 엄격한 제한 모드를 적용하려면 'Strict'(으)로 설정합니다.

 사용자가 YouTube에서 중간 제한 모드 및 엄격한 제한 모드만 사용하도록 하려면 'Moderate'(으)로 설정합니다. 제한 모드를 비활성화할 수 없습니다.

 YouTube에서 제한 모드를 적용하지 않도록 'Off’(으)로 설정하거나 이 정책을 구성하지 않습니다. YouTube 정책과 같은 외부 정책은 여전히 제한 모드를 적용할 수 있습니다.

정책 옵션 매핑:

* Off (0) = YouTube에서 제한 모드 적용 안 함

* Moderate (1) = YouTube에서 보통 제한 모드 이상만 적용

* Strict (2) = YouTube에서 엄격한 제한 모드 적용

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ForceYouTubeRestrict
  - GP 이름: 최소 YouTube 제한 모드 강제 적용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ForceYouTubeRestrict
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ForceYouTubeRestrict
  - 예제 값:
``` xml
<integer>0</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### FullscreenAllowed
  #### 전체 화면 모드 허용
  
  
  #### 지원되는 버전:
  - Windows 77 이상부터

  #### 설명
  전체 화면 모드의 사용 가능 여부를 설정합니다. 모든 Microsoft Edge UI가 숨겨지고 웹 콘텐츠만 표시됩니다.

이 정책을 사용하거나 구성하지 않으면 적절한 사용 권한이 있는 사용자, 앱 및 확장이 전체 화면 모드로 전환될 수 있습니다.

이 정책을 사용하지 않으면 사용자, 앱 및 확장이 전체 화면 모드로 전환될 수 없습니다.

전체 화면 모드를 사용하지 않으면 명령줄을 사용하여 키오스크 모드에서 Microsoft Edge를 열 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: FullscreenAllowed
  - GP 이름: 전체 화면 모드 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: FullscreenAllowed
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### GloballyScopeHTTPAuthCacheEnabled
  #### 전역 범위의 HTTP 인증 캐시 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 81 이상

  #### 설명
  이 정책은 HTTP 서버 인증 자격 증명을 사용하여 프로필당 단일 전역 캐시를 구성합니다.

이 정책을 사용하지 않거나 설정하지 않으면 브라우저는 교차 사이트 인증의 기본 동작을 사용하며(버전 80 부터) 최상위 사이트별로 HTTP 서버 인증 자격 증명의 범위를 지정합니다. 따라서 두 사이트에서 동일한 인증 도메인의 리소스를 사용하는 경우 두 사이트의 컨텍스트에서 자격 증명을 독립적으로 제공해야 합니다. 캐시된 프록시 자격 증명은 여러 사이트에서 다시 사용됩니다.

이 정책을 사용하면 한 사이트의 컨텍스트에 입력한 HTTP 인증 자격 증명이 다른 사이트의 컨텍스트에 자동으로 사용됩니다.

이 정책을 사용하도록 설정하면 사이트가 일부 유형의 교차 사이트 공격에 노출될 수 있으며, URL에 포함된 자격 증명을 사용한 HTTP 인증 캐시에 항목을 추가하여 쿠키 없이도 여러 사이트에서 사용자를 추적할 수 있습니다.

이 정책은 레거시 동작에 따라 엔터프라이즈에 로그인 절차를 업데이트할 수 있는 기회를 제공하기 위한 것이며 향후에 제거될 예정입니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: GloballyScopeHTTPAuthCacheEnabled
  - GP 이름: 전역 범위의 HTTP 인증 캐시 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: GloballyScopeHTTPAuthCacheEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: GloballyScopeHTTPAuthCacheEnabled
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### GoToIntranetSiteForSingleWordEntryInAddressBar
  #### 주소 표시줄에서 단일 단어 항목을 검색하는 대신 직접 인트라넷 사이트 탐색을 강제합니다.
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 78 이상

  #### 설명
  이 정책을 사용하면 주소 표시줄에 입력한 텍스트가 문장 부호가 없는 단일 단어인 경우 주소 표시줄 추천 단어 목록에서 최상위 자동 추천 결과는 인트라넷 사이트로 이동합니다.

문장 부호 없이 단일 단어를 입력하면 기본 탐색은 입력한 텍스트와 일치하는 인트라넷 사이트를 탐색합니다.

이 정책을 사용하면 이 텍스트가 문장 부호 없는 단일 단어인 경우 주소 표시줄 추천 단어 목록의 두 번째 자동 추천 결과는 입력한 텍스트 그대로 웹 검색을 수행합니다. 웹 검색을 금지하는 정책도 사용하지 않도록 설정하지 않는 한 기본 검색 공급자가 사용됩니다.

이 정책을 사용하면 다음과 같은 두 가지 효과가 있습니다.

기록 항목으로 해석되는 단일 단어 쿼리에 대한 응답으로 사이트 탐색이 더 이상 사이트를 탐색하지 않습니다. 대신, 브라우저는 조직의 인트라넷에 없을 수 있는 내부 사이트를 탐색합니다. 이로 인해 404 오류가 발생합니다.

인기 있는 단일 단어 검색어는 검색을 올바르게 수행하려면 검색 추천을 수동으로 선택해야 합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: GoToIntranetSiteForSingleWordEntryInAddressBar
  - GP 이름: 주소 표시줄에서 단일 단어 항목을 검색하는 대신 직접 인트라넷 사이트 탐색을 강제합니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: GoToIntranetSiteForSingleWordEntryInAddressBar
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: GoToIntranetSiteForSingleWordEntryInAddressBar
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### HSTSPolicyBypassList
  #### HSTS 정책 확인을 무시할 이름 목록 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 79 이상

  #### 설명
  이 목록에 지정된 호스트 이름은 요청을 "http://"에서 "https://"로 업그레이드할 수 있는 HSTS 정책 확인에서 제외됩니다. 이 정책에서는 단일 레이블 호스트 이름만 허용됩니다. 호스트 이름은 정규화되어야 합니다. 모든 IDN은 A 레이블 형식으로 변환되어야 하며 모든 ASCII 문자는 소문자여야 합니다. 이 정책은 지정된 특정 호스트 이름에만 적용됩니다. 목록에 있는 이름의 하위 도메인에는 적용되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: HSTSPolicyBypassList
  - GP 이름: HSTS 정책 확인을 무시할 이름 목록 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList\1 = "meet"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: HSTSPolicyBypassList
  - 예제 값:
``` xml
<array>
  <string>meet</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### HardwareAccelerationModeEnabled
  #### 가능한 경우 하드웨어 가속 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용 가능한 경우 하드웨어 가속을 사용하도록 지정합니다. 이 정책을 사용하거나 구성하지 않으면 GPU 기능이 명시적으로 차단되어 있지 않는 한 하드웨어 가속이 활성화됩니다.

이 정책을 사용하지 않으면 하드웨어 가속이 비활성화됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: HardwareAccelerationModeEnabled
  - GP 이름: 가능한 경우 하드웨어 가속 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: HardwareAccelerationModeEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: HardwareAccelerationModeEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### HideFirstRunExperience
  #### 첫 실행 경험 및 시작 화면 숨기기
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 80 이상

  #### 설명
  이 정책을 사용하면 Microsoft Edge를 처음 실행할 때 첫 실행 경험 및 시작 화면이 사용자에게 표시되지 않습니다.

첫 실행 경험에서 표시되는 구성 옵션의 경우 브라우저는 기본적으로 다음과 같이 설정됩니다.

-새 탭 페이지에서 피드 유형은 MSN 뉴스로 설정되고 레이아웃은 이미지형으로 설정됩니다.

-Windows 계정이 Azure AD 또는 MSA 유형인 경우에도 사용자는 여전히 Microsoft Edge에 자동으로 로그인됩니다.

-동기화는 기본적으로 사용하도록 설정되지 않으며 사용자가 동기화 설정에서 동기화를 활성화할 수 있습니다.

이 정책을 사용하지 않도록 설정하거나 구성하지 않으면 첫 실행 경험 및 시작 화면이 표시됩니다.

참고: 첫 실행 경험에서 사용자에게 표시되는 특정 구성 옵션은 다른 특정 정책을 사용하여 관리할 수도 있습니다. 이러한 정책과 함께 HideFirstRunExperience 정책을 사용하여 관리되는 장치에서 특정 브라우저 환경을 구성할 수 있습니다. 다른 정책 중 일부는 다음과 같습니다.

-[AutoImportAtFirstRun](#autoimportatfirstrun)

-[NewTabPageLocation](#newtabpagelocation)

-[NewTabPageSetFeedType](#newtabpagesetfeedtype)

-[SyncDisabled](#syncdisabled)

-[BrowserSignin](#browsersignin)

-[NonRemovableProfileEnabled](#nonremovableprofileenabled)

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: HideFirstRunExperience
  - GP 이름: 첫 실행 경험 및 시작 화면 숨기기
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: HideFirstRunExperience
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: HideFirstRunExperience
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ImportAutofillFormData
  #### 자동 채우기 양식 데이터 가져오기 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용자가 다른 브라우저에서 자동 채우기 양식 데이터를 Microsoft Edge로 가져올 수 있도록 허용합니다.

이 정책을 사용하면 자동 채우기 양식 데이터를 수동으로 가져오는 옵션이 자동으로 선택됩니다.

이 정책을 사용하지 않으면 처음 실행할 때 자동 채우기 양식 데이터를 가져오지 않으며, 사용자가 수동으로 가져올 수 없습니다.

이 정책을 구성하지 않으면 처음 실행할 때 자동 채우기 양식 데이터를 가져오고, 사용자는 나중에 검색 세션 중에 이 데이터를 수동으로 가져올지 여부를 선택할 수 있습니다.

이 정책을 권장 사항으로 설정할 수 있습니다. 즉, Microsoft Edge에서 처음 실행할 때 자동 채우기 양식 데이터를 가져오지만, 사용자가 수동 가져오기 중에 **자동 채우기 데이터** 옵션을 선택하거나 선택을 취소할 수 있습니다.

**참고**: 이 정책은 현재 Google Chrome (Windows 7, 8, 10, macOS의 경우), Mozilla Firefox(Windows 7, 8, 10, macOS의 경우) 브라우저에서 가져오기를 관리합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ImportAutofillFormData
  - GP 이름: 자동 채우기 양식 데이터 가져오기 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: ImportAutofillFormData
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ImportAutofillFormData
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ImportBrowserSettings
  #### 브라우저 설정 가져오기 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 78 이상

  #### 설명
  사용자가 다른 브라우저에서 Microsoft Edge에 대한 브라우저 설정을 가져올 수 있도록 허용합니다.

이 정책을 사용하면 **브라우저 데이터 가져오기** 대화 상자에서 **브라우저 설정** 확인란이 자동으로 선택됩니다.

이 정책을 사용하지 않으면 처음 실행 시 브라우저 설정을 가져오지 않으며 사용자가 수동으로 가져올 수 없습니다.

이 정책을 구성하지 않으면 처음 실행시 브라우저 설정을 가져오고 사용자는 나중에 검색 세션 동안 수동으로 가져올지 여부를 선택할 수 있습니다.

이 정책을 권장 사항으로 설정할 수도 있습니다. 즉, Microsoft Edge가 처음 실행될 때 설정을 가져오지만 용자는 수동 가져 오기 중에 ** 브라우저 설정 ** 옵션을 선택하거나 지울 수 있습니다.

**참고**:이 정책은 현재 Google Chrome(Windows 7, 8 및 10 및 macOS) 가져 오기를 관리합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ImportBrowserSettings
  - GP 이름: 브라우저 설정 가져오기 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: ImportBrowserSettings
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ImportBrowserSettings
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ImportCookies
  #### 쿠키 가져오기 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 81 이상

  #### 설명
  사용자가 다른 브라우저에서 Microsoft Edge에 대한 쿠키를 가져올 수 있도록 허용합니다.

이 정책을 사용하지 않으면 처음 실행 시 쿠키를 가져오지 않습니다.

이 정책을 구성하지 않으면 처음 실행 시 쿠키를 가져옵니다.

이 정책을 권장 사항으로 설정할 수도 있습니다. 즉, Microsoft Edge에서 처음 실행 시 쿠키를 가져옵니다.

**참고**: 이 정책은 현재 Google Chrome(Windows 7, 8 및 10 및 macOS) 가져오기를 관리합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ImportCookies
  - GP 이름: 쿠키 가져오기 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: ImportCookies
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ImportCookies
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ImportExtensions
  #### 확장 가져오기 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 81 이상

  #### 설명
  사용자가 다른 브라우저에서 확장을 Microsoft Edge로 가져올 수 있도록 허용합니다.

이 정책을 사용하면 **브라우저 데이터 가져 오기** 대화 상자에서 **확장** 확인란이 자동으로 선택됩니다.

이 정책을 사용하지 않으면 처음 실행 시 확장을 가져오지 않으며 사용자가 수동으로 가져올 수 없습니다.

이 정책을 구성하지 않으면 처음 실행 시 확장을 가져오고 사용자는 나중에 검색 세션 동안 수동으로 가져올지 여부를 선택할 수 있습니다.

이 정책을 권장 사항으로 설정할 수도 있습니다. 즉, Microsoft Edge가 처음 실행될 때 확장을 가져오지만 사용자는 수동 가져오기 중에 **확장** 옵션을 선택하거나 지울 수 있습니다.

**참고**: 이 정책은 현재 Google Chrome(Windows 7, 8 및 10 및 macOS)에서 가져오기만 지원합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ImportExtensions
  - GP 이름: 확장 가져오기 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: ImportExtensions
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ImportExtensions
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ImportFavorites
  #### 즐겨찾기 가져오기 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용자가 다른 브라우저에서 즐겨찾기를 Microsoft Edge로 가져올 수 있도록 허용합니다.

 이 정책을 사용하면 **브라우저 데이터 가져오기** 대화 상자에서 **즐겨찾기** 확인란이 자동으로 선택됩니다.

이 정책을 사용하지 않으면 처음 실행할 때 즐겨찾기를 가져오지 않으며, 사용자가 이 데이터를 수동으로 가져올 수 없습니다.

 이 정책을 구성하지 않으면 처음 실행할 때 즐겨찾기를 가져오고, 사용자는 나중에 검색 세션 중에 수동으로 가져올지 여부를 선택할 수 있습니다.

 이 정책을 권장 사항으로 설정할 수도 있습니다. 즉, Microsoft Edge에서 처음 실행할 때 즐겨찾기를 가져오지만, 사용자가 수동 가져오기 중에 **즐겨찾기** 옵션을 선택하거나 선택을 취소할 수 있습니다.

 **참고**: 이 정책은 현재 Internet Explorer(Windows 7, 8, 10의 경우), Google Chrome(Windows 7, 8, 10, macOS의 경우), Mozilla Firefox(Windows 7, 8, 10, macOS의 경우), Apple Safari(macOS의 경우) 브라우저에서 가져오기를 관리합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ImportFavorites
  - GP 이름: 즐겨찾기 가져오기 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: ImportFavorites
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ImportFavorites
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ImportHistory
  #### 검색 기록 가져오기 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용자가 다른 브라우저에서 검색 기록을 Microsoft Edge로 가져올 수 있도록 허용합니다.

이 정책을 사용하면 **브라우저 데이터 가져오기** 대화 상자에서 **검색 기록** 확인란이 자동으로 선택됩니다.

이 정책을 사용하지 않으면 처음 실행할 때 검색 기록 데이터를 가져오지 않으며, 사용자가 이 데이터를 수동으로 가져올 수 없습니다.

이 정책을 구성하지 않으면 처음 실행할 때 검색 기록 데이터를 가져오고, 사용자는 나중에 검색 세션 중에 수동으로 가져올지 여부를 선택할 수 있습니다.

이 정책을 권장 사항으로 설정할 수도 있습니다. 즉, Microsoft Edge에서 처음 실행할 때 검색 기록을 가져오지만, 사용자가 수동 가져오기 중에 **검색 기록** 옵션을 선택하거나 선택을 취소할 수 있습니다.

**참고**: 이 정책은 현재 Internet Explorer(Windows 7, 8, 10의 경우), Google Chrome(Windows 7, 8, 10, macOS의 경우), Mozilla Firefox(Windows 7, 8, 10, macOS의 경우), Apple Safari(macOS) 브라우저에서 가져오기를 관리합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ImportHistory
  - GP 이름: 검색 기록 가져오기 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: ImportHistory
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ImportHistory
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ImportHomepage
  #### 홈 페이지 설정 가져오기 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용자가 다른 브라우저에서 홈 페이지 설정을 Microsoft Edge로 가져올 수 있도록 허용합니다.

이 정책을 사용하면 홈 페이지 설정을 수동으로 가져오는 옵션이 자동으로 선택됩니다.

이 정책을 사용하지 않으면 처음 실행 시 홈 페이지 설정을 가져오지 않으며 사용자가 수동으로 가져올 수 없습니다.

이 정책을 구성하지 않으면 처음 실행 시 홈 페이지 설정을 가져오고 사용자는 나중에 검색 세션 동안 이 데이터를 수동으로 가져올지 여부를 선택할 수 있습니다.

이 정책을 권장 사항으로 설정할 수 있습니다. 즉, Microsoft Edge가 처음 실행 시 홈 페이지 설정을 가져오지만 사용자가 수동 가져오기 중에 **홈 페이지** 옵션을 선택하거나 선택을 취소할 수 있습니다.

**참고**: 이 정책은 현재 Internet Explorer(Windows 7, 8 및 10의 경우)에서 가져오기를 관리합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ImportHomepage
  - GP 이름: 홈 페이지 설정 가져오기 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ImportHomepage
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ImportHomepage
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ImportOpenTabs
  #### 열린 탭 가져오기 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 79 이상

  #### 설명
  사용자가 다른 브라우저에서 열려 있고 고정된 탭을 Microsoft Edge로 가져올 수 있도록 허용합니다.

이 정책을 사용하면 **브라우저 데이터 가져 오기** 대화 상자에서 **열립 탭** 확인란이 자동으로 선택됩니다.

이 정책을 사용하지 않으면 처음 실행 시 브라우저 설정을 가져오지 않으며 사용자가 수동으로 가져올 수 없습니다.

이 정책을 구성하지 않으면 처음 실행 시 열린 탭을 가져오고 사용자는 나중에 검색 세션 동안 수동으로 가져올지 여부를 선택할 수 있습니다.

이 정책을 권장 사항으로 설정할 수도 있습니다. 즉, Microsoft Edge가 처음 실행될 때 열린 탭을 가져오지만 사용자는 수동 가져오기 중에 **열린 탭** 옵션을 선택하거나 지울 수 있습니다.

**참고**: 이 정책은 현재 Google Chrome(Windows 7, 8 및 10 및 macOS)에서 가져오기만 지원합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ImportOpenTabs
  - GP 이름: 열린 탭 가져오기 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: ImportOpenTabs
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ImportOpenTabs
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ImportPaymentInfo
  #### 결제 정보 가져오기 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용자가 다른 브라우저에서 결제 정보를 Microsoft Edge로 가져올 수 있도록 허용합니다.

이 정책을 사용하면 **브라우저 데이터 가져오기** 대화 상자에서 **결제 정보** 확인란이 자동으로 선택됩니다.

이 정책을 사용하지 않으면 처음 실행 시 결제 정보를 가져오지 않으며 사용자가 수동으로 가져올 수 없습니다.

이 정책을 구성하지 않으면 처음 실행 시 결제 정보를 가져오고 사용자는 나중에 검색 세션 동안 수동으로 가져올지 여부를 선택할 수 있습니다.

이 정책을 권장 사항으로 설정할 수도 있습니다. 즉, Microsoft Edge가 처음 실행 시 결제 정보를 가져오지만 사용자가 수동 가져오기 중에 **결제 정보** 옵션을 선택하거나 선택을 취소할 수 있습니다.

**참고**: 이 정책은 현재 Google Chrome(Windows 7, 8 및 10, macOS)에서 가져오기를 관리합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ImportPaymentInfo
  - GP 이름: 결제 정보 가져오기 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: ImportPaymentInfo
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ImportPaymentInfo
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ImportSavedPasswords
  #### 저장된 암호 가져오기 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용자가 다른 브라우저에서 저장된 암호를 Microsoft Edge로 가져올 수 있도록 허용합니다.

이 정책을 사용하면 저장된 암호를 수동으로 가져오는 옵션이 자동으로 선택됩니다.

이 정책을 사용하지 않으면 저장된 암호를 처음 실행할 때 가져오지 않으며, 사용자가 수동으로 가져올 수 없습니다.

이 정책을 구성하지 않으면 처음 실행할 때 암호를 가져오고, 사용자는 나중에 검색 세션 중에 수동으로 가져올지 여부를 선택할 수 있습니다.

이 정책을 권장 사항으로 설정할 수 있습니다. 즉, Microsoft Edge에서 처음 실행할 때 암호를 가져오지만, 사용자가 수동 가져오기 중에 **암호** 옵션을 선택하거나 선택을 취소할 수 있습니다.

**참고**: 이 정책은 현재 Internet Explorer(Windows 7, 8, 10의 경우), Google Chrome(Windows 7, 8, 10, macOS의 경우), Mozilla Firefox(Windows 7, 8, 10, macOS의 경우) 브라우저에서 가져오기를 관리합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ImportSavedPasswords
  - GP 이름: 저장된 암호 가져오기 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: ImportSavedPasswords
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ImportSavedPasswords
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ImportSearchEngine
  #### 검색 엔진 설정 가져오기 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용자가 다른 브라우저에서 검색 엔진 설정을 Microsoft Edge로 가져올 수 있도록 허용합니다.

이 정책을 사용하면 검색 엔진 설정을 가져오는 옵션이 자동으로 선택됩니다.

이 정책을 사용하지 않으면 처음 실행 시 검색 엔진 설정을 가져오지 않으며 사용자가 수동으로 가져올 수 없습니다.

이 정책을 구성하지 않으면 처음 실행 시 검색 엔진 설정을 가져오고 사용자는 나중에 검색 세션 동안 이 데이터를 수동으로 가져올지 여부를 선택할 수 있습니다.

이 정책을 권장 사항으로 설정할 수 있습니다. 즉, Microsoft Edge가 처음 실행 시 검색 엔진 설정을 가져오지만 사용자가 수동 가져오기 중에 **검색 엔진** 옵션을 선택하거나 선택을 취소할 수 있습니다.

**참고**: 이 정책은 현재 Internet Explorer(Windows 7, 8 및 10의 경우)에서 가져오기를 관리합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ImportSearchEngine
  - GP 이름: 검색 엔진 설정 가져오기 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: ImportSearchEngine
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ImportSearchEngine
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ImportShortcuts
  #### 바로 가기 가져오기 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 81 이상

  #### 설명
  사용자가 다른 브라우저에서 바로가기를 Microsoft Edge로 가져올 수 있도록 허용합니다.

이 정책을 사용하지 않으면 처음 실행 시 바로가기를 가져오지 않습니다.

이 정책을 구성하지 않으면 처음 실행 시 바로가기를 가져옵니다.

이 정책을 권장 사항으로 설정할 수도 있습니다. 즉, Microsoft Edge에서 처음 실행 시 바로가기를 가져옵니다.

**참고**: 이 정책은 현재 Google Chrome(Windows 7, 8 및 10 및 macOS)에서 가져오기를 관리합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ImportShortcuts
  - GP 이름: 바로 가기 가져오기 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: ImportShortcuts
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ImportShortcuts
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### InPrivateModeAvailability
  #### InPrivate 모드 가용성 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용자가 Microsoft Edge에서 InPrivate 모드에서 페이지를 열 수 있는지 여부를 지정합니다.

이 정책을 구성하지 않거나 'Enabled'으(로) 설정하면 사용자가 InPrivate 모드에서 페이지를 열 수 있습니다.

사용자가 InPrivate 모드를 사용하지 않도록 하려면 이 정책을 'Disabled'(으)로 설정합니다.

항상 InPrivate 모드를 사용하려면 이 정책을 'Forced'(으)로 설정합니다.

정책 옵션 매핑:

* Enabled (0) = InPrivate 모드 사용할 수 있음

* Disabled (1) = InPrivate 모드 사용할 수 없음

* Forced (2) = InPrivate 모드 강제 적용

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: InPrivateModeAvailability
  - GP 이름: InPrivate 모드 가용성 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: InPrivateModeAvailability
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: InPrivateModeAvailability
  - 예제 값:
``` xml
<integer>1</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### InsecureFormsWarningsEnabled
  #### 안전하지 않은 양식에 대한 경고 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  이 정책은 브라우저의 보안 (HTTPS) 사이트에 포함된 안전하지 않은 양식 (HTTP를 통해 제출된 양식)의 처리를 제어합니다.
이 정책을 사용하거나 설정하지 않으면 안전하지 않은 양식이 제출된 경우 전체 페이지 경고가 표시됩니다. 또한 양식 필드에 초점이 맞춰지면 경고 풍선이 양식 필드 옆에 표시되고 해당 양식에 대해 자동 완성이 비활성화됩니다.
이 정책을 비활성화하면 안전하지 않은 양식에 대한 경고가 표시되지 않고 자동 완성이 정상적으로 작동합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: InsecureFormsWarningsEnabled
  - GP 이름: 안전하지 않은 양식에 대한 경고 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: InsecureFormsWarningsEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: InsecureFormsWarningsEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### IntensiveWakeUpThrottlingEnabled
  #### IntensiveWakeUpThrottling 기능 제어
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 85 이상

  #### 설명
  IntensiveWakeUpThrottling 기능을 사용하면 백그라운드 탭에서 Javascript 타이머가 적극적으로 제한 및 결합되어 페이지가 5분 이상 백그라운드된 후 분 당 한 번만 실행됩니다.

이 기능은 웹 표준을 준수하는 기능이지만 일부 웹 사이트에서 특정 작업을 최대 1분 이상 지연되게 하여 기능 이상을 일으키게 할 수 있습니다. 그러나 이 기능을 사용하면 CPU 및 배터리 절감 효과가 큽니다. 자세한 내용은 https://bit.ly/30b1XR4를 참조하세요.

이 정책을 사용하면 기능이 강제로 활성화되어 사용자가 해당 설정을 재정의할 수 없게 됩니다.
이 정책을 사용하지 않으면 기능이 강제로 해제되고 사용자가 해당 설정을 재정의할 수 없게 됩니다.
이 정책을 구성하지 않으면 기능은 자체 내부 논리에 의해 제어됩니다. 사용자는 해당 설정을 수동으로 구성할 수 있습니다.

정책은 렌더러 프로세스별로 적용되며 렌더러 프로세스 시작 시 가장 최근의 정책 설정 값이 적용된다는 사실에 유의하세요. 로드된 모든 탭이 일관된 정책 설정을 받도록 하려면 전체적으로 다시 시작해야 합니다. 이 정책의 다른 값으로 실행 시 프로세스가 손상되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: IntensiveWakeUpThrottlingEnabled
  - GP 이름: IntensiveWakeUpThrottling 기능 제어
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: IntensiveWakeUpThrottlingEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: IntensiveWakeUpThrottlingEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### InternetExplorerIntegrationEnhancedHangDetection
  #### Internet Explorer 모드에 대한 향상된 정지 감지 구성
  
  
  #### 지원되는 버전:
  - Windows 84 이상부터

  #### 설명
  향상된 행 탐지는 독립 실행형 Internet Explorer(인터넷 익스플로러)에서 사용하는 것보다 Internet Explorer(인터넷 익스플로러) 모드에서 행 웹 페이지를 보다 세부적으로 탐지하는 방법입니다. 중단된 웹 페이지가 탐지되면 브라우저가 나머지 브라우저가 중단되지 않도록 경감 기능을 적용합니다.

     이 설정을 사용하면 웹 사이트와 호환되지 않는 문제가 발생할 경우 향상된 행 탐지를 사용하도록 구성할 수 있습니다. Internet Explorer 모드에서는 "(웹사이트가 응답하지 않음)" 등의 알림이 표시되지만 독립 실행형 Internet Explorer에서는 표시되지 않는 경우에만 이 정책을 사용하지 않도록 설정하는 것이 좋습니다.

     이 설정은 다음 항목과 함께 작동합니다.
    [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)은(는) 목록에 하나 이상의 항목이 있는 'IEMode'
및
[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) 정책으로 설정됩니다.

     이 정책을 'Enabled'로 설정하거나 구성하지 않으면 Internet Explorer 모드에서 실행 중인 웹 사이트에서 향상된 행 탐지를 사용합니다.

     이 정책을 'Disabled'(으)로 설정하면 향상된 행 탐지가 사용되지 않도록 설정되고 사용자에게 기본 Internet Explorer 행 탐지 동작이 표시됩니다.

Internet Explorer 모드에 대한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)을 참조하시기 바랍니다.

정책 옵션 매핑:

* Disabled (0) = 향상된 정지 감지 비활성화

* Enabled (1) = 향상된 정지 감지 사용

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: InternetExplorerIntegrationEnhancedHangDetection
  - GP 이름: Internet Explorer 모드에 대한 향상된 정지 감지 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: InternetExplorerIntegrationEnhancedHangDetection
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### InternetExplorerIntegrationLevel
  #### Internet Explorer 통합 구성
  
  
  #### 지원되는 버전:
  - Windows 77 이상부터

  #### 설명
  Internet Explorer 모드를 위한 최적의 환경을 구성하는 방법에 대한 지침은 [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)를 참조하세요.

정책 옵션 매핑:

* None (0) = 없음

* IEMode (1) = Internet Explorer 모드

* NeedIE (2) = Internet Explorer 11

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: InternetExplorerIntegrationLevel
  - GP 이름: Internet Explorer 통합 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: InternetExplorerIntegrationLevel
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### InternetExplorerIntegrationSiteList
  #### 엔터프라이즈 모드 사이트 목록 구성
  
  
  #### 지원되는 버전:
  - Windows 78 이상부터

  #### 설명
  Internet Explorer 모드를 위한 최적의 환경을 구성하는 방법에 대한 지침은 [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: InternetExplorerIntegrationSiteList
  - GP 이름: 엔터프라이즈 모드 사이트 목록 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: InternetExplorerIntegrationSiteList
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"https://internal.contoso.com/sitelist.xml"
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### InternetExplorerIntegrationSiteRedirect
  #### Internet Explorer 모드 페이지에서 시작할 때 구성되지 않은 사이트에 대한 "페이지 내" 탐색 작동 방식 지정
  
  
  #### 지원되는 버전:
  - Windows 81 이상부터

  #### 설명
  현재 페이지의 링크, 스크립트 또는 양식에서 "페이지 내" 탐색이 시작됩니다. 또한 이전 "페이지 내" 탐색 시도의 서버 측 리디렉션일 수도 있습니다. 반대로 사용자는 브라우저 컨트롤을 사용하여 현재 페이지와 독립적으로 "페이지 내" 탐색을 시작할 수 있습니다. 예를 들어, 주소 표시줄, 뒤로 단추 또는 즐겨찾기 링크를 사용합니다.

     이 설정을 사용하면 Internet Explorer 모드에서 로드된 페이지에서 구성되지 않은 사이트(엔터프라이즈 모드 사이트 목록에 구성되지 않음)로 이동할 때 Microsoft Edge로 다시 전환할지 아니면 Internet Explorer 모드로 유지할지 지정할 수 있습니다.

     이 설정은 다음 항목과 함께 작동합니다.
     [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)은(는) 목록에 하나 이상의 항목이 있는 'IEMode'
     및
     [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) 정책으로 설정됩니다.

이 정책을 사용하지 않도록 설정하거나 구성하지 않으면 Internet Explorer(인터넷 익스플로러) 모드에서 열도록 구성된 사이트만 해당 모드로 열립니다. Internet Explorer 모드에서 열도록 구성되지 않은 사이트는 Microsoft Edge로 다시 리디렉션됩니다.

     이 정책을 'Default'(으)로 설정하면 Internet Explorer 모드에서 열도록 구성된 사이트만 해당 모드로 열립니다. Internet Explorer 모드에서 열도록 구성되지 않은 사이트는 Microsoft Edge로 다시 리디렉션됩니다.

이 정책을 '자동 탐색'으로 설정하면 됩니다.구성되지 않은 사이트로의 모든 자동 탐색(예: 302 리디렉션)이 Internet Explorer(인터넷 익스플로러) 모드로 유지된다는 점을 제외하고는 기본 환경이 제공됩니다.

     이 정책을 'AllInPageNavigations'로 설정하면 IE 모드로 로드된 페이지에서 구성되지 않은 사이트로의 모든 탐색이 Internet Explorer 모드(최소 권장 사항)로 유지됩니다.

Internet Explorer 모드에 대한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2105106](https://go.microsoft.com/fwlink/?linkid=2105106)을 참조하시기 바랍니다.

정책 옵션 매핑:

* Default (0) = 기본값

* AutomaticNavigationsOnly (1) = Internet Explorer 모드에서 자동 탐색만 유지

* AllInPageNavigations (2) = Internet Explorer 모드에서 모든 페이지 내 탐색 유지

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: InternetExplorerIntegrationSiteRedirect
  - GP 이름: Internet Explorer 모드 페이지에서 시작할 때 구성되지 않은 사이트에 대한 "페이지 내" 탐색 작동 방식 지정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: InternetExplorerIntegrationSiteRedirect
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### InternetExplorerIntegrationTestingAllowed
  #### Internet Explorer 모드 테스트 허용
  
  
  #### 지원되는 버전:
  - Windows 86 이상부터

  #### 설명
  이 정책은 ie-mode-test 플래그 정책을 대체합니다. 사용자가 UI 메뉴 옵션에서 IE 모드 탭을 열 수 있습니다.

      이 설정은 다음과 함께 작동합니다.
      [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)이(가) 'IEMode'로 설정
       및
       [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) 정책 목록에 항목이 하나 이상 있습니다.

      이 정책을 사용하면 사용자가 UI 옵션에서 IE 모드 탭을 열고 현재 사이트를 IE 모드 사이트로 이동할 수 있습니다.

사용 중지하면 이 정책을 사용하면 사용자가 메뉴에서 UI 옵션을 직접 볼 수 없습니다.

      이 정책을 구성하지 않으면 ie-mode-test 플래그를 수동으로 설정할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: InternetExplorerIntegrationTestingAllowed
  - GP 이름: Internet Explorer 모드 테스트 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: InternetExplorerIntegrationTestingAllowed
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### IsolateOrigins
  #### 특정 원본에 대해 사이트 격리 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  자신의 프로세스에서 단독으로 실행되도록 원본을 지정합니다.
 또한 이 정책은 하위 도메인에서 명명 한 원본을 분리합니다. 예를 들어 https://contoso.com/를 지정하면 https://foo.contoso.com/이 https://contoso.com/ 사이트의 일부로 격리됩니다.
 정책이 활성화된 경우 쉼표로 구분된 목록의 각 명명된 출처는 자체 프로세스에서 실행됩니다.
 이 정책을 사용하지 않으면 'IsolateOrigins' 및 'SitePerProcess' 기능이 모두 비활성화됩니다. 사용자는 명령줄 플래그를 통해 'IsolateOrigins' 정책을 수동으로 활성화할 수 있습니다.
정책을 구성하지 않은 경우 사용자가 이 설정을 변경할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: IsolateOrigins
  - GP 이름: 특정 원본에 대해 사이트 격리 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: IsolateOrigins
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"https://contoso.com/,https://fabrikam.com/"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: IsolateOrigins
  - 예제 값:
``` xml
<string>https://contoso.com/,https://fabrikam.com/</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### LocalProvidersEnabled
  #### 현지 공급자의 제안 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 83 이상

  #### 설명
  장치 추천 항목 공급자(로컬 공급자)의 추천 항목이 Microsoft Edge의 주소 표시줄 및 자동 추전 목록에 표시되게 허용합니다(예: 즐겨찾기 및 검색 기록).

이 정책을 사용하도록 설정할 경우 로컬 공급자의 추천 항목이 사용됩니다.

이 정책을 사용하지 않도록 설정할 경우 로컬 공급자의 추천 항목이 사용되지 않습니다. 로컬 기록 및 로컬 즐겨찾기 추천 항목이 표시되지 않습니다.

이 정책을 구성하지 않을 경우 로컬 공급자의 추천 항목이 허용되지만 사용자가 설정 토글을 사용하여 이를 변경할 수 있습니다.

이 기능을 사용하지 않도록 하는 정책이 적용될 경우 일부 기능을 사용하지 못할 수 있습니다. 예를 들어 [SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled) 정책을 사용하도록 설정하면 검색 기록 추천 항목을 사용할 수 없게 됩니다.

이 정책을 사용하려면 브라우저를 다시 시작하여 적용을 마쳐야 합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: LocalProvidersEnabled
  - GP 이름: 현지 공급자의 제안 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: LocalProvidersEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: LocalProvidersEnabled
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ManagedFavorites
  #### 즐겨찾기 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  관리되는 즐겨 찾기 목록을 구성합니다.

정책은 즐겨찾기 목록을 만듭니다. 각 즐겨찾기에는 즐겨찾기의 이름과 대상을 포함하는 "이름" 및 "URL" 키가 있습니다. "URL" 키는 없으나 위에 정의된 즐겨찾기 목록을 포함하는 추가 "자식" 키는 있는 즐겨찾기를 정의하여 하위 폴더를 구성할 수 있습니다(일부는 폴더일 수 있음). Microsoft Edge는 주소 표시줄을 통해 제출된 것처럼 불완전한 URL을 수정합니다. 예를 들어 "microsoft.com"은 "https://microsoft.com/"로 바뀝니다.

이러한 즐겨찾기는 사용자가 수정할 수 없는 폴더에 저장됩니다. 그러나 사용자가 즐겨찾기 모음에서 숨길 수 있습니다. 기본적으로 폴더 이름은 "관리되는 즐겨찾기"이지만 "toplevel_name" 키가 포함된 사전을 즐겨찾기 목록에 추가하여 원하는 폴더 이름을 값으로 변경할 수 있습니다.

관리되는 즐겨찾기는 사용자 계정에 동기화되지 않으며 확장에 의해 수정될 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 사전

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ManagedFavorites
  - GP 이름: 즐겨찾기 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ManagedFavorites
  - 값 형식: REG_SZ
  ##### 예제 값:
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


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ManagedFavorites
  - 예제 값:
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
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ManagedSearchEngines
  #### 검색 엔진 관리
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  최대 10개의 검색 엔진 목록을 구성할 수 있으며, 목록 중 하나는 기본 검색 엔진으로 표시되어야 합니다.
   인코딩을 지정할 필요가 없습니다. Microsoft Edge 80부터 suggest_url 및 image_search_url 매개 변수는 선택적입니다. 선택적 매개 변수인 image_search_post_params(쉼표로 구분된 이름/값 쌍으로 구성됨)는 Microsoft Edge 80부터 사용할 수 있습니다.

Microsoft Edge 83부터 allow_search_engine_discovery 선택적 매개 변수를 사용하여 검색 엔진 검색을 사용하도록 설정할 수 있습니다. 이 매개 변수는 목록에서 첫 번째 항목이어야 합니다. allow_search_engine_discovery를 지정하지 않으면, 검색 엔진 검색은 기본적으로 사용하지 않도록 설정됩니다. Microsoft Edge 84부터 이 정책을 검색 공급자 검색을 허용하는 권장 정책으로 설정할 수 있습니다. allow_search_engine_discovery 선택적 매개 변수를 추가할 필요가 없습니다.

   이 정책을 사용하면 사용자가 목록에서 검색 엔진을 추가, 제거 또는 변경할 수 없습니다. 사용자는 기본 검색 엔진을 목록에 있는 검색 엔진으로 설정할 수 있습니다.

   이 정책을 사용하지 않거나 구성하지 않으면 사용자가 원하는 대로 검색 엔진 목록을 수정할 수 있습니다.

  [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 정책이 설정된 경우 이 정책(ManagedSearchEngines)은 무시됩니다. 이 정책 적용을 마무리하려면 사용자가 브라우저를 다시 시작해야 합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 사전

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ManagedSearchEngines
  - GP 이름: 검색 엔진 관리
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: ManagedSearchEngines
  - 값 형식: REG_SZ
  ##### 예제 값:
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


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ManagedSearchEngines
  - 예제 값:
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
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### MaxConnectionsPerProxy
  #### 프록시 서버에 대 한 동시 연결의 최대 수
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  프록시 서버에 대한 최대 동시 연결 수를 지정합니다.

일부 프록시 서버는 클라이언트 당 많은 수의 동시 연결을 처리할 수 없으므로 이 정책을 더 낮은 값으로 설정하여 해당 문제를 해결할 수 있습니다.

이 정책의 값은 100보다 작고 6보다 커야 합니다. 기본값은 32입니다.

일부 웹 앱은 GET을 사용하여 많은 연결을 사용하는 것으로 알려져 있습니다. 최대 연결을 32개 아래로 낮추거나 이러한 종류의 웹 응용 프로그램이 너무 많이 열려 있으면 브라우저 네트워킹이 중단될 수 있습니다.

이 정책을 구성하지 않으면 기본값 (32)이 사용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: MaxConnectionsPerProxy
  - GP 이름: 프록시 서버에 대 한 동시 연결의 최대 수
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: MaxConnectionsPerProxy
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000020
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: MaxConnectionsPerProxy
  - 예제 값:
``` xml
<integer>32</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### MediaRouterCastAllowAllIPs
  #### Google Cast가 모든 IP 주소의 캐스트 장치에 연결하도록 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  이 정책을 사용하면 Google Cast가 RFC1918/RFC4193 개인 주소 뿐만 아니라 모든 IP 주소의 캐스트 장치에 연결할 수 있습니다.

RFC1918/RFC4193 개인 주소의 캐스트 장치에 대한 Google Cast를 제한하려면 이 정책을 사용하지 않도록 설정하세요.

이 정책을 구성하지 않으면 CastAllowAllIPs 기능을 사용하지 않는 한, RFC1918/RFC4193 개인 주소의 캐스트 장치에만 Google Cast를 연결합니다.

[EnableMediaRouter](#enablemediarouter) 정책을 사용하지 않도록 설정하면 이 정책은 적용되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: MediaRouterCastAllowAllIPs
  - GP 이름: Google Cast가 모든 IP 주소의 캐스트 장치에 연결하도록 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: MediaRouterCastAllowAllIPs
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: MediaRouterCastAllowAllIPs
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### MetricsReportingEnabled
  #### 사용 현황 및 크래시 관련 데이터 보고 사용 (사용되지 않음)
  >사용되지 않음: 이 정책은 더 이상 사용되지 않습니다. 현재 지원되고 있으나 향후 릴리스에서는 사용되지 않을 예정입니다.
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  이 정책은 더 이상 사용되지 않습니다. 현재 지원되고 있지만 Microsoft Edge 89에서 더 이상 사용되지 않습니다. 이 정책은 Windows 7, Windows 8, MacOS에 대한 새 정책 [DiagnosticData](#diagnosticdata)로 대체됩니다. 이 정책은 Win 10([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569))에 대한 원격 분석 허용으로 대체됩니다.

이 정책을 사용하면 Microsoft Edge에 대한 사용 현황 및 충돌 관련 데이터를 Microsoft에 보고할 수 있습니다.

이 정책을 사용하도록 설정하여 사용 현황 및 충돌 관련 데이터를 Microsoft에 전송할 수 있습니다. Microsoft에 데이터를 전송하지 않으려면 이 정책을 사용하지 않도록 설정합니다. 두 경우 모두 사용자가 설정을 변경하거나 재정의할 수 없습니다.

Windows 10에서 이 정책을 구성하지 않으면 Microsoft Edge는 기본적으로 Windows 진단 데이터 설정으로 설정됩니다. 이 정책을 사용하면 Microsoft Edge에서 Windows 진단 데이터 설정이 고급 또는 전체로 설정된 경우에만 사용 현황 데이터를 전송합니다. 이 정책을 사용하지 않도록 설정하면 Microsoft Edge에서는 사용 현황 데이터를 보내지 않습니다. 충돌 관련 데이터는 Windows 진단 데이터 설정에 따라 전송됩니다. Windows 진단 데이터 설정에 관한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)를 참조하세요.

Windows 7, Windows 8, MacOS에서 이 정책은 사용 현황 및 충돌 관련 데이터의 전송을 제어합니다. 이 정책을 구성하지 않으면 Microsoft Edge는 사용자 기본 설정으로 기본 설정됩니다.

이 정책을 사용하려면 [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)를 사용하는 것으로 설정해야 합니다. [MetricsReportingEnabled](#metricsreportingenabled)나 [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)가 구성되지 않거나 사용하도록 설정되지 않은 경우 이 데이터는 Microsoft에 전송되지 않습니다.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스 또는 MDM을 통해 관리되거나 MCX를 통해 도메인에 가입된 macOS 인스턴스에서만 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: MetricsReportingEnabled
  - GP 이름: 사용 현황 및 크래시 관련 데이터 보고 사용 (사용되지 않음)
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: MetricsReportingEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: MetricsReportingEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### NativeWindowOcclusionEnabled
  #### 기본 창 Occlusion 사용
  
  
  #### 지원되는 버전:
  - Windows 84 이상부터

  #### 설명
  Microsoft Edge에서 기본 창 폐쇄를 사용하도록 설정합니다.

이 설정을 사용 하면 Microsoft Edge CPU 및 전원 소비량을 줄일 수 있습니다. 는 창이 다른 창에 포함 될 때이를 감지 하 고 작업 칠하기 픽셀을 일시 중단 합니다.

이 설정을 사용 하지 않으면 Microsoft Edge에서 창이 다른 창에 적용 되는 경우이를 감지 하지 않습니다.

이 정책을 설정 하지 않으면 창 숨기기 검색이 사용 됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: NativeWindowOcclusionEnabled
  - GP 이름: 기본 창 Occlusion 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: NativeWindowOcclusionEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### NavigationDelayForInitialSiteListDownloadTimeout
  #### 엔터프라이즈 모드 사이트 목록에 대한 탭 탐색 지연 시간 설정
  
  
  #### 지원되는 버전:
  - Windows 84 이상부터

  #### 설명
  브라우저가 초기 기업 모드 사이트 목록을 다운로드할 때까지 탐색 대기 중인 Microsoft Edge 탭에 대한 시간 초과(초)를 설정할 수 있습니다.

      이 설정은 다음과 함께 작동합니다.
      [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)은(는) 'IEMode'
(으)로 설정되고,
      [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)(목록에는 하나 이상의 항목이 있고),

     [DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)은(는) "적격 가능한 모든 탐색"(1)으로 설정됩니다.

      탭은 Enterprise Mode 사이트 목록이 다운로드될 때까지 이 시간 초과보다 오래 기다리지 않습니다. 시간 초과가 만료될 때 브라우저가 Enterprise Mode 사이트 목록 다운로드를 완료하지 않은 경우 Microsoft Edge 탭이 계속 탐색됩니다. 시간 초과 값은 20초 이상 1초 이상이어야 합니다.

이 정책의 시간 초과 값을 기본값인 2초보다 큰 값으로 설정하면 2초 후에 사용자에게 알림 표시줄이 표시됩니다. 정보 표시줄에는 기업 모드 사이트 목록 다운로드가 완료될 때까지 기다리면서 사용자가 종료할 수 있는 단추가 있습니다.

이 정책을 구성하지 않으면 기본 시간 제한(2초)이 사용됩니다. 이 기본값은 나중에 변경될 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: NavigationDelayForInitialSiteListDownloadTimeout
  - GP 이름: 엔터프라이즈 모드 사이트 목록에 대한 탭 탐색 지연 시간 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: NavigationDelayForInitialSiteListDownloadTimeout
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x0000000a
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### NetworkPredictionOptions
  #### 네트워크 예측 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  네트워크 예측을 사용하도록 설정하고 사용자가 이 설정을 변경할 수 없게 합니다.

이 기능은 DNS 프리페치, TCP 및 SSL 사전 연결 및 웹 페이지 사전 렌더링을 제어합니다.

이 정책을 구성하지 않으면 네트워크 예측은 사용하도록 설정되지만 사용자가 변경할 수 있습니다.

정책 옵션 매핑:

* NetworkPredictionAlways (0) = 모든 네트워크 연결에서 네트워크 작업 예측

* NetworkPredictionWifiOnly (1) = 지원되지 않음. 이 값을 사용하는 경우 '모든 네트워크 연결에서 네트워크 작업 예측' (0)이 설정된 것처럼 처리됩니다.

* NetworkPredictionNever (2) = 모든 네트워크 연결에서 네트워크 작업 예측 안 함

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: NetworkPredictionOptions
  - GP 이름: 네트워크 예측 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: NetworkPredictionOptions
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: NetworkPredictionOptions
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### NonRemovableProfileEnabled
  #### 사용자가 회사 또는 학교 계정으로 자동으로 로그인한 기본 프로필을 항상 가지고 있는지 여부를 구성합니다.
  
  
  #### 지원되는 버전:
  - Windows 78 이상부터

  #### 설명
  이 정책은 사용자가 사용자의 회사 또는 학교 계정으로 자동으로 로그인되어 있는 Microsoft Edge 프로필을 제거할 수 있는지 여부를 결정합니다.

이 정책을 사용하면 Windows에서 사용자의 회사 또는 학교 계정으로 제거할 수 없는 프로필이 만들어집니다.

이 정책을 사용하지 않거나 구성하지 않으면 사용자가 Windows에서 사용자의 회사 또는 학교 계정으로 자동으로 로그인한 프로필을 로그아웃하거나 제거할 수 있습니다.

브라우저 로그인을 구성하려면 [BrowserSignin](#browsersignin) 정책을 사용하세요.

이 정책은 Microsoft Active Directory 도메인에 가입된 Windows 인스턴스, 장치 관리에 등록된 Windows 10 Pro나 Enterprise 인스턴스에서만 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: NonRemovableProfileEnabled
  - GP 이름: 사용자가 회사 또는 학교 계정으로 자동으로 로그인한 기본 프로필을 항상 가지고 있는지 여부를 구성합니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: NonRemovableProfileEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### OverrideSecurityRestrictionsOnInsecureOrigin
  #### 안전하지 않은 원본에 대한 보안 제한이 적용되는 위치 제어
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  보안되지 않은 출처에 대한 보안 제한이 적용되지 않는 원본 (URL) 또는 호스트 이름 패턴 (예: "* .contoso.com") 목록을 지정합니다.

이 정책을 사용하면 TLS를 배포할 수 없는 레거시 응용 프로그램의 허용된 원본을 지정하거나 개발자가 준비 서버에서 TLS를 배포하지 않고도 보안 컨텍스트가 필요한 기능을 테스트할 수 있도록 내부 웹 개발을 위한 준비 서버를 설정할 수 있습니다.레거시 응용 프로그램에 대 한 원본을 사용할 수 있습니다. 이 정책은 또한 출처가 검색 주소창에서 "안전하지 않음"으로 표시되는 것을 방지합니다.

이 정책에서 URL 목록을 설정하면 명령줄 플래그 '--unsafely-treat-insecure-origin-as-secure'를 동일한 URL의 쉼표로 구분 된 목록으로 설정하는 것과 같은 효과가 있습니다. 이 정책을 사용하면 명령줄 플래그가 재정의됩니다.

보안 컨텍스트에 대한 자세한 내용은 https://www.w3.org/TR/secure-contexts/를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: OverrideSecurityRestrictionsOnInsecureOrigin
  - GP 이름: 안전하지 않은 원본에 대한 보안 제한이 적용되는 위치 제어
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\1 = "http://testserver.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\2 = "*.contoso.com"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: OverrideSecurityRestrictionsOnInsecureOrigin
  - 예제 값:
``` xml
<array>
  <string>http://testserver.contoso.com/</string>
  <string>*.contoso.com</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PaymentMethodQueryEnabled
  #### 웹 사이트에서 사용 가능한 결제 방법을 쿼리할 수 있도록 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 80 이상

  #### 설명
  사용자가 결제 수단을 저장했는지 웹 사이트에서 확인할 수 있는지의 여부를 설정할 수 있습니다.

이 정책을 사용하지 않도록 설정하면 PaymentRequest.canMakePayment 또는 PaymentRequest.hasEnrolledInstrument API를 사용하는 웹 사이트에 결제 수단을 사용할 수 없다는 알림이 표시됩니다.

이 정책을 사용하거나 설정하지 않으면 웹 사이트에서 사용자에게 결제 방법이 저장되었는지 여부를 확인할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PaymentMethodQueryEnabled
  - GP 이름: 웹 사이트에서 사용 가능한 결제 방법을 쿼리할 수 있도록 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: PaymentMethodQueryEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PaymentMethodQueryEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PersonalizationReportingEnabled
  #### 검색 기록을 Microsoft에 보내 광고, 검색 및 뉴스의 개인 설정 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 80 이상

  #### 설명
  이 정책은 Microsoft가 사용자의 Microsoft Edge 검색 기록을 수집하여 광고, 검색, 뉴스 및 기타 Microsoft 서비스를 개인 설정하는 데 사용하지 못하게 합니다.

이 설정은 Microsoft 계정을 가진 사용자만 사용할 수 있습니다. 자녀 계정 또는 엔터프라이즈 계정에는 이 설정을 사용할 수 없습니다.

이 정책을 비활성화하면 사용자가 설정을 변경하거나 재정의할 수 없습니다. 이 정책이 활성화되거나 구성되지 않으면 Microsoft Edge에서 사용자의 기본 설정이 사용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PersonalizationReportingEnabled
  - GP 이름: 검색 기록을 Microsoft에 보내 광고, 검색 및 뉴스의 개인 설정 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: PersonalizationReportingEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PersonalizationReportingEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PinningWizardAllowed
  #### 작업 표시줄에 고정 마법사 허용
  
  
  #### 지원되는 버전:
  - Windows 80 이상부터

  #### 설명
  Microsoft Edge는 작업 표시줄에 고정 마법사를 사용하여 사용자가 제안된 사이트를 작업 표시줄에 고정할 수 있도록 합니다. 작업 표시줄에 고정 마법사 기능은 기본적으로 활성화되어 있으며, 설정 및 기타 메뉴를 통해 사용자가 액세스할 수 있습니다.

이 정책을 구성하지 않거나 활성화하면 사용자가 설정 및 기타 메뉴에서 작업 표시줄에 고정 마법사를 호출 할 수 있습니다. 프로토콜 실행을 통해 마법사를 호출할 수도 있습니다.

이 정책을 비활성화하면 작업 표시줄에 고정 마법사가 메뉴에서 비활성화되고 프로토콜 실행을 통해 호출할 수 없습니다.

작업 표시줄에 고정 마법사를 활성화 또는 비활성화하기 위한 사용자 설정을 사용할 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PinningWizardAllowed
  - GP 이름: 작업 표시줄에 고정 마법사 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: PinningWizardAllowed
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ProactiveAuthEnabled
  #### 사전 인증 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사전 인증을 사용할지 여부를 구성할 수 있습니다.

이 정책을 사용하면 Microsoft Edge는 Microsoft 서비스로 로그인한 사용자를 사전에 인증하려고 시도합니다. 정기적으로 Microsoft Edge는 온라인 서비스에서 이 작업을 수행하는 방법을 제어하는 구성을 포함하는 업데이트된 매니페스트에 대해 확인합니다.

이 정책을 사용하지 않으면 Microsoft Edge는 Microsoft 서비스로 로그인한 사용자를 사전에 인증하려고 시도하지 않습니다. Microsoft Edge는 더 이상 온라인 서비스에서 이 작업을 수행하기 위한 구성을 포함하는 업데이트된 매니페스트에 대해 확인하지 않습니다.

이 정책을 구성하지 않으면 사전 인증이 켜집니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ProactiveAuthEnabled
  - GP 이름: 사전 인증 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ProactiveAuthEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ProactiveAuthEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PromotionalTabsEnabled
  #### 전체 탭 프로모션 콘텐츠 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  전체 탭 프로모션 또는 교육 콘텐츠의 프레젠테이션을 제어합니다. 이 설정은 사용자가 Microsoft Edge에 로그인하거나 기본 브라우저를 선택하거나 제품 기능에 대한 정보를 알아보는 데 도움이 되는 시작 페이지의 프레젠테이션을 제어합니다.

이 정책을 사용(true로 설정)하거나 구성하지 않으면 Microsoft Edge가 사용자에게 전체 탭 콘텐츠를 표시하여 제품 정보를 제공할 수 있습니다.

이 정책을 사용하지 않으면(false로 설정) Microsoft Edge가 사용자에게 전체 탭 콘텐츠를 표시할 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PromotionalTabsEnabled
  - GP 이름: 전체 탭 프로모션 콘텐츠 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: PromotionalTabsEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PromotionalTabsEnabled
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### PromptForDownloadLocation
  #### 다운로드한 파일을 저장할 위치 묻기
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  다운로드하기 전에 파일을 저장할 위치를 묻는 메시지를 표시할지의 여부를 설정합니다.

이 정책을 사용하면 다운로드하기 전에 각 파일을 저장할 위치를 묻는 메시지가 표시됩니다. 구성하지 않은 경우 사용자에게 묻지 않고 파일이 자동으로 기본 위치에 저장됩니다.

이 정책을 구성하지 않으면 사용자가 이 설정을 변경할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: PromptForDownloadLocation
  - GP 이름: 다운로드한 파일을 저장할 위치 묻기
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: PromptForDownloadLocation
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: PromptForDownloadLocation
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### QuicAllowed
  #### QUIC 프로토콜 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge에서 QUIC 프로토콜의 사용을 허용합니다.

이 정책을 사용하거나 구성하지 않으면 QUIC 프로토콜이 허용됩니다.

이 정책을 사용하지 않으면 QUIC 프로토콜이 차단됩니다.

QUIC는 현재 TCP를 사용하는 웹 응용 프로그램의 성능을 향상시킬 수 있는 전송 계층 네트워크 프로토콜입니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: QuicAllowed
  - GP 이름: QUIC 프로토콜 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: QuicAllowed
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: QuicAllowed
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### RelaunchNotification
  #### 보류 중인 업데이트에 대해 브라우저 다시 시작이 권장되거나 필요함을 사용자에게 알림
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  보류 중인 업데이트를 적용하려면 Microsoft Edge을(를) 다시 시작해야 함을 사용자에게 알립니다.

이 정책을 구성하지 않으면 Microsoft Edge이(가) 위쪽 메뉴 모음의 오른쪽 끝에 휴지통 아이콘을 추가하여 업데이트를 적용하기 위해 브라우저를 다시 시작할지 사용자에게 묻습니다.

이 정책을 실행하고 'Recommended'(으)로 설정한 경우 사용자에게 다시 시작하는 것이 좋다는 메시지가 반복적으로 표시됩니다. 사용자는 이 경고를 무시하고 다시 시작을 연기할 수 있습니다.

정책을 'Required'로 설정하면 알림 기간이 경과하는 즉시 브라우저가 자동으로 재시작된다는 메시지가 반복적으로 표시됩니다. 기본 기간은 7일입니다. [RelaunchNotificationPeriod](#relaunchnotificationperiod) 정책을 사용하여 이 기간을 구성할 수 있습니다.

브라우저가 다시 시작될 때 사용자의 세션이 복원됩니다.

정책 옵션 매핑:

* Recommended (1) = 권장 - 사용자에게 다시 시작이 권장됨을 나타내는 메시지를 반복적으로 표시

* Required (2) = 필요 - 사용자에게 다시 시작이 필요함을 나타내는 메시지를 반복적으로 표시

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: RelaunchNotification
  - GP 이름: 보류 중인 업데이트에 대해 브라우저 다시 시작이 권장되거나 필요함을 사용자에게 알림
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: RelaunchNotification
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: RelaunchNotification
  - 예제 값:
``` xml
<integer>1</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### RelaunchNotificationPeriod
  #### 업데이트 알림 기간 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  보류 중인 업데이트를 적용하기 위해 Microsoft Edge를 다시 시작해야 한다는 것을 사용자에게 알리는 기간(밀리초)을 설정할 수 있습니다.

이 기간에는 업데이트가 필요하다는 것을 사용자에게 반복적으로 알립니다. Microsoft Edge에서 알림 기간의 1/3이 지나면 다시 시작이 필요함을 표시하도록 앱 메뉴가 변경됩니다. 알림 기간의 2/3가 지나면 알림 색을 변경하고, 전체 알림 기간이 지나면 다시 색을 변경합니다. [RelaunchNotification](#relaunchnotification) 정책에서 사용하는 추가 알림은 이와 동일한 일정을 따릅니다.

설정되지 않은 경우 기본 기간 604800000밀리초(1주)가 사용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: RelaunchNotificationPeriod
  - GP 이름: 업데이트 알림 기간 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: RelaunchNotificationPeriod
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x240c8400
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: RelaunchNotificationPeriod
  - 예제 값:
``` xml
<integer>604800000</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### RendererCodeIntegrityEnabled
  #### 렌더러 코드 무결성 사용
  
  
  #### 지원되는 버전:
  - Windows 78 이상부터

  #### 설명
  이 정책을 사용하거나 설정하지 않으면 렌더러 코드 무결성이 사용됩니다. 이 정책은 Microsoft Edge내에서 실행해야 하는 타사 소프트웨어에서 호환성 문제가 발생한 경우에만 사용하지 않도록 설정해야 합니다.

이 정책을 사용하지 않도록 설정하면 Microsoft Edge내에서 알 수 없는 잠재적으로 악의적인 코드가 로드될 수 있기 때문에 Microsoft Edge의 보안 및 안정성에 해로운 영향을 미칩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: RendererCodeIntegrityEnabled
  - GP 이름: 렌더러 코드 무결성 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: RendererCodeIntegrityEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### RequireOnlineRevocationChecksForLocalAnchors
  #### 온라인 OCSP/CRL 검사가 로컬 트러스트 앵커에 필요한지 여부를 지정합니다.
  
  
  #### 지원되는 버전:
  - Windows 77 이상부터

  #### 설명
  온라인 해지 확인(OCSP/CRL 확인)이 필요한지 여부를 제어합니다. Microsoft Edge에서 해지 상태 정보를 가져올 수 없는 경우 이러한 인증서는 해지된 것으로 처리됩니다("하드 오류").

이 정책을 사용하면 Microsoft Edge는 성공적으로 유효성을 검사하고 로컬로 설치된 CA 인증서에 의해 서명된 서버 인증서에 대한 해지 확인을 항상 수행합니다.

이 정책을 구성하거나 사용하지 않으면 Microsoft Edge는 기존 온라인 해지 확인 설정을 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: RequireOnlineRevocationChecksForLocalAnchors
  - GP 이름: 온라인 OCSP/CRL 검사가 로컬 트러스트 앵커에 필요한지 여부를 지정합니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: RequireOnlineRevocationChecksForLocalAnchors
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ResolveNavigationErrorsUseWebService
  #### 웹 서비스를 사용하여 탐색 오류 해결 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  호텔 및 공항 Wi-Fi와 같은 경우에 Microsoft Edge가 웹 서비스에 대한 데이터 없는 연결을 발급하여 연결을 위해 네트워크를 검색하도록 허용합니다.

이 정책을 사용하면 네트워크 연결 테스트에 웹 서비스가 사용됩니다.

이 정책을 사용하지 않으면 Microsoft Edge는 기본 API를 사용하여 네트워크 연결 및 탐색 문제를 해결하려고 시도합니다.

**참고**: Windows 8 및 이후 버전의 Windows를 제외하고 Microsoft Edge는 *항상* 연결 문제를 해결하기 위해 기본 API를 사용합니다.

이 정책을 구성하지 않으면 Microsoft Edge는 edge://settings/privacy의 서비스에 설정된 사용자 기본 설정을 사용합니다.
특히, 사용자가 켜거나 끌 수 있는 **웹 서비스를 사용하여 탐색 오류 해결** 토글이 있습니다. 이 정책(ResolveNavigationErrorsUseWebService)을 사용하도록 설정한 경우 **웹 서비스를 사용하여 탐색 오류 해결** 설정이 켜지고 사용자는 토글을 사용하여 설정을 변경할 수 없습니다. 이 정책을 사용하지 않으면 **웹 서비스를 사용하여 탐색 오류 해결** 설정이 꺼지고 사용자는 토글을 사용하여 설정을 변경할 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ResolveNavigationErrorsUseWebService
  - GP 이름: 웹 서비스를 사용하여 탐색 오류 해결 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: ResolveNavigationErrorsUseWebService
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ResolveNavigationErrorsUseWebService
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### RestrictSigninToPattern
  #### Microsoft Edge 기본 계정으로 사용할 수 있는 계정 제한
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge에서 브라우저 기본 계정으로 설정할 수 있는 계정(동기화 옵트인 흐름 중에 선택한 계정)을 결정합니다.

사용자가 이 패턴과 일치하지 않는 사용자 이름으로 브라우저 기본 계정을 구성하려고 하면 차단되고 적절한 오류 메시지가 표시됩니다. 패턴에 대한 Perl 스타일 정규식을 사용하여 여러 계정을 일치시키도록 이 정책을 구성할 수 있습니다. 패턴 일치는 대소문자를 구분합니다. 사용되는 정규식 규칙에 대한 자세한 내용은 https://go.microsoft.com/fwlink/p/?linkid=2133903.

이 정책을 구성하지 않거나 비워 두면 사용자는 Microsoft Edge에서 아무 계정이나 브라우저 기본 계정으로 설정할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: RestrictSigninToPattern
  - GP 이름: Microsoft Edge 기본 계정으로 사용할 수 있는 계정 제한
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: RestrictSigninToPattern
  - 값 형식: REG_SZ
  ##### 예제 값:
```
".*@contoso.com"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: RestrictSigninToPattern
  - 예제 값:
``` xml
<string>.*@contoso.com</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### RoamingProfileLocation
  #### 로밍 프로필 디렉토리 설정
  
  
  #### 지원되는 버전:
  - Windows 85 이상부터

  #### 설명
  프로필의 로밍 복사본을 저장하는 데 사용할 디렉터리를 구성합니다.

이 정책을 사용하면 [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) 정책도 사용하도록 설정한 경우에 한해 Microsoft Edge이(가) 제공된 디렉터리를 사용하여 프로필의 로밍 복사본을 저장합니다. [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) 정책을 사용하지 않거나 구성하지 않으면 이 정책에 저장된 값이 사용되지 않습니다.

사용할 수 있는 변수 목록은 [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041)을 참조하세요.

이 정책을 구성하지 않으면 기본 로밍 프로필 경로가 사용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: RoamingProfileLocation
  - GP 이름: 로밍 프로필 디렉토리 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: RoamingProfileLocation
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"${roaming_app_data}\\edge-profile"
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### RoamingProfileSupportEnabled
  #### Microsoft Edge 프로필 데이터에 대한 로밍 복사본 사용 설정
  
  
  #### 지원되는 버전:
  - Windows 85 이상부터

  #### 설명
  이 정책을 사용하도록 설정하여 Windows에서 로밍 프로필을 사용합니다. Microsoft Edge 프로필(즐겨찾기 및 기본 설정)에 저장된 설정은 로밍 사용자 프로필 폴더에 저장된 파일(또는 [RoamingProfileLocation](#roamingprofilelocation) 정책을 통해 관리자가 지정한 위치)에도 저장됩니다.

이 정책을 사용하지 않거나 구성하지 않으면 일반 로컬 프로필만 사용됩니다.

[SyncDisabled](#syncdisabled) 정책은 모든 데이터 동기화를 사용하지 않도록 설정하고 정책을 무시합니다.

로밍 사용자 프로필 사용에 대한 자세한 내용은 https://docs.microsoft.com/windows-server/storage/folder-redirection/deploy-roaming-user-profiles를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: RoamingProfileSupportEnabled
  - GP 이름: Microsoft Edge 프로필 데이터에 대한 로밍 복사본 사용 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: RoamingProfileSupportEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### RunAllFlashInAllowMode
  #### Adobe Flash 콘텐츠 설정을 모든 콘텐츠로 확장
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  이 정책을 사용하면 사용자 또는 엔터프라이즈 정책에 의해 콘텐츠 설정에서 Adobe Flash 콘텐츠 허용하도록 설정된 웹 사이트에 포함된 모든 Adobe Flash 콘텐츠가 실행됩니다. 여기에는 다른 원본의 콘텐츠 및/또는 작은 콘텐츠가 포함됩니다.

Adobe Flash를 실행하도록 허용할 웹 사이트를 제어하려면 [DefaultPluginsSetting](#defaultpluginssetting), [PluginsAllowedForUrls](#pluginsallowedforurls) 및 [PluginsBlockedForUrls](#pluginsblockedforurls) 정책에서 사양을 참조하세요.

이 정책을 사용하지 않거나 구성하지 않으면 다른 원본(바로 위에서 언급한 세 가지 정책에서 지정되지 않은 사이트)의 Adobe Flash 콘텐츠 또는 작 콘텐츠가 차단될 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: RunAllFlashInAllowMode
  - GP 이름: Adobe Flash 콘텐츠 설정을 모든 콘텐츠로 확장
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: RunAllFlashInAllowMode
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: RunAllFlashInAllowMode
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SSLErrorOverrideAllowed
  #### HTTPS 경고 페이지에서 사용자가 작업을 계속할 수 있도록 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge는 사용자가 SSL 오류가 있는 사이트를 방문할 때 경고 페이지를 표시합니다.

이 정책을 사용하거나 구성하지 않으면(기본값) 사용자가 이 경고 페이지에서 클릭하여 앞으로 나아갈 수 있습니다.

이 정책을 사용하지 않으면 사용자가 클릭하여 앞으로 나아가는 것이 모든 경고 페이지에서 차단됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SSLErrorOverrideAllowed
  - GP 이름: HTTPS 경고 페이지에서 사용자가 작업을 계속할 수 있도록 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: SSLErrorOverrideAllowed
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SSLErrorOverrideAllowed
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SSLVersionMin
  #### 최소 TLS 버전 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  지원되는 최소 버전의 SSL을 설정합니다. 이 정책을 구성하지 않으면 Microsoft Edge에서 기본 최소 버전인 TLS 1.0.

을 사용합니다.      이 정책을 실행하면 최소 버전을 'TLSv1', 'TLSv1.1' 또는 'TLSv1.2' 중 하나로 설정할 수 있습니다. 설정된 경우 Microsoft Edge은(는) 지정된 버전보다 낮은 버전의 SSL/TLS를 사용하지 않습니다. 인식할 수 없는 값은 무시됩니다.

정책 옵션 매핑:

* TLSv1 (tls1) = TLS 1.0

* TLSv1.1 (tls1.1) = TLS 1.1

* TLSv1.2 (tls1.2) = TLS 1.2

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SSLVersionMin
  - GP 이름: 최소 TLS 버전 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: SSLVersionMin
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"tls1"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SSLVersionMin
  - 예제 값:
``` xml
<string>tls1</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SaveCookiesOnExit
  #### Microsoft Edge 종료 시 쿠키를 저장합니다.
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  이 정책을 사용하면 브라우저를 닫을 때 지정된 쿠키 집합이 삭제되지 않습니다. 이 정책은
의 경우에만 적용됩니다.      - '쿠키 및 기타 사이트 데이터' 토글이 설정/개인 정보 보호 및 서비스/종료 시 검색 데이터 삭제로 구성되거나 또는
.      - 정책 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit)을(를) 사용하도록 설정하거나
.      - 정책 [DefaultCookiesSetting](#defaultcookiessetting)이(가) '세션 기간 동안 쿠키 유지'로 설정됩니다.

모든 세션에서 쿠키가 보존되는 URL 패턴을 기반으로 사이트 목록을 정의할 수 있습니다.

참고: 사용자가 계속해서 쿠키 사이트 목록을 편집하여 URL을 추가하거나 제거할 수 있습니다. 그러나 관리자가 추가한 URL은 제거할 수 없습니다.

이 정책을 사용하면 브라우저를 닫을 때 쿠키 목록이 삭제되지 않습니다.

이 정책을 사용하지 않도록 설정하거나 구성하지 않으면 사용자의 개인 구성이 사용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SaveCookiesOnExit
  - GP 이름: Microsoft Edge 종료 시 쿠키를 저장합니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SaveCookiesOnExit
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SavingBrowserHistoryDisabled
  #### 브라우저 기록 저장 사용 안 함
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  브라우저 기록 저장을 사용하지 않도록 설정하고 사용자가 이 설정을 변경할 수 없게 합니다.

이 정책을 사용하면 검색 기록 저장되지 않습니다. 이렇게 하면 탭 동기화도 사용하지 않도록 설정됩니다.

이 정책을 사용하지 않거나 구성하지 않으면, 검색 기록이 저장됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SavingBrowserHistoryDisabled
  - GP 이름: 브라우저 기록 저장 사용 안 함
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: SavingBrowserHistoryDisabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SavingBrowserHistoryDisabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ScreenCaptureAllowed
  #### 화면 캡처 허용 또는 거부
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 83 이상

  #### 설명
  이 정책을 사용하거나 이 정책을 구성하지 않으면 웹 페이지에서 화면 캡처를 위한 화면 공유 API(예: getDisplayMedia() 또는 데스크톱 캡처 확장 API)를 사용할 수 있습니다.
이 정책을 사용하지 않도록 설정하면 화면 공유 API 호출이 실패합니다. 예를 들어, 웹 기반 온라인 모임을 사용하는 경우 비디오나 화면 공유가 작동하지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ScreenCaptureAllowed
  - GP 이름: 화면 캡처 허용 또는 거부
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ScreenCaptureAllowed
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ScreenCaptureAllowed
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ScrollToTextFragmentEnabled
  #### URL 조각에 지정된 텍스트로의 스크롤 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 83 이상

  #### 설명
  이 기능을 사용하면 하이퍼링크 및 주소 표시줄 URL 탐색이 웹 페이지의 특정 텍스트를 대상으로 하여 웹 페이지 로드가 완료된 후 해당 텍스트를 스크롤할 수 있습니다.

이 정책을 사용하도록 설정하거나 구성하지 않으면 URL을 통한 특정 텍스트 조각으로의 웹 페이지 스크롤이 사용됩니다.

이 정책을 사용하지 않으면 URL을 통한 특정 텍스트 조각으로의 웹 페이지 스크롤이 사용되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ScrollToTextFragmentEnabled
  - GP 이름: URL 조각에 지정된 텍스트로의 스크롤 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ScrollToTextFragmentEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ScrollToTextFragmentEnabled
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SearchSuggestEnabled
  #### 검색 제안 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge의 주소 표시줄 및 자동 제안 목록에서 웹 검색 제안을 사용하도록 설정하고 사용자가 이 정책을 변경할 수 없도록 합니다.

이 정책을 사용하면 웹 검색 제안이 사용됩니다.

이 정책을 사용하지 않으면 웹 검색 제안은 절대 사용되지 않지만 로컬 검색 기록 및 로컬 즐겨찾기 제안은 계속 표시됩니다. 이 정책을 사용하지 않으면 입력한 문자나 방문한 URL이 모두 원격 분석에 포함되지 않습니다.

이 정책을 설정하지 않으면 검색 제안이 사용되지만 사용자가 변경할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SearchSuggestEnabled
  - GP 이름: 검색 제안 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: SearchSuggestEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SearchSuggestEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SecurityKeyPermitAttestation
  #### 직접 보안 키 증명 사용 권한이 필요하지 않은 웹 사이트 또는 도메인
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  보안 키의 증명 인증서를 요청할 때 명시 적 사용자의 사용 권한이 필요하지 않은 웹 사이트 및 도메인을 지정합니다. 또한 개별 증명을 사용할 수 있음을 나타내는 신호가 보안 키로 전송됩니다. 이 옵션이 없으면 사이트에서 보안 키의 인증을 요청할 때마다 사용자에게 메시지가 표시됩니다.

사이트 (예: https://contoso.com/some/path)은(는) U2F appID로만 일치합니다. 도메인(예: contoso.com)은(는) webauthn RP ID로만 일치합니다. 특정 사이트에 대한 U2F 및 webauthn API를 모두 포괄하려면 appID URL과 도메인을 모두 나열해야 합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SecurityKeyPermitAttestation
  - GP 이름: 직접 보안 키 증명 사용 권한이 필요하지 않은 웹 사이트 또는 도메인
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation\1 = "https://contoso.com"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SecurityKeyPermitAttestation
  - 예제 값:
``` xml
<array>
  <string>https://contoso.com</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SendIntranetToInternetExplorer
  #### 모든 인트라넷 사이트를 Internet Explorer로 보내기
  
  
  #### 지원되는 버전:
  - Windows 77 이상부터

  #### 설명
  Internet Explorer 모드를 위한 최적의 환경을 구성하는 방법에 대한 지침은 [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SendIntranetToInternetExplorer
  - GP 이름: 모든 인트라넷 사이트를 Internet Explorer로 보내기
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: SendIntranetToInternetExplorer
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SendSiteInfoToImproveServices
  #### Microsoft 서비스 개선을 위해 사이트 정보 보내기 (사용되지 않음)
  >사용되지 않음: 이 정책은 더 이상 사용되지 않습니다. 현재 지원되고 있으나 향후 릴리스에서는 사용되지 않을 예정입니다.
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  이 정책은 더 이상 사용되지 않습니다. 현재 지원되고 있지만 Microsoft Edge 89에서 더 이상 사용되지 않습니다. 이 정책은 Windows 7, Windows 8, macOS에 대한 새 정책 [DiagnosticData](#diagnosticdata)로 대체됩니다. 이 정책은 Win 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569))에 대한 원격 분석 허용으로 대체됩니다.

Microsoft Edge에서 방문한 웹 사이트에 대한 정보를 Microsoft에 전송하여 검색 등의 서비스를 개선하려면 이 정책을 사용하도록 설정합니다.

Microsoft Edge에서 방문한 웹 사이트에 대 한 정보를 Microsoft에 전송하려면 이 정책을 사용하도록 설정합니다. Microsoft Edge에서 방문한 웹 사이트에 대한 정보를 Microsoft에 전송하지 않으려면 이 정책을 사용하지 않도록 설정합니다. 두 경우 모두 사용자가 설정을 변경하거나 재정의할 수 없습니다.

Windows 10에서 이 정책을 구성하지 않으면 Microsoft Edge은(는) 기본적으로 Windows 진단 데이터 설정으로 설정됩니다. 이 정책을 사용하면 Microsoft Edge은(는) Windows 진단 데이터 설정이 전체로 설정된 경우에만 Microsoft Edge에서 방문한 웹 사이트에 대한 정보를 전송합니다. 이 정책을 사용하지 않도록 설정한 경우 Microsoft Edge은(는) 방문한 웹 사이트에 대한 정보를 전송하지 않습니다. Windows 진단 데이터 설정에 대한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)를 참조하세요.

Windows 7, Windows 8, MacOS에서 이 정책은 방문한 웹 사이트에 대한 정보의 전송을 제어합니다. 이 정책을 구성하지 않으면 Microsoft Edge은(는) 기본적으로 사용자의 기본 설정입니다.

이 정책을 사용하려면 [MetricsReportingEnabled](#metricsreportingenabled)을(를) 사용하는 것으로 설정해야 합니다. [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)(이)나 [MetricsReportingEnabled](#metricsreportingenabled)이(가) 구성되지 않거나 사용하도록 설정되지 않은 경우이 데이터는 Microsoft에 전송되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SendSiteInfoToImproveServices
  - GP 이름: Microsoft 서비스 개선을 위해 사이트 정보 보내기 (사용되지 않음)
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: SendSiteInfoToImproveServices
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SendSiteInfoToImproveServices
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SensorsAllowedForUrls
  #### 특정 사이트의 센서에 대한 액세스 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  URL 패턴을 기반으로 동작 및 광 센서와 같은 센서에 액세스하고 사용할 수 있는 사이트 목록을 정의합니다.

이 정책을 구성하지 않는 경우 [DefaultSensorsSetting](#defaultsensorssetting) 정책(설정된 경우) 또는 사용자의 개인 구성이 모든 사이트에 사용됩니다.

이 정책과 일치하지 않는 URL 패턴의 경우 다음 우선 순위가 사용됩니다. [SensorsBlockedForUrls](#sensorsblockedforurls) 정책(일치하는 경우), [DefaultSensorsSetting](#defaultsensorssetting) 정책(설정된 경우) 또는 사용자의 개인 설정.

이 정책에 정의된 URL 패턴은 [SensorsBlockedForUrls](#sensorsblockedforurls) 정책에 구성된 패턴과 충돌할 수 없습니다. URL을 허용 및 차단할 수 없습니다.

유효한 URL 패턴에 대한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SensorsAllowedForUrls
  - GP 이름: 특정 사이트의 센서에 대한 액세스 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SensorsAllowedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SensorsBlockedForUrls
  #### 특정 사이트의 센서에 대한 액세스 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  URL 패턴을 기반으로 동작 및 광 센서와 같은 센서에 액세스 할 수없는 사이트 목록을 정의합니다.

이 정책을 구성하지 않으면 [DefaultSensorsSetting](#defaultsensorssetting) 정책(설정된 경우) 또는 사용자의 개인 구성이 모든 사이트에 사용됩니다.

이 정책과 일치하지 않는 URL 패턴의 경우 다음 우선 순위가 사용됩니다. [SensorsAllowedForUrls](#sensorsallowedforurls) 정책(일치하는 결과가 있을 경우), [DefaultSensorsSetting](#defaultsensorssetting) 정책(설정된 경우) 또는 사용자의 개인 설정.

이 정책에 정의된 URL 패턴은 [SensorsAllowedForUrls](#sensorsallowedforurls) 정책에 구성된 패턴과 충돌 할 수 없습니다. URL을 허용 및 차단할 수 없습니다.

유효한 URL 패턴에 대한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SensorsBlockedForUrls
  - GP 이름: 특정 사이트의 센서에 대한 액세스 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SensorsBlockedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SerialAskForUrls
  #### 특정 사이트에서 직렬 API 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  URL 패턴을 기반으로 직렬 포트에 대한 액세스 권한을 사용자에게 요청할 수 있는 사이트 목록을 정의합니다.

이 정책을 구성하지 않으면 [DefaultSerialGuardSetting](#defaultserialguardsetting) 정책(설정된 경우) 또는 사용자의 개인 구성의 전역 기본값이 모든 사이트에 사용됩니다.

이 정책과 일치하지 않는 URL 패턴의 경우 [SerialBlockedForUrls](#serialblockedforurls) 정책(일치하는 경우), [DefaultSerialGuardSetting](#defaultserialguardsetting) 정책(설정된 경우) 또는 사용자 개인 설정의 순서로 사용됩니다.

이 정책에 정의된 URL 패턴이 [SerialBlockedForUrls](#serialblockedforurls) 정책에 구성된 URL 패턴과 충돌할 수 없습니다. URL을 허용할 수 없으며 차단할 수 없습니다.

유효한 URL 패턴에 대한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SerialAskForUrls
  - GP 이름: 특정 사이트에서 직렬 API 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SerialAskForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SerialBlockedForUrls
  #### 특정 사이트에서 직렬 API 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  URL 패턴을 기반으로 직렬 포트에 대한 액세스 권한 부여를 사용자에게 요청할 수 없는 사이트 목록을 정의합니다.

이 정책을 구성하지 않으면 [DefaultSerialGuardSetting](#defaultserialguardsetting) 정책(설정된 경우) 또는 사용자의 개인 구성의 전역 기본값이 모든 사이트에 사용됩니다.

이 정책과 일치하지 않는 URL 패턴의 경우 [SerialAskForUrls](#serialaskforurls) 정책(일치하는 경우), [DefaultSerialGuardSetting](#defaultserialguardsetting) 정책(설정된 경우) 또는 사용자 개인 설정의 순서로 사용됩니다.

이 정책의 URL 패턴은 [SerialAskForUrls](#serialaskforurls) 정책에 구성된 URL 패턴과 충돌할 수 없습니다. URL을 허용할 수 없으며 차단할 수 없습니다.

유효한 URL 패턴에 대한 자세한 내용은 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)를 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SerialBlockedForUrls
  - GP 이름: 특정 사이트에서 직렬 API 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SerialBlockedForUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### ShowOfficeShortcutInFavoritesBar
  #### 즐겨 찾기 모음에 Microsoft Office 바로 가기 표시
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  즐겨 찾기 모음에 Office.com에 대한 바로 가기를 포함할지 여부를 지정합니다. Microsoft Edge에 로그인한 사용자는 바로 가기를 통해 Microsoft Office 앱 및 문서로 이동합니다.

이 정책을 사용하거나 설정하지 않은 경우 즐겨 찾기 모음 상황에 맞는 메뉴에서 토글을 변경하여 바로 가기를 표시할지 여부를 선택할 수 있습니다.

정책을 사용하지 않으면 바로 가기가 표시되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: ShowOfficeShortcutInFavoritesBar
  - GP 이름: 즐겨 찾기 모음에 Microsoft Office 바로 가기 표시
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: ShowOfficeShortcutInFavoritesBar
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: ShowOfficeShortcutInFavoritesBar
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SignedHTTPExchangeEnabled
  #### 서명된 HTTP 교환(SXG) 지원 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 78 이상

  #### 설명
  서명된 HTTP Exchange(SXG) 지원을 사용하도록 설정합니다.

이 정책을 설정하거나 사용하지 않으면 Microsoft Edge가 서명된 HTTP Exchange로 제공되는 웹 콘텐츠를 수락합니다.

이 정책을 사용하지 않도록 설정하면 서명된 HTTP Exchange를 로드할 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SignedHTTPExchangeEnabled
  - GP 이름: 서명된 HTTP 교환(SXG) 지원 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: SignedHTTPExchangeEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SignedHTTPExchangeEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SitePerProcess
  #### 모든 사이트에 대해 사이트 격리 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  'SitePerProcess' 정책을 사용하면 사용자가 모든 사이트를 격리하는 기본 동작을 해제하지 못하도록 할 수 있습니다. [IsolateOrigins](#isolateorigins) 정책을 사용하여 보다 세분화된 추가 출처를 격리할 수도 있습니다.
이 정책을 사용하면 각 사이트가 자체 프로세스에서 실행되는 기본 동작을 사용자가 해제할 수 없습니다.
이 정책을 구성하지 않으면 사용자가 사이트 격리를 해제할 수 있습니다. 예를 들어, edge://flags에서 "사이트 격리 사용 안 함" 항목을 사용하여 해제합니다. 정책을 사용하지 않거나 구성하지 않아도 사이트 격리가 해제되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SitePerProcess
  - GP 이름: 모든 사이트에 대해 사이트 격리 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: SitePerProcess
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SitePerProcess
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SpellcheckEnabled
  #### 맞춤법 검사 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  정책을 사용하거나 사용하지 않으면 사용자가 맞춤법 검사를 사용할 수 있습니다.

이 정책을 사용하지 않으면 사용자가 맞춤법 검사를 사용할 수 없으며 [SpellcheckLanguage](#spellchecklanguage) 및 [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) 정책도 사용하지 않도록 설정됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SpellcheckEnabled
  - GP 이름: 맞춤법 검사 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: SpellcheckEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SpellcheckEnabled
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SpellcheckLanguage
  #### 특정 맞춤법 검사 언어 사용
  
  
  #### 지원되는 버전:
  - Windows 77 이상부터

  #### 설명
  맞춤법 검사에 대해 다른 언어를 사용하도록 설정합니다. 인식되지 않는 사용자가 지정한 언어는 무시됩니다.

이 정책을 사용하면 지정된 언어뿐만 아니라 사용자가 사용하도록 설정한 모든 언어에 대해 맞춤법 검사가 사용됩니다.

이 정책을 구성하지 않거나 사용하지 않으면 사용자의 맞춤법 기본 설정이 변경되지 않습니다.

[SpellcheckEnabled](#spellcheckenabled) 정책을 사용하지 않으면 이 정책이 적용되지 않습니다.

언어가 'SpellcheckLanguage'와 [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) 정책에 모두 포함되어 있으면 맞춤법 검사 언어가 사용됩니다.

지원되는 언어는 다음과 같습니다: af, bg, ca, cs, cy, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SpellcheckLanguage
  - GP 이름: 특정 맞춤법 검사 언어 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\2 = "es"

```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SpellcheckLanguageBlocklist
  #### 맞춤법 검사 언어 강제 사용 안 함
  
  
  #### 지원되는 버전:
  - Windows 78 이상부터

  #### 설명
  맞춤법 검사 언어를 강제로 사용하지 않도록 설정합니다. 해당 목록에서 인식할 수 없는 언어는 무시됩니다.

이 정책을 사용하면 지정된 언어에 대한 맞춤법 검사를 사용할 수 없습니다. 사용자는 계속 목록에 없는 언어에 대해 맞춤법 검사를 사용하거나 사용하지 않도록 설정할 수 있습니다.

이 정책을 설정하지 않거나 사용하지 않도록 설정하면 사용자의 맞춤법 검사 기본 설정이 변경되지 않습니다.

[SpellcheckEnabled](#spellcheckenabled) 정책을 사용 안 함으로 설정되어 있으면 이 정책은 적용되지 않습니다.

언어가 [SpellcheckLanguage](#spellchecklanguage) 및 'SpellcheckLanguageBlocklist' 정책에 모두 포함되어 있으면 맞춤법 검사 언어가 사용됩니다.

현재 지원되는 언어는 다음과 같습니다: af, bg, ca, cs, da, de, el, en-AU, en-CA, en-GB, en-US, es, es-419, es-AR, es-ES, es-MX, es-US, et, fa, fo, fr, he, hi, hr, hu, id, it, ko, lt, lv, nb, nl, pl, pt-BR, pt-PT, ro, ru, sh, sk, sl, sq, sr, sv, ta, tg, tr, uk, vi.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SpellcheckLanguageBlocklist
  - GP 이름: 맞춤법 검사 언어 강제 사용 안 함
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\2 = "es"

```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### StricterMixedContentTreatmentEnabled
  #### 혼합 콘텐츠에 대해 보다 엄격한 처리 가능 (사용되지 않음)
  >사용되지 않음: 이 정책은 더 이상 사용되지 않습니다. 현재 지원되고 있으나 향후 릴리스에서는 사용되지 않을 예정입니다.
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 81 이상

  #### 설명
  이 정책은 더욱 엄격한 혼합 콘텐츠 처리와 호환되지 않는 경우에 기업에 웹 콘텐츠를 업데이트하는 데 더 많은 시간을 제공하기 위한 목적의 단기간 메커니즘일 뿐이므로 사용되지 않습니다. 이 정책은 Microsoft Edge 버전 85에서 작동하지 않게 됩니다.

이 정책은 브라우저에서 혼합 콘텐츠(HTTPS 사이트의 HTTP 콘텐츠)에 대한 처리를 제어합니다.

 이 정책을 true로 설정하거나 설정하지 않으면 오디오 및 비디오 혼합 콘텐츠가 자동으로 HTTPS로 업그레이드됩니다. 즉, HTTPS를 통해 리소스를 사용할 수 없는 경우 대체 없이 URL이 HTTPS로 다시 작성됩니다. 이미지 혼합 콘텐츠의 경우 URL 표시줄에 '안전하지 않음' 경고가 표시됩니다.

이 정책을 false로 설정하면 오디오 및 비디오에 대한 자동 업그레이드가 비활성화되고 이미지에 대한 경고가 표시되지 않습니다.

 이 정책은 오디오, 비디오 및 이미지 이외의 다른 유형의 혼합 콘텐츠에는 영향을 주지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: StricterMixedContentTreatmentEnabled
  - GP 이름: 혼합 콘텐츠에 대해 보다 엄격한 처리 가능 (사용되지 않음)
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: StricterMixedContentTreatmentEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: StricterMixedContentTreatmentEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SuppressUnsupportedOSWarning
  #### 지원 되지 않는 OS 경고 표시 안 함
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge이(가) 더 이상 지원되지 않는 컴퓨터 나 운영 체제에서 실행되고 있을 때 표시되는 경고를 표시하지 않습니다.

이 정책이 false이거나 설정되어 있지 않으면 지원되지 않는 컴퓨터 또는 운영 체제에 경고가 표시됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SuppressUnsupportedOSWarning
  - GP 이름: 지원 되지 않는 OS 경고 표시 안 함
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: SuppressUnsupportedOSWarning
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SuppressUnsupportedOSWarning
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SyncDisabled
  #### Microsoft 동기화 서비스를 사용한 데이터의 동기화 사용 안 함
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge에서 데이터 동기화를 사용하지 않도록 설정합니다. 또한 이 정책은 동기화 동의 프롬프트가 나타나지 않도록 합니다.

이 정책을 설정하지 않거나 권장으로 적용하면 사용자는 동기화를 켜거나 끌 수 있습니다. 이 정책을 필수로 적용하면 사용자는 동기화를 켤 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SyncDisabled
  - GP 이름: Microsoft 동기화 서비스를 사용한 데이터의 동기화 사용 안 함
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: SyncDisabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SyncDisabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### SyncTypesListDisabled
  #### 동기화에서 제외되는 형식 목록 구성하기
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 83 이상

  #### 설명
  이 정책을 사용하면 모든 지정된 데이터 형식은 동기화에서 제외됩니다. 이 정책을 사용하여 Microsoft Edge 동기화 서비스로 업로드되는 데이터 형식을 제한할 수 있습니다.

이 정책에 대해 "favorites", "settings", "passwords", "addressesAndMore", "extensions", "history", "openTabs" 및 “collections” 데이터 형식 중 하나를 제공할 수 있습니다. 이러한 데이터 형식 이름은 대/소문자를 구분합니다.

사용자는 비활성화된 데이터 형식을 재정의할 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: SyncTypesListDisabled
  - GP 이름: 동기화에서 제외되는 형식 목록 구성하기
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled\1 = "favorites"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: SyncTypesListDisabled
  - 예제 값:
``` xml
<array>
  <string>favorites</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### TLS13HardeningForLocalAnchorsEnabled
  #### 로컬 트러스트 앵커에 대해 TLS 1.3 보안 기능을 사용하도록 설정합니다. (사용하지 않음)
  
  >사용되지 않음: 이 정책은 사용되지 않으며 Microsoft Edge 85 이후에는 작동되지 않습니다.
  #### 지원되는 버전:
  - Windows macOS 81 이후 85

  #### 설명
  이 정책은 엔터프라이즈가 영향을 받는 프록시를 업그레이드하는 데 보다 충분한 시간을 줄 수 있도록 단기 메커니즘의 목적으로만 사용되기 때문에 작동하지 않습니다.

이 정책은 다운그레이드 공격으로부터 연결을 보호하는 TLS 1.3의 보안 기능을 제어합니다. 이전 버전과 호환되며 호환되는 TLS 1.2 서버 또는 프록시에 대한 연결에는 영향을 주지 않습니다. 그러나 일부 TLS 가로채기 프록시의 이전 버전에는 호환되지 않도록 하는 구현 결함이 있습니다.

이 정책을 사용하거나 설정하지 않으면 Microsoft Edge에서 모든 연결에 대해 해당 보안 보호를 사용하도록 설정합니다.

이 정책을 사용하지 않으면 Microsoft Edge에서 로컬로 설치된 CA 인증서로 인증된 연결에 대해 해당 보안 보호를 사용하지 않도록 설정합니다. 이러한 보호는 공개적으로 신뢰할 수 있는 CA 인증서로 인증된 연결에 대해 항상 사용할 수 있습니다.

이 정책은 영향을 받는 프록시를 테스트하고 업그레이드하는 데 사용될 수 있습니다. 영향을 받는 프록시는 ERR_TLS13_DOWNGRADE_DETECTED 오류 코드로 연결에 실패할 것으로 예상됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: TLS13HardeningForLocalAnchorsEnabled
  - GP 이름: 로컬 트러스트 앵커에 대해 TLS 1.3 보안 기능을 사용하도록 설정합니다. (사용하지 않음)
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: TLS13HardeningForLocalAnchorsEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: TLS13HardeningForLocalAnchorsEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### TLSCipherSuiteDenyList
  #### 비활성화할 TLS 암호 그룹 지정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 85 이상

  #### 설명
  TLS 연결을 사용하지 않도록 설정된 암호 그룹 목록을 구성합니다.

해당 정책을 구성하면 TLS 연결 설정 시 구성된 암호 그룹 목록을 사용하지 않습니다.

해당 정책을 구성하지 않으면 브라우저가 사용할 TLS 암호 그룹을 선택합니다.

사용하지 않으려는 암호 그룹 값은 16비트 16진수 값으로 지정됩니다. 해당 값은 IANA(인터넷 할당 번호 기관) 레지스트리에 의해 할당됩니다.

TLS 1.3 암호 그룹 TLS_AES_128_GCM_SHA256 (0x1301)은 TLS 1.3에 필요하며 해당 정책으로 비활성화할 수 없습니다.

해당 정책은 QUIC 기반 연결에 영향을 주지 않습니다. QUIC는 [QuicAllowed](#quicallowed) 정책을 통해 설정 해제할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: TLSCipherSuiteDenyList
  - GP 이름: 비활성화할 TLS 암호 그룹 지정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\1 = "0x1303"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\2 = "0xcca8"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\3 = "0xcca9"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: TLSCipherSuiteDenyList
  - 예제 값:
``` xml
<array>
  <string>0x1303</string>
  <string>0xcca8</string>
  <string>0xcca9</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### TabFreezingEnabled
  #### 배경 탭의 고정 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 79 이상

  #### 설명
  Microsoft Edge가 5분 이상 백그라운드에 있는 탭을 고정할 수 있는지 여부를 제어합니다.

탭 고정은 CPU, 배터리, 및 메모리 사용량을 줄입니다. Microsoft Edge는 경험적 접근을 사용하여 알림 표시, 소리 재생 및 비디오 스트리밍과 같이 백그라운드에서 유용한 작업을 수행하는 탭이 고정되는 것을 방지합니다.

이 정책을 사용하도록 설정하거나 구성하지 않으면 5분 이상 백그라운드에 있었던 탭이 고정될 수 있습니다.

이 정책을 사용하지 않도록 설정하면 탭이 고정되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: TabFreezingEnabled
  - GP 이름: 배경 탭의 고정 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: TabFreezingEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: TabFreezingEnabled
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### TaskManagerEndProcessEnabled
  #### 브라우저 작업 관리자에서 종료 프로세스 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  이 정책을 사용하거나 사용하지 않도록 설정하면 사용자가 브라우저 작업 관리자에서 프로세스를 종료할 수 있습니다. 이 기능을 사용하지 않으면 사용자가 프로세스를 종료할 수 없으며 브라우저 작업 관리자에서 [프로세스 끝내기] 단추가 비활성화됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: TaskManagerEndProcessEnabled
  - GP 이름: 브라우저 작업 관리자에서 종료 프로세스 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: TaskManagerEndProcessEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: TaskManagerEndProcessEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### TotalMemoryLimitMb
  #### 단일 Microsoft Edge 인스턴스에서 사용할 수 있는 메모리 크기(MB)를 설정합니다.
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 80 이상

  #### 설명
  메모리를 절약하기 위해 탭이 삭제되기 전에 단일 Microsoft Edge 인스턴스에서 사용할 수 있는 메모리 양을 구성합니다. 탭에서 사용하는 메모리가 해제되며 전환될 때 탭이 다시 로드되어야 합니다.

이 정책을 사용하면 제한을 초과했을 때 브라우저에서 메모리를 절약하기 위해 탭을 삭제하기 시작합니다. 그러나 브라우저가 항상 제한 이하로 실행된다는 보장은 없습니다. 1024 미만의 모든 값은 1024로 반올림됩니다.

이 정책을 설정하지 않으면 브라우저는 컴퓨터의 실제 메모리 용량이 부족하다는 것을 감지한 경우에만 메모리 절약을 시도합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: TotalMemoryLimitMb
  - GP 이름: 단일 Microsoft Edge 인스턴스에서 사용할 수 있는 메모리 크기(MB)를 설정합니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: TotalMemoryLimitMb
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000800
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: TotalMemoryLimitMb
  - 예제 값:
``` xml
<integer>2048</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### TrackingPrevention
  #### 사용자의 웹 검색 활동 추적 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 78 이상

  #### 설명
  웹 사이트가 사용자의 웹 검색 활동을 추적하지 못하도록 차단할지 여부를 결정할 수 있습니다.

이 정책을 사용하지 않도록 설정하거나 구성하지 않으면 사용자가 자체 추적 방지 수준을 설정할 수 있습니다.

정책 옵션 매핑:

* TrackingPreventionOff (0) = 꺼짐(추적 방지 안 함)

* TrackingPreventionBasic (1) = 기본(유해한 추적기 차단, 콘텐츠 및 광고가 개인 설정됨)

* TrackingPreventionBalanced (2) = 균형 조정(유해한 추적기 및 사용자가 방문하지 않은 사이트의 추적기 차단, 콘텐츠 및 광고의 개인 설정 수준이 낮아짐)

* TrackingPreventionStrict (3) = 엄격(모든 사이트에서 유해한 추적기 및 대부분의 추적기 차단, 콘텐츠 및 광고의 개인 설정이 최소화됨, 사이트의 일부 부분이 작동하지 않을 수 있음)

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: TrackingPrevention
  - GP 이름: 사용자의 웹 검색 활동 추적 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: TrackingPrevention
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000002
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: TrackingPrevention
  - 예제 값:
``` xml
<integer>2</integer>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### TranslateEnabled
  #### 번역 사용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge에서 통합된 Microsoft 번역 서비스를 사용하도록 설정합니다.

이 정책을 사용하면 Microsoft Edge는 오른쪽 클릭 상황에 맞는 메뉴에서 통합된 번역 플라이아웃(해당되는 경우) 및 번역 옵션을 표시하여 사용자에게 번역 기능을 제공합니다.

이 정책을 사용하지 않으면 기본 제공 번역 기능이 모두 사용하지 않도록 설정됩니다.

정책을 구성하지 않으면 사용자가 변역 기능을 사용할지 여부를 선택할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 예
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: TranslateEnabled
  - GP 이름: 번역 사용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 관리 템플릿/Microsoft Edge - 기본 설정(사용자가 재정의할 수 없음)/
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): SOFTWARE\Policies\Microsoft\Edge\맞춤
  - 값 이름: TranslateEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: TranslateEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### URLAllowlist
  #### 허용된 URL 목록을 정의
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  URL 블록 목록에 대한 예외로 나열된 URL에 대한 액세스를 허용합니다.

[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)에 따라 URL 패턴을 포맷합니다.

이 정책을 사용하여 제한적 차단 목록에 대한 예외를 열 수 있습니다. 예를 들어 차단 목록에 '*'를 포함하여 모든 요청을 차단한 다음 이 정책을 사용하여 제한된 URL 목록에 액세스할 수 있습니다. 이 정책을 사용하여 특정 구성표, 다른 도메인의 하위 도메인 또는 특정 경로에 대한 예외를 열 수 있습니다.

가장 구체적인 필터는 URL의 차단 여부를 결정합니다. 허용된 목록이 차단 목록보다 우선합니다.

이 정책은 1000개의 항목으로 제한되며 후속 항목은 무시됩니다.

이 정책을 사용하면 브라우저가 "전화:" 또는 "ssh:"와 같은 프로토콜에 대해 프로토콜 처리기로 등록된 외부 응용 프로그램을 자동으로 호출할 수도 있습니다.

이 정책을 구성하지 않으면 [URLBlocklist](#urlblocklist) 정책에 차단 목록에 예외가 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: URLAllowlist
  - GP 이름: 허용된 URL 목록을 정의
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\URLAllowlist
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\5 = ".exact.hostname.com"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: URLAllowlist
  - 예제 값:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### URLBlocklist
  #### URL 목록에 대한 액세스 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  URL 패턴을 기반으로, 차단되는 사이트 목록을 정의합니다(사용자가 로드할 수 없음).

[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)에 따라 URL 패턴의 서식을 지정합니다.

[URLAllowlist](#urlallowlist) 정책에서 예외를 정의할 수 있습니다. 이 정책은 1000개의 항목으로 제한되며, 이후 항목은 무시됩니다.

참고: 내부 'edge://*' URL을 차단하는 것은 권장되지 않습니다. - 이렇게 하면 예기치 않은 오류가 발생할 수 있습니다.

이 정책은 페이지가 JavaScript를 통해 동적으로 업데이트되는 것을 막지 않습니다. 예를 들어 'contoso.com/abc'를 차단하면 페이지가 새로 고침되지 않는 한 'contoso.com'을 방문하고 링크를 클릭하여 'contoso.com/abc'를 방문할 수 있습니다.

이 정책을 구성하지 않으면 URL이 차단되지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: URLBlocklist
  - GP 이름: URL 목록에 대한 액세스 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\URLBlocklist
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
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


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: URLBlocklist
  - 예제 값:
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
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### UserAgentClientHintsEnabled
  #### 사용자 에이전트 클라이언트 힌트 기능 사용 (사용되지 않음)
  >사용되지 않음: 이 정책은 더 이상 사용되지 않습니다. 현재 지원되고 있으나 향후 릴리스에서는 사용되지 않을 예정입니다.
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 86 이상

  #### 설명
  이 정책은 엔터프라이즈에서 사용자 에이전트 클라이언트 힌트 기능과 호환되지 않는 경우 해당 웹 콘텐츠를 업데이트하는 데 충분한 시간을 줄 수 있도록 단기 메커니즘의 목적으로만 사용되기 때문에 더 이상 사용되지 않습니다. Microsoft Edge 버전 89에서는 작동하지 않습니다.

사용자 에이전트 클라이언트 힌트 기능은 사용자 브라우저(예: 브라우저 버전) 및 환경(예: 시스템 아키텍처)에 대한 정보를 제공하는 세분화된 요청 헤더를 보냅니다.

이 기능은 추가 기능이지만 새 헤더는 요청에 포함될 수 있는 문자를 제한하는 일부 웹 사이트를 손상시킬 수 있습니다.

이 정책을 사용하도록 설정하거나 구성하지 않으면 사용자 에이전트 클라이언트 힌트 기능을 사용할 수 있습니다. 이 정책을 사용하지 않도록 설정하면 이 기능을 사용할 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: UserAgentClientHintsEnabled
  - GP 이름: 사용자 에이전트 클라이언트 힌트 기능 사용 (사용되지 않음)
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: UserAgentClientHintsEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: UserAgentClientHintsEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### UserDataDir
  #### 사용자 데이터 디렉터리 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사용자 데이터를 저장하는 데 사용할 디렉터리를 설정합니다.

이 정책을 사용하면 Microsoft Edge는 사용자가 '--user-data-dir' 명령줄 플래그를 설정했는지 여부에 관계 없이 지정된 디렉터리를 사용합니다.

이 정책을 사용하지 않으면 기본 프로필 경로가 사용되지만 사용자가 '--user-data-dir' 플래그를 사용하여 이 경로를 재정의할 수 있습니다. 사용자는 프로필 경로에 있는 edge://version/에서 프로필 디렉터리를 찾을 수 있습니다.

데이터 손실이나 기타 오류가 발생하지 않도록 하려면 Microsoft Edge에서 콘텐츠를 관리하므로 볼륨의 루트 디렉터리 또는 다른 용도로 사용되는 디렉터리에 이 정책을 구성하지 마세요.

사용할 수 있는 변수 목록은 [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041)을 참조하세요.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: UserDataDir
  - GP 이름: 사용자 데이터 디렉터리 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: UserDataDir
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"${users}/${user_name}/Edge"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: UserDataDir
  - 예제 값:
``` xml
<string>${users}/${user_name}/Edge</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### UserDataSnapshotRetentionLimit
  #### 비상 롤백이 있을 경우 사용하기 위해 보존된 사용자 데이터 스냅숏 수를 제한합니다.
  
  
  #### 지원되는 버전:
  - Windows 86 이상부터

  #### 설명
  각 주요 버전 업데이트 후 Microsoft Edge는 임시 버전 롤백이 필요한 이후 비상 상황의 경우에 사용할 사용자의 검색 데이터 부분에 대한 스냅숏을 만듭니다. 사용자에게 해당 스냅숏이 있는 버전에 임시 롤백이 수행되면 스냅숏의 데이터가 복원됩니다. 이를 통해 사용자는 책갈피와 자동 채우기 데이터 등의 설정을 유지할 수 있습니다.

이 정책을 설정하지 않으면 세 가지 스냅숏의 기본값이 사용 됩니다.

이 정책을 설정하면 사용자가 설정한 제한을 고려하여 이전 스냅숏이 필요에 따라 삭제됩니다. 이 정책을 0으로 설정하면 스냅숏이 만들어지지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 정수

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: UserDataSnapshotRetentionLimit
  - GP 이름: 비상 롤백이 있을 경우 사용하기 위해 보존된 사용자 데이터 스냅숏 수를 제한합니다.
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: UserDataSnapshotRetentionLimit
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000003
```


  

  [맨 위로 이동](#microsoft-edge---정책)

  ### UserFeedbackAllowed
  #### 사용자 피드백 허용
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge는 사용자가 피드백, 제안 또는 고객 설문 조사를 보내고 브라우저 관련 문제를 보고할 수 있도록 Microsoft Edge 피드백 기능(기본적으로 사용하도록 설정됨)을 사용합니다.

이 정책을 사용하거나 구성하지 않으면 사용자가 피드백 가장자리를 호출할 수 있습니다.

이 정책을 사용하지 않으면 사용자가 Microsoft Edge 피드백을 호출할 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: UserFeedbackAllowed
  - GP 이름: 사용자 피드백 허용
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: UserFeedbackAllowed
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: UserFeedbackAllowed
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### VideoCaptureAllowed
  #### 비디오 캡처 허용 또는 차단
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  사이트에서 비디오를 캡처할 수 있는지 여부를 제어합니다.

이 정책을 사용하거나 구성하지 않으면(기본값) 메시지를 표시하지 않고 액세스 권한이 부여되는 [VideoCaptureAllowedUrls](#videocaptureallowedurls) 정책 목록에 구성된 URL을 제외한 모든 사이트의 비디오 캡처 액세스에 대해 사용자에게 묻는 메시지가 표시됩니다.

이 정책을 사용하지 않으면 사용자에게 메시지가 표시되지 않고, 비디오 캡처는 [VideoCaptureAllowedUrls](#videocaptureallowedurls) 정책에 구성된 URL에서만 사용할 수 있습니다.

이 정책은 기본 제공 카메라 뿐만 아니라 모든 유형의 비디오 입력에 영향을 줍니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: VideoCaptureAllowed
  - GP 이름: 비디오 캡처 허용 또는 차단
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: VideoCaptureAllowed
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000000
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: VideoCaptureAllowed
  - 예제 값:
``` xml
<false/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### VideoCaptureAllowedUrls
  #### 권한을 요청하지 않고 비디오 캡처 장치에 액세스할 수 있는 사이트
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  URL 패턴을 기반으로 사용자의 사용 권한없이 비디오 캡처 장치를 사용할 수 있는 웹 사이트를 지정합니다. 목록의 패턴은 요청 URL의 보안 원점과 비교됩니다. 일치할 경우 사이트에 자동으로 비디오 캡처 장치에 대한 액세스 권한이 부여됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: VideoCaptureAllowedUrls
  - GP 이름: 권한을 요청하지 않고 비디오 캡처 장치에 액세스할 수 있는 사이트
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: VideoCaptureAllowedUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### WPADQuickCheckEnabled
  #### WPAD 최적화 설정
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  Microsoft Edge에서 WPAD(웹 프록시 자동 검색) 최적화를 끌 수 있도록 허용합니다.

이 정책을 사용하지 않으면 WPAD 최적화가 사용하지 않도록 설정되므로 브라우저가 DNS 기반 WPAD 서버를 더 오래 기다립니다.

이 정책을 사용하거나 구성하지 않으면 WPAD 최적화가 사용하도록 설정됩니다.

이 정책의 사용 여부 또는 방법에 관계 없이 WPAD 최적화 설정은 사용자가 변경할 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: WPADQuickCheckEnabled
  - GP 이름: WPAD 최적화 설정
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: WPADQuickCheckEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: WPADQuickCheckEnabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### WebAppInstallForceList
  #### 강제 설치된 Web Apps 목록 구성
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 80 이상

  #### 설명
  사용자 상호 작용 없이 자동으로 설치되고 사용자가 제거하거나 사용할 수 없도록 설정한 웹 사이트 목록을 지정합니다.

정책의 각 목록 항목은 다음 멤버가 있는 개체입니다
  - "url"은 필수입니다. "url"은 설치할 웹앱의 URL이어야 합니다.

선택적 멤버의 값은 다음과 같습니다.
  - "launch_container"는 설치 후 웹앱을 어떻게 열 것인지를 나타내는 "윈도우"또는 "탭"이어야 합니다.
  - "create_desktop_shortcut"는 Windows에서 데스크탑 바로 가기를 만들어야 하는 경우 참이어야 합니다.

"default_launch_container"가 생략되면 앱이 기본적으로 탭에서 열립니다. "default_launch_container"의 값에 관계없이 사용자는 앱이 열리는 컨테이너를 변경할 수 있습니다. "create_desktop_shortcuts"가 생략되면 바탕 화면 바로 가기가 만들어지지 않습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 예

  #### 데이터 형식:
  - 사전

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: WebAppInstallForceList
  - GP 이름: 강제 설치된 Web Apps 목록 구성
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: WebAppInstallForceList
  - 값 형식: REG_SZ
  ##### 예제 값:
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


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: WebAppInstallForceList
  - 예제 값:
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
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### WebComponentsV0Enabled
  #### M84이 될 때까지 웹 구성 요소 v0 API 다시 사용 (사용하지 않음)
  
  >사용되지 않음: 이 정책은 사용되지 않으며 Microsoft Edge 84 이후에는 작동되지 않습니다.
  #### 지원되는 버전:
  - Windows macOS 80 이후 84

  #### 설명
  이 정책은 이 기능들이 Microsoft Edge 버전 85까지 선택적으로 다시 활성화되도록 허용하였기에 작동하지 않습니다. 웹 구성 요소 v0 API(Shadow DOM v0, 사용자 지정 요소 v0 및 HTML 가져오기)는 2018년에 사용이 중단되었으며, Microsoft Edge 버전 80부터 기본적으로 사용하지 않도록 설정되었습니다.

이 정책을 True로 설정하면 모든 사이트에 대해 웹 구성 요소 v0 기능이 사용하도록 설정됩니다.

이 정책을 False로 설정하거나 설정하지 않으면 Microsoft Edge 버전 80부터 웹 구성 요소 v0 기능이 기본적으로 사용하지 않도록 설정됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: WebComponentsV0Enabled
  - GP 이름: M84이 될 때까지 웹 구성 요소 v0 API 다시 사용 (사용하지 않음)
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: WebComponentsV0Enabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: WebComponentsV0Enabled
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### WebDriverOverridesIncompatiblePolicies
  #### WebDriver가 호환되지 않는 정책을 재정의하도록 허용 (사용하지 않음)
  
  >사용되지 않음: 이 정책은 사용되지 않으며 Microsoft Edge 84 이후에는 작동되지 않습니다.
  #### 지원되는 버전:
  - Windows macOS 77 이후 84

  #### 설명
  이 정책은 WebDriver가 이제 기존의 모든 정책과 호환되므로 작동하지 않습니다.

이 정책을 사용하면 WebDriver 기능의 사용자는 작업을 방해할 수 있는 정책을
무시할 수 있습니다.

현재 이 정책은 [SitePerProcess](#siteperprocess) 및 [IsolateOrigins](#isolateorigins) 정책을 사용하지 않도록 설정합니다.

이 정책을 사용하면 WebDriver에서 호환되지 않는
정책을 무시할 수 있습니다.
이 정책을 사용하지 않도록 설정하거나 구성하지 않으면 WebDriver는 호환되지 않는 정책을
무시할 수 없습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: WebDriverOverridesIncompatiblePolicies
  - GP 이름: WebDriver가 호환되지 않는 정책을 재정의하도록 허용 (사용하지 않음)
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: WebDriverOverridesIncompatiblePolicies
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: WebDriverOverridesIncompatiblePolicies
  - 예제 값:
``` xml
<true/>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### WebRtcLocalIpsAllowedUrls
  #### WebRTC에 의한 로컬 IP 주소 노출 관리
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 80 이상

  #### 설명
  로컬 IP 주소가 WebRTC에 의해 노출되어야 하는 원본(URL) 또는 호스트 이름 패턴(예: "*contoso.com*") 목록을 지정합니다.

이 정책을 사용하고 원본(URL) 또는 호스트 이름 패턴 목록을 설정하면 edge://flags/#enable-webrtc-hide-local-ips-with-mdns를 사용할 때 WebRTC는 목록에 있는 패턴과 일치하는 경우 로컬 IP 주소를 노출합니다.

이 정책을 사용하지 않도록 설정하거나 구성하지 않고 edge://flags/#enable-webrtc-hide-local-ips-with-mdns를 사용하면 WebRTC가 로컬 IP 주소를 노출하지 않습니다. 로컬 IP 주소는 mDNS 호스트 이름으로 숨겨집니다.

이 정책을 사용하거나 사용하지 않거나 구성하지 않고 edge://flags/#enable-webrtc-hide-local-ips-with-mdns를 사용하지 않도록 설정하면 WebRTC는 로컬 IP 주소를 노출합니다.

이 정책은 관리자가 필요로 하는 로컬 IP 주소의 보호를 약화시킵니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열 목록

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: WebRtcLocalIpsAllowedUrls
  - GP 이름: WebRTC에 의한 로컬 IP 주소 노출 관리
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls
  - 경로 (맞춤): 해당 없음
  - 값 이름: 1, 2, 3, ...
  - 값 형식: REG_SZ 목록
  ##### 예제 값:
```
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\2 = "*contoso.com*"

```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: WebRtcLocalIpsAllowedUrls
  - 예제 값:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>*contoso.com*</string>
</array>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### WebRtcLocalhostIpHandling
  #### WebRTC에 의한 로컬 IP 주소 노출 제한
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  WebRTC의 로컬 IP 주소 노출 여부를 설정할 수 있습니다.

이 정책을 "AllowAllInterfaces" 또는 "AllowPublicAndPrivate"로 설정한 경우입니다.인터페이스, WebRTC는 로컬 IP 주소를 노출합니다.

이 정책을 "PublicInterfaceOnly" 또는 "DisableNonProxiedUdp"로 설정하면 WebRTC가 로컬 IP 주소를 노출하지 않습니다.

이 정책을 설정하지 않았거나 사용하지 않도록 설정한 경우 WebRTC가 로컬 IP 주소를 노출합니다.

정책 옵션 매핑:

* AllowAllInterfaces (default) = 모든 인터페이스를 허용합니다. 로컬 IP 주소를 표시합니다.

* AllowPublicAndPrivateInterfaces (default_public_and_private_interfaces) = http 기본 경로를 통해 공개 및 비공개 인터페이스를 허용합니다. 로컬 IP 주소를 표시합니다.

* AllowPublicInterfaceOnly (default_public_interface_only) = http 기본 경로를 통한 공용 인터페이스를 허용합니다. 이는 로컬 IP 주소를 노출하지 않습니다.

* DisableNonProxiedUdp (disable_non_proxied_udp) = 프록시 서버가 UDP를 지원하지 않는 한 TCP를 사용하세요. 이것은 로컬 IP 주소를 노출하지 않습니다.

이 정책을 구성할 때 이전 정보를 사용합니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: WebRtcLocalhostIpHandling
  - GP 이름: WebRTC에 의한 로컬 IP 주소 노출 제한
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: WebRtcLocalhostIpHandling
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"default"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: WebRtcLocalhostIpHandling
  - 예제 값:
``` xml
<string>default</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### WebRtcUdpPortRange
  #### WebRTC에서 사용하는 로컬 UDP 포트 범위 제한
  
  
  #### 지원되는 버전:
  - Windows 및 macOS 이후 77 이상

  #### 설명
  WebRTC에서 사용하는 UDP 포트 범위를 지정된 포트 간격(끝점 포함)으로 제한합니다.

이 정책을 구성하면 WebRTC에서 사용할 수 있는 로컬 UDP 포트의 범위를 지정할 수 있습니다.

이 정책을 구성하지 않거나 빈 문자열 또는 잘못된 포트 범위로 설정하면 WebRTC는 사용 가능한 모든 로컬 UDP 포트를 사용할 수 있습니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 문자열

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: WebRtcUdpPortRange
  - GP 이름: WebRTC에서 사용하는 로컬 UDP 포트 범위 제한
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: WebRtcUdpPortRange
  - 값 형식: REG_SZ
  ##### 예제 값:
```
"10000-11999"
```


  #### Mac 정보 및 설정
  - 기본 설정 키 이름: WebRtcUdpPortRange
  - 예제 값:
``` xml
<string>10000-11999</string>
```
  

  [맨 위로 이동](#microsoft-edge---정책)

  ### WinHttpProxyResolverEnabled
  #### Windows 프록시 해결 프로그램 사용 (사용되지 않음)
  >사용되지 않음: 이 정책은 더 이상 사용되지 않습니다. 현재 지원되고 있으나 향후 릴리스에서는 사용되지 않을 예정입니다.
  
  #### 지원되는 버전:
  - Windows 84 이상부터

  #### 설명
  이 정책은 더 이상 사용되지 않고 이후 릴리스에서 유사한 기능으로 대체됩니다. https://crbug.com/1032820를 참조하세요.

   Windows를 사용하여 Microsoft Edge에 기본 제공되는 프록시 확인자 대신 모든 브라우저 네트워킹용 프록시를 확인합니다. Windows 프록시 확인자는 DirectAccess/NRPT와 같은 Windows 프록시 기능을 사용할 수 있습니다.

이 정책은 https://crbug.com/644030에 설명된 문제와 함께 제공되며 [ProxyPacUrl](#proxypacurl) 정책을 통해 설정된 PAC 파일을 포함하여 Windows 코드를 통해 PAC 파일을 가져와서 실행되도록 합니다. PAC 파일에 대한 네트워크 페치는 Microsoft Edge 코드 대신 Windows를 통해 발생하기 때문에 [DnsOverHttpsMode](#dnsoverhttpsmode)와(과) 같은 네트워크 정책은 PAC 파일에 대한 네트워크 페치에 적용되지 않습니다.

  이 정책을 사용하도록 설정하면 Windows 프록시 확인자가 사용됩니다.

  이 정책을 사용하지 않도록 설정하거나 구성하지 않으면 Microsoft Edge 프록시 확인자가 사용됩니다.

  #### 지원되는 기능:
  - 필수일 수 있음: 예
  - 권장될 수 있음: 아니요
  - 동적 정책 새로 고침: 아니요 - 브라우저 다시 시작 필요

  #### 데이터 형식:
  - 부울

  #### Windows 정보 및 설정
  ##### 그룹 정책(ADMX) 정보
  - GP 고유 이름: WinHttpProxyResolverEnabled
  - GP 이름: Windows 프록시 해결 프로그램 사용 (사용되지 않음)
  - GP 경로 (필수): 관리 템플릿/Microsoft Edge/
  - GP 경로 (맞춤): 해당 없음
  - GP ADMX 파일 이름: MSEdge.admx
  ##### Windows 레지스트리 설정
  - 경로 (필수): SOFTWARE\Policies\Microsoft\Edge
  - 경로 (맞춤): 해당 없음
  - 값 이름: WinHttpProxyResolverEnabled
  - 값 형식: REG_DWORD
  ##### 예제 값:
```
0x00000001
```


  

  [맨 위로 이동](#microsoft-edge---정책)


## 참고 항목
- [Microsoft Edge를 구성하는 중](configure-microsoft-edge.md)
- [Microsoft Edge 엔터프라이즈 방문 페이지](https://aka.ms/EdgeEnterprise)
- [Microsoft 보안 기준 블로그](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)