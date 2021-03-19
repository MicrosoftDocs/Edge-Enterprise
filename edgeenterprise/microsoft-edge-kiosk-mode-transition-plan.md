---
title: "Plan your kiosk mode transition"
ms.author: aguta
author: aguta
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Plan your kiosk mode transition"
---

# Plan your kiosk mode transition

This article provides guidance on how to transition your kiosk from Microsoft Edge Legacy to Microsoft Edge.  

> [!NOTE]
> This article applies to Microsoft Edge Stable, Beta and Dev Channels, version 87 or later.

> [!IMPORTANT]
> When support ends for Microsoft Edge Legacy on March 9, 2021, it will be removed and replaced with Microsoft Edge on Chromium as part of the Windows Update in April. For details, go to [this blog post](https://aka.ms/EdgeLegacyEOS). To continue to use your browser-based kiosk scenarios, you need to install Microsoft Edge on Chromium and set up kiosk mode prior to April’s Windows Update release to your device.

## Kiosk setup steps

Use the following steps as a guide to set up a kiosk in Microsoft Edge.

**Step 1: Evaluate your needs against released (and upcoming) kiosk mode functionality.** The following table lists the features supported by kiosk mode in Microsoft Edge on Chromium and Microsoft Edge Legacy. Use this table as a guide to transitioning to Microsoft Edge by comparing how these features are supported in both releases of Microsoft Edge.

|Feature|Digital\Interactive Signage|Public browsing|Available with Microsoft Edge version (and higher)|Available with Microsoft Edge Legacy|
|-|-|-|-|-|
|InPrivate Navigation|Y|Y|89|Y|
|Reset on inactivity|Y|Y|89|Y|
|[Read only address bar](./microsoft-edge-policies.md#kioskaddressbareditingenabled) (policy) |N|Y |89|N|
|[Delete downloads on exit](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) (policy)  | Y|Y |89|N|
|F11 blocked (enter/exit full-screen) | Y | Y | 89 |Y|
|F12 blocked (launch Developer Tools) | Y | Y | 89 |Y|
| Multi tab support | N| Y| 89|Y|
|[Allow URL support](./microsoft-edge-policies.md#urlallowlist) (policy)|Y|Y|89|N|
|[Block URL support](./microsoft-edge-policies.md#urlblocklist) (policy)|Y|Y|89|N|
|[Show home button](./microsoft-edge-policies.md#showhomebutton) (policy)|N|Y|89|Y|
|[Manage favorites](./microsoft-edge-policies.md#managedfavorites) (policy)|N|Y|89|Y|
|[Enable printer](./microsoft-edge-policies.md#printingenabled) (policy)|Y|Y|89|Y|
|[Configure the new tab page URL](./microsoft-edge-policies.md#newtabpagelocation) (policy)|N|Y||Y|
|End session button | N| Y| 89|Y|
|All internal Microsoft Edge URLs are blocked, except for *edge://downloads* and *edge://print* |N|Y|89|Y|
| CTRL+N blocked (open a new window) | Y | Y | 89 |Y|
| CTRL+T blocked (open new tab) |Y | Y | 89 |Y|
|Settings and more (...) will display only the required options  |Y |Y |89 |Y|
|Restrict the launch of other applications from the browser|Y|Y|90/91|Y|
|UI print settings lockdown|Y|Y|90/91|Y|
|[Set the new tab page as the home page](./microsoft-edge-policies.md#homepageisnewtabpage) (policy)|-|-|TBD|Y|

> [!NOTE]
> For information about the Microsoft Edge release schedule, see [Microsoft Edge release schedule](microsoft-edge-release-schedule.md).

**Step2: Test the new kiosk in Microsoft Edge.** We recommend that you test setting up kiosk mode in Microsoft Edge. A quick and easy way to test kiosk mode is to configure an assigned access single app using Windows Settings as described next.

1. Install the latest Windows 10 Insider Preview, version 20215 or higher. Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](/windows-insider/get-started).
2. Install the latest version of [Microsoft Edge Stable channel](https://www.microsoft.com/edge), version 87 or higher.  To test the latest features, you can download the latest [Microsoft Edge Beta channel](https://www.microsoftedgeinsider.com/download), version 89 or higher.

   > [!IMPORTANT]
   > Because a device level installation is required, the Canary channel isn't supported.

3. On the kiosk computer, open Windows Settings, and type "kiosk" in the search field. Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Set up kiosk with assigned access":::

4. On the **Set up a kiosk** page, click **Get started**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Kiosk page -get started":::

5. Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Kiosk mode - create account":::

6. On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Kiosk mode - choose an app":::

7. Select one of the following options for how Microsoft Edge displays when running in kiosk mode:

   - Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.
   - Public browser - Runs a limited multi-tab version of Microsoft Edge.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Kiosk mode display - full screen digital sign":::

8. Select **Next**.
9. Type the URL to load when the kiosk launches.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Kiosk mode - enter URL":::

10. Accept the default value of 5 minutes for the idle time or provide a value of your own.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Kiosk mode - enter idle time":::

11. Click **Next**.
12. Close the **Settings** window to save and apply your choices.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Kiosk mode - finish set up":::

13. Sign out from the kiosk device and sign in with the local kiosk account to validate the configuration.

**Step 3: Develop a transition plan.** Based on your testing and organizational needs, we recommend developing a transition plan and moving to Microsoft Edge on Chromium before support ends for Microsoft Edge Legacy on March 9, 2021.

## Additional scenarios that require you to recreate an existing kiosk mode

If you update to Windows 10, version 20H2, Microsoft Edge on Chromium will be installed, and Microsoft Edge Legacy will be hidden. In this instance, you will need to set up kiosk mode again in Microsoft Edge on Chromium.

## How to get help

Kiosk mode may be an important part of your everyday business, so we want to help make this transition as smooth as possible and help you avoid disruptions. If your business needs help transitioning to Microsoft Edge on Chromium:

- [Support](https://support.serviceshub.microsoft.com/supportforbusiness/create?sapId=a77ee9b7-b6b6-aa08-d7b9-887ebe228207) is available from Microsoft. 
- [FastTrack support](https://www.microsoft.com/fasttrack/microsoft-365/microsoft-edge?rtc=1) is also available at no additional charge to customers with 150 or more paid seats of Windows 10 Enterprise.
- [App Assure](https://www.microsoft.com/en-us/fasttrack/microsoft-365/app-assure) is available if you experience site or app compatibility issues.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [New Microsoft Edge to replace Microsoft Edge Legacy with April’s Windows 10 Update Tuesday release](https://techcommunity.microsoft.com/t5/microsoft-365-blog/new-microsoft-edge-to-replace-microsoft-edge-legacy-with-april-s/ba-p/2114224)