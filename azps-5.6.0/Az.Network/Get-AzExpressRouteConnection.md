---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
ms.openlocfilehash: 4665e67b64baa87273c365137cc2247e86efd2c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991026"
---
# <span data-ttu-id="770da-101">Get-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="770da-101">Get-AzExpressRouteConnection</span></span>

## <span data-ttu-id="770da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="770da-102">SYNOPSIS</span></span>
<span data-ttu-id="770da-103">Pobiera połączenie z usługą ExpressRoute według nazwy lub wyświetla wszystkie połączenia z usługą ExpressRoute połączone z bramą expressroute.</span><span class="sxs-lookup"><span data-stu-id="770da-103">Gets a ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="770da-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="770da-104">SYNTAX</span></span>

### <span data-ttu-id="770da-105">ByExpressRouteGatewayName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="770da-105">ByExpressRouteGatewayName (Default)</span></span>
```
Get-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770da-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="770da-106">ByExpressRouteGatewayObject</span></span>
```
Get-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770da-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="770da-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="770da-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="770da-108">DESCRIPTION</span></span>
<span data-ttu-id="770da-109">Pobiera połączenie z usługą ExpressRoute według nazwy lub zawiera listę wszystkich połączeń z usługą ExpressRoute połączonych z bramą expressRoute.</span><span class="sxs-lookup"><span data-stu-id="770da-109">Gets an ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="770da-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="770da-110">EXAMPLES</span></span>

### <span data-ttu-id="770da-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="770da-111">Example 1</span></span>

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
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
EnableInternetSecurity             : False
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

<span data-ttu-id="770da-112">Powyższe utworzy grupę zasobów, wirtualną sieć WAN, sieć wirtualną, centrum wirtualne i usługę ExpressRouteSite w Zachód w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="770da-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="770da-113">Brama usługi ExpressRoute zostanie utworzona w centrum wirtualnym z 2 jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="770da-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="770da-114">Po utworzeniu brama jest połączona z lokalnym obwodem usługi ExpressRoute przy użyciu New-AzExpressRouteConnection usługi.</span><span class="sxs-lookup"><span data-stu-id="770da-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="770da-115">Połączenie zostanie na nim nawiązaniu przy użyciu nazwy połączenia.</span><span class="sxs-lookup"><span data-stu-id="770da-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="770da-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="770da-116">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName ps9361 -ParentResourceName testExpressRoutegw -Name test*

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection1
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection1
EnableInternetSecurity             : False
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

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection2
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection2
EnableInternetSecurity             : False
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

<span data-ttu-id="770da-117">To polecenie spowoduje uruchomienie wszystkich połączeń w uście ExpressRoute "testExpressRoutegw", które zaczynają się od "test"</span><span class="sxs-lookup"><span data-stu-id="770da-117">This command will get all Connections in ExpressRoute "testExpressRoutegw" that start with "test"</span></span>

## <span data-ttu-id="770da-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="770da-118">PARAMETERS</span></span>

### <span data-ttu-id="770da-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770da-119">-DefaultProfile</span></span>
<span data-ttu-id="770da-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="770da-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="770da-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="770da-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="770da-122">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="770da-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770da-123">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="770da-123">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="770da-124">Nadrzędna brama expressroute dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="770da-124">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="770da-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="770da-125">-Name</span></span>
<span data-ttu-id="770da-126">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="770da-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="770da-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="770da-127">-ParentResourceId</span></span>
<span data-ttu-id="770da-128">Identyfikator zasobu nadrzędnej aplikacji ExpressRouteGateway dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="770da-128">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="770da-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="770da-129">-ResourceGroupName</span></span>
<span data-ttu-id="770da-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="770da-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770da-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770da-131">CommonParameters</span></span>
<span data-ttu-id="770da-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="770da-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770da-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="770da-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770da-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="770da-134">INPUTS</span></span>

### <span data-ttu-id="770da-135">System.String</span><span class="sxs-lookup"><span data-stu-id="770da-135">System.String</span></span>

## <span data-ttu-id="770da-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="770da-136">OUTPUTS</span></span>

### <span data-ttu-id="770da-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="770da-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="770da-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="770da-138">NOTES</span></span>

## <span data-ttu-id="770da-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="770da-139">RELATED LINKS</span></span>
