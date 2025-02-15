---
title: WESL_UserSetting.RemoveCustomShell
description: WESL_UserSetting.RemoveCustomShell
ms.date: 05/20/2024
ms.topic: reference
---

# WESL_UserSetting.RemoveCustomShell

This method removes a Shell Launcher configuration for a specific user or group, based on the security identifier (SID).

## Syntax

```powershell
[Static] uint32 RemoveCustomShell (
    [In, Required] string Sid
);
```

## Parameters

**Sid**</br>\[in, required\] A string containing the security identifier (SID) of the user or group that Shell Launcher is configured for.

## Return Value

Returns an HRESULT value that indicates [WMI status](/windows/win32/wmisdk/wmi-non-error-constants) or a [WMI error](/windows/win32/wmisdk/wmi-error-constants).

## Remarks

You must restart your device for the changes to take effect.

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
