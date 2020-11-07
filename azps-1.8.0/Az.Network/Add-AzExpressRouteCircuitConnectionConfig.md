---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: a3b5b20eac34076dd6a5490a5d9cf1a5e2c49684
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709686"
---
# <span data-ttu-id="085b9-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="085b9-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="085b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="085b9-102">SYNOPSIS</span></span>
<span data-ttu-id="085b9-103">Umożliwia dodanie konfiguracji połączenia obwodowego do prywatnych elementów równorzędnych obwodu usługi Express Route.</span><span class="sxs-lookup"><span data-stu-id="085b9-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="085b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="085b9-104">SYNTAX</span></span>

### <span data-ttu-id="085b9-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="085b9-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="085b9-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="085b9-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="085b9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="085b9-107">DESCRIPTION</span></span>
<span data-ttu-id="085b9-108">Polecenie cmdlet **Add-AzExpressRouteCircuitConnectionConfig** umożliwia dodanie konfiguracji połączenia obwodowego do prywatnych elementów równorzędnych dla obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="085b9-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="085b9-109">Umożliwia to komunikację równorzędną z dwiema drogami obwodowymi w różnych regionach lub abonamentach. Uwaga: po uruchomieniu polecenia **Add-AzExpressRouteCircuitPeeringConfig** musisz zadzwonić do apletu polecenia cmdlet Set-AzExpressRouteCircuit, aby aktywować konfigurację.</span><span class="sxs-lookup"><span data-stu-id="085b9-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="085b9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="085b9-110">EXAMPLES</span></span>

### <span data-ttu-id="085b9-111">Przykład 1: Dodawanie zasobu połączenia obwodowego do istniejącego obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="085b9-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="085b9-112">Przykład 2: Dodawanie konfiguracji połączenia obwodowego przy użyciu połączeń rurowych z istniejącym obwodem ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="085b9-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="085b9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="085b9-113">PARAMETERS</span></span>

### <span data-ttu-id="085b9-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="085b9-114">-AddressPrefix</span></span>
<span data-ttu-id="085b9-115">Obszar adresów klienta minimum/29, który umożliwia tworzenie tuneli VxLan między drogami obwodowymi Express</span><span class="sxs-lookup"><span data-stu-id="085b9-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="085b9-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="085b9-116">-AuthorizationKey</span></span>
<span data-ttu-id="085b9-117">Klucz autoryzacji do obwodu trasy peer Express w innej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="085b9-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="085b9-118">Autoryzacja na obwódze równorzędnym można utworzyć przy użyciu istniejących poleceń.</span><span class="sxs-lookup"><span data-stu-id="085b9-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="085b9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="085b9-119">-DefaultProfile</span></span>
<span data-ttu-id="085b9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="085b9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="085b9-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="085b9-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="085b9-122">Obwód ExpressRoute jest modyfikowany.</span><span class="sxs-lookup"><span data-stu-id="085b9-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="085b9-123">To jest obiekt Azure zwrócony przez polecenie cmdlet **Get-AzExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="085b9-123">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="085b9-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="085b9-124">-Name</span></span>
<span data-ttu-id="085b9-125">Nazwa zasobu połączenia obwodowego, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="085b9-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="085b9-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="085b9-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="085b9-127">Identyfikator zasobu dla prywatnego komunikacji równorzędnej obwodu zdalnego, który będzie równorzędny z bieżącym obwodem.</span><span class="sxs-lookup"><span data-stu-id="085b9-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="085b9-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="085b9-128">-Confirm</span></span>
<span data-ttu-id="085b9-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="085b9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="085b9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="085b9-130">-WhatIf</span></span>
<span data-ttu-id="085b9-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="085b9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="085b9-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="085b9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="085b9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="085b9-133">CommonParameters</span></span>
<span data-ttu-id="085b9-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="085b9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="085b9-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="085b9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="085b9-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="085b9-136">INPUTS</span></span>

### <span data-ttu-id="085b9-137">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="085b9-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="085b9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="085b9-138">System.String</span></span>

## <span data-ttu-id="085b9-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="085b9-139">OUTPUTS</span></span>

### <span data-ttu-id="085b9-140">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="085b9-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="085b9-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="085b9-141">NOTES</span></span>

## <span data-ttu-id="085b9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="085b9-142">RELATED LINKS</span></span>

[<span data-ttu-id="085b9-143">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="085b9-143">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="085b9-144">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="085b9-144">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="085b9-145">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="085b9-145">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="085b9-146">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="085b9-146">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="085b9-147">Nowe — AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="085b9-147">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="085b9-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="085b9-148">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="085b9-149">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="085b9-149">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)