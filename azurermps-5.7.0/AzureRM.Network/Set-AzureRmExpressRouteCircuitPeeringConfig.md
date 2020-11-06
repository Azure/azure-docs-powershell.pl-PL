---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: f9d2cc0959cd14e76500f2da85a23c93358c7e50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542519"
---
# <span data-ttu-id="e306a-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e306a-101">Set-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="e306a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e306a-102">SYNOPSIS</span></span>
<span data-ttu-id="e306a-103">Zapisuje zmodyfikowaną konfigurację komunikacji równorzędnej ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e306a-103">Saves a modified ExpressRoute peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e306a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e306a-104">SYNTAX</span></span>

### <span data-ttu-id="e306a-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e306a-105">SetByResource (Default)</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e306a-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="e306a-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e306a-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="e306a-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e306a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e306a-108">DESCRIPTION</span></span>
<span data-ttu-id="e306a-109">Polecenia cmdlet **Set-AzureRmExpressRouteCircuitPeeringConfig** umożliwiają powrót do platformy Azure zmodyfikowanej konfiguracji równorzędnej usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e306a-109">The **Set-AzureRmExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="e306a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e306a-110">EXAMPLES</span></span>

### <span data-ttu-id="e306a-111">Przykład 1. Zmienianie istniejącej konfiguracji komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="e306a-111">Example 1: Change an existing peering configuration</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzureRmExpressRouteCircuitPeeringConfig @parameters
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="e306a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e306a-112">PARAMETERS</span></span>

### <span data-ttu-id="e306a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e306a-113">-DefaultProfile</span></span>
<span data-ttu-id="e306a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e306a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e306a-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e306a-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="e306a-116">Obiekt obwodu ExpressRoute zawierający konfigurację komunikacji równorzędnej do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="e306a-116">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="e306a-117">-Legacymode</span><span class="sxs-lookup"><span data-stu-id="e306a-117">-LegacyMode</span></span>
<span data-ttu-id="e306a-118">Starszy tryb komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="e306a-118">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="e306a-119">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="e306a-119">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="e306a-120">W przypadku PeeringType MicrosoftPeering musisz podać listę wszystkich prefiksów, które mają być anonsowane przez sesję BGP.</span><span class="sxs-lookup"><span data-stu-id="e306a-120">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="e306a-121">Akceptowane są tylko publiczne prefiksy adresów IP.</span><span class="sxs-lookup"><span data-stu-id="e306a-121">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="e306a-122">Możesz wysłać listę rozdzielonych przecinkami, jeśli planujesz wysłać zestaw prefiksów.</span><span class="sxs-lookup"><span data-stu-id="e306a-122">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="e306a-123">Te prefiksy muszą być zarejestrowane w nazwie rejestru routingu (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="e306a-123">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="e306a-124">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="e306a-124">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="e306a-125">Jeśli masz prefiksy reklamowe, które nie są zarejestrowane w przypadku komunikacji równorzędnej jako liczba, możesz określić numer AS, na który są zarejestrowani.</span><span class="sxs-lookup"><span data-stu-id="e306a-125">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="e306a-126">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="e306a-126">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="e306a-127">Nazwa rejestru routingu (RIR/IRR), do której jest rejestrowany numer AS i prefiksy.</span><span class="sxs-lookup"><span data-stu-id="e306a-127">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="e306a-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e306a-128">-Name</span></span>
<span data-ttu-id="e306a-129">Nazwa konfiguracji komunikacji równorzędnej do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="e306a-129">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="e306a-130">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="e306a-130">-PeerAddressType</span></span>
<span data-ttu-id="e306a-131">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="e306a-131">PeerAddressType</span></span>

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

### <span data-ttu-id="e306a-132">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="e306a-132">-PeerASN</span></span>
<span data-ttu-id="e306a-133">Numer AS obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e306a-133">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="e306a-134">To musi być publiczna WPW, gdy PeeringType jest AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="e306a-134">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e306a-135">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="e306a-135">-PeeringType</span></span>
<span data-ttu-id="e306a-136">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="e306a-136">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="e306a-137">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e306a-137">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="e306a-138">Jest to zakres adresów IP dla podstawowej ścieżki routingu tej relacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="e306a-138">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="e306a-139">To musi być podsieć CIDR/30.</span><span class="sxs-lookup"><span data-stu-id="e306a-139">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="e306a-140">Pierwszy adres o numerze nieparzystym w tej podsieci powinien być przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="e306a-140">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="e306a-141">Na platformie Azure zostanie skonfigurowane kolejne adresy o numerze parzystym w interfejsie routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e306a-141">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="e306a-142">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="e306a-142">-RouteFilter</span></span>
<span data-ttu-id="e306a-143">To jest istniejący obiekt RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="e306a-143">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="e306a-144">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="e306a-144">-RouteFilterId</span></span>
<span data-ttu-id="e306a-145">Jest to identyfikator zasobu istniejącego obiektu RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="e306a-145">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="e306a-146">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e306a-146">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="e306a-147">Jest to zakres adresów IP pomocniczej ścieżki routingu tej relacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="e306a-147">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="e306a-148">To musi być podsieć CIDR/30.</span><span class="sxs-lookup"><span data-stu-id="e306a-148">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="e306a-149">Pierwszy adres o numerze nieparzystym w tej podsieci powinien być przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="e306a-149">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="e306a-150">Na platformie Azure zostanie skonfigurowane kolejne adresy o numerze parzystym w interfejsie routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e306a-150">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="e306a-151">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="e306a-151">-SharedKey</span></span>
<span data-ttu-id="e306a-152">Jest to opcjonalna wartość skrótu MD5 używana jako klucz wstępny dla konfiguracji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="e306a-152">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="e306a-153">-VlanId</span><span class="sxs-lookup"><span data-stu-id="e306a-153">-VlanId</span></span>
<span data-ttu-id="e306a-154">Jest to numer identyfikacyjny sieci VLAN przypisanej do tej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="e306a-154">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="e306a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e306a-155">CommonParameters</span></span>
<span data-ttu-id="e306a-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e306a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e306a-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e306a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e306a-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e306a-158">INPUTS</span></span>

### <span data-ttu-id="e306a-159">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e306a-159">PSExpressRouteCircuit</span></span>
<span data-ttu-id="e306a-160">Parametr "ExpressRouteCircuit" akceptuje wartość typu "PSExpressRouteCircuit" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="e306a-160">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="e306a-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e306a-161">OUTPUTS</span></span>

### <span data-ttu-id="e306a-162">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e306a-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e306a-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e306a-163">NOTES</span></span>

## <span data-ttu-id="e306a-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e306a-164">RELATED LINKS</span></span>

[<span data-ttu-id="e306a-165">Dodaj-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e306a-165">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e306a-166">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e306a-166">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e306a-167">Nowe — AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e306a-167">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e306a-168">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e306a-168">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)
