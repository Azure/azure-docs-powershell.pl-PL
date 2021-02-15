---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: a6308120303684a8e87280ef903056361fbaf848
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238900"
---
# <span data-ttu-id="1efb4-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="1efb4-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="1efb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1efb4-102">SYNOPSIS</span></span>
<span data-ttu-id="1efb4-103">Uzyskiwanie lub lista zasobów grup położenia odległości.</span><span class="sxs-lookup"><span data-stu-id="1efb4-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="1efb4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1efb4-104">SYNTAX</span></span>

### <span data-ttu-id="1efb4-105">DefaultParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="1efb4-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-ColocationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1efb4-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="1efb4-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ColocationStatus] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1efb4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1efb4-107">DESCRIPTION</span></span>
<span data-ttu-id="1efb4-108">To polecenie cmdlet pobierze lub na liście zasób grup położenie odległości.</span><span class="sxs-lookup"><span data-stu-id="1efb4-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="1efb4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1efb4-109">EXAMPLES</span></span>

### <span data-ttu-id="1efb4-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1efb4-110">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
VirtualMachines             : {}
VirtualMachineScaleSets     : {}
AvailabilitySets            : {}
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {[key1, val1]}
```

<span data-ttu-id="1efb4-111">To polecenie pobiera grupę położenia odległości</span><span class="sxs-lookup"><span data-stu-id="1efb4-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="1efb4-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1efb4-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="1efb4-113">To polecenie zawiera listę wszystkich grup położenia odległości w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="1efb4-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="1efb4-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="1efb4-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="1efb4-115">To polecenie zawiera listę wszystkich grup położenia odległości w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1efb4-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="1efb4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1efb4-116">PARAMETERS</span></span>

### <span data-ttu-id="1efb4-117">-ColocationStatus</span><span class="sxs-lookup"><span data-stu-id="1efb4-117">-ColocationStatus</span></span>
<span data-ttu-id="1efb4-118">Pokazuje stan kolokacji zasobu w grupie położenia odległości.</span><span class="sxs-lookup"><span data-stu-id="1efb4-118">Shows the colocation status of a resource in the proximity placement group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1efb4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1efb4-119">-DefaultProfile</span></span>
<span data-ttu-id="1efb4-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1efb4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1efb4-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1efb4-121">-Name</span></span>
<span data-ttu-id="1efb4-122">Nazwa grupy położenia odległości.</span><span class="sxs-lookup"><span data-stu-id="1efb4-122">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1efb4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1efb4-123">-ResourceGroupName</span></span>
<span data-ttu-id="1efb4-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1efb4-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1efb4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1efb4-125">-ResourceId</span></span>
<span data-ttu-id="1efb4-126">Identyfikator zasobu dla grupy położenia odległości.</span><span class="sxs-lookup"><span data-stu-id="1efb4-126">The resource id for the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1efb4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1efb4-127">CommonParameters</span></span>
<span data-ttu-id="1efb4-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1efb4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1efb4-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1efb4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1efb4-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1efb4-130">INPUTS</span></span>

### <span data-ttu-id="1efb4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1efb4-131">System.String</span></span>

## <span data-ttu-id="1efb4-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1efb4-132">OUTPUTS</span></span>

### <span data-ttu-id="1efb4-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="1efb4-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="1efb4-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1efb4-134">NOTES</span></span>

## <span data-ttu-id="1efb4-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1efb4-135">RELATED LINKS</span></span>
