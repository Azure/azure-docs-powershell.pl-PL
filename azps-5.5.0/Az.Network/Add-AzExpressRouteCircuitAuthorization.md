---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 047400472d3f42d5daff0f0ea6aed44455608eb3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193978"
---
# <span data-ttu-id="ef407-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ef407-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="ef407-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef407-102">SYNOPSIS</span></span>
<span data-ttu-id="ef407-103">Dodaje autoryzację obwodu w układzie ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ef407-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="ef407-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ef407-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef407-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ef407-105">DESCRIPTION</span></span>
<span data-ttu-id="ef407-106">Polecenie **cmdlet Add-AzExpressRouteCircuitAuthorization** powoduje dodanie autoryzacji do obwodu expressRoute.</span><span class="sxs-lookup"><span data-stu-id="ef407-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="ef407-107">Obwody usługi ExpressRoute łączą Twoją sieć lokalną z chmurą firmy Microsoft przy użyciu dostawcy łączności zamiast publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="ef407-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="ef407-108">Właściciel obwodu expressRoute może utworzyć aż 10 autoryzacji dla każdego obwodu. te autoryzacje generują klucz autoryzacji, za pomocą których właściciel sieci wirtualnej może połączyć swoją sieć z obwodem (jedna autoryzacja na sieć wirtualną).</span><span class="sxs-lookup"><span data-stu-id="ef407-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="ef407-109">**Dodatek AzExpressRouteCircuitAuthorization** dodaje nową autoryzację do obwodu, a jednocześnie generuje odpowiedni klucz autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="ef407-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="ef407-110">Te klucze można wyświetlić w dowolnym momencie, uruchamiając polecenie cmdlet Get-AzExpressRouteCircuitAuthorization, a następnie, w razie potrzeby, można je skopiować i przesyłać dalej do odpowiedniego właściciela sieci.</span><span class="sxs-lookup"><span data-stu-id="ef407-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="ef407-111">Zwróć uwagę, że po uruchomieniu dodatku **AzExpressRouteCircuitAuthorization** musisz wywołać Set-AzExpressRouteCircuit cmdlet, aby aktywować klucz.</span><span class="sxs-lookup"><span data-stu-id="ef407-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="ef407-112">Jeśli nie wywołasz **set-AzExpressRouteCircuit,** autoryzacja zostanie dodana do obwodu, ale nie będzie włączona do użycia.</span><span class="sxs-lookup"><span data-stu-id="ef407-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="ef407-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ef407-113">EXAMPLES</span></span>

### <span data-ttu-id="ef407-114">Przykład 1. Dodawanie autoryzacji do określonego obwodu usług ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="ef407-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="ef407-115">Polecenia w tym przykładzie dodają nową autoryzację do istniejącego obwodu expressRoute.</span><span class="sxs-lookup"><span data-stu-id="ef407-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="ef407-116">Pierwsze polecenie tworzy odwołanie do obiektu o nazwie ContosoCircuit za pomocą polecenia **Get-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="ef407-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="ef407-117">To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $Circuit.</span><span class="sxs-lookup"><span data-stu-id="ef407-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="ef407-118">W drugim poleceniu polecenie cmdlet **Add-AzExpressRouteCircuitAuthorization** służy do dodawania nowej autoryzacji (ContosoCircuitAuthorization) do obwodu expressRoute.</span><span class="sxs-lookup"><span data-stu-id="ef407-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="ef407-119">To polecenie powoduje dodanie autoryzacji, ale nie powoduje aktywowania tej autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="ef407-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="ef407-120">Aktywacja autoryzacji wymaga **ustawienia Set-AzExpressRouteCircuit** pokazanego w ostatnim poleceniu w przykładzie.</span><span class="sxs-lookup"><span data-stu-id="ef407-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="ef407-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef407-121">PARAMETERS</span></span>

### <span data-ttu-id="ef407-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef407-122">-DefaultProfile</span></span>
<span data-ttu-id="ef407-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef407-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef407-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ef407-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ef407-125">Określa obwód expressRoute, do który to polecenie cmdlet dodaje autoryzację.</span><span class="sxs-lookup"><span data-stu-id="ef407-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="ef407-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ef407-126">-Name</span></span>
<span data-ttu-id="ef407-127">Określa nazwę autoryzacji obwodu do dodania.</span><span class="sxs-lookup"><span data-stu-id="ef407-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="ef407-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef407-128">CommonParameters</span></span>
<span data-ttu-id="ef407-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef407-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef407-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef407-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef407-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef407-131">INPUTS</span></span>

### <span data-ttu-id="ef407-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ef407-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ef407-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ef407-133">OUTPUTS</span></span>

### <span data-ttu-id="ef407-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ef407-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ef407-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ef407-135">NOTES</span></span>

## <span data-ttu-id="ef407-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef407-136">RELATED LINKS</span></span>

[<span data-ttu-id="ef407-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ef407-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="ef407-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ef407-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="ef407-139">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ef407-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="ef407-140">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ef407-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="ef407-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ef407-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
