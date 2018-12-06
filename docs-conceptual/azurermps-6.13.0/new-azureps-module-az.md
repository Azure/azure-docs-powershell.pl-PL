---
title: Wprowadzenie do modułu Az programu Azure PowerShell
description: Przedstawiamy nowy moduł programu Azure PowerShell — Az — który zastąpi moduł AzureRM.
ms.date: 11/07/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b0f31341d4344bdac5b4d657a1f66acfd9984dda
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828114"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="4668b-103">Wprowadzenie do nowego modułu Az programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4668b-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="4668b-104">Począwszy od listopada 2018 r. moduł `Az` programu Azure PowerShell jest dostępny w publicznej wersji zapoznawczej.</span><span class="sxs-lookup"><span data-stu-id="4668b-104">Starting in November 2018, the Azure PowerShell `Az` module is available for full public preview.</span></span>
<span data-ttu-id="4668b-105">Moduł Az oferuje krótsze polecenia, lepszą stabilność i obsługuje systemy Windows, macOS i Linux.</span><span class="sxs-lookup"><span data-stu-id="4668b-105">Az offers shorter commands, improved stability, and supports Windows, macOS, and Linux.</span></span> <span data-ttu-id="4668b-106">Moduł Az zapewnia również równoważność funkcji i łatwą ścieżkę migracji z modułu AzureRM.</span><span class="sxs-lookup"><span data-stu-id="4668b-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="4668b-107">Moduł Az korzysta z biblioteki .NET Standard, co oznacza, że działa w programie PowerShell w wersjach 5.x i 6.x.</span><span class="sxs-lookup"><span data-stu-id="4668b-107">Az uses the .NET Standard library, which means it runs on PowerShell 5.x and PowerShell 6.x.</span></span>
<span data-ttu-id="4668b-108">Ponieważ program PowerShell w wersji 6.x działa w systemach Linux, macOS i Windows, oznacza to, że moduł Az jest dostępny dla wszystkich platform.</span><span class="sxs-lookup"><span data-stu-id="4668b-108">Since PowerShell 6.x can run on Linux, macOS, and Windows, that means Az is available for all platforms.</span></span>
<span data-ttu-id="4668b-109">Użycie biblioteki .NET Standard pozwala nam na ujednolicenie bazy kodu programu Azure PowerShell przy minimalnym wpływie na użytkowników.</span><span class="sxs-lookup"><span data-stu-id="4668b-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="4668b-110">Az to nowy moduł, dlatego wersja została zresetowana.</span><span class="sxs-lookup"><span data-stu-id="4668b-110">Az is a new module, so the version has been reset.</span></span> <span data-ttu-id="4668b-111">Pierwszą stabilną wersją będzie wersja 1.0, jednak od listopada 2018 r. moduł ten oferuje równoważność funkcji z modułem AzureRm.</span><span class="sxs-lookup"><span data-stu-id="4668b-111">The first stable release will be 1.0, but the module has feature parity with AzureRm as of November 2018.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="4668b-112">Uaktualnianie do modułu Az</span><span class="sxs-lookup"><span data-stu-id="4668b-112">Upgrade to Az</span></span>

<span data-ttu-id="4668b-113">Zaleca się, aby użytkownicy przeprowadzili uaktualnienie do nowego modułu `Az`.</span><span class="sxs-lookup"><span data-stu-id="4668b-113">It's recommended that users upgrade to the new `Az` module.</span></span> <span data-ttu-id="4668b-114">W tym celu:</span><span class="sxs-lookup"><span data-stu-id="4668b-114">To do so:</span></span>

* [<span data-ttu-id="4668b-115">Odinstaluj moduł AzureRM programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4668b-115">Uninstall the Azure PowerShell AzureRM module</span></span>](/powershell/azure/uninstall-azurerm-ps)
* [<span data-ttu-id="4668b-116">Zainstaluj moduł Az programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4668b-116">Install the Azure PowerShell Az module</span></span>](/powershell/azure/install-az-ps)
* <span data-ttu-id="4668b-117">Po zapoznaniu się z nowym zestawem poleceń włącz tryb zgodności dla modułu AzureRM za pomocą polecenia `Enable-AzureRMAlias`.</span><span class="sxs-lookup"><span data-stu-id="4668b-117">Enable compatibility mode for AzureRM with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="4668b-118">Migrowanie istniejących skryptów do modułu Az</span><span class="sxs-lookup"><span data-stu-id="4668b-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="4668b-119">Duże aktualizacje mogą być kłopotliwe.</span><span class="sxs-lookup"><span data-stu-id="4668b-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="4668b-120">Jednak moduł `Az` oferuje tryb zgodności, który ułatwia korzystanie z istniejących skryptów podczas pracy nad aktualizacjami do nowej składni.</span><span class="sxs-lookup"><span data-stu-id="4668b-120">However, the `Az` module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="4668b-121">Aby włączyć tryb zgodności z modułem `AzureRM`, użyj polecenia cmdlet `Enable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="4668b-121">Use the `Enable-AzureRmAlias` cmdlet to enable the `AzureRM` compatibility mode.</span></span> <span data-ttu-id="4668b-122">To polecenie cmdlet definiuje nazwy poleceń cmdlet modułu `AzureRM` jako aliasy dla nazw poleceń cmdlet nowego modułu `Az`.</span><span class="sxs-lookup"><span data-stu-id="4668b-122">This cmdlet defines `AzureRM` cmdlet names as aliases for the new `Az` cmdlet names.</span></span>

<span data-ttu-id="4668b-123">Nowe nazwy poleceń cmdlet zaprojektowano tak, aby były łatwe do zapamiętania.</span><span class="sxs-lookup"><span data-stu-id="4668b-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="4668b-124">Zamiast używać ciągu `AzureRm` lub `Azure` w nazwach poleceń cmdlet, wystarczy użyć ciągu `Az`.</span><span class="sxs-lookup"><span data-stu-id="4668b-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="4668b-125">Na przykład stare polecenie `New-AzureRmVm` to teraz polecenie `New-AzVm`.</span><span class="sxs-lookup"><span data-stu-id="4668b-125">For example, the old command `New-AzureRmVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="4668b-126">Aby zapoznać się z pełnym opisem procesu migracji, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="4668b-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="4668b-127">Przyszła obsługa techniczna modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="4668b-127">The future of support for AzureRM</span></span>

<span data-ttu-id="4668b-128">Po wydaniu wersji 1.0 modułu `Az` w grudniu 2018 r. w istniejącym module `AzureRM` nie będą już wprowadzane nowe polecenia cmdlet ani funkcje.</span><span class="sxs-lookup"><span data-stu-id="4668b-128">The existing `AzureRM` module will no longer receive new cmdlets or features when `Az` version 1.0 is released in December 2018.</span></span> <span data-ttu-id="4668b-129">Jednak moduł `AzureRM` jest nadal oficjalnie obsługiwany i będą do niego wydawane poprawki błędów.</span><span class="sxs-lookup"><span data-stu-id="4668b-129">However, `AzureRM` is still officially maintained and will get bug fixes.</span></span> <span data-ttu-id="4668b-130">Aby być na bieżąco z najnowszymi usługami i funkcjami platformy Azure, należy przejść na korzystanie z modułu `Az`.</span><span class="sxs-lookup"><span data-stu-id="4668b-130">To keep up with the latest Azure services and features, you should switch to the `Az` module.</span></span>