---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionArpTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionArpTable.md
ms.openlocfilehash: 4e23e96906874d8f19931005919ef088f9bc5ec1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952266"
---
# <span data-ttu-id="231e8-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="231e8-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="231e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="231e8-102">SYNOPSIS</span></span>
<span data-ttu-id="231e8-103">Pobiera tabelę ARP z połączenia krzyżowego expressRoute.</span><span class="sxs-lookup"><span data-stu-id="231e8-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="231e8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="231e8-104">SYNTAX</span></span>

### <span data-ttu-id="231e8-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="231e8-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="231e8-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="231e8-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="231e8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="231e8-107">DESCRIPTION</span></span>
<span data-ttu-id="231e8-108">Polecenie **cmdlet Get-AzExpressRouteCrossConnectionARPTable** pobiera tabelę ARP z obu interfejsów połączenia krzyżowego usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="231e8-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="231e8-109">Tabela ARP udostępnia mapowanie adresu IPv4 na adres MAC dla określonej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="231e8-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="231e8-110">Za pomocą tabeli ARP można sprawdzić poprawność konfiguracji i łączności warstwy 2.</span><span class="sxs-lookup"><span data-stu-id="231e8-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="231e8-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="231e8-111">EXAMPLES</span></span>

### <span data-ttu-id="231e8-112">Przykład 1. Wyświetlanie tabeli ARP dla elementu równorzędnego expressRoute</span><span class="sxs-lookup"><span data-stu-id="231e8-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="231e8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="231e8-113">PARAMETERS</span></span>

### <span data-ttu-id="231e8-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="231e8-114">-CrossConnectionName</span></span>
<span data-ttu-id="231e8-115">Nazwa połączenia krzyżowego trasy ekspresowej</span><span class="sxs-lookup"><span data-stu-id="231e8-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="231e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="231e8-116">-DefaultProfile</span></span>
<span data-ttu-id="231e8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="231e8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="231e8-118">— DevicePath</span><span class="sxs-lookup"><span data-stu-id="231e8-118">-DevicePath</span></span>
<span data-ttu-id="231e8-119">Dopuszczalne wartości dla tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="231e8-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="231e8-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="231e8-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="231e8-121">Połączenie krzyżowe trasy ekspresowej</span><span class="sxs-lookup"><span data-stu-id="231e8-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="231e8-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="231e8-122">-PeeringType</span></span>
<span data-ttu-id="231e8-123">Dopuszczalne wartości dla tego parametru to: `AzurePrivatePeering` `AzurePublicPeering` , i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="231e8-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="231e8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="231e8-124">-ResourceGroupName</span></span>
<span data-ttu-id="231e8-125">Nazwa grupy zasobów zawierającej połączenie krzyżowe expressRoute.</span><span class="sxs-lookup"><span data-stu-id="231e8-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="231e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="231e8-126">CommonParameters</span></span>
<span data-ttu-id="231e8-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="231e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="231e8-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="231e8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="231e8-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="231e8-129">INPUTS</span></span>

### <span data-ttu-id="231e8-130">Brak</span><span class="sxs-lookup"><span data-stu-id="231e8-130">None</span></span>
<span data-ttu-id="231e8-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="231e8-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="231e8-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="231e8-132">OUTPUTS</span></span>

### <span data-ttu-id="231e8-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="231e8-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="231e8-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="231e8-134">NOTES</span></span>

## <span data-ttu-id="231e8-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="231e8-135">RELATED LINKS</span></span>

[<span data-ttu-id="231e8-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="231e8-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="231e8-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="231e8-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
