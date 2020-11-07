---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 17e73f28595a0b99c8209634a6dee6838fa4599d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890462"
---
# <span data-ttu-id="d1bdc-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1bdc-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="d1bdc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d1bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="d1bdc-103">Tworzy konfigurację reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="d1bdc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d1bdc-104">SYNTAX</span></span>

### <span data-ttu-id="d1bdc-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d1bdc-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1bdc-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d1bdc-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1bdc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d1bdc-107">DESCRIPTION</span></span>
<span data-ttu-id="d1bdc-108">Polecenie cmdlet **New-AzNetworkSecurityRuleConfig** umożliwia utworzenie konfiguracji reguły zabezpieczeń sieci Azure dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="d1bdc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d1bdc-109">EXAMPLES</span></span>

### <span data-ttu-id="d1bdc-110">1: Tworzenie reguły zabezpieczeń sieci zezwalającej na protokół RDP</span><span class="sxs-lookup"><span data-stu-id="d1bdc-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="d1bdc-111">To polecenie tworzy regułę zabezpieczeń pozwalającą na dostęp z Internetu do portu 3389</span><span class="sxs-lookup"><span data-stu-id="d1bdc-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="d1bdc-112">2: Tworzenie reguły zabezpieczeń sieci, która umożliwia HTTP</span><span class="sxs-lookup"><span data-stu-id="d1bdc-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="d1bdc-113">To polecenie tworzy regułę zabezpieczeń pozwalającą na dostęp z Internetu do portu 80</span><span class="sxs-lookup"><span data-stu-id="d1bdc-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="d1bdc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1bdc-114">PARAMETERS</span></span>

