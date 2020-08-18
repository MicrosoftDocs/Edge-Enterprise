---
title: "Microsoft Edge configurations and experimentation"
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 02/20/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Microsoft Edge configurations and experimentation"
---

# Microsoft Edge configurations and experimentation

This article describes the interaction between Microsoft Edge and the Experimentation and Configuration Service (ECS). Microsoft Edge communicates with this service to request and receive different kinds of payloads. These payloads include configurations, feature rollouts, and experiments.

> [!IMPORTANT]
> Make sure clients are able to access `https://config.edge.skype.com` so payloads can be received.

> [!NOTE]
> This applies to Microsoft Edge version 77 or later.

## Configurations

Configurations are the payload meant to ensure product health, security, and privacy compliance, and are intended to have the same value for all the users (based on platforms and channels.) This could be to enable a feature flag for a domain action, and can also be used to disable a feature flag in the event of a bug.

## Controlled Feature Rollout

Controlled Feature Rollout (CFR) is a procedure for slowly increasing the size of the user group that receives a feature. By distributing a new feature to a randomly selected subset of the user population, it’s possible to compare user feedback to an equally sized control group without the feature to measure the impact of the feature.

## Experiments

Microsoft Edge builds have features and functionality that are still in development or are experimental. Experiments are like CFR, but the size of the user group is much smaller for testing the new concept. These features are hidden by default until the feature's rolled out or the experiment's finished. Experiment flags are used to enable and disable these features.

## About the ECS

In all the preceding scenarios, the service delivers the feature flag values to the browser client so they can be applied. Depending on the update, configurations are applied immediately or when the user restarts the browser.

Microsoft Edge's interaction with this service is controlled by settings in the [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol) policy. You can configure policy settings to:

- Retrieve configurations only
- Retrieve configurations and experiments
- Disable communication with the service

  > [!CAUTION]
  > If you disable communications with the service, this will affect Microsoft’s ability to respond to a severe bug in a timely manner.

## See also

- [Microsoft Edge Enterprise landing page](https://www.microsoftedgeinsider.com/enterprise)
- [Microsoft Edge documentation landing page](https://docs.microsoft.com/DeployEdge/)
