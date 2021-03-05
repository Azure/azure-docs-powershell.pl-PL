---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
ms.openlocfilehash: 77288758af2f0f3294d8f32c92b7f687dab79a97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964145"
---
# <span data-ttu-id="c9bd8-101">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c9bd8-101">New-AzVHubRouteTable</span></span>

## <span data-ttu-id="c9bd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="c9bd8-103">Tworzy zasób tabeli trasy centrum skojarzonego z usługą VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="c9bd8-103">Creates a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="c9bd8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c9bd8-104">SYNTAX</span></span>

### <span data-ttu-id="c9bd8-105">ByVirtualHubName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c9bd8-105">ByVirtualHubName (Default)</span></span>

```powershell
New-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9bd8-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="c9bd8-106">ByVirtualHubObject</span></span>

```powershell
New-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9bd8-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="c9bd8-107">ByVirtualHubResourceId</span></span>

```powershell
New-AzVHubRouteTable -ParentResourceId <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9bd8-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c9bd8-108">DESCRIPTION</span></span>
<span data-ttu-id="c9bd8-109">Tworzy określoną tabelę trasy, która jest skojarzona z określonym centrum wirtualnym z podanymi trasami i etykietami.</span><span class="sxs-lookup"><span data-stu-id="c9bd8-109">Creates the specified route table that is associated with the specified virtual hub with the provided routes and the labels.</span></span>

## <span data-ttu-id="c9bd8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c9bd8-110">EXAMPLES</span></span>

### <span data-ttu-id="c9bd8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c9bd8-111">Example 1</span></span>

```powershell
PS C:\> New-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan" -Location "westcentralus" -VirtualWANType "Standard" -AllowVnetToVnetTraffic -AllowBranchToBranchTraffic
PS C:\> $virtualWan = Get-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan"

PS C:\> New-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub" -Location "westcentralus" -AddressPrefix "10.0.0.0/16" -VirtualWan $virtualWan
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub"

PS C:\> $fwIp = New-AzFirewallHubPublicIpAddress -Count 1
PS C:\> $hubIpAddresses = New-AzFirewallHubIpAddress -PublicIP $fwIp
PS C:\> New-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg" -Location "westcentralus" -Sku AZFW_Hub -VirtualHubId $virtualHub.Id -HubIPAddress $hubIpAddresses
PS C:\> $firewall = Get-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg"

PS C:\> $route1 = New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> New-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route1) -Label @("testLabel")

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "private-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "10.30.0.0/16",
                               "10.40.0.0/16"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="c9bd8-112">To polecenie tworzy tabelę trasy centrum w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="c9bd8-112">This command creates a hub route table of the virtual hub.</span></span>

## <span data-ttu-id="c9bd8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9bd8-113">PARAMETERS</span></span>

### <span data-ttu-id="c9bd8-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c9bd8-114">-AsJob</span></span>
<span data-ttu-id="c9bd8-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c9bd8-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9bd8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9bd8-116">-DefaultProfile</span></span>
<span data-ttu-id="c9bd8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9bd8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9bd8-118">— Label</span><span class="sxs-lookup"><span data-stu-id="c9bd8-118">-Label</span></span>
<span data-ttu-id="c9bd8-119">Lista etykiet.</span><span class="sxs-lookup"><span data-stu-id="c9bd8-119">The list of labels.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9bd8-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c9bd8-120">-Name</span></span>
<span data-ttu-id="c9bd8-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="c9bd8-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9bd8-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="c9bd8-122">-ParentObject</span></span>
<span data-ttu-id="c9bd8-123">Obiekt nadrzędnego centrum wirtualnego tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="c9bd8-123">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9bd8-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="c9bd8-124">-ParentResourceName</span></span>
<span data-ttu-id="c9bd8-125">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="c9bd8-125">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9bd8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9bd8-126">-ResourceGroupName</span></span>
<span data-ttu-id="c9bd8-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c9bd8-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9bd8-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c9bd8-128">-ParentResourceId</span></span>
<span data-ttu-id="c9bd8-129">Identyfikator zasobu zasobu wirtualnego centrum.</span><span class="sxs-lookup"><span data-stu-id="c9bd8-129">The resource id of the virtual hub resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9bd8-130">— Trasuj</span><span class="sxs-lookup"><span data-stu-id="c9bd8-130">-Route</span></span>
<span data-ttu-id="c9bd8-131">Lista tras dla tej tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="c9bd8-131">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9bd8-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9bd8-132">-Confirm</span></span>
<span data-ttu-id="c9bd8-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c9bd8-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9bd8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9bd8-134">-WhatIf</span></span>
<span data-ttu-id="c9bd8-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9bd8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9bd8-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c9bd8-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9bd8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9bd8-137">CommonParameters</span></span>
<span data-ttu-id="c9bd8-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9bd8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9bd8-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9bd8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9bd8-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9bd8-140">INPUTS</span></span>

### <span data-ttu-id="c9bd8-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c9bd8-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="c9bd8-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c9bd8-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="c9bd8-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c9bd8-143">System.String</span></span>

## <span data-ttu-id="c9bd8-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9bd8-144">OUTPUTS</span></span>

### <span data-ttu-id="c9bd8-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c9bd8-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="c9bd8-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c9bd8-146">NOTES</span></span>

## <span data-ttu-id="c9bd8-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9bd8-147">RELATED LINKS</span></span>

[<span data-ttu-id="c9bd8-148">Get-AzvHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c9bd8-148">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="c9bd8-149">New-AzvHubRoute</span><span class="sxs-lookup"><span data-stu-id="c9bd8-149">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="c9bd8-150">Remove-AzvHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c9bd8-150">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="c9bd8-151">Update-AzvHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c9bd8-151">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)
