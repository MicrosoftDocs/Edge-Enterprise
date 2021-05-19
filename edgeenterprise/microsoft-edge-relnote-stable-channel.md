---
title: "Microsoft Edge release notes for Stable Channel"
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 04/29/2021
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
> Microsoft Edge Web Platform constantly evolves to improve user experience, security, and privacy. To learn more, see [Site compatibility-impacting changes coming to Microsoft Edge] (https://docs.microsoft.com/en-us/microsoft-edge/web-platform/site-impacting-changes).

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
-	[FetchKeepaliveDurationSecondsOnShutdown](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#fetchkeepalivedurationsecondsonshutdown)- Fetch keepalive duration on shutdown
-	[ManagedConfigurationPerOrigin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#managedconfigurationperorigin) - Sets managed configuration values for websites to specific origins
-	[PrintRasterizationMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printrasterizationmode) - Print Rasterization Mode
-	[QuickViewOfficeFilesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#quickviewofficefilesenabled) - Manage QuickView Office files capability in Microsoft Edge
-	[SSLErrorOverrideAllowedForOrigins](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sslerroroverrideallowedfororigins) - Allow users to proceed from the HTTPS warning page for specific origins
-	[WindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#windowocclusionenabled) - Enable Window Occlusion
-	[WindowsHelloForHTTPAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#windowshelloforhttpauthenabled) - Windows Hello For HTTP Auth Enabled

## Deprecated policies

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
## Version 88.0.705.81: February 25

Fixed various bugs and performance issues.

## Version 88.0.705.74: February 17

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#february-17-2021).

## Version 88.0.705.68: February 11

Fixed various bugs and performance issues.

## Version 88.0.705.63: February 5

> [!IMPORTANT]
> This update contains [CVE-2021-21148](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21148) which has been reported by the Chromium team as having an exploit in the wild.

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#february-5-2021).

## Version 88.0.705.62: February 4

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#february-4-2021).

Fixed various bugs and performance issues.

## Version 88.0.705.56: January 28

Fixed various bugs and performance issues.

## Version 88.0.705.53: January 26

Fixed various bugs and performance issues.

## Version 88.0.705.50: January 21

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#january-21-2021).

<!--- begin major 88  --->
### Feature updates

- **Deprecations:**

  - Deprecate support for FTP protocol. Support for the legacy FTP protocol has been removed from Microsoft Edge. Attempting to navigate to an FTP link will result in the browser directing the Operating System to open an external application to handle the FTP link. Alternatively, IT administrators can configure Microsoft Edge to use IE Mode for sites that rely on the FTP protocol.
  - Adobe Flash support will be removed. Starting with Microsoft Edge Beta version 88, Adobe Flash capability and support will be removed. Learn more: [Update on Adobe Flash Player End of Support - Microsoft Edge Blog (windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Authentication:**

  - Single Sign On (SSO) now available for Azure Active Directory (Azure AD) accounts and Microsoft Account (MSA) on down-level Windows. A user signed in on Microsoft Edge on down-level Microsoft Windows (7, 8.1) will now get automatically signed into websites that are configured to allow single sign on with Work and Microsoft accounts (e.g., bing.com, office.com, msn.com, outlook.com).<br>Note: A user may have to sign out and then sign back in if they'd signed into Microsoft Edge in a version prior to Microsoft Edge 88 to leverage this feature.
  
  - Single sign-on (SSO) to work sites using any Windows Azure Active Directory (Azure AD) accounts on system in non-Azure AD Microsoft Edge profiles. This feature can be enabled for any profile that isn’t signed-in with a work/school account and is not guest or in-private and allows the use of any signed-in work/school account on operating system with that profile. This feature can be configured in **Settings** > **Profiles** > **Profile Preferences** > **Allow single sign-on for work or school sites using this profile**.
  
    > [!NOTE]
    > "Single sign-on (SSO) for all Windows accounts using the Microsoft Edge profile" is an update to the January 21 release notes.

- **Kiosk mode option to end session**. The "End session" button is now available in a kiosk mode public browsing experience. This feature ensures that browser data and settings are deleted when Microsoft Edge is closed. Learn more about kiosk mode features and roadmap, [Configure Microsoft Edge kiosk mode](./microsoft-edge-configure-kiosk-mode.md).

- **Security and Privacy:**

  - Alerts are generated if a user's password is found in an online leak. User passwords are checked against a repository of known-breached credentials and sends the user an alert if a match is found. To ensure security and privacy, user passwords are hashed and encrypted when they're checked against the database of leaked credentials.
  - Automatically upgrade mixed content. Secure pages delivered over HTTPS may contain references images that are served over non-secure HTTP. To improve privacy and security in Microsoft Edge 88, those images will be retrieved over HTTPS instead. If the image is not available over HTTPS, it will not be loaded.
  - View site permissions by site and by recent activity. Starting with Microsoft Edge 88, users will be able to manage site permissions more easily. They will be able to view permissions by web site rather than just permission type. Additionally, we’ve added a recent activity section that will show a user all the recent changes to their site permissions.
  - Increased controls for browser cookies. Starting with Microsoft Edge 88, users can delete third party cookies without affecting first party cookies. Users will also be able to filter their cookies by first or third party and sort by name, number of cookies, and the amount of data stored and last modified.

- **Passwords:**

  - Password Generator. Microsoft Edge offers a built-in strong password generator that you can use when signing up for a new account or when changing an existing password. Just look for the browser-suggested password drop down in the password field and when selected, it will automatically save to the browser and sync across devices for easy future use.
  - Password Monitor. When any of your passwords saved to the browser matches with those seen in the list of leaked credentials, Microsoft Edge will notify you and prompt you to update your password. Password Monitor scans for matches on your behalf and is on by default.
  - Edit Password. You can now edit your saved passwords directly in Microsoft Edge Settings. Any time a password has been updated outside of Microsoft Edge, it’s easy to replace the saved older password with the new one by editing the saved entry in Settings. 

- **Improve Microsoft Edge startup speed with startup boost**. To improve Microsoft Edge startup speed, we’ve developed a feature named startup boost. Startup boost makes Microsoft Edge launch faster by enabling Microsoft Edge to run in the background. Note: This feature is limited to a randomly selected group of users who have enabled experimentation. These users are giving feedback to the feature team.

- **Productivity:**

  - Improve productivity and multi-tasking with vertical tabs. As the number of horizontal tabs grows, site titles start to get cut off and tab controls are lost as each tab shrinks. This interrupts user workflow as they spend more time finding, switching, and managing their tabs and less time on the task at hand. Vertical tabs let users move their tabs to the side, where vertically aligned icons and longer site titles make it easier to quickly scan, identify and switch to the tab they want to open.
  - Auto filling the date of birth field. Microsoft Edge already helps save time and effort while filling out forms and creating accounts online by auto filling user data such as addresses, names, phone numbers, etc. Microsoft Edge now supports the date of birth field which users can save and auto fill. A user can view, edit and delete this information anytime in their profile settings.
  - Improvements to Recently closed in History. Recently closed now keeps the last 25 tabs and windows from any past browsing session rather than just the previous session. Users can select Recently closed in the new History experience to see all the tabs that were open.
  - “Your day at a glance” feature enabled by default. Starting with Microsoft Edge version 88, information workers can benefit from intelligent productivity features on their New tab page (NTP). Microsoft Edge 87 users will also experience these features within 2 weeks after Microsoft Edge 88 release. We offer users signed in with their work or school account personalized and relevant content powered by their M365 Graph. Users can quickly scan their “Your day at a glance” modules to easily track their meetings and recent work as well as quickly launch the applications they want to use.

- **History and open tabs sync**. History and open tabs sync is now available for users to enjoy. Enabling these features will help users pick up where they left off by making their browsing history and open tabs available on all their syncing devices. We've updated sync and browser history policies, so now users are connected and productive across any devices by using Microsoft Edge. [Learn more](https://blogs.windows.com/windowsexperience/2021/01/21/this-year-lets-resolve-to-make-the-most-of-our-time-online-and-better-protect-ourselves-from-online-threats/).

- **PDF:**

  - PDF document display in book view (two page). Starting with Microsoft Edge version 88, users can view PDF documents in a single page or in the two page book view. To change the view, click the **Page View** button in the toolbar.
  - Anchored text notes support for PDF files. Starting with Microsoft Edge version 87, users can add typed text notes on any piece of text in PDF files.

- **Fonts:**

  - Browser icons are updated to the Fluent design system. As part of our continued work around Fluent Design in the browser, we've made changes to closer align icons to the new Microsoft icon system. These changes will impact many of our high-touch user interfaces, including tabs, address bar, as well as navigational and wayfinding icons found in our various menus.
  - Improved font rendering. Text rendering is improved for better clarity and to reduce blurriness.

### Policy updates

#### New policies

Eighteen new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added.

- [BasicAuthOverHttpEnabled](./microsoft-edge-policies.md#basicauthoverhttpenabled) - Allow Basic authentication for HTTP.
- [BlockExternalExtensions](./microsoft-edge-policies.md#blockexternalextensions) - Blocks external extensions from being installed.
- [InternetExplorerIntegrationLocalFileAllowed](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileallowed) - Allow launching of local files in Internet Explorer mode.
- [InternetExplorerIntegrationLocalFileExtensionAllowList](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist) - Open local files in Internet Explorer mode file extension allow list.
- [InternetExplorerIntegrationLocalFileShowContextMenu](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileshowcontextmenu) - Show context menu to open a link in Internet Explorer mode.
- [IntranetRedirectBehavior](./microsoft-edge-policies.md#intranetredirectbehavior) - Intranet Redirection Behavior.
- [PrinterTypeDenyList](./microsoft-edge-policies.md#printertypedenylist) - Disable printer types on the deny list.
- [ShowMicrosoftRewards](./microsoft-edge-policies.md#showmicrosoftrewards) - Show Microsoft Rewards experiences.
- [SleepingTabsEnabled](./microsoft-edge-policies.md#sleepingtabsenabled) - Configure Sleeping Tabs.
- [SleepingTabsTimeout](./microsoft-edge-policies.md#sleepingtabstimeout) - Set the background tab inactivity timeout for Sleeping Tabs.
- [SleepingTabsBlockedForUrls](./microsoft-edge-policies.md#sleepingtabsblockedforurls) - Block Sleeping Tabs on specific sites.
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled) - Enable startup boost.
- [TargetBlankImpliesNoOpener](./microsoft-edge-policies.md#targetblankimpliesnoopener) - Do not set window.opener for links targeting _blank.
- [UpdatePolicyOverride](./microsoft-edge-policies.md#updatepolicyoverride) - Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.
- [VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) - Configures availability of a vertical layout for tabs on the side of the browser.
- [WebRtcAllowLegacyTLSProtocols](./microsoft-edge-policies.md#webrtcallowlegacytlsprotocols) - Allow legacy TLS/DTLS downgrade in WebRTC.
- [WebWidgetAllowed](./microsoft-edge-policies.md#webwidgetallowed) - Enable the Web widget.
- [WebWidgetIsEnabledOnStartup](./microsoft-edge-policies.md#webwidgetisenabledonstartup) - Allow the Web widget at Windows startup.

#### Deprecated Policies

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) - Enable Proactive Authentication.
- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist) - Configure proxy bypass rules.
- [ProxyMode](./microsoft-edge-policies.md#proxymode) - Configure proxy server settings.
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl) - Set the proxy .pac file URL.
- [ProxyServer](./microsoft-edge-policies.md#proxyserver) - Configure address or URL of proxy server.
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) - Allow WebDriver to Override Incompatible Policies.

### Obsoleted Policies

- [AllowPopupsDuringPageUnload](./microsoft-edge-policies.md#allowpopupsduringpageunload) - Allows a page to show popups during its unloading.
- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting) - Default Adobe Flash setting.
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls) - Allow the Adobe Flash plug-in on specific sites.
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls) - Block the Adobe Flash plug-in on specific sites.
- [RunAllFlashInAllowMode](./microsoft-edge-policies.md#runallflashinallowmode) - Extend Adobe Flash content setting to all content.
<!--- end major 88  --->
## Version 87.0.664.75: January 7

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#january-7-2021).

## Version 87.0.664.66: December 17

Fixed various bugs and performance issues.

## Version 87.0.664.60: December 10

Fixed various bugs and performance issues.

## Version 87.0.664.57: December 7

Fixed various bugs and performance issues. Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#december-7-2020).

## Version 87.0.664.55: December 3

Fixed various bugs and performance issues. The following feature was updated for this release.

- **Shopping is enabled by default**. Starting with Microsoft Edge version 87, enterprise users can benefit from shopping in Microsoft Edge. With Shopping features, Microsoft Edge helps users find coupons and better prices while shopping online. (The coupon experience was released with Stable version 87.0.664.41). The price comparison experience is now available with this update. This feature can be configured using the [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) policy. See our [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) and [Learn More](/microsoft-edge/privacy-whitepaper#shopping) about Microsoft Shopping.

## Version 87.0.664.52: November 30

Fixed various bugs and performance issues.

## Version 87.0.664.47: November 23

Fixed various bugs and performance issues.

<!-- begin major 87 --->
## Version 87.0.664.41: November 19

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#november-19-2020).

### Feature updates

- **Automatic redirection for incompatible sites from Internet Explorer to Microsoft Edge**. Starting with the Microsoft Edge 87 Stable update, public websites that show an incompatibility message on Internet Explorer will be automatically redirected to Microsoft Edge. To learn more and to configure this experience, see [Redirecting incompatible sites](./edge-learnmore-neededge.md).

- **Kiosk mode privacy features enabled**. Starting with Microsoft Edge version 87, kiosk mode features that will help enterprises around the privacy of user data will be enabled. These features will enable experiences such as clear the user data on exit, delete downloaded files and to reset the configured start experience after a specified amount of idle time. Learn more about how to [Configure Microsoft Edge kiosk mode](./microsoft-edge-configure-kiosk-mode.md)

- **Shopping features enabled by default**. Starting with Microsoft Edge version 87 enterprise users can also benefit from shopping in Edge. With Shopping features, Microsoft Edge helps users to find coupons and better prices while shopping online. Coupon experience is available with this update and price comparison will be released in upcoming updates for Microsoft Edge 87. This feature can be configured through [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) policy. See our [Blog](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/) and [Learn More](/microsoft-edge/privacy-whitepaper#shopping) about Microsoft Shopping.

- **ClickOnce deployment enabled by default**. ClickOnce is enabled by default in Microsoft Edge 87, which reduces the barriers for enterprises to deploy software and better align with Microsoft Edge Legacy browser behavior. Starting in Microsoft Edge 87, the ClickOnceEnabled policy's "Not configured" state will reflect the new default ClickOnce state of Enabled (as compared to the previous default state of Disabled).

- **The enterprise new tab page (NTP) integrates productivity with customizable, work-relevant feed content**. The enterprise NTP blends the Office 365 productivity page we offer to users signed in with their work or school account with personalized, work-relevant company and industry feeds that are organized in a single page. Users will be able to recognize the familiar Office 365 content and Microsoft Search for Business powered by Bing. In addition, they can easily customize "My Feed" by choosing the most relevant content to them from the available content and modules for their organization. IT Administrators can control the News feed settings for their  organization, including the selected industry for the Edge new tab page by going to Microsoft 365 admin center. [Learn more](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/)

- **Privacy and Security:**

  - Support TLS Token Binding for policy-configured sites. TLS Token binding helps prevent token theft attacks to ensure that cookies can't be reused from a device other than the device upon which they were initially set. The use of TLS token binding requires setting the [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) policy and requires that the sites listed support this feature.

- **Keyboard support for highlighter on PDF files**. Users can use their keyboard keys to highlight any text on a PDF.

- **Printing:**

  - Choose which side to flip on when printing on both sides. Users can choose to flip on the long side or the short side of a sheet when printing on both sides.
  - Choose print rasterization mode for the enterprise. Control how Microsoft Edge prints to a non-PostScript printer on Windows. Sometimes print jobs on non-PostScript printers need to be rasterized to print correctly. The print options are "Full" and "Fast".

### Policy updates

#### New policies

Ten new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added.

- [ConfigureFriendlyURLFormat](./microsoft-edge-policies.md#configurefriendlyurlformat) - Configure the default paste format of URLs copied from Microsoft Edge, and determine if additional formats will be available to users.
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) - Shopping in Microsoft Edge enabled.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](./microsoft-edge-policies.md#hideinternetexplorerredirectuxforincompatiblesitesenabled) - Hide the one-time redirection dialog and the banner on Microsoft Edge.
- [KioskAddressBarEditingEnabled](./microsoft-edge-policies.md#kioskaddressbareditingenabled) - Configure address bar editing for kiosk mode public browsing experience.
- [KioskDeleteDownloadsOnExit](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) - Delete files downloaded as part of kiosk session when Microsoft Edge closes.
- [PasswordRevealEnabled](./microsoft-edge-policies.md#passwordrevealenabled) - Enable Password reveal button.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerpreventbhoinstall) - Prevent install of the browser helper object (BHO) to redirect incompatible sites from Internet Explorer to Microsoft Edge.
- [RedirectSitesFromInternetExplorerRedirectMode](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerredirectmode) - Redirect incompatible sites from Internet Explorer to Microsoft Edge.
- [SpeechRecognitionEnabled](./microsoft-edge-policies.md#speechrecognitionenabled) - Configure Speech Recognition.
- [WebCaptureEnabled](./microsoft-edge-policies.md#webcaptureenabled) - Enable web capture feature in Microsoft Edge.

#### Deprecated Policy

[NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype) - Configure the Microsoft Edge new tab page experience.

#### Obsoleted Policy

[EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures) - Re-enable deprecated web platform features for a limited time.

<!-- end major 87 -->

## Version 86.0.622.69: November 13

> [!IMPORTANT]
> This update contains [CVE-2020-16013](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16013) and [CVE-2020-16017](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16017), that have been reported by the Chromium team as having an exploit in the wild.

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#november-13-2020).

## Version 86.0.622.68: November 11

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#november-11-2020)

## Version 86.0.622.63: November 4

> [!IMPORTANT]
> This update contains [CVE-2020-16009](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16009), that has been reported by the Chromium team as having an exploit in the wild.

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#november-4-2020).

## Version 86.0.622.61: November 2

Fixed various bugs and performance issues.

## Version 86.0.622.58: October 29

Fixed various bugs and performance issues.

## Version 86.0.622.56: October 27

Fixed various bugs and performance issues.

## Version 86.0.622.51: October 22

Stable channel security updates are listed [here](./microsoft-edge-relnotes-security.md#october-22-2020)

## Version 86.0.622.48: October 20

Fixed various bugs and performance issues.

## Version 86.0.622.43: October 15

Fixed various bugs and performance issues.

<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)