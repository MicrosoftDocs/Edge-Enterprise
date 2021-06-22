---
title: "Interrupting Downloads of Potentially Dangerous Files"
ms.author: kvice
author: AndreaLBarr
manager: srugh
ms.date: 05/20/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Interrupting Downloads of Potentially Dangerous Files"
---

# Interrupting Downloads of Potentially Dangerous Files

Microsoft Edge’s File Type Policies component allows files to be classified by their level of “dangerousness”, such that harmless files (e.g. `.txt` files) can be downloaded freely, whilst potentially-dangerous files (e.g. `.dll` files) are subjected to a higher degree of vetting and a more security-conscious user-experience.

## Determining the Danger Level of a File Type

Microsoft Edge inherits its file type policies from the upstream Chromium browser; you can view the current contents of the list [here](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb). Within the list, you’ll see that each type has a danger_level, which is one of three values: `DANGEROUS`, `NOT_DANGEROUS`, or `ALLOW_ON_USER_GESTURE`.

The first two are simple: **NOT_DANGEROUS** means that the file is safe to download, even if the download was accidental. **DANGEROUS** means that the browser should always warn the user that the download may harm their device.

The third setting **ALLOW_ON_USER_GESTURE** is more subtle. Such files are potentially dangerous, but most likely harmless if the user requested the download. Microsoft Edge will allow such downloads to proceed automatically if two conditions are met:

1. There is a [user gesture](https://textslashplain.com/2020/05/18/browser-basics-user-gestures/) associated with the network request that initiated the download (e.g., the user clicked a link to the download).
2. There is a recorded prior visit to the referring origin (the page linking to the download) prior to the most recent midnight (i.e., yesterday or earlier). This implies that the user has a history of visiting the site.

The download will also proceed automatically if the user explicitly initiated it by using the **Save link as** context menu command, entered the download’s URL directly into the browser’s address bar, or if Microsoft Defender SmartScreen indicated that the file is safe.

**Update:** Starting in version 91, Microsoft Edge will interrupt downloads that lack the required gesture.

## User Experience for Downloads Lacking Gestures

If a download for a potentially dangerous type starts without the required gesture, Microsoft Edge states that the download “was blocked”. Commands named `Keep` and `Delete` are available from the … menu on the download item to allow the user to continue or cancel the download.

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/Dowload-was-blocked.png" alt-text="Download Was Blocked":::

On the `edge://downloads`, page, the user will see the same options:

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/msg-keep-delete-option.png" alt-text="MSG Keep Delete Option":::

## Enterprise Controls

While users are unlikely to encounter download interruptions for sites they use every day, they might encounter them for legitimate downloads on sites that they use rarely. To help streamline the user-experience for Enterprises, a Group Policy is available.

Enterprises can use [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) to specify the filetypes that are allowed to download from specific sites without interruption. For instance, the following policy allows XML files to download from contoso.com and woodgrovebank.com without interruption, and MSG files to download from any site.

`[{"file_extension":"xml","domains":["contoso.com", "woodgrovebank.com"]},
{"file_extension":"msg", "domains": ["*"]}]`

## File Types Requiring a Gesture

The latest [file types policies](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb) are published in the Chromium source code. As of May 2021, file types with a `danger_level` of `ALLOW_ON_USER_GESTURE` on at least one OS platform include:
`crx, pl, py, pyc, pyo, pyw, rb, efi, oxt, msi, msp, mst, ade, adp, mad, maf, mag, mam, maq, mar, mas, mat, mav, maw, mda, mdb, mde, mdt, mdw, mdz, accdb, accde, accdr, accda, ocx, ops, paf, pcd, pif, plg, prf, prg, pst, cpi, partial, xrm-ms, rels, svg, xml, xsl, xsd, ps1, ps1xml, ps2, ps2xml, psc1, psc2, js, jse, vb, vbe, vbs, vbscript, ws, wsc, wsf, wsh, msh, msh1, msh2, mshxml, msh1xml, msh2xml, ad, app, application, appref-ms, asp, asx, bas, bat, chi, chm, cmd, com, cpl, crt, cer, der, eml, exe, fon, fxp, hlp, htt, inf, ins, inx, isu, isp, job, lnk, mau, mht, mhtml, mmc, msc, msg, reg, rgs, scr, sct, search-ms, settingcontent-ms, shb, shs, slk, u3p, vdx, vsx, vtx, vsdx, vssx, vstx, vsdm, vssm, vstm, vsd, vsmacros, vss, vst, vsw, xnk, cdr, dart, dc42, diskcopy42, dmg, dmgpart, dvdr, dylib, img, imgpart, ndif, service, smi, sparsebundle, sparseimage, toast, udif, action, definition, wflow, caction, as, cpgz, command, mpkg, pax, workflow, xip, mobileconfig, configprofile, internetconnect, networkconnect, pkg, deb, pet, pup, rpm, slp, out, run, bash, csh, ksh, sh, shar, tcsh, desktop, dex,apk`

## Danger Level May Vary By Operating System

File type settings sometimes vary depending on the client OS platform. For instance, an `.exe` is not dangerous on a Mac, while an `.applescript` is harmless on Windows.
