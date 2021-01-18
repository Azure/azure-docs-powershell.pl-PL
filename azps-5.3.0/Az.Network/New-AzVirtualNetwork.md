---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: d131b4aa22f46fed151486ed2d87f32684b6035a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498686"
---
# <span data-ttu-id="d9c84-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d9c84-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="d9c84-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9c84-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c84-103">Tworzy sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="d9c84-103">Creates a virtual network.</span></span>

## <span data-ttu-id="d9c84-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9c84-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-BgpCommunity <String>] [-Tag <Hashtable>]
 [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-IpAllocation <PSIpAllocation[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9c84-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d9c84-105">DESCRIPTION</span></span>
<span data-ttu-id="d9c84-106">Polecenie cmdlet **New-AzVirtualNetwork** umożliwia utworzenie wirtualnej sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="d9c84-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="d9c84-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9c84-107">EXAMPLES</span></span>

### <span data-ttu-id="d9c84-108">Przykład 1. Tworzenie sieci wirtualnej z dwiema podsieciami</span><span class="sxs-lookup"><span data-stu-id="d9c84-108">Example 1: Create a virtual network with two subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="d9c84-109">W tym przykładzie przedstawiono tworzenie sieci wirtualnej z dwiema podsieciami.</span><span class="sxs-lookup"><span data-stu-id="d9c84-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="d9c84-110">Najpierw zostanie utworzona nowa grupa zasobów w regionie centralnym.</span><span class="sxs-lookup"><span data-stu-id="d9c84-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="d9c84-111">Następnie w przykładzie tworzone są reprezentacje w pamięci dwóch podsieci.</span><span class="sxs-lookup"><span data-stu-id="d9c84-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="d9c84-112">Polecenie cmdlet New-AzVirtualNetworkSubnetConfig nie powoduje utworzenia żadnej podsieci po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="d9c84-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="d9c84-113">Istnieje jedna podsieć o nazwie frontendSubnet i jedna podsieć o nazwie backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="d9c84-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="d9c84-114">Polecenie cmdlet New-AzVirtualNetwork powoduje utworzenie sieci wirtualnej przy użyciu notacji CIDR 10.0.0.0/16 jako prefiksu adresu i dwóch podsieci.</span><span class="sxs-lookup"><span data-stu-id="d9c84-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="d9c84-115">Przykład 2: tworzenie sieci wirtualnej przy użyciu ustawień DNS</span><span class="sxs-lookup"><span data-stu-id="d9c84-115">Example 2: Create a virtual network with DNS settings</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="d9c84-116">W tym przykładzie przedstawiono tworzenie sieci wirtualnej z dwiema podsieciami i dwoma serwerami DNS.</span><span class="sxs-lookup"><span data-stu-id="d9c84-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="d9c84-117">Efektem określenia serwerów DNS w sieci wirtualnej jest to, że karty sieciowe/maszyny wirtualne rozmieszczone w tej sieci wirtualnej będą dziedziczyć te serwery DNS jako domyślne.</span><span class="sxs-lookup"><span data-stu-id="d9c84-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="d9c84-118">Te wartości domyślne można przełączać na kartę sieciową za pośrednictwem ustawienia na poziomie karty NIC.</span><span class="sxs-lookup"><span data-stu-id="d9c84-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="d9c84-119">Jeśli w sieci wirtualnej nie są określone serwery DNS ani serwery DNS na kartach sieciowych, to w celu rozpoznawania nazw DNS są używane domyślne serwery DNS platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d9c84-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="d9c84-120">Przykład 3: tworzenie sieci wirtualnej z podsiecią, do której należy odwołanie do grupy zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="d9c84-120">Example 3: Create a virtual network with a subnet referencing a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="d9c84-121">W tym przykładzie jest tworzona Sieć wirtualna z podsieciami, które odwołują się do grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="d9c84-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="d9c84-122">Najpierw w przykładzie tworzona jest Grupa zasobów jako kontener dla zasobów, które zostaną utworzone.</span><span class="sxs-lookup"><span data-stu-id="d9c84-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="d9c84-123">Następnie zostanie utworzona grupa zabezpieczeń sieci umożliwiająca przychodzący dostęp do protokołu RDP, ale w przeciwnym razie wymusza domyślne reguły grupowych zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="d9c84-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="d9c84-124">Polecenie cmdlet New-AzVirtualNetworkSubnetConfig powoduje utworzenie reprezentacji w pamięci dwóch podsieci, które odwołują się do utworzonej grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="d9c84-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="d9c84-125">Następnie polecenie New-AzVirtualNetwork powoduje utworzenie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d9c84-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="d9c84-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9c84-126">PARAMETERS</span></span>

### <span data-ttu-id="d9c84-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d9c84-127">-AddressPrefix</span></span>
<span data-ttu-id="d9c84-128">Określa zakres adresów IP dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d9c84-128">Specifies a range of IP addresses for a virtual network.</span></span>

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

### <span data-ttu-id="d9c84-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9c84-129">-AsJob</span></span>
<span data-ttu-id="d9c84-130">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d9c84-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9c84-131">-BgpCommunity</span><span class="sxs-lookup"><span data-stu-id="d9c84-131">-BgpCommunity</span></span>
<span data-ttu-id="d9c84-132">Społeczność BGP zareklamował za pośrednictwem ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d9c84-132">The BGP Community advertised over ExpressRoute.</span></span>

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

### <span data-ttu-id="d9c84-133">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="d9c84-133">-DdosProtectionPlanId</span></span>
<span data-ttu-id="d9c84-134">Odwołanie do zasobu planu ochrony DDoS skojarzonego z siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="d9c84-134">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

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

### <span data-ttu-id="d9c84-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c84-135">-DefaultProfile</span></span>
<span data-ttu-id="d9c84-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9c84-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9c84-137">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="d9c84-137">-DnsServer</span></span>
<span data-ttu-id="d9c84-138">Określa serwer DNS dla podsieci.</span><span class="sxs-lookup"><span data-stu-id="d9c84-138">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="d9c84-139">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="d9c84-139">-EnableDdosProtection</span></span>
<span data-ttu-id="d9c84-140">Parametr przełącznika reprezentujący, czy włączono ochronę DDoS.</span><span class="sxs-lookup"><span data-stu-id="d9c84-140">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

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

### <span data-ttu-id="d9c84-141">-Force</span><span class="sxs-lookup"><span data-stu-id="d9c84-141">-Force</span></span>
<span data-ttu-id="d9c84-142">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d9c84-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9c84-143">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="d9c84-143">-IpAllocation</span></span>
<span data-ttu-id="d9c84-144">Określa IpAllocations dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d9c84-144">Specifies IpAllocations for a virtual network.</span></span>

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

### <span data-ttu-id="d9c84-145">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d9c84-145">-Location</span></span>
<span data-ttu-id="d9c84-146">Określa region sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d9c84-146">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="d9c84-147">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d9c84-147">-Name</span></span>
<span data-ttu-id="d9c84-148">Określa nazwę sieci wirtualnej, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9c84-148">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d9c84-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9c84-149">-ResourceGroupName</span></span>
<span data-ttu-id="d9c84-150">Określa nazwę grupy zasobów, która ma zawierać sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="d9c84-150">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="d9c84-151">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="d9c84-151">-Subnet</span></span>
<span data-ttu-id="d9c84-152">Określa listę podsieci, które mają być skojarzone z siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="d9c84-152">Specifies a list of subnets to associate with the virtual network.</span></span>

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

### <span data-ttu-id="d9c84-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="d9c84-153">-Tag</span></span>
<span data-ttu-id="d9c84-154">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d9c84-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d9c84-155">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="d9c84-155">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d9c84-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9c84-156">-Confirm</span></span>
<span data-ttu-id="d9c84-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9c84-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9c84-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9c84-158">-WhatIf</span></span>
<span data-ttu-id="d9c84-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9c84-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9c84-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d9c84-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9c84-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c84-161">CommonParameters</span></span>
<span data-ttu-id="d9c84-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9c84-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c84-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9c84-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c84-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9c84-164">INPUTS</span></span>

### <span data-ttu-id="d9c84-165">System. String</span><span class="sxs-lookup"><span data-stu-id="d9c84-165">System.String</span></span>

### <span data-ttu-id="d9c84-166">System. String []</span><span class="sxs-lookup"><span data-stu-id="d9c84-166">System.String[]</span></span>

### <span data-ttu-id="d9c84-167">Microsoft. Azure. Commands. Network. models. PSSubnet []</span><span class="sxs-lookup"><span data-stu-id="d9c84-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span></span>

### <span data-ttu-id="d9c84-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d9c84-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d9c84-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9c84-169">OUTPUTS</span></span>

### <span data-ttu-id="d9c84-170">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d9c84-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="d9c84-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9c84-171">NOTES</span></span>

## <span data-ttu-id="d9c84-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9c84-172">RELATED LINKS</span></span>

[<span data-ttu-id="d9c84-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d9c84-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="d9c84-174">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d9c84-174">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="d9c84-175">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d9c84-175">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="d9c84-176">Nowe — AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="d9c84-176">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)
