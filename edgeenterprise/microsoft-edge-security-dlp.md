---
title: "Data Loss Prevention in Microsoft Edge"
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 10/06/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Data Loss Prevention (DLP) in Microsoft Edge"
---

# Data Loss Prevention (DLP) in Microsoft Edge

This article describes Data Loss Prevention (DLP) - what it is, and why it's important.

> [!NOTE]
> This applies to Microsoft Edge version 85 or later.

## Overview

Data loss prevention (DLP) is a system of technologies that identify and safeguard sensitive enterprise data from unauthorized disclosure. To comply with business standards and industry regulations, organizations must protect sensitive information and prevent its unauthorized disclosure. Sensitive information includes financial data or personally identifiable information (PII) such as credit card numbers, social security numbers, or health records, among many other things.

### The impact of remote work

Remote work has increased the emphasis on using DLP. With the growing use of personal and work activities on devices, enterprises are seeing an increased risk of unauthorized sharing of corporate data outside the workplace.

This blending of user activities has spread to devices as well, where data is moved between personal and corporate devices over a variety of public and private networks. The net result is a dramatically increased risk of exposing sensitive data.

Microsoft Edge natively supports two different DLP solutions, Microsoft Endpoint DLP and Windows Information Protection (WIP).

## Microsoft Endpoint DLP

Microsoft Endpoint DLP is the next generation of DLP using modern concepts such as data centric protection. It's  built-in to Windows 10 and Microsoft Edge so it doesn't need additional agents or plugins on the device. To learn more about endpoint DLP, see [Learn about Microsoft 365 Endpoint data loss prevention](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide).

### Microsoft Edge support for Endpoint DLP

Microsoft Edge enforces admin configured policies for sensitive files and records audit events for non-compliant activities.

Some of the user activities that you can audit and manage on devices running Windows 10 include the following:

- File Upload: Protect sensitive file upload to unauthorized cloud locations.
- Clipboard Protection: Protect sensitive data from being copied out of the file.
- Print Protection: Protect sensitive file from being printed.
- Save to USB/Network: Protect sensitive file from being saved to removable USB storage or unauthorized network locations.

> [!NOTE]
> For more detailed information about user activities you can audit and manage, see [Endpoint activities you can monitor and take action on](https://docs.microsoft.com/en-us/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on).

## Windows Information Protection

Check out [Support for Windows Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection), which describes how Microsoft Edge supports Windows Information Protection (WIP). This article includes [System Requirements](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#system-requirements) such as Windows version and SKUs, and management solution required to run WIP in the enterprise. Support for Windows Information also lists the numerous benefits of WIP, among them:

- separation between personal and corporate data
- data protection for existing line-of-business apps
- audit reports for tracking issues
- integration with existing management systems

Additional benefits are described in  [Windows Information Protection Benefits](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#windows-information-protection-benefits).  

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Overview of data loss prevention](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies?view=o365-worldwide)
- [Protect your enterprise data using Windows Information Protection](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)
