---
title: "Microsoft Edge Update Policy Documentation"
ms.author: stmoody
author: dan-wesley
manager: archandr
ms.date: 07/24/2024
audience: ITPro
ms.topic: reference
ms.service: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: generated
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
| - | - |
|[Applications](#applications)|[Preferences](#preferences)|
|[Proxy Server](#proxy-server)|[Microsoft Edge Update](#microsoft-edge-update)|
|[Microsoft Edge WebView2 Runtime](#microsoft-edge-webview2-runtime)||

### [Applications](#applications-policies)
|Policy Name|Caption|
|-|-|
|[InstallDefault](#installdefault)|Allow installation default|
|[UpdateDefault](#updatedefault)|Update policy override default|
|[Install](#install)|Allow installation (per channel)|
|[Update](#update)|Update policy override (per channel)|
|[Allowsxs](#allowsxs)|Allow Microsoft Edge Side by Side browser experience|
|[CreateDesktopShortcutDefault](#createdesktopshortcutdefault)|Create Desktop Shortcut upon install default|
|[CreateDesktopShortcut](#createdesktopshortcut)|Create Desktop Shortcut upon install (per channel)|
|[RollbackToTargetVersion](#rollbacktotargetversion)|Rollback to Target version (per channel)|
|[TargetVersionPrefix](#targetversionprefix)|Target version override (per channel)|
|[TargetChannel](#targetchannel)|Target Channel override (per channel)|
|[RemoveDesktopShortcutDefault](#removedesktopshortcutdefault)|Remove Desktop Shortcuts upon update default|
|[RemoveDesktopShortcut](#removedesktopshortcut)|Remove Desktop Shortcuts upon update (per channel)|
|[EdgePreview](#edgepreview)|Allow users in the Windows Insider Program to be enrolled in Edge Preview (per channel)|
|[MeteredUpdatesDefault](#meteredupdatesdefault)|Let users update all apps on metered connections|
|[MeteredUpdates](#meteredupdates)|Let users update on metered connections (per channel)|
|[Uninstall](#uninstall)|Specify uninstall behavior for Microsoft Edge|

### [Preferences](#preferences-policies)
|Policy Name|Caption|
|-|-|
|[AutoUpdateCheckPeriodMinutes](#autoupdatecheckperiodminutes)|Auto-update check period override|
|[UpdatesSuppressed](#updatessuppressed)|Time period in each day to suppress auto-update check|

### [Proxy Server](#proxy-server-policies)
|Policy Name|Caption|
|-|-|
|[ProxyMode](#proxymode)|Choose how to specify a proxy server settings|
|[ProxyPacUrl](#proxypacurl)|URL to proxy .pac file|
|[ProxyServer](#proxyserver)|Address or URL of a proxy server|

### [Microsoft Edge Update](#microsoft-edge-update-policies)
|Policy Name|Caption|
|-|-|
|[UpdaterExperimentationAndConfigurationServiceControl](#updaterexperimentationandconfigurationservicecontrol)|Control updater's communication with the Experimentation and Configuration Service|

### [Microsoft Edge WebView2 Runtime](#microsoft-edge-webview2-runtime-policies)
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

You can override this policy for individual channels by enabling (1) the '[Allow installation](#install)' policy for specific channels.

If you disable (2) this policy, the installation of Microsoft Edge is blocked. This only affects the installation of Microsoft Edge software when the '[Allow installation](#install)' policy is set to Not Configured.

This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.

This policy is available only on Windows instances that are joined to a Microsoft&reg; Active Directory&reg; domain.
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
Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge. Can be overridden for individual channels by specifying the '[Update policy override](#update-webview)' policy for those specific channels.

If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:
- Updates disabled (0): Updates are never applied.
- Always allow updates (1) (recommended): Updates are always applied when found, either by periodic update check or by a manual update check.
- Manual updates only (2): Updates are applied only when the user runs a manual update check.
- Automatic silent updates only (3): Updates are applied only when they're found by the periodic update check.

If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available. If you disable updates, periodically check for updates, and distribute them to users.

If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update-webview)' policy.

This policy is available only on Windows instances that are joined to a Microsoft&reg; Active Directory&reg; domain.
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

  If you enable (1) this policy for a channel, Microsoft Edge will not be blocked from installation.

  If you disable (0) this policy for a channel (or set it to 'Installs disabled'), Microsoft Edge will be blocked from installation.

  If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge.

If you set this policy to Always allow Machine-Wide Installs but not Per-User Installs (4), 'Microsoft Edge' will only be deployed machine-wide.

If you set this policy to Force Installs (Machine-Wide) (5), 'Microsoft Edge' may only be deployed machine-wide if Microsoft Edge Update is pre-installed. Requires Microsoft Edge Update 1.3.155.43 or higher.

If you set this policy to Force Installs (Per-User) (6), 'Microsoft Edge' may only be deployed on a Per-User basis to all machines if Microsoft Edge Update is pre-installed Per-User. Requires Microsoft Edge Update 1.3.155.43 or higher.

This policy is available only on Windows instances that are joined to a Microsoft&reg; Active Directory&reg; domain.
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
  - Updates disabled (0): Updates are never applied.
  - Always allow updates (1) (Recommended): Updates are always applied when found, either by periodic update check or by a manual update check.
  - Manual updates only (2): Updates are applied only when the user runs a manual update check. (Not all apps provide an interface for this option.)
  - Automatic silent updates only (3): Updates are applied only when they're found by the periodic update check.

If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available. If you disable updates, periodically check for updates, and distribute them to users.

If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.

See [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) for more information.

This policy is available only on Windows instances that are joined to a Microsoft&reg; Active Directory&reg; domain.
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
0x00000001
```
[Back to top](#microsoft-edge---update-policies)


### Allowsxs
#### Allow Microsoft Edge Side by Side browser experience

>Microsoft Edge Update 1.2.145.5 and later

#### Description
This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side

If this policy is set to "Not configured", Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.  This is the same behavior as the "Disabled" setting.

The “Disabled” (0) setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.  This is the same behavior as the “Not Configured” setting.

When this policy is “Enabled” (1), Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.

For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update. Note: ​A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.

Starting with Windows 10 version 20H2 Microsoft Edge Legacy and the side-by-side browser experience are not supported.
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
#### Create Desktop Shortcut upon install default

>Microsoft Edge Update 1.3.128.0 and later

#### Description
Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.

  If you enable (1) this policy a desktop shortcut is created when Microsoft Edge is installed.
  If you disable (0) this policy, no desktop shortcut will be created when Microsoft Edge is installed.
  If you don't configure this policy a desktop shortcut to Microsoft Edge will be created during installation.
  If Microsoft Edge is already installed, this policy will have no effect.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: CreateDesktopShortcutDefault
- GP name: Create Desktop Shortcut upon install default
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
#### Create Desktop Shortcut upon install

>Microsoft Edge Update 1.3.128.0 and later

#### Description
If you enable (1) this policy a desktop shortcut is created when Microsoft Edge is installed.
  If you disable (0) this policy, no desktop shortcut will be created when Microsoft Edge is installed.
  If you don't configure this policy a desktop shortcut to Microsoft Edge will be created during installation.
  If Microsoft Edge is already installed, this policy will have no effect.

  If you don't configure this policy for a channel, the '[Create Desktop Shortcut upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: CreateDesktopShortcut
- GP name: Create Desktop Shortcut upon install
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

This policy has no effect unless '[Target version override](#targetversionprefix)' is set and '[Update policy override](#update-webview)' is set to one of the ON states (Always allow updates, Automatic silent updates only, Manual updates only).

If you disable (0) this policy or don't configure it, installs that have a version higher than that specified by '[Target version override](#targetversionprefix)' will be left as-is.

If you enable (1) this policy, installs that have a current version higher than specified by the '[Target version override](#targetversionprefix)' will be downgraded to the target version.

We recommend that users install the latest version of the Microsoft Edge browser to ensure protection by the latest security updates. Rollback to an earlier version risks exposure to known security issues. This policy is meant to be used as a temporary fix to address issues in a Microsoft Edge browser update.

Before temporarily rolling back your browser version, we recommend that you turn on Sync ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) for all users in your organization. If you don't turn on Sync, there is a risk of permanent browsing data loss. Use this policy at your own risk.

Note: All versions available for rollback can be viewed here [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).

This policy applies to Microsoft Edge version 86 or later.

See [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) for more information.

This policy is available only on Windows instances that are joined to a Microsoft&reg; Active Directory&reg; domain.
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

This policy is available only on Windows instances that are joined to a Microsoft&reg; Active Directory&reg; domain.
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


### TargetChannel
#### Target Channel override

>Microsoft Edge Update 1.3.147.1 and later

#### Description
Specifies which Channel Microsoft Edge should be updated to.

If you enable this policy, Microsoft Edge will be updated to the Channel according to how you configure the following options:

  - Stable: Microsoft Edge will be updated to the latest stable version.
  - Beta: Microsoft Edge will be updated to the latest beta version.
  - Dev: Microsoft Edge will be updated to the latest dev version.
  - Extended Stable: Microsoft Edge will be updated to the latest extended stable version, which follows a longer release cadence than stable. For more information, visit [https://go.microsoft.com/fwlink/?linkid=2163508](https://go.microsoft.com/fwlink/?linkid=2163508).

If you do not configure this policy, Microsoft Edge will be updated to the latest version available for the default Channel.

This policy is available only on Windows instances that are joined to a Microsoft&reg; Active Directory&reg; domain.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: TargetChannel
- GP name: Target Channel override
- GP path: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - (Stable): TargetChannel{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
- Value Type: REG_SZ
##### Example value:
```
dev
```
[Back to top](#microsoft-edge---update-policies)


### RemoveDesktopShortcutDefault
#### Remove Desktop Shortcuts upon update default

>Microsoft Edge Update 1.3.155.1 and later

#### Description
Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.

  If you set this policy to "Force delete system-level Desktop Shortcuts" (1), any existing system-level Microsoft Edge desktop shortcuts will be deleted when the browser updates or the machine reboots.
  If you set this policy to "Force delete system-level and user-level Desktop Shortcuts" (2), any existing system-level Microsoft Edge desktop shortcuts will be deleted when the browser updates or the machine reboots and any existing user-level desktop shortcuts will be deleted when the browser updates. This includes user-level desktop shortcuts that users might have made themselves.
  If you don't configure this policy or disable it (0), nothing will happen to existing Microsoft Edge desktop shortcuts.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: RemoveDesktopShortcutDefault
- GP name: Remove Desktop Shortcuts upon update default
- GP path: Administrative Templates/Microsoft Edge Update/Applications
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: RemoveDesktopShortcutDefault
- Value Type: REG_DWORD
##### Example value:
```
0x00000001
```
[Back to top](#microsoft-edge---update-policies)


### RemoveDesktopShortcut
#### Remove Desktop Shortcuts upon update

>Microsoft Edge Update 1.3.155.1 and later

#### Description
If you set this policy to "Force delete system-level Desktop Shortcuts" (1), any existing system-level Microsoft Edge desktop shortcuts will be deleted when the browser updates or the machine reboots.
  If you set this policy to "Force delete system-level and user-level Desktop Shortcuts" (2), any existing system-level Microsoft Edge desktop shortcuts will be deleted when the browser updates or the machine reboots and any existing user-level desktop shortcuts will be deleted when the browser updates. This includes user-level desktop shortcuts that users might have made themselves.
  If you don't configure this policy or disable it (0), nothing will happen to existing Microsoft Edge desktop shortcuts.

  If you don't configure this policy for a channel, the '[Remove Desktop Shortcuts upon update default](#removedesktopshortcutdefault)' policy configuration determines desktop shortcut removal.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: RemoveDesktopShortcut
- GP name: Remove Desktop Shortcuts upon update
- GP path: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - (Stable): RemoveDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): RemoveDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): RemoveDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): RemoveDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Value Type: REG_DWORD
##### Example value:
```
0x00000001
```
[Back to top](#microsoft-edge---update-policies)


### EdgePreview
#### Allow users in the Windows Insider Program to be enrolled in Edge Preview

>Microsoft Edge Update 1.3.168.21 and later

#### Description
Lets you specify whether users in the Windows Insider Program are enrolled in Edge Preview via Microsoft Edge Update.

  - If you enable (1) this policy, users in the Windows Insider Program are enrolled in Edge Preview via Microsoft Edge Update.

  - If you disable (0) this policy, users in the Windows Insider Program cannot be enrolled in Edge Preview via Microsoft Edge Update.

  - If you don't configure this policy, users in the Windows Insider Program are enrolled in Edge Preview via Microsoft Edge Update by default.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: EdgePreview
- GP name: Allow users in the Windows Insider Program to be enrolled in Edge Preview
- GP path: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - (Stable): EdgePreview{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): EdgePreview{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): EdgePreview{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): EdgePreview{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Value Type: REG_DWORD
##### Example value:
```
0x00000001
```
[Back to top](#microsoft-edge---update-policies)


### MeteredUpdatesDefault
#### Let users update all apps on metered connections

>Microsoft Edge Update 1.3.179.5 and later

#### Description
Specifies whether Microsoft Edge Update will update on connections marked as metered, such as cellular connections or others where data usage is controlled for all apps. 

If you don't enable and configure this policy, updates occur based the 'Download Updates over metered connections' toggle in the About Page of the Microsoft Edge browser. If a user doesn't make a choice, the Windows setting is used. You can find out more about the Windows setting here: [/windows/client-management/mdm/policy-csp-update#allowautowindowsupdatedownloadovermeterednetwork]/windows/client-management/mdm/policy-csp-update#allowautowindowsupdatedownloadovermeterednetwork)

Always allow updates (2): Updates are always downloaded when found, either by automatic update check or by a manual update check.

Updates disabled (1): Updates are not downloaded when using a metered connection.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: MeteredUpdatesDefault
- GP name: Let users update all apps on metered connections
- GP path: Administrative Templates/Microsoft Edge Update/Applications
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: MeteredUpdatesDefault
- Value Type: REG_DWORD
##### Example value:
```
0x00000001
```
[Back to top](#microsoft-edge---update-policies)


### MeteredUpdates
#### Let users update on metered connections

>Microsoft Edge Update 1.3.179.5 and later

#### Description
Specifies whether Microsoft Edge Update will update on connections marked as metered, such as cellular connections or others where data usage is controlled for the Microsoft Edge browser. 

If you don't enable and configure this policy, updates occur based the 'Download Updates over metered connections' toggle in the About Page of the Microsoft Edge browser. If a user doesn't make a choice, the Windows setting is used. You can find out more about the Windows setting here: [/windows/client-management/mdm/policy-csp-update#allowautowindowsupdatedownloadovermeterednetwork](/windows/client-management/mdm/policy-csp-update#allowautowindowsupdatedownloadovermeterednetwork)

Always allow updates (2): Updates are always downloaded when found, either by automatic update check or by a manual update check.

Disable updates (1): Updates are not downloaded when using a metered connection.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: MeteredUpdates
- GP name: Let users update on metered connections
- GP path: 
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary
  - Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - (Stable): MeteredUpdates{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): MeteredUpdates{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): MeteredUpdates{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): MeteredUpdates{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- Value Type: REG_DWORD
##### Example value:
```
0x00000001
```
[Back to top](#microsoft-edge---update-policies)

### Uninstall
#### Specify uninstall behavior for Microsoft Edge
>Microsoft Edge Update 1.3.193.5 and later

#### Description
You can specify whether Microsoft Edge (stable channel) is uninstalled, or is blocked from being uninstalled, on domain-joined devices in the European Economic Area (EEA).

If this policy is set to 'Enabled', Microsoft Edge will be automatically uninstalled on all devices in the EEA where this policy is deployed. User data will be kept on the device. Microsoft Edge will be uninstalled the next time Microsoft Edge Update automatically checks for updates. If Microsoft Edge is uninstalled from the devices, applications, widgets (for example, News, Search, and Weather) or any other Progressive Web Applications (PWAs) that depend on Microsoft Edge will no longer be available.

If this policy is set to 'Enabled and delete user data' (Setting '2'), Microsoft Edge will be automatically uninstalled on all devices in the EEA where this policy is deployed, and user data will be deleted from the device.

If this policy is set to 'Disabled' (Setting '3'), all users in the EEA are prevented from uninstalling Microsoft Edge where this policy is deployed.

If the policy is 'Not configured' (default setting), a user's Windows region setting determines whether they can uninstall Microsoft Edge on a domain-joined device. Only users in EEA countries will be able to uninstall Microsoft Edge if they choose to do so. Users outside of this area will not be able to uninstall Microsoft Edge.

This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.

If Microsoft Edge needs to be reinstalled:
- You can set the 'Install' Policy to Force Installs (Machine-Wide) to reinstall Microsoft Edge.
- If you set the Install policy to Force Installs (Machine-Wide), and also set the Uninstall policy to Enabled, the Force Installs (Machine-Wide) policy will override the Uninstall policy.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: Uninstall
- GP name: Specify uninstall behavior for Microsoft Edge
- GP path: Administrative Templates/Microsoft Edge Update/Applications
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
    - (Stable): Uninstall{56eb18f8-b008-4cbd-b6d2-8c97fe7e9062}
- Value Type: REG_DWORD
##### Example value:
```
0x00000001
```
[Back to top](#microsoft-edge---update-policies)

## Preferences policies

[Back to top](#microsoft-edge---update-policies)
### AutoUpdateCheckPeriodMinutes
#### Auto-update check period override

>Microsoft Edge Update 1.2.145.5 and later

#### Description
Minimum number of minutes between automatic update checks.

Set this policy to the value 0 to disable all periodic network traffic by Microsoft Edge Update. This is not recommended, as it prevents Microsoft Edge Update itself from receiving stability and security updates.

The 'Update policy override default' and per-application 'Update policy override' settings should be used to manage application updates rather than this setting.

The values for this policy can range from 0 to 43200.
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

  The values for this policy can range from 0 to 23 for hours, 0 to 59 for minutes and 0 to 960 for duration in minutes.
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
#### Choose how to specify a proxy server settings

>Microsoft Edge Update 1.3.21.81 and later

#### Description
Allows you to specify the proxy server settings that are used by Microsoft Edge Update.

  If you enable this policy, you can choose between the following proxy server options:
   - If you choose to never use a proxy server and always connect directly, all other options are ignored.
   - If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.
   - If you choose fixed server proxy mode, you can specify further options in '[Address or URL of a proxy server](#proxyserver)' policy.
   - If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to proxy .pac file](#proxypacurl)' policy.

  If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.

  If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: ProxyMode
- GP name: Choose how to specify a proxy server settings
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
#### URL to proxy .pac file

>Microsoft Edge Update 1.3.21.81 and later

#### Description
Allows you to specify a URL for a proxy auto-config (PAC) file.

  If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.

  This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify a proxy server settings](#proxymode)' policy.

  Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify a proxy server settings](#proxymode)' policy.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: ProxyPacUrl
- GP name: URL to proxy .pac file
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
#### Address or URL of a proxy server

>Microsoft Edge Update 1.3.21.81 and later

#### Description
Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.

  If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.

  This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify a proxy server settings](#proxymode)' policy.

  Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify a proxy server settings](#proxymode)' policy.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: ProxyServer
- GP name: Address or URL of a proxy server
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


## Microsoft Edge Update policies

[Back to top](#microsoft-edge---update-policies)
### UpdaterExperimentationAndConfigurationServiceControl
#### Control updater's communication with the Experimentation and Configuration Service

>Microsoft Edge Update 1.3.145.1 and later

#### Description
In Microsoft Edge Update, the Experimentation and Configuration Service is used to deploy experimentation payload.

Experimentation payload consists of a list of early in development features that Microsoft is enabling for testing and feedback.

If you enable (1) this policy, experimentation payload is downloaded from the Experimentation and Configuration Service.

If you disable (0) this policy, communication with the Experimentation and Configuration Service is stopped completely.

If you don't configure this policy, on a managed device the behavior is same as policy 'disabled'.

If you don't configure this policy, on an unmanaged device the behavior is same as policy 'enabled'.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: UpdaterExperimentationAndConfigurationServiceControl
- GP name: Control updater's communication with the Experimentation and Configuration Service
- GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge Update
- GP ADMX file name: msedgeupdate.admx
##### Windows Registry Settings
- Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: UpdaterExperimentationAndConfigurationServiceControl
- Value Type: REG_DWORD
##### Example value:
```
0x00000001
```
[Back to top](#microsoft-edge---update-policies)


## Microsoft Edge WebView2 Runtime policies

[Back to top](#microsoft-edge---update-policies)
### Install (WebView)
#### Allow installation

>Microsoft Edge Update 1.3.127.1 and later

#### Description
Lets you specify whether the WebView2 Runtime can be installed using Microsoft Edge Update.

  If you enable (1) this policy, users can install the WebView2 Runtime through Microsoft Edge Update.

  If you disable (0) this policy (or set it to 'Installs disabled'), users cannot install the WebView2 Runtime through Microsoft Edge Update.

  If you set this policy to Always allow Machine-Wide Installs but not Per-User Installs (4), the WebView2 Runtime will only be deployed machine-wide.

  If you set the policy to Force Installs (Machine-Wide) (5), users can install the WebView2 Runtime to all machines where Microsoft Edge Update is pre-installed. Requires Microsoft Edge Update 1.3.155.43 or higher.

  If you don't configure this policy, the WebView2 Runtime will be installed through Microsoft Edge Update.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: Install
- GP name: Allow installation
- GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView2 Runtime
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
Lets you specify whether or not automatic updates are enabled for the WebView2 Runtime. The WebView2 Runtime is a component used by applications to display web content.
  Automatic updates are enabled by default. Disabling automatic updates for the WebView2 Runtime might cause compatibility issues with applications that depend on this component.

  If you enable this policy, Microsoft Edge Update handles the WebView2 Runtime updates according to how you configure the following options:
  - Always allow updates (1): Updates are automatically downloaded and applied
  - Updates disabled (0): Updates are never downloaded or applied
 
  If you don't enable this policy, updates are automatically downloaded and applied.
#### Windows information and settings
##### Group Policy (ADMX) info
- GP unique name: Update
- GP name: Update policy override
- GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView2 Runtime
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
