---
title: "Allow list for Microsoft Edge endpoints"
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 11/25/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Allow list for Microsoft Edge endpoints"
---

# Allow list for Microsoft Edge endpoints

Microsoft Edge requires connectivity to the Internet to support its features. This article identifies the domain URLs that you need to add to the Allow list to ensure communications through firewalls and other security mechanisms.

> [!NOTE]
> This applies  to Microsoft Edge version 77 or later.

## Domain URLs to allow

Allow the following domain URLs for Microsoft Edge.

### Update Service

The service that Microsoft Edge uses to check for new updates.

- `https://msedge.api.cdp.microsoft.com`

### Experimentation and Configuration service

- `https://config.edge.skype.com`

### Download locations for Microsoft Edge

Locations Microsoft Edge can be downloaded from during an initial install or when an update is available. The download location is determined by the Update Service.

#### HTTP

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### HTTPS

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > To simplify the allow list for download locations a wild card can be used: `*.dl.delivery.mp.microsoft.com`

### Download locations for Microsoft Edge Extensions

Locations Microsoft Edge Extensions can be downloaded from during an initial install or when an update is available. The download location is determined by the Update Service.

#### HTTP

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### HTTPS

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > To simplify the allow list for download locations a wild card can be used: `*.dl.delivery.mp.microsoft.com`

### Optionally for Download Delivery Optimization

For information about delivery optimization, see [Delivery Optimization for Windows 10 updates](https://aka.ms/waas-do).

- Client to Service communication: `*.do.dsp.mp.microsoft.com` (HTTP Port 80, HTTPS Port 443)
- Client to Client communication: TCP port 7680 should be open for inbound traffic

### Sync

These endpoints manage the reading and writing of synced data, rights management for secure data, and notifying the browser when new sync data is available.

- Edge sync service endpoints:

  - `https://edge-enterprise.activity.windows.com`
  - `https://edge.activity.windows.com`

- Azure Information Protection endpoints:

  - `https://api.aadrm.com` (for most tenants)
  - `https://api.aadrm.de` (for tenants in Germany)
  - `https://api.aadrm.cn` (for tenants in China)

- [Windows Notification Service endpoints](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

## Other browser support services

Provide metadata for browser features such as tracking protection, certificate revocation lists, and other browser component updates. Provide downloadable spellcheck dictionaries and ad-blocking block lists. Provide services to support browser features such as collections, autofill, and extension store.

- `http://edge.microsoft.com/`
- `https://edge.microsoft.com/`

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge documentation landing page](https://docs.microsoft.com/DeployEdge/)
- [Manage connection endpoints for Windows 10 Enterprise, version 1903](https://docs.microsoft.com/windows/privacy/manage-windows-1903-endpoints)
