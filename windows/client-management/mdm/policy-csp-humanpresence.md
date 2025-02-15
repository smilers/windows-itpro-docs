---
title: HumanPresence Policy CSP
description: Learn more about the HumanPresence Area in Policy CSP.
ms.date: 02/13/2025
ms.topic: generated-reference
---

<!-- Auto-Generated CSP Document -->

<!-- HumanPresence-Begin -->
# Policy CSP - HumanPresence

[!INCLUDE [Windows Insider tip](includes/mdm-insider-csp-note.md)]

<!-- HumanPresence-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- HumanPresence-Editable-End -->

<!-- ForceAllowDimWhenExternalDisplayConnected-Begin -->
## ForceAllowDimWhenExternalDisplayConnected

<!-- ForceAllowDimWhenExternalDisplayConnected-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ❌ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 11, version 24H2 [10.0.26100] and later |
<!-- ForceAllowDimWhenExternalDisplayConnected-Applicability-End -->

<!-- ForceAllowDimWhenExternalDisplayConnected-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/HumanPresence/ForceAllowDimWhenExternalDisplayConnected
```
<!-- ForceAllowDimWhenExternalDisplayConnected-OmaUri-End -->

<!-- ForceAllowDimWhenExternalDisplayConnected-Description-Begin -->
<!-- Description-Source-ADMX -->
Determines whether Allow Adaptive Dimming When Battery Saver On checkbox is forced checked/unchecked by the MDM policy. The user won't be able to change this setting and the checkbox in the UI will be greyed out.
<!-- ForceAllowDimWhenExternalDisplayConnected-Description-End -->

<!-- ForceAllowDimWhenExternalDisplayConnected-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- ForceAllowDimWhenExternalDisplayConnected-Editable-End -->

<!-- ForceAllowDimWhenExternalDisplayConnected-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `int` |
| Access Type | Add, Delete, Get, Replace |
| Default Value  | 0 |
<!-- ForceAllowDimWhenExternalDisplayConnected-DFProperties-End -->

<!-- ForceAllowDimWhenExternalDisplayConnected-AllowedValues-Begin -->
**Allowed values**:

| Value | Description |
|:--|:--|
| 2 | ForcedUnchecked. |
| 1 | ForcedChecked. |
| 0 (Default) | DefaultToUserChoice. |
<!-- ForceAllowDimWhenExternalDisplayConnected-AllowedValues-End -->

<!-- ForceAllowDimWhenExternalDisplayConnected-GpMapping-Begin -->
**Group policy mapping**:

| Name | Value |
|:--|:--|
| Name | ForceAllowDimWhenExternalDisplayConnected |
| Friendly Name | Force Allow Dim When External Display Connected |
| Location | Computer Configuration |
| Path | Windows Components > Human Presence |
| Registry Key Name | Software\Policies\Microsoft\HumanPresence |
| Registry Value Name | ForceAllowDimWhenExternalDisplayConnected |
| ADMX File Name | Sensors.admx |
<!-- ForceAllowDimWhenExternalDisplayConnected-GpMapping-End -->

<!-- ForceAllowDimWhenExternalDisplayConnected-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- ForceAllowDimWhenExternalDisplayConnected-Examples-End -->

<!-- ForceAllowDimWhenExternalDisplayConnected-End -->

<!-- ForceAllowLockWhenExternalDisplayConnected-Begin -->
## ForceAllowLockWhenExternalDisplayConnected

<!-- ForceAllowLockWhenExternalDisplayConnected-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ❌ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 11, version 24H2 [10.0.26100] and later |
<!-- ForceAllowLockWhenExternalDisplayConnected-Applicability-End -->

<!-- ForceAllowLockWhenExternalDisplayConnected-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/HumanPresence/ForceAllowLockWhenExternalDisplayConnected
```
<!-- ForceAllowLockWhenExternalDisplayConnected-OmaUri-End -->

<!-- ForceAllowLockWhenExternalDisplayConnected-Description-Begin -->
<!-- Description-Source-ADMX -->
Determines whether Allow Lock on Leave When Battery Saver On checkbox is forced checked/unchecked by the MDM policy. The user won't be able to change this setting and the checkbox in the UI will be greyed out.
<!-- ForceAllowLockWhenExternalDisplayConnected-Description-End -->

