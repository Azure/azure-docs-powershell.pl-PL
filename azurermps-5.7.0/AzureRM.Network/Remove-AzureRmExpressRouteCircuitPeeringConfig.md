---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 36cf08aa4cb201beac284ae2296dfa508bf4edba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528026"
---
# <span data-ttu-id="ac934-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ac934-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="ac934-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac934-102">SYNOPSIS</span></span>
<span data-ttu-id="ac934-103">Usuwa konfigurację komunikacji równorzędnej obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ac934-103">Removes an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac934-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac934-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac934-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ac934-105">DESCRIPTION</span></span>
<span data-ttu-id="ac934-106">Polecenie cmdlet **Remove-AzureRmExpressRouteCircuitPeeringConfig** umożliwia usunięcie konfiguracji komunikacji równorzędnej ExpressRoute obwodu.</span><span class="sxs-lookup"><span data-stu-id="ac934-106">The **Remove-AzureRmExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="ac934-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac934-107">EXAMPLES</span></span>

### <span data-ttu-id="ac934-108">Przykład 1: Usuwanie konfiguracji komunikacji równorzędnej ze obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="ac934-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="ac934-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac934-109">PARAMETERS</span></span>

### <span data-ttu-id="ac934-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac934-110">-DefaultProfile</span></span>
<span data-ttu-id="ac934-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac934-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac934-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ac934-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ac934-113">Obwód ExpressRoute zawierający konfigurację komunikacji równorzędnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ac934-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="ac934-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ac934-114">-Name</span></span>
<span data-ttu-id="ac934-115">Nazwa konfiguracji elementu równorzędnego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ac934-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="ac934-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ac934-116">-PeerAddressType</span></span>
<span data-ttu-id="ac934-117">Rodzina adresów komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="ac934-117">The Address family of the peering</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac934-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac934-118">CommonParameters</span></span>
<span data-ttu-id="ac934-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac934-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac934-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac934-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac934-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac934-121">INPUTS</span></span>

### <span data-ttu-id="ac934-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ac934-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="ac934-123">Parametr "ExpressRouteCircuit" akceptuje wartość typu "PSExpressRouteCircuit" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ac934-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="ac934-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac934-124">OUTPUTS</span></span>

### <span data-ttu-id="ac934-125">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ac934-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ac934-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac934-126">NOTES</span></span>

## <span data-ttu-id="ac934-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac934-127">RELATED LINKS</span></span>

[<span data-ttu-id="ac934-128">Dodaj-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ac934-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ac934-129">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ac934-129">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="ac934-130">Nowe — AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ac934-130">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ac934-131">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ac934-131">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
