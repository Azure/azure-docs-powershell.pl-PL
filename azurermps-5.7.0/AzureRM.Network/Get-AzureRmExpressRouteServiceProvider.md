---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
ms.openlocfilehash: d8d5abedd0deaf5af341995552ad72bef4703058
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716620"
---
# <span data-ttu-id="d89ab-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="d89ab-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="d89ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d89ab-102">SYNOPSIS</span></span>
<span data-ttu-id="d89ab-103">Pobiera listę dostawców usług ExpressRoute i ich atrybuty.</span><span class="sxs-lookup"><span data-stu-id="d89ab-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d89ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d89ab-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d89ab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d89ab-105">DESCRIPTION</span></span>
<span data-ttu-id="d89ab-106">Polecenie cmdlet **Get-AzureRmExpressRouteServiceProvider** pobiera listę dostawców usług ExpressRoute i ich atrybuty.</span><span class="sxs-lookup"><span data-stu-id="d89ab-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="d89ab-107">Atrybuty obejmują Opcje lokalizacji i przepustowości.</span><span class="sxs-lookup"><span data-stu-id="d89ab-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="d89ab-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d89ab-108">EXAMPLES</span></span>

### <span data-ttu-id="d89ab-109">Przykład 1: uzyskiwanie listy dostawców usług z lokalizacjami w "Dolina Krzemowa"</span><span class="sxs-lookup"><span data-stu-id="d89ab-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="d89ab-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d89ab-110">PARAMETERS</span></span>

### <span data-ttu-id="d89ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d89ab-111">-DefaultProfile</span></span>
<span data-ttu-id="d89ab-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d89ab-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d89ab-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d89ab-113">CommonParameters</span></span>
<span data-ttu-id="d89ab-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d89ab-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d89ab-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d89ab-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d89ab-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d89ab-116">INPUTS</span></span>

### <span data-ttu-id="d89ab-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d89ab-117">None</span></span>
<span data-ttu-id="d89ab-118">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d89ab-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d89ab-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d89ab-119">OUTPUTS</span></span>

### <span data-ttu-id="d89ab-120">Microsoft. Azure. Commands. Network. models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="d89ab-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="d89ab-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d89ab-121">NOTES</span></span>

## <span data-ttu-id="d89ab-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d89ab-122">RELATED LINKS</span></span>

[<span data-ttu-id="d89ab-123">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d89ab-123">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="d89ab-124">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d89ab-124">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="d89ab-125">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d89ab-125">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="d89ab-126">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="d89ab-126">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
