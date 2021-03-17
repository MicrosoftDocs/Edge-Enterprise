---
title: "Configure Microsoft Edge kiosk mode"
ms.author: aguta
author: aguta
manager: srugh
ms.date: 03/16/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Learn about kiosk mode features and how to configure Microsoft Edge kiosk mode options."
---

# Configure Microsoft Edge kiosk mode

This article describes how to configure Microsoft Edge kiosk mode options that you can pilot. There's also a roadmap of features we're targeting.

> [!NOTE]
> This article applies to Microsoft Edge version 87 or later.

> [!IMPORTANT]
> Invoke Microsoft Edge kiosk mode features on Windows 10 using the command line arguments provided in [Use kiosk mode features](#use-kiosk-mode-features).

## Overview

Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers. The following lockdown experiences are available:  

- **Digital/Interactive Signage** experience - Displays a specific site in full-screen mode.
- **Public-Browsing** experience - Runs a limited multi-tab version of Microsoft Edge.

Both experiences are running a Microsoft Edge InPrivate session, which protects user data.

## Set up Microsoft Edge kiosk mode

An initial set of kiosk mode features is available to test with Microsoft Edge Stable Channel, version 87. You can download the latest version from [Microsoft Edge (Official Stable Channel)](https://www.microsoft.com/edge).

### Kiosk mode supported features

The following table lists the features supported by kiosk mode in Microsoft Edge and Microsoft Edge Legacy. Use this table as a guide to transitioning to Microsoft Edge by comparing how these features are supported in both versions of Microsoft Edge.

|Feature|Digital\Interactive Signage|Public browsing|Available with Microsoft Edge version (and higher)|Available with Microsoft Edge Legacy|
|-|-|-|-|-|
|InPrivate Navigation|Y|Y|89|Y|
|Reset on inactivity|Y|Y|89|Y|
|[Read only address bar](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (policy) |N|Y |89|N|
|[Delete downloads on exit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (policy)  | Y|Y |89|N|
|F11 blocked (enter/exit full-screen) | Y | Y | 89 |Y|
|F12 blocked (launch Developer Tools) | Y | Y | 89 |Y|
| Multi tab support | N| Y| 89|Y|
|[Allow URL support](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) (policy)|Y|Y|89|N|
|[Block URL support](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) (policy)|Y|Y|89|N|
|[Show home button](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showhomebutton) (policy)|N|Y|89|Y|
|[Manage favorites](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#managedfavorites) (policy)|N|Y|89|Y|
|[Enable printer](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printingenabled) (policy)|Y|Y|89|Y|
|[Configure the new tab page URL](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagelocation) (policy)|N|Y||Y|
|End session button * | N| Y| 89|Y|
|All internal Microsoft Edge URLs are blocked, except for *edge://downloads* and *edge://print* |N|Y|89|Y|
| CTRL+N blocked (open a new window) * | Y | Y | 89 |Y|
| CTRL+T blocked (open new tab) |Y | N | 89 |Y|
|Settings and more (...) will display only the required options  |Y |Y |89 |Y|
|Restrict the launch of other applications from the browser|Y|Y|90/91|Y|
|UI print settings lockdown|Y|Y|90/91|Y|
|[Set the new tab page as the home page](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepageisnewtabpage) (policy)|-|-|TBD|Y|

> [!NOTE]
> Features followed by "*" are only enabled in an assigned access single app scenario.

## Use kiosk mode features

Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options for Digital/Interactive signage and Public browsing.

### Kiosk mode Digital/Interactive signage
 
```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen
```

### Kiosk mode Public browsing

```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing
```

### Additional command line options

- **--no-first-run**: Disable the first Microsoft Edge run experience.

   ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --no-first-run
  ```

  ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --no-first-run
  ```

- **--kiosk-idle-timeout-minutes=**: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session. Replace "value" in the next example with the number of minutes.

   ```
   --kiosk-idle-timeout-minutes=value
   ``` 
   The following "values" are supported:

     - Default values (in minutes)
       - Full screen - 0 (turned off)
       - Public browsing - 5 minutes
    - Allowed values
      - 0 - turns off the timer
      - 1-1440 minutes for reset on idle timer


    ```
    msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --kiosk-idle-timeout-minutes=1
   ```

   ```
   msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --kiosk-idle-timeout-minutes=1
   ```

## Support policies for kiosk mode

Use any of the Microsoft Edge policies listed in the following table to enhance the kiosk experience for the Microsoft Edge kiosk mode type you configure. To learn more about these policies, see [Microsoft Edge – Browser policy reference](https://docs.microsoft.com/deployedge/microsoft-edge-policies).

> [!NOTE]
> Policy configuration isn't limited to the policies listed in the following table, however additional policies should be tested to ensure that kiosk mode functionality isn't negatively affected.

|Group policy|Digital\Interactive signage|Public browsing single-app|
|--|--|--|
|[Printing](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printing-policies) | Y|Y |
|[HomePageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation) |N | Y|
|[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton) |N | Y|
|[NewTabPageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) |N |Y |
|[FavoritesBarEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled) |N |Y |
|[URLAllowlist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) |Y |Y |
|[URLBlocklist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) |Y | Y|
|[ManagedSearchEngines](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedsearchengines) |N | Y|
|[UserFeedbackAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed) |N | Y|
|[VerticalTabsAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#verticaltabsallowed) | N|Y |
|[SmartScreen settings](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreen-settings-policies) |Y |Y |
|[EdgeCollectionsEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgecollectionsenabled)|Y|Y|

## Microsoft Edge with assigned access

### Single app kiosk

Microsoft Edge currently supports a subset of the same Microsoft Edge Legacy kiosk mode types for single-app assigned access with the following lockdown experiences: Digital/Interactive signage, and Public-browsing.  

Microsoft Edge kiosk mode with assigned access single app is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Beta Channel](https://www.microsoftedgeinsider.com/download), version 89 or higher.

**How do I get the Windows Insiders preview?**

To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).

### Multi-app kiosk

Microsoft Edge can be run with [multi-app assigned access](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing" kiosk mode type. To configure Microsoft Edge with multi-app assigned access, follow the instructions on how to [Set up a multi-app kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps). (The AUMID for the Microsoft Edge Stable channel is **Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe!MSEDGE**).

When using Microsoft Edge with multi-app assigned access, you can configure Microsoft Edge kiosk to use the[Microsoft Edge browser policies](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies) to configure the browsing experience to meet your unique requirements.

### Configure using Windows Settings

Windows Settings is the simplest way to set up one or two single-app kiosk devices. Use the following steps to set up a single-app kiosk computer.

1. Install the latest Windows 10 Insider Preview, version 20215 or higher. Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).
2. To test the latest features, you can download the latest [Microsoft Edge Beta channel](https://www.microsoftedgeinsider.com/download), version 89 or higher.
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

## Functional limitations

With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.

We currently don't support the following features and recommend that you turn off:

- [InPrivateModeAvailability](https://docs.microsoft.com/deployedge/microsoft-edge-policies#inprivatemodeavailability)
- [IsolateOrigins](https://docs.microsoft.com/deployedge/microsoft-edge-policies#isolateorigins)
- [ManagedFavorites](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedfavorites)
- [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgeshoppingassistantenabled)
- [EdgeCollectionsEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgecollectionsenabled)
- [UserFeedbackAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed)
- [DefaultPopupsSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultpopupssetting)
- [StartupBoostEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#startupboostenabled)
- [InternetExplorerIntegrationLevel](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [Extensions](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions-policies)
- [BackgroundModeEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#backgroundmodeenabled)
- [UserFeedbackAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed)

## Roadmap

### In early 2021

We'll add the following support and features:

- General availability of Microsoft Edge kiosk mode with assigned access single app on Windows 10 1909 and higher.
- Additional features for parity with Microsoft Edge Legacy.
- Integration with Intune to configure devices using kiosk mode profile UX.
- Restrict the launch of other applications from the browser.
- UI print settings lockdown.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Plan your deployment of Microsoft Edge](deploy-edge-plan-deployment.md)
- [Configure kiosks and digital signs on Windows desktop editions](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Plan your kiosk mode transition](microsoft-edge-kiosk-mode-transition-plan.md)
