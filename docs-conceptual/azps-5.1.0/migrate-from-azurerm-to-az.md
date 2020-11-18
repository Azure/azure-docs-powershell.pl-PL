---
title: Migrowanie skryptów programu Azure PowerShell z modułu AzureRM do modułu Az
description: Poznaj procedury i narzędzia dotyczące migracji skryptów z modułu AzureRM do nowego modułu Az.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715645"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Migrowanie programu Azure PowerShell z modułu AzureRM do modułu Az

Wszystkie wersje modułu AzureRM PowerShell są nieaktualne, ale nie są pozbawione pomocy technicznej. [Moduł Az programu PowerShell](install-az-ps.md) jest obecnie zalecanym modułem programu PowerShell na potrzeby interakcji z platformą Azure.

Skrypty napisane dla poleceń cmdlet modułu AzureRM nie będą automatycznie działać z nowym modułem. Aby ułatwić przeniesienie, opracowano [zestaw narzędzi do migracji modułu AzureRM do Az](https://github.com/Azure/azure-powershell-migration). Każda migracja do nowego zestawu poleceń jest kłopotliwa, jednak ten artykuł pomoże Ci rozpocząć przejście do modułu Az programu PowerShell. Aby dowiedzieć się więcej na temat przyczyn utworzenia modułu Az programu PowerShell, zobacz [Wprowadzenie do nowego modułu Az usługi Azure PowerShell](new-azureps-module-az.md).

Aby wyświetlić pełną listę zmian powodujących niezgodność między modułami AzureRM i Az, zobacz [wszystkie różnice między modułem AzureRM i Az](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Upewnianie się, że istniejące skrypty działają z najnowszą wersją modułu AzureRM

Przed wykonaniem jakichkolwiek kroków związanych z migracją sprawdź, które wersje modułu AzureRM są zainstalowane w systemie.
Dzięki temu możesz się upewnić, że skrypty są już uruchamiane w najnowszej wersji, i dowiedzieć, które wersje modułu AzureRM muszą zostać odinstalowane.

Aby sprawdzić, które wersje modułu AzureRM są zainstalowane, uruchom następujący przykład:

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

**Najnowszą** dostępną wersją modułu AzureRM jest wersja **6.13.1**. Jeśli ta wersja nie jest zainstalowana, może być konieczne dodatkowe zmodyfikowanie istniejących skryptów, aby działały z modułem Az, w sposób wykraczający poza zmiany opisane w tym artykule i na [liście zmian powodujących niezgodność](migrate-az-1.0.0.md).

Jeśli skrypty nie działają z wersją 6.13.1 modułu AzureRM, zaktualizuj je zgodnie z [przewodnikiem migracji modułu AzureRM z wersji 5.x do wersji 6.x](/powershell/azure/azurerm/migration-guide.6.0.0). Jeśli używasz wcześniejszej wersji modułu AzureRM, dostępne są przewodniki migracji dla wszystkich wersji głównych.

## <a name="install-the-azurerm-to-az-migration-toolkit"></a>Instalowanie zestawu narzędzi do migracji modułu AzureRM do Az

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a>Automatyczna migracja skryptów programu PowerShell

Za pomocą zestawu narzędzi do migracji modułu AzureRM do Az można wygenerować plan określający, jakie zmiany zostaną wykonane w skryptach przed wprowadzeniem jakichkolwiek modyfikacji i przed zainstalowaniem modułu Az programu PowerShell.

Przewodnik Szybki start [Automatyczne migrowanie skryptów programu PowerShell z modułu AzureRM do Az programu PowerShell](quickstart-migrate-azurerm-to-az-automatically.md) przeprowadzi Cię przez cały proces automatycznego aktualizowania skryptów programu PowerShell z modułu AzureRM do Az programu PowerShell.

## <a name="next-steps"></a>Następne kroki

[Instalowanie programu Azure PowerShell](install-az-ps.md)
[Odinstalowywanie modułu AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)
