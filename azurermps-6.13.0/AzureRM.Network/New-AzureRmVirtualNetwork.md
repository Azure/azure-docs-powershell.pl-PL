---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
ms.openlocfilehash: 9c52a5f234b374612b07d53b21ac9409a45cc35a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717617"
---
# <span data-ttu-id="195a7-101">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="195a7-101">New-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="195a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="195a7-102">SYNOPSIS</span></span>
<span data-ttu-id="195a7-103">Tworzy sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="195a7-103">Creates a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="195a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="195a7-104">SYNTAX</span></span>

```
New-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-Subnet <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]>]
 [-Tag <Hashtable>] [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-EnableVmProtection] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="195a7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="195a7-105">DESCRIPTION</span></span>
<span data-ttu-id="195a7-106">Polecenie cmdlet **New-AzureRmVirtualNetwork** umożliwia utworzenie wirtualnej sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="195a7-106">The **New-AzureRmVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="195a7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="195a7-107">EXAMPLES</span></span>

### <span data-ttu-id="195a7-108">1: tworzenie sieci wirtualnej z dwiema podsieciami</span><span class="sxs-lookup"><span data-stu-id="195a7-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="195a7-109">W tym przykładzie przedstawiono tworzenie sieci wirtualnej z dwiema podsieciami.</span><span class="sxs-lookup"><span data-stu-id="195a7-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="195a7-110">Najpierw zostanie utworzona nowa grupa zasobów w regionie centralnym.</span><span class="sxs-lookup"><span data-stu-id="195a7-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="195a7-111">Następnie w przykładzie tworzone są reprezentacje w pamięci dwóch podsieci.</span><span class="sxs-lookup"><span data-stu-id="195a7-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="195a7-112">Polecenie cmdlet New-AzureRmVirtualNetworkSubnetConfig nie powoduje utworzenia żadnej podsieci po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="195a7-112">The New-AzureRmVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="195a7-113">Istnieje jedna podsieć o nazwie frontendSubnet i jedna podsieć o nazwie backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="195a7-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="195a7-114">Polecenie cmdlet New-AzureRmVirtualNetwork powoduje utworzenie sieci wirtualnej przy użyciu notacji CIDR 10.0.0.0/16 jako prefiksu adresu i dwóch podsieci.</span><span class="sxs-lookup"><span data-stu-id="195a7-114">The New-AzureRmVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="195a7-115">2: tworzenie sieci wirtualnej przy użyciu ustawień DNS</span><span class="sxs-lookup"><span data-stu-id="195a7-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="195a7-116">W tym przykładzie przedstawiono tworzenie sieci wirtualnej z dwiema podsieciami i dwoma serwerami DNS.</span><span class="sxs-lookup"><span data-stu-id="195a7-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="195a7-117">Efektem określenia serwerów DNS w sieci wirtualnej jest to, że karty sieciowe/maszyny wirtualne rozmieszczone w tej sieci wirtualnej będą dziedziczyć te serwery DNS jako domyślne.</span><span class="sxs-lookup"><span data-stu-id="195a7-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="195a7-118">Te wartości domyślne można przełączać na kartę sieciową za pośrednictwem ustawienia na poziomie karty NIC.</span><span class="sxs-lookup"><span data-stu-id="195a7-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="195a7-119">Jeśli w sieci wirtualnej nie są określone serwery DNS ani serwery DNS na kartach sieciowych, to w celu rozpoznawania nazw DNS są używane domyślne serwery DNS platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="195a7-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="195a7-120">3: tworzenie sieci wirtualnej z podsiecią, do której należy odwołanie do grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="195a7-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="195a7-121">W tym przykładzie jest tworzona Sieć wirtualna z podsieciami, które odwołują się do grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="195a7-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="195a7-122">Najpierw w przykładzie tworzona jest Grupa zasobów jako kontener dla zasobów, które zostaną utworzone.</span><span class="sxs-lookup"><span data-stu-id="195a7-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="195a7-123">Następnie zostanie utworzona grupa zabezpieczeń sieci umożliwiająca przychodzący dostęp do protokołu RDP, ale w przeciwnym razie wymusza domyślne reguły grupowych zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="195a7-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="195a7-124">Polecenie cmdlet New-AzureRmVirtualNetworkSubnetConfig powoduje utworzenie reprezentacji w pamięci dwóch podsieci, które odwołują się do utworzonej grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="195a7-124">The New-AzureRmVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="195a7-125">Następnie polecenie New-AzureRmVirtualNetwork powoduje utworzenie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="195a7-125">The New-AzureRmVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="195a7-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="195a7-126">PARAMETERS</span></span>

### <span data-ttu-id="195a7-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="195a7-127">-AddressPrefix</span></span>
<span data-ttu-id="195a7-128">Określa zakres adresów IP dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="195a7-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="195a7-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="195a7-129">-AsJob</span></span>
<span data-ttu-id="195a7-130">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="195a7-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="195a7-131">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="195a7-131">-DdosProtectionPlanId</span></span>
<span data-ttu-id="195a7-132">Odwołanie do zasobu planu ochrony DDoS skojarzonego z siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="195a7-132">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

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

### <span data-ttu-id="195a7-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="195a7-133">-DefaultProfile</span></span>
<span data-ttu-id="195a7-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="195a7-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="195a7-135">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="195a7-135">-DnsServer</span></span>
<span data-ttu-id="195a7-136">Określa serwer DNS dla podsieci.</span><span class="sxs-lookup"><span data-stu-id="195a7-136">Specifies the DNS server for a subnet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="195a7-137">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="195a7-137">-EnableDdosProtection</span></span>
<span data-ttu-id="195a7-138">Parametr przełącznika reprezentujący, czy włączono ochronę DDoS.</span><span class="sxs-lookup"><span data-stu-id="195a7-138">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

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

### <span data-ttu-id="195a7-139">-EnableVmProtection</span><span class="sxs-lookup"><span data-stu-id="195a7-139">-EnableVmProtection</span></span>
<span data-ttu-id="195a7-140">Parametr przełącznika reprezentujący, czy włączono ochronę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="195a7-140">A switch parameter which represents if Vm protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="195a7-141">-Force</span><span class="sxs-lookup"><span data-stu-id="195a7-141">-Force</span></span>
<span data-ttu-id="195a7-142">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="195a7-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="195a7-143">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="195a7-143">-Location</span></span>
<span data-ttu-id="195a7-144">Określa region sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="195a7-144">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="195a7-145">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="195a7-145">-Name</span></span>
<span data-ttu-id="195a7-146">Określa nazwę sieci wirtualnej, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="195a7-146">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="195a7-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="195a7-147">-ResourceGroupName</span></span>
<span data-ttu-id="195a7-148">Określa nazwę grupy zasobów, która ma zawierać sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="195a7-148">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="195a7-149">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="195a7-149">-Subnet</span></span>
<span data-ttu-id="195a7-150">Określa listę podsieci, które mają być skojarzone z siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="195a7-150">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="195a7-151">-Tag</span><span class="sxs-lookup"><span data-stu-id="195a7-151">-Tag</span></span>
<span data-ttu-id="195a7-152">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="195a7-152">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="195a7-153">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="195a7-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="195a7-154">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="195a7-154">-Confirm</span></span>
<span data-ttu-id="195a7-155">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="195a7-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="195a7-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="195a7-156">-WhatIf</span></span>
<span data-ttu-id="195a7-157">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="195a7-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="195a7-158">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="195a7-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="195a7-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="195a7-159">CommonParameters</span></span>
<span data-ttu-id="195a7-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="195a7-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="195a7-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="195a7-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="195a7-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="195a7-162">INPUTS</span></span>

### <span data-ttu-id="195a7-163">System. String</span><span class="sxs-lookup"><span data-stu-id="195a7-163">System.String</span></span>

### <span data-ttu-id="195a7-164">System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="195a7-164">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="195a7-165">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSSubnet; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="195a7-165">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSSubnet, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="195a7-166">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="195a7-166">System.Collections.Hashtable</span></span>

### <span data-ttu-id="195a7-167">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="195a7-167">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="195a7-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="195a7-168">OUTPUTS</span></span>

### <span data-ttu-id="195a7-169">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="195a7-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="195a7-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="195a7-170">NOTES</span></span>

## <span data-ttu-id="195a7-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="195a7-171">RELATED LINKS</span></span>

[<span data-ttu-id="195a7-172">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="195a7-172">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="195a7-173">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="195a7-173">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="195a7-174">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="195a7-174">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="195a7-175">Nowe — AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="195a7-175">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)
