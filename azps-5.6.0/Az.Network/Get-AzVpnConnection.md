---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
ms.openlocfilehash: 51a4d6e2325685b81c01ce58c667412e209a8074
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964218"
---
# <span data-ttu-id="35659-101">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="35659-101">Get-AzVpnConnection</span></span>

## <span data-ttu-id="35659-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35659-102">SYNOPSIS</span></span>
<span data-ttu-id="35659-103">Łączy się z siecią VPN według nazwy lub zawiera listę wszystkich połączeń vpn połączonych z bramą VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="35659-103">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="35659-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="35659-104">SYNTAX</span></span>

### <span data-ttu-id="35659-105">ByVpnGatewayName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="35659-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35659-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="35659-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnConnection -ParentObject <PSVpnGateway> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35659-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="35659-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnConnection -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35659-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="35659-108">DESCRIPTION</span></span>
<span data-ttu-id="35659-109">Łączy się z siecią VPN według nazwy lub zawiera listę wszystkich połączeń vpn połączonych z bramą VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="35659-109">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="35659-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="35659-110">EXAMPLES</span></span>

### <span data-ttu-id="35659-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="35659-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
RoutingConfiguration      : {
                                "AssociatedRouteTable": {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                }
                                "PropagatedRouteTables": {
                                    "Labels": [],
                                    "Ids": [
                                    {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                                },
                                "VnetRoutes": {
                                    "StaticRoutes": []
                                }
                            }
```

<span data-ttu-id="35659-112">Powyższe spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego i witryny VpnSite w Zachód w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="35659-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="35659-113">Brama VPN zostanie utworzona w centrum wirtualnym z 2 jednostkami skalowania.</span><span class="sxs-lookup"><span data-stu-id="35659-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="35659-114">Po utworzeniu brama jest połączona z lokacją VpnSite za pomocą New-AzVpnConnection sieci.</span><span class="sxs-lookup"><span data-stu-id="35659-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="35659-115">Połączenie zostanie na nim nawiązaniu przy użyciu nazwy połączenia.</span><span class="sxs-lookup"><span data-stu-id="35659-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="35659-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="35659-116">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnConnection -ResourceGroupName ps9361 -ParentResourceName testvpngw -Name test*

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection1
RoutingConfiguration      : {
                                "AssociatedRouteTable": {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                }
                                "PropagatedRouteTables": {
                                    "Labels": [],
                                    "Ids": [
                                    {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                                },
                                "VnetRoutes": {
                                    "StaticRoutes": []
                                }
                            }

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection2
RoutingConfiguration      : {
                                "AssociatedRouteTable": {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                }
                                "PropagatedRouteTables": {
                                    "Labels": [],
                                    "Ids": [
                                    {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                                },
                                "VnetRoutes": {
                                    "StaticRoutes": []
                                }
                            }
```

<span data-ttu-id="35659-117">To polecenie cmdlet pobiera wszystkie połączenia, które zaczynają się od "testu".</span><span class="sxs-lookup"><span data-stu-id="35659-117">This cmdlet gets all connections that start with "test".</span></span>

## <span data-ttu-id="35659-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35659-118">PARAMETERS</span></span>

### <span data-ttu-id="35659-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35659-119">-DefaultProfile</span></span>
<span data-ttu-id="35659-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="35659-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35659-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="35659-121">-Name</span></span>
<span data-ttu-id="35659-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="35659-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35659-123">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="35659-123">-ParentObject</span></span>
<span data-ttu-id="35659-124">Nadrzędna aplikacja VpnGateway dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="35659-124">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35659-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="35659-125">-ParentResourceId</span></span>
<span data-ttu-id="35659-126">Identyfikator zasobu nadrzędnej aplikacji VpnGateway dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="35659-126">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35659-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="35659-127">-ParentResourceName</span></span>
<span data-ttu-id="35659-128">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="35659-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35659-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35659-129">-ResourceGroupName</span></span>
<span data-ttu-id="35659-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="35659-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35659-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35659-131">CommonParameters</span></span>
<span data-ttu-id="35659-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35659-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35659-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35659-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35659-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35659-134">INPUTS</span></span>

### <span data-ttu-id="35659-135">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="35659-135">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="35659-136">System.String</span><span class="sxs-lookup"><span data-stu-id="35659-136">System.String</span></span>

## <span data-ttu-id="35659-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35659-137">OUTPUTS</span></span>

### <span data-ttu-id="35659-138">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="35659-138">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="35659-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="35659-139">NOTES</span></span>

## <span data-ttu-id="35659-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35659-140">RELATED LINKS</span></span>

[<span data-ttu-id="35659-141">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="35659-141">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="35659-142">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="35659-142">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="35659-143">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="35659-143">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
