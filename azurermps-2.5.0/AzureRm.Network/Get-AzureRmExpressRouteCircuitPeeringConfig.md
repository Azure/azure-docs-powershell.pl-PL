---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
ms.openlocfilehash: 187b7848dc3634ee67521e03f46f4684f23b9913
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897958"
---
# <span data-ttu-id="3164c-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3164c-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="3164c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3164c-102">SYNOPSIS</span></span>
<span data-ttu-id="3164c-103">Pobiera konfigurację komunikacji równorzędnej obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3164c-103">Gets an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3164c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3164c-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3164c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3164c-105">DESCRIPTION</span></span>
<span data-ttu-id="3164c-106">Polecenie cmdlet **Get-AzureRmExpressRouteCircuitPeeringConfig** umożliwia pobranie konfiguracji relacji komunikacji równorzędnej dla obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3164c-106">The **Get-AzureRmExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="3164c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3164c-107">EXAMPLES</span></span>

### <span data-ttu-id="3164c-108">Przykład 1. Wyświetlanie konfiguracji komunikacji równorzędnej dla obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="3164c-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzureRmExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="3164c-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3164c-109">PARAMETERS</span></span>

### <span data-ttu-id="3164c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3164c-110">-DefaultProfile</span></span>
<span data-ttu-id="3164c-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3164c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3164c-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3164c-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="3164c-113">Obiekt obwodu ExpressRoute zawierający konfigurację komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="3164c-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3164c-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3164c-114">-Name</span></span>
<span data-ttu-id="3164c-115">Nazwa konfiguracji elementu równorzędnego do pobrania.</span><span class="sxs-lookup"><span data-stu-id="3164c-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3164c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3164c-116">CommonParameters</span></span>
<span data-ttu-id="3164c-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3164c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3164c-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3164c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3164c-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3164c-119">INPUTS</span></span>

### <span data-ttu-id="3164c-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3164c-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="3164c-121">Parametr "ExpressRouteCircuit" akceptuje wartość typu "PSExpressRouteCircuit" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="3164c-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="3164c-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3164c-122">OUTPUTS</span></span>

### <span data-ttu-id="3164c-123">Microsoft. Azure. Commands. Network. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="3164c-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="3164c-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3164c-124">NOTES</span></span>

## <span data-ttu-id="3164c-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3164c-125">RELATED LINKS</span></span>

[<span data-ttu-id="3164c-126">Dodaj-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3164c-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="3164c-127">Nowe — AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3164c-127">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="3164c-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3164c-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="3164c-129">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3164c-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
