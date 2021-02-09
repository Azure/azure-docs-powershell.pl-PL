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
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100012662"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>Szybki start: Automatyczne migrowanie skryptów programu PowerShell z modułu AzureRM do Az programu PowerShell

W tym artykule dowiesz się, jak przeprowadzić automatyczne uaktualnienie skryptów programu PowerShell i modułów skryptów z modułu AzureRM do Az programu PowerShell za pomocą modułu Az.Tools.Migration programu PowerShell. Aby uzyskać dodatkowe opcje migracji, zobacz [Migrowanie programu Azure PowerShell z modułu AzureRM do modułu Az](/powershell/azure/migrate-from-azurerm-to-az).

## <a name="requirements"></a>Wymagania

* Zaktualizuj istniejące skrypty programu PowerShell do najnowszej wersji [modułu AzureRM programu PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).
* Zainstaluj moduł Az.Tools.Migration programu PowerShell.

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>Krok 1. Generowanie planu uaktualniania

Za pomocą polecenia cmdlet **`New-AzUpgradeModulePlan`** wygeneruj plan uaktualniania służący do migrowania skryptów i modułów do modułu Az programu PowerShell. To polecenie cmdlet nie wprowadza żadnych zmian w istniejących skryptach. Użyj parametru **`FilePath`** , aby wskazać określony skrypt jako docelowy, lub użyj parametru **`DirectoryPath`** , aby wskazać wszystkie skrypty w określonym folderze jako docelowe.

> [!NOTE]
> Polecenie cmdlet **`New-AzUpgradeModulePlan`** nie wykonuje planu, tylko generuje kroki uaktualniania.

Poniższy przykład generuje plan dla wszystkich skryptów w folderze _`C:\Scripts`_ . Został określony parametr **`OutVariable`** , aby wyniki zostały zwrócone i jednocześnie zapisane w zmiennej o nazwie **`Plan`** .

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 5.2.0 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

Jak pokazano w poniższych danych wyjściowych, plan uaktualniania określa plik i punkty przesunięcia, które wymagają zmian podczas przechodzenia z modułu AzureRM do poleceń cmdlet modułu Az programu PowerShell.

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

Przed uaktualnieniem należy wyświetlić wyniki planu, aby sprawdzić je pod kątem problemów. W poniższym przykładzie jest zwracana lista skryptów i elementów w tych skryptach, które uniemożliwią ich automatyczne uaktualnienie.

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

Elementy widoczne w następujących danych wyjściowych nie zostaną uaktualnione automatycznie bez uprzedniego skorygowania problemów w sposób ręczny.

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

## <a name="step-2-perform-the-upgrade"></a>Krok 2. Uaktualnianie

> [!CAUTION]
> Tej operacji nie można cofnąć. Zawsze upewnij się, że masz kopię zapasową skryptów i modułów programu PowerShell, które próbujesz uaktualnić.

Jeśli plan spełnia Twoje wymagania, przeprowadź uaktualnienie za pomocą polecenia cmdlet **`Invoke-AzUpgradeModulePlan`** . Określ wartość **`SaveChangesToNewFiles`** dla parametru **`FileEditMode`** , aby zapobiec wprowadzeniu zmian w oryginalnych skryptach. W tym trybie uaktualnienie jest wykonywane przez utworzenie kopii każdego skryptu docelowego i dołączenie ciągu _`_az_upgraded`_ do nazw plików.

> [!WARNING]
> Polecenie cmdlet **`Invoke-AzUpgradeModulePlan`** jest destrukcyjne, jeśli zostanie określona opcja **`-FileEditMode ModifyExistingFiles`** ! Modyfikuje ono skrypty i funkcje w miejscu zgodnie z planem uaktualniania modułu wygenerowanym przez polecenie cmdlet **`New-AzUpgradeModulePlan`** . Można zamiast tego użyć opcji niedestrukcyjnej **`-FileEditMode SaveChangesToNewFiles`** .

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

W przypadku zwrócenia błędów można bliżej przyjrzeć się wynikom dla błędów za pomocą następującego polecenia:

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

## <a name="limitations"></a>Ograniczenia

* Operacje We/Wy na plikach używają domyślnego kodowania. Nietypowe kodowanie plików może powodować problemy.
* Polecenia cmdlet modułu AzureRM przekazane jako argumenty do pozornych instrukcji testu jednostkowego usługi Pester nie są wykrywane.
* Obecnie jako element docelowy jest obsługiwany tylko moduł Az programu PowerShell w wersji 5.2.0.

## <a name="how-to-report-issues"></a>Jak zgłaszać problemy

Opinie i problemy dotyczące modułu Az.Tools.Migration programu PowerShell można zgłaszać za pośrednictwem [problemu w usłudze GitHub](https://github.com/Azure/azure-powershell-migration/issues) w repozytorium `azure-powershell-migration`.

## <a name="next-steps"></a>Następne kroki

Aby dowiedzieć się więcej o module Az programu PowerShell, zapoznaj się z [dokumentacją programu Azure PowerShell](/powershell/azure/)
