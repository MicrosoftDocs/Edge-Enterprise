---
title: "Reset Microsoft Edge data in the cloud"
ms.author: archandr
author: dan-wesley
manager: silvanam
ms.date: 01/12/2024
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Learn how to reset Microsoft Edge data in the cloud"
---

# Reset Microsoft Edge data in the cloud

This article describes the steps for resetting your Microsoft Edge data in the cloud.

## Overview

There are situations in which you want to reset your Microsoft Edge data in the cloud. For example, you want to synchronize your data, but Microsoft Edge reports that it's unable to synchronize the data. Another example is to make sure that your data is removed from Microsoft's cloud. In both cases, Microsoft Edge lets you perform a cloud data reset.

## Back up your favorites

Before performing a reset, we recommend that you back up your favorites. Use the following steps to back up your favorites.

1. In Microsoft Edge, select **Ctrl + Shift + O** > select the **ellipsis (...)** > select **Export favorites**.
2. Choose the file where you want to save your favorites. You can provide your own filename or use the default name that Microsoft Edge provides, "favorites_month_day_year.html". For example, "favorites_07_05_21.html". If you need to restore your favorites later, you can do so from that file.
3. Select **Save**.

## Perform a reset to fix a synchronization problem

If Microsoft Edge reports that it can't synchronize your data and suggests resetting your data, perform a reset to fix the problem.

Use the following steps to do a reset.

1. First, make sure that you're signed out of Microsoft Edge on all your devices, including your mobile devices, except the device you're performing the reset on. To sign out of Microsoft Edge, select **Settings** > **Profiles** > **Sign out**. When signing out, don't select the option to clear favorites, settings, and etc. from your local device.
2. After you sign out of all your other devices, open Microsoft Edge on your desktop. Select **Settings** > **Profiles** > **Sync** > **Reset sync**. In the **Reset sync** dialog box, choose "Resume sync on this device after resetting sync", and then select **Reset**.

## Perform a reset to remove your data from Microsoft's cloud

If you want to remove your data from Microsoft's cloud, use the following steps to do a reset.

1. Stop synchronization on devices except the device you're performing the reset on. In Microsoft Edge, select **Settings** > **Profiles** > **Sync** > **Turn off sync**.  
2. After you stop synchronization, select **Settings** > **Profiles** > **Sync** > **Reset sync**. In the **Reset sync** dialog box, clear "Resume sync on this device after resetting sync", and then select **Reset**.

## What to expect during and after a data reset

A data reset can take from a few seconds to a few minutes, depending on how much data you've stored in Microsoft's cloud. In some cases, you might see a message saying that a reset couldn't be completed and a suggestion to reset again. In this case, wait a few hours and try to reset the data again. If you're still unable to reset your data, contact Microsoft Edge Support.

After a data reset has been successfully completed, data will once again synchronize from your device if you chose to resume sync after the reset. You'll need to sign back in on your other devices if you want to sync from those devices. However, if you didn't choose to resume sync, then your Microsoft Edge data is removed from the cloud and your data will no longer synchronize.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge Enterprise Sync](microsoft-edge-enterprise-sync.md)
