---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: 0950e09185783f0b352defafb7673a2f97461c74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554062"
---
# <span data-ttu-id="ba233-101">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba233-101">New-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="ba233-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba233-102">SYNOPSIS</span></span>
<span data-ttu-id="ba233-103">Tworzy konfigurację reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="ba233-103">Creates a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba233-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba233-104">SYNTAX</span></span>

### <span data-ttu-id="ba233-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ba233-105">SetByResource (Default)</span></span>
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

### <span data-ttu-id="ba233-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ba233-106">SetByResourceId</span></span>
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

## <span data-ttu-id="ba233-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ba233-107">DESCRIPTION</span></span>
<span data-ttu-id="ba233-108">Polecenie cmdlet **New-AzureRmNetworkSecurityRuleConfig** umożliwia utworzenie konfiguracji reguły zabezpieczeń sieci Azure dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="ba233-108">The **New-AzureRmNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="ba233-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba233-109">EXAMPLES</span></span>

### <span data-ttu-id="ba233-110">1: Tworzenie reguły zabezpieczeń sieci zezwalającej na protokół RDP</span><span class="sxs-lookup"><span data-stu-id="ba233-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="ba233-111">To polecenie tworzy regułę zabezpieczeń pozwalającą na dostęp z Internetu do portu 3389</span><span class="sxs-lookup"><span data-stu-id="ba233-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="ba233-112">2: Tworzenie reguły zabezpieczeń sieci, która umożliwia HTTP</span><span class="sxs-lookup"><span data-stu-id="ba233-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="ba233-113">To polecenie tworzy regułę zabezpieczeń pozwalającą na dostęp z Internetu do portu 80</span><span class="sxs-lookup"><span data-stu-id="ba233-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="ba233-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba233-114">PARAMETERS</span></span>

