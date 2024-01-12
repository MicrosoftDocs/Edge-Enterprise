---
title: "Provision favorites for Microsoft Edge"
ms.author: capoon
author: dan-wesley
manager: abutcher
ms.date: 01/12/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Provision favorites for Microsoft Edge"
---

# Provision favorites for Microsoft Edge

Based on customer feedback, we've made improvements to provisioning favorites. Starting with Microsoft Edge version 85, Admins no longer have to manually craft a file to provision favorites. Admins can add favorites and folders using the Microsoft Edge UI to generate a file that can be exported to a group policy.

This article describes how to provision a set of favorites and folders for your organization. You can use the [Configure favorites](microsoft-edge-policies.md#configure-favorites) policy to provision favorites and folders.

## Prerequisites and recommendations

- Microsoft Edge version 85 with the appropriate administrative template installed for group policies.
- We recommend that you use a new profile in Microsoft Edge to provision these favorites. All favorites that are saved with the profile will be included in the export.  

## Provision favorites and folders

Use the following steps to provision favorites and folders for your users.

1. Go to the Microsoft Edge address bar and type this URL: *edge://flags/#edge-favorites-admin-export*.

2. Under **Favorites configuration export for administrators**, pick **Enabled** from the dropdown list and then select **Restart**.

3. Go to the **Favorites** page at *edge://favorites* so you can add the favorites and folders that you want to provision.

4. When you finish adding favorites and folders you'll export them so they can be used by the **Configure favorites** policy. Go to the address bar and navigate to *edge://favorites*, select the ellipsis "**…**" and choose **Export favorites configuration**. The next screenshot shows the options you have when provisioning favorites.

   ![Menu options for working with favorites.](media/edge-learnmore-provision-favorites/provision-favorites-menu-options.png)

5. Under **Export your favorites configuration** you provide a name for the folder that your users will see. Type the Folder name and pick the Platform format you want to use. Select **Copy to clipboard**. The next screenshot shows "Managed favorites" for the folder name and the platform is Windows.

   ![Dialog for exporting favorites to a Windows folder.](media/edge-learnmore-provision-favorites/provision-favorites-export.png)

6. Open the Group Policy Editor, navigate to *Computer Configuration/Administrative Templates/Microsoft Edge/* and pick **Configure Favorites**. Enable the "Configure Favorites" policy. Under **Options:**, paste the exported contents in the Configure favorites text area then select **Apply**. The next screenshot shows an example of the "Managed favorites" folder from step 5.

   ![Use gpedit to enable and configure "Configure favorites" policy.](media/edge-learnmore-provision-favorites/provision-favorites-gpedit.png)

7. Select **OK** or **Apply** to save the policy settings.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)