---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
ms.openlocfilehash: d330b7e25cc1184a3efaea2c3deb569bf44171b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223011"
---
# <span data-ttu-id="65504-101">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="65504-101">Update-AzVHubRouteTable</span></span>

## <span data-ttu-id="65504-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65504-102">SYNOPSIS</span></span>
<span data-ttu-id="65504-103">Usuń zasób tabeli tras centrum skojarzony z VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="65504-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="65504-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65504-104">SYNTAX</span></span>

### <span data-ttu-id="65504-105">ByVHubRouteTableName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="65504-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Update-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String>[-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65504-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="65504-106">ByVirtualHubObject</span></span>
```powershell
Update-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65504-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="65504-107">ByVHubRouteTableObject</span></span>
```powershell
Update-AzVHubRouteTable -InputObject <PSVHubRouteTable> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65504-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="65504-108">ByVHubRouteTableResourceId</span></span>
```powershell
Update-AzVHubRouteTable -ResourceId <String> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65504-109">Opis</span><span class="sxs-lookup"><span data-stu-id="65504-109">DESCRIPTION</span></span>
<span data-ttu-id="65504-110">Aktualizuje określoną tabelę tras skojarzoną z określonym koncentratorem wirtualnym przy użyciu dostarczonych tras lub etykiet.</span><span class="sxs-lookup"><span data-stu-id="65504-110">Updates the specified route table that is associated with the specified virtual hub with the provided routes or the labels.</span></span>

## <span data-ttu-id="65504-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65504-111">EXAMPLES</span></span>

### <span data-ttu-id="65504-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="65504-112">Example 1</span></span>
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

PS C:\> $route2 = New-AzVHubRoute -Name "internet-traffic" -Destination @("0.0.0.0/0") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> Update-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route2)
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "internet-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "0.0.0.0/0"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="65504-113">To polecenie powoduje usunięcie tabeli routingu centrum wirtualnego centrum.</span><span class="sxs-lookup"><span data-stu-id="65504-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="65504-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65504-114">PARAMETERS</span></span>

### <span data-ttu-id="65504-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65504-115">-AsJob</span></span>
<span data-ttu-id="65504-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="65504-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65504-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65504-117">-DefaultProfile</span></span>
<span data-ttu-id="65504-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65504-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65504-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="65504-119">-InputObject</span></span>
<span data-ttu-id="65504-120">Zasób vhubroutetable do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="65504-120">The vhubroutetable resource to Update.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65504-121">-Label</span><span class="sxs-lookup"><span data-stu-id="65504-121">-Label</span></span>
<span data-ttu-id="65504-122">Lista etykiet.</span><span class="sxs-lookup"><span data-stu-id="65504-122">The list of labels.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65504-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="65504-123">-Name</span></span>
<span data-ttu-id="65504-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="65504-124">The resource name.</span></span>

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

### <span data-ttu-id="65504-125">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="65504-125">-ParentObject</span></span>
<span data-ttu-id="65504-126">Nadrzędny wirtualny obiekt piasta tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="65504-126">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="65504-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="65504-127">-ParentResourceName</span></span>
<span data-ttu-id="65504-128">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="65504-128">The parent resource name.</span></span>

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

### <span data-ttu-id="65504-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65504-129">-ResourceGroupName</span></span>
<span data-ttu-id="65504-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="65504-130">The resource group name.</span></span>

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

### <span data-ttu-id="65504-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65504-131">-ResourceId</span></span>
<span data-ttu-id="65504-132">Identyfikator zasobu zasobu vhubroutetable, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="65504-132">The resource id of the vhubroutetable resource to Update.</span></span>

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

### <span data-ttu-id="65504-133">-Route</span><span class="sxs-lookup"><span data-stu-id="65504-133">-Route</span></span>
<span data-ttu-id="65504-134">Lista tras dla tej tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="65504-134">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65504-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65504-135">-Confirm</span></span>
<span data-ttu-id="65504-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65504-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65504-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65504-137">-WhatIf</span></span>
<span data-ttu-id="65504-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65504-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65504-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="65504-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65504-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65504-140">CommonParameters</span></span>
<span data-ttu-id="65504-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65504-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65504-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65504-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65504-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65504-143">INPUTS</span></span>

### <span data-ttu-id="65504-144">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="65504-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="65504-145">Microsoft. Azure. Commands. Network. models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="65504-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="65504-146">System. String</span><span class="sxs-lookup"><span data-stu-id="65504-146">System.String</span></span>

## <span data-ttu-id="65504-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65504-147">OUTPUTS</span></span>

### <span data-ttu-id="65504-148">Microsoft. Azure. Commands. Network. models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="65504-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="65504-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65504-149">NOTES</span></span>

## <span data-ttu-id="65504-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65504-150">RELATED LINKS</span></span>

[<span data-ttu-id="65504-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="65504-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="65504-152">Nowe — AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="65504-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="65504-153">Nowe — AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="65504-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="65504-154">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="65504-154">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)