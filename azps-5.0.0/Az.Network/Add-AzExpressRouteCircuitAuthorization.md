---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 047400472d3f42d5daff0f0ea6aed44455608eb3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233973"
---
# <span data-ttu-id="919c8-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="919c8-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="919c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="919c8-102">SYNOPSIS</span></span>
<span data-ttu-id="919c8-103">Umożliwia dodanie autoryzacji obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="919c8-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="919c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="919c8-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="919c8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="919c8-105">DESCRIPTION</span></span>
<span data-ttu-id="919c8-106">Polecenie cmdlet **Add-AzExpressRouteCircuitAuthorization** umożliwia dodanie autoryzacji do obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="919c8-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="919c8-107">Obwody ExpressRoute łączą sieć lokalną z chmurą firmy Microsoft, korzystając z dostawcy usług łączności zamiast z publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="919c8-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="919c8-108">Właściciel obwodu ExpressRoute może utworzyć maksymalnie 10 zezwoleń dla każdego obwodu; te autoryzacje generują klucz autoryzacji, który może być wykorzystywany przez właściciela sieci wirtualnej w celu podłączenia sieci do obwodu (jednej autoryzacji na sieć wirtualną).</span><span class="sxs-lookup"><span data-stu-id="919c8-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="919c8-109">Polecenie **Add-AzExpressRouteCircuitAuthorization** dodaje nową autoryzację do obwodu, a jednocześnie generuje odpowiedni klucz autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="919c8-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="919c8-110">Te klucze można wyświetlać w dowolnej chwili, uruchamiając polecenie cmdlet Get-AzExpressRouteCircuitAuthorization, a w razie potrzeby można je skopiować i przesłać dalej do odpowiedniego właściciela sieci.</span><span class="sxs-lookup"><span data-stu-id="919c8-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="919c8-111">Uwaga: po uruchomieniu polecenia **Add-AzExpressRouteCircuitAuthorization** musisz zadzwonić do polecenia cmdlet Set-AzExpressRouteCircuit, aby aktywować klucz.</span><span class="sxs-lookup"><span data-stu-id="919c8-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="919c8-112">Jeśli rozmowa nie jest **ustawiona na AzExpressRouteCircuit** , autoryzacja zostanie dodana do obwodu, ale nie będzie można jej używać.</span><span class="sxs-lookup"><span data-stu-id="919c8-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="919c8-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="919c8-113">EXAMPLES</span></span>

### <span data-ttu-id="919c8-114">Przykład 1: Dodawanie autoryzacji do określonego obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="919c8-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="919c8-115">Polecenia w tym przykładzie dodają nowe pełnomocnictwo do istniejącego obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="919c8-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="919c8-116">W pierwszym poleceniu użyto polecenia **Get-AzExpressRouteCircuit** w celu utworzenia odwołania do obiektu dla obwodu o nazwie ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="919c8-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="919c8-117">Odwołanie do obiektu jest przechowywane w zmiennej o nazwie $Circuit.</span><span class="sxs-lookup"><span data-stu-id="919c8-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="919c8-118">W drugim poleceniu polecenie cmdlet **Add-AzExpressRouteCircuitAuthorization** jest używane do dodawania nowej autoryzacji (ContosoCircuitAuthorization) do obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="919c8-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="919c8-119">To polecenie dodaje autoryzację, ale nie uaktywnia tej autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="919c8-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="919c8-120">Aktywowanie autoryzacji wymaga, aby w tym przykładzie **AzExpressRouteCircuit** jest wyświetlany w ostatnim poleceniu.</span><span class="sxs-lookup"><span data-stu-id="919c8-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="919c8-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="919c8-121">PARAMETERS</span></span>

### <span data-ttu-id="919c8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="919c8-122">-DefaultProfile</span></span>
<span data-ttu-id="919c8-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="919c8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919c8-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="919c8-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="919c8-125">Określa obwód ExpressRoute, do którego jest dodawane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="919c8-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="919c8-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="919c8-126">-Name</span></span>
<span data-ttu-id="919c8-127">Określa nazwę autoryzacji obwodu, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="919c8-127">Specifies the name of the circuit authorization to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919c8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="919c8-128">CommonParameters</span></span>
<span data-ttu-id="919c8-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="919c8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="919c8-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="919c8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="919c8-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="919c8-131">INPUTS</span></span>

### <span data-ttu-id="919c8-132">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="919c8-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="919c8-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="919c8-133">OUTPUTS</span></span>

### <span data-ttu-id="919c8-134">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="919c8-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="919c8-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="919c8-135">NOTES</span></span>

## <span data-ttu-id="919c8-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="919c8-136">RELATED LINKS</span></span>

[<span data-ttu-id="919c8-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="919c8-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="919c8-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="919c8-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="919c8-139">Nowe — AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="919c8-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="919c8-140">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="919c8-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="919c8-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="919c8-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
