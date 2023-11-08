---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: archandr
author: dan-wesley
manager: likuba
ms.date: 11/08/2023
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: "Microsoft Edge release notes for Beta Channel"
---

# Release notes for Microsoft Edge Beta Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Beta Channel. Archived versions of these release notes are available at [Archived release notes for Microsoft Edge Beta Channel](./microsoft-edge-relnote-archive-beta-channel.md).

> [!NOTE]
> Microsoft Edge Web Platform constantly evolves to improve user experience, security, and privacy. To learn more, see [Site compatibility-impacting changes coming to Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).

## Version 120.0.xxxx.x: November x, 2023

Fixed various bugs and performance issues.

### Feature updates

- **RendererAppContainer.** For additional security benefits, the Windows native app container is enabled by default. **Note:** If Enterprise organizations identify a compatibility issue due to code injection from security software, they should follow up with the software vendor directly and/or use the [RendererAppContainerEnabled](/deployedge/microsoft-edge-policies#rendererappcontainerenabled) policy to trade-off the security benefits in Microsoft Edge with their other software.

- **Microsoft Edge migrates the updates experience into Browser Essentials.** Getting alerts on available Edge Updates will come from Browser Essentials instead of the Settings page for better visibility and experience. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

- **Updated SmartActionsBlockList Policy.**  The [SmartActionsBlockList](/deployedge/microsoft-edge-policies#smartactionsblocklist) policy has been updated with new policy option mappings.  Administrators can now configure the policy to control Smart actions like definitions on websites (smart_actions_website) or control Smart actions in pdfs and on websites (smart_actions).

- **Edge Workspaces improvements for offline functionality.**  Any workspace opened on a device previously will be cached locally and will be able to be opened on that device from that cache even if it fails to connect. Changes will persist on that device and be resolved into the synced version when a connection can finally be made. **Note:** This feature is a controlled feature rollout. If you don't see this feature, check back as we continue our rollout.

### Policy updates

#### New policies

- [AutoDiscardSleepingTabsEnabled](/deployedge/microsoft-edge-policies#autodiscardsleepingtabsenabled) - Configure auto discard sleeping tabs
- [AutomaticProfileSwitchingSiteList](/deployedge/microsoft-edge-policies#automaticprofileswitchingsitelist) - Configure the automatic profile switching site list
- [Edge3PSerpTelemetryEnabled](/deployedge/microsoft-edge-policies#edge3pserptelemetryenabled) - Edge 3P SERP Telemetry Enabled
- [WebAppSettings](/deployedge/microsoft-edge-policies#webappsettings) - Web App management settings

## Version 119.0.2151.44: November 2, 2023

Fixed various bugs and performance issues.

## Version 119.0.2151.42: November 1, 2023

Fixed various bugs and performance issues.

## Version 119.0.2151.38: October 30, 2023

Fixed various bugs and performance issues.

## Version 119.0.2151.32: October 27, 2023

Fixed various bugs and performance issues.

## Version 119.0.2151.30: October 26, 2023

Fixed various bugs and performance issues.

## Version 119.0.2151.24: October 23, 2023

Fixed various bugs and performance issues.

## Version 119.0.2151.12: October 17, 2023

Fixed various bugs and performance issues.

### Feature updates

- **Behavioral changes to the beforeunload event.** The behavior of the beforeunload event has changed such that calling preventDefault in a beforeunload event handler triggers a confirmation dialog. Setting returnValue to an empty string in a beforeunload event handler no longer triggers a confirmation dialog. This behavior takes effect starting in Microsoft Edge version 119. Administrators can temporarily opt out of this functionality by disabling the [BeforeunloadEventCancelByPreventDefaultEnabled](/deployedge/microsoft-edge-policies#beforeunloadeventcancelbypreventdefaultenabled) policy.

- **Split screen restore improvements.** Split screen allows you to simultaneously work on multiple tasks across two, side-by-side screens in one browsing tab to boost your productivity and multitask more efficiently. Now after the browser is restarted and the previous session is restored, the split tab will also be restored.

- **Additional capability to manage sidebar apps.** Administrators can utilize the "sidebar_auto_open_blocked" [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) policy field to control the auto-open behavior of sidebar apps.  For more information, see [Detailed guide to the ExtensionSettings](/deployedge/microsoft-edge-manage-extensions-ref-guide) policy.

- **Updates to Microsoft Edge enterprise sync settings page.** When the [ForceSyncTypes](/deployedge/microsoft-edge-policies#forcesynctypes) and [SyncTypesListDisabled](/deployedge/microsoft-edge-policies#synctypeslistdisabled) polices are used concurrently, the sync settings page (`edge://settings/profiles/sync`) accurately show the status for each data type.

### Policy updates

#### New policies

- [SwitchIntranetSitesToWorkProfile](/deployedge/microsoft-edge-policies#switchintranetsitestoworkprofile) - Switch intranet sites to a work profile
- [SwitchSitesOnIEModeSiteListToWorkProfile](/deployedge/microsoft-edge-policies#switchsitesoniemodesitelisttoworkprofile) - Switch sites on the IE mode site list to a work profile
- [OrganizationLogoOverlayOnAppIconEnabled](/deployedge/microsoft-edge-policies#organizationlogooverlayonappiconenabled) - Allow your organization's logo from M365 to be overlaid on the Microsoft Edge app icon of a work profile
- [OrganizationalBrandingOnWorkProfileUIEnabled](/deployedge/microsoft-edge-policies#organizationalbrandingonworkprofileuienabled) - Allow the use of your organization's branding assets from M365 on the profile-related UI of a work profile

## Version 118.0.2088.46: October 13, 2023

Fixed various bugs and performance issues.

## Version 118.0.2088.44: October 12, 2023

Fixed various bugs and performance issues.

## Version 118.0.2088.41: October 10, 2023

Fixed various bugs and performance issues.

## Version 118.0.2088.33: October 6, 2023

Fixed various bugs and performance issues.

## Version 118.0.2088.27: October 3, 2023

Fixed various bugs and performance issues.

## Version 118.0.2088.24: October 2, 2023

Fixed various bugs and performance issues.

## Version 118.0.2088.17: September 25, 2023

Fixed various bugs and performance issues.

<!-- Version 118.0.2088.11: September 20, 2023 to Version 117.0.2045.12: August 29, 2023 -->
<!-- Version 117.0.2045.9: August 25, 2023 to Version 116.0.1938.36: July 31, 2023 -->
<!-- Version 116.0.1938.29: July 24, 2023 to Version 115.0.1901.9: June 15, 2023 -->
<!-- from Version 115.0.1901.7: June 13, 2023 to Version 114.0.1823.18: May 15, 2023 -->
<!-- Version 114.0.1823.11: May 9, 2023 to Version 113.0.1774.15: April 18, 2023 -->
<!-- Version 113.0.1774.9: April 12, 2023 to Version 112.0.1722.15: March 21, 2023 -->
<!-- from Version 112.0.1722.11: March 17, 2023 to Version 111.0.1661.22: February 24, 2023 -->
<!-- from Version 111.0.1661.15: February 16, 2023 to Version 110.0.1587.22: January 24, 2023 -->
<!--- from Version 110.0.1587.17: January 20, 2023 to Version 109.0.1518.23: December 14, 2022 -->
<!--- from Version 109.0.1518.14: December 7, 2022 to Version 108.0.1462.20: November 14, 2022 -->
<!--- from Version 108.0.1462.15: November 10, 2022 to Version 107.0.1418.13: October 18, 2022 -->
<!--- from Version 107.0.1418.8: October 13, 2022 to Version 106.0.1370.17: September 16, 2022 -->
<!-- from Version 106.0.1370.15: September 15, 2022 to Version Version 105.0.1343.10: August 19, 2022 ---->
<!--- from Version 105.0.1343.7: August 16, 2022 to Version 104.0.1293.21: July 14 ---->
<!--- from Version 104.0.1293.14: July 7 to Version 103.0.1264.17: June 6 ---->
<!--- from Version 103.0.1264.13: June 2 to Version 102.0.1245.12: May 13 ---->
<!--- from Version 102.0.1245.7: May 10 to Version 101.0.1210.14: April 12 ---->
<!--- from Version 101.0.1210.10: April 8 to Version 100.0.1185.12: March 18 --->
<!--- from Version 100.0.1185.10: March 17 to Version 99.0.1150.16: February 14 --->
<!--- From Version 99.0.1150.11: February 9 to Version 98.0.1108.27: January 19 --->
<!-- archive from Version 98.0.1108.23: January 14 to Version 97.0.1072.28: December 8 -->
<!--- Version 97.0.1072.21: December 1 to Version 96.0.1054.13: November 5  --->
<!--- archive from Version 96.0.1054.8: November 1 to Version 95.0.1020.14: October 5  --->
<!-- archive from version 95.0.1020.9: September 28 to version 94.0.992.14: September 7 -->
<!-- archive from Version 94.0.992.9: September 2 to Version 92.0.902.40: July 6 -->
<!--Archive from Version 92.0.902.22: June 21 to Version 89.0.774.23: February 8  -->
<!-- Archive from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 --->
<!-- Archive from Version 87.0.664.12: October 20 to version 86.0.622.15: September 14 -->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
