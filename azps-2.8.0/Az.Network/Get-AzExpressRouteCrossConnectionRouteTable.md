---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: 3fbfcc2ba78bb05eb64764be16bb84189afdd958
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870196"
---
# <span data-ttu-id="4f35f-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="4f35f-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="4f35f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4f35f-102">SYNOPSIS</span></span>
<span data-ttu-id="4f35f-103">Pobiera tabelę tras z połączenia z ExpressRoute krzyżowego.</span><span class="sxs-lookup"><span data-stu-id="4f35f-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="4f35f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4f35f-104">SYNTAX</span></span>

### <span data-ttu-id="4f35f-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="4f35f-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f35f-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="4f35f-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f35f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4f35f-107">DESCRIPTION</span></span>
<span data-ttu-id="4f35f-108">Polecenie cmdlet **Get-AzExpressRouteCrossConnectionRouteTable** pobiera szczegółową tabelę tras obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4f35f-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="4f35f-109">W tabeli Route zostaną wyświetlone wszystkie trasy lub można filtrować, aby były wyświetlane trasy dla określonego typu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="4f35f-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="4f35f-110">Za pomocą tabeli Route można sprawdzić poprawność konfiguracji i łączności równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="4f35f-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="4f35f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4f35f-111">EXAMPLES</span></span>

### <span data-ttu-id="4f35f-112">Przykład 1. Wyświetlanie tabeli tras dla ścieżki podstawowej</span><span class="sxs-lookup"><span data-stu-id="4f35f-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="4f35f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f35f-113">PARAMETERS</span></span>

### <span data-ttu-id="4f35f-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="4f35f-114">-CrossConnectionName</span></span>
<span data-ttu-id="4f35f-115">Nazwa połączenia krzyżowego Express Route</span><span class="sxs-lookup"><span data-stu-id="4f35f-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="4f35f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f35f-116">-DefaultProfile</span></span>
<span data-ttu-id="4f35f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f35f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f35f-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="4f35f-118">-DevicePath</span></span>
<span data-ttu-id="4f35f-119">Dopuszczalne wartości tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="4f35f-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="4f35f-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="4f35f-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="4f35f-121">Połączenie krzyżowe w ramach routingu Express</span><span class="sxs-lookup"><span data-stu-id="4f35f-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="4f35f-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="4f35f-122">-PeeringType</span></span>
<span data-ttu-id="4f35f-123">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="4f35f-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="4f35f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f35f-124">-ResourceGroupName</span></span>
<span data-ttu-id="4f35f-125">Nazwa grupy zasobów zawierającej połączenie krzyżowe ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4f35f-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="4f35f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f35f-126">CommonParameters</span></span>
<span data-ttu-id="4f35f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f35f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f35f-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f35f-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f35f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f35f-129">INPUTS</span></span>

### <span data-ttu-id="4f35f-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4f35f-130">None</span></span>
<span data-ttu-id="4f35f-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4f35f-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4f35f-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4f35f-132">OUTPUTS</span></span>

### <span data-ttu-id="4f35f-133">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="4f35f-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="4f35f-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4f35f-134">NOTES</span></span>

## <span data-ttu-id="4f35f-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f35f-135">RELATED LINKS</span></span>

[<span data-ttu-id="4f35f-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="4f35f-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="4f35f-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4f35f-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
