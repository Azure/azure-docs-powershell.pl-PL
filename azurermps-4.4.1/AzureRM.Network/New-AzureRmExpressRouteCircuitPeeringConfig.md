---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 7008ec07c4ed8800d5817e6dbf306a1540d89a04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717036"
---
# <span data-ttu-id="85e02-101">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="85e02-101">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="85e02-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85e02-102">SYNOPSIS</span></span>
<span data-ttu-id="85e02-103">Tworzy nową konfigurację elementu równorzędnego do dodania do obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="85e02-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85e02-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85e02-104">SYNTAX</span></span>

### <span data-ttu-id="85e02-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="85e02-105">SetByResource (Default)</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85e02-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="85e02-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85e02-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="85e02-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <Int32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85e02-108">Opis</span><span class="sxs-lookup"><span data-stu-id="85e02-108">DESCRIPTION</span></span>
<span data-ttu-id="85e02-109">Polecenie cmdlet **New-AzureRmExpressRouteCircuitPeeringConfig** umożliwia dodanie konfiguracji komunikacji równorzędnej do obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="85e02-109">The **New-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="85e02-110">Obwody ExpressRoute łączą sieć lokalną z chmurą firmy Microsoft, korzystając z dostawcy usług łączności zamiast z publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="85e02-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="85e02-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85e02-111">EXAMPLES</span></span>

### <span data-ttu-id="85e02-112">Przykład 1. Tworzenie nowego obwodu ExpressRoute z konfiguracją komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="85e02-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
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

## <span data-ttu-id="85e02-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85e02-113">PARAMETERS</span></span>

### <span data-ttu-id="85e02-114">-Legacymode</span><span class="sxs-lookup"><span data-stu-id="85e02-114">-LegacyMode</span></span>
<span data-ttu-id="85e02-115">Starszy tryb komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="85e02-115">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="85e02-116">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="85e02-116">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="85e02-117">W przypadku PeeringType MicrosoftPeering musisz podać listę wszystkich prefiksów, które mają być anonsowane przez sesję BGP.</span><span class="sxs-lookup"><span data-stu-id="85e02-117">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="85e02-118">Akceptowane są tylko publiczne prefiksy adresów IP.</span><span class="sxs-lookup"><span data-stu-id="85e02-118">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="85e02-119">Możesz wysłać listę rozdzielonych przecinkami, jeśli planujesz wysłać zestaw prefiksów.</span><span class="sxs-lookup"><span data-stu-id="85e02-119">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="85e02-120">Te prefiksy muszą być zarejestrowane w nazwie rejestru routingu (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="85e02-120">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="85e02-121">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="85e02-121">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="85e02-122">Jeśli masz prefiksy reklamowe, które nie są zarejestrowane w przypadku komunikacji równorzędnej jako liczba, możesz określić numer AS, na który są zarejestrowani.</span><span class="sxs-lookup"><span data-stu-id="85e02-122">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="85e02-123">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="85e02-123">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="85e02-124">Nazwa rejestru routingu (RIR/IRR), do której jest rejestrowany numer AS i prefiksy.</span><span class="sxs-lookup"><span data-stu-id="85e02-124">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="85e02-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85e02-125">-Name</span></span>
<span data-ttu-id="85e02-126">Nazwa konfiguracji elementu równorzędnego do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="85e02-126">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="85e02-127">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="85e02-127">-PeerAddressType</span></span>
<span data-ttu-id="85e02-128">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="85e02-128">PeerAddressType</span></span>

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

### <span data-ttu-id="85e02-129">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="85e02-129">-PeerASN</span></span>
<span data-ttu-id="85e02-130">Numer AS obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="85e02-130">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="85e02-131">To musi być publiczna WPW, gdy PeeringType jest AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="85e02-131">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="85e02-132">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="85e02-132">-PeeringType</span></span>
<span data-ttu-id="85e02-133">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="85e02-133">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="85e02-134">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="85e02-134">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="85e02-135">Jest to zakres adresów IP dla podstawowej ścieżki routingu tej relacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="85e02-135">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="85e02-136">To musi być podsieć CIDR/30.</span><span class="sxs-lookup"><span data-stu-id="85e02-136">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="85e02-137">Pierwszy adres o numerze nieparzystym w tej podsieci powinien być przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="85e02-137">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="85e02-138">Na platformie Azure zostanie skonfigurowane kolejne adresy o numerze parzystym w interfejsie routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="85e02-138">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="85e02-139">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="85e02-139">-RouteFilter</span></span>
<span data-ttu-id="85e02-140">To jest istniejący obiekt RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="85e02-140">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="85e02-141">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="85e02-141">-RouteFilterId</span></span>
<span data-ttu-id="85e02-142">Jest to identyfikator zasobu istniejącego obiektu RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="85e02-142">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="85e02-143">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="85e02-143">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="85e02-144">Jest to zakres adresów IP pomocniczej ścieżki routingu tej relacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="85e02-144">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="85e02-145">To musi być podsieć CIDR/30.</span><span class="sxs-lookup"><span data-stu-id="85e02-145">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="85e02-146">Pierwszy adres o numerze nieparzystym w tej podsieci powinien być przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="85e02-146">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="85e02-147">Na platformie Azure zostanie skonfigurowane kolejne adresy o numerze parzystym w interfejsie routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="85e02-147">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="85e02-148">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="85e02-148">-SharedKey</span></span>
<span data-ttu-id="85e02-149">Jest to opcjonalna wartość skrótu MD5 używana jako klucz wstępny dla konfiguracji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="85e02-149">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="85e02-150">-VlanId</span><span class="sxs-lookup"><span data-stu-id="85e02-150">-VlanId</span></span>
<span data-ttu-id="85e02-151">Jest to numer identyfikacyjny sieci VLAN przypisanej do tej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="85e02-151">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="85e02-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85e02-152">-DefaultProfile</span></span>
<span data-ttu-id="85e02-153">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85e02-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85e02-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e02-154">CommonParameters</span></span>
<span data-ttu-id="85e02-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85e02-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e02-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85e02-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e02-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85e02-157">INPUTS</span></span>

## <span data-ttu-id="85e02-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85e02-158">OUTPUTS</span></span>

### <span data-ttu-id="85e02-159">Microsoft. Azure. Commands. Network. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="85e02-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="85e02-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85e02-160">NOTES</span></span>

## <span data-ttu-id="85e02-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85e02-161">RELATED LINKS</span></span>

[<span data-ttu-id="85e02-162">Dodaj-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="85e02-162">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="85e02-163">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="85e02-163">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="85e02-164">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="85e02-164">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="85e02-165">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="85e02-165">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
