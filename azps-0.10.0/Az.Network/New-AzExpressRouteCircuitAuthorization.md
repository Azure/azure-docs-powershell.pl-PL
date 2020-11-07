---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 0f17d30b6f47effab5b0039bd56172cbe580392c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890518"
---
# <span data-ttu-id="a0e86-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a0e86-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="a0e86-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0e86-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e86-103">Umożliwia utworzenie autoryzacji obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a0e86-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="a0e86-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0e86-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0e86-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a0e86-105">DESCRIPTION</span></span>
<span data-ttu-id="a0e86-106">Polecenie cmdlet **New-AzExpressRouteCircuitAuthorization** umożliwia utworzenie autoryzacji obwodu, którą można dodać do obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a0e86-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="a0e86-107">Obwody ExpressRoute łączą sieć lokalną z chmurą firmy Microsoft, korzystając z dostawcy usług łączności zamiast z publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="a0e86-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="a0e86-108">Właściciel obwodu ExpressRoute może utworzyć maksymalnie 10 zezwoleń dla każdego obwodu; te pozwolenia generują klucz autoryzacji, który może być wykorzystywany przez właściciela sieci wirtualnej w celu połączenia sieci z obwodem.</span><span class="sxs-lookup"><span data-stu-id="a0e86-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="a0e86-109">Istnieje tylko jedna autoryzacja na sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="a0e86-109">There can only one authorization per virtual network.</span></span>

<span data-ttu-id="a0e86-110">Po utworzeniu obwodu ExpressRoute możesz dodać autoryzację do tego obwodu za pomocą **dodatku Add-AzExpressRouteCircuitAuthorization** .</span><span class="sxs-lookup"><span data-stu-id="a0e86-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="a0e86-111">Możesz też użyć **nowych — AzExpressRouteCircuitAuthorization** , aby utworzyć autoryzację, którą można dodać do nowego obwodu w trakcie tworzenia obwodu.</span><span class="sxs-lookup"><span data-stu-id="a0e86-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="a0e86-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0e86-112">EXAMPLES</span></span>

### <span data-ttu-id="a0e86-113">Przykład 1. Tworzenie nowego zezwolenia na obwód</span><span class="sxs-lookup"><span data-stu-id="a0e86-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="a0e86-114">To polecenie tworzy nowy element autoryzacji obwodu o nazwie ContosoCircuitAuthorization, a następnie zapisuje ten obiekt w zmiennej o nazwie $Authorization.</span><span class="sxs-lookup"><span data-stu-id="a0e86-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="a0e86-115">Zapisanie obiektu jako zmiennej jest ważne: Chociaż **nowe-AzExpressRouteCircuitAuthorization** mogą utworzyć autoryzację obwodu, nie może ona dodać tej autoryzacji do trasy obwodu.</span><span class="sxs-lookup"><span data-stu-id="a0e86-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="a0e86-116">Zamiast tego zmienna $Authorization jest używana New-AzExpressRouteCircuit podczas tworzenia nowego obwodu ExpressRoute marki.</span><span class="sxs-lookup"><span data-stu-id="a0e86-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>

<span data-ttu-id="a0e86-117">Aby uzyskać więcej informacji, zobacz dokumentację New-AzExpressRouteCircuit polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0e86-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="a0e86-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0e86-118">PARAMETERS</span></span>

### <span data-ttu-id="a0e86-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e86-119">-DefaultProfile</span></span>
<span data-ttu-id="a0e86-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0e86-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0e86-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a0e86-121">-Name</span></span>
<span data-ttu-id="a0e86-122">Określa unikatową nazwę dla nowej autoryzacji obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a0e86-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="a0e86-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e86-123">CommonParameters</span></span>
<span data-ttu-id="a0e86-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0e86-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e86-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0e86-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e86-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0e86-126">INPUTS</span></span>

### <span data-ttu-id="a0e86-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a0e86-127">None</span></span>
<span data-ttu-id="a0e86-128">To polecenie cmdlet nie akceptuje danych wejściowych potoku.</span><span class="sxs-lookup"><span data-stu-id="a0e86-128">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="a0e86-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0e86-129">OUTPUTS</span></span>

### <span data-ttu-id="a0e86-130">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a0e86-130">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="a0e86-131">To polecenie cmdlet tworzy wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitAuthorization** .</span><span class="sxs-lookup"><span data-stu-id="a0e86-131">This cmdlet creates instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="a0e86-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0e86-132">NOTES</span></span>

## <span data-ttu-id="a0e86-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0e86-133">RELATED LINKS</span></span>

[<span data-ttu-id="a0e86-134">Dodaj-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a0e86-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="a0e86-135">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a0e86-135">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="a0e86-136">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a0e86-136">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

