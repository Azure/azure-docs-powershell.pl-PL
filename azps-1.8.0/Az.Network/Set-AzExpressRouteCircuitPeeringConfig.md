---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: ecbd0d101db979d5982891bbfbd4ad1e3083ee8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708989"
---
# <span data-ttu-id="a9c89-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a9c89-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="a9c89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9c89-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c89-103">Zapisuje zmodyfikowaną konfigurację komunikacji równorzędnej ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a9c89-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="a9c89-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9c89-104">SYNTAX</span></span>

### <span data-ttu-id="a9c89-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a9c89-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9c89-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="a9c89-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9c89-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="a9c89-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9c89-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a9c89-108">DESCRIPTION</span></span>
<span data-ttu-id="a9c89-109">Polecenia cmdlet **Set-AzExpressRouteCircuitPeeringConfig** umożliwiają powrót do platformy Azure zmodyfikowanej konfiguracji równorzędnej usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a9c89-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="a9c89-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9c89-110">EXAMPLES</span></span>

### <span data-ttu-id="a9c89-111">Przykład 1. Zmienianie istniejącej konfiguracji komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="a9c89-111">Example 1: Change an existing peering configuration</span></span>
```
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

## <span data-ttu-id="a9c89-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9c89-112">PARAMETERS</span></span>

### <span data-ttu-id="a9c89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c89-113">-DefaultProfile</span></span>
<span data-ttu-id="a9c89-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9c89-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9c89-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a9c89-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a9c89-116">Obiekt obwodu ExpressRoute zawierający konfigurację komunikacji równorzędnej do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="a9c89-116">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="a9c89-117">-Legacymode</span><span class="sxs-lookup"><span data-stu-id="a9c89-117">-LegacyMode</span></span>
<span data-ttu-id="a9c89-118">Starszy tryb komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="a9c89-118">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="a9c89-119">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="a9c89-119">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="a9c89-120">W przypadku PeeringType MicrosoftPeering musisz podać listę wszystkich prefiksów, które mają być anonsowane przez sesję BGP.</span><span class="sxs-lookup"><span data-stu-id="a9c89-120">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="a9c89-121">Akceptowane są tylko publiczne prefiksy adresów IP.</span><span class="sxs-lookup"><span data-stu-id="a9c89-121">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="a9c89-122">Możesz wysłać listę rozdzielonych przecinkami, jeśli planujesz wysłać zestaw prefiksów.</span><span class="sxs-lookup"><span data-stu-id="a9c89-122">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="a9c89-123">Te prefiksy muszą być zarejestrowane w nazwie rejestru routingu (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="a9c89-123">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="a9c89-124">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="a9c89-124">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="a9c89-125">Jeśli masz prefiksy reklamowe, które nie są zarejestrowane w przypadku komunikacji równorzędnej jako liczba, możesz określić numer AS, na który są zarejestrowani.</span><span class="sxs-lookup"><span data-stu-id="a9c89-125">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="a9c89-126">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="a9c89-126">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="a9c89-127">Nazwa rejestru routingu (RIR/IRR), do której jest rejestrowany numer AS i prefiksy.</span><span class="sxs-lookup"><span data-stu-id="a9c89-127">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="a9c89-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9c89-128">-Name</span></span>
<span data-ttu-id="a9c89-129">Nazwa konfiguracji komunikacji równorzędnej do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="a9c89-129">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="a9c89-130">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="a9c89-130">-PeerAddressType</span></span>
<span data-ttu-id="a9c89-131">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="a9c89-131">PeerAddressType</span></span>

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

### <span data-ttu-id="a9c89-132">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="a9c89-132">-PeerASN</span></span>
<span data-ttu-id="a9c89-133">Numer AS obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a9c89-133">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="a9c89-134">To musi być publiczna WPW, gdy PeeringType jest AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="a9c89-134">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="a9c89-135">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a9c89-135">-PeeringType</span></span>
<span data-ttu-id="a9c89-136">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a9c89-136">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="a9c89-137">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a9c89-137">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="a9c89-138">Jest to zakres adresów IP dla podstawowej ścieżki routingu tej relacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="a9c89-138">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="a9c89-139">To musi być podsieć CIDR/30.</span><span class="sxs-lookup"><span data-stu-id="a9c89-139">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="a9c89-140">Pierwszy adres o numerze nieparzystym w tej podsieci powinien być przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="a9c89-140">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="a9c89-141">Na platformie Azure zostanie skonfigurowane kolejne adresy o numerze parzystym w interfejsie routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a9c89-141">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="a9c89-142">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="a9c89-142">-RouteFilter</span></span>
<span data-ttu-id="a9c89-143">To jest istniejący obiekt RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="a9c89-143">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="a9c89-144">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="a9c89-144">-RouteFilterId</span></span>
<span data-ttu-id="a9c89-145">Jest to identyfikator zasobu istniejącego obiektu RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="a9c89-145">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="a9c89-146">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a9c89-146">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="a9c89-147">Jest to zakres adresów IP pomocniczej ścieżki routingu tej relacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="a9c89-147">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="a9c89-148">To musi być podsieć CIDR/30.</span><span class="sxs-lookup"><span data-stu-id="a9c89-148">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="a9c89-149">Pierwszy adres o numerze nieparzystym w tej podsieci powinien być przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="a9c89-149">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="a9c89-150">Na platformie Azure zostanie skonfigurowane kolejne adresy o numerze parzystym w interfejsie routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a9c89-150">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="a9c89-151">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="a9c89-151">-SharedKey</span></span>
<span data-ttu-id="a9c89-152">Jest to opcjonalna wartość skrótu MD5 używana jako klucz wstępny dla konfiguracji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="a9c89-152">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="a9c89-153">-VlanId</span><span class="sxs-lookup"><span data-stu-id="a9c89-153">-VlanId</span></span>
<span data-ttu-id="a9c89-154">Jest to numer identyfikacyjny sieci VLAN przypisanej do tej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="a9c89-154">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="a9c89-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c89-155">CommonParameters</span></span>
<span data-ttu-id="a9c89-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9c89-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c89-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9c89-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c89-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9c89-158">INPUTS</span></span>

### <span data-ttu-id="a9c89-159">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a9c89-159">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="a9c89-160">System. String</span><span class="sxs-lookup"><span data-stu-id="a9c89-160">System.String</span></span>

### <span data-ttu-id="a9c89-161">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a9c89-161">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="a9c89-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9c89-162">System.Boolean</span></span>

## <span data-ttu-id="a9c89-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9c89-163">OUTPUTS</span></span>

### <span data-ttu-id="a9c89-164">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a9c89-164">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a9c89-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9c89-165">NOTES</span></span>

## <span data-ttu-id="a9c89-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9c89-166">RELATED LINKS</span></span>

[<span data-ttu-id="a9c89-167">Dodaj-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a9c89-167">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a9c89-168">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a9c89-168">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a9c89-169">Nowe — AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a9c89-169">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a9c89-170">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a9c89-170">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)