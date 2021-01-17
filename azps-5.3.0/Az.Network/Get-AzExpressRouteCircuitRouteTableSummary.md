---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 0004d43d802e89da51035727aae258181e38b00e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489938"
---
# <span data-ttu-id="56e32-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="56e32-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="56e32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56e32-102">SYNOPSIS</span></span>
<span data-ttu-id="56e32-103">Pobiera podsumowanie tabeli tras obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="56e32-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="56e32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56e32-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56e32-105">Opis</span><span class="sxs-lookup"><span data-stu-id="56e32-105">DESCRIPTION</span></span>
<span data-ttu-id="56e32-106">Polecenie cmdlet **Get-AzExpressRouteCircuitRouteTableSummary** pobiera podsumowanie informacji o sąsiadach BGP dla określonego kontekstu routingu.</span><span class="sxs-lookup"><span data-stu-id="56e32-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="56e32-107">Te informacje są przydatne do określenia, jak długo został ustanowiony kontekst routingu oraz ile prefiksów trasy anonsowanych przez router równorzędny.</span><span class="sxs-lookup"><span data-stu-id="56e32-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="56e32-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56e32-108">EXAMPLES</span></span>

### <span data-ttu-id="56e32-109">Przykład 1. Wyświetl podsumowanie trasy dla ścieżki podstawowej</span><span class="sxs-lookup"><span data-stu-id="56e32-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="56e32-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56e32-110">PARAMETERS</span></span>

### <span data-ttu-id="56e32-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e32-111">-DefaultProfile</span></span>
<span data-ttu-id="56e32-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56e32-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56e32-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="56e32-113">-DevicePath</span></span>
<span data-ttu-id="56e32-114">Dopuszczalne wartości tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="56e32-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="56e32-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="56e32-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="56e32-116">Nazwa badanego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="56e32-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="56e32-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="56e32-117">-PeeringType</span></span>
<span data-ttu-id="56e32-118">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="56e32-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="56e32-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56e32-119">-ResourceGroupName</span></span>
<span data-ttu-id="56e32-120">Nazwa grupy zasobów zawierającej obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="56e32-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="56e32-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e32-121">CommonParameters</span></span>
<span data-ttu-id="56e32-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56e32-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e32-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56e32-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e32-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56e32-124">INPUTS</span></span>

### <span data-ttu-id="56e32-125">System. String</span><span class="sxs-lookup"><span data-stu-id="56e32-125">System.String</span></span>

## <span data-ttu-id="56e32-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56e32-126">OUTPUTS</span></span>

### <span data-ttu-id="56e32-127">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="56e32-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="56e32-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56e32-128">NOTES</span></span>

## <span data-ttu-id="56e32-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56e32-129">RELATED LINKS</span></span>

[<span data-ttu-id="56e32-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="56e32-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="56e32-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="56e32-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="56e32-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="56e32-132">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
