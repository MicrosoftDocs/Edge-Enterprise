---
title: "Reset Microsoft Edge data in the cloud"
ms.author: archandr
author: dan-wesley
manager: silvanam
ms.date: 03/25/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Learn how to reset Microsoft Edge data in the cloud."
---

# Reset Microsoft Edge data in the cloud

This article describes the steps for resetting your Microsoft Edge data in the cloud.

## Overview

There are situations in which you want to reset your Microsoft Edge data in the cloud. For example, you want to synchronize your data, but Microsoft Edge reports that it's unable to synchronize the data. Another example is to make sure that your data is removed from Microsoft's cloud. In both cases, Microsoft Edge lets you perform a cloud data reset.

## Back up your favorites

Before performing a reset, we recommend that you back up your favorites. Use the following steps to back up your favorites.

1. In Microsoft Edge, select **Ctrl + Shift + O** > select the **ellipsis (...)** > select **Export favorites**.
2. Choose the file where you want to save your favorites. You can provide your own filename or use the default name that Microsoft Edge provides, "favorites_month_day_year.html. For example, "favorites_07_05_21.html". If you need to restore your favorites later, you can do so from that file.
3. Select **Save**.

## Perform a reset to fix a synchronization problem

If Microsoft Edge reports that it can't synchronize your data and suggests resyncing your data, perform a resync to fix the problem.

Use the following steps to perform a resync:

1. Go to **Settings** > **Profiles** > **Sync** > **Re-sync data to this device** and then select on "Re-sync". A resync can take from a few seconds to a few minutes, depending on how much of your data is stored in Microsoft's cloud.  
2. If sync problems persist after a resync, select "Still having sync problems? Try another option" to see more steps and then select "Reset sync". It's important to keep the browser open until the reset is fully complete.

## Perform a reset to remove your data from Microsoft's cloud

If you want to remove your data from Microsoft's cloud, use the following steps to do a reset.

1. Stop synchronization on devices except the device you're performing the reset on. In Microsoft Edge, go to **Settings** > **Profiles** > **Sync**, and toggle off sync for the data types that you want to remove from Microsoft's cloud.
2. After you stop synchronization for the data types you chose, go to **Settings** > **Profiles** > **Sync** > **Re-sync data to this device** and select "Still having sync problems? Try another option" to see more steps and then select "Reset sync". It's important to keep the browser open until the reset is finished.

## What to expect during and after a data reset

A data reset can take from a few seconds to a few minutes, depending on how much of your data is stored in Microsoft's cloud. In some cases, you might see a message saying that a reset couldn't be completed and a suggestion to reset again. In this case, wait a few hours and try to reset the data again. If you're still unable to reset your data, contact Microsoft Edge Support.

After a data reset successfully completes, data will once again synchronize from your device if you chose to resume sync after the reset. You have to sign back in on your other devices if you want to sync from those devices. However, if you didn't choose to resume sync, then your Microsoft Edge data is removed from the cloud and your data is no longer synchronized.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge Enterprise Sync](microsoft-edge-enterprise-sync.md)
