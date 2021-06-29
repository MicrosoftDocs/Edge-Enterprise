---
title: "Edge for Virtualization desktop infrastructure"
ms.author: anlake
author: AndreaLBarr
manager: collw
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Microsoft Edge for Virtualized Desktop Infrastructure."
---

# Microsoft Edge for Virtualized Desktop Infrastructure

This article describes the requirements and limitations for using Microsoft Edge in a virtualized environment.

## What is VDI?

Virtual Desktop Infrastructure (VDI) is virtualization technology that hosts a desktop operating system and applications on a centralized server in a data center. This enables a fully personalized desktop experience for users with a fully secured and compliant centralized source.

Microsoft Edge can be used in such a virtualized environment in much the same ways as it can be used on the local device, all the while running from secure and controlled server environment. Depending on your chosen VDI solution it may also be possible to give your users seamless access to intranet Applications and Sites.

Most features of Edge are supported on VDI environments without any special configuration. However, to ensure an optimal experience it’s recommended to follow the guidance below.

## Platforms certified for Edge

- Azure Virtual Desktop
- Citrix Virtual Apps and Desktops (formerly known as XenApp and XenDesktop)

While other VDI solutions have not yet been verified by the Edge team, it is expected that the most common workflows in Edge should be supported. Guidance provided below may or may not be applicable to your chosen solution.

## Edge on VDI performance considerations

When designing your VDI environment you should carefully consider the workflows and needs of your users to achieve optimal performance, as well as the limits of your server configuration.

Edge recommends the following minimal requirements for deploying Edge to VDI environments:

- vCPU – 2-4 Cores per User
- RAM – 1 GB per User

Please note that large complex web applications and extensions will require more memory and will have to be accounted for when configuring your environment.

## Edge on non-persisted VDI environments

Many VDI solutions allow access to persisted environments, where users are assigned a virtual environment that persists between sessions, and non-persisted environments, where users are assigned to one of several available machines, possibly a different machine each session, user data may or may not sync between sessions.

When using a non-persisted environment, one usually creates a “golden image” which is used for each device that includes the needed apps and configurations. Below are our recommendations for preparing Edge for such an image.

### Deploy Edge

If you are on Windows 10, version 1803 and above, you should have Microsoft Edge installed on your system. However, if you are on an older version of Windows or wish to deploy a different channel of Edge, the following steps are recommended.

1. Download the Edge MSI package matching your VDI VM operating system from:

    - [Download Microsoft Edge for Business - Microsoft](https://www.microsoft.com/edge/business/download)

2. Install the MSI to the VDI VM by running the following command:

    - `msiexec /i <path_to_msi> /qn /norestart /l*v <install_logfile_name>`

### Disable automatic updates

For non-persisted machines it is best practice to disable automatic updates and instead update Edge by updating the “golden image” to ensure that there are no version mismatches among the pool of machines.

See the following policies for disabling automatic updates:

- [Update policy override default](/deployedge/microsoft-edge-update-policies#updatedefault)

- [Update policy override](/deployedge/microsoft-edge-update-policies#update)

### Profile management

On non-persisted setups it is important to consider that VMs may not maintain user state between sessions or users may be assigned a VM they have never used before and as such has none of their user data.

Edge supports several methods for syncing user data such that it is available regardless of how they are accessing Edge.

### Azure AD Sync

If your Azure AD plan supports it, Enterprise sync is the fastest and easiest method to ensure that Edge user data is synced to all user devices.  

See the following for more information on requirements and configuration.  

- [Configure Microsoft Edge enterprise sync | Microsoft Docs](/deployedge/microsoft-edge-enterprise-sync)

### On-premise Sync for Active Directory Users

With on-premises sync, Microsoft Edge saves an Active Directory user's favorites and settings to a file that can easily be moved between different computers.  

See the following for more information on requirements and configuration.  

- [On-premises sync for Active Directory (AD) users | Microsoft Docs](/deployedge/microsoft-edge-on-premises-sync)

### User Profile Redirection  

There are several solutions for migrating and redirecting the entire user folder to ensure that user context is maintained in such non-persisted environments. Check with your VDI provider to determine the recommended solution.

Some popular solutions include:

- [FSLogix Overview - FSLogix | Microsoft Docs](/fslogix/overview)
- [How to Configure Citrix Profile Management](https://support.citrix.com/article/CTX222893)

It is also may be recommended that when using this method unnecessary folders be excluded from the backed-up user folder to reduce initial loading times when users are logging on to a machine and the profile is being migrated. If so, we recommend the following folders be excluded from your backup to reduce size.

- %LocalAppData%\Microsoft\Edge\User Data\Default\Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed

## Known issues

### Microsoft Edge crashes in older versions of XenApp and XenDesktop

This issue should be mitigated in newer versions however if you are encountering this issue in your environment, you can work around the issue by disabling Citrix API Hooks for Edge, see [How to Disable Citrix API Hooks on a Per-application Basis.](https://support.citrix.com/article/CTX107825)

### Degraded performance when rendering pages with exceptionally large HTML tables

The following Citrix policies are known to slow rendering of html pages with very large (30,000+ row) tables.

- Automatic keyboard display
- Remote the combo box

See [Mobile experience policy settings (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html) for more information. Disabling these policies should mitigate the issue.

### Windows Account Manager authorization scenarios (i.e.  Azure sync) fail in Edge when run as a Citrix seamless application

This is a known issue in Edge and other applications that use WAM (i.e. Office) due to Windows components necessary for such scenarios not being initialized when running in the “seamless” mode. To work around this issue:

- Use Edge via a Remote Desktop to the Citrix Host instead of as a seamless remote application.
- Use Azure Virtual Desktop remote apps instead, which has mitigation's for this issue.
