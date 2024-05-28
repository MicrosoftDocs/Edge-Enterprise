---
title: "Microsoft Edge known issues"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 05/28/2024
audience: ITPro
ms.topic: conceptual
ms.service: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Microsoft Edge known issues, workarounds, and fixes"
---

# Microsoft Edge known issues

This article tracks the known issues, workarounds, and fixes for Microsoft Edge.

## High impact issues

These issues are high impact as identified by CSS. Check this article often as the Microsoft Edge team provides workarounds and fixes.

The following table lists the issues that the Microsoft Edge team is tracking closely, working on, or have resolved.
<!-----------
##### [latest](#tab/latest)
----->
| Channel |  Version  | Symptom | Workaround | Comment |
| --- | --- | --- | --- | --- |
|     | 124    |  Specific HTTPS websites are no longer accessible, with the error:<br>ERR_CONNECTION_ABORTED or ERR_SSL_PROTOCOL_ERROR.<br>This error may also occur when fetching resources on the page, causing display or delay issues.<br><br>This is caused by the feature "TLS 1.3 hybridized Kyber support", which had been enabled by default through Chromium.  | To verify if the issue is related the Kyber key encapsulation in TLS, you can disable the feature through its flag in `edge://flags/#enable-tls13-kyber`.<br><br>Enterprise administrators who need more time to update their certificates can set the **PostQuantumKeyAgreementEnabled** enterprise policy as a temporary workaround. Note that:<br>- This  is a temporary measure that will be removed in future versions of Microsoft Edge.<br>- Disabling this policy means that user traffic will be unprotected from decryption by quantum computers.<br>The registry-key for the  policy is:<br>[HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Edge] <br>(DWORD) "PostQuantumKeyAgreementEnabled"=0 |     |
|     | 121    |  Specific HTTPS websites are no longer accessible, with the error:<br>ERR_SSL_KEY_USAGE_INCOMPATIBLE<br><br>This is caused by enforcing X.509 key usage extensions for RSA keys in TLS 1.2 and earlier versions in Chromium.  |  Enterprise administrators who need more time to update their certificates can set the **RSAKeyUsageForLocalAnchorsEnabled enterprise** policy as a temporary workaround. This policy had been temporarily available for administrators who needed more time to update their certificates to meet the new RSA key usage requirements. Note that this policy is removed in Microsoft Edge version 124 and later.<br>The registry-key for the policy is:<br>[HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Edge]<br>(DWORD)RSAKeyUsageForLocalAnchorsEnabled"=0 |      |
|     | 120    |  When starting Microsoft Edge with an external HTTP-URL (for example,  `http://www.example.com`), Edge opens the page directly with HTTPS, in case the server has also enabled HTTPS. The same thing happens if you follow a hyperlink like this `http://www.example.com` in a new tab.<br><br>This change in behavior is due to the feature "HttpsDefault", which had been enabled by default through Chromium.   | With Microsoft Edge 120.0.2210.89, the policy **AutomaticHttpsDefault** can be used to disable the automatic switch from HTTP to HTTPS.<br>If you need to turn off the automatic switch from HTTP to HTTPS, deploy this policy:<br>"Configure Automatic HTTPS" -> "Automatic HTTPS functionality is disabled." (value 0)<br>The registry-key for the policy is:<br>[HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Edge]<br>(DWORD) "AutomaticHttpsDefault"=0<br><br>In a scenario where you only want to disable the automatic switch for specific websites, you can use the policy **InsecureContentAllowedForUrls** to configure these sites. |     |
|     | 119    |  Specific HTTPS websites are no longer accessible, with the error: ERR_SSL_PROTOCOL_ERROR.<br><br>This is caused by removing support for signature algorithms using SHA-1 for server signatures during the TLS handshake in Chromium. | Enterprise administrators who need more time can set the **InsecureHashesInTLSHandshakesEnabled** enterprise policy as a temporary workaround.  Note that:<br>- This is a temporary policy that is removed in Microsoft Edge version 124 and later.<br>- Because this allows an insecure hash function in a critical part of the TLS handshake, enabling this policy increases the risk of attackers impersonating servers in an enterprise deployment.<br>The registry-key for the policy is:<br>[HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Edge]<br>(DWORD) "InsecureHashesInTLSHandshakesEnabled"=1 |  |

<!------
##### [earlier](#tab/earlier)

| Channel |  Version  | Symptom | Workaround | Comment |
| --- | --- | --- | --- | --- |

---->

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
