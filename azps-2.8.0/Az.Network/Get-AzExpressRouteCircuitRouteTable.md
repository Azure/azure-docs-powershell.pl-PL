---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: c7b4f51e868522533756534b52fd0b0cf5c17f0c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401287"
---
# <span data-ttu-id="02608-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="02608-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="02608-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02608-102">SYNOPSIS</span></span>
<span data-ttu-id="02608-103">Pobiera tabelę trasy z obwodu expressroute.</span><span class="sxs-lookup"><span data-stu-id="02608-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="02608-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="02608-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02608-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="02608-105">DESCRIPTION</span></span>
<span data-ttu-id="02608-106">Polecenie **cmdlet Get-AzExpressRouteCircuitRouteTable** pobiera szczegółową tabelę tras obwodu expressRoute.</span><span class="sxs-lookup"><span data-stu-id="02608-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="02608-107">W tabeli tras będą wyświetlane wszystkie trasy lub można je filtrować w celu pokazania tras dla określonego typu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="02608-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="02608-108">Za pomocą tabeli trasy możesz sprawdzić konfigurację komunikacji równorzędnej i łączność.</span><span class="sxs-lookup"><span data-stu-id="02608-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="02608-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="02608-109">EXAMPLES</span></span>

### <span data-ttu-id="02608-110">Przykład 1. Wyświetlanie tabeli trasy dla ścieżki podstawowej</span><span class="sxs-lookup"><span data-stu-id="02608-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="02608-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02608-111">PARAMETERS</span></span>

### <span data-ttu-id="02608-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02608-112">-DefaultProfile</span></span>
<span data-ttu-id="02608-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="02608-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02608-114">— DevicePath</span><span class="sxs-lookup"><span data-stu-id="02608-114">-DevicePath</span></span>
<span data-ttu-id="02608-115">Dopuszczalne wartości dla tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="02608-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="02608-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="02608-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="02608-117">Nazwa sprawdzana jest nazwa obwodu w układzie ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="02608-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="02608-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="02608-118">-PeeringType</span></span>
<span data-ttu-id="02608-119">Dopuszczalne wartości dla tego parametru to: `AzurePrivatePeering` `AzurePublicPeering` , i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="02608-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="02608-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02608-120">-ResourceGroupName</span></span>
<span data-ttu-id="02608-121">Nazwa grupy zasobów zawierającej obwód expressroute.</span><span class="sxs-lookup"><span data-stu-id="02608-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="02608-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02608-122">CommonParameters</span></span>
<span data-ttu-id="02608-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02608-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02608-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02608-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02608-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02608-125">INPUTS</span></span>

### <span data-ttu-id="02608-126">System.String</span><span class="sxs-lookup"><span data-stu-id="02608-126">System.String</span></span>

## <span data-ttu-id="02608-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02608-127">OUTPUTS</span></span>

### <span data-ttu-id="02608-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="02608-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="02608-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="02608-129">NOTES</span></span>

## <span data-ttu-id="02608-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02608-130">RELATED LINKS</span></span>

[<span data-ttu-id="02608-131">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="02608-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="02608-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="02608-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="02608-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="02608-133">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
