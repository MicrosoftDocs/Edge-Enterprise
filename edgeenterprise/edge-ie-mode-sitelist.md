---
title: "Enterprise site configuration strategy"
ms.author: shisub
author: shisub
manager: srugh
ms.date: 03/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "A step-by-step guide to configuring the Enterprise Mode Site list for Internet Explorer mode."
---

# Enterprise site configuration strategy

This article describes changes to the Enterprise Mode Site List to support Internet Explorer mode for Microsoft Edge version 77 and later.

For more information on the schema for the Enterprise Mode Site List XML file, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

> [!NOTE]
> This article applies to Microsoft Edge version 77 or later.
<!--
## Updated schema elements

The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:

| **Element** | **Description** |
| --- | --- |
| \<open-in app="**true**"\> | A child element that controls what browser is used for sites. This element is required for sites that need to **open in IE11**.|

**Example:**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

The following table shows the possible values of the \<open-in\> element:

| **Value** | **Description** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | Opens the site in IE mode or a full IE11 window. To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | Opens the site in a full IE11 window |
| **\<open-in\>MSEdge\</open-in\>** | Opens the site in Microsoft Edge |
| **\<open-in\>None or not specified\</open-in\>** | Opens the site in the default browser or in the browser where the user navigated to the site. |
|**\<open-in\>Configurable\</open-in\>** | Allows the site to participate in IE mode engine determination. To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).  |

>[!NOTE]
> The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_. Adding it to the other 'open-in' elements won't change browser behavior.   -->

## Configuration strategy

The following steps are part of a site configuration strategy for IE mode:
1. Prepare your site list
2. Configure neutral sites
3. (Optional) Use cookie sharing if necessary

<!--
Step 1.  – if you don’t have one use Site Discovery Step-by-Step
Step 2 – Neutral sites + sticky mode
        Use more examples and explain sticky mode better
Step 3 – If that doesn’t cover your needs, then use Cookie sharing -->

## Prepare your site list

If you already have an Enterprise Mode site list for IE11 or Microsoft Edge Legacy, you can reuse it to configure IE mode.

However, if you don't have a site list, you can use the [Enterprise Site Discovery tool](https://docs.microsoft.com/deployedge/edge-ie-mode-site-discovery) to populate your site list.

## Configure neutral sites

In order for IE mode to work properly, authentication / Single Sign-On (SSO) servers will need to be explicitly configured as neutral sites. Otherwise, IE mode pages will try to redirect to Microsoft Edge, and authentication will fail.

A neutral site will use the browser where the navigation started - either Microsoft Edge or IE mode. Configuring neutral sites ensures that all applications using these authentication servers, both modern and legacy, continue to work.

You can configure neutral sites by setting the *Open In* dropdown to 'None' in the Enterprise Mode Site List Manager tool or by directly updating the site list XML:

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

To identify authentication servers, inspect the network traffic from an application using the IE11 Developer Tools. If you need more time to identify your authentication servers, you can configure a policy to keep all in-page navigations in IE mode to allow your users to continue their workflows uninterrupted. To minimize the use of IE mode when unnecessary, disable this setting once you've identified and added your authentication servers to the site list. For more information, see [Keep in-page navigation in IE mode](https://docs.microsoft.com/deployedge/edge-learnmore-inpage-nav).

>[!NOTE]
   >Enterprise Mode schema v.1 isn't supported for IE mode integration. If you are currently using schema v.1 with Internet Explorer 11, you must upgrade to schema v.2. For more information, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).

## (Optional) Use cookie sharing if necessary

By default, the Microsoft Edge and Internet Explorer processes don't share session cookies, and this lack of sharing can be inconvenient in some cases while using IE mode. For example, when a user has to reauthenticate in IE mode when previously they are accustomed to doing so or when signing out of a Microsoft Edge session doesn’t sign out of the Internet Explorer mode session for critical transactions. In these scenarios, you can configure specific cookies set by SSO to be sent from Microsoft Edge to Internet Explorer so the authentication experience becomes more seamless by eliminating the need to reauthenticate. For more information, see [Cookie sharing from Microsoft Edge to Internet Explorer](https://docs.microsoft.com/deployedge/edge-ie-mode-add-guidance-cookieshare).

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [About IE mode](./edge-ie-mode.md)
- [Additional Enterprise Mode information](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
