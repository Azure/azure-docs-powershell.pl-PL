---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 7da632a1496b22e2f0be183640995a2aaa96735e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007786"
---
# <span data-ttu-id="fe7a2-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="fe7a2-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="fe7a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe7a2-102">SYNOPSIS</span></span>
<span data-ttu-id="fe7a2-103">Pobiera konfigurację komunikacji równorzędnej obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fe7a2-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="fe7a2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe7a2-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe7a2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe7a2-105">DESCRIPTION</span></span>
<span data-ttu-id="fe7a2-106">Polecenie **cmdlet Get-AzExpressRouteCircuitPeeringConfig** pobiera konfigurację relacji komunikacji równorzędnej dla obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fe7a2-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="fe7a2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe7a2-107">EXAMPLES</span></span>

### <span data-ttu-id="fe7a2-108">Przykład 1. Wyświetlanie konfiguracji komunikacji równorzędnej dla obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="fe7a2-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="fe7a2-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe7a2-109">PARAMETERS</span></span>

### <span data-ttu-id="fe7a2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe7a2-110">-DefaultProfile</span></span>
<span data-ttu-id="fe7a2-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe7a2-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe7a2-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fe7a2-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="fe7a2-113">Obiekt obwodu usługi ExpressRoute zawierający konfigurację komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="fe7a2-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe7a2-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fe7a2-114">-Name</span></span>
<span data-ttu-id="fe7a2-115">Nazwa konfiguracji komunikacji równorzędnej do pobrania.</span><span class="sxs-lookup"><span data-stu-id="fe7a2-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe7a2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe7a2-116">CommonParameters</span></span>
<span data-ttu-id="fe7a2-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe7a2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe7a2-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe7a2-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe7a2-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe7a2-119">INPUTS</span></span>

### <span data-ttu-id="fe7a2-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fe7a2-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="fe7a2-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe7a2-121">OUTPUTS</span></span>

### <span data-ttu-id="fe7a2-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="fe7a2-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="fe7a2-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe7a2-123">NOTES</span></span>

## <span data-ttu-id="fe7a2-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe7a2-124">RELATED LINKS</span></span>

[<span data-ttu-id="fe7a2-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="fe7a2-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="fe7a2-126">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="fe7a2-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="fe7a2-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="fe7a2-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="fe7a2-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fe7a2-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
