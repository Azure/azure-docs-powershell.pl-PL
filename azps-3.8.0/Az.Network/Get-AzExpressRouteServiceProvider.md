---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 639e438a2ff3eb63282ba4f79aa984581128a082
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052318"
---
# <span data-ttu-id="ac552-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="ac552-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="ac552-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac552-102">SYNOPSIS</span></span>
<span data-ttu-id="ac552-103">Pobiera listę dostawców usług ExpressRoute i ich atrybuty.</span><span class="sxs-lookup"><span data-stu-id="ac552-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="ac552-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac552-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac552-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ac552-105">DESCRIPTION</span></span>
<span data-ttu-id="ac552-106">Polecenie cmdlet **Get-AzExpressRouteServiceProvider** pobiera listę dostawców usług ExpressRoute i ich atrybuty.</span><span class="sxs-lookup"><span data-stu-id="ac552-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="ac552-107">Atrybuty obejmują Opcje lokalizacji i przepustowości.</span><span class="sxs-lookup"><span data-stu-id="ac552-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="ac552-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac552-108">EXAMPLES</span></span>

### <span data-ttu-id="ac552-109">Przykład 1: uzyskiwanie listy dostawców usług z lokalizacjami w "Dolina Krzemowa"</span><span class="sxs-lookup"><span data-stu-id="ac552-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="ac552-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac552-110">PARAMETERS</span></span>

### <span data-ttu-id="ac552-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac552-111">-DefaultProfile</span></span>
<span data-ttu-id="ac552-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac552-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac552-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac552-113">CommonParameters</span></span>
<span data-ttu-id="ac552-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac552-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac552-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac552-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac552-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac552-116">INPUTS</span></span>

### <span data-ttu-id="ac552-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ac552-117">None</span></span>

## <span data-ttu-id="ac552-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac552-118">OUTPUTS</span></span>

### <span data-ttu-id="ac552-119">Microsoft. Azure. Commands. Network. models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="ac552-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="ac552-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac552-120">NOTES</span></span>

## <span data-ttu-id="ac552-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac552-121">RELATED LINKS</span></span>

[<span data-ttu-id="ac552-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ac552-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="ac552-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ac552-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="ac552-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ac552-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="ac552-125">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="ac552-125">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
