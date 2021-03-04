---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 42a2ec1c3fb19647cc956c6b7321f52e6ad6e63e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952042"
---
# <span data-ttu-id="42262-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="42262-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="42262-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42262-102">SYNOPSIS</span></span>
<span data-ttu-id="42262-103">Umożliwia zapisanie zmodyfikowanej konfiguracji komunikacji równorzędnej usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="42262-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="42262-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="42262-104">SYNTAX</span></span>

### <span data-ttu-id="42262-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="42262-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42262-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="42262-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42262-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="42262-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42262-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="42262-108">DESCRIPTION</span></span>
<span data-ttu-id="42262-109">Polecenia cmdlet **Set-AzExpressRouteCircuitPeeringConfig** zapisują zmodyfikowaną konfigurację komunikacji równorzędnej usługi ExpressRoute z powrotem na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="42262-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="42262-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="42262-110">EXAMPLES</span></span>

### <span data-ttu-id="42262-111">Przykład 1. Zmienianie istniejącej konfiguracji komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="42262-111">Example 1: Change an existing peering configuration</span></span>
```powershell
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

### <span data-ttu-id="42262-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="42262-112">Example 2</span></span>

<span data-ttu-id="42262-113">Umożliwia zapisanie zmodyfikowanej konfiguracji komunikacji równorzędnej usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="42262-113">Saves a modified ExpressRoute peering configuration.</span></span> <span data-ttu-id="42262-114">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="42262-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzExpressRouteCircuitPeeringConfig -ExpressRouteCircuit <PSExpressRouteCircuit> -Name 'cert01' -PeerASN 100 -PeerAddressType IPv4 -PeeringType AzurePrivatePeering -PrimaryPeerAddressPrefix '123.0.0.0/30' -SecondaryPeerAddressPrefix '123.0.0.4/30' -VlanId 300
```

## <span data-ttu-id="42262-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42262-115">PARAMETERS</span></span>

### <span data-ttu-id="42262-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42262-116">-DefaultProfile</span></span>
<span data-ttu-id="42262-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="42262-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42262-118">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="42262-118">-ExpressRouteCircuit</span></span>
<span data-ttu-id="42262-119">Obiekt obwodu usługi ExpressRoute zawierający konfigurację komunikacji równorzędnej do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="42262-119">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="42262-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="42262-120">-LegacyMode</span></span>
<span data-ttu-id="42262-121">Starszy tryb komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="42262-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="42262-122">-MicrosoftConfigAdvertconfigPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="42262-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="42262-123">W przypadku typu komunikacji równorzędnej microsoftPeering należy podać listę wszystkich prefiksów, które mają być ogłaszane za pośrednictwem sesji BGP.</span><span class="sxs-lookup"><span data-stu-id="42262-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="42262-124">Akceptowane są tylko prefiksy publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="42262-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="42262-125">Jeśli zamierzasz wysłać zestaw prefiksów, możesz wysłać listę rozdzieloną przecinkami.</span><span class="sxs-lookup"><span data-stu-id="42262-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="42262-126">Te prefiksy muszą być zarejestrowane w nazwie rejestru routingu (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="42262-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="42262-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="42262-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="42262-128">W przypadku reklamowania prefiksów, które nie są zarejestrowane dla numeru AS komunikacji równorzędnej, możesz określić numer AS, pod którym są one zarejestrowane.</span><span class="sxs-lookup"><span data-stu-id="42262-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="42262-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="42262-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="42262-130">Nazwa rejestru routingu (RIR/IRR), do której jest zarejestrowany numer AS i prefiksy.</span><span class="sxs-lookup"><span data-stu-id="42262-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="42262-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="42262-131">-Name</span></span>
<span data-ttu-id="42262-132">Nazwa konfiguracji komunikacji równorzędnej do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="42262-132">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="42262-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="42262-133">-PeerAddressType</span></span>
<span data-ttu-id="42262-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="42262-134">PeerAddressType</span></span>

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

### <span data-ttu-id="42262-135">- PeerASN</span><span class="sxs-lookup"><span data-stu-id="42262-135">-PeerASN</span></span>
<span data-ttu-id="42262-136">Numer AS obwodu expressroute.</span><span class="sxs-lookup"><span data-stu-id="42262-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="42262-137">Jeśli typ komunikacji równorzędnej to AzurePublicPeering, musi to być publiczna asn.</span><span class="sxs-lookup"><span data-stu-id="42262-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="42262-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="42262-138">-PeeringType</span></span>
<span data-ttu-id="42262-139">Dopuszczalne wartości dla tego parametru to: `AzurePrivatePeering` `AzurePublicPeering` , i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="42262-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="42262-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="42262-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="42262-141">Jest to zakres adresów IP dla podstawowej ścieżki routingu tej relacji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="42262-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="42262-142">Musi to być podsieci CIDR o proc. /30.</span><span class="sxs-lookup"><span data-stu-id="42262-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="42262-143">Pierwszy adres nieparzystych w tej podsieci powinien zostać przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="42262-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="42262-144">Platforma Azure skonfiguruje następny adres o numerze nawet do interfejsu routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="42262-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="42262-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="42262-145">-RouteFilter</span></span>
<span data-ttu-id="42262-146">Jest to istniejący obiekt RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="42262-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="42262-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="42262-147">-RouteFilterId</span></span>
<span data-ttu-id="42262-148">Jest to identyfikator zasobu istniejącego obiektu RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="42262-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="42262-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="42262-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="42262-150">Jest to zakres adresów IP dla pomocniczej ścieżki routingu tej relacji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="42262-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="42262-151">Musi to być podsieci CIDR o proc. /30.</span><span class="sxs-lookup"><span data-stu-id="42262-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="42262-152">Pierwszy adres nieparzystych w tej podsieci powinien zostać przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="42262-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="42262-153">Platforma Azure skonfiguruje następny adres o numerze nawet do interfejsu routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="42262-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="42262-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="42262-154">-SharedKey</span></span>
<span data-ttu-id="42262-155">Jest to opcjonalny skrót MD5 używany jako klucz wstępnie udostępniony dla konfiguracji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="42262-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="42262-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="42262-156">-VlanId</span></span>
<span data-ttu-id="42262-157">Jest to numer identyfikacyjny sieci VLAN przypisanej do tej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="42262-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="42262-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42262-158">CommonParameters</span></span>
<span data-ttu-id="42262-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42262-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42262-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42262-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42262-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42262-161">INPUTS</span></span>

### <span data-ttu-id="42262-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="42262-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="42262-163">System.String</span><span class="sxs-lookup"><span data-stu-id="42262-163">System.String</span></span>

### <span data-ttu-id="42262-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="42262-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="42262-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="42262-165">System.Boolean</span></span>

## <span data-ttu-id="42262-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42262-166">OUTPUTS</span></span>

### <span data-ttu-id="42262-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="42262-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="42262-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="42262-168">NOTES</span></span>

## <span data-ttu-id="42262-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42262-169">RELATED LINKS</span></span>

[<span data-ttu-id="42262-170">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="42262-170">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="42262-171">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="42262-171">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="42262-172">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="42262-172">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="42262-173">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="42262-173">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
