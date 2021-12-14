---
title: "Learn how to configure initial preferences on Microsoft Edge."
ms.author: collw
author: AndreaLBarr
manager: srugh
ms.date: 07/27/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Learn how to configure initial preferences on Microsoft Edge."
---

# Configure Microsoft Edge using Initial Preferences settings for the first run

Use the information in this article to configure Microsoft Edge Initial Preferences settings on your Windows devices.

> [!Note]
> This article applies to Microsoft Edge version 93 or later.

## Configure policy settings on Windows

Starting Microsoft Edge release 93, Microsoft supports a limited number of Initial Preferences, formerly named “Master Preferences”, to help admins configure browsers for the first run. For more information, see the supported settings in the following [Preference settings](#preference-settings) table.

When deployed, Initial Preferences act as the default browser settings on managed devices. These preferences are the settings preferred by admins to be used as default browser settings for the first run.

> [!NOTE]
> Initial preferences can be changed by users and aren't available for some devices because they aren't joined to an Active Directory® domain.

Some examples of initial preferences settings include initial configuration of a default homepage or tabs with specific URLs.

Preferences are only copied once from the *initial_preferences* file, changes made to this file after configuration won't be respected. If a setting is managed by a [Microsoft Edge policy](/deployedge/microsoft-edge-policies) and configured in the *initial_preferences file*, the policy always takes precedence.

### Preference settings

The following table shows the settings that are currently supported by Microsoft Edge.

| Preferences Category | Setting |
| - | - |
| Bookmark_bar | show_apps_shortcut<br>show_managed_bookmarks<br>show_on_all_tabs |
| Bookmarks | editing_enabled |
| Browser / clear_data | browsing_history<br>browsing_history_basic"<br>cache<br>cache_basic<br>cookies<br>download_history<br>form_data<br>passwords |
| History | browsing_history<br>cache<br>cookies<br>download_history<br>form_data<br>hosted_apps_data<br>passwords<br>site_settings |
| Browser | first_run_tabs<br>dark_theme<br>show_toolbar_bookmarks_button<br>show_toolbar_collections_butto<br>show_toolbar_downloads_button<br>show_home_button<br>show_prompt_before_closing_tabs<br>show_toolbar_history_button |
| default_search_provider | [default_search_provider] enabled |
| Fullscreen | Allowed |
| homepage | Homepage_url |
| homepage_is_newtabpage | homepage_is_newtabpage |
| Session | restore_on_startup<br>startup_urls |
| Extensions | Extensions: settings |

## 1: Download an example initial_preferences file

To get started, download the "Policy" file from the [Microsoft Edge Enterprise landing page](/edge/business/download). Extract the files in the download, and then open the *initial_preferences* file in the *examples* folder. The next screenshot shows the policy file options that are available to download

:::image type="content" source="media/initial-preferences-support-on-microsoft-edge-browser/edge-policy-files.png" alt-text="Microsoft Edge policy files available for download.":::

## 2: Customize and validate the initial_preferences file

Customize the preferences settings in the downloaded *initial_preferences* file and validate the changes to make sure that there are no errors in the JSON code. If you find errors, check the syntax and structure of the *initial_preferences* file, make corrections, and check it again. Few example tools to validate JSON, Online [JSON Tools](https://jsonformatter.org/) or [JSON editing in Visual Studio Code](https://code.visualstudio.com/docs/languages/json).

## 3: Deploy preferences to users' computer

Deploy the *initial_preferences* file to users' devices at the same time as Microsoft Edge is deployed and put the file in the following location on the device.

### Windows (AMD64 and ARM64)

| Channel | Location |
| - | - |
| Stable | `"C:\Program Files (x86)\Microsoft\Edge\Application"` |
| Beta | `"C:\Program Files (x86)\Microsoft\Edge Beta\Application"` |
|Canary | `"%LOCALAPPDATA%\Microsoft\Edge SxS\Application"` |
| Dev | `"C:\Program Files (x86)\Microsoft\Edge Dev\Application"` |

> [!NOTE]
> The *initial_preferences* file needs to be deployed to the same folder as the *msedge.exe* file on users' Windows computers.  

### macOS

| Channel | Location |
| - | - |
| Stable | `"~/Library/Application Support/Microsoft Edge/Microsoft Edge Initial Preferences"` |
| Beta | `“~/Library/Application Support/Microsoft Edge Beta/Microsoft Edge Initial Preferences"` |
| Canary | `“~/Library/Application Support/Microsoft Edge Canary/Microsoft Edge Initial Preferences"` |
| Dev | `"~/Library/Application Support/Microsoft Edge Dev/Microsoft Edge Initial Preferences"` |

## Important notes: MSI / Pkg Deployment and *initial_preferences* interaction

Initial preferences will only take effect after the *initial_preferences* file is deployed before the browser's first run by the end users.  

## See also

- [The *initial_prefrences* example template file](/edge/business/download)
