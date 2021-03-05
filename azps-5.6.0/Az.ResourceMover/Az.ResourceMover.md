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
# <span data-ttu-id="7891e-101">Moduł Az.ResourceMover</span><span class="sxs-lookup"><span data-stu-id="7891e-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="7891e-102">Opis</span><span class="sxs-lookup"><span data-stu-id="7891e-102">Description</span></span>
<span data-ttu-id="7891e-103">Microsoft Azure PowerShell: polecenia cmdlet ResourceMover</span><span class="sxs-lookup"><span data-stu-id="7891e-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="7891e-104">Az.ResourceMover Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7891e-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="7891e-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="7891e-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="7891e-106">Tworzy lub aktualizuje zasób przenoszenia w kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="7891e-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="7891e-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="7891e-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="7891e-108">Pobiera kolekcję przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="7891e-108">Gets the move collection.</span></span>

### [<span data-ttu-id="7891e-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="7891e-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="7891e-110">Pobiera zasób przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="7891e-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="7891e-111">Get-AzResourceMoverRequiredForResources</span><span class="sxs-lookup"><span data-stu-id="7891e-111">Get-AzResourceMoverRequiredForResources</span></span>](Get-AzResourceMoverRequiredForResources.md)
<span data-ttu-id="7891e-112">Lista zasobów przenoszenia, dla których jest wymagany zasób arm.</span><span class="sxs-lookup"><span data-stu-id="7891e-112">List of the move resources for which an arm resource is required for.</span></span>

### [<span data-ttu-id="7891e-113">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="7891e-113">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="7891e-114">Pobiera listę nierozpoznanych zależności.</span><span class="sxs-lookup"><span data-stu-id="7891e-114">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="7891e-115">Invoke-AzResourceMoverBulkRemove</span><span class="sxs-lookup"><span data-stu-id="7891e-115">Invoke-AzResourceMoverBulkRemove</span></span>](Invoke-AzResourceMoverBulkRemove.md)
<span data-ttu-id="7891e-116">Usuwa z kolekcji przenoszenie zestaw zasobów przeniesienia zawartych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="7891e-116">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="7891e-117">Projekt jest wykonywane przez usługę.</span><span class="sxs-lookup"><span data-stu-id="7891e-117">The orchestration is done by service.</span></span>
<span data-ttu-id="7891e-118">Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.</span><span class="sxs-lookup"><span data-stu-id="7891e-118">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="7891e-119">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="7891e-119">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="7891e-120">Zatwierdza zestaw zasobów uwzględniony w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="7891e-120">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="7891e-121">Operacja zatwierdzania jest wyzwalana dla operacji moveResources w operacji moveState "CommitPending" lub "CommitFailed" po pomyślnym ukończeniu operacji moveResource moveState przejście do stanu Zatwierdzone.</span><span class="sxs-lookup"><span data-stu-id="7891e-121">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="7891e-122">Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.</span><span class="sxs-lookup"><span data-stu-id="7891e-122">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="7891e-123">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="7891e-123">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="7891e-124">Odrzuca zestaw zasobów uwzględniony w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="7891e-124">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="7891e-125">Operacja odrzucania jest wyzwalana dla operacji moveResources w operacji moveState "CommitPending" lub "DiscardFailed" po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.</span><span class="sxs-lookup"><span data-stu-id="7891e-125">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="7891e-126">Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.</span><span class="sxs-lookup"><span data-stu-id="7891e-126">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="7891e-127">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="7891e-127">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="7891e-128">Przenosi zestaw zasobów uwzględniony w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="7891e-128">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="7891e-129">Operacja przenoszenia jest wyzwalana po tym, jak moveResources znajdują się w stanie moveState "MovePending" lub "MoveFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do commitPending.</span><span class="sxs-lookup"><span data-stu-id="7891e-129">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="7891e-130">Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.</span><span class="sxs-lookup"><span data-stu-id="7891e-130">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="7891e-131">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="7891e-131">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="7891e-132">Inicjuje przygotowywanie zestawu zasobów zawartych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="7891e-132">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="7891e-133">Operacja przygotowywania znajduje się na stronie moveResources, które znajdują się w operacji moveState "PreparePending" lub "PrepareFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.</span><span class="sxs-lookup"><span data-stu-id="7891e-133">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="7891e-134">Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.</span><span class="sxs-lookup"><span data-stu-id="7891e-134">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="7891e-135">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="7891e-135">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="7891e-136">Tworzy lub aktualizuje kolekcję przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="7891e-136">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="7891e-137">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="7891e-137">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="7891e-138">Usuwa kolekcję przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="7891e-138">Deletes a move collection.</span></span>

### [<span data-ttu-id="7891e-139">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="7891e-139">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="7891e-140">Usuwa zasób przenieś z kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="7891e-140">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="7891e-141">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="7891e-141">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="7891e-142">Oblicza, oblicza i sprawdza zależności elementów moveResources w kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="7891e-142">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

