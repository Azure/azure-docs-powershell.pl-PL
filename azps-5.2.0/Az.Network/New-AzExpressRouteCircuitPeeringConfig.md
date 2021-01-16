---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 6561faf00104bf0892747ac97c09b5d8fc2c6f2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354853"
---
# <span data-ttu-id="43c8d-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="43c8d-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="43c8d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="43c8d-103">Tworzy nową konfigurację elementu równorzędnego do dodania do obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="43c8d-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="43c8d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43c8d-104">SYNTAX</span></span>

### <span data-ttu-id="43c8d-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="43c8d-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43c8d-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="43c8d-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43c8d-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="43c8d-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43c8d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="43c8d-108">DESCRIPTION</span></span>
<span data-ttu-id="43c8d-109">Polecenie cmdlet **New-AzExpressRouteCircuitPeeringConfig** umożliwia dodanie konfiguracji komunikacji równorzędnej do obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="43c8d-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="43c8d-110">Obwody ExpressRoute łączą sieć lokalną z chmurą firmy Microsoft, korzystając z dostawcy usług łączności zamiast z publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="43c8d-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="43c8d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43c8d-111">EXAMPLES</span></span>

### <span data-ttu-id="43c8d-112">Przykład 1. Tworzenie nowego obwodu ExpressRoute z konfiguracją komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="43c8d-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
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

## <span data-ttu-id="43c8d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43c8d-113">PARAMETERS</span></span>

### <span data-ttu-id="43c8d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c8d-114">-DefaultProfile</span></span>
<span data-ttu-id="43c8d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43c8d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43c8d-116">-Legacymode</span><span class="sxs-lookup"><span data-stu-id="43c8d-116">-LegacyMode</span></span>
<span data-ttu-id="43c8d-117">Starszy tryb komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="43c8d-117">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="43c8d-118">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="43c8d-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="43c8d-119">W przypadku PeeringType MicrosoftPeering musisz podać listę wszystkich prefiksów, które mają być anonsowane przez sesję BGP.</span><span class="sxs-lookup"><span data-stu-id="43c8d-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="43c8d-120">Akceptowane są tylko publiczne prefiksy adresów IP.</span><span class="sxs-lookup"><span data-stu-id="43c8d-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="43c8d-121">Możesz wysłać listę rozdzielonych przecinkami, jeśli planujesz wysłać zestaw prefiksów.</span><span class="sxs-lookup"><span data-stu-id="43c8d-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="43c8d-122">Te prefiksy muszą być zarejestrowane w nazwie rejestru routingu (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="43c8d-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="43c8d-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="43c8d-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="43c8d-124">Jeśli masz prefiksy reklamowe, które nie są zarejestrowane w przypadku komunikacji równorzędnej jako liczba, możesz określić numer AS, na który są zarejestrowani.</span><span class="sxs-lookup"><span data-stu-id="43c8d-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="43c8d-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="43c8d-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="43c8d-126">Nazwa rejestru routingu (RIR/IRR), do której jest rejestrowany numer AS i prefiksy.</span><span class="sxs-lookup"><span data-stu-id="43c8d-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="43c8d-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="43c8d-127">-Name</span></span>
<span data-ttu-id="43c8d-128">Nazwa konfiguracji elementu równorzędnego do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="43c8d-128">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="43c8d-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="43c8d-129">-PeerAddressType</span></span>
<span data-ttu-id="43c8d-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="43c8d-130">PeerAddressType</span></span>

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

### <span data-ttu-id="43c8d-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="43c8d-131">-PeerASN</span></span>
<span data-ttu-id="43c8d-132">Numer AS obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="43c8d-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="43c8d-133">To musi być publiczna WPW, gdy PeeringType jest AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="43c8d-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="43c8d-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="43c8d-134">-PeeringType</span></span>
<span data-ttu-id="43c8d-135">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="43c8d-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="43c8d-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="43c8d-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="43c8d-137">Jest to zakres adresów IP dla podstawowej ścieżki routingu tej relacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="43c8d-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="43c8d-138">To musi być podsieć CIDR/30.</span><span class="sxs-lookup"><span data-stu-id="43c8d-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="43c8d-139">Pierwszy adres o numerze nieparzystym w tej podsieci powinien być przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="43c8d-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="43c8d-140">Na platformie Azure zostanie skonfigurowane kolejne adresy o numerze parzystym w interfejsie routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43c8d-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="43c8d-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="43c8d-141">-RouteFilter</span></span>
<span data-ttu-id="43c8d-142">To jest istniejący obiekt RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="43c8d-142">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="43c8d-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="43c8d-143">-RouteFilterId</span></span>
<span data-ttu-id="43c8d-144">Jest to identyfikator zasobu istniejącego obiektu RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="43c8d-144">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="43c8d-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="43c8d-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="43c8d-146">Jest to zakres adresów IP pomocniczej ścieżki routingu tej relacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="43c8d-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="43c8d-147">To musi być podsieć CIDR/30.</span><span class="sxs-lookup"><span data-stu-id="43c8d-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="43c8d-148">Pierwszy adres o numerze nieparzystym w tej podsieci powinien być przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="43c8d-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="43c8d-149">Na platformie Azure zostanie skonfigurowane kolejne adresy o numerze parzystym w interfejsie routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43c8d-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="43c8d-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="43c8d-150">-SharedKey</span></span>
<span data-ttu-id="43c8d-151">Jest to opcjonalna wartość skrótu MD5 używana jako klucz wstępny dla konfiguracji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="43c8d-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="43c8d-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="43c8d-152">-VlanId</span></span>
<span data-ttu-id="43c8d-153">Jest to numer identyfikacyjny sieci VLAN przypisanej do tej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="43c8d-153">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="43c8d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c8d-154">CommonParameters</span></span>
<span data-ttu-id="43c8d-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43c8d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c8d-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43c8d-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c8d-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43c8d-157">INPUTS</span></span>

### <span data-ttu-id="43c8d-158">System. String</span><span class="sxs-lookup"><span data-stu-id="43c8d-158">System.String</span></span>

### <span data-ttu-id="43c8d-159">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="43c8d-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="43c8d-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43c8d-160">System.Boolean</span></span>

## <span data-ttu-id="43c8d-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43c8d-161">OUTPUTS</span></span>

### <span data-ttu-id="43c8d-162">Microsoft. Azure. Commands. Network. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="43c8d-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="43c8d-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43c8d-163">NOTES</span></span>

## <span data-ttu-id="43c8d-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43c8d-164">RELATED LINKS</span></span>

[<span data-ttu-id="43c8d-165">Dodaj-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="43c8d-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="43c8d-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="43c8d-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="43c8d-167">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="43c8d-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="43c8d-168">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="43c8d-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