<!-- ForceAllowLockWhenExternalDisplayConnected-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- ForceAllowLockWhenExternalDisplayConnected-Editable-End -->

<!-- ForceAllowLockWhenExternalDisplayConnected-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `int` |
| Access Type | Add, Delete, Get, Replace |
| Default Value  | 0 |
<!-- ForceAllowLockWhenExternalDisplayConnected-DFProperties-End -->

<!-- ForceAllowLockWhenExternalDisplayConnected-AllowedValues-Begin -->
**Allowed values**:

| Value | Description |
|:--|:--|
| 2 | ForcedUnchecked. |
| 1 | ForcedChecked. |
| 0 (Default) | DefaultToUserChoice. |
<!-- ForceAllowLockWhenExternalDisplayConnected-AllowedValues-End -->

<!-- ForceAllowLockWhenExternalDisplayConnected-GpMapping-Begin -->
**Group policy mapping**:

| Name | Value |
|:--|:--|
| Name | ForceAllowLockWhenExternalDisplayConnected |
| Friendly Name | Force Allow Lock When External Display Connected |
| Location | Computer Configuration |
| Path | Windows Components > Human Presence |
| Registry Key Name | Software\Policies\Microsoft\HumanPresence |
| Registry Value Name | ForceAllowLockWhenExternalDisplayConnected |
| ADMX File Name | Sensors.admx |
<!-- ForceAllowLockWhenExternalDisplayConnected-GpMapping-End -->

<!-- ForceAllowLockWhenExternalDisplayConnected-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- ForceAllowLockWhenExternalDisplayConnected-Examples-End -->

<!-- ForceAllowLockWhenExternalDisplayConnected-End -->

<!-- ForceAllowWakeWhenExternalDisplayConnected-Begin -->
## ForceAllowWakeWhenExternalDisplayConnected

<!-- ForceAllowWakeWhenExternalDisplayConnected-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ❌ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 11, version 24H2 [10.0.26100] and later |
<!-- ForceAllowWakeWhenExternalDisplayConnected-Applicability-End -->

<!-- ForceAllowWakeWhenExternalDisplayConnected-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/HumanPresence/ForceAllowWakeWhenExternalDisplayConnected
```
<!-- ForceAllowWakeWhenExternalDisplayConnected-OmaUri-End -->

<!-- ForceAllowWakeWhenExternalDisplayConnected-Description-Begin -->
<!-- Description-Source-ADMX -->
Determines whether Allow Wake on Approach When External Display Connected checkbox is forced checked/unchecked by the MDM policy. The user won't be able to change this setting and the checkbox in the UI will be greyed out.
<!-- ForceAllowWakeWhenExternalDisplayConnected-Description-End -->

<!-- ForceAllowWakeWhenExternalDisplayConnected-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- ForceAllowWakeWhenExternalDisplayConnected-Editable-End -->

<!-- ForceAllowWakeWhenExternalDisplayConnected-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `int` |
| Access Type | Add, Delete, Get, Replace |
| Default Value  | 0 |
<!-- ForceAllowWakeWhenExternalDisplayConnected-DFProperties-End -->

<!-- ForceAllowWakeWhenExternalDisplayConnected-AllowedValues-Begin -->
**Allowed values**:

| Value | Description |
|:--|:--|
| 2 | ForcedUnchecked. |
| 1 | ForcedChecked. |
| 0 (Default) | DefaultToUserChoice. |
<!-- ForceAllowWakeWhenExternalDisplayConnected-AllowedValues-End -->

<!-- ForceAllowWakeWhenExternalDisplayConnected-GpMapping-Begin -->
**Group policy mapping**:

| Name | Value |
|:--|:--|
| Name | ForceAllowWakeWhenExternalDisplayConnected |
| Friendly Name | Force Allow Wake When External Display Connected |
| Location | Computer Configuration |
| Path | Windows Components > Human Presence |
| Registry Key Name | Software\Policies\Microsoft\HumanPresence |
| Registry Value Name | ForceAllowWakeWhenExternalDisplayConnected |
| ADMX File Name | Sensors.admx |
<!-- ForceAllowWakeWhenExternalDisplayConnected-GpMapping-End -->

<!-- ForceAllowWakeWhenExternalDisplayConnected-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- ForceAllowWakeWhenExternalDisplayConnected-Examples-End -->

<!-- ForceAllowWakeWhenExternalDisplayConnected-End -->

<!-- ForceDisableWakeWhenBatterySaverOn-Begin -->
## ForceDisableWakeWhenBatterySaverOn

<!-- ForceDisableWakeWhenBatterySaverOn-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ❌ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 11, version 24H2 [10.0.26100] and later |
<!-- ForceDisableWakeWhenBatterySaverOn-Applicability-End -->

<!-- ForceDisableWakeWhenBatterySaverOn-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/HumanPresence/ForceDisableWakeWhenBatterySaverOn
```
<!-- ForceDisableWakeWhenBatterySaverOn-OmaUri-End -->

