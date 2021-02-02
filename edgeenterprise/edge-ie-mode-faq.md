---
title: "IE mode FAQ"
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 12/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "FAQ and Troubleshooting for Microsoft Edge with IE mode"
---

# IE mode FAQ

This article provides troubleshooting tips and an FAQ for Microsoft Edge (version 77 or later).

> [!NOTE]
> This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels, version 77 or later.

## Troubleshoot IE mode

Use the information in this section to diagnose and fix IE mode problems.

### Internet Explorer mode diagnostic information

You can get Internet Explorer mode diagnostic information on the Microsoft Edge Compatibility tab. To open this tab, go to *edge://compat/iediagnostic*. This page may show diagnostic messages. This page also provides configuration information for the following categories:

- **Registry key check**. (Displayed only if the check fails.) Checks to see if Internet Explorer integration is set up correctly in the registry. If not, the user can click **Fix it** to resolve the problem.
- **Internet Explorer mode**. Shows the API version that's used, based on the configuration and OS. If there's a problem, the user may be prompted to install a **Windows Update**.
- **Internet Explorer mode setting**. Shows whether Internet Explorer mode is enabled, and how it's configured.
- **Command line**. Shows the command line string and switches used to start Microsoft Edge.
- **Group policy settings**. Shows whether IE mode is configured using group policies, and the policies that are applied.

### Error message: "To open this page in Internet Explorer mode, reinstall Microsoft Edge with administrator privileges."

You may see this error if you don't have all required Windows Updates. See the prerequisites listed in [About IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode) for the required versions of Windows and Microsoft Edge.

If you've already installed all required Windows Updates, you may see this error if:

- You're using the Canary channel, which is installed at the user level by default.
- You're using the Stable, Beta, or Dev channel, but when prompted for elevation when installing the elevation was canceled. When you cancel the elevation prompt, the installation will continue at the user level.
- Internet Explorer 11 has been disabled in Windows Features.

Possible solutions:

- Run the installer for any channel at the system level: `installer.exe --system-level`.
- Enable Internet Explorer 11 in Windows Features.

To check if Microsoft Edge is installed at the systems level, type "edge://version" in the Microsoft Edge address bar. The Executable path will show a path starting with *C:\Program Files*, which indicates a system install. If the Executable path begins with *C:\Users\*, uninstall and then reinstall Microsoft Edge with administrator privileges.

### Error message: "To open this page in IE mode, try restarting Microsoft Edge."

You may see this error if there was an unexpected error in Internet Explorer. Restarting Microsoft Edge usually fixes this error.

### Error message: "Turn off remote debugging to open this site in IE mode otherwise it might not work as expected."

You may see this error if you're remote debugging and navigate to a web page configured to run in IE mode. You can continue, but the page will be rendered using Microsoft Edge.

### Error message: "Error: Could not retrieve EMIE site list."

You may see this error on the *edge://compat/enterprise* page indicating that the site list download failed. Starting Edge 87, when cookies are blocked for third party requests using the [BlockThirdPartyCookies](https://docs.microsoft.com/deployedge/microsoft-edge-policies#blockthirdpartycookies) policy, HTTP authentication is also disallowed. You can allow cookies for the specific domain hosting your Enterprise Mode Site List using the [CookiesAllowedFOrURLs](https://docs.microsoft.com/deployedge/microsoft-edge-policies#cookiesallowedforurls) policy to ensure that site list downloads are successful.

## Frequently Asked Questions

### Will IE mode replace Internet Explorer 11?

We're committed to keeping Internet Explorer a supported, reliable, and safe browser. Internet Explorer is still a component of Windows and follows the support lifecycle of the OS on which it's installed. For details, see [Lifecycle FAQ - Internet Explorer](https://support.microsoft.com/help/17454/). While Microsoft continues to support and update Internet Explorer, the latest features and platform updates will only be available in Microsoft Edge.

### Can I use "Open with Explorer" or "View in File Explorer" in SharePoint with IE mode?

Yes, if this works in standalone Internet Explorer 11 it will work in IE mode. However, rather than use the Open with Explorer option, the recommended approach to managing files and folders outside of SharePoint is to [sync your SharePoint files](https://support.office.com/en-us/article/sync-sharepoint-files-with-the-onedrive-sync-app-6de9ede8-5b6e-4503-80b2-6190f3354a88) or [move or copy files in SharePoint](https://support.office.com/en-us/article/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc).

### Does IE mode on Microsoft Edge support the *nomerge* option that was supported in Internet Explorer 11?

There is no explicit command line in Microsoft Edge to mirror the *nomerge* option, but there are a couple of alternatives that we recommend to provide this functionality.

1. Use Profiles in Microsoft Edge - Each profile maps to a different IE session for IE mode pages, so it behaves identically to the *nomerge* option.
2. Use the `--user-data-dir=<path>` command line, but with a different path for each session. If needed, you can create a utility for the user to run that both launches Microsoft Edge and changes the path for the session.

If neither of the above options works for your scenario, reach out through one of our feedback channels:  Microsoft support, [TechCommunity forum](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise), or [Microsoft Edge UserVoice](https://microsoftedge.uservoice.com/forums/928825-enterprise).

### Can I save links as webpages in Internet Explorer mode?
 
Yes, you can enable the Save Target As option in the context menu for Internet Explorer mode in Microsoft Edge. To do this, configure the group policy *"Allow Save Target As in Internet Explorer mode"* located at *Computer Configuration > Administrative Templates > Windows Components > Internet Explorer*.
The save mechanism works the same as it does in Internet Explorer and if the target is saved as an html file, re-opening the file will render the page in Microsoft Edge.
 
Note that this functionality requires the following minimum operating system updates:
- Windows 10, version 2004, Windows Server version 2004, Windows 10, version 20H2 : [KB4580364](https://support.microsoft.com/help/4580364/windows-10-update-kb4580364)
- Windows 10, version 1903, Windows 10, version 1909, Windows Server version 1903: [KB4580386](https://support.microsoft.com/help/4580386/windows-10-update-kb4580386)
- Windows 10, version 1809, Windows Server version 1809, Windows Server 2019: [KB4580390](https://support.microsoft.com/help/4580390/windows-10-update-kb4580390)
- Windows 10, version 1803: [KB4586785](https://support.microsoft.com/help/4586785/windows-10-update-kb4586785)
- Windows 10, version 1607: [KB4586830](https://support.microsoft.com/help/4586830/windows-10-update-kb4586830)
- Windows 10, version 1507: [KB4586787](https://support.microsoft.com/help/4586787/windows-10-update-kb4586787)


## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [About IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [Additional Enterprise Mode information](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
