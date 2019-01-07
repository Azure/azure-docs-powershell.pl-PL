---
title: Wprowadzenie do modułu Az programu Azure PowerShell
description: Przedstawiamy nowy moduł programu Azure PowerShell — Az — który zastąpi moduł AzureRM.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: cff9a6ef64907c7ff493dbc9c83dd20a82f297d9
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/19/2018
ms.locfileid: "53594875"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Wprowadzenie do nowego modułu Az programu Azure PowerShell

Począwszy od grudnia 2018 r., moduł Az programu Azure PowerShell jest ogólnie dostępny i interakcja z platformą Azure powinna się teraz odbywać za pomocą tego modułu programu PowerShell. Moduł Az oferuje krótsze polecenia, lepszą stabilność i obsługę wielu platform. Moduł Az zapewnia również równoważność funkcji i łatwą ścieżkę migracji z modułu AzureRM.

Moduł Az korzysta z biblioteki .NET Standard, co oznacza, że działa w programie PowerShell w wersjach 5.x i 6.x.
Ponieważ program PowerShell w wersji 6.x działa w systemach Linux, macOS i Windows, program Azure PowerShell jest teraz dostępny dla wszystkich platform.
Użycie biblioteki .NET Standard pozwala nam na ujednolicenie bazy kodu programu Azure PowerShell przy minimalnym wpływie na użytkowników.

Az to nowy moduł, dlatego wersja została zresetowana do 1.0.0.

## <a name="upgrade-to-az"></a>Uaktualnianie do modułu Az

Zaleca się, aby wszyscy użytkownicy przeprowadzili uaktualnienie do nowego modułu Az. W tym celu:

* __ZALECANE__: [Odinstaluj moduł AzureRM programu Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
* [Zainstaluj moduł Az programu Azure PowerShell](/powershell/azure/install-az-ps)
* Za pomocą polecenia `Enable-AzureRMAlias` włącz tryb zgodności, aby dodać aliasy dla poleceń cmdlet modułu AzureRM na czas zapoznawania się z nowym zestawem poleceń. Włącz aliasy __tylko wtedy__, gdy nie masz zainstalowanego modułu AzureRM.

## <a name="migrate-existing-scripts-to-az"></a>Migrowanie istniejących skryptów do modułu Az

Duże aktualizacje mogą być kłopotliwe. Jednak moduł Az oferuje tryb zgodności, który ułatwia korzystanie z istniejących skryptów podczas pracy nad aktualizacjami do nowej składni. Aby włączyć tryb zgodności z modułem AzureRM, użyj polecenia cmdlet `Enable-AzureRmAlias`. To polecenie cmdlet definiuje nazwy poleceń cmdlet modułu AzureRM jako aliasy dla nazw poleceń cmdlet nowego modułu Az.

Nowe nazwy poleceń cmdlet zaprojektowano tak, aby były łatwe do zapamiętania. Zamiast używać ciągu `AzureRm` lub `Azure` w nazwach poleceń cmdlet, wystarczy użyć ciągu `Az`. Na przykład stare polecenie `New-AzureRMVm` to teraz polecenie `New-AzVm`.

Aby zapoznać się z pełnym opisem procesu migracji, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).

## <a name="the-future-of-support-for-azurerm"></a>Przyszła obsługa techniczna modułu AzureRM

W istniejącym module AzureRM nie będą już wprowadzane nowe polecenia cmdlet ani funkcje. Jednak moduł AzureRM jest nadal oficjalnie obsługiwany i będą dla niego wydawane poprawki błędów. Aby być na bieżąco z najnowszymi usługami i funkcjami platformy Azure, zmień używany moduł na Az.