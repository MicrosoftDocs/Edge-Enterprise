---
title: "Microsoft Edge - EdgeUpdater Policy Documentation"
ms.author: apryzgoda
author: dan-wesley
manager: azeigler
ms.date: 08/30/2023
audience: ITPro
ms.topic: reference
ms.service: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: 
description: "Documentation for all policies for macOS supported by the EdgeUpdater"
---

# Microsoft Edge - EdgeUpdater policies for macOS

The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.

For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)

For information about Update policies available in Microsoft Edge for Windows, check out [Microsoft Edge Update policy reference](/deployedge/microsoft-edge-update-policies).

For an example of how to use a plist to deploy the policies in this document, check out [Update configuration example](/deployedge/edge-learnmore-edgeupdater-for-macos#update-configuration-example)

> [!NOTE]
> This article applies to Microsoft Edge version 113 or later.

## Available policies

These tables list all of the update-related group policies available in this release of Microsoft Edge. Use the links in the table to get more details about specific policies.

|&nbsp;|&nbsp;|
|-|-|
|[Applications](#applications)|[Preferences](#preferences)|

### [Applications](#applications-policies)
|Policy Name|Caption|
|-|-|
|[UpdateDefault](#updatedefault)|Update policy override default|
|[Update](#update)|Update policy override (per channel)|

### [Preferences](#preferences-policies)
|Policy Name|Caption|
|-|-|
|[AutoUpdateCheckPeriodMinutes](#autoupdatecheckperiodminutes)|Auto-update check period override|
|[UpdatesSuppressed](#updatessuppressed)|Time period in each day to suppress auto-update check|
<!-- ==================================================== -->
## Applications policies

[Back to top](#microsoft-edge---edgeupdater-policies-for-macos)

### UpdateDefault

#### Update policy override default

>EdgeUpdater 109.0.1518.107 and later

#### Description

Lets you specify the default behavior for all channels concerning the way EdgeUpdater handles available updates for Microsoft Edge. Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.

If you enable this policy, EdgeUpdater handles Microsoft Edge updates according to how you configure the following options:

* Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.
* Automatic silent updates only: Updates are applied only when they're found by the periodic update check.
*  Manual updates only: Updates are applied only when the user runs a manual update check.
*  Updates disabled: Updates are never applied.

If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available. If you disable updates, periodically check for updates, and distribute them to users.

If you don't enable and configure this policy, EdgeUpdater handles available updates as specified by the '[Update policy override](#update)' policy.

##### Supported values:

```
0 // Always allow updates
1 // Automatic silent updates only
2 // Manual updates only
3 // Updates disabled
```

[Back to top](#microsoft-edge---edgeupdater-policies-for-macos)
<!-- ====================TEMP END ======================== -->

### Update

#### Update policy override

>EdgeUpdater 109.0.1518.107 and later

#### Description

Specifies how EdgeUpdater handles available updates from Microsoft Edge.

If you enable this policy, EdgeUpdater handles Microsoft Edge updates according to how you configure the following options:

* Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.
* Automatic silent updates only: Updates are applied only when they're found by the periodic update check.
* Manual updates only: Updates are applied only when the user runs a manual update check.
* Updates disabled: Updates are never applied.

If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available. If you disable updates, periodically check for updates, and distribute them to users.

If you don't enable and configure this policy, EdgeUpdater handles available updates as specified by the '[Update policy override](#update)' policy.

##### Supported values:

```
0 // Always allow updates
1 // Automatic silent updates only
2 // Manual updates only
3 // Updates disabled
```

[Back to top](#microsoft-edge---edgeupdater-policies-for-macos)
<!-- ==================================================== -->
## Preferences policies

[Back to top](#microsoft-edge---edgeupdater-policies-for-macos)

### AutoUpdateCheckPeriodMinutes

#### Auto-update check period override

>EdgeUpdater 109.0.1518.107 and later

#### Description

Minimum number of minutes between automatic update checks.

Set this policy to the value 0 to disable all periodic network traffic by EdgeUpdater. This is not recommended, as it prevents EdgeUpdater itself from receiving stability and security updates.

The 'Update policy override default' and per-application 'Update policy override' settings should be used to manage application updates rather than this setting.

##### Supported values:

```
0   // Always allow updates
```

[Back to top](#microsoft-edge---edgeupdater-policies-for-macos)

### UpdatesSuppressed

#### Time period in each day to suppress auto-update check

>EdgeUpdater 109.0.1518.107 and later

#### Description

If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes). Duration isn't affected by daylight saving time. For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.

If you disable or don't configure this policy, update checks aren't suppressed during any specific period.

##### Example value:

```
duration   : 60 //60 minutes
start hour : 1
start min  : 2 //1:02 am
```

[Back to top](#microsoft-edge---edgeupdater-policies-for-macos)

<!-- ==================================================== -->
## See also

* [Microsoft Edge for macOS switch from Microsoft AutoUpdate to EdgeUpdater](/deployedge/edge-learnmore-edgeupdater-for-macos)
* [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
