---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
ms.openlocfilehash: 1e2156b955f4b7a98f6c8886ea538f77cee7fe34
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050305"
---
# <span data-ttu-id="8e7e2-101">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="8e7e2-101">Set-AzExpressRouteConnection</span></span>

## <span data-ttu-id="8e7e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e7e2-102">SYNOPSIS</span></span>
<span data-ttu-id="8e7e2-103">Aktualizuje połączenie Express Route utworzone między routerem w usłudze Express Route a bramą lokalną w ramach obwodowej trasy Express.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-103">Updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="8e7e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e7e2-104">SYNTAX</span></span>

### <span data-ttu-id="8e7e2-105">ByExpressRouteConnectionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8e7e2-105">ByExpressRouteConnectionName (Default)</span></span>
```
Set-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e7e2-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="8e7e2-106">ByExpressRouteConnectionResourceId</span></span>
```
Set-AzExpressRouteConnection -ResourceId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e7e2-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="8e7e2-107">ByExpressRouteConnectionObject</span></span>
```
Set-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-AuthorizationKey <String>]
 [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e7e2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8e7e2-108">DESCRIPTION</span></span>
<span data-ttu-id="8e7e2-109">Polecenie cmdlet **Set-AzExpressRouteConnection** aktualizuje połączenie Express Route utworzone między obsługą komunikacji bezpośredniej bramy usługi Express Route i lokalnego obwodu trasy Express.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-109">The **Set-AzExpressRouteConnection** cmdlet updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="8e7e2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e7e2-110">EXAMPLES</span></span>

### <span data-ttu-id="8e7e2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8e7e2-111">Example 1</span></span>

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
PS C:\> Set-AzExpressRouteConnection -InputObject $ExpressRouteConnection -RoutingWeight 30

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 30
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
```

<span data-ttu-id="8e7e2-112">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum i ExpressRouteSite w zachodnim obszarze "testRG" w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="8e7e2-113">Brama ExpressRoute zostanie utworzona później w koncentratorze wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="8e7e2-114">Po utworzeniu bramy jest on połączony z równorzędnym obwodem ExpressRoute, korzystając z polecenia New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit peering using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="8e7e2-115">Po zaktualizowaniu połączenie będzie miało inne RoutingWeight, korzystając z polecenia Set-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-115">The connection is then updated to have a different RoutingWeight by using the Set-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="8e7e2-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e7e2-116">PARAMETERS</span></span>

### <span data-ttu-id="8e7e2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e7e2-117">-AsJob</span></span>
<span data-ttu-id="8e7e2-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8e7e2-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e7e2-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="8e7e2-119">-AuthorizationKey</span></span>
<span data-ttu-id="8e7e2-120">Klucz autoryzacji, który ma zostać wykorzystany do utworzenia połączenia bramy usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-120">The authorization key to be used to create the ExpressRoute gateway connection.</span></span>

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

### <span data-ttu-id="8e7e2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e7e2-121">-DefaultProfile</span></span>
<span data-ttu-id="8e7e2-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e7e2-123">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8e7e2-123">-EnableInternetSecurity</span></span>
<span data-ttu-id="8e7e2-124">Włącz zabezpieczenia internetowe dla tego połączenia bramy ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="8e7e2-124">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="8e7e2-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="8e7e2-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="8e7e2-126">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-126">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7e2-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8e7e2-127">-InputObject</span></span>
<span data-ttu-id="8e7e2-128">Obiekt ExpressRouteConnection do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-128">The ExpressRouteConnection object to update.</span></span>

```yaml
Type: PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7e2-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8e7e2-129">-Name</span></span>
<span data-ttu-id="8e7e2-130">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7e2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e7e2-131">-ResourceGroupName</span></span>
<span data-ttu-id="8e7e2-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7e2-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e7e2-133">-ResourceId</span></span>
<span data-ttu-id="8e7e2-134">Identyfikator zasobu obiektu ExpressRouteConnection, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-134">The resource id of the ExpressRouteConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7e2-135">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="8e7e2-135">-RoutingWeight</span></span>
<span data-ttu-id="8e7e2-136">Waga, która musi być przypisana do tego połączenia dla routingu pakietów.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-136">The weight that needs to be assigned to this connection for packet routing.</span></span>

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

### <span data-ttu-id="8e7e2-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8e7e2-137">-Confirm</span></span>
<span data-ttu-id="8e7e2-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e7e2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e7e2-139">-WhatIf</span></span>
<span data-ttu-id="8e7e2-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e7e2-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e7e2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7e2-142">CommonParameters</span></span>
<span data-ttu-id="8e7e2-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e7e2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7e2-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e7e2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7e2-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e7e2-145">INPUTS</span></span>

### <span data-ttu-id="8e7e2-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8e7e2-146">System.String</span></span>

### <span data-ttu-id="8e7e2-147">Microsoft. Azure. Commands. Network. models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="8e7e2-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="8e7e2-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e7e2-148">OUTPUTS</span></span>

### <span data-ttu-id="8e7e2-149">Microsoft. Azure. Commands. Network. models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="8e7e2-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="8e7e2-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e7e2-150">NOTES</span></span>

## <span data-ttu-id="8e7e2-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e7e2-151">RELATED LINKS</span></span>
