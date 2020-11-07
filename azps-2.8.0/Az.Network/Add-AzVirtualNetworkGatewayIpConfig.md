---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: a0369a598cd7a3a0fa4044a267568260fbfda86c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870824"
---
# <span data-ttu-id="d7321-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d7321-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="d7321-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7321-102">SYNOPSIS</span></span>
<span data-ttu-id="d7321-103">Dodaje konfigurację IP do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d7321-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="d7321-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7321-104">SYNTAX</span></span>

### <span data-ttu-id="d7321-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d7321-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7321-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d7321-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7321-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d7321-107">DESCRIPTION</span></span>
<span data-ttu-id="d7321-108">Polecenie cmdlet **Add-AzVirtualNetworkGatewayIpConfig** umożliwia dodanie konfiguracji IP do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d7321-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="d7321-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7321-109">EXAMPLES</span></span>

### <span data-ttu-id="d7321-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d7321-110">Example 1</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gw -Name GWIPConfig2 -Subnet $subnet -PublicIpAddress $gwpip2


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

## <span data-ttu-id="d7321-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7321-111">PARAMETERS</span></span>

### <span data-ttu-id="d7321-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7321-112">-DefaultProfile</span></span>
<span data-ttu-id="d7321-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7321-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7321-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d7321-114">-Name</span></span>
<span data-ttu-id="d7321-115">Określa nazwę konfiguracji IP bramy do dodania.</span><span class="sxs-lookup"><span data-stu-id="d7321-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="d7321-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d7321-116">-PrivateIpAddress</span></span>
<span data-ttu-id="d7321-117">Określa prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="d7321-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="d7321-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d7321-118">-PublicIpAddress</span></span>
<span data-ttu-id="d7321-119">Określa publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="d7321-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="d7321-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="d7321-120">-PublicIpAddressId</span></span>
<span data-ttu-id="d7321-121">Określa identyfikator publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="d7321-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="d7321-122">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="d7321-122">-Subnet</span></span>
<span data-ttu-id="d7321-123">Określa obiekt **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="d7321-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="d7321-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d7321-124">-SubnetId</span></span>
<span data-ttu-id="d7321-125">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="d7321-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="d7321-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d7321-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="d7321-127">Określa obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="d7321-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="d7321-128">To polecenie cmdlet modyfikuje określony obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="d7321-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="d7321-129">Możesz użyć polecenia cmdlet Get-AzVirtualNetworkGateway, aby pobrać obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="d7321-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="d7321-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7321-130">-Confirm</span></span>
<span data-ttu-id="d7321-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7321-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7321-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7321-132">-WhatIf</span></span>
<span data-ttu-id="d7321-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7321-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7321-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7321-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7321-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7321-135">CommonParameters</span></span>
<span data-ttu-id="d7321-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7321-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7321-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7321-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7321-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7321-138">INPUTS</span></span>

### <span data-ttu-id="d7321-139">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d7321-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d7321-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7321-140">OUTPUTS</span></span>

### <span data-ttu-id="d7321-141">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d7321-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d7321-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7321-142">NOTES</span></span>

## <span data-ttu-id="d7321-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7321-143">RELATED LINKS</span></span>

[<span data-ttu-id="d7321-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d7321-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d7321-145">Nowe — AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d7321-145">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="d7321-146">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d7321-146">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
