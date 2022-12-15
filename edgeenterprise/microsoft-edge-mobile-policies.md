---
title: "Microsoft Edge Mobile Policy Documentation"
ms.author: stmoody
author: dan-wesley
manager: venkatk
ms.date: 12/14/2022
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: 
description: "Windows and Mac documentation for all policies supported by the Microsoft Edge Browser"
---

# Microsoft Edge Mobile - Policies

The latest version of Microsoft Edge includes the following policies. You can use these policies to configure how Microsoft Edge mobile runs in your organization.

## Available policies

These tables list all of the browser-related policies available in this release of Microsoft Edge. Use the links in the table to get more details about specific policies.

- [PasswordManagerEnabled](#PasswordManagerEnabled)
- [DefaultPopupsSetting](#DefaultPopupsSetting)
- [URLAllowlist](#URLAllowlist)
- [URLBlocklist](#URLBlocklist)
- [SSLErrorOverrideAllowed](#SSLErrorOverrideAllowed)
- [CertificateTransparencyEnforcementDisabledForUrls](#CertificateTransparencyEnforcementDisabledForUrls)
- [NtlmV2Enabled](#NtlmV2Enabled)
- [AuthSchemes](#AuthSchemes)
- [DisableAuthNegotiateCnameLookup](#DisableAuthNegotiateCnameLookup)
- [AuthServerAllowlist](#AuthServerAllowlist)
- [AuthAndroidNegotiateAccountType](#AuthAndroidNegotiateAccountType)
- [AuthNegotiateDelegateAllowlist](#AuthNegotiateDelegateAllowlist)
- [ProxySettings](#ProxySettings)
- [DefaultSearchProviderEnabled](#DefaultSearchProviderEnabled)
- [DefaultSearchProviderName](#DefaultSearchProviderName)
- [DefaultSearchProviderSearchURL](#DefaultSearchProviderSearchURL)
- [DefaultSearchProviderSearchURLPostParams](#DefaultSearchProviderSearchURLPostParams)
- [DefaultSearchProviderAlternateURLs](#DefaultSearchProviderAlternateURLs)
- [DefaultSearchProviderEncodings](#DefaultSearchProviderEncodings)
- [DefaultSearchProviderImageURL](#DefaultSearchProviderImageURL)
- [DefaultSearchProviderImageURLPostParams](#DefaultSearchProviderImageURLPostParams)
- [DefaultSearchProviderKeyword](#DefaultSearchProviderKeyword)
- [DefaultSearchProviderNewTabURL](#DefaultSearchProviderNewTabURL)
- [DefaultSearchProviderSuggestURL](#DefaultSearchProviderSuggestURL)
- [DefaultSearchProviderSuggestURLPostParams](#DefaultSearchProviderSuggestURLPostParams)
- [SavingBrowserHistoryDisabled](#SavingBrowserHistoryDisabled)
- [SearchSuggestEnabled](#SearchSuggestEnabled)
- [TranslateEnabled](#TranslateEnabled)
- [DefaultCookiesSetting](#DefaultCookiesSetting)
- [CookiesAllowedForUrls](#CookiesAllowedForUrls)
- [CookiesBlockedForUrls](#CookiesBlockedForUrls)
- [CookiesSessionOnlyForUrls](#CookiesSessionOnlyForUrls)

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

Boolean

Android:choice

#### Android restriction name:

```
PasswordManagerEnabled
```

##### Example value:

```
true
```

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

Integer

Android:choice

#### Android restriction name:

```
DefaultPopupsSetting
```

##### Example value:

```
1
```

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

Android:string

#### Android restriction name:

```
URLAllowlist
```

##### Example value (Android):

```
[
 "example.com",
 "https://ssl.server.com",
 "hosting.com/good_path",
 "https://server:8080/path",
 ".exact.hostname.com"
]
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

Android:string

#### Android restriction name:

```
URLBlocklist
```

##### Example value:

```
[
 "example.com",
 "https://ssl.server.com",
 "hosting.com/bad_path",
 "https://server:8080/path",
 ".exact.hostname.com",
 "file://*",
 "custom_scheme:*",
 "*"
]
```

[Back to top](#microsoft-edge-mobile---policies)

### SSLErrorOverrideAllowed

#### Allow proceeding from the SSL warning page

#### Supported on:

- Microsoft Edge (Android) since version 109

#### Description

Setting the policy to Enabled or leaving it unset lets users click through warning pages Microsoft Edge shows when users navigate to sites that have SSL errors.

Setting the policy to Disabled prevent users from clicking through any warning pages.

- true = Allow users to click through SSL warning pages
- false = Prevent users from clicking through SSL warning pages

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

Boolean

Android:choice

#### Android restriction name:

```
SSLErrorOverrideAllowed
```

##### Example value:

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

### NtlmV2Enabled

#### Enable NTLMv2 authentication.

#### Supported on:

- Microsoft Edge (Android) since version 109

#### Description

Setting the policy to Enabled or leaving it unset turns NTLMv2 on.

Setting the policy to Disabled turns NTLMv2 off.

All recent versions of Samba and Microsoft® Windows® servers support NTLMv2. This should only be turned off for backward compatibility as it reduces the security of authentication.

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

- Microsoft Edge (Android) since version 109

- Android System WebView since version 109

#### Description

Setting the policy specifies the type of accounts provided by the Android authentication app that supports HTTP Negotiate authentication (such as Kerberos authentication). This information should be available from the supplier of the authentication app. For details, see The Chromium Projects ( https://goo.gl/hajyfN )

Leaving the policy unset turns off HTTP Negotiate authentication on Android.

#### Supported features:

- Dynamic Policy Refresh : No
- Per Profile : No

#### Data Type:

String

Android:choice

#### Android restriction name:

```
AuthAndroidNegotiateAccountType
```

##### Example value:

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



### ProxySettings

#### Proxy settings

#### Supported on:

- Microsoft Edge (Android) since version 109

#### Description

Setting the policy configures the proxy settings for Chrome and ARC-apps, which ignore all proxy-related options specified from the command line.

Leaving the policy unset lets users choose their proxy settings.

Setting the ProxySettings policy accepts the following fields: * ProxyMode, which lets you specify the proxy server Chrome uses and prevents users from changing proxy settings * ProxyPacUrl, a URL to a proxy .pac file * ProxyPacMandatory, which prevents the network stack from falling back to direct connections with invalid or unavailable PAC script * ProxyServer, a URL of the proxy server * ProxyBypassList, a list of hosts for which the proxy will be bypassed

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

Boolean

Android:choice

#### Android restriction name:

```
DefaultSearchProviderEnabled
```

##### Example value:

```
true
```



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

String

Android:choice

#### Android restriction name:

```
DefaultSearchProviderName
```

##### Example value:

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

String

Android:choice

#### Android restriction name:

```
DefaultSearchProviderSearchURL
```

##### Example value:

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

String

Android:choice

#### Android restriction name:

```
DefaultSearchProviderSearchURLPostParams
```

##### Example value:

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

#### Android restriction name:

```
DefaultSearchProviderAlternateURLs
```

##### Example value:

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

#### Android restriction name:

```
DefaultSearchProviderEncodings
```

##### Example value:

```
[
 "UTF-8",
 "UTF-16",
 "GB2312",
 "ISO-8859-1"
]
```

[Back to top](#microsoft-edge-mobile---policies)

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

String

Android:choice

#### Android restriction name:

```
DefaultSearchProviderImageURL
```

##### Example value:

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

String

Android:choice

#### Android restriction name:

```
DefaultSearchProviderImageURLPostParams
```

##### Example value:

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

String

Android:choice

#### Android restriction name:

```
DefaultSearchProviderKeyword
```

##### Example value:

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

String

Android:choice

#### Android restriction name:

```
DefaultSearchProviderNewTabURL
```

##### Example value:

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

String

Android:choice

#### Android restriction name:

```
DefaultSearchProviderSuggestURL
```

##### Example value:

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

String

Android:choice

#### Android restriction name:

```
DefaultSearchProviderSuggestURLPostParams
```

##### Example value:

```
q={searchTerms},ie=utf-8,oe=utf-8
```



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

Boolean

Android:choice

#### Android restriction name:

```
SavingBrowserHistoryDisabled
```

##### Example value:

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

Boolean

Android:choice

#### Android restriction name:

```
SearchSuggestEnabled
```

##### Example value:

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

Boolean

Android:choice

#### Android restriction name:

```
TranslateEnabled
```

##### Example value:

```
true
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

## See also

- [Configuring Microsoft Edge](configure-microsoft-edge.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Microsoft Security Baselines Blog](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)