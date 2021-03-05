---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: d8f77ffd6353ef55548e8ddc2a2cc4f823efe98d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005985"
---
# <span data-ttu-id="ddcaa-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ddcaa-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="ddcaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddcaa-102">SYNOPSIS</span></span>
<span data-ttu-id="ddcaa-103">Usuwa konfigurację adresu IP z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ddcaa-103">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="ddcaa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ddcaa-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddcaa-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ddcaa-105">DESCRIPTION</span></span>
<span data-ttu-id="ddcaa-106">Usuwa konfigurację adresu IP z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ddcaa-106">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="ddcaa-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ddcaa-107">EXAMPLES</span></span>

### <span data-ttu-id="ddcaa-108">Przykład 1.</span><span class="sxs-lookup"><span data-stu-id="ddcaa-108">Example 1:</span></span>
```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gateway -Name ActiveActive

Name                   : myGateway
ResourceGroupName      : myRG
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft
                         .Network/virtualNetworkGateways/VNet8GW
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/800000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/virtualNetworks/VNet8/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/publicIPAddresses/VNet8GWIP"
                             },
                             "Name": "gwipconfig1",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provider
                         s/Microsoft.Network/virtualNetworkGateways/VNet8GW/ipConfigurations/gwipconfig1"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : True
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "192.0.2.4,192.0.2.5",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="ddcaa-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddcaa-109">PARAMETERS</span></span>

### <span data-ttu-id="ddcaa-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddcaa-110">-DefaultProfile</span></span>
<span data-ttu-id="ddcaa-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ddcaa-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddcaa-112">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ddcaa-112">-Name</span></span>
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

### <span data-ttu-id="ddcaa-113">— VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ddcaa-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="ddcaa-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ddcaa-114">-Confirm</span></span>
<span data-ttu-id="ddcaa-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ddcaa-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddcaa-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddcaa-116">-WhatIf</span></span>
<span data-ttu-id="ddcaa-117">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddcaa-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddcaa-118">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ddcaa-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddcaa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddcaa-119">CommonParameters</span></span>
<span data-ttu-id="ddcaa-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddcaa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddcaa-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddcaa-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddcaa-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddcaa-122">INPUTS</span></span>

### <span data-ttu-id="ddcaa-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ddcaa-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ddcaa-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddcaa-124">OUTPUTS</span></span>

### <span data-ttu-id="ddcaa-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ddcaa-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ddcaa-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ddcaa-126">NOTES</span></span>

## <span data-ttu-id="ddcaa-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ddcaa-127">RELATED LINKS</span></span>

[<span data-ttu-id="ddcaa-128">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ddcaa-128">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="ddcaa-129">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ddcaa-129">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)
