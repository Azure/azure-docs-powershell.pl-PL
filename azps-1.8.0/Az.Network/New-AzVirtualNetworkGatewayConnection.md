---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 8f6b095a502c235927a48f2043a9140483cedc3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709226"
---
# <span data-ttu-id="a0e7c-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a0e7c-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="a0e7c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e7c-103">Umożliwia utworzenie połączenia VPN między lokacjami między bramą sieci wirtualnej a urządzeniem VPN na środowisku.</span><span class="sxs-lookup"><span data-stu-id="a0e7c-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="a0e7c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0e7c-104">SYNTAX</span></span>

### <span data-ttu-id="a0e7c-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a0e7c-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-AsJob] [-ExpressRouteGatewayBypass]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0e7c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a0e7c-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-AsJob] [-ExpressRouteGatewayBypass]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0e7c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a0e7c-107">DESCRIPTION</span></span>
<span data-ttu-id="a0e7c-108">Umożliwia utworzenie połączenia VPN między lokacjami między bramą sieci wirtualnej a urządzeniem VPN na środowisku.</span><span class="sxs-lookup"><span data-stu-id="a0e7c-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="a0e7c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0e7c-109">EXAMPLES</span></span>

### <span data-ttu-id="a0e7c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a0e7c-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="a0e7c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0e7c-111">PARAMETERS</span></span>

### <span data-ttu-id="a0e7c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0e7c-112">-AsJob</span></span>
<span data-ttu-id="a0e7c-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a0e7c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0e7c-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="a0e7c-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="a0e7c-115">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="a0e7c-115">-ConnectionType</span></span>

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

### <span data-ttu-id="a0e7c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e7c-116">-DefaultProfile</span></span>
<span data-ttu-id="a0e7c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0e7c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0e7c-118">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="a0e7c-118">-EnableBgp</span></span>

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

### <span data-ttu-id="a0e7c-119">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="a0e7c-119">-ExpressRouteGatewayBypass</span></span>

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

### <span data-ttu-id="a0e7c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a0e7c-120">-Force</span></span>

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

### <span data-ttu-id="a0e7c-121">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="a0e7c-121">-IpsecPolicies</span></span>
<span data-ttu-id="a0e7c-122">Lista zasad IPSec.</span><span class="sxs-lookup"><span data-stu-id="a0e7c-122">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="a0e7c-123">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="a0e7c-123">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="a0e7c-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a0e7c-124">-Location</span></span>

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

### <span data-ttu-id="a0e7c-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a0e7c-125">-Name</span></span>

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

### <span data-ttu-id="a0e7c-126">-Peer</span><span class="sxs-lookup"><span data-stu-id="a0e7c-126">-Peer</span></span>

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

### <span data-ttu-id="a0e7c-127">-PeerId</span><span class="sxs-lookup"><span data-stu-id="a0e7c-127">-PeerId</span></span>

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

### <span data-ttu-id="a0e7c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0e7c-128">-ResourceGroupName</span></span>

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

### <span data-ttu-id="a0e7c-129">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="a0e7c-129">-RoutingWeight</span></span>

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

### <span data-ttu-id="a0e7c-130">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="a0e7c-130">-SharedKey</span></span>

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

### <span data-ttu-id="a0e7c-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0e7c-131">-Tag</span></span>
<span data-ttu-id="a0e7c-132">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a0e7c-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a0e7c-133">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="a0e7c-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a0e7c-134">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="a0e7c-134">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="a0e7c-135">Używanie selektorów ruchu opartego na zasadach dla połączenia S2S</span><span class="sxs-lookup"><span data-stu-id="a0e7c-135">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="a0e7c-136">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="a0e7c-136">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="a0e7c-137">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="a0e7c-137">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="a0e7c-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0e7c-138">-Confirm</span></span>
<span data-ttu-id="a0e7c-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0e7c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0e7c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0e7c-140">-WhatIf</span></span>
<span data-ttu-id="a0e7c-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0e7c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0e7c-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a0e7c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0e7c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e7c-143">CommonParameters</span></span>
<span data-ttu-id="a0e7c-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0e7c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e7c-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0e7c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e7c-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0e7c-146">INPUTS</span></span>

### <span data-ttu-id="a0e7c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a0e7c-147">System.String</span></span>

### <span data-ttu-id="a0e7c-148">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a0e7c-148">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="a0e7c-149">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a0e7c-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="a0e7c-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a0e7c-150">System.Int32</span></span>

### <span data-ttu-id="a0e7c-151">Microsoft. Azure. Commands. Network. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="a0e7c-151">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="a0e7c-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0e7c-152">System.Boolean</span></span>

### <span data-ttu-id="a0e7c-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a0e7c-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a0e7c-154">Microsoft. Azure. Commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="a0e7c-154">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="a0e7c-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a0e7c-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a0e7c-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0e7c-156">OUTPUTS</span></span>

### <span data-ttu-id="a0e7c-157">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a0e7c-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="a0e7c-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0e7c-158">NOTES</span></span>

## <span data-ttu-id="a0e7c-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0e7c-159">RELATED LINKS</span></span>

[<span data-ttu-id="a0e7c-160">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a0e7c-160">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="a0e7c-161">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a0e7c-161">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="a0e7c-162">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a0e7c-162">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
