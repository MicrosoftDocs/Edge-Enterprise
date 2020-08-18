---
title: "Microsoft Edge kiosk mode"
ms.author: brianalt
author: brianalt
manager: seanlynd
ms.date: 01/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Microsoft Edge kiosk mode"
---

# Microsoft Edge kiosk mode

This article provides an overview of the Microsoft Edge (version 77 or later) kiosk mode options. It also covers what's required to continue using Microsoft Edge Legacy kiosk mode (version 45 and earlier.)

For information about Microsoft Edge Legacy kiosk mode (version 45 and earlier) see [Deploy Microsoft Edge kiosk mode](https://aka.ms/edgekioskmode).

## Microsoft Edge with assigned access

Microsoft Edge can be run with [multi-app assigned access](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing” kiosk mode type. To configure Microsoft Edge with multi-app assigned access follow the instructions on how to [Set up a multi-app kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps). The AUMID for the Microsoft Edge Stable channel is **MSEdge**.

When using Microsoft Edge with multi-app assigned access you can use the [Microsoft Edge browser policies](microsoft-edge-policies.md) to configure the browsing experience to meet your unique requirements.

Today Microsoft Edge does not support the same Microsoft Edge Legacy kiosk mode types for single-app assigned access and the "Public browsing" kiosk mode type in multi-app assigned access. If you need a browser for your single-app assigned access kiosk device, we recommend using [Microsoft Edge Legacy kiosk mode](https://aka.ms/edgekioskmode) or the [Microsoft Kiosk Browser app](https://www.microsoft.com/p/kiosk-browser/9ngb5s5xg2kp?activetab=pivot:overviewtab). 

## Microsoft Edge “--kiosk” command line parameter

You can launch Microsoft Edge in kiosk mode using the “`--kiosk`” command line parameter. This opens the browser in full screen with the full screen keyboard shortcut disabled (F11). To accomplish this, create a shortcut with the target set to:<br>
*`"<local path>\msedge.exe" --kiosk http://bing.com`*

> [!NOTE]
> The "`--kiosk`" parameter will not prevent the user from accessing Windows keyboard shortcuts and will not prevent other applications from running. To accomplish this type of control, consider using [AppLocker to create a Windows 10 kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-applocker) and [Keyboard Filter](https://docs.microsoft.com/windows-hardware/customize/enterprise/keyboardfilter).

To exit kiosk mode and close the browser use alt+F4.

## Support for Microsoft Edge Legacy kiosk mode

When the new version of Microsoft Edge Stable channel is installed, Microsoft Edge Legacy is hidden and all attempts to launch Microsoft Edge Legacy are redirected to the new version. For information about:

- Windows update requirements, see [Windows updates to support the next version of Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md) 
- Accessing Microsoft Edge Legacy after installing Microsoft Edge,  see [Access Microsoft Edge Legacy after installing the new version of Microsoft Edge](microsoft-edge-sysupdate-access-old-edge.md)
 
To continue using Microsoft Edge Legacy kiosk mode on your kiosk devices take one of the following actions: 

- If you plan to install Microsoft Edge Stable channel, want to allow it to be installed, or if it's already installed on your kiosk device deploy the Microsoft Edge [Allow Microsoft Edge Side by Side browser experience](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs) policy.
- To prevent Microsoft Edge Stable channel from being installed on your kiosk devices deploy the Microsoft Edge [Allow installation default](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allow-installation-default) policy for Stable channel or consider using the [Blocker toolkit to disable automatic delivery of Microsoft Edge](microsoft-edge-blocker-toolkit.md). 

## See also

- [Configure kiosks and digital signs on Windows desktop editions](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [Deploy Microsoft Edge Legacy kiosk mode](https://aka.ms/edgekioskmode) 
- [Plan your deployment of Microsoft Edge](deploy-edge-plan-deployment.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
