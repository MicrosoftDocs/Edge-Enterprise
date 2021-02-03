---
title: "Microsoft Edge kiosk transition plan"
ms.author: aguta
author: aguta
manager: srugh
ms.date: 02/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Create a transition plan for Microsoft Edge kiosk"
---

# Create a transition plan for a Microsoft Edge kiosk

This article provides guidance on how to transition your kiosk from Microsoft Edge Legacy to Microsoft Edge.  

> [!NOTE]
> This article applies to Microsoft Edge Stable, Beta and Dev Channels, version 87 or later.

> [!IMPORTANT]
> When support ends for Microsoft Edge Legacy on March 9, 2021, this out of support desktop application will be removed and replaced with the new release of Microsoft Edge as part of the Windows Update Tuesday (or “B”) release on April 13, 2021. Because of this, you will need to set up a new kiosk in Microsoft Edge.

## Kiosk setup options

You have two options for setting up a kiosk.

- Option 1 (Recommended): Download and install the new version of Microsoft Edge and set up kiosk mode before to applying the Windows 10 Update Tuesday (or “B”) release to your devices on or after April 13, 2021.
- Option 2: After you apply the Windows 10 Update Tuesday (or “B”) release on or after April 13, 2021, Microsoft Edge Legacy, and its kiosk, will no longer be available. You will need to set up a kiosk in Microsoft Edge to run kiosk scenarios. With this option, you will experience a disruption in your kiosk environment—which is why we strongly recommend Option 1.  

## Kiosk setup steps

Use the following steps as a guide  to set up a kiosk in Microsoft Edge.

**Step 1: Evaluate your needs against released (and upcoming) kiosk mode functionality.** The following table lists the features supported by kiosk mode in Microsoft Edge and Microsoft Edge Legacy. Use this table as a guide to transitioning to Microsoft Edge by comparing how these features are supported in both releases of Microsoft Edge.

|Feature|Digital\Interactive Signage|Public browsing|Available with Microsoft Edge version (and higher)|
|-|-|-|-|
|InPrivate Navigation|Y|Y|87|
|Reset on inactivity|Y|Y|87|
|[Read only address bar](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (policy) |N|Y |87|
|[Delete downloads on exit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (policy)  | Y|Y |87|
|F11 blocked (enter/exit full-screen) | Y | Y | 87 |
|F12 blocked (launch Developer Tools) | Y | Y | 87 |
| Multi tab support | N| Y| 87|
|End session button | N| Y| 88|
|All internal Microsoft Edge URLs are blocked, except for *edge://downloads* and *edge://print* |N|Y|88|
| CTRL+N blocked (open a new window) | Y | Y | 89 |
| CTRL+T blocked (open new tab) | N | Y | 89 |
|Settings and more (...) will display only the required options  |N |Y |89 |
> [!NOTE]
> For information about the Microsoft Edge release schedule, see [Microsoft Edge release schedule](microsoft-edge-release-schedule.md).

**Step2: Test the new kiosk in Microsoft Edge.** We recommend that you test setting up kiosk mode in Microsoft Edge. A quick and easy way to test kiosk mode is to configure an assigned access single app using Windows Settings as described next.

1. Install the latest Windows 10 Insider Preview, version 20215 or higher. Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).
2. Install the latest version of [Microsoft Edge Stable channel](https://www.microsoft.com/edge), version 87 or higher.  To test the latest features, you can download the latest [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), version 89 or higher.

   > [!IMPORTANT]
   > Because a device level installation is required, only a non-Canary channel is supported.

3. On the kiosk computer, open Windows Settings, and type "kiosk" in the search field. Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Set up kiosk with assigned access":::

4. On the **Set up a kiosk** page, click **Get started**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Kiosk page -get started":::

5. Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Kiosk mode - create account":::

6. On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.

   > [!NOTE]
   > This only applies to Microsoft Edge Dev, Beta, and Stable channels.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Kiosk mode - choose an app":::

7. Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:

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


**Step 3: Develop a transition plan.** Based on your testing and organizational needs, we recommend developing a transition plan and moving to the new version of Microsoft Edge before to support ends for Microsoft Edge Legacy on March 9, 2021.  

## Scenarios that require you to recreate an existing kiosk

If you update to Windows 10, version 20H2, the new version of Microsoft Edge will be installed and Microsoft Edge Legacy will be hidden and not usable. If so, you will need to set up a new kiosk as we've described.

## How to get help

A kiosk might be an important part of your everyday business, so we want to help make this transition as smooth as possible. If your business needs help with the transition, Microsoft Edge support from Microsoft is available. Additionally, if you experience site or app compatibility issues, get no-cost help using [App Assure](https://fasttrack.microsoft.com/portal). The App Assure compatibility promise is: if your web apps or sites work on Internet Explorer 11, supported versions of Google Chrome, or any version of Microsoft Edge, they'll work with the new version of Microsoft Edge.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)