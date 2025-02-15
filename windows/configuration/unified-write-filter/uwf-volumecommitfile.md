---
title: UWF_Volume.CommitFile
description: UWF_Volume.CommitFile
ms.date: 05/20/2024
ms.topic: reference
---

# UWF_Volume.CommitFile

Commits changes from the overlay to the physical volume for a specified file on a volume protected by Unified Write Filter (UWF).

## Syntax

```powershell
UInt32 CommitFile(
    [in] string FileName
);
```

## Parameters

**FileName**</br>\[in\] A string that contains the path of the file to commit on the overlay, but does not include the drive letter or volume name. For example, “\\users\\test.dat”.

## Return Value

Returns an HRESULT value that indicates [WMI status](/windows/win32/wmisdk/wmi-non-error-constants) or a [WMI error constant](/windows/win32/wmisdk/wmi-error-constants).

## Remarks

The *FileName* must contain the name of a file that exists. The **CommitFile** method cannot commit a file that does not exist.

You must use an administrator account to change any properties or call any methods that change the configuration settings.

## Requirements

| Windows Edition        | Supported |
|:-----------------------|:---------:|
| Windows Home           | No        |
| Windows Pro            | No        |
| Windows Enterprise     | Yes       |
| Windows Education      | Yes       |
| Windows IoT Enterprise | Yes       |

## Related articles

- [UWF_Volume](uwf-volume.md)
- [Unified Write Filter]( index.md)
