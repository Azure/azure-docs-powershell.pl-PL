---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: ce3d4e42c6644cd3181ec9389a7b571c7f6ca51a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890797"
---
# <span data-ttu-id="c546a-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="c546a-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="c546a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c546a-102">SYNOPSIS</span></span>
<span data-ttu-id="c546a-103">Pobiera listę dostawców usług ExpressRoute i ich atrybuty.</span><span class="sxs-lookup"><span data-stu-id="c546a-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="c546a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c546a-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c546a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c546a-105">DESCRIPTION</span></span>
<span data-ttu-id="c546a-106">Polecenie cmdlet **Get-AzExpressRouteServiceProvider** pobiera listę dostawców usług ExpressRoute i ich atrybuty.</span><span class="sxs-lookup"><span data-stu-id="c546a-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="c546a-107">Atrybuty obejmują Opcje lokalizacji i przepustowości.</span><span class="sxs-lookup"><span data-stu-id="c546a-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="c546a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c546a-108">EXAMPLES</span></span>

### <span data-ttu-id="c546a-109">Przykład 1: uzyskiwanie listy dostawców usług z lokalizacjami w "Dolina Krzemowa"</span><span class="sxs-lookup"><span data-stu-id="c546a-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="c546a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c546a-110">PARAMETERS</span></span>

### <span data-ttu-id="c546a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c546a-111">-DefaultProfile</span></span>
<span data-ttu-id="c546a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c546a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c546a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c546a-113">CommonParameters</span></span>
<span data-ttu-id="c546a-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c546a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c546a-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c546a-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c546a-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c546a-116">INPUTS</span></span>

## <span data-ttu-id="c546a-117">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c546a-117">OUTPUTS</span></span>

### <span data-ttu-id="c546a-118">Microsoft. Azure. Commands. Network. models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="c546a-118">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="c546a-119">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c546a-119">NOTES</span></span>

## <span data-ttu-id="c546a-120">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c546a-120">RELATED LINKS</span></span>

[<span data-ttu-id="c546a-121">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c546a-121">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="c546a-122">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c546a-122">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="c546a-123">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c546a-123">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="c546a-124">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="c546a-124">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
