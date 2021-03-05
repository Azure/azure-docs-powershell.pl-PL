---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 78adeb351c0b18fe8ca7e3c3a2d286abe2f97400
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977841"
---
# <span data-ttu-id="15e21-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="15e21-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="15e21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15e21-102">SYNOPSIS</span></span>
<span data-ttu-id="15e21-103">Tworzy połączenie VPN typu Witryna-witryna między wirtualną bramą sieciową a urządzeniem wirtualnym VPN.</span><span class="sxs-lookup"><span data-stu-id="15e21-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="15e21-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="15e21-104">SYNTAX</span></span>

### <span data-ttu-id="15e21-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="15e21-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-SharedKey <String>]
 [-Peer <PSPeering>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] 
 [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15e21-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="15e21-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-SharedKey <String>]
 [-PeerId <String>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] [-Force]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15e21-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="15e21-107">DESCRIPTION</span></span>
<span data-ttu-id="15e21-108">Tworzy połączenie VPN typu Witryna-witryna między wirtualną bramą sieciową a urządzeniem wirtualnym VPN.</span><span class="sxs-lookup"><span data-stu-id="15e21-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="15e21-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="15e21-109">EXAMPLES</span></span>

### <span data-ttu-id="15e21-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="15e21-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="15e21-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15e21-111">PARAMETERS</span></span>

### <span data-ttu-id="15e21-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="15e21-112">-AsJob</span></span>
<span data-ttu-id="15e21-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="15e21-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15e21-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="15e21-114">-AuthorizationKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="15e21-115">-ConnectionProtocol</span></span>
<span data-ttu-id="15e21-116">Protokół połączenia bramy:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="15e21-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="15e21-117">-ConnectionType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15e21-118">-DefaultProfile</span></span>
<span data-ttu-id="15e21-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="15e21-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15e21-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="15e21-120">-EnableBgp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="15e21-121">-ExpressRouteGatewayBypass</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="15e21-122">-Force</span></span>

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

### <span data-ttu-id="15e21-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="15e21-123">-IpsecPolicies</span></span>
<span data-ttu-id="15e21-124">Lista zasad IPSec.</span><span class="sxs-lookup"><span data-stu-id="15e21-124">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-125">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="15e21-125">-LocalNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="15e21-126">-Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="15e21-127">-Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-128">— Peer</span><span class="sxs-lookup"><span data-stu-id="15e21-128">-Peer</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-129">- PeerId</span><span class="sxs-lookup"><span data-stu-id="15e21-129">-PeerId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15e21-130">-ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-131">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="15e21-131">-RoutingWeight</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-132">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="15e21-132">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="15e21-133">Limit czasu wykrywania wymarłych równorzędnych połączeń (w sekundach)</span><span class="sxs-lookup"><span data-stu-id="15e21-133">Dead Peer Detection Timeout of the connection in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-134">- ConnectionMode</span><span class="sxs-lookup"><span data-stu-id="15e21-134">-ConnectionMode</span></span>
<span data-ttu-id="15e21-135">Tryb połączenia wirtualnej bramy sieciowej</span><span class="sxs-lookup"><span data-stu-id="15e21-135">Virtual Network Gateway Connection Mode</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: Default
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-136">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="15e21-136">-SharedKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-137">— Tag</span><span class="sxs-lookup"><span data-stu-id="15e21-137">-Tag</span></span>
<span data-ttu-id="15e21-138">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="15e21-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="15e21-139">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="15e21-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-140">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="15e21-140">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="15e21-141">Lista zasad selektora ruchu.</span><span class="sxs-lookup"><span data-stu-id="15e21-141">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-142">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="15e21-142">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="15e21-143">Czy użyć funkcji PrivateIP dla tego klienta sieci VPN S2S</span><span class="sxs-lookup"><span data-stu-id="15e21-143">Whether to use PrivateIP for this S2S VPN tunnel</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-144">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="15e21-144">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="15e21-145">Używanie selektorów ruchu opartych na zasadach dla połączenia S2S</span><span class="sxs-lookup"><span data-stu-id="15e21-145">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-146">- VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="15e21-146">-VirtualNetworkGateway1</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-147">— VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="15e21-147">-VirtualNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-148">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="15e21-148">-Confirm</span></span>
<span data-ttu-id="15e21-149">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="15e21-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15e21-150">-WhatIf</span></span>
<span data-ttu-id="15e21-151">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15e21-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15e21-152">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="15e21-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15e21-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15e21-153">CommonParameters</span></span>
<span data-ttu-id="15e21-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15e21-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15e21-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15e21-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15e21-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15e21-156">INPUTS</span></span>

### <span data-ttu-id="15e21-157">System.String</span><span class="sxs-lookup"><span data-stu-id="15e21-157">System.String</span></span>

### <span data-ttu-id="15e21-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="15e21-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="15e21-159">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="15e21-159">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="15e21-160">System.Int32</span><span class="sxs-lookup"><span data-stu-id="15e21-160">System.Int32</span></span>

### <span data-ttu-id="15e21-161">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="15e21-161">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="15e21-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="15e21-162">System.Boolean</span></span>

### <span data-ttu-id="15e21-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="15e21-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="15e21-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="15e21-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="15e21-165">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span><span class="sxs-lookup"><span data-stu-id="15e21-165">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="15e21-166">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="15e21-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="15e21-167">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15e21-167">OUTPUTS</span></span>

### <span data-ttu-id="15e21-168">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="15e21-168">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="15e21-169">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="15e21-169">NOTES</span></span>

## <span data-ttu-id="15e21-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15e21-170">RELATED LINKS</span></span>

[<span data-ttu-id="15e21-171">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="15e21-171">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="15e21-172">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="15e21-172">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="15e21-173">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="15e21-173">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
