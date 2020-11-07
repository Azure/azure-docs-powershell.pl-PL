---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 95c361199e813d5a79bd8f49858ad8d924bd02f3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890997"
---
# <span data-ttu-id="b552e-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b552e-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="b552e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b552e-102">SYNOPSIS</span></span>
<span data-ttu-id="b552e-103">Umożliwia dodanie konfiguracji komunikacji równorzędnej do obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b552e-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="b552e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b552e-104">SYNTAX</span></span>

### <span data-ttu-id="b552e-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b552e-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b552e-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="b552e-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b552e-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="b552e-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b552e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b552e-108">DESCRIPTION</span></span>
<span data-ttu-id="b552e-109">Polecenie cmdlet **Add-AzExpressRouteCircuitPeeringConfig** umożliwia dodanie konfiguracji komunikacji równorzędnej do obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b552e-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="b552e-110">Obwody ExpressRoute łączą sieć lokalną z chmurą firmy Microsoft, korzystając z dostawcy usług łączności zamiast z publicznego Internetu.</span><span class="sxs-lookup"><span data-stu-id="b552e-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="b552e-111">Uwaga: po uruchomieniu polecenia **Add-AzExpressRouteCircuitPeeringConfig** musisz zadzwonić do apletu polecenia cmdlet Set-AzExpressRouteCircuit, aby aktywować konfigurację.</span><span class="sxs-lookup"><span data-stu-id="b552e-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="b552e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b552e-112">EXAMPLES</span></span>

### <span data-ttu-id="b552e-113">Przykład 1: Dodawanie elementu równorzędnego do istniejącego obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="b552e-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
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

## <span data-ttu-id="b552e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b552e-114">PARAMETERS</span></span>

### <span data-ttu-id="b552e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b552e-115">-DefaultProfile</span></span>
<span data-ttu-id="b552e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b552e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b552e-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b552e-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="b552e-118">Obwód ExpressRoute jest modyfikowany.</span><span class="sxs-lookup"><span data-stu-id="b552e-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="b552e-119">To jest obiekt Azure zwrócony przez polecenie cmdlet **Get-AzExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="b552e-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b552e-120">-Legacymode</span><span class="sxs-lookup"><span data-stu-id="b552e-120">-LegacyMode</span></span>
<span data-ttu-id="b552e-121">Starszy tryb komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="b552e-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="b552e-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="b552e-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="b552e-123">W przypadku PeeringType MicrosoftPeering musisz podać listę wszystkich prefiksów, które mają być anonsowane przez sesję BGP.</span><span class="sxs-lookup"><span data-stu-id="b552e-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="b552e-124">Akceptowane są tylko publiczne prefiksy adresów IP.</span><span class="sxs-lookup"><span data-stu-id="b552e-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="b552e-125">Możesz wysłać listę rozdzielonych przecinkami, jeśli planujesz wysłać zestaw prefiksów.</span><span class="sxs-lookup"><span data-stu-id="b552e-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="b552e-126">Te prefiksy muszą być zarejestrowane w nazwie rejestru routingu (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="b552e-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="b552e-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="b552e-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="b552e-128">Jeśli masz prefiksy reklamowe, które nie są zarejestrowane w przypadku komunikacji równorzędnej jako liczba, możesz określić numer AS, na który są zarejestrowani.</span><span class="sxs-lookup"><span data-stu-id="b552e-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="b552e-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="b552e-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="b552e-130">Nazwa rejestru routingu (RIR/IRR), do której jest rejestrowany numer AS i prefiksy.</span><span class="sxs-lookup"><span data-stu-id="b552e-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="b552e-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b552e-131">-Name</span></span>
<span data-ttu-id="b552e-132">Nazwa relacji komunikacji równorzędnej, która ma zostać dodana.</span><span class="sxs-lookup"><span data-stu-id="b552e-132">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="b552e-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="b552e-133">-PeerAddressType</span></span>
<span data-ttu-id="b552e-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="b552e-134">PeerAddressType</span></span>

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

### <span data-ttu-id="b552e-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="b552e-135">-PeerASN</span></span>
<span data-ttu-id="b552e-136">Numer AS obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b552e-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="b552e-137">To musi być publiczna WPW, gdy PeeringType jest AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="b552e-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="b552e-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="b552e-138">-PeeringType</span></span>
<span data-ttu-id="b552e-139">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="b552e-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="b552e-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b552e-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="b552e-141">Jest to zakres adresów IP dla podstawowej ścieżki routingu tej relacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="b552e-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="b552e-142">To musi być podsieć CIDR/30.</span><span class="sxs-lookup"><span data-stu-id="b552e-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="b552e-143">Pierwszy adres o numerze nieparzystym w tej podsieci powinien być przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="b552e-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="b552e-144">Na platformie Azure zostanie skonfigurowane kolejne adresy o numerze parzystym w interfejsie routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b552e-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="b552e-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b552e-145">-RouteFilter</span></span>
<span data-ttu-id="b552e-146">To jest istniejący obiekt RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="b552e-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="b552e-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="b552e-147">-RouteFilterId</span></span>
<span data-ttu-id="b552e-148">Jest to identyfikator zasobu istniejącego obiektu RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="b552e-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="b552e-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b552e-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="b552e-150">Jest to zakres adresów IP pomocniczej ścieżki routingu tej relacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="b552e-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="b552e-151">To musi być podsieć CIDR/30.</span><span class="sxs-lookup"><span data-stu-id="b552e-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="b552e-152">Pierwszy adres o numerze nieparzystym w tej podsieci powinien być przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="b552e-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="b552e-153">Na platformie Azure zostanie skonfigurowane kolejne adresy o numerze parzystym w interfejsie routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b552e-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="b552e-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="b552e-154">-SharedKey</span></span>
<span data-ttu-id="b552e-155">Jest to opcjonalna wartość skrótu MD5 używana jako klucz wstępny dla konfiguracji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="b552e-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="b552e-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="b552e-156">-VlanId</span></span>
<span data-ttu-id="b552e-157">Jest to numer identyfikacyjny sieci VLAN przypisanej do tej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="b552e-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="b552e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b552e-158">CommonParameters</span></span>
<span data-ttu-id="b552e-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b552e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b552e-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b552e-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b552e-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b552e-161">INPUTS</span></span>

### <span data-ttu-id="b552e-162">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b552e-162">PSExpressRouteCircuit</span></span>
<span data-ttu-id="b552e-163">Parametr "ExpressRouteCircuit" akceptuje wartość typu "PSExpressRouteCircuit" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="b552e-163">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="b552e-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b552e-164">OUTPUTS</span></span>

### <span data-ttu-id="b552e-165">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b552e-165">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b552e-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b552e-166">NOTES</span></span>

## <span data-ttu-id="b552e-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b552e-167">RELATED LINKS</span></span>

[<span data-ttu-id="b552e-168">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b552e-168">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b552e-169">Nowe — AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b552e-169">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="b552e-170">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b552e-170">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="b552e-171">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b552e-171">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
