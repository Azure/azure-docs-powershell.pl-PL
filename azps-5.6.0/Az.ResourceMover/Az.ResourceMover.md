---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: 0f43535baa284dbe9f7c69aee5a688443172089a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000049"
---
# Moduł Az.ResourceMover
## Opis
Microsoft Azure PowerShell: polecenia cmdlet ResourceMover

## Az.ResourceMover Cmdlet
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
Tworzy lub aktualizuje zasób przenoszenia w kolekcji przenoszenia.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
Pobiera kolekcję przenoszenia.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
Pobiera zasób przenoszenia.

### [Get-AzResourceMoverRequiredForResources](Get-AzResourceMoverRequiredForResources.md)
Lista zasobów przenoszenia, dla których jest wymagany zasób arm.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
Pobiera listę nierozpoznanych zależności.

### [Invoke-AzResourceMoverBulkRemove](Invoke-AzResourceMoverBulkRemove.md)
Usuwa z kolekcji przenoszenie zestaw zasobów przeniesienia zawartych w treści żądania.
Projekt jest wykonywane przez usługę.
Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
Zatwierdza zestaw zasobów uwzględniony w treści żądania.
Operacja zatwierdzania jest wyzwalana dla operacji moveResources w operacji moveState "CommitPending" lub "CommitFailed" po pomyślnym ukończeniu operacji moveResource moveState przejście do stanu Zatwierdzone.
Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Odrzuca zestaw zasobów uwzględniony w treści żądania.
Operacja odrzucania jest wyzwalana dla operacji moveResources w operacji moveState "CommitPending" lub "DiscardFailed" po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.
Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Przenosi zestaw zasobów uwzględniony w treści żądania.
Operacja przenoszenia jest wyzwalana po tym, jak moveResources znajdują się w stanie moveState "MovePending" lub "MoveFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do commitPending.
Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
Inicjuje przygotowywanie zestawu zasobów zawartych w treści żądania.
Operacja przygotowywania znajduje się na stronie moveResources, które znajdują się w operacji moveState "PreparePending" lub "PrepareFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.
Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Tworzy lub aktualizuje kolekcję przenoszenia.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Usuwa kolekcję przenoszenia.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Usuwa zasób przenieś z kolekcji przenoszenia.

### [Resolve-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Oblicza, oblicza i sprawdza zależności elementów moveResources w kolekcji przenoszenia.

