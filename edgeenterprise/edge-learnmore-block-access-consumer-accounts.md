---
title: "Block access to consumer accounts"
ms.author: archandr
author: dan-wesley
manager: collw
ms.date: 03/30/2023
audience: ITPro
ms.topic: conceptual
ms.custom: generated
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Block access to consumer accounts"
---

# Block access to consumer accounts

The [AllowedDomainsForApps](/deployedge/microsoft-edge-policies#alloweddomainsforapps) policy prevents users from signing into Google services using any accounts other than the accounts you provided them with. Reasons for blocking access are to prevent users on your corporate network using their personal Gmail accounts, or accessing a managed Google account from another domain.

Users might see the following message when you block access to consumer accounts:
"This account is not allowed to sign in within this network".

> [!NOTE]
> This article applies to Microsoft Edge Stable version 104 or later.

## What does this policy do?

This policy causes the **X-GoogApps-Allowed-Domains:** header to be appended to all HTTP and HTTPS requests to all google.com domains. This header is followed by a comma-separated list with the allowed domain names.

Example: `X-GoogApps-Allowed-Domains: mydomain1.com, mydomain2.com`

> [!NOTE]
> Microsoft Edge, which is built on Chromium, is inheriting this upstream policy from the Chromium open source project.

## Configure policy settings

To learn how to configure Microsoft Edge policy settings in Intune, see [Configure Microsoft Edge policy settings with Microsoft Intune](configure-edge-with-intune.md).

## Content license

> [!NOTE]
> Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/). The original page can be found [here](https://support.google.com/a/answer/1668854).

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
