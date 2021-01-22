---
title: Migrowanie skryptów programu Azure PowerShell z modułu AzureRM do modułu Az
description: Poznaj procedury i narzędzia dotyczące migracji skryptów programu Azure PowerShell z modułu AzureRM do nowego modułu Az programu PowerShell.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 12/15/2020
ms.custom: devx-track-azurepowershell, contperf-fy21q2
ms.openlocfilehash: 6bccaf9a628f67b8945516bae70f07939cdce8f7
ms.sourcegitcommit: 12bb1a6d1f89789bf2a78992f9b8ca848691a4d7
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/19/2021
ms.locfileid: "98574150"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Migrowanie programu Azure PowerShell z modułu AzureRM do modułu Az

Wszystkie wersje modułu AzureRM programu PowerShell są nieaktualne. [Moduł Az programu PowerShell](install-az-ps.md) jest obecnie zalecanym modułem programu PowerShell na potrzeby interakcji z platformą Azure.

## <a name="why-a-new-module"></a>Dlaczego wprowadzamy nowy moduł?

Największa i najważniejsza zmiana wiąże się z tym, że program [PowerShell](/powershell/scripting/overview) oparty na bibliotece .NET Standard stał się produktem dla wielu platform od czasu jego wprowadzenia.

Podobnie jak w przypadku języka programu PowerShell, dążymy do tego, aby pomoc techniczna platformy Azure była możliwa na wszystkich platformach. Nasze zobowiązanie oznaczało konieczność aktualizacji modułów programu Azure PowerShell, aby korzystały z biblioteki .NET Standard i były zgodne z programem PowerShell Core. Zamiast modyfikować istniejący moduł AzureRM i wprowadzać złożone zmiany w celu dodania tej obsługi, utworzyliśmy moduł Az.

Ponadto utworzenie nowego modułu pozwoliło naszym inżynierom na uspójnienie projektu, nazw poleceń cmdlet oraz modułów. Wszystkie moduły rozpoczynają się teraz prefiksem `Az.`, a wszystkie polecenia cmdlet używają konwencji nazewnictwa `Verb-AzNoun`. Wcześniej nazwy poleceń cmdlet były dłuższe i niespójne.

Zmniejszona została również liczba modułów: Niektóre moduły, które działały z tymi samymi usługami, zostały połączone. Polecenia cmdlet płaszczyzny zarządzania i płaszczyzny danych w ramach tej samej usługi są teraz zawarte w pojedynczym module. Ta konsolidacja znacznie upraszcza pracę osobom, które ręcznie zarządzają zależnościami i importowaniem.

Wprowadzając te istotne zmiany, zespół zobowiązał się do uproszczenia korzystania z platformy Azure za pomocą poleceń cmdlet programu PowerShell oraz zapewnienia obsługi na jak największej liczbie platform niż kiedykolwiek wcześniej.

## <a name="upgrading-to-az-powershell"></a>Uaktualnianie do modułu Az programu PowerShell

