---
title: "Detailed guide to the ExtensionSettings policy"
ms.author: aspoddar
author: dan-wesley
manager: balajek
ms.date: 03/25/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "A detailed reference guide for configuring Microsoft Edge extensions using the ExtensionSettings policy."
---

# Detailed guide to the ExtensionSettings policy

Windows offers multiple ways to manage extensions. A common way is to set multiple policies in one place with a JSON string or in the Windows Registry using the [ExtensionSettings](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensionsettings) policy.

> [!NOTE]
> This article applies to Microsoft Edge version 77 or later.

## Before you begin

The extensions policy options assume that you already have Microsoft Edge managed for your users. For more information,  see the [Configure Microsoft Edge policy settings on Windows](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge).

The configuration steps in this article are for Windows, for the corresponding implementation in MAC/Linux, see the [Microsoft Edge browser policy](https://docs.microsoft.com/deployedge/microsoft-edge-policies) reference.

## Policy fields

This policy can control settings such as Update URL, where the extension will be downloaded from for initial install, and Blocked permissions, or which permissions aren't allowed to run.

## See also

- [Manage Microsoft Edge extensions in the enterprise](microsoft-edge-manage-extensions.md)
- [Use group policies to manage Microsoft Edge extensions](microsoft-edge-manage-extensions-policies.md)
- [FAQ for Microsoft Edge Extensions](microsoft-edge-manage-extensions-faq.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
