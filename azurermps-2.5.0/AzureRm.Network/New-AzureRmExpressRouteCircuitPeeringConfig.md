---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
ms.openlocfilehash: 9b07574a1d8895d8504660784bf3bafe4ed891bd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898290"
---
# <span data-ttu-id="370ff-101">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="370ff-101">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="370ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="370ff-102">SYNOPSIS</span></span>
<span data-ttu-id="370ff-103">Tworzy nową konfigurację elementu równorzędnego do dodania do obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="370ff-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="370ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="370ff-104">SYNTAX</span></span>

### <span data-ttu-id="370ff-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="370ff-105">SetByResource (Default)</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="370ff-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="370ff-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="370ff-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="370ff-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="370ff-108">Opis</span><span class="sxs-lookup"><span data-stu-id="370ff-108">DESCRIPTION</span></span>
<span data-ttu-id="370ff-109">Polecenie cmdlet **New-AzureRmExpressRouteCircuitPeeringConfig** umożliwia dodanie konfiguracji komunikacji równorzędnej do obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="370ff-109">The **New-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="370ff-110">Obwody ExpressRoute łączą sieć lokalną z chmurą firmy Microsoft, korzystając z dostawcy usług łączności zamiast z publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="370ff-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="370ff-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="370ff-111">EXAMPLES</span></span>

### <span data-ttu-id="370ff-112">Przykład 1. Tworzenie nowego obwodu ExpressRoute z konfiguracją komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="370ff-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
$PeerConfig = New-AzureRmExpressRouteCircuitPeeringConfig @parameters

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
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="370ff-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="370ff-113">PARAMETERS</span></span>

### <span data-ttu-id="370ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="370ff-114">-DefaultProfile</span></span>
<span data-ttu-id="370ff-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="370ff-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370ff-116">-Legacymode</span><span class="sxs-lookup"><span data-stu-id="370ff-116">-LegacyMode</span></span>
<span data-ttu-id="370ff-117">Starszy tryb komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="370ff-117">The legacy mode of the Peering</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="370ff-118">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="370ff-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="370ff-119">W przypadku PeeringType MicrosoftPeering musisz podać listę wszystkich prefiksów, które mają być anonsowane przez sesję BGP.</span><span class="sxs-lookup"><span data-stu-id="370ff-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="370ff-120">Akceptowane są tylko publiczne prefiksy adresów IP.</span><span class="sxs-lookup"><span data-stu-id="370ff-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="370ff-121">Możesz wysłać listę rozdzielonych przecinkami, jeśli planujesz wysłać zestaw prefiksów.</span><span class="sxs-lookup"><span data-stu-id="370ff-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="370ff-122">Te prefiksy muszą być zarejestrowane w nazwie rejestru routingu (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="370ff-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370ff-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="370ff-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="370ff-124">Jeśli masz prefiksy reklamowe, które nie są zarejestrowane w przypadku komunikacji równorzędnej jako liczba, możesz określić numer AS, na który są zarejestrowani.</span><span class="sxs-lookup"><span data-stu-id="370ff-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370ff-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="370ff-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="370ff-126">Nazwa rejestru routingu (RIR/IRR), do której jest rejestrowany numer AS i prefiksy.</span><span class="sxs-lookup"><span data-stu-id="370ff-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370ff-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="370ff-127">-Name</span></span>
<span data-ttu-id="370ff-128">Nazwa konfiguracji elementu równorzędnego do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="370ff-128">The name of the peering configuration to be created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370ff-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="370ff-129">-PeerAddressType</span></span>
<span data-ttu-id="370ff-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="370ff-130">PeerAddressType</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="370ff-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="370ff-131">-PeerASN</span></span>
<span data-ttu-id="370ff-132">Numer AS obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="370ff-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="370ff-133">To musi być publiczna WPW, gdy PeeringType jest AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="370ff-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370ff-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="370ff-134">-PeeringType</span></span>
<span data-ttu-id="370ff-135">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="370ff-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370ff-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="370ff-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="370ff-137">Jest to zakres adresów IP dla podstawowej ścieżki routingu tej relacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="370ff-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="370ff-138">To musi być podsieć CIDR/30.</span><span class="sxs-lookup"><span data-stu-id="370ff-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="370ff-139">Pierwszy adres o numerze nieparzystym w tej podsieci powinien być przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="370ff-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="370ff-140">Na platformie Azure zostanie skonfigurowane kolejne adresy o numerze parzystym w interfejsie routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="370ff-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370ff-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="370ff-141">-RouteFilter</span></span>
<span data-ttu-id="370ff-142">To jest istniejący obiekt RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="370ff-142">This is an existing RouteFilter object.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="370ff-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="370ff-143">-RouteFilterId</span></span>
<span data-ttu-id="370ff-144">Jest to identyfikator zasobu istniejącego obiektu RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="370ff-144">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="370ff-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="370ff-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="370ff-146">Jest to zakres adresów IP pomocniczej ścieżki routingu tej relacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="370ff-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="370ff-147">To musi być podsieć CIDR/30.</span><span class="sxs-lookup"><span data-stu-id="370ff-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="370ff-148">Pierwszy adres o numerze nieparzystym w tej podsieci powinien być przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="370ff-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="370ff-149">Na platformie Azure zostanie skonfigurowane kolejne adresy o numerze parzystym w interfejsie routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="370ff-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370ff-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="370ff-150">-SharedKey</span></span>
<span data-ttu-id="370ff-151">Jest to opcjonalna wartość skrótu MD5 używana jako klucz wstępny dla konfiguracji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="370ff-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370ff-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="370ff-152">-VlanId</span></span>
<span data-ttu-id="370ff-153">Jest to numer identyfikacyjny sieci VLAN przypisanej do tej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="370ff-153">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370ff-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="370ff-154">CommonParameters</span></span>
<span data-ttu-id="370ff-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="370ff-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="370ff-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="370ff-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="370ff-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="370ff-157">INPUTS</span></span>

## <span data-ttu-id="370ff-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="370ff-158">OUTPUTS</span></span>

### <span data-ttu-id="370ff-159">Microsoft. Azure. Commands. Network. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="370ff-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="370ff-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="370ff-160">NOTES</span></span>

## <span data-ttu-id="370ff-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="370ff-161">RELATED LINKS</span></span>

[<span data-ttu-id="370ff-162">Dodaj-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="370ff-162">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="370ff-163">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="370ff-163">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="370ff-164">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="370ff-164">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="370ff-165">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="370ff-165">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
