---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 0c07686b59f89bfee656701e14a7c938f49eeb86
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189458"
---
# <span data-ttu-id="c30b4-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="c30b4-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="c30b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c30b4-102">SYNOPSIS</span></span>
<span data-ttu-id="c30b4-103">Aktualizuje istniejącą usługę HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="c30b4-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="c30b4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c30b4-104">SYNTAX</span></span>

### <span data-ttu-id="c30b4-105">ByHubVirtualNetworkConnectionName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="c30b4-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c30b4-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="c30b4-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c30b4-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="c30b4-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c30b4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c30b4-108">DESCRIPTION</span></span>
<span data-ttu-id="c30b4-109">Aktualizuje istniejącą usługę HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="c30b4-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="c30b4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c30b4-110">EXAMPLES</span></span>

### <span data-ttu-id="c30b4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c30b4-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Update-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -EnableInternetSecurity $true
Name                   : testvnetconnection
Id                     : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : True
ProvisioningState      : Succeeded
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

<span data-ttu-id="c30b4-112">Powyższe spowoduje utworzenie grupy zasobów: Virtual WAN, Virtual Network, Virtual Hub w centrum centralnym Stanów Zjednoczonych w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="c30b4-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="c30b4-113">Jest również tworzone połączenie sieci wirtualnej, które jest równorzędne dla sieci wirtualnej z centrum wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="c30b4-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="c30b4-114">To połączenie sieci wirtualnej zostanie następnie zaktualizowane w celu włączenia zabezpieczeń internetowych.</span><span class="sxs-lookup"><span data-stu-id="c30b4-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="c30b4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c30b4-115">PARAMETERS</span></span>

### <span data-ttu-id="c30b4-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c30b4-116">-AsJob</span></span>
<span data-ttu-id="c30b4-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c30b4-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30b4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c30b4-118">-DefaultProfile</span></span>
<span data-ttu-id="c30b4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c30b4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30b4-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="c30b4-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="c30b4-121">Włącz zabezpieczenia internetowe dla tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="c30b4-121">Enable internet security for this connection.</span></span>

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

### <span data-ttu-id="c30b4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c30b4-122">-InputObject</span></span>
<span data-ttu-id="c30b4-123">Zasób hubvirtualnetworkconnection do modyfikowania.</span><span class="sxs-lookup"><span data-stu-id="c30b4-123">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c30b4-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c30b4-124">-Name</span></span>
<span data-ttu-id="c30b4-125">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="c30b4-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30b4-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="c30b4-126">-ParentResourceName</span></span>
<span data-ttu-id="c30b4-127">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="c30b4-127">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30b4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c30b4-128">-ResourceGroupName</span></span>
<span data-ttu-id="c30b4-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c30b4-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30b4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c30b4-130">-ResourceId</span></span>
<span data-ttu-id="c30b4-131">Identyfikator zasobu hubvirtualnetworkconnection do modyfikowania.</span><span class="sxs-lookup"><span data-stu-id="c30b4-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c30b4-132">- RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="c30b4-132">-RoutingConfiguration</span></span>
<span data-ttu-id="c30b4-133">Konfiguracja routingu dla tego połączenia</span><span class="sxs-lookup"><span data-stu-id="c30b4-133">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="c30b4-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c30b4-134">-Confirm</span></span>
<span data-ttu-id="c30b4-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c30b4-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30b4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c30b4-136">-WhatIf</span></span>
<span data-ttu-id="c30b4-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c30b4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c30b4-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c30b4-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30b4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c30b4-139">CommonParameters</span></span>
<span data-ttu-id="c30b4-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c30b4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c30b4-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c30b4-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c30b4-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c30b4-142">INPUTS</span></span>

### <span data-ttu-id="c30b4-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c30b4-143">System.String</span></span>

### <span data-ttu-id="c30b4-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="c30b4-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="c30b4-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c30b4-145">OUTPUTS</span></span>

### <span data-ttu-id="c30b4-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="c30b4-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="c30b4-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c30b4-147">NOTES</span></span>

## <span data-ttu-id="c30b4-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c30b4-148">RELATED LINKS</span></span>

[<span data-ttu-id="c30b4-149">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="c30b4-149">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
