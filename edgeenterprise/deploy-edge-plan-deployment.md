---
title: "Plan your deployment of Microsoft Edge"
ms.author: cjacks
author: appcompatguy
manager: saudm
ms.date: 04/23/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Plan your deployment of Microsoft Edge"
---

# Plan your deployment of Microsoft Edge

This article describes the recommended practices for deploying Microsoft Edge in an enterprise environment.

>[!NOTE]
>This article applies to Microsoft Edge version 77 or later.

## Evaluate your existing browser environment and browser needs

Take time to understand your current browser state and project vision to ensure that all project stakeholders are aligned and working towards the same result.

Start by defining your current state:

- Which browsers are currently deployed in your environment?
- Which browser is set as the default browser?
- Do you need to use Internet Explorer for some of your apps?
- Do you use an Enterprise Mode Site List to configure Internet Explorer today?
- What OS platforms are supported in your environment? (Windows 10, macOS, Windows 7, Windows Server, etc.)
- What management tools do you use for browser management?
- Who is responsible for browser configuration and management?
- What is your process for validating browser compatibility?

After you understand the current state, you can determine the desired goals for your browser deployment, taking into account the following:

- Do you want to [set Microsoft Edge as your default browser](https://docs.microsoft.com/DeployEdge/edge-default-browser)?
- Do you want to hide the legacy version of Microsoft Edge, or do you want to [leave it available for users](https://docs.microsoft.com/DeployEdge/microsoft-edge-sysupdate-access-old-edge)?
- How will you [configure Microsoft Edge](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge)?
- What features are critical to configure as part of your initial deployment?
- What is the process for addressing any identified compatibility or configuration issues?

You should also understand the **pre-requisites** for features you're interested in, such as:

- [Windows Defender Application Guard](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-application-guard/reqs-wd-app-guard)
- [Internet Explorer mode](https://docs.microsoft.com/DeployEdge/edge-ie-mode)
- [Authentication and sync](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-identity)

With these answers in mind, you're ready to planning your Microsoft Edge deployment.
<!--bookmark -->
## Determine your deployment methodology

After you know your desired end state, you're ready to start planning how to get there. The two main ways to deploy Microsoft Edge are by role, and by site.

### Deploy to end users by role

If app compatibility is your main concern, and you don't have a firm grasp on which apps to test, you might want to consider deploying to end users by role. This enables each wave of a phased deployment to provide feedback and insights on apps that might need to have their configuration modified to address compatibility issues.

### Deploy to end users by site

If bandwidth is your primary concern, you might want to consider doing application compatibility testing up front. After you finish testing, deploy to end users by site so you can leverage caching other software delivery optimizations.

## Do site discovery

If you have a dependency on legacy web applications, and plan to use Internet Explorer mode (which most customers do), then you probably need to do some additional site discovery.

### If you've already deployed and configured the legacy version of Microsoft Edge

If you've already configured your Enterprise Site List to work for the legacy version of Microsoft Edge, then your work is almost done! The one thing you may need to add are neutral sites.

Neutral sites are typically sites that provide Single Sign-On (SSO). If you navigate to a neutral site from Microsoft Edge, then you want to stay in Microsoft Edge to authenticate. If navigate to a neutral site in Internet Explorer mode, then you want to stay in Internet Explorer mode to authenticate.

Identify any SSO (or other neutral) sites that you use and add these to your Enterprise Site List.

### If you've configured Internet Explorer as your default browser

If you're currently only using Internet Explorer, you might not know which sites have upgraded to modern web standards and which still require Internet Explorer. You want to find these sites and add them to the Enterprise Site List. This lets you use Internet Explorer mode only on the sites that need it.

> [!TIP]
> Use the [Enterprise Site Discovery](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery?redirectedfrom=MSDN) tools to discover the sites that might need Internet Explorer mode. You can collect collect data on computers running Windows Internet Explorer 8 through Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7.

### Analyze site discovery data

After you've collected site data, we recommend the following 4-step process to analyze the data:

1. Sort the data by domain, and then by URL.
2. Define the boundaries of an "app" to configure for Internet Explorer mode. You want to include all the sites and web controls that define the app. But you don't want to include any extra sites and controls by defining the app too broadly. Some sites may be as simple as "http://contoso.com/app1" while others may require you to define multiple sites and pages.
3. Test the app to verify that it doesn't work natively. Many sites will offer modern content when they detect a modern browser, and only offer legacy content when they detect Internet Explorer.
4. Add the app to your Enterprise Site list if it fails testing.

   > [!NOTE]
   > As a best practice, group all of the sites that comprise an app. If the sites all need to be used to accomplish one task, and if they tend to be updated together, that is a good indication that they should be grouped. This way, when you upgrade an app, it's easier to remove the entire site from Internet Explorer mode and start using a modern browser for that app.

## Determine your channel strategy

Microsoft Edge is released in [multiple channels](https://docs.microsoft.com/DeployEdge/microsoft-edge-channels).

> [!NOTE]
> You can install more than one channel on a device

The Stable Channel is what you will want to deploy to most devices. However, you should consider a deployment strategy that includes multiple devices and multiple channels.

### Multiple devices and channels

We recommend having a representative subset of devices configured to use the Beta Channel. This lets you preview upcoming changes to the browser. You can see if these changes are going to affect your end users or apps.

You might also want to make the Dev Channel (or even the Canary Channel) available to some roles, such as web developers. Consider whether you would like to target some devices with more fluid and rapidly changing channels, or simply make these channels available for users to opt to install.

Because it's possible to install multiple channels on a device, you can mitigate the risk of testing for users who have opted to install a pre-release channel. For example, if you have a user who's using the Beta Channel, and there's a problem, they can switch to the Stable Channel and continue working. This unblocks them until the issue can be fixed.

> [!NOTE]
> If the user enabled Sync, then their configuration will sync across channels, making it even easier to transition between channels.

## Define and configure policies

After you've created your Enterprise Site List, we recommend identifying and configuring the policies that you intend to deploy with Microsoft Edge. This ensures that these policies are applied when you perform your testing.

First, consider the first-run experience you want your users to have. If you want to automatically import settings from the current browser, configure the policy for [AutoImportAtFirstRun](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoimportatfirstrun).

For security policies, we recommend starting with the Microsoft Edge Security Baseline. The Security Baseline can be applied using the [recommended security configuration baseline settings](https://techcommunity.microsoft.com/t5/Microsoft-Security-Baselines/Security-baseline-DRAFT-for-Chromium-based-Microsoft-Edge/ba-p/949991) or by using [Microsoft Intune](https://docs.microsoft.com/intune/protect/security-baseline-settings-edge).

For other policies, we recommend reviewing the policy configurations for [Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-policies) and [Microsoft Edge Updates](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies).

### Define your update strategy and policies

You also want to determine how you want to do updates after you deploy Microsoft Edge:

- **Allow Microsoft Edge to update itself** (default). If you choose to allow automatic updates of Microsoft Edge, then Microsoft Edge will automatically update itself at the pace determined by the channel(s) you deployed.
- **Update Microsoft Edge at your own pace**. If you prefer to have explicit control over when updates are deployed, you can disable automatic updates and deploy it yourself (see the [Update Policy reference](https://docs.microsoft.com/DeployEdge/microsoft-edge-update-policies).) After you disable automatic updates you can deploy updates for each channel using one of the following tools:

- [Intune](https://docs.microsoft.com/intune/apps/apps-windows-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json)
- [Configuration Manager](https://docs.microsoft.com/DeployEdge/deploy-edge-with-configuration-manager)
- the deployment tool of your choice.

Regardless of your update strategy, we recommend leveraging a ringed deployment strategy. With automatic updates, this means having a representative sample of users running the Beta Channel, to identify issues with what will become the Stable Channel. With manual updates, this might also include additional validation of a pilot group after a new Stable Channel build is released. This is followed by broad deployment.

>[!NOTE]
>Microsoft Edge support will only apply to the most recent version of Microsoft Edge in each channel

## Do app compatibility testing

Application compatibility for Microsoft Edge is extremely high - so high that Microsoft provides the following compatibility promises:

1. If it works on Microsoft Edge *version 45 and earlier*, it will work on Microsoft Edge *version 77 and later*.
2. If it works on Internet Explorer, it will work on Microsoft Edge in Internet Explorer mode.
3. If it works on Google Chrome, it will work on Microsoft Edge.

If you have an application where we don't meet this promise, then we stand behind the promise to fix it with [Microsoft App Assure](https://www.microsoft.com/fasttrack/microsoft-365/desktop-app-assure).

Despite this promise, we know that many organizations must validate some applications for their compliance or risk management reasons. Even though we expect this to be very straightforward, it's important to be organized and rigorous in app testing.

There are 2 ways to do app compatibility testing:

1. Lab testing. Applications are validated in a tightly controlled environment with specific configurations.
2. Pilot testing. Applications are validated by a limited number of users in their daily work environment using their own devices.

Choose the method that is most appropriate for each app,  to manage risk without over-investing in compatibility testing.

## Deploy Microsoft Edge to a pilot group

After you've defined your policies and have finished your initial app compatibility testing, you're ready to deploy to your pilot group. Deploy to your pilot group using one of the following tools:

- [Microsoft Intune for Windows](https://docs.microsoft.com/intune/apps/apps-windows-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json), or [Microsoft Intune for macOS](https://docs.microsoft.com/intune/apps/apps-edge-macos?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json)
- [Configuration Manager](https://docs.microsoft.com/DeployEdge/deploy-edge-with-configuration-manager).
- Another management tool, download and deploy the [MSI file for Microsoft Edge](https://www.microsoftedgeinsider.com/enterprise).

## Validate your deployment

After you deploy your pilot, you want to capture all the feedback you get from your users.

- Capture feedback on compatibility. Identify sites that belong on the Enterprise Site List that weren't identified during site discovery.
- Capture feedback on the policy configuration. Ensure that users can use key features and do their work while following security guidelines.
- Capture feedback on ease of use and new features. Identify any areas where training should be developed and delivered based on user questions.

## Broad deployment of Microsoft Edge

After a finishing the pilot and updating your deployment plan with lessons learned from the pilot, you're ready to do a full deployment of Microsoft Edge to all your users.  Congratulations!

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
- [Video - Deploy Microsoft Edge](microsoft-edge-video-deploy.md)
