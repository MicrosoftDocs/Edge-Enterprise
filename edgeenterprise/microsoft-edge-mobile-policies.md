---
title: "Microsoft Edge Mobile Policy Documentation"
ms.author: stmoody
author: dan-wesley
manager: venkatk
ms.date: 10/10/2024
audience: ITPro
ms.topic: reference
ms.service: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: generated
description: "Windows and Mac documentation for all policies supported by the Microsoft Edge Browser"
---

# Microsoft Edge Mobile - Policies

The latest version of Microsoft Edge includes the following policies that you can deploy to configure how Microsoft Edge mobile runs in your organization. You can use the mobile device management (MDM) OS channel on enrolled devices ([Managed App Configuration](https://developer.apple.com/library/archive/samplecode/sc2279/Introduction/Intro.html) for iOS or [Set up managed configurations](https://developer.android.com/work/managed-configurations) for Android). Users aren't required to sign in to Microsoft Edge to apply the policies.

> [!NOTE]
> The MDM OS channel in Microsoft Intune is a Managed Devices App Configuration Policy (ACP). For more information, see [Managed Devices ACP](/mem/intune/apps/app-configuration-policies-overview#apps-that-support-app-configuration). If you're not using Microsoft Intune, consult your Unified Endpoint Management (UEM) documentation to learn how to deploy these policies through mobile device management.

> [!NOTE]
> For Microsoft Edge Browser policy reference, see [Microsoft Edge - Policies](/deployedge/microsoft-edge-policies)

## Available policies

These tables list all of the browser-related policies available in this release of Microsoft Edge. Use the links in the table to get more details about specific policies.

- [Edge specific](#edge-specific)
- [Proxy server](#proxy-server)
- [HTTP authentication](#http-authentication)
- [Content settings](#content-settings)
- [Default search provider](#default-search-provider)
- [Password manager and protection](#password-manager-and-protection)
- [Idle browser actions](#idle-browser-actions)
- [Additional](#additional)
- [Edge website typo protection settings](#edge-website-typo-protection-settings)
<!-- ====================================== -->
### [*Edge specific*](#edge-specific)

|Policy Name|Caption|
|:-|-|
| [EdgeNewTabPageCustomURL](#edgenewtabpagecustomurl) | Homepage instead of New Tab Page experience |
| [EdgeMyApps](#edgemyapps) | My Apps bookmark  |
| [EdgeDefaultHTTPS](#edgedefaulthttps) |  Default protocol handler |
| [EdgeDisableShareUsageData](#edgedisableshareusagedata) |  Disable data sharing usage data for personalization   |
| [EdgeDisabledFeatures](#edgedisabledfeatures)  |   Disable specific features  |
| [EdgeEnableKioskMode](#edgeenablekioskmode)  |  Kiosk mode experiences on Android devices   |
| [EdgeShowAddressBarInKioskMode](#edgeshowaddressbarinkioskmode)   |   Kiosk mode address bar experiences on Android devices  |
| [EdgeShowBottomBarInKioskMode](#edgeshowbottombarinkioskmode)   |   Kiosk mode bottom bar experiences on Android devices   |
| [EdgeSyncDisabled](#edgesyncdisabled)  |   Manage account synchronization  |
| [EdgeNetworkStackPref](#edgenetworkstackpref)   |   Switch network stack between Chromium and iOS  |
| [EdgeImportPasswordsDisabled](#edgeimportpasswordsdisabled) |  Disable the import of passwords  |
| [OverlayPermissionDetectionEnabled](#overlaypermissiondetectionenabled) | Enable Overlay Permission Detection  |
| [EdgeBrandLogo](#edgebrandlogo)   | Configure Brand logo in New Tab Page  |
| [EdgeBrandColor](#edgebrandcolor)  | Configure Brand color in New Tab Page  |
| [EdgeProxyPacUrl](#edgeproxypacurl) | Specify a URL to a proxy auto-config (PAC) file  |
| [EdgeBlockSignInEnabled](#edgeblocksigninenabled) | Block users from signing in to Edge |
| [EdgeOneAuthProxy](#edgeoneauthproxy) | Specify a dedicated proxy to sign in to Edge in Android   |
| [EdgeLockedViewModeEnabled](#edgelockedviewmodeenabled)  | Edge locked view mode    |
| [EdgeLockedViewModeAllowedActions](#edgelockedviewmodeallowedactions)  |  Configure allowed actions in Edge locked view mode   |
| [EdgeCopilotEnabled](#edgecopilotenabled)  |  Enable Copilot in Edge  |
| [EdgeNewTabPageLayout](#edgenewtabpagelayout)  |  Manage New Tab Page layout settings  |
| [EdgeNewTabPageLayoutCustom](#edgenewtabpagelayoutcustom)  | Manage New Tab Page custom setting   |
| [EdgeNewTabPageLayoutUserSelectable](#edgenewtabpagelayoutuserselectable)  |  Manage whether the New Tab Page layout is selectable by users  |
| [EdgeSharedDeviceSupportEnabled](#edgeshareddevicesupportenabled) | Disable shared device mode |

<!-- ====================================== -->
### [*Proxy server*](#proxy-server)

|Policy Name|Caption|
|:-|-|
| [ProxySettings](#proxysettings) | Proxy settings   |
<!-- ====================================== -->
### [*HTTP authentication*](#http-authentication)

|Policy Name|Caption|
|:-|-|
| [NtlmV2Enabled](#ntlmv2enabled)  | Enable NTLMv2 authentication    |
| [AuthSchemes](#authschemes)  |  Supported authentication schemes   |
| [DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)   |  Disable CNAME lookup when negotiating Kerberos authentication   |
| [AuthServerAllowlist](#authserverallowlist)  |  Authentication server allowlist   |
| [AuthAndroidNegotiateAccountType](#authandroidnegotiateaccounttype) |  Account type for HTTP Negotiate authentication   |
| [AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)  |  Kerberos delegation server allowlist   |
| [AllHttpAuthSchemesAllowedForOrigins](#allhttpauthschemesallowedfororigins) | List of origins allowing all HTTP authentication  |
<!-- ====================================== -->
### [*Content settings*](#content-settings)

|Policy Name|Caption|
|:-|-|
| [DefaultPopupsSetting](#defaultpopupssetting)   |  Default pop-ups setting   |
| [PopupsAllowedForUrls](#popupsallowedforurls) | Allow pop-up windows on specific sites   |
| [PopupsBlockedForUrls](#popupsblockedforurls) | Block pop-up windows on specific sites   |
| [DefaultCookiesSetting](#defaultcookiessetting)   |   Default cookies setting   |
| [CookiesAllowedForUrls](#cookiesallowedforurls)   |   Allow cookies on these sites  |
| [CookiesBlockedForUrls](#cookiesblockedforurls)   |   Block cookies on these sites  |
| [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)   |  Limit cookies from matching URLs to the current session  |
<!-- ====================================== -->
### [*Default search provider*](#default-search-provider)

|Policy Name|Caption|
|:-|-|
| [DefaultSearchProviderEnabled](#defaultsearchproviderenabled)   |     |
| [DefaultSearchProviderName](#defaultsearchprovidername)   | Default search provider name   |
| [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)   |  Default search provider search URL   |
| [DefaultSearchProviderSearchURLPostParams](#defaultsearchprovidersearchurlpostparams)   |  Parameters for search URL which uses POST   |
| [DefaultSearchProviderAlternateURLs](#defaultsearchprovideralternateurls)   |  List of alternate URLs for the default search provider   |
| [DefaultSearchProviderEncodings](#defaultsearchproviderencodings)   |  Default search provider encodings   |
| [DefaultSearchProviderImageURL](#defaultsearchproviderimageurl)   |  Parameter providing search-by-image feature for the default search provider   |
| [DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams)   |  Parameters for image URL which uses POST   |
| [DefaultSearchProviderKeyword](#defaultsearchproviderkeyword)   |  Default search provider keyword   |
| [DefaultSearchProviderNewTabURL](#defaultsearchprovidernewtaburl)   |  Default search provider new tab page URL   |
| [DefaultSearchProviderSuggestURL](#defaultsearchprovidersuggesturl)   |  Default search provider suggest URL  |
| [DefaultSearchProviderSuggestURLPostParams](#defaultsearchprovidersuggesturlpostparams)   |   Parameters for suggest URL which uses POST  |
<!-- ====================================== -->
### [*Password manager and protection*](#password-manager-and-protection)

|Policy Name|Caption|
|:-|-|
| [PasswordManagerEnabled](#passwordmanagerenabled) | Enable saving passwords to the password manager |

<!-- ====================================== -->
### [*Idle browser actions*](#idle-browser-actions)

|Policy Name|Caption|
|:-|-|
| [IdleTimeout](#idletimeout) | Delay before running idle actions |
| [IdleTimeoutActions](#idletimeoutactions) | Actions to run when the computer is idle |
<!-- ====================================== -->
### [*Additional*](#additional)

|Policy Name|Caption|
|:-|-|
| [URLAllowlist](#urlallowlist)    |  Allow access to a list of URLs |
| [URLBlocklist](#urlblocklist)   |  Block access to a list of URLs   |
| [SSLErrorOverrideAllowed](#sslerroroverrideallowed)   |  Allow proceeding from the SSL warning page   |
| [CertificateTransparencyEnforcementDisabledForUrls](#certificatetransparencyenforcementdisabledforurls)   |  Disable Certificate Transparency enforcement for a list of URLs   |
| [CertificateTransparencyEnforcementDisabledForCas](#certificatetransparencyenforcementdisabledforcas)   |  Disable Certificate Transparency enforcement for a list of subjectPublicKeyInfo hashes   |
| [SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)   | Disable saving browser history    |
| [SearchSuggestEnabled](#searchsuggestenabled)   |  Enable search suggestions   |
| [TranslateEnabled](#translateenabled)   | Enable Translate    |
| [InPrivateModeAvailability](#inprivatemodeavailability) | InPrivate mode availability |
| [SmartScreenEnabled](#smartscreenenabled) | Configure Microsoft Defender SmartScreen |
| [MicrosoftRootStoreEnabled](#microsoftrootstoreenabled) | Determines whether the Microsoft Root Store and built-in certificate verifier will be used to verify server certificates |
| [ManagedFavorites](#managedfavorites)  |  Configure Favorites (bookmarks) |
| [ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol) |  Control communication with the Experimentation and Configuration Service   |
|  [HideFirstRunExperience](#hidefirstrunexperience)  |  Hide the First-run experience  |
|  [DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)  |  Set Microsoft Edge as default browser  |
<!-- ====================================== -->
### [Edge website typo protection settings](#edge-website-typo-protection)

|Policy Name|Caption|
|:-|-|
| [PreventTyposquattingPromptOverride](#preventtyposquattingpromptoverride) | Prevent bypassing Edge Website Typo Protection prompts for sites |
| [TyposquattingAllowListDomains](#typosquattingallowlistdomains) | Configure the list of domains for which Edge Website Typo Protection won't trigger warnings |

## HTTP authentication

[Back to top](#microsoft-edge-mobile---policies)

### NtlmV2Enabled

#### Enable NTLMv2 authentication

#### Supported on:

- Microsoft Edge (Android) since version 109

#### Description

Setting the policy to Enabled or leaving it unset turns NTLMv2 on.

Setting the policy to Disabled turns NTLMv2 off.

All recent versions of Samba and Microsoft&reg; Windows&reg; servers support NTLMv2. This should only be turned off for backward compatibility as it reduces the security of authentication.

- true = Turn NTLMv2 on
- false = Turn NTLMv2 off

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

Boolean

Android:choice

#### Android restriction name:

```
NtlmV2Enabled
```

##### Example value:

```
true
```

[Back to top](#microsoft-edge-mobile---policies)

### AuthSchemes

#### Supported authentication schemes

#### Supported on:

- Microsoft Edge (Android) since version 109

#### Description

Setting the policy specifies which HTTP authentication schemes Microsoft Edge supports.

Leaving the policy unset employs all 4 schemes.

Valid values:

\* basic

\* digest

\* ntlm

\* negotiate

Note: Separate multiple values with commas.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

String

Android:choice

#### Android restriction name:

```
AuthSchemes
```

##### Example value:

```
basic,digest,ntlm,negotiate
```

[Back to top](#microsoft-edge-mobile---policies)

### DisableAuthNegotiateCnameLookup

#### Disable CNAME lookup when negotiating Kerberos authentication

#### Supported on:

- Microsoft Edge (Android) since version 109

#### Description

Setting the policy to Enabled skips CNAME lookup. The server name is used as entered when generating the Kerberos SPN.

Setting the policy to Disabled or leaving it unset means CNAME lookup determines the canonical name of the server when generating the Kerberos SPN.

- true = Disable CNAME lookup during Kerberos authentication
- false = Use CNAME lookup during Kerberos authentication

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

Boolean

Android:choice

#### Android restriction name:

```
DisableAuthNegotiateCnameLookup
```

##### Example value:

```
false
```

[Back to top](#microsoft-edge-mobile---policies)

### AuthServerAllowlist

#### Authentication server allowlist

#### Supported on:

- Microsoft Edge (Android) since version 109

#### Description

Setting the policy specifies which servers should be allowed for integrated authentication. Integrated authentication is only on when Microsoft Edge gets an authentication challenge from a proxy or from a server in this permitted list.

Leaving the policy unset means Microsoft Edge tries to detect if a server is on the intranet. Only then will it respond to IWA requests. If a server is detected as internet, then Microsoft Edge ignores IWA requests from it.

Note: Separate multiple server names with commas. Wildcards, *, are allowed.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

String

Android:choice

#### Android restriction name:

```
AuthServerAllowlist
```

##### Example value:

```
*.example.com,example.com
```

[Back to top](#microsoft-edge-mobile---policies)

### AuthAndroidNegotiateAccountType

#### Account type for HTTP Negotiate authentication

#### Supported on:

- Microsoft Edge (Android) since version 118

#### Description

Specifies the type of accounts provided by the Android authentication app that supports HTTP Negotiate authentication (such as Kerberos authentication). This information should be available from the supplier of the authentication app. For more details see, [Write a SPNEGO Authenticator for Microsoft Edge on Android](/DeployEdge/edge-learnmore-write-spnego-authenticator).

If you disable or don't configure this policy, HTTP Negotiate authentication on Android is turned off.

If you enable the policy, Microsoft Edge will use the value to specify the Android authentication app

#### Supported features:

- Dynamic Policy Refresh : No
- Per Profile : No

#### Data Type:

Android:String

#### Android restriction name:

```
AuthAndroidNegotiateAccountType
```

##### Example value (Android):

```
com.example.spnego
```

[Back to top](#microsoft-edge-mobile---policies)

### AuthNegotiateDelegateAllowlist

#### Kerberos delegation server allowlist

#### Supported on:

Microsoft Edge (Android) since version 109

#### Description

Setting the policy assigns servers that Microsoft Edge may delegate to. Separate multiple server names with commas. Wildcards, *, are allowed.

Leaving the policy unset means Microsoft Edge won't delegate user credentials, even if a server is detected as intranet.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

String

Android:choice

#### Android restriction name:

```
AuthNegotiateDelegateAllowlist
```

##### Example value:

```
*.example.com,foobar.example.com
```

[Back to top](#microsoft-edge-mobile---policies)

### AllHttpAuthSchemesAllowedForOrigins

#### List of origins allowing all HTTP authentication

#### Supported on:

* Microsoft Edge (Android) since version 109

#### Description

Setting the policy specifies for which origins to allow all the HTTP authentication schemes Google Chrome supports regardless of the AuthSchemes policy.

Format the origin pattern according to this format (https://go.microsoft.com/fwlink/?linkid=2095322). Up to 1,000 exceptions can be defined in AllHttpAuthSchemesAllowedForOrigins. Wildcards are allowed for the whole origin or parts of the origin, either the scheme, host, port.

#### Supported features:
- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

List of strings

Android:string

#### Android restriction name:

```
AllHttpAuthSchemesAllowedForOrigins
```

##### Example value (Android):

```
[
 "*.example.com"
]
```

[Back to top](#microsoft-edge-mobile---policies)

## Content settings

[Back to top](#microsoft-edge-mobile---policies)

### DefaultPopupsSetting

#### Default pop-ups setting

#### Supported on:

- Microsoft Edge (Android) since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

Setting the policy to 1 lets websites display pop-ups. Setting the policy to 2 denies pop-ups.

Leaving it unset means BlockPopups applies, but users can change this setting.

- 1 = Allow all sites to show pop-ups
- 2 = Do not allow any site to show pop-ups

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

Android:Integer

iOS:Integer

#### Android and iOS restriction name:

```
DefaultPopupsSetting
```

##### Example value (Android and iOS):

```
1
```

[Back to top](#microsoft-edge-mobile---policies)

### PopupsAllowedForUrls

#### Allow pop-up windows on specific sites

#### Supported on:

- Microsoft Edge (Android) since version 120
- Microsoft Edge (iOS and iPadOS) since version 120

#### Description

Define a list of sites, based on URL patterns, that can open pop-up windows. * is not an accepted value for this policy.

If you don't configure this policy, the global default value from the [DefaultPopupsSetting](/deployedge/microsoft-edge-mobile-policies#defaultpopupssetting) policy (if set) or the user's personal configuration is used for all sites.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

List of strings

#### Android and iOS restriction name:

```
PopupsAllowedForUrls
```

##### Example value (Android):

```
[
"https://www.contoso.com",
"[*.] contoso.edu"
]
```

##### Example value (iOS):

```
<array>

  <string>https://www.contoso.com</string>

  <string>[*.]contoso.edu</string>

</array>
```

[Back to top](#microsoft-edge-mobile---policies)  

### PopupsBlockedForUrls

#### Block pop-up windows on specific sites

#### Supported on:

- Microsoft Edge (Android) since version 120
- Microsoft Edge (iOS and iPadOS) since version 120

#### Description

Define a list of sites, based on URL patterns, that are blocked from opening pop-up windows. * is not an accepted value for this policy.

If you don't configure this policy, the global default value from the [DefaultPopupsSetting](/deployedge/microsoft-edge-mobile-policies#defaultpopupssetting) policy (if set) or the user's personal configuration is used for all sites.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

List of strings

#### Android and iOS restriction name:

```
PopupsBlockedForUrls
```

##### Example value (Android):

```
[
https://www.contoso.com,
"[*.] contoso.edu"
]
```

##### Example value (iOS):

```
<array>

  <string>https://www.contoso.com</string>

  <string>[*.]contoso.edu</string>

</array>
```

[Back to top](#microsoft-edge-mobile---policies) 
### DefaultCookiesSetting

#### Default cookies setting

#### Supported on:

Microsoft Edge (Android) since version 109

#### Description

Unless the RestoreOnStartup policy is set to permanently restore URLs from previous sessions, then setting CookiesSessionOnlyForUrls lets you make a list of URL patterns that specify sites that can and can't set cookies for one session.

Leaving the policy unset results in the use of DefaultCookiesSetting for all sites, if it's set. If not, the user's personal setting applies. URLs not covered by the patterns specified also result in the use of defaults.

While no specific policy takes precedence, see CookiesBlockedForUrls and CookiesAllowedForUrls. URL patterns among these 3 policies must not conflict.

- 1 = Allow all sites to set local data
- 2 = Do not allow any site to set local data
- 4 = Keep cookies for the duration of the session

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

Integer

Android:choice

#### Android restriction name:

```
DefaultCookiesSetting
```

##### Example value:

```
1
```

[Back to top](#microsoft-edge-mobile---policies)


### CookiesAllowedForUrls

#### Allow cookies on these sites

#### Supported on:

- Microsoft Edge (Android) since version 109

#### Description

Allows you to set a list of url patterns that specify sites which are allowed to set cookies.

If this policy is left not set the global default value will be used for all sites either from the DefaultCookiesSetting policy if it is set, or the user's personal configuration otherwise.

See also policies CookiesBlockedForUrls and CookiesSessionOnlyForUrls. Note that there must be no conflicting URL patterns between these three policies - it is unspecified which policy takes precedence.

For detailed information on valid url patterns, please see https://go.microsoft.com/fwlink/?linkid=2095322. * is not an accepted value for this policy.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

List of strings

Android:string

#### Android restriction name:

```
CookiesAllowedForUrls
```

##### Example value:

```
[
 "https://www.example.com",
 "[*.]example.edu"
]
```

[Back to top](#microsoft-edge-mobile---policies)


### CookiesBlockedForUrls

#### Block cookies on these sites

#### Supported on:

Microsoft Edge (Android) since version 109

#### Description

Setting the policy lets you make a list of URL patterns that specify sites that can't set cookies.

Leaving the policy unset results in the use of DefaultCookiesSetting for all sites, if it's set. If not, the user's personal setting applies.

While no specific policy takes precedence, see CookiesAllowedForUrls and CookiesSessionOnlyForUrls. URL patterns among these 3 policies must not conflict.

For detailed information on valid url patterns, please see https://go.microsoft.com/fwlink/?linkid=2095322. * is not an accepted value for this policy.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

List of strings

Android:string

#### Android restriction name:

```
CookiesBlockedForUrls
```

##### Example value:

```
[
 "https://www.example.com",
 "[*.]example.edu"
]
```

[Back to top](#microsoft-edge-mobile---policies)


### CookiesSessionOnlyForUrls

#### Limit cookies from matching URLs to the current session

#### Supported on:

- Microsoft Edge (Android) since version 109

#### Description

Unless the RestoreOnStartup policy is set to permanently restore URLs from previous sessions, then setting CookiesSessionOnlyForUrls lets you make a list of URL patterns that specify sites that can and can't set cookies for one session.

Leaving the policy unset results in the use of DefaultCookiesSetting for all sites, if it's set. If not, the user's personal setting applies. URLs not covered by the patterns specified also result in the use of defaults.

While no specific policy takes precedence, see CookiesBlockedForUrls and CookiesAllowedForUrls. URL patterns among these 3 policies must not conflict.

For detailed information on valid url patterns, please see https://go.microsoft.com/fwlink/?linkid=2095322. * is not an accepted value for this policy.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

List of strings

Android:string

#### Android restriction name:

```
CookiesSessionOnlyForUrls
```

##### Example value:

```
[
 "https://www.example.com",
 "[*.]example.edu"
]
```

[Back to top](#microsoft-edge-mobile---policies)

## Default search provider

[Back to top](#microsoft-edge-mobile---policies)

### DefaultSearchProviderEnabled

#### Enable the default search provider

#### Supported on:

- Microsoft Edge (Android) since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

Setting the policy to Enabled means a default search is performed when a user enters non-URL text in the address bar. To specify the default search provider, set the rest of the default search policies. If you leave those policies empty, the user can choose the default provider. Setting the policy to Disabled means there's no search when the user enters non-URL text in the address bar.

If you set the policy, users can't change it in Microsoft Edge. If not set, the default search provider is on, and users can set the search provider list.

- true = Enable the default search provider
- false = Disable the default search provider
- not set = Enable the default search provider and allow users to modify the search provier list

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes
- Can Be Recommended : Yes

#### Data Type:

Android:Boolean

iOS:Boolean

#### Android and iOS restriction name:

```
DefaultSearchProviderEnabled
```

##### Example value (Android and iOS):

```
true
```

[Back to top](#microsoft-edge-mobile---policies)

### DefaultSearchProviderName

#### Default search provider name

#### Supported on:

- Microsoft Edge (Android) since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

If DefaultSearchProviderEnabled is on, then setting DefaultSearchProviderName specifies the default search provider's name.

Leaving DefaultSearchProviderName unset means the hostname specified by the search URL is used.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes
- Can Be Recommended : Yes

#### Data Type:

Android:String

iOS:String

#### Android and iOS restriction name:

```
DefaultSearchProviderName
```

##### Example value (Android and iOS):

```
My Intranet Search
```

[Back to top](#microsoft-edge-mobile---policies)

### DefaultSearchProviderSearchURL

#### Default search provider search URL

#### Supported on:

- Microsoft Edge (Android) since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

If DefaultSearchProviderEnabled is on, then setting DefaultSearchProviderSearchURL specifies the URL of the search engine used during a default search. The URL should include the string '{searchTerms}', replaced in the query by the user's search terms.

You can specify Google's search URL as: '{google:baseURL}search?q={searchTerms}&{google:RLZ}{google:originalQueryForSuggestion}{google:assistedQueryStats}{google:searchFieldtrialParameter}{google:searchClient}{google:sourceId}ie={inputEncoding}'.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes
- Can Be Recommended : Yes

#### Data Type:

Android:String

iOS:String

#### Android and iOS restriction name:

```
DefaultSearchProviderSearchURL
```

##### Example value (Android and iOS):

```
https://search.my.company/search?q={searchTerms}
```

[Back to top](#microsoft-edge-mobile---policies)


### DefaultSearchProviderSearchURLPostParams

#### Parameters for search URL which uses POST

#### Supported on:

- Microsoft Edge (Android) since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

If DefaultSearchProviderEnabled is on, then setting DefaultSearchProviderSearchURLPostParams specifies the parameters when searching a URL with POST. It consists of comma-separated, name-value pairs. If a value is a template parameter, such as '{searchTerms}', real search terms data replaces it.

Leaving DefaultSearchProviderSearchURLPostParams unset means search requests are sent using the GET method.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes
- Can Be Recommended : Yes

#### Data Type:

Android:String

iOS:String

#### Android and iOS restriction name:

```
DefaultSearchProviderSearchURLPostParams
```

##### Example value (Android and iOS):

```
q={searchTerms},ie=utf-8,oe=utf-8
```

[Back to top](#microsoft-edge-mobile---policies)


### DefaultSearchProviderAlternateURLs

#### List of alternate URLs for the default search provider

#### Supported on:

- Microsoft Edge (Android) since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

If DefaultSearchProviderEnabled is on, then setting DefaultSearchProviderAlternateURLs specifies a list of alternate URLs for extracting search terms from the search engine. The URLs should include the string '{searchTerms}'.

Leaving DefaultSearchProviderAlternateURLs unset means no alternate URLs are used to extract search terms.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes
- Can Be Recommended : Yes

#### Data Type:

List of strings

Android:string

iOS:String

#### Android and iOS restriction name:

```
DefaultSearchProviderAlternateURLs
```

##### Example value (Android and iOS):

```
[
 "https://search.my.company/suggest#q={searchTerms}",
 "https://search.my.company/suggest/search#q={searchTerms}"
]
```

[Back to top](#microsoft-edge-mobile---policies)


### DefaultSearchProviderEncodings

#### Default search provider encodings

#### Supported on:

- Microsoft Edge (Android) since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

If DefaultSearchProviderEnabled is on, setting DefaultSearchProviderEncodings specifies the character encodings supported by the search provider. Encodings are code page names such as UTF-8, GB2312, and ISO-8859-1. They're tried in the order provided.

Leaving DefaultSearchProviderEncodings unset puts UTF-8 in use.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes
- Can Be Recommended : Yes

#### Data Type:

List of strings

Android:string

iOS:string

#### Android and iOS restriction name:

```
DefaultSearchProviderEncodings
```

##### Example value (Android and iOS):

```
[
 "UTF-8",
 "UTF-16",
 "GB2312",
 "ISO-8859-1"
]
```

[Back to top](#microsoft-edge-mobile---policies)

<!---   pause here until data type: query answered --->
### DefaultSearchProviderImageURL

#### Parameter providing search-by-image feature for the default search provider

#### Supported on:

- Microsoft Edge (Android) since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

If DefaultSearchProviderEnabled is on, then setting DefaultSearchProviderImageURL specifies the URL of the search engine used for image search. (If DefaultSearchProviderImageURLPostParams is set, then image search requests use the POST method instead.)

Leaving DefaultSearchProviderImageURL unset means no image search is used.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes
- Can Be Recommended : Yes

#### Data Type:

Android: String

iOS:String

#### Android and iOS restriction name:

```
DefaultSearchProviderImageURL
```

##### Example value (Android and iOS):

```
https://search.my.company/searchbyimage/upload
```

[Back to top](#microsoft-edge-mobile---policies)

### DefaultSearchProviderImageURLPostParams

#### Parameters for image URL which uses POST

#### Supported on:

- Microsoft Edge (Android) since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

If DefaultSearchProviderEnabled is on, then setting DefaultSearchProviderImageURLPostParams specifies the parameters during image search with POST. It consists of comma-separated, name-value pairs. If a value is a template parameter, such as {imageThumbnail}, real image thumbnail data replaces it.

Leaving DefaultSearchProviderImageURLPostParams unset means image search request is sent using the GET method.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes
- Can Be Recommended : Yes

#### Data Type:

Android:String

iOS:String

#### Android and iOS restriction name:

```
DefaultSearchProviderImageURLPostParams
```

##### Example value (Android and iOS):

```
content={imageThumbnail},url={imageURL},sbisrc={SearchSource}
```

[Back to top](#microsoft-edge-mobile---policies)

### DefaultSearchProviderKeyword

#### Default search provider keyword

#### Supported on:

- Microsoft Edge (Android) since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

If DefaultSearchProviderEnabled is on, then setting DefaultSearchProviderKeyword specifies the keyword or shortcut used in the address bar to trigger the search for this provider.

Leaving DefaultSearchProviderKeyword unset means no keyword activates the search provider.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes
- Can Be Recommended : Yes

#### Data Type:

Android:String

iOS:String

#### Android and iOS restriction name:

```
DefaultSearchProviderKeyword
```

##### Example value (Android and iOS):

```
mis
```

[Back to top](#microsoft-edge-mobile---policies)


### DefaultSearchProviderNewTabURL

#### Default search provider new tab page URL

#### Supported on:

- Microsoft Edge (Android) since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

If DefaultSearchProviderEnabled is on, then setting DefaultSearchProviderNewTabURL specifies the URL of the search engine used to provide a New Tab page.

Leaving DefaultSearchProviderNewTabURL unset means no new tab page is provided.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes
- Can Be Recommended : Yes

#### Data Type:

Android:String

iOS:String

#### Android and iOS restriction name:

```
DefaultSearchProviderNewTabURL
```

##### Example value (Android and iOS):

```
https://search.my.company/newtab
```

[Back to top](#microsoft-edge-mobile---policies)

### DefaultSearchProviderSuggestURL

#### Default search provider suggest URL

#### Supported on:

- Microsoft Edge (Android) since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

If DefaultSearchProviderEnabled is on, then setting DefaultSearchProviderSuggestURL specifies the URL of the search engine to provide search suggestions. The URL should include the string '{searchTerms}', replaced in the query by the user's search terms.

You can specify Bing's search URL as: '{bing:baseURL}search?q={searchTerms}'.

specify Google's search URL as: '{google:baseURL}complete/search?output=chrome&q={searchTerms}'.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes
- Can Be Recommended : Yes

#### Data Type:

Android:String

iOS:String

#### Android and iOS restriction name:

```
DefaultSearchProviderSuggestURL
```

##### Example value (Android and iOS):

```
https://search.my.company/suggest?q={searchTerms}
```

[Back to top](#microsoft-edge-mobile---policies)

### DefaultSearchProviderSuggestURLPostParams

#### Parameters for suggest URL which uses POST

#### Supported on:

- Microsoft Edge (Android) since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

If DefaultSearchProviderEnabled is on, then setting DefaultSearchProviderSuggestURLPostParams specifies the parameters during suggestion search with POST. It consists of comma-separated, name-value pairs. If a value is a template parameter, such as '{searchTerms}', real search terms data replaces it.

Leaving DefaultSearchProviderSuggestURLPostParams unset unset means suggest search requests are sent using the GET method.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes
- Can Be Recommended : Yes

#### Data Type:

Android:String

iOS:String

#### Android and iOS restriction name:

```
DefaultSearchProviderSuggestURLPostParams
```

##### Example value (Android and iOS):

```
q={searchTerms},ie=utf-8,oe=utf-8
```

[Back to top](#microsoft-edge-mobile---policies)

## Edge specific policies

[Back to top](#microsoft-edge-mobile---policies)

### EdgeNewTabPageCustomURL

#### Homepage instead of New Tab Page experience

#### Supported on:

* Microsoft Edge (Android) since version 111

* Microsoft Edge (iOS and iPadOS) since version 111

#### Description

Edge for iOS and Android allows organizations to disable the New Tab Page experience and instead have a web site launch when the user opens a new tab. 

While this is a supported scenario, Microsoft recommends organizations take advantage of the New Tab Page experience to provide dynamic content that is relevant to the user.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes
- Can Be Recommended : Yes

#### Data Type:

Android:String

iOS:String

#### Android and iOS restriction name:

```
EdgeNewTabPageCustomURL
```

##### Example value (Android and iOS):

```
https://www.bing.com
```

[Back to top](#microsoft-edge-mobile---policies)

### EdgeMyApps

#### My Apps bookmark

#### Supported on:

* Microsoft Edge (Android) since version 111

* Microsoft Edge (iOS and iPadOS) since version 111

#### Description

By default, users have the My Apps bookmark configured within the organization folder inside Edge for iOS and Android.

- true = Shows My Apps within the Edge for iOS and Android bookmarks 
- false (Default) = Hides My Apps within Edge for iOS and Android

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

Android:Boolean

iOS:Boolean

#### Android and iOS restriction name:

```
EdgeMyApps
```

##### Example value (Android and iOS):

```
true
```

[Back to top](#microsoft-edge-mobile---policies)

### EdgeDefaultHTTPS

#### Default protocol handler

#### Supported on:

* Microsoft Edge (Android) since version 111
* Microsoft Edge (iOS and iPadOS) since version 111

#### Description

By default, Edge for iOS and Android uses the HTTPS protocol handler when the user doesn't specify the protocol in the URL. 

Generally, this is considered a best practice, but can be disabled.

- true (Default) = Default protocol handler is HTTPS 
- false = Default protocol handler is HTTP

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

Android:Boolean

iOS: Boolean

#### Android and iOS restriction name:

```
EdgeDefaultHTTPS
```

##### Example value (Android and iOS):

```
true
```

[Back to top](#microsoft-edge-mobile---policies)

### EdgeDisableShareUsageData
#### Disable data sharing usage data for personalization

#### Supported on:

* Microsoft Edge (Android) since version 111

* Microsoft Edge (iOS and iPadOS) since version 111

#### Description

By default, Edge for iOS and Android prompts users for usage data collection to personalize their browsing experience. Organizations can disable this data sharing by preventing this prompt from being shown to end users.

EdgeDisableShareUsageData:
- true = Disables this prompt from displaying to end users
- false (Default) =  Users are prompted to share usage data

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

Android:Boolean

iOS:Boolean

#### Android and iOS restriction name:

```
EdgeDisableShareUsageData
```

##### Example value (Android and iOS):

```
true
```

[Back to top](#microsoft-edge-mobile---policies)

### EdgeDisabledFeatures

#### Disable specific features

#### Supported on:

* Microsoft Edge (Android) since version 111

* Microsoft Edge (iOS and iPadOS) since version 111

#### Description

Edge for iOS and Android allows organizations to disable certain features that are enabled by default. To disable these features, configure the following setting:

- password = Disables prompts that offer to save passwords for the end user
- inprivate = Disables InPrivate browsing
- autofill = Disables "Save and Fill Addresses" and "Save and Fill Payment info". Autofill will be disabled even for previously saved information.
- translator = Disables translator, as of version 112
- readaloud = Disables Read Aloud, as of version 112
- drop = Disables Drop, which lets you send documents and messages to different devices directly from your browser, as of version 112
- developertools grays out the build version numbers to prevent users from accessing Developer options (Edge for Android only), as of version 112
- coupons = Disables coupons/shopping feature, as of version 117
- extensions = Disables extensions (Edge for Android only), as of version 122

To disable multiple features, separate values with |. For example, inprivate|password disables both InPrivate and password storage.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

Android:String

iOS:String

#### Android and iOS restriction name:

```
EdgeDisabledFeatures
```

##### Example value (Android and iOS):

```
inprivate | password
```

[Back to top](#microsoft-edge-mobile---policies)

### EdgeEnableKioskMode

#### Kiosk mode experiences on Android devices

#### Supported on:

* Microsoft Edge (Android) since version 111

#### Description

Edge for Android can be enabled as a kiosk app with the following settings:

EdgeEnableKioskMode:

- true = Enables kiosk mode for Edge for Android 
- false (Default) = Disables kiosk mode

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

Boolean

Android:choice

#### Android restriction name:

```
EdgeEnableKioskMode

```

##### Example value:

```
true
```

[Back to top](#microsoft-edge-mobile---policies)


### EdgeShowAddressBarInKioskMode

#### Kiosk mode address bar experiences on Android devices

#### Supported on:

* Microsoft Edge (Android) since version 111

#### Description

Edge for Android address bar in kiosk mode can be hidden with the following settings:


EdgeShowAddressBarInKioskMode:

- true = Shows the address bar in kiosk mode 
- false (Default) = Hides the address bar when kiosk mode is enabled

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

Boolean

Android:choice

#### Android restriction name:

```
EdgeShowAddressBarInKioskMode

```

##### Example value:

```
true
```

[Back to top](#microsoft-edge-mobile---policies)


### EdgeShowBottomBarInKioskMode

#### Kiosk mode bottom bar experiences on Android devices

#### Supported on:

* Microsoft Edge (Android) since version 111

#### Description

Edge for Android bottom bar in kiosk mode can be hidden with the following settings:


EdgeShowBottomBarInKioskMode

- true = Shows the bottom action bar in kiosk mode 
- false (Default) =  Hides the bottom bar when kiosk mode is enabled

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

Boolean

Android:choice

#### Android restriction name:

```
EdgeShowBottomBarInKioskMode
```

##### Example value:

```
true
```

[Back to top](#microsoft-edge-mobile---policies)


### EdgeSyncDisabled

#### Manage account synchronization

#### Supported on:

* Microsoft Edge (Android) since version 111

* Microsoft Edge (iOS and iPadOS) since version 111

#### Description

By default, Microsoft Edge sync enables users to access their browsing data across all their signed-in devices. 

The data supported by sync includes:

Favorites

Passwords

Addresses and more (autofill form entry)

Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.

For more information see [Microsoft Edge Sync](/DeployEdge/microsoft-edge-enterprise-sync).

Organizations have the capability to disable Edge sync on iOS and Android.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

Android:Boolean

iOS:Boolean

#### Android and iOS restriction name:

```
EdgeSyncDisabled
```

##### Example value (Android and iOS):

```
true
```

[Back to top](#microsoft-edge-mobile---policies)

<!-- ========= new policy =========== -->

### EdgeImportPasswordsDisabled

#### Disable the import of passwords

#### Supported on:

* Microsoft Edge (iOS and iPadOS) since version 117

#### Description

Edge for iOS and Android allows users to import passwords from Password Manager. Admins can disable import  passwords with the following settings:

EdgeImportPasswordsDisabled

- true = Disable the import of passwords
- false (default) =  Allow the import of passwords

Note:

In the Password Manager of Edge for iOS, there is an **Add** button. When the import passwords feature is disabled, the **Add** button will also be disabled.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

Android:Boolean

iOS:Boolean

#### #### Android and iOS restriction name:

```
EdgeImportPasswordsDisabled
```

##### Example value (Android and iOS):

```
true
```

[Back to top](#microsoft-edge-mobile---policies)

### EdgeNetworkStackPref

#### Switch network stack between Chromium and iOS

#### Supported on:

* Microsoft Edge (iOS and iPadOS) since version 111

#### Description

The layers of the network architecture are called the network stack. 
The layers of a network stack are broadly divided into sections, such as Network Interface, Network Driver Interface Specification (NDIS), Protocol Stack, System Drivers, and User-Mode Applications.

By default, Microsoft Edge for both iOS and Android use the Chromium network stack for Microsoft Edge service communication, including sync services and auto search suggestions. Microsoft Edge for iOS also provides the iOS network stack as a configurable option for Microsoft Edge service communication.

Organizations can modify their network stack preference by configuring the following setting.

- 0 (Default) = Use the Chromium network stack 
- 1 = Use the iOS network stack

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

Integer

iOS:choice

#### Android restriction name:

```
EdgeNetworkStackPref
```

##### Example value:

```
0
```

### OverlayPermissionDetectionEnabled

#### Enable Overlay Permission Detection

#### Description

This policy allows administrators to enable or disable the detection of overlay permissions in Microsoft Edge. 

If any app on the device has overlay drawing permissions, then Microsoft Edge will display an error message stating, "This site can't ask for your permission. Close any bubbles or overlays from other apps, then try again" when the browser requests any device permissions.

If enabled or left unset, Microsoft Edge will turn on this detection feature to remind users of potential risks.

If you disable this policy, Microsoft Edge will turn off this detection feature.

Please note that disabling overlay permission detection may increase the risk of malicious overlays or pop-ups gaining access to sensitive information without user consent. Therefore, it's recommended to use this policy with caution and only in trusted environments or when there's a specific need to bypass overlay detection.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:
Android: boolean

#### Android restriction name:

OverlayPermissionDetectionEnabled

##### Example value:

```
true

```

[Back to top](#microsoft-edge-mobile---policies)

### EdgeBrandLogo

#### Configure Brand logo in New Tab Page

#### Supported on:

- Microsoft Edge (Android) since version 120
- Microsoft Edge (iOS and iPadOS) since version 120

#### Description

Pull your organization's brand logo into Edge for iOS and Android.  You need to maintain your organization logo and brand color via [steps](/entra/fundamentals/how-to-customize-branding). **Banner logo** will be used as your organization and Page background color will be used as brand color. To apply brand logo, users need to sign in to Edge with work account.

- true = Show organization's brand logo
- false (Default) = Do not show organization's brand logo

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

Android:Boolean
iOS:Boolean

#### Android and iOS restriction name:

```
EdgeBrandLogo
```
##### Example value (Android and iOS):

```
true
```
[Back to top](#microsoft-edge-mobile---policies) 

### EdgeBrandColor

#### Configure Brand color in New Tab Page

#### Supported on:

- Microsoft Edge (Android) since version 120
- Microsoft Edge (iOS and iPadOS) since version 120

#### Description

Pull your organization's brand color into Edge for iOS and Android. You need to maintain your organization brand color via [steps](/entra/fundamentals/how-to-customize-branding). **Page background color** will be used as brand color. To apply brand color, users need to sign in to Edge with work account.

- true = Show organization's brand color
- false (Default) = Do not show organization's brand color

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

Android:Boolean
iOS:Boolean

#### Android and iOS restriction name:

```
EdgeBrandColor
```

#####  Example value (Android and iOS):

```
true
```

[Back to top](#microsoft-edge-mobile---policies) 

### EdgeProxyPacUrl

#### Specify a URL to a proxy auto-config (PAC) file

**Note:** This policy is in public preview and might be removed.

#### Supported on:

- Microsoft Edge (iOS and iPadOS) since version 120

#### Description

Specify a URL to a proxy auto-config (PAC) file

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

String

#### iOS restriction name:

```
EdgeProxyPacUrl
```

##### Example value (iOS):

```
https://internal.contoso.com/example.pac
```

[Back to top](#microsoft-edge-mobile---policies) 

### EdgeBlockSignInEnabled

#### Block users from signing in to Edge

#### Supported on:

- Microsoft Edge (Android) since version 121

- Microsoft Edge (iOS and iPadOS) since version 121

#### Description

By default, users are allowed to sign in to Edge with their personal accounts or work accounts. You can enable this policy to block users from signing in to Edge.

#### Supported features:
- Dynamic Policy Refresh: Yes

- Per Profile : No

#### Data Type:

Android:Boolean

iOS:Boolean

#### Android and iOS restriction name:

```
EdgeBlockSignInEnabled
```

#### Example value (Android and iOS):

```
true
```

[Back to top](#microsoft-edge-mobile---policies)

### EdgeOneAuthProxy
#### Specify a dedicated proxy to sign in to Edge in Android
#### Supported on:

- Microsoft Edge (Android) since version 121

#### Description

A Proxy Auto-Configuration (PAC) is typically configured in the VPN profile. However, due to platform limitation, the PAC cannot be recognized by Android WebView, which is used during Edge sign-in process. Users may not be able to sign in to Edge in Android.

You can specify dedicated proxy for users to sign in to Edge in Android.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

Android: String

#### Android restriction name:

```
EdgeOneAuthProxy
```

##### Example value (Android):

```
http://MyProxy.com:8080
```

[Back to top](#microsoft-edge-mobile---policies) 

### EdgeLockedViewModeEnabled

#### Edge locked view mode

#### Supported on:

- Microsoft Edge (Android) since version 117

- Microsoft Edge (iOS and iPadOS) since version 117

#### Description

This policy allows organizations to restrict various browser functionalities, providing a controlled and focused browsing experience.

- The URL address bar becomes read-only, preventing users from making changes to the web address
- Users are not allowed to create new tabs
- The contextual search feature on web pages is disabled
- The following buttons under the overflow menu are disabled

| Buttons | State |
|:-----|:-----|
| New InPrivate tab     |  Disabled   |
| Send to Devices     |  Disabled   |
| Drop     |  Disabled   |
| Add to Phone (Android)     |  Disabled   |
| Download Page (Android)     |  Disabled   |

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

Android: Boolean

iOS: Boolean

#### Android and iOS restriction name:

```
EdgeLockedViewModeEnabled
```

##### Example value (Android and iOS):

```
true
```

[Back to top](#microsoft-edge-mobile---policies)

### EdgeLockedViewModeAllowedActions

#### Configure allowed actions in Edge locked view mode

#### Supported on:

- Microsoft Edge (Android) since version 122

- Microsoft Edge (iOS and iPadOS) since version 122

#### Description

By default, users are not allowed to create new tabs in locked view mode. To allow tab creation, set policy EdgeLockedViewModeAllowedActions.

#### Supported features:

- Dynamic Policy Refresh : Yes

- Per Profile : Yes

#### Data Type:

Android: String

iOS: String

#### Android and iOS restriction name:

```
EdgeLockedViewModeAllowedActions
```
##### Example value (Android and iOS):

```
newtabs
```

[Back to top](#microsoft-edge-mobile---policies)

### EdgeCopilotEnabled 

#### Supported on:

- Microsoft Edge (Android) since version 123.2420.90
- Microsoft Edge (iOS and iPadOS) since version 123.2420.90

#### Description

By default, users can use Copilot in Edge mobile. You can disable Copilot by configuring the policy to false.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

Android:Boolean

iOS:Boolean

#### Android and iOS restriction name:

```
EdgeCopilotEnabled
```

##### Example value (Android and iOS):

```
false
```

[Back to top](#microsoft-edge-mobile---policies)


### EdgeNewTabPageLayout
 
#### Manage New Tab Page layout settings

#### Supported on:

- Microsoft Edge (Android) since version 124.0.2478.71

#### Description

The **Custom** layout is the default one for the new tab page. It shows top site shortcuts and news feed with wallpaper. Users can change the layout according to their preferences. Organizations can also manage the layout settings.

focused = Focused is selected<br>
inspirational = Inspirational is selected<br>
informational = Informational is selected<br>
custom (Default) = Custom is selected, top site shortcuts toggle is on, wallpaper toggle is on, and news feed toggle is on

Note that EdgeNewTabPageLayout policy is intended to set the initial layout. Users can change page layout settings based on their reference. Therefore, EdgeNewTabPageLayout policy only takes effect if users do not change layout settings. You can enforce EdgeNewTabPageLayout policy by configuring EdgeNewTabPageLayoutUserSelectable=false.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

Android: String

#### Android restriction name:

```
EdgeNewTabPageLayout
```
 
##### Example value (Android):

```
focused 
```

[Back to top](#microsoft-edge-mobile---policies)

### EdgeNewTabPageLayoutCustom

#### Manage New Tab Page custom setting

#### Supported on:

- Microsoft Edge (Android) since version 124.0.2478.71

#### Description

By default, topsites, wallpaper and newsfeed are turned on in the custom setting. Organization can manage the custom setting.
This policy only takes affect when EdgeNewTabPageLayout is configured as custom.

topsites = Turn on top site shortcuts<br>
wallpaper = Turn on wallpaper<br>
newsfeed = Turn on news feed<br>

To configure multiple features, separate values with |. 

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

```
Android:String
```

#### Android restriction name:

```
EdgeNewTabPageLayoutCustom
```

##### Example value (Android):

```
topsites | newsfeed
```
[Back to top](#microsoft-edge-mobile---policies)

### EdgeNewTabPageLayoutUserSelectable

#### Manage whether the New Tab Page layout is selectable by users

#### Supported on:

- Microsoft Edge (Android) since version 124.0.2478.71

#### Description

By default, users can change their settings on their own. Organization can manage whether the New Tab Page layout can be changed by users.

- true (default) = Users can change the page layout settings
- false = Users cannot change the page layout settings. The page layout is determined by the values specified via the policy or default values will be used

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

```
Android: Boolean
```

#### Android restriction name:

```
EdgeNewTabPageLayoutUserSelectable
```

##### Example value (Android):

```
false
```

[Back to top](#microsoft-edge-mobile---policies)

### EdgeSharedDeviceSupportEnabled 

#### Disable shared device mode

#### Supported on:

- Microsoft Edge (Android) since version 127
- Microsoft Edge (iOS and iPadOS) since version 126

#### Description

By default, Edge for iOS and Android starts in shared device mode when the devices are enrolled with shared device mode. You can disable shared device mode even in shared devices.

EdgeSharedDeviceSupportEnabled:

- true (default) =  Shared device mode is enabled in shared devices.
- false  = Shared device mode is disabled in shared devices.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

```
Android:Boolean
iOS:Boolean
```

#### Android and iOS restriction name:

```
EdgeSharedDeviceSupportEnabled
```

##### Example value (Android and iOS):

```
false
```

[Back to top](#microsoft-edge-mobile---policies)

<!-- =================================================== -->
## Proxy server policies

[Back to top](#microsoft-edge-mobile---policies)

### ProxySettings

#### Proxy settings

#### Supported on:

- Microsoft Edge (Android) since version 109

#### Description

Setting the policy configures the proxy settings for Chrome and ARC-apps, which ignore all proxy-related options specified from the command line.

Leaving the policy unset lets users choose their proxy settings.

Setting the ProxySettings policy accepts the following fields: * ProxyMode, which lets you specify the proxy server Microsoft Edge uses and prevents users from changing proxy settings * ProxyPacUrl, a URL to a proxy .pac file * ProxyPacMandatory, which prevents the network stack from falling back to direct connections with invalid or unavailable PAC script * ProxyServer, a URL of the proxy server * ProxyBypassList, a list of hosts for which the proxy will be bypassed

The ProxyServerMode field is deprecated in favor of the ProxyMode field.

For ProxyMode, if you choose the value: * direct, a proxy is never used and all other fields are ignored. * system, the systems's proxy is used and all other fields are ignored. * auto_detect, all other fields are ignored. * fixed_servers, the ProxyServer and ProxyBypassList fields are used. * pac_script, the ProxyPacUrl, ProxyPacMandatory and ProxyBypassList fields are used.

Note: For more detailed examples, visit The Chromium Projects ( https://go.microsoft.com/fwlink/?linkid=2094936).

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

Dictionary

Android:string

#### Android restriction name:

```
ProxySettings
```

##### Example value:

```
ProxySettings = {
 "ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/",
 "ProxyMode": "fixed_servers",
 "ProxyServer": "123.123.123.123:8080"
}
```

[Back to top](#microsoft-edge-mobile---policies)

## Password manager and protection policies

[Back to top](#microsoft-edge-mobile---policies)

### PasswordManagerEnabled

#### Enable saving passwords to the password manager

#### Supported on:

- Microsoft Edge (Android) since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

Setting the policy to Enabled means users have Microsoft Edge remember passwords and provide them the next time they sign in to a site.

Setting the policy to Disabled means users can't save new passwords, but previously saved passwords will still work.

If the policy is set, users can't change it in Microsoft Edge. If not set, the user can turn off password saving.

- true = Enable saving passwords using the password manager
- false = Disable saving passwords using the password manager

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes
- Can Be Recommended : Yes

#### Data Type:

Android:Boolean

iOS:Boolean

#### Android and iOS restriction name:

```
PasswordManagerEnabled
```

##### Example value (Android and iOS):

```
true
```
[Back to top](#microsoft-edge-mobile---policies)
<!-- ====================================== -->
## Idle browser actions

[Back to top](#microsoft-edge-mobile---policies)

### IdleTimeout

#### Delay before running idle actions

#### Supported on:

- Microsoft Edge (Android) since version 122
- Microsoft Edge (iOS and iPadOS) since version 122

#### Description

Triggers an action when the computer is idle.

If this policy is set, it specifies the length of time without user input (in minutes) before the browser runs actions configured via the IdleTimeoutActions policy.

If this policy is not set, no action will be ran.

The minimum threshold is 1 minute.

"User input" is defined by Operating System APIs, and includes things like moving the mouse or typing on the keyboard.

#### Supported features

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data type

Android:Integer

iOS:Integer

#### Android and iOS restriction name:

```
IdleTimeout
```
##### Example value (Android and iOS):

```
1
```

[Back to top](#microsoft-edge-mobile---policies)
<!-- ====================================== -->
###  IdleTimeoutActions

#### Actions to run when the computer is idle

#### Supported on:

- Microsoft Edge (Android) since version 122
- Microsoft Edge (iOS and iPadOS) since version 122

#### Description

List of actions to run when the timeout from the IdleTimeout policy is reached.

If the IdleTimeout policy is unset, this policy has no effect.

When the timeout from the IdleTimeout policy is reached, the browser runs the actions configured in this policy.

If this policy is empty or left unset, the IdleTimeout policy has no effect.

Supported actions are:

- 'close_tabs': close all open tabs and create a NTP (New Tab Page).
- 'clear_browsing_history': clear the browsing history.
- 'clear_cookies_and_other_site_data': clear browsing history and other site data.
- 'sign_out': Signs out the current signed in user. Only supported on iOS.

#### Supported features

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data type

Android: List of strings

iOS: List of strings

#### Android and iOS restriction name:

```
IdleTimeoutActions

```
##### Example value (Android):

```
[

"close_tabs",
"clear_browsing_history",
"clear_cookies_and_other_site_data"

]

```

##### Example value (iOS):

```
<array>

  <string>close_tabs</string>
  <string>clear_browsing_history</string>
  <string>clear_cookies_and_other_site_data</string>

</array>

```

[Back to top](#microsoft-edge-mobile---policies)
<!-- ====================================== -->
## Additional policies

[Back to top](#microsoft-edge-mobile---policies)

### URLAllowlist

#### Allow access to a list of URLs

#### Supported on:

- Microsoft Edge (Android) since version 109
- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

Setting the policy provides access to the listed URLs, as exceptions to URLBlocklist. See that policy's description for the format of entries of this list. For example, setting URLBlocklist to * will block all requests, and you can use this policy to allow access to a limited list of URLs. Use it to open exceptions to certain schemes, subdomains of other domains, ports, or specific paths, using the format specified at (https://go.microsoft.com/fwlink/?linkid=2095322 ). The most specific filter determines if a URL is blocked or allowed. The URLAllowlist policy takes precedence over URLBlocklist. This policy is limited to 1,000 entries.

This policy also allows enabling the automatic invocation by the browser of external application registered as protocol handlers for the listed protocols like "tel:" or "ssh:".

Leaving the policy unset allows no exceptions to URLBlocklist.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

List of strings

Android:String

iOS:String

#### Android and iOS restriction name:

```
URLAllowlist
```

##### Example value (Android):

```
[
 "example.com",
 https://ssl.server.com,
 "hosting.com/good_path",
 https://server:8080/path,
 ".exact.hostname.com"
]
```

##### Example value (iOS):

```
<array>
  <string>example.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```

[Back to top](#microsoft-edge-mobile---policies)

### URLBlocklist

#### Block access to a list of URLs

#### Supported on:

- Android System WebView since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

Setting the policy prevents webpages with prohibited URLs from loading. It provides a list of URL patterns that specify forbidden URLs. Leaving the policy unset means no URLs are prohibited in the browser. Format the URL pattern according to this format (https://go.microsoft.com/fwlink/?linkid=2095322 ). Up to 1,000 exceptions can be defined in URLAllowlist.

You can block javascript://* URLs. However, it affects only JavaScript entered in the address bar (or, for example, bookmarklets). In-page JavaScript URLs with dynamically loaded data aren't subject to this policy. For example, if you block example.com/abc, then example.com can still load example.com/abc using XMLHTTPRequest.

Note: Blocking internal edge://* can lead to unexpected errors or may be circumvented in special cases. Instead of blocking certain internal URLs, see if there are more specific policies available. 

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

List of strings

Android:String

iOS:String

#### Android and iOS restriction name:

```
URLBlocklist
```

##### Example value (Android)

```
[
 "example.com",
 https://ssl.server.com,
 "hosting.com/bad_path",
 https://server:8080/path,
 ".exact.hostname.com",
[ file://*]file://*,
 "custom_scheme:*",
 "*"
]
```

##### Example value (iOS)

```
<array>
  <string>example.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/bad_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
  <string>file://*</string>
  <string>custom_scheme:*</string>
  <string>*</string>
</array>
```

[Back to top](#microsoft-edge-mobile---policies)

### SSLErrorOverrideAllowed

#### Allow proceeding from the SSL warning page

#### Supported on:

- Microsoft Edge (Android) since version 109
- Microsoft Edge (iOS) since version 113

#### Description

Setting the policy to Enabled or leaving it unset lets users click through warning pages Microsoft Edge shows when users navigate to sites that have SSL errors.

Setting the policy to Disabled prevent users from clicking through any warning pages.

- true = Allow users to click through SSL warning pages
- false = Prevent users from clicking through SSL warning pages

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

Android:Boolean

iOS:Boolean

#### Android and iOS restriction name:

```
SSLErrorOverrideAllowed
```

##### Example value (Android and iOS):

```
true
```

[Back to top](#microsoft-edge-mobile---policies)

### CertificateTransparencyEnforcementDisabledForUrls

#### Disable Certificate Transparency enforcement for a list of URLs

#### Supported on:

- Microsoft Edge (Android) since version 109

#### Description

Setting the policy turns off Certificate Transparency disclosure requirements for the hostnames in the specified URLs. While making it harder to detect misissued certificates, hosts can keep using certificates that otherwise wouldn't be trusted (because they weren't properly publicly disclosed).

Leaving the policy unset means that if certificates requiring disclosure through Certificate Transparency aren't disclosed, then Microsoft Edge doesn't trust those certificates.

A URL pattern follows this format (https://go.microsoft.com/fwlink/?linkid=2095322 ). However, because the validity of certificates for a given hostname is independent of the scheme, port, or path, Microsoft Edge only considers the hostname portion of the URL. Wildcard hosts aren't supported.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

List of strings

Android:string

#### Android restriction name:

```
CertificateTransparencyEnforcementDisabledForUrls
```

##### Example value:

```
[
 "example.com",
 ".example.com"
]
```

[Back to top](#microsoft-edge-mobile---policies)

### CertificateTransparencyEnforcementDisabledForCas

#### Disable Certificate Transparency enforcement for a list of subjectPublicKeyInfo hashes

#### Supported on:

* Microsoft Edge (Android) since version 109

#### Description

Setting the policy turns off enforcement of Certificate Transparency disclosure requirements for a list of subjectPublicKeyInfo hashes. Enterprise hosts can keep using certificates that otherwise wouldn't be trusted (because they weren't properly publicly disclosed). To turn off enforcement, the hash must meet one of these conditions:

\* It's of the server certificate's subjectPublicKeyInfo.

\* It's of a subjectPublicKeyInfo that appears in a Certificate Authority (CA) certificate in the certificate chain. That CA certificate is constrained through the X.509v3 nameConstraints extension, one or more directoryName nameConstraints are present in the permittedSubtrees, and the directoryName has an organizationName attribute.

\* It's of a subjectPublicKeyInfo that appears in a CA certificate in the certificate chain, the CA certificate has one or more organizationName attributes in the certificate Subject, and the server's certificate has the same number of organizationName attributes, in the same order, and with byte-for-byte identical values.

Specify a subjectPublicKeyInfo hash by linking the hash algorithm name, a slash, and the Base64 encoding of that hash algorithm applied to the DER-encoded subjectPublicKeyInfo of the specified certificate. Base64 encoding format matches that of an SPKI Fingerprint. The only recognized hash algorithm is sha256; others are ignored.

Leaving the policy unset means that if certificates requiring disclosure through Certificate Transparency aren't disclosed, then Google Chrome doesn't trust those certificates.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

List of strings

Android:string

#### Android restriction name:

```
CertificateTransparencyEnforcementDisabledForCas
```

##### Example value:

```
[
 "sha256/AAAAAAAAAAAAAAAAAAAAAA==",
 "sha256//////////////////////w=="
]
```

[Back to top](#microsoft-edge-mobile---policies)

### SavingBrowserHistoryDisabled

#### Disable saving browser history

#### Supported on:

- Microsoft Edge (Android) since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

Setting the policy to Enabled means browsing history is not saved, tab syncing is off and users can't change this setting.

Setting the policy to Disabled or leaving it unset saves browsing history.

- true = Disable saving browser history
- false = Enable saving browser history

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

Android:Boolean

iOS:Boolean

#### Android and iOS restriction name:

```
SavingBrowserHistoryDisabled
```

##### Example value (Android and iOS):

```
true
```

[Back to top](#microsoft-edge-mobile---policies)

### SearchSuggestEnabled

#### Enable search suggestions

#### Supported on:

- Microsoft Edge (Android) since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

Setting the policy to True turns on search suggestions in Microsoft Edge's address bar. Setting the policy to False turns off these search suggestions.

Suggestions based on bookmarks or history are unaffected by the policy.

If you set the policy, users can't change it. If not set, search suggestions are on at first, but users can turn them off any time.

- true = Enable search suggestions
- false = Disable search suggestions

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes
- Can Be Recommended : Yes

#### Data Type:

Android:Boolean

iOS:Boolean

#### Android and iOS restriction name:

```
SearchSuggestEnabled
```

##### Example value (Android and iOS):

```
true
```

[Back to top](#microsoft-edge-mobile---policies)

### TranslateEnabled

#### Enable Translate

#### Supported on:

- Microsoft Edge (Android) since version 109

- Microsoft Edge (iOS and iPadOS) since version 109

#### Description

Setting the policy to True provides translation functionality when it's appropriate for users by showing an integrated translate toolbar in Microsoft Edge and a translate option on the right-click context menu. Setting the policy to False shuts off all built-in translate features.

If you set the policy, users can't change this function. Leaving it unset lets them change the setting.

- true = Always offer translation
- false = Never offer translation
- not set = Allow the user to decide

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes
- Can Be Recommended : Yes

#### Data Type:

Android:Boolean

iOS:Boolean

#### Android and iOS restriction name:

```
TranslateEnabled
```

##### Example value (Android and iOS):

```
true
```

[Back to top](#microsoft-edge-mobile---policies)

### InPrivateModeAvailability

#### InPrivate mode availability

#### Supported on:

- Microsoft Edge (Android) since version 116

- Microsoft Edge (iOS and iPadOS) since version 116

#### Description

Specifies whether the user may open pages in InPrivate mode in Microsoft Edge.

If 'Enabled' is selected or the policy is left unset, pages may be opened in InPrivate mode.

If 'Disabled' is selected, pages will not be opened in InPrivate mode.

If 'Forced' is selected, pages will be opened ONLY in InPrivate mode.

Note: On iOS, if the policy is changed during a session, it will only take effect on relaunch.

0 = InPrivate mode available
1 = InPrivate mode disabled
2 = InPrivate mode forced

#### Supported features:

- Dynamic Policy Refresh : Yes

- Per Profile : Yes

#### Data Type:

Android:Integer

iOS:Integer

[Back to top](#microsoft-edge-mobile---policies)


### SmartScreenEnabled

#### Configure Microsoft Defender SmartScreen

#### Supported on:

- Microsoft Edge (Android and iOS) since version 119

#### Description

This policy setting lets you configure whether to turn on Microsoft Defender SmartScreen. Microsoft Defender SmartScreen provides warning messages to help protect your users from potential phishing scams and malicious software. By default, Microsoft Defender SmartScreen is turned on.

If you enable this setting, Microsoft Defender SmartScreen is turned on.

If you disable this setting, Microsoft Defender SmartScreen is turned off.

If you don't configure this setting, users can choose whether to use Microsoft Defender SmartScreen

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

Android:Boolean
iOS: Boolean

[Back to top](#microsoft-edge-mobile---policies)

### MicrosoftRootStoreEnabled

#### Determines whether the Microsoft Root Store and built-in certificate verifier will be used to verify server certificates

#### Supported on:

Microsoft Edge (Android) since version 118

#### Description:

When this policy is set to enabled, Microsoft Edge will perform verification of server certificates using the built-in certificate verifier with the Microsoft Root Store as the source of public trust.

When this policy is set to disabled, Microsoft Edge will use the system certificate verifier and system root certificates.

When this policy is not set, the Microsoft Root Store or system provided roots may be used.

#### Supported features:

- Dynamic Policy Refresh : No
- Per Profile : No

#### Data Type:

Android:Boolean

#### Android restriction name:

MicrosoftRootStoreEnabled

##### Example value :

```
true

```

[Back to top](#microsoft-edge-mobile---policies)

### ManagedFavorites

#### Configure Favorites (bookmarks)

#### Supported on:

- Microsoft Edge (Android) since version 119
- Microsoft Edge (iOS and iPadOS) since version 119

#### Description:

Setting the policy sets up a list of bookmarks where each one is a dictionary with the keys "name" and "url".

These keys hold the bookmark's name and target. Admins can set up a subfolder by defining a bookmark without a "url" key, but with an additional "children" key. This key also has a list of bookmarks, some of which can also be folders. Microsoft Edge amends incomplete URLs as if they were submitted through the address bar. For example, "microsoft.com" becomes `https://microsoft.com/`.

Users can't change the folders the bookmarks are placed in (though they can hide it from the bookmark bar). The default folder name for managed bookmarks is "Managed bookmarks" but it can be changed by adding a new sub-dictionary to the policy with a single key named "toplevel_name" with the desired folder name as its value. Managed bookmarks are not synced to the user account and extensions can't modify them.

#### Supported features:

- Dynamic Policy Refresh : Yes

- Per Profile : Yes

#### Data Type:

Dictionary

#### Android and iOS restriction name:

```

ManagedFavorites

```

##### Example value (Android):

```

  [
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

##### Example value (iOS):
```xml

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

[Back to top](#microsoft-edge-mobile---policies)

### ExperimentationAndConfigurationServiceControl

#### Control communication with the Experimentation and Configuration Service

#### Supported on:

- Microsoft Edge (Android) since version 121

- Microsoft Edge (iOS and iPadOS) since version 121

#### Description

The Experimentation and Configuration Service is used to deploy Experimentation and Configuration payloads to the client.

Experimentation payload consists of a list of early in development features that Microsoft is enabling for testing and feedback.

Configuration payload consists of a list of recommended settings that Microsoft wants to deploy to optimize the user experience.

Configuration payload may also contain a list of actions to take on certain domains for compatibility reasons. For example, the browser may override the User Agent string on a website if that website is broken. Each of these actions is intended to be temporary while Microsoft tries to resolve the issue with the site owner.

If you set this policy to 'FullMode', the full payload is downloaded from the Experimentation and Configuration Service. This includes both the experimentation and configuration payloads.

If you set this policy to 'ConfigurationsOnlyMode', only the configuration payload is downloaded.

If you set this policy to 'RestrictedMode', the communication with the Experimentation and Configuration Service is stopped completely. Microsoft does not recommend this setting.

If you don't configure this policy on a managed device, the behavior on Beta and Stable channels is the same as the 'ConfigurationsOnlyMode'. On Canary and Dev channels the behavior is the same as 'FullMode'.

If you don't configure this policy on an unmanaged device, the behavior is the same as the 'FullMode'.

#### Policy options mapping:

- FullMode (2) = Retrieve configurations and experiments

- ConfigurationsOnlyMode (1) = Retrieve configurations only

- RestrictedMode (0) = Disable communication with the Experimentation and Configuration Service

Use the preceding information when configuring this policy.

#### Supported features:

- Dynamic Policy Refresh : Yes

- Per Profile : No

#### Data Type:

Android:Integer

iOS:Integer

#### Android and iOS restriction name:

```
ExperimentationAndConfigurationServiceControl
```

##### Example value (Android and iOS):

```
1
```

[Back to top](#microsoft-edge-mobile---policies)


### HideFirstRunExperience 

#### Hide the First-run experience

#### Supported on:

- Microsoft Edge (Android) since version 124
- Microsoft Edge (iOS and iPadOS) since version 124

#### Description

If you enable this policy, the First-run experience will not be shown to users when they run Microsoft Edge for the first time.
If you disable or don't configure this policy, the First-run experience will be shown.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

Android:Boolean

iOS:Boolean

####  Android and iOS restriction name:

HideFirstRunExperience 

##### Example value (Android and iOS):
```
true
```

  [Back to top](#microsoft-edge-mobile---policies)
  
### DefaultBrowserSettingEnabled
 
#### Set Microsoft Edge as default browser

#### Supported on:

- Microsoft Edge (Android) since version 124
- Microsoft Edge (iOS and iPadOS) since version 124

#### Description

If you set this policy to True, Microsoft Edge always checks whether it's the default browser on startup and, if possible, automatically registers itself.
If you set this policy to False, Microsoft Edge is stopped from ever checking if it's the default and turns user controls off for this option.
If you don't set this policy, Microsoft Edge lets users control whether it's the default and, if not, whether user notifications should appear.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

Android:Boolean

iOS:Boolean

#### Android and iOS restriction name:

DefaultBrowserSettingEnabled 

##### Example value (Android and iOS):
```
true
```

  [Back to top](#microsoft-edge-mobile---policies)
  
## Edge website typo protection

[Back to top](#microsoft-edge-mobile---policies)

### PreventTyposquattingPromptOverride

#### Prevent bypassing Edge Website Typo Protection prompts for sites

#### Supported on:

- Microsoft Edge (Android) since version 124

#### Description

This policy setting lets you decide whether users can override the Edge Website Typo Protection warnings about potential typosquatting websites.

If you enable this setting, users can't ignore Edge Website Typo Protection warnings and they are blocked from continuing to the site.

If you disable or don't configure this setting, users can ignore Edge Website Typo Protection warnings and continue to the site.

This will only take effect when TyposquattingCheckerEnabled policy is not set or set to enabled.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

Android:Boolean

#### Android restriction name:

```
PreventTyposquattingPromptOverride 
```

##### Example value (Android):

```
true
```

[Back to top](#microsoft-edge-mobile---policies)

### TyposquattingAllowListDomains

#### Configure the list of domains for which Edge Website Typo Protection won't trigger warnings

#### Supported on:

- Microsoft Edge (Android) since version 124
- Microsoft Edge (iOS and iPadOS) since version 124

#### Description

Configure the list of Edge Website Typo Protection trusted domains. This means: Edge Website Typo Protection won't check for potentially malicious typosquatting websites.

If you enable this policy, Edge Website Typo Protection trusts these domains. 
If you disable or don't set this policy, default Edge Website Typo Protection protection is applied to all resources.

This will only take effect when TyposquattingCheckerEnabled policy is not set or set to enabled.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

List of strings

#### Android and iOS restriction name:
```
TyposquattingAllowListDomains 
```

##### Example value (Android):
```
[
https://www.contoso.com,
"[*.] contoso.edu"
]
Example value (iOS):
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```


[Back to top](#microsoft-edge-mobile---policies)


## See also

- [Configuring Microsoft Edge](configure-microsoft-edge.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Microsoft Security Baselines Blog](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)