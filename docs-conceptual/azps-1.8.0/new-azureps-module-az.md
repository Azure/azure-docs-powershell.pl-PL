---
title: Wprowadzenie do modułu Az programu Azure PowerShell
description: Przedstawiamy nowy moduł programu Azure PowerShell — Az — który zastąpi moduł AzureRM.
ms.date: 02/12/2021
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: f6ffd66d20943541c3591d41db7c72861f44204c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415465"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Wprowadzenie do nowego modułu Az programu Azure PowerShell

Począwszy od grudnia 2018 r., moduł Az programu Azure PowerShell jest ogólnie dostępny i interakcja z platformą Azure powinna się teraz odbywać za pomocą tego modułu programu PowerShell. Moduł Az oferuje krótsze polecenia, lepszą stabilność i obsługę wielu platform. Moduł Az też ma równoważność funkcji z modułem AzureRM, co zapewnia łatwą ścieżkę migracji.

Dzięki modułowi Az program Azure PowerShell jest teraz zgodny z programem PowerShell 5.1 w systemie Windows oraz programem PowerShell Core w wersji 6.x i nowszych na wszystkich obsługiwanych platformach — w tym Windows, macOS i Linux.

Az to nowy moduł, dlatego wersja została zresetowana do 1.0.0.

## <a name="why-a-new-module"></a>Dlaczego wprowadzamy nowy moduł?

Duże aktualizacje mogą być kłopotliwe. Dlatego chcemy poinformować Cię o powodach podjęcia decyzji o wprowadzeniu nowego zestawu modułów z nowymi poleceniami cmdlet w celu interakcji z platformą Azure za pomocą programu PowerShell.

Największa i najważniejsza zmiana wiąże się z tym, że program PowerShell stał się produktem dla wielu platform od czasu wprowadzenia programu [PowerShell](/powershell/scripting/overview) opartego na bibliotece .NET Standard.
Dążymy do tego, aby obsługa platformy Azure była możliwa na wszystkich platformach, co oznaczało konieczność aktualizacji modułów programu Azure PowerShell, aby korzystały z biblioteki .NET Standard i były zgodne z programem PowerShell Core. Zamiast wprowadzać złożone zmiany w module AzureRM w celu dodania tej obsługi, utworzyliśmy moduł Az.

Ponadto utworzenie nowego modułu dało naszym inżynierom szansę na uspójnienie projektu i nazw poleceń cmdlet oraz modułów. Wszystkie moduły rozpoczynają się teraz prefiksem `Az.`, a wszystkie polecenia cmdlet używają formatu _Czasownik_-`Az`_Rzeczownik_. Wcześniej nazwy poleceń cmdlet były nie tylko dłuższe, ale też niespójne.

Zmniejszona została również liczba modułów: Niektóre moduły, które działały z tymi samymi usługami, zostały połączone, a wszystkie polecenia cmdlet płaszczyzny zarządzania i płaszczyzny danych znajdują się teraz w pojedynczych modułach dla odpowiednich usług. Znacznie upraszcza to pracę osobom, które ręcznie zarządzają zależnościami i importowaniem.

Wprowadzając te istotne zmiany wymagające utworzenia nowego modułu programu Azure PowerShell, zespół zobowiązał się do maksymalnego uproszczenia korzystania z platformy Azure za pomocą poleceń cmdlet programu PowerShell oraz zapewnienia obsługi na jak największej liczbie platform.

## <a name="upgrade-to-az"></a>Uaktualnianie do modułu Az

Aby być na bieżąco z najnowszymi funkcjami platformy Azure w programie PowerShell, jak najszybciej przeprowadź migrację do modułu Az. Jeśli Twoje środowisko nie jest gotowe do zainstalowania modułu Az w celu zastąpienia modułu AzureRM, dostępnych jest kilka opcji umożliwiających eksperymentowanie z modułem Az:

