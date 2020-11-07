---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetable
schema: 2.0.0
ms.openlocfilehash: 883d2ae51046f3dc1ee6c8350d996fedbfff083e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898724"
---
# <span data-ttu-id="a2411-101">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a2411-101">Get-AzureRmExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="a2411-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2411-102">SYNOPSIS</span></span>
<span data-ttu-id="a2411-103">Pobiera tabelę tras z obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a2411-103">Gets a route table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2411-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2411-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2411-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a2411-105">DESCRIPTION</span></span>
<span data-ttu-id="a2411-106">Polecenie cmdlet **Get-AzureRmExpressRouteCircuitRouteTable** pobiera szczegółową tabelę tras obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a2411-106">The **Get-AzureRmExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="a2411-107">W tabeli Route zostaną wyświetlone wszystkie trasy lub można filtrować, aby były wyświetlane trasy dla określonego typu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="a2411-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="a2411-108">Za pomocą tabeli Route można sprawdzić poprawność konfiguracji i łączności równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="a2411-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="a2411-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2411-109">EXAMPLES</span></span>

### <span data-ttu-id="a2411-110">Przykład 1. Wyświetlanie tabeli tras dla ścieżki podstawowej</span><span class="sxs-lookup"><span data-stu-id="a2411-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="a2411-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2411-111">PARAMETERS</span></span>

### <span data-ttu-id="a2411-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2411-112">-DefaultProfile</span></span>
<span data-ttu-id="a2411-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2411-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2411-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="a2411-114">-DevicePath</span></span>
<span data-ttu-id="a2411-115">Dopuszczalne wartości tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="a2411-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: DevicePathEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2411-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="a2411-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="a2411-117">Nazwa badanego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a2411-117">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2411-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a2411-118">-PeeringType</span></span>
<span data-ttu-id="a2411-119">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a2411-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2411-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2411-120">-ResourceGroupName</span></span>
<span data-ttu-id="a2411-121">Nazwa grupy zasobów zawierającej obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a2411-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2411-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2411-122">CommonParameters</span></span>
<span data-ttu-id="a2411-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2411-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2411-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2411-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2411-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2411-125">INPUTS</span></span>

## <span data-ttu-id="a2411-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2411-126">OUTPUTS</span></span>

### <span data-ttu-id="a2411-127">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="a2411-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="a2411-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2411-128">NOTES</span></span>

## <span data-ttu-id="a2411-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2411-129">RELATED LINKS</span></span>

[<span data-ttu-id="a2411-130">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a2411-130">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="a2411-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a2411-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="a2411-132">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="a2411-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
