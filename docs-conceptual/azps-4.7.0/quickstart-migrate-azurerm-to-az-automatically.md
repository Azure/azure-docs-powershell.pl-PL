---
title: Automatyczne migrowanie skryptów programu PowerShell z modułu AzureRM do Az programu PowerShell
description: Dowiedz się, jak można automatycznie migrować skrypty programu PowerShell z modułu AzureRM do Az programu PowerShell.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 09/11/2020
ms.openlocfilehash: d342ca65baf7664f430de3b7d294c0fc9815c0a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "92002339"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="b87bb-103">Szybki start: Automatyczne migrowanie skryptów programu PowerShell z modułu AzureRM do Az programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="b87bb-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="b87bb-104">W tym artykule dowiesz się, jak przeprowadzić automatyczne uaktualnienie skryptów programu PowerShell i modułów skryptów z modułu AzureRM do Az programu PowerShell za pomocą modułu Az.Tools.Migration programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b87bb-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b87bb-105">Moduł Az.Tools.Migration programu PowerShell jest obecnie w publicznej wersji zapoznawczej.</span><span class="sxs-lookup"><span data-stu-id="b87bb-105">The Az.Tools.Migration PowerShell module is currently in public preview.</span></span> <span data-ttu-id="b87bb-106">Ta wersja zapoznawcza jest dostępna bez umowy dotyczącej poziomu usług.</span><span class="sxs-lookup"><span data-stu-id="b87bb-106">This preview version is provided without a service level agreement.</span></span> <span data-ttu-id="b87bb-107">Nie jest ona zalecana w przypadku obciążeń produkcyjnych.</span><span class="sxs-lookup"><span data-stu-id="b87bb-107">It's not recommended for production workloads.</span></span> <span data-ttu-id="b87bb-108">Niektóre funkcje mogą być nieobsługiwane lub ograniczone.</span><span class="sxs-lookup"><span data-stu-id="b87bb-108">Certain features might not be supported or might have constrained capabilities.</span></span> <span data-ttu-id="b87bb-109">Aby uzyskać więcej informacji, zobacz [Uzupełniające warunki korzystania z wersji zapoznawczych platformy Microsoft Azure](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span><span class="sxs-lookup"><span data-stu-id="b87bb-109">For more information, see [Supplemental Terms of Use for Microsoft Azure Previews](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span></span>

