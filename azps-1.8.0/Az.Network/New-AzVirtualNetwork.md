---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: 0b839d0392153fc21b9d57c15a823158827bdc72
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709230"
---
# <span data-ttu-id="4077c-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4077c-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="4077c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4077c-102">SYNOPSIS</span></span>
<span data-ttu-id="4077c-103">Tworzy sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="4077c-103">Creates a virtual network.</span></span>

## <span data-ttu-id="4077c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4077c-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-Tag <Hashtable>] [-EnableDdosProtection]
 [-DdosProtectionPlanId <String>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4077c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4077c-105">DESCRIPTION</span></span>
<span data-ttu-id="4077c-106">Polecenie cmdlet **New-AzVirtualNetwork** umożliwia utworzenie wirtualnej sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="4077c-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="4077c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4077c-107">EXAMPLES</span></span>

### <span data-ttu-id="4077c-108">1: tworzenie sieci wirtualnej z dwiema podsieciami</span><span class="sxs-lookup"><span data-stu-id="4077c-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="4077c-109">W tym przykładzie przedstawiono tworzenie sieci wirtualnej z dwiema podsieciami.</span><span class="sxs-lookup"><span data-stu-id="4077c-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="4077c-110">Najpierw zostanie utworzona nowa grupa zasobów w regionie centralnym.</span><span class="sxs-lookup"><span data-stu-id="4077c-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="4077c-111">Następnie w przykładzie tworzone są reprezentacje w pamięci dwóch podsieci.</span><span class="sxs-lookup"><span data-stu-id="4077c-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="4077c-112">Polecenie cmdlet New-AzVirtualNetworkSubnetConfig nie powoduje utworzenia żadnej podsieci po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="4077c-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="4077c-113">Istnieje jedna podsieć o nazwie frontendSubnet i jedna podsieć o nazwie backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="4077c-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="4077c-114">Polecenie cmdlet New-AzVirtualNetwork powoduje utworzenie sieci wirtualnej przy użyciu notacji CIDR 10.0.0.0/16 jako prefiksu adresu i dwóch podsieci.</span><span class="sxs-lookup"><span data-stu-id="4077c-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="4077c-115">2: tworzenie sieci wirtualnej przy użyciu ustawień DNS</span><span class="sxs-lookup"><span data-stu-id="4077c-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="4077c-116">W tym przykładzie przedstawiono tworzenie sieci wirtualnej z dwiema podsieciami i dwoma serwerami DNS.</span><span class="sxs-lookup"><span data-stu-id="4077c-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="4077c-117">Efektem określenia serwerów DNS w sieci wirtualnej jest to, że karty sieciowe/maszyny wirtualne rozmieszczone w tej sieci wirtualnej będą dziedziczyć te serwery DNS jako domyślne.</span><span class="sxs-lookup"><span data-stu-id="4077c-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="4077c-118">Te wartości domyślne można przełączać na kartę sieciową za pośrednictwem ustawienia na poziomie karty NIC.</span><span class="sxs-lookup"><span data-stu-id="4077c-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="4077c-119">Jeśli w sieci wirtualnej nie są określone serwery DNS ani serwery DNS na kartach sieciowych, to w celu rozpoznawania nazw DNS są używane domyślne serwery DNS platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4077c-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="4077c-120">3: tworzenie sieci wirtualnej z podsiecią, do której należy odwołanie do grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="4077c-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="4077c-121">W tym przykładzie jest tworzona Sieć wirtualna z podsieciami, które odwołują się do grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="4077c-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="4077c-122">Najpierw w przykładzie tworzona jest Grupa zasobów jako kontener dla zasobów, które zostaną utworzone.</span><span class="sxs-lookup"><span data-stu-id="4077c-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="4077c-123">Następnie zostanie utworzona grupa zabezpieczeń sieci umożliwiająca przychodzący dostęp do protokołu RDP, ale w przeciwnym razie wymusza domyślne reguły grupowych zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="4077c-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="4077c-124">Polecenie cmdlet New-AzVirtualNetworkSubnetConfig powoduje utworzenie reprezentacji w pamięci dwóch podsieci, które odwołują się do utworzonej grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="4077c-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="4077c-125">Następnie polecenie New-AzVirtualNetwork powoduje utworzenie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4077c-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="4077c-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4077c-126">PARAMETERS</span></span>

### <span data-ttu-id="4077c-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4077c-127">-AddressPrefix</span></span>
<span data-ttu-id="4077c-128">Określa zakres adresów IP dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4077c-128">Specifies a range of IP addresses for a virtual network.</span></span>

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

### <span data-ttu-id="4077c-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4077c-129">-AsJob</span></span>
<span data-ttu-id="4077c-130">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4077c-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4077c-131">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="4077c-131">-DdosProtectionPlanId</span></span>
<span data-ttu-id="4077c-132">Odwołanie do zasobu planu ochrony DDoS skojarzonego z siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="4077c-132">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

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

### <span data-ttu-id="4077c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4077c-133">-DefaultProfile</span></span>
<span data-ttu-id="4077c-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4077c-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4077c-135">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="4077c-135">-DnsServer</span></span>
<span data-ttu-id="4077c-136">Określa serwer DNS dla podsieci.</span><span class="sxs-lookup"><span data-stu-id="4077c-136">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="4077c-137">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="4077c-137">-EnableDdosProtection</span></span>
<span data-ttu-id="4077c-138">Parametr przełącznika reprezentujący, czy włączono ochronę DDoS.</span><span class="sxs-lookup"><span data-stu-id="4077c-138">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

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

### <span data-ttu-id="4077c-139">-Force</span><span class="sxs-lookup"><span data-stu-id="4077c-139">-Force</span></span>
<span data-ttu-id="4077c-140">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4077c-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4077c-141">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4077c-141">-Location</span></span>
<span data-ttu-id="4077c-142">Określa region sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4077c-142">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="4077c-143">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4077c-143">-Name</span></span>
<span data-ttu-id="4077c-144">Określa nazwę sieci wirtualnej, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4077c-144">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4077c-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4077c-145">-ResourceGroupName</span></span>
<span data-ttu-id="4077c-146">Określa nazwę grupy zasobów, która ma zawierać sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="4077c-146">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="4077c-147">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="4077c-147">-Subnet</span></span>
<span data-ttu-id="4077c-148">Określa listę podsieci, które mają być skojarzone z siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="4077c-148">Specifies a list of subnets to associate with the virtual network.</span></span>

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

### <span data-ttu-id="4077c-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="4077c-149">-Tag</span></span>
<span data-ttu-id="4077c-150">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4077c-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4077c-151">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="4077c-151">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4077c-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4077c-152">-Confirm</span></span>
<span data-ttu-id="4077c-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4077c-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4077c-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4077c-154">-WhatIf</span></span>
<span data-ttu-id="4077c-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4077c-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4077c-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4077c-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4077c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4077c-157">CommonParameters</span></span>
<span data-ttu-id="4077c-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4077c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4077c-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4077c-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4077c-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4077c-160">INPUTS</span></span>

### <span data-ttu-id="4077c-161">System. String</span><span class="sxs-lookup"><span data-stu-id="4077c-161">System.String</span></span>

### <span data-ttu-id="4077c-162">System. String []</span><span class="sxs-lookup"><span data-stu-id="4077c-162">System.String[]</span></span>

### <span data-ttu-id="4077c-163">Microsoft. Azure. Commands. Network. models. PSSubnet []</span><span class="sxs-lookup"><span data-stu-id="4077c-163">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span></span>

### <span data-ttu-id="4077c-164">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4077c-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4077c-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4077c-165">OUTPUTS</span></span>

### <span data-ttu-id="4077c-166">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4077c-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4077c-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4077c-167">NOTES</span></span>

## <span data-ttu-id="4077c-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4077c-168">RELATED LINKS</span></span>

[<span data-ttu-id="4077c-169">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4077c-169">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="4077c-170">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4077c-170">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="4077c-171">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4077c-171">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="4077c-172">Nowe — AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="4077c-172">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)