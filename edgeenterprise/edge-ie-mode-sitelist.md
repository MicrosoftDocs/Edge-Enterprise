---
title: "Enterprise site configuration strategy"
ms.author: shisub
author: shisub
manager: archandr
ms.date: 07/18/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "A step-by-step guide to configuring the Enterprise Mode Site list for Internet Explorer mode."
---

# Enterprise site configuration strategy

This article describes changes to the Enterprise Mode Site List to support Internet Explorer mode for Microsoft Edge version 77 and later.

For more information on the schema for the Enterprise Mode Site List XML file, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

## Configuration strategy

The following steps are part of a site configuration strategy for IE mode:
1. Prepare your site list
2. Configure neutral sites
3. (Optional) Use cookie sharing if necessary

## Prepare your site list

If you already have an Enterprise Mode site list for IE11 or Microsoft Edge Legacy, you can reuse it to configure IE mode.

However, if you don't have a site list, you can use the [Enterprise Site Discovery tool](/deployedge/edge-ie-mode-site-discovery) to populate your site list.

## Configure neutral sites

In order for IE mode to work properly, authentication / single sign-on (SSO) servers need to be explicitly configured as neutral sites. Otherwise, IE mode pages try to redirect to Microsoft Edge, and authentication will fail.

A neutral site uses the browser where the navigation started - either Microsoft Edge or IE mode. Configuring neutral sites ensures that all applications using these authentication servers, both modern and legacy, continue to work.

You can configure neutral sites by setting the *Open In* dropdown to 'None' in the Enterprise Mode Site List Manager tool or by directly updating the site list XML:

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

To identify authentication servers, inspect the network traffic from an application using the IE11 Developer Tools. If you need more time to identify your authentication servers, you can configure a policy to keep all in-page navigations in IE mode to allow your users to continue their workflows uninterrupted. To minimize the use of IE mode when unnecessary, disable this setting once you've identified and added your authentication servers to the site list. For more information, see [Keep in-page navigation in IE mode](/deployedge/edge-learnmore-inpage-nav).

>[!NOTE]
   >Enterprise Mode schema v.1 isn't supported for IE mode integration. If you are currently using schema v.1 with Internet Explorer 11, you must upgrade to schema v.2. For more information, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

## (Optional) Use cookie sharing if necessary

By default, the Microsoft Edge and Internet Explorer processes don't share session cookies, and this lack of sharing can be inconvenient in some cases while using IE mode. For example, when a user has to reauthenticate in IE mode when previously they're accustomed to doing so or when signing out of a Microsoft Edge session doesn't sign out of the Internet Explorer mode session for critical transactions. In these scenarios, you can configure specific cookies set by SSO to be sent from Microsoft Edge to Internet Explorer so the authentication experience becomes more seamless by eliminating the need to reauthenticate. For more information, see [Cookie sharing from Microsoft Edge to Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare).

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [About IE mode](./edge-ie-mode.md)
- [Additional Enterprise Mode information](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
