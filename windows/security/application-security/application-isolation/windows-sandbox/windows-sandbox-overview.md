---
title: Windows Sandbox
description: Windows Sandbox overview
ms.topic: conceptual
ms.date: 09/09/2024
---

# Windows Sandbox

Windows Sandbox provides a lightweight desktop environment to safely run applications in isolation. Software installed inside the Windows Sandbox environment remains "sandboxed" and runs separately from the host machine.

A sandbox is temporary. When it's closed, all the software and files and the state are deleted. You get a brand-new instance of the sandbox every time you open the application. Note, however, that as of Windows 11, version 22H2, your data persists through a restart initiated from inside the virtualized environment—useful for installing applications that require the OS to reboot.

Software and applications installed on the host aren't directly available in the sandbox. If you need specific applications available inside the Windows Sandbox environment, they must be explicitly installed within the environment.

Windows Sandbox has the following properties:

- **Part of Windows**: Everything required for this feature is included in Windows 10 Pro and Enterprise. There's no need to download a Virtual Hard Disk (VHD).
- **Pristine**: Every time Windows Sandbox runs, it's as clean as a brand-new installation of Windows.
- **Disposable**: Nothing persists on the device. Everything is discarded when the user closes the application.
- **Secure**: Uses hardware-based virtualization for kernel isolation. It relies on the Microsoft hypervisor to run a separate kernel that isolates Windows Sandbox from the host.
- **Efficient:** Uses the integrated kernel scheduler, smart memory management, and virtual GPU.

> [!IMPORTANT]
> Windows Sandbox enables network connection by default. It can be disabled using the [Windows Sandbox configuration file](windows-sandbox-configure-using-wsb-file.md#networking).

[!INCLUDE [windows-sandbox](../../../../../includes/licensing/windows-sandbox.md)]

## Usage

1. Copy an executable file (and any other files needed to run the application) from the host and paste them into the **Windows Sandbox** window.
2. Run the executable file or installer inside the sandbox.
3. When you're finished experimenting, close the sandbox. A dialog box will state that all sandbox content will be discarded and permanently deleted. Select **Ok**.
4. Confirm that your host machine doesn't exhibit any of the modifications that you made in Windows Sandbox.
