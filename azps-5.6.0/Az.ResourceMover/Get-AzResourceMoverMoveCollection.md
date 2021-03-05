---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: a10ac77515b225c5e5ef06335f9cee1e99ecd3b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000042"
---
# <span data-ttu-id="340bb-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="340bb-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="340bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="340bb-102">SYNOPSIS</span></span>
<span data-ttu-id="340bb-103">Pobiera kolekcję przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="340bb-103">Gets the move collection.</span></span>

## <span data-ttu-id="340bb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="340bb-104">SYNTAX</span></span>

### <span data-ttu-id="340bb-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="340bb-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="340bb-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="340bb-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="340bb-107">Lista1</span><span class="sxs-lookup"><span data-stu-id="340bb-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="340bb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="340bb-108">DESCRIPTION</span></span>
<span data-ttu-id="340bb-109">Pobiera kolekcję przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="340bb-109">Gets the move collection.</span></span>

## <span data-ttu-id="340bb-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="340bb-110">EXAMPLES</span></span>

### <span data-ttu-id="340bb-111">Przykład 1. Uzyskaj szczegółowe informacje o wszystkich kolekcjach przenieś w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="340bb-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"270119e0-0000-0c00-0000-5f5c94940000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"39015ed4-0000-0c00-0000-5f5ce2760000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections
"1000b505-0000-0c00-0000-5f69db6e0000" centraluseuap MoveCollection-cus-eus-ccy         Microsoft.Migrate/moveCollections


```

<span data-ttu-id="340bb-112">Uzyskaj szczegółowe informacje o wszystkich kolekcjach przenieś w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="340bb-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="340bb-113">Przykład 2. Uzyskiwanie szczegółów kolekcji Move z określoną nazwą kolekcji przenoszenia w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="340bb-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -Name "PS-centralus-westcentralus-demoRMS"

Etag                                   Location      Name                               Type                             
----                                   --------      ----                               ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS Microsoft.Migrate/moveCollections

```

<span data-ttu-id="340bb-114">Uzyskaj szczegóły kolekcji Move z określoną nazwą kolekcji przenoszenia w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="340bb-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="340bb-115">Przykład 3. Uzyskiwanie szczegółów kolekcji Przenoszenie z określoną nazwą grupy zasobów w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="340bb-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"4e02b0a9-0000-0c00-0000-5fd101cc0000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections

```

<span data-ttu-id="340bb-116">Uzyskaj szczegóły kolekcji przenoszenia z określoną nazwą grupy zasobów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="340bb-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="340bb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="340bb-117">PARAMETERS</span></span>

### <span data-ttu-id="340bb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="340bb-118">-DefaultProfile</span></span>
<span data-ttu-id="340bb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="340bb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="340bb-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="340bb-120">-Name</span></span>
<span data-ttu-id="340bb-121">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="340bb-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="340bb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="340bb-122">-ResourceGroupName</span></span>
<span data-ttu-id="340bb-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="340bb-123">The Resource Group Name.</span></span>

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

### <span data-ttu-id="340bb-124">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="340bb-124">-SubscriptionId</span></span>
<span data-ttu-id="340bb-125">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="340bb-125">The Subscription ID.</span></span>

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

### <span data-ttu-id="340bb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="340bb-126">CommonParameters</span></span>
<span data-ttu-id="340bb-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="340bb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="340bb-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="340bb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="340bb-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="340bb-129">INPUTS</span></span>

## <span data-ttu-id="340bb-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="340bb-130">OUTPUTS</span></span>

### <span data-ttu-id="340bb-131">Microsoft.Azure.PowerShell.cmdlet.ResourceMover.Models.Api202101.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="340bb-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span></span>

## <span data-ttu-id="340bb-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="340bb-132">NOTES</span></span>

<span data-ttu-id="340bb-133">ALIASY</span><span class="sxs-lookup"><span data-stu-id="340bb-133">ALIASES</span></span>

## <span data-ttu-id="340bb-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="340bb-134">RELATED LINKS</span></span>

