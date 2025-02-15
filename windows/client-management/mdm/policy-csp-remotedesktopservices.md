---
title: RemoteDesktopServices Policy CSP
description: Learn more about the RemoteDesktopServices Area in Policy CSP.
ms.date: 02/13/2025
ms.topic: generated-reference
---

<!-- Auto-Generated CSP Document -->

<!-- RemoteDesktopServices-Begin -->
# Policy CSP - RemoteDesktopServices

[!INCLUDE [ADMX-backed CSP tip](includes/mdm-admx-csp-note.md)]

[!INCLUDE [Windows Insider tip](includes/mdm-insider-csp-note.md)]

<!-- RemoteDesktopServices-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- RemoteDesktopServices-Editable-End -->

<!-- AllowUsersToConnectRemotely-Begin -->
## AllowUsersToConnectRemotely

<!-- AllowUsersToConnectRemotely-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ✅ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 10, version 1703 [10.0.15063] and later |
<!-- AllowUsersToConnectRemotely-Applicability-End -->

<!-- AllowUsersToConnectRemotely-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/RemoteDesktopServices/AllowUsersToConnectRemotely
```
<!-- AllowUsersToConnectRemotely-OmaUri-End -->

<!-- AllowUsersToConnectRemotely-Description-Begin -->
<!-- Description-Source-ADMX -->
This policy setting allows you to configure remote access to computers by using Remote Desktop Services.

- If you enable this policy setting, users who are members of the Remote Desktop Users group on the target computer can connect remotely to the target computer by using Remote Desktop Services.

- If you disable this policy setting, users can't connect remotely to the target computer by using Remote Desktop Services. The target computer will maintain any current connections, but won't accept any new incoming connections.

- If you don't configure this policy setting, Remote Desktop Services uses the Remote Desktop setting on the target computer to determine whether the remote connection is allowed. This setting is found on the Remote tab in the System properties sheet. By default, remote connections aren't allowed.

> [!NOTE]
> You can limit which clients are able to connect remotely by using Remote Desktop Services by configuring the policy setting at Computer Configuration\Administrative Templates\Windows Components\Remote Desktop Services\Remote Desktop Session Host\Security\Require user authentication for remote connections by using Network Level Authentication.

You can limit the number of users who can connect simultaneously by configuring the policy setting at Computer Configuration\Administrative Templates\Windows Components\Remote Desktop Services\Remote Desktop Session Host\Connections\Limit number of connections, or by configuring the policy setting Maximum Connections by using the Remote Desktop Session Host WMI Provider.
<!-- AllowUsersToConnectRemotely-Description-End -->

<!-- AllowUsersToConnectRemotely-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- AllowUsersToConnectRemotely-Editable-End -->

<!-- AllowUsersToConnectRemotely-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `chr` (string) |
| Access Type | Add, Delete, Get, Replace |
<!-- AllowUsersToConnectRemotely-DFProperties-End -->

<!-- AllowUsersToConnectRemotely-AdmxBacked-Begin -->
[!INCLUDE [ADMX-backed policy note](includes/mdm-admx-policy-note.md)]

**ADMX mapping**:

| Name | Value |
|:--|:--|
| Name | TS_DISABLE_CONNECTIONS |
| Friendly Name | Allow users to connect remotely by using Remote Desktop Services |
| Location | Computer Configuration |
| Path | Windows Components > Remote Desktop Services > Remote Desktop Session Host > Connections |
| Registry Key Name | SOFTWARE\Policies\Microsoft\Windows NT\Terminal Services |
| ADMX File Name | TerminalServer.admx |
<!-- AllowUsersToConnectRemotely-AdmxBacked-End -->

<!-- AllowUsersToConnectRemotely-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- AllowUsersToConnectRemotely-Examples-End -->

<!-- AllowUsersToConnectRemotely-End -->

<!-- ClientConnectionEncryptionLevel-Begin -->
## ClientConnectionEncryptionLevel

<!-- ClientConnectionEncryptionLevel-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ✅ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 10, version 1703 [10.0.15063] and later |
<!-- ClientConnectionEncryptionLevel-Applicability-End -->

<!-- ClientConnectionEncryptionLevel-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/RemoteDesktopServices/ClientConnectionEncryptionLevel
```
<!-- ClientConnectionEncryptionLevel-OmaUri-End -->

<!-- ClientConnectionEncryptionLevel-Description-Begin -->
<!-- Description-Source-ADMX -->
Specifies whether to require the use of a specific encryption level to secure communications between client computers and RD Session Host servers during Remote Desktop Protocol (RDP) connections. This policy only applies when you are using native RDP encryption. However, native RDP encryption (as opposed to SSL encryption) isn't recommended. This policy doesn't apply to SSL encryption.

