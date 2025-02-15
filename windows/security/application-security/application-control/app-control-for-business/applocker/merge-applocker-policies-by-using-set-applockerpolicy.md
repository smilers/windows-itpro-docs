---
title: Merge AppLocker policies by using Set-ApplockerPolicy
description: This article for IT professionals describes the steps to merge AppLocker policies by using Windows PowerShell.
ms.localizationpriority: medium
ms.topic: conceptual
ms.date: 09/11/2024
---

# Merge AppLocker policies by using Set-ApplockerPolicy

This article for IT professionals describes the steps to merge AppLocker policies by using Windows PowerShell.

The **Set-AppLockerPolicy** cmdlet sets the specified Group Policy Object (GPO) to contain the specified AppLocker policy. If no Lightweight Directory Access Protocol (LDAP) is specified, the local policy is used. When the Merge parameter is used, rules in the specified AppLocker policy are merged with the AppLocker rules in the target GPO specified in the LDAP path. Merging policies removes rules with duplicate rule IDs, and the enforcement mode setting is chosen as described in [Working with AppLocker rules](working-with-applocker-rules.md#enforcement-modes). If the Merge parameter isn't specified, then the new policy overwrites the existing policy.

For info about using **Set-AppLockerPolicy**, including syntax descriptions and parameters, see [Set-AppLockerPolicy](/powershell/module/applocker/set-applockerpolicy).

For info about using Windows PowerShell for AppLocker, including how to import the AppLocker cmdlets into Windows PowerShell, see [Use the AppLocker Windows PowerShell cmdlets](use-the-applocker-windows-powershell-cmdlets.md).

You can also manually merge AppLocker policies. For information on the procedure to do this merging, see [Merge AppLocker policies manually](merge-applocker-policies-manually.md).

## To merge a local AppLocker policy with another AppLocker policy by using LDAP paths

1. Open the PowerShell command window. For info about performing Windows PowerShell commands for AppLocker, see [Use the AppLocker Windows PowerShell cmdlets](use-the-applocker-windows-powershell-cmdlets.md).
2. At the command prompt, type **C:\\PS&gt;Get-AppLockerPolicy -Local | Set-AppLockerPolicy -LDAP "LDAP: //***&lt;string&gt;***"** **-Merge** where *&lt;string&gt;* specifies the LDAP path of the unique GPO.

## Example

Gets the local AppLocker policy, and then merges the policy with the existing AppLocker policy in the GPO specified in the LDAP path.

```powershell
C:\PS>Get-AppLockerPolicy -Local | Set-AppLockerPolicy -LDAP "LDAP://DC13.Contoso.com/CN={31B2F340-016D-11D2-945F-00C044FB984F9},CN=Policies,CN=System,DC=Contoso,DC=com" -Merge
```
