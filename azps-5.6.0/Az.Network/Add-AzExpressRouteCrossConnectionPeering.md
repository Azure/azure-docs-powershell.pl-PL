---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: b16206fdcaf775315947ca9fe71f487d1f9d8df1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011914"
---
# <span data-ttu-id="ab7c6-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ab7c6-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="ab7c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab7c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ab7c6-103">Dodaje konfigurację komunikacji równorzędnej do połączenia krzyżowego usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="ab7c6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ab7c6-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab7c6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ab7c6-105">DESCRIPTION</span></span>
<span data-ttu-id="ab7c6-106">Polecenie **cmdlet Add-AzExpressRouteCrossConnectionPeering** dodaje konfigurację komunikacji równorzędnej do połączenia krzyżowego usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="ab7c6-107">Pamiętaj, że po uruchomieniu dodatku **AzExpressRouteCrossConnectionPeering** musisz wywołać Set-AzExpressRouteCrossConnection cmdlet, aby aktywować konfigurację.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering**, you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="ab7c6-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ab7c6-108">EXAMPLES</span></span>

### <span data-ttu-id="ab7c6-109">Przykład 1. Dodawanie elementu równorzędnego do istniejącego połączenia krzyżowego expressRoute</span><span class="sxs-lookup"><span data-stu-id="ab7c6-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    CrossConnection = $cc
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCrossConnectionPeering @parameters
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="ab7c6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab7c6-110">PARAMETERS</span></span>

### <span data-ttu-id="ab7c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab7c6-111">-DefaultProfile</span></span>
<span data-ttu-id="ab7c6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab7c6-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ab7c6-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="ab7c6-114">Modyfikowane połączenie krzyżowe expressroute.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="ab7c6-115">Jest to obiekt platformy Azure zwrócony przez polecenie cmdlet **Get-AzExpressRouteCrossConnection.**</span><span class="sxs-lookup"><span data-stu-id="ab7c6-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7c6-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ab7c6-116">-Force</span></span>
<span data-ttu-id="ab7c6-117">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="ab7c6-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7c6-118">-MicrosoftConfigAdvertconfigPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="ab7c6-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="ab7c6-119">W przypadku typu komunikacji równorzędnej microsoftPeering należy podać listę wszystkich prefiksów, które mają być ogłaszane za pośrednictwem sesji BGP.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="ab7c6-120">Akceptowane są tylko prefiksy publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="ab7c6-121">Jeśli zamierzasz wysłać zestaw prefiksów, możesz wysłać listę rozdzieloną przecinkami.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="ab7c6-122">Te prefiksy muszą być zarejestrowane w nazwie rejestru routingu (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="ab7c6-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="ab7c6-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="ab7c6-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="ab7c6-124">W przypadku reklamowania prefiksów, które nie są zarejestrowane dla numeru AS komunikacji równorzędnej, możesz określić numer AS, pod którym są one zarejestrowane.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="ab7c6-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="ab7c6-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="ab7c6-126">Nazwa rejestru routingu (RIR/IRR), do której jest zarejestrowany numer AS i prefiksy.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="ab7c6-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ab7c6-127">-Name</span></span>
<span data-ttu-id="ab7c6-128">Nazwa relacji komunikacji równorzędnej, która ma zostać dodana.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-128">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="ab7c6-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ab7c6-129">-PeerAddressType</span></span>
<span data-ttu-id="ab7c6-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ab7c6-130">PeerAddressType</span></span>

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

### <span data-ttu-id="ab7c6-131">- PeerASN</span><span class="sxs-lookup"><span data-stu-id="ab7c6-131">-PeerASN</span></span>
<span data-ttu-id="ab7c6-132">Numer AS połączenia krzyżowego z usługą ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="ab7c6-133">Jeśli typ komunikacji równorzędnej to AzurePublicPeering, musi to być publiczna asn.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="ab7c6-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="ab7c6-134">-PeeringType</span></span>
<span data-ttu-id="ab7c6-135">Dopuszczalne wartości dla tego parametru to: `AzurePrivatePeering` `AzurePublicPeering` , i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="ab7c6-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="ab7c6-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ab7c6-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="ab7c6-137">Jest to zakres adresów IP dla podstawowej ścieżki routingu tej relacji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="ab7c6-138">Musi to być podsieci CIDR o proc. /30.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="ab7c6-139">Pierwszy adres nieparzystych w tej podsieci powinien zostać przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="ab7c6-140">Platforma Azure skonfiguruje następny adres o numerze nawet do interfejsu routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="ab7c6-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ab7c6-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="ab7c6-142">Jest to zakres adresów IP dla pomocniczej ścieżki routingu tej relacji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="ab7c6-143">Musi to być podsieci CIDR o proc. /30.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="ab7c6-144">Pierwszy adres nieparzystych w tej podsieci powinien zostać przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="ab7c6-145">Platforma Azure skonfiguruje następny adres o numerze nawet do interfejsu routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="ab7c6-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="ab7c6-146">-SharedKey</span></span>
<span data-ttu-id="ab7c6-147">Jest to opcjonalny skrót MD5 używany jako klucz wstępnie udostępniony dla konfiguracji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="ab7c6-148">-VlanId</span><span class="sxs-lookup"><span data-stu-id="ab7c6-148">-VlanId</span></span>
<span data-ttu-id="ab7c6-149">Jest to numer identyfikacyjny sieci VLAN przypisanej do tej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-149">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="ab7c6-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab7c6-150">-Confirm</span></span>
<span data-ttu-id="ab7c6-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7c6-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab7c6-152">-WhatIf</span></span>
<span data-ttu-id="ab7c6-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab7c6-154">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7c6-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab7c6-155">CommonParameters</span></span>
<span data-ttu-id="ab7c6-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab7c6-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab7c6-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab7c6-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab7c6-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab7c6-158">INPUTS</span></span>

### <span data-ttu-id="ab7c6-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ab7c6-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="ab7c6-160">Parametr "ExpressRouteCrossConnection" przyjmuje wartość typu "PSExpressRouteCrossConnection" z potoku</span><span class="sxs-lookup"><span data-stu-id="ab7c6-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="ab7c6-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab7c6-161">OUTPUTS</span></span>

### <span data-ttu-id="ab7c6-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ab7c6-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="ab7c6-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ab7c6-163">NOTES</span></span>

## <span data-ttu-id="ab7c6-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab7c6-164">RELATED LINKS</span></span>

[<span data-ttu-id="ab7c6-165">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ab7c6-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="ab7c6-166">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ab7c6-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="ab7c6-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ab7c6-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="ab7c6-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ab7c6-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
