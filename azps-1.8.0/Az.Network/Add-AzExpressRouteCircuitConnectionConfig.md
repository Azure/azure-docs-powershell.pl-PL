---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: bc08305d7aa604dd9c7540573ffb5a199e85b287
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402137"
---
# <span data-ttu-id="02db3-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="02db3-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="02db3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02db3-102">SYNOPSIS</span></span>
<span data-ttu-id="02db3-103">Dodaje konfigurację połączenia obwodu do prywatnej komunikacji równorzędnej obwodu trasy expressowej.</span><span class="sxs-lookup"><span data-stu-id="02db3-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="02db3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="02db3-104">SYNTAX</span></span>

### <span data-ttu-id="02db3-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="02db3-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02db3-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="02db3-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02db3-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="02db3-107">DESCRIPTION</span></span>
<span data-ttu-id="02db3-108">Polecenie **cmdlet Add-AzExpressRouteCircuitConnectionConfig** dodaje konfigurację połączenia obwodu do prywatnej komunikacji równorzędnej dla obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="02db3-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="02db3-109">Dzięki temu można komunikacji równorzędnej dwóch obwodów trasy expressowej w regionach lub subskrypcjach. Pamiętaj, że po uruchomieniu dodatku **AzExpressRouteCircuitPeeringConfig** musisz wywołać Set-AzExpressRouteCircuit cmdlet, aby aktywować konfigurację.</span><span class="sxs-lookup"><span data-stu-id="02db3-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="02db3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="02db3-110">EXAMPLES</span></span>

### <span data-ttu-id="02db3-111">Przykład 1. Dodawanie zasobu połączenia obwodu do istniejącego obwodu expressRoute</span><span class="sxs-lookup"><span data-stu-id="02db3-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="02db3-112">Przykład 2. Dodawanie konfiguracji połączenia obwodu za pomocą połączeń rurowych do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="02db3-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="02db3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02db3-113">PARAMETERS</span></span>

### <span data-ttu-id="02db3-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="02db3-114">-AddressPrefix</span></span>
<span data-ttu-id="02db3-115">Minimalna /29 przestrzeń adresowa klienta do tworzenia obwodów VxLan między obwodami tras ekspresowych</span><span class="sxs-lookup"><span data-stu-id="02db3-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="02db3-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="02db3-116">-AuthorizationKey</span></span>
<span data-ttu-id="02db3-117">Klucz autoryzacji do komunikacji równorzędnej obwodu trasy expressowej w innej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="02db3-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="02db3-118">Autoryzację w obwodzie komunikacji równorzędnej można utworzyć przy użyciu istniejących poleceń.</span><span class="sxs-lookup"><span data-stu-id="02db3-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="02db3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02db3-119">-DefaultProfile</span></span>
<span data-ttu-id="02db3-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="02db3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02db3-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="02db3-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="02db3-122">Zmodyfikowany obwód expressroute.</span><span class="sxs-lookup"><span data-stu-id="02db3-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="02db3-123">Jest to obiekt platformy Azure zwrócony przez polecenie cmdlet **Get-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="02db3-123">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="02db3-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="02db3-124">-Name</span></span>
<span data-ttu-id="02db3-125">Nazwa zasobu połączenia obwodu, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="02db3-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="02db3-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="02db3-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="02db3-127">Identyfikator zasobu dla prywatnej komunikacji równorzędnej obwodu zdalnego, który będzie równorzędny z bieżącym obwodem.</span><span class="sxs-lookup"><span data-stu-id="02db3-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="02db3-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02db3-128">-Confirm</span></span>
<span data-ttu-id="02db3-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="02db3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02db3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02db3-130">-WhatIf</span></span>
<span data-ttu-id="02db3-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02db3-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02db3-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="02db3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02db3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02db3-133">CommonParameters</span></span>
<span data-ttu-id="02db3-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02db3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02db3-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02db3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02db3-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02db3-136">INPUTS</span></span>

### <span data-ttu-id="02db3-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="02db3-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="02db3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="02db3-138">System.String</span></span>

## <span data-ttu-id="02db3-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02db3-139">OUTPUTS</span></span>

### <span data-ttu-id="02db3-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="02db3-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="02db3-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="02db3-141">NOTES</span></span>

## <span data-ttu-id="02db3-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02db3-142">RELATED LINKS</span></span>

[<span data-ttu-id="02db3-143">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="02db3-143">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="02db3-144">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="02db3-144">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="02db3-145">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="02db3-145">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)





[<span data-ttu-id="02db3-146">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="02db3-146">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="02db3-147">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="02db3-147">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
