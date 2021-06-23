---
title: "Microsoft Edge password manager security "
ms.author: v-andreabarr
author: AndreaLBarr
manager: collw
ms.date: 05/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Microsoft Edge password manager security"
---
# Microsoft Edge password manager security 

The frequently asked questions in this article describe how Microsoft Edge's built-in password manager provides security for user passwords.

> [!Note]
>This article applies to Microsoft Edge version 77 or later.

## How are passwords stored in Microsoft Edge and how safe is this approach?

Microsoft Edge stores passwords encrypted on disk. They're encrypted using AES256 and the encryption key is saved in an operating system (OS) storage area. This technique is called local data encryption. Although not all of the browser’s data is encrypted, sensitive data such as passwords, credit card numbers, and cookies are encrypted when they are saved.

The Microsoft Edge password manager encrypts passwords so they can only be accessed when a user is logged on to the operating system. Even if an attacker has admin rights or offline access and can get to the locally stored data, the system is designed to prevent the attacker from getting the plaintext passwords of a user who isn't logged in.

The way to decrypt another user's passwords is if that user were logged on and the attacker had the user’s password or has compromised the domain controller.

### About the encryption method

The profile’s encryption key is protected using Chromium's OSCrypt and uses the following platform-specific OS storage locations:

- On Windows, the storage area is DPAPI

- On Mac, the storage area is the Keychain

- On Linux, the storage area is Gnome Keyring or KWallet

All these storage areas encrypt the AES256 key using a key accessible to some or all processes running as the user. This attack vector is often featured in blogs as a possible 'exploit' or 'vulnerability', which is an incorrect understanding of the browser threat model and security posture.

However, physically local attacks and malware are outside the threat model and, under these conditions, encrypted data would be vulnerable. If your computer's infected with malware, an attacker can get decrypted access to the browser's storage areas. The attacker's code, running as your user account, can do anything you can do.

## Why encrypt data locally? Why not store the encryption key elsewhere, or make it harder to obtain?

Internet browsers (including Microsoft Edge) aren’t equipped with defenses to protect against threats where the entire device is compromised due to malware running as the user on the computer. However, programs like Microsoft Defender SmartScreen and OS-level protections like Windows Defender are designed to ensure that the device isn't compromised to start with.

Despite its inability to protect against full-trust malware, Local Data Encryption is useful in certain scenarios. For example, if an attacker finds a way to steal files from the disk without the ability to execute code or has stolen a laptop that isn’t protected with Full Disk Encryption, Local Data Encryption will make it harder for the thief to get the stored data.

## Do you recommend storing passwords in Microsoft Edge?

Users who can rely on the Microsoft Edge's in-built password manager can (and do) use stronger and unique passwords more because they don’t need to remember them all and type them as often. And because the password manager will only autofill passwords on the sites to which they belong, users are less likely to fall for a phishing attack.

> [!Note]
>Industry reports show that 80% of online incidents are related to phishing, and more than 37% of untrained users fail phishing tests.

Microsoft Edge’s password manager is convenient and easily distributed, which contributes to improved security. When combined with sync, you can get all your passwords on all your devices and it's easy to use a different password for every website. You can use long and complex passwords that you don't have to remember for every site and skip the hassle of typing a complex string every single time. Password manager's convenience means there's less risk of falling for a phishing attack.

However, using a password manager that's keyed to the user’s operating system login session also means that an attacker in that session can immediately retrieve all the user’s saved passwords. Without a password manager to steal from, an adversary would need to track keystrokes or monitor submitted passwords.

The decision of whether to use a password manager comes down to assessing the many benefits we’ve described against the possibility of the entire device getting compromised. For most threat models, using the Microsoft Edge password manager is the recommended option.

