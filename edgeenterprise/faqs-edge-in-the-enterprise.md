---
title: "Frequently asked questions about Edge in the enterprise"
ms.author: jwhit
author: jwhit-MSFT
manager: laurawi
ms.date: 08/03/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Frequently asked questions about deploying Microsoft Edge in the enterprise"
---

# Frequently asked questions about Microsoft Edge in the enterprise

> [!NOTE]
> This article applies to Microsoft Edge version 77 or later.

## How do I know which version of Microsoft Edge I have?

In the upper right corner of Microsoft Edge, click the ellipses icon (**...**), and then click **Settings**. Select **About Microsoft Edge** to see your version of Microsoft Edge.

## Will Internet Explorer 11 continue to receive updates?

We're committed to keeping Internet Explorer a supported, reliable, and safe browser. Internet Explorer is still a component of Windows and follows the support lifecycle of the OS on which it's installed. For more information, see [Lifecycle FAQ - Internet Explorer](https://support.microsoft.com/help/17454/). While we continue to support and update Internet Explorer, the latest features and platform updates will be available only in Microsoft Edge.

## Can I run the current version of Microsoft Edge (Microsoft Edge Legacy) side by side when I'm trying the new version?

Yes, you can. After January 15th, 2020 the new version of Microsoft Edge (Chromium-based) will be distributed to Home and Pro Edition devices running Windows 10 version 1803 or newer. Domain-joined devices are excluded from this update. For more information, see [Overview of Microsoft Edge updates](https://docs.microsoft.com/deployedge/microsoft-edge-blocker-toolkit#overview). You can have a side by side installation of Microsoft Edge Legacy as you evaluate the next version of Microsoft Edge. For more information, see [How to access the old version of Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge). Additionally, each of the new Microsoft Edge channels also support side by side installations. For more information, see [Overview of Microsoft Edge channels](https://docs.microsoft.com/deployedge/microsoft-edge-channels).

## Does Microsoft Edge (Chromium-based) support ActiveX controls or BHOs like Silverlight or Java?

No. Microsoft Edge doesn't support ActiveX controls and BHOs like Silverlight or Java. However, if you're running web apps that use ActiveX controls, BHOs, or legacy document modes on Internet Explorer 11, you can configure them to run in IE mode on the new Microsoft Edge. For more information, see [Configure IE mode on Microsoft Edge](https://docs.microsoft.com/DeployEdge/edge-ie-mode).

## Will favorites be ported over from the current version of Microsoft Edge or will I have to re-add?

Currently, Microsoft Edge supports import from existing installs of Microsoft Edge, Chrome, Internet Explorer, and Firefox (on Win10). The following settings are supported for importing: Bookmarks, History, Passwords and Autofill (Payments, addresses and generic forms). You can choose to import either from the First-run Experience or from browser settings.  

## What's the difference between the Stable, Beta, Dev, and Canary channels/builds?

The Stable channel of the next version of Microsoft Edge is the most stable channel we offer with enterprise-focused features ready for you to [pilot and evaluate](https://aka.ms/EdgeEnterprise) across your organization. The Beta channel allows you to validate the next Stable release with a representative set of users. The Stable and Beta channels will be updated approximately every six weeks. The Dev and Canary channels will continue to update weekly and daily respectively. Offline installers (MSIs and PKG files) are only available for Stable, Beta and Dev channels. For more information, see [Overview of Microsoft Edge channels](https://docs.microsoft.com/deployedge/microsoft-edge-channels).

## What kind of extension support do I have with the new version of Microsoft Edge?

Microsoft Edge supports extensions from [Microsoft Edge Insider Addons](https://go.microsoft.com/fwlink/?linkid=2081222) and [Chrome Web Store](https://go.microsoft.com/fwlink/?linkid=2072338).

## Do you support Mobile Device Management (MDM) and Microsoft Intune?

Yes. Configuring Microsoft Edge on Windows 10 using Microsoft Intune and Mobile Device Management (MDM) is now supported. For more information, see [Configure Microsoft Edge using Microsoft Intune](configure-edge-with-intune.md) and [Configure Microsoft Edge using Mobile Device Management](configure-edge-with-mdm.md).

## Does WSUS support the initial deployment of the new Microsoft Edge?

No. WSUS supports updating existing MSI installs of Microsoft Edge, but it cannot be used for the initial deployment. If the intent is to ultimately manage updates via WSUS then the initial deployment can be done through a management tool, such as [ConfigMgr](https://docs.microsoft.com/configmgr/apps/deploy-use/deploy-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json).

## See also

- [Microsoft Edge documentation landing page](https://docs.microsoft.com/DeployEdge/)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
