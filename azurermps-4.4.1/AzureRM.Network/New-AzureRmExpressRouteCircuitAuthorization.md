---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2fec428adb2ba8621d09a1f0ae5e762cdbe4b913
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718513"
---
# <span data-ttu-id="eba41-101">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="eba41-101">New-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="eba41-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eba41-102">SYNOPSIS</span></span>
<span data-ttu-id="eba41-103">Umożliwia utworzenie autoryzacji obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="eba41-103">Creates an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eba41-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eba41-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eba41-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eba41-105">DESCRIPTION</span></span>
<span data-ttu-id="eba41-106">Polecenie cmdlet **New-AzureRmExpressRouteCircuitAuthorization** umożliwia utworzenie autoryzacji obwodu, którą można dodać do obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="eba41-106">The **New-AzureRmExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="eba41-107">Obwody ExpressRoute łączą sieć lokalną z chmurą firmy Microsoft, korzystając z dostawcy usług łączności zamiast z publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="eba41-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="eba41-108">Właściciel obwodu ExpressRoute może utworzyć maksymalnie 10 zezwoleń dla każdego obwodu; te pozwolenia generują klucz autoryzacji, który może być wykorzystywany przez właściciela sieci wirtualnej w celu połączenia sieci z obwodem.</span><span class="sxs-lookup"><span data-stu-id="eba41-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="eba41-109">Istnieje tylko jedna autoryzacja na sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="eba41-109">There can only one authorization per virtual network.</span></span>

<span data-ttu-id="eba41-110">Po utworzeniu obwodu ExpressRoute możesz dodać autoryzację do tego obwodu za pomocą **dodatku Add-AzureRmExpressRouteCircuitAuthorization** .</span><span class="sxs-lookup"><span data-stu-id="eba41-110">After you create an ExpressRoute circuit you can use **Add-AzureRmExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="eba41-111">Możesz też użyć **nowych — AzureRmExpressRouteCircuitAuthorization** , aby utworzyć autoryzację, którą można dodać do nowego obwodu w trakcie tworzenia obwodu.</span><span class="sxs-lookup"><span data-stu-id="eba41-111">Alternatively, you can use **New-AzureRmExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="eba41-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eba41-112">EXAMPLES</span></span>

### <span data-ttu-id="eba41-113">Przykład 1. Tworzenie nowego zezwolenia na obwód</span><span class="sxs-lookup"><span data-stu-id="eba41-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="eba41-114">To polecenie tworzy nowy element autoryzacji obwodu o nazwie ContosoCircuitAuthorization, a następnie zapisuje ten obiekt w zmiennej o nazwie $Authorization.</span><span class="sxs-lookup"><span data-stu-id="eba41-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="eba41-115">Zapisanie obiektu jako zmiennej jest ważne: Chociaż **nowe-AzureRmExpressRouteCircuitAuthorization** mogą utworzyć autoryzację obwodu, nie może ona dodać tej autoryzacji do trasy obwodu.</span><span class="sxs-lookup"><span data-stu-id="eba41-115">Saving the object to a variable is important: although **New-AzureRmExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="eba41-116">Zamiast tego zmienna $Authorization jest używana New-AzureRmExpressRouteCircuit podczas tworzenia nowego obwodu ExpressRoute marki.</span><span class="sxs-lookup"><span data-stu-id="eba41-116">Instead, the variable $Authorization is used New-AzureRmExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>

<span data-ttu-id="eba41-117">Aby uzyskać więcej informacji, zobacz dokumentację New-AzureRmExpressRouteCircuit polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eba41-117">For more information, see the documentation for the New-AzureRmExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="eba41-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eba41-118">PARAMETERS</span></span>

### <span data-ttu-id="eba41-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eba41-119">-Name</span></span>
<span data-ttu-id="eba41-120">Określa unikatową nazwę dla nowej autoryzacji obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="eba41-120">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="eba41-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba41-121">-DefaultProfile</span></span>
<span data-ttu-id="eba41-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eba41-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eba41-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba41-123">CommonParameters</span></span>
<span data-ttu-id="eba41-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eba41-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba41-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eba41-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba41-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eba41-126">INPUTS</span></span>

### <span data-ttu-id="eba41-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="eba41-127">None</span></span>
<span data-ttu-id="eba41-128">To polecenie cmdlet nie akceptuje danych wejściowych potoku.</span><span class="sxs-lookup"><span data-stu-id="eba41-128">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="eba41-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eba41-129">OUTPUTS</span></span>

### <span data-ttu-id="eba41-130">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="eba41-130">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="eba41-131">To polecenie cmdlet tworzy wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitAuthorization** .</span><span class="sxs-lookup"><span data-stu-id="eba41-131">This cmdlet creates instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="eba41-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eba41-132">NOTES</span></span>

## <span data-ttu-id="eba41-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eba41-133">RELATED LINKS</span></span>

[<span data-ttu-id="eba41-134">Dodaj-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="eba41-134">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="eba41-135">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="eba41-135">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="eba41-136">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="eba41-136">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)