> [!Note]
>If an enterprise is concerned about theft of a specific password or a site getting compromised because of a stolen password, additional precautions should be taken. Some effective solutions that help mitigate this kind of incident is Single Sign On (SSO) via Active Directory, Azure Active Directory, or a third party. Other solutions include 2FA (such as [MS Authenticator](/azure/active-directory/user-help/user-help-auth-app-download-install)) or [WebAuthN](https://webauthn.guide/).

## Should a password manager be enabled by an organization?

The simple and easy answer is: Yes, use the browser’s password manager.

A more complete response means having in-depth knowledge of your threat model because security options and choices vary depending on different threat models. Some relevant questions to consider when thinking about whether you should enable the password manager for your organization are:

- What kind of attackers are you worried about?

- What kind of websites do your users log on to?

- Do your users select strong, unique passwords?

- Are your users’ accounts protected with 2FA?

- What kind of attacks are most likely?

- How do you protect your enterprise devices from malware?

- What’s your users’ personal tolerance for inconvenience?

- Consider the impact of data sync.

It’s important to factor in the security of user data as it gets synced to various user devices and the amount of control the organization has on autofill data syncing.

Data syncing and Microsoft Edge:

- Data syncing can be enabled or disabled as desired across the organization.

- Data security in transit and at rest in the cloud: All synced data is encrypted in transit over HTTPS when transferred between the browser and Microsoft servers. The synced data is also stored in an encrypted state on Microsoft servers. Sensitive data types such as addresses, and passwords are further encrypted on the device before being synced. If you're using a work or school account, all data types are further encrypted before being synced using Microsoft Information Protection.

## Why do Microsoft security baselines recommend disabling the password manager?

The Microsoft security team has currently rated the impact of a worm that compromises a network of Enterprise PCS (resulting in loss of all credentials in all devices’ password managers) as more severe than the (more likely but lower impact) risk of targeted phishing attacks that compromise a single user-entered credential.

This assessment is under discussion and subject to change with the addition of new security-enhancing features in Microsoft Edge.

## Can malicious extensions gain access to passwords?

An extension with permission to interact with a page is inherently able to access anything from that page, including an auto filled password. Similarly, a malicious extension can modify the contents of form fields and network requests/responses to misuse the authority of the current user login context.

However, Microsoft Edge provides an extensive set of policies that enable fine control over installed extensions. Using the policies in the following table is necessary to protect corporate data.

| Policy | Caption |
|-|-|
|[BlockExternalExtensions](/deployedge/microsoft-edge-policies#blockexternalextensions)|Blocks external extensions from being installed|
|[ExtensionAllowedTypes](/deployedge/microsoft-edge-policies#extensionallowedtypes)|Configure allowed extension types|
|[ExtensionInstallAllowlist](/deployedge/microsoft-edge-policies#extensioninstallallowlist)|Allow specific extensions to be installed|
|[ExtensionInstallBlocklist](/deployedge/microsoft-edge-policies#extensioninstallblocklist)|Control which extensions cannot be installed|
|[ExtensionInstallForcelist](/deployedge/microsoft-edge-policies#extensioninstallforcelist)|Control which extensions are installed silently|
|[ExtensionInstallSources](/deployedge/microsoft-edge-policies#extensioninstallsources)|Configure extension and user script install sources|
| [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) |Configure extension management settings |

## How does the Microsoft Edge password manager compare with a third-party product?

The following table shows how Microsoft Edge password manager compares to third-party password managers.

| Third-party password manager | Microsoft Edge password manager|
|-|-|
| *Server sync*. Some products store passwords in the cloud to sync all your devices. This feature is helpful, but there's a risk if the cloud service gets compromised and your data is exposed. **Remarks:** The risk is mitigated by having passwords encrypted in the cloud and storing the encryption key on your device(s) so attackers can't get to the key and your passwords.| There's a cloud exposure risk because passwords are synced across Windows devices that have Microsoft Edge installed. **Remarks:** This risk is mitigated by the data security steps covered in this article.|
| *Trust*. It's necessary to trust that the third party isn't doing anything malicious, such as sending your passwords to another party. **Remarks:** This risk can be mitigated by reviewing the source code (in the case of open-source products), or by believing that the vendor cares about their reputation and revenue. | **Remarks:** Microsoft is a known and trusted vendor with decades of history in providing enterprise-grade security and productivity, with resources designed to protect your passwords worldwide. |
| *Supply chain security*. It's hard to verify that the vendor has secure supply chain/build/release processes for the source code. |**Remarks:** Microsoft has robust internal processes to ensure minimal risk to source code. |
| *Compromised client or account*. If a client device or user account is compromised, an attacker can get the passwords. **Remarks:** This risk is mitigated for some password managers that require the user to enter a Master Password that's not stored locally to decrypt the passwords. A Master Password is only partial mitigation because an attacker could read keystrokes and get the master password as it's typed or read passwords from process memory when filling in a form field. | **Remarks:** Microsoft offers OS-level protections like Windows Defender, designed to ensure that the device isn't compromised to start with. However, if a client device is compromised, an attacker may be able to decrypt the passwords. |

> [!Note]
> Third-party products might provide protection against additional threat models, but this is at the expense of complexity or ease-of-use. The Microsoft Edge password manager is designed to provide convenient and easy-to-use password management that can be fully controlled by IT Admins using Group Policy and doesn’t require trusting a third party.

## Why doesn't Microsoft offer a Master Password to protect the data?

When browser passwords are encrypted on disk, the encryption key is available to any process on your device, which includes any locally running malware. Even if passwords are encrypted in a "vault" by a master key, they’ll be decrypted when loaded in the browser’s memory space and can be harvested after you unlock the vault.

A Master Password feature (that authenticates the user before auto-filling their data) provides a trade-off in convenience for broader threat mitigation. Specifically, it helps to reduce the window of data exposure against latent malware or physically local attackers. However, a Master Password is not a panacea, and local attackers and dedicated malware have various strategies for circumventing the protection of a Master Password.

> [!Note]
> Microsoft recognizes the value in authenticating users before autofill and this functionality will be added to Microsoft Edge in a future release.

## Can using a password manager impact my privacy?

No, not if steps are taken to protect access to your saved passwords.

There’s a known exploit that some advertisers use, which uses stored passwords to uniquely identify and track users. For more information, see [Ad targeters are pulling data from your browser’s password manager](https://www.theverge.com/2017/12/30/16829804/browser-password-manager-adthink-princeton-research). Browsers have taken steps to mitigate this [privacy issue](https://bugs.chromium.org/p/chromium/issues/detail?id=798492). The PasswordValueGatekeeper class can be used to limit access to the password field data, even when the browser is configured to autofill when it loads.

This user information harvesting threat can be easily mitigated by enabling the optional  edge://flags/#fill-on-account-select feature. This feature only allows passwords to be added to a form field after the user explicitly chooses a credential, which ensures that users stay aware of who is receiving their passwords.

## See also

[Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download)

[How Microsoft Edge is more secure than Chrome for business on Windows 10](/DeployEdge/ms-edge-security-for-business)
