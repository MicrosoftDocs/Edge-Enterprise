---
title: "Create Microsoft Edge user data directory variables"
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Learn how to create Microsoft Edge user data directory variables"
---

# Create Microsoft Edge user data directory variables

This article explains how you can use data directory variables instead of using hard-coded paths when modifying Microsoft Edge.

>[!NOTE]
>This article applies to Microsoft Edge version 77 or later.

## Path variables

Policies for modifying data directory paths (For example, configuring the [UserDataDir](microsoft-edge-policies.md#userdatadir) or [DownloadDirectory](microsoft-edge-policies.md#downloaddirectory) support variables. When configuring these policies, you can use variables instead of hard-coded paths. For example, to store your profile data under user local application data on Windows instead of the default location. Set the [UserDataDir](microsoft-edge-policies.md#userdatadir) policy to **${local_app_data}\Edge\Profile**. On most Windows 10 installations, this path resolves to *C:\Users\\&lt;Current-user&gt;\AppData\Local\Microsoft\Edge\Profile*.

>[!NOTE]
>If left unset, Microsoft Edge uses default directory paths. A user can use the `--user-data-dir` command-line flag to override the default.

To view the current  **Profile path**, open the **About version** page (type "edge://version"). The **Profile path** follows this format: *C:\Users\\&lt;Current-user&gt;\AppData\Local\Microsoft\Edge\User Data\Default*.

### Guidance for using path variables

Review the following guidance before using variables for paths.

- All policies that involve paths where Microsoft Edge stores different data are platform dependent. Some of these policies are available only on specific platforms, but others can be used on all platforms.
- To avoid errors caused by applications starting from different locations on different occasions, make sure that paths are absolute.
- Every variable can occur only once in a path. For most of them, this is the only meaningful way to use variables, because they resolve to absolute paths.
- Almost all policies will create the path if it doesn't exist (if possible in the existing circumstances).
- Using network locations for some policies can lead to unexpected results due to differences in how different versions/channels of Microsoft Edge handle the folder structure.

### Supported path variables

Microsoft Edge supports the following path variables.

#### All platforms

| Variable | Description |
| --- | --- |
| **${user_name}** | The user who's using Microsoft Edge. Microsoft Edge respects SUIDs (Set owner User ID up on execution) Example: *audreysmall* |
| **${machine_name}** | The machine name, possibly including the domain name. Example: *audreysmall* or *audrey.ex.contoso.com* |

#### Windows only

| Variable | Description |
| --- | --- |
| **${documents}** | The Documents folder for the current user. Example: *C:\Users\Administrator\Documents* |
|**${local_app_data}** | The Application Data folder for the current user. Example: *C:\Users\Administrator\AppData\Local* |
|**${roaming_app_data}** | The Roamed Application Data folder for the current user. Example: *C:\Users\Administrator\AppData\Roaming* |
| **${profile}** | The home folder for the current user. Example: *C:\Users\Administrator* |
| **${global_app_data}** | The system-wide Application Data folder. Example: *C:\AppData* |
| **${program_files}** | The Program Files folder for the current process. This  folder  depends on whether it's a 32-bit or 64-bit process. Example resolution: *C:\Program Files (x86)* |
| **${windows}** | The Windows folder. Example: *C:\Windows* |
| **${client_name)** | The name of the client PC connected to an RDP or Citrix session. This variable is empty if it's used from a local session. If it's used in a path, prefix it with something that's guaranteed not to be empty. Example: *C:\edge_profiles\session_${client_name}* resolves to *C:\edge_profiles\session_&lt;ForlocalSessions&gt;* and *C:\edge_profiles\session_&lt;SomePCname&gt;* for remote sessions. |
| **${session_name}** | The name of the active session. Use this name to distinguish multiple simultaneously connected remote sessions that are using a single user profile. Example: *WinSta0 for local desktop sessions* |

#### macOS only

| Variable | Description |
| --- | --- |
| **${users}** | The folder where users' profiles are stored. Example: */Users* |
| **${documents}** | The Documents folder for the current user. Example: */Users/audreysmall/Documents* |

## Content license

>[!NOTE]
>Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms  described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/). The original page can be found [here](https://www.chromium.org/administrators/policy-list-3/user-data-directory-variables).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br/>This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)