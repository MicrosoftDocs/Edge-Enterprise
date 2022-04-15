---
title: "Microsoft Edge will disable modifying 'document.domain' to relax the same-origin policy"
ms.author: niarci
author: dan-wesley
manager: erikan
ms.date: 04/07/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Microsoft Edge will disable modifying 'document.domain' to relax the same-origin policy"
---

# Microsoft Edge will disable modifying `document.domain` to relax the same-origin policy

> [!NOTE]
> This article applies to Microsoft Edge Stable version 106 or later.

> [!WARNING]
> f your website relies on relaxing the same-origin policy via `document.domain`, your action is required. Continue to read more about why this is changing or go to the [Alternative cross-origin communication](#alternative-cross-origin-communication) for cross-origin communication.

## Introduction


## Security concerns with `document.domain`



## Alternative cross-origin communication



### Send the `Origin-Agent-Cluster: ?0` header as a last resort

If you have strong reasons to continue setting `document.domain`, you can send `Origin-Agent-Cluster: ?0` response header along with the target document.

``` 

Origin-Agent-Cluster: ?0 

```

The `Origin-Agent-Cluster` header instructs the browser whether the document should be handled by the origin-keyed agent cluster or not. To learn more about `Origin-Agent-Cluster`, read [Requesting performance isolation with the Origin-Agent-Cluster header](https://web.dev/origin-agent-cluster/).

When you send this header, your document can continue to set `document.domain` even after it becomes immutable by default.

## Browser compatibility

The following organizations support deprecating `document.domain` in the interest of browser compatibility.

- The [Origin specification](https://html.spec.whatwg.org/multipage/origin.html#:~:text=Because%20of%20these%20security%20pitfalls%2C%20this%20feature%20is%20in%20the%20process%20of%20being%20removed%20from%20the%20web%20platform), states that the feature should be removed.
- The [Mozilla standards position](https://github.com/mozilla/standards-positions/issues/601) considers disabling `document.domain` by default worth prototyping.
- [WebKit](https://github.com/w3ctag/design-reviews/issues/564#issuecomment-768450217) indicates that they're moderately positive about deprecating `document.domain` setter.

## Other resources

- [Document.domain](https://developer.mozilla.org/en-US/docs/Web/API/Document/domain)
- [Origin Isolation and Deprecating `document.domain`](https://github.com/mikewest/deprecating-document-domain/)
- [Deprecating `document.domain` setter](https://github.com/w3ctag/design-reviews/issues/564)

## Content license

> [!NOTE]
> Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms 
  described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/). The original page can be found [here](https://github.com/google/re2/wiki/Syntax).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.