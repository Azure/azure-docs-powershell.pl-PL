---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 4b3f7e455d11696ca92ae8a2e8b530dc8d875123
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408274"
---
# <span data-ttu-id="010a8-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="010a8-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="010a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="010a8-102">SYNOPSIS</span></span>
<span data-ttu-id="010a8-103">Pobiera tabelę ARP z obwodu expressRoute.</span><span class="sxs-lookup"><span data-stu-id="010a8-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="010a8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="010a8-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="010a8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="010a8-105">DESCRIPTION</span></span>
<span data-ttu-id="010a8-106">Polecenie **cmdlet Get-AzExpressRouteCircuitARPTable** pobiera tabelę ARP z obu interfejsów obwodu expressRoute.</span><span class="sxs-lookup"><span data-stu-id="010a8-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="010a8-107">Tabela ARP udostępnia mapowanie adresu IPv4 na adres MAC dla określonej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="010a8-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="010a8-108">Za pomocą tabeli ARP można sprawdzić poprawność konfiguracji i łączności warstwy 2.</span><span class="sxs-lookup"><span data-stu-id="010a8-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="010a8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="010a8-109">EXAMPLES</span></span>

### <span data-ttu-id="010a8-110">Przykład 1. Wyświetlanie tabeli ARP dla elementu równorzędnego expressRoute</span><span class="sxs-lookup"><span data-stu-id="010a8-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="010a8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="010a8-111">PARAMETERS</span></span>

### <span data-ttu-id="010a8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="010a8-112">-DefaultProfile</span></span>
<span data-ttu-id="010a8-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="010a8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="010a8-114">— DevicePath</span><span class="sxs-lookup"><span data-stu-id="010a8-114">-DevicePath</span></span>
<span data-ttu-id="010a8-115">Dopuszczalne wartości dla tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="010a8-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="010a8-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="010a8-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="010a8-117">Nazwa sprawdzana jest nazwa obwodu w układzie ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="010a8-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="010a8-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="010a8-118">-PeeringType</span></span>
<span data-ttu-id="010a8-119">Dopuszczalne wartości dla tego parametru to: `AzurePrivatePeering` `AzurePublicPeering` , i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="010a8-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="010a8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="010a8-120">-ResourceGroupName</span></span>
<span data-ttu-id="010a8-121">Nazwa grupy zasobów zawierającej obwód expressroute.</span><span class="sxs-lookup"><span data-stu-id="010a8-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="010a8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="010a8-122">CommonParameters</span></span>
<span data-ttu-id="010a8-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="010a8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="010a8-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="010a8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="010a8-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="010a8-125">INPUTS</span></span>

### <span data-ttu-id="010a8-126">System.String</span><span class="sxs-lookup"><span data-stu-id="010a8-126">System.String</span></span>

## <span data-ttu-id="010a8-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="010a8-127">OUTPUTS</span></span>

### <span data-ttu-id="010a8-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="010a8-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="010a8-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="010a8-129">NOTES</span></span>

## <span data-ttu-id="010a8-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="010a8-130">RELATED LINKS</span></span>

[<span data-ttu-id="010a8-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="010a8-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="010a8-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="010a8-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="010a8-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="010a8-133">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
