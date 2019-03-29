---
title: Migrowanie skryptów programu Azure PowerShell z modułu AzureRM do modułu Az
description: Poznaj procedury i narzędzia dotyczące migracji skryptów z modułu AzureRM do nowego modułu Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 28122ca953d62b405f19effbbc680f2dc6202cca
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475380"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a>Migrowanie z modułu AzureRM do modułu Az programu Azure PowerShell

Moduł Az zapewnia równoważność funkcji z modułem AzureRM, jednak używa krótszych i bardziej spójnych nazw poleceń cmdlet.
Skrypty napisane dla poleceń cmdlet modułu AzureRM nie będą automatycznie działać z nowym modułem. Aby ułatwić przejście, moduł Az oferuje narzędzia umożliwiające uruchamianie istniejących skryptów przy użyciu modułu AzureRM. Każda migracja do nowego zestawu poleceń jest kłopotliwa, jednak ten artykuł pomoże Ci rozpocząć przejście do nowego modułu.

Aby wyświetlić pełną listę zmian powodujących niezgodność między modułami AzureRM i Az, zobacz [Przewodnik migracji modułu Az 1.0.0](migrate-az-1.0.0.md)

## <a name="check-for-installed-versions-of-azurerm"></a>Sprawdzanie pod kątem zainstalowanych wersji modułu AzureRM

Moduły Az i AzureRM mogą być zainstalowane obok siebie, ale nie jest to zalecane. Przed wykonaniem jakichkolwiek kroków związanych z migracją sprawdź, które wersje modułu AzureRM są zainstalowane w systemie. Dzięki temu możesz się upewnić, że skrypty są już uruchamiane w najnowszej wersji, i dowiedzieć, czy możesz włączyć aliasy poleceń bez odinstalowywania modułu AzureRM.

Aby sprawdzić, które wersje modułu AzureRM są zainstalowane, uruchom polecenie:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a>Upewnianie się, że istniejące skrypty działają z najnowszą wersją modułu AzureRM

To jest najważniejszy krok! Uruchom istniejące skrypty i upewnij się, że działają one z _najnowszą_ wersją modułu AzureRM (__6.13.1__). Jeśli Twoje skrypty nie działają, zapoznaj się z [przewodnikiem po migracji modułu AzureRM](/powershell/azure/azurerm/migration-guide.6.0.0).

## <a name="install-the-azure-powershell-az-module"></a>Instalowanie modułu Az programu Azure PowerShell

Pierwszym krokiem jest zainstalowanie modułu Az na Twojej platformie. Po zainstalowaniu modułu Az zaleca się odinstalowanie modułu AzureRM. W poniższych krokach opisano, co zrobić, aby istniejące skrypty nadal działały, i jak włączyć zgodność ze starymi nazwami poleceń cmdlet.

Aby zainstalować moduł Az programu Azure PowerShell, wykonaj następujące kroki:

* __ZALECANE__: [Odinstaluj moduł AzureRM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).
  Upewnij się, że usuwasz _wszystkie_ zainstalowane wersje modułu AzureRM, a nie tylko najnowszą.
* [Zainstaluj moduł Az](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-compatibility-aliases"></a><a name="aliases"/>Włączanie aliasów zapewniających zgodność z modułem AzureRM 

> [!IMPORTANT]
>
> Tryb zgodności włącz tylko wtedy, gdy zostały odinstalowane _wszystkie_ wersje modułu AzureRM. Włączenie trybu zgodności, gdy polecenia cmdlet modułu AzureRM są nadal dostępne, może spowodować nieprzewidywalne zachowanie. Pomiń ten krok, jeśli chcesz pozostawić zainstalowany moduł AzureRM, ale pamiętaj, że wszelkie polecenia cmdlet modułu AzureRM będą używać starszych modułów i nie będą wywoływać żadnych poleceń cmdlet modułu Az.

Po upewnieniu się, że skrypty działają z najnowszą wersją modułu AzureRM, i odinstalowaniu modułu AzureRM następny krok to włączenie trybu zgodności dla modułu Az. Zgodność należy włączyć za pomocą polecenia:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Aliasy umożliwiają używanie starych nazw poleceń cmdlet po zainstalowaniu modułu Az. Te aliasy są wpisane w profil użytkownika dla wybranego zakresu. Jeśli profil użytkownika nie istnieje, jest on tworzony.

> [!WARNING]
>
> Dla tego polecenia możesz użyć innego parametru `-Scope`, ale nie jest to zalecane. Aliasy są wpisane w profil użytkownika dla wybranego zakresu, dlatego włączaj je dla tak ograniczonego zakresu, jak to możliwe. Włączenie aliasów dla całego systemu może także spowodować problemy dla innych użytkowników, którzy mają zainstalowany moduł AzureRM w swoim zakresie lokalnym.

Po włączeniu trybu aliasów ponownie uruchom skrypty, aby potwierdzić, że nadal działają zgodnie z oczekiwaniami. 

## <a name="change-module-imports-and-cmdlet-names"></a>Zmienianie importów modułu i nazw poleceń cmdlet

Ogólnie rzecz biorąc, nazwy modułu zostały zmienione tak, aby nazwy `AzureRM` i `Azure` stały się nazwą `Az` — to samo dotyczy poleceń cmdlet.
Na przykład nazwa modułu `AzureRM.Compute` została zmieniona na `Az.Compute`. Polecenie `New-AzureRMVM` stało się poleceniem `New-AzVM`, a polecenie `Get-AzureStorageBlob` to teraz polecenie `Get-AzStorageBlob`.

Istnieją wyjątki od tej reguły zmiany nazw, o których należy wiedzieć. Nazwy niektórych modułów zostały zmienione lub te moduły zostały scalone z istniejącymi modułami, przy czym nie miało to wpływu na sufiks ich poleceń cmdlet poza zmianą ciągu `AzureRM` lub `Azure` na `Az`. W pozostałych przypadkach pełny sufiks polecenia cmdlet został zmieniony, aby odzwierciedlić nową nazwę modułu.

| Moduł AzureRM | Moduł Az | Czy sufiks poleceń cmdlet uległ zmianie? |
|----------------|-----------|------------------------|
| AzureRM.Profile | Az.Accounts | Yes |
| AzureRM.Insights | Az.Monitor | Yes |
| AzureRM.DataFactories | Az.DataFactory | Yes |
| AzureRM.DataFactoryV2 | Az.DataFactory | Yes |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices | Nie |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices | Nie |
| AzureRM.Tags | Az.Resources | Nie |
| AzureRM.MachineLearningCompute | Az.MachineLearning | Nie |
| AzureRM.UsageAggregates | Az.Billing | Nie |
| AzureRM.Consumption | Az.Billing | Nie |

## <a name="summary"></a>Podsumowanie

Wykonując powyższe czynności, można zaktualizować wszystkie istniejące skrypty w celu korzystania z nowego modułu. Jeśli masz jakiekolwiek pytania lub problemy dotyczące tych kroków, które utrudniały migrację, dodaj komentarz do tego artykułu, abyśmy mogli ulepszyć instrukcje.
