---
title: "Microsoft Edge Update Policy Documentation"
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 11/12/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom:
description: "Documentation for all policies supported by the Microsoft Edge Updater"
---

# Microsoft Edge - Update policies

The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.

For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)
> [!NOTE]
> This article applies to Microsoft Edge version 77 or later.
## Available policies
These tables lists all of the update-related group policies available in this release of Microsoft Edge. Use the links in the table to get more details about specific policies.

|&nbsp;|&nbsp;|
|**-**|-|
|**[Applications](#applications)**|[Preferences](#preferences)|
|**[Proxy Server](#proxy-server)**|[Microsoft Edge WebView](#microsoft-edge-webview)|
### [Applications](#applications-policies)
|Policy Name|Caption|
|-|-|
|[InstallDefault](#installdefault)|Allow installation default|
|[UpdateDefault](#updatedefault)|Update policy override default|
|[Install](#install)|Allow installation (per channel)|
|[Update](#update)|Update policy override (per channel)|
|[Allowsxs](#allowsxs)|Allow Microsoft Edge Side by Side browser experience|
|[CreateDesktopShortcutDefault](#createdesktopshortcutdefault)|Prevent Desktop Shortcut creation upon install default|
|[CreateDesktopShortcut](#createdesktopshortcut)|Prevent Desktop Shortcut creation upon install (per channel)|
|[RollbackToTargetVersion](#rollbacktotargetversion)|Rollback to Target version (per channel)|
|[TargetVersionPrefix](#targetversionprefix)|Target version override (per channel)|

### [Preferences](#preferences-policies)
|Policy Name|Caption|
|-|-|
|[AutoUpdateCheckPeriodMinutes](#autoupdatecheckperiodminutes)|Auto-update check period override|
|[UpdatesSuppressed](#updatessuppressed)|Time period in each day to suppress auto-update check|

### [Proxy Server](#proxy-server-policies)
|Policy Name|Caption|
|-|-|
|[ProxyMode](#proxymode)|Choose how to specify proxy server settings|
|[ProxyPacUrl](#proxypacurl)|URL to a proxy .pac file|
|[ProxyServer](#proxyserver)|Address or URL of proxy server|

### [Microsoft Edge WebView](#microsoft-edge-webview-policies)
|Policy Name|Caption|
|-|-|
|[Install](#install-webview)|Allow installation|
|[Update](#update-webview)|Update policy override|

## Applications policies

[Back to top](#microsoft-edge---update-policies)
### InstallDefault
#### Allow installation default
>Microsoft Edge Update 1.2.145.5 and later

#### Description
You can specify the default behavior of all channels to allow or block Microsoft Edge on domain-joined devices.

You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.

If you disable this policy, the installation of Microsoft Edge is blocked. This only affects the installation of Microsoft Edge software when the '[Allow installation](#install)' policy is set to Not Configured.

This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.

This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: InstallDefault
- GP name: Allow installation default
- GP path: Administrative Templates/Microsoft Edge Update/Applications
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: InstallDefault
- Value Type: REG_DWORD
##### Example value:
```
0x00000001
```
[Back to top](#microsoft-edge---update-policies)


### UpdateDefault
#### Update policy override default
>Microsoft Edge Update 1.2.145.5 and later

#### Description
Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge. Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.

  If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:
   - Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.
   - Automatic silent updates only: Updates are applied only when they're found by the periodic update check.
   - Manual updates only: Updates are applied only when the user runs a manual update check.
   - Updates disabled: Updates are never applied.

  If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available. If you disable updates, periodically check for updates, and distribute them to users.

  If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.

  This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: UpdateDefault
- GP name: Update policy override default
- GP path: Administrative Templates/Microsoft Edge Update/Applications
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: UpdateDefault
- Value Type: REG_DWORD
##### Example value:
```
0x00000003
```
[Back to top](#microsoft-edge---update-policies)


### Install
#### Allow installation
>Microsoft Edge Update 1.2.145.5 and later

#### Description
Specifies whether a Microsoft Edge channel can be installed on domain-joined devices.

  If you enable this policy for a channel, Microsoft Edge will not be blocked from installation.

  If you disable this policy for a channel, Microsoft Edge will be blocked from installation.

  If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge.

  This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: Install
- GP name: Allow installation
- GP path: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - (Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Value Type: REG_DWORD
##### Example value:
```
0x00000001
```
[Back to top](#microsoft-edge---update-policies)


### Update
#### Update policy override
>Microsoft Edge Update 1.2.145.5 and later

#### Description
Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.

If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:
  - Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.
  - Automatic silent updates only: Updates are applied only when they're found by the periodic update check.
  - Manual updates only: Updates are applied only when the user runs a manual update check. (Not all apps provide an interface for this option.)
  - Updates disabled: Updates are never applied.

If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available. If you disable updates, periodically check for updates, and distribute them to users.

If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.

See [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) for more information.

This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: Update
- GP name: Update policy override
- GP path: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - (Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Value Type: REG_DWORD
##### Example value:
```
always allow updates 0x00000001
Automatic silent updates only 0x00000003
manual updates only 0x00000002
updates disabled 0x00000000
```
[Back to top](#microsoft-edge---update-policies)


### Allowsxs
#### Allow Microsoft Edge Side by Side browser experience
>Microsoft Edge Update 1.2.145.5 and later

#### Description
This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.

If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.  This is the same behavior as the “Disabled” setting.

The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.  This is the same behavior as the “Not Configured” setting.

When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.

For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update. Note: ​A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: Allowsxs
- GP name: Allow Microsoft Edge Side by Side browser experience
- GP path: Administrative Templates/Microsoft Edge Update/Applications
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: Allowsxs
- Value Type: REG_DWORD
##### Example value:
```
0x00000001
```
[Back to top](#microsoft-edge---update-policies)


### CreateDesktopShortcutDefault
#### Prevent Desktop Shortcut creation upon install default
>Microsoft Edge Update 1.3.128.0 and later

#### Description
Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.

  If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.
  If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.
  If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.
  If Microsoft Edge is already installed, this policy will have no effect.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: CreateDesktopShortcutDefault
- GP name: Prevent Desktop Shortcut creation upon install default
- GP path: Administrative Templates/Microsoft Edge Update/Applications
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: CreateDesktopShortcutDefault
- Value Type: REG_DWORD
##### Example value:
```
0x00000001
```
[Back to top](#microsoft-edge---update-policies)


### CreateDesktopShortcut
#### Prevent Desktop Shortcut creation upon install
>Microsoft Edge Update 1.3.128.0 and later

#### Description
If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.
  If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.
  If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.
  If Microsoft Edge is already installed, this policy will have no effect.

  If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: CreateDesktopShortcut
- GP name: Prevent Desktop Shortcut creation upon install
- GP path: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - (Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Value Type: REG_DWORD
##### Example value:
```
0x00000001
```
[Back to top](#microsoft-edge---update-policies)


### RollbackToTargetVersion
#### Rollback to Target version
>Microsoft Edge Update 1.3.133.3 and later

#### Description
Specifies that Microsoft Edge Update should rollback installations of Microsoft Edge to the version indicated in '[Target version override](#targetversionprefix)'.

This policy has no effect unless '[Target version override](#targetversionprefix)' is set and '[Update policy override](#update)' is set to one of the ON states (Always allow updates, Automatic silent updates only, Manual updates only).

If you disable this policy or don't configure it, installs that have a version higher than that specified by '[Target version override](#targetversionprefix)' will be left as-is.

If you enable this policy, installs that have a current version higher than specified by the '[Target version override](#targetversionprefix)' will be downgraded to the target version.

We recommend that users install the latest version of the Microsoft Edge browser to ensure protection by the latest security updates. Rollback to an earlier version risks exposure to known security issues. This policy is meant to be used as a temporary fix to address issues in a Microsoft Edge browser update.

Before temporarily rolling back your browser version, we recommend that you turn on Sync ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) for all users in your organization. If you don't turn on Sync, there is a risk of permanent browsing data loss. Use this policy at your own risk.

Note: All versions available for rollback can be viewed here [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).

This policy applies to Microsoft Edge version 86 or later.

See [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) for more information.

This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: RollbackToTargetVersion
- GP name: Rollback to Target version
- GP path: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - (Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Value Type: REG_DWORD
##### Example value:
```
0x00000001
```
[Back to top](#microsoft-edge---update-policies)


### TargetVersionPrefix
#### Target version override
>Microsoft Edge Update 1.3.119.43 and later

#### Description
When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.

The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.

If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.

If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.

See [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) for more information.

This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: TargetVersionPrefix
- GP name: Target version override
- GP path: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - (Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Value Type: REG_SZ
##### Example value:
```
83.0.499.12
```
[Back to top](#microsoft-edge---update-policies)


## Preferences policies

[Back to top](#microsoft-edge---update-policies)
### AutoUpdateCheckPeriodMinutes
#### Auto-update check period override
>Microsoft Edge Update 1.2.145.5 and later

#### Description
If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks. Otherwise, by default, auto-update checks for updates every 10 hours.

  If you want to disable all auto-update checks, set the value to 0 (not recommended).
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: AutoUpdateCheckPeriodMinutes
- GP name: Auto-update check period override
- GP path: Administrative Templates/Microsoft Edge Update/Preferences
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: AutoUpdateCheckPeriodMinutes
- Value Type: REG_DWORD
##### Example value:
```
0x00000578
```
[Back to top](#microsoft-edge---update-policies)


### UpdatesSuppressed
#### Time period in each day to suppress auto-update check
>Microsoft Edge Update 1.3.33.5 and later

#### Description
If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes). Duration isn't affected by daylight saving time. For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.

  If you disable or don't configure this policy, update checks aren't suppressed during any specific period.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: UpdatesSuppressed
- GP name: Time period in each day to suppress auto-update check
  - Options { Hour, Minute, Duration }
- GP path: Administrative Templates/Microsoft Edge Update/Preferences
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - UpdatesSuppressedDurationMin
  - UpdatesSuppressedStartHour
  - UpdatesSuppressedStartMin
- Value Type: REG_DWORD
##### Example value:
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[Back to top](#microsoft-edge---update-policies)


## Proxy Server policies

[Back to top](#microsoft-edge---update-policies)
### ProxyMode
#### Choose how to specify proxy server settings
>Microsoft Edge Update 1.3.21.81 and later

#### Description
Allows you to specify the proxy server settings that are used by Microsoft Edge Update.

  If you enable this policy, you can choose between the following proxy server options:
   - If you choose to never use a proxy server and always connect directly, all other options are ignored.
   - If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.
   - If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.
   - If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.

  If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.

  If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: ProxyMode
- GP name: Choose how to specify proxy server settings
- GP path: Administrative Templates/Microsoft Edge Update/Proxy Server
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: ProxyMode
- Value Type: REG_SZ
##### Example value:
```
fixed_servers
```
[Back to top](#microsoft-edge---update-policies)


### ProxyPacUrl
#### URL to a proxy .pac file
>Microsoft Edge Update 1.3.21.81 and later

#### Description
Allows you to specify a URL for a proxy auto-config (PAC) file.

  If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.

  This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.

  Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: ProxyPacUrl
- GP name: URL to a proxy .pac file
- GP path: Administrative Templates/Microsoft Edge Update/Proxy Server
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: ProxyPacUrl
- Value Type: REG_SZ
##### Example value:
```
https://www.microsoft.com
```
[Back to top](#microsoft-edge---update-policies)


### ProxyServer
#### Address or URL of proxy server
>Microsoft Edge Update 1.3.21.81 and later

#### Description
Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.

  If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.

  This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.

  Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: ProxyServer
- GP name: Address or URL of proxy server
- GP path: Administrative Templates/Microsoft Edge Update/Proxy Server
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: ProxyServer
- Value Type: REG_SZ
##### Example value:
```
https://www.microsoft.com
```
[Back to top](#microsoft-edge---update-policies)


## Microsoft Edge WebView policies

[Back to top](#microsoft-edge---update-policies)
### Install (WebView)
#### Allow installation
>Microsoft Edge Update 1.3.127.1 and later

#### Description
Lets you specify whether Microsoft Edge WebView can be installed using Microsoft Edge Update.

  - If you enable this policy, users can install Microsoft Edge WebView through Microsoft Edge Update.
  - If you disable this policy, users cannot install Microsoft Edge WebView through Microsoft Edge Update.
  - If you don't configure this policy, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install Microsoft Edge WebView through Microsoft Edge Update.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: Install
- GP name: Allow installation
- GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
- Value Type: REG_DWORD
##### Example value:
```
0x00000001
```
[Back to top](#microsoft-edge---update-policies)


### Update (WebView)
#### Update policy override
>Microsoft Edge Update 1.3.127.1 and later

#### Description
Lets you specify whether or not automatic updates are enabled for Microsoft Edge WebView. Microsoft Edge WebView is a component used by applications to display web content.
  Automatic updates are enabled by default. Disabling automatic updates for Microsoft Edge WebView might cause compatibility issues with applications that depend on this component.

  If you enable this policy, Microsoft Edge Update handles Microsoft Edge WebView updates according to how you configure the following options:
  - Always allow updates: Updates are automatically downloaded and applied
  - Updates disabled: Updates are never downloaded or applied

  If you don't enable this policy, updates are automatically downloaded and applied.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: Update
- GP name: Update policy override
- GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
- Value Type: REG_DWORD
##### Example value:
```
0x00000001
```
[Back to top](#microsoft-edge---update-policies)


## See also
  - [Configuring Microsoft Edge](configure-microsoft-edge.md)
  - [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
