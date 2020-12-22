---
title: "Configure Microsoft Edge kiosk mode"
ms.author: aguta
author: aguta
manager: srugh
ms.date: 12/22/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Configure Microsoft Edge kiosk mode"
---

# Configure Microsoft Edge kiosk mode

This article describes how to configure Microsoft Edge kiosk mode options that you can pilot. There's also a roadmap of features we're targeting.

> [!NOTE]
> This article applies to Microsoft Edge version 87 or later.

## Overview

Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers. The following lockdown experiences are available:  

- The Digital/Interactive signage experience displays a specific site in full-screen mode.
- The public-browsing experience runs a limited multi-tab version of Microsoft Edge.

Both experiences are running a Microsoft Edge InPrivate session, which protects user data.

## Set up Microsoft Edge kiosk mode

An initial set of kiosk mode features is now available to test with Microsoft Edge Canary Channel, version 87. You can download Microsoft Edge Canary from the [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) page.

### Kiosk mode supported features

The following table lists the features supported by kiosk mode.

|Feature|Digital\Interactive Signage|Public browsing|Available with Microsoft Edge version (and higher)|
|-|-|-|-|
|InPrivate Navigation|Y|Y|87|
|Reset on inactivity|Y|Y|87|
|[Read only address bar](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (policy) |N|Y |87|
|[Delete downloads on exit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (policy)  | Y|Y |87 |
|Initial set of lockdown functionalities (F11, F12, and etc.)  |Y |Y | 87|
| Multi tab support | N| Y| 87|
|End session button | N| Y| 88|
|Shortcuts (Accelerators blocked):<br>- CTRL+N<br> - CTRL+T<br> - edge://settings<br>- Other shortcuts | <br>Y<br>N<br>Y<br>Y |<br>Y<br>Y<br>Y<br>Y |<br>89 |
|The "…" settings menu will display only the required options  |N |Y |89 |

> [!NOTE]
> As kiosk mode evolves, more features will be available.

## Use kiosk mode features

You can invoke Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:

- Kiosk mode Digital/Interactive signage: `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- Kiosk mode public browsing: `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

### Additional command line options

- `--no-first-run` : Disable the first Microsoft Edge run experience.
- `--kiosk-idle-timeout-minutes` : Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session. The following values are supported:

  - Default values
    - Full screen - turned off
    - Public browsing - 5 minutes
  - Allowed values
    - 0 - turns off the timer
    - 1-1440 minutes for reset on idle timer

## Support policies for kiosk mode

Use any of the Microsoft Edge policies listed in the following table to enhance the kiosk experience for the Microsoft Edge kiosk mode type you configure. To learn more about these policies, see [Microsoft Edge – Browser policy reference](https://docs.microsoft.com/deployedge/microsoft-edge-policies).

|Group policy|Digital\Interactive signage|Public browsing single-app|
|--|--|--|
|[Printing](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printing-policies) | Y|Y |
|[HomePageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation) |N | Y|
|[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton) |N | Y|
|[NewTabPageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) |N |Y |
|[FavoritesBarEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled) |N |Y |
|[UrlAllowList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) |Y |Y |
|[UrlBlockList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) |Y | Y|
|[ManagedSearchEngines](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedsearchengines) |N | Y|
|[UserFeedbackAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed) |N | Y|
|[VerticalTabsAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#verticaltabsallowed) | N|Y |
|[SmartScreen settings](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreen-settings-policies) |Y |Y |

## Microsoft Edge with assigned access

### Single app kiosk

Microsoft Edge currently supports a subset of the same Microsoft Edge Legacy kiosk mode types for single-app assigned access with the following lockdown experiences, Digital/Interactive signage, and Public-browsing.  

Kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), version 87.0.644.4 or higher.

**How do I get the Windows Insiders preview?**

To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).

### Multi-app kiosk

Microsoft Edge can be run with [multi-app assigned access](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing" kiosk mode type. To configure Microsoft Edge with multi-app assigned access, follow the instructions on how to [Set up a multi-app kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps). (The AUMID for the Microsoft Edge Stable channel is **MSEdge**).

Configure Microsoft Edge kiosk mode When using Microsoft Edge with multi-app assigned access you can use the [Microsoft Edge browser policies](https://review.docs.microsoft.com/en-us/DeployEdge/microsoft-edge-policies) to configure the browsing experience to meet your unique requirements.

### Configure using Windows Settings

Windows Settings is the simplest way to set up one or two single-app kiosk devices. Use the following steps to set up a single-app kiosk computer.

1. Install the latest Windows 10 Insider Preview, version 20215 or higher. Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).
2. Install the latest version of [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), 87.0.644.4 or higher.

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

13. Sign off from the kiosk device and sign in with the local kiosk account to validate the configuration.

## Functional limitations

With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.

Although kiosk mode doesn't currently support the following functionality, work is underway on the following features:

- Collections
- Extensions
- Internet Explorer mode
- Windows Defender Application Guard (WDAG)

We recommend that you turn off:

- [StartupBoostEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#startupboostenabled)
- [InternetExplorerIntegrationLevel](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [Extensions](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions-policies)

## Roadmap
<!--
### Later this year (2020)

We'll add the following features:

- End session button
- Read only address bar  
  - Configurable with group policy
  - When enabled, users will be prevented from editing the address bar and navigating to another page.

- More lockdown functions:

  - Additional accelerators will be blocked (for example, CTRL+N)
  - The "…" settings menu will enable only required options (for example, Print, Help,  Feedback, and Read aloud)
  - Additional *edge://* pages lockdown (for example, *edge://settings*)
  - Configure print options UI
  - Limiting file explorer to the download folder only. -->

### In early 2021

We'll add the following support and features:

- General availability of Microsoft Edge kiosk mode with assigned access single app on Windows.
- Additional features for parity with Microsoft Edge Legacy.
- Integration with Intune to configure devices using kiosk mode profile UX.
- Additional accelerators will be blocked.
- Restrict the launch of other applications from the browser.

## See also

- [Configure kiosks and digital signs on Windows desktop editions](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Deploy Microsoft Edge Legacy kiosk mode](https://aka.ms/edgekioskmode)
- [Plan your deployment of Microsoft Edge](deploy-edge-plan-deployment.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
