---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489958"
---
# <span data-ttu-id="64201-101">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="64201-101">Get-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="64201-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64201-102">SYNOPSIS</span></span>
<span data-ttu-id="64201-103">Pobiera informacje na temat autoryzacji obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="64201-103">Gets information about ExpressRoute circuit authorizations.</span></span>

## <span data-ttu-id="64201-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64201-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64201-105">Opis</span><span class="sxs-lookup"><span data-stu-id="64201-105">DESCRIPTION</span></span>
<span data-ttu-id="64201-106">Polecenie cmdlet **Get-AzExpressRouteCircuitAuthorization** pobiera informacje o autoryzacjach przypisanych do obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="64201-106">The **Get-AzExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="64201-107">Obwody ExpressRoute łączą sieć lokalną z chmurą firmy Microsoft, korzystając z dostawcy usług łączności zamiast z publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="64201-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="64201-108">Właściciel obwodu ExpressRoute może utworzyć maksymalnie 10 zezwoleń dla każdego obwodu; te autoryzacje generują klucz autoryzacji, który może być wykorzystywany przez właściciela sieci wirtualnej w celu podłączenia sieci do obwodu (jednej autoryzacji na sieć wirtualną).</span><span class="sxs-lookup"><span data-stu-id="64201-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="64201-109">Klucze autoryzacji, a także inne informacje o autoryzacji można wyświetlać w dowolnym momencie, uruchamiając polecenie **Get-AzExpressRouteCircuitAuthorization**.</span><span class="sxs-lookup"><span data-stu-id="64201-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="64201-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64201-110">EXAMPLES</span></span>

### <span data-ttu-id="64201-111">Przykład 1: pobieranie wszystkich autoryzacji ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="64201-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="64201-112">Te polecenia zwracają informacje dotyczące wszystkich autoryzacji ExpressRoute skojarzonych z obwodem ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="64201-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="64201-113">W pierwszym poleceniu użyto polecenia cmdlet **Get-AzExpressRouteCircuit** w celu utworzenia odwołania do obiektu o obwodzie o nazwie ContosoCircuit; odwołanie do tego obiektu jest przechowywane w zmiennej $Circuit.</span><span class="sxs-lookup"><span data-stu-id="64201-113">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="64201-114">Drugie polecenie korzysta z tego odwołania do obiektu i polecenia cmdlet **Get-AzExpressRouteCircuitAuthorization** w celu zwrócenia informacji o autoryzacjach skojarzonych z ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="64201-114">The second command then uses that object reference and the **Get-AzExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="64201-115">Przykład 2: uzyskiwanie wszystkich autoryzacji ExpressRoute za pomocą polecenia cmdlet Where-Object</span><span class="sxs-lookup"><span data-stu-id="64201-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="64201-116">Te polecenia reprezentują odmianę poleceń używanych w przykładzie 1.</span><span class="sxs-lookup"><span data-stu-id="64201-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="64201-117">Jednak w tym przypadku informacje są zwracane tylko w przypadku tych autoryzacji, które są dostępne do użytku (czyli dla autoryzacji, które nie zostały przypisane do sieci wirtualnej).</span><span class="sxs-lookup"><span data-stu-id="64201-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="64201-118">W tym celu informacje o autoryzacji obwodu są zwracane w poleceniu 2 i są przełączane do polecenia cmdlet **WHERE-Object** .</span><span class="sxs-lookup"><span data-stu-id="64201-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="64201-119">**Gdzie-Object** wybiera tylko te pozwolenia, w których właściwość *AuthorizationUseStatus* jest ustawiona jako dostępna.</span><span class="sxs-lookup"><span data-stu-id="64201-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="64201-120">Aby wyświetlić listę tylko tych autoryzacji, które są niedostępne, użyj następującej składni dla klauzuli WHERE: `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="64201-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="64201-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64201-121">PARAMETERS</span></span>

### <span data-ttu-id="64201-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64201-122">-DefaultProfile</span></span>
<span data-ttu-id="64201-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64201-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64201-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="64201-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="64201-125">Określa autoryzację obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="64201-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="64201-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="64201-126">-Name</span></span>
<span data-ttu-id="64201-127">Określa nazwę autoryzacji obwodu ExpressRoute, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64201-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="64201-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="64201-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="64201-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64201-129">CommonParameters</span></span>
<span data-ttu-id="64201-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64201-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64201-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64201-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64201-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64201-132">INPUTS</span></span>

### <span data-ttu-id="64201-133">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="64201-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="64201-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64201-134">OUTPUTS</span></span>

### <span data-ttu-id="64201-135">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="64201-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="64201-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64201-136">NOTES</span></span>

## <span data-ttu-id="64201-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64201-137">RELATED LINKS</span></span>

[<span data-ttu-id="64201-138">Dodaj-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="64201-138">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="64201-139">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="64201-139">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="64201-140">Nowe — AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="64201-140">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="64201-141">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="64201-141">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)