Skrypty napisane dla poleceń cmdlet modułu AzureRM nie będą automatycznie działać z modułem Az. Aby ułatwić przeniesienie, opracowano [zestaw narzędzi do migracji modułu AzureRM do Az](https://github.com/Azure/azure-powershell-migration). Każda migracja do nowego zestawu poleceń jest kłopotliwa, jednak ten artykuł pomoże Ci rozpocząć przejście do modułu Az programu PowerShell. Aby dowiedzieć się więcej na temat przyczyn utworzenia modułu Az programu PowerShell, zobacz [Wprowadzenie do nowego modułu Az usługi Azure PowerShell](new-azureps-module-az.md).

Nowe nazwy poleceń cmdlet zaprojektowano tak, aby były łatwe do zapamiętania. Zamiast używać ciągu `AzureRm` lub `Azure` w nazwach poleceń cmdlet, wystarczy użyć ciągu `Az`. Na przykład stare polecenie cmdlet `New-AzureRMVm` to teraz polecenie `New-AzVm`.
Jednak migracja to coś więcej, niż tylko zapoznanie się z nowymi nazwami poleceń cmdlet. Zmieniono nazwy modułów i parametrów oraz wprowadzono inne ważne zmiany.

Aby wyświetlić pełną listę zmian powodujących niezgodność między modułami AzureRM i Az, zobacz [wszystkie różnice między modułem AzureRM i Az](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Upewnianie się, że istniejące skrypty działają z najnowszą wersją modułu AzureRM

Przed wykonaniem jakichkolwiek kroków związanych z migracją sprawdź, które wersje modułu AzureRM są zainstalowane w systemie.
Dzięki temu możesz się upewnić, że skrypty są już uruchamiane w najnowszej wersji, i dowiedzieć, które wersje modułu AzureRM muszą zostać odinstalowane.

Aby sprawdzić, które wersje modułu AzureRM są zainstalowane, uruchom następujący przykład:

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

**Najnowszą** dostępną wersją modułu AzureRM jest wersja **6.13.1**. Jeśli ta wersja nie jest zainstalowana, może być konieczne dodatkowe zmodyfikowanie istniejących skryptów, aby działały z modułem Az, w sposób wykraczający poza zakres opisany w tym artykule i na [liście zmian powodujących niezgodność](migrate-az-1.0.0.md).

Jeśli skrypty nie działają z wersją 6.13.1 modułu AzureRM, zaktualizuj je zgodnie z [przewodnikiem migracji modułu AzureRM z wersji 5.x do wersji 6.x](/powershell/azure/azurerm/migration-guide.6.0.0). Jeśli używasz wcześniejszej wersji modułu AzureRM, dostępne są przewodniki migracji dla wszystkich wersji głównych.

## <a name="option-1-recommended-automatically-migrate-your-powershell-scripts"></a>Opcja 1 (zalecana): Automatyczna migracja skryptów programu PowerShell

Ta zalecana opcja minimalizuje nakład pracy wymagany do migracji skryptów modułu AzureRM do modułu Az.

### <a name="install-the-azurerm-to-az-migration-toolkit"></a>Instalowanie zestawu narzędzi do migracji modułu AzureRM do Az

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

### <a name="convert-your-scripts-automatically"></a>Automatyczne konwertowanie skryptów

Za pomocą zestawu narzędzi do migracji modułu AzureRM do Az można wygenerować plan określający, jakie zmiany zostaną wykonane w skryptach przed wprowadzeniem jakichkolwiek modyfikacji i przed zainstalowaniem modułu Az programu PowerShell.

Przewodnik Szybki start [Automatyczne migrowanie skryptów programu PowerShell z modułu AzureRM do Az programu PowerShell](quickstart-migrate-azurerm-to-az-automatically.md) przeprowadzi Cię przez cały proces automatycznego aktualizowania skryptów programu PowerShell z modułu AzureRM do Az programu PowerShell.

## <a name="option-2-use-compatibility-mode-with-enable-azurermalias"></a>Opcja 2: Użycie trybu zgodności za pomocą polecenia Enable-AzureRmAlias

Moduł Az oferuje tryb zgodności, który ułatwia korzystanie z istniejących skryptów podczas pracy nad aktualizacjami do nowej składni. Polecenie cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) włącza tryb zgodności przy użyciu aliasów. Ten tryb pozwala na użycie istniejących skryptów z minimalnymi zmianami podczas pracy nad pełną migracją do modułu Az. Domyślnie polecenie `Enable-AzureRmAlias` włącza tylko aliasy zgodności dla bieżącej sesji programu PowerShell. Użyj parametru `Scope`, aby zachować aliasy zgodności między sesjami programu PowerShell. Aby uzyskać więcej informacji, zobacz [dokumentację dotyczącą polecenia Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).

> [!IMPORTANT]
> Chociaż dostępne są aliasy dla nazw poleceń cmdlet, w przypadku poleceń cmdlet modułu Az mogły zostać dodane (lub zmienione) parametry albo zmienione wartości zwracane. Nie oczekuj, że włączenie aliasów rozwiąże problem migracji za Ciebie. Zobacz [pełną listę zmian powodujących niezgodność](migrate-az-1.0.0.md), aby dowiedzieć się, w których miejscach skryptów trzeba wprowadzić aktualizacje.

## <a name="option-3-migrate-your-scripts-in-visual-studio-code-with-the-azure-powershell-extension"></a>Opcja 3: Migrowanie skryptów w programie Visual Studio Code za pomocą rozszerzenia programu Azure PowerShell

### <a name="install-the-azure-powershell-extension-for-visual-studio-code"></a>Instalowanie rozszerzenia programu Azure PowerShell dla programu Visual Studio Code

Zainstaluj [rozszerzenie programu Azure PowerShell dla programu VSCode](https://marketplace.visualstudio.com/items?itemName=azps-tools.azps-tools)

### <a name="convert-your-scripts-manually"></a>Ręczne konwertowanie skryptów

1. Załaduj skrypt modułu AzureRM do programu VSCode
2. Rozpocznij migrację, otwierając paletę poleceń `Ctrl+Shift+P` i wybierz polecenie `Migrate Azure PowerShell script`
3. Wybierz wersję źródłową `AzureRM`
4. Postępuj zgodnie z zalecanymi akcjami dla każdego podkreślonego polecenia lub parametru.

## <a name="next-steps"></a>Następne kroki

* [Odinstalowywanie modułu AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)
* [Instalowanie programu Azure PowerShell](install-az-ps.md)
