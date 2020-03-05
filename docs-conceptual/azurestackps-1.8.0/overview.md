---
title: Omówienie programu PowerShell dla administratora usługi Azure Stack | Microsoft Docs
description: Omówienie programu PowerShell dla administratora usługi Azure Stack z instrukcjami dotyczącymi instalacji i konfiguracji.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/24/2020
ms.openlocfilehash: ec406c80de6b457f7e340a23fe8caf2ab83be46a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "78264414"
---
# <a name="azure-stack-module-180"></a>Moduł usługi Azure Stack w wersji 1.8.0

## <a name="requirements"></a>Wymagania:

Minimalna obsługiwana wersja usługi Azure Stack to 1910.

Uwaga: Aby użyć starszych wersji usługi Azure Stack, zobacz [Instalowanie programu Azure Stack PowerShell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Instalowanie

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a>Informacje o wersji

* Obsługiwane z aktualizacją 1910
* Zmiany obejmują:

    - **Nowy moduł administracyjny dostawcy DRP**: Dostawca Deployment Resource Provider (DRP) umożliwia zorganizowane wdrożenia dostawców zasobów w usłudze Azure Stack Hub. Te polecenia współpracują z warstwą Azure Resource Manager w celu interakcji z dostawcą DRP.

    - **BRP**:
        - Obsługa przywracania pojedynczej roli na potrzeby tworzenia kopii zapasowej infrastruktury stosu platformy Azure.
        - Dodanie parametru `RoleName` do polecenia cmdlet języka R `estore-AzsBackup`.

    - **FRP**: Zmiany powodujące niezgodność dla zasobów **Dysk** i **Wolumin** z interfejsem API w wersji 2019-05-01. Te funkcje są obsługiwane przez usługę Azure Stack Hub w wersji 1910 lub nowszej:
        - Zmieniono wartość identyfikatora oraz parametrów `Name`, `HealthStatus` i `OperationalStatus`.
        - Obsługiwane są nowe właściwości `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer`i `StoragePool` dla zasobów **Dysk**.
        - Właściwości `CanPool` i `CannotPoolReason` zasobów **Dysk** są przestarzałe. Używaj zamiast nich właściwości `OperationalStatus`.
