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
ms.openlocfilehash: af0343e5ad92fa7f2b5c10e3e67cb7e10feb81c6
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/17/2019
ms.locfileid: "65855792"
---
# <a name="azure-stack-module-172"></a>Moduł usługi Azure Stack w wersji 1.7.2

## <a name="requirements"></a>Wymagania:

Minimalna obsługiwana wersja usługi Azure Stack to 1904.

Uwaga: Aby użyć starszych wersji usługi Azure Stack, zobacz [Instalowanie programu Azure Stack PowerShell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install-powershell-for-azure-stack"></a>Instalowanie programu PowerShell dla usługi Azure Stack

Instalacja składa się z trzech kroków:

1. Instalowanie programu Azure Stack PowerShell w zależności od wersji usługi Azure Stack
2. Włączanie dodatkowych funkcji magazynu
3. Potwierdzanie instalacji programu PowerShell

### <a name="install-azure-stack-powershell"></a>Instalowanie programu Azure Stack PowerShell

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install the AzureRM.BootStrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRM.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Get-AzureRmProfile -Update
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

### <a name="enable-additional-storage-features"></a>Włączanie dodatkowych funkcji magazynu

```
# Install the Azure.Storage module version 4.5.0
Install-Module -Name Azure.Storage -RequiredVersion 4.5.0 -Force -AllowClobber

# Install the AzureRm.Storage module version 5.0.4
Install-Module -Name AzureRM.Storage -RequiredVersion 5.0.4 -Force -AllowClobber

# Remove incompatible storage module installed by AzureRM.Storage
Uninstall-Module Azure.Storage -RequiredVersion 4.6.1 -Force

# Load the modules explicitly specifying the versions
Import-Module -Name Azure.Storage -RequiredVersion 4.5.0
Import-Module -Name AzureRM.Storage -RequiredVersion 5.0.4
```

## <a name="release-notes"></a>Informacje o wersji

* Obsługiwane z aktualizacją 1904
* To jest wersja zawierająca zmiany powodujące niezgodność. Aby uzyskać szczegółowe informacje na temat istotnych zmian, zobacz <https://aka.ms/azspshmigration170>
* Moduł Azs.Backup.Admin * Zmiana powodująca niezgodność: Kopia zapasowa zmienia się na tryb szyfrowania opartego na certyfikacie. Obsługa kluczy symetrycznych jest przestarzała.
* Moduł Azs.Fabric.Admin       * Wycofanie           * Polecenie Get-AzsInfrastructureVolume jest przestarzałe, udostępniamy nowe polecenie cmdlet Get-AzsVolume * Polecenie Get AzsStorageSystem jest przestarzałe, udostępniamy nowe polecenie cmdlet Get-AzsStorageSubSystem           * Polecenie Get AzsStoragePool jest przestarzałe, obiekt StorageSubSystem ma właściwość pojemności
* Moduł Azs.Compute.Admin           * Poprawka usterki: Add-AzsPlatformImage, Get-AzsPlatformImage: Wywoływanie polecenia ConvertTo-PlatformImageObject tylko w ścieżce powodzenia           * Poprawka usterki: Add-AzsVmExtension, Get-AzsVmExtension: Wywoływanie polecenia ConvertTo-VmExtensionObject tylko w ścieżce powodzenia
* Moduł Azs.Storage.Admin           * Poprawka usterki — nowy limit przydziału magazynu używa wartości domyślnych, jeśli żadne wartości nie zostaną podane.'
