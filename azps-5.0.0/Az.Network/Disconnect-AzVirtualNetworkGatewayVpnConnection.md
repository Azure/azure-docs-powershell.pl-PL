---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232843"
---
# <span data-ttu-id="7089b-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7089b-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="7089b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7089b-102">SYNOPSIS</span></span> 
<span data-ttu-id="7089b-103">Odłączanie połączeń klientów VPN z daną bramą sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7089b-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="7089b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7089b-104">SYNTAX</span></span>
### <span data-ttu-id="7089b-105">ByVpnGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7089b-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="7089b-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7089b-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="7089b-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7089b-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="7089b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7089b-108">DESCRIPTION</span></span>
<span data-ttu-id="7089b-109">Polecenie cmdlet **Disconnect-AzVirtualNetworkGatewayVpnConnection** umożliwia odłączenie połączenia klienta VPN.</span><span class="sxs-lookup"><span data-stu-id="7089b-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="7089b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7089b-110">EXAMPLES</span></span>

### <span data-ttu-id="7089b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7089b-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="7089b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7089b-112">PARAMETERS</span></span>

### <span data-ttu-id="7089b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7089b-113">-ResourceGroupName</span></span>
<span data-ttu-id="7089b-114">Nazwa grupy zasobów bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="7089b-114">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="7089b-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7089b-115">-ResourceName</span></span>
<span data-ttu-id="7089b-116">Nazwa bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="7089b-116">Virtual network gateway name</span></span>

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

### <span data-ttu-id="7089b-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7089b-117">-ResourceId</span></span>
<span data-ttu-id="7089b-118">Identyfikator zasobu bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="7089b-118">Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="7089b-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="7089b-119">-VpnConnectionId</span></span>
<span data-ttu-id="7089b-120">Identyfikatory połączeń sieci VPN</span><span class="sxs-lookup"><span data-stu-id="7089b-120">Vpn Connection Ids</span></span>

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

### <span data-ttu-id="7089b-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7089b-121">-InputObject</span></span>
<span data-ttu-id="7089b-122">Obiekt bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="7089b-122">Virtual network gateway object</span></span>

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

### <span data-ttu-id="7089b-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7089b-123">-AsJob</span></span>
<span data-ttu-id="7089b-124">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7089b-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7089b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7089b-125">CommonParameters</span></span>
<span data-ttu-id="7089b-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7089b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7089b-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7089b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7089b-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7089b-128">INPUTS</span></span>

### <span data-ttu-id="7089b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7089b-129">System.String</span></span>

## <span data-ttu-id="7089b-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7089b-130">OUTPUTS</span></span>

### <span data-ttu-id="7089b-131">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7089b-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7089b-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7089b-132">NOTES</span></span>

## <span data-ttu-id="7089b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7089b-133">RELATED LINKS</span></span>
