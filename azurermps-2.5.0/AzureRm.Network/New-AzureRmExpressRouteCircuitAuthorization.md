---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: f0e66c1e601ab63eec6d2540edd3ba0235727e9a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898294"
---
# <span data-ttu-id="557e2-101">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="557e2-101">New-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="557e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="557e2-102">SYNOPSIS</span></span>
<span data-ttu-id="557e2-103">Umożliwia utworzenie autoryzacji obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="557e2-103">Creates an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="557e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="557e2-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="557e2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="557e2-105">DESCRIPTION</span></span>
<span data-ttu-id="557e2-106">Polecenie cmdlet **New-AzureRmExpressRouteCircuitAuthorization** umożliwia utworzenie autoryzacji obwodu, którą można dodać do obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="557e2-106">The **New-AzureRmExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="557e2-107">Obwody ExpressRoute łączą sieć lokalną z chmurą firmy Microsoft, korzystając z dostawcy usług łączności zamiast z publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="557e2-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="557e2-108">Właściciel obwodu ExpressRoute może utworzyć maksymalnie 10 zezwoleń dla każdego obwodu; te pozwolenia generują klucz autoryzacji, który może być wykorzystywany przez właściciela sieci wirtualnej w celu połączenia sieci z obwodem.</span><span class="sxs-lookup"><span data-stu-id="557e2-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="557e2-109">Istnieje tylko jedna autoryzacja na sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="557e2-109">There can only one authorization per virtual network.</span></span>

<span data-ttu-id="557e2-110">Po utworzeniu obwodu ExpressRoute możesz dodać autoryzację do tego obwodu za pomocą **dodatku Add-AzureRmExpressRouteCircuitAuthorization** .</span><span class="sxs-lookup"><span data-stu-id="557e2-110">After you create an ExpressRoute circuit you can use **Add-AzureRmExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="557e2-111">Możesz też użyć **nowych — AzureRmExpressRouteCircuitAuthorization** , aby utworzyć autoryzację, którą można dodać do nowego obwodu w trakcie tworzenia obwodu.</span><span class="sxs-lookup"><span data-stu-id="557e2-111">Alternatively, you can use **New-AzureRmExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="557e2-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="557e2-112">EXAMPLES</span></span>

### <span data-ttu-id="557e2-113">Przykład 1. Tworzenie nowego zezwolenia na obwód</span><span class="sxs-lookup"><span data-stu-id="557e2-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="557e2-114">To polecenie tworzy nowy element autoryzacji obwodu o nazwie ContosoCircuitAuthorization, a następnie zapisuje ten obiekt w zmiennej o nazwie $Authorization.</span><span class="sxs-lookup"><span data-stu-id="557e2-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="557e2-115">Zapisanie obiektu jako zmiennej jest ważne: Chociaż **nowe-AzureRmExpressRouteCircuitAuthorization** mogą utworzyć autoryzację obwodu, nie może ona dodać tej autoryzacji do trasy obwodu.</span><span class="sxs-lookup"><span data-stu-id="557e2-115">Saving the object to a variable is important: although **New-AzureRmExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="557e2-116">Zamiast tego zmienna $Authorization jest używana New-AzureRmExpressRouteCircuit podczas tworzenia nowego obwodu ExpressRoute marki.</span><span class="sxs-lookup"><span data-stu-id="557e2-116">Instead, the variable $Authorization is used New-AzureRmExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>

<span data-ttu-id="557e2-117">Aby uzyskać więcej informacji, zobacz dokumentację New-AzureRmExpressRouteCircuit polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="557e2-117">For more information, see the documentation for the New-AzureRmExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="557e2-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="557e2-118">PARAMETERS</span></span>

### <span data-ttu-id="557e2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="557e2-119">-DefaultProfile</span></span>
<span data-ttu-id="557e2-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="557e2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="557e2-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="557e2-121">-Name</span></span>
<span data-ttu-id="557e2-122">Określa unikatową nazwę dla nowej autoryzacji obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="557e2-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="557e2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="557e2-123">CommonParameters</span></span>
<span data-ttu-id="557e2-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="557e2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="557e2-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="557e2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="557e2-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="557e2-126">INPUTS</span></span>

### <span data-ttu-id="557e2-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="557e2-127">None</span></span>
<span data-ttu-id="557e2-128">To polecenie cmdlet nie akceptuje danych wejściowych potoku.</span><span class="sxs-lookup"><span data-stu-id="557e2-128">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="557e2-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="557e2-129">OUTPUTS</span></span>

### <span data-ttu-id="557e2-130">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="557e2-130">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="557e2-131">To polecenie cmdlet tworzy wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitAuthorization** .</span><span class="sxs-lookup"><span data-stu-id="557e2-131">This cmdlet creates instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="557e2-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="557e2-132">NOTES</span></span>

## <span data-ttu-id="557e2-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="557e2-133">RELATED LINKS</span></span>

[<span data-ttu-id="557e2-134">Dodaj-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="557e2-134">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="557e2-135">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="557e2-135">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="557e2-136">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="557e2-136">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

