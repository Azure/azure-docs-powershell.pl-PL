---
title: Omówienie programu Azure PowerShell
description: Omówienie modułu Az programu Azure PowerShell wraz z informacjami na temat instalowania i rozpoczynania pracy.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 1978ba5415a27349ac68175144cca0d89fa26d96
ms.sourcegitcommit: 0b644bfecf4224b2ea83520d1a6a956734d9fba4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/12/2019
ms.locfileid: "67863889"
---
# <a name="overview-of-azure-powershell"></a>Omówienie programu Azure PowerShell

Program Azure PowerShell udostępnia zestaw poleceń cmdlet, które pozwalają zarządzać zasobami platformy Azure przy użyciu modelu usługi [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview). Program Azure PowerShell używa platformy .NET Standard, dzięki czemu jest dostępny dla systemów Windows, macOS i Linux.
Program Azure PowerShell jest również dostępny w usłudze Azure Cloud Shell.

## <a name="about-the-new-az-module"></a>Informacje o nowym module Az

W tej dokumentacji opisano nowy moduł Az programu Azure PowerShell. Ten nowy moduł został napisany od podstaw na platformie .NET Standard. Dzięki użyciu platformy .NET Standard program Azure PowerShell może działać w ramach programu PowerShell 5.1 w systemie Windows lub programu PowerShell Core 6.x lub nowszego na dowolnej platformie. Interakcja z platformą Azure za pośrednictwem programu PowerShell powinna się teraz odbywać za pomocą modułu Az.
Usterki w module AzureRM będą nadal usuwane, ale nie będą już w nim wprowadzane żadne nowe funkcje.

Szczegółowe informacje dotyczące nowego modułu, w tym zmienione nazwy poleceń i plany konserwacji modułu AzureRM, znajdują się w artykule [Wprowadzenie do modułu Az programu Azure PowerShell](new-azureps-module-az.md). Jeśli od razu chcesz rozpocząć pracę przy użyciu nowego modułu, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).

Dostępna jest także [dokumentacja modułu AzureRM](/powershell/azure/azurerm).

> [!IMPORTANT]
>
> Dokumentacja platformy Azure jest aktualizowana w celu odzwierciedlenia nowych nazw poleceń cmdlet modułu, ale artykuły mogą nadal zawierać polecenia modułu AzureRM. Po zainstalowaniu modułu Az zaleca się włączenie aliasów poleceń cmdlet modułu AzureRM za pomocą polecenia `Enable-AzureRmAlias`. Więcej szczegółów znajduje się w artykule [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).

## <a name="run-or-install"></a>Uruchamianie lub instalowanie

Program Azure PowerShell można zainstalować w programie PowerShell 5.1 lub nowszym w systemie Windows i w programie PowerShell Core 6.x lub nowszym na dowolnej platformie albo uruchamiać w usłudze Azure Cloud Shell.

* Aby uruchomić program w przeglądarce przy użyciu usługi Azure Cloud Shell, zobacz [Przewodnik Szybki start dotyczący programu PowerShell w usłudze Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).
* Aby zainstalować program Azure PowerShell w swoim systemie, zobacz [Instalowanie programu Azure PowerShell](install-az-ps.md).

Aby uzyskać informacje o najnowszej wersji programu Azure PowerShell, zobacz [informacje o wersji](release-notes-azureps.md).

## <a name="get-started"></a>Rozpoczęcie pracy

Przeczytaj artykuł [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md), aby poznać podstawy programu Azure PowerShell. Jeśli nie znasz programu PowerShell, pomocne może być wprowadzenie:

* [Instalowanie programu PowerShell](/powershell/scripting/install/installing-powershell)
* [Tworzenie skryptów przy użyciu programu PowerShell](/powershell/scripting/powershell-scripting)
* [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Podstawy programu PowerShell, część 1: Wprowadzenie do programu PowerShell)

Poniższe przykłady mogą pomóc w przypadku niektórych typowych zastosowań platformy Azure:

* [Maszyny wirtualne z systemem Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [Maszyny wirtualne z systemem Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [Bazy danych SQL](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a>Rozwijanie umiejętności dzięki środowisku Microsoft Learn

- [Automatyzowanie zadań platformy Azure za pomocą skryptów programu PowerShell](/learn/modules/automate-azure-tasks-with-powershell/)
- [Więcej interakcyjnych zasobów szkoleniowych...](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a>Inne moduły programu Azure PowerShell

* [Azure Active Directory](/powershell/azure/active-directory/)
* [Azure Service Fabric](/powershell/azure/service-fabric/)
* [Azure ElasticDB](/powershell/azure/elasticdbjobs/)
