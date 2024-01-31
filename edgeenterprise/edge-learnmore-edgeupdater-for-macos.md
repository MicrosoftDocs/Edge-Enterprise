---
title: "Microsoft Edge for macOS switch from Microsoft AutoUpdate to EdgeUpdater"
ms.author: azeigler
author: dan-wesley
manager: edmaurer
ms.date: 03/17/2023
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Starting with version 113, Microsoft Edge for macOS will switch from Microsoft AutoUpdate to EdgeUpdater"
---

# Microsoft Edge for macOS switches from Microsoft AutoUpdate to EdgeUpdater

Starting with Microsoft Edge 113, Microsoft Edge for macOS will start using a new updater named EdgeUpdater.

> [!NOTE]
> This updater change only applies to macOS, it doesn't affect Windows, Linux, iOS, or Android users.

## Overview

EdgeUpdater provides an update experience tailored to browser usage, with fast, reliable updates and minimal user interruption. Transitioning to EdgeUpdater also aligns our backend update systems and will allow us to deliver new macOS management experiences.

## Installation and recommendations

When Microsoft Edge 113 is installed, it will automatically start using EdgeUpdater instead of Microsoft AutoUpdate (MAU).

> [!NOTE]
> Microsoft Edge will automatically start using EdgeUpdater, but you still have to set policies to manage update behavior.

We recommend that you let Microsoft Edge update itself. If you choose to manually update Microsoft Edge for macOS, you need to set the new **UpdateDefault** preference to your desired choice.

> [!NOTE]
> If you use Microsoft AutoUpdate preferences to prevent browser updates, you will need to transition to the new EdgeUpdater **UpdateDefault** policy before version 113 to prevent future automatic updates.

## Update configuration example

This section shows how to use a plist to disable EdgeUpdater and turn off updates.

To create and deploy a plist, follow these steps:

1. Create a file named "com.microsoft.EdgeUpdater.plist".
2. Paste the following contents into the plist file:

   ```xml
   <?xml version="1.0" encoding="UTF-8"?>
   <!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" http://www.apple.com/DTDs/PropertyList-1.0.dtd>
   <plist version="1.0">
   <dict>
       <key>updatePolicies</key>
       <dict>
           <key>global</key>
           <dict>
               <key>UpdateDefault</key>
               <integer>3</integer>
           </dict>
       </dict>
   </dict>
   </plist>
   ```

3. Deploy your plist.

   Using Microsoft Intune, create a new device configuration profile targeting the macOS platform and select the **Preference file** profile type. Target **com.microsoft.EdgeUpdater** as the preference domain name and upload your plist. For more information, see [Add a property list file to macOS devices using Microsoft Intune](/mem/intune/configuration/preference-file-settings-macos).<br>

   For Jamf, upload the .plist file as a **Custom Settings** payload.

To test your configuration on a local device:

1. Copy the "com.microsoft.EdgeUpdater.plist" to */Library/Managed Preferences/com.microsoft.EdgeUpdater.plist*.
2. Change ownership of the managed preference with this command:

   ```bash
   sudo chown root:wheel /Library/Managed Preferences/com.microsoft.EdgeUpdater.plist
   ```

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)