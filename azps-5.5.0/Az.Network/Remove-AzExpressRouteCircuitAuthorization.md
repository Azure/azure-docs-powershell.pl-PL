---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191778"
---
# <span data-ttu-id="baae7-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="baae7-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="baae7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baae7-102">SYNOPSIS</span></span>
<span data-ttu-id="baae7-103">Usuwa istniejącą autoryzację konfiguracji usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="baae7-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="baae7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="baae7-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baae7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="baae7-105">DESCRIPTION</span></span>
<span data-ttu-id="baae7-106">Polecenie **cmdlet Remove-AzExpressRouteCircuitAuthorization** usuwa autoryzację przypisaną do obwodu expressRoute.</span><span class="sxs-lookup"><span data-stu-id="baae7-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="baae7-107">Obwody usługi ExpressRoute łączą Twoją sieć lokalną z platformą Azure przy użyciu dostawcy łączności zamiast publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="baae7-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="baae7-108">Właściciel obwodu expressRoute może utworzyć aż 10 autoryzacji dla każdego obwodu. te autoryzacje generują klucz autoryzacji, za pomocą których właściciel sieci wirtualnej może połączyć swoją sieć z obwodem.</span><span class="sxs-lookup"><span data-stu-id="baae7-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="baae7-109">W przypadku jednej sieci wirtualnej może być tylko jedna autoryzacja.</span><span class="sxs-lookup"><span data-stu-id="baae7-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="baae7-110">Jednak w dowolnym momencie właściciel obwodu może użyć funkcji **Remove-AzExpressRouteCircuitAuthorization** w celu usunięcia autoryzacji przypisanej do sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="baae7-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="baae7-111">W takim przypadku odpowiednia sieć wirtualna nie może już łączyć się z platformą Azure za pomocą obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="baae7-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="baae7-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="baae7-112">EXAMPLES</span></span>

### <span data-ttu-id="baae7-113">Przykład 1. Usuwanie autoryzacji obwodu z obwodu w układzie ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="baae7-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="baae7-114">W tym przykładzie autoryzacja obwodu jest usuwana z obwodu w układzie ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="baae7-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="baae7-115">Pierwsze polecenie używa polecenia cmdlet **Get-AzExpressRouteCircuit** w celu utworzenia odwołania do obiektu obwodu usługi ExpressRoute o nazwie ContosoCircuit i przechowuje wynik w zmiennej o nazwie $Circuit.</span><span class="sxs-lookup"><span data-stu-id="baae7-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="baae7-116">Drugie polecenie oznacza autoryzację obwodu ContosoCircuitAuthorization do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="baae7-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="baae7-117">Trzecie polecenie używa Set-AzExpressRouteCircuit cmdlet w celu potwierdzenia usunięcia obwodu usługi ExpressRoute przechowywanego w $Circuit danych.</span><span class="sxs-lookup"><span data-stu-id="baae7-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="baae7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="baae7-118">PARAMETERS</span></span>

### <span data-ttu-id="baae7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baae7-119">-DefaultProfile</span></span>
<span data-ttu-id="baae7-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="baae7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baae7-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="baae7-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="baae7-122">Określa obiekt ExpressRouteCircuit, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baae7-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="baae7-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="baae7-123">-Name</span></span>
<span data-ttu-id="baae7-124">Określa nazwę autoryzacji obwodu, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baae7-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="baae7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baae7-125">CommonParameters</span></span>
<span data-ttu-id="baae7-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baae7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baae7-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baae7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baae7-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="baae7-128">INPUTS</span></span>

### <span data-ttu-id="baae7-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="baae7-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="baae7-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="baae7-130">OUTPUTS</span></span>

### <span data-ttu-id="baae7-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="baae7-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="baae7-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="baae7-132">NOTES</span></span>

## <span data-ttu-id="baae7-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="baae7-133">RELATED LINKS</span></span>

[<span data-ttu-id="baae7-134">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="baae7-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="baae7-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="baae7-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="baae7-136">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="baae7-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="baae7-137">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="baae7-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="baae7-138">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="baae7-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
