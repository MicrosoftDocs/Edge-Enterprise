---
title: "Windows updates to support Microsoft Edge"
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 11/17/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Windows updates to support Microsoft Edge."
---

# Windows updates to support the next version of Microsoft Edge

This article describes how Windows will be updated to support the next version of Microsoft Edge

> [!IMPORTANT]
> Refer to the Microsoft Edge product team [blog post](https://aka.ms/EdgeLegacyEOS) about Microsoft Edge Legacy end of service.

> [!NOTE]
> This article applies to the Microsoft Edge Stable channel.

## Microsoft Edge and the Windows release cycle

The next version of Microsoft Edge features more frequent and more flexible updating capabilities. Because browser releases aren't bound to the Windows major releases, changes will be made to the operating system to ensure that the next version of Microsoft Edge fits seamlessly into Windows. As a result, feature updates will be released on a 4-week cycle (approximately). Security and compatibility updates will be shipped as needed.

## Updates and the user experience

Updates won’t change the user experience until the Stable channel of the next version of Microsoft Edge is installed. Installing Microsoft Edge Beta, Dev, or Canary won’t trigger any changes in Windows. These browser releases will be installed alongside existing browsers.

When all the updates are applied AND the Stable channel of the next version of Microsoft Edge is installed at the system-level, the following changes will take effect on the system:

- All start menu pins, tiles, and shortcuts for the current version of Microsoft Edge will migrate to the next version of Microsoft Edge.
- All taskbar pins and shortcuts for the current version of Microsoft Edge will migrate to the next version of Microsoft Edge.
- The next version of Microsoft Edge will be pinned to the taskbar. If the current version of Microsoft Edge is already pinned, it will be replaced.
- The next version of Microsoft Edge will add a shortcut to the desktop. If the current version of Microsoft Edge already has a shortcut, it will be replaced.
- Most protocols that Microsoft Edge handles by default will be migrated to the next version of Microsoft Edge.
- Current Microsoft Edge will be hidden from all UX surfaces in the OS, including settings, all apps, and any file or protocol support dialogs.
- All attempts to launch the current version of Microsoft Edge will redirect to the next version of Microsoft Edge.

  > [!NOTE]
  > User-level installs won’t trigger the preceding behaviors.

Along with the previous changes, there are changes that will happen regardless of whether the Stable channel of the next version of Microsoft Edge is installed.

- Microsoft Edge will de-register for the books and XML protocols that the next version of Microsoft Edge doesn't support. Users attempting to open these protocols will get a dialog that prompts them to choose a default app. Visit the Microsoft Store to see our recommendations for ebook readers.
  
## Older versions of Windows

To deploy Microsoft Edge on a device running a Windows version older than Windows 10 RS4, use [Configuration Manager](https://docs.microsoft.com/mem/configmgr/apps/deploy-use/deploy-edge?bc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Fbreadcrumb%2Ftoc.json&toc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Ftoc.json), [Microsoft Intune](https://docs.microsoft.com/mem/intune/apps/apps-windows-edge?bc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Fbreadcrumb%2Ftoc.json&toc=https%3A%2F%2Fdocs.microsoft.com%2FDeployEdge%2Ftoc.json), or upgrade to a supported version of Windows 10. The following article lists the currently supported versions of Windows 10 and Windows 11.

- [Supported versions of Windows client](/windows/release-health/supported-versions-windows-client)

> [!NOTE]
> For Windows 10 RS4-20H1, deploy a Windows LCU from May 2021 or newer to get Microsoft Edge. For more information, see [Windows 10 update history](https://support.microsoft.com/topic/windows-10-update-history-1b6aac92-bf01-42b5-b158-f80c6d93eb11)

> [!IMPORTANT]
> If you need updates not listed here, please run Windows Update or contact your administrator.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge documentation](./index.yml)