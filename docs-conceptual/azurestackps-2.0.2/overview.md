---
title: Omówienie programu PowerShell dla administratora usługi Azure Stack Hub | Microsoft Docs
description: Omówienie programu PowerShell dla administratora usługi Azure Stack Hub z instrukcjami dotyczącymi instalacji i konfiguracji.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 08/06/2020
ms.openlocfilehash: 754038a312a20e0dd87075bdeb51b13a1f1810a1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "88022970"
---
# <a name="azure-stack-hub-module-202"></a>Moduł usługi Azure Stack Hub w wersji 2.0.2

## <a name="requirements"></a>Wymagania:

Minimalna obsługiwana wersja usługi Azure Stack Hub to 2002.

Uwaga: Aby użyć starszych wersji usługi Azure Stack, zobacz [Instalowanie programu Azure Stack PowerShell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Instalowanie

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.2-preview -AllowPrerelease
```


## <a name="release-notes"></a>Informacje o wersji

* Obsługiwane z aktualizacją 2002.  

  Wersja 2.0.0 usługi Azure Stack Hub wprowadza zmiany powodujące niezgodność. Ten moduł korzysta z modułu Az, a nie modułu AzureRM. Przewodnik po migracji i listę zmian powodujących niezgodność można znaleźć w artykule [Migrowanie z modułu AzureRM do modułu Az w programie Azure PowerShell w usłudze Azure Stack Hub](https://aka.ms/AA7qsji).
