---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 99f73d9a24ab18c244e4122e5dca7dce0d4002d5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890802"
---
# <span data-ttu-id="2cbe4-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="2cbe4-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="2cbe4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2cbe4-102">SYNOPSIS</span></span>
<span data-ttu-id="2cbe4-103">Pobiera tabelę tras z obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2cbe4-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="2cbe4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2cbe4-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2cbe4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2cbe4-105">DESCRIPTION</span></span>
<span data-ttu-id="2cbe4-106">Polecenie cmdlet **Get-AzExpressRouteCircuitRouteTable** pobiera szczegółową tabelę tras obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2cbe4-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="2cbe4-107">W tabeli Route zostaną wyświetlone wszystkie trasy lub można filtrować, aby były wyświetlane trasy dla określonego typu komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="2cbe4-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="2cbe4-108">Za pomocą tabeli Route można sprawdzić poprawność konfiguracji i łączności równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="2cbe4-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="2cbe4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2cbe4-109">EXAMPLES</span></span>

### <span data-ttu-id="2cbe4-110">Przykład 1. Wyświetlanie tabeli tras dla ścieżki podstawowej</span><span class="sxs-lookup"><span data-stu-id="2cbe4-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="2cbe4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2cbe4-111">PARAMETERS</span></span>

### <span data-ttu-id="2cbe4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cbe4-112">-DefaultProfile</span></span>
<span data-ttu-id="2cbe4-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2cbe4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cbe4-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="2cbe4-114">-DevicePath</span></span>
<span data-ttu-id="2cbe4-115">Dopuszczalne wartości tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="2cbe4-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="2cbe4-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="2cbe4-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="2cbe4-117">Nazwa badanego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2cbe4-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="2cbe4-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="2cbe4-118">-PeeringType</span></span>
<span data-ttu-id="2cbe4-119">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="2cbe4-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="2cbe4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cbe4-120">-ResourceGroupName</span></span>
<span data-ttu-id="2cbe4-121">Nazwa grupy zasobów zawierającej obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2cbe4-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="2cbe4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cbe4-122">CommonParameters</span></span>
<span data-ttu-id="2cbe4-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cbe4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cbe4-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cbe4-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cbe4-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2cbe4-125">INPUTS</span></span>

## <span data-ttu-id="2cbe4-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2cbe4-126">OUTPUTS</span></span>

### <span data-ttu-id="2cbe4-127">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="2cbe4-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="2cbe4-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2cbe4-128">NOTES</span></span>

## <span data-ttu-id="2cbe4-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2cbe4-129">RELATED LINKS</span></span>

[<span data-ttu-id="2cbe4-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="2cbe4-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="2cbe4-131">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2cbe4-131">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="2cbe4-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="2cbe4-132">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
