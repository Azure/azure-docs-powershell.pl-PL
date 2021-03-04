---
title: Automatyczne migrowanie skryptów programu PowerShell z modułu AzureRM do Az programu PowerShell
description: Dowiedz się, jak można automatycznie migrować skrypty programu PowerShell z modułu AzureRM do Az programu PowerShell.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 12/18/2020
ms.openlocfilehash: 57218c130f172bc359334b83db16e5790fa5562c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101881895"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="8eb88-103">Szybki start: Automatyczne migrowanie skryptów programu PowerShell z modułu AzureRM do Az programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="8eb88-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="8eb88-104">W tym artykule dowiesz się, jak przeprowadzić automatyczne uaktualnienie skryptów programu PowerShell i modułów skryptów z modułu AzureRM do Az programu PowerShell za pomocą modułu Az.Tools.Migration programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8eb88-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span> <span data-ttu-id="8eb88-105">Aby uzyskać dodatkowe opcje migracji, zobacz [Migrowanie programu Azure PowerShell z modułu AzureRM do modułu Az](/powershell/azure/migrate-from-azurerm-to-az).</span><span class="sxs-lookup"><span data-stu-id="8eb88-105">For additional migration options, see [Migrate Azure PowerShell from AzureRM to Az](/powershell/azure/migrate-from-azurerm-to-az).</span></span>

## <a name="requirements"></a><span data-ttu-id="8eb88-106">Wymagania</span><span class="sxs-lookup"><span data-stu-id="8eb88-106">Requirements</span></span>

