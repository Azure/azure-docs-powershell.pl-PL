---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
ms.openlocfilehash: 3461d629eac47a1bbf2842d2cb0a913c2734f94e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203062"
---
# <span data-ttu-id="d1892-101">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d1892-101">Get-AzVHubRouteTable</span></span>

## <span data-ttu-id="d1892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1892-102">SYNOPSIS</span></span>
<span data-ttu-id="d1892-103">Pobiera zasób tabeli trasy centrum skojarzonego z usługą VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="d1892-103">Retrieves  a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="d1892-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d1892-104">SYNTAX</span></span>

### <span data-ttu-id="d1892-105">ByVHubRouteTableName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d1892-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Get-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1892-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="d1892-106">ByVirtualHubObject</span></span>
```powershell
Get-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1892-107">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="d1892-107">ByVHubRouteTableResourceId</span></span>
```powershell
Get-AzVHubRouteTable -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1892-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d1892-108">DESCRIPTION</span></span>
<span data-ttu-id="d1892-109">Pobiera tabelę określonej trasy centrum skojarzonej z określonym centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="d1892-109">Gets the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="d1892-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d1892-110">EXAMPLES</span></span>

### <span data-ttu-id="d1892-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d1892-111">Example 1</span></span>

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

<span data-ttu-id="d1892-112">To polecenie pobiera tabelę tras centrum w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="d1892-112">This command gets the hub route table of the virtual hub.</span></span>

### <span data-ttu-id="d1892-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d1892-113">Example 2</span></span>

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

<span data-ttu-id="d1892-114">To polecenie wyświetla listę wszystkich tabel tras centrum w określonej aplikacji VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="d1892-114">This command lists all the hub route tables in the specified VirtualHub.</span></span>

## <span data-ttu-id="d1892-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1892-115">PARAMETERS</span></span>

### <span data-ttu-id="d1892-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d1892-116">-AsJob</span></span>
<span data-ttu-id="d1892-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d1892-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1892-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1892-118">-DefaultProfile</span></span>
<span data-ttu-id="d1892-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1892-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1892-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d1892-120">-Name</span></span>
<span data-ttu-id="d1892-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="d1892-121">The resource name.</span></span>

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

### <span data-ttu-id="d1892-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="d1892-122">-ParentObject</span></span>
<span data-ttu-id="d1892-123">Nadrzędny obiekt centrum wirtualnego tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="d1892-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="d1892-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="d1892-124">-ParentResourceName</span></span>
<span data-ttu-id="d1892-125">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="d1892-125">The parent resource name.</span></span>

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

### <span data-ttu-id="d1892-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1892-126">-ResourceGroupName</span></span>
<span data-ttu-id="d1892-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d1892-127">The resource group name.</span></span>

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

### <span data-ttu-id="d1892-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1892-128">-ResourceId</span></span>
<span data-ttu-id="d1892-129">Identyfikator zasobu, który można pobrać.</span><span class="sxs-lookup"><span data-stu-id="d1892-129">The resource id of the vhubroutetable resource to Get.</span></span>

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

### <span data-ttu-id="d1892-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1892-130">-Confirm</span></span>
<span data-ttu-id="d1892-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d1892-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1892-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1892-132">-WhatIf</span></span>
<span data-ttu-id="d1892-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1892-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1892-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d1892-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1892-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1892-135">CommonParameters</span></span>
<span data-ttu-id="d1892-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1892-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1892-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1892-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1892-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1892-138">INPUTS</span></span>

### <span data-ttu-id="d1892-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d1892-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="d1892-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d1892-140">System.String</span></span>

## <span data-ttu-id="d1892-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1892-141">OUTPUTS</span></span>

### <span data-ttu-id="d1892-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d1892-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="d1892-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d1892-143">NOTES</span></span>

## <span data-ttu-id="d1892-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1892-144">RELATED LINKS</span></span>

[<span data-ttu-id="d1892-145">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="d1892-145">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="d1892-146">New-AzvHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d1892-146">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="d1892-147">Update-AzvHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d1892-147">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)

[<span data-ttu-id="d1892-148">Remove-AzvHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d1892-148">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)