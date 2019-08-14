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
ms.openlocfilehash: 1b3d707e862dd0c21e9e6b0a89f429ff21b1a99d
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861345"
---
# <a name="azure-stack-module-172"></a>Moduł usługi Azure Stack w wersji 1.7.2

## <a name="requirements"></a>Wymagania:

Minimalna obsługiwana wersja usługi Azure Stack to 1904.

Uwaga: Aby użyć starszych wersji usługi Azure Stack, zobacz [Instalowanie programu Azure Stack PowerShell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Instalowanie

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a>Informacje o wersji

* Obsługiwane z aktualizacją 1904
* To jest wersja zawierająca zmiany powodujące niezgodność. Aby uzyskać szczegółowe informacje na temat istotnych zmian, zobacz <https://aka.ms/azspshmigration170>
* Zmiana powodująca niezgodność: Kopia zapasowa zmienia się na tryb szyfrowania opartego na certyfikacie. Obsługa kluczy symetrycznych jest przestarzała.
* Aby uzyskać szczegółowe informacje na temat istotnych zmian, zobacz https://aka.ms/azspshmigration170
* Moduł Azs.Storage.Admin 
* Poprawka usterki — nowy limit przydziału magazynu używa wartości domyślnych, jeśli żadne wartości nie zostaną podane.
