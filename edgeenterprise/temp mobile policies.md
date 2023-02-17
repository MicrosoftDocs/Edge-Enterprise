---
title: "Microsoft Edge Mobile Policy Documentation"
ms.author: stmoody
author: dan-wesley
manager: venkatk
ms.date: 02/15/2023
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

[Edge specific](#edge-specific)
[Proxy server](#proxy-server)
[HTTP authentication](#http-authentication)
[Content settings](#content-settings)
[Default search provider](#default-search-provider)
[Password manager and protection](#password-manager-and-protection)
[Additional](#additional)

### [*Edge specific*](#edge-specific)

|Policy Name|Caption|
|:-|-|
| [EdgeNewTabPageCustomURL](#edgenewtabpagecustomurl) | Homepage instead of New Tab Page experience |
| [EdgeMyApps](#edgemyapps) | My Apps bookmark  |
| [EdgeDefaultHTTPS](#edgedefaulthttps) |  Default protocol handler |
| [EdgeDisableShareUsageData](#edgedisableshareusagedata) |  Disable data sharing usage data for personalization   |
| [EdgeDisableShareBrowsingHistory](#edgedisablesharebrowsinghistory)  |   Disable data sharing browsing history for personalization   |
| [EdgeDisabledFeatures](#edgedisabledfeatures)  |   Disable specific features  |
| [EdgeEnableKioskMode](#edgeenablekioskmode)  |  Kiosk mode experiences on Android devices   |
| [EdgeShowAddressBarInKioskMode](#edgeshowaddressbarinkioskmode)   |   Kiosk mode address bar experiences on Android devices  |
| [EdgeShowBottomBarInKioskMode](#edgeshowbottombarinkioskmode)   |   Kiosk mode bottom bar experiences on Android devices   |
| [EdgeSyncDisabled](#edgesyncdisabled)  |   Manage account synchronization  |
| [EdgeNetworkStackPref](#edgenetworkstackpref)   |   Switch network stack between Chromium and iOS  |

### [*Proxy server*](#proxy-server)

|Policy Name|Caption|
|:-|-|
| [ProxySettings](#proxysettings) | Proxy settings   |

### [*HTTP authentication*](#http-authentication)

|Policy Name|Caption|
|:-|-|
| [NtlmV2Enabled](#ntlmv2enabled)  | Enable NTLMv2 authentication    |
| [AuthSchemes](#authschemes)  |  Supported authentication schemes   |
| [DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)   |  Disable CNAME lookup when negotiating Kerberos authentication   |
| [AuthServerAllowlist](#authserverallowlist)  |  Authentication server allowlist   |
| [AuthAndroidNegotiateAccountType](#authandroidnegotiateaccounttype) |  Account type for HTTP Negotiate authentication   |
| [AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)  |  Kerberos delegation server allowlist   |

### NtlmV2Enabled

#### Enable NTLMv2 authentication

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

[Back to top](#microsoft-edge-mobile---policies)

### [*Content settings*](#content-settings)

|Policy Name|Caption|
|:-|-|
| [DefaultPopupsSetting]()   |     |
| [DefaultCookiesSetting]()   |     |
| [CookiesAllowedForUrls]()   |     |
| [CookiesBlockedForUrls]()   |     |
| [CookiesSessionOnlyForUrls]()   |     |
| []()   |     |
| []()   |     |

### [*Default search provider*](#default-search-provider)

|Policy Name|Caption|
|:-|-|
| [DefaultSearchProviderEnabled]()   |     |
| [DefaultSearchProviderName]()   |     |
| [DefaultSearchProviderSearchURL]()   |     |
| [DefaultSearchProviderSearchURLPostParams]()   |     |
| [DefaultSearchProviderAlternateURLs]()   |     |
| [DefaultSearchProviderEncodings]()   |     |
| [DefaultSearchProviderImageURL]()   |     |
| [DefaultSearchProviderImageURLPostParams]()   |     |
| [DefaultSearchProviderKeyword]()   |     |
| [DefaultSearchProviderNewTabURL]()   |     |
| [DefaultSearchProviderSuggestURL]()   |     |
| [DefaultSearchProviderSuggestURLPostParams]()   |     |

### [*Password manager and protection*](#password-manager-and-protection)

|Policy Name|Caption|
|:-|-|
| [PasswordManagerEnabled](#passwordmanagerenabled) | Enable saving passwords to the password manager |

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

## Edge specific policies

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

String

Android:choice

#### Android restriction name:

```
EdgeNewTabPageCustomURL
```

##### Example value:

```
https://www.bing.com
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

Boolean

Android:choice

#### Android restriction name:

```
EdgeDisableShareUsageData
```

##### Example value:

```
true
```

[Back to top](#microsoft-edge-mobile---policies)


## Proxy server policies

[Back to top](#microsoft-edge-mobile---policies)


### EdgeDisableShareBrowsingHistory

#### Disable data sharing browsing history for personalization

#### Supported on:

* Microsoft Edge (Android) since version 111

* Microsoft Edge (iOS and iPadOS) since version 111

#### Description

By default, Edge for iOS and Android prompts users for sharing browsing history to personalize their browsing experience. Organizations can disable this data sharing


EdgeDisableShareBrowsingHistory:
- true = Disables this prompt from displaying to end users
- false (Default) =  Users are prompted to share browsing history data

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : Yes

#### Data Type:

Boolean

Android:choice

#### Android restriction name:

```
EdgeDisableShareUsageData
```

##### Example value:

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

To disable multiple features, separate values with |. For example, inprivate|password disables both InPrivate and password storage.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

String

Android:string

#### Android restriction name:

```
EdgeDisabledFeatures
```

##### Example value:

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

For more information see [Microsoft Edge Sync](https://learn.microsoft.com/en-us/DeployEdge/microsoft-edge-enterprise-sync).

Organizations have the capability to disable Edge sync on iOS and Android.

#### Supported features:

- Dynamic Policy Refresh : Yes
- Per Profile : No

#### Data Type:

Boolean

Android:choice

#### Android restriction name:

```
EdgeSyncDisabled
```

##### Example value:

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

[Back to top](#microsoft-edge-mobile---policies)

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


## HTTP authentication policiesZZ

[Back to top](#microsoft-edge-mobile---policies)

## Content settings policiesZZ

[Back to top](#microsoft-edge-mobile---policies)

## Default search provider policiesZZ

[Back to top](#microsoft-edge-mobile---policies)

## Password manager and protection policies

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

## Additional policiesZZ

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
