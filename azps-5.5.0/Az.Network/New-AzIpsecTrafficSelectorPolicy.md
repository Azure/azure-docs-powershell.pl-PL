---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: f335272bce6591c617d8111dd1d0d81af50ec255
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193658"
---
# <span data-ttu-id="3d70c-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="3d70c-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="3d70c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d70c-102">SYNOPSIS</span></span>
<span data-ttu-id="3d70c-103">Tworzy zasady selektora ruchu.</span><span class="sxs-lookup"><span data-stu-id="3d70c-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="3d70c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3d70c-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d70c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3d70c-105">DESCRIPTION</span></span>
<span data-ttu-id="3d70c-106">Polecenie New-AzTrafficSelectorPolicy cmdlet tworzy propozycję zasad selektora ruchu, która ma być używana w połączeniu z wirtualną bramą sieciową.</span><span class="sxs-lookup"><span data-stu-id="3d70c-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="3d70c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3d70c-107">EXAMPLES</span></span>

### <span data-ttu-id="3d70c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3d70c-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="3d70c-109">Tworzy wystąpienie zasad selektora ruchu i dodaje je jako parametr podczas tworzenia połączenia wirtualnej bramy sieciowej za pomocą protokołu IKEv2.</span><span class="sxs-lookup"><span data-stu-id="3d70c-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="3d70c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d70c-110">PARAMETERS</span></span>

### <span data-ttu-id="3d70c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d70c-111">-DefaultProfile</span></span>
<span data-ttu-id="3d70c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3d70c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d70c-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="3d70c-113">-LocalAddressRange</span></span>
<span data-ttu-id="3d70c-114">Kolekcja zakresów adresów CIDR</span><span class="sxs-lookup"><span data-stu-id="3d70c-114">A collection of CIDR address ranges</span></span>

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

### <span data-ttu-id="3d70c-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="3d70c-115">-RemoteAddressRange</span></span>
<span data-ttu-id="3d70c-116">Zbiór zakresów adresów CIDR</span><span class="sxs-lookup"><span data-stu-id="3d70c-116">A collection of CIDR address ranges</span></span>

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

### <span data-ttu-id="3d70c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d70c-117">CommonParameters</span></span>
<span data-ttu-id="3d70c-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d70c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d70c-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d70c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d70c-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d70c-120">INPUTS</span></span>

### <span data-ttu-id="3d70c-121">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3d70c-121">System.String[]</span></span>

## <span data-ttu-id="3d70c-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d70c-122">OUTPUTS</span></span>

### <span data-ttu-id="3d70c-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="3d70c-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="3d70c-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3d70c-124">NOTES</span></span>

## <span data-ttu-id="3d70c-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d70c-125">RELATED LINKS</span></span>
