---
title: Wprowadzenie do modułu Az programu Azure PowerShell
description: Przedstawiamy nowy moduł programu Azure PowerShell — Az — który zastąpi moduł AzureRM.
ms.date: 05/20/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 0771bc474f43d8bbf392f2eba10da2e320d30556
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753869"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Wprowadzenie do nowego modułu Az programu Azure PowerShell

Począwszy od grudnia 2018 r., moduł Az programu Azure PowerShell jest ogólnie dostępny i interakcja z platformą Azure powinna się teraz odbywać za pomocą tego modułu programu PowerShell. Moduł Az oferuje krótsze polecenia, lepszą stabilność i obsługę wielu platform. Moduł Az też ma równoważność funkcji z modułem AzureRM, co zapewnia łatwą ścieżkę migracji.

> [!NOTE]
> Program PowerShell w wersji 7.x lub nowszej jest zalecaną wersją programu PowerShell do używania z programem Azure PowerShell na wszystkich platformach.

Dzięki najnowszemu modułowi Az program Azure PowerShell współpracuje z programem PowerShell 6.2.4 lub nowszym na wszystkich platformach, w tym w systemach Windows, macOS i Linux. Jest on również zgodny z programem PowerShell 5.1 w systemie Windows.

Az to nowy moduł, dlatego wersja została zresetowana do 1.0.0.

## <a name="why-a-new-module"></a>Dlaczego wprowadzamy nowy moduł?

Duże aktualizacje mogą być kłopotliwe. Dlatego chcemy poinformować Cię o powodach podjęcia decyzji o wprowadzeniu nowego zestawu modułów z nowymi poleceniami cmdlet w celu interakcji z platformą Azure za pomocą programu PowerShell.

Największa i najważniejsza zmiana wiąże się z tym, że program PowerShell stał się produktem dla wielu platform od czasu wprowadzenia programu [PowerShell](/powershell/scripting/overview) opartego na bibliotece .NET Standard.
Dążymy do tego, aby obsługa platformy Azure była możliwa na wszystkich platformach, co oznaczało konieczność aktualizacji modułów programu Azure PowerShell, aby korzystały z biblioteki .NET Standard i były zgodne z programem PowerShell Core. Zamiast wprowadzać złożone zmiany w module AzureRM w celu dodania tej obsługi, utworzyliśmy moduł Az.

Ponadto utworzenie nowego modułu pozwoliło naszym inżynierom na uspójnienie projektu i nazw poleceń cmdlet oraz modułów. Wszystkie moduły rozpoczynają się teraz prefiksem `Az.`, a wszystkie polecenia cmdlet używają formatu _Czasownik_-`Az`_Rzeczownik_ . Wcześniej nazwy poleceń cmdlet były nie tylko dłuższe, ale też niespójne.

Zmniejszona została również liczba modułów: Niektóre moduły, które działały z tymi samymi usługami, zostały połączone. Polecenia cmdlet płaszczyzny zarządzania i płaszczyzny danych są teraz zawarte w pojedynczych modułach dla swoich usług. Znacznie upraszcza to pracę osobom, które ręcznie zarządzają zależnościami i importowaniem.

Wprowadzając te istotne zmiany wymagające utworzenia nowego modułu programu Azure PowerShell, zespół zobowiązał się do maksymalnego uproszczenia korzystania z platformy Azure za pomocą poleceń cmdlet programu PowerShell oraz zapewnienia obsługi na jak największej liczbie platform.

## <a name="upgrade-to-az"></a>Uaktualnianie do modułu Az

Aby być na bieżąco z najnowszymi funkcjami platformy Azure w programie PowerShell, jak najszybciej przeprowadź migrację do modułu Az. Jeśli Twoje środowisko nie jest gotowe do zainstalowania modułu Az w celu zastąpienia modułu AzureRM, dostępnych jest kilka opcji umożliwiających eksperymentowanie z modułem Az:

