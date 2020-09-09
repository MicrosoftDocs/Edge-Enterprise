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

# Microsoft Edge - ポリシー
最新バージョンの Microsoft Edge には、次のポリシーが含まれます。これらのポリシーを使用して、組織内での Microsoft Edge の実行方法を構成することができます。

Microsoft Edge を更新する方法と時期を制御するために使用する追加ポリシーのセットについては、[Microsoft Edge 更新ポリシーのリファレンス](microsoft-edge-update-policies.md) を参照してください。

Microsoft Edge の推奨されるセキュリティ構成基準設定の [Microsoft Security コンプライアンス ツールキット](https://www.microsoft.com/download/details.aspx?id=55319) をダウンロードできます。詳細については、[Microsoft Security ベースライン ブログ](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines) を参照してください。

> [!注意]
> この記事は、Microsoft Edge バージョン 77 以降に適用されます。

## 利用可能なポリシー
次の表に、このリリースの Microsoft Edge で利用できるブラウザー関連のグループポリシーの一覧を示します。表のリンクを使用して、特定のポリシーに関する詳細を表示します。

|||
|-|-|
|[Application Guard の設定](#application-guard-の設定)|[Cast](#cast)|
|[HTTP 認証](#http-認証)|[SmartScreen の設定](#smartscreen-の設定)|
|[コンテンツの設定](#コンテンツの設定)|[スタートアップ、ホーム ページ、新しいタブ ページ](#スタートアップ、ホーム-ページ、新しいタブ-ページ)|
|[ネイティブ メッセージング](#ネイティブ-メッセージング)|[パスワード マネージャーと保護](#パスワード-マネージャーと保護)|
|[プロキシ サーバー](#プロキシ-サーバー)|[印刷](#印刷)|
|[拡張機能](#拡張機能)|[既定の検索プロバイダー](#既定の検索プロバイダー)|
|[Additional](#additional)|

### [*Application Guard の設定*](#application-guard-の設定-policies)
|ポリシー名|キャプション|
|-|-|
|[ApplicationGuardContainerProxy](#applicationguardcontainerproxy)|Application Guard コンテナー プロキシ|
### [*Cast*](#cast-policies)
|ポリシー名|キャプション|
|-|-|
|[EnableMediaRouter](#enablemediarouter)|Google Cast を有効にする|
|[ShowCastIconInToolbar](#showcasticonintoolbar)|ツール バーにキャスト アイコンを表示する|
### [*HTTP 認証*](#http-認証-policies)
|ポリシー名|キャプション|
|-|-|
|[AllowCrossOriginAuthPrompt](#allowcrossoriginauthprompt)|クロスオリジンでの HTTP 基本認証プロンプトを許可する|
|[AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)|Microsoft Edge がユーザー資格情報を委任できるサーバーのリストを指定する|
|[AuthSchemes](#authschemes)|サポートされている認証スキーム|
|[AuthServerAllowlist](#authserverallowlist)|許可されている認証サーバーのリストを構成する|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|Kerberos 認証をネゴシエートするときに CNAME 検索を無効にする|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|Kerberos SPN に非標準ポートを含める|
|[NtlmV2Enabled](#ntlmv2enabled)|NTLMv2 認証を有効にするかどうかを制御する|
### [*SmartScreen の設定*](#smartscreen-の設定-policies)
|ポリシー名|キャプション|
|-|-|
|[PreventSmartScreenPromptOverride](#preventsmartscreenpromptoverride)|サイトに関する Microsoft Defender SmartScreen プロンプトをバイパスしない|
|[PreventSmartScreenPromptOverrideForFiles](#preventsmartscreenpromptoverrideforfiles)|ダウンロードに関する Microsoft Defende SmartScreen の警告をバイパスしない|
|[SmartScreenAllowListDomains](#smartscreenallowlistdomains)|Microsoft Defender SmartScreen が警告をトリガーしないドメインのリストを構成する|
|[SmartScreenEnabled](#smartscreenenabled)|Microsoft Defender SmartScreen を構成する|
|[SmartScreenForTrustedDownloadsEnabled](#smartscreenfortrusteddownloadsenabled)|信頼された発行元からダウンロードするときに、Microsoft Defender SmartScreen のチェックを強制的に行う|
|[SmartScreenPuaEnabled](#smartscreenpuaenabled)|望ましくない可能性のあるアプリをブロックするように Microsoft Defender SmartScreen を構成する|
### [*コンテンツの設定*](#コンテンツの設定-policies)
|ポリシー名|キャプション|
|-|-|
|[AutoSelectCertificateForUrls](#autoselectcertificateforurls)|該当のサイトでクライアント証明書を自動的に選択する|
|[CookiesAllowedForUrls](#cookiesallowedforurls)|特定のサイトで Cookie を許可する|
|[CookiesBlockedForUrls](#cookiesblockedforurls)|特定のサイトで Cookie をブロックする|
|[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)|特定の Web サイトからの Cookie を現在のセッションに制限する|
|[DefaultCookiesSetting](#defaultcookiessetting)|Cookie を構成する|
|[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)|読み取り用のファイル システム API の使用を制御します|
|[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)|書き込みのためのファイル システム API の使用を制御します|
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|位置情報の既定の設定|
|[DefaultImagesSetting](#defaultimagessetting)|画像の既定の設定|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|セキュリティで保護されていないコンテンツの例外の使用を制御する|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|JavaScript の既定の設定|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|通知の既定の設定|
|[DefaultPluginsSetting](#defaultpluginssetting)|Adobe Flash の既定の設定|
|[DefaultPopupsSetting](#defaultpopupssetting)|ポップアップ ウィンドウの既定の設定|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|Web Bluetooth API の使用を制御する|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|WebUSB API の使用を制御する|
|[FileSystemReadAskForUrls](#filesystemreadaskforurls)|これらのサイトでファイル システム API を使用した読み取りアクセスを許可する|
|[FileSystemReadBlockedForUrls](#filesystemreadblockedforurls)|これらのサイトのファイル システム API を使用して読み取りアクセスをブロックする|
|[FileSystemWriteAskForUrls](#filesystemwriteaskforurls)|これらのサイトのファイルとディレクトリへの書き込みアクセスを許可する|
|[FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls)|これらのサイトのファイルとディレクトリへの書き込みアクセスをブロックする|
|[ImagesAllowedForUrls](#imagesallowedforurls)|これらのサイトでの画像表示を許可する|
|[ImagesBlockedForUrls](#imagesblockedforurls)|特定のサイトで画像をブロックする|
|[InsecureContentAllowedForUrls](#insecurecontentallowedforurls)|指定されたサイトのセキュリティで保護されていないコンテンツを許可する|
|[InsecureContentBlockedForUrls](#insecurecontentblockedforurls)|指定したサイトで安全でないコンテンツをブロックする|
|[JavaScriptAllowedForUrls](#javascriptallowedforurls)|特定のサイトで JavaScript を許可する|
|[JavaScriptBlockedForUrls](#javascriptblockedforurls)|特定のサイトで JavaScript をブロックする|
|[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)|従来の SameSite Cookie の動作に関する設定を有効にする|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist)|指定されたサイトの Cookie について、従来の SameSite の動作に戻す|
|[NotificationsAllowedForUrls](#notificationsallowedforurls)|特定のサイトで通知を許可する|
|[NotificationsBlockedForUrls](#notificationsblockedforurls)|特定のサイトで通知をブロックする|
|[PluginsAllowedForUrls](#pluginsallowedforurls)|特定のサイトで Adobe Flash プラグインを許可する|
|[PluginsBlockedForUrls](#pluginsblockedforurls)|特定のサイトで Adobe Flash プラグインをブロックする|
|[PopupsAllowedForUrls](#popupsallowedforurls)|特定のサイトでのポップアップ ウィンドウを許可する|
|[PopupsBlockedForUrls](#popupsblockedforurls)|特定のサイトでポップアップ ウィンドウをブロックする|
|[RegisteredProtocolHandlers](#registeredprotocolhandlers)|プロトコル ハンドラーを登録する|
|[SpotlightExperiencesAndRecommendationsEnabled](#spotlightexperiencesandrecommendationsenabled)|ユーザーがカスタマイズされた背景画像とテキスト、提案、通知、
および Microsoft サービスのヒントを受け取ることができるかどうかを選択する|
|[WebUsbAllowDevicesForUrls](#webusballowdevicesforurls)|特定の USB デバイスに接続するために、特定のサイトへのアクセスを許可します|
|[WebUsbAskForUrls](#webusbaskforurls)|特定のサイトでの WebUSB を許可する|
|[WebUsbBlockedForUrls](#webusbblockedforurls)|特定のサイトでの WebUSB をブロックする|
### [*スタートアップ、ホーム ページ、新しいタブ ページ*](#スタートアップ、ホーム-ページ、新しいタブ-ページ-policies)
|ポリシー名|キャプション|
|-|-|
|[HomepageIsNewTabPage](#homepageisnewtabpage)|新しいタブ ページをホーム ページとして設定する|
|[HomepageLocation](#homepagelocation)|ホーム ページの URL を構成する|
|[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)|新しいタブページのレイアウトで使用できる背景の種類を構成する|
|[NewTabPageCompanyLogo](#newtabpagecompanylogo)|新しいタブ ページでの会社のロゴを設定する (現在不使用)|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|新しいタブ ページで既定のトップ サイトを非表示にする|
|[NewTabPageLocation](#newtabpagelocation)|新しいタブ ページの URL を構成する|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|新しいタブ ページのクイック リンクを設定する|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|新しいタブ ページのプリロードを有効にして、レンダリングを高速化する|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|Microsoft Edge の新しいタブ ページ エクスペリエンスを構成する|
|[RestoreOnStartup](#restoreonstartup)|スタートアップ時に実行するアクション|
|[RestoreOnStartupURLs](#restoreonstartupurls)|ブラウザーの起動時に開くサイト|
|[ShowHomeButton](#showhomebutton)|ツール バーに [ホーム] ボタンを表示する|
### [*ネイティブ メッセージング*](#ネイティブ-メッセージング-policies)
|ポリシー名|キャプション|
|-|-|
|[NativeMessagingAllowlist](#nativemessagingallowlist)|ユーザーが使用できるネイティブ メッセージング ホストを制御する|
|[NativeMessagingBlocklist](#nativemessagingblocklist)|ネイティブ メッセージングの禁止リストを構成する|
|[NativeMessagingUserLevelHosts](#nativemessaginguserlevelhosts)|ユーザー レベルのネイティブ メッセージング ホスト (管理者のアクセス許可なしでインストールされるホスト) を許可する|
### [*パスワード マネージャーと保護*](#パスワード-マネージャーと保護-policies)
|ポリシー名|キャプション|
|-|-|
|[PasswordManagerEnabled](#passwordmanagerenabled)|パスワード マネージャーへのパスワードの保存を有効にする|
|[PasswordMonitorAllowed](#passwordmonitorallowed)|パスワードが安全でないことが判明した場合に、ユーザーにアラートを表示する|
|[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)|パスワード変更 URL を構成する|
|[PasswordProtectionLoginURLs](#passwordprotectionloginurls)|パスワード保護サービスによってパスワードのソルト付きハッシュがキャプチャされるエンタープライズ ログイン URL のリストを構成します|
|[PasswordProtectionWarningTrigger](#passwordprotectionwarningtrigger)|パスワード保護の警告トリガーを構成する|
### [*プロキシ サーバー*](#プロキシ-サーバー-policies)
|ポリシー名|キャプション|
|-|-|
|[ProxyBypassList](#proxybypasslist)|プロキシバイパスの規則を構成する|
|[ProxyMode](#proxymode)|プロキシ サーバーの設定を構成する|
|[ProxyPacUrl](#proxypacurl)|プロキシ .pac ファイルの URL を設定する|
|[ProxyServer](#proxyserver)|プロキシ サーバーのアドレスまたは URL を構成する|
|[ProxySettings](#proxysettings)|プロキシの設定|
### [*印刷*](#印刷-policies)
|ポリシー名|キャプション|
|-|-|
|[DefaultPrinterSelection](#defaultprinterselection)|既定のプリンターの選択規則|
|[PrintHeaderFooter](#printheaderfooter)|ヘッダーとフッターを印刷する|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|システム既定のプリンターを通常使用するプリンターとして設定する|
|[PrintingEnabled](#printingenabled)|印刷を有効にする|
|[PrintingPaperSizeDefault](#printingpapersizedefault)|既定の印刷ページ サイズ|
|[UseSystemPrintDialog](#usesystemprintdialog)|システム印刷ダイアログを使用して印刷する|
### [*拡張機能*](#拡張機能-policies)
|ポリシー名|キャプション|
|-|-|
|[ExtensionAllowedTypes](#extensionallowedtypes)|許可される拡張機能の種類を構成する|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|特定の拡張機能のインストールを許可する|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|インストールできない拡張機能を制御する|
|[ExtensionInstallForcelist](#extensioninstallforcelist)|サイレント インストールされる拡張機能を制御する|
|[ExtensionInstallSources](#extensioninstallsources)|拡張機能およびユーザー スクリプトのインストール ソースを構成する|
|[ExtensionSettings](#extensionsettings)|拡張子の管理設定を構成する|
### [*既定の検索プロバイダー*](#既定の検索プロバイダー-policies)
|ポリシー名|キャプション|
|-|-|
|[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)|既定の検索プロバイダーを有効にする|
|[DefaultSearchProviderEncodings](#defaultsearchproviderencodings)|既定の検索プロバイダーのエンコード|
|[DefaultSearchProviderImageURL](#defaultsearchproviderimageurl)|既定の検索プロバイダーの画像検索を指定する|
|[DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams)|POST を使用する画像の URL のパラメーター|
|[DefaultSearchProviderKeyword](#defaultsearchproviderkeyword)|既定の検索プロバイダーのキーワード|
|[DefaultSearchProviderName](#defaultsearchprovidername)|既定の検索プロバイダーの名前|
|[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)|既定の検索プロバイダーの検索 URL|
|[DefaultSearchProviderSuggestURL](#defaultsearchprovidersuggesturl)|検索候補を使用するための既定の検索プロバイダーの URL|
|[NewTabPageSearchBox](#newtabpagesearchbox)|新しいタブページの検索ボックスエクスペリエンスを構成する|
### [*Additional*](#additional-policies)
|ポリシー名|キャプション|
|-|-|
|[AddressBarMicrosoftSearchInBingProviderEnabled](#addressbarmicrosoftsearchinbingproviderenabled)|アドレス バーの Bing 候補で Microsoft Search を有効にする|
|[AdsSettingForIntrusiveAdsSites](#adssettingforintrusiveadssites)|押し付けがましい広告を表示するサイトに対する広告の設定|
|[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory)|ブラウザーとダウンロードの履歴の削除を有効にする|
|[AllowFileSelectionDialogs](#allowfileselectiondialogs)|ファイルの選択ダイアログを許可する|
|[AllowPopupsDuringPageUnload](#allowpopupsduringpageunload)|ページのアンロード中にポップアップの表示を許可する|
|[AllowSurfGame](#allowsurfgame)|サーフィン ゲームを許可する|
|[AllowSyncXHRInPageDismissal](#allowsyncxhrinpagedismissal)|ページを閉じるときにページで同期 XHR 要求を送信することを許可する (非推奨)|
|[AllowTokenBindingForUrls](#allowtokenbindingforurls)|Microsoft Edge によってトークンのバインドの確立が試行されるサイトの一覧を構成します。|
|[AllowTrackingForUrls](#allowtrackingforurls)|特定のサイトの追跡防止の例外を構成する|
|[AlternateErrorPagesEnabled](#alternateerrorpagesenabled)|Web ページが見つからない場合に類似したページを提示する|
|[AlwaysOpenPdfExternally](#alwaysopenpdfexternally)|PDF ファイルを常に外部で開く|
|[AmbientAuthenticationInPrivateModesEnabled](#ambientauthenticationinprivatemodesenabled)|InPrivate プロファイルとゲスト プロファイルに対してアンビエント認証を有効にする|
|[AppCacheForceEnabled](#appcacheforceenabled)|既定でオフになっている場合でも、AppCache 機能を再度有効にすることができます|
|[ApplicationLocaleValue](#applicationlocalevalue)|アプリケーションのロケールを設定する|
|[AudioCaptureAllowed](#audiocaptureallowed)|オーディオ キャプチャを許可または禁止する|
|[AudioCaptureAllowedUrls](#audiocaptureallowedurls)|アクセス許可を要求しなくてもオーディオ キャプチャ デバイスにアクセスできるサイト|
|[AudioSandboxEnabled](#audiosandboxenabled)|オーディオ サンドボックスの実行を許可する|
|[AutoImportAtFirstRun](#autoimportatfirstrun)|初回実行時に別のブラウザーのデータと設定を自動的にインポートする|
|[AutoLaunchProtocolsFromOrigins](#autolaunchprotocolsfromorigins)|ユーザーにメッセージを表示せずに、一覧表示された元の場所から外部アプリケーションを起動できるプロトコルの一覧を定義します。|
|[AutoOpenAllowedForURLs](#autoopenallowedforurls)|AutoOpenFileTypes を適用できる URL|
|[AutoOpenFileTypes](#autoopenfiletypes)|ダウンロード時に自動的に開く必要があるファイルの種類のリスト|
|[AutofillAddressEnabled](#autofilladdressenabled)|アドレスのオートフィルを有効にする|
|[AutofillCreditCardEnabled](#autofillcreditcardenabled)|クレジット カード情報についてオートフィルを有効にする|
|[AutoplayAllowed](#autoplayallowed)|Web サイトでのメディアの自動再生を許可する|
|[BackgroundModeEnabled](#backgroundmodeenabled)|Microsoft Edge が終了してもバックグラウンド アプリの実行を続行する|
|[BackgroundTemplateListUpdatesEnabled](#backgroundtemplatelistupdatesenabled)|テンプレートを使用するコレクションや他の機能で利用できるテンプレートの一覧について、バックグラウンドでの更新を有効にする|
|[BingAdsSuppression](#bingadssuppression)|Bing の検索結果のすべての広告をブロックする|
|[BlockThirdPartyCookies](#blockthirdpartycookies)|サードパーティの Cookie をブロックする|
|[BrowserAddProfileEnabled](#browseraddprofileenabled)|ID ポップアップ メニューまたは [設定] ページでのプロファイル作成を有効にする|
|[BrowserGuestModeEnabled](#browserguestmodeenabled)|ゲスト モードを有効にする|
|[BrowserNetworkTimeQueriesEnabled](#browsernetworktimequeriesenabled)|ブラウザー ネットワーク タイム サービスへのクエリを許可する|
|[BrowserSignin](#browsersignin)|ブラウザー サインインの設定|
|[BuiltInDnsClientEnabled](#builtindnsclientenabled)|組み込みの DNS クライアントを使用する|
|[BuiltinCertificateVerifierEnabled](#builtincertificateverifierenabled)|組み込みの証明書検証ツールを使用してサーバー証明書を検証するかどうかを決定します (非推奨)|
|[CertificateTransparencyEnforcementDisabledForCas](#certificatetransparencyenforcementdisabledforcas)|subjectPublicKeyInfo ハッシュのリストに対する証明書の透明性の適用を無効にする|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](#certificatetransparencyenforcementdisabledforlegacycas)|レガシ証明機関のリストに対する証明書の透明性の適用を無効にする|
|[CertificateTransparencyEnforcementDisabledForUrls](#certificatetransparencyenforcementdisabledforurls)|特定の URL に対する証明書の透明性の適用を無効にする|
|[ClearBrowsingDataOnExit](#clearbrowsingdataonexit)|Microsoft Edge を閉じるときに閲覧データを消去する|
|[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)|Microsoft Edge を閉じるときに、キャッシュされた画像とファイルを消去する|
|[ClickOnceEnabled](#clickonceenabled)|ユーザーが ClickOnce プロトコルを使用してファイルを開くことを許可する|
|[CollectionsServicesAndExportsBlockList](#collectionsservicesandexportsblocklist)|コレクション内の指定されたサービス リストとエクスポート対象へのアクセスをブロック|
|[CommandLineFlagSecurityWarningsEnabled](#commandlineflagsecuritywarningsenabled)|コマンドライン フラグのセキュリティ警告を有効にする|
|[ComponentUpdatesEnabled](#componentupdatesenabled)|Microsoft Edge でのコンポーネントの更新を有効にする|
|[ConfigureDoNotTrack](#configuredonottrack)|トラッキング拒否を構成する|
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|Azure AD ドメイン アカウントがない場合の Active Directory ドメイン アカウントによる自動サインインを構成する|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|オンライン音声合成を構成する|
|[ConfigureShare](#configureshare)|共有エクスペリエンスを構成する|
|[CustomHelpLink](#customhelplink)|カスタム ヘルプのリンクを指定する|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|DNS 傍受チェックが有効になっている|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|Microsoft Edge を既定のブラウザーとして設定する|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|既定の検索プロバイダーのコンテキストメニュー検索アクセスを許可する|
|[DefaultSensorsSetting](#defaultsensorssetting)|既定のセンサーの設定|
|[DefaultSerialGuardSetting](#defaultserialguardsetting)|Serial API の使用を制御する|
|[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)|タブ ナビゲーションの前にエンタープライズ モード サイト一覧が利用可能である必要がある|
|[DeleteDataOnMigration](#deletedataonmigration)|移行時に古いブラウザー データを削除する|
|[DeveloperToolsAvailability](#developertoolsavailability)|開発者ツールを使用できる状況を制御する|
|[DiagnosticData](#diagnosticdata)|ブラウザー使用状況に関する必要な診断データとオプションの診断データを送信する|
|[DirectInvokeEnabled](#directinvokeenabled)|ユーザーが DirectInvoke プロトコルを使用してファイルを開くことを許可する|
|[Disable3DAPIs](#disable3dapis)|3D グラフィックス API のサポートを無効にする|
|[DisableScreenshots](#disablescreenshots)|スクリーンショットの撮影を無効にする|
|[DiskCacheDir](#diskcachedir)|ディスク キャッシュ ディレクトリを設定する|
|[DiskCacheSize](#diskcachesize)|ディスク キャッシュ サイズをバイト単位で設定する|
|[DnsOverHttpsMode](#dnsoverhttpsmode)|DNS-over-HTTPS モードを制御|
|[DnsOverHttpsTemplates](#dnsoverhttpstemplates)|目的の DNS-over-HTTPS リゾルバーの URI テンプレートを指定します|
|[DownloadDirectory](#downloaddirectory)|ディレクトリをダウンロードする|
|[DownloadRestrictions](#downloadrestrictions)|ダウンロードの制限を許可する|
|[EdgeCollectionsEnabled](#edgecollectionsenabled)|コレクション機能を有効にする|
|[EditFavoritesEnabled](#editfavoritesenabled)|ユーザーによるお気に入りの編集を許可する|
|[EnableDeprecatedWebPlatformFeatures](#enabledeprecatedwebplatformfeatures)|制限された期間、非推奨の Web プラットフォーム機能を再度有効にする|
|[EnableDomainActionsDownload](#enabledomainactionsdownload)|マイクロソフトからのドメイン アクションのダウンロードを有効にする (現在不使用)|
|[EnableOnlineRevocationChecks](#enableonlinerevocationchecks)|オンライン OCSP/CRL チェックを有効にする|
|[EnableSha1ForLocalAnchors](#enablesha1forlocalanchors)|ローカルトラストアンカーによって発行された場合に、SHA-1 を使用して署名された証明書を許可する (非推奨)|
|[EnterpriseHardwarePlatformAPIEnabled](#enterprisehardwareplatformapienabled)|管理された拡張機能を有効にして、エンタープライズ ハードウェア プラットフォーム API を使用する|
|[EnterpriseModeSiteListManagerAllowed](#enterprisemodesitelistmanagerallowed)|Enterprise Mode Site List Manager ツールへのアクセスを許可する|
|[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](#exemptdomainfiletypepairsfromfiletypedownloadwarnings)|ドメインにおける指定されたファイルの種類に対して、ファイルの種類の拡張子に基づくダウンロードの警告を無効にする|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|実験および構成サービスとの通信を制御する|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox)|外部プロトコルのダイアログで [常に開く] チェック ボックスを表示する|
|[FamilySafetySettingsEnabled](#familysafetysettingsenabled)|ユーザーが Family Safety を構成することを許可する|
|[FavoritesBarEnabled](#favoritesbarenabled)|お気に入りバーを有効にする|
|[ForceBingSafeSearch](#forcebingsafesearch)|Bing セーフサーチを適用する|
|[ForceCertificatePromptsOnMultipleMatches](#forcecertificatepromptsonmultiplematches)|"AutoSelectCertificateForUrls" で構成されたサイトに複数の証明書が一致する場合、Microsoft Edge で証明書を自動的に選択するかどうかを構成します。|
|[ForceEphemeralProfiles](#forceephemeralprofiles)|一時プロファイルの使用を有効にする|
|[ForceGoogleSafeSearch](#forcegooglesafesearch)|Google セーフサーチを適用する|
|[ForceLegacyDefaultReferrerPolicy](#forcelegacydefaultreferrerpolicy)|no-referrer-when-downgrade の既定の参照ポリシーを使用 (非推奨)|
|[ForceNetworkInProcess](#forcenetworkinprocess)|ブラウザー プロセスでネットワーク コードを強制的に実行する (現在不使用)|
|[ForceSync](#forcesync)|ブラウザー データの同期を強制し、同期の同意プロンプトを表示しない|
|[ForceYouTubeRestrict](#forceyoutuberestrict)|最小限の YouTube の制限モードを強制する|
|[FullscreenAllowed](#fullscreenallowed)|全画面表示モードを許可する|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|グローバルにスコープが設定された HTTP 認証キャッシュを有効にする|
|[GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar)|アドレス バーへの 1 単語の入力で検索するのではなく、ダイレクト イントラネット サイト ナビゲーションを強制します|
|[HSTSPolicyBypassList](#hstspolicybypasslist)|HSTS ポリシー チェックをバイパスする名前の一覧を構成します|
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|使用可能な場合はハードウェア アクセラレータを使用する|
|[HideFirstRunExperience](#hidefirstrunexperience)|最初の実行エクスペリエンスとスプラッシュ スクリーンを非表示にする|
|[ImportAutofillFormData](#importautofillformdata)|オートフィルのフォーム データのインポートを許可する|
|[ImportBrowserSettings](#importbrowsersettings)|ブラウザーの設定のインポートを許可する|
|[ImportCookies](#importcookies)|Cookie のインポートを許可する|
|[ImportExtensions](#importextensions)|拡張機能のインポートを許可する|
|[ImportFavorites](#importfavorites)|お気に入りのインポートを許可する|
|[ImportHistory](#importhistory)|閲覧の履歴のインポートを許可する|
|[ImportHomepage](#importhomepage)|ホーム ページの設定のインポートを許可する|
|[ImportOpenTabs](#importopentabs)|開いているタブのインポートを許可する|
|[ImportPaymentInfo](#importpaymentinfo)|支払情報のインポートを許可する|
|[ImportSavedPasswords](#importsavedpasswords)|保存したパスワードのインポートを許可する|
|[ImportSearchEngine](#importsearchengine)|検索エンジンの設定のインポートを許可する|
|[ImportShortcuts](#importshortcuts)|ショートカットのインポートを許可する|
|[InPrivateModeAvailability](#inprivatemodeavailability)|InPrivate モードが利用できるかどうかを構成する|
|[InsecureFormsWarningsEnabled](#insecureformswarningsenabled)|セキュリティで保護されていないフォームの警告を有効にする|
|[IntensiveWakeUpThrottlingEnabled](#intensivewakeupthrottlingenabled)|IntensiveWakeUpThrottling 機能を制御する|
|[InternetExplorerIntegrationEnhancedHangDetection](#internetexplorerintegrationenhancedhangdetection)|Internet Explorer モードの拡張ハング検出を構成|
|[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)|Internet Explorer 統合を構成する|
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|エンタープライズ モード サイト一覧を構成する|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|Internet Explorer モードのページから開始した場合、未構成のサイトへの "ページ内" ナビゲーションがどのように動作するかを指定する|
|[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed)|Internet Explorer モードのテストを許可|
|[IsolateOrigins](#isolateorigins)|特定の出所に対してサイトの分離を有効にする|
|[LocalProvidersEnabled](#localprovidersenabled)|ローカル プロバイダーからの提案を許可|
|[ManagedFavorites](#managedfavorites)|お気に入りを構成する|
|[ManagedSearchEngines](#managedsearchengines)|検索エンジンの管理|
|[MaxConnectionsPerProxy](#maxconnectionsperproxy)|プロキシ サーバーへの同時実行の最大接続数|
|[MediaRouterCastAllowAllIPs](#mediaroutercastallowallips)|すべての IP アドレスで Cast デバイスに接続することを Google Cast に許可する|
|[MetricsReportingEnabled](#metricsreportingenabled)|使用状況とクラッシュに関するデータのレポート送信を有効にする (非推奨)|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|ネイティブウィンドウオクルージョンを有効にする|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|エンタープライズ モード サイト一覧のタブ ナビゲーションの遅延時間を設定する|
|[NetworkPredictionOptions](#networkpredictionoptions)|ネットワーク予測を有効にする|
|[NonRemovableProfileEnabled](#nonremovableprofileenabled)|職場または学校アカウントで自動的にサインインする既定のプロファイルを、ユーザーが常に持つ必要があるかどうかを構成する|
|[OverrideSecurityRestrictionsOnInsecureOrigin](#overridesecurityrestrictionsoninsecureorigin)|保護されていないオリジンに対するセキュリティ制限を適用する状況を制御する|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|Web サイトでの利用可能な支払い方法の照会を許可する|
|[PersonalizationReportingEnabled](#personalizationreportingenabled)|閲覧の履歴を Microsoft に送信して、広告、検索、ニュースの個人用設定を許可する|
|[PinningWizardAllowed](#pinningwizardallowed)|[タスク バー ウィザードにピン留めする] を許可する|
|[ProactiveAuthEnabled](#proactiveauthenabled)|事前認証を有効にする|
|[PromotionalTabsEnabled](#promotionaltabsenabled)|タブ全体にプロモーション コンテンツを表示できるようにする|
|[PromptForDownloadLocation](#promptfordownloadlocation)|ダウンロードしたファイルの保存場所を確認する|
|[QuicAllowed](#quicallowed)|QUIC プロトコルを許可する|
|[RelaunchNotification](#relaunchnotification)|ブラウザーの再起動が推奨されるか、または必須であることをユーザーに通知する|
|[RelaunchNotificationPeriod](#relaunchnotificationperiod)|更新通知の期間を設定する|
|[RendererCodeIntegrityEnabled](#renderercodeintegrityenabled)|レンダラー コードの整合性を有効にする|
|[RequireOnlineRevocationChecksForLocalAnchors](#requireonlinerevocationchecksforlocalanchors)|トラスト アンカーに対してオンライン OCSP/CRL チェックが必要であるかどうかを指定する|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|Web サービスを使用してナビゲーション エラーを解決できるようにする|
|[RestrictSigninToPattern](#restrictsignintopattern)|Microsoft Edge プライマリ アカウントとして使用できるアカウントを制限する|
|[RoamingProfileLocation](#roamingprofilelocation)|移動プロファイルのディレクトリを設定する|
|[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)|Microsoft Edge プロファイル データに対してローミング コピーの使用を有効にする|
|[RunAllFlashInAllowMode](#runallflashinallowmode)|Adobe Flash コンテンツの設定をすべてのコンテンツに拡張する|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|ユーザーが HTTPS 警告ページから先に進むことを許可する|
|[SSLVersionMin](#sslversionmin)|有効な TLS バージョンを最小限に抑える|
|[SaveCookiesOnExit](#savecookiesonexit)|Microsoft Edge 閉じたときに Cookie を保存|
|[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)|ブラウザーの履歴の保存を無効にする|
|[ScreenCaptureAllowed](#screencaptureallowed)|スクリーンショットを許可または拒否します|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|URL フラグメントで指定されたテキストへのスクロールを有効にする|
|[SearchSuggestEnabled](#searchsuggestenabled)|検索候補を有効にする|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|直接セキュリティ キー構成証明を使用するためのアクセス許可を必要としない Web サイトまたはドメイン|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|すべてのイントラネット サイトを Internet Explorer に送る|
|[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)|Microsoft サービスを改善するためにサイト情報を送信する (非推奨)|
|[SensorsAllowedForUrls](#sensorsallowedforurls)|特定のサイトのセンサーへのアクセスを許可|
|[SensorsBlockedForUrls](#sensorsblockedforurls)|特定のサイトのセンサーへのアクセスをブロック|
|[SerialAskForUrls](#serialaskforurls)|特定のサイトでシリアル API を許可する|
|[SerialBlockedForUrls](#serialblockedforurls)|特定のサイトでシリアル API をブロックする|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|Microsoft Office のショートカットをお気に入りバーに表示する|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|Signed HTTP Exchange (SXG) のサポートを有効にする|
|[SitePerProcess](#siteperprocess)|すべてのサイトでサイト分離を有効にする|
|[SpellcheckEnabled](#spellcheckenabled)|スペルチェックを有効にする|
|[SpellcheckLanguage](#spellchecklanguage)|特定のスペルチェック言語を有効にする|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|スペルチェック言語を強制的に無効にする|
|[StricterMixedContentTreatmentEnabled](#strictermixedcontenttreatmentenabled)|混合コンテンツの厳密な処理を有効にする (非推奨)|
|[SuppressUnsupportedOSWarning](#suppressunsupportedoswarning)|サポートされていない OS の警告を表示しない|
|[SyncDisabled](#syncdisabled)|Microsoft 同期サービスを使用しているデータの同期を無効にする|
|[SyncTypesListDisabled](#synctypeslistdisabled)|同期から除外される種類のリストを構成する|
|[TLS13HardeningForLocalAnchorsEnabled](#tls13hardeningforlocalanchorsenabled)|ローカル トラスト アンカーで TLS 1.3 セキュリティ機能を有効にします。 (現在不使用)|
|[TLSCipherSuiteDenyList](#tlsciphersuitedenylist)|無効にする TLS 暗号スイートを指定|
|[TabFreezingEnabled](#tabfreezingenabled)|バックグラウンド タブの固定を許可する|
|[TaskManagerEndProcessEnabled](#taskmanagerendprocessenabled)|ブラウザーのタスク マネージャーでプロセスの終了を有効にする|
|[TotalMemoryLimitMb](#totalmemorylimitmb)|1 つの Microsoft Edge インスタンスで使用できるメモリの上限を MB 単位で設定します。|
|[TrackingPrevention](#trackingprevention)|ユーザーの Web 閲覧アクティビティの追跡をブロックする|
|[TranslateEnabled](#translateenabled)|翻訳を有効にする|
|[URLAllowlist](#urlallowlist)|許可されている URL のリストを定義する|
|[URLBlocklist](#urlblocklist)|URL のリストへのアクセスをブロックする|
|[UserAgentClientHintsEnabled](#useragentclienthintsenabled)|User-Agent Client Hints 機能を有効にする (非推奨)|
|[UserDataDir](#userdatadir)|ユーザー データ ディレクトリを設定する|
|[UserDataSnapshotRetentionLimit](#userdatasnapshotretentionlimit)|緊急ロールバックの場合に使用するために保持されるユーザー データ スナップショットの数を制限|
|[UserFeedbackAllowed](#userfeedbackallowed)|ユーザー フィードバックを許可する|
|[VideoCaptureAllowed](#videocaptureallowed)|ビデオ キャプチャを許可または禁止する|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|アクセス許可を要求しなくてもビデオ キャプチャ デバイスにアクセスできるサイト|
|[WPADQuickCheckEnabled](#wpadquickcheckenabled)|WPAD 最適化を設定する|
|[WebAppInstallForceList](#webappinstallforcelist)|強制的にインストールされる Web アプリのリストを構成する|
|[WebComponentsV0Enabled](#webcomponentsv0enabled)|M84 まで、Web Components v0 API を再度有効にする (現在不使用)|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|互換性のないポリシーのオーバーライドを WebDriver に許可する (現在不使用)|
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|WebRTC によるローカル IP アドレスの公開を管理する|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|WebRTC によるローカル IP アドレスの公開を制限する|
|[WebRtcUdpPortRange](#webrtcudpportrange)|WebRTC で使用されるローカル UDP ポートの範囲を制限する|
|[WinHttpProxyResolverEnabled](#winhttpproxyresolverenabled)|Windows プロキシ リゾルバーを使用 (非推奨)|




  ## Application Guard の設定 policies

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ApplicationGuardContainerProxy
  #### Application Guard コンテナー プロキシ
  
  
  #### サポートされているバージョン:
  - Windows 以降の 84

  #### 説明
  Microsoft Edge Application Guard のプロキシ設定を構成します。
 このポリシーを有効にすると、Microsoft Edge Application Guard はプロキシ構成のその他のソースを無視します。

 このポリシーを構成しない場合、Microsoft Edge Application Guard はホストのプロキシ構成を使用します。

 このポリシーは、(ホスト上の) Application Guard の外にある Microsoft Edge のプロキシ構成には影響しません。

ProxyMode フィールドを使用して Microsoft Edge Application Guard が使用するプロキシ サーバーを指定できます。

ProxyPacUrl フィールドはプロキシ .pac ファイルの URL です。

ProxyServer フィールドはプロキシ サーバーの URL です。

「direct」値を「ProxyMode」として選択すると、他のすべてのフィールドが無視されます。

「auto_detect」値を「ProxyMode」として選択すると、他のすべてのフィールドが無視されます。

「fixed_servers」値を「ProxyMode」として選択すると、「ProxyServer」フィールドが使用されます。

「pac_script」値を「ProxyMode」として選択すると、「ProxyPacUrl」フィールドが使用されます。

 デュアル プロキシを介した Application Guard トラフィックの識別の詳細については、[https://go.microsoft.com/fwlink/?linkid=2134653](https://go.microsoft.com/fwlink/?linkid=2134653) にアクセスしてください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 辞書

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ApplicationGuardContainerProxy
  - GP の名前: Application Guard コンテナー プロキシ
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/Application Guard の設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ApplicationGuardContainerProxy
  - 値の種類: REG_SZ
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ## Cast policies

  [トップに戻る](#microsoft-edge---ポリシー)

  ### EnableMediaRouter
  #### Google Cast を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  このポリシーを有効にした場合、Google Cast が有効になります。ユーザーは、アプリ メニュー、ページのコンテキスト メニュー、Cast 対応 Web サイトのメディア コントロール、および Cast ツール バー アイコン (表示されている場合) から、Google Cast を起動できます。

このポリシーを無効にした場合、Google Cast は無効になります。

既定では、Google Cast は有効になっています。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: EnableMediaRouter
  - GP の名前: Google Cast を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/Cast
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: EnableMediaRouter
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: EnableMediaRouter
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ShowCastIconInToolbar
  #### ツール バーにキャスト アイコンを表示する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  このポリシーを true に設定すると、ツール バーまたはオーバーフロー メニューに Cast ツール バー アイコンが表示されます。ユーザーはこのアイコンを削除できません。

このポリシーを構成しなかった場合または無効にした場合、ユーザーは、コンテキスト メニューを使ってこのアイコンをピン留めしたり、削除したりすることができます。

[EnableMediaRouter](#enablemediarouter) ポリシーも false に設定されている場合、このポリシーは無視され、ツール バー アイコンは表示されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ShowCastIconInToolbar
  - GP の名前: ツール バーにキャスト アイコンを表示する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/Cast
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ShowCastIconInToolbar
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ShowCastIconInToolbar
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ## HTTP 認証 policies

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AllowCrossOriginAuthPrompt
  #### クロスオリジンでの HTTP 基本認証プロンプトを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ページ上にあるサード パーティのサブコンテンツで [HTTP 基本認証] ダイアログ ボックスを開くことができるかどうかを制御します。

通常、これはフィッシング詐欺の防衛策として無効になっています。このポリシーを構成しなかった場合、ポリシーは無効になり、サード パーティのサブコンテンツで [HTTP 基本認証] ダイアログ ボックスを開くことはできません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AllowCrossOriginAuthPrompt
  - GP の名前: クロスオリジンでの HTTP 基本認証プロンプトを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/HTTP 認証
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AllowCrossOriginAuthPrompt
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AllowCrossOriginAuthPrompt
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AuthNegotiateDelegateAllowlist
  #### Microsoft Edge がユーザー資格情報を委任できるサーバーのリストを指定する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge が委任できるサーバーのリストを構成します。

複数のサーバー名を入力するときはコンマで区切ります。ワイルドカード（*）を使用できます。

このポリシーを構成しなかった場合、サーバーがイントラネット上で検出されても、Microsoft Edge はユーザー資格情報を委任しません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AuthNegotiateDelegateAllowlist
  - GP の名前: Microsoft Edge がユーザー資格情報を委任できるサーバーのリストを指定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/HTTP 認証
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AuthNegotiateDelegateAllowlist
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"contoso.com"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AuthNegotiateDelegateAllowlist
  - サンプル値:
``` xml
<string>contoso.com</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AuthSchemes
  #### サポートされている認証スキーム
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  サポートされる HTTP 認証スキームを指定します。

このポリシーは、'basic'、'digest'、'ntlm'、'negotiate' の各値を使用して構成できます。値が複数ある場合はコンマで区切ります。

このポリシーを構成しなかった場合、4 つのスキームすべてが使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AuthSchemes
  - GP の名前: サポートされている認証スキーム
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/HTTP 認証
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AuthSchemes
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"basic,digest,ntlm,negotiate"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AuthSchemes
  - サンプル値:
``` xml
<string>basic,digest,ntlm,negotiate</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AuthServerAllowlist
  #### 許可されている認証サーバーのリストを構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  統合認証を有効にするサーバーを指定します。統合認証が有効になるのはMicrosoft Edge がこのリストに含まれているプロキシやサーバーから認証チャレンジを受信した場合のみです。

サーバー名を複数指定する場合はコンマで区切ります。ワイルドカード (*) を使用できます。

このポリシーを構成しなかった場合、Microsoft Edge はサーバーがイントラネット上にあるかどうかの検出を試行し、検出された場合にのみ、IWA 要求に応答します。サーバーがインターネット上にある場合は、そのサーバーからの IWA 要求は Microsoft Edge では無視されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AuthServerAllowlist
  - GP の名前: 許可されている認証サーバーのリストを構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/HTTP 認証
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AuthServerAllowlist
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"*contoso.com,contoso.com"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AuthServerAllowlist
  - サンプル値:
``` xml
<string>*contoso.com,contoso.com</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DisableAuthNegotiateCnameLookup
  #### Kerberos 認証をネゴシエートするときに CNAME 検索を無効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  正規の DNS 名 (CNAME) または入力された元の名前のどちらを基準にして Kerberos SPN を生成するかを決定します。

このポリシーを有効にした場合、CNAME 検索がスキップされ、入力したサーバー名がそのまま使用されます。

このポリシーを無効にした場合または構成しなかった場合、サーバーの正規名が使用されます。このサーバーの正規名は CNAME 検索によって決まります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DisableAuthNegotiateCnameLookup
  - GP の名前: Kerberos 認証をネゴシエートするときに CNAME 検索を無効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/HTTP 認証
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DisableAuthNegotiateCnameLookup
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DisableAuthNegotiateCnameLookup
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### EnableAuthNegotiatePort
  #### Kerberos SPN に非標準ポートを含める
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  生成された Kerberos SPN に非標準ポートを含めるかどうかを指定します。

このポリシーを有効にした場合、ユーザーが非標準ポート (80 と 443 以外のポート) を URL に含めると、生成された Kerberos SPN にそのポートが含まれます。

このポリシーを構成しなかった場合または無効にした場合は、どのような状況でも、生成された Kerberos SPN にはポートは含まれません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: EnableAuthNegotiatePort
  - GP の名前: Kerberos SPN に非標準ポートを含める
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/HTTP 認証
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: EnableAuthNegotiatePort
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: EnableAuthNegotiatePort
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NtlmV2Enabled
  #### NTLMv2 認証を有効にするかどうかを制御する
  
  
  #### サポートされているバージョン:
  - macOS 以降の 77

  #### 説明
  NTLMv2 を有効にするかどうかを指定します。

最新バージョンのすべての Samba サーバーと Windows サーバーでは、NTLMv2 がサポートされています。下位互換性の問題を解決する場合にのみ、NTLMv2 を無効にしてください。NTLMv2 を無効すると、認証のセキュリティが低下するためです。

このポリシーを構成しなかった場合、NTLMv2 は既定で有効になります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  

  #### Mac の情報と設定
  - 優先されるキーの名前: NtlmV2Enabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ## SmartScreen の設定 policies

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PreventSmartScreenPromptOverride
  #### サイトに関する Microsoft Defender SmartScreen プロンプトをバイパスしない
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  このポリシー設定では、悪意があると考えられる Web サイトに関する Microsoft Defender SmartScreen の警告をユーザーがオーバーライドできるかどうかを指定できます。

この設定を有効にした場合、ユーザーは Microsoft Defender SmartScreen の警告を無視できず、サイトへの移動がブロックされます。

この設定を無効にした場合または構成しなかった場合、ユーザーは Microsoft Defender SmartScreen の警告を無視して、サイトに移動することができます。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PreventSmartScreenPromptOverride
  - GP の名前: サイトに関する Microsoft Defender SmartScreen プロンプトをバイパスしない
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/SmartScreen の設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: PreventSmartScreenPromptOverride
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: PreventSmartScreenPromptOverride
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PreventSmartScreenPromptOverrideForFiles
  #### ダウンロードに関する Microsoft Defende SmartScreen の警告をバイパスしない
  
  
  #### サポートされているバージョン:
  - Windows 以降の 77
  - macOS 以降の 79

  #### 説明
  このポリシー設定では、未確認のダウンロードに関する Microsoft Defender SmartScreen の警告をユーザーがオーバーライドできるかどうかを指定できます。

このポリシーを有効にした場合、組織内のユーザーは Microsoft Defender SmartScreen の警告を無視できず、未確認のダウンロードを完了することはできません。

このポリシーを無効にした場合または構成しなかった場合、ユーザーは Microsoft Defender SmartScreen の警告を無視して、未確認のダウンロードを完了することができます。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PreventSmartScreenPromptOverrideForFiles
  - GP の名前: ダウンロードに関する Microsoft Defende SmartScreen の警告をバイパスしない
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/SmartScreen の設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: PreventSmartScreenPromptOverrideForFiles
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: PreventSmartScreenPromptOverrideForFiles
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SmartScreenAllowListDomains
  #### Microsoft Defender SmartScreen が警告をトリガーしないドメインのリストを構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Defender SmartScreen で信頼するドメインのリストを構成します。これは以下を意味します。
Microsoft Defender SmartScreen では、ソース URL がこれらのドメインに一致すると、フィッシング ソフトウェアや他のマルウェアなど、悪意があると考えられるリソースを確認しません。
Microsoft Defender SmartScreen のダウンロード保護サービスでは、これらのドメインでホストされているダウンロードを確認しません。

このポリシーを有効にした場合、Microsoft Defender SmartScreen はこれらのドメインを信頼します。
このポリシーを無効にした場合または設定しなかった場合、既定の Microsoft Defender SmartScreen 保護がすべてのリソースに適用されます。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。
また、組織で Microsoft Defender Advanced Threat Protection が有効になっていると、このポリシーが適用されません。代わりに、Microsoft Defender セキュリティ センターで許可リストと禁止リストを構成する必要があります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SmartScreenAllowListDomains
  - GP の名前: Microsoft Defender SmartScreen が警告をトリガーしないドメインのリストを構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/SmartScreen の設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\2 = "myuniversity.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: SmartScreenAllowListDomains
  - サンプル値:
``` xml
<array>
  <string>mydomain.com</string>
  <string>myuniversity.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SmartScreenEnabled
  #### Microsoft Defender SmartScreen を構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  このポリシー設定では、Microsoft Defender SmartScreen を有効にするかどうかを構成できます。Microsoft Defender SmartScreen は、フィッシング詐欺や悪意のあるソフトウェアの可能性からユーザーを保護するための警告メッセージを提示します。既定では、Microsoft Defender SmartScreen は有効になります。

この設定を有効にした場合、Microsoft Defender SmartScreen が有効になります。

この設定を無効にした場合、Microsoft Defender SmartScreen が無効になります。

この設定を構成しなかった場合、Microsoft Defender SmartScreen を使用するかどうかをユーザーが選択できます。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SmartScreenEnabled
  - GP の名前: Microsoft Defender SmartScreen を構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/SmartScreen の設定
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/SmartScreen の設定
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: SmartScreenEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: SmartScreenEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SmartScreenForTrustedDownloadsEnabled
  #### 信頼された発行元からダウンロードするときに、Microsoft Defender SmartScreen のチェックを強制的に行う
  
  
  #### サポートされているバージョン:
  - Windows 以降の 78

  #### 説明
  このポリシー設定では、Microsoft Defender SmartScreen が信頼できる発行元からダウンロード評価を確認するかどうかを構成できます。

この設定を有効にした場合または構成しなかった場合は、Microsoft Defender SmartScreen は、発行元にかかわらずダウンロード評価を確認します。

この設定を無効にした場合、Microsoft Defender SmartScreen は、信頼できる発行元からダウンロードする際にダウンロード評価を確認しません。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、またはデバイス管理用に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンスでのみ利用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SmartScreenForTrustedDownloadsEnabled
  - GP の名前: 信頼された発行元からダウンロードするときに、Microsoft Defender SmartScreen のチェックを強制的に行う
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/SmartScreen の設定
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/SmartScreen の設定
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: SmartScreenForTrustedDownloadsEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SmartScreenPuaEnabled
  #### 望ましくない可能性のあるアプリをブロックするように Microsoft Defender SmartScreen を構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 80

  #### 説明
  このポリシー設定では、Microsoft Defender SmartScreen を使用して望ましくない可能性のあるアプリのブロックを有効にするかどうかを構成できます。Microsoft Defender SmartScreen を使用して望ましくない可能性のあるアプリをブロックすると、Web サイトでホストされているアドウェア、コイン マイナー、バンドルウェア、および他の低評価のアプリからユーザーを保護するための警告メッセージが提示されます。既定では、Microsoft Defender SmartScreen を使用した望ましくない可能性のあるアプリのブロックは無効になります。

この設定を有効にした場合、Microsoft Defender SmartScreen での望ましくない可能性のあるアプリのブロックが有効になります。

この設定を無効にした場合、Microsoft Defender SmartScreen を使用した望ましくない可能性のあるアプリのブロックが無効になります。

この設定を構成しなかった場合、Microsoft Defender SmartScreen を使用して望ましくない可能性のあるアプリのブロックを使用するかどうかはユーザーが選択できます。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SmartScreenPuaEnabled
  - GP の名前: 望ましくない可能性のあるアプリをブロックするように Microsoft Defender SmartScreen を構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/SmartScreen の設定
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/SmartScreen の設定
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: SmartScreenPuaEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: SmartScreenPuaEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ## コンテンツの設定 policies

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AutoSelectCertificateForUrls
  #### 該当のサイトでクライアント証明書を自動的に選択する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  サイトがクライアント証明書を要求している場合に Microsoft Edge でクライアント証明書を自動的に選択するサイトのリストを、URL パターンに基づいて定義します。

値は、文字列化した JSON 辞書の配列で指定する必要があります。各辞書の形式は、{ "pattern": "$URL_PATTERN", "filter" : $FILTER } になっている必要があります。$URL_PATTERN はコンテンツ設定パターンを表します。$FILTER によって、ブラウザーで自動的に選択されるクライアント証明書の発行元を絞り込みます。ただしフィルターの設定に関わらず、選択されるのは、サーバーの証明書の要求に一致する証明書のみです。たとえば、$FILTER を { "ISSUER": { "CN": "$ISSUER_CN" } } という形式で指定すると、CommonName $ISSUER_CN を持つ証明書によって発行されたクライアント証明書のみが選択されます。$FILTER に "ISSUER" と "SUBJECT" のセクションが含まれている場合、クライアント証明書は、選択対象となる両方の条件を満たしている必要があります。$FILTER に組織 ("O") が指定されている場合、証明書は、選択対象となる指定の値に一致する組織を 1 つ以上含んでいる必要があります。$FILTER に組織単位 ("OU") が指定されている場合、証明書は、選択対象となる指定の値に一致する組織単位を 1 つ以上含んでいる必要があります。$FILTER が空の辞書 {} の場合、クライアント証明書の選択は、こうした制限を受けません。

このポリシーを構成しなかった場合、どのサイトについても証明書の自動選択は行われません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AutoSelectCertificateForUrls
  - GP の名前: 該当のサイトでクライアント証明書を自動的に選択する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls\1 = "{\"pattern\":\"https://www.contoso.com\",\"filter\":{\"ISSUER\":{\"CN\":\"certificate issuer name\", \"L\": \"certificate issuer location\", \"O\": \"certificate issuer org\", \"OU\": \"certificate issuer org unit\"}, \"SUBJECT\":{\"CN\":\"certificate subject name\", \"L\": \"certificate subject location\", \"O\": \"certificate subject org\", \"OU\": \"certificate subject org unit\"}}}"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: AutoSelectCertificateForUrls
  - サンプル値:
``` xml
<array>
  <string>{"pattern":"https://www.contoso.com","filter":{"ISSUER":{"CN":"certificate issuer name", "L": "certificate issuer location", "O": "certificate issuer org", "OU": "certificate issuer org unit"}, "SUBJECT":{"CN":"certificate subject name", "L": "certificate subject location", "O": "certificate subject org", "OU": "certificate subject org unit"}}}</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### CookiesAllowedForUrls
  #### 特定のサイトで Cookie を許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Cookie の設定が許可されるサイトのリストを、URL パターンに基づいて定義します。

このポリシーを構成しなかった場合、すべてのサイトで、[DefaultCookiesSetting](#defaultcookiessetting) ポリシーのグローバル デフォルト値 (設定されている場合)、またはユーザーの個人用の構成が使用されます。

詳細については、[CookiesBlockedForUrls](#cookiesblockedforurls) ポリシーと [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) ポリシーを参照してください。

以下の 3 つのポリシーでは、URL パターンが競合しない必要があります。

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- CookiesAllowedForUrls

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

終了時の Cookie の削除を除外する場合は、[SaveCookiesOnExit](#savecookiesonexit) ポリシーを構成してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: CookiesAllowedForUrls
  - GP の名前: 特定のサイトで Cookie を許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: CookiesAllowedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### CookiesBlockedForUrls
  #### 特定のサイトで Cookie をブロックする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Cookie を設定できないサイトのリストを、URL パターンに基づいて定義します。

このポリシーを構成しなかった場合、すべてのサイトで、[DefaultCookiesSetting](#defaultcookiessetting) ポリシーのグローバル デフォルト値 (設定されている場合)、またはユーザーの個人用の構成が使用されます。

詳細については、[CookiesAllowedForUrls](#cookiesallowedforurls) ポリシーと [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) ポリシーを参照してください。

以下の 3 つのポリシーでは、URL パターンが競合しない必要があります。

- CookiesBlockedForUrls

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: CookiesBlockedForUrls
  - GP の名前: 特定のサイトで Cookie をブロックする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: CookiesBlockedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### CookiesSessionOnlyForUrls
  #### 特定の Web サイトからの Cookie を現在のセッションに制限する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  定義した URL パターンに一致する Web サイトで作成された Cookie は、セッションの終了時 (ウィンドウを閉じたとき) に削除されます。

パターンに一致しない Web サイトで作成された Cookie は、[DefaultCookiesSetting](#defaultcookiessetting) ポリシー (設定されている場合)、またはユーザーの個人用の構成によって制御されます。これは、このポリシーを構成しなかった場合の既定の動作でもあります。

Microsoft Edge がバックグラウンド モードで実行されていると、最後のウィンドウを閉じたときに、セッションが終了しない場合があります。この場合、ウィンドウを閉じても Cookie は消去されません。Microsoft Edge がバックグラウンド モードで実行されているときに、どのような処理を行うかを構成する方法の詳細については、[BackgroundModeEnabled](#backgroundmodeenabled) ポリシーを参照してください。

Cookie を作成できる Web サイトを制御する場合は、[CookiesAllowedForUrls](#cookiesallowedforurls) ポリシーと [CookiesBlockedForUrls](#cookiesblockedforurls) ポリシーを使用することもできます。

以下の 3 つのポリシーでは、URL パターンが競合しない必要があります。

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- CookiesSessionOnlyForUrls

前のセッションから URL を復元するように [RestoreOnStartup](#restoreonstartup) ポリシーを設定した場合、このポリシーは無視され、それらのサイトでは Cookie が 永続的に保存されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: CookiesSessionOnlyForUrls
  - GP の名前: 特定の Web サイトからの Cookie を現在のセッションに制限する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: CookiesSessionOnlyForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultCookiesSetting
  #### Cookie を構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Web サイトがユーザーのデバイスに Cookie を作成できるかどうかを制御します。このポリシーは、すべての Web サイトを対象とするか、対象としないかのいずれかです。このポリシーを使用して、特定の Web サイトからの Cookie を有効にすることはできません。

ポリシーを「SessionOnly」に設定すると、セッションの終了時に Cookie が消去されます。Microsoft Edge がバックグラウンド モードで実行されていると、最後のウィンドウを閉じたときに、セッションが終了しない場合があります。この場合、ウィンドウを閉じても Cookie は消去されません。Microsoft Edge がバックグラウンド モードで実行されているときに、どのような処理を行うかを構成する方法の詳細については、[BackgroundModeEnabled](#backgroundmodeenabled) ポリシーを参照してください。

このポリシーを構成しなかった場合、既定の「AllowCookies」が使用され、ユーザーはこの設定を Microsoft Edge の設定で変更できます (ユーザーがこの設定を変更できないようにする場合は、ポリシーを構成してください)。

ポリシー オプションのマッピング:

* AllowCookies (1) = すべてのサイトに Cookie の作成を許可する

* BlockCookies (2) = 任意のサイトに Cookie の作成を許可しない

* SessionOnly (4) = セッションの継続時に Cookie を保持する ([SaveCookiesOnExit](#savecookiesonexit) に記載されているものを除く)

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultCookiesSetting
  - GP の名前: Cookie を構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DefaultCookiesSetting
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultCookiesSetting
  - サンプル値:
``` xml
<integer>1</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultFileSystemReadGuardSetting
  #### 読み取り用のファイル システム API の使用を制御します
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  このポリシーを 3 に設定した場合、Web サイトでは、ファイル システム API を使用して、ホスト オペレーティング システムのファイルシステムに対する読み取りアクセス権を要求できるようになります。このポリシーを 2 に設定した場合、アクセスは拒否されます。

このポリシーを設定しなかった場合、Web サイトはアクセス権を要求できます。ユーザーはこの設定を変更できます。

ポリシー オプションのマッピング:

* BlockFileSystemRead (2) = ファイル システム API を使用して、サイトがファイルとディレクトリへの読み取りアクセス権を要求することを許可しない

* AskFileSystemRead (3) = ファイルシステム API を使用して、サイトがファイルとディレクトリへの読み取りアクセス権をユーザーに要求することを許可する

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultFileSystemReadGuardSetting
  - GP の名前: 読み取り用のファイル システム API の使用を制御します
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DefaultFileSystemReadGuardSetting
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultFileSystemReadGuardSetting
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultFileSystemWriteGuardSetting
  #### 書き込みのためのファイル システム API の使用を制御します
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  このポリシーを 3 に設定した場合、Web サイトでは、ファイル システム API を使用して、ホスト オペレーティング システムのファイルシステムに対する書き込みアクセス権を要求できるようになります。このポリシーを 2 に設定した場合、アクセスは拒否されます。

このポリシーを設定しなかった場合、Web サイトはアクセス権を要求できます。ユーザーはこの設定を変更できます。

ポリシー オプションのマッピング:

* BlockFileSystemWrite (2) = ファイルとディレクトリへの書き込みアクセス権の要求をサイトに許可しない

* AskFileSystemWrite (3) = サイトがファイルとディレクトリへの書き込みアクセス権を付与するようユーザーに依頼することを許可する

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultFileSystemWriteGuardSetting
  - GP の名前: 書き込みのためのファイル システム API の使用を制御します
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DefaultFileSystemWriteGuardSetting
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultFileSystemWriteGuardSetting
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultGeolocationSetting
  #### 位置情報の既定の設定
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Web サイトがユーザーの物理的な場所を追跡できるかどうかを設定します。既定で追跡を許可する (「AllowGeolocation」)か、既定で拒否する (「BlockGeolocation」) か、Web サイトが場所を要求するたびにユーザーに尋ねます (「AskGeolocation」)。

このポリシーを構成しない場合、「AskGeolocation」が使用され、ユーザーはそれを変更できます。

ポリシー オプションのマッピング:

* AllowGeolocation (1) = ユーザーの物理的な場所の追跡をサイトに許可する

* BlockGeolocation (2) = どのサイトにもユーザーの物理的な場所を追跡することを許可しない

* AskGeolocation (3) = サイトでユーザーの物理的な場所を追跡する場合は常に確認する

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultGeolocationSetting
  - GP の名前: 位置情報の既定の設定
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DefaultGeolocationSetting
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultGeolocationSetting
  - サンプル値:
``` xml
<integer>1</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultImagesSetting
  #### 画像の既定の設定
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Web サイトで画像を表示できるかどうかを設定します。画像の表示は、すべてのサイトに対して許可 (「AllowImages」) したり、禁止 (「BlockImages」) したりすることができます。

このポリシーを構成しなかった場合、既定で画像の表示は許可されますが、ユーザーはこの設定を変更できます。

ポリシー オプションのマッピング:

* AllowImages (1) = すべての画像の表示をすべてのサイトに許可する

* BlockImages (2) = すべてサイトで画像の表示を許可しない

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultImagesSetting
  - GP の名前: 画像の既定の設定
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DefaultImagesSetting
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultImagesSetting
  - サンプル値:
``` xml
<integer>1</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultInsecureContentSetting
  #### セキュリティで保護されていないコンテンツの例外の使用を制御する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 80

  #### 説明
  特定のサイトについて混在コンテンツを許可するための例外をユーザーが追加できるかどうかを設定できます。

このポリシーは、[InsecureContentAllowedForUrls](#insecurecontentallowedforurls) ポリシーと [InsecureContentBlockedForUrls](#insecurecontentblockedforurls) ポリシーを使用することで、特定の URL パターンに対してオーバーライドすることができます。

このポリシーを設定しなかった場合、ユーザーは、ブロック可能な混在コンテンツを許可する例外や、オプションでブロック可能な混在コンテンツの自動アップグレードを無効にする例外を追加できます。

ポリシー オプションのマッピング:

* BlockInsecureContent (2) = すべてのサイトで混在したコンテンツの読み込みを許可しない

* AllowExceptionsInsecureContent (3) = ユーザーは混在したコンテンツを許可する例外を追加できる

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultInsecureContentSetting
  - GP の名前: セキュリティで保護されていないコンテンツの例外の使用を制御する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DefaultInsecureContentSetting
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultInsecureContentSetting
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultJavaScriptSetting
  #### JavaScript の既定の設定
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Web サイトで JavaScript を実行できるかどうかを設定します。JavaScript の実行は、すべてのサイトで許可したり (「AllowJavaScript」)、すべてのサイトで禁止したり (「BlockJavaScript」) することができます。

このポリシーを構成しなかった場合、既定ではすべてのサイトで JavaScript を実行できますが、ユーザーはこの設定を変更できます。

ポリシー オプションのマッピング:

* AllowJavaScript (1) = JavaScript の実行をすべてのサイトに許可する

* BlockJavaScript (2) = どのサイトに対しても JavaScript の実行を許可しない

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultJavaScriptSetting
  - GP の名前: JavaScript の既定の設定
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DefaultJavaScriptSetting
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultJavaScriptSetting
  - サンプル値:
``` xml
<integer>1</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultNotificationsSetting
  #### 通知の既定の設定
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Web サイトがデスクトップ通知を表示できるかどうかを設定します。通知の表示を既定で許可 (「AllowNotifications」) したり、通知の表示を既定で禁止 (「BlockNotifications」) したりすることができます。また、Web サイトで通知の表示が必要になるたびにユーザーに確認することもできます (「AskNotifications」)。

このポリシーを構成しなかった場合、通知の表示は既定で許可されますが、ユーザーはこの設定を変更できます。

ポリシー オプションのマッピング:

* AllowNotifications (1) = デスクトップ通知の表示をサイトに許可する

* BlockNotifications (2) = どのサイトに対してもデスクトップ通知の表示を許可しない

* AskNotifications (3) = サイトでデスクトップ通知を表示することを毎回確認する

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultNotificationsSetting
  - GP の名前: 通知の既定の設定
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DefaultNotificationsSetting
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultNotificationsSetting
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultPluginsSetting
  #### Adobe Flash の既定の設定
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  [PluginsAllowedForUrls](#pluginsallowedforurls) および [PluginsBlockedForUrls](#pluginsblockedforurls) が最初に確認されてから、このポリシーが確認されます。オプションは、 'ClickToPlay' と 'BlockPlugins' です。'BlockPlugins' に設定すると、このプラグインはすべての Web サイトで拒否されます。'ClickToPlay' に設定すると、Flash プラグインが実行され、ユーザーはプレースホルダーをクリックして開始します。

このポリシーを設定しない場合は、BlockPlugins が設定されますが、ユーザーはこの設定を変更できます。

注: 自動再生は [PluginsAllowedForUrls](#pluginsallowedforurls) ポリシーに明示的にリストされているドメインでのみ使用されます。自動再生をすべてのサイトに適用するには、http://* and https://* を URL の許可リストに追加します。

ポリシー オプションのマッピング:

* BlockPlugins (2) = Adobe Flash プラグインをブロックする

* ClickToPlay (3) = クリックして再生する

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultPluginsSetting
  - GP の名前: Adobe Flash の既定の設定
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DefaultPluginsSetting
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultPluginsSetting
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultPopupsSetting
  #### ポップアップ ウィンドウの既定の設定
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Web サイトでポップアップ ウィンドウを表示できるかどうかを設定します。ポップアップ ウィンドウの表示は、すべての Web サイトに対して許可 (「AllowPopups」) したり、禁止 (「BlockPopups」) したりすることができます。

このポリシーを構成しなかった場合、既定でポップアップ ウィンドウはブロックされますが、ユーザーはこの設定を変更できます。

ポリシー オプションのマッピング:

* AllowPopups (1) = ポップアップの表示をすべてのサイトに許可する

* BlockPopups (2) = どのサイトにもポップアップの表示を許可しない

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultPopupsSetting
  - GP の名前: ポップアップ ウィンドウの既定の設定
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DefaultPopupsSetting
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultPopupsSetting
  - サンプル値:
``` xml
<integer>1</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultWebBluetoothGuardSetting
  #### Web Bluetooth API の使用を制御する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Web サイトが近くにある Bluetooth デバイスにアクセスできるかどうかを制御します。アクセスを完全に禁止したり、Bluetooth デバイスにアクセスする必要がある場合は、サイトで毎回ユーザーに確認するように要求したりすることができます。

このポリシーを構成しなかった場合、既定値 (「AskWebBluetooth」、ユーザーは毎回確認されます) が使用されます、ユーザーはこの設定を変更できます。

ポリシー オプションのマッピング:

* BlockWebBluetooth (2) = サイトが Web Bluetooth API 経由での Bluetooth デバイスへのアクセスを要求できないようにする

* AskWebBluetooth (3) = 近くの Bluetooth デバイスへのアクセス権を付与するようユーザーに確認することをサイトに許可する

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultWebBluetoothGuardSetting
  - GP の名前: Web Bluetooth API の使用を制御する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DefaultWebBluetoothGuardSetting
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultWebBluetoothGuardSetting
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultWebUsbGuardSetting
  #### WebUSB API の使用を制御する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Web サイトが、接続されている USB デバイスにアクセスできるかどうかを設定します。アクセスを完全にブロックしたり、接続されている USB デバイスへのアクセスが Web サイトで必要になるたびにユーザーに確認したりすることができます。

特定の URL パターンに対してこのポリシーをオーバーライドすることができます。そのためには、「[WebUsbAskForUrls](#webusbaskforurls)」ポリシーと「[WebUsbBlockedForUrls](#webusbblockedforurls)」ポリシーを使用します。

このポリシーを構成しなかった場合、既定では、接続されている USB デバイスにサイトがアクセスできるかどうかをユーザーに確認しますが (「AskWebUsb」)、ユーザーはこの設定を変更できます。

ポリシー オプションのマッピング:

* BlockWebUsb (2) = すべてのサイトが WebUSB API 経由での USB デバイスへのアクセスを要求できないようにする

* AskWebUsb (3) = 接続されている USB デバイスへのアクセス権を付与するようユーザーに確認することをサイトに許可する

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultWebUsbGuardSetting
  - GP の名前: WebUSB API の使用を制御する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DefaultWebUsbGuardSetting
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultWebUsbGuardSetting
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### FileSystemReadAskForUrls
  #### これらのサイトでファイル システム API を使用した読み取りアクセスを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  ポリシーを設定すると、ファイル システム API を使用してホスト オペレーティング システムのファイル システム内のファイルまたはディレクトリへの読み取りアクセス権を付与するようユーザーに要求できるサイトを指定する URL パターンを一覧表示できます。

このポリシーが設定されていないままである場合は、[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) が設定されていれば、すべてのサイトに対して適用されます。設定されていない場合は、ユーザーの個人用設定が適用されます。

URL パターンは [FileSystemReadBlockedForUrls](#filesystemreadblockedforurls) と競合することはできません。URL が両方と一致した場合には、どちらのポリシーも優先されません。

有効な url パターンの詳細については、https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: FileSystemReadAskForUrls
  - GP の名前: これらのサイトでファイル システム API を使用した読み取りアクセスを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\2 = "[*.]example.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: FileSystemReadAskForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### FileSystemReadBlockedForUrls
  #### これらのサイトのファイル システム API を使用して読み取りアクセスをブロックする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  このポリシーを設定した場合、ファイル システム API を使用してホスト オペレーティング システムのファイル システム内のファイルまたはディレクトリへの読み取りアクセス権を付与するようユーザーに要求できないサイトを指定する URL パターンを一覧表示できます。

このポリシーを設定しない場合、[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) が設定されていれば、すべてのサイトに対して適用されます。設定されていない場合は、ユーザーの個人用設定が適用されます。

URL パターンは [FileSystemReadAskForUrls](#filesystemreadaskforurls) と競合することはできません。URL が両方と一致した場合には、どちらのポリシーも優先されません。

有効な url パターンの詳細については、https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: FileSystemReadBlockedForUrls
  - GP の名前: これらのサイトのファイル システム API を使用して読み取りアクセスをブロックする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\2 = "[*.]example.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: FileSystemReadBlockedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### FileSystemWriteAskForUrls
  #### これらのサイトのファイルとディレクトリへの書き込みアクセスを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  このポリシーを設定した場合、ホスト オペレーティング システムのファイル システム内のファイルまたはディレクトリへの書き込みアクセス権を付与するようユーザーに要求できるサイトを指定する URL パターンを一覧表示できます。

このポリシーを設定しない場合、[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) が設定されていれば、すべてのサイトに対して適用されます。設定されていない場合は、ユーザーの個人用設定が適用されます。

URL パターンは [FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls) と競合することはできません。URL が両方と一致した場合には、どちらのポリシーも優先されません。

有効な url パターンの詳細については、https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: FileSystemWriteAskForUrls
  - GP の名前: これらのサイトのファイルとディレクトリへの書き込みアクセスを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\2 = "[*.]example.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: FileSystemWriteAskForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### FileSystemWriteBlockedForUrls
  #### これらのサイトのファイルとディレクトリへの書き込みアクセスをブロックする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  このポリシーを設定した場合、ホスト オペレーティング システムのファイル システム内のファイルまたはディレクトリへの書き込みアクセス権を付与するようユーザーに要求できないサイトを指定する URL パターンを一覧表示できます。

このポリシーを設定しない場合、[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) が設定されていれば、すべてのサイトに対して適用されます。設定されていない場合は、ユーザーの個人用設定が適用されます。

URL パターンは [FileSystemWriteAskForUrls](#filesystemwriteaskforurls) と競合することはできません。URL が両方と一致した場合には、どちらのポリシーも優先されません。

有効な url パターンの詳細については、https://cloud.google.com/docs/chrome-enterprise/policies/url-patterns を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: FileSystemWriteBlockedForUrls
  - GP の名前: これらのサイトのファイルとディレクトリへの書き込みアクセスをブロックする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\2 = "[*.]example.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: FileSystemWriteBlockedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ImagesAllowedForUrls
  #### これらのサイトでの画像表示を許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  画像の表示できるサイトのリストを、URL パターンに基づいて定義します。

このポリシーを構成しなかった場合、すべてのサイトで、[DefaultImagesSetting](#defaultimagessetting) ポリシーのグローバル デフォルト値 (設定されている場合)、またはユーザーの個人用の構成が使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ImagesAllowedForUrls
  - GP の名前: これらのサイトでの画像表示を許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: ImagesAllowedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ImagesBlockedForUrls
  #### 特定のサイトで画像をブロックする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  画像の表示が禁止されるサイトのリストを、URL パターンに基づいて定義します。

このポリシーを構成しなかった場合、すべてのサイトで、[DefaultImagesSetting](#defaultimagessetting) ポリシーのグローバル デフォルト値 (設定されている場合)、またはユーザーの個人用の構成が使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ImagesBlockedForUrls
  - GP の名前: 特定のサイトで画像をブロックする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: ImagesBlockedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### InsecureContentAllowedForUrls
  #### 指定されたサイトのセキュリティで保護されていないコンテンツを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 80

  #### 説明
  安全でない混在コンテンツ (HTTPS サイトの HTTP コンテンツ) を表示できるサイトを指定する URL パターンのリストを作成します。

このポリシーを構成しなかった場合、ブロック可能な混在コンテンツはブロックされ、オプションでブロック可能な混在コンテンツはアップグレードされますが、ユーザーは、特定のサイトについて安全でない混在コンテンツを許可するための例外を設定することができます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: InsecureContentAllowedForUrls
  - GP の名前: 指定されたサイトのセキュリティで保護されていないコンテンツを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\2 = "[*.]example.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: InsecureContentAllowedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### InsecureContentBlockedForUrls
  #### 指定したサイトで安全でないコンテンツをブロックする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 80

  #### 説明
  ブロック可能な (アクティブな) 混在コンテンツ (HTTPS サイトの HTTP コンテンツ) の表示が許可されないサイトや、オプションでブロック可能な混在コンテンツのアップグレードが無効になるサイトを指定する URL パターンのリストを作成します。

このポリシーを構成しなかった場合、ブロック可能な混在コンテンツはブロックされ、オプションでブロック可能な混在コンテンツはアップグレードされますが、ユーザーは、特定のサイトについて安全でない混在コンテンツを許可するための例外を設定することができます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: InsecureContentBlockedForUrls
  - GP の名前: 指定したサイトで安全でないコンテンツをブロックする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\2 = "[*.]example.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: InsecureContentBlockedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### JavaScriptAllowedForUrls
  #### 特定のサイトで JavaScript を許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  JavaScript の実行が許可されるサイトのリストを、URL パターンに基づいて定義します。

このポリシーを構成しなかった場合、すべてのサイトで、[DefaultJavaScriptSetting](#defaultjavascriptsetting) ポリシーのグローバル デフォルト値 (設定されている場合)、またはユーザーの個人用の構成が使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: JavaScriptAllowedForUrls
  - GP の名前: 特定のサイトで JavaScript を許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: JavaScriptAllowedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### JavaScriptBlockedForUrls
  #### 特定のサイトで JavaScript をブロックする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  JavaScript の実行が許可されないサイトのリストを、URL パターンに基づいて定義します。

このポリシーを構成しなかった場合、すべてのサイトで、[DefaultJavaScriptSetting](#defaultjavascriptsetting) ポリシーのグローバル デフォルト値 (設定されている場合)、またはユーザーの個人用の構成が使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: JavaScriptBlockedForUrls
  - GP の名前: 特定のサイトで JavaScript をブロックする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: JavaScriptBlockedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### LegacySameSiteCookieBehaviorEnabled
  #### 従来の SameSite Cookie の動作に関する設定を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 80

  #### 説明
  すべての Cookie を、従来の SameSite の動作に戻すことができます。従来の動作に戻すと、SameSite 属性を指定していない Cookie は「SameSite=None」として処理され、「SameSite=None」Cookie には「Secure」属性を指定する必要がなくなります。

このポリシーを設定しなかった場合、SameSite 属性が指定されていない Cookie の既定の動作は、SameSite-by-default 機能に関する別の構成ソースによって決まります。この機能は、フィールド トライアルまたは edge://flags の same-site-by-default-cookies フラグを有効にすることによって設定されている場合があります。

ポリシー オプションのマッピング:

* DefaultToLegacySameSiteCookieBehavior (1) = すべてのサイトの Cookie について、従来の SameSite の動作に戻す

* DefaultToSameSiteByDefaultCookieBehavior (2) = すべてのサイトの Cookie について、SameSite-by-default の動作を使用する

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: LegacySameSiteCookieBehaviorEnabled
  - GP の名前: 従来の SameSite Cookie の動作に関する設定を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: LegacySameSiteCookieBehaviorEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: LegacySameSiteCookieBehaviorEnabled
  - サンプル値:
``` xml
<integer>1</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### LegacySameSiteCookieBehaviorEnabledForDomainList
  #### 指定されたサイトの Cookie について、従来の SameSite の動作に戻す
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 80

  #### 説明
  指定されたパターンに一致するドメインに対して設定された Cookie が、従来の SameSite の動作に戻ります。

従来の動作に戻すと、SameSite 属性を指定していない Cookie は "SameSite=None" として処理され、"SameSite=None" Cookie には "Secure" 属性を指定する必要がなくなります。

このポリシーを設定しなかった場合、グローバル デフォルト値が使用されます。グローバル デフォルト値は、指定したパターンに該当しないドメインの Cookie に対しても使用されます。

グローバル デフォルト値は、[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) ポリシーを使用して構成できます。[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) を設定しなかった場合、グローバル デフォルト値は、別の構成ソースに戻ります。

このポリシーに指定したパターンは、URL ではなくドメインとして扱われるため、スキームやポートは指定しないでください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: LegacySameSiteCookieBehaviorEnabledForDomainList
  - GP の名前: 指定されたサイトの Cookie について、従来の SameSite の動作に戻す
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\1 = "www.example.com"
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\2 = "[*.]example.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: LegacySameSiteCookieBehaviorEnabledForDomainList
  - サンプル値:
``` xml
<array>
  <string>www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NotificationsAllowedForUrls
  #### 特定のサイトで通知を許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  通知の表示を許可するサイトを指定するための URL パターンのリストを作成することができます。

このポリシーを設定しない場合、グローバルな既定値がすべてのサイトで使用されます。この既定値は、設定されている場合には [DefaultNotificationsSetting](#defaultnotificationssetting) ポリシーに基づいて、またはユーザーの個人設定に基づいて設定されます。有効な URL パターンに関する詳細については、[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: NotificationsAllowedForUrls
  - GP の名前: 特定のサイトで通知を許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: NotificationsAllowedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NotificationsBlockedForUrls
  #### 特定のサイトで通知をブロックする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  通知の表示を許可しないサイトを指定するための URL パターンのリストを作成することができます。

このポリシーを設定しない場合、グローバルな既定値がすべてのサイトで使用されます。この既定値は、設定されている場合には [DefaultNotificationsSetting](#defaultnotificationssetting) ポリシーに基づいて、またはユーザーの個人設定に基づいて設定されます。有効な URL パターンに関する詳細については、[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: NotificationsBlockedForUrls
  - GP の名前: 特定のサイトで通知をブロックする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: NotificationsBlockedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PluginsAllowedForUrls
  #### 特定のサイトで Adobe Flash プラグインを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Adobe Flash プラグインを実行できるサイトのリストを URL パターンに基づいて定義します。

このポリシーを設定しない場合、[DefaultPluginsSetting](#defaultpluginssetting) ポリシー (設定されている場合) のグローバルな既定値、またはユーザーの個人用の構成がすべてのサイトで使用されます。

有効な URL パターンの詳細については、[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) を参照してください。ただし、M85 以降、ホストに "*" と "[*.]" のワイルドカードを持つパターンについては、このポリシーではサポートされなくなりました。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PluginsAllowedForUrls
  - GP の名前: 特定のサイトで Adobe Flash プラグインを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\2 = "http://contoso.edu:8080"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: PluginsAllowedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PluginsBlockedForUrls
  #### 特定のサイトで Adobe Flash プラグインをブロックする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  URLパターンに基づいて、Adobe Flash の実行をブロックするサイトのリストを定義します。

このポリシーを設定しない場合、[DefaultPluginsSetting](#defaultpluginssetting) ポリシー (設定されている場合) のグローバルな既定値、またはユーザーの個人用の構成がすべてのサイトで使用されます。

有効な URL パターンの詳細については、[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) を参照してください。ただし、M85 以降、ホストに "*" と "[*.]" のワイルドカードを持つパターンについては、このポリシーではサポートされなくなりました。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PluginsBlockedForUrls
  - GP の名前: 特定のサイトで Adobe Flash プラグインをブロックする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\2 = "http://contoso.edu:8080"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: PluginsBlockedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PopupsAllowedForUrls
  #### 特定のサイトでのポップアップ ウィンドウを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ポップアップ ウィンドウを開くことができるサイトのリストを、URL パターンに基づいて定義します。

このポリシーを構成しなかった場合、すべてのサイトで、[DefaultPopupsSetting](#defaultpopupssetting) ポリシーのグローバル デフォルト値 (設定されている場合)、またはユーザーの個人用の構成が使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PopupsAllowedForUrls
  - GP の名前: 特定のサイトでのポップアップ ウィンドウを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: PopupsAllowedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PopupsBlockedForUrls
  #### 特定のサイトでポップアップ ウィンドウをブロックする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ポップアップ ウィンドウを開くことが禁止されているサイトのリストを、URL パターンに基づいて定義します。

このポリシーを構成しなかった場合、すべてのサイトで、[DefaultPopupsSetting](#defaultpopupssetting) ポリシーのグローバル デフォルト値 (設定されている場合)、またはユーザーの個人用の構成が使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PopupsBlockedForUrls
  - GP の名前: 特定のサイトでポップアップ ウィンドウをブロックする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: PopupsBlockedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### RegisteredProtocolHandlers
  #### プロトコル ハンドラーを登録する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  プロトコル ハンドラーのリストを登録する場合に、このポリシーを設定します (推奨のみ)。このリストは、ユーザーによって登録されたものと統合され、両方を使用できます。

プロトコル ハンドラーを登録するには:

- プロトコルのプロパティをスキームに設定します (例: "mailto")
- URL のプロパティを、"protocol" フィールドで指定されているスキームを処理するアプリケーションの URL プロパティに設定します。パターンには、処理された URL に置き換えられる "%s" プレースホルダーを含めることができます。

ユーザーは、このポリシーで登録されたプロトコル ハンドラーを削除できません。ただし、新しい既定のプロトコル ハンドラーをインストールして、既存のプロトコル ハンドラーを上書きすることができます。

  #### サポートされている機能:
  - 必須になる場合があります: いいえ
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 辞書

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: RegisteredProtocolHandlers
  - GP の名前: プロトコル ハンドラーを登録する
  - GP パス (必須): N/A
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/コンテンツの設定
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): N/A
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: RegisteredProtocolHandlers
  - 値の種類: REG_SZ
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [
  {
    "default": true, 
    "protocol": "mailto", 
    "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"
  }
]
```


  #### Mac の情報と設定
  - 優先されるキーの名前: RegisteredProtocolHandlers
  - サンプル値:
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
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SpotlightExperiencesAndRecommendationsEnabled
  #### ユーザーがカスタマイズされた背景画像とテキスト、提案、通知、
および Microsoft サービスのヒントを受け取ることができるかどうかを選択する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 86

  #### 説明
  ユーザーがカスタマイズされた背景画像とテキスト、提案、通知、Microsoft サービスのヒントを受け取ることができるかどうかを選択します。

この設定を有効にするか、設定しない場合、スポットライト エクスペリエンスとおすすめ候補がオンになります。

この設定を無効にすると、スポットライト エクスペリエンスとおすすめ候補はオフになります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SpotlightExperiencesAndRecommendationsEnabled
  - GP の名前: ユーザーがカスタマイズされた背景画像とテキスト、提案、通知、
および Microsoft サービスのヒントを受け取ることができるかどうかを選択する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: SpotlightExperiencesAndRecommendationsEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### WebUsbAllowDevicesForUrls
  #### 特定の USB デバイスに接続するために、特定のサイトへのアクセスを許可します
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  URL のリストを設定して、特定のベンダー ID と製品 ID を持つ USB デバイスへのアクセス許可が自動的に付与されるサイトを指定することを許可します。ポリシーを有効にするには、リストの各項目にデバイスと URL の両方が含まれている必要があります。デバイスに関する各項目には、ベンダー ID と製品 ID のフィールドを含めることができます。省略された ID はすべて、ワイルドカードとして扱われます。ただし、製品 ID を指定するときはベンダー ID も指定する必要があるので、注意してください。ベンダー ID を指定しないで製品 ID を指定した場合、このポリシーは無効になり、無視されます。

USB アクセス許可モデルでは、要求元サイト ("要求元 URL") の URL とトップレベルのフレーム サイト ("埋め込み URL") の URL を使用して、要求元 URL に対して USB デバイスへのアクセス許可を付与します。要求元サイトが iframe に読み込まれる場合、要求元 URL は、埋め込み URL とは異なる可能性があります。このため、"urls" フィールドに最大 2 個までの URL 文字列を含めて (コンマで区切ります)、要求元 URL と埋め込み URL をそれぞれ指定することができます。URL を 1 つだけ指定した場合は、埋め込みの状態に関係なく、要求元サイトの URL がこの URL と一致すると、対応する USB デバイスへのアクセスが許可されます。"urls" 内の URL は有効な URL である必要があります。有効な URL でない場合は、ポリシーは無視されます。

このポリシーを設定しなかった場合、すべてのサイトで、[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) ポリシーのグローバル デフォルト値 (設定されている場合)、またはユーザーの個人用の構成が使用されます。

このポリシーでの URL パターンは、[WebUsbBlockedForUrls](#webusbblockedforurls) で構成されているパターンとは重複しないパターンを指定してください。パターンが重複する場合、このポリシーは [WebUsbBlockedForUrls](#webusbblockedforurls) および [WebUsbAskForUrls](#webusbaskforurls) よりも優先されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 辞書

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: WebUsbAllowDevicesForUrls
  - GP の名前: 特定の USB デバイスに接続するために、特定のサイトへのアクセスを許可します
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: WebUsbAllowDevicesForUrls
  - 値の種類: REG_SZ
  ##### サンプル値:
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


  #### Mac の情報と設定
  - 優先されるキーの名前: WebUsbAllowDevicesForUrls
  - サンプル値:
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
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### WebUsbAskForUrls
  #### 特定のサイトでの WebUSB を許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  USB デバイスへのアクセスをユーザーに確認できるサイトのリストを、URL パターンに基づいて定義します。

このポリシーを構成しなかった場合、すべてのサイトで、[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) ポリシーのグローバル 既定値 (設定されている場合)、またはユーザーの個人用の構成が使用されます。

このポリシーで定義する URL パターンは、[WebUsbBlockedForUrls](#webusbblockedforurls) ポリシーで構成されている URL パターンと競合しないようにする必要があります。URL の許可とブロックの両方を構成することはできません。有効な URL パターンの詳細については、[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) を参照してください

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: WebUsbAskForUrls
  - GP の名前: 特定のサイトでの WebUSB を許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: WebUsbAskForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### WebUsbBlockedForUrls
  #### 特定のサイトでの WebUSB をブロックする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  USB デバイスへのアクセス権の付与をユーザーに確認することができないサイトのリストを、URL パターンに基づいて定義します。

このポリシーを構成しなかった場合、すべてのサイトで、[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) ポリシーのグローバル 既定値 (設定されている場合)、またはユーザーの個人用の構成が使用されます。

このポリシーの URL パターンは、[WebUsbAskForUrls](#webusbaskforurls) ポリシーで構成されている URL パターンと競合しないようにする必要があります。URL の許可とブロックの両方を構成することはできません。有効な URL パターンの詳細については、[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: WebUsbBlockedForUrls
  - GP の名前: 特定のサイトでの WebUSB をブロックする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/コンテンツの設定
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: WebUsbBlockedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ## スタートアップ、ホーム ページ、新しいタブ ページ policies

  [トップに戻る](#microsoft-edge---ポリシー)

  ### HomepageIsNewTabPage
  #### 新しいタブ ページをホーム ページとして設定する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge の既定のホームページを構成します。ホームページは、指定の URL に設定したり、新しいタブ ページに設定したりすることができます。

このポリシーを有効にした場合、新しいタブ ページが常にホーム ページに使用され、ホーム ページの URL の場所は無視されます。

このポリシーを無効にした場合、URL を 'edge://newtab' に設定しない限り、ユーザーのホーム ページは新しいタブ ページとして設定できません。

このポリシーを構成しなかった場合、ユーザーは新しいタブ ページをホーム ページにするかどうかを選択できます。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: HomepageIsNewTabPage
  - GP の名前: 新しいタブ ページをホーム ページとして設定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: HomepageIsNewTabPage
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: HomepageIsNewTabPage
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### HomepageLocation
  #### ホーム ページの URL を構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edgeでの既定のホーム ページの URL を構成します。

ホーム ページは、[ホーム] ボタンで開くページです。スタートアップ時に開くページは、[RestoreOnStartup](#restoreonstartup) ポリシーで制御します。

ここで URL を設定することも、新しいタブ ページを開くようにホーム ページを設定することもできます。新しいタブ ページを開くように選択した場合、このポリシーは適用されません。

このポリシーを有効にすると、ユーザーはホーム ページの URL を変更できなくなりますが、新しいタブ ページをホーム ページとして選択することはできます。

このポリシーを無効にした場合または構成しなかった場合、[HomepageIsNewTabPage](#homepageisnewtabpage) ポリシーが有効になっていなければ、ユーザーは自分のホーム ページを選択できます。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: HomepageLocation
  - GP の名前: ホーム ページの URL を構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: HomepageLocation
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"https://www.contoso.com"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: HomepageLocation
  - サンプル値:
``` xml
<string>https://www.contoso.com</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NewTabPageAllowedBackgroundTypes
  #### 新しいタブページのレイアウトで使用できる背景の種類を構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  Microsoft Edge の新しいタブ ページのレイアウトで使用できる背景画像の種類を構成できます。

このポリシーを構成しない場合、新しいタブ ページですべての背景画像の種類が有効になります。

ポリシー オプションのマッピング:

* DisableImageOfTheDay (1) = 毎日の背景画像の種類を無効にする

* DisableCustomImage (2) = ユーザー設定の背景画像の種類を無効にする

* DisableAll (3) = 背景画像の種類をすべて無効にする

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: NewTabPageAllowedBackgroundTypes
  - GP の名前: 新しいタブページのレイアウトで使用できる背景の種類を構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: NewTabPageAllowedBackgroundTypes
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: NewTabPageAllowedBackgroundTypes
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NewTabPageCompanyLogo
  #### 新しいタブ ページでの会社のロゴを設定する (現在不使用)
  
  >古い形式: このポリシーは古い形式であり、Microsoft Edge 85 以降では使用することができません。
  #### サポートされているバージョン:
  - Windows 以降、macOS と 79 を 85

  #### 説明
  このポリシーは、運用要件の変更のため適切に機能しません。そのため非推奨となっており、使用しないことをお勧めします。

Microsoft Edge の新しいタブ ページで使用する会社のロゴを指定します。

ポリシーは、ロゴを JSON 形式で表す文字列として構成する必要があります。たとえば、次のように指定します: { "default_logo": { "url": "https://www.contoso.com/logo.png", "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29" }, "light_logo": { "url": "https://www.contoso.com/light_logo.png", "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737" } }

このポリシーを構成するには、URL と暗号化ハッシュ (SHA-256) を指定します。URL は、Microsoft Edge でロゴをダウンロードできる URL です。暗号化ハッシュは、ダウンロードの整合性の検証に使用されます。ロゴは PNG 形式または SVG 形式で、そのファイル サイズは 16 MB 以下であることが必要です。ロゴはダウンロードされ、キャッシュされます。また、URL やハッシュが変更された場合は必ず再ダウンロードされます。URL には、認証なしでアクセスできる必要があります。

'default_logo' は必須で、背景画像がないときに使用されます。'light_logo' が指定されている場合は、ユーザーの新しいタブ ページに背景画像があるときにそのロゴが使用されます。透明な背景を持つ横向きのロゴを使用し、そのロゴを左揃えで、縦方向に中央揃えさせることをお勧めします。ロゴの最小の高さは 32 ピクセル、縦横比は 1:1 から 4:1 までにする必要があります。'default_logo' には、白黒の背景に対して適切なコントラストを設定する必要があります。これに対して、'light_logo' には、背景画像に対して適切なコントラストを設定する必要があります

このポリシーを有効にした場合、Microsoft Edge では指定したロゴがダウンロードされ、新しいタブ ページに表示されます。ユーザーは、ロゴをオーバーライドしたり、非表示にしたりすることはできません。

このポリシーを無効にした場合または構成しなかった場合、Microsoft Edge では、会社のロゴや Microsoft ロゴが新しいタブ ページに表示されません。

SHA-256 ハッシュの指定に役立つ情報については、https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/get-filehash を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 辞書

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: NewTabPageCompanyLogo
  - GP の名前: 新しいタブ ページでの会社のロゴを設定する (現在不使用)
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: NewTabPageCompanyLogo
  - 値の種類: REG_SZ
  ##### サンプル値:
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


  #### Mac の情報と設定
  - 優先されるキーの名前: NewTabPageCompanyLogo
  - サンプル値:
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
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NewTabPageHideDefaultTopSites
  #### 新しいタブ ページで既定のトップ サイトを非表示にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge で、新しいタブ ページに既定のトップ サイトが表示されないようにします。

このポリシーを true に設定した場合、既定のトップ サイトのタイルが非表示になります。

このポリシーを false に設定した場合または構成しなかった場合は、既定のトップ サイトのタイルは表示されたままになります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: NewTabPageHideDefaultTopSites
  - GP の名前: 新しいタブ ページで既定のトップ サイトを非表示にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: NewTabPageHideDefaultTopSites
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: NewTabPageHideDefaultTopSites
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NewTabPageLocation
  #### 新しいタブ ページの URL を構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  新しいタブ ページの既定の URL を構成します。

このポリシーは、新しいタブの作成時 (新しいウィンドウを開いた時も含む) に開くページを特定します。また、スタートアップ ページで新しいタブ ページを開くように設定している場合は、スタートアップ ページに対しても適用されます。

このポリシーでは、スタートアップ時に開くページは特定されません。このようなページは、[RestoreOnStartup](#restoreonstartup) ポリシーによって制御されます。またこのポリシーは、ホーム ページで新しいタブ ページを開くように設定している場合でも、ホーム ページに対しては適用されません。

このポリシーを構成しなかった場合、既定の新しいタブ ページが使用されます。

このポリシー*および* [NewTabPageSetFeedType](#newtabpagesetfeedtype) ポリシーを構成した場合は、このポリシーが優先されます。

無効な URL が指定された場合、新しいタブで about://blank が開きます。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: NewTabPageLocation
  - GP の名前: 新しいタブ ページの URL を構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: NewTabPageLocation
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"https://www.fabrikam.com"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: NewTabPageLocation
  - サンプル値:
``` xml
<string>https://www.fabrikam.com</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NewTabPageManagedQuickLinks
  #### 新しいタブ ページのクイック リンクを設定する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 79

  #### 説明
  既定では、Microsoft Edge は、ユーザーが追加したショートカットや閲覧の履歴に基づくトップ サイトから開かれる新しいタブ ページにクイック リンクを表示します。このポリシーでは、新しいタブページにクイック リンクのタイルを 3 つまで構成できます。これらのタイルは JSON オブジェクトとして表します

[ { "url": "https://www.contoso.com", "title": "Contoso Portal", "pinned": true/false }, ... ]

'url' フィールドは必須です。'title' と 'pinned' はオプションです。'title' が指定されていない場合は、URL が既定のタイトルとして使用されます。'pinned' が指定されていない場合は、既定値は false になります。

Microsoft Edge では、これらのタイルがリスト指定された順に、左から右へ表示されます。また、ピン留めされたすべてのタイルは、ピン留めされていないタイルよりも前に表示されます。

ポリシーを必須として設定した場合、'pinned' (ピン留めされた) フィールドは無視され、すべてのタイルがピン留めされます。ユーザーはタイルを削除できません。また、タイルは常にクイック リンク リストの先頭に表示されます。

このポリシーを推奨として設定した場合、ピン留めされたタイルはリストに残りますが、ユーザーはタイルを編集したり削除したりすることができます。ピン留めされていないクイック リンクのタイルは、既定のトップ サイトように動作し、他の Web サイトが頻繁にアクセスされるとこのタイルはリストから除外されます。ピン留めされていないリンクを、このポリシーを利用して既存のブラウザー プロファイルに適用すると、リンクのランクとユーザーの閲覧履歴との比較方法によっては、リンクが完全に表示されなくなる場合があります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 辞書

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: NewTabPageManagedQuickLinks
  - GP の名前: 新しいタブ ページのクイック リンクを設定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: NewTabPageManagedQuickLinks
  - 値の種類: REG_SZ
  ##### サンプル値:
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


  #### Mac の情報と設定
  - 優先されるキーの名前: NewTabPageManagedQuickLinks
  - サンプル値:
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
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NewTabPagePrerenderEnabled
  #### 新しいタブ ページのプリロードを有効にして、レンダリングを高速化する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 85

  #### 説明
  このポリシーを構成すると、新しいタブ ページの事前読み込みが有効になり、ユーザーはこの設定を変更できなくなります。このポリシーを構成しない場合、事前読み込みが有効になり、ユーザーはこの設定を変更できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: NewTabPagePrerenderEnabled
  - GP の名前: 新しいタブ ページのプリロードを有効にして、レンダリングを高速化する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: NewTabPagePrerenderEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: NewTabPagePrerenderEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NewTabPageSetFeedType
  #### Microsoft Edge の新しいタブ ページ エクスペリエンスを構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 79

  #### 説明
  新しいタブページに対して、Microsoft News または Office 365 のいずれかのフィード エクスペリエンスを選択できます。

このポリシーを「News」に設定すると、新しいタブ ページに Microsoft News フィード エクスペリエンスが表示されます。

このポリシーを「Office」に設定すると、ユーザーが Azure Active Directory ブラウザー サインインを使用している場合は、新しいタブ ページに Office 365 フィード エクスペリエンスが表示されます。

このポリシーを無効にした場合または構成しなかった場合:

- ユーザーが Azure Active Directory ブラウザー サインインを使用している場合は、Office 365 の新しいタブ ページ フィード エクスペリエンス、および標準の新しいタブ ページ フィード エクスペリエンスが提供されます。

- ユーザーが Azure Active Directory ブラウザー サインインを使用していない場合は、標準の新しいタブ ページ エクスペリエンスが表示されます。

このポリシー*および* [NewTabPageLocation](#newtabpagelocation) ポリシーを構成した場合は、[NewTabPageLocation](#newtabpagelocation) が優先されます。

既定の設定: 無効または未構成。

ポリシー オプションのマッピング:

* News (0) = Microsoft News フィード エクスペリエンス

* Office (1) = Office 365 フィード エクスペリエンス

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: NewTabPageSetFeedType
  - GP の名前: Microsoft Edge の新しいタブ ページ エクスペリエンスを構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: NewTabPageSetFeedType
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: NewTabPageSetFeedType
  - サンプル値:
``` xml
<integer>0</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### RestoreOnStartup
  #### スタートアップ時に実行するアクション
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge の起動時の動作を指定します。

起動時に常に新しいタブを開く場合は、'RestoreOnStartupIsNewTabPage' を選択します。

前回 Microsoft Edge の終了時に開いていた URL をもう一度開く場合は、'RestoreOnStartupIsLastSession' を選択します。閲覧セッションが前回と同様に復元されます。このオプションによって、セッションに依存する設定や終了時にアクションを実行する設定 (終了時の閲覧データの消去やセッション専用 Cookie の消去) など、一部の設定が無効になることに注意してください。

URL の特定のセットを開く場合は、'RestoreOnStartupIsURLs' を選択します。

この設定を無効にした場合、設定を構成していない状態と同じになり、ユーザーは、Microsoft Edge で設定を変更できます。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

ポリシー オプションのマッピング:

* RestoreOnStartupIsNewTabPage (5) = 新しいタブを開く

* RestoreOnStartupIsLastSession (1) = 最後のセッションを復元する

* RestoreOnStartupIsURLs (4) = URL の一覧を開く

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: RestoreOnStartup
  - GP の名前: スタートアップ時に実行するアクション
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: RestoreOnStartup
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000004
```


  #### Mac の情報と設定
  - 優先されるキーの名前: RestoreOnStartup
  - サンプル値:
``` xml
<integer>4</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### RestoreOnStartupURLs
  #### ブラウザーの起動時に開くサイト
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ブラウザーの起動時に自動的に表示する Web サイトのリストを指定します。このポリシーを構成しない場合、起動時にいずれのサイトも表示されません。

このポリシーは、[RestoreOnStartup](#restoreonstartup) ポリシーを 'URL のリストを開く' (4) に設定している場合にのみ適用されます。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: RestoreOnStartupURLs
  - GP の名前: ブラウザーの起動時に開くサイト
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ\RestoreOnStartupURLs
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\1 = "https://contoso.com"
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\2 = "https://www.fabrikam.com"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: RestoreOnStartupURLs
  - サンプル値:
``` xml
<array>
  <string>https://contoso.com</string>
  <string>https://www.fabrikam.com</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ShowHomeButton
  #### ツール バーに [ホーム] ボタンを表示する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge のツール バーに [ホーム] ボタンを表示します。

このポリシーを有効にすると、[ホーム] ボタンが常に表示されます。このポリシーを無効にすると、ホーム ボタンは表示されません。

このポリシーを構成しなかった場合、ユーザーは [ホーム] ボタンを表示するかどうかを選択できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ShowHomeButton
  - GP の名前: ツール バーに [ホーム] ボタンを表示する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/スタートアップ、ホーム ページ、新しいタブ ページ
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: ShowHomeButton
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ShowHomeButton
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ## ネイティブ メッセージング policies

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NativeMessagingAllowlist
  #### ユーザーが使用できるネイティブ メッセージング ホストを制御する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザーが Microsoft Edge で使用できる特定のネイティブ メッセージング ホストのリストを指定します。

既定では、すべてのネイティブ メッセージング ホストが許可されます。[NativeMessagingBlocklist](#nativemessagingblocklist) ポリシーを * に設定すると、すべてのネイティブ メッセージング ホストがブロックされ、ここで指定されたネイティブ メッセージング ホストのみが読み込まれます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: NativeMessagingAllowlist
  - GP の名前: ユーザーが使用できるネイティブ メッセージング ホストを制御する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/ネイティブ メッセージング
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\2 = "com.native.messaging.host.name2"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: NativeMessagingAllowlist
  - サンプル値:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NativeMessagingBlocklist
  #### ネイティブ メッセージングの禁止リストを構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  使用を禁止するネイティブ メッセージング ホストを指定します。

ネイティブ メッセージング ホストが明示的に許可リストに登録されていない場合は、'*' を使用して、すべてのネイティブ メッセージング ホストをブロックできます。

このポリシーを構成しなかった場合、Microsoft Edge では、インストールされているすべてのネイティブ メッセージング ホストが読み込まれます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: NativeMessagingBlocklist
  - GP の名前: ネイティブ メッセージングの禁止リストを構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/ネイティブ メッセージング
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\2 = "com.native.messaging.host.name2"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: NativeMessagingBlocklist
  - サンプル値:
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NativeMessagingUserLevelHosts
  #### ユーザー レベルのネイティブ メッセージング ホスト (管理者のアクセス許可なしでインストールされるホスト) を許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ネイティブ メッセージング ホストのユーザー レベルのインストールを有効にします。

このポリシーを無効にした場合、Microsoft Edge では、システム レベルでインストールされたネイティブ メッセージング ホストのみが使用されます。

このポリシーを構成しなかった場合、Microsoft Edge では、既定でユーザー レベルのネイティブ メッセージング ホストを使用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: NativeMessagingUserLevelHosts
  - GP の名前: ユーザー レベルのネイティブ メッセージング ホスト (管理者のアクセス許可なしでインストールされるホスト) を許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/ネイティブ メッセージング
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: NativeMessagingUserLevelHosts
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: NativeMessagingUserLevelHosts
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ## パスワード マネージャーと保護 policies

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PasswordManagerEnabled
  #### パスワード マネージャーへのパスワードの保存を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge を有効にして、ユーザーのパスワードを保存します。

このポリシーを有効にすると、ユーザーは Microsoft Edge でパスワードを保存できます。次回サイトにアクセスしたときに、Microsoft Edge でパスワードが自動的に入力されます。

このポリシーを無効にした場合、ユーザーは新しいパスワードを保存できませんが、前回保存したパスワードを使用することができます。

このポリシーを有効または無効にした場合、ユーザーは Microsoft Edge でこの設定を変更または上書きすることはできません。このポリシーを構成しなかった場合は、ユーザーはパスワードを保存することができ、この機能をオフにすることもできます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PasswordManagerEnabled
  - GP の名前: パスワード マネージャーへのパスワードの保存を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/パスワード マネージャーと保護
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/パスワード マネージャーと保護
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: PasswordManagerEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: PasswordManagerEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PasswordMonitorAllowed
  #### パスワードが安全でないことが判明した場合に、ユーザーにアラートを表示する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 85

  #### 説明
  Microsoft Edge によるユーザーのパスワードの監視を許可します。

 このポリシーを有効にし、ユーザーがこのポリシーの有効化に同意した場合、Microsoft Edge に保存されているパスワードのいずれかが安全でないことが判明すると、そのユーザーにアラートが表示されます。Microsoft Edge にはアラートが表示され、この情報は [設定] > [パスワード] > [パスワード モニター] にも表示されます。

 このポリシーを無効にした場合、ユーザーにこの機能を有効にするための許可を求めることはありません。ユーザーのパスワードはスキャンされず、アラートも表示されません。

 このポリシーを有効にしているか、設定していない場合は、ユーザーはこの機能をオンまたはオフにすることができます。

 Microsoft Edge が安全でないパスワードを検出する方法に関する詳細については、[https://go.microsoft.com/fwlink/?linkid=2133833](https://go.microsoft.com/fwlink/?linkid=2133833) を参照してください

その他のガイド:

 このポリシーは、推奨と必須の両方に設定することができますが、重要なコールアウトがあります。

 必須の有効化: 特定のユーザーに対してこの機能を有効にするには、個々のユーザーの同意が前提条件となるため、このポリシーには必須の有効化設定はありません。ポリシーに必須の有効化が設定されている場合、設定の UI は変更されず、以下のようなエラーメッセージが edge://policy に表示されます

エラー状態メッセージの例: "パスワード モニターをオンにするには、個々のユーザーの同意が必要であるため、このポリシー値は無視されます。組織内のユーザーに、[設定] > [プロファイル] > [パスワード] へとアクセスしてこの機能を有効にするよう求めることができます。"

 推奨の有効化: ポリシーに推奨の有効化が設定されている場合、設定の UI は "オフ" 状態のままですが、その横に [ブリーフケース] アイコンが表示され、カーソルを置くと次の説明が表示されます - "お客様の組織はこの設定に対して特定の値を推奨しており、お客様は別の値を選択しています"

 必須と推奨の無効化: これらの状態はどちらも通常どおりに動作し、ユーザーには通常のキャプションが表示されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PasswordMonitorAllowed
  - GP の名前: パスワードが安全でないことが判明した場合に、ユーザーにアラートを表示する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/パスワード マネージャーと保護
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/パスワード マネージャーと保護
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: PasswordMonitorAllowed
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PasswordProtectionChangePasswordURL
  #### パスワード変更 URL を構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  パスワード変更 URL (HTTP スキームと HTTPS スキームのみ) を構成します。

パスワード保護サービスは、ブラウザーで警告が表示された後、パスワードを変更するためにユーザーをこの URL にアクセスさせます。

このポリシーを有効にした場合、パスワード保護サービスは、パスワードを変更するためにユーザーをこの URL にアクセスさせます。

このポリシーを無効にした場合または構成しなかった場合、パスワード保護サービスは、パスワード変更 URL にユーザーをリダイレクトしません。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PasswordProtectionChangePasswordURL
  - GP の名前: パスワード変更 URL を構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/パスワード マネージャーと保護
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: PasswordProtectionChangePasswordURL
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"https://contoso.com/change_password.html"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: PasswordProtectionChangePasswordURL
  - サンプル値:
``` xml
<string>https://contoso.com/change_password.html</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PasswordProtectionLoginURLs
  #### パスワード保護サービスによってパスワードのソルト付きハッシュがキャプチャされるエンタープライズ ログイン URL のリストを構成します
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge がパスワードのソルト付きハッシュをキャプチャしてパスワード再利用の検出に使用する必要がある、エンタープライズ ログイン URL (HTTP および HTTPS スキームのみ) のリストを構成します。

このポリシーを有効にすると、定義された URL のパスワードのフィンガープリントが、パスワード保護サービスによってキャプチャされます。

このポリシーを無効にするか構成しない場合は、パスワードのフィンガープリントはキャプチャされません。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PasswordProtectionLoginURLs
  - GP の名前: パスワード保護サービスによってパスワードのソルト付きハッシュがキャプチャされるエンタープライズ ログイン URL のリストを構成します
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/パスワード マネージャーと保護
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\1 = "https://contoso.com/login.html"
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\2 = "https://login.contoso.com"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: PasswordProtectionLoginURLs
  - サンプル値:
``` xml
<array>
  <string>https://contoso.com/login.html</string>
  <string>https://login.contoso.com</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PasswordProtectionWarningTrigger
  #### パスワード保護の警告トリガーを構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  パスワード保護の警告をトリガーするタイミングを制御できます。パスワード保護は、ユーザーが保護されたパスワードを不審な可能性があるサイトで再利用するときに、ユーザーに警告します。

保護するパスワードを構成するには、[PasswordProtectionLoginURLs](#passwordprotectionloginurls) ポリシーと [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl) ポリシーを使用できます。

例外: [PasswordProtectionLoginURLs](#passwordprotectionloginurls) ポリシーと [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl) ポリシーで指定されているサイト、および [SmartScreenAllowListDomains](#smartscreenallowlistdomains) ポリシーで指定されているサイトのパスワードは、パスワード保護の警告をトリガーしません。

「PasswordProtectionWarningOff」に設定すると、パスワード保護の警告は表示されません。

「PasswordProtectionWarningOnPasswordReuse」に設定すると、許可リストに登録されていないサイトでユーザーが保護されたパスワードを再利用するときに、パスワード保護の警告が表示されます。

このポリシーを無効にした場合または構成しなかった場合、警告トリガーは表示されません。

ポリシー オプションのマッピング:

* PasswordProtectionWarningOff (0) = パスワード保護の警告がオフになっています

* PasswordProtectionWarningOnPasswordReuse (1) = パスワード保護に関する警告がパスワードの再利用でトリガーされます

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PasswordProtectionWarningTrigger
  - GP の名前: パスワード保護の警告トリガーを構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/パスワード マネージャーと保護
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: PasswordProtectionWarningTrigger
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: PasswordProtectionWarningTrigger
  - サンプル値:
``` xml
<integer>1</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ## プロキシ サーバー policies

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ProxyBypassList
  #### プロキシバイパスの規則を構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge がプロキシをバイパスするホストのリストを定義します。

このポリシーが適用されるのは、[ProxyMode](#proxymode) ポリシーで '固定プロキシ サーバーを使用する' を選択した場合のみです。プロキシ ポリシーの構成で他のモードを選択した場合は、このポリシーを有効にしたり、構成したりしないでください。

このポリシーを有効にした場合、Microsoft Edge がプロキシを使用しないホストのリストを作成できます。

このポリシーを構成しなかった場合、Microsoft Edge がプロキシをバイパスするホストのリストは作成されません。プロキシ ポリシーの設定で他の方法を指定した場合は、このポリシーを構成しないでください。

詳細な例については、[https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936) を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ProxyBypassList
  - GP の名前: プロキシバイパスの規則を構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/プロキシ サーバー
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ProxyBypassList
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"https://www.contoso.com, https://www.fabrikam.com"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ProxyBypassList
  - サンプル値:
``` xml
<string>https://www.contoso.com, https://www.fabrikam.com</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ProxyMode
  #### プロキシ サーバーの設定を構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge で使用されるプロキシ サーバーの設定を指定します。このポリシーを有効にした場合、ユーザーはプロキシ設定を変更できなくなります。

プロキシ サーバーを使用せず、常に直接接続することを選択すると、他のすべてのオプションは無視されます。

システム プロキシ設定を使用すると、他のすべてのオプションは無視されます。

プロキシ サーバーの自動検出を選択すると、他のすべてのオプションは無視されます。

固定サーバー プロキシ モードを選択すると、[ProxyServer](#proxyserver) や「プロキシ バイパス規則のカンマ区切りのリスト」で追加のオプションを指定できます。

.pac プロキシ スクリプトの使用を選択すると、「プロキシ .pac ファイルの URL」でスクリプトへの URL を指定する必要があります。

詳細な例については、[https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936) を参照してください。

このポリシーを有効にした場合、Microsoft Edge では、コマンド ラインから指定したプロキシ関連のすべてのオプションが無視されます。

このポリシーを構成しなかった場合、ユーザーは独自のプロキシ設定を選択できます。

ポリシー オプションのマッピング:

* ProxyDisabled (direct) = プロキシを使用しない

* ProxyAutoDetect (auto_detect) = プロキシの設定を自動的に検出する

* ProxyPacScript (pac_script) = .pac プロキシ スクリプトを使用する

* ProxyFixedServers (fixed_servers) = 固定のプロキシ サーバーを使用する

* ProxyUseSystem (system) = システム プロキシ設定を使用する

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ProxyMode
  - GP の名前: プロキシ サーバーの設定を構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/プロキシ サーバー
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ProxyMode
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"direct"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ProxyMode
  - サンプル値:
``` xml
<string>direct</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ProxyPacUrl
  #### プロキシ .pac ファイルの URL を設定する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  プロキシ自動構成 (PAC) ファイルの URL を指定します

このポリシーが適用されるのは、[ProxyMode](#proxymode) ポリシーで '.pac プロキシ スクリプトを使用する' を選択した場合のみです。プロキシ ポリシーの構成で他のモードを選択した場合は、このポリシーを有効にしたり、構成したりしないでください。

このポリシーを有効にした場合、PAC ファイルの URL を指定できます。このファイルでは、特定の Web サイトを取得するための適切なプロキシ サーバーをブラウザーで自動的に選択する方法が定義されています。

このポリシーを無効にした場合または構成しなかった場合、PAC ファイルは指定されません。プロキシ ポリシーの設定で他の方法を指定した場合は、このポリシーを構成しないでください。

詳細な例については、[https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936) を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ProxyPacUrl
  - GP の名前: プロキシ .pac ファイルの URL を設定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/プロキシ サーバー
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ProxyPacUrl
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"https://internal.contoso.com/example.pac"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ProxyPacUrl
  - サンプル値:
``` xml
<string>https://internal.contoso.com/example.pac</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ProxyServer
  #### プロキシ サーバーのアドレスまたは URL を構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  プロキシ サーバーの URL を指定します。

このポリシーが適用されるのは、[ProxyMode](#proxymode) ポリシーで '固定プロキシ サーバーを使用する' を選択した場合のみです。プロキシ ポリシーの構成で他のモードを選択した場合は、このポリシーを有効にしたり、構成したりしないでください。

このポリシーを有効にした場合、このポリシーによって構成されるプロキシ サーバーが、すべての URL に対して使用されます。

このポリシーを無効にした場合または構成しなかった場合、このプロキシ モード (固定プロキシ サーバーを使用する) のときに、ユーザーは独自のプロキシ設定を選択できます。プロキシ ポリシーの設定で他の方法を指定した場合は、このポリシーを構成しないでください。

その他のオプションや詳細な例については、[https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936) を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ProxyServer
  - GP の名前: プロキシ サーバーのアドレスまたは URL を構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/プロキシ サーバー
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ProxyServer
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"123.123.123.123:8080"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ProxyServer
  - サンプル値:
``` xml
<string>123.123.123.123:8080</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ProxySettings
  #### プロキシの設定
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge のプロキシ設定を構成します。

このポリシーを有効にした場合、Microsoft Edge では、コマンド ラインから指定したプロキシ関連のオプションがすべて無視されます。

このポリシーを設定しなかった場合、ユーザーは独自のプロキシ設定を選択できます。

このポリシーは、以下の各ポリシーをオーバーライドします。

[ProxyMode](#proxymode)
[ProxyPacUrl](#proxypacurl)
[ProxyServer](#proxyserver)
[ProxyBypassList](#proxybypasslist)

ProxyMode フィールドでは、Microsoft Edge で使用されるプロキシ サーバーを指定でき、ユーザーがプロキシ設定を変更できないようにします。

ProxyPacUrl フィールドには、プロキシ .pac ファイルへの URL を指定します。

ProxyServer フィールドには、プロキシ サーバーの URL を指定します。

ProxyBypassList フィールドには、Microsoft Edge がバイパスするプロキシ ホストのリストを指定します。

'ProxyMode' の値として 'direct' を選択した場合、プロキシは使用されず、他のフィールドはすべて無視されます。

'ProxyMode' の値として 'system' を選択した場合、システムのプロキシが使用され、他のフィールドはすべて無視されます。

'ProxyMode' の値として 'auto_detect' を選択した場合、他のフィールドはすべて無視されます。

'ProxyMode' の値として 'fixed_server' を選択した場合、'ProxyServer' フィールドと 'ProxyBypassList' フィールドが使用されます。

'ProxyMode' の値として 'pac_script' を選択した場合、'ProxyPacUrl' フィールドと 'ProxyBypassList' フィールドが使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 辞書

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ProxySettings
  - GP の名前: プロキシの設定
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/プロキシ サーバー
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ProxySettings
  - 値の種類: REG_SZ
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {
  "ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", 
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ProxySettings
  - サンプル値:
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
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ## 印刷 policies

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultPrinterSelection
  #### 既定のプリンターの選択規則
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge で通常使うプリンター選択規則よりも優先されます。このポリシーでは、ユーザーが初めてページを印刷しようとしたときに、Microsoft Edge で通常使うプリンターを選択するための規則を決定します。

このポリシーが構成されている場合、Microsoft Edge では、指定されたすべての属性に一致するプリンターの検索を試行し、そのプリンターを通常使うプリンターとして使用します。条件を満たすプリンターが複数ある場合は、最初に一致したプリンターが使用されます。

このポリシーを構成しない場合、またはタイムアウト期間内に一致するプリンターが見つからなかった場合は、既定のプリンターは組み込み PDF プリンターとなりますが、PDF プリンターが利用できない場合はプリンターなしになります。

この値は JSON オブジェクトとして解析され、次のスキーマに準拠します。{ "type": "object", "properties": { "idPattern": { "description": "Regular expression to match printer id.", "type": "string" }, "namePattern": { "description": "Regular expression to match printer display name.", "type": "string" } } }

フィールドを省略すると、すべての値が一致することになります。たとえば、接続を指定しない場合、印刷プレビューではすべての種類のローカル プリンターの検出を開始します。正規表現パターンは JavaScript RegExp 構文に従う必要があります。また、一致では大文字と小文字が区別されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultPrinterSelection
  - GP の名前: 既定のプリンターの選択規則
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/印刷
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DefaultPrinterSelection
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"{ \"idPattern\": \".*public\", \"namePattern\": \".*Color\" }"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultPrinterSelection
  - サンプル値:
``` xml
<string>{ "idPattern": ".*public", "namePattern": ".*Color" }</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PrintHeaderFooter
  #### ヘッダーとフッターを印刷する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  [印刷] ダイアログボックスで「ヘッダーとフッター」の入力をオンまたはオフにします。

このポリシーを構成しない場合は、ユーザーはヘッダーとフッターを印刷するかどうかを選択できます。

このポリシーを無効にした場合、ユーザーはヘッダーとフッターを印刷できません。

このポリシーを有効にした場合、ユーザーは常にヘッダーとフッターを印刷します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PrintHeaderFooter
  - GP の名前: ヘッダーとフッターを印刷する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/印刷
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/印刷
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: PrintHeaderFooter
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: PrintHeaderFooter
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PrintPreviewUseSystemDefaultPrinter
  #### システム既定のプリンターを通常使用するプリンターとして設定する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge に対して、[印刷プレビュー] で既定で選択されるプリンターとして、最近使用したプリンターではなく、システムの既定のプリンターを使用するように指示します。

このポリシーを無効にした場合または構成しなかった場合、[印刷プレビュー] では、最近使用したプリンターが既定の出力先として使用されます。

このポリシーを有効にした場合、[印刷プレビュー] では、OS のシステム既定のプリンターが既定の出力先として使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PrintPreviewUseSystemDefaultPrinter
  - GP の名前: システム既定のプリンターを通常使用するプリンターとして設定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/印刷
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/印刷
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: PrintPreviewUseSystemDefaultPrinter
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: PrintPreviewUseSystemDefaultPrinter
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PrintingEnabled
  #### 印刷を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge での印刷を有効にして、ユーザーがこの設定を変更できないようにします。

このポリシーを有効にした場合または構成しなかった場合、ユーザーは印刷することができます。

このポリシーを無効にした場合、ユーザーは Microsoft Edge から印刷できません。レンチ メニュー、拡張機能、JavaScript アプリケーションなどで印刷が無効になります。ただし、ユーザーは、印刷中に Microsoft Edge をバイパスするプラグインから印刷することができます。たとえば、Adobe Flash の一部のアプリケーションでは、コンテキスト メニューにこのポリシーが適用されない印刷オプションがあります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PrintingEnabled
  - GP の名前: 印刷を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/印刷
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: PrintingEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: PrintingEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PrintingPaperSizeDefault
  #### 既定の印刷ページ サイズ
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  既定の印刷ページ サイズを上書きします。

必要な用紙サイズがリストにない場合、name には、指定された形式の1つまたは ' custom ' が含まれている必要があります。' Custom ' 値が指定されている場合は custom_size プロパティを指定する必要があります。これは、必要な高さと幅をマイクロメートルで表します。それ以外の場合は custom_size プロパティを指定できません。これらの規則に違反するポリシーは無視されます。

ユーザーが選択したプリンターでページ サイズが利用できない場合、このポリシーは無視されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 辞書

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PrintingPaperSizeDefault
  - GP の名前: 既定の印刷ページ サイズ
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/印刷
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: PrintingPaperSizeDefault
  - 値の種類: REG_SZ
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\PrintingPaperSizeDefault = {
  "custom_size": {
    "height": 297000, 
    "width": 210000
  }, 
  "name": "custom"
}
```


  #### Mac の情報と設定
  - 優先されるキーの名前: PrintingPaperSizeDefault
  - サンプル値:
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
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### UseSystemPrintDialog
  #### システム印刷ダイアログを使用して印刷する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  印刷プレビューの代わりにシステムの印刷ダイアログを表示します。

このポリシーを有効にした場合、ユーザーがページを印刷するとき、Microsoft Edge では組み込みの印刷プレビューではなくシステムの印刷ダイアログを開きます。

このポリシーを構成しなかった場合または無効にした場合、印刷コマンドによって、Microsoft Edge の印刷プレビュー画面がトリガーされます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: UseSystemPrintDialog
  - GP の名前: システム印刷ダイアログを使用して印刷する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/印刷
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: UseSystemPrintDialog
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: UseSystemPrintDialog
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ## 拡張機能 policies

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ExtensionAllowedTypes
  #### 許可される拡張機能の種類を構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  インストールできる拡張機能の種類を制御し、ランタイム アクセスを制限します。

この設定では、許可される拡張機能の種類と、拡張機能とのやり取りができるホストを定義します。値は文字列のリストとして指定します。これらの文字列は、"extension"、"theme"、"user_script"、"hosted_app" のいずれかになります。これらの種類について詳しくは、Microsoft Edge の拡張機能に関するドキュメントをご覧ください。

このポリシーは、[ExtensionInstallForcelist](#extensioninstallforcelist) ポリシーを使用して強制的にインストールされる拡張機能にも影響します。

このポリシーを有効にした場合、リスト内の種類に一致する拡張機能のみがインストールされます。

このポリシーを構成しなかった場合、許可される拡張機能の種類に関する制限は適用されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ExtensionAllowedTypes
  - GP の名前: 許可される拡張機能の種類を構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/拡張機能
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes\1 = "hosted_app"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: ExtensionAllowedTypes
  - サンプル値:
``` xml
<array>
  <string>hosted_app</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ExtensionInstallAllowlist
  #### 特定の拡張機能のインストールを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  既定では、すべての拡張機能が許可されます。ただし、'ExtensionInstallBlockList' ポリシーを "*" に設定してすべての拡張機能をブロックすると、ユーザーがインストールできるのは、このポリシーに定義されている拡張機能のみになります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ExtensionInstallAllowlist
  - GP の名前: 特定の拡張機能のインストールを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/拡張機能
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\2 = "extension_id2"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: ExtensionInstallAllowlist
  - サンプル値:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ExtensionInstallBlocklist
  #### インストールできない拡張機能を制御する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザーが Microsoft Edge でインストールできない特定の拡張子を一覧表示します。このポリシーを導入すると、この一覧にある拡張子で既にインストールされているものはすべて無効になり、ユーザーは再度有効にすることができません。ブロックする拡張子の一覧からアイテムを削除すると、その拡張子は以前インストールされた場所で自動的に再度有効になります。

許可リストに明示的に指定されていないすべての拡張子をブロックするには、「*」を使用します。

このポリシーを設定しない場合、ユーザーは Microsoft Edge で任意の拡張子をインストールできます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ExtensionInstallBlocklist
  - GP の名前: インストールできない拡張機能を制御する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/拡張機能
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\2 = "extension_id2"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: ExtensionInstallBlocklist
  - サンプル値:
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ExtensionInstallForcelist
  #### サイレント インストールされる拡張機能を制御する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザーによる操作なしでサイレント インストールされる拡張機能を指定します。ユーザーは、これらの拡張機能をアンインストールしたり、無効にしたりすることはできません ("強制インストール")。拡張機能によって要求されるすべてのアクセス許可は、ユーザーが操作することなく暗黙的に付与されます。拡張機能の将来のバージョンによって要求される追加のアクセス許可も対象となります。また、アクセス許可は、enterprise.deviceAttributes 拡張機能 API や enterprise.platformKeys 拡張機能 API に対しても付与されます (これら 2 つの API は強制的にインストールされる拡張機能でのみ利用できます)。

このポリシーは、競合する可能性のある [ExtensionInstallBlocklist](#extensioninstallblocklist) ポリシーよりも優先されます。強制的にインストールされるリストから拡張機能を削除すると、その拡張機能は、Microsoft Edge によって自動的にアンインストールされます。

強制インストールは、次のいずれでもないインスタンスのMicrosoft EdgeアドオンWebサイトにリストされているアプリと拡張機能に限定されています: Microsoft Active Directoryドメインに参加している Windowsインスタンス、またはデバイス管理に登録されている Windows 10 Proまたは Enterpriseインスタンス、 MDM経由で管理されている、または MCX 経由でドメインに参加している MacOSインスタンス。

ただし、ユーザーは開発者ツールを使用することで、どの拡張機能のソース コードでも変更できます (その場合、拡張機能が機能しなくなることがあります)。このようなユーザーによる変更を禁止する場合は、[DeveloperToolsAvailability](#developertoolsavailability) ポリシーを設定してください。

以下の形式で拡張機能をリストに追加してください:

[extensionID];[updateURL]

- extensionID は 32 文字の文字列です。デベロッパー モードで edge://extensions を開くと確認できます。

- updateURL (省略可能) は、アプリや拡張機能の更新マニフェスト XML ドキュメントのアドレスです。[https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043) の説明をご覧ください。Chrome ウェブストアから拡張機能をインストールする場合は、Chrome ウェブストアの更新 URL https://clients2.google.com/service/update2/crx を指定します。このポリシーで設定された更新 URL は、初回のインストールでのみ使用され、その後の拡張機能の更新では、拡張機能のマニフェストで指定されている更新 URL が使用されます。updateURL を設定しなかった場合、拡張機能は Microsoft Store でホストされていると見なされて、次の更新 URL が使用されます: (https://edge.microsoft.com/extensionwebstorebase/v1/crx)

たとえば、gggmmkjegpiggikcnhidnjjhmicpibll;https://edge.microsoft.com/extensionwebstorebase/v1/crx では、Microsoft Store の "更新" URL から Microsoft Online アプリがインストールされます。拡張機能のホスティングについて詳しくは、[https://go.microsoft.com/fwlink/?linkid=2095044](https://go.microsoft.com/fwlink/?linkid=2095044) を参照してください。

このポリシーを構成しなかった場合、拡張機能は自動的にはインストールされず、ユーザーは Microsoft Edge のどの拡張機能でもアンインストールできます。

このポリシーは InPrivate モードには適用されないことに注意してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ExtensionInstallForcelist
  - GP の名前: サイレント インストールされる拡張機能を制御する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/拡張機能
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\1 = "gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\2 = "abcdefghijklmnopabcdefghijklmnop"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: ExtensionInstallForcelist
  - サンプル値:
``` xml
<array>
  <string>gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx</string>
  <string>abcdefghijklmnopabcdefghijklmnop</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ExtensionInstallSources
  #### 拡張機能およびユーザー スクリプトのインストール ソースを構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  拡張機能やテーマをインストールできる URL を定義します。

既定では、ユーザーはインストールする拡張機能やスクリプトそれぞれに対応した *.crx ファイルをダウンロードし、そのファイルを Microsoft Edge の設定ページにドラッグする必要があります。このポリシーでは、特定の URL を使用して、ユーザーに必要な拡張機能やスクリプトをインストールできるようにします。

このリストの各項目は、拡張機能スタイルの一致パターンに従っています ([https://go.microsoft.com/fwlink/?linkid=2095039](https://go.microsoft.com/fwlink/?linkid=2095039) を参照してください)。ユーザーは、このリストの項目に一致するどの URL からでも、アイテムを簡単にインストールできます。*.crx ファイルの場所およびダウンロードが開始されるページ (つまり、参照元) はどちらも、これらもパターンに基づいて許可されます。

[ExtensionInstallBlocklist](#extensioninstallblocklist) ポリシーは、このポリシーよりも優先されます。禁止リストで指定されている拡張機能は、このリストにあるサイトからの拡張機能であってもインストールされません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ExtensionInstallSources
  - GP の名前: 拡張機能およびユーザー スクリプトのインストール ソースを構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/拡張機能
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources\1 = "https://corp.contoso.com/*"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: ExtensionInstallSources
  - サンプル値:
``` xml
<array>
  <string>https://corp.contoso.com/*</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ExtensionSettings
  #### 拡張子の管理設定を構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge の拡張機能の管理設定を構成します。

このポリシーでは、拡張機能に関連する既存のポリシーで管理されている設定を含む、複数の設定を管理します。このポリシーとレガシ ポリシーの両方が設定されている場合は、このポリシーが優先されます。

このポリシーでは、拡張機能 ID または更新 URL をそれぞれの構成にマップします。拡張機能 ID を使用する場合、構成は特定の拡張機能にのみ適用されます。特別な ID "*" に対して既定の構成を設定すると、既定の構成が、このポリシーに明示されていないすべての拡張機能に適用されます。更新 URL を使用する場合、[https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043) で説明されているように、構成はこの拡張機能のマニフェストに示されている更新 URL を使用するすべての拡張機能に適用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 辞書

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ExtensionSettings
  - GP の名前: 拡張子の管理設定を構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/拡張機能
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ExtensionSettings
  - 値の種類: REG_SZ
  ##### サンプル値:
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


  #### Mac の情報と設定
  - 優先されるキーの名前: ExtensionSettings
  - サンプル値:
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
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ## 既定の検索プロバイダー policies

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultSearchProviderEnabled
  #### 既定の検索プロバイダーを有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  既定の検索プロバイダーを使用する機能を有効にします。

このポリシーを有効にした場合、ユーザーは、(入力する内容が URL でないかぎり) 用語をアドレス バーに入力して検索できます。

既定の検索ポリシーの残りの部分を有効にすることで、使用する既定の検索プロバイダーを指定できます。これらが空のまま (構成されていない) か正しく構成されていない場合、ユーザーは既定のプロバイダーを選択できます。

このポリシーを無効にした場合、ユーザーはアドレス バーから検索できません。

このポリシーを有効または無効にした場合、ユーザーはこのポリシーを変更したり、上書きしたりすることはできません。

このポリシーを構成しなかった場合、既定の検索プロバイダーが有効になり、ユーザーは既定の検索プロバイダーを選択して、検索プロバイダーの一覧を設定できます。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

Microsoft Edge 84 以降では、このポリシーを推奨ポリシーとして設定できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultSearchProviderEnabled
  - GP の名前: 既定の検索プロバイダーを有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/既定の検索プロバイダー
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/既定の検索プロバイダー
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: DefaultSearchProviderEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultSearchProviderEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultSearchProviderEncodings
  #### 既定の検索プロバイダーのエンコード
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  検索プロバイダーがサポートする文字エンコードを指定します。エンコーディングは、UTF-8、GB2312、ISO-8859-1 などのコード ページ名です。指定された順序で試行されます。

このポリシーはオプションです。構成されていない場合、デフォルトのUTF-8が使用されます。

このポリシーは、[DefaultSearchProviderEnabled](#defaultsearchproviderenabled) および [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) ポリシーを有効にした場合にのみ適用されます。

Microsoft Edge 84 以降では、このポリシーを推奨ポリシーとして設定できます。ユーザーが既に既定の検索プロバイダーを設定している場合、この推奨ポリシーで構成された既定の検索プロバイダーは、ユーザーが選択できる検索プロバイダーのリストに追加されません。これが望ましい動作である場合は、[ManagedSearchEngines](#managedsearchengines) ポリシーを使用します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultSearchProviderEncodings
  - GP の名前: 既定の検索プロバイダーのエンコード
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/既定の検索プロバイダー
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/既定の検索プロバイダー
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ\DefaultSearchProviderEncodings
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\1 = "UTF-8"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\2 = "UTF-16"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\3 = "GB2312"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\4 = "ISO-8859-1"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultSearchProviderEncodings
  - サンプル値:
``` xml
<array>
  <string>UTF-8</string>
  <string>UTF-16</string>
  <string>GB2312</string>
  <string>ISO-8859-1</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultSearchProviderImageURL
  #### 既定の検索プロバイダーの画像検索を指定する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  画像検索に使用する検索エンジンの URL を指定します。検索要求は GET メソッドを使用して送信されます。

このポリシーは省略可能です。このポリシーを構成しなかった場合、画像検索を利用することはできません。

Bing の画像検索 URL は次のように指定します。
'{bing:baseURL}images/detail/search?iss=sbiupload&FORM=ANCMS1#enterInsights'。

Google の画像検索 URL は、'{google:baseURL}searchbyimage/upload' のように指定します。

画像検索の構成を完了するには、[DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams) ポリシーを参照してください。

このポリシーは、[DefaultSearchProviderEnabled](#defaultsearchproviderenabled) ポリシーと [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) ポリシーを有効にした場合にのみ適用されます。

Microsoft Edge 84 以降では、このポリシーを推奨ポリシーとして設定できます。ユーザーが既に既定の検索プロバイダーを設定している場合、この推奨ポリシーで構成された既定の検索プロバイダーは、ユーザーが選択できる検索プロバイダーのリストに追加されません。これが望ましい動作である場合は、[ManagedSearchEngines](#managedsearchengines) ポリシーを使用します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultSearchProviderImageURL
  - GP の名前: 既定の検索プロバイダーの画像検索を指定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/既定の検索プロバイダー
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/既定の検索プロバイダー
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: DefaultSearchProviderImageURL
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"https://search.contoso.com/searchbyimage/upload"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultSearchProviderImageURL
  - サンプル値:
``` xml
<string>https://search.contoso.com/searchbyimage/upload</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultSearchProviderImageURLPostParams
  #### POST を使用する画像の URL のパラメーター
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  このポリシーを有効にした場合、POST を使った画像検索の実行時に使用するパラメーターが指定されます。このポリシーには、コンマで区切られた名前と値のペアが含まれます。値がテンプレート パラメーター (上記の例の {imageThumbnail} など) の場合は、実際の画像サムネイルのデータに置き換えられます。このポリシーは、[DefaultSearchProviderEnabled](#defaultsearchproviderenabled) ポリシーと [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) ポリシーを有効にした場合にのみ適用されます。

Bing の画像検索 URL の POST パラメーターは次のように指定します。
'imageBin={google:imageThumbnailBase64}'。

Google の画像検索 URL の POST パラメーターは次のように指定します。
'encoded_image={google:imageThumbnail},image_url={google:imageURL},sbisrc={google:imageSearchSource},original_width={google:imageOriginalWidth},original_height={google:imageOriginalHeight}'。

このポリシーを設定しなかった場合、画像検索要求は GET メソッドを使用して送信されます。

Microsoft Edge 84 以降では、このポリシーを推奨ポリシーとして設定できます。ユーザーが既に既定の検索プロバイダーを設定している場合、この推奨ポリシーで構成された既定の検索プロバイダーは、ユーザーが選択できる検索プロバイダーのリストに追加されません。これが望ましい動作である場合は、[ManagedSearchEngines](#managedsearchengines) ポリシーを使用します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultSearchProviderImageURLPostParams
  - GP の名前: POST を使用する画像の URL のパラメーター
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/既定の検索プロバイダー
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/既定の検索プロバイダー
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: DefaultSearchProviderImageURLPostParams
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"content={imageThumbnail},url={imageURL},sbisrc={SearchSource}"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultSearchProviderImageURLPostParams
  - サンプル値:
``` xml
<string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultSearchProviderKeyword
  #### 既定の検索プロバイダーのキーワード
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  このプロバイダーの検索をトリガーするためにアドレス バーで使用されるショートカットであるキーワードを指定します。

このポリシーはオプションです。構成しない場合、キーワードによって検索プロバイダーがアクティブ化されません。

このポリシーは、[DefaultSearchProviderEnabled](#defaultsearchproviderenabled) および [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) ポリシーを有効にした場合にのみ適用されます。

Microsoft Edge 84 以降では、このポリシーを推奨ポリシーとして設定できます。ユーザーが既に既定の検索プロバイダーを設定している場合、この推奨ポリシーで構成された既定の検索プロバイダーは、ユーザーが選択できる検索プロバイダーのリストに追加されません。これが望ましい動作である場合は、[ManagedSearchEngines](#managedsearchengines) ポリシーを使用します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultSearchProviderKeyword
  - GP の名前: 既定の検索プロバイダーのキーワード
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/既定の検索プロバイダー
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/既定の検索プロバイダー
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: DefaultSearchProviderKeyword
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"mis"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultSearchProviderKeyword
  - サンプル値:
``` xml
<string>mis</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultSearchProviderName
  #### 既定の検索プロバイダーの名前
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  既定の検索プロバイダーの名前を指定します。

このポリシーを有効にした場合、既定の検索プロバイダーの名前を設定します。

このポリシーを有効にしなかった場合または空白のままにした場合、検索 URL で指定されたホスト名が使用されます。

'DefaultSearchProviderName' は、組織で承認されている暗号化された検索プロバイダーに設定する必要があります。これは、DTBC-0008 で設定されている暗号化された検索プロバイダーに対応します。このポリシーは、[DefaultSearchProviderEnabled](#defaultsearchproviderenabled) ポリシーと [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) ポリシーが有効になっている場合にのみ適用されます。

Microsoft Edge 84 以降では、このポリシーを推奨ポリシーとして設定できます。ユーザーが既に既定の検索プロバイダーを設定している場合、この推奨ポリシーで構成された既定の検索プロバイダーは、ユーザーが選択できる検索プロバイダーのリストに追加されません。これが望ましい動作である場合は、[ManagedSearchEngines](#managedsearchengines) ポリシーを使用します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultSearchProviderName
  - GP の名前: 既定の検索プロバイダーの名前
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/既定の検索プロバイダー
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/既定の検索プロバイダー
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: DefaultSearchProviderName
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"My Intranet Search"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultSearchProviderName
  - サンプル値:
``` xml
<string>My Intranet Search</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultSearchProviderSearchURL
  #### 既定の検索プロバイダーの検索 URL
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  既定の検索で使用する検索エンジンの URL を指定します。URL には、文字列 '{searchTerms}' を含めます。クエリの実行時、この文字列はユーザーが検索する用語に置き換えられます。

Bing の検索 URL は次のように指定します。

'{bing:baseURL}search?q={searchTerms}'

Google の検索 URL は、'{google:baseURL}search?q={searchTerms}&{google:RLZ}{google:originalQueryForSuggestion}{google:assistedQueryStats}{google:searchFieldtrialParameter}{google:searchClient}{google:sourceId}ie={inputEncoding}' のように指定します。

このポリシーは、[DefaultSearchProviderEnabled](#defaultsearchproviderenabled) ポリシーを有効にした場合に必要となります。'DefaultSearchProviderEnabled' ポリシーを有効にしなかった場合、このポリシーは無視されます。

Microsoft Edge 84 以降では、このポリシーを推奨ポリシーとして設定できます。ユーザーが既に既定の検索プロバイダーを設定している場合、この推奨ポリシーで構成された既定の検索プロバイダーは、ユーザーが選択できる検索プロバイダーのリストに追加されません。これが望ましい動作である場合は、[ManagedSearchEngines](#managedsearchengines) ポリシーを使用します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultSearchProviderSearchURL
  - GP の名前: 既定の検索プロバイダーの検索 URL
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/既定の検索プロバイダー
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/既定の検索プロバイダー
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: DefaultSearchProviderSearchURL
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"https://search.contoso.com/search?q={searchTerms}"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultSearchProviderSearchURL
  - サンプル値:
``` xml
<string>https://search.contoso.com/search?q={searchTerms}</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultSearchProviderSuggestURL
  #### 検索候補を使用するための既定の検索プロバイダーの URL
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  検索候補の表示に使用する検索エンジンの URL を指定します。URL には文字列 '{searchTerms}' を含めます。クエリの実行時、この文字列はユーザーがこれまで入力したテキストに置き換えられます。

このポリシーは省略可能です。このポリシーを構成しなかった場合、ユーザーには検索候補は表示されません。閲覧の履歴とお気に入りに基づく候補が表示されます。

Bing での検索候補の URL は次のように指定できます。

'{bing:baseURL}qbox?query={searchTerms}'

Google での検索候補の URL は、'{google:baseURL}complete/search?output=chrome&q={searchTerms}' のように指定できます。

このポリシーは、[DefaultSearchProviderEnabled](#defaultsearchproviderenabled) ポリシーと [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) ポリシーを有効にした場合にのみ適用されます。

Microsoft Edge 84 以降では、このポリシーを推奨ポリシーとして設定できます。ユーザーが既に既定の検索プロバイダーを設定している場合、この推奨ポリシーで構成された既定の検索プロバイダーは、ユーザーが選択できる検索プロバイダーのリストに追加されません。これが望ましい動作である場合は、[ManagedSearchEngines](#managedsearchengines) ポリシーを使用します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultSearchProviderSuggestURL
  - GP の名前: 検索候補を使用するための既定の検索プロバイダーの URL
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/既定の検索プロバイダー
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/既定の検索プロバイダー
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: DefaultSearchProviderSuggestURL
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"https://search.contoso.com/suggest?q={searchTerms}"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultSearchProviderSuggestURL
  - サンプル値:
``` xml
<string>https://search.contoso.com/suggest?q={searchTerms}</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NewTabPageSearchBox
  #### 新しいタブページの検索ボックスエクスペリエンスを構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 85

  #### 説明
  新しいタブ ページの検索ボックスを構成して、「検索ボックス (推奨)」または「アドレス バー」を使用して新しいタブを検索できます。このポリシーは、[DefaultSearchProviderEnabled](#defaultsearchproviderenabled) と [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) の 2 つのポリシーを設定して、検索エンジンを Bing 以外の値に設定した場合にのみ機能します。

 このポリシーを無効にするか、構成しない場合:

- アドレス バーの既定の検索エンジンが Bing の場合、新しいタブ ページは検索ボックスを使用して新しいタブを検索します。
- アドレス バーの既定の検索エンジンが Bing でない場合、ユーザーは新しいタブで検索するときに追加の選択肢 (「アドレス バー」を使用) を提供されます。


このポリシーを有効にして次のように設定した場合:

- 「検索ボックス (推奨)」(「bing」) の新しいタブ ページは検索ボックスを使用して新しいタブを検索します。
- 「アドレス バー」(「リダイレクト」) の新しいタブ ページの検索ボックスはアドレス バーを使用して新しいタブを検索します。

ポリシー オプションのマッピング:

* bing (bing) = 検索ボックス (推奨)

* redirect (redirect) = アドレス バー

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: NewTabPageSearchBox
  - GP の名前: 新しいタブページの検索ボックスエクスペリエンスを構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/既定の検索プロバイダー
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/既定の検索プロバイダー
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: NewTabPageSearchBox
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"bing"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: NewTabPageSearchBox
  - サンプル値:
``` xml
<string>bing</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ## Additional policies

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AddressBarMicrosoftSearchInBingProviderEnabled
  #### アドレス バーの Bing 候補で Microsoft Search を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 81

  #### 説明
  ユーザーがアドレス バーで検索文字列を入力したとき、アドレス バーの候補リストに示される Bing 候補で、関連する Microsoft Search の表示を有効にします。このポリシーを有効にした場合または構成しなかった場合、Microsoft Edge のアドレス バーの候補リストに示される Bing 候補では、Microsoft Search によって実行された内部検索の結果を表示できます。Bing の検索結果で Microsoft Search を表示するには、ユーザーは、組織の Azure AD アカウントを使用して Microsoft Edge にサインインしている必要があります。
このポリシーを無効にした場合、Microsoft Edge のアドレス バーの候補リストには、内部検索の結果を表示することはできません。
既定の検索プロバイダー ([DefaultSearchProviderEnabled](#defaultsearchproviderenabled)、[DefaultSearchProviderName](#defaultsearchprovidername)、および [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)) を適用する一連のポリシーが有効になっており、指定された検索プロバイダーが Bing 以外の場合、このポリシーは適用されず、アドレス バーの候補リストに示される Bing 候補には Microsoft Search は表示されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AddressBarMicrosoftSearchInBingProviderEnabled
  - GP の名前: アドレス バーの Bing 候補で Microsoft Search を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AddressBarMicrosoftSearchInBingProviderEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AddressBarMicrosoftSearchInBingProviderEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AdsSettingForIntrusiveAdsSites
  #### 押し付けがましい広告を表示するサイトに対する広告の設定
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 78

  #### 説明
  煩わしい広告のあるサイトで広告をブロックするかどうかを制御します。

ポリシー オプションのマッピング:

* AllowAds (1) = すべてのサイトで広告を許可する

* BlockAds (2) = 押し付けがましい広告を表示するサイトで広告をブロックする (既定値)

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AdsSettingForIntrusiveAdsSites
  - GP の名前: 押し付けがましい広告を表示するサイトに対する広告の設定
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AdsSettingForIntrusiveAdsSites
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AdsSettingForIntrusiveAdsSites
  - サンプル値:
``` xml
<integer>1</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AllowDeletingBrowserHistory
  #### ブラウザーとダウンロードの履歴の削除を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ブラウザーの履歴とダウンロードの履歴の削除を有効にして、ユーザーがこの設定を変更できないようにします。

このポリシーを無効にしても、閲覧とダウンロードの履歴が保持されることは保証されない点に注意してください。ユーザーは履歴データベースのファイルを直接編集または削除できます。またブラウザー自体が、任意のまたはすべての履歴項目をいつでも削除 (有効期限に基づいて削除) したり、アーカイブしたりすることができます。

このポリシーを有効にした場合または構成しなかった場合、ユーザーは閲覧とダウンロードの履歴を削除できます。

このポリシーを無効にした場合、ユーザーは閲覧とダウンロードの履歴を削除できません。

このポリシーを有効にした場合、[ClearBrowsingDataOnExit](#clearbrowsingdataonexit) ポリシーを有効にしないでください。これは、両方でデータの削除を処理することになるためです。両方を有効にした場合、[ClearBrowsingDataOnExit](#clearbrowsingdataonexit) ポリシーが優先され、Microsoft Edge を終了したときに、このポリシーの構成方法に関係なく、すべてのデータが削除されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AllowDeletingBrowserHistory
  - GP の名前: ブラウザーとダウンロードの履歴の削除を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AllowDeletingBrowserHistory
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AllowDeletingBrowserHistory
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AllowFileSelectionDialogs
  #### ファイルの選択ダイアログを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge でファイル選択ダイアログを表示できるようにすることで、ローカル ファイルへのアクセスを許可します。

このポリシーを有効にした場合または構成しなかった場合は、ユーザーは通常どおりにファイル選択ダイアログを開くことができます。

このポリシーを無効にした場合、ファイル選択ダイアログをトリガーする操作 (お気に入りのインポート、ファイルのアップロード、リンクの保存など) をユーザーが実行したとき、操作が実行される代わりにメッセージが常に表示され、ユーザーはファイル選択ダイアログで [キャンセル] をクリックしたと見なされます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AllowFileSelectionDialogs
  - GP の名前: ファイルの選択ダイアログを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AllowFileSelectionDialogs
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AllowFileSelectionDialogs
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AllowPopupsDuringPageUnload
  #### ページのアンロード中にポップアップの表示を許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 78

  #### 説明
  このポリシーを使用すると、管理者は、ページのアンロード中にページにポップアップが表示されるよう指定できます。

このポリシーを有効に設定した場合、ページをアンロードしているときに、ページにポップアップを表示することができます。

このポリシーを無効に設定した場合または設定しなかった場合、ページをアンロードしているときに、ページにポップアップを表示することはできません。これは、仕様 (https://html.spec.whatwg.org/#apis-for-creating-and-navigating-browsing-contexts-by-name) に従うためです。

このポリシーは将来削除される予定です。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AllowPopupsDuringPageUnload
  - GP の名前: ページのアンロード中にポップアップの表示を許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AllowPopupsDuringPageUnload
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AllowPopupsDuringPageUnload
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AllowSurfGame
  #### サーフィン ゲームを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 83

  #### 説明
  このポリシーを無効にした場合、デバイスがオフラインのとき、またはユーザーが edge://surf に移動したときに、ユーザーはサーフィン ゲームをプレイできなくなります。

このポリシーを有効にした場合または構成しなかった場合、ユーザーはサーフィン ゲームをプレイできます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AllowSurfGame
  - GP の名前: サーフィン ゲームを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AllowSurfGame
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AllowSurfGame
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AllowSyncXHRInPageDismissal
  #### ページを閉じるときにページで同期 XHR 要求を送信することを許可する (非推奨)
  >非推奨: このポリシーは推奨されていません。現在サポートされていますが、将来のリリースでは使用されなくなります。
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 79

  #### 説明
  このポリシーは、ページ削除中に同期 XHR 要求を拒否する変更と互換性がないことが判明した場合に、企業が Web コンテンツを更新する時間を増やすための短期的なメカニズムとしてのみ使用されるため、廃止されました。バージョン 88 になると Microsoft Edge では動作しません。

このポリシーでは、ページ削除中にページが同期 XHR 要求を送信できるように指定できます。

このポリシーを無効にすると、ページ削除中にページが同期 XHR 要求を送信できます。

このポリシーを無効にした場合、またはこのポリシーを構成しない場合、ページ削除中にページが同期 XHR 要求を送信できません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AllowSyncXHRInPageDismissal
  - GP の名前: ページを閉じるときにページで同期 XHR 要求を送信することを許可する (非推奨)
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AllowSyncXHRInPageDismissal
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AllowSyncXHRInPageDismissal
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AllowTokenBindingForUrls
  #### Microsoft Edge によってトークンのバインドの確立が試行されるサイトの一覧を構成します。
  
  
  #### サポートされているバージョン:
  - Windows 以降の 83

  #### 説明
  ブラウザーが
を使用して Token Binding プロトコルを実行するサイトの URL パターンのリストを構成します。      このリストのドメインについては、ブラウザーは TLS ハンドシェイクの Token Binding ClientHello を送信します (https://tools.ietf.org/html/rfc8472 を参照してください)。
     サーバーが有効な ServerHello 応答を使って応答した場合、ブラウザーは、その後の https 要求で Token Binding メッセージを作成し送信します。詳細については、https://tools.ietf.org/html/rfc8471 を参照してください。

     リストが空である場合、Token Binding は無効になります。

     このポリシーは、仮想保護モード機能に対応する Windows 10 デバイスでのみ使用可能です。

     Microsoft Edge 86 以降、このポリシーでは動的な更新はサポートされなくなりました。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AllowTokenBindingForUrls
  - GP の名前: Microsoft Edge によってトークンのバインドの確立が試行されるサイトの一覧を構成します。
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\2 = "[*.]mydomain2.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\3 = "[*.].mydomain2.com"

```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AllowTrackingForUrls
  #### 特定のサイトの追跡防止の例外を構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 78

  #### 説明
  追跡防止の対象外とする URL パターンの一覧を構成します。

このポリシーを構成した場合、構成された URL パターンの一覧が追跡防止から除外されます。

このポリシーを構成しなかった場合、すべてのサイトで、"ユーザーの Web 閲覧アクティビティの追跡をブロックする" ポリシーのグローバル デフォルト値 (設定されている場合)、またはユーザーの個人用の構成が使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AllowTrackingForUrls
  - GP の名前: 特定のサイトの追跡防止の例外を構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: AllowTrackingForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AlternateErrorPagesEnabled
  #### Web ページが見つからない場合に類似したページを提示する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 80

  #### 説明
  Microsoft Edge で、Web サービスへの接続を発行し、DNS エラーなどの接続の問題に対処するための URL の生成や候補となるページの検索を実行できるようにします。

このポリシーを有効にした場合、Web サービスを使用して、ネットワーク エラーに対処するための URL の生成や候補となるページの検索が実行されます。

このポリシーを無効にした場合、Web サービスへの呼び出しは行われず、標準のエラーページが表示されます。

このポリシーを構成しなかった場合、Microsoft Edge では、edge://settings/privacy のサービスで設定されているユーザー設定に従います。
具体的には **Web ページが見つからない場合に類似のページを提案する** というトグルが使用されます。ユーザーはこのトグルのオン/オフを切り替えることができます。このポリシー (AlternateErrorPagesEnabled) を有効にした場合、[Web ページが見つからない場合に類似のページを提案する] の設定がオンになりますが、ユーザーはこのトグルを使用して設定を変更することができなくなります。このポリシーを無効にした場合は、[Web ページが見つからない場合に類似のページを提案する] の設定がオフになり、この場合もユーザーはこのトグルを使用して設定を変更することができなくなります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AlternateErrorPagesEnabled
  - GP の名前: Web ページが見つからない場合に類似したページを提示する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: AlternateErrorPagesEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AlternateErrorPagesEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AlwaysOpenPdfExternally
  #### PDF ファイルを常に外部で開く
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge の内部 PDF ビューアーを無効にします。

このポリシーを有効にした場合、Microsoft Edge では PDF ファイルがダウンロードとして扱われ、ユーザーは既定のアプリケーションでそれらのファイルを開くことができます。

このポリシーを構成しなかった場合、または無効にした場合は、Microsoft Edge は、(ユーザーが無効にしない限り) PDF ファイルを開きます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AlwaysOpenPdfExternally
  - GP の名前: PDF ファイルを常に外部で開く
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AlwaysOpenPdfExternally
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AlwaysOpenPdfExternally
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AmbientAuthenticationInPrivateModesEnabled
  #### InPrivate プロファイルとゲスト プロファイルに対してアンビエント認証を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 81

  #### 説明
  このポリシーを構成した場合、Microsoft Edge での InPrivate プロファイルとゲスト プロファイルに対してアンビエント認証を許可/禁止することができます。

アンビエント認証とは、NTLM/Kerberos/Negotiate のチャレンジ/レスポンス スキームを介して明示的な資格情報が指定されていない場合に適用される、既定の資格情報を持つ HTTP 認証です。

ポリシーを「RegularOnly」に設定すると、標準のセッションでのみアンビエント認証が許可されます。InPrivate セッションとゲスト セッションではアンビエント認証は許可されません。

ポリシーを「InPrivateAndRegular」に設定すると、InPrivate セッションと標準のセッションでアンビエント認証が許可されます。ゲスト セッションではアンビエント認証は許可されません。

ポリシーを「GuestAndRegular」に設定すると、ゲスト セッションと標準のセッションでアンビエント認証が許可されます。InPrivate セッションではアンビエント認証は許可されません。

ポリシーを「All」に設定すると、すべてのセッションでアンビエント認証が許可されます。

標準のプロファイルでは常にアンビエント認証が許可されます。

Microsoft Edge バージョン 81 以降では、このポリシーを設定しなかった場合、標準のセッションでのみアンビエント認証が有効になります。

ポリシー オプションのマッピング:

* RegularOnly (0) = 標準のセッションでのみアンビエント認証を有効にする

* InPrivateAndRegular (1) = InPrivate セッションと標準のセッションでアンビエント認証を有効にする

* GuestAndRegular (2) = ゲスト セッションと標準のセッションでアンビエント認証を有効にする

* All (3) = 標準のセッション、InPrivate セッション、ゲスト セッションでアンビエント認証を有効にする

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AmbientAuthenticationInPrivateModesEnabled
  - GP の名前: InPrivate プロファイルとゲスト プロファイルに対してアンビエント認証を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AmbientAuthenticationInPrivateModesEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AmbientAuthenticationInPrivateModesEnabled
  - サンプル値:
``` xml
<integer>0</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AppCacheForceEnabled
  #### 既定でオフになっている場合でも、AppCache 機能を再度有効にすることができます
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 84

  #### 説明
  このポリシーを true に設定すると、Microsoft Edge の AppCache が既定で使用できない場合でも、AppCache が有効になります。

このポリシーを false に設定するか、または設定しない場合、AppCache は Microsoft Edge の既定に従います。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AppCacheForceEnabled
  - GP の名前: 既定でオフになっている場合でも、AppCache 機能を再度有効にすることができます
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AppCacheForceEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AppCacheForceEnabled
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ApplicationLocaleValue
  #### アプリケーションのロケールを設定する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 77

  #### 説明
  Microsoft Edge のアプリケーション ロケールを構成し、ユーザーがロケールを変更できないようにします。

このポリシーを有効にした場合、Microsoft Edge では指定されたロケールが使用されます。構成したロケールがサポートされていない場合、代わりに 'en-US' が使用されます。

この設定を無効にした場合または構成しなかった場合、Microsoft Edge では、ユーザー指定の優先されるロケール (構成されている場合)、または代替のロケール 'en-US' が使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ApplicationLocaleValue
  - GP の名前: アプリケーションのロケールを設定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: ApplicationLocaleValue
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"en"
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AudioCaptureAllowed
  #### オーディオ キャプチャを許可または禁止する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  オーディオ キャプチャ デバイスへの Web サイト アクセスの許可をユーザーに確認するかどうかを設定できます。このポリシーは、[AudioCaptureAllowedUrls](#audiocaptureallowedurls) のリストで構成されている URL を除くすべての URL に適用されます。

このポリシーを有効にした場合または構成しなかった場合 (既定の設定)、ユーザーは、[AudioCaptureAllowedUrls](#audiocaptureallowedurls) のリストに含まれていない URL からのオーディオ キャプチャへのアクセスを許可するように求められます。このリストに含まれている URL については、ユーザーへの確認なしでアクセスが許可されます。

この設定を無効にした場合、ユーザーへの確認は行われず、オーディオ キャプチャにアクセスできるのは、[AudioCaptureAllowedUrls](#audiocaptureallowedurls) で構成されている URL からのみになります。

このポリシーは、内蔵マイクだけでなく、すべての種類のオーディオ入力に影響します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AudioCaptureAllowed
  - GP の名前: オーディオ キャプチャを許可または禁止する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AudioCaptureAllowed
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AudioCaptureAllowed
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AudioCaptureAllowedUrls
  #### アクセス許可を要求しなくてもオーディオ キャプチャ デバイスにアクセスできるサイト
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザーに対してアクセス許可を要求しなくてもオーディオ キャプチャ デバイスを使用できる Web サイトを、URL パターンに基づいて定義します。このリスト内のパターンは、要求元 URL のセキュリティ オリジンと照合されます。パターンが一致すると、サイトに対して、オーディオ キャプチャ デバイスへのアクセスが自動的に許可されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AudioCaptureAllowedUrls
  - GP の名前: アクセス許可を要求しなくてもオーディオ キャプチャ デバイスにアクセスできるサイト
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: AudioCaptureAllowedUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AudioSandboxEnabled
  #### オーディオ サンドボックスの実行を許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 81

  #### 説明
  このポリシーでは、オーディオ処理のサンドボックスを制御します。

このポリシーを有効にした場合、オーディオ処理がサンドボックス化されます。

このポリシーを無効にした場合、オーディオ処理はサンドボックス化されず、レンダラー処理では WebRTC オーディオ処理モジュールが実行されます。
この場合、サンドボックス化されていないオーディオ サブシステムの実行に関連して、ユーザーがセキュリティ上のリスクにさらされることになります。

このポリシーを構成しなかった場合、オーディオ サンドボックスに関する既定の設定が使用されます。既定の設定はプラットフォームごとに異なる場合があります。

このポリシーの目的は、企業が使用するセキュリティ ソフトウェアの設定がサンドボックスを妨げる場合に、企業がオーディオ サンドボックスを柔軟に無効化できるようにすることです。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AudioSandboxEnabled
  - GP の名前: オーディオ サンドボックスの実行を許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AudioSandboxEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AudioSandboxEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AutoImportAtFirstRun
  #### 初回実行時に別のブラウザーのデータと設定を自動的にインポートする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  このポリシーを有効にすると、指定したブラウザーからサポートされているすべてのデータ型と設定が、最初の実行時にサイレントで自動的にインポートされます。最初の実行エクスペリエンスで、インポート セクションもスキップされます。

Microsoft Edge 従来版からのブラウザー データは、このポリシーの値に関係なく、初回実行時に常に通知なしで移行されます。

このポリシーが「FromDefaultBrowser」に設定されている場合、管理対象デバイスの既定ブラウザーに対応するデータ型がインポートされます。

このポリシーの値で指定されているブラウザーがマネージド デバイスにない場合、Microsoft Edge では、ユーザーに通知することなくインポートがスキップされます。

このポリシーを「DisabledAutoImport」に設定した場合、初回実行エクスペリエンスのインポート セクションがすべてスキップされ、Microsoft Edge では、ブラウザー データや設定が自動的にインポートされなくなります。

このポリシーの値を「FromInternetExplorer」に設定した場合、以下のデータ型が Internet Explorer からインポートされます。
1. お気に入りまたはブックマーク
2. 保存されたパスワード
3. 検索エンジン
4. 閲覧の履歴
5. ホーム ページ

このポリシーの値を「FromGoogleChrome」に設定した場合、以下のデータ型が Google Chrome からインポートされます。
1. お気に入り
2. 保存されたパスワード
3. 住所など
4. 支払い情報
5. 閲覧の履歴
6. 設定
7. ピン留めされたタブと開いているタブ
8. 拡張機能
9. Cookie

Google Chrome からインポートされるものの詳細については、[https://go.microsoft.com/fwlink/?linkid=2120835](https://go.microsoft.com/fwlink/?linkid=2120835) を参照してください。

このポリシーが「FromSafari」の値に設定されている場合、ユーザー データは Microsoft Edge にインポートされなくなります。これは、Mac でのフル ディスク アクセスの動作方法によるものです。
macOS Mojave 以降では、Microsoft Edge への Safari データの自動無人インポートはできなくなりました。

Microsoft Edge バージョン 83 以降、このポリシーが「FromMozillaFirefox」の値に設定されている場合、次のデータ型が Mozilla Firefox からインポートされます。
1. お気に入りまたはブックマーク
2. 保存されたパスワード
3. アドレスなど
4. 閲覧の履歴

特定のデータ型をマネージド デバイスからインポートされるように制限する場合は、このポリシーを別のポリシー ([ImportAutofillFormData](#importautofillformdata)、[ImportBrowserSettings](#importbrowsersettings)、[ImportFavorites](#importfavorites) など) と共に使用してください。

ポリシー オプションのマッピング:

* FromDefaultBrowser (0) = サポートされているすべてのデータ型と設定を既定のブラウザーから自動的にインポートする

* FromInternetExplorer (1) = サポートされているすべてのデータ型と設定を Internet Explorer から自動的にインポートする

* FromGoogleChrome (2) = サポートされているすべてのデータ型と設定を Google Chrome から自動的にインポートする

* FromSafari (3) = サポートされているすべてのデータ型と設定を Safari から自動的にインポートする

* DisabledAutoImport (4) = 自動インポートを無効にし、初回実行エクスペリエンスのインポート セクションをスキップする

* FromMozillaFirefox (5) = サポートされているすべてのデータ型と設定を Mozilla Firefox から自動的にインポートする

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AutoImportAtFirstRun
  - GP の名前: 初回実行時に別のブラウザーのデータと設定を自動的にインポートする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AutoImportAtFirstRun
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AutoImportAtFirstRun
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AutoLaunchProtocolsFromOrigins
  #### ユーザーにメッセージを表示せずに、一覧表示された元の場所から外部アプリケーションを起動できるプロトコルの一覧を定義します。
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 85

  #### 説明
  プロトコルの一覧を設定したり、ユーザーにメッセージを表示せずに外部アプリケーションを起動できる、関連付けられた送信元パターンの一覧を各プロトコルに設定したりできます。プロトコルの一覧を表示するときは、末尾の区切り記号を含めないでください。たとえば、"skype:" や "skype://" ではなく、"skype" と表示します。

このポリシーを構成した場合、次の場合にポリシーによってメッセージを表示せずに、外部アプリケーションの起動のみが許可されます。

- プロトコルが一覧表示されている場合

- プロトコルを起動しようとしているサイトの元の場所が、そのプロトコルの allowed_origins 一覧にある元の場所のパターンのいずれかと一致している場合。

いずれかの条件が false の場合、外部プロトコル起動プロンプトはポリシーによって省略されません。

このポリシーを構成しなかった場合、メッセージを表示せずにプロトコルを起動することはできません。ユーザーは、[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox) ポリシーが無効に設定されていない限り、プロトコル/サイトごとにプロンプトを表示しないように設定できます。このポリシーは、ユーザーが設定したプロトコルごとの例外、またはサイトごとのプロンプトの除外には影響しません。

元の場所の一致パターンは、[URLBlocklist](#urlblocklist) ポリシーの場合と同様の形式を使用します。これは、[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) で説明されています。

ただし、このポリシーの元の一致パターンには、"/path" または "@query" 要素を含めることはできません。"/Path" または "@query" 要素を含むパターンはすべて無視されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 辞書

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AutoLaunchProtocolsFromOrigins
  - GP の名前: ユーザーにメッセージを表示せずに、一覧表示された元の場所から外部アプリケーションを起動できるプロトコルの一覧を定義します。
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AutoLaunchProtocolsFromOrigins
  - 値の種類: REG_SZ
  ##### サンプル値:
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


  #### Mac の情報と設定
  - 優先されるキーの名前: AutoLaunchProtocolsFromOrigins
  - サンプル値:
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
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AutoOpenAllowedForURLs
  #### AutoOpenFileTypes を適用できる URL
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 85

  #### 説明
  [AutoOpenFileTypes](#autoopenfiletypes) が適用される URL のリストです。このポリシーは、ダウンロード シェルフの... > [常にこの種類のファイルを開く] メニュー エントリを介してユーザーが設定した値を自動的に開くことには影響しません。

このポリシーで URL を設定すると、URL がこのセットの一部であり、ファイルの種類が [AutoOpenFileTypes](#autoopenfiletypes) にリストされている場合にのみ、ポリシーによってファイルが自動的に開きます。いずれかの条件が偽の場合、ダウンロードはポリシーによって自動的に開かれません。

このポリシーを設定しない場合、ファイルの種類が [AutoOpenFileTypes](#autoopenfiletypes) であるすべてのダウンロードが自動的に開かれます。

URL パターンは、[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) に従ってフォーマットする必要があります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AutoOpenAllowedForURLs
  - GP の名前: AutoOpenFileTypes を適用できる URL
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\1 = "example.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\5 = ".exact.hostname.com"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: AutoOpenAllowedForURLs
  - サンプル値:
``` xml
<array>
  <string>example.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AutoOpenFileTypes
  #### ダウンロード時に自動的に開く必要があるファイルの種類のリスト
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 85

  #### 説明
  このポリシーは、ダウンロード時に自動的に開く必要があるファイルの種類のリストを設定します。注: ファイルの種類を一覧表示するときは、先頭の区切り文字を含めないでください。そのため、「.txt」ではなく「txt」を指定してください。

既定では、これらのファイルの種類はすべての URL で自動的に開かれます。[AutoOpenAllowedForURLs](#autoopenallowedforurls) ポリシーを使用して、これらのファイルの種類が自動的に開かれる URL を制限できます。

自動的に開く必要がある種類のファイルは、有効な Microsoft Defender SmartScreen チェックの対象となり、それらのチェックに失敗した場合は開かれません。

ユーザーが自動的に開くように指定したファイルの種類は、ダウンロード時に引き続き開かれます。ユーザーは引き続き、自動的に開く他のファイルの種類を指定できます。

このポリシーを設定しない場合、ユーザーが自動的に開くように既に指定されているファイルの種類のみがダウンロードされます。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AutoOpenFileTypes
  - GP の名前: ダウンロード時に自動的に開く必要があるファイルの種類のリスト
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\1 = "exe"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\2 = "txt"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: AutoOpenFileTypes
  - サンプル値:
``` xml
<array>
  <string>exe</string>
  <string>txt</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AutofillAddressEnabled
  #### アドレスのオートフィルを有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  オートフィル機能を有効にし、以前に保存した情報を使用して Web フォームでの住所情報のオートコンプリートを有効にします。

このポリシーを無効にした場合、オートフィルによる住所情報の提案や入力が行われず、また、Web の閲覧中にユーザーが送信する可能性がある追加の住所情報も保存されません。

このポリシーを有効にした場合または構成しなかった場合、ユーザーはユーザー インターフェイスで住所のオートフィルを制御できます。

このポリシーを無効にした場合は、支払いとパスワードのフォームを除く、すべての Web フォームでアクティビティがすべて停止されることに注意してください。追加の入力内容は保存されず、Microsoft Edge では、以前の入力情報は候補として表示されず、オートフィルも実行されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AutofillAddressEnabled
  - GP の名前: アドレスのオートフィルを有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: AutofillAddressEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AutofillAddressEnabled
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AutofillCreditCardEnabled
  #### クレジット カード情報についてオートフィルを有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge のオートフィル機能を有効にし、前回保存された情報を使用して Web フォームでクレジット カード情報の入力を自動的に完了できるようにします。

このポリシーを無効にした場合、オートフィルで、クレジット カード情報の候補が表示または入力されたり、ユーザーが Web を閲覧しているときに送信する可能性のある追加のクレジット カード情報が保存されることはありません。

このポリシーを有効にした場合、または構成しなかった場合は、ユーザーはクレジット カードのオートフィルを制御できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AutofillCreditCardEnabled
  - GP の名前: クレジット カード情報についてオートフィルを有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: AutofillCreditCardEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AutofillCreditCardEnabled
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### AutoplayAllowed
  #### Web サイトでのメディアの自動再生を許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 78

  #### 説明
  このポリシーは、Web サイトでのメディアの自動再生のポリシーを設定します。

既定の設定では「未構成」となり、現在指定されているメディアの自動再生の設定が適用され、ユーザーは自動再生の設定を構成することができます。

「有効」に設定すると、メディアの自動再生が「許可」に設定されます。すべての Web サイトでメディアの自動再生が許可されます。ユーザーは、このポリシーをオーバーライドすることはできません。

「無効」に設定すると、メディアの自動再生が「禁止」に設定されます。どの Web サイトでもメディアの自動再生は許可されません。ユーザーは、このポリシーをオーバーライドすることはできません。

このポリシーを有効にするには、タブを閉じてからもう一度開く必要があります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: AutoplayAllowed
  - GP の名前: Web サイトでのメディアの自動再生を許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: AutoplayAllowed
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: AutoplayAllowed
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### BackgroundModeEnabled
  #### Microsoft Edge が終了してもバックグラウンド アプリの実行を続行する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 77

  #### 説明
  Microsoft Edge プロセスを OS サインイン時に開始し、最後のブラウザー ウィンドウが閉じられた後でもプロセスを引き続き実行できるようにします。このシナリオでは、バックグラウンド アプリと現在の閲覧セッション (すべてのセッション Cookie を含む) はアクティブな状態のままになります。実行中のバックグラウンド プロセスのアイコンは、システム トレイに表示されるため、いつでもシステム トレイからプロセスを終了させることができます。

このポリシーを有効にした場合、バックグラウンド モードが有効になります。

このポリシーを無効にした場合、バックグラウンド モードが無効になります。

このポリシーを構成しなかった場合、最初はバックグラウンド モードが無効になっていますが、ユーザーは edge://settings/system でバックグラウンド モードの動作を構成できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: BackgroundModeEnabled
  - GP の名前: Microsoft Edge が終了してもバックグラウンド アプリの実行を続行する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: BackgroundModeEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### BackgroundTemplateListUpdatesEnabled
  #### テンプレートを使用するコレクションや他の機能で利用できるテンプレートの一覧について、バックグラウンドでの更新を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 79

  #### 説明
  利用可能なテンプレートの一覧に対するバックグラウンドでの更新を有効または無効にすることができます。このテンプレートとは、コレクションや、テンプレートを使用する他の機能で利用できるテンプレートです。テンプレートは、ページがコレクションに保存されるときに、リッチ メタデータを Web ページから抽出するために使用されます。

この設定を有効にした場合または構成しなかった場合、利用可能なテンプレートの一覧が、24 時間ごとに Microsoft サービスからバックグラウンドでダウンロードされます。

この設定を無効にした場合、利用可能なテンプレートの一覧は要求に応じてダウンロードされます。この種類のダウンロードでは、コレクションやその他の機能について、若干のパフォーマンスの低下が発生する可能性があります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: BackgroundTemplateListUpdatesEnabled
  - GP の名前: テンプレートを使用するコレクションや他の機能で利用できるテンプレートの一覧について、バックグラウンドでの更新を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: BackgroundTemplateListUpdatesEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: BackgroundTemplateListUpdatesEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### BingAdsSuppression
  #### Bing の検索結果のすべての広告をブロックする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 83

  #### 説明
  Bing.com で広告なしの検索エクスペリエンスを有効にします

このポリシーを有効にすると、ユーザーは bing.com で検索して広告なしの検索エクスペリエンスを実現できます。同時に、セーフサーチ設定は「高」に設定され、ユーザーが変更することはできません。

このポリシーを構成しない場合、既定のエクスペリエンスでは、bing.com の検索結果に広告が表示されます。セーフサーチは既定で「中」に設定され、ユーザーによって変更される場合があります。

このポリシーは、Microsoft EDU テナントとして識別される K-12 SKU でのみ使用できます。

このポリシーの詳細について、または次のシナリオが当てはまる場合は、[https://go.microsoft.com/fwlink/?linkid=2119711](https://go.microsoft.com/fwlink/?linkid=2119711) を参照してください。

* EDU テナントはあるが、ポリシーが機能しない。

* 広告なしの検索エクスペリエンスを実現するために IP をホワイトリストに登録した。

* Microsoft Edge の従来で広告なしの検索エクスペリエンスを経験していて、新しい Microsoft Edge バージョンにアップグレードしたい。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: BingAdsSuppression
  - GP の名前: Bing の検索結果のすべての広告をブロックする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: BingAdsSuppression
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: BingAdsSuppression
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### BlockThirdPartyCookies
  #### サードパーティの Cookie をブロックする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Web ページの要素がアドレス バーに表示されているドメインからのものではない場合、この Web ページの要素による Cookie の設定を禁止します。

このポリシーを有効にした場合、アドレス バーに表示されているドメインからのものではない Web ページの要素は Cookie を設定できません。

このポリシーを無効にした場合、アドレス バーには表示されていないドメインからの Web ページの要素は Cookie を設定できます。

このポリシーを構成しなかった場合、サード パーティの Cookie が有効になりますが、ユーザーはこの設定を変更できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: BlockThirdPartyCookies
  - GP の名前: サードパーティの Cookie をブロックする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: BlockThirdPartyCookies
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: BlockThirdPartyCookies
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### BrowserAddProfileEnabled
  #### ID ポップアップ メニューまたは [設定] ページでのプロファイル作成を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザーは、**[プロファイルの追加]** オプションを使用して新しいプロファイルを作成できます。
このポリシーが有効になっている場合または構成されていない場合、Microsoft Edge では、ユーザーは ID ポップアップ メニューまたは設定ページから **[ユーザーの追加]** を使用して新しいプロファイルを作成できます。

このポリシーが無効になっている場合、ユーザーは ID ポップアップ メニューまたは設定ページから新しいプロファイルを追加することができません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: BrowserAddProfileEnabled
  - GP の名前: ID ポップアップ メニューまたは [設定] ページでのプロファイル作成を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: BrowserAddProfileEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: BrowserAddProfileEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### BrowserGuestModeEnabled
  #### ゲスト モードを有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge でゲスト プロファイルの使用を許可するためのオプションを有効にします。ゲスト プロファイルでは、ブラウザーは既存のプロファイルから閲覧データをインポートせず、すべてのゲスト プロファイルが閉じられたときに閲覧データを削除します。

このポリシーを有効にした場合または構成しなかった場合、Microsoft Edge では、ゲスト プロファイルでの閲覧がユーザーに許可されます。

このポリシーを無効にした場合、Microsoft Edge では、ゲスト プロファイルでの閲覧がユーザーに許可されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: BrowserGuestModeEnabled
  - GP の名前: ゲスト モードを有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: BrowserGuestModeEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: BrowserGuestModeEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### BrowserNetworkTimeQueriesEnabled
  #### ブラウザー ネットワーク タイム サービスへのクエリを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge が正確なタイムスタンプを取得するために、ブラウザー ネットワーク タイム サービスに不定期にクエリを送信するのを防ぎます。

このポリシーを無効にした場合、Microsoft Edge によるブラウザー ネットワーク タイム サービスへのクエリの送信を停止します。

このポリシーを有効にした場合、または構成しなかった場合は、Microsoft Edge では、ブラウザー ネットワーク タイム サービスにクエリが不定期に送信されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: BrowserNetworkTimeQueriesEnabled
  - GP の名前: ブラウザー ネットワーク タイム サービスへのクエリを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: BrowserNetworkTimeQueriesEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: BrowserNetworkTimeQueriesEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### BrowserSignin
  #### ブラウザー サインインの設定
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザーが自分のアカウントで Microsoft Edge にサインインして、アカウントに関連するサービス (同期やシングル サインオンなど) を使用できるかどうかを指定します。同期を利用できるかどうかを制御するには、代わりに [SyncDisabled](#syncdisabled) ポリシーを使用します。

このポリシーを「Disable」に設定した場合、[NonRemovableProfileEnabled](#nonremovableprofileenabled) ポリシーも無効に設定していることを確認してください。これは、[NonRemovableProfileEnabled](#nonremovableprofileenabled) によって、自動的にサインインされるブラウザー プロファイルの作成が無効になるためです。両方のポリシーが設定されていると、Microsoft Edge では「ブラウザー サインインを無効にする」ポリシーが使用され、[NonRemovableProfileEnabled](#nonremovableprofileenabled) が無効に設定されているものとして動作します。

このポリシーを「Enable」に設定した場合、ユーザーはブラウザーにサインインすることができます。ブラウザーにサインインしても、同期が既定で有効になるというわけではありません。同期の機能を使用するには、ユーザーは個別にオプトインする必要があります。

このポリシーを「Force」に設定した場合、ユーザーはブラウザーを使用するためにプロファイルにサインインする必要があります。既定では、ドメイン管理者や [SyncDisabled](#syncdisabled) ポリシーによって同期が無効になっていない限り、この設定よって、ユーザーは自分のアカウントと同期するかどうかを選択することができます。[BrowserGuestModeEnabled](#browserguestmodeenabled) ポリシーの既定値は false に設定されます。

このポリシーを構成しなかった場合、ユーザーは、ブラウザー サインイン オプションを有効にして、ブラウザーをユーザーに合った状態で使用できるようにするかどうかを指定できます。

ポリシー オプションのマッピング:

* Disable (0) = ブラウザー サインインを無効にする

* Enable (1) = ブラウザー サインインを有効にする

* Force (2) = ユーザーにサインインしてブラウザーを使用するよう強制する

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: BrowserSignin
  - GP の名前: ブラウザー サインインの設定
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: BrowserSignin
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: BrowserSignin
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### BuiltInDnsClientEnabled
  #### 組み込みの DNS クライアントを使用する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  組み込みの DNS クライアントを使用するかどうかを制御します。

これはどの DNS サーバーが使用されるかについては影響しません。DNS サーバーと通信するためにどれが使用されるのかという単なるソフトウェア スタックです。たとえば、オペレーティング システムがエンタープライズ DNS サーバーを使用するように構成されている場合、そのサーバーが組み込みの DNS クライアントによって使用されます。ただし、組み込みの DNS クライアントが、DNS-over-TLS などのより新しい DNS 関連プロトコルを使用して、さまざまな方法でサーバーに対応する可能性があります。

このポリシーを有効にした場合、組み込みの DNS クライアントが使用されます (使用可能な場合)。

このポリシーを無効にした場合、クライアントは使用されません。

このポリシーを構成しなかった場合、MacOS では組み込みの DNS クライアントが既定で有効になり、ユーザーは、edge://flags を編集するか、コマンド ライン フラグを指定することで、組み込みの DNS クライアントを使用するかどうかを変更できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: BuiltInDnsClientEnabled
  - GP の名前: 組み込みの DNS クライアントを使用する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: BuiltInDnsClientEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: BuiltInDnsClientEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### BuiltinCertificateVerifierEnabled
  #### 組み込みの証明書検証ツールを使用してサーバー証明書を検証するかどうかを決定します (非推奨)
  >非推奨: このポリシーは推奨されていません。現在サポートされていますが、将来のリリースでは使用されなくなります。
  
  #### サポートされているバージョン:
  - macOS 以降の 83

  #### 説明
  このポリシーは、企業が環境を更新し、組み込みの証明書検証機能と互換性がないことが判明した場合に企業が Web コンテンツを更新する時間を増やすための短期的なメカニズムとしてのみ使用されるため、廃止されました。

Mac OS X 上の従来の証明書検証機能のサポートが削除される予定の Microsoft Edge バージョン 87 では動作しません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  

  #### Mac の情報と設定
  - 優先されるキーの名前: BuiltinCertificateVerifierEnabled
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### CertificateTransparencyEnforcementDisabledForCas
  #### subjectPublicKeyInfo ハッシュのリストに対する証明書の透明性の適用を無効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  subjectPublicKeyInfo ハッシュのリストに対する証明書の透明性に関する要件の適用を無効にします。

このポリシーでは、指定された subjectpublickeyinfo ハッシュのいずれかを持つ証明書を含む証明書チェーンに対して、証明書の透明性の公開要件を無効にできます。これにより証明書を、引き続きエンタープライズ ホストに使用することができます。このポリシーを設定しない場合は、適切に公開されないため信頼できない証明書となります。

このポリシーが設定されているときに証明書の透明性の適用を無効にするには、次の条件のいずれかを満たしている必要があります。
1. サーバー証明書の subjectPublicKeyInfo のハッシュである。
2. 証明書チェーンの CA 証明書に表示される subjectPublicKeyInfo のハッシュである (CA 証明書が X.509v3 nameConstraints 拡張機能で制限されており、1 つ以上の directoryName nameConstraints が permittedSubtrees にある。また directoryName には organizationName 属性が含まれている)。
3. 証明書チェーンの CA 証明書に表示される subjectPublicKeyInfo のハッシュである。CA 証明書には証明書のサブジェクトに 1 つ以上の organizationName 属性が含まれ、サーバーの証明書には同じ数の organizationName 属性がバイトごとに同一の値を持ち、同じ順序で含まれている。

subjectPublicKeyInfo ハッシュは、ハッシュ アルゴリズムの名前、"/" 文字、および指定された証明書の subjectPublicKeyInfo (DER でエンコードされています) に適用されるハッシュ アルゴリズムの Base64 エンコードを連結することによって指定されます。この Base64 エンコード形式は、RFC 7469 のセクション 2.4 で定義されているように、SPKI フィンガープリントと同じ形式になります。認識されないハッシュ アルゴリズムは無視されます。現時点でサポートされているハッシュ アルゴリズムは、"sha256" だけです。

このポリシーを無効にした場合または構成しなかった場合、証明書の透明性を介して公開する必要のある証明書は、証明書の透明性ポリシーに従って公開されていない場合、信頼できないものとして扱われます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: CertificateTransparencyEnforcementDisabledForCas
  - GP の名前: subjectPublicKeyInfo ハッシュのリストに対する証明書の透明性の適用を無効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\2 = "sha256//////////////////////w=="

```


  #### Mac の情報と設定
  - 優先されるキーの名前: CertificateTransparencyEnforcementDisabledForCas
  - サンプル値:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### CertificateTransparencyEnforcementDisabledForLegacyCas
  #### レガシ証明機関のリストに対する証明書の透明性の適用を無効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  レガシ証明機関 (CA) のリストに対して、証明書の透明性に関する要件の適用を無効にします。

このポリシーを使用すると、指定された subjectPublicKeyInfo ハッシュのいずれかを持つ証明書が含まれた証明書チェーンに対して、証明書の透明性に関する開示要件を無効にできます。これにより、適切に公開されていないことを理由に通常であれば信頼できないものとして扱われる証明書を、企業のホストで引き続き使用できるようになります。

証明書の透明性の適用を無効にするには、レガシ証明機関 (CA) として認識されている CA 証明書に含まれる subjectPublicKeyInfo にハッシュを設定する必要があります。レガシ CA とは、Microsoft Edge でサポートされている 1 つ以上のオペレーティング システムで既に一般的に信頼されている CA です。

subjectPublicKeyInfo ハッシュを指定するには、ハッシュ アルゴリズム名、"/" 文字、およびこのハッシュ アルゴリズムの Base64 エンコード (指定された証明書の DER エンコード済み subjectPublicKeyInfo に適用されます) を連結します。この Base64 エンコードは、RFC 7469 のセクション 2.4 で規定されている SPKI フィンガープリントと同じ形式を使用します。認識できないハッシュ アルゴリズムは無視されます。現時点でサポートされているハッシュ アルゴリズムは、"sha256" のみです。

このポリシーを構成しなかった場合、証明書の透明性を介して開示する必要がある証明書はすべて、証明書の透明性ポリシーに従って開示されていない場合は、信頼できない証明書として扱われます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: CertificateTransparencyEnforcementDisabledForLegacyCas
  - GP の名前: レガシ証明機関のリストに対する証明書の透明性の適用を無効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\2 = "sha256//////////////////////w=="

```


  #### Mac の情報と設定
  - 優先されるキーの名前: CertificateTransparencyEnforcementDisabledForLegacyCas
  - サンプル値:
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### CertificateTransparencyEnforcementDisabledForUrls
  #### 特定の URL に対する証明書の透明性の適用を無効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  一覧表示された URL に対して証明書の透過性に関する要件の強制を無効にします。

このポリシーを使用すると、証明書の透過性を介して指定された URL 内のホスト名の証明書を非公開にできます。ポリシーを使用しない場合は適切に公開されないため信頼されない証明書となります。このポリシーによって証明書を使用できますが、これらのホストに対して不正に発行された証明書の検出が困難になります。

[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) に従って URL パターンを形成します。証明書は、スキーム、ポート、またはパスに関係なく、指定されたホスト名に対して有効であるため、URL のホスト名部分のみが考慮されます。ワイルドカード ホストはサポートされていません。

このポリシーを設定しない場合、証明書の透過性を介して公開する必要のあるすべての証明書は、公開されていない場合には信頼できない証明書として処理されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: CertificateTransparencyEnforcementDisabledForUrls
  - GP の名前: 特定の URL に対する証明書の透明性の適用を無効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\2 = ".contoso.com"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: CertificateTransparencyEnforcementDisabledForUrls
  - サンプル値:
``` xml
<array>
  <string>contoso.com</string>
  <string>.contoso.com</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ClearBrowsingDataOnExit
  #### Microsoft Edge を閉じるときに閲覧データを消去する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 78

  #### 説明
  Microsoft Edge は、既定では終了時に閲覧データを消去しません。閲覧データには、フォームやパスワードに入力した情報が含まれています。またアクセスした Web サイトで入力した情報も含まれています。

       このポリシーを有効にした場合、Microsoft Edge を終了するたびにすべての閲覧データが削除されます。このポリシーを有効にした場合、このポリシーは [DefaultCookiesSetting](#defaultcookiessetting)

の構成方法よりも優先されます。        このポリシーを無効にした場合または構成しなかった場合、ユーザーは [設定] で [閲覧データをクリア] オプションを設定できます。

       このポリシーを有効にした場合は、[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) ポリシーまたは [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit) ポリシーを有効にしないでください。これらのポリシーはすべて、閲覧データの削除を扱うためです。これら 2 つのポリシーとこのポリシーを構成した場合、[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) または [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit) の構成方法に関係なく、Microsoft Edge の終了時には、すべての閲覧データが削除されます。

        終了時の Cookie の削除を除外する場合は、[SaveCookiesOnExit](#savecookiesonexit) ポリシーを構成してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ClearBrowsingDataOnExit
  - GP の名前: Microsoft Edge を閉じるときに閲覧データを消去する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: ClearBrowsingDataOnExit
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ClearBrowsingDataOnExit
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ClearCachedImagesAndFilesOnExit
  #### Microsoft Edge を閉じるときに、キャッシュされた画像とファイルを消去する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 83

  #### 説明
  Microsoft Edge は、既定では終了時にキャッシュされた画像とファイルを消去しません。

このポリシーを有効にした場合、Microsoft Edge を終了するたびに、キャッシュされた画像とファイルが削除されます。

このポリシーを無効にした場合、ユーザーは、キャッシュされた画像とファイルのオプションを edge://settings/clearBrowsingDataOnClose で構成できなくなります。

このポリシーを構成しなかった場合、ユーザーはキャッシュされた画像とファイルを終了時に消去するかどうかを選択できます。

このポリシーを無効にした場合は、[ClearBrowsingDataOnExit](#clearbrowsingdataonexit) ポリシーを有効にしないでください。どちらのポリシーもデータの削除を扱うためです。両方のポリシーを構成した場合、[ClearBrowsingDataOnExit](#clearbrowsingdataonexit) ポリシーが優先され、[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit) の構成方法に関係なく、Microsoft Edge の終了時には、すべてのデータが削除されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ClearCachedImagesAndFilesOnExit
  - GP の名前: Microsoft Edge を閉じるときに、キャッシュされた画像とファイルを消去する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: ClearCachedImagesAndFilesOnExit
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ClearCachedImagesAndFilesOnExit
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ClickOnceEnabled
  #### ユーザーが ClickOnce プロトコルを使用してファイルを開くことを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 78

  #### 説明
  ユーザーが ClickOnce プロトコルを使用してファイルを開くことを許可します。ClickOnce プロトコルを使用すると、ユーザーのコンピューターまたはデバイス上の ClickOnce ファイル ハンドラーを使用して特定の URL からファイルをブラウザーで開くように、Web サイトから要求できます。

 このポリシーを有効にした場合、ユーザーは ClickOnce プロトコルを使用してファイルを開くことができます。このポリシーは、edge://flags/ ページのユーザーの ClickOnce 設定をオーバーライドします。

 このポリシーを無効にした場合、ユーザーは ClickOnce プロトコルを使用してファイルを開くことはできません。代わりに、ファイルはブラウザーを使用してファイル システムに保存されます。 このポリシーは、edge://flags/ ページのユーザーの ClickOnce 設定をオーバーライドします。

 このポリシーを構成しなかった場合、Microsoft Edge 87 より前の Microsoft Edge バージョンを使用しているユーザーは、デフォルトでは ClickOnce プロトコルを使用してファイルを開くことはできません。ただし、edge://flags/ ページで ClickOnce プロトコルを使用できるようにするオプションがあります。87 以降の Microsoft Edge バージョンを使用しているユーザーは、デフォルトで ClickOnce プロトコルを使用してファイルを開くことができますが、edge://flags/ ページで ClickOnce プロトコルを無効にするオプションがあります。

ClickOnce を無効にすると、ClickOnce アプリケーション (.application ファイル) が正常に起動されなくなる可能性があります。

 ClickOnce の詳細については、[https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) および [https://go.microsoft.com/fwlink/?linkid=2099880](https://go.microsoft.com/fwlink/?linkid=2099880) を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ClickOnceEnabled
  - GP の名前: ユーザーが ClickOnce プロトコルを使用してファイルを開くことを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ClickOnceEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### CollectionsServicesAndExportsBlockList
  #### コレクション内の指定されたサービス リストとエクスポート対象へのアクセスをブロック
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  特定のサービスを一覧表示し、ユーザーが Microsoft Edge のコレクション機能でアクセスできない対象をエクスポートします。これには、Bing からの追加データの表示、コレクションの Microsoft 製品または外部パートナーへのエクスポートが含まれます。

このポリシーを有効にすると、指定されたリストに一致するサービスおよびエクスポート対象がブロックされます。

このポリシーを構成しないでください。許容可能なサービスとエクスポート対象に制限はありません。

ポリシー オプションのマッピング:

* pinterest_suggestions (pinterest_suggestions) = Pinterest の提案

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: CollectionsServicesAndExportsBlockList
  - GP の名前: コレクション内の指定されたサービス リストとエクスポート対象へのアクセスをブロック
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\1 = "pinterest_suggestions"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: CollectionsServicesAndExportsBlockList
  - サンプル値:
``` xml
<array>
  <string>pinterest_suggestions</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### CommandLineFlagSecurityWarningsEnabled
  #### コマンドライン フラグのセキュリティ警告を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 78

  #### 説明
  無効にすると、危険性があるコマンドライン フラグで Microsoft Edge が起動されると、このポリシーはセキュリティ警告が表示されないようにします。

有効にするか設定しない場合、これらのコマンドライン フラグが Microsoft Edge に対して使用されると、セキュリティ警告は表示されます。

たとえば、--disable-gpu-sandbox フラグは次の警告を生成します: サポートされていないコマンドライン フラグ: --disable-gpu-sandbox を使用しています。これにより、安定性およびセキュリティに関するリスクが生じます。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: CommandLineFlagSecurityWarningsEnabled
  - GP の名前: コマンドライン フラグのセキュリティ警告を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: CommandLineFlagSecurityWarningsEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: CommandLineFlagSecurityWarningsEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ComponentUpdatesEnabled
  #### Microsoft Edge でのコンポーネントの更新を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  このポリシーを有効にした場合または構成しなかった場合、Microsoft Edge でコンポーネントの更新が有効になります。

この設定を無効にした場合または false に設定した場合、Microsoft Edge のすべてのコンポーネントに対してコンポーネントの更新が無効になります。

ただし、一部のコンポーネントはこのポリシーの適用対象外となります。このようなコンポーネントには、実行可能コードが含まれていないコンポーネント、ブラウザーの動作を大幅に変更しないコンポーネント、またはセキュリティ上重要なコンポーネントなどがあります。つまり、"セキュリティ上重要" と見なされる更新は、このポリシーを無効にした場合でも適用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ComponentUpdatesEnabled
  - GP の名前: Microsoft Edge でのコンポーネントの更新を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ComponentUpdatesEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ComponentUpdatesEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ConfigureDoNotTrack
  #### トラッキング拒否を構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  トラッキング拒否要求を、トラッキング情報を要求する Web サイトに送信するかどうかを指定します。トラッキング拒否要求を使用すると、ユーザーが閲覧アクティビティの追跡を希望していないこと、アクセスした Web サイトに伝えることができます。既定では、Microsoft Edge はトラッキング拒否要求を送信しませんが、ユーザーはこの機能を有効にして、トラッキング拒否要求を送信することができます。

この設定を有効にした場合、トラッキング拒否要求は、トラッキング情報を要求する Web サイトに常に送信されます。

この設定を無効にした場合、要求は送信されません。

このポリシーを構成しなかった場合、ユーザーはこれらの要求を送信するかどうかを選択できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ConfigureDoNotTrack
  - GP の名前: トラッキング拒否を構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ConfigureDoNotTrack
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ConfigureDoNotTrack
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ConfigureOnPremisesAccountAutoSignIn
  #### Azure AD ドメイン アカウントがない場合の Active Directory ドメイン アカウントによる自動サインインを構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 81

  #### 説明
  ユーザーのコンピューターがドメインに参加しており、ご利用の環境がハイブリッド参加していない場合、自動サインインで Active Directory アカウントを使用できるようにします。ユーザーが Azure Active Directory アカウントで自動的にサインインされるようにする場合は、ご利用の環境を Azure AD 参加させるか (詳細については [https://go.microsoft.com/fwlink/?linkid=2118197](https://go.microsoft.com/fwlink/?linkid=2118197) を参照)、ハイブリッド参加させてください (詳細については [https://go.microsoft.com/fwlink/?linkid=2118365](https://go.microsoft.com/fwlink/?linkid=2118365) を参照)。

[BrowserSignin](#browsersignin) ポリシーを無効に構成した場合、このポリシーは適用されません。

このポリシーを有効にして、「SignInAndMakeDomainAccountNonRemovable」に設定した場合、Microsoft Edge では、ドメインに参加しているコンピューター上のユーザーは、Active Directory アカウントを使用して自動的にサインインされます。

このポリシーを「Disabled」に設定した場合、またはこのポリシーを設定しなかった場合、Microsoft Edge では、ドメインに参加しているコンピューター上のユーザーは、Active Directory アカウントを使用して自動的にサインインされません。

ポリシー オプションのマッピング:

* Disabled (0) = 無効

* SignInAndMakeDomainAccountNonRemovable (1) = サインインして、ドメイン アカウントを削除できないようにする

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ConfigureOnPremisesAccountAutoSignIn
  - GP の名前: Azure AD ドメイン アカウントがない場合の Active Directory ドメイン アカウントによる自動サインインを構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ConfigureOnPremisesAccountAutoSignIn
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ConfigureOnlineTextToSpeech
  #### オンライン音声合成を構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ブラウザーでオンライン音声合成の音声フォント (Azure Cognitive Services の一部) を活用できるかどうかを設定します。これらの音声フォントは、プレインストールされているシステム音声フォントよりも品質が高くなっています。

このポリシーを有効にした場合または構成しなかった場合、SpeechSynthesis API を使用する Web ベースのアプリケーションは、オンライン音声合成の音声フォントを利用できます。

このポリシーを無効にした場合、音声フォントは利用できなくなります。

この機能の詳細については以下をご覧ください:
SpeechSynthesis API: [https://go.microsoft.com/fwlink/?linkid=2110038](https://go.microsoft.com/fwlink/?linkid=2110038)
Cognitive Services: [https://go.microsoft.com/fwlink/?linkid=2110141](https://go.microsoft.com/fwlink/?linkid=2110141)

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ConfigureOnlineTextToSpeech
  - GP の名前: オンライン音声合成を構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ConfigureOnlineTextToSpeech
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ConfigureOnlineTextToSpeech
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ConfigureShare
  #### 共有エクスペリエンスを構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 83

  #### 説明
  このポリシーを「ShareAllowed」(既定) に設定すると、ユーザーは Microsoft Edge の [設定] および [その他のメニュー] から Windows 10 共有エクスペリエンスにアクセスして、システム上の他のアプリと共有できます。

このポリシーを「ShareDisallowed」に設定すると、ユーザーは Windows 10 共有エクスペリエンスにアクセスできなくなります。[共有] ボタンがツールバーにある場合、それも非表示になります。

ポリシー オプションのマッピング:

* ShareAllowed (0) = 共有エクスペリエンスの使用を許可する

* ShareDisallowed (1) = 共有エクスペリエンスの使用を許可しない

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ConfigureShare
  - GP の名前: 共有エクスペリエンスを構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ConfigureShare
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### CustomHelpLink
  #### カスタム ヘルプのリンクを指定する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 79

  #### 説明
  ヘルプメニューまたは F1 キーへのリンクを指定してください。

このポリシーを有効にした場合、管理者は [ヘルプ] メニューまたは F1 キーへのリンクを指定できます。

このポリシーを無効にした場合、または構成しなかった場合は、[ヘルプ] メニューまたは F1 キーの既定のリンクが使用されます。

このポリシーは、デバイス管理用に登録されている Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: CustomHelpLink
  - GP の名前: カスタム ヘルプのリンクを指定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: CustomHelpLink
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"https://go.microsoft.com/fwlink/?linkid=2080734"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: CustomHelpLink
  - サンプル値:
``` xml
<string>https://go.microsoft.com/fwlink/?linkid=2080734</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DNSInterceptionChecksEnabled
  #### DNS 傍受チェックが有効になっている
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 80

  #### 説明
  このポリシーでは、DNS 傍受チェックを無効にするために使用できるローカル スイッチを構成します。これらのチェックでは、不明なホスト名にリダイレクトするプロキシの内側にブラウザーがあるかどうかが検出されます。

こうした検出は、ネットワーク構成がわかっているエンタープライズ環境では必要でない場合があります。この検出機能を無効にすると、スタートアップ時や DNS 構成を変更するたびに、追加の DNS や HTTP トラフィックが発生するのを回避できます。

このポリシーを有効にした場合または設定しなかった場合、DNS 傍受チェックが実行されます。

このポリシーを無効にした場合、DNS 傍受チェックは実行されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DNSInterceptionChecksEnabled
  - GP の名前: DNS 傍受チェックが有効になっている
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DNSInterceptionChecksEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DNSInterceptionChecksEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultBrowserSettingEnabled
  #### Microsoft Edge を既定のブラウザーとして設定する
  
  
  #### サポートされているバージョン:
  - Windows 7 以降の macOS と 77

  #### 説明
  このポリシーを True に設定すると、Microsoft Edge は常に起動時に既定のブラウザーであるかどうかを確認し、可能であれば自動的に登録します。

このポリシーを False に設定すると、Microsoft Edge はそれが既定であるかどうかの確認を中止し、このオプションのユーザー制御をオフにします。

このポリシーを設定しない場合、Microsoft Edge を使用すると、ユーザーはそれが既定かどうかを制御でき、そうでない場合は、ユーザー通知を表示するかどうかを制御できます。

Windows 管理者への注意: このポリシーは、Windows 7 を実行している PC でのみ機能します。それ以降のバージョンの Windows では、Microsoft Edge を https および http プロトコル (およびオプションで、FTP プロトコルと、.html、.htm、.pdf、.svg、.webp などのファイル形式) のハンドルにする「既定のアプリケーション関連付け」ファイルを展開する必要があります。詳細については、[https://go.microsoft.com/fwlink/?linkid=2094932](https://go.microsoft.com/fwlink/?linkid=2094932) を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultBrowserSettingEnabled
  - GP の名前: Microsoft Edge を既定のブラウザーとして設定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DefaultBrowserSettingEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultBrowserSettingEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultSearchProviderContextMenuAccessAllowed
  #### 既定の検索プロバイダーのコンテキストメニュー検索アクセスを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 85

  #### 説明
  コンテキスト メニューで既定の検索プロバイダーの使用を有効にします。

このポリシーを無効に設定すると、既定の検索プロバイダーに依存する検索コンテキスト メニューのアイテムが使用され、サイドバー検索は使用できなくなります。

このポリシーが有効または設定されていない場合、既定の検索プロバイダーとサイドバー検索のコンテキスト メニューのアイテムが利用可能になります。

ポリシー値は、[DefaultSearchProviderEnabled](#defaultsearchproviderenabled) ポリシーが有効になっている場合にのみ適用されます。それ以外の場合は適用されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultSearchProviderContextMenuAccessAllowed
  - GP の名前: 既定の検索プロバイダーのコンテキストメニュー検索アクセスを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DefaultSearchProviderContextMenuAccessAllowed
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultSearchProviderContextMenuAccessAllowed
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultSensorsSetting
  #### 既定のセンサーの設定
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  Web サイトがモーションセンサーや光センサーなどのセンサーにアクセスして使用できるかどうかを設定します。Web サイトがセンサーにアクセスするのを完全にブロックまたは許可できます。

ポリシーを 1 に設定すると、Web サイトがセンサーにアクセスして使用できるようになります。このポリシーを2に設定すると、シリアルポートへのアクセスが拒否されます。

[SensorsAllowedForUrls](#sensorsallowedforurls) および [SensorsBlockedForUrls](#sensorsblockedforurls) ポリシーを使用して、特定のURLパターンに対してこのポリシーを上書きできます。

このポリシーを構成しなかった場合、Web サイトは、Web サイトはセンサーにアクセスして使用でき、ユーザーはこの設定を変更できます。これは、[SensorsAllowedForUrls](#sensorsallowedforurls) および [SensorsBlockedForUrls](#sensorsblockedforurls) のグローバル既定です。

ポリシー オプションのマッピング:

* AllowSensors (1) = サイトのセンサーへのアクセスを許可

* BlockSensors (2) = センサーへのアクセスをサイトに許可しない

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultSensorsSetting
  - GP の名前: 既定のセンサーの設定
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DefaultSensorsSetting
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultSensorsSetting
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DefaultSerialGuardSetting
  #### Serial API の使用を制御する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  Web サイトがシリアルポートにアクセスできるかどうかを設定します。Web サイトがシリアルポートへのアクセス権を取得するたびに、アクセスを完全にブロックしたり、ユーザーに質問したりすることができます。

このポリシーを3に設定すると、Web サイトでシリアルポートへのアクセスを要求されます。このポリシーを2に設定すると、シリアルポートへのアクセスが拒否されます。

[SerialAskForUrls](#serialaskforurls) および [SerialBlockedForUrls](#serialblockedforurls) ポリシーを使用して、特定のURLパターンに対してこのポリシーを上書きできます。

  このポリシーを構成しなかった場合、既定では、Web サイトは、シリアルポートにアクセスできるかどうかをユーザーに確認することができます。ユーザーはこの設定を変更できます。

ポリシー オプションのマッピング:

* BlockSerial (2) = すべてのサイトがシリアル API 経由でのシリアルポートへのアクセスを要求できないようにする

* AskSerial (3) = ユーザーがシリアルポートにアクセスするためのアクセス許可をサイトに許可する

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DefaultSerialGuardSetting
  - GP の名前: Serial API の使用を制御する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DefaultSerialGuardSetting
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DefaultSerialGuardSetting
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DelayNavigationsForInitialSiteListDownload
  #### タブ ナビゲーションの前にエンタープライズ モード サイト一覧が利用可能である必要がある
  
  
  #### サポートされているバージョン:
  - Windows 以降の 84

  #### 説明
  ブラウザーが初期エンタープライズ モード サイト一覧をダウンロードし終わるまで Microsoft Edge のタブがナビゲーションを待つかどうかを指定できます。この設定は、ブラウザーのホーム ページを Internet Explorer モードで読み込む必要があるシナリオを想定したものです。IE モードを有効にした後のブラウザーの初回実行時に待つようにすることが重要です。このシナリオが存在しない場合は、ホーム ページの読み込みのパフォーマンスに悪影響を及ぼす可能性があるため、この設定を有効にしないことをお勧めします。この設定は、IE モードを有効にした後のブラウザーの初回実行など、Microsoft Edge にキャッシュされたエンタープライズ モード サイト一覧がない場合にのみ適用されます。

 この設定は次と連動して機能します。
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) が「IEMode」に設定されている
および
リストに少なくとも 1 つのエントリがある [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) ポリシー。

[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout) ポリシーを使用して、このポリシーのタイムアウトの動作を構成できます。

このポリシーを All に設定した場合、Microsoft Edge にエンタープライズ モード サイト リストのキャッシュされたバージョンがないときは、ブラウザーがサイト リストをダウンロードするまで、タブのナビゲーションが遅延します。サイト リストによって Internet Explorer モードで開くように構成されているサイトは、ブラウザーの初期ナビゲーション中であっても、Internet Explorer モードで読み込まれます。http:、https:、file:、ftp: 以外のスキームを使用したサイトなど、Internet Explorer で開くように構成されていないサイトは、ナビゲーションを遅延させず、Edge モードですぐに読み込まれます。

このポリシーを None に設定した場合、または構成しなかった場合、Microsoft Edge にエンタープライズ モード サイト一覧のキャッシュされたバージョンがないときは、タブはすぐに移動し、ブラウザーがエンタープライズ モード サイト一覧をダウンロードするまで待つことはありません。サイト リストによって Internet Explorer モードで開くように構成されているサイトは、ブラウザーがエンタープライズ モード サイト一覧のダウンロードを完了するまで Microsoft Edge モードで開きます。

ポリシー オプションのマッピング:

* None (0) = なし

* All (1) = 対象となるすべてのナビゲーション

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DelayNavigationsForInitialSiteListDownload
  - GP の名前: タブ ナビゲーションの前にエンタープライズ モード サイト一覧が利用可能である必要がある
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DelayNavigationsForInitialSiteListDownload
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DeleteDataOnMigration
  #### 移行時に古いブラウザー データを削除する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 83

  #### 説明
  このポリシーでは、Microsoft Edge バージョン 81 以降に移行した後で、Microsoft Edge 従来版からのユーザーの閲覧データを削除するかどうかを決定します。

このポリシーを「有効」に設定した場合、Microsoft Edge バージョン 81 以降に移行した後で、Microsoft Edge 従来版からのすべての閲覧データが削除されます。このポリシーを既存の閲覧データに適用させるには、Microsoft Edge バージョン 81 以降に移行する前に、このポリシーを設定する必要があります。

このポリシーを「無効」に設定した場合または構成しなかった場合、Microsoft Edge バージョン 83 以降に移行した後で、ユーザーの閲覧データは削除されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DeleteDataOnMigration
  - GP の名前: 移行時に古いブラウザー データを削除する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DeleteDataOnMigration
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DeveloperToolsAvailability
  #### 開発者ツールを使用できる状況を制御する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  開発者ツールを使用できる状況を制御します。

このポリシーを「DeveloperToolsDisallowedForForceInstalledExtensions」(既定) に設定した場合、基本的には、ユーザーは開発者ツールや JavaScript コンソールにアクセスできますが、エンタープライズ ポリシーによってインストールされた拡張機能では、開発者ツールや JavaScript コンソールにはアクセスできません。

このポリシーを「DeveloperToolsAllowed」に設定した場合、エンタープライズ ポリシーによってインストールされた拡張機能を含むすべての状況で、ユーザーは開発者ツールや JavaScript コンソールにアクセスできます。

このポリシーを「DeveloperToolsDisallowed」に設定した場合、ユーザーは開発者ツールにアクセスしたり、Web サイトの要素を検査したりすることはできません。開発者ツールや JavaScript コンソールを開くキーボード ショートカット、メニュー、コンテキスト メニューの各エントリは、無効になります。

ポリシー オプションのマッピング:

* DeveloperToolsDisallowedForForceInstalledExtensions (0) = エンタープライズ ポリシーによってインストールされた拡張機能での開発者ツールの使用を禁止するが、他の状況における開発者ツールの使用は許可する

* DeveloperToolsAllowed (1) = 開発者ツールの使用を許可する

* DeveloperToolsDisallowed (2) = 開発者ツールの使用を許可すしない

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DeveloperToolsAvailability
  - GP の名前: 開発者ツールを使用できる状況を制御する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DeveloperToolsAvailability
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DeveloperToolsAvailability
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DiagnosticData
  #### ブラウザー使用状況に関する必要な診断データとオプションの診断データを送信する
  
  
  #### サポートされているバージョン:
  - Windows 7 以降の macOS と 86

  #### 説明
  このポリシーは、ブラウザーの使用に関する必須およびオプションの診断データを Microsoft に送信することを制御します。

必要な診断データが収集され、Microsoft Edge が安全で最新の状態に維持され、期待どおりに実行されます。

オプションの診断データには、ブラウザーの使用方法、アクセスした Web サイト、製品やサービスの改善のために Microsoft に送るクラッシュ レポートに関するデータが含まれます。

このポリシーは、Windows 10 デバイスではサポートされていません。Windows 10 でこのデータ収集を制御するには、IT 管理者は Windows 診断データのグループ ポリシーを使用する必要があります。このポリシーは、Windows のバージョンに応じて、[テレメトリを許可] または [診断データを許可] のいずれかになります。Windows 10 の診断データ収集の詳細: [https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

次のいずれかの設定を使用して、このポリシーを構成します。

「Off」は、必須およびオプションの診断データの収集をオフにします。このオプションは推奨されません。

「RequiredData」は、必要な診断データを送信しますが、オプションの診断データの収集をオフにします。Microsoft Edge は必要な診断データを送信して、Microsoft Edge を安全で最新の状態に保ち、期待どおりに実行します。

「OptionalData」は、ブラウザーの使用状況、アクセスした Web サイト、製品とサービスの改善のために Microsoft に送信されるクラッシュ レポートに関するデータを含むオプションの診断データを送信します。

Windows 7/macOS の場合、このポリシーは必須およびオプションのデータを Microsoft に送信することを制御します。

このポリシーを構成しないか無効にすると、Microsoft Edge は既定でユーザーの設定になります。

ポリシー オプションのマッピング:

* Off (0) = 低 (推奨しません)

* RequiredData (1) = 必須データ

* OptionalData (2) = オプションのデータ

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DiagnosticData
  - GP の名前: ブラウザー使用状況に関する必要な診断データとオプションの診断データを送信する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DiagnosticData
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DiagnosticData
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DirectInvokeEnabled
  #### ユーザーが DirectInvoke プロトコルを使用してファイルを開くことを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 78

  #### 説明
  ユーザーが DirectInvoke プロトコルを使用してファイルを開くことを許可します。DirectInvoke プロトコルを使用すると、ユーザーのコンピューターまたはデバイス上の特定のファイル ハンドラーを使用して特定の URL からファイルをブラウザーで開くように、Web サイトから要求できます。

このポリシーを有効にした場合または構成しなかった場合、ユーザーは DirectInvoke プロトコルを使用してファイルを開くことができます。

このポリシーを無効にした場合、ユーザーは DirectInvoke プロトコルを使用してファイルを開くことはできません。代わりに、ファイルはファイル システムに保存されます。

注意: DirectInvoke を無効にすると、一部の Microsoft Office SharePoint Online 機能が予期したとおりに機能しなくなる場合があります。

DirectInvoke の詳細については、[https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) および [https://go.microsoft.com/fwlink/?linkid=2099871](https://go.microsoft.com/fwlink/?linkid=2099871) を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DirectInvokeEnabled
  - GP の名前: ユーザーが DirectInvoke プロトコルを使用してファイルを開くことを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DirectInvokeEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### Disable3DAPIs
  #### 3D グラフィックス API のサポートを無効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Web ページがグラフィック プロセッシング ユニット (GPU) にアクセスできないようにします。具体的には、Web ページは WebGL API にアクセスできず、プラグインでは Pepper 3D API を使用できなくなります。

このポリシーを構成しなかった場合または無効にした場合は、Web ページで WebGL API とプラグインを使用して、Pepper 3D API を使用することができます。Microsoft Edge では、既定でこれらの API を使用するためにコマンド ラインの引数を渡すことが必要になる場合があります。

[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled) ポリシーが false に設定されている場合、'Disable3DAPIs' ポリシーの設定は無視されます。これは、'Disable3DAPIs' ポリシーを true に設定することと同じです。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: Disable3DAPIs
  - GP の名前: 3D グラフィックス API のサポートを無効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: Disable3DAPIs
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: Disable3DAPIs
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DisableScreenshots
  #### スクリーンショットの撮影を無効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザーがブラウザー ページのスクリーンショットを撮ることができるかどうかを制御します。

このポリシーを有効にした場合、ユーザーはキーボード ショートカットや、拡張機能 API を使ってスクリーンショットを撮ることはできません。

このポリシーを無効にした場合または構成しなかった場合、ユーザーはスクリーンショットを撮ることができます。

このポリシーは、ブラウザー内から撮るスクリーンショットを制御することに注意してください。このポリシーを有効にしても、ユーザーはブラウザー外部の方法 (オペレーティング システムの機能や他のアプリケーションなど) を使用して、スクリーンショットを撮ることができる場合があります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DisableScreenshots
  - GP の名前: スクリーンショットの撮影を無効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DisableScreenshots
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DisableScreenshots
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DiskCacheDir
  #### ディスク キャッシュ ディレクトリを設定する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  キャッシュ ファイルを保存するために使用するディレクトリを構成します。

このポリシーを有効にした場合、Microsoft Edge では、ユーザーが '--disk-cache-dir' フラグを設定したかどうかに関係なく、ポリシーで指定されたディレクトリを使用します。データの損失や他の予期しないエラーを回避するために、このポリシーの構成では、ボリュームのルート ディレクトリまたは他の用途に使用されるディレクトリを指定しないでください。Microsoft Edge で、こうしたディレクトリのコンテンツを管理しているためです。

ディレクトリとパスを指定するときに使用できる変数のリストについては、[https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) を参照してください。

このポリシーを構成しなかった場合、既定のキャッシュ ディレクトリが使用されます。ユーザーは、'--disk-cache-dir' コマンド ライン フラグを使用して、既定のキャッシュ ディレクトリをオーバーライドできます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DiskCacheDir
  - GP の名前: ディスク キャッシュ ディレクトリを設定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DiskCacheDir
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"${user_home}/Edge_cache"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DiskCacheDir
  - サンプル値:
``` xml
<string>${user_home}/Edge_cache</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DiskCacheSize
  #### ディスク キャッシュ サイズをバイト単位で設定する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ファイルをディスク上に保存する場合に使用するキャッシュのサイズをバイト単位で構成します。

このポリシーを有効にした場合、Microsoft Edge では、ユーザーが '--disk-cache-size' フラグを指定したかどうかに関係なく、ポリシーで指定されたキャッシュ サイズを使用します。このポリシーで指定される値は、絶対的な境界値を示すものではなく、キャッシュ システム向けの推奨値を示すものです。数メガバイトを下回る値は小さすぎ、適正な最小値に引き上げられます。

このポリシーの値を 0 に設定した場合、既定のキャッシュ サイズが使用されます。ユーザーはこのサイズを変更できません。

このポリシーを構成しなかった場合、既定のサイズが使用されます。ユーザーは '--disk-cache-size' フラグを使用してこのサイズをオーバーライドできます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DiskCacheSize
  - GP の名前: ディスク キャッシュ サイズをバイト単位で設定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DiskCacheSize
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x06400000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DiskCacheSize
  - サンプル値:
``` xml
<integer>104857600</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DnsOverHttpsMode
  #### DNS-over-HTTPS モードを制御
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 83

  #### 説明
  DNS over HTTPS リゾルバーのモードを制御します。このポリシーでは、クエリごとに既定のモードのみが設定されることに注意してください。このモードは、DNS over HTTPS サーバーのホスト名を解決するための要求など、特殊なクエリの種類に対して上書きできます。

"off" モードを使用すると、DNS over HTTPS が無効になります。

"automatic" モードでは、DNS over HTTPS サーバーが使用可能で、エラーが発生した場合に安全なクエリの送信を行うために、DNS over HTTPS クエリがまず送信されます。

"secure" モードでは、DNS over HTTPS クエリのみが送信され、エラーが発生した場合には解決できません。

このポリシーを構成していない場合は、ユーザーが構成したシステムリゾルバーに関連付けられているリゾルバーに、DNS over HTTPS 要求を送信する場合があります。

ポリシー オプションのマッピング:

* off (off) = DNS-over-HTTPS を無効にする

* automatic (automatic) = 安全でないフォールバックを使用した DNS-over-HTTPS を有効にする

* secure (secure) = 安全でないフォールバックなしで DNS-over-HTTPS を有効にする

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DnsOverHttpsMode
  - GP の名前: DNS-over-HTTPS モードを制御
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DnsOverHttpsMode
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"off"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DnsOverHttpsMode
  - サンプル値:
``` xml
<string>off</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DnsOverHttpsTemplates
  #### 目的の DNS-over-HTTPS リゾルバーの URI テンプレートを指定します
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 83

  #### 説明
  目的の DNS-over-HTTPS リゾルバーの URI テンプレートです。複数の DNS-over-HTTPS リゾルバーを指定するには、対応する URI テンプレートをスペースで区切ります。

[DnsOverHttpsMode](#dnsoverhttpsmode) を "secure" に設定した場合、このポリシーを設定する必要があり、空にすることはできません。

[DnsOverHttpsMode](#dnsoverhttpsmode) を "automatic" に設定し、このポリシーを設定した場合、指定された URI テンプレートが使用されます。このポリシーを設定しない場合は、ハードコードされたマッピングを使用して、ユーザーの現在の DNS リゾルバーを同じプロバイダーが操作する DoH リゾルバーにアップグレードしようとします。

URI テンプレートに dns 変数が含まれている場合、リゾルバーへの要求には GET が使用されます。それ以外の場合は、要求で POST が使用されます。

形式が正しくないテンプレートは無視されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DnsOverHttpsTemplates
  - GP の名前: 目的の DNS-over-HTTPS リゾルバーの URI テンプレートを指定します
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: DnsOverHttpsTemplates
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"https://dns.example.net/dns-query{?dns}"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DnsOverHttpsTemplates
  - サンプル値:
``` xml
<string>https://dns.example.net/dns-query{?dns}</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DownloadDirectory
  #### ディレクトリをダウンロードする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ファイルをダウンロードするときに使用するディレクトリを構成します。

このポリシーを有効にした場合、Microsoft Edge では、ユーザーが既にディレクトリを設定しているかどうか、またはユーザーに対して毎回ダウンロードの場所を要求するように選択したかどうかに関係なく、ポリシーで指定されたディレクトリが使用されます。使用できる変数のリストについては、[https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) を参照してください。

このポリシーを無効にした場合または構成しなかった場合、既定のダウンロード ディレクトリが使用されます。ユーザーはこの既定のディレクトリを変更できます。

無効なパスを設定した場合、Microsoft Edge では、ユーザーの既定のダウンロード ディレクトリを既定のディレクトリとして使用します。

パスで指定されたフォルダーが存在しない場合、ダウンロードを実行すると、ダウンロードの保存場所をユーザーに確認するプロンプトが表示されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DownloadDirectory
  - GP の名前: ディレクトリをダウンロードする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: DownloadDirectory
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"\n      Linux-based OSes (including Mac): /home/${user_name}/Downloads\n      Windows: C:\\Users\\${user_name}\\Downloads"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DownloadDirectory
  - サンプル値:
``` xml
<string>
      Linux-based OSes (including Mac): /home/${user_name}/Downloads
      Windows: C:\Users\${user_name}\Downloads</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### DownloadRestrictions
  #### ダウンロードの制限を許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge で完全にブロックするダウンロードの種類を構成します。ユーザーは、セキュリティの判定結果をオーバーライドすることはできません。

  「BlockDangerousDownloads」に設定すると、Microsoft Defender SmartScreen の警告が表示される場合にダウンロードがブロックされ、それ以外の場合はすべてのダウンロードが許可されます。

「BlockPotentiallyDangerousDownloads」に設定すると、危険の可能性がある、または不要なダウンロードを示す Microsoft Defender SmartScreen の警告が表示される場合にダウンロードがブロックされ、それ以外の場合はすべてのダウンロードが許可されます。

すべてのダウンロードをブロックするには、「BlockAllDownloads」を設定します。

このポリシーを構成しなかった場合または「DefaultDownloadSecurity」オプションに設定した場合、Microsoft Defender SmartScreen の分析結果に基づいて、ダウンロードでは通常のセキュリティ制限が適用されます。

こうした制限は、Web ページのコンテンツや [ダウンロード リンク...] コンテキスト メニュー オプションからのダウンロードに適用されます。ただし、現在表示されているページの保存やダウンロードには適用されません。また、印刷オプションの [PDF として保存] オプションにも適用されません。

Microsoft Defender SmartScreen の詳細については、[https://go.microsoft.com/fwlink/?linkid=2094934](https://go.microsoft.com/fwlink/?linkid=2094934) を参照してください。

ポリシー オプションのマッピング:

* DefaultDownloadSecurity (0) = 特別な制限はありません

* BlockDangerousDownloads (1) = 危険なダウンロードをブロックする

* BlockPotentiallyDangerousDownloads (2) = その他の脅威または不要なダウンロードをブロック

* BlockAllDownloads (3) = すべてのダウンロードをブロックする

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: DownloadRestrictions
  - GP の名前: ダウンロードの制限を許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: DownloadRestrictions
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: DownloadRestrictions
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### EdgeCollectionsEnabled
  #### コレクション機能を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 78

  #### 説明
  ユーザーがコレクション機能にアクセスして、コンテンツの収集、整理、共有、およびエクスポートをより効率的に Office 統合を使用して行うことができるようになります。

このポリシーを有効にした場合、または構成しなかった場合、ユーザーは Microsoft Edge のコレクション機能にアクセスして使用することができます。

このポリシーを無効にした場合は、ユーザーは Microsoft Edge のコレクション機能にアクセスして使用できません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: EdgeCollectionsEnabled
  - GP の名前: コレクション機能を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: EdgeCollectionsEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: EdgeCollectionsEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### EditFavoritesEnabled
  #### ユーザーによるお気に入りの編集を許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  このポリシーを有効にした場合、ユーザーはお気に入りの追加、削除、変更を行うことができます。これは、ポリシーを構成しなかった場合の既定の動作です。

このポリシーを無効にした場合、ユーザーはお気に入りの追加、削除、変更を行うことができなくなります。ただし、既存のお気に入りは引き続き使用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: EditFavoritesEnabled
  - GP の名前: ユーザーによるお気に入りの編集を許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: EditFavoritesEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: EditFavoritesEnabled
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### EnableDeprecatedWebPlatformFeatures
  #### 制限された期間、非推奨の Web プラットフォーム機能を再度有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  一時的にもう一度有効にすることができる、非推奨の Web プラットフォーム機能のリストを指定します。

このポリシーを使用すると、限定された期間内であれば非推奨の Web プラットフォーム機能をもう一度有効にできます。機能は文字列タグで識別されます。

このポリシーを構成しないと、リストが空の場合、またはサポートされる文字列タグのいずれにも機能が一致しない場合は、すべての非推奨の Web プラットフォーム機能は無効のままとなります。

ポリシー自体は上記のプラットフォームでサポートされますが、このポリシーで有効になる機能は、一部のプラットフォームでは利用できない場合があります。一部の非推奨の Web プラットフォーム機能は、もう一度有効にすることはできません。もう一度有効にできるのは、下記のリストに明示的に指定されている機能のみで、有効にできる期間は限定されています。この期間は機能によって異なります。Web プラットフォーム機能の変更の背景にある目的については、https://bit.ly/blinkintents で確認できます。

文字列タグの一般的な形式は [DeprecatedFeatureName]_EffectiveUntil[yyyymmdd] です。

ポリシー オプションのマッピング:

* ExampleDeprecatedFeature (ExampleDeprecatedFeature_EffectiveUntil20080902) = 2008/09/02 からの ExampleDeprecatedFeature API を有効にする

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: EnableDeprecatedWebPlatformFeatures
  - GP の名前: 制限された期間、非推奨の Web プラットフォーム機能を再度有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures\1 = "ExampleDeprecatedFeature_EffectiveUntil20080902"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: EnableDeprecatedWebPlatformFeatures
  - サンプル値:
``` xml
<array>
  <string>ExampleDeprecatedFeature_EffectiveUntil20080902</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### EnableDomainActionsDownload
  #### マイクロソフトからのドメイン アクションのダウンロードを有効にする (現在不使用)
  
  >古い形式: このポリシーは古い形式であり、Microsoft Edge 84 以降では使用することができません。
  #### サポートされているバージョン:
  - Windows 以降、macOS と 77 を 84

  #### 説明
  競合する状態を回避する必要があるため、このポリシーは機能しません。このポリシーは、ドメイン アクションのリストのダウンロードを有効または無効にするために使用されますが、必ずしも目的の状態が実現されるわけではありません。ダウンロードを処理する実験および構成サービスには、サービスからダウンロードされる内容を構成するための独自のポリシーがあります。代わりに [ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol) ポリシーを使用してください。

Microsoft Edge では、ドメイン アクションとは、ブラウザーが Web 上で正常に動作する場合に役立つ一連の互換性機能を意味します。

Microsoft では、互換性に対応するために、特定のドメインで実行されるアクションのリストを保持しています。たとえば、Microsoft Edge での新しいユーザー エージェント文字列が原因で Web サイトが破損した場合、ブラウザーは Web サイト上のユーザー エージェント文字列を上書きする場合があります。こうしたアクションは一時的なものであり、Microsoft ではサイト所有者に関連する問題の解決を試行します。

ブラウザーが起動し、その後定期的に実行されると、ブラウザーは、実行する互換性アクションの最新のリストを保持している実験および構成サービスに接続します。このリストは、最初に取得された後、サーバーのコピーが変更された場合にのみ後続の要求でリストが更新されるように、ローカルで保存されます。

このポリシーを有効にした場合、ドメイン アクションのリストは引き続き実験および構成サービスからダウンロードされます。

このポリシーを無効にした場合、ドメイン アクションのリストは実験および構成サービスからダウンロードされなくなります。

このポリシーを構成しなかった場合、ドメイン アクションのリストは引き続き実験および構成サービスからダウンロードされます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: EnableDomainActionsDownload
  - GP の名前: マイクロソフトからのドメイン アクションのダウンロードを有効にする (現在不使用)
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: EnableDomainActionsDownload
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: EnableDomainActionsDownload
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### EnableOnlineRevocationChecks
  #### オンライン OCSP/CRL チェックを有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  オンライン失効チェックでは、セキュリティ上の重要なメリットが実現されず、既定では無効になっています。

このポリシーを有効にした場合、Microsoft Edge ではソフト フェイルのオンライン OCSP/CRL チェックが実行されます。"ソフト フェイル" とは、失効サーバーにアクセスできない場合に、証明書が有効と見なされることを意味します。

このポリシーを無効にした場合または構成しなかった場合、Microsoft Edge ではオンライン失効チェックが実行されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: EnableOnlineRevocationChecks
  - GP の名前: オンライン OCSP/CRL チェックを有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: EnableOnlineRevocationChecks
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: EnableOnlineRevocationChecks
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### EnableSha1ForLocalAnchors
  #### ローカルトラストアンカーによって発行された場合に、SHA-1 を使用して署名された証明書を許可する (非推奨)
  >非推奨: このポリシーは推奨されていません。現在サポートされていますが、将来のリリースでは使用されなくなります。
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 85

  #### 説明
  この設定を有効にすると、証明書がローカルにインストールされたルート証明書にチェーンされ、それ以外が有効である限り、Microsoft Edge は SHA-1 署名付き証明書によって保護された接続を許可します。

このポリシーは、SHA-1 署名を許可するオペレーティング システム (OS) の証明書検証スタックに依存することに注意してください。OS 更新により SHA-1 証明書の OS 処理が変更されると、このポリシーは無効になる可能性があります。さらに、このポリシーは、SHA-1 から移行するための時間を企業に与える一時的な回避策として意図されています。このポリシーは、2021 年半ばにリリースされる Microsoft Edge 92 で削除されます。

このポリシーを設定しなかったり、false に設定しなかったり、SHA-1 証明書チェーンを公的に信頼された証明書ルートに設定しなかったりした場合、Microsoft Edge は SHA-1 によって署名された証明書を許可しません。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: EnableSha1ForLocalAnchors
  - GP の名前: ローカルトラストアンカーによって発行された場合に、SHA-1 を使用して署名された証明書を許可する (非推奨)
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: EnableSha1ForLocalAnchors
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: EnableSha1ForLocalAnchors
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### EnterpriseHardwarePlatformAPIEnabled
  #### 管理された拡張機能を有効にして、エンタープライズ ハードウェア プラットフォーム API を使用する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 78

  #### 説明
  このポリシーが有効に設定されていると、エンタープライズ ポリシーによってインストールされた拡張機能では、エンタープライズ ハードウェア プラットフォーム API を使用できます。
このポリシーが無効に設定されているか、設定されていない場合、どの拡張機能もエンタープライズ ハードウェア プラットフォーム API を使用できません。
このポリシーは、コンポーネント拡張機能にも適用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: EnterpriseHardwarePlatformAPIEnabled
  - GP の名前: 管理された拡張機能を有効にして、エンタープライズ ハードウェア プラットフォーム API を使用する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: EnterpriseHardwarePlatformAPIEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: EnterpriseHardwarePlatformAPIEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### EnterpriseModeSiteListManagerAllowed
  #### Enterprise Mode Site List Manager ツールへのアクセスを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 86

  #### 説明
  ユーザーが Enterprise Mode Site List Manager を利用できるかどうかを設定できます。

このポリシーを有効にすると、Enterprise Mode Site List Manager のナビゲーション ボタンが edge://compat ページに表示されて、ユーザーはツールに移動して使用できます。

このポリシーを無効にするか構成しない場合、Enterprise Mode Site List Manager のナビゲーション ボタンは表示されず、ユーザーはツールを使用できません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: EnterpriseModeSiteListManagerAllowed
  - GP の名前: Enterprise Mode Site List Manager ツールへのアクセスを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: EnterpriseModeSiteListManagerAllowed
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  #### ドメインにおける指定されたファイルの種類に対して、ファイルの種類の拡張子に基づくダウンロードの警告を無効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 85

  #### 説明
  ファイルの種類の拡張子に基づくダウンロードの警告から除外される、ファイルの種類の拡張子および対応するドメインの一覧の辞書を作成する場合に、このポリシーを有効にできます。これにより、企業の管理者は、一覧にあるドメインに関連付けられたファイルに対する、ファイルの種類の拡張子に基づくダウンロードの警告をブロックできます。たとえば、"jnlp" 拡張子が "website1.com" に関連付けられている場合、"jnlp" ファイルを "website1.com" からダウンロードするときにユーザーに警告は表示されませんが、"jnlp" ファイルを "website2.com" からダウンロードすると、ダウンロードの警告が表示されます。

このポリシーで識別されるドメインに対して指定されているファイルの種類の拡張子を持つファイルであっても、コンテンツが混在している場合のダウンロードの警告や Microsoft Defender SmartScreen の警告など、ファイルの種類の拡張子ベースでないセキュリティの警告の対象にはなります。

このポリシーを無効にするか構成しない場合は、拡張子に基づくダウンロードの警告がトリガーされるファイルの種類については、警告がユーザーに表示されます。

このポリシーを有効にする場合:

* URL のパターンは [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) に従った書式にする必要があります。
* 入力するファイルの種類の拡張子は小文字の ASCII 文字にする必要があります。ファイルの種類の拡張子を一覧にするときは、先頭に区切り文字を含めないでください (".jnlp" ではなく "jnlp" を使用する必要があります)。

例:

次の例の値では、*.contoso.com ドメインの swf、exe、jnlp 拡張子に対してファイルの種類の拡張子に基づくダウンロードの警告が表示されなくなります。その他のドメインにおける exe と jnlp ファイルに対しては、ファイルの種類の拡張子に基づくダウンロードの警告がユーザーに表示されますが、swf ファイルに対しては表示されません。

[
  { "file_extension": "jnlp", "domains": ["contoso.com"] },
  { "file_extension": "exe", "domains": ["contoso.com"] },
  { "file_extension": "swf", "domains": ["*"] }
]

上記の例では、すべてのドメインの "swf" ファイルに対するファイルの種類の拡張子に基づくダウンロードの警告の抑制が示されていますが、すべてのドメインにおける危険なファイルの種類の拡張子に対してこのような警告を抑制することは、セキュリティ上の理由により推奨されていません。ここでは、このような機能があることを示す目的のためだけに例示されています。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - GP の名前: ドメインにおける指定されたファイルの種類に対して、ファイルの種類の拡張子に基づくダウンロードの警告を無効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\1 = {"domains": ["https://contoso.com", "contoso2.com"], "file_extension": "jnlp"}
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\2 = {"domains": ["*"], "file_extension": "swf"}

```


  #### Mac の情報と設定
  - 優先されるキーの名前: ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - サンプル値:
``` xml
<array>
  <string>{'domains': ['https://contoso.com', 'contoso2.com'], 'file_extension': 'jnlp'}</string>
  <string>{'domains': ['*'], 'file_extension': 'swf'}</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ExperimentationAndConfigurationServiceControl
  #### 実験および構成サービスとの通信を制御する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge では、実験および構成サービスを使用して実験および構成ペイロードを展開します。

実験ペイロードは、Microsoft がテストおよびフィードバックを有効にしている新しい開発機能のリストで構成されています。

構成ペイロードは、ユーザー エクスペリエンスを最適化するために Microsoft が Microsoft Edge に展開する設定のリストで構成されています。たとえば、構成ペイロードは、最新のペイロードを取得するために Microsoft Edge が実験および構成サービスに要求を送信する頻度を指定できます。

また、構成ペイロードには、互換性に対応するために特定のドメインで実行されるアクションのリストが含まれている場合があります。たとえば、Microsoft Edge での新しいユーザー エージェント文字列が原因で Web サイトが破損した場合、ブラウザーは Web サイト上のユーザー エージェント文字列を上書きする場合があります。こうしたアクションは一時的なものであり、Microsoft ではサイト所有者に関連する問題の解決を試行します。

このポリシーを「FullMode」に設定した場合、ペイロード全体は実験および構成サービスからダウンロードされます。これには、実験ペイロードと構成ペイロードの両方が含まれます。

このポリシーを「ConfigurationsOnlyMode」に設定した場合、構成ペイロードのみが提供されます。

このポリシーを「RestrictedMode」に設定した場合、実験および構成サービスとの通信は完全に停止します。

このポリシーを構成しなかった場合、安定版のチャネルとベータ版のチャネルのマネージド デバイスでは、動作が「ConfigurationsOnlyMode」と同じになります。

このポリシーを構成しなかった場合、アンマネージド デバイスでは、動作が「FullMode」と同じになります。

ポリシー オプションのマッピング:

* FullMode (2) = 構成と実験の取得

* ConfigurationsOnlyMode (1) = 構成のみを取得する

* RestrictedMode (0) = 実験および構成サービスとの通信を無効にする

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ExperimentationAndConfigurationServiceControl
  - GP の名前: 実験および構成サービスとの通信を制御する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ExperimentationAndConfigurationServiceControl
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ExperimentationAndConfigurationServiceControl
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ExternalProtocolDialogShowAlwaysOpenCheckbox
  #### 外部プロトコルのダイアログで [常に開く] チェック ボックスを表示する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 79

  #### 説明
  このポリシーは、外部プロトコルの起動確認メッセージに [このサイトがこの種類のリンクを開くことを常に許可する] チェックボックスを表示するかどうかを制御します。このポリシーは https:// links にのみ適用されます。

このポリシーを有効にすると、外部プロトコルの確認メッセージが表示されたときに、ユーザーが [常に許可する] を選択して、このサイトのプロトコルに関する今後の確認メッセージをすべてスキップできます。

このポリシーを無効にすると、[常に許可する] チェックボックスは表示されません。ユーザーは、外部プロトコルが呼び出されるたびに確認を求められます。

Microsoft Edge 83 より前でこのポリシーを構成しない場合は、[常に許可する] チェックボックスは表示されません。ユーザーは、外部プロトコルが呼び出されるたびに確認を求められます。

Microsoft Edge 83 でこのポリシーを構成しない場合は、チェックボックスの表示が edge://flags の [プロトコルの起動メッセージ設定の保存を有効にする] フラグによって制御されます。

Microsoft Edge 84 でこのポリシーを構成しない場合は、外部プロトコルの確認メッセージが表示されたときに、ユーザーが [常に許可する] を選択して、このサイトのプロトコルに関する今後の確認メッセージをすべてスキップできます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - GP の名前: 外部プロトコルのダイアログで [常に開く] チェック ボックスを表示する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ExternalProtocolDialogShowAlwaysOpenCheckbox
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### FamilySafetySettingsEnabled
  #### ユーザーが Family Safety を構成することを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 83

  #### 説明
  このポリシーは、[設定] の [Family Safety] ページを無効にし、完全に非表示にします。 edge://settings/familysafety へのナビゲーションもブロックされます。[Family Safety] ページには、ファミリー グループで利用できる機能と、ファミリー グループに参加する方法が記載されています。 Family Safety の詳細については、[https://go.microsoft.com/fwlink/?linkid=2098432](https://go.microsoft.com/fwlink/?linkid=2098432) を参照してください。

このポリシーを有効にした場合または構成しなかった場合、[Family Safety] ページが表示されます。

このポリシーを無効にした場合、[Family Safety] ページは表示されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: FamilySafetySettingsEnabled
  - GP の名前: ユーザーが Family Safety を構成することを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: FamilySafetySettingsEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: FamilySafetySettingsEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### FavoritesBarEnabled
  #### お気に入りバーを有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  お気に入りバーを有効または無効にします。

このポリシーを有効にすると、ユーザーにはお気に入りバーが表示されます。

このポリシーを無効にした場合、お気に入りバーはユーザーに表示されません。

このポリシーが構成されていない場合、ユーザーはお気に入りバーを使用するかどうかを選択できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: FavoritesBarEnabled
  - GP の名前: お気に入りバーを有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: FavoritesBarEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: FavoritesBarEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ForceBingSafeSearch
  #### Bing セーフサーチを適用する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Bing Web Search でのクエリが、指定された値に設定されたセーフサーチに基づいて実行されるようにします。ユーザーはこの設定を変更できません。

このポリシーを「BingSafeSearchNoRestrictionsMode」に構成すると、Bing Search のセーフサーチは Bing.com の値に戻ります。

このポリシーを「BingSafeSearchModerateMode」に構成すると、セーフサーチで中程度の設定が使用されます。中程度の設定では、検索結果で成人向けのビデオと画像がフィルターされますが、テキストはフィルターされません。

このポリシーを「BingSafeSearchStrictMode」に構成すると、セーフサーチで厳密な設定が使用されます。厳密な設定では、成人向けのテキスト、画像、ビデオがフィルターされます。

このポリシーを無効にした場合または構成しなかった場合、Bing Search のセーフサーチは適用されず、ユーザーは Bing.com で必要な値を設定できます。

ポリシー オプションのマッピング:

* BingSafeSearchNoRestrictionsMode (0) = Bing で検索制限を構成しない

* BingSafeSearchModerateMode (1) = Bing で中程度の検索制限を構成する

* BingSafeSearchStrictMode (2) = Bing で厳密な検索制限を構成する

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ForceBingSafeSearch
  - GP の名前: Bing セーフサーチを適用する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ForceBingSafeSearch
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ForceBingSafeSearch
  - サンプル値:
``` xml
<integer>0</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ForceCertificatePromptsOnMultipleMatches
  #### "AutoSelectCertificateForUrls" で構成されたサイトに複数の証明書が一致する場合、Microsoft Edge で証明書を自動的に選択するかどうかを構成します。
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 81

  #### 説明
  使用可能な証明書が複数あり、サイトが [AutoSelectCertificateForUrls](#autoselectcertificateforurls) で構成されている場合に、ユーザーに証明書の選択を求めるかどうかを切り替えます。サイトで [AutoSelectCertificateForUrls](#autoselectcertificateforurls) を構成しなかった場合、ユーザーは常に証明書を選択するように求められます。

このポリシーを True に設定した場合、Microsoft Edge は、ユーザーに対して、 [AutoSelectCertificateForUrls](#autoselectcertificateforurls) で定義されているリストにあるサイトの証明書を選択するように求められます。ただし、これは複数の証明書がある場合に限ります。

このポリシーを False に設定した場合または構成しなかった場合、Microsoft Edge では、証明書に一致するものが複数ある場合でも、自動的に証明書が選択されます。ユーザーは、 [AutoSelectCertificateForUrls](#autoselectcertificateforurls) で定義されたリストにあるサイトの証明書を選択するように求められません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ForceCertificatePromptsOnMultipleMatches
  - GP の名前: "AutoSelectCertificateForUrls" で構成されたサイトに複数の証明書が一致する場合、Microsoft Edge で証明書を自動的に選択するかどうかを構成します。
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ForceCertificatePromptsOnMultipleMatches
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ForceCertificatePromptsOnMultipleMatches
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ForceEphemeralProfiles
  #### 一時プロファイルの使用を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザー プロファイルを 一時モードに切り替えるかどうかを制御します。一時プロファイルは、セッションの開始時に作成され、セッションの終了時に削除されます。

このポリシーを有効にした場合、プロファイルは一時モードで実行されます。これにより、ユーザーはデバイスに閲覧データを保存しなくても、使用しているデバイスから作業を行うことができます。このポリシーを (Windows の GPO を使用するなどして) OS ポリシーとして有効にすると、システム上のすべてのプロファイルに適用されます。

このポリシーを無効にした場合、または構成しなかった場合、ユーザーにはブラウザーへのサインイン時に標準プロファイルが適用されます。

一時モードでは、ユーザー セッションの間のみプロファイル データがディスクに保存されます。ブラウザーの履歴、拡張機能とそのデータ、Cookie のような Web データ、また Web データベースなどの機能は、ブラウザーを閉じた後には保存されません。ユーザーはディスクに手動でデータをダウンロードしたり、ページを保存または印刷したりすることはできます。ユーザーが同期を有効にしている場合は、標準プロファイルと同様に、すべてのデータが同期アカウントに保持されます。明示的に無効にしていない限り、ユーザーは InPrivate ブラウズを一時モードで使用することもできます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ForceEphemeralProfiles
  - GP の名前: 一時プロファイルの使用を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ForceEphemeralProfiles
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ForceEphemeralProfiles
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ForceGoogleSafeSearch
  #### Google セーフサーチを適用する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  セーフサーチをアクティブに設定して実行される Google Web 検索でクエリを適用し、ユーザーがこの設定を変更できないようにします。

このポリシーを有効にした場合、Google 検索のセーフサーチは常にアクティブになります。

この設定を無効にした場合または構成しなかった場合、Google 検索のセーフサーチは適用されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ForceGoogleSafeSearch
  - GP の名前: Google セーフサーチを適用する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ForceGoogleSafeSearch
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ForceGoogleSafeSearch
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ForceLegacyDefaultReferrerPolicy
  #### no-referrer-when-downgrade の既定の参照ポリシーを使用 (非推奨)
  >非推奨: このポリシーは推奨されていません。現在サポートされていますが、将来のリリースでは使用されなくなります。
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 81

  #### 説明
  このポリシーは、現在の既定の参照ポリシーと互換性がないことが判明した場合に、企業が Web コンテンツを更新する時間を増やすための短期的なメカニズムとしてのみ使用されるため、廃止されました。バージョン 86 になると Microsoft Edge では機能しなくなります。

Microsoft Edge の既定の参照元ポリシーは、段階的なロールアウトを通じて、現在の値「no-referrer-when-downgrade」からさらに安全な「strict-origin-when-cross-origin」に変更され、セキュリティが強化されます。

ロールアウトまで、このエンタープライズ ポリシーは適用されません。ロールアウトの後、このエンタープライズ ポリシーが有効になっていると、Microsoft Edge の既定の参照元ポリシーがより前の値「no-referrer-when-downgrade」に設定されます。

このエンタープライズ ポリシーは既定で無効になっています。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ForceLegacyDefaultReferrerPolicy
  - GP の名前: no-referrer-when-downgrade の既定の参照ポリシーを使用 (非推奨)
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ForceLegacyDefaultReferrerPolicy
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ForceLegacyDefaultReferrerPolicy
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ForceNetworkInProcess
  #### ブラウザー プロセスでネットワーク コードを強制的に実行する (現在不使用)
  
  >古い形式: このポリシーは古い形式であり、Microsoft Edge 83 以降では使用することができません。
  #### サポートされているバージョン:
  - Windows から 78 までの 83

  #### 説明
  このポリシーは、ネットワーク API のフックに依存しないサード パーティのソフトウェアに移行するための時間を企業に与える短期的なメカニズムとして使用することのみが目的なため、機能しません。プロキシ サーバーは、LSP および Win32 API パッチ経由にすることをお勧めします。

このポリシーにより、ネットワーク コードがブラウザー プロセスで強制的に実行されます。

既定では、このポリシーは無効になっています。有効にした場合、ネットワーク プロセスがサンドボックス化されると、ユーザーがセキュリティの問題にさらされる可能性があります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ForceNetworkInProcess
  - GP の名前: ブラウザー プロセスでネットワーク コードを強制的に実行する (現在不使用)
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ForceNetworkInProcess
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ForceSync
  #### ブラウザー データの同期を強制し、同期の同意プロンプトを表示しない
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  Microsoft Edge でデータ同期を強制します。このポリシーにより、ユーザーは同期をオフにすることもできなくなります。

このポリシーを構成しない場合、ユーザーは同期をオンまたはオフにできます。このポリシーを有効にすると、ユーザーは同期をオフにできなくなります。

このポリシーを意図したとおりに機能させるには、
[BrowserSignin](#browsersignin) ポリシーを構成しないか、有効に設定する必要があります。[ForceSync](#forcesync) が無効に設定されている場合、[BrowserSignin](#browsersignin) は有効になりません。

[SyncDisabled](#syncdisabled) は構成しないか、False に設定する必要があります。これが True に設定されている場合、[ForceSync](#forcesync) は有効になりません。

0 = 自動的に同期を開始せず、同期の同意を表示する (既定)
1 = Azure AD/Azure AD-Degraded ユーザー プロファイルの同期を強制的にオンにし、同期の同意プロンプトを表示しない

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ForceSync
  - GP の名前: ブラウザー データの同期を強制し、同期の同意プロンプトを表示しない
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ForceSync
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ForceSync
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ForceYouTubeRestrict
  #### 最小限の YouTube の制限モードを強制する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  YouTube に最小限の制限モードを強制し、それより制限の少ないモードをユーザーが選択できないようにします。

「Strict」に設定すると、YouTube で厳格な制限モードを強制します。

「Moderate」に設定すると、YouTube で中程度の制限モードと厳格な制限モードのみの使用をユーザーに強制します。ユーザーは制限モードを無効にすることはできません。

このポリシーが「Off」に設定されているか、構成していない場合は、YouTube で制限モードを強制しません。YouTube ポリシーなどの外部ポリシーで、制限モードが引き続き適用される場合があります。

ポリシー オプションのマッピング:

* Off (0) = YouTube で厳格な制限モードを強制しない

* Moderate (1) = YouTube で少なくとも中程度の制限モードを強制する

* Strict (2) = YouTube に厳格な制限モードを強制する

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ForceYouTubeRestrict
  - GP の名前: 最小限の YouTube の制限モードを強制する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ForceYouTubeRestrict
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ForceYouTubeRestrict
  - サンプル値:
``` xml
<integer>0</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### FullscreenAllowed
  #### 全画面表示モードを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 77

  #### 説明
  全画面表示モードを使用できるかどうかを設定します。この表示モードでは、すべての Microsoft Edge の UI が非表示になり、Web コンテンツのみが表示されます。

このポリシーを有効にした場合または構成しなかった場合、適切なアクセス許可を持つユーザー、アプリ、拡張機能を全画面表示モードに切り替えることができます。

このポリシーを無効にした場合、ユーザー、アプリ、拡張機能は全画面表示モードに切り替えることはできません。

全画面表示モードが無効になっていると、コマンド ラインを使用してMicrosoft Edge をキオスク モードで開くことはできません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: FullscreenAllowed
  - GP の名前: 全画面表示モードを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: FullscreenAllowed
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### GloballyScopeHTTPAuthCacheEnabled
  #### グローバルにスコープが設定された HTTP 認証キャッシュを有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 81

  #### 説明
  このポリシーでは、HTTP サーバーの認証資格情報を使用して、プロファイルごとにグローバル キャッシュを 1 つ構成します。

このポリシーを無効にした場合または設定しなかった場合、ブラウザではクロスサイト認証の既定の動作が使用されます。つまりバージョン 80 以降、HTTP サーバーの認証資格情報のスコープはトップレベル サイトによって区切られます。したがって、2 つのサイトで同じ認証ドメインからのリソースを使用している場合は、両方のサイトのコンテキストごとに資格情報を提供する必要があります。サイト間では、キャッシュされたプロキシ資格情報が再利用されます。

このポリシーを有効にした場合、1 つのサイトのコンテキストで入力された HTTP 認証資格情報が、別のサイトのコンテキストでも自動的に使用されます。

このポリシーを有効にすると、サイトは一部の種類のクロスサイト攻撃にさらされることになります。また、URL に埋め込まれた資格情報を使用して HTTP 認証キャッシュにエントリを追加することで、Cookie がなくてもサイト間でユーザーを追跡できるようになります。

このポリシーの目的は、従来の動作に依存している企業にキャッシュを与えて、ログインの手続きを更新できるようにすることです。このポリシーは将来削除される予定です。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: GloballyScopeHTTPAuthCacheEnabled
  - GP の名前: グローバルにスコープが設定された HTTP 認証キャッシュを有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: GloballyScopeHTTPAuthCacheEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: GloballyScopeHTTPAuthCacheEnabled
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### GoToIntranetSiteForSingleWordEntryInAddressBar
  #### アドレス バーへの 1 単語の入力で検索するのではなく、ダイレクト イントラネット サイト ナビゲーションを強制します
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 78

  #### 説明
  このポリシーを有効にした場合、アドレス バーの候補リストで先頭に示される自動提案の結果によって、イントラネット サイトに移動されます (アドレス バーに入力されたテキストが句読点を含まない 1 単語であるとき)。

句読点を含まない 1 単語を入力したときの既定のナビゲーションでは、入力したテキストに一致するイントラネット サイトへの移動が実施されます。

このポリシーを有効にした場合、アドレス バーの候補リストに示される自動提案の 2 番目の結果によって、入力されたとおりに Web 検索が実施されます (入力されたテキストが句読点を含まない 1 単語であるとき)。Web 検索を禁止するポリシーが有効になっている場合を除き、既定の検索プロバイダーが使用されます。

このポリシーを有効にした場合の 2 つの効果は次のとおりです。

履歴の項目に通常解決される 1 単語のクエリに対応するサイトへのナビゲーションは、実施されなくなります。代わりに、ブラウザーは、組織のイントラネットに存在しない可能性がある内部サイトへ移動しようとします。この結果、404 エラーが発生します。

よく使用される 1 単語の検索語句では、検索を適切に実行するために検索候補の手動選択が必要になります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: GoToIntranetSiteForSingleWordEntryInAddressBar
  - GP の名前: アドレス バーへの 1 単語の入力で検索するのではなく、ダイレクト イントラネット サイト ナビゲーションを強制します
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: GoToIntranetSiteForSingleWordEntryInAddressBar
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: GoToIntranetSiteForSingleWordEntryInAddressBar
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### HSTSPolicyBypassList
  #### HSTS ポリシー チェックをバイパスする名前の一覧を構成します
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 79

  #### 説明
  この一覧に指定されたホスト名は、"http://" からの要求を "https://" にアップグレードする可能性がある HSTS ポリシー チェックから除外されます。このポリシーでは、単一ラベルのホスト名のみが許可されます。ホスト名は正規化する必要があります。IDN は A-ラベル形式に変換する必要があり、ASCII 文字はすべて小文字にする必要があります。このポリシーは指定された特定のホスト名にのみ適用され、一覧に含まれる名前のサブドメインには適用されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: HSTSPolicyBypassList
  - GP の名前: HSTS ポリシー チェックをバイパスする名前の一覧を構成します
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList\1 = "meet"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: HSTSPolicyBypassList
  - サンプル値:
``` xml
<array>
  <string>meet</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### HardwareAccelerationModeEnabled
  #### 使用可能な場合はハードウェア アクセラレータを使用する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ハードウェア アクセラレータが使用可能な場合は、これを使用するように指定します。このポリシーを有効にした場合または構成しなかった場合、GPU 機能が明示的にブロックされていない限り、ハードウェア アクセラレータが有効になります。

このポリシーを無効にした場合、ハードウェア アクセラレータは無効になります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: HardwareAccelerationModeEnabled
  - GP の名前: 使用可能な場合はハードウェア アクセラレータを使用する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: HardwareAccelerationModeEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: HardwareAccelerationModeEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### HideFirstRunExperience
  #### 最初の実行エクスペリエンスとスプラッシュ スクリーンを非表示にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 80

  #### 説明
  このポリシーを有効にした場合、Microsoft Edge を初めて実行したときに、初回実行エクスペリエンスとスプラッシュ スクリーンが、ユーザーに対して表示されなくなります。

初回実行エクスペリエンスに表示される構成オプションでは、ブラウザーの既定の設定は次のようになっています。

- 新しいタブ ページでは、フィードの種類は MSN ニュースに、レイアウトはインスピレーションに設定されます。

- Windows アカウントの種類が Azure AD または MSA であれば、ユーザーは Microsoft Edge に自動的にサインインされます。

- 既定では、同期は有効になりません。ユーザーは同期の設定から同期を有効にすることができます。

このポリシーを無効にした場合または構成しなかった場合、初回実行エクスペリエンスとスプラッシュ スクリーンが表示されます。

注意: 初回実行エクスペリエンスでユーザーに表示される特定の構成オプションは、他の特定のポリシーを使用して管理することもできます。HideFirstRunExperience ポリシーをこれら特定のポリシーと組み合わせて使用すると、マネージド デバイスにおける特定のブラウザー エクスペリエンスを構成できます。こうした組み合わせに使用できるポリシーの一部を次に示します。

-[AutoImportAtFirstRun](#autoimportatfirstrun)

-[NewTabPageLocation](#newtabpagelocation)

-[NewTabPageSetFeedType](#newtabpagesetfeedtype)

-[SyncDisabled](#syncdisabled)

-[BrowserSignin](#browsersignin)

-[NonRemovableProfileEnabled](#nonremovableprofileenabled)

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: HideFirstRunExperience
  - GP の名前: 最初の実行エクスペリエンスとスプラッシュ スクリーンを非表示にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: HideFirstRunExperience
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: HideFirstRunExperience
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ImportAutofillFormData
  #### オートフィルのフォーム データのインポートを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザーは、オートフィルのフォーム データを別のブラウザーから Microsoft Edge にインポートできます。

このポリシーを有効にした場合、オートフィルのフォーム データを手動でインポートするオプションが自動的に選択されます。

このポリシーを無効にした場合、オートフィルのフォーム データは初回実行時にインポートされず、またユーザーは手動でインポートすることもできません。

このポリシーを構成しなかった場合、オートフィルのデータは初回実行時にインポートされます。ユーザーは、後で閲覧セッションを実行しているときに、このデータを手動でインポートするかどうかを選択できます。

このポリシーは推奨事項として設定できます。つまり、Microsoft Edge では、初回起動時にオートフィルのデータがインポートされますが、ユーザーは、手動でインポートする際に **オートフィルのデータ** に関するオプションを選択したり、クリアしたりすることができます。

**注意**: 現在このポリシーでは、Google Chrome (Windows 7、8、10、および macOS)、Mozilla Firefox (Windows 7、8、10、および macOS) の各ブラウザーからのインポートを管理します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ImportAutofillFormData
  - GP の名前: オートフィルのフォーム データのインポートを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: ImportAutofillFormData
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ImportAutofillFormData
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ImportBrowserSettings
  #### ブラウザーの設定のインポートを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 78

  #### 説明
  ユーザーは、ブラウザーの設定を別のブラウザーから Microsoft Edge にインポートできます。

このポリシーを有効にした場合、**ブラウザー設定** ダイアログ ボックスにある **ブラウザー データをインポートする** チェック ボックスが自動的に選択されます。

このポリシーを無効にした場合、ブラウザーの設定は初回実行時にインポートされず、またユーザーは手動でインポートすることもできません。

このポリシーを構成しなかった場合、ブラウザーの設定は初回実行時にインポートされます。ユーザーは、後で閲覧セッションを実行しているときに、ブラウザーの設定を手動でインポートするかどうかを選択できます。

このポリシーは推奨事項として設定できます。つまり、Microsoft Edge では、初回起動時にブラウザーの設定がインポートされますが、ユーザーは、手動でインポートする際に**ブラウザーの設定**に関するオプションを選択したり、クリアしたりすることができます。

**注意:** 現在このポリシーでは、Google Chrome (Windows 7、8、10、および macOS) からのインポートを管理します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ImportBrowserSettings
  - GP の名前: ブラウザーの設定のインポートを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: ImportBrowserSettings
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ImportBrowserSettings
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ImportCookies
  #### Cookie のインポートを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 81

  #### 説明
  ユーザーは、Cookie を別のブラウザーから Microsoft Edge にインポートできます。

このポリシーを無効にした場合、Cookie は初回実行時にインポートされません。

このポリシーを構成しなかった場合、Cookie は初回実行時にインポートされます。

このポリシーは推奨事項として設定できます。つまり、Microsoft Edge では、初回起動時に Cookie がインポートされます。

**注意:** 現在このポリシーでは、Google Chrome (Windows 7、8、10、および macOS) からのインポートを管理します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ImportCookies
  - GP の名前: Cookie のインポートを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: ImportCookies
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ImportCookies
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ImportExtensions
  #### 拡張機能のインポートを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 81

  #### 説明
  ユーザーは、拡張機能を別のブラウザーから Microsoft Edge にインポートできます。

このポリシーを有効にした場合、**[ブラウザー データのインポート]** ダイアログ ボックスにある **[拡張機能]** チェック ボックスが自動的にオンになります。

このポリシーを無効にした場合、拡張機能は初回実行時にインポートされず、またユーザーは手動でインポートすることもできません。

このポリシーを構成しなかった場合、拡張機能は初回実行時にインポートされます。ユーザーは、後で閲覧セッションを実行しているときに、拡張機能を手動でインポートするかどうかを選択できます。

このポリシーは推奨事項として設定できます。つまり、Microsoft Edge では、拡張機能が初回起動時にインポートされますが、ユーザーは、手動でインポートする際に **[お気に入り]** オプションをオンにしたり、オフにしたりすることができます。

**注意:** 現在このポリシーでは、Google Chrome (Windows 7、8、10、および macOS) からのインポートのみをサポートします。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ImportExtensions
  - GP の名前: 拡張機能のインポートを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: ImportExtensions
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ImportExtensions
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ImportFavorites
  #### お気に入りのインポートを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザーは、お気に入りを別のブラウザーから Microsoft Edge にインポートできます。

このポリシーを有効にした場合、**お気に入り** ダイアログ ボックスの **ブラウザー データのインポート** チェック ボックスが自動的にオンになります。

このポリシーを無効にした場合、初回実行時にお気に入りはインポートされず、またユーザーはお気に入りを手動でインポートすることもできません。

このポリシーを構成しなかった場合、初回実行時にお気に入りがインポートされます。ユーザーは、後で閲覧セッションを実行しているときに、お気に入りを手動でインポートするかどうかを選択できます。

このポリシーは推奨事項として設定できます。つまり、Microsoft Edge では、初回起動時にお気に入りがインポートされますが、ユーザーは、手動でインポートする際に **お気に入り** に関するオプションを選択したり、クリアしたりすることができます。

**注意**: 現在このポリシーでは、Internet Explorer (Windows 7、8、10)、Google Chrome (Windows 7、8、10、および macOS)、Mozilla Firefox (Windows 7、8、10、および macOS)、Apple Safari (macOS) の各ブラウザーからのインポートを管理します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ImportFavorites
  - GP の名前: お気に入りのインポートを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: ImportFavorites
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ImportFavorites
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ImportHistory
  #### 閲覧の履歴のインポートを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザーは、閲覧の履歴を別のブラウザーから Microsoft Edge にインポートできます。

このポリシーを有効にした場合、**閲覧の履歴** ダイアログ ボックスの **ブラウザー データのインポート** チェック ボックスが自動的にオンになります。

このポリシーを無効にした場合、初回実行時に閲覧の履歴データはインポートされず、またユーザーはこのデータを手動でインポートすることもできません。

このポリシーを構成しなかった場合、初回実行時に閲覧の履歴データがインポートされます。ユーザーは、後で閲覧セッションを実行しているときに、このデータを手動でインポートするかどうかを選択できます

このポリシーは推奨事項として設定できます。つまり、Microsoft Edge では、初回起動時に閲覧の履歴がインポートされますが、ユーザーは、手動でインポートする際に **履歴** に関するオプションを選択したり、クリアしたりすることができます。

**注意**: 現在このポリシーでは、Internet Explorer (Windows 7、8、10)、Google Chrome (Windows 7、8、10、および macOS)、Mozilla Firefox (Windows 7、8、10、および macOS)、Apple Safari (macOS) の各ブラウザーからのインポートを管理します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ImportHistory
  - GP の名前: 閲覧の履歴のインポートを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: ImportHistory
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ImportHistory
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ImportHomepage
  #### ホーム ページの設定のインポートを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザーは、ホーム ページの設定を別のブラウザーから Microsoft Edge にインポートできます。

このポリシーを有効にした場合、ホーム ページの設定を手動でインポートするオプションが自動的に選択されます。

このポリシーを無効にした場合、ホーム ページの設定は初回実行時にインポートされず、またユーザーは手動でインポートすることもできません。

このポリシーを構成しなかった場合、ホーム ページの設定は初回実行時にインポートされます。ユーザーは、後で閲覧セッションを実行しているときに、このデータを手動でインポートするかどうかを選択できます。

このポリシーは推奨事項として設定できます。つまり、Microsoft Edge では、初回起動時にホーム ページの設定がインポートされますが、ユーザーは、手動でインポートする際に **ホーム ページ** に関するオプションを選択したり、クリアしたりすることができます。

**注意**: 現在このポリシーでは、Internet Explorer (Windows 7、8、10) からのインポートを管理します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ImportHomepage
  - GP の名前: ホーム ページの設定のインポートを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ImportHomepage
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ImportHomepage
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ImportOpenTabs
  #### 開いているタブのインポートを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 79

  #### 説明
  ユーザーは、開いているタブやピン留めされたタブを別のブラウザーから Microsoft Edge にインポートできます。

このポリシーを有効にした場合、**[ブラウザー データのインポート]** ダイアログ ボックスにある **[開いているタブ]** チェック ボックスが自動的にオンになります。

このポリシーを無効にした場合、開いているタブは初回実行時にインポートされず、またユーザーは手動でインポートすることもできません。

このポリシーを構成しなかった場合、開いているタブは初回実行時にインポートされます。ユーザーは、後で閲覧セッションを実行しているときに、開いているタブを手動でインポートするかどうかを選択できます。

このポリシーは推奨事項として設定できます。つまり、Microsoft Edge では、開いているタブが初回起動時にインポートされますが、ユーザーは、手動でインポートする際に **[開いているタブ]** オプションをオンにしたり、オフにしたりすることができます。

**注意:** 現在このポリシーでは、Google Chrome (Windows 7、8、10、および macOS) からのインポートのみをサポートします。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ImportOpenTabs
  - GP の名前: 開いているタブのインポートを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: ImportOpenTabs
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ImportOpenTabs
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ImportPaymentInfo
  #### 支払情報のインポートを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザーは、支払情報を別のブラウザーから Microsoft Edge にインポートできます。

このポリシーを有効にした場合、**支払情報** ダイアログ ボックスにある **ブラウザー データをインポートする** チェック ボックスが自動的に選択されます。

このポリシーを無効にした場合、支払情報は初回実行時にインポートされず、またユーザーは手動でインポートすることもできません。

このポリシーを構成しなかった場合、支払情報は初回実行時にインポートされます。ユーザーは、後で閲覧セッションを実行しているときに、支払情報を手動でインポートするかどうかを選択できます。

このポリシーは推奨事項として設定できます。つまり、Microsoft Edge では、初回起動時に支払情報がインポートされますが、ユーザーは、手動でインポートする際に **支払情報** に関するオプションを選択したり、クリアしたりすることができます。

**注意:** 現在このポリシーでは、Google Chrome (Windows 7、8、10、および macOS) からのインポートを管理します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ImportPaymentInfo
  - GP の名前: 支払情報のインポートを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: ImportPaymentInfo
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ImportPaymentInfo
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ImportSavedPasswords
  #### 保存したパスワードのインポートを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザーは、保存したパスワードを別のブラウザーから Microsoft Edge にインポートできます。

このポリシーを有効にした場合、保存したパスワードを手動でインポートするオプションが自動的に選択されます。

このポリシーを無効にした場合、保存したパスワードは初回実行時にインポートされず、またユーザーは手動でインポートすることもできません。

このポリシーを構成しなかった場合、パスワードは初回実行時にインポートされます。ユーザーは、後で閲覧セッションを実行しているときに、パスワードを手動でインポートするかどうかを選択できます

このポリシーは推奨事項として設定できます。つまり、Microsoft Edge では、初回起動時にパスワードがインポートされますが、ユーザーは、手動でインポートする際に **パスワード** に関するオプションを選択したり、クリアしたりすることができます。

**注意**: 現在このポリシーでは、Internet Explorer (Windows 7、8、10)、Google Chrome (Windows 7、8、10、および macOS)、Mozilla Firefox (Windows 7、8、10、および macOS) の各ブラウザーからのインポートを管理します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ImportSavedPasswords
  - GP の名前: 保存したパスワードのインポートを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: ImportSavedPasswords
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ImportSavedPasswords
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ImportSearchEngine
  #### 検索エンジンの設定のインポートを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザーは、検索エンジンの設定を別のブラウザーから Microsoft Edge にインポートできます。

このポリシーを有効にした場合、検索エンジンの設定を手動でインポートするオプションが自動的に選択されます。

このポリシーを無効にした場合、検索エンジンの設定は初回実行時にインポートされず、またユーザーは手動でインポートすることもできません。

このポリシーを構成しなかった場合、検索エンジンの設定は初回実行時にインポートされます。ユーザーは、後で閲覧セッションを実行しているときに、このデータを手動でインポートするかどうかを選択できます。

このポリシーは推奨事項として設定できます。つまり、Microsoft Edge では、初回起動時に検索エンジンの設定がインポートされますが、ユーザーは、手動でインポートする際に **検索エンジンの設定** に関するオプションを選択したり、クリアしたりすることができます。

**注意**: 現在このポリシーでは、Internet Explorer (Windows 7、8、10) からのインポートを管理します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ImportSearchEngine
  - GP の名前: 検索エンジンの設定のインポートを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: ImportSearchEngine
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ImportSearchEngine
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ImportShortcuts
  #### ショートカットのインポートを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 81

  #### 説明
  ユーザーは、ショートカットを別のブラウザーから Microsoft Edge にインポートできます。

このポリシーを無効にした場合、ショートカットは初回実行時にインポートされません。

このポリシーを構成しなかった場合、ショートカットは初回実行時にインポートされます。

このポリシーは推奨事項として設定できます。つまり、Microsoft Edge では、初回起動時にショートカットがインポートされます。

**注意:** 現在このポリシーでは、Google Chrome (Windows 7、8、10、および macOS) からのインポートを管理します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ImportShortcuts
  - GP の名前: ショートカットのインポートを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: ImportShortcuts
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ImportShortcuts
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### InPrivateModeAvailability
  #### InPrivate モードが利用できるかどうかを構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザーが Microsoft Edge で InPrivate モードを使用してページを開くことができるかどうかを指定します。

このポリシーを構成しなかった場合または「Enabled」に設定した場合、ユーザーは InPrivate モードでページを開くことができます。

このポリシーを「Disabled」に設定した場合、ユーザーは InPrivate モードを使用できません。

このポリシーを「Forced」に設定した場合、常に InPrivate モードが使用されます。

ポリシー オプションのマッピング:

* Enabled (0) = InPrivate モードが利用可能

* Disabled (1) = 無効な InPrivate モード

* Forced (2) = InPrivate モードを強制実行しました

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: InPrivateModeAvailability
  - GP の名前: InPrivate モードが利用できるかどうかを構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: InPrivateModeAvailability
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: InPrivateModeAvailability
  - サンプル値:
``` xml
<integer>1</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### InsecureFormsWarningsEnabled
  #### セキュリティで保護されていないフォームの警告を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  このポリシーは、ブラウザーの安全な (HTTPS) サイトに埋め込まれた安全でないフォーム (HTTP 経由で送信されたフォーム) の処理を制御します。
このポリシーを有効にするか、設定しない場合、安全でないフォームが送信されると、ページ全体の警告が表示されます。さらに、フォーカスされたフォーム フィールドの横に警告の吹き出しが表示され、それらのフォームの自動入力が無効になります。
このポリシーを無効にすると、安全でないフォームの警告は表示されず、自動入力は正常に機能します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: InsecureFormsWarningsEnabled
  - GP の名前: セキュリティで保護されていないフォームの警告を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: InsecureFormsWarningsEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: InsecureFormsWarningsEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### IntensiveWakeUpThrottlingEnabled
  #### IntensiveWakeUpThrottling 機能を制御する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 85

  #### 説明
  IntensiveWakeUpThrottling 機能を有効にすると、バックグラウンド タブの JavaScript タイマーが積極的に調整および結合され、ページが 5 分以上バックグラウンド化された後、毎分 1 回だけ実行されます。

 これは Web 標準に準拠した機能ですが、特定のアクションを最大 1 分遅延させることにより、一部の Web サイトの機能を中断する可能性があります。 ただし、有効にすると、CPU とバッテリーが大幅に節約されます。詳細については、https://bit.ly/30b1XR4 を参照してください

 このポリシーを有効にすると、機能が強制的に有効になり、ユーザーはこの設定を上書きできなくなります。
 このポリシーを無効にすると、機能が強制的に無効になり、ユーザーはこの設定を上書きできなくなります。
 このポリシーを構成しない場合、機能は独自の内部ロジックによって制御されます。 ユーザーはこの設定を手動で構成できます。

ポリシーはレンダラー プロセスごとに適用され、レンダラー プロセスの開始時にポリシー設定の最新の値が有効になることに注意してください。ロードされたすべてのタブが一貫したポリシー設定を受け取るようにするには、完全な再起動が必要です。プロセスがこのポリシーの異なる値で実行されていることは無害です。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: IntensiveWakeUpThrottlingEnabled
  - GP の名前: IntensiveWakeUpThrottling 機能を制御する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: IntensiveWakeUpThrottlingEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: IntensiveWakeUpThrottlingEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### InternetExplorerIntegrationEnhancedHangDetection
  #### Internet Explorer モードの拡張ハング検出を構成
  
  
  #### サポートされているバージョン:
  - Windows 以降の 84

  #### 説明
  拡張ハング検出は、スタンドアロン Internet Explorer が使用するものよりも、Internet Explorer モードでハングした Web ページを検出するためのより詳細なアプローチです。ハングした Web ページが検出されると、ブラウザーは緩和策を適用して、ブラウザーの残りの部分がハングするのを防ぎます。

 この設定により、どの Web サイトとも互換性のない問題が発生した場合に拡張ハング検出の使用を構成できます。このポリシーは、Internet Explorer モードで「(Web サイトが応答しない)」という通知が表示され、スタンドアロンの Internet Explorer では表示されない場合にのみ、このポリシーを無効にすることをお勧めします。

 この設定は、以下と連動します。
 [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) が「IEMode」に設定されている (1)
 および
 リストに少なくとも 1 つのエントリがある [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) ポリシーである場合。

 このポリシーを「Enabled」に設定した場合または構成していない場合、InternetExplorer モードで実行されている Web サイトは拡張ハング検出を使用します。

このポリシーを「Disabled」に設定すると、拡張ハング検出が無効になり、ユーザーは基本的な Internet Explorer ハング検出動作を取得します。

 Internet Explorer モードの詳細については、[https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210) を参照してください

ポリシー オプションのマッピング:

* Disabled (0) = 拡張ハング検出が無効になっています

* Enabled (1) = 拡張ハング検出が有効になっています

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: InternetExplorerIntegrationEnhancedHangDetection
  - GP の名前: Internet Explorer モードの拡張ハング検出を構成
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: InternetExplorerIntegrationEnhancedHangDetection
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### InternetExplorerIntegrationLevel
  #### Internet Explorer 統合を構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 77

  #### 説明
  Internet Explorer モードに最適なエクスペリエンスを構成するガイダンスについては、[https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210) を参照してください

ポリシー オプションのマッピング:

* None (0) = なし

* IEMode (1) = Internet Explorer モード

* NeedIE (2) = Internet Explorer 11

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: InternetExplorerIntegrationLevel
  - GP の名前: Internet Explorer 統合を構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: InternetExplorerIntegrationLevel
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### InternetExplorerIntegrationSiteList
  #### エンタープライズ モード サイト一覧を構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 78

  #### 説明
  Internet Explorer モードに最適なエクスペリエンスを構成するガイダンスについては、[https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210) を参照してください

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: InternetExplorerIntegrationSiteList
  - GP の名前: エンタープライズ モード サイト一覧を構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: InternetExplorerIntegrationSiteList
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"https://internal.contoso.com/sitelist.xml"
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### InternetExplorerIntegrationSiteRedirect
  #### Internet Explorer モードのページから開始した場合、未構成のサイトへの "ページ内" ナビゲーションがどのように動作するかを指定する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 81

  #### 説明
  「ページ内」ナビゲーションは、現在のページ上にあるリンク、スクリプト、またはフォームから始まります。また「ページ内」ナビゲーションが、前回行った「ページ内」ナビゲーションのサーバー側リダイレクトになる場合もあります。これに対して、ユーザーは、ブラウザー コントロールを使用したいくつかの方法で、現在のページに依存しない「ページ内」以外のナビゲーションを開始することができます。たとえば、アドレス バー、[戻る] ボタン、お気に入りのリンクを使用します。

この設定では、Internet Explorer モードで読み込まれたページから未構成のサイト (エンタープライズ モード サイト一覧に構成されていないサイト) へのナビゲーションを Microsoft Edge に戻すか、Internet Explorer モードのままにしておくかどうかを指定できます。

この設定は、以下の操作と連動して機能します:
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) を「IEMode」に設定する
および
エンタープライズ モード サイト一覧に少なくとも 1 つのエントリが含まれるように、[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) ポリシーを構成する

このポリシーを無効にした場合または構成しなかった場合、Internet Explorer モードで開くように構成されたサイトのみが、そのモードで開きます。Internet Explorer モードで開くように構成されていないサイトは、Microsoft Edge にリダイレクトされます。

このポリシーを Default に設定した場合、Internet Explorer モードで開くように構成されたサイトのみが、そのモードで開きます。Internet Explorer モードで開くように構成されていないサイトは、Microsoft Edge にリダイレクトされます。

このポリシーを「AutomaticNavigationsOnly」に設定した場合、既定のエクスペリエンスが Internet Explorer モードで維持されます。ただし、未構成のサイトへの自動ナビゲーション (302 リダイレクトなど) はすべて、このオプションの対象外となります。

このポリシーを「AllInPageNavigations」に設定した場合、IE モードで読み込まれたページから未構成のサイトへのすべてのナビゲーションが Internet Explorer モードで維持されます (ほとんどの場合に推奨されません)。

Internet Explorer モードの詳細については、[https://go.microsoft.com/fwlink/?linkid=2105106](https://go.microsoft.com/fwlink/?linkid=2105106) を参照してください

ポリシー オプションのマッピング:

* Default (0) = 既定

* AutomaticNavigationsOnly (1) = 自動ナビゲーションのみを Internet Explorer モードで維持する

* AllInPageNavigations (2) = すべてのページ内ナビゲーション を Internet Explorer モードで維持する

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: InternetExplorerIntegrationSiteRedirect
  - GP の名前: Internet Explorer モードのページから開始した場合、未構成のサイトへの "ページ内" ナビゲーションがどのように動作するかを指定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: InternetExplorerIntegrationSiteRedirect
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### InternetExplorerIntegrationTestingAllowed
  #### Internet Explorer モードのテストを許可
  
  
  #### サポートされているバージョン:
  - Windows 以降の 86

  #### 説明
  このポリシーは、ie-mode-test フラグ ポリシーに代わるものです。これにより、ユーザーは UI メニュー オプションから IE モード タブを開くことができます。

この設定は、以下と連動して機能します。
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) が「IEMode」に設定されている
および
[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) ポリシー リストに少なくとも 1 つのエントリがあります。

このポリシーを有効にすると、ユーザーは UI オプションから IE モードのタブを開き、現在のサイトを IE モードのサイトに移動できます。

無効にした場合、このポリシーでは、ユーザーはメニューに直接 UI オプションを表示できません。

このポリシーを構成しない場合は、ie-mode-test フラグを手動で設定できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: InternetExplorerIntegrationTestingAllowed
  - GP の名前: Internet Explorer モードのテストを許可
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: InternetExplorerIntegrationTestingAllowed
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### IsolateOrigins
  #### 特定の出所に対してサイトの分離を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  独自のプロセスで分離して実行されるオリジンを指定します。
またこのポリシーでは、サブドメインによって指定されたオリジンも分離されます。たとえば、https://contoso.com/ と指定すると、https://foo.contoso.com/ が https://contoso.com/ サイトの一部として 分離されます。
このポリシーを有効にした場合、コンマ区切りのリスト内にある指定のオリジンは、それぞれ独自のプロセスで実行されます。
このポリシーを無効にした場合、'IsolateOrigins' 機能と 'SitePerProcess' 機能はどちらも無効になります。ただしユーザーは、コマンド ライン フラグを使用して、手動で 'IsolateOrigins' ポリシーを有効にすることができます。
このポリシーを構成しなかった場合、ユーザーはこの設定を変更できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: IsolateOrigins
  - GP の名前: 特定の出所に対してサイトの分離を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: IsolateOrigins
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"https://contoso.com/,https://fabrikam.com/"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: IsolateOrigins
  - サンプル値:
``` xml
<string>https://contoso.com/,https://fabrikam.com/</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### LocalProvidersEnabled
  #### ローカル プロバイダーからの提案を許可
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 83

  #### 説明
  Microsoft Edge のアドレス バーと自動提案リストで、デバイスの提案プロバイダー (ローカル プロバイダー) からの提案 (お気に入りや閲覧履歴など) を許可します。

このポリシーを有効にすると、ローカル プロバイダーからの提案が使用されます。

このポリシーを無効にすると、ローカル プロバイダーからの提案は使用されません。ローカルの履歴とローカルのお気に入りの提案は表示されません。

このポリシーを構成しない場合、ローカル プロバイダーからの提案は許可されますが、ユーザーは設定の切り替えを使用して変更できます。

この機能を無効にするポリシーが適用されている場合、機能を使用できない場合があります。たとえば、[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled) ポリシーを有効にすると、閲覧履歴の提案は使用できなくなります。

このポリシーを適用するには、ブラウザーを再起動する必要があります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: LocalProvidersEnabled
  - GP の名前: ローカル プロバイダーからの提案を許可
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: LocalProvidersEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: LocalProvidersEnabled
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ManagedFavorites
  #### お気に入りを構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  管理対象のお気に入りのリストを構成します。

このポリシーによって、お気に入りのリストが作成されます。各お気に入りには、キーとなる "name" と "url" が含まれており、これらのキーはお気に入りの名前とターゲットを保持します。"url" キーを使用せずに、追加の "children" キーを使用してお気に入りを定義することによって、サブフォルダーを構成できます。"children" キーには、上で定義したお気に入りのリストが含まれています (これらのお気に入りの一部は再度フォルダーとして含まれる場合があります)。Microsoft Edge は、不完全な URL をアドレス バーから送信された URL のように修正します。たとえば、"microsoft.com" は "https://microsoft.com/" となります。

これらのお気に入りは、ユーザーが変更できないフォルダーに配置されます (ただし、お気に入りバーでこのフォルダーが非表示になるように選択することはできます)。既定では、フォルダー名は "Managed favorites" ですが、必要なフォルダー名を値として持つ "toplevel_name" キーを含んでいるディクショナリをお気に入りのリストに追加することで、フォルダー名を変更できます。

管理対象のお気に入りは、ユーザー アカウントとは同期されず、拡張機能によって変更することはできません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 辞書

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ManagedFavorites
  - GP の名前: お気に入りを構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ManagedFavorites
  - 値の種類: REG_SZ
  ##### サンプル値:
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


  #### Mac の情報と設定
  - 優先されるキーの名前: ManagedFavorites
  - サンプル値:
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
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ManagedSearchEngines
  #### 検索エンジンの管理
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  最大 10 個の検索エンジンが含まれるリストを構成できます。検索エンジンのいずれか一つは、既定の検索エンジンとしてマークする必要があります。
     エンコードを指定する必要はありません。Microsoft Edge 80 以降では、suggest_url パラメーターと image_search_url パラメーターはオプションです。オプションのパラメーターである image_search_post_params (コンマで区切られた名前と値のペアで構成されます) は、Microsoft Edge80 以降で利用できます。

Microsoft Edge 83 以降では、オプションのパラメーターである allow_search_engine_discovery を使用して、検索エンジンによる検出を有効にすることができます。このパラメーターは、リスト内の最初の項目として指定する必要があります。allow_search_engine_discovery を指定しないと、検索エンジンによる検出は既定では無効になります。Microsoft Edge84以降、このポリシーを推奨ポリシーとして設定して、検索プロバイダーの検出を許可できます。

このポリシーを有効にした場合、ユーザーはリスト内の検索エンジンを追加、削除、または変更できません。ユーザーは、リスト内のどの検索エンジンでも既定の検索エンジンとして設定できます。

このポリシーを無効にした場合または構成しなかった場合、ユーザーは検索エンジンのリストを必要に応じて変更できます。

[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)ポリシーを設定した場合、このポリシー (ManagedSearchEngines) は無視されます。このポリシーの適用を完了するには、ユーザーはブラウザーを再起動する必要があります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 辞書

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ManagedSearchEngines
  - GP の名前: 検索エンジンの管理
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: ManagedSearchEngines
  - 値の種類: REG_SZ
  ##### サンプル値:
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


  #### Mac の情報と設定
  - 優先されるキーの名前: ManagedSearchEngines
  - サンプル値:
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
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### MaxConnectionsPerProxy
  #### プロキシ サーバーへの同時実行の最大接続数
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  プロキシ サーバーへの最大同時接続数を指定します。

プロキシ サーバーによっては 1 つのクライアントに対して多数の同時接続を処理できない場合がありますが、このポリシーの値を小さく設定することによって、この問題を解決できます。

このポリシーの値は、7 以上 100 未満の間で設定する必要があります。既定値は 32 です。

一部の Web アプリでは、ハンギング GET で多数の接続が使用されることがわかっています。そのため、最大接続数を 32 未満の小さい値に設定すると、このような Web アプリを多く開きすぎた場合に、ブラウザー ネットワークが停止します。

このポリシーを構成しなかった場合、既定値 (32) が使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: MaxConnectionsPerProxy
  - GP の名前: プロキシ サーバーへの同時実行の最大接続数
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: MaxConnectionsPerProxy
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000020
```


  #### Mac の情報と設定
  - 優先されるキーの名前: MaxConnectionsPerProxy
  - サンプル値:
``` xml
<integer>32</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### MediaRouterCastAllowAllIPs
  #### すべての IP アドレスで Cast デバイスに接続することを Google Cast に許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  このポリシーを有効にした場合、Google Cast は、RFC1918/RFC4193 のプライベート アドレスだけでなく、すべての IP アドレスの Cast デバイスに接続できます。

このポリシーを無効にした場合、Google Cast は、RFC1918/RFC4193 のプライベート アドレスの Cast デバイスにのみ接続できます。

このポリシーを構成しなかった場合、CastAllowAllIPs 機能が有効になっていなければ、Google Cast は RFC1918/RFC4193 のプライベート アドレスの Cast デバイスにのみ接続できます。

[EnableMediaRouter](#enablemediarouter) ポリシーを無効にした場合、このポリシーは適用されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: MediaRouterCastAllowAllIPs
  - GP の名前: すべての IP アドレスで Cast デバイスに接続することを Google Cast に許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: MediaRouterCastAllowAllIPs
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: MediaRouterCastAllowAllIPs
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### MetricsReportingEnabled
  #### 使用状況とクラッシュに関するデータのレポート送信を有効にする (非推奨)
  >非推奨: このポリシーは推奨されていません。現在サポートされていますが、将来のリリースでは使用されなくなります。
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  このポリシーは廃止されました。現在サポートされていますが、Microsoft Edge 89 で廃止されます。このポリシーは、新しいポリシーに置き換えられます: Windows 7、Windows 8、および macOS の [DiagnosticData](#diagnosticdata)。このポリシーは、Win 10 の利用統計情報の許可 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)) に置き換えられました。

このポリシーによって、Microsoft Edge についての利用状況とクラッシュに関連するデータを Microsoft へ報告できるようになります。

利用状況とクラッシュに関連するデータのレポートを Microsoft に送信する場合は、このポリシーを有効にします。データを Microsoft に送信しない場合は、このポリシーを無効にします。どちらの場合も、ユーザーは設定を変更またはオーバーライドすることはできません。

Windows 10 では、このポリシーを構成しなかった場合、Microsoft Edge では、既定で Windows 診断データの設定が使用されます。このポリシーを有効にした場合に、Windows 診断データの設定が [拡張] または [フル] に設定されていると、Microsoft Edge では、利用状況データのみが送信されます。このポリシーを無効にした場合、Microsoft Edge では、利用状況データは送信されません。クラッシュに関するデータは、Windows 診断データの設定に基づいて送信されます。Windows 診断データの設定の詳細については、[https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569) を参照してください。

Windows 7、Windows 8、および macOS では、このポリシーは使用状況とクラッシュ関連データの送信を制御します。このポリシーを構成しない場合、Microsoft Edge は既定でユーザーの設定になります。

このポリシーを有効にするには、[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) を [有効] に設定する必要があります。[MetricsReportingEnabled](#metricsreportingenabled) または [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) が [未構成] か [無効] になっている場合、このデータは Microsoft に送信されません。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: MetricsReportingEnabled
  - GP の名前: 使用状況とクラッシュに関するデータのレポート送信を有効にする (非推奨)
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: MetricsReportingEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: MetricsReportingEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NativeWindowOcclusionEnabled
  #### ネイティブウィンドウオクルージョンを有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の 84

  #### 説明
  Microsoft Edge 内のネイティブ ウィンドウ オクルージョンを有効にします。

この設定を有効にすると、CPU と消費電力を削減するため、ウィンドウが他のウィンドウで覆われているときは、Microsoft Edge がそれを検出し、ピクセルを描画する作業を中断します。

この設定を無効にすると、ウィンドウが他のウィンドウで覆われていても、Microsoft Edge はそれを検出しなくなります。

このポリシーが設定されないままの場合は、ウィンドウの非表示検出が有効になります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: NativeWindowOcclusionEnabled
  - GP の名前: ネイティブウィンドウオクルージョンを有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: NativeWindowOcclusionEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NavigationDelayForInitialSiteListDownloadTimeout
  #### エンタープライズ モード サイト一覧のタブ ナビゲーションの遅延時間を設定する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 84

  #### 説明
  ブラウザーが初期エンタープライズ モード サイト一覧をダウンロードし終わるまで Microsoft Edge タブがナビゲーションを待つ場合のタイムアウトを秒単位で設定できます。

この設定は次と連動して機能します。
[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) が「IEMode」に設定されている
および
リストに少なくとも1つのエントリがある [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) ポリシー
および
[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload) が「対象となるすべてのナビゲーション」(1) に設定されている

タブは、エンタープライズ モード サイト一覧のタイムアウトを超えて待つことはありません。タイムアウト時間が切れたときにエンタープライズ モード サイト一覧のダウンロードが完了していない場合でも、Microsoft Edge タブはナビゲーションを続けます。タイムアウトの値は、20 秒より大きくしたり、1 秒未満にしたりしてはいけません。

このポリシーでタイムアウトを既定の 2 秒よりも大きい値に設定すると、ユーザーには 2 秒後に情報バーが表示されます。情報バーには、ユーザーがエンタープライズ モード サイト一覧のダウンロードを完了するまで待機するのを中止できるボタンがあります。

このポリシーを設定しない場合、既定のタイムアウトの 2 秒が使用されます。この既定値は、将来変更される可能性があります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: NavigationDelayForInitialSiteListDownloadTimeout
  - GP の名前: エンタープライズ モード サイト一覧のタブ ナビゲーションの遅延時間を設定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: NavigationDelayForInitialSiteListDownloadTimeout
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x0000000a
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NetworkPredictionOptions
  #### ネットワーク予測を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ネットワーク予測を有効にして、ユーザーがこの設定を変更できないようにします。

これにより、DNS プリフェッチ、TCP と SSL の接続数、および Web ページのプリレンダリングが制御されます。

このポリシーを構成しなかった場合は、ネットワーク予測が有効になりますが、ユーザーはこの設定を変更できます。

ポリシー オプションのマッピング:

* NetworkPredictionAlways (0) = 任意のネットワーク接続でのネットワーク操作を予測する

* NetworkPredictionWifiOnly (1) = サポートされていません。この値を使用すると、「ネットワーク接続のネットワーク アクションを予測する」(0) が設定されているものとして扱われます。

* NetworkPredictionNever (2) = 任意のネットワーク接続でのネットワーク操作を予測しない

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: NetworkPredictionOptions
  - GP の名前: ネットワーク予測を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: NetworkPredictionOptions
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: NetworkPredictionOptions
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### NonRemovableProfileEnabled
  #### 職場または学校アカウントで自動的にサインインする既定のプロファイルを、ユーザーが常に持つ必要があるかどうかを構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 78

  #### 説明
  このポリシーでは、ユーザーの職場または学校アカウントを使用して自動的にサインインされる Microsoft Edge のプロファイルを、ユーザーが削除できるかどうかを決定します。

このポリシーを有効にした場合、Windows におけるユーザーの職場または学校アカウントを使用して、削除不可能なプロファイルが作成されます。このプロファイルからサインアウトしたり、このプロファイルを削除したりすることはできません。

このポリシーを無効にした場合または構成しなかった場合、Windows におけるユーザーの職場または学校アカウントを使用して自動的にサインインされるプロファイルについては、ユーザーはサインアウトしたり、削除したりすることができます。

ブラウザー サインインを構成する場合は、[BrowserSignin](#browsersignin) ポリシーを使用してください。

このポリシーは、Microsoft Active Directory ドメインに参加している Windows インスタンス、デバイス管理に登録されている Windows 10 Pro インスタンスまたは Windows 10 Enterprise インスタンス、または MDM 経由で管理されているか MCX 経由でドメインに参加している macOS インスタンスでのみ利用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: NonRemovableProfileEnabled
  - GP の名前: 職場または学校アカウントで自動的にサインインする既定のプロファイルを、ユーザーが常に持つ必要があるかどうかを構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: NonRemovableProfileEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### OverrideSecurityRestrictionsOnInsecureOrigin
  #### 保護されていないオリジンに対するセキュリティ制限を適用する状況を制御する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  保護されていないオリジンに対してセキュリティ制限を適用しない場合に、そのオリジン (URL) やホスト名パターン ("*.contoso.com"など) のリストを指定します。

このポリシーを使用すると、TLS を展開できないまたは内部の Web 開発についてステージング サーバーをセットアップできないレガシ アプリケーションに対して、オリジンを許可するように指定できます。これにより開発者は、TLS をステージング サーバーに展開しなくても、セキュリティで保護されたコンテキストが必要となる機能をテストすることができます。このポリシーでは、omnibox で "セキュリティ保護なし" というラベルがオリジンに付くのを回避することもできます。

このポリシーで URL のリストを設定すると、同じ URL が指定されたコンマ区切りのリストに対してコマンド ライン フラグ '--unsafely-treat-insecure-origin-as-secure' を設定した場合と同じ効果があります。このポリシーを有効にした場合、コマンド ライン フラグはオーバーライドされます。

セキュリティで保護されたコンテキストの詳細については、https://www.w3.org/TR/secure-contexts/ を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: OverrideSecurityRestrictionsOnInsecureOrigin
  - GP の名前: 保護されていないオリジンに対するセキュリティ制限を適用する状況を制御する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\1 = "http://testserver.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\2 = "*.contoso.com"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: OverrideSecurityRestrictionsOnInsecureOrigin
  - サンプル値:
``` xml
<array>
  <string>http://testserver.contoso.com/</string>
  <string>*.contoso.com</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PaymentMethodQueryEnabled
  #### Web サイトでの利用可能な支払い方法の照会を許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 80

  #### 説明
  ユーザーが支払い方法を保存したことを Web サイトで確認できるようにするかどうかを設定できます。

このポリシーを無効にした場合、PaymentRequest.canMakePayment API または PaymentRequest.hasEnrolledInstrument API を使用する Web サイトでは、利用できる支払方法がないことが通知されます。

このポリシーを有効にした場合または設定しなかった場合、Web サイトでは、ユーザーが支払い方法を保存したかどうかを確認できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PaymentMethodQueryEnabled
  - GP の名前: Web サイトでの利用可能な支払い方法の照会を許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: PaymentMethodQueryEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: PaymentMethodQueryEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PersonalizationReportingEnabled
  #### 閲覧の履歴を Microsoft に送信して、広告、検索、ニュースの個人用設定を許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 80

  #### 説明
  このポリシーを有効にすると、広告、検索、ニュース、他の Microsoft サービスのパーソナル設定に使用される Microsoft Edge でのユーザーの閲覧履歴を、Microsoft で収集することができなくなります。

この設定は、Microsoft アカウントを持っているユーザーのみが使用できます。この設定は、お子様のアカウントやエンタープライズ アカウントでは使用できません。

このポリシーを無効にした場合、ユーザーは設定を変更またはオーバーライドすることはできません。このポリシーを有効にした場合または構成しなかった場合、Microsoft Edge では、既定でユーザー設定が使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PersonalizationReportingEnabled
  - GP の名前: 閲覧の履歴を Microsoft に送信して、広告、検索、ニュースの個人用設定を許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: PersonalizationReportingEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: PersonalizationReportingEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PinningWizardAllowed
  #### [タスク バー ウィザードにピン留めする] を許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 80

  #### 説明
  Microsoft Edge では、ユーザーが [タスク バー ウィザードにピン留めする] を使用して、お勧めのサイトをタスク バーにピン留めできるようにします。タスク バー ウィザードにピン留めする機能は既定で有効であり、[設定など] メニューからユーザーに対して表示されます。

このポリシーを有効にした場合、または構成しなかった場合、ユーザーは [設定など] メニューから [タスク バー ウィザードにピン留めする] を呼び出せます。プロトコルの起動経由でもウィザードを呼び出せます。

このポリシーを無効にした場合は、[タスク バー ウィザードにピン留めする] はメニューで無効にされ、プロトコルの起動経由で呼び出せません。

[タスク バー ウィザードにピン留めする] を有効または無効にするユーザー設定は使用できません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PinningWizardAllowed
  - GP の名前: [タスク バー ウィザードにピン留めする] を許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: PinningWizardAllowed
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ProactiveAuthEnabled
  #### 事前認証を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  事前認証を有効にするかどうかを構成できます。

このポリシーを有効にした場合、Microsoft Edge では、Microsoft サービスにサインインしているユーザーの事前認証を試行します。Microsoft Edge では、定期的にオンライン サービスを調べて、事前認証の方法を規定する構成が含まれているマニフェストが更新されているかどうかを確認します。

このポリシーを無効にした場合、Microsoft Edge では、Microsoft サービスにサインインしているユーザーの事前認証を試行しません。Microsoft Edge では、オンライン サービスを調べて、事前認証を行うための構成が含まれているマニフェストが更新されているかどうかを確認することはありません。

このポリシーを構成しなかった場合、事前認証が有効になります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ProactiveAuthEnabled
  - GP の名前: 事前認証を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ProactiveAuthEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ProactiveAuthEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PromotionalTabsEnabled
  #### タブ全体にプロモーション コンテンツを表示できるようにする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  フルタブのプロモーション用コンテンツや教育用コンテンツの表示を制御します。この設定は、Microsoft Edge へのサインインのサポート、既定のブラウザーの選択、製品の機能の説明を行うウェルカム ページの表示を制御します。

Iこのポリシーを有効にした場合 (true に設定) または構成しなかった場合、Microsoft Edge では、ユーザーに対してフルタブのコンテンツを表示し、製品情報が提示されます。

Iこの設定を無効にした場合 (false に設定)、Microsoft Edge では、ユーザーに対してフルタブのコンテンツを表示しません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PromotionalTabsEnabled
  - GP の名前: タブ全体にプロモーション コンテンツを表示できるようにする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: PromotionalTabsEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: PromotionalTabsEnabled
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### PromptForDownloadLocation
  #### ダウンロードしたファイルの保存場所を確認する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ダウンロードする前にファイルの保存場所を確認するかどうかを設定します。

この設定を有効にした場合、ユーザーはダウンロードする前にファイルの保存場所を確認されます。このポリシーを構成しなかった場合、ファイルは既定の場所に自動的に保存され、ユーザーへの確認はありません。

このポリシーを構成しなかった場合、ユーザーはこの設定を変更できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: PromptForDownloadLocation
  - GP の名前: ダウンロードしたファイルの保存場所を確認する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: PromptForDownloadLocation
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: PromptForDownloadLocation
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### QuicAllowed
  #### QUIC プロトコルを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge での QUIC プロトコルの使用を許可します。

このポリシーを有効にした場合または構成しなかった場合、QUIC プロトコルが許可されます。

このポリシーを無効にした場合、QUIC プロトコルはブロックされます。

QUIC とは、トランスポート層ネットワーク プロトコルで、現在 TCP を使用している Web アプリケーションのパフォーマンスを向上させることができます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: QuicAllowed
  - GP の名前: QUIC プロトコルを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: QuicAllowed
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: QuicAllowed
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### RelaunchNotification
  #### ブラウザーの再起動が推奨されるか、または必須であることをユーザーに通知する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  保留中の更新プログラムを適用するには Microsoft Edge を再起動する必要があることをユーザーに通知します。

このポリシーを構成しなかった場合、Microsoft Edge では、上部のメニュー バーの右端に  アイコンが追加され、ブラウザーを再起動して更新プログラムを適用するようにユーザーに通知します。

このポリシーを有効にして、「Recommended」に設定した場合、再起動が推奨されることをユーザーに通知する警告が定期的に表示されます。ユーザーはこの警告を無視して、再起動を延期できます。

ポリシーを「Required」に設定した場合は、通知期間が経過するとすぐにブラウザーが自動的に再起動されることをユーザーに通知する定期的な警告が表示されます。既定の期間は 7 日間です。この期間は [RelaunchNotificationPeriod](#relaunchnotificationperiod) ポリシーで構成できます。

ユーザーのセッションは、ブラウザーの再起動時に復元されます。

ポリシー オプションのマッピング:

* Recommended (1) = 推奨 - 再起動が推奨されることを示す定期的なプロンプトをユーザーに対して表示する

* Required (2) = 必須 - 再起動が必須であることを示す定期的なプロンプトをユーザーに対して表示する

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: RelaunchNotification
  - GP の名前: ブラウザーの再起動が推奨されるか、または必須であることをユーザーに通知する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: RelaunchNotification
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: RelaunchNotification
  - サンプル値:
``` xml
<integer>1</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### RelaunchNotificationPeriod
  #### 更新通知の期間を設定する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  保留中の更新プログラムを適用するために Microsoft Edge を再起動する必要があることをユーザーに通知する期間をミリ秒単位で設定できます。

この期間中、ユーザーには更新の必要性が繰り返し通知されます。Microsoft Edge では、通知期間の 3 分の 1 が経過すると、再起動が必要であることが示すために、アプリ メニューが変化します。この通知は、通知期間の 3 分の 2 がすると、また完全な通知期間が経過すると、色が変化します。[RelaunchNotification](#relaunchnotification) ポリシーによって有効にされる追加の通知は、これと同じスケジュールに従います。

設定しない場合、既定の期間である 6 億 480 万ミリ秒 (1 週間) が使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: RelaunchNotificationPeriod
  - GP の名前: 更新通知の期間を設定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: RelaunchNotificationPeriod
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x240c8400
```


  #### Mac の情報と設定
  - 優先されるキーの名前: RelaunchNotificationPeriod
  - サンプル値:
``` xml
<integer>604800000</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### RendererCodeIntegrityEnabled
  #### レンダラー コードの整合性を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の 78

  #### 説明
  このポリシーを有効にした場合または設定しなかった場合、レンダラー コードの整合性が有効になります。このポリシーを無効にするには、Microsoft Edge のレンダラー プロセス内で実行する必要があるサード パーティのソフトウェアとの間で互換性の問題が発生する場合のみにしてください。

このポリシーを無効にすると、Microsoft Edge のセキュリティや安定性が悪影響を受けます。これは、悪意を持つ可能性がある不明なコードが、Microsoft Edge のレンダラー プロセス内で読み込まれるためです。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: RendererCodeIntegrityEnabled
  - GP の名前: レンダラー コードの整合性を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: RendererCodeIntegrityEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### RequireOnlineRevocationChecksForLocalAnchors
  #### トラスト アンカーに対してオンライン OCSP/CRL チェックが必要であるかどうかを指定する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 77

  #### 説明
  オンライン失効確認 (OCSP/CRL チェック) が必要かどうかを制御します。Microsoft Edge が失効状態の情報を取得できない場合、該当の証明書は失効したものとして扱われます (ハード フェイル)。

このポリシーを有効にした場合、Microsoft Edge では、正常に確認されローカルにインストールされている CA 証明書によって署名されたサーバー証明書に対して、常に失効確認を実行します。

このポリシーを構成しなかった場合または無効にした場合、Microsoft Edge では、既存のオンライン失効確認の設定が使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: RequireOnlineRevocationChecksForLocalAnchors
  - GP の名前: トラスト アンカーに対してオンライン OCSP/CRL チェックが必要であるかどうかを指定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: RequireOnlineRevocationChecksForLocalAnchors
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ResolveNavigationErrorsUseWebService
  #### Web サービスを使用してナビゲーション エラーを解決できるようにする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge で、データレス接続を Web サービスに対して発行し、ホテルや空港の Wi-Fi などを利用する場合にネットワークの接続性を調べることができるようにします。

このポリシーを有効にした場合、ネットワーク接続のテストで Web サービスが使用されます。

このポリシーを無効にした場合、Microsoft Edge ではネイティブ API を使用して、ネットワーク接続とナビゲーションに関する問題の解決を試行します。

** 注意 **: Windows 8 およびそれ以降のバージョンの Windows を除き、Microsoft Edge では、*常に*ネイティブ API を使用して、接続の問題を解決します。

このポリシーを構成しなかった場合、Microsoft Edge では、edge://settings/privacy の [サービス] で設定されているユーザーの基本設定に従います。
具体的には **[ナビゲーションエラーを解決するために Web サービスを使用する]** というトグルが使用されます。ユーザーはこのトグルのオン/オフを切り替えることができます。ただし、このポリシー (ResolveNavigationErrorsUseWebService) を有効にした場合は、 **[ナビゲーションエラーを解決するために Web サービスを使用する]** の設定がオンになりますが、ユーザーはこのトグルを使用して設定を変更することができなくなります。このポリシーを無効にした場合は、**[ナビゲーションエラーを解決するために Web サービスを使用する]** の設定がオフになり、この場合もユーザーはこのトグルを使用して設定を変更することができなくなります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ResolveNavigationErrorsUseWebService
  - GP の名前: Web サービスを使用してナビゲーション エラーを解決できるようにする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: ResolveNavigationErrorsUseWebService
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ResolveNavigationErrorsUseWebService
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### RestrictSigninToPattern
  #### Microsoft Edge プライマリ アカウントとして使用できるアカウントを制限する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge でブラウザーのプライマリ アカウントとして設定できるアカウント (同期のオプトイン フローで選択されるアカウント) を決定します。

ユーザーがブラウザーのプライマリ アカウントを構成するときに、このパターンに一致しない場合、ブロックされ、適切なエラー メッセージが表示されます。パターンに Perl スタイルの正規表現を使用して、複数のアカウントに一致するようにこのポリシーを構成できます。パターン一致では大文字と小文字が区別されることに注意してください。使用される正規表現ルールの詳細については、https://go.microsoft.com/fwlink/p/?linkid=2133903 を参照してください。

このポリシーを設定しないか、空白のままにすると、ユーザーは任意のアカウントをブラウザーのプライマリ アカウントとして Microsoft Edge で設定できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: RestrictSigninToPattern
  - GP の名前: Microsoft Edge プライマリ アカウントとして使用できるアカウントを制限する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: RestrictSigninToPattern
  - 値の種類: REG_SZ
  ##### サンプル値:
```
".*@contoso.com"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: RestrictSigninToPattern
  - サンプル値:
``` xml
<string>.*@contoso.com</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### RoamingProfileLocation
  #### 移動プロファイルのディレクトリを設定する
  
  
  #### サポートされているバージョン:
  - Windows 以降の 85

  #### 説明
  プロファイルのローミング コピーを保存するために使用するディレクトリを構成します。

このポリシーを有効にすると、Microsoft Edge は、[RoamingProfileSupportEnabled](#roamingprofilesupportenabled) ポリシーも有効にしている限り、提供されたディレクトリを使用してプロファイルのローミング コピーを保存します。[RoamingProfileSupportEnabled](#roamingprofilesupportenabled) ポリシーを無効にするか、構成しない場合、このポリシーに格納されている値は使用されません。

使用できる変数のリストについては、[https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) を参照してください。

このポリシーを構成しなかった場合、既定の移動プロファイルのパスが使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: RoamingProfileLocation
  - GP の名前: 移動プロファイルのディレクトリを設定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: RoamingProfileLocation
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"${roaming_app_data}\\edge-profile"
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### RoamingProfileSupportEnabled
  #### Microsoft Edge プロファイル データに対してローミング コピーの使用を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の 85

  #### 説明
  このポリシーを有効にすると、Windows で移動プロファイルを使用できます。Microsoft Edge のプロファイルに保存されている設定 (お気に入りと設定) も、移動ユーザー プロファイル フォルダー (または、管理者が [RoamingProfileLocation](#roamingprofilelocation) ポリシーを使用して指定した場所) に格納されているファイルに保存されます。

このポリシーを無効にした場合または構成しなかった場合、通常のローカル プロファイルのみが使用されます。

[SyncDisabled](#syncdisabled) ポリシーを使用すると、このポリシーはオーバーライドされ、すべてのデータの同期が無効になります。

移動ユーザー プロファイルの使用に関する詳細については、https://docs.microsoft.com/windows-server/storage/folder-redirection/deploy-roaming-user-profiles を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: RoamingProfileSupportEnabled
  - GP の名前: Microsoft Edge プロファイル データに対してローミング コピーの使用を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: RoamingProfileSupportEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### RunAllFlashInAllowMode
  #### Adobe Flash コンテンツの設定をすべてのコンテンツに拡張する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  このポリシーを有効にした場合、コンテンツの設定で Adobe Flash が許可されている Web サイトでは (この許可はユーザーまたはエンタープライズ ポリシーによって指定されます)、埋め込まれているすべての Adobe Flash コンテンツが実行されます。こうしたコンテンツには、他のオリジンからのコンテンツや小さなコンテンツも含まれます。

Adobe Flash の実行を許可する Web サイトを制御するには、[DefaultPluginsSetting](#defaultpluginssetting)、[PluginsAllowedForUrls](#pluginsallowedforurls)、[PluginsBlockedForUrls](#pluginsblockedforurls) の各ポリシーの仕様を参照してください。

このポリシーを無効にした場合または構成しなかった場合、他のオリジン (上に示した 3 つのポリシーで指定されていないサイト) からの Adobe Flash コンテンツや小さなコンテンツはブロックされる可能性があります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: RunAllFlashInAllowMode
  - GP の名前: Adobe Flash コンテンツの設定をすべてのコンテンツに拡張する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: RunAllFlashInAllowMode
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: RunAllFlashInAllowMode
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SSLErrorOverrideAllowed
  #### ユーザーが HTTPS 警告ページから先に進むことを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザーが SSL エラーのあるサイトにアクセスしたときに、Microsoft Edge で警告ページが表示されます。

このポリシーを有効にした場合または構成しなかった場合 (既定)、ユーザーはこうした警告ページをクリック スルーすることができます。

このポリシーを無効にした場合、ユーザーはどのような警告ページもクリック スルーすることはできません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SSLErrorOverrideAllowed
  - GP の名前: ユーザーが HTTPS 警告ページから先に進むことを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: SSLErrorOverrideAllowed
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: SSLErrorOverrideAllowed
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SSLVersionMin
  #### 有効な TLS バージョンを最小限に抑える
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  サポートされる SSL の最小バージョンを設定します。このポリシーを構成しなかった場合、Microsoft Edge では既定の最小バージョン (TLS 1.0) が使用されます。

この設定を有効にした場合、最小バージョンを「TLSv1」、「TLSv1.1」または「TLSv1.2」のいずれかの値に設定できます。設定すると、Microsoft Edge では、指定されたバージョンより小さい SSL/TLS のバージョンは使用されません。認識されない値は無視されます。

ポリシー オプションのマッピング:

* TLSv1 (tls1) = TLS 1.0

* TLSv1.1 (tls1.1) = TLS 1.1

* TLSv1.2 (tls1.2) = TLS 1.2

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SSLVersionMin
  - GP の名前: 有効な TLS バージョンを最小限に抑える
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: SSLVersionMin
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"tls1"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: SSLVersionMin
  - サンプル値:
``` xml
<string>tls1</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SaveCookiesOnExit
  #### Microsoft Edge 閉じたときに Cookie を保存
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  このポリシーを有効にすると、ブラウザーを閉じたときに、指定した Cookie のセットが削除から除外されます。このポリシーは、次の場合にのみ有効です。
- [Cookie と他のサイトのデータ] トグルが [設定]/[プライバシーとサービス]/[閉じるときに閲覧データを消去]で構成されている
- ポリシー [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) が有効になっている
- ポリシー [DefaultCookiesSetting](#defaultcookiessetting) は [セッションの期間中 Cookie を保持する] に設定されている

セッション間で Cookie を保持するサイトのリストを、URLパターンに基づいて定義できます。

注: ユーザーは引き続き Cookie サイト リストを編集して、URL を追加または削除できます。ただし、管理者によって追加された URL を削除することはできません。

このポリシーを有効にした場合、ブラウザーを閉じても Cookie のリストはクリアされません。

このポリシーを無効にするか、構成しない場合は、ユーザーの個人設定が使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SaveCookiesOnExit
  - GP の名前: Microsoft Edge 閉じたときに Cookie を保存
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: SaveCookiesOnExit
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SavingBrowserHistoryDisabled
  #### ブラウザーの履歴の保存を無効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  閲覧の履歴の保存を無効にして、ユーザーがこの設定を変更できないようにします。

このポリシーを有効にした場合、閲覧の履歴は保存されません。これにより、タブの同期も無効になります。

このポリシーを無効にした場合、または構成しなかった場合は、閲覧の履歴が保存されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SavingBrowserHistoryDisabled
  - GP の名前: ブラウザーの履歴の保存を無効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: SavingBrowserHistoryDisabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: SavingBrowserHistoryDisabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ScreenCaptureAllowed
  #### スクリーンショットを許可または拒否します
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 83

  #### 説明
  このポリシーを有効にした場合、またはこのポリシーを構成しない場合は、Web ページで画面共有 API (getDisplayMedia() やデスクトップ キャプチャ拡張 API など) を使用して、画面をキャプチャできます。
このポリシーを無効にすると、画面共有 API の呼び出しは失敗します。たとえば、Web ベースのオンライン会議を使用している場合、ビデオまたは画面の共有は機能しません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ScreenCaptureAllowed
  - GP の名前: スクリーンショットを許可または拒否します
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ScreenCaptureAllowed
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ScreenCaptureAllowed
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ScrollToTextFragmentEnabled
  #### URL フラグメントで指定されたテキストへのスクロールを有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 83

  #### 説明
  この機能を使用すると、ハイパーリンクおよびアドレス バーの URL ナビゲーションで Web ページ上の特定のテキストを対象にすることができます。これは、Web ページの読み込みが完了した後にスクロールされます。

このポリシーを有効にした場合、または構成しない場合、URL を使用して特定のテキスト フラグメントにスクロールする Web ページが有効になります。

このポリシーを無効にした場合、URL を使用して特定のテキスト フラグメントにスクロールする Web ページが無効になります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ScrollToTextFragmentEnabled
  - GP の名前: URL フラグメントで指定されたテキストへのスクロールを有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ScrollToTextFragmentEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ScrollToTextFragmentEnabled
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SearchSuggestEnabled
  #### 検索候補を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge のアドレスバーおよび自動提案リストの Web 検索候補を有効にして、ユーザーがこのポリシーを変更できないようにします。

このポリシーを有効にした場合、Web 検索候補が使用されます。

このポリシーを無効にした場合、Web 検索候補は使用されませんが、ローカルの履歴とお気に入りの候補が表示されます。また、入力した文字やアクセスした URL は、マイクロソフトに送信される利用統計情報には含まれません。

このポリシーの構成を行わない場合、検索候補は有効になりますが、ユーザーはこれを変更できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SearchSuggestEnabled
  - GP の名前: 検索候補を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: SearchSuggestEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: SearchSuggestEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SecurityKeyPermitAttestation
  #### 直接セキュリティ キー構成証明を使用するためのアクセス許可を必要としない Web サイトまたはドメイン
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  セキュリティ キーからの構成証明書が要求されたときに明示的なユーザー アクセス許可を必要としない Web サイトやドメインを指定します。また、個人の構成証明を使用できることを示す信号がセキュリティ キーに送信されます。このポリシーを指定しなかった場合、サイトがセキュリティ キーの構成証明を要求するたびに、ユーザーに対して確認メッセージが表示されます。

サイト (https://contoso.com/some/path など) は U2F の appID としてのみ照合されます。ドメイン (contoso.com など) は webauthn の RP ID としてのみ照合されます。指定のサイトについて、U2F と webauthn の両方の API に対応するには、appID URL とドメインの両方をリストに指定する必要があります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SecurityKeyPermitAttestation
  - GP の名前: 直接セキュリティ キー構成証明を使用するためのアクセス許可を必要としない Web サイトまたはドメイン
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation\1 = "https://contoso.com"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: SecurityKeyPermitAttestation
  - サンプル値:
``` xml
<array>
  <string>https://contoso.com</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SendIntranetToInternetExplorer
  #### すべてのイントラネット サイトを Internet Explorer に送る
  
  
  #### サポートされているバージョン:
  - Windows 以降の 77

  #### 説明
  Internet Explorer モードに最適なエクスペリエンスを構成するガイダンスについては、[https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210) を参照してください

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SendIntranetToInternetExplorer
  - GP の名前: すべてのイントラネット サイトを Internet Explorer に送る
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: SendIntranetToInternetExplorer
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SendSiteInfoToImproveServices
  #### Microsoft サービスを改善するためにサイト情報を送信する (非推奨)
  >非推奨: このポリシーは推奨されていません。現在サポートされていますが、将来のリリースでは使用されなくなります。
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  このポリシーは廃止されました。現在サポートされていますが、Microsoft Edge 89 で廃止されます。このポリシーは、新しいポリシーに置き換えられます: Windows 7、Windows 8、および macOS の [DiagnosticData](#diagnosticdata)。このポリシーは、[Win 10 でテレメトリを許可する] ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)) に置き換えられました。

このポリシーを有効にすると、Microsoft Edge でアクセスした Web サイトに関する情報を Microsoft に送信して、検索などのサービスを向上させることができます。

このポリシーを有効にすると、Microsoft Edge でアクセスした Web サイトに関する情報を Microsoft に送信できます。Microsoft Edge でアクセスした Web サイトに関する情報を Microsoft に送信しないようにするには、このポリシーを無効にします。どちらの場合も、ユーザーは設定を変更またはオーバーライドすることはできません。

Windows 10 で、このポリシーを構成しなかった場合、Microsoft Edge では、既定で Windows 診断データの設定が使用されます。このポリシーを有効にすると、Microsoft Edge は、Windows 診断データの設定が [完全] に設定されている場合に、Microsoft Edge でアクセスした Web サイトに関する情報のみを送信します。このポリシーが無効になっている場合、Microsoft Edge はアクセスした Web サイトに関する情報を送信しません。Windows 診断データの設定の詳細については、[https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569) を参照してください。

Windows 7、Windows 8、および macOS では、このポリシーは使用状況とクラッシュ関連データの送信を制御します。このポリシーを構成しない場合、Microsoft Edge は既定でユーザーの設定になります。

このポリシーを有効にするには、[MetricsReportingEnabled](#metricsreportingenabled) を [有効] に設定する必要があります。[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) または [MetricsReportingEnabled](#metricsreportingenabled) が [未構成] か [無効] になっている場合、このデータは Microsoft に送信されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SendSiteInfoToImproveServices
  - GP の名前: Microsoft サービスを改善するためにサイト情報を送信する (非推奨)
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: SendSiteInfoToImproveServices
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: SendSiteInfoToImproveServices
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SensorsAllowedForUrls
  #### 特定のサイトのセンサーへのアクセスを許可
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  モーション センサーや光センサーなどのセンサーにアクセスして使用できるサイトのリストを、URL パターンに基づいて定義します。

  このポリシーを構成しなかった場合、すべてのサイトで、[DefaultSensorsSetting](#defaultsensorssetting) ポリシーのグローバル 既定値 (設定されている場合)、またはユーザーの個人用の構成が使用されます。

  このポリシーに一致しない URL パターンの場合は、[SensorsBlockedForUrls](#sensorsblockedforurls) ポリシー (一致する場合)、[DefaultSensorsSetting](#defaultsensorssetting) ポリシー (設定されている場合)、またはユーザーの個人設定の優先順位が使用されます。

このポリシーで定義された URL パターンは、[SensorsBlockedForUrls](#sensorsblockedforurls) ポリシーで構成されている URL パターンと競合しないようにする必要があります。URL の許可とブロックを構成することはできません。

有効な URL パターンの詳細については、[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SensorsAllowedForUrls
  - GP の名前: 特定のサイトのセンサーへのアクセスを許可
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: SensorsAllowedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SensorsBlockedForUrls
  #### 特定のサイトのセンサーへのアクセスをブロック
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  モーション センサーや光センサーなどのセンサーにアクセスできないサイトのリストを、URL パターンに基づいて定義します。

  このポリシーを構成しなかった場合、すべてのサイトで、[DefaultSensorsSetting](#defaultsensorssetting) ポリシーのグローバル 既定値 (設定されている場合)、またはユーザーの個人用の構成が使用されます。

  このポリシーに一致しない URL パターンの場合は、[SensorsAllowedForUrls](#sensorsallowedforurls) ポリシー (一致する場合)、[DefaultSensorsSetting](#defaultsensorssetting) ポリシー (設定されている場合)、またはユーザーの個人設定の優先順位が使用されます。

このポリシーで定義された URL パターンは、[SensorsAllowedForUrls](#sensorsallowedforurls) ポリシーで構成されている URL パターンと競合しないようにする必要があります。URL の許可とブロックを構成することはできません。

有効な URL パターンの詳細については、[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SensorsBlockedForUrls
  - GP の名前: 特定のサイトのセンサーへのアクセスをブロック
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: SensorsBlockedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SerialAskForUrls
  #### 特定のサイトでシリアル API を許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  シリアルポートへのアクセスをユーザーに確認できるサイトのリストを、URL パターンに基づいて定義します。

  このポリシーを構成しなかった場合、すべてのサイトで、[DefaultSerialGuardSetting](#defaultserialguardsetting) ポリシーのグローバル 既定値 (設定されている場合)、またはユーザーの個人用の構成が使用されます。

  このポリシーに一致しない URL パターンの場合は、[SerialBlockedForUrls](#serialblockedforurls) ポリシー (一致する場合)、[DefaultSerialGuardSetting](#defaultserialguardsetting) ポリシー (設定されている場合)、またはユーザーの個人設定の優先順位が使用されます。

このポリシーで定義された URL パターンは、[SerialBlockedForUrls](#serialblockedforurls) ポリシーで構成されている URL パターンと競合しないようにする必要があります。URL の許可とブロックを構成することはできません。

有効な URL パターンの詳細については、[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SerialAskForUrls
  - GP の名前: 特定のサイトでシリアル API を許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: SerialAskForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SerialBlockedForUrls
  #### 特定のサイトでシリアル API をブロックする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  シリアル ポートへのアクセス権の付与をユーザーに確認することができないサイトのリストを、URL パターンに基づいて定義します。

  このポリシーを構成しなかった場合、すべてのサイトで、[DefaultSerialGuardSetting](#defaultserialguardsetting) ポリシーのグローバル 既定値 (設定されている場合)、またはユーザーの個人用の構成が使用されます。

  このポリシーに一致しない URL パターンの場合は、[SerialAskForUrls](#serialaskforurls) ポリシー (一致する場合)、[DefaultSerialGuardSetting](#defaultserialguardsetting) ポリシー (設定されている場合)、またはユーザーの個人設定の優先順位が使用されます。

このポリシーの URL パターンは、[SerialAskForUrls](#serialaskforurls) ポリシーで構成されている URL パターンと競合しないようにする必要があります。URL の許可とブロックを構成することはできません。

有効な URL パターンの詳細については、[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SerialBlockedForUrls
  - GP の名前: 特定のサイトでシリアル API をブロックする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\2 = "[*.]contoso.edu"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: SerialBlockedForUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### ShowOfficeShortcutInFavoritesBar
  #### Microsoft Office のショートカットをお気に入りバーに表示する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Office.com へのショートカットをお気に入りバーに含めるかどうかを指定します。ユーザーが Microsoft Edge にサインインしている場合、ユーザーはショートカットによって Microsoft Office のアプリやドキュメントにアクセスすることができます。

このポリシーを有効にした場合または構成しなかった場合、ユーザーは、お気に入りバーのコンテキスト メニューで表示/非表示を切り替えることによって、ショートカットを表示するかどうかを選択できます。

この設定を無効にした場合、ショートカットは表示されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: ShowOfficeShortcutInFavoritesBar
  - GP の名前: Microsoft Office のショートカットをお気に入りバーに表示する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: ShowOfficeShortcutInFavoritesBar
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: ShowOfficeShortcutInFavoritesBar
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SignedHTTPExchangeEnabled
  #### Signed HTTP Exchange (SXG) のサポートを有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 78

  #### 説明
  Signed HTTP Exchange (SXG) のサポートを有効にします。

このポリシーが設定されていないか、有効にされている場合、Microsoft Edge では、Signed HTTP Exchanges として提供される Web コンテンツを承認します。

このポリシーが無効に設定されている場合、Signed HTTP Exchanges を読み込むことができません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SignedHTTPExchangeEnabled
  - GP の名前: Signed HTTP Exchange (SXG) のサポートを有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: SignedHTTPExchangeEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: SignedHTTPExchangeEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SitePerProcess
  #### すべてのサイトでサイト分離を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  「SitePerProcess」ポリシーを使用すると、すべてのサイトを分離する既定の動作をユーザーがオプトアウトするのを防ぐことができます。[IsolateOrigins](#isolateorigins) ポリシーを使用して、より細かいオリジンをさらに分離することもできます。
このポリシーを有効にした場合、ユーザーは既定の動作をオプトアウトできず、各サイトは独自のプロセスで実行されます。
このポリシーを無効にした場合またはこのポリシーを構成しなかった場合、ユーザーはサイトの分離をオプトアウトできます (たとえは、edge://flags で「サイトの分離を無効にする」エントリを使用)。このポリシーを無効にした場合または構成しなかった場合でも、サイトの分離は無効になりません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SitePerProcess
  - GP の名前: すべてのサイトでサイト分離を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: SitePerProcess
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: SitePerProcess
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SpellcheckEnabled
  #### スペルチェックを有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  このポリシーを有効にした場合または構成しなかった場合、ユーザーはスペルチェックを使用できます。

このポリシーを無効にした場合、ユーザーはスペルチェックを使用できなくなり、[SpellcheckLanguage](#spellchecklanguage) ポリシーと [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) ポリシーも無効になります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SpellcheckEnabled
  - GP の名前: スペルチェックを有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: SpellcheckEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: SpellcheckEnabled
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SpellcheckLanguage
  #### 特定のスペルチェック言語を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の 77

  #### 説明
  スペルチェックでさまざまな言語が利用できるようにします。指定した言語が認識されない場合は無視されます。

このポリシーを有効にした場合、ポリシーで指定した言語およびユーザーが有効にしたすべての言語でスペルチェックを利用できるようになります。

このポリシーを構成しなかった場合または無効にした場合、ユーザーのスペルチェックの設定は変更されません。

[SpellcheckEnabled](#spellcheckenabled) ポリシーを無効にした場合、このポリシーは適用されません。

言語が 'SpellcheckLanguage' ポリシーと [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) ポリシーの両方に含まれている場合、そのスペルチェック言語は有効なものとして扱われます。

次の言語がサポートされています: af、bg、ca、cs、cy、da、de、el、en-AU、en-CA、en-GB、en-US、es、es-419、es-AR、es-ES、es-MX、es-US、et、fa、fo、fr、he、hi、hr、hu、id、it、ko、lt、lv、nb、nl、pl、pt-BR、pt-PT、ro、ru、sh、sk、sl、sq、sr、sv、ta、tg、tr、uk、vi。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SpellcheckLanguage
  - GP の名前: 特定のスペルチェック言語を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\2 = "es"

```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SpellcheckLanguageBlocklist
  #### スペルチェック言語を強制的に無効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の 78

  #### 説明
  スペルチェック言語を強制的に無効にします。このリストにある認識されない言語は、無視されます。

このポリシーを有効にした場合、指定した言語のスペルチェックが無効になります。ただしユーザーは、リストにない言語に対してスペルチェックを有効または無効にすることができます。

このポリシーを設定しなかった場合または無効にした場合、ユーザーのスペルチェックの設定は変更されません。

[SpellcheckEnabled](#spellcheckenabled) ポリシーを無効に設定した場合、このポリシーは適用されません。

[SpellcheckLanguage](#spellchecklanguage) ポリシーと 'SpellcheckLanguageBlocklist' ポリシーの両方に言語が含まれている場合、そのスペルチェック言語は有効なものとして扱われます。

現在、次の言語がサポートされています: af、bg、ca、cs、da、de、el、en-AU、en-CA、en-GB、en-US、es、es-419、es-AR、es-ES、es-MX、es-US、et、fa、fo、fr、he、hi、hr、hu、id、it、ko、lt、lv、nb、nl、pl、pt-BR、pt-PT、ro、ru、sh、sk、sl、sq、sr、sv、ta、tg、tr、uk、vi。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SpellcheckLanguageBlocklist
  - GP の名前: スペルチェック言語を強制的に無効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\2 = "es"

```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### StricterMixedContentTreatmentEnabled
  #### 混合コンテンツの厳密な処理を有効にする (非推奨)
  >非推奨: このポリシーは推奨されていません。現在サポートされていますが、将来のリリースでは使用されなくなります。
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 81

  #### 説明
  このポリシーは、混在したコンテンツの厳格な処理と互換性がないことが判明した場合に、企業が Web コンテンツを更新する時間を増やすための短期的なメカニズムとしてのみ使用されるため、廃止されました。バージョン 85 になると Microsoft Edge では動作しません。

このポリシーは、ブラウザーでの混在したコンテンツ (HTTPS サイトの HTTP コンテンツ) の処理を制御します。

ポリシーを true または未設定にすると、オーディオとビデオの混在したコンテンツは自動的に HTTPS にアップグレードされ (つまり、リソースが HTTPS 経由で利用できない場合、フォールバックなしで URL は HTTPS に書き換えられます)、画像が混在したコンテンツの場合、URL バーに「安全ではありません」という警告が表示されます。

ポリシーを false に設定すると、オーディオとビデオの自動アップグレードが無効になり、画像の警告は表示されません。

このポリシーは、オーディオ、ビデオ、および画像以外の混在したコンテンツには影響しません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: StricterMixedContentTreatmentEnabled
  - GP の名前: 混合コンテンツの厳密な処理を有効にする (非推奨)
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: StricterMixedContentTreatmentEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: StricterMixedContentTreatmentEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SuppressUnsupportedOSWarning
  #### サポートされていない OS の警告を表示しない
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  現在サポートされていないコンピューターやオペレーティング システムで Microsoft Edge が実行されている場合に表示される警告が表示されなくなります。

このポリシーが False であるか、設定しなかった場合、サポートされないコンピューターまたはオペレーティング システムなどに警告が表示されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SuppressUnsupportedOSWarning
  - GP の名前: サポートされていない OS の警告を表示しない
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: SuppressUnsupportedOSWarning
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: SuppressUnsupportedOSWarning
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SyncDisabled
  #### Microsoft 同期サービスを使用しているデータの同期を無効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge でのデータ同期を無効にします。このポリシーでは、同期の同意プロンプトを表示しないようにすることもできます。

このポリシーを設定しなかった場合、または推奨されるポリシーとして適用した場合、ユーザーは同期を有効にしたり無効にしたりすることができます。このポリシーを必須のポリシーとして適用した場合、ユーザーは同期を有効にすることはできません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SyncDisabled
  - GP の名前: Microsoft 同期サービスを使用しているデータの同期を無効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: SyncDisabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: SyncDisabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### SyncTypesListDisabled
  #### 同期から除外される種類のリストを構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 83

  #### 説明
  このポリシーを有効にすると、指定したすべてのデータ型が同期から除外されます。このポリシーを使用して、Microsoft Edge 同期サービスにアップロードされるデータ型を制限できます。

このポリシーには、「お気に入り」、「設定」、「パスワード」、「アドレスなど」、「拡張機能」、「履歴」、「タブを開く」、「コレクション」のいずれかのデータ型を指定できます。これらのデータ型名は大文字と小文字が区別されることに注意してください。

ユーザーは無効なデータ型を上書きできません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: SyncTypesListDisabled
  - GP の名前: 同期から除外される種類のリストを構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled\1 = "favorites"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: SyncTypesListDisabled
  - サンプル値:
``` xml
<array>
  <string>favorites</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### TLS13HardeningForLocalAnchorsEnabled
  #### ローカル トラスト アンカーで TLS 1.3 セキュリティ機能を有効にします。 (現在不使用)
  
  >古い形式: このポリシーは古い形式であり、Microsoft Edge 85 以降では使用することができません。
  #### サポートされているバージョン:
  - Windows 以降、macOS と 81 を 85

  #### 説明
  このポリシーは、企業が影響を受けたプロキシのアップグレードの時間を増やすための短期のメカニズムになっているため利用できません。

このポリシーは、ダウングレードの攻撃から接続を保護する TLS 1.3 のセキュリティ機能を制御します。下位互換性があり、準拠している TLS 1.2 サーバーやプロキシへの接続に影響することはありません。一部の TLS インターセプト プロキシの以前のバージョンでは、実装に不備があるため互換性がありません。

このポリシー設定を有効にした場合、または設定しなかった場合は、Microsoft Edge は、すべての接続のセキュリティ保護を有効にします。

このポリシーを無効にした場合は、Microsoft Edge は、ローカルにインストールされたCA 証明書で認証された接続のセキュリティ保護を無効にします。一般的に信頼されている CA 証明書で承認された接続に対しては、これらの保護は常に有効です。

このポリシーは、影響を受けたプロキシをテストするため、およびアップグレードするために使用できます。影響を受けたプロキシは、エラーコード ERR_TLS13_DOWNGRADE_DETECTED で接続に失敗するおそれがあります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: TLS13HardeningForLocalAnchorsEnabled
  - GP の名前: ローカル トラスト アンカーで TLS 1.3 セキュリティ機能を有効にします。 (現在不使用)
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: TLS13HardeningForLocalAnchorsEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: TLS13HardeningForLocalAnchorsEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### TLSCipherSuiteDenyList
  #### 無効にする TLS 暗号スイートを指定
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 85

  #### 説明
  TLS 接続に対して無効になっている暗号スイートの一覧を構成します。

このポリシーを構成した場合、TLS 接続を確立するときに、構成された暗号の一覧は使用されません。

このポリシーを構成しなかった場合、ブラウザーはどの TLS 暗号スイートを使用するかを選択します。

無効にする暗号スイート値は、16 ビットの 16 進数値として指定されます。値は、Internet Assigned Numbers Authority (IANA) レジストリによって割り当てられます。

TLS 1.3 暗号スイート TLS_AES_128_GCM_SHA256 (0x1301) は TLS 1.3 に必要であり、このポリシーで無効にすることはできません。

このポリシーは、QUIC ベースの接続には影響しません。QUIC は、[QuicAllowed](#quicallowed) ポリシーを使用して無効にすることができます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: TLSCipherSuiteDenyList
  - GP の名前: 無効にする TLS 暗号スイートを指定
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\1 = "0x1303"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\2 = "0xcca8"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\3 = "0xcca9"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: TLSCipherSuiteDenyList
  - サンプル値:
``` xml
<array>
  <string>0x1303</string>
  <string>0xcca8</string>
  <string>0xcca9</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### TabFreezingEnabled
  #### バックグラウンド タブの固定を許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 79

  #### 説明
  Microsoft Edge で、5 分以上バックグラウンドで開かれるタブを固定できるかどうかを制御します。

タブを固定すると、CPU、バッテリ、およびメモリの使用量を減らすことができます。Microsoft Edge では、ヒューリスティックを使用して、重要な処理 (通知の表示、サウンドの再生、動画のストリーム配信など) をバックグラウンドで実行するタブが固定されるのを回避します。

このポリシーを有効にした場合または構成しなかった場合、5 分以上バックグラウンドで表示されていたタブが固定される可能性があります。

このポリシーを無効にした場合、タブは固定されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: TabFreezingEnabled
  - GP の名前: バックグラウンド タブの固定を許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: TabFreezingEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: TabFreezingEnabled
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### TaskManagerEndProcessEnabled
  #### ブラウザーのタスク マネージャーでプロセスの終了を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  このポリシーを有効にした場合、または構成しなかった場合、ユーザーは、ブラウザーのタスク マネージャーでプロセスを終了できます。この設定を無効にした場合、ユーザーはプロセスを終了できなくなり、ブラウザーのタスク マネージャーの [プロセスの終了] ボタンが無効になります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: TaskManagerEndProcessEnabled
  - GP の名前: ブラウザーのタスク マネージャーでプロセスの終了を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: TaskManagerEndProcessEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: TaskManagerEndProcessEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### TotalMemoryLimitMb
  #### 1 つの Microsoft Edge インスタンスで使用できるメモリの上限を MB 単位で設定します。
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 80

  #### 説明
  メモリの節約を目的としてタブを破棄するまでに 1 つの Microsoft Edge インスタンスで使用できるメモリ容量の上限を構成します。タブで使用されているメモリは解放されます。切り替え時にはタブを再読み込みする必要があります。

このポリシーを有効にした場合、メモリ容量の上限を超えると、ブラウザーではタブが破棄されメモリが節約されます。ただし、ブラウザーが常にメモリ容量の上限を超えずに実行されているとは限りません。1024 未満の値は、1024 に切り上げられます。

このポリシーを設定しなかった場合、コンピューターの物理メモリの容量が不足していることが検出されたときにのみ、ブラウザーはメモリの節約を試行します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: TotalMemoryLimitMb
  - GP の名前: 1 つの Microsoft Edge インスタンスで使用できるメモリの上限を MB 単位で設定します。
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: TotalMemoryLimitMb
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000800
```


  #### Mac の情報と設定
  - 優先されるキーの名前: TotalMemoryLimitMb
  - サンプル値:
``` xml
<integer>2048</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### TrackingPrevention
  #### ユーザーの Web 閲覧アクティビティの追跡をブロックする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 78

  #### 説明
  Web サイトがユーザーの Web 閲覧アクティビティを追跡するのをブロックするかどうかを決定できます。

このポリシーを無効にするか、または構成しない場合、ユーザーは独自のレベルの追跡防止を設定できます。

ポリシー オプションのマッピング:

* TrackingPreventionOff (0) = オフ (追跡防止なし)

* TrackingPreventionBasic (1) = 基本 (有害なトラッカーをブロックし、コンテンツと広告はパーソナル設定されます)

* TrackingPreventionBalanced (2) = バランス (有害なトラッカーとユーザーがアクセスしていないサイトのトラッカーをブロックします。コンテンツと広告はほとんどパーソナル設定されません)

* TrackingPreventionStrict (3) = 厳密 (有害なトラッカーとすべてのサイトの大部分のトラッカーをブロックします。コンテンツと広告のパーソナル設定を最小限に抑えます。サイトの一部が機能しない場合があります)

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: TrackingPrevention
  - GP の名前: ユーザーの Web 閲覧アクティビティの追跡をブロックする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: TrackingPrevention
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000002
```


  #### Mac の情報と設定
  - 優先されるキーの名前: TrackingPrevention
  - サンプル値:
``` xml
<integer>2</integer>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### TranslateEnabled
  #### 翻訳を有効にする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge で統合された Microsoft 翻訳サービスを有効にします。

このポリシーを有効にすると、Microsoft Edge では、(該当する場合) 統合された翻訳ポップアップと右クリックコンテキスト メニューの翻訳オプションを表示して、ユーザーに翻訳機能を提供します。

組み込みの翻訳機能をすべて無効にするには、このポリシーを無効にしてください。

ポリシーを構成しない場合、ユーザーは翻訳機能を使用するかどうかを選択できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: はい
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: TranslateEnabled
  - GP の名前: 翻訳を有効にする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): 管理用テンプレート/Microsoft Edge - 既定の設定 (ユーザーはオーバーライドできます)/
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): SOFTWARE\Policies\Microsoft\Edge\おすすめ
  - 値の名前: TranslateEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: TranslateEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### URLAllowlist
  #### 許可されている URL のリストを定義する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  URL 禁止リストの例外として、リストに登録された URL へのアクセスを許可します。

URL パターンの形式は、[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) に従って指定してください。

このポリシーを使用すると、アクセスを制限する禁止リストに対して例外を適用できます。たとえば、禁止リストに '*' を含めて、すべての要求をブロックしてから、このポリシーを使用し、リストに登録されている限定された URL へのアクセスを許可することができます。このポリシーを使用して、特定のスキーム、他のドメインのサブドメイン、ポート、特定のパスに対して例外を適用することができます。

具体的に指定されたフィルターによって、URL がブロックされるか許可されるかが決定されます。許可リストは、禁止リストよりも優先されます。

このポリシーに登録できるエントリは 1000 件までです。それ以降のエントリは無視されます。

このポリシーにより、ブラウザーは、「tel:」や「ssh:」などのプロトコルのプロトコル ハンドラーとして登録された外部アプリケーションを自動的に呼び出すことができます。

このポリシーを構成しなかった場合、[URLBlocklist](#urlblocklist) ポリシーの禁止リストに対して例外は設定されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: URLAllowlist
  - GP の名前: 許可されている URL のリストを定義する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\URLAllowlist
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\5 = ".exact.hostname.com"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: URLAllowlist
  - サンプル値:
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### URLBlocklist
  #### URL のリストへのアクセスをブロックする
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ブロックされるサイトのリストを、URL パターンに基づいて定義します (ユーザーはこれらのサイトを読み込むことはできません)。

URL パターンの形式は、[https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) に従って指定します。

例外は [URLAllowlist](#urlallowlist) ポリシーで定義できます。これらのポリシーに登録できるエントリは 1000 件までです。それ以降のエントリは無視されます。

内部 URL である 'edge://*' をブロックすることはお勧めしません。こうした URL をブロックすると、予期しないエラーが発生する可能性があります。

このポリシーは、JavaScript を使用した動的なページの更新を妨げるものではありません。たとえば、'contoso.com/abc' をブロックした場合、ユーザーは 'contoso.com' にアクセスし、'contoso.com/abc' のページが更新されていなければ、このページへアクセスするためのリンクをクリックすることはできます。

このポリシーを構成しなかった場合、どの URL もブロックされません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: URLBlocklist
  - GP の名前: URL のリストへのアクセスをブロックする
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\URLBlocklist
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
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


  #### Mac の情報と設定
  - 優先されるキーの名前: URLBlocklist
  - サンプル値:
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
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### UserAgentClientHintsEnabled
  #### User-Agent Client Hints 機能を有効にする (非推奨)
  >非推奨: このポリシーは推奨されていません。現在サポートされていますが、将来のリリースでは使用されなくなります。
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 86

  #### 説明
  このポリシーは、Web コンテンツが User-Agent Client Hints 機能と互換性がない場合に、企業が Web コンテンツのアップグレードの時間を増やすための短期のメカニズムになっているため推奨されていません。Microsoft Edge バージョン 89 では機能しません。

User-Agent Client Hints 機能を有効にした場合は、ユーザー ブラウザー (ブラウザーのバージョンなど) およびユーザー環境 (システムのアーキテクチャなど)　についての情報を提供する要求ヘッダーの詳細を送信します。

これは追加の機能ですが、 新しいヘッダーは、要求が含まれる文字を制限する一部の Web サイトを中断する可能性があります。

このポリシー設定を有効にした場合、または構成しなかった場合は、User-Agent Client Hints 機能は有効になります。このポリシーを無効にした場合は、この機能は利用できません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: UserAgentClientHintsEnabled
  - GP の名前: User-Agent Client Hints 機能を有効にする (非推奨)
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: UserAgentClientHintsEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: UserAgentClientHintsEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### UserDataDir
  #### ユーザー データ ディレクトリを設定する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザー データの保存に使用するディレクトリを設定します。

このポリシーを有効にした場合、Microsoft Edge では、ユーザーが '--user-data-dir' コマンド ライン フラグを設定したかどうかに関係なく、ポリシーで指定されたディレクトリを使用します。

このポリシーを有効にしなかった場合、既定のプロファイル パスが使用されますが、ユーザーは '--user-data-dir' フラグを使用して、既定のプロファイル パスをオーバーライドできます。プロファイルのディレクトリは、edge://version/ のプロファイル パスで見つけることができます。

データの損失や他のエラーを回避するために、このポリシーの構成では、ボリュームのルート ディレクトリまたは他の用途に使用されるディレクトリを指定しないでください。Microsoft Edge で、こうしたディレクトリのコンテンツを管理しているためです。

使用できる変数のリストについては、[https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041) を参照してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: UserDataDir
  - GP の名前: ユーザー データ ディレクトリを設定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: UserDataDir
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"${users}/${user_name}/Edge"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: UserDataDir
  - サンプル値:
``` xml
<string>${users}/${user_name}/Edge</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### UserDataSnapshotRetentionLimit
  #### 緊急ロールバックの場合に使用するために保持されるユーザー データ スナップショットの数を制限
  
  
  #### サポートされているバージョン:
  - Windows 以降の 86

  #### 説明
  Microsoft Edge は、メジャー バージョンが更新されるたびに、ユーザーの閲覧データの一部のスナップショットを作成し、後で一時的なバージョンのロールバックが必要になった場合に使用します。ユーザーが対応するスナップショットを持っているバージョンに対して一時的なロールバックを実行すると、スナップショット内のデータが復元されます。これにより、ユーザーはブックマークや自動入力データなどの設定を保持できます。

このポリシーを設定しない場合、既定値の 3 つのスナップショットが使用されます。

このポリシーを設定すると、設定した制限を守るために、必要に応じて古いスナップショットが削除されます。このポリシーを 0 に設定すると、スナップショットは作成されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 整数

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: UserDataSnapshotRetentionLimit
  - GP の名前: 緊急ロールバックの場合に使用するために保持されるユーザー データ スナップショットの数を制限
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: UserDataSnapshotRetentionLimit
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000003
```


  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### UserFeedbackAllowed
  #### ユーザー フィードバックを許可する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge では、Edge フィードバック機能 (既定で有効) を使用することで、ユーザーがフィードバック、提案、または顧客アンケートを送信したり、ブラウザーに関する問題を報告したりすることができます。また既定では、ユーザーは Edge フィードバック機能を無効にする (オフにする) ことができません。

このポリシーを有効にした場合または構成しなかった場合、ユーザーは Edge フィードバックを呼び出すことができます。

このポリシーを無効にした場合、ユーザーは Edge フィードバックを呼び出すことはできません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: UserFeedbackAllowed
  - GP の名前: ユーザー フィードバックを許可する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: UserFeedbackAllowed
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: UserFeedbackAllowed
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### VideoCaptureAllowed
  #### ビデオ キャプチャを許可または禁止する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  サイトがビデオをキャプチャできるかどうかを制御します。

このポリシーを有効にした場合または構成しなかった場合 (既定)、ユーザーは、すべてのサイトでビデオ キャプチャのアクセスを確認するよう要求されます。ただし、[VideoCaptureAllowedUrls](#videocaptureallowedurls) ポリシーのリストで構成されている URL を持つサイトは除外されます。こうしたサイトでは、ユーザーへの確認を要求せずにアクセスが許可されます。

このポリシーを無効にした場合、ユーザーに対する確認の要求は行われず、ビデオ キャプチャは、[VideoCaptureAllowedUrls](#videocaptureallowedurls) ポリシーで構成されている URL でのみ利用できます。

このポリシーは、内蔵カメラだけでなく、すべての種類のビデオ入力に影響します。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: VideoCaptureAllowed
  - GP の名前: ビデオ キャプチャを許可または禁止する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: VideoCaptureAllowed
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000000
```


  #### Mac の情報と設定
  - 優先されるキーの名前: VideoCaptureAllowed
  - サンプル値:
``` xml
<false/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### VideoCaptureAllowedUrls
  #### アクセス許可を要求しなくてもビデオ キャプチャ デバイスにアクセスできるサイト
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  ユーザーに対してアクセス許可を要求しなくてもビデオ キャプチャ デバイスを使用できる Web サイトを、URL パターンに基づいて定義します。このリスト内のパターンは、要求元 URL のセキュリティ オリジンと照合されます。パターンが一致すると、サイトに対して、ビデオ キャプチャ デバイスへのアクセスが自動的に許可されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: VideoCaptureAllowedUrls
  - GP の名前: アクセス許可を要求しなくてもビデオ キャプチャ デバイスにアクセスできるサイト
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: VideoCaptureAllowedUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### WPADQuickCheckEnabled
  #### WPAD 最適化を設定する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  Microsoft Edge で WPAD (Web プロキシ自動検出) の最適化を無効にすることを許可します。

このポリシーを無効にした場合、WPAD の最適化が無効になり、DNS ベースの WPAD サーバーに対するブラウザーの待機間隔が長くなります。

このポリシーを有効にした場合または構成しなかった場合は、WPAD の最適化が有効になります。

このポリシーが有効かどうか、またはポリシーの設定方法に関係なく、ユーザーは WPAD の最適化設定を変更することはできません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: WPADQuickCheckEnabled
  - GP の名前: WPAD 最適化を設定する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: WPADQuickCheckEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: WPADQuickCheckEnabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### WebAppInstallForceList
  #### 強制的にインストールされる Web アプリのリストを構成する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 80

  #### 説明
  ユーザーによる操作なしでサイレント インストールされる Web サイトのリストを指定します。ユーザーは、これらの Web サイトをアンインストールしたり、無効にしたりすることはできません。

ポリシーの各リスト アイテムは、次のメンバーを含むオブジェクトとなります。
  - "url"。必須のメンバーです。"url" はインストールする Web アプリの URL です。

省略可能なメンバーの値は次のとおりです。
  - "launch_container" は "window" または "tab" のいずれかで、Web アプリをインストールした場合にアプリを開く方法を示します。
  - "create_desktop_shortcut" は、Windows 上でデスクトップ ショートカットを作成する場合、true にします。

"default_launch_container" を省略すると、アプリは既定によりタブで開かれます。"default_launch_container" の値に関係なく、ユーザーはアプリが開かれるコンテナーを変更できます。"create_desktop_shortcuts" を省略すると、デスクトップ ショートカットは作成されません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: はい

  #### データ型:
  - 辞書

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: WebAppInstallForceList
  - GP の名前: 強制的にインストールされる Web アプリのリストを構成する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: WebAppInstallForceList
  - 値の種類: REG_SZ
  ##### サンプル値:
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


  #### Mac の情報と設定
  - 優先されるキーの名前: WebAppInstallForceList
  - サンプル値:
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
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### WebComponentsV0Enabled
  #### M84 まで、Web Components v0 API を再度有効にする (現在不使用)
  
  >古い形式: このポリシーは古い形式であり、Microsoft Edge 84 以降では使用することができません。
  #### サポートされているバージョン:
  - Windows 以降、macOS と 80 を 84

  #### 説明
  このポリシーは、Microsoft Edge バージョン 85 までこれらの機能を選択的に再度有効にすることができるため、動作しません。Web コンポーネント v0 API (Shadow DOM v0、カスタム要素 v0、HTML インポート) は2018 年に廃止され、Microsoft Edge バージョン 80 以降、既定で無効になっています。

このポリシーを True に設定した場合、すべてのサイトで Web コンポーネント v0 機能が有効になります。

このポリシーを False に設定した場合、またはこのポリシーを設定しない場合、Microsoft Edge バージョン 80 以降、Web コンポーネント v0 機能は既定で無効になります。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: WebComponentsV0Enabled
  - GP の名前: M84 まで、Web Components v0 API を再度有効にする (現在不使用)
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: WebComponentsV0Enabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: WebComponentsV0Enabled
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### WebDriverOverridesIncompatiblePolicies
  #### 互換性のないポリシーのオーバーライドを WebDriver に許可する (現在不使用)
  
  >古い形式: このポリシーは古い形式であり、Microsoft Edge 84 以降では使用することができません。
  #### サポートされているバージョン:
  - Windows 以降、macOS と 77 を 84

  #### 説明
  WebDriver が既存のすべてのポリシーと互換性を持っているため、このポリシーは動作しません。

 このポリシーを使用すると、WebDriver 機能を使用するユーザーは、
 動作を妨げる可能性のあるポリシーをオーバーライドできます。

 現在、このポリシーによって無効になるのは [SitePerProcess](#siteperprocess) ポリシーと [IsolateOrigins](#isolateorigins) ポリシーです。

 このポリシーを有効にした場合、WebDriver では互換性のないポリシーを
 オーバーライドできます。
このポリシーを無効にした場合または構成しなかった場合、WebDriver では互換性のないポリシーを
 オーバーライドできません。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: WebDriverOverridesIncompatiblePolicies
  - GP の名前: 互換性のないポリシーのオーバーライドを WebDriver に許可する (現在不使用)
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: WebDriverOverridesIncompatiblePolicies
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  #### Mac の情報と設定
  - 優先されるキーの名前: WebDriverOverridesIncompatiblePolicies
  - サンプル値:
``` xml
<true/>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### WebRtcLocalIpsAllowedUrls
  #### WebRTC によるローカル IP アドレスの公開を管理する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 80

  #### 説明
  WebRTC によってローカル IP アドレスを公開する場合に、その公開の対象となるオリジン (URL) やホスト名パターン ("*contoso.com*"など) のリストを指定します。

このポリシーを有効にして、オリジン (URL) やホスト名パターンのリストを設定した場合、edge://flags/#enable-webrtc-hide-local-ips-with-mdns が有効になっていると、リスト内のパターンに一致したときに、WebRTC によってローカル IP アドレスが公開されます。

このポリシーを無効にした場合または構成しなかった場合に、edge://flags/#enable-webrtc-hide-local-ips-with-mdns が有効になっていても、WebRTC によってローカル IP アドレスは公開されません。ローカル IP アドレスは mDNS ホスト名によって隠されています。

このポリシーを有効/無効にした場合、または構成しなかった場合に edge://flags/#enable-webrtc-hide-local-ips-with-mdns が無効になっていると、WebRTC によってローカル IP アドレスが公開されます。

このポリシーによって、管理者が必要とする可能性があるローカル IP アドレスの保護が弱くなることに注意してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列の一覧

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: WebRtcLocalIpsAllowedUrls
  - GP の名前: WebRTC によるローカル IP アドレスの公開を管理する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls
  - パス (おすすめ): N/A
  - 値の名前: 1, 2, 3, ...
  - 値の種類: REG_SZ の一覧
  ##### サンプル値:
```
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\2 = "*contoso.com*"

```


  #### Mac の情報と設定
  - 優先されるキーの名前: WebRtcLocalIpsAllowedUrls
  - サンプル値:
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>*contoso.com*</string>
</array>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### WebRtcLocalhostIpHandling
  #### WebRTC によるローカル IP アドレスの公開を制限する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  WebRTC がユーザーのローカル IP アドレスを公開するかどうかを設定できます。

このポリシーを「AllowAllInterfaces」または「AllowPublicAndPrivateInterfaces」に設定した場合、WebRTC はローカル IP アドレスを公開します。

このポリシーを「AllowPublicInterfaceOnly」または「DisableNonProxiedUdp」に設定すると、WebRTC はローカル IP アドレスを公開しません。

このポリシーを設定しない場合、または無効にする場合、WebRTC はローカル IP アドレスを公開します。

ポリシー オプションのマッピング:

* AllowAllInterfaces (default) = すべてのインターフェイスを許可する。これにより、ローカル IP アドレスが公開されます

* AllowPublicAndPrivateInterfaces (default_public_and_private_interfaces) = http の既定ルートでパブリック インターフェースやプライベート インターフェイスを許可する。これにより、ローカル IP アドレスが公開されます

* AllowPublicInterfaceOnly (default_public_interface_only) = http の既定ルートでパブリック インターフェイス許可する。これにより、ローカル IP アドレスが公開されなくなります

* DisableNonProxiedUdp (disable_non_proxied_udp) = プロキシ サーバーが UDP をサポートしていない場合は TCP を使用する。これにより、ローカル IP アドレスが公開されなくなります

このポリシーを構成するときは、前述の情報を使用してください。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: WebRtcLocalhostIpHandling
  - GP の名前: WebRTC によるローカル IP アドレスの公開を制限する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: WebRtcLocalhostIpHandling
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"default"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: WebRtcLocalhostIpHandling
  - サンプル値:
``` xml
<string>default</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### WebRtcUdpPortRange
  #### WebRTC で使用されるローカル UDP ポートの範囲を制限する
  
  
  #### サポートされているバージョン:
  - Windows 以降の macOS と 77

  #### 説明
  WebRTC で使用される UDP ポート範囲を、指定されたポート間隔 (エンドポイントも含む) に制限します。

このポリシー設定を構成することで、WebRTC で使用できるローカル UDP ポートの範囲を指定できます。

このポリシーを構成しなかった場合、または空の文字列あるいは無効なポート範囲に設定した場合、WebRTC では、利用可能な任意のローカル UDP ポートを使用できます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - 文字列

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: WebRtcUdpPortRange
  - GP の名前: WebRTC で使用されるローカル UDP ポートの範囲を制限する
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: WebRtcUdpPortRange
  - 値の種類: REG_SZ
  ##### サンプル値:
```
"10000-11999"
```


  #### Mac の情報と設定
  - 優先されるキーの名前: WebRtcUdpPortRange
  - サンプル値:
``` xml
<string>10000-11999</string>
```
  

  [トップに戻る](#microsoft-edge---ポリシー)

  ### WinHttpProxyResolverEnabled
  #### Windows プロキシ リゾルバーを使用 (非推奨)
  >非推奨: このポリシーは推奨されていません。現在サポートされていますが、将来のリリースでは使用されなくなります。
  
  #### サポートされているバージョン:
  - Windows 以降の 84

  #### 説明
  このポリシーは、今後のリリースで同様の機能に置き換わるため、廃止されました。https://crbug.com/1032820 をご覧ください。

Microsoft Edge に組み込まれたプロキシ リゾルバーの代わりに、Windows を使用してすべてのブラウザー ネットワークのプロキシを解決します。Windows プロキシ リゾルバーは、DirectAccess/NRPT などの Windows プロキシ機能を有効にします。

このポリシーには、https://crbug.com/644030 で説明されている問題が伴います。これにより、[ProxyPacUrl](#proxypacurl) ポリシーで設定された PAC ファイルを含む PAC ファイルが Windows のコードによって取得および実行されます。PAC ファイルのネットワーク取得が Microsoft Edge のコードではなく Windows によって行われるため、[DnsOverHttpsMode](#dnsoverhttpsmode) などのネットワーク ポリシーは PAC ファイルのネットワーク取得には適用されません。

このポリシーを有効にすると、Windows プロキシ リゾルバーが使用されます。

このポリシーを無効にするか、構成しない場合は、Microsoft Edge プロキシ リゾルバーが使用されます。

  #### サポートされている機能:
  - 必須になる場合があります: はい
  - 推奨される場合があります: いいえ
  - 動的ポリシーの更新: いいえ - ブラウザーの再起動が必要です

  #### データ型:
  - ブール値

  #### Windows の情報と設定
  ##### グループ ポリシー (ADMX) 情報
  - GP 固有の名前: WinHttpProxyResolverEnabled
  - GP の名前: Windows プロキシ リゾルバーを使用 (非推奨)
  - GP パス (必須): 管理用テンプレート/Microsoft Edge/
  - GP パス (おすすめ): N/A
  - GP ADMX ファイル名: MSEdge.admx
  ##### Windows レジストリの設定
  - パス (必須): SOFTWARE\Policies\Microsoft\Edge
  - パス (おすすめ): N/A
  - 値の名前: WinHttpProxyResolverEnabled
  - 値の種類: REG_DWORD
  ##### サンプル値:
```
0x00000001
```


  

  [トップに戻る](#microsoft-edge---ポリシー)


## 関連項目
- [Microsoft Edge の構成](configure-microsoft-edge.md)
- [Microsoft Edge Enterprise ランディング ページ](https://aka.ms/EdgeEnterprise)
- [Microsoft Security ベースライン ブログ](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)