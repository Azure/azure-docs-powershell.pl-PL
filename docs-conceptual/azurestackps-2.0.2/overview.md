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
ms.openlocfilehash: ec4591e4f44fa56b7482d2dec3f525cb02dbd94b
ms.sourcegitcommit: a24069b411d3a6011067770430b6dcdd4b2c2159
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/16/2020
ms.locfileid: "97532263"
---
# <a name="azure-stack-hub-module-202"></a><span data-ttu-id="5f26d-103">Moduł usługi Azure Stack Hub w wersji 2.0.2</span><span class="sxs-lookup"><span data-stu-id="5f26d-103">Azure Stack Hub Module 2.0.2</span></span>

## <a name="requirements"></a><span data-ttu-id="5f26d-104">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="5f26d-104">Requirements:</span></span>

<span data-ttu-id="5f26d-105">Minimalna obsługiwana wersja usługi Azure Stack Hub to 2002.</span><span class="sxs-lookup"><span data-stu-id="5f26d-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="5f26d-106">Uwaga: Aby użyć starszych wersji usługi Azure Stack, zobacz [Instalowanie programu Azure Stack PowerShell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="5f26d-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="5f26d-107">Instalowanie</span><span class="sxs-lookup"><span data-stu-id="5f26d-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease -SkipPublisherCheck

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.2-preview -AllowPrerelease
```


## <a name="release-notes"></a><span data-ttu-id="5f26d-108">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="5f26d-108">Release Notes</span></span>

* <span data-ttu-id="5f26d-109">Obsługiwane z aktualizacją 2002.</span><span class="sxs-lookup"><span data-stu-id="5f26d-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="5f26d-110">Wersja 2.0.0 usługi Azure Stack Hub wprowadza zmiany powodujące niezgodność.</span><span class="sxs-lookup"><span data-stu-id="5f26d-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="5f26d-111">Ten moduł korzysta z modułu Az, a nie modułu AzureRM.</span><span class="sxs-lookup"><span data-stu-id="5f26d-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="5f26d-112">Przewodnik po migracji i listę zmian powodujących niezgodność można znaleźć w artykule [Migrowanie z modułu AzureRM do modułu Az w programie Azure PowerShell w usłudze Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="5f26d-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span></span>
