---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
ms.openlocfilehash: e007f220b827db144a4c10b1adb5732e110ddf0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546723"
---
# <span data-ttu-id="7d164-101">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="7d164-101">Get-AzureRmExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="7d164-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d164-102">SYNOPSIS</span></span>
<span data-ttu-id="7d164-103">Pobiera tabelę ARP z obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7d164-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d164-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d164-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d164-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7d164-105">DESCRIPTION</span></span>
<span data-ttu-id="7d164-106">Polecenie cmdlet **Get-AzureRmExpressRouteCircuitARPTable** pobiera tabelę ARP z obu interfejsów obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7d164-106">The **Get-AzureRmExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="7d164-107">Tabela ARP zawiera mapowanie adresu IPv4 na adres MAC konkretnej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="7d164-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="7d164-108">Za pomocą tabeli ARP można sprawdzić konfigurację i łączność warstwy 2.</span><span class="sxs-lookup"><span data-stu-id="7d164-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="7d164-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d164-109">EXAMPLES</span></span>

### <span data-ttu-id="7d164-110">Przykład 1. Wyświetlanie tabeli ARP dla elementu równorzędnego ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="7d164-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="7d164-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d164-111">PARAMETERS</span></span>

### <span data-ttu-id="7d164-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d164-112">-DefaultProfile</span></span>
<span data-ttu-id="7d164-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d164-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d164-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="7d164-114">-DevicePath</span></span>
<span data-ttu-id="7d164-115">Dopuszczalne wartości tego parametru to: `Primary` lub `Secondary`</span><span class="sxs-lookup"><span data-stu-id="7d164-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="7d164-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="7d164-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="7d164-117">Nazwa badanego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7d164-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="7d164-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="7d164-118">-PeeringType</span></span>
<span data-ttu-id="7d164-119">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="7d164-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="7d164-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d164-120">-ResourceGroupName</span></span>
<span data-ttu-id="7d164-121">Nazwa grupy zasobów zawierającej obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7d164-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="7d164-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d164-122">CommonParameters</span></span>
<span data-ttu-id="7d164-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d164-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d164-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d164-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d164-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d164-125">INPUTS</span></span>

### <span data-ttu-id="7d164-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7d164-126">None</span></span>
<span data-ttu-id="7d164-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7d164-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7d164-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d164-128">OUTPUTS</span></span>

### <span data-ttu-id="7d164-129">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="7d164-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="7d164-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d164-130">NOTES</span></span>

## <span data-ttu-id="7d164-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d164-131">RELATED LINKS</span></span>

[<span data-ttu-id="7d164-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d164-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="7d164-133">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7d164-133">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="7d164-134">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="7d164-134">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
