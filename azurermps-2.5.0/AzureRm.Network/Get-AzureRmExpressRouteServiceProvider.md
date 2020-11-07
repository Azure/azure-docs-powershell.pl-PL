---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
ms.openlocfilehash: 7e4febe620b8a440d1f9a5eb0c9432da9ff47c74
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898369"
---
# <span data-ttu-id="a23fe-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="a23fe-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="a23fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a23fe-102">SYNOPSIS</span></span>
<span data-ttu-id="a23fe-103">Pobiera listę dostawców usług ExpressRoute i ich atrybuty.</span><span class="sxs-lookup"><span data-stu-id="a23fe-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a23fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a23fe-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a23fe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a23fe-105">DESCRIPTION</span></span>
<span data-ttu-id="a23fe-106">Polecenie cmdlet **Get-AzureRmExpressRouteServiceProvider** pobiera listę dostawców usług ExpressRoute i ich atrybuty.</span><span class="sxs-lookup"><span data-stu-id="a23fe-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="a23fe-107">Atrybuty obejmują Opcje lokalizacji i przepustowości.</span><span class="sxs-lookup"><span data-stu-id="a23fe-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="a23fe-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a23fe-108">EXAMPLES</span></span>

### <span data-ttu-id="a23fe-109">Przykład 1: uzyskiwanie listy dostawców usług z lokalizacjami w "Dolina Krzemowa"</span><span class="sxs-lookup"><span data-stu-id="a23fe-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="a23fe-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a23fe-110">PARAMETERS</span></span>

### <span data-ttu-id="a23fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a23fe-111">-DefaultProfile</span></span>
<span data-ttu-id="a23fe-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a23fe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a23fe-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a23fe-113">CommonParameters</span></span>
<span data-ttu-id="a23fe-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a23fe-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a23fe-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a23fe-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a23fe-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a23fe-116">INPUTS</span></span>

## <span data-ttu-id="a23fe-117">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a23fe-117">OUTPUTS</span></span>

### <span data-ttu-id="a23fe-118">Microsoft. Azure. Commands. Network. models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="a23fe-118">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="a23fe-119">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a23fe-119">NOTES</span></span>

## <span data-ttu-id="a23fe-120">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a23fe-120">RELATED LINKS</span></span>

[<span data-ttu-id="a23fe-121">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a23fe-121">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="a23fe-122">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a23fe-122">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="a23fe-123">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a23fe-123">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="a23fe-124">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="a23fe-124">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
