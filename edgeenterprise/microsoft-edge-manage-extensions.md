---
title: "Manage Microsoft Edge extensions in the enterprise"
ms.author: aspoddar
author: dan-wesley
manager: balajek
ms.date: 04/07/2021
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

Your users need access to certain apps, sites, and extensions to do their jobs while at the same time protecting users and company data. An effective security strategy involves asking the right questions for your enterprise and how extensions can fit your company’s needs. Some of the key questions to ask are:

- What regulations and compliance measures do I need to adhere to?
- Do some extensions ask for overly broad permissions, which could go against my company’s data security policies?
- How much user or corporate data is stored on my users’ devices?

As you answer these questions, you can use the granular policies that Microsoft Edge provides to:

- Block or allow extensions on users’ computers based on your data protection policies.
- Force-install extensions on your users' devices so they have tools that they need to be productive.
- Allowlist or blocklist extensions to allow the least amount of rights needed for your users to do their  work.

The traditional model for managing extensions uses the allowlist and blocklist approach for specific extensions. However, Microsoft Edge also lets you manage the permissions requested by extensions. Using this model, you can decide which rights and permissions you want to allow extensions to use on your computers and devices, and then implement a global policy that allows or block extensions based on your requirements.  

## Understand extension permissions

Extensions can require rights to make changes on a device or a web page to run properly. These rights are called permissions. Developers must list what rights and access their extensions need. There are two main categories for permissions, and many extensions need both of the following permissions:

- Host permissions require the extension to list webpages it may view or modify.
- Device permissions are the rights needed by an extension on the device where it’s running.

Some examples of these permissions are: access to a USB port, storage or viewing screen, and communicating with native programs.  

## Get ready to manage extensions

Before you begin
The extensions options assume that you already have Microsoft Edge managed for your users. For more information about setting up administrative templates for Microsoft Edge policies, see:
•	Configure Microsoft Edge policy settings on Windows
•	Configure for Windows with Intune
•	Configure for Windows with Mobile Device Management
•	Configure for macOS using a .plist
•	Configure for macOS with Jamf
The configuration steps in this article are for Windows, for the corresponding implementation in MAC/Linux, see the Microsoft Edge browser policy reference.

## Decide which extensions to allow

Most organizations should manage extensions by their permissions and what websites they have access to. This method is more secure, easier to manage, and is scalable for large organizations.  

- Blocked/allowed permissions – Lets you control extensions by the permissions they need.
- Runtime block hosts – Lets you to control what websites these extensions can access.

Using this approach saves time because you only need to set these once. And with the run-time hosts policy, your most important sites will be protected.There are other options as well such as:
•	Force install extensions – Lets you install extensions silently.
•	Allowlist/blocklist (if required) – Decide what extensions are allowed to be installed.

Use the following steps as a guide to decide which extensions to allow in your organization.

1. Create a list of which extensions employees need on their computers. Test the extensions in a test environment to diagnose any compatibility issues with internal apps.
2. Choose which sites need to be more secure.

   - Find out which sensitive internal websites or domains you need to block extensions from making changes to or reading data from.  
   - Prevent access to these sites by blocking the API calls when the extension is run. This includes blocking web requests, reading cookies, JavaScript injection, XHR, and so on.

3. Determine which permissions are required for these extensions to run. Identify which permissions pose potential risks to your users.

   - Audit the extensions your users have installed and see what permissions they need. You can look at the web app manifest JSON file in the code of the extension. Take the following steps to see what rights the extension needs:

     - Install the extension from the [Microsoft Edge Add-ons](https://microsoftedge.microsoft.com/addons/) website or the [Chrome Web Store](https://chrome.google.com/webstore).
     - Test the extension and understand how it works in your organization.
     - Review the permissions that the extension requires by navigating to *edge://extensions*. For example, the Microsoft Office extension shown in the next screenshot requests the permissions "Read your browsing history" and "Display notifications". Weigh the usefulness of this extension against the level of permissions it requests. After you approve an extension for your organization, manage it using the following tools.
   :::image type="content" source="media/microsoft-edge-manage-extensions/manage-extesions-office-extension.png" alt-text="Microsoft Office extension with permissions.":::

   - You can also validate the extensions requested by users in your organization before approving them in the organization. Some of the permissions that extensions use can be vague. For business-critical apps, you can reach out to the app developer or vendor directly to get more information about the extension or look at the source code. They should be able to detail the changes that the extension can make on devices and websites.
   - Review the Declare Permissions list, which lists all permissions an extension can use. From this list, you can decide which permissions you want to allow in your organization.

4. Create a master list from the data you collected.This list will include the following information:

   - **Required extensions**. This list could be organized by department, office location, or other relevant information.
   - **Extension Allowlist**. Required extensions with permissions that may be blocked but will be allowed to run. These extensions are needed by your users or are determined to not be a risk through conversations with the vendor.
   - **Extension Blocklist**. Extensions that are blocked from installation. The extensions in this list have the permissions that aren’t allowed to run. Also include the core sites and domains to be kept secure and not allowed extension access. Later you can compare this blocklist to others you already have in place. You might find that you can relax your current blocklist policies.

5. Present your list to your stakeholders and the IT team to get buy in.
6. Test out the new policy in your lab or with a small pilot in your organization.
7. Roll out these new sets of policies to employees in phases. For more information, see [Use group policies to manage Microsoft Edge extensions](microsoft-edge-manage-extensions-policies.md).
8. Review feedback from your users.
9. Repeat and fine-tune the process monthly, quarterly, or yearly.

With your baseline of allowed permissions enforced and sensitive corporate sites protected, you can provide your enterprise with more security while providing a better experience for users. Staff might install extensions that they couldn't before, but not run them on sensitive business sites.  

## See also

- [Use group policies to manage Microsoft Edge extensions](microsoft-edge-manage-extensions-policies.md)
- [Create a web store to host Microsoft Edge extensions](microsoft-edge-manage-extensions-webstore.md)
- [Reference guide for the ExtensionSettings policy](microsoft-edge-manage-extensions-ref-guide.md)
- [FAQ for Microsoft Edge Extensions](microsoft-edge-manage-extensions-faq.md)
- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)