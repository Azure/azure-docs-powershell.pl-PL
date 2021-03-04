---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952049"
---
# <span data-ttu-id="6a153-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6a153-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="6a153-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a153-102">SYNOPSIS</span></span>
<span data-ttu-id="6a153-103">Aktualizuje konfigurację połączenia obwodu utworzoną w prywatnych komunikacji równorzędnych dla obwodu trasy expressowej.</span><span class="sxs-lookup"><span data-stu-id="6a153-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="6a153-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6a153-104">SYNTAX</span></span>

### <span data-ttu-id="6a153-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6a153-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a153-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6a153-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a153-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6a153-107">DESCRIPTION</span></span>
<span data-ttu-id="6a153-108">Polecenie **cmdlet Set-AzExpressRouteCircuitConnectionConfig** aktualizuje konfigurację połączenia obwodu utworzoną w prywatnej komunikacji równorzędnej dla obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6a153-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="6a153-109">Dzięki temu można komunikacji równorzędnej dwóch obwodów trasy expressowej w regionach lub subskrypcjach.</span><span class="sxs-lookup"><span data-stu-id="6a153-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="6a153-110">Pamiętaj, że przed uruchomieniem **set-azExpressRouteCircuitConnectionConfig** musisz dodać połączenie obwodu za pomocą dodatku **AzExpressRouteCircuitConnectionConfig.**</span><span class="sxs-lookup"><span data-stu-id="6a153-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="6a153-111">Ponadto po uruchomieniu **set-azExpressRouteCircuitPeeringConfig** musisz wywołać Set-AzExpressRouteCircuit cmdlet, aby aktywować konfigurację.</span><span class="sxs-lookup"><span data-stu-id="6a153-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="6a153-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6a153-112">EXAMPLES</span></span>

### <span data-ttu-id="6a153-113">Przykład 1. Aktualizowanie zasobu połączenia obwodu do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="6a153-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="6a153-114">Przykład 2. Konfigurowanie połączenia obwodu za pomocą połączeń rurowych do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="6a153-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="6a153-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a153-115">PARAMETERS</span></span>

### <span data-ttu-id="6a153-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6a153-116">-AddressPrefix</span></span>
<span data-ttu-id="6a153-117">Minimalna /29 przestrzeń adresowa klienta do tworzenia obwodów VxLan między obwodami tras ekspresowych dla ruchu IPv4.</span><span class="sxs-lookup"><span data-stu-id="6a153-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="6a153-118">lub co najmniej /125 przestrzeni adresowej klienta, aby utworzyć obwody VxLan między obwodami tras ekspresowych dla adresów IPv6.</span><span class="sxs-lookup"><span data-stu-id="6a153-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="6a153-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="6a153-119">-AddressPrefixType</span></span>
<span data-ttu-id="6a153-120">Określa rodzinę adresów, do której należy prefiks.</span><span class="sxs-lookup"><span data-stu-id="6a153-120">Specifies the address family that address prefix belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: IPv4
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a153-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="6a153-121">-AuthorizationKey</span></span>
<span data-ttu-id="6a153-122">Klucz autoryzacji do komunikacji równorzędnej obwodu trasy expressowej w innej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6a153-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="6a153-123">Autoryzację w obwodzie komunikacji równorzędnej można utworzyć przy użyciu istniejących poleceń.</span><span class="sxs-lookup"><span data-stu-id="6a153-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="6a153-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a153-124">-DefaultProfile</span></span>
<span data-ttu-id="6a153-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a153-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a153-126">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a153-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="6a153-127">Zmodyfikowany obwód expressroute.</span><span class="sxs-lookup"><span data-stu-id="6a153-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="6a153-128">Jest to obiekt platformy Azure zwrócony przez polecenie cmdlet **Get-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="6a153-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a153-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6a153-129">-Name</span></span>
<span data-ttu-id="6a153-130">Nazwa zasobu połączenia obwodu, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="6a153-130">The name of the circuit connection resource to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a153-131">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="6a153-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="6a153-132">Identyfikator zasobu dla prywatnej komunikacji równorzędnej obwodu zdalnego, który będzie równorzędny z bieżącym obwodem.</span><span class="sxs-lookup"><span data-stu-id="6a153-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a153-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a153-133">-Confirm</span></span>
<span data-ttu-id="6a153-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6a153-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a153-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a153-135">-WhatIf</span></span>
<span data-ttu-id="6a153-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a153-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a153-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6a153-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a153-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a153-138">CommonParameters</span></span>
<span data-ttu-id="6a153-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a153-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a153-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a153-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a153-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a153-141">INPUTS</span></span>

### <span data-ttu-id="6a153-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a153-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="6a153-143">System.String</span><span class="sxs-lookup"><span data-stu-id="6a153-143">System.String</span></span>

## <span data-ttu-id="6a153-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a153-144">OUTPUTS</span></span>

### <span data-ttu-id="6a153-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a153-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="6a153-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6a153-146">NOTES</span></span>

## <span data-ttu-id="6a153-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a153-147">RELATED LINKS</span></span>

[<span data-ttu-id="6a153-148">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6a153-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="6a153-149">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6a153-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="6a153-150">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6a153-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="6a153-151">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a153-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="6a153-152">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6a153-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
