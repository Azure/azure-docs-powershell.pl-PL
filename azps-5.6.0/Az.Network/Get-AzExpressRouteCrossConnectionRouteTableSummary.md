---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: d5b6d1b9e5d3955b7ecbff9dec02405e030bbf33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979594"
---
# <span data-ttu-id="8406b-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8406b-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="8406b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8406b-102">SYNOPSIS</span></span>
<span data-ttu-id="8406b-103">Pobiera podsumowanie tabeli trasy dla połączenia krzyżowego expressRoute.</span><span class="sxs-lookup"><span data-stu-id="8406b-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="8406b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8406b-104">SYNTAX</span></span>

### <span data-ttu-id="8406b-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="8406b-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8406b-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="8406b-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8406b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8406b-107">DESCRIPTION</span></span>
<span data-ttu-id="8406b-108">Polecenie **cmdlet Get-AzExpressRouteCrossConnectionRouteTableSummary** pobiera podsumowanie informacji o sąsiadach BGP dla określonego kontekstu routingu.</span><span class="sxs-lookup"><span data-stu-id="8406b-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="8406b-109">Te informacje są przydatne do określenia, jak długo został ustalony kontekst routingu i liczba prefiksów tras ogłaszanych przez router komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="8406b-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="8406b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8406b-110">EXAMPLES</span></span>

### <span data-ttu-id="8406b-111">Przykład 1. Wyświetlanie podsumowania trasy ścieżki podstawowej</span><span class="sxs-lookup"><span data-stu-id="8406b-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="8406b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8406b-112">PARAMETERS</span></span>

### <span data-ttu-id="8406b-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="8406b-113">-CrossConnectionName</span></span>
<span data-ttu-id="8406b-114">Nazwa połączenia krzyżowego trasy ekspresowej</span><span class="sxs-lookup"><span data-stu-id="8406b-114">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="8406b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8406b-115">-DefaultProfile</span></span>
<span data-ttu-id="8406b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8406b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8406b-117">— DevicePath</span><span class="sxs-lookup"><span data-stu-id="8406b-117">-DevicePath</span></span>
<span data-ttu-id="8406b-118">Dopuszczalne wartości dla tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="8406b-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="8406b-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8406b-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="8406b-120">Połączenie krzyżowe trasy ekspresowej</span><span class="sxs-lookup"><span data-stu-id="8406b-120">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="8406b-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="8406b-121">-PeeringType</span></span>
<span data-ttu-id="8406b-122">Dopuszczalne wartości dla tego parametru to: `AzurePrivatePeering` `AzurePublicPeering` , i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="8406b-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="8406b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8406b-123">-ResourceGroupName</span></span>
<span data-ttu-id="8406b-124">Nazwa grupy zasobów zawierającej połączenie krzyżowe expressRoute.</span><span class="sxs-lookup"><span data-stu-id="8406b-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="8406b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8406b-125">CommonParameters</span></span>
<span data-ttu-id="8406b-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8406b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8406b-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8406b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8406b-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8406b-128">INPUTS</span></span>

### <span data-ttu-id="8406b-129">Brak</span><span class="sxs-lookup"><span data-stu-id="8406b-129">None</span></span>
<span data-ttu-id="8406b-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="8406b-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8406b-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8406b-131">OUTPUTS</span></span>

### <span data-ttu-id="8406b-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="8406b-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="8406b-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8406b-133">NOTES</span></span>

## <span data-ttu-id="8406b-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8406b-134">RELATED LINKS</span></span>

[<span data-ttu-id="8406b-135">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="8406b-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="8406b-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8406b-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)
