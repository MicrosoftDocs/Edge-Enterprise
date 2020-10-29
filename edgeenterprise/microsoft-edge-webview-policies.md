---
title: "Microsoft Edge WebView2 Policy Documentation"
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 10/28/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom:
description: "Windows and Mac documentation for all policies supported by the Microsoft Edge Browser"
---

# Microsoft Edge WebView2 - Policies

The latest version of Microsoft Edge WebView2 includes the following policies. You can use these policies to configure how Microsoft Edge WebView2 runs in your organization.

For information about an additional set of policies used to control how and when Microsoft Edge WebView2 is updated, check out [Microsoft Edge update policy reference](microsoft-edge-update-policies.md).


> [!NOTE]
> This article applies to Microsoft Edge version 87 or later.

## Available policies

These tables list all of the group policies available in this release of Microsoft Edge WebView2. Use the links in the table to get more details about specific policies.

|||
|-|-|
|[Loader Override Settings](#loader-override-settings)|

### [*Loader Override Settings*](#loader-override-settings-policies)

|Policy Name|Caption|
|-|-|
|[BrowserExecutableFolder](#browserexecutablefolder)|Configure the location of the browser executable folder|
|[ReleaseChannelPreference](#releasechannelpreference)|Set the release channel search order preference|




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

  ### ReleaseChannelPreference

  #### Set the release channel search order preference

  
  
  #### Supported versions:

  - On Windows since 87 or later

  #### Description

  The default channel search order is WebView2 Runtime, Beta, Dev, and Canary.

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
  - GP name: Set the release channel search order preference
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


## See also

- [Configuring Microsoft Edge](configure-microsoft-edge.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Microsoft Security Baselines Blog](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)