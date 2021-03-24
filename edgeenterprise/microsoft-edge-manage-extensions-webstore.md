---
title: "Self-host Microsoft Edge extensions"
ms.author: aspoddar
author: dan-wesley
manager: balajek
ms.date: 03/22/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Learn how to package and self-host Microsoft Edge extensions in the enterprise."
---

# Self-host Microsoft Edge extensions

This article provides basic guidance for packaging an extension to host on your own webstore. It also includes instructions on how to deploy extensions to devices and users in your organization.

## Prerequisites

To self-host your own extensions, you will need to provide your own web hosting services for the extensions and their manifest files.

 The following steps assume that you’ve already created your extension, have some experience with XML files, have a working knowledge of configuring group policy, and know how to use the Windows registry.

## Publish an extension

Before you publish an extension it needs to be packed into a CRX (Chrome extension) file. Use the following steps as a guide to packing an extension as a CRX file.

1. In the Microsoft Edge address bar, go to *edge://extensions* and turn on **Developer mode** if it’s not already enabled.
2. Under **Installed extensions**, click **Pack Extension** to create the CRX file.
3. Use the **Pack extension** dialog to find the directory that has the source for the extension. Select the directory and then click **Pack extension**.  This will create your CRX file, along with a PEM file. Save the PEM file because it’s needed for making version updates to the extension. The next screenshot shows the **Pack extension** dialog for locating the root directory of the extension.

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-pack-dialog.png" alt-text="Pack extension dialog for finding an extension's source code.":::

   > [!IMPORTANT]
   > Store the PEM file in a safe location because it’s the key for the extension and it’s needed for future updates.

4. Drag the CRX file into your extensions window and make sure that it loads.
5. Test the extension and take note of the ID field (this is the CRX ID) and version number. You’ll need this information later. The next screenshot shows 

## Publish updates to an extension

After you change and test the updated extension you can publish it. Use the following steps as a guide for publishing an update.

## Distribute a privately hosted extension

If you aren’t using the Admin console, you can use the policy called "Configure the list of force installed apps and extensions" to force-install an extension on your user's device. 




## See also

- [Manage Microsoft Edge extensions in the enterprise](microsoft-edge-manage-extensions.md)
- [Use group policies to manage Microsoft Edge extensions](microsoft-edge-manage-extensions-policies.md)
- [FAQ for Microsoft Edge Extensions](microsoft-edge-manage-extensions-faq.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
