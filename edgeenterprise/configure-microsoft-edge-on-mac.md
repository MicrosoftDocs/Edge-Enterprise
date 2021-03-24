---
title: "Configure Microsoft Edge for macOS using a .plist"
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 11/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Configure Microsoft Edge policy settings on macOS using a .plist"
---

# Configure Microsoft Edge policy settings for macOS using a .plist

This article describes how to configure Microsoft Edge on macOS using a property list (.plist) file. You'll learn how to create this file and then deploy it to Microsoft Intune.

For more information, see [About Information Property List Files](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (Apple's website) and [Custom payload settings](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).

> [!NOTE]
> This article applies to Microsoft Edge version 77 or later.

## Configure Microsoft Edge policies on macOS

The first step is to create your plist. You can create the plist file with any text editor or you can use [Terminal to create the configuration profile](#create-a-configuration-profile-using-terminal). However, it's easier to create and edit a plist file using a tool that formats the XML code for you. *Xcode* is a free integrated development environment that you can get from one of the following locations:

- [Apple developer website](https://developer.apple.com/xcode/)
- [Mac App Store](https://apps.apple.com/app/xcode/id497799835?mt=12)

For a list of supported policies and their preference key names, see [Microsoft Edge browser policies reference](microsoft-edge-policies.md). In the policy templates file, which can be downloaded from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise), there's an example plist (*itadminexample.plist*) in the **examples** folder. The example file contains all supported data types that you can customize to define your policy settings. 

The next step after you create the contents of your plist, is to name it using the Microsoft Edge preference domain, *com.microsoft.Edge*. The name is case sensitive and should not include the channel you are targeting because it applies to all Microsoft Edge channels. The plist file name must be **_com.microsoft.Edge.plist_**.

> [!IMPORTANT]
> Starting with build 78.0.249.2, all Microsoft Edge channels on macOS read from the **com.microsoft.Edge** preference domain. All prior releases read from a channel specific domain, such as **com.microsoft.Edge.Dev** for Dev channel.

The last step is to deploy your plist to your users' Mac devices using your preferred MDM provider, such as Microsoft Intune. For instructions see [Deploy your plist](#deploy-your-plist).

### Create a configuration profile using Terminal

1. In Terminal, use the following command to create a plist for Microsoft Edge on your desktop with your preferred settings:

   ```cmd
   /usr/bin/defaults write ~/Desktop/com.microsoft.Edge.plist RestoreOnStartup -int 1
   ```

2. Convert the plist from binary to plain text format:

   ```cmd
   /usr/bin/plutil -convert xml1 ~/Desktop/com.microsoft.Edge.plist
   ```

After converting the file verify that your policy data is correct and contains the settings you want for your configuration profile.

> [!NOTE]
> Only key value pairs should be in the contents of the plist or xml file. Prior to uploading your file into Intune remove all the \<plist> and \<dict> values, and xml headers from your file. The file should only contain key value pairs.

## Deploy your plist

For Microsoft Intune create a new device configuration profile targeting the macOS platform and select the *Preference file* profile type. Target **com.microsoft.Edge** as the preference domain name and upload your plist. For more information see [Add a property list file to macOS devices using Microsoft Intune](/intune/configuration/preference-file-settings-macos).

For Jamf upload the .plist file as a *Custom Settings* payload.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Configure for macOS with Jamf](configure-microsoft-edge-on-mac-jamf.md)
- [Configure for Windows](configure-microsoft-edge.md)
- [Configure for Windows with Intune](configure-edge-with-intune.md)