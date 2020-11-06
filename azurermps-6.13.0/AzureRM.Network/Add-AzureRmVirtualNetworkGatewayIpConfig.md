---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 22877a91c3b6939d35e2eae8d359dc9056425447
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552720"
---
# <span data-ttu-id="f551f-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f551f-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="f551f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f551f-102">SYNOPSIS</span></span>
<span data-ttu-id="f551f-103">Dodaje konfigurację IP do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f551f-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f551f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f551f-104">SYNTAX</span></span>

### <span data-ttu-id="f551f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f551f-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f551f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f551f-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f551f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f551f-107">DESCRIPTION</span></span>
<span data-ttu-id="f551f-108">Polecenie cmdlet **Add-AzureRmVirtualNetworkGatewayIpConfig** umożliwia dodanie konfiguracji IP do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f551f-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="f551f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f551f-109">EXAMPLES</span></span>

### <span data-ttu-id="f551f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f551f-110">Example 1</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gw -Name GWIPConfig2 -Subnet $subnet -PublicIpAddress $gwpip2


Name                   : VNet7GW
ResourceGroupName      : VPNGatewayV3
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW
Etag                   : W/"d27a784f-3c3f-4150-863d-764649b6e8e7"
ResourceGuid           : 3c2478a7-d5d4-4e80-8532-7ea2ad577598
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworks/Vnet7/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/VNet7GW_IP"
                             },
                             "Name": "default",
                             "Etag": "W/\"d27a784f-3c3f-4150-863d-764649b6e8e7\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW/ipConfigurations/default"
                           },
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/delIPConfig"
                             },
                             "Name": "GWIPConfig2",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupNotSet/providers/Microsoft.Network/virtualNetworkGateways/VirtualNetworkGatewayNameNotSet/virtualNetworkGatewayIpConfiguration/GWIPConfig2"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : True
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65534,
                           "BgpPeeringAddress": "10.7.255.254",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="f551f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f551f-111">PARAMETERS</span></span>

### <span data-ttu-id="f551f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f551f-112">-DefaultProfile</span></span>
<span data-ttu-id="f551f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f551f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f551f-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f551f-114">-Name</span></span>
<span data-ttu-id="f551f-115">Określa nazwę konfiguracji IP bramy do dodania.</span><span class="sxs-lookup"><span data-stu-id="f551f-115">Specifies the name of the gateway IP configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f551f-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f551f-116">-PrivateIpAddress</span></span>
<span data-ttu-id="f551f-117">Określa prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="f551f-117">Specifies the private IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f551f-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f551f-118">-PublicIpAddress</span></span>
<span data-ttu-id="f551f-119">Określa publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="f551f-119">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f551f-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f551f-120">-PublicIpAddressId</span></span>
<span data-ttu-id="f551f-121">Określa identyfikator publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="f551f-121">Specifies the ID of the public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f551f-122">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="f551f-122">-Subnet</span></span>
<span data-ttu-id="f551f-123">Określa obiekt **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="f551f-123">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f551f-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f551f-124">-SubnetId</span></span>
<span data-ttu-id="f551f-125">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="f551f-125">Specifies the ID of the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f551f-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f551f-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="f551f-127">Określa obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="f551f-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="f551f-128">To polecenie cmdlet modyfikuje określony obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="f551f-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="f551f-129">Możesz użyć polecenia cmdlet Get-AzureRmVirtualNetworkGateway, aby pobrać obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="f551f-129">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f551f-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f551f-130">-Confirm</span></span>
<span data-ttu-id="f551f-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f551f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f551f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f551f-132">-WhatIf</span></span>
<span data-ttu-id="f551f-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f551f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f551f-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f551f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f551f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f551f-135">CommonParameters</span></span>
<span data-ttu-id="f551f-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f551f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f551f-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f551f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f551f-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f551f-138">INPUTS</span></span>

### <span data-ttu-id="f551f-139">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f551f-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="f551f-140">Parametry: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f551f-140">Parameters: VirtualNetworkGateway (ByValue)</span></span>

## <span data-ttu-id="f551f-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f551f-141">OUTPUTS</span></span>

### <span data-ttu-id="f551f-142">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f551f-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f551f-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f551f-143">NOTES</span></span>

## <span data-ttu-id="f551f-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f551f-144">RELATED LINKS</span></span>

[<span data-ttu-id="f551f-145">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f551f-145">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f551f-146">Nowe — AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f551f-146">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="f551f-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f551f-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


