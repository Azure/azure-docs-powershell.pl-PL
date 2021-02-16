---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 3067df10f3cd1d49b519d6c83defe304fbcf0296
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203092"
---
# <span data-ttu-id="d39aa-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d39aa-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="d39aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d39aa-102">SYNOPSIS</span></span>
<span data-ttu-id="d39aa-103">Pobiera tabelę trasy z obwodu expressroute.</span><span class="sxs-lookup"><span data-stu-id="d39aa-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="d39aa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d39aa-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d39aa-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d39aa-105">DESCRIPTION</span></span>
<span data-ttu-id="d39aa-106">Polecenie **cmdlet Get-AzExpressRouteCircuitRouteTable** pobiera szczegółową tabelę tras obwodu expressRoute.</span><span class="sxs-lookup"><span data-stu-id="d39aa-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="d39aa-107">W tabeli tras będą wyświetlane wszystkie trasy lub można je filtrować w celu pokazania tras dla określonego typu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="d39aa-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="d39aa-108">Za pomocą tabeli trasy możesz sprawdzić konfigurację komunikacji równorzędnej i łączność.</span><span class="sxs-lookup"><span data-stu-id="d39aa-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="d39aa-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d39aa-109">EXAMPLES</span></span>

### <span data-ttu-id="d39aa-110">Przykład 1. Wyświetlanie tabeli trasy dla ścieżki podstawowej</span><span class="sxs-lookup"><span data-stu-id="d39aa-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="d39aa-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d39aa-111">PARAMETERS</span></span>

### <span data-ttu-id="d39aa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d39aa-112">-DefaultProfile</span></span>
<span data-ttu-id="d39aa-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d39aa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d39aa-114">— DevicePath</span><span class="sxs-lookup"><span data-stu-id="d39aa-114">-DevicePath</span></span>
<span data-ttu-id="d39aa-115">Dopuszczalne wartości dla tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="d39aa-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="d39aa-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="d39aa-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="d39aa-117">Nazwa sprawdzana jest nazwa obwodu aplikacji ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d39aa-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="d39aa-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="d39aa-118">-PeeringType</span></span>
<span data-ttu-id="d39aa-119">Dopuszczalne wartości dla tego parametru to: `AzurePrivatePeering` `AzurePublicPeering` , i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="d39aa-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="d39aa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d39aa-120">-ResourceGroupName</span></span>
<span data-ttu-id="d39aa-121">Nazwa grupy zasobów zawierającej obwód expressroute.</span><span class="sxs-lookup"><span data-stu-id="d39aa-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="d39aa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d39aa-122">CommonParameters</span></span>
<span data-ttu-id="d39aa-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d39aa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d39aa-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d39aa-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d39aa-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d39aa-125">INPUTS</span></span>

### <span data-ttu-id="d39aa-126">System.String</span><span class="sxs-lookup"><span data-stu-id="d39aa-126">System.String</span></span>

## <span data-ttu-id="d39aa-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d39aa-127">OUTPUTS</span></span>

### <span data-ttu-id="d39aa-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="d39aa-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="d39aa-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d39aa-129">NOTES</span></span>

## <span data-ttu-id="d39aa-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d39aa-130">RELATED LINKS</span></span>

[<span data-ttu-id="d39aa-131">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d39aa-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="d39aa-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d39aa-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="d39aa-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="d39aa-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
