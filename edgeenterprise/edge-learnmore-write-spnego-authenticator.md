---
title: "Write SPNEGO Authenticator for Microsoft Edge on Android"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 09/14/2023
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "This article describes how to write a SPNEGO authenticator for Edge on Android"
---

#  Write a SPNEGO Authenticator for Microsoft Edge on Android

Third parties can enable SPNEGO authentication in Microsoft Edge for Android. To provide this authentication, they must provide a SPNEGO Authenticator. This article describes the interface between Edge and the SPNEGO Authenticator.

## Introduction

The SPNEGO Authenticator is provided by an Android Service. The authenticator must be incorporated in an app, provided by the third party, that's installed on the user's device. The app is responsible for managing any accounts used for SPNEGO authentication, and for all communication with the SPNEGO server.

The SPNEGO Authenticator is an Android AccountAuthenticator. As such it must follow the pattern described in [AbstractAccountAuthenticator](https://developer.android.com/reference/android/accounts/AbstractAccountAuthenticator#getAuthToken(android.accounts.AccountAuthenticatorResponse,%20android.accounts.Account,%20java.lang.String,%20android.os.Bundle)). It must implement an authenticator class derived from `AbstractAccountAuthenticator`.

The SPNEGO Authenticator must define a new account type. The account type name should be derived from the writer's domain name (for example, com.example.spnego). The account type must be defined to use [customTokens](https://developer.android.com/reference/android/R.attr#customTokens) and must support the "SPNEGO" feature (HttpNegotiateConstants.SPNEGO_FEATURE).

## Interface to Microsoft Edge

Edge finds the SPNEGO authenticator through the Android account type it provides. The account type that's defined by the authenticator is passed to Edge through the **AuthAndroidNegotiateAccountType** policy.

The interface to Edge is through the Android account management framework, through [AbstractAccountManager.getAuthToken](https://developer.android.com/reference/android/accounts/AbstractAccountAuthenticator.html#getAuthToken(android.accounts.AccountAuthenticatorResponse,%20android.accounts.Account,%20java.lang.String,%20android.os.Bundle)) in particular. Edge, in [org.chromium.net.HttpNegotiateConstants](https://source.chromium.org/chromium/chromium/src/+/main:net/android/java/src/org/chromium/net/HttpNegotiateConstants.java), defines some more keys and values that are used in the arguments to `getAuthToken`, and in the returned result bundle.

### getAuthToken arguments

When [getAuthToken](https://developer.android.com/reference/android/accounts/AbstractAccountAuthenticator#getAuthToken(android.accounts.AccountAuthenticatorResponse,%20android.accounts.Account,%20java.lang.String,%20android.os.Bundle)) is called, the `authTokenType` is "SPNEGO:HOSTBASED:\<spn\>" where \<spn\> is the principal for the request. This will always be a host-based principal in the current implementation. Future versions may allow other types of principals, but if they do so they'll use a different prefix. SPNEGO Authenticators should check the prefix.

The `options` bundle will contain these keys:

- [KEY_CALLER_PID](http://developer.android.com/reference/android/accounts/AccountManager.html#KEY_CALLER_PID)
- [KEY_CALLER_UID](http://developer.android.com/reference/android/accounts/AccountManager.html#KEY_CALLER_UID)
- `HttpNegotiateConstants.KEY_CAN_DELEGATE` - True if delegation is allowed, false if not allowed.

If this is the second or later round of a multi-round authentication sequence it will also contain the following keys.

- `HttpNegotiateConstants.KEY_INCOMING_AUTH_TOKEN` - The incoming token from the WWW-Authenticate header, Base64 encoded.
- `HttpNegotiateConstants.KEY_SPNEGO_CONTEXT` - The SPNEGO context provided by the authenticator on the previous round. This is a bundle that Edge treats this as an opaque object and simply preserves it between rounds.

### getAuthToken result bundle

The final result bundle of [getAuthToken](https://developer.android.com/reference/android/accounts/AbstractAccountAuthenticator#getAuthToken(android.accounts.AccountAuthenticatorResponse,%20android.accounts.Account,%20java.lang.String,%20android.os.Bundle))
 (returned either as the return value of `getAuthToken`, or through the [AccountAuthenticatorResponse](https://developer.android.com/reference/android/accounts/AccountAuthenticatorResponse.html)) should contain the account name, account type, and token as defined in the Android documentation. In addition, the bundle should contain these keys:

- `HttpNegotiateConstants.KEY_SPNEGO_RESULT` - the SPNEGO result code. This should be one of the values defined in [HttpNegotiateConstants](https://source.chromium.org/chromium/chromium/src/+/main:net/android/java/src/org/chromium/net/HttpNegotiateConstants.java).
- `HttpNegotiateConstants.KEY_SPNEGO_CONTEXT` - a context to be returned to the authenticator in the next authentication round. This is only required if authentication is incomplete.

## Implementation recommendations

The following recommendations should be considered when implementing a SPNEGO authenticator.

- Each account provided by an SPNEGO Account Authenticator should correspond to a single user principal (account) provided by a single key distribution center.
- The account authenticator shouldn't store any passwords. Instead, it should store TGTs for the user principals and require the users to re-enter their passwords (or other authentication data) when their TGT expires.
- The account authenticator should keep a list of authorized applications (or application signatures) for each account and refuse to provide service tokens to other applications. The list of authorized applications can be:

  - Built into the account authenticator.
  - Configurable by the system administrator.
  - Configurable by the user. In this case the account authenticator might choose to allow the user to authorize new applications dynamically when they first request access.

  The authenticator can get the uid of the calling app using the KEY_CALLER_UID field of the options bundle, and then identify the requesting application using `context.getPackageManager().getNameForUid()` or similar call.

  This is required to ensure that malicious apps run by the user can't use the user's credentials to access services in unintended ways. This is particularly important since using the custom tokens option (as described above) disables Android's own signature check when getting auth tokens.

- Unless it's built into the account authenticator, the system administrator or user will need to be able to configure the location of the key distribution center.

## Error codes displayed in Microsoft Edge

In addition to the error codes that can be forwarded from the authenticator app, the following errors can be displayed when trying to authenticate a request:

- ERR_MISSING_AUTH_CREDENTIALS: The account information is not usable. It can be raised for example if the user did not log in to the authenticator app and no eligible account is found, if the account information can't be obtained because the current app does not have the required permissions, or if there's more than one eligible account and we can't obtain a selection from the user.
- ERR_UNEXPECTED: An unexpected error happened, and the request has been terminated.
- ERR_MISCONFIGURED_AUTH_ENVIRONMENT: The authentication can't be completed because of some issues in the configuration of the app. Some permissions may be missing.

Use [Logcat](https://developer.android.com/tools/logcat#SnippetTab) to search for the **cr_net_auth** tag in the system log to get more information about the cause of these errors.

## Use and test the authenticator with Microsoft Edge

Edge uses several [policies for controlling the use of SPNEGO authentication](/deployedge/microsoft-edge-mobile-policies#http-authentication). To enable SPNEGO authentication the [AuthServerAllowList](/deployedge/microsoft-edge-mobile-policies#authserverallowlist) must be configured and the [AuthAndroidNegotiateAccountType](/deployedge/microsoft-edge-mobile-policies#authandroidnegotiateaccounttype) must match the account type provided by the SPNEGO authenticator.

## Content license

> [!NOTE]
> Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms 
  described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/). The original page can be found [here](https://sites.google.com/a/chromium.org/dev/developers/design-documents/http-authentication/writing-a-spnego-authenticator-for-chrome-on-android).
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)