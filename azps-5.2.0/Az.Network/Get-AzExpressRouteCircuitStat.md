---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: 15b02ce4693e452bda370c9fb1ae9c69012e9574
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329758"
---
# <span data-ttu-id="68c4b-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="68c4b-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="68c4b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="68c4b-103">Pobiera statystykę użycia obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="68c4b-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="68c4b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68c4b-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68c4b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="68c4b-105">DESCRIPTION</span></span>
<span data-ttu-id="68c4b-106">Polecenie cmdlet **Get-AzExpressRouteCircuitStat** pobiera statystykę ruchu dla obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="68c4b-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="68c4b-107">Statystyka obejmuje liczbę bajtów wysłanych i odebranych w ramach tras podstawowych i pomocniczych.</span><span class="sxs-lookup"><span data-stu-id="68c4b-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="68c4b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68c4b-108">EXAMPLES</span></span>

### <span data-ttu-id="68c4b-109">Przykład 1: wyświetlanie statystyki ruchu dla elementu równorzędnego ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="68c4b-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="68c4b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68c4b-110">PARAMETERS</span></span>

### <span data-ttu-id="68c4b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68c4b-111">-DefaultProfile</span></span>
<span data-ttu-id="68c4b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="68c4b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68c4b-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="68c4b-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="68c4b-114">Nazwa badanego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="68c4b-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="68c4b-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="68c4b-115">-PeeringType</span></span>
<span data-ttu-id="68c4b-116">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="68c4b-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68c4b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68c4b-117">-ResourceGroupName</span></span>
<span data-ttu-id="68c4b-118">Nazwa grupy zasobów zawierającej obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="68c4b-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="68c4b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68c4b-119">CommonParameters</span></span>
<span data-ttu-id="68c4b-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68c4b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68c4b-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68c4b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68c4b-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68c4b-122">INPUTS</span></span>

### <span data-ttu-id="68c4b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="68c4b-123">System.String</span></span>

## <span data-ttu-id="68c4b-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68c4b-124">OUTPUTS</span></span>

### <span data-ttu-id="68c4b-125">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="68c4b-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="68c4b-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68c4b-126">NOTES</span></span>

## <span data-ttu-id="68c4b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68c4b-127">RELATED LINKS</span></span>

[<span data-ttu-id="68c4b-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="68c4b-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="68c4b-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="68c4b-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="68c4b-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="68c4b-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
