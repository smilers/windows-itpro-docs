---
title: Microsoft Connected Cache for Enterprise and Education troubleshooting
description: Details on how to troubleshoot common issues for Microsoft Connected Cache for Enterprise.
ms.service: windows-client
ms.subservice: itpro-updates
ms.topic: how-to
manager: naengler
ms.author: lichris
author: chrisjlin
appliesto: 
- ✅ <a href=https://learn.microsoft.com/windows/release-health/supported-versions-windows-client target=_blank>Windows 11</a>
- ✅ Supported Linux distributions
- ✅ <a href=https://learn.microsoft.com/windows/deployment/do/waas-microsoft-connected-cache target=_blank>Microsoft Connected Cache for Enterprise</a>	
ms.date: 10/30/2024
---


# Troubleshoot Microsoft Connected Cache for Enterprise and Education

This article contains instructions on how to troubleshoot different issues you may encounter while using Connected Cache. These issues are categorized by the task in which they may be encountered.

## Steps to obtain an Azure subscription ID

<!--Using include file, get-azure-subscription.md, do/mcc-isp.md for shared content-->
[!INCLUDE [Get Azure subscription](includes/get-azure-subscription.md)]

## Troubleshooting Azure resource creation

[Connected Cache Azure resource creation](mcc-ent-create-resource-and-cache.md) can be initiated using either the Azure portal user interface or the Azure CLI command set.

If you're encountering an error during resource creation, check that you have the necessary permissions to create Azure resources under your subscription and have filled out all required fields during the resource creation process.

## Troubleshooting cache node configuration

[Configuration of your Connected Cache node](mcc-ent-create-resource-and-cache.md) can be done using either the Azure portal user interface or the Azure CLI command set.

If you're encountering a validation error, check that you have filled out all required configuration fields.

If your configuration doesn't appear to be taking effect, check that you have selected the **Save** option at the top of the configuration page in the Azure portal user interface.

If you have changed the proxy configuration, you will need to re-provision the Connected Cache software on the host machine for the proxy configuration to take effect.

## Troubleshooting cache nodes created during early preview

Cache nodes created and deployed during the [Microsoft Connected Cache for Enterprise and Education early preview](mcc-ent-early-preview.md) should continue to function but can no longer be managed or monitored remotely via the Connected Cache Azure service.

As such, we strongly recommend you [recreate your existing resources in Azure](mcc-ent-create-resource-and-cache.md) and then [redeploy the Connected Cache software to your host machines](mcc-ent-deploy-to-windows.md) using the latest OS-specific installer.

## Troubleshooting cache node deployment to Windows host machine

### Collecting Windows-hosted installation logs

[Deploying a Connected Cache node to a Windows host machine](mcc-ent-deploy-to-windows.md) involves running a series of PowerShell scripts contained within the Windows provisioning package. These scripts will attempt to write log files to the installation directory specified in the provisioning command (`C:\mccwsl01\InstallLogs` by default).

There are three types of installation log files:

1. **WSL_Mcc_Install_Transcript**: This log file records the lines printed to the PowerShell window when running the installation script
1. **WSL_Mcc_Install_FromRegisteredTask_Status**: This log file records the high level status that is written during the registered tasks install
1. **WSL_Mcc_Install_FromRegisteredTask_Transcript**: This log file records the detailed status that is written during the registered tasks install

The Registered Task Transcript is usually the most useful for diagnosing the installation issue.

### WSL2 fails to install with message "A specified logon session does not exist"

If you are encountering this failure message when attempting to run the PowerShell command `wsl.exe --install --no-distribution` on your Windows host machine, verify that you are logged on as a local administrator and running the command from an elevated PowerShell window.

### Updating the WSL2 kernel

If the Connected Cache installation is failing due to WSL-related issues, try running `wsl.exe --update` to get the latest version of the WSL kernel.

### Checking if the Connected Cache container is running

Once the Connected Cache software has been successfully deployed to the Windows host machine, you can check if the cache node is running properly by doing the following on the Windows host machine:

1. Launch a PowerShell process as the account specified as the runtime account during the Connected Cache install
1. Run `wsl -d Ubuntu-22.04-Mcc-Base` to access the Linux distribution that hosts the Connected Cache container
1. Run `sudo iotedge list` to show which containers are running within the IoT Edge runtime

If it shows the **edgeAgent** and **edgeHub** containers but doesn't show **MCC**, you can view the status of the IoT Edge security manager using `sudo iotedge system logs -- -f`.

You can also reboot the IoT Edge runtime using `sudo systemctl restart iotedge`.

### Checking Connected Cache scheduled tasks

Once the Connected Cache container is running, a scheduled task is periodically run under the Connected Cache runtime account to keep WSL from cleaning up the Connected Cache container.

You can use Task Scheduler on the host machine to check the status of this scheduled task.

1. Open Task Scheduler on the host machine
1. Navigate to the Active Tasks section and double-click on **MCC_Monitor_Task**
1. Select the scheduled task **MCC_Monitor_Task**
1. Select the **Triggers** tab and confirm that the Status is **Enabled**

> [!Note]
> If the password of the runtime account changes, you'll need to update the user in all of the Connected Cache scheduled tasks in order for the Connected Cache node to continue functioning properly.

## Troubleshooting cache node deployment to Linux host machine

[Deploying a Connected Cache node to a Linux host machine](mcc-ent-deploy-to-linux.md) involves running a series of Bash scripts contained within the Linux provisioning package.

Once the Connected Cache software has been successfully deployed to the Linux host machine, you can check if the cache node is running properly by doing the following on the Linux host machine:

1. Run `sudo iotedge list` to show which containers are running within the IoT Edge runtime

If it shows the **edgeAgent** and **edgeHub** containers but doesn't show **MCC**, you can view the status of the IoT Edge security manager using `sudo iotedge system logs -- -f`.

You can also reboot the IoT Edge runtime using `sudo systemctl restart iotedge`.

## Troubleshooting cache node monitoring

Connected Cache node status and performance can be [monitored using the Azure portal user interface](mcc-ent-monitoring.md).

If the [basic monitoring](mcc-ent-monitoring.md#basic-monitoring) visuals on the Overview tab are showing unexpected or erroneous values, refresh the browser window.

If the issue persists, check that you have configured the Timespan and Cache node filters as desired.

## Diagnose and Solve

You can also use the **Diagnose and solve problems** functionality provided by the Azure portal interface. This tab within the Microsoft Connected Cache Azure resource will walk you through a few prompts to help narrow down the solution to your issue.
