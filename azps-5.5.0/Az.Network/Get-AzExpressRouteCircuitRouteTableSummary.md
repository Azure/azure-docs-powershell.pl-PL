---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 0004d43d802e89da51035727aae258181e38b00e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193891"
---
# <span data-ttu-id="27a71-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="27a71-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="27a71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27a71-102">SYNOPSIS</span></span>
<span data-ttu-id="27a71-103">Pobiera podsumowanie tabeli trasy obwodu expressRoute.</span><span class="sxs-lookup"><span data-stu-id="27a71-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="27a71-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="27a71-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27a71-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="27a71-105">DESCRIPTION</span></span>
<span data-ttu-id="27a71-106">Polecenie **cmdlet Get-AzExpressRouteCircuitRouteTableSummary** pobiera podsumowanie informacji sąsiadów BGP dla określonego kontekstu routingu.</span><span class="sxs-lookup"><span data-stu-id="27a71-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="27a71-107">Te informacje przydają się do określenia, jak długo został ustalony kontekst routingu i ile prefiksów trasy anonsuje router komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="27a71-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="27a71-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="27a71-108">EXAMPLES</span></span>

### <span data-ttu-id="27a71-109">Przykład 1. Wyświetlanie podsumowania trasy ścieżki podstawowej</span><span class="sxs-lookup"><span data-stu-id="27a71-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="27a71-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27a71-110">PARAMETERS</span></span>

### <span data-ttu-id="27a71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a71-111">-DefaultProfile</span></span>
<span data-ttu-id="27a71-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="27a71-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27a71-113">— DevicePath</span><span class="sxs-lookup"><span data-stu-id="27a71-113">-DevicePath</span></span>
<span data-ttu-id="27a71-114">Dopuszczalne wartości dla tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="27a71-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="27a71-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="27a71-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="27a71-116">Nazwa sprawdzana jest nazwa obwodu w układzie ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="27a71-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="27a71-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="27a71-117">-PeeringType</span></span>
<span data-ttu-id="27a71-118">Dopuszczalne wartości dla tego parametru to: `AzurePrivatePeering` `AzurePublicPeering` , i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="27a71-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="27a71-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27a71-119">-ResourceGroupName</span></span>
<span data-ttu-id="27a71-120">Nazwa grupy zasobów zawierającej obwód expressroute.</span><span class="sxs-lookup"><span data-stu-id="27a71-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="27a71-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a71-121">CommonParameters</span></span>
<span data-ttu-id="27a71-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27a71-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a71-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27a71-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a71-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27a71-124">INPUTS</span></span>

### <span data-ttu-id="27a71-125">System.String</span><span class="sxs-lookup"><span data-stu-id="27a71-125">System.String</span></span>

## <span data-ttu-id="27a71-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27a71-126">OUTPUTS</span></span>

### <span data-ttu-id="27a71-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="27a71-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="27a71-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="27a71-128">NOTES</span></span>

## <span data-ttu-id="27a71-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27a71-129">RELATED LINKS</span></span>

[<span data-ttu-id="27a71-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="27a71-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="27a71-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="27a71-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="27a71-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="27a71-132">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
