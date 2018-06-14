---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 91d97260568a36e1135196899503fb0c8e1c6731
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853019"
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