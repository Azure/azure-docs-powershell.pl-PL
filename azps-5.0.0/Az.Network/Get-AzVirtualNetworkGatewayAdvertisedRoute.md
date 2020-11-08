---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: d41e71afc27129d2b2de40df97f12b0bb8f07ae5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232809"
---
# <span data-ttu-id="d37a1-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="d37a1-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="d37a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d37a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d37a1-103">Wyświetla listę tras anonsowanych przez bramę sieci wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d37a1-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="d37a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d37a1-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d37a1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d37a1-105">DESCRIPTION</span></span>
<span data-ttu-id="d37a1-106">W polu IP elementu równorzędnego BGP wylicza trasy anonsowane na tym elemencie równorzędnym przez określoną bramę sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d37a1-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="d37a1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d37a1-107">EXAMPLES</span></span>

### <span data-ttu-id="d37a1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d37a1-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="d37a1-109">W przypadku bramy Azure Gateway o nazwie gatewayname w grupie resourceGroupName jest pobierana Lista tras anonsowanych do elementu równorzędnego BGP za pomocą 10.0.0.254 IP</span><span class="sxs-lookup"><span data-stu-id="d37a1-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="d37a1-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d37a1-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="d37a1-111">W przypadku bramy Azure Gateway o nazwie gatewayname w resourceGroupName Group (zasoby) są pobierane anonsowane trasy do pierwszego elementu równorzędnego BGP na liście elementów równorzędnych BGP.</span><span class="sxs-lookup"><span data-stu-id="d37a1-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="d37a1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d37a1-112">PARAMETERS</span></span>

### <span data-ttu-id="d37a1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d37a1-113">-AsJob</span></span>
<span data-ttu-id="d37a1-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d37a1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d37a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37a1-115">-DefaultProfile</span></span>
<span data-ttu-id="d37a1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d37a1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d37a1-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="d37a1-117">-Peer</span></span>
<span data-ttu-id="d37a1-118">Adres IP elementu równorzędnego BGP.</span><span class="sxs-lookup"><span data-stu-id="d37a1-118">BGP peer's IP address.</span></span> <span data-ttu-id="d37a1-119">Powinien to być adres IP w obszarze adresu dostępnym z poziomu sieci wirtualnej platformy Azure, w którym jest wdrożona brama.</span><span class="sxs-lookup"><span data-stu-id="d37a1-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="d37a1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d37a1-120">-ResourceGroupName</span></span>
<span data-ttu-id="d37a1-121">Nazwa grupy zasobów bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d37a1-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="d37a1-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="d37a1-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="d37a1-123">Nazwa bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d37a1-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="d37a1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37a1-124">CommonParameters</span></span>
<span data-ttu-id="d37a1-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d37a1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37a1-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d37a1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37a1-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d37a1-127">INPUTS</span></span>

### <span data-ttu-id="d37a1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d37a1-128">System.String</span></span>

## <span data-ttu-id="d37a1-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d37a1-129">OUTPUTS</span></span>

### <span data-ttu-id="d37a1-130">Microsoft. Azure. Commands. Network. models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="d37a1-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="d37a1-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d37a1-131">NOTES</span></span>
<span data-ttu-id="d37a1-132">To polecenie dotyczy tylko bram wirtualnej sieci Azure z obsługą połączeń BGP.</span><span class="sxs-lookup"><span data-stu-id="d37a1-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="d37a1-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d37a1-133">RELATED LINKS</span></span>
