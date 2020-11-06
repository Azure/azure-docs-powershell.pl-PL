---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 42960533c33cc2d5f8f4ee809cdd7a25c483c75d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546948"
---
# <span data-ttu-id="e589d-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="e589d-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="e589d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e589d-102">SYNOPSIS</span></span>
<span data-ttu-id="e589d-103">Zawiera listę elementów równorzędnych BGP bramy sieci wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e589d-103">Lists an Azure virtual network gateway's BGP peers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e589d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e589d-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e589d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e589d-105">DESCRIPTION</span></span>
<span data-ttu-id="e589d-106">To polecenie wylicza elementy równorzędne protokołu BGP brama usługi Azure Virtual Network jest skonfigurowana jako peer.</span><span class="sxs-lookup"><span data-stu-id="e589d-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="e589d-107">Stan każdego elementu równorzędnego jest również podany.</span><span class="sxs-lookup"><span data-stu-id="e589d-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="e589d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e589d-108">EXAMPLES</span></span>

### <span data-ttu-id="e589d-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e589d-109">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayBgpPeerStatus -ResourceGroupName resourceGroup -VirtualNetworkGatewayName gatewayName

Asn               : 65515
ConnectedDuration : 9.01:04:53.5768637
LocalAddress      : 10.1.0.254
MessagesReceived  : 14893
MessagesSent      : 14900
Neighbor          : 10.0.0.254
RoutesReceived    : 1
State             : Connected
```

<span data-ttu-id="e589d-110">Pobiera elementy równorzędne BGP dla bramy sieci wirtualnej platformy Azure o nazwie gatewayname w grupie zasobów Resource Group.</span><span class="sxs-lookup"><span data-stu-id="e589d-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>

<span data-ttu-id="e589d-111">W tym przykładzie pokazano, który połączony element równorzędny BGP ma adres IP 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="e589d-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="e589d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e589d-112">PARAMETERS</span></span>

### <span data-ttu-id="e589d-113">-Peer</span><span class="sxs-lookup"><span data-stu-id="e589d-113">-Peer</span></span>
<span data-ttu-id="e589d-114">IP elementu równorzędnego, aby pobrać stan</span><span class="sxs-lookup"><span data-stu-id="e589d-114">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="e589d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e589d-115">-ResourceGroupName</span></span>
<span data-ttu-id="e589d-116">Nazwa grupy zasobów bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e589d-116">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="e589d-117">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="e589d-117">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="e589d-118">Nazwa bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e589d-118">Virtual network gateway name</span></span>

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

### <span data-ttu-id="e589d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e589d-119">-DefaultProfile</span></span>
<span data-ttu-id="e589d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e589d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e589d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e589d-121">CommonParameters</span></span>
<span data-ttu-id="e589d-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e589d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e589d-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e589d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e589d-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e589d-124">INPUTS</span></span>

### <span data-ttu-id="e589d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e589d-125">System.String</span></span>

## <span data-ttu-id="e589d-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e589d-126">OUTPUTS</span></span>

### <span data-ttu-id="e589d-127">Microsoft. Azure. Commands. Network. models. PSBGPPeerStatus []</span><span class="sxs-lookup"><span data-stu-id="e589d-127">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus[]</span></span>

## <span data-ttu-id="e589d-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e589d-128">NOTES</span></span>

## <span data-ttu-id="e589d-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e589d-129">RELATED LINKS</span></span>

