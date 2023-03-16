---
title: "Microsoft Edge for macOS switch from Microsoft AutoUpdate to EdgeUpdater"
ms.author: azeigler
author: dan-wesley
manager: edmaurer
ms.date: 03/16/2023
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Starting with version 113, Microsoft Edge for macOS will switch from Microsoft AutoUpdate to EdgeUpdater"
---

# Microsoft Edge for macOS switches from Microsoft AutoUpdate to EdgeUpdater

Starting with Microsoft Edge 113, Microsoft Edge for macOS will start using a new updater named named EdgeUpdater.

> [!NOTE]
> This updater change only applies to macOS, it doesn't affect Windows, Linux, iOS, or Android users.

## Overview

EdgeUpdater provides an update experience tailored to browser usage, with fast, reliable updates and minimal user interruption. Transitioning to EdgeUpdater also aligns our backend update systems and will allow us to deliver new macOS management experiences.

## Installation and recommendations

When Microsoft Edge 113 is installed it will automatically start using EdgeUpdater instead of Microsoft AutoUpdate (MAU).

We recommend that you let Microsoft Edge update itself. If you choose to manually update Microsoft Edge for macOS, you need to set the new **UpdateDefault** preference to your desired choice.

> [!NOTE]
> If you use Microsoft AutoUpdate preferences to prevent browser updates, you will need to transition to the new EdgeUpdater **UpdateDefault** policy before version 113 to prevent future automatic updates.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)