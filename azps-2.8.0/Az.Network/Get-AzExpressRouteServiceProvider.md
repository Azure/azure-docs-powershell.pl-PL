---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 4017d9eba94f82b235b5016145ee0692ff56892c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410773"
---
# <span data-ttu-id="be5bb-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="be5bb-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="be5bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be5bb-102">SYNOPSIS</span></span>
<span data-ttu-id="be5bb-103">Pobiera listę dostawców usług ExpressRoute i ich atrybuty.</span><span class="sxs-lookup"><span data-stu-id="be5bb-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="be5bb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="be5bb-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be5bb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="be5bb-105">DESCRIPTION</span></span>
<span data-ttu-id="be5bb-106">Polecenie **cmdlet Get-AzExpressRouteServiceProvider** pobiera listę dostawców usług ExpressRoute i ich atrybuty.</span><span class="sxs-lookup"><span data-stu-id="be5bb-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="be5bb-107">Atrybut obejmuje opcje lokalizacji i przepustowości.</span><span class="sxs-lookup"><span data-stu-id="be5bb-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="be5bb-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="be5bb-108">EXAMPLES</span></span>

### <span data-ttu-id="be5bb-109">Przykład 1. Uzyskiwanie listy lokalizacji w usługodawca "Dolina Krzemowa"</span><span class="sxs-lookup"><span data-stu-id="be5bb-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="be5bb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be5bb-110">PARAMETERS</span></span>

### <span data-ttu-id="be5bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be5bb-111">-DefaultProfile</span></span>
<span data-ttu-id="be5bb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="be5bb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be5bb-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be5bb-113">CommonParameters</span></span>
<span data-ttu-id="be5bb-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be5bb-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be5bb-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be5bb-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be5bb-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be5bb-116">INPUTS</span></span>

### <span data-ttu-id="be5bb-117">Brak</span><span class="sxs-lookup"><span data-stu-id="be5bb-117">None</span></span>

## <span data-ttu-id="be5bb-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be5bb-118">OUTPUTS</span></span>

### <span data-ttu-id="be5bb-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="be5bb-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="be5bb-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="be5bb-120">NOTES</span></span>

## <span data-ttu-id="be5bb-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be5bb-121">RELATED LINKS</span></span>

[<span data-ttu-id="be5bb-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="be5bb-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="be5bb-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="be5bb-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="be5bb-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="be5bb-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="be5bb-125">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="be5bb-125">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
