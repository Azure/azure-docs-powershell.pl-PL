---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9996a42311ebfdf523b12822c1550b2faa78b6b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328109"
---
# <span data-ttu-id="1101c-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1101c-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="1101c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1101c-102">SYNOPSIS</span></span>
<span data-ttu-id="1101c-103">Pobiera konfigurację komunikacji równorzędnej obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1101c-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="1101c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1101c-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1101c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1101c-105">DESCRIPTION</span></span>
<span data-ttu-id="1101c-106">Polecenie cmdlet **Get-AzExpressRouteCircuitPeeringConfig** umożliwia pobranie konfiguracji relacji komunikacji równorzędnej dla obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1101c-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="1101c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1101c-107">EXAMPLES</span></span>

### <span data-ttu-id="1101c-108">Przykład 1. Wyświetlanie konfiguracji komunikacji równorzędnej dla obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="1101c-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="1101c-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1101c-109">PARAMETERS</span></span>

### <span data-ttu-id="1101c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1101c-110">-DefaultProfile</span></span>
<span data-ttu-id="1101c-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1101c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1101c-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1101c-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="1101c-113">Obiekt obwodu ExpressRoute zawierający konfigurację komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="1101c-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="1101c-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1101c-114">-Name</span></span>
<span data-ttu-id="1101c-115">Nazwa konfiguracji elementu równorzędnego do pobrania.</span><span class="sxs-lookup"><span data-stu-id="1101c-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="1101c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1101c-116">CommonParameters</span></span>
<span data-ttu-id="1101c-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1101c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1101c-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1101c-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1101c-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1101c-119">INPUTS</span></span>

### <span data-ttu-id="1101c-120">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1101c-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="1101c-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1101c-121">OUTPUTS</span></span>

### <span data-ttu-id="1101c-122">Microsoft. Azure. Commands. Network. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="1101c-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="1101c-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1101c-123">NOTES</span></span>

## <span data-ttu-id="1101c-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1101c-124">RELATED LINKS</span></span>

[<span data-ttu-id="1101c-125">Dodaj-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1101c-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="1101c-126">Nowe — AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1101c-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="1101c-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1101c-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="1101c-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1101c-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
