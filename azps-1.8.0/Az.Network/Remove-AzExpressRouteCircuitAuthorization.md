---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 62cfc4fc3555b9eb798a1d64c53b0b25e9abc14c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709148"
---
# <span data-ttu-id="894c0-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="894c0-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="894c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="894c0-102">SYNOPSIS</span></span>
<span data-ttu-id="894c0-103">Usuwa istniejącą autoryzację konfiguracji ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="894c0-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="894c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="894c0-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="894c0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="894c0-105">DESCRIPTION</span></span>
<span data-ttu-id="894c0-106">Polecenie cmdlet **Remove-AzExpressRouteCircuitAuthorization** usuwa autoryzację przypisaną do obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="894c0-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="894c0-107">ExpressRoute obwodów łączy się z siecią lokalną na platformie Azure, korzystając z dostawcy usług łączności zamiast z publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="894c0-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="894c0-108">Właściciel obwodu ExpressRoute może utworzyć maksymalnie 10 zezwoleń dla każdego obwodu; te pozwolenia generują klucz autoryzacji, który może być wykorzystywany przez właściciela sieci wirtualnej w celu podłączenia sieci do obwodu.</span><span class="sxs-lookup"><span data-stu-id="894c0-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="894c0-109">Może istnieć tylko jedna autoryzacja na sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="894c0-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="894c0-110">Jednak w dowolnym momencie właściciel obwodu może użyć narzędzia **Remove-AzExpressRouteCircuitAuthorization** w celu usunięcia autoryzacji przypisanej do sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="894c0-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="894c0-111">Gdy to nastąpi, odpowiednia sieć wirtualna nie może już używać obwodu ExpressRoute do łączenia się z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="894c0-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="894c0-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="894c0-112">EXAMPLES</span></span>

### <span data-ttu-id="894c0-113">Przykład 1: usuwanie autoryzacji obwodu z obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="894c0-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="894c0-114">W tym przykładzie jest usuwana autoryzacja obwodu ze obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="894c0-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="894c0-115">W pierwszym poleceniu użyto polecenia cmdlet **Get-AzExpressRouteCircuit** w celu utworzenia odwołania do obiektu dla obwodu ExpressRoute o nazwie ContosoCircuit i zapisanie wyniku w zmiennej o nazwie $Circuit.</span><span class="sxs-lookup"><span data-stu-id="894c0-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="894c0-116">Drugie polecenie oznacza ContosoCircuitAuthorization autoryzacji obwodu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="894c0-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="894c0-117">W trzecim poleceniu użyto polecenia cmdlet Set-AzExpressRouteCircuit w celu potwierdzenia usunięcia obwodu ExpressRoute przechowywanego w zmiennej $Circuit.</span><span class="sxs-lookup"><span data-stu-id="894c0-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="894c0-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="894c0-118">PARAMETERS</span></span>

### <span data-ttu-id="894c0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="894c0-119">-DefaultProfile</span></span>
<span data-ttu-id="894c0-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="894c0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="894c0-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="894c0-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="894c0-122">Określa obiekt ExpressRouteCircuit, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="894c0-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="894c0-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="894c0-123">-Name</span></span>
<span data-ttu-id="894c0-124">Określa nazwę autoryzacji obwodu usuniętego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="894c0-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="894c0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="894c0-125">CommonParameters</span></span>
<span data-ttu-id="894c0-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="894c0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="894c0-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="894c0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="894c0-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="894c0-128">INPUTS</span></span>

### <span data-ttu-id="894c0-129">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="894c0-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="894c0-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="894c0-130">OUTPUTS</span></span>

### <span data-ttu-id="894c0-131">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="894c0-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="894c0-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="894c0-132">NOTES</span></span>

## <span data-ttu-id="894c0-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="894c0-133">RELATED LINKS</span></span>

[<span data-ttu-id="894c0-134">Dodaj-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="894c0-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="894c0-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="894c0-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="894c0-136">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="894c0-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="894c0-137">Nowe — AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="894c0-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="894c0-138">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="894c0-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
