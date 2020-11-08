---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219392"
---
# <span data-ttu-id="7e8ca-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7e8ca-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="7e8ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e8ca-102">SYNOPSIS</span></span>
<span data-ttu-id="7e8ca-103">Umożliwia zaktualizowanie konfiguracji połączenia obwodowego utworzonego w odniesieniu do prywatnych elementów równorzędnych dla obwodu usługi Express Route.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="7e8ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e8ca-104">SYNTAX</span></span>

### <span data-ttu-id="7e8ca-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7e8ca-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e8ca-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7e8ca-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e8ca-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7e8ca-107">DESCRIPTION</span></span>
<span data-ttu-id="7e8ca-108">Polecenie cmdlet **Set-AzExpressRouteCircuitConnectionConfig** umożliwia zaktualizowanie konfiguracji połączenia obwodowego utworzonego w prywatnej komunikacji równorzędnej dla obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="7e8ca-109">Umożliwia to komunikację równorzędną z dwiema drogami obwodowymi w różnych regionach lub abonamentach.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="7e8ca-110">Pamiętaj, że przed uruchomieniem funkcji **Set-AzExpressRouteCircuitConnectionConfig** musisz dodać połączenie obwodu za pomocą polecenia **Add-AzExpressRouteCircuitConnectionConfig**.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="7e8ca-111">Ponadto po uruchomieniu polecenia **Set-AzExpressRouteCircuitPeeringConfig** musisz zadzwonić do polecenia cmdlet Set-AzExpressRouteCircuit, aby aktywować konfigurację.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="7e8ca-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e8ca-112">EXAMPLES</span></span>

### <span data-ttu-id="7e8ca-113">Przykład 1: aktualizowanie zasobu połączenia obwodowego do istniejącego obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="7e8ca-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="7e8ca-114">Przykład 2: Ustawianie konfiguracji połączenia obwodowego przy użyciu połączeń rurowych z istniejącym obwodem ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="7e8ca-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="7e8ca-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e8ca-115">PARAMETERS</span></span>

### <span data-ttu-id="7e8ca-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7e8ca-116">-AddressPrefix</span></span>
<span data-ttu-id="7e8ca-117">Obszar adresów klienta minimum/29, aby utworzyć tunele VxLan między obwodami routingu Express dla tuneli IPv4.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="7e8ca-118">lub minimum/125 adres klienta, aby utworzyć tunele VxLan między obwodami routingu Express dla tuneli IPv6.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="7e8ca-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="7e8ca-119">-AddressPrefixType</span></span>
<span data-ttu-id="7e8ca-120">Określa rodzinę adresów, do której należy prefiks adresu.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-120">Specifies the address family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="7e8ca-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="7e8ca-121">-AuthorizationKey</span></span>
<span data-ttu-id="7e8ca-122">Klucz autoryzacji do obwodu trasy peer Express w innej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="7e8ca-123">Autoryzacja na obwódze równorzędnym można utworzyć przy użyciu istniejących poleceń.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="7e8ca-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e8ca-124">-DefaultProfile</span></span>
<span data-ttu-id="7e8ca-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e8ca-126">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7e8ca-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="7e8ca-127">Obwód ExpressRoute jest modyfikowany.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="7e8ca-128">To jest obiekt Azure zwrócony przez polecenie cmdlet **Get-AzExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="7e8ca-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="7e8ca-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7e8ca-129">-Name</span></span>
<span data-ttu-id="7e8ca-130">Nazwa zasobu połączenia obwodowego, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-130">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="7e8ca-131">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="7e8ca-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="7e8ca-132">Identyfikator zasobu dla prywatnego komunikacji równorzędnej obwodu zdalnego, który będzie równorzędny z bieżącym obwodem.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="7e8ca-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e8ca-133">-Confirm</span></span>
<span data-ttu-id="7e8ca-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e8ca-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e8ca-135">-WhatIf</span></span>
<span data-ttu-id="7e8ca-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e8ca-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e8ca-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e8ca-138">CommonParameters</span></span>
<span data-ttu-id="7e8ca-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e8ca-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e8ca-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e8ca-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e8ca-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e8ca-141">INPUTS</span></span>

### <span data-ttu-id="7e8ca-142">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7e8ca-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="7e8ca-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7e8ca-143">System.String</span></span>

## <span data-ttu-id="7e8ca-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e8ca-144">OUTPUTS</span></span>

### <span data-ttu-id="7e8ca-145">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7e8ca-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7e8ca-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e8ca-146">NOTES</span></span>

## <span data-ttu-id="7e8ca-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e8ca-147">RELATED LINKS</span></span>

[<span data-ttu-id="7e8ca-148">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7e8ca-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7e8ca-149">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7e8ca-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7e8ca-150">Dodaj-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7e8ca-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7e8ca-151">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7e8ca-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="7e8ca-152">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7e8ca-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
