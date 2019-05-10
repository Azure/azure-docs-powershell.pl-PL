---
title: Wprowadzenie do modułu Az programu Azure PowerShell
description: Przedstawiamy nowy moduł programu Azure PowerShell — Az — który zastąpi moduł AzureRM.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 10665a72bc7dcae8ecf36b5ef4e2ab285a0e78b7
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048703"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="2784d-103">Wprowadzenie do nowego modułu Az programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2784d-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="2784d-104">Począwszy od grudnia 2018 r., moduł Az programu Azure PowerShell jest ogólnie dostępny i interakcja z platformą Azure powinna się teraz odbywać za pomocą tego modułu programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2784d-104">Starting in December 2018, the Azure PowerShell Az module is in general release and now the intended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="2784d-105">Moduł Az oferuje krótsze polecenia, lepszą stabilność i obsługę wielu platform.</span><span class="sxs-lookup"><span data-stu-id="2784d-105">Az offers shorter commands, improved stability, and cross-platform support.</span></span> <span data-ttu-id="2784d-106">Moduł Az zapewnia również równoważność funkcji i łatwą ścieżkę migracji z modułu AzureRM.</span><span class="sxs-lookup"><span data-stu-id="2784d-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="2784d-107">Moduł Az korzysta z biblioteki .NET Standard, co oznacza, że działa w programie PowerShell 5 i PowerShell 6.</span><span class="sxs-lookup"><span data-stu-id="2784d-107">Az uses the .NET Standard library, which means it runs on PowerShell 5 and PowerShell 6.</span></span>
<span data-ttu-id="2784d-108">Ponieważ program PowerShell w wersji 6 działa w systemach Linux, macOS i Windows, program Azure PowerShell jest teraz dostępny dla wszystkich platform.</span><span class="sxs-lookup"><span data-stu-id="2784d-108">Since PowerShell 6 can run on Linux, macOS, and Windows, Azure PowerShell is now available for all platforms.</span></span>
<span data-ttu-id="2784d-109">Użycie biblioteki .NET Standard pozwala nam na ujednolicenie bazy kodu programu Azure PowerShell przy minimalnym wpływie na użytkowników.</span><span class="sxs-lookup"><span data-stu-id="2784d-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="2784d-110">Az to nowy moduł, dlatego wersja została zresetowana do 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="2784d-110">Az is a new module, so the version has been reset to 1.0.0.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="2784d-111">Uaktualnianie do modułu Az</span><span class="sxs-lookup"><span data-stu-id="2784d-111">Upgrade to Az</span></span>

<span data-ttu-id="2784d-112">Zaleca się, aby wszyscy użytkownicy przeprowadzili uaktualnienie do nowego modułu Az.</span><span class="sxs-lookup"><span data-stu-id="2784d-112">It's recommended that all users upgrade to the new Az module.</span></span> <span data-ttu-id="2784d-113">W tym celu:</span><span class="sxs-lookup"><span data-stu-id="2784d-113">To do so:</span></span>

* <span data-ttu-id="2784d-114">__ZALECANE__: [Odinstaluj moduł AzureRM programu Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)</span><span class="sxs-lookup"><span data-stu-id="2784d-114">__RECOMMENDED__: [Uninstall the Azure PowerShell AzureRM module](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)</span></span>
* [<span data-ttu-id="2784d-115">Zainstaluj moduł Az programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2784d-115">Install the Azure PowerShell Az module</span></span>](/powershell/azure/install-az-ps)
* <span data-ttu-id="2784d-116">Za pomocą polecenia `Enable-AzureRMAlias` włącz tryb zgodności, aby dodać aliasy dla poleceń cmdlet modułu AzureRM na czas zapoznawania się z nowym zestawem poleceń.</span><span class="sxs-lookup"><span data-stu-id="2784d-116">Enable compatibility mode to add aliases for AzureRM cmdlets with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span> <span data-ttu-id="2784d-117">Włącz aliasy __tylko wtedy__, gdy nie masz zainstalowanego modułu AzureRM.</span><span class="sxs-lookup"><span data-stu-id="2784d-117">__Only__ enable aliases if you do not have AzureRM installed.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="2784d-118">Migrowanie istniejących skryptów do modułu Az</span><span class="sxs-lookup"><span data-stu-id="2784d-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="2784d-119">Duże aktualizacje mogą być kłopotliwe.</span><span class="sxs-lookup"><span data-stu-id="2784d-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="2784d-120">Jednak moduł Az oferuje tryb zgodności, który ułatwia korzystanie z istniejących skryptów podczas pracy nad aktualizacjami do nowej składni.</span><span class="sxs-lookup"><span data-stu-id="2784d-120">However, the Az module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="2784d-121">Aby włączyć tryb zgodności z modułem AzureRM, użyj polecenia cmdlet `Enable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="2784d-121">Use the `Enable-AzureRmAlias` cmdlet to enable the AzureRM compatibility mode.</span></span> <span data-ttu-id="2784d-122">To polecenie cmdlet definiuje nazwy poleceń cmdlet modułu AzureRM jako aliasy dla nazw poleceń cmdlet nowego modułu Az.</span><span class="sxs-lookup"><span data-stu-id="2784d-122">This cmdlet defines AzureRM cmdlet names as aliases for the new Az cmdlet names.</span></span>

<span data-ttu-id="2784d-123">Nowe nazwy poleceń cmdlet zaprojektowano tak, aby były łatwe do zapamiętania.</span><span class="sxs-lookup"><span data-stu-id="2784d-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="2784d-124">Zamiast używać ciągu `AzureRm` lub `Azure` w nazwach poleceń cmdlet, wystarczy użyć ciągu `Az`.</span><span class="sxs-lookup"><span data-stu-id="2784d-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="2784d-125">Na przykład stare polecenie `New-AzureRMVm` to teraz polecenie `New-AzVm`.</span><span class="sxs-lookup"><span data-stu-id="2784d-125">For example, the old command `New-AzureRMVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="2784d-126">Aby zapoznać się z pełnym opisem procesu migracji, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="2784d-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="2784d-127">Przyszła obsługa techniczna modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="2784d-127">The future of support for AzureRM</span></span>

<span data-ttu-id="2784d-128">W istniejącym module AzureRM nie będą już wprowadzane nowe polecenia cmdlet ani funkcje.</span><span class="sxs-lookup"><span data-stu-id="2784d-128">The existing AzureRM module will no longer receive new cmdlets or features.</span></span> <span data-ttu-id="2784d-129">Jednak moduł AzureRM jest nadal oficjalnie obsługiwany i będą dla niego wydawane poprawki błędów do grudnia 2020 r.</span><span class="sxs-lookup"><span data-stu-id="2784d-129">However, AzureRM is still officially maintained and will get bug fixes up through December 2020.</span></span> <span data-ttu-id="2784d-130">Aby być na bieżąco z najnowszymi usługami i funkcjami platformy Azure, zmień używany moduł na Az.</span><span class="sxs-lookup"><span data-stu-id="2784d-130">To keep up with the latest Azure services and features, switch to the Az module.</span></span>