### <span data-ttu-id="ba233-115">— Dostęp</span><span class="sxs-lookup"><span data-stu-id="ba233-115">-Access</span></span>
<span data-ttu-id="ba233-116">Określa, czy ruch sieciowy jest dozwolony, czy zabroniony.</span><span class="sxs-lookup"><span data-stu-id="ba233-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="ba233-117">Dopuszczalne wartości tego parametru to: Allow i Deny.</span><span class="sxs-lookup"><span data-stu-id="ba233-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba233-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba233-118">-DefaultProfile</span></span>
<span data-ttu-id="ba233-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba233-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba233-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="ba233-120">-Description</span></span>
<span data-ttu-id="ba233-121">Określa opis konfiguracji reguły zabezpieczeń sieci do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="ba233-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="ba233-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ba233-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="ba233-123">Określa prefiks adresu docelowego.</span><span class="sxs-lookup"><span data-stu-id="ba233-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="ba233-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ba233-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba233-125">Adres międzydomenowy (Classless indomain Routing)</span><span class="sxs-lookup"><span data-stu-id="ba233-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="ba233-126">Zakres docelowego adresu IP</span><span class="sxs-lookup"><span data-stu-id="ba233-126">A destination IP address range</span></span> 
- <span data-ttu-id="ba233-127">Symbol wieloznaczny (\*), aby dopasować dowolny adres IP, za pomocą których można korzystać ze znaczników, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="ba233-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="ba233-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ba233-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="ba233-129">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe dla reguły.</span><span class="sxs-lookup"><span data-stu-id="ba233-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="ba233-130">Nie można go użyć z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="ba233-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="ba233-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ba233-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="ba233-132">Grupa zabezpieczeń aplikacji ustawiona jako miejsce docelowe dla reguły.</span><span class="sxs-lookup"><span data-stu-id="ba233-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="ba233-133">Nie można go użyć z parametrem "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="ba233-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="ba233-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="ba233-134">-DestinationPortRange</span></span>
<span data-ttu-id="ba233-135">Określa port docelowy lub zakres.</span><span class="sxs-lookup"><span data-stu-id="ba233-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="ba233-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ba233-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba233-137">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="ba233-137">An integer</span></span>
- <span data-ttu-id="ba233-138">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="ba233-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="ba233-139">Znak wieloznaczny (\*), aby dopasować port</span><span class="sxs-lookup"><span data-stu-id="ba233-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="ba233-140">-Direction</span><span class="sxs-lookup"><span data-stu-id="ba233-140">-Direction</span></span>
<span data-ttu-id="ba233-141">Określa, czy reguła jest obliczana na ruch przychodzący lub wychodzący.</span><span class="sxs-lookup"><span data-stu-id="ba233-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="ba233-142">Dopuszczalne wartości tego parametru to: przychodzące i wychodzące.</span><span class="sxs-lookup"><span data-stu-id="ba233-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba233-143">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ba233-143">-Name</span></span>
<span data-ttu-id="ba233-144">Określa nazwę konfiguracji reguł zabezpieczeń sieci, którą to polecenie cmdlet tworzy.</span><span class="sxs-lookup"><span data-stu-id="ba233-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ba233-145">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="ba233-145">-Priority</span></span>
<span data-ttu-id="ba233-146">Określa priorytet konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="ba233-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="ba233-147">Dopuszczalne wartości tego parametru to: liczba całkowita między 100 a 4096.</span><span class="sxs-lookup"><span data-stu-id="ba233-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="ba233-148">Numer priorytetu musi być unikatowy dla każdej reguły w kolekcji.</span><span class="sxs-lookup"><span data-stu-id="ba233-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="ba233-149">Niższy numer priorytetu, wyższy priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="ba233-149">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="ba233-150">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="ba233-150">-Protocol</span></span>
<span data-ttu-id="ba233-151">Określa protokół sieciowy, którego dotyczy Nowa konfiguracja reguły.</span><span class="sxs-lookup"><span data-stu-id="ba233-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="ba233-152">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ba233-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba233-153">Protokoł</span><span class="sxs-lookup"><span data-stu-id="ba233-153">Tcp</span></span>
- <span data-ttu-id="ba233-154">Obsługiwane</span><span class="sxs-lookup"><span data-stu-id="ba233-154">Udp</span></span>
- <span data-ttu-id="ba233-155">Symbol wieloznaczny (\*), aby dopasować oba te znaki.</span><span class="sxs-lookup"><span data-stu-id="ba233-155">wildcard character (\*) to match both.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba233-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ba233-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="ba233-157">Określa prefiks adresu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="ba233-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="ba233-158">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ba233-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba233-159">CIDR</span><span class="sxs-lookup"><span data-stu-id="ba233-159">A CIDR</span></span>
- <span data-ttu-id="ba233-160">Zakres źródłowy adresu IP</span><span class="sxs-lookup"><span data-stu-id="ba233-160">A source IP range</span></span>
- <span data-ttu-id="ba233-161">Znak wieloznaczny (\*), aby dopasować dowolny adres IP.</span><span class="sxs-lookup"><span data-stu-id="ba233-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="ba233-162">Możesz również korzystać ze znaczników, takich jak VirtualNetwork, AzureLoadBalancer i Internet.</span><span class="sxs-lookup"><span data-stu-id="ba233-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="ba233-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ba233-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="ba233-164">Grupa zabezpieczeń aplikacji ustawiona jako źródło dla reguły.</span><span class="sxs-lookup"><span data-stu-id="ba233-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="ba233-165">Nie można go użyć z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="ba233-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="ba233-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ba233-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="ba233-167">Grupa zabezpieczeń aplikacji ustawiona jako źródło dla reguły.</span><span class="sxs-lookup"><span data-stu-id="ba233-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="ba233-168">Nie można go użyć z parametrem "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="ba233-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="ba233-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="ba233-169">-SourcePortRange</span></span>
<span data-ttu-id="ba233-170">Określa port źródłowy lub zakres.</span><span class="sxs-lookup"><span data-stu-id="ba233-170">Specifies the source port or range.</span></span>
<span data-ttu-id="ba233-171">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ba233-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba233-172">Liczba całkowita</span><span class="sxs-lookup"><span data-stu-id="ba233-172">An integer</span></span>
- <span data-ttu-id="ba233-173">Zakres liczb całkowitych z zakresu od 0 do 65535</span><span class="sxs-lookup"><span data-stu-id="ba233-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="ba233-174">Znak wieloznaczny (\*), aby dopasować port</span><span class="sxs-lookup"><span data-stu-id="ba233-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="ba233-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba233-175">CommonParameters</span></span>
<span data-ttu-id="ba233-176">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba233-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba233-177">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba233-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba233-178">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba233-178">INPUTS</span></span>

### <span data-ttu-id="ba233-179">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ba233-179">None</span></span>

## <span data-ttu-id="ba233-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba233-180">OUTPUTS</span></span>

### <span data-ttu-id="ba233-181">Microsoft. Azure. Commands. Network. models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="ba233-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="ba233-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba233-182">NOTES</span></span>

## <span data-ttu-id="ba233-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba233-183">RELATED LINKS</span></span>

[<span data-ttu-id="ba233-184">Dodaj-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba233-184">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ba233-185">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba233-185">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ba233-186">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba233-186">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ba233-187">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba233-187">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


