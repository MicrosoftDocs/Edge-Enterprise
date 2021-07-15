---
title: "Microsoft Edge enterprise privacy settings"
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Configure Microsoft Edge enterprise privacy settings"
---

# Configure Microsoft Edge policies to support enterprise privacy

Microsoft is committed to providing enterprises with the information and controls needed to make choices about data collection in Microsoft Edge.

## Overview

When Microsoft Edge is deployed on Windows 10, the default is to send diagnostic data based on the users' [Windows Diagnostic data setting](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

When Microsoft Edge is deployed on non-Windows platforms, diagnostic data is collected according to the settings of the following group policies:

- (DEPRECATED) [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - Enable usage and crash-related data reporting. This policy will be obsolete in Microsoft Edge version 89.
- (DEPRECATED) [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - Send site information to improve Microsoft services. This policy will be obsolete in Microsoft Edge version 89.

The preceding deprecated policies are replaced by [Allow Telemetry](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) on Windows 10, and [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) policy for all other platforms.  

## Configure policy settings

Before you begin, download and use the latest Microsoft Edge Policy Template (For more information, see [Configure Microsoft Edge](configure-microsoft-edge.md).)

### Send required and optional diagnostic data about browser usage

If the [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) policy is configured, it takes precedence over [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) and [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices).

#### Required and optional diagnostic data

Required diagnostic data is collected to keep Microsoft Edge secure, up to date and performing as expected.

Optional diagnostic data includes data about how you use the browser, websites you visit and crash reports to help keep Microsoft Edge secure, up to date, and performing as expected and is used to improve Microsoft Edge and other Microsoft products and services for all users.

> [!NOTE]
> This policy isn't supported on Windows 10 devices. To control data collection on Windows 10, IT admins must use the Windows diagnostic data group policy. This policy will either be to **Allow Telemetry** or to **Allow Diagnostic Data**, depending on the version of Windows. Learn more about [Windows 10 diagnostic data collection](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

Use one of the following settings to configure **DiagnosticData**:

- Off (Not recommended) (0) turns off required and optional diagnostic data collection. 
- Required data (1) sends required diagnostic data but turns off optional diagnostic data collection. Microsoft Edge will send required diagnostic data necessary to keep Microsoft Edge secure, up to date and performing as expected. 
- Optional data (2) sends optional diagnostic data includes data about browser usage, websites that are visited, crash reports sent to Microsoft to help keep Microsoft Edge secure, up to date, and performing as expected and is used to improve Microsoft Edge and other Microsoft products and services for all users.

On Windows 7, Windows 8/8.1, and macOS, this policy controls sending required and optional data to Microsoft.

If you don't configure this policy or disable it Microsoft Edge will default to the user's preference.

### (DEPRECATED) Enable usage and crash-related data reporting

The **MetricsReportingEnabled** policy enables reporting of usage and crash-related data about Microsoft Edge to Microsoft.

Microsoft Edge collects a set of required data that's necessary to keep the product up to date, secure, and performing as expected. This data includes basic device connectivity and configuration information from Microsoft Edge about the current data collection consent, app version, and installation state about your installation of Microsoft Edge. This data collection can be turned off by disabling the policy.

Enable this policy to send reporting of usage and crash-related data to Microsoft. Disable this policy to not send the data to Microsoft. In both cases, users can't change or override the setting.

When Microsoft Edge is running on Windows 10:

- If this policy isn't configured, Microsoft Edge will default to the Windows diagnostic data setting.
- If this policy is enabled, Microsoft Edge will only send usage data if the Windows Diagnostic data setting is set to **Enhanced** or **Full**.
  - If this policy is enabled, Microsoft Edge will only send usage data if [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) is also enabled.
- If this policy is disabled, Microsoft Edge will not send usage data. Crash-related data is sent based on the Windows Diagnostic data setting. [Learn more about Windows Diagnostic data settings](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

When Microsoft Edge is running on Windows 7, 8, and macOS:

- If this policy isn't configured, Microsoft Edge defaults to the user's preference.
-  If this policy is enabled, Microsoft Edge will only send usage data if [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) is also enabled.

### (DEPRECATED) Send site information to improve Microsoft services

The  **SendSiteInformationToImproveServices** policy enables sending information about websites visited in Microsoft Edge to Microsoft to improve Microsoft products and services such as search.

Enable this policy to send information about websites visited in Microsoft Edge to Microsoft. Disable this policy to not send information about the websites that are visited in Microsoft Edge to Microsoft. In both cases, users can't change or override the setting.

When Microsoft Edge is running on Windows 10:

- If this policy isn't configured, Microsoft Edge will default to the Windows diagnostic data setting.
- If this policy is enabled, Microsoft Edge will only send information about the websites that are visited if the Windows Diagnostic data setting is set to **Full**.
  - If this policy is enabled, Microsoft Edge will only send usage data if [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) is also enabled. 
- If this policy is disabled, Microsoft Edge will not send info about websites visited. To [learn more about Windows Diagnostic data settings](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

When Microsoft Edge is running on Windows 7, 8, and macOS:

- If this policy is enabled, Microsoft Edge will only send usage data if [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) is also enabled.
- If this policy isn't configured, Microsoft Edge defaults to the user's preference.

## Implementation details

For non-Windows 10 devices: 
- If [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) policy is configured, it takes precedence over [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) and [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices). 
- If [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) policy isn't configured, Microsoft Edge listens to [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) and [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices).  

For Windows 10 to understand our implementation with the dependency on the Windows Diagnostic data setting, the following table identifies whether **Required** and **Optional** diagnostic data is sent to Microsoft.

| Windows Diagnostic data setting | Required diagnostic data  | Optional diagnostic data |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| Security                        | Not sent                                      | Not sent                                            |
| Basic                           | Sent                                      | Not sent                                            |
| Enhanced                        | Sent                                          | Not sent                                            |
| Full                            | Sent                                          | Sent                                                |

> [!IMPORTANT]
> Microsoft Edge will support **MetricsReportingEnabled** and **SendSiteInfoToImproveServices** for Microsoft Edge versions 86 – 88 inclusive. In Microsoft Edge version 89, **MetricsReportingEnabled** and **SendSiteInfoToImproveServices** will no longer be supported and will default to **DiagnosticData** on non-Windows 10 platforms or the **Allow Telemetry** policy for Windows 10.

## Additional privacy policy options

You may want to consider the following group policies related to data privacy:

- Block cookies on specific sites
- Block third-party cookies
- Configure Do Not Track
- Disable InPrivate mode

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge policies](microsoft-edge-policies.md)
- [Microsoft Edge Privacy Whitepaper](/microsoft-edge/privacy-whitepaper)