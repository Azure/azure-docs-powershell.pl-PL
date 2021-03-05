---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: e0f4b24581860f17024c9b01e62b3c84616c6f81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997732"
---
# <span data-ttu-id="5a888-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="5a888-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="5a888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a888-102">SYNOPSIS</span></span>
<span data-ttu-id="5a888-103">Pobiera statystyki użycia obwodu expressroute.</span><span class="sxs-lookup"><span data-stu-id="5a888-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="5a888-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a888-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a888-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a888-105">DESCRIPTION</span></span>
<span data-ttu-id="5a888-106">Polecenie **cmdlet Get-AzExpressRouteCircuitStat** pobiera statystyki ruchu dla obwodu expressRoute.</span><span class="sxs-lookup"><span data-stu-id="5a888-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="5a888-107">Statystyki obejmują liczbę wysłanych i odebranych bajtów zarówno tras podstawowych, jak i pomocniczych.</span><span class="sxs-lookup"><span data-stu-id="5a888-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="5a888-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a888-108">EXAMPLES</span></span>

### <span data-ttu-id="5a888-109">Przykład 1. Wyświetlanie statystyk ruchu dla elementu równorzędnego expressRoute</span><span class="sxs-lookup"><span data-stu-id="5a888-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="5a888-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a888-110">PARAMETERS</span></span>

### <span data-ttu-id="5a888-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a888-111">-DefaultProfile</span></span>
<span data-ttu-id="5a888-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a888-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a888-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="5a888-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="5a888-114">Nazwa sprawdzana jest nazwa obwodu w układzie ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5a888-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="5a888-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="5a888-115">-PeeringType</span></span>
<span data-ttu-id="5a888-116">Dopuszczalne wartości dla tego parametru to: `AzurePrivatePeering` `AzurePublicPeering` , i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="5a888-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a888-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a888-117">-ResourceGroupName</span></span>
<span data-ttu-id="5a888-118">Nazwa grupy zasobów zawierającej obwód expressroute.</span><span class="sxs-lookup"><span data-stu-id="5a888-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="5a888-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a888-119">CommonParameters</span></span>
<span data-ttu-id="5a888-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a888-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a888-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a888-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a888-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a888-122">INPUTS</span></span>

### <span data-ttu-id="5a888-123">System.String</span><span class="sxs-lookup"><span data-stu-id="5a888-123">System.String</span></span>

## <span data-ttu-id="5a888-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a888-124">OUTPUTS</span></span>

### <span data-ttu-id="5a888-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="5a888-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="5a888-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a888-126">NOTES</span></span>

## <span data-ttu-id="5a888-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a888-127">RELATED LINKS</span></span>

[<span data-ttu-id="5a888-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="5a888-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="5a888-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="5a888-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="5a888-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5a888-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
