---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: aa3d229ec14118b87c960e234a00cf82f85754c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719097"
---
# <span data-ttu-id="c00c2-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c00c2-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="c00c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c00c2-102">SYNOPSIS</span></span>
<span data-ttu-id="c00c2-103">Pobiera podsumowanie tabeli tras obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c00c2-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c00c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c00c2-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c00c2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c00c2-105">DESCRIPTION</span></span>
<span data-ttu-id="c00c2-106">Polecenie cmdlet **Get-AzureRmExpressRouteCircuitRouteTableSummary** pobiera podsumowanie informacji o sąsiadach BGP dla określonego kontekstu routingu.</span><span class="sxs-lookup"><span data-stu-id="c00c2-106">The **Get-AzureRmExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="c00c2-107">Te informacje są przydatne do określenia, jak długo został ustanowiony kontekst routingu oraz ile prefiksów trasy anonsowanych przez router równorzędny.</span><span class="sxs-lookup"><span data-stu-id="c00c2-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="c00c2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c00c2-108">EXAMPLES</span></span>

### <span data-ttu-id="c00c2-109">Przykład 1. Wyświetl podsumowanie trasy dla ścieżki podstawowej</span><span class="sxs-lookup"><span data-stu-id="c00c2-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="c00c2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c00c2-110">PARAMETERS</span></span>

### <span data-ttu-id="c00c2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c00c2-111">-DefaultProfile</span></span>
<span data-ttu-id="c00c2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c00c2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c00c2-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="c00c2-113">-DevicePath</span></span>
<span data-ttu-id="c00c2-114">Dopuszczalne wartości tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="c00c2-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00c2-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="c00c2-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="c00c2-116">Nazwa badanego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c00c2-116">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c00c2-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="c00c2-117">-PeeringType</span></span>
<span data-ttu-id="c00c2-118">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="c00c2-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00c2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c00c2-119">-ResourceGroupName</span></span>
<span data-ttu-id="c00c2-120">Nazwa grupy zasobów zawierającej obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c00c2-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="c00c2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c00c2-121">CommonParameters</span></span>
<span data-ttu-id="c00c2-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c00c2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c00c2-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c00c2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c00c2-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c00c2-124">INPUTS</span></span>

### <span data-ttu-id="c00c2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c00c2-125">System.String</span></span>

## <span data-ttu-id="c00c2-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c00c2-126">OUTPUTS</span></span>

### <span data-ttu-id="c00c2-127">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="c00c2-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="c00c2-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c00c2-128">NOTES</span></span>

## <span data-ttu-id="c00c2-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c00c2-129">RELATED LINKS</span></span>

[<span data-ttu-id="c00c2-130">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c00c2-130">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="c00c2-131">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c00c2-131">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="c00c2-132">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="c00c2-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)