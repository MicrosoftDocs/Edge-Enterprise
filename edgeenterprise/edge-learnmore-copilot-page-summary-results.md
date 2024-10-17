---
title: "Copilot in Edge webpage summarization behavior"
ms.author: prithviokade
author: dan-wesley
manager: likuba
ms.date: 10/16/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "This article shows the results of Copilot page summary tests."
---

# Copilot in Edge webpage summarization behavior

> [!NOTE]
> Page summarization features are being rolled out for Copilot with enterprise data protection in Edge. You may not yet have access to this feature.  

The following chart explains the current behavior of Copilot in Edge webpage summarization on various document types. This information will be updated when support for summarization increases. This chart covers the behavior in Copilot both when enterprise data protection is applied and when it is not. Support for these document types only applies to Copilot in Edge.

> [!NOTE]
> Contextual grounding in Copilot in Edge: This is the ability to ground a chat conversation in the current webpage context. It applies to prompts such as "Summarize this document" or "What does this page say about…" in reference to the tab currently being viewed by the user in the main Edge window. Contextual grounding only applies to instances of chat when using Copilot in the Edge sidebar, because desktop/full-screen instances do not allow for simultaneous web context.

| Document type | Copilot and Copilot with Enterprise Data Protection |
|:-----|:-----|
| Intranet Sites such as SharePoint | Summarization is supported<br>\* Embedded Office docs in SharePoint aren't supported |
| Public Sites such as Wikipedia    | Summarization is supported |
| Outlook Web App                   | Summarization is supported |
| PDFs                              | Summarization is supported |
| Office Documents                  | Summarization isn't supported |
| Sites protected by Purview DLP Policies ** | Summarization isn't supported |
| Sites protected by MAM Policies ^^   |  Summarization isn't supported |
| Sites protected by MDA Policies ++ | Summarization isn't supported |

** Sites protected by Purview DLP Policies disallow summarization if any policy&mdash;except for "paste"&mdash;is set to "block" or "override."

++ Sites protected by MDA Policies disallow summarization if any policy is set to "audit" or "block."

^^ Sites protected by MAM Policies disallow summarization if any policy is set to "block."

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
