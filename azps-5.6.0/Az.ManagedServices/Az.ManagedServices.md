---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 33c6f65e258ee16b0ffb6a4616ffd1c7c5f16c77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962906"
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
