---
title: "IE mode troubleshooting and FAQ"
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Troubleshooting and FAQ for Microsoft Edge Internet Explorer mode"
---

# Internet Explorer (IE) mode troubleshooting and FAQ

> [!NOTE]
> The Internet Explorer 11 desktop application will be retired and go out of support on  June 15, 2022. To see the list of what’s in scope, see the [Internet Explorer 11 desktop app retirement FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549). The same IE11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode. To learn more, see the [The future of Internet Explorer on Windows 10 is in Microsoft Edge](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/) blog post.

This article provides troubleshooting tips and an FAQ for Microsoft Edge version 77 or later.

> [!NOTE]
> This article applies to Microsoft Edge version 77 or later.

## Troubleshoot IE Mode

Use the information in this section to diagnose and fix IE mode problems.

### Internet Explorer mode  general diagnostic information

You can get Internet Explorer mode diagnostic information on the Microsoft Edge Compatibility tab. To open this tab, go to *edge://compat/iediagnostic*. This page may show diagnostic messages. This page also provides configuration information for the following categories:

- **Registry key check.** (Displayed only if the check fails.) Checks to see if Internet Explorer integration is set up correctly in the registry. If not, the user can click Fix it to resolve the problem.
- **Internet Explorer mode.** Shows the API version that's used, based on the configuration and OS. If there's a problem, the user may be prompted to install a Windows Update.
- **Internet Explorer mode setting.** Shows whether Internet Explorer mode is enabled, and how it's configured.
- **Command line.** Shows the command line string and switches used to start Microsoft Edge.
- **Group policy settings.** Shows whether IE mode is configured using group policies, and the policies that are applied.

### Error message: "To open this page in Internet Explorer mode, reinstall Microsoft Edge with administrator privileges."

You might see this error if you don't have all required Windows Updates. See the prerequisites listed in [About IE mode](./edge-ie-mode.md) for the required versions of Windows and Microsoft Edge.

If you've already installed all required Windows Updates, you might see this error if:

- You're using the Canary channel, which is installed at the user level by default.
- You're using the Stable, Beta, or Dev channel, but when prompted for elevation when installing the elevation was canceled. When you cancel the elevation prompt, the installation will continue at the user level.
- Internet Explorer 11 has been disabled in Windows Features.

Possible solutions are:

- Run the installer for any channel at the system level: `installer.exe --system-level`.
- Enable Internet Explorer 11 in Windows Features.

To check if Microsoft Edge is installed at the systems level, type "edge://version" in the Microsoft Edge address bar. The Executable path will show a path starting with *C:\Program Files*, which indicates a system install. If the Executable path begins with *C:\Users*, uninstall and then reinstall Microsoft Edge with administrator privileges.

### Error message "To open this page in IE mode, try restarting Microsoft Edge."

You might see this error if there was an unexpected error in Internet Explorer. Restarting Microsoft Edge usually fixes this error.

### Error message: "Turn off remote debugging to open this site in IE mode otherwise it might not work as expected."

You might see this error if you're remote debugging and navigate to a web page configured to run in IE mode. You can continue, but the page will be rendered using Microsoft Edge.

### Error message: "Error: Could not retrieve EMIE site list."

You might see this error on the *edge://compat/enterprise* page indicating that the site list download failed. Starting with Microsoft Edge version 87, when cookies are blocked for third party requests using the [BlockThirdPartyCookies](/deployedge/microsoft-edge-policies#blockthirdpartycookies) policy, HTTP authentication is also disallowed. You can allow cookies for the specific domain hosting your Enterprise Mode Site List using the [CookiesAllowedForURLs](/deployedge/microsoft-edge-policies#cookiesallowedforurls) policy to ensure that site list downloads are successful.

## Frequently Asked Questions

### Will IE mode replace Internet Explorer 11?

Yes, the Internet Explorer 11 desktop application will be retired and go out of support on June 15, 2022. To see what’s in scope, see [Lifecycle FAQ - Internet Explorer](/lifecycle/faq/internet-explorer-microsoft-edge). The same IE11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode. To learn more, read [The future of Internet Explorer on Windows 10 is in Microsoft Edge](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).

### How can I debug my legacy application while using IE mode on Microsoft Edge?

You can use IEChooser to launch the Internet Explorer DevTools to debug the content of your IE mode tabs. To use IEChooser, follow these steps:

1. Open IEChooser.
   - Open the Run dialog box. For example, press the `Windows logo key` + `R`.
   - Enter `%systemroot%\system32\f12\IEChooser.exe`, and then select **Ok**.
2. In IEChooser, select the entry for the IE mode tab.

### Can I test a site in Microsoft Edge while it is configured to open IE mode in the Enterprise Mode Site List?

Yes, while you are modernizing your legacy sites, you can test IE mode configured applications on Microsoft Edge. To accomplish this, you can run Microsoft Edge with the `--ie-mode-test` command line flag. Make sure that there are no other Microsoft Edge instances running. Then you can select **Settings and more** (the ellipses icon ...) **> More Tools > Open sites in Edge mode**.

### Can I use "Open with Explorer" or "View in File Explorer" in SharePoint with IE mode?

Yes, if this option works in standalone Internet Explorer 11 it will work in IE mode. However, rather than use the Open with Explorer option, the recommended approach to managing files and folders outside of SharePoint is to [Sync SharePoint and Teams files with your computer](https://support.microsoft.com/office/sync-sharepoint-and-teams-files-with-your-computer-6de9ede8-5b6e-4503-80b2-6190f3354a88?ui=en-us&rs=en-us&ad=us) or [Move or copy files in SharePoint](https://support.microsoft.com/office/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc?ui=en-us&rs=en-us&ad=us).

### Does IE mode on Microsoft Edge support the 'no-merge' option that was supported in Internet Explorer 11?

The recommended alternatives for the no-merge functionality in Microsoft Edge are one of the following actions:

1. Use Profiles in Microsoft Edge - Each profile maps to a different IE session for IE mode pages, so it behaves identically to the no-merge option.
2. Use the `--user-data-dir=<path>` command line, but with a different path for each session. If needed, you can create a utility for the user to run that both launches Microsoft Edge and changes the path for the session.

If neither of those options work for your scenario, starting in Microsoft Edge version 93, IE mode on Microsoft Edge will support no-merge. For an end-user, when a new browser window is launched from an IE mode application, it will be in a separate session, like the no-merge behavior in IE11.

Behind the scenes, for each window of Microsoft Edge, the first time an IE mode tab is visited within that window, if it is one of the designated "*no-merge*" sites, that window is locked into a different "no-merge" IE session from all other Microsoft Edge windows at least until the last IE mode tab is closed in that window. This follows previous behavior where users could launch IE with no-merge and could also launch Microsoft Edge without no-merge via other mechanisms. All sites opening in a new window (through window.open) will respect the merge nature of the parent process. Please note that session switching isn’t supported; navigations within the same IE mode tab will use the same session.

You can validate the behavior in Microsoft Edge version 93 or later by following these steps:


## See also
  
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [About IE mode](./edge-ie-mode.md)
- [Additional Enterprise Mode information](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)