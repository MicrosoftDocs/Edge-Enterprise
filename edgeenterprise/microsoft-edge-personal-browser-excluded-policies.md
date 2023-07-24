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
| [BrowserExecutableFolder](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-webview-policies#browserexecutablefolder) | Configure the location of the browser executable folder    |
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
|[EfficiencyMode](#efficiencymode)|Configure when efficiency mode should become active|
|[EfficiencyModeEnabled](#efficiencymodeenabled)|Efficiency mode enabled|
|[EfficiencyModeOnPowerEnabled](#efficiencymodeonpowerenabled)|Enable efficiency mode when the device is connected to a power source|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|Include non-standard port in Kerberos SPN|
|[EnableOnlineRevocationChecks](#enableonlinerevocationchecks)|Enable online OCSP/CRL checks|
|[EncryptedClientHelloEnabled](#encryptedclienthelloenabled)|TLS Encrypted ClientHello Enabled|
|[EnforceLocalAnchorConstraintsEnabled](#enforcelocalanchorconstraintsenabled)|Determines whether the built-in certificate verifier will enforce constraints encoded into trust anchors loaded from the platform trust store (deprecated)|
|[EnhanceSecurityMode](#enhancesecuritymode)|Enhance the security state in Microsoft Edge|
|[EnhanceSecurityModeBypassIntranet](#enhancesecuritymodebypassintranet)|Enhanced Security Mode configuration for Intranet zone sites|
|[EnhanceSecurityModeBypassListDomains](#enhancesecuritymodebypasslistdomains)|Configure the list of domains for which enhance security mode will not be enforced|
|[EnhanceSecurityModeEnforceListDomains](#enhancesecuritymodeenforcelistdomains)|Configure the list of domains for which enhance security mode will always be enforced|
|[EnhanceSecurityModeIndicatorUIEnabled](#enhancesecuritymodeindicatoruienabled)|Manage the indicator UI of the Enhanced Security Mode (ESM) feature in Microsoft Edge|
|[EnhanceSecurityModeOptOutUXEnabled](#enhancesecuritymodeoptoutuxenabled)|Manage opt-out user experience for Enhanced Security Mode (ESM) in Microsoft Edge|
|  EnterpriseProfileCreationKeepBrowsingData  |    |
|[ExemptFileTypeDownloadWarnings](#exemptfiletypedownloadwarnings)|Disable download file type extension-based warnings for specified file types on domains|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|Control communication with the Experimentation and Configuration Service|
|[ExplicitlyAllowedNetworkPorts](#explicitlyallowednetworkports)|Explicitly allowed network ports|
|[ExtensionInstallSources](#extensioninstallsources)|Configure extension and user script install sources|
|[FamilySafetySettingsEnabled](#familysafetysettingsenabled)|Allow users to configure Family safety and Kids Mode|
|[FeatureFlagOverridesControl](#featureflagoverridescontrol)|Configure users ability to override feature flags|
|[ForceCertificatePromptsOnMultipleMatches](#forcecertificatepromptsonmultiplematches)|Configure whether Microsoft Edge should automatically select a certificate when there are multiple certificate matches for a site configured with "AutoSelectCertificateForUrls" (deprecated)|
| ForceEnablePepperVideoDecoderDevAPI   |    |
| [HSTSPolicyBypassList](#hstspolicybypasslist)|Configure the list of names that will bypass the HSTS policy check   |    |
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|Use hardware acceleration when available|
| HeadlessMode |  |
|[HeadlessModeEnabled](#headlessmodeenabled)|Control use of the Headless Mode|
|[HideFirstRunExperience](#hidefirstrunexperience)|Hide the First-run experience and splash screen|
|[HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](#hideinternetexplorerredirectuxforincompatiblesitesenabled)|Hide the one-time redirection dialog and the banner on Microsoft Edge|
|[HideRestoreDialogEnabled](#hiderestoredialogenabled)|Hide restore pages dialog after browser crash|
|  HighEfficiencyModeEnabled  |    |
|  HttpAllowlist  |    |
|[ImplicitSignInEnabled](#implicitsigninenabled)|Enable implicit sign-in|
|[InAppSupportEnabled](#inappsupportenabled)|In-app support Enabled|
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
