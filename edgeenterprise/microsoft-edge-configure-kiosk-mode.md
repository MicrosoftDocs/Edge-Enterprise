---
title: "Configure Microsoft Edge kiosk mode"
ms.author: aguta
author: aguta
manager: srugh
ms.date: 09/18/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Configure Microsoft Edge kiosk mode"
---

# Configure Microsoft Edge kiosk mode

This article describes how to configure Microsoft Edge kiosk mode options that you can pilot. There's also a roadmap of features we are targeting.

> [!NOTE]
> This article applies to Microsoft Edge version 87 or later.

For information about Microsoft Edge Legacy kiosk mode (version 45 and earlier) see [Deploy Microsoft Edge kiosk mode](https://aka.ms/edgekioskmode).

## Overview

Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers. The following lockdown experiences are available:  

- The full-screen experience displays a specific site in full-screen mode.
- The public-browsing experience runs a limited multi-tab version of Microsoft Edge.

Both experiences are running a Microsoft Edge InPrivate session, which protects user data.

## Set up Microsoft Edge kiosk mode  

An initial set of kiosk mode features are now available to test with Microsoft Edge Canary Channel, version 87. You can download Microsoft Edge Canary from the [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) page.

### Kiosk mode features

The following features are available:

- InPrivate navigation. Protects a user's data by deleting browser data and downloads when the session ends.
- Reset a user's session after a certain period of inactivity.
- Initial set of lockdown functionality. The following functions are available:

  - Mouse context menu
  - F12 Developer Tools
  - F11 Exit full screen
  - Blocking of the initial set of *Edge://* pages

> [!NOTE]
> As kiosk mode evolves, more features will be available.

### Use kiosk mode features

You can invoke Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:

- Kiosk mode full screen: `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- Kiosk mode public browsing: `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

#### Additional command line options

- `--no-first-run` : Disable the first run experience.
- `--kiosk-idle-timeout-minutes` : Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session. The following values are supported:

  - Default values
    - Full screen - 5 minutes
    - Public browsing - turned off
  - Allowed values
    - 0 - No idle timer
    - 1-1440 minutes for reset on idle timer

## Set up kiosk mode with assigned access

Microsoft Edge kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build in the Dev Channel](https://docs.microsoft.com/windows-insider/get-started).

**How do I get the Windows Insiders preview?**

To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/en-us/windows-insider/get-started).

### Configure using Windows Settings

Windows Settings is the simplest way to set up one or two single-app kiosk devices. Use the following steps to set up a single-app kiosk computer.

1. On the kiosk computer, open Windows Settings, and type "kiosk" in the search field. Select **Set up a kiosk (assigned access)**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="Set up kiosk with assigned access":::

2. On the **Set up a kiosk** page, click **Get started**. [insert screenshot].

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Kiosk page -get started":::

3. Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**. 

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Kiosk mode - create account":::

4. On the **Choose a kiosk app** page, select **Microsoft Edge*** and then click **Next**.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Kiosk mode - choose an app":::

5. Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:

   - Full screen - Displays a specific site in full-screen mode, running Microsoft Edge.

     :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Kiosk mode display - full screen digital sign":::

   - Public browser - Runs a limited multi-tab version of Microsoft Edge.

      :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5b-public-browser.png" alt-text="Kiosk mode display - public browser":::

6. Select **Next**.
7. Type the URL to load when the kiosk launches.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Kiosk mode - enter URL":::

8. Accept the default value of 5 minutes for the idle time or provide a value of your own.

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Kiosk mode - enter idle time":::

9. Click **Next**.
10. Close the **Settings** window to save and apply your choices.

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Kiosk mode - finish set up":::

11. Restart the kiosk computer and sign in with the local kiosk account to validate the configuration.

## Functional limitations and known issues

With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.

Currently, kiosk mode doesn't provide the following functionality:  

- Extensions
- Internet Explorer mode  
- Windows Defender Application Guard (WDAG)

We are currently working on improving the following issues:  

## Roadmap

### Later this year (2020)

We'll add the following features:

- End session button
- More lockdown functions:
  - Additional accelerators will be blocked (for example, CTRL+N)  
  - Limiting file explorer to the download folder only  

### In early 2021

We'll add the following support and features:

- General availability of Microsoft Edge kiosk mode with assigned access single app on Windows.
- Additional features for parity with Microsoft Edge Legacy.
- Integration with Intune to configure devices using kiosk mode profile UX.

## See also

- [Configure kiosks and digital signs on Windows desktop editions](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Deploy Microsoft Edge Legacy kiosk mode](https://aka.ms/edgekioskmode) 
- [Plan your deployment of Microsoft Edge](deploy-edge-plan-deployment.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)