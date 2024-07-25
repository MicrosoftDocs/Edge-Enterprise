---
title: "Frequently asked questions (FAQ) about Microsoft Edge in the enterprise"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 07/18/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Frequently asked questions (FAQ) about Microsoft Edge in the enterprise"
--- 


# Microsoft Edge frequently asked questions

This article contains frequently asked questions (FAQ) about Microsoft Edge in the enterprise.

## How do I know which version of Microsoft Edge I have?

Select the ellipses icon (**...**) in the upper-right corner of Microsoft Edge, and then select **Settings**. Select **About Microsoft Edge** to see your version of Microsoft Edge.

## What about Internet Explorer 11?

>[!Note]
> The retired, out-of-support Internet Explorer 11 desktop application has been permanently disabled through a Microsoft Edge update on certain versions of Windows 10. For more information, see [Internet Explorer 11 desktop app retirement FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549).

## Does Microsoft Edge support ActiveX controls or Browser Helper Objects like Silverlight or Java?

No. Microsoft Edge doesn't support ActiveX controls or Browser Help Objects (BHOs) like Silverlight or Java. If you run web apps that use ActiveX controls, BHOs, or legacy document modes on Internet Explorer (IE) 11, you can configure them to run in IE mode on  Microsoft Edge. For more information, see [Configure IE mode on Microsoft Edge](./edge-ie-mode.md).

## Will favorites be ported over from the current version of Microsoft Edge or do I have to add them back?

Microsoft Edge supports import from existing installs of Microsoft Edge, Chrome, Internet Explorer, and Firefox (on Win10). The following settings are supported for importing: Bookmarks, History, Passwords, and Autofill (payments, addresses, and generic forms). You can choose to import either from the First-run Experience or from browser settings.

## What's the difference between the Stable, Beta, Dev, and Canary channels/builds?

The Stable channel of Microsoft Edge is the most stable channel we offer with enterprise-focused features ready for you to [pilot and evaluate](https://aka.ms/EdgeEnterprise) across your organization. The Beta channel allows you to validate the next Stable release with a representative set of users. The Stable and Beta channels are updated approximately every four weeks. The Dev and Canary channels continue to update weekly and daily, respectively. Offline installers (MSIs and PKG files) are available only for Stable, Beta, and Dev channels. For more information, see [Overview of Microsoft Edge channels](./microsoft-edge-channels.md).

## What kind of extension support do I have with Microsoft Edge?

Microsoft Edge supports extensions from [Microsoft Edge Insider Addons](https://go.microsoft.com/fwlink/?linkid=2081222) and the [Chrome Web Store](https://go.microsoft.com/fwlink/?linkid=2072338).

## Do you support Mobile Device Management (MDM) and Microsoft Intune?

Yes. Configuring Microsoft Edge on Windows 10/11 using Microsoft Intune and Mobile Device Management (MDM) is now supported. For more information, see [Configure Microsoft Edge using Microsoft Intune](./configure-edge-with-intune.md) and [Configure Microsoft Edge using Mobile Device Management](./configure-edge-with-mdm.md).

## Does Windows Server Update Services (WSUS) support the initial deployment of Microsoft Edge?

Yes. There are packages in the [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Search.aspx?q=the%20new%20microsoft%20edge%20for%20windows) that can be used for the initial deployment of Microsoft Edge via WSUS. After initial deployment, automatic updates are configured by default. For more information, see [Update in WSUS for the new Microsoft Edge for Windows 10, version 1809, 1903, 1909, and 2004: October 29, 2020](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge).

 Manual updates can be done through a configuration management tool, like [ConfigMgr](/configmgr/apps/deploy-use/deploy-edge?bc=%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=%2fDeployEdge%2ftoc.json).

## Are Initial Preferences supported?

Yes. For more information, see [Configure Microsoft Edge using Initial Preferences settings for the first run.](./initial-preferences-support-on-microsoft-edge-browser.md)

## See also

- [Microsoft Edge documentation landing page](./index.yml)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
  