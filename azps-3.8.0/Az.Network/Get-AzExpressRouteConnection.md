---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
ms.openlocfilehash: 9c1d07a8e8c02b57a67b009f0ebe438134d7d56c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052429"
---
# <span data-ttu-id="df797-101">Get-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="df797-101">Get-AzExpressRouteConnection</span></span>

## <span data-ttu-id="df797-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df797-102">SYNOPSIS</span></span>
<span data-ttu-id="df797-103">Pobiera połączenie ExpressRoute według nazwy lub wyświetla wszystkie połączenia ExpressRoute połączone z ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="df797-103">Gets a ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="df797-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df797-104">SYNTAX</span></span>

### <span data-ttu-id="df797-105">ByExpressRouteGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="df797-105">ByExpressRouteGatewayName (Default)</span></span>
```
Get-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df797-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="df797-106">ByExpressRouteGatewayObject</span></span>
```
Get-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df797-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="df797-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df797-108">Opis</span><span class="sxs-lookup"><span data-stu-id="df797-108">DESCRIPTION</span></span>
<span data-ttu-id="df797-109">Pobiera połączenie ExpressRoute według nazwy lub wyświetla wszystkie połączenia ExpressRoute połączone z ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="df797-109">Gets an ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="df797-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df797-110">EXAMPLES</span></span>

### <span data-ttu-id="df797-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="df797-111">Example 1</span></span>

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
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
```

<span data-ttu-id="df797-112">Powyższego poziomu spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, wirtualnego centrum i ExpressRouteSite w zachodnim obszarze "testRG" w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="df797-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="df797-113">Brama ExpressRoute zostanie utworzona później w koncentratorze wirtualnym z dwoma jednostkami skali.</span><span class="sxs-lookup"><span data-stu-id="df797-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="df797-114">Po utworzeniu bramy jest ona połączona z obwodem lokalnego połączenia ExpressRoute przy użyciu polecenia New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="df797-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="df797-115">Następnie zostanie nawiązać połączenie przy użyciu nazwy połączenia.</span><span class="sxs-lookup"><span data-stu-id="df797-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="df797-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="df797-116">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName ps9361 -ParentResourceName testExpressRoutegw -Name test*

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection1
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection1

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection2
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection2
```

<span data-ttu-id="df797-117">To polecenie spowoduje wyświetlenie wszystkich połączeń w ExpressRoute "testExpressRoutegw", które zaczynają się od tekstu "test"</span><span class="sxs-lookup"><span data-stu-id="df797-117">This command will get all Connections in ExpressRoute "testExpressRoutegw" that start with "test"</span></span>

## <span data-ttu-id="df797-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df797-118">PARAMETERS</span></span>

### <span data-ttu-id="df797-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df797-119">-DefaultProfile</span></span>
<span data-ttu-id="df797-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df797-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df797-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="df797-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="df797-122">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="df797-122">The parent resource name.</span></span>

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

### <span data-ttu-id="df797-123">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="df797-123">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="df797-124">ExpressRouteGateway nadrzędny dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="df797-124">The parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="df797-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="df797-125">-Name</span></span>
<span data-ttu-id="df797-126">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="df797-126">The resource name.</span></span>

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

### <span data-ttu-id="df797-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="df797-127">-ParentResourceId</span></span>
<span data-ttu-id="df797-128">Identyfikator zasobu dla ExpressRouteGateway nadrzędnego dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="df797-128">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="df797-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df797-129">-ResourceGroupName</span></span>
<span data-ttu-id="df797-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="df797-130">The resource group name.</span></span>

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

### <span data-ttu-id="df797-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df797-131">CommonParameters</span></span>
<span data-ttu-id="df797-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df797-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df797-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df797-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df797-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df797-134">INPUTS</span></span>

### <span data-ttu-id="df797-135">System. String</span><span class="sxs-lookup"><span data-stu-id="df797-135">System.String</span></span>

## <span data-ttu-id="df797-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df797-136">OUTPUTS</span></span>

### <span data-ttu-id="df797-137">Microsoft. Azure. Commands. Network. models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="df797-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="df797-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df797-138">NOTES</span></span>

## <span data-ttu-id="df797-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df797-139">RELATED LINKS</span></span>
