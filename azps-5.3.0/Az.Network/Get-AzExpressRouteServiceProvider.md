---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 5e0464a4266a68905da26859f20faca918a9caab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500658"
---
# <span data-ttu-id="10bd0-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="10bd0-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="10bd0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="10bd0-103">Pobiera listę dostawców usług ExpressRoute i ich atrybuty.</span><span class="sxs-lookup"><span data-stu-id="10bd0-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="10bd0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10bd0-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10bd0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="10bd0-105">DESCRIPTION</span></span>
<span data-ttu-id="10bd0-106">Polecenie cmdlet **Get-AzExpressRouteServiceProvider** pobiera listę dostawców usług ExpressRoute i ich atrybuty.</span><span class="sxs-lookup"><span data-stu-id="10bd0-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="10bd0-107">Atrybuty obejmują Opcje lokalizacji i przepustowości.</span><span class="sxs-lookup"><span data-stu-id="10bd0-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="10bd0-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10bd0-108">EXAMPLES</span></span>

### <span data-ttu-id="10bd0-109">Przykład 1: uzyskiwanie listy dostawców usług z lokalizacjami w "Dolina Krzemowa"</span><span class="sxs-lookup"><span data-stu-id="10bd0-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="10bd0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10bd0-110">PARAMETERS</span></span>

### <span data-ttu-id="10bd0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10bd0-111">-DefaultProfile</span></span>
<span data-ttu-id="10bd0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="10bd0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10bd0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10bd0-113">CommonParameters</span></span>
<span data-ttu-id="10bd0-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10bd0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10bd0-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10bd0-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10bd0-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10bd0-116">INPUTS</span></span>

### <span data-ttu-id="10bd0-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="10bd0-117">None</span></span>

## <span data-ttu-id="10bd0-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10bd0-118">OUTPUTS</span></span>

### <span data-ttu-id="10bd0-119">Microsoft. Azure. Commands. Network. models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="10bd0-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="10bd0-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10bd0-120">NOTES</span></span>

## <span data-ttu-id="10bd0-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10bd0-121">RELATED LINKS</span></span>

[<span data-ttu-id="10bd0-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="10bd0-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="10bd0-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="10bd0-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="10bd0-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="10bd0-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="10bd0-125">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="10bd0-125">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
