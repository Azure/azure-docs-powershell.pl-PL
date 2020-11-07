---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 92740ce457c9e7c571f925e1813bc120a88a86a5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709684"
---
# <span data-ttu-id="8b750-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="8b750-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="8b750-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b750-102">SYNOPSIS</span></span>
<span data-ttu-id="8b750-103">Umożliwia dodanie konfiguracji równorzędnej do połączenia z ExpressRoute krzyżowej.</span><span class="sxs-lookup"><span data-stu-id="8b750-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="8b750-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b750-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b750-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8b750-105">DESCRIPTION</span></span>
<span data-ttu-id="8b750-106">Polecenie cmdlet **Add-AzExpressRouteCrossConnectionPeering** umożliwia dodanie konfiguracji komunikacji równorzędnej do połączenia krzyżowego ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8b750-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="8b750-107">Uwaga: po uruchomieniu polecenia **Add-AzExpressRouteCrossConnectionPeering** musisz zadzwonić do apletu polecenia cmdlet Set-AzExpressRouteCrossConnection, aby aktywować konfigurację.</span><span class="sxs-lookup"><span data-stu-id="8b750-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering** , you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="8b750-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b750-108">EXAMPLES</span></span>

### <span data-ttu-id="8b750-109">Przykład 1: Dodawanie elementu równorzędnego do istniejącego połączenia krzyżowego ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="8b750-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
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

## <span data-ttu-id="8b750-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b750-110">PARAMETERS</span></span>

### <span data-ttu-id="8b750-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b750-111">-DefaultProfile</span></span>
<span data-ttu-id="8b750-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b750-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b750-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8b750-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="8b750-114">Jest modyfikowane połączenie krzyżowe ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8b750-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="8b750-115">To jest obiekt Azure zwrócony przez polecenie cmdlet **Get-AzExpressRouteCrossConnection** .</span><span class="sxs-lookup"><span data-stu-id="8b750-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

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

### <span data-ttu-id="8b750-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8b750-116">-Force</span></span>
<span data-ttu-id="8b750-117">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="8b750-117">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="8b750-118">-MicrosoftConfigAdvertisedPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="8b750-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="8b750-119">W przypadku PeeringType MicrosoftPeering musisz podać listę wszystkich prefiksów, które mają być anonsowane przez sesję BGP.</span><span class="sxs-lookup"><span data-stu-id="8b750-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="8b750-120">Akceptowane są tylko publiczne prefiksy adresów IP.</span><span class="sxs-lookup"><span data-stu-id="8b750-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="8b750-121">Możesz wysłać listę rozdzielonych przecinkami, jeśli planujesz wysłać zestaw prefiksów.</span><span class="sxs-lookup"><span data-stu-id="8b750-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="8b750-122">Te prefiksy muszą być zarejestrowane w nazwie rejestru routingu (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="8b750-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="8b750-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="8b750-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="8b750-124">Jeśli masz prefiksy reklamowe, które nie są zarejestrowane w przypadku komunikacji równorzędnej jako liczba, możesz określić numer AS, na który są zarejestrowani.</span><span class="sxs-lookup"><span data-stu-id="8b750-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="8b750-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="8b750-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="8b750-126">Nazwa rejestru routingu (RIR/IRR), do której jest rejestrowany numer AS i prefiksy.</span><span class="sxs-lookup"><span data-stu-id="8b750-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="8b750-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8b750-127">-Name</span></span>
<span data-ttu-id="8b750-128">Nazwa relacji komunikacji równorzędnej, która ma zostać dodana.</span><span class="sxs-lookup"><span data-stu-id="8b750-128">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="8b750-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="8b750-129">-PeerAddressType</span></span>
<span data-ttu-id="8b750-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="8b750-130">PeerAddressType</span></span>

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

### <span data-ttu-id="8b750-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="8b750-131">-PeerASN</span></span>
<span data-ttu-id="8b750-132">Numer AS połączenia z ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8b750-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="8b750-133">To musi być publiczna WPW, gdy PeeringType jest AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="8b750-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="8b750-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="8b750-134">-PeeringType</span></span>
<span data-ttu-id="8b750-135">Dopuszczalne wartości tego parametru to: `AzurePrivatePeering` , `AzurePublicPeering` i `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="8b750-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="8b750-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8b750-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="8b750-137">Jest to zakres adresów IP dla podstawowej ścieżki routingu tej relacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="8b750-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="8b750-138">To musi być podsieć CIDR/30.</span><span class="sxs-lookup"><span data-stu-id="8b750-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="8b750-139">Pierwszy adres o numerze nieparzystym w tej podsieci powinien być przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="8b750-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="8b750-140">Na platformie Azure zostanie skonfigurowane kolejne adresy o numerze parzystym w interfejsie routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8b750-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="8b750-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8b750-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="8b750-142">Jest to zakres adresów IP pomocniczej ścieżki routingu tej relacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="8b750-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="8b750-143">To musi być podsieć CIDR/30.</span><span class="sxs-lookup"><span data-stu-id="8b750-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="8b750-144">Pierwszy adres o numerze nieparzystym w tej podsieci powinien być przypisany do interfejsu routera.</span><span class="sxs-lookup"><span data-stu-id="8b750-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="8b750-145">Na platformie Azure zostanie skonfigurowane kolejne adresy o numerze parzystym w interfejsie routera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8b750-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="8b750-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="8b750-146">-SharedKey</span></span>
<span data-ttu-id="8b750-147">Jest to opcjonalna wartość skrótu MD5 używana jako klucz wstępny dla konfiguracji komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="8b750-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="8b750-148">-VlanId</span><span class="sxs-lookup"><span data-stu-id="8b750-148">-VlanId</span></span>
<span data-ttu-id="8b750-149">Jest to numer identyfikacyjny sieci VLAN przypisanej do tej komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="8b750-149">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="8b750-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b750-150">-Confirm</span></span>
<span data-ttu-id="8b750-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b750-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b750-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b750-152">-WhatIf</span></span>
<span data-ttu-id="8b750-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b750-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b750-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8b750-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b750-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b750-155">CommonParameters</span></span>
<span data-ttu-id="8b750-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b750-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b750-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b750-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b750-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b750-158">INPUTS</span></span>

### <span data-ttu-id="8b750-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8b750-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="8b750-160">Parametr "ExpressRouteCrossConnection" akceptuje wartość typu "PSExpressRouteCrossConnection" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="8b750-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="8b750-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b750-161">OUTPUTS</span></span>

### <span data-ttu-id="8b750-162">Microsoft. Azure. Commands. Network. models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8b750-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="8b750-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b750-163">NOTES</span></span>

## <span data-ttu-id="8b750-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b750-164">RELATED LINKS</span></span>

[<span data-ttu-id="8b750-165">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="8b750-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="8b750-166">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="8b750-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="8b750-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8b750-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="8b750-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8b750-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
