---
title: "Windows updates for Microsoft Edge"
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Windows updates for Microsoft Edge."
---

# Windows updates to support the next version of Microsoft Edge

This article describes how Windows will be updated to support the next version of Microsoft Edge.

> [!IMPORTANT]
> Refer to the Microsoft Edge product team [blog post](https://aka.ms/EdgeLegacyEOS) about Microsoft Edge Legacy end of service.

> [!NOTE]
> This article applies to the Microsoft Edge Stable channel.

## Microsoft Edge and the Windows release cycle

The next version of Microsoft Edge features more frequent and more flexible updating capabilities. Because browser releases aren't bound to the Windows major releases, changes will be made to the operating system to ensure that the next version of Microsoft Edge fits seamlessly into Windows. As a result, feature updates will be released on a 6-week cycle (approximately). Security and compatibility updates will be shipped as needed.

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
  > User-level installs won’t trigger these behaviors.

Along with the previous changes, there are changes that will happen regardless of whether the Stable channel of the next version of Microsoft Edge is installed.

- Microsoft Edge will de-register for the books and XML protocols that the next version of Microsoft Edge doesn't support. Users attempting to open these protocols will get a dialog that prompts them to choose a default app. Learn more about changes to books support at [Download an ePub app to keep reading e-books](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fsupport.microsoft.com%2Fhelp%2F4517840&data=02%7C01%7Cv-danwes%40microsoft.com%7Cc9f8571b880549c30fcf08d72be5eaf9%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637026138803983526&sdata=qtb3DvVZQ6H%2FFXnBievkl%2B%2BngAQXwl340PcH8kRc3y4%3D&reserved=0).

## Timeline

The changes needed to support the described experience will be delivered with three updates for different versions of Windows.

### Windows versions 1903 and 1909

- First set of changes in optional July 2019 update, delivered with the August 2019 security update.
- Second set of changes in the optional August 2019 update, delivered with the September 2019 security update.

  > [!NOTE]
  > This is the update where Microsoft Edge will de-register for the XML protocol.

- Third set of changes in the optional September 2019 update, delivered with the October 2019 security update.

  > [!NOTE]
  > This is the update where Microsoft Edge will no longer support eBooks.

### Windows versions 1709, 1803, and 1809

- First set of changes in an optional August 2019 update, delivered with the September 2019 security update.
- Second set of changes in an optional September 2019 update, delivered with the October 2019 security update.

  > [!NOTE]
  > This is the update where Microsoft Edge will de-register for the XML protocol.

- Third set of changes in an optional October 2019 update, delivered with the November 2019 security update.

  > [!NOTE]
  > This is the update where Microsoft Edge will no longer support eBooks.

The following table gives the details for specific updates in each set of changes.

| Windows 10 | More Information | Required Download |
|--|--|--|
| Version 1709 | [KB4525241](https://support.microsoft.com/help/4525241/windows-10-update-kb4525241) | [Cumulative Update for Windows 10 Version 1709](https://www.catalog.update.microsoft.com/Search.aspx?q=4525241) |
| Version 1803  | [KB4525237](https://support.microsoft.com/help/4525237/windows-10-update-kb4525237) | [Cumulative Update for Windows 10 Version 1803](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4525237) |
| Version 1809  | [KB4523205](https://support.microsoft.com/help/4523205/windows-10-update-kb4523205) | [Cumulative Update for Windows 10 Version 1809](https://www.catalog.update.microsoft.com/Search.aspx?q=4523205) |
| Version 1903 and 1909 |[KB4517389](https://support.microsoft.com/help/4517389/windows-10-update-kb4517389)  | [Cumulative Update for Windows 10 Version 1903 and 1909](https://www.catalog.update.microsoft.com/Search.aspx?q=4517389) |

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge documentation](./index.yml)