---
title: "Copilot webpage summarization behavior"
ms.author: prithviokade
author: dan-wesley
manager: likuba
ms.date: 12/12/2023
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "This article shows the results of Copilot page summary tests."
---

# Copilot webpage summarization behavior

The following chart explains the current behavior of Copilot webpage summarization on various document types. This information will be updated when support for summarization increases. This chart covers the behavior in both Copilot and Copilot with Commercial Data Protection. Support for these document types only applies to Edge Copilot.

> [!NOTE]
> **Contextual grounding in Edge Copilot:** This is the ability to ground a chat conversation in the current web page context. It applies to queries such as "Summarize this document" or "What does this page say about…" in reference to the main Edge window. Contextual grounding only applies to Sidebar instances of chat, because desktop/full-screen instances do not allow for simultaneous web context.

| Document type | Copilot and Copilot with Commercial Data Protection |
|:-----|:-----|
| Intranet Sites such as SharePoint | Summarization is supported<br>\* Embedded Office docs in SharePoint aren't supported |
| Public Sites such as Wikipedia    | Summarization is supported |
| Outlook Web App                   | Summarization is supported |
| PDF                               | Summarization is supported |
| Office Documents                  | Summarization isn't supported |
| Purview DLP Policies **           | Summarization isn't supported |
| MAM/MDA Policies ++               | Summarization isn't supported |

** Purview DLP Policies need to be set to either "block" or "warn" and the admin must also flag "no page context extraction/summarization" to prevent these documents from being reviewed by Edge.

++ MAM "Block" policy will disable contextual grounding/summarization. MDA "Block" and "Audit" must both be active to disable contextual grounding/summarization.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
