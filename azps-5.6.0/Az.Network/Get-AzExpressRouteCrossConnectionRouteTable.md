---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: c92033fa0ed907aab4c36f7dd980fb977a47be73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979601"
---
# <span data-ttu-id="a272e-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a272e-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="a272e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a272e-102">SYNOPSIS</span></span>
<span data-ttu-id="a272e-103">Pobiera tabelę trasy z połączenia krzyżowego expressRoute.</span><span class="sxs-lookup"><span data-stu-id="a272e-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="a272e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a272e-104">SYNTAX</span></span>

### <span data-ttu-id="a272e-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="a272e-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a272e-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="a272e-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a272e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a272e-107">DESCRIPTION</span></span>
<span data-ttu-id="a272e-108">Polecenie **cmdlet Get-AzExpressRouteCrossConnectionRouteTable** pobiera szczegółową tabelę tras obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a272e-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="a272e-109">W tabeli tras będą wyświetlane wszystkie trasy lub można je filtrować w celu pokazania tras dla określonego typu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="a272e-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="a272e-110">Za pomocą tabeli trasy możesz sprawdzić konfigurację komunikacji równorzędnej i łączność.</span><span class="sxs-lookup"><span data-stu-id="a272e-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="a272e-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a272e-111">EXAMPLES</span></span>

### <span data-ttu-id="a272e-112">Przykład 1. Wyświetlanie tabeli trasy dla ścieżki podstawowej</span><span class="sxs-lookup"><span data-stu-id="a272e-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="a272e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a272e-113">PARAMETERS</span></span>

### <span data-ttu-id="a272e-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="a272e-114">-CrossConnectionName</span></span>
<span data-ttu-id="a272e-115">Nazwa połączenia krzyżowego trasy ekspresowej</span><span class="sxs-lookup"><span data-stu-id="a272e-115">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a272e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a272e-116">-DefaultProfile</span></span>
<span data-ttu-id="a272e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a272e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a272e-118">— DevicePath</span><span class="sxs-lookup"><span data-stu-id="a272e-118">-DevicePath</span></span>
<span data-ttu-id="a272e-119">Dopuszczalne wartości dla tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="a272e-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="a272e-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a272e-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="a272e-121">Połączenie krzyżowe trasy ekspresowej</span><span class="sxs-lookup"><span data-stu-id="a272e-121">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a272e-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a272e-122">-PeeringType</span></span>
<span data-ttu-id="a272e-123">Dopuszczalne wartości dla tego parametru to: `AzurePrivatePeering` `AzurePublicPeering` , i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a272e-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="a272e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a272e-124">-ResourceGroupName</span></span>
<span data-ttu-id="a272e-125">Nazwa grupy zasobów zawierającej połączenie krzyżowe expressRoute.</span><span class="sxs-lookup"><span data-stu-id="a272e-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a272e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a272e-126">CommonParameters</span></span>
<span data-ttu-id="a272e-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a272e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a272e-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a272e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a272e-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a272e-129">INPUTS</span></span>

### <span data-ttu-id="a272e-130">Brak</span><span class="sxs-lookup"><span data-stu-id="a272e-130">None</span></span>
<span data-ttu-id="a272e-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a272e-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a272e-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a272e-132">OUTPUTS</span></span>

### <span data-ttu-id="a272e-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="a272e-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="a272e-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a272e-134">NOTES</span></span>

## <span data-ttu-id="a272e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a272e-135">RELATED LINKS</span></span>

[<span data-ttu-id="a272e-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="a272e-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="a272e-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a272e-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
