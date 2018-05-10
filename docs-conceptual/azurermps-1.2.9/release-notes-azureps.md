---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 5fe7591855577e083aad5923aed37b18d0b2a40c
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/08/2018
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