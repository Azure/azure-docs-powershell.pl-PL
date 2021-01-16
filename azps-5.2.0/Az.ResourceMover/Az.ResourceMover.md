---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358780"
---
# AZ. ResourceMover, moduł
## Opis
Microsoft Azure PowerShell: polecenia cmdlet ResourceMover

## AZ. ResourceMover polecenia cmdlet
### [Dodaj-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
Tworzy lub aktualizuje zasób Przenieś w kolekcji Move.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
Pobiera kolekcję Przenieś.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
Pobiera przeniesienie zasobu.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
Pobiera listę nierozwiązanych zależności.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
Zatwierdza zbiór zasobów uwzględnionych w treści żądania.
Operacja Zatwierdź jest wyzwalana na moveResources w moveState "CommitPending" lub "CommitFailed", po poprawnym zakończeniu, moveResource moveState to przejście do zatwierdzenia.
Aby pomóc użytkownikowi na wstępną konieczność działania, z którym klient może nawiązać operację, należy ustawić właściwość validateOnly równą true.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Odrzuca zestaw zasobów uwzględnionych w treści żądania.
Operacja Odrzuć jest wyzwalana na moveResources w moveState "CommitPending" lub "DiscardFailed", po poprawnym zakończeniu, moveResource moveState, aby przejść do MovePending.
Aby pomóc użytkownikowi na wstępną konieczność działania, z którym klient może nawiązać operację, należy ustawić właściwość validateOnly równą true.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Powoduje przeniesienie zestawu zasobów uwzględnionych w treści żądania.
Operacja przenoszenia jest wyzwalana, gdy moveResources znajduje się w moveState "MovePending" lub "MoveFailed", po poprawnym wykonaniu moveResource moveState, aby przejść do CommitPending.
Aby pomóc użytkownikowi na wstępną konieczność działania, z którym klient może nawiązać operację, należy ustawić właściwość validateOnly równą true.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
Inicjuje przygotowanie zestawu zasobów uwzględnionych w treści żądania.
Operacja przygotowywania znajduje się na moveResourcesie, który znajduje się w moveState "PreparePending" lub "PrepareFailed", po poprawnym wykonaniu moveResource moveState to przejście do MovePending.
Aby pomóc użytkownikowi na wstępną konieczność działania, z którym klient może nawiązać operację, należy ustawić właściwość validateOnly równą true.

### [Nowe — AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Tworzy lub aktualizuje kolekcję Przenieś.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Usuwa kolekcję Przenieś.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Usuwa zasób Przenieś z kolekcji Move.

### [Rozpoznaj — AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Oblicza, rozpoznaje i sprawdza poprawność zależności moveResources w kolekcji Move.