<!-- ForceDisableWakeWhenBatterySaverOn-Description-Begin -->
<!-- Description-Source-ADMX -->
Determines whether Disable Wake on Approach When Battery Saver On checkbox is forced checked/unchecked by the MDM policy. The user won't be able to change this setting and the checkbox in the UI will be greyed out.
<!-- ForceDisableWakeWhenBatterySaverOn-Description-End -->

<!-- ForceDisableWakeWhenBatterySaverOn-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- ForceDisableWakeWhenBatterySaverOn-Editable-End -->

<!-- ForceDisableWakeWhenBatterySaverOn-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `int` |
| Access Type | Add, Delete, Get, Replace |
| Default Value  | 0 |
<!-- ForceDisableWakeWhenBatterySaverOn-DFProperties-End -->

<!-- ForceDisableWakeWhenBatterySaverOn-AllowedValues-Begin -->
**Allowed values**:

| Value | Description |
|:--|:--|
| 2 | ForcedUnchecked. |
| 1 | ForcedChecked. |
| 0 (Default) | DefaultToUserChoice. |
<!-- ForceDisableWakeWhenBatterySaverOn-AllowedValues-End -->

<!-- ForceDisableWakeWhenBatterySaverOn-GpMapping-Begin -->
**Group policy mapping**:

| Name | Value |
|:--|:--|
| Name | ForceDisableWakeWhenBatterySaverOn |
| Friendly Name | Force Disable Wake When Battery Saver On |
| Location | Computer Configuration |
| Path | Windows Components > Human Presence |
| Registry Key Name | Software\Policies\Microsoft\HumanPresence |
| Registry Value Name | ForceDisableWakeWhenBatterySaverOn |
| ADMX File Name | Sensors.admx |
<!-- ForceDisableWakeWhenBatterySaverOn-GpMapping-End -->

<!-- ForceDisableWakeWhenBatterySaverOn-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- ForceDisableWakeWhenBatterySaverOn-Examples-End -->

<!-- ForceDisableWakeWhenBatterySaverOn-End -->

<!-- ForceInstantDim-Begin -->
## ForceInstantDim

<!-- ForceInstantDim-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ❌ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 11, version 21H2 [10.0.22000] and later |
<!-- ForceInstantDim-Applicability-End -->

