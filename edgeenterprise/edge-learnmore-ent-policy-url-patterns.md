---
title: "URL pattern format for Microsoft Edge Enterprise policies"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 04/29/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Learn about the URL pattern format used for Microsoft Edge Enterprise policies."
---

# Enterprise policy URL pattern format

Multiple policies require a URL pattern to specify to which URLs they apply. The following rules describe the specification for these patterns.

## Valid pattern specifications

Valid pattern specifications are of one of the following forms (without the quotes):

- "*"
  - This pattern matches any URL, with any scheme, port, and path.

- **"scheme://domains:port/path"**
  - The supported schemes are "http" and "https".
  - The scheme can be left out, along with the scheme separator "://" to match any scheme. Alternatively, a wildcard "*" can be used to the same effect.
  - The domain is followed by a top-level domain, prefixed by one or more subdomains. Alternatively, a host (such as localhost) can be used instead.
    - A domain is prefixed by a wildcard "[\*.]" to match the domain or any of its subdomains. The domain in question can be a subdomain of any level. The wildcard "[\*.]" isn't followed by a dot and should be prefixed directly to the domain/subdomain.
    - A domain without the wildcard prefix only matches that exact domain and not any subdomains.
  - The port is a number in the range 0-65535. It can be left out along with the port separator ":" or replaced by a wildcard "*" to match any port.
  - Similarly, the path can be left out along with the part separator "/" or replaced by a wildcard "*" to match any path.
  - Wildcards can't be used for partially matching a scheme, domain, host, port, or path.
  - Using multiple wildcards in the same pattern (for example *://google.com:*/*) is supported.

- **"scheme://a.b.c.d:port/path"**
  - Instead of a domain, an IPv4 address in the form "a.b.c.d" can be used. While the rules for schemes, ports and paths remain the same as for domain URLs, wildcards can't be used at all for IP addresses.

- **"scheme://[a:b:c:d:e:f:g:h]:port/path"**
  - An IPv6 address can also be used in the form "[a:b:c:d:e:f:g:h]". The brackets are mandatory. Just like with IPv4 addresses, wildcards aren't supported. Rules for schemes, ports, and paths remain the same as for domain URLs and IPv4 addresses.

- **"file://path"**
  - If the "file" scheme is used, the path has to start with a "/", therefore "file://dir/myfile.html" is an invalid pattern. "file:///dir/myfile.html" (with three forward slashes after "file:") needs to be used instead. The only valid file URL wildcard format is "file:///*", which matches any valid file URL.
  - The domain part of a file URL needs to be empty, and matches any domain (or localhost). For example, "file:///file.html" matches "file://localhost/file.html" and "file://mysite.com/file.html".
  - Ports can't be used.

## Invalid patterns

The following patterns are invalid.

- [*.].mysite.com is invalid (notice the dot before "mysite").
- file://mysite.com/somefile.html is invalid as the domain is nonempty (not allowed in file URLs).
- file://somefile.html is invalid (only two forward slashes instead of three).
- file://somefile.*. (the only valid file URL that contains a wildcard is file:///*).
- [*.]127.0.0.1 is invalid (using subdomains or subdomain wildcards with IP addresses is invalid).

## Pattern examples

Some examples of patterns are:

- [*.]mysite.com matches both mysite.com and subdomain.mysite.com. It also matches any scheme, port, and path.
- [*.]ontoso.com doesn't match contoso.com. However, it does match subdomain.ontoso.com.
- file:///foo/bar.html matches file://localhost/foo/bar.html and file://mysite.com/foo/bar.html.
- file:///* is valid and matches any file:// URL.
- Schemes, ports, and paths can be used with IP addresses, for example https://[::1]:8080/myfile.html is valid.

## Content license

> [!NOTE]
> Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms 
  described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/). The original [Chromium page can be found here](https://chromeenterprise.google/policies/url-patterns/).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
