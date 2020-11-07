---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: ce1e05106350adda37ffa5877585ff37337dad87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870739"
---
# <span data-ttu-id="7fecd-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="7fecd-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="7fecd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7fecd-102">SYNOPSIS</span></span>
<span data-ttu-id="7fecd-103">Pobiera tabelę ARP z obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7fecd-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="7fecd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7fecd-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fecd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7fecd-105">DESCRIPTION</span></span>
<span data-ttu-id="7fecd-106">Polecenie cmdlet **Get-AzExpressRouteCircuitARPTable** pobiera tabelę ARP z obu interfejsów obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7fecd-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="7fecd-107">Tabela ARP zawiera mapowanie adresu IPv4 na adres MAC konkretnej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="7fecd-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="7fecd-108">Za pomocą tabeli ARP można sprawdzić konfigurację i łączność warstwy 2.</span><span class="sxs-lookup"><span data-stu-id="7fecd-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="7fecd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7fecd-109">EXAMPLES</span></span>

### <span data-ttu-id="7fecd-110">Przykład 1. Wyświetlanie tabeli ARP dla elementu równorzędnego ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="7fecd-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="7fecd-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7fecd-111">PARAMETERS</span></span>

### <span data-ttu-id="7fecd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fecd-112">-DefaultProfile</span></span>
<span data-ttu-id="7fecd-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7fecd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fecd-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="7fecd-114">-DevicePath</span></span>
<span data-ttu-id="7fecd-115">Dopuszczalne wartości tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="7fecd-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="7fecd-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="7fecd-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="7fecd-117">Nazwa badanego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7fecd-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="7fecd-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="7fecd-118">-PeeringType</span></span>
<span data-ttu-id="7fecd-119">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="7fecd-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="7fecd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fecd-120">-ResourceGroupName</span></span>
<span data-ttu-id="7fecd-121">Nazwa grupy zasobów zawierającej obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7fecd-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="7fecd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fecd-122">CommonParameters</span></span>
<span data-ttu-id="7fecd-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fecd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fecd-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fecd-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fecd-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7fecd-125">INPUTS</span></span>

### <span data-ttu-id="7fecd-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7fecd-126">System.String</span></span>

## <span data-ttu-id="7fecd-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7fecd-127">OUTPUTS</span></span>

### <span data-ttu-id="7fecd-128">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="7fecd-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="7fecd-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7fecd-129">NOTES</span></span>

## <span data-ttu-id="7fecd-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7fecd-130">RELATED LINKS</span></span>

[<span data-ttu-id="7fecd-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="7fecd-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="7fecd-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7fecd-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="7fecd-133">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="7fecd-133">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
