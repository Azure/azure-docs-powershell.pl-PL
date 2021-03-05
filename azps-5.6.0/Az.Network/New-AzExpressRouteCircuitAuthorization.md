---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9c247784a9f890d97aee301383656f97ef9c7dd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995359"
---
# <span data-ttu-id="e342d-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e342d-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="e342d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e342d-102">SYNOPSIS</span></span>
<span data-ttu-id="e342d-103">Tworzy autoryzację obwodu w układzie ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e342d-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="e342d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e342d-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e342d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e342d-105">DESCRIPTION</span></span>
<span data-ttu-id="e342d-106">Polecenie **cmdlet New-AzExpressRouteCircuitAuthorization** tworzy autoryzację obwodu, która może zostać dodana do obwodu expressRoute.</span><span class="sxs-lookup"><span data-stu-id="e342d-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="e342d-107">Obwody usługi ExpressRoute łączą Twoją sieć lokalną z chmurą firmy Microsoft przy użyciu dostawcy łączności zamiast publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="e342d-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="e342d-108">Właściciel obwodu expressRoute może utworzyć aż 10 autoryzacji dla każdego obwodu. te autoryzacje generują klucz autoryzacji, za pomocą których właściciel sieci wirtualnej może połączyć sieć z obwodem.</span><span class="sxs-lookup"><span data-stu-id="e342d-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="e342d-109">W przypadku jednej sieci wirtualnej może być dostępna tylko jedna autoryzacja.</span><span class="sxs-lookup"><span data-stu-id="e342d-109">There can only one authorization per virtual network.</span></span>
<span data-ttu-id="e342d-110">Po utworzeniu obwodu expressRoute możesz użyć funkcji **Add-AzExpressRouteCircuitAuthorization** w celu dodania autoryzacji do tego obwodu.</span><span class="sxs-lookup"><span data-stu-id="e342d-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="e342d-111">Możesz również użyć funkcji **New-AzExpressRouteCircuitAuthorization,** aby utworzyć autoryzację, która może zostać dodana do nowego obwodu jednocześnie z utworzeniem obwodu.</span><span class="sxs-lookup"><span data-stu-id="e342d-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="e342d-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e342d-112">EXAMPLES</span></span>

### <span data-ttu-id="e342d-113">Przykład 1. Tworzenie nowej autoryzacji obwodu</span><span class="sxs-lookup"><span data-stu-id="e342d-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="e342d-114">To polecenie tworzy nową autoryzację obwodu o nazwie ContosoCircuitAuthorization, a następnie przechowuje ten obiekt w zmiennej o nazwie $Authorization.</span><span class="sxs-lookup"><span data-stu-id="e342d-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="e342d-115">Zapisywanie obiektu w zmiennej jest ważne: chociaż **new-AzExpressRouteCircuitAuthorization** może utworzyć autoryzację obwodu, nie może dodać tej autoryzacji do trasy obwodu.</span><span class="sxs-lookup"><span data-stu-id="e342d-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="e342d-116">Zamiast tego zmienna $Authorization używana New-AzExpressRouteCircuit podczas tworzenia zupełnie nowego obwodu expressRoute.</span><span class="sxs-lookup"><span data-stu-id="e342d-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>
<span data-ttu-id="e342d-117">Aby uzyskać więcej informacji, zapoznaj się z dokumentacją tego New-AzExpressRouteCircuit cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e342d-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="e342d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e342d-118">PARAMETERS</span></span>

### <span data-ttu-id="e342d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e342d-119">-DefaultProfile</span></span>
<span data-ttu-id="e342d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e342d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e342d-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e342d-121">-Name</span></span>
<span data-ttu-id="e342d-122">Określa unikatową nazwę dla nowej autoryzacji obwodu w układzie ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e342d-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="e342d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e342d-123">CommonParameters</span></span>
<span data-ttu-id="e342d-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e342d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e342d-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e342d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e342d-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e342d-126">INPUTS</span></span>

### <span data-ttu-id="e342d-127">Brak</span><span class="sxs-lookup"><span data-stu-id="e342d-127">None</span></span>

## <span data-ttu-id="e342d-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e342d-128">OUTPUTS</span></span>

### <span data-ttu-id="e342d-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e342d-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="e342d-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e342d-130">NOTES</span></span>

## <span data-ttu-id="e342d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e342d-131">RELATED LINKS</span></span>

[<span data-ttu-id="e342d-132">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e342d-132">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="e342d-133">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e342d-133">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="e342d-134">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e342d-134">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

