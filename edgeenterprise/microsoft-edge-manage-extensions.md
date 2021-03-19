---
title: "Manage Microsoft Edge extensions in the enterprise"
ms.author: aspoddar
author: dan-wesley
manager: balajek
ms.date: 03/19/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Manage Microsoft Edge extensions in the enterprise"
---

# Manage Microsoft Edge extensions in the enterprise

This article provides best practice guidance for admins who are managing Microsoft Edge extensions in their organizations. You can use the information in this article to develop a strategy for managing extensions in your organization.

> [!NOTE]
> This article applies to Microsoft Edge version 77 or later.

## Introduction

Organizations want to protect corporate and user data and evaluate browser extensions to ensure that they’re safe and relevant to their enterprise. Admins want to:

- Prevent bad apps and extensions from being installed.
- Keep extensions that users need to do their job.
- Manage access to user and company data.  

This article is the first in a series that that helps admins manage extensions to provide a safe and productive experience for their users. This series walks through the different options and helps you pick the best method for managing extensions. The series consists of the following articles:

- [Manage Microsoft Edge extensions in the enterprise](microsoft-edge-manage-extensions.md). Create a strategy to manage extensions and set up administrative templates required for managing the browser.
- [Use group policies to manage Microsoft Edge extensions](microsoft-edge-manage-extensions-policies.md). Options using group policies to manage extensions.
- [Create a web store to host Microsoft Edge extensions](microsoft-edge-manage-extensions-webstore.md). Create and host extensions.
- [FAQ for Microsoft Edge Extensions](microsoft-edge-manage-extensions-faq.md). Frequently Asked Questions.

## Things to consider when managing extensions

## Understand extension permissions

Extensions can require rights to make changes on a devices or a web page to run properly. These rights are called permissions. Developers must list what rights and access their extensions need. There are two main categories for permissions, and many extensions need both of the following permissions:

- Host permissions require the extension to list webpages it may view or modify.
- Device permissions are the rights needed by an extension on the device where it’s running.

Some examples of these permissions are: access to a USB port, storage or viewing screen. Communicating with native programs.  

## Get ready to manage extensions

Most organizations should manage extensions by their permissions and what websites they have access to. This method is more secure, easier to manage, and is scalable for large organizations.  

- Blocked/allowed permissions – Lets you control extensions by the permissions they need.
- Runtime block hosts – Lets you to control what websites these extensions can access.
- Force install extensions – Lets you install extensions silently.
- Allowlist/blocklist (if required) – Decide what extensions are allowed to be installed.

Using this approach saves time because you only need to set these once. And with the run-time hosts policy, your most important sites will be protected.

### Decide which extensions to allow

## See also

- [Use group policies to manage Microsoft Edge extensions](microsoft-edge-manage-extensions-policies.md)
- [Create a web store to host Microsoft Edge extensions](microsoft-edge-manage-extensions-webstore.md)
- [FAQ for Microsoft Edge Extensions](microsoft-edge-manage-extensions-faq.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)