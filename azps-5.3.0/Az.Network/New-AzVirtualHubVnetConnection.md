---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: f4087782e247e574cd49634e148b6852e9fb8dc6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501236"
---
# <span data-ttu-id="73bf6-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="73bf6-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="73bf6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="73bf6-103">Polecenie cmdlet New-AzVirtualHubVnetConnection tworzy zasób HubVirtualNetworkConnection, który jest równorzędny siecią wirtualną do wirtualnego centrum usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="73bf6-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="73bf6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73bf6-104">SYNTAX</span></span>

### <span data-ttu-id="73bf6-105">ByVirtualHubNameByRemoteVirtualNetworkObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="73bf6-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73bf6-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="73bf6-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73bf6-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="73bf6-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73bf6-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="73bf6-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73bf6-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="73bf6-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73bf6-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="73bf6-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73bf6-111">Opis</span><span class="sxs-lookup"><span data-stu-id="73bf6-111">DESCRIPTION</span></span>
<span data-ttu-id="73bf6-112">Polecenie cmdlet New-AzVirtualHubVnetConnection tworzy zasób HubVirtualNetworkConnection, który jest równorzędny siecią wirtualną do wirtualnego centrum usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="73bf6-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="73bf6-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73bf6-113">EXAMPLES</span></span>

### <span data-ttu-id="73bf6-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="73bf6-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : False
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

<span data-ttu-id="73bf6-115">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN, sieć wirtualną, wirtualny koncentrator w centrum centrali w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="73bf6-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="73bf6-116">Następnie zostanie utworzone połączenie z siecią wirtualną, które będzie węzłem wirtualnym sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="73bf6-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="73bf6-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="73bf6-117">Example 2</span></span>

<span data-ttu-id="73bf6-118">Polecenie cmdlet New-AzVirtualHubVnetConnection tworzy zasób HubVirtualNetworkConnection, który jest równorzędny siecią wirtualną do wirtualnego centrum usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="73bf6-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="73bf6-119">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="73bf6-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```


### <span data-ttu-id="73bf6-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="73bf6-120">Example 3</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName $rgName -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> $routingconfig = New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

AssociatedRouteTable  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable"
PropagatedRouteTables : {
                          "Labels": [
                            "testLabel"
                          ],
                          "Ids": [
                            {
                              "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "route1",
                              "AddressPrefixes": [
                                "10.20.0.0/16",
                                "10.30.0.0/16"
                              ],
                              "NextHopIpAddress": "10.90.0.5"
                            }
                          ]
                        }
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork -RoutingConfiguration $routingconfig
```
<span data-ttu-id="73bf6-121">Powyższy sposób spowoduje utworzenie nowej konfiguracji routingu i utworzenie tras statycznych w konfiguracji routingu z następnym przeskokiem w określonym adresie IP.</span><span class="sxs-lookup"><span data-stu-id="73bf6-121">The above will create a new routing configuration and create static routes in the routing config with the next hop as a specified IP address.</span></span> <span data-ttu-id="73bf6-122">Taka konfiguracja routingu może zostać przekazana do polecenia New-AzVirtualHubVnetConnection jako parametr-RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="73bf6-122">This routing configuration can then be passed into  the New-AzVirtualHubVnetConnection command as the parameter -RoutingConfiguration.</span></span>

## <span data-ttu-id="73bf6-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73bf6-123">PARAMETERS</span></span>

### <span data-ttu-id="73bf6-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73bf6-124">-AsJob</span></span>
<span data-ttu-id="73bf6-125">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="73bf6-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73bf6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73bf6-126">-DefaultProfile</span></span>
<span data-ttu-id="73bf6-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="73bf6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73bf6-128">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="73bf6-128">-EnableInternetSecurity</span></span>
<span data-ttu-id="73bf6-129">Włączanie zabezpieczeń internetowych dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="73bf6-129">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="73bf6-130">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="73bf6-130">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="73bf6-131">Włączanie zabezpieczeń internetowych dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="73bf6-131">Enable internet security for this connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73bf6-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="73bf6-132">-Name</span></span>
<span data-ttu-id="73bf6-133">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="73bf6-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73bf6-134">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="73bf6-134">-ParentObject</span></span>
<span data-ttu-id="73bf6-135">Zasób nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="73bf6-135">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73bf6-136">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="73bf6-136">-ParentResourceId</span></span>
<span data-ttu-id="73bf6-137">Zasób nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="73bf6-137">The parent resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73bf6-138">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="73bf6-138">-ParentResourceName</span></span>
<span data-ttu-id="73bf6-139">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="73bf6-139">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73bf6-140">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="73bf6-140">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="73bf6-141">Zdalna Sieć wirtualna, do której jest podłączone połączenie z siecią wirtualną centrum.</span><span class="sxs-lookup"><span data-stu-id="73bf6-141">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73bf6-142">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="73bf6-142">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="73bf6-143">Zdalna Sieć wirtualna, do której jest podłączone połączenie z siecią wirtualną centrum.</span><span class="sxs-lookup"><span data-stu-id="73bf6-143">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73bf6-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73bf6-144">-ResourceGroupName</span></span>
<span data-ttu-id="73bf6-145">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="73bf6-145">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73bf6-146">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="73bf6-146">-RoutingConfiguration</span></span>
<span data-ttu-id="73bf6-147">Konfiguracja routingu dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="73bf6-147">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="73bf6-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="73bf6-148">-Confirm</span></span>
<span data-ttu-id="73bf6-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73bf6-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73bf6-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73bf6-150">-WhatIf</span></span>
<span data-ttu-id="73bf6-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73bf6-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73bf6-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="73bf6-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73bf6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73bf6-153">CommonParameters</span></span>
<span data-ttu-id="73bf6-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73bf6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73bf6-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73bf6-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73bf6-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73bf6-156">INPUTS</span></span>

### <span data-ttu-id="73bf6-157">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="73bf6-157">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="73bf6-158">System. String</span><span class="sxs-lookup"><span data-stu-id="73bf6-158">System.String</span></span>

## <span data-ttu-id="73bf6-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73bf6-159">OUTPUTS</span></span>

### <span data-ttu-id="73bf6-160">Microsoft. Azure. Commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="73bf6-160">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="73bf6-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73bf6-161">NOTES</span></span>

## <span data-ttu-id="73bf6-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73bf6-162">RELATED LINKS</span></span>

[<span data-ttu-id="73bf6-163">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="73bf6-163">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="73bf6-164">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="73bf6-164">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="73bf6-165">Nowe — AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="73bf6-165">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
