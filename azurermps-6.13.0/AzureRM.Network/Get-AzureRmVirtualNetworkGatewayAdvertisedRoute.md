---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: 288a2382470682c8c7b55f7342d5a0f193446019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554262"
---
# <span data-ttu-id="872ca-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="872ca-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="872ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="872ca-102">SYNOPSIS</span></span>
<span data-ttu-id="872ca-103">Wyświetla listę tras anonsowanych przez bramę sieci wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="872ca-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="872ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="872ca-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="872ca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="872ca-105">DESCRIPTION</span></span>
<span data-ttu-id="872ca-106">W polu IP elementu równorzędnego BGP wylicza trasy anonsowane na tym elemencie równorzędnym przez określoną bramę sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="872ca-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="872ca-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="872ca-107">EXAMPLES</span></span>

### <span data-ttu-id="872ca-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="872ca-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="872ca-109">W przypadku bramy Azure Gateway o nazwie gatewayname w grupie zasobów resourceGroupName, retrives listy tras anonsowanych do elementu równorzędnego BGP za pomocą adresu IP 10.0.0.254</span><span class="sxs-lookup"><span data-stu-id="872ca-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="872ca-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="872ca-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="872ca-111">W przypadku bramy Azure Gateway o nazwie gatewayname w resourceGroupName Group (zasoby) są pobierane anonsowane trasy do pierwszego elementu równorzędnego BGP na liście elementów równorzędnych BGP.</span><span class="sxs-lookup"><span data-stu-id="872ca-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="872ca-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="872ca-112">PARAMETERS</span></span>

### <span data-ttu-id="872ca-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="872ca-113">-AsJob</span></span>
<span data-ttu-id="872ca-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="872ca-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="872ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="872ca-115">-DefaultProfile</span></span>
<span data-ttu-id="872ca-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="872ca-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="872ca-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="872ca-117">-Peer</span></span>
<span data-ttu-id="872ca-118">Adres IP elementu równorzędnego BGP.</span><span class="sxs-lookup"><span data-stu-id="872ca-118">BGP peer's IP address.</span></span> <span data-ttu-id="872ca-119">Powinien to być adres IP w obszarze adresu dostępnym z poziomu sieci wirtualnej platformy Azure, w którym jest wdrożona brama.</span><span class="sxs-lookup"><span data-stu-id="872ca-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="872ca-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="872ca-120">-ResourceGroupName</span></span>
<span data-ttu-id="872ca-121">Nazwa grupy zasobów bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="872ca-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="872ca-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="872ca-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="872ca-123">Nazwa bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="872ca-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="872ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="872ca-124">CommonParameters</span></span>
<span data-ttu-id="872ca-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="872ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="872ca-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="872ca-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="872ca-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="872ca-127">INPUTS</span></span>

### <span data-ttu-id="872ca-128">System. String</span><span class="sxs-lookup"><span data-stu-id="872ca-128">System.String</span></span>

## <span data-ttu-id="872ca-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="872ca-129">OUTPUTS</span></span>

### <span data-ttu-id="872ca-130">Microsoft. Azure. Commands. Network. models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="872ca-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="872ca-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="872ca-131">NOTES</span></span>
<span data-ttu-id="872ca-132">To polecenie dotyczy tylko bram wirtualnej sieci Azure z obsługą połączeń BGP.</span><span class="sxs-lookup"><span data-stu-id="872ca-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="872ca-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="872ca-133">RELATED LINKS</span></span>
