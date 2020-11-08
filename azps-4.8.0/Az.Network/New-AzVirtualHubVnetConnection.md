---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e9156887f328242f8c4896dc707a1814f58f2869
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223327"
---
# <span data-ttu-id="4976d-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4976d-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="4976d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4976d-102">SYNOPSIS</span></span>
<span data-ttu-id="4976d-103">Polecenie cmdlet New-AzVirtualHubVnetConnection tworzy zasób HubVirtualNetworkConnection, który jest równorzędny siecią wirtualną do wirtualnego centrum usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="4976d-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="4976d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4976d-104">SYNTAX</span></span>

### <span data-ttu-id="4976d-105">ByVirtualHubNameByRemoteVirtualNetworkObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4976d-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4976d-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="4976d-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4976d-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="4976d-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4976d-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="4976d-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4976d-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="4976d-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4976d-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="4976d-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4976d-111">Opis</span><span class="sxs-lookup"><span data-stu-id="4976d-111">DESCRIPTION</span></span>
<span data-ttu-id="4976d-112">Polecenie cmdlet New-AzVirtualHubVnetConnection tworzy zasób HubVirtualNetworkConnection, który jest równorzędny siecią wirtualną do wirtualnego centrum usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="4976d-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="4976d-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4976d-113">EXAMPLES</span></span>

### <span data-ttu-id="4976d-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4976d-114">Example 1</span></span>

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

<span data-ttu-id="4976d-115">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN, sieć wirtualną, wirtualny koncentrator w centrum centrali w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="4976d-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="4976d-116">Następnie zostanie utworzone połączenie z siecią wirtualną, które będzie węzłem wirtualnym sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4976d-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="4976d-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4976d-117">Example 2</span></span>

<span data-ttu-id="4976d-118">Polecenie cmdlet New-AzVirtualHubVnetConnection tworzy zasób HubVirtualNetworkConnection, który jest równorzędny siecią wirtualną do wirtualnego centrum usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="4976d-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="4976d-119">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="4976d-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```

## <span data-ttu-id="4976d-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4976d-120">PARAMETERS</span></span>

### <span data-ttu-id="4976d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4976d-121">-AsJob</span></span>
<span data-ttu-id="4976d-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4976d-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4976d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4976d-123">-DefaultProfile</span></span>
<span data-ttu-id="4976d-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4976d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4976d-125">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="4976d-125">-EnableInternetSecurity</span></span>
<span data-ttu-id="4976d-126">Włączanie zabezpieczeń internetowych dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="4976d-126">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="4976d-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="4976d-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="4976d-128">Włączanie zabezpieczeń internetowych dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="4976d-128">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="4976d-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4976d-129">-Name</span></span>
<span data-ttu-id="4976d-130">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="4976d-130">The resource name.</span></span>

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

### <span data-ttu-id="4976d-131">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="4976d-131">-ParentObject</span></span>
<span data-ttu-id="4976d-132">Zasób nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="4976d-132">The parent resource.</span></span>

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

### <span data-ttu-id="4976d-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4976d-133">-ParentResourceId</span></span>
<span data-ttu-id="4976d-134">Zasób nadrzędny.</span><span class="sxs-lookup"><span data-stu-id="4976d-134">The parent resource.</span></span>

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

### <span data-ttu-id="4976d-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="4976d-135">-ParentResourceName</span></span>
<span data-ttu-id="4976d-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4976d-136">The resource group name.</span></span>

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

### <span data-ttu-id="4976d-137">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4976d-137">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="4976d-138">Zdalna Sieć wirtualna, do której jest podłączone połączenie z siecią wirtualną centrum.</span><span class="sxs-lookup"><span data-stu-id="4976d-138">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="4976d-139">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="4976d-139">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="4976d-140">Zdalna Sieć wirtualna, do której jest podłączone połączenie z siecią wirtualną centrum.</span><span class="sxs-lookup"><span data-stu-id="4976d-140">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="4976d-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4976d-141">-ResourceGroupName</span></span>
<span data-ttu-id="4976d-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4976d-142">The resource group name.</span></span>

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

### <span data-ttu-id="4976d-143">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="4976d-143">-RoutingConfiguration</span></span>
<span data-ttu-id="4976d-144">Konfiguracja routingu dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="4976d-144">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="4976d-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4976d-145">-Confirm</span></span>
<span data-ttu-id="4976d-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4976d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4976d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4976d-147">-WhatIf</span></span>
<span data-ttu-id="4976d-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4976d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4976d-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4976d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4976d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4976d-150">CommonParameters</span></span>
<span data-ttu-id="4976d-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4976d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4976d-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4976d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4976d-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4976d-153">INPUTS</span></span>

### <span data-ttu-id="4976d-154">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4976d-154">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="4976d-155">System. String</span><span class="sxs-lookup"><span data-stu-id="4976d-155">System.String</span></span>

## <span data-ttu-id="4976d-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4976d-156">OUTPUTS</span></span>

### <span data-ttu-id="4976d-157">Microsoft. Azure. Commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="4976d-157">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="4976d-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4976d-158">NOTES</span></span>

## <span data-ttu-id="4976d-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4976d-159">RELATED LINKS</span></span>

[<span data-ttu-id="4976d-160">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4976d-160">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="4976d-161">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4976d-161">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="4976d-162">Nowe — AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="4976d-162">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
