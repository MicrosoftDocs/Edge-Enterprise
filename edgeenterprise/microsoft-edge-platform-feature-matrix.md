---
title: "Platform support for Microsoft Edge features"
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 03/24/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Summary of platform support for Microsoft Edge features"
---

# Platform support for Microsoft Edge features

This article summarizes platform support for Microsoft Edge features.

> [!NOTE]
> This article applies to Microsoft Edge version 77 or later.

## Feature matrix for platforms

The following tables summarize feature support for the Windows and macOS platforms.

> [!NOTE]
> Android and iOS are currently not represented in the support tables but these platforms are being worked on and this information will be added when available.

| Security features |Win 10|Win 8.1|Win 7|macOS|URL|
|--------|-------|--------|-----|-------|---|
|Azure Active Directory (Azure AD) Conditional Access|Yes|Yes|Yes|Yes|[Azure AD Conditional Access](https://docs.microsoft.com/deployedge/ms-edge-security-conditional-access#accessing-conditional-access-protected-resources-in-microsoft-edge)|
|Microsoft Defender Application Guard|Yes (1890+)|No|No|No|[Microsoft Defender Application Guard](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-defender-application-guard) |
|Microsoft Defender SmartScreen|Yes|Yes|Yes|Yes|[Microsoft Defender SmartScreen](https://docs.microsoft.com/deployedge/microsoft-edge-security-smartscreen) |
|Microsoft Endpoint DLP|Yes|No|No|No|[Microsoft Endpoint DLP](https://docs.microsoft.com/deployedge/microsoft-edge-security-dlp#microsoft-endpoint-data-loss-prevention-endpoint-dlp)|
|Password Monitor|Yes|Yes|Yes|Yes|[Password Monitor](https://blogs.windows.com/msedgedev/2021/01/21/edge-88-privacy/)|
|Password Generator|Yes|Yes|Yes|Yes	|[Password Generator](https://blogs.windows.com/msedgedev/2021/01/21/edge-88-privacy/)|
|Windows Information Protection (WIP)|Yes (1607+)|No|No|No|[WIP](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#system-requirements)|



|Identity features| Win 10 | Win 8.1 | Win 7 | macOS | URL |
|--|--|--|--|--|--|
|Automatic Sign In (hybrid/AAD-J)|Yes|Yes|Yes|No|[hybrid/AAD-J](https://docs.microsoft.com/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Automatic Sign In (domain joined)|Yes|Yes|Yes|	No|[domain joined](https://docs.microsoft.com/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Automatic Sign In (OS default account is MSA)|Yes (1709+)|No|No|No|[MSA](https://docs.microsoft.com/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|Browser to Web Single Sign On (SSO)|Yes|Yes|Yes|Yes|[Browser-Web SSO](https://www.microsoft.com/microsoft-365/roadmap?featureid=66332)|
|Guided Switch/"Automatic Profile Switching"|Yes|Yes|Yes|Yes|[Using multiple profiles at work and at home](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) |
|Multiple Profiles|Yes|Yes|Yes|Yes|[Using multiple profiles at work and at home](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) |
|On-premises sync for Active Directory (AD)|Yes|Yes|Yes|No|[On-premises sync for Active Directory (AD) users](https://docs.microsoft.com/deployedge/microsoft-edge-on-premises-sync) |
|Seamless SSO|Yes (1709+)|Yes|Yes|Yes|[Seamless SSO](https://docs.microsoft.com/deployedge/microsoft-edge-security-identity#seamless-sso)|
|SSO with Primary Refresh Token (PRT)|Yes (1709+)|Yes|Yes|Yes (coming with version 90)|[SSO with PRT](https://docs.microsoft.com/deployedge/microsoft-edge-security-identity#sso-with-primary-refresh-token-prt)|
|Windows Integrated Authentication (WIA)|Yes|Yes|Yes|Yes* (Policy Required)|[WIA](https://docs.microsoft.com/deployedge/microsoft-edge-security-identity#windows-integrated-authentication-wia)|

|Additional features|Win 10|Win 8.1|Win 7|macOS|URL|
|--------|-------|--------|-----|-------|---|
|Collections|Yes|Yes|Yes|Yes|[Collections](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/) |
|Enterprise New Tab Page|Yes|Yes|Yes|Yes|[New Tab Page](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/) |
|IE mode|Yes|Yes|Yes|No|[IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode#prerequisites)|
|Kiosk Mode|Yes|No|No|No|[Kiosk Mode](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode)|
|Microsoft Search in Bing|Yes|Yes|Yes|Yes|[Intelligent Search in Bing](https://www.microsoft.com/edge/business/intelligent-search-with-bing) |
|PDF Reader|Yes|Yes|Yes|Yes|[PDF Reader](https://docs.microsoft.com/deployedge/microsoft-edge-pdf) |
|Shopping|Yes|Yes|Yes|Yes|[Shopping](https://techcommunity.microsoft.com/t5/articles/introducing-shopping-with-microsoft-edge/m-p/1870080) |
|Sleeping Tabs|Yes|Yes|Yes|Yes|[Feature overview](https://docs.microsoft.com/deployedge/microsoft-edge-relnote-stable-channel)<br>[Latest Blog Post](https://blogs.windows.com/msedgedev/2021/03/04/edge-89-performance/)<br>[Group Policies](https://docs.microsoft.com/deployedge/microsoft-edge-policies#sleeping-tabs-settings)|
|Startup Boost|Yes|Yes|Yes|No|[Startup Boost](https://techcommunity.microsoft.com/t5/articles/startup-boost-faq/td-p/1810423)|
|Sync|Yes|Yes|Yes|Yes| [Enterprise Sync](https://docs.microsoft.com/deployedge/microsoft-edge-enterprise-sync) |
|Version Rollback|Yes|Yes|Yes|No|[Version rollback](https://docs.microsoft.com/deployedge/edge-learnmore-rollback) |
|Vertical Tabs|Yes|Yes|Yes|Yes|[Vertical tabs](https://techcommunity.microsoft.com/t5/articles/vertical-tabs-preview-now-available-in-the-canary-and-dev/m-p/1823751) |

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)