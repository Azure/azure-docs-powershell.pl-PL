---
title: Omówienie programu PowerShell dla administratora usługi Azure Stack | Microsoft Docs
description: Omówienie programu PowerShell dla administratora usługi Azure Stack z instrukcjami dotyczącymi instalacji i konfiguracji.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: 4e1174236796e7da929ff276addb32e42c18b707
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/12/2019
ms.locfileid: "54240139"
---
# <a name="azure-stack-module-160"></a>Moduł usługi Azure Stack w wersji 1.6.0

## <a name="requirements"></a>Wymagania:
Minimalna obsługiwana wersja usługi Azure Stack to 1811.

Uwaga: Jeśli używasz starszej wersji, zainstaluj wersję 1.6.0

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

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a>Informacje o wersji
* Obsługiwane z aktualizacją 1811
* Moduł Azs.Compute.Admin
    * Naprawiono brakujący prefiks Azs dla polecenia New-DataDiskObject i dodano alias z ostrzeżeniem o przyszłym wycofaniu.
* Moduł Azs.Update.Admin
    * Dodano ostrzeżenie z zaleceniem użycia polecenia Test-AzureStack przed poleceniem Install-AzsUpdate
* Azs.Fabric.Admin
    * Nowe polecenia cmdlet (te funkcje są obsługiwane przez usługę Azure Stack w wersji 1811 lub nowszej)
        * Get-AzsDrive
        * Get-AzsVolume
        * Get-AzsStorageSubSystem
    * Przestarzałe
        * Polecenie cmdlet Get-AzsInfrastructureVolume jest teraz aliasem polecenia cmdlet Get-AzsVolume
* Azs.InfrastructureInsights.Admin
    *  Dodano nowe polecenie cmdlet Repair-AzsAlert
* Azs.Storage.Admin
    * Poprawiono usterkę, w przypadku której nie są używane wartości domyślne przydziału
* Moduł Azs.Subscriptions.Admin
    * Naprawiono brakujący prefiks Azs dla polecenia New-AddonPlanDefinitionObject i dodano alias z ostrzeżeniem o przyszłym wycofaniu.
