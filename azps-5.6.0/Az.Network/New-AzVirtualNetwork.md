---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: 9608dfd5a780006d2ab050a1ca2e85ee26949f97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961729"
---
# <span data-ttu-id="80c09-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="80c09-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="80c09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80c09-102">SYNOPSIS</span></span>
<span data-ttu-id="80c09-103">Tworzy sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="80c09-103">Creates a virtual network.</span></span>

## <span data-ttu-id="80c09-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="80c09-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-BgpCommunity <String>] [-Tag <Hashtable>]
 [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-IpAllocation <PSIpAllocation[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80c09-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="80c09-105">DESCRIPTION</span></span>
<span data-ttu-id="80c09-106">Polecenie **cmdlet New-AzVirtualNetwork** tworzy sieć wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="80c09-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="80c09-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="80c09-107">EXAMPLES</span></span>

### <span data-ttu-id="80c09-108">Przykład 1. Tworzenie sieci wirtualnej z dwiema podsieciami</span><span class="sxs-lookup"><span data-stu-id="80c09-108">Example 1: Create a virtual network with two subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="80c09-109">W tym przykładzie jest tworzyna sieć wirtualna z dwiema podsieciami.</span><span class="sxs-lookup"><span data-stu-id="80c09-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="80c09-110">Najpierw w regionie centralus jest tworzona nowa grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="80c09-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="80c09-111">Następnie w tym przykładzie są tworzyne reprezentacje w pamięci dwóch podsieci.</span><span class="sxs-lookup"><span data-stu-id="80c09-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="80c09-112">Polecenie New-AzVirtualNetworkSubnetConfig nie utworzy żadnej podsieci po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="80c09-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="80c09-113">Istnieje jedna podsieci o nazwie FrontendSubnet i jedna podsieci o nazwie BackendSubnet.</span><span class="sxs-lookup"><span data-stu-id="80c09-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="80c09-114">Polecenie cmdlet New-AzVirtualNetwork następnie tworzy sieć wirtualną, używając kodów CIDR 10.0.0.0/16 jako prefiksu adresu i dwóch podsieci.</span><span class="sxs-lookup"><span data-stu-id="80c09-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="80c09-115">Przykład 2. Tworzenie sieci wirtualnej z ustawieniami DNS</span><span class="sxs-lookup"><span data-stu-id="80c09-115">Example 2: Create a virtual network with DNS settings</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="80c09-116">W tym przykładzie jest tworzyć sieć wirtualną z dwoma podsieciami i dwoma serwerami DNS.</span><span class="sxs-lookup"><span data-stu-id="80c09-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="80c09-117">Określenie serwerów DNS w sieci wirtualnej jest skutkiem tego, że serwery niP/maszyny wirtualne wdrożone w tej sieci wirtualnej dziedziczą te serwery DNS jako domyślne.</span><span class="sxs-lookup"><span data-stu-id="80c09-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="80c09-118">Te ustawienia domyślne można za pomocą ustawienia na poziomie NIC zastępować na poziomie nic.</span><span class="sxs-lookup"><span data-stu-id="80c09-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="80c09-119">Jeśli w witrynie VNET nie określono żadnych serwerów DNS, a na tych sieciach nie określono serwerów DNS, na potrzeby rozpoznawania nazw DNS są używane domyślne serwery DNS platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="80c09-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="80c09-120">Przykład 3. Tworzenie sieci wirtualnej z podsiecią odwołującą się do grupy zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="80c09-120">Example 3: Create a virtual network with a subnet referencing a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="80c09-121">W tym przykładzie jest tworzyna sieć wirtualna z podsieciami odwołującymi się do grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="80c09-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="80c09-122">Najpierw w przykładzie jest tworzona grupa zasobów jako kontener dla zasobów, które zostaną utworzone.</span><span class="sxs-lookup"><span data-stu-id="80c09-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="80c09-123">Następnie jest tworzona grupa zabezpieczeń sieciowych, która umożliwia przychodzący dostęp za pomocą protokołu RDP, ale w przeciwnym razie wymusza domyślne reguły grupy zabezpieczeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="80c09-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="80c09-124">Następnie New-AzVirtualNetworkSubnetConfig cmdlet tworzy reprezentacje w pamięci dwóch podsieci, które odwołują się do utworzonej grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="80c09-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="80c09-125">Polecenie New-AzVirtualNetwork następnie tworzy sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="80c09-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="80c09-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80c09-126">PARAMETERS</span></span>

### <span data-ttu-id="80c09-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="80c09-127">-AddressPrefix</span></span>
<span data-ttu-id="80c09-128">Określa zakres adresów IP dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="80c09-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c09-129">— AsJob</span><span class="sxs-lookup"><span data-stu-id="80c09-129">-AsJob</span></span>
<span data-ttu-id="80c09-130">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="80c09-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80c09-131">-BgpCommunity</span><span class="sxs-lookup"><span data-stu-id="80c09-131">-BgpCommunity</span></span>
<span data-ttu-id="80c09-132">Społeczność BGP ogłaszana za pośrednictwem usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="80c09-132">The BGP Community advertised over ExpressRoute.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c09-133">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="80c09-133">-DdosProtectionPlanId</span></span>
<span data-ttu-id="80c09-134">Odwołanie do zasobu planu ochrony DDoS skojarzonego z siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="80c09-134">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c09-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c09-135">-DefaultProfile</span></span>
<span data-ttu-id="80c09-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="80c09-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80c09-137">- DnsServer</span><span class="sxs-lookup"><span data-stu-id="80c09-137">-DnsServer</span></span>
<span data-ttu-id="80c09-138">Określa serwer DNS dla podsieci.</span><span class="sxs-lookup"><span data-stu-id="80c09-138">Specifies the DNS server for a subnet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c09-139">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="80c09-139">-EnableDdosProtection</span></span>
<span data-ttu-id="80c09-140">Parametr przełącznika reprezentujący, czy ochrona przed DDoS jest włączona, czy nie.</span><span class="sxs-lookup"><span data-stu-id="80c09-140">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c09-141">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="80c09-141">-Force</span></span>
<span data-ttu-id="80c09-142">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="80c09-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="80c09-143">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="80c09-143">-IpAllocation</span></span>
<span data-ttu-id="80c09-144">Określa alokacje IpAllocations dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="80c09-144">Specifies IpAllocations for a virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c09-145">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="80c09-145">-Location</span></span>
<span data-ttu-id="80c09-146">Określa region sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="80c09-146">Specifies the region for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c09-147">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="80c09-147">-Name</span></span>
<span data-ttu-id="80c09-148">Określa nazwę sieci wirtualnej, która tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80c09-148">Specifies the name of the virtual network that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c09-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80c09-149">-ResourceGroupName</span></span>
<span data-ttu-id="80c09-150">Określa nazwę grupy zasobów, która ma zawierać sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="80c09-150">Specifies the name of a resource group to contain the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c09-151">-Subnet</span><span class="sxs-lookup"><span data-stu-id="80c09-151">-Subnet</span></span>
<span data-ttu-id="80c09-152">Określa listę podsieci do skojarzenia z siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="80c09-152">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c09-153">— Tag</span><span class="sxs-lookup"><span data-stu-id="80c09-153">-Tag</span></span>
<span data-ttu-id="80c09-154">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="80c09-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="80c09-155">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="80c09-155">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80c09-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80c09-156">-Confirm</span></span>
<span data-ttu-id="80c09-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="80c09-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c09-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80c09-158">-WhatIf</span></span>
<span data-ttu-id="80c09-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80c09-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80c09-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="80c09-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c09-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c09-161">CommonParameters</span></span>
<span data-ttu-id="80c09-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80c09-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c09-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80c09-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c09-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80c09-164">INPUTS</span></span>

### <span data-ttu-id="80c09-165">System.String</span><span class="sxs-lookup"><span data-stu-id="80c09-165">System.String</span></span>

### <span data-ttu-id="80c09-166">System.String[]</span><span class="sxs-lookup"><span data-stu-id="80c09-166">System.String[]</span></span>

### <span data-ttu-id="80c09-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span><span class="sxs-lookup"><span data-stu-id="80c09-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span></span>

### <span data-ttu-id="80c09-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="80c09-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="80c09-169">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80c09-169">OUTPUTS</span></span>

### <span data-ttu-id="80c09-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="80c09-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="80c09-171">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="80c09-171">NOTES</span></span>

## <span data-ttu-id="80c09-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80c09-172">RELATED LINKS</span></span>

[<span data-ttu-id="80c09-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="80c09-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="80c09-174">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="80c09-174">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="80c09-175">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="80c09-175">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="80c09-176">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="80c09-176">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)
