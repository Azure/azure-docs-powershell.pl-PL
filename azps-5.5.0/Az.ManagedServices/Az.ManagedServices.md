---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187491"
---
# Moduł Az.ManagedServices
## Opis
Ta funkcja jest używana przez klientów dostawców usług zarządzanych (MSP). Klienci zapewniają programowi MSP możliwość zarządzania swoją grupą subskrypcji lub zasobów. Oprócz udzielenia dostępu klient może również usunąć dostęp lub wyświetlić istniejący dostęp. Klienci, którzy przyznali im dostęp do subskrypcji, mogą wyświetlać listę klientów. W tym procesie biorą udział dwa obiekty: definicja rejestracji identyfikująca program MSP i definicje ról, które zostały udzielone użytkownikom tego oprogramowania. Program MSP może opcjonalnie zdefiniować ten obiekt przy użyciu witryny marketplace usług zarządzanych oferującej przypisania programu Access, które skojarzą subskrypcję z definicją.

## Az.ManagedServices Cmdlet
### [Get-AzManagedServicesAssignment](Get-AzManagedServicesAssignment.md)
Pobiera konkretne zadanie rejestru lub listę zadań rejestracji.

### [Get-AzManagedServicesDefinition](Get-AzManagedServicesDefinition.md)
Pobiera określoną definicję rejestracji lub listę definicji rejestracji.

### [New-AzManagedServicesAssignment](New-AzManagedServicesAssignment.md)
Tworzy lub aktualizuje zadanie rejestracji.

### [New-AzManagedServicesDefinition](New-AzManagedServicesDefinition.md)
Tworzy lub aktualizuje definicję rejestracji.

### [Remove-AzManagedServicesAssignment](Remove-AzManagedServicesAssignment.md)
Usuwa przypisanie rejestracji.

### [Remove-AzManagedServicesDefinition](Remove-AzManagedServicesDefinition.md)
Usuwa definicję rejestracji.
