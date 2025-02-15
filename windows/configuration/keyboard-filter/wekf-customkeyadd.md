---
title: WEKF_CustomKey.Add
description: WEKF_CustomKey.Add
ms.date: 01/13/2025
ms.topic: reference
---

# WEKF_CustomKey.Add

[!INCLUDE [supported-os-enterprise-plus](../../../includes/iot/supported-os-enterprise-plus.md)]

Creates a new custom key combination and enables Keyboard Filter to block the new key combination.

## Syntax

```powershell
[Static] uint32 Add(
    [In] string CustomKey
);
```

## Parameters

**CustomKey**</br>\[in\] The custom key combination to add. For a list of valid key names, see [Keyboard Filter key names](keyboardfilter-key-names.md).

## Return Value

Returns an HRESULT value that indicates a [WMI Non-Error Constant](/windows/win32/wmisdk/wmi-non-error-constants) or a [WMI Error Constant](/windows/win32/wmisdk/wmi-error-constants).

## Remarks

**WEKF_CustomKey.Add** creates a new **WEKF_CustomKey** object and sets the **Enabled** property of the new object to **true**, and the **Id** property to *CustomKey*.

If a **WEKF_CustomKey** object already exists with the **Id** property equal to *CustomKey*, then **WEKF_CustomKey.Add** returns an error code and doesn't create a new object or modify any properties of the existing object. If the existing **WEKF_CustomKey** object has the **Enabled** property set to **false**, Keyboard Filter does not block the custom key combination.

## Example

The following code demonstrates how to add or enable a custom key that Keyboard Filter will block by using the Windows Management Instrumentation (WMI) providers for Keyboard Filter.

```powershell
$COMPUTER = "localhost"
$NAMESPACE = "root\standardcimv2\embedded"

# Create a handle to the class instance so we can call the static methods
$classCustomKey = [wmiclass]"\\$COMPUTER\${NAMESPACE}:WEKF_CustomKey"

# Create a function to add or enable a key combination for Keyboard Filter to block
function Enable-Custom-Key($KeyId) {

# Check to see if the custom key object already exists
    $objCustomKey = Get-WMIObject -namespace $NAMESPACE -class WEKF_CustomKey |
            where {$_.Id -eq "$KeyId"};

    if ($objCustomKey) {

# The custom key already exists, so just enable it
        $objCustomKey.Enabled = 1;
        $objCustomKey.Put() | Out-Null;
        "Enabled ${KeyId}.";

    } else {

# Create a new custom key object by calling the static Add method
        $retval = $classCustomKey.Add($KeyId);

# Check the return value to verify that the Add is successful
        if ($retval.ReturnValue -eq 0) {
            "Added ${KeyID}."
        } else {
            "Unknown Error: " + "{0:x0}" -f $retval.ReturnValue
        }
    }
}

# Enable Keyboard Filter to block several custom keys

Enable-Custom-Key "Ctrl+v"
Enable-Custom-Key "Ctrl+v"
Enable-Custom-Key "Shift+4"
Enable-Custom-Key "Ctrl+Alt+w"

# List all the currently existing custom keys

$objCustomKeyList = get-WMIObject -namespace $NAMESPACE -class WEKF_CustomKey
foreach ($objCustomKeyItem in $objCustomKeyList) {
    "Custom key: " + $objCustomKeyItem.Id
    "   enabled: " + $objCustomKeyItem.Enabled
    }
```

## Related articles

- [WEKF_CustomKey](wekf-customkey.md)
- [Keyboard Filter](index.md)
