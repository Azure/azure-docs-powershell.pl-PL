---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
ms.openlocfilehash: c5de4de61a1a0d2aeb14d8a360500b928a28fdcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011905"
---
# <span data-ttu-id="4c736-101">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4c736-101">Get-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="4c736-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c736-102">SYNOPSIS</span></span>
<span data-ttu-id="4c736-103">Pobiera połączenie sieci wirtualnej w centrum wirtualnym lub wyświetla wszystkie wirtualne połączenia sieciowe w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="4c736-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="4c736-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4c736-104">SYNTAX</span></span>

### <span data-ttu-id="4c736-105">ByVirtualHubName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="4c736-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c736-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="4c736-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c736-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="4c736-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c736-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4c736-108">DESCRIPTION</span></span>
<span data-ttu-id="4c736-109">Pobiera połączenie sieci wirtualnej w centrum wirtualnym lub wyświetla wszystkie wirtualne połączenia sieciowe w centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="4c736-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="4c736-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4c736-110">EXAMPLES</span></span>

### <span data-ttu-id="4c736-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4c736-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
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

<span data-ttu-id="4c736-112">Powyższe spowoduje utworzenie grupy zasobów, Virtual WAN, Virtual Network, Virtual Hub w centrum centralnym Stanów Zjednoczonych w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="4c736-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="4c736-113">Po tym czasie zostanie utworzone połączenie sieci wirtualnej, które będzie równorzędne dla sieci wirtualnej z centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="4c736-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="4c736-114">Po utworzeniu połączenia sieci wirtualnej centrum otrzymuje ono połączenie z siecią wirtualną centrum przy użyciu nazwy grupy zasobów, nazwy centrum i nazwy połączenia.</span><span class="sxs-lookup"><span data-stu-id="4c736-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="4c736-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4c736-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
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

<span data-ttu-id="4c736-116">Powyższe spowoduje utworzenie grupy zasobów, Virtual WAN, Virtual Network, Virtual Hub w centrum centralnym Stanów Zjednoczonych w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="4c736-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="4c736-117">Po tym czasie zostanie utworzone połączenie sieci wirtualnej, które będzie równorzędne dla sieci wirtualnej z centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="4c736-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="4c736-118">Po utworzeniu połączenia sieci wirtualnej centrum wyświetla ono listę wszystkich połączeń sieci wirtualnej centrum przy użyciu nazwy grupy zasobów i nazwy centrum.</span><span class="sxs-lookup"><span data-stu-id="4c736-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

### <span data-ttu-id="4c736-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4c736-119">Example 3</span></span>

```powershell
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name test*

Name                 : testvnetconnection1
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection1
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
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

Name                 : testvnetconnection2
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection2
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
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

<span data-ttu-id="4c736-120">To polecenie cmdlet wyświetla listę wszystkich połączeń sieci wirtualnej centrum, rozpoczynając od "testu" przy użyciu nazwy grupy zasobów i nazwy centrum.</span><span class="sxs-lookup"><span data-stu-id="4c736-120">This cmdlet lists all the hub virtual network connections starting with "test" using its resource group name and the hub name.</span></span>

## <span data-ttu-id="4c736-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c736-121">PARAMETERS</span></span>

### <span data-ttu-id="4c736-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c736-122">-DefaultProfile</span></span>
<span data-ttu-id="4c736-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c736-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c736-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4c736-124">-Name</span></span>
<span data-ttu-id="4c736-125">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="4c736-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="4c736-126">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="4c736-126">-ParentObject</span></span>
<span data-ttu-id="4c736-127">Zasób nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="4c736-127">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c736-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4c736-128">-ParentResourceId</span></span>
<span data-ttu-id="4c736-129">Identyfikator zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="4c736-129">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c736-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="4c736-130">-ParentResourceName</span></span>
<span data-ttu-id="4c736-131">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="4c736-131">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c736-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c736-132">-ResourceGroupName</span></span>
<span data-ttu-id="4c736-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4c736-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c736-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c736-134">CommonParameters</span></span>
<span data-ttu-id="4c736-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c736-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c736-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c736-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c736-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c736-137">INPUTS</span></span>

### <span data-ttu-id="4c736-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4c736-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="4c736-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4c736-139">System.String</span></span>

## <span data-ttu-id="4c736-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c736-140">OUTPUTS</span></span>

### <span data-ttu-id="4c736-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="4c736-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="4c736-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4c736-142">NOTES</span></span>

## <span data-ttu-id="4c736-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c736-143">RELATED LINKS</span></span>

[<span data-ttu-id="4c736-144">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4c736-144">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="4c736-145">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4c736-145">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
