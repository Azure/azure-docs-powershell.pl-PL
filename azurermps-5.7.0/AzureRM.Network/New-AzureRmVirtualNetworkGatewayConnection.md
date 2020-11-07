---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 5beb3e7c2c010570089dfd0667eca48e5d1c6728
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718043"
---
# <span data-ttu-id="6ab64-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6ab64-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="6ab64-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ab64-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ab64-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ab64-103">SYNTAX</span></span>

### <span data-ttu-id="6ab64-104">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6ab64-104">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ab64-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6ab64-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ab64-106">Opis</span><span class="sxs-lookup"><span data-stu-id="6ab64-106">DESCRIPTION</span></span>

## <span data-ttu-id="6ab64-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ab64-107">EXAMPLES</span></span>

### <span data-ttu-id="6ab64-108">1:1</span><span class="sxs-lookup"><span data-stu-id="6ab64-108">1:</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="6ab64-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ab64-109">PARAMETERS</span></span>

### <span data-ttu-id="6ab64-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ab64-110">-AsJob</span></span>
<span data-ttu-id="6ab64-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6ab64-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ab64-112">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="6ab64-112">-AuthorizationKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-113">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="6ab64-113">-ConnectionType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab64-114">-DefaultProfile</span></span>
<span data-ttu-id="6ab64-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab64-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-116">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="6ab64-116">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6ab64-117">-Force</span></span>
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

### <span data-ttu-id="6ab64-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="6ab64-118">-IpsecPolicies</span></span>
<span data-ttu-id="6ab64-119">Lista zasad IPSec.</span><span class="sxs-lookup"><span data-stu-id="6ab64-119">A list of IPSec policies.</span></span>
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

### <span data-ttu-id="6ab64-120">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="6ab64-120">-LocalNetworkGateway2</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6ab64-121">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6ab64-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-123">-Peer</span><span class="sxs-lookup"><span data-stu-id="6ab64-123">-Peer</span></span>
```yaml
Type: PSPeering
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-124">-PeerId</span><span class="sxs-lookup"><span data-stu-id="6ab64-124">-PeerId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ab64-125">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-126">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="6ab64-126">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-127">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="6ab64-127">-SharedKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="6ab64-128">-Tag</span></span>
<span data-ttu-id="6ab64-129">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="6ab64-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6ab64-130">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="6ab64-130">For example:</span></span>

<span data-ttu-id="6ab64-131">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="6ab64-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-132">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="6ab64-132">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="6ab64-133">Używanie selektorów ruchu opartego na zasadach dla połączenia S2S</span><span class="sxs-lookup"><span data-stu-id="6ab64-133">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-134">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="6ab64-134">-VirtualNetworkGateway1</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-135">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="6ab64-135">-VirtualNetworkGateway2</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ab64-136">-Confirm</span></span>
<span data-ttu-id="6ab64-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ab64-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ab64-138">-WhatIf</span></span>
<span data-ttu-id="6ab64-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ab64-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ab64-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ab64-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab64-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab64-141">CommonParameters</span></span>
<span data-ttu-id="6ab64-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ab64-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab64-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ab64-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab64-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ab64-144">INPUTS</span></span>

### <span data-ttu-id="6ab64-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6ab64-145">None</span></span>
<span data-ttu-id="6ab64-146">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6ab64-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ab64-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ab64-147">OUTPUTS</span></span>

### <span data-ttu-id="6ab64-148">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6ab64-148">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="6ab64-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ab64-149">NOTES</span></span>

## <span data-ttu-id="6ab64-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ab64-150">RELATED LINKS</span></span>

[<span data-ttu-id="6ab64-151">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6ab64-151">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6ab64-152">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6ab64-152">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6ab64-153">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6ab64-153">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
