---
title: Troubleshoot Windows Sandbox
description: Troubleshoot Windows Sandbox
ms.topic: troubleshooting
ms.date: 09/09/2024
---

# Troubleshoot Windows Sandbox

This article lists some common issues with Windows Sandbox and possible solutions. To submit feedback about Windows Sandbox, see [Where can I provide feedback?](windows-sandbox-faq.yml##where-can-i-provide-feedback)

| Error | Possible Solution |
|--|--|
| `WININET_E_NAME_NOT_RESOLVED` <br>`WU_E_PT_ENDPOINT_UNREACHABLE` | Upgrade to Windows Sandbox app fails because user isn't connected to internet or network adapter is connected but no internet connection. Check your internet connection. |
| `ERROR_FILE_NOT_FOUND` | `.wsb` config file provided by the user doesn't exist. Make sure that the path to the `.wsb` file is correct. |
| `E_INVALIDARG` | The `.wsb` file provided by the user is invalid or has errors. Check the `.wsb` file. |
| `REGDB_E_IIDNOTREG` | Verify if Windows Sandbox component is enabled under 'Turn Windows features on or off'. For more information, see [Install Windows Sandbox](windows-sandbox-install.md) |
| `The following settings are enforced by your IT administrator.` | `.wsb` file has a setting enabled that is controlled via group policy. |
| General failure during installation. | Possible causes: <br><br>- Installing Windows Sandbox is disabled via group policy. Check with your IT Admin. <br>- Timeout error where we can't reach the Microsoft Store. Try again later. |
