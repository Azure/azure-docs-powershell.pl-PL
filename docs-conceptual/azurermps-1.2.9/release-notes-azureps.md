---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: c57ba563b5a4d4d19944fe8eca2cb4244ee5ed9e
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/06/2018
ms.locfileid: "34819715"
---
# <a name="release-notes"></a>Informacje o wersji

To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.

## <a name="version-129"></a>Wersja 1.2.9

Zmiany w tej wersji

* Moduł AzureRm.AzureStackAdmin
    + Zmiany w poleceniu cmdlet Add-AzureRmResourceProviderRegistration w celu obsługi podziału na administratora usługi Azure Resource Manager i dzierżawę usługi Azure Resource Manager. Został dodany nowy parametr -ResourceManagerType.
    + Z każdego polecenia cmdlet usunięto parametry -AdminUri, -ApiVersion, -SubscriptionId i -Token. Generowane były ostrzeżenia, że te parametry zostaną wycofane, a teraz zostały one usunięte.
* Moduł AzureStackStorage
    + Dodano nowe polecenia cmdlet do obsługi scenariuszy migracji kontenera.
    + Usunięto polecenia cmdlet odwołujące się do wewnętrznych składników i podstawowych funkcji.
* AzureRM.BootStrapper
    + Utworzono nowy moduł do zarządzania wersjami poleceń cmdlet programu Azure PowerShell przy użyciu profilów wersji