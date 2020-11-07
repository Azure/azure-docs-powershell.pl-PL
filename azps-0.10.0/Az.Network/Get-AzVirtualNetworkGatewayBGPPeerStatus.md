---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: f92b211befbf019f46869f733fa012e74e72c327
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890669"
---
# <span data-ttu-id="f8e12-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="f8e12-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="f8e12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8e12-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e12-103">Zawiera listę elementów równorzędnych BGP bramy sieci wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f8e12-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="f8e12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8e12-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8e12-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f8e12-105">DESCRIPTION</span></span>
<span data-ttu-id="f8e12-106">To polecenie wylicza elementy równorzędne protokołu BGP brama usługi Azure Virtual Network jest skonfigurowana jako peer.</span><span class="sxs-lookup"><span data-stu-id="f8e12-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="f8e12-107">Stan każdego elementu równorzędnego jest również podany.</span><span class="sxs-lookup"><span data-stu-id="f8e12-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="f8e12-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8e12-108">EXAMPLES</span></span>

### <span data-ttu-id="f8e12-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f8e12-109">Example 1</span></span>
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

<span data-ttu-id="f8e12-110">Pobiera elementy równorzędne BGP dla bramy sieci wirtualnej platformy Azure o nazwie gatewayname w grupie zasobów Resource Group.</span><span class="sxs-lookup"><span data-stu-id="f8e12-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>

<span data-ttu-id="f8e12-111">W tym przykładzie pokazano, który połączony element równorzędny BGP ma adres IP 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="f8e12-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="f8e12-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8e12-112">PARAMETERS</span></span>

### <span data-ttu-id="f8e12-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8e12-113">-AsJob</span></span>
<span data-ttu-id="f8e12-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f8e12-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8e12-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e12-115">-DefaultProfile</span></span>
<span data-ttu-id="f8e12-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8e12-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8e12-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="f8e12-117">-Peer</span></span>
<span data-ttu-id="f8e12-118">IP elementu równorzędnego, aby pobrać stan</span><span class="sxs-lookup"><span data-stu-id="f8e12-118">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="f8e12-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8e12-119">-ResourceGroupName</span></span>
<span data-ttu-id="f8e12-120">Nazwa grupy zasobów bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f8e12-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="f8e12-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="f8e12-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="f8e12-122">Nazwa bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f8e12-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="f8e12-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e12-123">CommonParameters</span></span>
<span data-ttu-id="f8e12-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8e12-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e12-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8e12-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e12-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8e12-126">INPUTS</span></span>

### <span data-ttu-id="f8e12-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f8e12-127">System.String</span></span>

## <span data-ttu-id="f8e12-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8e12-128">OUTPUTS</span></span>

### <span data-ttu-id="f8e12-129">Microsoft. Azure. Commands. Network. models. PSBGPPeerStatus []</span><span class="sxs-lookup"><span data-stu-id="f8e12-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus[]</span></span>

## <span data-ttu-id="f8e12-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8e12-130">NOTES</span></span>

## <span data-ttu-id="f8e12-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8e12-131">RELATED LINKS</span></span>