<!-- ForceInstantDim-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/HumanPresence/ForceInstantDim
```
<!-- ForceInstantDim-OmaUri-End -->

<!-- ForceInstantDim-Description-Begin -->
<!-- Description-Source-ADMX -->
Determines whether Attention Based Display Dimming is forced on/off by the MDM policy. The user won't be able to change this setting and the toggle in the UI will be greyed out.
<!-- ForceInstantDim-Description-End -->

<!-- ForceInstantDim-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
This is a power saving feature that prolongs battery charge.
<!-- ForceInstantDim-Editable-End -->

<!-- ForceInstantDim-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `int` |
| Access Type | Add, Delete, Get, Replace |
| Default Value  | 0 |
<!-- ForceInstantDim-DFProperties-End -->

<!-- ForceInstantDim-AllowedValues-Begin -->
**Allowed values**:

| Value | Description |
|:--|:--|
| 2 | ForcedOff. |
| 1 | ForcedOn. |
| 0 (Default) | DefaultToUserChoice. |
<!-- ForceInstantDim-AllowedValues-End -->

<!-- ForceInstantDim-GpMapping-Begin -->
**Group policy mapping**:

| Name | Value |
|:--|:--|
| Name | ForceInstantDim |
| Friendly Name | Force Instant Dim |
| Location | Computer Configuration |
| Path | Windows Components > Human Presence |
| Registry Key Name | Software\Policies\Microsoft\HumanPresence |
| ADMX File Name | Sensors.admx |
<!-- ForceInstantDim-GpMapping-End -->

<!-- ForceInstantDim-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- ForceInstantDim-Examples-End -->

<!-- ForceInstantDim-End -->

<!-- ForceInstantLock-Begin -->
## ForceInstantLock

<!-- ForceInstantLock-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ❌ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 11, version 21H2 [10.0.22000] and later |
<!-- ForceInstantLock-Applicability-End -->

<!-- ForceInstantLock-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/HumanPresence/ForceInstantLock
```
<!-- ForceInstantLock-OmaUri-End -->

<!-- ForceInstantLock-Description-Begin -->
<!-- Description-Source-ADMX -->
Determines whether Lock on Leave is forced on/off by the MDM policy. The user won't be able to change this setting and the toggle in the UI will be greyed out.
<!-- ForceInstantLock-Description-End -->

<!-- ForceInstantLock-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- ForceInstantLock-Editable-End -->

<!-- ForceInstantLock-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `int` |
| Access Type | Add, Delete, Get, Replace |
| Default Value  | 0 |
<!-- ForceInstantLock-DFProperties-End -->

<!-- ForceInstantLock-AllowedValues-Begin -->
**Allowed values**:

| Value | Description |
|:--|:--|
| 2 | ForcedOff. |
| 1 | ForcedOn. |
| 0 (Default) | DefaultToUserChoice. |
<!-- ForceInstantLock-AllowedValues-End -->

<!-- ForceInstantLock-GpMapping-Begin -->
**Group policy mapping**:

| Name | Value |
|:--|:--|
| Name | ForceInstantLock |
| Friendly Name | Force Instant Lock |
| Location | Computer Configuration |
| Path | Windows Components > Human Presence |
| Registry Key Name | Software\Policies\Microsoft\HumanPresence |
| Registry Value Name | ForceInstantLock |
| ADMX File Name | Sensors.admx |
<!-- ForceInstantLock-GpMapping-End -->

<!-- ForceInstantLock-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- ForceInstantLock-Examples-End -->

<!-- ForceInstantLock-End -->

<!-- ForceInstantWake-Begin -->
## ForceInstantWake

<!-- ForceInstantWake-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ❌ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 11, version 21H2 [10.0.22000] and later |
<!-- ForceInstantWake-Applicability-End -->

<!-- ForceInstantWake-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/HumanPresence/ForceInstantWake
```
<!-- ForceInstantWake-OmaUri-End -->

<!-- ForceInstantWake-Description-Begin -->
<!-- Description-Source-ADMX -->
Determines whether Wake On Arrival is forced on/off by the MDM policy. The user won't be able to change this setting and the toggle in the UI will be greyed out.
<!-- ForceInstantWake-Description-End -->

<!-- ForceInstantWake-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- ForceInstantWake-Editable-End -->

<!-- ForceInstantWake-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `int` |
| Access Type | Add, Delete, Get, Replace |
| Default Value  | 0 |
<!-- ForceInstantWake-DFProperties-End -->

<!-- ForceInstantWake-AllowedValues-Begin -->
**Allowed values**:

| Value | Description |
|:--|:--|
| 2 | ForcedOff. |
| 1 | ForcedOn. |
| 0 (Default) | DefaultToUserChoice. |
<!-- ForceInstantWake-AllowedValues-End -->

<!-- ForceInstantWake-GpMapping-Begin -->
**Group policy mapping**:

| Name | Value |
|:--|:--|
| Name | ForceInstantWake |
| Friendly Name | Force Instant Wake |
| Location | Computer Configuration |
| Path | Windows Components > Human Presence |
| Registry Key Name | Software\Policies\Microsoft\HumanPresence |
| Registry Value Name | ForceInstantWake |
| ADMX File Name | Sensors.admx |
<!-- ForceInstantWake-GpMapping-End -->

<!-- ForceInstantWake-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- ForceInstantWake-Examples-End -->

<!-- ForceInstantWake-End -->

<!-- ForceLockTimeout-Begin -->
## ForceLockTimeout

<!-- ForceLockTimeout-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ❌ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 11, version 21H2 [10.0.22000] and later |
<!-- ForceLockTimeout-Applicability-End -->

<!-- ForceLockTimeout-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/HumanPresence/ForceLockTimeout
```
<!-- ForceLockTimeout-OmaUri-End -->

