---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184746"
---
# <span data-ttu-id="d7999-101">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="d7999-101">Get-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="d7999-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7999-102">SYNOPSIS</span></span>
<span data-ttu-id="d7999-103">Pobiera informacje o autoryzacjach obwodów w układzie ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d7999-103">Gets information about ExpressRoute circuit authorizations.</span></span>

## <span data-ttu-id="d7999-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d7999-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7999-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d7999-105">DESCRIPTION</span></span>
<span data-ttu-id="d7999-106">Polecenie **cmdlet Get-AzExpressRouteCircuitAuthorization** pobiera informacje o autoryzacjach przypisanych do obwodu expressRoute.</span><span class="sxs-lookup"><span data-stu-id="d7999-106">The **Get-AzExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="d7999-107">Obwody usługi ExpressRoute łączą Twoją sieć lokalną z chmurą firmy Microsoft przy użyciu dostawcy łączności zamiast publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="d7999-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="d7999-108">Właściciel obwodu expressRoute może utworzyć aż 10 autoryzacji dla każdego obwodu. te autoryzacje generują klucz autoryzacji, za pomocą których właściciel sieci wirtualnej może połączyć swoją sieć z obwodem (jedna autoryzacja na sieć wirtualną).</span><span class="sxs-lookup"><span data-stu-id="d7999-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="d7999-109">Klucze autoryzacji, a także inne informacje o autoryzacji, można wyświetlić w dowolnym momencie, uruchamiając **get-AzExpressRouteCircuitAuthorization.**</span><span class="sxs-lookup"><span data-stu-id="d7999-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="d7999-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d7999-110">EXAMPLES</span></span>

### <span data-ttu-id="d7999-111">Przykład 1. Uzyskiwanie wszystkich autoryzacji w uchcie ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="d7999-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="d7999-112">Te polecenia zwracają informacje o wszystkich autoryzacjach w układzie ExpressRoute skojarzonych z obwodem expressRoute.</span><span class="sxs-lookup"><span data-stu-id="d7999-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="d7999-113">Pierwsze polecenie tworzy odwołanie do obiektu w obwodzie o nazwie ContosoCircuit za pomocą polecenia cmdlet **Get-AzExpressRouteCircuit.** to odwołanie do obiektu jest przechowywane w zmiennej $Circuit.</span><span class="sxs-lookup"><span data-stu-id="d7999-113">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="d7999-114">Drugie polecenie używa następnie tego odwołania do obiektu i polecenia **cmdlet Get-AzExpressRouteCircuitAuthorization** w celu zwrócenia informacji o autoryzacjach skojarzonych z ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="d7999-114">The second command then uses that object reference and the **Get-AzExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="d7999-115">Przykład 2. Uzyskiwanie wszystkich autoryzacji usługi ExpressRoute przy użyciu Where-Object cmdlet</span><span class="sxs-lookup"><span data-stu-id="d7999-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="d7999-116">Te polecenia reprezentują odmianę poleceń użytych w przykładzie 1.</span><span class="sxs-lookup"><span data-stu-id="d7999-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="d7999-117">W tym przypadku jednak informacje są zwracane tylko dla tych autoryzacji, które są dostępne do użycia (czyli dla autoryzacji, które nie zostały przypisane do sieci wirtualnej).</span><span class="sxs-lookup"><span data-stu-id="d7999-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="d7999-118">W tym celu informacje autoryzacji obwodu są zwracane w poleceniu 2 i są przekierowywane do polecenia cmdlet **Where-Object.**</span><span class="sxs-lookup"><span data-stu-id="d7999-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="d7999-119">**Następnie obiekt Where-Object** wybiera tylko te autoryzacje, dla których właściwość *AuthorizationUseStatus* jest ustawiona na Dostępny.</span><span class="sxs-lookup"><span data-stu-id="d7999-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="d7999-120">Aby wyświetlić listę tylko tych uprawnień, które nie są dostępne, należy użyć tej składni dla klauzuli Where: `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="d7999-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="d7999-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7999-121">PARAMETERS</span></span>

### <span data-ttu-id="d7999-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7999-122">-DefaultProfile</span></span>
<span data-ttu-id="d7999-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7999-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7999-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d7999-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="d7999-125">Określa autoryzację obwodu w układzie ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d7999-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="d7999-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d7999-126">-Name</span></span>
<span data-ttu-id="d7999-127">Określa nazwę autoryzacji obwodu expressRoute, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7999-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="d7999-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="d7999-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="d7999-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7999-129">CommonParameters</span></span>
<span data-ttu-id="d7999-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7999-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7999-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7999-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7999-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7999-132">INPUTS</span></span>

### <span data-ttu-id="d7999-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d7999-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d7999-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7999-134">OUTPUTS</span></span>

### <span data-ttu-id="d7999-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="d7999-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="d7999-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d7999-136">NOTES</span></span>

## <span data-ttu-id="d7999-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7999-137">RELATED LINKS</span></span>

[<span data-ttu-id="d7999-138">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="d7999-138">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="d7999-139">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d7999-139">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="d7999-140">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="d7999-140">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="d7999-141">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="d7999-141">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)
