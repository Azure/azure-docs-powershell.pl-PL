---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitarptable
schema: 2.0.0
ms.openlocfilehash: bdfb86eb53221466beca2566d8ea446072ea33d6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897965"
---
# <span data-ttu-id="ec5ed-101">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ec5ed-101">Get-AzureRmExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="ec5ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec5ed-102">SYNOPSIS</span></span>
<span data-ttu-id="ec5ed-103">Pobiera tabelę ARP z obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ec5ed-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec5ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec5ed-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec5ed-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ec5ed-105">DESCRIPTION</span></span>
<span data-ttu-id="ec5ed-106">Polecenie cmdlet **Get-AzureRmExpressRouteCircuitARPTable** pobiera tabelę ARP z obu interfejsów obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ec5ed-106">The **Get-AzureRmExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="ec5ed-107">Tabela ARP zawiera mapowanie adresu IPv4 na adres MAC konkretnej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="ec5ed-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="ec5ed-108">Za pomocą tabeli ARP można sprawdzić konfigurację i łączność warstwy 2.</span><span class="sxs-lookup"><span data-stu-id="ec5ed-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="ec5ed-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec5ed-109">EXAMPLES</span></span>

### <span data-ttu-id="ec5ed-110">Przykład 1. Wyświetlanie tabeli ARP dla elementu równorzędnego ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="ec5ed-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="ec5ed-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec5ed-111">PARAMETERS</span></span>

### <span data-ttu-id="ec5ed-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec5ed-112">-DefaultProfile</span></span>
<span data-ttu-id="ec5ed-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec5ed-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec5ed-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="ec5ed-114">-DevicePath</span></span>
<span data-ttu-id="ec5ed-115">Dopuszczalne wartości tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="ec5ed-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="ec5ed-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="ec5ed-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="ec5ed-117">Nazwa badanego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ec5ed-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="ec5ed-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="ec5ed-118">-PeeringType</span></span>
<span data-ttu-id="ec5ed-119">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="ec5ed-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="ec5ed-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec5ed-120">-ResourceGroupName</span></span>
<span data-ttu-id="ec5ed-121">Nazwa grupy zasobów zawierającej obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ec5ed-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="ec5ed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec5ed-122">CommonParameters</span></span>
<span data-ttu-id="ec5ed-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec5ed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec5ed-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec5ed-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec5ed-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec5ed-125">INPUTS</span></span>

## <span data-ttu-id="ec5ed-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec5ed-126">OUTPUTS</span></span>

### <span data-ttu-id="ec5ed-127">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="ec5ed-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="ec5ed-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec5ed-128">NOTES</span></span>

## <span data-ttu-id="ec5ed-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec5ed-129">RELATED LINKS</span></span>

[<span data-ttu-id="ec5ed-130">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ec5ed-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="ec5ed-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ec5ed-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="ec5ed-132">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="ec5ed-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
