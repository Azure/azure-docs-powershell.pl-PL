---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: f335272bce6591c617d8111dd1d0d81af50ec255
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050774"
---
# <span data-ttu-id="e72b9-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="e72b9-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="e72b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e72b9-102">SYNOPSIS</span></span>
<span data-ttu-id="e72b9-103">Tworzy zasady wyboru ruchu.</span><span class="sxs-lookup"><span data-stu-id="e72b9-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="e72b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e72b9-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e72b9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e72b9-105">DESCRIPTION</span></span>
<span data-ttu-id="e72b9-106">Polecenie cmdlet New-AzTrafficSelectorPolicy tworzy propozycję zasad wybierania ruchu, która będzie używana w połączeniu bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e72b9-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="e72b9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e72b9-107">EXAMPLES</span></span>

### <span data-ttu-id="e72b9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e72b9-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="e72b9-109">Tworzy wystąpienie zasad wyboru ruchu i dodaje je jako parametr podczas tworzenia połączenia bramy sieci wirtualnej za pomocą protokołu IKEv2.</span><span class="sxs-lookup"><span data-stu-id="e72b9-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="e72b9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e72b9-110">PARAMETERS</span></span>

### <span data-ttu-id="e72b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e72b9-111">-DefaultProfile</span></span>
<span data-ttu-id="e72b9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e72b9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e72b9-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="e72b9-113">-LocalAddressRange</span></span>
<span data-ttu-id="e72b9-114">Zbiór zakresów adresów CIDR</span><span class="sxs-lookup"><span data-stu-id="e72b9-114">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e72b9-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="e72b9-115">-RemoteAddressRange</span></span>
<span data-ttu-id="e72b9-116">Zbiór zakresów adresów CIDR</span><span class="sxs-lookup"><span data-stu-id="e72b9-116">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e72b9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e72b9-117">CommonParameters</span></span>
<span data-ttu-id="e72b9-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e72b9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e72b9-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e72b9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e72b9-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e72b9-120">INPUTS</span></span>

### <span data-ttu-id="e72b9-121">System. String []</span><span class="sxs-lookup"><span data-stu-id="e72b9-121">System.String[]</span></span>

## <span data-ttu-id="e72b9-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e72b9-122">OUTPUTS</span></span>

### <span data-ttu-id="e72b9-123">Microsoft. Azure. Commands. Network. models. PSTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="e72b9-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="e72b9-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e72b9-124">NOTES</span></span>

## <span data-ttu-id="e72b9-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e72b9-125">RELATED LINKS</span></span>