<span data-ttu-id="b87bb-110">Opinie i problemy dotyczące modułu Az.Tools.Migration programu PowerShell można zgłaszać za pośrednictwem [problemu w usłudze GitHub](https://github.com/Azure/azure-powershell-migration/issues) w repozytorium `azure-powershell-migration`.</span><span class="sxs-lookup"><span data-stu-id="b87bb-110">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="requirements"></a><span data-ttu-id="b87bb-111">Wymagania</span><span class="sxs-lookup"><span data-stu-id="b87bb-111">Requirements</span></span>

* <span data-ttu-id="b87bb-112">Zaktualizuj istniejące skrypty programu PowerShell do najnowszej wersji [modułu AzureRM programu PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="b87bb-112">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="b87bb-113">Zainstaluj moduł Az.Tools.Migration programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b87bb-113">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="b87bb-114">Krok 1. Generowanie planu uaktualniania</span><span class="sxs-lookup"><span data-stu-id="b87bb-114">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="b87bb-115">Za pomocą polecenia cmdlet `New-AzUpgradeModulePlan` wygeneruj plan uaktualniania służący do migrowania skryptów i modułów do modułu Az programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b87bb-115">You use the `New-AzUpgradeModulePlan` cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="b87bb-116">Plan uaktualniania zawiera szczegóły dotyczące określonego pliku i punktów przesunięcia, które wymagają zmian podczas przechodzenia z modułu AzureRM do modułu Az programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b87bb-116">The upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

> [!NOTE]
> <span data-ttu-id="b87bb-117">Polecenie cmdlet `New-AzUpgradeModulePlan` nie wykonuje planu, tylko generuje kroki uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="b87bb-117">The `New-AzUpgradeModulePlan` cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

<span data-ttu-id="b87bb-118">Przejrzyj wyniki planu uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="b87bb-118">Review the results of the upgrade plan.</span></span>

```powershell
# Show the entire upgrade plan
$Plan
```

<span data-ttu-id="b87bb-119">Uruchom następujące polecenie, aby przefiltrować wyniki poleceń, które mają ostrzeżenia lub błędy.</span><span class="sxs-lookup"><span data-stu-id="b87bb-119">Run the following command to filter the results to commands that have warnings or errors.</span></span> <span data-ttu-id="b87bb-120">Może to być przydatne w przypadku dużych zestawów wyników, aby szybko identyfikować błędy przed przeprowadzeniem uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="b87bb-120">This may be helpful on large result sets to quickly identify errors before performing the upgrade.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="b87bb-121">Krok 2. Uaktualnianie</span><span class="sxs-lookup"><span data-stu-id="b87bb-121">Step 2: Perform the upgrade</span></span>

<span data-ttu-id="b87bb-122">Plan uaktualniania jest wykonywany po uruchomieniu polecenia cmdlet `Invoke-AzUpgradeModulePlan`.</span><span class="sxs-lookup"><span data-stu-id="b87bb-122">The upgrade plan is executed when you run the `Invoke-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="b87bb-123">To polecenie wykonuje uaktualnienie określonego pliku lub folderów z wyjątkiem błędów, które zostały zidentyfikowane przez polecenie cmdlet `New-AzUpgradeModulePlan`.</span><span class="sxs-lookup"><span data-stu-id="b87bb-123">This command performs an upgrade of the specified file or folders except for any errors that were identified by the `New-AzUpgradeModulePlan` cmdlet.</span></span>

<span data-ttu-id="b87bb-124">To polecenie wymaga określenia, czy pliki mają być modyfikowane na miejscu, czy też nowe pliki powinny zostać zachowane razem z oryginalnymi plikami (pozostawiając oryginalne pliki bez modyfikacji).</span><span class="sxs-lookup"><span data-stu-id="b87bb-124">This command requires you to specify if the files should be modified in place or if new files should be saved alongside your original files (leaving originals unmodified).</span></span>

> [!CAUTION]
> <span data-ttu-id="b87bb-125">Tej operacji nie można cofnąć.</span><span class="sxs-lookup"><span data-stu-id="b87bb-125">There is no undo operation.</span></span> <span data-ttu-id="b87bb-126">Zawsze upewnij się, że masz kopię zapasową skryptów i modułów programu PowerShell, które próbujesz uaktualnić.</span><span class="sxs-lookup"><span data-stu-id="b87bb-126">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

> [!WARNING]
> <span data-ttu-id="b87bb-127">Polecenie cmdlet `Invoke-AzUpgradeModulePlan` jest destrukcyjne, jeśli zostanie określona opcja `-FileEditMode ModifyExistingFiles`!</span><span class="sxs-lookup"><span data-stu-id="b87bb-127">The `Invoke-AzUpgradeModulePlan` cmdlet is destructive when the `-FileEditMode ModifyExistingFiles` option is specified!</span></span> <span data-ttu-id="b87bb-128">Modyfikuje ono skrypty i funkcje na miejscu zgodnie z planem uaktualniania modułu wygenerowanym przez polecenie cmdlet `New-AzUpgradeModulePlan`.</span><span class="sxs-lookup"><span data-stu-id="b87bb-128">It modifies your scripts and functions in place according to the module upgrade plan generated by the `New-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="b87bb-129">Zamiast tego polecenia należy skorzystać z niedestrukcyjnego polecenia cmdlet `-FileEditMode SaveChangesToNewFiles`.</span><span class="sxs-lookup"><span data-stu-id="b87bb-129">For the non-destructive option specify `-FileEditMode SaveChangesToNewFiles` instead.</span></span>

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

<span data-ttu-id="b87bb-130">Przejrzyj wyniki operacji uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="b87bb-130">Review the results of the upgrade operation.</span></span>

```powershell
# Show the results for the entire upgrade operation
$Results
```

<span data-ttu-id="b87bb-131">W przypadku zwrócenia błędów można bliżej przyjrzeć się wynikom dla błędów za pomocą następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="b87bb-131">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a><span data-ttu-id="b87bb-132">Ograniczenia</span><span class="sxs-lookup"><span data-stu-id="b87bb-132">Limitations</span></span>

* <span data-ttu-id="b87bb-133">Automatyczne aktualizacje nazw parametrów w zestawach parametrów nie są obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="b87bb-133">Automated parameter name updates to splatted parameter sets aren't supported.</span></span> <span data-ttu-id="b87bb-134">W przypadku znalezienia takiego zestawu podczas generowania planu uaktualniania zostanie zwrócone ostrzeżenie.</span><span class="sxs-lookup"><span data-stu-id="b87bb-134">If any are found during upgrade plan generation, a warning is returned.</span></span>
* <span data-ttu-id="b87bb-135">Operacje We/Wy na plikach używają domyślnego kodowania.</span><span class="sxs-lookup"><span data-stu-id="b87bb-135">File I/O operations use default encoding.</span></span> <span data-ttu-id="b87bb-136">Nietypowe kodowanie plików może powodować problemy.</span><span class="sxs-lookup"><span data-stu-id="b87bb-136">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="b87bb-137">Polecenia cmdlet modułu AzureRM przekazane jako argumenty do pozornych instrukcji testu jednostkowego usługi Pester nie są wykrywane.</span><span class="sxs-lookup"><span data-stu-id="b87bb-137">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="b87bb-138">Obecnie jako element docelowy jest obsługiwany tylko moduł Az programu PowerShell w wersji 4.6.1.</span><span class="sxs-lookup"><span data-stu-id="b87bb-138">Currently, only Az PowerShell module version 4.6.1 is supported as a target.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b87bb-139">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="b87bb-139">Next steps</span></span>

<span data-ttu-id="b87bb-140">Aby dowiedzieć się więcej o module Az programu PowerShell, zapoznaj się z [dokumentacją programu Azure PowerShell](https://docs.microsoft.com/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="b87bb-140">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](https://docs.microsoft.com/powershell/azure/)</span></span>