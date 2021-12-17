---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: leahtu
author: dan-wesley
manager: srugh
ms.date: 12/17/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Microsoft Edge release notes for Stable Channel"
---

# Release notes for Microsoft Edge Stable Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Stable Channel.

- All the security updates are listed in [Release notes for Microsoft Edge Security Updates](./microsoft-edge-relnotes-security.md).
- Archived release notes for Microsoft Edge Stable Channel are located in [Archived release notes for Microsoft Edge Stable Channel](./microsoft-edge-relnote-archive-stable-channel.md).

 To understand Microsoft Edge channels, see the [Overview of the Microsoft Edge channels](./microsoft-edge-channels.md).

> [!NOTE]
> For the Stable Channel, updates will roll out progressively over one or more days. To learn more, see [Progressive rollouts for Microsoft Edge updates](./microsoft-edge-update-progressive-rollout.md).
>
> Microsoft Edge Web Platform constantly evolves to improve user experience, security, and privacy. To learn more, see [Site compatibility-impacting changes coming to Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## Version 97.0.0000.00: January 7
<!-- link to most recent, then delete this comment --->
Stable channel security updates are listed [here](/deployedge/microsoft-edge-relnotes-security#december-14-2021).

### Feature updates
<!-- placeholder ---->
- **Cloud Site List Management for IE mode in Public Preview.** verbiage

- **Use current profile to sign into websites when multiple work or school accounts are signed in on a device.** When multiple work or school accounts are signed in on a device, users will be asked to choose an account from the account picker to continue their visits to websites. In this release, users will be prompted to let Microsoft Edge sign in to the websites automatically with the work and school account signed into current profile. Users can turn this feature on and off in **Settings** > **Profile preferences**.

- **Add support for Microsoft Endpoint Data Loss Prevention (DLP) on MacOS.** Microsoft Endpoint DLP policy enforcement will be available natively on MacOS.

- **Automatic HTTPS.** Users will have the option to upgrade navigations from HTTP to HTTPS on domains that support this more secure protocol. This protocol support can also be configured to attempt delivery over HTTPS for all domains. Note: This feature is a Controlled Feature Rollout. If you don’t see this feature, check back as we continue our rollout.

- **Block WebSQL in 3rd-party contexts.** Use of the legacy WebSQL feature will be blocked from 3rd-party frames. An Enterprise policy [WebSQLInThirdPartyContextEnabled](/deployedge/microsoft-edge-policies#websqlinthirdpartycontextenabled) is available as an opt-out until Microsoft Edge version 101. This change is happening in the Chromium project, on which Microsoft Edge is based. For more information, see this [Chrome Platform Status](https://chromestatus.com/feature/5684870116278272) entry.

•	**Citations in Microsoft Edge.** Citing sources for research is a common requirement for students. They have to manage many research references and sources, which isn't easy. They also have to translate these citations to the correct citation formats such as APA, MLA, and Chicago. This new "Citations" feature in Microsoft Edge (now in Preview) gives students a better way to manage and generate citations as they research online. With Citations turned on in Collections (Ctrl + Shift + Y) or from Settings and more (Alt + F), Microsoft Edge automatically generates citations that students can use later so they can stay focused on their research. When they're done they can easily compile these citations into a final deliverable. For more information, see [Previewing Citations in Microsoft Edge](https://blogs.windows.com/msedgedev/2021/11/04/preview-citations-feature-edge/).


### Policy updates

#### New Policies
<!-- placeholder ---->
- [ApplicationGuardUploadBlockingEnabled](/DeployEdge/microsoft-edge-policies#applicationguarduploadblockingenabled) Prevents files from being uploaded while in Application Guard

#### Obsoleted Policies

