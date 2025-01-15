---
title: WESL_UserSetting.IsEnabled
description: WESL_UserSetting.IsEnabled
ms.date: 05/20/2024
ms.topic: reference
---

# WESL_UserSetting.IsEnabled

This method retrieves a value that indicates if Shell Launcher is enabled or disabled.

## Syntax

```powershell
[Static] uint32 IsEnabled(
    [Out, Required] boolean Enabled
);
```

## Parameters

**Enabled**</br>\[out, required\] A Boolean value that indicates if Shell Launcher is enabled.

## Return Value

Returns an HRESULT value that indicates [WMI status](/windows/win32/wmisdk/wmi-non-error-constants) or a [WMI error](/windows/win32/wmisdk/wmi-error-constants).

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
