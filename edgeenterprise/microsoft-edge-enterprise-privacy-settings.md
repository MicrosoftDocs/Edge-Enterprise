---
title: "Microsoft Edge enterprise privacy settings"
ms.author: likravit
author: dan-wesley
manager: srugh
ms.date: 05/26/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Configure Microsoft Edge enterprise privacy settings"
---

# Configure Microsoft Edge policies to support enterprise privacy

Microsoft is committed to providing enterprises with the information and controls needed to make choices about data collection in Microsoft Edge.

## Overview

By default, Microsoft Edge deployed on non-Windows platforms doesn't send diagnostic data or site information to Microsoft. When Microsoft Edge is deployed on Windows 10, the default is to send diagnostic data based on the users' [Windows Diagnostic data setting](https://go.microsoft.com/fwlink/?linkid=2099569).

You can also configure how Microsoft Edge handles data collection for your organization with the following group policies:

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - Enable usage and crash-related data reporting.
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - Send site information to improve Microsoft services.

## Configure policy settings

Before you begin, download and use the latest Microsoft Edge Policy Template (For more information, see [Configure Microsoft Edge](configure-microsoft-edge.md).)

### Enable usage and crash-related data reporting

This policy enables reporting of usage and crash-related data about Microsoft Edge to Microsoft.

Microsoft Edge collects a set of required data that's necessary to keep the product up to date, secure, and performing properly. This data includes basic device connectivity and configuration information from Microsoft Edge about the current data collection consent, app version, and installation state about your installation of Microsoft Edge. This data collection can be turned off by disabling the policy.

Enable this policy to send reporting of usage and crash-related data to Microsoft. Disable this policy to not send the data to Microsoft. In both cases, users can't change or override the setting.

When Microsoft Edge is running on Windows 10:

- If this policy isn't configured, Microsoft Edge will default to the Windows diagnostic data setting.
- If this policy is enabled, Microsoft Edge will only send usage data if the Windows Diagnostic data setting is set to **Enhanced** or **Full**.
- If this policy is disabled, Microsoft Edge will not send usage data. Crash-related data is sent based on the Windows Diagnostic data setting. [Learn more about Windows Diagnostic data settings](https://go.microsoft.com/fwlink/?linkid=2099569).

When Microsoft Edge is running on Windows 7, 8, and macOS:

- If this policy isn't configured, Microsoft Edge will default to the user's preference.

### Send site information to improve Microsoft services

This policy enables sending information about websites visited in Microsoft Edge to Microsoft to improve Microsoft products and services such as search.

Enable this policy to send information about websites visited in Microsoft Edge to Microsoft. Disable this policy to not send information about the websites that are visited in Microsoft Edge to Microsoft. In both cases, users can't change or override the setting.

When Microsoft Edge is running on Windows 10:

- If this policy isn't configured, Microsoft Edge will default to the Windows diagnostic data setting.
- If this policy is enabled, Microsoft Edge will only send information about the websites that are visited if the Windows Diagnostic data setting is set to **Full**.
- If this policy is disabled, Microsoft Edge will not send info about websites visited. To [learn more about Windows Diagnostic data settings](https://go.microsoft.com/fwlink/?linkid=2099569).

When Microsoft Edge is running on Windows 7, 8, and macOS:

- If this policy isn't configured, Microsoft Edge will default to the user's preference.

## Implementation details

For Windows 10 to understand our implementation with the dependency on the Windows Diagnostic data setting, the following table describes our configuration if **Enable usage and crash-related data reporting** and **Send site information to improve Microsoft services** were not configured.

| Windows Diagnostic data setting | Enable usage and crash-related data reporting | Send site information to improve Microsoft services |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| Security                        | Not sent                                      | Not sent                                            |
| Basic                           | Not sent                                      | Not sent                                            |
| Enhanced                        | Sent                                          | Not sent                                            |
| Full                            | Sent                                          | Sent                                                |

If your configurations for Windows 10 are misconfigured in accordance with the preceding table, we will fall back to the lesser data collection setting.

For example:

- You set the "Enable usage and crash-related data reporting" policy to **Enabled** but the Windows Diagnostic data setting is set to **Basic**. We won't send usage and crash-related data.
- You set the "Send site information to improve Microsoft services" policy to **Disabled** but the Windows Diagnostic data setting is set to **Full**. We won't send information about the sites that are visited.

The correct implementation for the previous settings is to set the "Enable usage and crash-related data reporting" policy to **Enabled** and set the Windows Diagnostic data setting to **Enhanced** or **Full**.

## Additional privacy policy options

You may want to consider the following group policies related to data privacy:

- Block cookies on specific sites
- Block third-party cookies
- Configure Do Not Track
- Disable InPrivate mode

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge policies](microsoft-edge-policies.md)
- [Microsoft Edge Privacy Whitepaper](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper)
