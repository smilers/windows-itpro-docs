---
title: Reboot CSP
description: Learn more about the Reboot CSP.
ms.date: 02/14/2025
ms.topic: generated-reference
---

<!-- Auto-Generated CSP Document -->

<!-- Reboot-Begin -->
# Reboot CSP

<!-- Reboot-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
The Reboot configuration service provider is used to configure reboot settings.
<!-- Reboot-Editable-End -->

<!-- Reboot-Tree-Begin -->
The following list shows the Reboot configuration service provider nodes:

- ./Device/Vendor/MSFT/Reboot
  - [RebootNow](#rebootnow)
  - [Schedule](#schedule)
    - [DailyRecurrent](#scheduledailyrecurrent)
    - [Single](#schedulesingle)
    - [WeeklyRecurrent](#scheduleweeklyrecurrent)
<!-- Reboot-Tree-End -->

<!-- Device-RebootNow-Begin -->
## RebootNow

<!-- Device-RebootNow-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ✅ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 10, version 1607 [10.0.14393] and later |
<!-- Device-RebootNow-Applicability-End -->

<!-- Device-RebootNow-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Reboot/RebootNow
```
<!-- Device-RebootNow-OmaUri-End -->

<!-- Device-RebootNow-Description-Begin -->
<!-- Description-Source-DDF -->
This node executes a reboot of the device. RebootNow triggers a reboot within 5 minutes to allow the user to wrap up any active work. If this node is set to execute during a sync session, the device will reboot at the end of the sync session.
<!-- Device-RebootNow-Description-End -->

<!-- Device-RebootNow-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- Device-RebootNow-Editable-End -->

<!-- Device-RebootNow-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `null` |
| Access Type | Exec, Get |
<!-- Device-RebootNow-DFProperties-End -->

<!-- Device-RebootNow-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- Device-RebootNow-Examples-End -->

<!-- Device-RebootNow-End -->

<!-- Device-Schedule-Begin -->
## Schedule

<!-- Device-Schedule-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ✅ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 10, version 1607 [10.0.14393] and later |
<!-- Device-Schedule-Applicability-End -->

<!-- Device-Schedule-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Reboot/Schedule
```
<!-- Device-Schedule-OmaUri-End -->

<!-- Device-Schedule-Description-Begin -->
<!-- Description-Source-DDF -->
The supported operation is Get.
<!-- Device-Schedule-Description-End -->

<!-- Device-Schedule-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- Device-Schedule-Editable-End -->

<!-- Device-Schedule-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `node` |
| Access Type | Get |
<!-- Device-Schedule-DFProperties-End -->

<!-- Device-Schedule-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- Device-Schedule-Examples-End -->

<!-- Device-Schedule-End -->

<!-- Device-Schedule-DailyRecurrent-Begin -->
### Schedule/DailyRecurrent

<!-- Device-Schedule-DailyRecurrent-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ✅ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 10, version 1607 [10.0.14393] and later |
<!-- Device-Schedule-DailyRecurrent-Applicability-End -->

<!-- Device-Schedule-DailyRecurrent-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Reboot/Schedule/DailyRecurrent
```
<!-- Device-Schedule-DailyRecurrent-OmaUri-End -->

<!-- Device-Schedule-DailyRecurrent-Description-Begin -->
<!-- Description-Source-DDF -->
Value in ISO8601 date and time format (such as 2025-10-07T10:35:00) is required. While it's supported to set either DailyRecurrent or WeeklyRecurrent schedules, it isn't supported to enable both settings simultaneously. A reboot will be scheduled to occur every day at the configured time starting at the specified date and time. Setting a null (empty) date will delete the existing schedule.
<!-- Device-Schedule-DailyRecurrent-Description-End -->

<!-- Device-Schedule-DailyRecurrent-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- Device-Schedule-DailyRecurrent-Editable-End -->

<!-- Device-Schedule-DailyRecurrent-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `chr` (string) |
| Access Type | Add, Delete, Get, Replace |
<!-- Device-Schedule-DailyRecurrent-DFProperties-End -->

<!-- Device-Schedule-DailyRecurrent-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- Device-Schedule-DailyRecurrent-Examples-End -->

<!-- Device-Schedule-DailyRecurrent-End -->

<!-- Device-Schedule-Single-Begin -->
### Schedule/Single

<!-- Device-Schedule-Single-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ✅ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 10, version 1607 [10.0.14393] and later |
<!-- Device-Schedule-Single-Applicability-End -->

<!-- Device-Schedule-Single-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Reboot/Schedule/Single
```
<!-- Device-Schedule-Single-OmaUri-End -->

<!-- Device-Schedule-Single-Description-Begin -->
<!-- Description-Source-DDF -->
Value in ISO8601 date and time format (such as 2025-10-07T10:35:00) is required. Both the date and time are required. A reboot will be scheduled to occur at the specified date and time. Setting a null (empty) date will delete the existing schedule.
<!-- Device-Schedule-Single-Description-End -->

<!-- Device-Schedule-Single-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- Device-Schedule-Single-Editable-End -->

<!-- Device-Schedule-Single-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `chr` (string) |
| Access Type | Add, Delete, Get, Replace |
<!-- Device-Schedule-Single-DFProperties-End -->

<!-- Device-Schedule-Single-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- Device-Schedule-Single-Examples-End -->

<!-- Device-Schedule-Single-End -->

<!-- Device-Schedule-WeeklyRecurrent-Begin -->
### Schedule/WeeklyRecurrent

<!-- Device-Schedule-WeeklyRecurrent-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ✅ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 11, version 24H2 [10.0.26100] and later |
<!-- Device-Schedule-WeeklyRecurrent-Applicability-End -->

<!-- Device-Schedule-WeeklyRecurrent-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Reboot/Schedule/WeeklyRecurrent
```
<!-- Device-Schedule-WeeklyRecurrent-OmaUri-End -->

<!-- Device-Schedule-WeeklyRecurrent-Description-Begin -->
<!-- Description-Source-DDF -->
Value in ISO8601 date and time format (such as 2025-10-07T10:35:00) is required. While it's supported to set either DailyRecurrent or WeeklyRecurrent schedules, it isn't supported to enable both settings simultaneously. A reboot will be scheduled to occur every week at the configured day and time starting at the specified date and time. Setting a null (empty) date will delete the existing schedule.
<!-- Device-Schedule-WeeklyRecurrent-Description-End -->

<!-- Device-Schedule-WeeklyRecurrent-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- Device-Schedule-WeeklyRecurrent-Editable-End -->

<!-- Device-Schedule-WeeklyRecurrent-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `chr` (string) |
| Access Type | Add, Delete, Get, Replace |
<!-- Device-Schedule-WeeklyRecurrent-DFProperties-End -->

<!-- Device-Schedule-WeeklyRecurrent-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- Device-Schedule-WeeklyRecurrent-Examples-End -->

<!-- Device-Schedule-WeeklyRecurrent-End -->

<!-- Reboot-CspMoreInfo-Begin -->
<!-- Add any additional information about this CSP here. Anything outside this section will get overwritten. -->
<!-- Reboot-CspMoreInfo-End -->

<!-- Reboot-End -->

## Related articles

[Configuration service provider reference](configuration-service-provider-reference.md)
