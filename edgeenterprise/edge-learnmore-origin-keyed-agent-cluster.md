---
title: "Microsoft Edge will disable modifying 'document.domain'"
ms.author: erikan
author: dan-wesley
manager: erikan
ms.date: 11/6/2023
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Microsoft Edge will disable modifying 'document.domain'"
---

# Microsoft Edge will disable modifying `document.domain`

> [!WARNING]
> If your website relies on relaxing the same-origin policy via `document.domain`, your action is required. Continue to read more about why this is changing or go to the [Alternative cross-origin communication](#alternative-cross-origin-communication) to learn about alternative mechanisms to achieve cross-origin communication.

## Introduction

The "domain" property of the Document interface gets or sets the domain part of the origin of the current document, as used by the [same-origin policy](https://developer.mozilla.org/docs/Web/Security/Same-origin_policy).

Microsoft Edge inherited this change from Chromium. Attempts to modify the `document.domain` property using JavaScript are now ignored.  You'll need to use alternative approaches, such as `postMessage()` or the Channel Messaging API, to communicate cross-origin. This change is in Edge 119 and later.

As an alternative, if your website relies on same-origin policy relaxation via `document.domain` to function correctly, the site may send an `Origin-Agent-Cluster: ?0` header; this header must be sent from all other documents that require the relaxation.

> [!NOTE]
> `document.domain` has no effect if only one document sets it.

## Why make `document.domain` immutable?

Some websites set `document.domain` to allow communication between "same-site but cross-origin" pages. Setting `document.domain` makes it possible for same-site documents to communicate more easily. Because this change [relaxes the same-origin policy](https://html.spec.whatwg.org/multipage/origin.html#relaxing-the-same-origin-restriction), a parent page can access a same-site iframe's document and traverse the DOM tree, and vice versa.

> [!IMPORTANT]
> Same-site but cross-origin sites have the same [eTLD+1](https://web.dev/same-site-same-origin/#:~:text=the%20whole%20site%20name%20is%20known%20as%20the%20etld%2B1) but different subdomains.

Let's say a page on `https://parent.example.com` embeds an iframe page from `https://video.example.com`. These pages have the same eTLD+1 (`example.com`) with different subdomains. When both pages' `document.domain` is set to `'example.com'`, the browser treats the two pages as if they're same-origin.

This technique is convenient; but  it introduces a security risk.  

## Security concerns with `document.domain`

Security concerns around `document.domain` have led to a change in the specification that warns developers about this concern and tells them to avoid using it if possible. The current discussion with [other browser vendors](https://github.com/w3ctag/design-reviews/issues/564) is moving in the same direction.

The following examples show how an attacker can abuse `document.domain`.

Consider a shared hosting service that provides a unique subdomain to each customer. If a developer sets `document.domain` in their page, an attacker's page served from a different subdomain can set the same value and modify the content of the victim page.

Similarly, consider a shared hosting service that serves pages using a different port for each customer. If a developer sets `document.domain` in their page, an attacker's page served from a different port can set the same value and modify the content of the victim page. This attack is possible because `document.domain` ignores the port number component of the origin.

> [!NOTE]
>To learn more about the security implications of setting `document.domain`, read the [Document.domain article on MDN](https://developer.mozilla.org/docs/Web/API/Document/domain#setter).

## How will I know if my site is affected?

If your website is affected by this change, Microsoft Edge will show a warning in the DevTools Issues panel. The following screenshot shows an example of this warning.

:::image type="content" source="media/edge-learnmore-origin-keyed-agent-cluster/document-domain-modification-warning.png" alt-text="Warning when document.domain is modified.":::

If you have a reporting endpoint set up, you'll also be sent deprecation reports. Learn more about [how to use the Reporting API](https://web.dev/reporting-api/) with existing report collection services or by building your own reporting solution.

> [!TIP]
> You can run your site through the [LightHouse deprecated API audit](https://web.dev/deprecations/) to find all APIs that are scheduled to be removed from Microsoft Edge.

## Alternative cross-origin communication

Currently you have two options to replace `document.domain` for your website. In most use cases, cross-origin [postMessage()](https://developer.mozilla.org/docs/Web/API/Window/postMessage) or the [Channel Messaging API](https://developer.mozilla.org/docs/Web/API/Channel_Messaging_API) can replace `document.domain`.

The following list shows the steps a developer needs to take to use `postMessage()` instead of `document.domain` for cross-origin DOM manipulation.

1. `https://parent.example.com` sends a message via `postMessage()` to an iframe containing `https://video.example.com` asking it to modify its own DOM.
2. `https://video.example.com` manipulates its DOM and uses `postMessage` to notify the parent of its success.
3. `https://parent.example.com` acknowledges the success.

For step 1 on `https://parent.example.com`:

```

// Configure a handler to receive messages from the subframe.
iframe.addEventListener('message', (event) => { 

// Reject all messages except from https://video.example.com 
  if (event.origin !== 'https://video.example.com') return;
  
  // Filter success messages 
    if (event.data === 'succeeded') { 

    // DOM manipulation is succeeded 

  } 

}); 

// Send a message to the subframe at https://video.example.com

iframe.postMessage('Request DOM manipulation', 'https://video.example.com'); 

```

For step 2 on `https://video.example.com`:

```

// Configure a handler to receive messages from the parent frame.
window.addEventListener('message', (event) => {
 
  // Reject all messages except ones from https://parent.example.com 
  
  if (event.origin !== 'https://parent.example.com') return;
  
  // Perform requested DOM manipulation on https://video.example.com.
  
  if (event.data === "showTheButton") {
     document.getElementById('btnContinue').style.visibility = 'visible';
     // Send a success message back to the parent.

     event.source.postMessage('succeeded', event.origin); 
  }
}); 

```

### Send the `Origin-Agent-Cluster: ?0` header as a last resort

If you have strong reasons to continue setting `document.domain`, you can send `Origin-Agent-Cluster: ?0` response header on the target document.

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

- [Document.domain](https://developer.mozilla.org/docs/Web/API/Document/domain)
- [Origin Isolation and Deprecating `document.domain`](https://github.com/mikewest/deprecating-document-domain/)
- [Deprecating `document.domain` setter](https://github.com/w3ctag/design-reviews/issues/564)

## Content license

> [!NOTE]
> Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/). The original page can be found [here](https://developer.chrome.com/blog/immutable-document-domain/).

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
