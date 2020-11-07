---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5feeba4ffb4f73365e9b6df86a03e8920b74f88e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890310"
---
# <span data-ttu-id="0bed2-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0bed2-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="0bed2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0bed2-102">SYNOPSIS</span></span>
<span data-ttu-id="0bed2-103">Usuwa konfigurację komunikacji równorzędnej obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0bed2-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="0bed2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0bed2-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bed2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0bed2-105">DESCRIPTION</span></span>
<span data-ttu-id="0bed2-106">Polecenie cmdlet **Remove-AzExpressRouteCircuitPeeringConfig** umożliwia usunięcie konfiguracji komunikacji równorzędnej ExpressRoute obwodu.</span><span class="sxs-lookup"><span data-stu-id="0bed2-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="0bed2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0bed2-107">EXAMPLES</span></span>

### <span data-ttu-id="0bed2-108">Przykład 1: Usuwanie konfiguracji komunikacji równorzędnej ze obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="0bed2-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="0bed2-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0bed2-109">PARAMETERS</span></span>

### <span data-ttu-id="0bed2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bed2-110">-DefaultProfile</span></span>
<span data-ttu-id="0bed2-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0bed2-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bed2-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0bed2-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="0bed2-113">Obwód ExpressRoute zawierający konfigurację komunikacji równorzędnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="0bed2-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="0bed2-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0bed2-114">-Name</span></span>
<span data-ttu-id="0bed2-115">Nazwa konfiguracji elementu równorzędnego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="0bed2-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="0bed2-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="0bed2-116">-PeerAddressType</span></span>
<span data-ttu-id="0bed2-117">Rodzina adresów komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="0bed2-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="0bed2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bed2-118">CommonParameters</span></span>
<span data-ttu-id="0bed2-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bed2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bed2-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bed2-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bed2-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bed2-121">INPUTS</span></span>

### <span data-ttu-id="0bed2-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0bed2-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="0bed2-123">Parametr "ExpressRouteCircuit" akceptuje wartość typu "PSExpressRouteCircuit" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="0bed2-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="0bed2-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0bed2-124">OUTPUTS</span></span>

### <span data-ttu-id="0bed2-125">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0bed2-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0bed2-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0bed2-126">NOTES</span></span>

## <span data-ttu-id="0bed2-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0bed2-127">RELATED LINKS</span></span>

[<span data-ttu-id="0bed2-128">Dodaj-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0bed2-128">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="0bed2-129">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0bed2-129">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="0bed2-130">Nowe — AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0bed2-130">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="0bed2-131">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0bed2-131">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
