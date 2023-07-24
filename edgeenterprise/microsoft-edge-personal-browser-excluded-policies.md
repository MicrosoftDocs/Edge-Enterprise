---
title: "Policies that aren't applied to an Enterprise personal browser profile"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 07/24/2023
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Policies excluded from the Enterprise personal browser profile"
---

# Policies that aren't applied to an Enterprise personal browser profile

The following policies aren't applied to the personal browser profile.

## Policy table

| Policy Name | Caption |
|:-|:-|
| AdditionalDnsQueryTypesEnabled   |    |
| [AllowCrossOriginAuthPrompt](/deployedge/microsoft-edge-policies#allowcrossoriginauthprompt)|Allow cross-origin HTTP Authentication prompts  | List of origins that allow all HTTP authentication   |
|[AllowFileSelectionDialogs](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-policies#allowfileselectiondialogs)|Allow file selection dialogs|
|[AllowTokenBindingForUrls](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-policies#allowtokenbindingforurls)|Configure the list of sites for which Microsoft Edge will attempt to establish a Token Binding with|
|[AmbientAuthenticationInPrivateModesEnabled](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled)|Enable Ambient Authentication for InPrivate and Guest profiles|
| [ApplicationGuardContainerProxy](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-policies#applicationguardcontainerproxy) | Application Guard Container Proxy   |
| [ApplicationGuardFavoritesSyncEnabled](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-policies#applicationguardfavoritessyncenabled)   | Application Guard Favorites Sync Enabled  |
| [ApplicationGuardPassiveModeEnabled](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-policies#applicationguardpassivemodeenabled) |   Ignore Application Guard site list configuration and browse Edge normally  |
| [ApplicationGuardTrafficIdentificationEnabled](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-policies#applicationguardtrafficidentificationenabled)   | Application Guard Traffic Identification   |
|  [ApplicationGuardUploadBlockingEnabled](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-policies#applicationguarduploadblockingenabled)  |  Prevents files from being uploaded while in Application Guard   |
|[ApplicationLocaleValue](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-policies#applicationlocalevalue)| Set application locale |
| [AuthNegotiateDelegateAllowlist](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-policies#authnegotiatedelegateallowlist) |  Specifies a list of servers that Microsoft Edge can delegate user credentials to |
| [AuthSchemes](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-policies#authschemes) |  Supported authentication schemes |
| [AuthServerAllowlist](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-policies#authserverallowlist)| Configure list of allowed authentication servers |
|[AutoImportAtFirstRun](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-policies#autoimportatfirstrun) | Automatically import another browser's data and settings at first run  |
|[BackgroundModeEnabled](#backgroundmodeenabled)|Continue running background apps after Microsoft Edge closes|
|[BasicAuthOverHttpEnabled](#basicauthoverhttpenabled)|Allow Basic authentication for HTTP|
| BatterySaverModeAvailability   |    |
|[BlockThirdPartyCookies](#blockthirdpartycookies)|Block third party cookies|
|   BrowserAddPersonEnabled  |    |
|[BrowserCodeIntegritySetting](#browsercodeintegritysetting)|Configure browser process code integrity guard setting|
|  BrowserContextAwareAccessSignalsAllowlist  |    |
| BrowserExecutableFolder |     |
|[BrowserGuestModeEnabled](#browserguestmodeenabled)|Enable guest mode|
| BrowserGuestModeEnforced  |    |
|[BrowserLegacyExtensionPointsBlockingEnabled](#browserlegacyextensionpointsblockingenabled)|Enable browser legacy extension point blocking|
|[BrowserSignin](#browsersignin)|Browser sign-in settings|
|[BrowsingDataLifetime](#browsingdatalifetime)|Browsing Data Lifetime Settings|
|[BuiltInDnsClientEnabled](#builtindnsclientenabled)|Use built-in DNS client|
|[CECPQ2Enabled](#cecpq2enabled)|CECPQ2 post-quantum key-agreement enabled for TLS|
|[CertificateTransparencyEnforcementDisabledForCas](#certificatetransparencyenforcementdisabledforcas)|Disable Certificate Transparency enforcement for a list of subjectPublicKeyInfo hashes|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](#certificatetransparencyenforcementdisabledforlegacycas)|Disable Certificate Transparency enforcement for a list of legacy certificate authorities|
|[CertificateTransparencyEnforcementDisabledForUrls](#certificatetransparencyenforcementdisabledforurls)|Disable Certificate Transparency enforcement for specific URLs|
| ChromeAppsWebViewPermissiveBehaviorAllowed   |    |
|[ClearBrowsingDataOnExit](#clearbrowsingdataonexit)|Clear browsing data when Microsoft Edge closes|
|[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)|Clear cached images and files when Microsoft Edge closes|
|[ClickOnceEnabled](#clickonceenabled)|Allow users to open files using the ClickOnce protocol|
|  CloudAPAuthEnabled |    |
|  CloudManagementEnrollmentMandatory  |    |
|  CloudPolicyOverridesPlatformPolicy  |    |
|[CommandLineFlagSecurityWarningsEnabled](#commandlineflagsecuritywarningsenabled)|Enable security warnings for command-line flags|
|[ComponentUpdatesEnabled](#componentupdatesenabled)|Enable component updates in Microsoft Edge|
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|Configure automatic sign in with an Active Directory domain account when there is no Azure AD domain account|
|[ConfigureViewInFileExplorer](#configureviewinfileexplorer)|Configure the View in File Explorer feature for SharePoint pages in Microsoft Edge|
|[CookiesAllowedForUrls](#cookiesallowedforurls)|Allow cookies on specific sites|
|[CookiesBlockedForUrls](#cookiesblockedforurls)|Block cookies on specific sites|
|[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)|Limit cookies from specific websites to the current session|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|DNS interception checks enabled|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|Set Microsoft Edge as default browser|
|[DefaultBrowserSettingsCampaignEnabled](#defaultbrowsersettingscampaignenabled)|Enables default browser settings campaigns|
|[DefaultCookiesSetting](#defaultcookiessetting)|Configure cookies|
|[DeleteDataOnMigration](#deletedataonmigration)|Delete old browser data on migration|
|[DiagnosticData](#diagnosticdata)|Send required and optional diagnostic data about browser usage|
|[DirectInvokeEnabled](#directinvokeenabled)|Allow users to open files using the DirectInvoke protocol|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|Disable CNAME lookup when negotiating Kerberos authentication|
|[DisableScreenshots](#disablescreenshots)|Disable taking screenshots|
|[DiskCacheDir](#diskcachedir)|Set disk cache directory|
|[DiskCacheSize](#diskcachesize)|Set disk cache size, in bytes|
|[DnsOverHttpsMode](#dnsoverhttpsmode)|Control the mode of DNS-over-HTTPS|
|[DnsOverHttpsTemplates](#dnsoverhttpstemplates)|Specify URI template of desired DNS-over-HTTPS resolver|
|  DomainReliabilityAllowed  |    |
|  EdgeAdminCenterEnabled |    |
|  EdgeAdminCenterEnrollmentToken  |    |
| EdgeAdminCenterUseOCPSEndpoint   |    |
|  EdgeAdminCenterUseTestEndpoint  |    |
|[EdgeDefaultProfileEnabled](#edgedefaultprofileenabled)|Default Profile Setting Enabled|
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |
|    |    |


## See also

- [Microsoft Edge for Business](/deployedge/microsoft-edge-for-business)
