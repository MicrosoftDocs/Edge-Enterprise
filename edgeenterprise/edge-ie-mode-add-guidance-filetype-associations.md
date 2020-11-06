---
title: "Add Internet Explorer mode to the Open with context menu"
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Add Internet Explorer mode to the Open with context menu"
---

# Add Internet Explorer mode to the "Open with" context menu

This article explains how to add Microsoft Edge with Internet Explorer mode as an option on the **Open with** menu and dialog box for a desktop application associated with a specific file type.  

> [!NOTE]
> This article applies to Microsoft Edge version 86 or later.

## “Open with” file type association example

The registry example used in the following instructions shows an entry that associates Microsoft Edge with IE mode with the XML file type. Use the following steps as a guide for setting a file association.

1. Define a new ProgID  with the Microsoft Edge channel to use to open with IE mode, including the application name and Icon and the path to msedge.exe.

   [HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeXML\Application]<br>
"ApplicationCompany"="Microsoft Corporation" 
"ApplicationName"="Microsoft Edge Canary with IE Mode"
"ApplicationIcon"="C:\\Users\\shisub\\AppData\\Local\\Microsoft\\Edge SxS\\Application\\msedge.exe,4" 
"AppUserModelId"=""

   [HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeXML\DefaultIcon]<br>
@="C:\\Users\\shisub\\AppData\\Local\\Microsoft\\Edge SxS\\Application\\msedge.exe,4"

2. Configure shell updates to pass the command line needed to open with IE mode.

   [HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeXML\shell\open\command]<br> 
@="\"C:\\Users\\shisub\\AppData\\Local\\Microsoft\\Edge SxS\\Application\\msedge.exe\" -ie-mode-file-url -- \"%1\"" 

3. \<explain why we are doing this at a high level\> 
Finally, associate the .xml file extension with a new ProgID. Add your ProgID as a value name, with the value type of REG_SZ.

   [HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.xml\OpenWithProgids]<br> 
"MSEdgeIEModeXML"=hex(0):

After you set the keys described in the previous example, your users will see an additional option on the **Open with** menu to open an XML file using Microsoft Edge \<channel\> with IE mode. 

## See also

- [About IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Configurable sites information](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [Additional Enterprise Mode information](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Setting file type associations](https://docs.microsoft.com/windows/win32/shell/fa-file-types)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
