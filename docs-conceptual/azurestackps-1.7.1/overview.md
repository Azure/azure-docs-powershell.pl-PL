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
ms.openlocfilehash: 6568dc4e6c51e8f250aad2c4dd765c065fe6a8bf
ms.sourcegitcommit: d3069aba7d1ac248aff755e4b21533af1f73251d
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/02/2019
ms.locfileid: "58808064"
---
# <a name="azure-stack-module-171"></a>Moduł usługi Azure Stack w wersji 1.7.1

## <a name="requirements"></a>Wymagania:

Minimalna obsługiwana wersja usługi Azure Stack to 1901.

Uwaga: Aby użyć starszych wersji usługi Azure Stack, zobacz [Instalowanie programu Azure Stack PowerShell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Instalowanie

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.1
```

## <a name="release-notes"></a>Informacje o wersji

* Obsługiwane z aktualizacją 1901
* To jest wersja zawierająca zmiany powodujące niezgodność. Aby uzyskać szczegółowe informacje na temat istotnych zmian, zobacz <https://aka.ms/azspshmigration170>
* Moduł Azs.Backup.Admin * Zmiana powodująca niezgodność: Kopia zapasowa zmienia się na tryb szyfrowania opartego na certyfikacie. Obsługa kluczy symetrycznych jest przestarzała.
* Moduł Azs.Fabric.Admin       * Wycofanie           * Polecenie Get-AzsInfrastructureVolume jest przestarzałe, udostępniamy nowe polecenie cmdlet Get-AzsVolume * Polecenie Get AzsStorageSystem jest przestarzałe, udostępniamy nowe polecenie cmdlet Get-AzsStorageSubSystem           * Polecenie Get AzsStoragePool jest przestarzałe, obiekt StorageSubSystem ma właściwość pojemności
* Moduł Azs.Compute.Admin           * Poprawka usterki: Add-AzsPlatformImage, Get-AzsPlatformImage: Wywoływanie polecenia ConvertTo-PlatformImageObject tylko w ścieżce powodzenia           * Poprawka usterki: Add-AzsVmExtension, Get-AzsVmExtension: Wywoływanie polecenia ConvertTo-VmExtensionObject tylko w ścieżce powodzenia
* Moduł Azs.Storage.Admin           * Poprawka usterki — nowy limit przydziału magazynu używa wartości domyślnych, jeśli żadne wartości nie zostaną podane.'
