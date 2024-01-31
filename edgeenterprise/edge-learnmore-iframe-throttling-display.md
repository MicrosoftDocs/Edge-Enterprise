---
title: "Throttling for all cross-origin iframes that are display: none and non-visible."
ms.author: sajos
author: dan-wesley
manager: alias
ms.date: 06/12/2023
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "A description of iframe throttling and the need for standardization."
---

# Throttling for all cross-origin iframes that are `display: none` and non-visible.

This article describes iframe throttling and the benefits of standardizing throttling for `display: none` and non-visible.

>[!NOTE]
>This article applies to Microsoft Edge version 116 or later.

## Summary

Cross-origin iframes that are `display: none` and non-visible are throttled when rendered cross-process, but not when they're rendered same-process. The absence of throttling in same-process scenarios could lead to unpredictable behavior for developers, who might not know the underlying process model used to render the page. Also, with this iframe scenario, a malicious actor can probe to see whether a browsing session has site/origin isolation enabled.

Throttled iframes lose access to `requestAnimationFrame` and `ResizeObserver`, so the different throttling approaches affect web developers. This feature standardizes throttling, so it applies to all cross-origin iframes, regardless of whether they're same-process or cross-process.

> [!NOTE]
> "non-visible" means a non-zero area frame that's outside the viewport.

## Objective

Iframe throttling is a Blink mechanism that tries to reduce layout and rendering overhead. Frames that are throttled only undergo partial layout, and `requestAnimationFrame` and `ResizeObserver` don't operate when a frame is throttled. Cross-origin iframes that are placed in a different process than their parent, and that are either `display: none` or non-visible are throttled. Currently a cross-origin frame that's rendered in the same-process as its parent isn'tthrottled, leading to different behavior based on a process model. When enabled, this policy throttles all cross-origin, `display: none` or non-visible frames, which gives consistent behavior between the same-process and cross-process cases.

## Content license

> [!NOTE]
> Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms 
  described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/). The original page can be found [here](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)