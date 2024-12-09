---
title: Windows 11 security book - Application and driver control
description: Application and driver control.
ms.topic: overview
ms.date: 11/18/2024
---

# Application and driver control

:::image type="content" source="images/application-security.png" alt-text="Diagram containing a list of application security features." lightbox="images/application-security.png" border="false":::

Windows 11 offers a rich application platform with layers of security like isolation and code integrity that help protect your valuable data. Developers can also take advantage of these
capabilities to build in security from the ground up to protect against breaches and malware.

## Smart App Control

Smart App Control prevents users from running malicious applications by blocking untrusted or unsigned applications. Smart App Control goes beyond previous built-in browser protections by adding another layer of security that is woven directly into the core of the OS at the process level. Using AI, Smart App Control only allows processes to run if they're predicted to be safe based on existing and new intelligence updated daily.

Smart App Control builds on top of the same cloud-based AI used in *App Control for Business* to predict the safety of an application, so that users can be confident that their applications are safe and reliable. Additionally, Smart App Control blocks unknown script files and macros from the web, greatly improving security for everyday users.

We've been making significant improvements to Smart App Control to increase the security, usability, and cloud intelligence response for apps in the Windows ecosystem. Users can get the latest and best experience with Smart App Control by keeping their devices up to date via Windows Update every month.

To ensure that users have a seamless experience with Smart App Control enabled, we ask developers to sign their applications with a code signing certificate from the Microsoft Trusted Root Program. Developers should include all binaries, such as exe, dll, temp installer files, and uninstallers. Trusted Signing makes the process of obtaining, maintaining, and signing with a trusted certificate simple and secure.

Smart App Control is disabled on devices enrolled in enterprise management. We suggest enterprises running line-of-business applications continue to use *App Control for Business*.

[!INCLUDE [learn-more](includes/learn-more.md)]

- [Smart App Control][LINK-1]

## App Control for Business

Your organization is only as secure as the applications that run on your devices. With *application control*, apps must earn trust to run, in contrast to an application trust model where all code is assumed trustworthy. By helping prevent unwanted or malicious code from running, application control is an important part of an effective security strategy. Many organizations cite application control as one of the most effective means of defending against executable file-based malware.

App Control for Business (previously called *Windows Defender Application Control*) and AppLocker are both included in Windows. App Control for Business is the next-generation app control solution for Windows and provides powerful control over what runs in your environment. Organizations that were using AppLocker on previous versions of Windows, can continue to use the feature as they consider whether to switch to App Control for Business for stronger protection.

Microsoft Intune<sup>[\[4\]](conclusion.md#footnote4)</sup> can configure App Control for Business in the admin console, including setting up Intune as a managed installer. Intune includes built-in options for App Control for Business and the possibility to upload policies as an XML file for Intune to package and deploy.

[!INCLUDE [learn-more](includes/learn-more.md)]

- [Application Control for Windows][LINK-2]
- [Automatically allow apps deployed by a managed installer with App Control for Business][LINK-3]

## :::image type="icon" source="images/soon-button-title.svg" border="false"::: Administrator protection

When users sign in with administrative rights to Windows, they have the power to make significant changes to the system, which can impact its overall security. These rights can be a target for malicious software.

Administrator protection is a new security feature in Windows 11 designed to safeguard these administrative rights. It allows administrators to perform all necessary functions with **just-in-time administrative rights**, while running most tasks without administrative privileges. The goal of administrator protection is to provide a secure and seamless experience, ensuring users operate with the least required privileges.

When administrator protection is enabled, if an app needs special permissions like administrative rights, the user is asked for approval. When an approval is needed, Windows Hello provides a secure and easy way to approve or deny these requests.

> [!NOTE]
> Administrator protection is currently in preview. For devices running previous versions of Windows, refer to [User Account Control (UAC)][LINK-5].

## Microsoft vulnerable driver blocklist

The Windows kernel is the most privileged software and is therefore a compelling target for malware authors. Since Windows has strict requirements for code running in the kernel, cybercriminals commonly exploit vulnerabilities in kernel drivers to get access. Microsoft works with ecosystem partners to constantly identify and respond to potentially vulnerable kernel drivers. To prevent vulnerable versions of drivers from running, Windows has a *block policy* turned on by default. Users can configure the policy from the Windows Security app.

[!INCLUDE [learn-more](includes/learn-more.md)]

- [Microsoft recommended driver block rules][LINK-4]

## :::image type="icon" source="images/new-button-title.svg" border="false"::: Trusted Signing

Trusted Signing is a Microsoft fully managed, end-to-end signing solution that simplifies the signing process and empowers third-party developers to easily build and distribute applications.

[!INCLUDE [learn-more](includes/learn-more.md)]

- [What is Trusted Signing](/azure/trusted-signing/overview)

<!--links-->

[LINK-1]: /windows/apps/develop/smart-app-control/overview
[LINK-2]: /windows/security/application-security/application-control/windows-defender-application-control/wdac
[LINK-3]: /windows/security/application-security/application-control/app-control-for-business/design/configure-authorized-apps-deployed-with-a-managed-installer
[LINK-4]: /windows/security/threat-protection/windows-defender-application-control/microsoft-recommended-driver-block-rules
[LINK-5]: /windows/security/identity-protection/user-account-control/how-user-account-control-works
