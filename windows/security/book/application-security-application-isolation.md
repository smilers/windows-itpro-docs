---
title: Windows 11 security book - Application isolation
description: Application isolation.
ms.topic: overview
ms.date: 11/18/2024
---

# Application isolation

:::image type="content" source="images/application-security.png" alt-text="Diagram containing a list of application security features." lightbox="images/application-security.png" border="false":::

## :::image type="icon" source="images/new-button-title.svg" border="false"::: Win32 app isolation

Win32 app isolation is a security feature designed to be the default isolation standard on Windows clients. It's built on [AppContainer][LINK-1], and offers several added security features to help the Windows platform defend against attacks that use vulnerabilities in applications or third-party libraries. To isolate their applications, developers can update them using Visual Studio.

Win32 app isolation follows a two-step process:

- In the first step, the Win32 application is launched as a low-integrity process using AppContainer, which is recognized as a security boundary by Windows. The process is limited to a specific set of Windows APIs by default and is unable to inject code into any process operating at a higher integrity level
- In the second step, least privilege is enforced by granting authorized access to Windows securable objects. This access is determined by capabilities that are added to the application manifest through MSIX packaging. *Securable objects* in this context refers to Windows resources whose access is safeguarded by capabilities. These capabilities enable the implantation of a [Discretionary Access Control List][LINK-2] on Windows

To help ensuring that isolated applications run smoothly, developers must define the access requirements for the application via access capability declarations in the application package manifest. The *Application Capability Profiler (ACP)* simplifies the entire process by allowing the application to run in *learn mode* with low privileges. Instead of denying access if the capability isn't present, ACP allows access and logs additional capabilities required for access if the application were to run isolated.

To create a smooth user experience that aligns with nonisolated, native Win32 applications, two key factors should be taken into consideration:

- Approaches for accessing data and privacy information
- Integrating Win32 apps for compatibility with other Windows interfaces

The first factor relates to implementing methods to manage access to files and privacy information within and outside the isolation boundary AppContainer. The second factor involves integrating Win32 apps with other Windows interfaces in a way that helps enable seamless functionality without causing perplexing user consent prompts.

[!INCLUDE [learn-more](includes/learn-more.md)]

- [Win32 app isolation][LINK-4]
- [Application Capability Profiler (ACP)][LINK-5]
- [Learn how to adopt Win32 app isolation with Visual Studio][LINK-6]
- [Sandboxing Python with Win32 app isolation][LINK-7]

## App containers

In addition to Windows Sandbox for Win32 apps, Universal Windows Platform (UWP) applications run in Windows containers known as *app containers*. App containers act as process and resource isolation boundaries, but unlike Docker containers, these are special containers designed to run Windows applications.

Processes that run in app containers operate at a low integrity level, meaning they have limited access to resources they don't own. Because the default integrity level of most resources is medium integrity level, the UWP app can access only a subset of the file system, registry, and other resources. The app container also enforces restrictions on network connectivity. For example, access to a local host isn't allowed. As a result, malware or infected apps have limited footprint for escape.

[!INCLUDE [learn-more](includes/learn-more.md)]

- [Windows and app container][LINK-8]

## Windows Sandbox

Windows Sandbox provides a lightweight desktop environment to safely run untrusted Win32 applications in isolation, using the same hardware-based virtualization technology as Hyper-V. Any untrusted Win32 app installed in Windows Sandbox stays only in the sandbox and can't affect the host.

Once Windows Sandbox is closed, nothing persists on the device. All the software with all its files and state are permanently deleted after the untrusted Win32 application is closed.

[!INCLUDE [learn-more](includes/learn-more.md)]

- [Windows Sandbox][LINK-9]

## Windows Subsystem for Linux (WSL)

With Windows Subsystem for Linux (WSL) you can run a Linux environment on a Windows device, without the need for a separate virtual machine or dual booting. WSL is designed to provide a seamless and productive experience for developers who want to use both Windows and Linux at the same time.

[!INCLUDE [new-24h2](includes/new-24h2.md)]

- **Hyper-V Firewall** is a network firewall solution that enables filtering of inbound and outbound traffic to/from WSL containers hosted by Windows
- **DNS Tunneling** is a networking setting that improves compatibility in different networking environments, making use of virtualization features to obtain DNS information rather than a networking packet
- **Auto proxy** is a networking setting that enforces WSL to use Windows' HTTP proxy information. Turn on when using a proxy on Windows, as it makes that proxy automatically apply to WSL distributions

These features can be set up using a device management solution such as Microsoft Intune<sup>[\[7\]](conclusion.md#footnote7)</sup>. Microsoft Defender for Endpoint (MDE) integrates with WSL, allowing it to monitor activities within a WSL distro and report them to the MDE dashboards.

[!INCLUDE [learn-more](includes/learn-more.md)]

- [Hyper-V Firewall][LINK-10]
- [DNS Tunneling][LINK-11]
- [Auto proxy][LINK-12]
- [Intune setting for WSL][LINK-13]
- [Microsoft Defender for Endpoint plug-in for WSL][LINK-14]

## :::image type="icon" source="images/new-button-title.svg" border="false"::: Virtualization-based security enclaves

A **Virtualization-based security enclave** is a software-based trusted execution environment (TEE) inside a host application. VBS enclaves enable developers to use VBS to protect their application's secrets from admin-level attacks. VBS enclaves are available on Windows 10 onwards on both x64 and ARM64.

[!INCLUDE [learn-more](includes/learn-more.md)]

- [Virtualization-based security enclave][LINK-15]

<!--links-->

[LINK-1]: /windows/win32/secauthz/implementing-an-appcontainer
[LINK-2]: /windows/win32/secauthz/access-control-lists
[LINK-4]: https://github.com/microsoft/win32-app-isolation
[LINK-5]: https://github.com/microsoft/win32-app-isolation/blob/main/docs/profiler/application-capability-profiler.md
[LINK-6]: https://github.com/microsoft/win32-app-isolation/blob/main/docs/packaging/packaging-with-visual-studio.md
[LINK-7]: https://blogs.windows.com/windowsdeveloper/2024/03/06/sandboxing-python-with-win32-app-isolation/
[LINK-8]: /windows/apps/windows-app-sdk/migrate-to-windows-app-sdk/feature-mapping-table?source=recommendations
[LINK-9]: /windows/security/threat-protection/windows-sandbox/windows-sandbox-overview
[LINK-10]: /windows/security/operating-system-security/network-security/windows-firewall/hyper-v-firewall
[LINK-11]: /windows/wsl/networking#dns-tunneling
[LINK-12]: /windows/wsl/networking#auto-proxy
[LINK-13]: /windows/wsl/intune
[LINK-14]: /defender-endpoint/mde-plugin-wsl
[LINK-15]: /windows/win32/trusted-execution/vbs-enclaves
