---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
ms.openlocfilehash: b3b4fe711cbccd195f4549ae936fe438185c9070
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951594"
---
# <span data-ttu-id="79c72-101">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="79c72-101">Update-AzVHubRouteTable</span></span>

## <span data-ttu-id="79c72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79c72-102">SYNOPSIS</span></span>
<span data-ttu-id="79c72-103">Usuwanie zasobu tabeli trasy centrum skojarzonego z usługą VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="79c72-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="79c72-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="79c72-104">SYNTAX</span></span>

### <span data-ttu-id="79c72-105">ByVHubRouteTableName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="79c72-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Update-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String>[-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79c72-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="79c72-106">ByVirtualHubObject</span></span>
```powershell
Update-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79c72-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="79c72-107">ByVHubRouteTableObject</span></span>
```powershell
Update-AzVHubRouteTable -InputObject <PSVHubRouteTable> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79c72-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="79c72-108">ByVHubRouteTableResourceId</span></span>
```powershell
Update-AzVHubRouteTable -ResourceId <String> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79c72-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="79c72-109">DESCRIPTION</span></span>
<span data-ttu-id="79c72-110">Aktualizuje określoną tabelę trasy skojarzoną z określonym centrum wirtualnym z podanymi trasami lub etykietami.</span><span class="sxs-lookup"><span data-stu-id="79c72-110">Updates the specified route table that is associated with the specified virtual hub with the provided routes or the labels.</span></span>

## <span data-ttu-id="79c72-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="79c72-111">EXAMPLES</span></span>

### <span data-ttu-id="79c72-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79c72-112">Example 1</span></span>
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

<span data-ttu-id="79c72-113">To polecenie usuwa tabelę trasy centrum w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="79c72-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="79c72-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79c72-114">PARAMETERS</span></span>

### <span data-ttu-id="79c72-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="79c72-115">-AsJob</span></span>
<span data-ttu-id="79c72-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="79c72-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79c72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c72-117">-DefaultProfile</span></span>
<span data-ttu-id="79c72-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="79c72-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79c72-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79c72-119">-InputObject</span></span>
<span data-ttu-id="79c72-120">Zasób, który można zaktualizować.</span><span class="sxs-lookup"><span data-stu-id="79c72-120">The vhubroutetable resource to Update.</span></span>

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

### <span data-ttu-id="79c72-121">— Label</span><span class="sxs-lookup"><span data-stu-id="79c72-121">-Label</span></span>
<span data-ttu-id="79c72-122">Lista etykiet.</span><span class="sxs-lookup"><span data-stu-id="79c72-122">The list of labels.</span></span>

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

### <span data-ttu-id="79c72-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="79c72-123">-Name</span></span>
<span data-ttu-id="79c72-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="79c72-124">The resource name.</span></span>

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

### <span data-ttu-id="79c72-125">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="79c72-125">-ParentObject</span></span>
<span data-ttu-id="79c72-126">Obiekt nadrzędnego centrum wirtualnego tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="79c72-126">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="79c72-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="79c72-127">-ParentResourceName</span></span>
<span data-ttu-id="79c72-128">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="79c72-128">The parent resource name.</span></span>

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

### <span data-ttu-id="79c72-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79c72-129">-ResourceGroupName</span></span>
<span data-ttu-id="79c72-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="79c72-130">The resource group name.</span></span>

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

### <span data-ttu-id="79c72-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79c72-131">-ResourceId</span></span>
<span data-ttu-id="79c72-132">Identyfikator zasobu, który można zaktualizować.</span><span class="sxs-lookup"><span data-stu-id="79c72-132">The resource id of the vhubroutetable resource to Update.</span></span>

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

### <span data-ttu-id="79c72-133">— Trasuj</span><span class="sxs-lookup"><span data-stu-id="79c72-133">-Route</span></span>
<span data-ttu-id="79c72-134">Lista tras dla tej tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="79c72-134">The list of routes for this route table.</span></span>

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

### <span data-ttu-id="79c72-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79c72-135">-Confirm</span></span>
<span data-ttu-id="79c72-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="79c72-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79c72-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79c72-137">-WhatIf</span></span>
<span data-ttu-id="79c72-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79c72-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79c72-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="79c72-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79c72-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c72-140">CommonParameters</span></span>
<span data-ttu-id="79c72-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c72-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c72-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79c72-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c72-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79c72-143">INPUTS</span></span>

### <span data-ttu-id="79c72-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="79c72-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="79c72-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="79c72-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="79c72-146">System.String</span><span class="sxs-lookup"><span data-stu-id="79c72-146">System.String</span></span>

## <span data-ttu-id="79c72-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79c72-147">OUTPUTS</span></span>

### <span data-ttu-id="79c72-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="79c72-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="79c72-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="79c72-149">NOTES</span></span>

## <span data-ttu-id="79c72-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79c72-150">RELATED LINKS</span></span>

[<span data-ttu-id="79c72-151">Get-AzvHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="79c72-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="79c72-152">New-AzvHubRoute</span><span class="sxs-lookup"><span data-stu-id="79c72-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="79c72-153">New-AzvHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="79c72-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="79c72-154">Remove-AzvHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="79c72-154">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)