- Korzystaj ze środowiska `PowerShell` w usłudze [Azure Cloud Shell](https://docs.microsoft.com/azure/cloud-shell/overview). Usługa Azure Cloud Shell to środowisko powłoki oparte na przeglądarce, w którym zainstalowano moduł Az oraz włączono aliasy zapewniające zgodność przy użyciu polecenia cmdlet `Enable-AzureRM`.
- Pozostaw moduł AzureRM zainstalowany w programie PowerShell 5.1 dla systemu Windows, ale zainstaluj moduł Az dla programu PowerShell w wersji 6.2.4 lub nowszej. Programy PowerShell 5.1 dla systemu Windows i PowerShell 6.2.4 lub nowsze korzystają z oddzielnych kolekcji modułów. Postępuj zgodnie z instrukcjami, aby zainstalować [najnowszą wersję programu PowerShell](/powershell/scripting/install/installing-powershell), a następnie [zainstaluj moduł Az](install-az-ps.md) z programu PowerShell 6.2.4 lub nowszego.

Aby uaktualnić istniejącą instalację modułu AzureRM:

1. [Odinstaluj moduł AzureRM programu Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
2. [Zainstaluj moduł Az programu Azure PowerShell](install-az-ps.md)
3. **OPCJONALNIE** : Za pomocą polecenia [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) włącz tryb zgodności, aby dodać aliasy dla poleceń cmdlet modułu AzureRM na czas zapoznawania się z nowym zestawem poleceń. Więcej szczegółowych informacji znajduje się w następnej sekcji oraz artykule [Rozpoczynanie migracji z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).

## <a name="migrate-existing-scripts-to-az"></a>Migrowanie istniejących skryptów do modułu Az

Nowe nazwy poleceń cmdlet zaprojektowano tak, aby były łatwe do zapamiętania. Zamiast używać ciągu `AzureRm` lub `Azure` w nazwach poleceń cmdlet, wystarczy użyć ciągu `Az`. Na przykład stare polecenie `New-AzureRMVm` to teraz polecenie `New-AzVm`.
Migracja to jednak nie tylko zapoznanie się z nowymi nazwami poleceń cmdlet. Zmieniono nazwy modułów i parametrów oraz wprowadzono inne ważne zmiany.

Aby ułatwić proces migracji z modułu AzureRM do Az, udostępniamy wiele zasobów:

- [Wprowadzenie do migracji z modułu AzureRM do Az](migrate-from-azurerm-to-az.md)
- [Pełna lista zmian powodujących niezgodność w module Az 1.0.0 względem modułu AzureRM](migrate-az-1.0.0.md)
- Polecenie cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias)

Moduł Az oferuje tryb zgodności, który ułatwia korzystanie z istniejących skryptów podczas pracy nad aktualizacjami do nowej składni. Polecenie cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) włącza tryb zgodności przy użyciu aliasów, aby możliwe było używanie istniejących skryptów z minimalnymi zmianami podczas pracy nad pełną migracją do modułu Az. Domyślnie polecenie `Enable-AzureRmAlias` włącza tylko aliasy zgodności dla bieżącej sesji programu PowerShell. Użyj parametru `Scope`, aby zachować aliasy zgodności między sesjami programu PowerShell. Aby uzyskać więcej informacji, zobacz [dokumentację dotyczącą polecenia Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).

> [!IMPORTANT]
> Chociaż dostępne są aliasy dla nazw poleceń cmdlet, w przypadku poleceń cmdlet modułu Az mogły zostać dodane (lub zmienione) parametry albo zmienione wartości zwracane. Nie oczekuj, że włączenie aliasów rozwiąże problem migracji za Ciebie. Zobacz [pełną listę zmian powodujących niezgodność](migrate-az-1.0.0.md), aby dowiedzieć się, w których miejscach skryptów trzeba wprowadzić aktualizacje.

## <a name="continued-support-for-azurerm"></a>Dalsze wsparcie modułu AzureRM

W module AzureRM nie będą już wprowadzane nowe polecenia cmdlet ani funkcje. Jednak moduł AzureRM jest nadal oficjalnie obsługiwany i będą dla niego wydawane poprawki błędów do grudnia 2020 r.
