---
title: "Access the old version of Microsoft Edge"
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 08/17/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Learn how to access the legacy version of Microsoft Edge."
---

# Access Microsoft Edge Legacy after installing the new version of Microsoft Edge

Learn how to access Microsoft Edge Legacy after installing the new version of Microsoft Edge.

> [!NOTE]
> This article applies to the Microsoft Edge [Stable channel](microsoft-edge-channels.md).

While most organizations will want to replace Microsoft Edge Legacy with the new version, there are some situations where users will need access to both versions. For example:

- Helpdesk and support staff who interact with users who are using either or both versions of Microsoft Edge.
- Developers who support customers who are using either or both versions of Microsoft Edge.

> [!IMPORTANT]
> Running Microsoft Edge Legacy side-by-side with the new version of Microsoft Edge is not recommended for use in production. This configuration should only be used in specific cases where testing with both browser versions is required.
>
> The Microsoft Edge Legacy desktop app will reach end of support on March 9, 2021 in favor of the new Microsoft Edge. This means that Microsoft Edge Legacy will not receive security updates after that date. This change is applicable to all experiences that run in the Microsoft Edge Legacy desktop app. [Learn more](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).

## Before you begin
> [!NOTE]
> Starting with Windows 10 version 20H2 Microsoft Edge Legacy is no longer included. Starting with this version of Windows 10 the side-by-side experience is not supported.

The procedures in this article apply to systems that have been updated with the latest security updates. When the new version of Microsoft Edge is installed, the old version (Microsoft Edge Legacy) will be hidden. By default, all attempts to launch the old version will redirect the user to the newly installed version of Microsoft Edge. This article describes how you can keep using Microsoft Edge Legacy after you install Microsoft Edge.

## Quickstart: Side-by-side experience with Microsoft Edge Beta Channel and Microsoft Edge Legacy

Before using the detailed instructions in this article, consider the following two steps to let your users run Microsoft Edge Legacy and the Microsoft Edge [Beta channel](microsoft-edge-channels.md) side-by-side.

1. Prevent the automatic install of the Stable Channel of Microsoft Edge by [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq).

   > [!TIP]
   > Use the [Blocker Toolkit](microsoft-edge-blocker-toolkit.md) to disable automatic delivery of Microsoft Edge.

2. Install the [Beta channel](https://www.microsoft.com/edge/business/download) of the new version of Microsoft Edge.

   > [!NOTE]
   > Read [Additional information](#additional-information) for information about Registry Key settings.

This side-by-side solution is less complex and requires less management than the detailed solution described in this article. However, this solution does mean that you'll be running the Beta Channel rather than the Stable Channel.

## Side-by-side experience with Microsoft Edge Stable Channel and Microsoft Edge Legacy

Installing the Stable Channel of the next version of Microsoft Edge at the system-level will cause the current version (Microsoft Edge Legacy) to be hidden. If you want to let your users see both versions of Microsoft Edge side by side in Windows, you can enable this experience by setting the **Allow Microsoft Edge Side by Side browser experience** group policy to **Enabled**.

This group policy is documented [here](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)

### To set up the side-by-side browser experience policy:

1. Install the Policy Definitions from [Microsoft Edge for Business](https://www.microsoft.com/edge/business/download).

   - Pick the CHANNEL/BUILD and PLATFORM you want to use, and then click GET POLICY FILES.
   - Extract the zipped files.
   - Copy msedge.admx and msedgeupdate.admx to the `C:\Windows\PolicyDefinitions` directory.
   - Copy msedge.adml and msedgeupdate.adml (from the appropriate language/locale directory) to the `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]` directory.

2. Open the Group Policy Editor (gpedit.msc).
3. Under **Computer Configuration**, go to *Administrative Templates>Microsoft Edge Update>Applications*.

    > [!NOTE]
    > If you don't see the *Microsoft Edge Update* folder, verify that step 1 was completed correctly.

4. Under **Applications**, double-click "Allow Microsoft Edge Side by Side browser experience". See our [best practice guidance](#best-practice-guidance) before continuing to the next step.

    > [!NOTE]
    > By default, this group policy is set to "Not configured", which results in Microsoft Edge Legacy being hidden when the new version of Microsoft Edge is installed.

5. Select **Enabled** and then click **OK**.  

Setting this policy will set the following Registry Key  to '00000001':

- Key: `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate`
- Value Name: `Allowsxs`
- Value Type: `'REG_DWORD'`

#### Best practice guidance

For the best experience, the **Allow Microsoft Edge Side by Side browser experience** should be enabled before the new version of Microsoft Edge is deployed to your users' devices.

If the group policy is enabled after Microsoft Edge is deployed, there are the following side effects and required actions:

1. **Allow Microsoft Edge Side by Side browser experience** won't take effect until after the installer for the new version of Microsoft Edge is run again.

   > [!NOTE]
   > The installer can be run directly or automatically when the new version of Microsoft Edge updates.

2. Microsoft Edge Legacy will need to be re-pinned to Start or the Taskbar because the pin is migrated when the new version of Microsoft Edge is deployed.
3. Sites that were pinned to Start or the Taskbar for Microsoft Edge Legacy will be migrated to the new version of Microsoft Edge.

## Additional information

After the systems are fully updated and the Stable channel of the next version of Microsoft Edge is installed, the following registry key and value is set:

- Key: `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}`
- Key value: `BrowserReplacement`

  > [!IMPORTANT]
  > This key is over-written every time the Microsoft Edge Stable channel is updated. As a best practice, we recommend that you DO NOT delete this key to allow users to access both versions of Microsoft Edge.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Windows updates to support Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md)
