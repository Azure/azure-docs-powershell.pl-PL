---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: 1cbbfcbc87ed1d9be869066f8ec6dd288ba3d4d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003706"
---
# <span data-ttu-id="5053d-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="5053d-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="5053d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5053d-102">SYNOPSIS</span></span> 
<span data-ttu-id="5053d-103">Odłączanie połączonych połączeń klienta vpn za pomocą owej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5053d-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="5053d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5053d-104">SYNTAX</span></span>
### <span data-ttu-id="5053d-105">ByVpnGatewayName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="5053d-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="5053d-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="5053d-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="5053d-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="5053d-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="5053d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5053d-108">DESCRIPTION</span></span>
<span data-ttu-id="5053d-109">Polecenie cmdlet **Disconnect-AzVirtualNetworkGatewayVpnConnection** umożliwia odłączenie danego połączonego połączenia klienta vpn.</span><span class="sxs-lookup"><span data-stu-id="5053d-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="5053d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5053d-110">EXAMPLES</span></span>

### <span data-ttu-id="5053d-111">Przykład</span><span class="sxs-lookup"><span data-stu-id="5053d-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="5053d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5053d-112">PARAMETERS</span></span>

### <span data-ttu-id="5053d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5053d-113">-ResourceGroupName</span></span>
<span data-ttu-id="5053d-114">Nazwa grupy zasobów bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5053d-114">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5053d-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5053d-115">-ResourceName</span></span>
<span data-ttu-id="5053d-116">Nazwa bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5053d-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5053d-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5053d-117">-ResourceId</span></span>
<span data-ttu-id="5053d-118">Identyfikator zasobu bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5053d-118">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5053d-119">- VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="5053d-119">-VpnConnectionId</span></span>
<span data-ttu-id="5053d-120">Identyfikatory połączeń vpn</span><span class="sxs-lookup"><span data-stu-id="5053d-120">Vpn Connection Ids</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5053d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5053d-121">-InputObject</span></span>
<span data-ttu-id="5053d-122">Obiekt bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5053d-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5053d-123">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5053d-123">-AsJob</span></span>
<span data-ttu-id="5053d-124">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5053d-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5053d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5053d-125">CommonParameters</span></span>
<span data-ttu-id="5053d-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5053d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5053d-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5053d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5053d-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5053d-128">INPUTS</span></span>

### <span data-ttu-id="5053d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5053d-129">System.String</span></span>

## <span data-ttu-id="5053d-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5053d-130">OUTPUTS</span></span>

### <span data-ttu-id="5053d-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5053d-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="5053d-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5053d-132">NOTES</span></span>

## <span data-ttu-id="5053d-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5053d-133">RELATED LINKS</span></span>