### <span data-ttu-id="d1bdc-115">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="d1bdc-115">-Access</span></span>
<span data-ttu-id="d1bdc-116">Określa, czy ruch sieciowy jest dozwolony, czy zabroniony.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="d1bdc-117">Dopuszczalne wartości tego parametru to: Allow i Deny.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1bdc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1bdc-118">-DefaultProfile</span></span>
<span data-ttu-id="d1bdc-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1bdc-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="d1bdc-120">-Description</span></span>
<span data-ttu-id="d1bdc-121">Określa opis konfiguracji reguły zabezpieczeń sieci do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="d1bdc-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d1bdc-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="d1bdc-123">Określa prefiks adresu docelowego.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="d1bdc-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d1bdc-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1bdc-125">Adres międzydomenowy (Classless indomain Routing)</span><span class="sxs-lookup"><span data-stu-id="d1bdc-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="d1bdc-126">Zakres docelowego adresu IP</span><span class="sxs-lookup"><span data-stu-id="d1bdc-126">A destination IP address range</span></span> 
- <span data-ttu-id="d1bdc-127">Znak wieloznaczny (\*), aby dopasować dowolny adres IP</span><span class="sxs-lookup"><span data-stu-id="d1bdc-127">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="d1bdc-128">Możesz korzystać ze znaczników, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-128">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="d1bdc-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d1bdc-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="d1bdc-130">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe dla reguły.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="d1bdc-131">Nie można go użyć z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="d1bdc-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1bdc-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d1bdc-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="d1bdc-133">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe dla reguły.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="d1bdc-134">Nie można go użyć z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="d1bdc-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1bdc-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="d1bdc-135">-DestinationPortRange</span></span>
<span data-ttu-id="d1bdc-136">Określa port docelowy lub zakres.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="d1bdc-137">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d1bdc-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1bdc-138">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="d1bdc-138">An integer</span></span>
- <span data-ttu-id="d1bdc-139">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="d1bdc-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="d1bdc-140">Znak wieloznaczny (\*), aby dopasować port</span><span class="sxs-lookup"><span data-stu-id="d1bdc-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="d1bdc-141">-Direction</span><span class="sxs-lookup"><span data-stu-id="d1bdc-141">-Direction</span></span>
<span data-ttu-id="d1bdc-142">Określa, czy reguła jest obliczana na ruch przychodzący lub wychodzący.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-142">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="d1bdc-143">Dopuszczalne wartości tego parametru to: przychodzące i wychodzące.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1bdc-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d1bdc-144">-Name</span></span>
<span data-ttu-id="d1bdc-145">Określa nazwę konfiguracji reguł zabezpieczeń sieci, którą to polecenie cmdlet tworzy.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-145">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d1bdc-146">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="d1bdc-146">-Priority</span></span>
<span data-ttu-id="d1bdc-147">Określa priorytet konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-147">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="d1bdc-148">Dopuszczalne wartości tego parametru to: liczba całkowita między 100 a 4096.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-148">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="d1bdc-149">Numer priorytetu musi być unikatowy dla każdej reguły w kolekcji.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-149">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="d1bdc-150">Niższy numer priorytetu, wyższy priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-150">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="d1bdc-151">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="d1bdc-151">-Protocol</span></span>
<span data-ttu-id="d1bdc-152">Określa protokół sieciowy, którego dotyczy Nowa konfiguracja reguły.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-152">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="d1bdc-153">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d1bdc-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1bdc-154">Protokoł</span><span class="sxs-lookup"><span data-stu-id="d1bdc-154">Tcp</span></span>
- <span data-ttu-id="d1bdc-155">Obsługiwane</span><span class="sxs-lookup"><span data-stu-id="d1bdc-155">Udp</span></span>
- <span data-ttu-id="d1bdc-156">Symbol wieloznaczny (\*), aby dopasować oba te znaki.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-156">wildcard character (\*) to match both.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1bdc-157">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d1bdc-157">-SourceAddressPrefix</span></span>
<span data-ttu-id="d1bdc-158">Określa prefiks adresu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-158">Specifies a source address prefix.</span></span>
<span data-ttu-id="d1bdc-159">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d1bdc-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1bdc-160">CIDR</span><span class="sxs-lookup"><span data-stu-id="d1bdc-160">A CIDR</span></span>
- <span data-ttu-id="d1bdc-161">Zakres źródłowy adresu IP</span><span class="sxs-lookup"><span data-stu-id="d1bdc-161">A source IP range</span></span>
- <span data-ttu-id="d1bdc-162">Znak wieloznaczny (\*), aby dopasować dowolny adres IP.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-162">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="d1bdc-163">Możesz również korzystać ze znaczników, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-163">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="d1bdc-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d1bdc-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="d1bdc-165">Grupa zabezpieczeń aplikacji ustawiona jako źródło dla reguły.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="d1bdc-166">Nie można go użyć z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="d1bdc-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1bdc-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d1bdc-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="d1bdc-168">Grupa zabezpieczeń aplikacji ustawiona jako źródło dla reguły.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="d1bdc-169">Nie można go użyć z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="d1bdc-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1bdc-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="d1bdc-170">-SourcePortRange</span></span>
<span data-ttu-id="d1bdc-171">Określa port źródłowy lub zakres.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-171">Specifies the source port or range.</span></span>
<span data-ttu-id="d1bdc-172">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d1bdc-172">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1bdc-173">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="d1bdc-173">An integer</span></span>
- <span data-ttu-id="d1bdc-174">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="d1bdc-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="d1bdc-175">Znak wieloznaczny (\*), aby dopasować port</span><span class="sxs-lookup"><span data-stu-id="d1bdc-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="d1bdc-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1bdc-176">CommonParameters</span></span>
<span data-ttu-id="d1bdc-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1bdc-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1bdc-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1bdc-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1bdc-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1bdc-179">INPUTS</span></span>

## <span data-ttu-id="d1bdc-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d1bdc-180">OUTPUTS</span></span>

### <span data-ttu-id="d1bdc-181">Microsoft. Azure. Commands. Network. models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="d1bdc-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="d1bdc-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d1bdc-182">NOTES</span></span>

## <span data-ttu-id="d1bdc-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1bdc-183">RELATED LINKS</span></span>

[<span data-ttu-id="d1bdc-184">Dodaj-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1bdc-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="d1bdc-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1bdc-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="d1bdc-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1bdc-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="d1bdc-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1bdc-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


