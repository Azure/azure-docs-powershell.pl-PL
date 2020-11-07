---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitstats
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
ms.openlocfilehash: d9978c50186b520d8e956dc20581d1ceb615b673
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719095"
---
# <span data-ttu-id="f893b-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="f893b-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="f893b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f893b-102">SYNOPSIS</span></span>
<span data-ttu-id="f893b-103">Pobiera statystykę użycia obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f893b-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f893b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f893b-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f893b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f893b-105">DESCRIPTION</span></span>
<span data-ttu-id="f893b-106">Polecenie cmdlet **Get-AzureRmExpressRouteCircuitStats** pobiera statystykę ruchu dla obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f893b-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="f893b-107">Statystyka obejmuje liczbę bajtów wysłanych i odebranych w ramach tras podstawowych i pomocniczych.</span><span class="sxs-lookup"><span data-stu-id="f893b-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="f893b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f893b-108">EXAMPLES</span></span>

### <span data-ttu-id="f893b-109">Przykład 1: wyświetlanie statystyki ruchu dla elementu równorzędnego ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f893b-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="f893b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f893b-110">PARAMETERS</span></span>

### <span data-ttu-id="f893b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f893b-111">-DefaultProfile</span></span>
<span data-ttu-id="f893b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f893b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f893b-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="f893b-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="f893b-114">Nazwa badanego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f893b-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="f893b-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="f893b-115">-PeeringType</span></span>
<span data-ttu-id="f893b-116">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="f893b-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="f893b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f893b-117">-ResourceGroupName</span></span>
<span data-ttu-id="f893b-118">Nazwa grupy zasobów zawierającej obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f893b-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="f893b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f893b-119">CommonParameters</span></span>
<span data-ttu-id="f893b-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f893b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f893b-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f893b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f893b-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f893b-122">INPUTS</span></span>

### <span data-ttu-id="f893b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f893b-123">System.String</span></span>

## <span data-ttu-id="f893b-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f893b-124">OUTPUTS</span></span>

### <span data-ttu-id="f893b-125">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="f893b-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="f893b-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f893b-126">NOTES</span></span>

## <span data-ttu-id="f893b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f893b-127">RELATED LINKS</span></span>

[<span data-ttu-id="f893b-128">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f893b-128">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="f893b-129">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f893b-129">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="f893b-130">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f893b-130">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)
