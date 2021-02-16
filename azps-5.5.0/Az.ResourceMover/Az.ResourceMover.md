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
# <span data-ttu-id="5b653-101">Moduł Az.ResourceMover</span><span class="sxs-lookup"><span data-stu-id="5b653-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="5b653-102">Opis</span><span class="sxs-lookup"><span data-stu-id="5b653-102">Description</span></span>
<span data-ttu-id="5b653-103">Microsoft Azure PowerShell: polecenia cmdlet ResourceMover</span><span class="sxs-lookup"><span data-stu-id="5b653-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="5b653-104">Az.ResourceMover Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b653-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="5b653-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="5b653-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="5b653-106">Tworzy lub aktualizuje zasób przenoszenia w kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="5b653-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="5b653-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="5b653-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="5b653-108">Pobiera kolekcję przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="5b653-108">Gets the move collection.</span></span>

### [<span data-ttu-id="5b653-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="5b653-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="5b653-110">Pobiera zasób przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="5b653-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="5b653-111">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="5b653-111">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="5b653-112">Pobiera listę nierozpoznanych zależności.</span><span class="sxs-lookup"><span data-stu-id="5b653-112">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="5b653-113">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="5b653-113">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="5b653-114">Zatwierdza zestaw zasobów uwzględniony w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="5b653-114">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="5b653-115">Operacja zatwierdzania jest wyzwalana dla operacji moveResources w operacji moveState "CommitPending" lub "CommitFailed", po pomyślnym ukończeniu operacji moveResource moveState przejście do stanu Zatwierdzone.</span><span class="sxs-lookup"><span data-stu-id="5b653-115">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="5b653-116">Aby pomóc użytkownikowi wstępnie skonfigurować operację, klient może wywołać operację z ustawioną tylko wartością validateOnly property ustawioną na true.</span><span class="sxs-lookup"><span data-stu-id="5b653-116">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="5b653-117">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="5b653-117">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="5b653-118">Odrzuca zestaw zasobów uwzględniony w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="5b653-118">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="5b653-119">Operacja odrzucania jest wyzwalana dla operacji moveResources w operacji moveState "CommitPending" lub "DiscardFailed" po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.</span><span class="sxs-lookup"><span data-stu-id="5b653-119">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="5b653-120">Aby pomóc użytkownikowi wstępnie skonfigurować operację, klient może wywołać operację z ustawioną tylko wartością validateOnly property ustawioną na true.</span><span class="sxs-lookup"><span data-stu-id="5b653-120">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="5b653-121">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="5b653-121">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="5b653-122">Przenosi zestaw zasobów uwzględniony w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="5b653-122">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="5b653-123">Operacja przenoszenia jest wyzwalana po tym, jak moveResources znajdują się w stanie moveState "MovePending" lub "MoveFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do commitPending.</span><span class="sxs-lookup"><span data-stu-id="5b653-123">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="5b653-124">Aby pomóc użytkownikowi wstępnie skonfigurować operację, klient może wywołać operację z ustawioną tylko wartością validateOnly property ustawioną na true.</span><span class="sxs-lookup"><span data-stu-id="5b653-124">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="5b653-125">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="5b653-125">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="5b653-126">Inicjuje przygotowywanie zestawu zasobów zawartych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="5b653-126">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="5b653-127">Operacja przygotowywania znajduje się na stronie moveResources, które znajdują się w operacji moveState "PreparePending" lub "PrepareFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.</span><span class="sxs-lookup"><span data-stu-id="5b653-127">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="5b653-128">Aby pomóc użytkownikowi wstępnie skonfigurować operację, klient może wywołać operację z ustawioną tylko wartością validateOnly property ustawioną na true.</span><span class="sxs-lookup"><span data-stu-id="5b653-128">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="5b653-129">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="5b653-129">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="5b653-130">Tworzy lub aktualizuje kolekcję przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="5b653-130">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="5b653-131">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="5b653-131">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="5b653-132">Usuwa kolekcję przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="5b653-132">Deletes a move collection.</span></span>

### [<span data-ttu-id="5b653-133">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="5b653-133">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="5b653-134">Usuwa zasób przenieś z kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="5b653-134">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="5b653-135">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="5b653-135">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="5b653-136">Oblicza, oblicza i sprawdza zależności elementów moveResources w kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="5b653-136">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

