---
title: "Enterprise Site Discovery Step by Step Guide"
ms.author: cjacks
author: appcompatguy
manager: saudm
ms.date: 04/07/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Use Enterprise Site Discovery to Prepare for IE mode"
---

# Enterprise Site Discovery Step-by-Step Guide

This article provides a step-by-step guide to using Enterprise Site Discovery with Microsoft Endpoint Configuration Manager.

Enterprise Site Discovery can help you configure your Enterprise Mode Site List. Enterprise Site Discovery will help you:

- Discover which sites are using legacy document modes. Unless these sites are detecting modern browsers and providing different HTML, they probably need to use IE mode.
- Discover which sites are using ActiveX controls. Microsoft Edge doesn't support ActiveX controls. Unless these sites are detecting modern browsers and providing different HTML, they probably need to use IE mode.

> [!NOTE]
> This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels, version 77 or later.

## Prerequisites

This guide assumes you're experienced with using Microsoft Endpoint Configuration Manager and have the following services and roles installed:

1. Microsoft Endpoint Configuration Manager
2. Microsoft SQL Server Reporting Services
3. (Optional) Configuration Manager Reporting Services Point Role configured

## Download Enterprise Site Discovery Tools

Download the following tools:

- [Enterprise Site Discovery Setup and Configuration Package](https://go.microsoft.com/fwlink/p/?LinkId=517719)
- [Microsoft Report Builder](https://www.microsoft.com/download/details.aspx?id=53613)

## Enable Enterprise Site Discovery

Before you can connect to Windows Management Instrumentation (WMI) to retrieve site discovery data, you must first deploy the WMI class provider to the device.

From the **Enterprise Site Discovery Setup and Configuration Package**, extract the contents to a folder in your definitive software library file share. Example: **\\\\DSL\\EnterpriseSiteDiscovery**.

Next, create a package in Microsoft Endpoint Configuration Manager, as described in the [documentation](https://docs.microsoft.com/configmgr/apps/deploy-use/packages-and-programs), selecting the following options:

- On the **Package** page, select **Name** and specify the name **Enable Site Discovery**
- On the **Package** page, select **This package contains source files**
- On the **Package** page, specify the source folder you extracted the files to (for example, **\\\\DSL\\EnterpriseSiteDiscovery**)
- On the **Program Type** page, choose **Standard Program**
- On the **Standard Program** page, enter the command line to configure Site Discovery on the device as follows:
  ```dos
  powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1
  ```
  > [!NOTE]
  > The script supports using command line switches for `-ZoneAllowList` and `-SiteAllowList`. For this step-by-step, we will configure these options via group policy (below).
- On the **Standard Program** page, select the option to run **Hidden**.
- On the **Standard Program** page, under **Program can run**, select the option **Whether or not a user is logged in**

After creating the package, double-click on the package name **Enable Site Discovery** to view its properties. In the **After running** property, select **Configuration manager restarts computer**. WMI data collection will begin after the devices reboot.

> [!NOTE]
> You can configure the amount of time a user has to restart the device as described in the [client settings documentation](https://docs.microsoft.com/configmgr/core/clients/deploy/about-client-settings#computer-restart).

## Configure Enterprise Site Discovery via Group Policy

With Enterprise Site Discovery enabled, you can configure what data you'll collect. Consider local laws and regulatory requirements as described [here](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery#what-data-is-collected).

1. Open Group Policy Editor
2. Click **Computer Configuration** > **Administrative Templates** > **Windows Components** > **Internet Explorer** 
3. Double-click **Turn on Site Discovery WMI output**
4. Select **Enabled**
5. Click **OK** or **Apply** to save this policy setting

You can limit the zones in which you collect site data:

1. Double-click **Limit Site Discovery output by Zone**
2. Select **Enabled**
3. Enter a bitmask indicating which zones to enable site discover for:
    1. Restricted Sites zone
    2. Internet zone
    3. Trusted Sites zone
    4. Local Intranet zone
    5. Local Machine zone
    
    Example 1: **00010** will collect data only for the Local Intranet zone

    Example 2: **10111** will collect data for all zones except the Internet zone
4. Click **OK** or **Apply** to save this policy setting

You can limit the domains for which you collect site data:

1. Double-click **Limit Site Discovery output by domain**
2. Select **Enabled**
3. Enter the domains you want to collect data for, one domain per line
4. Click **OK** or **Apply** to save this policy setting

## Collect Site Discovery data using Configuration Manager

Now that your devices are generating data, it's time to collect this data in Configuration Manager.

1. In the Configuration Manager console, choose **Administration** > **Client Settings** > **Default Client Settings**
2. On the **Home** tab, in the **Properties** group, choose **Properties**
3. In the **Default Client Settings** dialog box, choose **Hardware Inventory**
4. In the **Device Settings** list, choose **Set Classes**
5. In the **Hardware Inventory Classes** dialog box, choose **Add**
6. In the **Add Hardware Inventory Class** dialog box, click **Connect**
7. In the **Connect to Windows Management Instrumentation (WMI)** dialog box, enter the name of a computer where Enterprise Site Discovery is configured. If you're connecting to another computer, you'll need credentials with permission to access WMI.
8. In the **WMI Namespace** text box, enter **root\cimv2\IETelemetry**
9. Choose **Connect**
10. In the **Add Hardware Inventory Class** dialog box, in the **Inventory classes** list, select the WMI classes **IESystemINfo**, **IEUrlInfo**, and **IECountInfo*.
11. Click **OK** to close the **Class qualifiers** dialog box and the other open dialogs.

After the client updates settings from the management point, data will be reported when the next hardware inventory runs (by default every seven days).

## Import Site Discovery reports

The Enterprise Site Discovery package includes two sample reports. One report shows sites using ActiveX controls, and another shows sites using legacy document modes.

### Configure the Site Discovery sample report

Use the following procedure to create a sample report that uses three data sources: the sites a user visits, information about their system, and the document modes used by the sites. This report helps you identify sites that may depend on legacy document modes.

1. Copy the report **SCCM_Report-Site_Discovery.rdl** to your Configuration Manager server.
2. Install [Microsoft Report Builder](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder?view=sql-server-ver15).
3. Double-click **SCCM_Report-Site_Discovery.rdl** to open the report in Report Builder.
4. The first time you try to open the report, it will try to contact the server where it was created. When prompted to **Connect to Report Server**, click **No**.
5. After the report opens, expand **Data Sources** and double-click **DataSource1**.
6. In the **Data Source Properties** window, select **Use a connection embedded in my report** and then click the **Build...** button.
7. In the **Connection Properties** window, select **Server Name** and enter the name of the Configuration Manager server. Then, in **Select or enter a database name** select the name of the Configuration Manager database from the dropdown list.
8. Click **OK** to close the **Connection Properties** window.
9. Click **Test Connection** to test the connection. If the connection is successful, click **OK** to close the **Data Source Properties** window.
10. Repeat Steps 5 through 9 for **Data Source 2**.
11. Expand **Datasets** and double-click **DataSet1**.
12. In the **Dataset Properties** window, click in the **Query:** textbox and replace **USE CM_A1B** with the database name you selected in Step 7.
13. Repeat steps 11 through 12 for **DataSet2**, **DataSet3**, and **DataSet4**.
14. In the **Home** tab of the ribbon, click the **Run** button to test the report.
15. Save the report.
16. Close Microsoft Report Builder.
17. Rename the file to **Site Discovery.rdl**

### Configure the ActiveX sample report

Use the following procedure to create a sample report that uses one data source: the sites that are using ActiveX controls. Since Internet Explorer is the only browser that support ActiveX controls, these sites may require IE mode.

1. Copy the report **SCCM Report Sample - ActiveX.rdl** to your Configuration Manager server.
2. Install [Microsoft Report Builder](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder?view=sql-server-ver15).
3. Double-click **SCCM Report Sample - ActiveX.rdl** to open the report in Report Builder.
4. The first time you try to open the report, it will try to contact the server where it was created. When prompted to **Connect to Report Server**, click **No**.
5. After the report opens, expand **Data Sources** and double-click **AutoGen__5C6358F2_4BB6_4a1b_A16E_8D96795D8602_**.
6. In the **Data Source Properties** window, select **Use a connection embedded in my report** and then click the **Build...** button.
7. In the **Connection Properties** window, select **Server Name** and enter the name of the Configuration Manager server. Then, in **Select or enter a database name** select the name of the Configuration Manager database from the dropdown list.
8. Click **OK** to close the **Connection Properties** window.
9. Click **Test Connection** to test the connection. If the connection is successful, click **OK** to close the **Data Source Properties** window.
10. Expand **Datasets** and double-click **DataSet1**.
11. In the **Dataset Properties** window, click in the **Query:** textbox and replace **USE CM_A1B** with the database name you selected in Step 7.
12. In the **Home** tab of the ribbon, click the **Run** button to test the report.
13. Save the report.
14. Close Microsoft Report Builder.
15. Rename the file to **ActiveX**

### Upload configured reports to Microsoft SQL Server Reporting Services

After you've configured the reports for your environment, upload them to the reporting server.

1. Launch the **Reporting Services Configuration Manager** application.
2. In the **Report Server Connection** window, click **Connect** and then click on the URL listed under **Web Portal Site Identification**
3. In the browser window that opens, you should be on the **SQL Server Reporting Services Page** - click the **ConfigMgr_SCCMSiteCode** folder for your SCCM Site Code.
4. In the ribbon, hover over **+New** and click the **Folder** menu item.
5. Enter a folder name, such as **Enterprise Site Discovery**, and then click the **Create** button.
6. Click on the **Enterprise Site Discovery** folder.
7. In the ribbon, click the **Upload** button.
8. Select the **Site Discovery** report, and click **OK**.
9. Repeat steps 7 and 8 for the **ActiveX** report.

### View reports in Configuration Manager

Now that you've customized and uploaded the reports, you can view them in Configuration Manager.

1. In the Configuration Manager console, choose **Monitoring** > **Reporting** > **Reports** > **Enterprise Site Discovery**
2. Double-click on a report to view it.

## Disable Enterprise Site Discovery

When you're finished collecting data, you should disable Enterprise Site Discovery. Create a second package to disable Enterprise Site Discovery in Microsoft Endpoint Configuration Manager, as described in the [documentation](https://docs.microsoft.com/configmgr/apps/deploy-use/packages-and-programs), selecting the following options:

- On the **Package** page, select **Name** and specify the name **Disable Site Discovery**
- On the **Package** page, select **This package contains source files**
- On the **Package** page, specify the source folder you extracted the files to (for example, **\\\\DSL\\EnterpriseSiteDiscovery**)
- On the **Program Type** page, choose **Standard Program**
- On the **Standard Program** page, enter the command line that will disable Site Discovery on the device as follows:
  ```dos
  powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1 -IEFeatureOff
  ```
- On the **Standard Program** page, select the option to run **Hidden**
- On the **Standard Program** page, under **Program can run**, select the option **Whether or not a user is logged in**

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [About IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Additional Enterprise Mode information](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Additional Enterprise Site Discovery information](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery)