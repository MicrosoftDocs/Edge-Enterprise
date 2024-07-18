---
title: "Enterprise Site Discovery Step by Step Guide"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 07/18/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Guide to using Enterprise Site Discovery to prepare for IE mode."
---

# Enterprise Site Discovery Step-by-Step Guide

This article provides a step-by-step guide to using Enterprise Site Discovery with Microsoft Endpoint Configuration Manager.

> [!TIP]
> Unless your environment requires using the steps in this guide, we recommend that you use  the [Microsoft Edge deployment wizard](https://aka.ms/edgeadvisor) and the script it generates to configure Enterprise Site Discovery.

Enterprise Site Discovery can help you configure your Enterprise Mode Site List. Enterprise Site Discovery will help you:

- Discover which sites are using legacy document modes. Unless these sites are detecting modern browsers and providing different HTML, they probably need to use IE mode.
- Discover which sites are using ActiveX controls. Microsoft Edge doesn't support ActiveX controls. Unless these sites are detecting modern browsers and providing different HTML, they probably need to use IE mode.

> [!NOTE]
> This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels.

## Prerequisites

This guide assumes you're experienced with using Microsoft Endpoint Configuration Manager and have the following services and roles installed:

- Microsoft Endpoint Configuration Manager
- Microsoft SQL Server Reporting Services
- (Optional) Configuration Manager Reporting Services Point Role is configured

## Download Enterprise Site Discovery Tools

Download the following tools:

- [Enterprise Site Discovery Setup and Configuration Package](https://go.microsoft.com/fwlink/p/?LinkId=517719)
- [Microsoft Report Builder](https://www.microsoft.com/download/details.aspx?id=53613)

## Enable Enterprise Site Discovery

Before you can connect to Windows Management Instrumentation (WMI) to retrieve site discovery data, you need to deploy the WMI class provider to the device that's collecting this data.

From the **Enterprise Site Discovery Setup and Configuration Package**, extract the contents to a folder in your definitive software library file share. Example: **\\\\DSL\\EnterpriseSiteDiscovery**.

Next, create a package in Microsoft Endpoint Configuration Manager, as described in [Packages and programs in Configuration Manager](/configmgr/apps/deploy-use/packages-and-programs).

Configure the new package with the following settings:

- On the **Package** page:
  - select **Name** and specify the name **Enable Site Discovery**
  - select **This package contains source files**
  - specify the source folder you extracted the files to (for example, **\\\\DSL\\EnterpriseSiteDiscovery**)
- On the **Program Type** page, choose **Standard Program**
- On the **Standard Program** page, enter the following command to configure Site Discovery on the device:

  ```dos
  
    powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1

  ```

  > [!NOTE]
  > The script supports using command line switches for `-ZoneAllowList` and `-SiteAllowList`. For this step-by-step, we will configure these options via [group policy](#configure-enterprise-site-discovery-via-group-policy).

- On the **Standard Program** page:
  - select the option to run **Hidden**
  - under **Program can run**, select the option **Whether or not a user is logged in**

After creating the package, double-click on the package name **Enable Site Discovery** to view its properties. For the **After running** property, select **Configuration manager restarts computer**. WMI data collection will start after the devices reboot.

> [!NOTE]
> You can configure the amount of time a user has to restart the device as described in the [client settings documentation](/configmgr/core/clients/deploy/about-client-settings#computer-restart).

To confirm that data collection's working, visit a couple of websites and run the following PowerShell command to verify that data's being populated in the WMI namespace.

```powershell

Get-WmiObject -Namespace "root/cimv2/IETelemetry" -Class IEURLInfo | Select-Object URL, NumberOfVisits, CrashCount, DocMode | Sort-Object

```

## Configure Enterprise Site Discovery via Group Policy

With Enterprise Site Discovery enabled, you can configure what data you'll collect. Consider local laws and regulatory requirements as described in [What data is collected?](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery#what-data-is-collected).

1. Open the Group Policy Editor.
2. Select **Computer Configuration** > **Administrative Templates** > **Windows Components** > **Internet Explorer**.
3. Double-click **Turn on Site Discovery WMI output**.
4. Select **Enabled**.
5. Select **OK** or **Apply** to save this policy setting.

You can pick the zones where you want to collect site data:

1. Double-click **Limit Site Discovery output by Zone**.
2. Select **Enabled**.
3. Set the **Zone Mask**  to indicate which of the following zones to enable site discovery for.

    - Restricted Sites Zone
    - Internet Zone
    - Trusted Sites Zone
    - Local Intranet Zone
    - Local Machine Zone
   > [!NOTE]
   > To configure zone(s) included in site discovery, a binary number is formed based on the selected zones. The decimal representation of this number is used to represent this number in policy.

    Examples:
    Zone Mask 2: **00010** will collect data for the Local Intranet zone only
    Zone Mask 6: **00110** will collect data for Intranet and Trusted site zones only

4. Select **OK** or **Apply** to save this policy setting.

You can also limit the domains for which to collect site data:

1. Double-click **Limit Site Discovery output by domain**.
2. Select **Enabled**.
3. Enter the domains you want to collect data for, one domain per line.
4. Select **OK** or **Apply** to save this policy setting.

## Collect Site Discovery data using Configuration Manager

Now that your devices are generating data, it's time to collect this data in Configuration Manager.

1. In the Configuration Manager console, choose **Administration** > **Client Settings** > **Default Client Settings**.
2. On the **Home** tab's **Properties** group, choose **Properties**.
3. In the **Default Client Settings** dialog box, choose **Hardware Inventory**.
4. In the **Device Settings** list, choose **Set Classes**.
5. In the **Hardware Inventory Classes** dialog box, choose **Add**.
6. In the **Add Hardware Inventory Class** dialog box, select **Connect**.
7. In the **Connect to Windows Management Instrumentation (WMI)** dialog box, enter the name of a computer where Enterprise Site Discovery is configured. If you're connecting to another computer, you'll need credentials with permission to access WMI.
8. In the **WMI Namespace** text box, enter **root\cimv2\IETelemetry**.
9. Choose **Connect**.
10. In the **Add Hardware Inventory Class** dialog box, in the **Inventory classes** list, select the WMI classes **IESystemINfo**, **IEUrlInfo**, and **IECountInfo**.
11. Select **OK** to close the **Class qualifiers** dialog and the other open dialogs.

After the client updates settings from the management point, data will be reported when the next hardware inventory runs (by default every seven days).

## Import Site Discovery reports

The Enterprise Site Discovery package includes two sample reports. One report shows sites using ActiveX controls, and the report shows sites using legacy document modes.

### Configure the Site Discovery sample report

Use the steps as a guide to create a sample report that uses three data sources. These data sources are: the sites a user visits, information about their system, and the document modes used by the sites. This report helps you identify sites that may depend on legacy document modes.

1. Copy the report **SCCM_Report-Site_Discovery.rdl** to your Configuration Manager server.
2. Install [Microsoft Report Builder](/sql/reporting-services/install-windows/install-report-builder).
3. Double-click **SCCM_Report-Site_Discovery.rdl** to open the report in Report Builder.
4. The first time you try to open the report, it will try to contact the server where it was created. When prompted to **Connect to Report Server**, select **No**.
5. After the report opens, expand **Data Sources** and double-click **DataSource1**.
6. In the **Data Source Properties** window, select **Use a connection embedded in my report** and then select **Build...**.

> [!NOTE]
> Ensure that you select Microsoft SQL Server as the Data Source. Report Builder defaults to Microsoft SQL Server Analysis Services as the data source.

7. In the **Connection Properties** window, select **Server Name** and enter the name of the Configuration Manager server. Then, in **Select or enter a database name** select the name of the Configuration Manager database from the dropdown list.
8. Select **OK** to close the **Connection Properties** window.
9. Select **Test Connection** to test the connection. If the connection's successful, select **OK** to close the **Data Source Properties** window.
10. Repeat Steps 5 through 9 for **Data Source 2**.
11. Expand **Datasets** and double-click **DataSet1**.
12. In the **Dataset Properties** window, click in the **Query:** textbox. Copy the query to Notepad and then find and replace **CM_A1B** with the database name you selected in Step 7. Paste the updated query into the **Query:** textbox.
13. Repeat steps 11 through 12 for **DataSet2**, **DataSet3**, and **DataSet4**.
14. In the **Home** tab of the ribbon, select the **Run** button to test the report.
15. Save the report and close Microsoft Report Builder.
17. Rename the report file to **Site Discovery.rdl**

### Configure the ActiveX sample report

Use the following procedure to create a sample report that uses one data source: the sites that are using ActiveX controls. Because Internet Explorer is the only browser that supports ActiveX controls, these sites may require IE mode in Microsoft Edge.

1. Copy the report **SCCM Report Sample - ActiveX.rdl** to your Configuration Manager server.
2. Install [Microsoft Report Builder](/sql/reporting-services/install-windows/install-report-builder).
3. Double-click **SCCM Report Sample - ActiveX.rdl** to open the report in Report Builder.
4. The first time you try to open the report, it will try to contact the server where it was created. When prompted to **Connect to Report Server**, select **No**.
5. After the report opens, expand **Data Sources** and double-click **AutoGen__5C6358F2_4BB6_4a1b_A16E_8D96795D8602_**.
6. In the **Data Source Properties** window, select **Use a connection embedded in my report** and then select **Build...**.
7. In the **Connection Properties** window, select **Server Name** and enter the name of the Configuration Manager server. Then, in **Select or enter a database name** select the name of the Configuration Manager database from the dropdown list.
8. Select **OK** to close the **Connection Properties** window.
9. Select **Test Connection** to test the connection. If the connection is successful, select **OK** to close the **Data Source Properties** window.
10. Expand **Datasets** and double-click **DataSet1**.
11. In the **Dataset Properties** window, click in the **Query:** textbox. Copy the query to Notepad and then find and replace **CM_A1B** with the database name you selected in Step 7. Paste the updated query into the **Query:** textbox.
12. In the **Home** tab of the ribbon, select the **Run** button to test the report.
13. Save the report.
14. Close Microsoft Report Builder.
15. Rename the file to **ActiveX**

### Upload configured reports to Microsoft SQL Server Reporting Services

After you've configured the reports for your environment, upload them to the reporting server.

1. Launch the **Reporting Services Configuration Manager** application.
2. In the **Report Server Connection** window, select **Connect** and then select the URL listed under **Web Portal Site Identification**
3. In the browser window that opens, you should be on the **SQL Server Reporting Services Page** - select the **ConfigMgr_SCCMSiteCode** folder for your SCCM Site Code.
4. In the ribbon, hover over **+New** and select the **Folder** menu item.
5. Enter a folder name, such as **Enterprise Site Discovery**, and then select the **Create** button.
6. Select the **Enterprise Site Discovery** folder.
7. On the ribbon, select the **Upload** button.
8. Select the **Site Discovery** report, and select **OK**.
9. Repeat steps 7 and 8 for the **ActiveX** report.

### View reports in Configuration Manager

Now that you've customized and uploaded the reports, you can view them in Configuration Manager.

1. In the Configuration Manager console, choose **Monitoring** > **Reporting** > **Reports** > **Enterprise Site Discovery**
2. Double-click on a report to view it.

## Disable Enterprise Site Discovery

When you're finished collecting data, disable Enterprise Site Discovery. Create a second package to disable Enterprise Site Discovery in Microsoft Endpoint Configuration Manager, as described in the [Packages and programs in Configuration Manager](/configmgr/apps/deploy-use/packages-and-programs). Configure the following options:

- On the **Package** page:
  - select **Name** and specify the name **Disable Site Discovery**.
  - select **This package contains source files**.
  - specify the source folder you extracted the files to (for example, **\\\\DSL\\EnterpriseSiteDiscovery**).
- On the **Program Type** page, choose **Standard Program**.
- On the **Standard Program** page, enter the following command line to disable Site Discovery on the device:

  ```dos
  powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1 -IEFeatureOff

  ```

- On the **Standard Program** page:
  - select the run **Hidden** option.
  - under **Program can run**, select the option **Whether or not a user is logged in**.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [About IE mode](./edge-ie-mode.md)
- [Additional Enterprise Mode information](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Additional Enterprise Site Discovery information](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery)
