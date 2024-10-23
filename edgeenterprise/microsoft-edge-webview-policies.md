---
title: "Microsoft Edge WebView2 Policy Documentation"
ms.author: stmoody
author: dan-wesley
manager: venkatk
ms.date: 10/22/2024
audience: ITPro
ms.topic: reference
ms.service: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: generated
description: "Windows and Mac documentation for all policies supported by the Microsoft Edge WebView2"
---

# Microsoft Edge WebView2 - Policies

The latest version of Microsoft Edge WebView2 includes the following policies. You can use these policies to configure how Microsoft Edge WebView2 runs in your organization.

For information about an additional set of policies used to control how and when Microsoft Edge WebView2 is updated, check out [Microsoft Edge update policy reference](microsoft-edge-update-policies.md).


> [!NOTE]
> This article applies to Microsoft Edge version 87 or later.

## Available policies

These tables list all of the group policies available in this release of Microsoft Edge WebView2. Use the links in the table to get more details about specific policies.

- [Loader Override Settings](#loader-override-settings)
- [Network settings](#network-settings)
- [Additional](#additional)


### [*Loader Override Settings*](#loader-override-settings-policies)

|Policy Name|Caption|
|-|-|
|[BrowserExecutableFolder](#browserexecutablefolder)|Configure the location of the browser executable folder|
|[ChannelSearchKind](#channelsearchkind)|Configure the WebView2 release channel search kind|
|[ReleaseChannelPreference](#releasechannelpreference)|Set the release channel search order preference (deprecated)|
|[ReleaseChannels](#releasechannels)|Configure the WebView2 release channels|
### [*Network settings*](#network-settings-policies)

|Policy Name|Caption|
|-|-|
|[AccessControlAllowMethodsInCORSPreflightSpecConformant](#accesscontrolallowmethodsincorspreflightspecconformant)|Make Access-Control-Allow-Methods matching in CORS preflight spec conformant|
|[BlockTruncatedCookies](#blocktruncatedcookies)|Block truncated cookies|
|[ZstdContentEncodingEnabled](#zstdcontentencodingenabled)|Enable zstd content encoding support|
### [*Additional*](#additional-policies)

|Policy Name|Caption|
|-|-|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|Control communication with the Experimentation and Configuration Service|
|[ForcePermissionPolicyUnloadDefaultEnabled](#forcepermissionpolicyunloaddefaultenabled)|Controls whether unload event handlers can be disabled.|
|[HttpAllowlist](#httpallowlist)|HTTP Allowlist|
|[NewBaseUrlInheritanceBehaviorAllowed](#newbaseurlinheritancebehaviorallowed)|Allows enabling the feature NewBaseUrlInheritanceBehavior (deprecated)|
|[NewPDFReaderWebView2List](#newpdfreaderwebview2list)|Enable built-in PDF reader powered by Adobe Acrobat for WebView2|
|[RSAKeyUsageForLocalAnchorsEnabled](#rsakeyusageforlocalanchorsenabled)|Check RSA key usage for server certificates issued by local trust anchors (deprecated)|




  ## Loader Override Settings policies

  [Back to top](#microsoft-edge-webview2---policies)

  ### BrowserExecutableFolder

  #### Configure the location of the browser executable folder

  
  
  #### Supported versions:

  - On Windows since 87 or later

  #### Description

  This policy configures WebView2 applications to use the WebView2 Runtime in the specified path. The folder should contain the following files: msedgewebview2.exe, msedge.dll, and so on.

To set the value for the folder path, provide a Value name and Value pair. Set value name to the Application User Model ID or the executable file name. You can use the "*" wildcard as value name to apply to all applications.

  #### Supported features:

  - Can be mandatory: Yes
  - Can be recommended: No
  - Dynamic Policy Refresh: Yes

  #### Data Type:

  - List of strings

  #### Windows information and settings

  ##### Group Policy (ADMX) info

  - GP unique name: BrowserExecutableFolder
  - GP name: Configure the location of the browser executable folder
  - GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings
  - GP path (Recommended): N/A
  - GP ADMX file name: MSEdgeWebView2.admx

  ##### Windows Registry Settings

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder
  - Path (Recommended): N/A
  - Value Name: list of REG_SZ
  - Value Type: list of REG_SZ

  ##### Example value:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```

  

  [Back to top](#microsoft-edge-webview2---policies)

  ### ChannelSearchKind

  #### Configure the WebView2 release channel search kind

  
  
  #### Supported versions:

  - On Windows since 121 or later

  #### Description

  This policy configures the channel search kind for WebView2 applications. By default the channel search kind is 0, which is equivalent to the "Most Stable" search kind in the corresponding WebView2 API; This indicates that WebView2 environment creation should search for a release channel from the most to least stable: WebView2 Runtime, Beta, Dev, and Canary.

To reverse the default search order and use the "Least Stable" search kind, set this policy to 1.

To set the value for the channel search kind, provide a Value name and Value pair. Set value name to the Application User Model ID or the executable file name. You can use the "*" wildcard as value name to apply to all applications.

  #### Supported features:

  - Can be mandatory: Yes
  - Can be recommended: No
  - Dynamic Policy Refresh: Yes

  #### Data Type:

  - List of strings

  #### Windows information and settings

  ##### Group Policy (ADMX) info

  - GP unique name: ChannelSearchKind
  - GP name: Configure the WebView2 release channel search kind
  - GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings
  - GP path (Recommended): N/A
  - GP ADMX file name: MSEdgeWebView2.admx

  ##### Windows Registry Settings

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\ChannelSearchKind
  - Path (Recommended): N/A
  - Value Name: list of REG_SZ
  - Value Type: list of REG_SZ

  ##### Example value:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\ChannelSearchKind = "Name: WebView2APISample.exe, Value: 1"

```

  

  [Back to top](#microsoft-edge-webview2---policies)

  ### ReleaseChannelPreference

  #### Set the release channel search order preference (deprecated)

  >DEPRECATED: This policy is deprecated. It is currently supported but will become obsolete in a future release.
  
  #### Supported versions:

  - On Windows since 87 or later

  #### Description

  This policy is deprecated in favor of ChannelSearchKind, which has the same functionality, and will become obsolete in 124 release. The default channel search order is WebView2 Runtime, Beta, Dev, and Canary.

To reverse the default search order, set this policy to 1.

To set the value for the release channel preference, provide a Value name and Value pair. Set value name to the Application User Model ID or the executable file name. You can use the "*" wildcard as value name to apply to all applications.

  #### Supported features:

  - Can be mandatory: Yes
  - Can be recommended: No
  - Dynamic Policy Refresh: Yes

  #### Data Type:

  - List of strings

  #### Windows information and settings

  ##### Group Policy (ADMX) info

  - GP unique name: ReleaseChannelPreference
  - GP name: Set the release channel search order preference (deprecated)
  - GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings
  - GP path (Recommended): N/A
  - GP ADMX file name: MSEdgeWebView2.admx

  ##### Windows Registry Settings

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference
  - Path (Recommended): N/A
  - Value Name: list of REG_SZ
  - Value Type: list of REG_SZ

  ##### Example value:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference = "Name: *, Value: 1"

```

  

  [Back to top](#microsoft-edge-webview2---policies)

  ### ReleaseChannels

  #### Configure the WebView2 release channels

  
  
  #### Supported versions:

  - On Windows since 121 or later

  #### Description

  This policy configures the release channel options for WebView2 applications. To configure these options, set the value to a comma-separated string of integers, which map to the `COREWEBVIEW2_RELEASE_CHANNELS` values from the corresponding WebView2 API. These values are: WebView2 Runtime (0), Beta (1), Dev (2), and Canary (3). By default, environment creation searches for channels from most to least stable, using the first channel found on the device. When `ReleaseChannels` is provided, environment creation will only search for the channels specified in the set. For example, the values "0,2" and "2,0" indicate that environment creation should only search for Dev channel and the WebView2 Runtime, using the order indicated by `ChannelSearchKind`. Environment creation attempts to interpret each integer and treats any invalid entry as the Stable channel. Set `ChannelSearchKind` to reverse the search order so environment creation searches for least stable build first. If both `BrowserExecutableFolder` and `ReleaseChannels` are provided, the `BrowserExecutableFolder` takes precedence, regardless of whether the channel of `BrowserExecutableFolder` is included in the `ReleaseChannels`.

To set the value for release channels, provide a Value name and Value pair. Set the value name to the Application User Model ID or the executable file name. You can use the "*" wildcard as value name to apply to all applications.

  #### Supported features:

  - Can be mandatory: Yes
  - Can be recommended: No
  - Dynamic Policy Refresh: Yes

  #### Data Type:

  - List of strings

  #### Windows information and settings

  ##### Group Policy (ADMX) info

  - GP unique name: ReleaseChannels
  - GP name: Configure the WebView2 release channels
  - GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings
  - GP path (Recommended): N/A
  - GP ADMX file name: MSEdgeWebView2.admx

  ##### Windows Registry Settings

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannels
  - Path (Recommended): N/A
  - Value Name: list of REG_SZ
  - Value Type: list of REG_SZ

  ##### Example value:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannels = "Name: WebView2APISample.exe, Value: 0,1,2"

```

  

  [Back to top](#microsoft-edge-webview2---policies)

  ## Network settings policies

  [Back to top](#microsoft-edge-webview2---policies)

  ### AccessControlAllowMethodsInCORSPreflightSpecConformant

  #### Make Access-Control-Allow-Methods matching in CORS preflight spec conformant

  
  
  #### Supported versions:

  - On Windows since 123 or later

  #### Description

  This policy controls whether request methods are uppercased when matching with Access-Control-Allow-Methods response headers in CORS preflight.

If you disable this policy, request methods are uppercased. This is the behavior on or before Microsoft Edge 108.

If you enable or don't configure this policy, request methods are not uppercased, unless matching case-insensitively with DELETE, GET, HEAD, OPTIONS, POST, or PUT.

This would reject fetch(url, {method: 'Foo'}) + "Access-Control-Allow-Methods: FOO" response header,
and would accept fetch(url, {method: 'Foo'}) + "Access-Control-Allow-Methods: Foo" response header.

Note: request methods "post" and "put" are not affected, while "patch" is affected.

This policy is intended to be temporary and will be removed in the future.

  #### Supported features:

  - Can be mandatory: Yes
  - Can be recommended: No
  - Dynamic Policy Refresh: No - Requires browser restart

  #### Data Type:

  - Boolean

  #### Windows information and settings

  ##### Group Policy (ADMX) info

  - GP unique name: AccessControlAllowMethodsInCORSPreflightSpecConformant
  - GP name: Make Access-Control-Allow-Methods matching in CORS preflight spec conformant
  - GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Network settings
  - GP path (Recommended): N/A
  - GP ADMX file name: MSEdgeWebView2.admx

  ##### Windows Registry Settings

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2
  - Path (Recommended): N/A
  - Value Name: AccessControlAllowMethodsInCORSPreflightSpecConformant
  - Value Type: REG_DWORD

  ##### Example value:

```
0x00000001
```

  

  [Back to top](#microsoft-edge-webview2---policies)

  ### BlockTruncatedCookies

  #### Block truncated cookies

  
  
  #### Supported versions:

  - On Windows since 123 or later

  #### Description

  This policy provides a temporary opt-out for changes to how Microsoft Edge handles cookies set via JavaScript that contain certain control characters (NULL, carriage return, and line feed).
Previously, the presence of any of these characters in a cookie string would cause it to be truncated but still set.
Now, the presence of these characters will cause the whole cookie string to be ignored.

If you enable or don't configure this policy, the new behavior is enabled.

If you disable this policy, the old behavior is enabled.

  #### Supported features:

  - Can be mandatory: Yes
  - Can be recommended: No
  - Dynamic Policy Refresh: Yes

  #### Data Type:

  - Boolean

  #### Windows information and settings

  ##### Group Policy (ADMX) info

  - GP unique name: BlockTruncatedCookies
  - GP name: Block truncated cookies
  - GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Network settings
  - GP path (Recommended): N/A
  - GP ADMX file name: MSEdgeWebView2.admx

  ##### Windows Registry Settings

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2
  - Path (Recommended): N/A
  - Value Name: BlockTruncatedCookies
  - Value Type: REG_DWORD

  ##### Example value:

```
0x00000000
```

  

  [Back to top](#microsoft-edge-webview2---policies)

  ### ZstdContentEncodingEnabled

  #### Enable zstd content encoding support

  
  
  #### Supported versions:

  - On Windows since 125 or later

  #### Description

  This feature enables advertising "zstd" support in the Accept-Encoding request header and support for decompressing zstd web content.

If you enable or don't configure this policy, Microsoft Edge will accept server responses compressed with zstd.

If you disable this policy, the zstd content encoding feature will not be advertised or supported when processing server responses.

This policy is temporary and will be removed in the future.

  #### Supported features:

  - Can be mandatory: Yes
  - Can be recommended: No
  - Dynamic Policy Refresh: No - Requires browser restart

  #### Data Type:

  - Boolean

  #### Windows information and settings

  ##### Group Policy (ADMX) info

  - GP unique name: ZstdContentEncodingEnabled
  - GP name: Enable zstd content encoding support
  - GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Network settings
  - GP path (Recommended): N/A
  - GP ADMX file name: MSEdgeWebView2.admx

  ##### Windows Registry Settings

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2
  - Path (Recommended): N/A
  - Value Name: ZstdContentEncodingEnabled
  - Value Type: REG_DWORD

  ##### Example value:

```
0x00000001
```

  

  [Back to top](#microsoft-edge-webview2---policies)

  ## Additional policies

  [Back to top](#microsoft-edge-webview2---policies)

  ### ExperimentationAndConfigurationServiceControl

  #### Control communication with the Experimentation and Configuration Service

  
  
  #### Supported versions:

  - On Windows since 97 or later

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

Policy options mapping:

* FullMode (2) = Retrieve configurations and experiments

* ConfigurationsOnlyMode (1) = Retrieve configurations only

* RestrictedMode (0) = Disable communication with the Experimentation and Configuration Service

Use the preceding information when configuring this policy.

  #### Supported features:

  - Can be mandatory: Yes
  - Can be recommended: No
  - Dynamic Policy Refresh: Yes

  #### Data Type:

  - Integer

  #### Windows information and settings

  ##### Group Policy (ADMX) info

  - GP unique name: ExperimentationAndConfigurationServiceControl
  - GP name: Control communication with the Experimentation and Configuration Service
  - GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/
  - GP path (Recommended): N/A
  - GP ADMX file name: MSEdgeWebView2.admx

  ##### Windows Registry Settings

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2
  - Path (Recommended): N/A
  - Value Name: ExperimentationAndConfigurationServiceControl
  - Value Type: REG_DWORD

  ##### Example value:

```
0x00000002
```

  

  [Back to top](#microsoft-edge-webview2---policies)

  ### ForcePermissionPolicyUnloadDefaultEnabled

  #### Controls whether unload event handlers can be disabled.

  
  
  #### Supported versions:

  - On Windows since 118 or later

  #### Description

  unload event handlers are being deprecated. Whether they fire depends on the unload Permissions-Policy.
Currently, they are allowed by policy by default. In the future they will gradually move to being disallowed by default and sites must explicitly enable them using Permissions-Policy headers.
This enterprise policy can be used to opt out of this gradual deprecation by forcing the default to stay enabled.

Pages might depend on unload event handlers to save data or signal the end of a user session to the server.
This is not recommended because it's unreliable and impacts performance by blocking use of BackForwardCache.
Recommended alternatives exist, but the unload event has been used for a long time. Some applications might still rely on them.

If you disable this policy or don't configure it, unload event handlers will gradually be deprecated in-line with the deprecation rollout and sites which don't set Permissions-Policy header will stop firing `unload` events.

If you enable this policy then unload event handlers will continue to work by default.

  #### Supported features:

  - Can be mandatory: Yes
  - Can be recommended: No
  - Dynamic Policy Refresh: Yes

  #### Data Type:

  - Boolean

  #### Windows information and settings

  ##### Group Policy (ADMX) info

  - GP unique name: ForcePermissionPolicyUnloadDefaultEnabled
  - GP name: Controls whether unload event handlers can be disabled.
  - GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/
  - GP path (Recommended): N/A
  - GP ADMX file name: MSEdgeWebView2.admx

  ##### Windows Registry Settings

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2
  - Path (Recommended): N/A
  - Value Name: ForcePermissionPolicyUnloadDefaultEnabled
  - Value Type: REG_DWORD

  ##### Example value:

```
0x00000001
```

  

  [Back to top](#microsoft-edge-webview2---policies)

  ### HttpAllowlist

  #### HTTP Allowlist

  
  
  #### Supported versions:

  - On Windows since 123 or later

  #### Description

  Setting the policy specifies a list of hostnames or hostname patterns (such as '[\*.]example.com') that will not be upgraded to HTTPS and will not show an error interstitial if HTTPS-First Mode is enabled. Organizations can use this policy to maintain access to servers that do not support HTTPS, without needing to disable "AutomaticHttpsDefault".

Supplied hostnames must be canonicalized: Any IDNs must be converted to their A-label format, and all ASCII letters must be lowercase.

Blanket host wildcards (i.e., "*" or "[*]") are not allowed. Instead, HTTPS-First Mode and HTTPS Upgrades should be explicitly disabled via their specific policies.

Note: This policy does not apply to HSTS upgrades.

  #### Supported features:

  - Can be mandatory: Yes
  - Can be recommended: No
  - Dynamic Policy Refresh: Yes

  #### Data Type:

  - List of strings

  #### Windows information and settings

  ##### Group Policy (ADMX) info

  - GP unique name: HttpAllowlist
  - GP name: HTTP Allowlist
  - GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/
  - GP path (Recommended): N/A
  - GP ADMX file name: MSEdgeWebView2.admx

  ##### Windows Registry Settings

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\HttpAllowlist
  - Path (Recommended): N/A
  - Value Name: list of REG_SZ
  - Value Type: list of REG_SZ

  ##### Example value:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\HttpAllowlist = "testserver.example.com"
SOFTWARE\Policies\Microsoft\Edge\WebView2\HttpAllowlist = "[*.]example.org"

```

  

  [Back to top](#microsoft-edge-webview2---policies)

  ### NewBaseUrlInheritanceBehaviorAllowed

  #### Allows enabling the feature NewBaseUrlInheritanceBehavior (deprecated)

  >DEPRECATED: This policy is deprecated. It is currently supported but will become obsolete in a future release.
  
  #### Supported versions:

  - On Windows since 123 or later

  #### Description

  NewBaseUrlInheritanceBehavior is a Microsoft Edge feature that causes about:blank and about:srcdoc frames to consistently inherit their base url values via snapshots of their initiator's base url.

If you disable this policy, it prevents users or Microsoft Edge variations from enabling NewBaseUrlInheritanceBehavior, in case compatibility issues are discovered.

If you enable or don't configure this policy, it allows enabling NewBaseUrlInheritanceBehavior.

This policy is being deprecated because the feature NewBaseUrlInheritanceBehaviorAllowed has been removed.

This policy will be obsolete in release 133.

  #### Supported features:

  - Can be mandatory: Yes
  - Can be recommended: No
  - Dynamic Policy Refresh: Yes

  #### Data Type:

  - Boolean

  #### Windows information and settings

  ##### Group Policy (ADMX) info

  - GP unique name: NewBaseUrlInheritanceBehaviorAllowed
  - GP name: Allows enabling the feature NewBaseUrlInheritanceBehavior (deprecated)
  - GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/
  - GP path (Recommended): N/A
  - GP ADMX file name: MSEdgeWebView2.admx

  ##### Windows Registry Settings

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2
  - Path (Recommended): N/A
  - Value Name: NewBaseUrlInheritanceBehaviorAllowed
  - Value Type: REG_DWORD

  ##### Example value:

```
0x00000001
```

  

  [Back to top](#microsoft-edge-webview2---policies)

  ### NewPDFReaderWebView2List

  #### Enable built-in PDF reader powered by Adobe Acrobat for WebView2

  
  
  #### Supported versions:

  - On Windows since 116 or later

  #### Description

  This policy configures WebView2 applications to launch the new version of the PDF reader that's powered by Adobe Acrobat's PDF reader. The new PDF reader ensures that there's no loss of functionality and delivers an enhanced PDF experience. This experience includes richer rendering, improved performance, strong security for PDF file handling, and greater accessibility.

If this policy is specified for an application, it is possible that it may impact other related applications as well. The policy is applied to all WebView2s sharing the same WebView2 user data folder. These WebView2s could potentially belong to multiple applications if those applications, which are likely from the same product family, are designed to share the same user data folder.

Use a name-value pair to enable the new PDF reader for the application. Set the name to the Application User Model ID or the executable file name. You can use the "*" wildcard as value name to apply to all applications. Set the Value to true to enable the new reader or set it to false to use the existing one.

If you enable this policy for the specified WebView2 applications, they will use the new Adobe Acrobat powered PDF reader to open all PDF files.

If you disable the policy for the specified WebView2 applications or don't configure it, they will use the existing PDF reader to open all PDF files.

  #### Supported features:

  - Can be mandatory: Yes
  - Can be recommended: No
  - Dynamic Policy Refresh: No - Requires browser restart

  #### Data Type:

  - List of strings

  #### Windows information and settings

  ##### Group Policy (ADMX) info

  - GP unique name: NewPDFReaderWebView2List
  - GP name: Enable built-in PDF reader powered by Adobe Acrobat for WebView2
  - GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/
  - GP path (Recommended): N/A
  - GP ADMX file name: MSEdgeWebView2.admx

  ##### Windows Registry Settings

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\NewPDFReaderWebView2List
  - Path (Recommended): N/A
  - Value Name: list of REG_SZ
  - Value Type: list of REG_SZ

  ##### Example value:

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\NewPDFReaderWebView2List = {"name": "app1.exe", "value": true}
SOFTWARE\Policies\Microsoft\Edge\WebView2\NewPDFReaderWebView2List = {"name": "app_id_for_app2", "value": true}
SOFTWARE\Policies\Microsoft\Edge\WebView2\NewPDFReaderWebView2List = {"name": "*", "value": false}

```

  

  [Back to top](#microsoft-edge-webview2---policies)

  ### RSAKeyUsageForLocalAnchorsEnabled

  #### Check RSA key usage for server certificates issued by local trust anchors (deprecated)

  >DEPRECATED: This policy is deprecated. It is currently supported but will become obsolete in a future release.
  
  #### Supported versions:

  - On Windows since 123 or later

  #### Description

  This policy is deprecated because RSAKeyUsageForLocalAnchorsEnabled feature has been removed.

This policy will be removed in version 133.

The X.509 key usage extension declares how the key in a certificate can be
used. These instructions ensure certificates aren't used in an unintended
context, which protects against a class of cross-protocol attacks on HTTPS and
other protocols. HTTPS clients must verify that server certificates match the
connection's TLS parameters.

Starting in Microsoft Edge 124, this
check is always enabled.

Microsoft Edge 123 and earlier have the
following behavior:

If this policy is set to enabled,
Microsoft Edge will perform this key
check. This helps prevent attacks where an attacker manipulates the browser into
interpreting a key in ways that the certificate owner did not intend.

If this policy is set to disabled,
Microsoft Edge will skip this key check in
HTTPS connections that negotiate TLS 1.2 and use an RSA certificate that
chains to a local trust anchor. Examples of local trust anchors include
policy-provided or user-installed root certificates. In all other cases, the
check is performed independent of this policy's setting.

If this policy is not configured,
Microsoft Edge will behave as if the
policy is enabled.

This policy is available for administrators to preview the behavior of a
future release, which will enable this check by default. At that point, this
policy will remain temporarily available for administrators that need more
time to update their certificates to meet the new RSA key usage requirements.

Connections that fail this check will fail with the error
ERR_SSL_KEY_USAGE_INCOMPATIBLE. Sites that fail with this error likely have a
misconfigured certificate. Modern ECDHE_RSA cipher suites use the
"digitalSignature" key usage option, while legacy RSA decryption cipher suites
use the "keyEncipherment" key usage option. If uncertain, administrators should
include both in RSA certificates meant for HTTPS.

  #### Supported features:

  - Can be mandatory: Yes
  - Can be recommended: No
  - Dynamic Policy Refresh: Yes

  #### Data Type:

  - Boolean

  #### Windows information and settings

  ##### Group Policy (ADMX) info

  - GP unique name: RSAKeyUsageForLocalAnchorsEnabled
  - GP name: Check RSA key usage for server certificates issued by local trust anchors (deprecated)
  - GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/
  - GP path (Recommended): N/A
  - GP ADMX file name: MSEdgeWebView2.admx

  ##### Windows Registry Settings

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2
  - Path (Recommended): N/A
  - Value Name: RSAKeyUsageForLocalAnchorsEnabled
  - Value Type: REG_DWORD

  ##### Example value:

```
0x00000001
```

  

  [Back to top](#microsoft-edge-webview2---policies)


## See also

- [Configuring Microsoft Edge](configure-microsoft-edge.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Microsoft Security Baselines Blog](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)