---
title: "Manage extensions"
ms.author: katherinegan
author: dan-wesley
manager: archandr
ms.date: 09/17/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Provides steps for managing extensions for Microsoft Edge management service."
---

# Manage extensions

This article gives steps for managing extensions for Microsoft Edge management service.

## Manage extensions

To manage extension settings for a profile, go **Microsoft Edge management**, select the profile you want to work with and then select the **Extensions** pivot. You can configure profile settings that apply to all extensions. Any extensions you add to be managed will appear in the profile. You can add an extension to the allow list, block list, or forced-installed list by setting the installation policy. If you configure specific settings on an individual extension, then those settings override the profile settings.

### Import existing extension settings to an existing configuration profile

Follow these steps to import extension settings:

1. Select the profile you want to import extension settings to and go to the **Extensions** pivot.
1. Select **Import JSON**.
1. Under **Import JSON**, browse for the JSON file that contains your extension settings and then select **Import**. Importing might overwrite any previous configurations. Note that it may take some time to complete the import if the file is large.

After confirmation, your profile will be populated with the imported settings.

### Export extension settings to configure the ExtensionSettings policy

Follow these steps to export extension settings:

1. Select the profile you want to export extension settings from and go to the **Extensions** pivot.
1. Select **Export JSON** and the export will start downloading.

After the download is finished, you can apply the JSON as a value to the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) group policy.

### Manage settings for all extensions

Follow these steps to manage profile settings:

1. Select a profile and go to the **Extensions** pivot.
1. Select **Manage extensions** to configure any of the settings in the following table.

   | Setting | Description |
   |:-----|:-----|
   | Block all extensions | Users can't install any extensions (unless the extension is on the allow list). |
   | Allowed types of apps and extensions| Specify what types of app or extensions users are allowed to install. |
   | Install sources| Specify which URLs are allowed to install extensions. For URL pattern examples, see the [Defining match patterns](/microsoft-edge/extensions-chromium/developer-guide/match-patterns). |
   | External extensions | Allow or block installation of external extensions. |
   | Message for users when extension is blocked | Set a custom message that displays if users try to install a blocked extension. |
   | Blocked hosts | Prevent extensions from interacting with or modifying websites that you specify. The host pattern format is similar to [match patterns](/microsoft-edge/extensions-chromium/developer-guide/match-patterns) except you can't define the path. |
   | Allowed hosts | Allow extensions to interact with or modify websites, even if they're defined in blocked hosts. The host pattern format is similar to [match patterns](/microsoft-edge/extensions-chromium/developer-guide/match-patterns) except you can't define the path. |
   | Block extensions that require these permissions | Prevent users from installing/running extensions that need the permissions you select. |

1. When you're finished configuring extension settings, select **Save**.

### Add an extension

Follow these steps to add an extension:

1. Select a profile and go to the **Extensions** pivot.
1. Select **Select extension**.
1. Under **Select an extension**, select an extension from the **Microsoft Edge Add-ons** store or specify an external extension ID.
1. Select **Select**.

### Manage an extension

After selecting an extension, you can configure settings for a specific extension. These settings only apply to the extension that you select and will override any profile settings.

#### Manage extension policy

Decide if an extension is allowed, blocked, or forced by setting its installation policy. Follow these steps to configure this setting:

1. Select an extension.
1. Select **Manage installation policy** and choose one of the following options from the dropdown list:

   - Allow: Users can install the extension. This is the default setting.
   - Block: Users can't install the extension. You could remove the extension if users previously installed it. Also, you can write a message that displays when users try to install the extension.
   - Force: The extension is automatically installed. Users can't remove it. You can optionally specify an update URL for the initial extension installation and use it for subsequent updates.
   - Normal: The extension is automatically installed. Users can disable it. You can optionally specify an update URL for the initial extension installation and use it for subsequent updates.

1. Select **Save**.

#### Manage hosts

Control what websites extensions can access. Prevent extensions from altering web pages by specifying which URLs should block extensions from making changes or reading data from. Allow extensions to interact with or modify websites, even if they're defined in blocked hosts. The host pattern format is similar to [match patterns](/microsoft-edge/extensions-chromium/developer-guide/match-patterns) except you can't define the path. Follow these steps to configure this setting:

1. Select an extension.
1. Select **Manage hosts**. In the **Hosts** window, specify blocked and allowed host URLs.
1. Select **Save**.

#### Manage permissions

Prevent users from installing and using the extension if it requires certain permissions that your organization doesn't allow. Follow these steps to configure this setting:

1. Select an extension.
1. Select **Manage permissions**. You can choose to use the default permissions that were defined in the profile settings or change these permissions. Use the **Permissions** window to allow all permissions, or customize permissions by choosing certain permissions that aren't allowed.
1. Select **Save**.

#### Edit minimum version

Specify the minimum version required for the extension. The extension will be disabled if it's a version older than what's specified, even if its installation policy is forced. The format of the version string is the same as the one used in the extension manifest. Follow these steps to configure this setting:

1. Select an extension.
1. Select **Edit minimum version**. In the **Minimum version required** window, enter the minimum version in the textbox.
1. Select **Save**.

#### Manage toolbar state

Choose how an extension is displayed in the toolbar. Follow these steps to configure this setting:

1. Select an extension.
2. Under **Toolbar state**, choose one of the following options:

   - Hidden: This is the default setting.
   - Shown: Show the extension on installation. Users can hide it from the toolbar.
   - Force shown: Always show extension on the toolbar. Users won't be able to hide it from the toolbar.

3. Select **Save**.

### Manage extension requests

If you have blocked any extension for your organization, you can allow users to request access to them. To turn on this feature, go to a configuration profile and navigate to the **Requests** tab in the **Extensions** pivot. Select **Manage request settings** and set the value to **Enabled** to allow users to request blocked extensions. Once enabled, you can view all extensions that your users have requested on this page.

You can also choose to receive email notifications when new requests come in. To do this, use these steps:

1. Check the box that says **Notify me about incoming requests by email**.
2. Specify the email address where you would like to receive the notifications.
3. Set the frequency at which you would like to receive these notifications (daily, weekly, or monthly).
4. Select **Save**.

To set the installation policy on a requested extension, use these steps:

1. Select an extension.
2. Select **Manage installation policy** and choose one of the following options from the dropdown list:
   - Allow: Users can install the extension. This is the default setting.
   - Block: Users can't install the extension. You can remove the extension if a user previously installed it. Also, you can write a message that displays when users try to install the extension.
   - Force: The extension is automatically installed. Users can't remove it. You can optionally specify an update URL for the initial extension installation and use it for subsequent updates.
   - Normal: The extension is automatically installed. Users can disable it. You can optionally specify an update URL for the initial extension installation and use it for subsequent updates.

3. Select **Save**.

#### Manage sidebar apps

To manage sidebar apps for a profile, go to the profile and navigate to the **Extensions** pivot. You can allow, block, or force enable specific sidebar apps.

Use the following steps to manage sidebar apps:

1. Select **Select extension**.
1. Under **Select an extension**, navigate to the **Sidebar apps** pivot and select an app.
1. Select **Select**.

After selecting a sidebar app, you can configure its installation policy to Allow, Block, or Force.

## See also

- [Microsoft Edge management service](microsoft-edge-management-service.md)
