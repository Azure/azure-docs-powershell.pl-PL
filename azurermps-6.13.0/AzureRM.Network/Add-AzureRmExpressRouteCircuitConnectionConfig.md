---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: aab4e78cd01e814ed8eb81b820e20bd3da4c03f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552727"
---
# <span data-ttu-id="7dca4-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7dca4-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="7dca4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7dca4-102">SYNOPSIS</span></span>
<span data-ttu-id="7dca4-103">Umożliwia dodanie konfiguracji połączenia obwodowego do prywatnych elementów równorzędnych obwodu usługi Express Route.</span><span class="sxs-lookup"><span data-stu-id="7dca4-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dca4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7dca4-104">SYNTAX</span></span>

### <span data-ttu-id="7dca4-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7dca4-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dca4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7dca4-106">SetByResourceId</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dca4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7dca4-107">DESCRIPTION</span></span>
<span data-ttu-id="7dca4-108">Polecenie cmdlet **Add-AzureRmExpressRouteCircuitConnectionConfig** umożliwia dodanie konfiguracji połączenia obwodowego do prywatnych elementów równorzędnych dla obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7dca4-108">The **Add-AzureRmExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="7dca4-109">Umożliwia to komunikację równorzędną z dwiema drogami obwodowymi w różnych regionach lub abonamentach. Uwaga: po uruchomieniu polecenia **Add-AzureRmExpressRouteCircuitPeeringConfig** musisz zadzwonić do apletu polecenia cmdlet Set-AzureRmExpressRouteCircuit, aby aktywować konfigurację.</span><span class="sxs-lookup"><span data-stu-id="7dca4-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="7dca4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7dca4-110">EXAMPLES</span></span>

### <span data-ttu-id="7dca4-111">Przykład 1: Dodawanie zasobu połączenia obwodowego do istniejącego obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="7dca4-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="7dca4-112">Przykład 2: Dodawanie konfiguracji połączenia obwodowego przy użyciu połączeń rurowych z istniejącym obwodem ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="7dca4-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="7dca4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7dca4-113">PARAMETERS</span></span>

### <span data-ttu-id="7dca4-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7dca4-114">-AddressPrefix</span></span>
<span data-ttu-id="7dca4-115">Obszar adresów klienta minimum/29, który umożliwia tworzenie tuneli VxLan między drogami obwodowymi Express</span><span class="sxs-lookup"><span data-stu-id="7dca4-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="7dca4-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="7dca4-116">-AuthorizationKey</span></span>
<span data-ttu-id="7dca4-117">Klucz autoryzacji do obwodu trasy peer Express w innej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7dca4-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="7dca4-118">Autoryzacja na obwódze równorzędnym można utworzyć przy użyciu istniejących poleceń.</span><span class="sxs-lookup"><span data-stu-id="7dca4-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="7dca4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dca4-119">-DefaultProfile</span></span>
<span data-ttu-id="7dca4-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7dca4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dca4-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7dca4-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="7dca4-122">Obwód ExpressRoute jest modyfikowany.</span><span class="sxs-lookup"><span data-stu-id="7dca4-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="7dca4-123">To jest obiekt Azure zwrócony przez polecenie cmdlet **Get-AzureRmExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="7dca4-123">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="7dca4-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7dca4-124">-Name</span></span>
<span data-ttu-id="7dca4-125">Nazwa zasobu połączenia obwodowego, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="7dca4-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="7dca4-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="7dca4-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="7dca4-127">Identyfikator zasobu dla prywatnego komunikacji równorzędnej obwodu zdalnego, który będzie równorzędny z bieżącym obwodem.</span><span class="sxs-lookup"><span data-stu-id="7dca4-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="7dca4-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7dca4-128">-Confirm</span></span>
<span data-ttu-id="7dca4-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dca4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dca4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dca4-130">-WhatIf</span></span>
<span data-ttu-id="7dca4-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dca4-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7dca4-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7dca4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dca4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dca4-133">CommonParameters</span></span>
<span data-ttu-id="7dca4-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dca4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dca4-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dca4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dca4-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7dca4-136">INPUTS</span></span>

### <span data-ttu-id="7dca4-137">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7dca4-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="7dca4-138">Parametry: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7dca4-138">Parameters: ExpressRouteCircuit (ByValue)</span></span>

### <span data-ttu-id="7dca4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7dca4-139">System.String</span></span>

## <span data-ttu-id="7dca4-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7dca4-140">OUTPUTS</span></span>

### <span data-ttu-id="7dca4-141">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7dca4-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7dca4-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7dca4-142">NOTES</span></span>

## <span data-ttu-id="7dca4-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7dca4-143">RELATED LINKS</span></span>

[<span data-ttu-id="7dca4-144">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7dca4-144">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="7dca4-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7dca4-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7dca4-146">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7dca4-146">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7dca4-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7dca4-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7dca4-148">Nowe — AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7dca4-148">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7dca4-149">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7dca4-149">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="7dca4-150">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7dca4-150">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)
