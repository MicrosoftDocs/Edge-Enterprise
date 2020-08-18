---
title: "Progressive rollouts for Microsoft Edge Stable channel updates"
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 05/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Progressive rollouts for Microsoft Edge Stable channel updates"
---

# Progressive rollouts for Microsoft Edge Stable channel updates

Starting with Microsoft Edge 83 release, we will perform gradual rollouts of major updates to Microsoft Edge Stable channel over the span of a few days. This progressive rollout allows us to monitor upgrades and safely update the browser across the organization.

> [!NOTE]
> This applies to Microsoft Edge Stable channel version 83 or later.

## Why do we need progressive rollout?

By monitoring the health of our updates closely and rolling out the updates over the course of several days, we can limit the impact of issues that might occur with the new update. With Microsoft Edge release 83, Progressive Rollouts will be enabled for all Windows 7, Windows 8 & 8.1, and Windows 10 versions of Microsoft Edge. We will support Microsoft Edge on Mac as soon as it is ready.

## How will the updates work?

Each installation of Microsoft Edge is assigned an upgrade value. When we start rolling out incrementally, you'll see the update when the value on your device falls within the upgrade value range. As the rollout progresses (within a few days), all users will eventually get the update. Browser updates with critical security fixes will have a faster rollout cadence than updates that don't have critical security fixes. This is done to ensure prompt protection from vulnerabilities.

## How does this affect enterprises?

Microsoft Edge artifacts are distributed to enterprises using multiple mechanisms such as Microsoft Intune, Windows Server Update Service (WSUS), and Configuration Manager. These deployment tools behave differently with respect to Progressive Rollout:

- Enterprises that manage distribution via Microsoft Intune are registered for auto-updates. Progressive Rollout is used, and all the users will see an update in a few days.
- Enterprises that manage distribution through WSUS (Windows Server Update Services) or Configuration Manager are not registered for auto-updates. Administrators manage and apply the updates that will be available from the start. Progressive Rollout does not affect this process.

Please share your valuable feedback through user voice, the in-application feedback button, or below in the comments if you have any concerns or questions.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
