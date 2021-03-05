---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 23dc75532c7b23c584d586b486e0d67d32af795f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992587"
---
# <span data-ttu-id="e239c-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e239c-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="e239c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e239c-102">SYNOPSIS</span></span>
<span data-ttu-id="e239c-103">Tworzy nową konfigurację komunikacji równorzędnej, która ma zostać dodana do obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e239c-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="e239c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e239c-104">SYNTAX</span></span>

### <span data-ttu-id="e239c-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e239c-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e239c-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="e239c-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e239c-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="e239c-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e239c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e239c-108">DESCRIPTION</span></span>
<span data-ttu-id="e239c-109">Polecenie **cmdlet New-AzExpressRouteCircuitPeeringConfig** dodaje konfigurację komunikacji równorzędnej do obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e239c-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="e239c-110">Obwody usługi ExpressRoute łączą Twoją sieć lokalną z chmurą firmy Microsoft przy użyciu dostawcy łączności zamiast publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="e239c-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="e239c-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e239c-111">EXAMPLES</span></span>

### <span data-ttu-id="e239c-112">Przykład 1. Tworzenie nowego obwodu usługi ExpressRoute z konfiguracją komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="e239c-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```powershell
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
$PeerConfig = New-AzExpressRouteCircuitPeeringConfig @parameters

$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    Peering=$PeerConfig
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="e239c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e239c-113">PARAMETERS</span></span>

### <span data-ttu-id="e239c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e239c-114">-DefaultProfile</span></span>
<span data-ttu-id="e239c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e239c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e239c-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="e239c-116">-LegacyMode</span></span>
<span data-ttu-id="e239c-117">Starszy tryb komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="e239c-117">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="e239c-118">-MicrosoftConfigAdvertconfigPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="e239c-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="e239c-119">W przypadku typu komunikacji równorzędnej microsoftPeering należy podać listę wszystkich prefiksów, które mają być ogłaszane za pośrednictwem sesji BGP.</span><span class="sxs-lookup"><span data-stu-id="e239c-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="e239c-120">Akceptowane są tylko prefiksy publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="e239c-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="e239c-121">Jeśli zamierzasz wysłać zestaw prefiksów, możesz wysłać listę rozdzieloną przecinkami.</span><span class="sxs-lookup"><span data-stu-id="e239c-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="e239c-122">Te prefiksy muszą być zarejestrowane w nazwie rejestru routingu (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="e239c-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="e239c-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="e239c-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="e239c-124">W przypadku reklamowania prefiksów, które nie są zarejestrowane dla numeru AS komunikacji równorzędnej, możesz określić numer AS, pod którym są one zarejestrowane.</span><span class="sxs-lookup"><span data-stu-id="e239c-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="e239c-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="e239c-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="e239c-126">Nazwa rejestru routingu (RIR/IRR), do której jest zarejestrowany numer AS i prefiksy.</span><span class="sxs-lookup"><span data-stu-id="e239c-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="e239c-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e239c-127">-Name</span></span>
<span data-ttu-id="e239c-128">Nazwa konfiguracji komunikacji równorzędnej, która ma zostać utworzona.</span><span class="sxs-lookup"><span data-stu-id="e239c-128">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="e239c-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="e239c-129">-PeerAddressType</span></span>
<span data-ttu-id="e239c-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="e239c-130">PeerAddressType</span></span>

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

### <span data-ttu-id="e239c-131">- PeerASN</span><span class="sxs-lookup"><span data-stu-id="e239c-131">-PeerASN</span></span>
<span data-ttu-id="e239c-132">Numer AS obwodu expressroute.</span><span class="sxs-lookup"><span data-stu-id="e239c-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="e239c-133">Jeśli typ komunikacji równorzędnej to AzurePublicPeering, musi to być publiczna asn.</span><span class="sxs-lookup"><span data-stu-id="e239c-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="e239c-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="e239c-134">-PeeringType</span></span>
<span data-ttu-id="e239c-135">Dopuszczalne wartości dla tego parametru to: `AzurePrivatePeering` `AzurePublicPeering` , i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="e239c-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="e239c-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e239c-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="e239c-137">Jest to zakres adresów IP dla podstawowej ścieżki routingu tej relacji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="e239c-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="e239c-138">Musi to być podsieci CIDR o proc. /30.</span><span class="sxs-lookup"><span data-stu-id="e239c-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="e239c-139">Pierwszy adres nieparzystych w tej podsieci powinien zostać przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="e239c-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="e239c-140">Platforma Azure skonfiguruje następny adres o numerze nawet do interfejsu routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e239c-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="e239c-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="e239c-141">-RouteFilter</span></span>
<span data-ttu-id="e239c-142">Jest to istniejący obiekt RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="e239c-142">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="e239c-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="e239c-143">-RouteFilterId</span></span>
<span data-ttu-id="e239c-144">Jest to identyfikator zasobu istniejącego obiektu RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="e239c-144">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="e239c-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e239c-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="e239c-146">Jest to zakres adresów IP dla pomocniczej ścieżki routingu tej relacji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="e239c-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="e239c-147">Musi to być podsieci CIDR o proc. /30.</span><span class="sxs-lookup"><span data-stu-id="e239c-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="e239c-148">Pierwszy adres nieparzystych w tej podsieci powinien zostać przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="e239c-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="e239c-149">Platforma Azure skonfiguruje następny adres o numerze nawet do interfejsu routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e239c-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="e239c-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="e239c-150">-SharedKey</span></span>
<span data-ttu-id="e239c-151">Jest to opcjonalny skrót MD5 używany jako klucz wstępnie udostępniony dla konfiguracji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="e239c-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="e239c-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="e239c-152">-VlanId</span></span>
<span data-ttu-id="e239c-153">Jest to numer identyfikacyjny sieci VLAN przypisanej do tej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="e239c-153">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="e239c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e239c-154">CommonParameters</span></span>
<span data-ttu-id="e239c-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e239c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e239c-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e239c-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e239c-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e239c-157">INPUTS</span></span>

### <span data-ttu-id="e239c-158">System.String</span><span class="sxs-lookup"><span data-stu-id="e239c-158">System.String</span></span>

### <span data-ttu-id="e239c-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e239c-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="e239c-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e239c-160">System.Boolean</span></span>

## <span data-ttu-id="e239c-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e239c-161">OUTPUTS</span></span>

### <span data-ttu-id="e239c-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="e239c-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="e239c-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e239c-163">NOTES</span></span>

## <span data-ttu-id="e239c-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e239c-164">RELATED LINKS</span></span>

[<span data-ttu-id="e239c-165">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e239c-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e239c-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e239c-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="e239c-167">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e239c-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e239c-168">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e239c-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
