---
title: "Cookie sharing between Microsoft Edge and Internet Explorer"
ms.author: shisub
author: dan-wesley
manager: archandr
ms.date: 07/18/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Learn how to share cookies between Microsoft Edge and Internet Explorer"
---

# Cookie sharing between Microsoft Edge and Internet Explorer

This article explains how to configure session cookie sharing between a Microsoft Edge process and an Internet Explorer process, while using Internet Explorer mode.

## Prerequisites

To share session cookies from Microsoft Edge to Internet Explorer:

- Windows updates

  - Windows 11
  - Windows 10 version 2004, Windows Server version 2004 - KB4571744 or higher
  - Windows 10 version 1909, Windows Server version 1909 – KB4566116 or higher
  - Windows 10 version 1903, Windows Server version 1903 – KB4566116 or higher
  - Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019 - KB4571748 or higher
  - Windows 10 version 1803 – KB4577032 or higher
  - Windows 10 Enterprise 2016 LTSC and Windows Server 2016 - KB4580346 or higher
  - Windows 10 Enterprise 2015 LTSB - KB4580327 or higher
  - Windows 8.1 and Windows Server 2012 R2 - KB4586768 or higher  
- Microsoft Edge version 87 or later
- [IE mode](./edge-ie-mode.md) configured with Enterprise Mode Site List

To share session cookies between Microsoft Edge and Internet Explorer:

- Windows updates
  
  - Windows 11 - KB5010414 or higher
  - Windows Server 2022 - KB5010421 or higher
  - Windows 10 version 20H2 - KB5010415 or higher
  - Windows 10 version 21H1 - KB5010415 or higher
  - Windows 10 version 21H2-  KB5010415 or higher
  - Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019 - KB5028168 or higher
  - Windows 10 Enterprise 2016 LTSC and Windows Server 2016 - KB5031362 or higher
- Microsoft Edge version 99 or later
- [IE mode](./edge-ie-mode.md) configured with Enterprise Mode Site List

## Overview

A common configuration in large organizations is to have an application that works on a modern browser link to another application, which might be configured to open in Internet Explorer mode with Single Sign On (SSO) enabled as part of the workflow.

By default, the Microsoft Edge and Internet Explorer processes don't share session cookies, and this lack of sharing can be inconvenient in some cases. For example, when a user has to reauthenticate in Internet Explorer mode or when signing out of a Microsoft Edge session doesn't sign out of the Internet Explorer mode session. In these scenarios, you can configure specific cookies set by SSO to be sent from Microsoft Edge to Internet Explorer so the authentication experience becomes more seamless by eliminating the need to reauthenticate.

> [!NOTE]
> Before Microsoft Edge version 99, session cookies can only be shared from Microsoft Edge to Internet Explorer. Starting with Microsoft Edge version 99, sharing session cookies in reverse (from Internet Explorer to Microsoft Edge) is possible.

> [!NOTE]
> Persistent cookies, which have been created with an Expires-attribute, are not in scope for this feature and cannot be shared between Microsoft Edge and Internet Explorer.
## How cookie sharing works

The Enterprise Mode site list XML is extended to allow more elements to specify session cookies that need to be shared between Microsoft Edge and Internet Explorer.

The first time an Internet Explorer mode tab is created in a Microsoft Edge session, all matching cookies are shared to the Internet Explorer session. After that, anytime a cookie that matches a rule is added, deleted, or modified it's sent as an update to the Internet Explorer session. The set of shared cookies is also reevaluated when the site list is updated.

### Updated schema elements

The following table describes the \<shared-cookie\> element added to support the cookie sharing feature.

| Element| Description |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br>OR<br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |**(Required)** A \<shared-cookie\> element requires, at minimum, a *domain* (for domain cookies) or a *host* (for host-only cookies) attribute and a *name* attribute.<br>These attributes must be exact matches to the cookie's domain and name respectively. **Note** that subdomains do not match.<br><br>The *domain* attribute is used for domain cookies (and a leading dot is allowed but optional).<br>The *host* attribute is used for host-only cookies (and a leading dot is an error). Specifying neither or both will result in an error.<br>* A cookie is a domain cookie if a domain was specified in the cookie string (via HTTP Set-Cookie response header or document.cookie JS API). A domain cookie applies to the specified domain and all subdomains. If a domain wasn't specified in the cookie string, the cookie is a host-only cookie and only applies to the specific host that it was set for. Some classes of URLs such as single-word hostnames (for example, http://intranetsite) and IP addresses (for example, http://10.0.0.1) can only set host-only cookies.    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | **(Optional)** A *path* attribute may be specified. If no path attribute is specified (or if the path attribute is empty), any cookies matching domain/host and name match the policy, regardless of path (wildcard rule).<br><br>If a path is specified, it must be an exact match.<br>If a cookie matches a rule with a path, that takes precedence over a rule without a path. |
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1" **source-engine**="MSEdge"\>\</shared-cookie\><br><br>OR<br><br>\<shared-cookie **domain**=".contoso.com" **name**="cookie1" **source-engine**="IE11"\>\</shared-cookie\><br><br>OR<br><br>\<shared-cookie **domain**=".contoso.com" **name**="cookie1" **source-engine**="Both"\>\</shared-cookie\> | **(Optional)** The source-engine attribute specifies how the session cookies are shared between Microsoft Edge and Internet Explorer. Where:<br><br>- **MSEdge**. Share session cookies from Microsoft Edge to Internet Explorer.<br>- **IE11**.  Share session cookies from Internet Explorer to Microsoft Edge.<br>- **Both**. Share session cookies to and from Microsoft Edge and Internet Explorer.<br>- **Default or not specified**. Session cookies will be shared from Microsoft Edge to Internet Explorer. |

#### Sharing example

```xml
<site-list version="1"> 
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie>  
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c"> 
</shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie3" source-engine="MSEdge"></shared-cookie> 
</site-list> 
```

## See also

- [About IE mode](./edge-ie-mode.md)
- [Configurable sites information](./edge-learnmore-configurable-sites-ie-mode.md)
- [Additional Enterprise Mode information](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
