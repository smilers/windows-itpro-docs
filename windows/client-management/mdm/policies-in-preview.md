---
title: Configuration service provider preview policies
description: Learn more about configuration service provider (CSP) policies that are available for Windows Insider Preview.
ms.date: 02/13/2025
ms.topic: generated-reference
---

<!-- Auto-Generated CSP Document -->

# Configuration service provider policies in preview

[!INCLUDE [Windows Insider tip](includes/mdm-insider-csp-note.md)]

This article lists the policies that are applicable for Windows Insider Preview builds.

## AppDeviceInventory

- [TurnOffInstallTracing](policy-csp-appdeviceinventory.md#turnoffinstalltracing)
- [TurnOffAPISamping](policy-csp-appdeviceinventory.md#turnoffapisamping)
- [TurnOffApplicationFootprint](policy-csp-appdeviceinventory.md#turnoffapplicationfootprint)
- [TurnOffWin32AppBackup](policy-csp-appdeviceinventory.md#turnoffwin32appbackup)

## ApplicationManagement

- [AllowedNonAdminPackageFamilyNameRules](policy-csp-applicationmanagement.md#allowednonadminpackagefamilynamerules)

## ClientCertificateInstall CSP

- [AttestPrivateKey](clientcertificateinstall-csp.md#userscepuniqueidinstallattestprivatekey)

## CloudDesktop CSP

- [EnablePhysicalDeviceAccessOnCtrlAltDel](clouddesktop-csp.md#userenablephysicaldeviceaccessonctrlaltdel)
- [EnablePhysicalDeviceAccessOnErrorScreens](clouddesktop-csp.md#userenablephysicaldeviceaccessonerrorscreens)
- [EnableBootToCloudSharedPCMode](clouddesktop-csp.md#deviceenableboottocloudsharedpcmode)

## Connectivity

- [DisableCrossDeviceResume](policy-csp-connectivity.md#disablecrossdeviceresume)
- [UseCellularWhenWiFiPoor](policy-csp-connectivity.md#usecellularwhenwifipoor)
- [DisableCellularSettingsPage](policy-csp-connectivity.md#disablecellularsettingspage)
- [DisableCellularOperatorSettingsPage](policy-csp-connectivity.md#disablecellularoperatorsettingspage)

## DeclaredConfiguration CSP

- [Document](declaredconfiguration-csp.md#hostcompletedocumentsdociddocument)
- [Abandoned](declaredconfiguration-csp.md#hostcompletedocumentsdocidpropertiesabandoned)
- [ConflictResolution](declaredconfiguration-csp.md#managementserviceconfigurationconflictresolution)

## DeliveryOptimization

- [DODisallowCacheServerDownloadsOnVPN](policy-csp-deliveryoptimization.md#dodisallowcacheserverdownloadsonvpn)
- [DOVpnKeywords](policy-csp-deliveryoptimization.md#dovpnkeywords)

## DeviceGuard

- [MachineIdentityIsolation](policy-csp-deviceguard.md#machineidentityisolation)

## DevicePreparation CSP

- [PageEnabled](devicepreparation-csp.md#pageenabled)
- [PageStatus](devicepreparation-csp.md#pagestatus)
- [PageErrorPhase](devicepreparation-csp.md#pageerrorphase)
- [PageErrorCode](devicepreparation-csp.md#pageerrorcode)
- [PageErrorDetails](devicepreparation-csp.md#pageerrordetails)
- [PageSettings](devicepreparation-csp.md#pagesettings)
- [ExecutionContext](devicepreparation-csp.md#bootstrapperagentexecutioncontext)
- [Progress](devicepreparation-csp.md#mdmproviderprogress)
- [MdmAgentInstalled](devicepreparation-csp.md#mdmprovidermdmagentinstalled)
- [RebootRequired](devicepreparation-csp.md#mdmproviderrebootrequired)

## Display

- [ConfigureMultipleDisplayMode](policy-csp-display.md#configuremultipledisplaymode)
- [SetClonePreferredResolutionSource](policy-csp-display.md#setclonepreferredresolutionsource)

## DMClient CSP

- [DiscoveryEndpoint](dmclient-csp.md#deviceproviderprovideridlinkedenrollmentdiscoveryendpoint)
- [Enabled](dmclient-csp.md#deviceproviderprovideridconfigrefreshenabled)
- [Cadence](dmclient-csp.md#deviceproviderprovideridconfigrefreshcadence)
- [PausePeriod](dmclient-csp.md#deviceproviderprovideridconfigrefreshpauseperiod)

## FileSystem

- [EnableDevDrive](policy-csp-filesystem.md#enabledevdrive)
- [DevDriveAttachPolicy](policy-csp-filesystem.md#devdriveattachpolicy)

## HealthAttestation CSP

- [AttestErrorMessage](healthattestation-csp.md#attesterrormessage)

## HumanPresence

- [ForcePrivacyScreen](policy-csp-humanpresence.md#forceprivacyscreen)
- [ForcePrivacyScreenDim](policy-csp-humanpresence.md#forceprivacyscreendim)
- [ForcePrivacyScreenNotification](policy-csp-humanpresence.md#forceprivacyscreennotification)

## InternetExplorer

- [AllowLegacyURLFields](policy-csp-internetexplorer.md#allowlegacyurlfields)

## LanguagePackManagement CSP

- [Providers](language-pack-management-csp.md#installedlanguageslanguage-idproviders)
- [LanguageFeatures](language-pack-management-csp.md#installedlanguageslanguage-idlanguagefeatures)
- [Status](language-pack-management-csp.md#installlanguage-idstatus)
- [ErrorCode](language-pack-management-csp.md#installlanguage-iderrorcode)
- [CopyToDeviceInternationalSettings](language-pack-management-csp.md#installlanguage-idcopytodeviceinternationalsettings)
- [EnableLanguageFeatureInstallations](language-pack-management-csp.md#installlanguage-idenablelanguagefeatureinstallations)
- [StartInstallation](language-pack-management-csp.md#installlanguage-idstartinstallation)
- [SystemPreferredUILanguages](language-pack-management-csp.md#languagesettingssystempreferreduilanguages)

## LocalPoliciesSecurityOptions

- [InteractiveLogon_NumberOfPreviousLogonsToCache](policy-csp-localpoliciessecurityoptions.md#interactivelogon_numberofpreviouslogonstocache)
- [UserAccountControl_BehaviorOfTheElevationPromptForAdministratorProtection](policy-csp-localpoliciessecurityoptions.md#useraccountcontrol_behavioroftheelevationpromptforadministratorprotection)
- [UserAccountControl_TypeOfAdminApprovalMode](policy-csp-localpoliciessecurityoptions.md#useraccountcontrol_typeofadminapprovalmode)

## MixedReality

- [AutoUnlock](policy-csp-mixedreality.md#autounlock)
- [ConfigureSharedAccount](policy-csp-mixedreality.md#configuresharedaccount)
- [ConfigureDeviceStandbyAction](policy-csp-mixedreality.md#configuredevicestandbyaction)
- [ConfigureDeviceStandbyActionTimeout](policy-csp-mixedreality.md#configuredevicestandbyactiontimeout)

## NewsAndInterests

- [DisableWidgetsOnLockScreen](policy-csp-newsandinterests.md#disablewidgetsonlockscreen)
- [DisableWidgetsBoard](policy-csp-newsandinterests.md#disablewidgetsboard)

## PassportForWork CSP

- [DisablePostLogonProvisioning](passportforwork-csp.md#devicetenantidpoliciesdisablepostlogonprovisioning)

## Printers

- [ConfigureIppTlsCertificatePolicy](policy-csp-printers.md#configureipptlscertificatepolicy)

## RemoteDesktopServices

- [TS_SERVER_REMOTEAPP_USE_SHELLAPPRUNTIME](policy-csp-remotedesktopservices.md#ts_server_remoteapp_use_shellappruntime)

## SettingsSync

- [EnableWindowsbackup](policy-csp-settingssync.md#enablewindowsbackup)

## Start

- [AlwaysShowNotificationIcon](policy-csp-start.md#alwaysshownotificationicon)
- [TurnOffAbbreviatedDateTimeFormat](policy-csp-start.md#turnoffabbreviateddatetimeformat)

## SurfaceHub CSP

- [ExchangeModernAuthEnabled](surfacehub-csp.md#deviceaccountexchangemodernauthenabled)

## TextInput

- [TouchKeyboardControllerModeAvailability](policy-csp-textinput.md#touchkeyboardcontrollermodeavailability)

## Update

- [AllowTemporaryEnterpriseFeatureControl](policy-csp-update.md#allowtemporaryenterprisefeaturecontrol)

## Wifi

- [AllowWFAQosManagementMSCS](policy-csp-wifi.md#allowwfaqosmanagementmscs)
- [AllowWFAQosManagementDSCPToUPMapping](policy-csp-wifi.md#allowwfaqosmanagementdscptoupmapping)

## WindowsAI

- [SetDenyAppListForRecall](policy-csp-windowsai.md#setdenyapplistforrecall)
- [SetDenyUriListForRecall](policy-csp-windowsai.md#setdenyurilistforrecall)
- [SetMaximumStorageSpaceForRecallSnapshots](policy-csp-windowsai.md#setmaximumstoragespaceforrecallsnapshots)
- [SetMaximumStorageDurationForRecallSnapshots](policy-csp-windowsai.md#setmaximumstoragedurationforrecallsnapshots)
- [DisableImageCreator](policy-csp-windowsai.md#disableimagecreator)
- [DisableCocreator](policy-csp-windowsai.md#disablecocreator)
- [DisableGenerativeFill](policy-csp-windowsai.md#disablegenerativefill)
- [AllowRecallEnablement](policy-csp-windowsai.md#allowrecallenablement)

## WindowsLicensing CSP

- [SubscriptionType](windowslicensing-csp.md#subscriptionssubscriptiontype)
- [SubscriptionStatus](windowslicensing-csp.md#subscriptionssubscriptionstatus)
- [SubscriptionLastError](windowslicensing-csp.md#subscriptionssubscriptionlasterror)
- [SubscriptionLastErrorDescription](windowslicensing-csp.md#subscriptionssubscriptionlasterrordescription)
- [DisableSubscription](windowslicensing-csp.md#subscriptionsdisablesubscription)
- [RemoveSubscription](windowslicensing-csp.md#subscriptionsremovesubscription)

## Related articles

[Policy configuration service provider](policy-configuration-service-provider.md)
