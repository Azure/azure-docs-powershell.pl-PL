---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: 14af257cf6c5d5e547f81b76fd82a910580b3790
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546688"
---
# <span data-ttu-id="301b2-101">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="301b2-101">New-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="301b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="301b2-102">SYNOPSIS</span></span>
<span data-ttu-id="301b2-103">Tworzy konfigurację reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="301b2-103">Creates a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="301b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="301b2-104">SYNTAX</span></span>

### <span data-ttu-id="301b2-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="301b2-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="301b2-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="301b2-106">SetByResourceId</span></span>
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="301b2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="301b2-107">DESCRIPTION</span></span>
<span data-ttu-id="301b2-108">Polecenie cmdlet **New-AzureRmNetworkSecurityRuleConfig** umożliwia utworzenie konfiguracji reguły zabezpieczeń sieci Azure dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="301b2-108">The **New-AzureRmNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="301b2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="301b2-109">EXAMPLES</span></span>

### <span data-ttu-id="301b2-110">1: Tworzenie reguły zabezpieczeń sieci zezwalającej na protokół RDP</span><span class="sxs-lookup"><span data-stu-id="301b2-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="301b2-111">To polecenie tworzy regułę zabezpieczeń pozwalającą na dostęp z Internetu do portu 3389</span><span class="sxs-lookup"><span data-stu-id="301b2-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="301b2-112">2: Tworzenie reguły zabezpieczeń sieci, która umożliwia HTTP</span><span class="sxs-lookup"><span data-stu-id="301b2-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="301b2-113">To polecenie tworzy regułę zabezpieczeń pozwalającą na dostęp z Internetu do portu 80</span><span class="sxs-lookup"><span data-stu-id="301b2-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="301b2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="301b2-114">PARAMETERS</span></span>

