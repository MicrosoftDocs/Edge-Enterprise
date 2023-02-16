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
| [EdgeNewTabPageCustomURL]() |  |
| [EdgeMyApps]() |   |
| [EdgeDefaultHTTPS]() |   |
| [EdgeDisableShareUsageData]() |     |
| [EdgeDisableShareBrowsingHistory]()  |     |
| [EdgeDisabledFeatures]()  |     |
| [EdgeEnableKioskMode]()  |     |
| [EdgeShowAddressBarInKioskMode]()   |     |
| [EdgeShowBottomBarInKioskMode]()   |     |
| [EdgeSyncDisabled]()  |     |
| [EdgeNetworkStackPref]()   |     |


### [*Proxy server*](#proxy-server)

|Policy Name|Caption|
|:-|-|
| [ProxySettings]() |    |

### [*HTTP authentication*](#http-authentication)

|Policy Name|Caption|
|:-|-|
| [-NtlmV2Enabled]()   |     |
| [AuthSchemes]()   |     |
| [DisableAuthNegotiateCnameLookup]()   |     |
| [AuthServerAllowlist]()   |     |
| [AuthAndroidNegotiateAccountType]()   |     |
| [AuthNegotiateDelegateAllowlist]()   |     |
| []()   |     |


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

[Back to top](#microsoft-edge-mobile---policies)

## Proxy server policies

[Back to top](#microsoft-edge-mobile---policies)

## HTTP authentication policies

[Back to top](#microsoft-edge-mobile---policies)

## Content settings policies

[Back to top](#microsoft-edge-mobile---policies)

## Default search provider policies

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
