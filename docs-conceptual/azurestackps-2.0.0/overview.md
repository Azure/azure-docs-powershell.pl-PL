---
title: Omówienie programu PowerShell dla administratora usługi Azure Stack Hub | Microsoft Docs
description: Omówienie programu PowerShell dla administratora usługi Azure Stack Hub z instrukcjami dotyczącymi instalacji i konfiguracji.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 04/16/2020
ms.openlocfilehash: 166c5339c95507b8a9ef1a32d46f589b8d792794
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427959"
---
# <a name="azure-stack-hub-module-200"></a><span data-ttu-id="31cde-103">Moduł usługi Azure Stack Hub w wersji 2.0.0</span><span class="sxs-lookup"><span data-stu-id="31cde-103">Azure Stack Hub Module 2.0.0</span></span>

## <a name="requirements"></a><span data-ttu-id="31cde-104">Wymagania:</span><span class="sxs-lookup"><span data-stu-id="31cde-104">Requirements:</span></span>

<span data-ttu-id="31cde-105">Minimalna obsługiwana wersja usługi Azure Stack Hub to 2002.</span><span class="sxs-lookup"><span data-stu-id="31cde-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="31cde-106">Uwaga: Aby użyć starszych wersji usługi Azure Stack, zobacz [Instalowanie programu Azure Stack PowerShell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="31cde-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="31cde-107">Instalowanie</span><span class="sxs-lookup"><span data-stu-id="31cde-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.0-preview -AllowPrerelease
```


## <a name="release-notes"></a><span data-ttu-id="31cde-108">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="31cde-108">Release Notes</span></span>

* <span data-ttu-id="31cde-109">Obsługiwane z aktualizacją 2002.</span><span class="sxs-lookup"><span data-stu-id="31cde-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="31cde-110">Wersja 2.0.0 usługi Azure Stack Hub wprowadza zmiany powodujące niezgodność.</span><span class="sxs-lookup"><span data-stu-id="31cde-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="31cde-111">Ten moduł korzysta z modułu Az, a nie modułu AzureRM.</span><span class="sxs-lookup"><span data-stu-id="31cde-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="31cde-112">Przewodnik po migracji i listę zmian powodujących niezgodność można znaleźć w artykule [Migrowanie z modułu AzureRM do modułu Az w programie Azure PowerShell w usłudze Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="31cde-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span></span>