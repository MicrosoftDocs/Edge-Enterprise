---
title: "Microsoft Edge and split tunnel VPN support for WebRTC"
ms.author: juso
author: dan-wesley
manager: harneets
ms.date: 01/24/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Enable Microsoft Edge and split tunnel VPN support for WebRTC (Web Real-Time Communication)"
---

# Split tunnel VPN support for WebRTC (Web Real-Time Communication)
  
This article describes Microsoft Edge and split tunnel VPN support for WebRTC. This support lets enterprise customers get the benefit of VPN split tunneling for peer-to-peer traffic on Microsoft Edge. VPN split tunneling improves peer-to-peer media streaming quality for users and reduces VPN server load.

> [!NOTE]
> This article applies to Microsoft Edge version 96 or later.

## What is VPN split tunneling and why should I use it?

VPN split tunneling is a feature that enables users to use two different networks for traffic instead of having all the traffic routed through a VPN. Windows has supported this feature for native applications, and VPN split tunneling is also offered for Microsoft 365 applications over VPN split tunneling on on Windows. For more information, see [Overview: VPN split tunneling with Office 365 - Microsoft 365 Enterprise](/microsoft-365/enterprise/microsoft-365-vpn-split-tunnel?view=o365-worldwide&preserve-view=true). Microsoft Edge has also honored the VPN split tunneling configuration but support for the peer-to-peer traffic was missing.

We’ve heard about customers needs for routing peer-to-peer user traffic through their corporate network or cloud infrastructure over VPN. They were frustrated about the quality of video conference calls of their users on browsers compared to native applications. As demonstrated by  the native experience, VPN split-tunneling for peer-to-peer traffic can improve the quality of user video calls by routing it through normal Internet connections instead of VPN. It also can reduce the overall VPN server load by routing designated traffic off a VPN. Microsoft Edge now brings this peer-to-peer traffic improvement to enterprise customers.

## How to configure VPN split tunneling on Microsoft Edge

To enable VPN split tunneling and configure the networks for your users, we recommend you start with the guidance in [Implementing VPN split tunneling for Office 365 - Microsoft 365 Enterprise](/microsoft-365/enterprise/microsoft-365-vpn-implement-split-tunnel?view=o365-worldwide&preserve-view=true). With the proper routing table configured based on the information described in the preceding article, you just need to take the additional step of enabling the [WebRtcRespectOsRoutingTableEnabled](https://docs.microsoft.com/en-us/deployedge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) policy. This policy enables support for Windows OS routing table rules when making peer to peer connections via WebRTC. Now you’re ready to provide improved peer-to-peer media streaming experience on Microsoft Edge!

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
