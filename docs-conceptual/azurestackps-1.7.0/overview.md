---
title: Omówienie programu PowerShell dla administratora usługi Azure Stack | Microsoft Docs
description: Omówienie programu PowerShell dla administratora usługi Azure Stack z instrukcjami dotyczącymi instalacji i konfiguracji.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: af34497f243ce8f4f718e88312f6ad54eb6ad848
ms.sourcegitcommit: 993db64e68b222acbcfdeef2e81eb3316b160858
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2019
ms.locfileid: "56240535"
---
# <a name="azure-stack-module-170"></a>Moduł usługi Azure Stack w wersji 1.7.0

## <a name="requirements"></a>Wymagania:
Minimalna obsługiwana wersja usługi Azure Stack to 1901.

Uwaga: Jeśli używasz starszej wersji, zainstaluj wersję 1.7.0

## <a name="install"></a>Instalowanie
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.0
```
## <a name="release-notes"></a>Informacje o wersji
* Obsługiwane z aktualizacją 1901
* To jest wersja zawierająca zmiany powodujące niezgodność. Aby uzyskać szczegółowe informacje na temat istotnych zmian, zobacz https://aka.ms/azspshmigration170
* Moduł Azs.Backup.Admin * Zmiana powodująca niezgodność: Kopia zapasowa zmienia się na tryb szyfrowania opartego na certyfikacie. Obsługa kluczy symetrycznych jest przestarzała.
* Moduł Azs.Fabric.Admin       * Wycofanie           * Polecenie Get-AzsInfrastructureVolume jest przestarzałe, udostępniamy nowe polecenie cmdlet Get-AzsVolume * Polecenie Get AzsStorageSystem jest przestarzałe, udostępniamy nowe polecenie cmdlet Get-AzsStorageSubSystem           * Polecenie Get AzsStoragePool jest przestarzałe, obiekt StorageSubSystem ma właściwość pojemności
* Moduł Azs.Compute.Admin           * Poprawka usterki: Add-AzsPlatformImage, Get-AzsPlatformImage: Wywoływanie polecenia ConvertTo-PlatformImageObject tylko w ścieżce powodzenia           * Poprawka usterki: Add-AzsVmExtension, Get-AzsVmExtension: Wywoływanie polecenia ConvertTo-VmExtensionObject tylko w ścieżce powodzenia
* Moduł Azs.Storage.Admin           * Poprawka usterki — nowy limit przydziału magazynu używa wartości domyślnych, jeśli żadne wartości nie zostaną podane.'