* Korzystaj ze środowiska `PowerShell` w usłudze [Azure Cloud Shell](/azure/cloud-shell/overview). Usługa Azure Cloud Shell to środowisko powłoki oparte na przeglądarce, w którym zainstalowano moduł Az oraz włączono aliasy zapewniające zgodność przy użyciu polecenia cmdlet `Enable-AzureRM`.
* Pozostaw moduł AzureRM zainstalowany w programie PowerShell 5.1 dla systemu Windows, ale zainstaluj moduł Az w programie PowerShell Core w wersji 6.x lub nowszej. Programy PowerShell 5.1 dla systemu Windows i PowerShell Core korzystają z oddzielnych kolekcji modułów. Postępuj zgodnie z instrukcjami, aby [zainstalować program PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows), a następnie [zainstalować moduł Az](install-az-ps.md) z poziomu terminala programu PowerShell Core.

Aby uaktualnić istniejącą instalację modułu AzureRM:

1. [Odinstaluj moduł AzureRM programu Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
2. [Zainstaluj moduł Az programu Azure PowerShell](install-az-ps.md)
3. **OPCJONALNIE**: Za pomocą polecenia [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) włącz tryb zgodności, aby dodać aliasy dla poleceń cmdlet modułu AzureRM na czas zapoznawania się z nowym zestawem poleceń. Więcej szczegółowych informacji znajduje się w następnej sekcji oraz artykule [Rozpoczynanie migracji z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).

## <a name="migrate-existing-scripts-to-az"></a>Migrowanie istniejących skryptów do modułu Az

Nowe nazwy poleceń cmdlet zaprojektowano tak, aby były łatwe do zapamiętania. Zamiast używać ciągu `AzureRm` lub `Azure` w nazwach poleceń cmdlet, wystarczy użyć ciągu `Az`. Na przykład stare polecenie `New-AzureRMVm` to teraz polecenie `New-AzVm`.
Migracja to jednak nie tylko zapoznanie się z nowymi nazwami poleceń cmdlet: Zmieniono nazwy modułów i parametrów oraz wprowadzono inne ważne zmiany.

Aby ułatwić proces migracji z modułu AzureRM do Az, udostępniamy wiele zasobów:

* [Wprowadzenie do migracji z modułu AzureRM do Az](migrate-from-azurerm-to-az.md)
* [Pełna lista zmian powodujących niezgodność w module Az 1.0.0 względem modułu AzureRM](migrate-az-1.0.0.md)
* Polecenie cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias)

Moduł Az oferuje tryb zgodności, który ułatwia korzystanie z istniejących skryptów podczas pracy nad aktualizacjami do nowej składni. Polecenie cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) włącza tryb zgodności przy użyciu aliasów, aby możliwe było używanie istniejących skryptów z minimalnymi zmianami podczas pracy nad pełną migracją do modułu Az.

> [!IMPORTANT]
> Chociaż dostępne są aliasy dla nazw poleceń cmdlet, w przypadku poleceń cmdlet modułu Az mogły zostać dodane (lub zmienione) parametry albo zmienione wartości zwracane. Nie oczekuj, że włączenie aliasów rozwiąże problem migracji za Ciebie. Zobacz [pełną listę zmian powodujących niezgodność](migrate-az-1.0.0.md), aby dowiedzieć się, w których miejscach skryptów trzeba wprowadzić aktualizacje.

## <a name="support-for-azurerm"></a>Obsługa AzureRM

Ponieważ AZ PowerShell modules ma teraz wszystkie możliwości modułów AzureRM PowerShell i nie tylko, wycofamy moduły AzureRM PowerShell w dniu 29 lutego 2024.

Aby uniknąć przerw w działaniu usługi, [zaktualizuj skrypty](https://aka.ms/azpsmigrate) używające modułów AzureRM PowerShell do używania polecenia AZ PowerShell modules do 29 lutego 2024. Aby automatycznie aktualizować skrypty, postępuj zgodnie z [przewodnikiem Szybki Start](/powershell/azure/quickstart-migrate-azurerm-to-az-automatically).
