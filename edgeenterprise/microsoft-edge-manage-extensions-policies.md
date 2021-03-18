---
title: "Use group policies to manage Microsoft Edge extensions"
ms.author: aspoddar
author: dan-wesley
manager: balajek
ms.date: 03/17/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Use group policies to manage Microsoft Edge extensions in the enterprise"
---

# Use group policies to manage Microsoft Edge extensions

This article describes the options and steps for managing extensions by using group policies. These options  assume that you already have Microsoft Edge managed for your users.

> [!NOTE]
> This article applies to Microsoft Edge version 77 or later.

## Before you begin

The extensions options assume that you already have Microsoft Edge managed for your users. For more information,  see the [Configure Microsoft Edge policy settings on Windows](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge).

The configuration steps in this article are for Windows, for the corresponding implementation in MAC/Linux, see the [Microsoft Edge browser policy](https://docs.microsoft.com/deployedge/microsoft-edge-policies) reference.

## Block extensions based on their permissions

You can control what extensions your users can install based on permissions using the [ExtensionSettings](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensionsettings) policy. If an installed extension needs a permission that’s blocked, it just won't run. The extension isn't removed, just disabled.

Use the following steps as a guide for blocking an extension.

1. Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions**  and then select **Configure extension management settings**.
2. Enable the policy, then enter the permissions that you want allowed or blocked, by using a JSON string that gets compressed. The following example shows the JSON to block any extension that needs the use of permission "usb" and the compressed string.

   ```json
   { 

        "*": { 

             "blocked_permissions": ["usb"] 

        } 

   } 
   ```

   ```json
   {"*":{"blocked_permissions":["usb"]}} 
   ```

   > [!NOTE]
   > To block all extensions that use the permission, use an asterisk for the extension ID, as shown in the previous example. If you specify one extension ID, the policy will only apply to that extension. You can block more than one, but they need to be separate entries.

## Prevent extensions from altering web pages

This setting prevents extensions from reading and changing  data from sensitive websites and domains. Blocking unwanted actions is done by blocking actions such as script injection into your websites, reading the cookies, or making web-request modifications. This setting doesn’t prevent your users from installing or removing extensions, it only prevents extensions from altering the specified websites. 

You can configure the following settings in the ExtensionSettings policy to prevent (or allow) alterations of websites or domains:

- **Runtime_blocked_hosts**. This setting blocks extensions from making changes or reading data from the websites you specify.
- **Runtime_allowed_hosts**. This setting allows extensions to make changes or read data from the websites you specify. The following format is used for specifying your site(s) in the JSON string in the policy:

  ```json
  [http|https|ftp|*]://[subdomain|*].[hostname|*].[eTLD|*] [http|https|ftp|*],
  ```

  > [!NOTE]
  > `[hostname|*], and [eTLD|*]` sections are required, but `[subdomain|*]` section is optional.

The following table shows examples of valid host patterns and matching patterns.

|Valid host patterns|Matches|Doesn't match|
|--|--|--|
|  `*://*.example.*` | `http://example.com`<br>`https://test.example.co.uk`   | `https://example.microsoft.com`<br>`http://example.microsoft.co.uk`  |
| `http://example.*` | `http://example.com`<br>`http://example.ly` | `https://example.com`<br>`http://test.example.com`   |
| `http://example.com`   | `http://example.com` | `https://example.com`<br>`http://test.example.co.uk` |
| `*://*`   | All URLs  |   |

Use the following steps as a guide to block or allow extensions to access a website or domain.

1. Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions**, and then select **Configure extension management settings**.  
2. Enable the policy, then enter the permissions that you want allowed or blocked, compressing the permissions to a single JSON string.

The following examples show how to block extensions on a hostname and how to block extensions on the same domain.

### JSON example to block hostname

The next example shows the JSON and compressed JSON to block any extension from accessing the www.microsoft.com hostname.

```json
{ 
    "*":{ 
            "runtime_blocked_hosts":["www.microsoft.com"] 
    } 
} 
```

```json
{"*":{"runtime_blocked_hosts":["www.microsoft.com"]}} 
```

> [!NOTE]
> To block all extensions from accessing a webpage, use an asterisk for the extension ID, as shown in the previous example.  If you specify one extension ID instead of an asterisk, the policy will only apply to that extension. You can block more than one extension, but they need to be separate entries. .

### JSON example to block extensions on same domain

The next example shows the JSON and compressed JSON to block two extensions from running on the same domain.

```json
{ 

    "aapbdbdomjkkjkaonfhkkikfgjllcleb": { 

        "runtime_blocked_hosts": ["*://*.importantwebsite"] 

    }, 

    "bfbmjmiodbnnpllbbbfblcplfjjepjdn": { 

        "runtime_blocked_hosts": ["*://*.importantwebsite"] 

    } 

} 
```

```json
{"aapbdbdomjkkjkaonfhkkikfgjllcleb": {"runtime_blocked_hosts": ["*://,*.importantwebsite"]},"bfbmjmiodbnnpllbbbfblcplfjjepjdn": {"runtime_blocked_hosts": ["*://*.importantwebsite"]}} 
```

## Allow or block extensions in group policy

Use the following steps as a guide to allow all extensions except those you want to block.


## Force-install an extension

Use the following steps as a guide to force-install an extension. 

## Block extensions from a specific store or update URL

To block extensions from a particular store or URL, you only need to block the *update_url* for that store.  

## See also

- [Manage Microsoft Edge extensions in the enterprise](microsoft-edge-manage-extensions.md)
- [Create a web store to host Microsoft Edge extensions](microsoft-edge-manage-extensions-webstore.md)
- [FAQ for Microsoft Edge Extensions](microsoft-edge-manage-extensions-faq.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