- If you enable this policy setting, all communications between clients and RD Session Host servers during remote connections must use the encryption method specified in this setting. By default, the encryption level is set to High. The following encryption methods are available:

* High: The High setting encrypts data sent from the client to the server and from the server to the client by using strong 128-bit encryption. Use this encryption level in environments that contain only 128-bit clients (for example, clients that run Remote Desktop Connection). Clients that don't support this encryption level can't connect to RD Session Host servers.

* Client Compatible: The Client Compatible setting encrypts data sent between the client and the server at the maximum key strength supported by the client. Use this encryption level in environments that include clients that don't support 128-bit encryption.

* Low: The Low setting encrypts only data sent from the client to the server by using 56-bit encryption.

- If you disable or don't configure this setting, the encryption level to be used for remote connections to RD Session Host servers isn't enforced through Group Policy.

Important.

FIPS compliance can be configured through the System cryptography. Use FIPS compliant algorithms for encryption, hashing, and signing settings in Group Policy (under Computer Configuration\Windows Settings\Security Settings\Local Policies\Security Options). The FIPS compliant setting encrypts and decrypts data sent from the client to the server and from the server to the client, with the Federal Information Processing Standard (FIPS) 140 encryption algorithms, by using Microsoft cryptographic modules. Use this encryption level when communications between clients and RD Session Host servers requires the highest level of encryption.
<!-- ClientConnectionEncryptionLevel-Description-End -->

<!-- ClientConnectionEncryptionLevel-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- ClientConnectionEncryptionLevel-Editable-End -->

<!-- ClientConnectionEncryptionLevel-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `chr` (string) |
| Access Type | Add, Delete, Get, Replace |
<!-- ClientConnectionEncryptionLevel-DFProperties-End -->

<!-- ClientConnectionEncryptionLevel-AdmxBacked-Begin -->
[!INCLUDE [ADMX-backed policy note](includes/mdm-admx-policy-note.md)]

**ADMX mapping**:

| Name | Value |
|:--|:--|
| Name | TS_ENCRYPTION_POLICY |
| Friendly Name | Set client connection encryption level |
| Location | Computer Configuration |
| Path | Windows Components > Remote Desktop Services > Remote Desktop Session Host > Security |
| Registry Key Name | SOFTWARE\Policies\Microsoft\Windows NT\Terminal Services |
| ADMX File Name | TerminalServer.admx |
<!-- ClientConnectionEncryptionLevel-AdmxBacked-End -->

<!-- ClientConnectionEncryptionLevel-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- ClientConnectionEncryptionLevel-Examples-End -->

<!-- ClientConnectionEncryptionLevel-End -->

<!-- DisconnectOnLockLegacyAuthn-Begin -->
## DisconnectOnLockLegacyAuthn