<!-- ForceLockTimeout-Description-Begin -->
<!-- Description-Source-ADMX -->
Determines the timeout for Lock on Leave forced by the MDM policy. The user will be unable to change this setting and the toggle in the UI will be greyed out.
<!-- ForceLockTimeout-Description-End -->

<!-- ForceLockTimeout-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- ForceLockTimeout-Editable-End -->

<!-- ForceLockTimeout-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `int` |
| Access Type | Add, Delete, Get, Replace |
| Default Value  | 0 |
<!-- ForceLockTimeout-DFProperties-End -->

<!-- ForceLockTimeout-AllowedValues-Begin -->
**Allowed values**:

| Value | Description |
|:--|:--|
| 120 | TwoMinutes. |
| 30 | ThirtySeconds. |
| 10 | TenSeconds. |
| 1 | Immediate. |
| 0 (Default) | DefaultToUserChoice. |
<!-- ForceLockTimeout-AllowedValues-End -->

<!-- ForceLockTimeout-GpMapping-Begin -->
**Group policy mapping**:

| Name | Value |
|:--|:--|
| Name | ForceLockTimeout |
| Friendly Name | Lock Timeout |
| Location | Computer Configuration |
| Path | Windows Components > Human Presence |
| Registry Key Name | Software\Policies\Microsoft\HumanPresence |
| ADMX File Name | Sensors.admx |
<!-- ForceLockTimeout-GpMapping-End -->

<!-- ForceLockTimeout-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- ForceLockTimeout-Examples-End -->

<!-- ForceLockTimeout-End -->

<!-- ForcePrivacyScreen-Begin -->
## ForcePrivacyScreen

<!-- ForcePrivacyScreen-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ❌ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows Insider Preview |
<!-- ForcePrivacyScreen-Applicability-End -->

<!-- ForcePrivacyScreen-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/HumanPresence/ForcePrivacyScreen
```
<!-- ForcePrivacyScreen-OmaUri-End -->

<!-- ForcePrivacyScreen-Description-Begin -->
<!-- Description-Source-DDF -->
Determines whether detect when other people are looking at my screen is forced on/off by the MDM policy. The user won't be able to change this setting and the UI will be greyed out.
<!-- ForcePrivacyScreen-Description-End -->

<!-- ForcePrivacyScreen-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- ForcePrivacyScreen-Editable-End -->

<!-- ForcePrivacyScreen-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `int` |
| Access Type | Add, Delete, Get, Replace |
| Default Value  | 0 |
<!-- ForcePrivacyScreen-DFProperties-End -->

<!-- ForcePrivacyScreen-AllowedValues-Begin -->
**Allowed values**:

| Value | Description |
|:--|:--|
| 2 | ForcedOff. |
| 1 | ForcedOn. |
| 0 (Default) | DefaultToUserChoice. |
<!-- ForcePrivacyScreen-AllowedValues-End -->

<!-- ForcePrivacyScreen-GpMapping-Begin -->
**Group policy mapping**:

| Name | Value |
|:--|:--|
| Name | ForcePrivacyScreen |
| Path | Sensors > AT > WindowsComponents > HumanPresence |
<!-- ForcePrivacyScreen-GpMapping-End -->

<!-- ForcePrivacyScreen-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- ForcePrivacyScreen-Examples-End -->

<!-- ForcePrivacyScreen-End -->

<!-- ForcePrivacyScreenDim-Begin -->
## ForcePrivacyScreenDim

<!-- ForcePrivacyScreenDim-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ❌ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows Insider Preview |
<!-- ForcePrivacyScreenDim-Applicability-End -->

<!-- ForcePrivacyScreenDim-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/HumanPresence/ForcePrivacyScreenDim
```
<!-- ForcePrivacyScreenDim-OmaUri-End -->

