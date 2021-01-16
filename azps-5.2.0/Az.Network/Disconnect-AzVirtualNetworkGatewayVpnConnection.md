---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354154"
---
# <span data-ttu-id="f87cc-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f87cc-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="f87cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f87cc-102">SYNOPSIS</span></span> 
<span data-ttu-id="f87cc-103">Odłączanie połączeń klientów VPN z daną bramą sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f87cc-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="f87cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f87cc-104">SYNTAX</span></span>
### <span data-ttu-id="f87cc-105">ByVpnGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f87cc-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="f87cc-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="f87cc-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="f87cc-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="f87cc-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="f87cc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f87cc-108">DESCRIPTION</span></span>
<span data-ttu-id="f87cc-109">Polecenie cmdlet **Disconnect-AzVirtualNetworkGatewayVpnConnection** umożliwia odłączenie połączenia klienta VPN.</span><span class="sxs-lookup"><span data-stu-id="f87cc-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="f87cc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f87cc-110">EXAMPLES</span></span>

### <span data-ttu-id="f87cc-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f87cc-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="f87cc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f87cc-112">PARAMETERS</span></span>

### <span data-ttu-id="f87cc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f87cc-113">-ResourceGroupName</span></span>
<span data-ttu-id="f87cc-114">Nazwa grupy zasobów bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f87cc-114">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="f87cc-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f87cc-115">-ResourceName</span></span>
<span data-ttu-id="f87cc-116">Nazwa bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f87cc-116">Virtual network gateway name</span></span>

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

### <span data-ttu-id="f87cc-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f87cc-117">-ResourceId</span></span>
<span data-ttu-id="f87cc-118">Identyfikator zasobu bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f87cc-118">Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="f87cc-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="f87cc-119">-VpnConnectionId</span></span>
<span data-ttu-id="f87cc-120">Identyfikatory połączeń sieci VPN</span><span class="sxs-lookup"><span data-stu-id="f87cc-120">Vpn Connection Ids</span></span>

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

### <span data-ttu-id="f87cc-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f87cc-121">-InputObject</span></span>
<span data-ttu-id="f87cc-122">Obiekt bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f87cc-122">Virtual network gateway object</span></span>

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

### <span data-ttu-id="f87cc-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f87cc-123">-AsJob</span></span>
<span data-ttu-id="f87cc-124">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f87cc-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f87cc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f87cc-125">CommonParameters</span></span>
<span data-ttu-id="f87cc-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f87cc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f87cc-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f87cc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f87cc-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f87cc-128">INPUTS</span></span>

### <span data-ttu-id="f87cc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f87cc-129">System.String</span></span>

## <span data-ttu-id="f87cc-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f87cc-130">OUTPUTS</span></span>

### <span data-ttu-id="f87cc-131">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f87cc-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f87cc-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f87cc-132">NOTES</span></span>

## <span data-ttu-id="f87cc-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f87cc-133">RELATED LINKS</span></span>
