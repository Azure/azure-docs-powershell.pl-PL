---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: 4c93528c8cf89d64dd99640ce9eca4668d4093c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187186"
---
# <span data-ttu-id="d76fe-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="d76fe-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="d76fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d76fe-102">SYNOPSIS</span></span>
<span data-ttu-id="d76fe-103">Pobiera tabelę trasy z połączenia krzyżowego expressRoute.</span><span class="sxs-lookup"><span data-stu-id="d76fe-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="d76fe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d76fe-104">SYNTAX</span></span>

### <span data-ttu-id="d76fe-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="d76fe-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d76fe-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="d76fe-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d76fe-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d76fe-107">DESCRIPTION</span></span>
<span data-ttu-id="d76fe-108">Polecenie **cmdlet Get-AzExpressRouteCrossConnectionRouteTable** pobiera szczegółową tabelę tras obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d76fe-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="d76fe-109">W tabeli tras będą wyświetlane wszystkie trasy lub można je filtrować w celu pokazania tras dla określonego typu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="d76fe-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="d76fe-110">Za pomocą tabeli trasy możesz sprawdzić konfigurację komunikacji równorzędnej i łączność.</span><span class="sxs-lookup"><span data-stu-id="d76fe-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="d76fe-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d76fe-111">EXAMPLES</span></span>

### <span data-ttu-id="d76fe-112">Przykład 1. Wyświetlanie tabeli trasy dla ścieżki podstawowej</span><span class="sxs-lookup"><span data-stu-id="d76fe-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="d76fe-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d76fe-113">PARAMETERS</span></span>

### <span data-ttu-id="d76fe-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="d76fe-114">-CrossConnectionName</span></span>
<span data-ttu-id="d76fe-115">Nazwa połączenia krzyżowego trasy ekspresowej</span><span class="sxs-lookup"><span data-stu-id="d76fe-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="d76fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d76fe-116">-DefaultProfile</span></span>
<span data-ttu-id="d76fe-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d76fe-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d76fe-118">— DevicePath</span><span class="sxs-lookup"><span data-stu-id="d76fe-118">-DevicePath</span></span>
<span data-ttu-id="d76fe-119">Dopuszczalne wartości dla tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="d76fe-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="d76fe-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d76fe-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="d76fe-121">Połączenie krzyżowe trasy ekspresowej</span><span class="sxs-lookup"><span data-stu-id="d76fe-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="d76fe-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="d76fe-122">-PeeringType</span></span>
<span data-ttu-id="d76fe-123">Dopuszczalne wartości dla tego parametru to: `AzurePrivatePeering` `AzurePublicPeering` , i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="d76fe-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="d76fe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d76fe-124">-ResourceGroupName</span></span>
<span data-ttu-id="d76fe-125">Nazwa grupy zasobów zawierającej połączenie krzyżowe expressRoute.</span><span class="sxs-lookup"><span data-stu-id="d76fe-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="d76fe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d76fe-126">CommonParameters</span></span>
<span data-ttu-id="d76fe-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d76fe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d76fe-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d76fe-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d76fe-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d76fe-129">INPUTS</span></span>

### <span data-ttu-id="d76fe-130">Brak</span><span class="sxs-lookup"><span data-stu-id="d76fe-130">None</span></span>
<span data-ttu-id="d76fe-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d76fe-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d76fe-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d76fe-132">OUTPUTS</span></span>

### <span data-ttu-id="d76fe-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="d76fe-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="d76fe-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d76fe-134">NOTES</span></span>

## <span data-ttu-id="d76fe-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d76fe-135">RELATED LINKS</span></span>

[<span data-ttu-id="d76fe-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="d76fe-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="d76fe-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d76fe-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
