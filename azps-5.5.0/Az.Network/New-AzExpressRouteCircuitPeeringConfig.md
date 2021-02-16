---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 6561faf00104bf0892747ac97c09b5d8fc2c6f2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191882"
---
# <span data-ttu-id="8ec56-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8ec56-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="8ec56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ec56-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec56-103">Tworzy nową konfigurację komunikacji równorzędnej, która ma zostać dodana do obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8ec56-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="8ec56-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8ec56-104">SYNTAX</span></span>

### <span data-ttu-id="8ec56-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8ec56-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ec56-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="8ec56-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ec56-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="8ec56-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ec56-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8ec56-108">DESCRIPTION</span></span>
<span data-ttu-id="8ec56-109">Polecenie **cmdlet New-AzExpressRouteCircuitPeeringConfig** dodaje konfigurację komunikacji równorzędnej do obwodu usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8ec56-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="8ec56-110">Obwody usługi ExpressRoute łączą Twoją sieć lokalną z chmurą firmy Microsoft przy użyciu dostawcy łączności zamiast publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="8ec56-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="8ec56-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8ec56-111">EXAMPLES</span></span>

### <span data-ttu-id="8ec56-112">Przykład 1. Tworzenie nowego obwodu usługi ExpressRoute z konfiguracją komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="8ec56-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
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

## <span data-ttu-id="8ec56-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ec56-113">PARAMETERS</span></span>

### <span data-ttu-id="8ec56-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec56-114">-DefaultProfile</span></span>
<span data-ttu-id="8ec56-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ec56-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ec56-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="8ec56-116">-LegacyMode</span></span>
<span data-ttu-id="8ec56-117">Starszy tryb komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="8ec56-117">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="8ec56-118">-MicrosoftConfigAdvertconfigPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="8ec56-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="8ec56-119">W przypadku typu komunikacji równorzędnej microsoftPeering należy podać listę wszystkich prefiksów, które mają być ogłaszane za pośrednictwem sesji BGP.</span><span class="sxs-lookup"><span data-stu-id="8ec56-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="8ec56-120">Akceptowane są tylko prefiksy publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="8ec56-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="8ec56-121">Jeśli zamierzasz wysłać zestaw prefiksów, możesz wysłać listę rozdzieloną przecinkami.</span><span class="sxs-lookup"><span data-stu-id="8ec56-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="8ec56-122">Te prefiksy muszą być zarejestrowane w nazwie rejestru routingu (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="8ec56-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="8ec56-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="8ec56-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="8ec56-124">W przypadku reklamowania prefiksów, które nie są zarejestrowane dla numeru AS komunikacji równorzędnej, możesz określić numer AS, pod którym są one zarejestrowane.</span><span class="sxs-lookup"><span data-stu-id="8ec56-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="8ec56-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="8ec56-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="8ec56-126">Nazwa rejestru routingu (RIR/IRR), do której jest zarejestrowany numer AS i prefiksy.</span><span class="sxs-lookup"><span data-stu-id="8ec56-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="8ec56-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8ec56-127">-Name</span></span>
<span data-ttu-id="8ec56-128">Nazwa konfiguracji komunikacji równorzędnej, która ma zostać utworzona.</span><span class="sxs-lookup"><span data-stu-id="8ec56-128">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="8ec56-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="8ec56-129">-PeerAddressType</span></span>
<span data-ttu-id="8ec56-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="8ec56-130">PeerAddressType</span></span>

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

### <span data-ttu-id="8ec56-131">- PeerASN</span><span class="sxs-lookup"><span data-stu-id="8ec56-131">-PeerASN</span></span>
<span data-ttu-id="8ec56-132">Numer AS obwodu expressroute.</span><span class="sxs-lookup"><span data-stu-id="8ec56-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="8ec56-133">Jeśli typ komunikacji równorzędnej to AzurePublicPeering, musi to być publiczna asn.</span><span class="sxs-lookup"><span data-stu-id="8ec56-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="8ec56-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="8ec56-134">-PeeringType</span></span>
<span data-ttu-id="8ec56-135">Dopuszczalne wartości dla tego parametru to: `AzurePrivatePeering` `AzurePublicPeering` , i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="8ec56-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="8ec56-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8ec56-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="8ec56-137">Jest to zakres adresów IP dla podstawowej ścieżki routingu tej relacji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="8ec56-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="8ec56-138">Musi to być podsieci CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="8ec56-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="8ec56-139">Pierwszy adres nieparzystych w tej podsieci powinien być przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="8ec56-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="8ec56-140">Platforma Azure skonfiguruje następny adres o numerze nawet do interfejsu routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8ec56-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="8ec56-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8ec56-141">-RouteFilter</span></span>
<span data-ttu-id="8ec56-142">Jest to istniejący obiekt RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="8ec56-142">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="8ec56-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="8ec56-143">-RouteFilterId</span></span>
<span data-ttu-id="8ec56-144">Jest to identyfikator zasobu istniejącego obiektu RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="8ec56-144">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="8ec56-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8ec56-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="8ec56-146">Jest to zakres adresów IP dla pomocniczej ścieżki routingu tej relacji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="8ec56-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="8ec56-147">Musi to być podsieci CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="8ec56-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="8ec56-148">Pierwszy adres nieparzystych w tej podsieci powinien być przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="8ec56-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="8ec56-149">Platforma Azure skonfiguruje następny adres o numerze nawet do interfejsu routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8ec56-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="8ec56-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="8ec56-150">-SharedKey</span></span>
<span data-ttu-id="8ec56-151">Jest to opcjonalny skrót MD5 używany jako klucz wstępnie udostępniony dla konfiguracji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="8ec56-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="8ec56-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="8ec56-152">-VlanId</span></span>
<span data-ttu-id="8ec56-153">Jest to numer identyfikacyjny sieci VLAN przypisanej do tej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="8ec56-153">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="8ec56-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec56-154">CommonParameters</span></span>
<span data-ttu-id="8ec56-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ec56-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec56-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ec56-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec56-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ec56-157">INPUTS</span></span>

### <span data-ttu-id="8ec56-158">System.String</span><span class="sxs-lookup"><span data-stu-id="8ec56-158">System.String</span></span>

### <span data-ttu-id="8ec56-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8ec56-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="8ec56-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8ec56-160">System.Boolean</span></span>

## <span data-ttu-id="8ec56-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ec56-161">OUTPUTS</span></span>

### <span data-ttu-id="8ec56-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="8ec56-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="8ec56-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8ec56-163">NOTES</span></span>

## <span data-ttu-id="8ec56-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ec56-164">RELATED LINKS</span></span>

[<span data-ttu-id="8ec56-165">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8ec56-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="8ec56-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8ec56-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="8ec56-167">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8ec56-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="8ec56-168">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8ec56-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
