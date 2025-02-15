---
title: Roles and responsibilities
description: This article describes the roles and responsibilities provided by Windows Autopatch and what the customer must do
ms.date: 07/08/2024
ms.service: windows-client
ms.subservice: autopatch
ms.topic: concept-article
ms.localizationpriority: medium
author: tiaraquan
ms.author: tiaraquan
manager: aaroncz
ms.reviewer: hathind
ms.collection:
  - highpri
  - tier1
---

# Roles and responsibilities

This article outlines your responsibilities and Windows Autopatch's responsibilities when:

- [Preparing to activate Windows Autopatch features](#prepare)
- [Deploying the service](#deploy)
- [Operating with the service](#manage)

## Prepare

| Task | Your responsibility | Windows Autopatch |
| ----- | :-----: | :-----: |
| Review the [prerequisites](../prepare/windows-autopatch-prerequisites.md) | :heavy_check_mark: | :x: |
| Review the [FAQ](../overview/windows-autopatch-faq.yml) | :heavy_check_mark: | :x: |
| [Review the service data platform and privacy compliance details](../overview/windows-autopatch-privacy.md) | :heavy_check_mark: | :x: |
| Consult the [Deployment guide](../overview/windows-autopatch-deployment-guide.md) | :heavy_check_mark: | :x: |
| Ensure device [prerequisites](../prepare/windows-autopatch-prerequisites.md) are met and in place prior to feature activation | :heavy_check_mark: | :x: |
| Ensure [infrastructure and environment prerequisites](../prepare/windows-autopatch-configure-network.md) are met and in place before feature activation | :heavy_check_mark: | :x: |
| Prepare to remove your devices from existing unsupported [Windows update](../references/windows-autopatch-windows-update-unsupported-policies.md) and [Microsoft 365](../references/windows-autopatch-microsoft-365-policies.md) policies | :heavy_check_mark: | :x: |
| [Configure required network endpoints](../prepare/windows-autopatch-configure-network.md#required-microsoft-product-endpoints) | :heavy_check_mark: | :x: |
| [Activate Windows Autopatch features](../prepare/windows-autopatch-feature-activation.md) | :heavy_check_mark: | :x: |
| Identify stakeholders for deployment communications | :heavy_check_mark: | :x: |

For more information and assistance with preparing for your Windows Autopatch deployment journey, see [Need additional guidance](../overview/windows-autopatch-deployment-guide.md#need-additional-guidance).

## Deploy

| Task | Your responsibility | Windows Autopatch |
| ----- | :-----: | :-----: |
| [Add and verify admin contacts](../deploy/windows-autopatch-admin-contacts.md) in Microsoft Intune |  :heavy_check_mark: | :x: |
| [Deploy and configure Windows Autopatch service configuration](../references/windows-autopatch-changes-made-at-feature-activation.md) | :x: | :heavy_check_mark: |
| Educate users on the Windows Autopatch end user update experience<ul><li>[Windows quality update end user experience](../manage/windows-autopatch-windows-quality-update-end-user-exp.md)</li><li>[Windows feature update end user experience](../manage/windows-autopatch-manage-windows-feature-update-releases.md)</li><li>[Microsoft 365 Apps for enterprise end user experience](../manage/windows-autopatch-microsoft-365-apps-enterprise.md#end-user-experience)</li><li>[Microsoft Edge end user experience](../manage/windows-autopatch-edge.md)</li><li>[Microsoft Teams end user experience](../manage/windows-autopatch-teams.md#end-user-experience)</li></ul> | :heavy_check_mark: | :x: |
| Review network optimization<ul><li>[Prepare your network](../prepare/windows-autopatch-configure-network.md)</li><li>[Delivery Optimization](../prepare/windows-autopatch-configure-network.md#delivery-optimization) | :heavy_check_mark: | :x: |
| Review existing configurations<ul><li>Remove your devices from existing unsupported [Windows Update](../references/windows-autopatch-windows-update-unsupported-policies.md) and [Microsoft 365](../references/windows-autopatch-microsoft-365-policies.md) policies</li><li>Consult [General considerations](../overview/windows-autopatch-deployment-guide.md#general-considerations)</li></ul>|  :heavy_check_mark: | :x: |
| Confirm your update service needs and configure your workloads<ul><li>[Allow or block Microsoft 365 Apps for enterprise updates](../manage/windows-autopatch-microsoft-365-apps-enterprise.md#allow-or-block-microsoft-365-app-updates)</li><li>[Manage driver and firmware updates](../manage/windows-autopatch-manage-driver-and-firmware-updates.md)</li><li>[Customize Windows Update settings](../manage/windows-autopatch-customize-windows-update-settings.md)</li><li>Decide your [Windows feature update versions(s)](../manage/windows-autopatch-windows-feature-update-overview.md)</li></ul>| :heavy_check_mark: | :x: |
| [Consider your Autopatch groups distribution](../deploy/windows-autopatch-groups-overview.md)<ul><li>[Create an Autopatch group](../manage/windows-autopatch-manage-autopatch-groups.md#create-an-autopatch-group)</li></ul> | :heavy_check_mark: | :x: |
| [Register devices](../deploy/windows-autopatch-register-devices.md)<ul><li>[Review your device registration options](../deploy/windows-autopatch-device-registration-overview.md)</li><li>[Register your first devices](../deploy/windows-autopatch-register-devices.md) | :heavy_check_mark: | :x: |
| [Review devices report](../deploy/windows-autopatch-register-devices.md#devices-report) | :x: | :heavy_check_mark: |
| Automatically assign devices to deployment rings at device registration<ul><li>[Windows Autopatch group deployment rings](../deploy/windows-autopatch-groups-overview.md#autopatch-group-deployment-rings)</li></ul>| :x: | :heavy_check_mark: |
| Remediate registration issues<ul><li>[For devices displayed in the **Not ready** tab](../deploy/windows-autopatch-post-reg-readiness-checks.md#devices-blade-registered-and-not-registered-tabs)</li><li>[For devices displayed in the **Not registered** tab](../deploy/windows-autopatch-post-reg-readiness-checks.md#devices-blade-registered-and-not-registered-tabs)</li><li>[For devices with conflicting configurations](../references/windows-autopatch-conflicting-configurations.md)</li></ul> | :heavy_check_mark: | :x: |
| Populate the Test and Last deployment ring membership<ul><li>[Windows Autopatch group deployment rings](../deploy/windows-autopatch-groups-overview.md#autopatch-group-deployment-rings)</li></ul> | :heavy_check_mark: | :x: |
| [Manually override device assignments to deployment rings](../deploy/windows-autopatch-register-devices.md#move-devices-in-between-deployment-rings) | :heavy_check_mark: | :x: |
| Review device conflict scenarios<ul><li>[Device conflict in deployment rings within an Autopatch group](../manage/windows-autopatch-manage-autopatch-groups.md#device-conflict-in-deployment-rings-within-an-autopatch-group)</li><li>[Device conflict across different Autopatch groups](../manage/windows-autopatch-manage-autopatch-groups.md#device-conflict-across-different-autopatch-groups)</li></ul> | :heavy_check_mark: | :x: |
| Communicate to end-users, help desk and stakeholders | :heavy_check_mark: | :x: |

## Manage

| Task | Your responsibility | Windows Autopatch |
| ----- | :-----: | :-----: |
| [Maintain contacts in the Microsoft Intune admin center](../deploy/windows-autopatch-admin-contacts.md) | :heavy_check_mark: | :x: |
| [Maintain and manage the Windows Autopatch service configuration](../monitor/windows-autopatch-maintain-environment.md) | :x: | :heavy_check_mark: |
| [Maintain customer configuration to align with the Windows Autopatch service configuration](../monitor/windows-autopatch-maintain-environment.md) | :heavy_check_mark: | :x: |
| Resolve service remediated device conflict scenarios<ul><li>[Device conflict in deployment rings within an Autopatch group](../manage/windows-autopatch-manage-autopatch-groups.md#device-conflict-in-deployment-rings-within-an-autopatch-group)</li></ul> | :x: | :heavy_check_mark: |
| Resolve remediated device conflict scenarios<ul><li>[Device conflict across different Autopatch groups](../manage/windows-autopatch-manage-autopatch-groups.md#device-conflict-across-different-autopatch-groups)</li><li>[Device conflict prior to device registration](../manage/windows-autopatch-manage-autopatch-groups.md#device-conflict-before-device-registration)</li></ul> |  :heavy_check_mark: | :x: |
| Maintain the Test and Last deployment ring membership<ul><li>[Windows Autopatch deployment rings](../deploy/windows-autopatch-groups-overview.md#autopatch-group-deployment-rings)</li></ul> | :heavy_check_mark: | :x: |
| [Define and implement service default release schedule](../manage/windows-autopatch-windows-quality-update-overview.md) | :x: | :heavy_check_mark: |
| Maintain your workload configuration and custom release schedule<ul><li>[Manage driver and firmware updates](../manage/windows-autopatch-manage-driver-and-firmware-updates.md)</li><li>[Customize Windows Update settings](../manage/windows-autopatch-customize-windows-update-settings.md)</li><li>[Decide your Windows feature update version(s)](../manage/windows-autopatch-windows-feature-update-overview.md)</li></ul> | :heavy_check_mark: | :x: |
| Communicate the update [release schedule](../manage/windows-autopatch-windows-quality-update-communications.md) to IT admins | :x: | :heavy_check_mark: |
| Release updates (as scheduled)<ul><li>[Windows quality updates](../manage/windows-autopatch-windows-quality-update-overview.md)</li><li>[Windows feature updates](../manage/windows-autopatch-windows-feature-update-overview.md)</li><li>[Microsoft 365 Apps for enterprise](../manage/windows-autopatch-microsoft-365-apps-enterprise.md#update-release-schedule)</li><li>[Microsoft Edge](../manage/windows-autopatch-edge.md#update-release-schedule)</li><li>[Microsoft Teams](../manage/windows-autopatch-teams.md#update-release-schedule)</li><ul>| :x: | :heavy_check_mark: |
| [Release updates](../manage/windows-autopatch-windows-quality-update-overview.md) | :x: | :heavy_check_mark: |
| [Release updates (OOB)](../manage/windows-autopatch-windows-quality-update-overview.md#out-of-band-releases) | :x: | :heavy_check_mark: |
| Deploy updates to devices | :x: | :heavy_check_mark: |
| Monitor [Windows quality](../manage/windows-autopatch-windows-quality-update-overview.md) or [feature updates](../manage/windows-autopatch-windows-feature-update-overview.md) through the release cycle | :x: | :heavy_check_mark: |
| Review [release announcements](../manage/windows-autopatch-windows-quality-update-overview.md#) | :heavy_check_mark: | :x: |
| Review deployment progress using Windows Autopatch reports<ul><li>[Windows quality update reports](../monitor/windows-autopatch-windows-quality-and-feature-update-reports-overview.md#windows-quality-update-reports)</li><li>[Windows feature update reports](../monitor/windows-autopatch-windows-quality-and-feature-update-reports-overview.md#windows-feature-update-reports)</li></ul> | :heavy_check_mark: | :x: |
| [Pause updates (initiated by you)](../manage/windows-autopatch-windows-quality-update-overview.md#pause-and-resume-a-release) | :heavy_check_mark: | :x: |
| Run [ongoing post-registration device readiness checks](../deploy/windows-autopatch-post-reg-readiness-checks.md) | :x: | :heavy_check_mark: |
| Maintain existing configurations<ul><li>Remove your devices from existing and unsupported [Windows update](../references/windows-autopatch-windows-update-unsupported-policies.md) and [Microsoft 365](../references/windows-autopatch-microsoft-365-policies.md) policies</li><li>Consult [General considerations](../overview/windows-autopatch-deployment-guide.md#general-considerations)</ul> | :heavy_check_mark: | :x: |
| Understand the health of [Up to date](../monitor/windows-autopatch-windows-quality-and-feature-update-reports-overview.md#up-to-date-devices) devices and investigate devices that are<ul><li>[Not up to date](../monitor/windows-autopatch-windows-quality-and-feature-update-reports-overview.md#not-up-to-date-devices)</li><li>[Not ready](../monitor/windows-autopatch-windows-quality-and-feature-update-reports-overview.md#not-ready-devices)</li><li>have [Device alerts](../monitor/windows-autopatch-device-alerts.md)</li><li>have [conflicting configurations](../references/windows-autopatch-conflicting-configurations.md)</li></ul> | | |
| [Raise, manage and resolve a service incident if an update management area isn't meeting the service level objective](../manage/windows-autopatch-support-request.md) | :x: | :heavy_check_mark: |
| [Exclude a device](../manage/windows-autopatch-exclude-device.md) | :heavy_check_mark: | :x: |
| [Register a device that was previously excluded](../manage/windows-autopatch-exclude-device.md#restore-a-device-or-multiple-devices-previously-excluded) | :heavy_check_mark: | :x: |
| [Request deactivation from Windows Autopatch](../manage/windows-autopatch-feature-deactivation.md) | :heavy_check_mark: | :x: |
| [Remove Windows Autopatch data from the service and exclude devices](../manage/windows-autopatch-feature-deactivation.md#microsofts-responsibilities-during-deactivation) | :x: | :heavy_check_mark: |
| [Maintain update configuration & update devices post deactivation from Windows Autopatch](../manage/windows-autopatch-feature-deactivation.md#your-responsibilities-after-deactivating-windows-autopatch-features) | :heavy_check_mark: | :x: |
| Review and respond to Message Center and Service Health Dashboard notifications<ul><li>[Windows quality update communications](../manage/windows-autopatch-windows-quality-update-communications.md)</li><li>[Add and verify admin contacts](../deploy/windows-autopatch-admin-contacts.md)</li></ul> | :heavy_check_mark: | :x: |
| Highlight Windows Autopatch management alerts that require customer action<ul><li>[Tenant management alerts](../monitor/windows-autopatch-maintain-environment.md#windows-autopatch-tenant-actions)</li><li>[Policy health and remediation](../monitor/windows-autopatch-policy-health-and-remediation.md)</li></ul> | :x: | :heavy_check_mark: |
| Review and respond to Windows Autopatch management alerts<ul><li>[Tenant management alerts](../monitor/windows-autopatch-maintain-environment.md#windows-autopatch-tenant-actions)</li><li>[Policy health and remediation](../monitor/windows-autopatch-policy-health-and-remediation.md)</li></ul> | :heavy_check_mark: | :x: |
| [Raise and respond to support requests](../manage/windows-autopatch-support-request.md) | :heavy_check_mark: | :x: |
| [Manage and respond to support requests](../manage/windows-autopatch-support-request.md#manage-an-active-support-request) | :x: | :heavy_check_mark: |
| Review the [What's new](../whats-new/windows-autopatch-whats-new-2024.md) section to stay up to date with updated feature and service releases | :heavy_check_mark: | :x: |
