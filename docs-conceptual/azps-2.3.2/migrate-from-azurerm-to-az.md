---
title: Migrowanie skryptów programu Azure PowerShell z modułu AzureRM do modułu Az
description: Poznaj procedury i narzędzia dotyczące migracji skryptów z modułu AzureRM do nowego modułu Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/10/2019
ms.openlocfilehash: 02b39653ebb4aa0f74d2340a7be7b35e08d5e44d
ms.sourcegitcommit: 0356a4694f77eda40eec8c3759b9bb7f28979eb6
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/18/2019
ms.locfileid: "67193026"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Migrowanie programu Azure PowerShell z modułu AzureRM do modułu Az

Moduł Az zapewnia równoważność funkcji z modułem AzureRM, jednak używa krótszych i bardziej spójnych nazw poleceń cmdlet.
Skrypty napisane dla poleceń cmdlet modułu AzureRM nie będą automatycznie działać z nowym modułem. Aby ułatwić przejście, moduł Az oferuje narzędzia umożliwiające uruchamianie istniejących skryptów przy użyciu modułu AzureRM. Każda migracja do nowego zestawu poleceń jest kłopotliwa, jednak ten artykuł pomoże Ci rozpocząć przejście do nowego modułu.

Aby wyświetlić pełną listę zmian powodujących niezgodność między modułami AzureRM i Az, zobacz [wszystkie różnice między modułem AzureRM i Az](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Upewnianie się, że istniejące skrypty działają z najnowszą wersją modułu AzureRM

Przed wykonaniem jakichkolwiek kroków związanych z migracją sprawdź, które wersje modułu AzureRM są zainstalowane w systemie. Dzięki temu możesz się upewnić, że skrypty są już uruchamiane w najnowszej wersji, i dowiedzieć, które wersje modułu AzureRM muszą zostać odinstalowane.

Aby sprawdzić, które wersje modułu AzureRM są zainstalowane, uruchom polecenie:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

__Najnowszą__ dostępną wersją modułu AzureRM jest wersja __6.13.1__. Jeśli ta wersja nie jest zainstalowana, może być konieczne dodatkowe zmodyfikowanie istniejących skryptów, aby działały z modułem Az, w sposób wykraczający poza zmiany opisane tutaj i na [liście zmian powodujących niezgodność](migrate-az-1.0.0.md).

Jeśli skrypty nie działają z wersją 6.13.1 modułu AzureRM, zaktualizuj je zgodnie z [przewodnikiem migracji modułu AzureRM z wersji 5.x do wersji 6.x](/powershell/azure/azurerm/migration-guide.6.0.0).
Jeśli używasz wcześniejszej wersji modułu AzureRM, dostępne są przewodniki migracji dla wszystkich wersji głównych.

## <a name="uninstall-azurerm"></a>Odinstalowywanie modułu AzureRM

Zgodność modułu Az z wszelkimi istniejącymi instalacjami modułu AzureRM w programie PowerShell 5.1 dla systemu Windows nie jest gwarantowana. Przed zainstalowaniem modułu Az [odinstaluj moduł AzureRM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).

> [!IMPORTANT]
>
> Jeśli nie chcesz jeszcze usuwać modułu AzureRM z systemu, możesz zamiast tego zainstalować moduł Az dla programu [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) w wersji 6.x lub nowszej. Programy PowerShell Core i PowerShell 5.1 dla systemu Windows korzystają z różnych bibliotek modułów, więc nie wystąpią żadne konflikty. Nadal możesz [włączyć aliasy](#enable-azurerm-compatibility-aliases) w programie PowerShell Core.

## <a name="install-the-azure-powershell-az-module"></a>Instalowanie modułu Az programu Azure PowerShell

Pierwszym krokiem jest zainstalowanie modułu Az na Twojej platformie. Po zainstalowaniu modułu Az zaleca się odinstalowanie modułu AzureRM. W poniższych krokach opisano, co zrobić, aby istniejące skrypty nadal działały, i jak włączyć zgodność ze starymi nazwami poleceń cmdlet.

Aby zainstalować moduł Az programu Azure PowerShell, postępuj zgodnie z instrukcjami w artykule [Instalowanie modułu Az](install-az-ps.md).

> [!NOTE]
> W tym momencie możesz uruchomić polecenie cmdlet [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) udostępnione w module Az, aby upewnić się, że wszystkie wersje modułu AzureRM zostały odinstalowane i nie będą powodować konfliktów.

## <a name="enable-azurerm-compatibility-aliases"></a>Włączanie aliasów zapewniających zgodność z modułem AzureRM

Po upewnieniu się, że skrypty działają z najnowszą wersją modułu AzureRM, i odinstalowaniu modułu AzureRM następny krok to włączenie trybu zgodności dla modułu Az. Zgodność należy włączyć za pomocą polecenia:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Aliasy umożliwiają używanie starych nazw poleceń cmdlet po zainstalowaniu modułu Az. Te aliasy są zapisywane w profilu dla wybranego zakresu. Jeśli profil nie istnieje, zostanie utworzony.
W przypadku użycia parametru `-Scope` określającego zakres szerszy niż `CurrentUser` wymagane są uprawnienia niezbędne do utworzenia lub zaktualizowania odpowiedniego pliku profilu.

> [!IMPORTANT]
> Aliasy są tworzone __tylko__ dla nazw poleceń. Nie są tworzone aliasy nazw modułów. Jeśli używasz instrukcji `#Requires` lub `Import-Module`, list zależności w pliku `.psd1` albo w pełni kwalifikowanych nazw poleceń cmdlet, koniecznie przeprowadź ich migrację na tym etapie, zgodnie z procesem omówionym w sekcji dotyczącej nazw modułów artykułu z [listą zmian powodujących niezgodność](migrate-az-1.0.0.md).

> [!WARNING]
>
> Dla tego polecenia możesz użyć innego parametru `-Scope`, ale nie jest to zalecane. Aliasy są wpisane w profil użytkownika dla wybranego zakresu, dlatego włączaj je dla tak ograniczonego zakresu, jak to możliwe. Włączenie aliasów dla całego systemu może spowodować problemy dla innych użytkowników, którzy mają moduł AzureRM zainstalowany w swoim zakresie lokalnym.

Po włączeniu trybu aliasów ponownie uruchom skrypty, aby potwierdzić, że nadal działają zgodnie z oczekiwaniami.
Niektóre nazwy parametrów zostały zmienione lub dodane albo stały się wymagane przez moduł Az. Ponadto mogły ulec zmianie typy danych wyjściowych poleceń cmdlet. Te zmiany są szczegółowo opisane na [liście zmian powodujących niezgodność](migrate-az-1.0.0.md).

## <a name="update-cmdlets-modules-and-parameters"></a>Aktualizacja poleceń cmdlet, modułów i parametrów

Gdy skrypty zostaną zaktualizowane i będą działać przy użyciu aliasów, możesz stopniowo aktualizować je w celu używania nowych poleceń cmdlet i skorzystania z innych zmian, np. nowych funkcji. W przypadku większości skryptów wystarczy zaktualizować nazwy poleceń cmdlet [zgodnie z nowym schematem nazewnictwa poleceń cmdlet w module Az](migrate-az-1.0.0.md#cmdlet-noun-prefix-changes). Aby skrypty działały, być może trzeba będzie również wprowadzić inne zmiany w zależności od tego, jakie operacje przeprowadzają i z których funkcji programu Azure PowerShell korzystają.

Na przykład [polecenia cmdlet usługi Blob Storage](migrate-az-1.0.0.md#azstorage-previously-azurestorage-and-azurermstorage) zostały całkowicie przeprojektowane w celu używania nowego modelu asynchronicznego, więc aktualizacja skryptów, które z nich korzystają, będzie wymagać więcej pracy niż aktualizacja skryptów, w których wystarczy zmienić nazwy poleceń cmdlet.

Nawet jeśli do tej pory wystarczyło wprowadzić w skryptach niewielkie, proste zmiany (lub jeśli działają one bez zmian po włączeniu aliasów), przeczytaj [pełną listę zmian powodujących niezgodność w module Az 1.0.0](migrate-az-1.0.0.md), aby upewnić się, że nie polegasz na „przezroczystym” zachowaniu aliasów, które może zniknąć po zmianie nazw poleceń cmdlet i wyłączeniu aliasów.

## <a name="disable-aliases"></a>Wyłączanie aliasów

Po ukończeniu migracji, gdy już nie polegasz na zachowaniu aliasów, zaleca się wyłączenie aliasów. Służy do tego polecenie [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).

> [!IMPORTANT]
> Podczas uruchamiania tego polecenia cmdlet __upewnij się, że__ zostanie ono wywołane dla każdej wartości `-Scope`, dla której wywołano polecenie cmdlet `Enable-AzureRmAlias`. W przeciwnym razie w systemie mogą nadal istnieć skrypty polegające na zachowaniu aliasów.
