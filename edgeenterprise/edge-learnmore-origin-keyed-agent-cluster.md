---
title: "Microsoft Edge will disable modifying 'document.domain' to relax the same-origin policy"
ms.author: niarci
author: dan-wesley
manager: erikan
ms.date: 04/18/2022
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
> If your website relies on relaxing the same-origin policy via `document.domain`, your action is required. Continue to read more about why this is changing or go to the [Alternative cross-origin communication](#alternative-cross-origin-communication) for cross-origin communication.

## Introduction

The domain property of the Document interface gets or sets the domain part of the origin of the current document, as used by the [same-origin policy](https://developer.mozilla.org/docs/Web/Security/Same-origin_policy).

On Microsoft Edge, websites will be unable to set `document.domain`. You'll need to use alternative approaches, such as `postMessage()` or the Channel Messaging API, to communicate cross-origin. We're targeting Microsoft Edge version 106 to ship this change at the earliest.

If your website relies on same-origin policy relaxation via `document.domain` to function correctly, the site will need to send an `Origin-Agent-Cluster: ?0` header, as will all other documents that require that behavior.

> [!NOTE]
> `document.domain` has no effect if only one document sets it.

## Why make `document.domain` immutable?

Many websites set `document.domain` to allow communication between "same-site but cross-origin" pages.

> [!IMPORTANT]
> Same-site but cross-origin sites have the same [eTLD+1](https://web.dev/same-site-same-origin/#:~:text=the%20whole%20site%20name%20is%20known%20as%20the%20etld%2B1) but different subdomains.

Here's how `document.domain` is used.

Let's say a page on `https://parent.example.com` embeds an iframe page from `https://video.example.com`. These pages have the same eTLD+1 (`example.com`) with different subdomains. When both pages' `document.domain` is set to `'example.com'`, the browser treats the two origins as if they're same-origin.

The next example shows how to create a cross-origin DOM manipulation on `https://parent.example.com` against `https://video.example.com`.

The following code shows how to set the `document.domain` for `https://parent.example.com`:

```

// Confirm the current origin of "parent.example.com" 

console.log(document.domain); 

// Set the document.domain 

document.domain = 'example.com'; 

console.log(document.domain); 

```

The following code shows how to set the `document.domain` for `https://video.example.com`: 

```

// Confirm the current origin of "video.example.com" 

console.log(document.domain); 

// Set the document.domain 

document.domain = 'example.com'; 

console.log(document.domain); 

```

Now you can perform cross-origin DOM manipulation on `https://parent.example.com` against `https://video.example.com`.

Websites set `document.domain` to make it possible for same-site documents to communicate more easily. Because this change [relaxes the same-origin policy](https://html.spec.whatwg.org/multipage/origin.html#relaxing-the-same-origin-restriction), the parent page can access the iframe's document and traverse the DOM tree, and vice versa.

This technique is convenient; but  it introduces a security risk.  

## Security concerns with `document.domain`

Security concerns around `document.domain` have led to a change in the specification that warns users about this concern and tells them to avoid using it if possible. The current discussion with [other browser vendors](https://github.com/w3ctag/design-reviews/issues/564) is moving in the same direction.

The following example shows how an attacker can manipulate `document.domain`.

If a hosting service provides different subdomains per user, an attacker can set `document.domain` to pretend they're the same-origin as another user's page. An attacker can host a website under a shared hosting service, which serves sites through the same IP address with different port numbers. In this scenario, the attacker can pretend to be on the same-site-but-same-origin as yours.  This attack is possible because `document.domain` ignores the port number part of the domain.

To learn more about the security implications of setting `document.domain`, read the [Document.domain article on MDN](https://developer.mozilla.org/docs/Web/API/Document/domain#setter).

> [!NOTE]
> Microsoft Edge plans to make `document.domain` immutable in Microsoft Edge version 106.

## How will I know if my site is affected? 

If your website is affected by this change, Microsoft Edge will show a warning in the DevTools Issues panel. The following screenshot shows an example of this warning.

:::image type="content" source="media/edge-learnmore-origin-keyed-agent-cluster/document-domain-modification-warning.png" alt-text="Warning when document.domain is modified.":::

If you have a reporting endpoint set up, you'll also be sent deprecation reports. Learn more about [how to use the Reporting API](https://web.dev/reporting-api/) with existing report collection services or by building your own reporting solution.

> [!TIP]
> You can run your site through the [LightHouse deprecated API audit](https://web.dev/deprecations/) to find all APIs that are scheduled to be removed from Microsoft Edge.

## Alternative cross-origin communication

At this time, you have two options to replace `document.domain` for your website. In most use cases, cross-origin [postMessage()](https://developer.mozilla.org/docs/Web/API/Window/postMessage) or the [Channel Messaging API](https://developer.mozilla.org/docs/Web/API/Channel_Messaging_API) can replace `document.domain`.

The following list shows the steps a developer needs to take to use `postMessage()` instead of `document.domain` for cross-origin DOM manipulation.

1. `https://parent.example.com` requests `https://video.example.com` in an iframe to manipulate the DOM by sending a message via `postMessage()`.
2. `https://video.example.com` manipulates DOM as soon as it receives the message and notifies  the parent of its success.
3. `https://parent.example.com` acknowledges the success.


On `https://parent.example.com`:

```

// Send a message to https://video.example.com 

iframe.postMessage('Request DOM manipulation', 'https://video.example.com'); 

// Receive messages 

iframe.addEventListener('message', (event) => { 

  // Reject all messages except ones from https://video.example.com 

  if (event.origin !== 'https://video.example.com') return; 

  // Filter success messages 

  if (event.data === 'succeeded') { 

    // DOM manipulation is succeeded 

  } 

}); 

```

On `https://video.example.com`:

```

// Receive messages 

window.addEventListener('message', (event) => { 

  // Reject all messages except ones from https://parent.example.com 

  if (event.origin !== 'https://parent.example.com') return; 

  // Do a DOM manipulation on https://video.example.com. 

  // Send a success message to https://parent.example.com 

  event.source.postMessage('succeeded', event.origin); 

}); 

```

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

- [Document.domain](https://developer.mozilla.org/docs/Web/API/Document/domain)
- [Origin Isolation and Deprecating `document.domain`](https://github.com/mikewest/deprecating-document-domain/)
- [Deprecating `document.domain` setter](https://github.com/w3ctag/design-reviews/issues/564)

## Content license

> [!NOTE]
> Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms 
  described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/). The original page can be found [here](https://github.com/google/re2/wiki/Syntax).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.