---
title: "Prepare to deploy Microsoft Edge"
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 01/27/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Prepare to deploy Microsoft Edge"
---

# Prepare to deploy Microsoft Edge

This article describes how to prepare to deploy Microsoft Edge when Microsoft Edge Legacy reaches its end of service.

As per the Microsoft Edge Product Team’s [blog post](), support for the Microsoft Edge Legacy desktop application will end on March 9, 2021. The Update Tuesday (or "B") release in April will remove Microsoft Edge Legacy from devices running Windows 10 RS4 through 20H1 and replace it with Microsoft Edge.

## How to Prepare

To prepare for Microsoft Edge being installed on Windows 10 RS4 through 20H1 devices with the Update Tuesday release in April, we recommend reading [Plan your deployment of Microsoft Edge](deploy-edge-plan-deployment.md).

After you plan your deployment, use one of the following approaches to prepare to deploy Microsoft Edge.

- **Install group policies to customize your Microsoft Edge update approach**. For more information, see [Configure Microsoft Edge policy settings on Windows](configure-microsoft-edge.md), and pay special attention to the [Update Policy reference](microsoft-edge-update-policies.md) material. If you install group policies to manage your updates before installing April’s Update Tuesday release, Microsoft Edge will immediately start respecting your policy. If there isn't any installed group policy, Microsoft Edge will automatically update itself.

- **Deploy the remove the Microsoft Edge Legacy desktop application before its end of service date of March 9, 2021 and deploy Microsoft Edge**. For Windows 10 RS4 through 20H1, you can do this by using Windows Updates. For more information, see [Deploy Microsoft Edge with Windows 10 updates](deploy-edge-with-windows-10-updates.md).

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Plan your deployment of Microsoft Edge](deploy-edge-plan-deployment.md)