<!-- DisconnectOnLockLegacyAuthn-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ✅ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ [10.0.20348.2461] and later <br> ✅ [10.0.25398.887] and later <br> ✅ Windows 10, version 2004 [10.0.19041.4474] and later <br> ✅ Windows 11, version 21H2 with [KB5037770](https://support.microsoft.com/help/5037770) [10.0.22000.2960] and later <br> ✅ Windows 11, version 22H2 with [KB5037771](https://support.microsoft.com/help/5037771) [10.0.22621.3593] and later <br> ✅ Windows 11, version 24H2 [10.0.26100] and later |
<!-- DisconnectOnLockLegacyAuthn-Applicability-End -->

<!-- DisconnectOnLockLegacyAuthn-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/RemoteDesktopServices/DisconnectOnLockLegacyAuthn
```
<!-- DisconnectOnLockLegacyAuthn-OmaUri-End -->

<!-- DisconnectOnLockLegacyAuthn-Description-Begin -->
<!-- Description-Source-ADMX -->
This policy setting allows you to configure the user experience when the Remote Desktop session is locked by the user or by a policy. You can specify whether the remote session will show the remote lock screen or disconnect when the remote session is locked. Disconnecting the remote session ensures that a remote session can't be left on the lock screen and can't reconnect automatically due to loss of network connectivity.

This policy applies only when using legacy authentication to authenticate to the remote PC. Legacy authentication is limited to username and password, or certificates like smartcards. Legacy authentication doesn't leverage the Microsoft identity platform, such as Microsoft Entra ID. Legacy authentication includes the NTLM, CredSSP, RDSTLS, TLS, and RDP basic authentication protocols.

- If you enable this policy setting, Remote Desktop connections using legacy authentication will disconnect the remote session when the remote session is locked. Users can reconnect when they're ready and re-enter their credentials when prompted.

- If you disable or don't configure this policy setting, Remote Desktop connections using legacy authentication will show the remote lock screen when the remote session is locked. Users can unlock the remote session using their username and password, or certificates.
<!-- DisconnectOnLockLegacyAuthn-Description-End -->

<!-- DisconnectOnLockLegacyAuthn-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- DisconnectOnLockLegacyAuthn-Editable-End -->

<!-- DisconnectOnLockLegacyAuthn-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `chr` (string) |
| Access Type | Add, Delete, Get, Replace |
<!-- DisconnectOnLockLegacyAuthn-DFProperties-End -->

<!-- DisconnectOnLockLegacyAuthn-AdmxBacked-Begin -->
[!INCLUDE [ADMX-backed policy note](includes/mdm-admx-policy-note.md)]

**ADMX mapping**:

| Name | Value |
|:--|:--|
| Name | TS_DISCONNECT_ON_LOCK_POLICY |
| Friendly Name | Disconnect remote session on lock for legacy authentication |
| Location | Computer Configuration |
| Path | Windows Components > Remote Desktop Services > Remote Desktop Session Host > Security |
| Registry Key Name | SOFTWARE\Policies\Microsoft\Windows NT\Terminal Services |
| Registry Value Name | fDisconnectOnLockLegacy |
| ADMX File Name | TerminalServer.admx |
<!-- DisconnectOnLockLegacyAuthn-AdmxBacked-End -->

<!-- DisconnectOnLockLegacyAuthn-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- DisconnectOnLockLegacyAuthn-Examples-End -->

<!-- DisconnectOnLockLegacyAuthn-End -->

<!-- DisconnectOnLockMicrosoftIdentityAuthn-Begin -->
## DisconnectOnLockMicrosoftIdentityAuthn

<!-- DisconnectOnLockMicrosoftIdentityAuthn-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ✅ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ [10.0.20348.2461] and later <br> ✅ [10.0.25398.887] and later <br> ✅ Windows 10, version 2004 [10.0.19041.4474] and later <br> ✅ Windows 11, version 21H2 with [KB5037770](https://support.microsoft.com/help/5037770) [10.0.22000.2960] and later <br> ✅ Windows 11, version 22H2 with [KB5037771](https://support.microsoft.com/help/5037771) [10.0.22621.3593] and later <br> ✅ Windows 11, version 24H2 [10.0.26100] and later |
<!-- DisconnectOnLockMicrosoftIdentityAuthn-Applicability-End -->

<!-- DisconnectOnLockMicrosoftIdentityAuthn-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/RemoteDesktopServices/DisconnectOnLockMicrosoftIdentityAuthn
```
<!-- DisconnectOnLockMicrosoftIdentityAuthn-OmaUri-End -->

<!-- DisconnectOnLockMicrosoftIdentityAuthn-Description-Begin -->
<!-- Description-Source-ADMX -->
This policy setting allows you to configure the user experience when the Remote Desktop session is locked by the user or by a policy. You can specify whether the remote session will show the remote lock screen or disconnect when the remote session is locked. Disconnecting the remote session ensures that a remote session can't be left on the lock screen and can't reconnect automatically due to loss of network connectivity.

This policy applies only when using an identity provider that uses the Microsoft identity platform, such as Microsoft Entra ID, to authenticate to the remote PC. This policy doesn't apply when using Legacy authentication which includes the NTLM, CredSSP, RDSTLS, TLS, and RDP basic authentication protocols.

- If you enable or don't configure this policy setting, Remote Desktop connections using the Microsoft identity platform will disconnect the remote session when the remote session is locked. Users can reconnect when they're ready and can use passwordless authentication if configured.

- If you disable this policy setting, Remote Desktop connections using the Microsoft identity platform will show the remote lock screen when the remote session is locked. Users can unlock the remote session using their username and password, or certificates.
<!-- DisconnectOnLockMicrosoftIdentityAuthn-Description-End -->

<!-- DisconnectOnLockMicrosoftIdentityAuthn-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- DisconnectOnLockMicrosoftIdentityAuthn-Editable-End -->

<!-- DisconnectOnLockMicrosoftIdentityAuthn-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `chr` (string) |
| Access Type | Add, Delete, Get, Replace |
<!-- DisconnectOnLockMicrosoftIdentityAuthn-DFProperties-End -->

<!-- DisconnectOnLockMicrosoftIdentityAuthn-AdmxBacked-Begin -->
[!INCLUDE [ADMX-backed policy note](includes/mdm-admx-policy-note.md)]

**ADMX mapping**:

| Name | Value |
|:--|:--|
| Name | TS_DISCONNECT_ON_LOCK_AAD_POLICY |
| Friendly Name | Disconnect remote session on lock for Microsoft identity platform authentication |
| Location | Computer Configuration |
| Path | Windows Components > Remote Desktop Services > Remote Desktop Session Host > Security |
| Registry Key Name | SOFTWARE\Policies\Microsoft\Windows NT\Terminal Services |
| Registry Value Name | fDisconnectOnLockMicrosoftIdentity |
| ADMX File Name | TerminalServer.admx |
<!-- DisconnectOnLockMicrosoftIdentityAuthn-AdmxBacked-End -->

<!-- DisconnectOnLockMicrosoftIdentityAuthn-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- DisconnectOnLockMicrosoftIdentityAuthn-Examples-End -->

<!-- DisconnectOnLockMicrosoftIdentityAuthn-End -->

<!-- DoNotAllowDriveRedirection-Begin -->
## DoNotAllowDriveRedirection

<!-- DoNotAllowDriveRedirection-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ✅ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 10, version 1703 [10.0.15063] and later |
<!-- DoNotAllowDriveRedirection-Applicability-End -->

<!-- DoNotAllowDriveRedirection-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/RemoteDesktopServices/DoNotAllowDriveRedirection
```
<!-- DoNotAllowDriveRedirection-OmaUri-End -->

<!-- DoNotAllowDriveRedirection-Description-Begin -->
<!-- Description-Source-ADMX -->
This policy setting specifies whether to prevent the mapping of client drives in a Remote Desktop Services session (drive redirection).

By default, an RD Session Host server maps client drives automatically upon connection. Mapped drives appear in the session folder tree in File Explorer or Computer in the format `<driveletter>` on `<computername>`. You can use this policy setting to override this behavior.

- If you enable this policy setting, client drive redirection isn't allowed in Remote Desktop Services sessions, and Clipboard file copy redirection isn't allowed on computers running Windows XP, Windows Server 2003, Windows Server 2012 (and later) or Windows 8 (and later).

- If you disable this policy setting, client drive redirection is always allowed. In addition, Clipboard file copy redirection is always allowed if Clipboard redirection is allowed.

- If you don't configure this policy setting, client drive redirection and Clipboard file copy redirection aren't specified at the Group Policy level.
<!-- DoNotAllowDriveRedirection-Description-End -->

<!-- DoNotAllowDriveRedirection-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- DoNotAllowDriveRedirection-Editable-End -->

<!-- DoNotAllowDriveRedirection-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `chr` (string) |
| Access Type | Add, Delete, Get, Replace |
<!-- DoNotAllowDriveRedirection-DFProperties-End -->

<!-- DoNotAllowDriveRedirection-AdmxBacked-Begin -->
[!INCLUDE [ADMX-backed policy note](includes/mdm-admx-policy-note.md)]

**ADMX mapping**:

| Name | Value |
|:--|:--|
| Name | TS_CLIENT_DRIVE_M |
| Friendly Name | Do not allow drive redirection |
| Location | Computer Configuration |
| Path | Windows Components > Remote Desktop Services > Remote Desktop Session Host > Device and Resource Redirection |
| Registry Key Name | SOFTWARE\Policies\Microsoft\Windows NT\Terminal Services |
| Registry Value Name | fDisableCdm |
| ADMX File Name | TerminalServer.admx |
<!-- DoNotAllowDriveRedirection-AdmxBacked-End -->

<!-- DoNotAllowDriveRedirection-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- DoNotAllowDriveRedirection-Examples-End -->

<!-- DoNotAllowDriveRedirection-End -->

<!-- DoNotAllowPasswordSaving-Begin -->
## DoNotAllowPasswordSaving

<!-- DoNotAllowPasswordSaving-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ✅ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 10, version 1703 [10.0.15063] and later |
<!-- DoNotAllowPasswordSaving-Applicability-End -->

<!-- DoNotAllowPasswordSaving-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/RemoteDesktopServices/DoNotAllowPasswordSaving
```
<!-- DoNotAllowPasswordSaving-OmaUri-End -->

<!-- DoNotAllowPasswordSaving-Description-Begin -->
<!-- Description-Source-ADMX -->
Controls whether passwords can be saved on this computer from Remote Desktop Connection.

- If you enable this setting the password saving checkbox in Remote Desktop Connection will be disabled and users will no longer be able to save passwords. When a user opens an RDP file using Remote Desktop Connection and saves his settings, any password that previously existed in the RDP file will be deleted.

- If you disable this setting or leave it not configured, the user will be able to save passwords using Remote Desktop Connection.
<!-- DoNotAllowPasswordSaving-Description-End -->

<!-- DoNotAllowPasswordSaving-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- DoNotAllowPasswordSaving-Editable-End -->

<!-- DoNotAllowPasswordSaving-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `chr` (string) |
| Access Type | Add, Delete, Get, Replace |
<!-- DoNotAllowPasswordSaving-DFProperties-End -->

<!-- DoNotAllowPasswordSaving-AdmxBacked-Begin -->
[!INCLUDE [ADMX-backed policy note](includes/mdm-admx-policy-note.md)]

**ADMX mapping**:

| Name | Value |
|:--|:--|
| Name | TS_CLIENT_DISABLE_PASSWORD_SAVING_2 |
| Friendly Name | Do not allow passwords to be saved |
| Location | Computer Configuration |
| Path | Windows Components > Remote Desktop Services > Remote Desktop Connection Client |
| Registry Key Name | SOFTWARE\Policies\Microsoft\Windows NT\Terminal Services |
| Registry Value Name | DisablePasswordSaving |
| ADMX File Name | TerminalServer.admx |
<!-- DoNotAllowPasswordSaving-AdmxBacked-End -->

<!-- DoNotAllowPasswordSaving-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- DoNotAllowPasswordSaving-Examples-End -->

<!-- DoNotAllowPasswordSaving-End -->

<!-- DoNotAllowWebAuthnRedirection-Begin -->
## DoNotAllowWebAuthnRedirection

<!-- DoNotAllowWebAuthnRedirection-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ✅ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 11, version 22H2 [10.0.22621] and later |
<!-- DoNotAllowWebAuthnRedirection-Applicability-End -->

<!-- DoNotAllowWebAuthnRedirection-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/RemoteDesktopServices/DoNotAllowWebAuthnRedirection
```
<!-- DoNotAllowWebAuthnRedirection-OmaUri-End -->

<!-- DoNotAllowWebAuthnRedirection-Description-Begin -->
<!-- Description-Source-ADMX -->
This policy setting lets you control the redirection of web authentication (WebAuthn) requests from a Remote Desktop session to the local device. This redirection enables users to authenticate to resources inside the Remote Desktop session using their local authenticator (e.g., Windows Hello for Business, security key, or other).

By default, Remote Desktop allows redirection of WebAuthn requests.

- If you enable this policy setting, users can't use their local authenticator inside the Remote Desktop session.

- If you disable or don't configure this policy setting, users can use local authenticators inside the Remote Desktop session.
<!-- DoNotAllowWebAuthnRedirection-Description-End -->

<!-- DoNotAllowWebAuthnRedirection-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- DoNotAllowWebAuthnRedirection-Editable-End -->

<!-- DoNotAllowWebAuthnRedirection-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `chr` (string) |
| Access Type | Add, Delete, Get, Replace |
<!-- DoNotAllowWebAuthnRedirection-DFProperties-End -->

<!-- DoNotAllowWebAuthnRedirection-AdmxBacked-Begin -->
[!INCLUDE [ADMX-backed policy note](includes/mdm-admx-policy-note.md)]

**ADMX mapping**:

| Name | Value |
|:--|:--|
| Name | TS_WEBAUTHN |
| Friendly Name | Do not allow WebAuthn redirection |
| Location | Computer Configuration |
| Path | Windows Components > Remote Desktop Services > Remote Desktop Session Host > Device and Resource Redirection |
| Registry Key Name | SOFTWARE\Policies\Microsoft\Windows NT\Terminal Services |
| Registry Value Name | fDisableWebAuthn |
| ADMX File Name | TerminalServer.admx |
<!-- DoNotAllowWebAuthnRedirection-AdmxBacked-End -->

<!-- DoNotAllowWebAuthnRedirection-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- DoNotAllowWebAuthnRedirection-Examples-End -->

<!-- DoNotAllowWebAuthnRedirection-End -->

<!-- LimitClientToServerClipboardRedirection-Begin -->
## LimitClientToServerClipboardRedirection

<!-- LimitClientToServerClipboardRedirection-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ✅ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ✅ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ [10.0.20348.2523] and later <br> ✅ [10.0.25398.946] and later <br> ✅ Windows 11, version 21H2 [10.0.22000.3014] and later <br> ✅ Windows 11, version 22H2 with [KB5037853](https://support.microsoft.com/help/5037853) [10.0.22621.3672] and later <br> ✅ Windows 11, version 23H2 with [KB5037853](https://support.microsoft.com/help/5037853) [10.0.22631.3672] and later <br> ✅ Windows 11, version 24H2 [10.0.26100] and later |
<!-- LimitClientToServerClipboardRedirection-Applicability-End -->

<!-- LimitClientToServerClipboardRedirection-OmaUri-Begin -->
```User
./User/Vendor/MSFT/Policy/Config/RemoteDesktopServices/LimitClientToServerClipboardRedirection
```

```Device
./Device/Vendor/MSFT/Policy/Config/RemoteDesktopServices/LimitClientToServerClipboardRedirection
```
<!-- LimitClientToServerClipboardRedirection-OmaUri-End -->

<!-- LimitClientToServerClipboardRedirection-Description-Begin -->
<!-- Description-Source-ADMX -->
This policy setting allows you to restrict clipboard data transfers from client to server.

- If you enable this policy setting, you must choose from the following behaviors:

- Disable clipboard transfers from client to server.

- Allow plain text copying from client to server.

- Allow plain text and images copying from client to server.

- Allow plain text, images and Rich Text Format copying from client to server.

- Allow plain text, images, Rich Text Format and HTML copying from client to server.

- If you disable or don't configure this policy setting, users can copy arbitrary contents from client to server if clipboard redirection is enabled.

> [!NOTE]
> This policy setting appears in both Computer Configuration and User Configuration. If both policy settings are configured, the stricter restriction will be used.
<!-- LimitClientToServerClipboardRedirection-Description-End -->

<!-- LimitClientToServerClipboardRedirection-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- LimitClientToServerClipboardRedirection-Editable-End -->

<!-- LimitClientToServerClipboardRedirection-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `chr` (string) |
| Access Type | Add, Delete, Get, Replace |
<!-- LimitClientToServerClipboardRedirection-DFProperties-End -->

<!-- LimitClientToServerClipboardRedirection-AdmxBacked-Begin -->
[!INCLUDE [ADMX-backed policy note](includes/mdm-admx-policy-note.md)]

**ADMX mapping**:

| Name | Value |
|:--|:--|
| Name | TS_CLIENT_CLIPBOARDRESTRICTION_CS |
| Friendly Name | Restrict clipboard transfer from client to server |
| Location | Computer and User Configuration |
| Path | Windows Components > Remote Desktop Services > Remote Desktop Session Host > Device and Resource Redirection |
| Registry Key Name | SOFTWARE\Policies\Microsoft\Windows NT\Terminal Services |
| ADMX File Name | TerminalServer.admx |
<!-- LimitClientToServerClipboardRedirection-AdmxBacked-End -->

<!-- LimitClientToServerClipboardRedirection-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- LimitClientToServerClipboardRedirection-Examples-End -->

<!-- LimitClientToServerClipboardRedirection-End -->

<!-- LimitServerToClientClipboardRedirection-Begin -->
## LimitServerToClientClipboardRedirection

<!-- LimitServerToClientClipboardRedirection-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ✅ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ✅ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ [10.0.20348.2523] and later <br> ✅ [10.0.25398.946] and later <br> ✅ Windows 11, version 21H2 [10.0.22000.3014] and later <br> ✅ Windows 11, version 22H2 with [KB5037853](https://support.microsoft.com/help/5037853) [10.0.22621.3672] and later <br> ✅ Windows 11, version 23H2 with [KB5037853](https://support.microsoft.com/help/5037853) [10.0.22631.3672] and later <br> ✅ Windows 11, version 24H2 [10.0.26100] and later |
<!-- LimitServerToClientClipboardRedirection-Applicability-End -->

<!-- LimitServerToClientClipboardRedirection-OmaUri-Begin -->
```User
./User/Vendor/MSFT/Policy/Config/RemoteDesktopServices/LimitServerToClientClipboardRedirection
```

```Device
./Device/Vendor/MSFT/Policy/Config/RemoteDesktopServices/LimitServerToClientClipboardRedirection
```
<!-- LimitServerToClientClipboardRedirection-OmaUri-End -->

<!-- LimitServerToClientClipboardRedirection-Description-Begin -->
<!-- Description-Source-ADMX -->
This policy setting allows you to restrict clipboard data transfers from server to client.

- If you enable this policy setting, you must choose from the following behaviors:

- Disable clipboard transfers from server to client.

- Allow plain text copying from server to client.

- Allow plain text and images copying from server to client.

- Allow plain text, images and Rich Text Format copying from server to client.

- Allow plain text, images, Rich Text Format and HTML copying from server to client.

- If you disable or don't configure this policy setting, users can copy arbitrary contents from server to client if clipboard redirection is enabled.

> [!NOTE]
> This policy setting appears in both Computer Configuration and User Configuration. If both policy settings are configured, the stricter restriction will be used.
<!-- LimitServerToClientClipboardRedirection-Description-End -->

<!-- LimitServerToClientClipboardRedirection-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- LimitServerToClientClipboardRedirection-Editable-End -->

<!-- LimitServerToClientClipboardRedirection-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `chr` (string) |
| Access Type | Add, Delete, Get, Replace |
<!-- LimitServerToClientClipboardRedirection-DFProperties-End -->

<!-- LimitServerToClientClipboardRedirection-AdmxBacked-Begin -->
[!INCLUDE [ADMX-backed policy note](includes/mdm-admx-policy-note.md)]

**ADMX mapping**:

| Name | Value |
|:--|:--|
| Name | TS_CLIENT_CLIPBOARDRESTRICTION_SC |
| Friendly Name | Restrict clipboard transfer from server to client |
| Location | Computer and User Configuration |
| Path | Windows Components > Remote Desktop Services > Remote Desktop Session Host > Device and Resource Redirection |
| Registry Key Name | SOFTWARE\Policies\Microsoft\Windows NT\Terminal Services |
| ADMX File Name | TerminalServer.admx |
<!-- LimitServerToClientClipboardRedirection-AdmxBacked-End -->

<!-- LimitServerToClientClipboardRedirection-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- LimitServerToClientClipboardRedirection-Examples-End -->

<!-- LimitServerToClientClipboardRedirection-End -->

<!-- PromptForPasswordUponConnection-Begin -->
## PromptForPasswordUponConnection

<!-- PromptForPasswordUponConnection-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ✅ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 10, version 1703 [10.0.15063] and later |
<!-- PromptForPasswordUponConnection-Applicability-End -->

<!-- PromptForPasswordUponConnection-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/RemoteDesktopServices/PromptForPasswordUponConnection
```
<!-- PromptForPasswordUponConnection-OmaUri-End -->

<!-- PromptForPasswordUponConnection-Description-Begin -->
<!-- Description-Source-ADMX -->
This policy setting specifies whether Remote Desktop Services always prompts the client for a password upon connection.

You can use this setting to enforce a password prompt for users logging on to Remote Desktop Services, even if they already provided the password in the Remote Desktop Connection client.

By default, Remote Desktop Services allows users to automatically log on by entering a password in the Remote Desktop Connection client.

- If you enable this policy setting, users can't automatically log on to Remote Desktop Services by supplying their passwords in the Remote Desktop Connection client. They are prompted for a password to log on.

- If you disable this policy setting, users can always log on to Remote Desktop Services automatically by supplying their passwords in the Remote Desktop Connection client.

- If you don't configure this policy setting, automatic logon isn't specified at the Group Policy level.
<!-- PromptForPasswordUponConnection-Description-End -->

<!-- PromptForPasswordUponConnection-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- PromptForPasswordUponConnection-Editable-End -->

<!-- PromptForPasswordUponConnection-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `chr` (string) |
| Access Type | Add, Delete, Get, Replace |
<!-- PromptForPasswordUponConnection-DFProperties-End -->

<!-- PromptForPasswordUponConnection-AdmxBacked-Begin -->
[!INCLUDE [ADMX-backed policy note](includes/mdm-admx-policy-note.md)]

**ADMX mapping**:

| Name | Value |
|:--|:--|
| Name | TS_PASSWORD |
| Friendly Name | Always prompt for password upon connection |
| Location | Computer Configuration |
| Path | Windows Components > Remote Desktop Services > Remote Desktop Session Host > Security |
| Registry Key Name | SOFTWARE\Policies\Microsoft\Windows NT\Terminal Services |
| Registry Value Name | fPromptForPassword |
| ADMX File Name | TerminalServer.admx |
<!-- PromptForPasswordUponConnection-AdmxBacked-End -->

<!-- PromptForPasswordUponConnection-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- PromptForPasswordUponConnection-Examples-End -->

<!-- PromptForPasswordUponConnection-End -->

<!-- RequireSecureRPCCommunication-Begin -->
## RequireSecureRPCCommunication

<!-- RequireSecureRPCCommunication-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ✅ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ Windows 10, version 1703 [10.0.15063] and later |
<!-- RequireSecureRPCCommunication-Applicability-End -->

<!-- RequireSecureRPCCommunication-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/RemoteDesktopServices/RequireSecureRPCCommunication
```
<!-- RequireSecureRPCCommunication-OmaUri-End -->

<!-- RequireSecureRPCCommunication-Description-Begin -->
<!-- Description-Source-ADMX -->
Specifies whether a Remote Desktop Session Host server requires secure RPC communication with all clients or allows unsecured communication.

You can use this setting to strengthen the security of RPC communication with clients by allowing only authenticated and encrypted requests.

If the status is set to Enabled, Remote Desktop Services accepts requests from RPC clients that support secure requests, and doesn't allow unsecured communication with untrusted clients.

If the status is set to Disabled, Remote Desktop Services always requests security for all RPC traffic. However, unsecured communication is allowed for RPC clients that don't respond to the request.

If the status is set to Not Configured, unsecured communication is allowed.

> [!NOTE]
> The RPC interface is used for administering and configuring Remote Desktop Services.
<!-- RequireSecureRPCCommunication-Description-End -->

<!-- RequireSecureRPCCommunication-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- RequireSecureRPCCommunication-Editable-End -->

<!-- RequireSecureRPCCommunication-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `chr` (string) |
| Access Type | Add, Delete, Get, Replace |
<!-- RequireSecureRPCCommunication-DFProperties-End -->

<!-- RequireSecureRPCCommunication-AdmxBacked-Begin -->
[!INCLUDE [ADMX-backed policy note](includes/mdm-admx-policy-note.md)]

**ADMX mapping**:

| Name | Value |
|:--|:--|
| Name | TS_RPC_ENCRYPTION |
| Friendly Name | Require secure RPC communication |
| Location | Computer Configuration |
| Path | Windows Components > Remote Desktop Services > Remote Desktop Session Host > Security |
| Registry Key Name | SOFTWARE\Policies\Microsoft\Windows NT\Terminal Services |
| Registry Value Name | fEncryptRPCTraffic |
| ADMX File Name | TerminalServer.admx |
<!-- RequireSecureRPCCommunication-AdmxBacked-End -->

<!-- RequireSecureRPCCommunication-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- RequireSecureRPCCommunication-Examples-End -->

<!-- RequireSecureRPCCommunication-End -->

<!-- TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME-Begin -->
## TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME

<!-- TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME-Applicability-Begin -->
| Scope | Editions | Applicable OS |
|:--|:--|:--|
| ✅ Device <br> ❌ User | ✅ Pro <br> ✅ Enterprise <br> ✅ Education <br> ✅ Windows SE <br> ✅ IoT Enterprise / IoT Enterprise LTSC | ✅ [10.0.20348.2400] and later <br> ✅ [10.0.25398.827] and later <br> ✅ Windows 11, version 21H2 [10.0.22000.2898] and later <br> ✅ Windows 11, version 22H2 with [KB5035942](https://support.microsoft.com/help/5035942) [10.0.22621.3374] and later <br> ✅ Windows 11, version 23H2 with [KB5035942](https://support.microsoft.com/help/5035942) [10.0.22631.3374] and later <br> ✅ Windows Insider Preview |
<!-- TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME-Applicability-End -->

<!-- TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME-OmaUri-Begin -->
```Device
./Device/Vendor/MSFT/Policy/Config/RemoteDesktopServices/TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME
```
<!-- TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME-OmaUri-End -->

<!-- TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME-Description-Begin -->
<!-- Description-Source-Not-Found -->
<!-- TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME-Description-End -->

<!-- TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME-Editable-Begin -->
<!-- Add any additional information about this policy here. Anything outside this section will get overwritten. -->
<!-- TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME-Editable-End -->

<!-- TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME-DFProperties-Begin -->
**Description framework properties**:

| Property name | Property value |
|:--|:--|
| Format | `chr` (string) |
| Access Type | Add, Delete, Get, Replace |
<!-- TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME-DFProperties-End -->

<!-- TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME-AdmxBacked-Begin -->
<!-- ADMX-Not-Found -->
[!INCLUDE [ADMX-backed policy note](includes/mdm-admx-policy-note.md)]

**ADMX mapping**:

| Name | Value |
|:--|:--|
| Name | TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME |
| ADMX File Name | TerminalServer.admx |
<!-- TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME-AdmxBacked-End -->

<!-- TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME-Examples-Begin -->
<!-- Add any examples for this policy here. Examples outside this section will get overwritten. -->
<!-- TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME-Examples-End -->

<!-- TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME-End -->

<!-- RemoteDesktopServices-CspMoreInfo-Begin -->
<!-- Add any additional information about this CSP here. Anything outside this section will get overwritten. -->
<!-- RemoteDesktopServices-CspMoreInfo-End -->

<!-- RemoteDesktopServices-End -->

## Related articles

[Policy configuration service provider](policy-configuration-service-provider.md)
