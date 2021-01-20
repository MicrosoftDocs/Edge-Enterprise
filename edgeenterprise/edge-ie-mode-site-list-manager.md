---
title: "Enterprise Site List Manager in Microsoft Edge "
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 01/20/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Enable and use Enterprise Site List Manager in Microsoft Edge "
---

# Enterprise Site List Manager in Microsoft Edge

This article explains how to enable access to and use the Enterprise Site List Manager in Microsoft Edge to create, edit and export your Enterprise Mode Site List for Internet Explorer mode.

> [!NOTE]
> This article applies to Microsoft Edge version 89 or later.

## Overview

The Enterprise Site List Manager is an in-browser version of the [standalone Enterprise Mode Site List Manager tool](https://www.microsoft.com/download/details.aspx?id=49974) that lets you create, edit, and export your organization’s site list.

Future improvements to the tool for Internet Explorer mode will be available through Enterprise Site List Manager in Microsoft Edge. The standalone tool will continue to be available in the Download Center but won't get any feature updates.

## Enabling access to Enterprise Site List Manager

You can configure access to the tool by using the [EnterpriseModeSiteListManagerAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed) group policy.

If enabled, your users will see an option named Enterprise Site List Manager on the left navigation pane in *edge://compat*. If Disabled, users will not see the entry point to Enterprise Site List Manager in the left navigation pane. This is the default behavior.

## Using the Enterprise Site List Manager

The Enterprise Site List Manager tool uses the v.2 version of the schema. If you import a v.1 version schema into the Enterprise Site List Manager (schema v.2), the XML is saved into the v.2 version of the schema.

### Add single sites to your site list  

Use the following steps to add individual sites to your site list.

> [!NOTE]
> You can only add specific URLs, not Internet or Intranet Zones.

1. In the Enterprise Site List Manager, click **Add a site**.
2. Type the URL for the website you’d like to add, for example: <domain>.com or <domain>.com/<path> in the URL box.
3. Select one of the following options from the **Open in** list:

   - **IE11**. Opens the site in the IE11 application.
   - **IE mode**. Opens the site in Internet Explorer mode on Microsoft Edge if enabled and in the IE11 app otherwise. See [Internet Explorer mode on Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode).
   - **MSEdge**. Opens the site in Microsoft Edge.
   - **Configurable**. Allows the site to participate in IE mode engine determination. See [Configurable sites in IE mode](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
   - **None**. Opens in whatever browser the user chooses.  

4. Under **Compat Mode**, choose one of the following options:

   - **IE8Enterprise**. Loads the site in IE8 Enterprise Mode.
   - **IE7Enterprise**. Loads the site in IE7 Enterprise Mode.
   - **IE[x]**. Where [x] is the document mode number and the site loads in the specified document mode.
   - **Default Mode**. Loads the site using the default compatibility mode for the page.

   The path within a domain can require a different compatibility mode from the domain itself. For example, the domain might look fine in the default IE11 browser, but the path might have problems and require the use of Enterprise Mode. If you added the domain previously, your original compatibility choice is still selected. However, if the domain is new, **IE8 Enterprise Mode** is automatically selected.

   Enterprise Mode takes precedence over document modes, so sites that are already included in the Enterprise Mode site list won’t be affected by this update and will continue to load in Enterprise Mode, as usual. For more specific information about using document modes, see [Fix web compatibility issues using document modes and the Enterprise Mode site list](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/fix-compat-issues-with-doc-modes-and-enterprise-mode-site-list).

5. The **Allow Redirect** checkbox applies to the treatment of server-side redirects. If you check this box, server-side redirects will open in the browser specified by the open-in tag. For more information, see [here](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance#updated-schema-attributes).

6. Type any comments about the website into the **Comment** box. Administrators can only see comments while they’re in this tool and these comments are retained in the site list xml.

7. Click **Add** to add the site to your site list.

### Export site list to XML

After you create your site list in the Enterprise Site List Manager, you can export the contents to an Enterprise Mode (.EMIE) or XML file. 

> [!NOTE]
> This file includes all of your URLs, including your compatibility mode selections and should be stored somewhere safe.

To export the site list, follow these steps:

1. In the Enterprise Site List Manager, click **Export to XML**.
2. Enter a **Version number** and a **File name**.
3. Click **Export**.

You can save the file locally or to a network share. However, you must make sure you deploy it to the location specified in your registry key. For more information, see [Turn on Internet Explorer mode and use a site list](https://docs.microsoft.com/deployedge/edge-ie-mode-policies).

### Import multiple sites to your site list

After you create your .xml file, you can bulk add sites to the editor using **Import from XML**.

If you want to replace all the contents in the editor, click  the ellipsis (…) and then choose **Clear list**. After you clear the editor, use the following steps to import the site.

1. In the Enterprise Site List Manager, click **Import from XML**. 
2. Click **Choose file** to select your site list to add the included sites to the tool. Pick the site list you want to add and then click **Open**. Supported formats for Import are .xml, .emie or .txt containing the v.2 schema for Enterprise Mode Site List. See [Enterprise Mode schema v.2 guidance](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).
3. Click **Load** to add the sites from the file tp the editor.

You can save the file locally or to a network share. However, you must make sure you deploy it to the location specified in your registry key. For more information, see [Turn on Internet Explorer mode and use a site list](https://docs.microsoft.com/deployedge/edge-ie-mode-policies).

### Edit sites in your site list

 You can edit attributes of existing site entries in the Enterprise Site List Manager. You can also add, remove, or delete associated comments.

1. In the Enterprise Site List Manager, click the ellipsis (…) and choose **Edit site** for the URL you want to edit.
2. You can edit any attribute of the site entry except the URL. Click **Save** after you finish editing.

   > [!NOTE]
   > If you want to delete a site entry, choose **Delete site** in step 1.

3. Click **Export to XML**, and save the updated file.

You can save the file locally or to a network share. However, you must make sure you deploy it to the location specified in your registry key. For more information, see [Turn on Internet Explorer mode and use a site list](https://docs.microsoft.com/deployedge/edge-ie-mode-policies).

### Preview your site list in XML format

You can preview the sites in the editor in XML format before you export and save to your site list location. Click **XML preview** to open the file in a new tab.

### Search in the Enterprise Site List Manager

You can search to see if a specific site already appears in your site list so you don’t try to add it again.

To search, type part of the URL into the **Filter sites by URL** search box on the top right-hand corner of the editor.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [About IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Additional Enterprise Mode information](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Additional Enterprise Site Discovery information](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery)
