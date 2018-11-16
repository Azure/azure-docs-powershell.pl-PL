---
title: Migrowanie skryptów programu Azure PowerShell z modułu AzureRM do modułu Az
description: Poznaj procedury i narzędzia dotyczące migracji skryptów z modułu AzureRM do nowego modułu Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 0c73e7ac1d47a2a97b6136fa481d0adce8de33db
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574417"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a>Migrowanie z modułu AzureRM do modułu Az programu Azure PowerShell

Moduł Az zapewnia równoważność funkcji z modułem AzureRM, jednak używa krótszych i bardziej spójnych nazw poleceń cmdlet.
Skrypty napisane dla poleceń cmdlet modułu AzureRM nie będą automatycznie działać z nowym modułem. Aby ułatwić przejście, moduł Az oferuje narzędzia umożliwiające uruchamianie istniejących skryptów przy użyciu modułu AzureRM. Każda migracja do nowego zestawu poleceń jest kłopotliwa, jednak ten artykuł pomoże Ci rozpocząć przejście do nowego modułu.

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a>Upewnianie się, że istniejące skrypty działają z najnowszą wersją modułu AzureRM

To jest najważniejszy krok! Uruchom istniejące skrypty i upewnij się, że działają one z _najnowszą_ wersją modułu AzureRM (__6.12.0__). Jeśli Twoje skrypty nie działają, zapoznaj się z [przewodnikiem po migracji modułu AzureRM](migration-guide.6.0.0.md).

## <a name="install-the-azure-powershell-az-module"></a>Instalowanie modułu Az programu Azure PowerShell

Pierwszym krokiem jest zainstalowanie modułu Az na Twojej platformie. Aby zainstalować moduł Az, należy najpierw odinstalować moduł AzureRM.
W poniższych krokach opisano, co zrobić, aby istniejące skrypty nadal działały, i jak włączyć zgodność ze starymi nazwami poleceń cmdlet.

Aby zainstalować moduł Az programu Azure PowerShell, wykonaj następujące kroki:

* [Odinstaluj moduł AzureRM](uninstall-azurerm-ps.md). Upewnij się, że usuwasz _wszystkie_ zainstalowane wersje modułu AzureRM, a nie tylko najnowszą.
* [Zainstaluj moduł Az](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><a name="aliases"/>Włączanie trybu aliasów modułu AzureRM

Po upewnieniu się, że skrypty działają z najnowszą wersją modułu AzureRM, i odinstalowaniu modułu AzureRM nadszedł czas, aby włączyć tryb zgodności dla modułu Az. Zgodność należy włączyć za pomocą polecenia:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Aliasy umożliwiają używanie starych nazw poleceń cmdlet po zainstalowaniu modułu `Az`. Te aliasy są wpisane w profil użytkownika dla wybranego zakresu. Jeśli profil użytkownika nie istnieje, jest on tworzony.

> [!WARNING]
>
> Dla tego polecenia można użyć innego parametru `-Scope`, ale nie jest to zalecane! Aliasy są wpisane w profil użytkownika dla wybranego zakresu, dlatego włączaj je dla tak ograniczonego zakresu, jak to możliwe. Włączenie aliasów dla całego systemu może także spowodować problemy dla innych użytkowników, którzy mają zainstalowany moduł `AzureRM` w swoim zakresie lokalnym.

Po włączeniu trybu aliasów ponownie uruchom skrypty, aby potwierdzić, że nadal działają zgodnie z oczekiwaniami. 

## <a name="change-module-imports-and-cmdlet-names"></a>Zmienianie importów modułu i nazw poleceń cmdlet

Ogólnie rzecz biorąc, nazwy modułu zostały zmienione tak, aby nazwy `AzureRM` i `Azure` stały się nazwą `Az` — to samo dotyczy poleceń cmdlet.
Na przykład nazwa modułu `AzureRM.Compute` została zmieniona na `Az.Compute`. Polecenie `New-AzureRmVM` stało się poleceniem `New-AzVM`, a polecenie `Get-AzureStorageBlob` to teraz polecenie `Get-AzStorageBlob`.

Istnieją wyjątki od tej reguły zmiany nazw, o których należy wiedzieć przed rozpoczęciem zmieniania nazewnictwa:

| Moduł AzureRM | Moduł Az |
|----------------|-----------|
| AzureRM.DataFactories | Az.DataFactory |
| AzureRM.DataFactoryV2 | Az.DataFactory |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices |

## <a name="summary"></a>Podsumowanie

Wykonując powyższe czynności, można zaktualizować wszystkie istniejące skrypty w celu korzystania z nowego modułu. Jeśli masz jakiekolwiek pytania lub problemy dotyczące tych kroków, które utrudniały migrację, dodaj komentarz do tego artykułu, abyśmy mogli ulepszyć instrukcje.