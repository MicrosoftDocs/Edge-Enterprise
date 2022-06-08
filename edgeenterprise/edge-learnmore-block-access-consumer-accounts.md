---
title: "Block access to consumer accounts"
ms.author: v-danwesley
author: dan-wesley
manager: collw
ms.date: 06/08/2022
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Block access to consumer accounts"
---

# Block access to consumer accounts

You can prevent users from signing into Google services using any accounts other than the accounts you provided them with. Reasons for blocking access are to prevent users on your corporate network using their personal Gmail accounts, or accessing a managed Google account from another domain.

Users might see the following message when you block access to consumer accounts:
"This account is not allowed to sign in within this network".

> [!NOTE]
> This article applies to Microsoft Edge Stable version 104 or later.

## Allow access only from specific domains

The following steps describe how to allow users to access Google services with an account that’s in a list for specified Google Workspace domains.

1. Sign in to your Google Admin console with your administrator account.
2. From the Admin console Home page, go to **Devices**.
3. Select **Chrome** > **Settings** > **Users & browsers**.
4. Leave the top organizational unit selected if you want to apply the setting to everyone. Otherwise, pick a child organizational unit.
5. Go to **User experience** > **Sign-in to secondary accounts**.
6. Select **Allow users to only sign in to the domains below**.
7. Enter your organization’s domains. If you don’t, your users might not have access to Google services.

   > [!NOTE]
   > gserviceaccounts.com is included and critical for authenticated service accounts.

8. (Optional) To include consumer Google Accounts, such as those ending in @gmail.com and @googlemail.com, add **consumer_accounts** to the domain list.
9. Select **Save**. Settings usually take effect in minutes, but they might take up to an hour to apply to everyone.

### Optional next steps

Use the Google Admin console to add the following restrictions:

- Prevent users from browsing in Incognito mode. 
- Set a sign-in restriction so only users in your organization can sign in to devices running Chrome OS.
- Turn off guest browsing on devices.

## Use a web proxy server to block accounts

Use the following steps as a guide to set up a proxy server to block accounts. First, you have to pick a web proxy server, then use it to configure your network.

### Choose a web proxy server

Choose a web proxy server that you can configure to only allow users on your network to access Google services using specific Google Accounts from your domain. With this server you must be able to:

- **Add a header to all traffic directed to google.com.** Use this header to identify the domains from which users can access Google services.
- **Support SSL interception.** Because most traffic through your Google service is encrypted, your proxy server needs to support SSL interception.

Read specific instructions on how to block Google services from the following proxy service providers. Select a server that meets your needs.

- [Barracuda Networks](https://campus.barracuda.com/product/websecuritygateway/doc/17106182/g-suite-control-over-https)
- [Symantec](https://knowledge.broadcom.com/external/article?legacyId=TECH241152)
- [McAfee](https://docs.trellix.com/search?q=proxy%20server)
- [Forcepoint](https://www.websense.com/content/support/library/web/v85/wcg_help/gmail_add_hdr_rule.aspx )

### Configure the network to block accounts

Use the following steps to prevent users from signing in to Google services using Google Accounts other than the accounts you explicitly specify.

1. Route all  outbound traffic to google.com through your web proxy servers.
2. Enable SSL interception on the proxy server.
3. Configure every client device to trust your SSL proxy by:

   - Deploying the Internal Root Certificate Authority used by the proxy
   - Marking it as trusted

4. For each google.com request:

   - Intercept the request.
   - Add the HTTP header **X-GoogApps-Allowed-Domains:** followed by a comma-separated list with the allowed domain names.

      > [!IMPORTANT]
      > Make sure the list includes the domain you registered with Google Workspace and any secondary domains you added.
      > Example: `X-GoogApps-Allowed-Domains: mydomain1.com, mydomain2.com`

5. To let users sign in to specific accounts, add the following values to the header:

   - **domain_name** for accounts on specific domains, such as altostrat.com and tenorstrat.com for accounts ending in @altostrat.com and tenorstrat.com
   - **consumer_accounts** for consumer Google Accounts, such as @gmail.com and @googlemail.com
   - **gserviceaccounts.com** for authenticated service accounts

6. (Optional, but recommended) Create a proxy policy to prevent users from inserting their own headers.

> [!NOTE]
> - This proxy configuration blocks sign-in access to Google consumer services other than Google Search, but doesn’t necessarily prevent anonymous access.<br>
> - When you add the X-GoogApps-Allowed-Domains HTTP header, users will see errors accessing delegated mailboxes from a domain that's not in the header.

## Content license

> [!NOTE]
> Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/). The original page can be found [here](https://developer.chrome.com/blog/immutable-document-domain/).

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
