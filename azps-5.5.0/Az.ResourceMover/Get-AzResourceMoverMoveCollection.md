---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 73bb67577a9160440c2e42e1e5b3259ad8435c5c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242610"
---
# <span data-ttu-id="54531-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="54531-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="54531-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54531-102">SYNOPSIS</span></span>
<span data-ttu-id="54531-103">Pobiera kolekcję przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="54531-103">Gets the move collection.</span></span>

## <span data-ttu-id="54531-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="54531-104">SYNTAX</span></span>

### <span data-ttu-id="54531-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="54531-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="54531-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="54531-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="54531-107">Lista1</span><span class="sxs-lookup"><span data-stu-id="54531-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="54531-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="54531-108">DESCRIPTION</span></span>
<span data-ttu-id="54531-109">Pobiera kolekcję przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="54531-109">Gets the move collection.</span></span>

## <span data-ttu-id="54531-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="54531-110">EXAMPLES</span></span>

### <span data-ttu-id="54531-111">Przykład 1. Uzyskaj szczegółowe informacje o wszystkich kolekcjach przenieś w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="54531-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId e80eb9fa-c996-4435-aa32-5af6f3d3077c

Location    Name                                            Type
--------    ----                                            ----
eastus2     mvcolle2e07001                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e34745                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e56720                                  Microsoft.Migrate/moveCollections


```

<span data-ttu-id="54531-112">Uzyskaj szczegółowe informacje o wszystkich kolekcjach przenieś w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="54531-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="54531-113">Przykład 2. Uzyskiwanie szczegółów kolekcji Move z określoną nazwą kolekcji przenoszenia w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="54531-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM -Name PS-centralus-westcentralus-demoRM

Location    Name                              Type
--------    ----                              ----
eastus2     PS-centralus-westcentralus-demoRM Microsoft.Migrate/moveCollections

```

<span data-ttu-id="54531-114">Uzyskaj szczegóły kolekcji Move z określoną nazwą kolekcji przenoszenia w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="54531-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="54531-115">Przykład 3. Uzyskiwanie szczegółów kolekcji Przenoszenie z określoną nazwą grupy zasobów w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="54531-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
eastus2euap PS-centralus-westcentralus-demoRM2 Microsoft.Migrate/moveCollections


```

<span data-ttu-id="54531-116">Uzyskaj szczegóły kolekcji przenoszenia z określoną nazwą grupy zasobów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="54531-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="54531-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54531-117">PARAMETERS</span></span>

### <span data-ttu-id="54531-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54531-118">-DefaultProfile</span></span>
<span data-ttu-id="54531-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="54531-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54531-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="54531-120">-Name</span></span>
<span data-ttu-id="54531-121">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="54531-121">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54531-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54531-122">-ResourceGroupName</span></span>
<span data-ttu-id="54531-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="54531-123">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54531-124">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54531-124">-SubscriptionId</span></span>
<span data-ttu-id="54531-125">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="54531-125">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54531-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54531-126">CommonParameters</span></span>
<span data-ttu-id="54531-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54531-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54531-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54531-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54531-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54531-129">INPUTS</span></span>

## <span data-ttu-id="54531-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54531-130">OUTPUTS</span></span>

### <span data-ttu-id="54531-131">Microsoft.Azure.PowerShell.cmdlet.ResourceMover.Models.Api20191001Preview.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="54531-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="54531-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="54531-132">NOTES</span></span>

<span data-ttu-id="54531-133">ALIASY</span><span class="sxs-lookup"><span data-stu-id="54531-133">ALIASES</span></span>

## <span data-ttu-id="54531-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54531-134">RELATED LINKS</span></span>

