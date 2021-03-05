---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 3089d3654e471bbf31eb81e42e4374525d84010d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974778"
---
# <span data-ttu-id="81d78-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="81d78-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="81d78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81d78-102">SYNOPSIS</span></span>
<span data-ttu-id="81d78-103">Tworzy połączenie usługi ExpressRoute łączące bramę usługi ExpressRoute z lokalnym obwodem usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="81d78-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="81d78-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="81d78-104">SYNTAX</span></span>

### <span data-ttu-id="81d78-105">ByExpressRouteGatewayName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="81d78-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81d78-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="81d78-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81d78-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="81d78-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81d78-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="81d78-108">DESCRIPTION</span></span>
<span data-ttu-id="81d78-109">Tworzy połączenie usługi ExpressRoute między lokalnym obwodem usługi ExpressRoute komunikacji równorzędnej BGP z bramą usługi ExpressRoute w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="81d78-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="81d78-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="81d78-110">EXAMPLES</span></span>

### <span data-ttu-id="81d78-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="81d78-111">Example 1</span></span>

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

<span data-ttu-id="81d78-112">Powyższe spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego, bramy trasy expressowej i obwodu usługi ExpressRoute z prywatną komunikacji równorzędnej w West Central US w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="81d78-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="81d78-113">Po utworzeniu brama jest połączona z obwodem usługi ExpressRoute za pomocą New-AzExpressRouteConnection komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="81d78-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="81d78-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81d78-114">PARAMETERS</span></span>

### <span data-ttu-id="81d78-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="81d78-115">-AsJob</span></span>
<span data-ttu-id="81d78-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="81d78-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81d78-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="81d78-117">-AuthorizationKey</span></span>
<span data-ttu-id="81d78-118">Klucz uzyskany od właściciela obwodu usługi ExpressRoute w celu możliwości utworzenia połączenia z bramą w innej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="81d78-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

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

### <span data-ttu-id="81d78-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d78-119">-DefaultProfile</span></span>
<span data-ttu-id="81d78-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="81d78-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81d78-121">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="81d78-121">-EnableInternetSecurity</span></span>
<span data-ttu-id="81d78-122">Włączanie zabezpieczeń internetowych dla tego połączenia bramy usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="81d78-122">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="81d78-123">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="81d78-123">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="81d78-124">Identyfikator zasobu komunikacji równorzędnej obwodu trasy expressowej, z którym ma zostać utworzone połączenie bramy trasy expressowej.</span><span class="sxs-lookup"><span data-stu-id="81d78-124">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

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

### <span data-ttu-id="81d78-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="81d78-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="81d78-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81d78-126">The resource group name.</span></span>

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

### <span data-ttu-id="81d78-127">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="81d78-127">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="81d78-128">Nadrzędna brama expressroute dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="81d78-128">The parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="81d78-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="81d78-129">-Name</span></span>
<span data-ttu-id="81d78-130">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="81d78-130">The resource name.</span></span>

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

### <span data-ttu-id="81d78-131">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="81d78-131">-ParentResourceId</span></span>
<span data-ttu-id="81d78-132">Identyfikator zasobu nadrzędnej aplikacji ExpressRouteGateway dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="81d78-132">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="81d78-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d78-133">-ResourceGroupName</span></span>
<span data-ttu-id="81d78-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81d78-134">The resource group name.</span></span>

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

### <span data-ttu-id="81d78-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="81d78-135">-RoutingConfiguration</span></span>
<span data-ttu-id="81d78-136">Konfiguracja routingu dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="81d78-136">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="81d78-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="81d78-137">-RoutingWeight</span></span>
<span data-ttu-id="81d78-138">Waga routingu pakietów, która musi zostać przypisana do tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="81d78-138">The weight for packet routing that needs to be assigned to this connection.</span></span>

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

### <span data-ttu-id="81d78-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81d78-139">-Confirm</span></span>
<span data-ttu-id="81d78-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="81d78-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81d78-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81d78-141">-WhatIf</span></span>
<span data-ttu-id="81d78-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81d78-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81d78-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="81d78-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81d78-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d78-144">CommonParameters</span></span>
<span data-ttu-id="81d78-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81d78-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d78-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81d78-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d78-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81d78-147">INPUTS</span></span>

### <span data-ttu-id="81d78-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="81d78-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="81d78-149">System.String</span><span class="sxs-lookup"><span data-stu-id="81d78-149">System.String</span></span>

## <span data-ttu-id="81d78-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81d78-150">OUTPUTS</span></span>

### <span data-ttu-id="81d78-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="81d78-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="81d78-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="81d78-152">NOTES</span></span>

## <span data-ttu-id="81d78-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81d78-153">RELATED LINKS</span></span>

[<span data-ttu-id="81d78-154">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="81d78-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
