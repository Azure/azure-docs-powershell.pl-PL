---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 187921598b21747764436dd4ae6f988961d4a951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996402"
---
# <span data-ttu-id="4b322-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4b322-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="4b322-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b322-102">SYNOPSIS</span></span>
<span data-ttu-id="4b322-103">Usuwa konfigurację komunikacji równorzędnej obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4b322-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="4b322-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4b322-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b322-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4b322-105">DESCRIPTION</span></span>
<span data-ttu-id="4b322-106">Polecenie **cmdlet Remove-AzExpressRouteCircuitPeeringConfig** usuwa konfigurację komunikacji równorzędnej obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4b322-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="4b322-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4b322-107">EXAMPLES</span></span>

### <span data-ttu-id="4b322-108">Przykład 1. Usuwanie konfiguracji komunikacji równorzędnej z obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="4b322-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="4b322-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b322-109">PARAMETERS</span></span>

### <span data-ttu-id="4b322-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b322-110">-DefaultProfile</span></span>
<span data-ttu-id="4b322-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4b322-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b322-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4b322-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4b322-113">Obwód usługi ExpressRoute zawierający konfigurację komunikacji równorzędnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="4b322-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="4b322-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4b322-114">-Name</span></span>
<span data-ttu-id="4b322-115">Nazwa konfiguracji komunikacji równorzędnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="4b322-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="4b322-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="4b322-116">-PeerAddressType</span></span>
<span data-ttu-id="4b322-117">Rodzina adresów komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="4b322-117">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b322-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b322-118">CommonParameters</span></span>
<span data-ttu-id="4b322-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b322-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b322-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b322-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b322-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b322-121">INPUTS</span></span>

### <span data-ttu-id="4b322-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4b322-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4b322-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b322-123">OUTPUTS</span></span>

### <span data-ttu-id="4b322-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4b322-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4b322-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4b322-125">NOTES</span></span>

## <span data-ttu-id="4b322-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b322-126">RELATED LINKS</span></span>

[<span data-ttu-id="4b322-127">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4b322-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4b322-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4b322-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="4b322-129">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4b322-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4b322-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4b322-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
