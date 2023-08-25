---
title: "Microsoft Edge WebView2 Policy Documentation"
ms.author: stmoody
author: dan-wesley
manager: venkatk
ms.date: 08/25/2023
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: generated
description: "Windows and Mac documentation for all policies supported by the Microsoft Edge Browser"
---

# Microsoft Edge WebView2 - Policies

The latest version of Microsoft Edge WebView2 includes the following policies. You can use these policies to configure how Microsoft Edge WebView2 runs in your organization.

For information about an additional set of policies used to control how and when Microsoft Edge WebView2 is updated, check out [Microsoft Edge update policy reference](microsoft-edge-update-policies.md).


> [!NOTE]
> This article applies to Microsoft Edge version 87 or later.

## Available policies

These tables list all of the group policies available in this release of Microsoft Edge WebView2. Use the links in the table to get more details about specific policies.

- [Loader Override Settings](#loader-override-settings)
- [Additional](#additional)


### [*Loader Override Settings*](#loader-override-settings-policies)

|Policy Name|Caption|
|-|-|
|[BrowserExecutableFolder](#browserexecutablefolder)|Configure the location of the browser executable folder|
|[ReleaseChannelPreference](#releasechannelpreference)|Set the release channel search order preference|
### [*Additional*](#additional-policies)

|Policy Name|Caption|
|-|-|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|Control communication with the Experimentation and Configuration Service|
|[NewPDFReaderWebView2List](#newpdfreaderwebview2list)|Enable built-in PDF reader powered by Adobe Acrobat for WebView2|




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


## See also

- [Configuring Microsoft Edge](configure-microsoft-edge.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Microsoft Security Baselines Blog](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)