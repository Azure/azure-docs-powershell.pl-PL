---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: f6dc25bc1000466d853715f62e38237ddfc76aa2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323475"
---
# <span data-ttu-id="d6435-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d6435-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="d6435-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6435-102">SYNOPSIS</span></span>
<span data-ttu-id="d6435-103">Umożliwia utworzenie połączenia VPN między lokacjami między bramą sieci wirtualnej a urządzeniem VPN na środowisku.</span><span class="sxs-lookup"><span data-stu-id="d6435-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="d6435-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6435-104">SYNTAX</span></span>

### <span data-ttu-id="d6435-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d6435-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-SharedKey <String>]
 [-Peer <PSPeering>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] 
 [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6435-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d6435-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-SharedKey <String>]
 [-PeerId <String>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] [-Force]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6435-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d6435-107">DESCRIPTION</span></span>
<span data-ttu-id="d6435-108">Umożliwia utworzenie połączenia VPN między lokacjami między bramą sieci wirtualnej a urządzeniem VPN na środowisku.</span><span class="sxs-lookup"><span data-stu-id="d6435-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="d6435-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6435-109">EXAMPLES</span></span>

### <span data-ttu-id="d6435-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d6435-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="d6435-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6435-111">PARAMETERS</span></span>

### <span data-ttu-id="d6435-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6435-112">-AsJob</span></span>
<span data-ttu-id="d6435-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d6435-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6435-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="d6435-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="d6435-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="d6435-115">-ConnectionProtocol</span></span>
<span data-ttu-id="d6435-116">Protokół połączeń z bramą: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="d6435-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="d6435-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="d6435-117">-ConnectionType</span></span>

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

### <span data-ttu-id="d6435-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6435-118">-DefaultProfile</span></span>
<span data-ttu-id="d6435-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6435-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6435-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="d6435-120">-EnableBgp</span></span>

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

### <span data-ttu-id="d6435-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="d6435-121">-ExpressRouteGatewayBypass</span></span>

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

### <span data-ttu-id="d6435-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d6435-122">-Force</span></span>

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

### <span data-ttu-id="d6435-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="d6435-123">-IpsecPolicies</span></span>
<span data-ttu-id="d6435-124">Lista zasad IPSec.</span><span class="sxs-lookup"><span data-stu-id="d6435-124">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="d6435-125">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="d6435-125">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="d6435-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d6435-126">-Location</span></span>

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

### <span data-ttu-id="d6435-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d6435-127">-Name</span></span>

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

### <span data-ttu-id="d6435-128">-Peer</span><span class="sxs-lookup"><span data-stu-id="d6435-128">-Peer</span></span>

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

### <span data-ttu-id="d6435-129">-PeerId</span><span class="sxs-lookup"><span data-stu-id="d6435-129">-PeerId</span></span>

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

### <span data-ttu-id="d6435-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6435-130">-ResourceGroupName</span></span>

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

### <span data-ttu-id="d6435-131">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="d6435-131">-RoutingWeight</span></span>

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

### <span data-ttu-id="d6435-132">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="d6435-132">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="d6435-133">Limit czasu wykrywania nieaktywnych połączeń równorzędnych połączenia w sekundach</span><span class="sxs-lookup"><span data-stu-id="d6435-133">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="d6435-134">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="d6435-134">-SharedKey</span></span>

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

### <span data-ttu-id="d6435-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="d6435-135">-Tag</span></span>
<span data-ttu-id="d6435-136">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d6435-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d6435-137">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="d6435-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d6435-138">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="d6435-138">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="d6435-139">Lista zasad wyboru ruchu.</span><span class="sxs-lookup"><span data-stu-id="d6435-139">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="d6435-140">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="d6435-140">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="d6435-141">Czy używać PrivateIP dla tego tunelu VPN S2S</span><span class="sxs-lookup"><span data-stu-id="d6435-141">Whether to use PrivateIP for this S2S VPN tunnel</span></span>

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

### <span data-ttu-id="d6435-142">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="d6435-142">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="d6435-143">Używanie selektorów ruchu opartego na zasadach dla połączenia S2S</span><span class="sxs-lookup"><span data-stu-id="d6435-143">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="d6435-144">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="d6435-144">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="d6435-145">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="d6435-145">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="d6435-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6435-146">-Confirm</span></span>
<span data-ttu-id="d6435-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6435-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6435-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6435-148">-WhatIf</span></span>
<span data-ttu-id="d6435-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6435-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6435-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d6435-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6435-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6435-151">CommonParameters</span></span>
<span data-ttu-id="d6435-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6435-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6435-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6435-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6435-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6435-154">INPUTS</span></span>

### <span data-ttu-id="d6435-155">System. String</span><span class="sxs-lookup"><span data-stu-id="d6435-155">System.String</span></span>

### <span data-ttu-id="d6435-156">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d6435-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="d6435-157">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d6435-157">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="d6435-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d6435-158">System.Int32</span></span>

### <span data-ttu-id="d6435-159">Microsoft. Azure. Commands. Network. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="d6435-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="d6435-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d6435-160">System.Boolean</span></span>

### <span data-ttu-id="d6435-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d6435-161">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d6435-162">Microsoft. Azure. Commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="d6435-162">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="d6435-163">Microsoft. Azure. Commands. Network. models. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="d6435-163">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="d6435-164">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d6435-164">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d6435-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6435-165">OUTPUTS</span></span>

### <span data-ttu-id="d6435-166">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d6435-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="d6435-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6435-167">NOTES</span></span>

## <span data-ttu-id="d6435-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6435-168">RELATED LINKS</span></span>

[<span data-ttu-id="d6435-169">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d6435-169">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="d6435-170">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d6435-170">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="d6435-171">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d6435-171">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
