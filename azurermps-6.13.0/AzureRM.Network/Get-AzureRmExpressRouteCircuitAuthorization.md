---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 5b277ca35071c3639a3c7b341451cea78c024901
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553523"
---
# <span data-ttu-id="33967-101">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="33967-101">Get-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="33967-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33967-102">SYNOPSIS</span></span>
<span data-ttu-id="33967-103">Pobiera informacje na temat autoryzacji obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="33967-103">Gets information about ExpressRoute circuit authorizations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33967-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33967-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33967-105">Opis</span><span class="sxs-lookup"><span data-stu-id="33967-105">DESCRIPTION</span></span>
<span data-ttu-id="33967-106">Polecenie cmdlet **Get-AzureRmExpressRouteCircuitAuthorization** pobiera informacje o autoryzacjach przypisanych do obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="33967-106">The **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="33967-107">Obwody ExpressRoute łączą sieć lokalną z chmurą firmy Microsoft, korzystając z dostawcy usług łączności zamiast z publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="33967-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="33967-108">Właściciel obwodu ExpressRoute może utworzyć maksymalnie 10 zezwoleń dla każdego obwodu; te autoryzacje generują klucz autoryzacji, który może być wykorzystywany przez właściciela sieci wirtualnej w celu podłączenia sieci do obwodu (jednej autoryzacji na sieć wirtualną).</span><span class="sxs-lookup"><span data-stu-id="33967-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="33967-109">Klucze autoryzacji, a także inne informacje o autoryzacji można wyświetlać w dowolnym momencie, uruchamiając polecenie **Get-AzureRmExpressRouteCircuitAuthorization**.</span><span class="sxs-lookup"><span data-stu-id="33967-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzureRmExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="33967-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33967-110">EXAMPLES</span></span>

### <span data-ttu-id="33967-111">Przykład 1: pobieranie wszystkich autoryzacji ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="33967-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="33967-112">Te polecenia zwracają informacje dotyczące wszystkich autoryzacji ExpressRoute skojarzonych z obwodem ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="33967-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="33967-113">W pierwszym poleceniu użyto polecenia cmdlet **Get-AzureRmExpressRouteCircuit** w celu utworzenia odwołania do obiektu o obwodzie o nazwie ContosoCircuit; odwołanie do tego obiektu jest przechowywane w zmiennej $Circuit.</span><span class="sxs-lookup"><span data-stu-id="33967-113">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="33967-114">Drugie polecenie korzysta z tego odwołania do obiektu i polecenia cmdlet **Get-AzureRmExpressRouteCircuitAuthorization** w celu zwrócenia informacji o autoryzacjach skojarzonych z ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="33967-114">The second command then uses that object reference and the **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="33967-115">Przykład 2: uzyskiwanie wszystkich autoryzacji ExpressRoute za pomocą polecenia cmdlet Where-Object</span><span class="sxs-lookup"><span data-stu-id="33967-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="33967-116">Te polecenia reprezentują odmianę poleceń używanych w przykładzie 1.</span><span class="sxs-lookup"><span data-stu-id="33967-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="33967-117">Jednak w tym przypadku informacje są zwracane tylko w przypadku tych autoryzacji, które są dostępne do użytku (czyli dla autoryzacji, które nie zostały przypisane do sieci wirtualnej).</span><span class="sxs-lookup"><span data-stu-id="33967-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="33967-118">W tym celu informacje o autoryzacji obwodu są zwracane w poleceniu 2 i są przełączane do polecenia cmdlet **WHERE-Object** .</span><span class="sxs-lookup"><span data-stu-id="33967-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="33967-119">**Gdzie-Object** wybiera tylko te pozwolenia, w których właściwość *AuthorizationUseStatus* jest ustawiona jako dostępna.</span><span class="sxs-lookup"><span data-stu-id="33967-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="33967-120">Aby wyświetlić listę tylko tych autoryzacji, które są niedostępne, użyj następującej składni dla klauzuli WHERE: `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="33967-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="33967-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33967-121">PARAMETERS</span></span>

### <span data-ttu-id="33967-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33967-122">-DefaultProfile</span></span>
<span data-ttu-id="33967-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="33967-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33967-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="33967-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="33967-125">Określa autoryzację obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="33967-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="33967-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="33967-126">-Name</span></span>
<span data-ttu-id="33967-127">Określa nazwę autoryzacji obwodu ExpressRoute, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33967-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="33967-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="33967-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="33967-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33967-129">CommonParameters</span></span>
<span data-ttu-id="33967-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33967-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33967-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33967-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33967-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33967-132">INPUTS</span></span>

### <span data-ttu-id="33967-133">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="33967-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="33967-134">Parametry: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="33967-134">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="33967-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33967-135">OUTPUTS</span></span>

### <span data-ttu-id="33967-136">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="33967-136">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="33967-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33967-137">NOTES</span></span>

## <span data-ttu-id="33967-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33967-138">RELATED LINKS</span></span>

[<span data-ttu-id="33967-139">Dodaj-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="33967-139">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="33967-140">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="33967-140">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="33967-141">Nowe — AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="33967-141">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="33967-142">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="33967-142">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)
