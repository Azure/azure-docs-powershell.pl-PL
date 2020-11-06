---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 9d221f5ff25e43a750f939f80eae7a7878eacc44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545595"
---
# <span data-ttu-id="6350c-101">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6350c-101">Get-AzureRmExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="6350c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6350c-102">SYNOPSIS</span></span>
<span data-ttu-id="6350c-103">Pobiera tabelę tras z obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6350c-103">Gets a route table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6350c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6350c-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6350c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6350c-105">DESCRIPTION</span></span>
<span data-ttu-id="6350c-106">Polecenie cmdlet **Get-AzureRmExpressRouteCircuitRouteTable** pobiera szczegółową tabelę tras obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6350c-106">The **Get-AzureRmExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="6350c-107">W tabeli Route zostaną wyświetlone wszystkie trasy lub można filtrować, aby były wyświetlane trasy dla określonego typu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="6350c-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="6350c-108">Za pomocą tabeli Route można sprawdzić poprawność konfiguracji i łączności równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="6350c-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="6350c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6350c-109">EXAMPLES</span></span>

### <span data-ttu-id="6350c-110">Przykład 1. Wyświetlanie tabeli tras dla ścieżki podstawowej</span><span class="sxs-lookup"><span data-stu-id="6350c-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="6350c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6350c-111">PARAMETERS</span></span>

### <span data-ttu-id="6350c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6350c-112">-DefaultProfile</span></span>
<span data-ttu-id="6350c-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6350c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6350c-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="6350c-114">-DevicePath</span></span>
<span data-ttu-id="6350c-115">Dopuszczalne wartości tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="6350c-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="6350c-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="6350c-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="6350c-117">Nazwa badanego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6350c-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="6350c-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="6350c-118">-PeeringType</span></span>
<span data-ttu-id="6350c-119">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="6350c-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="6350c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6350c-120">-ResourceGroupName</span></span>
<span data-ttu-id="6350c-121">Nazwa grupy zasobów zawierającej obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6350c-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="6350c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6350c-122">CommonParameters</span></span>
<span data-ttu-id="6350c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6350c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6350c-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6350c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6350c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6350c-125">INPUTS</span></span>

### <span data-ttu-id="6350c-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6350c-126">None</span></span>
<span data-ttu-id="6350c-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6350c-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6350c-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6350c-128">OUTPUTS</span></span>

### <span data-ttu-id="6350c-129">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="6350c-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="6350c-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6350c-130">NOTES</span></span>

## <span data-ttu-id="6350c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6350c-131">RELATED LINKS</span></span>

[<span data-ttu-id="6350c-132">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6350c-132">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="6350c-133">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6350c-133">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="6350c-134">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="6350c-134">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
