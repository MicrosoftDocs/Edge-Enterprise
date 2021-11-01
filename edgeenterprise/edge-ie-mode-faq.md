---
title: "IE mode troubleshooting and FAQ"
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Troubleshooting and FAQ for Microsoft Edge Internet Explorer mode"
---

# IE mode troubleshooting and FAQ

> [!NOTE]
> The Internet Explorer 11 desktop application will be retired and go out of support on  June 15, 2022. To see the list of what’s in scope, see the [Internet Explorer 11 desktop app retirement FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549). The same IE11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode. To learn more, see the [The future of Internet Explorer on Windows 10 is in Microsoft Edge](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/) blog post.

This article provides troubleshooting tips and an FAQ for Microsoft Edge version 77 or later.

> [!NOTE]
> This article applies to Microsoft Edge version 77 or later.

## Troubleshoot IE Mode

Use the information in this section to diagnose and fix IE mode problems.

### Internet Explorer mode  general diagnostic information

You can get Internet Explorer mode diagnostic information on the Microsoft Edge Compatibility tab. To open this tab, go to *edge://compat/iediagnostic*. This page may show diagnostic messages. This page also provides configuration information for the following categories:

- Registry key check. (Displayed only if the check fails.) Checks to see if Internet Explorer integration is set up correctly in the registry. If not, the user can click Fix it to resolve the problem.
- Internet Explorer mode. Shows the API version that's used, based on the configuration and OS. If there's a problem, the user may be prompted to install a Windows Update.
- Internet Explorer mode setting. Shows whether Internet Explorer mode is enabled, and how it's configured.
- Command line. Shows the command line string and switches used to start Microsoft Edge.
- Group policy settings. Shows whether IE mode is configured using group policies, and the policies that are applied.

## Frequently Asked Questions

## See also
  
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [About IE mode](./edge-ie-mode.md)
- [Additional Enterprise Mode information](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)