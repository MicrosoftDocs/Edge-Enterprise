---
title: "Initial preferences support on Microsoft Edge browser"
ms.author: collw
author: AndreaLBarr
manager: srugh
ms.date: 07/20/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Initial preferences support on Microsoft Edge browser."
---

# Configure Microsoft Edge using Initial Preferences settings for the first run

Use the following information to configure Microsoft Edge Initial Preferences settings on your Windows devices.

> [!Note]
> This article applies to Microsoft Edge version 93 or later.

## Configure policy settings on Windows

Starting Microsoft Edge release 93, Microsoft supports a limited number of Initial Preferences, formerly named “Master Preferences”, to help admins configure browsers for the first run; see the list of the supported settings below.  

When deployed, Initial Preferences act as the default browser settings on managed devices; these are the settings that are preferred by admins to be used as default but can be changed by users or are not available for some devices as they are not joined to an Active Directory® domain.

Some examples of Intial Preferences settings include initial configuration of a default homepage or tabs with specific URLs.

Preferences are copied from initial_preferences file only once and any change made to this file after configuration will not be respected. If a setting is managed by a [Microsoft Edge policy](/deployedge/microsoft-edge-policies) and configured in the initial_preferences file, the policy always takes precedence.

Below is the list of preferences setting that are currently supported by Microsoft Edge:

| Preferences Category | Setting |
| - | - |
| Bookmark_bar | show_apps_shortcut<br>show_managed_bookmarks<br>show_on_all_tabs |
| Bookmarks | editing_enabled |
| Browser / clear_data | browsing_history<br>browsing_history_basic"<br>cache<br>cache_basic<br>cookies<br>download_history<br>form_data<br>passwords |
| History | browsing_history<br>cache<br>cookies<br>download_history<br>form_data<br>hosted_apps_data<br>passwords<br>site_settings |
| Browser | first_run_tabs<br>dark_theme<br>show_toolbar_bookmarks_button<br>show_toolbar_collections_butto<br>show_toolbar_downloads_button<br>show_home_button<br>show_prompt_before_closing_tabs<br>show_toolbar_history_button |
| default_search_provider | enabled<br>search_url |
| Fullscreen | Allowed |
| homepage | Homepage_url |
| homepage_is_newtabpage | true |
| incognito | mode_availability |
| Session | restore_on_startup<br>startup_urls |
| Extensions | Extensions : settings |

## 1: Download an example initial_preferences file

To get started, download the example *initial_preferences* file form this location the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download) **and** follow the steps below.

## 2: Customize and validate the initial_preferences file

Customize the preferences settings in the downloaded *initial_preferences* file and validate the changes to make sure that there are no errors in the JSON code. If you find errors, check the syntax and structure of the *initial_preferences* file, make corrections, and validate it again. Few example tools to validate JSON, Online [JSON Tools](https://jsonformatter.org/) or [JSON editing in Visual Studio Code](https://code.visualstudio.com/docs/languages/json).

## 3: Deploy / Push preferences to users' computer

Apply the *initial_preferences* file to users' devices at the same time as Microsoft Edge Browser is deployed and place the file in the following location on the device.

### Windows (AMD64 and ARM64)

| Channel | Location |
| - | - |
| Stable | `"C:\Program Files (x86)\Microsoft\Edge\Application"` |
| Beta | `"C:\Program Files (x86)\Microsoft\Edge Beta\Application"` |
|Canary | `"%LOCALAPPDATA%\Microsoft\Edge SxS\Application"` |
| Dev | `"C:\Program Files (x86)\Microsoft\Edge Dev\Application"` |

**Note**: The *initial_preferences* file needs to be added to the same folder as the msedge.exe file on users' Windows computers.  

### macOS

| Channel | Location |
| - | - |
| Stable: `"~/Library/Application Support/Microsoft Edge/Microsoft Edge Initial Preferences"` |
| Beta | `“~/Library/Application Support/Microsoft Edge Beta/Microsoft Edge Initial Preferences"` |
| Canary | `“~/Library/Application Support/Microsoft Edge Canary/Microsoft Edge Initial Preferences"` |
| Dev | `"~/Library/Application Support/Microsoft Edge Dev/Microsoft Edge Initial Preferences"` |

## Important notes: MSI / Pkg Deployment and *initial_preferences* interaction

The *initial_preferences* file can be placed and deployed in the above-mentioned directory before Microsoft Edge is installed through MSI / PKG file; i.e. Microsoft Edge browser can be installed and deployed later. The *initial_preferences* file would persist where it was deployed earlier, and the file would be read by Microsoft Edge in its first run after installation.
To apply Initial Preferences in cases that Microsoft Edge on Windows is preinstalled, IT admins shall configure and install the *initial_preferences* file, as instructed above, before users run the browser for the first time.

## See also

- [The *initial_prefrences* example template file](https://www.microsoft.com/edge/business/download)
