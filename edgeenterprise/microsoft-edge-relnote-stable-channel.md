---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 06/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Microsoft Edge release notes for Stable Channel"
---

# Release notes for Microsoft Edge Stable Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Stable Channel.

- All the security updates are listed [here](microsoft-edge-relnotes-security.md).
- Archived release notes for Microsoft Edge Stable Channel are located [here](microsoft-edge-relnote-archive-stable-channel.md).

 To understand Microsoft Edge channels, see the [Overview of the Microsoft Edge channels](microsoft-edge-channels.md).

> [!NOTE]
> For the Stable Channel, updates will roll out progressively over one or more days. To learn more, see [Progressive rollouts for Microsoft Edge updates](microsoft-edge-update-progressive-rollout.md).
>
> Microsoft Edge Web Platform constantly evolves to improve user experience, security, and privacy. To learn more, see [Site compatibility-impacting changes coming to Microsoft Edge](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes).

## Version 91.0.864.41: June 3

Stable channel security updates are listed [here](https://docs.microsoft.com/deployedge/microsoft-edge-relnotes-security#may-13-2021).

## Version 91.0.864.37: May 27

Stable channel security updates are listed [here](https://docs.microsoft.com/deployedge/microsoft-edge-relnotes-security#may-13-2021).

### Feature updates

- **Identify network traffic originating from Microsoft Defender Application Guard containers at the proxy level**. Starting with Microsoft Edge version 91, there’s built in support to tag network traffic originating from Application Guard containers, allowing enterprises to identify them and apply specific policies.

- **Support option to allow synchronizing Favorites from the host to the Edge Application Guard container**. Starting with Microsoft Edge version 91, users have the option to configure Application Guard to synchronize their favorites from the host to the container. This ensures new favorites appear on the container as well.

- **Starting with Microsoft Edge version 91 the browser will automatically interrupt downloads of types which could harm your computer if those downloads are started without a user interaction and are not supported by SmartScreen Application Reputation check**. Users may override and continue to download by right clicking and choosing “Keep” on the download item. Enterprise administrators may opt out of this behavior by configuring the following policy:
  - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](https://docs.microsoft.com/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings.md) - Disable download file type extension-based warnings for specified file types on domains

    For more information, see [Microsoft Edge Security downloads interruptions](microsoft-edge-security-downloads-interruptions.md).

- **Support for Speech Recognition APIs**. Starting with Microsoft Edge version 91, API support for speech recognition commands on Google.com and similar sites will be added. This feature is limited to a randomly selected group of users who have enabled experimentation. These users are giving feedback to the feature team.

- **Personalize your browser with new theme colors**. Make Microsoft Edge your own with one of the fourteen new theme colors on the Settings -> Appearance page. You can also install custom themes from the Microsoft Edge Add-on site. [Learn more](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

### Policy updates

#### New policies

Six new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added:

- [ApplicationGuardTrafficIdentificationEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) - Application Guard Traffic Identification
- [ExplicitlyAllowedNetworkPorts](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) - Explicitly allowed network ports
- [ImportStartupPageSettings](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importstartuppagesettings) - Allow importing of startup page settings
- [MathSolverEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#mathsolverenabled) - Let users snip a Math problem and get the solution with a step-by-step explanation in Microsoft Edge
- [NewTabPageContentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) - Allow Microsoft News content on the new tab page
- [NewTabPageQuickLinksEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) - Allow quick links on the new tab page

#### Obsoleted Policy

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) - Enable Proactive Authentication
<!-- end major 91 -->


## Version 90.0.818.66: May 20

Fixed various bugs and performance issues.

## Version 90.0.818.62: May 13

Stable channel security updates are listed [here](https://docs.microsoft.com/deployedge/microsoft-edge-relnotes-security#may-13-2021).

## Version 90.0.818.56: May 6

Fixed various bugs and performance issues.

## Version 90.0.818.51: April 29

Stable channel security updates are listed [here](https://docs.microsoft.com/deployedge/microsoft-edge-relnotes-security#april-29-2021).

## Version 90.0.818.49: April 26

Fixed various bugs and performance issues.

## Version 90.0.818.46: April 22 ##

Stable channel security updates are listed [here](https://docs.microsoft.com/deployedge/microsoft-edge-relnotes-security#april-22-2021).

## Version 90.0.818.42: April 19

Fixed various bugs and performance issues.

## Version 90.0.818.41: April 16 ##

> [!Important]
>This update contains [CVE-2021-21224](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21224) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).


Stable channel security updates are listed [here](https://docs.microsoft.com//deployedge/microsoft-edge-relnotes-security#april-16-2021).

## Version 90.0.818.39: April 15 ##

Stable channel security updates are listed [here](https://docs.microsoft.com/deployedge/microsoft-edge-relnotes-security#april-15-2021).

## Feature updates ##

-	 **Single Sign On (SSO) is now available for Azure Active Directory (Azure AD) accounts and Microsoft Account (MSA) on macOS.** A user signed in on Microsoft Edge on macOS will now get automatically signed into websites that are configured to allow single sign on with Work and Microsoft accounts (for example, bing.com, office.com, msn.com, and outlook.com).

- **Kiosk mode.** Starting with Microsoft Edge version 90, we have locked down the UI print settings to only allow the configured printers and “Print to PDF” options. We have also done improvements within the assigned access single app kiosk mode to restrict the launch of other applications from the browser. For more information about the kiosk mode features please go [here](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features).

- **Interrupt Downloads** Starting with Microsoft Edge version 91 the browser will automatically interrupt downloads of types which could harm your computer if those downloads are started without a user interaction and are not supported by SmartScreen Application Reputation check. Users may override and continue to download by right clicking and choosing “Keep” on the download item.
Enterprise administrators may opt out of this behavior one of these two policies:
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](https://docs.microsoft.com/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains
For more information, see [Microsoft Edge Security downloads interruptions](https://docs.microsoft.com/deployedge/microsoft-edge-security-downloads-interruptions)

- **Printing**:

    - **New print rasterization mode for non-PostScript printers.** Starting with Microsoft Edge version 90, Admins can use a new policy to define print rasterization mode for their users. This policy controls how Microsoft Edge prints to non-PostScript printers on Windows. Sometimes print jobs on non-PostScript printers need to be rasterized to print correctly. The print options are Full and Fast.
    
  -	**Additional page scaling options for printing.** Users are now able to customize scaling while printing webpages and PDF documents using additional options. The "Fit to Page" option ensures that the webpage or document is fit into the space available in the selected "Paper size" for printing. The "Actual size" option ensures that there are no changes in the size of the contents being printed regardless of the selected "Paper size".

-	**Productivity:**

    -	**Autofill suggestions are extended to include address fields content from clipboard.** Clipboard content is parsed when you click on a profile/address field (for example, phone, email, zip code, city, state, etc.) to show as autofill suggestions.

    -	**Users can search for autofill suggestions even if a form or field isn’t detected.** Today if you have your information saved on Microsoft Edge, autofill suggestions pop up automatically and help you save time while filling out forms. In cases where autofill misses a form, or if you want to fetch data in forms that don't typically have autofill (like temporary forms), you can search for your information use autofill.

-	**Access downloads from a flyout in the menu bar.** Downloads will appear in the top-right corner with all the active downloads in one place. This menu is easily dismissible so users can continue browsing uninterrupted, and they can monitor overall download progress right from the toolbar. [Learn more](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).

-	**Improvements to font rendering.** Starting with Microsoft Edge version 90, we made improvements to the rendering of text to improve clarity and reduce blurriness. Part of the font rendering improvements will land in Beta version 90 but are disabled by default.

- **Kids mode.** We have updated the policy so that when the policy is enabled, it will disable the Kid Mode feature in addition to family safety. More about Kids Mode [here](https://go.microsoft.com/fwlink/?linkid=2146910)

## Policy updates

## New policies

Eight new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added:
-	[ApplicationGuardFavoritesSyncEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardfavoritessyncenabled) - Application Guard Favorites Sync Enabled
- [ApplicationGuardTrafficIdentificationEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) Application Guard Traffic Identification
- [ExplicitlyAllowedNetworkPorts](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) Explicitly allowed network ports
- [ImportStartupPageSettings](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importstartuppagesettings) Allow importing of startup page settings
- [MathSolverEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#mathsolverenabled) Let users snip a Math problem and get the solution with a step-by-step explanation in Microsoft Edge
- [NewTabPageContentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) Allow Microsoft News content on the new tab page
- [NewTabPageQuickLinksEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) Allow quick links on the new tab page
-	[FetchKeepaliveDurationSecondsOnShutdown](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#fetchkeepalivedurationsecondsonshutdown)- Fetch keepalive duration on shutdown
-	[ManagedConfigurationPerOrigin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#managedconfigurationperorigin) - Sets managed configuration values for websites to specific origins
-	[PrintRasterizationMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printrasterizationmode) - Print Rasterization Mode
-	[QuickViewOfficeFilesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#quickviewofficefilesenabled) - Manage QuickView Office files capability in Microsoft Edge
-	[SSLErrorOverrideAllowedForOrigins](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sslerroroverrideallowedfororigins) - Allow users to proceed from the HTTPS warning page for specific origins
-	[WindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#windowocclusionenabled) - Enable Window Occlusion
-	[WindowsHelloForHTTPAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#windowshelloforhttpauthenabled) - Windows Hello For HTTP Auth Enabled

## Deprecated policies

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled) Enable Proactive Authentication
-	[NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - Enable Native Window Occlusion
-	[SSLVersionMin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sslversionmin)- Minimum TLS version enabled

## Version 89.0.774.77: April 14

> [!Important]
>This update contains  [CVE-2021-21206](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21206) and [CVE-2021-21220](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21220) which has been reported by the Chromium team as having an exploit in the wild.  For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](https://docs.microsoft.com/deployedge/microsoft-edge-relnotes-security#april-14-2021).

## Version 89.0.774.76: April 12

Fixed various bugs and performance issues.

## Version 89.0.774.75: April 8

Fixed various bugs and performance issues.

## Version 89.0.774.68: April 1

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#april-1-2021).

## Version 89.0.774.63: March 25

Fixed various bugs and performance issues.

## Version 89.0.774.57: March 18

Fixed various bugs and performance issues.

## Version 89.0.774.54: March 13

> [!IMPORTANT]
> This update contains [CVE-2021-21193](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21193) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#march-13-2021).

## Version 89.0.774.50: March 10

Fixed various bugs and performance issues.

## Version 89.0.774.48: March 8

Fixed various bugs and performance issues.

<!-- begin major 89 -->
## Version 89.0.774.45: March 4

> [!IMPORTANT]
> This update contains [CVE-2021-21166](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21166) which has been reported by the Chromium team as having an exploit in the wild. For more information, see the [Security Update Guide](https://msrc.microsoft.com/update-guide).

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#march-4-2021).

### Resolved issues

- **Taskbar and Start menu shortcut updates and fixes:**
  - Right-clicking the Microsoft Edge shortcut in the Start menu will now properly show the option to unpin Microsoft Edge from the taskbar when it’s pinned.
  - Start layouts that include a [taskbar configuration](/windows/configuration/configure-windows-10-taskbar) to pin Microsoft Edge to the taskbar will no longer result in a second Microsoft Edge shortcut getting pinned to the taskbar.
  - Organizations using Windows Roaming Profiles will no longer see a blank white icon in place of the Microsoft Edge icon on the taskbar when their users log on to Windows.

### Feature updates

- **Kiosk mode enables additional lockdown capabilities**. Starting with Microsoft Edge version 89, we have added additional lockdown capabilities within kiosk mode to enable customers to get the job done in a productive and more secure experience. [Learn more](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features).

- **The Enterprise Mode Site List Manager tool will be available in the browser through the *edge://compat* page**. You can use this tool to create, edit and export your site list XML for Internet Explorer mode on Microsoft Edge. You can enable access to this tool as needed through group policy. [Learn More](./edge-ie-mode-site-list-manager.md).

- **Improve browser performance with sleeping tabs**. Sleeping tabs improves browser performance by putting inactive tabs to sleep to free up system resources like memory and CPU so active tabs or other applications can use them. Users can prevent sites from going to sleep and configure the length of time before an inactive tab goes to sleep. To keep users in their flow, there are also [heuristics](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) to prevent certain sites from going to sleep, such as intranet sites. This feature can be managed with group policies.

- **Reset your Microsoft Edge sync data in the cloud manually**. We are introducing a way to reset your Microsoft Edge sync data from within the product. This ensures that your data is cleared from Microsoft services, as well as resolving certain product issues that previously required a support ticket.

- **Intelligent enablement of Single sign-on (SSO) for all Windows Azure Active Directory (Azure AD) accounts for users with a single non-Azure AD Microsoft Edge profile**.  Automatically turn this setting on for users that might benefit the most from this feature. If a user has only one Microsoft Edge profile (and it’s not Azure AD or Kids Mode), the setting will be automatically turned on when Microsoft Edge launches. This auto-toggle will also automatically turn off if a user later chooses to sign into a different Microsoft Edge profile with an Azure AD account. Users can manually update their preferences for this feature in **Settings > Profiles >Profile Preferences > Allow single sign-on for work or school sites using this profile**.

- **Improvements to text selection experience within PDF documents**. Users will begin to get a smoother and more consistent text selection experience across PDF documents opened in Microsoft Edge starting with version 89.

- **Date of birth field now supported in autofill**. Today Microsoft Edge helps you save time and effort while filling out forms and creating accounts online by auto filling your data like addresses, names, phone numbers, etc. Starting with Microsoft Edge version 89, we are adding support for another field that you can have saved and auto-filled - date of birth. You can view, edit and delete this information anytime in your profile settings.

### Policy updates

#### New policies

Seven new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added.

- [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime) - Browsing Data Lifetime Settings
- [MAMEnabled](./microsoft-edge-policies.md#mamenabled) - Mobile App Management Enabled
- [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages) - Define an ordered list of preferred languages that websites should display in if the site supports the language
- [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled) - Allow recommendations and promotional notifications from Edge
- [PrintingAllowedBackgroundGraphicsModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes) - Restrict background graphics printing mode
- [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault) - Default background graphics printing mode
- [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist) - Block smart actions  for a list of services

#### Obsoleted policies

The following policies are obsoleted.

- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) - Use a default referrer policy of no-referrer-when-downgrade
- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - Enable usage and crash-related data reporting
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - Send site information to improve Microsoft services
<!-- end major 89 -->

<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)