<!-- ForcePrivacyScreenDim-Description-Begin -->
<!-- Description-Source-DDF -->
Determines whether dim the screen when other people are looking at my screen checkbox is forced checked/unchecked by the MDM policy. The user won't be able to change this setting and the checkbox in the UI will be greyed out.
<!-- ForcePrivacyScreenDim-Description-End -->

<!-- ForcePrivacyScreenDim-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- ForcePrivacyScreenDim-Editable-End -->

<!-- ForcePrivacyScreenDim-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `int` |
| Access Type | Add, Delete, Get, Replace |
| Default Value  | 0 |
<!-- ForcePrivacyScreenDim-DFProperties-End -->

<!-- ForcePrivacyScreenDim-AllowedValues-Begin -->
**Allowed values**:

| Value | Description |
|:--|:--|
| 2 | ForcedUnchecked. |
| 1 | ForcedChecked. |
| 0 (Default) | DefaultToUserChoice. |
<!-- ForcePrivacyScreenDim-AllowedValues-End -->

<!-- ForcePrivacyScreenDim-GpMapping-Begin -->
**Group policy mapping**:

| Name | Value |
|:--|:--|
| Name | ForcePrivacyScreenDim |
| Path | Sensors > AT > WindowsComponents > HumanPresence |
<!-- ForcePrivacyScreenDim-GpMapping-End -->

<!-- ForcePrivacyScreenDim-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- ForcePrivacyScreenDim-Examples-End -->

<!-- ForcePrivacyScreenDim-End -->

<!-- ForcePrivacyScreenNotification-Begin -->
## ForcePrivacyScreenNotification

<!-- ForcePrivacyScreenNotification-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ❌ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows Insider Preview |
<!-- ForcePrivacyScreenNotification-Applicability-End -->

<!-- ForcePrivacyScreenNotification-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/HumanPresence/ForcePrivacyScreenNotification
```
<!-- ForcePrivacyScreenNotification-OmaUri-End -->

<!-- ForcePrivacyScreenNotification-Description-Begin -->
<!-- Description-Source-DDF -->
Determines whether providing alert when people are looking at my screen checkbox is forced checked/unchecked by the MDM policy. The user won't be able to change this setting and the checkbox in the UI will be greyed out.
<!-- ForcePrivacyScreenNotification-Description-End -->

<!-- ForcePrivacyScreenNotification-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- ForcePrivacyScreenNotification-Editable-End -->

<!-- ForcePrivacyScreenNotification-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `int` |
| Access Type | Add, Delete, Get, Replace |
| Default Value  | 0 |
<!-- ForcePrivacyScreenNotification-DFProperties-End -->

<!-- ForcePrivacyScreenNotification-AllowedValues-Begin -->
**Allowed values**:

| Value | Description |
|:--|:--|
| 2 | ForcedUnchecked. |
| 1 | ForcedChecked. |
| 0 (Default) | DefaultToUserChoice. |
<!-- ForcePrivacyScreenNotification-AllowedValues-End -->

<!-- ForcePrivacyScreenNotification-GpMapping-Begin -->
**Group policy mapping**:

| Name | Value |
|:--|:--|
| Name | ForcePrivacyScreenNotification |
| Path | Sensors > AT > WindowsComponents > HumanPresence |
<!-- ForcePrivacyScreenNotification-GpMapping-End -->

<!-- ForcePrivacyScreenNotification-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- ForcePrivacyScreenNotification-Examples-End -->

<!-- ForcePrivacyScreenNotification-End -->

<!-- HumanPresence-CspMoreInfo-Begin -->
<!-- Add any additional information about this CSP here. Anything outside this section will get overwritten. -->
<!-- HumanPresence-CspMoreInfo-End -->

<!-- HumanPresence-End -->

## Related articles

[Policy configuration service provider](policy-configuration-service-provider.md)
