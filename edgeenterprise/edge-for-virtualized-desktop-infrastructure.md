---
title: "Microsoft Edge for Virtual desktop infrastructure (VDI)"
ms.author: anlake
author: dan-wesley
manager: collw
ms.date: 11/12/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Microsoft Edge for Virtual desktop infrastructure (VDI)."
---

# Microsoft Edge for Virtual desktop infrastructure (VDI)

This article describes the requirements and limitations for using Microsoft Edge in a virtual environment.

## What is VDI?

Virtual desktop infrastructure (VDI) is a desktop virtualization technology that hosts an operating system and applications on a centralized server in a data center. This technology enables a fully personalized desktop experience for users on a secure and compliant centralized source.

Microsoft Edge can be used in a virtual environment in much the same way as it's used on a local device. A virtual desktop takes advantage of a secure and controlled server environment. Depending on the VDI solution you choose, it might also be possible to give your users seamless access to intranet applications and sites.

Most Microsoft Edge features are supported in VDI environments without any special configuration. However, to ensure an optimal experience we recommend that you review the following guidance.

## Platforms certified for Microsoft Edge

The following platforms are certified for Microsoft Edge:

- Azure Virtual Desktop
- Citrix Virtual Apps and Desktops (formerly known as XenApp and XenDesktop)

Although other VDI solutions haven't been certified by the Microsoft Edge team yet, it's expected that the most common workflows in Microsoft Edge should be supported. The following guidance may or may not be applicable to your chosen solution.

## Performance considerations for Microsoft Edge on VDI

When designing your VDI environment you should carefully consider the workflows and needs of your users to achieve optimal performance, and understand the limits of your server configuration.

The following minimum requirements are recommended for deploying Microsoft Edge on a VDI environment:

- vCPU – 2-4 cores per User
- RAM – 1 GB per User

Large and complex web applications and extensions will need more memory and processing capability, which must be considered when configuring your virtual environment.

## Microsoft Edge on non-persisted VDI environments

Many VDI solutions allow access to persisted environments, where users are assigned a virtual environment that persists between sessions, and non-persisted environments, where users are assigned to one of several available machines, possibly a different machine each session, user data may or may not sync between sessions.

When using a non-persisted environment, one usually creates a "golden image" that has the required apps and configurations that will be deployed on each device. Use the following recommendations as a guide for preparing a golden image.

### Deploy Microsoft Edge

If you are on Windows 10, version 1803 and above, you should already have Microsoft Edge installed on your system. However, if you're using an older version of Windows or want to deploy a different Microsoft Edge channel, follow these steps:

1. Download the Microsoft Edge MSI package that matches your VDI VM operating system from:

    - [Download Microsoft Edge for Business - Microsoft](https://www.microsoft.com/edge/business/download)

2. Run the following command to install the MSI to the VDI virtual machine (VM):

    - `msiexec /i <path_to_msi> /qn /norestart /l*v <install_logfile_name>`

### Disable automatic updates

For non-persisted machines, the best practice to disable automatic updates and update Microsoft Edge by updating the golden image to ensure that there are no version mismatches among the pool of virtual machines.

For more information about disabling automatic updates, see the following policies:

- [Update policy override default](/deployedge/microsoft-edge-update-policies#updatedefault)

- [Update policy override](/deployedge/microsoft-edge-update-policies#update)

### Profile management

On non-persisted setups, it's important to consider that VMs may not maintain user state between sessions or users may be assigned a VM they've never used before. In this scenario, the VM doesn't have any of the user's data.

Microsoft Edge supports several methods for syncing user data so it's available regardless of how they are accessing Microsoft Edge. Two methods are Azure Active Directory (Azure AD) sync and on-premises sync for AD users.

### Azure AD Sync

If your Azure AD plan supports it, Enterprise sync is the fastest and easiest method to ensure that Microsoft Edge user data is synced to all user devices. For more information, see [Configure Microsoft Edge enterprise sync](/deployedge/microsoft-edge-enterprise-sync)

### On-premise Sync for Active Directory Users

With on-premises sync, Microsoft Edge saves an Active Directory user's favorites and settings to a file that can easily be moved between different computers.  

For more information about requirements and configuration, see [On-premises sync for Active Directory (AD) users](/deployedge/microsoft-edge-on-premises-sync)

### User Profile Redirection  

There are several solutions for migrating and redirecting the entire user folder to ensure that user context is maintained in a non-persisted environment. Check with your VDI provider to determine the recommended solution for your environment.

Some popular solutions include the following options:

- [FSLogix Overview - FSLogix](/fslogix/overview)
- [How to Configure Citrix Profile Management](https://support.citrix.com/article/CTX222893)

It some cases, unnecessary folders should be excluded from the backed-up user folder to reduce initial loading times when a user's logging on to a machine and their profile is being migrated. If so, we recommend the following folders be excluded from your backup to reduce size.

- %LocalAppData%\Microsoft\Edge\User Data\Default\Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed

## Known issues

### Microsoft Edge crashes in older versions of XenApp and XenDesktop

This issue should be mitigated in newer versions of these products. However, if you're encountering this issue in your environment, you can work around the issue by disabling Citrix API Hooks for Microsoft Edge, see [How to Disable Citrix API Hooks on a Per-application Basis.](https://support.citrix.com/article/CTX107825)

### Degraded performance when rendering pages with exceptionally large HTML tables

The following Citrix policies are known to slow rendering of html pages with large (30,000+ row) tables.

- Automatic keyboard display
- Remote the combo box

For more information, see [Mobile experience policy settings (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html) for more information. Disabling these policies should mitigate the issue.

### Windows Account Manager authorization scenarios (that is, Azure sync) fail in Microsoft Edge when run as a Citrix seamless application

This is a known issue in Microsoft Edge and other applications that use WAM (that is, Office) due to necessary Windows components not being initialized when running in the "seamless" mode. Try one of the following options to work around this issue:

- Use Microsoft Edge via a Remote Desktop to the Citrix Host instead of as a seamless remote application.
- Use Azure Virtual Desktop remote apps instead, which has mitigations for this issue.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Azure Virtual Desktop](https://azure.microsoft.com/services/virtual-desktop/)