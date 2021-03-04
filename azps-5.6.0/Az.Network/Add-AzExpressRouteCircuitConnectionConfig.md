---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 19ceeb045c3a7cc86dd9152ee08d12078d858240
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957057"
---
# <span data-ttu-id="4cc56-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4cc56-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="4cc56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cc56-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc56-103">Dodaje konfigurację połączenia obwodu do prywatnej komunikacji równorzędnej obwodu trasy expressowej.</span><span class="sxs-lookup"><span data-stu-id="4cc56-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="4cc56-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4cc56-104">SYNTAX</span></span>

### <span data-ttu-id="4cc56-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="4cc56-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cc56-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4cc56-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cc56-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4cc56-107">DESCRIPTION</span></span>
<span data-ttu-id="4cc56-108">Polecenie **cmdlet Add-AzExpressRouteCircuitConnectionConfig** dodaje konfigurację połączenia obwodu do prywatnej komunikacji równorzędnej dla obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4cc56-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="4cc56-109">Dzięki temu można komunikacji równorzędnej dwóch obwodów trasy expressowej w regionach lub subskrypcjach. Pamiętaj, że po uruchomieniu dodatku **AzExpressRouteCircuitConnectionConfig** musisz wywołać Set-AzExpressRouteCircuit cmdlet, aby aktywować konfigurację.</span><span class="sxs-lookup"><span data-stu-id="4cc56-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitConnectionConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="4cc56-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4cc56-110">EXAMPLES</span></span>

### <span data-ttu-id="4cc56-111">Przykład 1. Dodawanie zasobu połączenia obwodu do istniejącego obwodu expressRoute</span><span class="sxs-lookup"><span data-stu-id="4cc56-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
$addressPrefixType = 'IPv4'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="4cc56-112">Przykład 2. Dodawanie konfiguracji połączenia obwodu za pomocą połączeń rurowych do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="4cc56-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="4cc56-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cc56-113">PARAMETERS</span></span>

### <span data-ttu-id="4cc56-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4cc56-114">-AddressPrefix</span></span>
<span data-ttu-id="4cc56-115">Minimalna /29 przestrzeń adresowa klienta do tworzenia obwodów VxLan między obwodami tras ekspresowych dla ruchu IPv4.</span><span class="sxs-lookup"><span data-stu-id="4cc56-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="4cc56-116">lub co najmniej /125 przestrzeni adresowej klienta, aby utworzyć obwody VxLan między obwodami tras ekspresowych dla adresów IPv6.</span><span class="sxs-lookup"><span data-stu-id="4cc56-116">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="4cc56-117">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="4cc56-117">-AddressPrefixType</span></span>
<span data-ttu-id="4cc56-118">Ta opcja określa, do której rodziny adresowej należy prefiks.</span><span class="sxs-lookup"><span data-stu-id="4cc56-118">This specifies the Address Family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="4cc56-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="4cc56-119">-AuthorizationKey</span></span>
<span data-ttu-id="4cc56-120">Klucz autoryzacji do komunikacji równorzędnej obwodu trasy expressowej w innej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4cc56-120">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="4cc56-121">Autoryzację w obwodzie komunikacji równorzędnej można utworzyć przy użyciu istniejących poleceń.</span><span class="sxs-lookup"><span data-stu-id="4cc56-121">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="4cc56-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc56-122">-DefaultProfile</span></span>
<span data-ttu-id="4cc56-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4cc56-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cc56-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4cc56-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4cc56-125">Zmodyfikowany obwód expressroute.</span><span class="sxs-lookup"><span data-stu-id="4cc56-125">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="4cc56-126">Jest to obiekt platformy Azure zwrócony przez polecenie cmdlet **Get-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="4cc56-126">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="4cc56-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4cc56-127">-Name</span></span>
<span data-ttu-id="4cc56-128">Nazwa zasobu połączenia obwodu, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="4cc56-128">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="4cc56-129">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="4cc56-129">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="4cc56-130">Identyfikator zasobu dla prywatnej komunikacji równorzędnej obwodu zdalnego, który będzie równorzędny z bieżącym obwodem.</span><span class="sxs-lookup"><span data-stu-id="4cc56-130">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="4cc56-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4cc56-131">-Confirm</span></span>
<span data-ttu-id="4cc56-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4cc56-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cc56-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cc56-133">-WhatIf</span></span>
<span data-ttu-id="4cc56-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cc56-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4cc56-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4cc56-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cc56-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc56-136">CommonParameters</span></span>
<span data-ttu-id="4cc56-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cc56-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc56-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cc56-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc56-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cc56-139">INPUTS</span></span>

### <span data-ttu-id="4cc56-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4cc56-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="4cc56-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4cc56-141">System.String</span></span>

## <span data-ttu-id="4cc56-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cc56-142">OUTPUTS</span></span>

### <span data-ttu-id="4cc56-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4cc56-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4cc56-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4cc56-144">NOTES</span></span>

## <span data-ttu-id="4cc56-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cc56-145">RELATED LINKS</span></span>

[<span data-ttu-id="4cc56-146">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4cc56-146">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="4cc56-147">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4cc56-147">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="4cc56-148">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4cc56-148">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="4cc56-149">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4cc56-149">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="4cc56-150">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4cc56-150">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)