### <span data-ttu-id="301b2-115">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="301b2-115">-Access</span></span>
<span data-ttu-id="301b2-116">Określa, czy ruch sieciowy jest dozwolony, czy zabroniony.</span><span class="sxs-lookup"><span data-stu-id="301b2-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="301b2-117">Dopuszczalne wartości tego parametru to: Allow i Deny.</span><span class="sxs-lookup"><span data-stu-id="301b2-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="301b2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301b2-118">-DefaultProfile</span></span>
<span data-ttu-id="301b2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="301b2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="301b2-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="301b2-120">-Description</span></span>
<span data-ttu-id="301b2-121">Określa opis konfiguracji reguły zabezpieczeń sieci do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="301b2-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="301b2-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="301b2-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="301b2-123">Określa prefiks adresu docelowego.</span><span class="sxs-lookup"><span data-stu-id="301b2-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="301b2-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="301b2-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="301b2-125">Adres międzydomenowy (Classless indomain Routing)</span><span class="sxs-lookup"><span data-stu-id="301b2-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="301b2-126">Zakres docelowego adresu IP</span><span class="sxs-lookup"><span data-stu-id="301b2-126">A destination IP address range</span></span> 
- <span data-ttu-id="301b2-127">Znak wieloznaczny (\*), aby dopasować dowolny adres IP</span><span class="sxs-lookup"><span data-stu-id="301b2-127">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="301b2-128">Możesz korzystać ze znaczników, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="301b2-128">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="301b2-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="301b2-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="301b2-130">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe dla reguły.</span><span class="sxs-lookup"><span data-stu-id="301b2-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="301b2-131">Nie można go użyć z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="301b2-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="301b2-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="301b2-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="301b2-133">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe dla reguły.</span><span class="sxs-lookup"><span data-stu-id="301b2-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="301b2-134">Nie można go użyć z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="301b2-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="301b2-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="301b2-135">-DestinationPortRange</span></span>
<span data-ttu-id="301b2-136">Określa port docelowy lub zakres.</span><span class="sxs-lookup"><span data-stu-id="301b2-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="301b2-137">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="301b2-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="301b2-138">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="301b2-138">An integer</span></span>
- <span data-ttu-id="301b2-139">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="301b2-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="301b2-140">Znak wieloznaczny (\*), aby dopasować port</span><span class="sxs-lookup"><span data-stu-id="301b2-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="301b2-141">-Direction</span><span class="sxs-lookup"><span data-stu-id="301b2-141">-Direction</span></span>
<span data-ttu-id="301b2-142">Określa, czy reguła jest obliczana na ruch przychodzący lub wychodzący.</span><span class="sxs-lookup"><span data-stu-id="301b2-142">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="301b2-143">Dopuszczalne wartości tego parametru to: przychodzące i wychodzące.</span><span class="sxs-lookup"><span data-stu-id="301b2-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="301b2-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="301b2-144">-Name</span></span>
<span data-ttu-id="301b2-145">Określa nazwę konfiguracji reguł zabezpieczeń sieci, którą to polecenie cmdlet tworzy.</span><span class="sxs-lookup"><span data-stu-id="301b2-145">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="301b2-146">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="301b2-146">-Priority</span></span>
<span data-ttu-id="301b2-147">Określa priorytet konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="301b2-147">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="301b2-148">Dopuszczalne wartości tego parametru to: liczba całkowita między 100 a 4096.</span><span class="sxs-lookup"><span data-stu-id="301b2-148">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="301b2-149">Numer priorytetu musi być unikatowy dla każdej reguły w kolekcji.</span><span class="sxs-lookup"><span data-stu-id="301b2-149">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="301b2-150">Niższy numer priorytetu, wyższy priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="301b2-150">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="301b2-151">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="301b2-151">-Protocol</span></span>
<span data-ttu-id="301b2-152">Określa protokół sieciowy, którego dotyczy Nowa konfiguracja reguły.</span><span class="sxs-lookup"><span data-stu-id="301b2-152">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="301b2-153">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="301b2-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="301b2-154">Protokoł</span><span class="sxs-lookup"><span data-stu-id="301b2-154">Tcp</span></span>
- <span data-ttu-id="301b2-155">Obsługiwane</span><span class="sxs-lookup"><span data-stu-id="301b2-155">Udp</span></span>
- <span data-ttu-id="301b2-156">Symbol wieloznaczny (\*), aby dopasować oba te znaki.</span><span class="sxs-lookup"><span data-stu-id="301b2-156">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="301b2-157">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="301b2-157">-SourceAddressPrefix</span></span>
<span data-ttu-id="301b2-158">Określa prefiks adresu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="301b2-158">Specifies a source address prefix.</span></span>
<span data-ttu-id="301b2-159">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="301b2-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="301b2-160">CIDR</span><span class="sxs-lookup"><span data-stu-id="301b2-160">A CIDR</span></span>
- <span data-ttu-id="301b2-161">Zakres źródłowy adresu IP</span><span class="sxs-lookup"><span data-stu-id="301b2-161">A source IP range</span></span>
- <span data-ttu-id="301b2-162">Znak wieloznaczny (\*), aby dopasować dowolny adres IP.</span><span class="sxs-lookup"><span data-stu-id="301b2-162">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="301b2-163">Możesz również korzystać ze znaczników, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="301b2-163">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="301b2-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="301b2-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="301b2-165">Grupa zabezpieczeń aplikacji ustawiona jako źródło dla reguły.</span><span class="sxs-lookup"><span data-stu-id="301b2-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="301b2-166">Nie można go użyć z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="301b2-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="301b2-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="301b2-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="301b2-168">Grupa zabezpieczeń aplikacji ustawiona jako źródło dla reguły.</span><span class="sxs-lookup"><span data-stu-id="301b2-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="301b2-169">Nie można go użyć z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="301b2-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="301b2-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="301b2-170">-SourcePortRange</span></span>
<span data-ttu-id="301b2-171">Określa port źródłowy lub zakres.</span><span class="sxs-lookup"><span data-stu-id="301b2-171">Specifies the source port or range.</span></span>
<span data-ttu-id="301b2-172">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="301b2-172">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="301b2-173">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="301b2-173">An integer</span></span>
- <span data-ttu-id="301b2-174">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="301b2-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="301b2-175">Znak wieloznaczny (\*), aby dopasować port</span><span class="sxs-lookup"><span data-stu-id="301b2-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="301b2-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301b2-176">CommonParameters</span></span>
<span data-ttu-id="301b2-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="301b2-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="301b2-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="301b2-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301b2-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="301b2-179">INPUTS</span></span>

### <span data-ttu-id="301b2-180">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="301b2-180">None</span></span>
<span data-ttu-id="301b2-181">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="301b2-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="301b2-182">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="301b2-182">OUTPUTS</span></span>

### <span data-ttu-id="301b2-183">Microsoft. Azure. Commands. Network. models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="301b2-183">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="301b2-184">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="301b2-184">NOTES</span></span>

## <span data-ttu-id="301b2-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="301b2-185">RELATED LINKS</span></span>

[<span data-ttu-id="301b2-186">Dodaj-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="301b2-186">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="301b2-187">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="301b2-187">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="301b2-188">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="301b2-188">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="301b2-189">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="301b2-189">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