* <span data-ttu-id="8eb88-107">Zaktualizuj istniejące skrypty programu PowerShell do najnowszej wersji [modułu AzureRM programu PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="8eb88-107">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="8eb88-108">Zainstaluj moduł Az.Tools.Migration programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8eb88-108">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="8eb88-109">Krok 1. Generowanie planu uaktualniania</span><span class="sxs-lookup"><span data-stu-id="8eb88-109">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="8eb88-110">Za pomocą polecenia cmdlet **`New-AzUpgradeModulePlan`** wygeneruj plan uaktualniania służący do migrowania skryptów i modułów do modułu Az programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8eb88-110">You use the **`New-AzUpgradeModulePlan`** cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="8eb88-111">To polecenie cmdlet nie wprowadza żadnych zmian w istniejących skryptach.</span><span class="sxs-lookup"><span data-stu-id="8eb88-111">This cmdlet doesn’t make any changes to your existing scripts.</span></span> <span data-ttu-id="8eb88-112">Użyj parametru **`FilePath`** , aby wskazać określony skrypt jako docelowy, lub użyj parametru **`DirectoryPath`** , aby wskazać wszystkie skrypty w określonym folderze jako docelowe.</span><span class="sxs-lookup"><span data-stu-id="8eb88-112">Use the **`FilePath`** parameter for targeting a specific script or the **`DirectoryPath`** parameter for targeting all scripts in a specific folder.</span></span>

> [!NOTE]
> <span data-ttu-id="8eb88-113">Polecenie cmdlet **`New-AzUpgradeModulePlan`** nie wykonuje planu, tylko generuje kroki uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="8eb88-113">The **`New-AzUpgradeModulePlan`** cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

<span data-ttu-id="8eb88-114">Poniższy przykład generuje plan dla wszystkich skryptów w folderze _`C:\Scripts`_ .</span><span class="sxs-lookup"><span data-stu-id="8eb88-114">The following example generates a plan for all the scripts in the _`C:\Scripts`_ folder.</span></span> <span data-ttu-id="8eb88-115">Został określony parametr **`OutVariable`** , aby wyniki zostały zwrócone i jednocześnie zapisane w zmiennej o nazwie **`Plan`** .</span><span class="sxs-lookup"><span data-stu-id="8eb88-115">The **`OutVariable`** parameter is specified so the results are returned and simultaneously stored in a variable named **`Plan`**.</span></span>

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 5.2.0 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

<span data-ttu-id="8eb88-116">Jak pokazano w poniższych danych wyjściowych, plan uaktualniania określa plik i punkty przesunięcia, które wymagają zmian podczas przechodzenia z modułu AzureRM do poleceń cmdlet modułu Az programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8eb88-116">As shown in the following output, the upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

```Output
Order Location                                                   UpgradeType     PlanResult             Original
----- --------                                                   -----------     ----------             --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter ReadyToUpgrade         ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          ReadyToUpgrade         New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          ReadyToUpgrade         New-AzureRmVM...
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          ReadyToUpgrade         New-AzureRmPu...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          ReadyToUpgrade         New-AzureRmVi...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          ReadyToUpgrade         New-AzureRmVi...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          ReadyToUpgrade         New-AzureRmRe...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter ReadyToUpgrade         ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          ReadyToUpgrade         New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          ReadyToUpgrade         New-AzureRmRe...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter ReadyToUpgrade         ExtensionName
...
```

<span data-ttu-id="8eb88-117">Przed uaktualnieniem należy wyświetlić wyniki planu, aby sprawdzić je pod kątem problemów.</span><span class="sxs-lookup"><span data-stu-id="8eb88-117">Before performing the upgrade, you need to view the results of the plan for problems.</span></span> <span data-ttu-id="8eb88-118">W poniższym przykładzie jest zwracana lista skryptów i elementów w tych skryptach, które uniemożliwią ich automatyczne uaktualnienie.</span><span class="sxs-lookup"><span data-stu-id="8eb88-118">The following example returns a list of scripts and the items in those scripts that will prevent them from being upgraded automatically.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

<span data-ttu-id="8eb88-119">Elementy widoczne w następujących danych wyjściowych nie zostaną uaktualnione automatycznie bez uprzedniego skorygowania problemów w sposób ręczny.</span><span class="sxs-lookup"><span data-stu-id="8eb88-119">The items shown in the following output will not be upgraded automatically without manually correcting the issues first.</span></span>

```Output
Order                  : 42
UpgradeType            : CmdletParameter
PlanResult             : ErrorParameterNotFound
PlanSeverity           : Error
PlanResultReason       : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="8eb88-120">Krok 2. Uaktualnianie</span><span class="sxs-lookup"><span data-stu-id="8eb88-120">Step 2: Perform the upgrade</span></span>

> [!CAUTION]
> <span data-ttu-id="8eb88-121">Tej operacji nie można cofnąć.</span><span class="sxs-lookup"><span data-stu-id="8eb88-121">There is no undo operation.</span></span> <span data-ttu-id="8eb88-122">Zawsze upewnij się, że masz kopię zapasową skryptów i modułów programu PowerShell, które próbujesz uaktualnić.</span><span class="sxs-lookup"><span data-stu-id="8eb88-122">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

<span data-ttu-id="8eb88-123">Jeśli plan spełnia Twoje wymagania, przeprowadź uaktualnienie za pomocą polecenia cmdlet **`Invoke-AzUpgradeModulePlan`** .</span><span class="sxs-lookup"><span data-stu-id="8eb88-123">After you’re satisfied with the plan, the upgrade is performed with the **`Invoke-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="8eb88-124">Określ wartość **`SaveChangesToNewFiles`** dla parametru **`FileEditMode`** , aby zapobiec wprowadzeniu zmian w oryginalnych skryptach.</span><span class="sxs-lookup"><span data-stu-id="8eb88-124">Specify **`SaveChangesToNewFiles`** for the **`FileEditMode`** parameter value to prevent changes from being made to your original scripts.</span></span> <span data-ttu-id="8eb88-125">W tym trybie uaktualnienie jest wykonywane przez utworzenie kopii każdego skryptu docelowego i dołączenie ciągu _`_az_upgraded`_ do nazw plików.</span><span class="sxs-lookup"><span data-stu-id="8eb88-125">When using this mode, the upgrade is performed by creating a copy of each script targeted with _`_az_upgraded`_ appended to the filenames.</span></span>

> [!WARNING]
> <span data-ttu-id="8eb88-126">Polecenie cmdlet **`Invoke-AzUpgradeModulePlan`** jest destrukcyjne, jeśli zostanie określona opcja **`-FileEditMode ModifyExistingFiles`** !</span><span class="sxs-lookup"><span data-stu-id="8eb88-126">The **`Invoke-AzUpgradeModulePlan`** cmdlet is destructive when the **`-FileEditMode ModifyExistingFiles`** option is specified!</span></span> <span data-ttu-id="8eb88-127">Modyfikuje ono skrypty i funkcje w miejscu zgodnie z planem uaktualniania modułu wygenerowanym przez polecenie cmdlet **`New-AzUpgradeModulePlan`** .</span><span class="sxs-lookup"><span data-stu-id="8eb88-127">It modifies your scripts and functions in place according to the module upgrade plan generated by the **`New-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="8eb88-128">Można zamiast tego użyć opcji niedestrukcyjnej **`-FileEditMode SaveChangesToNewFiles`** .</span><span class="sxs-lookup"><span data-stu-id="8eb88-128">For the non-destructive option specify **`-FileEditMode SaveChangesToNewFiles`** instead.</span></span>

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles -OutVariable Results
```

```Output
Order Location                                                   UpgradeType     UpgradeResult    Original
----- --------                                                   -----------     -------------    --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter UpgradeCompleted ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMExtens...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          UpgradeCompleted New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMSshPub...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMNetwor...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMSource...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMOperat...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          UpgradeCompleted New-AzureRmVMConfig
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkI...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          UpgradeCompleted New-AzureRmPublicIp...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          UpgradeCompleted New-AzureRmResource...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter UpgradeCompleted ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          UpgradeCompleted New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          UpgradeCompleted New-AzureRmResource...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter UpgradeCompleted ExtensionName
...
```

<span data-ttu-id="8eb88-129">W przypadku zwrócenia błędów można bliżej przyjrzeć się wynikom dla błędów za pomocą następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="8eb88-129">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

```Output
Order                  : 42
UpgradeType            : CmdletParameter
UpgradeResult          : UnableToUpgrade
UpgradeSeverity        : Error
UpgradeResultReason    : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="limitations"></a><span data-ttu-id="8eb88-130">Ograniczenia</span><span class="sxs-lookup"><span data-stu-id="8eb88-130">Limitations</span></span>

* <span data-ttu-id="8eb88-131">Operacje We/Wy na plikach używają domyślnego kodowania.</span><span class="sxs-lookup"><span data-stu-id="8eb88-131">File I/O operations use default encoding.</span></span> <span data-ttu-id="8eb88-132">Nietypowe kodowanie plików może powodować problemy.</span><span class="sxs-lookup"><span data-stu-id="8eb88-132">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="8eb88-133">Polecenia cmdlet modułu AzureRM przekazane jako argumenty do pozornych instrukcji testu jednostkowego usługi Pester nie są wykrywane.</span><span class="sxs-lookup"><span data-stu-id="8eb88-133">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="8eb88-134">Obecnie jako element docelowy jest obsługiwany tylko moduł Az programu PowerShell w wersji 5.2.0.</span><span class="sxs-lookup"><span data-stu-id="8eb88-134">Currently, only Az PowerShell module version 5.2.0 is supported as a target.</span></span>

## <a name="how-to-report-issues"></a><span data-ttu-id="8eb88-135">Jak zgłaszać problemy</span><span class="sxs-lookup"><span data-stu-id="8eb88-135">How to report issues</span></span>

<span data-ttu-id="8eb88-136">Opinie i problemy dotyczące modułu Az.Tools.Migration programu PowerShell można zgłaszać za pośrednictwem [problemu w usłudze GitHub](https://github.com/Azure/azure-powershell-migration/issues) w repozytorium `azure-powershell-migration`.</span><span class="sxs-lookup"><span data-stu-id="8eb88-136">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8eb88-137">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="8eb88-137">Next steps</span></span>

<span data-ttu-id="8eb88-138">Aby dowiedzieć się więcej o module Az programu PowerShell, zapoznaj się z [dokumentacją programu Azure PowerShell](/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="8eb88-138">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](/powershell/azure/)</span></span>
