---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: 5e0d9140e11ead75a1abbf43d520d44cffaf5463
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709547"
---
# <span data-ttu-id="1ae11-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1ae11-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="1ae11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ae11-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae11-103">Pobiera podsumowanie tabeli tras dla połączenia z ExpressRoute krzyżowego.</span><span class="sxs-lookup"><span data-stu-id="1ae11-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="1ae11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ae11-104">SYNTAX</span></span>

### <span data-ttu-id="1ae11-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="1ae11-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ae11-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="1ae11-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ae11-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1ae11-107">DESCRIPTION</span></span>
<span data-ttu-id="1ae11-108">Polecenie cmdlet **Get-AzExpressRouteCrossConnectionRouteTableSummary** pobiera podsumowanie informacji o sąsiadach BGP dla określonego kontekstu routingu.</span><span class="sxs-lookup"><span data-stu-id="1ae11-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="1ae11-109">Te informacje są przydatne do określenia, jak długo został ustanowiony kontekst routingu oraz ile prefiksów trasy anonsowanych przez router równorzędny.</span><span class="sxs-lookup"><span data-stu-id="1ae11-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="1ae11-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ae11-110">EXAMPLES</span></span>

### <span data-ttu-id="1ae11-111">Przykład 1. Wyświetl podsumowanie trasy dla ścieżki podstawowej</span><span class="sxs-lookup"><span data-stu-id="1ae11-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="1ae11-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ae11-112">PARAMETERS</span></span>

### <span data-ttu-id="1ae11-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="1ae11-113">-CrossConnectionName</span></span>
<span data-ttu-id="1ae11-114">Nazwa połączenia krzyżowego Express Route</span><span class="sxs-lookup"><span data-stu-id="1ae11-114">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="1ae11-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae11-115">-DefaultProfile</span></span>
<span data-ttu-id="1ae11-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ae11-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ae11-117">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="1ae11-117">-DevicePath</span></span>
<span data-ttu-id="1ae11-118">Dopuszczalne wartości tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="1ae11-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="1ae11-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1ae11-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="1ae11-120">Połączenie krzyżowe w ramach routingu Express</span><span class="sxs-lookup"><span data-stu-id="1ae11-120">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="1ae11-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="1ae11-121">-PeeringType</span></span>
<span data-ttu-id="1ae11-122">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="1ae11-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="1ae11-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae11-123">-ResourceGroupName</span></span>
<span data-ttu-id="1ae11-124">Nazwa grupy zasobów zawierającej połączenie krzyżowe ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1ae11-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="1ae11-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae11-125">CommonParameters</span></span>
<span data-ttu-id="1ae11-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae11-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae11-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ae11-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae11-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ae11-128">INPUTS</span></span>

### <span data-ttu-id="1ae11-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1ae11-129">None</span></span>
<span data-ttu-id="1ae11-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1ae11-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1ae11-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ae11-131">OUTPUTS</span></span>

### <span data-ttu-id="1ae11-132">Microsoft. Azure. Commands. Network. models. PSExpressRouteCrossConnectionRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="1ae11-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="1ae11-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ae11-133">NOTES</span></span>

## <span data-ttu-id="1ae11-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ae11-134">RELATED LINKS</span></span>

[<span data-ttu-id="1ae11-135">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="1ae11-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="1ae11-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ae11-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)