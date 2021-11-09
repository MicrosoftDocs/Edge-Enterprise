---
title: "Cookie sharing from Microsoft Edge to Internet Explorer"
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/04/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Learn how to share cookies from Microsoft Edge to Internet Explorer"
---

# Cookie sharing from Microsoft Edge to Internet Explorer

>[!Note]
> The Internet Explorer (IE) 11 desktop application will be retired and go out of support on June 15, 2022. To see what’s in scope and out of scope when IE 11 is retired, see [Internet Explorer 11 desktop app retirement FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549). The same IE 11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode. To learn more, see [The future of Internet Explorer on Windows 10 is in Microsoft Edge](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

This article explains how to configure session cookie sharing from a Microsoft Edge process to an Internet Explorer process, while using Internet Explorer mode.

> [!NOTE]
> This article applies to Microsoft Edge version 87 or later.

## Prerequisites

- Windows updates

  - Windows 10 version 2004, Windows Server version 2004 - KB4571744 or higher
  - Windows 10 version 1909, Windows Server version 1909 – KB4566116 or higher
  - Windows 10 version 1903, Windows Server version 1903 – KB4566116 or higher
  - Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019 - KB4571748 or higher
  - Windows 10 version 1803 – KB4577032 or higher
  - Windows 10 Enterprise 2016 LTSC and Windows Server 2016 - KB4580346 or higher
  - Windows 10 Enterprise 2015 LTSB - KB4580327 or higher
  - Windows 8.1 and Windows Server 2012 R2 - KB4586768 or higher
  - Windows 10 Enterprise 2016 LTSC and Windows Server 2016 - KB4580346 or higher
  - Windows 10 Enterprise 2015 LTSB - KB4580327 or higher
  - Windows 8.1 and Windows Server 2012 R2 - KB4586768 or higher

- Microsoft Edge version 87 or later
- [IE mode](./edge-ie-mode.md) configured with Enterprise Mode Site List

## Overview

A common configuration in large organizations is to have an application that works on a modern browser link to another application, which might be configured to open in Internet Explorer mode with Single Sign On (SSO) enabled as part of the workflow.

By default, the Microsoft Edge and Internet Explorer processes don't share session cookies, and this lack of sharing can be inconvenient in some cases. For example, when a user has to reauthenticate in Internet Explorer mode or when signing out of a Microsoft Edge session doesn’t sign out of the Internet Explorer mode session. In these scenarios, you can configure specific cookies set by SSO to be sent from Microsoft Edge to Internet Explorer so the authentication experience becomes more seamless by eliminating the need to reauthenticate.

> [!NOTE]
> Session cookies can only be shared from Microsoft Edge to Internet Explorer. Sharing session cookies in reverse (from Internet Explorer to Microsoft Edge) isn't possible.

## How cookie sharing works

The Enterprise Mode site list XML is extended to allow more elements to specify cookies that need to be shared from a Microsoft Edge session with Internet Explorer.  

The first time an Internet Explorer mode tab is created in a Microsoft Edge session, all matching cookies are shared to the Internet Explorer session. After that, anytime a cookie that matches a rule is added, deleted, or modified it is sent as an update to the Internet Explorer session. The set of shared cookies is also reevaluated when the site list is updated.

### Updated schema elements

The following table describes the \<shared-cookie\> element added to support the cookie sharing feature.

| Element| Description |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br>OR<br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |**(Required)** A \<shared-cookie\> element requires, at minimum, a *domain* (for domain cookies) or a *host* (for host-only cookies) attribute and a *name* attribute.<br>These attributes must be exact matches to the cookie's domain and name respectively. **Note** that subdomains do not match.<br><br>The *domain* attribute is used for domain cookies (and a leading dot is allowed but optional).<br>The *host* attribute is used for host-only cookies (and a leading dot is an error). Specifying neither or both will result in an error.<br>* A cookie is a domain cookie if a domain was specified in the cookie string (via HTTP Set-Cookie response header or document.cookie JS API). A domain cookie applies to the specified domain and all subdomains. If a domain wasn't specified in the cookie string, the cookie is a host-only cookie and only applies to the specific host that it was set for. Some classes of URLs such as single-word hostnames (for example, http://intranetsite) and IP addresses (for example, http://10.0.0.1) can only set host-only cookies.    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | **(Optional)** A *path* attribute may be specified. If no path attribute is specified (or if the path attribute is empty), any cookies matching domain/host and name match the policy, regardless of path (wildcard rule).<br><br>If a path is specified, it must be an exact match.<br>If a cookie matches a rule with a path, that takes precedence over a rule without a path. |

#### Sharing example

```xml
<site-list version="1">
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c">
</shared-cookie>
</site-list>
```

## See also

- [About IE mode](./edge-ie-mode.md)
- [Configurable sites information](./edge-learnmore-configurable-sites-ie-mode.md)
- [Additional Enterprise Mode information](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
