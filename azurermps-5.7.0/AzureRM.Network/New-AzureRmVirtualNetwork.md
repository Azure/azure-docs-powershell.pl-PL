---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
ms.openlocfilehash: b7dc6c405ae1a5a213cedcb4b9737ff23dcf2b36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718044"
---
# <span data-ttu-id="7a60b-101">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7a60b-101">New-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="7a60b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a60b-102">SYNOPSIS</span></span>
<span data-ttu-id="7a60b-103">Tworzy sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="7a60b-103">Creates a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a60b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a60b-104">SYNTAX</span></span>

```
New-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-Subnet <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]>]
 [-Tag <Hashtable>] [-EnableDDoSProtection] [-EnableVmProtection] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a60b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7a60b-105">DESCRIPTION</span></span>
<span data-ttu-id="7a60b-106">Polecenie cmdlet **New-AzureRmVirtualNetwork** umożliwia utworzenie wirtualnej sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="7a60b-106">The **New-AzureRmVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="7a60b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a60b-107">EXAMPLES</span></span>

### <span data-ttu-id="7a60b-108">1: tworzenie sieci wirtualnej z dwiema podsieciami</span><span class="sxs-lookup"><span data-stu-id="7a60b-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="7a60b-109">W tym przykładzie przedstawiono tworzenie sieci wirtualnej z dwiema podsieciami.</span><span class="sxs-lookup"><span data-stu-id="7a60b-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="7a60b-110">Najpierw zostanie utworzona nowa grupa zasobów w regionie centralnym.</span><span class="sxs-lookup"><span data-stu-id="7a60b-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="7a60b-111">Następnie w przykładzie tworzone są reprezentacje w pamięci dwóch podsieci.</span><span class="sxs-lookup"><span data-stu-id="7a60b-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="7a60b-112">Polecenie cmdlet New-AzureRmVirtualNetworkSubnetConfig nie powoduje utworzenia żadnej podsieci po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="7a60b-112">The New-AzureRmVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="7a60b-113">Istnieje jedna podsieć o nazwie frontendSubnet i jedna podsieć o nazwie backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="7a60b-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="7a60b-114">Polecenie cmdlet New-AzureRmVirtualNetwork powoduje utworzenie sieci wirtualnej przy użyciu notacji CIDR 10.0.0.0/16 jako prefiksu adresu i dwóch podsieci.</span><span class="sxs-lookup"><span data-stu-id="7a60b-114">The New-AzureRmVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="7a60b-115">2: tworzenie sieci wirtualnej przy użyciu ustawień DNS</span><span class="sxs-lookup"><span data-stu-id="7a60b-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="7a60b-116">W tym przykładzie przedstawiono tworzenie sieci wirtualnej z dwiema podsieciami i dwoma serwerami DNS.</span><span class="sxs-lookup"><span data-stu-id="7a60b-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="7a60b-117">Efektem określenia serwerów DNS w sieci wirtualnej jest to, że karty sieciowe/maszyny wirtualne rozmieszczone w tej sieci wirtualnej będą dziedziczyć te serwery DNS jako domyślne.</span><span class="sxs-lookup"><span data-stu-id="7a60b-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="7a60b-118">Te wartości domyślne można przełączać na kartę sieciową za pośrednictwem ustawienia na poziomie karty NIC.</span><span class="sxs-lookup"><span data-stu-id="7a60b-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="7a60b-119">Jeśli w sieci wirtualnej nie są określone serwery DNS ani serwery DNS na kartach sieciowych, to w celu rozpoznawania nazw DNS są używane domyślne serwery DNS platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7a60b-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="7a60b-120">3: tworzenie sieci wirtualnej z podsiecią, do której należy odwołanie do grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="7a60b-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="7a60b-121">W tym przykładzie jest tworzona Sieć wirtualna z podsieciami, które odwołują się do grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="7a60b-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="7a60b-122">Najpierw w przykładzie tworzona jest Grupa zasobów jako kontener dla zasobów, które zostaną utworzone.</span><span class="sxs-lookup"><span data-stu-id="7a60b-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="7a60b-123">Następnie zostanie utworzona grupa zabezpieczeń sieci umożliwiająca przychodzący dostęp do protokołu RDP, ale w przeciwnym razie wymusza domyślne reguły grupowych zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="7a60b-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="7a60b-124">Polecenie cmdlet New-AzureRmVirtualNetworkSubnetConfig powoduje utworzenie reprezentacji w pamięci dwóch podsieci, które odwołują się do utworzonej grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="7a60b-124">The New-AzureRmVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="7a60b-125">Następnie polecenie New-AzureRmVirtualNetwork powoduje utworzenie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7a60b-125">The New-AzureRmVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="7a60b-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a60b-126">PARAMETERS</span></span>

### <span data-ttu-id="7a60b-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7a60b-127">-AddressPrefix</span></span>
<span data-ttu-id="7a60b-128">Określa zakres adresów IP dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7a60b-128">Specifies a range of IP addresses for a virtual network.</span></span>

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

### <span data-ttu-id="7a60b-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a60b-129">-AsJob</span></span>
<span data-ttu-id="7a60b-130">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7a60b-130">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a60b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a60b-131">-DefaultProfile</span></span>
<span data-ttu-id="7a60b-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a60b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a60b-133">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="7a60b-133">-DnsServer</span></span>
<span data-ttu-id="7a60b-134">Określa serwer DNS dla podsieci.</span><span class="sxs-lookup"><span data-stu-id="7a60b-134">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="7a60b-135">-EnableDDoSProtection</span><span class="sxs-lookup"><span data-stu-id="7a60b-135">-EnableDDoSProtection</span></span>
<span data-ttu-id="7a60b-136">Parametr przełącznika reprezentujący, czy włączono ochronę DDoS.</span><span class="sxs-lookup"><span data-stu-id="7a60b-136">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a60b-137">-EnableVmProtection</span><span class="sxs-lookup"><span data-stu-id="7a60b-137">-EnableVmProtection</span></span>
<span data-ttu-id="7a60b-138">Parametr przełącznika reprezentujący, czy włączono ochronę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7a60b-138">A switch parameter which represents if Vm protection is enabled or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a60b-139">-Force</span><span class="sxs-lookup"><span data-stu-id="7a60b-139">-Force</span></span>
<span data-ttu-id="7a60b-140">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7a60b-140">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a60b-141">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7a60b-141">-Location</span></span>
<span data-ttu-id="7a60b-142">Określa region sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7a60b-142">Specifies the region for the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a60b-143">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7a60b-143">-Name</span></span>
<span data-ttu-id="7a60b-144">Określa nazwę sieci wirtualnej, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a60b-144">Specifies the name of the virtual network that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a60b-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a60b-145">-ResourceGroupName</span></span>
<span data-ttu-id="7a60b-146">Określa nazwę grupy zasobów, która ma zawierać sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="7a60b-146">Specifies the name of a resource group to contain the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a60b-147">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="7a60b-147">-Subnet</span></span>
<span data-ttu-id="7a60b-148">Określa listę podsieci, które mają być skojarzone z siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="7a60b-148">Specifies a list of subnets to associate with the virtual network.</span></span>

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

### <span data-ttu-id="7a60b-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="7a60b-149">-Tag</span></span>
<span data-ttu-id="7a60b-150">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7a60b-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7a60b-151">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="7a60b-151">For example:</span></span>

<span data-ttu-id="7a60b-152">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="7a60b-152">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a60b-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a60b-153">-Confirm</span></span>
<span data-ttu-id="7a60b-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a60b-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a60b-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a60b-155">-WhatIf</span></span>
<span data-ttu-id="7a60b-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a60b-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a60b-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7a60b-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a60b-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a60b-158">CommonParameters</span></span>
<span data-ttu-id="7a60b-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a60b-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a60b-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a60b-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a60b-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a60b-161">INPUTS</span></span>

### <span data-ttu-id="7a60b-162">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7a60b-162">None</span></span>
<span data-ttu-id="7a60b-163">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7a60b-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7a60b-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a60b-164">OUTPUTS</span></span>

### <span data-ttu-id="7a60b-165">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7a60b-165">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="7a60b-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a60b-166">NOTES</span></span>

## <span data-ttu-id="7a60b-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a60b-167">RELATED LINKS</span></span>

[<span data-ttu-id="7a60b-168">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7a60b-168">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="7a60b-169">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7a60b-169">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="7a60b-170">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7a60b-170">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)
