---
title: "Password Monitor auto-enabled for users"
ms.author: supalsul
author: dan-wesley
manager: tulasim
ms.date: 08/21/2023
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Password Monitor auto-enabled for users"
---

# Password Monitor auto-enabled for users

> [!NOTE]
> Microsoft Edge for Business is now available in Edge stable version 116! [Learn more](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/microsoft-edge-for-business-faq/ba-p/3891837) about the new, dedicated work experience with native enterprise grade security, productivity, manageability, and AI built in.

This article describes how admins can turn on Password Monitor in Microsoft Edge for select users. The article also gives the steps to control how monitoring is enabled.

> [!NOTE]
> This article applies to Microsoft Edge version 88 or later.

## Introduction, benefits, and availability

Password Monitor helps Microsoft Edge users protect their online accounts by informing them if any of their passwords have been found in an online leak. Online leaks or data breaches happen when bad actors steal data from third-party apps or websites. To learn more, see the [Password Monitor: Safeguarding passwords in Microsoft Edge](https://www.microsoft.com/research/blog/password-monitor-safeguarding-passwords-in-microsoft-edge/)  paper on the Microsoft Research Blog.

### Benefits

Given the frequency and scope of these online attacks having this kind of protection has become necessary for everyone. Microsoft Edge has the built-in ability to securely check a user's saved passwords against passwords that are known to be compromised and alerts them if a match is found.  

## Configure group policy for Password Monitor

This feature is controlled via the [PasswordMonitorAllowed](./microsoft-edge-policies.md#passwordmonitorallowed) group policy.

After the policy is enabled, users still need to provide consent to turn on the feature. Consent is required because the feature contains user's sensitive and personal data (passwords). If the feature is disabled using group policy, users can't override this setting.  

## Enabling Password Monitor for users

After the password monitor policy is enabled, there are different ways this feature is made available to users.

- Auto-enablement. Users that are signed-in using their work account (Active Directory or Microsoft Entra ID) and syncing their passwords are auto-enabled for this feature. They'll see the notification in the next screenshot informing them that the feature's turned on.

  :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-enabled-notice.png" alt-text="Password Monitor enabled notice":::

-  Getting explicit consent. Users that don't have Password Sync turned on are asked for permission to turn on Password Monitor. They're prompted when the following actions happen:
   - When a user is saving a new password.
 
     :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-save-pw-prompt.png" alt-text="Prompt to save password":::

   - When a user has signed-in to the browser using a saved password.
  
     :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-after-signin.png" alt-text="Confirmation prompt after sign-in":::
   
- Direct activation. Users can go to **Settings** > **Passwords** anytime and turn the feature On or Off.

## User scenarios with Password Monitor auto-enabled

The following table shows scenarios where Password Monitor is auto-enabled and how it works on user devices.

| Scenario | Base conditions | Impact |
|--|--|--|
| 1 with Sync on | Sync ON<br>Feature enabled previously: No<br>Response to Consent UI: None | Feature enabled by default and a notice bubble is shown 2 min after browser starts.<br>- If sync is turned off after that, the feature is disabled.<br>-  Feature turned off before altering sync, sync no longer affects the feature.   |
| 2 with Sync on | Sync ON<br>Feature enabled previously: Yes<br>Response to Consent UI: None | Feature stays the same as user choice.  Notice bubble isn't shown and there's no affect of sync change on feature value.|
| 3 with Sync off | Sync Off<br>Feature enabled previously: No<br>Response to Consent UI: None | Sync is off and the feature stays disabled<br>- At any point after that if user turns on the sync without altering the feature: the feature is enabled and auto-enablement notification is shown 2 minutes after Sync is turned on. <br> - If sync is turned off again, the  feature is disabled <br>- If the feature is changed before turning on sync, sync no longer affects Password Monitor.  |  
| 4 with Sync off | Sync OFF<br>Feature enabled previously: Yes<br>Response to Consent UI: None | Feature stays the same as user choice, notice bubble isn't shown, and there's no effect of sync change on the feature value.  |

In addition, if a user is signed-in using a work account that's restricted via policies for any of the following, the feature is NOT auto-enabled for them:

- Password Monitor is disabled  
- Password Sync is disabled
- Sharing of data with Microsoft servers is disabled

## Frequently Asked Questions

### How can Password Monitor be disabled for my organization?

You can disable Password Monitor for your organization by:
- Using the [PasswordMonitorAllowed](/deployedge/microsoft-edge-policies#passwordmonitorallowed) group policy.
- Stopping data from being synchronized and sent to Microsoft servers.

  > [!NOTE]
  > Password Monitor can work even if Password Sync is disabled, as long as the user has given explicit consent to turn the feature On or have turned it on themselves via Settings.

### What happens if a user for whom the feature has been auto-enabled, turns Password Monitor off via Settings?

The user setting is honored and the feature remains disabled for that user. However, they might be shown a consent dialog again in case they've never previously responded to the consent prompt.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)