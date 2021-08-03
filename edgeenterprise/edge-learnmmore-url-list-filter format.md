---
title: "Filter format for Microsoft Edge URL policies"
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Learn about the filter format used for Microsoft Edge URLBlocklist and URLAllowlist policies."
---

# Filter format for URL list-based policies

This article describes the filter format used for the Microsoft Edge URL list-based policies (For example, [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist), and [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls) policies.

> [!NOTE]
> This article applies to Microsoft Edge version 77 or later.

## The filter format

The filter format is:

```
    [scheme://][.]host[:port][/path][@query]
```

The fields in the filter format are:

| Field | Description |
| --- | --- |
| **scheme** (*optional*) | It can be http://, https://, ftp://, edge://, etc. |
| **host** (*required*) | It must be a valid host name and you can use a wildcard ("\*"). To disable subdomain matching, include an optional dot (".") before **host**. A single IP Address Literal hostname may be specified, but wildcarding is not supported for an IP Address Literal hostname. |
| **port** (*optional*) | Valid values range from 1 to 65535. |
| **path** (*optional*) | You can use any string in the path. |
| **query** (*optional*) | The **query** is either key-value or key-only tokens separated by an ampersand ("&"). Separate key-value tokens with an equal sign ("="). To indicate a prefix match, you can use an asterisk ("\*") at the end of the **query**. |

## Comparing the filter format to the URL format

The filter format resembles the URL format, except for the following differences:

- If you include "user:pass", it will be ignored. For example, http://user:pass@ftp.contoso.com/pub/example.iso.
- If you include a fragment identifier ("#"), it and everything that follows the identifier is ignored.
- You can use a wildcard ("*") as the **host** and you can prefix it with a dot (".").
- You can use a forward slash ("/") or a dot (".") as a suffix for the **host**. In this case, the suffix is ignored.

## Filter selection criteria

The filter selected for a URL is the most specific match found after processing the following filter selection rules:

1. Filters with the longest **host** match are selected first.
2. From the selected filters, any filter with a non-matching scheme or port is discarded.
3. From the remaining filters, the filter with the longest matching **path** is selected.
4. From the remaining filters, the filter with the longest set of query tokens is selected. At this step, the allow list filter takes precedence over the block list filter if both filters have the same **path** length and number of **query** tokens.
5. If there's no valid filter remaining, then the left-most subdomain is removed from **host** and the selection process starts over at step 1. The special asterisk ("*") **host** is the last searched and it matches all hosts.
6. If a filter's available, it blocks or allows the URL request.

   >[!NOTE]
   >The default behavior is to allow the URL request if no filter is matched.

## Example filter selection criteria

In this example, when searching for a match to "https://sub.contoso.com/docs" the filter selection will:

1. Search for a filter for "sub.contoso.com". If it finds a filter, the search moves to step 2. If a filter isn't found, then it tries again with "contoso.com", "com", and finally "".
2. From the selected filters, any that don't have "http" in the **scheme** are removed.
3. From the remaining filters, any that have an exact port number that isn't "80" are removed.
4. From the remaining filters, any that don't have "/docs" as a prefix of the **path** are removed.
5. From the remaining filters, the filter with the longest path prefix is selected and applied. If a filter isn't found, the selection process starts over again at step 1. The process is repeated with the next subdomain.

### Additional filter information

If a filter has a dot (".") prefixing the **host** then only exact **host** matches are filtered. For example:

- "contoso.com" (no dot) will match "contoso.com", "www.contoso.com", and "sub.www.contoso.com"
- ".www.contoso.com" (with a dot prefix) will only match "www.contoso.com"

You can use either a standard or custom **schema**. Supported standard schemas include:

- _about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_, and _wss_.

Any other **schema** is treated as a custom **schema**, but only the _schema:*_ and _schema://*_ patterns are allowed. For example:

- "custom:\*" or "custom://\*" will match "custom:app"
- "custom:app" or "custom://app" are invalid

**schema** and **host** aren't case-sensitive. For example:

- "http://contoso.com" filter matches "HTTP://contoso.com", "http://contoso.COM", and "http://contoso.com"

**path** and **query** are case-sensitive. For example:

- "http://contoso.com/path?query=A" filter doesn't match "http://contoso.com/Path?query=A" or "http://contoso.com/path?Query=A". It does match "http://contoso.COM/path?query=A".

## Content license

> [!NOTE]
> Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms 
  described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/). The original [Chromium page can be found here](https://www.chromium.org/administrators/url-blacklist-filter-format).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
