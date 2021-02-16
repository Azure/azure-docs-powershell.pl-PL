---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242618"
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

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
Pobiera listę nierozpoznanych zależności.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
Zatwierdza zestaw zasobów uwzględniony w treści żądania.
Operacja zatwierdzania jest wyzwalana dla operacji moveResources w operacji moveState "CommitPending" lub "CommitFailed", po pomyślnym ukończeniu operacji moveResource moveState przejście do stanu Zatwierdzone.
Aby pomóc użytkownikowi wstępnie skonfigurować operację, klient może wywołać operację z ustawioną tylko wartością validateOnly property ustawioną na true.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Odrzuca zestaw zasobów uwzględniony w treści żądania.
Operacja odrzucania jest wyzwalana dla operacji moveResources w operacji moveState "CommitPending" lub "DiscardFailed" po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.
Aby pomóc użytkownikowi wstępnie skonfigurować operację, klient może wywołać operację z ustawioną tylko wartością validateOnly property ustawioną na true.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Przenosi zestaw zasobów uwzględniony w treści żądania.
Operacja przenoszenia jest wyzwalana po tym, jak moveResources znajdują się w stanie moveState "MovePending" lub "MoveFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do commitPending.
Aby pomóc użytkownikowi wstępnie skonfigurować operację, klient może wywołać operację z ustawioną tylko wartością validateOnly property ustawioną na true.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
Inicjuje przygotowywanie zestawu zasobów zawartych w treści żądania.
Operacja przygotowywania znajduje się na stronie moveResources, które znajdują się w operacji moveState "PreparePending" lub "PrepareFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.
Aby pomóc użytkownikowi wstępnie skonfigurować operację, klient może wywołać operację z ustawioną tylko wartością validateOnly property ustawioną na true.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Tworzy lub aktualizuje kolekcję przenoszenia.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Usuwa kolekcję przenoszenia.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Usuwa zasób przenieś z kolekcji przenoszenia.

### [Resolve-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Oblicza, oblicza i sprawdza zależności elementów moveResources w kolekcji przenoszenia.

