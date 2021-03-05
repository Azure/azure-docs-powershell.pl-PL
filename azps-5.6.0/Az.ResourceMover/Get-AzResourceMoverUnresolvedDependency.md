---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 34cae1bcc6020e2e0c2a8b2f6b70e302c8576f2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999994"
---
# <span data-ttu-id="8b794-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="8b794-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="8b794-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b794-102">SYNOPSIS</span></span>
<span data-ttu-id="8b794-103">Pobiera listę nierozpoznanych zależności.</span><span class="sxs-lookup"><span data-stu-id="8b794-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="8b794-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8b794-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DependencyLevel <DependencyLevel>] [-Filter <String>] [-Orderby <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8b794-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8b794-105">DESCRIPTION</span></span>
<span data-ttu-id="8b794-106">Pobiera listę nierozpoznanych zależności.</span><span class="sxs-lookup"><span data-stu-id="8b794-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="8b794-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8b794-107">EXAMPLES</span></span>

### <span data-ttu-id="8b794-108">Przykład 1. Uzyskiwanie listy nierozpoznanych zasobów zależnych dla kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="8b794-108">Example 1: Get list of unresolved dependent resources for a Move Collection.</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -DependencyLevel Descendant
Count Id                                                                                                                                        
----- --                                                                                                                                        
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111   
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet     
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
    3 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm
```

<span data-ttu-id="8b794-109">Pobierz listę nierozpoznanych zasobów zależnych dla kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="8b794-109">Get a list of unresolved dependent resources for a Move Collection.</span></span>

## <span data-ttu-id="8b794-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b794-110">PARAMETERS</span></span>

### <span data-ttu-id="8b794-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b794-111">-DefaultProfile</span></span>
<span data-ttu-id="8b794-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b794-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b794-113">-DependencyLevel</span><span class="sxs-lookup"><span data-stu-id="8b794-113">-DependencyLevel</span></span>
<span data-ttu-id="8b794-114">Definiuje poziom zależności.</span><span class="sxs-lookup"><span data-stu-id="8b794-114">Defines the dependency level.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.DependencyLevel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b794-115">— Filtr</span><span class="sxs-lookup"><span data-stu-id="8b794-115">-Filter</span></span>
<span data-ttu-id="8b794-116">Filtr, który ma być stosować do operacji.</span><span class="sxs-lookup"><span data-stu-id="8b794-116">The filter to apply on the operation.</span></span>
<span data-ttu-id="8b794-117">Na przykład: $apply=filter(count eq 2).</span><span class="sxs-lookup"><span data-stu-id="8b794-117">For example, $apply=filter(count eq 2).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b794-118">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="8b794-118">-MoveCollectionName</span></span>
<span data-ttu-id="8b794-119">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="8b794-119">The Move Collection Name.</span></span>

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

### <span data-ttu-id="8b794-120">- Orderby</span><span class="sxs-lookup"><span data-stu-id="8b794-120">-Orderby</span></span>
<span data-ttu-id="8b794-121">Opcja kolejności danych OData według kwerendy.</span><span class="sxs-lookup"><span data-stu-id="8b794-121">OData order by query option.</span></span>
<span data-ttu-id="8b794-122">Można na przykład użyć funkcji $orderby=Licznik.</span><span class="sxs-lookup"><span data-stu-id="8b794-122">For example, you can use $orderby=Count desc.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b794-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b794-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b794-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8b794-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="8b794-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b794-125">-SubscriptionId</span></span>
<span data-ttu-id="8b794-126">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8b794-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="8b794-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b794-127">CommonParameters</span></span>
<span data-ttu-id="8b794-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b794-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b794-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b794-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b794-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b794-130">INPUTS</span></span>

## <span data-ttu-id="8b794-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b794-131">OUTPUTS</span></span>

### <span data-ttu-id="8b794-132">Microsoft.Azure.PowerShell.Cmdlet.ResourceMover.Models.Api202101.IUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="8b794-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IUnresolvedDependency</span></span>

## <span data-ttu-id="8b794-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8b794-133">NOTES</span></span>

<span data-ttu-id="8b794-134">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8b794-134">ALIASES</span></span>

## <span data-ttu-id="8b794-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b794-135">RELATED LINKS</span></span>

