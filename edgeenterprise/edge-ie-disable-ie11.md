---
title: "Disable Internet Explorer 11"
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 04/20/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Learn how to disable Internet Explorer 11 and use Internet Explorer mode in Microsoft Edge."
---

# Disable Internet Explorer 11

This article describes how to disable Internet Explorer 11 as a standalone browser in your environment.

## Prerequisites

The following Windows updates and Microsoft Edge software are required:

- Windows updates

  - Windows 10, version 2004, Windows Server version 2004, Windows 10, version 20H2: [KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b) or later
  - Windows 10 version 1909, Windows Server version 1909: [KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) or later
  - Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019: [KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) or later
  - Windows 10, version 1607, Windows Server 2016: [KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) or later
   - Windows 10 initial version (July 2015): [KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) or later
  - Windows 8.1: [KB4601384](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) or later
  - Windows Server 2012: [KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) or later
  
- Microsoft Edge Stable Channel


## Overview

For organizations that require Internet Explorer 11 (IE11) for legacy compatibility, Internet Explorer mode (IE mode) on Microsoft Edge provides a seamless, single browser experience. Users can access legacy applications from within Microsoft Edge without having to switch back to IE11.

After you configure IE mode, you can disable IE11 as a standalone browser **without affecting IE mode functionality** across your organization using group policy.

> [!NOTE]
> If you need the standalone IE11 app for specific sites, and want to redirect all other browser traffic to Microsoft Edge, you can configure the [Send all sites not included in the site list to Microsoft Edge](./edge-ie-mode-policies.md#redirect-sites-from-ie-to-microsoft-edge) policy to redirect sites from IE to Microsoft Edge.

## User experience after redirecting traffic to Microsoft Edge

When you enable the **Disable Internet Explorer 11 as a standalone browser** policy, all IE11 activity is redirected to Microsoft Edge and users have the following experience:

- The IE11 icon on the Start Menu will be removed, but the one on the taskbar will remain.
- When users try to launch shortcuts or file associations that use IE11, they will be redirected to open the same file/URL in Microsoft Edge.
- When users try to launch IE11 by directly invoking the iexplore.exe binary, Microsoft Edge will launch instead.

As part of setting the policy for this experience, you can optionally show a redirect message for each user who tries to launch IE11. This message can be set to display "Always" or "Once per user". By default, the redirect message shown in the next screenshot is never shown.

:::image type="content" source="media/edge-ie-disable-ie11/disable-ie-redirect-msg.png" alt-text="Alert when trying to open IE after when a redirect to Microsoft Edge is active.":::

If your Enterprise Mode Site List contains applications that are configured to open in the IE11 app and you disable IE11 with this policy, they will open in IE mode on Microsoft Edge.
> [!NOTE]
> There was a known issue with the user flow when a site is configured to open in the IE11 application and the disable IE11 policy is set. The issue has been fixed in Microsoft Edge versions 91.0.840.0 or later.

## Disable Internet Explorer 11 as a standalone browser

To disable Internet Explorer 11 using group policy, follow these steps:

1. Ensure you have the pre-requisite operating system updates. This step will update the ADMX files on your machine directly (specifically inetres.adml and inetres.admx). Please note that if you want to update your Central Store, you will need to copy over the .adml and .admx files from a machine that has the pre-requisite updates. For more information, see [Create and manage Central Store](/troubleshoot/windows-client/group-policy/create-and-manage-central-store)
2. Open the Group Policy Editor.
3. Go to ***Computer Configuration/Administrative Templates/Windows Components/Internet Explorer***. 
4. Double-click **Disable Internet Explorer 11 as a standalone browser**.
5. Select **Enabled**.
6. Under **Options**, pick one of the following values:

   - **Never** if you don’t want to notify users that IE11 is disabled.
   - **Always** if you want to notify users every time they're redirected from IE11.
   - **Once per user** if you want to notify users only the first time they are redirected.

7. Click **OK** or **Apply** to save this policy setting.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [About IE mode](./edge-ie-mode.md)
- [Additional Enterprise Mode information](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
