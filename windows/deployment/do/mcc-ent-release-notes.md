---
title: Microsoft Connected Cache Release Notes
description: Release Notes for Microsoft Connected Cache for Enterprise and Education.
ms.service: windows-client
ms.subservice: itpro-updates
ms.topic: conceptual
ms.author: lichris
author: chrisjlin
manager: naengler
appliesto: 
- ✅ <a href=https://learn.microsoft.com/windows/release-health/supported-versions-windows-client target=_blank>Windows 11</a>
- ✅ Supported Linux distributions
- ✅ <a href=https://learn.microsoft.com/windows/deployment/do/waas-microsoft-connected-cache target=_blank>Microsoft Connected Cache for Enterprise and Education</a>	
ms.date: 10/30/2024
---

# Release Notes for Microsoft Connected Cache for Enterprise and Education

This article contains details about the latest releases of Connected Cache. Since Connected Cache is a preview service, some releases may contain breaking changes.

## Install script v2.0.0.2

Released on **2/5/2025**

These changes only affect the installation scripts for Connected Cache. To take advantage of these changes, you will need to re-deploy your existing cache nodes using the updated installation script.

### Improvements

- **Removes dependency on AMQP/MQTT ports**: Cache nodes deployed using this updated installation script will no longer use AMQP (5671) or MQTT (8883) ports. This change simplifies the network configuration for cache nodes and reduces the number of ports that need to be opened in your network security group.
- **Improves cleanup during uninstall**: Windows-hosted cache nodes will now remove port proxy rules when uninstalled using the `uninstallmcconwsl.ps1` script. This change ensures that the host machine's WSL port-forwarding rules are cleaned up properly when uninstalling Connected Cache.
- **Changes install error codes from decimal to hex code**: Install error codes for Windows-hosted cache nodes are now displayed in hex code format, improving error code readability.
- **Uses configured proxy to perform install**: If a proxy was configured for the Windows-hosted cache node in Azure Portal, the cache node will use the specified proxy during installation.

## Release v1.2.1.2076_E (public preview launch)

The public preview released on **10/30/2024**

For customers that installed earlier versions of Connected Cache, this release contains breaking changes that affect both Linux and Windows host machines. Please see the [early preview documentation page](mcc-ent-early-preview.md) for more details.

### Feature updates

- **Metrics and charts in Azure portal**: You can now visualize *Outbound egress* and *Volume by Content type* charts for your cache node on Azure portal. You can also create custom monitoring charts for your cache nodes. This capability is under the **Metrics** tab on Azure portal.
- **Cache nodes for Windows or Linux host machines**: Cache nodes can now be created and deployed to Windows host machine or Linux host machines by simply choosing the OS when creating cache nodes.
- **Ubuntu 22.04 LTS**: Cache nodes can now be deployed on Ubuntu 22.04 LTS.
- **Azure CLI support**: Cache nodes can now be created and managed via Azure CLI.
- **Proxy**: We added support for unauthenticated proxy and cloud proxy integration.
- **Updates**: Your cache nodes are now updated automatically and we also added the capability to set each cache node's update ring to govern the cadence of Microsoft Connected Cache container updates.

### Fixes
- We fixed various bugs to achieve a smoother installation experience.

## Related content

- [Overview of Connected Cache](mcc-ent-edu-overview.md)
