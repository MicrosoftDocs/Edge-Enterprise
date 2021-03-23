---
title: "On-premises sync for Active Directory (AD) users"
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 02/12/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "On-premises sync for Active Directory (AD) users"
---

# On-premises sync for Active Directory (AD) users

This article explains how Active Directory (AD) users can roam Microsoft Edge favorites and settings between computers without connecting to Microsoft cloud services.

> [!NOTE]
> This article applies to Microsoft Edge version 85 or later.

## Introduction

Syncing user data in Microsoft Edge normally requires either a Microsoft Account or an Azure Active Directory (Azure AD) account, and a connection to Microsoft cloud services. With on-premises sync, Microsoft Edge saves an Active Directory user's favorites and settings to a file that can be moved between different computers. On-premises sync doesn't interfere with cloud syncing for those profiles that allow it.

## How it works

Microsoft Edge allows profiles to be associated with Active Directory (AD) accounts, which can't be used with cloud sync. When on-premises sync is enabled, the data from the AD profile is saved to a file named profile.pb. By default, this file is stored in *%APPDATA%/Microsoft/Edge*. After this file is written, it can be moved between different computers, and user data will be read and written on each computer. Microsoft Edge only reads and writes from this file; it is the admin's responsibility to ensure that the file is moved as needed.

## Use on-premises sync

To use on-premises sync, you have to enable it, associate a profile with an AD account, and optionally, change the location of the user data.

### Enable on-premises sync

To enable on-premises sync in Microsoft Edge, configure the [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled) policy.

### Ensure that a profile is associated with an Active Directory account

On-premises sync only works with the profile associated with an Active Directory (AD) account. If no such profile exists, on-premises sync will not function. To ensure that users sign on with an AD account, configure the [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin) policy. For on-premises sync, Microsoft Edge only relies on AD to establish an identity for the user data, and there's no direct relationship between how Microsoft Edge reads and writes on-premises data to how the admin has configured roaming for an AD user.

### Change the location of the user data (optional)

By default, the user data is stored in a filed named **profile.pb** in *%APPDATA%/Microsoft/Edge*. To change the location of this file, configure the [RoamingProfileLocation](./microsoft-edge-policies.md#roamingprofilelocation) policy.

## Changes in the user experience when on-premises sync is enabled

When on-premises sync is enabled, users won't be asked to enable sync. In addition, users can't turn off sync in Sync settings, and they can't turn on sync types that aren't supported by on-premises sync.

## On-premises sync usage notes

### Running cloud sync and on-premises sync on the same computer

On-premises sync doesn't interfere with cloud sync. If Microsoft Edge has multiple Microsoft Account or Azure Active Directory profiles that sync to the cloud, these profiles will continue to sync while on-premises sync is enabled.

### Running Microsoft Edge on more than one computer at a time isn't recommended

Because on-premises sync works by moving a user data file between computers, on-premises sync doesn't sync changes between simultaneous sessions. For this reason, on-premises sync works best when used on one computer at a time. If there are simultaneous on-premises sessions running, data on any of the computers may be unexpectedly overwritten by data from another computer the next time you start a browser session.

> [!NOTE]
> Microsoft Edge locks the **profile.pb** file when on-premises sync is enabled. If folder redirection is used to share a single **profile.pb** file between different computers, then only one instance of Microsoft Edge using that file can be started.

### Using other sync policies with on-premises sync

The [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) policy can be used to selectively disable either favorites or settings sync if desired. The [SyncDisabled](./microsoft-edge-policies.md#syncdisabled) policy has no impact on on-premises sync.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md)
- [Microsoft Edge Enterprise Sync](microsoft-edge-enterprise-sync.md)