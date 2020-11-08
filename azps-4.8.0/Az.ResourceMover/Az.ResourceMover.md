---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220914"
---
# <span data-ttu-id="e97d5-101">AZ. ResourceMover, moduł</span><span class="sxs-lookup"><span data-stu-id="e97d5-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="e97d5-102">Opis</span><span class="sxs-lookup"><span data-stu-id="e97d5-102">Description</span></span>
<span data-ttu-id="e97d5-103">Microsoft Azure PowerShell: polecenia cmdlet ResourceMover</span><span class="sxs-lookup"><span data-stu-id="e97d5-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="e97d5-104">AZ. ResourceMover polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="e97d5-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="e97d5-105">Dodaj-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="e97d5-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="e97d5-106">Tworzy lub aktualizuje zasób Przenieś w kolekcji Move.</span><span class="sxs-lookup"><span data-stu-id="e97d5-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="e97d5-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="e97d5-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="e97d5-108">Pobiera kolekcję Przenieś.</span><span class="sxs-lookup"><span data-stu-id="e97d5-108">Gets the move collection.</span></span>

### [<span data-ttu-id="e97d5-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="e97d5-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="e97d5-110">Pobiera przeniesienie zasobu.</span><span class="sxs-lookup"><span data-stu-id="e97d5-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="e97d5-111">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="e97d5-111">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="e97d5-112">Pobiera listę nierozwiązanych zależności.</span><span class="sxs-lookup"><span data-stu-id="e97d5-112">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="e97d5-113">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="e97d5-113">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="e97d5-114">Zatwierdza zbiór zasobów uwzględnionych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="e97d5-114">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="e97d5-115">Operacja Zatwierdź jest wyzwalana na moveResources w moveState "CommitPending" lub "CommitFailed", po poprawnym zakończeniu, moveResource moveState to przejście do zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="e97d5-115">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="e97d5-116">Aby pomóc użytkownikowi na wstępną konieczność działania, z którym klient może nawiązać operację, należy ustawić właściwość validateOnly równą true.</span><span class="sxs-lookup"><span data-stu-id="e97d5-116">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="e97d5-117">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="e97d5-117">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="e97d5-118">Odrzuca zestaw zasobów uwzględnionych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="e97d5-118">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="e97d5-119">Operacja Odrzuć jest wyzwalana na moveResources w moveState "CommitPending" lub "DiscardFailed", po poprawnym zakończeniu, moveResource moveState, aby przejść do MovePending.</span><span class="sxs-lookup"><span data-stu-id="e97d5-119">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="e97d5-120">Aby pomóc użytkownikowi na wstępną konieczność działania, z którym klient może nawiązać operację, należy ustawić właściwość validateOnly równą true.</span><span class="sxs-lookup"><span data-stu-id="e97d5-120">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="e97d5-121">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="e97d5-121">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="e97d5-122">Powoduje przeniesienie zestawu zasobów uwzględnionych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="e97d5-122">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="e97d5-123">Operacja przenoszenia jest wyzwalana, gdy moveResources znajduje się w moveState "MovePending" lub "MoveFailed", po poprawnym wykonaniu moveResource moveState, aby przejść do CommitPending.</span><span class="sxs-lookup"><span data-stu-id="e97d5-123">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="e97d5-124">Aby pomóc użytkownikowi na wstępną konieczność działania, z którym klient może nawiązać operację, należy ustawić właściwość validateOnly równą true.</span><span class="sxs-lookup"><span data-stu-id="e97d5-124">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="e97d5-125">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="e97d5-125">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="e97d5-126">Inicjuje przygotowanie zestawu zasobów uwzględnionych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="e97d5-126">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="e97d5-127">Operacja przygotowywania znajduje się na moveResourcesie, który znajduje się w moveState "PreparePending" lub "PrepareFailed", po poprawnym wykonaniu moveResource moveState to przejście do MovePending.</span><span class="sxs-lookup"><span data-stu-id="e97d5-127">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="e97d5-128">Aby pomóc użytkownikowi na wstępną konieczność działania, z którym klient może nawiązać operację, należy ustawić właściwość validateOnly równą true.</span><span class="sxs-lookup"><span data-stu-id="e97d5-128">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="e97d5-129">Nowe — AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="e97d5-129">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="e97d5-130">Tworzy lub aktualizuje kolekcję Przenieś.</span><span class="sxs-lookup"><span data-stu-id="e97d5-130">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="e97d5-131">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="e97d5-131">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="e97d5-132">Usuwa kolekcję Przenieś.</span><span class="sxs-lookup"><span data-stu-id="e97d5-132">Deletes a move collection.</span></span>

### [<span data-ttu-id="e97d5-133">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="e97d5-133">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="e97d5-134">Usuwa zasób Przenieś z kolekcji Move.</span><span class="sxs-lookup"><span data-stu-id="e97d5-134">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="e97d5-135">Rozpoznaj — AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="e97d5-135">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="e97d5-136">Oblicza, rozpoznaje i sprawdza poprawność zależności moveResources w kolekcji Move.</span><span class="sxs-lookup"><span data-stu-id="e97d5-136">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

