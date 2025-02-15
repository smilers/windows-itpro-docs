---
title: WESL_UserSetting.SetEnabled
description: WESL_UserSetting.SetEnabled
ms.date: 05/20/2024
ms.topic: reference
---

# WESL_UserSetting.SetEnabled

This method enables or disables Shell Launcher.

## Syntax

```powershell
[Static] uint32 SetEnabled(
    [In, Required] boolean Enabled
);
```

## Parameters

**Enabled**</br>\[in, required\] A Boolean value that indicates whether to enable or disable Shell Launcher.

## Return Value

Returns an HRESULT value that indicates [WMI status](/windows/win32/wmisdk/wmi-non-error-constants) or a [WMI error](/windows/win32/wmisdk/wmi-error-constants).

## Remarks

This method enables or disables Shell Launcher by modifying the **Shell** value in the registry key `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon`. If Unified Write Filter (UWF) is enabled, you may need to disable UWF or commit this registry key by using [UWF_RegistryFilter.CommitRegistry](../unified-write-filter/uwf-registryfiltercommitregistry.md) in order to enable or disable Shell Launcher.

Enabling or disabling Shell Launcher does not take effect until a user signs in.

## Requirements

| Windows Edition        | Supported |
|:-----------------------|:---------:|
| Windows Home           | No        |
| Windows Pro            | No        |
| Windows Enterprise     | Yes       |
| Windows Education      | Yes       |
| Windows IoT Enterprise | Yes       |

## Related topics

- [WESL_UserSetting](wesl-usersetting.md)
- [Shell Launcher](index.md)
