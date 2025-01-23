---
title: Checkpoint cumulative updates and the Microsoft Update Catalog
description: This article describes how to handle checkpoint cumulative updates when you use the Microsoft Update Catalog to update devices and images.
ms.service: windows-client
ms.subservice: itpro-updates
ms.topic: conceptual
ms.author: mstewart
author: mestew
manager: aaroncz
ms.collection:
  - tier2
ms.localizationpriority: medium
appliesto: 
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11, version 24H2 and later</a>
ms.date: 01/23/2025
---

# Checkpoint cumulative updates and Microsoft Update Catalog usage

Starting Windows 11, version 24H2, monthly security updates and optional nonsecurity preview release updates may be preceded by a checkpoint cumulative update (CU). Devices (and images) updating from Windows Update (WU) and Windows Server Update Services (WSUS) release channels can continue to seamlessly install the latest monthly security update or the optional nonsecurity preview release regardless of whether there are any preceding checkpoint CUs, so update processes involving WU and WSUS remain unchanged. This article covers how Catalog users can easily update their devices (or images) through checkpoint CUs.

## Checkpoint CUs

Windows 11 quality updates use servicing technology and are built cumulatively from the time when a new Windows OS was "released to manufacturing" (RTM). These monthly updates include all the changes since RTM in the form of binary differentials computed from the initial version of those binaries.

With Windows 11, version 24H2, Microsoft introduced a new concept of checkpoint cumulative updates. This will allow you to get features and security enhancements via the latest cumulative update through smaller, incremental differentials containing only the changes since the previous checkpoint cumulative update. This means that you can save time, bandwidth, and hard drive space.

Going forward, Microsoft might periodically release cumulative updates as checkpoints. The subsequent updates will then consist of:
- The update package files associated with the checkpoints, and
- New update package files that contain incremental binary differentials against the version of binaries in the last checkpoint.

This process may be repeated multiple times, thereby generating multiple checkpoints during the lifecycle of a given Windows release. The Windows 11, version 24H2 servicing stack can merge all the checkpoints and only download and install content that's missing on the device.

If any checkpoint CUs precede a target update, a device or image needs to take all prior checkpoint CUs before it can take the target update. In other words, a post-checkpoint LCU can be applied to images/devices that are on that checkpoint or on a subsequent LCU. For updates sourced from WU and WSUS this happens seamlessly, and you can continue to use the same tools and processes that you currently use for approving and deploying updates.

### Applicability

A checkpoint CU is just another monthly security update that informs how subsequent updates are built. There is no policy change or new requirement around when users must take these updates, though it is best practice to take monthly security updates at the earliest opportunity to keep your devices protected and productive.

This feature does not introduce any change to the applicability of monthly security updates. As before, these updates apply to the main OS (install.wim) and to WinPE (boot.wim) but not to WinRE (winre.wim).

WinRE is serviced by applying the servicing stack update (SSU) from OnePackage (LCU does not apply) and SafeOS DU. This is how it has been for a while now, and there is no recent change to WinRE servicing and certainly no change due to the checkpoint cumulative updates feature. We understand that not everybody may have had a shared understanding about this, but applying SSU then SafeOS DU is the only way to ensure WinRE is serviced. For more information, see [Update Windows installation media with Dynamic Update](media-dynamic-update.md).

### Current Checkpoint CUs
 
For Windows 11, version 24H2 and above, for a given update the KB article will note all preceding checkpoint CUs under the **Catalog** release channel tab. We expect that your experience updating through a checkpoint CU will position you to efficiently take future checkpoint CUs.

## Updating from the Microsoft Update Catalog

When installing a given monthly security or optional nonsecurity preview update, [Microsoft Update Catalog](https://www.catalog.update.microsoft.com) users can determine and download the prior checkpoint CUs and apply these sequentially under certain situations or in one go using DISM.

### Finding prior Checkpoint CUs

For a given update, users can look up the KB article and find all preceding checkpoints, if any, listed under the **Catalog** release channel. For instance, the 2024-12 monthly security update (KB5048667) has one preceding checkpoint CU per [December 10, 2024—KB5048667 (OS Build 26100.2605)](https://support.microsoft.com/topic/708755a6-d809-4a8a-8d20-53c4108590e6#ID0ELBD=Catalog):


|&nbsp|
|---|
|<b>Method 2: Install each MSU file individually, in order</b> <p>Download and install each MSU file individually either using DISM or [Windows Update Standalone Installer](https://support.microsoft.com/topic/799ba3df-ec7e-b05e-ee13-1cdae8f23b19) in the following order: <ul><li> windows11.0-kb5043080-x64_953449672073f8fb99badb4cc6d5d7849b9c83e8.msu </li> <li>windows11.0-kb5048667-x64_d4ad0ca69de9a02bc356757581e0e0d6960c9f93.msu </li></ul>|

> <b>Method 2: Install each MSU file individually, in order</b> <p>Download and install each MSU file individually either using DISM or [Windows Update Standalone Installer](https://support.microsoft.com/topic/799ba3df-ec7e-b05e-ee13-1cdae8f23b19) in the following order: <ul><li> windows11.0-kb5043080-x64_953449672073f8fb99badb4cc6d5d7849b9c83e8.msu </li> <li>windows11.0-kb5048667-x64_d4ad0ca69de9a02bc356757581e0e0d6960c9f93.msu </li></ul>