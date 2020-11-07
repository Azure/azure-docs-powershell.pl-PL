---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetablesummary
schema: 2.0.0
ms.openlocfilehash: bf358159ef7f8895fa2f801435716ac13635a5d6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897954"
---
# <span data-ttu-id="c759b-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c759b-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="c759b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c759b-102">SYNOPSIS</span></span>
<span data-ttu-id="c759b-103">Pobiera podsumowanie tabeli tras obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c759b-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c759b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c759b-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c759b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c759b-105">DESCRIPTION</span></span>
<span data-ttu-id="c759b-106">Polecenie cmdlet **Get-AzureRmExpressRouteCircuitRouteTableSummary** pobiera podsumowanie informacji o sąsiadach BGP dla określonego kontekstu routingu.</span><span class="sxs-lookup"><span data-stu-id="c759b-106">The **Get-AzureRmExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="c759b-107">Te informacje są przydatne do określenia, jak długo został ustanowiony kontekst routingu oraz ile prefiksów trasy anonsowanych przez router równorzędny.</span><span class="sxs-lookup"><span data-stu-id="c759b-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="c759b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c759b-108">EXAMPLES</span></span>

### <span data-ttu-id="c759b-109">Przykład 1. Wyświetl podsumowanie trasy dla ścieżki podstawowej</span><span class="sxs-lookup"><span data-stu-id="c759b-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="c759b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c759b-110">PARAMETERS</span></span>

### <span data-ttu-id="c759b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c759b-111">-DefaultProfile</span></span>
<span data-ttu-id="c759b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c759b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c759b-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="c759b-113">-DevicePath</span></span>
<span data-ttu-id="c759b-114">Dopuszczalne wartości tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="c759b-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: DevicePathEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c759b-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="c759b-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="c759b-116">Nazwa badanego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c759b-116">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c759b-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="c759b-117">-PeeringType</span></span>
<span data-ttu-id="c759b-118">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="c759b-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c759b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c759b-119">-ResourceGroupName</span></span>
<span data-ttu-id="c759b-120">Nazwa grupy zasobów zawierającej obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c759b-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c759b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c759b-121">CommonParameters</span></span>
<span data-ttu-id="c759b-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c759b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c759b-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c759b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c759b-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c759b-124">INPUTS</span></span>

## <span data-ttu-id="c759b-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c759b-125">OUTPUTS</span></span>

### <span data-ttu-id="c759b-126">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="c759b-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="c759b-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c759b-127">NOTES</span></span>

## <span data-ttu-id="c759b-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c759b-128">RELATED LINKS</span></span>

[<span data-ttu-id="c759b-129">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c759b-129">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="c759b-130">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c759b-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="c759b-131">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="c759b-131">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
