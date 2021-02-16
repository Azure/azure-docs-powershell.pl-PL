---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 1c59ef12964ddd022add01ae296b8ecac9ad0acd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179890"
---
# <span data-ttu-id="262d5-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="262d5-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="262d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="262d5-102">SYNOPSIS</span></span>
<span data-ttu-id="262d5-103">Pobiera tabelę ARP z obwodu expressRoute.</span><span class="sxs-lookup"><span data-stu-id="262d5-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="262d5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="262d5-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="262d5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="262d5-105">DESCRIPTION</span></span>
<span data-ttu-id="262d5-106">Polecenie **cmdlet Get-AzExpressRouteCircuitARPTable** pobiera tabelę ARP z obu interfejsów obwodu expressRoute.</span><span class="sxs-lookup"><span data-stu-id="262d5-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="262d5-107">Tabela ARP udostępnia mapowanie adresu IPv4 na adres MAC dla określonej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="262d5-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="262d5-108">Za pomocą tabeli ARP można sprawdzić poprawność konfiguracji i łączności warstwy 2.</span><span class="sxs-lookup"><span data-stu-id="262d5-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="262d5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="262d5-109">EXAMPLES</span></span>

### <span data-ttu-id="262d5-110">Przykład 1. Wyświetlanie tabeli ARP dla elementu równorzędnego expressRoute</span><span class="sxs-lookup"><span data-stu-id="262d5-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="262d5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="262d5-111">PARAMETERS</span></span>

### <span data-ttu-id="262d5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="262d5-112">-DefaultProfile</span></span>
<span data-ttu-id="262d5-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="262d5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="262d5-114">— DevicePath</span><span class="sxs-lookup"><span data-stu-id="262d5-114">-DevicePath</span></span>
<span data-ttu-id="262d5-115">Dopuszczalne wartości dla tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="262d5-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="262d5-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="262d5-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="262d5-117">Nazwa sprawdzana jest nazwa obwodu w układzie ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="262d5-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="262d5-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="262d5-118">-PeeringType</span></span>
<span data-ttu-id="262d5-119">Dopuszczalne wartości dla tego parametru to: `AzurePrivatePeering` `AzurePublicPeering` , i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="262d5-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="262d5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="262d5-120">-ResourceGroupName</span></span>
<span data-ttu-id="262d5-121">Nazwa grupy zasobów zawierającej obwód expressroute.</span><span class="sxs-lookup"><span data-stu-id="262d5-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="262d5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262d5-122">CommonParameters</span></span>
<span data-ttu-id="262d5-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="262d5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262d5-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="262d5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262d5-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="262d5-125">INPUTS</span></span>

### <span data-ttu-id="262d5-126">System.String</span><span class="sxs-lookup"><span data-stu-id="262d5-126">System.String</span></span>

## <span data-ttu-id="262d5-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="262d5-127">OUTPUTS</span></span>

### <span data-ttu-id="262d5-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="262d5-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="262d5-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="262d5-129">NOTES</span></span>

## <span data-ttu-id="262d5-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="262d5-130">RELATED LINKS</span></span>

[<span data-ttu-id="262d5-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="262d5-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="262d5-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="262d5-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="262d5-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="262d5-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
