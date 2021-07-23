---
title: "Configure IE mode Policies"
ms.author: collw
author: AndreaLBarr
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Configure IE mode policies"
---

# Configure IE mode policies

>[!Note]
> The Internet Explorer 11 desktop application will be retired and go out of support on June 15, 2022 (for a list of what’s in scope, [see the FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)). The same IE11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode. [Learn more here](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

This article explains how to configure IE mode policies.

> [!NOTE]
> This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels, version 77 or later.

Configuring IE mode requires three steps:

1. [Configure Internet Explorer integration](#configure-internet-explorer-integration)
2. [Redirect sites from Microsoft Edge to IE mode](#redirect-sites-from-microsoft-edge-to-ie-mode)
3. (Optional) [Redirect sites from IE to Microsoft Edge](#redirect-sites-from-ie-to-microsoft-edge)

    1. If you are ready to disable the IE11 app, follow the steps in [Disable Internet Explorer 11](/deployedge/edge-ie-disable-ie11)
    2. Otherwise,  follow the rest of the steps in [Redirect sites from IE to Microsoft Edge](/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge)

> [!NOTE]
> Policies to enable IE mode can be configured through Intune. For more information, see [Add Microsoft Edge to Microsoft Intune](/intune/apps/apps-windows-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) and [Configure Microsoft Edge policies with Microsoft Intune](./configure-edge-with-intune.md).

## Configure Internet Explorer integration

You can configure Internet Explorer to open directly within Microsoft Edge (IE mode). You can also configure Internet Explorer to open with a standalone Internet Explorer 11 window. Most users prefer when sites open directly within Microsoft Edge in IE mode.

### Enable Internet Explorer integration using Group Policy

1. Download and use the latest [Microsoft Edge Policy Template](https://www.microsoft.com/en-us/edge/business/download).
2. Open Group Policy Editor.
3. Click **User Configuration/Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.
4. Double-click **Configure Internet Explorer integration**.
5. Select **Enabled**.
6. Under **Options**, set the dropdown value to 
   -  **Internet Explorer mode** if you want sites to open in IE mode on Microsoft Edge
   -  **Internet Explorer 11** if you want sites to open in a standalone Internet Explorer 11 window (This option will not be supported after June 15, 2022 when the Internet Explorer 11 desktop application will be retired and go out of support.  After June 15, 2022 when IE11 will no longer be available, this option will behave the same as the Internet Explorer mode option.)  
   -  **None** if you want to stop users from configuring Internet Explorer mode via edge://flags or through the command line

   > [!NOTE]
   > Setting the policy to **Disabled** implies IE mode is disabled by policy, but can be set through edge://flags or command line options.
7. Click **OK** or **Apply** to save this policy setting.

## Redirect sites from Microsoft Edge to IE mode

There are two options for identifying which sites should open in IE mode:

- (Recommended) [Configure sites on the Enterprise Site list](#configure-sites-on-the-enterprise-site-list)
- [Configure all Intranet sites](#configure-all-intranet-sites)

### Configure sites on the Enterprise Site list

You can use the following group policies to configure specific sites to open in IE mode:

- [Use the Enterprise Mode IE website list](#configure-using-the-use-the-enterprise-mode-ie-website-list-policy) (Internet Explorer)
- [Configure the Enterprise Mode Site List](#configure-using-the-configure-the-enterprise-mode-site-list-policy) (Microsoft Edge, version 78 or later)<br/>This policy lets you create a separate Enterprise Mode Site list for Microsoft Edge. Enabling this policy overrides the settings in the "Use the Enterprise Mode IE website list" policy, if "Configure Internet Explorer integration" is enabled. Disabling or not configuring this policy doesn't affect the default behavior of the "Configure Internet Explorer integration" policy.
    > [!NOTE]
    > It is not mandatory to configure the Microsoft Edge policy. Many organizations use this as an override, allowing them to target the current Site List at all users with the IE policy, and more easily target an updated version to pilot uses with the Microsoft Edge policy.

For more information about Enterprise Mode Site lists, see:

- [Use the Enterprise Mode Site List Manager](/internet-explorer/ie11-deploy-guide/use-the-enterprise-mode-site-list-manager)
- [Add multiple sites to the Enterprise Mode site list using a file and the Enterprise Mode Site List Manager (schema v.2)](/internet-explorer/ie11-deploy-guide/add-multiple-sites-to-enterprise-mode-site-list-using-the-version-2-schema-and-enterprise-mode-tool).

### Configure using the Use the Enterprise Mode IE website list policy

IE mode can use the existing policy configuring the Enterprise Site List for Internet Explorer, allowing you to create and maintain a single list.

1. Create or reuse a Site List XML
    1. All sites that have the element _\<open-in\>IE11\</open-in\>_ will now open in IE mode.
2. Open Group Policy Editor.
3. Click **User Configuration/Computer Configuration** > **Administrative Templates** > **Windows Components** > **Internet Explorer**.
4. Double-click **Use the Enterprise Mode IE website list**.
5. Select **Enabled**.
6. Under **Options**, type the location of website list. You can use one of the following locations:
    - (Recommended) HTTPS location: **https**:**//iemode/sites.xml**
    - Local network file: **\\\network\shares\sites.xml**
    - Local file: **file:///c:/Users/\<user\>/Documents/sites.xml**
7. Click **OK** or **Apply** to save these settings.

### Configure using the Configure the Enterprise Mode Site List policy

You can also configure IE mode with a separate policy for Microsoft Edge. This additional policy allows you to override the IE site list. For example, some organizations will target the production site list to all users. You can then deploy the pilot site list to a small group of users using this policy.

1. Create or reuse a Site List XML
    1. All sites that have the element _\<open-in\>IE11\</open-in\>_ will now open in IE mode.
2. Open Group Policy Editor.
3. Click **User Configuration/Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.
4. Double-click **Configure the Enterprise Mode Site List**.
5. Select **Enabled**.
6. Under **Options**, type the location of website list. You can use one of the following locations:
    - (Recommended) HTTPS location: **https**:**//iemode/sites.xml** <!--Trying to keep this from being an active link in MD -->
    - Local network file: **\\\network\shares\sites.xml**
    - Local file: **file:///c:/Users/\<user\>/Documents/sites.xml**
7. Click **OK** or **Apply** to save these settings.

### Configure all intranet sites

IE mode can be configured as for all sites in the Local Intranet zone. You can remove individual sites from IE mode using an Enterprise Mode Site List.

>[!NOTE]
>
> The Local Intranet zone contains explicitly added sites, but also assigns sites to this zone using heuristics. This can include dotless host names (e.g. **https**:**//payroll**) and sites that the proxy configuration script configures to bypass the proxy. If an external party controls DNS or proxy, they could potentially force websites into IE mode.

1. Open Local Group Policy Editor.
2. Click **User Configuration/Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.
3. Double-click **Send all intranet sites to Internet Explorer**.
4. Select **Enabled**, and then click **OK** or **Apply** to save the policy settings.

## Redirect sites from IE to Microsoft Edge

You can prevent your users from using Internet Explorer for sites that don't need it. Internet Explorer can automatically redirect sites to Microsoft Edge if they aren't on your site list.

1. Open Group Policy Editor.
2. Click **User Configuration/Computer Configuration** > **Administrative Tools** > **Windows Components** > **Internet Explorer**.
3. Double-click **Send all sites not included in the Enterprise Mode Site List to Microsoft Edge.**
4. Select **Enabled**
5. Click **OK** or **Apply** to save these settings.
6. Double-click **Configure which channel of Microsoft Edge to use for opening redirected sites**.
7. Select **Enabled**.
8. Under **Options**, select your top three choices for the channel to use - Internet Explorer will redirect to the highest ranked choice that the user has installed on that device:
   - Microsoft Edge Stable
   - Microsoft Edge Beta version 77 or later
   - Microsoft Edge Dev version 77 or later
   - Microsoft Edge Canary version 77 or later
   - Microsoft Edge version 45 or earlier
9. Click **OK** or **Apply** to save these settings.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [About IE mode](./edge-ie-mode.md)
- [Additional Enterprise Mode information](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
