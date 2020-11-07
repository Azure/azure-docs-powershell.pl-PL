---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: 9b41eb0c95c2b1693e56c8b11fee86b6e49a4609
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898413"
---
# <span data-ttu-id="71917-101">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="71917-101">Add-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="71917-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71917-102">SYNOPSIS</span></span>
<span data-ttu-id="71917-103">Umożliwia dodanie autoryzacji obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="71917-103">Adds an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71917-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71917-104">SYNTAX</span></span>

```
Add-AzureRmExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71917-105">Opis</span><span class="sxs-lookup"><span data-stu-id="71917-105">DESCRIPTION</span></span>
<span data-ttu-id="71917-106">Polecenie cmdlet **Add-AzureRmExpressRouteCircuitAuthorization** umożliwia dodanie autoryzacji do obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="71917-106">The **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="71917-107">Obwody ExpressRoute łączą sieć lokalną z chmurą firmy Microsoft, korzystając z dostawcy usług łączności zamiast z publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="71917-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="71917-108">Właściciel obwodu ExpressRoute może utworzyć maksymalnie 10 zezwoleń dla każdego obwodu; te autoryzacje generują klucz autoryzacji, który może być wykorzystywany przez właściciela sieci wirtualnej w celu podłączenia sieci do obwodu (jednej autoryzacji na sieć wirtualną).</span><span class="sxs-lookup"><span data-stu-id="71917-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="71917-109">Polecenie **Add-AzureRmExpressRouteCircuitAuthorization** dodaje nową autoryzację do obwodu, a jednocześnie generuje odpowiedni klucz autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="71917-109">**Add-AzureRmExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="71917-110">Te klucze można wyświetlać w dowolnej chwili, uruchamiając polecenie cmdlet Get-AzureRmExpressRouteCircuitAuthorization, a w razie potrzeby można je skopiować i przesłać dalej do odpowiedniego właściciela sieci.</span><span class="sxs-lookup"><span data-stu-id="71917-110">These keys can be viewed at any time by running the Get-AzureRmExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>

<span data-ttu-id="71917-111">Uwaga: po uruchomieniu polecenia **Add-AzureRmExpressRouteCircuitAuthorization** musisz zadzwonić do polecenia cmdlet Set-AzureRmExpressRouteCircuit, aby aktywować klucz.</span><span class="sxs-lookup"><span data-stu-id="71917-111">Note that, after running **Add-AzureRmExpressRouteCircuitAuthorization** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="71917-112">Jeśli rozmowa nie jest **ustawiona na AzureRmExpressRouteCircuit** , autoryzacja zostanie dodana do obwodu, ale nie będzie można jej używać.</span><span class="sxs-lookup"><span data-stu-id="71917-112">If you do not call **Set-AzureRmExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="71917-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71917-113">EXAMPLES</span></span>

### <span data-ttu-id="71917-114">Przykład 1: Dodawanie autoryzacji do określonego obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="71917-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="71917-115">Polecenia w tym przykładzie dodają nowe pełnomocnictwo do istniejącego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="71917-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="71917-116">W pierwszym poleceniu użyto polecenia **Get-AzureRmExpressRouteCircuit** w celu utworzenia odwołania do obiektu dla obwodu o nazwie ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="71917-116">The first command uses **Get-AzureRmExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="71917-117">Odwołanie do obiektu jest przechowywane w zmiennej o nazwie $Circuit.</span><span class="sxs-lookup"><span data-stu-id="71917-117">That object reference is stored in a variable named $Circuit.</span></span>

<span data-ttu-id="71917-118">W drugim poleceniu polecenie cmdlet **Add-AzureRmExpressRouteCircuitAuthorization** jest używane do dodawania nowej autoryzacji (ContosoCircuitAuthorization) do obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="71917-118">In the second command, the **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="71917-119">To polecenie dodaje autoryzację, ale nie uaktywnia tej autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="71917-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="71917-120">Aktywowanie autoryzacji wymaga, aby w tym przykładzie **AzureRmExpressRouteCircuit** jest wyświetlany w ostatnim poleceniu.</span><span class="sxs-lookup"><span data-stu-id="71917-120">Activating an authorization requires the **Set-AzureRmExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="71917-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71917-121">PARAMETERS</span></span>

### <span data-ttu-id="71917-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71917-122">-DefaultProfile</span></span>
<span data-ttu-id="71917-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71917-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71917-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="71917-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="71917-125">Określa obwód ExpressRoute, do którego jest dodawane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71917-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="71917-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71917-126">-Name</span></span>
<span data-ttu-id="71917-127">Określa nazwę autoryzacji obwodu, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="71917-127">Specifies the name of the circuit authorization to be added.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71917-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71917-128">CommonParameters</span></span>
<span data-ttu-id="71917-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71917-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71917-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71917-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71917-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71917-131">INPUTS</span></span>

### <span data-ttu-id="71917-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="71917-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="71917-133">Polecenie **Add-AzureRmExpressRouteCircuitAuthorization** akceptuje potokowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="71917-133">**Add-AzureRmExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="71917-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71917-134">OUTPUTS</span></span>

### <span data-ttu-id="71917-135">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="71917-135">PSExpressRouteCircuit</span></span>
<span data-ttu-id="71917-136">Polecenie **Add-AzureRmExpressRouteCircuitAuthorization** modyfikuje instancje obiektu **Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="71917-136">**Add-AzureRmExpressRouteCircuitAuthorization** modifies instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="71917-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71917-137">NOTES</span></span>

## <span data-ttu-id="71917-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71917-138">RELATED LINKS</span></span>

[<span data-ttu-id="71917-139">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="71917-139">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="71917-140">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="71917-140">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="71917-141">Nowe — AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="71917-141">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="71917-142">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="71917-142">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="71917-143">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="71917-143">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
