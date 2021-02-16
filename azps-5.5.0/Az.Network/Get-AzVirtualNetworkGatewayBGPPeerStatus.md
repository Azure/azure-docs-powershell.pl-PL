---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 62fed5537cc22ee21679cbe1b8d126d9d30efb71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179811"
---
# <span data-ttu-id="8a6fd-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="8a6fd-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="8a6fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a6fd-102">SYNOPSIS</span></span>
<span data-ttu-id="8a6fd-103">Lista równorzędnych BGP bramy sieci wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8a6fd-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="8a6fd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8a6fd-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a6fd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8a6fd-105">DESCRIPTION</span></span>
<span data-ttu-id="8a6fd-106">To polecenie wylicza, że równorzędne BGP są konfigurowane do komunikacji równorzędnej bramy wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8a6fd-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="8a6fd-107">Jest również podawany stan każdej równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="8a6fd-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="8a6fd-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8a6fd-108">EXAMPLES</span></span>

### <span data-ttu-id="8a6fd-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8a6fd-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayBgpPeerStatus -ResourceGroupName resourceGroup -VirtualNetworkGatewayName gatewayName

Asn               : 65515
ConnectedDuration : 9.01:04:53.5768637
LocalAddress      : 10.1.0.254
MessagesReceived  : 14893
MessagesSent      : 14900
Neighbor          : 10.0.0.254
RoutesReceived    : 1
State             : Connected
```

<span data-ttu-id="8a6fd-110">Pobiera współpracowników BGP dla bramy sieci wirtualnej platformy Azure o nazwie nazwana nazwa_bramy w grupie zasobów resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8a6fd-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="8a6fd-111">W tym przykładzie dane wyjściowe przedstawia jeden połączony element równorzędny BGP o adresie IP 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="8a6fd-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="8a6fd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a6fd-112">PARAMETERS</span></span>

### <span data-ttu-id="8a6fd-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8a6fd-113">-AsJob</span></span>
<span data-ttu-id="8a6fd-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8a6fd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a6fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a6fd-115">-DefaultProfile</span></span>
<span data-ttu-id="8a6fd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a6fd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a6fd-117">— Peer</span><span class="sxs-lookup"><span data-stu-id="8a6fd-117">-Peer</span></span>
<span data-ttu-id="8a6fd-118">Adres IP współpracownika, dla których ma zostać pobrany stan</span><span class="sxs-lookup"><span data-stu-id="8a6fd-118">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="8a6fd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a6fd-119">-ResourceGroupName</span></span>
<span data-ttu-id="8a6fd-120">Nazwa grupy zasobów bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="8a6fd-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="8a6fd-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="8a6fd-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="8a6fd-122">Nazwa bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="8a6fd-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="8a6fd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a6fd-123">CommonParameters</span></span>
<span data-ttu-id="8a6fd-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a6fd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a6fd-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a6fd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a6fd-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a6fd-126">INPUTS</span></span>

### <span data-ttu-id="8a6fd-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8a6fd-127">System.String</span></span>

## <span data-ttu-id="8a6fd-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a6fd-128">OUTPUTS</span></span>

### <span data-ttu-id="8a6fd-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="8a6fd-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="8a6fd-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8a6fd-130">NOTES</span></span>

## <span data-ttu-id="8a6fd-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a6fd-131">RELATED LINKS</span></span>
