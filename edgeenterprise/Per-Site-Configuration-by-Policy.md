---
title: "Per-Site Configuration by Policy "
ms.author: v-andreabarr
author: AndreaLBarr
manager: laurawi
ms.date: 05/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Per-Site Configuration by Policy "
---
# PerSite Configuration by Policy

## Introduction: Browsers as Decision Makers

As a part of every page load, browsers make many decisions — should a particular API be available? Should a resource load be permitted? Should script be allowed to run? The list is long.

In most cases, decisions are governed by two inputs: a user setting, and the URL of the page for which the decision is being made.

In the legacy Internet Explorer web platform, each of these decisions was called an [URLAction](https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178%28v%3dvs.85%29), and Enterprise Group Policy and user settings inside the Internet Control Panel controlled how the browser would handle each decision.  

In the Microsoft Edge, most per-site permissions are controlled by settings and policies expressed using a simple syntax with limited wild carding support. Windows Security Zones are still used only for a small number of configuration decisions.

## Background: Windows Security Zones

To simplify configuration for the user or their administrator, the legacy platform classified sites into five different **Security Zones:** Local Machine, Local Intranet, Trusted, Internet, and Restricted Sites.

When making a decision, the browser would first map the website to a Zone, then consult the setting for that URLAction for that Zone to decide what to do. Reasonable defaults like “Automatically satisfy authentication challenges from my Intranet” meant that most users never needed to change any settings away from their defaults.

Users can use the Internet Control Panel to assign specific sites to Zones and to configure the permission results for each zone. In managed environments, administrators can use Group Policy to assign specific sites to Zones (via “Site to Zone Assignment List” policy) and specify the settings for URLActions on a per-zone basis. Beyond manual administrative or user assignment of sites to Zones, additional heuristics could [assign sites to the Local Intranet Zone](https://docs.microsoft.com/archive/blogs/ieinternals/the-intranet-zone). In particular, dot less host names (e.g.://payroll) were assigned to the Intranet Zone. If a Proxy Configuration script was used, any sites configured to bypass the proxy would be mapped to the Intranet Zone.

Microsoft Edge Legacy inherited the Zones architecture from its Internet Explorer predecessor with a few simplifying changes:

- Windows’ five built-in Zones were collapsed to three: Internet (Internet), Trusted (Intranet+Trusted), and Local Computer. The Restricted Sites Zone was removed.

- Zone to URLAction mappings were hardcoded into the browser, ignoring Group Policies and settings in the Internet Control Panel.

## Per-Site Permissions in the Microsoft Edge

Unlike its predecessors, the new Microsoft Edge makes very limited use of Windows Security Zones. Instead, most permissions and features that offer administrators per-site configuration via [policy](https://docs.microsoft.com/deployedge/microsoft-edge-policies) rely on lists of rules in the [URL Filter Format](https://docs.microsoft.com/DeployEdge/edge-learnmmore-url-list-filter%20format).

When end-users open <code>edge://settings/content/siteDetails?site=https://example.com</code>, they’ll find a long list of configuration switches and lists for various permissions. Users rarely use the Settings Page directly, instead making choices while browsing using various widgets and toggles in the **Page Info** dropdown (which appears when you click the lock icon in the address bar) or via various prompts or buttons at the right-edge of the address bar.

Enterprises can use Group Policy to provision site lists for individual policies that control the browser’s behavior. To find these policies, simply open the [Microsoft Edge Group Policy documentation](https://docs.microsoft.com/deployedge/microsoft-edge-policies) and search for **ForUrls** to find the policies that allow and block behavior based on the loaded site’s URL. Most of the relevant settings are listed within the [Group Policy for Content Settings](https://docs.microsoft.com/deployedge/microsoft-edge-policies#content-settings) section.

There are also a number of policies (whose names contain **Default**) that control the default behavior for a given setting.

Many of the settings are very obscure (WebSerial, WebMIDI) and there’s very often no reason to change a setting away from the default (Images).

## Common Questions

## Q: Can the URL Filter Format match on a site’s IP address?

No, the format does not support specifying an IP-range for allow and block lists. It does support specification of individual IP **literals**, but such rules are only respected if the user navigates to the site using said literal (e.g. <http://127.0.0.1/>). If a hostname is used (<http://localhost>), the IP Literal rule will not be respected even though the resolved IP of the host matches the filter-listed IP.

## Q: Can URL Filters match just dot less host names?

No. You must individually list each desired hostname, e.g. (<https://payroll>, <https://stock>, <https://who>, etc).

If you were forward-thinking enough to structure your intranet such that your host names are of the form:

- <div style="display: inline">https://payroll.contoso-intranet.com</div>

- <div style="display: inline">https://timecard.contoso-intranet.com</div>

- <div style="display: inline">https://sharepoint.contoso-intranet.com</div>

Congratulations, you’ve implemented a best practice. You can configure each desired policy with a ***.contoso-intranet.com** entry and your entire Intranet will be opted in.

## Use of Security Zones in the Microsoft Edge

While Microsoft Edge mostly relies upon individual policies using the URL Filter format, it continues to use Windows’ Security Zones by default in a small number of places in order to simplify deployment within Enterprises that have historically relied upon Zones configuration. The following behaviors are controlled by Zone policy:

1. When deciding whether to release Windows Integrated Authentication (Kerberos/NTLM) credentials automatically

2. When deciding how to handle File Downloads

3. For Internet Explorer Mode

## Credential Release

By default, Microsoft Edge will evaluate URLACTION_CREDENTIALS_USE to decide whether Windows Integrated Authentication is used automatically, or the user should instead see a manual authentication prompt. Configuring an [AuthServerAllowlist site list policy](https://docs.microsoft.com/deployedge/microsoft-edge-policies#authserverallowlist) will prevent Zone Policy from being consulted.

## File Downloads

Evidence about the origins of a file download (the so-called “[Mark of the Web](https://textslashplain.com/2016/04/04/downloads-and-the-mark-of-the-web/) is recorded for files downloaded from the Internet Zone. Other applications (e.g. the Windows Shell, Microsoft Office, etc) may take this origin evidence into account when deciding how to handle a file.

If the Windows Security Zone policy is configured to Disable the setting Launching applications and unsafe files, the Microsoft Edge download manager will block file downloads from sites in that Zone with a note: “Couldn’t download – Blocked.”  

## IE mode

IE mode can be configured to [open all Intranet sites in IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode#configure-all-intranet-sites). When in this configuration, Edge evaluates the Zone of a URL when deciding whether or not it should open in IE mode. Beyond this initial decision, IE mode tabs are really running Internet Explorer, and as a consequence they evaluate Zones settings for every policy decision just as Internet Explorer itself did.

## Summary

In most cases, Microsoft Edge settings can be left at their defaults. Administrators who wish to change the defaults for all sites or specific sites can use the appropriate Group Policies to specify Site Lists or default behaviors. In a handful of cases (credential release, file download, and IE mode), administrators will continue to control behavior by configuring Windows Security Zones settings.
