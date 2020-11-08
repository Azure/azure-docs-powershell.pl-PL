---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
ms.openlocfilehash: d9c7b4895d05b4f55ef91705062db7c200d702cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223329"
---
# <span data-ttu-id="5603a-101">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5603a-101">New-AzVHubRouteTable</span></span>

## <span data-ttu-id="5603a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5603a-102">SYNOPSIS</span></span>
<span data-ttu-id="5603a-103">Tworzy zasób tabeli routingu centrum skojarzony z VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="5603a-103">Creates a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="5603a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5603a-104">SYNTAX</span></span>

### <span data-ttu-id="5603a-105">ByVirtualHubName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5603a-105">ByVirtualHubName (Default)</span></span>

```powershell
New-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5603a-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="5603a-106">ByVirtualHubObject</span></span>

```powershell
New-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5603a-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="5603a-107">ByVirtualHubResourceId</span></span>

```powershell
New-AzVHubRouteTable -ParentResourceId <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5603a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5603a-108">DESCRIPTION</span></span>
<span data-ttu-id="5603a-109">Tworzy określoną tabelę tras skojarzoną z określonym koncentratorem wirtualnym z podanymi trasami i etykietami.</span><span class="sxs-lookup"><span data-stu-id="5603a-109">Creates the specified route table that is associated with the specified virtual hub with the provided routes and the labels.</span></span>

## <span data-ttu-id="5603a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5603a-110">EXAMPLES</span></span>

### <span data-ttu-id="5603a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5603a-111">Example 1</span></span>

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

<span data-ttu-id="5603a-112">To polecenie tworzy tabelę routingu centrum wirtualnego centrum.</span><span class="sxs-lookup"><span data-stu-id="5603a-112">This command creates a hub route table of the virtual hub.</span></span>

## <span data-ttu-id="5603a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5603a-113">PARAMETERS</span></span>

### <span data-ttu-id="5603a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5603a-114">-AsJob</span></span>
<span data-ttu-id="5603a-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5603a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5603a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5603a-116">-DefaultProfile</span></span>
<span data-ttu-id="5603a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5603a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5603a-118">-Label</span><span class="sxs-lookup"><span data-stu-id="5603a-118">-Label</span></span>
<span data-ttu-id="5603a-119">Lista etykiet.</span><span class="sxs-lookup"><span data-stu-id="5603a-119">The list of labels.</span></span>

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

### <span data-ttu-id="5603a-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5603a-120">-Name</span></span>
<span data-ttu-id="5603a-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="5603a-121">The resource name.</span></span>

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

### <span data-ttu-id="5603a-122">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="5603a-122">-ParentObject</span></span>
<span data-ttu-id="5603a-123">Nadrzędny wirtualny obiekt piasta tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="5603a-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="5603a-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="5603a-124">-ParentResourceName</span></span>
<span data-ttu-id="5603a-125">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="5603a-125">The parent resource name.</span></span>

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

### <span data-ttu-id="5603a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5603a-126">-ResourceGroupName</span></span>
<span data-ttu-id="5603a-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5603a-127">The resource group name.</span></span>

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

### <span data-ttu-id="5603a-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5603a-128">-ParentResourceId</span></span>
<span data-ttu-id="5603a-129">Identyfikator zasobu wirtualnego centrum.</span><span class="sxs-lookup"><span data-stu-id="5603a-129">The resource id of the virtual hub resource.</span></span>

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

### <span data-ttu-id="5603a-130">-Route</span><span class="sxs-lookup"><span data-stu-id="5603a-130">-Route</span></span>
<span data-ttu-id="5603a-131">Lista tras dla tej tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="5603a-131">The list of routes for this route table.</span></span>

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

### <span data-ttu-id="5603a-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5603a-132">-Confirm</span></span>
<span data-ttu-id="5603a-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5603a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5603a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5603a-134">-WhatIf</span></span>
<span data-ttu-id="5603a-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5603a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5603a-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5603a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5603a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5603a-137">CommonParameters</span></span>
<span data-ttu-id="5603a-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5603a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5603a-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5603a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5603a-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5603a-140">INPUTS</span></span>

### <span data-ttu-id="5603a-141">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5603a-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="5603a-142">Microsoft. Azure. Commands. Network. models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5603a-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="5603a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5603a-143">System.String</span></span>

## <span data-ttu-id="5603a-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5603a-144">OUTPUTS</span></span>

### <span data-ttu-id="5603a-145">Microsoft. Azure. Commands. Network. models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5603a-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="5603a-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5603a-146">NOTES</span></span>

## <span data-ttu-id="5603a-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5603a-147">RELATED LINKS</span></span>

[<span data-ttu-id="5603a-148">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5603a-148">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="5603a-149">Nowe — AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="5603a-149">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="5603a-150">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5603a-150">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="5603a-151">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5603a-151">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)
