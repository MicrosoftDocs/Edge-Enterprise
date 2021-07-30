---
title: "Detailed guide to the ExtensionSettings policy"
ms.author: aspoddar
author: dan-wesley
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "A detailed reference guide for configuring Microsoft Edge extensions using the ExtensionSettings policy."
---

# Detailed guide to the ExtensionSettings policy

Microsoft Edge offers multiple ways to manage extensions. A common way is to set multiple policies in one place with a JSON string in the Windows Group Policy Editor or in the Windows Registry using the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) policy.

> [!NOTE]
> This article applies to Microsoft Edge version 77 or later.

## Before you begin

You decide if you want to set all extension management settings here or set these controls through other policies.
  
The ExtensionSettings policy can overwrite other policies that you've set elsewhere in group policy, including the following policies:

- [ExtensionAllowedTypes](/DeployEdge/microsoft-edge-policies#extensionallowedtypes)
- [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist)
- [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)
- [ExtensionInstallSources](/DeployEdge/microsoft-edge-policies#extensioninstallsources)
- [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallsources)

## ExtensionSettings policy fields

This policy can control settings such as Update URL, where the extension will be downloaded from for initial install, and Blocked permissions, or which permissions aren't allowed to run. The available policy fields are described in the following table.

| &nbsp; | Description |
|--|--|
| **allowed_types** | Can only be used to configure the default configuration, *. Specifies what types of app or extension users are allowed to install on Microsoft Edge. The value is a list of strings, each of which should be one of the following types: "extension", "theme", "user_script", and "hosted_app"   |
| **blocked_install_message**| If you block users from installing certain extensions, you can specify a custom message to display in the browser if users try to install them.<br>Append text to the generic error message that is displayed on the Microsoft Edge Add-ons website. For example, you can tell users how to contact their IT department or why a particular extension is unavailable. The message can be up to 1,000 characters long.   |
|**blocked_permissions**  | Prevents users from installing and running extensions that request certain API permissions that your organization doesn’t allow. For example, you can block extensions that access cookies. If an extension requires a permission that you blocked, the user can’t install it. If users previously installed the extension, it will no longer load. If an extension contains a blocked permission as an optional requirement, it installs as usual. Then, while the extension is running, blocked permissions are automatically declined.<br>For a list of available permissions, see [declare permissions](/microsoft-edge/extensions-chromium/enterprise/declare-permissions).   |
| **installation_mode**| Controls if and how extensions that you specify are added to Microsoft Edge. You can set the installation mode to one of the following options:<br>- allowed: Users can install the extension. If no installation mode is defined, this setting is the default.<br>- blocked: Users can’t install the extension.<br>- force_installed: Automatically install the extension without user interaction. Users can’t remove it. You also need to define the extension download location using update_url. **Note**: You can’t use this setting with * because Microsoft Edge wouldn't know which extension to automatically install.<br>- normal_installed: Automatically install the extension without user interaction. Users can disable it. You also need to define the extension download location using update_url. **Note**: You can’t use this setting with * because Microsoft Edge wouldn't know which extension to automatically install.<br>- removed: Users can’t install the extension. If users previously installed the extension, Microsoft Edge removes it. |  |
| **install_sources** | Can be used only to configure the default configuration, *. Specifies which URLs are allowed to install extensions. Both the location of the *.crx file and the page where the download is started from (the referrer) must be allowed by these patterns. For URL pattern examples, see the [match patterns](/microsoft-edge/extensions-chromium/enterprise/match-patterns).  |
| **minimum_version_required** |Microsoft Edge disables extensions, including force-installed extensions, with a version older than the specified minimum version.<br>The format of the version string is the same as the one used in the extension manifest.     |
| **update_url** | Only applies to force_installed and normal_installed. Specifies where Microsoft Edge should download an extension from. If the extension is hosted in the Microsoft Edge Add-ons website, use this location: `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.<br>Microsoft Edge uses the URL that you specify for the initial extension installation. For subsequent extension updates, Microsoft Edge uses the URL in the extension's manifest.   |
| **runtime_allowed_hosts**| Allows extensions to interact with specified websites, even if they’re also defined in runtime_blocked_hosts. You can specify up to 100 entries. Extra entries are discarded.<br>The host pattern format is similar to [match patterns](/microsoft-edge/extensions-chromium/enterprise/match-patterns) except you can’t define the path. For example:<br>- *://*.example.com<br>- *://example.*—eTLD wildcards are supported     |
| **runtime_blocked_hosts**| Prevent extensions from interacting with or modifying websites that you specify. Modifications include blocking JavaScript injection, cookie access, and web-request modifications.<br>You can specify up to 100 entries. Extra entries are discarded.<br>The host pattern format is similar to match patterns except you can’t define the path. For example:<br>- *://*.example.com<br>- *://example.*—eTLD wildcards are supported   |
| **override_update_url**| Available from Edge 93<br>If this is set to `true`, Edge uses the update URL specified in the ExtensionSettings policy or in the ExtensionInstallForcelist policy, for subsequent extension updates.<br>If this is not set or is set to `false`, Edge uses the URL specified in the extension's manifest for updates.|
| **toolbar_state**| Available from Edge 93<br>This policy setting allows you to force show an installed extension to the toolbar. The default state is `default_shown` for all extensions. Following states are possible for this setting<br>-`force_shown`: You can choose to force show an installed extension on the toolbar. Users will not be able to hide the specificed extension icon from the toolbar.<br>-`default_hidden`: You can choose to change the default setting for an extension's state on the toolbar as hidden.<br>-`default_shown`: This is the deafult setting of all the installed extensions on the browser.

## Configure using a JSON string in Windows Group Policy Editor

The steps to use the extension settings policy using GPO assume that you've already imported the ADM/ADMX for Microsoft Edge Policies.

1. Open the group policy editor and go to go to **Microsoft Edge > Extensions > Configure extension management setting policy**.
2. Enable the policy and enter its compact JavaScript Object Notation (JSON) data in the text box as a single line with no line breaks.
3. To validate the policy and compact it into a single line, use a JSON compression tool.

### Properly format JSON for the extension settings policy

You need to understand the two parts to this policy — the default scope and the individual scope. The default scope is a catch-all for extensions without their own scope. The individual scope is applied to that extension only.  

The default scope is identified by the asterisk (*). The next example defines a default scope and an individual extension scope.

```json
{ 
   “*”: {}, 
   “nckgahadagoaajjgafhacjanaoiihapd”: {} 
} 
```

An extension will only get its settings from one scope. If there’s an individual extension scope for that extension, those will be the settings that apply to that extension. If no individual extension scope exists, then the extension will use the default scope.  

The next JSON example blocks any extension from running on `.example.com` and blocks any extension that requires the permission "USB".

```json
{ 
  "*": { 
    "runtime_blocked_hosts": ["*://*.example.com"], 
    "blocked_permissions": ["usb"] 
  } 
} 
```

**Compact JSON**

```json
{"*":{"runtime_blocked_hosts":["*://*.example.com"],"blocked_permissions":["usb"]}} 
```

### A few more JSON examples for extension settings

#### Using installation_mode property to allow and block extensions

- User can install all extensions - this is the default setting 

  `{ "*": {"installation_mode": "allowed" }}`
- User can’t install any extensions.  

  `{ "*": {"installation_mode": "blocked" }}`

- Specify a custom message to display when installation is blocked.

   `{"*": {"blocked_install_message": ["Call IT(408 - 555 - 1234) for an exception"]}}`

#### Using installation_mode property to force install extensions

When using installation_mode as "force_installed", the extension is automatically installed without user interaction. A user can’t disable or remove the extension. If an extension is "normal" or "force" installed, the **update_url** field must also be defined. This field points to the location where the extension can be installed from. Use the following locations for the **update_url** field:

- If the extension you’re downloading is hosted on the Microsoft Edge Add-ons store, use [https://edge.microsoft.com/extensionwebstorebase/v1/crx](https://edge.microsoft.com/extensionwebstorebase/v1/crx).
- If the extension you’re downloading is hosted on the Chrome Web Store, use [https://clients2.google.com/service/update2/crx](https://clients2.google.com/service/update2/crx).
- If you’re hosting the extension on your own server, use the URL where Microsoft Edge can download the packed extension (.crx file). JSON example:

   `{"nckgahadagoaajjgafhacjanaoiihapd": {"installation_mode": "force_installed","update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"}}`
  
In the above example Instead of "force_installed", if you use "normal_installed", then the extension is automatically installed without user interaction, but they can disable the extension.  

   > [!TIP]
   > Formatting a JSON string correctly can be tricky. Use a JSON checker before implementing the policy. Or try the early version of [Extension Settings Generator Tool](https://microsoft.github.io/edge-extension-settings-generator/minimal)

## Configure using the Windows Registry

The ExtensionSettings policy should be written to the registry under this key:

`HKLM\Software\Policies\Microsoft\Edge\`

> [!NOTE]
> It’s possible to use HKCU instead of HKLM. The equivalent path can be configured with Group Policy Object (GPO).  

For Microsoft Edge, all settings will start under this key:

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\`

The next key that you will create is either the Extension ID for individual scope or an asterisk (*) for the Default Scope. For example, you'd use the following location for settings that apply to Google Hangouts:

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings\nckgahadagoaajjgafhacjanaoiihapd`

For settings that apply to the Default Scope, use this location:

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings\*`

Different settings will require different formats, depending on whether they are a string or an array of strings. Array values require [＂value＂]. String values can be entered as is. The following list shows which settings are arrays or strings:

- Installation_mode = String
- update_url = String
- blocked_permissions = Array of strings
- allowed_permissions = Array of Strings
- minimum_version_required = String
- runtime_blocked_hosts = Array of strings
- runtime_allowed_hosts = Array of Strings
- blocked_install_message = String


## See also

- [Manage Microsoft Edge extensions in the enterprise](microsoft-edge-manage-extensions.md)
- [Use group policies to manage Microsoft Edge extensions](microsoft-edge-manage-extensions-policies.md)
- [FAQ for Microsoft Edge Extensions](microsoft-edge-manage-extensions-faq.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
