---
title: "Initial preferences support on Microsoft Edge browser"
ms.author: collw
author: AndreaLBarr
manager: srugh
ms.date: 07/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Initial preferences support on Microsoft Edge browser."
---

# Initial preferences support on Microsoft Edge browser

Microsoft Edge, supports initial_preferences from stable release 93. As an admin, one can use initial preferences to deploy default preferences to Microsoft Edge browser users; on managed computers. These preferences are applied when users first open the Microsoft Edge browser. For example, one can set the homepage or choose which tabs and URLs are shown when they open the Microsoft Edge browser. Preferences are copied from initial_preferences file only once. Changes to the initial_preferences file made after that are not respected.  

## When to use initial preferences

Use Initial Preferences to:  

- Configure default settings that users can change later.

- Deploy settings that you do not want to manage, or are not available, with a [Microsoft Edge policy](/deployedge/microsoft-edge-policies).

Apply settings to Microsoft® Windows® computers that are not joined to an Active Directory® domain.

To apply settings that you don’t want users to change, but enforced [Microsoft Edge policies](/deployedge/microsoft-edge-policies) on Windows or Mac computers instead.

If a setting is managed by a [Microsoft Edge policy](/deployedge/microsoft-edge-policies) and configured in the initial_preferences file, the policy takes precedence and users cannot edit the setting.

## Configure Microsoft Edge using Initial Preferences settings for the first run [linked to the page]

*The file named “initial_preferences” will replace the “master_preferences” file in the near future; therefore, "Initial Preferences" is used instead of "Master Preferences" here.*

*Initial_preferences can be deployed as default preferences on managed devices when users first open the browser. These settings can be used for the following scenarios:*  

- *settings that are not available for the users*

- *settings that do not need to be managed by admins and can be changed by users later*

- *settings that are used to customize browser for devices that are not joined to an Active Directory® domain.*

*Some examples include initial configuration of the default homepage or the tabs with specific URLs for the browser.*

*Most of the initial references are linked to their associated policies. The policy configuration always takes precedence when a setting is configured in both initial preferences file AND is managed by a policy.*

*Microsoft supports a limited number of initial preferences to help admins configure and make the browser ready for the first run; see the list of the supported settings [LINKED].  To get started, follow the steps below.*

## 1: Download an example initial_preferences file

Microsoft supports a limited number of initial preference settings to help admins configure and make the browser ready for the first run; Below is the list of preferences setting that are supported. To get started, download the example initial_preferences file form this location <[Local Link to File](https://microsoft.sharepoint.com/teams/Edge/Documents/Forms/AllItems.aspx?id=%2Fteams%2FEdge%2FDocuments%2FEnterprise%2Fpolicy%5Ftemplates%2FMaster%20Preferences%20Demo%2Finitial%5Fpreferences&parent=%2Fteams%2FEdge%2FDocuments%2FEnterprise%2Fpolicy%5Ftemplates%2FMaster%20Preferences%20Demo&p=true&originalPath=aHR0cHM6Ly9taWNyb3NvZnQuc2hhcmVwb2ludC5jb20vOnU6L3QvRWRnZS9FV1IxWms0VFdWUkN1Sm1tUWs3eXBzSUJRRkJhWkt5aW5OLTJnMTR1ZU1oRGpBP3J0aW1lPVBJSzJjRjFDMlVn)> and follow the steps below.

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
| Session | restore_on_startup<br>startup_urls 
| Extensions | Extensions : settings |

## 2: Customize and validate the initial_preferences file

Customize with your preferences in the downloaded initial_preferences file.  Validate your customized initial_preferences file to make sure that there are no errors in the JSON code. If you find errors, check the syntax and structure of the initial_preferences file, make corrections, and validate it again. Few example tools to validate JSON, Online [JSON Tools](https://jsonformatter.org/) or [JSON editing in Visual Studio Code](https://code.visualstudio.com/docs/languages/json).

## 3: Deploy / Push preferences to users' computer

Apply the initial_preferences file to users' computers at the same time as Microsoft Edge Browser is deployed and any policies are applied. Place the initial_preferences file in the following location on the device.

### Location for initial_preferences file for Windows (AMD64 and ARM64) is:

Stable: C:\Program Files (x86)\Microsoft\Edge\Application 
Beta: C:\Program Files (x86)\Microsoft\Edge Beta\Application 
Canary: %LOCALAPPDATA%\Microsoft\Edge SxS\Application 
Dev: C:\Program Files (x86)\Microsoft\Edge Dev\Application 
**Note**: The initial_preferences file needs to be added to the same folder as the msedge.exe file on users' Windows computers.  

### Location for initial_preferences file for macOS:

Stable: "~/Library/Application Support/Microsoft Edge/Microsoft Edge Initial Preferences"   
Beta: “~/Library/Application Support/Microsoft Edge Beta/Microsoft Edge Initial Preferences" 
Canary: “~/Library/Application Support/Microsoft Edge Canary/Microsoft Edge Initial Preferences" 
Dev: "~/Library/Application Support/Microsoft Edge Dev/Microsoft Edge Initial Preferences" 

## Tip: MSI / Pkg Deployment and initial_preferences interaction

Before Microsoft Edge is installed through MSI / PKG file, initial_preferences file can be placed / deployed in the above-mentioned directory.
Microsoft Edge browser can be installed / deployed later. The initial_preferences file would persist where it was deployed earlier, and the file would be read by Microsoft Edge in its first run after installation.

On preinstalled Microsoft Edge version on Windows, before the first run of the browser by the user, IT admins can configure and install the initial_preferences in the above-mentioned location to make this feature work.

 