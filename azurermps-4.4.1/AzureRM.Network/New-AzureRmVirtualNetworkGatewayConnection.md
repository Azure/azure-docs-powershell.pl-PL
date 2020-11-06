---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 0c619b306d6dece23006d351f666637afe9f852a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527433"
---
# <span data-ttu-id="7e486-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7e486-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7e486-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e486-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e486-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e486-103">SYNTAX</span></span>

### <span data-ttu-id="7e486-104">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7e486-104">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e486-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7e486-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e486-106">Opis</span><span class="sxs-lookup"><span data-stu-id="7e486-106">DESCRIPTION</span></span>

## <span data-ttu-id="7e486-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e486-107">EXAMPLES</span></span>

### <span data-ttu-id="7e486-108">1:1</span><span class="sxs-lookup"><span data-stu-id="7e486-108">1:</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="7e486-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e486-109">PARAMETERS</span></span>

### <span data-ttu-id="7e486-110">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="7e486-110">-AuthorizationKey</span></span>
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

### <span data-ttu-id="7e486-111">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="7e486-111">-ConnectionType</span></span>
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

### <span data-ttu-id="7e486-112">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7e486-112">-EnableBgp</span></span>
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

### <span data-ttu-id="7e486-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7e486-113">-Force</span></span>
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

### <span data-ttu-id="7e486-114">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="7e486-114">-IpsecPolicies</span></span>
<span data-ttu-id="7e486-115">Lista zasad IPSec.</span><span class="sxs-lookup"><span data-stu-id="7e486-115">A list of IPSec policies.</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e486-116">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="7e486-116">-LocalNetworkGateway2</span></span>
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

### <span data-ttu-id="7e486-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7e486-117">-Location</span></span>
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

### <span data-ttu-id="7e486-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7e486-118">-Name</span></span>
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

### <span data-ttu-id="7e486-119">-Peer</span><span class="sxs-lookup"><span data-stu-id="7e486-119">-Peer</span></span>
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

### <span data-ttu-id="7e486-120">-PeerId</span><span class="sxs-lookup"><span data-stu-id="7e486-120">-PeerId</span></span>
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

### <span data-ttu-id="7e486-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e486-121">-ResourceGroupName</span></span>
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

### <span data-ttu-id="7e486-122">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="7e486-122">-RoutingWeight</span></span>
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

### <span data-ttu-id="7e486-123">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7e486-123">-SharedKey</span></span>
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

### <span data-ttu-id="7e486-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e486-124">-Tag</span></span>
<span data-ttu-id="7e486-125">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7e486-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7e486-126">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="7e486-126">For example:</span></span>

<span data-ttu-id="7e486-127">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="7e486-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7e486-128">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="7e486-128">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="7e486-129">Używanie selektorów ruchu opartego na zasadach dla połączenia S2S</span><span class="sxs-lookup"><span data-stu-id="7e486-129">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="7e486-130">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="7e486-130">-VirtualNetworkGateway1</span></span>
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

### <span data-ttu-id="7e486-131">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="7e486-131">-VirtualNetworkGateway2</span></span>
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

### <span data-ttu-id="7e486-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e486-132">-Confirm</span></span>
<span data-ttu-id="7e486-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e486-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e486-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e486-134">-WhatIf</span></span>
<span data-ttu-id="7e486-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e486-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e486-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7e486-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e486-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e486-137">-DefaultProfile</span></span>
<span data-ttu-id="7e486-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e486-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e486-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e486-139">CommonParameters</span></span>
<span data-ttu-id="7e486-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e486-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e486-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e486-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e486-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e486-142">INPUTS</span></span>

## <span data-ttu-id="7e486-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e486-143">OUTPUTS</span></span>

### <span data-ttu-id="7e486-144">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7e486-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7e486-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e486-145">NOTES</span></span>

## <span data-ttu-id="7e486-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e486-146">RELATED LINKS</span></span>

[<span data-ttu-id="7e486-147">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7e486-147">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7e486-148">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7e486-148">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7e486-149">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7e486-149">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
