---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: d41e71afc27129d2b2de40df97f12b0bb8f07ae5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179827"
---
# <span data-ttu-id="5b1ec-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="5b1ec-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="5b1ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b1ec-102">SYNOPSIS</span></span>
<span data-ttu-id="5b1ec-103">Lista tras ogłaszanych przez bramę sieci wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5b1ec-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="5b1ec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5b1ec-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b1ec-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5b1ec-105">DESCRIPTION</span></span>
<span data-ttu-id="5b1ec-106">Biorąc pod uwagę adres IP elementu równorzędnego BGP, wylicza trasy ogłaszane do tej równorzędnej przez określoną bramę sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="5b1ec-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5b1ec-107">EXAMPLES</span></span>

### <span data-ttu-id="5b1ec-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5b1ec-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="5b1ec-109">Dla bramy platformy Azure o nazwie nazwana nazwa_bramy w grupie zasobów ResourceGroupName pobiera listę tras ogłaszanych do elementu równorzędnego BGP z adresem IP 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="5b1ec-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5b1ec-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="5b1ec-111">Dla bramy platformy Azure o nazwie nazwana nazwa gatewayName w grupie zasobów nazwa_grupy zasobów pobiera trasy ogłaszane do pierwszej równorzędnej komunikacji BGP na liście równorzędnych BGP bramy.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="5b1ec-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b1ec-112">PARAMETERS</span></span>

### <span data-ttu-id="5b1ec-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5b1ec-113">-AsJob</span></span>
<span data-ttu-id="5b1ec-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5b1ec-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b1ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b1ec-115">-DefaultProfile</span></span>
<span data-ttu-id="5b1ec-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b1ec-117">— Peer</span><span class="sxs-lookup"><span data-stu-id="5b1ec-117">-Peer</span></span>
<span data-ttu-id="5b1ec-118">Adres IP współpracownika BGP.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-118">BGP peer's IP address.</span></span> <span data-ttu-id="5b1ec-119">Powinien to być adres IP w przestrzeni adresów dostępnej z poziomu sieci wirtualnej platformy Azure, w ramach których wdrożono bramę.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="5b1ec-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b1ec-120">-ResourceGroupName</span></span>
<span data-ttu-id="5b1ec-121">Nazwa grupy zasobów bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5b1ec-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="5b1ec-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="5b1ec-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="5b1ec-123">Nazwa bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5b1ec-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="5b1ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b1ec-124">CommonParameters</span></span>
<span data-ttu-id="5b1ec-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b1ec-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b1ec-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b1ec-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b1ec-127">INPUTS</span></span>

### <span data-ttu-id="5b1ec-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5b1ec-128">System.String</span></span>

## <span data-ttu-id="5b1ec-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b1ec-129">OUTPUTS</span></span>

### <span data-ttu-id="5b1ec-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="5b1ec-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="5b1ec-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5b1ec-131">NOTES</span></span>
<span data-ttu-id="5b1ec-132">To polecenie ma zastosowanie tylko do bram sieci wirtualnej platformy Azure z włączonymi połączeniami BGP.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="5b1ec-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b1ec-133">RELATED LINKS</span></span>
