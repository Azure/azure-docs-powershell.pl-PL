---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 4c1205599f048e33534f0ce0aa844da7b428b076
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011930"
---
# <span data-ttu-id="428c4-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="428c4-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="428c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="428c4-102">SYNOPSIS</span></span>
<span data-ttu-id="428c4-103">Dodaje konfigurację komunikacji równorzędnej do obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="428c4-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="428c4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="428c4-104">SYNTAX</span></span>

### <span data-ttu-id="428c4-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="428c4-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="428c4-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="428c4-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="428c4-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="428c4-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="428c4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="428c4-108">DESCRIPTION</span></span>
<span data-ttu-id="428c4-109">Polecenie **cmdlet Add-AzExpressRouteCircuitPeeringConfig** dodaje konfigurację komunikacji równorzędnej do obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="428c4-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="428c4-110">Obwody usługi ExpressRoute łączą Twoją sieć lokalną z chmurą firmy Microsoft przy użyciu dostawcy łączności zamiast publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="428c4-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="428c4-111">Pamiętaj, że po uruchomieniu dodatku **AzExpressRouteCircuitPeeringConfig** musisz wywołać Set-AzExpressRouteCircuit cmdlet, aby aktywować konfigurację.</span><span class="sxs-lookup"><span data-stu-id="428c4-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="428c4-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="428c4-112">EXAMPLES</span></span>

### <span data-ttu-id="428c4-113">Przykład 1. Dodawanie elementu równorzędnego do istniejącego obwodu w układzie ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="428c4-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="428c4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="428c4-114">PARAMETERS</span></span>

### <span data-ttu-id="428c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="428c4-115">-DefaultProfile</span></span>
<span data-ttu-id="428c4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="428c4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="428c4-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="428c4-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="428c4-118">Zmodyfikowany obwód expressroute.</span><span class="sxs-lookup"><span data-stu-id="428c4-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="428c4-119">Jest to obiekt platformy Azure zwrócony przez polecenie cmdlet **Get-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="428c4-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="428c4-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="428c4-120">-LegacyMode</span></span>
<span data-ttu-id="428c4-121">Starszy tryb komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="428c4-121">The legacy mode of the Peering</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="428c4-122">-MicrosoftConfigAdvertconfigPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="428c4-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="428c4-123">W przypadku typu komunikacji równorzędnej microsoftPeering należy podać listę wszystkich prefiksów, które mają być ogłaszane za pośrednictwem sesji BGP.</span><span class="sxs-lookup"><span data-stu-id="428c4-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="428c4-124">Akceptowane są tylko prefiksy publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="428c4-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="428c4-125">Jeśli zamierzasz wysłać zestaw prefiksów, możesz wysłać listę rozdzieloną przecinkami.</span><span class="sxs-lookup"><span data-stu-id="428c4-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="428c4-126">Te prefiksy muszą być zarejestrowane w nazwie rejestru routingu (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="428c4-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428c4-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="428c4-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="428c4-128">W przypadku reklamowania prefiksów, które nie są zarejestrowane dla numeru AS komunikacji równorzędnej, możesz określić numer AS, pod którym są one zarejestrowane.</span><span class="sxs-lookup"><span data-stu-id="428c4-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428c4-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="428c4-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="428c4-130">Nazwa rejestru routingu (RIR/IRR), do której jest zarejestrowany numer AS i prefiksy.</span><span class="sxs-lookup"><span data-stu-id="428c4-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="428c4-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="428c4-131">-Name</span></span>
<span data-ttu-id="428c4-132">Nazwa relacji komunikacji równorzędnej, która ma zostać dodana.</span><span class="sxs-lookup"><span data-stu-id="428c4-132">The name of the peering relationship to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428c4-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="428c4-133">-PeerAddressType</span></span>
<span data-ttu-id="428c4-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="428c4-134">PeerAddressType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="428c4-135">- PeerASN</span><span class="sxs-lookup"><span data-stu-id="428c4-135">-PeerASN</span></span>
<span data-ttu-id="428c4-136">Numer AS obwodu expressroute.</span><span class="sxs-lookup"><span data-stu-id="428c4-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="428c4-137">Jeśli typ komunikacji równorzędnej to AzurePublicPeering, musi to być publiczna asn.</span><span class="sxs-lookup"><span data-stu-id="428c4-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428c4-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="428c4-138">-PeeringType</span></span>
<span data-ttu-id="428c4-139">Dopuszczalne wartości dla tego parametru to: `AzurePrivatePeering` `AzurePublicPeering` , i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="428c4-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428c4-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="428c4-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="428c4-141">Jest to zakres adresów IP dla podstawowej ścieżki routingu tej relacji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="428c4-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="428c4-142">Musi to być podsieci CIDR o proc. /30.</span><span class="sxs-lookup"><span data-stu-id="428c4-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="428c4-143">Pierwszy adres nieparzystych w tej podsieci powinien zostać przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="428c4-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="428c4-144">Platforma Azure skonfiguruje następny adres o numerze nawet do interfejsu routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="428c4-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428c4-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="428c4-145">-RouteFilter</span></span>
<span data-ttu-id="428c4-146">Jest to istniejący obiekt RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="428c4-146">This is an existing RouteFilter object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="428c4-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="428c4-147">-RouteFilterId</span></span>
<span data-ttu-id="428c4-148">Jest to identyfikator zasobu istniejącego obiektu RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="428c4-148">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="428c4-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="428c4-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="428c4-150">Jest to zakres adresów IP dla pomocniczej ścieżki routingu tej relacji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="428c4-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="428c4-151">Musi to być podsieci CIDR o proc. /30.</span><span class="sxs-lookup"><span data-stu-id="428c4-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="428c4-152">Pierwszy adres nieparzystych w tej podsieci powinien zostać przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="428c4-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="428c4-153">Platforma Azure skonfiguruje następny adres o numerze nawet do interfejsu routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="428c4-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428c4-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="428c4-154">-SharedKey</span></span>
<span data-ttu-id="428c4-155">Jest to opcjonalny skrót MD5 używany jako klucz wstępnie udostępniony dla konfiguracji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="428c4-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="428c4-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="428c4-156">-VlanId</span></span>
<span data-ttu-id="428c4-157">Jest to numer identyfikacyjny sieci VLAN przypisanej do tej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="428c4-157">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428c4-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="428c4-158">CommonParameters</span></span>
<span data-ttu-id="428c4-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="428c4-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="428c4-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="428c4-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="428c4-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="428c4-161">INPUTS</span></span>

### <span data-ttu-id="428c4-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="428c4-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="428c4-163">System.String</span><span class="sxs-lookup"><span data-stu-id="428c4-163">System.String</span></span>

### <span data-ttu-id="428c4-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="428c4-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="428c4-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="428c4-165">System.Boolean</span></span>

## <span data-ttu-id="428c4-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="428c4-166">OUTPUTS</span></span>

### <span data-ttu-id="428c4-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="428c4-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="428c4-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="428c4-168">NOTES</span></span>

## <span data-ttu-id="428c4-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="428c4-169">RELATED LINKS</span></span>

[<span data-ttu-id="428c4-170">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="428c4-170">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="428c4-171">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="428c4-171">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="428c4-172">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="428c4-172">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="428c4-173">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="428c4-173">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
