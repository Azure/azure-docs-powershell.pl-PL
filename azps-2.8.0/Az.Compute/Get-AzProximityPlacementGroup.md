---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: 9ec2760ba50d4ed97ebf36f5bab7c02d110d77ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706434"
---
# <span data-ttu-id="e71e4-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e71e4-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="e71e4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e71e4-102">SYNOPSIS</span></span>
<span data-ttu-id="e71e4-103">Uzyskiwanie lub wyświetlanie listy zasobów grupy położenia zbliżeniowe.</span><span class="sxs-lookup"><span data-stu-id="e71e4-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="e71e4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e71e4-104">SYNTAX</span></span>

### <span data-ttu-id="e71e4-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e71e4-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e71e4-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e71e4-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e71e4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e71e4-107">DESCRIPTION</span></span>
<span data-ttu-id="e71e4-108">To polecenie cmdlet otrzyma lub wyświetla listę zasobów grupy położenia w pobliżu.</span><span class="sxs-lookup"><span data-stu-id="e71e4-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="e71e4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e71e4-109">EXAMPLES</span></span>

### <span data-ttu-id="e71e4-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e71e4-110">Example 1</span></span>
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

<span data-ttu-id="e71e4-111">To polecenie pobiera grupę położenia zbliżeniowe</span><span class="sxs-lookup"><span data-stu-id="e71e4-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="e71e4-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e71e4-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="e71e4-113">To polecenie powoduje wyświetlenie listy wszystkich grup rozłożeń w danej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e71e4-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="e71e4-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e71e4-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="e71e4-115">To polecenie wyświetla listę wszystkich grup rozłożeń w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e71e4-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="e71e4-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e71e4-116">PARAMETERS</span></span>

### <span data-ttu-id="e71e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e71e4-117">-DefaultProfile</span></span>
<span data-ttu-id="e71e4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e71e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e71e4-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e71e4-119">-Name</span></span>
<span data-ttu-id="e71e4-120">Nazwa grupy położenia zbliżeniowe.</span><span class="sxs-lookup"><span data-stu-id="e71e4-120">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="e71e4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e71e4-121">-ResourceGroupName</span></span>
<span data-ttu-id="e71e4-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e71e4-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="e71e4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e71e4-123">-ResourceId</span></span>
<span data-ttu-id="e71e4-124">Identyfikator zasobu dla grupy rozmieszczenia zbliżeniowe.</span><span class="sxs-lookup"><span data-stu-id="e71e4-124">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="e71e4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e71e4-125">CommonParameters</span></span>
<span data-ttu-id="e71e4-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e71e4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e71e4-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e71e4-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e71e4-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e71e4-128">INPUTS</span></span>

### <span data-ttu-id="e71e4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e71e4-129">System.String</span></span>

## <span data-ttu-id="e71e4-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e71e4-130">OUTPUTS</span></span>

### <span data-ttu-id="e71e4-131">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e71e4-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="e71e4-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e71e4-132">NOTES</span></span>

## <span data-ttu-id="e71e4-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e71e4-133">RELATED LINKS</span></span>
