---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 4d329b0521e5b0f4974c25382be53ff32267e51c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203215"
---
# <span data-ttu-id="4628a-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4628a-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="4628a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4628a-102">SYNOPSIS</span></span>
<span data-ttu-id="4628a-103">Dodaje konfigurację komunikacji równorzędnej do obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4628a-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="4628a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4628a-104">SYNTAX</span></span>

### <span data-ttu-id="4628a-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="4628a-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4628a-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="4628a-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4628a-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="4628a-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4628a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4628a-108">DESCRIPTION</span></span>
<span data-ttu-id="4628a-109">Polecenie **cmdlet Add-AzExpressRouteCircuitPeeringConfig** dodaje konfigurację komunikacji równorzędnej do obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4628a-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="4628a-110">Obwody usługi ExpressRoute łączą Twoją sieć lokalną z chmurą firmy Microsoft przy użyciu dostawcy łączności zamiast publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="4628a-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="4628a-111">Pamiętaj, że po uruchomieniu dodatku **AzExpressRouteCircuitPeeringConfig** musisz wywołać Set-AzExpressRouteCircuit cmdlet, aby aktywować konfigurację.</span><span class="sxs-lookup"><span data-stu-id="4628a-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="4628a-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4628a-112">EXAMPLES</span></span>

### <span data-ttu-id="4628a-113">Przykład 1. Dodawanie elementu równorzędnego do istniejącego obwodu expressRoute</span><span class="sxs-lookup"><span data-stu-id="4628a-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
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

## <span data-ttu-id="4628a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4628a-114">PARAMETERS</span></span>

### <span data-ttu-id="4628a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4628a-115">-DefaultProfile</span></span>
<span data-ttu-id="4628a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4628a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4628a-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4628a-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4628a-118">Modyfikowany obwód w układzie ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4628a-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="4628a-119">Jest to obiekt platformy Azure zwrócony przez polecenie cmdlet **Get-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="4628a-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="4628a-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="4628a-120">-LegacyMode</span></span>
<span data-ttu-id="4628a-121">Starszy tryb komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="4628a-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="4628a-122">-MicrosoftConfigAdvertconfigPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="4628a-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="4628a-123">W przypadku typu komunikacji równorzędnej microsoftPeering należy podać listę wszystkich prefiksów, które mają być ogłaszane za pośrednictwem sesji BGP.</span><span class="sxs-lookup"><span data-stu-id="4628a-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="4628a-124">Akceptowane są tylko prefiksy publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="4628a-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="4628a-125">Jeśli zamierzasz wysłać zestaw prefiksów, możesz wysłać listę rozdzieloną przecinkami.</span><span class="sxs-lookup"><span data-stu-id="4628a-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="4628a-126">Te prefiksy muszą być zarejestrowane w nazwie rejestru routingu (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="4628a-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="4628a-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="4628a-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="4628a-128">W przypadku reklamowania prefiksów, które nie są zarejestrowane dla numeru AS komunikacji równorzędnej, możesz określić numer AS, pod którym są one zarejestrowane.</span><span class="sxs-lookup"><span data-stu-id="4628a-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="4628a-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="4628a-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="4628a-130">Nazwa rejestru routingu (RIR/IRR), do której jest zarejestrowany numer AS i prefiksy.</span><span class="sxs-lookup"><span data-stu-id="4628a-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="4628a-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4628a-131">-Name</span></span>
<span data-ttu-id="4628a-132">Nazwa relacji komunikacji równorzędnej, która ma zostać dodana.</span><span class="sxs-lookup"><span data-stu-id="4628a-132">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="4628a-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="4628a-133">-PeerAddressType</span></span>
<span data-ttu-id="4628a-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="4628a-134">PeerAddressType</span></span>

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

### <span data-ttu-id="4628a-135">- PeerASN</span><span class="sxs-lookup"><span data-stu-id="4628a-135">-PeerASN</span></span>
<span data-ttu-id="4628a-136">Numer AS obwodu expressRoute.</span><span class="sxs-lookup"><span data-stu-id="4628a-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="4628a-137">Jeśli typ komunikacji równorzędnej to AzurePublicPeering, musi to być publiczna asn.</span><span class="sxs-lookup"><span data-stu-id="4628a-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="4628a-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="4628a-138">-PeeringType</span></span>
<span data-ttu-id="4628a-139">Dopuszczalne wartości dla tego parametru to: `AzurePrivatePeering` `AzurePublicPeering` , i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="4628a-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="4628a-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4628a-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="4628a-141">Jest to zakres adresów IP dla podstawowej ścieżki routingu tej relacji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="4628a-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="4628a-142">Musi to być podsieci CIDR o proc. /30.</span><span class="sxs-lookup"><span data-stu-id="4628a-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="4628a-143">Pierwszy adres nieparzystych w tej podsieci powinien zostać przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="4628a-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="4628a-144">Platforma Azure skonfiguruje następny adres o numerze nawet do interfejsu routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4628a-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="4628a-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4628a-145">-RouteFilter</span></span>
<span data-ttu-id="4628a-146">Jest to istniejący obiekt RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="4628a-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="4628a-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="4628a-147">-RouteFilterId</span></span>
<span data-ttu-id="4628a-148">Jest to identyfikator zasobu istniejącego obiektu RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="4628a-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="4628a-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4628a-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="4628a-150">Jest to zakres adresów IP dla pomocniczej ścieżki routingu tej relacji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="4628a-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="4628a-151">Musi to być podsieci CIDR o proc. /30.</span><span class="sxs-lookup"><span data-stu-id="4628a-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="4628a-152">Pierwszy adres nieparzystych w tej podsieci powinien być przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="4628a-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="4628a-153">Platforma Azure skonfiguruje następny adres o numerze nawet do interfejsu routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4628a-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="4628a-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="4628a-154">-SharedKey</span></span>
<span data-ttu-id="4628a-155">Jest to opcjonalny skrót MD5 używany jako klucz wstępnie udostępniony dla konfiguracji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="4628a-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="4628a-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="4628a-156">-VlanId</span></span>
<span data-ttu-id="4628a-157">Jest to numer identyfikacyjny sieci VLAN przypisanej do tej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="4628a-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="4628a-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4628a-158">CommonParameters</span></span>
<span data-ttu-id="4628a-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4628a-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4628a-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4628a-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4628a-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4628a-161">INPUTS</span></span>

### <span data-ttu-id="4628a-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4628a-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="4628a-163">System.String</span><span class="sxs-lookup"><span data-stu-id="4628a-163">System.String</span></span>

### <span data-ttu-id="4628a-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4628a-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="4628a-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4628a-165">System.Boolean</span></span>

## <span data-ttu-id="4628a-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4628a-166">OUTPUTS</span></span>

### <span data-ttu-id="4628a-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4628a-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4628a-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4628a-168">NOTES</span></span>

## <span data-ttu-id="4628a-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4628a-169">RELATED LINKS</span></span>

[<span data-ttu-id="4628a-170">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4628a-170">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="4628a-171">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4628a-171">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4628a-172">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4628a-172">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4628a-173">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4628a-173">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
