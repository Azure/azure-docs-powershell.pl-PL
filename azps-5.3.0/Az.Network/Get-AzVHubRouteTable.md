---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
ms.openlocfilehash: 3461d629eac47a1bbf2842d2cb0a913c2734f94e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503596"
---
# <span data-ttu-id="b5fd9-101">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5fd9-101">Get-AzVHubRouteTable</span></span>

## <span data-ttu-id="b5fd9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="b5fd9-103">Pobiera zasób tabeli tras centrum skojarzony z VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="b5fd9-103">Retrieves  a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="b5fd9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5fd9-104">SYNTAX</span></span>

### <span data-ttu-id="b5fd9-105">ByVHubRouteTableName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b5fd9-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Get-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5fd9-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="b5fd9-106">ByVirtualHubObject</span></span>
```powershell
Get-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5fd9-107">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="b5fd9-107">ByVHubRouteTableResourceId</span></span>
```powershell
Get-AzVHubRouteTable -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5fd9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b5fd9-108">DESCRIPTION</span></span>
<span data-ttu-id="b5fd9-109">Pobiera określoną tabelę tras centrum, która jest skojarzona z określonym koncentratorem wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="b5fd9-109">Gets the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="b5fd9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5fd9-110">EXAMPLES</span></span>

### <span data-ttu-id="b5fd9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b5fd9-111">Example 1</span></span>

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
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

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

<span data-ttu-id="b5fd9-112">To polecenie umożliwia wyświetlenie tabeli routingu centrum wirtualnego centrum.</span><span class="sxs-lookup"><span data-stu-id="b5fd9-112">This command gets the hub route table of the virtual hub.</span></span>

### <span data-ttu-id="b5fd9-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b5fd9-113">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName


Name                   : defaultRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []


Name                   : noneRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="b5fd9-114">To polecenie wyświetla listę wszystkich tabel tras centrum w określonym VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="b5fd9-114">This command lists all the hub route tables in the specified VirtualHub.</span></span>

## <span data-ttu-id="b5fd9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5fd9-115">PARAMETERS</span></span>

### <span data-ttu-id="b5fd9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5fd9-116">-AsJob</span></span>
<span data-ttu-id="b5fd9-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b5fd9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5fd9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5fd9-118">-DefaultProfile</span></span>
<span data-ttu-id="b5fd9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5fd9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5fd9-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b5fd9-120">-Name</span></span>
<span data-ttu-id="b5fd9-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b5fd9-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fd9-122">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="b5fd9-122">-ParentObject</span></span>
<span data-ttu-id="b5fd9-123">Nadrzędny wirtualny obiekt piasta tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="b5fd9-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="b5fd9-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="b5fd9-124">-ParentResourceName</span></span>
<span data-ttu-id="b5fd9-125">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="b5fd9-125">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fd9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5fd9-126">-ResourceGroupName</span></span>
<span data-ttu-id="b5fd9-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b5fd9-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fd9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5fd9-128">-ResourceId</span></span>
<span data-ttu-id="b5fd9-129">Identyfikator zasobu vhubroutetable do pobrania.</span><span class="sxs-lookup"><span data-stu-id="b5fd9-129">The resource id of the vhubroutetable resource to Get.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5fd9-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5fd9-130">-Confirm</span></span>
<span data-ttu-id="b5fd9-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5fd9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5fd9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5fd9-132">-WhatIf</span></span>
<span data-ttu-id="b5fd9-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5fd9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5fd9-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b5fd9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5fd9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5fd9-135">CommonParameters</span></span>
<span data-ttu-id="b5fd9-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5fd9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5fd9-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5fd9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5fd9-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5fd9-138">INPUTS</span></span>

### <span data-ttu-id="b5fd9-139">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b5fd9-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="b5fd9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b5fd9-140">System.String</span></span>

## <span data-ttu-id="b5fd9-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5fd9-141">OUTPUTS</span></span>

### <span data-ttu-id="b5fd9-142">Microsoft. Azure. Commands. Network. models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5fd9-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="b5fd9-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5fd9-143">NOTES</span></span>

## <span data-ttu-id="b5fd9-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5fd9-144">RELATED LINKS</span></span>

[<span data-ttu-id="b5fd9-145">Nowe — AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="b5fd9-145">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="b5fd9-146">Nowe — AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5fd9-146">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="b5fd9-147">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5fd9-147">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)

[<span data-ttu-id="b5fd9-148">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5fd9-148">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)