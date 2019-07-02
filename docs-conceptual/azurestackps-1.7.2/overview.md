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
ms.openlocfilehash: b77e09f6fcd5b7752af9f51a42d357db4f1b13db
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/12/2019
ms.locfileid: "67037673"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="ae5cd-103">Moduł usługi Azure Stack w wersji 1.7.2</span><span class="sxs-lookup"><span data-stu-id="ae5cd-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="ae5cd-104">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="ae5cd-104">Requirements:</span></span>

<span data-ttu-id="ae5cd-105">Minimalna obsługiwana wersja usługi Azure Stack to 1904.</span><span class="sxs-lookup"><span data-stu-id="ae5cd-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="ae5cd-106">Uwaga: Aby użyć starszych wersji usługi Azure Stack, zobacz [Instalowanie programu Azure Stack PowerShell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="ae5cd-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="ae5cd-107">Instalowanie</span><span class="sxs-lookup"><span data-stu-id="ae5cd-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a><span data-ttu-id="ae5cd-108">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="ae5cd-108">Release Notes</span></span>

* <span data-ttu-id="ae5cd-109">Obsługiwane z aktualizacją 1904</span><span class="sxs-lookup"><span data-stu-id="ae5cd-109">Supported with 1904 update</span></span>
* <span data-ttu-id="ae5cd-110">To jest wersja zawierająca zmiany powodujące niezgodność.</span><span class="sxs-lookup"><span data-stu-id="ae5cd-110">This a breaking change release.</span></span> <span data-ttu-id="ae5cd-111">Aby uzyskać szczegółowe informacje na temat istotnych zmian, zobacz <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="ae5cd-111">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="ae5cd-112">Zmiana powodująca niezgodność: Kopia zapasowa zmienia się na tryb szyfrowania opartego na certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="ae5cd-112">Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="ae5cd-113">Obsługa kluczy symetrycznych jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="ae5cd-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="ae5cd-114">Aby uzyskać szczegółowe informacje na temat istotnych zmian, zobacz https://aka.ms/azspshmigration170</span><span class="sxs-lookup"><span data-stu-id="ae5cd-114">For details on the breaking changes, refer to https://aka.ms/azspshmigration170</span></span>
* <span data-ttu-id="ae5cd-115">Moduł Azs.Storage.Admin</span><span class="sxs-lookup"><span data-stu-id="ae5cd-115">Azs.Storage.Admin Module</span></span> 
* <span data-ttu-id="ae5cd-116">Poprawka usterki — nowy limit przydziału magazynu używa wartości domyślnych, jeśli żadne wartości nie zostaną podane.</span><span class="sxs-lookup"><span data-stu-id="ae5cd-116">Bug fix - New Storage Quota uses defaults if none provided.</span></span>
