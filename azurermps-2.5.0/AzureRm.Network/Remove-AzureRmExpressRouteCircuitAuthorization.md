---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: 144d70318463b7c5ffebfa6b7d942ec2a351fc24
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897885"
---
# <span data-ttu-id="d23a6-101">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="d23a6-101">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="d23a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d23a6-102">SYNOPSIS</span></span>
<span data-ttu-id="d23a6-103">Usuwa istniejącą autoryzację konfiguracji ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d23a6-103">Removes an existing ExpressRoute configuration authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d23a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d23a6-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d23a6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d23a6-105">DESCRIPTION</span></span>
<span data-ttu-id="d23a6-106">Polecenie cmdlet **Remove-AzureRmExpressRouteCircuitAuthorization** usuwa autoryzację przypisaną do obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d23a6-106">The **Remove-AzureRmExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="d23a6-107">ExpressRoute obwodów łączy się z siecią lokalną na platformie Azure, korzystając z dostawcy usług łączności zamiast z publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="d23a6-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="d23a6-108">Właściciel obwodu ExpressRoute może utworzyć maksymalnie 10 zezwoleń dla każdego obwodu; te pozwolenia generują klucz autoryzacji, który może być wykorzystywany przez właściciela sieci wirtualnej w celu podłączenia sieci do obwodu.</span><span class="sxs-lookup"><span data-stu-id="d23a6-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="d23a6-109">Może istnieć tylko jedna autoryzacja na sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="d23a6-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="d23a6-110">Jednak w dowolnym momencie właściciel obwodu może użyć narzędzia **Remove-AzureRmExpressRouteCircuitAuthorization** w celu usunięcia autoryzacji przypisanej do sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d23a6-110">At any time, however, the circuit owner can use **Remove-AzureRmExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="d23a6-111">Gdy to nastąpi, odpowiednia sieć wirtualna nie może już używać obwodu ExpressRoute do łączenia się z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d23a6-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="d23a6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d23a6-112">EXAMPLES</span></span>

### <span data-ttu-id="d23a6-113">Przykład 1: usuwanie autoryzacji obwodu z obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="d23a6-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="d23a6-114">W tym przykładzie jest usuwana autoryzacja obwodu ze obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d23a6-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="d23a6-115">W pierwszym poleceniu użyto polecenia cmdlet **Get-AzureRmExpressRouteCircuit** w celu utworzenia odwołania do obiektu dla obwodu ExpressRoute o nazwie ContosoCircuit i zapisanie wyniku w zmiennej o nazwie $Circuit.</span><span class="sxs-lookup"><span data-stu-id="d23a6-115">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>

<span data-ttu-id="d23a6-116">Drugie polecenie oznacza ContosoCircuitAuthorization autoryzacji obwodu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d23a6-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>

<span data-ttu-id="d23a6-117">W trzecim poleceniu użyto polecenia cmdlet Set-AzureRmExpressRouteCircuit w celu potwierdzenia usunięcia obwodu ExpressRoute przechowywanego w zmiennej $Circuit.</span><span class="sxs-lookup"><span data-stu-id="d23a6-117">The third command uses the Set-AzureRmExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="d23a6-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d23a6-118">PARAMETERS</span></span>

### <span data-ttu-id="d23a6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d23a6-119">-DefaultProfile</span></span>
<span data-ttu-id="d23a6-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d23a6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d23a6-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d23a6-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="d23a6-122">Określa obiekt ExpressRouteCircuit, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d23a6-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d23a6-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d23a6-123">-Name</span></span>
<span data-ttu-id="d23a6-124">Określa nazwę autoryzacji obwodu usuniętego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d23a6-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d23a6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d23a6-125">CommonParameters</span></span>
<span data-ttu-id="d23a6-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d23a6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d23a6-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d23a6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d23a6-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d23a6-128">INPUTS</span></span>

### <span data-ttu-id="d23a6-129">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d23a6-129">PSExpressRouteCircuit</span></span>
<span data-ttu-id="d23a6-130">To polecenie cmdlet akceptuje potokowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="d23a6-130">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="d23a6-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d23a6-131">OUTPUTS</span></span>

### <span data-ttu-id="d23a6-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d23a6-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="d23a6-133">To polecenie cmdlet modyfikuje istniejące wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="d23a6-133">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="d23a6-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d23a6-134">NOTES</span></span>

## <span data-ttu-id="d23a6-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d23a6-135">RELATED LINKS</span></span>

[<span data-ttu-id="d23a6-136">Dodaj-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="d23a6-136">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="d23a6-137">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d23a6-137">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d23a6-138">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="d23a6-138">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="d23a6-139">Nowe — AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="d23a6-139">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="d23a6-140">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d23a6-140">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
