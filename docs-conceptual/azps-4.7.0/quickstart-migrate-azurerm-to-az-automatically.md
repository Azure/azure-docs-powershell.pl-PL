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
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>Szybki start: Automatyczne migrowanie skryptów programu PowerShell z modułu AzureRM do Az programu PowerShell

W tym artykule dowiesz się, jak przeprowadzić automatyczne uaktualnienie skryptów programu PowerShell i modułów skryptów z modułu AzureRM do Az programu PowerShell za pomocą modułu Az.Tools.Migration programu PowerShell.

> [!IMPORTANT]
> Moduł Az.Tools.Migration programu PowerShell jest obecnie w publicznej wersji zapoznawczej. Ta wersja zapoznawcza jest dostępna bez umowy dotyczącej poziomu usług. Nie jest ona zalecana w przypadku obciążeń produkcyjnych. Niektóre funkcje mogą być nieobsługiwane lub ograniczone. Aby uzyskać więcej informacji, zobacz [Uzupełniające warunki korzystania z wersji zapoznawczych platformy Microsoft Azure](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).

Opinie i problemy dotyczące modułu Az.Tools.Migration programu PowerShell można zgłaszać za pośrednictwem [problemu w usłudze GitHub](https://github.com/Azure/azure-powershell-migration/issues) w repozytorium `azure-powershell-migration`.

## <a name="requirements"></a>Wymagania

* Zaktualizuj istniejące skrypty programu PowerShell do najnowszej wersji [modułu AzureRM programu PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).
* Zainstaluj moduł Az.Tools.Migration programu PowerShell.

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>Krok 1. Generowanie planu uaktualniania

Za pomocą polecenia cmdlet `New-AzUpgradeModulePlan` wygeneruj plan uaktualniania służący do migrowania skryptów i modułów do modułu Az programu PowerShell. Plan uaktualniania zawiera szczegóły dotyczące określonego pliku i punktów przesunięcia, które wymagają zmian podczas przechodzenia z modułu AzureRM do modułu Az programu PowerShell.

> [!NOTE]
> Polecenie cmdlet `New-AzUpgradeModulePlan` nie wykonuje planu, tylko generuje kroki uaktualniania.

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

Przejrzyj wyniki planu uaktualniania.

```powershell
# Show the entire upgrade plan
$Plan
```

Uruchom następujące polecenie, aby przefiltrować wyniki poleceń, które mają ostrzeżenia lub błędy. Może to być przydatne w przypadku dużych zestawów wyników, aby szybko identyfikować błędy przed przeprowadzeniem uaktualnienia.

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a>Krok 2. Uaktualnianie

Plan uaktualniania jest wykonywany po uruchomieniu polecenia cmdlet `Invoke-AzUpgradeModulePlan`. To polecenie wykonuje uaktualnienie określonego pliku lub folderów z wyjątkiem błędów, które zostały zidentyfikowane przez polecenie cmdlet `New-AzUpgradeModulePlan`.

To polecenie wymaga określenia, czy pliki mają być modyfikowane na miejscu, czy też nowe pliki powinny zostać zachowane razem z oryginalnymi plikami (pozostawiając oryginalne pliki bez modyfikacji).

> [!CAUTION]
> Tej operacji nie można cofnąć. Zawsze upewnij się, że masz kopię zapasową skryptów i modułów programu PowerShell, które próbujesz uaktualnić.

> [!WARNING]
> Polecenie cmdlet `Invoke-AzUpgradeModulePlan` jest destrukcyjne, jeśli zostanie określona opcja `-FileEditMode ModifyExistingFiles`! Modyfikuje ono skrypty i funkcje na miejscu zgodnie z planem uaktualniania modułu wygenerowanym przez polecenie cmdlet `New-AzUpgradeModulePlan`. Zamiast tego polecenia należy skorzystać z niedestrukcyjnego polecenia cmdlet `-FileEditMode SaveChangesToNewFiles`.

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

Przejrzyj wyniki operacji uaktualniania.

```powershell
# Show the results for the entire upgrade operation
$Results
```

W przypadku zwrócenia błędów można bliżej przyjrzeć się wynikom dla błędów za pomocą następującego polecenia:

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a>Ograniczenia

* Automatyczne aktualizacje nazw parametrów w zestawach parametrów nie są obsługiwane. W przypadku znalezienia takiego zestawu podczas generowania planu uaktualniania zostanie zwrócone ostrzeżenie.
* Operacje We/Wy na plikach używają domyślnego kodowania. Nietypowe kodowanie plików może powodować problemy.
* Polecenia cmdlet modułu AzureRM przekazane jako argumenty do pozornych instrukcji testu jednostkowego usługi Pester nie są wykrywane.
* Obecnie jako element docelowy jest obsługiwany tylko moduł Az programu PowerShell w wersji 4.6.1.

## <a name="next-steps"></a>Następne kroki

Aby dowiedzieć się więcej o module Az programu PowerShell, zapoznaj się z [dokumentacją programu Azure PowerShell](https://docs.microsoft.com/powershell/azure/)