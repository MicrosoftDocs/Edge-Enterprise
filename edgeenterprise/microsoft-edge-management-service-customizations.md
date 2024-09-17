---
title: "Customization settings"
ms.author: katherinegan
author: dan-wesley
manager: archandr
ms.date: 09/16/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Provides steps for configuring customizations for Microsoft Edge management service."
---

# Customization settings

This article gives the steps for configuring Microsoft Edge management service customizations.

## Add customization settings

To configure groups of settings that create specific customizations for a profile, select the profile you want to work with and navigate to the **Customization settings** tab. Then, select the page that contains settings for the experiences you would like to create.

### Manage enterprise secure AI settings

To manage AI settings for a profile, navigate to the **enterprise secure AI** tab. You can configure AI related settings on this page. Once any setting is edited on this page, all of the configurations will appear in the **Policies** tab in that profile. If you edit a setting on this page that already has an existing configuration, the new edit will override the existing value.

**Blocking Access to Third-Party LLM Chatbots** will add a dynamic set of URLs to the URLBlocklist policy for blocking access to well-known AI chatbots. This dynamic URL-set is managed by Microsoft and may be updated over time. As of the time of writing, the list includes:

- https://bard.google.com
- https://chat.openai.com
- https://gemini.google.com
- https://claude.ai
- https://perplexity.ai
- https://jasper.ai
- https://you.com
- https://writesonic.com/chat
- https://cohere.com/coral

Disabling this feature will automatically remove these URLs from the policy, even if they were manually added beforehand. Values not included in this dynamic URL set will remain unaffected.

#### Manage settings for Copilot

The page will detect whether your organization has access to Copilot and the Microsoft Edge sidebar. Based on this information, one of the following states will exist:

- If Copilot and the Microsoft Edge sidebar are enabled, all settings in this section will be available to configure.

- If Copilot is enabled and the Microsoft Edge sidebar is disabled, the unapplicable settings will be disabled. However, the option to enable the sidebar will appear, and if enabled, will unlock the ability to configure the now applicable setting.

- If Copilot is disabled, all settings in this section won't be available to configure.

- If it can't be identified that Copilot is enabled for your organization, the default settings for this section will apply and won't be available to configure.

#### Manage settings for other AI features

The settings in this section let you configure Microsoft Edge settings that involve the use of AI. To configure a setting:

1. Check/uncheck the box corresponding to the setting that you want to enable/disable respectively.
2. Select **Save changes.** The settings in this section allow you to configure Microsoft Edge settings that involve the use of AI.

### Customize organization branding

To customize the browser with your organization's branding assets, go to the **Organization branding** tab. You can use the default Edge for Business branding elements, or use custom branding assets. A preview of how the browser elements will look on a user's account is shown on the page.

If you don't have any organization branding policies enabled, the default Edge for Business branding will be displayed. When you choose **Use custom branding**, any existing branding assets associated with your Microsoft Entra ID will be imported and displayed in the preview. These changes won't take effect until you choose **Save changes**.

From **Use custom branding**, you can customize each of the following browser elements with the brand assets you choose:

- Organization name: This name will be displayed in the profile pill.
- Accent color: This color will appear in the profile flyout header.
- Organization logo: This logo will appear in the profile flyout header. To ensure that your logo displays properly:
  - You must upload an SVG (Scalable Vector Graphics) file with a maximum size of 150 KB.
  - The uploaded file should have dimensions with width >= height. We recommend choosing a rectangular logo.
  - For non-square logos, file dimensions must be included at the SVG level ("<svg width="500 pixels" height="200 pixels"...)
- Taskbar icon: This logo will overlay the Edge for Business icon on the taskbar. To ensure that your logo displays properly:
  - You must upload an SVG file with a maximum size of 150 KB.
  - The uploaded file should be a square logo that has dimensions with a 1:1 ratio. The file resolution should be no greater than 480 pixels x 480 pixels.

After you finish customizing the browser elements with your organization branding assets, confirm that the preview displays the correct visual appearance and then select **Save changes**.


### Manage automatic profile switching settings

To manage profile switching behaviors for a profile, navigate to the **automatic profile switching** tab. You can choose which profile you want specific hostnames to open in for your users. 

#### Manage default switching settings

The toggles on this page control a category of hostnames. When the toggle is turned on, the hostnames that apply to that category will automatically open in a user's work profile. When the toggle is turned off, no profile switching will occur, independent of the profile it is open in. To override an individual site that falls into one of the hostname categories, add it to the **Switch list**.

#### Manage custom switch list

You can specify individual hostnames and the profile you would like them to open in on the **Switch list** tab of this page. To add a hostname to this list:

1. Select **add entry**.
2. Enter the hostname.
3. Choose the profile you would like the hostname to open in. If you would like the profile to not switch on the hostname, select **Allow user preference**.
4. (Optional) If the profile selected is work, you can optionally choose to specify the domain that the hostname opens in. This may be necessary for users with multiple work profiles. The domain entered should match the format *\*username@company.com* (note: the \* is required).
5. Select **Add**.

### Configure security settings

To add settings that help protect against security threats, navigate to the security settings tab. Here you can choose to configure settings that help protect your users against security vulnerabilities.

#### Enable enhanced security mode

[Enhanced security mode](/deployedge/microsoft-edge-security-browse-safer) helps reduce the risk of an attack caused by memory-related vulnerabilities by automatically applying stricter security settings on unfamiliar sites. To enable this mode:

1. Turn on the **Enhanced security mode toggle**.
2. Specify the **Balanced** or **Strict** mode depending on the level of security you would like.
3. Select **Save changes**.

#### Block alternative browser use

> [!NOTE]
> This setting is only available for customers with a Microsoft Intune license.

Users with configured security settings may still be at risk on other browsers. To mitigate this risk, you can choose to block alternative browser use. When this setting is enabled, a new configuration policy will be created in Intune. Any modifications you make to this new policy in Intune or in a configuration profile with identical groups in the Microsoft Edge management service may lead to unexpected behaviors.

## See also

- [Microsoft Edge management service](microsoft-edge-management-service.md)