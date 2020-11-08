---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 565e79420821e8d8764b5e461e33d275247ddb3c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233008"
---
# <span data-ttu-id="a1248-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a1248-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="a1248-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1248-102">SYNOPSIS</span></span>
<span data-ttu-id="a1248-103">Tworzy połączenie ExpressRoute, które łączy bramę ExpressRoute z lokalną obwódem ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="a1248-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="a1248-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1248-104">SYNTAX</span></span>

### <span data-ttu-id="a1248-105">ByExpressRouteGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a1248-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1248-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a1248-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1248-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="a1248-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1248-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a1248-108">DESCRIPTION</span></span>
<span data-ttu-id="a1248-109">Tworzy połączenie ExpressRoute między lokalnym węzłem równorzędnym BGP a bramą ExpressRoute w koncentratorze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="a1248-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="a1248-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1248-110">EXAMPLES</span></span>

### <span data-ttu-id="a1248-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a1248-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
RoutingConfiguration               : {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                       },
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                             "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                           }
                                         ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     }
```

<span data-ttu-id="a1248-112">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum danych, bramy usługi Express Route i obwodu ExpressRoute z prywatnym współdziałaniem w Stanach Zjednoczonych w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a1248-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="a1248-113">Po utworzeniu bramy jest ona połączona z równorzędnym obwodem ExpressRoute za pomocą polecenia New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="a1248-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="a1248-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1248-114">PARAMETERS</span></span>

### <span data-ttu-id="a1248-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1248-115">-AsJob</span></span>
<span data-ttu-id="a1248-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a1248-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1248-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="a1248-117">-AuthorizationKey</span></span>
<span data-ttu-id="a1248-118">Klucz uzyskany od właściciela obwodu ExpressRoute w celu umożliwienia utworzenia połączenia z bramą w innej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a1248-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1248-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1248-119">-DefaultProfile</span></span>
<span data-ttu-id="a1248-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1248-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1248-121">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="a1248-121">-EnableInternetSecurity</span></span>
<span data-ttu-id="a1248-122">Włącz zabezpieczenia internetowe dla tego połączenia bramy ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="a1248-122">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="a1248-123">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="a1248-123">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="a1248-124">Identyfikator zasobu komunikacji równorzędnej ze obwodem usługi Express Route, do którego ma zostać utworzone połączenie w ramach bramy Express Route.</span><span class="sxs-lookup"><span data-stu-id="a1248-124">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1248-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="a1248-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="a1248-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a1248-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1248-127">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a1248-127">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="a1248-128">ExpressRouteGateway nadrzędny dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="a1248-128">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1248-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a1248-129">-Name</span></span>
<span data-ttu-id="a1248-130">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a1248-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1248-131">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a1248-131">-ParentResourceId</span></span>
<span data-ttu-id="a1248-132">Identyfikator zasobu dla ExpressRouteGateway nadrzędnego dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="a1248-132">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1248-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1248-133">-ResourceGroupName</span></span>
<span data-ttu-id="a1248-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a1248-134">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1248-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1248-135">-RoutingConfiguration</span></span>
<span data-ttu-id="a1248-136">Konfiguracja routingu dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="a1248-136">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1248-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="a1248-137">-RoutingWeight</span></span>
<span data-ttu-id="a1248-138">Waga rozsyłania pakietów, która musi być przypisana do tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="a1248-138">The weight for packet routing that needs to be assigned to this connection.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1248-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1248-139">-Confirm</span></span>
<span data-ttu-id="a1248-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1248-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1248-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1248-141">-WhatIf</span></span>
<span data-ttu-id="a1248-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1248-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1248-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a1248-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1248-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1248-144">CommonParameters</span></span>
<span data-ttu-id="a1248-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1248-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1248-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1248-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1248-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1248-147">INPUTS</span></span>

### <span data-ttu-id="a1248-148">Microsoft. Azure. Commands. Network. models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="a1248-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="a1248-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a1248-149">System.String</span></span>

## <span data-ttu-id="a1248-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1248-150">OUTPUTS</span></span>

### <span data-ttu-id="a1248-151">Microsoft. Azure. Commands. Network. models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a1248-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="a1248-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1248-152">NOTES</span></span>

## <span data-ttu-id="a1248-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1248-153">RELATED LINKS</span></span>

[<span data-ttu-id="a1248-154">Nowe — AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1248-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
