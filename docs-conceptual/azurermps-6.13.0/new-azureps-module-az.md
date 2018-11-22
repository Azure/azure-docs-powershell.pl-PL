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
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259738"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Wprowadzenie do nowego modułu Az programu Azure PowerShell

Począwszy od listopada 2018 r. moduł `Az` programu Azure PowerShell jest dostępny w publicznej wersji zapoznawczej.
Moduł Az oferuje krótsze polecenia, lepszą stabilność i obsługuje systemy Windows, macOS i Linux. Moduł Az zapewnia również równoważność funkcji i łatwą ścieżkę migracji z modułu AzureRM.

Moduł Az korzysta z biblioteki .NET Standard, co oznacza, że działa w programie PowerShell w wersjach 5.x i 6.x.
Ponieważ program PowerShell w wersji 6.x działa w systemach Linux, macOS i Windows, oznacza to, że moduł Az jest dostępny dla wszystkich platform.
Użycie biblioteki .NET Standard pozwala nam na ujednolicenie bazy kodu programu Azure PowerShell przy minimalnym wpływie na użytkowników.

Az to nowy moduł, dlatego wersja została zresetowana. Pierwszą stabilną wersją będzie wersja 1.0, jednak od listopada 2018 r. moduł ten oferuje równoważność funkcji z modułem AzureRm.

## <a name="upgrade-to-az"></a>Uaktualnianie do modułu Az

Zaleca się, aby użytkownicy przeprowadzili uaktualnienie do nowego modułu `Az`. W tym celu:

* [Odinstaluj moduł AzureRM programu Azure PowerShell](/powershell/azure/uninstall-azurerm-ps)
* [Zainstaluj moduł Az programu Azure PowerShell](/powershell/azure/install-az-ps)
* Po zapoznaniu się z nowym zestawem poleceń włącz tryb zgodności dla modułu AzureRM za pomocą polecenia `Enable-AzureRMAlias`.

## <a name="migrate-existing-scripts-to-az"></a>Migrowanie istniejących skryptów do modułu Az

Duże aktualizacje mogą być kłopotliwe. Jednak moduł `Az` oferuje tryb zgodności, który ułatwia korzystanie z istniejących skryptów podczas pracy nad aktualizacjami do nowej składni. Aby włączyć tryb zgodności z modułem `AzureRM`, użyj polecenia cmdlet `Enable-AzureRmAlias`. To polecenie cmdlet definiuje nazwy poleceń cmdlet modułu `AzureRM` jako aliasy dla nazw poleceń cmdlet nowego modułu `Az`.

Nowe nazwy poleceń cmdlet zaprojektowano tak, aby były łatwe do zapamiętania. Zamiast używać ciągu `AzureRm` lub `Azure` w nazwach poleceń cmdlet, wystarczy użyć ciągu `Az`. Na przykład stare polecenie `New-AzureRmVm` to teraz polecenie `New-AzVm`.

Aby zapoznać się z pełnym opisem procesu migracji, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).

## <a name="the-future-of-support-for-azurerm"></a>Przyszła obsługa techniczna modułu AzureRM

Po wydaniu wersji 1.0 modułu `Az` w grudniu 2018 r. w istniejącym module `AzureRM` nie będą już wprowadzane nowe polecenia cmdlet ani funkcje. Jednak moduł `AzureRM` jest nadal oficjalnie obsługiwany i będą do niego wydawane poprawki błędów. Aby być na bieżąco z najnowszymi usługami i funkcjami platformy Azure, należy przejść na korzystanie z modułu `Az`.