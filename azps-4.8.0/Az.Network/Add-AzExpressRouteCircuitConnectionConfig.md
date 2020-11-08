---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: e8691d31956e1ee59f692cc3d37fa1e2d5598efa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223868"
---
# <span data-ttu-id="1f564-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1f564-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="1f564-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f564-102">SYNOPSIS</span></span>
<span data-ttu-id="1f564-103">Umożliwia dodanie konfiguracji połączenia obwodowego do prywatnych elementów równorzędnych obwodu usługi Express Route.</span><span class="sxs-lookup"><span data-stu-id="1f564-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="1f564-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f564-104">SYNTAX</span></span>

### <span data-ttu-id="1f564-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1f564-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f564-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1f564-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f564-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1f564-107">DESCRIPTION</span></span>
<span data-ttu-id="1f564-108">Polecenie cmdlet **Add-AzExpressRouteCircuitConnectionConfig** umożliwia dodanie konfiguracji połączenia obwodowego do prywatnych elementów równorzędnych dla obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1f564-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="1f564-109">Umożliwia to komunikację równorzędną z dwiema drogami obwodowymi w różnych regionach lub abonamentach. Uwaga: po uruchomieniu polecenia **Add-AzExpressRouteCircuitConnectionConfig** musisz zadzwonić do apletu polecenia cmdlet Set-AzExpressRouteCircuit, aby aktywować konfigurację.</span><span class="sxs-lookup"><span data-stu-id="1f564-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitConnectionConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="1f564-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f564-110">EXAMPLES</span></span>

### <span data-ttu-id="1f564-111">Przykład 1: Dodawanie zasobu połączenia obwodowego do istniejącego obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="1f564-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
$addressPrefixType = 'IPv4'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="1f564-112">Przykład 2: Dodawanie konfiguracji połączenia obwodowego przy użyciu połączeń rurowych z istniejącym obwodem ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="1f564-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="1f564-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f564-113">PARAMETERS</span></span>

### <span data-ttu-id="1f564-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1f564-114">-AddressPrefix</span></span>
<span data-ttu-id="1f564-115">Obszar adresów klienta minimum/29, aby utworzyć tunele VxLan między obwodami routingu Express dla tuneli IPv4.</span><span class="sxs-lookup"><span data-stu-id="1f564-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="1f564-116">lub minimum/125 adres klienta, aby utworzyć tunele VxLan między obwodami routingu Express dla tuneli IPv6.</span><span class="sxs-lookup"><span data-stu-id="1f564-116">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="1f564-117">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="1f564-117">-AddressPrefixType</span></span>
<span data-ttu-id="1f564-118">Ta funkcja określa rodzinę adresów, do której należy prefiks adresu.</span><span class="sxs-lookup"><span data-stu-id="1f564-118">This specifies the Address Family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="1f564-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="1f564-119">-AuthorizationKey</span></span>
<span data-ttu-id="1f564-120">Klucz autoryzacji do obwodu trasy peer Express w innej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1f564-120">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="1f564-121">Autoryzacja na obwódze równorzędnym można utworzyć przy użyciu istniejących poleceń.</span><span class="sxs-lookup"><span data-stu-id="1f564-121">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="1f564-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f564-122">-DefaultProfile</span></span>
<span data-ttu-id="1f564-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f564-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f564-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1f564-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="1f564-125">Obwód ExpressRoute jest modyfikowany.</span><span class="sxs-lookup"><span data-stu-id="1f564-125">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="1f564-126">To jest obiekt Azure zwrócony przez polecenie cmdlet **Get-AzExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="1f564-126">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="1f564-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f564-127">-Name</span></span>
<span data-ttu-id="1f564-128">Nazwa zasobu połączenia obwodowego, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="1f564-128">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="1f564-129">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="1f564-129">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="1f564-130">Identyfikator zasobu dla prywatnego komunikacji równorzędnej obwodu zdalnego, który będzie równorzędny z bieżącym obwodem.</span><span class="sxs-lookup"><span data-stu-id="1f564-130">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="1f564-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f564-131">-Confirm</span></span>
<span data-ttu-id="1f564-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f564-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f564-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f564-133">-WhatIf</span></span>
<span data-ttu-id="1f564-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f564-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f564-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1f564-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f564-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f564-136">CommonParameters</span></span>
<span data-ttu-id="1f564-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f564-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f564-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f564-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f564-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f564-139">INPUTS</span></span>

### <span data-ttu-id="1f564-140">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1f564-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="1f564-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1f564-141">System.String</span></span>

## <span data-ttu-id="1f564-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f564-142">OUTPUTS</span></span>

### <span data-ttu-id="1f564-143">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1f564-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="1f564-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f564-144">NOTES</span></span>

## <span data-ttu-id="1f564-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f564-145">RELATED LINKS</span></span>

[<span data-ttu-id="1f564-146">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1f564-146">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="1f564-147">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1f564-147">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="1f564-148">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1f564-148">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="1f564-149">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1f564-149">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="1f564-150">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1f564-150">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)