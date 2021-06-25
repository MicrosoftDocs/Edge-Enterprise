---
title: "Self-host Microsoft Edge extensions"
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 04/08/2021
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
5. Test the extension and take note of the ID field (this is the CRX ID) and version number. You’ll need this information later. The next screenshot shows a test extension with its CRX ID.

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-test-extension.png" alt-text="Extension example showing CRX ID":::

6. Upload the the CRX file to the host and note the URL of the location it will be downloaded from. This information is needed for the XML manifest file.
7. To create a manifest XML file with the app/extension ID, download URL, and version, define the following fields:  

   - **appid** - The extension ID from step 5
   - **codebase** - The download location for the CRX file from step 6
   - **version** - The version of the app/extension, which should match the version specified in the manifest of the extension.

   The next code snippet shows an example of an XML manifest file.

   ```xml
   <?xml version='1.0' encoding='UTF-8'?> 
   <gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'> 
     <app appid='ekilpdeokbpjmminmhfcgkncmmohmfeb'> 
     <updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.0' /> 
     </app> 
   </gupdate> 
   ```

   For more information, see [Auto-update extensions in Microsoft Edge - Microsoft Edge Development](/microsoft-edge/extensions-chromium/enterprise/auto-update).

8. Upload the completed XML file to a location where it can be downloaded from, noting the URL. This URL will be needed when you install the extension using a group policy. See [Distribute a privately hosted extension](#distribute-a-privately-hosted-extension).

   > [!IMPORTANT]
   > The hosting location for the extension doesn’t need authentication. It needs to be accessible by user devices wherever they might be used.

## Publish updates to an extension

After you change and test the updated extension you can publish it. Use the following steps as a guide for publishing an update.

1. Change the version number in your extension's manifest.JSON file to a higher number using the following syntax: `"version":"versionString"`. If the "version":"1.0", then you can update to "version":"1.1" or any number higher than "1.0".
2. Update the "version" of `<updatecheck>` in the XML file to match the number that you put in the manifest file in the previous step. For example:<br>`<updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.1' />`
3. Create a CRX file that includes the new changes. Go to *edge://extensions* and enable **Developer mode**.
4. Click **Pack extension** and go to the directory for the extension source.

   > [!IMPORTANT]
   > Use the same PEM file that was generated and saved the first time the CRX file was created. If you don't use the same PEM file the app ID of the extension will change and the update will be treated as a new extension.

5. Drag and drop the CRX file into the extensions window and verify that it loads.
6. Test the updated extension.
7. Replace the old CRX file and XML file with the new files for the updated extension.

The extension's changes will be picked up during the next policy sync cycle. For more information about updating extensions, see: [Update URL](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) and [Update manifest](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest).

## Distribute a privately hosted extension

You can share the link of the location where the CRX file is hosted, and as soon as users enter the URL in their browser the extension will be downloaded and installed. Users can enable the extension from the edge://extensions page. To allow users to install self-hosted extensions, you need to add the extension CRX IDs to the [ExtensionInstallAllowList](/deployedge/microsoft-edge-policies#extensioninstallallowlist) policy.

Alternatively, you can use group policy [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) to Force-install an extension on your users’ devices.

You can apply these policies to your selected users, devices, or both. Remember though that policy updates are not instantaneous, and it will take time for the policy settings to take effect.

## See also

- [Manage Microsoft Edge extensions in the enterprise](microsoft-edge-manage-extensions.md)
- [Use group policies to manage Microsoft Edge extensions](microsoft-edge-manage-extensions-policies.md)
- [Detailed guide to the ExtensionSettings policy](microsoft-edge-manage-extensions-ref-guide.md)
- [FAQ for Microsoft Edge Extensions](microsoft-edge-manage-extensions-faq.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
