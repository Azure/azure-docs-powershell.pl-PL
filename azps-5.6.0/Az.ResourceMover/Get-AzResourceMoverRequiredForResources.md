---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemoverrequiredforresources
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverRequiredForResources.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverRequiredForResources.md
ms.openlocfilehash: 9aa09de52a6b731fbf57b309fb605c0ba07325da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000010"
---
# <span data-ttu-id="b1df7-101">Get-AzResourceMoverRequiredForResources</span><span class="sxs-lookup"><span data-stu-id="b1df7-101">Get-AzResourceMoverRequiredForResources</span></span>

## <span data-ttu-id="b1df7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1df7-102">SYNOPSIS</span></span>
<span data-ttu-id="b1df7-103">Lista zasobów przenoszenia, dla których jest wymagany zasób arm.</span><span class="sxs-lookup"><span data-stu-id="b1df7-103">List of the move resources for which an arm resource is required for.</span></span>

## <span data-ttu-id="b1df7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b1df7-104">SYNTAX</span></span>

```
Get-AzResourceMoverRequiredForResources -MoveCollectionName <String> -ResourceGroupName <String>
 -SourceId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b1df7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b1df7-105">DESCRIPTION</span></span>
<span data-ttu-id="b1df7-106">Lista zasobów przenoszenia, dla których jest wymagany zasób arm.</span><span class="sxs-lookup"><span data-stu-id="b1df7-106">List of the move resources for which an arm resource is required for.</span></span>

## <span data-ttu-id="b1df7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b1df7-107">EXAMPLES</span></span>

### <span data-ttu-id="b1df7-108">Przykład 1. Uzyskaj listę wymaganych identyfikatorów ZAOSZCZĘDÓW ZASOBÓW, które muszą zostać dodane, aby dodać określony zasób.</span><span class="sxs-lookup"><span data-stu-id="b1df7-108">Example 1: Get a list of required resource ARMIDs that are required to be added, to add the specified resource.</span></span>
```powershell
PS C:\> Get-AzResourceMoverRequiredForResources -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -SourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups"

/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="b1df7-109">Uzyskaj listę wymaganych identyfikatorów DVD zasobów, które muszą zostać dodane, aby dodać określony zasób.</span><span class="sxs-lookup"><span data-stu-id="b1df7-109">Get a list of required resource ARMIDs that are required to be added, to add the specified resource.</span></span>

## <span data-ttu-id="b1df7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1df7-110">PARAMETERS</span></span>

### <span data-ttu-id="b1df7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1df7-111">-DefaultProfile</span></span>
<span data-ttu-id="b1df7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1df7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1df7-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="b1df7-113">-MoveCollectionName</span></span>
<span data-ttu-id="b1df7-114">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="b1df7-114">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1df7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1df7-115">-ResourceGroupName</span></span>
<span data-ttu-id="b1df7-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b1df7-116">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1df7-117">-SourceId</span><span class="sxs-lookup"><span data-stu-id="b1df7-117">-SourceId</span></span>
<span data-ttu-id="b1df7-118">The sourceId for which the api is invoked.</span><span class="sxs-lookup"><span data-stu-id="b1df7-118">The sourceId for which the api is invoked.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1df7-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1df7-119">-SubscriptionId</span></span>
<span data-ttu-id="b1df7-120">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b1df7-120">The Subscription ID.</span></span>

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

### <span data-ttu-id="b1df7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1df7-121">CommonParameters</span></span>
<span data-ttu-id="b1df7-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1df7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1df7-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1df7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1df7-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1df7-124">INPUTS</span></span>

## <span data-ttu-id="b1df7-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1df7-125">OUTPUTS</span></span>

### <span data-ttu-id="b1df7-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b1df7-126">System.String</span></span>

## <span data-ttu-id="b1df7-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b1df7-127">NOTES</span></span>

<span data-ttu-id="b1df7-128">ALIASY</span><span class="sxs-lookup"><span data-stu-id="b1df7-128">ALIASES</span></span>

## <span data-ttu-id="b1df7-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1df7-129">RELATED LINKS</span></span>

